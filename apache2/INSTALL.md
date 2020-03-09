# Protocolo de instalación LAMP
## 1. Servidor HTTP
- [ ] Instalación apache2 
- [ ] Cortafuegos (ufw help)
- [ ] Comprobación de funcionamiento
    * Desde la máquina anfitriona
    * Desde el propio servidor (instala el cliente HTTP, **curl**)


## 2. Servidor de aplicaciones PHP con MySQL

###  Servidor MySQL

- [ ] Instalación de MySQL (mysql-server)
- [ ] Testear funcionamiento de MySQL
- [ ] Versión de mysql
    
### PHP 
- [ ] Instalación de **PHP 7.4**
- [ ] Instalar la librería **libapache2-mod-php** 
- [ ] Testear funcionamiento de PHP
- [ ] Versión instalada 
        
### Configuración PHP con Apache
Editar el fichero /etc/php/7.4/apache2/php.ini
```bash
file-uploads = On
allow-url_fopen = On
memory_limit = 256M
upload_max_filesize = 100M
max_execution_time = 360
date.timezone = Europe/Madrid
```

| php.ini | Entorno Desarrollo | Entorno Producción |
| ---     | ---                | ---                |
| Errores | display_errors  = On / display_startup_errors = On | display_errors  = Off  /display_startup_errors = Off |
### MÓDULOS PHP 7.4
Listado o búsqueda de los módulos de php
```bash
 apt-cache search  php7.4
```
Instalar módulos
```bash
sudo apt install nombredelmodulo
```
### Mantenimiento de módulos PHP 
- [ ] php7.x-mysql
- [ ] php7.x-intl
- [ ] php7.x-xml
- [ ] php7.x-soap
- [ ] php7.x-zip


### Mantenimiento de módulos de Apache
En el módulo /etc/apache2/mod-enabled/dir.conf añadir el fichero index.php
```bash
<IfModule mod_dir.c>
    DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
</IfModule>
```

### Herramienta de desarrollo Xdebug para PHP
Instalación
```bash
sudo apt install php-xdebug
```
Configuración editar el fichero /etc/php/7.x/mods-available/xdebug.ini
```bash
zend_extension=xdebug.so
xdebug.show_error_trace = 1
xdebug.remote_enable = on
xdebug.remote_handler = dbgp
xdebug.remote_host = localhost
xdebug.remote_port = 9000
```

### Instalacion phpMyAdmin
- [ ] Instalación phpmyadmin
- [ ] Comprobación http://IP/phpmyadmin

## 3. Servidor SSH: Usuarios
- [ ] Instalación/Comprobación de SSH (openssh-server)
- [ ] Listar los puertos (netstat -ltn, puerto 22)
- [ ] Creación de usuario:

* Nombre del usuario operadorweb, su home /var/www y grupo www-data
* Permisos de /var/www/html son 2775 y propietario operadorweb:www-data de forma recursiva
- [ ] Modificar el fichero /etc/ssh/sshd_config para enjaular al usuario
```bash

Subsystem sftp internal-sftp

Match Group www-data
   ChrootDirectory %h
   ForceCommand internal-sftp -u 2
   AllowTcpForwarding yes
   PermitTunnel no
   X11Forwarding no 
```
  

