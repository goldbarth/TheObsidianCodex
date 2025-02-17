# Top-Down RPG Prototype

This project aims to create a Top-Down RPG prototype in Unreal Engine. It focuses on both core RPG mechanics (such as a leveling and combat system) and visual highlights (shader effects, dynamic lighting, interactive feedback).

---

# Table of Contents

1. [Summary (High Concept)](#1-summary-high-concept)
2. [Objectives](#2-objectives)
3. [Gameplay Elements](#3-gameplay-elements)
    1. [Character Controls (Top-Down, C++)](#31-character-controls-top-down-c)
    2. [Level System (C++)](#32-level-system-c)
    3. [Achievements (Bonus Feature)](#33-achievements-bonus-feature)
4. [Tech-Art Features (Phase 2)](#4-tech-art-features-phase-2)
    1. [Shader-Based Effects](#41-shader-based-effects)
    2. [Dynamic Environment & Mini-Puzzles](#42-dynamic-environment--mini-puzzles)
    3. [Visual Effects for Status Changes](#43-visual-effects-for-status-changes)
5. [Future Ideas (Phase 3)](#5-future-ideas-phase-3)
    1. [Status Effects (Buffs/Debuffs)](#51-status-effects-buffsdebuffs)
    2. [Combat System & Damage Calculation (C++)](#52-combat-system--damage-calculation-c)
6. [Technical & Implementation Details](#6-technical--implementation-details)
    1. [Engine & Tools](#61-engine--tools)
    2. [Art & Assets](#62-art--assets)
    3. [Audio (Optional Extension)](#63-audio-optional-extension)
7. [Project Organization & Roadmap](#7-project-organization--roadmap)
8. [Risks & Challenges](#8-risks--challenges)
9. [Appendix & Additional Notes](#9-appendix--additional-notes)

---

## 1. Summary (High Concept)

- **Goal:**  
  Create a Top-Down RPG prototype in Unreal Engine that demonstrates both fundamental RPG mechanics and impressive tech-art features.

- **Focus:**  
  Integration of core gameplay systems with cutting-edge visual effects.

---

## 2. Objectives

- **Player Experience:**  
  A concise, well-designed RPG loop (exploration, puzzle solving, combat, leveling) enriched with eye-catching tech-art elements.

- **Technical Demonstration:**  
  Use C++ in Unreal for:
    - Character controls
    - Leveling system
    - Combat mechanics

- **Visual Demonstration:**  
  Utilize advanced shader and VFX techniques to enhance:
    - Environment
    - UI
    - Special effects

- **Extensibility:**  
  Maintain a clear separation between core systems and art assets, allowing for the easy addition of further features (e.g., buffs/debuffs, more complex puzzles).

---

## 3. Gameplay Elements

<a id="">31-character-controls-top-down-c</a>
### 3.1 Character Controls (Top-Down, C++)

- **Movement:**
    - Top-down perspective with WASD/keyboard or controller input.
    - Smooth transitions with animations and collision checks.

- **Interaction:**
    - Context-sensitive interaction system for objects and triggers.
    - Puzzle triggers, such as mechanisms for opening doors.

### 3.2 Level System (C++)

- **Experience Points (XP):**
    - Earn XP by completing puzzles and defeating enemies.
    - Automatic level-up or skill choice upon reaching XP thresholds.

- **Stat Improvements:**
    - Increases in health points, attack power, stamina, etc.
    - Optional skill tree or talent points for future expansion.

### 3.3 Achievements (Bonus Feature)

- **Examples:**
    - “Complete your first puzzle!”
    - “Defeat 10 enemies!”

- **Integration:**
    - Save progress (e.g., in a SaveGame file).
    - UI elements to display achievement notifications.

---

## 4. Tech-Art Features (Phase 2)

### 4.1 Shader-Based Effects

- **Ability Effects:**
    - Particle or post-processing effects for spells and special attacks.
    - Visual cues for healing, buffs, or damage states.

- **UI Effects:**
    - Dynamic shaders for health bars, skill cooldowns, or level-up screens.
    - Animated transitions (e.g., pulsing or glow effects).

### 4.2 Dynamic Environment & Mini-Puzzles

- **Light & Shadow Puzzles:**
    - Switch-based light changes that cast shadows into specific areas.
    - Shader hints (e.g., glowing footprints) to guide the player.

- **Door Mechanisms with Switches:**
    - Switches that open/close doors or activate traps.
    - Visual feedback such as doors glowing or changing material.

### 4.3 Visual Effects for Status Changes

- **Level-Up:**
    - Glowing outline effect or particle burst around the character.
    - A short sequence or slow-motion moment during level-up.

- **Magical Interactions:**
    - Runes, circles, or flowing particles when activating objects.
    - Material changes (e.g., turning solid stone transparent to reveal symbols).

---

## 5. Future Ideas (Phase 3)

### 5.1 Status Effects (Buffs/Debuffs)

- **Base System:**
    - C++ class managing time-limited effects (e.g., +10% damage, -20% movement).
    - Effects that are either stackable or exclusive (e.g., certain debuffs block others).

- **Visual Feedback:**
    - Colored outlines or particle effects on the character.
    - HUD overlay icons (e.g., a small flame icon for fire damage).

### 5.2 Combat System & Damage Calculation (C++)

- **Melee & Ranged Attacks:**
    - Implementation using physical collision or trace checks.
    - Hit feedback, such as screen flashes or enemy recoil.

- **Scalable Damage:**
    - Formula: Base Damage + ([Strength/Intelligence] * multiplier).
    - Consideration of armor or resistances for enemies.

- **Animations:**
    - Separate states for idle, attack, hit reaction, and death.
    - Linked via Animation Blueprints in Unreal.

---

## 6. Technical & Implementation Details

### 6.1 Engine & Tools

- **Engine:**  
  Unreal Engine (e.g., version 5.x)

- **Core Functionality in C++:**
    - Character Classes (e.g., `ACharacter` or `Pawn`)
    - Gameplay Systems (e.g., `UGameplayStatics` for puzzle triggers)

- **Blueprints:**  
  For rapid prototyping and visual effects.

- **Version Control:**  
  Git or Perforce for team collaboration.

### 6.2 Art & Assets

- **3D Models:**  
  Placeholder models for testing; final assets can be swapped later.

- **Shaders:**  
  Complex materials and post-processing volumes for unique puzzle elements.

- **UI:**  
  A minimalistic but customizable interface (e.g., health bar, XP bar, achievements).

### 6.3 Audio (Optional Extension)

- **Sound Effects:**  
  For combat, UI confirmations, and puzzle feedback.

- **Music:**  
  Atmospheric background tracks for exploration and combat.

---

## 7. Project Organization & Roadmap

- **Phase 1: Core Gameplay**
    - Character control and interaction system (C++).
    - Level system with basic XP/stat handling.
    - Achievements (optional, if time allows).

- **Phase 2: Tech Art**
    - Implementation of shader effects (abilities, environmental hints, UI effects).
    - Dynamic light/shadow puzzles.
    - Visual effects for level-up and status changes.

- **Phase 3: Expansion**
    - Status effects (buffs/debuffs).
    - Combat system and damage calculation.
    - Additional puzzle mechanics and environment reactions.

---

## 8. Risks & Challenges

- **Performance:**  
  Shader and particle effects can be resource-intensive and may require optimization.

- **Complexity:**  
  Too many parallel systems could slow development—focus on core features first.

- **Scope Creep:**  
  It’s important to clearly define which features belong in each phase.

---

## 9. Appendix & Additional Notes

- **Documentation:**  
  Regularly update the Wiki/README (e.g., for assets and code changes).

- **Playtests:**  
  Conduct internal tests after each phase to gather feedback on core gameplay.

- **Target Audience:**  
  Primarily a showcase/demo project that still offers engaging, short-term fun.

> *This document serves as a framework. Specific details (e.g., story elements, unique puzzle concepts, buff types) can be added or modified once initial prototype tests are completed.*
