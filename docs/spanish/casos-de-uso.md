# Casos de Uso en Make

Como ya hemos comentado en la documentación, Make permite automatizar una amplia varidad de procesos utilizando diferentes patrones de diseño (si decidimos aplicarlos). A continuación, voy a mostrar algunas ideas de automatizaciones en función del tipo de patrón.

## 1. Event-Driven

#### Notificación automática de nuevos leads.

- Escenario:
Cuando un usuario completa un formulario de una web (ejemplo de Google Forms), se envía un correo electrónico de bienvenida al usuario y se puede registrar información del usuario en un CRM (Airtable). "Recomendable siempre indicar al user lo que se hace con sus datos =)".

- Workflow:
1. Trigger: recepción de una respuesta del form.
2. Acction: almacenar datos en CRM.
3. Acction: enviar un correo de bienvenida.

## 2. Orchestration

#### Gestión de pedidos en una E-commerce

- Escenario:
Automatización del proceso de gestión de pedidos desde la recepción hasta la actualización del inventario y el envío de confirmaciones.

- Workflow:
1. Trigger: nuevo pedido en shopify o wooCommerce (o cuilquier plataforma que admita Make)
2. Action: crear una orden en el sistema de gestión de inventario (se puede usar "Airtable")
3. Action: enviar confirmación de compra al cliente
4. Action: notificar al equipo logístico o involucrados

## 3. Choreography

#### Sincronización de Datos entre aplicaciones

- Escenario:
Varias aplicaciones intercambian información de manera descentralizada sin depender de un controlador central.

- Workflow:
1. Trigger: actualización de información en un CRM. (HubSpot por ejemplo)
2. Action: enviar actualización a google sheets
3. Action: sincronizar datos con slack para notificar al equipo.
4. Action: enviar actualización a una base de datos centralizada.

## 4. Batch Processing

#### Generación de informes automáticos

- Escenario:
Procesamiento de grandes volúmenes de datos y generación de informes periódicos.

- Workflow:
1. Trigger: ejecución programada cada semana
2. Action: extraer datos de múltiples fuentes (google analytics, salesforce...)
3. Action: generar informe en google sheet o incluso PowerBi si se tiene un licencia adecuada (que permita usar PowerBi Service).
4. Action: enviar el informe por correo electrónico, usar los chats de jira, slack, discord ...etc.

## 5. CI/CD

#### Automatización de Despliegues (deprecated)

- Escenario:
Integración de workflow de CI/CD para despliegues automáticos en un entorno de desarrollo.

- Workflow:
1. Trigger: push a un repositorio (Github, GitLab, Gitea(este es el mejor 😎))
2. Action: ejecutar pruebas automáticas
3. Action: construcción y despliegue (ejecutar un deploy para subir a firebase, por ej.)
4. Action: notificación en slack sobre el estado del despliegue, en discord para los contribuidores o incluso creación de una realease en github.

## Conclusiones

Estos "casos de uso" o ejemplos muestran algunas ideas aplicables en función del patrón, pero realmente hay infinidad de ideas, procesos o workflows que se pueden crear siempre que se identifiquen de forma correcta las necesidades a abarcar y como aplicar algunos de los patrones existentes (o incluso realizar modificaciones o combinarlos) para aportar valor y utilidad a las automatizaciones.

Volviendo a los "casos de usos" mostrados anteriormente, si construimos múltiples escenarios, en su conjunto construyen un sistema completo automatizado para la gestión de una pequeña pyme con un e-commerce de compra y venta de productos físicos, digitales o incluso de software. Al integrar todos los flujos "diseñados" se optimizan las gestión de pedidos, sincronización de datos, generación de reportes y despliegue de software, permitiendo una operación más eficiente y escalable de los procesos de "esta empresa".

Si nos fijamos en los ejemplos propuestos, al combinarlos, en realidad estamos creando un sistema automatizado de software on demand, donde cada proceso clave de la empresa queda optimizado y automatizado.

Además, al integrar todos estos patrones, se construye un entorno flexible y adaptable a diferentes necesidades empresariales. En este caso, el enfoque ha sido una empresa de software on demand, pero el mismo principio puede aplicarse a otros modelos de negocio con procesos similares.


En [examples](/examples/) puedes consultar o incluso probar por tu cuenta algunas de las automatizaciones implementadas.