# Creación de un Bot de Telegram para Make

## Introducción
Para integrar Telegram con Make y automatizar acciones, primero necesitamos crear un bot en Telegram, obtener su API Token y configurarlo correctamente.

## 1. Crear un Bot de Telegram
Para crear un bot en Telegram, sigue estos pasos:

1. Abre Telegram y usa la barra de búsqueda para encontrar **BotFather**.
2. Inicia un chat con **@BotFather** y envía el comando `/newbot`.
3. Asigna un nombre a tu bot (ejemplo: `MiBotAutomatizadoPFTT2024`).
4. Asigna un nombre de usuario único que termine en `bot` (ejemplo: `MiBotPepe_Bot`).
5. **BotFather** generará un **API Token**. Copia y guarda este token en un lugar seguro, ya que lo necesitarás para conectar Telegram con Make.

> **Nota:** No compartas el API Token públicamente, ya que permite el control total de tu bot. Si llegará a filtrarse tu API token solo debes ir al chat de BotFather y usar el comando para eliminar el bot: /deletebot

## 2. Agregar el Bot a un Grupo o Canal
Si deseas que el bot interactúe en un grupo o canal, debes agregarlo como administrador:

1. Abre el grupo o canal en Telegram.
2. Toca el nombre del grupo/canal en la parte superior.
3. Ve a **Administradores** y selecciona **Añadir Administrador**.
4. Busca el bot por su nombre de usuario y agrégalo.
5. Otorga los permisos necesarios para leer y enviar mensajes.

Para los [ejemplos](/examples/simple-automation/AutomatedTelegramBot.md) usados hemos interactuado directamente desde el chat del bot.

## 3. Obtener el Chat ID
El **Chat ID** es necesario para que el bot pueda enviar mensajes a un grupo o usuario específico. Sigue estos pasos para obtenerlo:

### **Para Grupos o Canales Públicos**
1. Abre el grupo o canal en Telegram.
2. Ve a la configuración y busca el enlace del grupo (`t.me/nombreGrupo`).
3. El texto después de `t.me/` es el **Chat ID**.

> **Nota**: si lo prefieres puede usar directamente el @NombreGrupo/Canal del grupo o canal.

### **Para Grupos o Canales Privados** [USADO en el [ejemplo](/examples/simple-automation/AutomatedTelegramBot.md)]
1. Crea un escenario en **Make**.
2. Agrega el módulo **Telegram Bot - Watch Updates**.
3. Configura una nueva conexión con el API Token del bot.
4. Ejecuta el módulo en modo **Run once**.
5. Envía un mensaje al grupo/canal donde el bot es administrador.
6. En **Make**, revisa la respuesta del webhook y busca el campo `message.chat.id`. Ese es el **Chat ID**. 

> **Nota**: el chat id también se puede obtener de 'message.from.id'.

## 4. Configurar el Bot en Make
Con el **API Token** y el **Chat ID**, puedes configurar el bot en **Make**:

1. Crea un nuevo escenario en **Make**.
2. Agrega el módulo **Telegram Bot - Watch Updates** (para recibir mensajes) o **Send a Text Message** (para enviar mensajes).
3. Configura la conexión pegando el **API Token**.
4. Usa el **Chat ID** para indicar a dónde enviar los mensajes.