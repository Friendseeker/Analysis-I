# List of Axioms & Lemmas

Note: Tao implicitly use zeroth-order and first-order logic throughout chapter 2
& 3. Hence, zeroth-order and first-order logic Axioms belongs to the list.

## Main Text

### Axiom 2.1

$0$ is a natural number.

### Axiom 2.2

If $n$ is a natural number, then $n++$ is also a natural number.

### Definition 2.1.3

We define $1$ to be the number $0++$, $2$ to be the number $(0++)++$, $3$ to be the number
$((0++)++)++$, etc. (In other words,$1:=0++$,$2:=1++$,$3:=2++$,etc. In this text I
use $x:=y$ to denote the statement that $x$ is defined to equal $y$.)

### Axiom 2.3

0 is not the successor of any natural number; i.e., we have n++ ̸= 0 for every
natural number n.

### Axiom 2.4

Different natural numbers must have different successors; i.e., if n, m are
natural numbers and n ̸= m, then n++ ̸= m++. Equivalently, if n++ = m++, then we
must have n = m.

### Axiom 2.5 (Principle of mathematical induction)

Let P(n) be any property pertaining to a natural number n. Suppose that P(0) is
true, and suppose that whenever P(n) is true, P(n++) is also true. Then P(n) is
true for every natural number n.

### Proposition 2.1.16 (Recursive Definitions)

Suppose for each natural number n, we have some function fn : N → N from the
natural numbers to the natural numbers. Let c be a natural number. Then we can
assign a unique natural number an to each natural number n, such that a0 = c and
an++ = fn(an) for each natural number n.

### Definition 2.2.1 (Addition of natural numbers)

Let m be a natural number. To add zero to m, we define 0 + m := m. Now suppose
inductively that we have defined how to add n to m. Then we can add n++ to m by
defining (n++) + m := (n + m)++. (aka g(0, m) = m. g(n++, m) = g(n, m)++)

### Lemma 2.2.2

For any natural number n, n + 0 = n. (aka g(n, 0) = n).

### Lemma 2.2.3

For any natural numbers n and m, n + (m++) = (n + m)++. (aka g(n, m++) = g(n,
m)++)

### Proposition 2.2.4 (Addition is commutative)

For any natural numbers n and m, n+m=m+n.

### Proposition 2.2.5 (Addition is associative)

For any natural numbers a,b,c, we have (a+b)+c=a+(b+c).

### Proposition 2.2.6 (Cancellation law)

Let a,b,c be natural numbers such that a+b=a+c. Then we have b=c.

### Proposition 2.2.6’ (Converse of Cancellation law)

Let a, b, c be natural numbers such that b = c. Then we have a + b = a + c for
arbitrary natural number a.

### Definition 2.2.7 (Positive natural numbers)

A natural number n is said to be positive iff it is not equal to 0. (“iff” is
shorthand for “if and only if” - see Section A.1).

### Proposition 2.2.8

If a is positive and b is a natural number, then a+b is positive (and hence b +
a is also, by Proposition 2.2.4).

### Corollary 2.2.9

If a and b are natural numbers such that a + b = 0, then a=0 and b=0.

### Lemma 2.2.10

Let a be a positive number. Then there exists exactly one natural number b such
that b++ = a.

### Definition 2.2.11 (Ordering of the natural numbers)

Let n and m be natural numbers. We say that n is greater than or equal to m, and
write n ≥ m or m ≤ n, iff we have n = m + a for some natural number a. We say
that n is strictly greater than m, and write n > m or m < n, iff n ≥ m and n ̸=
m.

### Proposition 2.2.12 (Basic properties of order for natural numbers).

Let a, b, c be natural numbers. Then

- a. (Order is reflexive) a ≥ a.
- b. (Order is transitive) If a≥b and b≥c, then a≥c.
- c. (Order is anti-symmetric) If a ≥ b and b ≥ a, then a = b.
- d. (Addition preserves order) a≥b if and only if a+c≥b+c.
  - Easy to prove that $a>b$ iff $a+c>b+c$ too
- e. a<b if and only if a++≤b.
- f. a<b if and only if b=a+d for some positive number d.

### Proposition 2.2.13 (Trichotomy of order for natural numbers)

Let a and b be natural numbers. Then exactly one of the following statements is
true: a<b, a=b, or a>b.

### Proposition 2.2.14 (Strong principle of induction)

