# Physics 2212 — Test 2 Notes (Weeks 4–7)

> [!abstract] What's on Test 2 (and what isn't)
> **Three problems, no numbers, no calculator, no coding.** You get a printed formula sheet. Graders care about your **process** more than the final answer.
>
> | Problem | Topic | Where in these notes |
> |---|---|---|
> | 1 | **Distributed charge**: find $\vec E$ from a continuous charge distribution. Any geometry is allowed (rod, arc, ring, disk, sheet, shell, ball, non-uniform density, 3D shapes) | Parts I–II (§1–§7) |
> | 2 | **Potential difference & potential energy**: $\Delta V=-\int\vec E\cdot d\vec l$ for constant *and* non-constant fields, energy conservation | Part III (§8–§13) |
> | 3 | **Circuits**: batteries and resistors only, using the loop and junction rules | Part IV (§14–§19) |
>
> **NOT on the test (so not in these notes):** magnetism (Lectures 13 second half, 14, 15), capacitance, dielectrics, and capacitors in circuits ("No cap!"). **Power** is "fair game but never a focus," so you get one short section on it (§17).
>
> **Test 1 material** shows up only where Test 2 depends on it. Part 0 is a short prerequisite recap. Part II (conductors and polarization) is included because the instructor's recommended practice list for this test includes it. The full Test 1 material lives in [[Physics 2212 Test 1 Notes]].
>
> **Quick review version:** [[Physics 2212 Test 2 Review]].
>
> **Integrals:** sometimes you only set one up, sometimes you also evaluate it. It depends on the problem, and the GPS problems ask you to do both, so practice both. §5 has the integrals you'll actually meet.

> [!tip] How to use these notes
> They assume you know nothing. Read each part in order the first time. Every formula is derived, because on this exam **the derivation is the answer**. After a section, cover the worked example and redo it on blank paper. Then change one thing (a different observation point, a different geometry) and redo it again. That's exactly the practice the instructor recommends.

