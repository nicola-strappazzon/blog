+++
title = "Rol de un DBA"
date = "2015-01-14"
draft = false
tags = ["database"]
+++

Puede que este papel hoy en día se este perdiendo, y se haya mezclado con los de Operaciones o con algún Desarrollador, está mal!, en proyectos grandes es muy importante dedicarle todo el tiempo posible, llega un momento que el volumen de datos y el tráfico se vuelve insostenible, a este punto, **cuando algo falla es catastrófico y no suele arreglarse rápidamente**, la prevención es bastante crucial y se vuelve una eterna lucha.

Ser Administrador de Bases de Datos es algo bastante exigente, **porqué debes saber un poco de todo**; de programación, de sistemas y mucho de Bases de Datos. El dominio de cada una de ellas es bastante crucial para entender como gestionar bien los recursos, prevenir incidencias e incluso resolverlas.

![DBA](image.png)

Debes trabajar codo a codo con los Desarrolladores, antes que ellos se pongan a programar, debes estar diseñando nuevos modelos de datos, pensando principalmente como influye en el rendimiento y mantener la integridad, una vez terminada la parte de programación, debes hacer un Code Review de la Pull Request, luego es enviada al equipo de Quality Assurance, de ellos te puedes esperar de todo, es la idea no? Una vez que todo está listo, pasa a producción y aún no puedes quedarte tranquilo, debes seguir vigilando.

**Cada empresa tiene un modelos de datos particular**, depende mucho del modelo del negocio, de lo que consigues cuando llegas, de las personas, incluso el lenguaje de programación puede influenciar. Por eso que hay que ser flexibles hasta cierto punto.

Mientras no estás trabajando con los desarrolladores, te dedicas más a la parte de sistemas, hacer actualizaciones, ver porque hay retraso de una replica, revisar un respaldo, revisar las gráficas buscando anomalías, tunear, probar cosas nuevas y ver que puedes ir mejorando, aquí la creatividad se te puede ir de las manos.

Para saber que **funciones cumple** el rol, te listos unas cuantas:

*   Instalar, actualizar e implementar parches.
*   Diseñar las bases de datos.
*   Desarrollar, automatizar y probar estrategias de respaldo y restauración.
*   Administrar los servidores de bases de datos.
*   Administrar el almacenamiento y IOPS de MySQL.
*   Administrar la seguridad de los servidores y de MySQL.
*   Administrar los objetos de MySQL, como; tablas, particiones, índices, eventos, vistas y procedimientos almacenados.
*   Desarrollar y mantener mecanismos de ofuscación de datos sensibles en los respaldos para los desarrolladores.
*   Monitorizar y configurar la base de datos para el óptimo rendimiento.
*   Investigar, y reunir información de diagnostico para realizar reportes de futuras incidencias.
*   Evaluar y probar nuevas funcionalidad de MySQL.
*   Gestionar las migraciones o cambios que se llevan sobre el modelo.
*   Documentar todo.

También podemos ir un poco más allá, mezclando lo nuestro con la parte de Operaciones y así somos más ágiles e independientes:

*   Implementar una infraestructura de monitoring y alertas.
*   Implementar y mantener los balanceadores de carga.
*   Ofrecer una plataforma de bases de datos para Business Intelligence.
*   Usar herramientas para gestionar de forma automática la configuración.

Es mucho para no seguirlos aburriendo, para la próxima.
