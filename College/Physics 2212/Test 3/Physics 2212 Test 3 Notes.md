# Physics 2212 — Test 3 Notes (Weeks 8–11)

> [!abstract] What's on Test 3
> **Three problems, symbols only (no numbers, no calculator).** Process is graded, as on Tests 1–2.
>
> | Problem | Topic | Sections |
> |---|---|---|
> | 1 | $\vec B$ from moving charges, currents, and dipoles (any geometry) | §1–§8 |
> | 2 | Magnetic forces on moving charges and their paths | §9–§13 |
> | 3 | Force and torque on loops and dipoles, including dipoles acting on each other | §14–§19 |
>
> - You **won't derive** fields by integrating over a current; you apply the standard results below and add them up.
> - "Dipoles" means both magnetic ($\vec m$) and electric ($\vec p$) ones.
> - Not tested: RC circuits, Gauss's law, flux, Faraday's law, EMF.
> - Earlier material still counts: [[Physics 2212 Test 1 Notes]], [[Physics 2212 Test 2 Notes]].
>
> Short version: [[Physics 2212 Test 3 Review]]. Practice: [[Physics 2212 Test 3 Practice Questions]]. **⚠️** marks results not on the slides that follow directly from them.

> [!info] The formula sheet
> Every formula below is marked:
> - **✅ on the sheet:** start from it directly.
> - **🧠 memorize:** the sheet lists these as "things you must have memorized" (magnetic force on a charge, field of a moving point charge, $\vec F=q\vec E$, point-charge $\vec E$, superposition, Newton's 2nd law, energy conservation).
> - **✍️ not on the sheet:** the exam rule is "if a formula you need is not given, you must derive it," so write the short derivation shown next to it.
>
> **Notation:** the sheet writes $\dfrac{\mu_0}{4\pi}$ where these notes write $k_m$ (they're equal, $10^{-7}$ T·m/A; see §0.3 for what $\mu_0$ is, and §0.4 for every symbol), uses $\vec\mu$ for the dipole moment ($\vec m$ here), and gives dipole and wire fields as **magnitudes**: the direction is always yours to find.
>
> The sheet also prints flux, Gauss's law, Faraday's law, Ampère's law, and radiation formulas. Test 3 doesn't use them.

## Table of Contents
- [[#Part 0 — Tools]]
- [[#Part I — Magnetic Fields]]
- [[#Part II — Magnetic Dipoles]]
- [[#Part III — Force on Moving Charges]]
- [[#Part IV — Forces and Torques on Currents and Dipoles]]
- [[#Part V — Checklist and Formula Summary]]

---

# Part 0 — Tools

## 0.1 The cross product

Almost every magnetism formula has a cross product $\vec A\times\vec B$: a vector perpendicular to both $\vec A$ and $\vec B$, with

$$
\lvert\vec A\times\vec B\rvert=AB\sin\theta\qquad(\theta=\text{angle between them, tail to tail})
$$

- **Direction (right-hand rule):** fingers along $\vec A$, curl them toward $\vec B$; your thumb points along $\vec A\times\vec B$.
- **Unit vectors:** $\hat x\times\hat y=\hat z$, $\hat y\times\hat z=\hat x$, $\hat z\times\hat x=\hat y$. Reversed order gives a minus sign ($\hat y\times\hat x=-\hat z$), and any vector crossed with itself is $0$.
- **Components** ✅ (in the sheet's math help), if the directions aren't obvious:
$$\vec A\times\vec B=(A_yB_z-A_zB_y)\,\hat x+(A_zB_x-A_xB_z)\,\hat y+(A_xB_y-A_yB_x)\,\hat z$$

**Drawing 3D on paper:** $\odot$ is a vector **out of the page** (toward you), $\otimes$ is **into the page**. With $\hat x$ right and $\hat y$ up, $\hat z$ is out of the page.

## 0.2 Two things carried over from electricity

- **Separation vector** $\vec r=\vec r_{\text{obs}}-\vec r_{\text{source}}$ (observation point minus source), $r=|\vec r|$, $\hat r=\vec r/r$.
- **Superposition:** fields from several sources add as vectors (add components, not magnitudes).

## 0.3 The magnetic constant $\mu_0$ (and $k_m$)

**$\mu_0$** ("mu-naught," called the **permeability of free space** or the **magnetic constant**) is a fixed constant of nature. It sets how strong a magnetic field a given current or moving charge produces, the same way $\epsilon_0$ (through $k=\frac1{4\pi\epsilon_0}$) sets how strong an electric field a given charge produces. You never calculate it; it's just a number that appears in every magnetic field formula:

$$
\mu_0=4\pi\times10^{-7}\ \text{T·m/A}
$$

Since it almost always shows up as $\mu_0/4\pi$, the slides give that combination its own name, **$k_m$**:

$$
k_m=\frac{\mu_0}{4\pi}=10^{-7}\ \text{T·m/A}\qquad\left(\mu_0=4\pi k_m\right)
$$
 notes write $k_m$. To switch between forms, replace $\mu_0$ with $4\pi k_m$: e.g. $\dfrac{\mu_0I}{2\pi r}=\dfrac{4\pi k_mI}{2\pi r}=\dfrac{2k_mI}{r}$.
✅ Both are in the sheet's constants table. $k_m$ plays the role in magnetism that $k$ plays in electricity: compare $\vec E=\dfrac{kq}{r^2}\hat r$ with $\vec B=\dfrac{k_mq\,\vec v\times\hat r}{r^2}$. The sheet writes $\dfrac{\mu_0}{4\pi}$ everywhere these

Magnetic field $B$ is measured in **tesla** (T); $1\ \text{T}=1\ \text{N/(A·m)}$.

## 0.4 Symbols used in these notes

| Symbol | Meaning | Units |
|---|---|---|
| $\vec B$ | magnetic field | T (tesla) |
| $\vec E$ | electric field | N/C |
| $\mu_0$, $k_m$ | magnetic constant; $k_m=\mu_0/4\pi$ (§0.3) | T·m/A |
| $k$, $\epsilon_0$ | electric constant; $k=1/(4\pi\epsilon_0)$ | N·m²/C² |
| $q$ | charge of a particle ($+e$ for a proton, $-e$ for an electron) | C |
| $e$ | elementary charge, $1.6\times10^{-19}$ C (always positive) | C |
| $\vec v$, $v$ | particle's velocity, speed | m/s |
| $v_d$ | drift speed of the charges moving in a wire | m/s |
| $\vec r$, $r$, $\hat r$ | separation vector (observation point minus source), its length, its direction | m |
| $I$ | current (direction = where positive charge would flow) | A |
| $d\vec\ell$ (sheet: $\Delta\vec\ell$) | tiny piece of wire, pointing along the current | m |
| $\vec\ell$, $L$ | a wire's length (as a vector along the current), a wire's or solenoid's length | m |
| $s$ | perpendicular distance from a point to a wire | m |
| $R$ | radius (of a ring, arc, or a particle's circular path) | m |
| $z$ | distance along a ring's axis from its center | m |
| $N$ | number of turns of wire | — |
| $A$ | area enclosed by a loop | m² |
| $\vec m$ (sheet: $\vec\mu$) | **magnetic dipole moment** of a loop or magnet | A·m² |
| $m$ | **mass** in $F=ma$ and circular-motion formulas (§10, §12); otherwise the size of $\vec m$. Check which one a formula means | kg |
| $\vec p$ | electric dipole moment, $\vec p=q\vec s$ | C·m |
| $\vec F$, $\vec\tau$, $U$ | force, torque, potential energy | N, N·m, J |
| $\theta$ | an angle (each formula says which one) | rad |
| $\omega$, $T$ | angular frequency and period of circular motion | rad/s, s |
| $\odot$ / $\otimes$ | vector out of / into the page | — |

---

# Part I — Magnetic Fields

## 1. A moving point charge

A charge at rest makes only an electric field. A charge $q$ moving with velocity $\vec v$ also makes a **magnetic field** $\vec B$:

$$
\boxed{\ \vec B=k_m\frac{q\,\vec v\times\vec r}{r^3}\ }\qquad\left(\text{same as }k_m\frac{q\,\vec v\times\hat r}{r^2}\right)
$$

where $q$ is the moving charge (with its sign), $\vec v$ its velocity, $\vec r$ the vector **from the charge to the point** where you want the field, $r=|\vec r|$, and $\hat r=\vec r/r$.

🧠 **Memorize this one**: the sheet lists it as "magnetic field of a moving point charge" without printing it.

- $\vec B$ is perpendicular to both $\vec v$ and $\vec r$, so it **circles the line of motion**.
- Size $k_m|q|v\sin\theta/r^2$, where $\theta$ is the angle between $\vec v$ and $\vec r$. **$\vec B=0$ anywhere on the line of motion** (ahead of or behind the charge).
- A negative charge makes the opposite field.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dotout/.pic={\draw[thick,cacc] (0,0) circle (0.17); \fill[cacc] (0,0) circle (0.05);},
crossin/.pic={\draw[thick,cacc] (0,0) circle (0.17); \draw[thick,cacc] (-0.12,-0.12)--(0.12,0.12) (-0.12,0.12)--(0.12,-0.12);}}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[dashed,cgry] (-3.5,0)--(5.5,0);
\node[cgry,font=\small,anchor=west] at (5.6,0) {$\vec B=0$ on this line};
\draw[vec,cneg] (0.35,0)--(1.7,0) node[below]{$\vec v$};
\node[pc] at (0,0) {$+$};
\foreach \p in {(-2.5,1.4),(-0.5,1.9),(1.5,1.9),(3.5,1.4)} \pic at \p {dotout};
\foreach \p in {(-2.5,-1.4),(-0.5,-1.9),(1.5,-1.9),(3.5,-1.4)} \pic at \p {crossin};
\draw[vec,corg] (0.2,0.12)--(3.3,1.3);
\node[corg] at (2.2,0.35) {$\vec r$};
\node[cacc,font=\small,anchor=west] at (4.1,1.4) {$\vec B$ out of page};
\node[cacc,font=\small,anchor=west] at (4.1,-1.4) {$\vec B$ into page};
\end{tikzpicture}
\end{document}
```

**Example.** A proton ($+e$) passes the origin with velocity $v\hat x$. Find $\vec B$ at $(d,d,0)$.
1. $\vec r=\langle d,d,0\rangle$, $\ r=\sqrt2\,d$, so $r^3=2\sqrt2\,d^3$.
2. $\vec v\times\vec r=v\hat x\times(d\hat x+d\hat y)=vd\,\hat z$.
3. $\vec B=\boxed{\dfrac{k_mev}{2\sqrt2\,d^2}\,\hat z}$ (out of the page, matching the picture: the point is above the line of motion).

**Facts that show up as conceptual questions:**
- $\vec E$ (along $\hat r$) and $\vec B$ (perpendicular to $\vec r$) of a moving charge are **never parallel**.
- If one charge moves straight toward another, its $\vec B$ at the other charge is zero ($\vec v\parallel\vec r$), so it exerts **no magnetic force** on it.

## 2. From charges to currents

A current is many moving charges. A short piece of wire of length $d\ell$ carrying current $I$ acts like a single moving charge with $q\vec v$ replaced by $I\,d\vec\ell$, where $d\vec\ell$ points **along the current** (opposite to the electrons' motion):

$$
d\vec B=k_m\frac{I\,d\vec\ell\times\vec r}{r^3}\qquad\text{(Biot–Savart law)}
$$

where $I$ is the current in the wire, $d\vec\ell$ the small piece of wire (length $d\ell$, pointing along $I$), and $\vec r$ the vector from that piece to the observation point.

✅ On the sheet as $\Delta\vec B=\dfrac{\mu_0}{4\pi}\dfrac{I\Delta\vec\ell\times\hat r}{r^2}$ ("short wire").

Every wire result below comes from adding up these pieces. You only need the results, but this explains two quick rules: a point **along the line of a straight piece** gets no field from it ($d\vec\ell\parallel\vec r$), and **the field always circles the current**.

## 3. Straight wires

**Right-hand rule for wires:** thumb along the current, fingers curl in the direction of $\vec B$. The field lines are circles around the wire.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
vec/.style={-{Stealth[length=3mm]},very thick},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=3mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\foreach \r in {0.9,1.7,2.7} {
  \draw[cacc,thick,mid=0.13] (0,0) circle (\r);
  \draw[cacc,thick,mid=0.63] (0,0) circle (\r);}
\fill[corg] (0,0) circle (0.28);
\fill[white] (0,0) circle (0.08);
\draw[vec,cneg] (0,0)--(-1.53,-2.23);
\node[cneg] at (-1.2,-0.85) {$r$};
\draw[vec,cacc] (2.7,0)--(2.7,1.3) node[right]{$\vec B$};
\node[font=\small,align=left,anchor=west] at (3.3,-1.2) {current $I$ toward you (center):\\ $\vec B$ circles counterclockwise;\\ lines spread out as $B\propto 1/r$};
\end{tikzpicture}
\end{document}
```

**Sizes.** $I$ is the wire's current, $L$ its length, and $s$ the perpendicular distance from the point to the wire's line.

| Wire | $B$ | Sheet |
|---|---|---|
| Length $L$, point on its perpendicular bisector | $\dfrac{k_mIL}{s\sqrt{s^2+(L/2)^2}}$ | ✅ |
| Infinite (or $s\ll L$) | $\dfrac{2k_mI}{s}$ $\left(=\dfrac{\mu_0I}{2\pi s}\right)$ | ✅ |
| Semi-infinite, point beside its end ⚠️ | $\dfrac{k_mI}{s}$ (half of infinite) | ✍️ |
| Any segment ⚠️ | $\dfrac{k_mI}{s}(\sin\theta_2-\sin\theta_1)$ | ✍️ |
| Point on the wire's own line (its extension) | $0$ | ✍️ |

**Deriving the ✍️ rows on the exam:**
- **Semi-infinite:** an infinite wire is two semi-infinite halves meeting at the foot of the perpendicular. By symmetry each half contributes equally, so each gives half of $2k_mI/s$.
- **On the wire's own line:** every piece has $\Delta\vec\ell\parallel\hat r$, so $\Delta\vec\ell\times\hat r=0$ in the sheet's short-wire formula.
- **Any segment:** integrate the short-wire formula (as in practice problem 1.3), or avoid it by building the wire from the cases above.

In the any-segment formula, $\theta_1$ and $\theta_2$ are the angles from the perpendicular (from the point to the wire) to the segment's two ends, negative on one side of the perpendicular and positive on the other. The other rows are special cases of it.

**Limits of the finite wire:** close up ($s\ll L$) it looks infinite, $2k_mI/s$; far away ($s\gg L$) it looks like one moving point charge, $k_mIL/s^2$.

**Two parallel wires** with equal currents a distance $d$ apart, on the line midway between them:
- currents in the **same** direction: the fields point opposite ways and cancel, $\vec B=0$;
- currents in **opposite** directions: the fields add, $B=2\cdot\dfrac{2k_mI}{d/2}=\dfrac{8k_mI}{d}$.

**A flat sheet of current** (current along $+x$ in the $z=0$ plane): think of it as many parallel wires. Their vertical components cancel in pairs, so $\vec B$ points along $-\hat y$ above the sheet and $+\hat y$ below.

## 4. Rings and arcs

**Ring of radius $R$, on its axis** at distance $z$ from the center:

$$
\boxed{\ B=\frac{2\pi k_mIR^2}{(R^2+z^2)^{3/2}}\ }\qquad\text{at the center: }B=\frac{2\pi k_mI}{R}
$$

where $I$ is the ring's current, $R$ its radius, and $z$ the distance from the ring's center to the point, measured along the axis. ✅ On the sheet (with its far-away form). For the center, set $z=0$ in the sheet formula.

- **Direction:** curl your right-hand fingers along the current; your thumb gives $\vec B$ along the axis, the same direction on both sides of the ring.
- Why only the axial part survives: pieces on opposite sides of the ring make sideways components that cancel.
- **Far away** ($z\gg R$): $B\approx 2k_m\dfrac{I\pi R^2}{z^3}$, a dipole field (§7).
- $N$ turns: multiply by $N$.

**Arc of angle $\theta$ (radians), at its center** ⚠️ ✍️ (not on the sheet: write this derivation). In the sheet's short-wire formula, every piece is the same distance $R$ away and perpendicular to $\hat r$, so $|\Delta\vec\ell\times\hat r|=\Delta\ell$ and all the pieces point the same way. Adding them up gives total length $R\theta$:

$$
B=\frac{k_mI\theta}{R}\qquad(\text{full circle }\theta=2\pi\text{ gives }2\pi k_mI/R\ ✓)
$$

where $\theta$ is the angle the arc covers **in radians** (a semicircle is $\pi$, a quarter circle $\pi/2$) and $R$ its radius. Same direction rule as the ring. Straight leads pointing **straight at** the center add nothing.

**Example: a hairpin.** A long wire comes in from the left along $y=+R$, turns around a semicircle of radius $R$ centered at O, and goes back out along $y=-R$. Find $\vec B$ at O.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=3mm]}}}},
mid/.default=0.5,
crossin/.pic={\draw[thick,cacc] (0,0) circle (0.17); \draw[thick,cacc] (-0.12,-0.12)--(0.12,0.12) (-0.12,0.12)--(0.12,-0.12);}}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[corg,line width=2.5pt,mid=0.5] (-5,1.5)--(0,1.5);
\draw[corg,line width=2.5pt,mid=0.5] (0,1.5) arc (90:-90:1.5);
\draw[corg,line width=2.5pt,mid=0.5] (0,-1.5)--(-5,-1.5);
\node[corg] at (-2.5,1.9) {$I$};
\node[corg] at (-2.5,-1.9) {$I$};
\pic at (0,0) {crossin};
\node[anchor=north east] at (-0.1,-0.1) {O};
\draw[dim] (0.2,0)--(1.5,0) node[midway,below]{$R$};
\node[cgry,font=\small] at (-5.6,1.5) {$\cdots$};
\node[cgry,font=\small] at (-5.6,-1.5) {$\cdots$};
\end{tikzpicture}
\end{document}
```

1. **Top wire:** semi-infinite and O is beside its end, so $B=k_mI/R$. Current to the right, O below it: into the page.
2. **Bottom wire:** same size $k_mI/R$. Current to the left, O above it: also into the page.
3. **Semicircle:** $\theta=\pi$, so $B=k_mI\pi/R$. The current goes clockwise around O: into the page.
4. All three point the same way: $\vec B_O=\boxed{\dfrac{k_mI}{R}(2+\pi)}$ into the page.

## 5. The solenoid

A **solenoid** is a coil of $N$ turns over a length $L$ carrying current $I$. It acts like $N$ rings stacked together.

- **Inside** (long solenoid): a uniform field along the axis,
$$\boxed{\ B=\frac{4\pi k_mNI}{L}=\mu_0\frac NLI\ }$$
where $N$ is the number of turns, $L$ the solenoid's length (so $N/L$ is turns per meter), and $I$ the current in the wire. It doesn't depend on the radius or on where you are inside. ✅ on the sheet ($\mu_0NI/L$); direction by the ring rule (fingers along the current in the turns, thumb along $\vec B$).
- **Outside:** the field of a single dipole with moment $M=NIA$ (§6–§7).

---

# Part II — Magnetic Dipoles

## 6. The magnetic dipole moment

Any flat loop of current $I$ enclosing area $A$ has a **magnetic dipole moment** $\vec m$ (also called magnetic moment):

$$
\boxed{\ |\vec m|=IA\quad(NIA\text{ for }N\text{ turns}),\qquad\text{direction: fingers along }I\text{, thumb along }\vec m\ }
$$

where $I$ is the loop's current and $A$ the flat area it encloses ($\pi R^2$ for a circle, $ab$ for an $a\times b$ rectangle). Units A·m². ✅ The sheet gives $\mu=IA=I\pi R^2$ (the sheet calls the moment $\mu$, these notes call it $m$); for $N$ turns, multiply by $N$ (each turn adds its own $IA$). Only the area matters, not the shape. The head of $\vec m$ is the **north pole**, the tail the **south pole**.

**Bar magnets** have moments too, even with no current: each electron is a tiny dipole (its **spin**), and in iron, cobalt, and nickel the spins line up so their moments add. A bar magnet behaves exactly like a current loop with the same $\vec m$, pointing from its S end to its N end.

**Reading $\vec m$ off a loop** (common question): if the current goes counterclockwise as you look at the loop, $\vec m$ points toward you; clockwise, away from you.

## 7. The field of a dipole

Far from any small loop (or magnet), the field depends only on $\vec m$:

$$
\boxed{\ \vec B=k_m\frac{3(\vec m\cdot\hat r)\,\hat r-\vec m}{r^3}\ }
$$

where $\vec m$ is the dipole moment, $\vec r$ the vector from the dipole to the point ($r$ its length, $\hat r$ its direction), and $r$ is much bigger than the loop or magnet. The **axis** is the line through the dipole along $\vec m$; the **equator** is the plane through the dipole perpendicular to $\vec m$.

✍️ This general formula is **not** on the sheet. You'll mostly need two special places, and those **are** on the sheet (as magnitudes):

| Where the point is | $\vec B$ | Sheet |
|---|---|---|
| On the axis (either side) | $\dfrac{2k_m\vec m}{r^3}$, **along** $\vec m$ | ✅ $B_{\text{dipole},\parallel}$ |
| On the equator (perpendicular to $\vec m$) | $-\dfrac{k_m\vec m}{r^3}$, **opposite** $\vec m$, half the size | ✅ $B_{\text{dipole},\perp}$ (size only; you supply "opposite $\vec m$") |

If a problem puts the point at an odd angle (like configuration B in practice problem 1.7), use symmetry or quote the general formula as your starting point.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
vec/.style={-{Stealth[length=3mm]},very thick},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=2.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[dashed,cgry] (0,-3.4)--(0,3.4);
\draw[dashed,cgry] (-4.6,0)--(4.6,0);
\draw[cgry,mid=0.5] (0,0.35) .. controls (0.2,2.4) and (2.2,2.2) .. (2.0,0) .. controls (2.2,-2.2) and (0.2,-2.4) .. (0,-0.35);
\draw[cgry,mid=0.5] (0,0.35) .. controls (-0.2,2.4) and (-2.2,2.2) .. (-2.0,0) .. controls (-2.2,-2.2) and (-0.2,-2.4) .. (0,-0.35);
\draw[corg,line width=2pt] (0,0) ellipse (0.8 and 0.25);
\draw[vec,cpos] (0,-0.15)--(0,0.95) node[right]{$\vec m$};
\draw[vec,cacc] (0,2.4)--(0,3.4);
\node[cacc,anchor=west] at (0.15,2.75) {axis: $\vec B_\parallel=2k_m\vec m/r^3$};
\draw[vec,cacc] (0,-3.4)--(0,-2.4);
\draw[vec,cacc] (3.8,0.5)--(3.8,-0.5);
\node[cacc,anchor=north] at (3.8,-0.6) {equator: $\vec B_\perp=-k_m\vec m/r^3$};
\draw[vec,cacc] (-3.8,0.5)--(-3.8,-0.5);
\end{tikzpicture}
\end{document}
```

This is exactly the electric dipole field ($k\,2\vec p/r^3$ on the axis, $-k\vec p/r^3$ on the equator) with $k\to k_m$ and $\vec p\to\vec m$. The field lines leave the N end, loop around, and come back in at the S end.

**Working backward:** if you're shown far-away field arrows, the arrows on the axis point along $\vec m$ (and the ones on the equator point against it). Then use the right-hand rule to get the current's direction.

**Example: two bar magnets.** Two magnets, each with moment $M$ pointing up ($+\hat y$). The point P is a distance $d$ directly above magnet 2 (on its axis) and a distance $d$ to the right of magnet 1 (on its equator).
- Magnet 2 (axis): $+\dfrac{2k_mM}{d^3}\hat y$.
- Magnet 1 (equator): $-\dfrac{k_mM}{d^3}\hat y$.
- Total: $\vec B=\boxed{\dfrac{k_mM}{d^3}\hat y}$.

## 8. Adding dipole moments

Moments add as vectors, $\vec M=\vec m_1+\vec m_2+\cdots$, and far away the whole thing makes a dipole field with that total.

| System | Total moment |
|---|---|
| Solenoid of $N$ turns | $N\vec m=NIA$, along the axis |
| Toroid (solenoid bent into a doughnut) | $0$: the rings' moments point around a circle and cancel |
| Loop bent along a fold into two flat halves | add each half's moment: e.g. two $w\times w$ halves facing $\hat y$ and $\hat z$ give $Iw^2(\hat y+\hat z)$ |
| Two stacked rings, same current direction | $2\vec m$ |
| Two stacked rings, opposite currents | $0$, but the far field is **not** zero (it's weaker, falling faster than $1/r^3$) |
| A charge $q$ circling with period $T$ | a loop with current $I=q/T$, so $m=\dfrac qT\cdot\pi R^2$ |

---

# Part III — Force on Moving Charges

## 9. The magnetic force

A charge moving through a magnetic field feels

$$
\boxed{\ \vec F=q\vec v\times\vec B\ }\qquad\text{(with an electric field too: }\vec F=q\vec E+q\vec v\times\vec B)
$$

where $q$ is the particle's charge (with its sign), $\vec v$ its velocity, and $\vec B$ the field at the particle's location (made by **something else**: a charge never pushes on itself).

🧠 **Memorize**: the sheet's "relationship: magnetic field and magnetic force."

- Size $|q|vB\sin\theta$, where $\theta$ is the angle between $\vec v$ and $\vec B$. **Zero** if the charge is at rest or moves along $\vec B$.
- $\vec F$ is perpendicular to both $\vec v$ and $\vec B$. Flip the direction for a negative charge.
- **It does no work**, because it's always perpendicular to the motion. So the **speed never changes**; only the direction does. Energy conservation ($K+qV=$ constant) is unaffected by $\vec B$.

**Example.** An electron moves right ($+\hat x$) into a field pointing into the page ($-\hat z$). $\hat x\times(-\hat z)=+\hat y$, and the negative charge flips it: the force points **down**.

**Force between two moving charges:** find the first charge's $\vec B$ at the second (§1), then $\vec F_2=q_2\vec v_2\times\vec B_1$. Two separate sign flips if both are negative: one for the source, one for the target.

## 10. Circular motion

In a uniform field with $\vec v\perp\vec B$, the force is always perpendicular to the velocity with constant size $|q|vB$. That's a centripetal force, so the charge moves in a **circle**. Set $|q|vB=mv^2/R$:

$$
\boxed{\ R=\frac{mv}{|q|B},\qquad \omega=\frac{|q|B}{m},\qquad T=\frac{2\pi m}{|q|B}\ }
$$

where **$m$ is the particle's mass** (not a dipole moment), $v$ its speed, $|q|$ the size of its charge, $B$ the field strength, $R$ the radius of the circle, $\omega$ the angular frequency (radians per second), and $T$ the time for one full circle.

✍️ None of these are on the sheet. Derive them in one line: the sheet gives circular motion as $\left|\dfrac{d\vec p}{dt}\right|_\perp=\dfrac{mv^2}{R}$ ✅, and the force is $|q|vB$ 🧠, so write $|q|vB=mv^2/R$ and solve. Then $\omega=v/R$ and $T=2\pi R/v$.

- The period and angular frequency **don't depend on the speed**: a faster particle moves on a bigger circle and takes the same time.
- **Which way it circles:** find $\vec F$ at one point; the center is in that direction. For $\vec B$ into the page, positive charges go counterclockwise and negative ones clockwise.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
pc/.style={circle,fill=cpos,draw=black,text=white,inner sep=0pt,minimum size=5.5mm},
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=3mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\foreach \x in {-3,-2,...,3} \foreach \y in {-3,-2,...,3} {
  \draw[cgry] (\x-0.08,\y-0.08)--(\x+0.08,\y+0.08) (\x-0.08,\y+0.08)--(\x+0.08,\y-0.08);}
\node[cgry,anchor=west] at (3.3,3) {$\vec B$ into page};
\draw[thick,mid=0.37,mid=0.87] (0,0) circle (2.2);
\draw[dim] (0,0)--(-1.556,1.556) node[midway,above right]{$R$};
\node[pc] at (0,-2.2) {$+$};
\draw[vec,cneg] (0.3,-2.2)--(1.6,-2.2) node[below]{$\vec v$};
\draw[vec,cpos] (0,-1.9)--(0,-0.9) node[right]{$\vec F$};
\node[pc] at (2.2,0) {$+$};
\draw[vec,cneg] (2.2,0.3)--(2.2,1.6) node[right]{$\vec v$};
\draw[vec,cpos] (1.9,0)--(0.9,0) node[above]{$\vec F$};
\end{tikzpicture}
\end{document}
```

**Cyclotron** (a particle accelerator): the particle circles in a uniform $\vec B$ and gets a voltage kick each half turn, so its circle grows. Because $T$ doesn't depend on speed, the kicks can come at a fixed frequency $f=|q|B/(2\pi m)$. ⚠️ It leaves at the outer radius $R$ with speed $v=|q|BR/m$, so $K_{\max}=\dfrac{q^2B^2R^2}{2m}$.

## 11. The general path: a helix

If $\vec v$ has a part along $\vec B$, split it: $\vec v=\vec v_\parallel+\vec v_\perp$. The parallel part feels no force ($\vec v_\parallel\times\vec B=0$), so it stays constant, while the perpendicular part makes a circle of radius $mv_\perp/(|q|B)$. Together: a **helix** around the field lines. ⚠️ It moves forward $v_\parallel T=\dfrac{2\pi mv_\parallel}{|q|B}$ per turn.

## 12. Trajectory problems

> [!example] Recipe: a charge entering a uniform field
> 1. **Force at entry:** $\vec F=q\vec v\times\vec B$ (flip for negative $q$). The circle's center lies in that direction.
> 2. **Radius:** $R=mv/(|q|B)$. If the charge was first accelerated from rest through a potential difference $\Delta V$, get the speed from energy: $\tfrac12mv^2=|q\Delta V|$.
> 3. **Draw the circle** and find where it leaves the field region.
> 4. **Time inside** = (fraction of a full circle) $\times\ T$.
> 5. The **speed** is the same when it leaves.

**Example.** A proton moving right at speed $v$ enters a field $\vec B$ into the page that fills the region $x>0$, crossing the boundary at the origin.
1. $\vec F=ev\hat x\times(-B\hat z)=evB\,\hat y$: up, so it curves counterclockwise.
2. It makes a half circle of radius $R=mv/(eB)$ and leaves at $(0,2R)$, moving left at speed $v$.
3. Time inside: half a period, $\pi m/(eB)$.
4. An electron would curve down (clockwise) on a smaller circle, since its mass is smaller.

**Velocity selector.** $\vec E$ points down and $\vec B$ into the page; a positive charge moves right. The electric force $qE$ is down and the magnetic force $qvB$ is up. They cancel for exactly one speed:

$$
qE=qv_0B\quad\Longrightarrow\quad\boxed{v_0=\frac EB}
$$

✍️ Not on the sheet; write the force balance. Here $E$ and $B$ are the sizes of the two fields and $v_0$ the one speed that passes straight through. Particles with that speed go straight; others bend. The charge's sign and mass don't matter (both forces flip together).

## 13. The Hall effect

Current flows through a strip in a perpendicular field. The magnetic force pushes the drifting charges (drift speed $v_d$) toward one edge; the charge that piles up there makes an electric field $E_H$ across the strip that pushes back. It grows until the forces balance, just like the velocity selector:

$$
eE_H=ev_dB\quad\Longrightarrow\quad E_H=v_dB,\qquad |\Delta V_H|=v_dBw
$$

where $E_H$ is the Hall field across the strip, $v_d$ the drift speed of the moving charges, $\Delta V_H$ the voltage between the two edges, and $w$ the strip's width (the distance between the two edges). ✍️ Not on the sheet; write the force balance.

---

# Part IV — Forces and Torques on Currents and Dipoles

## 14. Force on a current-carrying wire

Replacing $q\vec v$ with $I\,d\vec\ell$ again:

$$
\boxed{\ \vec F=I\vec\ell\times\vec B\ }\ \text{(straight wire, uniform field)},\qquad \vec F=\int I\,d\vec\ell\times\vec B\ \text{(general)}
$$

where $I$ is the wire's current, $\vec\ell$ a vector as long as the wire pointing along the current, and $\vec B$ the field (from something else) at the wire. ✅ On the sheet as $\Delta\vec F=I\Delta\vec\ell\times\vec B$; for a long straight piece in a uniform field, the pieces just add up.

- **Uniform field:** a **closed loop** feels **zero net force** (its pieces' forces cancel), though it can still feel a torque (§17).
- ⚠️ **Uniform field, curved wire:** the force equals that on a straight wire between the same two endpoints. Example: a semicircle of radius $R$ feels $I(2R)B$.
- **Non-uniform field:** find the force on each straight side separately (§15 has the standard example).

## 15. Forces between wires

**Two parallel wires** a distance $d$ apart: wire 1's field at wire 2 is $2k_mI_1/d$, perpendicular to wire 2, so

$$
\boxed{\ \frac FL=\frac{2k_mI_1I_2}{d}\ }\qquad\text{parallel currents attract, opposite currents repel}
$$

(the reverse of charges). Here $F/L$ is the force per meter of wire, $I_1$ and $I_2$ the two currents, and $d$ the distance between the wires. ✍️ Not on the sheet: combine the sheet's wire field ($2k_mI_1/d$ for $r\ll L$) with $\Delta\vec F=I\Delta\vec\ell\times\vec B$. Check directions with the right-hand rule: find $\vec B_1$ at wire 2, then $\vec F_2=I_2\vec L\times\vec B_1$.

**A rectangular loop next to a long wire.** The wire carries $I_1$ upward. The loop carries $I_2$; its sides of length $a$ are parallel to the wire (the near one at distance $d$, carrying current upward), and its sides of length $b$ are perpendicular.

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
vec/.style={-{Stealth[length=3mm]},very thick},
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=3mm]}}}},
mid/.default=0.5,
crossin/.pic={\draw[cacc] (0,0) circle (0.13); \draw[cacc] (-0.09,-0.09)--(0.09,0.09) (-0.09,0.09)--(0.09,-0.09);}}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[corg,line width=3pt,mid=0.85] (0,-2.6)--(0,2.6);
\node[corg] at (-0.45,2.2) {$I_1$};
\draw[cneg,very thick,mid=0.5] (2,-1.25)--(2,1.25);
\draw[cneg,very thick,mid=0.5] (2,1.25)--(5,1.25);
\draw[cneg,very thick,mid=0.5] (5,1.25)--(5,-1.25);
\draw[cneg,very thick,mid=0.5] (5,-1.25)--(2,-1.25);
\node[cneg] at (3.5,0) {$I_2$};
\foreach \p in {(1,1.8),(1,-1.8),(3.5,0.7),(3.5,-0.7),(6,1.8),(6,-1.8)} \pic at \p {crossin};
\node[cacc,font=\small,anchor=west] at (6.25,1.8) {$\vec B_1$ into page};
\draw[vec,cpos] (1.9,0)--(0.9,0) node[above]{$\vec F_{\mathrm{near}}$};
\draw[vec,cpos] (5.1,0)--(5.8,0) node[above]{$\vec F_{\mathrm{far}}$};
\draw[vec,cgry] (3.5,1.35)--(3.5,2.1);
\draw[vec,cgry] (3.5,-1.35)--(3.5,-2.1);
\draw[dim] (0,-3)--(2,-3) node[midway,below]{$d$};
\draw[dim] (2,-3)--(5,-3) node[midway,below]{$b$};
\draw[dim] (6.6,-1.25)--(6.6,1.25) node[midway,right]{$a$};
\end{tikzpicture}
\end{document}
```

1. The wire's field $2k_mI_1/x$ points into the page on this side, weaker farther away.
2. **Near side** (parallel to $I_1$): attracted, force $I_2a\cdot\dfrac{2k_mI_1}{d}$ toward the wire.
3. **Far side** (opposite to $I_1$): repelled, force $I_2a\cdot\dfrac{2k_mI_1}{d+b}$ away from the wire.
4. **Top and bottom sides:** their forces are equal and opposite (one up, one down), so they cancel.
5. Net force, toward the wire:
$$\boxed{\ F=2k_mI_1I_2a\left(\frac1d-\frac1{d+b}\right)\ }$$

The near side wins because it's closer. This is why a closed loop **can** feel a net force when the field isn't uniform.

## 16. Forces between loops and magnets

**The magnetic charge trick.** Treat the north pole (head of $\vec m$) as a **positive** charge and the south pole (tail) as a **negative** charge. Then like poles repel, opposite poles attract, and the **closest poles win**. It works for loops, solenoids, and bar magnets.

| Arrangement of two moments | Closest poles | Result |
|---|---|---|
| Lined up head to tail ($\uparrow$ above $\uparrow$) | N next to S | attract |
| Head to head or tail to tail ($\uparrow$ above $\downarrow$) | S next to S | repel |
| Side by side, parallel ($\uparrow\ \uparrow$) | N next to N, S next to S | repel |
| Side by side, antiparallel ($\uparrow\ \downarrow$) | N next to S | attract |

The same answers come from the wires: two stacked loops with the same circulation have parallel nearest currents (attract); two side-by-side loops have opposite nearest currents (repel).

⚠️ ✍️ **Sizes**, if a problem asks for them (none of this is on the sheet). A dipole in a field has energy $U=-\vec m\cdot\vec B$ (§17), and the force pushes toward lower energy: $\vec F=\nabla(\vec m\cdot\vec B)$. For two moments $m_1,m_2$ a distance $r$ apart:

| Arrangement | Force |
|---|---|
| Head to tail on one axis | attract, $\dfrac{6k_mm_1m_2}{r^4}$ |
| Side by side, parallel | repel, $\dfrac{3k_mm_1m_2}{r^4}$ |

(For example, head to tail: $U=-m_2\cdot\dfrac{2k_mm_1}{r^3}$, and $F=-dU/dr=-\dfrac{6k_mm_1m_2}{r^4}$, negative meaning attractive.)

## 17. Torque on a loop

A uniform field puts **no net force** on a loop, but it **twists** it:

$$
\boxed{\ \vec\tau=\vec m\times\vec B,\qquad\tau=mB\sin\theta\ }
$$

where $\vec\tau$ is the torque (the twist, in N·m), $\vec m$ the loop's dipole moment ($m=NIA$), $\vec B$ the outside field, and $\theta$ the angle between $\vec m$ (perpendicular to the loop) and $\vec B$, **not** between the loop's plane and $\vec B$. ✅ On the sheet ($\vec\tau=\vec\mu\times\vec B$).

- The torque turns $\vec m$ **toward** $\vec B$ and is zero once they line up. That's why a compass needle (a tiny magnet) points along the field.
- **Energy:** $U=-\vec m\cdot\vec B$ ⚠️ ✍️ (not on the sheet). Derive it from the work against the torque: $U(\theta)=\int_{90°}^{\theta}mB\sin\theta'\,d\theta'=-mB\cos\theta$. Lowest ($-mB$) when aligned, which is stable; highest ($+mB$) when opposite. Flipping a dipole from aligned to opposite takes work $2mB$.

**Where it comes from (rectangular loop, sides $a$ and $b$):** two sides of length $b$ feel forces $IbB$, equal and opposite but along different lines. Each has a lever arm $\tfrac a2\sin\theta$ from the center:

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
vec/.style={-{Stealth[length=3mm]},very thick},
dotout/.pic={\draw[thick,corg] (0,0) circle (0.17); \fill[corg] (0,0) circle (0.05);},
crossin/.pic={\draw[thick,corg] (0,0) circle (0.17); \draw[thick,corg] (-0.12,-0.12)--(0.12,0.12) (-0.12,0.12)--(0.12,-0.12);}}
\begin{document}
\begin{tikzpicture}[font=\large]
\coordinate (T) at (-1,1.73);
\coordinate (Bt) at (1,-1.73);
\draw[corg,line width=3pt] (T)--(Bt);
\pic at (T) {dotout};
\pic at (Bt) {crossin};
\fill (0,0) circle (2.5pt);
\draw[dashed,cgry] (-1,1.73)--(-1,0.2);
\draw[cgry] (-1,0.9) arc (-90:-60:0.83);
\node[cgry,font=\small] at (-0.75,0.55) {$\theta$};
\draw[vec,cpos] (-1,2)--(-1,3.3) node[above]{$\vec F_1=IbB\,\hat z$};
\draw[vec,cpos] (1,-2)--(1,-3.3) node[below]{$\vec F_2=-IbB\,\hat z$};
\draw[vec,cneg] (-2.6,-0.6)--(-1.6,-0.6) node[above]{$\vec B$};
\draw[vec,cneg] (2.2,0.6)--(3.4,0.6) node[right]{$\vec B$};
\draw[vec,cacc] (0,0)--(1.73,1) node[right]{$\vec m$};
\draw[cacc] (0.8,0) arc (0:30:0.8);
\draw[dashed,cgry] (0,0)--(1.2,0);
\node[cacc,font=\small] at (1.05,0.25) {$\theta$};
\node[corg,font=\small,anchor=west] at (-0.75,1.95) {current out};
\node[corg,font=\small,anchor=east] at (0.75,-1.95) {current in};
\begin{scope}[xshift=-4.3cm,yshift=-2.6cm]
\draw[->] (0,0)--(0.8,0) node[right]{$y$};
\draw[->] (0,0)--(0,0.8) node[above]{$z$};
\pic at (0,0) {dotout};
\node[anchor=north east] at (-0.1,-0.1) {$x$};
\end{scope}
\end{tikzpicture}
\end{document}
```

$$
\tau=2\cdot\frac a2\sin\theta\cdot IbB=(Iab)B\sin\theta=mB\sin\theta
$$

(the loop is seen edge-on; the other two sides' forces cancel and make no torque).

**Example: same wire, different shape.** A square of side $L$ ($m=IL^2$) has maximum torque $IL^2B$. Bent into a circle, the same wire has $2\pi R=4L$, so $m=I\pi R^2=4IL^2/\pi$. For the circle's torque to equal the square's maximum: $\dfrac{4IL^2B}{\pi}\sin\theta=IL^2B$, so $\sin\theta=\pi/4$.

## 18. Several dipoles acting on each other

> [!example] Recipe: torque or force on dipole 2 from dipole 1
> 1. Is dipole 2 on dipole 1's **axis**, its **equator**, or neither?
> 2. **Field of 1 at 2:** axis $2k_m\vec m_1/r^3$, equator $-k_m\vec m_1/r^3$, otherwise the full formula (§7).
> 3. **Torque:** $\vec\tau_2=\vec m_2\times\vec B_1$.
> 4. **Force:** direction from the magnetic charge trick; size from §16 if needed.
> 5. **Swap roles** for the effect on dipole 1.

**Example.** Two small magnets with equal moments $m$, a distance $d$ apart. The left one points right ($\vec m_L=m\hat x$, at the origin); the right one points up ($\vec m_R=m\hat y$, at $(d,0)$). Released so they can rotate but not move, which way does each start to turn?
1. **Left magnet:** it sits on the right magnet's equator, so $\vec B_R=-\dfrac{k_mm}{d^3}\hat y$ there. $\vec\tau_L=m\hat x\times\left(-\dfrac{k_mm}{d^3}\hat y\right)=-\dfrac{k_mm^2}{d^3}\hat z$: **clockwise**.
2. **Right magnet:** it sits on the left magnet's axis, so $\vec B_L=\dfrac{2k_mm}{d^3}\hat x$ there. $\vec\tau_R=m\hat y\times\dfrac{2k_mm}{d^3}\hat x=-\dfrac{2k_mm^2}{d^3}\hat z$: **clockwise**, twice as strong.

Both turn clockwise; the two torques are **not** equal and opposite.

## 19. Electric dipoles work the same way

An **electric dipole** is charges $\pm q$ a distance $s$ apart, with **electric dipole moment** $\vec p=q\vec s$ (size $qs$, pointing from $-$ to $+$; units C·m). $\vec E$ is the outside electric field and $k=\frac1{4\pi\epsilon_0}$. Swap $\vec m\to\vec p$, $\vec B\to\vec E$, $k_m\to k$:

| | Electric dipole | Magnetic dipole |
|---|---|---|
| Net force in a uniform field | $0$ | $0$ |
| Torque | $\vec p\times\vec E$ (✍️ not on the sheet) | $\vec m\times\vec B$ (✅) |
| Energy | $-\vec p\cdot\vec E$ (✍️) | $-\vec m\cdot\vec B$ (✍️) |
| Field on its axis / equator | $2k\vec p/r^3$ / $-k\vec p/r^3$ (✅) | $2k_m\vec m/r^3$ / $-k_m\vec m/r^3$ (✅) |

Why $\vec p\times\vec E$ (the derivation to write, since it isn't on the sheet): the $+q$ end gets pushed along $\vec E$ and the $-q$ end against it. The two forces cancel but act at opposite ends, so they twist the dipole: torque $=\tfrac{\vec s}{2}\times q\vec E+\left(-\tfrac{\vec s}{2}\right)\times(-q\vec E)=q\vec s\times\vec E$.

---

# Part V — Checklist and Formula Summary

## 20. Before you hand it in

- **Start from the sheet:** quote a ✅ formula by name. If you use a ✍️ result (arc, semi-infinite wire, $R=mv/qB$, $U=-\vec m\cdot\vec B$…), write its one-line derivation first, or it doesn't count.
- **Vector notation:** every field and force has a magnitude **and** a direction ($\hat x$, $\odot$, "into the page"). Box answers. Stuck on one part? Name the missing quantity with a symbol and finish the rest.
- **Signs:** flip for negative charges, separately for the source charge (its $\vec B$) and the charge feeling the force.
- **Cross-product order:** $\vec v\times\vec B$, $d\vec\ell\times\vec r$, $\vec m\times\vec B$, never reversed.
- **Current direction:** $d\vec\ell$ and $\vec\ell$ point along the current, opposite to how the electrons move.
- **Dipole on the equator:** the field points **opposite** $\vec m$ and is half the axis value.
- **Magnetic forces never change speed.**
- **Closed loop:** zero net force only in a **uniform** field.
- **Angle in $mB\sin\theta$:** between $\vec m$ and $\vec B$.
- **How fields fall off:** moving charge $1/r^2$, infinite wire $1/r$, dipole $1/r^3$, force between dipoles $1/r^4$.
- **Quick zeros:** $\vec B=0$ on a charge's line of motion, along a straight wire's own line, and midway between equal parallel currents.

## 21. Formula summary

### Fields

✅ on the sheet · 🧠 memorize · ✍️ derive on the exam

| Source | Field | Sheet |
|---|---|---|
| Moving charge | $\vec B=k_m\dfrac{q\vec v\times\vec r}{r^3}$ | 🧠 |
| Current piece | $d\vec B=k_m\dfrac{I\,d\vec\ell\times\vec r}{r^3}$ | ✅ |
| Wire of length $L$, on its bisector | $\dfrac{k_mIL}{s\sqrt{s^2+(L/2)^2}}$ | ✅ |
| Infinite wire ($s\ll L$) | $\dfrac{2k_mI}{s}$, circling the wire | ✅ |
| Semi-infinite wire, beside its end ⚠️ | $\dfrac{k_mI}{s}$ | ✍️ |
| Any segment ⚠️ | $\dfrac{k_mI}{s}(\sin\theta_2-\sin\theta_1)$ | ✍️ |
| Ring, on axis | $\dfrac{2\pi k_mIR^2}{(R^2+z^2)^{3/2}}$; center ($z=0$) $\dfrac{2\pi k_mI}{R}$ | ✅ |
| Arc, at center ⚠️ | $\dfrac{k_mI\theta}{R}$ | ✍️ |
| Long solenoid, inside | $\dfrac{4\pi k_mNI}{L}$ | ✅ |
| Dipole, axis / equator | $\dfrac{2k_m\vec m}{r^3}$ / $-\dfrac{k_m\vec m}{r^3}$ | ✅ (magnitudes) |
| Dipole, general direction | $k_m\dfrac{3(\vec m\cdot\hat r)\hat r-\vec m}{r^3}$ | ✍️ |
| Dipole moment | $\vec m=NIA$, right-hand rule | ✅ ($IA$) |

### Forces, motion, torque

| Quantity | Formula | Sheet |
|---|---|---|
| Force on a charge | $\vec F=q\vec E+q\vec v\times\vec B$ | 🧠 |
| Circular motion | $\left\lvert\dfrac{d\vec p}{dt}\right\rvert_\perp=\dfrac{mv^2}{R}$ | ✅ |
| Circle in a $B$ field | $R=\dfrac{mv}{\lvert q\rvert B}$, $\ \omega=\dfrac{\lvert q\rvert B}{m}$, $\ T=\dfrac{2\pi m}{\lvert q\rvert B}$ | ✍️ |
| Velocity selector | $v_0=E/B$ | ✍️ |
| Hall field | $E_H=v_dB$ | ✍️ |
| Force on a wire | $\vec F=I\vec\ell\times\vec B$, or $\int I\,d\vec\ell\times\vec B$ | ✅ |
| Parallel wires | $F/L=\dfrac{2k_mI_1I_2}{d}$ | ✍️ |
| Magnetic torque | $\vec\tau=\vec m\times\vec B$ | ✅ |
| Electric torque | $\vec\tau=\vec p\times\vec E$ | ✍️ |
| Dipole energy | $U=-\vec m\cdot\vec B$, $\ -\vec p\cdot\vec E$ | ✍️ |
| Force between dipoles ⚠️ | head to tail $6k_mm_1m_2/r^4$ (attract), side by side $3k_mm_1m_2/r^4$ (repel) | ✍️ |
