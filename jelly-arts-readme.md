# Jelly Arts - Jellycraft Juggernauts

## Overview
Jelly Arts define the **unique abilities and attacks** available to Juggernauts in *Jellycraft Juggernauts*. These abilities dictate how a Juggernaut interacts in battle, whether through direct attacks, healing, status infliction, or environmental manipulation. Each Jelly Art can evolve through **Jellymancy**, allowing players to customize and enhance their Juggernaut’s abilities.

## JSON Structure
Each Jelly Art follows a structured format:

- **`id`** *(string)* – Unique identifier for the Jelly Art.
- **`name`** *(string)* – The name of the Jelly Art.
- **`target`** *(string)* – Determines the targeting type (e.g., `Ranged`, `Touch`, `Self`, `Ambient`).
- **`damage`** *(integer)* – The amount of damage inflicted by the Jelly Art.
- **`status-effect`** *(string or null)* – The associated status effect applied by this ability (e.g., `Burn`, `Stun`, `Poison`).
- **`status-X-value`** *(integer or null)* – If applicable, represents the variable strength of the status effect (e.g., `Burn(1)`).
- **`lifesteal`** *(integer or null)* – Amount of health absorbed by the user when dealing damage.
- **`tier`** *(integer)* – Represents the evolution level of the Jelly Art (`0` to `3`).
- **`cost`** *(integer)* – The Jelly Jem cost to use this Jelly Art.
- **`jellymancy`** *(array of IDs)* – References to other Jelly Arts that this ability can evolve into.

## Example Entry
```json
{
  "id": "JA016",
  "name": "Absorb",
  "target": "Touch",
  "damage": 2,
  "status-effect": null,
  "lifesteal": 1,
  "tier": 1,
  "cost": 1,
  "jellymancy": ["JA017"]
}
```

## Jellymancy (Evolution System)
Jelly Arts can evolve into stronger versions through **Jellymancy**. Each evolution enhances its previous ability, either by increasing its effectiveness, changing targeting conditions, or adding status effects.

Example Evolution Chain:
- **Absorb (JA016)** → Evolves into **Devour (JA017)**
  - `Devour` deals more damage, applies `Stun`, and has stronger lifesteal.

## Contribution & Expansion
Jelly Arts are designed to be **modular and expandable**. Contributors can add new Jelly Arts while maintaining game balance. When creating new Jelly Arts:
- Ensure they follow the **JSON schema**.
- Maintain **game balance** when adding evolutions.
- Follow the **existing categorization** of attack types.

---
This document is part of the **Jellycraft Juggernauts Open Source Project**. For the latest updates, check the **GitHub repository**.

