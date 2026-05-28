# 🚴 Bicicleta — Training Dashboard

Dashboard personal de entrenamientos en bicicleta. Diseñado para monitorear progreso cardiovascular, consistencia y recuperación.

## 📊 Ver Dashboard

👉 **[sakhbeconsultores.github.io/Bicicleta](https://sakhbeconsultores.github.io/Bicicleta)**

## 🔧 Cómo funciona

- Los datos se registran manualmente en **Notion** después de cada sesión
- Un **GitHub Action** corre cada noche y jala los datos vía la API de Notion
- El dashboard HTML se actualiza automáticamente y se publica en GitHub Pages

## 📈 Métricas monitoreadas

- Consistencia semanal y mensual
- Tiempo en zonas cardíacas (Zona 1–5)
- Cadencia promedio y tendencia
- FC de recuperación (1 minuto post-esfuerzo)
- Eficiencia cardiovascular (velocidad / FC)
- Bienestar subjetivo: energía, sueño, dolor articular

## 🗂 Estructura del repositorio

```
Bicicleta/
├── index.html          # Dashboard principal
├── data/
│   └── sessions.json   # Datos exportados desde Notion
├── .github/
│   └── workflows/
│       └── sync.yml    # GitHub Action de sincronización diaria
└── README.md
```

## ⚙️ Configuración

Para activar la sincronización automática, agrega estos secrets en tu repositorio:

| Secret | Descripción |
|--------|-------------|
| `NOTION_TOKEN` | Token de integración de Notion |
| `NOTION_DATABASE_ID` | ID de la base de datos "Sesiones de Bicicleta" |

---

*Proyecto personal — Gustavo Mondragón*
