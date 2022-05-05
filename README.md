# Servidor-NGINX

En primer lugar acudiremos a la terminal de Ubuntu y instalaremos NGINX mediante el comando `sudo apt-get install nginx`

![image](https://user-images.githubusercontent.com/91564872/166506611-11acb911-4701-4b70-b4ea-9b57e85a1eaf.png)

Iremos al navegador e introduciremos `localhost` para comprobar que se ha instalado correctamente

![image](https://user-images.githubusercontent.com/91564872/166961750-8804afad-5c4d-44ea-9b34-ab71aca18dec.png)

A continuación nos dirigiremos al directorio de nginx "sites-available"

![image](https://user-images.githubusercontent.com/91564872/166507562-c0d662ba-d5aa-4ade-bbbe-67d22b3d84e2.png)

Copiamos el archivo default 2 veces para usarlos con las dos páginas web que vamos a usar

![image](https://user-images.githubusercontent.com/91564872/166508287-b634566c-ccce-4dd7-9e90-bb8486c4daf4.png)
![image](https://user-images.githubusercontent.com/91564872/166508363-3ae07240-6b70-420b-b4d2-ead82e2be55f.png)

A continuación introduciremos `sudo vim primero.com` y editaremos el archivo para modificar el apartado de server name y root

![image](https://user-images.githubusercontent.com/91564872/166513879-f647b1df-48a6-436d-a0d3-c6532bfde9af.png)

Ahora nos moveremos al directorio sites-enabled y mediante el comando `ln -s ..` más la ruta del archivo, crearemos un archivo para los dominios que se encuentran en sites-available. También quiero destacar que les he tenido que cambiar el nombre a los archivos a `primero.sistemas.com` y `segundo.sistemas.com` ya que con los anteriores me causaba problemas y en algunas capturas de pantalla saldrán con el nombre original (`asciicamera.onehtmlpagechallenge.com` y `fireworks.onehtmlpagechallenge.com`) 

![image](https://user-images.githubusercontent.com/91564872/166962631-7a81edad-506e-4802-8fe9-023ed87e8db9.png)
![image](https://user-images.githubusercontent.com/91564872/166962537-d912d1ed-4912-4af3-8b90-6ffe30d36faf.png)

A continuación volveremos a editar primero.com mediante el comando `vim` para eliminar dos configuraciones que nos limitan a recargar nginx al estar configuradas para el "default-server"

![image](https://user-images.githubusercontent.com/91564872/166517376-c0fa50f0-cac7-41db-8b15-fe1b84e9ed8b.png)

A continuación descargaremos los codigos html de dos páginas web de onehtmlpagechallenge.com (en mi caso ASCII Camera y Adjustable Fireworks) y los moveremos con el nombre de index a unas carpetas creadas (primero y segundo) dentro del directorio `/var/www`. Una vez hecho esto usaremos `sudo nano hosts` para modificar el archivo hosts y introducir nuestras dos paginas web que se ejecutarán dentro del servidor nginx. 

![image](https://user-images.githubusercontent.com/91564872/166959751-5ad2df34-ae0f-4319-8908-fcb9974d5102.png)

![image](https://user-images.githubusercontent.com/91564872/166959611-6934850d-1860-4a59-bb2f-543d2861e3cb.png)

Finalmente introduciremos en nuestro navegador el dominio que les hemos puesto a nuestras paginas web (en mi caso primero.sistemas.com y segundo.sistemas.com) y como vemos en las imágenes funcionan a la perfección

![image](https://user-images.githubusercontent.com/91564872/166960140-942dd3bd-25a9-471d-8392-0c5a7ccd1b6d.png)

![image](https://user-images.githubusercontent.com/91564872/166960046-a294142d-e0d9-486b-a36c-569fa8367515.png)

