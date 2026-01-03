# 🚀 Vector Nayan — Run Configuration

A **lightweight, public configuration interface** for the Vector Nayan V44
physics-driven engine simulation system.

This repository does **not** contain any engine code, models, or solvers.  
It provides a **clean, controlled input contract** (`run_config.json`) used by
the Vector Nayan execution system.

---

## 🎯 Why this configuration exists

Modern engine simulation workflows fail not because of physics,
but because of **uncontrolled inputs** and **opaque assumptions**.

Vector Nayan solves this by separating:

- **What users can change** → Configuration  
- **What must remain protected** → Physics kernel  

This repository defines the **only allowed boundary** for user interaction.

---

## 🧠 What this configuration controls

| Category | What user can tune | Why it matters |
|--------|------------------|----------------|
| ⚙️ Operating Range | RPM min / max | Explore low, nominal, and high-speed behavior |
| 🔄 Cycles | Total cycles | Stability, drift, convergence analysis |
| 📐 Geometry | Bore, stroke, conrod | Real engine architecture sensitivity |
| 🧯 Compression | Compression ratio | IMEP, knock margin, efficiency |
| 🔥 Ignition | Start angle | Combustion phasing & misfire zones |
| ♻️ Residuals | Residual fraction | Trapped gas realism |
| ⚡ Efficiency | Combustion efficiency | Load & loss sensitivity |

All values are **explicit, auditable, and deterministic**.

---

## 📊 What makes Vector Nayan robust (comparison)

| Feature | Vector Nayan | Typical Black-Box Tools |
|------|-------------|-------------------------|
| 🔬 Physics-first | ✅ Yes | ❌ Often empirical |
| 🧭 Cycle-aware | ✅ Yes | ❌ Snapshot-based |
| 🧠 Drift detection | ✅ Built-in | ❌ Post-processing |
| ⚠️ Misfire logic | ✅ Physics-aware | ❌ Threshold only |
| 🔒 Kernel safety | ✅ Fully protected | ❌ Often exposed |
| 📄 Input clarity | ✅ JSON contract | ❌ Hidden UI logic |
| 🧪 Reproducibility | ✅ Deterministic | ❌ Version-fragile |

---

## 🧱 Design philosophy

| Principle | Implementation |
|---------|----------------|
| 🔐 Separation of concerns | Config ≠ Kernel |
| 📜 Auditability | Single JSON contract |
| 🧪 Scientific control | Explicit assumptions |
| 🧩 Modularity | Plug-and-run pipeline |
| 🚫 No magic | No hidden defaults |

---

## 📌 Boundary conditions (important)

This configuration **does not**:

- ❌ Modify physics equations  
- ❌ Change combustion models  
- ❌ Alter thermodynamic constants  
- ❌ Bypass safety logic  

All physics remain **authoritative and protected**.

---

## ⚠️ Assumptions (explicit)

| Assumption | Reason |
|----------|--------|
| Single-zone cylinder model | Cycle-level robustness |
| Ideal gas framework | Deterministic behavior |
| Fixed wall temperature | Controlled heat loss |
| No external calibration | Physics-first validation |

These assumptions are **intentional**, not limitations.

---

## 📁 Repository contents
vector-nayan-run-config/ ├── run_config.json   ← user-editable contract └── README.md         ← this document
Copy code

Nothing else is required.

---

## 🧠 Who should use this

- 🔧 Engine researchers validating cycle behavior  
- 📊 Analysts studying IMEP, drift, and stability  
- 🧪 Engineers testing boundary conditions  
- 🧱 Teams needing **safe, repeatable simulations**

---

## ✅ Summary (one line)

> **Vector Nayan treats configuration as a first-class engineering artifact —
not a side effect.**

Edit the contract.  
Run the system.  
Trust the physics.
