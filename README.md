# ChatBot -> Flask - OpenAI - Render

<p align="center">
<img src="images/banner.jpeg"  height=400>
</p>

# Índice

* [Página en Local](#Página-en-Local) 
* [Construcción del ChatBot](#Construcción-del-ChatBot) 
* [Deploy en Render](#Deploy-en-Render) 
* [Requisitos](#Requisitos) 
* [Autor](#Autor)


# Página en Local

Se utilizó la librería Flask, para la construcción de la página web del chatbot.

**Archivos Principales**:
   - [`app.py`](https://github.com/jrguignan/ChatBot/blob/main/app.py): Es el archivo principal de la aplicación Flask que gestiona el servidor y las rutas necesarias para el funcionamiento del chatbot. Contiene las configuraciones para realizar solicitudes a la API de OpenAI y devuelve las respuestas del chatbot a la interfaz de usuario.
   - [`index.html`](https://github.com/jrguignan/ChatBot/blob/main/templates/index.html): Este archivo define la estructura y el diseño de la interfaz del chatbot. Ubicado en la carpeta `templates`, es responsable de la visualización y disposición de los elementos de la página (campos de entrada, botón de envío, mensajes del chat, etc.).

**Recursos Estáticos**:
   - Carpeta `static/images`: Dentro de la carpeta `static` se creó una subcarpeta `images` para almacenar la imagen utilizada en la interfaz del chatbot (como un logo o avatar). Flask sirve automáticamente estos archivos cuando se refieren en el HTML, facilitando la organización de recursos estáticos.

## Cómo Ejecutar la Aplicación Localmente

```python
#Para correr en local la página en Flask

#Clona este repositorio en tu equipo:
git clone https://github.com/jrguignan/ChatBot.git

#Entrar dentro del directorio
cd ChatBot

#Ejecutar app.py para ver la página en local
python app.py

#Luego se puede ver un navegador en esta dirección: http://127.0.0.1:5000
```

# Construcción del ChatBot

Para la construcción del chatbot, se utilizó **ChatGPT**, un modelo de lenguaje avanzado proporcionado por OpenAI. La comunicación con ChatGPT se realiza mediante la **API de OpenAI**, que permite integrar funcionalidades de conversación basadas en IA en aplicaciones externas, como este chatbot web.

El flujo general de la construcción del chatbot es el siguiente:

**Configuración del Entorno de Desarrollo**:
   - Se creó un entorno virtual de Python para instalar las dependencias necesarias, como Flask (framework de desarrollo web) y la biblioteca de OpenAI para interactuar con su API.
   - La API Key de OpenAI se configura como una variable de entorno para asegurar la seguridad y evitar la exposición directa de la clave en el código. Esto permite que Flask pueda acceder a la API de OpenAI de manera segura.

**Integración con la API de OpenAI**:
   - A través de la biblioteca `openai` para Python, el chatbot envía mensajes del usuario a la API de OpenAI y recibe las respuestas generadas por ChatGPT.
   - En el archivo [`app.py`](https://github.com/jrguignan/ChatBot/blob/main/app.py), se configuran los parámetros necesarios para la comunicación con OpenAI, como el modelo a utilizar (por ejemplo, `gpt-3.5-turbo`), y la función de generación de mensajes de respuesta del chatbot en base al input del usuario.
   - Para más detalles sobre la biblioteca de OpenAI, visita su [repositorio oficial](https://github.com/openai/openai-python).

**Creación de la Interfaz del Chat**:
   - La interfaz de usuario está construida con HTML y CSS en el archivo [`index.html`](https://github.com/jrguignan/ChatBot/blob/main/templates/index.html), ubicado en la carpeta `templates`. Este archivo permite que el usuario pueda interactuar con el chatbot ingresando mensajes y visualizando las respuestas en tiempo real.
   - A través de JavaScript, los mensajes del usuario se envían al backend de Flask mediante una solicitud `POST`. Al recibir la respuesta de la API de OpenAI, el backend la envía de regreso y se muestra en la interfaz.
   
**Diseño del Flujo de Conversación**:
   - La interfaz visual del chatbot sigue un estilo intuitivo, permitiendo que los mensajes del usuario y las respuestas del chatbot se diferencien claramente. Cada mensaje tiene un estilo distinto según su remitente (usuario o chatbot), mejorando así la experiencia visual y de interacción del usuario.

**Control de Errores y Respuesta del Chatbot**:
   - Se incluye un manejo de excepciones en el archivo `app.py` para gestionar posibles errores en la comunicación con la API (por ejemplo, fallos de conexión o errores de autenticación). En caso de error, se envía un mensaje amigable de advertencia al usuario.

Este flujo de construcción permite que el chatbot funcione de manera eficaz y segura, garantizando una comunicación fluida con el modelo de lenguaje de OpenAI para generar respuestas relevantes y coherentes.

---


# Deploy en Render

[Link Render](https://chatbot-zz60.onrender.com/)


# Requisitos

- Python==3.11.5: Necesario para ejecutar Flask y las dependencias de la API.

- Flask==3.0.3: Framework web para Python.

- openai==1.52.2 - API Key de OpenAI: Asegúrate de configurar tu clave de la API en las variables de entorno para que el chatbot pueda comunicarse con el modelo de lenguaje de OpenAI.

<br>[Volver al Índice](#Índice)

# Autor

- José R. Guignan
- Mail: joserguignan@gmail.com
- Linkedin: [https://www.linkedin.com/in/jrguignan/](https://www.linkedin.com/in/jrguignan)
- Portafolio: [https://jrguignan.github.io/](https://jrguignan.github.io/)
