# Physics 2212 — Test 3 Practice Questions

> [!abstract] How to use this
> Problems are grouped by the three exam problem types. **Solutions are folded**: try each problem on paper first, then open the "Solution" bar. Every solution names the concept, writes the **general formula first**, and only then plugs in.
>
> **Sources:** GPS 7, 8, 9 and the homework/aiPlato problems you sent. The flux, Faraday's-law (induced EMF/current/field), and Gauss's-law problems are left out because Test 3 doesn't cover them.
>
> Theory: [[Physics 2212 Test 3 Notes]] · Quick version: [[Physics 2212 Test 3 Review]]

> [!tip] The toolbox every solution uses
>
> | Tool | Formula |
> |---|---|
> | Separation vector | $\vec r=\vec r_{\text{obs}}-\vec r_{\text{source}}$ |
> | Moving charge | $\vec B=k_m\dfrac{q\,\vec v\times\vec r}{r^3}$ |
> | Current piece | $d\vec B=k_m\dfrac{I\,d\vec\ell\times\vec r}{r^3}$ |
> | Infinite wire / semi-infinite wire beside its end | $\dfrac{2k_mI}{s}$ / $\dfrac{k_mI}{s}$ |
> | Arc of angle $\theta$, at its center | $\dfrac{k_mI\theta}{R}$ |
> | Ring center / dipole axis / dipole equator | $\dfrac{2\pi k_mI}{R}$ / $\dfrac{2k_m\vec m}{r^3}$ / $-\dfrac{k_m\vec m}{r^3}$ |
> | Dipole moment | $\vec m=NIA$, right-hand rule |
> | Forces | $\vec F=q\vec v\times\vec B$, $\ \vec F=I\vec\ell\times\vec B$ |
> | Torque, energy, force on a dipole | $\vec\tau=\vec m\times\vec B$, $\ U=-\vec m\cdot\vec B$, $\ \vec F=\nabla(\vec m\cdot\vec B)$ |
>
> $k_m=\mu_0/4\pi=10^{-7}$ T·m/A. Answers may use either: $2k_m=\mu_0/2\pi$, $4\pi k_m=\mu_0$.

