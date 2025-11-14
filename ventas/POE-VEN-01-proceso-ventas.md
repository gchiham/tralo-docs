# POE-VEN-01 — Proceso de Ventas / Ingreso de Cliente
**Versión:** v1.0  
**Área:** Ventas  
**Responsable:** Asesor de Ventas  
**Aprobado por:** Gerente General  
**Fecha:** _(llenar)_

---

## 1. Objetivo
Definir el proceso estándar para:
- Registrar nuevos clientes en TRALO  
- Recibir solicitudes de servicio de transporte  
- Verificar la información mínima necesaria antes de pasar el servicio a Logística  
- Garantizar que solo se ofrezcan servicios a clientes válidos y con estado crediticio permitido

---

## 2. Alcance
Este procedimiento aplica a:
- Asesor de Ventas  
- Administradora  
- Gerente General  

Cubre todo servicio solicitado por clientes nuevos y existentes.

---

## 3. Responsabilidades

### **Asesor de Ventas**
- Registrar clientes nuevos.  
- Verificar requisitos de POL-CLI-01.  
- Verificar que el cliente no esté bloqueado por crédito.  
- Registrar la solicitud de servicio en el formato correspondiente.  
- Confirmar precio y condiciones con el cliente.  
- Enviar la orden de servicio completa a Logística y Administración.  

### **Administradora**
- Validar que el cliente esté creado correctamente en Odoo.  
- Verificar estado de crédito antes de permitir despacho.  
- Bloquear clientes en mora.  
- Actualizar estado de pagos y límite de crédito.

### **Gerente General**
- Aprobar clientes especiales.  
- Definir tarifas generales y condiciones especiales.  
- Autorizar desbloqueo de clientes o ampliaciones de crédito.

---

## 4. Documentos relacionados
- POL-CLI-01 Requisitos de Apertura de Cliente  
- POE-ADM-01 Facturación y Cobros  
- POE-CRE-01 Gestión de Crédito y Aprobaciones  
- POE-LOG-01 Despacho y Entrega  

---

## 5. Procedimiento

---

### **5.1 Registro de nuevo cliente**

1. Asesor solicita al cliente los requisitos definidos en **POL-CLI-01**.  
2. Verifica que la información esté completa:  
   - Nombre o razón social  
   - RTN / Cédula  
   - Teléfono y correo  
   - Dirección  
   - Contacto principal  
   - Forma de pago solicitada (contado o crédito)  
3. Crea el cliente en Odoo:  
   - Contacto  
   - Información fiscal  
   - Dirección de facturación  
   - Términos de pago  
4. Si el cliente solicita crédito → seguir POE-CRE-01.  
5. Administradora valida que la cuenta esté bien creada.  

---

### **5.2 Recepción de solicitud de servicio**

Toda solicitud debe incluir:

- Cliente  
- Tipo de carga  
- Punto de carga  
- Punto de entrega  
- Fecha y hora requerida  
- Kilometraje o tarifa aplicada  
- Precio acordado  
- Contacto en origen y destino  

**Regla TRALO:**  
❗ *NO se inicia ningún servicio sin tener precio confirmado y evidencia del cliente aceptando por WhatsApp, correo o mensaje.*

---

### **5.3 Validación antes de enviar a Logística**

El Asesor debe verificar:

1. Cliente activo en Odoo  
2. Cliente NO está bloqueado por crédito  
3. Tarifa aprobada por Gerente (si aplica)  
4. Información del servicio completa  

Luego envía la orden de servicio a:
- Administradora  
- Logística  
- Gerente (si es un cliente nuevo o tarifa especial)

---

### **5.4 Envío de Orden de Servicio a Logística**

El Asesor debe enviar la orden en formato:

