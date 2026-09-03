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

---

## Supuestos y restricciones adicionales

### Supuestos

- Servingeniería opera desde una sola bodega física de materiales.
- El área de contabilidad seguirá gestionando precios y facturación de forma independiente al sistema.

### Restricciones

- El sistema no incluye precios, facturación electrónica ni reportes para la DIAN.
- No se contemplan productos que requieran tratamiento regulatorio especial.
- No se implementan más niveles de permisos que la distinción entre empleado y administrador.
- El catálogo de estados no es editable desde la operación diaria.
- El producto, el empleado, las categorías y los catálogos no manejan un estado de activo o inactivo en esta versión.

### Pendientes de confirmar

- Qué ocurre cuando se cancela un pedido o proyecto que ya tiene entradas o salidas parcialmente completadas.
- Si el pedido debe registrar los productos y cantidades solicitados desde el momento de su creación, o si es suficiente registrarlos al momento de la entrada.
- Si eliminar por completo la cuenta de un empleado puede afectar el historial de pedidos, entradas y salidas que ese empleado haya registrado.
- Nivel de conocimiento tecnológico real de los empleados de campo.
- Qué funcionalidades quedan fuera de la primera fase en caso de restricción de presupuesto o tiempo.
- Catálogo de estados: fijo, no editable por el usuario.
