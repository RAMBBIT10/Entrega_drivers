# ServiStack — Sistema de Gestión de Inventario para Servingeniería

## ¿Qué es este proyecto?

Servingeniería es una empresa dedicada al mantenimiento y montaje de plantas de tratamiento de agua. Hasta ahora, todo el control de su inventario de materiales se ha llevado de forma manual en hojas de Excel, a cargo de una sola persona en la bodega: Diana Marcela González Posada. Esto ha generado descuadres, pérdidas de material y demoras, porque nadie más puede saber con certeza qué hay disponible sin depender de esa persona o de un archivo que se puede perder o desactualizar.

ServiStack es el sistema que resuelve ese problema: una aplicación web y móvil, disponible en la nube, que permite a cualquier empleado consultar el stock en tiempo real, gestionar pedidos, entradas y salidas de material, y asociar ese material a los proyectos de mantenimiento o montaje donde se usa. Todo esto reemplazando el Excel manual por una fuente de información confiable y compartida.

---

## Objetivo del sistema

Permitir a los empleados de Servingeniería consultar el stock de materiales en tiempo real, gestionar pedidos, entradas y salidas de productos, y administrar los proyectos de mantenimiento y montaje, con el fin de reducir los descuadres, pérdidas monetarias y demoras generados por el control manual actual.

### Objetivos específicos

- Registrar, categorizar y consultar productos por nombre, código QR o código de barras.
- Agilizar la gestión de pedidos a proveedores y su recepción.
- Registrar salidas de productos asociadas a proyectos específicos, con trazabilidad de cantidades.
- Dar visibilidad en tiempo real de la disponibilidad de cada producto, sin depender de una sola persona ni de un archivo de Excel.
- Generar alertas automáticas cuando el stock de un producto esté por debajo del mínimo establecido.
- Consultar el historial de pedidos, entradas, salidas y proyectos realizados.

---

## Alcance

### Incluye

- Registro y categorización de productos identificados por código QR o código de barras.
- Gestión de pedidos a proveedores y su recepción mediante entradas de mercancía.
- Registro de salidas de productos asociadas a proyectos específicos.
- Consulta en tiempo real de disponibilidad de productos.
- Notificaciones automáticas de stock bajo y de eventos de pedidos.
- Historial de movimientos: pedidos, entradas, salidas y proyectos.
- Exportación de información a Excel.
- Disponibilidad como aplicación web y aplicación móvil, en la nube.

### No incluye

- Manejo de precios, facturación electrónica o reportes contables para la DIAN.
- Gestión de nómina, ventas o compras a clientes finales.
- Tratamiento especial para productos regulados.
- Niveles de permisos más allá de la distinción entre empleado y administrador. Solo el administrador puede crear y eliminar cuentas de empleado.
- Inactivación o baja de productos, empleados o categorías registradas.

---

## Usuarios del sistema

En el sistema solo existen dos roles de acceso:

| Rol del sistema | Qué puede hacer |
|-----------------|-----------------|
| Empleado | Todo lo operativo: productos, pedidos, entradas, salidas, proyectos, historial, notificaciones y exportación. |
| Administrador | Exactamente lo mismo que el empleado, más crear y eliminar cuentas de empleado. |

### Tipos de personas que usan el sistema

| Tipo de persona | Cómo entra al sistema | Qué hace principalmente |
|-----------------|-----------------------|-------------------------|
| Empleado de inventario | Como Empleado | Maneja productos, pedidos, entradas y consulta de stock en bodega. |
| Empleado de campo | Como Empleado | Registra salidas, trabaja con proyectos y escanea códigos QR o de barras desde el celular. |
| Empleado contable | Como Empleado | Consulta historiales y exporta información a Excel. |
| Empleado administrador del sistema | Como Administrador | Hace todo lo anterior y además crea o elimina cuentas de empleado. |

---

## Requisitos funcionales

### Gestión de empleados

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-01 | Un administrador debe poder crear una cuenta de empleado, indicando nombre, usuario y contraseña de acceso. | Media |
| RU-71 | Un administrador debe poder eliminar la cuenta de un empleado. | Media |
| RU-02 | El sistema debe permitir consultar la información de un empleado específico. | Baja |
| RU-03 | El sistema debe permitir consultar el listado completo de empleados registrados. | Media |
| RU-04 | El sistema debe permitir editar la información de un empleado: nombre y usuario. | Baja |

### Gestión de productos

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-05 | El empleado debe poder registrar un nuevo producto especificando nombre, categoría, código QR o código de barras, y cantidad mínima de stock. | Alta |
| RU-06 | El empleado debe poder consultar el detalle y la disponibilidad actual de un producto específico en tiempo real. | Alta |
| RU-07 | El empleado debe poder consultar el detalle de un producto escaneando su código QR o de barras con la cámara del dispositivo. | Alta |
| RU-08 | El empleado debe poder consultar el listado completo de productos. | Media |
| RU-09 | El empleado debe poder consultar productos filtrando por nombre. | Media |
| RU-10 | El empleado debe poder consultar productos filtrando por categoría. | Media |
| RU-11 | El empleado debe poder editar la información de un producto ya registrado: nombre, categoría, código QR o de barras, cantidad mínima de stock. | Alta |

### Gestión de categorías de producto

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-12 | El sistema debe permitir crear una categoría de producto, indicando su nombre. | Media |
| RU-13 | El sistema debe permitir consultar el listado completo de categorías de producto. | Media |
| RU-14 | El sistema debe permitir editar el nombre de una categoría de producto ya existente. | Baja |

### Gestión de pedidos

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-15 | El empleado debe poder crear un pedido, indicando el proveedor al cual se le solicita la mercancía. | Alta |
| RU-16 | El empleado debe poder consultar el detalle de un pedido específico. | Alta |
| RU-17 | El empleado debe poder consultar el listado completo de pedidos. | Alta |
| RU-18 | El empleado debe poder consultar pedidos filtrando por estado. | Media |
| RU-19 | El empleado debe poder editar un pedido mientras no tenga entradas asociadas. | Media |
| RU-20 | El empleado debe poder cancelar un pedido. | Media |

### Gestión de entradas

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-21 | El empleado debe poder registrar una entrada de mercancía asociada a un pedido existente, indicando los productos recibidos y la cantidad de cada uno. | Alta |
| RU-22 | El empleado debe poder registrar una entrada de mercancía que no proviene de un pedido formal, indicando el tipo de entrada y los productos involucrados. | Media |
| RU-23 | El empleado debe poder consultar el detalle de una entrada específica, incluyendo el estado de cada producto dentro de ella. | Alta |
| RU-24 | El empleado debe poder consultar el listado completo de entradas. | Alta |
| RU-25 | El empleado debe poder consultar entradas filtrando por estado. | Media |
| RU-26 | El empleado debe poder editar los datos de una entrada o de una línea de producto dentro de ella, mientras no esté marcada como completada. | Media |
| RU-27 | El empleado debe poder marcar como completada la línea de un producto dentro de una entrada, una vez confirmada su llegada física. | Alta |
| RU-28 | El empleado que registra la entrada de mercancía puede ser distinto del empleado que generó el pedido asociado. | Media |

### Gestión de proyectos

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-29 | El empleado debe poder crear un proyecto de mantenimiento o montaje, indicando su nombre y descripción. | Alta |
| RU-30 | El empleado debe poder asignar uno o varios empleados a un proyecto, indicando su tipo de participación. | Media |
| RU-31 | El empleado debe poder consultar el detalle de un proyecto específico, incluyendo los empleados asignados y las salidas registradas. | Alta |
| RU-32 | El empleado debe poder consultar el listado completo de proyectos. | Media |
| RU-33 | El empleado debe poder consultar proyectos filtrando por estado. | Media |
| RU-65 | El empleado debe poder consultar proyectos filtrando por nombre. | Media |
| RU-34 | El empleado debe poder editar los datos de un proyecto mientras esté en curso. | Media |
| RU-35 | El empleado debe poder finalizar o cancelar un proyecto. | Media |
| RU-36 | El empleado debe poder reasignar o retirar a un empleado de un proyecto. | Baja |

### Gestión de salidas

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-37 | El empleado debe poder registrar la salida de productos asociada a un proyecto específico, indicando el producto y la cantidad de cada uno. | Alta |
| RU-69 | El empleado debe poder agregar un producto a una salida escaneando su código QR o código de barras con la cámara del dispositivo. | Alta |
| RU-70 | El empleado debe poder agregar un producto a una salida buscándolo por nombre. | Alta |
| RU-38 | El empleado debe poder consultar con certeza cuántos productos y en qué cantidad se han usado en un proyecto específico. | Alta |
| RU-39 | El empleado debe poder consultar el detalle de una salida específica, incluyendo el estado de cada producto dentro de ella. | Media |
| RU-40 | El empleado debe poder consultar el listado completo de salidas. | Media |
| RU-41 | El empleado debe poder consultar salidas filtrando por estado. | Media |
| RU-42 | El empleado debe poder editar los datos de una salida o de una línea de producto dentro de ella, mientras no esté marcada como completada. | Media |
| RU-43 | El empleado debe poder cancelar una salida. | Baja |

### Módulo de historial

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-44 | El empleado debe poder consultar el historial de pedidos realizados, incluyendo cada cambio de estado registrado. | Media |
| RU-66 | El empleado debe poder consultar el historial de pedidos dentro de un rango de fechas específico. | Media |
| RU-45 | El empleado debe poder consultar el historial de entradas realizadas, incluyendo el detalle de los productos recibidos y cada cambio de estado. | Media |
| RU-67 | El empleado debe poder consultar el historial de entradas dentro de un rango de fechas específico. | Media |
| RU-46 | El empleado debe poder consultar el historial de salidas realizadas, incluyendo el detalle de los productos entregados y cada cambio de estado. | Media |
| RU-68 | El empleado debe poder consultar el historial de salidas dentro de un rango de fechas específico. | Media |
| RU-47 | El empleado debe poder consultar el historial de proyectos, incluyendo cada cambio de estado. | Baja |

### Módulo de notificaciones

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-48 | El sistema debe notificar automáticamente al empleado cuando el stock de un producto caiga por debajo del mínimo establecido. | Media |
| RU-49 | El sistema debe notificar al empleado responsable cuando se cree un nuevo pedido. | Baja |
| RU-50 | El sistema debe notificar al empleado responsable cuando un pedido cambie de estado. | Baja |
| RU-51 | El empleado debe poder consultar el listado de notificaciones de producto y de pedido recibidas. | Media |
| RU-52 | El empleado debe poder marcar una notificación como leída. | Media |

### Gestión de catálogos

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-53 | El sistema debe permitir crear, consultar y editar tipos de entrada. | Media |
| RU-54 | El sistema debe permitir crear, consultar y editar tipos de participación de un empleado dentro de un proyecto. | Baja |
| RU-55 | El sistema debe permitir crear, consultar y editar tipos de notificación de producto y de pedido. | Baja |

### Acceso al sistema

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-56 | El empleado debe poder iniciar sesión con usuario y contraseña para acceder al sistema. | Alta |

### Exportación de información a Excel

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-57 | El empleado debe poder exportar el historial de pedidos a un archivo Excel. | Media |
| RU-58 | El empleado debe poder exportar el historial de entradas, incluyendo el detalle de productos por entrada, a un archivo Excel. | Media |
| RU-59 | El empleado debe poder exportar el historial de salidas, incluyendo el detalle de productos por salida, a un archivo Excel. | Media |
| RU-60 | El empleado debe poder exportar el listado de proyectos junto con los productos y cantidades utilizadas en cada uno, a un archivo Excel. | Media |
| RU-61 | El empleado debe poder exportar el inventario actual de productos a un archivo Excel. | Media |

### Funcionalidades de valor diferencial

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RU-62 | El empleado debe poder consultar, al ingresar al sistema, un resumen general con los productos en stock bajo y los proyectos actualmente en curso. | Media |
| RU-63 | El empleado debe poder escanear el código QR o de barras de un producto para agregarlo directamente a una entrada en curso. | Alta |
| RU-64 | El empleado debe poder consultar el listado de proyectos en los que participa un empleado específico. | Baja |

---

## Requisitos no funcionales

| Código | Descripción | Prioridad |
|--------|-------------|-----------|
| RNU-01 | El sistema debe estar disponible en la nube, tanto como aplicación web como aplicación móvil. | Alta |
| RNU-02 | Las consultas de productos, pedidos, entradas y salidas deben responder en un tiempo aproximado menor a 1.5 segundos. | Alta |
| RNU-03 | El sistema debe permitir usar la cámara del dispositivo móvil para leer códigos QR o de barras al registrar productos, entradas o salidas. | Alta |
| RNU-04 | El sistema debe ser fácil de usar, requiriendo una capacitación muy básica para empleados con conocimiento tecnológico limitado. | Alta |
| RNU-05 | El sistema no requiere niveles de seguridad avanzados ni manejo de información de pago, ya que solo será usado internamente por los empleados. | Media |
| RNU-06 | El sistema debe restringir la creación y eliminación de cuentas de empleado exclusivamente al administrador. El resto de las funcionalidades estarán disponibles por igual para todos los usuarios. | Alta |

---

## Requisitos de información

| Código | Entidad | Datos que maneja |
|--------|---------|------------------|
| RI01 | Empleado | Nombre, usuario, contraseña. |
| RI02 | Producto | Nombre, categoría, código QR o de barras, cantidad mínima de stock, stock actual. |
| RI03 | Categoría de producto | Nombre. |
| RI04 | Pedido | Proveedor, estado. |
| RI05 | Entrada | Pedido asociado si aplica, tipo de entrada, productos y cantidades, estado general y por línea de producto. |
| RI06 | Proyecto | Nombre, descripción, empleados asignados con su tipo de participación, estado, salidas asociadas. |
| RI07 | Salida | Proyecto asociado, productos y cantidades, estado general y por línea de producto. |
| RI08 | Notificación | Tipo, estado de lectura. |
| RI09 | Historial | Registro de cambios de estado de pedidos, entradas, salidas y proyectos. |
| RI10 | Catálogos | Tipo de entrada, tipo de participación en proyecto, tipo de notificación. |

---

## Atributos de calidad priorizados

| Prioridad | Atributo | Puntaje total | Ponderado global | Por qué importa |
|-----------|----------|---------------|------------------|-----------------|
| 1 | Rendimiento | 22 | 0.2619 | El stock tiene que responder rápido. Si alguien pregunta si hay material disponible, no puede esperar. |
| 2 | Disponibilidad | 17 | 0.2024 | Si el sistema se cae seguido, vuelven al Excel. Se busca alta disponibilidad en horario laboral. |
| 3 | Seguridad | 14 | 0.1667 | Login con usuario y contraseña, contraseñas cifradas, y solo el administrador crea o elimina cuentas. |
| 3 | Integridad | 14 | 0.1667 | El stock debe ser exacto. No puede haber descuadres por salidas concurrentes o estados inconsistentes. |
| 5 | Usabilidad | 11 | 0.1310 | Empleados de bodega y de campo con poco conocimiento técnico. La interfaz debe ser clara. |
| 6 | Modificabilidad | 6 | 0.0714 | Hay reglas de negocio aún pendientes de definir. El sistema va a seguir cambiando. |

### Escenarios más votados

