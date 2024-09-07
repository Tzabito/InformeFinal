**UNIVERSIDAD PERUANA DE CIENCIAS APLICADAS**

![Logotipo Descripción generada automáticamente](https://res.cloudinary.com/daassyisd/image/upload/v1714691535/gmplcgrlsv9sihpusivm.png)

**SI572-2402-WV71 Desarrollo de Soluciones IOT**

Informe de Trabajo Final TB1

**Carrera:** Ingeniería de Software

**Ciclo:** 07

**Sección:** WV71

**Profesor:** Angel Augusto Velasquez Nuñez

**Startup:** Fractalies

**Producto:** Green Tools

**Integrantes:**

Miguel Angel Ramirez Alfaro (U20)

Lino Abraham Quenta Leon (U202022353)

Giovanni Andres Ramos Calderon (U20)

Jean Patrick Yemsi Sanchez Rios (U20)

Franco Felix Yance Gutierrez (U20)

**Agosto, 25 de 2024**

# Registro de Versiones del Informe

| Versión | Fecha | Autor | Descripción de modificación |
|---------|-------|-------|---------------------------|
| 1.0 | 2024-08-20 | Miguel Angel  | Versión inicial del informe |
| 1.1 | 2024-08-22 | Lino Quenta | Adición de la sección "Lean UX Process" |
| 1.2 | 2024-08-23 | Giovanni Andres | Corrección de errores en la sección "Competidores" |
| 1.3 | 2024-08-27 | Miguel Angel | Mejora de la sección "User Personas" basada en retroalimentación del docente |
| 1.4 | 2024-08-29 | Lino Quenta | Adición de la sección "Impact Mapping" |
| 2.0 | 2024-08-30 |Giovanni Andres| Reestructuración completa del informe para mejorar la coherencia |
| 2.1 | 2024-09-22 | Jean Patrick | Actualización de la sección "Software Architecture" |
| 2.3 | 2024-09-05 | Jean Patrick | Adición de la sección "Solution UX Design" |
| 2.4 | 2024-09-20 | Lino Quenta | Mejoras en las Hisotorias de Usuario.|
| 3.0 | 2024-09-26 | Giovanni Andres  | Mejoras en la arquitectura de C4 Model. |

Contenido

- [Capítulo I: Introducción](#capítulo-i-introducción)
  - [1.1. Startup Profile](#11-startup-profile)
    - [1.1.1. Descripción de la Startup](#111-descripción-de-la-startup)
    - [1.1.2. Perfiles de integrantes del equipo](#112-perfiles-de-integrantes-del-equipo)
  - [1.2. Solution Profile](#12-solution-profile)
    - [1.2.1. Antecedentes y problemática](#121-antecedentes-y-problemática)
    - [1.2.2. Lean UX Process](#122-lean-ux-process)
      - [1.2.2.1. Lean UX Problem Statements](#1221-lean-ux-problem-statements)
      - [1.2.2.2. Lean UX Assumptions](#1222-lean-ux-assumptions)
      - [1.2.2.3. Lean UX Hypothesis Statements](#1223-lean-ux-hypothesis-statements)
      - [1.2.2.4. Lean UX Canvas](#1224-lean-ux-canvas)
  - [1.3. Segmentos objetivo](#13-segmentos-objetivo)
  
- [Capítulo II: Requirements Elicitation & Analysis](#capítulo-ii-requirements-elicitation--analysis)
  - [2.1. Competidores](#21-competidores)
    - [2.1.1. Análisis competitivo](#211-análisis-competitivo)
    - [2.1.2. Estrategias y tácticas frente a competidores](#212-estrategias-y-tácticas-frente-a-competidores)
  - [2.2. Entrevistas](#22-entrevistas)
    - [2.2.1. Diseño de entrevistas](#221-diseño-de-entrevistas)
    - [2.2.2. Registro de entrevistas](#222-registro-de-entrevistas)
    - [2.2.3. Análisis de entrevistas](#223-análisis-de-entrevistas)
  - [2.3. Needfinding](#23-needfinding)
    - [2.3.1. User Personas](#231-user-personas)
    - [2.3.2. User Task Matrix](#232-user-task-matrix)
    - [2.3.3. User Journey Mapping](#233-user-journey-mapping)
    - [2.3.4. Empathy Mapping](#234-empathy-mapping)
    - [2.3.5. As-is Scenario Mapping](#235-as-is-scenario-mapping)
  - [2.4. Ubiquitous Language](#24-ubiquitous-language)

- [Capítulo III: Requirements Specification](#capítulo-iii-requirements-specification)
  - [3.1. To-Be Scenario Mapping](#31-to-be-scenario-mapping)
  - [3.2. User Stories](#32-user-stories)
  - [3.3. Impact Mapping](#33-impact-mapping)
  - [3.4. Product Backlog](#34-product-backlog)

- [Capítulo IV: Solution Software Design](#capítulo-iv-solution-software-design)
  - [4.1. Strategic-Level Domain-Driven Design](#41-strategic-level-domain-driven-design)
    - [4.1.1. EventStorming](#411-eventstorming)
      - [4.1.1.1 Candidate Context Discovery](#4111-candidate-context-discovery)
      - [4.1.1.2 Domain Message Flows Modeling](#4112-domain-message-flows-modeling)
      - [4.1.1.3 Bounded Context Canvases](#4113-bounded-context-canvases)
    - [4.1.2. Context Mapping](#412-context-mapping)
    - [4.1.3. Software Architecture](#413-software-architecture)
      - [4.1.3.1. Software Architecture System Landscape Diagram](#4131-software-architecture-system-landscape-diagram)
      - [4.1.3.2. Software Architecture Context Level Diagrams](#4132-software-architecture-context-level-diagrams)
      - [4.1.3.2. Software Architecture Container Level Diagrams](#4132-software-architecture-container-level-diagrams)
      - [4.1.3.3. Software Architecture Deployment Diagrams](#4133-software-architecture-deployment-diagrams)
  - [4.2. Tactical-Level Domain-Driven Design](#42-tactical-level-domain-driven-design)
    - [4.2.1. Bounded Context: \<Bounded Context Name>](#421-bounded-context-bounded-context-name)
      - [4.2.1.1. Domain Layer](#4211-domain-layer)
      - [4.2.1.2. Interface Layer](#4212-interface-layer)
      - [4.2.1.3. Application Layer](#4213-application-layer)
      - [4.2.1.4. Infrastructure Layer](#4214-infrastructure-layer)
      - [4.2.1.6. Bounded Context Software Architecture Component Level Diagrams](#4216-bounded-context-software-architecture-component-level-diagrams)
      - [4.2.1.7. Bounded Context Software Architecture Code Level Diagrams](#4217-bounded-context-software-architecture-code-level-diagrams)
      - [4.2.1.7.1. Bounded Context Domain Layer Class Diagrams](#42171-bounded-context-domain-layer-class-diagrams)
      - [4.2.1.7.2. Bounded Context Database Design Diagram](#42172-bounded-context-database-design-diagram)

- [Capítulo V: Solution UI/UX Design](#capítulo-v-solution-uiux-design)
  - [5.1. Style Guidelines](#51-style-guidelines)
    - [5.1.1. General Style Guidelines](#511-general-style-guidelines)
    - [5.1.2. Web, Mobile and IoT Style Guidelines](#512-web-mobile-and-iot-style-guidelines)
  - [5.2. Information Architecture](#52-information-architecture)
    - [5.2.1. Organization Systems](#521-organization-systems)
    - [5.2.2. Labeling Systems](#522-labeling-systems)
    - [5.2.3. SEO Tags and Meta Tags](#523-seo-tags-and-meta-tags)
    - [5.2.4. Searching Systems](#524-searching-systems)
    - [5.2.5. Navigation Systems](#525-navigation-systems)
  - [5.3. Landing Page UI Design](#53-landing-page-ui-design)
    - [5.3.1. Landing Page Wireframe](#531-landing-page-wireframe)
    - [5.3.2. Landing Page Mock-up](#532-landing-page-mock-up)
  - [5.4. Applications UX/UI Design](#54-applications-uxui-design)
    - [5.4.1. Applications Wireframes](#541-applications-wireframes)
    - [5.4.2. Applications Wireflow Diagrams](#542-applications-wireflow-diagrams)
    - [5.4.3. Applications Mock-ups](#543-applications-mock-ups)
    - [5.4.4. Applications User Flow Diagrams](#544-applications-user-flow-diagrams)
  - [5.5. Applications Prototyping](#55-applications-prototyping)

- [Capítulo VI: Product Implementation, Validation & Deployment](#capítulo-vi-product-implementation-validation--deployment)
  - [6.1. Software Configuration Management](#61-software-configuration-management)
    - [6.1.1. Software Development Environment Configuration](#611-software-development-environment-configuration)
    - [6.1.2. Source Code Management](#612-source-code-management)
    - [6.1.3. Source Code Style Guide & Conventions](#613-source-code-style-guide--conventions)
    - [6.1.4. Software Deployment Configuration](#614-software-deployment-configuration)
  - [6.2. Landing Page, Services & Applications Implementation](#62-landing-page-services--applications-implementation)
    - [6.2.1. Sprint 1](#621-sprint-1)
      - [6.2.1.1. Sprint Planning n](#6211-sprint-planning-n)
      - [6.2.1.2. Sprint Backlog n](#6212-sprint-backlog-n)
      - [6.2.1.3. Development Evidence for Sprint Review](#6213-development-evidence-for-sprint-review)
      - [6.2.1.4. Testing Suite Evidence for Sprint Review](#6214-testing-suite-evidence-for-sprint-review)
      - [6.2.1.5. Execution Evidence for Sprint Review](#6215-execution-evidence-for-sprint-review)
      - [6.2.1.6. Services Documentation Evidence for Sprint Review](#6216-services-documentation-evidence-for-sprint-review)
      - [6.2.1.7. Software Deployment Evidence for Sprint Review](#6217-software-deployment-evidence-for-sprint-review)
      - [6.2.1.8. Team Collaboration Insights during Sprint](#6218-team-collaboration-insights-during-sprint)
    - [6.2.2. Sprint 2](#622-sprint-2)
      - [6.2.2.1. Sprint Planning n](#6221-sprint-planning-n)
      - [6.2.2.2. Sprint Backlog n](#6222-sprint-backlog-n)
      - [6.2.2.3. Development Evidence for Sprint Review](#6223-development-evidence-for-sprint-review)
      - [6.2.2.4. Testing Suite Evidence for Sprint Review](#6224-testing-suite-evidence-for-sprint-review)
      - [6.2.2.5. Execution Evidence for Sprint Review](#6225-execution-evidence-for-sprint-review)
      - [6.2.2.6. Services Documentation Evidence for Sprint Review](#6226-services-documentation-evidence-for-sprint-review)
      - [6.2.2.7. Software Deployment Evidence for Sprint Review](#6227-software-deployment-evidence-for-sprint-review)
      - [6.2.2.8. Team Collaboration Insights during Sprint](#6228-team-collaboration-insights-during-sprint)
  - [6.3. Validation Interviews](#63-validation-interviews)
    - [6.3.1. Diseño de Entrevistas](#631-diseño-de-entrevistas)
    - [6.3.2. Registro de Entrevistas](#632-registro-de-entrevistas)
    - [6.3.3. Evaluaciones según heurísticas](#633-evaluaciones-según-heurísticas)
  - [6.4. Video About-the-Product](#64-video-about-the-product)

# Project Report Collaboration Insights

URL de nuestro repositorio para el Project Report:[ https://github.com/linoabraham/Fractalis](https://github.com/FractalisGrupo03IOT/InformeFinal)

## Desarrollo de actividades y colaboración

### Entrega 1 (TB1)

Aca las primeras cosas que se trabajaran 

### Entrega 2 (TP1)

-----

### Entrega 3 (TB2)

-----

### Entrega 4 (TF1)

----

## Evidencia de colaboración

![image](url aca)




# Student Outcome

| Competencia ABET | Criterio específico                                                                                             | Acciones realizadas |
|------------------|-----------------------------------------------------------------------------------------------------------------|---------------------|
| **ABET 5**       | **Criterio 1:** Trabaja en equipo para proporcionar liderazgo en forma conjunta                                  |                     |
|                  | **Criterio 2:** Crea un entorno colaborativo e inclusivo, establece metas, planifica tareas y cumple objetivos    |                     |



# Capítulo I: Introducción

## 1.1. Startup Profile

### 1.1.1. Descripción de la Startup

### 1.1.2. Perfiles de integrantes del equipo

## 1.2. Solution Profile

### 1.2.1. Antecedentes y problemática

### 1.2.2. Lean UX Process

#### 1.2.2.1. Lean UX Problem Statements

#### 1.2.2.2. Lean UX Assumptions

#### 1.2.2.3. Lean UX Hypothesis Statements

#### 1.2.2.4. Lean UX Canvas

## 1.3. Segmentos objetivo

# Capítulo II: Requirements Elicitation & Analysis

## 2.1. Competidores

### 2.1.1. Análisis competitivo

### 2.1.2. Estrategias y tácticas frente a competidores

## 2.2. Entrevistas

### 2.2.1. Diseño de entrevistas

### 2.2.2. Registro de entrevistas

### 2.2.3. Análisis de entrevistas

## 2.3. Needfinding

### 2.3.1. User Personas

### 2.3.2. User Task Matrix

### 2.3.3. User Journey Mapping

### 2.3.4. Empathy Mapping

### 2.3.5. As-is Scenario Mapping

## 2.4. Ubiquitous Language

# Capítulo III: Requirements Specification

## 3.1. To-Be Scenario Mapping
### Cultivadores de invernadero

[![Imagen de Cultivadores de invernadero](https://media.discordapp.net/attachments/1228537935368945717/1277297738538815602/Diagrama_en_blanco_-_Pagina_1_1.png?ex=66dd2277&is=66dbd0f7&hm=76955413de78a6701e14fe2f56c79f69b49266772ca2a19b51e60667d9ba1f4a&=&format=webp&quality=lossless&width=1025&height=345)]

### Micro cultivo

[![Imagen de Micro cultivo](https://media.discordapp.net/attachments/1228537935368945717/1277297738903589117/Diagrama_en_blanco_-_Pagina_1.png?ex=66dd2277&is=66dbd0f7&hm=dac1156e5fd3a1d76c553a76d72e6591a17365f1031ec626019c5e52a5326d4e&=&format=webp&quality=lossless&width=1025&height=345)]

## 3.2. User Stories
### Epics

| Epic ID | Título                        | Descripción                                                                                                                                  |
|---------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| EP1     | Landing Page                  | Desarrollo de la página de aterrizaje para Green Tools con secciones de encabezado, beneficios, características, planes y precios, testimonios y footer. |
| EP2     | Aplicación Móvil              | Desarrollo de la aplicación móvil en Flutter que incluye monitoreo en tiempo real, control remoto, visualización de datos históricos, gestión de perfiles de cultivo, alertas y notificaciones, y configuración de horarios de dispositivos. |
| EP3     | Aplicación Web                | Desarrollo de la aplicación web en Angular que incluye dashboard centralizado, administración de cultivos, análisis y reportes, gestión de dispositivos IoT, y gestión de usuarios y permisos. |
| EP4     | Backend, Lógica de Negocio e IoT   | Desarrollo del backend en Spring Boot para la gestión de cultivos, sensores, dispositivos, usuarios, automatización, integración con IoT y generación de reportes. Además, incluye la configuración de un simulador IoT utilizando Wokwi con ESP32 para la simulación de sensores y actuadores como un servo motor para la automatización. |

### Historias de Usuario - AgroVision

| Epic / Story ID | Título                                  | Descripción                                                                                                                                                        | Criterios de Aceptación                                                                                                                                                   | Relacionado con (Epic ID) |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| EP1/US1         | Crear Encabezado Principal              | Como visitante, quiero ver un encabezado atractivo con el título y subtítulo de Green Tools para captar mi interés.                                                 | **SCENARIO 1**: Visualización del encabezado principal. <br> **Dado** que estoy en la landing page, **Cuando** veo el encabezado, **Entonces** debo ver el título "Green Tools: La Revolución en Cultivos Controlados de Precisión" y el subtítulo. | EP1                       |
| EP1/US2         | Mostrar Beneficios Clave                | Como visitante, quiero leer los beneficios clave de AgroVision para entender por qué elegirlo.                                                                     | **SCENARIO 1**: Lectura de beneficios clave. <br> **Dado** que estoy en la sección de beneficios, **Cuando** leo la sección, **Entonces** debo ver los beneficios clave como monitoreo en tiempo real, control inteligente, análisis y soporte. | EP1                       |
| EP1/US3         | Destacar Características Clave          | Como visitante, quiero conocer las características principales de Green Tools para evaluar sus capacidades.                                                         | **SCENARIO 1**: Visualización de características clave. <br> **Dado** que estoy en la sección de características, **Cuando** leo la sección, **Entonces** debo ver características como integración IoT avanzada, interfaz intuitiva, alertas, y personalización. | EP1             |
| EP1/US4         | Mostrar Planes y Precios                | Como visitante, quiero ver los planes y precios disponibles para elegir el que mejor se adapte a mis necesidades.                                                  | **SCENARIO 1**: Visualización de planes y precios. <br> **Dado** que estoy en la sección de planes y precios, **Cuando** leo la sección, **Entonces** debo ver una descripción clara de los planes Básico y Premium con llamadas a la acción correspondientes. | EP1           |
| EP1/US5         | Mostrar Testimonios y Casos de Éxito    | Como visitante, quiero leer testimonios y casos de éxito para ver cómo otros han mejorado con Green Tools.                                                          | **SCENARIO 1**: Visualización de testimonios y casos de éxito. <br> **Dado** que estoy en la sección de testimonios, **Cuando** leo la sección, **Entonces** debo ver testimonios reales de clientes y casos de éxito que demuestren los beneficios de AgroVision. | EP1           |
| EP1/US6         | Implementar Footer                      | Como visitante, quiero encontrar información de contacto y enlaces legales al final de la página para obtener más detalles y soporte.                              | **SCENARIO 1**: Visualización de footer. <br> **Dado** que estoy en el footer, **Cuando** leo la sección, **Entonces** debo ver enlaces a contacto, redes sociales, política de privacidad, y términos de servicio.                      | EP1                       |
| EP2/US1         | Monitoreo en Tiempo Real                | Como usuario, quiero ver datos en tiempo real de mis cultivos para monitorear sus condiciones actuales.                                                            | **SCENARIO 1**: Visualización de datos en tiempo real. <br> **Dado** que estoy en la aplicación móvil, **Cuando** accedo a la sección de monitoreo, **Entonces** debo ver gráficos interactivos con datos actualizados de temperatura, humedad y nutrientes. | EP2            |
| EP2/US2         | Control Remoto de Dispositivos          | Como usuario, quiero controlar dispositivos conectados desde la aplicación para gestionar mi cultivo.                                                              | **SCENARIO 1**: Control de dispositivos de forma remota. <br> **Dado** que estoy en la aplicación móvil, **Cuando** accedo a la sección de control remoto, **Entonces** debo poder encender/apagar dispositivos y ajustar parámetros manualmente o de forma automática. | EP2        |
| EP2/US3         | Visualización de Datos Históricos       | Como usuario, quiero ver datos históricos de mis cultivos para analizar tendencias y patrones.                                                                     | **SCENARIO 1**: Visualización de datos históricos. <br> **Dado** que estoy en la sección de datos históricos, **Cuando** accedo a los gráficos, **Entonces** debo poder seleccionar rangos de fechas y comparar diferentes períodos de tiempo.      | EP2                       |
| EP2/US4         | Gestión de Perfiles de Cultivo          | Como usuario, quiero crear y gestionar perfiles de cultivo personalizados para ajustar parámetros específicos.                                                    | **SCENARIO 1**: Creación y gestión de perfiles de cultivo. <br> **Dado** que estoy en la sección de perfiles de cultivo, **Cuando** creo o edito un perfil, **Entonces** debo poder ajustar parámetros como humedad, temperatura, y nutrientes, y guardar la configuración. | EP2         |
| EP2/US5         | Configuración de Alertas y Notificaciones| Como usuario, quiero recibir notificaciones sobre condiciones críticas para tomar acciones rápidamente.                                                             | **SCENARIO 1**: Configuración de alertas y notificaciones. <br> **Dado** que estoy en la aplicación móvil, **Cuando** se detecta una condición crítica, **Entonces** debo recibir una notificación push o local con información relevante sobre la situación del cultivo. | EP2       |
| EP2/US6         | Configuración de Horarios de Dispositivos| Como usuario, quiero programar horarios para los dispositivos conectados para automatizar tareas.                                                                  | **SCENARIO 1**: Programación de horarios de dispositivos. <br> **Dado** que estoy en la sección de configuración de horarios, **Cuando** configuro un horario, **Entonces** debo poder elegir fechas y horas, y guardar la configuración para que el dispositivo actúe automáticamente. | EP2      |
| EP2/US7         | Iniciar Sesión                          | Como usuario, quiero iniciar sesión en la aplicación para acceder a mis datos personales y configuraciones.                                                       | **SCENARIO 1**: Inicio de sesión. <br> **Dado** que estoy en la pantalla de inicio de sesión, **Cuando** ingreso mis credenciales, **Entonces** debo poder acceder a mi cuenta y ver mis datos personales.                         | EP2                       |
| EP3/US1         | Dashboard Centralizado                  | Como usuario, quiero ver una vista integral de todos mis cultivos y datos en tiempo real para un análisis centralizado.                                            | **SCENARIO 1**: Visualización de dashboard centralizado. <br> **Dado** que estoy en el dashboard, **Cuando** accedo a la vista centralizada, **Entonces** debo ver métricas clave, gráficos interactivos y mapas de calor sobre el estado de los cultivos y sensores. | EP3         |
| EP3/US2         | Administración de Cultivos              | Como usuario, quiero gestionar y configurar mis cultivos desde la aplicación web para ajustar sus parámetros.                                                     | **SCENARIO 1**: Administración de cultivos. <br> **Dado** que estoy en la sección de administración de cultivos, **Cuando** edito la configuración de un cultivo, **Entonces** debo poder ajustar parámetros específicos y ver el estado general del cultivo. | EP3      |
| EP3/US3         | Generación de Reportes                  | Como usuario, quiero generar y exportar reportes detallados sobre mis cultivos para análisis y seguimiento.                                                       | **SCENARIO 1**: Generación de reportes. <br> **Dado** que estoy en la sección de reportes, **Cuando** genero un reporte, **Entonces** debo poder personalizar el contenido, exportar en PDF o CSV, y ver un resumen visual de los datos. | EP3          |
| EP3/US4         | Gestión de Dispositivos IoT             | Como usuario, quiero gestionar dispositivos IoT conectados desde la web para ver su estado y ajustar configuraciones.                                             | **SCENARIO 1**: Gestión de dispositivos IoT. <br> **Dado** que estoy en la sección de gestión de dispositivos, **Cuando** accedo a la configuración de un dispositivo, **Entonces** debo ver su estado y poder ajustarlo o recibir actualizaciones sobre su rendimiento. | EP3     |
| EP3/US5         | Gestión de Usuarios y Permisos          | Como administrador, quiero gestionar cuentas de usuarios y permisos para controlar el acceso a las funcionalidades.                                                | **SCENARIO 1**: Gestión de usuarios y permisos. <br> **Dado** que estoy en la sección de gestión de usuarios, **Cuando** creo o actualizo un usuario, **Entonces** debo poder asignar roles, controlar permisos y gestionar accesos a diferentes funcionalidades. | EP3    |
| EP4/US1         | Gestión de Cultivos y Sensores          | Como desarrollador, quiero gestionar los cultivos y sensores en el backend para almacenar y actualizar datos.                                                      | **SCENARIO 1**: Gestión de cultivos y sensores. <br> **Dado** que un usuario interactúa con cultivos y sensores, **Cuando** se realizan cambios, **Entonces** el backend debe permitir la creación, actualización y consulta de cultivos y sensores. | EP4        |
| EP4/US2         | Control de Dispositivos y Automatización | Como desarrollador, quiero implementar la lógica para controlar dispositivos y aplicar reglas de automatización.                                                  | **SCENARIO 1**: Control de dispositivos y automatización. <br> **Dado** que se recibe una solicitud para controlar un dispositivo, **Cuando** el backend procesa el comando, **Entonces** debe actualizar el estado del dispositivo y aplicar las reglas de automatización correspondientes. | EP4    |
| EP4/US3         | Gestión de Usuarios y Accesos           | Como desarrollador, quiero gestionar la autenticación y permisos de usuarios para proteger el acceso a la plataforma.                                             | **SCENARIO 1**: Gestión de usuarios y accesos. <br> **Dado** que un usuario intenta autenticarse, **Cuando** proporciona credenciales válidas, **Entonces** el backend debe autenticar al usuario, generar un token JWT, y gestionar permisos de acceso según el rol. | EP4     |
| EP4/US4         | Integración con Dispositivos IoT        | Como desarrollador, quiero integrar con dispositivos IoT para enviar comandos y recibir datos.                                                                    | **SCENARIO 1**: Integración con dispositivos IoT. <br> **Dado** que se envía un comando a un dispositivo IoT, **Cuando** el backend lo procesa, **Entonces** debe enviar el comando al dispositivo y recibir datos actualizados.                  | EP4                       |
| EP4/US5         | Generación de Reportes                  | Como desarrollador, quiero generar reportes basados en datos históricos y actuales de cultivos.                                                                   | **SCENARIO 1**: Generación de reportes. <br> **Dado** que se solicita un reporte, **Cuando** el backend procesa la solicitud, **Entonces** debe generar un reporte detallado basado en datos históricos y actuales, y proporcionar los resultados en el formato solicitado. | EP4  |
| EP4/US6         | Gestión de Carga de IoT                 | Como desarrollador, quiero implementar un backend adicional para distribuir la carga o gestionar de manera más eficiente los datos que se recopilan de dispositivos IoT. | **SCENARIO 1**: Distribución de carga de IoT. <br> **Dado** que el backend principal no maneja eficientemente la carga de datos, **Cuando** se distribuye la carga al backend adicional, **Entonces** la latencia en la actualización de datos debe reducirse significativamente. | EP4 |
| EP4/US7         | Registro de Serial de Sensores IoT      | Como desarrollador, quiero registrar los seriales de los sensores IoT para mantener un control adecuado de los dispositivos conectados.                            | **SCENARIO 1**: Registro de serial de sensores IoT. <br> **Dado** que un nuevo sensor IoT es conectado, **Cuando** se registra su serial en el sistema, **Entonces** debe quedar asociado al dispositivo correspondiente y visible en el backend para su gestión. | EP4 |
| EP4/US8         | Configuración de Simulación IoT en Wokwi| Como desarrollador, quiero configurar la simulación de dispositivos IoT en Wokwi utilizando un ESP32 para probar la integración y funcionalidad de sensores y actuadores. | **SCENARIO 1**: Configuración de simulación en Wokwi. <br> **Dado** que el backend está conectado a la plataforma de simulación, **Cuando** el ESP32 recibe comandos o envía datos, **Entonces** debo poder verificar la correcta interacción de los sensores (temperatura, humedad, pH) y actuador (servo motor para válvula de riego). | EP4 |

## 3.3. Impact Mapping
[![Texto alternativo](![image](https://github.com/user-attachments/assets/13ac363f-26bf-4bb7-8f05-6116676e091c)]

## 3.4. Product Backlog


| Orden | User Story ID | Título                                 | Descripción                                                                                                                                                        | Story Points |
|-------|---------------|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| 1     | EP1/US1       | Crear Encabezado Principal             | Como visitante, quiero ver un encabezado atractivo con el título y subtítulo de Green Tools para captar mi interés.                                                 | 2            |
| 2     | EP1/US2       | Mostrar Beneficios Clave               | Como visitante, quiero leer los beneficios clave de AgroVision para entender por qué elegirlo.                                                                     | 3            |
| 3     | EP1/US3       | Destacar Características Clave         | Como visitante, quiero conocer las características principales de Green Tools para evaluar sus capacidades.                                                         | 3            |
| 4     | EP1/US4       | Mostrar Planes y Precios               | Como visitante, quiero ver los planes y precios disponibles para elegir el que mejor se adapte a mis necesidades.                                                  | 3            |
| 5     | EP1/US5       | Mostrar Testimonios y Casos de Éxito   | Como visitante, quiero leer testimonios y casos de éxito para ver cómo otros han mejorado con Green Tools.                                                          | 2            |
| 6     | EP1/US6       | Implementar Footer                     | Como visitante, quiero encontrar información de contacto y enlaces legales al final de la página para obtener más detalles y soporte.                              | 2            |
| 7     | EP2/US1       | Monitoreo en Tiempo Real               | Como usuario, quiero ver datos en tiempo real de mis cultivos para monitorear sus condiciones actuales.                                                            | 5            |
| 8     | EP2/US2       | Control Remoto de Dispositivos         | Como usuario, quiero controlar dispositivos conectados desde la aplicación para gestionar mi cultivo.                                                              | 5            |
| 9     | EP2/US3       | Visualización de Datos Históricos      | Como usuario, quiero ver datos históricos de mis cultivos para analizar tendencias y patrones.                                                                     | 4            |
| 10    | EP2/US4       | Gestión de Perfiles de Cultivo         | Como usuario, quiero crear y gestionar perfiles de cultivo personalizados para ajustar parámetros específicos.                                                    | 5            |
| 11    | EP2/US5       | Configuración de Alertas y Notificaciones| Como usuario, quiero recibir notificaciones sobre condiciones críticas para tomar acciones rápidamente.                                                             | 4            |
| 12    | EP2/US6       | Configuración de Horarios de Dispositivos| Como usuario, quiero programar horarios para los dispositivos conectados para automatizar tareas.                                                                  | 3            |
| 13    | EP2/US7       | Iniciar Sesión                         | Como usuario, quiero iniciar sesión en la aplicación para acceder a mis datos personales y configuraciones.                                                       | 2            |
| 14    | EP3/US1       | Dashboard Centralizado                 | Como usuario, quiero ver una vista integral de todos mis cultivos y datos en tiempo real para un análisis centralizado.                                            | 8            |
| 15    | EP3/US2       | Administración de Cultivos             | Como usuario, quiero gestionar y configurar mis cultivos desde la aplicación web para ajustar sus parámetros.                                                     | 6            |
| 16    | EP3/US3       | Generación de Reportes                 | Como usuario, quiero generar y exportar reportes detallados sobre mis cultivos para análisis y seguimiento.                                                       | 4            |
| 17    | EP3/US4       | Gestión de Dispositivos IoT            | Como usuario, quiero gestionar dispositivos IoT conectados desde la web para ver su estado y ajustar configuraciones.                                             | 7            |
| 18    | EP3/US5       | Gestión de Usuarios y Permisos         | Como administrador, quiero gestionar cuentas de usuarios y permisos para controlar el acceso a las funcionalidades.                                                | 5            |
| 19    | EP4/US1       | Gestión de Cultivos y Sensores         | Como desarrollador, quiero gestionar los cultivos y sensores en el backend para almacenar y actualizar datos.                                                      | 8            |
| 20    | EP4/US2       | Control de Dispositivos y Automatización| Como desarrollador, quiero implementar la lógica para controlar dispositivos y aplicar reglas de automatización.                                                  | 8            |
| 21    | EP4/US3       | Gestión de Usuarios y Accesos          | Como desarrollador, quiero gestionar la autenticación y permisos de usuarios para proteger el acceso a la plataforma.                                             | 6            |
| 22    | EP4/US4       | Integración con Dispositivos IoT       | Como desarrollador, quiero integrar con dispositivos IoT para enviar comandos y recibir datos.                                                                    | 7            |
| 23    | EP4/US5       | Generación de Reportes                 | Como desarrollador, quiero generar reportes basados en datos históricos y actuales de cultivos.                                                                   | 6            |
| 24    | EP4/US6       | Gestión de Carga de IoT                | Como desarrollador, quiero implementar un backend adicional para distribuir la carga o gestionar de manera más eficiente los datos que se recopilan de dispositivos IoT. | 8            |
| 25    | EP4/US7       | Registro de Serial de Sensores IoT     | Como desarrollador, quiero registrar los seriales de los sensores IoT para mantener un control adecuado de los dispositivos conectados.                            | 4            |
| 26    | EP4/US8       | Configuración de Simulación IoT en Wokwi| Como desarrollador, quiero configurar la simulación de dispositivos IoT en Wokwi utilizando un ESP32 para probar la integración y funcionalidad de sensores y actuadores. | 5            |



# Capítulo IV: Solution Software Design

## 4.1. Strategic-Level Domain-Driven Design

### 4.1.1. EventStorming

#### 4.1.1.1. Candidate Context Discovery
##### Step 1: Unstructured Exploration
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407433528737846/Green_Tols.jpg?ex=66d7f7d8&is=66d6a658&hm=a2af2a4f3bf9e3ceacd01c3078271745a098ca8de0c485454a35774e1184a750&=&format=webp&width=334&height=671)]
##### Step 2: Timelines
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407433260564520/Green_Tols_1.jpg?ex=66d7f7d8&is=66d6a658&hm=ea824a416d759777c7e1a6e06b2900e834b72926d8c8b8f4504b4c2570b12289&=&format=webp&width=839&height=671)]
##### Step 3: Paint Points
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407433017036830/Green_Tols_2.jpg?ex=66d7f7d8&is=66d6a658&hm=6ce9f5047c3626a8dd2545077e9a85f82aa42d3452987db05a32efd90a2b068d&=&format=webp&width=862&height=671)]
##### Step 4: Pivotal Points
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407432702459946/Green_Tols_3.jpg?ex=66d7f7d8&is=66d6a658&hm=f41f599a57ee57f99c0e9e05391162256c64aaa6e100594c69279bcfd6c9bcfc&=&format=webp&width=737&height=671)]
##### Step 5: Commands
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280409740698062858/Green_Tols_18.jpg?ex=66d7f9ff&is=66d6a87f&hm=367a892df6a5ea0b07053786fe9d927acfc2deb8672983d227adf5cad4b4bbec&=&format=webp&width=1075&height=671)]
##### Step 6: Policies
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407435223236618/Green_Tols_4.jpg?ex=66d7f7d9&is=66d6a659&hm=983c9d558034dae9d8bd08733d179da8cb490b040344a088a0d2347295e2643f&=&format=webp&width=1045&height=671)]
##### Step 7: Read Models
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407434778902639/Green_Tols_5.jpg?ex=66d7f7d9&is=66d6a659&hm=4a882368dde33bfcb49cc10d8c0f7acd0216fc0920fcbae6f6895df4453722db&=&format=webp&width=1097&height=671)]
##### Step 8: External Systems
No hay sistemas externos
##### Step 9: Aggregates
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280411167126196297/Green_Tols_19.jpg?ex=66d7fb53&is=66d6a9d3&hm=dc714a7ad1daa72b19585f2f8a2389f7dce182d689fb99ab2ee6502a7ba79b2f&=&format=webp&width=1075&height=671)]
##### Step 10: Bounded Contexts
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407434518597652/Green_Tols_6.jpg?ex=66d7f7d9&is=66d6a659&hm=94f13c92e765854864dcc1b5c812294bc9382fa3ce099abfe2fec9327aab9cbb&=&format=webp&width=1114&height=671)]

#### 4.1.1.2. Domain Message Flows Modeling
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407493847154719/Green_Tols_12.jpg?ex=66d7f7e7&is=66d6a667&hm=c85c0e04a86ac3fdfee6b6707f62730d93bd08a03b87741770b53a6ce7415a24&=&format=webp&width=1202&height=671)]
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407494287687774/Green_Tols_11.jpg?ex=66d7f7e7&is=66d6a667&hm=1f4dd2b21d5cc18bee14c5a2028e67dccaf8866fa9e9fdb793d31a457418b399&=&format=webp&width=1207&height=671)]
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407494690345094/Green_Tols_10.jpg?ex=66d7f7e7&is=66d6a667&hm=8d96f5f93272e2e1409a416cda3ce03817158e78ac1fdf699eb244d3438ed5bb&=&format=webp&width=1204&height=671)]
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407495176622122/Green_Tols_9.jpg?ex=66d7f7e7&is=66d6a667&hm=bf6deb432de8668a184d0119799a197fcd80239c5d9e29fb82aa189967ebc2d3&=&format=webp&width=1217&height=671)]
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407495499710547/Green_Tols_8.jpg?ex=66d7f7e7&is=66d6a667&hm=ff265d75fce254b14f28a08b7adeddb24a60ed84e738aac61b8724db0ece8386&=&format=webp&width=1201&height=671)]
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407495843516416/Green_Tols_7.jpg?ex=66d7f7e7&is=66d6a667&hm=de1a52d81e29e2f8b456462b471d7b0aa350de9c16bcd8f76ccf34c1f9ddc1dc&=&format=webp&width=1183&height=671)]

#### 4.1.1.3. Bounded Context Canvases
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407493406625823/Green_Tols_13.jpg?ex=66d7f7e7&is=66d6a667&hm=fc2b0cc42fd62a50968392e385c2b1b82a1d79d43f21881fad38fbb2f582a1bc&=&format=webp&width=1162&height=671)]
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407496107888672/Green_Tols_16.jpg?ex=66d7f7e7&is=66d6a667&hm=2275b29ed02d4e6480c5fb3a70d52da8bec99631c832367584d49cd2a637ab31&=&format=webp&width=1144&height=671)]
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407496489439332/Green_Tols_15.jpg?ex=66d7f7e7&is=66d6a667&hm=eb97d3ba500461f06739d3e67f5696920b9719f27fb4cbc5e467406e37d92b60&=&format=webp&width=1159&height=671)]
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407496875315232/Green_Tols_14.jpg?ex=66d7f7e8&is=66d6a668&hm=2e9a63f418876a59eb94332979f58c4d54fcb19606973b278d1c17a616ebffd0&=&format=webp&width=1163&height=671)]

### 4.1.2. Context Mapping

### 4.1.3. Software Architecture

#### 4.1.3.1. Software Architecture System Landscape Diagram
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280938931776651388/Green_Tools-Landscape.png?ex=66d9e6d8&is=66d89558&hm=d4cae0aa462ab892a792bc76b607d74eb9f5953bf71689cfff0d5ac008b7de32&=&format=webp&quality=lossless&width=785&height=664)]

#### 4.1.3.2. Software Architecture Context Level Diagrams
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280938932044959745/Green_Tools-Context.png?ex=66d9e6d8&is=66d89558&hm=4c74bbaf300c8713b1f10123dd18ca9aa12c432addc476cd80d2f6802c196017&=&format=webp&quality=lossless&width=598&height=357)]

#### 4.1.3.3. Software Architecture Container Level Diagrams.
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407434019733525/Green_Tools-Containers.png?ex=66d7f7d9&is=66d6a659&hm=551ad6f47c5eccda9495132ab8c1282e705d1a39009b68fe3869cd63923968db&=&format=webp&quality=lossless&width=854&height=671)]

#### 4.1.3.4. Software Architecture Deployment Diagrams
[![Texto alternativo](https://media.discordapp.net/attachments/1280405882517196875/1280407433763622994/Green_Tools-Deployment.png?ex=66d7f7d9&is=66d6a659&hm=14c907db9c50d45eb98e0c69147a0d0a4f621bd7db8987db8f4c048feb02c841&=&format=webp&quality=lossless&width=939&height=671)]

## 4.2. Tactical-Level Domain-Driven Design

### 4.2.1. Bounded Context: \<Account>

#### 4.2.1.1. Domain Layer

Entities:
Value Objects: 
Aggregates:
Repositories:
Services:

#### 4.2.1.2. Interface Layer

API Endpoints:
DTOs:
View Models: 
Controllers:

#### 4.2.1.3. Application Layer

Services:
Commands/Queries:
Command Handlers: 
Event Handlers:

#### 4.2.1.4. Infrastructure Layer

Persistence Mechanisms:
External Service Integrations:
Factories:
API Clients: 

#### 4.2.1.5. Bounded Context Software Architecture Component Level Diagrams

#### 4.2.1.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.1.6.1. Bounded Context Domain Layer Class Diagrams

![Account Bounded Context-DiagramaC](https://github.com/user-attachments/assets/839f44b5-c3e7-4a28-8b0f-d4c66adb7c26)

##### 4.2.1.6.2. Bounded Context Database Design Diagram

![Account Bounded Context](https://github.com/user-attachments/assets/f571b0d8-b4b5-4940-9752-8dd968ba1437)

### 4.2.2. Bounded Context: \<IoT System>

#### 4.2.2.1. Domain Layer

Entities:
Value Objects: 
Aggregates:
Repositories:
Services:

#### 4.2.2.2. Interface Layer

API Endpoints:
DTOs:
View Models: 
Controllers:

#### 4.2.2.3. Application Layer

Services:
Commands/Queries:
Command Handlers: 
Event Handlers:

#### 4.2.2.4. Infrastructure Layer

Persistence Mechanisms:
External Service Integrations:
Factories:
API Clients: 

#### 4.2.2.5. Bounded Context Software Architecture Component Level Diagrams

#### 4.2.2.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.2.6.1. Bounded Context Domain Layer Class Diagrams

![IoT System Bounded Context-DiagramC](https://github.com/user-attachments/assets/84368510-5475-47ea-8345-df7ecfee0220)

##### 4.2.2.6.2. Bounded Context Database Design Diagram

![IoT System Bounded Context](https://github.com/user-attachments/assets/079afb50-8f12-431b-bdfa-fb08f394b741)

### 4.2.3. Bounded Context: \<Crop Inventory>

#### 4.2.3.1. Domain Layer

Entities:
Value Objects: 
Aggregates:
Repositories:
Services:

#### 4.2.3.2. Interface Layer

API Endpoints:
DTOs:
View Models: 
Controllers:

#### 4.2.3.3. Application Layer

Services:
Commands/Queries:
Command Handlers: 
Event Handlers:

#### 4.2.3.4. Infrastructure Layer

Persistence Mechanisms:
External Service Integrations:
Factories:
API Clients: 

#### 4.2.3.5. Bounded Context Software Architecture Component Level Diagrams

#### 4.2.3.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.3.6.1. Bounded Context Domain Layer Class Diagrams

![Crop Inventory Bounded Context-DiagramC](https://github.com/user-attachments/assets/a877c231-1ced-4af2-b58f-2c2c0e222659)

##### 4.2.3.6.2. Bounded Context Database Design Diagram

![Crop Status Bounded Context](https://github.com/user-attachments/assets/022acbc4-ca0b-4639-9603-3ae33bd8cdc9)

### 4.2.4. Bounded Context: \<Crop Status>

#### 4.2.4.1. Domain Layer

Entities:
Value Objects: 
Aggregates:
Repositories:
Services:

#### 4.2.4.2. Interface Layer

API Endpoints:
DTOs:
View Models: 
Controllers:

#### 4.2.4.3. Application Layer

Services:
Commands/Queries:
Command Handlers: 
Event Handlers:

#### 4.2.4.4. Infrastructure Layer

Persistence Mechanisms:
External Service Integrations:
Factories:
API Clients: 

#### 4.2.4.5. Bounded Context Software Architecture Component Level Diagrams

#### 4.2.4.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.4.6.1. Bounded Context Domain Layer Class Diagrams

![Crop Status Bounded Context-DiagramC](https://github.com/user-attachments/assets/6c828cf5-8263-42fe-943b-69287cad3d06)

##### 4.2.4.6.2. Bounded Context Database Design Diagram

![Crop Status Bounded Context](https://github.com/user-attachments/assets/c5cfacfb-f312-4e08-b5c5-df79bfce18bf)

# Capítulo V: Solution UI/UX Design

## 5.1. Style Guidelines

### 5.1.1. General Style Guidelines

### 5.1.2. Web, Mobile and IoT Style Guidelines

## 5.2. Information Architecture

### 5.2.1. Organization Systems

### 5.2.2. Labeling Systems

### 5.2.3. SEO Tags and Meta Tags

### 5.2.4. Searching Systems

### 5.2.5. Navigation Systems

## 5.3. Landing Page UI Design

### 5.3.1. Landing Page Wireframe

### 5.3.2. Landing Page Mock-up

## 5.4. Applications UX/UI Design

### 5.4.1. Applications Wireframes

### 5.4.2. Applications Wireflow Diagrams

### 5.4.3. Applications Mock-ups

### 5.4.4. Applications User Flow Diagrams

## 5.5. Applications Prototyping

# Capítulo VI: Product Implementation, Validation & Deployment

## 6.1. Software Configuration Management

### 6.1.1. Software Development Environment Configuration

### 6.1.2. Source Code Management

### 6.1.3. Source Code Style Guide & Conventions

### 6.1.4. Software Deployment Configuration

## 6.2. Landing Page, Services & Applications Implementation

### 6.2.1. Sprint 1

#### 6.2.1.1. Sprint Planning n

#### 6.2.1.2. Sprint Backlog n

#### 6.2.1.3. Development Evidence for Sprint Review

#### 6.2.1.4. Testing Suite Evidence for Sprint Review

#### 6.2.1.5. Execution Evidence for Sprint Review

#### 6.2.1.6. Services Documentation Evidence for Sprint Review

#### 6.2.1.7. Software Deployment Evidence for Sprint Review

#### 6.2.1.8. Team Collaboration Insights during Sprint

### 6.2.2. Sprint 2

#### 6.2.2.1. Sprint Planning n

#### 6.2.2.2. Sprint Backlog n

#### 6.2.2.3. Development Evidence for Sprint Review

#### 6.2.2.4. Testing Suite Evidence for Sprint Review

#### 6.2.2.5. Execution Evidence for Sprint Review

#### 6.2.2.6. Services Documentation Evidence for Sprint Review

#### 6.2.2.7. Software Deployment Evidence for Sprint Review

#### 6.2.2.8. Team Collaboration Insights during Sprint

## 6.3. Validation Interviews

### 6.3.1. Diseño de Entrevistas

### 6.3.2. Registro de Entrevistas

### 6.3.3. Evaluaciones según heurísticas

## 6.4. Video About-the-Product
