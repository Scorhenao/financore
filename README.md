### **Documento de Requisitos y Organización del Desarrollo del Proyecto Financore**  
#### **Aplicación de Control de Presupuesto Inteligente**  

---

## **1. Descripción General**  

El objetivo de este proyecto es desarrollar una **Aplicación de Control de Presupuesto Inteligente** que permita a los usuarios gestionar sus finanzas personales de manera eficiente. La aplicación estará disponible tanto en la web como en dispositivos móviles. Facilitará las siguientes funciones:  
- **Creación de presupuestos mensuales**.  
- **Registro de gastos e ingresos**.  
- **Categorización de transacciones**.  
- **Análisis y estadísticas financieras**.  

El desarrollo se iniciará con una **versión mobile en React-Native** para implementar las funcionalidades principales y luego se expandirá a web utilizando **React**. La versión final de la aplicación incluirá características avanzadas de notificaciones push y gráficos interactivos.  

**Fecha de entrega inicial:**  
- **Fecha de entrega**: 14 de diciembre, 12:00 p.m.  
- **Duración estimada**: 3 semanas.  

---

## **2. Funcionalidades Principales**  

### **2.1. Gestión de Presupuestos y Transacciones**  
- **Creación de Presupuesto Mensual**:  
   - El usuario podrá **crear un presupuesto mensual**, asignando un monto general y presupuestos específicos por categoría (e.g., comida, transporte, entretenimiento).
   - **Fecha de inicio y finalización** para cada presupuesto, que puede coincidir con el mes o ser personalizado.  
   - El presupuesto global se ajustará automáticamente a medida que se registren gastos.

- **Registro de Gastos e Ingresos**:  
   - Los usuarios podrán **registrar gastos e ingresos** especificando la fecha, el monto y la categoría.
   - **Tipos de ingresos**: El sistema permitirá agregar un tipo de ingreso general, el cual se sumará al presupuesto de cada categoría o al monto general.
   - Los **gastos registrados** se descontarán automáticamente del presupuesto de la categoría correspondiente y el monto general.  
   - Los **gráficos** se actualizarán con cada cambio, mostrando la relación entre ingresos y gastos.

- **Alertas y Notificaciones**:  
   - Alertas para situaciones críticas, como cuando el usuario **gasta más de lo presupuestado** en un corto período (día, semana).
   - Notificaciones **push** enviadas al usuario cuando el presupuesto de alguna categoría se esté agotando o se gaste más de lo previsto.
   - Al hacer clic en la notificación, el usuario será redirigido a la sección correspondiente dentro de la app para que pueda tomar acción.

---

### **2.2. Visualización y Análisis Financiero**  
- **Gráficos**:  
   - Se generarán gráficos interactivos para mostrar:  
     - Los **gastos e ingresos a lo largo del mes**.  
     - Un **gráfico general** que represente el presupuesto global vs. los gastos.  
     - Un **gráfico circular** para cada presupuesto por categoría.  
   - Las gráficas deben mostrar **porcentajes** para visualizar de manera clara cómo se distribuye el presupuesto entre las diferentes categorías.

- **Filtrado de Transacciones**:  
   - Los usuarios podrán **filtrar transacciones** por categoría para un análisis más detallado.

- **Edición de Presupuestos**:  
   - Durante el mes en curso, se permitirá la **edición del presupuesto**. Fuera de este periodo, los presupuestos no podrán modificarse hasta el siguiente mes.

**Herramientas sugeridas para gráficos**:  
- [MagicPattern SVG Chart Generator](https://www.magicpattern.design/tools/svg-chart-generator).  

---

### **2.3. Acceso y Seguridad**  
- **Registro y Login**:  
   - La aplicación permitirá a los usuarios registrarse e iniciar sesión utilizando su correo electrónico y contraseña.  
   - **Recuperación de contraseña** estará disponible para los usuarios que olviden sus credenciales.

- **Roles**:  
   - No habrá roles diferenciados en esta versión del producto; todos los usuarios tendrán acceso a las mismas funcionalidades.

---

## **3. Tecnologías y Herramientas**  

| **Aspecto**              | **Herramienta/Paquete**          | **Notas**                                                                 |
|---------------------------|----------------------------------|---------------------------------------------------------------------------|
| **Frontend Web**          | React                           | Desarrollo de la interfaz web principal utilizando React.                |
| **Frontend Móvil**        | React Native                    | Desarrollo de la versión móvil para iOS y Android utilizando React Native.|
| **Notificaciones Push**   | [React Native OneSignal](https://www.npmjs.com/package/react-native-onesignal) | Implementación de notificaciones push para alertas en tiempo real.       |
| **Gráficos**              | [MagicPattern SVG Charts](https://www.magicpattern.design/tools/svg-chart-generator) | Generación de gráficos interactivos y personalizados.                    |
| **Estado**                | Redux / Context API             | Manejo del estado global de la aplicación.                               |
| **Estilo**                | TailwindCSS / CSS Modules       | Estilos modernos y responsivos utilizando TailwindCSS y CSS Modules.     |
| **Backend**               | NestJS                          | Backend desarrollado con NestJS para manejar la lógica de negocio.      |
| **Base de Datos**         | PostgreSQL o MongoDB            | Base de datos relacional (PostgreSQL) o NoSQL (MongoDB).                |
| **Despliegue Backend**    | Render                          | Despliegue del backend con Render para facilitar la gestión de servidores. |

---

## **4. Flujo de Trabajo**  

### **Semana 1: Inicio y Configuración**  
1. Configuración del entorno de desarrollo (Frontend y Backend).  
2. Implementación de **registro** e **inicio de sesión**, incluyendo **recuperación de contraseña**.  
3. Diseño e implementación de la **estructura inicial para presupuestos y transacciones**.  

### **Semana 2: Funcionalidades Base**  
1. Desarrollo de las funcionalidades principales:  
   - Creación de presupuesto mensual.  
   - Registro de gastos e ingresos.  
   - Actualización de presupuesto al registrar gastos.  
2. Implementación de **gráficos básicos** para gastos, ingresos y categorías.  
3. Desarrollo de alertas y notificaciones push básicas con **OneSignal**.  

### **Semana 3: Finalización y Ajustes**  
1. **Pruebas de usuario** y ajustes finales en la interfaz y la funcionalidad.  
2. **Edición de presupuestos y filtros por categorías**.  
3. Optimización y finalización de **gráficos interactivos**.  
4. Documentación del proyecto y preparación para la entrega final.

---

## **5. Indicadores de Éxito (KPIs)**  
- **Funcionalidades principales** implementadas y funcionales en la versión mobile.
- **Gráficos interactivos** generados y actualizados en tiempo real.  
- **Alertas push** enviadas correctamente en tiempo real.  
- **Registro de transacciones** y **edición de presupuestos** sin errores.  

---

## **6. Notas Finales**  
La primera entrega incluirá un **MVP (Producto Mínimo Viable)** con las siguientes características:  
- Creación y edición de presupuestos.  
- Registro de transacciones.  
- Visualización básica de gráficos.  
- Notificaciones push funcionales.  

Las funcionalidades avanzadas como gráficos más detallados y complejos, junto con la optimización de notificaciones, se perfeccionarán en la siguiente fase del proyecto o después de la entrega inicial.  

---
