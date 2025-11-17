# calculadora-de-presupuesto-mensual-[#README.md](https://github.com/user-attachments/files/23572664/README.md)
#README
Caso 3: Calculadora de Presupuesto Mensual
#### Descripción del Caso
La Calculadora de Presupuesto Mensual es una aplicación diseñada para facilitar la gestión y el control de las finanzas personales. Permite a los usuarios registrar sus ingresos y gastos, calcular el balance mensual, y gestionar sus datos de manera eficiente.

#### Problemática Identificada
El sistema resuelve la necesidad de tener un control financiero preciso y centralizado, eliminando los riesgos asociados a los métodos manuales:

Cálculo manual propenso a errores: La gestión en papel o en hojas de cálculo básicas es propensa a errores matemáticos en el balance final (RF3).

Falta de análisis de tendencia: Sin el historial básico (RF4), el usuario carece de visibilidad sobre sus patrones de gasto a largo plazo.

Riesgo de seguridad de datos: La información financiera personal sin autenticación (RNF3) corre un riesgo de exposición.

#### Objetivos
Objetivo General
Proporcionar una herramienta para el control financiero personal, facilitando el registro, procesamiento y gestión de transacciones para garantizar la precisión, reducir errores de cálculo y mejorar la experiencia del usuario.

Objetivos Específicos
1. Automatizar el proceso de cálculo del balance (RF3).

2. Mejorar la planificación presupuestaria del usuario a través de datos históricos (RF4).

3. Garantizar la integridad y protección de los datos financieros (RF5 y RNF3).

4. Ofrecer una experiencia intuitiva (RNF1) para el registro diario de transacciones.

#### Requerimientos del Sistema
Requerimientos Funcionales (RFs)
RF1: Registro de Ingresos: Permitir registrar nuevas fuentes de ingresos, con monto y descripción.

RF2: Registro de Gastos: Permitir registrar nuevos gastos, incluyendo monto, descripción y categoría (e.g., comida, transporte).

RF3: Cálculo Automático: Calcular el balance mensual como Ingresos Totales - Gastos Totales.

RF4: Historial Básico: Permitir visualizar los totales de ingresos y gastos para meses anteriores.

RF5: Edición/Eliminación: Permitir al usuario modificar o eliminar cualquier registro de ingreso o gasto ya ingresado.

Requerimientos No Funcionales (RNFs)
RNF1: Usabilidad (Intuitivo): Interfaz simple que permita completar el registro de una transacción en un máximo de 3 pasos o clics.

RNF2: Rendimiento: Responder a solicitudes de cálculo y visualización del balance en menos de 2 segundos.

RNF3: Seguridad: Requerir autenticación (inicio de sesión) para acceder a los datos de presupuesto.

#### Tabla de Pruebas
El proceso de pruebas es el paso fundamental para la validación del software, verificando la precisión y la calidad del sistema.

Pruebas Unitarias (TU)

TU-01 (RF3: Cálculo Automático): Datos de Entrada: Ingreso ($1000), Gastos ($400 y $100). Resultado Esperado: Total: $500.00.

TU-02 (RF2: Validación de Datos): Datos de Entrada: Cantidad: "Texto no numérico". Resultado Esperado: Error: "El monto debe ser numérico".

TU-03 (RF5: Edición/Eliminación): Datos de Entrada: Eliminar un gasto de $50. Resultado Esperado: El registro se elimina y el balance se incrementa en $50.

Pruebas de Validación (TV)
TV-01 (RNF2: Rendimiento): Datos de Entrada: Calcular el balance con 50 registros de ingresos y gastos. Resultado Esperado: Completar en ≤2 segundos.

TV-02 (RNF3: Seguridad): Datos de Entrada: Intento de acceder a la sección de presupuesto sin iniciar sesión. Resultado Esperado: Redirección automática a la página de login.

Tipo de Mantenimiento Propuesto
Mantenimiento Perfectivo
Este mantenimiento es el más relevante, enfocado en la mejora continua de la funcionalidad para el análisis financiero.

Informes Visuales: Añadir gráficos que muestren la distribución de gastos por categoría. Impacto: Elimina la incertidumbre del usuario sobre dónde gasta más dinero.

Alertas de Presupuesto: Notificaciones PUSH o in-app cuando el usuario se acerque al límite de gasto definido para una categoría. Impacto: Mejora el control proactivo.

Métodos de Exportación: Añadir funcionalidad para exportar el historial de transacciones a CSV/Excel. Impacto: Incrementa la conveniencia para análisis externos.

#### Mantenimiento Correctivo
Este mantenimiento se enfoca en solucionar defectos críticos en la lógica del sistema.

Objetivo: Corregir defectos en la lógica de negocio.

Problema Crítico: Error persistente en la fórmula de RF3 que causa que el balance sea incorrecto.

Impacto: Pérdida de integridad de datos y nulifica el objetivo principal de la calculadora.

#### Reflexión sobre Control de Versiones
Importancia en el Desarrollo
El control de versiones es fundamental para el mantenimiento eficiente del software, ya que permite la trazabilidad completa y la gestión segura de la lógica financiera.

Beneficios Implementados
Trazabilidad completa de todos los cambios realizados en el código de cálculo.

Rollback seguro en caso de implementaciones que comprometan la seguridad (RNF3) o la precisión (RF3).

Documentación automática del historial de desarrollo.

Lecciones Aprendidas
Mensajes descriptivos son esenciales para el mantenimiento a largo plazo.

Code reviews sistemáticos son necesarios para asegurar la calidad de la lógica matemática.

Tags semánticos (e.g., v1.0.0) agilizan el proceso de liberación de versiones estables.

El uso adecuado reduce significativamente los costos al facilitar la identificación de cambios problemáticos.