| Código | Atributo | Escenario | Inventario | Admin | Campo | Contable | Total |
|--------|----------|-----------|------------|-------|-------|----------|-------|
| ESC-CAL-INTG-0007 | Integridad | Salida válida asociada a proyecto | 2 | 0 | 2 | 0 | 4 |
| ESC-CAL-INTG-0008 | Integridad | Salida rechazada por stock insuficiente | 2 | 0 | 2 | 0 | 4 |
| ESC-CAL-REN-0005 | Rendimiento | Registro de salida confirmado en menos de 1.5 segundos | 2 | 0 | 2 | 0 | 4 |
| ESC-CAL-DIS-0001 | Disponibilidad | Disponibilidad del sistema en horario laboral | 0 | 0 | 3 | 0 | 3 |
| ESC-CAL-DIS-0002 | Disponibilidad | Acceso al sistema desde web y móvil | 0 | 0 | 3 | 0 | 3 |
| ESC-CAL-INTG-0003 | Integridad | Consulta de stock actualizado | 3 | 0 | 0 | 0 | 3 |
| ESC-CAL-REN-0001 | Rendimiento | Consulta de stock en menos de 1 segundo | 3 | 0 | 0 | 0 | 3 |
| ESC-CAL-REN-0007 | Rendimiento | Exportación de historial de pedidos con datos | 0 | 0 | 0 | 3 | 3 |
| ESC-CAL-REN-0013 | Rendimiento | Exportación de proyectos con datos | 0 | 0 | 0 | 3 | 3 |
| ESC-CAL-REN-0015 | Rendimiento | Exportación de inventario actual con datos | 0 | 0 | 0 | 3 | 3 |
| ESC-CAL-SEG-0007 | Seguridad | Administrador crea una cuenta de empleado | 0 | 3 | 0 | 0 | 3 |
| ESC-CAL-SEG-0011 | Seguridad | Intento de modificación libre de TipoEmpleado | 0 | 3 | 0 | 0 | 3 |
| ESC-CAL-USA-0003 | Usabilidad | Consulta de producto mediante código válido | 0 | 0 | 3 | 0 | 3 |
| ESC-CAL-USA-0006 | Usabilidad | Agregar producto a salida por escaneo | 1 | 0 | 2 | 0 | 3 |
| ESC-CAL-INTG-0005 | Integridad | Registro de entrada asociado a pedido válido | 2 | 0 | 0 | 0 | 2 |

---

## Caracterización de atributos de calidad

### Seguridad

| Código Característica | Descripción característica | Categoría | Código de escenario | Descripción Escenario |
|-----------------------|----------------------------|-----------|---------------------|-----------------------|
| CAR-SEG-0001 | El sistema debe validar la identidad del empleado antes de permitir el acceso a las funciones del inventario. | Autenticación | ESC-CAL-SEG-0001 | Inicio de sesión exitoso |
|  |  |  | ESC-CAL-SEG-0002 | Inicio de sesión rechazado por credenciales incorrectas |
| CAR-SEG-0002 | El sistema debe emitir un token de autenticación solamente después de una autenticación exitosa. | Autenticación | ESC-CAL-SEG-0003 | Generación de token tras login exitoso |
|  |  |  | ESC-CAL-SEG-0004 | No generación de token ante login fallido |
| CAR-SEG-0003 | La sesión del empleado debe manejarse mediante un token con expiración para evitar sesiones indefinidas. | Gestión de sesión | ESC-CAL-SEG-0005 | Expiración de una sesión |
| CAR-SEG-0004 | Las contraseñas de los empleados deben almacenarse cifradas y no como texto legible. | Confidencialidad | ESC-CAL-SEG-0006 | Almacenamiento protegido de contraseñas |
| CAR-SEG-0005 | La creación de cuentas de empleado debe estar restringida exclusivamente a usuarios de tipo Administrador. | Autorización | ESC-CAL-SEG-0007 | Administrador crea una cuenta de empleado |
|  |  |  | ESC-CAL-SEG-0008 | Empleado intenta crear una cuenta |
| CAR-SEG-0006 | La eliminación física de cuentas de empleado debe estar restringida exclusivamente a usuarios de tipo Administrador. | Autorización | ESC-CAL-SEG-0009 | Administrador elimina una cuenta de empleado |
|  |  |  | ESC-CAL-SEG-0010 | Empleado intenta eliminar una cuenta |
| CAR-SEG-0007 | El catálogo TipoEmpleado no debe quedar abierto a edición libre para evitar escalamiento de privilegios. | Autorización | ESC-CAL-SEG-0011 | Intento de modificación libre de TipoEmpleado |
| CAR-SEG-0008 | La recuperación de contraseña debe evitar revelar si un correo está registrado y debe aceptar únicamente enlaces o códigos válidos y vigentes. | Recuperación de credenciales | ESC-CAL-SEG-0012 | Solicitud de recuperación con correo registrado |
|  |  |  | ESC-CAL-SEG-0013 | Solicitud de recuperación con correo no registrado |
|  |  |  | ESC-CAL-SEG-0014 | Restablecimiento con código válido |
|  |  |  | ESC-CAL-SEG-0015 | Restablecimiento con código inválido o vencido |

### Integridad

| Código Característica | Descripción característica | Categoría | Código de escenario | Descripción Escenario |
|-----------------------|----------------------------|-----------|---------------------|-----------------------|
| CAR-INTG-0001 | La creación de productos debe validar los datos obligatorios y establecer el stock inicial en cero. | Validación de datos | ESC-CAL-INTG-0001 | Creación válida de producto |
|  |  |  | ESC-CAL-INTG-0002 | Producto rechazado por campo obligatorio faltante |
| CAR-INTG-0002 | La consulta de un producto debe mostrar su stock actual correspondiente al estado vigente del inventario. | Consistencia de inventario | ESC-CAL-INTG-0003 | Consulta de stock actualizado |
|  |  |  | ESC-CAL-INTG-0004 | Consulta de producto inexistente |
| CAR-INTG-0003 | Toda entrada debe quedar asociada obligatoriamente a un pedido existente y contener un tipo de entrada y al menos una línea válida. | Reglas de negocio | ESC-CAL-INTG-0005 | Registro de entrada asociado a pedido válido |
|  |  |  | ESC-CAL-INTG-0006 | Entrada rechazada por pedido inexistente o cantidad inválida |
| CAR-INTG-0004 | Toda salida debe asociarse a un proyecto y validar el stock antes de registrar el movimiento. | Reglas de negocio | ESC-CAL-INTG-0007 | Salida válida asociada a proyecto |
|  |  |  | ESC-CAL-INTG-0008 | Salida rechazada por stock insuficiente |
| CAR-INTG-0005 | El cambio de estado de un pedido debe ser manual y no derivarse del estado de sus entradas. | Estados manuales | ESC-CAL-INTG-0009 | Cambio manual válido de estado de pedido |
|  |  |  | ESC-CAL-INTG-0010 | Estado de pedido fuera del catálogo |
|  |  |  | ESC-CAL-INTG-0011 | Pedido completado con elementos hijos cancelados |
| CAR-INTG-0006 | El cambio de estado de una entrada y de sus líneas debe ser manual e independiente. | Estados manuales | ESC-CAL-INTG-0012 | Cambio manual válido del estado de una entrada |
|  |  |  | ESC-CAL-INTG-0013 | Entrada completada con una línea cancelada |
|  |  |  | ESC-CAL-INTG-0014 | Cambio manual válido del estado de una línea de entrada |
|  |  |  | ESC-CAL-INTG-0015 | Estado inválido para línea de entrada |
| CAR-INTG-0007 | El cambio de estado de una salida debe aceptar únicamente estados válidos y conservar el estado actual cuando el cambio es rechazado. | Estados manuales | ESC-CAL-INTG-0016 | Cambio de estado inválido de una salida |
|  |  |  | ESC-CAL-INTG-0017 | Salida completada con línea cancelada |
|  |  |  | ESC-CAL-INTG-0018 | Cambio manual válido de línea de salida |
|  |  |  | ESC-CAL-INTG-0019 | Estado inválido para línea de salida |
| CAR-INTG-0008 | El estado de un proyecto debe cambiarse manualmente y no derivarse del estado de sus salidas. | Estados manuales | ESC-CAL-INTG-0020 | Cambio manual válido de estado de proyecto |
|  |  |  | ESC-CAL-INTG-0021 | Proyecto completado con salida cancelada |
| CAR-INTG-0009 | El estado actual de cada entidad debe corresponder al registro de estado con la fecha más reciente. | Consistencia temporal | ESC-CAL-INTG-0022 | Determinación del estado actual |
| CAR-INTG-0010 | La edición de entradas o líneas completadas debe estar restringida. | Control de modificación | ESC-CAL-INTG-0023 | Edición de línea de entrada no completada |
|  |  |  | ESC-CAL-INTG-0024 | Edición bloqueada de línea de entrada completada |
| CAR-INTG-0011 | La edición de salidas o líneas completadas debe estar restringida. | Control de modificación | ESC-CAL-INTG-0025 | Edición de línea de salida no completada |
|  |  |  | ESC-CAL-INTG-0026 | Edición bloqueada de línea de salida completada |
| CAR-INTG-0012 | La edición de un proyecto debe permitirse únicamente mientras el proyecto esté en curso. | Control de modificación | ESC-CAL-INTG-0027 | Edición de proyecto en curso |
|  |  |  | ESC-CAL-INTG-0028 | Edición bloqueada de proyecto completado o cancelado |
| CAR-INTG-0013 | La asignación de empleados a proyectos debe evitar duplicados para el mismo proyecto. | Consistencia de relaciones | ESC-CAL-INTG-0029 | Asignación válida de empleado a proyecto |
|  |  |  | ESC-CAL-INTG-0030 | Asignación duplicada rechazada |
| CAR-INTG-0014 | Las notificaciones automáticas deben generarse de manera coherente con los eventos de negocio definidos. | Consistencia de notificaciones | ESC-CAL-INTG-0031 | Notificación por stock bajo |
|  |  |  | ESC-CAL-INTG-0032 | Sin notificación cuando el stock permanece sobre el mínimo |
|  |  |  | ESC-CAL-INTG-0033 | Notificación por creación de pedido |
|  |  |  | ESC-CAL-INTG-0034 | Pedido rechazado sin notificación de creación |
|  |  |  | ESC-CAL-INTG-0035 | Notificación por cambio de estado de pedido |
| CAR-INTG-0015 | El sistema debe conservar y mostrar todos los cambios de estado de cada pedido ordenados por fecha. | Historial de estados | ESC-CAL-INTG-0036 | Consulta del historial de un pedido |
| CAR-INTG-0016 | El historial de pedidos debe poder consultarse dentro de un rango de fechas válido. | Consulta temporal | ESC-CAL-INTG-0037 | Consulta de pedidos por rango válido |
|  |  |  | ESC-CAL-INTG-0038 | Rango de fechas inválido en historial de pedidos |
| CAR-INTG-0017 | El sistema debe conservar el historial de entradas con sus productos recibidos y cambios de estado. | Historial de movimientos | ESC-CAL-INTG-0039 | Consulta del historial de una entrada |
|  |  |  | ESC-CAL-INTG-0040 | Consulta de entradas por rango inválido |
|  |  |  | ESC-CAL-INTG-0041 | Consulta de entradas por rango válido |
| CAR-INTG-0018 | El sistema debe conservar el historial de salidas con productos entregados y cambios de estado. | Historial de movimientos | ESC-CAL-INTG-0042 | Consulta del historial de una salida |
|  |  |  | ESC-CAL-INTG-0043 | Consulta de salidas por rango válido |
|  |  |  | ESC-CAL-INTG-0044 | Consulta de salidas por rango inválido |
| CAR-INTG-0019 | El sistema debe conservar el historial de proyectos con cada cambio de estado. | Historial de estados | ESC-CAL-INTG-0045 | Consulta del historial de proyecto |
| CAR-INTG-0020 | El sistema debe calcular la cantidad total usada de cada producto dentro de un proyecto a partir de sus salidas. | Trazabilidad de materiales | ESC-CAL-INTG-0046 | Cálculo de materiales usados por proyecto |
| CAR-INTG-0021 | Las notificaciones generadas por eventos de negocio deben conservar correspondencia con el evento que las origina y enviarse mediante el servicio de notificaciones definido. | Consistencia de notificaciones | ESC-CAL-INTG-0047 | Envío consistente de notificación al servicio push |

### Modificabilidad

| Código Característica | Descripción característica | Categoría | Código de escenario | Descripción Escenario |
|-----------------------|----------------------------|-----------|---------------------|-----------------------|
| CAR-MOD-0001 | TipoEstado debe poder ampliarse o editarse para Pedido sin afectar la lógica manual del módulo. | TipoEstado | ESC-CAL-MOD-0001 | Agregar o editar TipoEstado para Pedido |
|  |  |  | ESC-CAL-MOD-0002 | TipoEstado inválido o duplicado para Pedido |
| CAR-MOD-0002 | TipoEstado debe poder ampliarse o editarse para Entrada sin afectar la lógica manual del módulo. | TipoEstado | ESC-CAL-MOD-0003 | Agregar o editar TipoEstado para Entrada |
|  |  |  | ESC-CAL-MOD-0004 | TipoEstado inválido o duplicado para Entrada |
| CAR-MOD-0003 | TipoEstado debe poder ampliarse o editarse para EntradaProducto sin afectar la confirmación por línea. | TipoEstado | ESC-CAL-MOD-0005 | Agregar o editar TipoEstado para EntradaProducto |
|  |  |  | ESC-CAL-MOD-0006 | TipoEstado inválido o duplicado para EntradaProducto |
| CAR-MOD-0004 | TipoEstado debe poder ampliarse o editarse para Salida sin afectar la lógica manual del módulo. | TipoEstado | ESC-CAL-MOD-0007 | Agregar o editar TipoEstado para Salida |
|  |  |  | ESC-CAL-MOD-0008 | TipoEstado inválido o duplicado para Salida |
| CAR-MOD-0005 | TipoEstado debe poder ampliarse o editarse para SalidaProducto sin afectar la confirmación por línea. | TipoEstado | ESC-CAL-MOD-0009 | Agregar o editar TipoEstado para SalidaProducto |
|  |  |  | ESC-CAL-MOD-0010 | TipoEstado inválido o duplicado para SalidaProducto |
| CAR-MOD-0006 | TipoEstado debe poder ampliarse o editarse para Proyecto sin afectar la lógica manual del módulo. | TipoEstado | ESC-CAL-MOD-0011 | Agregar o editar TipoEstado para Proyecto |
|  |  |  | ESC-CAL-MOD-0012 | TipoEstado inválido o duplicado para Proyecto |
| CAR-MOD-0007 | El catálogo de tipos de entrada debe poder crearse, consultarse y editarse sin requerir cambios en la estructura de una entrada. | Catálogos configurables | ESC-CAL-MOD-0013 | Creación o edición válida de TipoEntrada |
|  |  |  | ESC-CAL-MOD-0014 | TipoEntrada vacío o duplicado |
| CAR-MOD-0008 | Los tipos de participación en proyecto deben poder crearse, consultarse y editarse como catálogo independiente. | Catálogos configurables | ESC-CAL-MOD-0015 | Creación o edición válida de tipo de participación |
|  |  |  | ESC-CAL-MOD-0016 | Tipo de participación vacío o duplicado |
| CAR-MOD-0009 | Los tipos de notificación de producto y pedido deben poder crearse, consultarse y editarse independientemente. | Catálogos configurables | ESC-CAL-MOD-0017 | Creación o edición válida de tipo de notificación |
|  |  |  | ESC-CAL-MOD-0018 | Tipo de notificación vacío o duplicado |

### Rendimiento

