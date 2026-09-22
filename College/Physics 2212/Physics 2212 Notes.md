# Physics 2212A — Electricity & Magnetism: Comprehensive Notes (Weeks 1–5)

*2026-09-22*

These notes consolidate Lectures 1–9 of Physics 2212A (Electricity & Magnetism): vectors and Coulomb's law, the electric field, the electric dipole, polarization of atoms and matter, conductors and insulators, the electric field of continuous charge distributions (lines, rings, disks, sheets, shells, and solid spheres), electric potential energy and potential, the potential of continuous charge distributions, and capacitance and dielectrics.

## 1. Vectors and Coulomb's Law

**Vector basics.** A vector is defined by magnitude and direction.

$$
r = |\vec r| = \sqrt{r_x^2+r_y^2}, \qquad \hat r = \frac{\vec r}{r}, \qquad \vec r = r_x\hat x + r_y\hat y = \langle r_x, r_y, 0\rangle
$$

Components (angle $\theta$ from the x-axis): $r_x = r\cos\theta$, $r_y = r\sin\theta$. The unit vector $\hat r$ always has magnitude 1.

Vector addition (head-to-tail rule): the head of $\vec A$ meets the tail of $\vec B$; $\vec A+\vec B$ runs from the tail of $\vec A$ to the head of $\vec B$.

$$
\vec A+\vec B=(A_x+B_x)\hat x+(A_y+B_y)\hat y
$$

Dot ("scalar") product — the result is a scalar:

$$
\vec A \cdot \vec B = AB\cos\theta = A_xB_x + A_yB_y + A_zB_z
$$

The cross ("vector") product of two vectors is itself a vector; it appears later in the course.

**Electric charge.**
- Charge is an intrinsic, indestructible property of matter. The smallest magnitude of charge is $e = 1.6\times10^{-19}$ C.
- proton: $+e$, electron: $-e$, neutron: $0$.
- A sample with $N_p$ protons and $N_e$ electrons has net charge $q = e(N_p - N_e)$.
- Charge is **conserved**: it is never created or destroyed in ordinary processes (quantum mechanics does allow creation of an electron–proton pair together, e.g. neutron decay $n \to p + e + \bar\nu$, but total charge before and after is unchanged).

**Coulomb's Law.** The force that point charge $q_1$ at $\vec r_1$ exerts on point charge $q_2$ at $\vec r_2$:

$$
\vec F_{21} = k\,q_1 q_2\, \frac{\vec r_2-\vec r_1}{|\vec r_2-\vec r_1|^3} = -\vec F_{12}
$$

with Coulomb's constant $k = 9\times10^9$ N·m²/C². Magnitude, with $R = |\vec r_2-\vec r_1|$:

$$
|\vec F| = \frac{k|q_1q_2|}{R^2}
$$

An inverse-square law, just like Newton's law of gravitation. Like charges repel; opposite charges attract. Coulomb's law obeys Newton's third law ($\vec F_{21} = -\vec F_{12}$) because it depends only on the separation of the two charges, not an arbitrarily chosen origin.

**Superposition of forces.** When several charges $1, 2, \ldots, N$ act on a charge $Q$, the net force is the vector sum of the individual Coulomb forces — never a scalar sum:

$$
\vec F_Q = \vec F_{Q1}+\vec F_{Q2}+\cdots+\vec F_{QN}
$$

**Useful approximation: the binomial approximation.** For any real exponent $n$ and any small $\epsilon$ ($|\epsilon| \ll 1$):

$$
(1+\epsilon)^n \approx 1+n\epsilon
$$

This comes from truncating the full binomial series $(1+\epsilon)^n = 1+n\epsilon+\frac{n(n-1)}{2!}\epsilon^2+\cdots$ after the first-order term, since every higher-order term is smaller by an extra factor of $\epsilon$. It works for any $n$ — positive, negative, fractional — not just positive integers, and it is the single most useful trick for taking a "far away" or "very close" limit anywhere in this course.

**How to use it, step by step.**
1. Identify a large quantity (call it $d$) and a small quantity (call it $s$), with $d \gg s$.
2. Force whatever expression you have into the form $(\text{big})^n(1+\epsilon)^n$ by factoring the large quantity out of every term, leaving $\epsilon = \pm s/d$ (or similar) as the leftover small ratio.
3. Replace $(1+\epsilon)^n$ with $1+n\epsilon$.
4. Distribute and simplify — the leading (zeroth-order) term is often what you already knew, and the interesting physics is in the $n\epsilon$ correction term.

**Worked example: the on-axis dipole field, redone with this tool.** Starting from Section 3's exact expression and factoring $r$ out of each denominator, $(r\mp s/2)^{-2} = r^{-2}(1\mp s/2r)^{-2}$. Apply the rule with $n=-2$ and $\epsilon=\mp s/(2r)$:

$$
\left(1-\frac{s}{2r}\right)^{-2} \approx 1+2\cdot\frac{s}{2r} = 1+\frac{s}{r}, \qquad \left(1+\frac{s}{2r}\right)^{-2} \approx 1-2\cdot\frac{s}{2r} = 1-\frac{s}{r}
$$

$$
\vec E_\parallel(\vec r) = \frac{kq}{r^2}\left[\left(1+\frac{s}{r}\right)-\left(1-\frac{s}{r}\right)\right]\hat r = \frac{kq}{r^2}\cdot\frac{2s}{r}\,\hat r = k\frac{2qs}{r^3}\hat r = k\frac{2\vec p}{r^3}
$$

matching Section 3 exactly — the binomial tool is just a faster, more systematic way to get there than combining the two fractions by hand and canceling.

