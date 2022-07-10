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

Easy to verify that the above function has the desired domain & range $\{n \in \N, n \leq N++\} \rightarrow N$. We remains to show that the function satisfies the desired properties, aka:

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
