# AP Precalculus Review

> [!abstract] Exam at a glance
> **2 h 55 min, Units 1–3 only.** 42 multiple choice: 29 without a calculator, then 13 with one. 4 FRQs: 1 and 2 with a calculator, 3 and 4 without. Radian mode; round to 3 decimals at the end.
> Units: 1 (30–40%), 2 (25–40%), 3 (30–35%). Unit 4 (matrices) isn't on the exam.
> Full explanations and diagrams: [[AP Precalculus Notes]] · Practice: [[AP Precalculus Practice]]

---

# Unit 0 — Prerequisites

| Skill | Key fact |
|---|---|
| Slope | $m=\frac{y_2-y_1}{x_2-x_1}$; point-slope $y-y_1=m(x-x_1)$ |
| Inequalities | multiplying or dividing by a negative flips the sign |
| Factoring | GCF first; $a^2-b^2=(a-b)(a+b)$; AC method; $a^3\pm b^3=(a\pm b)(a^2\mp ab+b^2)$ |
| Quadratic formula | $x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}$; vertex at $x=-\frac b{2a}$ |
| Discriminant $b^2-4ac$ | $>0$ two real, $=0$ one repeated, $<0$ two non-real |
| Exponents | $b^mb^n=b^{m+n}$, $(b^m)^n=b^{mn}$, $b^{-n}=\frac1{b^n}$, $b^{m/n}=\sqrt[n]{b^m}$ |
| Complex numbers | $i^2=-1$; divide by multiplying by the conjugate $a-bi$ |
| Percent change | $a(1+r)^t$ growth, $a(1-r)^t$ decay |

---

# Unit 1A — Polynomial Functions

### 1.1–1.3 Functions, rates of change, concavity

| Term | Meaning |
|---|---|
| Function | each input → exactly one output |
| Domain / range | set of inputs / set of outputs |
| Independent / dependent variable | input / output |
| Increasing on an interval | $a<b\Rightarrow f(a)<f(b)$ |
| Zero | input where the output is 0 ($x$-intercept) |
| AROC on $[a,b]$ | $\frac{f(b)-f(a)}{b-a}$ = slope of the secant line; units "output per input" |
| Rate of change at a point | estimated by AROC over a tiny interval |
| Concave up / down | rate of change increasing / decreasing |
| Point of inflection | concavity switches |

- **Linear:** constant AROC (constant first differences). **Quadratic:** AROCs over consecutive equal intervals change by a constant (constant second differences).
- **Concave up → secant above the graph; concave down → secant below.**
- "At an increasing rate" = rate of change increasing = concave up (whatever the direction).

| | Concave up | Concave down |
|---|---|---|
| Increasing | increasing at an increasing rate | increasing at a decreasing rate |
| Decreasing | decreasing at an increasing rate | decreasing at a decreasing rate |

### 1.4–1.6 Polynomials

- $p(x)=a_nx^n+\dots+a_0$: degree $n$, leading coefficient $a_n$.
- Local extremum where the function switches between increasing and decreasing; between two real zeros there's at least one. An even-degree polynomial has a global max or min.
- Degree $n$ → exactly $n$ complex zeros (with multiplicity). Non-real zeros come in conjugate pairs $a\pm bi$.
- $(x-a)$ is a factor ⇔ $a$ is a zero. Degree = the first $n$ with constant $n$th differences.

| Multiplicity | Graph | Sign |
|---|---|---|
| 1 | crosses | changes |
| even | bounces (tangent) | stays |
| odd ≥ 3 | flattens, crosses | changes |

| | Even function | Odd function |
|---|---|---|
| Rule | $f(-x)=f(x)$ | $f(-x)=-f(x)$ |
| Symmetry | $y$-axis | origin |
| Example | $x^2$, $\cos x$ | $x^3$, $\sin x$ |

| End behavior | Leading coefficient $>0$ | Leading coefficient $<0$ |
|---|---|---|
| Even degree | ↑ ↑ | ↓ ↓ |
| Odd degree | ↓ ↑ | ↑ ↓ |

Write it as $\lim_{x\to\infty}p(x)=\infty$, etc.

---

# Unit 1B — Rational Functions

