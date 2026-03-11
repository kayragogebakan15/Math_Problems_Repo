# Solutions


# Task List 1 — Events and Probability (Sample Spaces): Solutions

---

## Task 1 — Coin Tossing

### 1. Sample space for one coin toss

$$\Omega_1 = \{H, T\}$$

- **Number of outcomes:** $|\Omega_1| = 2$
- **Elementary outcome:** The result of a single coin flip — either Heads (H) or Tails (T).

---

### 2. Sample space for two coin tosses

$$\Omega_2 = \{HH, HT, TH, TT\}$$

**Tree diagram:**
```
START
 ├── H
 │     ├── H  → (H,H)
 │     └── T  → (H,T)
 └── T
       ├── H  → (T,H)
       └── T  → (T,T)
```

- **Number of outcomes:** $|\Omega_2| = 2^2 = 4$
- **Elementary outcome:** An ordered pair representing the result of the first and second toss.

---

### 3. Sample space for three coin tosses

$$\Omega_3 = \{HHH, HHT, HTH, HTT, THH, THT, TTH, TTT\}$$

- **Number of outcomes:** $|\Omega_3| = 2^3 = 8$
- **Elementary outcome:** An ordered triple representing the results of all three consecutive tosses.

---

## Task 2 — Rolling a Die

### 1. Sample space for one die roll

$$\Omega_1 = \{1, 2, 3, 4, 5, 6\}$$

- **Number of outcomes:** $|\Omega_1| = 6$
- **Elementary outcome:** The number showing on the top face of the die after one roll.

---

### 2. Sample space for two consecutive rolls

$$\Omega_2 = \{(i,j) : i,j \in \{1,2,3,4,5,6\}\}$$

All ordered pairs $(1,1), (1,2), \ldots, (6,6)$.

- **Number of outcomes:** $|\Omega_2| = 6^2 = 36$
- **Elementary outcome:** An ordered pair $(i,j)$ where $i$ is the result of the first roll and $j$ is the result of the second roll.

---

### 3. Sample space for three consecutive rolls

$$\Omega_3 = \{(i,j,k) : i,j,k \in \{1,2,3,4,5,6\}\}$$

- **Number of outcomes:** $|\Omega_3| = 6^3 = 216$
- **Elementary outcome:** An ordered triple $(i,j,k)$ representing the results of three consecutive die rolls.

---

## Task 3 — Drawing Cards

A standard deck has 52 cards: 4 suits (♥ ♦ ♣ ♠), each with 13 ranks (A, 2–10, J, Q, K).

### 1. Sample space for one card drawn

$$\Omega_1 = \{\text{all 52 cards}\}$$

- **Number of outcomes:** $|\Omega_1| = 52$
- **Elementary outcome:** A single card identified by its suit and rank.

---

### 2. Sample space for two draws **with replacement**

$$\Omega_2 = \{(c_1, c_2) : c_1, c_2 \in \text{52 cards}\}$$

- **Number of outcomes:** $|\Omega_2| = 52^2 = 2{,}704$
- **Elementary outcome:** An ordered pair of cards where the first card is returned to the deck before the second draw.

---

### 3. Sample space for two draws **without replacement**

$$\Omega_2' = \{(c_1, c_2) : c_1, c_2 \in \text{52 cards},\ c_1 \neq c_2\}$$

- **Number of outcomes:** $|\Omega_2'| = 52 \times 51 = 2{,}652$
- **Elementary outcome:** An ordered pair of **distinct** cards; the first drawn card is not returned to the deck.

---

## Task 4 — Weekly Weather Observation

States: Sunny (S), Cloudy (C), Rainy (R).

### 1. Sample space for one day

$$\Omega_1 = \{S, C, R\}$$

- **Number of outcomes:** $|\Omega_1| = 3$

---

### 2. Sample space for two consecutive days

$$\Omega_2 = \{(SS), (SC), (SR), (CS), (CC), (CR), (RS), (RC), (RR)\}$$

- **Number of outcomes:** $|\Omega_2| = 3^2 = 9$

---

### 3. Sample space for seven consecutive days

$$\Omega_7 = \{(w_1, w_2, w_3, w_4, w_5, w_6, w_7) : w_i \in \{S, C, R\}\}$$

- **Number of outcomes:** $|\Omega_7| = 3^7 = 2{,}187$
- **Elementary outcome:** An ordered 7-tuple representing the weather state on each of the seven days of the week.

---

## Task 5 — Buffon's Needle Experiment

A needle of length $L$ is thrown onto a floor with parallel lines spaced $d$ apart. Assume $L \leq d$.

### 1. Sample space

