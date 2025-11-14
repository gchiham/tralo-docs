# POE-ADM-01 — Facturación y Cobros  
**Versión:** v1.0  
**Área:** Administración  
**Responsable:** Administrador
**Aprobado por:** Gerente General  
**Fecha:** 11 de Noviembre de 2025

---

## 1. Objetivo
Establecer el procedimiento estándar para generar facturas, registrar pagos, controlar ingresos y mantener un flujo de cobros claro y ordenado para TRALO.

---

## 2. Alcance
Este procedimiento aplica a:
- Administrador
- Gerente General  
- Asesor de ventas (solo envío de información)  

Aplica a todos los servicios de transporte realizados por TRALO.

---

## 3. Responsabilidades

### **Administrador**
- Generar facturas en Odoo.  
- Registrar pagos.  
- Verificar que el cliente cumpla los requisitos antes de facturar.  
- Mantener actualizado el estado de cuenta del cliente.  
- Notificar a Ventas cuando un cliente entre en mora o llegue a su límite de crédito.  

### **Asesor de ventas**
- Enviar la orden de servicio con toda la información correcta.  
- Verificar que el cliente tenga permisos activos (no bloqueado por crédito).

### **Gerente General**
- Autorizar ajustes de facturas.  
- Aprobar crédito y ampliación de límite (según POE-CRE-01).  
- Validar cierres mensuales de ingresos.

---

## 4. Documentos relacionados
- POL-CLI-01 Requisitos de Apertura de Cliente  
- POE-VEN-01 Proceso de Ventas  
- POE-CRE-01 Gestión de Crédito y Aprobaciones  

---

## 5. Procedimiento

### **5.1 Recepción de información para facturar**
1. Ventas envía la orden de servicio completa:  
   - Cliente  
   - Ruta  
   - Fecha del servicio  
   - Monto acordado  
   - Tipo de carga  
   - Evidencia POD (si aplica)

2. La administradora valida:  
   - Cliente registrado en Odoo  
   - Cliente no bloqueado por crédito  
   - Servicio aprobado y entregado  

---

### **5.2 Generación de factura**
1. Ingresar a Odoo → Módulo de **Facturación**.  
2. Seleccionar cliente.  
3. Registrar servicio prestado.  
4. Verificar impuestos y montos.  
5. Confirmar factura.  
6. Enviar copia PDF al cliente por correo/WhatsApp.  

---

### **5.3 Registro de pagos**
Cuando el cliente realiza un pago:

#### **Transferencia**
1. Cliente envía comprobante.  
2. Administradora verifica en banca en línea.  
3. Registrar pago en Odoo → “Registrar Pago → Transferencia bancaria”.

#### **Cheques**
1. Registrar como pago “cheque”.  
2. Marcar como “pendiente de acreditación”.

---

### **5.4 Control de cuentas por cobrar**
1. Revisar semanalmente el reporte de **Clientes → Cuentas por Cobrar**.  
2. Identificar clientes en mora o cerca de su límite de crédito.  
3. Notificar a Ventas.  
4. Actualizar el documento interno de control de pagos.

---

### **5.5 Cierre mensual**
1. Verificar que todas las facturas del mes estén registradas.  
2. Revisar pagos incompletos o pendientes.  
3. Entregar al Gerente el reporte mensual:  
   - Total facturado  
   - Total cobrado  
   - Cartera vencida  
   - Clientes bloqueados  

4. El Gerente valida y firma el cierre.

---

## 6. Controles internos
- No se emiten facturas si el cliente está bloqueado por crédito.  
- Toda factura debe tener POD o evidencia de entrega (según servicio).  
- Solo el Gerente puede:  
  - Aprobar notas de crédito  
  - Ajustar montos  
  - Dar ampliación de crédito    

---

## 7. Flujo resumido (Mermaid)

```mermaid
flowchart TD
A[Ventas envía orden de servicio] --> B[Administradora valida cliente y servicio]
B --> C[Generar factura en Odoo]
C --> D[Enviar factura al cliente]
D --> E[Cliente paga]
E --> F[Registrar pago en Odoo]
F --> G[Actualizar cuentas por cobrar]
G --> H[Cierre mensual y reporte al Gerente]