| Código Característica | Descripción característica | Categoría | Código de escenario | Descripción Escenario |
|-----------------------|----------------------------|-----------|---------------------|-----------------------|
| CAR-REN-0001 | El sistema debe responder a la consulta del stock de un producto específico en menos de 1 segundo bajo condiciones normales de uso. | Consulta de inventario | ESC-CAL-REN-0001 | Consulta de stock en menos de 1 segundo |
| CAR-REN-0002 | El sistema debe responder a la consulta del listado completo de productos en menos de 1.5 segundos bajo condiciones normales de uso. | Consulta de inventario | ESC-CAL-REN-0002 | Consulta del listado de productos en menos de 1.5 segundos |
| CAR-REN-0003 | El sistema debe confirmar el registro de un pedido en menos de 1.5 segundos bajo condiciones normales de uso. | Registro de movimientos | ESC-CAL-REN-0003 | Registro de pedido confirmado en menos de 1.5 segundos |
| CAR-REN-0004 | El sistema debe confirmar el registro de una entrada en menos de 1.5 segundos bajo condiciones normales de uso. | Registro de movimientos | ESC-CAL-REN-0004 | Registro de entrada confirmado en menos de 1.5 segundos |
| CAR-REN-0005 | El sistema debe confirmar el registro de una salida en menos de 1.5 segundos bajo condiciones normales de uso. | Registro de movimientos | ESC-CAL-REN-0005 | Registro de salida confirmado en menos de 1.5 segundos |
| CAR-REN-0006 | El sistema debe responder a la consulta del historial de pedidos, entradas o salidas en menos de 1.5 segundos bajo condiciones normales de uso. | Consulta histórica | ESC-CAL-REN-0006 | Consulta de historial en menos de 1.5 segundos |
| CAR-REN-0007 | El sistema debe generar la exportación del historial de pedidos en formato Excel en menos de 1.5 segundos. | Exportación de información | ESC-CAL-REN-0007 | Exportación de historial de pedidos con datos |
|  |  |  | ESC-CAL-REN-0008 | Exportación de historial de pedidos sin datos |
| CAR-REN-0008 | El sistema debe generar la exportación del historial de entradas en formato Excel en menos de 1.5 segundos. | Exportación de información | ESC-CAL-REN-0009 | Exportación de historial de entradas con datos |
|  |  |  | ESC-CAL-REN-0010 | Exportación de historial de entradas sin datos |
| CAR-REN-0009 | El sistema debe generar la exportación del historial de salidas en formato Excel en menos de 1.5 segundos. | Exportación de información | ESC-CAL-REN-0011 | Exportación de historial de salidas con datos |
|  |  |  | ESC-CAL-REN-0012 | Exportación de historial de salidas sin datos |
| CAR-REN-0010 | El sistema debe generar la exportación de proyectos en formato Excel en menos de 1.5 segundos. | Exportación de información | ESC-CAL-REN-0013 | Exportación de proyectos con datos |
|  |  |  | ESC-CAL-REN-0014 | Exportación de proyectos sin datos |
| CAR-REN-0011 | El sistema debe generar la exportación del inventario actual en formato Excel en menos de 1.5 segundos. | Exportación de información | ESC-CAL-REN-0015 | Exportación de inventario actual con datos |
|  |  |  | ESC-CAL-REN-0016 | Exportación de inventario actual sin datos |

### Disponibilidad

| Código Característica | Descripción característica | Categoría | Código de escenario | Descripción Escenario |
|-----------------------|----------------------------|-----------|---------------------|-----------------------|
| CAR-DIS-0001 | El sistema debe poder funcionar en un 99.999% del tiempo en horario laboral | Continuidad del servicio | ESC-CAL-DIS-0001 | Disponibilidad del sistema en horario laboral |
| CAR-DIS-0002 | El sistema debe permitir el acceso a sus funcionalidades mediante la aplicación web y la aplicación móvil soportada. | Canales de acceso | ESC-CAL-DIS-0002 | Acceso al sistema desde web y móvil |

### Usabilidad

| Código Característica | Descripción característica | Categoría | Código de escenario | Descripción Escenario |
|-----------------------|----------------------------|-----------|---------------------|-----------------------|
| CAR-USA-0001 | La interfaz debe ser comprensible para empleados con conocimiento tecnológico básico y mantener una curva de aprendizaje mínima. | Facilidad de uso | ESC-CAL-USA-0001 | Registro guiado de una entrada |
|  |  |  | ESC-CAL-USA-0002 | Mensaje comprensible ante dato inválido |
| CAR-USA-0002 | La aplicación móvil debe facilitar la consulta y el registro de productos mediante el escaneo de códigos QR con la cámara del dispositivo. | Facilidad de operación | ESC-CAL-USA-0003 | Consulta de producto mediante código válido |
|  |  | Manejo de errores de operación | ESC-CAL-USA-0004 | Código escaneado sin producto asociado |
|  |  | Facilidad de operación | ESC-CAL-USA-0005 | Agregar producto a entrada por escaneo |
|  |  | Facilidad de operación | ESC-CAL-USA-0006 | Agregar producto a salida por escaneo |

---

# Escenarios de Calidad

### ESC-CAL-SEG-0001

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0001 |
| **Nombre** | Inicio de sesión exitoso |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Autenticación |
| **Característica** | El sistema debe validar la identidad del empleado antes de permitir el acceso a las funciones del inventario. |
| **Objetivo** | Comprobar que un empleado registrado pueda autenticarse con credenciales válidas. |
| **Criterios de éxito** | El sistema autentica al empleado y lo redirige a la pantalla principal. |
| **Prerrequisitos** | 1. El empleado existe.<br>2. Usuario y contraseña son correctos.<br>3. El servicio de autenticación está disponible. |
| **Requisito relacionado** | RF-65 / RU-56 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Ingresa usuario y contraseña válidos y selecciona ingresar. | Operación normal | Módulo de autenticación | Valida las credenciales y permite el acceso. | El acceso se concede únicamente cuando las credenciales coinciden con un empleado registrado. |

---

### ESC-CAL-SEG-0002

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0002 |
| **Nombre** | Inicio de sesión rechazado por credenciales incorrectas |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Autenticación |
| **Característica** | El sistema debe validar la identidad del empleado antes de permitir el acceso a las funciones del inventario. |
| **Objetivo** | Evitar el acceso cuando el usuario o la contraseña no son válidos sin revelar cuál dato falló. |
| **Criterios de éxito** | El sistema rechaza el ingreso y muestra un mensaje genérico. |
| **Prerrequisitos** | 1. Se presenta el formulario de login.<br>2. Al menos una credencial es incorrecta. |
| **Requisito relacionado** | RF-65 / RU-56 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Ingresa credenciales incorrectas e intenta iniciar sesión. | Operación con falla en autenticación | Módulo de autenticación | Rechaza la autenticación y mantiene al usuario fuera del sistema. | No se concede acceso y el mensaje no identifica si falló el usuario o la contraseña. |

---

### ESC-CAL-SEG-0003

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0003 |
| **Nombre** | Generación de token tras login exitoso |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Autenticación |
| **Característica** | El sistema debe emitir un token de autenticación solamente después de una autenticación exitosa. |
| **Objetivo** | Asegurar que una sesión válida quede asociada al empleado autenticado. |
| **Criterios de éxito** | Se genera un token válido asociado al empleado. |
| **Prerrequisitos** | 1. Las credenciales fueron validadas correctamente. |
| **Requisito relacionado** | RF-66 / RU-56 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Completa correctamente la validación de credenciales. | Operación normal | Módulo de autenticación | Emite un token asociado al empleado autenticado. | Todo login exitoso produce un token válido asociado al empleado. |

---

### ESC-CAL-SEG-0004

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0004 |
| **Nombre** | No generación de token ante login fallido |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Autenticación |
| **Característica** | El sistema debe emitir un token de autenticación solamente después de una autenticación exitosa. |
| **Objetivo** | Impedir que un intento de autenticación fallido produzca una sesión válida. |
| **Criterios de éxito** | No se genera token alguno. |
| **Prerrequisitos** | 1. La validación de credenciales ha fallado. |
| **Requisito relacionado** | RF-66 / RU-56 |
| **Tipo de escenario** | Restricción |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Recibe un resultado de login fallido. | Operación con falla en autenticación | Módulo de autenticación | Finaliza el intento sin emitir token. | La respuesta de autenticación fallida no contiene un token válido. |

---

### ESC-CAL-SEG-0005

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0005 |
| **Nombre** | Expiración de una sesión |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Gestión de sesión |
| **Característica** | La sesión del empleado debe manejarse mediante un token con expiración para evitar sesiones indefinidas. |
| **Objetivo** | Asegurar que un token vencido no permita continuar ejecutando operaciones protegidas. |
| **Criterios de éxito** | El sistema exige una nueva autenticación cuando el token ha expirado. |
| **Prerrequisitos** | 1. El empleado inició sesión.<br>2. El token tiene expiración configurada.<br>3. El token ya venció. |
| **Requisito relacionado** | RNF-10 |
| **Tipo de escenario** | Restricción |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta ejecutar una operación protegida con un token expirado. | Operación con falla en gestión de sesión | Módulo de autenticación | Rechaza la sesión vencida y solicita autenticación nuevamente. | Ninguna operación protegida se ejecuta usando un token vencido. |

---

### ESC-CAL-SEG-0006

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0006 |
| **Nombre** | Almacenamiento protegido de contraseñas |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Confidencialidad |
| **Característica** | Las contraseñas de los empleados deben almacenarse cifradas y no como texto legible. |
| **Objetivo** | Evitar que una contraseña quede expuesta en texto legible dentro del almacenamiento del sistema. |
| **Criterios de éxito** | La contraseña persistida no corresponde al texto ingresado por el empleado. |
| **Prerrequisitos** | 1. Se crea o actualiza una contraseña válida. |
| **Requisito relacionado** | RNF-10 |
| **Tipo de escenario** | Restricción |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Persiste la contraseña de una cuenta. | Operación con falla en gestión de credenciales | Módulo de autenticación | Almacena una representación cifrada de la contraseña. | Una revisión del registro persistido no permite obtener la contraseña como texto legible. |

---

### ESC-CAL-SEG-0007

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0007 |
| **Nombre** | Administrador crea una cuenta de empleado |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Autorización |
| **Característica** | La creación de cuentas de empleado debe estar restringida exclusivamente a usuarios de tipo Administrador. |
| **Objetivo** | Permitir que un Administrador registre una nueva cuenta con datos válidos. |
| **Criterios de éxito** | La cuenta queda creada con su TipoEmpleado y se confirma la operación. |
| **Prerrequisitos** | 1. El solicitante está autenticado.<br>2. Su TipoEmpleado es Administrador.<br>3. Los datos son válidos. |
| **Requisito relacionado** | RF-01 / RNF-11 / RN-11 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Administrador | Solicita crear una cuenta de empleado. | Operación normal | Módulo de empleados | Crea la cuenta y muestra confirmación. | La cuenta queda registrada una sola vez con los datos suministrados. |

---

### ESC-CAL-SEG-0008

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0008 |
| **Nombre** | Empleado intenta crear una cuenta |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Autorización |
| **Característica** | La creación de cuentas de empleado debe estar restringida exclusivamente a usuarios de tipo Administrador. |
| **Objetivo** | Impedir que un usuario sin privilegios administrativos cree cuentas. |
| **Criterios de éxito** | La operación es rechazada y no se crea ningún empleado. |
| **Prerrequisitos** | 1. El solicitante está autenticado como Empleado. |
| **Requisito relacionado** | RF-01 / RNF-11 / RN-11 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta crear una cuenta de empleado. | Operación con falla en gestión de empleados | Módulo de empleados | Bloquea la operación y muestra un mensaje de permisos insuficientes. | La cantidad de cuentas permanece sin cambios. |

---

### ESC-CAL-SEG-0009

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0009 |
| **Nombre** | Administrador elimina una cuenta de empleado |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Autorización |
| **Característica** | La eliminación física de cuentas de empleado debe estar restringida exclusivamente a usuarios de tipo Administrador. |
| **Objetivo** | Permitir la baja física de una cuenta cuando la solicita un Administrador. |
| **Criterios de éxito** | El registro del empleado es eliminado y se confirma la operación. |
| **Prerrequisitos** | 1. Administrador autenticado.<br>2. La cuenta objetivo existe. |
| **Requisito relacionado** | RF-02 / RNF-11 / RN-11 / RN-13 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Administrador | Solicita eliminar una cuenta de empleado. | Operación normal | Módulo de empleados | Elimina físicamente el registro y confirma la acción. | La cuenta deja de existir como registro activo del sistema. |

---

### ESC-CAL-SEG-0010

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0010 |
| **Nombre** | Empleado intenta eliminar una cuenta |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Autorización |
| **Característica** | La eliminación física de cuentas de empleado debe estar restringida exclusivamente a usuarios de tipo Administrador. |
| **Objetivo** | Impedir que un usuario no administrador elimine cuentas. |
| **Criterios de éxito** | El sistema rechaza la operación y conserva la cuenta. |
| **Prerrequisitos** | 1. Usuario autenticado como Empleado.<br>2. La cuenta objetivo existe. |
| **Requisito relacionado** | RF-02 / RNF-11 / RN-11 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita eliminar una cuenta. | Operación con falla en gestión de empleados | Módulo de empleados | Bloquea la acción y muestra permisos insuficientes. | La cuenta objetivo permanece registrada sin cambios. |

---

### ESC-CAL-SEG-0011

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0011 |
| **Nombre** | Intento de modificación libre de TipoEmpleado |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Autorización |
| **Característica** | El catálogo TipoEmpleado no debe quedar abierto a edición libre para evitar escalamiento de privilegios. |
| **Objetivo** | Evitar que un usuario pueda modificar libremente el catálogo que determina privilegios. |
| **Criterios de éxito** | El sistema no permite una modificación libre del catálogo TipoEmpleado. |
| **Prerrequisitos** | 1. Existe un usuario autenticado.<br>2. Se intenta acceder a una edición no autorizada del catálogo. |
| **Requisito relacionado** | RN-12 |
| **Tipo de escenario** | Restricción |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta crear o modificar libremente valores de TipoEmpleado. | Operación con falla en gestión de roles de empleado | Módulo de empleados | Impide la edición libre del catálogo. | No se modifica TipoEmpleado mediante una operación de edición libre; el mecanismo exacto de administración está pendiente de definición. |

---

### ESC-CAL-SEG-0012

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0012 |
| **Nombre** | Solicitud de recuperación con correo registrado |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Recuperación de credenciales |
| **Característica** | La recuperación de contraseña debe evitar revelar si un correo está registrado y debe aceptar únicamente enlaces o códigos válidos y vigentes. |
| **Objetivo** | Permitir que un empleado solicite restablecimiento mediante su correo registrado. |
| **Criterios de éxito** | Se envían instrucciones y se muestra confirmación de solicitud. |
| **Prerrequisitos** | 1. El correo pertenece a un empleado registrado. |
| **Requisito relacionado** | RF-75 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita recuperar la contraseña usando su correo. | Operación normal | Módulo de autenticación | Genera y envía las instrucciones de restablecimiento. | Se muestra la confirmación definida y se inicia el proceso de recuperación. |

---

