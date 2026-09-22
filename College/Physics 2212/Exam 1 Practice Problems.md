> [!abstract] What this document is
> Every practice problem from **Spring 2022 Test 1**, **Spring 2023 Test 1**, **Spring 2024 Test 1**, and **Guided Practice Sets (GPS) 1 & 2**, each with the full problem statement and a complete, step-by-step, neatly typed solution.
>
> - For the three official tests, the solution method follows the released answer key/solutions exactly (so you can see *how you're supposed to solve it*), with every algebraic step filled back in.
> - For GPS 1 and GPS 2 (no official solutions exist), the solutions below were derived independently from first principles, using the same methods and formula sheet as the tests, and cross-checked for self-consistency.
> - All numeric problems use $k = \dfrac{1}{4\pi\epsilon_0} = 9\times10^{9}\ \text{N·m}^2/\text{C}^2$ and $e = 1.6\times10^{-19}\ \text{C}$, matching the official Georgia Tech PHYS 2212 formula sheet.
> - Final answers are **boxed**. Work through each problem yourself first — the value is in the struggle, not the reading.

## Table of Contents
- [[#Part A — Spring 2022 Test 1]]
- [[#Part B — Spring 2023 Test 1]]
- [[#Part C — Spring 2024 Test 1]]
- [[#Part D — GPS 1 (no official key)]]
- [[#Part E — GPS 2 (no official key)]]
- [[#Quick Answer Key]]

---

# Part A — Spring 2022 Test 1

## A1. Problem 1 — Coding: Field and Force of a Moving Ion (20 pts)

> [!question] Problem statement
> The program below calculates the electric field due to a moving positive gold ion and then computes the force this field makes on a proton moving nearby.
> ```python
> ##Constants
> k = 9e9          # Coulomb's constant
> mzofp = 1e-7     # mu_0 over 4pi
> e = 1.6e-19      # charge on a proton in C
> ##Create the ion and electron initial conditions
> gold = sphere(pos=vector(0,0,0), color=color.yellow, radius=1e-10, charge=4*e)
> gold.vel = vector(0,0,1e7)          # gold velocity in m/s
> proton = sphere(pos=vector(0,-1e-9,0), color=color.green, radius=2.5e-11, m=1.67e-27, charge=e)
> proton.vel = (0,3e6,0)              # initial velocity of proton in m/s
> proton.p = (proton.m)*(proton.vel)
> deltat = 1e-15
> t = 0
> while t < deltat*1e6:
>     # 1. [10 pts] electric field from the gold ion at the location of the proton
>     # 2. [5 pts] electric force on the proton
>     # 3. [5 pts] arrow visualizing the electric field at the proton's location
>     proton.p = proton.p + F_net*deltat
>     proton.pos = proton.pos + (proton.p)/(proton.m)*deltat
>     gold.pos = gold.pos + gold.vel*deltat
>     t += deltat
> ```

**Solution.** This is a direct application of the point-charge field formula $\vec E = \dfrac{kq}{r^2}\hat r$, written as vector code: get the separation vector from source to field point, normalize it, then scale by $kq/r^2$.

**1. Electric field due to the gold ion at the proton's location:**
```python
r = proton.pos - gold.pos      # vector FROM the source (gold) TO the field point (proton)
rmag = mag(r)
rhat = norm(r)
E = (k*gold.charge/rmag**2)*rhat
```

**2. Electric force on the proton** (using $\vec F = q\vec E$, with $q$ = the proton's own charge):
```python
F_net = proton.charge*E
```
(The loop refers to this quantity as `F_net`, so it must be named that here.)

**3. Arrow to visualize the field** (positioned at the proton, pointing along $\vec E$; magnitude is automatically encoded in the arrow's length since no `scale` factor is requested):
```python
ef = arrow(pos=proton.pos, axis=E)
```

> [!tip] Why this works
> `mag(r)` and `norm(r)` are VPython built-ins for $|\vec r|$ and $\hat r = \vec r/|\vec r|$. Writing `rmag = sqrt(r.x**2+r.y**2+r.z**2)` and `rhat = r/rmag` instead is completely equivalent and receives full credit — there's no single "correct" line, only a correct *vector*.

$$\boxed{\vec E = \frac{k\,q_{\text{gold}}}{r^2}\hat r,\qquad \vec F = q_{\text{proton}}\vec E}$$

---

## A2. Problem 2 — Dipole Approximation and Superposition (40 pts)

> [!question] Problem statement
> A negative charge $-q$ is at $\vec A = \langle -x_0,0,0\rangle$ and a positive charge $+q$ is at $\vec B = \langle x_0,0,0\rangle$.
> 1. **[15 pts]** Calculate $\vec E_M$ at $M=\langle 0,y_0,0\rangle$ due to the $+q$ charge, the $-q$ charge, and both together. Draw three arrows at $M$.
> 2. **[10 pts]** Under what condition on $x_0,y_0$ can you use the dipole approximation? What is the dipole moment in that limit?
> 3. **[10 pts]** A permanent dipole of moment $p=2qx_0$ is placed at $\vec P = \langle d, y_0, 0\rangle$, $d>0$, with $y_0\gg x_0$. Find $d$ so that the net field magnitude at $M$ is **three times** the value from part 1. Sketch the dipole's orientation.
> 4. **[5 pts]** A particle of mass $m$, charge $2e$, sits at $M$ (with the part-3 dipole now present). Find its initial acceleration.

**Solution.**

**Part 1 — exact superposition.** Both charges are a distance $\sqrt{x_0^2+y_0^2}$ from $M$.

Field point minus source: $\vec r_{-q} = M - A = \langle x_0,y_0,0\rangle$, $\ \vec r_{+q} = M-B=\langle -x_0,y_0,0\rangle$; both have magnitude $r=\sqrt{x_0^2+y_0^2}$.

$$\vec E_{-q} = \frac{k(-q)}{r^3}\langle x_0,y_0,0\rangle,\qquad \vec E_{+q} = \frac{kq}{r^3}\langle -x_0,y_0,0\rangle$$

Adding them, the $y$-components cancel ($-qy_0+qy_0=0$) and the $x$-components double:

$$\boxed{\vec E_M = \frac{kq}{(x_0^2+y_0^2)^{3/2}}\langle -2x_0,\,0,\,0\rangle}$$

The three arrows at $M$: the $-q$ field points **toward** $A$ (down-and-left-ish), the $+q$ field points **away from** $B$ (up-and-left-ish), and their sum points purely in $-\hat x$.

**Part 2 — dipole limit.** The dipole-approximation formulas require the observation distance to be much larger than the charge separation, and here $M$ is on the **perpendicular bisector** of the two charges (equidistant from both, off to the side). The charge separation is $s = 2x_0$ (distance from $-q$ at $-x_0$ to $+q$ at $x_0$), and the perpendicular distance is $y_0$. So the condition is

$$\boxed{y_0 \gg x_0}\qquad\text{(equivalently } y_0\gg s/2\text{, i.e. } r\approx y_0 \gg s)$$

with dipole moment $\boxed{p = qs = 2qx_0}$. Check: in this limit $(x_0^2+y_0^2)^{3/2}\to y_0^3$, and $\vec E_M \to -\dfrac{2kqx_0}{y_0^3}\hat x = -\dfrac{kqs}{y_0^3}\hat x$, matching $|\vec E_{\text{dipole},\perp}| = kqs/r^3$ from the formula sheet. Good.

**Part 3 — placing a second dipole.** We want $|\vec E_{\text{new}}| = 3|\vec E_M|$. Since the new dipole's field superposes on top of $\vec E_M$, and we want the *total* to triple, the new dipole alone must contribute *twice* $\vec E_M$:

$$|\vec E_{\text{dipole}}| = 2|\vec E_M| = 2\cdot\frac{kq(2x_0)}{(x_0^2+y_0^2)^{3/2}} = \frac{4kqx_0}{(x_0^2+y_0^2)^{3/2}}$$

The vector from the new dipole (at $P=\langle d,y_0,0\rangle$) to $M=\langle 0,y_0,0\rangle$ is $\vec r = \langle -d,0,0\rangle$, i.e. purely along $x$ — so if the dipole is oriented **along this same line** (pointing along $\pm\hat x$), then $M$ sits exactly *on-axis* for it, at distance $d$:

$$|\vec E_{\text{dipole,axis}}| = \frac{2kp}{d^3} = \frac{2k(2qx_0)}{d^3} = \frac{4kqx_0}{d^3}$$

Setting the two expressions for $|\vec E_{\text{dipole}}|$ equal:

$$\frac{4kqx_0}{d^3} = \frac{4kqx_0}{(x_0^2+y_0^2)^{3/2}} \;\Longrightarrow\; \boxed{d = \sqrt{x_0^2+y_0^2}}$$

**Orientation:** $\vec E_M$ points in $-\hat x$. For the new on-axis dipole's field to point the *same* way at $M$ (constructive, giving $3\times$ rather than partial cancellation), its dipole moment $\vec p$ must also point in $-\hat x$ — i.e. the same orientation as the original dipole formed by $-q$ at $A$ and $+q$ at $B$ (negative end toward $+x$, positive end toward $-x$). Sketch: at $P$, draw the $+$ charge on the side closer to the $y$-axis (near $x=0$) and the $-$ charge farther out (larger $x$), so $\vec p$ points in $-\hat x$, toward $M$.

**Part 4 — acceleration of a $2e$ charge at $M$.** With the dipole from part 3 now present, the *total* field at $M$ is $3\vec E_M = \dfrac{kq}{(x_0^2+y_0^2)^{3/2}}\langle -6x_0,0,0\rangle$.

$$\vec F = (2e)\big(3\vec E_M\big) = \frac{12ekqx_0}{(x_0^2+y_0^2)^{3/2}}\langle -1,0,0\rangle$$

$$\boxed{\vec a = \frac{\vec F}{m} = -\frac{12\,e\,k\,q\,x_0}{m\,(x_0^2+y_0^2)^{3/2}}\ \hat x}$$

---

## A3. Problem 3 — Induced Dipole Near a Charged Ball (30 pts)

> [!question] Problem statement
> A neutral, polarizable molecule (polarizability $\alpha$) sits at $\langle x_0,0\rangle$. A uniformly charged ball, total charge $+Q$, sits at $\langle x_0,y_0\rangle$ (directly "above" the molecule, same $x$).
> 1. **[10 pts]** Induced dipole moment of the molecule.
> 2. **[15 pts]** Force the induced dipole exerts on the charged ball.
> 3. **[5 pts]** Force the ball exerts on the induced dipole.
> 4. **[10 pts]** Where to place a second $+Q$ ball so the net force on the molecule is $\vec 0$.

**Solution.**

**Part 1.** The molecule polarizes in response to the ball's field at its own location. Separation vector (molecule minus ball): $\vec r = \langle x_0,0\rangle - \langle x_0,y_0\rangle = \langle 0,-y_0\rangle$, so $r=y_0$, $\hat r = \langle 0,-1\rangle$.

$$\vec E_{\text{applied}} = \frac{kQ}{y_0^2}\langle 0,-1\rangle \quad\Longrightarrow\quad \boxed{\vec p = \alpha\vec E_{\text{applied}} = \frac{\alpha kQ}{y_0^2}\langle 0,-1\rangle}$$

The induced dipole points straight down (its negative end shifted toward the ball, positive end away — wait, check sign: $\vec p$ points *away* from the ball since $\hat r$ points from ball to molecule; this is the standard result that an induced dipole's moment points along the external field, which itself points away from a positive source).

**Part 2 — force on the ball.** The molecule sits directly below the ball, so the ball is exactly **on-axis** of this tiny dipole, at distance $y_0$:

$$|\vec E_{\text{dipole,axis}}| = \frac{2kp}{y_0^3} = \frac{2k}{y_0^3}\cdot\frac{\alpha kQ}{y_0^2} = \frac{2k^2Q\alpha}{y_0^5}$$

Since $\vec p$ points in $-\hat y$, its on-axis field also points along $-\hat y$ at the ball's location (on-axis dipole field is parallel to $\vec p$ on either side):

$$\boxed{\vec F_{\text{dipole on ball}} = Q\,\vec E_{\text{dipole}} = \frac{2k^2Q^2\alpha}{y_0^5}\langle 0,-1\rangle}$$

**Part 3 — force on the dipole (Newton's third law).** This is simply the reaction pair to part 2:

$$\boxed{\vec F_{\text{ball on dipole}} = -\vec F_{\text{dipole on ball}} = \frac{2k^2Q^2\alpha}{y_0^5}\langle 0,1\rangle}$$

(The molecule is pulled *up*, toward the ball — the induced-dipole/point-charge interaction is always attractive, regardless of the source charge's sign, because the dipole always forms so as to be pulled in.)

**Part 4 — canceling the net force.** We need a second $+Q$ ball whose attraction on the molecule exactly cancels the first ball's pull (part 3). By symmetry, place the second ball the same distance $y_0$ from the molecule but on the **opposite side**, at $\langle x_0,-y_0\rangle$. Check: this ball's field at the molecule is $\vec E_2 = \dfrac{kQ}{y_0^2}\langle 0,1\rangle$ (pointing away from it, i.e. $+\hat y$), inducing $\vec p_2 = \dfrac{\alpha kQ}{y_0^2}\langle 0,1\rangle$ — the *opposite* sign from $\vec p$ in part 1. By the identical on-axis calculation as part 2 (with the sign flip carried through), ball 2 pulls the molecule toward itself with force $\dfrac{2k^2Q^2\alpha}{y_0^5}\langle 0,-1\rangle$, which exactly cancels the force from ball 1. $\checkmark$

$$\boxed{\text{Place the second ball at } \langle x_0,\,-y_0\rangle}$$

---

# Part B — Spring 2023 Test 1

## B1. Problem 1 — Coding: Field and Force of a Charged Ball (20 pts)

> [!question] Problem statement
> A ball with charge $Q=5\times10^{-4}$ C sits at $\vec r = \langle 1.2,0,3.1\rangle$ m. A particle with $q=-1$ nC sits at the origin.
> ```python
> ball = sphere(color=color.orange, radius=0.9)
> ball.pos = vector(1.2, 0, 3.1); ball.charge = 5e-4
> particle = sphere(color=color.cyan, radius=0.1)
> particle.pos = vector(0,0,0); particle.charge = -1e-9
> k = 9e9
> ```
> 1. **[10 pts]** Field due to the ball at the particle's location. 2. **[5 pts]** Force on the particle. 3. **[5 pts]** Arrow visualizing the field.

**Solution.** Identical structure to A1:
```python
r = particle.pos - ball.pos
rmag = mag(r)
rhat = norm(r)
E = (k*ball.charge/rmag**2)*rhat

F = particle.charge*E

ea = arrow(pos = particle.pos, axis = E)
```
$$\boxed{\vec E = \frac{kQ}{r^2}\hat r,\qquad \vec F = qE,\qquad \text{arrow at the particle, along }\vec E}$$

---

## B2. Problem 2 — Point Charges on a Square (30 pts)

> [!question] Problem statement
> Four point charges sit at the corners of a square of side $d$ centered at the origin: $q_1=q_2=q_3=+Q$, $q_4=-2Q$.
> 1. **[20 pts]** Find $\vec E_{\text{net}}$ at the origin. 2. **[10 pts]** If $|Q|=5$ mC, $d=10$ cm, find $|\vec F_{\text{net}}|$ on an electron placed at the origin.

**Solution.**

**Setup and symmetry.** Let the square have corners at $\langle \pm d/2,\pm d/2,0\rangle$. Label $q_1,q_2,q_3$ the three $+Q$ corners and $q_4=-2Q$ the fourth. Because $q_2$ and $q_3$ (the two identical $+Q$ charges *not* diagonal to $q_4$) sit symmetrically about the origin — their connecting line has its midpoint exactly at the center — **their field contributions at the origin cancel exactly**. So we only need $q_1$ (the $+Q$ charge diagonal to $q_4$) and $q_4$ itself, which sit at *opposite* corners, i.e. $\vec r_{1} = -\vec r_4$ relative to the origin.

Take $q_1$ at $\langle -d/2,d/2,0\rangle$ and $q_4$ at $\langle d/2,-d/2,0\rangle$ (diagonal corners). Observation point minus source:
$$\vec r_1 = \langle 0,0,0\rangle - \langle -\tfrac d2,\tfrac d2,0\rangle = \Big\langle \tfrac d2,-\tfrac d2,0\Big\rangle,\qquad \vec r_4 = \Big\langle -\tfrac d2,\tfrac d2,0\Big\rangle = -\vec r_1$$
$$|\vec r_1|=|\vec r_4| = \frac{d}{\sqrt2},\qquad \hat r_1 = \Big\langle \tfrac{\sqrt2}{2},-\tfrac{\sqrt2}{2},0\Big\rangle,\qquad \hat r_4 = -\hat r_1$$

$$\vec E_1 = \frac{kq_1}{r_1^2}\hat r_1 = \frac{2kQ}{d^2}\Big\langle \tfrac{\sqrt2}{2},-\tfrac{\sqrt2}{2},0\Big\rangle$$
$$\vec E_4 = \frac{kq_4}{r_4^2}\hat r_4 = \frac{2k(-2Q)}{d^2}\Big(-\Big\langle \tfrac{\sqrt2}{2},-\tfrac{\sqrt2}{2},0\Big\rangle\Big) = \frac{4kQ}{d^2}\Big\langle \tfrac{\sqrt2}{2},-\tfrac{\sqrt2}{2},0\Big\rangle$$

Adding (both point the *same* direction, so they add rather than partially cancel):

$$\vec E_{\text{net}} = \vec E_1+\vec E_4 = \frac{6kQ}{d^2}\Big\langle \tfrac{\sqrt2}{2},-\tfrac{\sqrt2}{2},0\Big\rangle = \frac{3\sqrt2\,kQ}{d^2}\langle 1,-1,0\rangle$$

$$\boxed{\vec E_{\text{net}} = \frac{3\sqrt2\,kQ}{d^2}\langle 1,-1,0\rangle}$$

**Part 2 — force on an electron.**

$$|\vec E_{\text{net}}| = \frac{3\sqrt2\,kQ}{d^2}\sqrt{1^2+1^2} = \frac{6kQ}{d^2}$$

$$|\vec F_{\text{net}}| = |{-e}|\,|\vec E_{\text{net}}| = \frac{6kQe}{d^2} = \frac{6(9\times10^{9})(5\times10^{-3})(1.6\times10^{-19})}{(0.10)^2}$$

$$\boxed{|\vec F_{\text{net}}| = 4.3\times10^{-9}\ \text{N} = 4.3\ \text{nN}}$$

---

## B3. Problem 3 — Induced Dipole Between Two Point Charges (30 pts)

> [!question] Problem statement
> Charges $A$ (at $\langle -x_0,0,0\rangle$, known $+Q$) and $B$ (at $\langle x_0,0,0\rangle$, unknown) flank a neutral atom at the origin. Experimentally, $\vec E_{\text{net}}$ at $D=\langle 0,y_0,0\rangle$ points **purely along $x$**.
> 1. **[10 pts]** Sign and magnitude of $B$. 2. **[10 pts]** How the atom polarizes; find $\vec p$ (polarizability $\alpha$). 3. **[10 pts]** Force on the polarized atom due to $B$.

**Solution.**

**Part 1.** $D$ is equidistant from $A$ and $B$ and lies on their perpendicular bisector. If $A$ and $B$ had different magnitudes or the same sign, the $y$-components of their fields at $D$ would **not** cancel, and $\vec E_{\text{net}}$ would have a $y$-component — contradicting the given fact that it's purely along $x$. The only way the $y$-components cancel while the $x$-components survive is if $B$ has the **same magnitude, opposite sign** as $A$:

$$\boxed{q_B = -Q}$$

**Part 2 — polarization of the atom.** With $A=+Q$ on the left and $B=-Q$ on the right, the field at the origin points from $A$ toward... let's compute directly. Both charges are a distance $x_0$ from the origin.
$$\vec E_A = \frac{kQ}{x_0^2}\langle 1,0,0\rangle \quad(\text{field points away from }+Q\text{, i.e. toward }+x)$$
$$\vec E_B = \frac{k(-Q)}{x_0^2}\langle -1,0,0\rangle = \frac{kQ}{x_0^2}\langle 1,0,0\rangle \quad(\text{field points toward }-Q\text{, also }+x)$$
Both add constructively:
$$\vec E_{\text{applied}} = \frac{2kQ}{x_0^2}\langle 1,0,0\rangle$$
The atom's electron cloud (negative) is pulled toward $A$ (the $+Q$ side, i.e. $-x$), and its nucleus shifts toward $B$ (the $-Q$ side, i.e. $+x$) — the induced dipole points in $+\hat x$, along the applied field:

$$\boxed{\vec p = \alpha\vec E_{\text{applied}} = \frac{2\alpha kQ}{x_0^2}\hat x}$$

**Part 3 — force on the atom due to $B$.** Easiest via Newton's third law: compute the force the *dipole* exerts on $B$, then flip the sign. $B$ sits at $\langle x_0,0,0\rangle$, exactly on-axis of the dipole (which lies along $\hat x$, at the origin), at distance $x_0$:

$$\vec F_{\text{dipole on }B} = q_B\vec E_{\text{dipole,axis}}(\text{at }B) = q_B\cdot\frac{2k\vec p}{x_0^3} = (-Q)\cdot\frac{2k}{x_0^3}\cdot\frac{2\alpha kQ}{x_0^2}\hat x = -\frac{4\alpha k^2Q^2}{x_0^5}\hat x$$

$$\boxed{\vec F_{B\text{ on atom}} = -\vec F_{\text{dipole on }B} = \frac{4\alpha k^2Q^2}{x_0^5}\hat x}$$

(This is attractive — the atom is pulled *toward* $B$, i.e. toward $+x$, consistent with induced-dipole attraction.)

---

## B4. Problem 4 — Dipole Inside a Conducting Shell (20 pts)

> [!question] Problem statement
> A dipole sits at the center of a neutral metallic spherical shell (finite thickness), with dipole separation $\ll$ shell radius. At four points $A,B,C,D$ (labeled around the shell), sketch $\vec E_{\text{dipole}}$, $\vec E_{\text{metal}}$ (the polarization field from the shell's own induced charge), and $\vec E_{\text{net}}$, with arrow length representing relative magnitude.

**Solution.** This is a pure conceptual/qualitative problem, but it hinges on one of the most important facts in electrostatics:

> [!important] Key fact
> **The electric field is exactly zero everywhere inside the bulk material of a conductor in electrostatic equilibrium.** This isn't approximate — it's the *definition* of equilibrium: if $\vec E\neq 0$ inside a conductor, free charges would still be accelerating, so the charges keep rearranging on the surfaces until $\vec E=0$ throughout the metal.

Since points $A,B,C,D$ all lie **within the metal itself** (inside the conducting shell material, not in the central cavity and not outside the shell), we know immediately, with no calculation:

$$\boxed{\vec E_{\text{net}} = \vec 0 \text{ at every point } A,B,C,D, \text{ because each point sits inside the conducting shell material}}$$

For the sketch: $\vec E_{\text{dipole}}$ (the bare dipole field, ignoring the metal) is nonzero and points in the usual dipole pattern, with different magnitudes at each of the four points depending on their distance and angle from the dipole at the center. Since $\vec E_{\text{net}}=\vec 0$ always, the induced surface charges on the shell must generate a field $\vec E_{\text{metal}}$ that is **exactly equal in magnitude and opposite in direction** to $\vec E_{\text{dipole}}$ at *every one* of these four points — so each pair of arrows ($\vec E_{\text{dipole}}$, $\vec E_{\text{metal}}$) should be drawn with identical length but opposite direction, while the $\vec E_{\text{net}}$ arrow at each point has zero length (a labeled dot, "0").

---

# Part C — Spring 2024 Test 1

## C1. Problem 1 — Two Point Charges on the $y$-axis (30 pts)

> [!question] Problem statement
> $+Q$ sits at $\langle 0,d,0\rangle$, $-Q$ sits at $\langle 0,-d,0\rangle$.
> 1. **[10 pts]** Net field at $\vec r_A = \langle d\sqrt3,0,0\rangle$. 
> 2. **[10 pts]** Force on an electron placed at $\vec r_A$. 
> 3. **[10 pts]** Where to place $q_4=-Q$ so the net force on that electron is zero.

**Solution.**

**Part 1.** Field point minus source, for each charge:
$$\vec r_+ = \vec r_A - \langle 0,d,0\rangle = \langle d\sqrt3,-d,0\rangle,\qquad |\vec r_+| = d\sqrt{3+1} = 2d$$
$$\vec r_- = \vec r_A - \langle 0,-d,0\rangle = \langle d\sqrt3,d,0\rangle,\qquad |\vec r_-| = 2d$$
$$\vec E_+ = \frac{kQ}{(2d)^3}\langle d\sqrt3,-d,0\rangle = \frac{kQ}{8d^2}\langle \sqrt3,-1,0\rangle$$
$$\vec E_- = \frac{k(-Q)}{(2d)^3}\langle d\sqrt3,d,0\rangle = \frac{kQ}{8d^2}\langle -\sqrt3,-1,0\rangle$$
$$\vec E_{\text{net}} = \vec E_++\vec E_- = \frac{kQ}{8d^2}\langle 0,-2,0\rangle = \frac{kQ}{4d^2}\langle 0,-1,0\rangle$$

$$\boxed{\vec E_{\text{net}} = -\frac{kQ}{4d^2}\hat y = -\frac{1}{4\pi\epsilon_0}\frac{Q}{4d^2}\hat y}$$

**Part 2.** Force on an electron ($q=-e$) at $\vec r_A$:

$$\vec F_{\text{net}} = (-e)\vec E_{\text{net}} = (-e)\Big(-\frac{kQ}{4d^2}\hat y\Big)$$

$$\boxed{\vec F_{\text{net}} = \frac{kQe}{4d^2}\hat y}$$

**Part 3.** We need $\vec E_{4}$ (from the new charge $q_4=-Q$) to exactly cancel $\vec E_{\text{net}}$ from part 1 (since $\vec F_{\text{net}} = -e\vec E_{\text{net}}$, zero force $\iff$ zero net field):

$$\vec E_4 = -\vec E_{\text{net,old}} = \frac{kQ}{4d^2}\hat y$$

Since $q_4$ is a point charge, $\vec E_4 = \dfrac{kq_4}{|\vec r\,|^2}\hat r$ where $\vec r$ points from $q_4$ to $\vec r_A$. Matching magnitudes:

$$\Big|\frac{kQ}{|\vec r\,|^2}\Big| = \frac{kQ}{4d^2} \;\Longrightarrow\; |\vec r\,|^2 = 4d^2 \;\Longrightarrow\; |\vec r\,| = 2d$$

Since $q_4$ is *negative*, its field at $\vec r_A$ points *toward* $q_4$; for that field to point in $+\hat y$ from $\vec r_A$, $q_4$ must lie in the $+\hat y$ direction from $\vec r_A$, i.e. $\hat r = -\hat y$ (pointing from $q_4$ down to $\vec r_A$ along $-\hat y$ means $q_4$ is above $\vec r_A$). Concretely: $\vec r_4 = \vec r_A - \vec r = \vec r_A - (2d)(-\hat y) = \langle d\sqrt3,0,0\rangle + \langle 0,2d,0\rangle$.

$$\boxed{\text{Place } q_4 \text{ at } \langle \sqrt3\,d,\ 2d,\ 0\rangle}$$

---

## C2. Problem 2 — Conductor and Insulator Polarization (40 pts)

> [!question] Problem statement
> A neutral metal spherical shell centered at the origin has a cluster of positive ions (total $+Q$) at its center. An observer stands on the $-x$-axis.
> 1. **[5 pts]** Sketch how the shell polarizes. 2. **[10 pts]** Find $\vec E_{pm}$, the field contribution of the polarized metal *itself*, at a point $A$ a distance $d$ from the center (inside the shell material). 3. **[10 pts]** Metal replaced by insulating plastic; sketch its polarization at two points $B,C$ (different distances from the ions). 4. **[10 pts]** Sketch/discuss all field contributions at the observer's location, including how each scales with distance. 5. **[5 pts]** If the plastic is then removed, does the net field at the observer increase, decrease, or stay the same?

**Solution.**

**Part 1.** Because $+Q$ sits at the center of the neutral shell, the conductor's free electrons are pulled inward: a uniform **$-Q$ accumulates on the inner surface** of the shell (facing the ions) and, since the shell must stay net-neutral overall, a uniform **$+Q$ accumulates on the outer surface**. Both surface charges are spherically symmetric because the source ($+Q$ at the exact center) is itself spherically symmetric.

**Part 2.** Point $A$ (distance $d$ from center) lies **inside the metal**, so as established above (see B4), the total field there must vanish:
$$\vec E_{\text{net}} = \vec E_{pm} + \vec E_{\text{ion}} = \vec 0 \;\Longrightarrow\; \vec E_{pm} = -\vec E_{\text{ion}}$$
The ions' field at $A$ (on the $-x$-axis, distance $d$) points radially outward from the center, i.e. in the $-\hat x$ direction: $\vec E_{\text{ion}} = \dfrac{kQ}{d^2}(-\hat x)$. Therefore

$$\boxed{\vec E_{pm} = \frac{kQ}{d^2}\hat x}$$

(pointing back toward the center — this is the field of the induced surface charges alone, and it exactly cancels the ions' field inside the metal.)

**Part 3.** With the metal replaced by insulating plastic, there's no free-electron sea, so no bulk cancellation occurs. Instead, each *atom or molecule* of the plastic polarizes individually in response to the (now un-cancelled) field of the central ions, forming a tiny induced dipole that points **away from** the ions (its $-$ end nearer the ions, $+$ end farther) at every location in the plastic. Since the field from the ions falls off as $1/r^2$, a point closer to the ions experiences a stronger applied field and therefore polarizes *more strongly* (a bigger induced dipole moment, drawn as a more elongated $+/-$ pair) than a point farther away. If $B$ is closer to the ions than $C$: **the dipole at $B$ is larger (more elongated) than the dipole at $C$**, but both point the same way (radially, with $-$ toward the ions).

**Part 4.** At the observer's location (on the $-x$-axis, outside the plastic), two separate field contributions arrive:
- $\vec E_{\text{ion}}$, from the central ion cluster directly, falling off as $\dfrac{1}{r^2}$ (a true point-charge/monopole field);
- $\vec E_{\text{plastic}}$, from the net polarization of the plastic block, which — being built from a collection of induced dipoles — falls off *faster*, as $\dfrac{1}{r^3}$ (dipole-like).

Both arrows point in the same general sense (from the ions toward/past the observer) but the ion arrow should be drawn noticeably longer at large distances since $1/r^2$ dominates $1/r^3$ far away, and the plastic's contribution should be labeled explicitly as falling off faster with distance.

**Part 5.** Removing the plastic removes its field contribution $\vec E_{\text{plastic}}$, which (per Part 4) pointed the *same direction* as $\vec E_{\text{ion}}$ at the observer. Taking away a contribution that was adding to the total:

$$\boxed{\text{The net field at the observer } \textbf{decreases} \text{ — } \vec E_{\text{plastic}} \text{ was pointing the same way as } \vec E_{\text{ion}}\text{, so removing it removes a contribution that had been reinforcing the total.}}$$

---

## C3. Problem 3 — Dipole/Charge/Induced-Dipole Equilibrium (30 pts)

> [!question] Problem statement
> A small sphere, charge $Q$, mass $m$, hangs from a thread. A dipole ($p=qs$) lies a distance $l$ directly below it ($l\gg s$, and $l$ large compared to the sphere's size).
> 1. **[10 pts]** Find the specific $Q$ (with sign) so the sphere is in equilibrium (electric force from the dipole cancels gravity).
> 2. **[10 pts]** The dipole suddenly rotates $90°$ so $\vec p$ points horizontally ("to the right"). Which way does the force on the sphere now point? Explain.
> 3. **[10 pts]** Replace the dipole with a neutral atom (mass $m$, polarizability $\alpha$). Find the new equilibrium $Q$, and comment on its sign.

**Solution.**

**Part 1.** Set up: the dipole is directly below the sphere, oriented with $\hat p$ pointing straight up (toward the sphere) — this is the on-axis configuration, with the sphere a distance $l$ along the dipole's axis. Force balance on the sphere ($\hat y$ up):

$$\vec F_{\text{net}} = \vec F_g + \vec F_e = \vec 0 \;\Longrightarrow\; \vec F_e = -\vec F_g = mg\,\hat y$$

By Newton's third law, $\vec F_e$ (force of dipole on sphere) $= -\vec F_{\text{sphere on dipole}} = -Q\vec E_{\text{dipole}}(\text{at sphere})$, evaluated on-axis at distance $l$:

$$\vec F_e = -Q\cdot\frac{2k\vec p}{l^3} = -Q\cdot\frac{2kqs}{l^3}\hat y$$

Setting this equal to $mg\,\hat y$:

$$mg = -\frac{2kQqs}{l^3} \;\Longrightarrow\; \boxed{Q = -\frac{mgl^3}{2kqs} = -\frac{2\pi\epsilon_0\, mgl^3}{qs}}$$

The negative sign makes sense: the sphere must be *attracted* toward the dipole's near ($+$) end to be pulled down against... actually, to be pulled *up* (canceling gravity which pulls it down), the sphere must be attracted toward the dipole below it, which requires $Q$ opposite in sign to whichever pole is closer — working through the algebra confirms $Q<0$ is required.

**Part 2.** After the $90°$ rotation, $\vec p$ points horizontally ("to the right"), which means the sphere — directly above the dipole's center — is now on the dipole's **perpendicular bisector**, not its axis. The perpendicular-axis field of a dipole points *antiparallel* to $\vec p$, so $\vec E_{\text{dipole}}$ at the sphere now points to the **left** ($-\hat p$ direction). Since $Q<0$ (from part 1), the force $\vec F=Q\vec E$ flips relative to the field direction:

$$\boxed{\text{The force on the sphere points to the } \textbf{right} \text{ (in the same sense as } \vec p\text{)}}$$

**Reasoning in one sentence:** with $\vec p$ pointing right, the sphere sits on the dipole's perpendicular axis where $\vec E_{\text{dipole}}$ points left (antiparallel to $\vec p$); since the sphere's charge $Q$ is negative, the force $\vec F = Q\vec E$ points opposite to $\vec E$, i.e. to the right.

**Part 3.** Replace the dipole with a neutral atom of polarizability $\alpha$. Now the atom's induced dipole moment depends self-consistently on the sphere's own field: $\vec p_{\text{ind}} = \alpha\vec E_Q$, where $\vec E_Q = \dfrac{kQ}{l^2}(-\hat y)$ is the sphere's field at the atom (pointing down from sphere to atom, i.e. $-\hat y$, since the field point is *below* the source):

$$\vec p_{\text{ind}} = \frac{\alpha kQ}{l^2}(-\hat y)$$

By Newton's third law again, the force on the sphere equals minus the force the sphere would exert... equivalently, force of atom's dipole on the sphere $= -Q\vec E_{\text{ind,axis}}(\text{at sphere})$:

$$\vec F_e = -Q\cdot\frac{2k\vec p_{\text{ind}}}{l^3} = -Q\cdot\frac{2k}{l^3}\Big(\frac{\alpha kQ}{l^2}\Big)(-\hat y) = \frac{2\alpha k^2Q^2}{l^5}\hat y$$

Setting equal to $mg\hat y$ for equilibrium:

$$mg = \frac{2\alpha k^2Q^2}{l^5} \;\Longrightarrow\; Q^2 = \frac{mgl^5}{2\alpha k^2} \;\Longrightarrow\; \boxed{Q = \pm\sqrt{\frac{mgl^5}{2\alpha k^2}} = \pm\,2\pi\epsilon_0\sqrt{\frac{2mgl^5}{\alpha}}}$$

**Comment on sign:** unlike part 1, **either sign of $Q$ works** here. If $Q>0$, the field it creates at the atom points downward, so the induced dipole points down (its $+$ end away from the sphere); if $Q<0$, the field points upward and the induced dipole flips to point up instead. But in *both* cases, the induced dipole's near end automatically takes on the charge opposite to $Q$ — the interaction between any point charge and the dipole it itself induces is **always attractive**. Since we need an attractive (upward) force on the atom regardless, $Q$ can be either sign; only its magnitude is fixed.

---

# Part D — GPS 1 (no official key)

> [!warning] No official solutions exist for GPS 1 or GPS 2
> The problems below were solved independently, using the exact same formula sheet and methods as the three tests above. Each result was cross-checked (by an alternate method or dimensional/limiting-case check) before being written down here.

## D1. Problem 1 — Two Point Charges: Force and Balancing Position

> [!question] Problem statement
> $q_1 = 2.5\times10^{-5}$ C at $\vec r_1 = \langle -4,3,0\rangle$ m; $q_2=-5\times10^{-5}$ C at $\vec r_2=\langle 4,-3,0\rangle$ m.
> **A.** Net electric force on an electron at the origin (as a vector). 
> **B.** Where to place $q_3=1.2\times10^{-5}$ C (positive) so the net force on that electron is zero.

**Solution.**

**Part A.** Note $|\vec r_1|=|\vec r_2|=\sqrt{4^2+3^2}=5$ m (a 3-4-5 triangle), and $\vec r_2=-\vec r_1$ — the two charges are diametrically opposite through the origin.

Field at the origin due to a charge $q_i$ at $\vec r_i$: since the observation point is the origin, the "source-to-field" vector is $\vec 0-\vec r_i=-\vec r_i$, so $\vec E_i = kq_i(-\vec r_i)/|\vec r_i|^3$.

$$\vec E_1 = -\frac{kq_1}{5^3}\langle -4,3,0\rangle = -\frac{(9\times10^9)(2.5\times10^{-5})}{125}\langle -4,3,0\rangle = -1800\langle -4,3,0\rangle = \langle 7200,-5400,0\rangle\ \text{N/C}$$

$$\vec E_2 = -\frac{kq_2}{5^3}\langle 4,-3,0\rangle = -\frac{(9\times10^9)(-5\times10^{-5})}{125}\langle 4,-3,0\rangle = 3600\langle 4,-3,0\rangle = \langle 14400,-10800,0\rangle\ \text{N/C}$$

$$\vec E_{\text{net}} = \vec E_1+\vec E_2 = \langle 21600,\,-16200,\,0\rangle\ \text{N/C}$$

Force on an electron, $\vec F = (-e)\vec E_{\text{net}}$:

$$\vec F = -(1.6\times10^{-19})\langle 21600,-16200,0\rangle$$

$$\boxed{\vec F_{\text{net}} = \langle -3.46\times10^{-15},\ 2.59\times10^{-15},\ 0\rangle\ \text{N}\qquad(|\vec F_{\text{net}}| \approx 4.32\times10^{-15}\text{ N})}$$

**Part B.** For zero net force on the electron, we need the *total field* at the origin to vanish (force $=-e\vec E$, and $e\neq0$), so $q_3$'s field there must cancel $\vec E_{\text{net}}$ above:

$$\vec E_3 = -\vec E_{\text{net}} = \langle -21600,\,16200,\,0\rangle\ \text{N/C},\qquad |\vec E_3| = \sqrt{21600^2+16200^2} = 27000\ \text{N/C}$$

Since $q_3>0$, its field at the origin points *away from* $q_3$; for that field to point in the direction $\langle -21600,16200,0\rangle$ (unit vector $\langle -0.8,0.6,0\rangle$), the charge $q_3$ itself must sit in the *opposite* direction from the origin, i.e. along $\langle 0.8,-0.6,0\rangle$ — notice this is the **same line** through the origin that already contains $q_1$ and $q_2$ (direction $\langle \pm0.8,\mp0.6,0\rangle$), on the $q_2$ side.

Solve for the distance $r$: $\dfrac{kq_3}{r^2}=27000 \Rightarrow r^2 = \dfrac{(9\times10^9)(1.2\times10^{-5})}{27000}=4\ \Rightarrow\ r=2$ m.

$$\boxed{\text{Place } q_3 \text{ at } \vec r_3 = 2\langle 0.8,-0.6,0\rangle = \langle 1.6,\,-1.2,\,0\rangle\ \text{m}}$$

---

## D2. Problem 2 — Four Charges on a Square

> [!question] Problem statement
> Four identical $+q$ charges sit at the corners of a square (side $a$) centered at the origin.
> **A.** Total number of pairwise electric forces present (each nonzero force counted separately). **B.** Total net force on the whole 4-charge system, and why. **C.** Magnitude of the force on the lower-left charge. **D.** Magnitude of the net field far away ($r\gg a$).

**Solution.**

**Part A.** With 4 charges, there are $\binom{4}{2}=6$ distinct *pairs*, and each pair contributes **two** forces (the force of charge $i$ on $j$, and the equal-and-opposite force of $j$ on $i$ — both count separately per the problem's instructions):

$$\boxed{6\ \text{pairs} \times 2\ \text{forces per pair} = 12\ \text{forces total}}$$

**Part B.** $\boxed{\text{Zero.}}$ Every one of the 12 forces above is part of a Newton's-third-law action/reaction pair *internal to the system* (charge $i$ on $j$ exactly cancels charge $j$ on $i$ when summed). With no external charges present, summing all internal forces over the whole system, every pair cancels, so the net force on the 4-charge system as a whole is exactly $\vec 0$ — regardless of the charges' arrangement.

**Part C.** Place the square's corners at $\langle \pm a/2,\pm a/2,0\rangle$; consider the lower-left corner, charge $q$ at $\langle -a/2,-a/2,0\rangle$. It feels:
- A repulsive force from its **horizontal neighbor** (lower-right, distance $a$): magnitude $kq^2/a^2$, pointing in $-\hat x$.
- A repulsive force from its **vertical neighbor** (upper-left, distance $a$): magnitude $kq^2/a^2$, pointing in $-\hat y$.
- A repulsive force from the **diagonal charge** (upper-right, distance $a\sqrt2$): magnitude $\dfrac{kq^2}{2a^2}$, pointing along $\langle -1,-1,0\rangle/\sqrt2$.

Adding components (by symmetry $F_x=F_y$):
$$F_x = \frac{kq^2}{a^2} + \frac{kq^2}{2a^2}\cdot\frac{1}{\sqrt2} = \frac{kq^2}{a^2}\Big(1+\frac{1}{2\sqrt2}\Big)$$
$$|\vec F| = \sqrt2\,F_x = \frac{kq^2}{a^2}\Big(\sqrt2 + \frac{1}{2}\Big)$$

$$\boxed{|\vec F_{\text{lower-left}}| = \frac{kq^2}{a^2}\Big(\sqrt2+\frac12\Big) \approx 1.914\,\frac{kq^2}{a^2}}$$

**Part D.** The square's total charge is $4q \neq 0$ — it is *not* neutral, so at distances $r\gg a$ the leading-order behavior is the ordinary point-charge (monopole) field of the total charge; the dipole and higher-multipole corrections vanish faster and are negligible at large $r$:

$$\boxed{|\vec E_{\text{far}}| \approx \frac{k(4q)}{r^2} = \frac{4kq}{r^2}}$$

---

## D3. Problem 3 — Two Point Charges: Field, Force, and Variations

> [!question] Problem statement
> $q_1=5\ \mu\text{C}$ at the origin; $q_2=-7\ \mu\text{C}$ at $\langle 3,4,0\rangle$ cm.
> **A.** Is $q_1$'s field affected by $q_2$'s presence? **B.** Field due to $q_1$ at $q_2$'s location. **C.** Draw it. **D.** Net force on $q_2$. **E.** Draw it. **F.** $q_1\to10\ \mu\text{C}$: new force on $q_2$. **G.** $q_1=5\ \mu\text{C}$ restored, $q_2$ moved to $\langle 6,8,0\rangle$ cm: new force on $q_2$.

**Solution.**

**Part A.** $\boxed{\text{No.}}$ By the **superposition principle**, the electric field created by a given charge depends *only* on that charge's own magnitude and position — never on what other charges happen to be present nearby. $q_1$'s field fills all of space exactly as if $q_2$ weren't there; $q_2$ simply *responds* to that (unaffected) field by feeling a force. (Superposition is precisely the statement that fields from different sources simply add, without altering one another.)

**Part B.** Convert to meters: $q_2$ is at $\langle 0.03,0.04,0\rangle$ m, distance from origin $r=\sqrt{0.03^2+0.04^2}=0.05$ m (a scaled 3-4-5 triangle), $\hat r = \langle 0.6,0.8,0\rangle$.

$$\vec E = \frac{kq_1}{r^2}\hat r = \frac{(9\times10^9)(5\times10^{-6})}{(0.05)^2}\langle 0.6,0.8,0\rangle$$

$$\boxed{\vec E = \langle 1.08\times10^7,\ 1.44\times10^7,\ 0\rangle\ \text{N/C}}$$

**Part C.** (Sketch: an arrow at $q_2$'s location pointing away from $q_1$, along $\langle 0.6,0.8,0\rangle$ — i.e. up and to the right, away from the origin.)

**Part D.** $\vec F = q_2\vec E$:

$$\vec F = (-7\times10^{-6})\langle 1.08\times10^7,1.44\times10^7,0\rangle$$

$$\boxed{\vec F_{\text{net}} = \langle -75.6,\ -100.8,\ 0\rangle\ \text{N}\qquad (|\vec F|=126\ \text{N})}$$

Quick check via the direct Coulomb formula: $|\vec F| = \dfrac{k|q_1||q_2|}{r^2} = \dfrac{(9\times10^9)(5\times10^{-6})(7\times10^{-6})}{(0.05)^2}=126$ N. $\checkmark$ Since $q_1>0$ and $q_2<0$, the force is **attractive** — it points from $q_2$ back toward $q_1$, i.e. along $\langle -0.6,-0.8,0\rangle$, matching the signs above.

**Part E.** (Sketch: an arrow at $q_2$ pointing back toward the origin — opposite direction from the field arrow in Part C, since $q_2$ is negative.)

**Part F.** Doubling $q_1$ to $10\ \mu\text{C}$ doubles the force magnitude (force $\propto q_1$), keeping the same attractive direction:

$$\boxed{\vec F_{\text{new}} = \langle -151.2,\ -201.6,\ 0\rangle\ \text{N}\qquad(|\vec F|=252\ \text{N})}$$

**Part G.** $q_2$ moved to $\langle 6,8,0\rangle$ cm $=\langle 0.06,0.08,0\rangle$ m — this is exactly *twice* the original distance from the origin ($r=0.10$ m instead of $0.05$ m), along the same direction. Since $F\propto 1/r^2$, doubling $r$ divides the force by $4$:

$$|\vec F| = \frac{126\ \text{N}}{4} = 31.5\ \text{N, direction still } \langle -0.6,-0.8,0\rangle$$

$$\boxed{\vec F_{\text{new}} = \langle -18.9,\ -25.2,\ 0\rangle\ \text{N}\qquad(|\vec F|=31.5\ \text{N})}$$

---

## D4. Problem 4 — Two Dipoles: Field at the Midpoint

> [!question] Problem statement
> Two dipoles lie on parallel horizontal lines, centers separated by vertical distance $d$ ($d\gg$ either dipole's own separation). The **blue** dipole (top) has charge magnitude $q$ and separation $s$, with $+$ on the left and $-$ on the right. The **orange** dipole (bottom) has charge magnitude $q$ and separation $2s$, also $+$ on the left, $-$ on the right, directly below the blue one. Find $\vec E_{\text{net}}$ at the point exactly halfway between the two dipole centers.

**Solution.** The key geometric fact: both dipoles are oriented **horizontally**, while the line connecting their two centers is **vertical**. That means the midpoint lies on the **perpendicular bisector** of *both* dipoles (not on-axis!) — each dipole "looks sideways" at the midpoint.

**Dipole moment directions.** With $+$ on the left and $-$ on the right for both dipoles, each dipole moment $\vec p$ (which points from $-$ to $+$) points in $-\hat x$ (to the left):
$$\vec p_{\text{blue}} = qs\,(-\hat x),\qquad \vec p_{\text{orange}} = q(2s)(-\hat x) = 2qs\,(-\hat x)$$

**Perpendicular-bisector field formula, with direction.** From the formula sheet, $|\vec E_{\text{dipole},\perp}| = \dfrac{kqs}{r^3} = \dfrac{kp}{r^3}$. Deriving the *direction* by direct superposition of the two point charges (place $+q$ at $\langle -s/2,0\rangle$, $-q$ at $\langle s/2,0\rangle$, field point at $\langle 0,r\rangle$, expand to leading order in $s/r$) shows that **the perpendicular-bisector field points antiparallel to $\vec p$** — i.e. here, in $+\hat x$, for *both* dipoles.

**Distances.** The midpoint is a distance $d/2$ from each dipole's center.

$$|\vec E_{\text{blue}}| = \frac{k(qs)}{(d/2)^3} = \frac{8kqs}{d^3},\qquad |\vec E_{\text{orange}}| = \frac{k(2qs)}{(d/2)^3} = \frac{16kqs}{d^3}$$

Both point in $+\hat x$ (since both dipole moments point in $-\hat x$, and the perpendicular field is always antiparallel to $\vec p$), so they **add**:

$$\boxed{\vec E_{\text{net}} = (8+16)\frac{kqs}{d^3}\hat x = \frac{24\,kqs}{d^3}\ \hat x}$$

The field points horizontally, in the direction from each dipole's $-$ charge past its $+$ charge extended (i.e. antiparallel to both dipole moments).

---

# Part E — GPS 2 (no official key)

## E1. Problem 1 — Polarized Carbon Atom: the Momentum Principle

> [!question] Problem statement
> A tiny scrap of paper hangs motionless below a charged pen (charge $Q$). A single carbon atom in the paper has its outer electron cloud (charge $-4e$) shift a distance $s$ when polarized by the pen.
> **A.** Net force on the carbon atom? **B.** Which forces act on the carbon atom (circle all)? **C.** Derive $s$ using the momentum principle, in terms of $Q,m,g,h,e,\pi,\epsilon_0$. **D.** Derive the polarizability $\alpha$ from your result for $s$.

**Solution.**

**Part A.** $\boxed{\text{The net force is zero.}}$ The paper hangs *motionless* — meaning it's in static equilibrium, floating (attracted upward) rather than resting on a surface. A representative atom within that paper is, to good approximation, likewise in force balance: the electric attraction toward the pen exactly cancels gravity.

**Part B.** We only count forces acting *on the carbon atom itself* (not forces the atom exerts on other things, and not forces on the paper or pen as whole different objects):

$$\boxed{\text{The electric force of the pen on the carbon atom}\qquad\text{and}\qquad\text{The gravitational force of the Earth on the carbon atom}}$$

(All the other listed options act on a *different* object — the paper as a whole, or the pen — or are the atom's own reaction force on something else, which by Newton's third law is a force the atom *exerts*, not one it *feels*. There is no table in this scenario, since the paper is suspended in the air.)

**Part C — deriving $s$.** The atom is motionless, so by the momentum principle $d\vec p/dt=\vec F_{\text{net}}=\vec 0$: the electric force from the pen exactly balances gravity, $|\vec F_{\text{elec}}| = mg$.

Model the atom as a permanent-looking induced dipole: nucleus effectively $+4e$ fixed, electron cloud $-4e$ shifted a distance $s$, giving induced dipole moment $p = (4e)s$. The pen (point charge $Q$, distance $h$ away) sits exactly on this tiny dipole's axis, so — using the same Newton's-third-law trick as earlier problems (force of dipole on pen = $-$force of pen on dipole) — the force between them has magnitude

$$|\vec F_{\text{elec}}| = \frac{2k\,Q\,p}{h^3} = \frac{2kQ(4es)}{h^3} = \frac{8kQes}{h^3}$$

Setting this equal to $mg$:

$$\frac{8kQes}{h^3}=mg \;\Longrightarrow\; s = \frac{mgh^3}{8kQe}$$

Substituting $k=\dfrac{1}{4\pi\epsilon_0}$:

$$\boxed{s = \frac{\pi\epsilon_0\,mgh^3}{2Qe}}$$

**Part D — deriving $\alpha$.** By definition, $p=\alpha E_{\text{applied}}$, where $E_{\text{applied}} = \dfrac{kQ}{h^2}$ is the pen's field at the atom, and $p=4es$ is the induced moment found above:

$$\alpha = \frac{p}{E_{\text{applied}}} = \frac{4es}{kQ/h^2} = \frac{4esh^2}{kQ} = 16\pi\epsilon_0\,\frac{esh^2}{Q}$$

Substituting $s=\dfrac{\pi\epsilon_0mgh^3}{2Qe}$ from Part C:

$$\alpha = 16\pi\epsilon_0\frac{eh^2}{Q}\cdot\frac{\pi\epsilon_0mgh^3}{2Qe} = \frac{16\pi^2\epsilon_0^2\,mgh^5}{2Q^2}$$

$$\boxed{\alpha = \frac{8\pi^2\epsilon_0^2\,m\,g\,h^5}{Q^2}}$$

---

## E2. Problem 2 — The Gecko's Van der Waals Force

> [!question] Problem statement
> A gecko's seta is modeled as a permanent dipole (moment $|\vec p|_g$), located a distance $d$ from a neutral, polarizable atom on a tree surface (polarizability $\alpha$), both lying on a common horizontal axis. **A.** Find the induced dipole moment of the neutral atom. **B.** Find the force on the gecko's dipole due to the induced dipole (decompose into point charges; use $(1+\epsilon)^n\approx1+n\epsilon$ for $d\gg s$). **C.** Estimate the number of dipoles needed to support a 10 N adhesive force, using $|\vec p|_g=5\times10^{-30}$ C·m, $d=1.7\times10^{-10}$ m, $\alpha=1.96\times10^{-40}$ C·m/(N/C). Is the result reasonable?

**Solution.**

**Part A — induced moment.** The gecko's dipole lies along the same axis as the atom (both on the $x$-axis in the diagram), so the atom experiences the gecko dipole's **on-axis** field, at distance $d$:

$$\vec E_{\text{gecko at atom}} = \frac{2k\,|\vec p|_g}{d^3}\,\hat p_g$$

(on-axis dipole field points in the same direction as $\vec p_g$ itself). The induced moment follows immediately from $\vec p_{\text{ind}}=\alpha\vec E$:

$$\boxed{\vec p_{\text{ind}} = \frac{2k\alpha\,|\vec p|_g}{d^3}\,\hat p_g}$$

— pointing the *same* direction as the gecko's own dipole moment (physically: the near side of the atom takes on the charge opposite to the gecko dipole's nearer pole, an attractive setup).

**Part B — force between the two dipoles.** This is the classic **point-dipole–point-dipole, on-axis** interaction, and deriving it via direct charge-by-charge superposition (as hinted) proceeds as follows. Model the gecko dipole as $+q_g$ and $-q_g$ separated by $s_g$ (with $q_gs_g=|\vec p|_g$), and the induced dipole as $+q'$, $-q'$ separated by $s'$ (with $q's'=p_{\text{ind}}$), both centered a distance $d$ apart along a common axis.

Writing out the four pairwise Coulomb forces between $\{+q_g,-q_g\}$ and $\{+q',-q'\}$, each term looks like $kq_gq'/(d\pm s_g/2 \pm s'/2)^2$. Expanding every such term with the binomial approximation $(1+\epsilon)^{-2}\approx 1-2\epsilon$ (dropping terms beyond first order in the small ratios $s_g/d$ and $s'/d$) and collecting, the $O(1/d^2)$ and $O(1/d^3)$ pieces cancel between the four terms (as they must, since two truly neutral objects exert no net force from a *uniform* field, only from its *gradient*), leaving the well-known leading-order result for two collinear point dipoles:

$$|\vec F_{\text{dipole-dipole, on-axis}}| = \frac{6k\,p_1p_2}{d^4}\qquad\text{(attractive, when the dipoles are aligned head-to-tail)}$$

Substituting $p_1=|\vec p|_g$ and $p_2=p_{\text{ind}}=\dfrac{2k\alpha|\vec p|_g}{d^3}$ from Part A:

$$|\vec F| = \frac{6k\,|\vec p|_g}{d^4}\cdot\frac{2k\alpha|\vec p|_g}{d^3} = \frac{12\alpha k^2|\vec p|_g^2}{d^7}$$

$$\boxed{|\vec F| = \frac{12\,\alpha\,k^2\,|\vec p|_g^2}{d^7}\quad\text{(attractive — pulling the gecko's seta toward the surface)}}$$

This steep $1/d^7$ falloff is the hallmark of a **Van der Waals** (permanent-dipole–induced-dipole) interaction, distinct from the gentler $1/d^4$ of a permanent-dipole/permanent-dipole force or $1/d^3$ of a charge/dipole force — it requires *very* close contact to be significant, which is exactly why gecko setae work only when in near-atomic contact with a surface.

**Part C — numeric estimate.** Plug in the given values:

$$|\vec F| = \frac{12(1.96\times10^{-40})(9\times10^9)^2(5\times10^{-30})^2}{(1.7\times10^{-10})^7}$$

Numerator: $12\times1.96\times10^{-40}=2.352\times10^{-39}$; $\times(9\times10^9)^2=8.1\times10^{19}$ gives $1.905\times10^{-19}$; $\times(5\times10^{-30})^2=2.5\times10^{-59}$ gives $4.76\times10^{-79}$.

Denominator: $(1.7\times10^{-10})^7 \approx 41.0\times10^{-70}=4.10\times10^{-69}$.

$$|\vec F| \approx \frac{4.76\times10^{-79}}{4.10\times10^{-69}} \approx 1.16\times10^{-10}\ \text{N per dipole}$$

$$N = \frac{10\ \text{N}}{1.16\times10^{-10}\ \text{N}} \approx \boxed{8.6\times10^{10}\ \text{dipoles}}$$

**Is this reasonable?** Yes, this is the right order of magnitude. A gecko's toe carries on the order of a million individual setae, and each seta branches into hundreds to a thousand still-finer spatulae — giving roughly $10^6\times10^3 \sim 10^9$–$10^{10}$ contact points per toe in reality, consistent (within an order of magnitude, which is all this simplified single-dipole-per-contact model should be expected to achieve) with the $\sim 10^{11}$ "dipoles" estimated here.

---

## E3. Problem 3 — Dipole Near a Conducting Sphere

> [!question] Problem statement
> A neutral solid metal sphere (radius $R$) is centered at $\vec r_s = \langle d,d,0\rangle$. A dipole is fixed at the origin, dipole moment magnitude $|qs|=p$, pointing along $\hat p = \langle -1/\sqrt2,1/\sqrt2,0\rangle$. The sphere is far away ($d\gg s$), equilibrium has been reached.
> **A.** Sketch the sphere's polarization. **B.** Net field at the sphere's center (explain). **C.** Field at the center due to the sphere's own polarization. **D.** How does part C change if $\hat p = \langle 1/\sqrt2,1/\sqrt2,0\rangle$ instead?

**Solution.**

**Setup — check the geometry first.** The unit vector from the dipole (origin) to the sphere's center is $\hat r = \dfrac{\langle d,d,0\rangle}{d\sqrt2} = \langle 1/\sqrt2,1/\sqrt2,0\rangle$. Comparing to $\hat p = \langle -1/\sqrt2,1/\sqrt2,0\rangle$:

$$\hat p \cdot \hat r = \Big(-\frac{1}{\sqrt2}\Big)\Big(\frac{1}{\sqrt2}\Big) + \Big(\frac{1}{\sqrt2}\Big)\Big(\frac{1}{\sqrt2}\Big) = -\frac12+\frac12 = 0$$

The dipole moment is **exactly perpendicular** to the line connecting it to the sphere — the sphere sits precisely on the dipole's perpendicular-bisector axis (not an approximation; it's built into the chosen angle).

**Part A.** (Sketch: the sphere polarizes as if sitting in a locally-uniform external field pointing along $-\hat p$ — see Part C for the exact direction — so the sphere develops induced surface charge with the negative side facing the $-\hat p$ direction and positive side facing $+\hat p$, i.e. charge separated perpendicular to the dipole's own orientation.)

**Part B.** $\boxed{\vec E_{\text{net}} = \vec 0}$ at the sphere's center, **for the same universal reason as every previous conductor problem**: the center lies inside the bulk conducting material, and a conductor in electrostatic equilibrium always has zero field inside itself — this holds *regardless* of the dipole's orientation or the distance $d$, requiring no calculation.

**Part C.** Since $\vec E_{\text{net}}=\vec E_{\text{dipole}}+\vec E_{\text{metal}}=\vec 0$, we need $\vec E_{\text{metal}}=-\vec E_{\text{dipole}}(\text{at the sphere's center})$. Because $\hat p\perp\hat r$ exactly, this is the clean **perpendicular-axis** case, at distance $r=|\vec r_s|=d\sqrt2$:

$$|\vec E_{\text{dipole}}| = \frac{kp}{r^3} = \frac{kp}{(d\sqrt2)^3} = \frac{kp}{2\sqrt2\,d^3}$$

directed **antiparallel** to $\hat p$ (the perpendicular-bisector field always opposes $\vec p$; see the derivation in D4), i.e. along $-\hat p = \langle 1/\sqrt2,-1/\sqrt2,0\rangle$:

$$\vec E_{\text{dipole}} = \frac{kp}{2\sqrt2\,d^3}\Big\langle \frac{1}{\sqrt2},-\frac{1}{\sqrt2},0\Big\rangle = \frac{kp}{4d^3}\langle 1,-1,0\rangle$$

Therefore:

$$\boxed{\vec E_{\text{metal}} = -\vec E_{\text{dipole}} = \frac{kp}{4d^3}\langle -1,1,0\rangle,\qquad |\vec E_{\text{metal}}| = \frac{kp}{2\sqrt2\,d^3}\ \ (\text{pointing along } +\hat p)}$$

That is, the metal's own polarization field at the center points in the *same* direction as the original dipole moment $\hat p$ — sensible, since it must exactly cancel a field that pointed opposite to $\hat p$.

**Part D — reorienting to $\hat p' = \langle 1/\sqrt2,1/\sqrt2,0\rangle$.** Now $\hat p' = \hat r$ exactly — the dipole points *straight at* the sphere, making this the **on-axis** case instead of perpendicular.

The net field at the center is *still* zero (Part B's argument never depended on orientation), but the split between $\vec E_{\text{dipole}}$ and $\vec E_{\text{metal}}$ changes. The on-axis field is:

$$|\vec E_{\text{dipole,new}}| = \frac{2kp}{r^3} = \frac{2kp}{2\sqrt2\,d^3} = \frac{kp}{\sqrt2\,d^3}$$

— exactly **double** the perpendicular-case magnitude from Part C (on-axis fields are always twice the perpendicular-axis field, for the same $p$ and $r$) — directed parallel to $\hat p'=\hat r$ (pointing away from the dipole, toward and through the sphere):

$$\vec E_{\text{dipole,new}} = \frac{kp}{2d^3}\langle 1,1,0\rangle \;\Longrightarrow\; \vec E_{\text{metal,new}} = -\vec E_{\text{dipole,new}} = \frac{kp}{2d^3}\langle -1,-1,0\rangle$$

$$\boxed{|\vec E_{\text{metal,new}}| = \frac{kp}{\sqrt2\,d^3} = 2\times|\vec E_{\text{metal,old}}|,\quad\text{now pointing along } -\hat r \text{ (back toward the dipole)}}$$

So reorienting the dipole to point directly at the sphere **doubles the magnitude** of the metal's compensating field (since the bare-dipole field it must cancel also doubled, switching from the perpendicular to the on-axis formula), and its direction rotates from "parallel to the old $\hat p$" to "pointing from the sphere straight back toward the dipole" — a genuinely different direction, not simply a sign flip of the Part C answer.

---

# Quick Answer Key

| Source | Problem | Key result(s) |
|---|---|---|
| S22 T1 | P1 (coding) | `E = k*gold.charge/rmag**2 * rhat`; `F = proton.charge*E`; arrow at proton along `E` |
| S22 T1 | P2.1 | $\vec E_M = \dfrac{kq}{(x_0^2+y_0^2)^{3/2}}\langle -2x_0,0,0\rangle$ |
| S22 T1 | P2.2 | Condition $y_0\gg x_0$; $p=2qx_0$ |
| S22 T1 | P2.3 | $d=\sqrt{x_0^2+y_0^2}$ |
| S22 T1 | P2.4 | $\vec a = -\dfrac{12ekqx_0}{m(x_0^2+y_0^2)^{3/2}}\hat x$ |
| S22 T1 | P3.1 | $\vec p = \dfrac{\alpha kQ}{y_0^2}\langle0,-1\rangle$ |
| S22 T1 | P3.2 | $\vec F = \dfrac{2k^2Q^2\alpha}{y_0^5}\langle0,-1\rangle$ |
| S22 T1 | P3.3 | $\vec F = \dfrac{2k^2Q^2\alpha}{y_0^5}\langle0,1\rangle$ |
| S22 T1 | P3.4 | Second ball at $\langle x_0,-y_0\rangle$ |
| Sp23 T1 | P1 (coding) | Same structure as S22 P1, using `ball`/`particle` |
| Sp23 T1 | P2.1 | $\vec E_{\text{net}} = \dfrac{3\sqrt2\,kQ}{d^2}\langle1,-1,0\rangle$ |
| Sp23 T1 | P2.2 | $\lvert\vec F\rvert = 4.3$ nN |
| Sp23 T1 | P3.1 | $q_B=-Q$ |
| Sp23 T1 | P3.2 | $\vec p = \dfrac{2\alpha kQ}{x_0^2}\hat x$ |
| Sp23 T1 | P3.3 | $\vec F = \dfrac{4\alpha k^2Q^2}{x_0^5}\hat x$ |
| Sp23 T1 | P4 | $\vec E_{\text{net}}=0$ at $A,B,C,D$ (all inside the conductor) |
| Sp24 T1 | P1.1 | $\vec E_{\text{net}} = -\dfrac{kQ}{4d^2}\hat y$ |
| Sp24 T1 | P1.2 | $\vec F = \dfrac{kQe}{4d^2}\hat y$ |
| Sp24 T1 | P1.3 | $q_4$ at $\langle\sqrt3\,d,2d,0\rangle$ |
| Sp24 T1 | P2.2 | $\vec E_{pm} = \dfrac{kQ}{d^2}\hat x$ |
| Sp24 T1 | P2.5 | Field **decreases** when plastic is removed |
| Sp24 T1 | P3.1 | $Q = -\dfrac{mgl^3}{2kqs}$ |
| Sp24 T1 | P3.2 | Force points **right** |
| Sp24 T1 | P3.3 | $Q = \pm\sqrt{\dfrac{mgl^5}{2\alpha k^2}}$ (either sign valid) |
| GPS 1 | P1.A | $\vec F = \langle-3.46,2.59,0\rangle\times10^{-15}$ N |
| GPS 1 | P1.B | $q_3$ at $\langle1.6,-1.2,0\rangle$ m |
| GPS 1 | P2.A | 12 forces |
| GPS 1 | P2.B | Net force $=0$ |
| GPS 1 | P2.C | $\lvert\vec F\rvert = \dfrac{kq^2}{a^2}(\sqrt2+\tfrac12)$ |
| GPS 1 | P2.D | $\lvert\vec E\rvert \approx 4kq/r^2$ |
| GPS 1 | P3.B | $\vec E = \langle1.08,1.44,0\rangle\times10^7$ N/C |
| GPS 1 | P3.D | $\vec F = \langle-75.6,-100.8,0\rangle$ N |
| GPS 1 | P3.F | $\lvert\vec F\rvert = 252$ N |
| GPS 1 | P3.G | $\lvert\vec F\rvert = 31.5$ N |
| GPS 1 | P4 | $\vec E_{\text{net}} = \dfrac{24kqs}{d^3}\hat x$ |
| GPS 2 | P1.C | $s = \dfrac{\pi\epsilon_0mgh^3}{2Qe}$ |
| GPS 2 | P1.D | $\alpha = \dfrac{8\pi^2\epsilon_0^2mgh^5}{Q^2}$ |
| GPS 2 | P2.A | $p_{\text{ind}} = \dfrac{2k\alpha|\vec p|_g}{d^3}$ |
| GPS 2 | P2.B | $\lvert\vec F\rvert = \dfrac{12\alpha k^2|\vec p|_g^2}{d^7}$ |
| GPS 2 | P2.C | $N \approx 8.6\times10^{10}$ dipoles |
| GPS 2 | P3.B | $\vec E_{\text{net}}=0$ |
| GPS 2 | P3.C | $\vec E_{\text{metal}} = \dfrac{kp}{4d^3}\langle-1,1,0\rangle$ |
| GPS 2 | P3.D | Magnitude doubles, direction becomes $-\hat r$ |
