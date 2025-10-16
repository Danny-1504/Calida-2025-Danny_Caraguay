# Sesión 3 — ISO/IEC 25010
Objetivo: clasificar problemas de MediTurnos con el modelo y escribir requisitos
medibles.
Entregables: Matriz CSV completa + 3–5 hallazgos en este README.
| Caso narrado | Condición | Característica ISO/IEC 25010 | Subcaracterística |
|---------------|------------|------------------------------|-------------------|
| La lista de médicos tarda 5–7 segundos en cargar. | Rendimiento lento | Eficiencia del rendimiento | Comportamiento temporal |
| Al fallar el login muestra “error 401” (no explica qué hacer). | Señalamiento de error sin recomendación de qué hacer | Usabilidad | Protección frente a errores |
| Si cierras la pestaña en un computador compartido, el siguiente usuario queda logueado. | Sesión permanece abierta / acceso indebido | Seguridad | Confidencialidad |
| Si el navegador se actualiza durante la reserva, se pierde el turno. | Pérdida de datos por actualización | Fiabilidad | Tolerancia a fallos |
| Exportar a calendario funciona con Google, pero falla en Outlook. | Incompatibilidad con otras plataformas | Compatibilidad | Interoperabilidad |
| En tablets el formulario se descuadra y el botón Confirmar queda oculto. | Problema de visualización en distintos dispositivos | Usabilidad | Estética de la UI |
| El botón Cancelar turno está muy cerca de Confirmar (hay errores por clic). | Diseño provoca acciones erróneas | Usabilidad | Protección frente a errores |
| El sistema permite reservar dos turnos solapados para el mismo paciente. | Falta de validación de reglas / doble reserva | Adecuación funcional | Corrección funcional |

HALLAZGOS

1. El sistema presenta **problemas críticos de rendimiento y seguridad**, especialmente en la carga del listado de médicos y el cierre automático de sesión.
2. Se detectaron **fallos de usabilidad**, como mensajes de error poco claros y botones mal ubicados que provocan errores del usuario.
3. La **interoperabilidad** con plataformas externas (Outlook Calendar) no está completamente implementada, lo que afecta la compatibilidad.
4. La aplicación **no conserva el estado** al actualizar la página, lo que impacta la fiabilidad y genera pérdida de datos.
5. Se requiere implementar **validaciones funcionales adicionales** para evitar turnos solapados, mejorando la corrección funcional del sistema.

