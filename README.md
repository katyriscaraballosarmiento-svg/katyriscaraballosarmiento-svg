# 📁 Mi Portafolio de Software QA

Bienvenido a mi portafolio de control de calidad de software (QA). Aquí encontrarás la documentación, el diseño y la ejecución de pruebas para diferentes proyectos, demostrando mis habilidades en pruebas manuales, de APIs, bases de datos y automatización.

---

## 👨‍💻 Sobre Mí

**Katyris Caraballo** Tecnica en Desarrollo de Software | QA Analyst

**Herramientas y Habilidades:**
* Testing Manual (Diseño y ejecución de casos de prueba, reporte de defectos)
* Postman (API Testing)
* SQL (Validación de datos y consultas)
* Git / GitHub
* Node.js & Playwright (Automatización - En progreso)
* WordPress / WooCommerce / Elementor

**LinkedIn: www.linkedin.com/in/katyris-caraballo-sarmien
**GitHub:** [github.com/katyriscaraballosarmiento-svg](https://github.com/katyriscaraballosarmiento-svg)

---

# Proyecto 1: Pruebas de Software - Aplicación WILPOS 🧪

## Descripción
Planificación, diseño y ejecución de pruebas manuales para la aplicación de punto de venta (POS) **WILPOS**, asegurando la correcta gestión de transacciones, inventario y flujos de usuario.

## Alcance
Módulos probados:
* Autenticación de Usuarios (Login/Registro)
* Gestión de Inventario / Catálogo de Productos
* Procesamiento de Ventas (Carrito de Compras / Facturación)
* Módulo de Checkout y Cierre de Caja

## Casos de Prueba

### TC-001 - Login Exitoso
**Precondición:** El usuario debe estar previamente registrado en el sistema.  

**Pasos:**
1. Abrir la interfaz de Login de WILPOS.
2. Ingresar un correo/usuario válido.
3. Ingresar la contraseña correcta.
4. Presionar el botón "Entrar".

**Resultado Esperado:** El sistema debe permitir el acceso correctamente y redirigir al panel principal (Dashboard).

---

### TC-002 - Validaciar de Contraseña Incorrecta
**Pasos:**
1. Abrir la interfaz de Login de WILPOS.
2. Ingresar un usuario válido.
3. Ingresar una contraseña errónea.
4. Presionar "Entrar".

**Resultado Esperado:** El sistema debe denegar el acceso y mostrar el mensaje de alerta: *"Usuario o contraseña incorrectos."*

---
## Caso de Prueba: US-01 - Acceso y Validar:
### ID: TC-01
 Titulo: Acceso y Validar de Licencia Demo
 
 Modulo: Configuración / Licenciamiento
 
 Precondiciones: Aplicación Wilpos instalada y en pantalla de inicio(Login/licencia.
 
 Datos: Llave “DEMO”

Pasos: 
1.	Buscar la app llamada “WILPOS”  
2.	Iniciar la aplicación 
3.	Dirigirse al módulo de Configuración.
4. Seleccionar la sección de Estado de Licencia.
5-	4. Verificar el estado de la licencia y el texto descriptivo del plan.

Resultado Esperado El sistema debe permitir el acceso al ingresar una llave válida de tipo "DEMO" en el campo de licencia.

Resultado actua: El sistema  mostro  la licencia como "Activa" y el texto descriptivo exactamente: " Demo gratuito"  

---
## Caso de Prueba: US-02 - Verificar de Indicador en Footer
### ID: TC-02
Titulo: Validar de texto persistente en el pie de página (Footer)

Modulo: Interfaz de Usuario (UI)

Precondiciones: El sistema debe estar iniciado con una licencia tipo "DEMO" activa.

Datos: Inspección visual del footer( pies de pagina).

Pasos:
1. Iniciar la aplicación WilPOS.
2. Observar la barra inferior (footer) en el Dashboard principal.
3. Navegar a otros módulos (Caja, Inventario) y verificar si el texto permanece.

Resultado esperado: Al estar activa la licencia demo, debe mostrarse un indicador persistente en el footer (pie de página) del sistema con el texto: "Modo Demo Activo"

Resultado actual: El sistema muestra el texto "Demo Gratuito" dentro de un botón gris. No coincide con el texto requerido en la especificación.

Estado: FAIL (Fallido)
---
## Caso de Prueba: US-03 - Unificar del Flujo de Entrada
### ID: TC-03
Titulo: Verificar de flujo de entrada unificado (Sin botón independiente)

Modulo: Acceso/ UX (Experiencia de Usuario)

Preocondiciones: La aplicación debe estar en la pantalla de inicio (sin licencia activa).

Datos: Inspección visual de la pantalla de bienvenida/activación.

Pasos: 
1.	Abrir la aplicación WilPOS.
2. Revisar si existe algún botón etiquetado como "Iniciar Modo Demo", "Probar Gratis" o similar que evite el paso de la licencia.
3.	Confirmar que solo existe un campo para ingresar llaves de activación
   
Resultado Esperado: No debe existir un botón de "Iniciar Modo Demo" independiente; el flujo de entrada debe ser el mismo que una licencia comercial.

Resultado actual: Se confirma que el sistema no presenta botones de acceso rápido para la demo. El usuario debe ingresar obligatoriamente una llave en el campo estándar para acceder.
 
Tipo de Prueba: Funcional / Diseño de Flujo
Estado: PASS(APROBAR)

---

## US-02: Gestión de Ventas (Retail/Pos)
## Caso de Prueba: US-01 - Búsqueda y Selecionar de Productos
### ID: TC-04 
Titulo: Búsqueda por nombre y selecionar manual de productos en el POS(Punto de Venta)

Modulo: CAJA

Precondiciones:
1. Licencia Demo activa. 
2. Existencia de productos cargados en el inventario inicial.
   
Datos:
Búsqueda: coca-cola
Pasos: 
1.	Iniciar sección con credenciales correctas 
2.	Hacer clic en el módulo de Caja.
3.	 Ubicar la barra de búsqueda de productos.
4.	Escribir el nombre de un producto conocido EJ: ”Coca Cola”  

Resultado Esperado: El sistema debe mostrar el producto y permitir su selección para el carrito de compras.  

Resultado Actual: EXITOSO. El sistema mostró correctamente el producto "coca cola"  y se añadió con un precio de RD$88.50 

---
Estado: Pass(aprobado)

## Caso de Prueba: US-02 - Selecionar Métodos de Pago
### ID: TC-05
Titulo: Validar de métodos de pago: Efectivo 

Madulo: Punto de Venta (Caja)

Precondiciones:  
1. Caja abierta.
2. Al menos un producto añadido al carrito de compras.

   
Datos: Producto: Coca Cola (RD$88.50).

Pasos: 
1.	Iniciar sección con credenciales correctas 
2. Hacer clic en el módulo de Caja.
3.	Ubicar la barra de búsqueda de productos.
4. Poner nombre de producto ej” coca cola”
5. Hacer clic en el producto coca cola
6. Hacer clic en el botón “procesar venta”
7. Seleccionar “Efectivo”
8. Hacer click en “Confirmar”
9. Vizualizacion previa de factura
 
Resultado esperado: Se deben permitir pagos con métodos: Efectivo (Simulado).

Resultado actual: EXITOSO. El sistema despliega las opciones de pago. Se validó que el método "efectivo" permite cerrar venta de manera inmediata, cumpliendo con la simulación requerida.

---

## Caso de Prueba: US-02 - Selecionar de Métodos de Pago
### ID: TC-06
Titulo: Validar de métodos de pago: Tarjeta

Madulo: Punto de Venta (Caja)

Precondiciones:  
1. Caja abierta.
2. Al menos un producto añadido al carrito de compras.

Datos: Producto: jabon (RD$29.50).

Pasos: 
1.	Iniciar sección con credenciales correctas  
2. Hacer clic en el módulo de Caja.
3. Ubicar la barra de búsqueda de productos.
4. Poner nombre de producto ej” jabon ”
5. Hacer clic en el producto jabón 
6. Hacer clic en el botón “procesar venta”	
7. Seleccionar “tarjeta”
8. Hacer clic en  “Confirmar” 
9. Vizualizacion previa de factura
 
Resultado esperado: Se deben permitir pagos con método: Tarjeta (Simulado).

Resultado actual: EXITOSO. El sistema despliega las opciones de pago. Se validó que el método "tarjeta" permite cerrar venta de manera inmediata, cumpliendo con la simulación requerida.

Tipo de Prueba: Funcional 

---

## Caso de Prueba: US-02 - Visualizar de Comprobante (PDF)

### ID: TC-07
Titulo: visualizar de factura en formato digital

Modulo: caja (punto de venta)

Precondiciones: Venta finalizada con método de pago seleccionado (Efectivo).

Datos: producto jabon

Pasos:
1. Finalizar la venta del producto "jabon". 
2. Confirmar el pago (Método: efectivo)  
3. Haz clic en el botón  “ Confirmar “. 
4. Verificar la apertura automática de la "Vista Previa de Factura".
 
Resultado esperado: Restricción de Impresión: Al finalizar una venta, no se enviará comando a impresoras físicas, pero debe abrirse un visor de PDF con el recibo generado

Resultado actual: EXITOSO. Se generó la Factura #5. El sistema calculó correctamente el ITBIS (RD$4.50 sobre un neto de RD$25.00) y muestra todos los campos requeridos en el visor digital
Tipo de Prueba: Funcional / Salida de Datos.

---

## Caso de Prueba: US-08 - Verificar de Cálculos de ITBIS
### ID: TC-08
Titulo: Validar de cálculo automático de ITBIS (18%)

Modulo: Caja “venta”

Precondiciones: El producto en el carrito debe estar marcado como gravado con el 18%.

Datos: Precio Neto: RD$25.00 / Tasa ITBIS: 18%.

Pasos:
1.	Tener agregado un producto al carrito (Ej: Jabón).  
2. Verificar el desglose de precios en la parte inferior del carrito.  
3.	Finalizar la venta y revisar el desglose en el comprobante PDF.  

Resultado esperado: El cálculo de ITBIS (18%) debe aplicarse correctamente sobre los productos gravados del dataset de prueba.

Resultado actual: 
EXITOSO. Como se observa en la captura, el sistema realiza el cálculo inverso correctamente: RD$25.00 (Neto) x 0.18 = RD$4.50. La suma total coincide perfectamente con el precio del producto.  

---


# Práctica de Exploración: Plataforma OrangeHRM

---

## 📋 Desarrollo de la Tarea

### 1. Acceso al Sistema (Login)
* **Acción:** Ingresé a la URL oficial de *OrangeHRM Demo*. Introduje las credenciales proporcionadas: Usuario `Admin` y Contraseña `admin123`.
* **Observación:** La interfaz es limpia y profesional. Presenta un formulario centralizado con validación de seguridad.

### 2. Dashboard (Panel Principal)
* **Acción:** Tras iniciar sesión, la página me redirigió automáticamente al Dashboard
* **Observación:** En el Dashboard observé varios widgets que resumen la actividad diaria de la empresa, lo que facilita la toma de decisiones rápidas sin navegar por todos los módulos[cite: 1]. El sistema cuenta con una sección de *Quick Launch* que actúa como un atajo para las tareas más comunes, optimizando el flujo de trabajo del usuario.

### 3. Módulo de PIM (Personal Information Management)
* **Acción:** Hice clic en la opción **"PIM"** del menú lateral izquierdo y seleccioné **"Employee List"**
* **Observación:** Este módulo PIM es el eje central de OrangeHRM, ya que centraliza toda la base de datos del personal. Permite buscar personal por nombre, ID o estado de contrato. Descubrí que se puede añadir, editar o eliminar información detallada de cada trabajador.

### 4. Módulo de Leave (Gestión de Permisos)
* **Acción:** Seleccioné el módulo **"Leave"** en el menú lateral.
* **Observación:** Aquí se gestionan las vacaciones y ausencias. Exploré la sección **"Apply"**, donde un empleado puede solicitar días libres seleccionando el tipo de permiso y el rango de fechas. El sistema muestra automáticamente el balance de días disponibles.

### 5. Módulo de Recruitment (Reclutamiento)
* **Acción:** Ingresé al módulo de **"Recruitment"** y revisé la pestaña **"Candidates"**.
* **Observación:** Este apartado sirve para gestionar el flujo de contratación. Permite ver las vacantes abiertas y los candidatos que han aplicado, facilitando el seguimiento de entrevistas y procesos de selección.

---

## 🎯 Conclusión

Tras la exploración detallada de la plataforma *OrangeHRM Demo*, puedo concluir que se trata de una herramienta integral y sumamente intuitiva para la gestión del capital humano. La interfaz facilita la navegación gracias a su estructura modular y al uso de elementos visuales como los widgets en el panel principal.

Desde mi perspectiva, el módulo de **PIM** resultó ser el más interesante y relevante, ya que funciona como la columna vertebral de todo el sistema. Al centralizar la información maestra de cada colaborador, garantiza que procesos como la gestión de permisos en el módulo de *Leave* o el seguimiento de vacantes en *Recruitment* operen de manera precisa y organizada.

En definitiva, esta práctica me permitió comprender cómo la digitalización de los procesos de Recursos Humanos no solo ahorra tiempo mediante funciones como el *Quick Launch*, sino que también aporta transparencia y eficiencia a la administración de una empresa moderna.


# Práctica 2: Diseño de Casos de Prueba - OrangeHRM

---

## 📋 Especificación de Casos de Prueba (15 Escenarios)

### Módulo 1: Login (Inicio de Sesión)

#### 🔍 Caso de Prueba #1
* **ID:** `TC-LOGIN-001`
* **Título:** Iniciar de sesión con credenciales correctas
* **Módulo:** Login
* **Precondición:** Usuario registrado previamente en el sistema.
* **Datos de prueba:** * Usuario: `Admin`
  * Contraseña: `admin123`
* **Pasos:**
  1. Ingresar a la URL del sistema.
  2. Digitar el usuario válido en el campo correspondiente.
  3. Digitar la contraseña válida en el campo correspondiente.
  4. Presionar el botón "Login".
* **Resultado Esperado:** El sistema permite el acceso correctamente y redirige a la pantalla del Dashboard.
* **Tipo:** Positiva (Funcional)
* **Prioridad:** Alta

#### 🔍 Caso de Prueba #2
* **ID:** `TC-LOGIN-002`
* **Título:** Iniciar de sesión con credenciales incorrectas
* **Módulo:** Login
* **Precondición:** El usuario ingresado no está registrado en el sistema.
* **Datos de prueba:** * Usuario: `katyris`
  * Contraseña: `1234`
* **Pasos:**
  1. Ingresar a la URL del sistema.
  2. Digitar el usuario no válido `katyris`.
  3. Digitar la contraseña no válida `1234` (o `1253`).
  4. Presionar el botón "Login".
* **Resultado Esperado:** El sistema bloquea el acceso y despliega una alerta de error en pantalla que indica: *"Invalid credentials"*.
* **Tipo:** Negativa (Validación)
* **Prioridad:** Alta

---

### Módulo 2: PIM (Personal Information Management)

#### 🔍 Caso de Prueba #3
* **ID:** `TC-PIM-003`
* **Título:** Registrar exitoso de un nuevo empleado
* **Módulo:** PIM
* **Precondición:** Sesión activa con rol de Administrador.
* **Datos de prueba:** * Nombre: `Angel Miguel`
  * Apellido: `Sarmiento`
  * Employee ID: `1213`
* **Pasos:**
  1. Ir al menú lateral y hacer clic en el módulo "PIM".
  2. Hacer clic en la pestaña superior "Add Employee".
  3. Llenar los campos obligatorios con el Nombre y el Apellido de prueba.
  4. Ingresar la identificación manual en el campo "Employee ID" (`1213`).
  5. Hacer clic en el botón "Save".
* **Resultado Esperado:** Se muestra un mensaje emergente verde indicando *"Successfully Saved"* y se crea el perfil cargando los detalles personales del nuevo empleado.
* **Tipo:** Positiva (Funcional)
* **Prioridad:** Alta

#### 🔍 Caso de Prueba #4
* **ID:** `TC-PIM-004`
* **Título:** Validar de campos obligatorios vacíos al agregar empleado
* **Módulo:** PIM
* **Precondición:** Sesión activa con rol de Administrador; ubicarse en la vista "Add Employee".
* **Datos de prueba:** Borrar o dejar en blanco el campo "First Name".
* **Pasos:**
  1. Intentar guardar el formulario del nuevo empleado manteniendo el campo del nombre completamente en blanco.
  2. Hacer clic en el botón "Save".
* **Resultado Esperado:** El sistema debe impedir el guardado definitivo y desplegar un mensaje de error en color rojo debajo del campo vacío con la etiqueta *"Required"*.
* **Tipo:** Validación / Negativa
* **Prioridad:** Alta

---

### Módulo 3: Leave (Gestión de Licencias / Permisos)

#### 🔍 Caso de Prueba #5
* **ID:** `TC-LEAVE-005`
* **Título:** Validar de regla de negocio por saldo insuficiente al asignar licencia
* **Módulo:** Leave
* **Precondición:** Sesión activa con rol de Administrador. El empleado seleccionado no debe tener días acumulados disponibles.
* **Datos de prueba:** * Empleado: `Peter Mac Anderson`
  * Tipo de licencia: `Maternidad` (u otra licencia vacacional)
  * Rango de fechas: `01/03/2026 - 10/03/2026`
  * Duración: `Todos los días / Medio día - tarde`
* **Pasos:**
  1. Ir al módulo "Leave" en el menú principal.
  2. Hacer clic en la pestaña "Assign Leave".
  3. Completar todos los parámetros solicitados con los datos de prueba.
  4. Hacer clic en el botón "Assign".
* **Resultado Esperado:** El sistema interrumpe el flujo automático y lanza una alerta flotante de confirmación advirtiendo: *"El empleado no tiene suficiente saldo de vacaciones para la solicitud..."*.
* **Tipo:** Escenario Alterno / Regla de Negocio
* **Prioridad:** Alta

---

### Módulo 4: Admin (Administración del Sistema)

#### 🔍 Caso de Prueba #6
* **ID:** `TC-ADM-006`
* **Título:** Agregar una nueva nacionalidad al catálogo
* **Módulo:** Admin
* **Precondición:** El nombre de la nacionalidad a registrar no debe existir en la lista actual.
* **Datos de prueba:** Nacionalidad: `dominicano`
* **Pasos:**
  1. Navegar al módulo "Admin" en el menú izquierdo.
  2. Desplegar o seleccionar la sección "Nationalities".
  3. Hacer clic en el botón verde "+ Add".
  4. Ingresar el texto `dominicano` en el campo "Name".
  5. Hacer clic en el botón "Save".
* **Resultado Esperado:** La nacionalidad se almacena correctamente, reindexando la tabla general con el mensaje emergente *"Successfully Saved"*.
* **Tipo:** Positiva (Funcional)
* **Prioridad:** Alta

#### 🔍 Caso de Prueba #7
* **ID:** `TC-ADM-007`
* **Título:** Editar satisfactoriamente una nacionalidad existente
* **Módulo:** Admin
* **Precondición:** Debe existir previamente el registro de la nacionalidad elegida en el catálogo.
* **Datos de prueba:** * Registro origen: `AMERICANO`
  * Nuevo valor: `mexicano`
* **Pasos:**
  1. Ir al módulo "Admin" y ubicarse en la tabla de "Nationalities".
  2. Buscar el registro `AMERICANO` y hacer clic en su respectivo icono de lápiz ("Edit").
  3. Modificar el campo del nombre reemplazándolo por el valor `mexicano`.
  4. Hacer clic en el botón "Save".
* **Resultado Esperado:** Se actualiza el nombre en la lista general y el sistema lanza la confirmación emergente *"Successfully Saved"*.
* **Tipo:** Positiva (Funcional)
* **Prioridad:** Alta

#### 🔍 Caso de Prueba #8
* **ID:** `TC-ADM-008`
* **Título:** Eliminar masiva de registros en la tabla
* **Módulo:** Admin
* **Precondición:** Deben existir al menos dos o más registros creados en el listado de nacionalidades.
* **Datos de prueba:** Selección múltiple de casillas de verificación (Checkboxes).
* **Pasos:**
  1. Ir al listado de nacionalidades dentro del módulo Admin.
  2. Marcar las casillas de verificación de múltiples registros simultáneamente.
  3. Hacer clic en el botón superior "Delete Selected".
  4. Confirmar la acción en el cuadro de diálogo de advertencia.
* **Resultado Esperado:** Todas las nacionalidades seleccionadas son eliminadas de la base de datos de manera conjunta, mostrando un mensaje confirmando el éxito de la operación.
* **Tipo:** Positiva (Funcional)
* **Prioridad:** Alta

---

### Módulo 5: Time (Control de Asistencia y Tiempo)

#### 🔍 Caso de Prueba #9
* **ID:** `TC-TIME-009`
* **Título:** Visualizar y consulta exitosa de registros de asistencia
* **Módulo:** Time
* **Precondición:** El empleado consultado debe encontrarse en estado activo dentro del sistema con marcaciones previas.
* **Datos de prueba:** * Employee Name: `Peter Mac Anderson`
  * Date: `2026-03-03`
* **Pasos:**
  1. Ingresar al módulo de "Time" desde el menú lateral principal.
  2. Seleccionar la opción de submenú "Attendance > My Records / Attendance Records".
  3. En el buscador "Employee Name", escribir las iniciales y seleccionar al empleado sugerido por el autocompletado.
  4. Hacer clic en el icono del calendario e ingresar la fecha específica `2026-03-03`.
  5. Hacer clic en el botón "View".
* **Resultado Esperado:** El sistema procesa la consulta de manera fluida y carga detalladamente la tabla horaria del día para ese empleado.
* **Tipo:** Positiva (Consulta)
* **Prioridad:** Alta

#### 🔍 Caso de Prueba #10
* **ID:** `TC-TIME-010`
* **Título:** Validar del sistema cuando no existen registros para una fecha específica
* **Módulo:** Time
* **Precondición:** Escoger un día sin actividad laboral o una fecha en el futuro.
* **Datos de prueba:** * Employee Name: `Peter Mac Anderson`
  * Date: `2029-01-01`
* **Pasos:**
  1. Ingresar a la sección "Attendance Records" dentro de Time.
  2. Seleccionar al empleado de prueba.
  3. Introducir una fecha donde no haya registros de marcación (`2029-01-01`).
  4. Hacer clic en el botón "View".
* **Resultado Esperado:** El sistema debe manejar la consulta limpiamente mostrando un aviso informativo central que declare: *"No Records Found"*, sin romper el diseño de la tabla.
* **Tipo:** Negativa / Validación
* **Prioridad:** Media

---

### Módulo 6: Performance (Gestión del Desempeño)

#### 🔍 Caso de Prueba #11
* **ID:** `TC-PERF-011`
* **Título:** Búsqueda y filtrado avanzado de revisiones de desempeño
* **Módulo:** Performance
* **Precondición:** Existencia previa de evaluaciones cargadas con los estados e información correspondiente.
* **Datos de prueba:** * Employee Name: `Peter Mac Anderson`
  * Review Status: `In Progress`
  * Job Title: `Account Clerk` (o Account Assistant)
  * Incluir: Empleados actuales y pasados
* **Pasos:**
  1. Ingresar al módulo "Performance" en el menú principal.
  2. Seleccionar la opción "Manage Reviews".
  3. Ingresar y seleccionar el nombre del empleado.
  4. Cambiar el menú desplegable de estado a `"In Progress"`.
  5. Ajustar el cargo en el selector a `"Account Clerk"`.
  6. Hacer clic en el botón "Search".
* **Resultado Esperado:** La interfaz filtra dinámicamente el contenedor y muestra con total exactitud las evaluaciones que coincidan con los tres filtros ingresados.
* **Tipo:** Positiva (Filtro)
* **Prioridad:** Alta

#### 🔍 Caso de Prueba #12
* **ID:** `TC-PERF-012`
* **Título:** Validar búsqueda con filtros que no coinciden (Sin resultados)
* **Módulo:** Performance
* **Precondición:** Ingresar variables cruzadas de empleados sin procesos evaluativos asignados.
* **Datos de prueba:** * Employee Name: `Angel`
  * Review Status: `Activated`
* **Pasos:**
  1. Dirigirse a la pantalla de "Manage Reviews" dentro de Performance.
  2. Introducir un empleado de prueba que no tenga evaluaciones (`Angel`).
  3. Configurar el estado del filtro en `"Activated"`.
  4. Hacer clic en el botón "Search".
* **Resultado Esperado:** La grilla de datos oculta las filas genéricas y despliega limpiamente el mensaje institucional *"No Records Found"*.
* **Tipo:** Validación / Negativa
* **Prioridad:** Media

---

### Módulo 7: Dashboard (Tablero Principal)

#### 🔍 Caso de Prueba #13
* **ID:** `TC-DASH-013`
* **Título:** Verificar de carga e interactividad de widgets en el panel principal
* **Módulo:** Dashboard
* **Precondición:** El usuario se encuentra debidamente autenticado con un rol activo del sistema.
* **Datos de prueba:** N/A (Inspección Visual de la interfaz de usuario)
* **Pasos:**
  1. Completar el Login o hacer clic directo sobre la opción "Dashboard" del menú lateral.
  2. Inspeccionar la renderización de bloques: *Time at Work*, *My Actions*, *Quick Launch*, *Buzz Latest Posts*, *Employee Distribution by Subunit* y *Employee Distribution by Location*.
  3. Pasar el puntero del mouse sobre las gráficas circulares.
  4. Hacer clic sobre un icono de acceso directo en *Quick Launch* (Ej: Assign Leave).
* **Resultado Esperado:**
  1. Todos los widgets cargan sin errores del tipo "404" o "Data not found".
  2. El widget "Time at Work" muestra el estado actual del reloj del usuario.
  3. Los gráficos circulares son interactivos (muestran etiquetas de datos al pasar el mouse).
  4. Los botones de atajo redirigen correctamente a sus pantallas operativas correspondientes.
* **Tipo:** UI / Interfaz de Usuario e Integración
* **Prioridad:** Media

---

### Módulo 8: Claim (Gestión de Reclamos)

#### 🔍 Caso de Prueba #14
* **ID:** `TC-CLAIM-014`
* **Título:** Crear y asignae exitosa de un evento de reclamo
* **Módulo:** Claim
* **Precondición:** El usuario que ejecuta posee privilegios de Admin o Claim Manager.
* **Datos de prueba:** * Employee Name: `Alice Duval`
  * Event: `Accommodation` (Alojamiento)
  * Currency: `United States Dollar`
  * Remarks: `Reembolso por estadía en conferencia de tecnología.`
* **Pasos:**
  1. Navegar al menú lateral "Claim" y seleccionar la acción "Assign Claim".
  2. Buscar y seleccionar la empleada `Alice Duval`.
  3. Seleccionar la categoría de evento `Accommodation` en el menú desplegable.
  4. Configurar la moneda en `United States Dollar`.
  5. Redactar las observaciones en el bloque de notas de texto "Remarks".
  6. Hacer clic en el botón "Create".
* **Resultado Esperado:** El flujo concluye exitosamente guardando la cabecera del reclamo y mostrando la alerta superior flotante *"Successfully Saved"*.
* **Tipo:** Positiva (Funcional)
* **Prioridad:** Alta

#### 🔍 Caso de Prueba #15
* **ID:** `TC-CLAIM-015`
* **Título:** Validar de campos requeridos obligatorios al asignar un reclamo
* **Módulo:** Claim
* **Precondición:** Acceder a la sección "Assign Claim" y omitir la entrada de datos.
* **Datos de prueba:** Formulario vacío.
* **Pasos:**
  1. Entrar a la interfaz de asignación de reclamos.
  2. Mantener todos los campos de selección y búsqueda completamente en blanco.
  3. Hacer clic directamente en el botón "Create".
* **Resultado Esperado:** El sistema detiene el envío, bloquea el guardado y resalta en rojo los campos obligatorios (*Employee Name*, *Event* y *Currency*) acompañados de
