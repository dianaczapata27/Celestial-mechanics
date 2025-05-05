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

View notebook: [`halley_orbit_animation.ipynb`](halley_orbit_animation.ipynb)  
View aniamtion: ![Halley's Comet Animation](anim.gif)

### 5. Two-Body Problem Verification

In this project, we verify that many of the theoretical results from the two-body problem hold for real celestial systems in the Solar System. We focused on the Earth–Moon system.

We retrieved the positions and velocities of the Earth and Moon from the [JPL Horizons system](https://ssd.jpl.nasa.gov/horizons/) over a span of 3 months, corresponding to approximately three orbital periods of the Moon. Using this data, we:

- Computed the specific relative angular momentum vector $$\vec{h} = \vec{r} \times \dot{\vec{r}}$$.
- Computed the specific relative energy $$\epsilon = \frac{1}{2} \dot{\vec{r}}^2 - \frac{\mu}{r}$$.
- Computed the Laplace–Runge–Lenz vector $$\vec{e} = \frac{\dot{\vec{r}} \times \vec{h}}{\mu} - \frac{\vec{r}}{r}$$.
- Verified that these quantities remain approximately constant over time.

We also calculated the average values of these quantities to derive the orbital parameters of the relative motion:

- Eccentricity: $$e = \sqrt{1 + \frac{2 \epsilon h^2}{\mu^2}}$$
- Semilatus rectum: $$p = \frac{h^2}{\mu}$$
- Semi-major axis: $$a = -\frac{\mu}{2\epsilon}$$

Then, using Astroquery, we compared our results with the orbital elements provided by JPL Horizons for:

- The Moon around the Earth–Moon barycenter.
- The Earth around the same barycenter.

I found that the theoretical predictions closely match the observed orbital parameters.

View notebook: [`two_body_problem_earth_moon.ipynb`](two_body_problem_earth_moon.ipynb)

