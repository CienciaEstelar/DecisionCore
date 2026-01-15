# DecisionCore: Event-Driven Decision Engine ⚡

DecisionCore es un motor de inferencia de eventos en tiempo real, diseñado para detectar anomalías y facilitar la toma de decisiones automatizadas en entornos de alta incertidumbre.

Inspirado en problemas de latencia crítica del trading algorítmico, su arquitectura ha evolucionado hacia un diseño agnóstico al dominio, desacoplando completamente la Ingesta de Datos de la Lógica de Negocio.  
Esto permite su implementación inmediata en Logística, IoT Industrial y Fintech con cambios mínimos de configuración.

Python 3.11+ | Architecture: Event-Driven | License: MIT | Status: Active

---------------------------------------------------------------------

🚀 APLICACIONES INDUSTRIALES

Aunque el núcleo matemático es universal, el sistema está optimizado para los siguientes escenarios.  
Las features listadas corresponden a implementaciones base extensibles.

Sector: Logística & Retail  
Caso de uso: Prevención de quiebre de stock  
Feature engineering: Detección de picos de demanda (Velocity Index), análisis de estabilidad de flujo

Sector: IoT & Energía  
Caso de uso: Mantenimiento predictivo  
Feature engineering: Monitoreo de sensores (Z-Score), detección de anomalías, compresión de volatilidad

Sector: Fintech  
Caso de uso: Detección de fraude  
Feature engineering: Patrones transaccionales inusuales, divergencia de tendencias en tiempo real

---------------------------------------------------------------------

🏗️ ARQUITECTURA DE SOFTWARE

DecisionCore implementa patrones de diseño clásicos como Adapter, Strategy y Dependency Injection para garantizar escalabilidad, mantenibilidad y testabilidad.

Flujo lógico de datos:

Data Source -> Normalización -> Feature Extraction -> Contexto Estadístico -> Regla -> Evento Accionable

Diagrama conceptual de arquitectura (Mermaid):

graph LR
    A["Data Source (SQL / API / IoT)"] -->|Adapter Interface| B[Normalized Data Snapshot]
    B --> C[Feature Engine]
    C --> D[Statistical Context]
    D --> E[Decision Core]
    E --> F[Actionable Event]

---------------------------------------------------------------------

🧩 COMPONENTES PRINCIPALES

Core Engine  
Orquestador de decisiones basado en estados y evaluación de contexto estadístico.

Feature Library  
Librería matemática pura para cálculo estadístico (Z-Score, RSI, Rolling StdDev).  
Diseñada para funcionar sin dependencias numéricas pesadas (NumPy opcional).

Adapters  
Capa de abstracción que normaliza datos provenientes de fuentes heterogéneas como SQL, REST APIs, WebSockets y sensores IoT.

---------------------------------------------------------------------

📂 ESTRUCTURA DEL PROYECTO

DecisionCore/
├── core/
│   ├── adapters/         Conectores a fuentes de datos (SQL, APIs, Streams)
│   ├── engine.py         Motor de inferencia y toma de decisiones
│   ├── features.py       Funciones matemáticas y estadísticas
│   └── interfaces.py     Contratos y definiciones de tipos
├── main.py               Punto de entrada (demo funcional)
├── requirements.txt      Dependencias ligeras
└── README.md             Documentación

---------------------------------------------------------------------

🛠️ INSTALACIÓN Y USO

1. Clonar el repositorio

git clone https://github.com/CienciaEstelar/DecisionCore.git
cd DecisionCore

2. Instalar dependencias

pip install -r requirements.txt

3. Ejecutar demo

python main.py

---------------------------------------------------------------------

👨‍💻 AUTOR

Juan de Dios  
Estudiante de Ingeniería de Ejecución en Computación e Informática — USACH  
Software Engineer & Data Scientist | Physics Enthusiast

Apasionado por la intersección entre la Física Computacional y la Ingeniería de Software, enfocado en la creación de sistemas resilientes, escalables y eficientes para la industria moderna.