**Where else this appears in these notes.** The point-charge limit of the disk's potential (Section 11.2) is the $n=1/2$ case of the same rule, applied to $\sqrt{z^2+R^2}=|z|(1+R^2/z^2)^{1/2}\approx|z|\left(1+\tfrac{1}{2}\tfrac{R^2}{z^2}\right)$. Any time you see a "far field" ($r \gg$ the object's size) or "close-up" limit taken in these notes, this is the tool doing the work under the hood.

## 2. The Electric Field

**Faraday's idea.** The total Coulomb force on a charge $Q$ sitting at point $P$ is

$$
\vec F_Q = Q\,\vec E(P)
$$

where $\vec E(P)$ is the electric field at $P$ produced by *every other* charge in the world — it exists whether or not $Q$ is actually there.

**Field of a point charge** (rewriting Coulomb's law with the source charge at the origin):

$$
\vec E(\vec r) = \frac{kq}{r^2}\hat r
$$

**Two equivalent pictures:** the length of the $\vec E$-vector at a point, or the density of field lines there, is proportional to the field's magnitude.

**Rotational symmetry.** A point charge looks identical after any rotation about any axis through it, so its field must too: the direction is purely radial and the magnitude depends only on $r$, $\vec E(\vec r) = E(r)\,\hat r$. This symmetry argument is used throughout the course to guess a field's *direction* before doing any integral.

**Field-line rules** (true always, not just for point charges):
- Lines begin on positive charge (or at infinity).
- Lines end on negative charge (or at infinity).

**Superposition of fields.** The field at any point is the vector sum of the fields produced by each source charge separately:

$$
\vec E(P) = \vec E_1(P)+\vec E_2(P)+\cdots
$$

Inserting a charge $Q$ at $P$ afterward simply gives $\vec F_Q = Q\vec E(P)$; the presence of $Q$ does not change $\vec E(P)$ itself.

**Far-field theorem (charged objects).** Viewed from far away ($r \gg s$, the object's size), *any* object with nonzero net charge $Q$ behaves electrically just like a point charge:

$$
\vec E(\vec r) \approx \frac{kQ}{r^2}\hat r \qquad (r\gg s)
$$

**Do neutral ($Q=0$) objects produce a field?** The $1/r^2$ far-field above vanishes for $Q=0$, but that does not mean $\vec E = 0$ everywhere — it depends on whether the object has internal charge separation:
- An isolated **atom**: no separation of + and − on opposite sides → $\vec E_{atom}(\vec r) = 0$ everywhere.
- A **water molecule**: O is more electronegative than H, pulling electron density toward itself → there *is* separation → $\vec E_{molecule}(\vec r) \neq 0$, even though $Q_{total}=0$.

The prototype charge-neutral, charge-separated object is the **electric dipole** (Section 3), which explains this behavior quantitatively.

## 3. The Electric Dipole

Two charges $-q$ and $+q$ separated by a small distance $s$ form the prototype charge-neutral, charge-separated object.

**Dipole moment vector:** points from $-q$ to $+q$, magnitude $p=qs$. In general, for any collection of charges,

$$
\vec p = \sum_{k=1}^N q_k \vec r_k
$$

(for the two-charge dipole this reduces to $\vec p = qs\,\hat x$ along the separation direction).

**On the symmetry axis** (parallel field), superposing the $+q$ and $-q$ point-charge fields and taking $r \gg s$:

$$
\vec E_\parallel(\vec r) = k\left[\frac{q}{(r-s/2)^2}-\frac{q}{(r+s/2)^2}\right]\hat r \;\approx\; k\,\frac{2\vec p}{r^3}
$$

**On the perpendicular bisector**, $r \gg s$:

$$
\vec E_\perp(\vec r) \approx -k\,\frac{\vec p}{r^3}
$$

Both fall off as **$1/r^3$** (inverse cube) — steeper than the $1/r^2$ of a single point charge. This $1/r^3$ behavior is the signature of a dipole field.

**General dipole field**, valid at any point $\vec r$ (any angle between $\vec p$ and $\hat r$):

$$
\vec E(\vec r) = k\,\frac{3(\vec p\cdot\hat r)\hat r - \vec p}{r^3}
$$

Check: $\hat r \perp \vec p$ gives $\vec E = -k\vec p/r^3 = \vec E_\perp$; $\hat r \parallel \vec p$ gives $\vec E = k(3\vec p-\vec p)/r^3 = 2k\vec p/r^3 = \vec E_\parallel$ — consistent with the two limits above.

**Far-field theorem for any neutral object.** Far away ($r \gg s$) from *any* object with zero net charge ($Q=0$) but nonzero dipole moment ($\vec p \neq 0$), the field is exactly the dipole field above, using $\vec p = \sum q_k \vec r_k$ computed from the object's own charges. This is why a neutral water molecule still produces a nonzero field far away, while a neutral atom (no charge separation, $\vec p = 0$) does not.

**Other useful facts:** superposition still applies when combining a dipole's field with a point charge's field or with another dipole's field; field lines still begin on + charge and end on − charge.

## 4. Polarization of Atoms, Molecules, and Matter

**Induced polarization (nonpolar atoms/molecules).** An external field $\vec E_{ext}$ displaces + and − charge in opposite directions inside a neutral atom or a nonpolar molecule (e.g. N₂), creating an induced dipole moment

$$
\vec p = \alpha\,\vec E_{ext}
$$

$\alpha$ is the atomic/molecular **polarizability** (species-dependent, tabulated in handbooks). $\vec p \to 0$ as soon as $\vec E_{ext} \to 0$.

**Permanent polarization (polar molecules).** Chemical bonding alone, with no external field, separates charge in molecules like H₂O: O is more electronegative than H and pulls electron density toward itself, producing a **permanent** dipole moment $\vec p_{mol}$ even when $\vec E_{ext}=0$.

**Dipole–dipole interaction.** Two antiparallel dipoles (e.g. two oppositely oriented water molecules) attract overall: the stronger near-end attraction beats the weaker, more distant repulsion.

**Force between a point charge and an induced dipole.** A charge (e.g. an electron) at distance $d$ from a nonpolar molecule induces $\vec p = \alpha\vec E_O$ in it; by Newton's third law the molecule pulls back on the charge with

$$
\vec F_O = -\frac{2\alpha k^2 e^2}{d^5}\hat x
$$

an attractive force falling off as **$1/d^5$** — steeper than Coulomb's $1/d^2$ because one "charge" is only induced, not fixed.

**How a bulk insulator polarizes.** Every atom acquires $\vec p_{atom} = \alpha\vec E_{ext}$. The + and − charges at the touching ends of neighboring polarized atoms cancel throughout the bulk; only the front and back surfaces keep net charge $\pm Q$. The whole body's dipole moment is therefore

$$
\vec p_{body} = \sum_{\text{atom}} \vec p_{atom} = Q\vec s
$$

i.e. equivalent to charges $\pm Q$ separated by the body's thickness $\vec s$.

**Field inside a polarized insulator.** The surface polarization charges create a field $\vec E_{pol}$ that opposes (partially cancels) $\vec E_{ext}$:

$$
\vec E_{inside} = \vec E_{ext}+\vec E_{pol} = \vec E_{ext} - |\vec E_{pol}| = \frac{\vec E_{ext}}{\kappa}
$$

$\kappa > 1$ is the **dielectric constant**: $E_{inside}$ stays parallel to $E_{ext}$ but is reduced in magnitude (contrast a conductor, Section 5, where the cancellation is complete).

**Conductors vs. insulators, microscopically.**
- Insulator: every electron is bound to one particular atom.
- Conductor: valence electrons migrate freely from atom to atom.

**Charging methods (static electricity).**
- *Frictional rubbing* transfers electrons between two initially neutral insulators (glass+silk, amber+wool); the two objects end up with equal and opposite charge. A rough triboelectric ranking (loses electrons → gains electrons): human skin, glass, wool, cat fur, wood, silk, amber, rubber, styrofoam.
- *Charging a conductor by contact*: touching a charged insulating rod to a neutral conducting sphere transfers charge, which then spreads over the sphere's surface.
- *Charging by polarization/induction*: bring a charged rod near two touching neutral conductors (polarizing them), separate the two conductors while the rod is still nearby, then remove the rod — the result is two conductors with equal and opposite charge, and the rod is unchanged.
- *Grounding*: connecting a charged conductor to Earth lets charge flow until it is neutralized. This happens spontaneously because it lowers the electrostatic energy of the whole system.

## 5. Conductors: E = 0 Inside, and Shielding

**The conductor's "superpower."** In electrostatic equilibrium, $\vec E = 0$ at every point inside a conductor's material — always, regardless of the charges outside or in a cavity. Mobile charges rearrange on the surface(s) until the field they create exactly cancels any external field throughout the interior:

$$
\vec E_{inside} = \vec E_{ext} + \vec E_{pol} = 0 \quad\Rightarrow\quad |\vec E_{pol}| = |\vec E_{ext}|
$$

Contrast an insulator (Section 4), where $\vec E_{pol}$ only partially cancels $\vec E_{ext}$, leaving $E_{inside} = E_{ext}/\kappa \neq 0$.

**Polarization of an oddly shaped conductor.** Surface charge distributes itself (not necessarily uniformly) so that $\vec E = 0$ everywhere inside the solid conductor, no matter its shape or how many external charges sit nearby.

**Shielding (Faraday-cage effect).** If a cavity is scooped out of a conductor, the surface charge still arranges itself so that $\vec E = 0$ throughout the solid conductor material — and, remarkably, $\vec E = 0$ throughout the empty cavity as well, as long as no charge sits inside the cavity itself. This is why a conducting shell shields its interior from outside fields.

**Worked conceptual examples.**
- Two point charges placed symmetrically around the center $C$ of a solid metal cube: $E(C) = 0$, simply because $C$ sits inside conductor material.
- A dipole $\vec p$ held outside a solid **metal** cube at perpendicular distance $d$ from center $C$ polarizes the cube. Because $E_{inside}$ must be zero, the cube's own field at $C$ must exactly cancel the dipole's field there: $\vec E_{cube}(C) = -\vec E_{dipole}(C) = +k\vec p/d^3$ (using $E_\perp = -k\vec p/d^3$ for this perpendicular geometry).
- The same dipole outside a **plastic** (insulating) cube instead: the cube still polarizes and makes its own field $\vec E_{cube}(\vec r)$, but nothing forces it to cancel the dipole's field, so $\vec E_{total}(C) = \vec E_{dipole}(C) + \vec E_{cube}(C) \neq 0$ in general — the defining difference between a conductor and an insulator.
- A positive point charge embedded at the center of an insulating sphere, itself coated with a thick conducting shell: the shell's *outer* surface acquires charge equal in sign and magnitude to the embedded charge, because $\vec E = 0$ must hold everywhere inside the metal.

## 6. Continuous Charge Distributions

Real objects spread their charge over a volume, surface, or line rather than concentrating it at isolated points. Define a charge density so that $dq$ is the charge in an infinitesimal volume, area, or length element:

$$
\text{volume: } \rho(\vec r)=\frac{\Delta q}{\Delta V}\ (dq=\rho\,dV), \qquad \text{surface: } \sigma=\frac{\Delta q}{\Delta A}\ (dq=\sigma\,dA), \qquad \text{line: } \lambda=\frac{\Delta q}{\Delta \ell}\ (dq=\lambda\,d\ell)
$$

For a uniform density, the charge $Q_0$ contained in a sub-volume $V_0$ of a total volume $V$ carrying total charge $Q$ is $Q_0 = \rho V_0 = QV_0/V$.

**General superposition integral.** Treat the distribution as a continuum of point charges $dq$ and integrate the point-charge field over the whole source:

$$
\vec E(\vec r) = \int d\vec E = k\int \frac{\vec r-\vec r_q}{|\vec r-\vec r_q|^3}\,dq
$$

Convert $dq$ using the density appropriate to the geometry ($\rho$, $\sigma$, or $\lambda$) and the geometry's coordinate variables **before** integrating. Because the terms being summed are vectors pointing in different directions, this integral is only tractable by hand for distributions with enough symmetry — line, ring, disk, sheet, or sphere (Section 7).

**Far-field theorem still applies.** If the total charge $Q = \int\rho\,dV \neq 0$, then far from the object ($r \gg$ its size) $\vec E(\vec r) \approx (kQ/r^2)\hat r$, exactly as for a point charge.

## 7. Field of Standard Charge Distributions

### 7.1 Uniformly charged rod (length $L$, charge $q$, $\lambda = q/L$)

Divide the rod into segments $dq = \lambda\,dy$, each acting as a point charge, and integrate. Along the perpendicular midline $(x,0)$, the $y$-components cancel by up–down symmetry, leaving only

$$
E_x(x,0) = \frac{kq}{x\sqrt{x^2+(L/2)^2}}, \qquad E_y(x,0)=0
$$

- **Far** from the rod ($x \gg L$): $E_x \to kq/x^2$ — the far-field theorem.
- **Close** to the rod, or equivalently an **infinite line charge** with linear density $\lambda$:

$$
\vec E(\vec s) = \frac{2k\lambda}{s}\,\hat s
$$

($\vec s$ points radially outward from the line's axis) — falls off as **$1/s$**, not $1/s^2$.

### 7.2 Uniformly charged ring (radius $R$, charge $q$), on-axis at height $z$

By symmetry, the radial (perpendicular) components from opposite ring elements cancel; only the axial component survives. With $dq = \lambda\,ds = (q/2\pi)\,d\phi$:

$$
E_z(z)=\frac{kqz}{(z^2+R^2)^{3/2}}
$$

- Far away ($z \gg R$): $E_z \to kq/z^2$ (far-field theorem).
- $E_z(z)$ is continuous everywhere, zero at $z=0$, and peaks at a finite $z$ — no discontinuity for a ring.

### 7.3 Uniformly charged disk (radius $R$, $\sigma = q/\pi R^2$), on-axis

Build the disk from concentric rings of radius $r$, width $dr$, charge $dq = \sigma\cdot2\pi r\,dr$, and sum their on-axis fields:

$$
E_z(z)=kz\int_0^R \frac{\sigma\,2\pi r}{(z^2+r^2)^{3/2}}\,dr = 2\pi k\sigma\left[\frac{z}{|z|}-\frac{z}{\sqrt{z^2+R^2}}\right]
$$

- $E_z(z)$ is **discontinuous** at $z=0$ (jumps from $-2\pi k\sigma$ to $+2\pi k\sigma$): $E$ is always discontinuous when the observation point crosses an infinitesimally thin charged surface.

### 7.4 Infinite flat sheet of charge ($\sigma$)

Taking $z \ll R$ in the disk result (equivalently $R \to \infty$):

$$
E_z(z) = 2\pi k\sigma\,\frac{z}{|z|} = \begin{cases}+2\pi k\sigma & z>0\\-2\pi k\sigma & z<0\end{cases}
$$

The field is **uniform**: magnitude $|E|=2\pi k\sigma$ on both sides, pointing away from the sheet (toward it if $\sigma<0$), and independent of distance from the sheet.

### 7.5 Two parallel infinite sheets, charges $+\sigma$ and $-\sigma$

Superposing the two sheet fields ($2\pi k\sigma$ each):

$$
E_{\text{between}} = 4\pi k\sigma\ \text{(fields add)}, \qquad E_{\text{outside both}} = 0\ \text{(fields cancel)}
$$

This is the idealized **parallel-plate capacitor**: a uniform field $E_{in}=4\pi k\sigma$ exists only between the plates; $E_{out}=0$ everywhere outside.

### 7.6 Hollow spherical shell of charge (radius $R$, total charge $Q$, $\sigma=Q/4\pi R^2$)

Spherical symmetry plus the far-field theorem (must look like a point charge $Q$ far away, and symmetry allows no other possibility close in):

$$
\vec E_{\text{out}}(r) = \frac{kQ}{r^2}\hat r\ (r>R), \qquad \vec E_{\text{in}}(r) = 0\ (r<R)
$$

- **Discontinuous** at $r=R$ (jumps from $0$ to $kQ/R^2$), again because the shell is an infinitesimally thin charged surface. (A full proof of $E_{in}=0$ by direct integration is possible but harder; it follows quickly later in the course from Gauss's law.)

### 7.7 Solid uniformly charged ball (radius $R$, total charge $Q$, $\rho = Q/(\tfrac{4}{3}\pi R^3)$)

Outside, the same far-field/symmetry argument as the shell:

$$
\vec E_{\text{out}}(r) = \frac{kQ}{r^2}\hat r\quad (r>R)
$$

Inside, build the ball from nested shells: the inner sphere of radius $r<R$ (enclosed charge $Q(r)=Qr^3/R^3$) acts like a point charge, while every shell of material *outside* radius $r$ contributes zero field there (Section 7.6). So

$$
\vec E_{\text{in}}(r) = \frac{kQ(r)}{r^2}\hat r = \frac{kQ}{R^3}\,r\,\hat r\quad (r<R)
$$

$E_{in}$ grows **linearly** with $r$ and matches $E_{out}=kQ/R^2$ exactly at $r=R$ — **no discontinuity**, because charge is spread through a volume rather than concentrated on an infinitesimally thin surface.

**Pattern to remember:** $E$ is discontinuous crossing an infinitesimally thin charged surface (disk, sheet, shell); $E$ is continuous when charge fills a 3D volume (solid ball).

## 9. Work, Energy, and Electric Potential Energy

**Work done by a force** (brief review from mechanics). The work done by a force $\vec F(\vec r)$ as an object moves from $\vec r_i$ to $\vec r_f$ is a line integral:

$$
W_F = \int_{\vec r_i}^{\vec r_f} \vec F(\vec r)\cdot d\vec r
$$

$dW_F>0$ when $\vec F$ and $d\vec r$ point more in the same direction than opposite (the force helps the motion); $dW_F<0$ when they point more opposite than the same (the force resists the motion).

**Conservation of total energy.** The work–kinetic-energy theorem says the work integral above equals $K_f-K_i=\Delta K$. Potential energy $U$ is *defined* so that $-\Delta U$ equals that same work integral:

$$
U(\vec r_f)-U(\vec r_i) = -\int_{\vec r_i}^{\vec r_f}\vec F(\vec r)\cdot d\vec r = W_F = \Delta K
$$

Total energy $E=K+U$ is then conserved: $\Delta E=0 \Rightarrow \Delta K=-\Delta U$.

**Applying this to the electric force.** For a point charge $q$, $\vec F(\vec r)=q\vec E(\vec r)$, so

$$
U(\vec r_f)-U(\vec r_i) = -\int_{\vec r_i}^{\vec r_f} q\,\vec E(\vec r)\cdot d\vec r
$$

**Defining the electric potential.** Dividing both sides by $q$ and defining $V(\vec r)\equiv U(\vec r)/q$ removes the test charge from the equation entirely:

$$
V(\vec r_f)-V(\vec r_i) = -\int_{\vec r_i}^{\vec r_f}\vec E(\vec r)\cdot d\vec r, \qquad U(\vec r)=qV(\vec r)
$$

$V(\vec r)$ depends only on the source charges (through $\vec E$), never on the test charge $q$ — this is what makes it so useful, exactly parallel to how $\vec E(\vec r)$ let us remove $Q$ from Coulomb's law in Section 2.

## 10. Electric Potential $V(\vec r)$

**Units.** $V=U/q$ has units of joule/coulomb, named the **volt** (after Alessandro Volta, inventor of the battery):

$$
[V] = \frac{[U]}{[q]} = \frac{\text{joule}}{\text{coulomb}} = \text{volt}
$$

**Two ways to move between $\vec E$ and $V$.** If you know the field, integrate it to get potential differences; if you know the potential, differentiate it to get the field:

$$
V(\vec r_2)-V(\vec r_1) = -\int_{\vec r_1}^{\vec r_2} \vec E\cdot d\vec r \qquad\text{(field known)}
$$

$$
E_x = -\frac{\partial V}{\partial x}, \qquad E_y = -\frac{\partial V}{\partial y}, \qquad E_z = -\frac{\partial V}{\partial z} \qquad\text{(potential known)}
$$

The second line follows from writing $dV=-E_xdx-E_ydy-E_zdz$ (from the definition of work) and comparing it with the ordinary calculus expression for $dV$ in terms of partial derivatives. In short: calculate the scalar function $V(\vec r)$ from the source charges, then take derivatives to get $\vec E(\vec r)$ — often much easier than the vector superposition integral for $\vec E$ directly, because $V$ is a single scalar function instead of three components pointing in different directions.

**$V(\vec r)$ for a point charge at the origin.** Choose a path from $\vec r_1$ to $\vec r_2$ built only from radial segments (where $d\vec r \parallel \hat r$, so $\hat r\cdot d\vec r = dr$) and circular arcs (where $d\vec r \perp \hat r$, so $\hat r\cdot d\vec r = 0$). Only the radial segments contribute:

$$
V(\vec r_2)-V(\vec r_1) = -\int_{\vec r_1}^{\vec r_2} k\frac{q}{r^2}\hat r\cdot d\vec r = -\int_{r_1}^{r_2} k\frac{q}{r^2}\,dr = \frac{kq}{r_2}-\frac{kq}{r_1}
$$

Choosing the reference point at infinity ($V(\infty)=0$) gives the standard result:

$$
V(\vec r) = \frac{kq}{r}
$$

**Check by working backward.** Differentiating $V(r)=kq/r$ with respect to $x,y,z$ (using $r=\sqrt{x^2+y^2+z^2}$) reproduces exactly the point-charge field:

$$
E_x = -\frac{\partial}{\partial x}\frac{kq}{r} = \frac{kq}{r^3}x, \ \text{similarly for } E_y,E_z \quad\Rightarrow\quad \vec E(\vec r)=\frac{kq}{r^3}\vec r=\frac{kq}{r^2}\hat r
$$

**Path independence of $\Delta V$.** Any path at all from $\vec r_1$ to $\vec r_2$ can be decomposed into radial and circular segments, so the same result holds no matter which path you integrate along — this is not special to point charges, it is always true for an electrostatic field.

**Consequence: closed loops.** Going from $A$ to $B$ along one path and back along a different path must give contributions that cancel:

$$
\oint \vec E(\vec r)\cdot d\vec r = 0 \qquad\text{around any closed loop}
$$

**Superposition for $V(\vec r)$.** Unlike the field, which sums as vectors, the potential from $N$ point charges sums as ordinary scalars — no components, no directions to track:

$$
V(\vec r) = \sum_{i=1}^N \frac{kq_i}{r_i}, \qquad r_i=|\vec r-\vec r_i|
$$

This scalar superposition is one of the biggest practical advantages of working with $V$ instead of $\vec E$.

**Worked example: two equal positive charges.** Two point charges $q,q$ (both positive, equal magnitude) hang symmetrically apart. At point $P$ on the line joining them, $V(P)=kq/r_1+kq/r_2 \ge 0$ always — it can equal zero only infinitely far from both charges. Contrast this with $\vec E$ for the same configuration: $\vec E$ *can* be zero at a finite point (e.g. the midpoint between two equal charges) because it adds as vectors that can cancel, while $V$ adds as scalars that, for same-sign charges, never cancel at any finite distance.

## 11. Electric Potential of Continuous Charge Distributions

**General integral.** Exactly as with the field, treat the distribution as a continuum of point charges $dq$ and sum the point-charge potential over the whole source. Because potential is a scalar, this integral has no components to track:

$$
V(\vec r) = \sum_{i=1}^N \frac{kq_i}{|\vec r-\vec r_i|} \quad\Rightarrow\quad V(\vec r) = \int \frac{k\,dq}{|\vec r-\vec r_{dq}|}
$$

where $\vec r_{dq}$ points from the origin to the element of charge $dq$.

### 11.1 Uniformly charged ring (radius $R$, charge $Q$), on-axis at height $z$

Every element $dq$ is the same distance $r=\sqrt{z^2+R^2}$ from the on-axis point, so it factors straight out of the integral:

$$
dV = k\frac{dq}{r} = k\frac{dq}{\sqrt{z^2+R^2}} \quad\Rightarrow\quad V(z)=\int dV = \frac{k}{\sqrt{z^2+R^2}}\int dq = \frac{kQ}{\sqrt{z^2+R^2}}
$$

Differentiating recovers the on-axis ring field from Section 7.2, confirming consistency between the two methods:

$$
E_z(z) = -\frac{dV}{dz} = \frac{kQz}{(z^2+R^2)^{3/2}}
$$

### 11.2 Uniformly charged disk (radius $R$, $\sigma=Q/\pi R^2$), on-axis

Treat every annular ring of radius $r$, width $dr$, charge $dq=\sigma\,dA=\sigma(2\pi r\,dr)$ as a ring source and sum the potentials of all such rings from $r=0$ to $r=R$:

$$
dV = k\frac{dq}{\sqrt{z^2+r^2}} = k\sigma\frac{2\pi r\,dr}{\sqrt{z^2+r^2}}
$$

$$
V(z) = 2\pi k\sigma \int_0^R \frac{r\,dr}{\sqrt{z^2+r^2}} = 2\pi k\sigma\left[\sqrt{z^2+R^2}-|z|\right]
$$

**$V$ is continuous, $E$ is not.** $V(z)$ has no jump at $z=0$ ($V$ is *always* continuous crossing an infinitesimally thin charged surface, even though it has a kink — a discontinuous slope — there). Differentiating gives back the disk field from Section 7.3, which *is* discontinuous at $z=0$:

$$
E_z(z) = -\frac{dV}{dz} = 2\pi k\sigma\left[\frac{z}{|z|}-\frac{z}{\sqrt{z^2+R^2}}\right]
$$

**Infinite-plane limit ($z \ll R$).** Approximating $\sqrt{z^2+R^2}\approx R$:

$$
V(z) \approx 2\pi k\sigma\left[R-|z|\right] = 2\pi k\sigma R - 2\pi k\sigma|z| \quad\Rightarrow\quad E_z(z) = -\frac{dV}{dz} = \pm 2\pi k\sigma
$$

matching the infinite-sheet field from Section 7.4. ($V$ itself grows without bound as the sheet's radius grows, which is why an infinite sheet has no well-defined $V(\infty)=0$ reference — only $\vec E$ is well-behaved in that limit.)

**Point-charge limit ($z \gg R$).** Write $\sqrt{z^2+R^2}=|z|\sqrt{1+R^2/z^2}$ and Taylor-expand $\sqrt{1+x}\approx 1+x/2$:

$$
V(z) = 2\pi k\sigma\left[|z|\sqrt{1+\tfrac{R^2}{z^2}}-|z|\right] \approx 2\pi k\sigma\,|z|\left(1+\tfrac{1}{2}\tfrac{R^2}{z^2}\right)-2\pi k\sigma|z| = 2\pi k\sigma\,\frac{R^2}{2|z|} = \frac{kQ}{|z|}
$$

(using $Q=\sigma\pi R^2$) — the far-field theorem again, this time for the potential.

### 11.3 Hollow spherical shell (radius $R$, total charge $Q$)

Outside ($r>R$): $\vec E_{out}(r)$ is identical to the field of a point charge $Q$, and both $r$ and $\infty$ are outside the shell, so $V_{out}(r)$ equals the point-charge potential:

$$
V_{\text{out}}(r) = \frac{kQ}{r} \qquad (r>R)
$$

Inside ($r<R$): since $E_{in}(r)=0$ everywhere inside (Section 7.6), the integral of $\vec E_{in}$ between any two interior points is zero, so $V$ is *constant* throughout the interior. Matching that constant to $V_{out}$ at the boundary $r=R$ gives:

$$
V_{\text{in}}(r) = \frac{kQ}{R} \qquad (r<R,\ \text{constant})
$$

So $E$ jumps discontinuously at $r=R$ while $V$ is continuous there (matching at the boundary) but has a kink, consistent with $E=-dV/dr$ jumping.

### 11.4 Solid uniformly charged ball (radius $R$, total charge $Q$) — supplementary

Outside ($r>R$), the same reasoning as the shell gives $V_{out}(r)=kQ/r$. Inside, integrating $E(r)$ inward from infinity (using $E_{in}(r)=kQr/R^3$ from Section 7.7) gives:

$$
V_{\text{in}}(r) = \frac{kQ}{2R}\left(3-\frac{r^2}{R^2}\right) \qquad (r<R)
$$

This matches $V_{out}(R)=kQ/R$ at the boundary (plug in $r=R$: $\tfrac{kQ}{2R}(3-1)=kQ/R$) and peaks at the center with $V_{in}(0)=3kQ/2R$. Like the shell, $E$ has no jump for a solid ball (Section 7.7), and here $V$ is smooth throughout with no kink at all.

## 12. Capacitance and Dielectrics

**Ideal parallel-plate capacitor.** Two oppositely charged infinite sheets ($+\sigma$ and $-\sigma$) separated by a gap of length $\ell$ produce a uniform field $E=4\pi k\sigma$ between them (Section 7.5). Integrating along the straight path from the $+$ plate ($x=0$) to the $-$ plate ($x=\ell$):

$$
\Delta V = V_- - V_+ = -\int_0^{\ell} E\hat x \cdot dx\,\hat x = -E\ell
$$

$$
\Delta V = -4\pi k\sigma \ell = -\frac{Q}{C}, \qquad C \equiv \frac{Q}{|\Delta V|} = \frac{Q}{4\pi k(Q/A)\ell} = \frac{A}{4\pi k\ell}
$$

$C$ is called the **capacitance** of this two-plate system: a purely geometric quantity (area $A$, plate separation $\ell$) that tells you how much charge $Q$ the plates hold per volt of potential difference.

**A real parallel-plate capacitor.** Real metal plates of area $A$ carrying charge $Q$ (so $\sigma=Q/A$) reproduce the ideal picture in the bulk — $E_{in}\approx4\pi k\sigma$ between the plates, $E_{out}\approx0$ outside them, and $E=0$ inside the metal of the plates themselves (Section 5) — except near the edges, where field lines bulge outward as a **fringe field**, a real-world deviation from the idealized uniform-field picture.

**Dielectric constant of common materials** ($\kappa$, dimensionless):

| Material | $\kappa$ |
| --- | --- |
| Vacuum | 1.0000 |
| Air (1 atm) | 1.0006 |
| Paraffin | 2.2 |
| Polystyrene | 2.6 |
| Vinyl (plastic) | 2–4 |
| Paper | 3.7 |
| Quartz | 4.3 |
| Oil | 4 |
| Glass, Pyrex | 5 |
| Rubber, neoprene | 6.7 |
| Porcelain | 6–8 |
| Mica | 7 |
| Water (liquid) | 80 |
| Strontium titanate | 300 |

**Inserting a dielectric.** Slipping an insulator between the charged plates polarizes it exactly as in Section 4: the induced surface charge creates a field that partially cancels the plates' field, so the field inside the dielectric is reduced:

$$
E_\kappa = \frac{E}{\kappa}
$$

**Potential and capacitance with a dielectric.** The potential difference across the gap shrinks in proportion:

$$
|\Delta V| = E\ell \quad(\text{no dielectric}), \qquad |\Delta V_\kappa| = E_\kappa\ell = \frac{E}{\kappa}\ell \quad(\text{with dielectric})
$$

Since $C=Q/|\Delta V|$ and $\Delta V$ dropped by a factor of $\kappa$ while $Q$ stayed the same:

$$
C_\kappa = \frac{Q}{|\Delta V_\kappa|} = \kappa C > C
$$

Inserting a dielectric between the plates of a capacitor always increases its capacitance.

**Potential across a conductor.** Because $\vec E(\vec r)=0$ everywhere inside a conductor in electrostatic equilibrium (Section 5), the potential difference between any two points $i$ and $f$ inside (or on the surface of) the conductor is:

$$
V_f - V_i = -\int_{\vec r_i}^{\vec r_f} \vec E(\vec r)\cdot d\vec r = 0
$$

So $V(\vec r)=\text{constant}$ everywhere inside and on the surface of a conductor in equilibrium. (This is no longer true once electric current flows through a conductor — a preview of circuits, covered later in the course.)

## 13. Worked Conceptual Examples

**Electron moving in the direction of $\vec E$ between charged sheets.** An electron travels from point $A$ to point $B$ in the direction of the field between two parallel infinite sheets with surface charges $+\sigma$ and $-\sigma$. Because the electron's charge is negative, the force on it points opposite to $\vec E$, so it decelerates: $\Delta K<0$. Since total energy is conserved ($\Delta K+\Delta U=0$), $\Delta U>0$ by exactly the same amount.

**Field between two stacked parallel-plate pairs.** Four parallel sheets are stacked in the order $+\sigma,-\sigma,+\sigma,-\sigma$. At a point between the second sheet ($-\sigma$) and the third sheet ($+\sigma$) — between the two capacitor-like pairs — the fields from every sheet superpose to exactly zero: a direct application of superposition (Section 2) to more than two sheets, showing that stacking oppositely oriented plate-pairs back to back can produce field-free regions between them.

**$E$ at the center of a shell, due to a nearby charged ball.** A charged hollow shell (total charge $Q_1$) and a charged solid ball (total charge $Q_2$) have centers separated by distance $d$. The total field at the shell's own center is the vector sum of two contributions: the field the shell produces at its own center, which is exactly zero (Section 7.6), and the field the ball produces there, which is that of a point charge $Q_2$ at distance $d$: $kQ_2/d^2$. So the net field at the shell's center is simply $kQ_2/d^2$ — a clean illustration of how a shell's zero self-field simplifies superposition problems.

**Potential $V_A$ from three point charges at corners of a rectangle.** Charges $Q_1$ (positive), $Q_2$ (negative), and $Q_3$ (positive) sit at three corners of a rectangle with side lengths $x$ and $y$; point $A$ is the fourth corner, diagonally opposite $Q_2$. Using scalar superposition (Section 10) with the correct distance to each charge — $x$ from $Q_1$, the diagonal $\sqrt{x^2+y^2}$ from $Q_2$, and $y$ from $Q_3$ — and keeping the signs of the charges explicit:

$$
V_A = \frac{kQ_1}{x} - \frac{kQ_2}{\sqrt{x^2+y^2}} + \frac{kQ_3}{y}
$$

The lesson: each term uses the straight-line distance from that specific charge to point $A$ (not a shared distance), and the algebraic sign of each charge carries straight through since $V$ superposition is a plain scalar sum.

## 14. Quick-Reference Formula Sheet

Constants: $e = 1.6\times10^{-19}$ C, $k = 9\times10^9$ N·m²/C².

### 14.1 Coulomb's Law, Fields, and Forces

| Concept | Formula |
| --- | --- |
| Coulomb's Law | $\vec F_{21} = kq_1q_2\,\dfrac{\vec r_2-\vec r_1}{\lVert\vec r_2-\vec r_1\rVert^3}$ |
| Field of a point charge | $\vec E(\vec r) = \dfrac{kq}{r^2}\hat r$ |
| Force from a field | $\vec F = Q\vec E$ |
| Far-field, net charge $Q$ | $\vec E \approx \dfrac{kQ}{r^2}\hat r$, for $r\gg s$ |

### 14.2 Electric Dipole

| Concept                     | Formula                                                              |
| --------------------------- | -------------------------------------------------------------------- |
| Dipole moment               | $\vec p = qs$ (points $-q\to+q$); general: $\vec p=\sum q_k\vec r_k$ |
| Dipole field, on-axis       | $\vec E_\parallel \approx k\dfrac{2\vec p}{r^3}$                     |
| Dipole field, ⊥ bisector    | $\vec E_\perp \approx -k\dfrac{\vec p}{r^3}$                         |
| Dipole field, general point | $\vec E(\vec r) = k\dfrac{3(\vec p\cdot\hat r)\hat r-\vec p}{r^3}$   |

### 14.3 Polarization, Conductors, and Insulators

| Concept | Formula |
| --- | --- |
| Induced dipole moment | $\vec p = \alpha\vec E_{ext}$ |
| Force: point charge on induced dipole | $F_O = -2\alpha k^2 e^2/d^5$ (attractive, toward the charge) |
| Bulk insulator dipole moment | $\vec p_{body} = Q\vec s$ |
| Field inside a polarized insulator | $E_{inside}=E_{ext}/\kappa$ ($\kappa>1$, dielectric constant) |
| Conductor polarization condition | $\vec E_{pol}=-\vec E_{ext}$, so $\lvert\vec E_{pol}\rvert=\lvert\vec E_{ext}\rvert$ |
| Field inside a conductor | $E_{inside}=0$ (always) |
| Potential inside a conductor | $V=\text{constant}$ (everywhere inside and on the surface) |

### 14.4 Continuous Charge Distributions (Field)

| Concept                          | Formula                                                                              |
| -------------------------------- | ------------------------------------------------------------------------------------ |
| Charge density definitions       | $\rho=\Delta q/\Delta V$; $\sigma=\Delta q/\Delta A$; $\lambda=\Delta q/\Delta\ell$  |
| Infinite line charge             | $\vec E(\vec s) = \dfrac{2k\lambda}{s}\hat s$                                        |
| Ring, on-axis                    | $E_z = \dfrac{kqz}{(z^2+R^2)^{3/2}}$                                                 |
| Disk, on-axis                    | $E_z = 2\pi k\sigma\left[\dfrac{z}{\lvert z\rvert}-\dfrac{z}{\sqrt{z^2+R^2}}\right]$ |
| Infinite sheet                   | $E = 2\pi k\sigma$ (uniform, both sides)                                             |
| Parallel-plate capacitor (field) | $E_{in}=4\pi k\sigma$; $E_{out}=0$                                                   |
| Spherical shell, $r>R$           | $E=kQ/r^2$                                                                           |
| Spherical shell, $r<R$           | $E=0$                                                                                |
| Solid ball, $r>R$                | $E=kQ/r^2$                                                                           |
| Solid ball, $r<R$                | $E=kQr/R^3$                                                                          |

### 14.5 Electric Potential

| Concept | Formula |
| --- | --- |
| Electric potential energy | $U(\vec r)=qV(\vec r)$ |
| Potential from field | $V(\vec r_2)-V(\vec r_1)=-\displaystyle\int_{\vec r_1}^{\vec r_2}\vec E\cdot d\vec r$ |
| Field from potential | $E_x=-\partial V/\partial x$ (similarly $y,z$) |
| Point charge potential | $V(\vec r)=kq/r$ |
| Potential superposition | $V=\displaystyle\sum_i kq_i/r_i$ (scalar sum) |

### 14.6 Potential of Continuous Charge Distributions

| Concept | Formula |
| --- | --- |
| Ring potential, on-axis | $V(z)=kQ/\sqrt{z^2+R^2}$ |
| Disk potential, on-axis | $V(z)=2\pi k\sigma\left[\sqrt{z^2+R^2}-\lvert z\rvert\right]$ |
| Spherical shell potential, $r>R$ | $V=kQ/r$ |
| Spherical shell potential, $r<R$ | $V=kQ/R$ (constant) |
| Solid ball potential, $r>R$ | $V=kQ/r$ |
| Solid ball potential, $r<R$ | $V=\dfrac{kQ}{2R}\left(3-\dfrac{r^2}{R^2}\right)$ |

### 14.7 Capacitance and Dielectrics

| Concept | Formula |
| --- | --- |
| Ideal parallel-plate capacitance | $C=A/(4\pi k\ell)$ |
| Dielectric-filled capacitance | $C_\kappa=\kappa C$ ($\kappa>1$) |

**Discontinuity rule:** $E$ is discontinuous crossing an infinitesimally thin charged surface (disk, sheet, shell); $E$ is continuous crossing into a charge that fills a volume (solid ball).
