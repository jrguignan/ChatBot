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


```python
#Para correr en local la página en Flask

python app.py

#Luego se puede ven un navegador en esta dirección: http://127.0.0.1:5000
```




# Construcción del ChatBot



# Deploy en Render



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
