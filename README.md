# Servidor-NGINX

En primer lugar acudiremos a la terminal de Ubuntu y instalaremos NGINX mediante el comando `sudo apt-get install nginx`

![image](https://user-images.githubusercontent.com/91564872/166506611-11acb911-4701-4b70-b4ea-9b57e85a1eaf.png)

A continuación nos dirigiremos al directorio de nginx "sites-available"

![image](https://user-images.githubusercontent.com/91564872/166507562-c0d662ba-d5aa-4ade-bbbe-67d22b3d84e2.png)

Copiamos el archivo default 2 veces para usarlos con las dos páginas web que vamos a usar

![image](https://user-images.githubusercontent.com/91564872/166508287-b634566c-ccce-4dd7-9e90-bb8486c4daf4.png)
![image](https://user-images.githubusercontent.com/91564872/166508363-3ae07240-6b70-420b-b4d2-ead82e2be55f.png)

A continuación introduciremos `sudo vim primero.com` (le ha cambiado el nombre ya que con el nombre anterior no se copiaba bien el archivo default) y editaremos el archivo para modificar el apartado de server name y root

![image](https://user-images.githubusercontent.com/91564872/166513879-f647b1df-48a6-436d-a0d3-c6532bfde9af.png)

Ahora nos moveremos al directorio sites-enabled y mediante el comando `ln -s ..` más la ruta del archivo, crearemos un archivo para los dominios que se encuentran en sites-available

![image](https://user-images.githubusercontent.com/91564872/166516198-560a70cc-fe5e-44d9-a118-4644be76d9cd.png)

A continuación volveremos a editar primero.com mediante el comando `vim` para eliminar dos configuraciones que nos limitan a recargar nginx al estar configuradas para el "default-server"

![image](https://user-images.githubusercontent.com/91564872/166517376-c0fa50f0-cac7-41db-8b15-fe1b84e9ed8b.png)

![image](https://user-images.githubusercontent.com/91564872/166959751-5ad2df34-ae0f-4319-8908-fcb9974d5102.png)


![image](https://user-images.githubusercontent.com/91564872/166959611-6934850d-1860-4a59-bb2f-543d2861e3cb.png)

![image](https://user-images.githubusercontent.com/91564872/166960140-942dd3bd-25a9-471d-8392-0c5a7ccd1b6d.png)

![image](https://user-images.githubusercontent.com/91564872/166960046-a294142d-e0d9-486b-a36c-569fa8367515.png)

