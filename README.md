# Block World Planning with DLV

This repository contains a planning problem for the **Block World** domain, implemented using **DLV**. The goal is to manipulate blocks using logical rules and planning constraints.

## 📌 Overview

The Block World consists of:
- A set of **blocks** (`a`, `b`, `c`).
- A **table** (`mesa`) as the initial resting place for all blocks.
- Actions to **grasp, release, lift, and lower** blocks according to specific conditions.

The objective is to **stack the blocks in a specific order**, following logical constraints.

## 📂 Files

- **`file1.lp`** → Defines blocks and locations.
- **`file2.plan`** → Specifies fluents, actions, and constraints.
- **`file3.plan`** → Sets the initial state and the goal configuration.

## 🛠 Requirements

- **DLV Solver** (Download from: [DLV System](http://www.dlvsystem.com))
- Command-line interface (CLI)

## 🚀 Execution

### 1️⃣ Running the Solver

To solve the planning problem, execute the following command:

```bash
dlv.mingw.exe file1.lp file2.plan file3.plan
```

### 2️⃣ Expected Output

The solver will generate an execution sequence to achieve the goal:

```css
Action: agarrar(a)
Action: subir(a)
Action: bajar(a, b)
...
Goal Reached: sobre(a, b), sobre(b, c), sobre(c, mesa)
```

## 🎯 Goal State

The desired final arrangement of blocks:

<p align= "center">
    <img src="https://github.com/user-attachments/assets/7bc88e7b-6a30-4225-8983-77a06db0ed3d" style="width: 20%; height: auto;">
</p>
