#Contents#
* automatic table of contents goes here
{:toc}

##Definition 

A __Malcev operation__ on a [[set]] $X$ is a ternary operation, a [[function]]

$$ t:X\times X\times X\to X,\,\,\,(x,y,z)\mapsto t(x,y,z) ,$$

which satisfies the identities $t(x,x,z)=z$ and $t(x,z,z)=x$.
An important motivating example is the operation $t$ of a [[heap]], for example the operation on a [[group]] defined by $t(x, y, z) = x y^{-1} z$. 

An [[algebraic theory]] $T$ is a __Malcev theory__ when $T$ contains a Malcev operation. An algebraic theory is Malcev iff one of the following equivalent statements is true:

1. in the category of $T$-algebras, every [[internal relation|internal]] [[reflexive relation]] is a [[congruence]];

2. in the category of $T$-algebras, the composite (as internal relations) of any two congruences is a congruence;

3. in the category of $T$-algebras, the composition of equivalence relations is commutative.

Statement (1) is one of the motivations to introduce the notion of [[Malcev category]]. 

A __Malcev variety__ is the category of $T$-algebras for a Malcev theory $T$, thought of as a [[variety of algebras]]. 

## Proofs of equivalence 

If $R \hookrightarrow X \times Y$ is a binary relation on sets, write $R(x, y)$ to say that $(x, y) \in R$. If $X$, $Y$ are $T$-algebras, then $R$ is an internal relation in $T$-$Alg$ if the conditions $R(x_1, y_1) \wedge \ldots \wedge R(x_n, y_n)$, and $\theta(x_1, \ldots, x_n) = x$, $\theta(y_1, \ldots, y_n) = y$ for any $n$-ary operation $\theta$ of $T$, jointly imply $R(x, y)$. 

The set-theoretic composite of two internal relations in $T$-$Alg$ is also an internal relation, and the equality relation is always internal, so we may (and will) apply ordinary set-theoretic reasoning in our proofs below. 

+-- {: .un_prop}
######Proposition 1
If $T$ is a Malcev theory, then any internal reflexive relation in $T$-$Alg$ is an internal equivalence relation. 
=--

+-- {: .proof}
######Proof
If $t$ is a Malcev operation and $R$ is any internal reflexive relation on a $T$-algebra $X$, then $R$ is transitive because given $R(x, y) \wedge R(y, z)$, we infer $R(x, y) \wedge R(y, y) \wedge R(y, z)$, and this together with $t(x, y, y) = x$ and $t(y, y, z) = z$ gives $R(x, z)$ since $R$ is internal. Also $R$ is symmetric, because if $R(x, y)$, we infer $R(x, x) \wedge R(x, y) \wedge R(y, y)$, which together with $t(x, x, y) = y$ and $t(x, y, y) = x$ gives $R(y, x)$. 
=-- 

+-- {: .un_prop}
######Proposition 2
If every internal reflexive relation is an internal equivalence relation, then the composite of any two internal equivalence relations is also an internal equivalence relation. 
=--

+-- {: .proof} 
######Proof
The hypothesis is that internal reflexive relations and internal equivalence relations coincide. But (internal) reflexive relations are 
clearly closed under composition: $\Delta = \Delta \circ \Delta \subseteq R \circ S$.  
=-- 

+-- {: .un_prop}
######Proposition 3
If internal equivalence relations are closed under composition, then composition of internal equivalence relations is commutative. 
=--

+-- {: .proof}
######Proof 
If $R$ and $S$ are equivalence relations and so is $S \circ R$, then 
$$S \circ R = (S \circ R)^{op} = R^{op} \circ S^{op} = R \circ S,$$
as desired. 
=--

+-- {: .un_prop}
######Proposition 4
If composition of internal equivalence relations in $T$-$Alg$ is commutative, then the theory $T$ has a Malcev operation $t$. 
=--

+-- {: .proof} 
######Proof
According to the yoga of (Lawvere) [[Lawvere theory|algebraic theories]], $n$-ary operations are identified with elements of $F(n)$, the free $T$-algebra on $n$ generators (more precisely, the Lawvere theory is the category opposite to the category of finitely generated free $T$-algebras). Thus we must exhibit a suitable element $t$ of $F(3)$. 

Let $x, y, z$ be the generators of $F(3)$, and let $a, b$ be the generators of $F(2)$. Let $\phi$ be the unique algebra map $F(3) \to F(2)$ taking $x$ and $y$ to $a$ and $z$ to $b$, and let $\psi$ be the unique algebra map $F(3) \to F(2)$ taking $x$ to $a$ and $y$ and $z$ to $b$. An operation $t \in F(3)$ is Malcev precisely when 

$$\phi(t) = b \qquad \psi(t) = a$$ 

Let $R$ be the equivalence relation on $F(3)$ given by the kernel pair of $\phi$, and let $S$ be the kernel pair of $\psi$. Then $R(x, y)$ and $S(y, z)$, so $(S \circ R)(x, z)$. Then, since composition of equivalence relations is assumed commutative, $(R \circ S)(x, z)$. This means there exists $t$ such that $S(x, t)$ and $R(t, z)$, or that $\psi(x) = \psi(t)$ and $\phi(t) = \phi(z)$. This completes the proof. 
=--

## Examples 

* The theory of [[group]]s, where $t(x, y, z) = x y^{-1} z$, is Malcev. 

* The theory of [[Heyting algebra]]s, where 
$$t(x, y, z) = ((z \Rightarrow y) \Rightarrow x) \wedge ((x \Rightarrow y) \Rightarrow z),$$
is Malcev. 