### ESC-CAL-SEG-0013

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0013 |
| **Nombre** | Solicitud de recuperación con correo no registrado |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Recuperación de credenciales |
| **Característica** | La recuperación de contraseña debe evitar revelar si un correo está registrado y debe aceptar únicamente enlaces o códigos válidos y vigentes. |
| **Objetivo** | Evitar la enumeración de cuentas durante la recuperación de contraseña. |
| **Criterios de éxito** | Se muestra el mismo mensaje de confirmación usado para un correo registrado. |
| **Prerrequisitos** | 1. El correo no pertenece a ninguna cuenta. |
| **Requisito relacionado** | RF-75 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita recuperar contraseña con un correo no registrado. | Operación con falla en recuperación de contraseña | Módulo de autenticación | No revela si el correo existe y muestra el mensaje genérico de solicitud. | La respuesta visible no permite distinguir entre correo registrado y no registrado. |

---

### ESC-CAL-SEG-0014

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0014 |
| **Nombre** | Restablecimiento con código válido |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Recuperación de credenciales |
| **Característica** | La recuperación de contraseña debe evitar revelar si un correo está registrado y debe aceptar únicamente enlaces o códigos válidos y vigentes. |
| **Objetivo** | Permitir establecer una nueva contraseña usando un enlace o código vigente. |
| **Criterios de éxito** | La contraseña se actualiza y se confirma el cambio. |
| **Prerrequisitos** | 1. El enlace o código es válido y vigente. |
| **Requisito relacionado** | RF-76 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Envía una nueva contraseña con un enlace o código válido. | Operación normal | Módulo de autenticación | Actualiza la contraseña y confirma la operación. | La nueva contraseña queda registrada y el código utilizado deja de ser necesario para completar el cambio. |

---

### ESC-CAL-SEG-0015

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-SEG-0015 |
| **Nombre** | Restablecimiento con código inválido o vencido |
| **Atributo de calidad** | Seguridad |
| **Categoría** | Recuperación de credenciales |
| **Característica** | La recuperación de contraseña debe evitar revelar si un correo está registrado y debe aceptar únicamente enlaces o códigos válidos y vigentes. |
| **Objetivo** | Impedir cambios de contraseña con credenciales de recuperación inválidas. |
| **Criterios de éxito** | El sistema rechaza la operación y mantiene la contraseña anterior. |
| **Prerrequisitos** | 1. El enlace o código es inválido o vencido. |
| **Requisito relacionado** | RF-76 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta establecer una nueva contraseña. | Operación con falla en recuperación de contraseña | Módulo de autenticación | Rechaza el cambio y muestra un mensaje de error. | La contraseña almacenada no se modifica. |

---
### Integridad

#### ESC-CAL-INTG-0001

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0001 |
| **Nombre** | Creación válida de producto |
| **Atributo de calidad** | Integridad |
| **Categoría** | Validación de datos |
| **Característica** | La creación de productos debe validar los datos obligatorios y establecer el stock inicial en cero. |
| **Objetivo** | Asegurar que un producto completo se registre de forma consistente. |
| **Criterios de éxito** | El producto se crea con stock inicial igual a cero y se confirma la operación. |
| **Prerrequisitos** | 1. Nombre, categoría, código y cantidad mínima están completos. |
| **Requisito relacionado** | RF-06 / RU-05 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Registra un producto con todos los datos obligatorios. | Operación normal | Módulo de inventario | Crea el producto con stock inicial en cero. | El nuevo registro contiene los datos suministrados y stock_actual = 0. |

#### ESC-CAL-INTG-0002

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0002 |
| **Nombre** | Producto rechazado por campo obligatorio faltante |
| **Atributo de calidad** | Integridad |
| **Categoría** | Validación de datos |
| **Característica** | La creación de productos debe validar los datos obligatorios y establecer el stock inicial en cero. |
| **Objetivo** | Evitar productos incompletos en el inventario. |
| **Criterios de éxito** | El sistema no crea el producto e informa el campo faltante. |
| **Prerrequisitos** | 1. Al menos un campo obligatorio está vacío. |
| **Requisito relacionado** | RF-06 / RU-05 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta crear un producto incompleto. | Operación con falla en gestión de productos | Módulo de inventario | Rechaza el registro y muestra error. | No se crea ningún producto parcial. |

#### ESC-CAL-INTG-0003

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0003 |
| **Nombre** | Consulta de stock actualizado |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consistencia de inventario |
| **Característica** | La consulta de un producto debe mostrar su stock actual correspondiente al estado vigente del inventario. |
| **Objetivo** | Verificar que la consulta de un producto refleje su stock actual. |
| **Criterios de éxito** | El sistema retorna el producto y su stock actualizado. |
| **Prerrequisitos** | 1. El producto existe. |
| **Requisito relacionado** | RF-07 / RU-06 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta el detalle de un producto. | Operación normal | Módulo de inventario | Obtiene el detalle y el stock actual. | El valor mostrado coincide con el stock persistido después de los movimientos registrados. |

#### ESC-CAL-INTG-0004

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0004 |
| **Nombre** | Consulta de producto inexistente |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consistencia de inventario |
| **Característica** | La consulta de un producto debe mostrar su stock actual correspondiente al estado vigente del inventario. |
| **Objetivo** | Evitar presentar información de stock para un producto que no existe. |
| **Criterios de éxito** | El sistema informa que el producto no fue encontrado. |
| **Prerrequisitos** | 1. El identificador no corresponde a ningún producto. |
| **Requisito relacionado** | RF-07 / RU-06 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta un producto inexistente. | Operación con falla en gestión de productos | Módulo de inventario | No devuelve un stock ficticio y muestra el mensaje correspondiente. | No se presenta un valor de stock asociado a un producto inexistente. |

#### ESC-CAL-INTG-0005

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0005 |
| **Nombre** | Registro de entrada asociado a pedido válido |
| **Atributo de calidad** | Integridad |
| **Categoría** | Reglas de negocio |
| **Característica** | Toda entrada debe quedar asociada obligatoriamente a un pedido existente y contener un tipo de entrada y al menos una línea válida. |
| **Objetivo** | Mantener la relación obligatoria entre entrada y pedido. |
| **Criterios de éxito** | Se crea la entrada y sus líneas asociadas al pedido. |
| **Prerrequisitos** | 1. Pedido existente.<br>2. Tipo de entrada válido.<br>3. Al menos un producto con cantidad válida. |
| **Requisito relacionado** | RF-22 / RN-01 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Registra una entrada seleccionando pedido, tipo y productos. | Operación normal | Módulo de entradas | Crea entrada y líneas y confirma el registro. | Toda entrada creada contiene exactamente un pedido asociado. |

#### ESC-CAL-INTG-0006

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0006 |
| **Nombre** | Entrada rechazada por pedido inexistente o cantidad inválida |
| **Atributo de calidad** | Integridad |
| **Categoría** | Reglas de negocio |
| **Característica** | Toda entrada debe quedar asociada obligatoriamente a un pedido existente y contener un tipo de entrada y al menos una línea válida. |
| **Objetivo** | Evitar entradas huérfanas o inconsistentes. |
| **Criterios de éxito** | La entrada no se crea. |
| **Prerrequisitos** | 1. El pedido no existe o alguna cantidad es inválida. |
| **Requisito relacionado** | RF-22 / RN-01 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta registrar la entrada. | Operación con falla en gestión de entradas | Módulo de entradas | Rechaza toda la operación y muestra error. | No queda creada ni la entrada ni sus líneas. |

#### ESC-CAL-INTG-0007

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0007 |
| **Nombre** | Salida válida asociada a proyecto |
| **Atributo de calidad** | Integridad |
| **Categoría** | Reglas de negocio |
| **Característica** | Toda salida debe asociarse a un proyecto y validar el stock antes de registrar el movimiento. |
| **Objetivo** | Registrar una salida solo cuando existe proyecto y stock suficiente. |
| **Criterios de éxito** | La salida se crea y el stock disminuye en la misma operación. |
| **Prerrequisitos** | 1. Proyecto válido.<br>2. Productos existentes.<br>3. Cantidades no superiores al stock. |
| **Requisito relacionado** | RF-39 / RN-14 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Registra una salida para un proyecto. | Operación normal | Módulo de salidas | Crea la salida y decrementa el stock. | Toda salida creada referencia un proyecto y el stock resultante refleja las cantidades registradas. |

#### ESC-CAL-INTG-0008

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0008 |
| **Nombre** | Salida rechazada por stock insuficiente |
| **Atributo de calidad** | Integridad |
| **Categoría** | Reglas de negocio |
| **Característica** | Toda salida debe asociarse a un proyecto y validar el stock antes de registrar el movimiento. |
| **Objetivo** | Evitar que el inventario quede con cantidades inválidas. |
| **Criterios de éxito** | La operación se rechaza sin modificar el stock. |
| **Prerrequisitos** | 1. Alguna cantidad solicitada supera el stock actual. |
| **Requisito relacionado** | RF-39 / RU-37 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta registrar una salida con cantidad superior al stock. | Operación con falla en gestión de salidas | Módulo de salidas | Rechaza el registro y conserva el stock previo. | No se crea la salida y ningún stock es decrementado por la operación rechazada. |

#### ESC-CAL-INTG-0009

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0009 |
| **Nombre** | Cambio manual válido de estado de pedido |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El cambio de estado de un pedido debe ser manual y no derivarse del estado de sus entradas. |
| **Objetivo** | Conservar el control manual del estado del pedido. |
| **Criterios de éxito** | Se registra el nuevo estado con confirmación. |
| **Prerrequisitos** | 1. Pedido existente.<br>2. Estado pertenece al catálogo. |
| **Requisito relacionado** | RF-21 / RN-02 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Selecciona manualmente un nuevo estado para el pedido. | Operación normal | Módulo de pedidos | Registra el estado seleccionado. | El estado registrado corresponde exactamente al seleccionado por el empleado. |

#### ESC-CAL-INTG-0010

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0010 |
| **Nombre** | Estado de pedido fuera del catálogo |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El cambio de estado de un pedido debe ser manual y no derivarse del estado de sus entradas. |
| **Objetivo** | Evitar registrar estados no definidos. |
| **Criterios de éxito** | La operación es rechazada. |
| **Prerrequisitos** | 1. El valor no corresponde a un TipoEstado registrado. |
| **Requisito relacionado** | RF-21 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta asignar un estado inválido. | Operación con falla en gestión de pedidos | Módulo de pedidos | Rechaza el cambio y muestra error. | No se agrega un registro de estado inválido. |

#### ESC-CAL-INTG-0011

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0011 |
| **Nombre** | Pedido completado con elementos hijos cancelados |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El cambio de estado de un pedido debe ser manual y no derivarse del estado de sus entradas. |
| **Objetivo** | Respetar la regla que permite completar un pedido aunque existan hijos cancelados. |
| **Criterios de éxito** | El sistema permite registrar Completado sin derivar el estado de sus hijos. |
| **Prerrequisitos** | 1. Pedido existente.<br>2. Algún elemento hijo está cancelado.<br>3. Completado pertenece al catálogo. |
| **Requisito relacionado** | RF-21 / RN-03 |
| **Tipo de escenario** | Alterno |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Marca manualmente el pedido como Completado. | Operación normal con condición alterna en gestión de pedidos | Módulo de pedidos | Registra Completado sin bloquear por hijos cancelados. | El pedido queda con el nuevo registro Completado y los hijos conservan sus propios estados. |

#### ESC-CAL-INTG-0012

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0012 |
| **Nombre** | Cambio manual válido del estado de una entrada |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El cambio de estado de una entrada y de sus líneas debe ser manual e independiente. |
| **Objetivo** | Permitir que el empleado determine manualmente el estado de la entrada. |
| **Criterios de éxito** | Se registra el nuevo estado de la entrada. |
| **Prerrequisitos** | 1. Entrada existente.<br>2. Estado válido. |
| **Requisito relacionado** | RF-28 / RN-02 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Selecciona un nuevo estado para la entrada. | Operación normal | Módulo de entradas | Registra el estado con la fecha actual. | La entrada refleja el estado seleccionado sin calcularlo desde sus líneas. |

#### ESC-CAL-INTG-0013

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0013 |
| **Nombre** | Entrada completada con una línea cancelada |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El cambio de estado de una entrada y de sus líneas debe ser manual e independiente. |
| **Objetivo** | Mantener independencia entre estado padre y estados de líneas. |
| **Criterios de éxito** | La entrada puede marcarse como Completada. |
| **Prerrequisitos** | 1. Existe una línea cancelada.<br>2. El empleado selecciona Completada. |
| **Requisito relacionado** | RF-28 / RN-03 |
| **Tipo de escenario** | Alterno |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Marca la entrada como Completada. | Operación normal con condición alterna en gestión de entradas | Módulo de entradas | Acepta el cambio manual. | El registro Completada se guarda aunque una línea permanezca Cancelada. |

#### ESC-CAL-INTG-0014

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0014 |
| **Nombre** | Cambio manual válido del estado de una línea de entrada |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El cambio de estado de una entrada y de sus líneas debe ser manual e independiente. |
| **Objetivo** | Registrar la confirmación o descarte individual de una línea. |
| **Criterios de éxito** | La línea recibe el estado seleccionado con fecha actual. |
| **Prerrequisitos** | 1. Línea de entrada existente.<br>2. Estado permitido por el catálogo. |
| **Requisito relacionado** | RF-27 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Marca una línea como completada o cancelada. | Operación normal | Módulo de entradas | Registra el nuevo estado de la línea. | La línea conserva su propio historial de estado independiente de la entrada. |

#### ESC-CAL-INTG-0015

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0015 |
| **Nombre** | Estado inválido para línea de entrada |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El cambio de estado de una entrada y de sus líneas debe ser manual e independiente. |
| **Objetivo** | Evitar valores fuera del catálogo. |
| **Criterios de éxito** | La modificación es rechazada. |
| **Prerrequisitos** | 1. Valor de estado no pertenece al catálogo. |
| **Requisito relacionado** | RF-27 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta asignar un estado inválido a la línea. | Operación con falla en gestión de entradas | Módulo de entradas | Rechaza el estado. | No se agrega un registro de estado inválido. |

#### ESC-CAL-INTG-0016

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0016 |
| **Nombre** | Cambio de estado inválido de una salida |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El cambio de estado de una salida debe aceptar únicamente estados válidos y conservar el estado actual cuando el cambio es rechazado. |
| **Objetivo** | Verificar que un estado inválido no altere la información de la salida. |
| **Criterios de éxito** | El sistema rechaza el cambio y conserva el estado vigente de la salida. |
| **Prerrequisitos** | 1. Salida existente.<br>2. El empleado selecciona o envía un estado no válido para la salida. |
| **Requisito relacionado** | RF-48 / RN-02 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta cambiar una salida a un estado no válido. | Operación con falla en cambio de estado de salida | Módulo de salidas | Rechaza el cambio y conserva el estado vigente de la salida. | No se registra el estado inválido y la salida mantiene su estado anterior. |

#### ESC-CAL-INTG-0017

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0017 |
| **Nombre** | Salida completada con línea cancelada |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El cambio de estado de una salida y de sus líneas debe ser manual e independiente. |
| **Objetivo** | Permitir completar la salida aunque una línea esté cancelada. |
| **Criterios de éxito** | Se registra Completada sin modificar automáticamente las líneas. |
| **Prerrequisitos** | 1. Existe una línea cancelada. |
| **Requisito relacionado** | RF-48 / RN-03 |
| **Tipo de escenario** | Alterno |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Marca la salida como Completada. | Operación normal con condición alterna en gestión de salidas | Módulo de salidas | Acepta el cambio. | La salida queda Completada y la línea conserva Cancelada. |

