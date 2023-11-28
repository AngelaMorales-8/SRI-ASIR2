# Práctica Servidores web

### Vamos a instalar un servidor web interno para un instituto.
- Instalación del servidor web apache. Usaremos dos dominios mediante el archivo hosts: centro.intranet y departamentos.centro.intranet. El primero servirá el contenido mediante wordpress y el segundo una aplicación en python.
Instalamos Apache con: **sudo apt install2**

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/bd777988-be0c-4da5-b6ac-5feeaf49dd49)


Creamos dos carpetas,con una página principal para cada una.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/af5687b0-9062-4d52-8423-8fe580316027)

Una página:

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/7ea9b298-219b-43d5-8aba-2cd926c32a8a)

Otra página:







- Activar los módulos necesarios para ejecutar php y acceder a mysql
- Instala y configura wordpress
- Activar el módulo “wsgi” para permitir la ejecución de aplicaciones Python
- Crea y despliega una pequeña aplicación python para comprobar que funciona correctamente.
- Adicionalmente protegeremos el acceso a la aplicación python mediante autenticación
- Instala y configura awstat.
- Instala un segundo servidor de tu elección (nginx, lighttpd) bajo el dominio “servidor2.centro.intranet”. Debes configurarlo para que sirva en el puerto 8080 y haz los cambios necesarios para ejecutar php. Instala phpmyadmin.
