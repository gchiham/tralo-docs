# POE-LOG-01 — Despacho y Entrega  
**Versión:** v1.0  
**Área:** Logística  
**Responsable:** Encargado de Logística  
**Aprobado por:** Gerente General  
**Fecha:** 13 de noviembre de 2025

---

## 1. Objetivo
Establecer el procedimiento estándar para programar, despachar y realizar entregas de carga en TRALO, garantizando seguridad, cumplimiento de horarios, comunicación efectiva y trazabilidad operativa.

---

## 2. Alcance
Este procedimiento aplica a:
- Encargado de Logística  
- Operadores (conductores)  
- Asesor de Ventas  
- Administrador  

Cubre todas las operaciones de transporte realizadas por TRALO.

---

## 3. Documentos relacionados
- [POE-VEN-01 Proceso de Ventas](../ventas/POE-VEN-01-proceso-ventas.md)  
- [POE-ADM-01 Facturación y Cobros](../administracion/POE-ADM-01-facturacion-cobros.md)  
- [POE-CRE-01 Gestión de Crédito](../credito/POE-CRE-01-gestion-credito-aprobaciones.md)  
- [MAN-LOG-01 Manual del Operador](../logistica/MAN-LOG-01-manual-operador.md)  
- [CHK-LOG-01 Checklist de Salida](../logistica/CHK-LOG-01-checklist-despacho.md)  

---

## 4. Responsabilidades

### **Encargado de Logística**
- Recibir la orden de servicio enviada por Ventas.  
- Verificar disponibilidad de unidades y operadores.  
- Asignar vehículo y horario.  
- Coordinar con el operador puntos de carga y entrega.  
- Dar seguimiento en tiempo real.  
- Reportar incidentes a Gerente y Ventas.  

### **Operador**
- Completar el checklist de salida (CHK-LOG-01).  
- Cumplir ruta y horario asignado.  
- Mantener comunicación constante con Logística.  
- Tomar evidencia fotográfica y POD.  
- Reportar incidentes de inmediato.  

### **Asesor de Ventas**
- Enviar la orden de servicio completa.  
- Mantener comunicación con el cliente.  
- Coordinar cambios de última hora.  

### **Administrador**
- Validar que el cliente no esté bloqueado.  
- Recibir evidencia final para facturación.  
- Actualizar estado del servicio si hay incidentes.

---

## 5. Procedimiento

### **5.1 Recepción de la orden de servicio**
1. Ventas envía orden de servicio con:
   - Cliente  
   - Ruta  
   - Carga  
   - Fecha y hora  
   - Contactos  
   - Evidencia de tarifa aprobada  

2. Logística debe confirmar recepción en máximo **10 minutos**.

---

### **5.2 Validación del cliente**
El Administrador debe confirmar:

- Cliente activo  
- No bloqueado por crédito  
- No supera el límite de crédito  

Si está bloqueado → **NO se despacha**.

---

### **5.3 Asignación del operador y unidad**
1. Revisar disponibilidad.  
2. Confirmar documentos del vehículo.  
3. Confirmar horario de carga.  
4. Enviar asignación:


### Formato de Despacho – TRALO

- **Cliente:**  
- **Ruta:**  
- **Unidad asignada:**  
- **Operador asignado:**  
- **Salida:**  
- **Entrega estimada:**  

---

### **5.4 Checklist previo (operador)**
El operador debe enviar foto del CHK-LOG-01:

- [ ] Luces  
- [ ] Llantas  
- [ ] Frenos  
- [ ] Documentos  
- [ ] Parabrisas  
- [ ] Combustible  
- [ ] Equipo de seguridad  

---

### **5.5 Carga en origen**
El operador debe:

1. Llegar puntual  
2. Coordinación con contacto  
3. Tomar fotos de carga antes de subir  
4. Verificar coincidencia con orden  
5. Asegurar carga  
6. Enviar fotos a Logística  

---

### **5.6 Ruta y seguimiento**
Logística debe:

- Dar seguimiento por WhatsApp o llamada  
- Mantener comunicación mínima cada etapa  
- Estar atento a incidentes  

Operador debe reportar:

- Salida  
- Avances relevantes  
- Llegada a destino  
- Cualquier retraso o problema  

---

### **5.7 Entrega**
El operador debe:

1. Coordinar con el receptor  
2. Descargar según instrucciones  
3. Tomar fotos de entrega  
4. Obtener POD:
   - Nombre  
   - Firma  
   - Foto de evidencia  

POD debe enviarse a Logística y Administrador.

---

### **5.8 Cierre del servicio**
1. Logística confirma con cliente.  
2. Envia evidencia a Administrador.  
3. Administrador procede con facturación.  
4. Logística archiva evidencias digitalmente.

---

## 6. Prohibiciones

- Salir sin checklist.  
- Despachar clientes bloqueados.  
- Enviar operadores sin contacto claro.  
- No tomar fotos de carga y entrega.  
- Modificar ruta sin autorización.  
- Usar el vehículo para fines personales.

---

## 7. Flujo del proceso (Mermaid)

```mermaid
flowchart TD
    A[Ventas envía orden de servicio] --> B[Logística recibe y confirma]
    B --> C[Administrador valida cliente no bloqueado]
    C -->|Bloqueado| Z[Servicio NO autorizado]
    C -->|Aprobado| D[Asignar operador y unidad]
    D --> E[Operador completa checklist CHK-LOG-01]
    E --> F[Cargar mercancía y enviar fotos]
    F --> G[Seguimiento en ruta]
    G --> H[Entrega y POD]
    H --> I[Enviar evidencia a Administrador]
    I --> J[Facturación inicia proceso]
    J --> K[Cierre del servicio]
