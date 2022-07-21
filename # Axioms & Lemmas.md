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

Suppose for each natural number $n$, we have some function $f_n : N → N$ from the
natural numbers to the natural numbers. Let $c$ be a natural number. Then we can
assign a unique natural number an to each natural number $n$, such that $a_0 = c$ and
$a_{n++} = f_n(a_n)$ for each natural number $n$.

Note: The non-trivial parts are:

- Every natural number is assigned
  - s.t. there's no number without assignment
- Every natural number is assigned exactly once
  - s.t. no number is assigned twice with two distinct values

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

Let $n,m$ be natural numbers. Then $n \times m=m \times n$.

### Lemma 2.3.2'

$m \times 0 = 0$

### Lemma 2.3.2’’

$m \times (n++) = m \times n + m$

### Lemma 2.3.3 (Positive natural numbers have no zero divisors)

Let $n,m$ be natural numbers. Then $n \times m = 0$ if and only if at least one of $n, m$
is equal to zero. In particular, if $n$ and $m$ are both positive, then $nm$ is also
positive.

### Proposition 2.3.4 (Distributive law). For any natural numbers a, b, c,

we have a(b+c)=ab+ac and (b+c)a=ba+ca.

### Proposition 2.3.5 (Multiplication is associative)

For any natural numbers a,b,c, we have (a×b)×c=a×(b×c).

### Proposition 2.3.6 (Multiplication preserves order)

If a, b are natural numbers such that a < b, and c is positive, then ac < bc.

### Proposition 2.3.9 (Euclidean algorithm)

Let $n$ be a natural number, and let $q$ be a positive number. Then there exist
natural numbers $m, r$ such that $0 ≤ r < q$ and $n = mq + r$.

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

### Definition 3.6.1 (Equal cardinality)

We say that two sets $X$ and $Y$ have equal cardinality iff there exists a bijection $f : X → Y$ from $X$ to $Y$.

### Proposition 3.6.4

Let $X, Y , Z$ be sets. Then:

- $X$ has equal cardinality with $X$. 
- If $X$ has equal cardinality with $Y$, then $Y$ has equal cardinality with $X$. 
- If $X$ has equal cardinality with $Y$ and $Y$ has equal cardinality with $Z$, then $X$ has equal cardinality with $Z$.

### Proposition 3.6.8 (Uniqueness of cardinality)

Let $X$ be a set with some cardinality $n$. Then $X$ cannot have any other cardinality, i.e., $X$ cannot have cardinality $m$ for any $m \neq n$.

### Lemma 3.6.9

Suppose that $n ≥ 1$, and $X$ has cardinality $n$. Then $X$ is non-empty, and if $x$ is any element of $X$, then the set $X − \{x\}$ (i.e., $X$ with the element $x$ removed) has cardinality $n − 1$.

### Proposition 3.6.14 (Cardinal arithmetic)

- (a) Let $X$ be a finite set, and let $x \notin X$, then $x \cup X$ is finite and $\#(X \cup \{x\}) = \#(X) + 1$
- (b) Let $X, Y$ be finite sets. Then $X \cup Y$ is finite and $\#(X \cup Y) \leq \#(X) + \#(Y)$. If $X \cap Y = 0$ (aka $X, Y$ disjoint) in addition, then $\#(X \cup Y) = \#(X) + \#(Y)$
- (c) Let $X$ be a finite set, and let $Y \subseteq X$, then $Y$ is finite, and $\#(Y) \leq \#(X)$. If $Y \neq X$ in addition, then $\#(Y) \leq \#(X)$
- (d) If $X$ is a finite set, and $f: X \rightarrow Y$ is a function, then $f(X)$ is a finite set with $\#(f(X)) \leq \#(X)$. If in addition $f$ is one to one, then $\#(f(X)) = \#(X)$
- (e) Let $X, Y$ be finite sets, then $\#(X \times Y) = \#(X) \times \#(Y)$
- (f) Let $X, Y$ be finite sets, then then $\#(Y^X) = \#(Y)^{\#(X)}$