Let m0 be a natural number, and let P (m) be a property pertaining to an
arbitrary natural number m. Suppose that for each m ≥ m0, we have the following
implication: if P(m′) is true for all natural numbers m0 ≤ m′ < m, then P(m) is
also true. (In particular, this means that P(m0) is true, since in this case the
hypothesis is vacuous.) Then we can conclude that P (m) is true for all natural
numbers m ≥ m0.

### Exercise 2.2.6

Let n be a natural number, and let P(m) be a property pertaining to the natural
numbers such that whenever P (m++) is true, then P (m) is true. Suppose that
P(n) is also true. Prove that P(m) is true for all natural numbers m ≤ n; this
is known as the principle of backwards induction. (Hint: apply induction to the
variable n.)

### Definition 2.3.1 (Multiplication of natural numbers)

Let m be a natural number. To multiply zero to m, we define 0×m := 0. Now
suppose inductively that we have defined how to multiply n to m. Then we can
multiply n++ to m by defining (n++) × m := (n × m) + m.

### Lemma 2.3.2 (Multiplication is commutative)

Let n,m be natural numbers. Then n×m=m×n.

### Lemma 2.3.2'

m x 0 = 0

### Lemma 2.3.2’’

m x (n++) = m \* n + m

### Lemma 2.3.3 (Positive natural numbers have no zero divisors)

Let n,m be natural numbers. Then n × m = 0 if and only if at least one of n, m
is equal to zero. In particular, if n and m are both positive, then nm is also
positive.

### Proposition 2.3.4 (Distributive law). For any natural numbers a, b, c,

we have a(b+c)=ab+ac and (b+c)a=ba+ca.

### Proposition 2.3.5 (Multiplication is associative)

For any natural numbers a,b,c, we have (a×b)×c=a×(b×c).

### Proposition 2.3.6 (Multiplication preserves order)

If a, b are natural numbers such that a < b, and c is positive, then ac < bc.

### Proposition 2.3.9 (Euclidean algorithm)

Let n be a natural number, and let q be a positive number. Then there exist
natural numbers m, r such that 0 ≤ r < q and n = mq + r.

### Definition 2.3.11 (Exponentiation for natural numbers)

Let m be a natural number. To raise m to the power 0, we define $m^0 = 1$; in
particular, we define $0^0 = 1$. Now suppose recursively that mn has been
defined for some natural number n, then we define $m^n++ = m^n × m$.

### Exercise 2.3.4

$(a + b)^2 = a^2 + 2ab + b^2$ for all natural numbers $a, b$.

### Definition 3.1.1

(Informal) We define a set $A$ to be any unordered collection of objects, e.g.,
$\{3,8,5,2\}$ is a set. If $x$ is an object, we say that $x$ is an element of
$A$ or $x \in A$ if $x$ lies in the collection; otherwise we say that
$x \notin A$. For instance, $3 \in \{1,2,3,4,5\}$ but $7 \notin \{1,2,3,4,5\}$.

### Axiom 3.1 (Sets are objects)

If $A$ is a set, then $A$ is also an object. In particular, given two sets $A$
and $B$, it is meaningful to ask whether $A$ is also an element of $B$.

### Definition 3.1.4 (Equality of sets)

Two sets $A$ and $B$ are equal, $A = B$, iff every element of $A$ is an element
of $B$ and vice versa. To put it another way, $A = B$ if and only if every
element $x$ of $A$ belongs also to $B$, and every element $y$ of $B$ belongs
also to $A$. Aka $\forall x, x \in A \leftrightarrow x \in B$

### Axiom 3.2 (Empty set)

There exists a set $\empty$, known as the empty set, which contains no elements,
i.e., for every object $x$ we have $x \notin \empty$.

### Lemma 3.1.6 (Single choice)

Let $A$ be a non-empty set. Then there exists an object $x$ such that $x \in A$.

### Axiom 3.3 (Singleton sets and pair sets)

If $a$ is an object, then there exists a set $\{a\}$ whose only element is $a$,
i.e., for every object $y$, we have $y \in \{a\}$ if and only if $y=a$ We refer
to $\{a\}$ as the singleton set whose element is $a$. Furthermore, if $a$ and
$b$ are objects, then there exists a set $\{a, b\}$ whose only elements are $a$
and $b$. i.e., for every object $y$, we have $y ∈ \{a, b\}$ if and only if
$y = a$ or $y = b$; we refer to this set as the pair set formed by $a$ and $b$.

