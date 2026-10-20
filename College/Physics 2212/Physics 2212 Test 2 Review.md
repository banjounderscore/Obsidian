# Physics 2212 — Test 2 Review (Weeks 4–7)

> [!abstract] Exam at a glance
> **3 problems, symbolic only (no numbers, no calculator, no coding). A formula sheet is provided. Process is graded.**
> 1. **Distributed charge**: find $\vec E$ for any geometry
> 2. **Potential difference & potential energy**: constant and non-constant $\vec E$
> 3. **Circuits**: batteries and resistors only
>
> **Not on the test:** magnetism, capacitors. **Power:** fair game, minor.
> Full derivations are in [[Physics 2212 Test 2 Notes]].

> [!info] Formula sheet
> **Memorize:** $\vec F=q\vec E$, point-charge $\vec E$, charge conservation, superposition, energy conservation.
> **Given (✅ below):** $U=qV$, $\Delta V=-\int\vec E\cdot d\vec l$, point-charge $\Delta V$, rod (bisector and close-up), ring, disk, plane, and capacitor fields, all circuit material relations (mobility notation $\bar v=uE$, $\sigma=\lvert q\rvert nu$), $P=I\Delta V$, six integrals.
> **Derive / justify (✍️):** shell, ball, arc, rod on its axis, every continuous-distribution $V$, the loop and junction rules, series/parallel.
> **Rules:** start from sheet formulas unless the problem says *derive*. Solve algebraically (otherwise −80%). Use vector notation. Cross out wrong work. Box answers. Stuck? Invent a symbol and keep going.

---

## 1. Distributed Charge → $\vec E$

### 1.1 Core equations
$$
d\vec E=k\frac{dq}{|\vec r|^3}\vec r,\qquad \vec r=\vec r_{\text{obs}}-\vec r_{\text{source}},\qquad k=\frac1{4\pi\epsilon_0}
$$
Integrate **each component separately**.

### 1.2 $dq$ cheat table
| Shape | $dq$ |
|---|---|
| Rod along $x$ | $\lambda\,dx$ |
| Arc/ring, radius $R$ | $\lambda R\,d\theta$ |
| Disk as rings | $\sigma\,2\pi r\,dr$ |
| Rectangle | $\sigma\,dx\,dy$ |
| Sphere surface as rings | $\sigma\,2\pi R^2\sin\theta\,d\theta$ |
| Ball as shells | $\rho\,4\pi r^2\,dr$ |
| Cylinder surface as rings | $\sigma\,2\pi R\,dz$ |

- **Uniform:** $\lambda=Q/L$ (for an arc, $L=R\Delta\theta$), $\sigma=Q/A$, $\rho=Q/V$.
- **Non-uniform:** keep $\lambda(x)$ inside the integral; the total charge is $Q=\int dq$.

### 1.3 Recipe (write every line; each one earns points)
1. Draw it, set the axes, mark P.
2. Choose a general $dq$ at a general location (coordinates in your integration variable).
3. Write $dq$ using the density.
4. Find $\vec r$ (obs − source) in components.
5. Find $|\vec r|$.
6. Write $d\vec E=k\,dq\,\vec r/|\vec r|^3$ and split it into components.
7. Use symmetry to kill components, and **say why**.
8. Set the limits.
9. Integrate. Only source coordinates are variables; $h,z,d$ are constants.
10. Check units, direction, and the far limit ($\to kQ/d^2$).

