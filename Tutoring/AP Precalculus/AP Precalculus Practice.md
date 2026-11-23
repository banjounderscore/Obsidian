# AP Precalculus Practice

> [!abstract] How to use this
> Questions are grouped by unit, then by topic, in AP multiple-choice style, with FRQ-style short-answer problems at the end. **Answers are folded**: pick your answer first, then click the "Answer" bar. Each answer says why, so a wrong pick tells you what to review.
>
> All questions are original (the class's practice exam is locked on the Drive). *(calculator)* marks questions meant for a graphing calculator; the rest should be done by hand.
>
> Theory: [[AP Precalculus Notes]] · Quick version: [[AP Precalculus Review]]

## Contents
- [[#Unit 0 — Prerequisite Skills]]
- [[#Unit 1A — Polynomial Functions]]
- [[#Unit 1B — Rational Functions]]
- [[#Unit 1C — Transformations, Piecewise Functions, and Models]]
- [[#Unit 2A — Sequences and Exponential Functions]]
- [[#Unit 2B — Inverses and Logarithmic Functions]]
- [[#Unit 3A — Trigonometry, Sine, and Cosine]]
- [[#Unit 3B — Tangent, Inverse Trig, Identities, and Polar]]
- [[#Unit 4 — Matrices]]
- [[#Mixed and Short-Answer]]

---

# Unit 0 — Prerequisite Skills

**0.1** Which is an equation of the line through $(-2,5)$ and $(3,8)$?
- A. $3x-5y=-31$
- B. $5x-3y=-25$
- C. $3x+5y=19$
- D. $5x+3y=5$

> [!success]- Answer
> **A.** The slope is $\frac35$, so $y-5=\frac35(x+2)$; multiplying by 5 and rearranging gives $3x-5y=-31$. Check: $3(3)-5(8)=-31$. B and D flip the slope's numbers; C has slope $-\frac35$.

**0.2** Solve $3x^2-17x+10>0$.
- A. $\frac23<x<5$
- B. $x<\frac23$ or $x>5$
- C. $x>5$ only
- D. $-5<x<-\frac23$

> [!success]- Answer
> **B.** $(3x-2)(x-5)>0$ is positive outside the zeros $\frac23$ and 5. A is where it's negative; C misses the left piece; D uses the wrong signs on the zeros.

**0.3** Simplify $\dfrac{3+7i}{2-i}$.
- A. $\dfrac{13+11i}{5}$
- B. $\dfrac{-1+17i}{3}$
- C. $\dfrac{-1+17i}{5}$
- D. $3+7i$

> [!success]- Answer
> **C.** Multiply by the conjugate $\frac{2+i}{2+i}$: numerator $6+3i+14i+7i^2=-1+17i$, denominator $4-i^2=5$. B forgets that $-i^2=+1$ in the denominator (it's 5, not 3).

**0.4** How many solutions does $2x^2+3x+5=0$ have, and of what kind?
- A. two distinct real solutions
- B. one repeated real solution
- C. no solutions of any kind
- D. two non-real solutions

> [!success]- Answer
> **D.** The discriminant is $9-40=-31<0$, so there are two non-real (complex conjugate) solutions. C is wrong because every quadratic has two complex solutions.

---

# Unit 1A — Polynomial Functions

## Change in tandem

**1.1** $P(t)$ gives a town's population $t$ years after 2000. What does the dependent variable represent?
- A. the number of years since 2000
- B. the town's population
- C. the year 2000
- D. how fast the population is changing

> [!success]- Answer
> **B.** The dependent variable is the output, $P(t)$: the population. A is the independent variable (the input). D is a rate of change, not the variable.

**1.2** A function $f$ is either always increasing or always decreasing. Which statement about $f$ on $[1,5]$ is true?

| $x$ | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| $f(x)$ | 95 | 90 | 75 | 50 | 10 |

- A. $f$ is increasing because all the outputs are positive.
- B. $f$ is increasing because the outputs change by larger amounts.
- C. $f$ is decreasing because as the inputs increase, the outputs always decrease.
- D. $f$ is neither increasing nor decreasing.

> [!success]- Answer
> **C.** Every time $x$ increases, $f(x)$ decreases. A confuses positive with increasing; B describes the size of the changes (that's about concavity), not their direction.

**1.3** The graph of $f$ crosses the $x$-axis at $(-3,0)$ and $(4,0)$ and the $y$-axis at $(0,6)$. Which is true?
- A. $f(0)=-3$
- B. 6 is a zero of $f$
- C. $f(-3)=f(4)=6$
- D. The zeros of $f$ are $-3$ and 4, and $f(0)=6$.

> [!success]- Answer
> **D.** Zeros are the inputs where the output is 0 ($x$-intercepts), and the $y$-intercept is $(0,f(0))$. B treats the $y$-intercept as a zero.

## Rates of change

**1.4** What is the average rate of change of $f(x)=x^3$ on $[1,3]$?
- A. 13
- B. 26
- C. 9
- D. $\frac{13}{3}$

> [!success]- Answer
> **A.** $\frac{27-1}{3-1}=13$. B forgets to divide by the change in input; C is $f(3)/3$.

**1.5** Using the table, what is the average rate of change of distance from $t=13$ to $t=25$ seconds?

| time (s) | 10 | 13 | 19 | 25 |
|---|---|---|---|---|
| distance (m) | 80 | 76 | 43 | 30 |

- A. 3.833 m/s
- B. $-46$ m/s
- C. $-3.833$ m/s
- D. $-0.261$ m/s

> [!success]- Answer
> **C.** $\frac{30-76}{25-13}=\frac{-46}{12}\approx-3.833$. A drops the sign; B is only the change in output; D puts input over output.

**1.6** *(calculator)* Using the average rate of change on $[4,4.01]$, estimate the rate of change of $f(x)=\sqrt x$ at $x=4$.
- A. 2
- B. 0.5
- C. 4
- D. 0.25

> [!success]- Answer
> **D.** $\frac{\sqrt{4.01}-2}{0.01}\approx0.2498\approx0.25$. A is $f(4)$, not a rate.

**1.7** As the price of a concert ticket increases, the number of tickets sold decreases. The rate of change of tickets sold with respect to price is:
- A. positive
- B. negative
- C. zero
- D. impossible to tell

> [!success]- Answer
> **B.** One quantity goes up while the other goes down, so the rate of change is negative.

## Linear and quadratic rates of change; concavity

**1.8** A quadratic function has average rate of change 3 on $[0,2]$ and 7 on $[2,4]$. What is its average rate of change on $[4,6]$?
- A. 10
- B. 11
- C. 14
- D. 15

> [!success]- Answer
> **B.** For a quadratic, AROCs over consecutive equal-length intervals change by a constant amount: $3\to7$ is $+4$, so the next is 11.

**1.9** A function's concavity doesn't change. Which conclusion and reason are correct?

| $x$ | 0 | 2 | 4 | 6 | 8 |
|---|---|---|---|---|---|
| $f(x)$ | 10 | 11 | 14 | 20 | 29 |

- A. concave down, because the outputs increase
- B. linear, because the inputs change by 2 each time
- C. concave up, because the AROCs over equal-length intervals increase
- D. concave up, because the outputs increase

> [!success]- Answer
> **C.** The AROCs are $0.5,1.5,3,4.5$, which are increasing, so concave up. D has the right concavity but the wrong reason: increasing outputs say nothing about concavity.

**1.10** On an interval, the graph of $g$ is increasing and concave down. Which describes $g$ there?
- A. increasing at a decreasing rate
- B. increasing at an increasing rate
- C. decreasing at an increasing rate
- D. decreasing at a decreasing rate

> [!success]- Answer
> **A.** Concave down means the rate of change is decreasing, and the function is increasing. B would be concave up; C and D are decreasing.

**1.11** The graph of $f$ is concave up on $[2,6]$. If the secant line through $(2,f(2))$ and $(6,f(6))$ is used to estimate $f(4)$, the estimate is:
- A. an underestimate
- B. exact
- C. impossible to classify
- D. an overestimate

> [!success]- Answer
> **D.** On a concave-up interval the secant line lies above the graph, so its values are too high. A would be true for concave down.

## Polynomial functions and rates of change

**1.12** What is the local maximum value of $p(x)=x^3-3x$?
- A. 2
- B. $-2$
- C. 0
- D. 3

> [!success]- Answer
> **A.** The local max is at $x=-1$, where $p(-1)=-1+3=2$. B is the local min value; there's no global max (odd degree).

**1.13** A polynomial has exactly three real zeros, at $x=-2$, 1, and 5, each of multiplicity 1. Which must be true?
- A. It has exactly one local extremum.
- B. It has at least two local extrema.
- C. It has a global maximum.
- D. It has a point of inflection at $x=1$.

> [!success]- Answer
> **B.** There's at least one local extremum between each pair of consecutive distinct zeros: one in $(-2,1)$ and one in $(1,5)$. C depends on the degree and sign of the leading term; zeros aren't usually inflection points (D).

**1.14** Which function must have a global maximum or a global minimum?
- A. $x^3+x$
- B. $2x^5-x$
- C. $-x^4+3x^2$
- D. $x^7$

> [!success]- Answer
> **C.** Even-degree polynomials have a global max or min (here a max, since the leading coefficient is negative). The others are odd degree, with ends going in opposite directions.

## Complex zeros, multiplicity, even and odd

**1.15** A degree-5 polynomial with real coefficients has $2i$ and $3+i$ as zeros. How many real zeros does it have, counting multiplicity?
- A. 0
- B. 3
- C. 5
- D. 1

> [!success]- Answer
> **D.** Non-real zeros come in conjugate pairs, so $-2i$ and $3-i$ are zeros too. That's 4 non-real zeros out of 5 total, leaving exactly 1 real zero.

**1.16** What does the graph of $p(x)=(x+1)^2(x-3)$ do at $x=-1$?
- A. It touches the $x$-axis and bounces back (tangent).
- B. It crosses the $x$-axis in a straight line.
- C. It has a vertical asymptote.
- D. It flattens and crosses.

> [!success]- Answer
> **A.** $x=-1$ has even multiplicity (2), so the sign doesn't change and the graph is tangent to the axis. B is multiplicity 1; D is odd multiplicity 3 or more.

**1.17** Which function is even?
- A. $x^3+x$
- B. $x^2+x$
- C. $x^4-2x^2+1$
- D. $x^5-1$

> [!success]- Answer
> **C.** It has only even powers (1 is $x^0$), so $f(-x)=f(x)$. A is odd; B and D mix powers and are neither.

**1.18** What is the lowest degree of a polynomial that fits this table?

| $x$ | 0 | 1 | 2 | 3 | 4 |
|---|---|---|---|---|---|
| $f(x)$ | 1 | 2 | 9 | 28 | 65 |

- A. 2
- B. 3
- C. 4
- D. It isn't a polynomial; it's exponential.

> [!success]- Answer
> **B.** First differences $1,7,19,37$; second $6,12,18$; third $6,6$. The third differences are constant, so the degree is 3. D fails because the ratios aren't constant.

**1.19** Solve $(x+2)(x-1)^2(x-4)<0$.
- A. $-2<x<4$
- B. $x<-2$ or $x>4$
- C. $1<x<4$
- D. $-2<x<1$ or $1<x<4$

> [!success]- Answer
> **D.** The signs on the intervals are $+,-,-,+$, but $x=1$ makes the product 0, which isn't $<0$, so it's excluded. A includes $x=1$; B is where it's positive.

## End behavior

**1.20** For $p(x)=-3x^4+x^3+7$, what is $\lim_{x\to-\infty}p(x)$?
- A. $-\infty$
- B. $\infty$
- C. 0
- D. $-3$

> [!success]- Answer
> **A.** The leading term $-3x^4$ has even degree and a negative coefficient, so both ends go down.

**1.21** Which describes the end behavior of $p(x)=-x^3+4x^2-1$?
- A. $\lim_{x\to\infty}p(x)=\infty$ and $\lim_{x\to-\infty}p(x)=\infty$
- B. $\lim_{x\to\infty}p(x)=\infty$ and $\lim_{x\to-\infty}p(x)=-\infty$
- C. $\lim_{x\to\infty}p(x)=-\infty$ and $\lim_{x\to-\infty}p(x)=\infty$
- D. $\lim_{x\to\infty}p(x)=-\infty$ and $\lim_{x\to-\infty}p(x)=-\infty$

> [!success]- Answer
> **C.** Odd degree with a negative leading coefficient: up on the left, down on the right. B is the positive-coefficient case; A and D are even-degree shapes.

---

# Unit 1B — Rational Functions

## End behavior and asymptotes

**1.22** What is the horizontal asymptote of $r(x)=\dfrac{6x^2-1}{2x^2+x}$?
- A. $y=0$
- B. $y=3$
- C. $y=6$
- D. There isn't one.

> [!success]- Answer
> **B.** Equal degrees, so the asymptote is the ratio of leading coefficients, $\frac62$. A is for a bigger denominator degree; D is for a bigger numerator degree.

**1.23** What is the slant asymptote of $r(x)=\dfrac{x^2+3x+5}{x-1}$?
- A. $y=x+3$
- B. $y=x$
- C. $y=x+4$
- D. $y=1$

> [!success]- Answer
> **C.** Long division gives $x+4$ remainder 9, and the slant asymptote is the quotient. A just drops the denominator's constant.

**1.24** What is $\lim_{x\to-\infty}\dfrac{x^3+2}{x-1}$?
- A. 0
- B. $-\infty$
- C. 1
- D. $\infty$

> [!success]- Answer
> **D.** The quotient of leading terms is $\frac{x^3}{x}=x^2$, which goes to $\infty$ at both ends. B would be true for odd-degree behavior.

## Zeros and inequalities

**1.25** What are the zeros of $r(x)=\dfrac{(x-2)(x+5)}{(x-2)(x+1)}$?
- A. $x=-5$ only
- B. $x=2$ and $x=-5$
- C. $x=-1$
- D. $x=2$ only

> [!success]- Answer
> **A.** $x=2$ cancels completely, so it's a hole, not a zero. C is a vertical asymptote.

**1.26** Solve $\dfrac{x-2}{x+1}\ge0$.
- A. $x\le-1$ or $x\ge2$
- B. $x<-1$ or $x\ge2$
- C. $-1<x\le2$
- D. $x\ge2$ only

> [!success]- Answer
> **B.** The key values are $-1$ and 2, with signs $+,-,+$. $x=2$ is included (it gives 0) but $x=-1$ isn't (division by zero), which is A's mistake.

## Vertical asymptotes and holes

**1.27** For $r(x)=\dfrac{x+2}{x-3}$, what is $\lim_{x\to3^-}r(x)$?
- A. $\infty$
- B. 1
- C. 0
- D. $-\infty$

> [!success]- Answer
> **D.** Just left of 3 (say 2.99) the numerator is about 5 and the denominator is a tiny negative number, so $r\to-\infty$. A is the right-hand limit; B is the horizontal asymptote.

**1.28** What are all the vertical asymptotes of $r(x)=\dfrac{x-1}{(x-1)(x+4)(x-2)}$?
- A. $x=1$, $x=-4$, and $x=2$
- B. $x=-4$ only
- C. $x=-4$ and $x=2$
- D. There are none.

> [!success]- Answer
> **C.** $x-1$ cancels, so $x=1$ is a hole. The remaining denominator zeros, $-4$ and 2, are asymptotes.

**1.29** Where is the hole in the graph of $r(x)=\dfrac{x^2-x-2}{x^2-4}$?
- A. $\left(2,\frac34\right)$
- B. $(2,0)$
- C. $\left(-2,\frac14\right)$
- D. There is no hole.

> [!success]- Answer
> **A.** $\frac{(x-2)(x+1)}{(x-2)(x+2)}$ simplifies to $\frac{x+1}{x+2}$; at $x=2$ that's $\frac34$. $x=-2$ is a vertical asymptote, not a hole (C).

**1.30** Let $h(x)=\dfrac{(x-4)^2}{x-4}$. What happens at $x=4$?
- A. a vertical asymptote
- B. a zero only
- C. both a zero and a vertical asymptote
- D. a hole at $(4,0)$

> [!success]- Answer
> **D.** The numerator's multiplicity (2) is at least the denominator's (1), so it's a hole. It simplifies to $x-4$, which is 0 at $x=4$, so the hole is at $(4,0)$. B fails because $h(4)$ is undefined.

## Equivalent representations

**1.31** What is the coefficient of $x$ in the expansion of $(2x-1)^3$?
- A. $-6$
- B. 6
- C. 12
- D. $-12$

> [!success]- Answer
> **B.** The term is $3(2x)(-1)^2=6x$. D is the $x^2$ coefficient ($3(2x)^2(-1)=-12x^2$).

**1.32** Which form of a polynomial most directly shows its end behavior?
- A. standard form
- B. factored form
- C. a table of values
- D. a list of its zeros

> [!success]- Answer
> **A.** Standard form shows the leading term, which controls end behavior. B and D show zeros and intercepts.

**1.33** What is the remainder when $2x^3-3x^2+4x-5$ is divided by $x-2$?
- A. $-5$
- B. 0
- C. 7
- D. 3

> [!success]- Answer
> **C.** Long division gives $2x^2+x+6$ remainder 7. Check: $(x-2)(2x^2+x+6)+7=2x^3-3x^2+4x-5$. A is just the constant term.

---

# Unit 1C — Transformations, Piecewise Functions, and Models

## Transformations

**1.34** How does the graph of $g(x)=f(x+3)-2$ compare to the graph of $f$?
- A. right 3, down 2
- B. left 3, up 2
- C. right 3, up 2
- D. left 3, down 2

> [!success]- Answer
> **D.** Inside changes go the opposite way ($+3$ moves left); outside changes go as written ($-2$ moves down).

**1.35** The point $(1,4)$ is on the graph of $f$. Which point must be on the graph of $y=-2f(x+3)+1$?
- A. $(-2,-7)$
- B. $(4,-7)$
- C. $(-2,9)$
- D. $(4,9)$

> [!success]- Answer
> **A.** $x$: $1-3=-2$. $y$: $-2(4)+1=-7$. B shifts the wrong way; C forgets the reflection.

**1.36** What transformation turns $f(x)$ into $f(3x)$?
- A. a vertical dilation by a factor of 3
- B. a horizontal dilation by a factor of 3
- C. a horizontal dilation by a factor of $\frac13$
- D. a vertical dilation by a factor of $\frac13$

> [!success]- Answer
> **C.** Multiplying the input by $b$ is a horizontal dilation by $\frac1b$, so the graph is squeezed to a third of its width. B is the common opposite-direction trap.

**1.37** What is the range of $g(x)=\sqrt{x-2}+1$?
- A. $y\ge0$
- B. $y\ge1$
- C. $y\ge2$
- D. all real numbers

> [!success]- Answer
> **B.** $\sqrt{x-2}\ge0$, and adding 1 shifts every output up. C confuses the range with the domain ($x\ge2$).

## Piecewise functions

**1.38** Let $p(x)=\begin{cases}4-x,&x\le1\\[2pt]\dfrac{4x}{x+1},&x>1\end{cases}$. What is $p(1)+p(3)$?
- A. 5
- B. 3
- C. 7
- D. 6

> [!success]- Answer
> **D.** $p(1)$ uses the first piece (since $1\le1$): 3. $p(3)$ uses the second: $\frac{12}4=3$. A uses the second piece for $p(1)$ ($\frac42=2$).

**1.39** For $x<1.5$, $|2x-3|$ equals:
- A. $2x-3$
- B. $2x+3$
- C. $-2x+3$
- D. $-2x-3$

> [!success]- Answer
> **C.** For $x<1.5$ the inside $2x-3$ is negative, so the absolute value negates it: $-(2x-3)=-2x+3$. A is the piece for $x\ge1.5$.

## Models

**1.40** Squares are cut from the corners of a sheet of cardboard, which is then folded into an open box. Which type of function best models the box's volume in terms of the square's side length?
- A. cubic
- B. quadratic
- C. exponential
- D. linear

> [!success]- Answer
> **A.** Volume is three-dimensional: $V(x)=x(L-2x)(W-2x)$ is a product of three linear factors. Quadratics fit areas (B).

**1.41** Over equal input steps, a data set's second differences are roughly constant. Which model fits best?
- A. linear
- B. quadratic
- C. cubic
- D. exponential

> [!success]- Answer
> **B.** Constant second differences mean the AROCs change linearly, which is the quadratic pattern. Linear needs constant first differences; cubic needs constant third differences.

**1.42** What is the smallest degree $n$ such that any 5 points with distinct inputs can be fit exactly by a polynomial of degree at most $n$?
- A. 3
- B. 5
- C. 4
- D. 6

> [!success]- Answer
> **C.** A polynomial of degree at most $n$ can fit any $n+1$ points with distinct inputs, so 5 points need degree at most 4.

**1.43** Gravitational force is inversely proportional to the square of the distance between two objects. Which models the force?
- A. $F(d)=kd^2$
- B. $F(d)=k\cdot2^{-d}$
- C. $F(d)=kd$
- D. $F(d)=\dfrac{k}{d^2}$

> [!success]- Answer
> **D.** Inversely proportional means dividing by the quantity, which gives a rational model. A is directly proportional to $d^2$.

**1.44** A ball's height is $h(t)=-16t^2+56t+6$ feet, $t$ seconds after it's thrown, and it lands at $t\approx3.604$. What is the best domain for the model?
- A. $0\le t\le3.604$
- B. $t\ge0$
- C. all real numbers
- D. $0\le t\le1.75$

> [!success]- Answer
> **A.** Time starts at 0, and the model stops making sense once the ball hits the ground. B allows negative heights; D stops at the peak.

---

# Unit 2A — Sequences and Exponential Functions

## Arithmetic and geometric sequences

**2.1** An arithmetic sequence has $a_3=10$ and $a_8=35$. Which gives $a_n$?
- A. $a_n=10+7(n-3)$
- B. $a_n=10+5(n-3)$
- C. $a_n=5+10n$
- D. $a_n=35+5n$

> [!success]- Answer
> **B.** Five steps add 25, so $d=5$, and $a_n=a_3+d(n-3)$. Check: $a_8=10+25=35$. C has the numbers swapped.

**2.2** A geometric sequence has $g_2=12$ and $g_5=96$. What is $g_0$?
- A. 3
- B. 6
- C. 12
- D. 4

> [!success]- Answer
> **A.** $r^3=\frac{96}{12}=8$, so $r=2$. Going back two steps: $12\div2\div2=3$. B goes back only one step.

## Linear vs. exponential

**2.3** Which table is best modeled by an exponential function?
- A. $y$: 2, 5, 8, 11 for $x$ = 0, 1, 2, 3
- B. $y$: 2, 4, 8, 14 for $x$ = 0, 1, 2, 3
- C. $y$: 1, 4, 9, 16 for $x$ = 0, 1, 2, 3
- D. $y$: 2, 6, 18, 54 for $x$ = 0, 1, 2, 3

> [!success]- Answer
> **D.** Each output is 3 times the last: proportional over equal-length input intervals. A adds 3 each time (linear); C is $(x+1)^2$ (quadratic); B's ratios aren't constant.

**2.4** Which exponential function passes through $(1,6)$ and $(3,54)$?
- A. $f(x)=6\cdot3^x$
- B. $f(x)=3\cdot2^x$
- C. $f(x)=2\cdot3^x$
- D. $f(x)=2\cdot9^x$

> [!success]- Answer
> **C.** Two steps multiply by 9, so $b=3$, and $f(1)=6$ gives $a=2$. A treats $(1,6)$ as the initial value; D uses the two-step factor as the base.

## Exponential functions and manipulation

**2.5** Which function shows exponential decay?
- A. $f(x)=4(0.7)^x$
- B. $f(x)=0.5(3)^x$
- C. $f(x)=3(1.2)^x$
- D. $f(x)=2^x$

> [!success]- Answer
> **A.** Decay needs $a>0$ and $0<b<1$. B has a small initial value but base 3, so it grows.

**2.6** What is the horizontal asymptote of $f(x)=5\cdot2^x-3$?
- A. $y=0$
- B. $y=5$
- C. $x=-3$
- D. $y=-3$

> [!success]- Answer
> **D.** Adding $-3$ shifts the graph, and its asymptote $y=0$, down 3. C is a vertical line, which exponentials don't have.

**2.7** Which expression equals $2^{x+3}$?
- A. $2^x+8$
- B. $6\cdot2^x$
- C. $8\cdot2^x$
- D. $2^{3x}$

> [!success]- Answer
> **C.** Product property: $2^{x+3}=2^3\cdot2^x$. A horizontal shift of an exponential is a vertical dilation.

**2.8** Which expression equals $3^{2x+1}$?
- A. $9^x+3$
- B. $3\cdot9^x$
- C. $3\cdot6^x$
- D. $9^{x+1}$

> [!success]- Answer
> **B.** $3^{2x+1}=3^1\cdot(3^2)^x=3\cdot9^x$. C multiplies the base by 2 instead of squaring it.

## Context and modeling

**2.9** A population grows 6% per year ($t$ in years). What is its monthly growth factor?
- A. $\frac{1.06}{12}$
- B. 1.005
- C. $1.06^{12}$
- D. $1.06^{1/12}$

> [!success]- Answer
> **D.** $1.06^t=\left(1.06^{1/12}\right)^{12t}$, and $12t$ counts months. That's about 1.00487. B is the simple guess $0.06/12$, which isn't quite right; C is the factor for 12 years.

**2.10** Coffee cools in a 70° room. Its temperature is 190°, 130°, 100°, 85° at $t=0,1,2,3$ hours. Which model fits?
- A. $T(t)=70+120(0.5)^t$
- B. $T(t)=190(0.5)^t$
- C. $T(t)=190-60t$
- D. $T(t)=120(0.5)^t$

> [!success]- Answer
> **A.** Subtracting the room temperature gives 120, 60, 30, 15, which halve each hour, so add 70 back to the exponential. B ignores the 70° floor; C assumes a constant drop.

**2.11** A model predicts 47.5, but the actual value is 50. Which is correct?
- A. The residual is 2.5 and the model overestimates.
- B. The residual is 2.5 and the model underestimates.
- C. The residual is $-2.5$ and the model underestimates.
- D. The residual is $-2.5$ and the model overestimates.

> [!success]- Answer
> **B.** Residual = actual − predicted = 2.5. Positive means the actual value is above the prediction, so the model is too low.

**2.12** A residual plot shows a clear U-shaped pattern. What does that mean?
- A. The model is appropriate.
- B. Every residual is positive.
- C. A different type of model would fit better.
- D. The data are linear.

> [!success]- Answer
> **C.** A good model's residuals scatter randomly with no pattern. A curved pattern means the model type misses the data's shape.

## Composition

**2.13** If $f(x)=x^2$ and $g(x)=x+3$, what is $g(f(2))$?
- A. 25
- B. 10
- C. 5
- D. 7

> [!success]- Answer
> **D.** $f$ first: $f(2)=4$, then $g(4)=7$. A computes $f(g(2))$ instead; order matters.

**2.14** If $f(x)=\sqrt x$ and $g(x)=x-5$, what is the domain of $f(g(x))$?
- A. $x\ge5$
- B. $x\ge0$
- C. $x\ge-5$
- D. all real numbers

> [!success]- Answer
> **A.** $f(g(x))=\sqrt{x-5}$ needs $x-5\ge0$. B is $f$'s own domain.

---

# Unit 2B — Inverses and Logarithmic Functions

## Decomposition and inverses

**2.15** $h(x)=(x^2+1)^3$ is written as $f(g(x))$ with $g(x)=x^2+1$. What is $f(x)$?
- A. $x^2+1$
- B. $x^3$
- C. $3x$
- D. $(x+1)^3$

> [!success]- Answer
> **B.** $g$ is the inside; $f$ cubes whatever it receives.

**2.16** What is the inverse of $f(x)=\dfrac{2x-1}{3}$?
- A. $\dfrac{3}{2x-1}$
- B. $\dfrac{3x-1}{2}$
- C. $\dfrac{3x+1}{2}$
- D. $\dfrac{2x+1}{3}$

> [!success]- Answer
> **C.** Swap and solve: $x=\frac{2y-1}3\Rightarrow3x=2y-1\Rightarrow y=\frac{3x+1}2$. A is the reciprocal, which is not the inverse.

**2.17** Does $f$ have an inverse on this domain, and why?

| $x$ | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| $f(x)$ | 4 | 7 | 2 | 7 | 9 |

- A. Yes, because every input has an output.
- B. Yes, because the outputs are all positive.
- C. No, because it fails the horizontal line test.
- D. No, because $f(2)=f(4)=7$.

> [!success]- Answer
> **D.** An output that comes from two inputs means the function isn't one-to-one. C is the right idea but isn't an acceptable justification on the AP exam; cite the repeated value.

**2.18** If $f(3)=8$, then $f^{-1}(8)=$
- A. 3
- B. $\frac18$
- C. 8
- D. $\frac13$

> [!success]- Answer
> **A.** The inverse swaps the pair $(3,8)$ to $(8,3)$. B treats $f^{-1}$ as a reciprocal.

## Logarithmic expressions and functions

**2.19** What is $\log_3\frac19$?
- A. 2
- B. $-2$
- C. $\frac12$
- D. $-\frac12$

> [!success]- Answer
> **B.** $3^{-2}=\frac19$.

**2.20** $\log_210$ is between which two integers?
- A. 2 and 3
- B. 1 and 2
- C. 4 and 5
- D. 3 and 4

> [!success]- Answer
> **D.** $2^3=8<10<16=2^4$. (It's about 3.32.)

**2.21** The point $(3,8)$ is on the graph of $y=2^x$. Which point is on $y=\log_2x$?
- A. $(3,8)$
- B. $(-3,8)$
- C. $(8,3)$
- D. $\left(3,\frac18\right)$

> [!success]- Answer
> **C.** Inverse functions swap coordinates.

**2.22** What is the domain of $f(x)=\log(x+4)$?
- A. $x>-4$
- B. $x>0$
- C. $x>4$
- D. $x\ge-4$

> [!success]- Answer
> **A.** The argument must be positive: $x+4>0$. D includes $-4$, where the argument is 0 and the log is undefined.

**2.23** Inputs 1, 3, 9, 27 give outputs 2, 5, 8, 11. Which model fits best?
- A. linear
- B. exponential
- C. logarithmic
- D. quadratic

> [!success]- Answer
> **C.** The inputs change multiplicatively (×3) while the outputs change additively (+3). Exponential is the reverse (B).

## Log properties

**2.24** Which is equivalent to $\log_2\dfrac{8x^3}{y}$?
- A. $8+3\log_2x-\log_2y$
- B. $3+3\log_2x-\log_2y$
- C. $3\log_2(8x)-\log_2y$
- D. $\dfrac{3+\log_2x^3}{\log_2y}$

> [!success]- Answer
> **B.** Quotient → subtract, product → add, power → multiply: $\log_28+3\log_2x-\log_2y$, and $\log_28=3$. A doesn't evaluate $\log_28$; D treats the quotient rule as division.

**2.25** Which expression equals $\log_520$?
- A. $\dfrac{\ln5}{\ln20}$
- B. $\ln20-\ln5$
- C. $\ln4$
- D. $\dfrac{\ln20}{\ln5}$

> [!success]- Answer
> **D.** Change of base: $\log_bx=\frac{\ln x}{\ln b}$. B and C equal $\ln\frac{20}5=\ln4$, which is a different number.

## Equations and inequalities

**2.26** Solve $\log_2x+\log_2(x-2)=3$.
- A. $x=4$ only
- B. $x=4$ and $x=-2$
- C. $x=-2$ only
- D. There is no solution.

> [!success]- Answer
> **A.** $\log_2(x(x-2))=3\Rightarrow x^2-2x-8=0\Rightarrow x=4$ or $-2$. $x=-2$ is extraneous because $\log_2(-2)$ is undefined, so B is the trap.

**2.27** Solve $e^{2x}-5e^x+6=0$.
- A. $x=2$ and $x=3$
- B. $x=\ln2$ and $x=\ln3$
- C. $x=\ln5$ and $x=\ln6$
- D. $x=\ln6$ only

> [!success]- Answer
> **B.** With $u=e^x$: $u^2-5u+6=(u-2)(u-3)=0$, so $e^x=2$ or 3. A forgets to undo $u=e^x$.

**2.28** Solve $\left(\frac12\right)^x>4$.
- A. $x>-2$
- B. $x>2$
- C. $x<-2$
- D. $x<2$

> [!success]- Answer
> **C.** $4=\left(\frac12\right)^{-2}$. The base is less than 1 (a decreasing function), so the inequality flips: $x<-2$.

**2.29** What is the inverse of $f(x)=2\ln(x+3)-1$?
- A. $e^{(x-1)/2}+3$
- B. $\dfrac{e^x+1}{2}-3$
- C. $\ln\dfrac{x+1}{2}-3$
- D. $e^{(x+1)/2}-3$

> [!success]- Answer
> **D.** Swap and undo in reverse order: $x=2\ln(y+3)-1\Rightarrow\frac{x+1}2=\ln(y+3)\Rightarrow y=e^{(x+1)/2}-3$. A undoes each step with the wrong sign.

## Log models and semi-log plots

**2.30** A model $f(x)=a\ln x+k$ passes through $(1,5)$ and $(e^2,11)$. What is $f(x)$?
- A. $3\ln x+5$
- B. $5\ln x+3$
- C. $6\ln x+5$
- D. $3\ln x+11$

> [!success]- Answer
> **A.** $\ln1=0$, so $k=5$. Then $a\ln e^2+5=2a+5=11$, so $a=3$. C forgets that $\ln e^2=2$.

**2.31** On a semi-log plot (base-10 log scale on the $y$-axis), data fall on the line $\log y=0.3x+1$. Which model fits?
- A. $y=0.3x+1$
- B. $y=10\left(10^{0.3}\right)^x$
- C. $y=0.3\cdot10^x$
- D. $y=(0.3)^x$

> [!success]- Answer
> **B.** For $y=ab^x$, $\log y=(\log b)x+\log a$, so $\log b=0.3$ and $\log a=1$, giving $b=10^{0.3}$ and $a=10$. A reads the line as the model itself.

**2.32** How do exponential data appear on a semi-log plot (log scale on the $y$-axis)?
- A. as a parabola
- B. as a horizontal line
- C. as a straight line
- D. as a curve that levels off

> [!success]- Answer
> **C.** Taking the log of $ab^x$ gives a linear function of $x$.

---

# Unit 3A — Trigonometry, Sine, and Cosine

## Right triangles, periodicity, radians

**3.1** A board leans against a wall, making a 72° angle with the floor, with its foot 2.5 ft from the wall. How long is the board?
- A. $2.5\cos72°$
- B. $\dfrac{2.5}{\sin72°}$
- C. $2.5\tan72°$
- D. $\dfrac{2.5}{\cos72°}$

> [!success]- Answer
> **D.** The 2.5 ft is adjacent to the angle and the board is the hypotenuse: $\cos72°=\frac{2.5}{L}$, so $L\approx8.09$ ft. C is the height up the wall.

**3.2** A tide's maximum heights happen at $t=2$, 14, and 26 hours. What is the period?
- A. 2 hours
- B. 12 hours
- C. 24 hours
- D. 6 hours

> [!success]- Answer
> **B.** The period is the time between consecutive maxima. D is the time from a max to the next min.

**3.3** An angle in a circle of radius 4 subtends an arc of length 8.796. What is the angle in radians?
- A. 2.199
- B. 35.184
- C. 0.455
- D. 4.796

> [!success]- Answer
> **A.** $\theta=\frac sr=\frac{8.796}4$. B multiplies instead; C divides the wrong way.

**3.4** In which quadrant is the terminal ray of an angle of 4.37 radians?
- A. I
- B. II
- C. III
- D. IV

> [!success]- Answer
> **C.** $\pi\approx3.14<4.37<\frac{3\pi}2\approx4.71$.

**3.5** What is 150° in radians?
- A. $\frac{2\pi}3$
- B. $\frac{5\pi}6$
- C. $\frac{3\pi}4$
- D. $\frac{5\pi}3$

> [!success]- Answer
> **B.** $150\cdot\frac\pi{180}=\frac{5\pi}6$. A is 120°, C is 135°, and D is 300°.

## Sine and cosine values

**3.6** What is $\sin\frac{7\pi}6$?
- A. $\frac12$
- B. $-\frac{\sqrt3}2$
- C. $\frac{\sqrt3}2$
- D. $-\frac12$

> [!success]- Answer
> **D.** The reference angle is $\frac\pi6$, and sine is negative in Quadrant III. B uses the cosine value.

**3.7** The terminal ray of $\frac{2\pi}3$ meets a circle of radius 6 centered at the origin. At what point?
- A. $(3,3\sqrt3)$
- B. $(-3\sqrt3,3)$
- C. $(-3,3\sqrt3)$
- D. $(-3,-3\sqrt3)$

> [!success]- Answer
> **C.** $(6\cos\frac{2\pi}3,\ 6\sin\frac{2\pi}3)=(6\cdot(-\frac12),\ 6\cdot\frac{\sqrt3}2)$. B swaps sine and cosine; A ignores the Quadrant II sign.

**3.8** What is $\tan\frac{5\pi}4$?
- A. 1
- B. $-1$
- C. $\frac{\sqrt2}2$
- D. undefined

> [!success]- Answer
> **A.** Sine and cosine are both $-\frac{\sqrt2}2$ in Quadrant III, so the ratio is positive 1. Tangent is positive in Quadrant III.

## Sinusoidal functions

**3.9** A sinusoidal model has a maximum of 18 and a minimum of 4. What are its amplitude and midline?
- A. amplitude 14, midline $y=11$
- B. amplitude 7, midline $y=11$
- C. amplitude 7, midline $y=4$
- D. amplitude 11, midline $y=7$

> [!success]- Answer
> **B.** Amplitude $=\frac{18-4}2=7$; midline $y=\frac{18+4}2=11$. A uses the full height.

**3.10** What is the period of $y=3\sin(4\theta)+1$?
- A. 4
- B. $8\pi$
- C. $4\pi$
- D. $\frac\pi2$

> [!success]- Answer
> **D.** Period $=\frac{2\pi}{4}$. B and C multiply by $b$ instead of dividing.

**3.11** What is the phase shift of $y=\sin\left(2\theta-\frac\pi2\right)$?
- A. right $\frac\pi2$
- B. left $\frac\pi4$
- C. right $\frac\pi4$
- D. left $\frac\pi2$

> [!success]- Answer
> **C.** Factor out $b$: $\sin\left(2\left(\theta-\frac\pi4\right)\right)$. A forgets to factor.

**3.12** What is the maximum value of $y=-2\cos\theta+5$, and where does it first occur for $\theta\ge0$?
- A. 7, at $\theta=\pi$
- B. 7, at $\theta=0$
- C. 3, at $\theta=0$
- D. 5, at $\theta=\frac\pi2$

> [!success]- Answer
> **A.** $-2\cos\theta$ is largest when $\cos\theta=-1$, at $\theta=\pi$: $2+5=7$. At $\theta=0$ the value is 3, the minimum (that's C).

## Sinusoidal modeling

**3.13** A Ferris wheel's center is 25 m high, its radius is 20 m, and one turn takes 8 minutes. A rider starts at the bottom at $t=0$. Which gives the rider's height?
- A. $h(t)=20\cos\left(\frac\pi4t\right)+25$
- B. $h(t)=-20\cos\left(\frac\pi4t\right)+25$
- C. $h(t)=-20\cos(8t)+25$
- D. $h(t)=-25\cos\left(\frac\pi4t\right)+20$

> [!success]- Answer
> **B.** $b=\frac{2\pi}8=\frac\pi4$, the midline is 25, and the amplitude is 20. Starting at a minimum means $-\cos$. A starts at the top; C uses the period as $b$; D swaps the amplitude and midline.

**3.14** On a sinusoid, G is on the midline going down and J is the next minimum. On the interval from G to J, the graph is:
- A. concave down, and the rate of change is decreasing
- B. concave up, and the rate of change is decreasing
- C. concave down, and the rate of change is increasing
- D. concave up, and the rate of change is increasing

> [!success]- Answer
> **D.** Below the midline, a sinusoid is concave up, which means its rate of change is increasing. The function itself is decreasing there, but that's a separate question.

---

# Unit 3B — Tangent, Inverse Trig, Identities, and Polar

## Tangent and the reciprocal functions

**3.15** What is the period of $y=\tan\frac\theta2$?
- A. $\frac\pi2$
- B. $\pi$
- C. $2\pi$
- D. $4\pi$

> [!success]- Answer
> **C.** Tangent's period is $\frac\pi{\lvert b\rvert}=\frac{\pi}{1/2}$. D uses sine's $2\pi$ as the starting period.

**3.16** Where are the vertical asymptotes of $y=\tan\theta$?
- A. $\theta=\frac\pi2+k\pi$
- B. $\theta=k\pi$
- C. $\theta=\frac\pi4+k\pi$
- D. $\theta=2k\pi$

> [!success]- Answer
> **A.** Where $\cos\theta=0$. B gives tangent's zeros (and cotangent's asymptotes).

**3.17** What is $\csc\frac\pi6$?
- A. $\frac12$
- B. $\frac{2}{\sqrt3}$
- C. 2
- D. $\sqrt3$

> [!success]- Answer
> **C.** $\csc=\frac1{\sin}=\frac1{1/2}$. B is $\sec\frac\pi6$.

**3.18** What is the range of $y=\sec\theta$?
- A. all real numbers
- B. $-1\le y\le1$
- C. $y\ge1$ only
- D. $y\le-1$ or $y\ge1$

> [!success]- Answer
> **D.** Cosine's values lie in $[-1,1]$, so their reciprocals have size at least 1. B is cosine's range.

**3.19** Where does $y=\cot\theta$ have vertical asymptotes?
- A. where $\sin\theta=0$
- B. where $\cos\theta=0$
- C. where $\tan\theta=1$
- D. nowhere

> [!success]- Answer
> **A.** $\cot\theta=\frac{\cos\theta}{\sin\theta}$ is undefined where its denominator is 0. B gives its zeros.

## Inverse trig

**3.20** What is $\arccos\left(-\frac12\right)$?
- A. $-\frac\pi3$
- B. $\frac\pi3$
- C. $\frac{4\pi}3$
- D. $\frac{2\pi}3$

> [!success]- Answer
> **D.** Arccosine outputs are in $[0,\pi]$, and $\cos\frac{2\pi}3=-\frac12$. C has the right cosine but is outside the range; A uses the arcsine range.

**3.21** What is $\arcsin\left(\sin\frac{5\pi}6\right)$?
- A. $\frac{5\pi}6$
- B. $\frac\pi6$
- C. $-\frac\pi6$
- D. undefined

> [!success]- Answer
> **B.** $\sin\frac{5\pi}6=\frac12$, and arcsine's output must be in $[-\frac\pi2,\frac\pi2]$, so it's $\frac\pi6$. A assumes they cancel.

**3.22** What is $\sin\left(\arccos\frac35\right)$?
- A. $\frac34$
- B. $\frac54$
- C. $\frac45$
- D. $\frac35$

> [!success]- Answer
> **C.** Draw a right triangle with adjacent side 3 and hypotenuse 5: the opposite side is 4, so sine is $\frac45$ (positive, since arccos gives an angle in $[0,\pi]$).

## Trig equations

**3.23** What are all solutions of $2\sin\theta-1=0$?
- A. $\theta=\frac\pi6+2\pi k$ and $\theta=\frac{5\pi}6+2\pi k$
- B. $\theta=\frac\pi6+2\pi k$ only
- C. $\theta=\frac\pi6+\pi k$
- D. $\theta=\frac\pi3+2\pi k$ and $\theta=\frac{2\pi}3+2\pi k$

> [!success]- Answer
> **A.** $\sin\theta=\frac12$ in Quadrants I and II. B misses the second quadrant; C uses tangent's period; D uses the cosine-value angles.

**3.24** How many solutions does $\cos2\theta=0$ have in $[0,2\pi)$?
- A. 1
- B. 2
- C. 3
- D. 4

> [!success]- Answer
> **D.** $2\theta$ runs through $[0,4\pi)$, two full turns, giving $\theta=\frac\pi4,\frac{3\pi}4,\frac{5\pi}4,\frac{7\pi}4$. B forgets the second turn.

**3.25** Solve $\sin\theta\ge\frac12$ on $[0,2\pi)$.
- A. $0\le\theta\le\frac\pi6$
- B. $\frac\pi6\le\theta\le\frac{5\pi}6$
- C. $\frac{5\pi}6\le\theta<2\pi$
- D. $\frac\pi3\le\theta\le\frac{2\pi}3$

> [!success]- Answer
> **B.** Sine is at least $\frac12$ between its two solutions, where the unit circle is highest. A and C are where it's smaller.

## Identities

**3.26** What is the exact value of $\sin\frac\pi{12}$?
- A. $\dfrac{\sqrt6+\sqrt2}4$
- B. $\dfrac{\sqrt6-\sqrt2}4$
- C. $\dfrac{\sqrt2}4$
- D. $\dfrac{\sqrt3-1}2$

> [!success]- Answer
> **B.** $\sin\left(\frac\pi3-\frac\pi4\right)=\frac{\sqrt3}2\cdot\frac{\sqrt2}2-\frac12\cdot\frac{\sqrt2}2$. A is $\cos\frac\pi{12}$ (the sum version).

**3.27** Which expression equals $\cos2\theta$?
- A. $2\sin^2\theta-1$
- B. $2\sin\theta\cos\theta$
- C. $1-2\sin^2\theta$
- D. $\cos^2\theta+\sin^2\theta$

> [!success]- Answer
> **C.** From $\cos^2\theta-\sin^2\theta$, replace $\cos^2\theta$ with $1-\sin^2\theta$. B is $\sin2\theta$; D equals 1.

**3.28** $\tan^2\theta+1=$
- A. $\csc^2\theta$
- B. $\cot^2\theta$
- C. $\sin^2\theta$
- D. $\sec^2\theta$

> [!success]- Answer
> **D.** Divide $\sin^2\theta+\cos^2\theta=1$ by $\cos^2\theta$. A is $1+\cot^2\theta$.

## Polar coordinates and graphs

**3.29** What are the rectangular coordinates of the polar point $\left(4,\frac{2\pi}3\right)$?
- A. $(-2,2\sqrt3)$
- B. $(2,2\sqrt3)$
- C. $(-2\sqrt3,2)$
- D. $(-2,-2\sqrt3)$

> [!success]- Answer
> **A.** $x=4\cos\frac{2\pi}3=-2$ and $y=4\sin\frac{2\pi}3=2\sqrt3$. C swaps sine and cosine.

**3.30** What are polar coordinates (with $r>0$) of the rectangular point $(-3,3)$?
- A. $\left(3\sqrt2,-\frac\pi4\right)$
- B. $\left(3\sqrt2,\frac{3\pi}4\right)$
- C. $\left(6,\frac{3\pi}4\right)$
- D. $\left(3\sqrt2,\frac\pi4\right)$

> [!success]- Answer
> **B.** $r=\sqrt{9+9}=3\sqrt2$. Since $x<0$, $\theta=\arctan(-1)+\pi=\frac{3\pi}4$. A forgets to add $\pi$, which puts the point in Quadrant IV.

**3.31** How many petals does $r=2\cos3\theta$ have?
- A. 6
- B. 2
- C. 3
- D. 9

> [!success]- Answer
> **C.** For $r=a\cos n\theta$, odd $n$ gives $n$ petals. A applies the even rule ($2n$).

**3.32** What is the graph of $r=1+2\cos\theta$?
- A. a cardioid
- B. a circle
- C. a convex limaçon
- D. a limaçon with an inner loop

> [!success]- Answer
> **D.** $a=1<b=2$, so it passes through the pole twice and forms an inner loop. A needs $a=b$; C needs $a\ge2b$.

## Rates of change in polar functions

**3.33** On an interval, $r=f(\theta)$ is negative and decreasing. Is the point $(f(\theta),\theta)$ moving toward or away from the pole?
- A. toward the pole
- B. away from the pole
- C. neither; the distance is constant
- D. there's not enough information

> [!success]- Answer
> **B.** Distance from the pole is $\lvert r\rvert$. A negative number that's decreasing gets more negative, so $\lvert r\rvert$ grows.

**3.34** What is the average rate of change of $r=1+2\cos\theta$ on $\left[0,\frac\pi2\right]$?
- A. $-\dfrac4\pi$
- B. $-2$
- C. $\dfrac4\pi$
- D. $-\dfrac\pi4$

> [!success]- Answer
> **A.** $\frac{r(\pi/2)-r(0)}{\pi/2-0}=\frac{1-3}{\pi/2}$. B is just the change in $r$; D flips the fraction.

---

# Unit 4 — Matrices

**4.1** What size is the product of a $2\times3$ matrix and a $3\times4$ matrix?
- A. $2\times4$
- B. $3\times3$
- C. $4\times2$
- D. It's undefined.

> [!success]- Answer
> **A.** The inner numbers match (3 and 3), and the outer numbers give the size.

**4.2** What is $\det\begin{bmatrix}2&1\\5&3\end{bmatrix}$?
- A. 11
- B. 1
- C. $-1$
- D. 13

> [!success]- Answer
> **B.** $ad-bc=6-5$. A adds instead of subtracting.

**4.3** What is the inverse of $\begin{bmatrix}2&1\\5&3\end{bmatrix}$?
- A. $\begin{bmatrix}3&-1\\-5&2\end{bmatrix}$
- B. $\begin{bmatrix}3&1\\5&2\end{bmatrix}$
- C. $\begin{bmatrix}2&-1\\-5&3\end{bmatrix}$
- D. $\begin{bmatrix}-3&1\\5&-2\end{bmatrix}$

> [!success]- Answer
> **A.** Swap the diagonal, negate the other two entries, and divide by $\det=1$. C forgets the swap; D negates the wrong entries.

**4.4** The matrix $\begin{bmatrix}0&-1\\1&0\end{bmatrix}$ rotates vectors 90° counterclockwise. Where does it send $\langle3,1\rangle$?
- A. $\langle1,-3\rangle$
- B. $\langle-1,3\rangle$
- C. $\langle-3,1\rangle$
- D. $\langle3,-1\rangle$

> [!success]- Answer
> **B.** Row 1: $0\cdot3+(-1)\cdot1=-1$. Row 2: $1\cdot3+0\cdot1=3$. A is the clockwise rotation.

**4.5** When does a $2\times2$ matrix have no inverse?
- A. when its determinant is 1
- B. when all its entries are positive
- C. when its determinant is 0
- D. when it's square

> [!success]- Answer
> **C.** The inverse formula divides by the determinant. A determinant of 0 also means the column vectors are parallel.

**4.6** With $T=\begin{bmatrix}0.8&0.1\\0.2&0.9\end{bmatrix}$ and state vector $\begin{bmatrix}300\\0\end{bmatrix}$, what is the next state?
- A. $\begin{bmatrix}300\\0\end{bmatrix}$
- B. $\begin{bmatrix}270\\30\end{bmatrix}$
- C. $\begin{bmatrix}60\\240\end{bmatrix}$
- D. $\begin{bmatrix}240\\60\end{bmatrix}$

> [!success]- Answer
> **D.** $0.8(300)+0.1(0)=240$ and $0.2(300)+0.9(0)=60$. C swaps the states.

---

# Mixed and Short-Answer

**S.1** *(FRQ 1 style)* Which type of function best models $f$? Justify your answer.

| $x$ | 0 | 1 | 2 | 3 | 4 |
|---|---|---|---|---|---|
| $f(x)$ | 3 | 6 | 12 | 24 | 48 |

> [!success]- Answer
> **Exponential.** The outputs are proportional over equal-length input-value intervals: $\frac63=\frac{12}6=\frac{24}{12}=\frac{48}{24}=2$. The outputs change multiplicatively by a factor of 2 while the inputs change additively by 1.

**S.2** For $r(x)=\dfrac{x^2-x-6}{x^2-9}$, find the hole, vertical asymptote, horizontal asymptote, zero, and $y$-intercept.

> [!success]- Answer
> Factor: $\frac{(x-3)(x+2)}{(x-3)(x+3)}=\frac{x+2}{x+3}$ for $x\ne3$.
> - Hole: $\left(3,\frac56\right)$
> - Vertical asymptote: $x=-3$
> - Horizontal asymptote: $y=1$ (equal degrees)
> - Zero: $x=-2$
> - $y$-intercept: $\left(0,\frac23\right)$

**S.3** *(FRQ 2 style, calculator)* A bacteria population is modeled by $P(t)=ab^t$, $t$ in hours. $P(0)=200$ and $P(4)=450$.
1. Find $a$ and $b$.
2. Find the average rate of change of $P$ from $t=0$ to $t=4$, with units.
3. Use the secant line from part 2 to estimate $P(2)$. Is this an overestimate or underestimate of the model's value? Explain using concavity.

> [!success]- Answer
> 1. $a=200$; $200b^4=450\Rightarrow b=2.25^{1/4}\approx1.225$.
> 2. $\frac{450-200}{4-0}=62.5$ bacteria per hour.
> 3. Secant estimate: $200+62.5(2)=325$. The model gives $P(2)=200b^2=200(1.5)=300$. Because $P$ is concave up on $0<t<4$ (exponential growth), the secant line is above the graph there, so the estimate overestimates the model's value.

**S.4** *(FRQ 3 style, no calculator)* A point on a wheel is $h(t)$ meters above the ground. The wheel's center is 4 m up, its radius is 3 m, and it turns once every 10 seconds. At $t=0$ the point is at its highest.
1. On a graph of two full cycles starting at $t=0$, the max at $t=0$ is F, the next midline point is G, the min is J, the next midline point is K, and the next max is P. Give their coordinates.
2. $h(t)=a\cos(b(t+c))+d$. Give values of $a$, $b$, $c$, $d$.
3. On the interval from J to K, are the values of $h$ positive or negative, and increasing or decreasing? Describe the concavity and the rate of change.

> [!success]- Answer
> 1. Key points every $\frac{10}4=2.5$ s: F$(0,7)$, G$(2.5,4)$, J$(5,1)$, K$(7.5,4)$, P$(10,7)$.
> 2. $a=3$, $b=\frac{2\pi}{10}=\frac\pi5$, $c=0$, $d=4$. (Cosine starts at a max, so $a>0$ and there's no shift.)
> 3. Positive and increasing. The graph is concave up, and the rates of change are increasing over this interval.

**S.5** *(FRQ 4 style, no calculator)*
1. Solve $2^{x+1}=5$.
2. Rewrite $\ln(x^2)+\ln3-\ln x$ as a single natural logarithm, for $x>0$.
3. Find all solutions of $2\cos^2\theta+3\cos\theta+1=0$.

> [!success]- Answer
> 1. $x+1=\log_25$, so $x=\log_25-1=\frac{\ln5}{\ln2}-1$.
> 2. $\ln\frac{3x^2}{x}=\ln(3x)$.
> 3. Factor: $(2\cos\theta+1)(\cos\theta+1)=0$, so $\cos\theta=-\frac12$ or $-1$. All solutions: $\theta=\frac{2\pi}3+2\pi k$, $\frac{4\pi}3+2\pi k$, or $\pi+2\pi k$, for any integer $k$.

**S.6** Find the inverse of $f(x)=3\cdot2^{x-1}+4$ and state its domain.

> [!success]- Answer
> Swap and solve: $x=3\cdot2^{y-1}+4\Rightarrow\frac{x-4}3=2^{y-1}\Rightarrow f^{-1}(x)=1+\log_2\frac{x-4}3$. Domain: $x>4$ (the range of $f$).

**S.7** Divide $2x^3-3x^2+4x-5$ by $x-2$ using long division.

> [!success]- Answer
> $2x^3\div x=2x^2$; subtract $2x^3-4x^2$ to get $x^2+4x$. Then $x^2\div x=x$; subtract $x^2-2x$ to get $6x-5$. Then $6x\div x=6$; subtract $6x-12$ to get 7.
> Result: $2x^2+x+6+\dfrac{7}{x-2}$.

**S.8** Expand $(x-3)^4$ with the binomial theorem.

> [!success]- Answer
> Row 4 of Pascal's triangle is 1, 4, 6, 4, 1, with $b=-3$:
> $x^4+4(-3)x^3+6(9)x^2+4(-27)x+81=x^4-12x^3+54x^2-108x+81$.

**S.9** Verify the identity $\dfrac{1-\cos^2\theta}{\sin\theta\cos\theta}=\tan\theta$.

> [!success]- Answer
> By the Pythagorean identity $1-\cos^2\theta=\sin^2\theta$, so the left side is $\frac{\sin^2\theta}{\sin\theta\cos\theta}=\frac{\sin\theta}{\cos\theta}=\tan\theta$.

**S.10** For $r=3\sin2\theta$:
1. How many petals does the graph have?
2. On $\left(\frac\pi4,\frac\pi2\right)$, is the point moving toward or away from the pole?
3. On $\left(\frac\pi2,\frac{3\pi}4\right)$, is it moving toward or away from the pole?

> [!success]- Answer
> 1. $n=2$ is even, so $2n=4$ petals.
> 2. $2\theta$ goes from $\frac\pi2$ to $\pi$, so $r$ is positive and decreasing (3 down to 0): **toward** the pole.
> 3. $2\theta$ goes from $\pi$ to $\frac{3\pi}2$, so $r$ is negative and decreasing (0 down to $-3$): $\lvert r\rvert$ grows, so the point moves **away** from the pole.

**S.11** Solve with a matrix inverse: $x+2y=5$, $3x+4y=11$.

> [!success]- Answer
> $A=\begin{bmatrix}1&2\\3&4\end{bmatrix}$, $\det A=4-6=-2$, $A^{-1}=-\frac12\begin{bmatrix}4&-2\\-3&1\end{bmatrix}=\begin{bmatrix}-2&1\\1.5&-0.5\end{bmatrix}$.
> $X=A^{-1}\begin{bmatrix}5\\11\end{bmatrix}=\begin{bmatrix}-10+11\\7.5-5.5\end{bmatrix}=\begin{bmatrix}1\\2\end{bmatrix}$, so $x=1$, $y=2$.

**S.12** Let $g(x)=\begin{cases}x+2,&x<0\\3,&0\le x<2\\(x-3)^2,&x\ge2\end{cases}$. Find $g(-1)$, $g(1)$, and $g(5)$, and state the domain and range of $g$.

> [!success]- Answer
> $g(-1)=1$, $g(1)=3$, $g(5)=4$.
> - Domain: all real numbers (the three intervals cover everything).
> - Range: the first piece gives $y<2$, the middle gives 3, and the parabola on $x\ge2$ gives $y\ge0$ (its vertex is at $x=3$). Together that's all real numbers.