#### ESC-CAL-INTG-0018

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0018 |
| **Nombre** | Cambio manual válido de línea de salida |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El cambio de estado de una salida y de sus líneas debe ser manual e independiente. |
| **Objetivo** | Registrar de manera independiente el estado de cada producto entregado. |
| **Criterios de éxito** | Se guarda el estado seleccionado con fecha actual. |
| **Prerrequisitos** | 1. Línea existente.<br>2. Estado válido. |
| **Requisito relacionado** | RF-44 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Marca una línea de salida como completada o cancelada. | Operación normal | Módulo de salidas | Registra el estado de la línea. | La línea mantiene un estado independiente de la salida padre. |

#### ESC-CAL-INTG-0019

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0019 |
| **Nombre** | Estado inválido para línea de salida |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El cambio de estado de una salida y de sus líneas debe ser manual e independiente. |
| **Objetivo** | Evitar estados no definidos en una línea. |
| **Criterios de éxito** | El sistema rechaza la operación. |
| **Prerrequisitos** | 1. Estado no pertenece al catálogo. |
| **Requisito relacionado** | RF-44 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta asignar un estado inválido. | Operación con falla en gestión de salidas | Módulo de salidas | Rechaza el cambio. | No se crea un registro de estado inválido. |

#### ESC-CAL-INTG-0020

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0020 |
| **Nombre** | Cambio manual válido de estado de proyecto |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El estado de un proyecto debe cambiarse manualmente y no derivarse del estado de sus salidas. |
| **Objetivo** | Conservar control manual sobre el ciclo del proyecto. |
| **Criterios de éxito** | Se registra el nuevo estado. |
| **Prerrequisitos** | 1. Proyecto existente.<br>2. Estado válido. |
| **Requisito relacionado** | RF-37 / RN-02 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Selecciona un nuevo estado para el proyecto. | Operación normal | Módulo de proyectos | Registra el estado seleccionado. | El proyecto refleja el estado elegido sin calcularlo desde sus salidas. |

#### ESC-CAL-INTG-0021

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0021 |
| **Nombre** | Proyecto completado con salida cancelada |
| **Atributo de calidad** | Integridad |
| **Categoría** | Estados manuales |
| **Característica** | El estado de un proyecto debe cambiarse manualmente y no derivarse del estado de sus salidas. |
| **Objetivo** | Permitir completar el proyecto aunque una salida esté cancelada. |
| **Criterios de éxito** | Se registra Completado. |
| **Prerrequisitos** | 1. Existe al menos una salida cancelada. |
| **Requisito relacionado** | RF-37 / RN-03 |
| **Tipo de escenario** | Alterno |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Marca el proyecto como Completado. | Operación normal con condición alterna en gestión de proyectos | Módulo de proyectos | Acepta el cambio manual. | El proyecto queda Completado y la salida conserva su estado. |

#### ESC-CAL-INTG-0022

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0022 |
| **Nombre** | Determinación del estado actual |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consistencia temporal |
| **Característica** | El estado actual de cada entidad debe corresponder al registro de estado con la fecha más reciente. |
| **Objetivo** | Evitar inconsistencias al consultar el estado vigente. |
| **Criterios de éxito** | El sistema toma como actual el registro con fecha más reciente. |
| **Prerrequisitos** | 1. La entidad posee dos o más registros históricos de estado. |
| **Requisito relacionado** | RN-04 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta una entidad con historial de estados. | Operación normal | Módulo de estados | Selecciona el registro de fecha más reciente como estado actual. | El estado mostrado coincide con el registro cuya fecha_cambio es la más reciente. |

#### ESC-CAL-INTG-0023

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0023 |
| **Nombre** | Edición de línea de entrada no completada |
| **Atributo de calidad** | Integridad |
| **Categoría** | Control de modificación |
| **Característica** | La edición de entradas o líneas completadas debe estar restringida. |
| **Objetivo** | Permitir correcciones mientras la línea no esté completada. |
| **Criterios de éxito** | El sistema actualiza la línea y confirma la edición. |
| **Prerrequisitos** | 1. La línea existe y no está completada. |
| **Requisito relacionado** | RF-26 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Edita datos permitidos de la línea. | Operación normal | Módulo de entradas | Guarda los cambios. | Los nuevos datos quedan persistidos. |

#### ESC-CAL-INTG-0024

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0024 |
| **Nombre** | Edición bloqueada de línea de entrada completada |
| **Atributo de calidad** | Integridad |
| **Categoría** | Control de modificación |
| **Característica** | La edición de entradas o líneas completadas debe estar restringida. |
| **Objetivo** | Preservar la integridad de movimientos ya completados. |
| **Criterios de éxito** | El sistema rechaza la edición. |
| **Prerrequisitos** | 1. La línea ya está completada. |
| **Requisito relacionado** | RF-26 |
| **Tipo de escenario** | Restricción |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta editar la línea completada. | Operación con falla en gestión de entradas | Módulo de entradas | Bloquea la operación y explica la causa. | Los datos de la línea permanecen sin cambios. |

#### ESC-CAL-INTG-0025

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0025 |
| **Nombre** | Edición de línea de salida no completada |
| **Atributo de calidad** | Integridad |
| **Categoría** | Control de modificación |
| **Característica** | La edición de salidas o líneas completadas debe estar restringida. |
| **Objetivo** | Permitir editar una línea mientras no esté completada. |
| **Criterios de éxito** | El sistema guarda los cambios. |
| **Prerrequisitos** | 1. Línea existente y no completada. |
| **Requisito relacionado** | RF-47 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Edita una línea de salida. | Operación normal | Módulo de salidas | Actualiza la línea y confirma. | Los cambios quedan persistidos. |

#### ESC-CAL-INTG-0026

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0026 |
| **Nombre** | Edición bloqueada de línea de salida completada |
| **Atributo de calidad** | Integridad |
| **Categoría** | Control de modificación |
| **Característica** | La edición de salidas o líneas completadas debe estar restringida. |
| **Objetivo** | Evitar alteraciones a movimientos cerrados. |
| **Criterios de éxito** | El sistema rechaza la edición. |
| **Prerrequisitos** | 1. La línea está completada. |
| **Requisito relacionado** | RF-47 |
| **Tipo de escenario** | Restricción |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta editar una línea completada. | Operación con falla en gestión de salidas | Módulo de salidas | Bloquea la operación. | La línea permanece sin cambios. |

#### ESC-CAL-INTG-0027

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0027 |
| **Nombre** | Edición de proyecto en curso |
| **Atributo de calidad** | Integridad |
| **Categoría** | Control de modificación |
| **Característica** | La edición de un proyecto debe permitirse únicamente mientras el proyecto esté en curso. |
| **Objetivo** | Permitir modificar información mientras el proyecto está activo. |
| **Criterios de éxito** | Nombre, descripción o empleados asignados se actualizan. |
| **Prerrequisitos** | 1. Proyecto existente en estado En curso. |
| **Requisito relacionado** | RF-36 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Edita el proyecto. | Operación normal | Módulo de proyectos | Guarda los cambios y confirma. | La información modificada queda persistida. |

#### ESC-CAL-INTG-0028

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0028 |
| **Nombre** | Edición bloqueada de proyecto completado o cancelado |
| **Atributo de calidad** | Integridad |
| **Categoría** | Control de modificación |
| **Característica** | La edición de un proyecto debe permitirse únicamente mientras el proyecto esté en curso. |
| **Objetivo** | Impedir cambios fuera del estado permitido. |
| **Criterios de éxito** | El sistema rechaza la edición. |
| **Prerrequisitos** | 1. Proyecto completado o cancelado. |
| **Requisito relacionado** | RF-36 |
| **Tipo de escenario** | Restricción |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta editar el proyecto. | Operación con falla en gestión de proyectos | Módulo de proyectos | Bloquea la modificación y muestra error. | No se modifica la información del proyecto. |

#### ESC-CAL-INTG-0029

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0029 |
| **Nombre** | Asignación válida de empleado a proyecto |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consistencia de relaciones |
| **Característica** | La asignación de empleados a proyectos debe evitar duplicados para el mismo proyecto. |
| **Objetivo** | Registrar una participación válida. |
| **Criterios de éxito** | Se crea la asignación con su tipo de participación. |
| **Prerrequisitos** | 1. Empleado y proyecto existen.<br>2. La asignación no existe. |
| **Requisito relacionado** | RF-31 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Asigna un empleado a un proyecto. | Operación normal | Módulo de proyectos | Crea la asignación. | Existe una sola asignación para la relación registrada. |

#### ESC-CAL-INTG-0030

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0030 |
| **Nombre** | Asignación duplicada rechazada |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consistencia de relaciones |
| **Característica** | La asignación de empleados a proyectos debe evitar duplicados para el mismo proyecto. |
| **Objetivo** | Evitar duplicidad de participaciones. |
| **Criterios de éxito** | El sistema rechaza la asignación repetida. |
| **Prerrequisitos** | 1. El empleado ya está asignado al proyecto. |
| **Requisito relacionado** | RF-31 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta crear nuevamente la misma asignación. | Operación con falla en gestión de proyectos | Módulo de proyectos | Rechaza la operación y muestra error. | No se crea una segunda asignación duplicada. |

#### ESC-CAL-INTG-0031

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0031 |
| **Nombre** | Notificación por stock bajo |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consistencia de notificaciones |
| **Característica** | Las notificaciones automáticas deben generarse de manera coherente con los eventos de negocio definidos. |
| **Objetivo** | Generar alerta cuando el stock resultante alcanza o queda por debajo del mínimo. |
| **Criterios de éxito** | Se crea una notificación de producto. |
| **Prerrequisitos** | 1. Una salida o ajuste deja stock ≤ cantidad mínima. |
| **Requisito relacionado** | RF-56 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Actualiza el stock y detecta el umbral mínimo. | Operación normal | Módulo de inventario | Crea la notificación correspondiente. | Existe una nueva notificación vinculada al producto cuando stock_resultante ≤ mínimo. |

#### ESC-CAL-INTG-0032

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0032 |
| **Nombre** | Sin notificación cuando el stock permanece sobre el mínimo |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consistencia de notificaciones |
| **Característica** | Las notificaciones automáticas deben generarse de manera coherente con los eventos de negocio definidos. |
| **Objetivo** | Evitar alertas incorrectas. |
| **Criterios de éxito** | No se genera notificación de stock bajo. |
| **Prerrequisitos** | 1. El stock resultante es mayor al mínimo. |
| **Requisito relacionado** | RF-56 |
| **Tipo de escenario** | Alterno |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Actualiza el stock. | Operación normal con condición alterna en control de stock | Módulo de inventario | No crea alerta de stock bajo. | No aparece una nueva notificación de stock bajo para ese movimiento. |

#### ESC-CAL-INTG-0033

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0033 |
| **Nombre** | Notificación por creación de pedido |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consistencia de notificaciones |
| **Característica** | Las notificaciones automáticas deben generarse de manera coherente con los eventos de negocio definidos. |
| **Objetivo** | Registrar la alerta asociada a un pedido creado correctamente. |
| **Criterios de éxito** | Se crea una notificación de pedido tipo Creación. |
| **Prerrequisitos** | 1. El pedido fue creado con éxito. |
| **Requisito relacionado** | RF-57 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Finaliza la creación de un pedido. | Operación normal | Módulo de pedidos | Genera la notificación de creación. | Todo pedido creado exitosamente produce la notificación definida. |

#### ESC-CAL-INTG-0034

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0034 |
| **Nombre** | Pedido rechazado sin notificación de creación |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consistencia de notificaciones |
| **Característica** | Las notificaciones automáticas deben generarse de manera coherente con los eventos de negocio definidos. |
| **Objetivo** | Evitar notificaciones de pedidos que no existen. |
| **Criterios de éxito** | No se genera notificación. |
| **Prerrequisitos** | 1. La creación del pedido fue rechazada. |
| **Requisito relacionado** | RF-57 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Recibe resultado fallido de creación. | Operación con falla en gestión de pedidos | Módulo de pedidos | No genera notificación de creación. | No existe alerta de creación vinculada a un pedido no creado. |

#### ESC-CAL-INTG-0035

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0035 |
| **Nombre** | Notificación por cambio de estado de pedido |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consistencia de notificaciones |
| **Característica** | Las notificaciones automáticas deben generarse de manera coherente con los eventos de negocio definidos. |
| **Objetivo** | Mantener coherencia entre cambio de estado y alertas. |
| **Criterios de éxito** | Se genera la notificación correspondiente al nuevo estado. |
| **Prerrequisitos** | 1. El cambio de estado del pedido fue registrado. |
| **Requisito relacionado** | RF-58 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Detecta un nuevo registro de estado para un pedido. | Operación normal | Módulo de pedidos | Crea la notificación asociada. | Cada cambio de estado registrado genera su notificación de pedido. |

#### ESC-CAL-INTG-0036

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0036 |
| **Nombre** | Consulta del historial de un pedido |
| **Atributo de calidad** | Integridad |
| **Categoría** | Historial de estados |
| **Característica** | El sistema debe conservar y mostrar todos los cambios de estado de cada pedido ordenados por fecha. |
| **Objetivo** | Permitir reconstruir la evolución del estado de un pedido. |
| **Criterios de éxito** | Se muestran todos los registros de estado ordenados por fecha. |
| **Prerrequisitos** | 1. Pedido existente con uno o más estados. |
| **Requisito relacionado** | RF-49 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta el historial de un pedido. | Operación normal | Módulo de historiales | Retorna todos los cambios de estado. | La cantidad y orden de registros mostrados coincide con los estados almacenados del pedido. |

#### ESC-CAL-INTG-0037

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0037 |
| **Nombre** | Consulta de pedidos por rango válido |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consulta temporal |
| **Característica** | El historial de pedidos debe poder consultarse dentro de un rango de fechas válido. |
| **Objetivo** | Acotar la trazabilidad a un periodo específico. |
| **Criterios de éxito** | Se retornan únicamente pedidos con movimientos dentro del rango. |
| **Prerrequisitos** | 1. Fecha inicial ≤ fecha final. |
| **Requisito relacionado** | RF-50 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta historial indicando rango válido. | Operación normal | Módulo de historiales | Filtra los movimientos por fecha. | No se muestran movimientos fuera del intervalo solicitado. |

#### ESC-CAL-INTG-0038

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0038 |
| **Nombre** | Rango de fechas inválido en historial de pedidos |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consulta temporal |
| **Característica** | El historial de pedidos debe poder consultarse dentro de un rango de fechas válido. |
| **Objetivo** | Evitar resultados inconsistentes por intervalos inválidos. |
| **Criterios de éxito** | La consulta es rechazada. |
| **Prerrequisitos** | 1. Fecha inicial > fecha final. |
| **Requisito relacionado** | RF-50 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta con rango inválido. | Operación con falla en consulta de historiales | Módulo de historiales | Muestra un mensaje de error. | No se devuelve un conjunto de resultados para el rango inválido. |

#### ESC-CAL-INTG-0039

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0039 |
| **Nombre** | Consulta del historial de una entrada |
| **Atributo de calidad** | Integridad |
| **Categoría** | Historial de movimientos |
| **Característica** | El sistema debe conservar el historial de entradas con sus productos recibidos y cambios de estado. |
| **Objetivo** | Reconstruir qué productos ingresaron y cómo cambió su estado. |
| **Criterios de éxito** | Se muestran líneas de producto y registros de estado. |
| **Prerrequisitos** | 1. Entrada existente. |
| **Requisito relacionado** | RF-51 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta el historial de una entrada. | Operación normal | Módulo de historiales | Retorna líneas y estados asociados. | La información mostrada corresponde a los registros persistidos de la entrada. |

