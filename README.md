# BioSimHub

## 🧬 Overview
**BioSimHub** is a modular, open-source framework designed for simulating multicellular biological systems. It enables developmental biology simulations through dynamic cell states, lineage trees, and bioelectric or signaling fields. Designed with extensibility and open science in mind, BioSimHub serves as both an educational and research-grade toolkit for computational biology.

---

## 🚀 Features
- 📈 **Dynamic Simulation Engine** for multicellular interactions
- 🌱 **Cell State Modeling** based on position, lineage, and signaling
- 🧠 **Bioelectric/Signal Field Integration**
- 🧬 **Lineage Tree Modeling** with customizable rules
- 📊 **Built-in Visualization Support**
- 📁 **Modular Structure** for easy expansion and research integration

---

## 📂 Directory Structure
```
BioSimHub/
├── pyproject.toml                # Poetry-based Python packaging
├── README.md                     # Project overview
├── src/
│   └── biosimhub/
│       ├── __init__.py           # Module initializer
│       ├── engine.py             # Main simulation loop
│       ├── cell.py               # Cell agent definitions
│       ├── field.py              # Bioelectric/signal field simulator
│       ├── lineage.py            # Placeholder for lineage trees
│       └── utils.py              # Utility functions
├── notebooks/
│   └── demo_lineage_diffusion.ipynb   # Example notebook
├── tests/
│   └── test_engine.py           # Unit tests
├── .github/
│   └── workflows/
│       └── ci.yml               # GitHub Actions CI config
├── .pre-commit-config.yaml      # Pre-commit hooks (e.g., Black, Flake8)
├── Dockerfile                   # Reproducible Docker environment
└── docker-compose.yml           # Multi-container orchestration
```

---

## 🔧 Installation
### Option 1: Clone & Install via Poetry
```bash
git clone https://github.com/yourname/BioSimHub.git
cd BioSimHub
poetry install
```

### Option 2: Using Docker
```bash
docker-compose up --build
```

---

## 📈 Example: Simulating Differentiation in a Lineage
Launch the Jupyter notebook:
```bash
poetry run jupyter notebook notebooks/demo_lineage_diffusion.ipynb
```
Or view an animated signal field:
```python
from biosimhub.engine import SimulationEngine
from biosimhub.cell import Cell
from biosimhub.field import SignalField

cells = [Cell(id=i, state=1.0, position=(i, i)) for i in range(10)]
field = SignalField((20, 20))
sim = SimulationEngine(cells, field)

for _ in range(10):
    sim.step()
```

---

## 🧱 Dependencies
Core:
- `numpy`, `scipy`, `pandas`, `matplotlib`, `networkx`

Optional (for GUI or speed):
- `streamlit`, `jax`, `numba`, `panel`

---

## 🔬 Use Cases
- Simulate lineage tree differentiation with dynamic field feedback
- Explore how bioelectric fields influence developmental patterning
- Model fusion and syncytial dynamics with customizable agents
- Serve as a backend for educational or research visualization tools

---

## 📚 Future Plans
- [ ] Add support for SBML model import/export
- [ ] GUI with Streamlit or PyQt
- [ ] Plugin system for external biological models
- [ ] Integration with `celegans`, `bioelectric-differentiation`, etc.

---

## 🤝 Contributing
1. Fork the repo
2. Create your feature branch: `git checkout -b feature/YourFeature`
3. Commit your changes: `git commit -m 'Add feature'`
4. Push to the branch: `git push origin feature/YourFeature`
5. Open a pull request

All contributions welcome — from simulation models to docs!

---

## 📄 License
[MIT License](LICENSE)

---

## 🌐 Citation / Acknowledgments
If you use this in your work, please cite the GitHub repository and consider linking to any associated publications (to be added).

BioSimHub is part of a broader open science initiative exploring developmental biology, biophysics, and computational modeling.