| Comparing degrees (numerator vs. denominator) | End behavior |
|---|---|
| lower | horizontal asymptote $y=0$ |
| equal | horizontal asymptote $y=\frac{\text{leading coefficient of numerator}}{\text{leading coefficient of denominator}}$ |
| one higher | slant asymptote = quotient from long division |
| two or more higher | like the polynomial quotient of leading terms |

| Feature | Rule |
|---|---|
| Zero | numerator zero that's in the domain |
| Vertical asymptote $x=a$ | denominator zero with higher multiplicity than in the numerator |
| Hole at $x=c$ | multiplicity in numerator ≥ multiplicity in denominator; $y$-value = simplified function at $c$ |
| One-sided limits | $x\to a^+$ from the right, $x\to a^-$ from the left; test a nearby value for the sign |
| Rational inequality | sign chart with zeros of numerator **and** denominator |

- **Factored form** → zeros, asymptotes, holes, domain. **Standard form** → end behavior.
- **Long division:** $f=gq+r$; slant asymptote $y=q(x)$. Example: $\frac{x^2+3x+5}{x-1}=x+4+\frac9{x-1}$, so $y=x+4$.
- **Binomial theorem:** coefficients of $(a+b)^n$ = row $n$ of Pascal's triangle (1; 1 1; 1 2 1; 1 3 3 1; 1 4 6 4 1). $(x+2)^4=x^4+8x^3+24x^2+32x+16$.

---

# Unit 1C — Transformations, Piecewise, Models

| Form | Effect |
|---|---|
| $f(x)+k$ | up $k$ |
| $f(x+h)$ | left $h$ (opposite sign) |
| $a\,f(x)$ | vertical dilation by $\lvert a\rvert$; $a<0$ flips over the $x$-axis |
| $f(bx)$ | horizontal dilation by $\frac1{\lvert b\rvert}$; $b<0$ flips over the $y$-axis |

- $y=a\,f(b(x-h))+k$ sends $(x,y)\to\left(\frac xb+h,\ ay+k\right)$.
- **Piecewise:** use the piece whose condition holds; closed dot for $\le,\ge$, open for $<,>$. $|2x-3|=-2x+3$ for $x<1.5$, $2x-3$ for $x\ge1.5$.

| Model | Clue |
|---|---|
| Linear | constant rate of change |
| Quadratic | linear rate of change, one max/min, area |
| Cubic | volume; constant third differences |
| Degree $n$ polynomial | $n+1$ points fit exactly; several zeros or extrema |
| Piecewise | different behavior on different intervals |
| Rational | inverse proportion ($\frac k{d^2}$) |

- Models have assumptions and need domain/range restrictions from context (time ≥ 0, whole people).
- Regressions: linear, quadratic, cubic, quartic.

---

# Unit 2A — Sequences and Exponentials

| | Arithmetic / linear | Geometric / exponential |
|---|---|---|
| Step | add $d$ (or slope $m$) | multiply by $r$ (or base $b$) |
| Formula | $a_n=a_0+dn=a_k+d(n-k)$ | $g_n=g_0r^n=g_kr^{n-k}$ |
| Function | $f(x)=b+mx=y_i+m(x-x_i)$ | $f(x)=ab^x=y_ib^{x-x_i}$ |
| Equal input steps | outputs change by a constant amount | outputs change by a constant factor (proportional) |

- $f(x)=ab^x$: $a\ne0$, $b>0$, $b\ne1$. Growth $b>1$, decay $0<b<1$. Asymptote $y=0$ (or $y=k$ for $ab^x+k$). Always increasing or decreasing, one concavity, no extrema, no inflection.
- $b^{x+k}=b^k\cdot b^x$ (horizontal shift = vertical dilation); $b^{cx}=(b^c)^x$ (horizontal dilation = new base); $b^{-x}=(\frac1b)^x$.
- Growth factor $b=1+r$; change time units by rewriting: $2^d=128^{d/7}$ (daily ×2 = weekly ×128).
- $e\approx2.718$. Half-life: $A_0(\frac12)^{t/h}$.
- **Residual** = actual − predicted (positive = model underestimates). Good model: residual plot has no pattern.
- **Composition** $f(g(x))$: $g$ first. Not commutative. Domain: $x$ in the domain of $g$ with $g(x)$ in the domain of $f$. The identity $I(x)=x$ changes nothing.

