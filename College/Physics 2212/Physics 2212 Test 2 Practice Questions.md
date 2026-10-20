# Physics 2212 — Test 2 Practice Questions

> [!abstract] How to use this
> Problems are grouped by the three exam problem types. Each one shows the problem's diagram (redrawn in TikZ from the original) and the full problem. **Solutions are folded.** Try the problem on blank paper first, then click the "Solution" bar to open it.
>
> **Sources:** Fall 2021 Test 1 and Test 2 keys, Fall 2020 Test 1 key, the 2020 "remote" Test 2 key, the Fall 2015 and Fall 2014 Test 2 keys, and GPS 3, 4, 5 (no official key; solved here from scratch). A few problems marked *(original)* fill gaps. Nothing here uses magnetism or capacitors in circuits.
>
> **Notation:** $k=\dfrac{1}{4\pi\epsilon_0}$. Official keys often write $\dfrac{1}{4\pi\epsilon_0}$ or $\epsilon_0$; the two are interchangeable ($2k=\tfrac{1}{2\pi\epsilon_0}$, $4\pi k=\tfrac{1}{\epsilon_0}$).
>
> Theory is in [[Physics 2212 Test 2 Notes]] and the quick version is in [[Physics 2212 Test 2 Review]].

> [!tip] Instructor's advice
> "Can you complete the problem again with no notes or help? If so, can you change one small thing about the problem and complete it with no support?" Each problem ends with a **Variation** line to do exactly that.

