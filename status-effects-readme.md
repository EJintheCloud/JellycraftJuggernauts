# Jellycraft Juggernauts - Status Effects

## Overview
This document defines the various **Status Effects** in *Jellycraft Juggernauts*, providing structured mechanics for each effect, its duration, triggers, and resolution method. These effects play a crucial role in battles by modifying Juggernaut behaviors, actions, and vulnerabilities.

## Status Effects Schema
Each status effect is defined with the following attributes:

- **`name`**: The effect’s name.
- **`effect`**: A brief description of how the effect modifies the target's abilities.
- **`X-value`**: A numerical value associated with the effect (if applicable).
- **`X-value-type`**: Defines what the X-value represents (e.g., damage, turns, armor, etc.).
- **`duration-type`**: Specifies how long the effect lasts (`turns`, `rounds`, `trigger`, or `permanent`).
- **`duration-value`**: Specifies the numeric duration of the effect if applicable.
- **`duration-trigger-type`**: Defines a condition under which the effect's duration is modified.
- **`duration-trigger-target`**: Specifies the entity that triggers the duration change.
- **`effect-trigger-type`**: The event that activates the effect.
- **`effect-trigger-target`**: The entity that is affected by the effect-trigger.
- **`conflict-type`**: The resolution method for contested effects (e.g., `Rock-Paper-Scissors`, `Coin Flip`, `None`).

## Status Effects List

### **Burn**
- **Effect**: Increases damage Target takes from all sources.
- **Trigger**: Damage Received
- **Duration**: Permanent
- **Conflict Type**: None

### **Poison**
- **Effect**: Deals damage to Target at the end of their turn.
- **Trigger**: End of Each Turn
- **Duration**: Permanent
- **Conflict Type**: Coin Flip

### **Exhaust**
- **Effect**: Deals damage whenever Target performs an Action.
- **Trigger**: Action Taken
- **Duration**: Permanent
- **Conflict Type**: None

### **Restrain**
- **Effect**: Target cannot use Actions until the Inflictor's next turn.
- **Trigger**: Immediate
- **Duration**: Until Beginning of Next Turn
- **Conflict Type**: Rock-Paper-Scissors

### **Disable**
- **Effect**: Disables the Jelly Arts of a specific Jelly Part attached to Target.
- **Trigger**: Immediate
- **Duration**: Permanent
- **Conflict Type**: None

### **Confuse**
- **Effect**: While under the effect, Target must initiate a Rock-Paper-Scissors conflict with the Inflictor immediately upon declaring an Action. If Target succeeds, the Action continues. Otherwise, the Action fails.
- **Trigger**: Action Taken
- **Duration**: Turns (until resolved)
- **Conflict Type**: Rock-Paper-Scissors

### **Mark**
- **Effect**: Target receives increased damage from Inflictor.
- **Trigger**: Damage Received
- **Duration**: Permanent
- **Conflict Type**: None

### **Weaken**
- **Effect**: Reduces the damage Target deals with all Jelly Arts.
- **Trigger**: Damage Dealt
- **Duration**: Permanent
- **Conflict Type**: None

### **Dilute**
- **Effect**: Disables Target's Jelly Parts.
- **Trigger**: Immediate
- **Duration**: Turns (until resolved)
- **Conflict Type**: None

### **Stun**
- **Effect**: Target must flip a coin after declaring Actions and Reactions. On heads, the Action (or Reaction) fails.
- **Trigger**: Immediate
- **Duration**: Turns (until resolved)
- **Conflict Type**: Coin Flip

## Additional Notes
- **`duration-types`**: The effect's longevity can be **turn-based**, **round-based**, or **trigger-dependent**.
- **`trigger-types`**: Status effects are activated by specific game events such as **damage received, action taken, or reaction taken**.
- **Resolution Methods (`conflict-type`)**:
  - **Rock-Paper-Scissors (RPS)**: Used for competitive interaction.
  - **Coin Flip**: Introduces uncertainty into certain effects.
  - **None**: The effect applies without requiring additional resolution.

---
This document is part of the **Jellycraft Juggernauts Open Source Game Project**. For the latest updates, visit the **GitHub repository**.

