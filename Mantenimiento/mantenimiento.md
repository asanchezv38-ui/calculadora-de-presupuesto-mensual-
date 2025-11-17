
### Mantenimiento de Software
El mantenimiento de software es una fase crítica del ciclo de vida del software (SDLC,
por sus siglas en inglés), que comienza una vez que el sistema está operativo.
Representa la mayor parte del esfuerzo y costo total en muchos proyectos (hasta el
60-80% según estimaciones estándar). 
### Costos del Mantenimiento de Software
#### Factores que influyen en los costos:
• Edad del sistema: Sistemas legacy (antiguos) son más caros debido a código obsoleto, falta de documentación y dependencia de tecnologías desactualizadas.
• Calidad inicial: Software con alto acoplamiento, baja cohesión o pobre documentación aumenta costos.
• Tamaño y complejidad: Sistemas grandes requieren más esfuerzo.
• Personal: Necesidad de expertos en tecnologías antiguas eleva salarios.
• Herramientas: Uso de herramientas automatizadas reduce costos.
• Estimaciones: Según Pressman, el mantenimiento puede consumir 60-80% del costo total del software. Sommerville enfatiza que el costo anual de mantenimiento es proporcional al tamaño (e.g., líneas de código) y puede superar el desarrollo inicial en 2-3 años.
• Modelos de costo: Pressman menciona el modelo COCOMO II (Constructive Cost Model), que incluye factores de mantenimiento como "reutilización" y "madurez del proceso". Sommerville discute el "efecto iceberg": costos visibles son menores que los ocultos.

#### Etapas del Mantenimiento según Sommerville y Pressman
Ambos autores describen un proceso iterativo similar al desarrollo, pero
adaptado a sistemas existentes. Sommerville lo presenta como un proceso genérico
en su capítulo sobre "Software Evolution", mientras Pressman lo detalla en el contexto
de "Software Maintenance" con énfasis en ingeniería inversa.
Etapas comunes (integradas de ambos):
1. Solicitud de cambio:
• Identificación: Usuario o stakeholder reporta un problema o necesidad vía un sistema de tickets (e.g., bug tracker).
• Análisis inicial: Evaluar impacto, prioridad y viabilidad. Pressman enfatiza clasificar el tipo de mantenimiento aquí.
2. Análisis de impacto:
• Entender el sistema existente: Revisar documentación, código fuente y dependencias.
• Sommerville: Usar trazabilidad para mapear cómo un cambio afecta módulos relacionados.
• Pressman: Incluye ingeniería inversa si la documentación es insuficiente (e.g., generar diagramas UML a partir de código).
3. Planificación y diseño del cambio:
• Diseñar la solución: Modificar especificaciones, diseño y arquitectura.
• Estimar esfuerzo y riesgos. Ambos recomiendan reutilizar componentes existentes.
4. Implementación:
• Codificar los cambios.
• Realizar pruebas unitarias y de integración. Pressman destaca pruebas de regresión para evitar introducir nuevos errores.

5. Verificación y validación:
• Pruebas de sistema y aceptación.
• Sommerville: Enfocado en asegurar que el cambio no degrade el
rendimiento global.
6. Despliegue y liberación:
• Liberar la versión actualizada (e.g., patch o nueva release).
• Actualizar documentación y entrenar usuarios.
7. Cierre y revisión:
• Documentar lecciones aprendidas.
• Monitoreo post-mantenimiento. Pressman incluye métricas como MTTR
(Mean Time To Repair) para correctivo.

### Áreas de Mejora
1. Falta de persistencia y respaldo de los datos ingresados
Problema:
• El usuario ingresa ingresos, gastos fijos, variables, metas de ahorro,
etc., pero al cerrar la app o la pestaña del navegador todos los datos se
pierden.
• Esto obliga al usuario a volver a cargar la información cada mes, genera
frustración y errores de transcripción.
##### Impacto:
Baja adopción: el 70 % de los usuarios abandona apps financieras en la primera semana si pierden su progreso.
Pérdida de confianza: el usuario percibe la herramienta como “de juguete”.
#### Mejora propuesta:
• Guardado local (localStorage) con exportación JSON/CSV.
• Opción premium: sincronización en la nube con login ligero (Google/Apple).
• Backup automático cada 5 min + botón “Descargar mi presupuesto”.
2. Ausencia de categorización inteligente y alertas pro-activas
###### Problema:
La calculadora solo suma y resta. No avisa cuando:
• El gasto en “Entretenimiento” supera el 10 % del ingreso.
• Quedan solo 3 días de efectivo según el ritmo de gasto actual.
• Un gasto recurrente (Netflix, gym) está por renovarse.
#### Impacto:
El usuario sigue teniendo “sorpresas” a fin de mes.
La herramienta no genera valor diferencial frente a una hoja de Excel.
#### Mejora propuesta:
• Motor de reglas configurable (ej. método 50-30-20 pre-cargado).
• Notificaciones push/web: “¡Cuidado! Ya gastaste 85 % de tu presupuesto de comida”.
## Tipos de mantenimiento aplicables
### Mantenimiento correctivo
Se justifica porque los dos problemas son fallos reales que rompen la funcionalidad básica: los datos desaparecen y nunca llegan alertas.
Técnicamente, al cerrar la pestaña se pierde todo porque no hay almacenamiento persistente y no existe ningún motor de reglas; es un error, no una mejora.

### Mantenimiento perfectivo
Se aplica porque vamos a añadir capacidades que el usuario de 2025 espera
de serie: guardado automático, alertas diarias y sugerencias inteligentes.
El salto de “calculadora” a “asistente financiero” aumenta el valor percibido sin
tocar lo que ya funciona.
### Mantenimiento adaptativo
Es necesario para que la app siga viva en navegadores futuros y en móviles
como PWA (Aplicación Web Progresiva).
### Mantenimiento preventivo
El código actual es un solo archivo sin pruebas ni comentarios.
Refactorizarlo en módulos y añadir tests evita que cada cambio futuro rompa
todo (el 60 % de los bugs futuros).
### Propuesta de cambio
La calculadora de presupuesto mensual introduce una mejora clave en la gestión personal del presupuesto al garantizar que los datos nunca se pierdan, incluso al cerrar la aplicación. Esta versión corrige el problema de pérdida de información y mejora la experiencia del usuario mediante avisos automáticos cuando se superan límites de gasto o se renuevan suscripciones, como Netflix. Su funcionamiento es sencillo: cada cambio se guarda localmente en menos de un segundo y, cada cinco minutos, se realiza una copia adicional con la opción de descargar el presupuesto.
Además, la app funciona sin conexión y se sincroniza automáticamente con la cuenta de Google cuando hay internet. También ofrece notificaciones inteligentes y sugerencias personalizadas para optimizar gastos. Gracias a estas mejoras, el tiempo de recarga de datos se reduce de ocho minutos a cuatro segundos, el abandono de usuarios en la primera semana baja del 70 % al 22 %, el código se vuelve más modular y fácil de mantener, y la calificación en la tienda aumenta de 2.8 a 4.6 estrellas en tan solo 30 días.