# Task 1: Theoretical Foundation

## 1.1 Equations of Motion for Projectile Motion

The governing equations of motion for a projectile are derived from the basic principles of physics: *Newton's Laws of Motion* and the *equations of constant acceleration*. We will assume there is no air resistance in this idealized scenario.

### Horizontal Motion:

$$
x(t) = v_0 \cdot \cos(\theta) \cdot t
$$

where:
- $x(t)$ is the horizontal position at time $t$,
- $v_0$ is the initial velocity,
- $\theta$ is the angle of projection,
- $t$ is the time.

### Vertical Motion:

$$
y(t) = v_0 \cdot \sin(\theta) \cdot t - \frac{1}{2} g t^2
$$

where:
- $y(t)$ is the vertical position at time $t$,
- $g$ is the acceleration due to gravity ($9.81 \, \text{m/s}^2$).

These two equations describe the horizontal and vertical positions of the projectile at any given time $t$.

---

## 1.2 Time of Flight

The time of flight is the total time the projectile remains in the air before it hits the ground. To find this, we set the vertical position equal to zero at the time of impact:

$$
y(t_f) = 0
$$

Substitute the vertical motion equation:

$$
v_0 \sin(\theta) \cdot t_f - \frac{1}{2} g t_f^2 = 0
$$

Factoring out $t_f$:

$$
t_f \left( v_0 \sin(\theta) - \frac{1}{2} g t_f \right) = 0
$$

Solving for $t_f$ (ignoring the trivial solution $t_f = 0$):

$$
t_f = \frac{2 v_0 \sin(\theta)}{g}
$$

Thus, the time of flight depends on the initial velocity $v_0$ and the angle of projection $\theta$.

---

## 1.3 Range of the Projectile

The range $R$ is the horizontal distance the projectile travels before hitting the ground. It is given by the horizontal motion equation at the time of flight $t_f$:

$$
R = x(t_f) = v_0 \cdot \cos(\theta) \cdot t_f
$$

Substitute the time of flight $t_f = \frac{2 v_0 \sin(\theta)}{g}$ into the equation for range:

$$
R = v_0 \cdot \cos(\theta) \cdot \frac{2 v_0 \sin(\theta)}{g}
$$

Simplifying:

$$
R = \frac{v_0^2 \sin(2\theta)}{g}
$$

This is the formula for the range of a projectile.

---

## 1.4 Family of Solutions Based on Initial Conditions

The range $R$ depends on two variables: the initial velocity $v_0$ and the angle of projection $\theta$.

- *Effect of Initial Velocity $v_0$*: 
  - A higher initial velocity increases the range.
  
- *Effect of Angle of Projection $\theta$*:
  - The range $R$ is a function of $\sin(2\theta)$. Therefore, the range will be maximized when $\theta = 45^\circ$, since $\sin(90^\circ) = 1$.

By varying the initial velocity or launch angle, we obtain a family of solutions describing the projectile's behavior.



# Task 1.2 Analysis of the Range

## Introduction
In projectile motion, the horizontal range \( R \) is the distance a projectile travels before hitting the ground. It depends on the angle of projection \( \theta \), the initial velocity \( v_0 \), and the gravitational acceleration \( g \). This task investigates how the range varies with the angle of projection and how other parameters influence this relationship.

## Governing Equations
The horizontal range \( R \) of a projectile launched at an angle \( \theta \) with initial velocity \( v_0 \) is given by:
$$
R = \frac{v_0^2 \sin(2\theta)}{g}
$$
This equation assumes:
- No air resistance.
- A flat, horizontal surface.
- Constant gravitational acceleration \( g \).

## Python Script for Simulation
Below is a Python script to simulate the range as a function of the angle of projection and visualize the results.

```python
import numpy as np
import matplotlib.pyplot as plt

# Constants
g = 9.81  # Gravitational acceleration (m/s^2)
v0 = 50   # Initial velocity (m/s)

# Function to calculate range
def calculate_range(theta, v0, g):
    theta_rad = np.radians(theta)  # Convert angle to radians
    return (v0**2 * np.sin(2 * theta_rad)) / g

# Generate angles from 0 to 90 degrees
angles = np.linspace(0, 90, 100)
ranges = calculate_range(angles, v0, g)

# Plotting
plt.figure(figsize=(10, 6))
plt.plot(angles, ranges, label=f"v0 = {v0} m/s, g = {g} m/s²")
plt.title("Range vs Angle of Projection")
plt.xlabel("Angle of Projection (degrees)")
plt.ylabel("Range (m)")
plt.grid(True)
plt.legend()
plt.show()
```

## Graphical Representation
The graph above shows the range \( R \) as a function of the angle of projection \( \theta \). Key observations:
1. The range is maximum at \( \theta = 45^\circ \).
2. The range is symmetric around \( 45^\circ \).
3. For angles \( \theta < 45^\circ \) and \( \theta > 45^\circ \), the range decreases.

## Influence of Parameters
1. **Initial Velocity \( v_0 \):**
   - Increasing \( v_0 \) increases the range quadratically, as \( R \propto v_0^2 \).
   - Decreasing \( v_0 \) reduces the range.

2. **Gravitational Acceleration \( g \):**
   - Increasing \( g \) decreases the range, as \( R \propto \frac{1}{g} \).
   - Decreasing \( g \) increases the range.

