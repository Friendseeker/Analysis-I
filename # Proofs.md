# Proofs

For Chapter 2 & Appendix a, the proofs are stored in
<https://docs.google.com/document/d/1Ku0jlRZO5Kit4JJhbBh5hFHnCimUzOeX8XO8VW0fKMA/edit?usp=sharing>.

## Chapter 3

### Lemma 3.1.6 (Single choice)

Let $A$ be a non-empty set. Then there exists an object $x$ such that $x \in A$.

#### Proof

Assume that $\nexists x, x\in A$, hence, $x\in A$ is false for all $x$ (as
Definition 3.1.1 ensures the dichotomy of $x\in A$ and $x \notin A$).

By Axiom 3.2, $\forall x, x \notin \empty$, hence, $x \in \empty$ is false for
all $x$.

Therefore, it holds that $\forall x, x \in A \leftrightarrow x \in \empty$. By
Definition 3.1.4, $A = \empty$, contradiction as desired.

Remark: Note that Predicate Logic is independent of Set Axioms. As to why it can
be used there, it is because Predicate Logic is Logic. We have Axioms and
Mathematical Models in place, then we use Logic to perform deductions on the
Axioms and Mathematical Models.

Hence, compared to Chapter 2, the only difference is that we are using first
order Logic (Predicate Logic) instead of zeroth order Logic (Propositional
Logic).

### Remark 3.1.9

There is only one singleton set for each object $a$.

#### Proof

Assume we have two singleton sets $A, A'$ for object $a$. Then, $x \in A$ iff
$x = a$ by Axiom 3.3, and $x \in A'$ iff $x = a$ by Axiom 3.3. Hence by
transitivity $x \in A \Leftrightarrow x \in A'$. By Definition 3.1.4,
$(x \in A \Leftrightarrow x \in A') \Leftrightarrow A = A'$, as desired.

Given any two objects $a$ and $b$, there is only one pair set formed by $a$ and
$b$

#### Proof

Assume there exists two pair sets $P, P'$ for objects $a, b$. Then, Then,
$x \in P$ iff $x = a \lor x = b$ by Axiom 3.3, and $x \in P'$ iff
$x = a \lor x = b$ by Axiom 3.3. The rest of the proof follows from proof for
"There is only one singleton set for each object $a$."

$\{a, a\} = \{a\}$ (aka pair set of $a, a$ is $\{a\}$

Proof

Denote $A = \{a, a\}, A' = \{a\}$, then, $x \in A$ iff $x = a \lor x = a$ by
Axiom 3.3. aka, $x \in A$ iff $x = a$. Similarly, $x \in A'$ iff $x = a$ by
Definition 3.1.1. Similar reasoning (based on transitivity) follows.

Hence, Axiom 3.3 is redundant, in the way that if pair set exists, we can
construct singleton sets from pair sets. We can also construct pair set from
singleton set and Axiom 3.4.

### Exercise 3.1.1

Show that the definition of equality in Definition 3.1.4 is reflexive,
symmetric, and transitive.

Proof:

By definition of equality: $$\forall x, x \in A \Leftrightarrow x \in B$$

Note that $\Leftrightarrow$ is reflexive, symmetric and transitive, hence set
equality is also reflexive, symmetric and transitive.

### Exercise 3.1.2

Show $ ∅, \{∅\}, \{\{∅\}\},\{∅, \{∅\}\}$ are distinct.

Proof:

We need to show:

- $∅$ is distinct from all other sets
- $\{∅\}$ is distinct from $\{\{∅\}\},\{∅, \{∅\}\}$
- $\{\{∅\}\} $ is distinct from $\{∅, \{∅\}\}$

Part 1: $∅$ is distinct from all other sets

By Axiom 3.3:

- $\empty \in \{∅\}, \{∅, \{∅\}\}$
- $\{∅\} \in \{\{∅\}\}$

By Lemma 3.1.6, All 3 other sets are non-empty, as desired.

Part 2: $\{∅\}$ is distinct from $\{\{∅\}\},\{∅, \{∅\}\}$

Assume $\{∅\} = \{\{∅\}\}$, then by Definition 3.1.4,
$\empty \in \{∅\} \Leftrightarrow  \empty \in\{\{∅\}\}$. However,
$\empty \in \{∅\}$ is true while $ \empty \in\{\{∅\}\}$ is false (By Axiom 3.3),
contradiction as desired.

Showing $\{∅\} \neq \{∅, \{∅\}\}$ is similar.

Part 3: $\{\{∅\}\} $ is distinct from $\{∅, \{∅\}\}$

Similar to Part 2.

### Remark 3.1.12

Show Pairwise Union (as defined in Axiom 3.4) satisfies substitution axiom.

Aka:

- If $A, B, A'$ are sets, and $A$ is equal to $A'$, then $A ∪ B$ is equal to
  $A' ∪ B$
- If $B'$ is a set which is equal to $B$, then $A ∪ B$ is equal to $A ∪ B'$

Proof

WLOG we prove the first case. (Proof for second case is similar)

We have:

$x \in A \cup B \Leftrightarrow (x\in A \lor x\in B)$

$x \in A' \cup B \Leftrightarrow (x\in A' \lor x\in B)$

Since $A = A'$, $x \in A \Leftrightarrow x \in A'$ (By Definition 3.1.4). Hence:

$x \in A' \cup B \Leftrightarrow (x\in A \lor x\in B)$

Therefore, by transitivity, $x \in A \cup B \Leftrightarrow x \in A' \cup B$. By
definition 3.1.4, $A \cup B = A' \cup B$ as desired.

### Lemma 3.1.13

- If $a$ and $b$ are objects, then $\{a, b\} = \{a\} ∪ \{b\}$.
- If $A, B, C$ are sets, then the union operation
  - is commutative (i.e., $A \cup B = B\cup A$)
  - is associative (i.e., $(A∪B)∪C = A∪(B∪C)$).
- Also, we have $A ∪ A = A ∪ \empty = \empty ∪ A = A$.

Proof

This is actually 4 Lemmas.

Part 1: Pair set can be constructed from singleton set & Pairwise Union

Proof

We have $x \in \{a, b\} \Leftrightarrow (x = a) \lor (x = b)$ (By Axiom 3.3)

We have $x \in \{a\} ∪ \{b\} \Leftrightarrow (x = a) \lor (x = b)$ (By Axiom
3.4)

Hence by transitivity, $x \in \{a, b\} \Leftrightarrow x \in \{a\} ∪ \{b\}$. By
definition 3.1.4, $\{a, b\} = \{a\} ∪ \{b\}$ as desired.

Part 2: Pairwise Union is commutative

Proof

By Axiom 3.4:

- $x \in A \cup B \Leftrightarrow x \in A \lor x \in B$
- $x \in B \cup A \Leftrightarrow x \in B \lor x \in A$

By propositional logic,
$(x \in A \lor x \in B) \Leftrightarrow (x \in B \lor x \in A)$. Hence, by
transitivity $x \in A \cup B \Leftrightarrow x \in B \cup A$. By Definition
3.1.4 $x \in A \cup B = x \in B \cup A$ as desired.

Part 3: Pairwise Union is associative

By Axiom 3.4:

- $x \in A \cup (B \cup C) \Leftrightarrow x \in A \lor x \in (B \cup C)$
- $x \in (A \cup B) \cup C \Leftrightarrow x \in (A \cup B) \lor x \in C$

Hence, note $x \in A \cup B \Leftrightarrow x \in A \lor x \in B$, therefore
since $\Leftrightarrow$ is analogous to equality in propositional logic, we can
employ substitution axiom:

- $x \in (A \cup B) \cup C \Leftrightarrow x \in A \lor x \in B \lor x \in C$

Similarly, we can show:

- $x \in A \cup (B \cup C) \Leftrightarrow x \in A \lor x \in B \lor x \in C$

By transitivity,
$x \in A \cup (B \cup C) \Leftrightarrow x \in (A \cup B) \cup C$, by definition
3.1.4 $A \cup (B \cup C) = (A \cup B) \cup C$ as desired.

Part 4: $A ∪ A = A ∪ \empty = \empty ∪ A = A$

$A ∪ \empty = \empty ∪ A$ follows from commutativity. Remains to show that:

- $A \cup A = A$
- $A \cup \empty = A$

For $A \cup A = A$, note (by Axiom 3.4):

$x \in A \cup A \Leftrightarrow x \in A \lor x \in A$

And since $x \in A \lor x \in A = x \in A$ (by propositional logic), we use
substitution axiom.

$x \in A \cup A \Leftrightarrow x \in A$

Similarly by Axiom 3.4:

$x \in A \Leftrightarrow x \in A$

Rest follows from transitivity and Definition 3.1.4.

For $A \cup \empty = A$, by Axiom 3.4:

$x \in A \cup \empty \Leftrightarrow x \in A \lor x \in \empty$

Since $x \in \empty$ is always false (By Axiom 3.2), above can be simplified
using propositional logic.

$x \in A \cup \empty \Leftrightarrow x \in A$

Note:

$x \in A \cup A \Leftrightarrow x \in A$

Rest follows from transitivity and Definition 3.1.4.

### Proposition 3.1.18 (Sets are partially ordered by set inclusion)

Let $A,B,C$ be sets. If $A⊆B$ and $B⊆C$ then $A⊆C$. If $A⊆B$ and $B ⊆ A$, then
$A = B$. Finally, if $A \subsetneq B$ and $B \subsetneq C$ then
$A \subsetneq C$.

Proof

Part 1: If $A⊆B$ and $B⊆C$ then $A⊆C$

By definition 3.1.15:

- $x \in A \rightarrow x \in B$
- $x \in B \rightarrow x \in C$

We need to show:

- $x \in A \rightarrow x \in C$

Above can be shown with propositional logic. Can either use propositional logic
laws or enumerate through all $8$ states.

Part 2: If $A⊆B$ and $B ⊆ A$, then $A = B$

By definition 3.1.15, we have:

- $x \in A \rightarrow x \in B$
- $x \in B \rightarrow x \in A$

We need to show (from definition 3.1.4):

- $x \in A \leftrightarrow x \in B$

Similarly we can use propositional logic to perform the deduction.

Part 3: if $A \subsetneq B$ and $B \subsetneq C$ then $A \subsetneq C$

Ah now I need first order logic there...

- $\forall x, x \in A \rightarrow x \in B$
- $\forall x, x \in B \rightarrow x \in C$
- $\sim \forall x, x \in A \leftrightarrow x \in B$
- $\sim \forall x, x \in B \leftrightarrow x \in C$

Need to show:

- $\forall x, x \in A \rightarrow x \in C$
- $\sim \forall x, x \in A \leftrightarrow x \in C$

Part 1: $\forall x, x \in A \rightarrow x \in C$

We can combine first 2 statements to form:

- $\forall x, (x \in A \rightarrow x \in B) \land (x \in B \rightarrow x \in C)$

Above, by propositional logic, simplifies to:

$\forall x, x \in A \rightarrow x \in C$

As desired.

Part 2: $\sim \forall x, x \in A \leftrightarrow x \in C$ (aka $A != C$)

Note: I tried to find a formalized predicate logic textbook, and my brain is now
exploded. The deductions are... painful and there's no more truth table cheese.

Hence I will get slightly informal in my deduction. However, as a remainder to
myself there's always a formal way to do it. And, I strongly suspect that the
below proof can be directly converted into a formal proof.

Assume $A = C$, then all element of $C$ is in $A$ (Definition 3.1.4). However,
since $B \subsetneq C$, some element $x \in C$ is not in $B$ (Follows from
simple contradiction from Definition 3.1.4 and Definition 3.1.15). There are two
cases: $x \in A$ and $x \notin A$ (Definition 3.1.1)

Case 1: $x \in A$

Then, $x \in B$ as $A \subsetneq B$ (Definition 3.1.15). Contradiction as
$x \notin B$.

Case 2: $x \notin A$

Then, since $x \in C$, by definition 3.1.4 it must hold that $x \in A$.
Contradiction.

Hence, in neither case, $A = C$, as desired.

### Proposition 3.1.28 (Sets form a boolean algebra)

Let $A, B, C$ be sets, and let $X$ be a set containing $A, B, C$ as subsets.

- (a) (Minimal element) We have $A∪∅=A$ and $A∩∅=∅$.
- (b) (Maximal element) We have $A ∪ X = X$ and $A ∩ X = A$.
- (c) (Identity) We have $A∩A=A$ and $A∪A=A$.
- (d) (Commutativity) We have $A∪B=B∪A$ and $A∩B=B∩A$.
- (e) (Associativity) We have $(A∪B)∪C = A∪(B∪C)$ and $(A∩B)∩C = A ∩ (B ∩ C)$.
- (f) (Distributivity) We have $A∩(B∪C) = (A∩B)∪(A∩C)$ and
  $A ∪ (B ∩ C) = (A ∪ B) ∩ (A ∪ C)$.
- (g) (Partition) We have $A ∪ (X\backslash A) = X$ and
  $A ∩ (X\backslash A) = ∅$
- (h) (de Morgan laws) we have
  $X\backslash(A ∪ B) = (X\backslash A) ∩ (X\backslash B)$ and
  $x\backslash (A ∩ B) = (X\backslash A) ∪ (X\backslash B)$.

Proof

a)

Follows from Lemma 3.1.13

b)

Part 1

By Axiom 3.4:

$$x \in A \cup X \Leftrightarrow x \in A \lor x \in X$$

By Definition 3.1.15 $$x \in A \rightarrow x \in X$$

Therefore:

$$x \in A \cup X \Leftrightarrow x \in X$$

Hence by definition of equality $A \cup X = X $ as desired.

Part 2

By definition 3.1.23:

$$x \in A \cap X \Leftrightarrow x \in A \land x\in X$$

By Definition 3.1.15 $$x \in A \rightarrow x \in X$$

Hence, if $x \in A$, then $x \in A \land x\in X$ is true, if $x \notin A$, then
$x \in A \land x\in X$ is false. Therefore:

$$x \in A \cap X \Leftrightarrow x \in A$$

As desired.

c)

Part 1

Follows from Lemma 3.1.13

Part 2

By Definition of intersection:

$$x \in A \cap A \Leftrightarrow x \in A \land x \in A$$

By propositional logic, $x \in A \land x \in A$ simplifies to $x \in A$, hence:

$$x \in A \cap A \Leftrightarrow x \in A $$

As desired.

d)

Part 1:

Follow from Lemma 3.1.13

Part 2:

By Definition of intersection:

$$x \in A \cap B \Leftrightarrow x \in A \land x \in B$$

$$x \in B \cap A \Leftrightarrow x \in B \land x \in A$$

Since $\land$ is commutative:

$$x \in B \cap A \Leftrightarrow x \in A \land x \in B$$

Hence, by transitivity:

$$x \in A \cap B \Leftrightarrow x \in B \cap A$$

As desired.

e)

Part 1:

Follow from Lemma 3.1.13

Part 2:

Similar to proof for Lemma 3.1.13, hence omitted

f)

Again we can reduce the problem to propositional logic.

Part 1

$$x \in A \cap (B \cup C) \Leftrightarrow x \in A \land (x \in B \lor x \in C)$$

$$x \in (A \cup B) \cap (A \cup C) \Leftrightarrow x \in (A \cup B) \land x \in (A \cup C)$$

We perform further expansion:

$$x \in (A \cup B) \cap (A \cup C) \Leftrightarrow (x \in A \lor x \in B) \land (x \in A \lor x \in C)$$

We remains to show that
$(x \in A \lor x \in B) \land (x \in A \lor x \in C)\Leftrightarrow (x \in B \lor x \in C)$,
which follows from propositional logic, as desired.

Part 2:

Similar to part 1.

g) h)

We similarly:

- Apply the definition
- Use propositional logic
- Transitivity + Definition of set equality

### Exercise 3.1.5

Let $A,B$ be sets. Show that the three statements $A ⊆ B, A ∪ B = B, A ∩ B = A$
are logically equivalent (any one of them implies the other two).

Proof:

We have $A \subseteq B$ if $x \in A \rightarrow x \in B$.

We have $A \cup B = B$ if $x \in A \lor x \in B \Leftrightarrow x \in B$

We have $A \cap B = A$ if $x \in A \land x \in B \Leftrightarrow x \in A$

We can use propositional logic to prove that the above 3 are equivalent. Simply
enumerate all 4 configurations in truth table.

### Exercise 3.1.7

- Let $A,B,C$ be sets. Show that $A∩B ⊆ A$ and $A∩B ⊆ B$.

- Furthermore, show that $C⊆A$ and $C⊆B$ if and only if $C⊆A∩B$.

- In a similar spirit, show that $A ⊆ A ∪ B$ and $B ⊆ A ∪ B$, and furthermore
  that $A⊆C$ and $B⊆C$ if and only if $A∪B⊆C$.

Proof

Part 1

WLOG consider the first equation. We need to show $x \in A$ from
$x \in A \land x \in B$. This is trivially true as $x \in A \land x \in B$ is
true implies that $x \in A$.

Part 2 & 3

Similar reasoning follows. Propositional Logic for the win.

### Exercise 3.1.11. Show that the axiom of replacement implies the axiom of specification

To construct $\{x \in A: P(x)\}$, we construct $P(x, y)$ such that it is true
iff $P(x)$ is true and $y = x$. $P(x,y)$ is permissible as there's at most one
$y$ for each $x$ such that $P(x,y)$ is true (with the one $y$ being $y = x$).

Hence, via Axiom of specification we construct the set:

$$\{y: P(x,y) \land x \in A\}$$

We need to prove that the set is equal to $\{x \in A: P(x)\}$.

Note, an element $y' \in \{y: P(x,y) \land x \in A\}$ if and only if
$P(x, y') \land (x \in A)$, which is $P(x) \land (y' = x) \land (x \in A)$.

Similarly, an element $y' \in \{x \in A: P(x)\}$ iff $P(y') \land (y' \in A)$.

Note, $P(x) \land (y' = x)$ iff $P(y')$ by axiom of substitution. Hence,
$P(x) \land (y' = x) \land (x \in A)$ iff $P(y') \land (y' \in A)$

Rest follows from transitivity and definition for set equivalence.

### Contradiction via introduction of Axiom 3.8

We can construct:

$$\Omega = \{x: x \; \text{is a set} \land x \notin x\}$$

Now, $\Omega \in \Omega$ leads to contradiction (due to $x \notin x$
constraint.). Hence, it must hold that $\Omega \notin \Omega$. However, since
$\Omega$ is a set and $\Omega \notin \Omega$, $\Omega$ satisfies the condition
to be in $\Omega$ (aka $\Omega \in \Omega$), contradiction as desired (as
neither $\Omega \in \Omega$ nor $\Omega \notin \Omega$)

Hence Axiom 3.8 cannot be introduced as an axiom.

### Exercise 3.2.1

Show that the universal specification axiom, Axiom 3.8, if assumed to be true,
would imply Axioms 3.2, 3.3, 3.4, 3.5, and 3.6. (If we assume that all natural
numbers are objects, we also obtain Axiom 3.7.) Thus, this axiom, if permitted,
would simplify the foundations of set theory tremendously (and can be viewed as
one basis for an intuitive model of set theory known as “naive set theory”).
Unfortunately, as we have seen, Axiom 3.8 is “too good to be true”!

Proof

Axiom 3.2

Let $P(x)$ always return false.

Axiom 3.3

Let $P(x)$ be $x = a$ (for singleton set)

Let $P(x)$ be $x = a \lor x = b$ (for pair set)

Axiom 3.4

Let $P(x)$ be $x \in A \lor x \in B$

Axiom 3.5

Let $P'(x)$ be $x \in A \land P(x)$.

Axiom 3.6

Let $P(y)$ be $P(x,y) \; \text{is true for some} \; x \in A$.

Axiom 3.7

Under the assumption that all natural number are objects:

Let $P(x)$ be $x$ is a natural number.

### Exercise 3.2.2

Part 1:

Assume $A$ exists, and $A \in A$, then by Axiom 3.3, $\{A\}$ exists. Hence, by
Axiom 3.9, $\{A\}$ must contain an element that is either not a set, or a set
that is disjoint from $\{A\}$.

By Axiom 3.3, only $A \in \{A\}$, hence it must hold that $A$ must be disjoint
from $\{A\}$. (aka $A \cap A' = \empty$)

However, $A \in A$ and $A \in \{A\}$, indicating that $A \in A \cap \{A\}$ (By
definition of intersection). Contradiction as desired.

Part 2:

Equivalent of showing that :

- $A \in B \land B \in A$ never happens
- All 3 others can happen
  - Existence by example is sufficient.
  - e.g. $(\{1,2\}, \{1\})$, $(\{1\}, \{2\}), (\{1\}, \{1,2\})$

By Axiom 3.3, we construct the pair set $\{A, B\}$. Hence, by Axiom 3.9,
$\{A, B\}$ must contain an element that is either not a set or a set that is
disjoint from $\{A, B\}$.

The element must be either be $A$ or $B$ (By Axiom 3.3). The element cannot be
$A$, as:

$$B \in \{A, B\} \cap A$$

Contradiction.

The element cannot be $B$, as:

$$A \in \{A, B\} \cap B$$

Contradiction.

Hence in either case we reach contradiction, as desired.

### Exercise 3.2.3

Show (assuming the other axioms of set theory) that the universal specification
axiom, Axiom 3.8, is equivalent to an axiom postulating the existence of a
“universal set” Ω consisting of all objects (i.e., for all objects x, we have x
∈ Ω). In other words, if Axiom 3.8 is true, then a universal set exists, and
conversely, if a universal set exists, then Axiom 3.8 is true. (This may explain
why Axiom 3.8 is called the axiom of universal specification). Note that if a
universal set Ω existed, then we would have Ω ∈ Ω by Axiom 3.1, contradicting
Exercise 3.2.2. Thus the axiom of foundation specifically rules out the axiom of
universal specification.

Proof

Converse:

If $\Omega$ exists, then we can apply Axiom 3.5 to $x \in \Omega$ to obtain
axiom of universal specification.

Other direction:

Use Axiom 3.8 with property $P(x): x \; \text{is an object}$.

### Lemma 3.3.12 (Composition is associative)

Part 1: Show that $f\circ(g\circ h), (f\circ g)\circ h$ have the same domain &
range.

Reason: they may have different domain & range, and they are equal in the
intersection of domain & range, which is a false positive.

Proof

$g \circ h$ maps from $X \to Z$ (by definition of composition), hence
$f\circ(g\circ h)$ maps from $X \rightarrow W$ (by definition of composition)

Similarly $(f\circ g)\circ h$ also maps from $X \rightarrow W$, as desired.

Part 2: Show that $f\circ(g\circ h) = (f\circ g)\circ h$

Proof

Via definition of composition, $f\circ(g\circ h) = f(g(h(x)))$. Similarly,
$(f\circ g)\circ h = f(g(h(x)))$. Hence, by transitivity of equality
$f\circ(g\circ h) = (f\circ g)\circ h$ as desired.


### Corollary of Definition 3.3.1

Show that Function obeys axiom of substitution.

Proof:

Assumption: Property satisfies Axiom of substitution.

Need to show $x = x' \rightarrow f(x) = f(x')$

Note, $P(x, f(x)), P(x', f(x'))$ are true, by definition of function.

Hence, by Axiom of substitution (on property), $P(x, f(x)), P(x, f(x'))$ are
both true. By definition of function, there's exactly one $y$ such that
$P(x, y)$ is true. Hence, it must hold that $y = f(x) = f(x')$ (otherwise there
will be at least two different $y$, being $f(x)$ and $f(x')$). As desired.

### Exercise 3.3.1

Show that the definition of equality in Definition 3.3.7 is reflexive, symmetric, and transitive.

Reflexivity:

Say we have $f: X \rightarrow Y$, then, by definition of equality, we need to show:

$\forall x, f(x) = f(x)$

Note $f(x)$ has a single output $y$ (By definition of function). Since $f$ also satisfies Axiom of substitution, $f(x) = f(x)$ as desired.

Symmetricity:

Need to show if $f = g$, then $g = f$.

Say if $f = g$, then by definition of equality, if must hold that:

- $f, g$ has same domain & range.
- $\forall x, f(x) = g(x)$

The condition for $g = f$ are (by definition of equality):

- $g, f$ has same domain & range.
- $\forall x, g(x) = f(x)$

Which are the same as:

- $f, g$ has same domain & range.
  - By symmetry of set equality
- $\forall x, f(x) = g(x)$
  - By symmetry of object equality.

As desired.

Transitivity:

Need to show if $f = g$ and $g = h$, then $f = h$.

Aka, need to show:

- $f, h$ has same domain & range.
- $\forall x, f(x) = h(x)$

Since $f,g$ and $g,h$ has same domain and range, it must hold that $f, h$ has same domain & range, by transitivity of set equality.

Also, since $\forall f(x) = g(x) \land g(x) = h(x)$, it holds that $f(x) = h(x)$ as desired.

Composition obeys the axiom of substitution.

Proof

Need to show $x = x' \rightarrow g(f(x)) = g(f(x'))$

Since function satisfies axiom of substitution, we have $f(x) = f(x')$. For convenience let $y = f(x), y' = f(x'), y = y'$. Hence we remain to show that $g(y) = g(y')$, which is true by axiom of substitution, as desired.

### Exercise 3.3.2

Part 1: $f,g$ injective implies $g(f(x))$ is injective

We directly show $x \neq x' \rightarrow g(f(x)) = g(f(x'))$.

Since $f$ is injective, $f(x) \neq f(x')$ (by definition of injectivity). Similarly it must hold that $g(f(x)) = g(f(x'))$ as desired.

Part 2: $f,g$ surjective implies $g(f(x))$ is surjective

Say $f: X \rightarrow Y$ and $g: Y \rightarrow Z$, then $g(f(x)): X \rightarrow Z$.

Need to show $\forall z\in Z, \exists x, g(f(x)) = z$.

Direct Proof:

Since $g$ is surjective, by definition of surjectivity, $\exists y, g(y) = z$. Hence, we need to show $\exists x, f(x) = y$. By definition of surjectivity, $x$ must exist as desired.

### Exercise 3.3.3

 When is the empty function $f: \empty \rightarrow Y$ $injective? surjective? bijective?

Injectivity:

Always satisfied. Assume injectivity is not satisfied, then there exists $x \neq x', f(x) = f(x')$, requiring that $x, x' \in \empty$, contradiction as desired.

Surjectivity:

Only when $Y = \empty$. If we have $y \in Y$, then surjectivity is not satisfied as there exists no $x$ such that $f(x) = y$ (necessity). In addition if $Y = \empty$, surjectivity is vacuously true (sufficiency).

Bijective:

$Y = \empty$, being the necessary and sufficient condition for surjectivity.

### Exercise 3.3.4

Part 1

We have:

- $\forall x \in X, g(f(x)) = g(\hat{f}(x))$
- $g$ is injective

Need to show:

$\forall x \in X, f(x) = \hat{f}(x)$

Proof

By injectivity of $g$, it holds that $\forall x \in X, f(x) = \hat{f}(x)$, as desired. (as $g(f(x)) = g(\hat{f}(x)) \rightarrow f(x) = \hat{f}(x)$).

If $g$ is not injective, then it is false. e.g. we can have $g$ be constant function. Hence, regardless of $f$, $g(f(x)) = g(\hat{f}(x))$ holds.

Part 2

We have:

- $\forall x \in X, g(f(x)) = \hat{g}(f(x))$
- $f$ is surjective

Need to show:

$\forall y \in Y, g(y) = \hat{g}(y)$

Proof

Choose an arbitrary $y$. It must hold that $y = f(x)$ (by surjectivity of $f$). Hence, $g(y) = g(f(x)), \hat{g}(y) = \hat{g}(f(x))$. Since $g(f(x)) = \hat{g}(f(x))$, $g(y) = \hat{g}(y)$ by transitivity as desired.

If $f$ is not surjective, then it is false. As, there must be $y$ not in range of $f(x)$, and $g(y)$ may not equal to $\hat{g}(y)$ at such points.

### Exercise 3.3.5

Part 1

Since $g(f(x))$ is injective, it holds that for $x, x' \in X$, $x \neq x' \rightarrow g(f(x)) \neq g(f(x'))$.

Assume $f$ is not injective, then there exists $x, x' \in X$  s.t. $x \neq x, f(x) = f(x')$. Then, there exists $x \neq x', g(f(x)) = g(f'(x))$. Contradiction as desired.

Injectivity of $g$ is not necessary, by example, $g(x): \{1,2\} \rightarrow \{1\}$, being constant function that maps everything to $1$.

And $f:  \{1,2\} \rightarrow \{1\}$, mapping only $1$ to $1$. The composition is injective, yet $g$ is not injective.

Part 2

Since $g(f(x))$ is surjective, it holds that $\forall z \in Z, \exists y, z = g(y)$.

Assume $g$ is not surjective, then there exists 

### Exercise 3.3.6

Part 1:

Recall the definition of $f^{-1}(y)$, it is implicitly defined as:

$$\forall y \in Y, \forall x \in X, f^{-1}(y) = x \Leftrightarrow f(x) = y$$

(Aka $f(x) = y$ is the desired property)

We proceed with two steps:

- Show that the property is permissible
  - If the property is not permissible, then we can prove everything via absurdum, by treating something that is not a function as a function.
- Show that $f^{-1}(f(x)) = x$

Permissibility:

We need to show there's exactly one $x$ s.t. $f(x) = y$.

Note, there's at least one $x$ s.t. $f(x) = y$ by surjectivity. Assume, there exists more than one $x$, say $x \neq x', f(x) = y \land f(x') = y$, then $f$ is not injective, contradiction. Hence there's exactly one $x$ such that $f(x) = y$, as desired.

Remark: We has also shown the converse. If $f$ is not invertible (aka the property is not permissible), then there's either no $x$ or more than one $x$ s.t. $f(x) = y$, which implies that $f$ is not bijective. Hence bijectivity = invertibility. 

Show that $f^{-1}(f(x)) = x$:

We first show that $f(x)$ is in the domain of $f^{-1}$, aka $f(x) \in Y$.

- The motivation is again, to ensure no absurdity happens

Since $f: X \rightarrow Y$, it follows that $f(x) \in Y$ by definition of function, as desired.

Hence, say we have $f^{-1}(f(x))$. Then denote $y = f(x)$. $f^{-1}(y)$ therefore evaluates to the only object $x'$ such that $y = f(x')$. Since $f$ is injective, $f(x) = f(x') \rightarrow x = x'$. Hence $f^{-1}(f(x)) = x' = x$ as desired.

Part 2:

We need to show:

- $f^{-1}(y)$ is in the domain of $f$ (aka $f^{-1}(y) \in X$)
- $f(f^{-1}(y)) = y$

For the first statement, note $f^{-1}: Y \rightarrow X$ by definition, as desired.

For the second statement, denote $f^{-1}(y) = x$, then, by definition of inverse function, it must hold that $f(x) = y$. Hence, we can use Axiom of substitution (substitute $f^{-1}(y) = x$ into $f(x) = y$) to conclude $f(f^{-1}(y)) = y$, as desired.

Part 3:

We first show that $f^{-1}$ is invertible.

In Part 1, it is shown that invertibility = bijectivity, hence it remains to show that $f^{-1}$ is bijective. 

Surjectivity:

Need to show $\exists y \in Y$ s.t. $\forall x \in X, f^{-1}(y) = x$.

Note, for a given $x$, there exists $f(x) = y$. Which, by definition of inverse function implies $f^{-1}(y) = x$, as desired.

Injectivity:

Need to show $y \neq y' \rightarrow f^{-1}(y) \neq f^{-1}(y')$

Denote $x = f^{-1}(y)$ and $x' = f^{-1}(y')$. Then, assume $x = x'$, it must hold that $f(x) = f(x')$. Since, by definition of inverse function, $f(x) = y, f(x') = y'$, we have $y = y' \land y \neq y'$, contradiction as desired.

Then, note, by Part 1:

$(f^{-1})^{-1}(f^{-1}(y)) = y$

By Part 2:

$f(f^{-1}(y)) = y$

Since $f^{-1}(y)$ is surjective, by Exercise 3.3.4:

$f = (f^{-1})^{-1}$

As desired.

### Exercise 3.3.7

Part 1: Show $g \circ f$ is bijective

Consequence of Exercise 3.3.2.

Part 2: Show $(g \circ f)^{-1} = f^{-1} \circ g^{-1}$

By definition of inverse function:

$$\forall z \in Z, \forall x \in X, (g \circ f)^{-1}(z) = x \Leftrightarrow g(f(x)) = z$$

By definition of inverse function, $g(f(x)) = z \Leftrightarrow f(x) = g^{-1}(z) \Leftrightarrow x = f^{-1}(g^{-1}(z))$.

Hence:

$$\forall z \in Z, \forall x \in X, (g \circ f)^{-1}(z) = x \Leftrightarrow x = f^{-1}(g^{-1}(z))$$

By universal instantiation:

$$\forall z \in Z, (g \circ f)^{-1}(z) = x \Leftrightarrow x = f^{-1}(g^{-1}(z))$$

Hence, by transitivity of equality:

$$\forall z \in Z, (g \circ f)^{-1}(z)  = f^{-1}(g^{-1}(z))$$

Rest follows from definition of function equality, as desired.

### Exercise 3.3.8

a)

