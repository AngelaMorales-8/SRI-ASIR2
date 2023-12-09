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

Vamos a crear un archivo para añadir los ficheros creados anteriormente.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/6eaa5a3e-5a92-4050-9c7c-fed4a4c5ae11)

Copiaremos el archivo de configuración que lee WordPress usando el de muestra que trae.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/12985af4-0b45-4cc9-8297-fdb825624bd8)

Creamos el archivo en el que se instalar las actualizaciones de Wordpress para que si Wordpress tuviera que hacerlo por su cuenta no tuvieramos problemas con los permisos.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/38df0f6c-d8a5-49d6-a9d7-3268bb152181)

Configurar el directorio de WordPress
Primero damos permisos al usuario y al grupo www-data que es el que puede escribir archivos de WordPress.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/cad96ffb-2453-4e4b-99b5-519ff9b90369)

Establecemos los permisos a directorios y ficheros de wordpress.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/ebddc97a-8470-42c1-9ec2-7529cce35036)

Ahora vamos a configurar unos cambios en el archivo de configuración principal de WordPress. Vamos a ajustar las claves secretas para proporcionar más seguridad a nuestra instalación. WordPress tiene un generador de estos valores, usaremos el siguiente comando para ejecutarlo.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/4a54f6b4-cbc8-41f2-84a7-fcbebc285c3c)

Ahora copiamos estos valores en el archivo de configuración de WordPress. Lo abrimos con nano.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/0c2e01ac-bd0c-4d90-bbf9-ab55630e1ee0)

Buscamos el apartado en el que se encuentran los valores y los copiamos.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/579bddf4-1893-4898-b4fa-6a94819c6a04)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/68169f76-d542-4cbc-b8dc-81ba2e1868f3)

Después vamos a ajustar los parámetros de nuestra base de datos en el fichero de configuración, añadiremos nuestro nombre, usuario y contraseña creados anteriormente. Aparte también agregaremos otra línea la cual indica la forma en la que escribirá WordPress en el sistema de archivos. 

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/e768cdcc-6810-44be-8e84-cef79a80c1fb)


Una vez completado todo si entramos en un navegador usando el dominio creado, se nos abrirá la interfaz gráfica de configuración de WordPress.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/25bb6ece-af51-486e-9e08-e55d6eb56eef)

Rellenamos los campos con nuestros datos y pulsamos instalar.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/dd4a4279-1af9-4cd5-8c53-b8f8b0fefb9f)

Una vez instalado WordPress y ahora podemos iniciar sesión.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/d0d1f25a-0a54-41f3-904c-665bbf68b33c)

Al iniciar sesión ya podemos empezar a configurar páginas en la web de WordPress.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/e2a0d40a-0fad-4797-afe3-5797e06530bc)


- Activar el módulo “wsgi” para permitir la ejecución de aplicaciones Python.
  
Primero haremos que Apache incorpore un soporte para servir archivos Python, para ello ejecutaremos la línea de comandos:

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/283ca721-403b-43a3-ae3d-1a643a33e6eb)

Reiniciamos apache para que se apliquen los cambios.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/b2e9d417-027b-4b62-866f-1c4528a6cccb)
  
- Crea y despliega una pequeña aplicación python para comprobar que funciona correctamente.

Antes de crear y desplegar la aplicación en Python tenemos que crear los directorios necesarios. Debemos tener un directorio principal destinado a montar toda la aplicación en el cuál añadiremos los distintos directorios de configuración. La arquitectura de este directorio estára dividida en dos partes.

1.Estará destinada al almacenaje de nuestra aplicación Python y será un directorio privado.

2.Estará destinada a servir el contenido siendo un directorio público en el cuál almacenaremos archivos estáticos.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/fe0e2e9a-efb7-4937-b700-c6693600cf0e)


Ahora crearemos un controlador que será un archivo almacenado en nuestro directorio pythonapp, el cual se encargue de las peticiones realizadas por el usuario. Lo crearemos usando el editor de texto nano.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/5013e426-d0d1-4f0c-9b0b-fc88b2f57141)

