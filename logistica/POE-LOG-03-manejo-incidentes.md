# POE-LOG-03 — Manejo de Incidentes Operativos  
**Versión:** v1.0  
**Área:** Logística  
**Responsable:** Encargado de Logística  
**Aprobado por:** Gerente General  
**Fecha:** 13 de noviembre de 2025

---

## 1. Objetivo
Establecer el procedimiento estándar para gestionar incidentes operativos en TRALO, asegurando respuesta rápida, comunicación clara, evidencia completa y reducción de riesgos para el cliente, el operador y la empresa.

---

## 2. Alcance
Este procedimiento aplica a:
- Encargado de Logística  
- Operadores  
- Administrador  
- Gerente General  

Incluye todo incidente ocurrido antes, durante o después de un servicio de transporte.

---

## 3. Documentos relacionados
- [POE-LOG-01 Despacho y Entrega](../logistica/POE-LOG-01-despacho-entrega.md)  
- [CHK-LOG-01 Checklist de Salida](../logistica/CHK-LOG-01-checklist-despacho.md)  
- [MAN-LOG-01 Manual del Operador](../logistica/MAN-LOG-01-manual-operador.md)  

---

## 4. Definición de Incidente Operativo

Se considera incidente operativo cualquier situación que afecte:

- Seguridad del operador  
- Integridad de la carga  
- Tiempos de entrega  
- Documentación  
- Imagen de la empresa  
- Continuidad del servicio  

### Tipos comunes de incidentes:
- Retraso mayor a 15 minutos  
- Fallas mecánicas  
- Llantas dañadas  
- Accidente vial  
- Carga dañada o mal manipulada  
- Problemas con el cliente  
- Dirección incorrecta  
- Operador extraviado  
- Intentos de robo  
- Clima extremo  
- Unidad inmovilizada  

---

## 5. Responsabilidades

### **Operador**
- Reportar el incidente inmediatamente.  
- Enviar evidencia completa (fotos, video, ubicación).  
- No abandonar la unidad.  
- Seguir instrucciones de Logística.  

### **Encargado de Logística**
- Atender el reporte en tiempo real.  
- Evaluar el nivel de gravedad.  
- Informar al Administrador y/o Gerente.  
- Coordinar acciones (grúa, soporte, reemplazo).  
- Mantener informado al cliente.  

### **Administrador**
- Registrar el incidente en el sistema interno.  
- Generar reporte para facturación si aplica.  
- Revisar posibles reclamos de clientes.  

### **Gerente General**
- Tomar decisiones en casos graves:  
  - Carga perdida  
  - Accidentes mayores  
  - Conflictos con autoridades  
  - Incidentes legales  

---

## 6. Procedimiento

---

### **6.1 Reporte inmediato del Operador**

El operador debe enviar por WhatsApp:

### Formato de Reporte de Incidente – TRALO

- **Tipo de incidente:**  
- **Ubicación:**  
- **Hora:**  
- **Descripción:**  
- **Fotos y/o video:**  
- **Riesgos actuales:**  
- **Necesita asistencia:** Sí / No  

---

### **6.2 Tipos de incidente y respuesta**

---

### **A. Retrasos**
- Operador notifica motivo y tiempo estimado.  
- Logística informa al cliente.  
- Nuevo horario se registra.  

---

### **B. Fallas mecánicas**
- Operador envía fotos.  
- Logística determina si se repara en sitio o se envía grúa.  
- Si la carga es urgente → asignar unidad de reemplazo.  

---

### **C. Llantas dañadas**
- Operador debe usar repuesto si es seguro.  
- Si no es posible → grúa o soporte mecánico.  

---

### **D. Accidentes viales**
- Prioridad: integridad del operador.  
- Llamar 911 si aplica.  
- Tomar fotos de:  
  - Placas  
  - Vehículos involucrados  
  - Carga  
  - Área del accidente  
- Notificar a cliente y Gerente General.  

---

### **E. Robo o intento de robo**
- Operador debe ponerse a salvo.  
- NO confrontar.  
- Reportar a autoridades y logística.  

---

### **F. Carga dañada**
- Tomar fotos inmediatamente.  
- No descargar sin autorización del cliente.  
- Logística coordina con cliente solución.  

---

## 7. Comunicación con el cliente
Logística debe informar al cliente:

- Tipo de incidente  
- Evidencia cuando aplique  
- Medidas tomadas  
- Nuevo tiempo de entrega  

Toda comunicación debe quedar registrada.

---

## 8. Cierre del incidente
1. Logística verifica que el servicio fue finalizado.  
2. Administrador documenta el incidente.  
3. Si hubo daño o pérdida → generar reporte interno.  
4. Gerente decide si aplica ajuste en tarifa o reclamo.  
5. Se archiva evidencia en carpeta digital.  

---

## 9. Prohibiciones

- No reportar incidentes.  
- Mentir sobre ubicación o estado de la unidad.  
- Omitir fotos.  
- Abandonar la unidad.  
- Tratar de resolver incidentes graves sin apoyo.  
- Ocultar daños a la carga o unidad.  

---

## 10. Flujo del proceso (Mermaid)

```mermaid
flowchart TD
    A[Incidente ocurre] --> B[Operador reporta al instante]
    B --> C[Logística evalúa gravedad]
    C -->|Leve| D[Informar cliente y continuar]
    C -->|Moderado| E[Coordinar asistencia o retraso]
    C -->|Grave| F[Notificar Gerente General]
    E --> G[Operador retoma ruta]
    F --> H[Decisiones críticas: grúa, reemplazo, autoridad]
    G --> I[Entrega finalizada]
    H --> I[Entrega finalizada o servicio cancelado]
    I --> J[Administrador registra incidente]
    J --> K[Cierre y archivo]
