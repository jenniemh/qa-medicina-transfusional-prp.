# 🩸 Sistema de Gestión de Medicina Transfusional - PRP Clínico
### 🛠️ Creador, Product Owner & QA Lead

Este software es una plataforma web especializada en la gestión, trazabilidad y control de tratamientos de **Plasma Rico en Plaquetas (PRP)** y hemoterapia celular. 

> 💡 **Nota de Autoría y Desarrollo:** Este sistema ha sido ideado, diseñado y creado en su totalidad por mi persona, utilizando herramientas avanzadas de Inteligencia Artificial para la aceleración del código y la lógica de negocio. Este repositorio funciona como un caso de estudio donde demuestro mi capacidad para liderar un producto de software desde la idea hasta su despliegue, combinando mi experiencia clínica con el Aseguramiento de Calidad (QA) bajo los estándares más estrictos del sector HealthTech.

---

## 🖼️ Recorrido del Sistema y Alcance del Testing

### 1. Control de Acceso y Seguridad (Login)
*   **Descripción de la Pantalla:** Formulario de inicio de sesión unificado con campos restringidos para personal autorizado de la clínica.
*   **Enfoque de QA (Qué se testeó):** Verificación de políticas de autenticación, manejo correcto de tokens de sesión y bloqueo ante intentos de accesos no autorizados a la base de datos de hemoterapia.
*   **Evidencia Visual:**
    ![01-Login-PRP](PRP.1.png)

---

### 2. Panel de Control y Métricas Clínicas (Dashboard)
*   **Descripción de la Pantalla:** Panel principal que centraliza los KPIs operativos (Total de sesiones, Pacientes activos, Tasa de alta) y gráficos analíticos de las sesiones mensuales y distribución por zonas anatómicas tratadas.
*   **Enfoque de QA (Qué se testeó):** Validación de la integridad y actualización de datos en tiempo real dentro de las gráficas (zonas de rodilla, hombro y cadera) frente a nuevos registros ingresados en la base de datos.
*   **Evidencia Visual:**
    ![02-Dashboard-PRP](PRP.2.png)

---

### 3. Gestión y Registro Avanzado de Pacientes
*   **Descripción de la Pantalla:** Grilla centralizada con estados del paciente (Activo, Evaluación, Completado), diagnósticos médicos parametrizados (Gonartrosis, Tendinopatía rotuliana, Hernia discal) y protocolos específicos de plasma asignados.
*   **Enfoque de QA (Qué se testeó):** Pruebas funcionales de los filtros de búsqueda rápida por nombre o DNI, control de paginación del listado y flujos de inserción de nuevos registros clínicos anonimizados.
*   **Evidencia Visual:**
    ![03-Pacientes-PRP](PRP.3.png)

---

### 4. Detalle y Trazabilidad del Paciente Clínico
*   **Descripción de la Pantalla:** Vista interna del perfil de un paciente donde se registra el historial de aplicaciones de plasma, evolución sintomática y notas de control médico.
*   **Enfoque de QA (Qué se testeó):** Persistencia de datos al cambiar entre pestañas del expediente y correcta vinculación del ID del paciente con su historial clínico.
*   **Evidencia Visual:**
    ![04-Detalle-PRP](PRP.4.png)

---

### 5. Agenda y Programación de Sesiones
*   **Descripción de la Pantalla:** Módulo de calendario y agenda cronológica para el control técnico de citas médicas pendientes en el área de hemoterapia celular.
*   **Enfoque de QA (Qué se testeó):** Control de lógica relacional en la asignación de fechas futuras y disparo de alertas visuales en la interfaz ante superposición de turnos médicos.
*   **Evidencia Visual:**
    ![05-Sesiones-PRP](PRP.5.png)

---

### 6. Configuración de Protocolos de Centrifugación (Core Médico)
*   **Descripción de la Pantalla:** Catálogo de estándares de centrifugación médica (como LP-PRP y LR-PRP), detallando las fases críticas de separación de eritrocitos y concentración plaquetaria por RPM y minutos.
*   **Enfoque de QA (Qué se testeó):** Pruebas de caja negra con valores límite (Boundary Value Testing) en los campos numéricos de RPM y tiempos de centrifugado para mitigar riesgos biológicos en el procesamiento de muestras reales.
*   **Evidencia Visual:**
    ![06-Protocolos-PRP](PRP.6.png)

---

### 7. Módulo de Reportes Estadísticos y Exportación
*   **Descripción de la Pantalla:** Interfaz gráfica para la auditoría de sesiones totales filtradas por tipo de protocolo aplicados a lo largo del año.
*   **Enfoque de QA (Qué se testeó):** Validación de consistencia de datos de las funciones de exportación (`Exportar pacientes` y `Exportar sesiones`) asegurando formatos CSV/Excel limpios y listos para auditorías institucionales.
*   **Evidencia Visual:**
    ![07-Reportes-PRP](PRP.7.png)

---

## 🛠️ Matriz de Pruebas Destacadas (Test Cases)

| ID | Módulo | Descripción del Caso de Prueba | Tipo de Prueba | Resultado Esperado |
| :--- | :--- | :--- | :--- | :--- |
| **TC-PAC-001** | Barra de Búsqueda | Ingresar un DNI que no existe en el sistema (ej: `99999999`). | Validación de Campos | La grilla debe vaciarse y mostrar un mensaje claro de *"No se encontraron pacientes"*, sin romper la interfaz. |
| **TC-PAC-002** | Filtros de Estado | Hacer clic en el botón de filtro `Evaluación`. | Funcional (Sanity) | La tabla debe actualizarse instantáneamente mostrando **únicamente** los pacientes cuyo estado sea `Evaluación`. |
| **TC-PAC-003** | Badge de Sesiones | Verificar que el contador de `SES.` (círculo rojo) sea un número entero mayor a cero. | Reglas de Negocio | El sistema no debe permitir valores negativos ni decimales en las sesiones acumuladas de tratamiento. |

---

## 🎯 Habilidades Técnicas Demostradas en este Proyecto
*   **QA con Conocimiento de Dominio (Domain Knowledge):** Aplicación de criterios de prueba basados en normativas médicas y procesos biológicos reales (centrifugación de plasma, resguardo de datos de pacientes).
*   **Diseño de Datos de Prueba (Test Data Design):** Creación de perfiles clínicos ficticios complejos para pruebas de cobertura funcional de extremo a extremo (E2E).
*   **Desarrollo impulsado por IA:** Optimización, estructuración y aceleración de código mediante técnicas de prompt engineering.
