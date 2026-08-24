# Diagnóstico de cobertura: huérfanos, cadenas rotas y trazas parciales

| Identificador | Patología | Causa | Acción tomada |
|---|---|---|---|
| Clases `Administrator`, `Role`, `UserRole` | Cadena rota | Se modeló un subsistema completo de administración y gestión de roles (Diagrama de clases, partición Usuarios y Roles) sin que ningún RF lo especifique; "administrador" solo aparece como ejemplo genérico en el glosario del ERS. | **Resuelto.** Clases eliminadas del diagrama de clases (partición Usuarios y Roles). Se corrigió además RD-02, que aún mencionaba "administradores" en su descripción y en las tablas resumen. El control de acceso por tipo de usuario queda cubierto por la herencia `Shelter`/`Owner`/`Veterinarian` → `User`. |
| Clase `VeterinaryAppointment` | Cadena rota | Se modeló la gestión de citas veterinarias (agendar/cancelar), en la partición Mascotas y Salud, sin que exista RF ni CU correspondiente; contradice además dos exclusiones de alcance ya declaradas en el ERS ("no reemplaza consulta veterinaria", "no ofrece agenda médica completa"). | **Resuelto.** Eliminada de la partición Mascotas y Salud. RF-10 (recordatorios pasivos) queda diferenciado de la reserva activa de turnos, que sigue fuera de alcance. |
| RF-11 (Administrar privacidad) | Traza parcial | Tenía CU-06, HU-08 y CA-08, pero ninguna clase propia en el diagrama de clases; las secuencias de CU-06 mencionan `PrivacySettingsRepository`, nunca modelada. | **Resuelto.** Se agregó la clase `PrivacySettings` (composición 1:1 con `Pet`), con los atributos y métodos usados en las secuencias de CU-06/CU-10. |
| RF-20 (Coordinar encuentros de socialización supervisados) | Traza parcial (hallazgo adicional, no detectado en la primera revisión) | Tiene CU-08, pero ninguna clase propia; su propia postcondición menciona un "historial de interacciones" que nunca se modeló. | **Resuelto.** Se agregó la clase `Interaction`, asociada a `Pet` (0..* en ambos extremos), que registra el encuentro coordinado vía CU-08. |
| RF-23 (Alertas de riesgo sanitario o físico) | Traza parcial | Tenía CU-06, HU-15 y CA-15, pero ninguna clase propia. | **Resuelto.** Se agregó el método `checkRiskAlert(): string`, compartido entre `Interaction` y `BreedingRequest`, ya que la alerta es una validación transitoria (no persistida) evaluada antes de confirmar la interacción o solicitud. |

## Nota sobre huérfanos

No se agrega ninguna fila de este tipo porque los 43 elementos (27 RF + 16 RNF) cuentan con fuente (código de participante o derivación del equipo) y al menos un CU o designación transversal. **Cero requisitos huérfanos detectados.**

## Diagnóstico global

De 43 elementos evaluados, se identificaron inicialmente 0 huérfanos, 2 cadenas rotas y 2 trazas parciales; en el proceso de corrección se detectó una tercera traza parcial (RF-20) no capturada en la revisión inicial.

Las 5 patologías identificadas quedaron resueltas mediante:
- 2 eliminaciones de clases sin respaldo (`Administrator`/`Role`/`UserRole`, `VeterinaryAppointment`)
- 2 incorporaciones al diagrama de clases (`PrivacySettings`, `Interaction`)
- 1 método compartido (`checkRiskAlert()`)

El diagnóstico de cobertura del ERS de MundiPets cierra **sin patologías pendientes**.
