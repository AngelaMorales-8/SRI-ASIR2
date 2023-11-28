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




















- Activar los módulos necesarios para ejecutar php y acceder a mysql
- Instala y configura wordpress
- Activar el módulo “wsgi” para permitir la ejecución de aplicaciones Python
- Crea y despliega una pequeña aplicación python para comprobar que funciona correctamente.
- Adicionalmente protegeremos el acceso a la aplicación python mediante autenticación
- Instala y configura awstat.
- Instala un segundo servidor de tu elección (nginx, lighttpd) bajo el dominio “servidor2.centro.intranet”. Debes configurarlo para que sirva en el puerto 8080 y haz los cambios necesarios para ejecutar php. Instala phpmyadmin.

**Fin del Proyecto**