## Contents
- [[#Part 1 — Distributed Charge & Conductors]]
  - [[#1.1 Charged rod and the "T"]] · [[#1.2 Quarter-circle arc]] · [[#1.3 Arc of any angle α]] · [[#1.4 Two oppositely charged rods]] · [[#1.5 Charged annulus]] · [[#1.6 Non-uniform rod]] · [[#1.7 Metal Mario]] · [[#1.8 Metal block between a ball and a dipole]]
- [[#Part 2 — Potential Difference & Potential Energy]]
  - [[#2.1 The charged shells]] · [[#2.2 The CRT]] · [[#2.3 Dipole potential difference and a released electron]] · [[#2.4 HF molecule]] · [[#2.5 Wire inside a metal tube]] · [[#2.6 Two charged shells]] · [[#2.7 Dipole on a circle]] · [[#2.8 Uniform field, diagonal path]]
- [[#Part 3 — Circuits (Batteries & Resistors)]]
  - [[#3.1 Single loop, opposing batteries]] · [[#3.2 Two batteries and three bulbs]] · [[#3.3 Four resistors, two batteries]] · [[#3.4 Three branches, two batteries]] · [[#3.5 Conveyor belt and wires of different thickness]] · [[#3.6 Quick conceptual checks]]
- [[#Answer Key]]

---

# Part 1 — Distributed Charge & Conductors

## 1.1 Charged rod and the "T"
*Fall 2021 Test 1, Problem 2*

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
\draw[->,cgry] (-3,0)--(3,0) node[right]{$x$};
\draw[->,cgry] (0,-2.8)--(0,5.2) node[above]{$y$};
\fill[cneg] (-0.12,0) rectangle (0.12,3.6);
\node[cneg,right] at (0.2,1.8) {$-Q$};
\filldraw[fill=cneg,fill opacity=0.3,draw=cneg,dashed] (-1.8,3.6) rectangle (1.8,3.85);
\node[cneg,right,font=\small] at (1.9,3.73) {$-Q$, length $L$ (part 3)};
\draw[dim] (-0.7,0)--(-0.7,3.6) node[midway,left]{$L$};
\draw[dim] (-0.7,0)--(-0.7,-2) node[midway,left]{$h$};
\node at (0,-2) {$\times$};
\node[right] at (0.1,-2) {$P=\langle0,-h,0\rangle$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> An insulating rod of length $L$ is uniformly charged with negative charge $-Q$. It lies on the $y$-axis with one end at the origin, running from $y=0$ to $y=L$.
> 1. Find the field $d\vec E$ at the observation location $\langle 0,-h,0\rangle$ due to an infinitesimal piece $dy$ of the rod.
> 2. Find the net electric field at the observation location.
> 3. A second, identical rod ($-Q$, length $L$) is placed horizontally on top of the first, forming a "T" (centered on the $y$-axis at $y=L$). Find the new net field at the observation location.

> [!success]- Solution
> **Part 1.** The charge density is $\lambda=\dfrac{-Q}{L}$, so a piece at $\langle0,y,0\rangle$ has $dQ=-\dfrac{Q}{L}dy$.
>
> Separation vector (observation − source):
> $$\vec r=\langle0,-h,0\rangle-\langle0,y,0\rangle=\langle0,-(h+y),0\rangle,\qquad |\vec r|=h+y,\qquad \hat r=-\hat y$$
> Field of the piece:
> $$d\vec E=\frac{k\,dQ}{|\vec r|^2}\hat r=\frac{k\left(-\frac QL dy\right)}{(h+y)^2}(-\hat y)=\boxed{\frac{kQ\,dy}{L(h+y)^2}\,\hat y}$$
> **Direction check:** the rod is negative, so the field points *toward* it. The rod is above P, so the field points up ($+\hat y$) ✓.
>
> **Part 2.** Integrate over the rod, $y=0\to L$ (a ✅ formula-sheet integral):
> $$\vec E=\frac{kQ}{L}\hat y\int_0^L\frac{dy}{(h+y)^2}=\frac{kQ}{L}\left[-\frac1{h+y}\right]_0^L\hat y=\frac{kQ}{L}\left(\frac1h-\frac1{h+L}\right)\hat y=\boxed{\frac{kQ}{h(h+L)}\,\hat y}$$
> **Check:** for $h\gg L$, this becomes $kQ/h^2$ (far-field) ✓.
>
> **Part 3.** Use superposition: $\vec E_{\text{net}}=\vec E_{\text{vertical rod}}+\vec E_{\text{top rod}}$.
>
> P is on the **perpendicular bisector** of the top rod, a distance $r=h+L$ from its center, so the sheet's rod formula applies: $|\vec E|=\dfrac{kQ}{r\sqrt{r^2+(L/2)^2}}$. The rod is negative, so this field also points toward the rod ($+\hat y$):
> $$\vec E_{\text{net}}=\left[\frac{kQ}{h(h+L)}+\frac{kQ}{(h+L)\sqrt{(h+L)^2+L^2/4}}\right]\hat y=\boxed{\frac{kQ}{h+L}\left(\frac1h+\frac{1}{\sqrt{(h+L)^2+\frac{L^2}{4}}}\right)\hat y}$$
>
> **Variation:** put P at $\langle d,0,0\rangle$ (beside the rod's bottom end). Now $\vec r=\langle d,-y,0\rangle$, and you need both $E_x$ and $E_y$.

---

## 1.2 Quarter-circle arc
*Fall 2020 Test 1, "Quarter"*

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
\draw[->,cgry] (-1,0)--(4.4,0) node[right]{$x$};
\draw[->,cgry] (0,-1)--(0,4.2) node[above]{$y$};
\draw[line width=4pt,cneg] (3.2,0) arc (0:90:3.2);
\node[cneg] at (45:3.75) {$-Q$};
\draw[cgry] (0,0)--(60:3.2) node[pos=0.6,left]{$R$};
\draw (0.8,0) arc (0:60:0.8);
\node at (30:1.1) {$\theta$};
\fill (0,0) circle (2.5pt);
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A thin glass arc of radius $R$ subtends $90°$ in the first quadrant, centered on the origin, and carries uniform charge $-Q$.
> - **A.** For a piece subtending $d\theta$ at angle $\theta$ from the $x$-axis, find $dQ$.
> - **B.** Find $d\vec E$ of that piece at the origin.
> - **C.** Integrate to find $\vec E$ at the origin (in terms of $R$, $Q$, and constants).
> - **D.** An identical arc with charge $+Q$ is placed in the third quadrant. How does the field at the origin change? (a) goes to zero (b) doubles, same direction (c) quadruples, same direction (d) doubles, opposite direction (e) quadruples, opposite direction (f) can't be determined

> [!success]- Solution
> **A.** The arc length is $\tfrac{\pi}{2}R$, so $\lambda=\dfrac{-Q}{\pi R/2}=-\dfrac{2Q}{\pi R}$. A piece has length $R\,d\theta$, so
> $$dQ=\lambda R\,d\theta=\boxed{-\frac{2Q}{\pi}\,d\theta}$$
>
> **B.** The source is at $\langle R\cos\theta,R\sin\theta,0\rangle$, so
> $$\vec r=\vec 0-\langle R\cos\theta,R\sin\theta,0\rangle,\qquad |\vec r|=R,\qquad \hat r=\langle-\cos\theta,-\sin\theta,0\rangle$$
> $$d\vec E=\frac{k\,dQ}{R^2}\hat r=\frac{k\left(-\frac{2Q}{\pi}d\theta\right)}{R^2}\langle-\cos\theta,-\sin\theta,0\rangle=\boxed{\frac{2kQ\,d\theta}{\pi R^2}\langle\cos\theta,\sin\theta,0\rangle}$$
> Each piece is negative, so its field points toward that piece, outward into the first quadrant ✓.
>
> **C.** Integrate $\theta=0\to\pi/2$:
> $$\vec E=\frac{2kQ}{\pi R^2}\left\langle\int_0^{\pi/2}\cos\theta\,d\theta,\ \int_0^{\pi/2}\sin\theta\,d\theta,\ 0\right\rangle=\frac{2kQ}{\pi R^2}\langle1-0,\ 0-(-1),\ 0\rangle=\boxed{\frac{2kQ}{\pi R^2}\langle1,1,0\rangle}$$
> The magnitude is $\dfrac{2\sqrt2\,kQ}{\pi R^2}$, pointing at $45°$ into the first quadrant.
>
> **D. (b) Doubles, same direction.** The $+Q$ arc in the third quadrant pushes the field *away* from itself, which is toward the first quadrant. That's the same direction as the $-Q$ arc's pull, with the same magnitude by symmetry.
>
> **Grader note:** the key takes off points for an extra factor of $R$. The most common error is $dQ=\lambda\,d\theta$ instead of $\lambda R\,d\theta$.
>
> **Variation:** put the arc in the second quadrant ($\theta=\pi/2\to\pi$) with $+Q$.

---

## 1.3 Arc of any angle α
*GPS 3, Problem 1*

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
\draw[->,cgry] (-0.5,0)--(4.4,0) node[right]{$x$};
\draw[->,cgry] (0,-0.5)--(0,4.2) node[above]{$y$};
\draw[line width=4pt,cneg] (3.4,0) arc (0:70:3.4);
\node[cneg] at (35:3.95) {$-Q$};
\draw[vec,cgry] (0,0)--(70:3.4) node[pos=0.55,left]{$R$};
\draw (0.9,0) arc (0:70:0.9);
\node at (35:1.2) {$\alpha$};
\fill (0,0) circle (2.5pt);
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A thin plastic rod is bent into a circular arc of radius $R$ centered on the origin, running from the $+x$ axis ($\theta=0$) to angle $\alpha$. It carries uniform charge $-Q$. Angles are in radians.
> - **A.** For a piece of angular length $d\theta$ at angle $\theta$, find the vector $\vec r$ from the piece to the observation point (the origin).
> - **B.** Find $dQ$.
> - **C.** Find $d\vec E$ at the origin and sketch its direction.
> - **D.** Integrate to find $\vec E$ at the origin.

> [!success]- Solution
> **A.**
> $$\vec r=\vec r_{\text{obs}}-\vec r_{\text{src}}=\langle0,0,0\rangle-\langle R\cos\theta,R\sin\theta,0\rangle=\boxed{\langle-R\cos\theta,\,-R\sin\theta,\,0\rangle}$$
>
> **B.** The arc length is $R\alpha$, so $\lambda=-\dfrac{Q}{R\alpha}$ and $dQ=\lambda R\,d\theta=\boxed{-\dfrac{Q}{\alpha}\,d\theta}$.
>
> **C.**
> $$d\vec E=\frac{k\,dQ}{|\vec r|^3}\vec r=\frac{k\left(-\frac Q\alpha d\theta\right)}{R^3}\langle-R\cos\theta,-R\sin\theta,0\rangle=\boxed{\frac{kQ}{\alpha R^2}\langle\cos\theta,\sin\theta,0\rangle\,d\theta}$$
> It points from the origin **toward** the piece, since the piece is negative.
>
> **D.**
> $$\vec E=\frac{kQ}{\alpha R^2}\left\langle\int_0^\alpha\cos\theta\,d\theta,\ \int_0^\alpha\sin\theta\,d\theta,\ 0\right\rangle=\boxed{\frac{kQ}{\alpha R^2}\langle\sin\alpha,\ 1-\cos\alpha,\ 0\rangle}$$
>
> **Checks:**
> - $\alpha=\pi/2$ gives $\frac{2kQ}{\pi R^2}\langle1,1,0\rangle$, which matches 1.2 ✓.
> - $\alpha=\pi$ gives $\frac{2kQ}{\pi R^2}\hat y$ (semicircle) ✓.
> - $\alpha=2\pi$ gives $\vec 0$ (full ring) ✓.
>
> **Variation:** let the arc run from $\theta=-\alpha/2$ to $+\alpha/2$ (symmetric about $+x$). Then $E_y=0$ by symmetry and $E_x=-\dfrac{2kQ}{\alpha R^2}\sin\dfrac\alpha2$.

---

## 1.4 Two oppositely charged rods
*GPS 3, Problem 2*

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
\draw[->,cgry] (-1.5,0)--(5,0) node[right]{$x$};
\draw[->,cgry] (0,-3)--(0,3.1) node[above]{$y$};
\draw[line width=5pt,cneg] (0,0)--(0,2.4);
\draw[line width=5pt,cpos] (0,0)--(0,-2.4);
\node[cneg,right] at (0.2,2.2) {$-Q$};
\node[cpos,right] at (0.2,-2.2) {$+Q$};
\fill[cgry] (-0.13,1.2) rectangle (0.13,1.45);
\node[right] at (0.2,1.33) {$dy$};
\draw[dim] (-0.6,0)--(-0.6,2.4) node[midway,left]{$L/2$};
\draw[dim] (-0.6,0)--(-0.6,-2.4) node[midway,left]{$L/2$};
\node at (3.8,0) {$\times$};
\node[above] at (3.8,0.1) {$\langle x,0,0\rangle$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> Two thin rods, each of length $L/2$, lie end to end on the $y$-axis, centered on the origin. The top rod ($0<y<L/2$) has charge $-Q$; the bottom rod ($-L/2<y<0$) has $+Q$. The observation point is $\langle x,0,0\rangle$.
> - **A.** Sketch three arrows at the observation point: $d\vec E_-$ from a small piece of the negative rod at $+y$, $d\vec E_+$ from the matching piece of the positive rod at $-y$, and their sum.
> - **B.** Write an expression for $d\vec E=d\vec E_-+d\vec E_+$.
> - **C.** Integrate, then simplify in the limit $x\gg L$. Hint: $(1+\epsilon)^N\approx1+N\epsilon+\frac{N(N-1)}{2}\epsilon^2$.

> [!success]- Solution
> **Densities:** each rod has $|\lambda|=\dfrac{Q}{L/2}=\dfrac{2Q}{L}$.
>
> **A.**
> - $d\vec E_-$ points **toward** the negative piece at $(0,y)$: up and to the left.
> - $d\vec E_+$ points **away from** the positive piece at $(0,-y)$: up and to the right.
> - The $x$-components cancel, so $d\vec E$ points straight **up** ($+\hat y$).
>
> **B.** Negative piece at $\langle0,y,0\rangle$, with $dQ_-=-\dfrac{2Q}{L}dy$ and $\vec r_-=\langle x,-y,0\rangle$:
> $$d\vec E_-=k\frac{-\frac{2Q}{L}dy}{(x^2+y^2)^{3/2}}\langle x,-y,0\rangle$$
> Positive piece at $\langle0,-y,0\rangle$, with $dQ_+=+\dfrac{2Q}{L}dy$ and $\vec r_+=\langle x,y,0\rangle$:
> $$d\vec E_+=k\frac{\frac{2Q}{L}dy}{(x^2+y^2)^{3/2}}\langle x,y,0\rangle$$
> Adding them, the $x$-parts cancel and the $y$-parts add:
> $$\boxed{d\vec E=\frac{4kQ}{L}\frac{y\,dy}{(x^2+y^2)^{3/2}}\,\hat y}$$
>
> **C.** Integrate $y=0\to L/2$ (a ✅ sheet integral):
> $$\vec E=\frac{4kQ}{L}\left[-\frac{1}{\sqrt{x^2+y^2}}\right]_0^{L/2}\hat y=\boxed{\frac{4kQ}{L}\left(\frac1x-\frac{1}{\sqrt{x^2+L^2/4}}\right)\hat y}$$
> **Far limit ($x\gg L$):**
> $$\frac{1}{\sqrt{x^2+L^2/4}}=\frac1x\left(1+\frac{L^2}{4x^2}\right)^{-1/2}\approx\frac1x\left(1-\frac{L^2}{8x^2}\right)$$
> so the bracket is $\approx\dfrac{L^2}{8x^3}$, giving
> $$\vec E\approx\boxed{\frac{kQL}{2x^3}\,\hat y}$$
> **Check:** this is a dipole. The charge centers sit at $\pm L/4$, so $p=Q\cdot\frac L2$, pointing from $-$ to $+$ ($-\hat y$). The perpendicular dipole field is $-k\vec p/x^3=+\dfrac{kQL}{2x^3}\hat y$ ✓.
>
> **Variation:** put the observation point on the $y$-axis at $\langle0,-D,0\rangle$ below both rods. (No symmetry help, but only $E_y$ survives.)

---

## 1.5 Charged annulus
*GPS 3, Problem 3*

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
\fill[cpos,fill opacity=0.2,even odd rule] (0,0) ellipse (3 and 1) (0,0) ellipse (1.5 and 0.5);
\draw (0,0) ellipse (3 and 1) (0,0) ellipse (1.5 and 0.5);
\draw[cpos,line width=2pt] (0,0) ellipse (2.2 and 0.733);
\draw[->,cgry] (0,0)--(0,4) node[above]{$z$};
\fill (0,3.2) circle (2.5pt) node[right]{$A=\langle0,0,z\rangle$};
\draw[dim] (0,0)--(-3,0) node[pos=0.8,above]{$R$};
\draw[dim] (0,0)--(1.5,0) node[pos=0.6,above]{$\frac{R}{2}$};
\draw[cpos,thick] (1.9,-0.4)--(3.1,-1.2) node[right]{ring: radius $r$, width $dr$};
\node at (-2.6,1.25) {$+Q$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A thin plastic annulus (outer radius $R$, inner radius $R/2$) is centered on the origin in the $xy$-plane and carries uniform charge $+Q$. The observation point is $A=\langle0,0,z\rangle$.
> - **A.** For a thin ring of radius $r$ and width $dr$, find $dQ$.
> - **B.** Write $d\vec E$ of that ring at $A$.
> - **C.** Integrate to find $\vec E$ at $A$ (in terms of $R$, $Q$, $z$, constants).
> - **D.** Find $\vec E$ in the limit $0<z\ll R$.

> [!success]- Solution
> **A.** The area is $\pi R^2-\pi\left(\frac R2\right)^2=\frac34\pi R^2$, so $\sigma=\dfrac{4Q}{3\pi R^2}$. A ring has area $2\pi r\,dr$:
> $$dQ=\sigma\,2\pi r\,dr=\boxed{\frac{8Q}{3R^2}\,r\,dr}$$
>
> **B.** Use the ✅ ring formula with $q\to dQ$ and $R\to r$:
> $$d\vec E=\frac{k\,dQ\,z}{(z^2+r^2)^{3/2}}\hat z=\boxed{\frac{8kQz}{3R^2}\frac{r\,dr}{(z^2+r^2)^{3/2}}\,\hat z}$$
>
> **C.** Integrate $r=R/2\to R$ (substitute $u=z^2+r^2$):
> $$\vec E=\frac{8kQz}{3R^2}\left[-\frac{1}{\sqrt{z^2+r^2}}\right]_{R/2}^{R}\hat z=\boxed{\frac{8kQz}{3R^2}\left(\frac{1}{\sqrt{z^2+R^2/4}}-\frac{1}{\sqrt{z^2+R^2}}\right)\hat z}$$
> **Cross-check by superposition:** a full disk of radius $R$ minus a disk of radius $R/2$ (same $\sigma$), each using the ✅ disk formula, gives the same answer.
>
> **D.** For $z\ll R$, the bracket is $\approx\dfrac{1}{R/2}-\dfrac1R=\dfrac1R$, so
> $$\vec E\approx\boxed{\frac{8kQz}{3R^3}\,\hat z}$$
> The field is zero at the center and grows linearly with $z$. There's no charge at the hole, so there's no "sheet" jump at $z=0$, unlike a full disk.
>
> **Far check:** for $z\gg R$, expanding both terms gives $kQ/z^2$ ✓.

---

## 1.6 Non-uniform rod
*(original; the "weird density" type of problem)*

> [!question] Problem
> A rod lies on the $x$-axis from $x=0$ to $x=L$ with linear charge density $\lambda(x)=\alpha x$ ($\alpha>0$ is a constant).
> - **A.** Find the total charge $Q$ in terms of $\alpha$ and $L$.
> - **B.** Find $d\vec E$ at P $=\langle-d,0,0\rangle$ (a distance $d$ to the left of the origin).
> - **C.** Integrate to find $\vec E$ at P.
> - **D.** Show that it reduces to a point charge when $d\gg L$.

> [!success]- Solution
> **A.** $dQ=\lambda\,dx=\alpha x\,dx$, so $Q=\displaystyle\int_0^L\alpha x\,dx=\boxed{\tfrac12\alpha L^2}$. ✅ (This is a polynomial integral from the sheet.)
>
> **B.** The piece is at $\langle x,0,0\rangle$:
> $$\vec r=\langle-d,0,0\rangle-\langle x,0,0\rangle=\langle-(d+x),0,0\rangle,\qquad |\vec r|=d+x$$
> $$d\vec E=\frac{k\,\alpha x\,dx}{(d+x)^3}\langle-(d+x),0,0\rangle=\boxed{-\frac{k\alpha\,x\,dx}{(d+x)^2}\,\hat x}$$
>
> **C.** Split the integrand so it uses only sheet integrals: $\dfrac{x}{(d+x)^2}=\dfrac{1}{d+x}-\dfrac{d}{(d+x)^2}$. Then
> $$\int_0^L\frac{x\,dx}{(d+x)^2}=\Big[\ln(d+x)\Big]_0^L+d\left[\frac{1}{d+x}\right]_0^L=\ln\frac{d+L}{d}-\frac{L}{d+L}$$
> $$\boxed{\vec E=-k\alpha\left[\ln\!\left(1+\frac Ld\right)-\frac{L}{L+d}\right]\hat x}$$
>
> **D.** Let $\epsilon=L/d\ll1$. Then $\ln(1+\epsilon)\approx\epsilon-\tfrac12\epsilon^2$ and $\dfrac{\epsilon}{1+\epsilon}\approx\epsilon-\epsilon^2$, so the bracket is $\approx\tfrac12\epsilon^2=\dfrac{L^2}{2d^2}$. That gives
> $$\vec E\approx-\frac{k\alpha L^2}{2d^2}\hat x=-\frac{kQ}{d^2}\hat x\ \checkmark$$
> (pointing away from the positive rod, toward $-x$).

---

## 1.7 Metal Mario
*Fall 2020 Test 1 (on the instructor's recommended list)*

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
\draw[->,cgry] (-6,0)--(4,0) node[right]{$x$};
\draw[->,cgry] (0,-1.6)--(0,2) node[above]{$y$};
\draw[dim] (-4.8,1.1)--(0,1.1) node[midway,above]{$2d$};
\draw[dim] (0,1.1)--(2.4,1.1) node[midway,above]{$d$};
\node[pc,label=below:{$+Q$}] at (-4.8,0) {$+$};
\node[pc,label=below:{$+Q$}] at (2.4,0) {$+$};
\filldraw[fill=cgry!60,draw=black,rounded corners=2pt] (-0.3,-0.45) rectangle (0.3,0.45);
\node[below] at (0,-0.5) {\small Mario (metal)};
\begin{scope}[xshift=7cm]
\foreach \i/\a in {1/90,2/45,3/0,4/-45,5/-90,6/-135,7/180,8/135} {\draw[->,thick,corg] (0,0)--(\a:1); \node[font=\small] at (\a:1.3) {\i};}
\node[font=\small,align=left] at (0,-2.1) {9 = zero\\10 = need more info};
\end{scope}
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A neutral metal Mario sits at the origin. Two insulating balls, each $+Q$, are at $\vec r_1=\langle d,0,0\rangle$ and $\vec r_2=\langle-2d,0,0\rangle$, with $d$ much larger than Mario. Mario is in equilibrium.
> - **A.** Which direction does Mario's dipole moment point? (Use the 8-direction compass: 1 = up, 3 = right, 5 = down, 7 = left, etc.)
> - **B.** Which direction does the net force on Mario point?
> - **C.** Find the electric field at the origin due to Mario's polarization.
> - **D.** Mario melts into a metal cube at the origin. Sketch its charge distribution.
> - **E.** Repeat D if the cube were plastic.

> [!success]- Solution
> **External field at the origin.** Use $\vec r=$ obs − source for each ball:
> - Ball at $\langle d,0,0\rangle$: $\vec r=\langle-d,0,0\rangle$, so $\vec E_1=\dfrac{kQ}{d^2}(-\hat x)$.
> - Ball at $\langle-2d,0,0\rangle$: $\vec r=\langle2d,0,0\rangle$, so $\vec E_2=\dfrac{kQ}{4d^2}(+\hat x)$.
>
> Together:
> $$\vec E_{\text{ext}}=-\frac{3kQ}{4d^2}\hat x$$
>
> **A. Direction 7 ($-\hat x$).** An induced dipole lines up with the applied field, $\vec p=\alpha\vec E_{\text{ext}}$.
>
> **B. Direction 3 ($+\hat x$).** An induced dipole is always attracted toward the **stronger** field, i.e. toward the nearer charge. Mario's $-$ end faces the closer ball at $+d$, and that attraction beats the repulsion of the $+$ end.
>
> **C.** Mario is a conductor, so $\vec E_{\text{net}}=0$ inside, which means $\vec E_{\text{Mario}}=-\vec E_{\text{ext}}$:
> $$\boxed{\vec E_{\text{Mario}}=\frac{3kQ}{4d^2}\hat x=\frac{3Q}{16\pi\epsilon_0d^2}\hat x}$$
>
> **D. Metal cube:** excess charge sits **on the surface**. Electrons move opposite $\vec E_{\text{ext}}$ (toward $+x$), so the **right face is $-$** and the **left face is $+$**. The interior is neutral.
>
> **E. Plastic cube:** charges can't travel. Every molecule becomes a small dipole with its $+$ end on the left and $-$ end on the right, slightly stronger near the right side (closer to the nearer ball). There is no net surface charge pile-up like in metal.

---

## 1.8 Metal block between a ball and a dipole
*Fall 2021 Test 1, Problem 3*

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
\filldraw[fill=cneg,fill opacity=0.3,draw=cneg] (0,0) circle (0.55);
\node at (0,0) {$-Q$};
\node[above] at (0,0.6) {\small glass ball};
\filldraw[fill=cgry,fill opacity=0.3,draw=black] (3,-0.5) rectangle (6,0.5);
\fill (4.5,0) circle (2pt);
\node[above] at (4.5,0.55) {\small neutral metal block};
\node[nc] at (9,0.45) {$-$};
\node[pc] at (9,-0.45) {$+$};
\node[right,font=\small] at (9.3,0) {dipole, $|\vec p|=Qs$};
\draw[dim] (0,-1.2)--(4.5,-1.2) node[midway,below]{$d/2$};
\draw[dim] (4.5,-1.2)--(9,-1.2) node[midway,below]{$d/2$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A small glass ball has uniform charge $-Q$. A distance $d$ to its right is a permanent dipole with moment $|\vec p|=Qs$, oriented vertically with its $-$ end on top ($d\gg s$). A **neutral metal block** is placed so its center is at the midpoint ($d/2$ from each).
> 1. Sketch the block's charge distribution.
> 2. At the block's center, draw $\vec E_{\text{dipole}}$, $\vec E_{\text{ball}}$, $\vec E_{\text{metal}}$, and $\vec E_{\text{net}}$.
> 3. Find $|\vec E_{\text{metal}}|$ at the block's center.

> [!success]- Solution
> **Fields at the center** (take the ball on the left, $+x$ to the right, $+y$ up):
> - **Ball** ($-Q$, distance $d/2$): the field points toward the ball, $\vec E_{\text{ball}}=-\dfrac{kQ}{(d/2)^2}\hat x=-\dfrac{4kQ}{d^2}\hat x$.
> - **Dipole:** $\vec p$ points from $-$ to $+$, i.e. down ($-\hat y$). The center lies on the dipole's perpendicular bisector, so the ✅ sheet formula gives $\vec E_\perp=-\dfrac{k\vec p}{r^3}=+\dfrac{kQs}{(d/2)^3}\hat y=\dfrac{8kQs}{d^3}\hat y$.
>
> **1. Charge distribution:** electrons move opposite $\vec E_{\text{ext}}$, which is mostly $-x$ with a slight $+y$. So the **right face is $-$** and the **left face is $+$**, with a slight $+$ on top and $-$ on the bottom. All of it is on the surface.
>
> **2.** $\vec E_{\text{ball}}$ is a long arrow pointing left. $\vec E_{\text{dipole}}$ is a short arrow pointing up (since $s\ll d$). $\vec E_{\text{metal}}$ points right and slightly down, exactly canceling the two. $\vec E_{\text{net}}=0$ (say "zero" explicitly).
>
> **3.** The block is a conductor, so $\vec E_{\text{net}}=0$:
> $$\vec E_{\text{metal}}=-(\vec E_{\text{ball}}+\vec E_{\text{dip}})=\left\langle\frac{4kQ}{d^2},\ -\frac{8kQs}{d^3},\ 0\right\rangle$$
> $$|\vec E_{\text{metal}}|=\boxed{\frac{4kQ}{d^2}\sqrt{1+\frac{4s^2}{d^2}}}$$

---

# Part 2 — Potential Difference & Potential Energy

## 2.1 The charged shells
*2020 Test 2 (on the recommended list)*

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
\draw[cneg,line width=2.5pt] (0,0) circle (2.6);
\filldraw[fill=cgry,fill opacity=0.4,draw=black] (0,0) circle (1.1);
\node at (0,0.45) {$+2Q$};
\draw[vec,thick] (0,0)--(200:1.1);
\node[above] at (200:0.6) {$R_a$};
\draw[vec,thick,cneg] (0,0)--(-20:2.6) node[pos=0.75,above]{$R_b$};
\node[cneg] at (0,3) {$-Q$ (plastic shell)};
\node at (0,-1.5) {\small metal sphere};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A solid **metal** sphere of radius $R_a$ carries $+2Q$ ($Q>0$). It sits at the center of a thin **plastic** shell of radius $R_b>R_a$ carrying $-Q$ spread uniformly.
> - **A.** Find $V_{R_a}-V_{R_b}$ (outer surface of the sphere minus inner surface of the shell).
> - **B.** Find $V_0-V_\infty$ (center of the sphere minus infinity).
> - **C.** The whole object is placed between two large oppositely charged plates. How does $V_0-V_{R_a}$ change? (no change / increases / decreases / can't tell)

> [!success]- Solution
> **Field in each region** (only charge *inside* radius $r$ contributes, since a shell gives zero inside itself):
> | Region | $\vec E$ |
> |---|---|
> | $r<R_a$ (inside the metal) | $0$ (conductor) |
> | $R_a<r<R_b$ | $\dfrac{2kQ}{r^2}\hat r$ |
> | $r>R_b$ | $\dfrac{k(2Q-Q)}{r^2}\hat r=\dfrac{kQ}{r^2}\hat r$ |
>
> **A.** Go radially from $R_b$ to $R_a$ with $d\vec l=dr\,\hat r$:
> $$V_{R_a}-V_{R_b}=-\int_{R_b}^{R_a}\frac{2kQ}{r^2}dr=2kQ\left[\frac1r\right]_{R_b}^{R_a}=\boxed{2kQ\left(\frac1{R_a}-\frac1{R_b}\right)}$$
> **Sign check:** you moved inward, against $\vec E$ (which points outward), so $\Delta V>0$ ✓.
>
> **B.** Add up the regions:
> $$V_0-V_\infty=\underbrace{(V_0-V_{R_a})}_{0\text{ (metal)}}+\underbrace{(V_{R_a}-V_{R_b})}_{\text{part A}}+\underbrace{(V_{R_b}-V_\infty)}_{kQ/R_b}$$
> $$=\boxed{kQ\left(\frac{2}{R_a}-\frac1{R_b}\right)}$$
> **Superposition check:** at the center, the sphere contributes $\dfrac{k(2Q)}{R_a}$ and the shell (constant inside) contributes $-\dfrac{kQ}{R_b}$ ✓.
>
> **C. No change.** $\vec E=0$ inside the metal no matter what external field is applied, so $V_0-V_{R_a}=0$ always.

---

## 2.2 The CRT
*2020 Test 2 / GPS 4, Problem 1 (on the recommended list)*

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
\fill[cgry] (-0.08,-2.6) rectangle (0.08,-0.15);
\fill[cgry] (-0.08,0.15) rectangle (0.08,2.6);
\fill[cgry] (0.72,-2.6) rectangle (0.88,2.6);
\node at (0,2.95) {$-Q$};
\node at (0.8,2.95) {$+Q$};
\draw[dim] (0,2.3)--(0.8,2.3);
\node at (0.4,2.55) {\small$s$};
\draw[line width=3pt,cgry] (1.300,-0.150)--(5.995,0.848) node[right]{$-3Q$};
\draw[line width=3pt,cgry] (1.154,0.535)--(5.850,1.533) node[right]{$+3Q$};
\draw[dim] (1.394,-0.590)--(6.089,0.408) node[midway,below]{$2R$};
\draw[dotted,thick,cpos] (1.154,1.735) arc (90:12:1.2);
\node at (1.704,1.285) {$\theta$};
\node[nc] (e) at (-1.6,0) {$-$};
\draw[dashed,thick,cneg,-{Stealth}] (e)--(0.85,0) .. controls (2.8,0.3) and (4.6,0.85) .. (5.450,1.333);
\node[below,font=\small] at (-1.6,-0.35) {$\vec v_i=\langle v_0,0,0\rangle$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> An electron (mass $m_e$, charge $-e$) moves with $\vec v_i=\langle v_0,0,0\rangle$ through two parallel-plate capacitors (circular plates of radius $R$, separation $s\ll R$). The first has plates $-Q$ (left) and $+Q$ (right). The second is tilted by $\theta$ and has plates $\pm3Q$.
> - **A.** The electron enters the first capacitor through a small hole, moving perpendicular to the plates. Find its change in electric potential energy across the gap.
> - **B.** It then enters the second capacitor just missing the negative plate and exits after crossing the full separation $s$, just missing the positive plate. Find its exit speed. (The field outside the capacitors is negligible.)

> [!success]- Solution
> **Fields (✅ sheet capacitor formula):** inside each capacitor $|\vec E|=\dfrac{Q/A}{\epsilon_0}$ with $A=\pi R^2$:
> $$E_1=\frac{Q}{\pi R^2\epsilon_0},\qquad E_2=\frac{3Q}{\pi R^2\epsilon_0}$$
> Each field is uniform and points from the $+$ plate to the $-$ plate.
>
> **A.** The electron goes from the $-$ plate to the $+$ plate, i.e. **against** $\vec E_1$. In a uniform field $\Delta V=-\vec E\cdot\Delta\vec r=+E_1s$:
> $$\Delta V_1=\frac{Qs}{\pi R^2\epsilon_0},\qquad \Delta U_1=q\Delta V_1=\boxed{-\frac{eQs}{\pi R^2\epsilon_0}}$$
> **Sign check:** the electron is attracted to the $+$ plate, so it speeds up. $\Delta K>0$ means $\Delta U<0$ ✓.
>
> **B.** Split the electron's displacement into a part along the plates (perpendicular to $\vec E_2$, contributing $\Delta V=0$) and a part across the gap (length $s$, from the $-$ side to the $+$ side, against $\vec E_2$):
> $$\Delta V_2=+E_2s=\frac{3Qs}{\pi R^2\epsilon_0},\qquad \Delta U_2=-\frac{3eQs}{\pi R^2\epsilon_0}$$
> **Energy conservation** (system: electron + capacitors): $\Delta K=-(\Delta U_1+\Delta U_2)=\dfrac{4eQs}{\pi R^2\epsilon_0}$. Then
> $$\tfrac12m_ev_f^2=\tfrac12m_ev_0^2+\frac{4eQs}{\pi R^2\epsilon_0}\quad\Longrightarrow\quad\boxed{v_f=\sqrt{v_0^2+\frac{8eQs}{\pi R^2\epsilon_0m_e}}}$$
> The angle $\theta$ and the length of the path inside the plates **don't matter**. Only the displacement along $\vec E$ counts.

---

## 2.3 Dipole potential difference and a released electron
*Fall 2021 Test 2, Problem 2 (on the recommended list)*

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
\draw[->,cgry] (-1.2,0)--(7.2,0) node[right]{$x$};
\draw[->,cgry] (0,-1)--(0,4) node[above]{$y$};
\node[pc,minimum size=4.5mm] at (-0.28,0) {\small$+$};
\node[nc,minimum size=4.5mm] at (0.28,0) {\small$-$};
\node at (3,0) {$\times$}; \node[above] at (3,0.1) {A};
\node at (6,0) {$\times$}; \node[above] at (6,0.1) {B};
\node at (0,3) {$\times$}; \node[right] at (0.1,3) {C};
\draw[dim] (0,-0.6)--(3,-0.6) node[midway,below]{$d$};
\draw[dim] (3,-0.6)--(6,-0.6) node[midway,below]{$d$};
\draw[dim] (-0.6,0)--(-0.6,3) node[midway,left]{$d$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A dipole of charges $\pm q$ separated by $s$ lies along the $x$-axis at the origin, with $+q$ on the **left** and $-q$ on the right. Points: $A=\langle d,0,0\rangle$, $B=\langle2d,0,0\rangle$, $C=\langle0,d,0\rangle$, with $d\gg s$.
> 1. Find $V_B-V_A$. Make sure the sign is right.
> 2. An electron is released from rest at $B$. Find its kinetic energy very far away ($r=\infty$).
> 3. Find $V_C-V_B$.

> [!success]- Solution
> **Dipole moment:** $\vec p$ points from $-$ to $+$, so $\vec p=qs(-\hat x)$. On the axis (✅ sheet):
> $$\vec E_\parallel=\frac{2k\vec p}{x^3}=-\frac{2kqs}{x^3}\hat x$$
> The field points toward the dipole along this axis, because you're on the $-$ side.
>
> **1.** Path along $x$ from $d$ to $2d$, $d\vec l=dx\,\hat x$:
> $$V_B-V_A=-\int_d^{2d}\left(-\frac{2kqs}{x^3}\right)dx=2kqs\left[-\frac{1}{2x^2}\right]_d^{2d}=kqs\left(\frac1{d^2}-\frac1{4d^2}\right)=\boxed{\frac{3kqs}{4d^2}}$$
> **Sign check:** you move $+x$, against $\vec E$ (which points $-x$), so $\Delta V>0$ ✓ ("uphill").
>
> **2.** First,
> $$V_\infty-V_B=-\int_{2d}^{\infty}\left(-\frac{2kqs}{x^3}\right)dx=2kqs\cdot\frac{1}{2(2d)^2}=\frac{kqs}{4d^2}$$
> Energy conservation, with $K_i=0$ and charge $-e$:
> $$\Delta K=-q\Delta V=-(-e)\frac{kqs}{4d^2}\quad\Longrightarrow\quad\boxed{K_f=\frac{ekqs}{4d^2}}$$
> **Sanity:** near the $-$ end $V$ is negative, and an electron is pushed toward higher $V$, so it speeds up going out to $\infty$ ✓.
>
> **3.** Path independence: go from $B$ out to $\infty$, then in along the $y$-axis to $C$:
> $$V_C-V_B=(V_C-V_\infty)+(V_\infty-V_B)$$
> On the perpendicular bisector, $\vec E_\perp$ is parallel to $\hat x$ while $d\vec l=dy\,\hat y$, so $\vec E\cdot d\vec l=0$ and $V_C-V_\infty=0$. Therefore
> $$V_C-V_B=\boxed{\frac{kqs}{4d^2}}$$

---

## 2.4 HF molecule
*Fall 2015 Test 2, Problem 2 (on the recommended list)*

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
\draw[cgry] (-1.2,0)--(7.4,0);
\draw[dashed,cgry] (0,-0.5)--(0,4.5);
\node[nc,minimum size=4.5mm,label=below:{\small F$^-$}] at (-0.28,0) {\small$-$};
\node[pc,minimum size=4.5mm,label=below:{\small H$^+$}] at (0.28,0) {\small$+$};
\node at (3.5,0) {$\times$}; \node[above] at (3.5,0.1) {1};
\node at (6.6,0) {$\times$}; \node[above] at (6.6,0.1) {2};
\node at (0,2) {$\times$}; \node[right] at (0.1,2) {4};
\node at (0,4) {$\times$}; \node[right] at (0.1,4) {3};
\draw[dim] (0,-1.1)--(3.5,-1.1) node[midway,below]{$d_1$};
\draw[dim] (0,-1.9)--(6.6,-1.9) node[midway,below]{$d_2$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> An HF molecule is modeled as $F^-$ ($-e$, left) and $H^+$ ($+e$, right) separated by $s$. Points 1 and 2 are on the molecular axis at distances $d_1<d_2$ (both $\gg s$). Points 3 and 4 lie on the line through the molecule's midpoint perpendicular to the axis.
> - **(a)** Find $V_2-V_1$, with the correct sign.
> - **(b)** A proton is released from rest at location 2. Find its speed very far away.
> - **(c)** Find $V_3-V_4$.
> - **(extra credit)** Find $V_4-V_1$.

> [!success]- Solution
> $\vec p=es\,\hat x$ (from $F^-$ to $H^+$). On the axis, $\vec E=\dfrac{2kes}{x^3}\hat x$, pointing **away** from the dipole on the $+$ side.
>
> **(a)**
> $$V_2-V_1=-\int_{d_1}^{d_2}\frac{2kes}{x^3}dx=kes\left[\frac{1}{x^2}\right]_{d_1}^{d_2}=\boxed{kes\left(\frac1{d_2^2}-\frac1{d_1^2}\right)}<0$$
> You moved along $\vec E$, so the potential went **down** ✓.
>
> **(b)** First, $V_\infty-V_2=kes\left(0-\dfrac{1}{d_2^2}\right)=-\dfrac{kes}{d_2^2}$. Then $\tfrac12m_pv^2=-e(V_\infty-V_2)=\dfrac{ke^2s}{d_2^2}$, so
> $$\boxed{v=\frac{e}{d_2}\sqrt{\frac{2ks}{m_p}}}$$
>
> **(c)** Along the perpendicular line, $\vec E\perp d\vec l$, so $\boxed{V_3-V_4=0}$.
>
> **(EC)** Go from 1 out to $\infty$ along the axis, around at infinity, then in to 4 along the perpendicular (which adds 0):
> $$V_4-V_1=(V_4-V_\infty)+(V_\infty-V_1)=0+kes\left(0-\frac1{d_1^2}\right)=\boxed{-\frac{kes}{d_1^2}}$$

---

## 2.5 Wire inside a metal tube
*Fall 2014 Test 2, Problem 2 (on the recommended list)*

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
\draw[cneg,line width=3pt] (0,0) circle (2.4);
\filldraw[fill=cpos,fill opacity=0.5,draw=cpos] (0,0) circle (0.28);
\draw[vec,thick,cneg] (0,0)--(45:2.4) node[pos=0.65,above left]{$R$};
\draw[vec,thick,cpos] (0,0)--(-80:0.28);
\node[cpos] at (-0.15,-0.6) {$r$};
\node[cneg,right] at (2.6,1.4) {tube: $-Q$};
\node[cpos,right] at (2.6,0.4) {wire: $+Q$};
\node[right,font=\small] at (2.6,-0.8) {both length $L$ (into page)};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A long thin metal wire (radius $r$, length $L$) sits on the axis of a concentric long metal tube (radius $R$). A power supply keeps $+Q$ on the wire and $-Q$ on the tube. Like a spherical shell, the tube produces zero field everywhere inside itself. Find $V_{\text{tube}}-V_{\text{wire}}$, and check the sign.

> [!success]- Solution
> **Field between them:** only the wire contributes (the tube gives 0 inside). The wire is long ($\rho\ll L$), so the ✅ sheet formula gives
> $$\vec E=\frac{1}{4\pi\epsilon_0}\frac{2Q/L}{\rho}\hat\rho=\frac{2kQ}{L\rho}\hat\rho$$
> (radially outward).
>
> **Integrate outward** from the wire surface ($\rho=r$) to the tube ($\rho=R$), with $d\vec l=d\rho\,\hat\rho$:
> $$V_{\text{tube}}-V_{\text{wire}}=-\int_r^R\frac{2kQ}{L\rho}d\rho=-\frac{2kQ}{L}\ln\frac Rr=\boxed{\frac{2kQ}{L}\ln\frac rR=\frac{Q}{2\pi\epsilon_0L}\ln\frac rR}$$
> **Sign check:** $r<R$, so $\ln(r/R)<0$. You moved along $\vec E$, so $\Delta V<0$ ✓.
>
> **Variation:** a point at radius $\rho_0$ between them. $V(\rho_0)-V_{\text{wire}}=-\dfrac{2kQ}{L}\ln\dfrac{\rho_0}{r}$.

---

## 2.6 Two charged shells
*GPS 4, Problem 2*

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
\draw[->,cgry] (-4.3,0)--(4.4,0) node[right]{$x$};
\draw[->,cgry] (0,-3.2)--(0,1.8) node[above]{$y$};
\draw[cneg,line width=2.5pt] (-2.6,0) circle (1);
\draw[cpos,line width=2.5pt] (2.6,0) circle (1);
\node[cneg] at (-2.6,-1.4) {$-Q$};
\node[cpos] at (2.6,-1.4) {$+Q$};
\draw[dim] (-2.6,1.4)--(0,1.4) node[midway,above]{$L/2$};
\draw[dim] (0,1.4)--(2.6,1.4) node[midway,above]{$L/2$};
\draw[dim] (-0.5,0)--(-0.5,-2.6) node[midway,left]{$L/2$};
\node at (0,0) {$\times$}; \node[above right] at (0,0) {2};
\node at (2.6,0) {$\times$}; \node[above right] at (2.6,0) {3};
\node at (0,-2.6) {$\times$}; \node[right] at (0.1,-2.6) {1};
\node[cgry,font=\small] at (3.95,0.85) {radius $R$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> Two plastic spherical shells of radius $R$ have centers at $\langle-L/2,0,0\rangle$ (charge $-Q$) and $\langle+L/2,0,0\rangle$ (charge $+Q$), with $R<L/2$. Points: $1=\langle0,-L/2,0\rangle$, $2=\langle0,0,0\rangle$, $3=\langle L/2,0,0\rangle$ (the center of the $+$ shell).
> - **A.** Find $V_2-V_1$ due to the **positive** shell only.
> - **B.** Find $V_2-V_1$ due to the **negative** shell only.
> - **C.** Find $V_3-V_2$ due to the **net** field (use superposition).
> - **D.** Adding A + B + C gives $V_3-V_1$. How would it change if point 1 were at $\langle0,0,L/2\rangle$ instead?

> [!success]- Solution
> **Tool:** outside a shell, it acts like a point charge, so the ✅ sheet formula $\Delta V=kq\left(\frac1{r_f}-\frac1{r_i}\right)$ applies. Inside a shell, $V$ is constant.
>
> **Distances to each center:** point 1 is $\sqrt{(L/2)^2+(L/2)^2}=L/\sqrt2$ away; point 2 is $L/2$ away; point 3 is $L$ from the $-$ center and at the center of the $+$ shell.
>
> **A.** $r_i=L/\sqrt2$, $r_f=L/2$:
> $$V_2-V_1=kQ\left(\frac2L-\frac{\sqrt2}{L}\right)=\boxed{\frac{kQ}{L}(2-\sqrt2)}$$
>
> **B.** Same distances, charge $-Q$: $\boxed{-\dfrac{kQ}{L}(2-\sqrt2)}$.
>
> **C.**
> - $+$ shell: from 2 (outside, $r=L/2$) to its surface, then inside where nothing changes. That gives $kQ\left(\frac1R-\frac2L\right)$.
> - $-$ shell: from $r=L/2$ to $r=L$ gives $-kQ\left(\frac1L-\frac2L\right)=+\frac{kQ}{L}$.
> $$V_3-V_2=\boxed{kQ\left(\frac1R-\frac1L\right)}$$
>
> **D. No change.** The new point 1 is also $L/\sqrt2$ from both centers, so A and B are unchanged (and still cancel). In fact, every point on the midplane $x=0$ has $V=0$.

---

## 2.7 Dipole on a circle
*GPS 4, Problem 3*

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
\draw[->,cgry] (-1.2,0)--(5,0) node[right]{$x$};
\draw[->,cgry] (0,-1)--(0,4.8) node[above]{$y$};
\draw[dashed,thick,cgry] (0,4) arc (90:0:4);
\draw[->,cgry] (0,0)--(60:4) node[pos=0.6,right]{$R$};
\draw (0,1.2) arc (90:60:1.2);
\node at (75:1.5) {$\theta$};
\node[nc,minimum size=4.5mm] at (-0.28,0) {\small$-$};
\node[pc,minimum size=4.5mm] at (0.28,0) {\small$+$};
\node at (0,4) {$\times$}; \node[left] at (-0.15,4) {A};
\node at (4,0) {$\times$}; \node[below] at (4,-0.15) {B};
\node[right] at (60:4.05) {$P_\theta$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A dipole $\vec p=p\hat x$ sits at the origin. $A$ is on the $y$-axis and $B$ is on the $x$-axis, each a distance $R$ from the center (far from the dipole).
> - **A.** Find $V_A-V_\infty$.
> - **B.** Find $V_B-V_\infty$.
> - **C.** Point $P_\theta$ is on the circle of radius $R$ at angle $\theta$ from the $+y$ axis. Find $V_A-V_{P_\theta}$ by treating each charge of the dipole separately and using the binomial expansion.
> - **D.** An electron starts at $B$ with speed $v$ and (somehow) follows the circular path to $A$. Sketch its speed along the way.

> [!success]- Solution
> **A.** Come in from $\infty$ along the $y$-axis. $\vec E_\perp$ is parallel to $\hat x$ and $d\vec l$ is parallel to $\hat y$, so $\vec E\cdot d\vec l=0$ and $\boxed{V_A-V_\infty=0}$.
>
> **B.** On the axis, $\vec E=\dfrac{2kp}{x^3}\hat x$:
> $$V_B-V_\infty=-\int_\infty^R\frac{2kp}{x^3}dx=\boxed{\frac{kp}{R^2}}$$
>
> **C.** Put $+q$ at $\langle\frac s2,0,0\rangle$ and $-q$ at $\langle-\frac s2,0,0\rangle$, with $p=qs$. The point is $P_\theta=\langle R\sin\theta,R\cos\theta,0\rangle$. Its distances to the two charges are
> $$r_\pm^2=R^2\mp Rs\sin\theta+\tfrac{s^2}{4}\approx R^2\left(1\mp\frac sR\sin\theta\right)$$
> Using $(1\mp\epsilon)^{-1/2}\approx1\pm\frac\epsilon2$:
> $$\frac1{r_\pm}\approx\frac1R\left(1\pm\frac{s}{2R}\sin\theta\right)$$
> Each charge's potential relative to $\infty$ is $kq/r$, so
> $$V_{P_\theta}=\frac{kq}{r_+}-\frac{kq}{r_-}\approx\frac{kq}{R}\cdot\frac sR\sin\theta=\frac{kp\sin\theta}{R^2}$$
> $$V_A-V_{P_\theta}=\boxed{-\frac{kp\sin\theta}{R^2}}$$
> **Check:** $\theta=90°$ (point B) gives $-kp/R^2$, consistent with A and B ✓.
>
> **D.** Measured from B, the electron's potential energy rises along the path: $\Delta U=-e\left[V(\theta)-V_B\right]=\dfrac{ekp}{R^2}(1-\sin\theta)$. Energy conservation then gives
> $$v(\theta)=\sqrt{v^2-\frac{2ekp}{m_eR^2}(1-\sin\theta)}$$
> The speed **decreases smoothly** from $v$ at $B$ to its minimum $\sqrt{v^2-2ekp/(m_eR^2)}$ at $A$. (The electron is moving from high $V$ to low $V$, which slows a negative charge.)

---

## 2.8 Uniform field, diagonal path
*Fall 2015 Test 2, Problem 4b (made symbolic)*

> [!question] Problem
> In a region of uniform field $\vec E=\langle E_x,E_y,0\rangle$, find $V_B-V_A$ for $A=\langle x_A,y_A,0\rangle$ and $B=\langle x_B,y_B,0\rangle$. The original problem used $\vec E=\langle200,-250,0\rangle$ V/m, $A=\langle0.02,0.03,0\rangle$ m, $B=\langle0.05,-0.06,0\rangle$ m.

> [!success]- Solution
> For a constant field, $\vec E$ comes out of the integral:
> $$V_B-V_A=-\int_A^B\vec E\cdot d\vec l=-\vec E\cdot(\vec r_B-\vec r_A)=\boxed{-\left[E_x(x_B-x_A)+E_y(y_B-y_A)\right]}$$
> Original numbers: $-\left[200(0.03)+(-250)(-0.09)\right]=-(6+22.5)=-28.5\ \text{V}$.
>
> **Lesson:** only the displacement **along** $\vec E$ matters, and the path shape doesn't.

---

# Part 3 — Circuits (Batteries & Resistors)

> [!info] Sign conventions (memorize)
> When walking a loop: battery $-\to+$ is $+\mathcal E$; battery $+\to-$ is $-\mathcal E$; through a resistor **with** the current is $-IR$; **against** the current is $+IR$. At a junction: current in = current out.

## 3.1 Single loop, opposing batteries
*(original; same skills as Fall 2014 Test 3 Problem 2)*

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
\draw (0,0) to[battery1,invert,l=$\mathcal{E}_1$] (0,3) to[R,l=$R_1$] (4,3);
\draw (4,0) to[battery1,invert,l_=$\mathcal{E}_2$] (4,3);
\draw (0,0) to[R,l_=$R_2$] (4,0);
\fill (4,3) circle (2.5pt) node[above right]{a};
\fill (0,0) circle (2.5pt) node[below left]{b};
\end{circuitikz}
\end{document}
```

> [!question] Problem
> A single loop contains $\mathcal E_1$ (left side, $+$ on top), $R_1$ (top), $\mathcal E_2$ (right side, $+$ on top), and $R_2$ (bottom). Point $a$ is the top-right corner and point $b$ is the bottom-left corner. Assume $\mathcal E_1>\mathcal E_2$.
> 1. Find the current $I$ (magnitude and direction).
> 2. Find $V_a-V_b$ two different ways.
> 3. Find the power delivered or absorbed by each battery and dissipated in each resistor, and check energy conservation.

> [!success]- Solution
> **1.** Guess clockwise $I$. Walk clockwise from $b$:
> - up through $\mathcal E_1$ ($-\to+$): $+\mathcal E_1$
> - across $R_1$ with $I$: $-IR_1$
> - down through $\mathcal E_2$ ($+\to-$): $-\mathcal E_2$
> - across $R_2$ with $I$: $-IR_2$
> $$\mathcal E_1-IR_1-\mathcal E_2-IR_2=0\quad\Longrightarrow\quad\boxed{I=\frac{\mathcal E_1-\mathcal E_2}{R_1+R_2}}\ \text{clockwise}$$
> (If $\mathcal E_2>\mathcal E_1$, $I$ comes out negative, meaning the current runs counterclockwise.)
>
> **2.** Path 1, from $b$ up the left side and across the top:
> $$V_a-V_b=\mathcal E_1-IR_1=\mathcal E_1-\frac{R_1(\mathcal E_1-\mathcal E_2)}{R_1+R_2}=\boxed{\frac{\mathcal E_1R_2+\mathcal E_2R_1}{R_1+R_2}}$$
> Path 2, from $b$ across the bottom (against $I$, so $+IR_2$), then up through $\mathcal E_2$ ($-\to+$):
> $$V_a-V_b=IR_2+\mathcal E_2=\frac{\mathcal E_1R_2+\mathcal E_2R_1}{R_1+R_2}\ \checkmark$$
>
> **3.** $\mathcal E_1$ delivers $\mathcal E_1I$. $\mathcal E_2$ has current forced in at its $+$ terminal, so it **absorbs** $\mathcal E_2I$ (it's being charged). The resistors dissipate $I^2R_1$ and $I^2R_2$. Check: $\mathcal E_1I-\mathcal E_2I=I(\mathcal E_1-\mathcal E_2)=I^2(R_1+R_2)$ ✓.

---

## 3.2 Two batteries and three bulbs
*GPS 5, Problem 2*

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
\draw (0,3) to[battery1,l=1.5 V] (1.8,3) to[battery1,l=1.5 V] (3.6,3)
to[short] (4,3) to[lamp,l=Bulb 1] (6,3) -- (6.6,3);
\draw (6.6,3) to[short,*-] (6.6,4.1) to[lamp,l=Bulb 2] (9,4.1) -- (9,3);
\draw (6.6,3) -- (6.6,1.9) to[lamp,l_=Bulb 3] (9,1.9) to[short,-*] (9,3);
\draw (9,3) -- (9.8,3) -- (9.8,0) -- (5.6,0) to[nos] (4,0) -- (-0.8,0) -- (-0.8,3) -- (0,3);
\node[above left] at (0,3) {A}; \node[above] at (3.7,3.1) {N};
\node[below] at (4.1,2.9) {M}; \node[below] at (5.9,2.9) {L};
\node[above left] at (6.6,3) {K}; \node[above right] at (9,3) {D};
\node[below] at (5.6,-0.1) {C}; \node[below] at (4,-0.1) {B};
\node[cpos] at (-0.15,3.5) {$+$}; \node[cneg] at (3.75,3.5) {$-$};
\end{circuitikz}
\end{document}
```

> [!question] Problem
> Two batteries, each with EMF $\mathcal E$ (1.5 V), are in series ($A$ is the $+$ end, $N$ the $-$ end). They drive bulb 1 ($R_1$) in series with bulbs 2 and 3 ($R_2$, $R_3$) in parallel. A switch sits between $B$ and $C$. The wires are ideal. Original values: $R_1=14\,\Omega$, $R_2=35\,\Omega$, $R_3=28\,\Omega$.
> - **A.** With the switch open, find $V_B-V_C$.
> - **B.** With the switch open, find $V_D-V_K$.
> - **C.** With the switch closed (steady state), write the loop and node rules for $I_1,I_2,I_3$.
> - **D.** Solve for $I_1,I_2,I_3$.
> - **E.** How many electrons leave the battery at $N$ each second?
> - **F.** What power do the batteries deliver?

> [!success]- Solution
> **A.** With the switch open, **no current flows**, so there's no drop across any bulb. $B$ is wired to $A$, and $C$ connects through the (currentless) bulbs to $N$. So
> $$V_B-V_C=V_A-V_N=\boxed{2\mathcal E}=3.0\text{ V}$$
> The entire battery voltage appears across the open gap.
>
> **B.** No current means no drop across bulbs 2/3, so $\boxed{V_D-V_K=0}$.
>
> **C.** Current leaves the $+$ terminal $A$, goes around through $B$, $C$, $D$, through bulbs 2 and 3 in parallel to $K$, through bulb 1 to $N$.
> - Loop through bulb 2: $2\mathcal E-I_1R_1-I_2R_2=0$
> - Loop through bulb 3: $2\mathcal E-I_1R_1-I_3R_3=0$
> - Node at $D$ (or $K$): $I_1=I_2+I_3$
> - (The loop around bulbs 2 and 3 only, $I_2R_2-I_3R_3=0$, is not independent.)
>
> **D.** Subtracting the loops gives $I_2R_2=I_3R_3$. Combined with the node rule:
> $$I_1=\frac{2\mathcal E}{R_1+\frac{R_2R_3}{R_2+R_3}},\qquad I_2=I_1\frac{R_3}{R_2+R_3},\qquad I_3=I_1\frac{R_2}{R_2+R_3}$$
> With numbers: $R_{23}=\frac{35\cdot28}{63}=15.6\,\Omega$, so
> $$I_1=\frac{3.0}{29.6}\approx\boxed{0.101\text{ A}},\qquad I_2\approx\boxed{0.045\text{ A}},\qquad I_3\approx\boxed{0.056\text{ A}}$$
>
> **E.** Electrons flow opposite to conventional current, so they leave through the $-$ terminal $N$ at the rate
> $$\frac{I_1}{e}=\frac{0.101}{1.6\times10^{-19}}\approx\boxed{6.3\times10^{17}\ \text{electrons/s}}$$
>
> **F.** $P=(2\mathcal E)I_1=3.0\times0.101\approx\boxed{0.30\text{ W}}$. Check: $I_1^2R_1+I_2^2R_2+I_3^2R_3\approx0.144+0.071+0.089=0.30$ W ✓.

---

## 3.3 Four resistors, two batteries
*GPS 5, Problem 3*

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
\draw (0,0) to[R,l=$R_1$] (0,2.6) to[battery1,invert,l=$\mathcal{E}_A$] (0,5) -- (0,6) -- (5.5,6);
\draw (3,6) to[R,l=$R_2$,*-*] (3,3) to[R,l=$R_3$] (3,0);
\draw (5.5,3) to[battery1,invert,l_=$\mathcal{E}_B$] (5.5,6);
\draw (3,3) to[short,-*] (5.5,3) to[R,l_=$R_4$] (5.5,0);
\draw (0,0) -- (3,0) to[short,*-] (5.5,0);
\end{circuitikz}
\end{document}
```

> [!question] Problem
> Four identical resistors and two batteries are connected as shown. $\mathcal E_A$ and $R_1$ form the left branch. $R_2$ and $\mathcal E_B$ each connect the top wire to a middle wire. $R_3$ and $R_4$ each connect the middle wire to the bottom wire.
> - **A.** Mark directions for $I_1,\dots,I_4$.
> - **B.** Write the node rule relating $I_1,I_3,I_4$ (not $I_2$).
> - **C.** Write all the loop rules (symbols only).
> - **D.** Solve for the currents with $\mathcal E_A=6$ V, $\mathcal E_B=3$ V, and each $R=100\,\Omega$.

> [!success]- Solution
> **Spot the structure first.** There are only **three nodes**: top (T), middle (M), and bottom (Bot).
> - $R_2$ and $\mathcal E_B$ are both connected between T and M, so they're **in parallel**: $V_T-V_M=\mathcal E_B$ exactly.
> - $R_3$ and $R_4$ are both connected between M and Bot, so they're in parallel too.
>
> **A.** Choose $I_1$ **up** through $R_1$ (out of $\mathcal E_A$'s $+$ terminal), and $I_2$, $I_3$, $I_4$ all **down**.
>
> **B.** Everything that comes down through $R_3$ and $R_4$ must go back up the left branch:
> $$\boxed{I_1=I_3+I_4}$$
>
> **C.**
> - Big left loop (up the left branch, down $R_2$, down $R_3$): $\boxed{\mathcal E_A-I_1R_1-I_2R_2-I_3R_3=0}$
> - $R_2$–$\mathcal E_B$ loop (down $R_2$, up through $\mathcal E_B$ from $-$ to $+$): $\boxed{\mathcal E_B-I_2R_2=0}$
> - $R_3$–$R_4$ loop (down $R_3$, up $R_4$ against $I_4$): $\boxed{-I_3R_3+I_4R_4=0}$
>
> **D.**
> - From the second loop: $I_2=\mathcal E_B/R=3/100=\boxed{0.030\text{ A}}$.
> - Equal resistors give $I_3=I_4$, so $I_1=2I_3$.
> - The big loop becomes $\mathcal E_A-2I_3R-\mathcal E_B-I_3R=0$, so $I_3=\dfrac{\mathcal E_A-\mathcal E_B}{3R}=\dfrac{3}{300}=\boxed{0.010\text{ A}}=I_4$.
> - Then $I_1=\boxed{0.020\text{ A}}$.
>
> **Bonus:** at node T, $I_1$ comes in and $I_2$ goes down $R_2$. The rest goes down through $\mathcal E_B$: $I_1-I_2=-0.010$ A. The negative sign means $0.010$ A actually flows **up** through $\mathcal E_B$, out of its $+$ terminal.
>
> **Check** with the big loop: $6-2-3-1=0$ ✓.

---

## 3.4 Three branches, two batteries
*Adapted from Fall 2021 Test 2, Problem 3 (on the recommended list), with the capacitor replaced by a wire*

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
\draw (0,0) to[battery1,invert,l=$3\mathcal{E}$] (0,2) to[R,l=$R$,i>_=$I_a$] (0,4) -- (3,4) to[short,*-] (6,4);
\draw (3,4) to[battery1,invert,l=$\mathcal{E}$,i>^=$I_b$] (3,0);
\draw (6,4) to[R,l=$2R$,i>^=$I_c$] (6,0) -- (3,0) to[short,*-] (0,0);
\node[above] at (3,4) {A};
\node[below] at (3,0) {B};
\end{circuitikz}
\end{document}
```

> [!question] Problem
> Three branches connect node $A$ (top) to node $B$ (bottom):
> - **left:** battery $3\mathcal E$ ($+$ on top) in series with $R$
> - **middle:** battery $\mathcal E$ ($+$ on the **bottom**)
> - **right:** resistor $2R$
>
> Currents: $I_a$ up the left branch, $I_b$ down the middle, $I_c$ down the right.
> 1. Write the node rule and two independent loop rules.
> 2. Solve for $I_a,I_b,I_c$. Which one flows opposite to the guess?
> 3. Find $V_A-V_B$ two ways.
> 4. Check that the power supplied equals the power dissipated.

> [!success]- Solution
> **1.**
> - Node A: $\boxed{I_a=I_b+I_c}$
> - Left pane, clockwise (up the left, down the middle): $+3\mathcal E-I_aR+\mathcal E=0$. Going down the middle you enter the $-$ terminal and exit the $+$, so it's $+\mathcal E$.
> - Right pane, clockwise (down the right, up the middle): $-I_c(2R)-\mathcal E=0$. Going up the middle you go from $+$ to $-$, so it's $-\mathcal E$.
>
> **2.**
> $$I_a=\boxed{\frac{4\mathcal E}{R}},\qquad I_c=\boxed{-\frac{\mathcal E}{2R}},\qquad I_b=I_a-I_c=\boxed{\frac{9\mathcal E}{2R}}$$
> $I_c<0$: the current through $2R$ actually flows **up**, from $B$ to $A$.
>
> **3.**
> - Walking from $B$ up the middle ($+\to-$): $V_A-V_B=\boxed{-\mathcal E}$.
> - Walking up the right branch against the assumed $I_c$: $+I_c(2R)=-\mathcal E$ ✓.
>
> **4.**
> - Supplied: $3\mathcal E\cdot I_a=\dfrac{12\mathcal E^2}{R}$. The middle battery has $I_b$ entering its $-$ and leaving its $+$, so it also supplies: $\mathcal E\cdot I_b=\dfrac{9\mathcal E^2}{2R}$. Total $\dfrac{33\mathcal E^2}{2R}$.
> - Dissipated: $I_a^2R+I_c^2(2R)=\dfrac{16\mathcal E^2}{R}+\dfrac{\mathcal E^2}{2R}=\dfrac{33\mathcal E^2}{2R}$ ✓.

---

## 3.5 Conveyor belt and wires of different thickness
*GPS 5, Problem 1 (uses the formula sheet's mobility notation)*

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
\fill[cgry] (-0.75,-1.2) rectangle (-0.6,1.9);
\fill[cgry] (0.6,-1.2) rectangle (0.75,1.9);
\node at (-0.68,2.25) {$+$}; \node at (0.68,2.25) {$-$};
\draw[dim] (-0.6,1.6)--(0.6,1.6) node[midway,above]{\small$s$};
\draw[thick,rounded corners=6pt] (-0.45,0.3) rectangle (0.45,0.75);
\node[nc,minimum size=3.5mm] at (-0.15,1.05) {\tiny$-$};
\draw[-{Stealth},thick] (0.05,1.05)--(0.45,1.05) node[above]{\small$F$};
\node at (0,-0.5) {\small$\times\,a$};
\draw[line width=6pt,cgry] (-0.75,1.2)--(-4,1.2) arc (90:270:1.6) -- (-2.2,-2);
\draw[line width=2pt,cgry] (-2.2,-2)--(-1.4,-2);
\draw[line width=6pt,cgry] (-1.4,-2)--(1.4,-2);
\draw[line width=2pt,cgry] (1.4,-2)--(2.2,-2);
\draw[line width=6pt,cgry] (2.2,-2)--(4,-2) arc (-90:90:1.6) -- (0.75,1.2);
\node at (-2.4,1.7) {\small$\times\,b$};
\node at (-6,-0.4) {\small$c\times$};
\node at (-1.8,-2.5) {\small$\times\,d$};
\node[above,font=\small] at (-2.4,2.05) {thick: $L_1$, $D_1$};
\node[above,font=\small] at (2.4,2.05) {thick: $L_1$, $D_1$};
\node[below,font=\small] at (0,-2.4) {thick $L_3$};
\node[below,font=\small] at (1.8,-2.4) {thin $L_2$};
\node[font=\small,align=left] at (0,-3.6) {thin wires: length $L_2$, diameter $D_2$;\quad $3L_2=3L_3=L_1$, $3D_2=D_1$};
\end{tikzpicture}
\end{document}
```

> [!question] Problem
> A frictionless conveyor belt carries electrons left to right across a gap $s$ between two large metal plates, applying a constant force $F$ to each electron. Wires connect the plates around a loop:
> - two thick wires of length $L_1$ (diameter $D_1$)
> - a thick bottom-middle wire of length $L_3$ (diameter $D_1$)
> - two thin wires of length $L_2$ (diameter $D_2$)
>
> with $3L_2=3L_3=L_1$ and $3D_2=D_1$. The wires have $n$ free electrons per m³ and mobility $u$.
> - **A.** Describe the steady-state field directions and the approximate surface charge.
> - **B.** Find the field magnitudes $E_a$ (in the gap), $E_b$ and $E_c$ (thick wire), and $E_d$ (thin wire).

> [!success]- Solution
> **A.** The belt piles electrons onto the **right** plate ($-$), leaving the left plate $+$. In the wires, conventional current flows from the $+$ (left) plate around the loop to the $-$ (right) plate. $\vec E$ in every wire points **along** that current. In the gap, $\vec E$ points from the left plate to the right plate. Surface charge goes from $+$ near the left plate, smoothly through zero, to $-$ near the right plate, with the steepest gradient along the thin wires (where $E$ is biggest).
>
> **B.**
> - **Gap:** each electron moves at steady speed with no friction, so $F$ balances the electric force: $eE_a=F$, giving $\boxed{E_a=F/e}$. The EMF is $\mathcal E=E_as=Fs/e$.
> - **Same current everywhere** (series, steady state): $I=enAuE$, so $E\propto1/A$. Since $D_2=D_1/3$, $A_{\text{thin}}=A_{\text{thick}}/9$, so $E_{\text{thin}}=9E_{\text{thick}}$.
> - **Loop rule:** the EMF equals the sum of $EL$ around the wires:
> $$E_{\text{thick}}(2L_1+L_3)+E_{\text{thin}}(2L_2)=\frac{Fs}{e}$$
> With $L_2=L_3=L_1/3$: $E_{\text{thick}}\left(\tfrac73L_1\right)+9E_{\text{thick}}\left(\tfrac23L_1\right)=\tfrac{25}{3}L_1E_{\text{thick}}$. So
> $$\boxed{E_b=E_c=\frac{3Fs}{25\,eL_1}},\qquad \boxed{E_d=\frac{27Fs}{25\,eL_1}}$$
> $n$ and $u$ cancel out. You'd need them only to get the current: $I=enA_1uE_b$.

---

## 3.6 Quick conceptual checks
*(from lecture clickers and the old tests)*

> [!question] Questions
> 1. A constant current flows through a wire that narrows in the middle (region 2) and widens again. Rank $E_1,E_2,E_3$.
> 2. Electrons collide with Pt ions more often than with Cu ions. Same battery, same loop shape: which has the larger drift speed?
> 3. Two identical bulbs in series across a battery $\mathcal E$: what power does one bulb dissipate? What if they're in parallel?
> 4. A metal loop with **no battery**: can a steady current flow?
> 5. Is Kirchhoff's junction rule a consequence of energy conservation or charge conservation? And the loop rule?
> 6. You add another bulb in parallel to an ideal battery circuit. What happens to the battery current, and to the brightness of the original bulb?

> [!success]- Answers
> 1. $E_1=E_3<E_2$. The same $I$ flows everywhere and $E=I/(\sigma A)$, so the field is biggest where the wire is thinnest.
> 2. **Cu.** More frequent collisions (smaller $\tau$) mean a smaller drift speed $v=e\tau E/m$.
> 3. Series: $I=\mathcal E/2R$, so each bulb dissipates $\mathcal E^2/4R$. Parallel: each dissipates $\mathcal E^2/R$ (brighter).
> 4. **No.** Without energy input, the loop reaches equilibrium with $E=0$ inside the metal. A battery is needed to maintain the steady state.
> 5. The junction rule comes from **charge** conservation. The loop rule comes from **energy** conservation (path independence of $V$).
> 6. The total resistance drops, so **more** battery current flows. The original bulb is **unchanged**, because it still has the full $\mathcal E$ across it.

---

# Answer Key

| # | Final answer(s) |
|---|---|
| 1.1 | $d\vec E=\frac{kQ\,dy}{L(h+y)^2}\hat y$; $\ \vec E=\frac{kQ}{h(h+L)}\hat y$; T: $\frac{kQ}{h+L}\left(\frac1h+\frac1{\sqrt{(h+L)^2+L^2/4}}\right)\hat y$ |
| 1.2 | $dQ=-\frac{2Q}{\pi}d\theta$; $\ \vec E=\frac{2kQ}{\pi R^2}\langle1,1,0\rangle$; D: (b) |
| 1.3 | $\vec E=\frac{kQ}{\alpha R^2}\langle\sin\alpha,1-\cos\alpha,0\rangle$ |
| 1.4 | $\vec E=\frac{4kQ}{L}\left(\frac1x-\frac1{\sqrt{x^2+L^2/4}}\right)\hat y\to\frac{kQL}{2x^3}\hat y$ |
| 1.5 | $\vec E=\frac{8kQz}{3R^2}\left(\frac1{\sqrt{z^2+R^2/4}}-\frac1{\sqrt{z^2+R^2}}\right)\hat z$; near center: $\frac{8kQz}{3R^3}\hat z$ |
| 1.6 | $Q=\frac12\alpha L^2$; $\ \vec E=-k\alpha\left[\ln(1+L/d)-\frac{L}{L+d}\right]\hat x$ |
| 1.7 | $\hat p$: 7; $\ \vec F$: 3; $\ \vec E_{\text{Mario}}=\frac{3kQ}{4d^2}\hat x$ |
| 1.8 | $\lvert\vec E_{\text{metal}}\rvert=\frac{4kQ}{d^2}\sqrt{1+4s^2/d^2}$ |
| 2.1 | $2kQ\left(\frac1{R_a}-\frac1{R_b}\right)$; $\ kQ\left(\frac2{R_a}-\frac1{R_b}\right)$; no change |
| 2.2 | $\Delta U_1=-\frac{eQs}{\pi R^2\epsilon_0}$; $\ v_f=\sqrt{v_0^2+\frac{8eQs}{\pi R^2\epsilon_0m_e}}$ |
| 2.3 | $\frac{3kqs}{4d^2}$; $\ K_f=\frac{ekqs}{4d^2}$; $\ \frac{kqs}{4d^2}$ |
| 2.4 | $kes\left(\frac1{d_2^2}-\frac1{d_1^2}\right)$; $\ v=\frac e{d_2}\sqrt{\frac{2ks}{m_p}}$; $\ 0$; $\ -\frac{kes}{d_1^2}$ |
| 2.5 | $V_{\text{tube}}-V_{\text{wire}}=\frac{2kQ}{L}\ln\frac rR<0$ |
| 2.6 | $\pm\frac{kQ}{L}(2-\sqrt2)$; $\ kQ\left(\frac1R-\frac1L\right)$; no change |
| 2.7 | $0$; $\ \frac{kp}{R^2}$; $\ -\frac{kp\sin\theta}{R^2}$; speed decreases |
| 2.8 | $-[E_x\Delta x+E_y\Delta y]$ ($-28.5$ V) |
| 3.1 | $I=\frac{\mathcal E_1-\mathcal E_2}{R_1+R_2}$; $\ V_a-V_b=\frac{\mathcal E_1R_2+\mathcal E_2R_1}{R_1+R_2}$ |
| 3.2 | $3.0$ V; $0$; $I_1\approx0.101$, $I_2\approx0.045$, $I_3\approx0.056$ A; $6.3\times10^{17}$/s; $0.30$ W |
| 3.3 | $I_1=I_3+I_4$; $I_1=0.020$, $I_2=0.030$, $I_3=I_4=0.010$ A |
| 3.4 | $I_a=\frac{4\mathcal E}R$, $I_b=\frac{9\mathcal E}{2R}$, $I_c=-\frac{\mathcal E}{2R}$; $V_A-V_B=-\mathcal E$ |
| 3.5 | $E_a=\frac Fe$; $E_b=E_c=\frac{3Fs}{25eL_1}$; $E_d=\frac{27Fs}{25eL_1}$ |
