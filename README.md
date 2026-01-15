# DecisionCore: Event-Driven Decision Engine ⚡

**DecisionCore** es un motor de inferencia de eventos en tiempo real, diseñado para detectar anomalías y facilitar la toma de decisiones automatizadas en entornos de alta incertidumbre.

Inspirado en problemas de **latencia crítica del trading algorítmico**, su arquitectura ha evolucionado hacia un diseño **agnóstico al dominio**, desacoplando completamente la **Ingesta de Datos** de la **Lógica de Negocio**.  
Esto permite su aplicación en **Logística**, **IoT Industrial** y **Fintech** con cambios mínimos de configuración.

![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)
![Architecture](https://img.shields.io/badge/Architecture-Event--Driven-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)

---

## 🚀 Aplicaciones Industriales

Aunque el núcleo matemático es universal, el sistema está optimizado para los siguientes escenarios. Las features listadas corresponden a **implementaciones base extensibles**.

| Sector | Caso de Uso | Feature Engineering |
|:--- |:--- |:--- |
| 📦 **Logística & Retail** | Prevención de quiebre de stock | Detección de picos de demanda (Velocity Index), análisis de estabilidad de flujo |
| 🏭 **IoT & Energía** | Mantenimiento predictivo | Monitoreo de sensores (Z-Score), detección de anomalías, compresión de volatilidad |
| 💳 **Fintech** | Detección de fraude | Patrones transaccionales inusuales, divergencia de tendencias en tiempo real |

---

## 🏗️ Arquitectura de Software

DecisionCore implementa patrones de diseño clásicos (**Adapter**, **Strategy**, **Dependency Injection**) para garantizar **escalabilidad**, **testabilidad** y **mantenibilidad**.

### Flujo de alto nivel
`Data Source` → `Normalización` → `Feature Extraction` → `Contexto Estadístico` → `Regla` → `Evento Accionable`

### Diagrama de Arquitectura

```mermaid
graph LR
    A["Data Source<br/>(SQL / API / IoT)"] -->|Adapter Interface| B[Normalized Data Snapshot]
    B --> C{Feature Engine}
    C -->|Math & Stats| D[Statistical Context]
    D --> E[Decision Core]
    E -->|Business Rules| F[Actionable Event]
🧩 Componentes Principales
Core Engine: Orquestador de decisiones basado en estados y evaluación de contexto.

Feature Library: Librería matemática pura para cálculo estadístico (Z-Score, RSI, Rolling StdDev). Diseñada para funcionar sin dependencias numéricas pesadas (NumPy opcional).

Adapters: Capa de abstracción que normaliza datos provenientes de fuentes heterogéneas (SQL, REST APIs, Streams, sensores IoT).

📂 Estructura del Proyecto
Plaintext

DecisionCore/
├── core/
│   ├── adapters/         # Conectores a fuentes de datos (SQL, APIs, Streams)
│   ├── engine.py         # Motor de inferencia y toma de decisiones
│   ├── features.py       # Funciones matemáticas y estadísticas
│   └── interfaces.py     # Contratos y definiciones de tipos
├── main.py               # Punto de entrada (demo funcional)
├── requirements.txt      # Dependencias ligeras
└── README.md             # Documentación
🛠️ Instalación y Uso
Bash

# 1. Clonar el repositorio
git clone [https://github.com/CienciaEstelar/DecisionCore.git](https://github.com/CienciaEstelar/DecisionCore.git)
cd DecisionCore

# 2. Instalar dependencias
pip install -r requirements.txt

# 3. Ejecutar demo
python main.py

Autor:
Juan de Dios Estudiante de Ingeniería de Ejecución en Computación e Informática — USACH Software Engineer & Data Scientist | Physics Enthusiast

Apasionado por la intersección entre la Física Computacional y la Ingeniería de Software, enfocado en la creación de sistemas resilientes, escalables y eficientes para la industria moderna.
