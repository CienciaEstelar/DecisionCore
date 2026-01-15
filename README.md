# DecisionCore: High-Frequency Event Analysis Engine ⚡

**DecisionCore** es un motor de inferencia de eventos en tiempo real, diseñado para detectar anomalías y facilitar la toma de decisiones automatizada en entornos de alta incertidumbre. 

Originalmente concebido para manejar la latencia crítica del Trading de Alta Frecuencia (HFT), su arquitectura ha evolucionado hacia un diseño **agnóstico al dominio**, desacoplando completamente la **Ingesta de Datos** de la **Lógica de Negocio**. Esto permite su implementación en Logística, IoT Industrial y Fintech con cambios mínimos de configuración.

![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)
![Architecture](https://img.shields.io/badge/Architecture-Event--Driven-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)

## 🚀 Aplicaciones Industriales

Aunque el núcleo matemático es universal, el sistema está optimizado para:

| Sector | Caso de Uso | Feature Engineering (Implementado) |
| :--- | :--- | :--- |
| **📦 Logística & Retail** | **Prevención de Quiebre de Stock** | Detección de picos de demanda (Velocity Index), Análisis de estabilidad de flujo. |
| **🏭 IoT & Energía** | **Mantenimiento Predictivo** | Monitoreo de sensores (Z-Score Anomaly Detection), Compresión de Volatilidad. |
| **💳 Fintech** | **Detección de Fraude** | Patrones transaccionales inusuales, Divergencia de tendencias en tiempo real. |

## 🏗️ Arquitectura de Software

El sistema implementa patrones de diseño robustos (**Adapter**, **Strategy**, **Dependency Injection**) para garantizar la escalabilidad y mantenibilidad.

```mermaid
graph LR
    A["Data Source<br/>(SQL / API / IoT)"] -->|Adapter Interface| B(Normalized Data Snapshot)
    B --> C{Feature Engine}
    C -->|Math & Stats| D[Statistical Context]
    D --> E[Decision Core]
    E -->|Business Rules| F[Actionable Event]
