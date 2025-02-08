# Manual de Usuario - Creación de un escenario en Make

## 1. Introducción

Antes de comenzar con la creación de nuestro primer escenario en Make, recomiendo conocer algunas de las [buenas prácticas](buenas-practicas.md) (patrones de diseño) que pueden aplicarse a flujos de trabajo y la ["instalación"](instalacionMake.md) o acceso a Make. 


## 2. Creación de un nuevo Escenario

#### Paso 1: Acceder a Make

Aunque es más que evidente este paso, es necesario [acceder](https://www.make.com) a Make y disponer de una cuenta con al menos el plan gratuito y con operaciones para poder crear y posteriormente probar el flujo de trabajo (workflow) creado.

#### Paso 2: Crear escenario

Hay diversas formas de poder crear un escenario pero el más sencillo y userfriendly es dirigirse a la sección de Scenarios y pulsar arriba a la derecha en "Create a new scenario"

![new scenario screenshoot](/img/scenarios.png)

#### Paso 3: Seleccionar un trigger (disparador)

En este punto debemos seleccionar una operación o trigger de los disponibles en Make, hay una cantidad de operaciones e integraciones bastante amplia. Para usar de ejemplo uno de los patrones de diseños indicados en la [documentación](buenas-practicas.md), vamos a poner de ejemplo **Event-Driven**, este consiste en ejecutar una acción en base a un evento. Vamos a configurar una automatización para recibir datos de un form de Google (Google Forms) y almacenar dichos datos en un documento calc de Google. (Realmente Google Forms permite conectarlo con un sheet, por lo que esta automatización realmente no es muy eficiente.)

📌[Enlace al form](https://docs.google.com/forms/d/e/1FAIpQLSfqkUpUEztW4FIlRdybUR3oA4DOZFQXHZ-vE6TogB9SH8W7Yg/viewform?usp=header)

![new scenario screenshoot](/img/new_scenario.png)

- Debemos seleccionar en el nuevo scenario Google Forms "Watch Responses"

![trigger screenshoots](/img/trigger.png)

- Ahora si no tenemos conectado Google FOrms con Make debemos hacerlo:

![create connection screenshoot](/img/create-connection.png)

- Ahora llega el momento de configurar el trigger, en este caso nos pide el id del Form, que debemos obtener pulsando el boton search e indicando el nombre del form y el número de respuestas a procesar por ciclo, en nuestro caso con dejar el por defecto (2) o incluso bajarlo a 1 es suficiente, de esta manera podemos probarlo y evitar un gasto inecesario de operaciones, ya que solo disponemos de 1000/mo.

![form id](/img/formId.png)

![trigger configuration](/img/triggerConf.png)

Para terminar de configurar el trigger, indicamos cuando va a empezar a "estar escuchando", es decir, cuando va a comenzar a recibir respuestas:

![trigger final step](/img/trigger-final.png)

#### Paso 4: Agregar una acción

Ahora pasamos a configurar la respuesta de nuestro patron Event-Driven.

- Agregamos un modulo de Google sheets para crear entradas a una sheet. Selecciona en Google sheet add Row

![google sheet action](/img/google_sheet.png)

- Ahora configuramos esta acción, como ya hemos conectado Make con Google solo tendremos que seleccionar la cuenta.

![google sheet connection](/img/googleSheetConnection.png)

- Ahora debemos de terminar de configurar la acción donde seleccionaremos el sheet, el espacio donde se ecuentra en Google Drive y los valores de la row a agregar.

En primer lugar vamos a elegir una spreedsheet que previamente hemos tenido que crear:

![spreedsheet](/img/spreedsheet.png)

Ahora elegimos los valores a agregar en las columns, estos valores debemos obtenerlo de los datos que se reciben del trigger.

![trigger data to row](/img/values.png)

Si nos fijamos en la imagen, se muestran en contenedores de colores los posibles datos que se pueden obtener del trigger de Google FOrm, recomiendo ejecutar de forma individual el trigger para ver los datos que trae de respuesta de manera que podamos agregarlos de forma correcta. Ya que se trata de un trigger basta con realizar el form creado:

![form repond](/img/Formrespond.png)

Aquí lo obtenido en make:

![trigger data](/img/trigger2data.png)

Como se puede observar podemos ver nuevos contenedores.

La configuración final quedaría:

![final conf](/img/finalConf.png)

Como he comentado antes, si ejecutamos el trigger podemos ver los valores recibidos.

Cabe aclarar que para que realmente esto funciona debemos activar el scenario para que cada 15 minutos (ya sea todo el scenario o solo el trigger) se ejecute, de esta manera cada 15 minutos va a coger las respuestas recibidas y las envia a Google Sheets, si obtamos por el plan Pro de Make podemos poner 1 minuto de manera que la automatización es casi en tiempo real.

![scenario](/img/scenario.png)

Para probarlo simplemente tendremos que responder el form y esperar 15 minutos, o una vez enviado el form darle al boton de ejecutar el scenario y si observamos podemos ver las respuestas que recibe y los datos que envia a google sheets:

Aquí se observa que recibe una respuesta y envia una al form
![running scenario](/img/runningScenario.png)

![google sheets data](/img/dataSpreadSheet.png)


#### Paso 5: Configurar notificaciones (Opcional)

Para mantener un registro en tiempo real, podemos agregar un módulo de Notificaciones por Email.

- Añade un módulo Email y selecciona Send an Email.
- Configura el destinatario, asunto y cuerpo del correo con los datos recibidos o simplemente indicando que se ha recibido datos y el enlace al spreadsheets.

![notifications](/img/notifications.png)


## 3. Conclusiones

LLegados a este punto ya hemos creado nuestro primer escenario en Make usando un patrón Event-Driven, capturando datos desde GoogleForm y almacenandolos en Google Sheets, además de recibir notificaciones al realizar este proceso.

Ahora es donde entra la práctica y la creatividad para crear workflows más complejos y útiles. En el directorio [examples](/examples/) se ecuentran algunos ejemplos creados en Make que se pueden probar y usar. Además en el documento [use-cases](casos-de-uso.md) comento algunas ideas o workflows aplicables a los diferentes patrones mostrados en [buenas-prácticas](buenas-practicas.md).