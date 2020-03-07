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
En el módulo /etc/apache2/sites-enabled/dir.conf añadir el fichero index.php
```bash
<IfModule mod_dir.c>
    DirectoryIndex index.html index.cgi index.pl **index.php** index.xhtml index.htm
</IfModule>
```


### Instalacion phpMyAdmin
- [ ] Instalación phpmyadmin
- [ ] Comprobación http://IP/phpmyadmin