### Definition 4.1.1 (Integers)

An integer is an expression of the form $a \text{---} b$, where $a$ and $b$ are natural numbers. Two integers are considered to be equal, $a \text{---} b = c \text{---} d$, if and only if $a + d = c + b$. We let $\Z$ denote the set of all integers.

### Definition 4.1.2

The sum of two integers, $(a\text{---}b)+(c\text{---}d)$, is defined by the formula $(a\text{---}b) + (c\text{---}d) := (a + c)\text{---}(b + d)$
The product of two integers, $(a\text{---}b) × (c\text{---}d)$, is defined by
$(a\text{---}b) × (c\text{---}d) := (ac + bd)\text{---}(ad + bc)$.

### Isomorphism between integer & natural number

Note $n$ behaves similarly to $n \text{---} 0$, as one can verify:

$$
\begin{align*}
(n \text{---} 0) + (m \text{---} 0) &= (n + m)\text{---}0 \\
(n \text{---} 0) \times (m \text{---} 0) &= (n \times m)\text{---}0 \\
\end{align*}
$$

Hence, we may say for $n \in \N$, $n\text{---}0 = n$, as both are isomorphic to each other, aka every equation in $\N$ maps to an equation in $\Z$.

### Definition 4.1.4 (Negation of integers)

If $(a\text{---}b)$ is an integer, we define the negation $−(a\text{---}b)$ to be the integer $(b\text{---}a)$. In particular if $n = n\text{---}0$ is a positive natural number, we can define its negation $−n = 0\text{---}n$.

### Lemma 4.1.5 (Trichotomy of integers)

Let $x$ be an integer. Then exactly one of the following three statements is true: (a) $x$ is zero; (b) $x$ is equal to a positive natural number $n$; or (c) $x$ is the negation $−n$ of a positive natural number $n$.

If $n$ is a positive natural number, we call $−n$ a negative integer. Thus every integer is positive, zero, or negative, but not more than one of these at a time.

### Proposition 4.1.6 (Laws of algebra for integers)

Let $x, y, z$ be integers.
Then we have
$$
\begin{align*}
x+y&=y+x \\
(x + y) + z &= x + (y + z) \\
x+0=0+x&=x  \\ 
x + (−x) = (−x) + x &= 0 \\
xy &= yx \\
(xy)z &= x(yz) \\
x1 = 1x &= x \\
x(y + z) &= xy + xz \\
(y + z)x &= yx + zx
\end{align*}
$$

Aka $\Z$ forms a commutative ring.

### Subtraction of integers

We now define the operation of subtraction $x − y$ of two integers by the formula
$x − y := x + (−y)$

Then, for $a, b \in \N$:

$$a − b = a + (−b) = (a\text{---}0) + (0\text{---}b) = a\text{---}b$$

Hence we can discard $\text{---}$ in favor of $-$.

### Proposition 4.1.8 (Integers have no zero divisors)

Let $a$ and $b$ be integers such that $ab=0$. Then either $a=0$ or $b=0$ (or both).

### Corollary 4.1.9 (Cancellation law for integers)

If $a, b, c$ are integers
such that $ac = bc$ and $c$ is non-zero, then $a = b$.

### Definition 4.1.10 (Ordering of the integers)

Let $n$ and $m$ be integers. We say that $n$ is greater than or equal to $m$, and write $n ≥ m$ or $m ≤ n$, iff we have $n = m+a$ for some natural number $a$. We say that $n$ is strictly greater than $m$, and write $n > m$ or $m < n$, iff $n ≥ m$ and $n \neq m$.

### Lemma 4.1.11 (Properties of order)

Let $a, b, c$ be integers.

