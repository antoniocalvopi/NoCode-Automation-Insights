# Buenas Prácticas al Crear Automatizaciones con Herramientas NoCode

Antes de comenzar a crear automatizaciones con cualquiera de las herramientas disponibles de noCode, es fundamental tener en cuenta ciertas buenas prácticas que nos permitan estructurar de manera eficiente los flujos y creaciones de escenaros (terminología de make, se explica en el manual de uso) para aseguridad la escalabilidad y mantenimiento de las soluciones que creemos. Una de las principales recomendaciones es aplicar patrones de diseño, al igual que se utilizan en el desarrollo de software sostenible se puede aplicar de manera efectiva en la automatización de procesos.

## 1. Event-Driven (Basado en eventos)

Event-Driven se basa en la idea de que un sistema puede reaccionar a eventos o cambios en el estado del sistema. En automatización consistiría en crear flujos de trabajo que respondan automáticamente en función a un evento específicp, por ejemplo, cuando se recibe un correo realizar una acción específica. En la mayoría, por no decir todas, permiten integrar los flujos de trabajo con diversas plataformas para realizar acciones en fución a eventos..etc. 


## 2. Orchestration (Orquestación)

Es un patrón que consiste en la centralización del control de los distintos servicios y procesos que intervienen en una automatización, proceso, proyecto... Es decir, en lugar de que cada componente de un sistema funcione de manera independiente, la orquestación coordina y organiza los distintos procesos de manera que trabajen de forma "orquestada".

En el caso de la automatización, consiste en crear un flujo de trabajo que guíe el orden y la secuencia de las acciones entre distintos servicios o aplicaciones.


## 3. Choreography (Coreografía)

Este patrón permite que cada parte del sistema gestione de forma "independiente" sus procesos. En lugar de depender de un controlador centralizado, como en el caso de la orquestación, las diferentes partes del sistema controlan sus procesos pero se comunican entre ellas en función de si es necesario o no.

En herramientas noCode se pueden utilizar las integraciones con diferentes plataformas para manejar información y eventos y comunicar entre las diferentes "tareas" o partes del sistema automatizado la información que necesiten, un ejemplo muy práctico sería obtener con una api noticias, y con la integración de cahtGpt realizar un resumen de cada una de ellas. Realmente son dos procesos "autónomos" pero requieren estar coordinados para poder completar al 100% su objetivo.


## 4. Batch-Processing (Procesamiento por lotes)

Como bien indica el nombre, consiste en realizar el procesamiento por lotes de operaciones o tareas y estas se procesan de un solo paso. Este patrón es interesante para la importación o exportación de grandes volúmenes de datos, actualización de registros, ejecución de informes.

Un ejemplo con herramientas noCode sería similar al del patrón de coreografía, todas las noticias obtenidas se podrían dividir en lotes para procesarlas de un solo paso, es decir, si tenemos 30 articulos podrías dividirlos en lotes de 10, de esta manera cuando de forma normal se ejecuta solo el resumen con chatGpt de la noticia con procesamiento por lotes podrías obtener 3 noticias resumidas. Este ejemplo es más teórico que prático, ya que se debería conocer los limites de la integración con chatGpt, como la concurrencia a la hora de ejecutar prompts...etc.


## 5. CI/CD (Integración continua y despliegue continuo)

EL patrón CI/CD consiste en integrar y desplegar actualizaciones de "software" continuamente y de forma automatizada. En el contexto de noCode, se puede aplicar para los procesos de pruebas y lanzamiento de nuevas versiones automatizadas, de esta manera podemos aseguridad que cualquier cambio o mejora se publique de forma controlada y sin errores, porque para que esto suceda debemos establecer un tests para evitar que se publiquen de forma automatica errores.

Un ejemplo sencillo sería el uso de actions de github en un entorno de producción, de manera que en cuanto pasen las pruebas se publique de forma automática, e incluso podemos automatizar con herramientas como Make que realice publicaciones en diferentes redes para indicar a sus usuarios o contribuidores los nuevos cambios.

## Conclusión

Aunque estos patrones de muchos otros que existen se suelen aplicar a software, realmente se pueden "convertir" o modificar para implementarlos en automatización noCode, de manera que se pueda crear soluciones más robustas, escalables y fáciles de mantener (o al menos en la teoría). La idea de incorporar este enfoque de uso de patrones esque podemos "conseguir" una mayor eficacia en el diseño de nuestro sistema con automatizaciones. Este sistema puede ser desde el tracking automatizado de nuestras sesiones de ejercicio hasta el despligue automatico de nuestras creaciones.

En la [bibliografía](bibliografia.md) hay algunos recursos bastante interesantes sobre algunos de los patrones más comunes y artículos a como poder aplicarlo de forma correcta a automatizaciones.