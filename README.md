backup-ldap
==========

Función
-------

Realizar un backup completo de LDAP con configuración OLC:  
* LDAP config (slapcat -n 0)
* LDAP DIT (slapcat -n 1)  
  
Los backups se guardan en el directorio /var/backups/ con nombres:
* backup-config-ldap-$TIMESTAMP.ldif
* backup-db-ldap-$TIMESTAMP.ldif  

Instalación
-----------

La forma más sencilla de instalarlo es ejecutar estos comandos en el servidor ldap:

   $ wget --no-check-certificate -O /usr/local/sbin/backup-ldap https://raw.githubusercontent.com/algodelinux/backup-ldap/master/backup-ldap
   $ chmod 755 /usr/local/sbin/backup-ldap
  

Uso                   
---

   $ ldap-backup

Sugerencia
----------

Programar tarea cron: 00 9    * * 7   root    /usr/local/sbin/backup-ldap  
