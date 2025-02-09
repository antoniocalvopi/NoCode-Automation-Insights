# JuanMecánico: Un Bot de Telegram para Automatización Automovilística

## Introducción
A continuación voy a mostrar un ejemplo más complejo de como se puede usar las automatizaciones para crear una "herramienta" atractiva y divertida. En este caso se trata de usar un bot de Telegram que anteriormente hemos creado llamado JuanMecánico, diseñado para facilitar diversas tareas relacionadas con el automovilismo. Este bot permite a los usuarios acceder a información, recibir noticias, realizar consultas y más, todo de manera automatizada.

## Objetivo
El propósito de esta automatización es demostrar un escenario complejo en Make donde múltiples flujos de trabajo se combinan en un solo sistema controlado a través de un bot de Telegram. Los usuarios podrán interactuar con el bot para obtener datos, recibir notificaciones y gestionar diversas acciones relacionadas con el mundo automovilístico.


## 1. Funcionalidades Principales
A través de JuanMecánico, los usuarios podrán:

### 📢 **Noticias Automovilísticas Personalizadas**
- El bot obtiene cada hora las últimas noticias sobre automovilismo (rally,clubs JDM, Fórmula 1, etc.) de una API de noticias.
- Resumen de cada noticia generado con GPT-4, otro modelo o a "pelo".
- Almacenamiento de las noticias en Airtable.
- Opción para que el usuario reciba un resumen diario o instantáneo de las noticias en su chat de Telegram.

> **Nota**: debido al problema encontrado al usar la api de gpt 4 en el ejemplo de [IA news for content creators](/examples/simple-automation/AutomatedAInewsforcontentcreators.md) es posible que el resumen de las noticias sean el propio de la api o se usará un modelo de IA autohosteado (por lo tanto sin limite de uso, bueno limite de hardware).

### ⚙️ **Consulta de Especificaciones de Vehículos**
- Los usuarios pueden escribir el nombre de un modelo de coche y recibir especificaciones técnicas detalladas.
- Integración con una API de datos de automóviles para obtener información como potencia, consumo, peso, etc.

### ⏰ **Recordatorios de Mantenimiento**
- Los usuarios pueden registrar sus vehículos en el bot.
- El sistema enviará recordatorios para cambios de aceite, revisiones y mantenimiento según el kilometraje estimado.
- Opción de recibir consejos de mantenimiento preventivo.

### 🔧 **Asistencia Mecánica Rápida**
- Si el usuario tiene un problema mecánico, el bot ofrecerá una lista de problemas comunes y posibles soluciones.
- Posibilidad de conectar con un mecánico en línea si el problema requiere asistencia avanzada.

## 2. Arquitectura de la Automatización
Cada funcionalidad está estructurada en flujos de trabajo dentro de Make, conectando diferentes módulos de manera eficiente.

### **Triggers y Actions:**

#### 🏁 **Trigger Principal: Interacción en Telegram**
- **Trigger:** `Watch Updates (Telegram Bot)` - Captura mensajes de los usuarios y los analiza para determinar la acción a realizar.
- **Acción:** Analiza el comando del usuario y ejecuta el flujo correspondiente.

#### 📰 **Noticias Automovilísticas**
- **Trigger:** `Scheduler (cada hora)`
- **Acción 1:** Obtener noticias de la API de automovilismo.
- **Acción 2:** Pasar cada noticia por GPT-4 para generar un resumen atractivo.
- **Acción 3:** Guardar los resúmenes en Airtable.
- **Acción 4:** Enviar noticias a usuarios suscritos a través de Telegram.

#### 🚘 **Consulta de Especificaciones de Vehículos**
- **Trigger:** Mensaje en Telegram con el nombre del coche.
- **Acción 1:** Consultar API de especificaciones de vehículos.
- **Acción 2:** Formatear la respuesta y enviarla al usuario.

#### 🛠️ **Asistencia Mecánica**
- **Trigger:** Mensaje con un problema mecánico (ejemplo: "Mi coche hace un ruido extraño").
- **Acción 1:** Analizar el mensaje con IA para clasificar el problema. (caso ideal, se emplearán filtros con palabras clave)
- **Acción 2:** Enviar sugerencias de solución o derivar a un mecánico online.
## 3. Integraciones Utilizadas
| Integración | Uso |
|------------|-----|
| **Telegram Bot** | Comunicación con los usuarios |
| **NewsAPI** | Obtención de noticias |
| **OpenAI GPT-4 o deepseekr1-13b local** | Generación de resúmenes y asistencia IA |
| **Airtable** | Almacenamiento de datos |
| **Google Sheets** | Registro de historial de usuarios |
| **API de Vehículos** | Consulta de especificaciones |

## 4. Mejoras Futuras
- 📍 **Localización de talleres cercanos** con Google Maps API.
- 📊 **Comparación de modelos de autos** basada en datos técnicos.
- 🔗 **Publicación automática de noticias** en redes sociales (Twitter, Facebook).
- 🤖 **Asistente de voz** para consultas interactivas dentro de Telegram.

## Conclusión
Este escenario de automatización demuestra cómo se pueden combinar múltiples procesos dentro de Make para crear un sistema robusto y altamente interactivo sin conocimientos técnicos. JuanMecánico es un bot potente que centraliza información y asistencia automovilística en un solo canal de comunicación, mostrando el potencial de la automatización avanzada en Telegram.

## Capturas