### 1.4 Standard results
| Geometry | $\vec E$ | Sheet |
|---|---|---|
| Rod $0\to L$, at $(L+d,0)$ | $\dfrac{kQ}{d(L+d)}\hat x$ | ✍️ |
| Rod $0\to L$, at $(0,h)$ | $E_x=-k\lambda\left(\frac1h-\frac1{\sqrt{L^2+h^2}}\right)$, $E_y=\dfrac{k\lambda L}{h\sqrt{L^2+h^2}}$ | ✍️ |
| Rod, perpendicular bisector | $\dfrac{kQ}{x\sqrt{x^2+(L/2)^2}}$ | ✅ |
| Infinite line / rod close-up | $\dfrac{2k\lambda}{s}\hat s$ | ✅ |
| Arc at center, $\theta_1\to\theta_2$ | $\dfrac{k\lambda}{R}\left\langle-(\sin\theta_2-\sin\theta_1),\ \cos\theta_2-\cos\theta_1\right\rangle$ | ✍️ |
| Quarter circle ($0\to\pi/2$) | $-\dfrac{2kQ}{\pi R^2}(\hat x+\hat y)$ | ✍️ |
| Semicircle ($0\to\pi$) | $-\dfrac{2kQ}{\pi R^2}\hat y$ | ✍️ |
| Ring, on axis | $\dfrac{kQz}{(z^2+R^2)^{3/2}}$ | ✅ |
| Disk, on axis ($z>0$) | $2\pi k\sigma\left(1-\dfrac{z}{\sqrt{z^2+R^2}}\right)$ | ✅ |
| Annulus $a\to R$ | $2\pi k\sigma z\left(\frac1{\sqrt{z^2+a^2}}-\frac1{\sqrt{z^2+R^2}}\right)$ | ✍️ |
| Infinite sheet | $2\pi k\sigma$, uniform, pointing away | ✅ |
| Plates $\pm\sigma$ | $4\pi k\sigma$ between, 0 outside | ✅ |
| Hemisphere shell, at center | $\dfrac{kQ}{2R^2}$, pointing away from the shell | ✍️ |
| Shell | $kQ/r^2$ outside, 0 inside | ✍️ justify (symmetry + far-field) |
| Uniform ball | $kQ/r^2$ outside, $kQr/R^3$ inside | ✍️ justify (enclosed charge) |
| Non-uniform ball | $E=kQ_{\text{enc}}/r^2$, with $Q_{\text{enc}}=\int_0^r\rho\,4\pi r'^2dr'$ | ✍️ |
| Rod with $\lambda=\alpha x$, at $(-d,0)$ | $-k\alpha\left[\ln(1+L/d)-\frac{L}{L+d}\right]\hat x$ | ✍️ |

- $E$ **jumps** across a thin charged surface (disk, sheet, shell); it is continuous for rings and solid balls.
- Superposition shortcuts: a hole is a full shape plus a negative-density piece; sheets add region by region; a shell contributes 0 inside itself.

### 1.5 Integrals
| Integral | Result | Sheet | Shows up in |
|---|---|---|---|
| $\displaystyle\int\frac{dx}{(x^2+a^2)^{3/2}}$ | $\dfrac{x}{a^2\sqrt{x^2+a^2}}$ | ✅ | rod, off the end or on the bisector |
| $\displaystyle\int\frac{x\,dx}{(x^2+a^2)^{3/2}}$ | $-\dfrac{1}{\sqrt{x^2+a^2}}$ | ✅ | rod components, disk, annulus |
| $\displaystyle\int\frac{dx}{x+a}$ | $\ln(x+a)$ | ✅ | potential of a rod, line charge $\Delta V$ |
| $\displaystyle\int\frac{dx}{(x+a)^2}$ | $-\dfrac{1}{x+a}$ | ✅ | rod on its axis |
| $\displaystyle\int\frac{dx}{(x+a)^3}$ | $-\dfrac{1}{2(x+a)^2}$ | ✅ | dipole $\Delta V$ on the axis |
| $\displaystyle\int\frac{a\,dx}{x(x+b)}$ | $\dfrac ab\displaystyle\int\left(\frac1x-\frac1{x+b}\right)dx$ | ✅ | partial fractions |
| $\displaystyle\int a\,dx,\ \int ax\,dx,\ \int ax^2\,dx$ | $ax,\ \tfrac12ax^2,\ \tfrac13ax^3$ | ✅ | non-uniform $\lambda$, total charge $Q$ |
| $\displaystyle\int\frac{dx}{\sqrt{x^2+a^2}}$ | $\ln\!\left(x+\sqrt{x^2+a^2}\right)$ | ✍️ | $V$ of a rod on its bisector |
| $\displaystyle\int\frac{x\,dx}{\sqrt{x^2+a^2}}$ | $\sqrt{x^2+a^2}$ | ✍️ | $V$ of a disk |
| $\displaystyle\int\cos\theta\,d\theta,\ \int\sin\theta\,d\theta$ | $\sin\theta,\ -\cos\theta$ | ✍️ | arcs |
| $\displaystyle\int\sin\theta\cos\theta\,d\theta$ | $\tfrac12\sin^2\theta$ | ✍️ | hemisphere |

Split $\frac{x}{(d+x)^2}=\frac1{d+x}-\frac{d}{(d+x)^2}$ to reduce it to sheet integrals.

An odd integrand over symmetric limits integrates to 0.