Note both sides is a mapping from $X \to Z$ (By definition of composition). Need to show for any arbitrary input $x \in X$, both sides are equal (by definition of function equality.)

Since $X \subseteq Y \subseteq Z$, it holds that $X \subseteq Z$ by proposition 3.1.18. Hence, by definition of inclusion map, $RHS = x$.

For $LHS$, note $\iota_{X \rightarrow Y}(x) = x$ if $x \in X$, and $\iota_{Y \rightarrow Z}(x) = x$ if $x \in Y$. Note $x \in X \rightarrow x \in Y$ by definition of subset.

Hence:

$$
LHS = \iota_{Y \rightarrow Z}(\iota_{X \rightarrow Y}(x)) \\
= \iota_{Y \rightarrow Z}(x) \\
= x \\
= RHS
$$

As desired.

b)

Need to show $f = f \circ \iota_{A \rightarrow A}$ and $f = \iota_{B \rightarrow B} \circ f$.

Similar to $a$, say we are given input $x$, we show LHS = RHS.

Part 1:

Note $f(\iota_{A \rightarrow A}(x)) = f(x)$, as $x \in A$, and by definition of inclusion map $\iota_{A \rightarrow A}(x) = x$ if $x \in A$, as desired.

Part 2:

Note $\iota_{B \rightarrow B}(f(x)) = f(x)$. As, $f: A \rightarrow B$, hence $f(x) \in B$, rest follows from definition of inclusion map.

c)

Since $f$ is bijective, $f^{-1}$ exists. Easy to verify both sides maps from $B \rightarrow B$.

We remains to show $LHS = RHS$ for any arbitrary input $y \in B$.

For $RHS$, since $y \in B$, by definition of inclusion map $RHS = y$.

For $LHS$, by Exercise 3.3.6, $LHS = y$ as desired.

d)

We know $h: X \cup Y \rightarrow Z$, hence by definition of function, we can defined $h$ via finding a permissible property $P(t, z)$.

We let $P(t, z)$ be:

- If $t \in X$, $z = f(t)$
- If $t \in Y$, $z = g(t)$

We proceed to show that the property is permissible. Aka, for every $t \in X \cup Y$, there's exactly one $z$ such that $P(t, z)$ is true.

Given $t \in X \cup Y$, by definition of pairwise union it must hold that $t \in X \lor t \in Y$. By definition of disjoint set it must hold that $t \in X$ and $t \in Y$ cannot be mutually true.

Hence, it must hold that exactly one of $t \in X$ and $t \in Y$ is true. WLOG assume $t \in X$, then there exists exactly one $z$, being $f(t)$, for which $P$ is true, as desired. $f(t)$ is also well defined as $f: X \rightarrow Z$ and $t \in X$.

After defining $h$, we proceed to show that $h$ does satisfy the desired properties. 

- $h\circ \iota_{X→X∪Y} =f $
- $h\circ \iota_{Y→X∪Y} =g $

WLOG we prove $h\circ \iota_{X→X∪Y} =f$. First, easy to verify both sides maps $X \rightarrow Z$. Then, $RHS = f(t)$,

$$
LHS = h\circ \iota_{X→X∪X}(t) \\
    = h (t) \; \text{as} \; \iota_{Y→X∪Y}(t) = t \; (\text{since} \; t \in X) \\
    = f(t) \; \text{as} \; t \in X
$$

As desired.

Challenge: Construct Image of sets with Axiom of specification

Choose $Y$ as the set, $\exists x, y = f(x)$ as the filtering property.

### Exercise 3.4.1

We call the forward image $S$ and inverse image $S'$. By definition of image:

$$S = \{f^{-1}(y): y \in V\}$$
$$S' = \{x \in X: f(x) \in V\}$$

We proceed with 2 steps:

- Show $S \subseteq S'$
- Show $S' \subseteq S$

Then we use Prop 3.1.18 to conclude $S = S'$

Part 1

Need to show $\forall x, x \in S \rightarrow x \in S'$ (by definition of subset)

Proof

Assume $x \in S$, then it holds that $x = f^{-1}(y)$ for some $y \in V$. Since $V \subseteq Y$, $y \in V \rightarrow y \in Y$. Hence $f^{-1}(y)$ is well defined and it holds that $x \in X$ (as $f^{-1}: Y \rightarrow X$). It also holds that $y = f(x)$ (by definition of inverse function). As $y \in V$, $f(x) \in V$, as desired.

Part 2:

Need to show $\forall x, x \in S' \rightarrow x \in S$ (by definition of subset)

Proof:

Assume $x \in S'$, then it holds that $x \in X$ and $f(x) \in V$. We need to show that there exists $y$ s.t. $x = f^{-1}(y)$ and $y \in V$. We claim that $y = f(x)$ satisfies both conditions.

Since $y = f(x)$, then by definition of inverse function $x = f^{-1}(y)$, as desired.

Since $f(x) = y$, $f(x) \in V \rightarrow y \in V$ as desired.

### Exercise 3.4.2

Part 1:

Claim: $S \subseteq f^{-1}(f(S))$

Note: it cannot hold that $S = f^{-1}(f(S))$ or $S \supseteq f^{-1}(f(S))$ in general, consider $f$ being constant function.

Proof:

Assume $x \in S$. Then, $f(x) \in f(S)$, by definition of image. Then, since $f(x) \in f(S)$, $x \in f^{-1}(f(S))$ by definition of inverse image, as desired.

Part 2:

Claim: $f(f^{-1}(U)) \subseteq U$

Note: Example on page 58 shows it cannot hold that $f(f^{-1}(U)) = U$ or $f(f^{-1}(U)) \supseteq U$ in general.

Proof:

Assume $y \in f(f^{-1}(U))$. There must exist $x \in f^{-1}(U)$ such that $f(x) = y$ (by definition of image). Since $x \in f^{-1}(U)$, it must hold that $f(x) \in U$. Since $f(x) = y$. it holds that $y = f(x) \in U$, as desired.

### Exercise 3.4.3

Part 1

Need to show $y \in f(A \cap B) \rightarrow y \in f(A) \land y \in f(B)$

By definition of image $y \in f(A \cap B)$ only if $\exists x \in A \cap B, f(x) = y$. Hence, it must hold that $x \in A \land x \in B$. Therefore by definition of image $y \in f(A) \land y \in f(B)$ as desired.

The converse is not true. Let $f$ be constant function, and $A, B$ be disjoint sets. $f(A) \cap f(B)$ is not empty, yet $f(A \cap B)$ is empty.

### Part 2

Need to show $y \in f(A) \land y \notin f(B) \rightarrow y \in f(A \backslash B)$

By definition of image, $\exists x \in A, f(x) = y$, and $\forall x \in B, f(x) \neq y$. Hence, it must hold that $\exists x \in A \backslash B, f(x) = y$.

Proof

We know $\exists x \in A, f(x) = y$. Assume $x \in B$. Then, $y \in f(B)$ by definition of image, contradiction. Hence if $x$ exists, it must hold that $x \in A \land x \notin B$, as desired.

Therefore, since $\exists x \in A \backslash B, f(x) = y$, it follows from definition of image that $y \in f(A \backslash B)$, as desired.

The converse is not true, using same construction from Part 1. $f(A \backslash B)$ is nonempty, and $ y \notin f(B)$ is false, as $f(A) = f(B) = \{\text{constant}\}$.

### Part 3

Need to show:

- $y \in f(A) \lor y \in f(B) \rightarrow y \in f(A \cup B)$
- $y \in f(A \cup B) \rightarrow y \in f(A) \lor y \in f(B)$

Proof for the first statement

WLOG $y \in A$. Then, $\exists x \in A, f(x) = y$. Since $A \subseteq A \cup B$ (by Exercise 3.1.7), we have $\exists x \in A \cup B, f(x) = y$. By definition of image $y \in f(A \cup B)$, as desired.

Proof for the second statement

Since $y \in f(A \cup B)$, $\exists x \in A \cup B, y = f(x)$. By definition of pairwise union it must hold that $x \in A$ or $x \in B$ (or both).

WLOG assume $x \in A$, then $\exists x \in A, y = f(x)$, by definition of image, $y \in f(A)$, hence $y \in f(A) \lor y \in f(B)$, as desired.

### Exercise 3.4.4

Part 1

Need to show $\forall x, x \in f^{-1}(U∪V) \leftrightarrow x \in f^{-1}(U)∪f^{-1}(V)$ (By definition of set equality.

Note, $x \in f^{-1}(U∪V)$ iff $f(x) \in U \cup V$ (by definition of inverse image), and $x \in f^{-1}(U)∪f^{-1}(V)$ iff $x \in f^{-1}(U) \lor x \in f^{-1}(V)$ (by definition of pairwise union), which is equivalent to $f(x) \in U \lor f(x) \in V$ (by definition of inverse image). Hence, the predicate is equivalent to:

$\forall x, x \in f(x) \in U \cup V \leftrightarrow f(x) \in U \lor f(x) \in V$

The above is trivially true by definition of pairwise union, as desired.

Part 2, 3

Similar reasoning.

### Exercise 3.4.5

Surjectivity (if direction)

Need to show:

- $y \in f(f^{-1}(S)) \rightarrow y \in S $
- $y \in S \rightarrow y \in f(f^{-1}(S))$

Part 1:

$y \in f(f^{-1}(S))$ implies $\exists x\in f^{-1}(S) , f(x) = y$ (by definition of image). Hence, $\exists y' \in S, f(x) = y'$ (By definition of inverse image). Note $y = f(x)$, hence $y = y' \in S$, as desired.

Part 2:

(Sufficiency)
Assume $y \in S$, then $y \in Y$ as $S \subseteq Y$. Since $y \in Y$, $\exists x, f(x) = y$ by surjectivity. By definition of reverse image, it holds that the same $x$ is in $f^{-1}(S)$. By definition of image, $\exists y' \in f(f^{-1}(S)), f(x) = y'$. Hence, $y = y' \in f(f^{-1}(S))$, as desired.

Surjectivity (only if direction)

Proof by contradiction

Assume we have $f$ non-surjective, which means $\exists y \in Y, \forall x \in X, f(x) \neq y$. Denote that $y$ as $y'$.

Since $y' \in Y$, $\{y'\} \subseteq Y$, hence it must hold that:

$$\{y'\} = f(f^{-1}(\{y'\}))$$

