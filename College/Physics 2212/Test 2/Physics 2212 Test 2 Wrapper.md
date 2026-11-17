# Test 2 Wrapper

[[Physics 2212 Test 2 Notes]] | [[Physics 2212 Test 2 Review]]

---

## Problem 1 (30 pts) — Concentric Spheres

Plastic sphere radius $R_1$, charge $-Q_1$ on surface. Metal shell inner $R_2$, outer $R_3$, inner surface $+Q_2$, outer surface $+Q_3$. $Q_2+Q_3>Q_1$.

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{cred}{RGB}{170,60,60}
\definecolor{cblue}{RGB}{55,95,175}
\begin{document}
\begin{tikzpicture}[font=\small]
\begin{scope}[even odd rule]
  \fill[cblue] (0,0) circle (3) (0,0) circle (2);
\end{scope}
\fill[cred] (0,0) circle (1);
\draw[thick] (0,0) circle (1);
\draw[thick] (0,0) circle (2);
\draw[thick] (0,0) circle (3);
\draw[-{Stealth}] (-3.6,0)--(4,0) node[right]{$x$};
\draw (1,0.1)--(1,-0.1) node[below]{$R_1$};
\draw (2,0.1)--(2,-0.1) node[below]{$R_2$};
\draw (3,0.1)--(3,-0.1) node[below]{$R_3$};
\node at (0,0) {$-Q_1$};
\node at (0,2.4) {$+Q_2$};
\node at (0,3.35) {$+Q_3$};
\node at (1.5,0.25) {\small air};
\node at (-2.5,0) {\small metal};
\end{tikzpicture}
\end{document}
```

Gaussian surface radius $r$: $\;E(4\pi r^2)=Q_\text{enc}/\varepsilon_0 \implies E = kQ_\text{enc}/r^2$

| Region          | $Q_\text{enc}$ | $                    | \vec E           | $   | Direction |
| --------------- | -------------- | -------------------- | ---------------- | --- | --------- |
| $r < R_1$       | $0$            | $0$                  | —                |     |           |
| $R_1 < r < R_2$ | $-Q_1$         | $kQ_1/r^2$           | radially inward  |     |           |
| $R_2 < r < R_3$ | $0$            | $0$                  | — (conductor)    |     |           |
| $r > R_3$       | $Q_2+Q_3-Q_1$  | $k(Q_2+Q_3-Q_1)/r^2$ | radially outward |     |           |

---

## Problem 2 (4 pts) — Find $Q_2$

Inside conductor: $E=0 \implies Q_\text{enc}=0$

$$-Q_1 + Q_2 = 0 \implies \boxed{Q_2 = Q_1}$$

---

## Problem 3 (10 pts) — Disk: $d\vec E$ from ring of radius $r$, thickness $dr$

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{cred}{RGB}{214,39,40}
\definecolor{cblue}{RGB}{31,119,180}
\begin{document}
\begin{tikzpicture}[font=\small]
\fill[gray!15] (-3,-0.07) rectangle (3,0.07);
\draw[thick] (-3,0)--(3,0);
\draw[cred, line width=3.5pt] (1.8,0)--(2.2,0);
\draw[-{Stealth}] (0,-0.8)--(0,4.6) node[above]{$z$};
\draw[-{Stealth}] (-3.3,0)--(3.6,0) node[right]{};
\draw[{Stealth}-{Stealth}] (0,-0.6)--(3,-0.6) node[midway,below]{$R$};
\draw[{Stealth}-{Stealth}] (0,0.35)--(2.0,0.35) node[midway,above]{$r$};
\draw[{Stealth}-{Stealth}] (1.8,-0.6)--(2.2,-0.6) node[midway,below]{$dr$};
\fill (0,3.5) circle (3pt) node[right]{$P$};
\draw[dashed] (2.0,0)--(0,3.5);
\node[right] at (1.15,1.85) {$d=\!\sqrt{r^2+z_0^2}$};
\draw[{Stealth}-{Stealth}] (-0.35,0)--(-0.35,3.5) node[midway,left]{$z_0$};
\draw (0,3.5) ++(270:0.65) arc(270:300:0.65);
\node at (0.28,2.88) {$\theta$};
\draw[-{Stealth}, cblue, very thick] (0,3.5)--(0,4.3) node[right]{$d\vec{E}$};
\end{tikzpicture}
\end{document}
```

$$\sigma = \frac{Q}{\pi R^2}$$

$$dA = 2\pi r\,dr \implies dq = \sigma\,dA = \frac{2Q\,r\,dr}{R^2}$$

$$d = \sqrt{r^2+z_0^2}, \qquad \cos\theta = \frac{z_0}{\sqrt{r^2+z_0^2}}$$

Horizontal components cancel (symmetry). Only $\hat z$ survives:

$$dE_z = \frac{k\,dq}{d^2}\cos\theta = \frac{k\,dq\,z_0}{(r^2+z_0^2)^{3/2}}$$

Substitute $dq$:

$$\boxed{d\vec E = \frac{2kQz_0\,r\,dr}{R^2(r^2+z_0^2)^{3/2}}\,\hat z}$$

**Try it:**
- $z_0=0$ — why is $E=0$?
- Washer (inner radius $a$) — change lower integration limit to $a$
- $z_0 \gg R$ — should recover $E = kQ/z_0^2$