### Axiom 3.4 (Pairwise union)

Given any two sets $A, B$, there exists a set $A \cup B$, called the union
$A \cup B$ of $A$ and $B$, whose elements consists of all the elements which
belong to $A$ or $B$ or both. In other words, for any object $x$,
$x \in A \cup B \Leftrightarrow (x\in A \lor x\in B)$.

### Lemma 3.1.13

If $a$ and $b$ are objects, then $\{a, b\} = \{a\} ∪ \{b\}$. If $A, B, C$ are
sets, then the union operation is commutative (i.e., $A \cup B = B\cup A$) and
associative (i.e., $(A∪B)∪C = A∪(B∪C)$). Also, we have
$A ∪ A = A ∪ \empty = \empty ∪ A = A$.

### Definition 3.1.15 (Subsets)

Let $A,B$ be sets. We say that $A$ is a subset of $B$, denoted $A ⊆ B$, iff
every element of $A$ is also an element of $B$, i.e. For any object
$x, x ∈ A \rightarrow x ∈ B$. We say that $A$ is a proper subset of $B$, denoted
$A \subsetneq B$, if $A ⊆ B$ and $A \neq B$.

### Remark 3.1.16

Because these definitions involve only the notions of equality and the “is an
element of” relation, both of which already obey the axiom of substitution, the
notion of subset also automatically obeys the axiom of substitution. Thus for
instance if $A ⊆ B$ and $A = A'$, then $A' ⊆ B$.

### Proposition 3.1.18 (Sets are partially ordered by set inclusion)

Let $A,B,C$ be sets. If $A⊆B$ and $B⊆C$ then $A⊆C$. If $A⊆B$ and $B ⊆ A$, then
$A = B$. Finally, if $A \subsetneq B$ and $B \subsetneq C$ then
$A \subsetneq C$.

### Axiom 3.5 (Axiom of specification)

Let $A$ be a set, and for each $x ∈ A$, let $P(x)$ be a property pertaining to
$x$ (i.e., $P(x)$ is either a true statement or a false statement). Then there
exists a set, called $\{x ∈ A : P(x) \; \text{is true}\}$ (or simply
$\{x ∈ A : P(x)\}$ for short), whose elements are precisely the elements $x$ in
$A$ for which $P(x)$ is true. In other words, for any object $y$,
$y∈\{x∈A:P(x) \; \text{is true}\} \Leftrightarrow (y∈A \land P(y)\; \text{is true})$.

### Definition 3.1.23 (Intersections)

The intersection $S_1 ∩ S_2$ of two sets is defined to be the set
$$S_1 ∩S_2 := \{x∈S_1 :x∈S_2\} $$

In other words, $S_1 ∩ S_2$ consists of all the elements which belong to both
$S_1$ and $S_2$. Thus, for all objects $x$:

$$x∈S_1∩S_2 \Leftrightarrow x∈S_1 \land x∈S_2$$

### Definition 3.1.27 (Difference sets)

Given two sets $A$ and $B$, we define the set $A−B$ or $A \backslash B$ to be
the set $A$ with any elements of $B$ removed:

$$A \backslash B := \{x ∈ A : x \notin B\}$$

for instance, $\{1, 2, 3, 4\}\backslash \{2, 4, 6\} = \{1, 3\}$. In many cases
$B$ will be a subset of $A$, but not necessarily.

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
  $a ∩ (x\backslash a) = ∅$
- (h) (de Morgan laws) we have
  $X\backslash(A ∪ B) = (X\backslash A) ∩ (X\backslash B)$ and
  $x\backslash (A ∩ B) = (X\backslash A) ∪ (X\backslash B)$.

### Axiom 3.6 (Replacement)

Let $A$ be a set. For any object $x \in A$, and any object $y$, suppose we have
a statement $P(x,y)$ pertaining to $x$ and $y$, such that for each $x \in A$
there is at most one $y$ for which $P(x,y)$ is true. Then there exists a set
$\{y: P(x,y) \; \text{is true for some} \; x\in A\}$, such that for any object
$z$,

$$z \in \{y: P(x,y) \; \text{is true for some} \; x\in A\} \Leftrightarrow P(x,z) \; \text{is true for some} \; x\in A$$

### Axiom 3.7 (Infinity)

There exists a set $\N$, whose elements are called natural numbers, as well as
an object $0$ in $\N$, and an object $n++$ assigned to every natural number
$n ∈ \N$, such that the Peano axioms (Axioms 2.1 - 2.5) hold.

