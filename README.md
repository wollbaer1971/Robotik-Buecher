# Robotik-Buecher

Buchserie: **Robotik entwickeln lernen**

## Bände

| Band | Titel | Inhalt | Status |
|------|-------|--------|--------|
| Band 1 | Die Robotik-Werkstatt | Linux, Docker, Entwicklungswerkzeuge | ✅ in Arbeit |
| Band 2 | Python für Robotik und ROS2 | Python-Grundlagen bis ROS2-Einstieg | ✅ in Arbeit |
| Band 3 | ROS2 vertieft | Navigation, Sensorfusion, Docker | 🔲 geplant |
| Band 4 | Embedded AI | OpenCV, YOLO, Edge-Deployment | 🔲 geplant |

## Repo-Struktur

```
Robotik-Buecher/
├── shared/
│   ├── preamble.tex          ← pdfLaTeX-Basis (Band 2–4)
│   ├── theme-werkstatt.tex   ← Werkstatt-Theme: Farben, Boxen, Listings
│   ├── titelseite.tex        ← Titelseiten-Template (Band 2–4)
│   └── frontmatter.tex       ← Bandreihen-Übersicht (alle Bände)
├── band1/
│   ├── main.tex              ← LuaLaTeX + \input{../shared/theme-werkstatt}
│   └── chapters/
│       ├── titelseite.tex    ← Werkstatt-Titelseite (band-eigen)
│       ├── frontmatter.tex   ← Didaktisches Konzept Band 1 (band-eigen)
│       ├── teil1_idee.tex    ← Vollständig ausgearbeitet
│       ├── teil2–9.tex       ← Strukturierte Platzhalter
│       └── anhang.tex
├── band2/
│   ├── main.tex              ← pdfLaTeX + \input{../shared/preamble}
│   └── chapters/             ← 15 Module, 45 Lektionen
├── band3/                    ← Platzhalter
└── band4/                    ← Platzhalter
```

## Shared-Dateien im Überblick

| Datei | Verwendung | Bände |
|-------|-----------|-------|
| `shared/preamble.tex` | pdfLaTeX-Pakete, Farben, Boxen (Band 2-Stil) | Band 2–4 |
| `shared/theme-werkstatt.tex` | Werkstatt-Farben, 10 Boxtypen, 5 Code-Stile | Band 1 |
| `shared/titelseite.tex` | Titelseiten-Template mit Band-Variablen | Band 2–4 |
| `shared/frontmatter.tex` | Bandreihen-Übersichtstabelle | alle Bände |

## Overleaf-Einrichtung pro Band

| Band | Main document | Compiler | Hinweis |
|------|---------------|----------|---------|
| Band 1 | `band1/main.tex` | **LuaLaTeX** | fontspec erfordert LuaLaTeX |
| Band 2 | `band2/main.tex` | pdfLaTeX | Standard |
| Band 3 | `band3/main.tex` | pdfLaTeX | Standard |
| Band 4 | `band4/main.tex` | pdfLaTeX | Standard |

**Compiler umstellen:** Overleaf → Menu → Compiler

## Didaktische Konzepte

**Band 1 (Werkstatt-Serie)**
Problem → Wissenslücke → Lösung → Typische Fehler → Merksatz → Übungen → Quiz → Unter der Haube → Transfer

**Band 2 (Python-Serie)**
Lernziele → Analogie → Theorie → Praxis → Übung → ROS2-Verbindung

## Neue Kapitel schreiben

Band 1: `band1/chapters/anhang.tex` enthält das Kapitel-Template mit allen 14 Schritten.

Band 2: Kapitelstruktur folgt modul01.tex als Vorlage.
