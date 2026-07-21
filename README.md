# Robotik-Buecher

Buchserie: **Robotik entwickeln lernen**

## Bände

| Band | Titel | Inhalt | Status |
|---|---|---|---|
| 1 | Die Robotik-Werkstatt       | Linux, Docker, Entwicklungswerkzeuge | ✅ fertig (28 Kap.) |
| 2 | Python für Robotik und ROS2 | Python, rclpy, autonome Navigation   | 🔨 Entwurf (15 Kap.) |
| 3 | C++ für Robotik und ROS2    | C++17, rclcpp, Lifecycle Nodes       | 🔨 Entwurf (13 Kap.) |
| 4 | ROS2 vertieft               | SLAM, Nav2, micro-ROS                | 🔲 geplant |
| 5 | Embedded AI                 | OpenCV, YOLO, Edge-Deployment        | 🔲 geplant |
| 6 | Mathematik I                | Mobile Roboter, Kinematik            | 🔲 geplant |
| 7 | Mathematik II               | Manipulatoren, Dynamik               | 🔲 geplant |

## Referenzprojekt

Alle Bände arbeiten mit demselben Hardware-Projekt:
**robotik-uno-q** (Arduino UNO Q + L298N + HC-SR04-Dual-Sensor).
Repo: [`wollbaer1971/robotik-uno-q`](https://github.com/wollbaer1971/robotik-uno-q)

## Repo-Struktur

```
Robotik-Buecher/
├── shared/
│   ├── preamble.tex          ← pdfLaTeX-Basis: Pakete, Farben, Box-Umgebungen (Band 2–7)
│   ├── theme-werkstatt.tex   ← Werkstatt-Theme: Farben, 10 Boxtypen, Listings (Band 1)
│   ├── titelseite.tex        ← Titelseiten-Template mit Band-Variablen (Band 2–7)
│   └── frontmatter.tex       ← Bandreihen-Übersichtstabelle (alle Bände)
├── band1/
│   ├── main.tex              ← LuaLaTeX, KDP-Format (6,69 × 9,61 Zoll)
│   └── chapters/
│       ├── teil1_idee.tex    ← Kap. 1–2:   Die Idee der Robotik-Werkstatt
│       ├── teil2.tex         ← Kap. 3–7:   Linux praktisch
│       ├── teil3.tex         ← Kap. 8–10:  Skripte & YAML
│       ├── teil4.tex         ← Kap. 11–12: VS Code & Projektstruktur
│       ├── teil5.tex         ← Kap. 13–15: Git & GitHub
│       ├── teil6.tex         ← Kap. 16–20: Docker
│       ├── teil7.tex         ← Kap. 21–22: IPC & Pub-Sub
│       ├── teil8.tex         ← Kap. 23–25: Hardware, udev, Echtzeit
│       ├── teil9.tex         ← Kap. 26–29: ROS2-Vorbereitung
│       └── anhang.tex        ← Befehlsübersicht + Kapitel-Template
├── band2/
│   ├── main.tex              ← pdfLaTeX + \input{../shared/preamble}
│   └── chapters/
│       ├── teil1_python_kompakt.tex   ← Kap. 1–5:  Python-Grundlagen für ROS2
│       ├── teil2_bibliotheken.tex     ← Kap. 6–8:  NumPy, Matplotlib, OpenCV
│       ├── teil3_rclpy.tex            ← Kap. 9–14: ROS2 mit Python (rclpy)
│       └── teil4_projekt.tex          ← Kap. 15:   vollständiger Node-Stack
├── band3/
│   ├── main.tex              ← pdfLaTeX + \input{../shared/preamble}
│   └── chapters/
│       ├── teil1_cpp_kompakt.tex      ← Kap. 1–4:  C++17 für ROS2
│       ├── teil2_rclcpp.tex           ← Kap. 5–8:  ROS2 mit C++ (rclcpp)
│       ├── teil3_echtzeit.tex         ← Kap. 9–11: Echtzeit, Latenz, Profiling
│       └── teil4_projekt.tex          ← Kap. 12–13: hybrides Python/C++-Deployment
├── band4/                    ← Platzhalter (main.tex)
└── band5–7/                  ← geplant
```

## Shared-Dateien

| Datei | Verwendung | Bände |
|---|---|---|
| `shared/preamble.tex` | pdfLaTeX-Pakete, Farben, Box-Umgebungen | 2–7 |
| `shared/theme-werkstatt.tex` | Werkstatt-Theme, 10 Boxtypen, 5 Code-Stile | 1 |
| `shared/titelseite.tex` | Titelseiten-Template (nutzt `\BandTitel`, `\BandNummer` etc.) | 2–7 |
| `shared/frontmatter.tex` | Bandreihen-Übersichtstabelle, roter Faden | alle |

## Overleaf-Einrichtung

| Band | Main document | Compiler | Hinweis |
|---|---|---|---|
| 1 | `band1/main.tex` | **LuaLaTeX** | fontspec erfordert LuaLaTeX |
| 2 | `band2/main.tex` | pdfLaTeX | |
| 3 | `band3/main.tex` | pdfLaTeX | |
| 4–7 | `bandX/main.tex` | pdfLaTeX | |

**Compiler umstellen:** Overleaf → Menu → Compiler → Main document → `bandX/main.tex`

## Didaktisches Schema

Jedes Kapitel folgt demselben Aufbau:

> **Situation → Aufgabe → Erster Versuch → Problem → Wissen → Lösung →
> Projektstand (robotik-uno-q) → Merksatz → Typische Fehler → Übungen →
> Quiz → Unter der Haube → ROS2-Transfer**

Box-Umgebungen: `aufgabeBox`, `problemBox`, `wissenBox`, `loesungBox`,
`merksatzBox`, `fehlerBox`, `uebungBox`, `quizBox`, `haubeBox`,
`robotikBox`, `projektBox` — definiert in `shared/preamble.tex` (Band 2–7)
bzw. `shared/theme-werkstatt.tex` (Band 1).

## Neue Kapitel schreiben

**Band 1:** `band1/chapters/anhang.tex` enthält das vollständige Kapitel-Template.

**Band 2 (Python):** `band2/chapters/teil1_python_kompakt.tex` Kap. 1 als Vorlage.

**Band 3 (C++):** `band3/chapters/teil1_cpp_kompakt.tex` Kap. 1 als Vorlage.
