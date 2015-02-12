---
layout: post
title: "analista de airbnb"
description: ""
category: Data-Analist
tags: [san francisco, spanish, airbnb]
---
{% include JB/setup %}

<img src='https://pbs.twimg.com/media/BVCKo98CUAAoD9f.jpg' class='pull-right span5 img-polaroid' />
##SF Data Scientist <small>Riley Newman</small>##
Fui uno de los primeros empleados en AirBnB, el octavo.

###--Como era al principio?###
Todo era caotico, hay mil historias, éramos una combinación de "apagar incendios" y buscar nuevas oportunidades. La perspectiva de los nuevos era como usemos datos demográficos y eso, yo decidí concentrarme en la experiencia y la información de los usuarios que nos permitiera decidir como crecer.  Así que investigue hacia que ciudades vuela la gente, y donde encontramos un ratio interesante íbamos y abríamos, para asegurar un gran retorno.

###--Como es el ratio del que hablas?###
Lo que hicimos fue cuantificar mercados, para poder comparar por ejemplo a SF con NY, la idea era comparar los resultados de lugares en arriendo de ubicaciones en comparación a otros para encontrar ciudades donde hubiera el supply para arrendar. Entonces por ejemplo aunque a SF vienen muchas personas, hay muy pocas arrendado entonces no era tan buena idea comenzar ahí. El ratio es la relación entre la oferta y la demanda de lugares donde quedarte.
Reviews are super important, necesitabamos compenzar por la falta de reviews entonces hicimos varias cosas para esto, como enviar fotógrafos profesionales a los sitios para verificar que es verdad que son como decían, y fortificar las características de la plataforma para que las personas confíen en ella.

###Como se les ocurrió lo del fotografo?###
--AirBnb tiene bien integrado lo de la fotografia, desde el principio siempre supimos que era súper relevante, aumenta la confianza de la gente y hace que la plataforma se vea mucho mejor; hicimos varias investigaciones para validar que las personas lo consideran importante, fue un proceso de varias iteraciones; buscamos los listados menos usados en SF, que no tenían fotos y pésima descripción, enviamos los fotógrafos y después de tener las imágenes se incrementaron resto las reservas. Así que decidimos hacer eso para todos los mercados no balanceados.

>the founder of chartio has an airbnb profile and is renting his place to someone in the audience

###-Como luce la infraestructura de los datos hoy?###
Solo llevamos dos años, y hemos cambiado algunas veces el cluster ha cambiado y ha sido una mierda, al principio corríamos queries en producción, casual, casi no teníamos datos, pero luego mientras ha ido incrementado hemos tenido que crear nuevos clusters y copias para poder hacer estos procesos sin afectar la base de datos, estamos usando redshift para algunas cosas, y contratando expertos en sql para optimizar todo.

###-Quien te influencio en esto, quien admiras?###
El internet ha sido mi profesor, uso google siempre, pero afortunadamente en el equipo hay gente genial que me enseña muchas cosas y estå siempre dispuesto a colaborar, pair programming, reuniones, etc, y tratamos de promover eso porque a cualquiera le pasa que se bloquea y necesita ayuda, entonces hay que forzar la colaboración para mantener el flujo de trabajo activo siempre. Tenemos esta modalidad donde dos personas del equipo con skills diferentes están disponibles para ayudar a cualquiera que lo necesite con lo que pidan, trabajando juntos, una vez a la semana y se turnan.
También traemos con frecuencia personas muy tesas a dar charlas y ayudar a los miembros del equipo a aprender cosas bien avanzadas y que el equipo siempre mejore.