However, $f^{-1}(\{y'\}) = \empty$, as $\forall x \in X, f(x) \neq y'$. Hence, $f(f^{-1}(\{y'\})) = f(\empty) = \empty \neq LHS$, contradiction as desired.

Injectivity (if direction)

- $x \in f^{-1}(f(S)) \rightarrow x \in S $
- $x \in S \rightarrow x \in f^{-1}(f(S))$

Part 1:

Similarly to surjectivity part 1

Part 2:

(Sufficiency) Since $x \in S$, $x \in X$ as $S \subseteq X$. Hence,$\exists y \in f(S), f(x) = y$ (By definition of image). By definition of reverse image, $\exists x' \in f^{-1}(f(S)), f(x') = y$. By injectivity, $f(x') = y \land f(x) = y \rightarrow x = x'$. Hence $x = x' \in f^{-1}(f(S))$, as desired.

Injectivity (only of direction)

Assume $f$ is not injective, then $\exists x_1, x_2 \in X, (x_1 \neq x_2) \land (f(x_1) = f(x_2))$

Consider the set $S = \{x_1\}$. Then, it must hold that

$$S = f^{-1}(f(S))$$

However, note $x_2 \notin S$, yet $x_2 \in f^{-1}(f(S))$. Contradiction as desired.

### Exercise 3.4.6

Intuition: the set hinted by Tao contains all possible partitions for $X$, being $(f^{-1}(0), f^{-1}(1))$ pairs.

Denote the set formed by applying the replacement Axiom on $\{0, 1\}^X$ as $P$, aka:

$$P = \{Y: Y = f^{-1}(\{1\}) \; \text{for some} \; f \in \{0, 1\}^X\}$$

We claim that $2^X =  P$, via showing that:

- $Y \in 2^X \rightarrow Y \in P$
- $Y \in P \rightarrow Y \in 2^X$

Part 1

$Y \in 2^X$ iff $Y \subseteq X$, by definition of power set. Consider the following function $f: X \rightarrow \{0, 1\}$ s.t. $P(x,y)$ being:

- $x \in Y$ and $y = 1$
- $x \notin Y$ and $y = 0$

Above property is permissible as:

- for any input $x$, there's a corresponding output
  - As either $x \in Y$ or $x \notin Y$, at least one of the clauses are true
- Fixing $x$, There's exactly one $y$ that that $P(x,y)$ is true.
  - WLOG if $x \in Y$, then $y = 1$ is the only candidate.

Since $f: X \rightarrow \{0, 1\}$, $f \in \{0, 1\}^X$. Take $Y' = f^{-1}(\{1\})$, by definition of $P$, $Y' \in P$. We remain to show that $Y = Y'$, hence, we show:

- $x \in Y \rightarrow x \in Y'$
- $x \in Y' \rightarrow x \in Y$

First statement:

Given $x \in Y$, note $Y \subseteq X$, hence $x \in X$, which means $x$ is a valid input for $f$. Note $f(x) = 1$ (as $x \in Y$). Hence $f(x) \in \{1\}$, therefore by definition of inverse image, $x \in f^{-1}(\{1\})$, as desired.

Second statement:

Since $x \in f^{-1}(\{1\})$, $f(x) = 1$, by definition of inverse image. Hence, assume $x \notin Y$, then $f(x) = 0 \neq 1$, contradiction as desired.

Part 2

For $Y \in P$, it holds that there's $f: X \rightarrow \{0, 1\}$ s.t. $Y = f^{-1}(\{1\})$. We need to show $Y \in 2^X$, which is equivalent to showing $Y \subseteq X$.

Given $x \in Y$, by definition of inverse image, it holds that $x \in X \land f(x) = y$. Hence, $x \in Y \rightarrow x \in X$, as desired.

### Exercise 3.4.7

By Exercise 3.4.6, the followings are sets:

$$A = \{X':X' \subseteq X\}$$
$$B = \{Y':Y' \subseteq Y\}$$

For each $Y' \in B$, $Y'^{X'}$ is a set. Hence, for each $X' \subseteq X$, denote $A_{X'} = Y'^{X'}$. Then, we construct:

$$B_{Y'} = \bigcup_{X' \in X} A_{X'}$$

We claim:

$$C = \bigcup_{Y' \in B} B_{Y'}$$

Is the desired set.

Proof:

Part 1: Show element in $C$ are partial functions

Say given an element $f \in C$, then by definition of union, $\exists Y' \in B, f \in B_{Y'}$. Since $B_{Y'} = \bigcup_{X' \in X} A_{X'}$, $\exists X' \in A, f \in A_{X'}$. Since $A_{X'} = Y'^{X'}$, it holds that $f: X' \rightarrow Y'$, with $X' \in X, Y' \in Y$, as desired.

Part 2: Show a given partial function is in $C$

Given $f: X'' \rightarrow Y''$ s.t. $X'' \subseteq X, Y'' \subseteq Y$. Note $f \in C$ iff $\exists Y' \in B, f \in B_{Y'}$. We claim $Y' = Y''$ is permissible. Aka, we need to verify:

- $Y'' \in B$
- $f \in B_{Y''}$

The first statement is true by definition of $B$. For the second statement, note $f \in B_{Y''}$ iff $\exists X'' \in A, f \in A_{X''}$, by definition of $B_{Y''}$. We let $X' = X''$. Then, we need to verify:

- $X'' \in A$
- $f \in A_{X''}$

The first one is true, by definition of $A$. For the second one, note $A_{X''} = Y''^{X''}$, hence by definition of power set $f \in A_{X''}$, as desired.


### Exercise 3.4.8

Given two sets $A, B$, we wish to construct a set $A \cup B$ s.t.:

$x \in A \cup B \leftrightarrow x \in A \lor x \in B$

Proof

By Axiom 3.1, $A, B$ are objects. Hence, by Axiom 3.4, $\{A, B\}$ is a set. By Axiom 3.11, there exists a set $U$ s.t.

$$x \in U \leftrightarrow x \in S \; \text{for some} \; S \in \{A, B\}$$

We claim $U = A \cup B$.

Part 1: $x \in A \cup B \rightarrow x \in U$

Given an element $x \in A \cup B$, then it must hold that $x \in A$ or $x \in B$ (or both).

WLOG assume $x \in A$. then since $A \in S$, the property $\exists S \in \{A, B\}, x \in S$ is satisfied, hence $x \in S$ as desired.

Part 2: $x \in U \rightarrow x \in A \cup B$

Given $x \in U$, it holds $\exists S \in \{A, B\}, x \in S$. WLOG let $S = A$, then $x \in A$, hence $x \in A \cup B$ as desired.

### Exercise 3.4.9

For sake of simplicity denote two sets as LHS and RHS.

WLOG we show $LHS \subseteq RHS$.

Assume $x \in LHS$, then it holds that:

- $x \in A_\alpha$ for all $\alpha \in I$

Hence, since $\beta' \in I$, it must hold that:

- $x \in A_{\beta'}$

Hence. since:

- $x \in A_{\beta'}$
- $x \in A_\alpha$ for all $\alpha \in I$

$x \in RHS$, as desired.

### Exercise 3.4.10

Part 1

Need to show:
$$(\bigcup_{\alpha \in I} A_\alpha) \cup (\bigcup_{\alpha \in J} A_\alpha) = \bigcup_{\alpha \in I \cup J} A_\alpha$$

Proof

Assume $x \in (\bigcup_{\alpha \in I} A_\alpha) \cup (\bigcup_{\alpha \in J} A_\alpha)$
, then, by definition of pairwise union, it must either hold that:

- $x \in \bigcup_{\alpha \in I} A_\alpha$
- $x \in \bigcup_{\alpha \in J} A_\alpha$

WLOG assume $x \in \bigcup_{\alpha \in I} A_\alpha$, then, by definition of union, $\exists \beta \in I, x \in A_\beta$. Hence, $\exists \beta \in I \cup J, x \in A_\beta$ (as $I \subseteq I \cup J$ by Exercise 3.1.7). Therefore $x \in \bigcup_{\alpha \in I \cup J} A_\alpha$ as desired.

Note: if $\bigcup_{\alpha \in I} A_\alpha$ is empty, above reasoning still applies to $x \in \bigcup_{\alpha \in J} A_\alpha$, if both are empty, then $LHS \subseteq RHS$ is vacuously true as desired.

For the other direction, assume $x \in \bigcup_{\alpha \in I \cup J} A_\alpha$, then it must hold that $\exists \beta \in I \cup J, x \in A_\beta$. Hence, it must hold that either:

- $\exists \beta \in I, x \in A_\beta$
- $\exists \beta \in J, x \in A_\beta$

(By definition of Pairwise Union)

WLOG say $\exists \beta \in I, x \in A_\beta$, then $x \in \bigcup_{\alpha \in I} A_\alpha$ by definition of union. Hence, $x \in (\bigcup_{\alpha \in I} A_\alpha) \cup (\bigcup_{\alpha \in J} A_\alpha)$ by definition of pairwise union, as desired.

Part 2

Need to show
$$(\bigcap_{\alpha \in I} A_\alpha) \cap (\bigcap_{\alpha \in J} A_\alpha) = \bigcap_{\alpha \in I \cup J} A_\alpha$$

(If $I, J$ are non-empty)

Proof

Given $x \in (\bigcap_{\alpha \in I} A_\alpha) \cap (\bigcap_{\alpha \in J} A_\alpha)$, it must hold that:

- $x \in (\bigcap_{\alpha \in I} A_\alpha)$
- $x \in (\bigcap_{\alpha \in J} A_\alpha)$

By definition of intersection.

Hence, it must hold that:

- $\forall a \in I, x \in A_\alpha$
- $\forall a \in J, x \in A_\alpha$

(By (3.4))

Which can be rewritten as:

- $\forall a, a \in I \rightarrow x \in A_\alpha$
- $\forall a, a \in J \rightarrow x \in A_\alpha$

Combining both:
$$\forall a, (a \in I \rightarrow x \in A_\alpha) \land (a \in J \rightarrow x \in A_\alpha)$$
$$\forall a, (a \in I \lor  a \in J) \rightarrow x \in A_\alpha$$
$$\forall a, a \in I \cup J \rightarrow x \in A_\alpha$$
$$\forall a \in I \cup J, x \in A_\alpha$$

Therefore $x \in \bigcap_{\alpha \in I \cup J} A_\alpha$, as desired.

Other direction:

Given $x \in \bigcap_{\alpha \in I \cup J} A_\alpha$, it must hold that:

- $\forall a \in I \cup J, x \in A_\alpha$

Hence, both of:

- $\forall a \in I, x \in A_\alpha$
- $\forall a \in J, x \in A_\alpha$

holds (via previous reasoning)

Therefore

- $x \in (\bigcap_{\alpha \in I} A_\alpha)$
- $x \in (\bigcap_{\alpha \in J} A_\alpha)$

holds

As desired.

Note: intersection on family of sets is undefined if either of $I, J$ are empty. Hence, important to check if the index set is non-empty when applying intersection lemmas.

For instance, (3.4) is vacuously true for any $y$, if the index set is empty.

This shows the importance of ZFC, as by applying ZFC to construct intersection on family set if becomes obvious that non-emptiness of index is necessary.

Side Note: when taking out an element from a set, need to consider what if the set is empty.

### Exercise 3.4.11

Part 1

Show:

$$X \backslash \bigcup_{\alpha \in I} A_\alpha = \bigcap_{\alpha \in I} (X \backslash A_\alpha)$$

Proof

We show:

- $LHS \subseteq RHS$
- $RHS \subseteq LHS$

For $LHS \subseteq RHS$, note $x \in X \backslash \bigcup_{\alpha \in I} A_\alpha$ iff $x \in X \land x \notin \bigcup_{\alpha \in I} A_\alpha$. Hence, we have:

- $x \in X$
- $\nexists a \in I, x \in A_\alpha$
  - which, by first-order logic, equates to $\forall a \in I, x \notin A_\alpha$

Hence. it holds that:

- $\forall a \in I, x \in X \land x \notin A_\alpha$

Which becomes $\forall a \in I, x \in X \backslash A_\alpha$ as desired.

For $RHS \subseteq LHS$, note given $x \in \bigcap_{\alpha \in I} (X \backslash A_\alpha)$, we have:

$$\forall a \in I, x \in X \backslash A_\alpha$$
$$\forall a \in I, x \in X \land x \notin A_\alpha$$
$$\forall a \in I, x \notin A_\alpha$$

Hence, $x \notin \bigcup_{\alpha \in I} A_\alpha$. Remains to show $x \in X$. Assume $x \in X$, then $\forall a \in I, x \in X \land x \notin A_\alpha$ is either false, or vacuously true (which requires $I$ being empty). Either case is a contradiction, as desired. 

- Note: indeed cannot deduce $x \in X$ directly from $\forall a \in I, x \notin A_\alpha$, but rather can only deduce $x \in X \lor I = \empty$. Need to be careful doing Predicate Logic when the manipulation is outside of what I had seen in CS121.

Part 2:

Show: 
$$X \backslash \bigcap_{\alpha \in I} A_\alpha = \bigcup_{\alpha \in I} (X \backslash A_\alpha)$$

Need to show that:

- $LHS \subseteq RHS$
- $RHS \subseteq LHS$

Part 1

Given $x \in X \backslash \bigcap_{\alpha \in I} A_\alpha$, it must hold that:

- $x \in X$
- $x \notin \bigcap_{\alpha \in I} A_\alpha$
  - Which equates to $\exists \alpha \in I, x \notin A_\alpha$

Hence:

$$\exists \alpha \in I, x \in X \land x \notin A_\alpha$$
$$\exists \alpha \in I, x \in X \backslash A_\alpha$$

As desired.

Part 2

For $x \in \bigcup_{\alpha \in I} (X \backslash A_\alpha)$

We have:

$$\exists \alpha \in I, x \in X \backslash A_\alpha$$
$$\exists \alpha \in I, x \in X \land x \notin A_\alpha$$

Assume $x \notin X$, then $\exists \alpha \in I, x \in X \land x \notin A_\alpha$ is false, contradiction. Hence $x \in X$.

By weakening $\exists \alpha \in I, x \in X \land x \notin A_\alpha$, we deduce:

$$\exists \alpha \in I, x \notin A_\alpha$$

As desired.

### Lemma 3.5.12

We use strong induction.

- Mainly to have $P(1)$ as base case instead of $P(0)$

Base case $P(1)$:

Need to show there exists a $1$-tuple $(x_1)$ s.t. $x_1 \in X_1$, for no-empty set $X_1$.

Note by Lemma 3.1.6, $x_1$ exists, hence, $(x_1)$ exists as desired.

- Exact construction of $(x_1)$ from $x_1$ to be done in future exercises

Inductive Step:

Suppose $P(n)$ is true, then a n-tuple $(x_i)_{1≤i≤n}$ exists such that $x_i ∈ X_i$ for all $1≤i≤n$. Hence, for $(x_i)_{1≤i≤n+1}$, we simply take $(x_i)_{1≤i≤n}$, and take an element $e \in X_{n+1}$ to append it ($e$ exists due to Lemma 3.1.6), as desired.

### Exercise 3.5.1

Part 1: Show that $(x, y) = \{\{x\}, \{x, y\}\}$ satisfies:

$$(x,y) = (x',y') \Leftrightarrow (x = x' \land y = y')$$

Proof:

We show:

$$(x,y) = (x',y') \rightarrow (x = x' \land y = y')$$
$$(x = x' \land y = y') \rightarrow (x,y) = (x',y')$$

First statement

Assume $\{\{x\}, \{x, y\}\} = \{\{x'\}, \{x', y'\}\}$. Then, assume $x \neq x'$, then $\{x\} \neq \{x'\}$ (as $x \in \{x\}$, yet $x \notin \{x'\}$). Then, $\{x\} \in \{\{x\}, \{x, y\}\}$, yet $\{x\} \notin \{\{x'\}, \{x', y'\}\}$ (Assume $\{x\} \in \{\{x'\}, \{x', y'\}\}$, then $\{x\} = \{x', y'\}$, however $y' \notin \{x\}$, contradiction).

Similarly, assume $y \neq y'$, then, $\{x, y\} \neq \{x', y'\}$, As, $y \in \{x, y\}$, and $y \notin  \{x', y'\}$, contradiction. (Unless $y = x'$, however in this case, $y = x' = x$, and similarly we conclude $y' =  x' = x$, hence $y = y'$, contradiction as desired).

Second Statement

Assume $x = x', y = y'$. Then, note:

- $\{x\} \in \{\{x'\}, \{x', y'\}\}$
- $\{x, y\}\ \in \{\{x'\}, \{x', y'\}\}$
- $\{x'\} \in \{\{x\}, \{x, y\}\}$
- $\{x', y'\}\ \in \{\{x\}, \{x, y\}\}$

Rest follows from Definition of set equality, as desired.

### Exercise 3.5.1 (Additional Challenge)

Part 1: Show that $(x, y) = \{x, \{x, y\}\}$ satisfies:

$$(x,y) = (x',y') \Leftrightarrow (x = x' \land y = y')$$

Proof:

We show:

$$(x,y) = (x',y') \rightarrow (x = x' \land y = y')$$
$$(x = x' \land y = y') \rightarrow (x,y) = (x',y')$$

First statement:

Assume $\{x, \{x, y\}\} = \{x', \{x', y'\}\}$. Then, assume $x \neq x'$. Then, $x \in \{x, \{x, y\}\}$, yet $x \notin \{x', \{x', y'\}\}$.

As, $x \in \{x', \{x', y'\}\}$ iff $x = x'$ or $x = \{x', y'\}$. $x = x'$ is false. Hence, only $x = \{x', y'\}$ is possible. Therefore we have:

$$\{\{x', y'\}, \{x, y\}\} = \{x', \{x', y'\}\}$$

Hence, it holds that $x' = \{x, y\}$ or $x' = \{x', y'\}$. Assume $x' = \{x', y'\}$, then $x' = x$, contradiction. Hence, must hold that $x' = \{x, y\}$. 

Therefore, we have:

- $x' = \{x, y\}$
- $x = \{x', y'\}$

Hence $x' \in x$, $x \in x'$. Contradiction by Exercise 3.2.2.

Assume $y \neq y'$, then, $\{x, y\} \neq \{x', y'\}$. (As $y \in \{x, y\}$, yet $y \notin \{x', y'\}$), contradiction. Or, we may have $y \in \{x', y'\}$, if $y = x'$. However, we can then deduce $y' = x$, and hence $y' = x' = x = y$, contradiction as desired.

Second Statement

Assume $x = x', y = y'$, then:

- $x \in \{x', \{x', y'\}\}$
- $\{x, y\}\ \in \{x', \{x', y'\}\}$
- $x' \in \{x, \{x, y\}\}$
- $\{x', y'\}\ \in \{x, \{x, y\}\}$

Rest follows from Definition of set equality, as desired.

Exercise 3.5.2

Part 1

Need to show:

$$(x_i)_{1≤i≤n} = (y_i)_{1≤i≤n}$$

Given LHS, RHS are two surjective functions with domain $\{i \in N : 1 \leq i \leq n\}$, and $\forall i \in \{i \in N : 1 \leq i \leq n\}, x(i) = y(i)$.

Step 1: Verify that two functions have same domain and range.

$x, y$ have same domain, by definition of $n$-tuple. Assume $x$ has range $X$, and $y$ has range $X'$. We proceed to show $X = X'$.

Assume there exists $e \in X$. Then, by surjectivity of $x$, $\exists i \in \{i \in N : 1 \leq i \leq n\}, x(i) = e$. Since $\forall i \in \{i \in N : 1 \leq i \leq n\}, x(i) = y(i)$, it holds that:

$$\exists i \in \{i \in N : 1 \leq i \leq n\}, y(i) = e$$

Hence $e \in X \rightarrow e \in X'$. Similarly we show $e \in X' \rightarrow e \in X$, hence $X = X'$, as desired.

With domain & range shown to be identical, by definition of function equality $x, y$ are equal iff:

$$\forall i \in \{i \in N : 1 \leq i \leq n\}, x(i) = y(i)$$

Which is a priori, as desired.

Part 2

Need to show:

$$\forall i \in \{i \in N : 1 \leq i \leq n\}, x(i) = y(i)$$

Given $x = y$, $x, y$ surjective and $x,y$ has domain $\{i \in N : 1 \leq i \leq n\}$.

Proof: by definition of function equality, it must hold that:

$$\forall i \in \{i \in N : 1 \leq i \leq n\}, x(i) = y(i)$$

As desired.

Part 3

Need to show:

$$\prod_{1≤i≤n}X_i = \{(x_i)_{1≤i≤n} :x_i ∈ X_i \text{ for all } 1≤i≤n\}.$$

is a set

For which $(X_i)_{1 \leq i \leq n}$ is an ordered $n$-tuple of sets.

Proof

Lemma: $\prod_{1≤i≤n}X_i$ contains only functions with domain $\{i \in N : 1 \leq i \leq n\}$, and range being subset of $\bigcup_{1 \leq i \leq n} X_i$.

Proof: assume for some $x \in \prod_{1≤i≤n}X_i$, range of $x$ (denote it $R$) is not subset of $\bigcup_{1 \leq i \leq n} X_i$. Then, $\exists y \in R, y \notin \bigcup_{1 \leq i \leq n} X_i$. By surjectivity of $x$, it holds $\exists i' \in \{i \in N : 1 \leq i \leq n\}, x(i) = y$. However, $y = x(i) \in X_i$ by definition of $\prod_{1≤i≤n}X_i$, contradiction.

Hence, we construct the following set:

$$\{x: x \text{ is a partial function from } i' \in \{i \in N : 1 \leq i \leq n\} \text{ to } \bigcup_{1 \leq i \leq n} X_i\}$$

The above set exists by Exercise 3.4.7. Then, we apply axiom of specification, with the property $P(x)$ being:

- $x(i) ∈ X_i \text{ for all } 1≤i≤n \text{ and } x(i) \text{ is surjective} \\ \text{and } x \text{ has domain } \{i \in N : 1 \leq i \leq n\}$.

As desired.

### Exercise 3.5.3

Note ordered pair is a 2-tuple.

Definition: Two ordered $n$-tuples $(x_i)_{1≤i≤n}$ and $(y_i)_{1≤i≤n}$ are said to be equal iff $x_i = y_i$ for all $1 ≤ i ≤ n$.

Reflexivity ($A = A$)

Given $n$-tuple $A = (x_i)_{1≤i≤n}$,it holds that $x_i = x_i$ for all $1 ≤ i ≤ n$ (via Reflexivity of $x_i$), as desired.

Symmetry ($A = B \Leftrightarrow B = A$)

Say $A = (x_i)_{1≤i≤n}, B = (y_i)_{1≤i≤n}$, $A = B$ implies $x_i = y_i$ for all $1 ≤ i ≤ n$, hence $y_i = x_i$ for all $1 ≤ i ≤ n$, implying $B = A$ as desired.

Similarly, we deduce $B = A \rightarrow A = B$, as desired.

Transitivity $(A = B) \land (B = C) \rightarrow A = C$

Say $A = (x_i)_{1≤i≤n}, B = (y_i)_{1≤i≤n}, C = (z_i)_{1≤i≤n}$. Then, $A = B$ implies $x_i = y_i$ for all $1 ≤ i ≤ n$, $B = C$ implies $y_i = z_i$ for all $1 ≤ i ≤ n$, hence $x_i = z_i$ for all $1 ≤ i ≤ n$ as desired.

### Exercise 3.5.4

Part 1: $A×(B∪C) = (A×B)∪(A×C)$

Assume $x \in A×(B∪C)$, then $x_1 \in A, x_2 \in B \cup C$. 

WLOG $x_2 \in B$, then $(x_1, x_2) \in (A \times B)$, hence $(x_1, x_2) \in (A \times B) \cup  (A \times C) $, as desired.

Assume $x \in (A×B)∪(A×C)$, then either:

- $x_1 \in A \land x_2 \in B$
- $x_1 \in A \land x_2 \in C$

WLOG assume $x_1 \in A \land x_2 \in B$, then $x_1 \in A$, $x_2 \in B$ implying $x_2 \in B \cup C$ as desired.

Part 2: $A×(B∩C) = (A×B)∩(A×C)$

Assume $x \in A×(B∩C)$, then $x_1 \in A, x_2 \in B \cap C$.

Hence, $x_2 \in B \cap C$ implies $x_2 \in B$, therefore $x_1 \in A, x_2 \in B$ implies $x \in (A×B)$.

Similarly we show $x \in (A×C)$, hence $x \in (A×B)∩(A×C)$, as desired.

Assume $x \in (A×B)∩(A×C)$, then:

- $x_1 \in A$
- $x_2 \in B$
- $x_2 \in C$

Hence, $x_2 \in B \cap C$. Therefore $x \in A×(B∩C)$ as desired.

Part 3: $A×(B\backslash C) = (A×B) \backslash (A×C)$

Assume $x \in A×(B\backslash C)$, then $x_1 \in A, x_2 \in B, x_2 \notin C$.

From $x_1 \in A, x_2 \in B$, $x \in (A×B)$.

From $x_2 \notin C$, $x \notin (A \times C)$.

Hence, $x \in (A×B) \backslash (A×C)$ as desired.

Assume $x \in (A×B) \backslash (A×C)$, then:

- $x_1 \in A \land x_2 \in B$
- $\neg (x_1 \in A \land x_2 \in C)$
  - Which, by de Morgan $(x_1 \notin A \lor x_2 \notin C)$

Hence, we have $x_1 \in A, x_2 \in B, x_2 \notin C$ as desired.

### Exercise 3.5.5

Need to show:
$$(A × B) ∩ (C × D) = (A ∩ C)×(B∩D)$$

Assume $x \in (A × B) ∩ (C × D)$, then $x \in (A × B)$ and $x \in (C × D)$. Hence, it holds that:

- $x_1 \in A$
- $x_1 \in C$
- $x_2 \in B$
- $x_2 \in D$

Therefore $x_1 \in A \land x_1 \in C$, hence $x_1 \in A \cap C$. Similarly $x_2 \in B \cap D$, as desired.

Assume $x \in (A ∩ C)×(B∩D)$, then:

- $x_1 \in A \land x_1 \in C$
- $x_2 \in B \land x_2 \in D$

Hence:

- $x_1 \in A \land x_2 \in B$
- $x_1 \in C \land x_2 \in D$

Therefore $x \in (A × B)$ and $x \in (C × D)$, hence $x \in (A × B) ∩ (C × D)$, as desired.

Is it true that $(A×B)∪(C×D)=(A∪C)×(B∪D)$?

False, consider $A, B, C, D = \{a\}, \{b\}, \{c\}, \{d\}$.

Is it true that $(A × B)\backslash(C × D) = (A\backslash C) × (B\backslash D)$?

False, consider $A, B, C, D = \{a\}, \{b\}, \{a\}, \{d\}$.

### Exercise 3.5.6

Recall definition:

$$\prod_{1≤i≤n}X_i = \{(x_i)_{1≤i≤n} :x_i ∈ X_i \text{ for all } 1≤i≤n\}.$$

If direction:

For $(x_i)_{1≤i≤2} \in A \times B$, it must hold that $x_1 \in A \land x_2 \in B$ (by definition of Cartesian product).

Hence, since $A \subseteq C, B \subseteq D$, it holds that $x_1 \in C \land x_2 \in D$, hence $(x_i)_{1≤i≤2} \in C \times D$ as desired.

Only if direction:

Assume $A \nsubseteq C$, then $\exists x_1 \in A, x_1 \notin C$. Since $B$ is nonempty, we can pick an arbitrary $x_2 \in B$, s.t. $(x_1, x_2) \in A \times B$. Since $A \times B \subseteq C \times D$, $(x_1, x_2) \in C \times D$, hence $x_1 \subseteq C$ (by definition of Cartesian product), contradiction.

Similarly we show $B \subseteq D$ is necessary.

Removal of non-empty constraint:

Only if direction no longer holds. If direction still holds.

### Exercise 3.5.7

Part 1: Showing $h$ exists

Define $h: Z \rightarrow X \times Y$ as:

$$h(z) = (f(z), g(z))$$

Aka, the property $P(z, (x,y))$ for $h$ being $(x,y) = (f(z), g(z))$

We proceed to show that $h$ is a function. Note $f(z) \in X, g(z) \in Y$, hence $(f(z), g(z)) \in X \times Y$.

Then, assume there exists $x', y'$ s.t. $P(z, (x,y)), P(z, (x',y'))$ are true, then it must hold that $(x,y) = (x', y') = (f(z), g(z))$, as desired. Hence $h$ is a function.

Then, note:

$$
\begin{align*}
π_{X×Y→X} \circ h(z) &= π_{X×Y→X}((f(z), g(z))) &\text{by definition of } h\\
&= f(z) &\text{by definition of } \pi
\end{align*}
$$

As desired.

Similarly we show $π_{X×Y→Y} \circ h(z) = g(z)$

Part 2: Showing $h$ is unique

Assume there exists $h' \neq h$ that also satisfies the property. Therefore, $\exists z \in Z, h(z) \neq h'(z)$. Call that $z$ $z'$. Denote $h(z') = (f(z), g(z)), h'(z') = (a, b)$.

WLOG assume $f(z') \neq a$, then:

$$
\begin{align*}
π_{X×Y→X} \circ h'(z') &= π_{X×Y→X}((a, b))\\
&= a \\
&\neq f(z')
\end{align*}
$$

Contradiction, as desired. Similarly $g(z') \neq b$ also yields contradiction, hence it must be the case that $h(z') = h'(z')$, implying $h = h'$.

### Exercise 3.5.8

Recall definition:

$$\prod_{1≤i≤n}X_i = \{(x_i)_{1≤i≤n} :x_i ∈ X_i \text{ for all } 1≤i≤n\}.$$

If direction:

Note $\exist i \in 1≤i≤n, X_i = \empty$. Denote the $i$ as $i'$. Then, assume $\prod_{1≤i≤n}X_i$ is non-empty, we have $x \in \prod_{1≤i≤n}X_i$ (by single choice), such that $x_i ∈ X_i \text{ for all } 1≤i≤n$.

However, $x_i ∈ X_i \text{ for all } 1≤i≤n$ is always false. (As otherwise we have $x_{i'} \in X_{i'}$, yet $X_{i'}$ is empty, contradiction). Contradiction as desired.

Only if:

Lemma 3.5.12

### Exercise 3.5.9

Show that:

$$(\bigcup_{\alpha \in I} A_\alpha) \cap (\bigcup_{\beta \in J} B_\beta) = \bigcup_{(\alpha, \beta) \in I \times J} (A_\alpha \cap B_\beta)$$

Proof

Assume $x \in (\bigcup_{\alpha \in I} A_\alpha) \cap (\bigcup_{\beta \in J} B_\beta)$, then it holds that:

- $x \in \bigcup_{\alpha \in I} A_\alpha$
- $x \in \bigcup_{\beta \in J} B_\beta$

Hence, it must hold that:

- $\exists a \in I, x \in A_\alpha$
- $\exists b \in J, x \in B_\beta$

Hence, by definition of ordered pair:

$$\exists (a, b) \in I \times J, x \in A_\alpha \land x \in B_\beta$$
$$\exists (a, b) \in I \times J, x \in A_\alpha \cap B_\beta$$
$$x \in \bigcup_{(\alpha, \beta) \in I \times J} (A_\alpha \cap B_\beta)$$

As desired.

Assume $x \in \bigcup_{(\alpha, \beta) \in I \times J} (A_\alpha \cap B_\beta)$, then:

$$\exists (a, b) \in I \times J, x \in A_\alpha \cap B_\beta$$
$$\exists (a, b) \in I \times J, x \in A_\alpha \land x \in B_\beta$$

By definition of ordered pair:

- $\exists a \in I, x \in x \in A_\alpha \land x \in B_\beta$
- $\exists b \in J, x \in x \in A_\alpha \land x \in B_\beta$

Hence:

- $\exists a \in I, x \in A_\alpha$
- $\exists b \in J, x \in B_\beta$

Hence:

- $x \in \bigcup_{\alpha \in I} A_\alpha$
- $x \in \bigcup_{\beta \in J} B_\beta$

Therefore:

$$x \in (\bigcup_{\alpha \in I} A_\alpha) \cap (\bigcup_{\beta \in J} B_\beta)$$

As desired.

### Exercise 3.5.10

Part 1: show that two functions $f, g: X \rightarrow Y$ are equal if and only if they have the same graph.

If direction:

Assume $f = g$, then the graph of $f$ is:

$$\{(x, f(x)): x \in X\}$$

The graph of $g$ is:

$$\{(x, g(x)): x \in X\}$$

WLOG given $(x', y') \in \{(x, f(x)): x \in X\}$, it holds that $(x', y') \in \{(x, g(x)): x \in X\}$. As, by Axiom of Replacement, $(x, y) \in \{(x, f(x)): x \in X\}$ iff $\exists x'' \in X, (x', y') = (x'', g(x''))$. We simply let $x'' = x'$, as desired (we can easily verify that $x'' = x'$ works, steps omitted).

Only if direction:

Assume:

$$\{(x, f(x)): x \in X\} = \{(x, g(x)): x \in X\}$$

Then, assume $f \neq g$, then there exists $x' \in X, f(x') \neq g(x')$. Then, $(x', f(x')) \in \{(x, f(x)): x \in X\}$, yet $(x', f(x')) \notin \{(x, g(x)): x \in X\}$, contradiction.

As, if $(x', f(x')) \in \{(x, g(x)): x \in X\}$, it must hold that, by Axiom of replacement, $\exists x'' \in X, (x', f(x')) = (x'', g(x''))$. Hence, $x' = x''$ and $f(x') = g(x'') = g(x')$, contradiction.

Part 2

Show $f$ exists

Denote the property $P(x,y)$ as $(x,y) \in G$, then we claim that:

- $f: X \rightarrow Y$ with property $P(x,y)$ is a function
- $f$ has graph $G$

Note $(x,y) \in G$ is permissible if for all $x \in X$, there exists exactly one $y$ such that $(x,y) \in G$ is true. As, there is at least one $y$ by taking an element from $\{y \in Y: (x,y) \in G\}$ (as the set is non-empty). Assume there more than one $y$ (call them $y, y'$) s.t. the property is true, then $\{y \in Y: (x,y) \in G\}$ has two elements $y, y'$, contradiction.

Say $f$ has graph $G' = \{(x, f(x)): x \in X\}$, then we show $G = G'$.

Assume $(x',y') \in G$, then it holds that $y' = f(x')$ (As $P(x', y')$ is true). Let $x = x'$, then by Axiom of Replacement $(x', f(x')) \in G'$. Hence, since $(x',y') = (x', f(x'))$, $(x', y') \in G'$ as desired.

Assume $(x', y') \in G'$, then it holds that $y' = f'(x)$, by definition of graph. Consequently $P(x',y')$ is true, hence $(x',y') \in G$, as desired.

Show $f$ is unique

Assume there exists $f' \neq f$ s.t. $f'$ also has graph $G$.

Then $\exists x' \in X, f(x') \neq f'(x')$. Then, by definition of graph, it must hold that $(x', f'(x')) \in G$ and $(x', f(x')) \in G$. Hence, $f(x') \in \{y \in Y: (x,y) \in G\}$, and $f'(x') \in \{y \in Y: (x,y) \in G\}$, yet $f'(x') \neq f(x')$, implying that $\{y \in Y: (x,y) \in G\}$ has two elements, contradiction.

### Exercise 3.5.11

Consider $X \times Y$, then, by Lemma 3.4.9, there exists a set $P$ that contains all subsets of $X \times Y$. Then, we apply Axiom of Specification to $P$:

$$P':\{G \in X \times Y: \forall x 
\in X, \{y \in Y, (x,y) \in G\} \text{ has exactly one element}\}$$

Via Exercise 3.5.10, there exists exactly one function $f: X \rightarrow Y$ for each $G \in P'$ such that $G$ is graph of $f$. Hence, we apply Axiom of Replacement to $P'$, to form:

$$F: \{f: X \rightarrow Y \text{ has graph }G: G \in P'\}$$

We claim that $F$ is the desired set, aka the set of all functions $f: X \rightarrow Y$.

Proof:

Denote the set of all functions $f: X \rightarrow Y$ as $F'$.

Take $f \in F$, $f: X \rightarrow Y$, hence $f \in F'$ as desired.

Take $f \in F'$, then $f$ has a graph $G$. Hence we need to show $G \in P'$, aka, we need to show:

- $G \in X \times Y$
- $\forall x 
\in X, \{y \in Y, (x,y) \in G\} \text{ has exactly one element}$

Take $(x,y) \in G$, then, by definition of graph, $x \in X$ and $y = f(x) \in Y$, hence $(x,y) \in X \times Y$ as desired.

Assume $\forall x \in X, \{y \in Y, (x,y) \in G\} \text{ has exactly one element}$ is false, then for some $x'$, $\{y \in Y, (x',y) \in G\}$ is either empty or has more than one elements. Note $f(x') \in \{y \in Y, (x',y) \in G\}$, hence $\{y \in Y, (x',y) \in G\}$ is non-empty. Similarly if $y, y' \in \{y \in Y, (x',y) \in G\}, y \neq y'$, then by definition of graph $y = f(x'), y' = f(x')$, yet $y \neq y'$, contradiction.

Hence $f \in F \rightarrow f \in F'$ and $f \in F' \rightarrow f \in F$, indicating that $F = F'$ by definition of set equality, as desired.

### Exercise 3.5.12

We use induction to show existence of $a_N:\{n \in \N, n \leq N\} \rightarrow N$ s.t. $a_N(0) = c$ and $\forall n < N, a_N(n++) = f(n, a_N(n))$, then we use $a_N$ to construct $a$.

Let $P(N)$ be $a_N$ exists. Then, for the base case, easy to construct (by definition of function) $a_0: \{0\} \rightarrow \N$ s.t. $a_0(0) = c$, as desired.

Assume true for $P(N)$, then, for $P(N++)$, we construct the function $a_{N++}$ s.t.:

- For $n < N++$, $a_{N++}(n) = a_{N}(n)$
- For $n = N++$, $a_{N++}(N++) = f(N, a_{N}(N))$

First, we can verify that the above is a function (that passes vertical line test). Assume there exists $a_{N++}(n)$ s.t. it is assigned with two values $y, y'$. Then, $n < N++$ is false as $a_{N++}(n) = a_{N}(n)$, and $a_{N}(n)$ is assigned with one value by inductive hypothesis. Hence, it must hold that $n = N++$ (by trichotomy of order), however, $a_{N++}(N++) = f(N, a_{N}(N))$, for which RHS has only one value, as desired.

Also, easy to verify that the above function has the desired domain & range $\{n \in \N, n \leq N++\} \rightarrow N$.

We remains to show that the function satisfies the desired properties, aka:

- $a_{N++}(0) = c$
- $\forall n < N++, a_{N++}(n++) = f(n, a_{N++}(n))$

For $a_{N++}(0) = c$, note, it must hold that $0 < N++$. As, otherwise by trichotomy of order, we have $0 = N++$ or $0 > N++$. $0 = N++$ contradicts Axiom 2.3. $0 > N++$ implies that $0 = d + (N++)$ for some natural number $d$. By Corollary 2.2.9 it implies $0 = N++$, contradiction.

Hence, $a_{N++}(0) = a_{N}(0) = c$ by inductive hypothesis, as desired.

For $\forall n < N++, a_{N++}(n++) = f(n, a_N(n))$, we prove by cases. 

For $n < N$, it must hold that $n + d = N$ for some positive $d$, hence $(n + d)++ = N++$ By Axiom of substitution and therefore $(n++) + d = N++$ by addition laws, hence $n++ < N++$. Therefore $a_{N++}(n++) = a_{N}(n++) = f(n, a_{N}(n))$. Note $n < N++$, hence $f(n, a_{N}(n)) = f(n, a_{N++}(n))$, as desired.

For $n = N$, $a_{N++}(n++) = a_{N++}(N++) = f(N, a_{N}(N))$ by construction, as desired.

For $n > N$, $n \geq N++$ by 2.2.12 e. Hence, either $n = N++$ or $n > N++$, both violates trichotomy of order as $n < N++$. Therefore the case is vacuous, as desired.

For existence of $a$, we define $a(n) = a_N(n)$. Then, $a(0) = a_0(0) = c, a(n++) = a_{N++}(n) = f(n, a_{N}(n)) = f(n, a(n))$ as desired.

For uniqueness of $a$, assume there exists $b$ that satisfies the conditions. We proceed to show that $\forall n \in N, a(n) = b(n)$, aka $a = b$.

We let $P(n)$ be $a(n) = b(n)$. Then, $a(0) = b(0) = c$ by definition, hence the base case is satisfied.

For $P(n++)$, note $a(n++) = f(n, a(n)), b(n++) = f(n, b(n))$. Hence since $a(n) = b(n)$ by inductive hypothesis, $f(n, a(n)) = f(n, b(n))$, hence $a(n++) = b(n++)$ as desired.

Therefore $a$ is unique.

Problem with the above proof: Circularity. Order is defined using addition, which is then defined using recursive definition.

Bonus: TODO

### Exercise 3.5.13

We first show that $f$ exists, using Exercise 3.5.12, then we show that $f$ has the desired property:

- $f$ needs to be bijective
- $f(n) = n' \Leftrightarrow f(n++) = n'++$ 

Existence: we define $f: \N \rightarrow \N'$ as:

- $f(0) = 0'$
- $f(n++) = f(n)++$

Above uniquely defines a function by Exercise 3.5.12, as desired.

For $f(n) = n' \Leftrightarrow f(n++) = n'++$, note $f(n) = n'$ implies $f(n++) = f(n)++ = n'++$, as desired. And, $f(n++) = n'++$ implies $f(n)++ = n'++$, which, by Axiom 2.4, implies that $f(n) = n'$, as desired. Using this, we can also inductively show that $f(n) = n'$.

We proceed to prove that $f$ is bijective. For surjectivity, let the inductive hypothesis $P(n')$ be $\exists x \in N, f(x) = n'$. Then, for $P(0')$, we let $x = 0$ as desired. For $P(n++)$, note by inductive hypothesis we have $f(c) = n'$. Hence $f(c++) = n'++$, as desired.

For injectivity, assume $f(n) = f(m)$. Then, we have $f(n) = n', f(m) = m'$, hence $f(n) = f(m) \rightarrow n' = m'$, as desired.

### Exercise 3.6.1

Reflexivity:

Consider the mapping $f: X \rightarrow X$ s.t. $f(x) = x$. Easy to confirm that it is a bijection.

Symmetry:

If $X$ has same cardinality with $Y$, then there exists a bijective function $f: X \rightarrow Y$. Hence, by Exercise 3.3.6, there exists bijective $f^{-1}: Y \rightarrow X$, hence $Y$ has same cardinality with $X$ as desired.

Transitivity:

If $X$ has same cardinality with $Y$, there exists bijective $f: X \rightarrow Y$. If $Y$ has same cardinality with $Z$, then there exists bijective $g: Y \rightarrow Z$. By Exercise 3.3.7, $f \circ g: X \rightarrow Z$ exists & is bijective, as desired.

### Exercise 3.6.2

Note $\{i \in \N; 1 \leq i \leq 0\}$ is empty, as $i \leq 0$ implies $i + d = 0$, which then by Corollary 2.2.9 implies that $i = 0$, yet $1 + a = i$ for some $a$, leading to $1 = 0$, yet $1 = 0++$, hence $0++ = 0$, contradicting Axiom 2.3.

Only If direction:

Assume $X$ is non-empty, yet $X$ has cardinality $0$, then we have bijection $f: \empty \rightarrow X$. However, $f$ is not surjective, as given $x \in X$, there exists no $e \in \empty$ s.t. $f(e) = x$. Hence $f$ is not bijective, contradiction.

If direction:

If $X$ is empty, then, obvious bijection $f: \empty \rightarrow \empty$ exists, as desired.

### Exercise 3.6.3

We induct on $n$. Vacuously true for $n = 0$. For $P(n++)$, consider $f: \{i \in \N, 1 \leq i \leq n++\} \rightarrow \N$, consider $g: \{i \in \N, 1 \leq i \leq n\} \rightarrow \N$ s.t. $\forall 1 \leq i \leq n, g(i) = f(i)$, then by inductive hypothesis $\exists M' \in \N, \forall 1 \leq i \leq n, g(i) = f(i) \leq M'$.

Therefore, we let $M = \max(M', f(n++))$, then:

$$\forall 1 \leq i \leq n, f(i) \leq M' \leq  \max(M', f(n++))$$

$$f(n++) \leq \max(M', f(n++))$$

Combined:

$$\forall 1 \leq i \leq n++, f(i) \leq  \max(M', f(n++))$$

As desired.

### Exercise 3.6.4

(a) Let $\#(X) = n$. Then, there exists a bijective function $f: X \rightarrow \{i \in \N, 1 \leq i \leq n\}$

We define $g: X \cup \{x\} \rightarrow \{i \in \N, 1 \leq i \leq n + 1\}$ as:

- If $e \in X$, $g(e) = f(e)$
- Else $g(e) = n + 1$

$g$ is surjective, as, for $y \in \{i \in \N, 1 \leq i \leq n + 1\}$, it must either hold that $y \leq n$ or $y = n + 1$, by rules of order. If $y \leq n$, then $\exists e \in X, f(e) = y$, by surjectivity of $f$. Hence, $\exists e \in X, f(e) = g(e)= y$, therefore $\exists e \in X \cup \{x\}, g(e)= y$, as desired.

If $y = n + 1$, then $g(x) = n + 1$ (as $x \notin X$), as desired.

$g$ is injective. as, say $g(a) = g(b)$, then either $a, b \in X$ or some of $a,b \notin X$.

If $a, b \in X$, then $g(a) = g(b)$ implies $f(a) = f(n)$, hence $a = b$ by injectivity of $f$.

Else, WLOG assume $a \in X$ and $b \notin X$, then $g(b) = n + 1, g(a) = f(a)$. However $f(a) \in \{i \in \N, 1 \leq i \leq n\}$, $g(b) \notin \{i \in \N, 1 \leq i \leq n\}$. Hence, $f(a) \neq g(b)$, contradiction.

Therefore, it must hold that both $a, b \notin X$. However, $a, b \in X \cup \{x\}$, hence $a = b = x$, as desired.

(b)

Note $Y - X \subseteq Y$, hence by (c):

$$
\begin{align*}
\#(Y - X) &\leq \#(Y) \\
\#(X) + \#(Y - X) &\leq \#(X) + \#(Y) \\
\end{align*}
$$

We remain to show that $\#(X \cup Y) = \#(X) + \#(Y - X)$. Note there exists bijection $f: X \rightarrow \{i \in \N: 1 \leq i \leq \#(X)\}, g: Y - X \rightarrow \{i \in \N: 1 \leq i \leq \#(Y - X)\}$.

And, we construct $h: X \cup Y \rightarrow \{i \in \N: 1 \leq i \leq \#(X) + \#(Y - X)\}$, for which:

- For $e \in X, h(e) = f(e)$
- Else, $h(e) = g(e) + \#(X)$

We proceed to show that $h$ is bijective.

For injectivity, consider $h(e) = h(e')$, then if $e \in X, e' \notin X$, then $h(e) \leq \#(X)$, $h(e') = h(e) > \#(X)$, violating trichotomy of order. If $e \in X, e' \in X$, then $h(e) = h(e')$ implies $f(e) = f(e')$, which implies $e = e'$ by injectivity of $f$.

Similarly, if $e, e' \notin X$, $h(e) = h(e')$ implies $g(e) + \#(X) = g(e') + \#(X)$, which implies $g(e) = g(e')$, which implies $e = e'$ by injectivity of $g$, as desired.

For surjectivity, consider $i' \in \{i \in \N: 1 \leq i \leq \#(X) + \#(Y - X)\}$, we either have $i' \leq \#(X)$ or $i' > \#(X)$. 

For the first case, note $\exists e \in X, f(e) = i'$, since $f(e) = g(e)$, the same $e$ yields $g(e) = i'$ as desired.

For the second case, note $\exists e \notin X, g(e) = i' - \#(X)$. (As $\#(X) + \#(Y - X) \geq i'$ implies $\#(Y - X) \geq i' - \#(X)$ which implies $i' - \#(X) \in \{i \in \N: 1 \leq i \leq \#(Y - X)\}$), hence $\exists e \notin X, g(e) + \#(X)= i'$, which implies $\exists e \notin X, h(e) = i'$ as desired.

Note: Above used subtraction, which will be defined later. And introduction here should not cause circular reasoning.

If $X, Y$ disjoint, then $Y - X  = Y$, hence $\#(X \cup Y) = \#(X) + \#(Y - X) = \#(X) + \#(Y)$ as desired.

(c)

Note, if $Y = X$, then we have $\#(Y) = \#(X)$, hence $\#(Y) \leq \#(X)$ as desired.

For case $Y \neq X$, $Y \subset X$. We induct on $\#(X)$. When $\#(X) = 0$, by Exercise 3.6.2, $X = \empty$. For $Y \subset X$, either $Y = \empty$ or $Y \neq \empty$. $Y = \empty$ implies $X = Y$, hence not under the case $Y \neq X$. $Y \neq \empty$ implies $y \in Y$ (by single choice), yet $Y \subset X$ implies $y \in X$, contradiction. Hence, $\#(X) = 0$ is vacuously true.

For $\#(X) = 1$, by Exercise 3.6.2, $X$ is non-empty, hence by single choice there exists $x \in X$. We claim $X = \{x\}$. Assume there exists $x' \in X, x' \neq x$, then we can define bijection $f: X \rightarrow \{1, 2\}, f(x) = 1, f(x') = 2$. Hence $\#(X) = 2$, contradiction.

Assume $Y$ is non-empty, then we claim $Y = X = \{x\}$. As, assume $Y$ contains $2$ elements $y, y'$, then $y \in Y, y' \in Y$ as $Y \subset X$, hence $y = y' = x$, as desired. Hence, this does not fall under the case $Y \neq X$.

Assume $Y$ is empty, then $Y \subset X$, as desired.

For $P(n++)$, we take $x \in X, x \notin Y$ (which exists as $X \neq Y$. By Lemma 3.6.9 $\#(X - \{x\}) = n$. Hence, if $X - \{x\} \neq Y$, it must then hold that $X - \{x\} \subset Y$, therefore $\#(Y) < \#(X - \{x\})$, by inductive hypothesis. Hence $\#(Y) < \#(X - \{x\}) < n++ = \#(X)$ as desired.

If $X - \{x\} = Y$, then $\#(Y) = \#(X - \{x\}) = n < n++ = \#(X)$, closing the induction.

(d)

Let $\#(X) = n$, we induct on $\#(X)$.

For $n = 0$, by Exercise 3.6.2, $X = \empty$, hence $f(X) = \empty$. Therefore $\#(X) = \#(f(X)) = 0$, as desired.

For $P(n++)$, we take an element $x \in X$ and consider $X - \{x\}$. Note by Lemma 3.6.9, $\#(X - \{x\}) = n$, hence $\#(f(X - \{x\}))\leq \#(X - \{x\})$ by inductive hypothesis. 

Then, we perform case analysis. If there exist $x' \in X, x \neq x'$ s.t. $f(x) = f(x')$, then $f(X - \{x\}) = f(X)$. As, given $y \in f(X)$, it must hold that $y = f(c)$ for some $c \in X$. If $c \in X - \{x\}$, then $y \in f(X - \{x\})$. If $c \notin X - \{x\}$, since $c \in X$ it must hold that $c = x$. Hence $y = f(c) = f(x') \in f(X)$ as desired. Similarly for $y \in f(X - \{x\})$, we can show that $y \in f(X)$, as desired.

Therefore, $f(X - \{x\}) = f(X)$, hence $\#f(X - \{x\}) = \#f(X)$, consequently $\#f(X) \leq \#(X - \{x\})$, note $\#(X - \{x\}) = n$, hence $\#f(X) \leq n < n++$ as desired.

If there doesn't exist $x' \in X, x \neq x'$ s.t. $f(x) = f(x')$, then easy to verify $f(X - \{x\}) = f(X) - \{f(x)\}$. Since $f(x) \in f(X)$, $\#(f(X - \{x\})) = \#(f(X) - \{f(x)\}) = \#(f(X)) - 1$. Hence:

$$
\begin{align*}
\#(f(X - \{x\})) &\leq \#(X - \{x\}) \\
\#(f(X)) - 1 &\leq n \\
\#(f(X)) &\leq n++ \\
\end{align*}
$$

As desired.

For $f$ one-to-one, we can either modify the above induction proof or directly consider function $g: X \rightarrow f(X)$ s.t. $g(x) = f(x)$, and show $g$ is bijective.

(e)

Since $X, Y$ are finite sets, denote $\#(X) = n, \#(Y) = m$. 
WLOG assume $n = 0$, then $RHS = 0$, and $LHS = 0$ by Exercise 3.5.8, as desired.

Consider the case $n, m \neq 0$. There exists bijections:

$$
\begin{align*}
f&: \{X \rightarrow {i \in \N, 1 \leq i \leq n}\} \\
g&: \{Y \rightarrow {i \in \N, 1 \leq i \leq m}\}
\end{align*}
$$

Define $h: \{X \times Y \rightarrow \{i \in \N, 1 \leq i \leq nm\}\}$ as:

$h(x, y) = (g(y) - 1)n + f(x)$

Easy to verify that $h$ does have desired domain & range.

We claim that $h$ is bijective. For injectivity, assume we have $h(x,y) = h(x', y')$, then $(g(y) - 1)n + f(x) = (g(y') - 1)n + f(x')$, then $(g(y) - 1)n + f(x) = (g(y') - 1)n + f(x')$, then $g(y)n + f(x) = g(y')n + f(x')$.

We induct on $n$ to show that $g(y)n + f(x) = g(y')n + f(x')$ implies $f(x) = f(x'), g(y) = h(y')$. We prove a Lemma:

- Given $n, q \in \N, n, q \geq 1$, there exists unique $r \in \N, 1 \leq r \leq q, m \in \N$ s.t. $n = mq + r$.

Proof: 

For existence, note there exists $m, 0 \leq r - 1 < q$ by applying Proposition 2.3.9 to $n - 1 = mq + (r - 1)$.

For uniqueness, Induct on $n$.

For $n = 1$, $1 = mq + r$. Hence, it must hold that $r = 1$, then $mq = 0$. Since $q \geq 1$, then by Lemma 2.3.3, $m = 0$ must hold, as desired.

For $P(n++)$, we have $n++ = mq + r$. Assume we also have $n++ = mq + r'$, s.t. $r \neq r'$, then contradiction as $mq + r = mq + r' \rightarrow r = r'$. Similarly, cannot have $m \neq m' \land r = r'$. Therefore must have $m \neq m' \land r \neq r'$

Then, if $r, r' > 1$, we have $n = mq + (r - 1) = m'q + (r' - 1)$, contradicting $P(n)$.

If $r = 1 \land r' \geq 1$, then $n = mq, n = (m - 1)q + q$. (Note: we can take $m - 1$ as if $m = 0$, $n = mq = 0$, violating $n \geq 1$). Also $n = m'q + (r' - 1)$. Note since $r' \geq q$, it must hold that $r' - 1 < q$, hence $(r' - 1) \neq q$, contradicting $P(n)$. This closes the induction.

Hence, let $L = g(y)n + f(x) = g(y')n + f(x')$. It immediately follows that $g(y) = g(y'), f(x) = f(x')$ via the Lemma, as desired.

For surjectivity, given $L \in \{i \in \N: 1 \leq i \leq nm\}$, there exists $u, t$ s.t. $L = un + t$ by Lemma, hence $L = ((u + 1) - 1)n + t$. We take $a = g^{-1}(u + 1), b = f^{-1}(t)$. Since $1 \leq t \leq n$, $t$ is in domain of $f^{-1}$. Similarly, assume $u + 1 > m$, then $L \geq mn + t > mn$. Contradiction. Hence $u + 1$ is in domain of $g^{-1}$. Then:

$$
\begin{align*}
h(a, b) &= h(g^{-1}(u + 1), f^{-1}(t)) \\
        &= (g(g^{-1}(u + 1)) - 1)n + f(f^{-1}(t)) \\
        &= ((u + 1) - 1)n + t \\
        &= L
\end{align*}
$$

As desired.

Note: For injectivity, induction can be circumvented, by bounding $f(x) - f(x')$ and show that it lies between multiple of $n$. Surjectivity can also be shown by Euclidean Algorithm + bound estimation. This offers an alternative way of doing the problem.

(f)

Let $\#(X) = n$, We induct on $n$.

When $n = 0$, we have $\#(Y)^{\#(X)} = 1$ and $X = \empty$ (By 3.6.2), and there exists $1$ function $f: X \rightarrow \empty$, as desired.

For $P(n++)$, consider taking $x \in X$, and hence $Y^{X - \{x\}} = \#(Y)^n$ by inductive hypothesis.

We proceed to show that there exists a bijection between $Y^{X - \{x\}} \times Y^{\{x\}}$ and $Y^X$. Let $g: Y^{X - \{x\}} \times Y^{\{x\}} \rightarrow Y^X$ be:

- $g(h, i) = f$ s.t. $\forall x' \in X - \{x\}, f(x') = h(x')$, else $f(x) = i(x)$

We proceed to prove that $g$ is injective. For $g(h, i), g(h', i')$, it must hold that:

- $\forall x' \in X - \{x\}, f(x') = h(x')$
- $\forall x' \in X - \{x\}, f(x') = h'(x')$

Hence, $\forall x' \in X - \{x\}, h(x') = h'(x')$, therefore $h = h'$. Similarly, $i(x) = i'(x)$, as desired.

For surjectivity, given a function $f \in Y^X$, we define:

- $h: X - \{x\} \rightarrow Y$ s.t. $\forall x' \in X - \{x\}, h(x') = f(x')$
- $i: \{x\} \rightarrow Y$ s.t. $i(x) = f(x)$.

Hence, $h \in Y^{X - \{x\}}, i \in Y^{\{x\}}$. Easy to verify $g(h, i) = f$, as desired.

Then, we show that $\#(Y^{\{x\}}) = \#(Y)$. We similarly establish construct $h: Y^{\{x\}} \rightarrow Y$ s.t. $h(f) = f(x)$. Then, $h$ is injective, as, given $f(x) = f'(x)$, it must hold that $f = f'$ by definition of equality. $h$ is surjective, as, given $y \in Y$, we can construct $f(x) = y$ as desired.

Hence:

$$
\begin{align*}
\#(Y^X) &= \#(Y^{X - \{x\}}) \times \#(Y^{\{x\}}) \quad \text{By e)} \\
        &= \#(Y)^n \times \#(Y) \quad \text{By inductive hypothesis} \\
        &= \#(Y)^{n + 1}
\end{align*}
$$

As desired.

### Exercise 3.6.5

We consider $f: A \times B \rightarrow B \times A$ s.t. $f(a, b) = (b, a)$.

$f$ is injective as, given $f(a, b) = f(c, d)$, then $(b, a) = (d, c)$, hence $b = d$ and $a = c$, therefore $(a, b) = (c, d)$ as desired.

$f$ is surjective, as, given $(a, b) \in B \times A$, we have $f(b, a) = (a, b)$ as desired.

Alternate proof of Lemma 2.3.2:

For $m, n \in \N$, there exists two sets $M, N$ with cardinality $m, n$. By Proposition 3.6.14 e), $\#(M \times N) = m \times n, \#(N \times M) = n \times m$. Yet, by Exercise 3.6.5, $\#(M \times N) = \#(N \times M)$, hence $m \times n = n \times m$, as desired.

### Exercise 3.6.6

Note:

$$f \in (A^B)^C \Leftrightarrow f: C \rightarrow A^B$$

$$g \in A^{B \times C} \Leftrightarrow g: B \times C \rightarrow A$$

Consider $h: (A^B)^C \rightarrow A^{B \times C}$ s.t. $\forall (b,c) \in B \times C, h(f)(b, c) = f(c)(b)$. We claim that $h$ is a bijection.

$h$ is injective as say we have $h(f) = h(f')$, then $\forall (b,c) \in B \times C, f(c)(b) = f'(c)(b)$. Denote $f(c) = g, f'(c) = g'$, then $\forall (b,c) \in B \times C, g(b) = g'(b)$. Hence $\forall b \in B, g(b) = g'(b)$, hence $g = g'$. Therefore $\forall c \in C, f(c) = f'(c)$, hence $f = f'$ as desired.

$h$ is surjective as, given $g: B \times C \rightarrow A$, we define $f: C \rightarrow A^B$ as $f(c) = g(b, c)$. With $c$ fixed, $g(b, c) \in A^B$ as desired.

Given $a, b, c \in N$, construct $A, B, C$ with cardinality $a, b, c$. Then, $\#((A^B)^C) = (a^b)^c, \#(A^{B \times C}) = a^{b \times c}$ by Proposition 3.6.14. Hence, $(a^b)^c = a^{b \times c}$ as desired.

For $a^b \times a^c = a^{b + c}$, consider sets $A, B, C$ with cardinality $a, b, c$ and $B, C$ disjoint. Then, consider bijection $t: A^{B \cup C} \rightarrow A^B \times A^C$, for which $t(h) = (f, g)$, with $\forall b \in B, f(b) = h(b), \forall c \in C, g(c) = h(c)$. Rest similar to the above proof.

### Exercise 3.6.7

Only if

$f: A \rightarrow B$ is an injection. Denote $g: A \rightarrow f(A)$ s.t. $\forall a \in A, g(a) = f(a)$. Then, $g$ is a bijection. As, $g$ is injective, given $g(a) = g(a')$, then $f(a) = f(a')$, hence $a = a'$ by injectivity of $f$. $g$ is surjective, as, for all $b \in f(A)$, $\exists a \in a$ s.t. $f(a) = b$, by definition of image.

Hence, $\#(A) = \#(f(A))$. Note $f(A) \subseteq B$, hence by 3.6.14 c), $\#(A) = \#(f(A)) \leq \#(B)$.

If

Given $\#(A) \leq \#(B)$, then there exists:

- $f: A \rightarrow \{i \in \N: 1 \leq i \leq \#(A)\}$
- $g: \{i \in \N: 1 \leq i \leq \#(B)\} \rightarrow B$

We construct $g': \{i \in \N: 1 \leq i \leq \#(A)\} \rightarrow B$ s.t. $\forall i \in \{i \in \N: 1 \leq i \leq \#(A)\}, g'(i) = g(i)$.

Then, we claim that $h = g \circ f, h: A \rightarrow B$ is an injection. First, note domain & range of $g, f$ satisfies conditions in Definition 3.3.10, hence $h: A \rightarrow B$ is a function. Then, given $h(a) = h(a')$, we deduce $g(f(a)) = g(f(a'))$, which by injectivity of $g$ we deduce $f(a) = f(a')$, hence $a = a'$ by injectivity of $f$ as desired.

### Exercise 3.6.8

Consider $h: A \rightarrow f(A)$. Then, similar to Exercise 3.6.7 reasoning, $h$ is bijective. Hence, consider $h^{-1}: f(A) \rightarrow A$, then $h^{-1}$ is bijective, hence surjective. Finally consider $g: B \rightarrow A$ s.t.:

- If $b \in f(A)$, $g(b) = h^{-1}(b)$
- Else we choose $a \in A$, and let $g(b) = a$

Note: we can take $a \in A$, as if $A = \empty$, injectivity of $f$ implies $B = \empty$, for which $g: \empty \rightarrow \empty$ exist as trivial bijection.

Easy to verify $g$ has desired domain & range.

For surjectivity, take $a \in A$, then $g(h(a)) = h^{-1}(h(a)) = a$ as desired.

### Exercise 3.6.9

In Exercise 3.6.4 b), it is shown that $\#(X \cup Y) = \#(Y) + \#(X - Y)$.

We proceed to show that $\#(X \cap Y) = \#(X) - \#(X - Y)$. Note $\#(X \cap Y) + \#(X - Y) = \#((X \cap Y) \cup (X - Y)) = \#(X)$ (by Exercise 3.6.4 b, as $X - Y, X \cap Y$ disjoint), hence $\#(X \cap Y) = \#(X) - \#(X - Y)$.

Add $\#(X \cap Y) = \#(X) - \#(X - Y)$ and $\#(X \cup Y) = \#(Y) + \#(X - Y)$ yields the result.

### Exercise 3.6.10

Assume $\forall i \in \{1, ..., n\}, \#(A_i) \leq 1$.

Then, by 3.6.14 b):

$$\# \bigcup_{i \in \{1, ..., n\}} A_i = \sum_{i \in \{1, ..., n\}} \#(A_i) \leq \sum_{i \in \{1, ..., n\}} 1 = n$$

Contradiction. Hence $\exists i \in \{1, ..., n\}, \#(A_i) > 1$, which by rules of order, $\exists i \in \{1, ..., n\}, \#(A_i) \geq 2$, as desired.

### Exercise 4.1.1

Reflexivity:

Given $a\text{---}b$, obviously $a + b = a + b$, hence $a\text{---}b = a\text{---}b$.

Symmetry:

If $a\text{---}b = c\text{---}d$, then $a + d = c + b$, hence by Reflexivity of Natural Number equality, $c + b = a + d$, hence $a\text{---}b = c\text{---}d$ as desired.

### Exercise 4.1.2

If $a\text{---}b = a'\text{---}b'$, then $a + b' = a' + b$. Hence $b' + a = b + a'$, therefore $(b' \text{---} a') = (b \text{---} a)$, hence $-(a\text{---}b) = -(a'\text{---}b')$ as desired.

### Exercise 4.1.3

Let $a = x - y$
$$
\begin{align*}
(-1) \times (x \text{---} y) &= (0\text{---}1) \times (x \text{---} y) \\
                    &= (0 \times x + y)\text{---}(0 \times y + x) \\
                    &= y \text{---} x \\
                    &= -a
\end{align*}
$$

As desired.

### Exercise 4.1.4

For $x + y = y + x$, let $x = a \text{---} b, y = x = c \text{---} d$, then $x + y = (a + c) \text{---} (b + d), y + x = (c + a) \text{---} (d + b)$.

Note $(a + c) + (d + b) = (c + a) + (b + d)$, hence $x + y = y + x$ as desired.

For $(x + y) + z = x + (y + z)$, let $x = a \text{---} b, y = c \text{---} d, z = e \text{---} f$, then:

- $(x + y) + z = (a + c) + e \text{---} (b + d) + f$
- $x + (y + z) = a + (c + e) \text{---} b + (d + f)$

Hence, we remains to show $(a + c) + e + b + (d + f) = a + (c + e) + (b + d) + f$, which is true by natural number addition rules as desired.

For $x + 0 = 0 + x = x$, let $x = a \text{---} b$, then $x + 0 = (a \text{---} b) + (0 \text{---} 0) = (a + 0) \text{---} (b + 0) = (a \text{---} b) = x$ as desired. For $x + 0 = 0 + x$, it follows from $x + y = y + x$.

For $x + (−x) = (−x) + x = 0$, similarly $x + (−x) = (−x) + x$ follows from $x + y = y + x$. Remains to show $x + (-x) = 0$. Let $x = a \text{---} b$, then $x + (-x) = a \text{---} b + b \text{---} a = (a + b) \text{---} (b + a)$. We claim $(a + b) \text{---} (b + a) = 0 \text{---} 0$, as $a + b + 0 = 0 + b + a$, as desired.

For $xy = yx$, let $x = a \text{---} b, y = x = c \text{---} d$, then $xy = (ac + bd) \text{---} (ad + bc), yx = (ca + db) \text{---} (cb + da) = (ac + bd) \text{---} (ad + bc)$. Rest follows from reflexivity.

For $x1 = 1x = x$, note $x1 = 1x$ by $xy = yx$. Remains to show that $x1 = x$. Let $x = a \text{---} b$, then $x1 = (a \text{---} b) \times (1 \text{---} 0) = (a1 + b0) \text{---} (a0 + b1) = a \text{---} b = x$ as desired.

For $x(y + z) = xy + xz$, let $x = a \text{---} b, y = c \text{---} d, z = e \text{---} f$, then $x(y + z) = (a \text{---} b) \times ((c + e) \text{---} (d + f)) = a(c+e) + b(d + f) \text{---} (a(d + f) + b(c + e))$.

$xy + xz = (ac + bd) \text{---} (ad + bc) + (ae + bf) \text{---} (af + be) = ((ac + bd) + (ae + bf)) \text{---} (ad + bc) + (af + be)$. Note $(ac + bd) + (ae + bf) = a(c+e) + b(d + f)$ and $(ad + bc) + (af + be) = a(d + f) + b(c + e)$, rest follows from reflexivity.

For $(y + z)x = yx + zx$, note $(y + z)x = x(y + z)$ by $xy = yx$. Then, $x(y + z) = xy + xz$. Finally $xy + xz = yx + zx$ by $xy = yx$, as desired.

### Exercise 4.1.5

Let $x = (a \text{---} b), y = (c \text{---} d)$, then $xy = (ac + bd) \text{---} (ad + bc) = 0 \text{---} 0$. Hence $ac + bd + 0 = (ad + bc) + 0$ implying $ac + bd = ad + bc$. Then, we need to prove either $a = b$ or $c = d$.

Note:

$$
\begin{align*}
ac + bd &= ad + bc \\
ac + bd - bd - ad &= ad + bc - bd - ad \quad \text{by substitution Axiom}\\
ac - ad &= bc - bd \\
a(c - d) &= b(c - d) \\
a(c - d) - b(c - d) &= 0 \\
(a - b)(c - d) &= 0
\end{align*}
$$

WLOG assume $a > b, c > d$, then By Lemma 4.1.5, $(a - b), (c - d)$ equates to natural numbers. Hence, by Proposition 4.1.8 either $a = b$ or $c = d$ as desired.

If $a - b < 0$ or $c - d < 0$, then we can simply multiply both sides by $-1$ and the same argument holds.

### Exercise 4.1.6

If $ac = bc$, then $ac - bc = 0$, hence $c(a - b) = 0$. Therefore, by Proposition 4.1.8, either $c = 0$ or $a - b = 0$. Since $c \neq 0$, then $a - b = 0$ must hold, therefore $a = b$ as desired.

Alternate proof:

By Corollary 2.3.7, $c$ is either positive, or negation of positive number.

WLOG say $c$ is positive (if $c$ is negative, we multiply both sides by $-1$). Then, assume $a, b \in \N$, then the conclusion follows from Corollary 2.3.7. Assume $a, b \notin \N$, then we multiply both sides by $-1$ to yield $-a = -b$, which then we can deduce $a = b$ as desired. Assume $a \in \N, b \notin \N$, then we can show $ac \in \N$, $bc = -(-b)c \notin \N$, contradiction hence the case is vacuous, as desired.

### Exercise 4.1.7

a) 

Only if:

Assume $a > b$, then $a = b + c$ for some positive $c$. Hence:

$$
\begin{align*}
a &= b + c \\
a - b &= b + c - b \\
a - b &= c
\end{align*}
$$

As desired.

If:

Assume $a - b = c$ for some positive $c$, then:

$$
\begin{align*}
a - b &= c \\
a - b + b &= c + b \\
a &= b + c \\
a &> b
\end{align*}
$$
As desired.

b)

$a + c - (b + c) = a + c - b - c = a - b$. Since $a > b$, $a + c - (b + c)  = a - b$ is a positive number, hence $a + c > b + c$ as desired.

c)

$ac - bc = (a - b)c$. Since $a - b, c$ are positive, $(a - b)c$ is positive, hence $ac > bc$ as desired.

d)

$-b - (-a) = -b + a = a - b$. Since $a > b$, $-b - (-a) = a - b$ is positive, hence $-b > -a$ as desired.

e)

Note $a = b + e, b - f = c$ for some positive $e, f$, hence:

$a - c = (b + e) - (b - f) = e + f > 0$, hence $a > c$ as desired.

f)

Equivalent of showing exactly one of $a - b > 0$, $a - b$ positive, $a - b$ negative is true, which follows from Trichotomy of integers.

### Exercise 4.1.8

Let $P(n)$ denote $n \geq 0$. Then, $P(0)$ is true as $0 \geq 0$.

For $P(n++)$, note $n++ > n \geq 0$ (by $P(n)$), as desired.

However, $P(-1)$, aka $-1 \geq 0$ is false.

### Exercise 4.2.1

Reflexivity:

Let $x = a // b$, then $x = x \Leftrightarrow ab = ab$. Since $ab = ab$ always true $x = x$ as desired.

Symmetry:

Let $x = a // b, y = c // d$. Then $x = y$ implies $ad = bc$, which implies $bc = ad$ hence $y = x$ as desired.

Transitivity:

Let $x = a // b, y = c // d, z = e // f$. Assume $x = y$, $y = z$, then $ad = bc, cf = ed$. Hence $bcf = bed$, hence $adf = bed$. Since $d \neq 0$, $af = be$ by Corollary 4.1.9, hence $x = z$ as desired.

### Exercise 4.2.2

For addition, say we have $x = x', x = a // b, y = c // d, x
' = a' // b'$, then:

$$
\begin{align*}
x + y &= (ad + bc) // bd \\
x' + y &= (a'd + b'c) // b'd
\end{align*}
$$

Now, we remain to show that $(ad + bc)b'd = (a'd + b'c)bd$. Note $ab' = a'b$, then $(ad + bc)b'd = ab'dd + bb'cd = a'bdd + bb'cd = (a'd + b'c)bd$ as desired.

Similarly, say $x = a // b, y = c // d, y' = y, y' = c' // d'$, then:

$$
\begin{align*}
x + y &= (ad + bc) // bd \\
x + y' &= (ad' + bc') // bd'
\end{align*}
$$

Then, remain to show $(ad + bc)bd' = (ad' + bc')bd$. Note $cd' = c'd$, then $(ad + bc)bd' = adbd' + cd'bb = adbd' + c'dbb = (ad' + c'b)bd$ as desired.

For product:

$$
\begin{align*}
x * y &= ac // bd \\
x' * y &= a'c // b'd
\end{align*}
$$

Note $ab' = a'b$, then $ac b'd = a'cbd$ as desired.

Similarly:

$$
\begin{align*}
x * y &= ac // bd \\
x * y' = ac' // bd'
\end{align*}
$$

Note $cd' = c'd$, then $acbd' = ac'bd$ as desired.

For negation, say we have $x = a // b, x' = x, x' = a' // b'$, then $-x = (-a) // b, -x' = (-a') // b'$. Remains to show $-ab' = -a'b$. Note $ab' = a'b$, then $-ab' = -a'b$ as desired.

### Exercise 4.2.3

Let $x = a // b, y = c // d, z = e // f$.

For $x + y = y + x$, note $x + y = (ad + bc) // bd, y + x = (da + cb) // bd = (ad + bc) // bd$ as desired.

For $x + 0 = 0 + x = x$, note $x + 0 = 0 + x$ by $x + y = y + x$. Remains to show $x + 0 = 0$. Note $x + 0 = (a1 + b0) // b = a // b = x$  as desired.

For $x + (-x) = (-x) + x = 0$, note $x + (-x) = (-x) + x$ by $x + y = y + x$, hence remains to show $x + (-x) = 0$. Note $x + (-x) = (ab + b(-a)) // bb = 0 // bb$. We claim $0 // bb = 0 // 1$, as $0 \times 1 = 0 \times bb = 0$, as desired.

For $xy = yx$, note $xy = ac // bd$, $yx = ca // db = ac // bd$, rest follows by reflexivity.

For $(xy)z = x(yz)$, note $(xy)z = (ac)e // (bd)f$, $(xy)z = a(ce) // b(df) = (ac)e // (bd)f$ as desired.

For $x1 = 1x = x$, note $x1 = 1x$ follows from $xy = yx$. For $x1 = x$, note $x1 = a1 // b1 = a // b = x$ as desired.

For $x(y + z) = xy + xz$, note $x(y + z) = (a // b)(cf + de // df) = a(cf + de) // bdf$

$xy + xz = ac // bd + ae // bf = (acbf + aebd) // bdbf$

Then, need to show $a(cf + de)bdbf = (abcf + aebd)bdf$, which, since $b, d, f \neq 0$, is equivalent to $a(cf + de) = (acf + aed)$. which is true by distributive law of integer, as desired.

For $(y + z)x = yx + zx$, note $(y + z)x = x(y + z)$ by $xy = yx$, then $x(y + z) = xy + xz = yx + zx$ as desired.

For $x x^{-1} = x^{-1} x = 1$, note $x x^{-1} = x^{-1} x$ by $xy = yx$. Remains to show $x x ^{-1} = 1$. Note $x x^{-1} = ab // ba$. Since $ab1 = ba1$, $x x^{-1} = 1$ as desired.

### Exercise 4.2.4

Let $x = a / b$. Then, assume $b$ positive. (If $b$ is not positive, easy to prove $(-a) / (-b) = a / b$), with $(-b)$ positive.

Then, we either have $a < 0, a = 0, a > 0$ by Lemma 4.1.11 f).

If $a < 0$, then by definition $x$ is negative. If $a = 0$, then by definition $x = 0$. If $a > 0$, then by definition $x$ is positive. Hence at least one of (a) (b) (c) is true.

Then, we show (a), (b) cannot happen at the same time. Assume $a / b = 0 / 1$, then $a1 = b0$, hence $a = 0$, contradiction, Similarly (b) (c) cannot happen at the same time.

For (a), (c), assume $x = a / b = c / d$ for $a, b, d > 0, c < 0$, then $ad = bc$ holds. Note $ad$ is positive by Lemma 4.1.11 c), yet $bc$ is negative, contradiction as desired.

### Exercise 4.2.5

a)  Equivalent to exactly one of $x - y = 0$, $x - y$ positive, $x - y$ negative is true, which follows from Lemma 4.2.7.

b) One have $x < y$ if $x - y$ is negative. We claim $y - x$ is positive. Say $x = a/b, y = c/d$ for some $b, d \in \Z, b, d > 0$, then $x - y = (ad - bc) / bd, y - x = (bc - ad) / bd = -(ad - bc) / bd$, hence by definition of negation $x - y = -(y - x)$. Hence $y - x$ negative by Definition 4.2.6, therefore $y > x$.

The other direction can be proved similarly.

c) If $x < y$ and $y < z$, then $y - x$, $z - y$ are both positive. Hence, $(y - x) + (z - y) = z - x$ is positive, therefore $x < z$ as desired.

Note: easy to prove sum of two positive numbers are positive. Assume we have $x, y > 0, x = a/b, y = c/d, a,b,c,d > 0$, then $x + y = (ad + bc) / bd$. Note $bd$ is positive as $b > 0$, by 4.1.11 c) $bd > 0d = 0$, and $ad + bc$ is positive as say we have $m, n > 0$, then $m + n > 0 + n$ by 4.1.11 b), and since $0 + n = n > 0$, $m + n > 0$ by 4.1.11 e) as desired.

d) $x < y$ implies $y - x$ is positive. Hence $y + z - (x + z) = y - x$ is positive as desired.

e) $yz - xz = (y - x)z$. Since $y > x$, $y - x$ is positive, we call it $d$. We remains to prove that product of two positive rational is positive. Say $m = a / b, n = c / d$, for some $a,b,c,d > 0$, then $mn = ac / bd$. Hence, we remain to show $ac, bd$ are positive, given $a,b,c,d$ positive, It is already shown in c), as desired.

### Exercise 4.2.6

$xz - yz = (x - y)z = 1(x - y)z = (-1)(-1)(x - y)z = (y - x)(-z)$. Since $y - x, -z$ are positive, their product is positive via similar reasoning in Exercise 4.2.9 c).

### Exercise 4.3.1

(a) By trichotomy of rational number, we either have $x$ positive, $x$ negative or $x = 0$.

Assume $x$ positive, then by definition $|x| = x$, which is positive as desired. 

Assume $x$ negative, then by definition $|x| = -x$. Assume $x = a / b$ for some $a < 0, b > 0$, then $-x = (-a) / b$ with $-a, b$ positive hence $-x$ is positive.

Assume $x = 0$, then by definition $x = 0 \geq 0$ as desired,

(b) By trichotomy of rational number, we break into cases.

If $x = 0$, $|x + y| = |y| = 0 + |y| = |x| + |y| \leq |x| + |y|$ as desired. Similar reasoning for $y = 0$.

If $x, y$ are positive, then $|x + y| = x + y = |x| + |y| \leq |x| + |y|$ as desired.

If $x, y$ are negative, then $|x + y| = -(x + y) = (-x) + (-y) = |x| + |y| \leq |x| + |y|$ as desired.

If $x$ positive and $y$ negative, then we either have $x + y$ positive, $x + y$ negative, or $x + y = 0$, If $x + y$ is positive, then $|x + y| = x + y, |x| + |y| = x - y, |x| + |y| - |x + y| = x - y - (x + y) = -2y > 0$ as desired.

If $x + y = 0$, then $|x + y| = 0, |x| + |y| \geq 0 = |x + y|$ as desired.

If $x + y < 0$, then $|x + y| = -(x + y), |x| + |y| = x - y, |x| + |y| - |x + y| = x - y + (x + y) = 2x > 0$ as desired.

c)

If direction:

If $y \geq |x|$, assume $x \geq 0$, then $y \geq x \geq 0$. Note since $y \geq 0$, $-y \leq 0$ by Exercise 4.2.6, hence $y \geq x \geq 0 \geq -y$ as desired.

Assume $x < 0$, then $-x > 0$ by Exercise 4.2.6, hence $y \geq -x > 0$, therefore $-y \leq x < 0$ by Exercise 4.2.6. Note since $y > 0$, $-y \leq x < 0 < y$ as desired.

d)

Assume $x, y$ both positive, then $|xy| = xy = |x||y|$ as desired. Assume $x, y$ both negative, then $|xy| = (-x)(-y) = |x||y|$ as desired. Assume $x = 0$, then $|xy| = |0| = 0 = 0|y| = |x||y|$ as desired. Assume $x$ positive and $y$ negative then $|xy| = x(-y) = |x||y|$ as desired.

e)

$|x - y| \geq 0$ by a). Also, by a), $|x - y| = 0$ iff $x - y = 0$ iff $x = y$ as desired.

f)

$|x - y| = 1|x - y| = |-1||x - y| = |(-1)(x - y)| = |y - x|$ as desired.

g):

Need to show $|x - z| \leq |x - y| + |y - z|$. Let $x - y = a, y - z = b$, then $x - z = x - y + y - z = a + b$. Hence, since by b) $|a + b| \leq |a| + |b|$, $|x - z| \leq |x - y| + |y - z|$ by substitution as desired.

### Exercise 4.3.2

a)

If $x = y$, then $d(y, x) = 0$. Hence $\epsilon > 0 = d(y,x)$ as desired.

For the converse, WLOG assume $x < y$, then $y - x = d$ for some positive $d$. Then, $d(x, y) = d$. We choose $\epsilon = d / 2$, then we claim $d > d / 2$. Say $d = a / b$ for some $a, b > 0$, then $d / 2 = (a / b) \times (1 / 2) = a / 2b$. One can easily verify $d = 2a / 2b$, hence $d - d / 2 = (2a - a) / 2b = a / 2b$, which is positive, as desired.

Hence, $d > d/2$ implies $d(y, x) > d/2$, hence $x$ is not $\epsilon$-close to $y$ for $\epsilon = d / 2$, contradiction as desired.

b)