The outcome of each throw is determined by two parameters:
- $X \in \left[0, \dfrac{d}{2}\right]$ — distance from the needle's **center** to the **nearest line** (using symmetry).
- $\theta \in \left[0, \dfrac{\pi}{2}\right]$ — **angle** between the needle and the lines (using symmetry).
- $\Omega = \{(x, \theta) : x \in \left[0, \frac{d}{2}\right],\ \theta \in \left[0, \frac{\pi}{2}\right]\}$

### 2. Parameters determining the outcome

Each throw is fully described by the pair $(x, \theta)$:
- $x$: position (distance of needle center to the nearest line),
- $\theta$: orientation angle of the needle.

### 3. Elementary outcome representation

An elementary outcome is a point $(x, \theta) \in \Omega$.

### 4. Why is this sample space continuous?

Unlike Tasks 1–4, the parameters $x$ and $\theta$ can take **any real value** within their respective intervals — there are **uncountably many** possible outcomes. This makes $\Omega$ a **continuous** (uncountably infinite) sample space, and probabilities of events are computed using **area ratios** (geometric probability / integration), not by counting.

---

## Task 6 — Events and Probabilities in Coin Tossing

All elementary outcomes are **equally likely** (fair coin).

- $P(\omega) = \dfrac{1}{2}$ for $\omega \in \Omega_1$

- $P(\omega) = \dfrac{1}{4}$ for $\omega \in \Omega_2$

- $P(\omega) = \dfrac{1}{8}$ for $\omega \in \Omega_3$

---

### One Coin Toss

- $A_1 = \{H\}$ — result is **heads**:
$$P(A_1) = \frac{1}{2}$$

- $B_1 = \{T\}$ — result is **tails**:
$$P(B_1) = \frac{1}{2}$$

- $C_1 = \{H\}$ — result is **not tails** (same as $A_1$):
$$P(C_1) = \frac{1}{2}$$

---

### Two Coin Tosses

- $A_2 = \{HT, TH\}$ — **exactly one head**:
$$P(A_2) = \frac{2}{4} = \frac{1}{2}$$

- $B_2 = \{HH, HT, TH\}$ — **at least one head**:
$$P(B_2) = \frac{3}{4}$$

- $C_2 = \{HH, TT\}$ — **both tosses give the same result**:
$$P(C_2) = \frac{2}{4} = \frac{1}{2}$$

---

### Three Coin Tosses

- $A_3 = \{HHT, HTH, THH\}$ — **exactly two heads**:
$$P(A_3) = \frac{3}{8}$$

- $B_3 = \Omega_3 \setminus \{HHH\}$ — **at least one tail** (complement of all heads):
$$P(B_3) = 1 - \frac{1}{8} = \frac{7}{8}$$

- $C_3 = \{HHH, TTT\}$ — **all three tosses the same**:
$$P(C_3) = \frac{2}{8} = \frac{1}{4}$$

**Additional event (self-defined):**

$D_3 = \{HTT, THT, TTH\}$ — **exactly one head** in three tosses:
$$P(D_3) = \frac{3}{8}$$

---

## Task 7 — Events and Probabilities in Die Rolling

All elementary outcomes are **equally likely** (fair die).

- $P(\omega) = \dfrac{1}{6}$ for $\omega \in \Omega_1$

- $P(\omega) = \dfrac{1}{36}$ for $\omega \in \Omega_2$

- $P(\omega) = \dfrac{1}{216}$ for $\omega \in \Omega_3$

---

### One Die Roll

- $A_1 = \{2,4,6\}$ — result is **even**:
$$P(A_1) = \frac{3}{6} = \frac{1}{2}$$

- $B_1 = \{5,6\}$ — result is **greater than 4**:
$$P(B_1) = \frac{2}{6} = \frac{1}{3}$$

- $C_1 = \{1,2,3\}$ — result is **at most 3**:
$$P(C_1) = \frac{3}{6} = \frac{1}{2}$$

---

### Two Die Rolls

- $A_2$ — **sum equals 7**: pairs $(1,6),(2,5),(3,4),(4,3),(5,2),(6,1)$:
$$P(A_2) = \frac{6}{36} = \frac{1}{6}$$

- $B_2 = \{(1,1),(2,2),(3,3),(4,4),(5,5),(6,6)\}$ — **both results the same**:
$$P(B_2) = \frac{6}{36} = \frac{1}{6}$$

- $C_2$ — **sum at least 10**: pairs with sum 10, 11, or 12:
  - Sum 10: $(4,6),(5,5),(6,4)$ — 3 pairs
  - Sum 11: $(5,6),(6,5)$ — 2 pairs
  - Sum 12: $(6,6)$ — 1 pair
$$P(C_2) = \frac{6}{36} = \frac{1}{6}$$

---

