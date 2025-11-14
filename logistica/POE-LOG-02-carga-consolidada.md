# POE-LOG-02 — Carga Consolidada  
**Versión:** v1.0  
**Área:** Logística  
**Responsable:** Encargado de Logística  
**Aprobado por:** Gerente General  
**Fecha:** 13 de noviembre de 2025

---

## 1. Objetivo
Establecer el procedimiento estándar para la gestión, coordinación y entrega de servicios de carga consolidada en TRALO, asegurando que cada destino, cliente y paquete se registre, controle y entregue correctamente.

---

## 2. Alcance
Este procedimiento aplica a:
- Encargado de Logística  
- Operadores  
- Asesor de Ventas  
- Administrador  

Cubre todos los servicios donde un mismo viaje incluye múltiples entregas.

---

## 3. Documentos relacionados
- [POE-VEN-01 Proceso de Ventas](../ventas/POE-VEN-01-proceso-ventas.md)  
- [POE-LOG-01 Despacho y Entrega](../logistica/POE-LOG-01-despacho-entrega.md)  
- [POE-ADM-01 Facturación y Cobros](../administracion/POE-ADM-01-facturacion-cobros.md)  
- [CHK-LOG-01 Checklist de Salida](../logistica/CHK-LOG-01-checklist-despacho.md)  

---

## 4. Definición de Carga Consolidada
Servicio donde varios clientes o un cliente con múltiples destinos son atendidos en un solo viaje, compartiendo unidad, operador y ruta base.

---

## 5. Responsabilidades

### **Encargado de Logística**
- Organizar rutas por zonas.  
- Generar el listado consolidado.  
- Definir orden de entregas.  
- Coordinar horarios y puntos con el operador.  
- Confirmar entregas con clientes.  

### **Operador**
- Completar checklist CHK-LOG-01.  
- Respetar secuencia asignada.  
- Verificar cada paquete antes de entregar.  
- Tomar evidencia por destino.  
- Obtener POD en cada entrega.  

### **Asesor de Ventas**
- Enviar información correcta por cliente/destino.  
- Confirmar tarifas individuales.  
- Atender consultas del cliente final.  

### **Administrador**
- Validar que clientes no estén bloqueados.  
- Recibir evidencia final para facturación.  

---

## 6. Procedimiento

### **6.1 Recepción de solicitudes**
Ventas envía lista de entregas con:

- Cliente  
- Dirección  
- Persona que recibe  
- Teléfono  
- Tipo de paquete  
- Tarifa por entrega  
- Observaciones  

---

### **6.2 Consolidación de ruta**
Logística agrupa por:

- Zonas  
- Proximidad  
- Horarios  
- Prioridad  

Luego genera el:

### Listado Consolidado – TRALO

### Formato de Consolidado – TRALO

- **Ruta principal:**  
- **Unidad asignada:**  
- **Operador asignado:**  
- **Salida:**  
- **Entrega estimada final:**  

### Entregas:
1. **Cliente:**  
   - **Dirección:**  
   - **Contacto:**  
   - **Teléfono:**  
   - **Paquete:**  
   - **Tarifa:**  
   - **Observaciones:**  

2. **Cliente:**  
   - **Dirección:**  
   - **Contacto:**  
   - **Teléfono:**  
   - **Paquete:**  
   - **Tarifa:**  
   - **Observaciones:**  

*(Se repite según cantidad de entregas)*

---

### **6.3 Validación del cliente**
Administrador valida:

- Cliente activo  
- Sin bloqueo  
- Información fiscal correcta  

Si está bloqueado → NO se incluye en el consolidado.

---

### **6.4 Asignación de operador y unidad**
Logística asigna operador y comunica:

- Hora de salida  
- Secuencia de entregas  
- Listado consolidado  
- Fotos o descripción de paquetes  

---

### **6.5 Checklist previo**
Operador completa CHK-LOG-01 y envía foto a Logística.

---

### **6.6 Carga y reconocimiento**
El operador debe:

- Tomar foto de cada paquete  
- Ordenar carga según secuencia  
- Asegurar cada paquete  
- Enviar fotos de carga final  

---

### **6.7 Entregas**
En cada destino operador debe:

- Confirmar nombre del receptor  
- Tomar foto del paquete antes de entregar  
- Obtener POD:  
  - Nombre  
  - Firma  
  - Foto de evidencia  
- Reportar entrega a Logística  

---

### **6.8 Cierre del consolidado**
- Logística confirma entregas con cada cliente.  
- Envia evidencia completa al Administrador.  
- Administrador inicia proceso de facturación por entrega.  
- Logística archiva evidencia digital.

---

## 7. Prohibiciones

- Entregar paquetes a personas no autorizadas.  
- Cambiar el orden de entregas sin aprobación.  
- No enviar evidencia fotográfica.  
- Transportar paquetes no registrados.  
- Marcar entregas como realizadas sin POD.  
- Dejar carga sin supervisión.  

---

## 8. Flujo del proceso (Mermaid)

```mermaid
flowchart TD
    A[Ventas envía solicitudes] --> B[Logística consolida entregas]
    B --> C[Administrador valida clientes]
    C -->|Bloqueado| Z[Entrega NO autorizada]
    C -->|Aprobado| D[Asignar unidad y operador]
    D --> E[Operador realiza checklist]
    E --> F[Cargar y organizar paquetes]
    F --> G[Ejecución de entregas múltiples]
    G --> H[Evidencia por destino]
    H --> I[Logística confirma con clientes]
    I --> J[Administrador envía a facturación]
    J --> K[Cierre del consolidado]