---

# Unit 2B — Inverses and Logarithms

- **Inverse:** exists when outputs never repeat (one-to-one). $f(a)=b\iff f^{-1}(b)=a$; swap $x$ and $y$ and solve; reflect over $y=x$; domain and range swap; $f(f^{-1}(x))=x$. $f^{-1}\ne\frac1f$.
- **Decompose:** $\sqrt{3x+1}=f(g(x))$ with $f=\sqrt x$, $g=3x+1$. Adding/multiplying inside = horizontal; outside = vertical.
- **Log:** $\log_bc=a\iff b^a=c$. $\log$ = base 10, $\ln$ = base $e$. A log scale goes $10^0,10^1,10^2,\dots$

| Feature | $b^x$ | $\log_bx$ |
|---|---|---|
| Domain | all reals | $x>0$ |
| Range | $y>0$ | all reals |
| Asymptote | $y=0$ | $x=0$ |
| Key point | $(0,1)$ | $(1,0)$ |
| Pattern | outputs multiply as inputs add | outputs add as inputs multiply |

| Property | Rule |
|---|---|
| Product | $\log_b(xy)=\log_bx+\log_by$ |
| Quotient | $\log_b\frac xy=\log_bx-\log_by$ |
| Power | $\log_bx^n=n\log_bx$ |
| Change of base | $\log_bx=\frac{\ln x}{\ln b}$ |
| Inverse | $\log_bb^x=x$, $b^{\log_bx}=x$ |

**Solving:**

- Match bases: $2^{x+1}=2^{3x}\Rightarrow x=\frac12$.
- Take logs: $5^x=20\Rightarrow x=\frac{\ln20}{\ln5}$.
- Isolate the log and exponentiate: $\log_2(x-1)=2\Rightarrow x=5$.
- Condense logs, then **check for extraneous solutions** (every log argument must be $>0$).
- $e^{2x}-5e^x+6=0$: factor as a quadratic in $e^x$.
- Inequalities: base $<1$ flips the sign.
- Inverse of $3\cdot2^{x-1}+4$ is $1+\log_2\frac{x-4}3$.

**Modeling:**

- Log model: inputs ×constant while outputs +constant. LnReg gives $y=a+b\ln x$.
- **Semi-log plot** (log $y$-axis): exponential data look linear; $y=ab^x\to\log y=(\log b)x+\log a$.

---

# Unit 3A — Sine and Cosine

- **SOH CAH TOA.** Special triangles: 45-45-90 → $1:1:\sqrt2$; 30-60-90 → $1:\sqrt3:2$.
- **Period:** smallest $k$ with $f(x+k)=f(x)$.
- **Radian:** $\theta=\frac sr$; $2\pi$ = full turn; degrees × $\frac\pi{180}$. Positive = counterclockwise; coterminal angles differ by $2\pi k$.
- **Unit circle:** $P=(\cos\theta,\sin\theta)$; radius $r$: $(r\cos\theta,r\sin\theta)$; $\tan\theta=\frac{\sin\theta}{\cos\theta}$ = slope of the terminal ray.

| $\theta$ | $0$ | $\frac\pi6$ | $\frac\pi4$ | $\frac\pi3$ | $\frac\pi2$ |
|---|---|---|---|---|---|
| $\sin$ | $0$ | $\frac12$ | $\frac{\sqrt2}2$ | $\frac{\sqrt3}2$ | $1$ |
| $\cos$ | $1$ | $\frac{\sqrt3}2$ | $\frac{\sqrt2}2$ | $\frac12$ | $0$ |
| $\tan$ | $0$ | $\frac{\sqrt3}3$ | $1$ | $\sqrt3$ | undefined |

Signs: All (QI), Sin (QII), Tan (QIII), Cos (QIV). Use the reference angle for the size.

**$y=a\sin(b(\theta+c))+d$** (same for cosine):

| Parameter | Gives |
|---|---|
| $\lvert a\rvert$ | amplitude $=\frac{\max-\min}2$ |
| $b$ | period $\frac{2\pi}{\lvert b\rvert}$; frequency $=\frac1{\text{period}}$ |
| $c$ | phase shift $-c$ (factor $b$ out first) |
| $d$ | midline $y=d=\frac{\max+\min}2$ |

