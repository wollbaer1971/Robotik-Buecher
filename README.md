# Robotik-Buecher

Buchserie: **Robotik entwickeln lernen**

## Bände

| Band | Titel | Inhalt | Status |
|------|-------|--------|--------|
| Band 0 | Die Robotik-Werkstatt | Linux, Docker, Entwicklungswerkzeuge | ✅ in Arbeit |
| Band 1 | Python für Robotik und ROS2 | Python-Grundlagen bis ROS2-Einstieg | ✅ in Arbeit |
| Band 2 | ROS2 vertieft | Navigation, Sensorfusion, Docker | 🔲 geplant |
| Band 3 | Embedded AI | OpenCV, YOLO, Edge-Deployment | 🔲 geplant |

## Repo-Struktur

```
Robotik-Buecher/
├── shared/
│   ├── preamble.tex          ← pdfLaTeX-Basis (Band 1–3)
│   ├── theme-werkstatt.tex   ← Werkstatt-Theme: Farben, Boxen, Listings
│   ├── titelseite.tex        ← Titelseiten-Template (Band 1–3)
│   └── frontmatter.tex       ← Bandreihen-Übersicht (alle Bände)
├── band0/
│   ├── main.tex              ← LuaLaTeX + \input{../shared/theme-werkstatt}
│   └── chapters/
│       ├── titelseite.tex    ← Werkstatt-Titelseite (band-eigen)
│       ├── frontmatter.tex   ← Didaktisches Konzept Band 0 (band-eigen)
│       ├── teil1_idee.tex    ← Vollständig ausgearbeitet
│       ├── teil2–9.tex       ← Strukturierte Platzhalter
│       └── anhang.tex
├── band1/
│   ├── main.tex              ← pdfLaTeX + \input{../shared/preamble}
│   └── chapters/             ← 15 Module, 45 Lektionen
├── band2/                    ← Platzhalter
└── band3/                    ← Platzhalter
```

## Shared-Dateien im Überblick

| Datei | Verwendung | Bände |
|-------|-----------|-------|
| `shared/preamble.tex` | pdfLaTeX-Pakete, Farben, Boxen (Band 1-Stil) | Band 1–3 |
| `shared/theme-werkstatt.tex` | Werkstatt-Farben, 10 Boxtypen, 5 Code-Stile | Band 0 |
| `shared/titelseite.tex` | Titelseiten-Template mit Band-Variablen | Band 1–3 |
| `shared/frontmatter.tex` | Bandreihen-Übersichtstabelle | alle Bände |

## Overleaf-Einrichtung pro Band

| Band | Main document | Compiler | Hinweis |
|------|---------------|----------|---------|
| Band 0 | `band0/main.tex` | **LuaLaTeX** | fontspec erfordert LuaLaTeX |
| Band 1 | `band1/main.tex` | pdfLaTeX | Standard |
| Band 2 | `band2/main.tex` | pdfLaTeX | Standard |
| Band 3 | `band3/main.tex` | pdfLaTeX | Standard |

**Compiler umstellen:** Overleaf → Menu → Compiler

## Didaktische Konzepte

**Band 0 (Werkstatt-Serie)**
Problem → Wissenslücke → Lösung → Typische Fehler → Merksatz → Übungen → Quiz → Unter der Haube → Transfer

**Band 1 (Python-Serie)**
Lernziele → Analogie → Theorie → Praxis → Übung → ROS2-Verbindung

## Neue Kapitel schreiben

Band 0: `band0/chapters/anhang.tex` enthält das Kapitel-Template mit allen 14 Schritten.

Band 1: Kapitelstruktur folgt modul01.tex als Vorlage.
