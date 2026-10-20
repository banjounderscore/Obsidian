# Physics 2212 — Test 1 Notes (Weeks 1–3)

> Test 2 material (continuous charge distributions, electric potential, circuits) is in [[Physics 2212 Test 2 Notes]].


---

## 1. Mathematical Toolkit: Vectors and the Binomial Approximation

Everything in E&M is a vector field or a scalar field, so before touching a single Coulomb force you need fluency with vectors. This section is the toolbox; every later derivation reaches back into it.

### 1.1 Vectors: magnitude and direction

A **vector** is any quantity defined by a magnitude *and* a direction (contrast a **scalar**, which is just a number: temperature, mass, charge).

![Vector components](images/01_vector_components.png)

For a position vector $\vec r$ making angle $\theta$ with the x-axis:

$$
r = |\vec r| = \sqrt{r_x^2+r_y^2}, \qquad \hat r = \frac{\vec r}{r}, \qquad \vec r = r_x\hat x + r_y\hat y = \langle r_x, r_y, 0\rangle
$$

- **Magnitude** $r$ is always $\ge 0$; it's the length of the arrow.
- **Components** are scalars: $r_x = r\cos\theta$, $r_y = r\sin\theta$ (if you instead measure the angle $\phi$ from the y-axis, the sine and cosine swap: $r_x=r\sin\phi$, $r_y=r\cos\phi$ — always re-derive from a picture, never memorize blindly).
- **Unit vector** $\hat r$ always has magnitude exactly 1: $|\hat r| = \vec r/r = r/r = 1$. It carries *only* direction information. You will use $\hat r$ constantly — it is what lets you turn "how far" into "which way."

> [!tip] Why unit vectors matter so much in this course
> Coulomb's law, the electric field, and the dipole field are all "(some scalar magnitude) $\times\ \hat r$." Separating magnitude from direction like this is the single biggest simplification in the whole course — internalize it now.

### 1.2 Vector addition

![Head-to-tail vector addition](images/02_vector_addition.png)

Vectors add component-by-component:

$$
\vec A+\vec B=(A_x+B_x)\hat x+(A_y+B_y)\hat y
$$

Geometrically, this is the **head-to-tail rule**: slide $\vec B$'s tail to $\vec A$'s head; the sum runs from $\vec A$'s tail to $\vec B$'s head. You'll use this picture constantly to *guess* the direction of a net force or field before grinding through algebra.

### 1.3 The dot ("scalar") product

$$
\vec A \cdot \vec B = AB\cos\theta = A_xB_x + A_yB_y + A_zB_z
$$

The result is a **scalar** (a plain number), not a vector. Two useful special cases: $\vec A\cdot\vec B=0$ when the vectors are perpendicular, and $\vec A \cdot \hat r$ picks out the component of $\vec A$ along $\hat r$. This shows up constantly when computing $\vec E\cdot d\vec r$ for the electric potential (Test 2).

The cross ("vector") product of two vectors is itself a vector — you'll meet it later in the course (magnetism); it doesn't appear in Weeks 1–3.

### 1.4 The binomial approximation

This is the single most useful piece of math in the entire course. For any real exponent $n$ and any small number $\epsilon$ (meaning $|\epsilon|\ll 1$):

$$
(1+\epsilon)^n \approx 1+n\epsilon
$$

**Where it comes from.** The full (Taylor/binomial) series is $(1+\epsilon)^n = 1+n\epsilon+\frac{n(n-1)}{2!}\epsilon^2+\cdots$. Each successive term is smaller than the last by an extra factor of $\epsilon$, so if $\epsilon$ is small, truncating after the first-order term throws away something tiny. It works for *any* $n$ — positive, negative, or fractional — not just positive integers.

**Step-by-step recipe** (memorize this procedure, not just the formula):

1. Identify a large quantity $d$ and a small quantity $s$ with $d\gg s$ in your expression.
2. Algebraically force the expression into the form $(\text{big})^n(1+\epsilon)^n$, by factoring the large quantity out of every term inside a sum or difference, so that what's left over is a small ratio $\epsilon=\pm s/d$.
3. Replace $(1+\epsilon)^n$ with $1+n\epsilon$.
4. Distribute and simplify. Often the zeroth-order term ($1$) reproduces something you already knew, and the *interesting new physics* is hiding in the $n\epsilon$ correction.

