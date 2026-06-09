# Robotik-Buecher

Buchserie: **Python für Robotik und ROS2**

| Band | Titel | Status |
|------|-------|--------|
| Band 1 | Grundlagen bis ROS2-Einstieg | ✅ in Arbeit |
| Band 2 | ROS2 vertieft: Navigation, Sensorfusion, Docker | 🔲 geplant |
| Band 3 | Embedded AI: OpenCV, YOLO, Edge-Deployment | 🔲 geplant |

## Struktur

```
Robotik-Buecher/
├── shared/          ← zentrale Konfiguration (gilt für alle Bände)
│   ├── preamble.tex
│   └── titelseite.tex
├── band1/
│   ├── main.tex     ← \input{../shared/preamble}
│   └── chapters/
├── band2/
└── band3/
```

## Overleaf-Workflow

1. GitHub Sync → dieses Repo
2. Menu → Main document → `band1/main.tex` für Band 1
3. Menu → Main document → `band2/main.tex` für Band 2

**Ein Repo, ein Overleaf-Projekt, alle Bände.**
