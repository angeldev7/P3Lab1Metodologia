Validación de Historias de Usuario - Criterio INVEST

¿Qué es INVEST?

INVEST es un acrónimo que ayuda a recordar las características de una buena historia de usuario:

- Independent (Independiente)
- Negotiable (Negociable)
- Valuable (Valiosa)
- Estimable (Estimable)
- Small (Pequeña)
- Testable (Testeable)


Validación INVEST para nuestras Historias

HU-001: Agendar Cita

Independent: SI - No depende de otras historias para ser implementada
Negotiable: SI - La forma de agendar puede negociarse con stakeholders
Valuable: SI - Aporta valor directo al usuario principal del sistema
Estimable: SI - Se puede estimar en 8 story points
Small: SI - Puede completarse en un sprint
Testable: SI - Se puede verificar el agendamiento exitoso

Resultado: CUMPLE INVEST


HU-002: Ver Disponibilidad

Independent: NO - Depende de HU-007 (Gestionar Horarios)
Negotiable: SI - Formato de visualización es negociable
Valuable: SI - Esencial para que los usuarios puedan agendar
Estimable: SI - Se puede estimar en 5 story points
Small: SI - Funcionalidad acotada
Testable: SI - Se puede verificar que muestre horarios correctos

Resultado: REVISAR - Mejorar independencia

Acción correctiva: Reformular para que sea más independiente o aceptar la dependencia natural.


HU-005: Reprogramar Cita

Independent: NO - Requiere HU-001 (Agendar Cita) y HU-004 (Cancelar Cita)
Negotiable: SI - Proceso de reprogramación puede ajustarse
Valuable: SI - Funcionalidad importante para flexibilidad del usuario
Estimable: SI - Estimada en 8 story points
Small: REVISION - Podría dividirse en cancelar + agendar nueva
Testable: SI - Se puede verificar reprogramación exitosa

Resultado: REVISAR - Considerar división

Acción correctiva: Dividir en: "Cancelar cita existente" y "Agendar nueva cita"


HU-011: Generar Reportes

Independent: NO - Requiere datos de citas existentes
Negotiable: SI - Tipo de reportes es negociable
Valuable: SI - Aporta valor para decisiones administrativas
Estimable: REVISION - 8 story points podría ser muy grande
Small: REVISION - Historia podría ser grande para un sprint
Testable: SI - Se puede verificar generación de reportes

Resultado: REVISAR - Confirmar tamaño

Acción correctiva: Validar si puede completarse en un sprint o dividir por tipo de reporte.


Resumen de Validación INVEST

Historia          Cumple INVEST    Acciones Requeridas
HU-001           SI               Ninguna
HU-002           REVISAR          Revisar dependencia
HU-003           SI               Ninguna
HU-004           SI               Ninguna
HU-005           REVISAR          Considerar división
HU-006           SI               Ninguna
HU-007           SI               Ninguna
HU-008           SI               Ninguna
HU-009           SI               Ninguna
HU-010           SI               Ninguna
HU-011           REVISAR          Confirmar tamaño
HU-012           SI               Ninguna

Estadísticas:
- Historias que cumplen INVEST: 9/12 (75%)
- Historias que requieren revisión: 3/12 (25%)
- Historias que no cumplen: 0/12 (0%)