If $|x - y| \leq \epsilon$, then $|y - x| = |x - y| = \epsilon$ as desired.

c)

Given $|x - y| \leq \epsilon, |y - z| \leq \delta$, then $|x - y| + |y - z| \leq \epsilon + |y - z| \leq \epsilon + \delta$. Note by 4.3.3 f), $|x - z| \leq |x - y| + |y - z| \leq \epsilon + |y - z| \leq \epsilon + \delta$ as desired.

d)

Note:
$$
\begin{align*}
d(x + z, y + w) &= |x + z - (y + w)| \\ 
                &= |(x - y) + (z - w)| \\ 
                &\leq |x - y| + |z - w| \quad \text{by 4.3.3 (b)} \\
                &= \epsilon + \delta
\end{align*}
$$

As desired.

Similarly:

$$
\begin{align*}
d(x - z, y - w) &= |x - z - (y - w)| \\ 
                &= |(x - y) + (-1)(z - w)| \\ 
                &\leq |x - y| + |z - w| \quad \text{by 4.3.3 (b), (d)} \\
                &= \epsilon + \delta
\end{align*}
$$

As desired.

e)

$|x - y| \leq \epsilon < \epsilon'$ as desired.

f)

WLOG assume $y \leq w \leq z$. Then $y - x \leq w - x \leq z - x$. Hence we either have $w < x, w \geq x$. Assume $w < x$, then $x - w > 0$, note $x - y \geq x - w > 0$, hence $|x - y| \geq |x - w|$ implying $\epsilon \geq d(w, x)$ as desired.

