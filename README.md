\# Automatización de Servidores con Ansible (IaC)



Este repositorio contiene playbooks y plantillas de Ansible diseñados para automatizar el despliegue, configuración y securización de infraestructura Linux. El enfoque principal es mantener la infraestructura como código, garantizando la idempotencia, reduciendo los tiempos de despliegue y eliminando la configuración manual por SSH.



\## Proyectos Incluidos



\* \[\*\*Despliegue de Fail2ban + MSMTP\*\*](./fail2ban-msmtp-deployment): Automatización de seguridad perimetral para servidores web. Detecta dinámicamente el motor (Nginx u OpenResty) e inyecta reglas de bloqueo personalizadas.

\* \[\*\*Relay SMTP con Postfix (Azure)\*\*](./postfix-azure-relay): Provisión ágil de servidores de correo satélite en la nube. Incluye soporte multi-SO y gestión segura de credenciales mediante Ansible Vault.



\## Tecnologías y Herramientas



\* \*\*Automatización:\*\* Ansible, Jinja2, Ansible Vault.

\* \*\*Sistemas Operativos:\*\* Debian/Ubuntu, RHEL/CentOS.

\* \*\*Servicios Web \& Red:\*\* Nginx, OpenResty, Postfix, Fail2ban, MSMTP.

\* \*\*Cloud:\*\* Microsoft Azure.

