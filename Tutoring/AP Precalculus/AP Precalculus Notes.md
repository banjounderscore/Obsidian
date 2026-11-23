# AP Precalculus Notes

> [!abstract] What this covers
> The whole year, by the class's units (0, 1A–1C, 2A–2B, 3A–3B, 4). Topic numbers match the handouts and the College Board framework.
>
> **AP exam** (2 h 55 min, Units 1–3): 42 multiple choice (29 no calculator, 13 calculator) and 4 FRQs (1–2 calculator, 3–4 no calculator). Radian mode. Weights: Unit 1 30–40%, Unit 2 25–40%, Unit 3 30–35%. Unit 4 isn't on it.
>
> 🔒 = lesson handout locked on the class Drive; written from the College Board framework.
>
> Quick version: [[AP Precalculus Review]] · Practice: [[AP Precalculus Practice]]

## Table of Contents
- [[#Unit 0 — Prerequisite Skills]]
- [[#Unit 1A — Polynomial Functions]]
- [[#Unit 1B — Rational Functions]]
- [[#Unit 1C — Transformations, Piecewise Functions, and Models]]
- [[#Unit 2A — Sequences and Exponential Functions]]
- [[#Unit 2B — Inverses and Logarithmic Functions]]
- [[#Unit 3A — Trigonometry, Sine, and Cosine]]
- [[#Unit 3B — Tangent, Inverse Trig, Identities, and Polar]]
- [[#Unit 4 — Matrices]]
- [[#Exam Strategy — The Four FRQs]]

---

# Unit 0 — Prerequisite Skills

In a quadratic, $a$, $b$, $c$ are the coefficients of $ax^2+bx+c$. In the factoring patterns, $a$ and $b$ stand for any two terms.

| Skill | Rule | Example |
|---|---|---|
| Slope | $m=\frac{y_2-y_1}{x_2-x_1}$ for the line through $(x_1,y_1)$ and $(x_2,y_2)$ | $(-2,5),(3,8)$: $m=\frac35$ |
| Line forms | point-slope $y-y_1=m(x-x_1)$; slope-intercept $y=mx+b$ ($b$ = $y$-intercept); standard $Ax+By=C$ ($A,B,C$ integers) | $3x-5y=-31$ |
| Inequalities | multiplying/dividing by a negative flips the sign | $-2x>6\Rightarrow x<-3$ |
| Difference of squares | $a^2-b^2=(a-b)(a+b)$ | $4x^2-81=(2x-9)(2x+9)$ |
| AC method | two numbers with product $ac$, sum $b$; split and group | $3x^2+13x-10=(3x-2)(x+5)$ |
| Sum/difference of cubes | $a^3\pm b^3=(a\pm b)(a^2\mp ab+b^2)$ | $x^3-8=(x-2)(x^2+2x+4)$ |
| Quadratic formula | $ax^2+bx+c=0\Rightarrow x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}$; vertex at $x=-\frac b{2a}$ | $2x^2-2x-5=0\Rightarrow x=\frac{1\pm\sqrt{11}}2$ |
| Discriminant | $b^2-4ac$: $>0$ two real, $=0$ one, $<0$ two non-real | $2x^2+3x+5$: $-31$ |
| Quadratic inequality | find zeros, test signs between them | $(3x-2)(x-5)>0\Rightarrow x<\frac23$ or $x>5$ |
| Rational expressions | factor and cancel; note excluded values | $\frac{x^2-x-6}{x^2-7x+12}=\frac{x+2}{x-4}$, $x\ne3,4$ |
| Percent change | $a(1+r)^t$ growth, $a(1-r)^t$ decay ($a$ = starting amount, $r$ = rate as a decimal, $t$ = time) | 30%/h: $250(1.3)^t$ |

**Exponents** (base $b$, exponents $m$, $n$): $b^mb^n=b^{m+n}$, $\frac{b^m}{b^n}=b^{m-n}$, $(b^m)^n=b^{mn}$, $b^0=1$, $b^{-n}=\frac1{b^n}$, $b^{m/n}=\sqrt[n]{b^m}$. **Radicals:** pull out squares ($\sqrt{75}=5\sqrt3$); rationalize ($\frac2{\sqrt3}=\frac{2\sqrt3}3$).

**Complex numbers:** $i=\sqrt{-1}$, $i^2=-1$. A **complex number** is $a+bi$, where $a$ (the real part) and $b$ (the imaginary part) are real numbers. It's **non-real** if $b\ne0$; its **conjugate** is $a-bi$. Divide by multiplying by the conjugate: $\frac{3+7i}{2-i}=\frac{(3+7i)(2+i)}{5}=\frac{-1+17i}5$.

---

# Unit 1A — Polynomial Functions

## 1.1 Change in tandem

- A **function** maps each input to exactly one output. In **function notation** $f(x)$, $f$ names the function, $x$ is the input, and $f(x)$ is the output. **Domain** = inputs, **range** = outputs. **Independent variable** = input, **dependent variable** = output. Two functions are **equal** if they share a domain and every output.
- **Image** of an input = its output; **preimage** of an output = all inputs giving it.
- Inputs and outputs vary together; a function can be given **V**erbally, **A**nalytically, **N**umerically, or **G**raphically (VANG).
- **Increasing** on an interval: for any two inputs $a<b$ in it, $f(a)<f(b)$. **Decreasing**: $a<b\Rightarrow f(a)>f(b)$. (Open vs. closed endpoints aren't tested.)
- A **zero** is an input with output 0 (an $x$-intercept). The $y$-intercept is $(0,f(0))$.

## 1.2 Rates of change

- **Average rate of change (AROC)** on the interval $[a,b]$ (from input $a$ to input $b$): $\dfrac{f(b)-f(a)}{b-a}$, outputs on top, units "output per input". Distance 76 m at 13 s and 30 m at 25 s: $\frac{-46}{12}\approx-3.833$ m/s.
- **Rate of change at a point**: estimate with the AROC over a tiny interval. $x^3$ at 1: AROC on $[1,1.001]\approx3.003$.
- **Positive** rate: both quantities move the same way. **Negative**: opposite ways.

## 1.3 Linear and quadratic rates of change; concavity

- The **secant line** through $(a,f(a))$ and $(b,f(b))$ has slope = AROC.
- **Linear**: AROC constant (constant **first differences**, the changes in outputs over equal input steps).
- **Quadratic**: AROCs over consecutive equal intervals change by a constant (constant **second differences**). $x^2$ on $[1,2],[2,3],[3,4]$: $3,5,7$.
- **Concave up**: rate of change increasing (cup). **Concave down**: decreasing (cap). **Point of inflection**: concavity switches. From a table, increasing AROCs → concave up.

| | Concave up (rate of change increasing) | Concave down (rate of change decreasing) |
|---|---|---|
| Increasing | at an increasing rate: $x^2$, $x>0$ | at a decreasing rate: $\sqrt x$ |
| Decreasing | at an increasing rate: $\frac1x$, $x>0$ | at a decreasing rate: $-x^2$, $x>0$ |

"At an increasing rate" always means concave up, whatever the direction. Concave up → secant **above** the graph; concave down → **below** (FRQ 2).

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{corg}{RGB}{230,126,34}
\begin{document}
\begin{tikzpicture}[font=\large,>=Stealth]
\draw[->] (0,0) -- (4.6,0) node[right] {$x$};
\draw[->] (0,0) -- (0,4.6) node[above] {$y$};
\draw[very thick,domain=0:4.2,samples=60] plot (\x,{0.25*\x*\x});
\draw[corg,very thick] (0.5,0.0625) -- (3.5,3.0625);
\fill[corg] (0.5,0.0625) circle (2.5pt) (3.5,3.0625) circle (2.5pt);
\node[corg] at (1.3,2.4) {secant};
\node[align=center] at (2.3,-1.1) {concave up:\\secant line above the graph};
\begin{scope}[xshift=7cm]
\draw[->] (0,0) -- (4.6,0) node[right] {$x$};
\draw[->] (0,0) -- (0,4.6) node[above] {$y$};
\draw[very thick,domain=0:4.2,samples=60] plot (\x,{4-0.25*(4-\x)*(4-\x)});
\draw[corg,very thick] (0.5,0.9375) -- (3.5,3.9375);
\fill[corg] (0.5,0.9375) circle (2.5pt) (3.5,3.9375) circle (2.5pt);
\node[corg] at (3.0,2.2) {secant};
\node[align=center] at (2.3,-1.1) {concave down:\\secant line below the graph};
\end{scope}
\end{tikzpicture}
\end{document}
```

## 1.4 Polynomial functions and rates of change

- A **polynomial function** is $p(x)=a_nx^n+\dots+a_1x+a_0$, where $n$ is a positive integer and the **coefficients** $a_n,\dots,a_0$ are real numbers with $a_n\ne0$: **degree** $n$, **leading term** $a_nx^n$, **leading coefficient** $a_n$.
- **Local (relative) max/min**: where it switches between increasing and decreasing (or an included endpoint). **Global (absolute) max/min**: largest/smallest output overall. Together these are **extrema**.
- Between two distinct real zeros there's at least one local extremum. Even degree → a global max or a global min (a quadratic's is its vertex).
- Example: $x^3-3x$ has local max 2 at $x=-1$, local min $-2$ at $x=1$, inflection at $x=0$.

## 1.5 Polynomial functions and complex zeros

- If a number $a$ (real or non-real) gives $p(a)=0$, then $a$ is a **zero** of $p$ (a **root** of $p(x)=0$). For real $a$: $(x-a)$ is a factor ⇔ $a$ is a zero.
- A factor repeated $n$ times gives a zero of **multiplicity** $n$. Degree $n$ → exactly $n$ complex zeros, counting multiplicity.
- Non-real zeros come in **conjugate pairs** $a\pm bi$ (real $a,b$, $b\ne0$), so odd degree → at least one real zero.
- Real zeros are $x$-intercepts and split the number line for inequalities: $(x+2)(x-1)^2(x-4)<0$ has signs $+,-,-,+$, so $-2<x<1$ or $1<x<4$.
- Degree = smallest $n$ with constant $n$th differences (outputs 1, 2, 9, 28, 65 → third differences 6, 6 → cubic).

| Multiplicity | Graph at the zero | Sign across it |
|---|---|---|
| 1 | crosses | changes |
| even | bounces, **tangent** to the axis | stays |
| odd ≥ 3 | flattens and crosses | changes |

```tikz
\usetikzlibrary{arrows.meta}
\begin{document}
\begin{tikzpicture}[font=\large,>=Stealth]
\foreach \s/\f/\t in {0/{\x}/{multiplicity 1:\\crosses}, 5/{\x*\x}/{multiplicity 2:\\bounces}, 10/{\x*\x*\x}/{multiplicity 3:\\flattens and crosses}} {
\begin{scope}[xshift=\s cm]
\draw[->] (-1.8,0) -- (1.8,0) node[right] {$x$};
\draw[->] (0,-1.8) -- (0,1.8);
\draw[very thick,domain=-1.2:1.2,samples=60] plot (\x,{\f});
\fill (0,0) circle (2.5pt);
\node[align=center] at (0,-2.6) {\t};
\end{scope}}
\end{tikzpicture}
\end{document}
```

| Type | Rule | Symmetry | Example |
|---|---|---|---|
| Even | $f(-x)=f(x)$ | over the $y$-axis | $x^4-2x^2+1$ |
| Odd | $f(-x)=-f(x)$ | about the origin | $x^3-x$ |

## 1.6 End behavior

**End behavior** is what a polynomial $p(x)$ does as $x\to\pm\infty$ ($x$ grows without bound in either direction), written with **limit notation**: $\lim_{x\to\infty}p(x)=\infty$. The leading term decides it.

| Degree | Leading coefficient $>0$ | Leading coefficient $<0$ |
|---|---|---|
| Even | both ends up ($x^2$) | both ends down ($-x^2$) |
| Odd | left down, right up ($x^3$) | left up, right down ($-x^3$) |

---

# Unit 1B — Rational Functions

## 1.7 Rational functions and end behavior

A **rational function** is $r(x)=\frac{p(x)}{q(x)}$ with polynomials $p,q$. End behavior comes from the quotient of leading terms:

| Degrees | End behavior | Example |
|---|---|---|
| numerator < denominator | **horizontal asymptote** $y=0$ | $\frac{3x+1}{x^2-4}$ |
| equal | horizontal asymptote $y=\frac{\text{leading coef. top}}{\text{leading coef. bottom}}$ | $\frac{6x^2-1}{2x^2+x}\to y=3$ |
| numerator one higher | **slant asymptote** = long-division quotient | $\frac{x^2+3x+5}{x-1}\to y=x+4$ |
| numerator ≥ two higher | like the polynomial quotient | $\frac{x^3+2}{x-1}$ acts like $x^2$ |

A horizontal asymptote $y=b$ (for a constant $b$, meaning $\lim_{x\to\pm\infty}r(x)=b$) describes only the ends; the graph can cross it in the middle.

## 1.8 Rational functions and zeros

- Zeros of $r$ = zeros of the numerator that are in the domain.
- Inequalities: sign chart using zeros of numerator **and** denominator. $\frac{x-2}{x+1}\ge0\Rightarrow x<-1$ or $x\ge2$.

## 1.9 Vertical asymptotes

- **Vertical asymptote** $x=a$ (a vertical line at input $a$): $a$ zeroes the denominator with higher multiplicity than in the numerator; outputs go to $\pm\infty$.
- **One-sided limits**: $x\to a^+$ from the right, $x\to a^-$ from the left. Test a nearby value: $\frac{x+2}{x-3}$ has $\lim_{x\to3^+}=\infty$, $\lim_{x\to3^-}=-\infty$.

## 1.10 Holes

A **hole** (a single missing point) is at an input $x=c$ when $c$'s multiplicity in the numerator is **at least** its multiplicity in the denominator. Cancel, then plug $c$ into the simplified form for its $y$-value: $\lim_{x\to c}r(x)$.

Example: $\frac{(x-1)(x+2)}{(x-1)(x-3)}=\frac{x+2}{x-3}$, $x\ne1$: hole $(1,-1.5)$, vertical asymptote $x=3$, horizontal asymptote $y=1$, zero $x=-2$, $y$-intercept $-\frac23$.

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\begin{document}
\begin{tikzpicture}[font=\large,>=Stealth,scale=0.55]
\draw[->] (-7.5,0) -- (9.5,0) node[right] {$x$};
\draw[->] (0,-6.5) -- (0,6.8) node[above] {$y$};
\draw[cgry,dashed,thick] (3,-6.5) -- (3,6.5);
\draw[cgry,dashed,thick] (-7.5,1) -- (9.5,1);
\node[cgry,right] at (3,6.3) {$x=3$};
\node[cgry,above] at (8,1) {$y=1$};
\draw[very thick,domain=-7.3:2.29,samples=120] plot (\x,{(\x+2)/(\x-3)});
\draw[very thick,domain=4:9.3,samples=80] plot (\x,{(\x+2)/(\x-3)});
\draw[corg,very thick,fill=white] (1,-1.5) circle (5pt);
\draw[corg,thick,->] (3.6,-3) -- (1.3,-1.7);
\node[corg,right] at (3.6,-3) {hole $(1,-1.5)$};
\fill (-2,0) circle (5pt);
\node[below left] at (-2,0) {zero};
\end{tikzpicture}
\end{document}
```

## 1.11 Equivalent representations

- **Factored form** shows zeros, asymptotes, holes, and the domain. **Standard form** shows end behavior.
- **Binomial theorem**: $(a+b)^n$ (any two terms $a$, $b$; whole-number power $n$) takes its coefficients from row $n$ of **Pascal's triangle** (1; 1 1; 1 2 1; 1 3 3 1; 1 4 6 4 1). $(x+2)^4=x^4+8x^3+24x^2+32x+16$.
- **Polynomial long division**: dividing a polynomial $f$ by a polynomial $g$ gives $f=g\cdot q+r$, with **quotient** $q$ and **remainder** $r$ (lower degree than $g$). $\frac{x^2+3x+5}{x-1}=x+4+\frac9{x-1}$; the quotient $y=x+4$ is the slant asymptote.

---

# Unit 1C — Transformations, Piecewise Functions, and Models

## 1.12 Transformations

A **parent function** is the simplest of its family ($x^2$, $\sqrt x$, $|x|$, $\frac1x$, $2^x$…). Adding a constant **translates** (slides) the graph; multiplying **dilates** (stretches) it. Below, $f$ is the original function and $k$, $h$, $a$, $b$ are constants.

| Equation | Effect on $f$ |
|---|---|
| $f(x)+k$ | up $k$ |
| $f(x+h)$ | **left** $h$ (opposite of the sign) |
| $a\,f(x)$ | vertical dilation by $\lvert a\rvert$; $a<0$ reflects over the $x$-axis |
| $f(bx)$ | horizontal dilation by $\frac1{\lvert b\rvert}$; $b<0$ reflects over the $y$-axis |

$y=a\,f(b(x-h))+k$ sends each point $(x,y)$ on the graph of $f$ to $\left(\frac xb+h,\ ay+k\right)$: the **preimage** point maps to its **image**. Example: $-2f(x+3)+1$ sends $(1,4)$ to $(-2,-7)$. Domain and range can change.

## Piecewise functions (between 1.12 and 1.13)

A **piecewise-defined function** uses different formulas on non-overlapping intervals: $p(x)=\begin{cases}4-x,&x\le1\\\frac{4x}{x+1},&x>1\end{cases}$ gives $p(1)=3$, $p(3)=3$.

- Closed dot for $\le,\ge$; open dot for $<,>$.
- $|2x-3|=-2x+3$ for $x<1.5$ and $2x-3$ for $x\ge1.5$.
- Find domain and range piece by piece: $\begin{cases}x+4,&x<-3\\(x+2)^2-2,&-3\le x<0\\3,&x\ge2\end{cases}$ has domain $x<0$ or $x\ge2$ and range $y<2$ or $y=3$.

## 1.13 Model selection and assumptions

| Model | Use when | Example |
|---|---|---|
| Linear | constant rate of change | taxi fare per mile |
| Quadratic | linear rate of change; one max/min; area | thrown ball |
| Cubic | volume; constant third differences | open box |
| Degree $n$ | $n+1$ points fit exactly; several zeros or extrema | 4 points → cubic |
| Piecewise | different behavior on different intervals | accelerate, cruise, brake |
| Rational | inverse proportion | gravity $\frac k{d^2}$ ($d$ = distance, $k$ = a constant) |

Models carry **assumptions** (what stays constant) and need **domain/range restrictions** from context (time ≥ 0, whole people). FRQ 2 Part C asks for these.

## 1.14 Model construction and application

Build from context (cut $x$-inch squares from the corners of a 20 × 30 inch sheet and fold up the sides: the box's volume is $V(x)=x(20-2x)(30-2x)$, $0<x<10$), from transformations of a parent, from **regression** (linear, quadratic, cubic, quartic on a calculator; round to 3 decimals at the end), or by combining pieces. Use the model to predict values and AROCs, with units.

---

# Unit 2A — Sequences and Exponential Functions

## 2.1–2.2 Sequences; linear vs. exponential

A **sequence** is a function on whole numbers $n=0,1,2,\dots$; its outputs are **terms**, and its graph is dots.

Variables below:
- $n$ is the term number, $a_n$ (arithmetic) or $g_n$ (geometric) is the $n$th term, and $a_0$, $g_0$ are the starting terms.
- $k$ is the number of any term you already know, so $a_k$ or $g_k$ is that known term.
- For functions, $(x_i,y_i)$ is any known point. In the linear form, $b$ is the starting value (the $y$-intercept). In the exponential form, $a$ is the starting value and $b$ is the base.

| | Arithmetic / linear | Geometric / exponential |
|---|---|---|
| Step | add a **common difference** $d$ (slope $m$) | multiply by a **common ratio** $r$ (base $b$) |
| Sequence | $a_n=a_0+dn=a_k+d(n-k)$ | $g_n=g_0r^n=g_kr^{n-k}$ |
| Function | $f(x)=b+mx=y_i+m(x-x_i)$ | $f(x)=ab^x=y_ib^{x-x_i}$ |
| Equal input steps | outputs change by a constant amount | outputs change by a constant factor (**proportional**) |

- Two points determine either type. $g_2=12$, $g_5=96$: $r^3=8$, $r=2$, $g_n=12\cdot2^{n-2}$.
- Increasing arithmetic grows by equal amounts; increasing geometric grows by bigger amounts each step.

## 2.3 Exponential functions

$f(x)=ab^x$: **initial value** $a=f(0)\ne0$, **base** $b>0$, $b\ne1$. **Growth** if $a>0,b>1$; **decay** if $a>0,0<b<1$.

- Domain all reals; always increasing or decreasing; one concavity; no extrema or inflection points.
- Horizontal asymptote $y=0$ ($\lim_{x\to-\infty}2^x=0$). Adding a constant $k$, as in $ab^x+k$, moves it to $y=k$; subtract $k$ from data to reveal proportional outputs.

## 2.4 Exponential manipulation

Base $b>0$; $k$ and $c$ are constants.

| Rule | Meaning | Example |
|---|---|---|
| $b^{x+k}=b^k\cdot b^x$ | horizontal shift = vertical dilation | $2^{x+3}=8\cdot2^x$ |
| $b^{cx}=(b^c)^x$ | horizontal dilation = new base | $3^{2x+1}=3\cdot9^x$ |
| $b^{-x}=(\frac1b)^x$ | reflection swaps growth and decay | $2^{-x}=0.5^x$ |
| $b^{1/k}=\sqrt[k]b$ | fractional exponent = root | $8^{1/3}=2$ |

## 2.5 Exponential modeling

- Growth factor $b=1+r$ ($r$ = percent change per unit of input, as a decimal); decay $b=1-r$.
- Rewrite to change units: with $d$ in days, $2^d=128^{d/7}$ (×2 daily = ×128 weekly); yearly 1.06 = monthly $1.06^{1/12}\approx1.00487$.
- Half-life (the time $h$ for the amount to halve): $A_0(\frac12)^{t/h}$, with starting amount $A_0$ and time $t$.
- Build from an initial value and ratio, two points, transformations, or **exponential regression**. The **natural base** $e\approx2.718$ is common in models.

## 2.6 Competing models

- **Residual** = actual − predicted. Positive → model **underestimates**.
- **Residual plot** (residuals vs. input): no pattern → appropriate model; a curve → wrong model type.
- Context decides whether over- or underestimating is safer.

## 2.7A Composition

For two functions $f$ and $g$, the **composition** $(f\circ g)(x)=f(g(x))$ applies $g$, then $f$.

- Domain: $x$ in $g$'s domain with $g(x)$ in $f$'s domain ($\sqrt{x-5}$ needs $x\ge5$).
- Not commutative: $f(x)=x^2$, $g(x)=x+3$ give $(x+3)^2$ vs. $x^2+3$.
- From tables: find $g(2)$, then look up $f$ of that.
- The **identity function** $I(x)=x$ leaves any function unchanged under composition.

---

# Unit 2B — Inverses and Logarithmic Functions

(Taught after 2.15 in class; placed here because logs are defined as inverses.)

## 2.7B Decomposition

Write a function as $f(g(x))$: $\sqrt{3x+1}$ has $f=\sqrt x$, $g=3x+1$. Adding or multiplying **inside** $f$ acts horizontally; **outside** acts vertically.

## 2.8 Inverse functions

- **Invertible** on a domain if each output comes from exactly one input (**one-to-one**).
- The **inverse** $f^{-1}$ reverses every input-output pair: if $f$ sends input $a$ to output $b$, then $f^{-1}$ sends $b$ back to $a$ ($f(a)=b\iff f^{-1}(b)=a$). $f(f^{-1}(x))=f^{-1}(f(x))=x$; domain and range swap; the graph reflects over $y=x$.
- To find it, swap $x$ and $y$ and solve: $f(x)=\frac{2x-1}3\Rightarrow f^{-1}(x)=\frac{3x+1}2$.
- Restrict the domain to make a function invertible ($x^2$ on $x\ge0$ → $\sqrt x$). $f^{-1}\ne\frac1f$.
- FRQ 1: justify "not invertible" with a repeated output ("$f(3)=f(5)=2$"), not the horizontal line test.

## 2.9 Logarithmic expressions

A **logarithm** gives an exponent: $\log_bc$ is the power you raise the **base** $b$ to in order to get $c$.

$$\log_bc=a\iff b^a=c\qquad(b>0,\ b\ne1,\ c>0)$$

$\log x$ is base 10 (**common log**); $\ln x$ is base $e$ (**natural log**). Examples: $\log_28=3$, $\log_3\frac19=-2$, $\log_b1=0$, $\log_bb=1$. Estimate by bracketing: $\log_210$ is between 3 and 4. On a **logarithmic scale** each step multiplies by the base ($10^0,10^1,10^2,\dots$).

## 2.10–2.11 Logarithmic functions

A **logarithmic function** is $f(x)=a\log_bx$ (constant $a\ne0$, base $b$). $\log_bx$ is the inverse of $b^x$: if a point $(s,t)$ is on $y=b^x$, then $(t,s)$ is on $y=\log_bx$. Exponential: outputs multiply as inputs add. Logarithmic: outputs add as inputs multiply.

| Feature | $b^x$ ($b>1$) | $\log_bx$ ($b>1$) |
|---|---|---|
| Domain | all reals | $x>0$ |
| Range | $y>0$ | all reals |
| Asymptote | $y=0$ | $x=0$ ($\lim_{x\to0^+}=-\infty$) |
| Key point | $(0,1)$ | $(1,0)$ |
| Shape | increasing, concave up | increasing, concave down |

Logs, like exponentials, have no extrema and no inflection points. Shifting by a constant $k$, $\log_b(x+k)$ has its asymptote at $x=-k$.

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\begin{document}
\begin{tikzpicture}[font=\large,>=Stealth,scale=0.8]
\draw[->] (-3.5,0) -- (6.8,0) node[right] {$x$};
\draw[->] (0,-3.5) -- (0,6.8) node[above] {$y$};
\draw[cgry,dashed,thick] (-3.3,-3.3) -- (6.5,6.5) node[above right] {$y=x$};
\draw[very thick,domain=-3.3:2.65,samples=80] plot (\x,{2^\x});
\draw[corg,very thick,domain=0.1:6.5,samples=120] plot (\x,{ln(\x)/ln(2)});
\node at (1.4,5.6) {$y=2^x$};
\node[corg] at (5.8,1.9) {$y=\log_2x$};
\fill (1,2) circle (3pt) node[left] {$(1,2)$};
\fill[corg] (2,1) circle (3pt) node[below right] {$(2,1)$};
\fill (0,1) circle (3pt) node[left] {$(0,1)$};
\fill[corg] (1,0) circle (3pt) node[below right] {$(1,0)$};
\end{tikzpicture}
\end{document}
```

## 2.12 Log properties

For positive $x$ and $y$, any real power $n$, and bases $b$ (positive, not 1):

| Property | Rule | Graph meaning |
|---|---|---|
| Product | $\log_b(xy)=\log_bx+\log_by$ | horizontal dilation = vertical shift |
| Quotient | $\log_b\frac xy=\log_bx-\log_by$ | dividing the input shifts the graph down |
| Power | $\log_bx^n=n\log_bx$ | vertical dilation |
| Change of base | $\log_bx=\frac{\ln x}{\ln b}$ | all logs are dilations of each other |
| Inverse | $\log_bb^x=x$, $b^{\log_bx}=x$ | they undo each other |

Expand: $\log_2\frac{8x^3}y=3+3\log_2x-\log_2y$. Never: $\log(x+y)=\log x+\log y$.

## 2.13 Exponential and log equations

| Method | Example |
|---|---|
| Match bases | $2^{x+1}=8^x=2^{3x}\Rightarrow x=\frac12$ |
| Take a log | $5^x=20\Rightarrow x=\frac{\ln20}{\ln5}$ |
| Isolate the log, exponentiate | $3\log_2(x-1)+4=10\Rightarrow x=5$ |
| Condense logs | $\log_2x+\log_2(x-2)=3\Rightarrow x=4$ |
| Quadratic in $e^x$ | $e^{2x}-5e^x+6=0\Rightarrow x=\ln2,\ln3$ |

- **Extraneous solutions**: reject answers that make a log argument $\le0$ (above, $x=-2$).
- Inequalities: a base below 1 flips the sign ($(\frac12)^x>4\Rightarrow x<-2$).
- $b^x=e^{x\ln b}$.
- Inverses: undo steps in reverse. $3\cdot2^{x-1}+4\to1+\log_2\frac{x-4}3$; $2\ln(x+3)-1\to e^{(x+1)/2}-3$.

## 2.14 Log modeling

Use a log model when inputs multiply while outputs add (inputs 1, 3, 9, 27 → outputs 2, 5, 8, 11). Build from two points or **logarithmic regression** (LnReg fits $y=a+b\ln x$ and reports the constants $a$ and $b$). Through $(1,5)$ and $(e^2,11)$: $f(x)=3\ln x+5$.

## 2.15 Semi-log plots

A **semi-log plot** has a log-scaled $y$-axis; exponential data look **linear**. Taking $\log$ (base 10) of $y=ab^x$ gives $\log y=(\log b)x+\log a$: a line with slope $\log b$ and intercept $\log a$. A line $\log y=0.3x+1$ means $y=10(10^{0.3})^x$.

---

# Unit 3A — Trigonometry, Sine, and Cosine

## 3.0 Right-triangle review 🔒

In a right triangle with acute angle $\theta$: $\sin\theta=\frac{\text{opposite}}{\text{hypotenuse}}$, $\cos\theta=\frac{\text{adjacent}}{\text{hypotenuse}}$, $\tan\theta=\frac{\text{opposite}}{\text{adjacent}}$ (SOH CAH TOA). Special triangles: 45-45-90 is $1:1:\sqrt2$; 30-60-90 is $1:\sqrt3:2$ (short leg opposite 30°).

## 3.1 Periodic phenomena

A relationship is **periodic** if its outputs repeat over equal input intervals. The **period** is the smallest positive number $k$ with $f(x+k)=f(x)$ for every input $x$; one period of graph is a **cycle**. Estimate it as the time between consecutive maxima.

## 3.2 Sine, cosine, tangent

- **Standard position**: vertex at the origin, **initial ray** on the positive $x$-axis; the other ray is the **terminal ray**. Counterclockwise is positive. **Coterminal** angles differ by $2\pi k$ for some integer $k$ (whole turns).
- **Radians**: $\theta=\frac sr$, where $s$ is the length of the arc the angle cuts off and $r$ is the circle's radius. $2\pi$ = full turn; degrees × $\frac\pi{180}$. On the **unit circle** (radius 1), $\theta=s$.
- Let $P=(x,y)$ be a point on the terminal ray and $r$ its distance from the origin: $\sin\theta=\frac yr$, $\cos\theta=\frac xr$, $\tan\theta=\frac yx=\frac{\sin\theta}{\cos\theta}$ (the terminal ray's slope).

## 3.3 Sine and cosine values

On a circle of radius $r$, $P=(r\cos\theta,r\sin\theta)$.

| $\theta$ | $0$ | $\frac\pi6$ | $\frac\pi4$ | $\frac\pi3$ | $\frac\pi2$ |
|---|---|---|---|---|---|
| $\sin$ | $0$ | $\frac12$ | $\frac{\sqrt2}2$ | $\frac{\sqrt3}2$ | $1$ |
| $\cos$ | $1$ | $\frac{\sqrt3}2$ | $\frac{\sqrt2}2$ | $\frac12$ | $0$ |
| $\tan$ | $0$ | $\frac{\sqrt3}3$ | $1$ | $\sqrt3$ | undefined |

Other angles: the **reference angle** (to the $x$-axis) gives the size and the quadrant gives the sign ("All Students Take Calculus"). $\sin\frac{7\pi}6=-\frac12$; $\tan\frac{2\pi}3=-\sqrt3$.

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\begin{document}
\begin{tikzpicture}[>=Stealth]
\draw (-3.25,0) -- (3.25,0);
\draw (0,-3.25) -- (0,3.25);
\draw[very thick] (0,0) circle (3);
\foreach \a/\t in {0/0, 30/\frac{\pi}{6}, 45/\frac{\pi}{4}, 60/\frac{\pi}{3}, 90/\frac{\pi}{2}, 120/\frac{2\pi}{3}, 135/\frac{3\pi}{4}, 150/\frac{5\pi}{6}, 180/\pi, 210/\frac{7\pi}{6}, 225/\frac{5\pi}{4}, 240/\frac{4\pi}{3}, 270/\frac{3\pi}{2}, 300/\frac{5\pi}{3}, 315/\frac{7\pi}{4}, 330/\frac{11\pi}{6}} {
\draw[cgry] (0,0) -- (\a:3);
\fill (\a:3) circle (2pt);
\node at (\a:3.65) {$\t$};}
\node[corg,font=\large] at (45:1.9) {All};
\node[corg,font=\large] at (135:1.9) {Sin};
\node[corg,font=\large] at (225:1.9) {Tan};
\node[corg,font=\large] at (315:1.9) {Cos};
\end{tikzpicture}
\end{document}
```

## 3.4 Sine and cosine graphs

$\sin\theta$ tracks $P$'s $y$-coordinate and $\cos\theta$ its $x$-coordinate. Domain all reals, range $[-1,1]$.

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{corg}{RGB}{230,126,34}
\begin{document}
\begin{tikzpicture}[font=\large,>=Stealth,yscale=1.4]
\draw[->] (-0.3,0) -- (7,0) node[right] {$\theta$};
\draw[->] (0,-1.5) -- (0,1.6);
\foreach \x/\t in {1.5708/\frac{\pi}{2}, 3.1416/\pi, 4.7124/\frac{3\pi}{2}, 6.2832/2\pi} {\draw (\x,0.06) -- (\x,-0.06); \node at (\x,-1.35) {$\t$};}
\draw (0.08,1) -- (-0.08,1) node[left] {$1$};
\draw (0.08,-1) -- (-0.08,-1) node[left] {$-1$};
\draw[very thick,domain=0:6.2832,samples=100] plot (\x,{sin(\x r)});
\draw[corg,very thick,dashed,domain=0:6.2832,samples=100] plot (\x,{cos(\x r)});
\node at (2.1,1.25) {$\sin\theta$};
\node[corg] at (6.6,1.2) {$\cos\theta$};
\end{tikzpicture}
\end{document}
```

## 3.5 Sinusoidal functions

A **sinusoidal function** is a transformation of $\sin\theta$; $\cos\theta=\sin(\theta+\frac\pi2)$.

- **Frequency** = $\frac1{\text{period}}$. **Amplitude** = $\frac{\max-\min}2$. **Midline** $y=\frac{\max+\min}2$.
- Concave down above the midline, concave up below; inflection points on the midline.
- Sine is odd; cosine is even.

## 3.6 Sinusoidal transformations

$f(\theta)=a\sin(b(\theta+c))+d$, with constants $a$, $b$, $c$, $d$ (same for cosine):

| Parameter | Effect | In $3\sin(2(\theta-\frac\pi4))+1$ |
|---|---|---|
| $a$ | amplitude $\lvert a\rvert$; negative reflects | 3 |
| $b$ | period $\frac{2\pi}{\lvert b\rvert}$ | $\pi$ |
| $c$ | **phase shift** $-c$ | right $\frac\pi4$ |
| $d$ | midline $y=d$ | $y=1$ |

Factor $b$ out first: $\sin(2\theta-\frac\pi2)$ shifts right $\frac\pi4$, not $\frac\pi2$. Sketch with five key points spaced $\frac{\text{period}}4$ apart.

## 3.7 Sinusoidal modeling

Period from consecutive maxima → $b=\frac{2\pi}{\text{period}}$; amplitude and $d$ from max and min; phase shift from a known point (cosine starts at a max, $-\cos$ at a min, sine on the midline going up). Or use sinusoidal regression.

Ferris wheel (center 25 m, radius 20 m, 8 min per turn, starts at the bottom): the rider's height in meters after $t$ minutes is $h(t)=-20\cos(\frac\pi4t)+25$. FRQ 3 labels the points as below: F$(4,45)$, G$(6,25)$, J$(8,5)$, K$(10,25)$, P$(12,45)$.

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{corg}{RGB}{230,126,34}
\definecolor{cgry}{RGB}{140,140,140}
\begin{document}
\begin{tikzpicture}[font=\large,>=Stealth]
\draw[->] (0,0) -- (10.4,0) node[right] {$t$ (min)};
\draw[->] (0,0) -- (0,5.2) node[above] {$h$ (m)};
\foreach \t in {2,4,...,16} {\draw (0.6*\t,0.06) -- (0.6*\t,-0.06) node[below] {$\t$};}
\foreach \h in {5,25,45} {\draw (0.06,0.1*\h) -- (-0.06,0.1*\h) node[left] {$\h$};}
\draw[cgry,dashed,thick] (0,2.5) -- (9.9,2.5) node[right] {midline};
\draw[very thick,domain=0:16,samples=150] plot ({0.6*\x},{0.1*(-20*cos(45*\x)+25)});
\foreach \n/\t/\h/\p in {F/4/45/above, G/6/25/above right, J/8/5/below, K/10/25/above left, P/12/45/above} {
\fill[corg] (0.6*\t,0.1*\h) circle (3pt) node[\p,corg] {$\n$};}
\end{tikzpicture}
\end{document}
```

| Interval | Concavity | Rate of change |
|---|---|---|
| F to G, K to P | concave down | decreasing |
| G to J, J to K | concave up | increasing |

---

# Unit 3B — Tangent, Inverse Trig, Identities, and Polar

## 3.8 Tangent 🔒

$\tan\theta=\frac{\sin\theta}{\cos\theta}$: period $\pi$, vertical asymptotes at $\frac\pi2+k\pi$, zeros at $k\pi$ ($k$ any integer). It increases between asymptotes (concave down, then up; inflection at the zero). For $a\tan(b(\theta+c))+d$ (constants $a$, $b$, $c$, $d$): vertical dilation $\lvert a\rvert$ (no amplitude), period $\frac\pi{\lvert b\rvert}$, shift $-c$, and $d$ moves the inflection points.

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{cgry}{RGB}{140,140,140}
\begin{document}
\begin{tikzpicture}[font=\large,>=Stealth,scale=0.9]
\draw[->] (-5.3,0) -- (5.6,0) node[right] {$\theta$};
\draw[->] (0,-3.3) -- (0,3.5) node[above] {$y$};
\foreach \x/\t in {-4.7124/-\frac{3\pi}{2}, -1.5708/-\frac{\pi}{2}, 1.5708/\frac{\pi}{2}, 4.7124/\frac{3\pi}{2}} {\draw[cgry,dashed,thick] (\x,-3.2) -- (\x,3.2); \node[cgry,below right] at (\x,-0.05) {$\t$};}
\foreach \x/\t in {-3.1416/-\pi, 3.1416/\pi} {\node[below right] at (\x,-0.05) {$\t$};}
\foreach \c in {-3.1416,0,3.1416} {\draw[very thick,domain=\c-1.249:\c+1.249,samples=80] plot (\x,{tan((\x-\c) r)});}
\node at (2.3,2.8) {$y=\tan\theta$};
\end{tikzpicture}
\end{document}
```

## 3.9 Inverse trig 🔒

Trig functions are invertible only on restricted domains. The inverses take a ratio and return an angle.

| Inverse | Input | Output | Example |
|---|---|---|---|
| $\arcsin x=\sin^{-1}x$ | $[-1,1]$ | $[-\frac\pi2,\frac\pi2]$ | $\arcsin(-\frac12)=-\frac\pi6$ |
| $\arccos x=\cos^{-1}x$ | $[-1,1]$ | $[0,\pi]$ | $\arccos(-\frac12)=\frac{2\pi}3$ |
| $\arctan x=\tan^{-1}x$ | all reals | $(-\frac\pi2,\frac\pi2)$ | $\arctan(-\sqrt3)=-\frac\pi3$ |

$\sin^{-1}x\ne\frac1{\sin x}$. Outputs must land in the range: $\arcsin(\sin\frac{5\pi}6)=\frac\pi6$. Use a triangle for mixes: $\sin(\arccos\frac35)=\frac45$.

## 3.10 Trig equations and inequalities 🔒

Isolate the trig function, find every solution in $[0,2\pi)$ (usually two quadrants), then add $2\pi k$ (sine, cosine) or $\pi k$ (tangent), where $k$ is any integer.

| Equation | Solutions in $[0,2\pi)$ |
|---|---|
| $2\sin\theta-1=0$ | $\frac\pi6,\frac{5\pi}6$ |
| $\cos2\theta=0$ ($2\theta$ goes around twice) | $\frac\pi4,\frac{3\pi}4,\frac{5\pi}4,\frac{7\pi}4$ |
| $\cos\theta(2\cos\theta-1)=0$ | $\frac\pi2,\frac{3\pi}2,\frac\pi3,\frac{5\pi}3$ |
| $\sin\theta=0.3$ (calculator) | $0.305,\ \pi-0.305\approx2.837$ |

Inequalities: solve the equation, then read intervals from the circle ($\sin\theta\ge\frac12$: $\frac\pi6\le\theta\le\frac{5\pi}6$).

## 3.11 Secant, cosecant, cotangent 🔒

| Function | Definition | Asymptotes | Period | Range |
|---|---|---|---|---|
| $\sec\theta$ | $\frac1{\cos\theta}$ | $\cos\theta=0$ | $2\pi$ | $\lvert y\rvert\ge1$ |
| $\csc\theta$ | $\frac1{\sin\theta}$ | $\sin\theta=0$ | $2\pi$ | $\lvert y\rvert\ge1$ |
| $\cot\theta$ | $\frac{\cos\theta}{\sin\theta}$ | $\sin\theta=0$ | $\pi$ | all reals (decreasing) |

## 3.12 Identities 🔒

An **identity** holds for every input where both sides are defined. $\alpha$ and $\beta$ are any two angles.

| Identity | Formula |
|---|---|
| Pythagorean | $\sin^2\theta+\cos^2\theta=1$; $\tan^2\theta+1=\sec^2\theta$; $1+\cot^2\theta=\csc^2\theta$ |
| Sum/difference | $\sin(\alpha\pm\beta)=\sin\alpha\cos\beta\pm\cos\alpha\sin\beta$; $\cos(\alpha\pm\beta)=\cos\alpha\cos\beta\mp\sin\alpha\sin\beta$ |
| Double angle | $\sin2\theta=2\sin\theta\cos\theta$; $\cos2\theta=\cos^2\theta-\sin^2\theta=2\cos^2\theta-1=1-2\sin^2\theta$ |
| Even/odd | $\cos(-\theta)=\cos\theta$; $\sin(-\theta)=-\sin\theta$ |

- Exact value: $\sin\frac\pi{12}=\sin(\frac\pi3-\frac\pi4)=\frac{\sqrt6-\sqrt2}4$.
- Verify: $\sec\theta-\cos\theta=\frac{1-\cos^2\theta}{\cos\theta}=\sin\theta\tan\theta$.
- Solve: $\cos2\theta=\sin\theta\Rightarrow(2\sin\theta-1)(\sin\theta+1)=0\Rightarrow\theta=\frac\pi6,\frac{5\pi}6,\frac{3\pi}2$.

## 3.13 Polar coordinates 🔒

The **polar coordinate system** uses circles around the **pole** (origin) and rays from it; the **polar axis** is the positive $x$-axis. A point $(r,\theta)$ is at angle $\theta$ and signed distance $r$; negative $r$ points the opposite way, so $(2,\frac\pi6)=(-2,\frac{7\pi}6)$.

- Polar → rectangular: $x=r\cos\theta$, $y=r\sin\theta$. $(4,\frac{2\pi}3)\to(-2,2\sqrt3)$.
- Rectangular → polar: $r=\sqrt{x^2+y^2}$, $\theta=\arctan\frac yx$ (add $\pi$ if $x<0$). $(-3,3)\to(3\sqrt2,\frac{3\pi}4)$.
- Complex plane: $a+bi$ is the point $(a,b)$; with that point's polar coordinates $(r,\theta)$, it's $r\cos\theta+ir\sin\theta$.

## 3.14 Polar graphs 🔒

A **polar function** $r=f(\theta)$ takes an angle and gives a radius. Plot from a table of $\theta$ values; restricting $\theta$ draws part of the curve.

Below, $a$ and $b$ are positive constants and $n$ is a positive integer.

| Curve | Equation | Tell |
|---|---|---|
| Circle | $r=a$; $r=a\cos\theta$ or $a\sin\theta$ | around the pole; through the pole |
| Rose | $r=a\cos n\theta$ or $a\sin n\theta$ | $n$ petals if $n$ odd, $2n$ if even |
| Cardioid | $r=a\pm a\cos\theta$ | touches the pole once |
| Limaçon, inner loop | $r=a\pm b\cos\theta$, $a<b$ | passes the pole twice |
| Limaçon, dimpled/convex | $a>b$ | dimpled if $a<2b$, convex if $a\ge2b$ |
| Spiral | $r=\theta$ | grows each turn |

```tikz
\usetikzlibrary{arrows.meta}
\definecolor{corg}{RGB}{230,126,34}
\begin{document}
\begin{tikzpicture}[font=\large,>=Stealth]
\draw[->] (-2.6,0) -- (2.7,0);
\draw[->] (0,-2.4) -- (0,2.5);
\draw[very thick,domain=0:180,samples=200] plot ({2*cos(3*\x)*cos(\x)},{2*cos(3*\x)*sin(\x)});
\node at (0,-3) {rose $r=2\cos3\theta$};
\begin{scope}[xshift=7cm]
\draw[->] (-2,0) -- (3.6,0);
\draw[->] (0,-2.4) -- (0,2.5);
\draw[corg,very thick,domain=0:360,samples=200] plot ({(1+2*cos(\x))*cos(\x)},{(1+2*cos(\x))*sin(\x)});
\node at (0.8,-3) {lima\c{c}on $r=1+2\cos\theta$};
\end{scope}
\end{tikzpicture}
\end{document}
```

## 3.15 Polar rates of change 🔒

Distance from the pole is $\lvert r\rvert$:

| | $r$ increasing | $r$ decreasing |
|---|---|---|
| $r>0$ | away from the pole | toward the pole |
| $r<0$ | toward the pole | away from the pole |

Where $r$ switches direction, the point is relatively closest to or farthest from the pole. AROC of $r$ = $\frac{\Delta r}{\Delta\theta}$ ($\Delta$ means "change in"; radius per radian): $r=1+2\cos\theta$ on $[0,\frac\pi2]$ gives $-\frac4\pi$.

---

# Unit 4 — Matrices

🔒 Taught after the AP exam; **not on the AP exam**.

Notation: capital letters ($A$, $B$, $T$, $X$) are matrices. A $2\times2$ matrix is written $\begin{bmatrix}a&b\\c&d\end{bmatrix}$. A **vector** $\vec v=\langle x,y\rangle$ is a quantity with two components, written as a column; $\vec0=\langle0,0\rangle$.

| Topic | Key facts | Example |
|---|---|---|
| 4.10 **Matrix** | a grid of numbers; $n\times m$ = $n$ rows × $m$ columns. $AB$ needs columns of $A$ = rows of $B$; entry = **dot product** of row and column (multiply matching entries, add). Usually $AB\ne BA$ | $\begin{bmatrix}1&2\\3&4\end{bmatrix}\begin{bmatrix}5\\6\end{bmatrix}=\begin{bmatrix}17\\39\end{bmatrix}$ |
| 4.11 **Identity, determinant, inverse** | $I$ has 1s on the diagonal. $\det=ad-bc$. $A^{-1}=\frac1{ad-bc}\begin{bmatrix}d&-b\\-c&a\end{bmatrix}$, exists iff $\det\ne0$. $\lvert\det\rvert$ = parallelogram area | $\begin{bmatrix}2&1\\5&3\end{bmatrix}^{-1}=\begin{bmatrix}3&-1\\-5&2\end{bmatrix}$ |
| Systems | $AX=B$ ($A$ = coefficients, $X$ = unknowns, $B$ = constants) $\Rightarrow X=A^{-1}B$ | $2x+y=4$, $5x+3y=11$ → $(1,2)$ |
| 4.12 **Linear transformation** | a function $L$ from vectors to vectors with $L(\vec v)=A\vec v$ for a matrix $A$; outputs are sums of constant multiples of inputs; sends $\vec0$ to $\vec0$ | many vectors at once: put them in columns |
| 4.13 Matrices as functions | columns = images of $\langle1,0\rangle,\langle0,1\rangle$; rotation $\begin{bmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{bmatrix}$; $\lvert\det\rvert$ = area scale; $B$ then $A$ = $AB$; inverse uses $A^{-1}$ | 90°: $\langle3,1\rangle\to\langle-1,3\rangle$ |
| 4.14 **Transition matrix** | $T$ holds the rates of moving between states, with columns = "from" states; the **state vector** $\vec x$ holds the current counts. Next $=T\vec x$, past $=T^{-1}\vec x$, steady state $T\vec x=\vec x$ | $T=\begin{bmatrix}0.8&0.1\\0.2&0.9\end{bmatrix}$: $\begin{bmatrix}300\\0\end{bmatrix}\to\begin{bmatrix}240\\60\end{bmatrix}$; steady 100/200 |

---

# Exam Strategy — The Four FRQs

From the class's FRQ guides. Always: radian mode, store values and round to 3 decimals only at the end, and write only true equations.

| FRQ | Calculator | Content | Parts |
|---|---|---|---|
| 1 Function concepts | yes | Units 1–2; one function as a table/graph, one as an equation | A: composition (show work), inverse/table values. B: solve (no work needed), end behavior in limit notation. C: a justified claim |
| 2 Non-periodic modeling | yes | Units 1–2 word problem | A: plug data into the model, solve for parameters. B (3 pts): AROC with work, secant estimate with units, concavity comparison. C: a model limitation |
| 3 Periodic modeling | no | sinusoid in context | A: F, G, J, K, P coordinates. B: $a,b,c,d$. C: behavior + concavity on an interval |
| 4 Symbolic | no | exp, log, trig, inverse trig | A/B: one "solve", one "rewrite", full work. C: hardest; unit circle, identities, general solutions |

**FRQ 1 justifications:**

| Claim | Reason |
|---|---|
| Linear | outputs change by a constant over equal-length input intervals |
| Quadratic | second differences constant over equal-length input intervals |
| Exponential | outputs proportional: ×[factor] as inputs +[step] |
| Logarithmic | inputs ×[factor] as outputs +[step] |
| Invertible | no repeated outputs; each output from a unique input |
| Not invertible | cite a repeat: "$f(3)=f(5)=2$" |

**FRQ 2 concavity script:** "Because $f$ is concave down on $2<t<6$, the secant line is below the graph there, so AROC estimates are less than the model on $2<t<6$" (greater for $t>6$). Concave up flips both.

**FRQ 3 method:**
- $y$-values: F and P are maxima, J is the minimum, G and K are on the midline.
- $t$-values: put the start at $t=0$ (extend left if it starts at a min), then step by $\frac{\text{period}}4$.
- For $h(t)=a\sin(b(t+c))+d$ or $a\cos(b(t+c))+d$, find $b$ and $d$ first. Sine must start on the midline, cosine at a max or min. $a<0$ if you start at G (sine) or J (cosine). $c$ = −(starting $t$).
- Part C script: "The graph is concave up, and the rates of change are increasing over this interval."
