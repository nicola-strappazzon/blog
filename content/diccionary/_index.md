+++
draft = true
title = 'Diccionario de base de datos'
+++

En el mundo de base de datos existe una gran variedad de términos técnicos que deberíamos estar familiarizados:

- **Asíncrono:** Es la comunicación más rápida. Quien envía al receptor no espera y continúa con su ejecución inmediatamente.
- **Atómico:** Es uno de los términos que conforma el acrónimo del ACID. Hace referencia a todo o nada de una transacción. Como una transacción puede estar conformada por varios pasos, para garantizar la Integridad, hay mecanismos de controles internos que permiten aplicar un cambio si no hay interrupciones en el flujo.
- **CatchUp:** Acción que realiza un slave para actualizarse y tener el lag a cero.
- **co-masters:** Hace referencia a otro master del mismo cluster.
- **Consistencia:** Cuando la base de datos refleja el último cambio recibido casi de forma instantanea.
- **Consistencia eventual:** Cuando las bases de datos distribuidas reflejan el último cambio recibido en todos los nodos casi de forma instantanea.
- **Contención:** Hace referencia a la acción producida por el bloqueo. Esto ocurre cuando multiples procesos intentan acceder al mismo recurso simultaneamente y se encuentra bloqueado por otro proceso, y así se apilan los procesos. Esto es debido a que el tiempo de espera para liberar el recurso es muy prolongado.
- **Crawler:** Son aquellos servicios que se encargan de ir extrayendo los datos constantemente para luego ser procesados por otros servicios.
- **DDL:** Es el acrónimo de Data Definition Language, son un grupo de sentencias SQL utilizadas para definir las diferentes estructuras de la base de datos, como lo son; la misma base de datos, las tablas, índices, triggers, funciones, vistas. Por ejemplo son aquellas sentencias que empiezan por `CREATE [DATABASE|TABLE]`, `ALTER`, etc...
- **DML:** Es el acrónimo de Data Manipulation Language, son un grupo de sentencias SQL que son utilizadas para manipular los rows, estos son: SELECT, INSERT, UPDATE, y DELETE.
- **Fetcher:** Es un crawler.
- **Field:** Campo, columna, atributo.
- **Latencia:** quiere decir que no hay retraso Which means that there is no lag when the write operations are being written to the disk.
- **MPM:** Este es un término creado por mí para hacer referencia a los diferentes fork de MySQL, Percona y MariaDB.
- **On-premise:** Servicio en tu infraestructura local o en tu cloud y gestionada por la organización, lo opuesto a SaaS.
- **Resiliencia:** Es la capacidad de un sistema en reponerse a su normalidad luego de un incidente.
- **Row:** Tupla, record, registro
- **Sincrono:** Quien envía permanece bloqueado esperando a que llegue una respuesta del receptor antes de realizar cualquier otra tarea. Se puede decir que la realización estándar de MySQL es síncrona. Cuando hay escrituras paralelas, se aplican de forma paralela en todos los nodos, mientras en la realización estándar de MySQL es una a la vez.
- **SPoF:** Single Point of Failure.
- **Tenant:** Cuando un cliente se le dedica un servidor con su propia base de datos y no es compartida con otros clientes.
- **Transacción:** Son un conjunto de órdenes que se ejecutan en la DB formando una unidad lógica de trabajo (a esto se le llama atomicidad). Transacciones no finalicen en un estado intermedio.
- **Tupla:** Es el término usado para referirse a un registro de una tabla, se utiliza en el lenguaje de base de datos relacional, difiere del término Row porque no es del léxico del SQL.
