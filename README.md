# 1920DAW
Despliegue de Aplicaciones Web
## Configuración de red

  * Servidor HTTP Apache XXX-USED
  * Servidor DNS y LDAP XXX-LDAP
  
  | Host | Network |
  | ------ | ----- |
  | XXX-USED | *IP.:* 192.168.x.20x/24 *GW.:* 192.168.x.1 *DNS.:* 192.168.x.10X/24 8.8.8.8 |
  | XXX-LDAD | *IP.:* 192.168.x.10x/24 *GW.:* 192.168.x.1 *DNS.:* 192.168.x.10X/24 8.8.8.8 |
  
## Usuarios 
| Servicio | Usuario |
| --------- | ------- |
| SSH | miadmin/paso | 
| Apache | operadorweb/paso |
| MySQL | root/-- |
| - | admindb/paso|
| tomcat | tomcat/paso |
