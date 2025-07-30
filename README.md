# Understanding SR Latches: From Basic to Clocked Versions

![Status](https://img.shields.io/badge/status-active-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Platform](https://img.shields.io/badge/platform-Proteus-blue)

This repository contains media resources such as circuit diagrams, truth tables, and simulation GIFs for understanding **SR Latches**, including the **Basic**, **Gated**, and **Clocked** versions. These are foundational components in digital electronics, widely used in memory circuits and sequential logic.

---

## 🧠 Overview

The **SR Latch (Set-Reset Latch)** is one of the earliest memory elements introduced in digital logic. It forms the base of most sequential circuits and is often used in flip-flops and memory storage applications. Variants such as the **Gated SR Latch** and **Clocked SR Latch** provide enhanced control using enable and clock signals.

Originally implemented using NOR or NAND gates, the SR latch can store binary data and is capable of maintaining its state based on input conditions.

---

## 🔌 Inputs and Outputs

- **Inputs**:
  - `S` (Set)
  - `R` (Reset)
  - `EN` (Enable) *(Gated Latch only)*
  - `CLK` (Clock) *(Clocked Latch only)*

- **Outputs**:
  - `Q` (Normal output)
  - `Q̅` (Inverted output)

---

## 📊 SR Latch Truth Table

| S | R | Q (Next State)       | Description      |
|---|---|----------------------|------------------|
| 0 | 0 | Last State           | Hold             |
| 0 | 1 | 0                    | Set              |
| 1 | 0 | 1                    | Reset            |
| 1 | 1 | Unpredictable        | Forbidden State  |

> ⚠️ The (1,1) condition leads to undefined behavior and should be avoided.

---

## 📚 SR Latch Variants

### 🔹 Basic SR Latch

- Built using **NOR** or **NAND** gates.
- Outputs change based on `S` and `R` input levels.
- Commonly used in early memory and control circuits.

![SR Latch Symbol & Truth Table]

---

### 🔹 Gated SR Latch

- Adds an **Enable (EN)** input for control.
- Only allows state changes when `EN = 1`.
- Helps synchronize state changes in larger systems.

---

### 🔹 Clocked SR Latch (SR Flip-Flop)

- Replaces Enable with a **Clock (CLK)** input.
- Outputs change on **clock edges** only.
- Functions as a basic **synchronous flip-flop**.

---

## 📽️ Simulations Included

This repo includes working simulation **GIFs** for all versions of the SR Latch, created using **P**
