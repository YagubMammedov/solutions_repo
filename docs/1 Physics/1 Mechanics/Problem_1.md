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