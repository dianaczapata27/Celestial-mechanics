# Celestial Mechanics Projects

This repository contains several computational projects developed during the Celestial Mechanics course. Each project focuses on a different aspect of celestial motion, using tools like Astroquery, NumPy, and Matplotlib for data analysis and visualization.

## List of Projects

### 1. Solar System Orbits

Using `Astroquery` and `Matplotlib`, I created a 3D plot of the orbits of the planets in the Solar System (excluding dwarf planets). The goal was to reproduce as closely as possible the diagram provided by the professor as a reference.

View notebook: [`solar_system_orbits.ipynb`](solar_system_orbits.ipynb)

### 2. Laplace Plane and Conservation Laws

In this project, I used the [SPICE Toolkit](https://naif.jpl.nasa.gov/naif/toolkit.html) to analyze the conservation of energy and angular momentum in the Solar System, as well as the geometry of the invariable Laplace plane over a 100-year span. The analysis included:
- Computing the total energy of the Solar System and comparing it with Jupiter’s kinetic energy.
- Verifying the constancy of total energy over time.
- Calculating the angular momentum vector of the Solar System at two different epochs.
- Measuring the inclination of each planet’s orbital plane with respect to the invariable Laplace plane.

View notebook: [`laplace_plane_and_conservation_laws.ipynb`](laplace_plane_and_conservation_laws.ipynb)