- $\cos\theta=\sin(\theta+\frac\pi2)$. Sine is odd, cosine is even.
- Above the midline the graph is concave down; below it, concave up.
- Key points every $\frac{\text{period}}4$: cosine starts at a max, sine on the midline going up.
- **Modeling:** period = time between maxima; $b=\frac{2\pi}{\text{period}}$; match the start to set $a$'s sign and $c$.

---

# Unit 3B — Tangent, Inverse Trig, Identities, Polar

| Function | Period | Vertical asymptotes | Range |
|---|---|---|---|
| $\tan\theta=\frac{\sin}{\cos}$ | $\pi$ | $\frac\pi2+k\pi$ | all reals |
| $\sec\theta=\frac1{\cos}$ | $2\pi$ | $\frac\pi2+k\pi$ | $\lvert y\rvert\ge1$ |
| $\csc\theta=\frac1{\sin}$ | $2\pi$ | $k\pi$ | $\lvert y\rvert\ge1$ |
| $\cot\theta=\frac{\cos}{\sin}$ | $\pi$ | $k\pi$ | all reals |

Tangent increases between asymptotes (inflection at its zeros); cotangent decreases. For $a\tan(b(\theta+c))+d$, the period is $\frac\pi{\lvert b\rvert}$.

| Inverse | Input | Output |
|---|---|---|
| $\arcsin x$ | $[-1,1]$ | $[-\frac\pi2,\frac\pi2]$ |
| $\arccos x$ | $[-1,1]$ | $[0,\pi]$ |
| $\arctan x$ | all reals | $(-\frac\pi2,\frac\pi2)$ |

- **Trig equations:** isolate; find all solutions in $[0,2\pi)$ (two quadrants!); add $2\pi k$ (sine, cosine) or $\pi k$ (tangent). For $\cos2\theta$, go around twice.
- **Identities:**
  - $\sin^2\theta+\cos^2\theta=1$, $\tan^2\theta+1=\sec^2\theta$, $1+\cot^2\theta=\csc^2\theta$
  - $\sin(\alpha\pm\beta)=\sin\alpha\cos\beta\pm\cos\alpha\sin\beta$
  - $\cos(\alpha\pm\beta)=\cos\alpha\cos\beta\mp\sin\alpha\sin\beta$
  - $\sin2\theta=2\sin\theta\cos\theta$, $\cos2\theta=\cos^2\theta-\sin^2\theta=2\cos^2\theta-1=1-2\sin^2\theta$
- **Polar** $(r,\theta)$: $x=r\cos\theta$, $y=r\sin\theta$, $r^2=x^2+y^2$, $\theta=\arctan\frac yx$ ($+\pi$ if $x<0$). Negative $r$ = opposite direction. $a+bi$ = $r\cos\theta+ir\sin\theta$.

| Polar curve | Equation | Tell |
|---|---|---|
| Circle | $r=a$; $r=a\cos\theta$ or $a\sin\theta$ | centered at pole; through pole |
| Rose | $r=a\cos n\theta$ | $n$ petals if $n$ odd, $2n$ if $n$ even |
| Cardioid | $r=a\pm a\cos\theta$ | touches the pole once |
| Limaçon with loop | $r=a\pm b\cos\theta$, $a<b$ | inner loop |
| Dimpled / convex limaçon | $a>b$ | dimpled if $a<2b$, convex if $a\ge2b$ |

| Polar rate of change | $r$ increasing | $r$ decreasing |
|---|---|---|
| $r>0$ | away from the pole | toward the pole |
| $r<0$ | toward the pole | away from the pole |

AROC of $r$ = $\frac{\Delta r}{\Delta\theta}$ (radius per radian).

---

# Unit 4 — Matrices (not on the AP exam)