> [!example] Worked example: the on-axis dipole field
> Starting from the exact two-charge sum (Section 5) and factoring $r$ out of each denominator: $(r\mp s/2)^{-2} = r^{-2}(1\mp s/2r)^{-2}$. Apply the rule with $n=-2$, $\epsilon=\mp s/(2r)$:
> $$
> \left(1-\frac{s}{2r}\right)^{-2} \approx 1+2\cdot\frac{s}{2r} = 1+\frac{s}{r}, \qquad \left(1+\frac{s}{2r}\right)^{-2} \approx 1-2\cdot\frac{s}{2r} = 1-\frac{s}{r}
> $$
> $$
> \vec E_\parallel(\vec r) = \frac{kq}{r^2}\left[\left(1+\frac{s}{r}\right)-\left(1-\frac{s}{r}\right)\right]\hat r = \frac{kq}{r^2}\cdot\frac{2s}{r}\,\hat r = k\frac{2qs}{r^3}\hat r = k\frac{2\vec p}{r^3}
> $$
> This matches the exact-limit result from Section 5 — the binomial trick is just a faster, more systematic route than combining fractions by hand.

Any "far field" ($r\gg$ object size) or "close-up" limit in this course is this tool at work under the hood.

---

## 2. Electric Charge

### 2.1 What charge is

The ancient Greeks discovered that rubbing amber with fur made it attract feathers and straw. Benjamin Franklin later invented the algebraic convention ($\pm$) that quantifies the strength of this force: **electric charge**.

> [!important] Fundamental facts about charge
> - Charge is an **intrinsic, indestructible property** of the elementary constituents of matter — not something "made of" anything more basic.
> - The smallest magnitude of charge is $e = 1.602\times10^{-19}$ C (often rounded to $1.6\times10^{-19}$ C).
> - proton: $+e$ · electron: $-e$ · neutron: $0$.
> - A sample of matter with $N_p$ protons and $N_e$ electrons has net charge $q = e(N_p - N_e)$.

### 2.2 Conservation of charge

Charge is **conserved**: it is never created or destroyed in any ordinary process, because it is an intrinsic property of electrons and protons, and those particles themselves are not created or destroyed in ordinary (non-nuclear) processes.

**Full disclosure:** quantum mechanics *does* permit creation of an electron and a proton together — for example, radioactive neutron decay $n \to p + e + \bar\nu$ — but notice that the *total* charge before ($0$, a neutral neutron) and after ($+e-e=0$) is unchanged. Charge conservation survives even this exception.

### 2.3 Charge can be *moved* extremely easily

The electron-to-proton mass ratio is $m_e/m_p \approx 5\times10^{-4}$, meaning electrons are almost 2000× lighter than protons. This makes electrons vastly easier to strip off or add to atoms than protons — and it's the single fact underlying **static electricity, polarization, and electrical conduction**, the three phenomena that dominate the next few sections. (J.J. Thomson's 1897 discovery of the electron — for which he won the 1906 Nobel Prize — is what made this whole picture possible.)

---

## 3. Coulomb's Law

Charles-Augustin de Coulomb (1736–1806) experimentally quantified the force between two charged objects.

### 3.1 Statement of the law

**Coulomb's Law:** the force that a point charge* $q_1$ located at $\vec r_1$ exerts on a point charge $q_2$ located at $\vec r_2$:

$$
\vec F_{21} = k\,q_1 q_2\, \frac{\vec r_2-\vec r_1}{|\vec r_2-\vec r_1|^3} = -\vec F_{12}
$$

with Coulomb's constant

$$
k = \frac{1}{4\pi\epsilon_0} = 9\times10^9\ \text{N·m}^2\text{/C}^2
$$

$\epsilon_0$ (the *permittivity of free space*) is a fundamental physical constant of Nature, playing a role analogous to Newton's gravitational constant $G$.

*\*A point charge is a charged object so small that its physical size plays no role in the physics — an idealization, like a "point mass" in mechanics.*

### 3.2 Magnitude: an inverse-square law

Taking the magnitude of both sides, with $R \equiv |\vec r_2-\vec r_1|$ the separation distance:

$$
|\vec F_{21}| = |\vec F_{12}| = \frac{1}{4\pi\epsilon_0}\frac{|q_1q_2|}{R^2} = \frac{k|q_1q_2|}{R^2}
$$

