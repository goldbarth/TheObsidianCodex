# Top-Down RPG Prototyp

Dieses Projekt ist ein Top-Down RPG-Prototyp in Unreal Engine. Er kombiniert grundlegende RPG-Mechaniken (wie Levelsystem und Kampfsystem) mit visuellen Highlights (Shader-Effekte, dynamische Beleuchtung, Interaktions-Feedback).

---

# Table of Contents

1. [Zusammenfassung (High Concept)](#1-zusammenfassung-high-concept)
2. [Zielsetzungen](#2-zielsetzungen)
3. [Gameplay-Elemente](#3-gameplay-elemente)
   1. [Charaktersteuerung](#31-charaktersteuerung-top-down-c)
   2. [Levelsystem](#32-levelsystem-c)
   3. [Achievements](#33-achievements-bonus-feature)
4. [Tech-Art-Features (Phase 2)](#4-tech-art-features-phase-2)
   1. [Shader-basierte Effekte](#41-shader-basierte-effekte)
   2. [Dynamische Umgebung & Mini-Rätsel](#42-dynamische-umgebung--mini-rätsel)
   3. [Visuelle Effekte für Status-Änderungen](#43-visuelle-effekte-für-status-änderungen)
5. [Weitere Ideen (Phase 3)](#5-ausblick-weitere-ideen-phase-3)
   1. [Status-Effekte (Buffs/Debuffs)](#51-status-effekte-buffsdebuffs)
   2. [Kampfsystem & Schadensberechnung (C++)](#52-kampfsystem--schadensberechnung-c)
6. [Technik & Implementierungsdetails](#6-technik-implementierungsdetails)
   1. [Engine & Tools](#61-engine--tools)
   2. [Art & Assets](#62-art--assets)
7. [Projektorganisation & Roadmap](#7-projektorganisation-roadmap)
8. [Risiken & Herausforderungen](#8-risiken-herausforderungen)
9. [Anhang & Weiteres](#9-anhang-weiteres)

---

<a id="1-zusammenfassung-high-concept"></a>
## 1. Zusammenfassung (High Concept)

- **Ziel:** Ein Top-Down RPG-Prototyp in Unreal, der sowohl klassische RPG-Mechaniken als auch fortschrittliche Tech-Art-Features demonstriert.
- **Fokus:** Integration von grundlegenden Gameplay-Systemen und beeindruckenden visuellen Effekten.

---

<a id="2-zielsetzungen"></a>
## 2. Zielsetzungen

- **Spielerlebnis:**  
  Ein kurzer, aber durchdachter RPG-Loop (Erkunden, Rätsel lösen, Kämpfen, Leveln) kombiniert mit beeindruckenden Tech-Art-Elementen.

- **Technische Demonstration:**  
  Nutzung von C++ in Unreal Engine für:
    - Charaktersteuerung
    - Levelsystem
    - Kampfsystem

- **Visuelle Demonstration:**  
  Einsatz fortgeschrittener Shader- und VFX-Techniken zur Hervorhebung von:
    - Umgebung
    - UI
    - Spezialeffekten

- **Erweiterbarkeit:**  
  Klare Trennung von Kernsystemen und Art-Assets, um zukünftige Erweiterungen (z. B. Buffs/Debuffs, komplexere Rätsel) zu ermöglichen.

---

<a id="3-gameplay-elemente"></a>
## 3. Gameplay-Elemente

<a id="31-charaktersteuerung-top-down-c"></a>
### 3.1 Charaktersteuerung (Top-Down, C++)

- **Bewegung:**
    - Top-Down-Perspektive mit WASD/Tastatureingabe oder Controller.
    - Fließende Übergänge (Animationen + Kollisionsabfrage).

- **Interaktion:**
    - Kontextsensitives Interaktionssystem zur Ansprache von Objekten oder Schaltern.
    - Rätsel-Trigger, z. B. für das Öffnen einer Tür.

<a id="32-levelsystem-c"></a>
### 3.2 Levelsystem (C++)

- **Erfahrungspunkte (XP):**
    - XP für erfolgreich abgeschlossene Rätsel und besiegte Gegner.
    - Automatisches Aufleveln oder Skillwahl beim Erreichen bestimmter Schwellenwerte.

- **Stat-Verbesserungen:**
    - Erhöhung von Lebenspunkten, Angriffsstärke, Ausdauer.
    - Optional: Skillbäume oder Talentpunkte für zukünftige Erweiterungen.

<a id="33-achievements-bonus-feature"></a>
### 3.3 Achievements (Bonus-Feature)

- **Beispiele:**
    - „Löse dein erstes Rätsel!“
    - „Besiege 10 Gegner!“

- **Integration:**
    - Fortschritt speicherbar (z. B. über SaveGame).
    - UI-Elemente zur Benachrichtigung bei Freischaltung.

---

<a id="4-tech-art-features-phase-2"></a>
## 4. Tech-Art-Features (Phase 2)

<a id="41-shader-basierte-effekte"></a>
### 4.1 Shader-basierte Effekte

- **Fähigkeits-Effekte:**
    - Partikel- oder Post-Processing-Effekte bei Zaubern und Spezialangriffen.
    - Visuelles Feedback, z. B. bei Heilung, Buffs oder Verwundungen.

- **UI-Effekte:**
    - Dynamische Shader für Healthbars, Skill-Cooldowns und Level-Up-Anzeigen.
    - Animierte Übergänge (Pulse- oder Glow-Effekte).

<a id="42-dynamische-umgebung--mini-rätsel"></a>
### 4.2 Dynamische Umgebung & Mini-Rätsel

- **Licht- & Schattenrätsel:**
    - Beleuchtungswechsel durch Schalter, die Schatten in spezifische Bereiche lenken.
    - Shader als Hinweisgeber (z. B. leuchtende Fußspuren).

- **Türmechaniken mit Schaltern:**
    - Schalter, die Türen öffnen/schließen oder Fallen aktivieren.
    - Visuelles Feedback, wie Leuchten der Türen oder Materialwechsel.

<a id="43-visuelle-effekte-für-status-änderungen"></a>
### 4.3 Visuelle Effekte für Status-Änderungen

- **Level-Up:**
    - Glühender Outline-Effekt oder Partikelemission um den Charakter.
    - Kurze Sequenz oder Zeitlupe als optisches Highlight.

- **Magische Interaktionen:**
    - Darstellung mittels Kreisen, Runen oder fließenden Partikeln.
    - Materialveränderungen (z. B. durchsichtig werdender Stein mit Symbolen).

---

<a id="5-ausblick-weitere-ideen-phase-3"></a>
## 5. Ausblick: Weitere Ideen (Phase 3)

<a id="51-status-effekte-buffsdebuffs"></a>
### 5.1 Status-Effekte (Buffs/Debuffs)

- **Basis-System:**
    - C++-Klasse zur Verwaltung zeitlich begrenzter Effekte (z. B. +10% Schaden, -20% Bewegung).
    - Effekte können stapelbar oder exklusiv sein (bestimmte Debuffs schließen andere aus).

- **Visuelles Feedback:**
    - Farbige Umrandung der Charakter-UI oder Partikeleffekte.
    - Symbol-Overlays im HUD (z. B. Flammensymbol für Feuerschaden).

<a id="52-kampfsystem--schadensberechnung-c"></a>
### 5.2 Kampfsystem & Schadensberechnung (C++)

- **Melee & Ranged Attacken:**
    - Umsetzung mit physikalischer Kollision oder Trace-Abfragen.
    - Trefferfeedback, z. B. Bildschirm-Blinken oder Gegnerreaktion.

- **Skalierbarer Schaden:**
    - Formel: Basis-Schaden + ([Stärke/Intelligenz] * Faktor).
    - Berücksichtigung von Rüstung und Resistenzen.

- **Animationen:**
    - Separate States für Idle, Angriff, Treffer und Tod.
    - Anbindung über Animation Blueprints in Unreal.

---

<a id="6-technik-implementierungsdetails"></a>
## 6. Technik & Implementierungsdetails

<a id="61-engine--tools"></a>
### 6.1 Engine & Tools

- **Engine:**  
  Unreal Engine (Version nach Bedarf, z. B. 5.x)

- **Kernfunktionen in C++:**
    - Charakterklassen (z. B. `ACharacter` oder `Pawn`)
    - Gameplay-Systeme (z. B. `UGameplayStatics` für Rätsel-Trigger)

- **Blueprints:**  
  Für schnelle Iteration von Prototyp-Funktionen und visuellen Effekten.

- **Version Control:**  
  Git oder Perforce für die Zusammenarbeit.

<a id="62-art--assets"></a>
### 6.2 Art & Assets

- **3D-Modelle:**  
  Platzhalter-Modelle zum Testen; spätere Anpassung mit finalen Assets.

- **Shader:**  
  Komplexe Materialien und Post-Processing-Volumes für spezielle Rätsel.

- **UI:**  
  Minimalistisches, aber anpassbares Interface (z. B. Healthbar, EXP-Leiste, Achievements).

<a id="1-zusammenfassung-high-concept"></a>
### 6.3 Audio (Optional erweiterbar)

- **Soundeffekte:**  
  Für Angriffe, UI-Bestätigungen und Rätsel-Feedback.

- **Musik:**  
  Stimmungsvolle Hintergrundmusik für Erforschung und Kampf.

---

<a id="7-projektorganisation-roadmap"></a>
## 7. Projektorganisation & Roadmap

- **Phase 1: Core Gameplay**
    - Implementierung der Charaktersteuerung & des Interaktionssystems (C++).
    - Aufbau des Levelsystems mit einfachem XP-/Stat-Handling.
    - Optional: Achievements bei verfügbarer Zeit.

- **Phase 2: Tech Art**
    - Implementierung von Shader-Effekten (Fähigkeiten, Umgebungshinweise, UI-Effekte).
    - Aufbau dynamischer Licht- und Schattensysteme für Rätsel.
    - Umsetzung visueller Effekte (Level-Up, Statusänderungen).

- **Phase 3: Erweiterung**
    - Einführung von Status-Effekten (Buffs/Debuffs).
    - Erweiterung des Kampfsystems und der Schadensberechnung.
    - Weitere Rätselmechaniken und Umgebungsreaktionen.

---

<a id="8-risiken-herausforderungen"></a>
## 8. Risiken & Herausforderungen

- **Performance:**  
  Shader- und Partikeleffekte können ressourcenintensiv sein – Optimierung ist notwendig.

- **Komplexität:**  
  Zu viele parallele Systeme können die Entwicklung verzögern – Fokus auf Kernfeatures.

- **Scope-Creep:**  
  Klare Abgrenzung der Features je Phase, um den Projektumfang zu kontrollieren.

---

<a id="9-anhang-weiteres"></a>
## 9. Anhang & Weiteres

- **Dokumentation:**  
  Regelmäßige Updates im Wiki/README (z. B. zu neuen Assets und Code-Änderungen).

- **Playtests:**  
  Interne Tests nach jeder Phase zur Sammlung von Feedback.

- **Zielgruppe:**  
  Primär ein Showcase-/Demoprojekt, das dennoch kurzweiligen Spielspaß bietet.

> *Dieses Dokument dient als grobe Struktur. Spezielle Details (wie Story-Elemente, einzigartige Rätselideen, Buff-Typen etc.) können nach Bedarf ergänzt oder angepasst werden, sobald erste Prototyp-Tests abgeschlossen sind.*