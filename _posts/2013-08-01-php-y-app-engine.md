---
layout: post
title: "php y app engine"
description: ""
category: 
tags: []
---
{% include JB/setup %}

#Ventajas de Php
Php es un lenguaje flexible, ampliamente adoptado por la comunidad latinoamericana. Por su flexibilidad permite que hayan personas que sean más estrictas y otros que hacen cosas de menor calidad.

#App Engine
App Engine es la infraestructura que usa Google que tiene para sus aplicaciones puesta a disposición de los desarrolladores. App Engine es una muy buena plataforma que permite facilmente escalar las aplicaciones, sin embargo demanda un aprendizaje complicado, conocer sus limitaciones, exige adaptar el codigo a sus restricciones. 

#Php y App Engine
En latinoamerica Php es el lenguaje más usado en latinoamerica para la web, 

#Escalabilidad
Previo a la nube el tiempo y dinero que se invertia en infraestructura era muy alto, y esto perjudicaba mucho a los desarrolladores y a sus platafromas, muchas veces también los equipos no cuentan con un SysAdmin, personas que estén capacitadas en la configuración y el manejo de Apache, mySql, etc; algunas personas subestiman este cargo y creen que es sudo tasksel lamp, cuando en realidad hay muchos problemas de seguridad, compatilidad y rendimiento que pueden ser causados por malas configuraciones de la maquina. 

#Limitaciones Php en App Engine
  No hay acceso al filesystem, se debe usar un CDN.
  Funciones de red, operaciones de sockets.
  Limites que no puedes extender
    Request Size            32 M
    Response Size         32 M
    Request Duration    60S
    Maximum Files       10K, 1K per directory
    Max App Size          32M

#Servicios y Apis de Google
  Logs | syslog ("")
  App Identity
  Mail
  MemCache
  UrlFetch
  Users
  Task Queues (superando el limite de los 60s)

  Google Cloud Sql
  noSql
  CloudStorage


#Lo Malo de App Engine



#A qué se enfrenta un desarrollador de Php ante esto
No existe .htacces, hay  un archivo yaml donde se configura esto, si usas un framework o todas las peticiones las recibe solo un archivo, sino hay que manualmente ingresar cada url. 

No es tan trivial conectarse a mySql, hay que dar toda la ruta al socket o usar el api de Google y su base de datos. 