### Three Die Rolls

- $A_3$ — **sum equals 10**: Counting compositions of 10 with three dice values in $\{1,\ldots,6\}$:

  Using the stars-and-bars / direct count method, there are **27** outcomes with sum 10.

$$P(A_3) = \frac{27}{216} = \frac{1}{8}$$

- $B_3$ — **exactly two rolls give the same number**: Choose the repeated value (6 ways), choose its position pair $\binom{3}{2}=3$ ways, choose the third value from remaining 5:

$$|B_3| = 6 \times 3 \times 5 = 90$$
$$P(B_3) = \frac{90}{216} = \frac{5}{12}$$

- $C_3 = \{(2,2,3),(2,3,2),(3,2,2)\}$ — **two twos and one three** (in any order):
$$P(C_3) = \frac{3}{216} = \frac{1}{72}$$

**Additional event (self-defined):**

$D_3$ — **all three rolls show the same number** (triple):
$$D_3 = \{(1,1,1),(2,2,2),(3,3,3),(4,4,4),(5,5,5),(6,6,6)\}$$
$$P(D_3) = \frac{6}{216} = \frac{1}{36}$$

---

## Task 8 — Events and Probabilities in Card Drawing

### Probability assignments

- One card: $P(\omega) = \dfrac{1}{52}$
- Two cards with replacement: $P(\omega) = \dfrac{1}{52^2} = \dfrac{1}{2{,}704}$
- Two cards without replacement: $P(\omega) = \dfrac{1}{52 \times 51} = \dfrac{1}{2{,}652}$

---

### One Card Drawn

- $A_1$ — card is a **heart** (13 hearts):
$$P(A_1) = \frac{13}{52} = \frac{1}{4}$$

- $B_1$ — card is a **king** (4 kings):
$$P(B_1) = \frac{4}{52} = \frac{1}{13}$$

- $C_1$ — card is **not a face card** (52 − 12 face cards = 40):
$$P(C_1) = \frac{40}{52} = \frac{10}{13}$$

---

### Two Cards Drawn (with replacement)

- $A_2$ — **both cards are hearts** ($13 \times 13 = 169$ outcomes):
$$P(A_2) = \frac{13 \times 13}{52 \times 52} = \frac{169}{2704} = \frac{1}{16}$$

- $B_2$ — **both cards have the same rank** (13 ranks, each with $4 \times 4 = 16$ ordered pairs):
$$P(B_2) = \frac{13 \times 16}{2704} = \frac{208}{2704} = \frac{1}{13}$$

- $C_2$ — **at least one ace** (complement: no ace; $48 \times 48 = 2304$ outcomes without any ace):
$$P(C_2) = 1 - \frac{48 \times 48}{2704} = 1 - \frac{2304}{2704} = \frac{400}{2704} = \frac{25}{169}$$

---

### Two Cards Drawn (without replacement)

- $A_3$ — **both cards are hearts** ($13 \times 12 = 156$ ordered pairs):
$$P(A_3) = \frac{13 \times 12}{52 \times 51} = \frac{156}{2652} = \frac{1}{17}$$

- $B_3$ — **both cards have the same rank** (13 ranks, each with $4 \times 3 = 12$ ordered pairs):
$$P(B_3) = \frac{13 \times 12}{2652} = \frac{156}{2652} = \frac{1}{17}$$

- $C_3$ — **one king and one queen in any order** ($4 \times 4 \times 2 = 32$ ordered pairs):
$$P(C_3) = \frac{4 \times 4 \times 2}{2652} = \frac{32}{2652} = \frac{8}{663}$$

**Additional event (self-defined):**

$D_3$ — **the first card is an ace and the second is a king** ($4 \times 4 = 16$ ordered pairs):
$$P(D_3) = \frac{16}{2652} = \frac{4}{663}$$

---

## Task 9 — Events and Probabilities in Weekly Weather Observation

$\Omega_7$: each day independently takes a state from $\{S, C, R\}$ with probability $\frac{1}{3}$ each.

$P(\text{any specific 7-day sequence}) = \left(\frac{1}{3}\right)^7 = \frac{1}{2187}$

Label days: Mon=1, Tue=2, Wed=3, Thu=4, Fri=5, **Sat=6, Sun=7**.

---

### Events

**$A$** — the **entire weekend is sunny** (days 6 and 7 are both $S$):

The remaining 5 days are free (each has 3 choices):
$$P(A) = 1 \times 1 \times 3^5 \cdot \frac{1}{3^7} = \frac{3^5}{3^7} = \frac{1}{3^2} = \frac{1}{9}$$

---

**$B$** — **Wednesday, Thursday, and Friday are all rainy** (days 3, 4, 5 are $R$):

