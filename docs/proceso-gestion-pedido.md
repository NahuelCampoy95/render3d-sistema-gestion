# Proceso de Gestión y Producción de un Pedido

## 1. Nombre del proceso

**Proceso de gestión y producción de un pedido de Render 3D**

## 2. Objetivo

El proceso tiene como objetivo organizar el recorrido de un pedido desde la solicitud realizada por el cliente hasta la finalización y entrega del producto, integrando la gestión de pedidos, la disponibilidad de materiales y la producción.

## 3. Participantes

El proceso contempla los siguientes participantes:

### Cliente

Solicita un producto y proporciona las especificaciones necesarias para su fabricación.

### Render 3D

La organización interviene mediante diferentes áreas y funciones:

- Ventas y Atención al Cliente.
- Sistema de Gestión.
- Administración y Compras.
- Producción.

## 4. Flujo general del proceso

El proceso comienza cuando el cliente realiza una solicitud de pedido.

### 1. Recepción del pedido

Ventas y Atención al Cliente recibe la solicitud y registra el pedido en el sistema.

### 2. Confirmación de especificaciones

Se registran y confirman las características solicitadas por el cliente, incluyendo:

- Producto o diseño.
- Cantidad.
- Color.
- Tamaño.
- Personalización.

### 3. Validación y consulta de stock

El Sistema de Gestión valida los datos del pedido y consulta la disponibilidad de los materiales necesarios.

En este punto se presenta una decisión:

**¿Hay stock/material disponible?**

### 4. Material disponible

Si existe disponibilidad suficiente, el pedido continúa directamente hacia Producción.

### 5. Material no disponible

Si no existe disponibilidad suficiente, Administración y Compras gestiona la adquisición de los materiales necesarios.

Una vez recibidos los materiales, el Sistema de Gestión actualiza la información de stock y el pedido continúa hacia Producción.

### 6. Producción

Producción prepara el trabajo y fabrica el producto de acuerdo con las especificaciones registradas en el pedido.

### 7. Control de calidad

Una vez finalizada la fabricación, se verifica el producto.

El control considera que:

- El color corresponda al solicitado.
- El tamaño sea el indicado.
- El diseño o personalización coincida con el pedido.
- El producto no presente defectos visibles de impresión.
- El acabado sea adecuado.

Se plantea una segunda decisión:

**¿Cumple con las especificaciones del pedido?**

### 8. Producto correcto

Si el producto cumple con las especificaciones, el Sistema de Gestión actualiza el estado del pedido como **Listo**.

Ventas y Atención al Cliente coordina la entrega e informa al cliente.

El cliente recibe el producto y finaliza el proceso.

### 9. Producto incorrecto

Si el producto no cumple con las especificaciones, Producción debe corregir o repetir la fabricación.

Una vez realizada la corrección, el producto vuelve al control de calidad para ser verificado nuevamente.

## 5. Secuencia resumida

```text
Cliente
   ↓
Realiza pedido
   ↓
Ventas y Atención al Cliente
   ↓
Registra pedido y confirma especificaciones
   ↓
Sistema de Gestión
   ↓
Valida datos y consulta stock
   ↓
¿Hay stock/material disponible?
   ├── Sí ───────────────→ Producción
   │                         ↓
   │                    Fabrica producto
   │                         ↓
   │                    Control de calidad
   │                         ↓
   │              ¿Cumple especificaciones?
   │                    ├── Sí → Sistema actualiza "Listo"
   │                    │          ↓
   │                    │       Ventas coordina entrega
   │                    │          ↓
   │                    │       Cliente recibe producto
   │                    │
   │                    └── No → Corregir/Repetir producción
   │                               ↓
   │                         Control de calidad
   │
   └── No → Administración y Compras
              ↓
         Compra materiales
              ↓
         Recibe materiales
              ↓
         Sistema actualiza stock
              ↓
           Producción
```

## 6. Modelado BPMN

El proceso será representado mediante notación **BPMN**, utilizando:

- **Pool** para representar al Cliente y a Render 3D.
- **Lanes** para diferenciar las áreas y funciones internas de Render 3D.
- **Eventos de inicio y fin** para delimitar el proceso.
- **Tareas** para representar las actividades realizadas.
- **Compuertas (gateways)** para representar las decisiones relacionadas con disponibilidad de materiales y control de calidad.
- **Flujos de secuencia** para indicar el orden de las actividades.
- **Flujos de mensaje** para representar la comunicación entre el Cliente y Render 3D.

## 7. Lanes de Render 3D

Dentro del pool de Render 3D se utilizarán las siguientes lanes:

1. **Ventas y Atención al Cliente**
2. **Sistema de Gestión**
3. **Administración y Compras**
4. **Producción**

Esta división permite representar claramente qué área o función interviene en cada actividad del proceso.

## 8. Relación con el sistema de información

El proceso se encuentra directamente relacionado con el sistema de gestión de pedidos, stock y producción definido para Render 3D.

El sistema interviene principalmente en:

- Registro y validación de pedidos.
- Consulta de disponibilidad de materiales.
- Actualización del stock.
- Seguimiento del estado del pedido.
- Actualización del pedido una vez finalizada la producción.

De esta manera, el proceso integra las entidades de datos definidas previamente: **Cliente, Pedido, Producto y Producción**.

## 9. Resultado esperado

El proceso permite realizar un seguimiento ordenado de cada pedido, contemplando tanto la disponibilidad de materiales como el control del producto terminado antes de su entrega al cliente.

El modelado BPMN permitirá visualizar las actividades, responsables, decisiones y posibles caminos alternativos del proceso.

**Fuente:** Trabajo Práctico Integrador y Progresivo N.º 4 — Organización Empresarial.