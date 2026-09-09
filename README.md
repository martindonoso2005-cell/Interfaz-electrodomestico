# Entrega 1: Lámina de Análisis — Interfaces de un Electrodoméstico
**Asignatura:** Taller de Interfaces (2026) | Universidad Adolfo Ibáñez  
**Estudiante:** Martín Donoso  
**Profesor:** Jorge Forero  
**Portafolio Web:** [Ver Proyecto Desplegado](https://martindonoso2005-cell.github.io/Interfaz-electrodomestico/)

---

## 1. Producto Seleccionado y Contexto de Uso
* **Objeto:** Hervidor Eléctrico Digital (Modelo Genérico con Control Térmico).
* **Función Principal:** Ebullición y control térmico programable de agua para consumo doméstico mediante resistencia eléctrica.
* **Contexto de Uso:** Superficie de trabajo en cocina/encimera. Interacción orientada a ciclos rápidos, segura ante altas temperaturas y con retroalimentación clara en tiempo real.

---

## 2. Clasificación de Interfaces

A continuación se detalla la matriz de entradas (*inputs*) y salidas (*outputs*) modeladas en el análisis, clasificadas según su tipología:

| Tipo de Interfaz | Entradas (Inputs del Usuario / Sistema) | Salidas (Outputs del Producto) |
| :--- | :--- | :--- |
| **Física** | • Botón de encendido / apagado.<br>• Selector de temperatura (ajuste térmico).<br>• Botón / pulsador indicador de nivel de agua.<br>• Tapa de apertura fácil (accionamiento mecánico). | • Calor transferido al agua (resistencia térmica).<br>• Evaporación y disipación de calor.<br>• Flujo / vertido de agua caliente hacia el exterior. |
| **Visual / Gráfica** | • Referencias gráficas y marcas serigrafiadas en el panel de control. | • Pantalla LCD con lectura de temperatura actual.<br>• Pantalla LCD con visualización de temperatura seleccionada / final.<br>• Luz indicadora LED de encendido/operación.<br>• Agua hirviendo y burbujeo visible a través del cuerpo/visor. |
| **Acústica / Audio** | • *(No aplica input acústico directo en modelos manuales)*. | • Señal acústica (*bip*) de inicio de ciclo.<br>• Sonido natural de ebullición del agua.<br>• Señal acústica (*bip*) al alcanzar la temperatura programada / ebullición. |

---

## 3. Diagrama de Flujo de Interacción

El siguiente diagrama modela la secuencia operativa entre las acciones del usuario y las respuestas automáticas del sistema:

```text
[ INICIO ]
    │
    ▼
[ 1. Conectar a la red eléctrica (Input Físico) ]
    │
    ▼
[ 2. Abrir tapa y cargar agua (Input Físico) ]
    │
    ▼
[ 3. Seleccionar temperatura deseada y pulsar Encendido (Input Físico) ]
    │
    ├─► Feedback Inmediato: Bip sonoro inicial (Output Acústico)
    ├─► Feedback Visual: Luz LED activa + Pantalla LCD muestra temp. objetivo
    │
    ▼
[ 4. Fase de calentamiento en curso ]
    │
    ├─► Output Físico: Transferencia de calor por resistencia
    ├─► Output Visual: LCD actualiza temperatura en tiempo real + Burbujeo
    ├─► Output Acústico: Sonido progresivo de ebullición
    │
    ▼
[ 5. El agua alcanza la temperatura programada ]
    │
    ├─► Output Acústico: Bip sonoro de finalización / corte
    ├─► Output Visual: LCD confirma temperatura final; Luz LED cambia o se apaga
    ├─► Output Físico: Corte térmico automático (paro de resistencia)
    │
    ▼
[ 6. Servir agua caliente a través de la boquilla (Output Físico) ]
    │
    ▼
[ FIN ]