The remaining 4 days are free:
$$P(B) = \frac{3^4}{3^7} = \frac{1}{3^3} = \frac{1}{27}$$

---

**$C$** — **at least one sunny day** (complement: no sunny day at all):

$$P(\text{no sunny day}) = \left(\frac{2}{3}\right)^7 = \frac{128}{2187}$$
$$P(C) = 1 - \frac{128}{2187} = \frac{2059}{2187}$$

---

**$D$** — **no rainy day during the entire week** (each day is $S$ or $C$):

$$P(D) = \left(\frac{2}{3}\right)^7 = \frac{128}{2187}$$

---

**$E$** — **exactly two sunny days**:

Choose 2 days out of 7 for $S$: $\binom{7}{2} = 21$ ways. The remaining 5 days are $C$ or $R$ ($\frac{2}{3}$ each):

$$P(E) = \binom{7}{2} \left(\frac{1}{3}\right)^2 \left(\frac{2}{3}\right)^5 = 21 \cdot \frac{1}{9} \cdot \frac{32}{243} = \frac{21 \times 32}{2187} = \frac{672}{2187} = \frac{224}{729}$$

---

**Additional event (self-defined):**

$F$ — **exactly three rainy days and the rest sunny** (no cloudy days):

Choose 3 days out of 7 for $R$: $\binom{7}{3} = 35$ ways. The other 4 days are $S$.

$$P(F) = \binom{7}{3} \left(\frac{1}{3}\right)^3 \left(\frac{1}{3}\right)^4 = 35 \cdot \frac{1}{3^7} = \frac{35}{2187}$$

---

## Task 10 — Events and Probabilities in Buffon's Needle Experiment

**Setup:** $L \leq d$, $X \sim \text{Uniform}\left[0, \frac{d}{2}\right]$, $\theta \sim \text{Uniform}\left[0, \frac{\pi}{2}\right]$, independent.

The area of the full sample space:
$$|\Omega| = \frac{d}{2} \cdot \frac{\pi}{2} = \frac{\pi d}{4}$$

The needle **intersects a line** if and only if:
$$X \leq \frac{L}{2}\sin\theta$$

---

### Events

**$A$** — the needle **intersects one of the lines**:

$$P(A) = \frac{1}{\frac{\pi d}{4}} \int_0^{\pi/2} \frac{L}{2}\sin\theta \, d\theta = \frac{4}{\pi d} \cdot \frac{L}{2} \cdot \left[-\cos\theta\right]_0^{\pi/2} = \frac{4}{\pi d} \cdot \frac{L}{2} \cdot 1 = \frac{2L}{\pi d}$$

---

**$B$** — the needle **does not intersect any line** (complement of $A$):

$$P(B) = 1 - \frac{2L}{\pi d}$$

---

**$C$** — the **angle is smaller than $\frac{\pi}{6}$**:

$\theta$ is uniform on $\left[0, \frac{\pi}{2}\right]$, so:
$$P(C) = \frac{\pi/6}{\pi/2} = \frac{1}{3}$$

---

**$D$** — the **center of the needle falls at a distance less than $\frac{d}{4}$ from the nearest line**:

$X$ is uniform on $\left[0, \frac{d}{2}\right]$, so:
$$P(D) = \frac{d/4}{d/2} = \frac{1}{2}$$

---

**$E$** — the needle **intersects a line AND the angle is greater than $\frac{\pi}{4}$**:

The needle intersects a line when $X \leq \frac{L}{2}\sin\theta$. For $\theta \in \left(\frac{\pi}{4}, \frac{\pi}{2}\right]$:

$$P(E) = \frac{1}{\frac{\pi d}{4}} \int_{\pi/4}^{\pi/2} \frac{L}{2}\sin\theta \, d\theta = \frac{4}{\pi d} \cdot \frac{L}{2} \cdot \left[-\cos\theta\right]_{\pi/4}^{\pi/2}$$

$$= \frac{2L}{\pi d} \left(0 + \frac{\sqrt{2}}{2}\right) = \frac{2L}{\pi d} \cdot \frac{\sqrt{2}}{2} = \frac{L\sqrt{2}}{\pi d}$$

---

**Additional event (self-defined):**

$F$ — the **center of the needle is within $\frac{d}{4}$ of the nearest line AND the angle is at most $\frac{\pi}{4}$**:

Since $X$ and $\theta$ are independent:
$$P(F) = P\!\left(X \leq \frac{d}{4}\right) \cdot P\!\left(\theta \leq \frac{\pi}{4}\right) = \frac{1}{2} \cdot \frac{\pi/4}{\pi/2} = \frac{1}{2} \cdot \frac{1}{2} = \frac{1}{4}$$

---

