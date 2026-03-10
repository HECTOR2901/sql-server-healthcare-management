# 🏥 Sistema de Gestión de Datos Relacionales: Sector Salud (SQL Server)

## 📌 1. Introducción y Alcance del Proyecto
Este proyecto integrador desarrolla una solución de arquitectura de datos para una entidad de salud de alta complejidad (Caso: Clínica San Pablo). El objetivo central fue enfrentar los desafíos de fragmentación de información y falta de trazabilidad en el ciclo de suministros y gestión de personal mediante el diseño y despliegue de una base de datos relacional robusta.

El sistema garantiza la **integridad referencial** y la **escalabilidad**, permitiendo una transición eficiente desde procesos manuales hacia una gestión automatizada basada en datos.

---

## 🏗️ 2. Arquitectura de Datos y Segmentación por Esquemas
A diferencia de modelos convencionales, se implementó una arquitectura basada en **esquemas lógicos**, optimizando la seguridad y la administración de objetos:

### 👥 Esquema `Salud.Personal`
Centraliza el capital humano de la clínica. 
* **Tablas Maestras:** Médicos, Especialidades y Pisos.
* **Impacto:** Permite la asignación dinámica de personal y el control de turnos operativos, facilitando la auditoría de recursos en sala.

### 📦 Esquema `Salud.Inventario`
Estructura el catálogo maestro de insumos críticos.
* **Tablas Maestras:** Artículos, Categorías técnicas y Unidades de Medida (UOM).
* **Impacto:** Asegura la consistencia en el conteo de existencias y estandariza la clasificación de suministros médicos.

### 💳 Esquema `Salud.Sourcing`
Administra el flujo de abastecimiento y relación con proveedores.
* **Tablas Transaccionales:** Órdenes de Compra (Cabecera y Detalle), Proveedores y Estados de Pago.
* **Impacto:** Proporciona trazabilidad total desde el requerimiento hasta la liquidación financiera.

---

## 🛠️ 3. Rigor Técnico y Modelamiento
El diseño se rige por principios avanzados de ingeniería de datos:

1. **Normalización (3FN):** El modelo cumple con la **Tercera Forma Normal**, eliminando redundancias transitivas y asegurando la consistencia atómica de los datos.
2. **Integridad Referencial:** Implementación jerárquica de **Primary Keys (PK)** y **Foreign Keys (FK)**, impidiendo registros huérfanos y garantizando la validez de cada transacción.
3. **Optimización de Tipos de Datos:** Uso eficiente de `VARCHAR`, `INT`, `DECIMAL` y `DATETIME` para minimizar el almacenamiento y maximizar la velocidad de consulta.

---

## 📈 4. Analítica Operativa y Business Intelligence (KPIs)
El sistema integra scripts de **T-SQL Avanzado** para la generación de indicadores clave de desempeño:

* **Control de Stock Mínimo:** Consultas automáticas que identifican insumos por debajo del nivel de seguridad para evitar desabastecimiento.
* **Análisis de Gasto por Proveedor:** Uso de `INNER JOINs`, `GROUP BY` y funciones de agregación para evaluar el volumen de compras y cumplimiento de pagos.
* **Distribución Operativa:** Reportes cruzados de personal médico por especialidad y ubicación física en la clínica.

---

## 🚀 5. Tecnologías y Metodología
* **Motor de Base de Datos:** Microsoft SQL Server (T-SQL).
* **Modelamiento Lógico:** Bizagi Modeler y Diagramas Entidad-Relación (DER).
* **Documentación Técnica:** Informe detallado de procesos y arquitectura (disponible en formato PDF).
* **Enfoque Estadístico:** Criterios de validación y limpieza de datos propios de la formación académica en la **UNALM**.

---

## 📂 6. Estructura del Repositorio
* `/Scripts`: Contiene el archivo `.sql` con el código DDL/DML para la creación y carga del sistema.
* `/Documentacion`: Informe técnico final con diagramas de flujo y análisis de negocio.
* `/Media`: Capturas de pantalla del Diagrama Entidad-Relación (DER).

---

**Autor:** Héctor Estéfano Gómez Vigo  
**Contacto:** 20230397@lamolina.edu.pe  
**LinkedIn:** [Héctor Estéfano Gómez](https://www.linkedin.com/in/héctor-estéfano-gómez-9b6079289)
