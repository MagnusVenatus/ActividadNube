# ActividadNube
-Crear Carpeta y Crear docker-compose.yml
-en docker-compose.yml crear primera imagen bd, usar MariaDB v11, la BD se llama ActNube, Root pass: root123, usuario: Nico y Pass : app123
-Volmen guardado de datos en /var/lib/mysql con nombre de volumen act_db
-restart en "unless-stopped
-agregar networks como wp_network
-Healtheck

<img width="592" height="385" alt="image" src="https://github.com/user-attachments/assets/70bcc603-6770-46ab-ad4d-8d6f10d870bd" />


-Crear Imagen Wordpress v Latest, nombre contenedor: wordpress_nube y debe depender de bd
-el puerto sera "8082:80"
-Configurar environment con datos como host (db:3306), usuario: Nico, db pass: app123 y nombre db: ActNube, entre otros datos
-Volumen llamado wordpress_data en /mnt/data
-restart en "unless-stopped
-agregar network como: wp_network

<img width="415" height="439" alt="image" src="https://github.com/user-attachments/assets/bcace230-b0c1-40cb-a8cd-682d4caba193" />


-Finalizar docker-compose.yml con los volumenes a usar (act_db y wordpress_data)
-agregar networks (wp_networks)

<img width="172" height="129" alt="image" src="https://github.com/user-attachments/assets/9dc79def-7637-4b5c-bec7-7a4c588dec4b" />