###-Que cosas del futuro o cool nos cuentas?###
El equipo esta organizado de forma que revela como ha evolucionado la compañía, pero el equipo de data está distribuido por todas partes, como una firma de consultoría, que ayuda a todos los sectores de la empresa a organizar y analizar sus datos.
Ahora estamos investigando como medir la confianza, es una pregunta gigante, como medir el amor y la confianza. Como podemos saber si la gente se está yendo, o dejando de usarlo, para AirBnb la confianza de los usuarios es súper importante entonces necesitamos manifestar confianza. Eso en lo intangible, en lo más 'tangible' estamos siempre tratando mejorar el algoritmo de búsqueda, para que cuando estés por viajar a una nueva ciudad puedas encontrar lo más rápido posible el lugar perfecto para estar.


###-Que estás tratando de lograr para medir el confianza y amor?###
Qué es la confianza? - nos preguntamos esto y miramos varias experiencias al respecto, porque las personas en diferentes situaciones tienen como ciertos niveles diferentes. Cuando se es primer usuario se tiene el más miedo y se le crea confianza con la reputación de la marca. Miramos reviews, análisis blogs de la gente, customer support etc para buscar cuales son las experiencias negativas o positivas que tienen los usuarios para reforzar o cambiar las cosas.

Cuando una persona decide alquilar también toma algo de confianza, porque siempre da miedo que no te paguen, o sean psicópatas. entonces diseñamos varios algoritmos para medir y buscar esto.

###-Como ser un buen host en AirBnb?###
es muy fácil, nuestro algoritmo esta alrededor de la experiencia, un buen anuncio es aquel donde la persona hace click y lo contacta, las fotos deben ser buenas y la descripción lo más detallada posible; y un precio razonable.
AirBnb es un marketplace con las normas de oferta y demanda, y se ve como actúan de forma agresiva las personas cambiando los precios y etc, es bien interesante.

###-A veces la gente es patan y deja malos reviews o falsos?###
Tenemos un algoritmo de verificación, analizamos reviews de verdad con sospechosos, buscamos patrones, hay usuarios que siempre dejan reviews altos entonces quizá no son tan objetivos, etc, y hemos tratado de analizar las experiencias AFK con el review dejado. Pero hemos dado prioridad a tener en cuenta otras cosas porque hemos visto que hay personas que van a quedarse en sitios aunque tengan una estrella.
Tratamos de usar AirBnb varias veces, quedarnos en sitios con diferentes niveles de reviews y analizar que lleva a las personas a comentar.

###-Cuantos hay en el equipo?###
Somos 16 data scientist en AirBnb, la mayoria han llegado en los últimos seis meses, saber como contratar ha sido dificil pero se nos ocurrió algo.
Primero hacemos un reto donde les damos unos sets de data y les damos unas preguntas para que resuelvan, entonces si son capaces de resolverlo vale la pena entrevistarlo, porque es una jartera entrevistar mil personas cuando solo 20 valía la pena hablar con ellas.
Si lo resuelven les damos la oportunidad de sentarse con el equipo y resolver algunos ejercicios, y escuchamos sus ideas, las herramientas que usan, cual es su metodología para resolver problemas, es algo genial, además porque podemos ver sus habilidades de comunicarse.

>Comunicarse es muy importante, muchas veces la gente no le da importancia a las habilidades de comunicación, cuando esto es lo mas importante, no importa cuanto sepas ni cuanto hayas descubierto sino puedes comunicarlo.
si pasan todo eso, les damos la oportunidad de hablar con otras personas de la empresa, para que entiendan los problemas a los que van a estar siendo enfrentados y ver sus habilidades de comunicación con personas no técnicas.

###-Que compone tu equipo?###
tenemos de todas las carreras, pero lo mas divicil es encontrar personas con experiencia en manejar datos, porque en la universidad no te dan datos de verdad, ni siquiera nos importa el lenguaje que saben usar, siempre que puedan entender los datos y demostrarlo

