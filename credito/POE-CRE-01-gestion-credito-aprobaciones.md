# POE-CRE-01 — Gestión de Crédito y Aprobaciones  
**Versión:** v1.0  
**Área:** Crédito / Administración  
**Responsable:** Administradora  
**Aprobado por:** Gerente General  
**Fecha:** 13 de noviembre de 2025

---

## 1. Objetivo
Establecer el procedimiento estándar para evaluar clientes, asignar límites de crédito, controlar su desempeño de pago y definir el proceso de bloqueo y aprobación de ampliaciones de crédito en TRALO.

---

## 2. Alcance
Este procedimiento aplica a:
- Administrador
- Gerente General  
- Asesor de Ventas  

Aplica a **clientes que soliciten crédito** y **clientes activos con crédito asignado**.

---

## 3. Documentos relacionados
- [POL-CLI-01 Requisitos de Apertura de Cliente](../credito/POL-CLI-01-requisitos-apertura-cliente.md)  
- [POE-VEN-01 Proceso de Ventas](../ventas/POE-VEN-01-proceso-ventas.md)  
- [POE-ADM-01 Facturación y Cobros](../administracion/POE-ADM-01-facturacion-cobros.md)  

---

## 4. Responsabilidades

### **Administrador**
- Evaluar la solicitud de crédito.  
- Calcular el score del cliente.  
- Definir el límite de crédito inicial.  
- Registrar términos de pago en Odoo.  
- Bloquear clientes en mora o con límite excedido.  
- Notificar a Ventas sobre restricciones.  

### **Gerente General**
- Aprobar créditos especiales.  
- Aprobar ampliaciones de crédito.  
- Autorizar desbloqueos en casos excepcionales.  

### **Asesor de Ventas**
- Verificar si el cliente tiene crédito o está bloqueado antes de vender.  
- NO enviar servicios cuando el cliente está bloqueado.  
- Coordinar con la Administradora cuando un cliente está cerca del límite.  

---

## 5. Requisitos para solicitar crédito
Todo cliente debe presentar:

- RTN o DNI  
- Dirección y contacto  
- Historial de pago (si es cliente previo)  
- Referencias comerciales (opcional según riesgo)  
- Promedio estimado de cargas por mes  

Si falta información → **NO se evalúa crédito**.

---

## 6. Score del cliente (modelo TRALO)

| Factor | Peso | Evaluación |
|--------|------|------------|
| Antigüedad como cliente | 30% | +10 pts por cada 3 meses (máx 30) |
| Historial de pagos | 40% | 0 = malo, 20 = algunas demoras, 40 = impecable |
| Relación comercial esperada | 20% | 5, 10 o 20 pts |
| Reputación / referencias | 10% | 0–10 pts |

### **Puntaje final (0–100)**

- **80–100 ➜ Crédito recomendado hasta L 40,000**  
- **60–79 ➜ Crédito moderado L 20,000–L 30,000**  
- **40–59 ➜ Crédito limitado L 10,000–15,000**  
- **<40 ➜ Solo contado**

TRALO es microempresa, así que los límites son **conservadores**.

---

## 7. Límite de crédito inicial

La Administradora asigna:

- Según puntaje del score  
- Según comportamiento esperado  
- Según capacidad TRALO (no comprometer flujo)

El Gerente puede autorizar montos mayores si lo considera estratégico.

---

## 8. Registro en Odoo
La Administradora debe:

1. Configurar **Términos de pago** (Ej: 15 días / 30 días).  
2. Establecer **Límite de crédito** en la ficha del cliente.  
3. Activar alerta para facturas vencidas.  
4. Activar bloqueo automático si se sobrepasa el límite.

---

## 9. Bloqueo de clientes
Un cliente debe bloquearse cuando:

- Tiene más de **1 factura vencida**  
- Supera el límite de crédito  
- Presenta más de 7 días de mora  
- El Gerente lo ordena  

### Acciones automáticas TRALO:
- Administradora cambia estado del cliente a **Bloqueado**  
- Ventas recibe notificación  
- Logística NO puede despachar  
- Odoo impide facturación nueva

---

## 10. Ampliación o modificación de crédito

### La ampliación solo se autoriza si:
- El cliente tiene historial positivo  
- No tiene facturas vencidas  
- Tiene al menos 3 servicios pagados puntuales  

### Proceso:
1. Ventas solicita ampliación indicando motivo.  
2. Administradora revisa score actualizado.  
3. Gerente decide si se aprueba.  
4. Administradora actualiza límite en Odoo.  
5. Se notifica a Ventas.

---

## 11. Prohibiciones

- No se otorga crédito sin score.  
- No se despacha carga si el cliente está bloqueado.  
- No se hace ampliación sin aprobación del Gerente.  
- No se facturan servicios nuevos si hay mora.  
- No se crean acuerdos “informales”.

---

## 12. Flujo del proceso (Mermaid)

```mermaid
flowchart TD
    A[Cliente solicita crédito] --> B[Administradora recibe información]
    B --> C[Calcular score TRALO]
    C --> D{Score suficiente?}
    D -->|No| E[Rechazo - Contado]
    D -->|Sí| F[Definir límite de crédito]
    F --> G[Registrar condiciones en Odoo]
    G --> H[Cliente activo]
    
    H --> I[Cliente supera límite o entra en mora]
    I --> J[Administradora bloquea cliente en Odoo]
    J --> K[Notificar a Ventas y Gerente]

    K --> L{Cliente solicita ampliación?}
    L -->|Sí| M[Revisar score actualizado]
    M --> N[Gerente aprueba o rechaza]
    N -->|Aprobado| O[Actualizar límite de crédito]
    N -->|Rechazado| P[Mantener bloqueo]
