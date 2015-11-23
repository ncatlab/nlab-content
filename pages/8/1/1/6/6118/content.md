
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Relational $\beta$-modules
* table of contents
{: toc}

## Idea

>One of my early Honours students at [[Macquarie University]] baffled his proposed Queensland graduate studies supervisor who asked whether the student knew the definition of a [[topological space]]. The aspiring researcher on [[dynamical system]]s answered positively: "Yes, it is a relational $\beta$-module!"  I received quite a bit of flak from colleagues concerning that one; but the student [[Peter Kloeden]] went on to become a full professor of mathematics in Australia then Germany.
---[[Ross Street]], in _[[An Australian conspectus of higher categories]]_

In [1970](#Barr), [[Michael Barr]] gave an abstract definition of [[topological space]] based on a notion of [[convergence]] between [[ultrafilters]] (building on work by [[Ernest Manes]] on [[compact Hausdorff spaces]]).  Succinctly, Barr defined topological spaces as 'relational $\beta$-modules'.  It was subsequently realized that this was a special case of the notion of [[generalized multicategory]].  Here we unpack this definition and examine its properties.

The correctness of this definition (in the sense of matching [[Bourbaki]]\'s definition) is equivalent to the [[ultrafilter principle]] ($UP$).  However, the definition can be treated on its own, even in a context without $UP$.  So we also consider the properties of relational $\beta$-modules when these might not match [[topological space|Bourbaki spaces]]. 


## Definitions

### Abstract description {#abstract} 

If $S$ is a [[set]], let $\beta{S}$ be the set of [[ultrafilters]] on $S$. This set is canonically identified with the set of Boolean algebra homomorphisms 

$$P(S) \to \mathbf{2},$$ 

from the power set of $S$ to $\mathbf{2}$, the unique Boolean algebra with two elements. The 2-element set carries a [[dualizing object]] structure that induces an evident [[adjoint pair]] 

$$(Set \stackrel{P}{\to} Bool^{op}) \; \dashv \;  (Bool^{op} \stackrel{\hom(-, \mathbf{2})}{\to} Set)$$ 

so that the composite [[functor]] $\beta = \hom(P-, \mathbf{2}): Set \to Set$ carries a [[monad]] structure. 

The functor $\beta : Set \to Set$ extends to [[Rel]] as follows: given a [[binary relation]] $r\colon X \to Y$, written as a subobject in $Set$

$$R \stackrel{\langle \pi_1, \pi_2 \rangle}{\to} X \times Y,$$ 

we define $\beta(r): \beta(X) \to \beta(Y)$ to be the relation obtained by taking the image of $\langle \beta(\pi_1), \beta(\pi_2) \rangle: \beta(R) \to \beta(X) \times \beta(Y)$. It turns out, although it is by no means obvious, that $\beta$ is according to this definition a _strict_ functor on $Rel$. 

The monad structure on $\beta: Set \to Set$, given by a unit $u: 1 \to \beta$ and multiplication $m: \beta \beta \to \beta$, extends not to a strict monad on $Rel$, but rather one where the transformations $u, m$ are [[lax natural transformation|op-lax]] in the sense of there being inequalities 

$$\array{
X & \stackrel{u_X}{\to} & \beta X & & & & & & \beta \beta X & \stackrel{m_X}{\to} & \beta X \\  
\mathllap{r} \downarrow & \leq & \downarrow \mathrlap{\beta(r)} & & & & & & \mathllap{\beta \beta (r)} \downarrow & \leq & \downarrow \mathrlap{\beta(r)} \\
Y & \underset{u_Y}{\to} & \beta Y & & & & & & \beta \beta Y & \underset{m_Y}{\to} & \beta Y
}$$ 

(while of course the monad associativity and unit conditions remain as equations: hold on the nose). 

Then a __relational $\beta$-module__ is a [[lax algebra]] (module) of $\beta$ on the [[2-poset]] $Rel$. In other words, a set $S$ equipped with a relation $\xi: \beta S \to S$ such that the following inequalities hold: 

$$\label{rel1} \array{
S & \stackrel{u_S}{\to} & \beta S & & & & & & \beta \beta S & \stackrel{m_S}{\to} & \beta S \\
 & \mathllap{1_S} \searrow \; \leq & \downarrow \mathrlap{\xi} & & & & & & \mathllap{\beta(\xi)} \downarrow & \leq & \downarrow \mathrlap{\xi} \\ 
 & & S & & & & & & \beta S & \underset{\xi}{\to} & S
}$$ 

Arguably, it is better to consider $Rel$ as a [[proarrow equipment]] in this construction, in order to accommodate [[continuous functions]] between topological spaces (not continuous relations!) as the appropriate abstract notion of morphism between relational $\beta$-modules.  We touch on this below, but for a much wider context, see [[generalized multicategory]]. 


### Bridge to a concrete description 

A __relational $\beta$-module__ is a [[set]] $S$ and a [[binary relation]] $\xi: \beta S \to S$ between [[ultrafilters]] on $S$ and [[elements]] of $S$ that satisfy the conditions (eq:rel1) . For $F \in \beta S$ and $x \in S$, we write $F \rightsquigarrow_\xi x$ if $(F, x)$ satisfies the relation $\xi$, or often just $F \rightsquigarrow x$ if the relation is clear. We pronounce this by saying "the ultrafilter $F$ _converges_ to the point $x$", so that $\xi$ plays the role of "notion of convergence". 

Preliminary to explaining the conditions (eq:rel1), we first set up a [[Galois connection]] between $\xi \in Rel(\beta S, S)$ and subsets $\mathcal{C} \in P P(S)$, so that fixed points on the $P P(S)$ side are exactly topologies on $S$, and fixed points on the other side are (as we show below) lax $\beta$-module structures on $S$. The Galois connection would then of course restrict to a Galois correspondence between topologies and lax module structures. 

Recall that each topology $\mathcal{O} \subseteq P(S)$ induces a notion of convergence where $F \rightsquigarrow x$ means $N_x \subseteq F$ ($F$ contains the filter of neighborhoods of $x$). Accordingly, for general $\mathcal{C} \subseteq P(S)$, define the relation $conv(\mathcal{C}) = \xi: \beta S \to S$ by 

$$F \rightsquigarrow_\xi x \;\;\; \Leftrightarrow \;\;\; (\forall_{U: P(S)})\; U \in \mathcal{C} \; \wedge \; x \in U \; \Rightarrow \; U \in F.$$ 

Conversely, a topology $\mathcal{O}$ can be retrieved from its notion of convergence: under the ultrafilter principle, the neighborhood filter of a point $x$ is just the intersection of all ultrafilters containing it (hence all $F$ such that $F \rightsquigarrow x$), and then a set is open if it is a neighborhood of all of its elements. Accordingly, for general "notions of convergence" $\xi \in Rel(\beta S, S)$, we define a collection $\tau(\xi) \subseteq P(S)$ by 

$$\tau(\xi) \coloneqq \{U \subseteq S: \; (\forall_{F: \beta S, x: S})\; (x \in U \; \wedge\; F \rightsquigarrow_\xi x) \Rightarrow U \in F\}.$$ 

+-- {: .num_prop #topology} 
###### Proposition 
$\tau(\xi)$ is a topology on $S$, for any $\xi: Rel(\beta S, S)$. 
=-- 

+-- {: .proof}
###### Proof 
It is trivial that $S \in \tau(\xi)$. If $U, V \in \tau(\xi)$, and if $x \in U \cap V$ and $F \rightsquigarrow x$, then also $x \in U$ and $x \in V$ and we conclude $U, V \in F$, whence $U \cap V \in F$ since $F$ is an ultrafilter, so that $U \cap V$ satisfies the condition of belonging to $\tau(\xi)$. Given a collection of elements $U_i \in \tau(\xi)$, if $x \in \cup_i U_i$ and $F \rightsquigarrow x$, then $x \in U_i$ for some $i$ and we conclude $U_i \in F$, whence $\cup_i U_i \in F$ since $F$ is upward closed. Therefore $\cup_i U_i$ satisfies the condition of belonging to $\tau(\xi)$ (vacuously so if the collection is empty). 
=-- 

+-- {: .num_prop #galois} 
###### Proposition 
There is a Galois connection between notions of convergence on $S$ and subsets of $P(S)$, according to the bi-implication 

$$\mathcal{C} \subseteq \tau(\xi) \; \Leftrightarrow \; \xi \subseteq conv(\mathcal{C}).$$ 

=-- 

+-- {: .proof} 
###### Proof 
To establish the bi-implication, it suffices to observe that both containments $\mathcal{C} \subseteq \tau(\xi)$ and $\xi \subseteq conv(\mathcal{C})$ are equivalent to the condition 

$$\forall_{F: \beta S} \forall_{U: P S} \forall_{x: S} (F \rightsquigarrow_\xi x) \; \wedge \; (U \in \mathcal{C}) \; \wedge \; (x \in U) \; \; \Rightarrow \; \; (U \in F).$$ 
=-- 

+-- {: .num_prop #fix} 
###### Proposition 
If $\mathcal{O}$ is a topology on $S$, then $\mathcal{O} = \tau(conv(\mathcal{O}))$ (i.e., topologies are fixed points of the [[closure operator]] $\tau \circ \conv$). 
=-- 

+-- {: .proof} 
###### Proof 
We already have $\mathcal{O} \subseteq \tau(conv(\mathcal{O}))$ from Proposition \ref{galois}. For the other direction, we must show that any $V$ belonging to $\tau(conv(\mathcal{O}))$ is an $\mathcal{O}$-neighborhood of each of its points. Suppose the contrary: that $x \in V$ but $V$ is not an $\mathcal{O}$-neighborhood of $x$. Then for every $\mathcal{O}$-neighborhood $U \in N_x$, we have $U \cap \neg V \neq \emptyset$, so that sets of this form generate a filter. By the ultrafilter principle, we may extend this filter to an ultrafilter $F$; clearly we have $F \rightsquigarrow x$ and $\neg V \in F$, but since $F \rightsquigarrow x$ and $V \in \tau(conv(\mathcal{O}))$ and $x \in V$, we also have $V \in F$, which is inconsistent with $\neg V \in F$. 
=-- 

Propositions \ref{topology}, \ref{galois}, and \ref{fix} more or less show that a topological space $(S, \mathcal{O})$ is a particular type of [[pseudotopological space]]: 

+-- {: .num_defn} 
###### Definition 
A pseudotopological space is set $S$ equipped with a relation $\xi: \beta S \to S$ such that $1_S \leq \xi \circ u_S$. 
=--  

All that remains is to check is: 

+-- {: .num_prop #pseudo} 
###### Proposition 
The lax unit condition $1_S \leq \xi \circ u_S$ holds if $\xi = conv(\mathcal{O})$, for a topology $\mathcal{O}$. 
=-- 

The unit $u_S: S \to \beta S$ may also be denoted $prin_S$, as it takes an element $x \in S$ to the principal ultrafilter 

$$prin_S(x) = \{U \subseteq S: x \in U\}$$ 

and now the unit condition says $prin_S(x) \rightsquigarrow_\xi x$ for all $x$. For $\xi = conv(\mathcal{O})$, this says $N_x \subseteq prin_S(x)$, or that $x \in V$ for all neighborhoods $V \in N_x$, which is a tautology. 

One of our goals is to prove the following theorem: 

+-- {: .num_theorem #conc} 
###### Theorem 
**(Main Theorem)** 
An arrow $\xi: \beta(S) \to S$ in $Rel$ is of the form $conv(\tau(\xi))$ if and only if the following inequalities are satisfied: 

$$1_S \leq \xi \circ prin_S, \qquad \xi \circ \beta(\xi) \leq \xi \circ m_S$$ 

where $m_S: \beta \beta(S) \to \beta(S)$ is the multiplication on the ultrafilter monad. 
=--

## Ultrafilter monad on $Rel$ {#functor} 

Before rolling up our sleeves and proving the main theorem, we pause to consider some more abstract contexts in which to place the concept of lax $\beta$-module, leading up to the context of generalized multicategories. 

### Extending the ultrafilter functor to $Rel$ 

First we examine more closely the extension of the ultrafilter functor $\beta: Set \to Set$ to $Rel$, showing in particular that the extension is a strict functor. First we slightly rephrase our earlier definition: 

+-- {: .num_defn} 
###### Definition 
For a relation $r: X \to Y$ between sets, given by a subobject $R \hookrightarrow X \times Y$ in $Set$ with projections $f: R \to X$ and $g: R \to Y$, define $\bar{\beta}(r)$ to be the composite 

$$\beta(X) \stackrel{\beta(f)^{o}}{\to} \beta(R) \stackrel{\beta(g)}{\to} \beta(Y)$$ 

in the bicategory of relations. 
=-- 

Any span of functions $(h: S \to X, k: S \to Y)$ that represents $r$ (in the sense that $r = k h^{o}$ in the bicategory of relations) would serve in place of $(f, g)$, since for any such span there is an epi $s: S \to R$ with $h = f s$, $k = g s$, whence $\beta(s)$ is epi (because the epi $s$ splits in $Set$) and we have 

$$\array{
\beta(g)\beta(f)^{o} & = & \beta(g)\beta(s)\beta(s)^{o}\beta(f)^{o} \\
 & = & \beta(g)\beta(s)(\beta(f)\beta(s))^{o} \\ 
 & = & \beta(g s)\beta(f s)^{o} \\ 
 & = & \beta(k)\beta(h)^{o}.
}$$ 

In particular, $\bar{\beta}$ is well-defined. Since $\bar{\beta}$ extends $\beta: Set \to Set$, there is no harm in writing $\beta(r)$ in place of $\bar{\beta}(r)$. If $r \leq r': X \to Y$, then $\beta(r) \leq \beta(r')$ (as can be seen from the calculation displayed above, but replacing the epi $s$ by a general map $t$, and the first equation by an inequality $\geq$). 

+-- {: .num_remark #oplax}
###### Remark 
The same recipe works to extend any functor $T: Set \to Set$ to $Rel$, and the extension $\bar{T}: Rel \to Rel$ is always an _op-lax_ functor in the sense that 

$$\bar{T}(r s) \leq \bar{T}(r) \bar{T}(s)$$ 

as is easily seen by contemplating a pullback diagram (where $r = g f^{o}$ and $s = k h^{o}$): 

$$\array{
 & & & & Q & & & & \\ 
 & & & \mathllap{p} \swarrow & & \searrow \mathrlap{q} & & & \\
 & & R & & & & S & & \\
 & \mathllap{f} \swarrow & & \searrow \mathrlap{g} & & \mathllap{h} \swarrow & & \searrow \mathrlap{k} & \\ 
X & & & & Y & & & & Z
}$$ 

whereupon one calculates 

$$\array{
\bar{T}(r s) & = & T(k q) T(f p)^{o} \\ 
 & = & T(k) T(q) T(p)^{o} T(f)^{o} \\ 
 & \leq & T(k) T(h)^{o} T(g) T(f)^{o} \\ 
 & = & \bar{T}(r) \bar{T}(s) 
}$$ 

where the inequality comes from $T(q) T(p)^{o} \leq T(h)^{o} T(g)$, which is equivalent to $T(h) T(q) \leq T(g) T(p)$ (where even equality holds). This calculation shows that $\bar{T}$ is an actual (not just an op-lax) functor on $Rel$ iff $T$ satisfies the **Beck-Chevalley** condition: if $(p, q)$ is a pullback of $(g, h)$, then 

$$T(q) T(p)^{o} = T(h)^{o} T(g).$$ 

This in turn amounts to $T$ preserving weak pullbacks. (It actually says $T$ takes pullbacks to weak pullbacks, but this implies $T$ takes weak pullbacks to weak pullbacks because any endofunctor $T$ on $Set$ preserves epis, using the axiom of choice.) 
=-- 

+-- {: .num_prop #BC} 
###### Proposition 
The functor $\beta: Set \to Set$ satisfies the Beck-Chevalley condition (and therefore the extension $\beta: Rel \to Rel$ is a strict functor). 
=-- 

+-- {: .proof} 
###### Proof 
Referring to the pullback diagram in Remark \ref{oplax}, let $Q = R \times_Y S$ be the pullback. We must show that the canonical map 

$$\beta(R \times_Y S) \to \beta(R) \times_{\beta(Y)} \beta(S)$$ 

is epic. Viewing this as a continuous map between compact Hausdorff spaces (see [this section](http://ncatlab.org/nlab/show/compactum#ultrafilters_form_a_compactum_23) of the article on [[compacta]]), it suffices to show that the canonical map 

$$R \times_Y S \to \beta(R) \times_{\beta(Y)} \beta(S)$$ 

has a dense image. Let $(G, H) \in \beta(R) \times_{\beta(Y)} \beta(S)$, so that $\beta(g)(G) = \beta(h)(H)$ are the same ultrafilter $J \in \beta(Y)$. Let $\hat{A}$ and $\hat{B}$ be [basic open neighborhoods](http://ncatlab.org/nlab/show/compactum#the_space_of_ultrafilters_19) of $G$ and $H$ in $\beta(R)$ and $\beta(S)$ respectively; we must show that there is $(r, s) \in R \times_Y S$ such that 

$$(prin(r), prin(s)) \in \hat{A} \times \hat{B}$$ 

or in other words such that $r \in A$ and $s \in B$. We have $g^{-1}(g(A)) \in G$ since $A \in G$ and $A \subseteq g^{-1}(g(A))$, so that $g(A)$ belongs to 

$$J = \beta(g)(G) \coloneqq \{C \subseteq Y: g^{-1}(C) \in G\}$$ 

and similarly $h(B) \in J$. It follows that $g(A) \cap h(B) \in J$ so that $g(A) \cap h(B) \neq \emptyset$. Any element $y \in g(A) \cap h(B)$ can be written as $y = g(r)$ and $y = h(s)$ for some $r \in A$ and $s \in B$, and this completes the proof. 
=-- 

### Ultrafilter monad on the equipment $\mathbf{Rel}$ 

As mentioned in an [earlier section](/nlab/show/relational+beta-module#abstract), the natural transformations $u = prin: 1_{Set} \to \beta$, $m: \beta\beta \to \beta$ **do not** extend to (strict) natural transformations on the locally posetal bicategory $Rel$, but only to transformations that are op-lax in the sense of inequalities 

$$prin_Y \circ r \leq \beta(r) \circ prin_X, \qquad m_Y \circ \beta\beta(r) \leq \beta(r) \circ m_X$$ 

for every relation $r: X \to Y$. These are equivalent to inequalities 

$$r \leq prin_Y^o \circ \beta(r) \circ prin_X, \qquad \beta\beta(r) \leq m_Y^o \circ \beta(r) \circ m_X$$ 

and they may be deduced simply by staring at naturality diagrams in $Set$, in which we represent or [[bicategory of relations|tabulate]] $r$ by $\pi_2 \circ \pi_1^o$: 

$$\array{
 & & R & &  & & & & & &   & & \beta\beta (R) & & \\
 & \mathllap{\pi_1} \swarrow & \downarrow_\mathrlap{prin_R} & \searrow \mathrlap{\pi_2} &  & & & & & &  & _\mathllap{\beta\beta\pi_1} \swarrow & \downarrow_\mathrlap{m_R} & \searrow_\mathrlap{\beta\beta\pi_2} & \\ 
X & & \beta (R) & & Y   & & & & & &  \beta \beta (X) & & \beta (R) & & \beta \beta (Y) \\ 
 _\mathllap{prin_X} \downarrow & \swarrow_\mathrlap{\beta \pi_1} & &  _\mathllap{\beta \pi_2} \searrow & \downarrow_\mathrlap{prin_Y}  & & & & & & \mathllap{m_X} \downarrow & \swarrow_\mathrlap{\beta \pi_1} & &  _\mathllap{\beta \pi_2} \searrow & \downarrow \mathrlap{m_Y} \\ 
\beta (X) & & & & \beta (Y) & & & & & & \beta (X) & & & & \beta (Y)
}$$ 

**To get an actual monad**, it is more satisfactory in this context to consider not the bicategory $Rel$, but rather the [[equipment]] or [[framed bicategory]] $\mathbf{Rel}$. That is, there is a 2-category $Equip$ of equipments (as a sub-2-category of a 2-category of double categories), so that the notion of monad makes sense therein, and it turns out the data to hand induces such a monad $\bar{\beta}: \mathbf{Rel} \to \mathbf{Rel}$. 

In more detail: the 0-cells of $\mathbf{Rel}$ are sets, and the horizontal arrows are relations between sets. Vertical arrows are functions between sets, and a 2-cell of shape 

$$\array{
A & \stackrel{r}{\to} & B \\
\mathllap{f} \downarrow & \Downarrow & \downarrow \mathrlap{g} \\ 
C & \stackrel{s}{\to} & D; 
}$$ 

is an inequality $g \circ r \leq s \circ f$. We straightforwardly get a [[double category]] $\mathbf{Rel}$, and the ultrafilter functor on $Set$ extends to a functor $\bar{\beta}: \mathbf{Rel} \to \mathbf{Rel}$ between double categories (or in this case, equipments), preserving all structure in sight. 

Some attention must be paid to the notion of transformation between functors $F, G: \mathbf{B} \to \mathbf{C}$ between equipments. A _transformation_ $\eta: F \to G$ assigns to each 0-cell $b$ of $\mathbf{B}$ a _vertical_ arrow $\eta b: F b \to G b$, and to each horizontal arrow $r: b \to b'$ a 2-cell $\eta r$ of the form 

$$\array{
F b & \stackrel{F r}{\to} & F b' \\
\mathllap{\eta b} \downarrow & \Downarrow \mathrlap{\eta r} & \downarrow \mathrlap{\eta b'} \\ 
G b & \stackrel{G r}{\to} & G b'; 
}$$ 

suitably compatible with the double category structures. 

We thus find that the op-lax structures of the transformations $prin: 1 \to \bar{\beta}$, $m: \bar{\beta} \bar{\beta} \to \bar{\beta}$ on $Rel$ qua _bicategory_ are exactly what we need to produce honest transformations $u: 1 \to \bar{\beta}$, $m: \bar{\beta} \bar{\beta} \to \bar{\beta}$ on $\mathbf{Rel}$ qua _equipment_, and the result is an ultrafunctor monad on the equipment $\mathbf{Rel}$. 

Given a monad $T$ on an equipment $\mathbf{B}$, one may proceed to construct a _horizontal Kleisli equipment_ $HKl(\mathbf{B}, T)$ with the same 0-cells and vertical arrows as $\mathbf{B}$, but whose horizontal arrows are of the form $r: b \to T b'$. A 2-cell in $HKl(\mathbf{B}, T)$ (with vertical source $f$ and vertical target $g$) is a 2-cell in $\mathbf{B}$ of the form 

$$\array{
b & \stackrel{r}{\to} & T b' \\
\mathllap{f} \downarrow & \Downarrow \mathrlap{\alpha} & \downarrow \mathrlap{T g} \\ 
c & \stackrel{s}{\to} & T c'; 
}$$

with horizontal compositions being performed in familiar Kleisli fashion. (When we say "familiar Kleisli fashion", we are using the fact that an equipment allows one to "translate" vertical arrows, in particular the map $m_b: T T b \to T b$, into horizontal arrows, which are then composed horizontally. Similarly, the unit of the monad is translated into a horizontal arrow, where it plays the role of an identity in the Kleisli construction.) 

In an equipment, there is a notion of monoid and monoid homomorphism. A _monoid_ consists of a horizontal arrow $\xi: b \to b$ together with unit and multiplication 2-cells 

$$\array{
b & \stackrel{1_b}{\to} & b & & & & & & b & \stackrel{\xi}{\to}\;\;\; b \;\;\; \stackrel{\xi}{\to} & b\\
\mathllap{1} \downarrow & \Downarrow \mathrlap{\eta} & \downarrow \mathrlap{1} & & & & & & \mathllap{1} \downarrow & \Downarrow \mathrlap{\mu} & \downarrow \mathrlap{1}\\ 
b & \stackrel{\xi}{\to} & b & & & & & & b & \stackrel{\xi}{\to} & b
}$$ 

satisfying evident identities. A _monoid homomorphism_ from $(b, \xi)$ to $(c, \theta)$ consists of a vertical arrow and 2-cell $(f, \phi)$ of the form 

$$\array{
b & \stackrel{\xi}{\to} & b \\
\mathllap{f} \downarrow & \Downarrow \mathrlap{\phi} & \downarrow \mathrlap{f} \\ 
c & \underset{\theta}{\to} & c
}$$ 

that is suitably compatible with the unit and multiplication cells. 

The following notion gives an _interim_ notion of generalized multicategory that applies in particular to relational $\beta$-modules. 

+-- {: .num_defn} 
###### Definition 
Given a monad $T$ on an equipment $\mathbf{B}$, a $T$-*monoid* is a monoid in the horizontal Kleisli equipment $HKl(\mathbf{B}, T)$. A _map_ of $T$-monoids is a homomorphism between monoids in $HKl(\mathbf{B}, T)$. 
=-- 

+-- {: .num_prop} 
###### Proposition 
For the ultrafilter monad $\beta$ on the equipment $\mathbf{Rel}$, a structure of $\beta$-monoid is equivalent to a structure of relational $\beta$-module, and a homomorphism of $\beta$-monoids is the same as a lax map of relational $\beta$-modules in the bicategory $Rel$. 
=-- 

+-- {: .proof} 
###### Proof 
This is really just a matter of unwinding definitions. The data of a $\beta$-monoid in the equipment $\mathbf{Rel}$ amounts to a set $X$ together with a horizontal arrow in the Kleisli construction, that is to say a relation $c: X \to \beta X$ (opposite to our conventional direction, i.e., $c = \xi^o$). The unit and multiplication cells for $c$ are inequalities $1_X \leq c$ and $c \circ_{Kl} c \leq c$ (the vertical source and target being identity maps), where the identity $1_X$ in the Kleisli construction uses the unit for $\beta$ and the Kleisli composition uses the multiplication. Back in the bicategory $Rel$ these translate to relational inequalities 

$$prin_X \leq c, \qquad m_X \circ \beta c \circ c \leq c$$ 

or, with $c = \xi^o$, 

$$prin_X \leq \xi^o, \qquad m_X \circ (\beta (\xi))^o \circ \xi^o \leq \xi^o.$$ 

These boil down to relational inequalities 

$$1_X \leq prin_X^o \circ \xi^o, \qquad (\beta (\xi))^o \circ \xi^o \leq m_X^o \circ \xi^o$$ 

or to 

$$1_X \leq \xi \circ prin_X, \qquad \xi \circ \beta (\xi) \leq \xi \circ m_X,$$

as in the axioms on relational beta-modules. Similarly, a $\beta$-monoid homomorphism $(X, c) \to (Y, d)$ is a vertical arrow $f: X \to Y$ in $HKl(\mathbf{Rel}, \beta)$ together with a suitable 2-cell, which after some unraveling comes down to a relational inequality 

$$\beta (f) \circ c \leq d \circ f$$ 

or to an inequality $\beta (f) \circ \xi_X^o \leq \xi_Y^o \circ f$, which may be further massaged into the form $\xi_X^o \circ f^o \leq (\beta (f))^o \circ \xi_Y^o$, or simply to 

$$f \circ \xi_X \leq \xi_Y \circ \beta (f)$$ 

as advertised in the notion of lax morphism of relational $\beta$-modules (cf. theorem \ref{contmap} below). 
=--

+-- {: .num_remark} 
###### Remark 
In some sense, relational $\beta$-modules as presented here are a toy example of generalized multicategory theory as set out by Cruttwell and Shulman, where they argue that in order to get a fully satisfying theory that unifies all the relevant constructions and examples, one should really work in the context of monads $T$ acting on _virtual_ equipments and study _normalized_ $T$-monoids. Explaining all this requires a lengthy build-up. Even in the relatively restricted packet of unifications that come under the rubric of $(T, V)$-algebras, as studied by [Clementino, Hofmann, Tholen](#CHT2), [Seal](#Seal) and others as a way of bringing topological spaces, uniform spaces, metric spaces, approach spaces, closure spaces, and related notions under one conceptual umbrella, the relevant constructions (e.g. of canonical and op-canonical extensions of [[taut monads]] to lax monads on $V$-matrices) can be somewhat elaborate, and mildly daunting. 

The example of the ultrafilter monad acting on $Rel$ has just enough niceness to it (e.g., the Beck-Chevalley condition) that we are able to elide over most of the complications, while still giving a taste of the generality that goes beyond the "classical" examples of generalized multicategories involving cartesian monads and Kleisli constructions on bicategories of spans. Thus, relational beta-modules can serve as a useful key of entry into this subject. 
=-- 


## Proof of Main Theorem 

We now return to the task of proving theorem \ref{conc}. 

+-- {: .num_remark #open} 
###### Remark 
For a topological space $(S, \mathcal{O})$ and a point $x \in S$, let $\xi = conv(\mathcal{O})$, and let $\mathcal{O}_x$ be the collection of _open_ neighborhoods of $x$. Then $F \rightsquigarrow_\xi x$, i.e., $N_x \subseteq F$, is equivalent to $\mathcal{O}_x \subseteq F$. This is because $N_x$ is the filter generated by $\mathcal{O}_x$. 
=-- 

+-- {: .num_remark} 
###### Remark 
The following conditions are equivalent: 

* $\xi = conv(\mathcal{C})$ for some $\mathcal{C} \subseteq P(S)$; 

* $\xi = conv(\mathcal{O})$ for some topology $\mathcal{O} \subseteq P(S)$; 

* $\xi = conv(\tau(\xi))$. 

Indeed, $conv \circ \tau \circ conv = conv$ by general properties of Galois connections. Applying $conv \circ \tau$ to both sides of the first equation, we have 

$$conv(\tau(\xi)) = (conv \circ \tau \circ conv)(\mathcal{C}) =  conv(\mathcal{C}) = \xi$$ 

so the first equation implies the third. Which in turn implies the second, since we know by proposition \ref{topology} that collections $\mathcal{O}$ of the form $\tau(\xi)$ are topologies. The second equation trivially implies the first. 
=-- 

We now break up our Main Theorem \ref{conc} into the following two theorems. 

+-- {: .num_theorem} 
###### Theorem 
If $\xi = conv(\mathcal{O})$ for a topology $\mathcal{O}$, then the two inequalities of (eq:rel1) are satisfied. 
=-- 

+-- {: .proof} 
###### Proof 
The first inequality (lax unit condition) was already verified in proposition \ref{pseudo}. For the second (lax associativity), let us represent the relation $\xi$ by a span $\beta S \stackrel{\pi_1}{\leftarrow} R \stackrel{\pi_2}{\to} S$, so that $\beta(\xi) = \beta(\pi_2) \beta(\pi_1)^o$. The lax associativity condition becomes 

$$\pi_2 \pi_1^o \beta(\pi_2) \beta(\pi_1)^o \leq \pi_2 \pi_1^o m_S$$ 

which (using $\beta(\pi_1) \dashv \beta(\pi_1)^o$) is equivalent to 

$$\label{assoc} \pi_2 \pi_1^o \beta(\pi_2) \leq \pi_2 \pi_1^o m_S \beta(\pi_1)$$ 

or in other words that for all $\mathcal{G}: \beta(R)$, $x: S$ 

$$\label{conv1} \beta(\pi_2)(\mathcal{G}) \rightsquigarrow_\xi x \;\; \vdash \;\; m_S \beta(\pi_1)(\mathcal{G}) \rightsquigarrow_\xi x.$$ 

Here $\beta(\pi_2)(\mathcal{G})$ is, by definition, 

$$\{U \subseteq S: \pi_2^{-1}(U) \in \mathcal{G}\},$$ 

with $\beta(\pi_1)(\mathcal{G})$ defined similarly. The monad multiplication $m_S: \beta \beta S \to \beta S$ is by definition 

$$(\mathcal{U}: \beta\beta S) \;\; m_S(\mathcal{U}) \coloneqq \{A \subseteq S: \hat{A} \in \mathcal{U}\}$$ 

where $\hat{A} = \{F \in \beta S: A \in F\}$ (see also the [previous section](/nlab/show/relational+beta-module#functor)). 

Thus, (eq:conv1) translates into the following entailment (using remark \ref{open}):  

$$\array{
 & & \mathcal{O}_x \subseteq \{A \subseteq S: \pi_2^{-1}(A) \in \mathcal{G}\} \\ 
 & \vdash & \forall_{U: P S} U \in \mathcal{O}_x \Rightarrow \pi_1^{-1}(\hat{U}) \in \mathcal{G}.
}$$ 

This would naturally follow if 

$$\forall_{U \in \mathcal{O}_x} \pi_2^{-1}(U) \subseteq \pi_1^{-1}(\hat{U}).$$ 

But a pair $(F, y)$ belongs to $\pi_2^{-1}(U)$ if $F \rightsquigarrow_\xi y$ and $y \in U$; we want to show this implies $F = \pi_1(F, y)$ belongs to $\hat{U}$, or in other words that $U \in F$. But this is tautological, given how $conv(\mathcal{O})$ is defined in terms of a topology $\mathcal{O}$. 
=-- 

The next theorem establishes the converse of the preceding theorem; the two theorems together establish the Main Theorem. First we need a remark and a lemma. 

+-- {: .num_remark #closed0} 
###### Remark 
Given any relation $\xi: Rel(\beta S, S)$ and $A \subseteq S$, then $A$ is closed wrt the topology $\tau(\xi)$ if and only if for all $x \in S$, 

$$(\exists_{F: \beta S} A \in F \; \wedge \; F \rightsquigarrow_\xi x) \implies x \in A$$

This follows by inverting the definition of the open sets in $\tau(\xi)$.
=-- 

+-- {: .num_lemma #closed} 
###### Lemma 
If a relation $\xi: Rel(\beta S, S)$ satisfies the inequalities of (eq:rel1) and $x: S$, $A \subseteq S$, we have that $x$ belongs to the closure $\bar{A}$ wrt the topology $\tau(\xi)$ if and only if $\exists_{F: \beta S} A \in F \; \wedge \; F \rightsquigarrow_\xi x$. 
=-- 

+-- {: .proof} 
###### Proof 
For any $A \subseteq S$, denote $A^+ = \{x \mid \exists_{F: \beta S} A \in F \; \wedge \; F \rightsquigarrow_\xi x\}$; we want to show that $A^+ = \bar{A}$. It suffices to show that $A \subseteq A^+ \subseteq \bar{A}$ and that $A^+$ is closed.

That $A^+ \subseteq \bar{A}$ is clear from the characterization of closed sets given in Remark \ref{closed0}; $A^+$ is in some sense the "one-step closure" of $A$. That $A \subseteq A^+$ follows from the lax unit condition for relational $\beta$-modules: if $x \in A$, then $prin(x) \rightsquigarrow_\xi$ and $A \in prin(x)$.

It's clear from the characterization of closed sets given in Remark \ref{closed0} that a set $A$ is closed if and only if $A = A^+$. We will establish that $A^+$ is closed by showing that $(A^+)^+ = A^+$. By the previous paragraph we know that $A^+ \subseteq (A^+)^+$ so we just need the reverse containment. So suppose that $x \in (A^+)^+$, and pick an ultrafilter $F \in \beta S$ with $A^+ \in F$ and $F \rightsquigarrow_\xi x$. In order to show that $x \in A^+$, we need to produce an ultrafilter $F' \in \beta S$ with $A \in F'$ such that $F' \rightsquigarrow_\xi x$. We will do this by applying the lax associativity condition, using an appropriate ultrafilter $\mathcal{G} \in \beta R$.  In fact, we claim that any $\mathcal{G}$ extending the following [filterbase](http://ncatlab.org/nlab/show/filter#filterbases) on $R$:

$$\mathcal{G}_0 = \{\pi_1^{-1}(\hat{A}) \cap \pi_2^{-1}(U)\} \mid U \in F\}$$

will fit the bill. First let us verify that such an ultrafilter $\mathcal{G}$ exists. By the ultrafilter principle, it suffices to verify that $\mathcal{G}_0$ generates a proper filter. It's clear that $\mathcal{G}_0$ is closed under finite intersection. So the filter it generates is proper iff $\mathcal{G}_0$ is proper, i.e. doesn't contain the empty set. Now, a typical element of $\mathcal{G}_0$ is of the form $\pi_1^{-1}(\hat{A}) \cap \pi_2^{-1}(U) = \{(G \in \beta S, \; y \in U) \mid A \in G, G \rightsquigarrow_\xi y\}$ for some $U \in F$. Since $U \in F$ and $A^+ \in F$, we can pick $y \in U \cap A^+$. Since $y \in A^+$, there is $G \in F$ with $A \in G$ such that $G \rightsquigarrow_\xi y$ as desired.

So we can pick a $\mathcal{G} \in \beta R$ extending $\mathcal{G}_0$. We want to establish that

1. $\beta \pi_2(\mathcal{G}) \rightsquigarrow_\xi x$
2. $A \in F':= m_S(\beta \pi_1(\mathcal{G}))$

From (1) it follows that $F' \rightsquigarrow_\xi x$ by lax associativity. Then (2), along with the fact that $F' \rightsquigarrow_\xi x$, implies that $x \in A^+$, as desired. 

For (1) we show that $\beta \pi_2(\mathcal{G}) = F$; this suffices since $F \rightsquigarrow_\xi x$ by hypothesis. Since both sides of the equations are ultrafilters, It further suffices to show that $F \subseteq \beta \pi_2(\mathcal{G})$. So suppose that $U \in F$. We want to show that $U \in \beta \pi_2(\mathcal{G})$ i.e. that $\pi_2^{-1}(U) \in \mathcal{G}$. This is true because $\pi_1^{-1}(\hat{A}) \cap \pi_2^{-1}(U) \in \mathcal{G}$ and the fact that $\mathcal{G}$ is upward closed.

For (2) we want to show that $A \in m_S(\beta \pi_1(\mathcal{G}))$ i.e. that $\hat{A} \in \beta \pi_1(\mathcal{G})$, i.e. that $\pi_1^{-1}(\hat{A}) \in \mathcal{G}$. This is true because $\pi_1^{-1}(\hat{A}) \cap \pi_2^{-1}(U) \in \mathcal{G}$ and the fact that $\mathcal{G}$ is upward closed.
=-- 

+-- {: .num_theorem} 
###### Theorem 
If $\xi: \beta S \to S$ in $Rel$ satisfies the inequalities of (eq:rel1), then $\xi = conv(\tau(\xi))$. 
=-- 

+-- {: .proof} 
###### Proof 
We have $\xi \leq conv(\tau(\xi))$ from the Galois connection (proposition \ref{galois}), so we just need to prove $conv(\tau(\xi)) \leq \xi$, or that $F \rightsquigarrow_{conv(\tau(\xi))} x$ (henceforth abbreviated as $F \rightsquigarrow_{\tau(\xi)} x$) implies $F \rightsquigarrow_\xi x$ under the conditions (eq:rel1). 

If $F \rightsquigarrow_{\tau(\xi)} x$, then every neighborhood $V$ of $x$ belongs to $F$, so that for every $U \in F$, every neighborhood $V$ of $x$ intersects $U$ in a nonempty set. But this just means $x \in \bar{U}$ for every $U \in F$, or in other words (using lemma \ref{closed}) that 

$$U \in F \; \; \vdash \; \; \exists_{G: \beta S} U \in G \; \wedge \; G \rightsquigarrow_\xi x.$$ 

Representing the relation $\xi$ as usual by a subset $\langle \pi_1, \pi_2 \rangle: R \hookrightarrow \beta S \times S$, another way of expressing the existential formula on the right of this entailment is: 

$$\exists_{(G, x): \beta S \times S} \; (G, x) \in R \; \wedge \; G \in \hat{U}$$ 

or 

$$\exists_{\gamma: R} \pi_1(\gamma) \in \hat{U} \wedge \pi_2(\gamma) = x$$ 

or even just 

$$\label{ult} \pi_1^{-1}(\hat{U}) \wedge \pi_2^{-1}(\{x\}) \neq \emptyset$$ 

as subsets of $R$, as $U$ ranges over all elements of $F$. We therefore have that subsets of the form (eq:ult) generate a proper filter of $R$. By the ultrafilter principle, we may extend this filter to an ultrafilter $\mathcal{G} \in \beta R$. 

By construction, we have 

$$F \subseteq \{B \subseteq X: \pi_1^{-1}(\hat{B})) \in \mathcal{G}\} \qquad prin_S(x) \subseteq \{A \subseteq X: \pi_2^{-1}(A) \in \mathcal{G}\}$$ 

but in fact these inclusions are equalities since the left sides and right sides are ultrafilters. Put differently, we have established 

$$F = (m_S \circ \beta(\pi_1))(\mathcal{G}), \qquad prin_S(x) = \beta(\pi_2)(\mathcal{G}).$$ 

Notice that the lax unit condition of (eq:rel1) implies that $prin_S(x) = \beta(\pi_2)(\mathcal{G}) \rightsquigarrow_\xi x$, or that $(\mathcal{G}, x)$ belongs to the relation $\xi \circ \beta(\pi_2)$. Recall also that the lax associativity condition is equivalent to (eq:assoc), which says 

$$\xi \circ \beta(\pi_2) \leq \xi \circ m_S \circ \beta(\pi_1);$$ 

in other words $(\mathcal{G}, x)$ belongs to $\xi \circ m_S \circ \beta(\pi_1)$, i.e., $F = (m_S \circ \beta(\pi_1))(\mathcal{G}) \rightsquigarrow_\xi x$, as was to be shown. 
=-- 

This completes the proof of the Main Theorem (theorem \ref{conc}). 

## Continuous maps 

+-- {: .num_theorem #contmap} 
###### Theorem 
A function between two topological spaces $f: X \to Y$ is continuous if and only if $f \circ \xi \leq \theta \circ \beta(f)$ for their respective topological notions of convergence $\xi, \theta$. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose first that $f$ is continuous, and that $(F, y) \in \beta(X) \times Y$ belongs to $f \circ \xi$, i.e., there is $x$ such that $F \rightsquigarrow x$ and $f(x) = y$. We want to show $\beta(f)(F) \rightsquigarrow y = f(x)$, or that any open set $V$ containing $f(x)$ belongs to $\beta(f)(F)$. The latter means $f^{-1}(V) \in F$, which is true since $f^{-1}(V)$ is an open set containing $x$ and $F \rightsquigarrow x$. 

Now suppose $f \circ \xi \leq \theta \circ \beta(f)$. To show $f$ is continuous, it suffices to show that 

$$f(\bar{A}) \subseteq \widebar{f(A)}$$ 

for any $A \subseteq X$ (easy exercise). For $x \in \bar{A}$, lemma \ref{closed} shows there is $F: \beta(X)$ with $A \in F$ and $F \rightsquigarrow x$. Under the supposition we have $\beta(f)(F) \rightsquigarrow f(x)$, and we also have $f(A) \in \beta(f)(F)$, because $A \subseteq f^{-1}(f(A))$ and $F$ is upward closed and $A \in F$ implies $f^{-1}(f(A)) \in F$. Then again by lemma \ref{closed}, $f(A) \in \beta(f)(F)$ and $\beta(f)(F) \rightsquigarrow f(x)$ implies $f(x) \in \widebar{f(A)}$, as desired. 
=-- 

+-- {: .num_cor #equivalence}
###### Corollary (Barr)

The category of topological spaces is equivalent (even isomorphic to) the category of lax $\beta$-modules and lax morphisms between them. 
=-- 


## Properties 

As above, a [[subset]] $A$ of $S$ is __[[open subset|open]]__ if $A \in \mathcal{U}$ whenever $\mathcal{U} \to x \in A$.  On the other hand, by lemma \ref{closed}, $A$ is __[[closed subset|closed]]__ if $x \in A$ whenever $A \in \mathcal{U} \to x$.

A relational $\beta$-module is __[[compact space|compact]]__ if every ultrafilter converges to at least one point.  It is __[[Hausdorff space|Hausdorff]]__ if every ultrafilter converges to at most one point.  Thus, a __[[compactum]]__ is (assuming $UF$) precisely a relational $\beta$-module in which every ultrafilter converges to exactly one point, that is in which the action of the monad $\beta$ lives in $Set$ rather than in $Rel$. Full proofs may be found at [[compactum]]; see also [[ultrafilter monad]]. 

A continuous map $f$ from $(X, \xi: \beta X \to X)$ to $(Y, \theta: \beta Y \to Y)$ is [[proper map|proper]] if the square 

$$\array{
\beta X & \stackrel{\xi}{\to} & X \\
\mathllap{\beta (f)} \downarrow & & \downarrow \mathrlap{f} \\
\beta Y & \underset{\theta}{\to} & Y
}$$ 

commutes (strictly) in $Rel$, and $f$ is [[open map|open]] if the square 

$$\array{
\beta X & \stackrel{\xi}{\to} & X \\
\mathllap{\beta (f)^o} \uparrow & & \uparrow \mathrlap{f^o} \\
\beta Y & \underset{\theta}{\to} & Y
}$$ 

commutes in $Rel$. From this point of view, a space $X$ is Hausdorff if the diagonal map $\delta: X \to X \times X$ is proper, and compact if $\epsilon: X \to 1$ is proper (and these facts remain true even for pseudotopological spaces). See [Clementino, Hofmann, and Janelidze](#CHJ), _infra_ corollary 2.5. 

The following _ultrafilter interpolation_ result is due to [Pisani](#Pis): 

+-- {: .un_theorem} 
###### Theorem 
A topological space $(X, \xi)$ is exponentiable if, whenever $m_X(\mathcal{U}) \rightsquigarrow_\xi x$ for $\mathcal{U} \in \beta\beta X$ and $x \in X$, there exists $F \in \beta X$ with $\mathcal{U} \rightsquigarrow_{\beta(\xi)} F$ and $F \rightsquigarrow_\xi x$. 
=-- 

For an convergence-approach extension of this result to exponentiable _maps_ in $Top$, see [Clementino, Hofmann, and Tholen](#CHT). 

+-- {: .num_defn} 
###### Definition 
A continuous map $f: X \to Y$ is a _discrete fibration_ if, whenever $G \rightsquigarrow y$ in $Y$ and $f(x) = y$, there exists a unique $F \in \beta(X)$ such that $\beta(f)(F) = G$ and $F \rightsquigarrow x$ in $X$. 
=-- 

+-- {: .num_prop} 
###### Proposition 
A continuous map $f: X \to Y$ is &#233;tale (a local homeomorphism) if $f$ and $\delta_f: X \to X \times_Y X$ are both discrete fibrations. 
=-- 

For more on this, see [Clementino, Hofmann, and Janelidze](#CHJ). 

## Relation to nonstandard analysis

In [[nonstandard analysis]] (which implicitly relies throughout on $UF$), one may define a topological space using a relation between hyperpoints (elements of $S^*$) and standard points (elements of $S$).  If $u$ is a hyperpoint and $x$ is a standard point, then we write $u \approx x$ and say that $x$ is a __[[standard part]]__ of $u$ or that $u$ belongs to the __[[halo]]__ (or _monad_, but *not* the category-theoretic kind) of $x$.  This relation must satisfy a condition analogous to the condition in the definition of a relational $\beta$-module.  The nonstandard defintions of open set, compact space, etc are also analogous.  (Accordingly, one can speak of *the* standard part of $u$ only for Hausdorff spaces.)

So ultrafilters behave very much like hyperpoints.  This is not to say that ultrafilters *are* (or even can be) hyperpoints, as they don\'t obey the [[transfer principle]].  Nevertheless, one does use ultrafilters to construct the [[model]]s of nonstandard analysis in which hyperpoints actually live.  Intuitions developed for nonstandard analysis can profitably be applied to ultrafilters, but the transfer principle is not valid in proofs.


## Relation to other topological concepts

If $\beta$ is treated as a monad on $Set$ instead of on $Rel$, then its algebras are the [[compacta]] (the compact Hausdorff spaces), again assuming $UP$; see [[ultrafilter monad]], and more especially [[compactum]]. 

One might hope that there would be an analogous treatment of [[uniform spaces]] based on an [[equivalence relation]] between ultrafilters.  (In nonstandard analysis, this becomes a relation $\approx$ of infinite closeness between arbitrary hyperpoints, instead of only a relation between hyperpoints and standard points.)  The description in terms of generalized multicategories is known to generalize to a description of uniform spaces, but rather than using relations between ultrafilters, this description uses pro-relations between points. 

For more on relations between Barr's approach to topological spaces, Lawvere's approach to [[metric spaces]], as well as uniform structures, [[prometric spaces]], and [[approach structures]], see [Clementino, Hofmann, and Tholen](#CHT2). 

## References 

* Michael Barr, _Relational algebras_, Springer Lecture Notes in Math. 137 (1970), 39-55.
{#Barr} 

* Maria Manuel Clementino, Dirk Hofmann, and George Janelidze, _On exponentiability of &#233;tale algebraic homomorphisms_, Preprint 11-35, University of Coimbra. ([pdf](http://www.mat.uc.pt/preprints/ps/p1135.pdf))
{#CHJ} 

* Maria Manuel Clementino, Dirk Hofmann, and Walter Tholen, _The convergence approach to exponentiable maps_, Portugaliae Mathematica (Nova Series), Vol. 60 Issue 2 (2003), 139-160. ([web](https://eudml.org/doc/51942)) ([pdf](https://cmuc.mat.uc.pt/rdonweb/publications/publication22.pdf)) 
{#CHT} 

* Maria Manuel Clementino, Dirk Hofmann, and Walter Tholen, _One Setting for All: Metric, Topology, Uniformity, Approach Structure._ ([pdf](http://www.math.yorku.ca/~tholen/ProMat_V_.pdf)) 
{#CHT2} 

* Gavin J. Seal, _Canonical and op-canonical lax algebras_, Theory and 
Applications of Categories, 14 (2005), 221&#8211;243. ([web](http://www.tac.mta.ca/tac/volumes/14/10/14-10abs.html)) 
{#Seal}

* Claudio Pisani, Convergence in exponentiable spaces, Theory Appl. Categories 5 (1999), 148-162. ([web](http://www.tac.mta.ca/tac/volumes/1999/n6/5-06abs.html))
{#Pis}

* [[Geoff Cruttwell]] and [[Mike Shulman]], _A unified framework for generalized multicategories_, [arxiv/0907.2460](http://arxiv.org/abs/0907.2460)




[[!redirects relational beta-module]]
[[!redirects relational beta-modules]]
[[!redirects relational ∞-module]]
[[!redirects relational ∞-modules]]
