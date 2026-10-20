# Test 1, Problem 1: Three Point Charges

Three point charges are fixed in the $xy$-plane:

$q_1 = +2q$ at $\vec r_1 = \langle 0,0\rangle$, $q_2 = -3q$ at $\vec r_2 = \langle 4a, 0\rangle$, $q_3 = +4q$ at $\vec r_3 = \langle 0, 3a\rangle$.

1. Find the electric field at $\vec r_1$ due to $q_2$ and $q_3$.
2. Find the $x$ and $y$ components of the net force on $q_1$.
3. Find the net electric field at $P = \langle 4a, 3a\rangle$ due to all three charges.

![[30_three_charges_sketch.svg]]

---

## Recipe

$$\vec E = \frac{kq}{r^2}\,\hat r, \qquad \vec r = \vec r_{\text{field point}} - \vec r_{\text{source}}, \qquad \hat r = \frac{\vec r}{|\vec r|}$$

1. $\vec r$ points **from the source to the field point**
2. Find $|\vec r|$ and $\hat r$
3. Plug in $q$ **with its sign**
4. Add the vectors by components

---

## Part 1: $\vec E$ at $\vec r_1$ from $q_2$ and $q_3$

$$\vec E_{net} = \vec E_{1,2} + \vec E_{1,3}$$

**From $q_2$:**

$$\vec r = \langle 0,0\rangle - \langle 4a,0\rangle = \langle -4a, 0\rangle,\quad r = 4a,\quad \hat r = -\hat x$$

$$\vec E_{1,2} = \frac{k(-3q)}{(4a)^2}(-\hat x) = +\frac{3kq}{16a^2}\,\hat x$$

**From $q_3$:**

$$\vec r = \langle 0,0\rangle - \langle 0,3a\rangle = \langle 0, -3a\rangle,\quad r = 3a,\quad \hat r = -\hat y$$

$$\vec E_{1,3} = \frac{k(4q)}{(3a)^2}(-\hat y) = -\frac{4kq}{9a^2}\,\hat y$$

**Total:**

$$\boxed{\vec E_{net} = \frac{3kq}{16a^2}\,\hat x - \frac{4kq}{9a^2}\,\hat y}$$

---

## Part 2: Force on $q_1$

$$\vec F = q_1 \vec E_{net} = (2q)\left(\frac{3kq}{16a^2}\,\hat x - \frac{4kq}{9a^2}\,\hat y\right)$$

$$\boxed{F_x = \frac{3kq^2}{8a^2}, \qquad F_y = -\frac{8kq^2}{9a^2}}$$

---

## Part 3: $\vec E$ at $P = \langle 4a, 3a\rangle$

$$\vec E_{P} = \vec E_{P,1} + \vec E_{P,2} + \vec E_{P,3}$$

**From $q_1$ ($+2q$ at the origin):**

$$\vec r = \langle 4a, 3a\rangle,\quad r = \sqrt{16a^2 + 9a^2} = 5a,\quad \hat r = \left\langle \tfrac{4}{5}, \tfrac{3}{5}\right\rangle$$

$$\vec E_{P,1} = \frac{k(2q)}{(5a)^2}\left\langle \tfrac{4}{5}, \tfrac{3}{5}\right\rangle = \frac{2kq}{25a^2}\left\langle \tfrac{4}{5}, \tfrac{3}{5}\right\rangle$$

**From $q_2$ ($-3q$ at $(4a,0)$):**

$$\vec r = \langle 0, 3a\rangle,\quad r = 3a,\quad \hat r = \langle 0, 1\rangle$$

$$\vec E_{P,2} = \frac{k(-3q)}{(3a)^2}\langle 0,1\rangle = -\frac{kq}{3a^2}\langle 0,1\rangle$$

**From $q_3$ ($+4q$ at $(0,3a)$):**

$$\vec r = \langle 4a, 0\rangle,\quad r = 4a,\quad \hat r = \langle 1, 0\rangle$$

$$\vec E_{P,3} = \frac{k(4q)}{(4a)^2}\langle 1,0\rangle = \frac{kq}{4a^2}\langle 1,0\rangle$$

**Add by components:**

$$E_x = \frac{8kq}{125a^2} + \frac{kq}{4a^2} = \frac{kq}{a^2}\left(\frac{32}{500} + \frac{125}{500}\right) = \frac{157}{500}\frac{kq}{a^2}$$

$$E_y = \frac{6kq}{125a^2} - \frac{kq}{3a^2} = \frac{kq}{a^2}\left(\frac{18}{375} - \frac{125}{375}\right) = -\frac{107}{375}\frac{kq}{a^2}$$

$$\boxed{\vec E_P = \frac{kq}{a^2}\left\langle \frac{157}{500},\, -\frac{107}{375}\right\rangle }$$