# Robotik-Buecher

Buchserie: **Robotik entwickeln lernen**

| Band | Titel | Status | Compiler |
|------|-------|--------|----------|
| Band 0 | Die Robotik-Werkstatt -- Linux, Docker, Entwicklungswerkzeuge | ✅ in Arbeit | LuaLaTeX |
| Band 1 | Python für Robotik und ROS2 -- Grundlagen bis ROS2-Einstieg | ✅ in Arbeit | pdfLaTeX |
| Band 2 | ROS2 vertieft: Navigation, Sensorfusion, Docker | 🔲 geplant | pdfLaTeX |
| Band 3 | Embedded AI: OpenCV, YOLO, Edge-Deployment | 🔲 geplant | pdfLaTeX |

## Struktur

```
Robotik-Buecher/
├── shared/
│   ├── preamble.tex          ← Basis für pdfLaTeX-Bände (Band 1–3)
│   ├── theme-werkstatt.tex   ← Werkstatt-Theme für Band 0
│   └── titelseite.tex        ← Titelseiten-Template (Band 1–3)
├── band0/
│   ├── main.tex              ← LuaLaTeX, \input{../shared/theme-werkstatt}
│   └── chapters/
├── band1/
│   ├── main.tex              ← pdfLaTeX, \input{../shared/preamble}
│   └── chapters/
├── band2/                    ← Platzhalter
└── band3/                    ← Platzhalter
```

## Overleaf-Workflow

1. GitHub Sync → dieses Repo als ein Overleaf-Projekt
2. `Menu → Main document` wechseln je nach Band:
   - Band 0: `band0/main.tex` → **Compiler: LuaLaTeX**
   - Band 1: `band1/main.tex` → **Compiler: pdfLaTeX**
3. Eine Änderung in `shared/theme-werkstatt.tex` wirkt sofort auf alle Werkstatt-Bände.
4. Eine Änderung in `shared/preamble.tex` wirkt sofort auf Band 1–3.

## Didaktische Struktur

**Band 0 (Werkstatt-Serie):** Problem → Wissenslücke → Lösung → Transfer zu Robotik/ROS2

**Band 1 (Python-Serie):** Lernziele → Analogie → Theorie → Praxis → Übung → ROS2-Verbindung
