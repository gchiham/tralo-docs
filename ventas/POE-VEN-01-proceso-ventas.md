
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
