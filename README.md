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

### TC-002 - Validación de Contraseña Incorrecta
**Pasos:**
1. Abrir la interfaz de Login de WILPOS.
2. Ingresar un usuario válido.
3. Ingresar una contraseña errónea.
4. Presionar "Entrar".

**Resultado Esperado:** El sistema debe denegar el acceso y mostrar el mensaje de alerta: *"Usuario o contraseña incorrectos."*

---
## Caso de Prueba: US-01 - Acceso y Validación:
### ID: TC-01
1. Titulo: Acceso y Validación de Licencia Demo
2. Modulo: Configuración / Licenciamiento
3. Precondiciones: Aplicación Wilpos instalada y en pantalla de inicio(Login/licencia.
4. Datos: Llave “DEMO”

5. Pasos: 
1.	Buscar la app llamada “WILPOS”  
2.	Iniciar la aplicación 
3.	Dirigirse al módulo de Configuración.
4. Seleccionar la sección de Estado de Licencia.
5-	4. Verificar el estado de la licencia y el texto descriptivo del plan.

Resultado Esperado El sistema debe permitir el acceso al ingresar una llave válida de tipo "DEMO" en el campo de licencia.
Resultado actua: El sistema  mostro  la licencia como "Activa" y el texto descriptivo exactamente: " Demo gratuito"  

---
## Caso de Prueba: US-02 - Verificación de Indicador en Footer
### ID: TC-02
Titulo: Validación de texto persistente en el pie de página (Footer)
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
## Caso de Prueba: US-03 - Unificación del Flujo de Entrada
### ID: TC-03
Titulo: Verificación de flujo de entrada unificado (Sin botón independiente)
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
## Caso de Prueba: US-01 - Búsqueda y Selección de Productos
### ID: TC-04 
Titulo: Búsqueda por nombre y selección manual de productos en el POS(Punto de Venta)
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

## Caso de Prueba: US-02 - Selección de Métodos de Pago
### ID: TC-05
Titulo: Validación de métodos de pago: Efectivo 
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

## Caso de Prueba: US-02 - Selección de Métodos de Pago
### ID: TC-06
Titulo: Validación de métodos de pago: Tarjeta
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

## Caso de Prueba: US-02 - Visualización de Comprobante (PDF)

### ID: TC-07
Titulo: visualización de factura en formato digital
Modulo: caja (punto de venta)
Precondiciones: Venta finalizada con método de pago seleccionado (Efectivo).
Datos: producto jabon
Pasos:
1. DFinalizar la venta del producto "jabon". 
2. Confirmar el pago (Método: efectivo)  
3. Haz clic en el botón  “ Confirmar “. 
4. Verificar la apertura automática de la "Vista Previa de Factura".
 
Resultado esperado: Restricción de Impresión: Al finalizar una venta, no se enviará comando a impresoras físicas, pero debe abrirse un visor de PDF con el recibo generado
Resultado actual: EXITOSO. Se generó la Factura #5. El sistema calculó correctamente el ITBIS (RD$4.50 sobre un neto de RD$25.00) y muestra todos los campos requeridos en el visor digital
Tipo de Prueba: Funcional / Salida de Datos.

---

## Caso de Prueba: US-08 - Verificación de Cálculos de ITBIS
### ID: TC-08
Titulo: Validación de cálculo automático de ITBIS (18%)
Modulo: Caja “venta”
Precondiciones: El producto en el carrito debe estar marcado como gravado con el 18%.
Datos: Precio Neto: RD$25.00 / Tasa ITBIS: 18%
Pasos:
1.	Tener agregado un producto al carrito (Ej: Jabón).  
2. Verificar el desglose de precios en la parte inferior del carrito.  
3.	Finalizar la venta y revisar el desglose en el comprobante PDF.  

Resultado esperado: El cálculo de ITBIS (18%) debe aplicarse correctamente sobre los productos gravados del dataset de prueba.
Resultado actual: 
EXITOSO. Como se observa en la captura, el sistema realiza el cálculo inverso correctamente: RD$25.00 (Neto) x 0.18 = RD$4.50. La suma total coincide perfectamente con el precio del producto.  

---


