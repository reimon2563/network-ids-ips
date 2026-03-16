# 🦹‍♂️ Sistema de Detección de Intrusiones (IDS/IPS)

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)](https://python.org/)
[![Machine Learning](https://img.shields.io/badge/ML-TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)](https://tensorflow.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)](https://docker.com/)
[![Snort](https://img.shields.io/badge/Snort-2A2A2A?style=flat)](https://snort.org/)

Sistema de detección y prevención de intrusiones con Machine Learning para analizar tráfico de red en tiempo real.

## ✨ Características

- 🔍 Detección de anomalías en tráfico de red
- 🤖 Machine Learning para clasificación de amenazas
- 📊 Dashboard en tiempo real con Grafana
- 🚨 Alertas instantáneas por Telegram/Slack
- 📝 Logs estructurados con ELK Stack
- 🐳 Despliegue completo con Docker Compose

## 🏗️ Arquitectura

```
┌─────────────────────────────────────────────────────────────┐
│                    Captura de Tráfico                        │
│                    (tcpdump / ngrep)                        │
└──────────────────────────┬──────────────────────────────────┘
                           │
              ┌────────────▼────────────┐
              │   ML Engine (TensorFlow) │
              │   Random Forest / LSTM   │
              └────────────┬────────────┘
                           │
        ┌─────────────────┼─────────────────┐
        │                 │                 │
   ┌────▼────┐      ┌─────▼─────┐     ┌────▼────┐
   │  Alerta │      │  Grafana  │     │  ELK    │
   │ Telegram│      │ Dashboard  │     │ Stack   │
   └─────────┘      └───────────┘     └─────────┘
```

## 🚀 Despliegue

```bash
git clone https://github.com/reimon2563/network-ids-ips.git
cd network-ids-ips

# Iniciar sistema completo
docker-compose up -d

# Acceder a Grafana
# http://localhost:3000 (admin/admin)
```

## 📊 Monitoreo

| Métrica | Descripción |
|---------|-------------|
| Paquetes/seg | Tráfico de red |
| Amenazas detectadas | Alertas clasificadas |
| Falsos positivos | Predicciones ML |
| Anomalías | Comportamiento inusual |

## 🛡️ Tipos de Detección

- **Signature-based**: Detección por patrones conocidos
- **Anomaly-based**: ML para comportamiento anómalo
- **Protocol analysis**: Violaciones de protocolo
- **Traffic analysis**: Patrones de tráfico suspeitos

## 📝 Licencia

MIT License - © 2026 reimon2563