Assume $w \geq x$, then $w - x \geq 0$, hence $0 \leq w - x \leq z - x$, therefore $|w - x| \leq |z - x|$ implying $d(w, x) \leq \epsilon$ as desired.

g)

Note $z$ non-zero required as Definition 4.3.4 mandates that $\epsilon > 0$.

$$
\begin{align*}
d(xz, yz) &= |xz - yz| \\
          &= |z(x - y)| \\
          &= |z||x - y| \quad \text{By 4.3.3 (d)} \\
          &\leq |z|\epsilon
\end{align*}
$$

As desired.

### Exercise 4.3.3

a)

Let $P(n)$ be $x^nx^m = x^{n + m}$.

Then, $P(0)$ denote $x^0x^m = x^m$, which is true as $x^0 = 1$ by definition 4.3.9.

For $P(n + 1)$, note $x^{n + 1}x^m = x^nxx^m = x^{n + m}x$ by $P(n)$, then $x^{n + m}x = x^{n + m + 1} = x^{(n + 1) + m}$ by definition 4.3.9 as desired.

Similarly, let $P(m)$ denote $(x^n)^m = x^{nm}$, then $P(0)$ denote $(x^n)^0 = x^{n0}$, which is true as both side evaluates to $1$.

For $P(m + 1)$, note $(x^n)^{m+1} = (x^n)^mx^n = x^{nm}x^n$ by $P(m)$, which, by $x^nx^m = x^{n + m}$ equals to $x^{nm + n} = x^{n(m + 1)}$ as desired.

Let $P(n)$ denote $(xy)^n = x^n y^n$, then $P(0)$ is true as both sides equates to $1$. For $P(n + 1)$, note $(xy)^{n+1} = (xy)^n xy = x^n y^n xy$ by inductive hypothesis, which then, by Definition 4.3.9, equals to $x^{n + 1} y^{n + 1}$ as desired.

b)

If direction:

Note $x^n = x^{n-1}x$. Note $n - 1 \in \N$ as each positive natural number has a natural predecessor (Lemma 2.2.10). Hence, since $x = 0$, $x^{n - 1}x = x^{n - 1} 0 = 0$ as desired.

Only if direction:

We prove the contraposition, let $P(n)$ be $x \neq 0 \Rightarrow x^n \neq 0$. Then, $P(1)$ is true as $x^1 = x^0x = x \neq 0$. For $P(n + 1)$, note $x^{n + 1} = x^nx$. Since $x \neq 0$ and $x^n \neq 0$ by $P(n)$, then their product $x^nx \neq 0$ as desired.

c)

Note if $y = 0$, then $y^n = 0 \geq 0$ as desired. For $y > 0$, Let $P(n)$ denote $y > 0 \Rightarrow y^n > 0$. Then, $P(0)$ is true as $y^0 = 1 > 0$. For $P(n+1)$, note if $y > 0$, then $y^{n+1} = y^n y > y^n0 = 0$ as desired.

For $x^n \geq y^n$ (given $x \geq y \geq 0$), let $P(n)$ denote $x^n \geq y^n$. Then, $P(0)$ is true as $x \geq y$. For $P(n + 1)$, note

$$
\begin{align*}
x^{n + 1} &= x^nx \\ 
          &\geq x^n y \quad &\text{As } x^n \geq 0, x > y\\ 
          &\geq y^ny \quad &\text{By } P(n) \\
          &= y^{n + 1} \quad &\text{By Definition 4.3.9}
\end{align*}
$$

As desired.

d)

Assume $x \geq 0$, then $|x^n| = x^n = |x|^n$ as desired. Assume $x < 0$, then $|x^n| = |(-1)^n(-x)^n| = |(-1)^n||(-x)^n| = |(-x)^n| = (-x)^n = |x|^n$ as desired.

We remain to show $|(-1)^n| = 1$. If $n = 0$, then $|(-1)^0| = 1$ as desired. For $P(n+1)$, note $|(-1)^{n+1}| = |(-1)^n(-1)| = |(-1)^n||-1| = 1 \times 1 = 1$ as desired.

### Exercise 4.3.4

a)

Assume $n, m$ negative, then $x^nx^m = (x^{-n})^{-1} \times (x^{-m})^{-1} = (x^{-n} x^{-m})^{-1} = (x^{-(n + m)})^{-1} = x^{n + m}$ as desired.  First equality follows from definition 4.3.11. Second equality follows from $a^{-1}b^{-1} = (ab)^{-1}$. Third equality follows from 4.3.10 a). Last inequality follows from definition 4.3.10 a). 

We remain to show $a^{-1}b^{-1} = (ab)^{-1}$. We first show that $a^{-1}$ as exponent is consistent with $a^{-1}$ as inverse. Note $a^{-1} = 1 / a = 1 \times \text{Inverse of }a$ as desired.

Then $(ab)^{-1}ab = 1$ by Proposition 4.2.4, then $(ab)^{-1}aba^{-1}b^{-1} = a^{-1}b^{-1}$, then, $(ab)^{-1}aba^{-1}b^{-1} = (ab)^{-1}(aa^{-1})(bb^{-1}) = (ab)^{-1}$ by Proposition 4.2.4 as desired.

Assume $n$ positive, $m$ negative. Let $m' = -m$ be positive. We propose Lemma 1: $x^a / x^b = x^{a - b}$ if $a, b, a - b \in \N$. We induct on $a$. If $a = 0$, then $x^{a - b} = x^{-b}, x^a / x^b = 1/ x^b = x^{-b}$ as desired.

Note definition 4.3.11 only ensures $1/x^n = x^{-n}$ if $n$ is negative. Hence, we prove Lemma 2: $1/x^n = x^{-n}$ for any $n \in \Z$. Proof: Assume $n \geq 0$, then $1/x^n = 1 / (1 / x^{-n})$ for some negative $-n$ by definition 4.3.11. Easy to verify $1 / (1 / a) = a$ for $a \in \R$, hence $1 / x^n = 1 / (1 / x^{-n}) = x^{-n}$ as desired, ensuring that $1/x^b = x^{-b}$ is true.

Therefore for $P(a + 1)$, $x^{a+1} / x^b = x(x^a) / x^b = x \times x^{a - b} = x^{(a + 1) - b}$, with second inequality is ensured by $P(a)$, other inequalities ensured by Definition 4.3.9 (As $a - b \in \N$) as desired.

We remain to show $x^nx^{-m'} = x^{n - m'}$. Note $x^n x^{-m'} = x^n \times (1 / x^{m'}) = x^n \times (x^{m'})^{-1} = x^n / x^{m'}$. The first inequality is ensured by Lemma 2, second inequality is ensured by Definition 4.3.11 and third inequality follows from definition of division.

Hence, if $n - m \geq 0$, result directly follows from Lemma 1. Otherwise, $x^n/x^{m'} = 1/(x^{m'} / x^n) = 1/x^{m' - n} = x^{n - m'}$ as desired.

