# 🧭 Vector Nayan — θ-Domain Engine Boundary System  
**Black-Box • Physics-Locked • Configuration-Driven**

> This is a **protected engineering system**, not a code repository.  
> What is exposed is *control and behavior* — not internal physics logic.

---

## 🚦 What this system is

Vector Nayan is a **θ-domain engine behavior system** built for **early-stage validation**  
before CFD, ECU logic, or hardware calibration.

It answers one core engineering question:

> **Is this operating direction physically stable — or already broken?**

This system is intentionally designed as a **black-box execution engine**.

- Physics is **locked**
- Assumptions are **explicit**
- Outputs are **inspectable**
- Calibration is **external and modular**

---

## 🔒 System Protection Model (Important)

| Layer | Status |
|---|---|
| Physics kernel | 🔐 Fully locked |
| Diagnostics logic | 🔐 Fully locked |
| Drift & safety logic | 🔐 Fully locked |
| Execution environment | 🔐 Server-side only |
| User access | ✅ Configuration only |
| Output access | ✅ CSV artifacts |

There is **no partial access**, **no tunable shortcuts**, and **no exposed internals**.

---

## 📦 Repository Contents (Minimal by Design)
vector-nayan-run-config/ ├── run_config.json   ← user-editable engineering contract └── README.md         ← system definition, scope, limits

Nothing else is required.  
No source files.  
No scripts.  
No hidden knobs.

---

## 🎛️ What you can change vs what you cannot

| Category | User Control | System Control |
|---|---|---|
| RPM range | ✅ Yes | ❌ |
| Ignition timing | ✅ Yes | ❌ |
| Cycle count | ✅ Yes | ❌ |
| Engine geometry | ✅ Yes | ❌ |
| Combustion physics | ❌ | ✅ |
| Gas dynamics logic | ❌ | ✅ |
| Diagnostics thresholds | ❌ | ✅ |
| Drift & safe-mode logic | ❌ | ✅ |

➡️ **Configuration is the interface.  
Physics is the authority.**

---

## 🔬 What the system evaluates (Outputs)

| Domain | What you get |
|---|---|
| Combustion | Pressure & temperature trends |
| Stability | Cycle-to-cycle repeatability |
| Diagnostics | Misfire, early-fire, low compression |
| Breathing | VE trends & flow limits |
| Mechanical | Load-induced θ drift |
| Safety | Automatic stabilization response |

All results are delivered as **CSV files** for independent analysis.

---

## 🔁 Calibration Philosophy (Very Important)

This system is **calibration-ready**, not calibration-dependent.

| Aspect | Behavior |
|---|---|
| Default model | Generic petrol engine |
| Calibration | External, plug-and-play |
| Vehicle specific tuning | ✅ Supported |
| Engine family changes | ✅ Supported |
| Architecture changes | ❌ Not required |

Calibration is treated as a **replaceable layer**, not baked logic.

You can adapt the same system to:
- A small commuter engine  
- A performance engine  
- A research prototype  
- Even non-automotive reciprocating systems  

➡️ **The core architecture does not change. Only calibration does.**

---

## ▶️ How execution works

This repository uses a **secure CI-based execution flow**.

### Run steps

1. Edit `run_config.json`
2. Commit & push
3. Open the **Actions** tab
4. Select **Vector Nayan Black Box Run**
5. Click **Run workflow**

After completion:
- 📁 Download the generated **CSV artifacts**
- 📊 Inspect trends, stability, and boundaries

> 🔐 The physics engine executes in a protected environment  
> and is never exposed to the user.

---

## 🧪 Who this system is for

- 🔧 Engine researchers testing cycle behavior  
- 📊 Analysts studying stability & drift  
- 🧪 Engineers exploring operating boundaries  
- 🧱 Teams needing **safe, repeatable early validation**

If you need **certified numbers**, this is not the tool.  
If you need **directional truth**, this is exactly the tool.

---

## ⚠️ What this system will NOT do

- ❌ Replace CFD / GT-Power / ANSYS  
- ❌ Predict certified torque or emissions  
- ❌ Auto-tune engines  
- ❌ Hide uncertainty behind ML  

Boundaries are **shown**, not smoothed.

---

## 🧠 Design Principle (One Line)

> **Configuration is treated as a first-class engineering artifact —  
not a side effect.**

Edit the contract.  
Run the system.  
Trust — and challenge — the physics.

---

## 📌 Status

- ✔ Architecture complete  
- ✔ Validation performed  
- ✔ Outputs reproducible  
- ✔ Calibration extensible  

This is a **research-grade boundary system**,  
not a demo script.
