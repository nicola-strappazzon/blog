+++
title = "El mito del 'código debe ser agnóstico a la base de datos'"
date = "2020-06-27"
draft = false
tags = ["database"]
+++

Muchas veces nos dicen que **el código debe ser agnóstico a la base de datos** y esto se debería de interpretarse de una forma, pero lo cierto es que es ambiguo y cada quien lo entiende a su forma y necesidad, vamos a explicar esta filosofía tan compleja y a su vez _conflictiva_:

El término [agnóstico](https://es.wikipedia.org/wiki/Agnosticismo) significa del griego "sin conocimiento", y se cree que su origen surge cuando se crearon los primeros software intermedios llamados [DBAL/DAL](https://en.wikipedia.org/wiki/Database_abstraction_layer) que son librerías que ayudaban a la comunicación entre aplicación y base de datos, una [API](https://en.wikipedia.org/wiki/Application_programming_interface#Libraries_and_frameworks) más y no la del HTTP. De esta forma se puede abstraer el funcionamiento y crear compatibilidad con múltiples gestores de bases de datos usando el mismo código. Existen muchas variantes de este tipo de software, y pueden ser cualquiera de las siguientes variantes de nombres; DBAL, ODBC, ORM, ADO, PDO, DAL, Active Record, etc... En este post no hablaremos qué hace cada una, sino filosofar.

Los gestores de base de datos relacionales en su momento pensaron entre otras cosas en "estandarizar" con un lenguaje común para manipular los datos llamándolo SQL (Structured Query Language), luego la comunidad definió un estándar [SQL ANSI](https://blog.ansi.org/2018/10/sql-standard-iso-iec-9075-2016-ansi-x3-135/) por el cual "todos deberían" tener un mínimo de compatibilidad, lo cierto es que hay una gran similitud entre las funcionalidades básicas pero luego cada quien las amplio con otras propias, por más que se intento controlar del lado de las bases de datos ha sido limitado, y ésta es una razón más para tener un software intermedio (DAL).

Este software intermedio generó una gran aceptación en el mundo del desarrollo por la comodidad de no aprender un lenguaje adicional como el SQL o el JSON de un ElasticSearch o el de un MongoDB, permitiendo despreocuparse del detalle de los gestores de bases de datos, simplemente usando su lenguaje de programación principal podía manipular datos sin necesidad de saber los detalles internos. Ésta forma de trabajar ha generado muchos debates a favor y en contra.

Lo cierto es que cada Engine tiene sus particularidades; Un MySQL puede tener un lenguaje, componentes y un propósito parecido al PostgreSQL, pero comparado con MongoDB es completamente opuesto, posiblemente el DAL haga una compatibilidad bastante cercana, y puede que lamentablemente usemos un MongoDB como un MariaDB. Aquí hay que conocer cuales son las ventajas y limitaciones de cada uno, para eso hay que conocer bien el Engine y exprimir cada uno lo más que se pueda, cada uno esta hecho para un propósito, no existe uno que haga todo bien.

Se suele afirmar con cualquier situación que un DAL ofrece a tu aplicación la portabilidad entre gestores de bases de datos, y eso es muy subjetivo. Si tu desarrollo esta hecho para hacer un blog seguramente estés en lo cierto, pero a nivel empresarial cambiar de gestor de base de datos de un proyecto en producción no es así de simple. Primero que se apruebe el riesgo, luego viene todo el infierno (que me gusta) de migrar y transformar los datos, adaptar los modelos de datos, gestionar la redundancia, y un sin fin de obstáculos que habrán.

En mi opinión, las ventajas de usar un DAL es por lo práctico y rápido para desarrollar aplicaciones y estandarizar con un mismo lenguaje casi todo, pero hacer las cosas rápido no significa que sea igual de eficiente como cuando algo esta hecho a medida y con detalle. A lo que quiero llegar, es que; para muchos casos usar un DAL es bastante acertado, pero siempre hay momentos que se requiera realizar acciones a "bajo nivel" aprovechando ventajas propias que puede carecer un DAL en particular, es cierto que hay unos más completos que otros. También como desarrollador debes entender como funciona el Engine para saber que estas haciendo lo correcto con el DAL.

Considero que es muy practico escribir con el mismo lenguaje para conectarnos a un MariaDB para el registro y Login de un usuario, o gestionar los Token de acceso con un Redis, generar eventos y procesarlos en el Kafka, tener un ElasticSearch para hacer búsqueda y sugerencias de productos, guardar el catalogo en MongoDB. Todo esto bajo un mismo lenguaje, es una pasada.

Conclusión, aprende a usar bien el Engine para sacarle el máximo partido.

Todo lo que digo es subjetivo y dependerá de las variables particulares de cada proyecto.