For $(x^n)^{m} = x^{nm}$, assume $n, m$ are negative, then it remains to prove $(x^{-n'})^{-m'} = x^{-n'-m'}$ for $n' = -n, m' = -n, n', m' \in \N$.

We propose Lemma 3: $1/a^n = (1/a)^n$ for $n \in \N$. $P(0)$ is true as $1/a^0 = (1/a)^0 = 1$. For $P(n + 1)$:

$$
\begin{align*}
\frac{1}{a^{n+1}} &= \frac{1}{a a^n} \quad \text{By Definition 4.3.9} \\
                  &= \frac{1}{a} \frac{1}{a^n} \quad \text{By Division Rules} \\
                  &= \frac{1}{a} (\frac{1}{a})^n \quad \text{By } P(n) \\
                  &= (\frac{1}{a})^{n + 1}  \quad \text{By Definition 4.3.9}
\end{align*}
$$

As desired.

Then, with Lemma 3:
$$
\begin{align*}
(x^{-n'})^{-m'} &= (\frac{1}{x^{n'}})^{-m'} \quad \text{By Definition 4.3.11} \\
                &= 1 / ((1 / x^{n'})^{m'}) \quad \text{By Definition 4.3.11} \\
                &= 1 / (1 / (x^{n'})^{m'}) \quad \text{By Lemma 3} \\
                &= 1 / (1 / x^{n'm'}) \quad \text{By 4.3.10 (a)} \\
                &= x^{n'm'} \quad \text{By Division rules} \\
                &= x^{(-n')(-m')}
\end{align*}
$$

As desired.

Similarly, if $n$ is positive, and $m$ is negative, we let $m' = -m \in \N$, then:

$$
\begin{align*}
(x^n)^{-m'} &= 1 / (x^n)^{m'} \quad \text{By Definition 4.3.11} \\
            &= 1 / x^{nm'} \quad \text{By 4.3.10 (a)} \\
            &= x^{n(-m')} \quad \text{By Lemma 2} 
\end{align*}
$$

As desired.

If $n$ is negative, and $m$ is positive, then let $n' = -n \in \N$:

$$
\begin{align*}
(x^{-n'})^{m} &= (1 / x^{n'})^{m} \quad \text{By Definition 4.3.11} \\
              &= (1/(x^{n'})^{m}) \quad \text{By Lemma 3} \\
              &= 1 / x^{n'm} \quad \text{By 4.3.10 (a)} \\
              &= x^{(-n')m} \quad \text{By Lemma 2} 
\end{align*}
$$

As desired.

For $(xy)^n = x^n y^n$, consider $n$ negative, and let $n' = -n \in \N$:

$$
\begin{align*}
(xy)^{-n'} &= 1 / (xy)^{n'} \quad \text{By Definition 4.3.11} \\
            &= 1 / (x^{n'} y^{n'})  \quad \text{By 4.3.10 (a)} \\
            &= (1 / x^{n'})(1 / y^{n'}) \quad \text{By Definition 4.2.2} \\
            &= x^{-n'} y^{-n'} \quad \text{By Definition 4.3.11}
\end{align*}
$$

As desired.

b)

Say $n$ negative, then let $n' = -n \in \N, x = a/b, y = c/d, a,b,c,d \in \N$. Easy to verify $x^{-n'} = b^{n'} / a^{n'}$. By 4.3.10 c), $b^{n'} > 0, a^{n'} > 0$, hence $x^{-n'} > 0$ as desired as $x^{-n'} - 0$ is a positive rational number by Definition 4.2.6, and the inequality is true by 4.2.7.

For $x^{-n'} \leq y^{-n'}$, note:

$$
\begin{align*}
y^{n'} &\leq x^{n'} \quad \text{By 4.3.10 (c)} \\
1 &\leq \frac{x^{n'}}{y^{n'}} \quad \text{By 4.2.9 (e) and Lemma 1} \\
x^{-n'} &\leq y^{-n'} \quad \text{By 4.2.9 (e) and Lemma 1}
\end{align*}
$$

As desired. (Note: Definition 4.3.11 or many other facts can be used instead of Lemma 1).

c)

We start by introducing Lemma 4: $a^n = 1 \Rightarrow a = 1$, for $a \in \mathbf{Q}, n \in \Z - \{0\}$.

Proof: Consider $n$ positive, then we induct on $n$. Let $n = 1$, then $a^1 = 1$ implies $a = 1$ as desired. For $P(n+1)$, note $a^{n+1} = 1$ implies $a a^n = 1$ which by $P(n)$ implies $a = 1$ as desired.

For $n$ negative, let $n' = -n \in \N$, then:

$$
\begin{align*}
a^{-n'} &= 1 \\
a^{-n'}a^{n'} &= a^{n'} \\
1 &= a^{n'} \\
1 &= a
\end{align*}
$$

As desired.

Then:

$$
\begin{align*}
x^n &= y^n \\
x^n (\frac{1}{y})^n &= 1 \quad \text{By Lemma 3} \\
(x/y)^n &= 1 \quad \text{By 4.3.12 (a)} \\
x/y &= 1 \quad \text{By Lemma 4} \\
x &= y
\end{align*}
$$

As desired.

d)

We start with Lemma 5: $|1 / a| = 1 / |a|, a \neq 0$. Assume $a$ is positive, then easy to verify $1/a$ is positive, hence $|1 / a| = 1 / a = 1 / |a|$ as desired. Assume $a$ is negative, then easy to verify $1/a$ is negative, hence $|1 / a| = 1 / (-a) = 1 / |a|$ as desired.

Assume $n$ negative, then let $n' = -n \in \N$, then:

$$
\begin{align*}
|x^{-n'}| &= |\frac{1}{x^{n'}}| \quad \text{By Definition 4.3.11} \\
          &= \frac{1}{|x^{n'}|} \quad \text{By Lemma 5} \\
          &= \frac{1}{|x|^{n'}} \quad \text{By 4.3.10 (d)} \\
          &= |x|^{-n'} \quad \text{By Definition 4.3.11}
\end{align*}
$$

As desired.

### Exercise 4.3.5

Let $P(n)$ be $2^n \geq n$. Then, $P(1)$ is true as $2 > 1$. For $P(n + 1)$, note $2^{n + 1} = 2^n \times 2 \geq n \times 2$ by inductive hypothesis. Then $n \times 2 > n$ (as $n \times 2 - n = n \geq 1 > 0$) as desired.

### Proposition 4.4.5

Note: Tao's proof is difficult to understand with my average IQ, hence this writing to fill in the gaps.

Let $\epsilon > 0, \epsilon \in \mathbf{Q}$. Then, for contradiction assume no such $x$ exists. Then, the statement $x^2 < 2 < (x + \epsilon)^2$ is false for all nonnegative $x \in \mathbf{Q}$. This implies whenever $x^2 < 2$, $(x + \epsilon)^2 \leq 2$. (Otherwise $x^2 < 2 < (x + \epsilon)^2$ would be true). By Proposition 4.4.4, since $x + \epsilon \in \mathbf{Q}$, it cannot hold that $(x + \epsilon)^2 = 2$, hence it must hold that $(x + \epsilon)^2 < 2$.

We set $x = 0$. Since $x^2 < 2$ and $x$ is non-negative, it holds that $(0 + \epsilon)^2 < 2$, hence $\epsilon^2 < 2$.

Similarly, we set $x = \epsilon$, then since $\epsilon^2 < 2$, it holds that $(\epsilon + \epsilon)^2 \leq 2$, aka $(2\epsilon^2)<2$.

We then claim $(n\epsilon)^2<2$ for $n \in \N$. $P(0)$ is already proven. For $P(n + 1)$, note $(n \epsilon)^2 < 2$ by inductive hypothesis, hence set $x = n \epsilon$, then $(n \epsilon + \epsilon)^2 < 2$ implying $((n + 1)\epsilon^2) < 2$ as desired.

However, by proposition 4.4.1, there exists a natural number $n > 2 / \epsilon$, as $2 / \epsilon$ is a rational number. Hence, it holds that, for that particular $n$, $n \epsilon > 2$, hence $(n \epsilon)^2 > 4$. However $(n \epsilon)^2 < 2 < 4$, contradiction as desired.

My comment: basically the proof bounds $n \epsilon$ and constructs a large enough $n$ to show that $n \epsilon$ cannot be bounded to create contradiction. Proposition 4.4.1 is probably not strictly needed, and other estimation would suffice in the construction of sufficiently large $n$.

### Exercise 4.4.1

Consider $x \geq 0$, then $x = a/b$ for some $a, b \in \N$.

$$
\begin{align*}
n \leq x &< n + 1 \\
n \leq a/b &< n + 1\\
bn \leq a &< b(n + 1)
\end{align*}
$$

We claim there exists $n \in \N$ s.t. the above inequality is true. Note $bn \leq a$ iff $bn + c = a$ for some $c \in \N$, then by proposition 2.3.9 there exists such $n, c \in \N$ s.t. $bn + c = a$ and furthermore $c < b$.

We claim that the found $n$ satisfies $a < b(n + 1)$. Note $b(n + 1) - a = b(n + 1) - (bn + c) = b - c > 0$ as desired.

For $x < 0$, let $x' = -x$, then there exists $n' \in \N$ s.t. $n' \leq x' < n' + 1$, aka $-n' - 1 < x \leq -n'$.

Assume $x \neq n'$, then $x < n'$. We let $n = -n' - 1$, then $x < -n' = n + 1$, and $-n' - 1 = n + 1 - 1 = n$, hence $-n' - 1 < x$ implies $n < x$, which implies $n \leq x$ as desired.

Assume $x = n'$, then $x \in \Z$. We simply let $n = x$ as desired.

For uniqueness, say we have $n \leq x < n + 1, m \leq x < n + 1$. WLOG say $n < m$. Then $n < m \leq x < n + 1 < m + 1$. Hence $n < m < n + 1$. Hence $m \in \Z$ is between two consecutive integers, contradiction.

We can prove that $n < m < n + 1$ does indeed lead to contradiction. Since $n < m$, $m - n = d$ for some positive integer $d$. Similarly $n + 1 - m = d'$ for some positive $d'$. Note $n + 1 - m = -(m - n) + 1 = -d + 1 = d'$, hence $d' + d - 1 = 0$. Since $d - 1$ is natural by Lemma 2.2.10, by Corollary 2.2.9, $d' = d - 1 = 0$, hence $d = 1$. However, $d' + (d - 1) = (d' - 1) + d$, hence similarly $d = 0$, contradiction as desired. 

### Exercise 4.4.2

a)

We claim $\forall n \in \N, a_n \geq k$ for all $k \in \N$.

We induct on $k$. Base case $P(0)$ is true as $\forall n \in \N, a_n \in \N$, and a natural number is either equal or greater than $0$ as desired.

For $P(k + 1)$, note:

$$
\begin{align*}
\forall n \in \N&, a_n > a_{n + 1} \geq k \quad \text{By} \; P(k) \\
\forall n \in \N&, a_n \geq k + 1
\end{align*}
$$

As desired.

Hence, we claim $a_1 \geq a_0$. Yet $a_0 > a_1$, contradiction as desired.

b)

Principle of infinite descent doesn't work if the sequence can take integer values. As, integer is not bounded below. Positive rational value also doesn't suffice. Consider the sequence $a_0 = 1, a_{n + 1} = a_n / 2$. Easy to prove for any arbitrary $n$, $a_n > 0$.

### Exercise 4.4.3

A natural number $p$ is either even or odd as say $p = 2k + r$, then there exists $k \in \N, 0 \leq r < 2$ s.t. $p = 2k + r$. Since $0 \leq r < 2$. $r = 0, 1$ as desired.

A natural number $p$ cannot be both even and odd, as, say $p = 2a = 2b + 1$ for some $a, b \in \N$, then $2a = 2b + 1, 2(a - b) = 1, a - b = 1/2$. However, integer subtraction is closed, yet $1/2$ is not an integer, contradiction as desired.

We can show $1/2$ is not an integer, as, assume $1/2$ is an integer, then there exists $a/1 = 1/2$, then $1 = 2a$ for some integer $a$. Easy to verify via induction $\forall a \in \N, 2a \neq 1$, and similarly $\forall a \in \N, -1 \neq 2a$ by trichotomy of order as desired.

If $p$ is odd, then $p = 2k + 1, p^2 = (2k + 1)^2 = 4k^2 + 4k + 1 = 2(2k^2 + 2k) + 1 = 2k' + 1$ as desired.

Since $p^2 = 2q^2$, then assume $q = p$, then $p^2 = 2p^2$ implying $pp = 0$ hence $p = 0$, contradiction as $p$ is positive integer.

Similarly assume $q > p$, then $q^2 > pq$ and $pq > p^2$, hence $q^2 > p^2, p^2 = 2q^2 > 2p^2$ implying $p^2 > 2p^2$, hence $0 > p^2$, hence $0 = p^2 + d$ for some $d \in \N$, hence $p^2 = 0$, hence $p = 0$, contradiction as desired.

### Exercise 5.1.1

Choose $\epsilon = 1$, then for some $N$, $|a_j - a_k| \leq 1$ for all $j, k \geq N$.

Then, $a_{1}^{N - 1}$ is bounded by some $M'$ Lemma 5.1.14. We claim $a_{N}^{\infty}$ is also bounded. Pick $a_k$ s.t. $k \geq N$, then $|a_k - a_N| \leq 1$. Then, note $|a_k| - |a_N| \leq |a_k - a_N|$, then $|a_k| \leq |a_k - a_N| + |a_N|\leq 1 + |a_N|$ as desired.

Hence, pick $M = M' + 1 + |a_N|$ as desired.

Proof for $|x| - |y| \leq |x - y|$:

Note $x = (x - y) + y$, hence $|x| \leq |x - y| + |y|$ by triangle inequality. Therefore $|x| - |y| \leq |x - y|$ as desired.

### Exercise 5.2.1

Note, for any $\epsilon, \epsilon'> 0$, there exists $N, N'$ s.t.

$$
\begin{align*}
\forall i,j \geq N, |a_i - a_j| \leq \epsilon \\
\forall i \geq N', |b_i - b_j| \leq \epsilon'
\end{align*}
$$

Then, pick $N'' = \max(N, N')$, it holds that:

$$
\begin{align*}
\forall i, j \geq N'', |b_i - b_j| \leq |b_i - a_i| + |a_i - b_j|& &\text{By triangle inequality} \\
\forall i,j \geq N'', |b_i - b_j| \leq \epsilon' + |a_i - b_j|& &\text{As } |b_i - a_i| \leq \epsilon' \\
\forall i,j \geq N'', |b_i - b_j| \leq \epsilon' + |a_i - a_j| + |a_j - b_j|& &\text{By triangle inequality} \\
\forall i,j \geq N'', |b_i - b_j| \leq \epsilon' + \epsilon + \epsilon'& \\
\forall i,j \geq N'', |b_i - b_j| \leq 2\epsilon' + \epsilon&
\end{align*}
$$

Hence, we simply let $\epsilon' = \epsilon = \epsilon'' / 3$, then it holds that:

$$
\forall i,j \geq N'', |b_i - b_j| \leq \epsilon''
$$

Hence $(a_n)_{n=1}^{\infty}$ is Cauchy Sequence implies $(b_n)_{n=1}^{\infty}$ is Cauchy Sequence. Easy to verify equivalent sequence is reflexive, symmetric and transitive, hence the other direction follows from symmetry as desired.

Comment: Thanks MVT and C-R equation proof telling me the triangle inequality trick.

### Exercise 5.2.2

Assume $a$ is bounded by some $M$, then:

$$
\begin{align*}
\forall i \geq N, |a_i - b_i| \leq \epsilon& &\text{As }a, b \text{ eventually } \epsilon \text{ close} \\
\forall i \geq N, |b_i| - |a_i| \leq |a_i - b_i| \leq \epsilon& &\text{By reverse triangle inequality} \\
\forall i \geq N, |b_i| - |a_i| \leq \epsilon& \\
\forall i \geq N, |b_i| \leq \epsilon + |a_i|& \\
\forall i \geq N, |b_i| \leq \epsilon + M& &\text{As } a \text{ is bounded by some } M
\end{align*}
$$

By Lemma 5.1.14, $(b_n)_{n=1}^{N - 1}$ is bounded by some $M'$, hence $(b_n)_{n=1}^{\infty}$ is bounded by $\max(M, \epsilon + M')$ as desired.

The other direction follows similarly.

### Exercise 5.3.1

Reflexivity:

Note $\forall n \geq 1, |a_n - a_n| = 0 \leq \epsilon$ for any $\epsilon > 0$ as desired.

Symmetry:

If $\forall n \geq N, |a_n - b_n| \leq \epsilon$, then $\forall n \geq N, |b_n - a_n| = |a_n - b_n| \leq \epsilon$ as desired.

Transitivity:

Say $\forall n \geq N, |a_n - b_n| \leq \epsilon, \forall n \geq M, |b_n - c_n| \leq \delta$, then $\forall n \geq \max(N, M), |a_n - c_n| \leq |a_n - b_n| + |b_n - c_n| = \epsilon + \delta$. Remains to set $\epsilon = \delta = \epsilon'/2$, then $\forall n \geq \max(N, M), |a_n - c_n| \leq |a_n - b_n| + |b_n - c_n| = \epsilon + \delta = \epsilon'$. as desired.

### Exercise 5.3.2

Show $xy$ is a real number:

By proposition 4.3.7 h), say $\forall i,j \geq N,|a_i - a_j| \leq \epsilon, \forall i,j \geq M, |b_i - b_j| \leq \delta$, then:

$$\forall i,j \geq \max(N, M), |a_ib_i - a_jb_j| \leq \epsilon|b_i| + \delta|a_i| + \epsilon\delta$$

Note by Lemma 5.1.15, $|a_i| \leq A, |b_i| \leq B$ for some $A, B \in \mathbb{Q}$. Hence:

$$\forall i,j \geq \max(N, M), |a_ib_i - a_jb_j| \leq \epsilon B + \delta A + \epsilon\delta$$

We wish that:

$$\forall i,j \geq N', |a_ib_i - a_jb_j| \leq \epsilon'$$

Hence, we let $N' = \max(N, M), \epsilon = \epsilon'/(3B), \delta = 2\epsilon' / 3(A + \epsilon)$, then:

$$
\begin{align*}
\forall i,j \geq \max(N, M), |a_ib_i - a_jb_j| \leq \epsilon B + \delta A + \epsilon\delta& \\
\forall i,j \geq N', |a_ib_i - a_jb_j| \leq \frac{\epsilon'}{3B} B + \frac{2\epsilon'}{3(A + \epsilon)}(A + \epsilon)& \\
\forall i, j \geq N', |a_ib_i - a_jb_j| \leq \frac{\epsilon'}{3} + \frac{2\epsilon'}{3} = \epsilon'&
\end{align*}
$$

As desired.

Note: Issa Rice offers a much cleaner way to do this part in contrast to the brute force above

Show $x = x' \Rightarrow xy = x'y$

Need to show:

$$\forall n \geq N', |a_nb_n - a_n'b_n| \leq \epsilon'$$

Note $$\forall n \geq N, |a_n - a_n'| \leq \epsilon$$ as $x = x'$.

Hence, let $N' = N, \epsilon = \epsilon' / B$ for which $b$ is bounded by $B$ (exists by Lemma 5.1.15), then:

$$
\begin{align*}
|a_nb_n - a_n'b_n| &= |b_n||a_n - a_n'| \\
                   &\leq B \epsilon'/B \\
                   &= \epsilon'
\end{align*}
$$

As desired.
### Exercise 5.3.3

If direction

It holds that $|a - b| \leq \epsilon$ for any $\epsilon \in \mathbb{Q}, \epsilon > 0$.

Assume $a \neq b$, then $|a - b| \neq 0$. Easy to verify $|a - b| > |a - b| / 2$. Hence, it cannot hold that $|a - b| \leq |a - b|/2$ by trichotomy of order, contradiction as desired.

Only if direction

Since $a = b$, $|a - b| = 0 \leq \epsilon$ for any $\epsilon > 0$ as desired.

### Exercise 5.3.4

Since $(b_n)^{\infty}_{n=0}$ is equivalent to $(a_n)^{\infty}_{n=0}$, $(b_n)^{\infty}_{n=0}$ is eventually $\epsilon$-close to $(a_n)^{\infty}_{n=0}$ for some $\epsilon > 0$. Rest follows from Exercise 5.2.2.

### Exercise 5.3.5

Need to show there exists $N$ s.t. $\forall n \geq N, |1/n - 0| \leq \epsilon$ for any $\epsilon > 0$.

Note $|1/n - 0| = 1/n \leq 1/N$, and, $1/N \leq \epsilon \Leftrightarrow 1/\epsilon \leq N$. By Proposition 4.4.1 such $N$ exists as desired.

### Exercise 5.4.1

Say $x$ is negative, then $x = (a_n)^{\infty}_{n=1}$ for some $(a_n)^{\infty}_{n=1}$ negatively bounded. Easy to verify $-x = -(a_n)^{\infty}_{n=1}$ is positively bounded. Other direction follows similarly.

Say $x = \operatorname{LIM}_{n\rightarrow\infty}(a_n)^{\infty}_{n=1}, y = \operatorname{LIM}_{n\rightarrow\infty}(b_n)^{\infty}_{n=1}$, with both sequence positively bounded away from zero. Then it holds that $a_n \geq A, b_n \geq B$ for some $A, B > 0, A, B \in \mathbb{Q}$. Hence $a_n + b_n \geq A + B > 0$ as desired. Similar reasoning for $xy$ being positive.

Other Part: Note we either have $x = 0$ or $x \neq 0$. Say $x = 0$ aka $x = \operatorname{LIM}_{n\rightarrow\infty}(0)_{n=1}^{\infty}$. Easy to verify $x$ is neither positive nor negative, hence the trichotomy.

Say $x \neq 0$, then we claim $x$ is either positive or negative. By Lemma 5.3.14 $x = \operatorname{LIM}_{n\rightarrow\infty} (a_n)^{\infty}_{n=1}$ for which $\forall n, |a_n| \geq c$ for some rational $c > 0$.

As $(a_n)^{\infty}_{n=1}$ is a Cauchy sequence, it holds that $\exists N, \forall n \geq N, |a_n - a_N| \leq \epsilon$ for all $\epsilon > 0$.

Since $a_N \neq 0$ (as $|a_N| > c$), either $a_N < 0$ or $a_N > 0$. WLOG assume $a_N < 0$, then $a_N = |a_N| \geq c$. Then WLOG assume $a_n - a_N \geq 0$, we then have $a_n - a_N \leq \epsilon$. Setting $\epsilon = c/2$ yields $a_n - a_N \leq c/2$. Since $|a_N| \geq c$ and $a_N < 0$, $a_N \leq -c$, hence:

$$
\begin{align*}
a_n - a_N \leq c/2& \\
a_n \leq c/2 + a_N \leq c/2 - c \leq -c/2&
\end{align*}
$$

Hence $\exists N, \forall n \geq N, a_n \leq -c/2$. Hence, we define $(b_n)^{\infty}_{n=1}$ s.t. $\forall n < N, b_n = -1, \forall n \geq N, b_n = a_n$. Easy to verify $|b_n| \leq \min(-1, -c/2)$ (aka $(b_n)^{\infty}_{n=1}$ is negatively bounded from $0$), $(b_n)^{\infty}_{n=1}$ is Cauchy and $(a_n)^{\infty}_{n=1} = (b_n)^{\infty}_{n=1}$ as desired.

### Exercise 5.4.2

Note by Proposition 5.3.11, Proposition 4.1.6 holds for $\R$.

a)

Consider $x - y$, then we either have $x - y > 0, x - y = 0, x - y < 0$, hence we either have $x > y, x = y, x < y$ as desired.

b)

One has $x < y$ iff $x - y$ is negative. Note $y - x = -(x - y)$. By Proposition 5.4.4, $y - x$ positive, hence $y > x$ as desired.

Other direction follows similarly.

c)

If $x < y$, then $y - x$ is positive, similarly $z - y$ is positive. Hence $(y - x) + (z - y) = z - x$ is positive (by Proposition 5.4.4), hence $x < z$ as desired.

d)

If $x < y$, then $y - x$ is positive. Note $(y + z) - (x + z) = y - x$, which is also positive, hence $y + z > x + z$ as desired.

e)

Proven in the text.

### Exercise 5.4.3

Uniqueness follows similar reasoning from Exercise 4.4.1.

For existence, we either have $x < 0, x = 0, x > 0$.

Consider the case $x > 0$, then we argue by contradiction. Assume $\lnot (\forall x \in \R^{+}, \exists N \in \Z, N \leq x < N + 1)$, then $\exists x \in \R^{+}, \forall N \in \Z, x < N \lor x \geq N + 1$. We claim for that particular $x$, $x \geq n$ for all $n \in \N$. We prove by induction.

For $P(0)$, $x > 0$ hence $x \geq 0$ as desired.

For $P(n+1)$, note we have $x < n \lor x \geq n + 1$. Easy to verify $x < n, x \geq n + 1$ are mutually exclusive. Note by $P(n)$, $x \geq n$. Hence $x < n$ cannot hold, therefore $x \geq n + 1$ as desired.

However, there exists $N \in Z^{+}$ s.t. $x \leq N$ by Proposition 5.4.12. Hence we have $x \geq N + 1$ (by $P(N + 1)$) and $x \leq N$, contradiction.

(Above proof similar to in-text proof for Proposition 4.4.5 and the inductive proof for principle of infinite descent).

For the case $x = 0$, $0 \leq 0 < 1$ as desired.

For the case $x < 0$, same reasoning in Exercise 4.4.1 solution applies.

Note: A direct proof using Proposition 4.4.1 and Corollary 5.4.10 would also suffice. Albeit I had enough suffering in this section already and I will not bother with it. The indirect proof is just much more elegant.

### Exercise 5.4.4

Easy to show for all $N \in \N$, $1/N > 0$.

Remains to show $\exists N \in \N, x > 1/N$ for any $x \in \R^{+}$. Note $x > 1/N \Rightarrow N > 1/x \Rightarrow N1 > 1/x$. Since $1, 1/x$ are positive real numbers, $N$ exists by Corollary 5.4.13 as desired.

### Exercise 5.4.5

Say $q = a/b$, then:

$$
\begin{align*}
x < a/b < y& \\
bx < a < by& \\
0 < a - bx < b(y - x)&
\end{align*}
$$

Now, note by Exercise 5.4.4, there exists $y - x > 1/N$ for some $N \in \Z^{+}$. We make leap of faith and claim $b = N$, then we remains to find $a \in \Z$. Note $y - x > 1/b$ implies $b(y - x) > 1$. Hence $a - bx \leq 1$ implies $a - bx < b(y - x)$

$$
\begin{align*}
0 < a - bx \leq 1& \\
bx < a \leq bx + 1
\end{align*}
$$

We proceed to prove in general $\exists a \in \Z, r < a \leq r + 1$ for all $r \in \R$. Note by Exercise 5.4.3, there exists $n \in \Z$ s.t. $n \leq r < n + 1$. We claim $a = n + 1$ is suitable, as $n \leq r \Rightarrow n + 1 \leq r + 1 \Rightarrow a \leq r + 1$, and $r < n + 1 \Rightarrow r < a$, as desired.

My comment: Too many leap of faith required for this question...

### Exercise 5.4.6

WLOG we only prove $<$ case as $\leq$ case is similar

If direction

We either have $x - y \geq 0$ or $x - y < 0$.

WLOG $x - y \geq 0$, then $|x - y| = x - y$. Hence $x - y < \epsilon$ implies $x < y + \epsilon$. Note $x - y \geq 0$ implies $y \leq x$, hence $y - \epsilon < y \leq x < y + \epsilon$ as desired.

Only if direction

Note $y - \epsilon < x < y + \epsilon$ iff $- \epsilon < x - y < \epsilon$. We argue by contradiction. Assume $|x - y| \geq \epsilon$, then either $x - y \geq \epsilon$ or $-\epsilon \geq x - y$. First one contradict $x - y < \epsilon$ and second one contradict $-\epsilon < x - y$ as desired.

### Exercise 5.4.7

First statement

If direction

Say $x \leq y$, then $x \leq y < y + \epsilon$ hence $x \leq y + \epsilon$ as desired.

Only if direction

Assume $x > y$, then $x - y = c$ for some $c > 0$. Then, we claim $x > y + c/2$, as $x - (y + c/2) = c - c/2 = c/2 > 0$. Hence let $\epsilon = c/2$, it cannot hold that $x \leq y + c/2$ as desired.

Second Statement

If direction

If $x = y$ then $x - y = 0$. Hence $|x - y| = x - y = 0 < \epsilon \leq \epsilon$ as desired.

Only if direction

Say we have $|x - y| \leq \epsilon$, then by Exercise 5.4.6 it holds that $y - \epsilon \leq x \leq y + \epsilon$. Hence, $x \leq y + \epsilon$ for any $\epsilon > 0$ implies $x \leq y$ by the first statement. $y - \epsilon \leq x \Rightarrow y \leq y + \epsilon$ for any $\epsilon > 0$ implies $y \leq x$. Hence, $x \leq y \land y \leq x$ implies $x = y$ as desired.

### Exercise 5.4.8

We prove the contraposition. Assume $\operatorname{LIM}_{n\rightarrow\infty} a_n > x$, then by Proposition 5.4.14 there exists $q \in \mathbb{Q}$ s.t. $\operatorname{LIM}_{n\rightarrow\infty} a_n > q > x$. Hence, $\operatorname{LIM}_{n\rightarrow\infty}a_n > \operatorname{LIM}_{n\rightarrow\infty}q$. Therefore $\lnot (\operatorname{LIM}_{n\rightarrow\infty} a_n\leq \operatorname{LIM}_{n\rightarrow\infty}q)$, hence by Corollary 5.4.10 $\exists n \geq 1, a_n > q > x$. Hence $\lnot \forall n \geq 1, a_n \leq x$ as desired.

### Exercise 5.5.1

Assume $-M \neq \inf(-E)$, then, either:

- $-M$ is not a lower bound
- There exists $-M' > -M$ which is a lower bound

Assume $-M$ is not a lower bound, then $\exists -x \in -E, -x < M$. Hence it holds that $x \geq M$. Note $-x \in -E \Leftrightarrow x \in E$. Hence $x \geq M$ means $M \neq \sup(E)$, contradiction.

Assume $-M' > -M$ exists which is a lower bound, then $\forall -x \in -E, -x \geq -M'$. Hence $\forall x \in E, -x \geq -M'$, hence $\forall x \in E, x \leq M'$. Therefore $M' < M$ is also an upper bound for $E$, contradiction.

Note: it may seen trivial that $-x \in -E \Leftrightarrow x \in E$, however it can still be proven. $x \in E \Rightarrow -x \in -E$ follows from Axiom of substitution. $-x \in -E \Rightarrow x \in E$ as for every $-x \in -E$ there exists $x' \in E$ s.t. $-x' = -x$ by Axiom of substitution, hence $x = x' \in E$ as desired.

### Exercise 5.5.2

Similar to Exercise 5.4.3 Solution.

Say $\lnot (\exists L < m \leq k, m/n \text{ is upper bound} \land (m - 1) / n \text{ is not upper bound})$, then $\forall L < m \leq k, m/n \text{ is not upper bound} \lor (m - 1) / n \text{ is upper bound}$.

Now we induct on $m$ and claim $L \leq m \leq k \rightarrow m/n \text{ is not upper bound}$.

For base case $m = L$, $L / n$ is not upper bound as desired.

For $P(m + 1)$, note if $m+ 1 \leq k$, then either $(m + 1) / n$ is not upper bound or $m/n$ is upper bound. Since $m/n$ is not upper bound by $P(m)$, $(m + 1)/n$ is not upper bound has to hold as desired, closing the induction.

Hence, since $L \leq k \leq k$, it holds that $k/n$ is not an upper bound, contradiction.

### Exercise 5.5.3

Since $(m - 1)/n$ is not upper bound, there exists element $x \in E$ s.t. $x > (m - 1) / E$. Similarly there exists $x' \in E, x' > (m' - 1) / E$. Let $X = \max(x, x')$, easy to verify $X \in E, X > (m - 1)/E, X > (m' - 1)/E$.

WLOG say $m > m'$, then:

$$
\begin{align*}
m/n \geq X > (m - 1) / n \\
m'/n \geq X > (m' - 1) / n \\
m/n > m'/n \geq x > (m - 1) / n > (m' - 1) / n
\end{align*}
$$

Hence we have $m'/n > (m - 1)/n$ and $m/n > (m' - 1)/n$, therefore $m' > m - 1, m > m' - 1$, hence by Proposition 2.2.12 e), $m' \geq m, m \geq m'$, therefore $m = m'$, contradiction as desired.

### Exercise 5.5.4

By Corollary 5.4.13, for any $\epsilon$ there exists $M \in \Z^{+}$ s.t. $1 < \epsilon M$, hence there exists $M$ s.t. $1/M < \epsilon$.

Therefore, $|q_n - q_{n'}| \leq 1/M < \epsilon$ as desired.

To prove that $\forall M \geq 1, |q_M - S| \leq 1/M$, note:

$$
\begin{align*}
\forall M \geq 1, \forall n \geq M, |q_n - q_M| \leq 1/M \quad \text{By Given Property} \\
\forall M \geq 1, \forall n \geq M, q_M - 1/M \leq q_n \leq q_M + 1/M \quad \text{By Exercise 5.4.6}
\end{align*}
$$

Now define $q'_n = q_n$ if $n \geq M$, $q_M$ if $n < M$, easy to verify $(q'_n)^{\infty}_{n=1}$ is Cauchy and $\operatorname{LIM}_{n\rightarrow\infty}(q'_n)^{\infty}_{n=1} = \operatorname{LIM}_{n\rightarrow\infty}(q_n)^{\infty}_{n=1}$.

Note $\forall n \geq 1, q_M - 1/M \leq q'_n \leq q_M + 1/M$, hence by Exercise 5.4.8, $q_M - 1/M \leq S \leq q_M + 1/M$, hence $|q_M - S| \leq 1/M$ follows from Exercise 5.4.6.

### Exercise 5.5.5

We start by proving a stronger version of Proposition 5.5.14. Given $x, y \in \R, x < y$, we can always find $r \in \mathbb{Q}, r \neq 0$ s.t. $x < r < y$.

If $x, y > 0$ or $x , y < 0$, then apply Proposition 5.5.14, easy to verify $r > 0$ or $r < 0$ correspondingly.

WLOG if $x \leq 0, y > 0$, apply Proposition 5.5.14 to find $y/2 < r < y$, as desired.

Denote $x = \sqrt{2}$ as the real number such that $x > 0, x^2 = 2$. It exists by Proposition 5.5.12.

Then, by stronger version of Proposition 5.4.14, there exists $r \in \mathbb{Q}$ s.t. $x / \sqrt{2} < r < y / \sqrt{2}$. Hence, $x < \sqrt{2}r < y$. We claim that $\sqrt{2}r$ is irrational. Assume $\sqrt{2}r$ is rational, then $\sqrt{2}r / r = \sqrt{2}$ (we can divide as $r \neq 0$), hence $\sqrt{2}$ is rational as division is closed, contradicting Proposition 4.4.4.

### Exercise 5.6.1

a)

We denote $E: \{y' \in \R, y' \geq 0, (y')^n \leq x\}$. Hence $y = x^{1/x} = \sup(E)$

We argue by contradiction. Assume $y^n \neq x$, then either $y^n < x$ or $y^n > x$.

Assume $y^n < x$, then we claim we can find $0 < \epsilon < 1$ s.t. $(y + \epsilon)^n \leq x$, hence $y + \epsilon \in E$, yet $y + \epsilon > \sup(E)$, contradiction.

For construction of $\epsilon$, we establish estimation for $(y + \epsilon)^n$:

$$
\begin{align*}
(y + \epsilon)^n &= \sum_{j=0}^{n} \binom{n}{j} y^j\epsilon^{n-j}& \text{Binomial Theorem} \\
&= y^n + \sum_{j=0}^{n-1}\binom{n}{j}y^{j}\epsilon^{n-j} \\
&= y^n + \sum_{j=0}^{n-1}\binom{n}{j} y^{j} \epsilon \epsilon^{n-j-1} \\
&\leq y^n + \sum_{j=0}^{n-1}\binom{n}{j} y^{j} \epsilon& \text{As } \epsilon \leq 1, \epsilon^i \leq 1 \text{ for } i \in \N\\
&= y^n + k_{n, y}\epsilon& \text{By factoring out } \epsilon
\end{align*}
$$

With $k_{n, y} \in \R^{+}$ depending on $n, y$. We remain to show that we can find $0 < \epsilon < 1$ such that $y^n + k_{n,y} \epsilon \leq x$. Since $y^n < x$, it is always possible, as desired. (e.g. we can let $\epsilon = \min(1/2, (x - y^n)/k_{n, y})$, easy to verify $0 < \epsilon < 1$ and $y^n + k_{n, y} \epsilon \leq x$).

Note: we take $\min$ as $x - y^n$ may exceed $k_{n, y}$ causing the obvious choice $\epsilon = (x - y^n)/k_{n, y}$ to fail as $\epsilon > 1$.

Similarly, assume $y^n > x$, we claim we can find $0 < \epsilon < 1$ s.t. $(y - \epsilon)^n > x$. Hence, $y - \epsilon$ is a lower bound of $E$, yet $y - \epsilon <\sup(E)$, contradiction.

For $y - \epsilon$ being lower bound: assume $\exists y' \in E, y - \epsilon < y'$, then $(y - \epsilon)^n \leq (y')^n \leq x$, yet $(y - \epsilon)^n > x$, contradiction.

To find $0 < \epsilon < 1$, we establish estimation for $(y - \epsilon)^n$:

$$
\begin{align*}
(y - \epsilon)^n &= \sum_{j=0}^{n} \binom{n}{j} y^j(-\epsilon)^{n-j}& \text{Binomial Theorem} \\
&= y^n + \sum_{j=0}^{n-1}\binom{n}{j}y^{j}(-\epsilon)^{n-j} \\
&> y^n + \sum_{n - j \text{ odd}, j=0}^{n-1} \binom{n}{j}y^j (-\epsilon^{n-j})& \text{Discard Positive Terms} \\
&= y^n + \sum_{n - j \text{ odd}, j=0}^{n-1} \binom{n}{j}y^j \epsilon(-\epsilon^{n-j-1})& \\
&\geq y^n + \sum_{n - j \text{ odd}, j=0}^{n-1} \binom{n}{j}y^j \epsilon(-1)& \text{As } \epsilon \leq 1, -\epsilon^i \geq -1 \text{ for } i \in \N\\
&= y^n - \sum_{n - j \text{ odd}, j=0}^{n-1} \binom{n}{j}y^j \epsilon& \\
&= y^n - k_{n, y}\epsilon& \text{By factoring out } \epsilon
\end{align*}
$$

Remains to show there exists $0 < \epsilon < 1$ s.t. $y^n - k_{n, y}\epsilon \geq x$. Since $y^n > x$, we similarly take $\epsilon = \min(1/2, (y^n - x)/k_{n, y})$ as desired.

Note: Part a) basically shows $(x^{1/n})^n = x$, aka cancellation.

b)

Note since $y^n = x$, $((y^n)^{1/n})^n = (x^{1/n})^n$. By a), $((y^n)^{1/n})^n = y^n$, hence we have $y^n = (x^{1/n})^n$, with $n \in \Z^{+}$. By Proposition 5.6.3 & Proposition 4.3.12 c), $y = x^{1/n}$ as desired.

Note: Part b) basically shows $(y^{n})^{1/n} = y$, aka cancellation in slightly different order.

c)

I assume it actually means $x > 0 \Rightarrow x^{1/n} > 0$.

Note by definition $x^{1/n} = \sup\{y \in \R, 0 \leq y \land y^n \leq x\}$. Since $0 \in \{y \in \R, 0 \leq y \land y^n \leq x\}$, it holds that $x^{1/n} \geq 0$. Remains to show $x^{1/n} \neq 0$. Assume $x^{1/n} = 0$, then $(x^{1/n})^n = 0$ as $n \neq 0$. By Lemma 5.6.6 a), $(x^{1/n})^n = x$, hence $x = 0$, contradicting $x > 0$ as desired.

d)

By Proposition 4.3.10 c), $x^{1/n} > y^{1/n}$ iff $(x^{1/n})^n > (y^{1/n})^n$. By a), $(x^{1/n})^n = x, (y^{1/n})^n = y$. Hence $(x^{1/n})^n > (y^{1/n})^n$ iff $x > y$ as desired.

e)

For case $x > 1$:

$$
\begin{align*}
x > 1& \\
x^{k+1} > x^{k}& \quad \text{By 5.4.7 \& 4.2.9 e)}\\
(x^{1/k})^{k(k+1)} > (x^{1/(k+1)})^{k(k+1)}& \quad \text{By a), 5.6.3, 4.3.10 a)} \\
x^{1/k} > x^{1/(k+1)}& \quad \text{By 5.6.3 \& 4.3.10 c)}&
\end{align*}
$$

Remain follows from simple induction.

Case $x < 1$ is similar.

f)
$$
\begin{align*}
xy = xy& \\
((xy)^{1/n})^n = (x^{1/n})^n (y^{1/n})^n& \quad \text{By a)} \\
((xy)^{1/n})^n = (x^{1/n}y^{1/n})^n& \quad \text{By 5.6.3 \& 4.3.10 a)} \\
(xy)^{1/n} = x^{1/n} y^{1/n}& \quad \text{By 5.6.3 \& 4.3.10 c)}
\end{align*}
$$

g)

$$
\begin{align*}
x = x& \\
((x^{1/n})^{1/m})^{nm} = (x^{1/nm})^{nm}& \quad \text{By a), 5.6.3, 4.3.10 a)}\\
(x^{1/n})^{1/m} = x^{1/nm}& \quad \text{By 5.6.3 \& 4.3.10 c)}
\end{align*}
$$

### Exercise 5.6.2

Let $q = a/b, r = c/d, a,b,c,d \in \Z^{+}$
a)

$x^q = (x^{1/a})^b$ by Definition 5.6.7. Since $x > 0$, $x^{1/a} > 0$ by 5.6.6 d), and $(x^{1/a})^b > 0$ by 4.3.10 c) as desired.

b)

$$
\begin{align*}
(x^{1/bd})^{ad + bc} = (x^{1/bd})^{ad}(x^{1/bd})^{bc}& \quad \text{By 4.3.10 a)} \\
x^{a/b + c/d} = x^{a/b}x^{c/d}& \quad \text{By 5.6.7}
\end{align*}
$$

$$
\begin{align*}
x^{a/b} = x^{ad/bd}& \quad \text{By 5.6.8}\\
((x^{a/b})^{1/d})^d = (x^{a/bd})^d& \quad \text{By 5.6.6 a), 5.6.7}\\
(x^{a/b})^{1/d} = x^{a/bd}& \quad \text{By 4.3.10 c)} \\
((x^{a/b})^{1/d})^{c} = (x^{a/bd})^{c} \\
({n\rightarrow\infty}({n\rightarrow\infty}(x^{a/b})^{c/d} = ((x^{1/bd})^a)^c& \quad \text{By 5.6.7} \\
(x^q)^r = (x^{1/bd})^{ac}& \quad \text{By 4.3.10 a)} \\
(x^q)^r = x^{ac/bd}& \quad \text{By 5.6.7} \\
(x^q)^r = x^{qr}
\end{align*}
$$

c)

$$
\begin{align*}
x^{-q} &= x^{-a/b} \\
       &= (x^{1/{b}})^{-a} \\
       &= 1/(x^{1/b})^a\\
       &= 1/x^{a/b} \\
       &= 1/x^q
\end{align*}
$$

d)

Note $x^{a/b} > y^{a/b}$ iff $(x^{a/b})^b > (y^{a/b})^b$ by Proposition 4.3.10 c) iff $x^a > y^a$ by 5.6.9 b) iff $x > y$ by Proposition 4.3.10 c) as desired.

e)

Let $q = a/b, r = c/d, a,b,c,d \in \Z, c,d > 0$. Then $q > r$ iff $q - r > 0$ iff $ad - bc > 0$ iff $ad > bc$. 

WLOG say $x > 1$  then $x^{q} = x^{ad/bd} > x^{bc/bd} = x^{r}$ iff $ad > bc$ by 5.6.6 e) as desired.

### Exercise 5.6.3

Assume $x = 0$, easy to verify $LHS = RHS = 0$.

Assume $x > 0$, then by Lemma 5.6.9 b), $RHS = x$. $LHS = x$ by definition of absolute value as desired.

Assume $x < 0$, then $x = -y$ for some $y > 0$. Remains to show $|-y| = ((-y)^{2})^{1/2}$. Note $LHS = y$ by definition. For RHS, $(-y)^2 = y^2$, and $(y^2)^{1/2} = y$ by 5.6.9 b) as desired.

### Exercise 6.1.1

We fix $n$ and induct on $m$.

For $m = n + 1$, clearly $a_m = a_{n+1} > a_{n}$ as desired.

For $m+1$, note $a_{m+1} > a_m$, and $a_m > a_n$ by inductive hypothesis as desired.

### Exercise 6.1.2

$(a_n)^{\infty}_{n=m}$ converges to $L$ iff $(a_n)^{\infty}_{n=m}$ is eventually $\epsilon$-close to $L$ for any $\epsilon > 0$, which happens iff $(a_n)_{n=N}^{\infty}$ is $\epsilon$-close to $L$ for some $N \geq m$ any $\epsilon > 0$, which happens iff $\forall \epsilon > 0, \exists N \geq M, \forall n \geq N, |a_n - L| \leq \epsilon$ as desired.

Every iff is ensured by Definition 6.1.5. 

### Exercise 6.1.3

Only if:

Since $(a_n)^{\infty}_{n=m}$ is convergent to $c$, $\forall \epsilon > 0, \exists N \geq m, \forall n \geq N, |a_n - c| \leq \epsilon$.

Since $m' \geq m$, it holds that $N \geq m'$, hence $\forall \epsilon > 0, \exists N \geq m', \forall n \geq N, |a_n - c| \leq \epsilon$. Therefore $(a_n)^{\infty}_{n=m'}$ is convergent as desired.

If

We have $\forall \epsilon > 0, \exists N' \geq m', \forall n \geq N', |a_n - c| \leq \epsilon$. We choose $N = \max(N, m)$, easy to verify $N \geq m$ and $N \geq N'$. Since $N \geq N'$, $\forall n \geq N, |a_n - c| \leq \epsilon$ implies $\forall n \geq N', |a_n - c| \leq \epsilon$ as desired.

### Exercise 6.1.4

If

We have  $\forall \epsilon > 0, \exists N \geq m, \forall n \geq N, |a_{n+k} - c| \leq \epsilon$.

Hence, we have $\forall \epsilon > 0, \exists N + k \geq m, \forall n, n + k \geq N + k, |a_{n+k} - c| \leq \epsilon$. Let $N' = N + k$, we claim $\forall \epsilon > 0, \exists N' \geq m, \forall n' \geq N', |a_{n'} - c| \leq \epsilon$. Say given $n' \geq N'$, then $n' = n + k$ for some $n \geq N' - k = N$, hence $|a_{n'} - c| = |a_{n+k} - c| \leq \epsilon$ as desired.

Only if:

We have $\forall \epsilon > 0, \exists N' \geq m, \forall n' \geq N', |a_{n'} - c| \leq \epsilon$.

We need to show  $\forall \epsilon > 0, \exists N \geq m, \forall n \geq N, |a_{n+k} - c| \leq \epsilon$.

Similarly, we let $N = N'$. Note $n + k \geq N = N'$. Hence let $n' = n + k$, $|a_{n+k} - c = |a_{n'} - c| \leq \epsilon$ asa desired.

Alternative proof (informal):

Note we have $(a_{n+k})^{\infty}_{n = m}$ term by term equal to $(a_n)^{\infty}_{n = m + k}$. Hence result follows from Exercise 6.1.3.

Albeit, the problem being... need to show term by term equal yields the same limit. The concept seems to be obvious, as both intuitively represent the same sequence, but proving it may be another story.

### Exercise 6.1.5

We have $\forall \epsilon' > 0, \exists N' \geq m, \forall n \geq N', |a_{n} - c| \leq \epsilon'$

We need to show $\forall \epsilon > 0, \exists N \geq m, \forall i, j \geq N, |a_{i} - a_{j}| \leq \epsilon$.

Let $\epsilon' = \epsilon / 2$, then $\exists N' \geq m, \forall n \geq N', |a_n - c| \leq \epsilon / 2$. Choose $N = N'$, then $|a_i - a_j| \leq |a_i - L| + |L - a_j| = \epsilon/2 + \epsilon/2 = \epsilon$ as desired.

### Exercise 6.1.6

Let $(a_n)^{\infty}_{n=m}$ be a Cauchy Sequence of rationals and let $L = \operatorname{LIM}_{n\rightarrow\infty} a_n$. Then:

$$\forall \epsilon > 0, \exists N \geq m, \forall i, j \geq m, |a_i - a_j| \leq \epsilon$$

We argue by contradiction. Assume $(a_n)^{\infty}_{n=m}$ does not converge to $L$, then:

$$\exists \epsilon > 0, \forall M \geq m, \exists i' \geq M, |a_{i'} - L| > \epsilon$$

Hence, choosing that $\epsilon$, and noting $(a_n)^{\infty}_{n=m}$ is $\epsilon/2$ stable, then:

$$\exists N \geq m, \forall i, j \geq N, |a_i - a_j| \leq \epsilon/2$$

Since $i' \geq n$, then $\forall j \geq N, |a_{i'} - a_j| \leq \epsilon/2$. By Exercise 5.4.6, $\forall j \geq N, a_{i'} - \epsilon/2 \leq a_{j} \leq a_{i'} + \epsilon/2$.