| Term | Fact |
|---|---|
| $n\times m$ matrix | $n$ rows, $m$ columns |
| Product $AB$ | needs columns of $A$ = rows of $B$; entry = row · column |
| Identity $I$ | 1s on the diagonal; $AI=A$ |
| Determinant | $\det\begin{bmatrix}a&b\\c&d\end{bmatrix}=ad-bc$; $\lvert\det\rvert$ = parallelogram area / area scale factor |
| Inverse | $\frac1{ad-bc}\begin{bmatrix}d&-b\\-c&a\end{bmatrix}$, exists iff $\det\ne0$ |
| System $AX=B$ | $X=A^{-1}B$ |
| Linear transformation | $L(\vec v)=A\vec v$; columns of $A$ = images of $\langle1,0\rangle,\langle0,1\rangle$ |
| Rotation by $\theta$ | $\begin{bmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{bmatrix}$ |
| Composition | $B$ then $A$ = $AB$ |
| Transition matrix | next state $=T\vec x$; past state $=T^{-1}\vec x$; steady state $T\vec x=\vec x$ |

---

# FRQ Scripts

| FRQ | Calculator | Content | Must-know move |
|---|---|---|---|
| 1 Function concepts | yes | Units 1–2: composition, inverse, zeros, end behavior, model type | show work for $f(g(\#))$; justify with the reasons below |
| 2 Non-periodic modeling | yes | Units 1–2 in context | A: set up equations; B: AROC + secant estimate + concavity comparison; C: model limitation |
| 3 Periodic modeling | no | sinusoid in context | A: F,P max, J min, G,K midline, step $\frac{\text{period}}4$; B: $a,b,c,d$; C: behavior + concavity |
| 4 Symbolic | no | exp, log, trig, inverse trig | solve and rewrite with full work; general solutions |

| Model type | Justification |
|---|---|
| Linear | outputs change by a constant over equal-length input intervals |
| Quadratic | second differences constant over equal-length input intervals |
| Exponential | outputs proportional (×constant) over equal-length input intervals |
| Logarithmic | inputs change proportionally while outputs change by equal amounts |
| Invertible | each output comes from a unique input (no repeated outputs) |
| Not invertible | cite a repeat: "$f(3)=f(5)=2$" (not "horizontal line test") |

**FRQ 2 concavity script:** "Because $f$ is concave down on $(t_1,t_2)$, the secant line is below the graph there, so AROC estimates are **less** than the model on $(t_1,t_2)$" (and greater beyond $t_2$). For concave up, everything flips.

**FRQ 3 Part C script:** "The graph is concave up, and the rates of change are increasing over this interval." (Don't say "positive/negative" here.)

---

# Exam Traps

| Wrong-answer wording | Right concept |
|---|---|
| "$f(x+3)$ shifts right 3" | inside changes go the opposite way: left 3 |
| "$\sin(2\theta-\frac\pi2)$ shifts $\frac\pi2$" | factor out $b$: shift $\frac\pi4$ |
| "decreasing at an increasing rate means concave down" | "increasing rate" means the rate of change increases: concave up |
| "Every denominator zero is a vertical asymptote" | if the factor cancels fully, it's a hole |
| "Horizontal asymptotes can't be crossed" | they describe only the ends; the middle can cross |
| "$f^{-1}(x)=\frac1{f(x)}$" | inverse means swapped inputs and outputs |
| "Passes the horizontal line test" as a justification | name a repeated output (or say none repeat) |
| "$\log(x+y)=\log x+\log y$" | only $\log(xy)$ splits into a sum |
| Keeping $x=-2$ in $\log_2x+\log_2(x-2)=3$ | extraneous: log arguments must be positive |
| "$\arcsin(\sin\frac{5\pi}6)=\frac{5\pi}6$" | arcsine outputs lie in $[-\frac\pi2,\frac\pi2]$: $\frac\pi6$ |
| "$\sin\theta=\frac12$ has one solution" | two per period ($\frac\pi6,\frac{5\pi}6$), plus $2\pi k$ |
| "Tangent has period $2\pi$ and an amplitude" | period $\pi$, no amplitude |
| "A negative $r$ means the point is moving toward the pole" | it depends on whether $\lvert r\rvert$ grows: negative and decreasing moves away |
| "Positive residual = overestimate" | positive residual = actual above the model = underestimate |
| "Concave up, so the secant estimate is too low" | concave up: the secant is above the graph, so estimates are too high (inside the interval) |
| "Even multiplicity zero crosses the axis" | even multiplicity bounces; the sign doesn't change |
| "$a_n$ starts at $n=1$" | AP sequences usually start at $a_0$; read the problem |
