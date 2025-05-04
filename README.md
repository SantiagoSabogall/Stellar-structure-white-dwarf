# 🌀 White Dwarf Structure & Gravitational Potential

Numerical simulation of the internal structure of a white dwarf using a relativistic polytropic model. The project computes both the hydrostatic equilibrium profile and the gravitational potential via the Poisson equation.

---

## 📂 Contents

- `white_dwarf_structure.py` – Python script for structure and pressure-mass-radius integration.
- `gravitational_potential.py` – Poisson equation solver using RK4.
- `white_dwarf_theory.md` – Markdown file with full theoretical background.
- `notebook.ipynb` – Jupyter notebook with simulation, visualization and commentary.
- Output plots (density, pressure, mass, potential).

---

## 🧪 Physics Background

This project models a white dwarf assuming:

- A relativistic degenerate electron gas.
- Polytropic index \( \gamma = 4/3 \).
- Central density \( \rho_c = 10^{10} \ \text{g/cm}^3 \).

It solves the following equations:

- Hydrostatic equilibrium:
  
  $$
  \frac{dp}{dr} = -\frac{G M(r) \rho(r)}{r^2}
  $$

- Mass conservation:

  $$
  \frac{dM}{dr} = 4\pi r^2 \rho(r)
  $$

- Equation of state:

  $$
  p = K \rho^\gamma
  $$

- Poisson equation for the potential:

  $$
  \frac{1}{r^2} \frac{d}{dr} \left( r^2 \frac{d\phi}{dr} \right) = 4\pi G \rho(r)
  $$

---

## ⚙️ Methods

- 4th-order Runge-Kutta integration (RK4)
- Interpolation of numerical density for Poisson's equation
- Matching interior and exterior potential at stellar radius
- Unit conversion (cgs → km, kg, solar units)

---

## 📊 Output

- Mass-radius profile
- Pressure and density profiles
- Gravitational potential (interior + exterior)
- Escape energy from the center

---

## 👤 Author

**Santiago Sabogal**  
_Universidad Nacional de Colombia_  


---

## 📄 License

This project is part of a computational astrophysics course (2025-I) and is intended for academic purposes.
# stellar-structure-white-dwarf