WLOG say $a_{i'} - L \geq 0$, then $a_{i'} - L = |a_{i'} - L| > \epsilon$. Note $a_j \geq a_{i'} - \epsilon/2$. Hence $a_{i'} - L + a_j > \epsilon + a_{i'} - \epsilon/2$, which simplifies to $\forall j \geq N, a_j > L + \epsilon/2$

We construct sequence $(b_n)^{\infty}_{n=1}$ s.t. $\forall j < M, b_j = L + \epsilon/2, \forall j \geq M, b_j = a_j$. Then it holds that $\forall j \geq 1, b_j \geq L + \epsilon/2$. By Exercise 5.4.3, $L = \operatorname{LIM}_{n\rightarrow\infty} a_j = \operatorname{LIM}_{n\rightarrow\infty} b_j \geq L + \epsilon/2$. Hence $L \geq L + \epsilon/2 \Rightarrow 0 \geq \epsilon/2$, contradiction as desired.

Comment: Basically we show that if $(a_n)^{\infty}_{n=m}$ doesn't converge to $L$, then its formal limit is not $L$ either. The tricky part is usage of Exercise 5.4.6 and how cases should be split. Very tricky to see the sign of $a_{i'} - L$ matters.

### Exercise 6.1.7

Assume a sequence of rational numbers $(a_n)^{\infty}_{n=m}$ is bounded by a real number $M$. Then, by proposition 5.4.14 there exists $r \in \mathbb{Q}, M < r < M + 1$. Hence $(a_n)^{\infty}_{n=m}$ is bounded by $r$ as desired.

### Exercise 6.1.8

a)

Need to show:

$$\forall \epsilon > 0, \exists M \geq m, \forall n \geq m, |a_n + b_n - (x + y)| \leq \epsilon$$

Note we have $\exists A \geq M, \forall n \geq M, |a_n - x| \leq \epsilon/2, \exists B \geq M, \forall n \geq M, |b_n - y| \leq \epsilon/2$. Hence, choose $M = \max(A, B)$, then $\forall n \geq M, |a_n + b_n - (x + y)| \leq |a_n - x| + |b_n - y| = \epsilon$ as desired.

b)

I can use 4.3.7 h), however it is... ugly. Hence using something else this time.

Need to show:
$$\forall \epsilon > 0, \exists M \geq m, \forall n \geq M, |a_nb_n - xy| \leq \epsilon$$

Note by Corollary 6.1.17, $\forall n, |a_n| \leq U$. Then:

$$\exists A \geq m, \forall n \geq M, |a_n - x| \leq \epsilon/(2U)$$

$$\exists B \geq m, \forall n \geq M, |b_n - y| \leq \epsilon/(2|y|)$$

Hence, choose $M = \max(A, B)$, it holds that, for all $n \geq M$:

$$
\begin{align*}
|a_nb_n - xy| &= |a_nb_n + a_ny - a_ny - xy| \\
              &= |a_n(b_n - y) + y(a_n - x)| \\
              &\leq |a_n||b_n - y| + |y||a_n - x| \\
              &\leq U|b_n - y| + |y||a_n - x| \\
              &\leq U \epsilon/(2U) + |y| \epsilon/(2|y|) \\
              &= \epsilon 
\end{align*}
$$

As desired.

c)

Follows from b) by defining $b_n = c$ for all $n$.

d)

$$
\begin{align*}
\lim_{n\rightarrow\infty}(a_n - b_n) &= \lim_{n\rightarrow\infty} (a_n + (-b_n)) \\
&= \lim_{n\rightarrow\infty} a_n + \lim_{n\rightarrow\infty} (-b_n) &\quad \text{By a)} \\
&= \lim_{n\rightarrow\infty} a_n - \lim_{n\rightarrow\infty} b_n &\quad \text{By c)}
\end{align*}
$$

e)

Note we have:

$$\forall \epsilon' > 0, \exists N' \geq m, \forall n \geq N',|b_n - y| \leq \epsilon'$$

Then, note by Lemma 5.3.15, $b_n^{-1}$ is a Cauchy Sequence, by Proposition 6.1.15, a Cauchy Sequence is convergent, by Corollary 6.1.17, a convergent sequence is bounded, hence, $|b_n^{-1}| \leq U$ for some $U$.

We need to show:

$$\forall \epsilon > 0, \exists N \geq M, |1/b_n - 1/y| \leq \epsilon$$

Hence, choose $\epsilon' = y\epsilon/M, N = N'$, it holds that, for $n \geq N$:

$$
\begin{align*}
|1/b_n - 1/y| &= \frac{1}{|b_n|y}|y - b_n| \\
              &\leq \frac{M}{y} y\epsilon/M \\
              &= \epsilon
\end{align*}
$$

As desired.

f)

$$
\begin{align*}
\lim_{n\rightarrow\infty} \frac{a_n}{b_n} &= \lim_{n\rightarrow\infty} a_n b_n^{-1} \\
&= \lim_{n\rightarrow\infty} a_n \lim_{n\rightarrow\infty} b_n^{-1} &\quad \text{By b)} \\
&= \lim_{n\rightarrow\infty} a_n (\lim_{n\rightarrow\infty} b_n)^{-1} &\quad \text{By c)} \\
\end{align*}
$$

As desired.

g)

WLOG assume $x \leq y$, then:

$$\exists A \geq m, \forall n \geq A, |a_n - x| \leq \frac{y - x}{2}$$

$$\exists B \geq m, \forall n \geq B, |b_n - y| \leq \frac{y - x}{2}$$

Hence, for all $n \geq \max(A, B)$:

$$
a_n \leq x + \frac{y - x}{2} = \frac{x + y}{2} = y - \frac{y - x}{2} \leq b_n
$$

Hence $\forall n \geq \max(A, B), a_n \leq b_n$.

Since $(b_n)^{\infty}_{n=m}$ is convergent, it holds:

$$
\begin{align*}
\forall \epsilon > 0, \exists N' \geq m, \forall n \geq N', |b_n - y| \leq \epsilon
\end{align*}
$$

Choose $N = \max(N', A, B)$, it holds that:

$$
\begin{align*}
\forall \epsilon > 0, \exists N \geq m, \forall n \geq N, |b_n - y| \leq \epsilon \\
\forall \epsilon > 0, \exists N \geq m, \forall n \geq N, |\max(a_n, b_n) - \max(x, y)| \leq \epsilon
\end{align*}
$$

As desired.

h)

We exploit duality of $\max, \min$.
$$
\begin{align*}
\lim_{n\rightarrow\infty} \min(a_n, b_n) &= \lim_{n\rightarrow\infty} -\max(-a_n, -b_n) \\
&= -\lim_{n\rightarrow\infty} \max(-a_n, -b_n) &\quad \text{By c)} \\
&= -\max(\lim_{n\rightarrow\infty} -a_n, \lim_{n\rightarrow\infty} -b_n) &\quad \text{By g)} \\
&= \min(\lim_{n\rightarrow\infty} a_n, \lim_{n\rightarrow\infty} b_n)
\end{align*}
$$
### Exercise 6.1.9

We can have $a_n = b_n = 1/n, a_n/b_n = 1$. Hence $LHS = 1$, yet $RHS$ is undefined as $\lim_{n\rightarrow\infty}b_n = 0$.

### Exercise 6.1.10

Only if direction is trivial as $\epsilon \in \mathbb{Q} \rightarrow \epsilon \in \R$.

For if direction, given $\epsilon \in \R$, then there exists $0 < \epsilon' < \epsilon$, s.t. $\epsilon' \in \mathbb{Q}$ by Proposition 5.4.14. Hence, $\exists N' \geq 0, \forall n \geq N, |a_n - b_n| \leq \epsilon'$. We let $N = N'$, then $\forall \epsilon \in \R^{+}, \exists N \geq 0, \forall n \geq N, |a_n - b_n| \leq \epsilon' < \epsilon$ as desired.

### Exercise 6.2.1

Reflexivity:

Note $\R^{*} = \R \cup \{\infty\} \cup \{-\infty\}$

Hence, since $\infty, -\infty$ are distinct from all elements in $\R$ by Definition 6.2.1, it holds that a number $x \in \R^{*}$ is either:

- $x \in \R$
- $x = \infty$
- $x = -\infty$

$x \in \R$ case follows from Definition 6.2.3 a) and analogue of reflexivity in $\R$ .

For $x = \infty$, $x \leq x$ follows from Definition 6.2.3 b). $x = -\infty$ case follows from Definition 6.2.3 c), as desired.

Trichotomy:

When $x, y \in \R$, trichotomy follows from analogue in $\R$ (Proposition 5.4.7).

When $x \in \R, y = \infty$, $x = y$ is false by Definition 6.2.1. $x < y$ is true as $x \leq y$ (By Definition 6.2.3 b)) and $x \neq y$. $x > y$ is false as $x \geq y$ (aka $y \leq x$) is false. (We can verify neither of 6.2.3 a), b), c) are satisfied).

$7$ cases remain, and the verification is similar to above cases hence omitted.

Transitivity:

If $x, y, z \in \R$, follows from analogue in $\R$.

If $x \in \R^{*} - \R, y, z \in \R$, easy to verify $x = -\infty$, hence since $z \in \R$, $x < z$ as desired.

Other cases follow similarly. There may be a proof not involving 8 cases (prob via building some Lemmas first) but I am too average to figure it out.

Negation reverses order:

If $x, y \in \R$, follows from analogue in $\R$.

If $x \in \R^{*} - \R, y \in \R$, easy to verify $x = -\infty$. Hence $-x = \infty$, $-y \leq \infty = -x$ as desired.

Other case follow similarly.

### Exercise 6.2.2

If $E \subseteq \R$, then the 3 claims follow from Definition 5.5.10 and Exercise 5.5.1.

If $\infty \in E$, then by Definition 6.2.6, $\sup(E) = \infty, \inf(E) = -\sup(-E)$. Then, if $-\infty \in E$, then $\infty \in -E$ hence $\inf(E) = -\infty$. 

Hence, a) is true by Definition 6.2.3.

For b), since $\infty \in E$, then $\infty \leq M$. Hence $\sup(E) = \infty \leq M$ as desired.

For c), note $-\infty \in E$, hence $-\infty \geq M$. Using similar reasoning $\inf(E) = -\infty \geq M$ as desired.

If $-\infty \notin E$, consider $\inf(E - \{\infty\})$. Since $E - \{\infty\} \subseteq \R$, it follows from Exercise 5.5.1 that $\inf(E - \{\infty\})$ is the greater lower bound of $E - \{\infty\}$. Note $\inf(E - \{\infty\}) \leq \infty$, and $\inf(E) = \inf(E - \{\infty\})$, claim a), c) follows.

Why $\inf(E) = \inf(E - \{\infty\})$?

Note $\inf(E) = -\sup(-E)$. Remains to show $\sup(-E) = \sup(-E - \{-\infty\})$. It follows from Definition 6.2.6 c) as desired.

$\infty \notin E$ case follows similarly.

### Exercise 6.3.1

For $\inf(a_n)^{\infty}_{n=m} = 0$. Note, by Proposition 6.2.5 b), we either have $\inf(a_n)^{\infty}_{n=m} < 0, \inf(a_n)^{\infty}_{n=m} = 0, \inf(a_n)^{\infty}_{n=m} > 0$.

If $\inf(a_n)^{\infty}_{n=m} < 0$, then note $0$ is a lower bound. (As $\forall n \geq 1, 1/n > 0$). Yet by 6.2.11 c) we have $\inf(a_n)^{\infty}_{n=m} \geq 0$, contradiction.

If $\inf(a_n)^{\infty}_{n=m} > 0$, then denote it as $\epsilon$. By Archimedes easy to verify we can find sufficiently large $N \in \Z^{+}$ s.t. $1/N < \epsilon$. Hence $\inf(a_n)^{\infty}_{n=m}$ is not a lower bound, contradicting Exercise 5.5.1.

Hence it must hold $\inf(a_n)^{\infty}_{n=m} = 0$.

For $\sup(a_n)^{\infty}_{n=m} = 1$, easy to verify $1$ is an upper bound. (As $\forall n \in Z^{+}, 1/n \leq 1$). Hence, remains to show it is the least upper bound by Definition 5.5.10. Assume $1$ is not least upper bound, then by Theorem 6.2.11 b), $1 > \sup(a_n)^{\infty}_{n=m}$. However since $1 = a_{1}$, $a_1 > \sup(a_n)^{\infty}_{n=m}$, contradicting Definition 5.5.10 as desired.

### Exercise 6.3.2

$\forall n \geq m, a_n \leq \sup(a_n)^{\infty}_{n=m}$ follows from 6.2.11 a) (via letting $E = (a_n)^{\infty}_{n=m}$)

$x \leq M$ for any upper bound $M$ follows from 6.2.11 b)

For third claim, we argue by contradiction. Assume $\exists y < x, \forall n \geq m, y \geq a_n$, then $y$ is a lower bound. Hence $y \geq x$ by 6.2.11 b). However, $y < x$, contradiction as desired.

### Exercise 6.3.3

Note for all $\epsilon > 0$, there exists $N \geq m$ s.t.:

$$\sup(a_n)^{\infty}_{n=m} - \epsilon \leq a_N \leq \sup(a_n)^{\infty}_{n=m} + \epsilon$$

The first inequality follows from 6.3.6 3rd claim as $\sup(a_n)^{\infty}_{n=m} - \epsilon < \sup(a_n)^{\infty}_{n=m}$. The second inequality follows from same claim as $a_n \leq \sup(a_n)^{\infty}_{n=m} \leq \sup(a_n)^{\infty}_{n=m} + \epsilon$.

Note for all $n \geq N$, $a_n \geq a_N$, hence:

$$\sup(a_n)^{\infty}_{n=m} - \epsilon \leq a_N \leq a_n \leq \sup(a_n)^{\infty}_{n=m} + \epsilon$$

Therefore, by Exercise 5.4.6, it holds that:

$$\forall \epsilon > 0, \exists N \geq m, \forall n \geq m, |a_n - \sup(a_n)^{\infty}_{n=m}| \leq \epsilon$$

As desired.

### Exercise 6.3.4

Explain: When $x > 1$, the sequence is no longer bounded above.

Show: Assume $\lim_{n\rightarrow\infty} x^n =L$. Then since $x > 1$, $1/x < 1$. Hence, $\lim_{n\rightarrow\infty} (1/x)^n = 0$.

However, $\lim_{n\rightarrow\infty} x^n(1/x)^n = 1$, yet $\lim_{n\rightarrow\infty}x^n \lim_{n\rightarrow\infty} (1/x)^n = L \times 0 = 0 \neq 1$, contradiction as desired.

Example 1.2.3 flaw: Change of variable (As in Exercise 6.1.4) applies only to convergent series. In fact Example 1.2.3 serves as a valid proof by contradiction for proving divergence of the series.

### Exercise 6.4.1

We have:

$$\forall \epsilon > 0, \exists M \geq m, \forall n \geq M, |a_n - L| \leq \epsilon$$

We need to show:

$$\forall \epsilon > 0, \forall N \geq m, \exists n \geq m, |a_n - L| \leq \epsilon$$

Fix $\epsilon$, we choose $n = \max(N, M)$, then $|a_n - L| \leq \epsilon$ as desired.

### Exercise 6.4.2

#### Limit Point

Exercise 6.1.3

Only if direction:

Recall definition of Limit Point, we have:

$$\forall \epsilon > 0, \forall N \geq m, \exists n \geq N, |a_n - x| \leq c$$

Note since $m' \geq m$, $\forall N \geq m$ implies $\forall N \geq m'$, hence:

$$\forall \epsilon > 0, \forall N \geq m', \exists n \geq N, |a_n - x| \leq c$$

Which, by definition of limit point implies $c$ is a limit point of $(a_n)^{\infty}_{n = m'}$, as desired.

If direction:

We have:

$$\forall \epsilon > 0, \forall N \geq m', \exists n \geq N, |a_n - x| \leq \epsilon \quad \text{(1)}$$

Hence, by instantiating $N = m'$:

$$\forall \epsilon > 0, \exists n' \geq m', |a_{n'} - x| \leq \epsilon \quad \text{(2)}$$

We need to show:

$$\forall \epsilon > 0, \forall N \geq m, \exists n \geq N, |a_n - x| \leq \epsilon \quad \text{(3)}$$

Fix $\epsilon$, we split $\forall N \geq m$ into cases, and show in each case there exists a permissible $n$.

For $m' > N$, we can merely choose $n = n'$ with $n'$ from (2) (using the same $\epsilon$ in (2)). We need to test $n' \geq N$ and $|a_{n'} - x| \leq \epsilon$. Since $n' \geq m'$ and $m' > M$, $n' \geq N$. By (2), $|a_{n'} - x| \leq \epsilon$. Hence $n'$ satisfies the conditions.

For $N \geq m'$, we can choose the same $n$ in (1). Easy to confirm the conditions are satisfied by such choice.

Hence, in both case $\exists n \geq N, |a_n - x| \leq \epsilon$, and the reasoning holds for any $\epsilon > 0$, as desired.

Exercise 6.1.4

Only if direction:

By Definition of Limit Point, we have:

$$\forall \epsilon > 0, \forall N' \geq m, \exists n' \geq N, |a_{n'} - x| \leq \epsilon \quad \text{(1)}$$

We need to show:

$$\forall \epsilon > 0, \forall N \geq m, \exists n \geq N, |a_{n + k} - x| \leq \epsilon \quad \text{(2)}$$

Fix $\epsilon, N$, we need to show a permissible $n$ exists via (1).

We instantiate (1) via setting $N' = N + k$, then $\exists n' > N, |a_{n'} - x| \leq \epsilon$. We claim $n = n' - k$ is permissible.

We first verify $n \geq N$. Note $n' \geq N + k$, hence $n' - k \geq N$. Therefore $n = n' - k \geq N$ as desired.

Then, $|a_{n + k} - x| = |a_{n'} - x| \leq \epsilon$, as desired.

If direction:

We have:

$$\forall \epsilon > 0, \forall N' \geq m + k, \exists n' \geq N', |a_{n'} - x| \leq \epsilon \quad \text{(1)}$$

We need to show:

$$\forall \epsilon > 0, \forall N \geq m, \exists n \geq N, |a_n - x| \leq \epsilon$$

Fix $\epsilon$. We split into case $N \geq m + k$ and $N < m + k$, and show in each case a permissible $n$ exists.

Case $N \geq m + k$ is shown by (1), by instantiating $N' = N$ and take $n'$ as $n$. Easy to verify it is permissible.

Remains to consider case $N < m + k$. In that case, note by instantiating $N' = m + k$ in (1), we deduce $\exists n' \geq m + k, |a_{n'} - x| \leq \epsilon$. We show $n'$ is permissible, as since $n' \geq m + k$ and $m + k > N$, it holds that $n' \geq N$. And, $|a_n - x| \leq \epsilon$, as desired.

#### $\lim\sup_{n\rightarrow\infty}$ case

Exercise 6.1.3

Need to show $\inf(\sup(a_n)^{\infty}_{n = N})^{\infty}_{N = m} = \inf(\sup(a_n)^{\infty}_{n = N})^{\infty}_{N = m'}$ for which $m' \geq m$.

We first show $\sup(a_n)^{\infty}_{n=N} \geq \sup(a_n)^{\infty}_{n = N + 1}$

First note by Proposition 6.3.6, $\forall n \geq N, \sup(a_n)^{\infty}_{n = N} \geq a_n$. Hence, $\forall n \geq N + 1, \sup(a_n)^{\infty}_{n = N} \geq a_n$. Therefore $\sup(a_n)^{\infty}_{n = N}$ is an upper bound for $(a_n)^{\infty}_{n = N + 1}$. Rest follows by Proposition 6.3.6 as desired.

Then we perform induction on $m'$. For ease of notation denote $I(m') = \inf(\sup(a_n)^{\infty}_{n = N})^{\infty}_{N = m'}, b_N = \sup(a_n)^{\infty}_{n=N}$. Note $b_N \geq b_{N+1}$. Hence, the inductive hypothesis can be expressed as $P(m'): I(m) = I(m')$.

Base case $P(m)$ is trivially true. Assume true for $P(m')$. By Proposition 6.3.6, we have $\forall N \geq m', I(m') \leq b_N$. Hence it holds that $\forall N \geq m' + 1, I(m') \leq b_N$. Hence $I(m')$ is a lower bound of $(b_N)^{\infty}_{N = m' + 1}$.

Similarly, $\forall N \geq m' + 1, I(m' + 1) \leq b_N$. And, noting $I(m'+1) \leq b_{m'+1} \leq b_{m'}$, we have $\forall N \geq m', I(m' + 1) \leq b_N$. Hence $I(m'+1)$ is lower bound of $(b_{N})^{\infty}_{N = m}$.

Therefore, by Proposition 6.3.6, we have $I(m') \geq I(m'+1), I(m'+1) \geq I(m')$. Hence $I(m') = I(m'+1)$. And, by inductive hypothesis $I(m'+1) = I(m') = I(m)$ as desired.

Exercise 6.1.4

We start with a Lemma:

$$\{\sup(a_n)^{\infty}_{n = N + k}: N \geq m\} = \{\sup(a_n)^{\infty}_{n = N'}: N' \geq m + k\}$$

Proof:

Say given $\sup(a_n)^\infty_{n=N+k}$ for some $N \geq m$, then $N + k \geq m + k$, hence letting $N' = n + k$, by Axiom of Substitution $\sup(a_n)^\infty_{n = N + k} = \sup(a_n)^\infty_{n = N'} \in RHS$ as desired.

Similarly, given $\sup(a_n)^{\infty}_{n = N'}$ for some $N' \geq m + k$, then $N' - k \geq m$. Hence letting $N = N' - k$, $\sup(a_n)^{\infty}_{n = N'} = \sup(a_n)^\infty_{n = N' - k + k} = \sup(a_n)^\infty_{N + k} \in LHS$ as desired.

Hence:

$$
\begin{align*}
\inf(\sup(a_n)^{\infty}_{n = N + k})^{\infty}_{N = m} &= \inf(\sup(a_n)^{\infty}_{n = N})^{\infty}_{N = m + k} &\quad \text{By Lemma} \\
&= \inf(\sup(a_n)^{\infty}_{n = N})^{\infty}_{N = m} &\quad \text{By Exercise 6.1.3}
\end{align*}
$$

As desired.

#### $\lim\inf_{n\rightarrow\infty}$ case

Similar to $\lim\sup_{n\rightarrow\infty}$ case hence omitted.

### Exercise 6.4.3

c)

We first show $\inf(a_n)^\infty_{n=m} \leq L^{-}$.

By definition of $L^{-}$ and $a_{N}^-$, above is equivalent to $\inf(a_n)^\infty_{n=m} \leq \sup(\inf(a_n)^\infty_{n = N})^\infty_{N=m}$.

Since $\inf(a_n)^{\infty}_{n = m} \in \{\inf(a_n)^{\infty}_{n = N} : N \geq m\}$ (can show via setting $N = m$ on the right side and result follows from Axiom of Substitution), by Proposition 6.3.6 we have $\inf(a_n)^\infty_{n=m} \leq \sup(\inf(a_n)^\infty_{n = N})^\infty_{N=m}$ as desired.

Can similarly show $L^{+} \leq \sup(a_n)^{\infty}_{n = m}$

Remains to show $L^{-} \leq L^{+}$. By definition of $L^{-}, L^{+}$, the inequality is equivalent to $\sup(a_N^-)^\infty_{N = m} \leq \inf(a_N^+)^\infty_{N = m}$. We argue by contradiction. Assume $\sup(a_N^-)^\infty_{N = m} > \inf(a_N^+)^\infty_{N = m}$, then, by Proposition 6.3.6:

$$\exists N_0 \geq m, \sup(a_N^-)^\infty_{N = m} \geq a_{N_0}^- > \inf(a_N^+)^\infty_{N=m}$$

Taking $a_{N_0}^- > \inf(a_N^+)^{\infty}_{N=m}$, we apply Proposition 6.3.6 again yielding:

$$\exists N_1 \geq m, a_{N_0}^- > a_{N_1}^+ \geq \inf(a_N^{+})^\infty_{N = m}$$

We claim $a_{N_0}^- > a_{N_1}^+$ is the desired contradiction. Let $M = \max(N_0, N_1)$, then by Proposition 6.3.6, $\sup(a_n)^\infty_{n = N_0} \geq a_M \geq \inf(a_n)^\infty_{n = N_1}$, hence $\sup(a_n)^\infty_{n = N_0} \geq \inf(a_n)^\infty_{n = N_1}$, contradicting $\inf(a_n)^\infty_{n = N_1} > \sup(a_n)^\infty_{n = N_0}$ as desired.

d)

We argue by contradiction. To show $L^- \leq c$ for any sequence, assume $L^- > c$ for some sequence $(a_n)^\infty_{n = m}$. Then, by Definition 6.4.6, we have $\sup(A_N^-)^\infty_{N = m} > c$. By Proposition 6.3.6, we have:

$$\exists N_0 \geq m, \sup(A_N^-)^\infty_{N = m} \geq A^-_{N_0} > c$$

Hence we have $A^-_{N_0} > c$ for some $N_0 \geq m$. By Definition 6.4.6, we have $\inf(a_n)^\infty_{n = N_0} > c$. Since by Proposition 6.3.6, we have $\forall n \geq N_0, a_n \geq \inf(a_n)^\infty_{n = N_0}$ and $\inf(a_n)^\infty_{n = N_0} > c$, we have $\forall n \geq N_0, a_n > c$.

Since $c$ is a limit point of $(a_n)^\infty_{n = m}$, by Definition 6.4.1, we have:

$$\forall \epsilon > 0, \forall N \geq m, \exists n \geq N, |a_n - c| \leq \epsilon$$

Set $\epsilon = (\inf(a_n)^\infty_{n = N_0} - c) / 2, N = N_0$, we have $\exists n \geq N_0, |a_n - c| \leq  (\inf(a_n)^\infty_{n = N_0} - c) / 2$, hence:

$$
\begin{align*}
a_n - c &\leq (\inf(a_n)^\infty_{n = N_0} - c) / 2 &\text{As } n \geq N_0 \Rightarrow a_n > c \\
a_n + a_n - c &\leq \inf(a_n)^\infty_{n = N_0} \\
a_n &< \inf(a_n)^\infty_{n = N_0} &\text{As } a_n > c
\end{align*}
$$

It was shown that $\forall n \geq N_0, a_n \geq \inf(a_n)^\infty_{n = N_0}$, since $n \geq N_0$, we have $a_n \geq \inf(a_n)^\infty_{n = N_0}$, contradicting $a_n < \inf(a_n)^\infty_{n = N_0}$ as desired.

e)

By Definition 6.4.1, Showing $L^-$ is a limit point is equivalent of showing:

$$\forall \epsilon > 0, \forall N \geq m, \exists n \geq N, |a_n - L^-| \leq \epsilon$$

Fix $\epsilon, N$. Then, by Definition 6.4.6, $L^- = \sup(a_{N'}^-)^\infty_{N' = m}$. By Exercise 6.4.2, it equals to $\sup(a^-_{N'})^\infty_{N' = N}$.

Hence, by Proposition 6.3.6:

$$
\begin{align*}
&\exists N_0 \geq N, L^- \geq a_{N_0}^- > L^- - \epsilon / 2 \\
&\exists N_0 \geq N, 0 \geq a_{N_0}^- - L^- > -\epsilon / 2 \\
&\exists N_0 \geq N, 0 \leq L^- - a_{N_0}^- < \epsilon / 2 \\
&\exists N_0 \geq N, |L^- - a_{N_0}^-| < \epsilon / 2
\end{align*}
$$

Then, by Proposition 6.3.6 again:

$$
\begin{align*}
&\exists n_0 \geq N_0, a_{N_0}^- \leq a_{n_0} < a_{N_0}^- + \epsilon / 2\\
&\exists n_0 \geq N_0, 0 \leq a_{n_0} - a_{N_0} < \epsilon / 2\\
&\exists n_0 \geq N_0, |a_{n_0} - a_{N_0}| < \epsilon / 2
\end{align*}
$$

We claim $n = n_0$ is permissible. First, $n_0 \geq N_0$, and $N_0 \geq N$, hence $n_0 \geq N$. Then:

$$
\begin{align*}
|a_{n_0} - L^-| &\leq |a_{n_0} - a_{N_0}^-| + |a_{N_0}^- - L^-| &\text{By Triangle Inequality} \\
&< \epsilon / 2 + \epsilon / 2\\
&= \epsilon
\end{align*}
$$

As desired.

f)

#### If $(a_n)^∞_{n=m}$ converges to $c$, then we must have $L^+ = L^− = c$

For simplicity we only show $L^+ = c$.

Since $(a_n)^∞_{n=m}$ converges to $c$, by Definition 6.1.5, we have:

$$\forall \epsilon > 0, \exists N_{\epsilon} > m, \forall n \geq N_{\epsilon}, |a_n - c| \leq \epsilon$$

By Exercise 5.4.6, the above is equivalent to:

$$\forall \epsilon > 0, \exists N_{\epsilon} > m, \forall n \geq N_{\epsilon}, c - \epsilon \leq a_n \leq c + \epsilon$$

Hence, taking the right side of the inequality:

$$\forall \epsilon > 0, \exists N_{\epsilon} > m, \forall n \geq N_{\epsilon}, a_n \leq c + \epsilon$$

Therefore, by Definition 5.5.1, $c + \epsilon$ is an upper bound for $(a_n)^\infty_{N_{\epsilon}}$. Hence, by Proposition 6.3.6, we have $\sup(a_n)^\infty_{n = N_{\epsilon}} \leq c + \epsilon$. Since, by Definition 6.4.6, $\sup(a_n)^\infty_{n = N_{\epsilon}} = a^+_{N_{\epsilon}}$, and $L^+ = \inf(a^+_{N})^\infty_{N = m}$, we have, by Proposition 6.3.6:

$$\forall \epsilon > 0, \exists N_{\epsilon} > m, L^+ = \inf(a^+_{N})^\infty_{N = m} \leq a^+_{N_{\epsilon}} \leq c + \epsilon$$

$$\forall \epsilon > 0, \exists N_{\epsilon} > m, L^+ \leq c + \epsilon$$

$$\forall \epsilon > 0, L^+ \leq c + \epsilon$$

We claim $L^+ \leq c$. We argue by contradiction. Assume $L^+ > c$, then choose $\epsilon = (L^+ - c)/2$, we deduce:

$$
\begin{align*}
L^- &\leq c + (L^- - c)/2 \\
2L^- &\leq 2c + L^- - c \\
L^- &\leq c
\end{align*}
$$

Which contradicts $L^+ > c$ as desired.

Then, we deduce $c \leq L^+$.

Similar to how we established $\sup(a_n)^\infty_{n = N_{\epsilon}} \leq c + \epsilon$, we have $c - \epsilon \leq \inf(a_n)^\infty_{n = N_\epsilon}$. Then, by Definition 6.4.2, $\inf(a_N^+)^\infty_{N = m} = \inf(a_N^+)^\infty_{N = N_{\epsilon}}$, hence $L^+ = \inf(a_N^+)^\infty_{N = N_{\epsilon}}$. Then, by Proposition 6.3.6, $\forall N \geq N_{\epsilon}, a_N \leq a^+_N$. Hence, by Lemma 6.4.13, $\inf(a_n)^\infty_{n = N_{\epsilon}} \leq \inf(a^+_N)^\infty_{N = N_{\epsilon}}$, therefore:

$$\forall \epsilon > 0, c - \epsilon \leq \inf(a_n)^\infty_{n = N_{\epsilon}} \leq \inf(a^+_N)^\infty_{N = N_{\epsilon}} = L^+$$

$$\forall \epsilon > 0, c - \epsilon \leq L^+$$

Using similar argument for showing $L^+ \leq c$, we can show above predicate implies $c \leq L^+$. Hence $c \leq L^+ \leq c$, implying $L^+ = c$ as desired

#### If $L^+ = L^- = c$, then $(a_n)^\infty_{n = m}$ converges to $c$

By Exercise 6.1.2, $(a_n)^\infty_{n = m}$ converges to $c$ iff:

$$\forall \epsilon > 0, \exists N \geq m, \forall n \geq N, |a_n - c| \leq \epsilon$$

By Exercise 5.4.6, above is true iff:

$$\forall \epsilon > 0, \exists N \geq m, \forall n \geq N, c - \epsilon \leq a_n \leq c + \epsilon$$

Fix $\epsilon$. Since $c + \epsilon = L^+ + \epsilon > L^+$, by Proposition 6.4.12 a):

$$\exists N_0 \geq m, \forall n \geq N_0, a_n < c + \epsilon$$

Similarly:

$$\exists N_1 \geq m, \forall n \geq N_1, c - \epsilon < a_n$$

Hence, we claim $N = \max(N_0, N_1)$ is permissible. Note $N \geq m$ as $N \geq N_0$ and $N_0 \geq m$. And, since $n \geq N$ implies $n \geq N_0$ and $n \geq N_1$:

$$\forall n \geq N, c - \epsilon < a_n < c + \epsilon$$

$$\forall n \geq N, c - \epsilon \leq a_n \leq c + \epsilon$$

As desired.

### Exercise 6.4.4

For $\sup(a_n)^\infty_{n = m} \leq \sup(b_n)^\infty_{n = m}$. We argue by contradiction. Assume $\sup(a_n)^\infty_{n = m} > \sup(b_n)^\infty_{n = m}$. Then by Proposition 6.3.4, $\exists n_0 > 0, \sup(a_n)^{\infty}_{n = m} \geq a_{n_0} > \sup(b_n)^\infty_{n=m}$. Hence we have $a_{n_0} > \sup(b_n)^\infty_{n = m}$. However, since $\forall n \geq m, a_n \leq b_n$, we have $a_{n_0} \leq b_{n_0}$. We also have $b_{n_0} \leq \sup(b_n)^\infty_{n = m}$ by Proposition 6.3.6. Hence we have $a_{n_0} \leq \sup(b_n)^\infty_{n = m}$, contradicting $a_{n_0} > \sup(b_n)^\infty_{n = m}$ as desired.

Similarly we can show $\inf(a_n)^\infty_{n = m} \leq \inf(b_n)^\infty_{n = m}$.

For $\lim\sup_{n\rightarrow\infty} a_n \leq \lim\sup_{n\rightarrow\infty} b_n$, by Definition 6.4.6 the inequality is equivalent to $\inf(a_N^+)^\infty_{n = m} \leq \inf(b_N^+)^{\infty}_{n=m}$. Note since $\forall n \geq m, a_n \leq b_n$, by 6.4.4 1) we have $\forall N \geq m$, $a_N^+ \leq b_N^+$. Hence by 6.4.4 2) we have $\inf(a_N^+)^\infty_{n = m} \leq \inf(b_N^+)^{\infty}_{n=m}$ as desired.

Similarly we can show $\lim\inf_{n\rightarrow\infty} a_n \leq \lim\inf_{n\rightarrow\infty} b_n$, as desired.

### Exercise 6.4.5

By Proposition 6.4.12 f), since $L = \lim_{n\rightarrow\infty}a_n, L = \lim\sup_{n\rightarrow\infty} a_n$. Similarly $L = \lim\sup_{n\rightarrow\infty} c_n$.

Since $a_n \leq b_n \leq c_n$, By Lemma 6.4.13 f), we have:

$$L = \lim\sup_{n\rightarrow\infty}a_n \leq \lim\sup_{n\rightarrow\infty} b_n \leq \lim\sup_{n\rightarrow\infty}c_n = L$$

$$\lim\sup_{n\rightarrow\infty} b_n= L$$

Similarly we can conclude $\lim\inf_{n\rightarrow\infty} b_n = L$. Hence by Lemma 6.4.13 f), $\lim_{n\rightarrow\infty}b_n = L$ as desired.

### Exercise 6.4.6

Let $a_n = 1 - 1/n, b_n = 1$. It is the desired example as $a_n < b_n$ and easy to verify $\lim\sup_{n\rightarrow\infty}a_n = \lim\sup_{n\rightarrow\infty}b_n = 1$. 

It does not contradict Lemma 6.4.13 as Lemma 6.4.13 only claims $\lim\sup_{n\rightarrow\infty}a_n \leq \lim\sup_{n\rightarrow\infty}b_n$, which still holds as $1 \leq 1$.

### Exercise 6.4.7

If direction:

Note $\lim_{n\rightarrow\infty} -|a_n| = \lim_{n\rightarrow\infty} |a_n| = 0$, and $-|a_n| \leq a_n \leq |a_n|$. By Corollary 6.4.14, $\lim_{n\rightarrow\infty} a_n = 0$ as desired.

Only if direction

Note $\min(-a_n, a_n) \leq |a_n| \leq \max(-a_n, a_n)$.

By 6.1.19 g) h), $\lim_{n\rightarrow\infty}\min(-a_n, a_n) = \lim_{n\rightarrow\infty}\max(-a_n, a_n) = 0$. Hence $\lim_{n\rightarrow\infty} a_n = 0$ by Corollary 6.4.14 as desired.

