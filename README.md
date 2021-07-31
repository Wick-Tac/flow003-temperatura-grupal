# flow003-temperatura-grupal
Este repositorio contiene el flow 3 de los ejercicios de Introducción a NodeRed.

Este flow muestra la información de ID, temperatura y mensaje personalizado enviado por alumnos por MQTT.

Puedes encontrar el curso de introducción a NodeRed en el siguiente enlace

https://edu.codigoiot.com/course/view.php?id=817

Para que este flow funcione, requieres de los nodos dashboard.

https://flows.nodered.org/node/node-red-dashboard

Los alumnos deben enviar un mensaje en JSON al siguiente tema MQTT

`codigoIoT/SIC/flow3/temp`

Este flow se conecta al la ip de un broker publico, por ejemplo broker.hivemq.com

Para obtener la IP de dicho broker se puede ejecutar el siguiente comando en una terminal de Linux

`nslookup broker.hivemq.com`

Las variables que se deben enviar son ID,Temp y mnsg.

Este flow muestra los mensajes, ID y valores de Temperatura recien llegados. Adicionalmente hace una gráfica del historio de valores enviados por todos los alumnos.

Este flow también demuestra el uso de "IF" con ayuda del nodo "SWITCH".

Este flow demuestra el uso de las notificaciones de voz con ayuda del nodo "CHANGE".

Este flow envía una respuesta al broker publico en el siguiente tema

`codigoIoT/SIC/flow3/sw`

Los nodos funcition requieren código extra para filtrar los datos que requieren los nodos dashboard. Los códigos se encuentran en la carpeta functionNodes y cada nodo de función requiere del código que se encuentra en el archivo de texto del mismo nombre.

El nodo JSON debe configurarse como `Always convert to Java Script Object`.

Los nodos dashboard deben configurarse por los alumnos para generar la interfaz visual como se expresa en la siguiente imagen.

![](https://github.com/codigo-iot/flow003-temperatura-grupal/blob/main/grafica.jpg)

El nodo SWITCH debe ser configurado para contar con dos salidas segun el umbral de temperatura que se desee comprobar.

Los nodos CHANGE deben configurarse para enviar el mensaje que requiere el nodo SWITCH de la sección DASHBOARD (true/false) o lo que sea que se desee que el nodo de voz mencione.

Por: [Hugo Vargas](https://github.com/hugoescalpelo)
.
