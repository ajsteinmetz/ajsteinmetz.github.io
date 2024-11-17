
---

### **1. Damped and Forced Harmonic Oscillator**
A damped harmonic oscillator is subjected to a sinusoidal driving force. Its equation of motion is:
\[
m\ddot{x} + c\dot{x} + kx = F_0 \cos(\omega t),
\]
where \(m\) is the mass, \(c\) is the damping coefficient, \(k\) is the spring constant, \(F_0\) is the driving force amplitude, and \(\omega\) is the driving frequency.

**Problem:**
1. Solve for the steady-state solution \(x(t)\) of the oscillator.
2. Determine the resonance frequency of the system and discuss how it is affected by the damping coefficient \(c\).
3. Plot the amplitude of the steady-state motion as a function of \(\omega\) for three different damping values (\(c = c_0, c_0/2, c_0/4\)).

---

### **2. Nonlinear Pendulum Dynamics**
The motion of a simple pendulum with length \(L\) and mass \(m\) is governed by:
\[
\ddot{\theta} + \frac{g}{L}\sin\theta = 0.
\]

**Problem:**
1. Using the conservation of energy, show that the angular velocity \(\dot{\theta}\) as a function of \(\theta\) is:
   \[
   \dot{\theta} = \pm \sqrt{\frac{2g}{L} (\cos\theta - \cos\theta_0)},
   \]
   where \(\theta_0\) is the maximum angular displacement.
2. Determine the time period of the motion in terms of an integral and discuss how it differs from the time period of small oscillations.

---

### **3. Critical Damping in Oscillators**
A critically damped oscillator satisfies:
\[
\ddot{x} + 2\beta\dot{x} + \omega_0^2 x = 0, \quad \text{where } \beta = \omega_0.
\]

**Problem:**
1. Solve for \(x(t)\) given the initial conditions \(x(0) = x_0\) and \(\dot{x}(0) = v_0\).
2. Sketch the phase space trajectory (\(x \) vs. \(\dot{x}\)) for the initial conditions \(x_0 = 1, v_0 = 0\).
3. Show that the total energy of the system decreases over time and find its functional form.

---

### **4. Lagrangian of a Spring Pendulum**
Consider a spring pendulum consisting of a mass \(m\) attached to a spring of natural length \(L_0\) and spring constant \(k\). The system is free to oscillate in both radial (\(r\)) and angular (\(\theta\)) directions in a vertical plane under gravity \(g\).

**Problem:**
1. Write the Lagrangian of the system in terms of the generalized coordinates \(r\) (radial distance from the pivot) and \(\theta\) (angular displacement).
2. Derive the equations of motion using the Euler-Lagrange equations.
3. Linearize the equations for small angular and radial oscillations (\(\theta \ll 1\) and \(r \approx L_0\)) and obtain simplified coupled equations of motion.

---

### **5. Nonlinear Oscillation in a Potential Well**
A particle of mass \(m\) moves in a potential \(U(x) = \frac{1}{4}ax^4 - \frac{1}{2}bx^2\), where \(a, b > 0\).

**Problem:**
1. Identify the equilibrium points and determine their stability.
2. Linearize the equation of motion near the stable equilibrium and find the small oscillation frequency.
3. Using energy conservation, determine the maximum displacement \(x_\text{max}\) for an initial velocity \(v_0\) at \(x = 0\).

---

### **6. Pendulum on a Vertically Oscillating Table**
A pendulum of length \(L\) and mass \(m\) is placed on a table oscillating vertically such that the effective gravitational acceleration of the pendulum is \(g(t) = g_0 + a \cos(\alpha t)\), where \(g_0\) is the constant gravitational acceleration, \(a\) is the amplitude of oscillation, and \(\alpha\) is the oscillation frequency.

**Problem:**
1. Write the Lagrangian of the system considering the time-dependent \(g(t)\).
2. Derive the equations of motion for the pendulum using the Euler-Lagrange equations.

---