###-Cuantos empleados tuvo la compañía hasta que contrataron más gente?###
Uy, éramos muchas personas en toda la empresa y en todos los demás equipos pero durante muchos meses yo era el único analista, lo que hacia el trabajo muy dificil porque tenia que responder las preguntas de todo, luego cuando el equipo fue creciendo fue también muy complicado, al principio casi no dejaba trabajar a mis nuevos subordinados porque no sentía que fueran capaces aun, y me ha sido dificil estructurar al equipo y las herramientas; como no tenia experiencia en administración tuve que imaginarme muchas cosas; una decisión complicada fue cuando decidimos tener un equipo centralizado en vez de analistas en cada uno de los equipos de la empresa; cualquier persona de la empresa viene a nosotros y les resolvemos sus dudas y hacemos los cálculos y análisis que necesitan. y es chevere porque las personas de toda la empresa cuentan con nosotros y pueden aprender mucho
Unos retos complicados es determinar cuando una métrica es importante y cuando no, a veces la empresa quiere datos que son vanity pero desperdician el potencial del equipo de analíticas, entonces decidimos que el equipo va solo a trabajar en 'proyectos', entonces si alguna sección de la empresa necesita algo hace una petición y la justifica y en el equipo le asignamos los analistas para resolver sus dudas y darle los datos, de acuerdo a unos ordenes de prioridad para escoger lo más valioso para la empresa.

###-Como encuentras datos?, como encuentras datos en áreas que no estas midiendo? como escoges áreas para medir?###
En el offline experience casi no tenemos datos, es díficil averiguar que pasa en cada situación, entonces tratamos de emparejar los reviews y los datos que si tenemos para imaginar como era la experiencia offline. Entonces con el equipo de producto tratamos de desarrollar nuevas preguntas y secciones que nos permitan tener la mayor cantidad de información posible, registrar la mayor cantidad de eventos posibles y así poder comparar una cosa con otra.

###-Tienen como genios o matemáticos y eso?###
Cuando llegas al tamaño de twitter cualquier .00001 de crecimiento te sirve, entonces los analistas tienen que ser todos genios y buscar algoritmos muy complicados, nosotros todavía tenemos mucho por crecer entonces los retos no son aún tan complicados, por eso lo que más nos interesa es personas con buenas habilidades de comunicación que entiendan cuales son los problemas de la empresa y puedan comunicar efectivamente sus descubrimientos.

###-Que cosas tienes en cuenta para priorizar los proyectos y la data con la que van a trabajar?###
Cuando estaba yo solo tenia que ser muy cuidadoso con mi tiempo y por eso debía decirle no a casi todo, no era ideal pero así era, y aún hoy en día tenemos que descartar muchas ideas en valor de las más importantes. A veces nos pasa que los empleados no preguntan realmente lo que necesitan saber entonces tratamos de responderles y guiarlos hacia la información que realmente necesitan.

###-has hecho cosas que capturan data y finalmente no fueran usados?###
Siempre tenemos dashboards y cosas tratamos de sacar muchos datos, entonces muchas veces la información que capturamos no se usan, pero tratamos de no descartar las mediciones nunca, sin llenar de información inútil al equipo, entonces debemos ser claros con que información se usa y cual no porque si das demasiados datos puedes confundir al equipo

###-como decidieron cuanto cobrar?###
le cobramos al host 3% por el manejo de la transacción y eso, y el revenue lo sacamos del guest, 7 - 12% dependiendo del tamaño de la transacción.
Una cosa que puede ser útil, al principio teníamos algo así súper estricto como 7% si tal cosa, 8% si tal otra, etc, y luego cuando hicimos la curva mas lisa se aumento un montón el revenue.

###-como mides la productividad de tu equipo?###
lol, podemos correlacionar todo, pero hacemos unos encuestas en la empresa para tener como su opinión en el valor del trabajo que estamos haciendo.

###Que herramientas usan?###
Arrancamos con Google Analytics pero pronto nos dimos cuenta que los datos que nos daba eran muy pocos, y tuvimos que crear nuestra propia infraestructura para poder capturar y correlacionar datos, no es suficiente saber cuantas visitas tienes y cuantos alquileres han habido, necesitas saber todo el proceso de los visitantes y todo lo que han hecho en la página para poder tomar decisiones


