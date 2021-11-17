
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Equicontinuous functions
* table of contents
{: toc}

## Idea

A [[function]] $f$ is [[continuous map|continuous]] if, roughly speaking, $f(x)$ is arbitrarily close to $f(y)$ whenever $x$ is sufficiently close to $y$.  However, 'close' is relative, and $f(x)$ may be much closer to $f(y)$ than $g(x)$ is to $g(y)$, even if both $f$ and $g$ are continuous.  Nevertheless, given a [[family]] of functions, we may have that $f(x)$ is arbitrarily close to $f(y)$ for *every* function $f$ in the family at once whenever $x$ is sufficiently close to $y$.  In this case, the family of functions is _equicontinuous_.


## Definitions

Because we are considering the relative degree of closeness between potentially unrelated pairs of points, we need a [[uniform structure]] to define this concept.  So let $X$ and $Y$ be [[uniform spaces]] (although the concept should make sense in somewhat greater generality), and let $\mathcal{F}$ be a [[family]] of [[functions]] from $X$ to $Y$.

+-- {: .num_defn #Continuous}
###### Definition

The family $\mathcal{F}$ is __continuous__ if each member is [[continuous function|continuous]]:  For each [[entourage]] $E$ in $Y$, for each function $f$ in $\mathcal{F}$ and each [[point]] $x \in X$, for some entourage $D$ in $X$, for each point $y$ in $X$, whenever $x \approx_D y$, we have $f(x) \approx_E f(y)$.
=--

In short:
$$ \forall E,\; \forall f,\; \forall x,\; \exists D,\; \forall y,\; x \approx_D y \;\Rightarrow\; f(x) \approx_E f(y) .$$

+-- {: .num_defn #UniformlyContinuous}
###### Definition

The family $\mathcal{F}$ is __uniformly continuous__ if each member is [[uniformly continuous function|uniformly continuous]]:  For each [[entourage]] $E$ in $Y$, for each function $f$ in $\mathcal{F}$, for some entourage $D$ in $X$, for each [[point]] $x$ in $X$, for each point $y$ in $X$, whenever $x \approx_D y$, we have $f(x) \approx_E f(y)$.
=--

In short:
$$ \forall E,\; \forall f,\; \exists D,\; \forall x,\; \forall y,\; x \approx_D y \;\Rightarrow\; f(x) \approx_E f(y) .$$

+-- {: .num_defn #Equicontinuous}
###### Definition

The family $\mathcal{F}$ is __equicontinuous__ if:  For each [[entourage]] $E$ in $Y$, for each [[point]] $x$ in $X$, for some entourage $D$ in $X$, for each function $f$ in $\mathcal{F}$, for each point $y$ in $X$, whenever $x \approx_D y$, we have $f(x) \approx_E f(y)$.
=--

In short:
$$ \forall E,\; \forall x,\; \exists D,\; \forall f,\; \forall y,\; x \approx_D y \;\Rightarrow\; f(x) \approx_E f(y) .$$

+-- {: .num_defn #UniformlyEquicontinuous}
###### Definition

The family $\mathcal{F}$ is __uniformly equicontinuous__ if:  For each [[entourage]] $E$ in $Y$, for some entourage $D$ in $X$, for each function $f$ in $\mathcal{F}$ and each [[point]] $x$ in $X$, for each point $y$ in $X$, whenever $x \approx_D y$, we have $f(x) \approx_E f(y)$.
=--

In short:
$$ \forall E,\; \exists D,\; \forall f,\; \forall x,\; \forall y,\; x \approx_D y \;\Rightarrow\; f(x) \approx_E f(y) .$$

All of these definitions are identical except for the placement of the [[quantifiers]] $\forall f$ and $\forall x$ before or after the quantifier $\exists D$.

Just as it is reasonable to speak of a single function $f$ continuous at a single point $x$, so it is reasonable to speak of a family equicontinuous at a single point $x$ (or, for that matter, of a single function $f$ uniformly continuous).  However, it makes no sense to speak of a single function $f$ equicontinuous (or uniformly equicontinuous), nor can we speak of a family of functions uniformly equicontinuous at a single point $x$.


## Properties

### Cauchy sum theorem

The [[Cauchy sum theorem]] holds for an equicontinuous family of functions (from the [[real line]] to itself), *without* the requirement for [[uniform convergence]].


### Arzela-Ascoli theorem 

The importance of equicontinuity is perhaps best illustrated by the Arzel&#224;-Ascoli theorem, which gives conditions for a set in a [[exponential law for spaces|function space]] to be compact. A reasonably general version is this: 

+-- {: .num_theorem} 
###### Theorem 
Let $X$ be a [[convergence space]] and $Y$ a [[uniform space]]. Then a subset $F \subseteq C(X, Y)$ is [[relatively compact subspace|relatively compact]] (has compact closure) iff it is equicontinuous and $\{f(x):\; f \in F\}$ is relatively compact in $Y$ for each $x \in X$. 
=-- 

See [BB, corollary 2.4.9](#BB). Here the topology on the space $C(X, Y)$ of continuous functions $X \to Y$ is the so-called _natural topology_, namely the largest topology on $C(X, Y)$ such that for all spaces $A$, the continuity of a map $g: A \times X \to Y$ implies the continuity of its transpose $\hat{g}: A \to C(X, Y)$. This is the same as the exponential in $Top$ whenever the exponential exists. See [Escard&#243;, sections 8.1 and 10.2](#Es); see also [ELS](#ELS) where it is shown that the natural topology on $C(X, Y)$ coincides with the topology of continuous convergence (which is the context for the theorem above). 

(Some applications of Arzela-Ascoli should also be given.) 


### Representability

It happens that the property of a family of functions being (uniformly) equicontinuous is equivalent to them defining a single function which is (uniformly) continuous.

Recall that for a family of functions $f_i : A \to B$ for $i \in I$, we can define a function $\hat f : A \to B^I$ by $\hat f(a)(i) = f_i(a)$, and that the $f_i$ are all (uniformly) continuous iff $\hat f$ is (uniformly) continuous when $B^I$ is given the product uniformity.

However, we can give $B^I$ another uniformity more analogous to the [[box topology]] of topological spaces. Specifically, the box power $B^{\square I}$ is the uniform space with point set $B^I$, and where $E \subseteq B^I \times B^I$ is an entourage iff there is some entourage $G$ on $B$ such that for all $f \sim_E g$ in $B^I$ and all $i \in I$, $f(i) \sim_G g(i)$. This means that the entoruages of $B^{\square I}$ are generated by $G^I$ for entourages $G$ on $B$.

With this definition, we can see that the family of functions $f_i : A \to B$ is (uniformly) equicontinuous iff $\hat f : A \to B^{\square I}$ is (uniformly) continuous.

This also gives a convenient way to show that an equicontinuous net of continuous functions which converge pointwise converges to a continuous function: a net of equicontinuous functions $f_d : A \to B$ gives a continuous function $A \to B^{\square D}$. By the below proposition, if the $f_d$ converge pointwise, they converge to a continuous function.

+-- {: .num_prop} 
###### Proposition

Let $B$ be a separated uniform space and $D$ a directed set, let $conv(D,B)$ be the subspace of $B^{\square D}$ which contains the convergent nets. Then the map $lim : conv(D,B) \to B$ which takes a net to the point it converges to is continuous.
=-- 

+-- {: .proof}
###### Proof

Let $M$ in $conv(D,B)$ and $lim M \in U \subset B$ be open. Then there is an entourage $E$ on $B$ such that $ (E \circ E)[lim M] \subset U $. $E^D[M] := \{N \mid \forall i. M(i) \sim_E N(i) \} \subset conv(D,B)$ is a neighbourhood of $M$. For any $N \in E^D[M]$, we have that $lim N \in \widebar{E[lim M]}$ (as all $N(i)$ are in this closed set), so $lim N \in \widebar{E[x]} \subseteq \(E \circ E)[x] \subseteq U$. This means that $lim$ is continuous at $M$, as required.

=--


## References

* Wikipedia, _[Equicontinuity](http://en.wikipedia.org/wiki/Equicontinuity)_ 

* R. Beattie and H.-P. Butzmann, _Convergence Structures and Applications to Functional Analysis_, Kluwer Academic Publishers (2002). 
 {#BB} 

* Mart&#237;n Escard&#243;, _Synthetic topology of data types and classical spaces_, Electronic Notes in Theor. Comp. Sci. (2004). ([pdf](http://www.cs.bham.ac.uk/~mhe/papers/barbados.pdf)) 
 {#Es} 

* Mart&#237;n Escard&#243;, Jimmie Lawson, and Alex Simpson, _Comparing cartesian closed categories of (core) compactly generated spaces_, Topology and its Applications Vol. 143 Iss. 1-3 (2004), 105-145. ([web](http://www.sciencedirect.com/science/article/pii/S0166864104000550)) 
 {#ELS}


[[!redirects equicontinuous family]]
[[!redirects equicontinuous families]]
[[!redirects equicontinuous family of functions]]
[[!redirects equicontinuous families of functions]]
[[!redirects equicontinuous family of maps]]
[[!redirects equicontinuous families of maps]]

[[!redirects equicontinuous collection]]
[[!redirects equicontinuous collections]]
[[!redirects equicontinuous collection of functions]]
[[!redirects equicontinuous collections of functions]]
[[!redirects equicontinuous collection of maps]]
[[!redirects equicontinuous collections of maps]]

[[!redirects equicontinuous sequence]]
[[!redirects equicontinuous sequences]]
[[!redirects equicontinuous sequence of functions]]
[[!redirects equicontinuous sequences of functions]]
[[!redirects equicontinuous sequence of maps]]
[[!redirects equicontinuous sequences of maps]]

[[!redirects equicontinuous function]]
[[!redirects equicontinuous functions]]
[[!redirects equicontinuous map]]
[[!redirects equicontinuous maps]]


[[!redirects uniformly equicontinuous family]]
[[!redirects uniformly equicontinuous families]]
[[!redirects uniformly equicontinuous family of functions]]
[[!redirects uniformly equicontinuous families of functions]]
[[!redirects uniformly equicontinuous family of maps]]
[[!redirects uniformly equicontinuous families of maps]]

[[!redirects uniformly equicontinuous collection]]
[[!redirects uniformly equicontinuous collections]]
[[!redirects uniformly equicontinuous collection of functions]]
[[!redirects uniformly equicontinuous collections of functions]]
[[!redirects uniformly equicontinuous collection of maps]]
[[!redirects uniformly equicontinuous collections of maps]]

[[!redirects uniformly equicontinuous sequence]]
[[!redirects uniformly equicontinuous sequences]]
[[!redirects uniformly equicontinuous sequence of functions]]
[[!redirects uniformly equicontinuous sequences of functions]]
[[!redirects uniformly equicontinuous sequence of maps]]
[[!redirects uniformly equicontinuous sequences of maps]]

[[!redirects uniformly equicontinuous function]]
[[!redirects uniformly equicontinuous functions]]
[[!redirects uniformly equicontinuous map]]
[[!redirects uniformly equicontinuous maps]]