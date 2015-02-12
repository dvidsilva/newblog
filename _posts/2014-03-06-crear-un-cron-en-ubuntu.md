---
layout: post
title: "crear un cron en ubuntu"
description: ""
category: Programando
tags: [programming, spanish, ubuntu, cron]
---
{% include JB/setup %}

Para agregar un cron tienes que correr el comando sudo crontab -e


si el comando falla puede ser que no tengas cron instalado, dale sudo apt-get install gnome-schedule


tienes que agregar una fila donde le explicas cada cuando corre y que va a correr


minutos (0-59), horas (0-23, 0 = midnight), dias (1-31), meses (1-12), dia de la semana (0-6, 0 = Sunday),



si pones * * * * *  se va a ejecutar cada minuto

si pones */60 *  * * * se va a ejecutar cada segundo




* * * * * /usr/bin/php /var/www/ruta/archivo.php




puedes mirar el listado de crons con sudo crontab -l


en el archivo de php que vayas a ejecutar tienes que tener cuidado de como usas los include, porque se va a estar ejecutando desde una ruta absoluta, no desde la carpeta raiz, y tambien, el resultado del archivo no va al navegador ni nada, sino que tienes que escribir supongo que al disco duro.
