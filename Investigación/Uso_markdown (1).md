
## ¿Qué es Markdown?
Markdown es un lenguaje de marcado ligero creado con el objetivo de lograr la máxima legibilidad en su forma de código fuente. Permite escribir usando un formato de texto plano simple que luego puede ser convertido a HTML u otros formatos. Se caracteriza por usar símbolos como asteriscos (*), guiones (-) o almohadillas (#) para aplicar formato.

Por qué se utiliza en proyectos de software
Markdown es el lenguaje estándar para la documentación en proyectos de software por las siguientes razones:

Simplicidad y Rapidez: Permite a los desarrolladores escribir documentación rápidamente sin interrumpir su flujo de trabajo, ya que es texto plano fácil de teclear.

Control de Versiones: Los archivos Markdown (.md o .tmd) son archivos de texto plano que funcionan perfectamente con sistemas de control de versiones como Git, facilitando la trazabilidad de los cambios en la documentación.

Legibilidad: El código fuente (el archivo .md) es legible por humanos, incluso antes de ser renderizado a HTML.

Uso Universal: Es el formato predeterminado para archivos clave del proyecto, como el README (como se ve en la imagen) y la documentación Wiki.

Ejemplo Práctico de Uso de Markdown
El siguiente ejemplo muestra cómo se utilizan los elementos básicos de Markdown:

Encabezados
 # Título Principal

Equivale a h1

## Sección Importante

Equivalente a h2

Listas
Código (Lista Desordenada): 
* Elemento Uno, 
  * Elemento Dos

Resultado: Se renderiza con viñetas.

Código (Lista Ordenada): 
1. Primer Paso, 
 2. Segundo Paso

Resultado: Se renderiza con numeración.

Tablas

| Artículo | Cantidad |
 |:---|:---| 
 | Pan | 1 barra |

Resultado: Se crea una tabla con columnas y filas.

### Énfasis
Código (Negrita): **Texto en Negrita**

Resultado: Texto en Negrita

Código (Cursiva): *Texto en Cursiva*

Resultado: Texto en Cursiva

Enlaces

[Enlace a UNEMI](https://www.unemi.edu.ec/)

Resultado: Se crea un hipervínculo que enlaza la URL al texto.

#### Imágenes
 ![Descripción de la imagen](https://images.ctfassets.net/denf86kkcx7r/4IPlg4Qazd4sFRuCUHIJ1T/f6c71da7eec727babcd554d843a528b8/gatocomuneuropeo-97?fm=webp&w=612)

Resultado: Muestra la imagen.

#### Ventajas de utilizar Markdown en combinación con GitHub
GitHub y otras plataformas de alojamiento de repositorios como GitLab o Bitbucket tienen un soporte nativo total para Markdown, lo que ofrece las siguientes ventajas:

Visualización Automática del README.md: GitHub automáticamente detecta y renderiza el archivo README.md en la página principal del repositorio. Esto proporciona a los visitantes una descripción inmediata del proyecto, como su propósito y la problemática que resuelve.

Documentación Colaborativa: Permite a múltiples desarrolladores contribuir y editar la documentación del proyecto con la misma facilidad con la que editan el código, utilizando Pull Requests y revisiones.

Renderizado Consistente: Asegura que la documentación se vea uniforme y profesional directamente en el navegador, sin necesidad de herramientas externas o formato HTML complejo.

Integración con Wikis y Issues: Markdown se utiliza dentro del sistema de gestión de incidencias (Issues) y en las páginas Wiki de GitHub, manteniendo la coherencia del formato en todas las áreas de documentación.