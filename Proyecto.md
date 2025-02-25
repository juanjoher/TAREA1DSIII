# Sistema de Gestión de Órdenes y Entregas con Microservicios

## Integrantes Grupo 11
- Marlon Astudillo - 202259462 
- Laura Couicue - 202276652
- Juan José Gallego - 202259433 
- Juan José Hernández - 202259500 
- Laura Peñaloza - 202259485

## 1. Descripción General 
El objetivo del proyecto es desarrollar un sistema basado en microservicios para la gestión de órdenes de compra y entregas en una tienda en línea. Este sistema permitirá a los clientes realizar pedidos, a los administradores gestionar el inventario 
y a los repartidores consultar rutas de entrega en tiempo real. 

El proyecto será desarrollado en equipos aplicando la metodología SCRUM, 
utilizando herramientas y tecnologías modernas para el desarrollo, integración y 
despliegue de microservicios.

## 2. Requisitos del Sistema  

### 2.1 Microservicios del Proyecto
- Gestión de Usuarios.
  - Registro y autenticación de usuarios
  - Roles: Cliente, Administrador, Repartidor.

-  Gestión de Productos e Inventario.
    - CRUD de productos con control de stock.  
    - Búsqueda y categorización de productos.

- Gestión de Órdenes de Compra  
  - Creación y seguimiento de órdenes de compra. 
  - Integración con sistema de pagos simulado. 
  - Notificaciones a los usuarios. 

- Gestión de Entregas y Rutas 
  - Asignación de pedidos a repartidores.
  - Seguimiento de entregas en tiempo real. 

- API Gateway  
  - Administración centralizada de acceso a los servicios.
  - Control de autenticación y balanceo de carga

- Sistema de Monitoreo y Logs   
  - Registro de eventos y métricas del sistema. 
  - Generación de alertas sobre fallos o comportamientos inesperados.



## 3. Requisitos de Calidad del Proyecto 
- **Disponibilidad:**  El sistema debe garantizar acceso continuo a los servicios críticos. En caso de fallo de un servicio, las solicitudes deben redirigirse automáticamente a instancias activas y el sistema debe generar una alerta de recuperación.   


- **Escalabilidad:** La infraestructura debe permitir la expansión del sistema sin afectar su rendimiento. Si la carga del sistema supera cierto umbral, deben desplegarse automáticamente nuevas instancias de los microservicios.


- **Rendimiento:** Las solicitudes deben responder en un tiempo óptimo. Si el tiempo de respuesta de un servicio supera los 300 ms, el sistema debe aplicar estrategias de optimización de consultas y reducción de latencia.  


- **Facilidad de modificación y mantenibilidad:** Los microservicios deben 
diseñarse de forma modular para permitir cambios sin afectar otros servicios. 
Si una nueva funcionalidad requiere modificaciones en más de un 
microservicio, estas deben ser documentadas y probadas antes de su 
despliegue en producción. 


- **Seguridad:** La confidencialidad e integridad de los datos deben garantizarse en todo momento. Si se detecta un intento de acceso no autorizado, el sistema debe registrar el evento y bloquear al usuario automáticamente. 


- **Garantía de entrega de mensajes:**  La comunicación entre microservicios debe asegurar que los mensajes sean procesados sin pérdidas ni duplicaciones. Si un mensaje no se procesa correctamente, debe reenviarse a una cola de eventos pendientes para su procesamiento posterior. 

## 4. Tecnologías y Herramientas  
- **Backend:** Spring Boot para desarrollo de microservicios. 
- **Autenticación:**  OAuth2 y JWT para validación de identidad.
- **Mensajería Asíncrona:**  Kafka o RabbitMQ para comunicación entre 
microservicios.
- **Orquestación:**  Kubernetes para gestionar despliegues y escalabilidad. 
- **CI/CD:** GitHub Actions para integración y despliegue continuo. 
- **Pruebas Automatizadas:**  JUnit, Mockito, Testcontainers para validar la funcionalidad del sistema. 
- **Monitoreo:** Prometheus y Grafana para registrar métricas y eventos en el sistema.   
- **API Gateway:**  Spring Cloud Gateway o Kong para gestionar el acceso a los microservicios. 