#### ESC-CAL-INTG-0040

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0040 |
| **Nombre** | Consulta de entradas por rango inválido |
| **Atributo de calidad** | Integridad |
| **Categoría** | Historial de movimientos |
| **Característica** | El sistema debe conservar el historial de entradas con sus productos recibidos y cambios de estado. |
| **Objetivo** | Evitar consultas temporales inconsistentes. |
| **Criterios de éxito** | Se rechaza el rango inválido. |
| **Prerrequisitos** | 1. Fecha inicial > fecha final. |
| **Requisito relacionado** | RF-52 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta historial de entradas con rango inválido. | Operación con falla en consulta de historiales | Módulo de historiales | Muestra error y no ejecuta el filtro. | No se retornan resultados para el rango inválido. |

#### ESC-CAL-INTG-0041

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0041 |
| **Nombre** | Consulta de entradas por rango válido |
| **Atributo de calidad** | Integridad |
| **Categoría** | Historial de movimientos |
| **Característica** | El sistema debe conservar el historial de entradas con sus productos recibidos y cambios de estado. |
| **Objetivo** | Filtrar entradas por periodo. |
| **Criterios de éxito** | Se retornan las entradas correspondientes. |
| **Prerrequisitos** | 1. Rango válido. |
| **Requisito relacionado** | RF-52 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta historial de entradas por fechas. | Operación normal | Módulo de historiales | Retorna solo las entradas del rango. | No aparecen entradas fuera del intervalo. |

#### ESC-CAL-INTG-0042

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0042 |
| **Nombre** | Consulta del historial de una salida |
| **Atributo de calidad** | Integridad |
| **Categoría** | Historial de movimientos |
| **Característica** | El sistema debe conservar el historial de salidas con productos entregados y cambios de estado. |
| **Objetivo** | Reconstruir los productos entregados y estados de una salida. |
| **Criterios de éxito** | Se muestran las líneas y los registros de estado. |
| **Prerrequisitos** | 1. Salida existente. |
| **Requisito relacionado** | RF-53 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta historial de una salida. | Operación normal | Módulo de historiales | Retorna líneas y estados. | Los datos mostrados corresponden a los registros persistidos. |

#### ESC-CAL-INTG-0043

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0043 |
| **Nombre** | Consulta de salidas por rango válido |
| **Atributo de calidad** | Integridad |
| **Categoría** | Historial de movimientos |
| **Característica** | El sistema debe conservar el historial de salidas con productos entregados y cambios de estado. |
| **Objetivo** | Filtrar salidas por fechas. |
| **Criterios de éxito** | Se retornan las salidas correspondientes. |
| **Prerrequisitos** | 1. Rango válido. |
| **Requisito relacionado** | RF-54 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta historial de salidas indicando fechas. | Operación normal | Módulo de historiales | Filtra por rango. | No se incluyen salidas fuera del intervalo. |

#### ESC-CAL-INTG-0044

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0044 |
| **Nombre** | Consulta de salidas por rango inválido |
| **Atributo de calidad** | Integridad |
| **Categoría** | Historial de movimientos |
| **Característica** | El sistema debe conservar el historial de salidas con productos entregados y cambios de estado. |
| **Objetivo** | Evitar consultas temporales inválidas. |
| **Criterios de éxito** | La consulta se rechaza. |
| **Prerrequisitos** | 1. Fecha inicial > fecha final. |
| **Requisito relacionado** | RF-54 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta un rango inválido. | Operación con falla en consulta de historiales | Módulo de historiales | Muestra error. | No se devuelven resultados. |

#### ESC-CAL-INTG-0045

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0045 |
| **Nombre** | Consulta del historial de proyecto |
| **Atributo de calidad** | Integridad |
| **Categoría** | Historial de estados |
| **Característica** | El sistema debe conservar el historial de proyectos con cada cambio de estado. |
| **Objetivo** | Permitir reconstruir la evolución del proyecto. |
| **Criterios de éxito** | Se muestran sus registros de estado. |
| **Prerrequisitos** | 1. Proyecto existente. |
| **Requisito relacionado** | RF-55 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta el historial de un proyecto. | Operación normal | Módulo de proyectos | Retorna registros de estado. | Los registros presentados corresponden al historial persistido del proyecto. |

#### ESC-CAL-INTG-0046

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0046 |
| **Nombre** | Cálculo de materiales usados por proyecto |
| **Atributo de calidad** | Integridad |
| **Categoría** | Trazabilidad de materiales |
| **Característica** | El sistema debe calcular la cantidad total usada de cada producto dentro de un proyecto a partir de sus salidas. |
| **Objetivo** | Conocer con certeza la cantidad consumida por producto en un proyecto. |
| **Criterios de éxito** | El sistema suma todas las líneas de salida agrupadas por producto. |
| **Prerrequisitos** | 1. Proyecto existente con salidas registradas. |
| **Requisito relacionado** | RF-42 / RN-14 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta el total usado de materiales del proyecto. | Operación normal | Módulo de proyectos | Calcula los totales por producto. | Cada total coincide con la suma de las cantidades de todas las líneas de salida del producto en el proyecto. |

#### ESC-CAL-INTG-0047

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-INTG-0047 |
| **Nombre** | Envío consistente de notificación al servicio push |
| **Atributo de calidad** | Integridad |
| **Categoría** | Consistencia de notificaciones |
| **Característica** | Las notificaciones generadas por eventos de negocio deben conservar correspondencia con el evento que las origina y enviarse mediante el servicio de notificaciones definido. |
| **Objetivo** | Garantizar que una notificación generada por el sistema corresponda al evento de negocio que la originó y sea enviada al servicio de notificaciones. |
| **Criterios de éxito** | La notificación enviada corresponde al evento que la generó y no se produce una alerta distinta o duplicada. |
| **Prerrequisitos** | 1. Existe una notificación generada por un evento de negocio.<br>2. El servicio de notificaciones está disponible. |
| **Requisito relacionado** | RF-56 / RF-57 / RF-58 / Interfaz de software 7.3 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Genera una alerta que debe enviarse al dispositivo. | Operación normal | Módulo de notificaciones | Envía al servicio push la notificación correspondiente al evento de negocio. | La notificación enviada corresponde al evento que la originó y no se genera una alerta distinta o duplicada. |

### Modificabilidad

#### ESC-CAL-MOD-0001

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0001 |
| **Nombre** | Agregar o editar TipoEstado para Pedido |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | TipoEstado |
| **Característica** | TipoEstado debe poder ampliarse o editarse para Pedido sin afectar la lógica manual del módulo. |
| **Objetivo** | Permitir modificar TipoEstado utilizado por Pedido sin introducir lógica automática de cambio de estado. |
| **Criterios de éxito** | El nuevo valor queda disponible para ser seleccionado manualmente en Pedido. |
| **Prerrequisitos** | 1. El nombre de TipoEstado es válido y no está duplicado. |
| **Requisito relacionado** | RN-05 / RF-64 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Crea o edita un valor de TipoEstado utilizado por Pedido. | Operación normal | Módulo de configuración | Guarda el valor y el módulo puede utilizarlo mediante selección manual. | El nuevo TipoEstado queda disponible como opción válida sin modificar automáticamente estados existentes. |

#### ESC-CAL-MOD-0002

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0002 |
| **Nombre** | TipoEstado inválido o duplicado para Pedido |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | TipoEstado |
| **Característica** | TipoEstado debe poder ampliarse o editarse para Pedido sin afectar la lógica manual del módulo. |
| **Objetivo** | Evitar que una modificación incorrecta de TipoEstado introduzca valores inválidos. |
| **Criterios de éxito** | La modificación es rechazada. |
| **Prerrequisitos** | 1. El nombre de TipoEstado está vacío o ya existe. |
| **Requisito relacionado** | RN-05 / RF-64 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta crear o editar un TipoEstado inválido para Pedido. | Operación con falla en configuración de catálogos | Módulo de configuración | Rechaza el cambio y muestra error. | TipoEstado conserva sus valores anteriores y no incorpora el valor inválido o duplicado. |

#### ESC-CAL-MOD-0003

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0003 |
| **Nombre** | Agregar o editar TipoEstado para Entrada |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | TipoEstado |
| **Característica** | TipoEstado debe poder ampliarse o editarse para Entrada sin afectar la lógica manual del módulo. |
| **Objetivo** | Permitir modificar TipoEstado utilizado por Entrada sin introducir lógica automática de cambio de estado. |
| **Criterios de éxito** | El nuevo valor queda disponible para ser seleccionado manualmente en Entrada. |
| **Prerrequisitos** | 1. El nombre de TipoEstado es válido y no está duplicado. |
| **Requisito relacionado** | RN-06 / RF-64 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Crea o edita un valor de TipoEstado utilizado por Entrada. | Operación normal | Módulo de configuración | Guarda el valor y el módulo puede utilizarlo mediante selección manual. | El nuevo TipoEstado queda disponible como opción válida sin modificar automáticamente estados existentes. |

#### ESC-CAL-MOD-0004

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0004 |
| **Nombre** | TipoEstado inválido o duplicado para Entrada |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | TipoEstado |
| **Característica** | TipoEstado debe poder ampliarse o editarse para Entrada sin afectar la lógica manual del módulo. |
| **Objetivo** | Evitar que una modificación incorrecta de TipoEstado introduzca valores inválidos. |
| **Criterios de éxito** | La modificación es rechazada. |
| **Prerrequisitos** | 1. El nombre de TipoEstado está vacío o ya existe. |
| **Requisito relacionado** | RN-06 / RF-64 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta crear o editar un TipoEstado inválido para Entrada. | Operación con falla en configuración de catálogos | Módulo de configuración | Rechaza el cambio y muestra error. | TipoEstado conserva sus valores anteriores y no incorpora el valor inválido o duplicado. |

#### ESC-CAL-MOD-0005

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0005 |
| **Nombre** | Agregar o editar TipoEstado para EntradaProducto |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | TipoEstado |
| **Característica** | TipoEstado debe poder ampliarse o editarse para EntradaProducto sin afectar la confirmación por línea. |
| **Objetivo** | Permitir modificar TipoEstado utilizado por EntradaProducto sin introducir lógica automática de cambio de estado. |
| **Criterios de éxito** | El nuevo valor queda disponible para ser seleccionado manualmente en EntradaProducto. |
| **Prerrequisitos** | 1. El nombre de TipoEstado es válido y no está duplicado. |
| **Requisito relacionado** | RN-07 / RF-64 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Crea o edita un valor de TipoEstado utilizado por EntradaProducto. | Operación normal | Módulo de configuración | Guarda el valor y el módulo puede utilizarlo mediante selección manual. | El nuevo TipoEstado queda disponible como opción válida sin modificar automáticamente estados existentes. |

#### ESC-CAL-MOD-0006

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0006 |
| **Nombre** | TipoEstado inválido o duplicado para EntradaProducto |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | TipoEstado |
| **Característica** | TipoEstado debe poder ampliarse o editarse para EntradaProducto sin afectar la confirmación por línea. |
| **Objetivo** | Evitar que una modificación incorrecta de TipoEstado introduzca valores inválidos. |
| **Criterios de éxito** | La modificación es rechazada. |
| **Prerrequisitos** | 1. El nombre de TipoEstado está vacío o ya existe. |
| **Requisito relacionado** | RN-07 / RF-64 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta crear o editar un TipoEstado inválido para EntradaProducto. | Operación con falla en configuración de catálogos | Módulo de configuración | Rechaza el cambio y muestra error. | TipoEstado conserva sus valores anteriores y no incorpora el valor inválido o duplicado. |

#### ESC-CAL-MOD-0007

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0007 |
| **Nombre** | Agregar o editar TipoEstado para Salida |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | TipoEstado |
| **Característica** | TipoEstado debe poder ampliarse o editarse para Salida sin afectar la lógica manual del módulo. |
| **Objetivo** | Permitir modificar TipoEstado utilizado por Salida sin introducir lógica automática de cambio de estado. |
| **Criterios de éxito** | El nuevo valor queda disponible para ser seleccionado manualmente en Salida. |
| **Prerrequisitos** | 1. El nombre de TipoEstado es válido y no está duplicado. |
| **Requisito relacionado** | RN-08 / RF-64 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Crea o edita un valor de TipoEstado utilizado por Salida. | Operación normal | Módulo de configuración | Guarda el valor y el módulo puede utilizarlo mediante selección manual. | El nuevo TipoEstado queda disponible como opción válida sin modificar automáticamente estados existentes. |

#### ESC-CAL-MOD-0008

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0008 |
| **Nombre** | TipoEstado inválido o duplicado para Salida |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | TipoEstado |
| **Característica** | TipoEstado debe poder ampliarse o editarse para Salida sin afectar la lógica manual del módulo. |
| **Objetivo** | Evitar que una modificación incorrecta de TipoEstado introduzca valores inválidos. |
| **Criterios de éxito** | La modificación es rechazada. |
| **Prerrequisitos** | 1. El nombre de TipoEstado está vacío o ya existe. |
| **Requisito relacionado** | RN-08 / RF-64 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta crear o editar un TipoEstado inválido para Salida. | Operación con falla en configuración de catálogos | Módulo de configuración | Rechaza el cambio y muestra error. | TipoEstado conserva sus valores anteriores y no incorpora el valor inválido o duplicado. |

#### ESC-CAL-MOD-0009

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0009 |
| **Nombre** | Agregar o editar TipoEstado para SalidaProducto |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | TipoEstado |
| **Característica** | TipoEstado debe poder ampliarse o editarse para SalidaProducto sin afectar la confirmación por línea. |
| **Objetivo** | Permitir modificar TipoEstado utilizado por SalidaProducto sin introducir lógica automática de cambio de estado. |
| **Criterios de éxito** | El nuevo valor queda disponible para ser seleccionado manualmente en SalidaProducto. |
| **Prerrequisitos** | 1. El nombre de TipoEstado es válido y no está duplicado. |
| **Requisito relacionado** | RN-09 / RF-64 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Crea o edita un valor de TipoEstado utilizado por SalidaProducto. | Operación normal | Módulo de configuración | Guarda el valor y el módulo puede utilizarlo mediante selección manual. | El nuevo TipoEstado queda disponible como opción válida sin modificar automáticamente estados existentes. |

#### ESC-CAL-MOD-0010

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0010 |
| **Nombre** | TipoEstado inválido o duplicado para SalidaProducto |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | TipoEstado |
| **Característica** | TipoEstado debe poder ampliarse o editarse para SalidaProducto sin afectar la confirmación por línea. |
| **Objetivo** | Evitar que una modificación incorrecta de TipoEstado introduzca valores inválidos. |
| **Criterios de éxito** | La modificación es rechazada. |
| **Prerrequisitos** | 1. El nombre de TipoEstado está vacío o ya existe. |
| **Requisito relacionado** | RN-09 / RF-64 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta crear o editar un TipoEstado inválido para SalidaProducto. | Operación con falla en configuración de catálogos | Módulo de configuración | Rechaza el cambio y muestra error. | TipoEstado conserva sus valores anteriores y no incorpora el valor inválido o duplicado. |

#### ESC-CAL-MOD-0011

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0011 |
| **Nombre** | Agregar o editar TipoEstado para Proyecto |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | TipoEstado |
| **Característica** | TipoEstado debe poder ampliarse o editarse para Proyecto sin afectar la lógica manual del módulo. |
| **Objetivo** | Permitir modificar TipoEstado utilizado por Proyecto sin introducir lógica automática de cambio de estado. |
| **Criterios de éxito** | El nuevo valor queda disponible para ser seleccionado manualmente en Proyecto. |
| **Prerrequisitos** | 1. El nombre de TipoEstado es válido y no está duplicado. |
| **Requisito relacionado** | RN-10 / RF-64 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Crea o edita un valor de TipoEstado utilizado por Proyecto. | Operación normal | Módulo de configuración | Guarda el valor y el módulo puede utilizarlo mediante selección manual. | El nuevo TipoEstado queda disponible como opción válida sin modificar automáticamente estados existentes. |

