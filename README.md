# backup-ldap
Realizar un backup completo de LDAP con configuración OLC:  
* LDAP config (slapcat -n 0)
* LDAP DIT (slapcat -n 1)  
  
Los backups se guardan en el directorio /var/backups/ con nombres:
* backup-config-ldap-$TIMESTAMP.ldif
* backup-db-ldap-$TIMESTAMP.ldif  
  
*uso*                 : ldap-backup  
*instalación*         : Guardar en  /usr/local/sbin/  
*sugerencia*          : Programar tarea cron: 00 9    * * 7   root    /usr/local/sbin/backup-ldap  
