# RabbitMQ Config - Corvus Platform

Este repositorio mantiene los archivos de configuración estática para el Message Broker (RabbitMQ) de la plataforma Corvus. Se utilizan estos archivos para aprovisionar automáticamente el entorno sin tener que configurar las cosas manualmente desde la interfaz gráfica.

## Archivos Principales
* `rabbitmq.conf`: Habilita plugins, puertos y vincula el archivo de definiciones json.
* `definitions.json`: Precarga los usuarios (`corvus_admin`), el Virtual Host `/`, los exchanges (ej. `corvus_events`) y las colas iniciales (`notifications_queue`, `email_queue`).

## Integración
El repositorio de Orquestación (`orchestration-back-corvus`) monta estos archivos como volúmenes de lectura directamente en el contenedor de RabbitMQ.