## Contents
- [[#Part 1 — Magnetic Fields]]
  - [[#1.1 A moving electric dipole]] · [[#1.2 Field of a proton at a general point]] · [[#1.3 L-shaped wire]] · [[#1.4 Rectangle with a half-loop]] · [[#1.5 Bar magnet and a coil]] · [[#1.6 Three loops on one axis]] · [[#1.7 Four magnets around a point]]
- [[#Part 2 — Forces on Moving Charges]]
  - [[#2.1 Electron and proton passing each other]] · [[#2.2 Electron near a wire]] · [[#2.3 Neon mass spectrometer]] · [[#2.4 True or false: charges]]
- [[#Part 3 — Force and Torque on Loops and Dipoles]]
  - [[#3.1 Long wire and rectangular loop]] · [[#3.2 Current loop among four magnets]] · [[#3.3 Loop, bar magnet, and wire above it]] · [[#3.4 Flipping a bar magnet]] · [[#3.5 Dipole in a non-uniform field]] · [[#3.6 True or false: loops]]
- [[#Answer Key]]

---

# Part 1 — Magnetic Fields

## 1.1 A moving electric dipole
*GPS 7, Problem 1*

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
vec/.style={-{Stealth[length=3mm]},very thick}}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[->,cgry] (-4,0)--(4,0) node[right]{$x$};
\draw[->,cgry] (0,-3)--(0,3) node[above]{$y$};
\draw[dashed,cgry] (-1,-3)--(-1,3);
\draw[dashed,cgry] (1,-3)--(1,3);
\draw[line width=3pt,black!70] (-1,0)--(1,0);
\node[nc] at (-1,0) {$-$};
\node[pc] at (1,0) {$+$};
\draw[vec,cacc] (0,-0.1)--(0,-1.5) node[right]{$\vec v$};
\node[cgry,font=\small] at (-1,3.3) {$x=-a$};
\node[cgry,font=\small] at (1,3.3) {$x=+a$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A permanent electric dipole ($+e$ at $\langle a,0,0\rangle$, $-e$ at $\langle -a,0,0\rangle$) moves **down** with velocity $\vec v=-v\hat y$. Describe the net magnetic field in each region of the $xy$-plane: between the dashed lines, on them, and outside them. Where is it zero?

> [!success]- Solution
> **Concept:** each moving charge makes its own field, and the net field is the sum (superposition).
> $$\vec B=k_m\frac{q\,\vec v\times\vec r}{r^3}$$
>
> **The $+e$ charge** at $\langle a,0,0\rangle$: $\vec r=\langle x-a,\ y,\ 0\rangle$.
> $$\vec v\times\vec r=(-v\hat y)\times\big((x-a)\hat x+y\hat y\big)=-v(x-a)(\hat y\times\hat x)=v(x-a)\,\hat z$$
> $$\vec B_+=k_m\frac{ev(x-a)}{r_+^3}\,\hat z$$
> Out of the page to the right of $x=a$, into the page to the left, zero on the line $x=a$ (its own line of motion).
>
> **The $-e$ charge** at $\langle -a,0,0\rangle$: same steps with $q=-e$ and $x-a\to x+a$:
> $$\vec B_-=-k_m\frac{ev(x+a)}{r_-^3}\,\hat z$$
> Into the page to the right of $x=-a$, out of the page to the left.
>
> Every field is along $\pm\hat z$ (in or out of the page), because $\vec v$ and $\vec r$ both lie in the page.
>
> | Region | $\vec B_+$ | $\vec B_-$ | Net |
> |---|---|---|---|
> | Between the lines ($-a<x<a$) | into | into | into the page (they add: strongest here) |
> | On the line $x=+a$ | 0 | into | into the page |
> | On the line $x=-a$ | into | 0 | into the page |
> | Right of $x=+a$, near the $x$-axis | out (closer, stronger) | into | out of the page |
> | Right of $x=+a$, far above or below | out | into (bigger factor $x+a$) | into the page |
> | Left of $x=-a$ | into | out (closer near the axis) | mirror image: out near the axis, into far above/below |
>
> **Zero:** outside each dashed line the two fields point opposite ways. Near the $x$-axis the closer charge wins (out); far above or below, the two distances are nearly equal and the larger lever factor $(x+a)$ wins (into). So the net field crosses zero along a **curve** in each outside region; mark the "x"s there. It's never zero between the lines or on them.
>
> **Variation:** reverse the velocity (dipole moving up). Every field flips, so every "in" becomes "out" and vice versa; the zero curves stay put.

## 1.2 Field of a proton at a general point
*GPS 7, Problem 2*

> [!question] Problem
> A proton at $\vec r_{\text{proton}}=\langle0,d,0\rangle$ has velocity $\vec v=\langle v_x,v_y,0\rangle$. Find at $\vec r_{\text{obs}}=\langle r_x,0,r_z\rangle$:
> 1. the separation vector $\vec r$;
> 2. $\vec v\times\hat r$;
> 3. the magnitude of the proton's magnetic field.

> [!success]- Solution
> **Part 1.** Observation minus source:
> $$\vec r=\vec r_{\text{obs}}-\vec r_{\text{source}}=\langle r_x,0,r_z\rangle-\langle0,d,0\rangle=\boxed{\langle r_x,\,-d,\,r_z\rangle},\qquad r=\sqrt{r_x^2+d^2+r_z^2}$$
>
> **Part 2.** Cross product in components:
> $$\vec A\times\vec B=\langle A_yB_z-A_zB_y,\ A_zB_x-A_xB_z,\ A_xB_y-A_yB_x\rangle$$
> With $\vec A=\vec v=\langle v_x,v_y,0\rangle$ and $\vec B=\vec r=\langle r_x,-d,r_z\rangle$:
> $$\vec v\times\vec r=\langle v_yr_z-0,\ \ 0-v_xr_z,\ \ -v_xd-v_yr_x\rangle$$
> Divide by $r$ to use $\hat r=\vec r/r$:
> $$\boxed{\vec v\times\hat r=\frac{\langle v_yr_z,\ -v_xr_z,\ -(v_xd+v_yr_x)\rangle}{\sqrt{r_x^2+d^2+r_z^2}}}$$
>
> **Part 3.** Field of a moving charge, with $q=+e$:
> $$|\vec B|=k_m\frac{e\,|\vec v\times\vec r|}{r^3}$$
> $$|\vec B|=\boxed{\frac{k_me\sqrt{(v_x^2+v_y^2)r_z^2+(v_xd+v_yr_x)^2}}{(r_x^2+d^2+r_z^2)^{3/2}}}$$
> (Using $(v_yr_z)^2+(v_xr_z)^2=(v_x^2+v_y^2)r_z^2$.)
>
> **Variation:** make it an electron. The magnitude is the same; the direction flips.

## 1.3 L-shaped wire
*GPS 7, Problem 3*

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=3.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[->,cgry] (0,0)--(3.5,0) node[right]{$x$};
\draw[->,cgry] (0,0)--(0,2) node[above]{$y$};
\draw[cneg,line width=3pt,mid=0.6] (-4,0)--(0,0);
\draw[cneg,line width=3pt,mid=0.5] (0,0)--(0,-3.5);
\node[cneg] at (-2,0.45) {$I$};
\node[cneg] at (0.45,-2) {$I$};
\node at (2,0) {$\times$};
\draw[dim] (0,0.45)--(2,0.45) node[midway,above]{$d$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A current $I$ comes in along the negative $x$-axis (from $-\infty$ to the origin), turns, and leaves along the negative $y$-axis (to $-\infty$). Find the magnetic field at $\langle d,0,0\rangle$:
> 1. the direction, by sketch;
> 2. $d\vec B$ from a piece $d\vec L$ at $\langle -x,0,0\rangle$;
> 3. $d\vec B$ from a piece $d\vec L$ at $\langle 0,-y,0\rangle$;
> 4. the net field.

> [!success]- Solution
> **Concept:** Biot–Savart, one piece at a time:
> $$d\vec B=k_m\frac{I\,d\vec L\times\vec r}{r^3}$$
>
> **Part 2 (horizontal piece).** $d\vec L=dx\,\hat x$ (current flows $+x$). $\vec r=\langle d,0,0\rangle-\langle -x,0,0\rangle=\langle d+x,0,0\rangle$, which is parallel to $d\vec L$:
> $$d\vec L\times\vec r=dx\,(d+x)\,(\hat x\times\hat x)=0\quad\Longrightarrow\quad\boxed{d\vec B=0}$$
> The point lies on this wire's own line, so the whole horizontal wire contributes nothing.
>
> **Part 3 (vertical piece).** $d\vec L=-dy\,\hat y$ (current flows $-y$). $\vec r=\langle d,0,0\rangle-\langle0,-y,0\rangle=\langle d,\,y,\,0\rangle$, $r=\sqrt{d^2+y^2}$.
> $$d\vec L\times\vec r=(-dy\,\hat y)\times(d\hat x+y\hat y)=-d\,dy\,(\hat y\times\hat x)=d\,dy\,\hat z$$
> $$\boxed{d\vec B=k_m\frac{I\,d\,dy}{(d^2+y^2)^{3/2}}\,\hat z}$$
>
> **Part 4.** Add up the vertical wire, $y=0\to\infty$, using $\int\frac{dy}{(y^2+a^2)^{3/2}}=\frac{y}{a^2\sqrt{y^2+a^2}}$:
> $$\vec B=k_mId\,\hat z\int_0^\infty\frac{dy}{(d^2+y^2)^{3/2}}=k_mId\left[\frac{y}{d^2\sqrt{d^2+y^2}}\right]_0^\infty\hat z=k_mId\cdot\frac1{d^2}\,\hat z=\boxed{\frac{k_mI}{d}\,\hat z}$$
> That's the semi-infinite-wire result: half of an infinite wire's $2k_mI/d$.
>
> **Part 1 (sketch):** out of the page ($+\hat z$). Check with the right-hand rule: thumb down along the vertical wire, and your fingers come out of the page on its right side.
>
> **Variation:** move the point to $\langle d,-d,0\rangle$. Now the horizontal wire contributes too (also out of the page, by symmetry the same size as the vertical one's).

## 1.4 Rectangle with a half-loop
*GPS 8, Problem 1*

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=3.5mm]}}}},
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[->,cgry] (0,0)--(0,2.4) node[above]{$y$};
\draw[->,cgry] (3,0)--(4.3,0) node[right]{$x$};
\draw[->,cgry,dashed] (0,0)--(-1.6,-1.44) node[below left]{$z$};
\draw[cpos,line width=2.5pt,mid=0.55] (-3,0)--(-1,0);
\draw[cpos,line width=2.5pt,mid=0.5] (-1,0) arc (180:0:1);
\draw[cpos,line width=2.5pt] (1,0)--(3,0)--(2.2,-0.72);
\draw[cpos,line width=2.5pt,mid=0.5] (2.2,-0.72)--(-3.8,-0.72);
\draw[cpos,line width=2.5pt] (-3.8,-0.72)--(-3,0);
\fill (0,0) circle (2.5pt);
\node[anchor=north west] at (0.05,-0.05) {O};
\draw[->,cgry] (0,0)--(-0.6,0.8);
\node[cgry] at (-0.55,0.35) {$R$};
\node[cpos] at (-2,0.35) {$I$};
\node at (0.9,-1.15) {$L$ (front edge, at $z=w$)};
\node at (3.2,-0.6) {$w$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A wire forms an $L\times w$ rectangle in the $xz$-plane. The back long side lies on the $x$-axis, except that at its middle it bulges up into a semicircle of radius $R$ in the $xy$-plane, centered on the origin O. Current $I$ runs along the back side in the $+x$ direction (over the semicircle) and comes back along the front side (at $z=w$) in the $-x$ direction. At O, find:
> 1. the direction of the field from the half-loop alone;
> 2. its magnitude;
> 3. the direction of the field from the front side (length $L$) alone;
> 4. the net field, for $w\ll L$, neglecting the two short sides;
> 5. how including the two short sides would change it.

> [!success]- Solution
> **Parts 1–2 (half-loop).** **Concept:** an arc of angle $\theta$ at its center.
> $$B=\frac{k_mI\theta}{R}\qquad\Longrightarrow\qquad B_{\text{half}}=\frac{k_mI\pi}{R}=\boxed{\frac{\mu_0I}{4R}}$$
> **Direction**, from $d\vec\ell\times\hat r$ at the top of the arc: the current there runs $+\hat x$ and $\hat r$ points from the wire down to O, $-\hat y$:
> $$\hat x\times(-\hat y)=-\hat z\qquad\Longrightarrow\qquad\boxed{-\hat z}$$
>
> **The straight parts of the back side** lie on the $x$-axis, the same line as O, so they contribute **zero** ($d\vec\ell\parallel\vec r$).
>
> **Part 3 (front side).** Current $-\hat x$, and O is a distance $w$ behind it, so $\hat r=-\hat z$:
> $$(-\hat x)\times(-\hat z)=\hat x\times\hat z=-\hat y\qquad\Longrightarrow\qquad\boxed{-\hat y}$$
>
> **Part 4.** **Concept:** finite wire on its bisector (O is opposite the middle of the front side):
> $$B=\frac{k_mIL}{w\sqrt{w^2+(L/2)^2}}\ \xrightarrow{\ w\ll L\ }\ \frac{2k_mI}{w}\quad\text{(looks infinite from close up)}$$
> Add the two pieces as vectors:
> $$\boxed{\vec B_O=-\frac{2k_mI}{w}\,\hat y-\frac{\pi k_mI}{R}\,\hat z=-\frac{\mu_0I}{2\pi w}\,\hat y-\frac{\mu_0I}{4R}\,\hat z}$$
>
> **Part 5.** The right short side carries current $+\hat z$ at $x=L/2$: $\hat z\times(-\hat x)=-\hat y$. The left one carries $-\hat z$ at $x=-L/2$: $(-\hat z)\times\hat x=-\hat y$. Both add a little more in the $-\hat y$ direction, so $|B_y|$ grows slightly (by an amount that's small because they're short and far away).

## 1.5 Bar magnet and a coil
*GPS 8, Problem 2*

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
magN/.style={fill=cpos,draw=black,text=white,minimum width=5mm,minimum height=5mm,inner sep=0pt,font=\small},
magS/.style={fill=cneg,draw=black,text=white,minimum width=5mm,minimum height=5mm,inner sep=0pt,font=\small}}
\begin{document}
\begin{tikzpicture}[font=\large]
\node at (0,3.5) {part 1};
\draw[->,cgry] (-2.6,0)--(2.6,0) node[right]{$x$};
\draw[->,cgry] (0,-2.6)--(0,2.6) node[above]{$y$};
\node[magS] at (0,0.25) {S};
\node[magN] at (0,-0.25) {N};
\foreach \p in {(0,2),(0,-2),(2,0),(-2,0)} \node[cacc] at \p {$\times$};
\begin{scope}[xshift=7.5cm]
\node at (0,3.5) {parts 2--4};
\draw[->,cgry] (-3,0)--(3.2,0) node[right]{$x$};
\draw[->,cgry] (0,-2.2)--(0,2.6) node[above]{$y$};
\node[magS] at (-2,0.25) {S};
\node[magN] at (-2,-0.25) {N};
\fill[corg] (1.6,-0.12) rectangle (2.4,0.12);
\node[corg,font=\small] at (2,-0.5) {coil ($xz$-plane)};
\draw[dim] (-2,1.2)--(0,1.2) node[midway,above]{$d$};
\draw[dim] (0,1.2)--(2,1.2) node[midway,above]{$d$};
\fill (0,0) circle (2.5pt);
\end{scope}
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> 1. A bar magnet (S on top, N on the bottom) sits at the origin in the $xy$-plane. Sketch $\vec B$ at the four marked points, each a distance $d$ away, paying attention to relative sizes.
> 2. Now the magnet is moved to $\langle -d,0,0\rangle$, and a coil ($N$ turns, radius $R\ll d$, current $I$) lying in the $xz$-plane is centered at $\langle d,0,0\rangle$. The two fields exactly cancel at the origin. Which way does the coil's current go?
> 3. Find the magnet's dipole moment $\mu$ in terms of $N$, $I$, $R$.
> 4. The magnet is rotated $90°$ clockwise (seen from $+z$). Find the net field at the origin.

> [!success]- Solution
> **Concept:** a magnet is a dipole whose $\vec m$ points from S to N. Here S is on top, so $\vec m=-m\hat y$.
> $$\text{axis: }\vec B=\frac{2k_m\vec m}{r^3}\qquad\text{equator: }\vec B=-\frac{k_m\vec m}{r^3}$$
>
> **Part 1.**
> - Points on the $y$-axis (top and bottom) are on the magnet's **axis**: $\vec B=\dfrac{2k_m\vec m}{d^3}$, pointing **down** ($-\hat y$, along $\vec m$) at both, length 2.
> - Points on the $x$-axis are on its **equator**: $\vec B=-\dfrac{k_m\vec m}{d^3}$, pointing **up** ($+\hat y$, against $\vec m$), length 1 (half as long).
>
> **Part 2.** The origin is on the magnet's equator (the magnet points along $y$, the origin is off to its side):
> $$\vec B_{\text{mag}}=-\frac{k_m(-\mu\hat y)}{d^3}=+\frac{k_m\mu}{d^3}\hat y$$
> The coil lies in the $xz$-plane, so its axis is the $y$ direction, and the origin (in the coil's plane, off to the side) is on the coil's **equator**. To cancel, the coil must give $-\hat y$ there:
> $$-\frac{k_m\vec m_{\text{coil}}}{d^3}=-\frac{k_m\mu}{d^3}\hat y\quad\Longrightarrow\quad\vec m_{\text{coil}}=+m_{\text{coil}}\hat y$$
> A moment along $+\hat y$ means the current runs **counterclockwise as seen from $+y$** (looking down on the coil).
>
> **Part 3.** Equal distances and both on equators, so the moments must be equal. A coil's moment is $NIA$:
> $$\mu=m_{\text{coil}}=NIA=\boxed{NI\pi R^2}$$
>
> **Part 4.** Rotating $-\hat y$ by $90°$ clockwise gives $-\hat x$, so the magnet now points along $-\hat x$, straight away from the origin. The origin is now on the magnet's **axis**:
> $$\vec B_{\text{mag}}=\frac{2k_m(-\mu\hat x)}{d^3}=-\frac{2k_m\mu}{d^3}\hat x$$
> The coil is unchanged: $-\dfrac{k_m\mu}{d^3}\hat y$. Sum:
> $$\boxed{\vec B=-\frac{k_mNI\pi R^2}{d^3}\left(2\hat x+\hat y\right)},\qquad|\vec B|=\frac{\sqrt5\,k_mNI\pi R^2}{d^3}$$

## 1.6 Three loops on one axis
*GPS 8, Problem 3*

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry}}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[->,cgry] (-1.5,0)--(8,0) node[right]{$z$};
\foreach \z/\lab/\dir in {0/1/-1,3.2/2/1,6.4/3/-1} {
  \draw[thick] (\z,0) ellipse (0.35 and 1.2);
  \fill (\z,0) circle (2pt);
  \node at (\z+0.7,-0.4) {\lab};
  \draw[-{Stealth[length=3mm]},very thick,cneg] (\z-0.35,-0.25*\dir)--(\z-0.35,0.35*\dir);}
\draw[dim] (0,1.6)--(3.2,1.6) node[midway,above]{$D$};
\draw[dim] (3.2,1.6)--(6.4,1.6) node[midway,above]{$D$};
\draw[dim] (-0.9,0)--(-0.9,1.2) node[midway,left]{$R$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> Three identical loops (radius $R$, current $I$) lie in planes perpendicular to the $z$-axis, spaced $D\gg R$ apart. The two outer loops circulate the same way; the middle one circulates the opposite way (the arrows show the current on the side nearest you). Points 1, 2, 3 are the loops' centers.
> 1. Where is the net field largest?
> 2. Where is it smallest?
> 3. Is it zero at any numbered point?
> 4. Is it zero anywhere else on the $z$-axis?

> [!success]- Solution
> **Concept:** superposition of ring fields. Each loop is huge at its own center and a weak dipole field everywhere else.
> $$\text{own center: }B_0=\frac{2\pi k_mI}{R}\qquad\text{distance }z\gg R\text{ on the axis: }\frac{2k_mm}{z^3}=\frac{2\pi k_mIR^2}{z^3}$$
> Call the far field at distance $D$: $b=\dfrac{2\pi k_mIR^2}{D^3}$. Then at distance $2D$ it's $b/8$. Since $D\gg R$, $b\ll B_0$.
>
> **Directions.** The outer loops' moments point one way along $z$ (call it $-\hat z$, from the right-hand rule on the arrows); the middle loop's moment points the other way ($+\hat z$). On the axis, each loop's field points along its own moment.
>
> | Point | Own loop | Neighbor at $D$ | Loop at $2D$ | Net size |
> |---|---|---|---|---|
> | 1 | $B_0$ ($-\hat z$) | $b$ ($+\hat z$, loop 2) | $b/8$ ($-\hat z$, loop 3) | $B_0-\tfrac78b$ |
> | 2 | $B_0$ ($+\hat z$) | $b$ ($-\hat z$, loop 1) | $b$ ($-\hat z$, loop 3, also at $D$) | $B_0-2b$ |
> | 3 | $B_0$ ($-\hat z$) | $b$ ($+\hat z$) | $b/8$ ($-\hat z$) | $B_0-\tfrac78b$ |
>
> 1. **Largest at points 1 and 3** (tied): only one opposing neighbor is close.
> 2. **Smallest at point 2:** both neighbors oppose it at distance $D$.
> 3. **Zero at none of them**, since $B_0\gg b$.
> 4. **Yes, twice.** Between loops 1 and 2: near loop 1 its field ($-\hat z$) dominates; near loop 2 its field ($+\hat z$) dominates. The field changes sign in between, so it passes through zero (just past the midpoint, toward loop 2, because loop 3 adds a little $-\hat z$). By symmetry, again between loops 2 and 3. Beyond the outer loops, the nearest loop (an outer one, $-\hat z$) always beats the middle loop, which is farther away with the same moment, so there's no zero there.

## 1.7 Four magnets around a point
*Homework problem 2(a)–(c)*

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry},
magN/.style={fill=cpos,draw=black,text=white,minimum width=5mm,minimum height=5mm,inner sep=0pt,font=\small},
magS/.style={fill=cneg,draw=black,text=white,minimum width=5mm,minimum height=5mm,inner sep=0pt,font=\small}}
\begin{document}
\begin{tikzpicture}[font=\large]
\node at (0,3.4) {configuration A};
\draw[thick] (0,2.4)--(2.4,0)--(0,-2.4)--(-2.4,0)--cycle;
\node[magN] at (0,2.65) {N}; \node[magS] at (0,2.15) {S};
\node[magN] at (0,-2.15) {N}; \node[magS] at (0,-2.65) {S};
\node[magS] at (-2.4,0.25) {S}; \node[magN] at (-2.4,-0.25) {N};
\node[magS] at (2.4,0.25) {S}; \node[magN] at (2.4,-0.25) {N};
\fill (0,0) circle (2.5pt) node[below]{O};
\draw[dim] (0.1,0)--(2.1,0) node[midway,above]{$d$};
\begin{scope}[xshift=7.5cm]
\node at (0,3.4) {configuration B};
\draw[thick] (-1.8,1.8)--(1.8,1.8)--(1.8,-1.8)--(-1.8,-1.8)--cycle;
\node[magN] at (-1.8,2.05) {N}; \node[magS] at (-1.8,1.55) {S};
\node[magN] at (1.8,2.05) {N}; \node[magS] at (1.8,1.55) {S};
\node[magS] at (-1.8,-1.55) {S}; \node[magN] at (-1.8,-2.05) {N};
\node[magS] at (1.8,-1.55) {S}; \node[magN] at (1.8,-2.05) {N};
\node[font=\small] at (-1.8,2.65) {1};
\node[font=\small] at (1.8,2.65) {3};
\node[font=\small] at (-1.8,-2.65) {4};
\node[font=\small] at (1.8,-2.65) {2};
\fill (0,0) circle (2.5pt) node[below]{O};
\draw[dim] (-1.6,1.6)--(-0.1,0.1) node[midway,above right]{$d$};
\end{scope}
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> Four fixed magnets, each with moment $m_0$, sit a distance $d$ from point O.
> 1. Configuration A (diamond): find the direction of $\vec B$ at O.
> 2. Find its magnitude.
> 3. Configuration B (square, magnets at the corners): find $\vec B$ at O.

> [!success]- Solution
> **Concept:** superposition of dipole fields. For each magnet, $\vec m$ points from S to N; then decide whether O is on its axis or its equator.
> $$\text{axis: }\frac{2k_m\vec m}{d^3}\qquad\text{equator: }-\frac{k_m\vec m}{d^3}$$
>
> **Parts 1–2 (configuration A).**
>
> | Magnet | $\vec m$ | Where O is | Field at O |
> |---|---|---|---|
> | Top | $+\hat y$ (N on top) | on its axis (directly below) | $+\dfrac{2k_mm_0}{d^3}\hat y$ |
> | Bottom | $+\hat y$ | on its axis (directly above) | $+\dfrac{2k_mm_0}{d^3}\hat y$ |
> | Left | $-\hat y$ (N on bottom) | on its equator (off to the side) | $-\dfrac{k_m(-m_0\hat y)}{d^3}=+\dfrac{k_mm_0}{d^3}\hat y$ |
> | Right | $-\hat y$ | on its equator | $+\dfrac{k_mm_0}{d^3}\hat y$ |
>
> All four point the same way:
> $$\vec B_O=(2+2+1+1)\frac{k_mm_0}{d^3}\hat y=\boxed{\frac{6k_mm_0}{d^3}\,\hat y=\frac{3\mu_0m_0}{2\pi d^3}\,\hat y}$$
> Direction $+\hat y$; magnitude $6k_mm_0/d^3$.
>
> **Part 3 (configuration B).** Now O is at $45°$ from every magnet: neither axis nor equator. Use the general dipole formula:
> $$\vec B=k_m\frac{3(\vec m\cdot\hat r)\hat r-\vec m}{d^3}$$
> **Shortcut:** this expression doesn't change if $\hat r\to-\hat r$ (it appears twice), and it flips sign if $\vec m\to-\vec m$. Magnets 1 and 2 are at opposite corners (so their $\hat r$'s are opposite) and point opposite ways ($+\hat y$ and $-\hat y$), so their fields at O cancel exactly. Same for magnets 3 and 4.
> $$\boxed{\vec B_O=0}$$
> (Check one pair explicitly: magnet 1 at the top left has $\hat r=\tfrac{1}{\sqrt2}\langle1,-1\rangle$ and $\vec m=m_0\hat y$, so $\vec m\cdot\hat r=-m_0/\sqrt2$ and $\vec B_1=\tfrac{k_mm_0}{d^3}\langle-\tfrac32,\tfrac12\rangle$. Magnet 2 gives $\tfrac{k_mm_0}{d^3}\langle\tfrac32,-\tfrac12\rangle$. They cancel ✓.)

---

# Part 2 — Forces on Moving Charges

## 2.1 Electron and proton passing each other
*GPS 9, Problem 1*

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
dim/.style={{Stealth[length=2mm]}-{Stealth[length=2mm]},cgry}}
\begin{document}
\begin{tikzpicture}[font=\large]
\node[pc] at (0,2.5) {$+$};
\draw[vec,cacc] (-0.3,2.5)--(-1.8,2.5) node[above]{$\vec v$};
\node[nc] at (0,0) {$-$};
\draw[vec,cacc] (0.3,0)--(1.8,0) node[below]{$\vec v$};
\draw[dashed,cgry] (0,0.3)--(0,2.2);
\draw[dim] (0.8,0.05)--(0.8,2.45) node[midway,right]{$d$};
\draw[->] (-3.5,0.6)--(-2.8,0.6) node[right]{$x$};
\draw[->] (-3.5,0.6)--(-3.5,1.3) node[above]{$y$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> An electron ($-e$) at the origin moves in the $+x$ direction with speed $v$. A proton ($+e$) a distance $d$ directly above it moves in the $-x$ direction with the same speed.
> 1. Direction of the electron's field at the proton?
> 2. Direction of the proton's field at the electron?
> 3. Magnetic force on the proton (magnitude and direction)?
> 4. Magnetic force on the electron?

> [!success]- Solution
> **Concept:** first the **source** charge's field at the other charge, then the force on the **target** charge.
> $$\vec B=k_m\frac{q_{\text{source}}\,\vec v_{\text{source}}\times\vec r}{r^3}\qquad\vec F=q_{\text{target}}\,\vec v_{\text{target}}\times\vec B$$
>
> **Part 1.** Source: electron. $\vec r$ from the electron up to the proton is $d\hat y$.
> $$\vec v\times\vec r=v\hat x\times d\hat y=vd\,\hat z\qquad\vec B_e=k_m\frac{(-e)vd}{d^3}\hat z=\boxed{-\frac{k_mev}{d^2}\,\hat z}\ \text{(into the page)}$$
>
> **Part 2.** Source: proton. $\vec r$ from the proton down to the electron is $-d\hat y$.
> $$\vec v\times\vec r=(-v\hat x)\times(-d\hat y)=vd\,\hat z\qquad\vec B_p=k_m\frac{(+e)vd}{d^3}\hat z=\boxed{+\frac{k_mev}{d^2}\,\hat z}\ \text{(out of the page)}$$
>
> **Part 3.** Target: proton, $q=+e$, $\vec v=-v\hat x$, in field $\vec B_e$:
> $$\vec F_p=e(-v\hat x)\times\left(-\frac{k_mev}{d^2}\hat z\right)=\frac{k_me^2v^2}{d^2}(\hat x\times\hat z)=\boxed{-\frac{k_me^2v^2}{d^2}\,\hat y}$$
> Down, toward the electron.
>
> **Part 4.** Target: electron, $q=-e$, $\vec v=v\hat x$, in field $\vec B_p$:
> $$\vec F_e=(-e)(v\hat x)\times\frac{k_mev}{d^2}\hat z=-\frac{k_me^2v^2}{d^2}(\hat x\times\hat z)=\boxed{+\frac{k_me^2v^2}{d^2}\,\hat y}$$
> Up, toward the proton. They attract magnetically (as well as electrically). **Check:** both are currents in the $-x$ direction (an electron moving $+x$ is a current in $-x$), and parallel currents attract ✓.
>
> **Variation:** make both particles move in $+x$. Now the currents are opposite and the magnetic forces become repulsive.

## 2.2 Electron near a wire
*GPS 9, Problem 2*

> [!question] Problem
> A long wire along the $x$-axis carries $6.3$ A in the $-x$ direction. An electron at $\langle0,-0.003,0\rangle$ m has velocity $\langle-2\times10^5,\,-2.4\times10^5,\,0\rangle$ m/s.
> 1. Find $\vec B$ from the wire at the electron.
> 2. Find the magnetic force on the electron.
> 3. Find the force if it were a proton instead.

> [!success]- Solution
> **Part 1.** **Concept:** infinite wire.
> $$B=\frac{2k_mI}{s}=\frac{2(10^{-7})(6.3)}{0.003}=4.2\times10^{-4}\ \text{T}$$
> **Direction** from $d\vec\ell\times\hat r$: current $-\hat x$; $\hat r$ points from the wire down to the electron, $-\hat y$:
> $$(-\hat x)\times(-\hat y)=\hat x\times\hat y=\hat z\qquad\Longrightarrow\qquad\boxed{\vec B=\langle0,\,0,\,4.2\times10^{-4}\rangle\ \text{T}}$$
>
> **Part 2.** **Concept:** $\vec F=q\vec v\times\vec B$. Cross product in components (with $\vec B=B_z\hat z$ only):
> $$\vec v\times\vec B=\langle v_yB_z,\ -v_xB_z,\ 0\rangle=\langle(-2.4\times10^5)(4.2\times10^{-4}),\ -(-2\times10^5)(4.2\times10^{-4}),\ 0\rangle=\langle-100.8,\ 84,\ 0\rangle$$
> Multiply by $q=-1.6\times10^{-19}$ C:
> $$\boxed{\vec F=\langle1.61\times10^{-17},\ -1.34\times10^{-17},\ 0\rangle\ \text{N}}\qquad|\vec F|=2.1\times10^{-17}\ \text{N}$$
>
> **Part 3.** Same $\vec v\times\vec B$, opposite charge, so the force flips:
> $$\boxed{\vec F_p=\langle-1.61\times10^{-17},\ 1.34\times10^{-17},\ 0\rangle\ \text{N}}$$

## 2.3 Neon mass spectrometer
*Homework problem 5(a)–(d)*

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
vec/.style={-{Stealth[length=3mm]},very thick},
dotout/.pic={\draw[cgry] (0,0) circle (0.12); \fill[cgry] (0,0) circle (0.035);}}
\begin{document}
\begin{tikzpicture}[font=\large]
\fill[cgry,fill opacity=0.12] (0,-3) rectangle (4,3);
\draw[line width=3pt] (0,0.3)--(0,3);
\draw[line width=3pt] (0,-0.3)--(0,-3);
\foreach \x in {1,2,3} \foreach \y in {-2,-1,1,2} \pic at (\x,\y) {dotout};
\node[cgry] at (2,3.4) {$\vec B=B\hat z$ (out of page)};
\draw[vec,cpos] (-2.2,0)--(-0.05,0);
\node[cpos,above] at (-1.2,0.05) {ion beam};
\node[cpos,below] at (-1.2,-0.05) {$\vec v=v\hat x$};
\draw[->] (-3.5,-2.5)--(-2.8,-2.5) node[right]{$x$};
\draw[->] (-3.5,-2.5)--(-3.5,-1.8) node[above]{$y$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> Singly ionized neon ions ($q=+e$) enter a detector through a small hole with velocity $v\hat x$, into a uniform field $B\hat z$ (out of the page). Two streams, $a$ and $b$, are measured with radii $R_a>R_b$.
> 1. Sketch both trajectories with the correct direction of curvature.
> 2. Which stream is neon-22 (heavier) and which is neon-20?
> 3. Starting from the magnetic force, derive $\Delta m=|m_a-m_b|$.
> 4. A third stream $c$ has $R_c=R_b/2$. What's the best physical explanation?

> [!success]- Solution
> **Part 1.** **Concept:** the force direction at entry tells you where the center of the circle is.
> $$\vec F=q\vec v\times\vec B=e\,v\hat x\times B\hat z=evB(\hat x\times\hat z)=-evB\,\hat y$$
> The force is **down** at the entrance, so both streams curve **downward** (clockwise): each makes a **half circle** and hits the wall below the hole, stream $a$ at distance $2R_a$ and stream $b$ at $2R_b$ (closer to the hole).
>
> **Part 2.** **Concept:** the radius of circular motion. Newton's second law with the magnetic force as the centripetal force:
> $$|q|vB=\frac{mv^2}{R}\quad\Longrightarrow\quad R=\frac{mv}{|q|B}$$
> Same $q$, $v$, $B$ for both, so $R\propto m$. The bigger circle is the heavier ion: **$a$ is neon-22, $b$ is neon-20.**
>
> **Part 3.** Solve the same equation for the mass:
> $$evB=\frac{mv^2}{r}\quad\Longrightarrow\quad m=\frac{eBr}{v}$$
> $$\Delta m=|m_a-m_b|=\left|\frac{eBR_a}{v}-\frac{eBR_b}{v}\right|=\boxed{\frac{eB}{v}(R_a-R_b)}$$
>
> **Part 4.** $R=\dfrac{mv}{qB}$, so halving $R$ means halving $m/q$. Neon with half the mass doesn't exist, but **doubling the charge** does it: stream $c$ is **doubly ionized neon-20** ($q=2e$, same mass as $b$).

## 2.4 True or false: charges
*Homework problem 1(a), (d)*

> [!question] Problem
> 1. A charged particle falls through a region with a non-zero magnetic field. Gravity does work on it, but the magnetic force does not.
> 2. A point charge at rest feels no force from a bar magnet that is also at rest.

> [!success]- Solution
> 1. **True.** $\vec F=q\vec v\times\vec B$ is always perpendicular to $\vec v$, so $dW=\vec F\cdot\vec v\,dt=0$. The magnetic force only bends the path; gravity is what speeds the particle up.
> 2. **True.** The magnetic force $q\vec v\times\vec B$ needs $\vec v\ne0$, and a neutral magnet makes no electric field. No force.

---

# Part 3 — Force and Torque on Loops and Dipoles

## 3.1 Long wire and rectangular loop
*GPS 9, Problem 3 (also homework 22.10.2)*

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
mid/.default=0.5}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[cneg,line width=3pt,mid=0.9] (0,-2)--(0,2.5);
\node[cneg] at (-0.45,2.2) {$I_1$};
\draw[cneg,very thick,mid=0.75] (2,1.2)--(5,1.2);
\draw[cneg,very thick] (5,1.2)--(5,-0.8)--(2,-0.8)--(2,1.2);
\node[cneg] at (4.4,1.6) {$I_2$};
\draw[dashed] (0,0.2)--(2,0.2);
\node at (1,0.55) {$d$};
\node at (3.5,-1.2) {$w$};
\node at (5.35,0.2) {$h$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A long wire carries $I_1$ upward. A rectangular loop (height $h$, width $w$) in the same plane carries $I_2$ clockwise; its left side is a distance $d$ from the wire. Find $B_l$ and $B_r$ (the wire's field at the left and right sides), the forces $F_l$ and $F_r$ on those sides, and the net force on the loop.

> [!success]- Solution
> **Concept:** the wire's field isn't uniform ($B\propto1/s$), so find the force on each side of the loop separately, then add.
> $$B=\frac{2k_mI_1}{s}\qquad\vec F=I_2\vec\ell\times\vec B$$
>
> **Field.** To the right of an upward current, the right-hand rule gives $\vec B$ **into the page**.
> $$B_l=\frac{2k_mI_1}{d}=\frac{\mu_0I_1}{2\pi d}\qquad B_r=\frac{2k_mI_1}{d+w}=\frac{\mu_0I_1}{2\pi(d+w)}$$
>
> **Left side.** Clockwise means the left side's current runs **up**, parallel to $I_1$, so it's **attracted** (toward the wire, $-\hat x$). Check: $\hat y\times(-\hat z)=-\hat x$ ✓.
> $$F_l=I_2hB_l=\frac{\mu_0I_1I_2h}{2\pi d}$$
> **Right side.** Current runs **down**, opposite to $I_1$, so it's **repelled** ($+\hat x$):
> $$F_r=I_2hB_r=\frac{\mu_0I_1I_2h}{2\pi(d+w)}$$
> **Top and bottom.** Equal fields along each, opposite currents, so their forces (up and down) cancel.
>
> **Net.** The left side is closer, so it wins:
> $$\vec F=-(F_l-F_r)\hat x=\boxed{-\frac{\mu_0I_1I_2h}{2\pi}\left(\frac1d-\frac1{d+w}\right)\hat x=-\frac{\mu_0I_1I_2hw}{2\pi d(d+w)}\,\hat x}$$
> Toward the wire.
>
> **Variation:** make the loop counterclockwise. Every force flips: the net force pushes the loop away.

## 3.2 Current loop among four magnets
*Homework problem 2(d)–(e)*

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=3mm]}}}},
mid/.default=0.5,
magN/.style={fill=cpos,draw=black,text=white,minimum width=5mm,minimum height=5mm,inner sep=0pt,font=\small},
magS/.style={fill=cneg,draw=black,text=white,minimum width=5mm,minimum height=5mm,inner sep=0pt,font=\small}}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[thick] (0,2.4)--(2.4,0)--(0,-2.4)--(-2.4,0)--cycle;
\node[magN] at (0,2.65) {N}; \node[magS] at (0,2.15) {S};
\node[magN] at (0,-2.15) {N}; \node[magS] at (0,-2.65) {S};
\node[magS] at (-2.4,0.25) {S}; \node[magN] at (-2.4,-0.25) {N};
\node[magS] at (2.4,0.25) {S}; \node[magN] at (2.4,-0.25) {N};
\draw[cacc,very thick,mid=0.1,mid=0.6] (0,0) circle (0.7);
\node[cacc] at (1,0.5) {$I$};
\draw[->] (-3.6,1.6)--(-2.9,1.6) node[right]{$x$};
\draw[->] (-3.6,1.6)--(-3.6,2.3) node[above]{$y$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A small current loop (moment $\vec m$, current $I$ counterclockwise as seen in the drawing) is placed at O in configuration A of problem 1.7, in the same plane as the magnets, free to move and rotate.
> 1. What is the direction of the torque on the loop?
> 2. What is the direction of the net force on the loop?

> [!success]- Solution
> **From 1.7:** the magnets' field at O is $\vec B=\dfrac{6k_mm_0}{d^3}\hat y$.
>
> **Part 1.** **Concept:** torque on a dipole.
> $$\vec\tau=\vec m\times\vec B$$
> Counterclockwise as you look at it means $\vec m$ points **toward you**: $\vec m=m\hat z$.
> $$\vec\tau=m\hat z\times\frac{6k_mm_0}{d^3}\hat y=\frac{6k_mmm_0}{d^3}(\hat z\times\hat y)=\boxed{-\frac{6k_mmm_0}{d^3}\,\hat x}$$
> Around the $-x$ axis: the loop tips so that $\vec m$ swings from out of the page toward $+\hat y$, lining up with $\vec B$.
>
> **Part 2.** **Concept:** a dipole feels a net force only where the field changes across it, $\vec F=\nabla(\vec m\cdot\vec B)$; here $\vec m\cdot\vec B=mB_z$.
> - Every magnet lies in the plane, so their field **in** the plane has no $z$-component: $B_z=0$ all over the plane, and so do its $x$- and $y$-slopes.
> - Moving slightly out of the plane, the top magnet makes $B_z$ change one way and the bottom magnet (same orientation, mirror position) the other way, by the same amount; the side magnets contribute nothing to it.
>
> Everything cancels:
> $$\boxed{\vec F=0}$$
> The loop rotates but doesn't move.

## 3.3 Loop, bar magnet, and wire above it
*Homework problem 4(a)–(g)*

```tikz
\usetikzlibrary{arrows.meta,decorations.markings,calc}
\definecolor{cpos}{RGB}{214,39,40}
\definecolor{cneg}{RGB}{31,119,180}
\definecolor{cacc}{RGB}{39,158,85}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\tikzset{
mid/.style={postaction={decorate},decoration={markings,mark=at position #1 with {\arrow{Stealth[length=3mm]}}}},
mid/.default=0.5,
magN/.style={fill=cpos,draw=black,text=white,minimum width=5.5mm,minimum height=5mm,inner sep=0pt,font=\small},
magS/.style={fill=cneg,draw=black,text=white,minimum width=5.5mm,minimum height=5mm,inner sep=0pt,font=\small}}
\begin{document}
\begin{tikzpicture}[font=\large]
\draw[thick,mid=0.55] (-1.5,0.45)--(2.5,0.45);
\draw[thick,mid=0.55] (2.5,0.45)--(1.5,-0.45);
\draw[thick,mid=0.55] (1.5,-0.45)--(-2.5,-0.45);
\draw[thick,mid=0.55] (-2.5,-0.45)--(-1.5,0.45);
\node at (-2.8,-0.75) {$I_0$};
\fill (0,0) circle (2.5pt);
\node[below] at (0.1,-0.05) {O};
\draw[dashed] (0,0)--(0,4);
\fill (0,4) circle (2.5pt);
\node[anchor=east] at (-0.6,4) {P};
\node at (0.3,2) {$z$};
\node at (0.6,0.75) {$\ell$};
\node at (2.4,-0.25) {$w$};
\begin{scope}[shift={(0,4)},rotate=-45]
\node[magS,rotate=-45] at (-0.3,0) {S};
\node[magN,rotate=-45] at (0.3,0) {N};
\end{scope}
\draw[->,cgry] (0,4.8) arc (90:-40:0.8);
\node[cgry] at (1.05,4.75) {$\theta$};
\begin{scope}[shift={(-4.2,2.5)}]
\draw[->] (0,0)--(0,0.9) node[above]{$\hat z$};
\draw[->] (0,0)--(0.9,0) node[right]{$\hat y$};
\draw[->] (0,0)--(-0.55,-0.5) node[below left]{$\hat x$};
\end{scope}
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A rectangular loop (width $w$ along $x$, length $\ell$ along $y$) lies in the $xy$-plane centered on O, carrying current $I_0$ clockwise as seen from above. P is on the $z$-axis at height $z\gg w,\ell$.
> 1. Find the loop's dipole moment $\vec m_L$.
> 2. Find $\vec B$ at P.
> 3. A bar magnet with moment $\vec m_B$ (in the $yz$-plane, at angle $\theta>90°$ from the $+z$ axis, N end lower) is released at P. Find the torque's magnitude.
> 4. How does the magnet rotate?
> 5. Which way is the force on the magnet?
> 6. The magnet is replaced by a long wire through P along the $y$-axis, current $I$ in the $-y$ direction. Which way is the force on the wire?
> 7. Which way does the loop rotate because of that wire?

> [!success]- Solution
> **Part 1.** **Concept:** dipole moment of a flat loop.
> $$\vec m=IA\,\hat n\quad\text{(right-hand rule: fingers along the current, thumb along }\vec m)$$
> The area is $A=w\ell$. Clockwise seen from above means the thumb points down:
> $$\boxed{\vec m_L=-I_0w\ell\,\hat z}$$
>
> **Part 2.** **Concept:** P is far away and on the loop's axis:
> $$\vec B=\frac{2k_m\vec m}{r^3}\quad\Longrightarrow\quad\boxed{\vec B(P)=-\frac{2k_mI_0w\ell}{z^3}\,\hat z=-\frac{\mu_0I_0w\ell}{2\pi z^3}\,\hat z}$$
>
> **Part 3.** **Concept:** torque on a dipole, $|\vec\tau|=m_BB\sin\phi$, where $\phi$ is the angle between $\vec m_B$ and $\vec B$. $\vec B$ points along $-\hat z$, so $\phi=180°-\theta$, and $\sin(180°-\theta)=\sin\theta$:
> $$\boxed{\tau=m_BB\sin\theta=\frac{2k_mm_BI_0w\ell}{z^3}\sin\theta}$$
>
> **Part 4.** The torque turns $\vec m_B$ **toward $\vec B$**, which points straight down. The magnet rotates within the $yz$-plane (about the $x$-axis) until its N end points straight down at the loop, swinging the N end down toward the dashed axis. (Formally: $\vec m_B\times\vec B\propto-m_{B,y}\hat x$, about the $-x$ axis.)
>
> **Part 5.** **Concept:** magnetic charges, closest poles win. The loop's $\vec m_L$ points down, so its **top face is an S pole**. The magnet's **N end** is the lower end, the one nearer the loop. N near S attracts, so the force points **down, toward the loop** ($-\hat z$).
>
> **Part 6.** **Concept:** force on a wire, $\vec F=I\vec\ell\times\vec B$. At P, $\vec B$ (from part 2) points $-\hat z$ and the wire's current is $-\hat y$:
> $$(-\hat y)\times(-\hat z)=\hat y\times\hat z=\hat x\qquad\Longrightarrow\qquad\boxed{+\hat x}$$
>
> **Part 7.** **Concept:** the wire's field at the loop, then $\vec\tau=\vec m_L\times\vec B$.
> - **Field.** The loop is below the wire. With the current along $-\hat y$ and $\hat r=-\hat z$ (down to the loop): $(-\hat y)\times(-\hat z)=\hat x$, so $\vec B_{\text{wire}}$ points $+\hat x$ at the loop.
> - **Torque.**
> $$\vec\tau=\vec m_L\times\vec B=(-m_L\hat z)\times(B\hat x)=-m_LB(\hat z\times\hat x)=-m_LB\,\hat y$$
> - **Rotation.** The loop rotates about the $y$-axis so that its $\vec m_L$ (now pointing down) swings toward $+\hat x$. Physically, the front edge (the $+x$ side) tips **up** and the back edge tips **down**.

## 3.4 Flipping a bar magnet
*Homework 22.8.2*

> [!question] Problem
> A bar magnet on a table has its moment $\vec\mu$ along $+x$. A uniform field $\vec B$ points along $-x$. You slowly rotate the magnet until $\vec\mu$ points along $\vec B$.
> 1. Find the initial torque.
> 2. Find the work done by your hand.

> [!success]- Solution
> **Part 1.** **Concept:** torque on a dipole.
> $$\tau=\mu B\sin\theta$$
> Initially $\vec\mu$ and $\vec B$ are opposite, so $\theta=180°$:
> $$\tau=\mu B\sin180°=\boxed{0}$$
> It's an **unstable** equilibrium: any small nudge and the field flips the magnet around.
>
> **Part 2.** **Concept:** potential energy of a dipole.
> $$U=-\vec\mu\cdot\vec B=-\mu B\cos\theta$$
> $$U_i=-\mu B\cos180°=+\mu B,\qquad U_f=-\mu B\cos0°=-\mu B$$
> "Slowly" means no kinetic energy is gained, so all the energy change goes through your hand:
> $$W_h=\Delta U=U_f-U_i=\boxed{-2\mu B}$$
> Negative: the field does the turning, and your hand only holds it back.
>
> **Variation:** start with $\vec\mu$ along $\vec B$ and rotate it to point against $\vec B$. Now $W_h=+2\mu B$, since you have to force it.

## 3.5 Dipole in a non-uniform field
*Homework 22.7.3(d)*

> [!question] Problem
> A dipole of fixed magnitude $\mu$ lies in the $xy$-plane in the field $\vec B(x,y)=\dfrac{B_0}{L}\langle x,\,-y,\,0\rangle$. Its moment makes angle $\theta$ with the $+x$ axis. Find the magnitude of the magnetic force for any $\theta$.

> [!success]- Solution
> **Concept:** a dipole in a non-uniform field feels a force pushing it toward lower energy:
> $$U=-\vec\mu\cdot\vec B\qquad\vec F=-\nabla U=\nabla(\vec\mu\cdot\vec B)$$
>
> **Dot product**, with $\vec\mu=\mu\langle\cos\theta,\sin\theta,0\rangle$:
> $$\vec\mu\cdot\vec B=\frac{\mu B_0}{L}\left(x\cos\theta-y\sin\theta\right)$$
> **Gradient** ($\theta$ is fixed, so only $x$ and $y$ vary):
> $$\vec F=\left\langle\frac{\partial}{\partial x},\frac{\partial}{\partial y},\frac{\partial}{\partial z}\right\rangle(\vec\mu\cdot\vec B)=\frac{\mu B_0}{L}\langle\cos\theta,\,-\sin\theta,\,0\rangle$$
> **Magnitude:**
> $$|\vec F|=\frac{\mu B_0}{L}\sqrt{\cos^2\theta+\sin^2\theta}=\boxed{\frac{\mu B_0}{L}}$$
> It's the same for every angle; only the direction changes with $\theta$.

## 3.6 True or false: loops
*Homework problem 1(b), (c), (j)*

> [!question] Problem
> 1. A circular loop and a square loop with the same dipole moment feel the same **non-zero** magnetic force in a constant magnetic field.
> 2. A circular loop and a square loop with the same dipole moment (perpendicular to the field) feel the same non-zero magnetic **torque** in a constant magnetic field.
> 3. Any two adjacent turns of a tightly wound solenoid repel each other.

> [!success]- Solution
> 1. **False.** In a uniform field every closed loop feels **zero** net force: $\vec F=I\left(\oint d\vec\ell\right)\times\vec B=0$.
> 2. **True.** $\vec\tau=\vec m\times\vec B$ depends only on $\vec m$, not the shape. Same $\vec m$, same torque, and it's non-zero because $\vec m\perp\vec B$.
> 3. **False.** Neighboring turns carry current in the **same** direction, and parallel currents **attract**. (Equivalently: the turns are stacked dipoles lined up head to tail, which attract.)

---

# Answer Key

| # | Final answer(s) |
|---|---|
| 1.1 | Into the page between and on the dashed lines; outside: out near the axis, into far above/below; zero along a curve outside each line |
| 1.2 | $\vec r=\langle r_x,-d,r_z\rangle$; $\ \vec v\times\hat r=\frac{\langle v_yr_z,-v_xr_z,-(v_xd+v_yr_x)\rangle}{\sqrt{r_x^2+d^2+r_z^2}}$; $\ B=\frac{k_me\sqrt{(v_x^2+v_y^2)r_z^2+(v_xd+v_yr_x)^2}}{(r_x^2+d^2+r_z^2)^{3/2}}$ |
| 1.3 | $d\vec B=0$ (horizontal); $\ d\vec B=\frac{k_mId\,dy}{(d^2+y^2)^{3/2}}\hat z$; $\ \vec B=\frac{k_mI}{d}\hat z$ |
| 1.4 | $-\hat z$; $\ \frac{\mu_0I}{4R}$; $\ -\hat y$; $\ \vec B=-\frac{\mu_0I}{2\pi w}\hat y-\frac{\mu_0I}{4R}\hat z$; short sides add a little more $-\hat y$ |
| 1.5 | Axis points: $2k_m\mu/d^3$ down; equator points: $k_m\mu/d^3$ up; counterclockwise from $+y$; $\ \mu=NI\pi R^2$; $\ \vec B=-\frac{k_mNI\pi R^2}{d^3}(2\hat x+\hat y)$ |
| 1.6 | Largest: 1 and 3; smallest: 2; zero at none; zero once between 1–2 and once between 2–3 |
| 1.7 | $+\hat y$; $\ \frac{6k_mm_0}{d^3}$; $\ \vec B=0$ in configuration B |
| 2.1 | $-\hat z$; $\ +\hat z$; $\ \vec F_p=-\frac{k_me^2v^2}{d^2}\hat y$; $\ \vec F_e=+\frac{k_me^2v^2}{d^2}\hat y$ |
| 2.2 | $\vec B=4.2\times10^{-4}\hat z$ T; $\ \vec F_e=\langle1.61,-1.34,0\rangle\times10^{-17}$ N; $\ \vec F_p=\langle-1.61,1.34,0\rangle\times10^{-17}$ N |
| 2.3 | Both curve down (half circles); $a$ = Ne-22, $b$ = Ne-20; $\ \Delta m=\frac{eB}{v}(R_a-R_b)$; $c$ = doubly ionized Ne-20 |
| 2.4 | True; True |
| 3.1 | $\vec F=-\frac{\mu_0I_1I_2hw}{2\pi d(d+w)}\hat x$ (toward the wire) |
| 3.2 | $\vec\tau=-\frac{6k_mmm_0}{d^3}\hat x$; $\ \vec F=0$ |
| 3.3 | $\vec m_L=-I_0w\ell\hat z$; $\ \vec B(P)=-\frac{\mu_0I_0w\ell}{2\pi z^3}\hat z$; $\ \tau=\frac{\mu_0m_BI_0w\ell}{2\pi z^3}\sin\theta$; N end swings to point straight down; force toward the loop ($-\hat z$); wire: $+\hat x$; loop: $\vec\tau\propto-\hat y$, front edge tips up |
| 3.4 | $\tau=0$; $\ W_h=-2\mu B$ |
| 3.5 | $F=\frac{\mu B_0}{L}$ |
| 3.6 | False; True; False |