#### ESC-CAL-MOD-0012

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0012 |
| **Nombre** | TipoEstado inválido o duplicado para Proyecto |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | TipoEstado |
| **Característica** | TipoEstado debe poder ampliarse o editarse para Proyecto sin afectar la lógica manual del módulo. |
| **Objetivo** | Evitar que una modificación incorrecta de TipoEstado introduzca valores inválidos. |
| **Criterios de éxito** | La modificación es rechazada. |
| **Prerrequisitos** | 1. El nombre de TipoEstado está vacío o ya existe. |
| **Requisito relacionado** | RN-10 / RF-64 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta crear o editar un TipoEstado inválido para Proyecto. | Operación con falla en configuración de catálogos | Módulo de configuración | Rechaza el cambio y muestra error. | TipoEstado conserva sus valores anteriores y no incorpora el valor inválido o duplicado. |

#### ESC-CAL-MOD-0013

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0013 |
| **Nombre** | Creación o edición válida de TipoEntrada |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | Catálogos configurables |
| **Característica** | El catálogo de tipos de entrada debe poder crearse, consultarse y editarse sin requerir cambios en la estructura de una entrada. |
| **Objetivo** | Permitir ampliar los motivos de entrada. |
| **Criterios de éxito** | El tipo queda disponible para nuevas entradas. |
| **Prerrequisitos** | 1. Nombre válido y no duplicado. |
| **Requisito relacionado** | RF-61 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Crea o edita un tipo de entrada. | Operación normal | Módulo de configuración | Guarda el tipo y lo deja disponible. | El catálogo refleja el nuevo valor sin alterar entradas existentes. |

#### ESC-CAL-MOD-0014

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0014 |
| **Nombre** | TipoEntrada vacío o duplicado |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | Catálogos configurables |
| **Característica** | El catálogo de tipos de entrada debe poder crearse, consultarse y editarse sin requerir cambios en la estructura de una entrada. |
| **Objetivo** | Evitar valores inválidos en el catálogo. |
| **Criterios de éxito** | La operación es rechazada. |
| **Prerrequisitos** | 1. Nombre vacío o duplicado. |
| **Requisito relacionado** | RF-61 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta guardar el tipo. | Operación con falla en configuración de catálogos | Módulo de configuración | Rechaza el cambio. | El catálogo no incorpora el valor inválido. |

#### ESC-CAL-MOD-0015

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0015 |
| **Nombre** | Creación o edición válida de tipo de participación |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | Catálogos configurables |
| **Característica** | Los tipos de participación en proyecto deben poder crearse, consultarse y editarse como catálogo independiente. |
| **Objetivo** | Permitir adaptar las formas de participación de empleados en proyectos. |
| **Criterios de éxito** | El tipo queda disponible para nuevas asignaciones. |
| **Prerrequisitos** | 1. Nombre válido y no duplicado. |
| **Requisito relacionado** | RF-62 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Crea o edita un tipo de participación. | Operación normal | Módulo de configuración | Guarda el nuevo valor. | El tipo puede seleccionarse en una asignación sin alterar las ya existentes. |

#### ESC-CAL-MOD-0016

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0016 |
| **Nombre** | Tipo de participación vacío o duplicado |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | Catálogos configurables |
| **Característica** | Los tipos de participación en proyecto deben poder crearse, consultarse y editarse como catálogo independiente. |
| **Objetivo** | Evitar inconsistencias de catálogo. |
| **Criterios de éxito** | El sistema rechaza la operación. |
| **Prerrequisitos** | 1. Nombre vacío o duplicado. |
| **Requisito relacionado** | RF-62 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta guardar un valor inválido. | Operación con falla en configuración de catálogos | Módulo de configuración | Rechaza el cambio. | El catálogo permanece sin el valor inválido. |

#### ESC-CAL-MOD-0017

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0017 |
| **Nombre** | Creación o edición válida de tipo de notificación |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | Catálogos configurables |
| **Característica** | Los tipos de notificación de producto y pedido deben poder crearse, consultarse y editarse independientemente. |
| **Objetivo** | Permitir ampliar los tipos de alertas definidos por el sistema. |
| **Criterios de éxito** | El nuevo tipo queda disponible en su catálogo correspondiente. |
| **Prerrequisitos** | 1. Nombre válido y no duplicado. |
| **Requisito relacionado** | RF-63 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Crea o edita un tipo de notificación. | Operación normal | Módulo de configuración | Guarda el valor. | El nuevo tipo queda disponible sin modificar notificaciones históricas. |

#### ESC-CAL-MOD-0018

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-MOD-0018 |
| **Nombre** | Tipo de notificación vacío o duplicado |
| **Atributo de calidad** | Modificabilidad |
| **Categoría** | Catálogos configurables |
| **Característica** | Los tipos de notificación de producto y pedido deben poder crearse, consultarse y editarse independientemente. |
| **Objetivo** | Evitar valores inconsistentes. |
| **Criterios de éxito** | La operación se rechaza. |
| **Prerrequisitos** | 1. Nombre vacío o duplicado. |
| **Requisito relacionado** | RF-63 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta guardar un tipo inválido. | Operación con falla en configuración de catálogos | Módulo de configuración | Rechaza el cambio. | No se incorpora el valor inválido. |

---

### Rendimiento

#### ESC-CAL-REN-0001

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0001 |
| **Nombre** | Consulta de stock en menos de 1 segundo |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Consulta de inventario |
| **Característica** | El sistema debe responder a la consulta del stock de un producto específico en menos de 1 segundo bajo condiciones normales de uso. |
| **Objetivo** | Verificar el tiempo de respuesta especificado en los requisitos no funcionales. |
| **Criterios de éxito** | La operación se completa en menos de 1 segundo. |
| **Prerrequisitos** | 1. Sistema operativo bajo condiciones normales de uso.<br>2. Datos válidos para ejecutar la operación. |
| **Requisito relacionado** | RF-07 / RNF-02 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta el stock de un producto específico. | Operación normal | Módulo de inventario | Procesa la solicitud y entrega la respuesta correspondiente. | Tiempo transcurrido desde la solicitud hasta la respuesta: menos de 1 segundo. |

#### ESC-CAL-REN-0002

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0002 |
| **Nombre** | Consulta del listado de productos en menos de 1.5 segundos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Consulta de inventario |
| **Característica** | El sistema debe responder a la consulta del listado completo de productos en menos de 1.5 segundos bajo condiciones normales de uso. |
| **Objetivo** | Verificar el tiempo de respuesta especificado en los requisitos no funcionales. |
| **Criterios de éxito** | La operación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. Sistema operativo bajo condiciones normales de uso.<br>2. Datos válidos para ejecutar la operación. |
| **Requisito relacionado** | RF-09 / RNF-03 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita el listado completo de productos. | Operación normal | Módulo de inventario | Procesa la solicitud y entrega la respuesta correspondiente. | Tiempo transcurrido desde la solicitud hasta la respuesta: menos de 1.5 segundos. |

#### ESC-CAL-REN-0003

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0003 |
| **Nombre** | Registro de pedido confirmado en menos de 1.5 segundos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Registro de movimientos |
| **Característica** | El sistema debe confirmar el registro de un pedido en menos de 1.5 segundos bajo condiciones normales de uso. |
| **Objetivo** | Verificar el tiempo de respuesta especificado en los requisitos no funcionales. |
| **Criterios de éxito** | La operación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. Sistema operativo bajo condiciones normales de uso.<br>2. Datos válidos para ejecutar la operación. |
| **Requisito relacionado** | RF-16 / RNF-04 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Registra un pedido válido. | Operación normal | Módulo de pedidos | Procesa la solicitud y entrega la respuesta correspondiente. | Tiempo transcurrido desde la solicitud hasta la respuesta: menos de 1.5 segundos. |

#### ESC-CAL-REN-0004

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0004 |
| **Nombre** | Registro de entrada confirmado en menos de 1.5 segundos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Registro de movimientos |
| **Característica** | El sistema debe confirmar el registro de una entrada en menos de 1.5 segundos bajo condiciones normales de uso. |
| **Objetivo** | Verificar el tiempo de respuesta especificado en los requisitos no funcionales. |
| **Criterios de éxito** | La operación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. Sistema operativo bajo condiciones normales de uso.<br>2. Datos válidos para ejecutar la operación. |
| **Requisito relacionado** | RF-22 / RNF-05 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Registra una entrada válida. | Operación normal | Módulo de entradas | Procesa la solicitud y entrega la respuesta correspondiente. | Tiempo transcurrido desde la solicitud hasta la respuesta: menos de 1.5 segundos. |

#### ESC-CAL-REN-0005

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0005 |
| **Nombre** | Registro de salida confirmado en menos de 1.5 segundos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Registro de movimientos |
| **Característica** | El sistema debe confirmar el registro de una salida en menos de 1.5 segundos bajo condiciones normales de uso. |
| **Objetivo** | Verificar el tiempo de respuesta especificado en los requisitos no funcionales. |
| **Criterios de éxito** | La operación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. Sistema operativo bajo condiciones normales de uso.<br>2. Datos válidos para ejecutar la operación. |
| **Requisito relacionado** | RF-39 / RNF-06 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Registra una salida válida. | Operación normal | Módulo de salidas | Procesa la solicitud y entrega la respuesta correspondiente. | Tiempo transcurrido desde la solicitud hasta la respuesta: menos de 1.5 segundos. |

#### ESC-CAL-REN-0006

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0006 |
| **Nombre** | Consulta de historial en menos de 1.5 segundos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Consulta histórica |
| **Característica** | El sistema debe responder a la consulta del historial de pedidos, entradas o salidas en menos de 1.5 segundos bajo condiciones normales de uso. |
| **Objetivo** | Verificar el tiempo de respuesta especificado en los requisitos no funcionales. |
| **Criterios de éxito** | La operación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. Sistema operativo bajo condiciones normales de uso.<br>2. Datos válidos para ejecutar la operación. |
| **Requisito relacionado** | RF-49 a RF-54 / RNF-07 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Consulta historial de pedidos, entradas o salidas. | Operación normal | Módulo de historiales | Procesa la solicitud y entrega la respuesta correspondiente. | Tiempo transcurrido desde la solicitud hasta la respuesta: menos de 1.5 segundos. |

#### ESC-CAL-REN-0007

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0007 |
| **Nombre** | Exportación de historial de pedidos con datos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Exportación de información |
| **Característica** | El sistema debe generar la exportación del historial de pedidos en formato Excel en menos de 1.5 segundos. |
| **Objetivo** | Verificar que la exportación solicitada se genere dentro del tiempo de respuesta definido. |
| **Criterios de éxito** | La exportación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. Existen datos del módulo a exportar. |
| **Requisito relacionado** | RF-67 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita exportación de historial de pedidos. | Operación normal | Módulo de exportación | Genera el archivo Excel y confirma la exportación. | Tiempo transcurrido desde la solicitud hasta la generación del archivo: menos de 1.5 segundos. |

#### ESC-CAL-REN-0008

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0008 |
| **Nombre** | Exportación de historial de pedidos sin datos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Exportación de información |
| **Característica** | El sistema debe generar la exportación del historial de pedidos en formato Excel en menos de 1.5 segundos. |
| **Objetivo** | Verificar que la exportación solicitada se genere dentro del tiempo de respuesta definido. |
| **Criterios de éxito** | La exportación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. No existen registros del módulo. |
| **Requisito relacionado** | RF-67 |
| **Tipo de escenario** | Alterno |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita exportación de historial de pedidos. | Operación normal con condición alterna en exportación de información | Módulo de exportación | Genera el archivo con encabezados y muestra el mensaje de ausencia de datos. | Tiempo transcurrido desde la solicitud hasta la generación del archivo: menos de 1.5 segundos. |

#### ESC-CAL-REN-0009

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0009 |
| **Nombre** | Exportación de historial de entradas con datos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Exportación de información |
| **Característica** | El sistema debe generar la exportación del historial de entradas en formato Excel en menos de 1.5 segundos. |
| **Objetivo** | Verificar que la exportación solicitada se genere dentro del tiempo de respuesta definido. |
| **Criterios de éxito** | La exportación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. Existen datos del módulo a exportar. |
| **Requisito relacionado** | RF-68 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita exportación de historial de entradas. | Operación normal | Módulo de exportación | Genera el archivo Excel y confirma la exportación. | Tiempo transcurrido desde la solicitud hasta la generación del archivo: menos de 1.5 segundos. |

#### ESC-CAL-REN-0010

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0010 |
| **Nombre** | Exportación de historial de entradas sin datos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Exportación de información |
| **Característica** | El sistema debe generar la exportación del historial de entradas en formato Excel en menos de 1.5 segundos. |
| **Objetivo** | Verificar que la exportación solicitada se genere dentro del tiempo de respuesta definido. |
| **Criterios de éxito** | La exportación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. No existen registros del módulo. |
| **Requisito relacionado** | RF-68 |
| **Tipo de escenario** | Alterno |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita exportación de historial de entradas. | Operación normal con condición alterna en exportación de información | Módulo de exportación | Genera el archivo con encabezados y muestra el mensaje de ausencia de datos. | Tiempo transcurrido desde la solicitud hasta la generación del archivo: menos de 1.5 segundos. |

#### ESC-CAL-REN-0011

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0011 |
| **Nombre** | Exportación de historial de salidas con datos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Exportación de información |
| **Característica** | El sistema debe generar la exportación del historial de salidas en formato Excel en menos de 1.5 segundos. |
| **Objetivo** | Verificar que la exportación solicitada se genere dentro del tiempo de respuesta definido. |
| **Criterios de éxito** | La exportación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. Existen datos del módulo a exportar. |
| **Requisito relacionado** | RF-69 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita exportación de historial de salidas. | Operación normal | Módulo de exportación | Genera el archivo Excel y confirma la exportación. | Tiempo transcurrido desde la solicitud hasta la generación del archivo: menos de 1.5 segundos. |

#### ESC-CAL-REN-0012

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0012 |
| **Nombre** | Exportación de historial de salidas sin datos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Exportación de información |
| **Característica** | El sistema debe generar la exportación del historial de salidas en formato Excel en menos de 1.5 segundos. |
| **Objetivo** | Verificar que la exportación solicitada se genere dentro del tiempo de respuesta definido. |
| **Criterios de éxito** | La exportación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. No existen registros del módulo. |
| **Requisito relacionado** | RF-69 |
| **Tipo de escenario** | Alterno |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita exportación de historial de salidas. | Operación normal con condición alterna en exportación de información | Módulo de exportación | Genera el archivo con encabezados y muestra el mensaje de ausencia de datos. | Tiempo transcurrido desde la solicitud hasta la generación del archivo: menos de 1.5 segundos. |

#### ESC-CAL-REN-0013

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0013 |
| **Nombre** | Exportación de proyectos con datos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Exportación de información |
| **Característica** | El sistema debe generar la exportación de proyectos en formato Excel en menos de 1.5 segundos. |
| **Objetivo** | Verificar que la exportación solicitada se genere dentro del tiempo de respuesta definido. |
| **Criterios de éxito** | La exportación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. Existen datos del módulo a exportar. |
| **Requisito relacionado** | RF-70 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita exportación de proyectos. | Operación normal | Módulo de exportación | Genera el archivo Excel y confirma la exportación. | Tiempo transcurrido desde la solicitud hasta la generación del archivo: menos de 1.5 segundos. |

