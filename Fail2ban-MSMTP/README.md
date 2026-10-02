\# Automatización de Despliegue: Fail2ban + MSMTP



Este playbook estandariza la instalación de Fail2ban y el envío de alertas por correo (MSMTP) en entornos de preproducción. Está diseñado para garantizar que todos los servidores queden configurados de forma idéntica sin intervención manual.



\## Características Principales



\* \*\*Detección dinámica del motor web:\*\* El código revisa si el servidor corre bajo Nginx u OpenResty y adapta los paths de los logs de forma automática para inyectar la configuración correcta.

\* \*\*Despliegue idempotente y seguro:\*\* Inicia el servicio con su configuración por defecto para forzar al sistema a generar los logs de forma nativa (`/var/log/fail2ban.log`). Esto asegura que al aplicar las reglas definitivas no haya fallos de lectura.

\* \*\*Filtros corporativos personalizados:\*\* Despliega reglas específicas para bloquear errores SSL, peticiones 4xx recurrentes y accesos denegados de forma automatizada.

\* \*\*Ejecución condicional:\*\* La instalación del cliente MSMTP se controla mediante la variable `usar\_msmtp`, evitando conflictos en servidores que ya cuentan con servicios de correo nativos.



\## Estructura del Proyecto



\* `Fail2ban.yml`: Playbook principal de ejecución.

\* `docs/`: Documentación técnica original en PDF.

