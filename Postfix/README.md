\# Despliegue de Servidores Relay Postfix en Azure



Automatización de la provisión y configuración de servidores de correo emisor (satélite/relay) hospedados en Microsoft Azure. El paso de un modelo manual a este modelo IaC reduce el tiempo de despliegue de \~45 minutos a menos de 10 segundos por máquina.



\## Características Principales



\* \*\*Arquitectura Multi-SO:\*\* El playbook contiene lógica condicional para detectar y adaptarse automáticamente a las familias de sistemas operativos Debian (Ubuntu) y RedHat (CentOS/Rocky Linux).

\* \*\*Seguridad Enterprise:\*\* Los servidores se configuran para escuchar únicamente en la interfaz de loopback (`127.0.0.1`), evitando la creación de open relays. Las comunicaciones hacia el exterior van cifradas por TLS.

\* \*\*Gestión de Secretos:\*\* Se utiliza Ansible Vault para el almacenamiento centralizado y cifrado de las credenciales de autenticación SASL (Office 365 / Exchange).

\* \*\*Plantillas Dinámicas:\*\* Uso de Jinja2 para generar los archivos de configuración (`main.cf` y mapeos de contraseñas) en tiempo de ejecución, inyectando las variables del inventario según el entorno.



\## Estructura del Proyecto



\* `instalar\_postfix.yml`: Playbook principal de orquestación.

\* `inventario.ini`: Definición de hosts, grupos y parámetros de conexión (bastion/SSH).

\* `templates/`: Plantillas Jinja2 para la configuración de Postfix y credenciales SASL.

\* `docs/`: Documentación técnica y diagramas de arquitectura en PDF.

