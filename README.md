# Modulo-2---Fundamentos-del-Backend-y-la-Web

## Fundamentos de backend y la web

### Conceptos base

#### ¿Qué es un servidor?

Un servidor es un equipo o dispositivo en una red que administra los recursos de la misma. Tiene la capacidad de almacenar archivos y aplicaciones, proporcionar acceso a esos archivos y aplicaciones, y procesar solicitudes de varios usuarios o dispositivos a la vez. Los servidores se encargan de gestionar las solicitudes de los clientes conectados, proporcionándoles los datos que necesitan a la aplicación que quieren utilizar.

Un servidor es responsable de administrar y distribuir los recursos a través de una red. Esto incluye el manejo del almacenamiento y el intercambio de datos, permitiendo el acceso a documentos y aplicaciones compartidos, el alojamiento de sitios web y páginas web, el envío de correos electrónicos, la configuración del intercambio de archivos, el acceso seguro a través de internet mediante VPTN, así como la prestación de servicios adicionales según el tipo de servidor que sea

Existen diferentes tipos de servidores, los mas comunes son:

1. Servidores de corre
2. Servidores web
3. Servidores de juegos
4. Servidores de aplicaciones
5. Servidores de archivos
6. Servidores de impresión
7. Servidores de bases de datos.

#### Cliente vs Servidor

Un cliente se comunica con un servidor mediante varios protocolos y tecnologías. Para los clientes basados en web, el protocolo más común es el protocolo de transferencia de hipertexto (HTTP), que permite a un navegador web solicitar páginas web desde un servidor web. Otros protocolos como el protocolo simple de transferencia de correo (SMTP) y el protocolo de acceso a mensajes de Internet (IMAP) se utilizan para que los clientes de correo electrónico envíen y reciban correos electrónicos. Además existen protocolos como el protocolo de transferencia de archivos (FTP) para clientes de transferencia de archivos y el transporte de telemetría de cola de mensajes (MQTT) para clientes de internet de las cosas (loT).

La diferencia entre un cliente y un servidor es que el cliente es un dispositivo o aplicación de software que solicita y recibe servicios o datos de un servidor. Por otro lado el servidor es una poderosa computadora o aplicación de software que proporciona servicios o recursos a los clientes. Mientras los clientes inician las solicitudes, los servidores esperan las solicitudes y responden en consecuencia.

#### ¿Qué es una API?

Una API (application programming interface), o interfaz de programación de aplicaciones, es un conjunto de reglas o protocolos que permiten que las aplicaciones de software se comuniquen entre sí para intercambiar datos, características y funcionalidades. Las principales funciones de las APIS son poder facilitarles el trabajo a los desarrolladores y ahorrarles tiempo y dinero. Por ejemplo, si estás creando una aplicación que es una tienda online, no necesitarás crear desde cero un sistema de pagos y otros para verificar si hay stock disponible de un producto. Podrás utilizar la API de un servicio de pago ya existente por ejemplo PayPal, y pedirle a tu distribuidor una API que te permita saber el stock que ellos tienen. Se trata de utilizar tecnologías que ya existen.

### HTTP en profundidad

HTTP (Hypertext Transfer Protocol) es el protocolo fundamental de la web que define cómo los navegadores y los servidores web se comunican para transferir datos como páginas HTML, imágenes y videos, usando un modelo de solicitud-respuesta para intercambiar información.

#### Request / Response

Este modelo es la base de la comunicación web en donde un cliente envía una petición HTTP a un servidor, y este responde con una respuesta HTTP, que incluye un código de estado (Como 200 OK o 404 Not Found), encabezados y, a menudo, un cuerpo con el recurso solicitado (HTML, imágenes, datos JSON). Este ciclo bidireccional permite a los usuarios interactuar con la web, solicitando y recibiendo información de manera estructurada, utilizando métodos como GET o POST. 

#### Métodos HTTP (GET, POST, PUT, DELETE, PATCH)

HTTP define un conjunto de métodos de petición para indicar la acciona que se desea realizar para un recurso determinado. Aunque estos también puedan ser sustantivos. estos métodos de solicitud a veces son llamados HTTP verbs. Cada uno de ellos implementa una semántica diferente, pero algunas características similares son compartidas por un grupo de ellos.

1. GET: Solicita una representació9n de un recurso específico. Las peticiones que usan este método sólo deben recuperar datos.
2. HEAD: Este método pide una respuesta idéntica a la de una petición GET, pero sin el cuerpo de la respuesta.
3. POST: Se utiliza para enviar una entidad a un recurso en específico, causando a menudo un cambio en el estado o efectos secundarios en el servidor.
4. PUT: Reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición.
5. DELET: Borra un recurso en específico.
6. CONNECT: Establece túnel hacia el servidor identificado por el recurso.
7. OPTIONS: Se utiliza para describir las opciones de comunicación para el recurso de destino.
8. TRACE: Este realiza una prueba de bucle de retorno de mensaje a lo largo de la ruta al recurso de destino.
9. PATCH: Es utilizado para aplicar modificaciones parciales a un recursos.

#### Códigos de estado

Los códigos de estado de respuesta HTTP indican si se ha completado satisfactoriamente una solicitud HTTP específica. Las respuestas se agrupan en cinco clases:

1. Respuestas informativas (100-199).
2. Respuestas satisfactor (200-299).
3. Redirecciones (300-399).
4. Errores de los clientes (400-499).
5. Errores de los servidores (500-599).

#### JSON como formato de intercambio

JSON (JavaScript Object Notation) es un formato ligero de intercambio de datos. JSON es de fácil lectura y escritura para los usuarios. JSON es fácil de analizar y generar por partes de las máquinas. JSON se basa en un subconjunto de lenguaje de programación JavaScript. JSON es un formato de texto completamente independiente del lenguaje , pero que utiliza ocnvenios que resultan familiares a los programadores de lenguajes de la familia C, incluidos C, C++, C#, Java, JavaScript, Perl, Python y muchos otros. Estas características hacen JSON un lenguaje de intercambio de datos ideal. 

#### SOAP, XML y contexto histórico
1. XML (eXtensible Markup Lnaguage)

XML es un formato de datos creado a finales de los 90s para compartir información entre sistemas distintos, mantener estructura estricta y ser legible por humanos y máquinas 

un ejemplo de XML: 

```jsx
<usuario>
    <id>10</id>
    <nombre>Juan</nombre>
    <activo>true</activo>
</usuario>
```

Problemas de XML:

XML suele ser muy verboso, es decir que tiene mucho texto lo cual lo sueles hace difícil de leer y que lo hace más pesado para la red.

2.- SOAP (Simple Obkect Access Protocol)

SOAP es un protocolo (no solo un formato) que usa XML, define reglas estrictas de comunicación y fue creado para sistemas empresariales grandes

Ejemplo:

```jsx
<soap:Envelope>
  <soap:Body>
    <getUsuario>
      <id>10</id>
    </getUsuario>
  </soap:Body>
</soap:Envelope>
```

Sus principales características son que utiliza XML de manera obligatoria y que usa WSDL que son Web Services Description Language, es decir que usa contratos formales que define métodos disponibles, tipos de datos y estructura exacta del mensaje. Si no cumple el contrato, la petición falla. 

SOAP era usado en bancos, gobiernos, sistemas ERP, seguros y en empresas grandes pero con el tiempo fue decayendo por diversos impactos y por la llegada de REST + JSON.