> [!info] What the formula sheet gives you (and what it doesn't)
> **Memorize (the sheet lists these as "things you must have memorized"):** $\vec F=q\vec E$; the point-charge field $\vec E=kq\vec r/r^3$; conservation of charge; superposition; Newton's 2nd law; conservation of energy.
>
> **On the sheet (Test 2 relevant):**
> - Potential: $U_E=qV$, $\ \Delta V=-\int_i^f\vec E\cdot d\vec l$, $\ \Delta V=\frac{q}{4\pi\epsilon_0}\left(\frac1{r_f}-\frac1{r_i}\right)$ (point charge)
> - Fields: rod on its perpendicular bisector, rod for $r\ll L$ ($\tfrac{1}{4\pi\epsilon_0}\tfrac{2Q/L}{r}$), ring on axis, disk on axis, infinite plane ($\tfrac{Q/A}{2\epsilon_0}$), capacitor ($\tfrac{Q/A}{\epsilon_0}$), and the dipole fields
> - Circuits: $i=nA\bar v$, $\ I=\lvert q\rvert nA\bar v$, $\ \bar v=uE$ ($u$ = **mobility**), $\ \sigma=1/\rho=\lvert q\rvert nu$, $\ J=I/A=\sigma E$, $\ R=L/(\sigma A)=\rho L/A$, $\ I=\lvert\Delta V\rvert/R$, $\ P=I\Delta V$
> - Six integrals (marked in §5), plus the sphere's $A=4\pi r^2$ and $V=\tfrac43\pi r^3$
>
> **NOT on the sheet, so you must derive or argue them:** shell and ball fields, arc fields, rod on its axis, potentials of continuous distributions (ring, disk, line, shell, ball), the loop and junction rules (from energy and charge conservation), series/parallel resistance, $\int dx/\sqrt{x^2+a^2}$, and trig integrals.
>
> **Official rule:** "Unless specifically asked to derive a result, you can start from the formulas given on the formula sheet… If a formula you need is not given, you must derive it." So when a problem says *derive*, you start from $d\vec E=k\,dq\,\vec r/r^3$ even if the result is on the sheet.
>
> Gauss's law (flux) is printed on the sheet because the sheet is shared across all tests, but it wasn't taught in Weeks 4–7. Use the symmetry + far-field arguments in §4.10 instead.

## Table of Contents
- [[#Part 0 — Prerequisite Recap (from Test 1)]]
- [[#Part I — Electric Field of Continuous Charge Distributions]]
- [[#Part II — Conductors, Insulators, and Superposition Tricks]]
- [[#Part III — Electric Potential, Potential Difference, and Potential Energy]]
- [[#Part IV — Current, Resistance, and Circuits]]
- [[#Part V — Exam Strategy, Common Mistakes, Formula Summary]]

---

# Part 0 — Prerequisite Recap (from Test 1)

## 0.1 Charge, Coulomb's law, and $k$

Electric charge comes in two signs. Like charges repel, unlike charges attract. The charge of a proton is $+e$ and of an electron is $-e$. Charge is **conserved**: it is never created or destroyed, only moved around.

Coulomb's law gives the force that a source charge $q_1$ exerts on charge $q_2$:

$$
\vec F_{1\to 2} = k\frac{q_1q_2}{r^2}\,\hat r, \qquad k=\frac{1}{4\pi\epsilon_0}
$$

Here $\vec r$ points **from the source $q_1$ to the charge feeling the force, $q_2$**, $r=|\vec r|$, and $\hat r=\vec r/r$ is the unit vector in that direction. If $q_1q_2>0$ the force points along $+\hat r$ (repulsion); if $q_1q_2<0$ it points along $-\hat r$ (attraction).

This course writes everything with $k$. If your formula sheet uses $\epsilon_0$, just swap in $k=1/(4\pi\epsilon_0)$; for example, $2\pi k\sigma = \sigma/(2\epsilon_0)$ and $4\pi k\sigma=\sigma/\epsilon_0$.

## 0.2 The electric field

The **electric field** $\vec E(\vec r)$ is the force per unit charge that a test charge would feel at the point $\vec r$:

$$
\vec F = q\,\vec E \qquad\Longleftrightarrow\qquad \vec E = \frac{\vec F}{q}
$$

The field is produced by the **source** charges and exists whether or not a test charge is there. For a single point charge $q$:

$$
\boxed{\ \vec E(\vec r) = k\frac{q}{r^2}\hat r = k\frac{q\,\vec r}{r^3}\ }
$$

where $\vec r$ points **from the source to the observation point**. The second form, $kq\vec r/r^3$, is the one you will use most: it carries the direction automatically inside $\vec r$, so you never have to separately figure out $\hat r$. (Check: $\vec r/r^3 = (r\hat r)/r^3 = \hat r/r^2$.)

- $\vec E$ points **away** from positive charges and **toward** negative charges.
- Units: N/C, which equals V/m.

> [!important] The single most important vector in this whole test
> $$\vec r = \vec r_{\text{obs}} - \vec r_{\text{source}} \qquad \text{("observation minus source")}$$
> Get this right and the direction of every field comes out automatically. Get it backwards and every sign is wrong.

## 0.3 Superposition

The field from many charges is the **vector sum** of the fields from each one separately:

$$
\vec E_{\text{net}} = \vec E_1+\vec E_2+\cdots = \sum_i k\frac{q_i\,\vec r_i}{r_i^3}
$$

"Vector sum" means you add $x$-components to $x$-components, and $y$-components to $y$-components. You **cannot** just add magnitudes unless all the vectors point the same way.

## 0.4 Vectors, magnitudes, unit vectors, dot product

For $\vec r = \langle r_x, r_y, r_z\rangle$:

$$
r=|\vec r|=\sqrt{r_x^2+r_y^2+r_z^2},\qquad \hat r=\frac{\vec r}{r},\qquad \vec A\cdot\vec B = A_xB_x+A_yB_y+A_zB_z = AB\cos\theta
$$

The dot product is a **scalar** (a number). It is positive when the vectors point roughly the same way, zero when they're perpendicular, and negative when they point roughly opposite ways. That sign behavior drives all of Part III.

## 0.5 The binomial approximation (for limiting-case checks)

For $|\epsilon|\ll1$ and any power $n$:

$$
(1+\epsilon)^n\approx 1+n\epsilon
$$

Examples you'll use:
- $\dfrac{1}{\sqrt{1+\epsilon}}=(1+\epsilon)^{-1/2}\approx1-\tfrac12\epsilon$
- $\sqrt{1+\epsilon}\approx1+\tfrac12\epsilon$
- $\ln(1+\epsilon)\approx\epsilon-\tfrac12\epsilon^2$ (Taylor series, needed for some log answers)

**Why:** $(1+\epsilon)^n=1+n\epsilon+\frac{n(n-1)}{2}\epsilon^2+\cdots$, and each term is smaller by another factor of $\epsilon$. (If the first two terms cancel, keep the $\epsilon^2$ term.)

**How:** factor the **big** quantity out so a $1+(\text{small})$ is left. Example, $z\gg R$:
$$\frac{z}{\sqrt{z^2+R^2}}=\frac{z}{z\sqrt{1+R^2/z^2}}=\left(1+\frac{R^2}{z^2}\right)^{-1/2}\approx1-\frac{R^2}{2z^2}$$

You use this to check answers: far from any charged object with net charge $Q$, the field must look like $kQ/r^2$. That is the **far-field theorem**.

---

# Part I — Electric Field of Continuous Charge Distributions

## 1. Why we need integrals

A real object (a rod, a plate, a ball) holds trillions of charges smeared out smoothly. You can't sum $kq_i\vec r_i/r_i^3$ over every electron, so instead:

1. Chop the object into infinitesimally small pieces, each with charge $dq$.
2. Each piece is so small it acts like a **point charge**, producing $d\vec E = k\,dq\,\vec r/r^3$.
3. Add up (integrate) all the little $d\vec E$'s.

$$
\boxed{\ \vec E(\vec r_{\text{obs}}) = \int d\vec E = k\int\frac{\vec r_{\text{obs}}-\vec r_{\text{source}}}{|\vec r_{\text{obs}}-\vec r_{\text{source}}|^3}\,dq\ }
$$

> [!warning] It's a vector integral
> Each $d\vec E$ points in a different direction. You must integrate **each component separately**: $E_x=\int dE_x$, $E_y=\int dE_y$, $E_z=\int dE_z$. Integrating the magnitude $\int|d\vec E|$ is wrong unless every $d\vec E$ points the same way.

## 2. Charge density: converting $dq$ into something you can integrate

You can't integrate "$dq$" directly. You have to write it as (density) × (a small length, area, or volume) expressed in coordinates.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\fill[cneg,fill opacity=0.12] (0,0) rectangle (2.5,2.5);
\draw (0,0) rectangle (2.5,2.5);
\foreach \p in {(0.67,0.38),(1.02,0.49),(0.30,1.03),(2.17,1.91),(1.83,0.64),(1.33,0.76),(0.53,0.38),(0.62,2.19),(1.97,1.92),(1.91,0.58),(0.83,1.53),(1.76,2.03),(2.09,0.34),(1.48,1.63),(1.26,0.54),(1.19,0.35),(2.21,2.05),(1.35,0.81),(2.15,1.41),(2.09,2.02),(1.27,1.06),(1.47,1.10),(0.50,0.82),(1.94,0.25),(0.25,1.53),(0.77,1.33),(1.19,0.90),(2.34,0.58),(1.06,0.60),(1.54,0.76)} \fill[cneg] \p circle (1.5pt);
\node at (1.25,3) {volume};
\node at (1.25,-0.6) {$\rho=\Delta q/\Delta V$};
\begin{scope}[xshift=5.5cm,yshift=1.25cm]
\fill[corg,fill opacity=0.15] (0,0) ellipse (1.5 and 0.85);
\draw (0,0) ellipse (1.5 and 0.85);
\foreach \p in {(-0.43,0.42),(-0.54,0.10),(0.80,0.20),(-0.79,-0.29),(-0.97,-0.07),(-0.27,0.75),(0.36,0.54),(-0.62,-0.52),(-0.17,-0.62),(0.85,-0.23),(-0.63,-0.68),(0.53,-0.60),(-1.38,-0.02),(-1.13,0.05),(0.82,-0.15),(-0.77,-0.15),(0.99,-0.00),(-0.77,-0.50),(-0.81,0.63),(1.28,0.11),(1.20,0.26),(0.87,0.42)} \fill[corg] \p circle (1.5pt);
\node at (0,1.75) {surface};
\node at (0,-1.85) {$\sigma=\Delta q/\Delta A$};
\end{scope}
\begin{scope}[xshift=8.5cm,yshift=1.25cm]
\draw[line width=3pt,cacc] (0,0)--(3,0);
\foreach \x in {0.15,0.45,...,2.9} \fill (\x,0) circle (1.5pt);
\node at (1.5,1.75) {line};
\node at (1.5,-1.85) {$\lambda=\Delta q/\Delta\ell$};
\end{scope}
\end{tikzpicture}
\end{document}
```

| Dimension | Density | Definition | $dq=$ | Uniform case |
|---|---|---|---|---|
| 1D (line, rod, arc, ring) | $\lambda$ (lambda), C/m | charge per length | $\lambda\,dl$ | $\lambda=Q/L$ |
| 2D (sheet, disk, shell surface) | $\sigma$ (sigma), C/m² | charge per area | $\sigma\,dA$ | $\sigma=Q/A$ |
| 3D (ball, cylinder, cube) | $\rho$ (rho), C/m³ | charge per volume | $\rho\,dV$ | $\rho=Q/V$ |

### 2.1 The $dl$, $dA$, $dV$ you need, by geometry

Memorize *how to get* these, not just the results. Each one is "how much length/area/volume do I sweep out when I nudge my coordinate by a tiny amount?"

| Geometry | Coordinate | Small piece | $dq$ |
|---|---|---|---|
| Straight rod along $x$ | $x$ | $dl=dx$ | $\lambda\,dx$ |
| Arc / ring of radius $R$ | angle $\theta$ | arc length $dl=R\,d\theta$ | $\lambda R\,d\theta$ |
| Disk / annulus (rings of radius $r$) | $r$ | ring area $dA=2\pi r\,dr$ (circumference × width) | $\sigma\,2\pi r\,dr$ |
| Flat rectangle | $x,y$ | $dA=dx\,dy$ | $\sigma\,dx\,dy$ |
| Thin rectangular strip of width $dx$, height $h$ | $x$ | $dA=h\,dx$ | $\sigma h\,dx$ |
| Spherical surface, radius $R$, cut into rings at polar angle $\theta$ | $\theta$ | ring radius $R\sin\theta$, width $R\,d\theta$, so $dA=2\pi R^2\sin\theta\,d\theta$ | $\sigma\,2\pi R^2\sin\theta\,d\theta$ |
| Solid ball cut into shells | $r$ | shell volume $dV=4\pi r^2\,dr$ (area × thickness) | $\rho\,4\pi r^2\,dr$ |
| Solid cylinder cut into cylindrical shells | $r$ | $dV=2\pi r L\,dr$ | $\rho\,2\pi rL\,dr$ |
| Cylindrical surface cut into rings along its axis | $z$ | $dA=2\pi R\,dz$ | $\sigma\,2\pi R\,dz$ |

### 2.2 Non-uniform densities

Sometimes the density varies, e.g. $\lambda(x)=\alpha x$ or $\sigma(r)=\beta r$. Then:

- $dq=\lambda(x)\,dx$, and the $x$-dependence of $\lambda$ goes **inside the integral**.
- The total charge is no longer "density × length". You have to integrate: $Q=\int\lambda(x)\,dx$.
- Watch the units of the constant. If $\lambda=\alpha x$ has units C/m, then $\alpha$ has units C/m².

**Example.** A rod from $x=0$ to $x=L$ has $\lambda(x)=\alpha x$. Its total charge is
$$Q=\int_0^L\alpha x\,dx=\frac{\alpha L^2}{2}\quad\Longrightarrow\quad\alpha=\frac{2Q}{L^2}.$$

**Example.** A disk of radius $R$ has $\sigma(r)=\beta r$. Its total charge is
$$Q=\int_0^R\beta r\cdot2\pi r\,dr=\frac{2\pi\beta R^3}{3}.$$

## 3. THE RECIPE (use it every single time)

This is what the graders want to see written out, step by step. Practice-exam rubrics award points for each of these lines separately, often before you even reach the integral.

> [!example] The distributed-charge recipe
> 1. **Draw** the object, the axes, and the observation point P. Pick the origin to make things simple: usually at a center of symmetry, or with the object along an axis.
> 2. **Pick a tiny piece $dq$** at a *general* location (not a special one like an endpoint). Label its coordinates in terms of your integration variable, e.g. $(x,0,0)$ or $(R\cos\theta,R\sin\theta,0)$.
> 3. **Write $dq$** using the density: $dq=\lambda\,dx$, $\lambda R\,d\theta$, $\sigma\,2\pi r\,dr$, …
> 4. **Write the separation vector** $\vec r=\vec r_{\text{obs}}-\vec r_{\text{source}}$ in components.
> 5. **Find its magnitude** $|\vec r|$.
> 6. **Write $d\vec E$**:
>   $$d\vec E = k\frac{dq}{|\vec r|^3}\,\vec r$$
>   and split it into components $dE_x, dE_y, dE_z$.
> 7. **Use symmetry** to argue that some components integrate to zero. *Say why in words* ("for every $dq$ at $+y$ there's a matching one at $-y$ whose $dE_y$ cancels").
> 8. **Set limits** from where the object starts and ends in your coordinate.
> 9. **Integrate** each surviving component.
> 10. **Check**: units ($k\times$charge/length² is a field), direction (does it point away from + charge?), and a limiting case (far away it must become $kQ/d^2$).

> [!tip] Constants out, variables in
> Before integrating, pull every constant outside the integral ($k$, $\lambda$, the observation coordinates like $h$ or $z$). Leave only the integration variable inside. Then the integral usually matches a standard form (§5).

## 4. Worked examples: the standard geometries

### 4.1 Finite rod, observation point on its axis (beyond the end)

**Setup.** A rod of length $L$ and charge $Q$ (uniform, $\lambda=Q/L$) lies on the $x$-axis from $x=0$ to $x=L$. Find $\vec E$ at P $=(L+d,\,0)$, a distance $d$ past the right end.

1. Piece at $(x,0)$ with $dq=\lambda\,dx$.
2. $\vec r = \langle L+d,0\rangle-\langle x,0\rangle=\langle L+d-x,\ 0\rangle$, so $|\vec r|=L+d-x$ (positive, since $x\le L$).
3. Every piece pushes P in the $+x$ direction, so there are no components to cancel:
$$
dE_x = k\frac{\lambda\,dx}{(L+d-x)^3}(L+d-x)=k\frac{\lambda\,dx}{(L+d-x)^2}
$$
4. Integrate over the rod, $x=0\to L$. **Antiderivative:** substitute $u=L+d-x$, so $du=-dx$ and $\int\frac{dx}{(L+d-x)^2}=\int\frac{-du}{u^2}=+\frac1u=\frac{1}{L+d-x}$. (The minus from $du=-dx$ cancels the minus from $\int u^{-2}du=-1/u$.) Then plug in the limits:
$$
E_x=k\lambda\int_0^L\frac{dx}{(L+d-x)^2}=k\lambda\left[\frac{1}{L+d-x}\right]_0^L=k\lambda\left(\frac1d-\frac1{L+d}\right)=k\lambda\frac{L}{d(L+d)}
$$
$$
\boxed{\vec E=\frac{kQ}{d(L+d)}\,\hat x}
$$
5. **Check.** Far away ($d\gg L$): $d(L+d)\approx d^2$, so $E\to kQ/d^2$ ✓ (far-field theorem).

### 4.2 Finite rod, observation point NOT symmetric (the general case)

This is the "no symmetry" version. Both components survive, and you have to do both integrals.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[->,cgry] (-0.6,0)--(6.4,0) node[right]{$x$};
\draw[->,cgry] (0,-0.6)--(0,4) node[above]{$y$};
\draw[line width=4pt,corg] (0,0)--(5,0);
\node[below] at (5,-0.15) {$L$};
\node[below left] at (0,0) {$0$};
\fill[cpos] (2.85,-0.13) rectangle (3.15,0.13);
\node[below] at (3,-0.2) {$dq=\lambda\,dx$ at $(x,0)$};
\draw[vec,cneg] (3,0)--(0,3) node[pos=0.45,above right]{$\vec r=\langle -x,h\rangle$};
\fill (0,3) circle (2.5pt) node[left]{$P=(0,h)$};
\end{tikzpicture}
\end{document}
```

**Setup.** A rod from $x=0$ to $x=L$ with uniform $\lambda=Q/L$. Find $\vec E$ at P $=(0,h)$, directly above the left end.

1. $dq=\lambda\,dx$ at $(x,0)$.
2. $\vec r=\langle0,h\rangle-\langle x,0\rangle=\langle -x,\ h\rangle$, and $|\vec r|=\sqrt{x^2+h^2}$.
3. Write the field from one piece:
$$
d\vec E = k\frac{\lambda\,dx}{(x^2+h^2)^{3/2}}\langle -x,\ h\rangle
$$
4. **$x$-component** (negative, because the rod is to the right of P and pushes it left):
$$
E_x=-k\lambda\int_0^L\frac{x\,dx}{(x^2+h^2)^{3/2}}=-k\lambda\left[-\frac{1}{\sqrt{x^2+h^2}}\right]_0^L=-k\lambda\left(\frac1h-\frac1{\sqrt{L^2+h^2}}\right)
$$
5. **$y$-component**:
$$
E_y=k\lambda h\int_0^L\frac{dx}{(x^2+h^2)^{3/2}}=k\lambda h\left[\frac{x}{h^2\sqrt{x^2+h^2}}\right]_0^L=\frac{k\lambda L}{h\sqrt{L^2+h^2}}
$$
6. **Check.** As $h\gg L$: $\sqrt{L^2+h^2}\approx h$, so $E_y\to k\lambda L/h^2=kQ/h^2$ ✓. For $E_x$, factor out $h$ and use the binomial approximation: $\frac1h-\frac{1}{\sqrt{L^2+h^2}}=\frac1h\left[1-\left(1+\frac{L^2}{h^2}\right)^{-1/2}\right]\approx\frac1h\cdot\frac{L^2}{2h^2}$. So $E_x\approx-\frac{k\lambda L^2}{2h^3}$, which shrinks like $1/h^3$, faster than $E_y$. The field becomes purely "up", as it should when the rod looks like a point charge directly below.

### 4.3 Finite rod, observation point on its perpendicular bisector

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[->,cgry] (-1.2,0)--(6.3,0) node[right]{$x$};
\draw[->,cgry] (0,-3)--(0,3.4) node[above]{$y$};
\draw[line width=4pt,corg] (0,-2.5)--(0,2.5);
\draw[vec,cneg] (0,1.5)--(4,0) node[pos=0.45,above right]{$\vec r=\langle x,-y\rangle$};
\draw[vec,cacc] (4,0)--(5.5,-0.56) node[right]{$d\vec E$};
\draw[vec,cacc,dashed,opacity=0.55] (4,0)--(5.5,0.56) node[right]{\small from the piece at $-y$};
\fill[cpos] (-0.13,1.35) rectangle (0.13,1.65);
\node[left] at (-0.2,1.5) {$dq=\lambda\,dy$};
\fill[cpos,opacity=0.5] (-0.13,-1.65) rectangle (0.13,-1.35);
\fill (4,0) circle (2.5pt) node[below]{$P=(x,0)$};
\draw[dim] (-0.9,0)--(-0.9,-2.5) node[midway,left]{$L/2$};
\end{tikzpicture}
\end{document}
```

**Setup.** A rod along the $y$-axis from $-L/2$ to $+L/2$, uniform $\lambda=Q/L$. P $=(x,0)$.

1. $dq=\lambda\,dy$ at $(0,y)$. $\vec r=\langle x,-y\rangle$, $|\vec r|=\sqrt{x^2+y^2}$.
2. $d\vec E=k\lambda\,dy\,\dfrac{\langle x,-y\rangle}{(x^2+y^2)^{3/2}}$.
3. **Symmetry:** the piece at $+y$ and the piece at $-y$ have equal $dE_x$ but opposite $dE_y$. Mathematically, the $E_y$ integrand $-y/(x^2+y^2)^{3/2}$ is an **odd function** integrated over symmetric limits, so $E_y=0$.
4. Then integrate $E_x$:
$$
E_x=k\lambda x\int_{-L/2}^{L/2}\frac{dy}{(x^2+y^2)^{3/2}}=k\lambda x\left[\frac{y}{x^2\sqrt{x^2+y^2}}\right]_{-L/2}^{L/2}
$$
Plugging in the limits: the top limit gives $\frac{L/2}{x^2\sqrt{x^2+L^2/4}}$, and subtracting the bottom limit subtracts $\frac{-L/2}{x^2\sqrt{x^2+L^2/4}}$, so the two halves add to $\frac{L}{x^2\sqrt{x^2+L^2/4}}$. Multiply by $k\lambda x$ (one $x$ cancels):
$$
E_x=\frac{k\lambda L}{x\sqrt{x^2+(L/2)^2}}
$$
$$
\boxed{\vec E(x,0)=\frac{kQ}{x\sqrt{x^2+(L/2)^2}}\,\hat x}
$$

```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\begin{axis}[width=9cm,height=6cm,axis lines=left,xmin=0,xmax=2.5,ymin=0,ymax=15,
xlabel={$x$ (units of $L$)},ylabel={$E_x$ (units of $kq/L^2$)},
legend style={draw=none,fill=none,font=\small},legend pos=north east]
\addplot[very thick,domain=0.066:2.5,samples=160]{1/(x*sqrt(x^2+0.25))};
\addlegendentry{exact: $\frac{kq}{x\sqrt{x^2+(L/2)^2}}$}
\addplot[very thick,dashed,cacc,domain=0.259:2.5,samples=120]{1/x^2};
\addlegendentry{far field: $kq/x^2$}
\end{axis}
\end{tikzpicture}
\end{document}
```

**Limits:**
- Far ($x\gg L$): $E\to kQ/x^2$ ✓.
- Close ($x\ll L$): $\sqrt{x^2+L^2/4}\approx L/2$, so $E\to\dfrac{kQ}{x(L/2)}=\dfrac{2k\lambda}{x}$. That is the field of an infinite line (next).

### 4.4 Infinite line of charge

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\node at (0,2.9) {side view};
\draw[line width=4pt,corg] (0,-2.2)--(0,2.2);
\foreach \y in {-1.6,-0.8,0,0.8,1.6} {\draw[-{Stealth[length=2.5mm]},thick,cgry] (0.25,\y)--(1.9,\y); \draw[-{Stealth[length=2.5mm]},thick,cgry] (-0.25,\y)--(-1.9,\y);}
\begin{scope}[xshift=6cm]
\node at (0,2.9) {end view (line out of page)};
\foreach \a in {0,30,...,330} \draw[-{Stealth[length=2.5mm]},thick,cgry] (\a:0.35)--(\a:1.9);
\fill[corg] (0,0) circle (0.18);
\end{scope}
\node at (3,-2.9) {$\vec E=\frac{2k\lambda}{s}\,\hat s$ (points straight away from the line)};
\end{tikzpicture}
\end{document}
```

$$
\boxed{\ \vec E=\frac{2k\lambda}{s}\,\hat s\ }
$$

Here $s$ is the perpendicular distance from the line and $\hat s$ points radially away from it. Notice the field falls as $1/s$, not $1/s^2$. Symmetry tells you it can only point radially: an infinite line looks the same if you slide along it or rotate around it.

### 4.5 Arc of charge, field at the center (polar coordinates)

This is a favorite exam geometry: quarter circles, semicircles, arbitrary arcs.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[->,cgry] (-0.6,0)--(4.4,0) node[right]{$x$};
\draw[->,cgry] (0,-0.6)--(0,4.2) node[above]{$y$};
\draw[line width=4pt,corg] (3.5,0) arc (0:90:3.5);
\draw[dashed,cgry] (0,0)--(50:3.5);
\draw[vec,cneg] (50:3.5)--(50:0.2) node[pos=0.4,above left]{$\vec r=\langle-R\cos\theta,-R\sin\theta\rangle$};
\fill[cpos] (50:3.5) circle (4pt);
\node[right] at (50:3.65) {$dq=\lambda R\,d\theta$};
\draw (1,0) arc (0:50:1);
\node at (25:1.35) {$\theta$};
\fill (0,0) circle (2.5pt) node[below left]{P};
\node[below] at (3.5,-0.1) {$R$};
\end{tikzpicture}
\end{document}
```

**Setup.** An arc of radius $R$ centered on the origin, from angle $\theta_1$ to $\theta_2$, total charge $Q$. The uniform density is $\lambda=\dfrac{Q}{R(\theta_2-\theta_1)}$ (charge ÷ arc length). Find $\vec E$ at the origin.

1. $dq=\lambda R\,d\theta$ at $(R\cos\theta,\ R\sin\theta)$.
2. $\vec r=\vec 0-\langle R\cos\theta,R\sin\theta\rangle=\langle-R\cos\theta,\,-R\sin\theta\rangle$, and $|\vec r|=R$ (constant, which is the nice part).
3. Field from one piece:
$$
d\vec E=k\frac{\lambda R\,d\theta}{R^3}\langle -R\cos\theta,-R\sin\theta\rangle=\frac{k\lambda}{R}\langle-\cos\theta,\,-\sin\theta\rangle\,d\theta
$$
4. Integrate each component:
$$
E_x=-\frac{k\lambda}{R}\int_{\theta_1}^{\theta_2}\cos\theta\,d\theta=-\frac{k\lambda}{R}(\sin\theta_2-\sin\theta_1),\qquad E_y=-\frac{k\lambda}{R}\int_{\theta_1}^{\theta_2}\sin\theta\,d\theta=\frac{k\lambda}{R}(\cos\theta_2-\cos\theta_1)
$$

**Quarter circle** ($0\to\pi/2$, so $\lambda=2Q/\pi R$):
$$E_x=-\frac{k\lambda}{R},\quad E_y=-\frac{k\lambda}{R}\quad\Longrightarrow\quad\vec E=-\frac{2kQ}{\pi R^2}(\hat x+\hat y)$$
That points toward the lower-left, i.e. away from the arc, as expected for $Q>0$.

**Semicircle** ($0\to\pi$, so $\lambda=Q/\pi R$):
$$E_x=0\ \text{(symmetry)},\qquad E_y=-\frac{2k\lambda}{R}=-\frac{2kQ}{\pi R^2}$$

**Full ring** ($0\to2\pi$): $\vec E=0$ at the center ✓. Every piece is cancelled by the opposite piece.

> [!warning] Common arc mistakes
> - $dq=\lambda\,d\theta$ is **wrong**. Arc length is $R\,d\theta$, so $dq=\lambda R\,d\theta$.
> - $\lambda=Q/(2\pi R)$ only for a full ring. For a quarter circle, the arc length is $\pi R/2$.
> - The "$\langle\cos,\sin\rangle$" pattern depends on where you measure $\theta$ from. If the arc is in a different quadrant or $\theta$ is measured from the $y$-axis, **redraw and recompute** the source coordinates. Don't copy formulas.

### 4.6 Ring of charge, on its axis

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[dashed,cgry] (0,-1.2)--(0,0);
\draw[->,cgry] (0,0)--(0,5) node[above]{$z$};
\draw[corg,line width=2.5pt] (0,0) ellipse (2.6 and 0.8);
\draw[dim] (0,0)--(2.6,0) node[midway,above]{$R$};
\draw[dim] (-0.5,0)--(-0.5,3.6) node[midway,left]{$z$};
\draw[vec,cneg] (2.252,-0.4)--(0,3.6) node[pos=0.45,right]{$\vec r$};
\fill[cpos] (2.252,-0.4) circle (3.5pt) node[below right]{$dq=\lambda R\,d\phi$};
\draw[vec,cacc] (0,3.6)--(-0.64,4.73) node[left]{$d\vec E$};
\draw[dashed,cacc] (-0.64,4.73)--(0,4.73);
\fill (0,3.6) circle (2.5pt) node[right]{P};
\node[font=\small,align=left] at (4.3,3.4) {sideways parts cancel\\with the opposite piece;\\only $dE_z$ survives};
\end{tikzpicture}
\end{document}
```

**Setup.** A ring of radius $R$ and charge $Q$ in the $xy$-plane, centered on the origin. Find $\vec E$ at $(0,0,z)$.

1. $dq=\lambda R\,d\phi$ with $\lambda=Q/2\pi R$, located at $(R\cos\phi,R\sin\phi,0)$.
2. $\vec r=\langle-R\cos\phi,\,-R\sin\phi,\,z\rangle$, $|\vec r|=\sqrt{R^2+z^2}$ (the same for every piece).
3. The $x$- and $y$-components involve $\int_0^{2\pi}\cos\phi\,d\phi=\int_0^{2\pi}\sin\phi\,d\phi=0$. They cancel by symmetry: opposite sides of the ring push sideways in opposite directions.
4. That leaves the $z$-component. From $d\vec E=k\,dq\,\vec r/|\vec r|^3$, the $z$-part uses $r_z=z$, so $dE_z=\dfrac{k\,dq\,z}{(R^2+z^2)^{3/2}}$. Everything except $dq$ is the same for every piece, so it comes outside the integral, and $\int dq=Q$ (adding up every piece's charge gives the total):
$$
E_z=k\frac{z}{(R^2+z^2)^{3/2}}\int dq=\boxed{\ \frac{kQz}{(z^2+R^2)^{3/2}}\ }
$$

```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\begin{axis}[width=9cm,height=6cm,axis lines=left,xmin=-6.5,xmax=6.5,ymin=-0.45,ymax=0.45,
xlabel={$z$ (units of $R$)},ylabel={$E_z$ (units of $kq/R^2$)},ytick={-0.4,-0.2,0,0.2,0.4}]
\addplot[cgry,domain=-6.5:6.5] {0};
\addplot[very thick,domain=-6:6,samples=200]{x/(x^2+1)^1.5};
\end{axis}
\end{tikzpicture}
\end{document}
```

- $E=0$ at the center ($z=0$) ✓.
- Far away: $E\to kQ/z^2$ ✓.
- $E$ is continuous everywhere, because a ring is a curve, not a surface you pass through.

### 4.7 Disk of charge, on its axis (build from rings)

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\foreach \r in {0.5,1,1.5,2.5} \draw[corg,opacity=0.55] (0,0) ellipse ({\r} and {0.3*\r});
\draw[corg,line width=2pt] (0,0) ellipse (3 and 0.9);
\fill[corg,fill opacity=0.35,even odd rule] (0,0) ellipse (2.25 and 0.675) (0,0) ellipse (1.95 and 0.585);
\draw[corg!70!black,thick] (0,0) ellipse (2.25 and 0.675) (0,0) ellipse (1.95 and 0.585);
\draw[->,cgry] (0,0)--(0,4.2) node[above]{$z$};
\fill (0,3.5) circle (2.5pt) node[right]{P};
\draw[dim] (0,0)--(2.1,0) node[midway,above]{$r$};
\draw[dim] (0,-1.15)--(3,-1.15) node[midway,below]{$R$};
\draw[dashed,cgry] (3,0)--(3,-1.2);
\node[right,font=\small] at (3.1,0.3) {ring: width $dr$, $dq=\sigma\,2\pi r\,dr$};
\end{tikzpicture}
\end{document}
```

**Setup.** A disk of radius $R$ with uniform $\sigma=Q/\pi R^2$. Find $\vec E$ at $(0,0,z)$.

**Strategy:** you already know the field of a ring (§4.6). Treat the disk as nested rings of radius $r$ and width $dr$.

1. The ring of radius $r$ has charge $dq=\sigma\,dA=\sigma\,2\pi r\,dr$.
2. Use the ring result with $Q\to dq$ and $R\to r$:
$$
dE_z=\frac{k\,dq\,z}{(z^2+r^2)^{3/2}}=\frac{2\pi k\sigma z\,r\,dr}{(z^2+r^2)^{3/2}}
$$
3. Integrate $r=0\to R$ (substitute $u=z^2+r^2$, $du=2r\,dr$):
$$
E_z=2\pi k\sigma z\int_0^R\frac{r\,dr}{(z^2+r^2)^{3/2}}=2\pi k\sigma z\left[-\frac{1}{\sqrt{z^2+r^2}}\right]_0^R
$$
$$
\boxed{\ E_z=2\pi k\sigma\left(\frac{z}{|z|}-\frac{z}{\sqrt{z^2+R^2}}\right)\ }
$$
**Where $z/|z|$ comes from:** at the lower limit $r=0$, the bracket is $-\frac{1}{\sqrt{z^2}}$, and $\sqrt{z^2}=|z|$ (a square root is never negative). Subtracting the lower limit gives $+\frac{1}{|z|}$, and multiplying by the $z$ out front gives $\frac{z}{|z|}$. That's just the sign of $z$: $+1$ above the disk, $-1$ below. (For $z>0$ the result is $2\pi k\sigma\left(1-\dfrac{z}{\sqrt{z^2+R^2}}\right)$.)

```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\begin{axis}[name=E,width=7.5cm,height=6cm,axis lines=left,xmin=-4.3,xmax=4.3,ymin=-1.25,ymax=1.25,
xlabel={$z/R$},ylabel={$E_z\ (2\pi k\sigma)$},title={$E_z$ jumps at $z=0$}]
\addplot[cgry,domain=-4.3:4.3] {0};
\addplot[very thick,domain=0.002:4,samples=120]{1-x/sqrt(x^2+1)};
\addplot[very thick,domain=-4:-0.002,samples=120]{-1-x/sqrt(x^2+1)};
\addplot[only marks,mark=o,mark size=2.5pt,thick] coordinates {(0,1) (0,-1)};
\end{axis}
\begin{axis}[at={(E.outer east)},anchor=outer west,xshift=0.6cm,width=7.5cm,height=6cm,axis lines=left,xmin=-4.3,xmax=4.3,ymin=0,ymax=1.15,
xlabel={$z/R$},ylabel={$V\ (2\pi k\sigma R)$},title={$V$ is continuous (kinked)}]
\addplot[very thick,cacc,domain=-4:4,samples=201]{sqrt(x^2+1)-abs(x)};
\end{axis}
\end{tikzpicture}
\end{document}
```

- **$E$ jumps** from $-2\pi k\sigma$ to $+2\pi k\sigma$ as you pass through the disk. $E$ is always discontinuous across an infinitely thin charged surface.
- Far away, use the binomial expansion: $\dfrac{z}{\sqrt{z^2+R^2}}=\left(1+\dfrac{R^2}{z^2}\right)^{-1/2}\approx1-\dfrac{R^2}{2z^2}$. So $E\approx2\pi k\sigma\dfrac{R^2}{2z^2}=\dfrac{k(\sigma\pi R^2)}{z^2}=\dfrac{kQ}{z^2}$ ✓.

**Annulus (disk with a hole of radius $a$):** same integral but with limits $r=a\to R$:
$$E_z=2\pi k\sigma z\left(\frac1{\sqrt{z^2+a^2}}-\frac1{\sqrt{z^2+R^2}}\right)$$

### 4.8 Infinite sheet (the $R\to\infty$ limit of the disk)

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[line width=4pt,corg] (-3,0)--(3,0);
\node[cpos,right] at (3.1,0) {$+\sigma$};
\foreach \x in {-2.5,-1.5,...,2.5} {\draw[-{Stealth[length=2.5mm]},thick,cgry] (\x,0.2)--(\x,1.8); \draw[-{Stealth[length=2.5mm]},thick,cgry] (\x,-0.2)--(\x,-1.8);}
\node at (0,2.3) {$E=2\pi k\sigma$ (same at every distance)};
\node at (0,-2.3) {$E=2\pi k\sigma$};
\end{tikzpicture}
\end{document}
```

Let $R\to\infty$ in the disk result. The second term $\frac{z}{\sqrt{z^2+R^2}}$ goes to zero, because its denominator grows without limit while the top stays fixed. Only $\frac{z}{|z|}=\pm1$ survives:
$$
\boxed{\ |\vec E|=2\pi k\sigma=\frac{\sigma}{2\epsilon_0}\ }\quad\text{pointing away from the sheet (if }\sigma>0\text{) on both sides}
$$

**It doesn't depend on distance.** A sheet's field is uniform.

### 4.9 Two parallel sheets / parallel-plate capacitor

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\fill[cpos] (-0.12,0) rectangle (0.12,4);
\fill[cneg] (2.88,0) rectangle (3.12,4);
\node[cpos] at (0,4.45) {$+\sigma$};
\node[cneg] at (3,4.45) {$-\sigma$};
\foreach \y in {0.5,1.25,...,3.5} \draw[-{Stealth[length=2.5mm]},thick] (0.3,\y)--(2.7,\y);
\node[cgry] at (-1.3,2) {$E=0$};
\node[cgry] at (4.3,2) {$E=0$};
\draw[dim] (0,-0.4)--(3,-0.4) node[midway,below]{$d$};
\node at (1.5,-1.3) {$E_{\rm in}=4\pi k\sigma=\sigma/\epsilon_0$ (uniform)};
\end{tikzpicture}
\end{document}
```

Put sheet $+\sigma$ on the left and $-\sigma$ on the right. Each makes a field of magnitude $2\pi k\sigma$:
- **Between** the sheets, both fields point from $+$ toward $-$, so they **add**: $E_{\text{in}}=4\pi k\sigma=\sigma/\epsilon_0$, uniform.
- **Outside** the sheets, the fields point in opposite directions and **cancel**: $E_{\text{out}}=0$.

If both sheets have the **same** sign $+\sigma$: the fields cancel between them ($E=0$) and add outside ($4\pi k\sigma$, pointing outward).

### 4.10 Spherical shell and solid ball (symmetry results, no integral needed)

> [!warning] These are NOT on the formula sheet
> If you use them, justify them in a sentence or two, the way the lecture did:
> - **Shell, outside:** "By spherical symmetry, $\vec E$ is radial with magnitude depending only on $r$. Far away it must be $kQ/r^2$ (far-field theorem), and symmetry leaves no other possible form closer in. So $E=kQ/r^2$ for all $r>R$."
> - **Shell, inside:** $E_{\text{in}}=0$ (shell theorem, from lecture).
> - **Ball, inside:** "Only the charge at radius $<r$ contributes, since each outer shell gives zero inside itself. That inner charge acts like a point charge at the center."

**Thin spherical shell** (radius $R$, charge $Q$):
$$
\vec E_{\text{out}}=\frac{kQ}{r^2}\hat r\ (r>R),\qquad \vec E_{\text{in}}=0\ (r<R)
$$
Outside, the shell acts like a point charge at its center. Inside, the field is exactly zero.

**Why zero inside:** from any inside point, the near patch of shell is close but small, and the opposite patch is far but bigger. Patch area grows like distance², which exactly offsets the $1/r^2$, so opposite patches cancel.

```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\begin{axis}[name=E,width=7.5cm,height=5.5cm,axis lines=left,xmin=0,xmax=4.2,ymin=0,ymax=1.15,
xlabel={$r/R$},ylabel={$E\ (kQ/R^2)$},title={$E$: jumps at $r=R$},xtick={1,2,3,4},ytick={0.5,1}]
\addplot[very thick,domain=0:1]{0};
\addplot[very thick,domain=1:4,samples=80]{1/x^2};
\addplot[dotted,cgry] coordinates {(1,0) (1,1.1)};
\addplot[only marks,mark=*,mark size=2.5pt] coordinates {(1,1)};
\addplot[only marks,mark=o,mark size=2.5pt,thick] coordinates {(1,0)};
\end{axis}
\begin{axis}[at={(E.outer east)},anchor=outer west,xshift=1.2cm,width=7.5cm,height=5.5cm,axis lines=left,xmin=0,xmax=4.2,ymin=0,ymax=1.15,
xlabel={$r/R$},ylabel={$V\ (kQ/R)$},title={$V$: continuous, kinked at $r=R$},xtick={1,2,3,4},ytick={0.5,1}]
\addplot[very thick,cacc,domain=0:1]{1};
\addplot[very thick,cacc,domain=1:4,samples=80]{1/x};
\addplot[dotted,cgry] coordinates {(1,0) (1,1.1)};
\end{axis}
\end{tikzpicture}
\end{document}
```

**Uniform solid ball** (radius $R$, charge $Q$):
$$
\vec E_{\text{out}}=\frac{kQ}{r^2}\hat r,\qquad \vec E_{\text{in}}=\frac{kQ\,r}{R^3}\hat r
$$
Why: treat the ball as nested shells. Shells outside radius $r$ give zero; shells inside act like a point charge at the center. Charge is proportional to volume, so
$$Q_{\text{enc}}=Q\cdot\frac{\tfrac43\pi r^3}{\tfrac43\pi R^3}=Q\frac{r^3}{R^3},\qquad E_{\text{in}}=\frac{kQ_{\text{enc}}}{r^2}=\frac{kQ}{r^2}\cdot\frac{r^3}{R^3}=\frac{kQr}{R^3}.$$
At $r=R$ both formulas give $kQ/R^2$, so there's no jump.

```tikz
\usepackage{pgfplots}
\pgfplotsset{compat=1.16}
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\begin{axis}[name=E,width=7.5cm,height=5.5cm,axis lines=left,xmin=0,xmax=4.2,ymin=0,ymax=1.15,
xlabel={$r/R$},ylabel={$E\ (kQ/R^2)$},title={$E$: no jump},xtick={1,2,3,4},ytick={0.5,1}]
\addplot[very thick,domain=0:1]{x};
\addplot[very thick,domain=1:4,samples=80]{1/x^2};
\addplot[dotted,cgry] coordinates {(1,0) (1,1.1)};
\end{axis}
\begin{axis}[at={(E.outer east)},anchor=outer west,xshift=1.2cm,width=7.5cm,height=5.5cm,axis lines=left,xmin=0,xmax=4.2,ymin=0,ymax=1.65,
xlabel={$r/R$},ylabel={$V\ (kQ/R)$},title={$V$: smooth everywhere},xtick={1,2,3,4},ytick={0.5,1,1.5}]
\addplot[very thick,cacc,domain=0:1,samples=40]{(3-x^2)/2};
\addplot[very thick,cacc,domain=1:4,samples=80]{1/x};
\addplot[dotted,cgry] coordinates {(1,0) (1,1.6)};
\end{axis}
\end{tikzpicture}
\end{document}
```

**Non-uniform ball** ($\rho(r)$ given): same logic, but you integrate to get the enclosed charge:
$$
Q_{\text{enc}}(r)=\int_0^r\rho(r')\,4\pi r'^2\,dr',\qquad E(r)=\frac{kQ_{\text{enc}}(r)}{r^2}
$$
Here $\rho\,4\pi r'^2\,dr'$ is the charge in a thin shell of radius $r'$ and thickness $dr'$ (shell area $4\pi r'^2$ times thickness). Example: $\rho=\beta r$ gives
$$Q_{\text{enc}}=\int_0^r\beta r'\cdot4\pi r'^2\,dr'=4\pi\beta\frac{r^4}{4}=\pi\beta r^4,\qquad E=\frac{k\pi\beta r^4}{r^2}=k\pi\beta r^2.$$

### 4.11 Non-uniform rod

**Setup.** A rod on the $x$-axis from $0$ to $L$ with $\lambda(x)=\alpha x$. Find $\vec E$ at P $=(-d,0)$, a distance $d$ to the left of the origin.

1. $dq=\alpha x\,dx$ at $(x,0)$. $\vec r=\langle -d-x,\,0\rangle$, $|\vec r|=d+x$, so the direction is $-\hat x$.
2. Field from one piece:
$$
dE_x=-k\frac{\alpha x\,dx}{(d+x)^2}
$$
3. Integrate with $u=d+x$, $x=u-d$:
$$
\int_0^L\frac{x\,dx}{(d+x)^2}=\int_d^{d+L}\left(\frac1u-\frac{d}{u^2}\right)du=\ln\frac{d+L}{d}-\frac{L}{d+L}
$$
$$
\boxed{\ \vec E=-k\alpha\left[\ln\!\left(1+\frac Ld\right)-\frac{L}{L+d}\right]\hat x\ }
$$
4. **Check far away** with $\epsilon=L/d\ll1$: $\ln(1+\epsilon)-\dfrac{\epsilon}{1+\epsilon}\approx(\epsilon-\tfrac12\epsilon^2)-(\epsilon-\epsilon^2)=\tfrac12\epsilon^2$. So $E\approx k\alpha L^2/(2d^2)=kQ/d^2$ with $Q=\alpha L^2/2$ ✓.

### 4.12 A 3D surface: hemispherical shell, field at the center

"All geometries are fair game." Here's how a curved surface works.

**Setup.** A hemispherical shell of radius $R$ (the top half, $z\ge0$) with charge $Q$ spread uniformly, so $\sigma=Q/(2\pi R^2)$. Find $\vec E$ at the center.

1. Slice it into rings at polar angle $\theta$ (measured from the $+z$ axis). A ring has radius $R\sin\theta$, sits at height $z=R\cos\theta$, and has width $R\,d\theta$. So
$$dq=\sigma(2\pi R\sin\theta)(R\,d\theta)=2\pi\sigma R^2\sin\theta\,d\theta$$
2. Each ring is a ring (§4.6). The center is on its axis at distance $R\cos\theta$ *below* it, and every point of the ring is a distance $R$ from the center. By symmetry only $z$-components survive, and they point in the $-z$ direction (away from the charge):
$$
dE_z=-\frac{k\,dq\,(R\cos\theta)}{R^3}=-2\pi k\sigma\sin\theta\cos\theta\,d\theta
$$
3. Integrate $\theta=0\to\pi/2$:
$$
E_z=-2\pi k\sigma\int_0^{\pi/2}\sin\theta\cos\theta\,d\theta=-2\pi k\sigma\cdot\frac12=-\pi k\sigma=\boxed{-\frac{kQ}{2R^2}}
$$

> [!tip] The "reuse a known result" trick
> The disk (rings), the hemisphere (rings), and a cylinder's surface (rings) are all built from **pieces whose field you already know**. If an exam shape decomposes into rings, rods, or sheets, use the known $d\vec E$ for that piece instead of starting from point charges.

## 5. The integrals you'll actually meet

The ✅ rows are printed on the formula sheet. Know the ✍️ rows yourself (each is a one-line $u$-substitution, except the trig-sub log).

| Integral | Result | Sheet? |
|---|---|---|
| $\displaystyle\int\frac{dx}{(x^2+a^2)^{3/2}}$ | $\dfrac{x}{a^2\sqrt{x^2+a^2}}$ | ✅ |
| $\displaystyle\int\frac{x\,dx}{(x^2+a^2)^{3/2}}$ | $-\dfrac{1}{\sqrt{x^2+a^2}}$ | ✅ |
| $\displaystyle\int\frac{dx}{x+a}$ | $\ln(x+a)$ | ✅ |
| $\displaystyle\int\frac{dx}{(x+a)^2}$ | $-\dfrac{1}{x+a}$ | ✅ |
| $\displaystyle\int\frac{dx}{(x+a)^3}$ | $-\dfrac{1}{2(x+a)^2}$ | ✅ |
| $\displaystyle\int\frac{a\,dx}{x(x+b)}$ | $\dfrac ab\displaystyle\int\left(\frac1x-\frac1{x+b}\right)dx=\dfrac ab\ln\dfrac{x}{x+b}$ | ✅ (partial fractions) |
| $\displaystyle\int a\,dx,\ \int ax\,dx,\ \int ax^2\,dx$ | $ax,\ \tfrac12ax^2,\ \tfrac13ax^3$ | ✅ |
| $\displaystyle\int\frac{dx}{\sqrt{x^2+a^2}}$ | $\ln\!\left(x+\sqrt{x^2+a^2}\right)$ | ✍️ trig sub |
| $\displaystyle\int\frac{x\,dx}{\sqrt{x^2+a^2}}$ | $\sqrt{x^2+a^2}$ | ✍️ $u=x^2+a^2$ |
| $\displaystyle\int\cos\theta\,d\theta,\ \int\sin\theta\,d\theta$ | $\sin\theta,\ -\cos\theta$ | ✍️ |
| $\displaystyle\int\sin\theta\cos\theta\,d\theta$ | $\tfrac12\sin^2\theta$ | ✍️ $u=\sin\theta$ |

For the non-uniform rod in §4.11, the integrand $\frac{x}{(d+x)^2}$ splits into $\frac1{d+x}-\frac{d}{(d+x)^2}$. Both pieces are ✅ sheet integrals.

**Odd-function rule:** if $f(-x)=-f(x)$, then $\int_{-a}^{a}f(x)\,dx=0$. This is the math behind "cancels by symmetry."

---

# Part II — Conductors, Insulators, and Superposition Tricks

The recommended practice list groups conductors and polarization under the distributed-charge topic, so you need these ideas too.

## 6. Conductors vs. insulators

**Conductor (metal):** some electrons are free to move through the whole object. **Insulator (plastic, glass):** electrons are bound to their atoms and can only shift slightly.

Polarization: put an object in an external field $\vec E_{\text{ext}}$ and its charges shift, creating their own field $\vec E_{\text{pol}}$. The total field is
$$\vec E_{\text{tot}}=\vec E_{\text{ext}}+\vec E_{\text{pol}}$$

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\node at (1.5,3.6) {Insulator};
\fill[cneg,fill opacity=0.08] (0,0) rectangle (3,3);
\draw (0,0) rectangle (3,3);
\foreach \y in {0.5,1.5,2.5} \draw[-{Stealth[length=2.5mm]},thick,cgry] (-1.7,\y)--(-0.4,\y);
\foreach \y in {0.9,2.1} {\node[nc,minimum size=4mm] at (0,\y) {\tiny$-$}; \node[pc,minimum size=4mm] at (3,\y) {\tiny$+$};}
\draw[-{Stealth[length=2.5mm]},thick,dashed,cacc] (2.3,1.5)--(0.7,1.5) node[midway,above]{\small$\vec E_{\rm pol}$};
\node at (1.5,-0.6) {$E_{\rm tot}<E_{\rm ext}$};
\begin{scope}[xshift=6.5cm]
\node at (1.5,3.6) {Conductor};
\fill[corg,fill opacity=0.15] (0,0) rectangle (3,3);
\draw (0,0) rectangle (3,3);
\foreach \y in {0.5,1.5,2.5} \draw[-{Stealth[length=2.5mm]},thick,cgry] (-1.7,\y)--(-0.4,\y);
\foreach \y in {0.45,1.15,1.85,2.55} {\node[nc,minimum size=4mm] at (0,\y) {\tiny$-$}; \node[pc,minimum size=4mm] at (3,\y) {\tiny$+$};}
\node[cpos] at (1.5,1.5) {$\vec E_{\rm tot}=0$};
\node at (1.5,-0.6) {$E_{\rm pol}=E_{\rm ext}$ exactly};
\end{scope}
\end{tikzpicture}
\end{document}
```

| | Conductor (in equilibrium) | Insulator |
|---|---|---|
| Inside field | $\vec E_{\text{tot}}=0$ **exactly** | $\vec E_{\text{tot}}$ reduced but **not** zero |
| Why | Free electrons keep moving until their field exactly cancels $\vec E_{\text{ext}}$ | Each atom/molecule becomes a small dipole; $\vec E_{\text{pol}}$ never fully cancels $\vec E_{\text{ext}}$ |
| Where excess charge sits | On the **surface** only | Wherever you put it (it can't move) |
| Potential | Same everywhere inside and on the surface (equipotential) | Varies |

### 6.1 Key conductor facts (equilibrium)

1. $\vec E=0$ everywhere inside the metal, whether the conductor is charged or neutral, polarized or not.
2. Since $\vec E=0$ inside, $\Delta V=-\int\vec E\cdot d\vec l=0$ between any two points of the metal. **The whole conductor is at one potential.**
3. Any net charge lives on the surface. Why: excess charge inside the metal would make a field around itself, which contradicts fact 1. Like charges also repel each other, so they spread out as far apart as they can get, which is the surface.
4. Just outside the surface, $\vec E$ is perpendicular to the surface. (A sideways component would push surface charges along, which isn't equilibrium.)
5. **Empty cavity inside a conductor:** $\vec E=0$ in the cavity too (shielding / Faraday cage). Proof: take any path through the cavity that starts and ends on the cavity wall. Both endpoints are at the same potential, so $\int\vec E\cdot d\vec l=0$ for *every* path, which forces $\vec E_{\text{cavity}}=0$.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\fill[corg,fill opacity=0.2,even odd rule] (0,0) circle (2.4) (0,0) circle (1.2);
\draw (0,0) circle (2.4) (0,0) circle (1.2);
\foreach \y in {-1.6,-0.8,0,0.8,1.6} {\draw[-{Stealth[length=2.5mm]},thick,cgry] (-4.4,\y)--(-2.9,\y); \draw[-{Stealth[length=2.5mm]},thick,cgry] (2.9,\y)--(4.4,\y);}
\node at (-3.65,2.2) {$\vec E_{\rm ext}$};
\foreach \a in {140,165,195,220} \node[cneg] at (\a:2.65) {$-$};
\foreach \a in {40,15,-15,-40} \node[cpos] at (\a:2.65) {$+$};
\node at (0,0) {\begin{tabular}{c}$\vec E=0$\\(cavity)\end{tabular}};
\node at (0,1.8) {\small$\vec E=0$ (metal)};
\end{tikzpicture}
\end{document}
```

### 6.2 Charge inside a hollow conductor

Put charge $+q$ inside the cavity of a neutral, thick-walled metal shell:
- The inner wall gets $-q$ (induced, to make $\vec E=0$ in the metal).
- The outer surface gets $+q$ (the shell is neutral overall: $-q+q=0$).
- Outside, the field is that of $+q$ (spread uniformly over the outer surface if it is spherical).

If the shell also carries its own net charge $Q$: inner wall $-q$, outer surface $Q+q$.

### 6.3 Polarized insulators near charges

A neutral insulator near a charge gets polarized, with the opposite-sign end closer to the charge. It is **attracted**, because the near end (opposite sign, attracted) is closer than the far end (same sign, repelled), and Coulomb's force is stronger at shorter distance. So attraction wins. The polarization field inside points opposite to $\vec E_{\text{ext}}$ and reduces it, but **never** reverses or fully cancels it.

> [!example] Lecture-style conceptual question
> Two equal negative balls sit near a neutral plastic block. What is the field at the block's center? Add three contributions: ball 1, ball 2, and the block's polarization. The polarization field opposes the net external field but is smaller, so **the net field still points the way the external field does**.

## 7. Superposition tricks for distributed charge

1. **Add pieces:** rod + point charge, two rods, arc + straight segments. Compute each $\vec E$ separately (each with its own $\vec r$), then add components.
2. **Subtract a hole:** a disk with a hole = full disk ($+\sigma$) + a small disk of $-\sigma$ where the hole is. A sphere with a cavity works the same way.
3. **Sheets:** each infinite sheet contributes $2\pi k|\sigma|$ pointing away (if $+$) or toward (if $-$). Add them region by region.
4. **Field at the center of a shell from another object:** the shell contributes 0 inside itself, so only the other object counts. (A lecture clicker question: the field at the center of a charged shell due to a ball a distance $d$ away is $kq_{\text{ball}}/d^2$.)

---

# Part III — Electric Potential, Potential Difference, and Potential Energy

## 8. Work and potential energy (the mechanics foundation)

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[thick,cgry,postaction={decorate},decoration={markings,mark=at position 0.2 with {\arrow{Stealth[length=2.5mm]}},mark=at position 0.42 with {\arrow{Stealth[length=2.5mm]}},mark=at position 0.8 with {\arrow{Stealth[length=2.5mm]}}}] (0,0) .. controls (2,0.3) and (5,1.5) .. (6,4);
\fill (0,0) circle (2.5pt) node[below left]{$\vec r_i$};
\fill (6,4) circle (2.5pt) node[above right]{$\vec r_f$};
\draw[vec,cpos] (3.708,1.378)--(5.507,1.308) node[right]{$\vec F$};
\draw[vec] (3.708,1.378)--(4.465,1.865) node[above left]{$d\vec r$};
\node at (3,4.6) {$W_F=\displaystyle\int_{\vec r_i}^{\vec r_f}\vec F\cdot d\vec r$};
\end{tikzpicture}
\end{document}
```

**Work** done by a force along a path:
$$
W=\int_{\vec r_i}^{\vec r_f}\vec F\cdot d\vec l
$$
($d\vec l$ = a tiny step along the path; see §9.)
- $W>0$ when the force points along the motion (it speeds the object up).
- $W<0$ when the force opposes the motion.

**Work–energy theorem:** $W_{\text{net}}=\Delta K$, with $K=\tfrac12mv^2$.

**Conservative force:** its work doesn't depend on the path (electric force from static charges: yes; friction: no). Only these get a potential energy, since $U$ must depend only on position.

**Potential energy** is defined so that
$$
\Delta U=U_f-U_i=-W=-\int_i^f\vec F\cdot d\vec l
$$

**Energy conservation** (only conservative forces like the electric force): $\Delta K+\Delta U=0$, or equivalently
$$
K_i+U_i=K_f+U_f
$$

> [!example] Lecture clicker question
> An electron moves *in the direction of* $\vec E$ between two parallel plates. The force on the electron is $-e\vec E$, which is *opposite* its motion, so $W<0$, $\Delta K<0$ (it slows down), and $\Delta U>0$.

## 9. Electric potential $V$

For the electric force, $\vec F=q\vec E$:
$$
\Delta U=-q\int_i^f\vec E\cdot d\vec l
$$
Now divide by $q$. The result depends only on the field, not on the charge you move. Call it the **electric potential difference**:

$$
\boxed{\ \Delta V=V_f-V_i=-\int_i^f\vec E\cdot d\vec l\ }\qquad\qquad \boxed{\ \Delta U=q\,\Delta V\ }
$$

> [!important] What is $d\vec l$?
> A **tiny step along your path** from $i$ to $f$ (also written $d\vec r$ or $d\vec s$). $\vec E\cdot d\vec l$ keeps only the part of the step along $\vec E$:
> - along $\vec E$: $\Delta V<0$ · against $\vec E$: $\Delta V>0$ · perpendicular: $\Delta V=0$
>
> Write it in the **positive** coordinate direction ($dx\,\hat x$, $dy\,\hat y$, $dr\,\hat r$) and let the **limits** (start → end) set the direction. Example, radial path: $\Delta V=-\int_{r_1}^{r_2}\frac{kq}{r^2}\hat r\cdot dr\,\hat r=-\int_{r_1}^{r_2}\frac{kq}{r^2}dr$, even if $r_2<r_1$. Using $-dr\,\hat r$ **and** reversed limits counts the direction twice.

- **Potential $V$** (volts, V = J/C) is a property of a *location* in space, set up by the source charges.
- **Potential energy $U$** (joules) belongs to a *specific charge $q$* sitting at that location: $U=qV$.
- Only **differences** matter. You pick where $V=0$ (the reference). For finite charge distributions the usual choice is $V(\infty)=0$.

### 9.1 What the signs mean (memorize these)

| Statement | Why |
|---|---|
| $\vec E$ points from **high V to low V** | Moving along $\vec E$ gives $\vec E\cdot d\vec l>0$, so $\Delta V<0$ |
| Moving **along** $\vec E$: $\Delta V<0$ | |
| Moving **against** $\vec E$: $\Delta V>0$ | |
| Moving **perpendicular** to $\vec E$: $\Delta V=0$ | $\vec E\cdot d\vec l=0$ (equipotential) |
| A free **positive** charge accelerates toward **lower** $V$ | It lowers its $U=qV$ |
| A free **negative** charge (electron) accelerates toward **higher** $V$ | $q<0$, so lower $U$ means higher $V$ |
| Positive charges sit at high $V$; negative charges at low $V$ | $V=kq/r$ has the sign of $q$ |

### 9.2 Equipotentials

**Equipotential surfaces** are surfaces of constant $V$. $\vec E$ is always **perpendicular** to them and points toward lower $V$. Why perpendicular: a step $d\vec l$ *along* an equipotential has $\Delta V=0$, so $\vec E\cdot d\vec l=0$ for every such step, which means $\vec E$ has no component along the surface. For a point charge, they are concentric spheres. For a uniform field, they are flat planes perpendicular to $\vec E$.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\foreach \r in {0.8,1.4,2.0,2.6} \draw[dashed,thick,cacc] (0,0) circle (\r);
\foreach \a in {0,30,...,330} \draw[-{Stealth[length=2.5mm]},thick,cgry] (\a:0.4)--(\a:2.95);
\node[pc] at (0,0) {$+$};
\node[cacc,right] at (2.8,1.9) {equipotentials (dashed)};
\node[cgry,right] at (2.8,1.3) {field lines (arrows)};
\end{tikzpicture}
\end{document}
```

### 9.3 Path independence and closed loops

The electric field from static charges is **conservative**: $\Delta V$ between two points is the same for **every** path. Why: around a point charge, any path splits into radial steps (which change $V$) and arc steps ($\perp\vec E$, no change), and the radial steps always total the same (§10.2). Any distribution is a sum of point charges. Consequences:
- **Pick the easiest path.** Break it into segments along $\vec E$ (where $\vec E\cdot d\vec l=E\,dl$) and segments perpendicular to $\vec E$ (where it is 0).
- **Closed loops:** $\oint\vec E\cdot d\vec l=0$. Around any closed path, the potential differences sum to zero. **This is the physics behind Kirchhoff's loop rule** in Part IV.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[cgry,dotted] (0,0) circle (1.5) (0,0) circle (3);
\draw[vec,cneg] (20:1.5)--(20:3);
\draw[vec,cneg] (20:3) arc (20:75:3);
\draw[vec,cacc,dashed] (20:1.5) arc (20:75:1.5);
\draw[vec,cacc,dashed] (75:1.5)--(75:3);
\fill (20:1.5) circle (2.5pt) node[below right]{$\vec r_1$};
\fill (75:3) circle (2.5pt) node[above]{$\vec r_2$};
\node[pc] at (0,0) {$+$};
\node[cneg,right,font=\small,align=left] at (3.3,1.2) {solid: radial out, then arc};
\node[cacc,right,font=\small,align=left] at (3.3,0.6) {dashed: arc, then radial out};
\node[right,font=\small,align=left] at (3.3,-0.2) {arcs: $\vec E\perp d\vec l$, so $\Delta V=0$\\both paths give the same $\Delta V$};
\end{tikzpicture}
\end{document}
```

## 10. Computing $\Delta V=-\int\vec E\cdot d\vec l$: the procedure

> [!example] The potential-difference recipe
> 1. **Find $\vec E$ everywhere along the path.** It may be piecewise, different in different regions (e.g. inside vs. outside a shell). This is often Part (a) of the exam problem.
> 2. **Choose a path** from the start point $i$ to the end point $f$. For radial fields, go radially.
> 3. **Write $d\vec l$** in coordinates. For a radial path, $d\vec l=dr\,\hat r$. **Always write $d\vec l$ in the *positive* coordinate direction** ($+dr\,\hat r$, $+dx\,\hat x$), and let the **limits of integration** (start → end) handle the direction. This is the #1 sign trap.
> 4. **Compute $\vec E\cdot d\vec l$.** For a radial field and radial path: $E_r\,dr$.
> 5. **Integrate from start to finish**, one region at a time, adding the pieces.
> 6. **Sign check**: did you move along $\vec E$ (expect $\Delta V<0$) or against it (expect $\Delta V>0$)?

> [!warning] The double-negative trap
> Moving inward from $r=b$ to $r=a<b$, students write $d\vec l=-dr\,\hat r$ **and** integrate from $b$ to $a$. That counts the direction twice. Pick one: either $d\vec l=+dr\,\hat r$ with limits $b\to a$ (recommended), or flip the limits. Never both.

### 10.1 Uniform (constant) field

For constant $\vec E$, the field is the same at every step, so it comes out of the integral, and adding up all the steps gives the total displacement, $\int_i^f d\vec l=\Delta\vec r=\vec r_f-\vec r_i$:
$$
\Delta V=-\int_i^f\vec E\cdot d\vec l=-\vec E\cdot\int_i^f d\vec l=-\vec E\cdot\Delta\vec r
$$
For a straight move of distance $d$ along $\vec E$: $\Delta V=-Ed$.

**Parallel plates** (separation $d$, field $E=4\pi k\sigma$ pointing from $+$ to $-$):
$$
V_+-V_-=+Ed=4\pi k\sigma d
$$
The positive plate is at higher potential.

**Diagonal path:** only the component along $\vec E$ matters. If $\vec E=E\hat x$ and you move $\Delta\vec r=\langle a,b\rangle$, then $\Delta V=-Ea$.

**Two sheets with the same sign:** $E=0$ between them, so $\Delta V=0$ between them (lecture clicker).

**Metal slab between the plates** (thickness $t$): $E=0$ inside the metal, so only the empty gaps contribute: $|\Delta V|=E(d-t)$. Integrate region by region, the same way as for the shells in §10.6.

### 10.2 Point charge: derive $V(r)=kq/r$

Take $\vec E=\dfrac{kq}{r^2}\hat r$ and a radial path from $r_1$ to $r_2$:
$$
V(r_2)-V(r_1)=-\int_{r_1}^{r_2}\frac{kq}{r^2}dr=kq\left[\frac1r\right]_{r_1}^{r_2}=\frac{kq}{r_2}-\frac{kq}{r_1}
$$
(The antiderivative of $r^{-2}$ is $-1/r$; that minus combines with the minus in front of the integral to give $+kq/r$.)
Now set $V(\infty)=0$ (let $r_1\to\infty$):
$$
\boxed{\ V(r)=\frac{kq}{r}\ }
$$
Any path works, because any path can be broken into radial pieces (which contribute) and circular arcs (where $\vec E\perp d\vec l$, contributing zero).

**Check by going backwards:** $E_r=-\dfrac{dV}{dr}=-\dfrac{d}{dr}\dfrac{kq}{r}=\dfrac{kq}{r^2}$ ✓.

### 10.3 Infinite line charge (and coaxial cylinders)

$\vec E=\dfrac{2k\lambda}{r}\hat r$. Integrate radially from $r_a$ to $r_b$:
$$
V(r_b)-V(r_a)=-\int_{r_a}^{r_b}\frac{2k\lambda}{r}dr=-2k\lambda\ln\frac{r_b}{r_a}
$$
You **cannot** set $V(\infty)=0$ here: $\ln\infty$ diverges, because the line has infinite total charge. Only differences make sense.

**Coaxial cylinders** (inner radius $a$ carrying $+\lambda$, outer radius $b$ carrying $-\lambda$): between them only the inner charge produces a field (the outer cylinder contributes zero inside itself, like a shell), so $E=2k\lambda/r$. Then
$$
V_a-V_b=2k\lambda\ln\frac ba>0
$$

### 10.4 Spherical shell

Outside, the field is that of a point charge, so $V_{\text{out}}(r)=kQ/r$. Inside, $\vec E=0$, so $V$ is **constant**, and $V$ must be continuous at $r=R$:
$$
V_{\text{out}}=\frac{kQ}{r}\ (r\ge R),\qquad V_{\text{in}}=\frac{kQ}{R}\ (r\le R)
$$
Note that $\vec E$ is discontinuous at the surface, but $V$ is **continuous**. $V$ never jumps (that would mean an infinite field).

### 10.5 Solid ball, inside

Start from the surface, where $V(R)=kQ/R$, and integrate inward using $E_{\text{in}}=kQr/R^3$:
$$
V(r)-V(R)=-\int_R^r\frac{kQr'}{R^3}dr'=-\frac{kQ}{2R^3}(r^2-R^2)
$$
$$
\boxed{\ V_{\text{in}}(r)=\frac{kQ}{2R^3}(3R^2-r^2)\ }
$$
At the center, $V(0)=\tfrac32\dfrac{kQ}{R}$, which is higher than at the surface ✓ (you move against $\vec E$ going in).

### 10.6 Concentric shells, region by region (classic exam problem)

This is "The charged shells" problem from the recommended list.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[cneg,line width=2.5pt] (0,0) circle (2.8);
\draw[cpos,line width=2.5pt] (0,0) circle (1.3);
\draw[vec,cpos,thick] (0,0)--(-40:1.3) node[midway,below left]{$R_1$};
\draw[vec,cneg,thick] (0,0)--(65:2.8) node[pos=0.75,left]{$R_2$};
\node[cpos] at (0,1.65) {$q_1$};
\node[cneg] at (0,3.2) {$q_2$};
\node at (-0.45,-0.35) {I};
\node at (1.9,-0.6) {II};
\node at (3.2,-1.9) {III};
\end{tikzpicture}
\end{document}
```

**Setup.** An inner shell of radius $R_1$ with charge $q_1$, and an outer shell of radius $R_2$ with charge $q_2$.

**Step 1: the field in each region** (only charge *inside* radius $r$ contributes):
- Region I ($r<R_1$): $E=0$
- Region II ($R_1<r<R_2$): $E=kq_1/r^2$
- Region III ($r>R_2$): $E=k(q_1+q_2)/r^2$

**Step 2: integrate in from infinity**, with $V(\infty)=0$:

Region III: $V(r)=-\int_\infty^r\dfrac{k(q_1+q_2)}{r'^2}dr'=\dfrac{k(q_1+q_2)}{r}$

Region II:
$$
V(r)=V(R_2)-\int_{R_2}^{r}\frac{kq_1}{r'^2}dr'=\frac{k(q_1+q_2)}{R_2}+kq_1\left(\frac1r-\frac1{R_2}\right)=\frac{kq_1}{r}+\frac{kq_2}{R_2}
$$

Region I: constant, equal to $V(R_1)=\dfrac{kq_1}{R_1}+\dfrac{kq_2}{R_2}$.

**Shortcut (superposition of $V$):** each shell gives $kq/r$ outside itself and $kq/R$ (constant) inside itself. Add them. Same answer, much faster, so use it to check your integral.

**Potential difference between the shells:**
$$
V(R_1)-V(R_2)=kq_1\left(\frac1{R_1}-\frac1{R_2}\right)
$$
It depends **only on the inner charge**, because the outer shell adds the same constant to both points. (Lecture example: an inner conducting ball $+Q$ and an outer shell $-Q$ give $V_{\text{in}}-V_{\text{out}}=kQ(1/R_2-1/R_1)$ in their labeling, where $R_2<R_1$ is the inner radius.)

### 10.7 A charged sphere: count the electrons

(Lecture clicker, symbolic version.) To raise a sphere of radius $R$ to potential $V$: $V=kQ/R$, so $Q=VR/k$, and the number of electrons is $N=Q/e=VR/(ke)$.

## 11. Potential by direct superposition (a scalar sum — easier!)

Potential is a **scalar**, so superposition means adding plain numbers. No components, no cancellation by symmetry, no vectors.

**Point charges:**
$$
V(\vec r)=\sum_i\frac{kq_i}{|\vec r-\vec r_i|}
$$
Keep the **sign** of each $q_i$. Lecture example: $+q_1$, $-q_2$, $+q_3$ at distances $a$, $a$, $\sqrt{a^2+b^2}$ gives $V=k\left(\dfrac{q_1}{a}-\dfrac{q_2}{a}+\dfrac{q_3}{\sqrt{a^2+b^2}}\right)$.

> [!example] Clicker: where is $V=0$ between two charges?
> Two identical positive charges: $V=kq/r_1+kq/r_2>0$ everywhere at finite distance. So $V=0$ only infinitely far away. (Compare: $\vec E=0$ at the midpoint, but $V$ there is $2kq/(d/2)\ne0$. **$E=0$ does not mean $V=0$**, and vice versa.)

**Continuous distribution:**
$$
V(\vec r)=k\int\frac{dq}{|\vec r-\vec r_{\text{source}}|}
$$
Same $dq$ and $|\vec r|$ as Part I, just no vector components.

### 11.1 Ring on axis

Every $dq$ is the same distance $\sqrt{z^2+R^2}$ away, so
$$
V(z)=\frac{kQ}{\sqrt{z^2+R^2}}
$$
**Check:** $E_z=-\dfrac{dV}{dz}=\dfrac{kQz}{(z^2+R^2)^{3/2}}$ ✓ (matches §4.6).

### 11.2 Disk on axis

Use rings with $dq=\sigma2\pi r\,dr$:
$$
V(z)=\int_0^R\frac{k\,\sigma2\pi r\,dr}{\sqrt{z^2+r^2}}=2\pi k\sigma\left[\sqrt{z^2+r^2}\right]_0^R=2\pi k\sigma\left(\sqrt{z^2+R^2}-|z|\right)
$$
$V$ is **continuous** at $z=0$, while $E$ jumps there.

Limits:
- Close to the disk ($|z|\ll R$): $V\approx2\pi k\sigma(R-|z|)$, a constant minus $2\pi k\sigma|z|$. That is the linear $V$ of an infinite sheet.
- Far away: factor out $|z|$ and use the binomial approximation, $\sqrt{z^2+R^2}=|z|\left(1+\frac{R^2}{z^2}\right)^{1/2}\approx|z|\left(1+\frac{R^2}{2z^2}\right)$. Subtracting $|z|$ leaves $\dfrac{R^2}{2|z|}$, so $V\approx2\pi k\sigma\dfrac{R^2}{2|z|}=\dfrac{k(\sigma\pi R^2)}{|z|}=\dfrac{kQ}{|z|}$ ✓.

### 11.3 Rod on axis, beyond its end

Same setup as §4.1:
$$
V=\int_0^L\frac{k\lambda\,dx}{L+d-x}=k\lambda\Big[-\ln(L+d-x)\Big]_0^L=k\lambda\big[-\ln d+\ln(L+d)\big]=k\lambda\ln\frac{L+d}{d}
$$
(With $u=L+d-x$, $du=-dx$, so $\int\frac{dx}{L+d-x}=-\ln u$.) Each piece is a distance $L+d-x$ from P, and potential needs only that distance, not a direction.

### 11.4 Rod on its perpendicular bisector

Same setup as §4.3:
$$
V=k\lambda\int_{-L/2}^{L/2}\frac{dy}{\sqrt{x^2+y^2}}=k\lambda\Big[\ln\big(y+\sqrt{x^2+y^2}\big)\Big]_{-L/2}^{L/2}=k\lambda\ln\frac{L/2+\sqrt{x^2+L^2/4}}{-L/2+\sqrt{x^2+L^2/4}}
$$
(The ✍️ integral $\int\frac{dy}{\sqrt{x^2+y^2}}=\ln(y+\sqrt{x^2+y^2})$ from §5; subtracting two logs gives the log of a ratio.)

## 12. Getting $\vec E$ from $V$

$$
E_x=-\frac{\partial V}{\partial x},\quad E_y=-\frac{\partial V}{\partial y},\quad E_z=-\frac{\partial V}{\partial z}\qquad\left(\vec E=-\nabla V\right)
$$
- **What $\partial V/\partial x$ means:** a *partial* derivative. Differentiate with respect to $x$ while treating $y$ and $z$ as constants. Example: $V=kq/\sqrt{x^2+y^2}$ gives $\partial V/\partial x=-kqx/(x^2+y^2)^{3/2}$.
- **Why the minus sign:** it's the reverse of $\Delta V=-\int\vec E\cdot d\vec l$. For a tiny step $dx$ along $x$, $dV=-E_x\,dx$, so $E_x=-dV/dx$.
- $\vec E$ points in the direction $V$ **decreases** fastest.
- In 1D: $E_x=-dV/dx$. A steep $V(x)$ graph means a strong field.
- Shortcut: $V$ is a scalar integral (easy), and its derivative gives $\vec E$. **Warning:** if you only know $V$ along an axis, you only get the field component along that axis.

## 13. Potential energy and energy conservation problems

### 13.1 Potential energy of a system of charges

The energy to assemble point charges from infinity:
$$
U_{\text{pair}}=\frac{kq_1q_2}{r_{12}},\qquad U_{\text{system}}=\sum_{\text{pairs}}\frac{kq_iq_j}{r_{ij}}
$$
**Where it comes from:** $U=qV$. Charge $q_1$ makes potential $V=kq_1/r$ at distance $r$; put $q_2$ there and $U=q_2V=kq_1q_2/r$. That's the work you'd do to bring $q_2$ in from infinity (where $U=0$).

Count each pair **once**: three charges have three pairs, four charges have six. $U>0$ for like charges (you had to push them together); $U<0$ for unlike charges.

### 13.2 A charge moving through a potential difference

For a charge $q$ moving from $i$ to $f$:
$$
\Delta U=q\Delta V,\qquad \Delta K=-q\Delta V
$$
$$
\frac12mv_f^2=\frac12mv_i^2-q(V_f-V_i)
$$

- **Released from rest through $|\Delta V|$** (going "downhill" for its sign): $\tfrac12mv^2=|q||\Delta V|$, so $v=\sqrt{2|q||\Delta V|/m}$.
- A proton ($+e$) gains speed going from high $V$ to low $V$. An electron ($-e$) gains speed going from low $V$ to high $V$.

> [!example] "The CRT" / particle in a capacitor (recommended practice)
> An electron (mass $m$, charge $-e$) enters the gap between parallel plates (field magnitude $E=4\pi k\sigma$, separation $d$) at speed $v_0$, moving from the $-$ plate side toward the $+$ plate. Find its exit speed.
> 1. The field points from $+$ to $-$, so the electron moves *against* $\vec E$: $\Delta V=V_+-V_-=+Ed$.
> 2. $\Delta U=q\Delta V=(-e)(Ed)=-eEd$, so it loses potential energy.
> 3. $\Delta K=+eEd$, so $\tfrac12mv_f^2=\tfrac12mv_0^2+eEd$, giving
> $$v_f=\sqrt{v_0^2+\frac{2eEd}{m}}=\sqrt{v_0^2+\frac{8\pi k\sigma ed}{m}}$$
> 4. **Sanity:** the force on the electron, $-e\vec E$, points toward the $+$ plate, i.e. along its motion. So it speeds up ✓.

### 13.3 Escape / closest-approach problems

A charge $q_2$ (mass $m$) is fired straight at a **fixed** charge $q_1$ of the same sign, starting far away with speed $v_0$. Repulsion slows it until it momentarily stops at the closest distance $r_{\min}$. All the starting kinetic energy has become potential energy ($U=0$ far away, $K=0$ at the turning point), so
$$
\frac12mv_0^2=\frac{kq_1q_2}{r_{\min}}\qquad\text{(starting from far away)}
$$

---

# Part IV — Current, Resistance, and Circuits

## 14. Electric current

**Current** $I$ is the rate at which charge flows through a cross-section:
$$
I=\frac{dQ}{dt}\qquad[\text{A = C/s}]
$$
**Conventional current** points in the direction **positive** charges would move. In metals the carriers are electrons, so the electrons actually drift **opposite** to $I$.

### 14.1 Microscopic picture: $I=|q|nAv$

Suppose carriers with charge $q$ and number density $n$ (carriers per volume) all drift at speed $v$ through a wire of cross-sectional area $A$. In time $\Delta t$ they travel $v\Delta t$, so the carriers in the volume $A\,v\Delta t$ pass through. That's $N=nAv\Delta t$ carriers, and
$$
I=\frac{|q|N}{\Delta t}=|q|nAv\qquad(\text{electrons: } I=enAv)
$$
A typical drift speed is ~0.5 mm/s. That's very slow; the *signal* travels fast, but each electron crawls.

### 14.2 Equilibrium vs. steady state

| Equilibrium | Steady state |
|---|---|
| Nothing changes in time | Nothing changes in time |
| **No** energy input | **Continuous** energy input (a battery) |
| $\vec E=0$ inside a conductor | $\vec E\ne0$ inside a conductor, **constant** along the wire |
| No current | Steady current $I$ |

A metal loop with no battery can't carry a steady current, because in equilibrium the field inside is zero. A battery keeps the system out of equilibrium.

### 14.3 What a battery does: EMF

Chemical reactions pile up excess electrons at the $-$ terminal and a deficit at the $+$ terminal. The battery maintains a potential difference between its terminals called the **electromotive force** (EMF, $\mathcal E$):
$$
\mathcal E=V_+-V_->0
$$
Despite the name, EMF is a **potential difference** (volts), not a force. Inside the battery, chemistry pushes positive charge "uphill" from $-$ to $+$, against the battery's internal field. That uses up chemical energy, which is why batteries run down.

**Where does the field inside the wire come from?** The battery's terminal charges alone (a dipole) can't make a field that follows a bent wire. The field inside the wire comes mostly from **charges on the wire's surface**, which arrange themselves so that $\vec E$ follows the wire with constant magnitude. Very few are needed (lecture estimate: on the order of **one electron** to turn a corner in a copper wire carrying 1 A). Outside the wire, the field comes mostly from the battery's terminal charges.

## 15. Why current is steady: the Drude model

**Analogy:** a skydiver reaches terminal velocity when drag balances gravity. An electron in a wire reaches a constant **drift velocity** when collisions balance the electric force.

- The field accelerates the electron: $\vec F_E=-e\vec E$.
- Collisions with the lattice ions act like a drag force $-m\vec v/\tau$, where $\tau$ is the average time between collisions: each collision wipes out momentum $m\vec v$, once per $\tau$, and force = momentum lost per time.
- Steady state means zero net force:
$$
-e\vec E-\frac{m\vec v}{\tau}=0\quad\Longrightarrow\quad\vec v_d=-\frac{e\tau}{m}\vec E,\qquad |v_d|=\frac{e\tau E}{m}
$$
- **More frequent collisions** (smaller $\tau$) mean a **slower** drift for the same field. (Clicker: Pt, which has more collisions than Cu, has the smaller drift speed.)

> [!info] Formula-sheet notation: mobility $u$
> The sheet writes the drift speed as $\bar v=uE$, where $u$ is the **mobility**. Comparing with Drude, $u=e\tau/m$. Then $I=\lvert q\rvert nA\bar v=\lvert q\rvert nuAE$, which defines the conductivity $\sigma=\lvert q\rvert nu$ (equal to $ne^2\tau/m$). Same physics, different letters. Use whichever the problem uses.

## 16. Ohm's law and resistance

Plug the drift speed into $I=enAv_d$:
$$
I=enA\frac{e\tau E}{m}=\underbrace{\frac{ne^2\tau}{m}}_{\sigma_c}AE
$$
Here $\sigma_c=ne^2\tau/m$ is the **conductivity** (a material property). Its inverse $\rho_c=1/\sigma_c$ is the **resistivity**. (Don't confuse these with charge densities $\sigma$ and $\rho$; same letters, different meaning.)

In a uniform wire of length $L$, the steady-state field is constant and points along the wire. Walking the length of the wire, $\vec E\cdot d\vec l=E\,dl$ at every step, so $|\Delta V|=\int E\,dl=EL$ (the uniform-field result from §10.1). Then $E=\Delta V/L$:
$$
I=\sigma_cA\frac{\Delta V}{L}\quad\Longrightarrow\quad\boxed{\ \Delta V=IR\ },\qquad\boxed{\ R=\frac{L}{\sigma_cA}=\frac{\rho_cL}{A}\ }
$$

**Resistance** $R$ (ohms, Ω) depends on the material ($\rho_c$) and the shape. Longer means more resistance; thicker means less.

> [!important] What Ohm's law actually says
> When current $I$ flows through a resistor $R$, the potential **drops** by $IR$ going *in the direction of the current*. Current flows from high $V$ to low $V$ through a resistor. Ohm's law says nothing about batteries.

**Current density:** $J=I/A=\sigma_cE$.

### 16.1 Field in a wire whose thickness changes (clicker)

The same current $I$ flows through every cross-section (charge conservation in steady state). From $I=\sigma_cAE$:
$$
E=\frac{I}{\sigma_cA}
$$
The **thinner** section has the **larger** field (field lines squeeze together to stay in the wire), and also the faster drift speed, since $v=I/(enA)$.

### 16.2 Scaling questions

- Double the voltage across the same wire: $I$ doubles, $E=\Delta V/L$ doubles, and $v_d\propto E$ doubles.
- Double $R$ by stretching the wire while keeping $I$ fixed: $\Delta V=IR$ doubles. But $L$ also doubled, so $E=\Delta V/L$ stays the same.

## 17. Power and Joule heating (fair game, not a focus)

When charge $Q$ goes through a potential drop $\Delta V$, it loses potential energy $Q\Delta V$. Per unit time, that's a rate of $I\Delta V$. The collisions transfer this energy to the jiggling ions, and we feel it as heat:
$$
\boxed{\ P=I\Delta V=I^2R=\frac{(\Delta V)^2}{R}\ }
$$
The battery supplies power $P_{\text{bat}}=\mathcal EI$. By energy conservation, $\sum P_{\text{batteries}}=\sum I^2R$.

> [!example] Two identical bulbs in series
> A battery $\mathcal E$ drives two bulbs, each with resistance $R$, in series. $R_{\text{eq}}=2R$ and $I=\mathcal E/2R$. Each bulb dissipates $I^2R=\mathcal E^2/4R$, a quarter of what one bulb alone would ($\mathcal E^2/R$).
> **In parallel:** each bulb gets the full $\mathcal E$, so each dissipates $\mathcal E^2/R$. Parallel bulbs are brighter.

## 18. Kirchhoff's rules

### 18.1 Circuit symbols and the "lumped" idea

All of a wire's resistance gets "lumped" into resistor symbols, and connecting wires are treated as **ideal**: zero resistance, so **no voltage change along a wire**. Every point on a continuous stretch of ideal wire is at the same potential. Batteries are ideal (no internal resistance) unless the problem says otherwise.

- Battery symbol: the **long** line is $+$, the **short thick** line is $-$.
- Resistor symbol: a zigzag.

### 18.2 The loop rule (Kirchhoff's voltage law, KVL)

$$
\boxed{\ \sum_{\text{closed loop}}\Delta V_i=0\ }
$$
**Why:** potential is path-independent (§9.3). Walk around any loop and come back to where you started, and you end at the same $V$. It's energy conservation for a charge going around.

```tikz
\usepackage{circuitikz}
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{circuitikz}[american,font=\large]
\draw (0,0) to[battery1,invert] (3,0);
\node[cneg] at (0.15,0.4) {$-$}; \node[cpos] at (2.85,0.4) {$+$};
\draw[->,thick,cneg] (0.5,-0.7)--(2.5,-0.7) node[midway,below]{walk};
\node at (1.5,1.1) {(a) $-\to+$: $\;+\mathcal{E}$};
\draw (5,0) to[battery1] (8,0);
\node[cpos] at (5.15,0.4) {$+$}; \node[cneg] at (7.85,0.4) {$-$};
\draw[->,thick,cneg] (5.5,-0.7)--(7.5,-0.7) node[midway,below]{walk};
\node at (6.5,1.1) {(b) $+\to-$: $\;-\mathcal{E}$};
\draw (0,-3) to[R,i>^=$I$] (3,-3);
\draw[->,thick,cneg] (0.5,-3.7)--(2.5,-3.7) node[midway,below]{walk};
\node at (1.5,-1.9) {(c) with $I$: $\;-IR$};
\draw (8,-3) to[R,i>^=$I$] (5,-3);
\draw[->,thick,cneg] (5.5,-3.7)--(7.5,-3.7) node[midway,below]{walk};
\node at (6.5,-1.9) {(d) against $I$: $\;+IR$};
\end{circuitikz}
\end{document}
```

> [!important] Sign conventions (pick a traversal direction, then apply)
> | You walk through… | $\Delta V$ |
> |---|---|
> | a battery from **− to +** | $+\mathcal E$ |
> | a battery from **+ to −** | $-\mathcal E$ |
> | a resistor **in the same direction as** your assumed current $I$ | $-IR$ |
> | a resistor **opposite to** your assumed current $I$ | $+IR$ |
>
> The battery sign depends only on which terminal you enter, **not** on the current direction. The resistor sign depends only on your walking direction compared to the assumed current.

**Why these signs:** the $+$ terminal is $\mathcal E$ higher than the $-$ terminal, and current flows through a resistor from high $V$ to low $V$ (drop $IR$). A wrong guess for the current direction just makes $I$ come out negative.

**Single loop, one battery, one resistor:** $+\mathcal E-IR=0$, so $\mathcal E=IR$. That follows from the loop rule plus Ohm's law; it isn't a law by itself.

### 18.3 The junction rule (Kirchhoff's current law, KCL)

$$
\boxed{\ \sum I_{\text{in}}=\sum I_{\text{out}}\ }
$$
**Why: conservation of charge.** Charge can't pile up at a junction in steady state. Every electron that enters must leave.

Sign convention: write $+I$ for currents entering and $-I$ for currents leaving, and set the sum to zero (e.g. $I_1+I_2-I_3=0$).

> [!important] Current does NOT change through an element
> The same current that enters a resistor or battery leaves it, with the same magnitude and sign. Current only splits or merges at **junctions** (nodes where 3+ wires meet). It is never "used up" by a resistor; what gets used up is *energy* (potential).

### 18.4 Series and parallel (derived from Kirchhoff)

```tikz
\usepackage{circuitikz}
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{circuitikz}[american,font=\large]
\node at (2.5,4) {Series: same $I$, $\Delta V$s add};
\draw (0,0) to[battery1,invert,l=$\mathcal{E}$] (0,3) to[R,l=$R_1$,i>^=$I$] (2.5,3) to[R,l=$R_2$] (5,3) -- (5,0) -- (0,0);
\node at (2.5,-0.8) {$R_{\rm series}=R_1+R_2$};
\begin{scope}[xshift=7.5cm]
\node at (2.5,4) {Parallel: same $\Delta V$, $I$s add};
\draw (0,0) to[battery1,invert,l=$\mathcal{E}$] (0,3) -- (2.5,3) to[R,l=$R_1$,*-*] (2.5,0) -- (0,0);
\draw (2.5,3) -- (5,3) to[R,l=$R_2$] (5,0) -- (2.5,0);
\node at (2.5,-0.8) {$\frac{1}{R_{\rm par}}=\frac{1}{R_1}+\frac{1}{R_2}$};
\end{scope}
\end{circuitikz}
\end{document}
```

**Series** (one after another, same current): the loop rule gives $\mathcal E-IR_1-IR_2=0$, so
$$
R_{\text{series}}=R_1+R_2+\cdots
$$
The voltage splits in proportion to $R$ (the **voltage divider**): $\Delta V_1=\mathcal E\dfrac{R_1}{R_1+R_2}$.

**Parallel** (both ends connected to the same two nodes, same $\Delta V$): each branch has $I_i=\Delta V/R_i$, and the junction rule gives $I=I_1+I_2=\Delta V\left(\dfrac1{R_1}+\dfrac1{R_2}\right)$, so
$$
\frac1{R_{\text{par}}}=\frac1{R_1}+\frac1{R_2}+\cdots,\qquad\text{two resistors: }R_{\text{par}}=\frac{R_1R_2}{R_1+R_2}
$$
- $R_{\text{par}}$ is always **smaller** than the smallest branch.
- Two equal resistors in parallel give $R/2$; $N$ equal ones give $R/N$.
- **Current divider:** $I_1=I\dfrac{R_2}{R_1+R_2}$ (more current goes through the smaller resistor).

> [!warning] How to recognize series vs. parallel
> - **Series:** there are no junctions between the two elements, so the same current *must* go through both.
> - **Parallel:** both ends of each element connect (by wire alone) to the same two nodes.
> - Many circuits are **neither**, especially ones with batteries in more than one branch. Then you **must** use the full Kirchhoff method (§19), and the exam likes those.

## 19. The Kirchhoff method: solving any circuit

> [!example] The circuit recipe
> 1. **Label every node** (junction) and **every branch current** with an assumed direction. A *branch* is a path between two junctions; it carries one current throughout.
> 2. **Count unknowns** (usually the branch currents). You need that many independent equations.
> 3. **Junction rule** at the nodes. With $n$ nodes you get $n-1$ independent equations (the last one is redundant).
> 4. **Loop rule** for enough independent loops to make up the rest (usually the "window panes" of the circuit). Pick a traversal direction for each and apply the sign table **term by term**, writing every term down.
> 5. **Solve** the linear system: substitute or eliminate.
> 6. **Interpret signs:** a negative current just means it flows opposite to your guess. **Keep the negative sign** if you reuse that current in other equations.
> 7. **Check:** plug into a loop you *didn't* use; it should come out to zero.

### 19.1 Example: one loop, two opposing batteries

A loop contains $\mathcal E_1$, $\mathcal E_2$ (oriented so they oppose each other), $R_1$, and $R_2$, all in series. Assume $I$ runs clockwise, out of $\mathcal E_1$'s $+$ terminal. Going clockwise, you cross $\mathcal E_1$ from $-$ to $+$ and $\mathcal E_2$ from $+$ to $-$:
$$
+\mathcal E_1-IR_1-\mathcal E_2-IR_2=0\quad\Longrightarrow\quad I=\frac{\mathcal E_1-\mathcal E_2}{R_1+R_2}
$$
If $\mathcal E_2>\mathcal E_1$, then $I<0$: the current runs counterclockwise and the bigger battery wins.

### 19.2 Example: one battery, resistors in parallel (lecture example)

A battery $\mathcal E$ drives $R_1$ and $R_2$ connected in parallel. Unknowns: $I$ (through the battery), $I_1$, $I_2$.
- Junction X: $I-I_1-I_2=0$
- Loop through $R_1$: $\mathcal E-I_1R_1=0$, so $I_1=\mathcal E/R_1$
- Loop through $R_2$: $\mathcal E-I_2R_2=0$, so $I_2=\mathcal E/R_2$
- Loop around $R_1$ and $R_2$ alone (no battery): $-I_2R_2+I_1R_1=0$. Redundant, but it makes a good check.

Then $I=\mathcal E\left(\dfrac1{R_1}+\dfrac1{R_2}\right)$, which is the parallel law.

### 19.3 Example: "rightmost resistor" (based on the Lecture 12 clicker)

A battery $\mathcal E$ has resistor $R_1$ directly across it (one branch), plus a second branch of three resistors $R$, $R$, $R$ in series. Find the voltage across the rightmost resistor.

Loop through the series branch: $\mathcal E-IR-IR-IR=0$, so $I=\mathcal E/3R$ and $\Delta V=IR=\mathcal E/3$. **You don't need the total current.** Pick the loop that contains only what you need.

### 19.4 Example: two batteries, two loops (the classic exam circuit)

```tikz
\usepackage{circuitikz}
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
nc/.style={circle,fill=cneg,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{circuitikz}[american,font=\large]
\draw (0,0) to[battery1,invert,l=$\mathcal{E}_1$] (0,2) to[R,l=$R_1$,i>_=$I_1$] (0,4)
-- (3,4) to[short,*-] (6,4) to[R,l=$R_2$,i<^=$I_2$] (6,2) to[battery1,invert,l=$\mathcal{E}_2$,invert] (6,0)
-- (3,0) to[short,*-] (0,0);
\draw (3,4) to[R,l=$R_3$,i>^=$I_3$] (3,0);
\node[above] at (3,4) {A};
\node[below] at (3,0) {B};
\draw[->,cgry,thick] (1.9,2.8) arc (90:-200:0.6);
\node[cgry,font=\small] at (1.5,0.7) {loop 1};
\draw[->,cgry,thick] (4.1,2.8) arc (90:380:0.6);
\node[cgry,font=\small] at (4.5,0.7) {loop 2};
\end{circuitikz}
\end{document}
```

**Setup.** Three branches run between node A (top) and node B (bottom). Left branch: $\mathcal E_1$ ($+$ on top) with $R_1$. Middle branch: $R_3$. Right branch: $\mathcal E_2$ ($+$ on top) with $R_2$. Assumed currents: $I_1$ up the left branch, $I_2$ up the right branch, $I_3$ down the middle.

**Junction A** (in: $I_1$, $I_2$; out: $I_3$):
$$
I_1+I_2-I_3=0
$$

**Loop 1** (left pane, clockwise, starting at bottom-left): up through $\mathcal E_1$ from $-$ to $+$ gives $+\mathcal E_1$; up through $R_1$ along $I_1$ gives $-I_1R_1$; across the top to A, then down through $R_3$ along $I_3$ gives $-I_3R_3$; back along the bottom wire adds 0.
$$
\mathcal E_1-I_1R_1-I_3R_3=0
$$

**Loop 2** (right pane, counterclockwise, starting at bottom-right): up through $\mathcal E_2$ from $-$ to $+$ gives $+\mathcal E_2$; up through $R_2$ along $I_2$ gives $-I_2R_2$; left to A, then down $R_3$ along $I_3$ gives $-I_3R_3$.
$$
\mathcal E_2-I_2R_2-I_3R_3=0
$$

**Solve.** From the loops, $I_1=\dfrac{\mathcal E_1-I_3R_3}{R_1}$ and $I_2=\dfrac{\mathcal E_2-I_3R_3}{R_2}$. Substitute into the junction equation:
$$
\frac{\mathcal E_1}{R_1}+\frac{\mathcal E_2}{R_2}=I_3\left(1+\frac{R_3}{R_1}+\frac{R_3}{R_2}\right)
$$
Let $D=R_1R_2+R_2R_3+R_1R_3$. Then
$$
\boxed{\ I_3=\frac{\mathcal E_1R_2+\mathcal E_2R_1}{D},\qquad I_1=\frac{\mathcal E_1(R_2+R_3)-\mathcal E_2R_3}{D},\qquad I_2=\frac{\mathcal E_2(R_1+R_3)-\mathcal E_1R_3}{D}\ }
$$

**Special case: all resistors equal to $R$.** Then $D=3R^2$, and
$$I_3=\frac{\mathcal E_1+\mathcal E_2}{3R},\quad I_1=\frac{2\mathcal E_1-\mathcal E_2}{3R},\quad I_2=\frac{2\mathcal E_2-\mathcal E_1}{3R}$$
If $\mathcal E_2>2\mathcal E_1$, then $I_1<0$: current is forced *backwards* through battery 1 (from its $+$ to its $-$ terminal), and battery 1 absorbs energy.

**Check with the outer loop** (counterclockwise from bottom-left: down $R_1$, down $\mathcal E_1$, across, up $\mathcal E_2$, up $R_2$, back across the top). Going down the left branch you cross $R_1$ against $I_1$ ($+I_1R_1$) and $\mathcal E_1$ from $+$ to $-$ ($-\mathcal E_1$). Going up the right branch you get $+\mathcal E_2-I_2R_2$. So the sum should be $I_1R_1-\mathcal E_1+\mathcal E_2-I_2R_2=0$. Substituting the loop equations: $(\mathcal E_1-I_3R_3)-\mathcal E_1+\mathcal E_2-(\mathcal E_2-I_3R_3)=0$ ✓.

### 19.5 Potential difference between two points ("walk the circuit")

To find $V_B-V_A$: start at A, walk **any** path to B, and add up the changes using the **same sign table**:
$$
V_B-V_A=\sum_{\text{A}\to\text{B}}\Delta V
$$
In §19.4: walking from B up the middle branch to A, you cross $R_3$ *against* $I_3$, so $V_A-V_B=+I_3R_3$. Walking up the left branch instead gives $V_A-V_B=\mathcal E_1-I_1R_1$. That's the same number (it's just Loop 1), which makes a good check.

> [!tip] Potential "map" trick
> Set one node to $V=0$ (ground), then go around assigning a potential to every node. Batteries raise $V$ by $\mathcal E$ going $-\to+$. Resistors drop $V$ by $IR$ going along the current. The highest-potential node is always at the $+$ side of some battery, and current flows through resistors from high to low node potential.

### 19.6 Conceptual circuit facts

- **Ideal wire across a resistor ("short"):** the resistor has $\Delta V=0$, so no current goes through it. All the current takes the wire.
- **Open switch / break:** no current in that branch, but there can still be a potential difference across the gap.
- **Adding a resistor in parallel** lowers the total resistance, so more current comes out of the battery. With an ideal battery, the existing parallel branches are unchanged (same $\Delta V$).
- **Adding a resistor in series** raises the total resistance, so there is less current everywhere in that loop.
- **Batteries in series** (same orientation): EMFs add. Opposing: they subtract.
- **Bulb brightness** $\propto P=I^2R$. For identical bulbs, compare the currents.

---

# Part V — Exam Strategy, Common Mistakes, Formula Summary

## 20. What the graders want to see

> [!important] Process > answer
> "We aren't interested so much in your answer (which we already know) but in your process." Show every step from the recipes (§3, §10, §19). Typical rubric items for a distributed-charge problem: a **correct $dq$**, a **correct $\vec r$** (observation − source), a **correct $|\vec r|$**, a **correct $d\vec E$** with components, **symmetry reasoning in words**, **correct limits**, the final integral, then the evaluation.

**Multi-part structure to expect** (based on the recommended old-test problems):
- Distributed charge: (a) write $dq$; (b) write $\vec r$ and $|\vec r|$; (c) write $d\vec E$; (d) set up or evaluate the integral; (e) a limiting case or conceptual question (conductors/polarization).
- Potential: (a) find $\vec E$ in each region; (b) integrate to get $\Delta V$; (c) use $\Delta U=q\Delta V$ and energy conservation to find a speed or KE.
- Circuits: (a) write the junction and loop equations; (b) solve for the currents; (c) find $\Delta V$ between two points; maybe (d) power.

**Upload something for every Gradescope prompt.** You have 15 minutes to scan after the exam.

> [!warning] Official grading rules (from the exam instructions)
> - Solve **algebraically**. An incorrect solution that isn't done algebraically gets an **80% deduction**.
> - Show all steps, **with correct vector notation** (arrows, hats, $\langle\ \rangle$ components).
> - A correct answer without adequate explanation counts as **wrong**.
> - Incorrect work mixed in with correct work counts as wrong, so **cross out** anything you don't want graded.
> - Include diagrams. Label every sub-part and **box final answers**. Symbolic answers carry no units.
> - You may start from anything on the formula sheet unless the problem says *derive*. Anything not on the sheet must be derived.
> - **Stuck on one part?** Invent a symbol for the quantity you couldn't find (say that you're doing it, e.g. "let $E_0$ be the field from part (a)") and use it to finish the rest. This saves a lot of partial credit.

## 21. Top mistakes (and how to avoid them)

1. **$\vec r$ backwards.** It's *observation minus source*. Check: for positive $dq$, $d\vec E$ should point **away** from the piece.
2. **Integrating a magnitude.** Do $E_x$ and $E_y$ separately.
3. **Missing Jacobian factors:** $dq=\lambda R\,d\theta$ (not $\lambda\,d\theta$); $dq=\sigma2\pi r\,dr$ (not $\sigma\,dr$).
4. **Wrong density:** $\lambda=Q/(\text{actual length})$. For an arc, that's $R\Delta\theta$.
5. **Putting the observation coordinate inside the integral as a variable.** $h$, $z$, and $d$ are constants; only the source coordinate gets integrated.
6. **Claiming symmetry when there isn't any.** Off-center points (§4.2) have **two** non-zero components.
7. **Double negatives in $\Delta V$.** Write $d\vec l=+dr\,\hat r$ and let the limits set the direction.
8. **Using one formula across regions.** Shells and balls have different $E(r)$ inside and outside, so split the integral at each boundary.
9. **Loop rule signs.** The battery sign depends on which terminal you enter, not on the current. The resistor sign depends on the current direction compared to your walking direction.
10. **Dropping a negative current** when you substitute it into another equation.
11. **Thinking current gets used up in a resistor.** The current is the same in and out; the potential drops.
12. **$\Delta U$ vs. $\Delta V$:** $\Delta U=q\Delta V$. For an electron, $q=-e$, so the signs flip.

## 22. Sanity checks you can always do

- **Units:** $kQ/L^2$ is a field, $kQ/L$ is a potential, $\mathcal E/R$ is a current.
- **Far-field:** any finite object with net charge $Q$ gives $E\to kQ/d^2$ and $V\to kQ/d$.
- **Symmetric limits:** a full ring gives 0 at its center; a symmetric rod has no component along itself on its bisector.
- **Direction:** $\vec E$ points away from $+$ and toward $-$, and from high $V$ to low $V$.
- **Continuity:** $V$ is always continuous. $E$ jumps only across a charged surface.
- **Circuits:** check an unused loop; check that power supplied equals power dissipated.

## 23. Formula summary

✅ = printed on the formula sheet · 🧠 = must be memorized (the sheet says so) · ✍️ = not given, so derive or justify it on the exam

### Fields
| | | |
|---|---|---|
| Force | $\vec F=q\vec E$ | 🧠 |
| Point charge | $\vec E=kq\vec r/r^3$, $\ \vec r=\vec r_{\text{obs}}-\vec r_{\text{source}}$ | 🧠 |
| Continuous | $\vec E=k\int dq\,\vec r/\lvert\vec r\rvert^3$; $\ dq=\lambda\,dl,\ \sigma\,dA,\ \rho\,dV$ | ✍️ (superposition) |
| Rod, on axis, distance $d$ past the end | $kQ/[d(L+d)]$ | ✍️ |
| Rod, perpendicular bisector | $kQ/[x\sqrt{x^2+(L/2)^2}]$ | ✅ |
| Rod close-up / infinite line | $2k\lambda/s$ | ✅ |
| Arc center, $\theta_1\to\theta_2$ | $\vec E=\frac{k\lambda}{R}\langle-(\sin\theta_2-\sin\theta_1),\ \cos\theta_2-\cos\theta_1\rangle$ | ✍️ |
| Ring on axis | $kQz/(z^2+R^2)^{3/2}$ | ✅ |
| Disk on axis | $2\pi k\sigma\left(1-\lvert z\rvert/\sqrt{z^2+R^2}\right)$ | ✅ |
| Infinite sheet | $2\pi k\sigma=\sigma/2\epsilon_0$ | ✅ |
| Parallel plates | $4\pi k\sigma=\sigma/\epsilon_0$ inside, 0 outside | ✅ (inside value) |
| Shell | $kQ/r^2$ outside, 0 inside | ✍️ justify |
| Uniform ball | $kQ/r^2$ outside, $kQr/R^3$ inside | ✍️ justify |

### Potential
| | | |
|---|---|---|
| Definition | $\Delta V=-\int_i^f\vec E\cdot d\vec l$; $\ U=qV$ | ✅ |
| Energy conservation | $K_i+qV_i=K_f+qV_f$ | 🧠 |
| $\vec E$ from $V$ | $\vec E=-\nabla V$ | ✍️ |
| Uniform field | $\Delta V=-\vec E\cdot\Delta\vec r$; plates: $\lvert\Delta V\rvert=Ed$ | ✍️ (one-line integral) |
| Point charge | $\Delta V=kq(1/r_f-1/r_i)$, so $V=kq/r$ | ✅ |
| Pair energy | $U=kq_1q_2/r$ | ✍️ ($U=qV$ with the point-charge $V$) |
| Line charge | $V_b-V_a=-2k\lambda\ln(r_b/r_a)$ | ✍️ |
| Shell | $kQ/r$ outside, $kQ/R$ inside | ✍️ |
| Ball | $kQ/r$ outside, $kQ(3R^2-r^2)/2R^3$ inside | ✍️ |
| Ring on axis | $kQ/\sqrt{z^2+R^2}$ | ✍️ |
| Disk on axis | $2\pi k\sigma(\sqrt{z^2+R^2}-\lvert z\rvert)$ | ✍️ |

### Circuits
| | | |
|---|---|---|
| Current | $i=nA\bar v$ (electrons/s), $\ I=\lvert q\rvert nA\bar v$ | ✅ |
| Drift | $\bar v=uE$ ($u$ = mobility $=e\tau/m$ in Drude) | ✅ |
| Conductivity / resistivity | $\sigma=1/\rho=\lvert q\rvert nu$, $\ J=I/A=\sigma E$ | ✅ |
| Resistance | $R=L/(\sigma A)=\rho L/A$ | ✅ |
| Ohm | $I=\lvert\Delta V\rvert/R$ | ✅ |
| Power | $P=I\Delta V$ (✅); $I^2R=\Delta V^2/R$, battery $\mathcal EI$ | ✍️ |
| Loop rule | $\sum\Delta V=0$: $\pm\mathcal E$ (− → + is +), $\mp IR$ (with $I$ is −) | ✍️ (energy conservation) |
| Junction rule | $\sum I_{\text{in}}=\sum I_{\text{out}}$ | ✍️ (charge conservation) |
| Series / parallel | $R_s=\sum R_i$; $\ 1/R_p=\sum1/R_i$ | ✍️ |

## 24. Practice plan

From the instructor's recommended list (Canvas → Files → Study Aids → Old Tests; the "Remote" problems are in the 2020 folder):

- **Distributed charge:** Fall 2021 T1 P2, Fall 2014 T1 P4 (polar), Spring 2011 Lab Quiz 2, Fall 2021 T1 P3 (conductor), Fall 2014 T1 P2 / Fall 2015 T1 P3 (polarization), Remote T1 "Metal Mario" and "Quarter" (arc).
- **Potential:** Remote T2 "The charged shells" (§10.6), Remote T2 "The CRT" (§13.2), Fall 2015 T2 P2 and Fall 2021 T2 P2, Fall 2014 T2 P2 and Spring 2011 Lab Quiz 3.
- **Circuits:** Fall 2014 T3 P1, Fall 2014 T3 P2(a–c), Fall 2015 T3 P2(a only), Fall 2021 T2 P3 (parts 1 and 3) / Remote "The RC Circuit" A and C. **Skip the capacitor parts.**
- **GPS 3, 4, 5** and the aiPlato exam review (up to 2 bucket points).

**Method:** solve with no notes. If you succeed, change one thing (move the observation point, change the arc angle, flip a battery) and solve again. Only then move on.
