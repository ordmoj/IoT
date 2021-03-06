---

copyright:
  years: 2015, 2018
lastupdated: "2018-05-17"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# Desarrollo de {{site.data.keyword.iot_short_notm}} utilizando Node-RED
{: #dev_nodered}

Node-RED es una herramienta visual que puede utilizar para desarrollar las aplicaciones, dispositivos y pasarelas en {{site.data.keyword.iot_full}}. Node-RED proporciona funciones para conectar dispositivos de hardware, API y servicios en línea de formas nuevas e interesantes. Node-RED está creado en la parte superior de Node.js y aprovecha el gran ecosistema de módulo de nodo para proporcionar una herramienta que pueda integrar muchos sistemas distintos.
{:shortdesc}

IBM proporciona nodos Node-RED para que le ayuden a conectarse a los dispositivos, pasarelas y aplicaciones en {{site.data.keyword.iot_short_notm}} y para crear soluciones IoT rápidamente.


## Watson IoT Node   
{: #watson_iot_node}  

![Imagen de Watson IoT Node](../images/node-red-watson.png "Imagen de Watson IoT Node")


Watson IoT Node es un par de nodos para conectar los dispositivos o pasarelas al {{site.data.keyword.iot_short_notm}}. Los dispositivos o pasarelas pueden utilizar estos nodos para enviar sucesos y para recibir mandatos de la aplicación.

Para obtener más información sobre Watson IoT Node, consulte los siguientes recursos:

- [Watson IoT Node on GitHub ![Icono de enlace externo](../../../icons/launch-glyph.svg "Icono de enlace externo")](https://github.com/ibm-watson-iot/node-red-contrib-ibm-watson-iot){: new_window}
- [Documentación de Watson IoT Node ![Icono de enlace externo](../../../icons/launch-glyph.svg "Icono de enlace externo")](https://www.npmjs.com/package/node-red-contrib-ibm-watson-iot){: new_window}


## IBM IoT App Node  
{: #watson_app_node}  


![Imagen de IBM IoT App Node](../images/node-red-ibmiot.png "Imagen de IBM IoT App Node")

IBM IoT App Node es un par de nodos para conectar las aplicaciones a {{site.data.keyword.iot_short_notm}}. Las aplicaciones pueden utilizar los nodos para recibir los sucesos de dispositivo y enviar mandatos de nuevo al dispositivo.

Para obtener más información sobre IBM IoT App Node, consulte los siguientes recursos:

- [IBM IoT App Node on GitHub ![Icono de enlace externo](../../../icons/launch-glyph.svg "Icono de enlace externo")](https://github.com/ibm-watson-iot/node-red-contrib-scx-ibmiotapp){: new_window}
- [Documentación de IBM IoT App Node ![Icono de enlace externo](../../../icons/launch-glyph.svg "Icono de enlace externo")](http://flows.nodered.org/node/node-red-contrib-scx-ibmiotapp){: new_window}


## Más información y ejemplos   
{: #more_info}


Para ayudarle a empezar, utilice las siguientes recetas de ejemplo:
- [Iniciación a {{site.data.keyword.iot_short_notm}} mediante Node-RED ![Icono de enlace externo](../../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/recipes/tutorials/getting-started-with-watson-iot-platform-using-node-red/){: new_window}
- [Conexión de Raspberry Pi como dispositivo a {{site.data.keyword.iot_short_notm}} mediante Node-RED ![Icono de enlace externo](../../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/recipes/tutorials/deploy-watson-iot-node-on-raspberry-pi/){: new_window}

Para obtener más información, consulte también [Creación de apps con Node-RED Starter](https://console.ng.bluemix.net/docs/starters/Node-RED/nodered.html#nodered).
