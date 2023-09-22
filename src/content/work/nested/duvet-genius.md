---
title: Gestión Hotelera
publishDate: 2020-03-04 00:00:00
img: /assets/stock-3.jpg
img_alt: Imagen del proyecto en su vista principal, donde se ven diferentes hoteles.
description: |
  Desarrollamos un sistema de gestión hotelera, de una cadena de hoteles para la empresa Tranqui Descanso.
tags:
  - Java
  - Spring Boot
  - Hibernate
  - JPA
  - MVC
  - Postgres
---

## Proyecto de Gestión Hotelera

### Backend para Gestión Hotelera

Para desarrollar la robusta capa backend de nuestro sistema de gestión hotelera, hemos optado por utilizar un conjunto de tecnologías líderes en la industria para garantizar la eficiencia y la escalabilidad. El backend de nuestro sistema se basa en el siguiente conjunto de tecnologías:

- **Java**: Utilizamos Java como nuestro lenguaje de programación principal debido a su versatilidad y robustez. Java es ideal para aplicaciones empresariales y nos permite implementar una lógica de negocio sólida y segura.
- **Spring Boot**: Hemos adoptado Spring Boot como nuestro marco de desarrollo, lo que nos permite acelerar el proceso de desarrollo y centrarnos en la creación de servicios web de alta calidad. Spring Boot también nos brinda características de seguridad y gestión de dependencias que son esenciales para un proyecto de esta envergadura.
- **Hibernate y JPA**: Para la gestión de datos y la interacción con nuestra base de datos PostgreSQL, hemos elegido Hibernate junto con JPA (Java Persistence API). Estas tecnologías nos permiten mapear objetos Java a entidades de base de datos de manera eficiente y realizar operaciones de CRUD de manera sencilla.
  - Utilizamos Hibernate para mapear nuestras clases Java a entidades de base de datos. Esto nos permite realizar operaciones CRUD de manera eficiente y sencilla.
  - Utilizamos JPA (Java Persistence API) para definir las entidades de base de datos y sus relaciones. JPA nos permite definir las entidades de base de datos utilizando anotaciones Java, lo que nos permite mantener un código limpio y legible.
- **MVC (Modelo-Vista-Controlador)**: Implementamos el patrón de diseño Modelo-Vista-Controlador para mantener una estructura organizada y escalable en nuestro backend. Esto nos ayuda a separar la lógica de negocio, la presentación y el control de las operaciones.

- **PostgreSQL**: Como sistema de gestión de bases de datos, hemos seleccionado PostgreSQL debido a su confiabilidad y capacidades de escalabilidad. PostgreSQL es una opción sólida para manejar los datos críticos de nuestra cadena hotelera.

Con esta poderosa combinación de tecnologías, hemos desarrollado un backend que proporciona una API RESTful eficiente y segura para gestionar todas las operaciones relacionadas con la gestión de hoteles y reservas. Nuestro backend se integra perfectamente con la base de datos PostgreSQL y proporciona un rendimiento óptimo para garantizar una experiencia fluida para nuestros usuarios y clientes.

### Premisa

La cadena de hoteles TRANQUIDESCANSO S.A. desea administrar los datos de sus operaciones a través de una base de datos relacional. Dentro de esta cadena hotelera existen varios hoteles registrados a nivel nacional, de cada uno de estos hoteles se cuenta con su nombre, dirección, teléfonos, año de inauguración, antigüedad y categoría. De acuerdo con la reglamentación hotelera nacional, todos los hoteles deben estar clasificados en una categoría (cinco estrellas, cuatro estrellas…), es posible que el hotel pueda disminuir o aumentar de categoría y es importante dejar registrado el momento en que realiza cambio de categoría.

Además, los hoteles ofrecen a sus huéspedes diferentes tipos de habitaciones (individual, doble, suite…) en donde cada una de ellas tiene una identificación particular para lograr diferenciarlas en el momento de asignarlas.

Las habitaciones pueden ser reservadas por los huéspedes directamente, en cuyo caso se requiere registrar número de identificación, nombre, dirección y teléfonos de contacto de quien realiza la reserva y quedará como responsable de la misma. Si la reserva es realizada por una agencia de viajes, es importante que se registren los datos del huésped responsable de la reserva (identificación, nombre, dirección y teléfonos) y los datos de la agencia que realiza la reserva incluyendo la identificación y el nombre. Es importante dejar el registro de la fecha en la cual se realiza la reserva, la fecha en la que iniciaría y finalizaría la reserva, cantidad de personas, cantidad de habitaciones, el tipo de habitación y servicios adicionales que pudiera requerir como por ejemplo parqueadero, cuido de mascotas, entre otros.

La cadena hotelera da la opción de pagar el 20% del valor de la reserva hasta 24 horas antes, si esto no se notifica al hotel la reserva se cancelará y las habitaciones quedarán disponibles para ser asignadas a otros huéspedes. Por otra parte, el 80% restante del valor de la reserva se deberá cancelar en el momento de realizar el registro de llegada al hotel. La hora en la que inicia el registro de entrada de los huéspedes es a las 3:00 pm y se darán máximo 4 horas adicionales para este proceso. Si pasadas las cuatro horas, es decir, si a las 7:00 pm del día en el que inicia la reserva no se ha realizado el registro en el hotel, las habitaciones quedarán disponibles para ser asignadas y el huésped no podrá pedir reintegro del dinero abonado a la reserva.

Una vez se ha realizado el registro de llegada, es importante diligenciar la identificación y nombre de cada una de las personas que se hospedarán en el hotel bajo el número de reserva y la habitación a la cual queda asignado cada uno de estos huéspedes. Así mismo, es importante recordar que debe quedar pagado el saldo existente para la reserva. Una vez se ha completado este proceso, se puede hacer entrega de las llaves de las habitaciones y los huéspedes podrán hacer uso de los servicios con que cuenta el hotel.

Una vez culmina la estadía de los huéspedes en el hotel, para hacer entrega de la habitación primero es importante pagar los servicios adicionales que hayan consumido y así con el paz y salvo podrán abandonar las instalaciones del hotel.

Al hotel le interesa que a partir de los datos registrados en la base de datos sea posible obtener información como la siguiente:

- Reservas realizadas en un período de tiempo.
- Reservas que fueron canceladas sin pagar el valor del 20% de anticipo.
- Reservas que no fueron utilizadas y pagaron el 20% de anticipo.
- Reservas que tuvieron registro de llegada de los huéspedes a tiempo (registraron 3 pm a 7 pm de lo contrario no llegaron a tiempo).
- Reservas que registraron huéspedes menores de edad y/o mascotas.
- Reservas que pagaron servicios adicionales.
- Datos de los huéspedes correspondientes a una reserva particular.
