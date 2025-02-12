# NoCode Automation Insights - Explorando la Automatización con Make
[![Instalar](https://img.shields.io/badge/Instalar-Click_Here-blue)](/docs/)
[![Star](https://img.shields.io/github/stars/usuario/repositorio?style=social)](https://github.com/antoniocalvopi/NoCode-Automation-Insights)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## Tabla de Contenidos
- [Descripción](#descripción)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Instalación](#instalación)
- [Casos de Uso](#casos-de-uso)
- [Buenas Prácticas en Automatización](#buenas-prácticas-en-automatización)
- [Análisis de Mercado](#análisis-de-mercado)
- [Opiniones y Crítica](#conclusión-y-crítica)
- [FAQ](#faq---preguntas-frecuentes)
- [Créditos](#créditos)

## Descripción

Es este repositorio se explora el potencial de la automatización sin código utilizando la plataforma Make. Además de crear ejemplos prácticos de automatizaciones, también se analiza el mercado actual, mejores prácticas, patrones de diseño aplicados a la automatización y una guía detallada para crear nuestro primer flujo automatizado.

Este proyecto forma parte de la asignatura **Plataformas, Frameworks y Tendencias Tecnológicas (PFTT)**.


## Estructura del Proyecto

```plaintext
📂 NoCode-Automation-Insights/
├── 📜 README.md               # Explicación general del proyecto
├── 📂 docs/                   # Documentación general
│   ├── 📝 estudio-mercado.md  # Análisis del mercado de automatización
│   ├── 📝 buenas-practicas.md # Mejores prácticas en automatización
│   ├── 📝 bibliografía.md     # Fuentes y referencias
│   ├── 📝 instalacionMake.md     # Instalación y acceso a Make
│   ├── 📝 manual-usuarioMake.md      # Manual de uso detallado
│   ├── 📝 casos-de-uso.md        # Aplicaciones y ejemplos
│   ├── 📝 conclusiones-pros-cons.md  # Análisis crítico
│   ├── 📝 crear_bot_telegram.md  # Instrucciones para crear un bot en telgram (doc adicional para ejemplos)
├── 📂 examples/               # Casos de uso en Make
│   ├── 📂 simple-automation/  # Ejemplos básicos junto con doc + JSON
│   ├── 📂 complex-automation/ # Ejemplo con múltiples integraciones doc + JSON
├── 📸 img/               # Imagenes usadas en la documentación
│   ├── 🛣️ screenshoot.png 
│   ├── ...
├── 📜 CONTRIBUTING.md         # Guía para contribuciones
├── 📜 LICENSE                 # Tipo de licencia
├── 📜 CODE_OF_CONDUCT         # Código de conducta
```

## Instalación

### Requisitos
1. Una cuenta en **Make** (https://www.make.com/)
2. Conexión a internet (más que evidente)

### Pasos de Instalación
Sigue los pasos descritos en la documentación [installation.md](docs/instalacionMake.md) para configurar tu entorno y crear tu helloWorld de automatización noCode.

También puedes explorar los ejemplos realizados en el directorio [`/examples/`](examples/) y prueba a replicarlos en tu cuenta (Puedes importarlos directamente desde Make usando los JSON disponibles).

## Casos de Uso

En la carpeta [`/examples/`](examples/) se encuentran dos tipos de ejemplos de automatizaciones:

- **Simple Automation:** Algunas automatizaciónes básicas para entender los fundamentos de Make.
- **Complex Automation:** Un caso de uso avanzado con múltiples integraciones entre servicios (Creación completa de un bot de telegram).

Para más detalles, consulta la documentación en [use-cases.md](docs/casos-de-uso.md).

O

Puedes explorar los ejemplos disponibles [`/examples/`](examples/).


## Buenas Prácticas en Automatización

El archivo [buenas-practicas.md](docs/buenas-practicas.md) recopila algunos patrones de diseño y estrategias clave para crear automatizaciones eficientes y escalables en Make.

Ejemplos de patrones abordados:
- **Patrón de Orquestación**
- **Patrón de Event-Driven Workflow**
- ...

## Análisis de Mercado

Para comprender el impacto de las herramientas NoCode, se realiza un análisis del mercado de automatización en [estudio-mercado.md](docs/estudio-mercado.md). En este documento se abordan:

- Explicación del concept **NoCode** y su impacto en el desarrollo de software.
- Análisis del crecimiento de estas herramientas en diferentes industrias.
- Proyecciones de crecimiento del mercado y adapción futura.

Se incluyen referencias de estudios como **Global Growth Insights (2024)** y **Expert Market Research**, que proyectan un crecimiento del 8.6% anual en la automatización hasta el año 2024.

Todo la bibliografía consultada se encuentra en [bibliografia.md](docs/bibliografia.md).

## Conclusión y Crítica

El documento [opinion-pros-cons.md](docs/opinion-pros-cons.md) contiene un análisis detallado de las ventajas y desventajas de las plataformas de automatización NoCode.

### **Pros y Beneficios:**
✅ **Aumento de la Productividad:** Reduce tareas repetitivas y permite enfocarse en tareas más importantes.

✅ **Accesibilidad:** Cualquier persona sin conocimientos técnicos puede crear automatizaciones.

✅ **Reducción de Costos:** Disminuye el tiempo y dinero en desarrollo de software.

✅ **Escalabilidad:** Fácil integración con herramientas como Google Sheets, Slack y CRMs.

### **Contras y Limitaciones:**
❌ **Dependencia de Plataformas de Terceros:** Cambios en políticas pueden afectar los flujos de trabajo.

❌ **Falta de Personalización Avanzada:** Algunas necesidades requieren código "tradicional".

❌ **Seguridad y Privacidad:** Riesgos al almacenar datos en servidores externos.

❌ **Pérdida de Control:** Automatizaciones mal diseñadas pueden generar errores críticos. Make permite agregar modulos para controlar los errores. (es decir, como un try-catch)

### **¿Es realmente eficiente automatizar con NoCode?**

- **Para PYMEs y emprendedores:** más que adecuado y eficiente por su accesibilidad y rapidez.
- **Para grandes empresas:** es muy útil pero puede quedarser escaso para sistemas complejos.
- **Para freelancers y usuarios individuales:** es más que adecuado para automatizar tareas repetitivas y ayudar a mejorar la eficiencia en algunos procesos.

### **Conclusión**

Las plataformas NoCode han cambiado la manera en que empresas y usuarios optimizan procesos. Su facilidad de uso y accesibilidad las hacen herramientas muy útiles y eficientes, pero presentan algunos desafíos como la personalización, seguridad y dependencia de terceros. 

## FAQ - Preguntas Frecuentes

1. **¿Necesito saber programación para usar usar Make?**

   No, aunque conocimientos básicos de lógica pueden ser útiles, además de conocimiento de patrones de diseño. En la [bibliografía](docs/bibliografia.md) puedes consultar información sobre los patrones de diseño.

2. **¿Make es gratuito?**

   Tiene un plan gratuito con límites. Consulta la documentación de [instalación](docs/instalacionMake.md) para conocer más sobre la plataforma y como empezar a usarla.

3. **¿Cómo puedo contribuir?**

   Consulta [CONTRIBUTING.md](CONTRIBUTING.md) para colaborar con mejoras, ejemplos o documentación.

4. **¿Puedo usar este proyecto?**

   Sí, revisa la licencia en [LICENSE](LICENSE).

## Créditos

Este proyecto ha sido creado como parte de la asignatura **Plataformas Frameworks y Tendencias Tecnológicas (PFTT)**.

- **Herramientas utilizadas:**
  - Make para la automatización.
  - Markdown para documentación.
  - GitHub para control de versiones de la doc y respaldo del proyecto.

Si encuentras este proyecto útil, considera dejar una ⭐ en el repositorio.

👉 [Deja tu estrella aquí](https://github.com/antoniocalvopi/NoCode-Automation-Insights) 🚀

