# TP3 — Estructura Formal y Diseño de Datos

## 1. Estructura formal

La estructura organizacional propuesta para Render 3D ubica a **Dirección** como autoridad máxima.

Debajo de Dirección se encuentran:

- Ventas y Atención al Cliente.
- Producción.
- Administración y Compras.

Dentro de Producción se encuentra:

- Stock y Materiales.

El área de **Sistemas** funciona como unidad de staff y se vincula directamente con Dirección mediante una relación de apoyo.

La línea continua representa autoridad formal y la línea de trazos representa la relación de staff.

## 2. Diccionario de datos preliminar

### Cliente

Representa a la persona o negocio que realiza pedidos.

| Campo | Tipo | Descripción |
|---|---|---|
| `id_cliente` | Integer | Identificador único del cliente. |
| `nombre` | String | Nombre y apellido o razón social. |
| `telefono` | String | Número de contacto, conservando prefijos y formatos. |
| `email` | String | Dirección de correo electrónico de contacto. |

### Pedido

Representa una solicitud registrada por un cliente.

| Campo | Tipo | Descripción |
|---|---|---|
| `id_pedido` | Integer | Identificador único del pedido. |
| `id_cliente` | Integer | Referencia al cliente que realizó el pedido. |
| `fecha_ingreso` | Date | Fecha en que el pedido se registra en el sistema. |
| `fecha_prevista` | Date | Fecha estimada para la entrega solicitada o acordada. |
| `estado` | String | Situación del pedido, por ejemplo pendiente, en producción o entregado. |

### Producto

Representa un producto del catálogo que Render 3D puede fabricar o comercializar.

| Campo | Tipo | Descripción |
|---|---|---|
| `id_producto` | Integer | Identificador único del producto. |
| `nombre` | String | Nombre con el que se identifica el producto. |
| `descripcion` | String | Características funcionales o personalizadas del producto. |
| `material_principal` | String | Material principal requerido para fabricar el producto. |
| `stock_minimo_material` | Decimal | Umbral de referencia para revisar la disponibilidad del material asociado. |

### Producción

Representa el seguimiento de fabricación asociado a un pedido.

| Campo | Tipo | Descripción |
|---|---|---|
| `id_produccion` | Integer | Identificador único del registro de producción. |
| `id_pedido` | Integer | Referencia al pedido cuya fabricación se realiza. |
| `fecha_inicio` | Date | Fecha en que comienza el trabajo de producción. |
| `fecha_fin` | Date | Fecha de finalización; puede quedar sin valor mientras el trabajo siga activo. |
| `estado` | String | Situación de producción, por ejemplo pendiente, en proceso o finalizada. |

## 3. Relaciones funcionales

Las principales relaciones consideradas son:

- Un cliente puede realizar varios pedidos.
- Cada pedido referencia a un cliente.
- Un pedido puede generar un seguimiento de producción.
- El producto aporta información sobre el material necesario para orientar el control de existencias.

Estas relaciones constituyen una base preliminar para continuar con el diseño técnico de la base de datos.

## 4. Conclusión

La estructura formal organiza las unidades de Render 3D alrededor de Dirección y mantiene la dependencia de Stock y Materiales respecto de Producción. Sistemas se incorpora como staff de apoyo.

El diccionario de datos proporciona una primera definición de las entidades necesarias para el sistema de pedidos, stock y producción, y permite continuar con las etapas posteriores de diseño.

**Fuente:** Trabajo Práctico Integrador N.º 3 — Organización Empresarial.