Configuramos el virtualhost.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/b785be17-c6f5-4219-84f7-b87d244532e6)

Una vez configurado el virtualhost habilitamos el sitio web y recargamos apache.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/f7a5ee1e-db18-4b04-a270-d1a79dfee703)

- Debemos proteger el acceso a la aplicación para poder proteger el acceso a la aplicación de Python tenemos que instalar primero el paquete de utilidades de Apache. 

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/7330199b-96c2-4cf7-affd-57a45ed7e52c)

Ahora crearemos el archivo de la contraseña usando el comando htpasswd. La primera vez que se use este comando debemos añadir la opción -c para crear el passwdfile. Para ello especificamos un nombre de usuario que será el que usaremos más tarde para autenticarnos en la aplicación Python. En mi caso crearé una carpeta llamada password en los archivos de configuración del dominio departamentos.centro.intranet.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/8d5eea91-f227-488f-a0b2-28c20b88daab)

Si visualizamos el contenido de la carpeta donde hemos guardado la contraseña podemos ver el nombre de usuario que hemos creado y junto a él la contraseña.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/9ed94137-bbb1-4e8d-8fe3-dbb5277f58e8)

Nos pedirá la ruta con el nombre del fichero, un usuario y una contraseña. Una vez creado, configuraremos el VirtualHost de la siguiente manera:

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/a61665dc-4027-4254-99ac-6500bbd71e90)

Reiniciamos apache y si accedemos a nuestra página nos pedira autenticación para ver el contenido.

Cuando ponemos un usuario y contraseña validos nos permite ver el contenido.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/dacaa430-016c-4e75-877f-ea389e0cf150)


![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/f7a5ee1e-db18-4b04-a270-d1a79dfee703)

- Instala y configura awstat.
  
![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/13cf72c4-b4d6-4279-abe6-a8f8488c1426)


![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/45e7155f-fd74-42b8-83c4-868ce90f829a)

Copiamos el archivo de configuración por defecto de awstats para cada servidor en el que lo queramos añadir. Configuramos los siguientes parámetros dentro del fichero usando nano para poder editarlo. Editaremos LogFile,SiteDomain y HostAliases.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/4223ae36-eb2e-4fb9-9307-526a2a0b511d)

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/1f606593-ee88-42b4-add3-95034aa32009)

Reiniciamos apache y ejecutararemos el siguiente comando para actualizar los ficheros.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/03e6ef24-a8ff-4135-8712-b940fadeb6c6)

Una vez hecho esto entramos en la ruta establecida de nuestro dominio y podemos ver todas las estadísticas que se muestran.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/c65c619e-d471-4674-80da-cdcdf5ce4d62)


- Instala un segundo servidor de tu elección (nginx, lighttpd) bajo el dominio “servidor2.centro.intranet”. Debes configurarlo para que sirva en el puerto 8080 y haz los cambios necesarios para ejecutar php. Instala phpmyadmin.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/8fecb943-81e4-4f3f-9ff5-e6d4ed2c654d)

Para instalar nginx usamos el comando **sudo apt install nginx**
y lo iniciamos con **sudo systemctl start nginx**

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/ce30636c-c1d2-42f9-8033-17b132c85cfe)

Entramos con el dominio y el puerto que hemos añadido podemos ver como carga nginx

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/c842d892-f3ed-425d-b067-acc14ac054ab)

Instalamos mysql y php.

![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/509342ec-d7f4-4b40-9b15-cc47048066a4)

Modificamos la configuración
Si entramos después de haber modificado el fichero de configuración de nginx y activando las siguientes líneas podemos ver como muestra la información de php.


![image](https://github.com/AngelaMorales-8/SRI-ASIR2/assets/122454505/fad3e642-257a-4c8e-8a2d-bd7b3cb151d6)



**Fin del Proyecto**