This is an **inverse-square law** — structurally identical to Newton's law of gravitation, $F=Gm_1m_2/R^2$. That resemblance is not a coincidence you need to explain; it's a pattern worth noticing because your mechanics intuition (e.g. about orbits, potential wells) often carries over directly.

### 3.3 Direction: attraction and repulsion

![Like charges repel; opposite charges attract](images/03_coulomb_repel_attract.png)

- **Like charges repel.**
- **Opposite charges attract.**

Coulomb's law automatically satisfies **Newton's third law** ($\vec F_{21}=-\vec F_{12}$), because the force depends only on the *separation* $\vec r_2-\vec r_1$ between the two charges — never on where you happened to put your coordinate origin. This is worth pausing on: if the physics depended on the origin, the theory would be broken, since the origin is a bookkeeping choice, not a physical feature of the world.

### 3.4 Superposition: forces add as vectors

![Superposition of forces](images/04_superposition_forces.png)

When several charges $1,2,\ldots,N$ simultaneously act on a charge $Q$, the **net force is the vector sum** of the individual Coulomb forces:

$$
\vec F_Q = \vec F_{Q1}+\vec F_{Q2}+\cdots+\vec F_{QN}
$$

> [!warning] The single most common beginner mistake
> This is **vector** addition, never scalar addition. You cannot add magnitudes and then "figure out" a direction afterward — you must add the $x$-components together and the $y$-components together separately (or draw the head-to-tail diagram), *then* take the magnitude of the result if you need it. A force of 5 N right plus a force of 5 N left is **0**, not 10 N.

**Worked example.** Three charges: $q_1=+e$, a test charge $Q$ sits between them, and $q_3=-2e$. The force on $Q$ is $\vec F_2 = \vec F_{21}+\vec F_{23}$ — you compute each Coulomb force separately using the formula above (each pointing along the line connecting the relevant pair of charges, repulsive from $q_1$ since $Q$ is presumably positive, attractive toward $q_3$ since it's negative), then add the two vectors head-to-tail to get the true net force direction — which in general points *nowhere near* either individual contribution.

---

## 4. The Electric Field

### 4.1 Faraday's idea: separating the "victim" from the "source"

Michael Faraday came from a poor English family, was schooled only through age 12, and apprenticed to a bookbinder — yet by thinking hard about his own experiments (he knew almost no formal mathematics) he introduced one of the most powerful concepts in all of physics: the **field**.

A field assigns a value to *every point in space*. A **scalar field** like temperature $T(\vec r)$ assigns a number to each point; a **vector field** like wind velocity $\vec W(\vec r)$ assigns a magnitude and direction to each point.

Faraday's insight, applied to electricity: the total Coulomb force on a charge $Q$ sitting at a point $P$ is

$$
\vec F_Q = Q\,\vec E(P)
$$

where $\vec E(P)$ is the **electric field** at $P$ — produced by *every other* charge in the world — and it exists at $P$ whether or not $Q$ is actually sitting there to feel it. The field is a property of *space itself*, sourced by charges; a test charge dropped into that space merely reveals the field that was already there.

### 4.2 Field of a point charge

Rewrite Coulomb's law by simply factoring out the "victim" charge $Q$:

$$
\vec F_{Qq} = kQq\,\frac{\vec r_Q-\vec r_q}{|\vec r_Q-\vec r_q|^3} = Q\underbrace{\left[kq\,\frac{\vec r_Q-\vec r_q}{|\vec r_Q-\vec r_q|^3}\right]}_{\vec E_q(\vec r_Q-\vec r_q)}
$$

so that, for a charge $q$ sitting at the origin, the field it produces at position $\vec r$ is

$$
\vec E(\vec r) = \frac{kq}{r^2}\hat r
$$

### 4.3 Two equivalent pictures of a field

![Field of a positive/negative point charge](images/05_point_charge_field_lines.png)

- The **length of the $\vec E$-vector** drawn at a point is proportional to the field's magnitude there, *or*
- The **density of field lines** through a region is proportional to the field's magnitude there.

Both pictures describe the same physical object; use whichever is more convenient for the argument you're making.

### 4.4 Symmetry: a very big idea in physics

A point charge looks *exactly the same* after any rotation, about any axis through its center. Since the field it produces must respect that same symmetry:

- The **direction** of the field must be purely radial: $\vec E(\vec r) = E(\vec r)\,\hat r$.
- The **magnitude** must depend only on distance $r$, never on angle: $E(\vec r) = E(r)$.

We say the point charge (and its field) exhibits **rotational symmetry**. This is not just a description of the point-charge result — it's a *technique*: throughout this course, you use the symmetry of a charge distribution to guess the *direction* of its field before ever writing an integral (you'll see this with rings, sheets, shells, and balls in Test 2).

