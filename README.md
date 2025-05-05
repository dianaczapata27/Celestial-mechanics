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

### 3. Virial Theorem in the Sun–Jupiter–Saturn System

This project explores the validity of the virial theorem in a simplified Solar System model consisting of the Sun, Jupiter, and Saturn. I computed the kinetic, potential, and total energy over 100 years, evaluated the virial expression, and checked whether the relation

$$
\langle U \rangle = -2 \langle K \rangle
$$

holds true within numerical accuracy. The results confirm that the system behaves as expected for a bound system.

View notebook: [`virial_theorem_solar_system.ipynb`](virial_theorem_solar_system.ipynb)

### 4. Planetary Animation: Halley's Comet Return (1986–2061)

In this project, I recreated a planetary animation showing the Solar System bodies and Halley's Comet from February 2, 1986 to July 28, 2061.

The goal was to generate an animation as close as possible to a reference GIF, using accurate planetary data from `Astroquery` and time steps that avoid exact multiples of 24 hours or 60 minutes (32538 minutes ≈ 22.59 days), in order to vary hours and minutes across frames. The dates were displayed using the full month name for visual clarity.

To make the animation resemble the reference GIF, we rotated the coordinate system by 90° using:

$$
x' = x \cos\theta - y \sin\theta \\
y' = x \sin\theta + y \cos\theta
$$

which simplifies to:

$$
x' = -y \\
y' = x
$$

Therefore, we plotted $-y$ on the x-axis and $x$ on the y-axis.

View notebook: [`halley_orbit_animation.ipynb`](halley_orbit_animation.ipynb)  
![Halley's Comet Animation](anim.gif)


