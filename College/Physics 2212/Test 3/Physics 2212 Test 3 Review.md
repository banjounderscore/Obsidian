# Physics 2212 — Test 3 Review (Weeks 8–11)

> [!abstract] Exam at a glance
> **3 problems, symbols only.** 1: $\vec B$ from charges, currents, dipoles. 2: forces and paths of moving charges. 3: force and torque on loops and dipoles.
> No deriving $\vec B$ from current distributions; apply the results. Full explanations: [[Physics 2212 Test 3 Notes]]. Practice: [[Physics 2212 Test 3 Practice Questions]]. ⚠️ = not on the slides but follows from them.

> [!info] Formula sheet
> **✅ on the sheet** · **🧠 memorize** (the sheet names it but doesn't print it) · **✍️ not on the sheet**: write a one-line derivation, since "if a formula you need is not given, you must derive it."
> The sheet writes $\mu_0/4\pi$ for $k_m$ and $\vec\mu$ for $\vec m$, and gives dipole and wire fields as magnitudes only.

---

## Part 0 — Tools

- $|\vec A\times\vec B|=AB\sin\theta$; right-hand rule; $\hat x\times\hat y=\hat z$ (cyclic $+$, reversed $-$); parallel vectors give 0. Component formula ✅.
- $\odot$ out of the page, $\otimes$ into it; with $\hat x$ right and $\hat y$ up, $\hat z$ is out.
- $\vec r=\vec r_{\text{obs}}-\vec r_{\text{source}}$; fields add as vectors 🧠.
- $\mu_0$ = **permeability of free space** (the magnetic constant): a fixed constant that sets how strong magnetic fields are, the way $\epsilon_0$ does for electric fields. $\mu_0=4\pi\times10^{-7}$ T·m/A ✅.
- $k_m=\mu_0/4\pi=10^{-7}$ T·m/A ✅, the magnetic version of $k$. The sheet writes $\mu_0/4\pi$ wherever these notes write $k_m$.

| Symbol | Meaning |
|---|---|
| $\vec B$ | magnetic field (tesla, T) |
| $q$, $e$ | particle's charge (with sign); $e=1.6\times10^{-19}$ C |
| $\vec v$, $v_d$ | particle velocity; drift speed in a wire |
| $\vec r$ | from the source to the observation point |
| $I$, $d\vec\ell$ | current; small piece of wire pointing along $I$ |
| $s$ | perpendicular distance to a wire |
| $L$ | wire or solenoid length |
| $R$, $z$ | ring/arc/orbit radius; distance along a ring's axis |
| $N$, $A$ | number of turns; loop area |
| $\vec m$ (sheet: $\vec\mu$) | magnetic dipole moment, $NIA$ |
| $m$ in $R=mv/qB$, $F=ma$ | **mass** (not the dipole moment) |
| $\vec p$ | electric dipole moment, $q\vec s$ |
| $\theta$ | angle: between $\vec v$ and $\vec B$ in $qvB\sin\theta$; between $\vec m$ and $\vec B$ in $mB\sin\theta$; arc angle (radians) in $k_mI\theta/R$ |
| $\omega$, $T$ | angular frequency; period |

---

## Part I — Magnetic Fields

### 1–2. Moving charge and current pieces

| Source | Formula | Sheet |
|---|---|---|
| Moving charge | $\vec B=k_m\dfrac{q\vec v\times\vec r}{r^3}$ | 🧠 |
| Current piece | $d\vec B=k_m\dfrac{I\,d\vec\ell\times\vec r}{r^3}$ | ✅ ("short wire") |

- $\vec B$ circles the line of motion; $\vec B=0$ on that line.
- $\vec E$ and $\vec B$ of a moving charge are never parallel.
- A charge moving straight at another exerts no magnetic force on it.
- $d\vec\ell$ points along the current, not the electrons.

### 3. Straight wires

| Wire ($s$ = perpendicular distance) | $B$ | Sheet |
|---|---|---|
| Length $L$, on its bisector | $\dfrac{k_mIL}{s\sqrt{s^2+(L/2)^2}}$ | ✅ |
| Infinite ($s\ll L$) | $2k_mI/s$ | ✅ |
| Semi-infinite, beside its end ⚠️ | $k_mI/s$ | ✍️ half of infinite, by symmetry |
| Any segment ⚠️ | $\dfrac{k_mI}{s}(\sin\theta_2-\sin\theta_1)$ | ✍️ integrate the short-wire formula |
| On the wire's own line | $0$ | ✍️ $\Delta\vec\ell\parallel\hat r$ |

- Thumb along $I$, fingers give $\vec B$.
- Finite wire: close up acts infinite; far away acts like a moving point charge ($k_mIL/s^2$).
- Two equal parallel currents: $\vec B=0$ midway. Opposite currents: $8k_mI/d$ midway.
- Current sheet (current $+x$ in $z=0$): $-\hat y$ above, $+\hat y$ below.

### 4. Rings and arcs

| Source | $B$ | Sheet |
|---|---|---|
| Ring, on axis | $\dfrac{2\pi k_mIR^2}{(R^2+z^2)^{3/2}}$ | ✅ |
| Ring, center | $\dfrac{2\pi k_mI}{R}$ | ✅ (set $z=0$) |
| Arc of angle $\theta$, center ⚠️ | $\dfrac{k_mI\theta}{R}$ | ✍️ every piece at distance $R$, $\Delta\vec\ell\perp\hat r$, total length $R\theta$ |

- Fingers along $I$, thumb along $\vec B$; same direction on both sides of the ring.
- Far from a ring: dipole field $2k_m(I\pi R^2)/z^3$ ✅.
- Radial leads add nothing at the center.
- Hairpin (two semi-infinite wires + semicircle): $\dfrac{k_mI}{R}(2+\pi)$.

### 5. Solenoid

- Inside: $B=\dfrac{4\pi k_mNI}{L}=\dfrac{\mu_0NI}{L}$ ✅, uniform, along the axis.
- Outside: a dipole with $M=NIA$.

---

## Part II — Magnetic Dipoles

### 6. Moment

- $|\vec m|=IA$ ✅ ($NIA$ for $N$ turns), any shape; fingers along $I$, thumb along $\vec m$.
- Head = N pole, tail = S pole.
- Counterclockwise as you look → $\vec m$ toward you.
- Bar magnets: aligned electron spins (Fe, Co, Ni); act like a loop with the same $\vec m$ (S → N).

### 7. Dipole field

$$\vec B=k_m\frac{3(\vec m\cdot\hat r)\hat r-\vec m}{r^3}\qquad\text{✍️ not on the sheet}$$

| Where | $\vec B$ | Sheet |
|---|---|---|
| Axis (either side) | $+2k_m\vec m/r^3$, along $\vec m$ | ✅ (magnitude) |
| Equator | $-k_m\vec m/r^3$, opposite $\vec m$, half size | ✅ (magnitude; you add "opposite $\vec m$") |

- Same as the electric dipole ($\vec E$ dipole fields also ✅) with $k\to k_m$, $\vec p\to\vec m$.
- Far-field arrows on the axis point along $\vec m$.
- Two magnets $M\uparrow$: point on magnet 2's axis and magnet 1's equator, distance $d$ each → $+k_mM/d^3\,\hat y$.

### 8. Adding moments

| System | Total moment |
|---|---|
| Solenoid | $NIA$ |
| Toroid | $0$ |
| Loop folded into two $w\times w$ halves | $Iw^2(\hat y+\hat z)$ |
| Stacked rings, same current | $2\vec m$ |
| Stacked rings, opposite currents | $0$, far field weaker but **not** zero |
| Charge $q$ circling with period $T$ | $I=q/T$, $m=IA$ |

---

## Part III — Force on Moving Charges

### 9. Magnetic force

$$\vec F=q\vec E+q\vec v\times\vec B\qquad\text{🧠}$$

- $|q|vB\sin\theta$; zero at rest or along $\vec B$; flip for negative $q$.
- No work → speed constant.
- Electron moving right, $\vec B$ into page → force down.

### 10–11. Circles and helices

Start from the sheet's circular motion $\left|\frac{d\vec p}{dt}\right|_\perp=\frac{mv^2}{R}$ ✅ with $|q|vB$ 🧠. Here **$m$ is the particle's mass**.

| Quantity | Formula | Sheet |
|---|---|---|
| Radius | $R=\dfrac{mv}{\lvert q\rvert B}$ | ✍️ from $\lvert q\rvert vB=mv^2/R$ |
| Angular frequency | $\omega=\dfrac{\lvert q\rvert B}{m}$ (independent of speed) | ✍️ $\omega=v/R$ |
| Period | $T=\dfrac{2\pi m}{\lvert q\rvert B}$ | ✍️ $T=2\pi R/v$ |
| Cyclotron max KE ⚠️ | $\dfrac{q^2B^2R^2}{2m}$ | ✍️ |
| Helix pitch ⚠️ | $\dfrac{2\pi mv_\parallel}{\lvert q\rvert B}$ ($v_\parallel$ unchanged) | ✍️ |

- $\vec B$ into page: positive charges counterclockwise, negative clockwise.

### 12. Trajectories

1. $\vec F$ at entry → the center is that way.
2. $R=mv/|q|B$; from rest through $\Delta V$: $\tfrac12mv^2=|q\Delta V|$ first ($\Delta U=q\Delta V$ ✅, energy conservation 🧠).
3. Geometry → exit point; time = fraction × $T$.

- Proton entering a half-space field (into page) moving right: half circle, exits at $(0,2R)$ moving left, after $\pi m/eB$.
- Velocity selector: $qE=qv_0B$ → $v_0=E/B$ ✍️ (any charge, any mass).

### 13. Hall effect

- $eE_H=ev_dB$ → $E_H=v_dB$; $|\Delta V_H|=v_dBw$ ✍️.

---

## Part IV — Forces and Torques

### 14. Force on a wire

- $\vec F=I\vec\ell\times\vec B$ ✅ ($\Delta\vec F=I\Delta\vec\ell\times\vec B$); general $\int I\,d\vec\ell\times\vec B$.
- Uniform field: closed loop → $\vec F=0$; curved wire = straight wire between its endpoints ⚠️.

### 15. Between wires

- $F/L=2k_mI_1I_2/d$ ✍️ (sheet's $B_{\text{wire}}$ + $\Delta\vec F$); parallel attract, opposite repel.
- Loop beside a wire (near side parallel, distance $d$, sides $a\parallel$, $b\perp$): $F=2k_mI_1I_2a\left(\dfrac1d-\dfrac1{d+b}\right)$ toward the wire; top and bottom cancel.

### 16. Between loops and magnets

N = $+$, S = $-$; closest poles win.

| Arrangement | Result |
|---|---|
| Head to tail ($\uparrow$ above $\uparrow$) | attract |
| Head to head / tail to tail ($\uparrow$ above $\downarrow$) | repel |
| Side by side, parallel ($\uparrow\ \uparrow$) | repel |
| Side by side, antiparallel ($\uparrow\ \downarrow$) | attract |

- ⚠️ ✍️ $\vec F=\nabla(\vec m\cdot\vec B)$: head to tail $6k_mm_1m_2/r^4$, side by side $3k_mm_1m_2/r^4$.

### 17. Torque

- $\vec\tau=\vec m\times\vec B$ ✅, $\tau=mB\sin\theta$ ($\theta$ between $\vec m$ and $\vec B$).
- Uniform field: no net force; torque turns $\vec m$ toward $\vec B$.
- ⚠️ ✍️ $U=-\vec m\cdot\vec B$ (integrate the torque: $\int mB\sin\theta\,d\theta=-mB\cos\theta$): aligned stable, flip costs $2mB$.
- Rectangle: forces $IbB$, lever arms $\tfrac a2\sin\theta$ → $IabB\sin\theta$.
- Same wire as square vs. circle: $m_{\text{circle}}=4IL^2/\pi$; equal torque needs $\sin\theta=\pi/4$.

### 18. Several dipoles

1. Axis or equator? → $\vec B_1$ at 2.
2. $\vec\tau_2=\vec m_2\times\vec B_1$; force from poles.
3. Swap roles.

- Left magnet $\rightarrow$, right magnet $\uparrow$ on its axis: $\tau_L=-k_mm^2/d^3\,\hat z$, $\tau_R=-2k_mm^2/d^3\,\hat z$ → both clockwise, not equal and opposite.

### 19. Electric dipoles

| | Electric | Magnetic |
|---|---|---|
| Torque | $\vec p\times\vec E$ ✍️ (forces $\pm q\vec E$ at the two ends) | $\vec m\times\vec B$ ✅ |
| Energy | $-\vec p\cdot\vec E$ ✍️ | $-\vec m\cdot\vec B$ ✍️ |
| Net force, uniform field | 0 | 0 |

---

## Exam Traps

| Wrong idea | Right concept |
|---|---|
| "$\vec E$ and $\vec B$ of a moving charge can be parallel" | Never: $\vec B\perp\vec r$ |
| "$\vec B$ is largest ahead of a moving charge" | $\vec B=0$ on the line of motion |
| "$d\vec\ell$ points the way the electrons move" | Along the current |
| "Equator field points along $\vec m$" | Opposite $\vec m$, half the axis value |
| "Total moment 0 → no far field" | Weaker, not zero |
| "Toroid has moment $Nm$" | 0 |
| "The magnetic force speeds the particle up" | No work; speed is constant |
| "A faster particle takes longer per orbit" | $T$ doesn't depend on speed |
| "$v_0=B/E$" | $v_0=E/B$ |
| "A closed loop never feels a net force" | Only in a uniform field |
| "Opposite currents attract like opposite charges" | Opposite currents repel |
| "Stacked loops with the same current repel" | Attract |
| "$\theta$ in $mB\sin\theta$ is the angle to the loop's plane" | Angle between $\vec m$ and $\vec B$ |
| "Use the same $q$ in both formulas" | Source's $q$ in $\vec B$, target's $q$ in $\vec F$; flip each negative one |
| "Torques between two magnets are equal and opposite" | Not in general |
| "I can just quote $R=mv/qB$ or the arc formula" | Not on the sheet: derive it in a line first |
| "The sheet's $B_{\text{dipole},\perp}$ gives the direction" | It's a magnitude; equator field points opposite $\vec m$ |
