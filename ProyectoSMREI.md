# Práctica Servidores web

### Vamos a instalar un servidor web interno para un instituto.
- Instalación del servidor web apache. Usaremos dos dominios mediante el archivo hosts: centro.intranet y departamentos.centro.intranet. El primero servirá el contenido mediante wordpress y el segundo una aplicación en python.
Instalamos Apache con: **sudo apt install2**

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/bd777988-be0c-4da5-b6ac-5feeaf49dd49)


Creamos dos carpetas,con una página principal para cada una.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/486db158-1288-4412-b76b-e2f48a5e8bbe)


Una página:

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/6e63be8b-6a10-487c-9073-84fe850197c0)


Otra página:

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/6ea27eb9-1dab-4396-8559-1deb46e3b401)


Ahora creamos los dominios de configuración de estos sitios.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/fffd769a-300c-487d-b869-1c5a6204e0fa)


![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/bc92caa9-a984-4742-adcd-b9fe9f16a10f)


![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/213b073e-1083-4a17-803e-c7131c7435c5)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/6606c430-c2c5-46df-a967-9d9528d46815)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/9c39c3fb-044a-41ad-beca-1491fe3f0344)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/ed728992-3d80-4c4c-a409-4d222712fa2b)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/bc14c095-2588-4553-847f-0a228a79b1de)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/5f366208-a0b8-42de-8603-bfda378df630)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/036a5e97-fe64-4468-b3f1-bfbf2f202148)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/456429aa-5128-4ab5-ad8b-c7392234d7d9)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/ef30e774-7818-4a5a-81d8-72856fbef90e)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/937a279e-e942-4fb0-bb40-0dbf6e665e06)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/7e3a567b-766f-45ec-8926-527bd0181b4f)

Ajustamos los permisos para que apache pueda acceder a ellas y abrir el archivo index.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/84d67e49-3b3e-440b-ae91-c863b11c933c)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/05f0fc03-b287-4cb9-9a8f-4b57b58f9d38)


** New

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/40cffdde-68ba-4b6c-ad5e-913812ff53a7)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/2482884c-d66c-49ac-8805-6550f6256a0c)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/05e20b51-5640-4f3c-a84d-31c64182a18c)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/2f79805a-0673-4fa8-be8a-befa7ddeb8b8)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/df683d8f-ff79-4fbd-9625-a5c12e6fd1a6)

** NEW 2

# Práctica Servidores web

### Vamos a instalar un servidor web interno para un instituto.
- Instalación del servidor web apache. Usaremos dos dominios mediante el archivo hosts: centro.intranet y departamentos.centro.intranet. El primero servirá el contenido mediante wordpress y el segundo una aplicación en python.
Instalamos Apache con: **sudo apt install2**

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/6ffaec23-0740-4752-93f8-15787cd0fad7)

Con el comando **mkdir** creamos las virtual hosts de cada dominio, en la ruta /var/www

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/6c75264a-3b59-4c21-be35-d43192a7f60f)

Una vez tengamos los directorios, añadimos un archivo index.html a cada uno.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/3cc758bb-a05d-4a66-b177-1160a134b8b7)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/04061bef-017f-4f38-8623-59b85bf4417b)

Configuramos el servidor





Habilitamos los VirtualHosts y reiniciamos apache.







- Activar los módulos necesarios para ejecutar php y acceder a mysql
- Instala y configura wordpress
- Activar el módulo “wsgi” para permitir la ejecución de aplicaciones Python
- Crea y despliega una pequeña aplicación python para comprobar que funciona correctamente.
- Adicionalmente protegeremos el acceso a la aplicación python mediante autenticación
- Instala y configura awstat.
- Instala un segundo servidor de tu elección (nginx, lighttpd) bajo el dominio “servidor2.centro.intranet”. Debes configurarlo para que sirva en el puerto 8080 y haz los cambios necesarios para ejecutar php. Instala phpmyadmin.

**Fin del Proyecto**
