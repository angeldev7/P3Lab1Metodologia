Definition of Ready (DoR) - Sistema de Gestión de Citas en Línea

¿Qué es Definition of Ready?

La Definition of Ready (DoR) es un conjunto de criterios que debe cumplir una historia de usuario antes de ser incluida en un sprint. Asegura que el equipo de desarrollo tenga toda la información necesaria para implementar la funcionalidad.


Criterios de Definition of Ready

1. Criterios de Negocio
- Historia de usuario claramente definida con formato "Como... Quiero... Para que..."
- Criterios de aceptación específicos y medibles
- Valor de negocio identificado y justificado
- Prioridad asignada por Product Owner
- Dependencias identificadas y documentadas

2. Criterios Técnicos
- Estimación realizada por el equipo de desarrollo
- Definición de Hecho (DoD) clara para la historia
- Riesgos técnicos identificados y mitigados
- Arquitectura/diseño básico definido
- APIs o interfaces necesarias documentadas

3. Criterios de Calidad
- Casos de prueba principales identificados
- Criterios de rendimiento definidos (si aplica)
- Criterios de seguridad identificados (si aplica)
- Criterios de usabilidad establecidos

4. Criterios de Entendimiento
- Equipo de desarrollo comprende completamente la historia
- Dudas y ambigüedades resueltas
- Mockups o wireframes disponibles (si es necesario)
- Datos de prueba identificados


Aplicación de DoR a Historias Prioritarias

HU-001: Agendar Cita

Criterios de Negocio
- Historia bien definida: Como usuario, quiero agendar una cita para ser atendido
- Criterios de aceptación definidos (ver abajo)
- Valor: Funcionalidad core del sistema de citas
- Prioridad: Alta
- Dependencias: HU-002 (Ver Disponibilidad), HU-008 (Gestionar usuarios)

Criterios de Aceptación
1. El usuario debe poder seleccionar fecha y hora disponible
2. El sistema debe mostrar solo horarios disponibles
3. El usuario debe poder seleccionar tipo de cita
4. Se debe generar número de confirmación único
5. Se debe enviar confirmación por email
6. La cita debe aparecer en el historial del usuario

Criterios Técnicos
- Estimación: 8 story points
- DoD: Código implementado, pruebas unitarias, integración con calendario
- Riesgos: Concurrencia en agendamiento, validación de disponibilidad
- Diseño: API REST, base de datos citas, sistema de notificaciones
- Interfaces: POST /api/appointments, GET /api/availability

Criterios de Calidad
- Casos de prueba: Agendamiento exitoso, horario ocupado, datos inválidos
- Rendimiento: menor a 3 segundos para confirmar cita
- Seguridad: Solo usuarios autenticados, validación de datos
- Usabilidad: Calendario intuitivo, confirmaciones claras

Criterios de Entendimiento
- Equipo comprende: Proceso de agendamiento clarificado
- Dudas resueltas: Tipos de cita disponibles
- Mockups: Flujo completo de agendamiento disponible
- Datos de prueba: Horarios disponibles, tipos de cita

Resultado DoR: READY


HU-007: Gestionar Horarios

Criterios de Negocio
- Historia bien definida: Como personal de atención, quiero gestionar mis horarios para definir disponibilidad
- Criterios de aceptación definidos
- Valor: Esencial para que los usuarios puedan agendar citas
- Prioridad: Alta
- Dependencias: HU-008 (Gestionar usuarios)

Criterios de Aceptación
1. Personal puede crear bloques de horarios disponibles
2. Personal puede modificar horarios existentes
3. Personal puede eliminar horarios (si no tienen citas agendadas)
4. Sistema valida que no se superpongan horarios
5. Los horarios están disponibles inmediatamente para agendamiento
6. Se notifica a usuarios con citas pendientes si hay cambios

Criterios Técnicos
- Estimación: 8 story points
- DoD: CRUD completo, validaciones, notificaciones automáticas
- Riesgos: Validación de superposición, manejo de cambios con citas existentes
- Diseño: API de horarios, validador de conflictos
- Interfaces: GET/POST/PUT/DELETE /api/schedules

Criterios de Calidad
- Casos de prueba: CRUD exitoso, validaciones de superposición, cambios con citas
- Rendimiento: menor a 2 segundos para operaciones
- Seguridad: Solo personal autorizado puede modificar sus horarios
- Usabilidad: Interfaz tipo calendario, validaciones en tiempo real

Criterios de Entendimiento
- Equipo comprende: Lógica de validación de horarios
- Dudas resueltas: Manejo de cambios con citas existentes
- Mockups: Interfaz de gestión de horarios disponible
- Datos de prueba: Horarios de ejemplo, escenarios de conflicto

Resultado DoR: READY


HU-011: Generar Reportes

Criterios de Negocio
- Historia bien definida: Como administrador, quiero generar reportes para analizar uso del sistema
- Criterios de aceptación definidos
- Valor: Información para toma de decisiones administrativas
- Prioridad: Media
- Dependencias: Todas las historias de gestión de datos

Criterios de Aceptación
1. Administrador puede generar reporte de citas por período
2. Administrador puede generar reporte de usuarios más activos
3. Administrador puede generar reporte de horarios más solicitados
4. Reportes se pueden exportar en PDF y Excel
5. Reportes incluyen gráficos básicos
6. Sistema permite filtrar por fechas y tipos

Criterios Técnicos
- Estimación: 13 story points
- DoD: Módulo de reportes, exportación, gráficos básicos
- Riesgos: Rendimiento con grandes volúmenes de datos
- Diseño: Motor de reportes, API de estadísticas
- Interfaces: GET /api/reports/*

Criterios de Calidad
- Casos de prueba: Generación exitosa, filtros, exportación
- Rendimiento: menor a 10 segundos para reportes complejos
- Seguridad: Solo administradores, datos anonimizados si es necesario
- Usabilidad: Interfaz de configuración de reportes simple

Criterios de Entendimiento
- Equipo comprende: Tipos de reportes requeridos
- Dudas resueltas: Formatos de exportación necesarios
- Mockups: Interfaz de generación de reportes pendiente
- Datos de prueba: Base de datos con volumen representativo

Resultado DoR: REVIEW - Requiere mockups y refinamiento de estimación


CheckList DoR por Historia

Historia     Negocio   Técnico   Calidad   Entendimiento   Estado
HU-001       SI        SI        SI        SI              READY
HU-002       SI        SI        SI        SI              READY
HU-003       SI        SI        SI        SI              READY
HU-004       SI        SI        SI        SI              READY
HU-005       SI        REVISAR   SI        SI              REVIEW
HU-006       SI        SI        SI        SI              READY
HU-007       SI        SI        SI        SI              READY
HU-008       SI        SI        SI        SI              READY
HU-009       SI        SI        SI        SI              READY
HU-010       SI        SI        SI        REVISAR         REVIEW
HU-011       SI        REVISAR   SI        REVISAR         REVIEW
HU-012       SI        SI        SI        SI              READY

Estadísticas DoR:
- Historias READY: 9/12 (75%)
- Historias en REVIEW: 3/12 (25%)
- Historias NOT READY: 0/12 (0%)