If $0$ is replaced with some other number (say $1$), clearly false. Note $\lim_{n\rightarrow\infty} -1 \neq \lim_{n\rightarrow\infty} |-1|$.

### Exercise 6.4.8

We proceed to prove by cases. Either $(a_n)^\infty_{n=m}$ have finite upper bound or $(a_n)^\infty_{n=m}$ does not have finite upper bound.

If $(a_n)^{\infty}_{n = m}$ has finite upper bound, then we show $\lim\sup_{n\rightarrow\infty} a_n$ is finite. Let $M$ be the finite upper bound of $(a_n)^\infty_{n=m}$. Define $(b_n)^{\infty}_{n=m}$ as constant sequence with each term being $M$. Hence, $\lim_{n\rightarrow\infty} b_n = M$. Therefore, by Proposition 6.4.12 f), $\lim\sup_{n\rightarrow\infty} b_n = M$. By definition of upper bound, it holds that $\forall n \geq m, a_n \leq b_n$. Hence, by Lemma 6.4.13, $\lim\sup_{n\rightarrow\infty} a_n \leq \lim\sup_{n\rightarrow\infty} b_n = M$. Hence $\lim\sup_{n\rightarrow\infty} a_n$ is finite.

Therefore, by Proposition 6.4.12 e), $\lim\sup_{n\rightarrow\infty} a_n$ is a limit point as under Definition 6.4.1. Hence, by Proposition 6.4.12 f), for all limit point $c$ as under Definition 6.4.1, $c \leq \lim\sup_{n\rightarrow\infty} a_n$. There does not exist other limit points as $(a_n)^\infty_{n = m}$ has finite upper bound, hence for all limit point $c$, $c \leq \lim\sup_{n\rightarrow\infty} a_n$ as desired.

If $(a_n)^{\infty}_{n = m}$ has no finite upper bound, then we show $\lim\sup_{n\rightarrow\infty} a_n = \infty$. By Definition 6.4.6, it is equivalent of showing $\lim\sup_{n\rightarrow\infty} a_n = \inf(a_N^+)^\infty_{N = m}$. We start by showing $\forall N \geq m, a_N^+ = \infty$.

By Definition 5.5.10, it is equivalent of showing $(a_n)^{\infty}_{n = N}$ has no finite upper bound for all $N \geq m$. We use induction. For base case $N = m$, $(a_n)^{\infty}_{n = N}$ has no finite upper bound due to the case we are under. For $P(N + 1)$, we prove by contraposition and show $\lnot P(N + 1) \Rightarrow \lnot P(N)$. Assume $P(N + 1)$ has upper bound $M$, then $\forall n \geq N + 1, a_n \leq M$. Since $M \leq \max(M, a_{N})$, we deduce $\forall n \geq N + 1, a_n \leq \max(M, a_{N})$. Note $a_{N} \leq \max(M, a_{N})$, hence $\forall n \geq N, a_n \leq \max(M, a_{N})$, therefore $\max(M, a_{N})$ is a finite upper bound for $(a_n)^\infty_{n = N}$, hence $\lnot P(N)$, as desired.

Alternative method of showing $(a_n)^{\infty}_{n = N}$ for all $N \geq m$ has no finite upper bound: We argue by contradiction. Assume for some $N \geq m$, $(a_n)^\infty_{n = N}$ has finite upper bound $M$, then by Lemma 5.1.14, $a_m, a_{m + 1}, ... a_{N}$ is bounded by some finite $M'$. Hence, $(a_n)^\infty_{n = m}$ is bounded by $\max(M, M')$, contradicting $(a_n)^\infty_{n = m}$ has no finite upper bound, as desired.

Since $\forall N \geq m, a_N^+ = \infty$, we deduce $\forall N \geq m, a_N^+ \geq \infty$. Hence $\infty$ is a lower bound for $a_N^+$. Since $\infty$ is a lower bound for $a_N^+$, it holds $\inf(a_N^+)^{\infty}_{N = m} \geq \infty$ by Proposition 6.2.11 c), hence $\inf(a_N^+)^{\infty}_{n = m} = \infty$, therefore $\lim\sup_{n\rightarrow\infty} a_n = \inf(a_N^+)^{\infty}_{n = m} = \infty$.

Since $\lim\sup_{n\rightarrow\infty} a_n = \infty$ and $\infty$ is a limit point, $\lim\sup_{n\rightarrow\infty} a_n $ is a limit point. Furthermore, for any given limit point $c \in \R^{*}$, it holds that $c \leq \infty = \lim\sup_{n\rightarrow\infty} a_n$ as desired.

### Exercise 6.4.9

Consider $1, -1, 0, 2, -2, 0, 3, -3, 0...$

TODO: prove it has exactly 3 limit points.

### Exercise 6.4.10

Since each $b_m$ is limit point of $(a_n)^\infty_{n = N}$, we have, for any $m \geq M$:

$$\forall \epsilon_0 > 0, \forall N_0 \geq N, \exists n_0 \geq N_0, |a_{n_0} - b_m| \leq \epsilon \quad \text{(1)}$$

Since $c$ is limit point of $b_n$, we also have:

$$\forall \epsilon_1 > 0, \forall M_0 \geq M, \exists m_0 \geq M_0, |b_{m_0} - c| \leq \epsilon \quad \text{(2)}$$

By Definition of limit point, showing $c$ is a limit point of $(a_n)^{\infty}_{n = N}$ is equivalent of showing:

$$\forall \epsilon > 0, \forall N' \geq N, \exists n \geq N', |a_n - c| \leq \epsilon \quad \text{(3)}$$

We fix $\epsilon, N'$. Then, we instantiate (2), setting $\epsilon_1  = \epsilon / 2, M_0 = M$, yielding:

$$\exists m_0 \geq M, |b_{m_0} - c| \leq \epsilon / 2 \quad \text{(4)}$$

Then, we instantiate (1), setting $m = m_0, \epsilon_0 = \epsilon/2, N_0 = N'$, then:

$$\exists n_0 \geq N', |a_{n_0} - b_{m_0}| \leq \epsilon/2 \quad \text{(5)}$$

We claim, in (3), setting $n = n_0$ is permissible. Note $n_0 \geq N'$, remains to check $|a_{n_0} - c| \leq \epsilon$.

$$
\begin{align*}
|a_{n_0} - c| &\leq |a_{n_0} - b_{m_0}| + |b_{m_0} - c| &\text{By Triangle Inequality} \\
              &\leq \epsilon / 2 + \epsilon / 2 &\text{By (4), (5)} \\
              &\leq \epsilon
\end{align*}
$$

As desired.

### Exercise 6.5.1

$$
\begin{align*}
\lim_{n\rightarrow\infty}(1/n)^q &= \lim_{n\rightarrow\infty} (1/n)^{a/b} \\
&= \lim_{n\rightarrow\infty} ((1/n)^{1/b})^a &\text{By Definition 5.6.7}\\
&= (\lim_{n\rightarrow\infty} (1/n)^{1/b})^a &\text{By Theorem 6.1.19 b) and Induction}\\
&= 0^a &\text{As } a > 0\\
&= 0
\end{align*}
$$

Remark: The fact that $a, b \in \Z^+$ is essential. Definition 6.5.7 only applies if $a \in \Z, b \in \Z^+$. Theorem 6.1.19 b) and induction applies only because $a \in \Z^+$. $0^a$ is well defined because $a > 0$ ($0^{-1}$ would be undefined).

### Exercise 6.5.2

#### $\lim_{n\rightarrow\infty} x^n = 0$ when $|x| < 1$

By Corollary 6.4.17, $\lim_{n\rightarrow\infty} x^n = 0$ iff $\lim_{n\rightarrow\infty} |x^n| = 0$. Hence:

$$
\begin{align*}
\lim_{n\rightarrow\infty} |x^n| &= \lim_{n\rightarrow\infty} |x|^n &\text{by 4.3.10 d)} \\
&= 0 &\text{by 6.3.10}
\end{align*}
$$

Remark: Proposition 4.3.10 d) can be used since $n \in \N$. If $n \in \R$ things are more tricky. Proposition 6.3.10 can be used as $0 < |x| < 1$. Note we may have $|x| = 0$, but in that case the limit is still trivially $0$, as desired.

#### $\lim_{n\rightarrow\infty} x^n = 1$ when $x = 1$

Since $x^n = 1^n = 1$, by Definition 6.1.5 it follows that $\lim_{n\rightarrow\infty} x^n = \lim_{n\rightarrow\infty} 1 = 1$ as desired.

#### $\lim_{n\rightarrow\infty} x^n$ diverges when $x = -1$ or when $|x| > 1$

When $x = -1$, then both $-1, 1$ are limit points (can show via Definition 6.4.1), hence by Proposition 6.4.12 d) it holds that $L^- \leq -1, L^+ \geq 1$, hence $L^- \neq L^+$, implying $\lim_{n\rightarrow\infty} x^n$ diverges by Proposition 6.4.12 f).

(Or we can manually evaluate $L^-, L^+$ and show they are not equal).

When $|x| > 1$, note similar reasoning for Exercise 6.3.4 still applies. Assume $\lim_{n\rightarrow\infty} x^n = L$, then $\lim_{n\rightarrow\infty} x^n \lim_{n\rightarrow\infty} (1/x)^n = 1$. However, since $|x| > 1$, $1/|x| < 1$, hence $|1/x| < 1$. Therefore by 6.5.2 a), $\lim_{n\rightarrow\infty} (1/x)^n = 0$, hence we have $L \times 0 = 1$, contradiction.

### Exercise 6.5.3

We argue by cases. Assume $x = 1$, then $x^{1/n} = 1$, hence $\lim_{n\rightarrow\infty} x^{1/n} = 1$ as desired.

Assume $x > 1$, then by Lemma 5.6.9 d), $x^{1/n} > 1^{1/n}$, hence $x^{1/n} > 1$. Hence, $1$ is a lower bound for $(x^{1/n})^\infty_{n = 1}$. Since $x > 1$, by Lemma 5.6.6 e), $x^{1/n}$ is a decreasing function of $n$. Hence, by Proposition 6.3.8, $(x^{1/n})^\infty_{n = 1}$ converges, and $\lim_{n\rightarrow\infty} x^{1/n} = \inf(x^{1/n}) ^\infty_{n = 1} \geq 1$.

We then show $\inf(x^{1/n})^{\infty}_{n = 1} > 1$ causes contradiction. Assume $\inf(x^{1/n})^\infty_{n = 1} = 1 + d$ for some $d \in \R^{+}$, then $\forall n \geq 1, (1 + d) \leq x^{1/n}$. By 4.3.12 c), $\forall n \geq 1, (1 + d)^n  \leq x$. Via Binomial Theorem, easy to show $(1 + d)^n \geq nd^2$. By Corollary 5.4.13, there exists $n' \in \Z^{+}$, $n' d^2 > x$. Hence $(1 + d)^{n'} \geq n'd^2 > x$, which is the desired contradiction.

Hence, $\lim_{n\rightarrow\infty} x^{1/n} = \inf(x^{1/n}) ^\infty_{n = 1} = 1$, as desired.

Case $0 < x < 1$ remains. Via similar application of Lemma 5.6.9 d), 5.6.6 e), Proposition 6.3.8, we can show $\lim_{n\rightarrow\infty} x^{1/n}$ exists. Then, by Theorem 6.1.19 b);

$$\lim_{n\rightarrow\infty} x^{1/n} \lim_{n\rightarrow\infty} (1/x)^{1/n} = \lim_{n\rightarrow\infty} x^{1/n} (1/x)^{1/n}$$

Easy to show $RHS = 1$. Then, since $0 < x < 1$, $1/x > 1$, hence $\lim_{n\rightarrow\infty} (1/x)^{1/n} = 1$, therefore we have $\lim_{n\rightarrow\infty} x^{1/n} \times 1 = 1$, hence $\lim_{n\rightarrow\infty} x^{1/n} = 1$ as desired.

Remark: The estimation $(1 + d)^n \geq nd^2$ cannot be proven easily by induction. However, one may still avoid usage of Binomial Theorem by using estimation $(1 + d)^n \geq 1 + dn$ instead. This estimation, also called Bernoulli's inequality can be easily proven with induction.

### Exercise 6.6.1

#### Show $(a_n)^\infty_{n=0}$ is subsequence of $(a_n)^\infty_{n = 0}$
Let $f: \N \rightarrow \N$ be $f(n) = n$. Then, $f$ is strictly increasing. Since $\forall n \in \N, a_n = a_{f(n)}$, $(a_n)^\infty_{n = 0}$ is a subsequence of $(a_n)^\infty_{n = 0}$ by Definition 6.6.1.

#### Show $(c_n)^\infty_{n = 0}$ is subsequence of $(a_n)^\infty_{n = 0}$

Since $(c_n)^\infty_{n = 0}$ is subsequence of $(b_n)^\infty_{n = 0}$, by Definition 6.6.1 there exists $g: \N \rightarrow \N$ s.t. $\forall n \in \N, c_n = b_{g(n)}$. Since $(b_n)^\infty_{n = 0}$ is subsequence of $(a_n)^\infty_{n = 0}$, by Definition 6.6.1 there exists $f: \N \rightarrow \N$ s.t. $\forall n \in \N, b_n = a_{f(n)}$.

We now claim $\forall n \in \N, c_n = a_{f(g(n))}$. Since $\forall n \in \N, b_n = a_{f(n)}$ and $g(n) \in \N$, it holds that $\forall n \in \N, b_{g(n)} = a_{f(g(n))}$. Since $\forall n \in \N, c_n = b_{g(n)}$, it holds that $\forall n \geq \N, c_n = a_{f(g(n))}$, as desired.

Then, note by Definition 3.3.10, $f \circ g: \N \rightarrow \N$. Hence $f \circ g$ satisfies the domain & range requirement by Definition 6.6.1. Remains to show $\forall n \in \N, f(g(n + 1)) \geq f(g(n))$. Since $g$ is strictly increasing, $g(n + 1) > g(n)$. Since $f$ is strictly increasing, easy to show via induction that $a \geq b \Rightarrow f(a) \geq f(b)$, hence $f(g(n + 1)) \geq f(g(n))$ as desired.

### Exercise 6.6.2

Consider $a: 1,2,1,2,1,2...$ and $b: 2,1,2,1,2,1$...

Note $b_n = a_{n+1}, a_{n} = b_{n + 1}$.

### Exercise 6.6.3

We define $f: \N \times \N \rightarrow \N$ as:

$$f(j, k) = \min\{n \in \N: |a_n| \geq j + 1; n > k\}$$

For which $\min(E)$ is implicitly defined as a natural number s.t.:

- $\min(E) \in E$
- $\forall e \in E, \min(E) \leq e$

We claim that if $E$ is a non-empty subset of $\N$, then:

- $\min(E)$ exists
- $\min(E)$ is unique.

For existence of $\min(E)$, we argue by contradiction. Assume $\min(E)$ does not exist for a set $E$. Then, we use strong induction: let $P(n)$ denote $n \notin E$. Then base case $P(0)$ is true. As, if $0 \in E$, $\forall e \in E, 0 \leq e$ (as $e \in E$ implies $e \in \N$), hence $\min(E) = 0$ is permissible, contradiction. 

For $P(n + 1)$, note $0, 1, 2, ..., n \notin E$ by inductive hypothesis. Hence, assume $n + 1 \in E$, then $\forall e \in E, n + 1 \leq e$ (otherwise $\exists e \in E, n + 1 > e$, hence $e \leq n$, contradicting $0, 1, 2,..., n \notin E$). Hence $\min(E) = n + 1$ is permissible, contradiction, thus closing the induction.

Since $E$ is a non-empty subset of $\N$, by Lemma 3.1.16 we can take $c \in E$, and since $E \subseteq \N$, it holds that $c \in \N$, Since $c \in \N$, $c \notin E$ by $P(c)$, contradiction as desired.

We proceed to show $f$ is well defined, which is equivalent to showing $\min\{n \in \N: |a_n| \geq j; n > k\}$ exists & is unique, which is equivalent to showing $\{n \in \N: |a_n| \geq j; n > k\}$ is subset of $\N$ & non-empty.

For $\{n \in \N: |a_n| \geq j; n > k\} \subseteq \N$, it follows from Axiom of specification. For $\{n \in \N: |a_n| \geq j + 1; n > k\} \neq \empty$. We argue by contradiction. Assume the contrary, then $\forall n > k, |a_n| < j + 1$. Yet, by Lemma 5.1.14, $\forall n \leq k, |a_n| \leq M$ for some finite $M$. Hence, $(a_n)^\infty_{n = 0}$ is bounded by $\max(M, j + 1)$, contradiction. Hence $f$ is a function.

We recursively define $n: \N \rightarrow \N$ as:

$$
\begin{align*}
n(0) &= \{n \in \N: |a_n| \geq 0\} \\
n(j + 1) &= f(j, n(j))
\end{align*}
$$

(This does uniquely define a function by Exercise 3.5.12)

Then, easy to verify $n(j + 1) > n(j)$. Hence, by Definition 6.6.1 we can define subsequence $(b_j)^\infty_{j = 0}$ of $(a_n)^\infty_{n = 0}$ via:

$$b_j = a_{f(j)}$$

We claim $(b_j)^\infty_{j = 0}$ is the desired subsequence, aka:

$$\lim_{j\rightarrow\infty} \frac{1}{b_j} = 0$$

By definition of $f(j)$, it holds that $|a_{f(j)}| \geq j + 1$, hence:

$$
\begin{align*}
\lim_{j\rightarrow\infty} |\frac{1}{b_j}| &= \lim_{n\rightarrow\infty} |\frac{1}{a_{f(j)}}| \\
&\leq \lim_{j\rightarrow\infty} \frac{1}{j + 1} &\text{By 6.4.14} \\
&= \lim_{j\rightarrow\infty} \frac{1}{j} &\text{By 6.1.4} \\
&= 0
\end{align*}
$$

Hence, by Corollary 6.4.17, $\lim_{j\rightarrow\infty} 1/b_j = 0$, as desired.

### Exercise 6.6.4

#### (b) implies (a)

By Lemma 6.6.4, $(a_n)^\infty_{n = 0}$ is a subsequence of $(a_n)^\infty_{n = 0}$. Hence, every subsequence of $(a_n)^\infty_{n = 0}$ converges to $L$ implies $(a_n)^\infty_{n = 0}$ converges to $L$.

#### (a) implies (b)

Since $(a_n)^\infty_{n = 0}$ converges to $L$, by Definition 6.1.5:

$$\forall \epsilon' > 0, \exists N' \geq 0, \forall n' \geq N', |a_{n'} - L| \leq \epsilon \quad \text{(1)}$$

Denote a subsequence of $(a_n)^\infty_{n = 0}$ as $(b_n)^\infty_{n = 0}$ s.t. $\forall n \geq 0, b_n = a_{f(n)}$ for some strictly increasing function $f: \N \rightarrow \N$. We need to show $(b_n)^\infty_{n = 0}$ converges to $L$, which, By Definition 6.1.5, is equivalent to:

$$\forall \epsilon > 0, \exists N \geq 0, \forall n \geq N, |b_n - L| \leq \epsilon \quad \text{(2)}$$

Since $\forall n \geq 0, b_{n} = a_{f(n)}$, and $n \geq N \geq 0$ in (2), we conclude $|b_n - L| \leq \epsilon$ iff $|a_{f(n)} - L| \leq \epsilon$, hence (2) is equivalent to:

$$\forall \epsilon > 0, \exists N \geq 0, \forall n \geq N, |a_{f(n)} - L| \leq \epsilon \quad \text{(3)}$$

Fix $\epsilon$, then by instantiating $(1)$ with $\epsilon' = \epsilon$, we deduce:

$$\exists N' \geq 0, \forall n' \geq N', |a_{n'} - L| \leq \epsilon \quad \text{(4)}$$

Then, we claim $\exists N'' \in \N, f(N'') > N'$. We argue by contradiction. Assume $\forall N \in \N, f(N) \leq N'$. Then, define $(c_N)^\infty_{N = 0}$ s.t. $\forall N \in \N, c_N = N' - f(n)$. Then, since $\forall N \in \N, f(N) < f(N + 1)$, $\forall N \in \N, c_N > c_{N + 1}$. Yet, $\forall N \in \N, c_N \in \N$. Thus contradiction by Exercise 4.4.2 (a).

We claim (3) is true, as $N = N''$ is permissible. Easy to verify $N'' \geq 0$. Remains to show $\forall n \geq N'', |a_{f(n)} - L| \leq \epsilon$. Since $f$ is strictly increasing, via easy induction $\forall n \geq N'', f(n) \geq f(N'')$. Since $f(N'') > N'$, $\forall n \geq N'', f(n) > N'$. Therefore by (4), $|a_{f(n)} - L| \leq \epsilon$ as desired.

### Exercise 6.6.5

#### (a) implies (b)
We borrow definition of $\min$ from Exercise 6.6.3

Then, we define $n: \N \rightarrow \N$ via:

$$
\begin{align*}
n(0) &= 0 \\
n(j + 1) &= f(j, n(j)) \\
\end{align*}
$$

For which $f: \N \times \N \rightarrow \N$ is defined as:

$$f(j, k) = \min\{n > k : |a_n − L| ≤ \frac{1}{j + 1}\}$$

Similar to Exercise 6.6.3 solution, to ensure that $n: \N \rightarrow \N$ is well defined, we merely need to show $\{n > k : |a_n − L| ≤ \frac{1}{j + 1}\}$ is non-empty.

Since $(a_n)^\infty_{n = 0}$ has limit point $L$, by Definition 6.4.1 it holds that:

$$\forall \epsilon > 0, \forall N \geq 0, \exists n \geq N, |a_n - L| \leq \epsilon$$

Instantiate the above with $\epsilon = 1/{j + 1}, N = k + 1$ yields:

$$\exists n \geq k + 1, |a_n - L| \leq \frac{1}{j + 1}$$

$$\exists n > k, |a_n - L| \leq \frac{1}{j + 1}$$

Hence $\{n > k : |a_n − L| ≤ \frac{1}{j + 1}\}$ is non-empty.

Easy to verify $n(j+1) > n(j)$, hence by Definition 6.6.1, we can define subsequence $(b_j)^\infty_{j = 0}$ of $(a_n)^\infty_{n = 0}$ via:

$$b_j = a_{f(j)}$$

We claim $(b_j)^\infty_{j = 0}$ is the desired subsequence, aka $(b_j)^\infty_{j = 0}$ converges to $L$. By Definition 6.1.5, it is equivalent to showing:

$$\forall \epsilon > 0, \exists N \geq 0, \forall n \geq N, |b_n - L| \leq \epsilon \quad \text{(1)}$$

Observe, $|a_{f(n)} - L| \leq 1/n$. Hence, $|b_n - L| \leq 1/n$. Fixing $\epsilon$, we can choose $N$ s.t. $1/N \leq \epsilon$. Such $N$ exists as by Corollary 5.4.13, $\exists N \in \Z^{+}, N \epsilon \geq 1$. Divide $\epsilon$ by both sides yields $1/N \leq \epsilon$. (Or we can note $1/N \leq \epsilon \Leftrightarrow 1/\epsilon \leq N$ and use Proposition 5.4.12).

We claim the same $N$ is permissible for (1), as, for all $n \geq N$:

$$
\begin{align*}
|b_n - L| &\leq 1/n \\
          &\leq 1/N &\text{As } n \geq N \\
          &\leq \epsilon
\end{align*}
$$

As desired.

#### (b) implies (a)

We prove a stronger statement. Call the subsequence $(b_n)^\infty_{n = 0}$, for which $\forall n \in \N, b_n = a_{f(n)}$ for a strictly increasing function $f: \N \rightarrow \N$. Say $L$ is a limit point of $(b_n)^\infty_{n = 0}$, then, by Definition 6.4.1:

$$\forall \epsilon' > 0, \forall N' \geq 0, \exists n' \geq N', |b_{n'} - L| \leq \epsilon' \quad \text{(1)}$$

We want to show $(a_n)^\infty_{n = 0}$ has limit point $L$, which, by Definition 6.4.1, is equivalent to:

$$\forall \epsilon > 0, \forall N \geq 0, \exists n \geq N, |a_n - L| \leq \epsilon \quad \text{(2)}$$

Fix $\epsilon, N$. By solution of Exercise 6.6.4, $\exists N_0 \in \N, f(N_0) \geq N$. We instantiate (1) with $\epsilon' = \epsilon, N' = N_0$, then:

$$\exists n' \geq N_0, |b_{n'} - L| \leq \epsilon$$
$$\exists n' \geq N_0, |a_{f(n')} - L| \leq \epsilon$$

Then, $n = f(n')$ is permissible, as $f(n') \geq f(N_0) \geq N$ and $|a_{f(n')} - L| \leq \epsilon$, as desired.
