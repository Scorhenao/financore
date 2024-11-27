### **Epics, Features, User Stories y Tasks**  

---

## **Epics**  

### **EP01: Gestión de Presupuestos**  
Desarrollar funcionalidades para que los usuarios puedan crear, editar y gestionar presupuestos mensuales, incluyendo categorías personalizadas y ajustes en tiempo real.  

### **EP02: Registro de Transacciones**  
Permitir a los usuarios registrar ingresos y gastos asociados a categorías y reflejar los cambios en los presupuestos.  

### **EP03: Visualización y Análisis**  
Generar gráficos interactivos para representar ingresos, gastos y presupuestos, ofreciendo filtros por categoría y porcentajes.  

### **EP04: Acceso y Seguridad**  
Implementar registro, inicio de sesión y recuperación de contraseñas para los usuarios.  

### **EP05: Notificaciones y Alertas**  
Agregar notificaciones push y alertas para informar a los usuarios sobre presupuestos agotados o comportamientos financieros importantes.  

---

## **Features**  

### **FT01: Creación de Presupuestos**  
- Crear presupuestos generales y por categoría.  
- Asignar fechas de inicio y finalización personalizables.  
- Ajustar presupuestos automáticamente con base en las transacciones registradas.  

### **FT02: Registro de Transacciones**  
- Registro de ingresos y gastos con fecha, monto y categoría.  
- Ajustes dinámicos de presupuestos y actualización de gráficos en tiempo real.  

### **FT03: Gráficos Interactivos**  
- Mostrar gráficos generales (global) y específicos (por categoría).  
- Gráficos circulares para mostrar distribución de gastos por categorías.  
- Visualización de porcentajes y totales.  

### **FT04: Seguridad y Autenticación**  
- Implementación de registro, inicio de sesión y recuperación de contraseñas.  
- Sin roles diferenciados en esta fase inicial.  

### **FT05: Alertas y Notificaciones Push**  
- Alertas en tiempo real para presupuestos agotados o gastos excesivos.  
- Integración con **React Native OneSignal** para enviar notificaciones push.  

---

## **User Stories (Historias de Usuario)**  

### **US01: Crear Presupuesto Mensual**  
**Como** usuario,  
**quiero** crear presupuestos mensuales con categorías personalizadas,  
**para** gestionar mis finanzas de manera organizada.  

**Criterios de Aceptación:**  
- El usuario puede asignar un monto general y específicos para cada categoría.  
- Los presupuestos deben incluir fecha de inicio y fin.  
- Deben reflejarse los cambios al registrar transacciones.  

---

### **US02: Registrar Gastos e Ingresos**  
**Como** usuario,  
**quiero** registrar mis ingresos y gastos,  
**para** mantener actualizados mis presupuestos y ver su impacto en tiempo real.  

**Criterios de Aceptación:**  
- Registro de montos con categoría, fecha y descripción opcional.  
- Los gastos deben descontarse automáticamente de la categoría correspondiente.  
- Actualización dinámica de gráficos tras cada registro.  

---

### **US03: Visualizar Gráficos de Presupuestos**  
**Como** usuario,  
**quiero** visualizar gráficos detallados de mis ingresos y gastos,  
**para** entender cómo estoy manejando mis finanzas.  

**Criterios de Aceptación:**  
- Gráficos generales para presupuestos globales vs gastos.  
- Gráficos circulares específicos por categoría.  
- Visualización de porcentajes y datos filtrados por categoría.  

---

### **US04: Recibir Notificaciones Push**  
**Como** usuario,  
**quiero** recibir notificaciones sobre mis gastos y presupuestos,  
**para** tomar decisiones financieras a tiempo.  

**Criterios de Aceptación:**  
- Notificaciones push al exceder el presupuesto de una categoría o el global.  
- Redirección a la sección específica de la app desde la notificación.  

---

### **US05: Recuperar Contraseña**  
**Como** usuario,  
**quiero** recuperar mi contraseña si la olvido,  
**para** poder acceder nuevamente a la aplicación.  

**Criterios de Aceptación:**  
- El sistema debe enviar un enlace o código de recuperación al correo registrado.  

---

## **Tasks (Tareas)**  

### **T01: Crear Interfaz de Presupuesto (React Native)**  
**Epic**: Gestión de Presupuestos.  
**Estado**: To do.  
**Descripción**:  
Escenario: Interfaz de creación de presupuesto.  
**Given**: El usuario accede a la sección de presupuestos.  
**When**: Selecciona la opción para "Crear Presupuesto".  
**Then**: Se despliega un formulario para ingresar el monto, categorías y fechas.  
**And**: Al guardar, se actualiza la base de datos y la interfaz principal.  
**Dificultad**: 5 (Fibonacci).  
**Dependencias**: Context API/Redux para estado global, React Native UI.  

---

### **T02: Registrar Transacción (Backend - NestJS)**  
**Epic**: Registro de Transacciones.  
**Estado**: To do.  
**Descripción**:  
Escenario: Registro de gastos e ingresos.  
**Given**: El usuario accede a la sección de transacciones.  
**When**: Completa el formulario de registro con categoría, monto y fecha.  
**Then**: El sistema guarda la transacción en la base de datos y ajusta los presupuestos.  
**Dificultad**: 8 (Fibonacci).  
**Dependencias**: Base de datos PostgreSQL/MongoDB, API de NestJS.  

---

### **T03: Generar Gráficos (Frontend - React Native)**  
**Epic**: Visualización y Análisis.  
**Estado**: To do.  
**Descripción**:  
Escenario: Visualización de gráficos de presupuesto.  
**Given**: El usuario navega a la sección de análisis financiero.  
**When**: Selecciona un período o categoría.  
**Then**: Se muestra un gráfico actualizado en tiempo real con los datos seleccionados.  
**Dificultad**: 8 (Fibonacci).  
**Dependencias**: Herramienta SVG Charts, React Native.  

---

### **T04: Implementar Notificaciones Push (React Native)**  
**Epic**: Notificaciones y Alertas.  
**Estado**: To do.  
**Descripción**:  
Escenario: Notificación por gastos excesivos.  
**Given**: El usuario gasta más del presupuesto en una categoría.  
**When**: El monto excede el límite configurado.  
**Then**: Se envía una notificación push al dispositivo.  
**Dificultad**: 5 (Fibonacci).  
**Dependencias**: React Native OneSignal.  

---