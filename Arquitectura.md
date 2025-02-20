# TAREA1DSIII

## 1. Introducción  
Este documento describe la arquitectura inicial del sistema de gestión de órdenes y entregas, incluyendo requisitos funcionales, requisitos de calidad y restricciones clave que deben ser consideradas en el diseño del software.

**Integrantes:**     
Juan José Hernández 2259500\
			Juan José Gallego 2259433\
			Marlon Astudillo 2259462\
			Laura Peñaloza 2259485\
			Laura Couicue  2276652\
**Fecha:** _20/02/2025_  

---

## 2. Requisitos Funcionales  
Los requisitos funcionales se presentan en forma de **historias de usuario**, especificando los **criterios de aceptación**.

### **Historias de Usuario**
| **Número**    | **Historia de Usuario**                                                                                                           | **Criterios de Aceptación**                                                                                                                                                                                                                                                                                            |
| --------- | --------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **US-01** | _Como cliente registrado, quiero iniciar sesión en la plataforma para acceder a mi historial de pedidos y realizar nuevas compras._ | _- El usuario debe ingresar un correo y contraseña válidos.<br>- Si las credenciales son correctas, el usuario es redirigido a su perfil.<br>- Si las credenciales son incorrectas, se muestra un mensaje de error sin revelar detalles específicos.<br>- El usuario puede solicitar un restablecimiento de contraseña._ |
| **US-02** | _Como cliente registrado, quiero que la plataforma me permita agregar al carrito los productos para poder realizar mi compra con éxito._                                   | _- El usuario debe agregar productos al carrito.<br>- El usuario debe ingresar que cantidad requiere de cada producto antes de agregarlo al carrito. <br> -El usuario debe poder ver un resumen de los productos agregados al carrito, incluyendo cantidad y precio total. <br> -El usuario debe poder modificar la cantidad o eliminar productos del carrito antes de finalizar la compra._                                                                                                                                                                                                 |
| **US-03** | _Como cliente registrado, quiero que la plataforma me permita elegir entre diferentes métodos de pago para tener opciones a la hora de realizar el pago._                            | _- El usuario debe elegir entre los métodos de pago disponibles. <br> -El usuario debe digitar sus datos bancarios. <br> -El sistema debe validar la información ingresada antes de procesar el pago. <br> -El usuario debe recibir una notificación de confirmación del pago realizado._                                                                                                                                                                                                         
| **US-04** | _Como cliente registrado, quiero que la plataforma me permita filtrar los productos para hacer más fáci el proceso de compra._                            | _- El usuario debe poder filtrar por la categoria del producto. <br> -El usuario debe poder combinar múltiples filtros en una misma búsqueda. <br> -Los resultados deben actualizarse dinámicamente según los filtros aplicados._                                                                                                                                                                                                         


>  **Instrucciones:**  
> - Completar al menos **tres historias de usuario**.  
> - Asegurar que cada historia tenga criterios de aceptación claros y verificables.  

---

## 3. Requisitos de Calidad  
Los requisitos de calidad se presentan en forma de **historias de calidad**, siguiendo la estructura de Len Bass.

### **Historias de Calidad**
| **ID**    | **Fuente**               | **Estímulo**                                                                                             | **Artefactos**                                                  | **Entorno**             | **Respuesta**                                                          | **Medida de Respuesta**                                                                                 |
| --------- | ------------------------ | -------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- | ----------------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| **RQ-01** | Desarrollador            | Se solicita modificar la lógica de asignación de pedidos para incluir nuevos criterios de prioridad.     | Código y configuración de reglas de negocio.                    | Tiempo de ejecución     | Se debe modificar, probar y desplegar la nueva lógica de asignación.   | El esfuerzo requerido no debe superar 2 horas de trabajo y no deben generarse más de 2 defectos nuevos. |
| **RQ-02** | _Ingeniero de seguridad_ | _Proteger las credenciales y datos de clientes frente a algunos ataques de inyección_                    | _Mecanismos de cifrado, base de datos y código_                 | _Pruebas de seguridad_  | _Se debe aplicar cifrado fuerte, validar entradas contra inyecciones._ | _El esfuerzo que se requiere es que deben de trabajarlo hasta que no se encuentren vulnerabilidades_    |
| **RQ-03** | _DevOps_                 | _El sistema debe de poder escalar horizontalmente para soportar un 50% de aumento en la demanda mensual_ | _Configuración de la infraestructura y balanceamiento de carga_ | _Entorno de producción_ | _Se debe de implementar un autoescalado y un balanceo dinámico_        | _La infraestructura debe adaptarse automáticamente sin intervención manual._                            |
|           |                          |                                                                                                          |                                                                 |                         |                                                                        |                                                                                                         |

>  **Instrucciones:**  
> - Completar al menos **tres historias de calidad**, alineadas con atributos clave como **rendimiento, escalabilidad y seguridad**.  
> - Definir cómo se medirá la respuesta esperada ante la situación planteada.  

---

## 4. Restricciones del Sistema  
Las restricciones establecen **limitaciones** en la arquitectura del sistema, ya sean tecnológicas, de negocio, regulatorias o de infraestructura.

### **Lista de Restricciones**
| **Tipo de Restricción** | **Descripción**                                                                                                                                                          |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Tecnológica             | El sistema debe desarrollarse utilizando **Spring Boot y PostgreSQL**, debido a la infraestructura actual de la empresa y su compatibilidad con otros sistemas internos. |
| _Regulatoria_           | _Se debe de cumplir con una norma de seguridad como la ISO  27001 para la protección de datos personales_                                                                |
|                         |                                                                                                                                                                          |

>  **Tipos de restricciones:**  
> - **Tecnológicas:** Lenguajes, frameworks o herramientas que deben utilizarse.  
> - **De negocio:** Normativas o estándares de la empresa.  
> - **Regulatorias:** Cumplimiento de normativas legales o de seguridad.  
> - **De infraestructura:** Limitaciones en hardware, red o almacenamiento.  


---

## 5. Formato de Entrega  
- **Formato:** Markdown (`.md`) en el repositorio de Codelabs, El documento debe llamarse `Arquitectura.md`.  
- **Extensión máxima:** 3 páginas.  

---

## **Tiempo estimado para completar el ejercicio: 50 minutos**  
**15 min** → Definir **3 historias de usuario con criterios de aceptación**.  
**15 min** → Definir **3 historias de calidad alineadas con atributos clave**.  
**10 min** → Identificar **2 restricciones relevantes**.  
**10 min** → Revisión y ajustes finales del documento.