### 1.6 Conductors & polarization
- **Conductor in equilibrium:** $\vec E=0$ inside; charge sits on the surface; the whole thing is at one potential $V$; $\vec E\perp$ the surface just outside; an empty cavity has $E=0$.
- **Charge $q$ in the cavity of a shell with net charge $Q$:** inner wall $-q$, outer surface $Q+q$.
- **Insulator:** the field inside is reduced, never zero and never reversed. A neutral object is attracted to a charge.
- $\vec E_{\text{tot}}=\vec E_{\text{ext}}+\vec E_{\text{pol}}$.

---

## 2. Potential & Potential Energy

### 2.1 Core equations
$$
\Delta V=V_f-V_i=-\int_i^f\vec E\cdot d\vec l,\qquad \Delta U=q\Delta V,\qquad \vec E=-\nabla V,\qquad K_i+qV_i=K_f+qV_f
$$

### 2.2 Sign rules
- Along $\vec E$: $\Delta V<0$. Against $\vec E$: $\Delta V>0$. Perpendicular to $\vec E$: $\Delta V=0$.
- $\vec E$ points from high $V$ to low $V$, perpendicular to equipotentials.
- $+q$ speeds up going toward low $V$; $-q$ (an electron) speeds up going toward high $V$.
- $V$ is path-independent; $\oint\vec E\cdot d\vec l=0$.
- $V$ is always continuous.
- $E=0$ does **not** imply $V=0$, and vice versa.

### 2.3 Recipe
1. Find $\vec E$ in **every region** along the path.
2. Choose a path (radial for radial fields).
3. Write $d\vec l=+dr\,\hat r$ and let the limits (start → end) set the direction. **No double negatives.**
4. Integrate region by region, splitting at the boundaries.
5. Sign-check against the direction of $\vec E$.

### 2.4 Results
| Case | $V$ or $\Delta V$ |
|---|---|
| Uniform field | $\Delta V=-\vec E\cdot\Delta\vec r$ |
| Parallel plates | $V_+-V_-=Ed=4\pi k\sigma d$ |
| Same-sign sheets | $\Delta V=0$ between them |
| Metal slab of thickness $t$ in the gap | $\lvert\Delta V\rvert=E(d-t)$ |
| Point charge | $V=kq/r$ |
| Line / coaxial cylinders | $V_b-V_a=-2k\lambda\ln(r_b/r_a)$; $V_a-V_b=2k\lambda\ln(b/a)$ (no $V(\infty)=0$) |
| Shell | $kQ/r$ outside, $kQ/R$ (constant) inside |
| Ball | $kQ/r$ outside, $\dfrac{kQ(3R^2-r^2)}{2R^3}$ inside |
| Ring, on axis | $kQ/\sqrt{z^2+R^2}$ |
| Disk, on axis | $2\pi k\sigma(\sqrt{z^2+R^2}-\lvert z\rvert)$ |
| Rod, on axis $d$ past the end | $k\lambda\ln\frac{L+d}{d}$ |
| Charges / continuous (scalar sum) | $V=\sum kq_i/r_i$, $\ V=k\int dq/\lvert\vec r\rvert$ |

**Concentric shells** ($q_1$ at radius $R_1$, $q_2$ at radius $R_2>R_1$):

| Region | $E$ | $V$ |
|---|---|---|
| $r>R_2$ | $k(q_1+q_2)/r^2$ | $k(q_1+q_2)/r$ |
| $R_1<r<R_2$ | $kq_1/r^2$ | $kq_1/r+kq_2/R_2$ |
| $r<R_1$ | $0$ | $kq_1/R_1+kq_2/R_2$ |

$V(R_1)-V(R_2)=kq_1\left(\dfrac1{R_1}-\dfrac1{R_2}\right)$, which depends only on the inner charge.

### 2.5 Energy
- **Pair:** $U=kq_1q_2/r$. **System:** sum over each pair once.
- **From rest:** $v=\sqrt{2\lvert q\Delta V\rvert/m}$.
- **CRT (electron entering at the − plate, moving toward the + plate):** $v_f=\sqrt{v_0^2+2eEd/m}$.
- **Closest approach (from far away):** $\tfrac12mv_0^2=kq_1q_2/r_{\min}$.

---

## 3. Circuits (Batteries + Resistors)

