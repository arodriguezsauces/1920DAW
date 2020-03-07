# Protocolo de instalación LAMP
## 1. Servidor HTTP
- [ ] Instalación apache2 
- [ ] Cortafuegos (ufw help)
- [ ] Comprobación de funcionamiento


## 2. Servidor de aplicaciones PHP con MySQL

###  Servidor MySQL

- [ ] Instalación de MySQL (mysql-server)
- [ ] Testear funcionamiento de MySQL
    
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
### Instalación de módulos PHP dependiendo de la versión php instalada
- [ ] php7.x-mysql
- [ ] php7.x-intl
- [ ] php7.x-xml
- [ ] php7.x-soap
- [ ] php7.x-zip


### Instalacion phpMyAdmin
- [ ] Instalación phpmyadmin
- [ ] Comprobación http://IP/phpmyadmin