* If $T$ is Malcev, and if $T \to T'$ is a morphism of algebraic theories, then $T'$ is Malcev. From this point of view, the theory of groups is Malcev because the theory of heaps is Malcev, and the theory of Heyting algebras is Malcev because the theory of [[cartesian closed category|cartesian closed]] [[meet-semilattice]]s is Malcev. 

See also [[Malcev category]]. 

## The lattice of congruences $Equiv(X)$

### $Equiv(X)$ is a modular lattice

In any [[finitely complete category]], the intersection of two congruences (equivalence relations) on an object $X$ is a congruence, so that the set of equivalence relations $Equiv(X)$ is a meet-semilattice. 

In a [[regular category]] such as a variety of algebras, where there is a sensible calculus of relations and relational composition, it is a simple matter to prove that if $Equiv(X)$ is closed under relational composition, then $R \circ S$ is the join $R \vee S$ in $Equiv(X)$. For, if $R, S \in Equiv(X)$, then 

$$R = R \circ \Delta \subseteq R \circ S, \qquad S = \Delta \circ S \subseteq R \circ S$$ 

while if $R, S \subseteq T$ in $Equiv(X)$, then 

$$R \circ S \subseteq T \circ T \subseteq T.$$

+-- {: .un_prop}
######Proposition 
In a regular category, if $Equiv(X)$ is closed under relational composition (equivalently, if composition of equivalence relations is commutative), then $Equiv(X)$ is a [[modular lattice]]. 
=-- 

+-- {: .proof} 
######Proof
The (poset-enriched) category of relations in a regular category is an [[allegory]], and hence satisfies Freyd's modular law 

$$R \wedge (S \circ T) \subseteq S \circ ((S^{op} \circ R) \wedge T)$$ 

whenever $T: X \to Y$, $S: Y \to Z$, $R: X \to Z$ are relations. As we have just seen, the hypothesis implies that joins in $Equiv(X)$ are given by composition (so $Equiv(X)$ is a lattice), and so for $R, S, T \in Equiv(X)$ we have

$$R \wedge (S \vee T) \subseteq S \vee ((S \vee R) \wedge T).$$ 

Therefore, if $S \subseteq R$, we have both

$$R \wedge (S \vee T) \subseteq S \vee (R \wedge T)$$ 

and also $S \vee (R \wedge T) \subseteq R \wedge (S \vee T)$. Thus $S \subseteq R$ implies $R \wedge (T \vee S) = (R \wedge T) \vee S$: the modular law is satisfied in $Equiv(X)$. 
=--

+-- {: .un_cor}
######Corollary
If $T$ is a Malcev theory, then the lattice of congruences $Equiv(X)$ on any $T$-algebra $X$ is a modular lattice. 
=--

### $Equiv(X)$ is a Desarguesian lattice 

A similar argument shows that congruence lattices for $T$-algebras $X$, for $T$ a Malcev theory, satisfy the following property (stronger than the modular property):

* [[Desarguesian axiom|Desarguesian property]]: if $R_i, S_i, T_i \in Equiv(X)$ for $i = 1, 2$, then
$$(R_1 \vee R_2) \wedge (S_1 \vee S_2)) \subseteq T_1 \vee T_2 \qquad implies \qquad (R_1 \vee S_1) \wedge (R_2 \vee S_2) \subseteq ((R_1 \vee T_1) \wedge (R_2 \vee T_2)) \vee ((S_1 \vee T_1) \wedge (S_2 \vee T_2))$$ 

Freyd-Scedrov's [[Categories, Allegories]] (2.157, pp. 206-207) gives the following argument: given relations $R_1, S_1, T_1: X \to Y$, $R_2, S_2, T_2: Y \to Z$ between sets, it is "easily verified" that  

$$R_2 R_1 \cap S_2 S_2 \subseteq T_2 T_1 \qquad implies \qquad S_1 R_{1}^{op} \cap S_{2}^{op} R_2 \subseteq (S_1 T_{1}^{op} \wedge S_{2}^{op} T_2)(T_1 R_{1}^{op} \cap T_{2}^{op}R_2)$$ 

Then, under the assumption that equivalence relations internal to $T$-$Alg$ commute (so that the join of equivalence relations $R, S$ on $X$ is their relational composite $R S = R \circ S$), the Desarguesian axiom follows immediately. 

## References

See the monograph [[Borceux-Bourn]].


## Spelling

The original is 'Мальцев'; Malcev spelled his name as 'Malcev' in his non-Russian papers.
This has also been transliterated 'Mal'cev', 'Mal'tsev' and 'Maltsev'.

[[!redirects Mal'cev variety]]
[[!redirects Mal'cev varieties]]
[[!redirects Mal'cev operation]]
[[!redirects Mal'cev operations]]
[[!redirects Mal'cev theory]]
[[!redirects Mal'cev theories]]
[[!redirects Malcev varieties]]
[[!redirects Malcev operation]]
[[!redirects Malcev operations]]
[[!redirects Malcev theory]]
[[!redirects Malcev theories]]
[[!redirects Maltsev variety]]
[[!redirects Maltsev varieties]]
[[!redirects Maltsev operation]]
[[!redirects Maltsev operations]]
[[!redirects Maltsev theory]]
[[!redirects Maltsev theories]] 
[[!redirects Мальцев variety]]
[[!redirects Мальцев varieties]]
[[!redirects Мальцев operation]]
[[!redirects Мальцев operations]]
[[!redirects Мальцев theory]]
[[!redirects Мальцев theories]]