### Axiom 3.8 (Universal specification) (Dangerous!)

Suppose for every object $x$ we have a property $P(x)$ pertaining to $x$ (so
that for every $x$, $P(x)$ is either a true statement or a false statement).
Then there exists a set $\{x : P (x)\}$ such that for every object $y$,

$$y∈\{x:P(x)\} \Leftrightarrow P(y)$$

### Axiom 3.9 (Regularity)

If $A$ is a non-empty set, then there is at least one element $x$ of $A$ which
is either not a set, or is disjoint from $A$.

- Two sets $A, B$ are disjoint if $A \cap B = \empty$

### Definition 3.3.1 (Functions)

Let $X,Y$ be sets, and let $P(x,y)$ be a property pertaining to an object
$x ∈ X$ and an object $y ∈ Y$ , such that for every $x ∈ X$, there is exactly
one $y ∈ Y$ for which $P(x,y)$ is true (this is sometimes known as the vertical
line test). Then we define the function $f : X → Y$ defined by $P$ on the domain
$X$ and range $Y$ to be the object which, given any input $x ∈ X$, assigns an
output $f(x) ∈ Y$ , defined to be the unique object $f(x)$ for which $P(x,f(x))$
is true. Thus, for any $x ∈ X$ and $y ∈ Y$ , $$y=f(x) \Leftrightarrow P(x,y)$$

- Functions obey Axiom of substitution
- Different input can generate same output (e.g. constant function)
- Empty function is defined as $f: \empty \rightarrow Y$

Note: The definition postulates that a function object exists. Exercise 3.5.10 offers a way to construct functions in ZFC (aka remove the postulation).

### Definition 3.3.7 (Equality of functions)

Two functions $f : X → Y , g:X→Y$ with the same domain and range are said to be
equal, $f=g$, if and only if $f(x) = g(x)$ for all $x ∈ X$. (If $f(x)$ and
$g(x)$ agree for some values of $x$, but not others, then we do not consider $f$
and $g$ to be equal.)

### Definition 3.3.10 (Composition)

Let $f : X → Y, g : Y → Z$ be two functions, such that the range of $f$ is the
same set as the domain of $g$. We then define the composition
$g \circ f : X → Z$ of the two functions $g, f$ to be the function defined
explicitly by the formula $$(g \circ f)(x) := g(f(x))$$ If the range of $f$ does
not match the domain of $g$, we leave the composition $g \circ f$ undefined.

Remark:

- Exercise 3.3.4 has handy cancellation law for composition

### Lemma 3.3.12 (Composition is associative)

Let $f : Z → W,  g : Y → Z, h:X→Y$ be functions. Then
$f\circ(g\circ h)=(f\circ g)\circ h$.

### Definition 3.3.14 (One-to-one functions)