### 4.5 Field-line rules (always true, not just for point charges)

- Field lines **begin** on positive charge (or at infinity).
- Field lines **end** on negative charge (or at infinity).

### 4.6 Superposition of fields

The field at any point is the vector sum of the fields produced separately by every source charge:

$$
\vec E(P) = \vec E_1(P)+\vec E_2(P)+\cdots
$$

Inserting a charge $Q$ at $P$ *afterward* simply gives $\vec F_Q = Q\vec E(P)$ — the presence of $Q$ does not itself change $\vec E(P)$ (we assume $Q$ is a small "test charge" that doesn't disturb the source charges).

### 4.7 The far-field theorem for charged objects

> [!important] Far-field theorem
> Viewed from far away ($r\gg s$, where $s$ is the object's own size), **any** object with nonzero net charge $Q\ne0$ behaves electrically just like a single point charge:
> $$
> \vec E(\vec r) \approx \frac{kQ}{r^2}\hat r \qquad (r\gg s)
> $$

This is why, no matter how complicated a charged duck, rod, or disk looks up close, from across the room it just looks like a point charge $Q$ sitting at its center of charge.

### 4.8 Do neutral objects produce a field?

The $1/r^2$ far field above literally vanishes when $Q=0$ — but that does **not** mean $\vec E=0$ everywhere for a neutral object. It depends on whether the object has *internal charge separation*:

- An isolated **atom**: no separation of $+$ and $-$ charge on opposite sides → $\vec E_{\text{atom}}(\vec r) = 0$ everywhere.
- A **water molecule**: oxygen is more electronegative than hydrogen and pulls electron density toward itself → there *is* charge separation → $\vec E_{\text{molecule}}(\vec r) \ne 0$, even though the total charge is zero.

The prototype charge-neutral, charge-separated object is the **electric dipole** — the subject of the next section, and the key that explains this behavior quantitatively.

---

## 5. The Electric Dipole

Two charges $-q$ and $+q$, separated by a small distance $s$, form the prototype charge-neutral, charge-separated object.

### 5.1 The dipole moment vector

The **electric dipole moment** $\vec p$ points from $-q$ to $+q$ and has magnitude $p=qs$. More generally, for *any* collection of charges $q_k$ at positions $\vec r_k$:

$$
\vec p = \sum_{k=1}^N q_k \vec r_k
$$

(For the simple two-charge dipole, placing the origin at the midpoint, this reduces to $\vec p = qs\,\hat x$ pointing along the separation direction — you can verify: $\vec p = q_1\vec r_1+q_2\vec r_2 = e(s/2)\hat x + (-e)(-s/2)\hat x = qs\,\hat x$.)

### 5.2 On-axis field $\vec E_\parallel$: full derivation

![On-axis dipole geometry|588](images/07_dipole_on_axis_geometry.png)

Restrict to points on the symmetry axis, i.e. points $(x,0,0)$. Call this field $\vec E_\parallel(x)$. **Strategy: superpose the two point-charge fields.**

With the $+q$ charge at $(s/2,0,0)$ and $-q$ at $(-s/2,0,0)$, distances from each to the field point are $r_+=x-s/2$ and $r_-=x+s/2$:

$$
\vec E_+ = k\frac{q}{r_+^2}\hat x, \qquad \vec E_- = k\frac{-q}{r_-^2}\hat x
$$

$$
\vec E_\parallel = \vec E_+ + \vec E_- = k\left[\frac{q}{(x-s/2)^2}-\frac{q}{(x+s/2)^2}\right]\hat x
$$

This is the **exact** result for any $x$. Taking $r\gg s$ (using the binomial approximation from Section 1.4):

$$
\vec E_\parallel(\vec r) \approx k\,\frac{2\vec p}{r^3}
$$

### 5.3 Perpendicular-bisector field $\vec E_\perp$: full derivation

![Perpendicular-bisector dipole geometry|460](images/08_dipole_perp_geometry.png)

Now restrict to observation points on the axis *perpendicular* to the dipole's symmetry axis. By the geometry, the $x$-components of the two point-charge fields cancel ($E_x = -E_x'$) while the $y$-components add ($E_y=E_y'=-E_y\hat y$ each), giving $\vec E_\perp = \vec E + \vec E' = -2E_y\,\hat y$. Writing $E=kq/(r^2+(s/2)^2)$ and $\sin\theta = (s/2)/\sqrt{r^2+(s/2)^2}$:

$$
\vec E_\perp = -2E\sin\theta\,\hat y = -2\frac{kq}{r^2+(s/2)^2}\cdot\frac{s/2}{\sqrt{r^2+(s/2)^2}}\,\hat y
$$

Taking $r\gg s$:

$$
\vec E_\perp(\vec r) \approx -k\,\frac{\vec p}{r^3}
$$

### 5.4 Why bother defining $\vec p$?

Once you have $\vec p$, both special-case results compress into single expressions with no leftover reference to $q$ and $s$ separately:

$$
\vec E_\parallel \approx k\,\frac{2\vec p}{r^3}, \qquad \vec E_\perp \approx -k\,\frac{\vec p}{r^3}
$$

**Both fall off as $1/r^3$** (inverse cube) — a full power steeper than the $1/r^2$ of a single point charge. This $1/r^3$ signature is how you *recognize* a dipole field at a glance.

> [!tip] Units check (a technique worth stealing)
> Introduce the notation $[x]$ for "the units of $x$." We know $[E_q]=[k][q]/[r]^2$. We claim $[E_\parallel] = [k][2qs]/[r]^3 = [k][q]/[r]^2 \times [s]/[r]$. Since $[s]=[r]$ (both are lengths), the extra factor is dimensionless and $[E_\parallel]=[E_q]$ — consistent. Running a quick units check like this after every derivation catches algebra mistakes fast.

### 5.5 General dipole field at any point

![General dipole field-point geometry|445](images/09_dipole_general_geometry.png)

There is a single formula valid at *any* angle between $\vec p$ and $\hat r$ (not just on-axis or perpendicular):

$$
\vec E(\vec r) = k\,\frac{3(\vec p\cdot\hat r)\hat r - \vec p}{r^3}
$$

**Check against the two special cases:**
- $\hat r\perp\vec p$: then $\vec p\cdot\hat r=0$, so $\vec E(\vec r)=-k\vec p/r^3=\vec E_\perp$. ✓
- $\hat r\parallel\vec p$: then $\vec p\cdot\hat r = p$, so $\vec E(\vec r)=k(3\vec p-\vec p)/r^3=2k\vec p/r^3=\vec E_\parallel$. ✓

![Qualitative dipole field-line pattern|544](images/06_dipole_field_lines.png)

### 5.6 The far-field theorem for *any* neutral object

> [!important] Far-field theorem, extended
> Far away ($r\gg s$) from *any* object with zero net charge ($Q=0$) but nonzero dipole moment ($\vec p\ne0$), the field is *exactly* the dipole field above, using $\vec p=\sum q_k\vec r_k$ computed from the object's own charges.

This is precisely why a neutral water molecule still produces a nonzero field far away, while a neutral atom (no charge separation, $\vec p=0$) does not: the far field of *any* charge distribution is controlled by the first nonvanishing term in a hierarchy — net charge $Q$ first, then dipole moment $\vec p$ if $Q=0$, and so on.

**Other useful facts:** superposition still applies when combining a dipole's field with a point charge's field, or with another dipole's field; field lines still begin on $+$ charge and end on $-$ charge.

---

## 6. Polarization of Atoms, Molecules, and Matter

### 6.1 Induced polarization (nonpolar atoms and molecules)

![Atom polarization: induced dipole|700](images/10_atom_polarization.png)

An external field $\vec E_{ext}$ pushes positive and negative charge within a neutral atom (or a nonpolar molecule, e.g. N₂) in *opposite* directions, since $\vec F = q\vec E_{ext}$ has opposite sign for $+$ and $-$ charge. The result is a small **induced dipole moment**:

$$
\vec p = \alpha\,\vec E_{ext}
$$

$\alpha$ is the atomic or molecular **polarizability** — a species-dependent constant you look up in a handbook. Crucially, $\vec p\to0$ the instant $\vec E_{ext}\to0$: there is nothing "permanent" about this dipole moment.

### 6.2 Permanent polarization (polar molecules)

In molecules like H₂O, chemical bonding *alone* — with no external field required — separates charge: oxygen is more electronegative than hydrogen and pulls electron density toward itself. The result is a **permanent** electric dipole moment $\vec p_{mol}$ that exists even when $\vec E_{ext}=0$. (You look these values up in handbooks, just like $\alpha$.)

### 6.3 Dipole–dipole interaction

Two **antiparallel** dipoles (e.g. two oppositely oriented water molecules) attract overall — the near ends (opposite charges, close together) attract more strongly than the far ends (also opposite charges, but farther apart) repel, so the net force is attractive. This is the microscopic origin of hydrogen bonding and a huge amount of everyday chemistry.

### 6.4 Force between a point charge and an induced dipole

A charge (say, an electron) at distance $d$ from a nonpolar molecule induces $\vec p=\alpha\vec E_O$ in that molecule. You cannot use $\vec F=Q\vec E$ directly on the molecule since the *neutral* molecule has $Q=0$ — instead use Newton's third law: compute the force the *molecule's induced dipole field* exerts back on the electron, then flip the sign.

$$
\vec F_e = -e\,\vec E_{\text{at }e}, \qquad \vec p = \alpha \vec E_O = \alpha\left(-k\frac{e}{d^2}\right)\hat x = -\frac{\alpha k e}{d^2}\hat x
$$

$$
\vec F_O = -\vec F_e = -\frac{2\alpha k^2 e^2}{d^5}\hat x
$$

This is an **attractive** force falling off as $1/d^5$ — a full three powers steeper than Coulomb's $1/d^2$, because one of the two "charges" involved is only *induced*, not fixed: as $d$ increases, not only does the ordinary Coulomb $1/d^2$ kick in, but the induced dipole moment itself *also* shrinks (since $E_O\propto 1/d^2$), giving extra powers of $1/d$.

### 6.5 How a bulk insulator polarizes

![How a bulk insulator polarizes|524](images/11_bulk_insulator_polarization.png)

Every atom in the material acquires $\vec p_{\text{atom}}=\alpha\vec E_{ext}$. Picture the material as a lattice of tiny aligned dipoles: the $+$ end of one atom sits right next to the $-$ end of its neighbor, and these touching charges **cancel** throughout the interior. Only the outermost front and back faces are left with uncancelled net charge $\pm Q$. The whole body's dipole moment is therefore

$$
\vec p_{\text{body}} = \sum_{\text{atom}} \vec p_{\text{atom}} = Q\vec s
$$

i.e., equivalent to two point charges $\pm Q$ separated by the body's own thickness $\vec s$ — a "macro-dipole" built from billions of microscopic ones.

### 6.6 Field inside a polarized insulator

![Field inside insulator vs. conductor](images/12_field_inside_insulator_conductor.png)

The surface polarization charges create their own field $\vec E_{pol}$ that points **opposite** to $\vec E_{ext}$ and *partially* cancels it:

$$
\vec E_{inside} = \vec E_{ext}+\vec E_{pol} = \vec E_{ext} - |\vec E_{pol}| = \frac{\vec E_{ext}}{\kappa}
$$

$\kappa>1$ is the **dielectric constant**: the interior field stays *parallel* to $\vec E_{ext}$ but is *reduced in magnitude*. Contrast this with a conductor (Section 7), where the cancellation is total.

---

## 7. Conductors and Insulators

### 7.1 The microscopic difference

- **Insulator:** every electron is bound to one particular atom — it cannot wander.
- **Conductor:** valence electrons migrate freely from atom to atom throughout the material.

This one microscopic fact is the root of every macroscopic difference between the two.

### 7.2 Charging methods

- **Frictional rubbing** transfers electrons between two initially neutral insulators (glass+silk, amber+wool); afterward the two objects carry equal and opposite charge. A rough triboelectric ranking, from *loses* electrons most easily to *gains* electrons most easily: human skin, glass, wool, cat fur, wood, silk, amber, rubber, styrofoam. *(For fun: one microscopic theory is that frictional motion breaks chemical bonds, the released bond energy locally heats each surface unequally, the temperature difference drives a thermoelectric field, and that field is what actually drives the electron transfer.)*
- **Charging a conductor by contact:** touch a charged insulating rod to a neutral conducting sphere — charge transfers onto the sphere and then spreads itself over the entire conducting surface.
- **Charging by polarization/induction:** bring a charged rod near two touching neutral conductors (which polarizes them), separate the two conductors *while the rod is still nearby*, then remove the rod. Result: two conductors left with equal and opposite charge, and the rod itself is completely unchanged.
- **Grounding:** connect a charged conductor to the Earth, and charge flows until the conductor is neutralized. This happens *spontaneously* — with no need for anything to "push" it — because it lowers the total electrostatic energy of the whole system, and systems evolve toward lower energy.

### 7.3 The conductor's "superpower": $\vec E=0$ inside, always

![Field inside insulator vs. conductor](images/12_field_inside_insulator_conductor.png)

In electrostatic equilibrium, $\vec E=0$ at **every** point inside a conductor's material — regardless of the conductor's shape, regardless of what charges sit outside it or in a cavity within it. Mobile charges physically rearrange themselves on the surface(s) until the field *they* create exactly cancels any external field throughout the entire interior:

$$
\vec E_{inside} = \vec E_{ext} + \vec E_{pol} = 0 \quad\Rightarrow\quad |\vec E_{pol}| = |\vec E_{ext}|
$$

> [!important] The defining property of a conductor
> $E_{inside}=0$ **always**, for a conductor in electrostatic equilibrium — full cancellation, not the partial cancellation ($E_{inside}=E_{ext}/\kappa$) you get for an insulator.

**Why this must be true, physically:** if $\vec E\ne0$ anywhere inside a conductor, mobile charges there would feel a force and *keep moving* — by definition, that is not yet equilibrium. Equilibrium, for a conductor, is only reached once the internal field vanishes everywhere and nothing is left to push the charges around.

### 7.4 Shielding: the Faraday-cage effect

![Shielding by a conducting shell](images/13_shielding_cavity.png)

If you scoop a cavity out of a conductor, the surface charge still rearranges so that $\vec E=0$ throughout the solid conductor material — and, remarkably, $\vec E=0$ throughout the *empty cavity* too, as long as no charge sits inside the cavity itself. This is exactly why a conducting shell shields its interior from any external field — the working principle behind a Faraday cage.

### 7.5 Worked conceptual examples

- **Two point charges placed symmetrically around the center $C$ of a solid metal cube:** $E(C)=0$ — not because the two contributions happen to cancel, but simply because $C$ sits inside conductor material, and $E_{inside}=0$ *always*, no matter the external charge arrangement.
- **A dipole $\vec p$ held outside a solid metal cube**, at perpendicular distance $d$ from center $C$: this polarizes the cube. Since $E_{inside}$ must vanish, the cube's own field at $C$ must exactly cancel the dipole's field there: $\vec E_{cube}(C)=-\vec E_{dipole}(C)=+k\vec p/d^3$ (using $E_\perp=-k\vec p/d^3$ for this perpendicular geometry).
- **The same dipole outside a plastic (insulating) cube instead:** the cube still polarizes and produces its own field $\vec E_{cube}(\vec r)$, but nothing *forces* that field to cancel the dipole's field at $C$, so $\vec E_{total}(C)=\vec E_{dipole}(C)+\vec E_{cube}(C)\ne0$ in general. This contrast is the defining functional difference between a conductor and an insulator.
- **A positive point charge embedded at the center of an insulating sphere, itself coated with a thick conducting shell:** the shell's *outer* surface acquires charge equal in sign and magnitude to the embedded charge — because $\vec E=0$ must hold everywhere inside the metal, which forces the inner shell surface to carry $-q$ (canceling the embedded $+q$'s field within the metal) and, since the shell started neutral, the outer surface is left with $+q$.

---

## 8. Worked Conceptual Examples (Clicker-Question Digest)

These are the reasoning patterns tested throughout the first three weeks — read them as a diagnostic: if any one of these feels unfamiliar, go back to the referenced section.

**1. Which quadrant places a negative charge $Q$ so the net force on a negative charge at the origin is zero?** (Section 3.4) Work out the force from the *known* charges first, then ask what additional force — in both direction *and* magnitude — would exactly cancel it. The charge producing that canceling force can be either sign, depending on which side of the origin you place it (attraction vs. repulsion flips with sign, but so does which side pulls "the right way").

**2. Sketching field lines for two point charges.** (Section 4.5–4.6) Two rules do all the work: very close to either individual charge, the field must locally resemble that single isolated point charge's radial pattern; and any point of exact symmetry between equal-and-opposite or equal-and-same charges may (or may not) have $\vec E=0$, which you check directly from superposition.

**3. Electric field of a "duck" with net negative charge, viewed from far away.** (Section 4.7) However lumpy the near-field lines look up close, *every* field line shown at large distance must still terminate on the duck (since it's negatively charged, field lines end there) — the far-field theorem guarantees the large-scale pattern looks exactly like that of a single point charge equal to the duck's total charge.

**4. Two charges $+2q$ and $-q$: does the field look like a dipole?** (Sections 4.7, 5.6) **No.** The net charge is $Q=2q-q=q\ne0$, so the far-field theorem for *charged* objects applies: far away, this looks like a single point charge $+q$, falling off as $1/r^2$ — not like a dipole's $1/r^3$. The dipole far-field formula only kicks in when $Q=0$ exactly.

**5. Water molecule polarizing a neutral atom nearby.** (Section 6.1, 6.4) The polar molecule's own field polarizes the initially-unpolarized neutral atom, inducing a dipole moment in it; the two dipoles then interact exactly as in Section 6.3 — an overall attractive force (near-end attraction beats far-end repulsion).

**6. Force $\vec F_1$ on an electron near a polarized H₂O molecule vs. force $\vec F_2$ on a different electron near a polarized O₂ molecule.** The key insight in problems like this: identify what physical vector (the source dipole moment, or the field it produces) actually controls the direction of the force in question, and compare the *geometry* of the two setups — parallel, anti-parallel, or perpendicular — rather than re-deriving each force from scratch.

**7. Charge sitting inside an uncharged conducting shell with thick walls.** (Section 7.5) The shell's *inner* surface acquires charge opposite in sign to the enclosed charge (forcing $E=0$ within the metal itself); since the shell overall is neutral, its *outer* surface is left with charge equal in sign and magnitude to the enclosed charge.

**8. Insulating block with two nearby charged balls — field at the midpoint, and at the block's center.** (Section 6.5–6.6) There are *three* contributions to add by superposition: the field from each of the two external balls, *plus* the field from the block's own induced polarization charges — and importantly, the induced field $E_{pol}$ never fully cancels the external field for an insulator (contrast a conductor, where it would cancel completely).

---

## 9. Quick-Reference Formula Sheet

Constants: $e = 1.602\times10^{-19}$ C, $k=1/(4\pi\epsilon_0) = 9\times10^9$ N·m²/C².

### 9.1 Coulomb's Law, Fields, and Forces

| Concept                   | Formula                                                                             |
| ------------------------- | ----------------------------------------------------------------------------------- |
| Coulomb's Law             | $\vec F_{21} = kq_1q_2\,\dfrac{\vec r_2-\vec r_1}{\lVert\vec r_2-\vec r_1\rVert^3}$ |
| Field of a point charge   | $\vec E(\vec r) = \dfrac{kq}{r^2}\hat r$                                            |
| Force from a field        | $\vec F = Q\vec E$                                                                  |
| Far-field, net charge $Q$ | $\vec E \approx \dfrac{kQ}{r^2}\hat r$, for $r\gg s$                                |

### 9.2 Electric Dipole

| Concept                     | Formula                                                              |
| --------------------------- | -------------------------------------------------------------------- |
| Dipole moment               | $\vec p = qs$ (points $-q\to+q$); general: $\vec p=\sum q_k\vec r_k$ |
| Dipole field, on-axis       | $\vec E_\parallel \approx k\dfrac{2\vec p}{r^3}$                     |
| Dipole field, ⊥ bisector    | $\vec E_\perp \approx -k\dfrac{\vec p}{r^3}$                         |
| Dipole field, general point | $\vec E(\vec r) = k\dfrac{3(\vec p\cdot\hat r)\hat r-\vec p}{r^3}$   |

### 9.3 Polarization, Conductors, and Insulators

| Concept | Formula |
| --- | --- |
| Induced dipole moment | $\vec p = \alpha\vec E_{ext}$ |
| Force: point charge on induced dipole | $F_O = -2\alpha k^2 e^2/d^5$ (attractive, toward the charge) |
| Bulk insulator dipole moment | $\vec p_{body} = Q\vec s$ |
| Field inside a polarized insulator | $E_{inside}=E_{ext}/\kappa$ ($\kappa>1$, dielectric constant) |
| Conductor polarization condition | $\vec E_{pol}=-\vec E_{ext}$, so $\lvert\vec E_{pol}\rvert=\lvert\vec E_{ext}\rvert$ |
| Field inside a conductor | $E_{inside}=0$ (always) |