#### ESC-CAL-REN-0014

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0014 |
| **Nombre** | Exportación de proyectos sin datos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Exportación de información |
| **Característica** | El sistema debe generar la exportación de proyectos en formato Excel en menos de 1.5 segundos. |
| **Objetivo** | Verificar que la exportación solicitada se genere dentro del tiempo de respuesta definido. |
| **Criterios de éxito** | La exportación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. No existen registros del módulo. |
| **Requisito relacionado** | RF-70 |
| **Tipo de escenario** | Alterno |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita exportación de proyectos. | Operación normal con condición alterna en exportación de información | Módulo de exportación | Genera el archivo con encabezados y muestra el mensaje de ausencia de datos. | Tiempo transcurrido desde la solicitud hasta la generación del archivo: menos de 1.5 segundos. |

#### ESC-CAL-REN-0015

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0015 |
| **Nombre** | Exportación de inventario actual con datos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Exportación de información |
| **Característica** | El sistema debe generar la exportación del inventario actual en formato Excel en menos de 1.5 segundos. |
| **Objetivo** | Verificar que la exportación solicitada se genere dentro del tiempo de respuesta definido. |
| **Criterios de éxito** | La exportación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. Existen datos del módulo a exportar. |
| **Requisito relacionado** | RF-71 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita exportación de inventario actual. | Operación normal | Módulo de exportación | Genera el archivo Excel y confirma la exportación. | Tiempo transcurrido desde la solicitud hasta la generación del archivo: menos de 1.5 segundos. |

#### ESC-CAL-REN-0016

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-REN-0016 |
| **Nombre** | Exportación de inventario actual sin datos |
| **Atributo de calidad** | Rendimiento |
| **Categoría** | Exportación de información |
| **Característica** | El sistema debe generar la exportación del inventario actual en formato Excel en menos de 1.5 segundos. |
| **Objetivo** | Verificar que la exportación solicitada se genere dentro del tiempo de respuesta definido. |
| **Criterios de éxito** | La exportación se completa en menos de 1.5 segundos. |
| **Prerrequisitos** | 1. No existen registros del módulo. |
| **Requisito relacionado** | RF-71 |
| **Tipo de escenario** | Alterno |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Solicita exportación de inventario actual. | Operación normal con condición alterna en exportación de información | Módulo de exportación | Genera el archivo con encabezados y muestra el mensaje de ausencia de datos. | Tiempo transcurrido desde la solicitud hasta la generación del archivo: menos de 1.5 segundos. |

---

### Disponibilidad

#### ESC-CAL-DIS-0001

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-DIS-0001 |
| **Nombre** | Disponibilidad del sistema en horario laboral |
| **Atributo de calidad** | Disponibilidad |
| **Categoría** | Continuidad del servicio |
| **Característica** | El sistema debe poder funcionar en un 99.999% del tiempo en horario laboral |
| **Objetivo** | Garantizar que los usuarios puedan utilizar el sistema de forma continua durante el horario laboral y reducir al mínimo las interrupciones del servicio. |
| **Criterios de éxito** | El sistema mantiene una disponibilidad igual o superior al 99.999 % durante el horario laboral. |
| **Prerrequisitos** | 1. La infraestructura en la nube se encuentra operativa.<br>2. Los servicios principales del sistema están desplegados y configurados.<br>3. El usuario dispone de conectividad para acceder al sistema. |
| **Requisito relacionado** | RNF-01 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Intenta acceder o utilizar una funcionalidad del sistema durante el horario laboral | Operación normal | Aplicación web y aplicación móvil | El sistema se mantiene disponible y permite al usuario acceder a las funcionalidades requeridas. | El sistema debe alcanzar una disponibilidad mínima del 99.999 % durante el horario laboral. |

#### ESC-CAL-DIS-0002

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-DIS-0002 |
| **Nombre** | Acceso al sistema desde web y móvil |
| **Atributo de calidad** | Disponibilidad |
| **Categoría** | Canales de acceso |
| **Característica** | El sistema debe permitir el acceso a sus funcionalidades mediante la aplicación web y la aplicación móvil soportada. |
| **Objetivo** | Garantizar que el empleado pueda acceder al sistema desde los canales web y móvil definidos para la solución. |
| **Criterios de éxito** | Las funcionalidades previstas están disponibles desde la aplicación web y desde la aplicación móvil soportada. |
| **Prerrequisitos** | 1. La infraestructura en la nube está operativa.<br>2. La aplicación web o móvil está disponible para el empleado. |
| **Requisito relacionado** | RNF-01 / RNF-12 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Accede al sistema desde uno de los clientes soportados. | Operación normal | Aplicación web y aplicación móvil | Permite el acceso a las funcionalidades disponibles desde el canal utilizado. | El empleado puede acceder a las funcionalidades previstas desde la aplicación web y desde la aplicación móvil soportada. |

---

### Usabilidad

#### ESC-CAL-USA-0001

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-USA-0001 |
| **Nombre** | Registro guiado de una entrada |
| **Atributo de calidad** | Usabilidad |
| **Categoría** | Facilidad de uso |
| **Característica** | La interfaz debe ser comprensible para empleados con conocimiento tecnológico básico y mantener una curva de aprendizaje mínima. |
| **Objetivo** | Comprobar que una operación central pueda ejecutarse siguiendo la interfaz sin conocimientos técnicos avanzados. |
| **Criterios de éxito** | El empleado identifica pedido, tipo y productos y completa el registro siguiendo los controles visibles. |
| **Prerrequisitos** | 1. Empleado autenticado.<br>2. Existe un pedido válido. |
| **Requisito relacionado** | RNF-09 / RF-22 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Registra una entrada desde la interfaz. | Operación normal | Interfaz de usuario | Presenta controles y mensajes comprensibles durante el flujo. | El requisito exige curva de aprendizaje mínima, pero no define número de pasos, tiempo máximo ni porcentaje de éxito; no se agrega una métrica no documentada. |

#### ESC-CAL-USA-0002

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-USA-0002 |
| **Nombre** | Mensaje comprensible ante dato inválido |
| **Atributo de calidad** | Usabilidad |
| **Categoría** | Facilidad de uso |
| **Característica** | La interfaz debe ser comprensible para empleados con conocimiento tecnológico básico y mantener una curva de aprendizaje mínima. |
| **Objetivo** | Evitar que un error de captura deje al empleado sin orientación. |
| **Criterios de éxito** | El sistema muestra el mensaje de error definido por el requisito funcional. |
| **Prerrequisitos** | 1. El empleado introduce un dato inválido en una operación con criterio de error documentado. |
| **Requisito relacionado** | RNF-09 / criterios de aceptación RF |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Confirma una operación con información inválida. | Operación con falla en uso de la interfaz | Interfaz de usuario | Rechaza la operación y presenta el error correspondiente. | El usuario recibe una indicación de error coherente con el criterio de aceptación del RF involucrado. |

#### ESC-CAL-USA-0003

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-USA-0003 |
| **Nombre** | Consulta de producto mediante código válido |
| **Atributo de calidad** | Usabilidad |
| **Categoría** | Facilidad de operación |
| **Característica** | La aplicación móvil debe facilitar la consulta y el registro de productos mediante el escaneo de códigos QR con la cámara del dispositivo. |
| **Objetivo** | Facilitar al empleado la consulta de un producto mediante el escaneo de su código QR. |
| **Criterios de éxito** | El sistema muestra la información del producto correspondiente al código escaneado sin requerir una búsqueda manual. |
| **Prerrequisitos** | 1. Cámara disponible.<br>2. Código QR corresponde a un producto registrado. |
| **Requisito relacionado** | RF-08 / RNF-08 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Escanea el código QR de un producto. | Operación normal | Aplicación móvil | Muestra la información del producto asociado al código escaneado. | El producto mostrado corresponde al código escaneado y el empleado accede a la información sin realizar una búsqueda manual. |

#### ESC-CAL-USA-0004

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-USA-0004 |
| **Nombre** | Código escaneado sin producto asociado |
| **Atributo de calidad** | Usabilidad |
| **Categoría** | Manejo de errores de operación |
| **Característica** | La aplicación móvil debe facilitar la consulta y el registro de productos mediante el escaneo de códigos QR con la cámara del dispositivo. |
| **Objetivo** | Informar de forma comprensible cuando el código escaneado no corresponde a un producto registrado. |
| **Criterios de éxito** | El sistema no muestra un producto incorrecto e informa que el código no está asociado a un producto. |
| **Prerrequisitos** | 1. Cámara disponible.<br>2. Código QR no corresponde a un producto registrado. |
| **Requisito relacionado** | RF-08 / RNF-08 |
| **Tipo de escenario** | Fallo controlado |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Escanea un código desconocido. | Operación con falla en lectura de código QR | Aplicación móvil | Informa que no existe un producto asociado al código escaneado. | No se muestra un producto incorrecto y el empleado recibe un mensaje comprensible sobre el código no registrado. |

#### ESC-CAL-USA-0005

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-USA-0005 |
| **Nombre** | Agregar producto a entrada por escaneo |
| **Atributo de calidad** | Usabilidad |
| **Categoría** | Facilidad de operación |
| **Característica** | La aplicación móvil debe facilitar la consulta y el registro de productos mediante el escaneo de códigos QR con la cámara del dispositivo. |
| **Objetivo** | Facilitar al empleado el registro de productos en una entrada mediante el escaneo del código QR. |
| **Criterios de éxito** | El producto escaneado se agrega a la entrada en curso sin requerir una búsqueda manual. |
| **Prerrequisitos** | 1. Entrada en construcción.<br>2. Cámara disponible.<br>3. Código QR válido. |
| **Requisito relacionado** | RF-73 / RNF-08 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Escanea un producto dentro de una entrada. | Operación normal | Aplicación móvil | Identifica el producto y lo agrega a la entrada en curso. | El producto agregado corresponde al código escaneado y se incorpora a la entrada sin búsqueda manual. |

#### ESC-CAL-USA-0006

| Campo | Valor |
|-------|-------|
| **Código** | ESC-CAL-USA-0006 |
| **Nombre** | Agregar producto a salida por escaneo |
| **Atributo de calidad** | Usabilidad |
| **Categoría** | Facilidad de operación |
| **Característica** | La aplicación móvil debe facilitar la consulta y el registro de productos mediante el escaneo de códigos QR con la cámara del dispositivo. |
| **Objetivo** | Facilitar al empleado el registro de productos en una salida mediante el escaneo del código QR. |
| **Criterios de éxito** | El producto escaneado se agrega a la salida en curso sin requerir una búsqueda manual. |
| **Prerrequisitos** | 1. Salida en construcción.<br>2. Cámara disponible.<br>3. Código QR válido. |
| **Requisito relacionado** | RF-40 / RNF-08 |
| **Tipo de escenario** | Éxito |

| Fuente del estímulo | Estímulo | Ambiente | Artefacto | Respuesta | Medida de la respuesta |
|---------------------|----------|----------|-----------|-----------|------------------------|
| Empleado | Escanea un producto dentro de una salida. | Operación normal | Aplicación móvil | Identifica el producto y lo agrega a la salida en curso. | El producto agregado corresponde al código escaneado y se incorpora a la salida sin búsqueda manual. |



## Restricciones de negocio

| Tipo | Restricción de negocio | Justificación | Plan de acción |
|------|------------------------|---------------|----------------|
| Humano | El equipo de desarrollo es pequeño y es un trabajo académico. Nadie queda dando soporte después de la entrega. | Si se diseña algo muy complejo, después no va a haber quién lo mantenga. | Se opta por una arquitectura simple y bien documentada. |
| Humano | El equipo de negocio solo cuenta con una hora diaria para trabajar en el proyecto. | Hay que aprovechar ese tiempo limitado. | Distribuir las tareas según esa hora disponible al día. |
| Tiempo | El proyecto tiene un tiempo límite definido por la universidad. | Es un proyecto académico con fechas establecidas. | Dividir el proyecto en etapas claras. |
| Presupuesto | No hay presupuesto definido para hosting ni servicios en la nube. | Elegir mal el servicio de hospedaje podría comprometer la disponibilidad. | Usar servicios en la nube con planes gratuitos como Render, Railway o Firebase. |
| Legal | El sistema no debe incumplir la normativa de facturación electrónica de la DIAN. | Evitar sanciones a Servingeniería. | Se delimita el alcance para que no gestione precios ni facturación. |
| Organizacional | Servingeniería nunca ha usado un sistema digital para este proceso. | Un cambio muy brusco puede dificultar la adopción. | Se diseña la primera versión imitando la lógica y el lenguaje del Excel actual. |
| Proceso | Algunas reglas de negocio aún se están definiendo. | Hay decisiones pendientes sobre cancelaciones, estados y permisos. | Ir documentando e implementando cada necesidad a medida que el cliente la confirme. |
| Tecnológico | El equipo no tiene experiencia previa construyendo apps con escaneo de cámara. | Es una parte clave del sistema. | Se desarrolla un prototipo del escaneo QR desde las primeras semanas. |

---

## Restricciones técnicas

| Tipo | Categoría | Restricción técnica | Justificación |
|------|-----------|---------------------|---------------|
| Impuesta por el cliente | Tecnología base | La aplicación debe ser accesible tanto desde un navegador web como desde un dispositivo móvil. | Solicitado explícitamente por la encargada de bodega. |
| Impuesta por el cliente | Tecnología base | La aplicación debe permitir usar la cámara del dispositivo para leer códigos QR y de barras. | Necesidad puntual para agilizar el registro. |
| Impuesta por el cliente | Rendimiento | La consulta del stock de un producto debe responder en un tiempo muy corto, cercano al tiempo real. | La stakeholder fue explícita en que no quería depender de preguntar a otra persona. |
| Propia del proyecto | Reactividad | El sistema debe apoyarse en principios de reactividad. | Para mantener la información al día sin refrescar manualmente. |
| Propia del proyecto | Capacidad concurrente | El sistema debe permitir que varios empleados registren movimientos al mismo tiempo sin generar inconsistencias. | Condición necesaria para un entorno multi-usuario. |
| Propia del proyecto | Disponibilidad | El sistema debe poder funcionar con alta disponibilidad en horario laboral. | Prioridad indicada por el usuario. |
| Propia del proyecto | Prácticas de diseño | El diseño y desarrollo debe seguir los principios SOLID. | Para lograr un software más mantenible. |
| Propia del proyecto | Prácticas de diseño | Bajo acoplamiento entre módulos. | Para que un cambio en un módulo no afecte a los demás. |
| Propia del proyecto | Prácticas de diseño | Los catálogos de tipos y estados deben poder ampliarse sin modificar el código existente. | Coincide con la decisión de que estos catálogos sean editables. |
| Propia del proyecto | Patrones de diseño | Propender por el uso de patrones como DRY y KISS. | Evitar duplicación y mantener el sistema simple. |
| Propia del proyecto | Código limpio | Propender por prácticas de código limpio. | Facilita que cualquier persona del equipo entienda y modifique el sistema. |
| Propia del proyecto | Organización | Organización clara entre capas o módulos. | Facilita el mantenimiento y el crecimiento. |
| Propia del proyecto | Metodología | Desarrollo con metodología ágil. | Varias decisiones se han ido ajustando durante el proceso. |
| Propia del proyecto | Prácticas DevOps | Propender por automatizar pruebas y despliegues. | Reducir errores manuales y entregar cambios de forma confiable. |



