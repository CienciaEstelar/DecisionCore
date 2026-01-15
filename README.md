DecisionCore: High-Frequency Event Analysis Engine ⚡DecisionCore es un motor de inferencia de eventos en tiempo real, diseñado para detectar anomalías y facilitar la toma de decisiones automatizadas en entornos de alta incertidumbre.Originalmente inspirado en la latencia crítica del trading algorítmico, su arquitectura ha evolucionado hacia un diseño agnóstico al dominio, desacoplando completamente la Ingesta de Datos de la Lógica de Negocio. Esto permite su implementación inmediata en Logística, IoT Industrial y Fintech.🚀 Aplicaciones IndustrialesAunque el núcleo matemático es universal, el sistema está optimizado para:SectorCaso de UsoFeature Engineering (Implementado)📦 LogísticaPrevención de quiebre de stockDetección de picos de demanda (Velocity Index)🏭 IoTMantenimiento predictivoMonitoreo de sensores (Z-Score), Anomalías💳 FintechDetección de fraudePatrones inusuales, Divergencia de tendencias🏗️ Arquitectura de SoftwareEl sistema implementa patrones de diseño robustos como Adapter, Strategy y Dependency Injection para garantizar la máxima escalabilidad.Flujo de Datosgraph LR
    A["Data Source<br/>(SQL / API / IoT)"] -->|Adapter| B(Normalized Snapshot)
    B --> C{Feature Engine}
    C -->|Stats| D[Statistical Context]
    D --> E[Decision Core]
    E -->|Business Rules| F[Actionable Event]
🧩 Componentes PrincipalesCore Engine: Orquestador de decisiones basado en estados y evaluación de contexto histórico.Feature Library: Librería matemática pura para cálculo estadístico (Z-Score, RSI, Rolling StdDev) sin dependencias pesadas.Adapters: Capa de abstracción que normaliza datos de fuentes heterogéneas (SQL, REST APIs, sensores).📂 Estructura del ProyectoDecisionCore/
├── core/
│   ├── adapters/     # Conectores a fuentes de datos (SQL, APIs)
│   ├── engine.py     # Motor de inferencia y toma de decisiones
│   ├── features.py   # Librería matemática y estadística
│   └── interfaces.py # Contratos y definiciones de tipos
├── main.py           # Punto de entrada (Demo funcional)
├── requirements.txt  # Dependencias ligeras
└── README.md         # Documentación
🛠️ Instalación y Uso# 1. Clonar el repositorio
git clone [https://github.com/CienciaEstelar/DecisionCore.git](https://github.com/CienciaEstelar/DecisionCore.git)
cd DecisionCore

# 2. Instalar dependencias
pip install -r requirements.txt

# 3. Ejecutar demostración
python main.py
👨‍💻 AutorJuan de DiosEstudiante de Ingeniería de Ejecución en Computación e Informática — USACHSoftware Engineer & Data Scientist | Physics EnthusiastApasionado por la intersección entre la Física Computacional y la Ingeniería de Software, enfocado en la creación de sistemas resilientes y eficientes para la industria moderna.