A function $f$ is one-to-one (or injective) if different elements map to
different elements: $$x \neq x' \rightarrow f(x) \neq f(x')$$ Equivalently, a
function is one-to-one if $$f(x) = f(x') \rightarrow x = x'$$

### Definition 3.3.17 (Onto functions)

A function $f$ is onto (or surjective) if $f(X) = Y$ , i.e., every element in
$Y$ comes from applying $f$ to some element in $X$:
$$\forall y \in Y, \exists x \in X, f(x)=y$$

- Note: a function can be neither injective nor surjective.

### Definition 3.3.20 (Bijective functions)

Functions $f : X → Y$ which are both one-to-one and onto are also called
bijective or invertible.

Aka:

If $f$ is bijective, then for every $y ∈ Y$ , there is exactly one $x$ such that
$f(x) = y$ (there is at least one because of surjectivity, and at most one
because of injectivity).

- A bijective function $f$ has an inverse $f^{-1}$

Rigorous definition:

$$\forall y \in Y, \forall x \in X, f^{-1}(y) = x \Leftrightarrow f(x) = y$$

Remark:

Exercise 3.3.6 has shown:

- Invertibility (existence of inverse function)= bijectivity
- $f^{-1}$ must be bijective

### Definition 3.4.1 (Images of sets)

If $f : X → Y$ is a function from $X$ to $Y$ , and $S$ is a set in $X$, we
define $f(S)$ to be the set $$f(S) := \{f(x) : x ∈ S\}$$ this set is a subset of
$Y$ , and is sometimes called the image of $S$ under the map $f$. We sometimes
call $f(S)$ the forward image of $S$ to distinguish it from the concept of the
inverse image $f^{-1}(S)$ of S, which is defined below.

### Definition 3.4.4 (Inverse images)

If $U$ is a subset of $Y$ , we define the set $f^{-1}(U)$ to be the set:

$$f^{-1}(U):=\{x∈X :f(x)∈U\}$$

In other words, $f^{−1}(U)$ consists of all the elements of $X$ which map into
$U$.

$$f(x)∈U \Leftrightarrow x∈f^{-1}(U)$$

We call $f^{-1}(U)$ the inverse image of $U$.

### Axiom 3.10 (Power set axiom)

Let $X, Y$ be sets. Then there exists a set, denoted $Y^X$ , which consists of
all the functions from $X$ to $Y$ , thus
$$f ∈Y^X \Leftrightarrow (f \; \text{is a function with domain} \; X \; \text{and range} \; Y)$$

### Lemma 3.4.9

Let $X$ be a set. Then the set $\{Y : Y \; \text{is a subset of} \; X\}$ is a
set.

### Axiom 3.11 (Union)

Let $A$ be a set, all of whose elements are themselves sets. Then there exists a
set $\bigcup A$ whose elements are precisely those objects which are elements of
the elements of $A$, thus for all objects $x$:

$$x \in \bigcup A \Leftrightarrow (x \in S \text{ for some } S \in A)$$

### Index set, label, and family of sets

By Applying Axiom of replacement to a given set $A$. we can construct a new set such that $a \in A$ is replaced with set $A_{a}$. $A$ is called index set, with $a$ being called as labels. The set of $A_{a}$ are called a family of sets.

We can then perform union on family of sets by Axiom of union, or intersection by Axiom of specification.

- Note: the above construction requires the index set to be non-empty, which cannot be overlooked.

### Definition 3.5.1 (Ordered pair)

If $x$ and $y$ are any objects (possibly equal), we define the ordered pair $(x,y)$ to be a new object, consisting of $x$ as its first component and $y$ as its second component. Two ordered pairs $(x,y)$ and $(x',y')$ are considered equal if and only if both their components match, i.e.
$$(x,y) = (x',y') \Leftrightarrow (x = x' \land y = y')$$

### Definition 3.5.4 (Cartesian product)

 If $X$ and $Y$ are sets, then we define the Cartesian product $X × Y$ to be the collection of ordered pairs, whose first component lies in $X$ and second component lies in $Y$ , thus
$$X×Y =\{(x,y):x∈X,y∈Y\}$$
or equivalently
$$a∈(X×Y) ⇐⇒ (a=(x,y) \text{ for some }x∈X \text{ and }y∈Y)$$

### Definition 3.5.7 (Ordered n-tuple and n-fold Cartesian product)

Let $n$ be a natural number. An ordered $n$-tuple $(x_i)_{1≤i≤n}$ (also denoted $(x_1,...,x_n)$) is a collection of objects $x_i$, one for every natural number $i$ between $1$ and $n$; we refer to $x_i$ as the $i_{th}$ component of the ordered $n$-tuple. Two ordered $n$-tuples $(x_i)_{1≤i≤n}$ and $(y_i)_{1≤i≤n}$ are said to be equal iff $x_i = y_i$ for all $1 ≤ i ≤ n$. If $(X_i)_{1≤i≤n}$ is an ordered $n$-tuple of sets, we define their Cartesian product $\prod_{1≤i≤n}X_i$ ) (also denoted as $X_1 \times ... \times X_n$) by:

$$\prod_{1≤i≤n}X_i = \{(x_i)_{1≤i≤n} :x_i ∈ X_i \text{ for all } 1≤i≤n\}.$$

### Lemma 3.5.12 (Finite choice)

Let $n ≥ 1$ be a natural number, and for each natural number $1 ≤ i ≤ n$, let $X_i$ be a non-empty set. Then there exists an $n$-tuple $(x_i)_{1≤i≤n}$ such that $x_i ∈ X_i$ for all $1≤i≤n$.
 
Aka, if each $X_i$ is non-empty, then the set $\prod_{1≤i≤n}X_i$ is non-empty.

## Appendix a

Refer to
<https://docs.google.com/document/d/1Akjw9_wFH3w6X-e-Lwk2pxYUZur21rhWixyrZ1_RvKQ/edit?usp=sharing>