- (a) $a>b$ if and only if $a−b$ is a positive natural number.
- (b) (Addition preserves order) If $a>b$, then $a+c>b+c$.
- (c) (Positive multiplication preserves order) If $a > b$ and $c$ is positive, then $ac > bc$.
- (d) (Negation reverses order) If $a > b$, then $−a < −b$.
- (e) (Order is transitive) If $a>b$ and $b>c$, then $a>c$.
- (f) (Order trichotomy ) Exactly one of the statements $a > b$, $a < b$, or $a=b$ is true.

### Definition 4.2.1

A rational number is an expression of the form $a//b$, where $a$ and $b$ are integers and $b$ is non-zero; $a//0$ is not considered to be a rational number. Two rational numbers are considered to be equal, $a//b = c//d$, if and only if $ad = cb$. The set of all rational numbers is denoted $\mathbf{Q}$.

### Definition 4.2.2

If $a//b$ and $c//d$ are rational numbers, we define their sum
their product and the negation

- $(a//b) + (c//d) := (ad + bc)//(bd)$
- $(a//b) * (c//d) := (ac)//(bd)$
- $−(a//b) := (−a)//b$

Note that if $b$ and $d$ are non-zero, then $bd$ is also non-zero, by Proposition 4.1.8, so the sum or product of two rational numbers remains a rational number.

### Isomorphism between rational number and integer

Note:
$$
\begin{align*}
(a//1) + (b//1) &= (a + b)//1 \\ 
(a//1) × (b//1) &= (ab//1) \\
−(a//1) &= (−a)//1
\end{align*}
$$

Hence we define $a = a//1$

### Definition for reciprocal

If $x = a//b$ is a non-zero rational (so that $a, b \neq 0$) then we define the reciprocal $x^{-1}$ of $x$ to be the rational number $x^{-1} := b//a$.

### Proposition 4.2.4 (Laws of algebra for rationals)

Let $x, y, z$ be rationals. Then the following laws of algebra hold:
$$
\begin{align*}
x+y &=y+x \\
(x + y) + z &= x + (y + z) \\
x+0=0+x&=x \\ 
x + (−x) = (−x) + x &= 0 \\
xy &= yx \\
(xy)z &= x(yz) \\
x1 = 1x &= x \\
x(y + z) &= xy + xz \\ 
(y + z)x &= yx + zx \\
xx^{-1} = x^{-1}x &= 1 \quad \text{If } x \neq 0
\end{align*}
$$

### Quotient & subtraction of rationals

We can now define the quotient $x/y$ of two rational numbers $x$ and $y$, provided that $y$ is non-zero, by the formula $x/y := x × y^{-1}$

Hence, $a/b = a//b$ for every integer $a$ and every non-zero integer $b$. Therefore the notation $a//b$ can be discarded.

Similarly:

$$x − y := x + (−y)$$

### Definition 4.2.6

A rational number $x$ is said to be positive iff we have $x = a/b$ for some positive integers $a$ and $b$. It is said to be negative iff we have $x = −y$ for some positive rational $y$ (i.e., $x = (−a)/b$ for some positive integers $a$ and $b$).

### Lemma 4.2.7 (Trichotomy of rationals)

Let $x$ be a rational number. Then exactly one of the following three statements is true: (a) $x$ is equal to $0$. (b) $x$ is a positive rational number. (c) $x$ is a negative rational number.

### Definition 4.2.8 (Ordering of the rationals)

Let $x$ and $y$ be rational numbers. We say that $x > y$ iff $x − y$ is a positive rational number, and $x < y$ iff $x−y$ is a negative rational number. We write $x ≥ y$ iff either $x > y$ or $x = y$, and similarly define $x ≤ y$.

### Proposition 4.2.9 (Basic properties of order on the rationals)

Let $x, y, z$ be rational numbers. Then the following properties hold.

- (a) (Order trichotomy) Exactly one of the three statements $x = y, x<y, x>y$ is true.
- (b) (Order is anti-symmetric) One has $x < y$ if and only if $y > x$.
- (c) (Order is transitive) If $x<y $ and $y<z$,then $x<z$.
- (d) (Addition preserves order) If $x<y$, then $x+z<y+z$.
- (e) (Positive multiplication preserves order) If $x < y$ and $z$ is positive, then $xz < yz$.

### Definition 4.3.1 (Absolute value)

If $x$ is a rational number, the absolute value $|x|$ of $x$ is defined as follows. If $x$ is positive, then $|x| := x$. If $x$ is negative, then $|x| := −x$. If $x$ is zero, then $|x| := 0$.

### Definition 4.3.2 (Distance)

Let $x$ and $y$ be rational numbers. The quantity $|x − y|$ is called the distance between $x$ and $y$ and is sometimes denoted $d(x, y)$, thus $d(x, y) := |x − y|$. For instance, $d(3, 5) = 2$.

### Proposition 4.3.3 (Basic properties of absolute value and distance)

Let $x, y, z$ be rational numbers.

- (a) (Non-degeneracy of absolute value) We have $|x| ≥ 0$. Also, $|x| = 0$ if and only if $x$ is $0$.
- (b) (Triangle inequality for absolute value) We have $|x+y| ≤ |x|+|y|$.
- (c) We have the inequalities $−y≤x≤y$ if and only if $y≥|x|$. In particular, we have $−|x| ≤ x ≤ |x|$.
- (d) (Multiplicativity of absolute value) We have $|xy| = |x| |y|$. In
particular, $| − x| = |x|$.
- (e) (Non-degeneracy of distance) We have $d(x, y) ≥ 0$. Also, $d(x, y) = 0$ if and only if $x=y$.
- (f) (Symmetry of distance) $d(x, y) = d(y, x)$.
- (g) (Triangle inequality for distance) $d(x, z) ≤ d(x, y) + d(y, z)$.

Note: Another useful inequality not included in the list is $|x| - |y| \leq |x - y|$. Note $x = (x - y) + y$, hence $|x| \leq |x - y| + |y|$ by triangle inequality. Therefore $|x| - |y| \leq |x - y|$. Similarly $|y| - |x| \leq |x - y|$. 

### Definition 4.3.4 ($\epsilon$-closeness)

Let $\epsilon > 0$ be a rational number, and let $x,y$ be rational numbers. We say that $y$ is $\epsilon$-close to $x$ iff we have $d(y, x) ≤ \epsilon$.

### Proposition 4.3.7

Let $x, y, z, w$ be rational numbers.

- (a) If $x = y$, then $x$ is $\epsilon$-close to $y$ for every $\epsilon > 0$. Conversely, if $x$ is $\epsilon$-close to $y$ for every $\epsilon>0$, then we have $x=y$.
- (b) Let $\epsilon>0$. If $x$ is $\epsilon$-close to $y$, then $y$ is $\epsilon$-close to $x$.
- (c) Let $\epsilon,\delta > 0$. If $x$ is $\epsilon$-close to $y$, and $y$ is $\delta$-close to $z$, then $x$ and $z$ are $(\epsilon + \delta)$-close.
- (d) Let $\epsilon,\delta > 0$. If $x$ and $y$ are $\epsilon$-close, and $z$ and $w$ are $\delta$-close, then $x+z$ and $y+w$ are $(\epsilon+\delta)$-close, and $x−z$ and $y−w$ are also $(\epsilon + \delta)$-close.
- (e) Let $\epsilon > 0$. If $x$ and $y$ are $\epsilon$-close, they are also $\epsilon$′-close for every $\epsilon′ > \epsilon$.
- (f) Let $\epsilon>0$. If $y$ and $z$ are both $\epsilon$-close to $x$, and $w$ is between $y$ and $z$ (i.e., $y ≤ w ≤ z$ or $z ≤ w ≤ y$), then $w$ is also $\epsilon$-close to $x$.
- (g) Let $\epsilon > 0$. If $x$ and $y$ are $\epsilon$-close, and $z$ is non-zero, then $xz$ and $yz$ are $\epsilon|z|$-close.
- (h) Let $\epsilon,\delta > 0$. If $x$ and $y$ are $\epsilon$-close, and $z$ and $w$ are $\delta$-close, then $xz$ and $yw$ are $(\epsilon|z| + \delta|x| + \epsilon\delta)$-close.

### Definition 4.3.9 (Exponentiation to a natural number)

Let $x$ be a rational number. To raise $x$ to the power $0$, we define $x^0 := 1$; in particular we define $0^0 := 1$. Now suppose inductively that $x_n$ has been defined for some natural number $n$, then we define $x^{n+1} := x^n \times x$.

### Proposition 4.3.10 (Properties of exponentiation, I)

Let $x,y$ be rational numbers, and let $n, m$ be natural numbers.

- (a) We have $x^n x^m = x^{n+m}$, $(x^n)^m = x^{nm}$, and $(xy)^n = x^ny^n$.
- (b) Suppose $n>0$. Then we have $x^n =0$ if and only if $x=0$.
- (c) If $x ≥ y ≥ 0$, then $x^n ≥ y^n ≥ 0$. If $x > y ≥ 0$ and $n > 0$, then $x^n > y^n ≥ 0$.
- (d) We have $|x^n| = |x|^n$.

### Definition 4.3.11 (Exponentiation to a negative number)

Let $x$ be a non-zero rational number. Then for any negative integer $-n$, we define $x^{−n} := 1 / x^n$.

### Proposition 4.3.12 (Properties of exponentiation, II)

Let $x, y$ be non-zero rational numbers, and let $n, m$ be integers.

- (a) We have $x^nx^m = x^{n+m}$, $(x^n)^m = x^{nm}$, and $(xy)^n = x^ny^n$.
- (b) If $x≥y>0$, then $x^n ≥ y^n >0$ if $n$ is positive,and $0< x^n ≤ y^n$ if $n$ is negative.
- (c) If $x,y>0,n \neq 0$, and $x^n =y^n$,then $x=y$.
- (d) We have $|x^n| = |x|^n$.

### Proposition 4.4.1 (Interspersing of integers by rationals)

Let $x$ be a rational number. Then there exists an integer $n$ such that $n ≤ x < n+1$. In fact, this integer is unique (i.e., for each $x$ there is only one $n$ for which $n ≤ x < n + 1$). In particular, there exists a natural number $N$ such that $N > x$ (i.e., there is no such thing as a rational number which is larger than all the natural numbers).

### Proposition 4.4.3 (Interspersing of rationals by rationals)

If $x$ and $y$ are two rationals such that $x < y$, then there exists a third rational $z$ such that $x < z < y$.

### Proposition 4.4.4

There does not exist any rational number $x$ for which $x^2 = 2$.

### Proposition 4.4.5

For every rational number $ε > 0$, there exists a non-negative rational number $x$ such that $x^2 < 2 < (x + ε)^2$.

### Definition 5.1.1 (Sequences)

Let $m$ be an integer. A sequence $(a_n)^{\infty}_n=m$ of rational numbers is any function from the set $\{n ∈ \Z : n ≥ m\}$ to $\mathbf{Q}$, i.e., a mapping which assigns to each integer $n$ greater than or equal to $m$, a rational number $a_n$. More informally, a sequence $(a_n)^{\infty}_n=m$ of rational numbers is a collection of rationals $a_m, a_{m+1}, a_{m+2}, ...$

### Definition 5.1.3 (ε-steadiness)

Let $ε > 0$. A sequence $(a_n)^{\infty}_n=0$ is said to be $ε$-steady iff each pair $a_j, a_k$ of sequence elements is $\epsilon$-close for every natural number $j, k$. In other words, the sequence $a_0, a_1, a_2,...$. is $ε$-steady iff $d(a_j,a_k) ≤ ε$ for all $j,k$.

### Definition 5.1.6 (Eventual ε-steadiness)

Let $ε > 0$. A sequence $(a_n)^{\infty}_n=0$ is said to be eventually $ε$-steady iff the sequence $a_N, a_{N+1}, a_{N+2}, ...$ is $\epsilon$-steady for some natural number $N ≥ 0$. In other words, the sequence $a_0, a_1, a_2, ...$ is eventually $ε$-steady iff there exists an $N ≥ 0$ such that $d(a_j,a+k) ≤ ε$ for all $j,k ≥ N$.

### Definition 5.1.8 (Cauchy sequences)

A sequence $(a_n)^{\infty}_n=0$ of rational numbers is said to be a Cauchy sequence iff for every rational $ε > 0$, the sequence $(a_n)^{\infty}_n=0$ is eventually $ε$-steady. In other words, the sequence $a_0, a_1, a_2, ...$ is a Cauchy sequence iff for every $ε > 0$, there exists an $N ≥ 0$ such that $d(a_j,a_k) ≤ ε$ for all $j,k ≥ N$.

### Definition 5.1.12 (Bounded sequences)

Let $M ≥ 0$ be rational. A finite sequence $a_1, a_2,...,a_n$ is bounded by $M$ iff $|a_i| ≤ M$ for all $1 ≤ i ≤ n$. An infinite sequence $(a_n)^{\infty}_n=1$ is bounded by $M$ iff $|a_i| ≤ M$ for all $i ≥ 1$. A sequence is said to be bounded iff it is bounded by $M$ for some rational $M ≥ 0$.

### Lemma 5.1.14 (Finite sequences are bounded)

Every finite sequence $a_1,a_2,...,a_n$ is bounded.

### Lemma 5.1.15 (Cauchy sequences are bounded)

Every Cauchy sequence $(a_n)^{\infty}_{n=1}$ is bounded.

### Definition 5.2.1 ($ε$-close sequences)

Let $(a_n)^{∞}_{n}=0$ and $(b_n)^{∞}_{n}=0$ be two sequences, and let $ε > 0$. We say that the sequence $(a_n)^{∞}_n=0$ is $\epsilon$-close to $(b_n)^{∞}_{n}=0$ iff $a_n$ is $ε$-close to bn for each $n ∈ \N$. In other words, the sequence $a_0,a_1,a_2,...$ is $ε$-close to the sequence $b_0,b_1,b_2,...$ iff $|a_n − b_n| ≤ ε$ for all $n = 0,1,2,....$

### Definition 5.2.3 (Eventually ε-close sequences)

Let $(a_n)^{∞}_n=0$ and $(b_n)^{∞}_n=0$ be two sequences, and let $ε > 0$. We say that the sequence $(a_n)^{∞}_n=0$ is eventually $\epsilon$-close to $(b_n)^{∞}_n=0$ iff there exists an $N ≥ 0$ such that the sequences $(a_n)^{∞}_{n=N}$ and $(b_n)^{∞}_{n=N}$ are $\epsilon$-close. In other words, $a_0,a_1,a_2,...$ is eventually $ε$-close to $b_0,b_1,b_2,...$ iff there exists an $N ≥ 0$ such that $|a_n − b_n| ≤ ε$ for all $n ≥ N$.

### Definition 5.2.6 (Equivalent sequences)

Two sequences $(a_n)^{∞}_n=0$ and $(b_n)^{∞}_n=0$ are equivalent iff for each rational $ε > 0$, the sequences $(a_n)^{∞}_n=0$ and $(b_n)^{∞}_n=0$ are eventually $ε$-close. In other words, $a_0, a_1, a_2, ...$ and $b_0,b_1,b_2,...$ are equivalent iff for every rational $ε > 0$, there exists an $N ≥ 0$ such that $|a_n − b_n| ≤ ε$ for all $n ≥ N$.

### Definition 5.3.1 (Real numbers)

A real number is defined to be an object of the form $\operatorname{LIM}_{n→∞} a_n$, where $(a_n)^{∞}_{n=1}$ is a Cauchy sequence of rational numbers. Two real numbers $\operatorname{LIM}_{n→∞} a_n$ and $\operatorname{LIM}_{n→∞}b_n$ are said to be equal iff $(a_n)^{∞}_{n=1}$ and $(b_n)^{∞}_{n=1}$ are equivalent Cauchy sequences. The set of all real numbers is denoted $\R$.

### Proposition 5.3.3 (Formal limits are well-defined)

Let $x = \operatorname{LIM}_{n→∞} a_n, y = \operatorname{LIM}_{n→∞} b_n$, and $z = \operatorname{LIM}_{n→∞} c_n$ be real numbers. Then, with the above definition of equality for real numbers, we have $x=x$. Also, if $x=y$,then $y=x$. Finally, if $x=y$ and $y=z$,then $x = z$.

### Definition 5.3.4 (Addition of reals)

Let $x = \operatorname{LIM}_{n\rightarrow \infty} a_n$ and $y = \operatorname{LIM}_{n\rightarrow \infty} b_n$ be real numbers. Then we define the sum $x + y$ to be $x + y := \operatorname{LIM}_{n\rightarrow \infty}(a_n + b_n)$.

### Lemma 5.3.6 (Sum of Cauchy sequences is Cauchy)

Let $x = \operatorname{LIM}_{n\rightarrow \infty} a_n$ and $y = \operatorname{LIM}_{n\rightarrow \infty} b_n$ be real numbers. Then $x + y$ is also a real number (i.e., $(a_n + b_n)^{∞}_{n=1} is a Cauchy sequence of rationals).

### Lemma 5.3.7 (Sums of equivalent Cauchy sequences are equivalent)

Let $x = \operatorname{LIM}_{n\rightarrow \infty} a_n, y = \operatorname{LIM}_{n\rightarrow \infty} b_n$, and $x′ = \operatorname{LIM}_{n\rightarrow \infty} a_n'$ be real numbers. Suppose that $x=x′$. Then we have $x+y=x′+y$.

### Definition 5.3.9 (Multiplication of reals)

Let $x = \operatorname{LIM}_{n\rightarrow \infty} a_n$ and $y = \operatorname{LIM}_{n\rightarrow \infty} b_n$ be real numbers. Then we define the product $xy$ to be $xy := \operatorname{LIM}_{n\rightarrow \infty} a_nb_n$.

### Proposition 5.3.10 (Multiplication is well defined)

Let $x = \operatorname{LIM}_{n\rightarrow \infty} a_n, y = \operatorname{LIM}_{n\rightarrow \infty} b_n$, and $x' = \operatorname{LIM}_{n\rightarrow \infty} a_n'$ be real numbers. Then $xy$ is also a real number. Furthermore, if $x = x'$, then $xy = x'y$.

### Proposition 5.3.11

All the laws of algebra from Proposition 4.1.6 hold not only for the integers, but for the reals as well.

### Definition 5.3.12 (Sequences bounded away from zero)

A sequence $(a_n)^{∞}_{n=1}$ of rational numbers is said to be bounded away from zero iff there exists a rational number $c > 0$ such that $|a_n| ≥ c$ for all $n ≥ 1$.

### Lemma 5.3.14

Let $x$ be a non-zero real number. Then $x = \operatorname{LIM}_{n\rightarrow \infty} a_n$ for some Cauchy sequence $(a_n)^{∞}_{n=1}$ which is bounded away from zero.

### Lemma 5.3.15

Suppose that $(a_n)^{∞}_{n=1}$ is a Cauchy sequence which is
bounded away from zero. Then the sequence $(a_n^{−1})^{∞}_{n=1}$ is also a Cauchy sequence.

### Definition 5.3.16 (Reciprocals of real numbers)

Let $x$ be a non-zero real number. Let $(a_n)^{∞}_{n=1}$ be a Cauchy sequence bounded away from zero such that $x = \operatorname{LIM}_{n\rightarrow \infty} a_n$ (such a sequence exists by Lemma 5.3.14).

Then we define the reciprocal $x^{-1}$ by the formula $x^{-1} := \operatorname{LIM}_{n\rightarrow \infty} a_n^{-1}$.
(From Lemma 5.3.15 we know that $x^{−1}$ is a real number.)

### Lemma 5.3.17 (Reciprocation is well defined)

Let $(a_n)^{∞}_{n=1}$ and $(b_n)^{∞}_{n=1}$ be two Cauchy sequences bounded away from zero such that $\operatorname{LIM}_{n\rightarrow \infty} a_n = \operatorname{LIM}_{n\rightarrow \infty} b_n$ (i.e., the two sequences are equivalent). Then $\operatorname{LIM}_{n\rightarrow\infty} a_n^{−1} = \operatorname{LIM}_{n\rightarrow\infty} b_n^{−1}$.

### Definition 5.4.1

Let $(a_n)^{\infty}_{n=1}$ be a sequence of rationals. We say that this sequence is positively bounded away from zero iff we have a positive rational $c > 0$ such that $a_n ≥ c$ for all $n ≥ 1$ (in particular, the sequence is entirely positive). The sequence is negatively bounded away from zero iff we have a negative rational $−c<0$ such that $a_n ≤−c$ for all $n≥1$ (in particular, the sequence is entirely negative).

### Definition 5.4.3

A real number $x$ is said to be positive iff it can be written as $x = \operatorname{LIM}_{n→∞} a_n$ for some Cauchy sequence $(a_n)^{\infty}_{n=1}$ which is positively bounded away from zero. $x$ is said to be negative iff it can be written as $x = \operatorname{LIM}_{n→∞}$ an for some sequence $(a_n)^{\infty}_{n=1}$ which is negatively bounded away from zero.

### Proposition 5.4.4 (Basic properties of positive reals)

For every real number $x$, exactly one of the following three statements is true:

- (a) $x$ is zero
- (b) $x$ is positive
- (c) $x$ is negative.

A real number $x$ is negative if and only if $−x$ is positive. If $x$ and $y$ are positive, then so are $x + y$ and $xy$.

### Definition 5.4.5 (Absolute value)

Let $x$ be a real number. We define the absolute value $|x|$ of $x$ to equal $x$ if $x$ is positive, $−x$ when $x$ is negative, and $0$ when $x$ is zero.

### Definition 5.4.6 (Ordering of the real numbers)

Let $x$ and $y$ be real numbers. We say that $x$ is greater than $y$, and write $x > y$, if $x−y$ is a positive real number, and $x < y$ iff $x − y$ is a negative real number. We define $x ≥ y$ iff $x > y$ or $x = y$, and similarly define $x ≤ y$.

### Proposition 5.4.7

All the claims in Proposition 4.2.9 which held for rationals, continue to hold for real numbers.

### Proposition 5.4.8

Let $x$ be a positive real number. Then $x^{-1}$ is also positive. Also, if $y$ is another positive number and $x > y$, then $x^{−1} < y^{−1}$.

### Corollary 5.4.10

Let $(a_n)^{∞}_{n=1}$ and $(b_n)^{∞}_{n=1}$ be Cauchy sequences of rationals such that $a_n ≥ b_n$ for all $n ≥ 1$. Then $\operatorname{LIM}_{n→∞} a_n ≥ \operatorname{LIM}_{n→∞} b_n$.

### Proposition 5.4.12 (Bounding of reals by rationals)

Let $x$ be a positive real number. Then there exists a positive rational number $q$ such that $q ≤ x$, and there exists a positive integer $N$ such that $x ≤ N$.

### Corollary 5.4.13 (Archimedean property)

Let $x$ and $ε$ be any positive real numbers. Then there exists a positive integer $M$ such that $Mε > x$.

### Proposition 5.4.14

Given any two real numbers $x < y$, we can find a rational number $q$ such that $x < q < y$.

## Appendix a

Refer to
<https://docs.google.com/document/d/1Akjw9_wFH3w6X-e-Lwk2pxYUZur21rhWixyrZ1_RvKQ/edit?usp=sharing>
