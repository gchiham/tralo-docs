# POE-VEN-01 — Proceso de Ventas / Ingreso de Cliente  
**Versión:** v1.0  
**Área:** Ventas  
**Responsable:** Asesor de Ventas  
**Aprobado por:** Gerente General  
**Fecha:** 13 de noviembre de 2025

---

## 1. Objetivo
Establecer el procedimiento estándar para el registro de nuevos clientes, la recepción de solicitudes de transporte y la validación previa al despacho, asegurando que todo servicio comercializado por TRALO cumpla con los requisitos administrativos, crediticios y operativos.

---

## 2. Alcance
Este procedimiento aplica a:
- Asesor de Ventas  
- Administradora  
- Gerente General  

Aplica a clientes nuevos, clientes existentes y toda solicitud de servicio de transporte.

---

## 3. Responsabilidades

### **Asesor de Ventas**
- Registrar nuevos clientes de acuerdo con [POL-CLI-01 Requisitos de Apertura de Cliente](../credito/POL-CLI-01-requisitos-apertura-cliente.md).  
- Verificar que el cliente esté activo y sin bloqueo crediticio.  
- Confirmar precios y condiciones antes del servicio.  
- Recopilar información completa para cada orden de servicio.  
- Garantizar que la información mínima esté completa antes de enviar la orden a Logística.  
- Mantener comunicación con el cliente antes, durante y después del servicio.

### **Administradora**
- Validar la creación correcta del cliente en Odoo.  
- Verificar el estado de crédito del cliente.  
- Bloquear clientes en mora o con límite excedido.  
- Informar a Ventas sobre cualquier restricción del cliente.  

### **Gerente General**
- Aprobar clientes especiales o con condiciones distintas.  
- Definir tarifas o ajustes fuera del estándar.  
- Autorizar desbloqueos y ampliaciones de crédito.

---

## 4. Documentos relacionados
- [POL-CLI-01 Requisitos de Apertura de Cliente](../credito/POL-CLI-01-requisitos-apertura-cliente.md)  
- [POE-CRE-01 Gestión de Crédito y Aprobaciones](../credito/POE-CRE-01-gestion-credito-aprobaciones.md)  
- [POE-ADM-01 Facturación y Cobros](../administracion/POE-ADM-01-facturacion-cobros.md)  
- [POE-LOG-01 Despacho y Entrega](../logistica/POE-LOG-01-despacho-entrega.md)  

---

## 5. Procedimiento

### **5.1 Registro de nuevo cliente**
1. Solicitar al cliente la información descrita en POL-CLI-01.  
2. Verificar que la información esté completa:  
   - Nombre o razón social  
   - RTN / Cédula  
   - Teléfono y correo  
   - Dirección  
   - Contacto principal  
   - Forma de pago solicitada (contado o crédito)  
3. Crear el cliente en Odoo ingresando datos fiscales y de contacto.  
4. Si solicita crédito, iniciar proceso del POE-CRE-01.  
5. Administradora valida la creación del cliente.

---

### **5.2 Recepción de solicitud de servicio**
Toda solicitud debe incluir:

- Cliente  
- Fecha del servicio  
- Tipo de carga  
- Punto de carga y punto de entrega  
- Tarifa acordada  
- Contacto en origen y contacto en destino  
- Condiciones especiales (si aplica)

**Regla TRALO:**  
❗ *No se inicia ningún servicio sin evidencia del cliente aceptando el precio (WhatsApp, correo o mensaje).*

---

### **5.3 Validación previa al envío a Logística**
Antes de enviar la orden, el Asesor de Ventas debe confirmar que:

1. El cliente está activo en Odoo.  
2. El cliente NO está bloqueado por crédito.  
3. La tarifa está aprobada (según tabla o por Gerente).  
4. La información del servicio está completa.  

---

### **5.4 Envío de la orden de servicio a Logística**
El Asesor debe enviar la orden de servicio en el siguiente formato:

### Formato de Orden de Servicio – TRALO

- **Cliente:**  
- **Ruta:**  
- **Carga:**  
- **Fecha y hora del servicio:**  
- **Tarifa:**  
- **Condiciones especiales:**  
- **Contacto en punto de carga:**  
- **Contacto en punto de entrega:**  


La orden se envía simultáneamente a:
- Logística  
- Administradora  
- Gerente (si es cliente nuevo o caso especial)

---

### **5.5 Seguimiento del servicio**
El Asesor debe:

- Coordinar con el cliente horarios de carga y entrega.  
- Dar seguimiento al chofer para actualizaciones.  
- Solicitar POD o evidencia de entrega.  
- Notificar al cliente cuando el servicio finalice.  

---

## 6. Prohibiciones

- Vender servicios sin tarifa confirmada.  
- Enviar órdenes incompletas o sin datos críticos.  
- Despachar a clientes bloqueados o en mora.  
- Prestar servicios sin evidencia de autorización del cliente.  
- Modificar tarifas sin aprobación del Gerente.

---

## 7. Flujo de proceso (Mermaid)

```mermaid
flowchart TD
    A[Cliente solicita servicio] --> B[Asesor solicita requisitos POL-CLI-01]
    B --> C{Cliente nuevo?}
    C -->|Sí| D[Registrar cliente en Odoo]
    C -->|No| E[Validar cliente existente]
    D --> F[Verificar estado de crédito]
    E --> F[Verificar estado de crédito]
    F -->|Aprobado| G[Recopilar información completa del servicio]
    G --> H[Confirmar tarifa con cliente y obtener evidencia]
    H --> I[Enviar orden de servicio a Logística y Administración]
    I --> J[Servicio se ejecuta]
    J --> K[Recibir POD y notificar al cliente]
