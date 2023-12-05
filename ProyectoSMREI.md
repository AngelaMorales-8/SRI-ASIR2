# Práctica Servidores web

### Vamos a instalar un servidor web interno para un instituto.
- Instalación del servidor web apache. Usaremos dos dominios mediante el archivo hosts: centro.intranet y departamentos.centro.intranet. El primero servirá el contenido mediante wordpress y el segundo una aplicación en python.

Instalamos Apache con: **sudo apt install2**

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/bd777988-be0c-4da5-b6ac-5feeaf49dd49)

Comprobamos que apache se ha instalado y está funcionando.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/f0cfe498-0284-48ee-8f96-7fc73a9baae4)


Con el comando **mkdir** creamos las virtual hosts de cada dominio, en la ruta /var/www

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/6c75264a-3b59-4c21-be35-d43192a7f60f)

Una vez tengamos los directorios, añadimos un archivo index.html a cada uno.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/3cc758bb-a05d-4a66-b177-1160a134b8b7)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/04061bef-017f-4f38-8623-59b85bf4417b)

Configuramos el servidor, con estos parámetros:

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/c5bb87de-c1da-4160-b468-a36bc0066871)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/0cd33834-05ea-4ab3-984f-b4dc91966543)

Utilizamos el comando **a2ensite hosts** para habilitar los hosts. Después de esto reiniciamos apache con: **systemctl reload apache2**

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/11646a16-aa57-4d2a-abc4-632259c8fd00)

Entramos en el fichero hosts y añadimos los dominios.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/c9a57c6f-1888-4116-addc-e09af443e50d)

Reiniciamos apache

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/b9b2be88-8346-4a13-a248-25c1646d41ee)

Ahora introducimos el dominio que hemos añadido en el navegador que queramos y podemos ver el contenido que hay en el fichero que creamos antes.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/51cc1022-c41f-4992-b673-d38134acc432)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/6743e0ad-cde9-4bd3-a7f7-6b18f44f9a23)

- Activar los módulos necesarios para ejecutar php y acceder a mysql.
  
  Instalamos mysql,con el comando: **apt install-mysql-server.**

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/69bdf10c-68c8-4916-9a3b-8771f52e79c1)

Para confirmar que está instalado escribimos en la línea de comando **mysql** y vemos como entramos en el programa, para luego salir ponemos **exit**.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/a854966a-ef6d-4172-a48b-658bb7086ff8)

Instalamos php con el comando: **apt install php libapache2-mod-php php-mysql**. Con **libapache2-mod-php** Apache gestione archivos php y con php-mysql php se comunica con las bases de datos de mysql.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/11c19593-7ebc-4abe-946c-8dd145decb95)

Comprobamos que está bien instalado con php -v.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/f0c68c76-399b-4dd1-8122-ec9d5219184f)

- Instala y configura wordpress.
  Configuramos la base de datos. Iniciamos sesión con el usuario root en mysql. Con el parámetro -u indicamos el usuario y con -p indicamos que nos solicite contraseña.
  
![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/ff8d35b3-7eb6-4e3f-90d6-d5285bc8ba3e)

Creamos la base de datos, para almacenar el sitio que vamos a mostrar

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/f7545aaf-384d-49cb-8fb2-abec93a9c5cd)

Creamos el usuario,para administrar la base de datos.

Con % vamos a tener acceso a todas las máquinas y con identified by establecemos la contraseña.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/41ac79f3-e5b0-4030-9e2a-527ef68f722c)

Damos permisos al usuario.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/498d5185-758f-4f3f-99d6-3ae08848bc03)

Reiniciamos con este comando para que se apliquen los cambios.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/9a8732df-821a-45a3-96a3-b2081780e3f3)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/b657c66b-227e-4a19-bb51-5e7e4aa299a9)


Instalamos extensiones para PHP.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/d7b1c53b-2216-4828-93b4-860bfe0eac49)


![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/c96dc775-4ee4-46c1-ba6f-0b46e0b7bff0)

Entramos en el fichero de virtualhost, escribimos un comando para permtir archivos .htaccess.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/c2bb2d9b-9d20-47f9-8cb6-68a1db75be34)


![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/0fa8e524-dc1a-496d-91e8-6c9fc0210301)

Con el comando **a2enmod rewrite** habilitamos el módulo de reescritura.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/829a5230-bc9b-44e1-ac8b-1a697304b9e5)

Una vez habilitados los cambios, para verificar que no hay errores, usamos apache2ctl configtest.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/fadb26e4-84d6-4e08-904a-54f5bd8125a0)

Descarga de Wordpress

Nos situamos en la carpeta que queramos descargar WordPress e introducimos la siguiente línea de comando. Luego lo descargamos usando tar.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/6b728bd8-e132-4d52-941d-be72b5f82748)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/0edafb21-5749-43d5-84a3-b40a047f66ca)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/127359af-f495-46d7-99f0-aad3b95727c9)


![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/2e0279e0-f4ab-4009-bbfc-fbba12b3a030)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/6eaa5a3e-5a92-4050-9c7c-fed4a4c5ae11)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/12985af4-0b45-4cc9-8297-fdb825624bd8)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/38df0f6c-d8a5-49d6-a9d7-3268bb152181)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/cad96ffb-2453-4e4b-99b5-519ff9b90369)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/ebddc97a-8470-42c1-9ec2-7529cce35036)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/4a54f6b4-cbc8-41f2-84a7-fcbebc285c3c)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/7df01eab-9f25-45cf-b4ec-74f414cd881f)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/125a978e-f25d-4327-be78-581f7b1da401)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/579bddf4-1893-4898-b4fa-6a94819c6a04)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/68169f76-d542-4cbc-b8dc-81ba2e1868f3)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/e768cdcc-6810-44be-8e84-cef79a80c1fb)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/139e4200-8d04-4e2e-9364-cd26bc8713ee)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/f0c0f8e2-adb3-4e23-ba32-77ca1ce10997)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/38e94d16-6e00-47a8-8513-3c04c5f140d4)

- Activar el módulo “wsgi” para permitir la ejecución de aplicaciones Python.
  
Primero haremos que Apache incorpore un soporte para servir archivos Python, para ello ejecutaremos la línea de comandos:

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/283ca721-403b-43a3-ae3d-1a643a33e6eb)

Reiniciamos apache para que se apliquen los cambios.
  
- Crea y despliega una pequeña aplicación python para comprobar que funciona correctamente.

Antes de crear y desplegar la aplicación en Python tenemos que crear los directorios necesarios. Debemos tener un directorio principal destinado a montar toda la aplicación en el cuál añadiremos los distintos directorios de configuración. La arquitectura de este directorio estára dividida en dos partes.

1.Estará destinada al almacenaje de nuestra aplicación Python y será un directorio privado.
2.Estará destinada a servir el contenido siendo un directorio público en el cuál almacenaremos archivos estáticos.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/fe0e2e9a-efb7-4937-b700-c6693600cf0e)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/25bb6ece-af51-486e-9e08-e55d6eb56eef)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/dd4a4279-1af9-4cd5-8c53-b8f8b0fefb9f)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/d0d1f25a-0a54-41f3-904c-665bbf68b33c)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/e2a0d40a-0fad-4797-afe3-5797e06530bc)



Ahora crearemos un controlador que será un archivo almacenado en nuestro directorio pythonapp, el cual se encargue de las peticiones realizadas por el usuario. Lo crearemos usando el editor de texto nano.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/7330199b-96c2-4cf7-affd-57a45ed7e52c)



  
- Adicionalmente protegeremos el acceso a la aplicación python mediante autenticación

Para poder proteger el acceso a la aplicación de Python tenemos que instalar primero el paquete de utilidades de Apache. En mi caso ya lo tengo y por eso me sale el siguiente mensaje diciendo que ya está instalado en su versión más reciente.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/b0ecf7ca-74d5-46eb-9cdb-4db9b24cb41f)

Ahora crearemos el archivo de la contraseña usando el comando htpasswd. La primera vez que se use este comando debemos añadir la opción -c para crear el passwdfile. Para ello especificamos un nombre de usuario que será el que usaremos más tarde para autenticarnos en la aplicación Python. En mi caso crearé una carpeta llamada password en los archivos de configuración del dominio departamentos.centro.intranet.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/8d5eea91-f227-488f-a0b2-28c20b88daab)

Si visualizamos el contenido de la carpeta donde hemos guardado la contraseña podemos ver el nombre de usuario que hemos creado y junto a él la contraseña cifrada.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/9ed94137-bbb1-4e8d-8fe3-dbb5277f58e8)

Ahora configuraremos el virtualhost para añadir la siguiente directiva.


- Instala y configura awstat.
- Instala un segundo servidor de tu elección (nginx, lighttpd) bajo el dominio “servidor2.centro.intranet”. Debes configurarlo para que sirva en el puerto 8080 y haz los cambios necesarios para ejecutar php. Instala phpmyadmin.

**Fin del Proyecto**
