# Sistema de Gestión de Pedidos, Stock y Producción — Render 3D

1. Descripción del proyecto

El presente proyecto consiste en el desarrollo de un sistema de información para Render 3D, emprendimiento dedicado al diseño, fabricación y comercialización de productos realizados mediante impresión 3D.

El sistema tiene como finalidad centralizar y organizar la información relacionada con los pedidos, el stock de materiales y el proceso de producción, permitiendo mejorar el seguimiento de los pedidos y facilitar la gestión de las actividades internas.

El proyecto integra los contenidos desarrollados progresivamente en los Trabajos Prácticos Integradores (TPI) de la asignatura Organización Empresarial.

---

2. Objetivo del sistema

Desarrollar una solución informática que permita gestionar de manera organizada los pedidos de los clientes, controlar la disponibilidad de materiales y realizar el seguimiento del proceso de producción hasta la finalización del pedido.

---

3. Alcance

El sistema contempla principalmente:

- Registro y gestión de clientes.
- Registro y seguimiento de pedidos.
- Control de materiales y stock.
- Seguimiento del estado de producción.
- Actualización del estado de los pedidos.
- Consulta de información para facilitar la toma de decisiones.

El proyecto se encuentra enfocado en los procesos de pedidos, stock y producción de Render 3D.

---

4. Áreas involucradas

La estructura organizacional considerada para el proyecto contempla las siguientes áreas:

- Dirección
- Ventas y Atención al Cliente
- Producción
- Stock y Materiales
- Administración y Compras
- Sistemas, como área de apoyo a Dirección.

El sistema de gestión permite integrar información proveniente de las distintas áreas involucradas en el proceso.

---

5. Principales entidades de datos

El modelo inicial de datos contempla las siguientes entidades:

 Cliente
    Representa a las personas o empresas que realizan pedidos.

Principales datos:

- ID del cliente
- Nombre
- Teléfono
- Email

 Pedido
    Representa una solicitud realizada por un cliente.

Principales datos:

- ID del pedido
- ID del cliente
- Fecha de ingreso
- Estado

 Producto
    Representa los productos que pueden ser fabricados y comercializados.

Principales datos:

- ID del producto
- Nombre
- Material
- Stock

 Producción
    Representa el proceso de fabricación asociado a un pedido.

Principales datos:

- ID de producción
- ID del pedido
- Fecha de inicio
- Estado

---

6. Proceso principal

El proceso principal modelado corresponde a la gestión y producción de un pedido.

De manera general, el proceso contempla:

1. El cliente realiza un pedido.
2. Ventas y Atención al Cliente registra el pedido.
3. El sistema valida los datos y verifica la disponibilidad de materiales.
4. Si no existe stock suficiente, Administración y Compras gestiona la adquisición de los materiales necesarios.
5. Producción prepara y fabrica el producto.
6. Se realiza un control de calidad.
7. Se verifica que el producto cumpla con las especificaciones del pedido.
8. El sistema actualiza el estado del pedido.
9. Ventas coordina la entrega y comunica al cliente.

El proceso será representado mediante BPMN, utilizando pools, lanes, tareas, eventos, compuertas y flujos.

---

7. Historias de usuario

 Gestión de pedidos

Como usuario de Ventas y Atención al Cliente, quiero registrar los pedidos de los clientes, para mantener organizada la información y facilitar su seguimiento.

 Control de stock

Como responsable de Stock y Materiales, quiero consultar y actualizar el stock de materiales, para conocer su disponibilidad y detectar cuándo es necesario realizar una compra.

 Seguimiento de producción

Como responsable de Producción, quiero consultar el estado de los pedidos y actualizar su avance, para realizar un seguimiento ordenado de la fabricación.

---

8. Gestión del proyecto

El desarrollo y la documentación del proyecto se gestionan mediante Git y GitHub.

Se utiliza:

- Repositorio público en GitHub.
- Rama principal `main`.
- Ramas secundarias para desarrollar y organizar cambios.
- Commits descriptivos.
- Pull Requests para revisión e integración de cambios.
- GitHub Desktop como herramienta de apoyo para la gestión del repositorio.
- GitHub Projects para la gestión del backlog y las actividades del proyecto.

---

9. Estructura inicial del repositorio

La documentación del proyecto se organizará de la siguiente manera:

render3d-sistema-gestion/
|
|--- README.md
|
|--- docs/
|   |--- tp1-empresa.md
|   |--- tp2-planificacion.md
|   |--- tp3-estructura-datos.md
|   |--- proceso-gestion-pedido.md
|
|--- historias-usuario/
    |--- pedidos.md
    |--- stock.md
    |--- produccion.md

Esta estructura podrá modificarse durante el desarrollo según las necesidades del proyecto.

---

10. Documentación del proyecto

El repositorio contiene la documentación correspondiente al desarrollo progresivo del sistema:

- TP1: análisis de la organización y definición del sistema.
- TP2: diagnóstico, análisis FODA, objetivos, metas y planificación.
- TP3: estructura formal y diccionario de datos inicial.
- TP4: procesos BPMN, gestión colaborativa, Git/GitHub, backlog y control.

---

11. Declaración de uso de Inteligencia Artificial

Para la elaboración y organización de este proyecto se utilizó ChatGPT, un modelo de lenguaje de gran escala (LLM) desarrollado por OpenAI, como herramienta de apoyo.

La herramienta fue utilizada principalmente para:

- Comprender y organizar las consignas de los trabajos prácticos.
- Proponer estructuras iniciales para la documentación.
- Analizar alternativas para el diseño del proceso y su modelado.
- Ayudar a estructurar historias de usuario y documentación técnica.
- Revisar y mejorar la redacción de los contenidos.

Los resultados generados mediante IA fueron revisados y corregidos de forma manual. Se verificó su coherencia con el proyecto de Render 3D y con las consignas de la asignatura, manteniendo la responsabilidad sobre las decisiones, modificaciones y contenido final presentado.

---

12. Autor

Nahuel Campoy

Proyecto académico desarrollado para la asignatura Organización Empresarial — TUP AD, UTN.