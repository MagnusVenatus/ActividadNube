# ActividadNube
-Crear Carpeta "ActividadNube" y Crear docker-compose.yml
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


Ejecutar Comando: "docker run -d --name wp -p 8082:80 wordpress:6-apache" en CMD dentro de Carpeta "ActividadNube" (antes de crear y configurar docker-compose.yml)
Ó, usar "docker compose up -d --build" despues de configurar el .yml

<img width="873" height="216" alt="image" src="https://github.com/user-attachments/assets/fdaf9f7f-0b63-4b57-a5d8-e6828d251b35" />

rellenar datos 

<img width="765" height="896" alt="image" src="https://github.com/user-attachments/assets/bcc8687e-daa6-41d0-8dc5-6b1241aabb3d" />

<img width="802" height="562" alt="image" src="https://github.com/user-attachments/assets/6fdc58e2-f7d3-4fa3-8b5a-d2c0f572d3c9" />

Iniciar sesion 

<img width="449" height="777" alt="image" src="https://github.com/user-attachments/assets/c6862e16-74c5-42bb-819a-240446bb63fd" />

Listo

<img width="1903" height="930" alt="image" src="https://github.com/user-attachments/assets/41d15571-9a95-4aa2-85fc-965e8d6be8e4" />




