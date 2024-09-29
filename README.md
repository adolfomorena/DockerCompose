Instalar Odoo con Docker:
- Instalamos Postgres como gestor de BBDD:
- Abrimos Windows PowerShell y escribimos el siguiente comando:
-   docker run -d -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo -e POSTGRES_DB=postgres --name db postgres:16
- Instalamos Odoo enlazado a la BBDD (Escribimos el siguiente comando):
-   docker run -p 8069:8069 --name odoo --link db:db -t odoo
  
Para crear un modulo en Docker con Compose:
- Abrimos la consola de dockercompose-web1
- Escribimos ls para ver los directorios donde nos encontramos
- Nos movemos al directorio "mnt": cd mnt
- Nos movemos al directorio "extra-addons": cd extra-addons
- Para crear un modulo escribimos: odoo scaffold "nombre del modulo"