### 3.1 Physics
- **Current:** $I=dQ/dt=\lvert q\rvert nAv$. Conventional current flows the way + charge moves; electrons drift the opposite way.
- **Steady state:** $\vec E\ne0$ inside the wire, constant in magnitude, produced by charges on the wire's **surface**. Compare equilibrium, where $E=0$.
- **Battery:** EMF $\mathcal E=V_+-V_-$, maintained by chemistry.
- **Drude:** $v_d=e\tau E/m$. More collisions (smaller $\tau$) mean slower drift.
- **Sheet notation ✅:** $\bar v=uE$ (mobility $u=e\tau/m$), $\ \sigma=1/\rho=\lvert q\rvert nu$, $\ J=I/A=\sigma E$, $\ i=nA\bar v$.
- **Conductivity:** $\sigma_c=ne^2\tau/m$, $\rho_c=1/\sigma_c$, $J=\sigma_cE$.
- **Ohm's law:** $\Delta V=IR$, with $R=\rho_cL/A$. $V$ drops along the current through a resistor.
- **Varying cross-section:** $I$ is the same everywhere, so $E=I/(\sigma_cA)$ is larger where the wire is thinner.
- **Power:** $P=I\Delta V=I^2R=\Delta V^2/R$. A battery supplies $\mathcal EI$. Supplied power equals dissipated power.

### 3.2 Kirchhoff
- **Loop rule:** $\sum\Delta V=0$ around any closed loop (energy / path independence).
- **Junction rule:** $\sum I_{\text{in}}=\sum I_{\text{out}}$ (charge conservation).

| You traverse… | $\Delta V$ |
|---|---|
| battery − → + | $+\mathcal E$ |
| battery + → − | $-\mathcal E$ |
| resistor **with** $I$ | $-IR$ |
| resistor **against** $I$ | $+IR$ |

- Current never changes through an element; it only splits at junctions.
- Ideal wire: $\Delta V=0$.

### 3.3 Recipe
1. Label the nodes and the branch currents (guess directions).
2. Junction rule at $n-1$ nodes.
3. Loop rule on independent loops, term by term.
4. Solve. A negative current means the flow is opposite your guess; **keep the sign** when substituting.
5. Check with an unused loop.
6. For $V_B-V_A$, walk any path from A to B using the same sign table.

### 3.4 Results
- **Series:** $R_s=\sum R_i$; same $I$; divider $\Delta V_1=\mathcal E R_1/(R_1+R_2)$.
- **Parallel:** $1/R_p=\sum1/R_i$; same $\Delta V$; two resistors $R_1R_2/(R_1+R_2)$; current divider $I_1=IR_2/(R_1+R_2)$.
- **Opposing batteries in one loop:** $I=(\mathcal E_1-\mathcal E_2)/(R_1+R_2)$.
- **Two-loop circuit**, with branches $\mathcal E_1R_1$ \| $R_3$ \| $\mathcal E_2R_2$ (both + on top; $I_1,I_2$ up, $I_3$ down). Let $D=R_1R_2+R_2R_3+R_1R_3$:
  - Junction: $I_1+I_2=I_3$
  - Loops: $\mathcal E_1-I_1R_1-I_3R_3=0$, $\ \mathcal E_2-I_2R_2-I_3R_3=0$
  - $I_3=\dfrac{\mathcal E_1R_2+\mathcal E_2R_1}{D}$, $\ I_1=\dfrac{\mathcal E_1(R_2+R_3)-\mathcal E_2R_3}{D}$
  - $V_A-V_B=I_3R_3$
- **Identical bulbs:** in series each gets $\mathcal E^2/4R$; in parallel each gets $\mathcal E^2/R$.
- **Short circuit:** no current through the shorted resistor.
- **Adding a resistor in parallel:** total $R$ drops, so battery current rises.

---

## 4. Mistake Checklist
- [ ] $\vec r$ = obs − source; $d\vec E$ points away from a + $dq$
- [ ] Components integrated separately, not magnitudes
- [ ] $dq=\lambda R\,d\theta$ and $\sigma2\pi r\,dr$ (no missing factors)
- [ ] $\lambda$ uses the true length (arc $=R\Delta\theta$)
- [ ] Symmetry claimed only when it really exists
- [ ] $\Delta V$: $d\vec l=+dr\,\hat r$, the limits set the direction, the integral split at boundaries
- [ ] $\Delta U=q\Delta V$, sign flipped for electrons
- [ ] Battery sign from the terminal entered; resistor sign from the current direction
- [ ] Negative currents kept negative
- [ ] Anything not on the sheet (shell, ball, arc, loop rule…) derived or justified in words
- [ ] Vector notation used; wrong work crossed out; answers boxed; sub-parts labeled
- [ ] Stuck on a part? Invent a symbol, say so, and finish the rest
- [ ] Every Gradescope upload prompt filled
