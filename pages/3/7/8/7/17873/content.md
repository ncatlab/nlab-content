
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Cohesion
+-- {: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A **sufficiently cohesive topos** is a [[topos]] that has enough connected objects in the sense that every object embeds into a [[connected object]].

This can be viewed as a strong form of [[cohesive topos|cohesiveness]] in the context of [[William Lawvere|Lawvere's]] axiomatic approach to [[gros toposes]]. In fact, in Lawvere ([1986](#Law86)) a big topos of spaces was  defined as (one equivalent to) a sufficiently cohesive topos.

## Terminology

Sufficient cohesion is a relative concept and requires minimally the presence of an [[essential geometric morphism]] $p:\mathcal{E}\to\mathcal{S}$. Here we state it for an [[adjoint quadruple]] between toposes 

$$p_!\dashv p^* \dashv p_* \dashv p^!:\mathcal{S}\to\mathcal{E}$$

such that $p^!$ (and hence $p^\ast$) is [[fully faithful]] and $p_!$ preserves [[finite products]].

This (and $\mathcal{E}$ in particular) is called a 'cohesive topos' (over $\mathcal{S}$) at _[[cohesive topos]]_, and will be referred to as a _'weakly cohesive topos'_ in the present entry - a sufficiently cohesive topos in this context corresponds to the three axioms (0-2) for a 'gros topos' in Lawvere ([1986](#Law86)) where the concept of sufficient cohesion was considered for the first time. 

A weakly cohesive topos is called _pre-cohesive_ if $p$ furthermore satisfies the [[Nullstellensatz]] i.e. the canonical map $\theta:p_\ast\to p_!$ is an epimorphism. This is the situation explored in Menni ([2014a](#Menni14a), [2014b](#Menni14b)).

A pre-cohesive topos that moreover satisfies the _continuity principle_ that $p_!(X^{p^\ast(Y)})\simeq p_!(X)^{Y}$ natural in $X\in\mathcal{E}$, $Y\in\mathcal{S}$, is called _'cohesive'_ in Lawvere ([2007](#Law07)) where the term 'sufficently cohesive' occurs for the first time although the notion is defined in a more restricted environment than the earlier papers (cf. Lawvere [1986](#Law86), [1992](#Law92), [1999](#Law99)).

## Definitions

+-- {: .num_defn #Contractible_object}
###### Definition 
An object $X$ in a weakly cohesive topos $p:\mathcal{E}\to\mathcal{S}$ is called _[[contractible object|contractible]]_ if for every object $Y\in\mathcal{E}$: $p_!(X^Y)=1$. 
=--

+-- {: .num_remark}
###### Remark
In particular, a contractible object is connected: $p_!(X)=p_!(X^1)=1$. Since exponentiation $(-)^Y$ preserves $1$ in any Cartesian closed category, the terminal object is contractible in any weakly cohesive topos.
=--

+-- {: .num_defn #Sufficient_Cohesion}
###### Definition 
A weakly cohesive topos $p:\mathcal{E}\to\mathcal{S}$ is called _sufficiently cohesive_ if the [[subobject classifier]] $\Omega\in\mathcal{E}$ is contractible i.e. $p_!(\Omega^X)=1$ for every object $X\in\mathcal{E}$ or, in other words, if all [[power object|power objects]] are connected. 
=--

+-- {: .num_remark}
###### Remark
Since in general, every object $X$ embeds into its power object via the singleton map $\{\}:X\rightarrowtail\Omega^X$ it follows that in a sufficiently cohesive topos $\mathcal{E}$ every object embeds into a [[connected object]] i.e. $\mathcal{E}$ has _enough connected objects_.

Furthermore, since in a [[Cartesian closed category]]
$$(X^Y)^Z\simeq X^{(Y\times Z)}\simeq X^{(Z\times Y)}\simeq (X^Z)^Y$$
one sees that in a sufficiently cohesive topos power objects $\Omega^X$ are not only connected but even contractible:
$$p_!((\Omega^X)^Z)=p_!(\Omega^{X\times Z})=1$$
and hence it follows that in a sufficiently cohesive topos _every object embeds into a contractible object_.

Conversely, if every power object $\Omega^X$ embeds into a connected object then the power objects $\Omega^X$ will be connected themselves by proposition \ref{connected_retract} below since power objects are injective in general. Whence a topos is sufficiently cohesive iff every object embeds into a connected object iff every object embeds into a contractible object. The last formulation is taken as the definition of sufficient cohesion in Lawvere ([2007](#Law07)).
=--

+-- {: .num_remark}
###### Remark
The definition of sufficient cohesion by 'having enough contractible objects' (Lawvere [2007](#Law07)) has of course the advantage that it even works in the wider context of Cartesian closed [[extensive category|extensive categories]] that lack a subobject classifier. The definition by 'having enough connected objects' would be feasible for merely [[distributive category|distributive categories]] that are not necessarily Cartesian closed (cf. Lawvere [1991](#Law91a), [1992](#Law92)) but Lawvere ([1991](#Law91a), p.4) suggests that in this case the definition should be strenghtened to demand that every object is the equaliser of a pair of maps between two connected objects.
=--

## Properties

Let us first record some easy but useful facts concerning the interplay between connectedness and constancy.

Recall that in a category with a terminal object a morphism $c:X\to Y$ is called _constant_ if $c$ factors through the [[terminal object]] $1$:
$$X\overset{c}{\to} Y=X\overset{!_X}{\to}1\overset{c_\ast}{\to} Y\quad .$$

+-- {: .num_prop #constant_identity}
###### Observation
An object $X$ is a terminal object iff $id_X$ is constant.
=--

**Proof**. "$\Leftarrow$": By assumption $id_X=(id_X)_\ast\circ !_X$. Since $X$ has a point $(id_X)_\ast$ there exists for every object $Z$ at least one map $Z\to X$. Suppose then that $f$ is some map $Z\to X$:

$$f=id_X\circ f=(id_X)_\ast\circ !_X\circ f=(id_X)_\ast\circ !_Z\quad .$$

But the righthand side does not depend on $f$ hence it is the only map $Z\to X$. $\qed$

+-- {: .num_prop #constant_homotopy}
###### Observation
Let $X$ be an object in a weakly cohesive topos and $c:X\to X$ be a constant endomap such that $p_!(c)=p_!(id_X)$. Then $X$ is connected i.e. $p_!(X)=1$.
=--

**Proof**. Since by assumption $p_!(1)=1$, $p_!(c)$ and, accordingly, $p_!(id_X)=id_{p_!(X)}$ are constants. $\qed$

+-- {: .num_prop #connected_retract}
###### Observation
In a weakly cohesive topos, retracts of connected objects are connected themselves.
=--

**Proof**. Let $X$ be a retract of $Y$ with $p_!(Y)=1$. Then $id_X$ factors as $X\rightarrowtail Y\to X$ and applying $p_!$ shows that $id_{p_!(X)}$ factors through the terminal object $p_!(Y)$. $\qed$

Since in general, injective objects $I$ are retracts of the objects $X$ that they embed into because such inclusions $I\rightarrowtail X$ factor through $id_I$ by injectivity, it follows that in a weakly cohesive topos _injective objects that embed into a connected object are connected_ themselves.

In particular, _all_ injective objects are connected in a sufficiently cohesive topos. Since power objects are injective in general one gets the converse as well:

+-- {: .num_prop #sufficient_injective}
###### Proposition
A weakly cohesive topos is sufficiently cohesive iff all injective objects are connected. $\qed$
=--

## Cohesively connected truth

In a sufficiently cohesive topos the subobject classifier is obviously connected since $\Omega=\Omega^1$. It is the aim of this section to prove that in a weakly cohesive topos the converse holds as well: $\Omega$ is connected iff $\Omega$ is contractible.

Before embarking on a proof let us consider two examples that illustrate that the concept of sufficient cohesion results from the interplay between the _connectedness_ of the subobject classifier and the _exactness_ properties of the components functor $p_!$:

+-- {: .num_example}
###### (Non)examples
The [[Sierpinski topos]] $Set^\to$ is weakly cohesive over $Set$ since there exists a string of adjoint functors $L\dashv\Pi\dashv\Delta\dashv\Gamma\dashv B: Set\to Set^\to$ with 

* $L(Z)=\emptyset \to Z$

* $\Pi(X\to Y) = Y$

* $\Delta(Z)=Z\overset{id}{\to} Z$

* $\Gamma (X\to Y) = X$

* $B(Z)=Z\to 1$.

The Nullstellensatz fails as does the continuity principle. As a right adjoint $\Pi$ preserves all limits and the terminal object in particular whence $1$ is connected in $Set^\to$. Since the underlying category $\to$ satisfies the [[Ore condition]] trivially, it follows then from a general result[^bouquet] of Lawvere that $\Omega$ is not connected[^bouquet] and, accordingly, that the _Sierpinski topos is not sufficiently cohesive!_

On the other hand, the topos of [[quiver|quivers]] $Set^\rightrightarrows$ has a connected subobject classifier but lacks the right adjoint $B$ nor does its connected components functor $\Pi$ preserve finite products. $\qed$
=--

[^bouquet]: (Theorem 12.2.3 in La Palme Reyes et al. ([2004](#RRZ04), p.221)). Of course, this can also easily be proved directly or read off the concrete objects and properties worked out in La Palme Reyes et al. (2004) where the Sierpinski topos is called the category of bouquets.

Recall that in any topos, the subobject classifier $\Omega$ has two points $\mathsf{true},\mathsf{false}$ fitting into the following pullback diagram (which is an equaliser diagram as well) due to the classifying property of $\Omega$ for the monomorphism $0\to 1$:

$$
\array{
0 &\to & 1 
\\
\downarrow & &\downarrow\mathsf{true}
\\
1 &\underset{\mathsf{false}}{\to} &\Omega
}
$$

In a sufficiently cohesive topos $\Omega$ is furthermore connected whence together with its [[Heyting algebra|Heyting algebra structure]] we can view it as a generalized (non linear) "interval" object:

+-- {: .num_defn #connector}
###### Definition 
An object $T$ in a weakly cohesive topos is called a _(cohesive) connector_ if $p_!(T)=1$ and $T$ has two points $t_0,t_1:1\to T$ with empty [[equaliser]]: $0\overset{e}{\to} 1\overset{t_0}{\underset{t_1}{\rightrightarrows}} T$.
=--

In a topos with a connected subobject classifier $\Omega$ itself is a connector. Conversely the existence of a connector implies the connectedness of $\Omega$:

+-- {: .num_prop #connecting_truth}
###### Proposition
Let $\mathcal{E}$ be weakly cohesive topos. $\mathcal{E}$ has a connector $T$ iff $p_!(\Omega)=1$.
=--

**Proof**.
"$\Rightarrow$": Let $1\overset{t_0}{\underset{t_1}{\rightrightarrows}} T$ be a connector. Then $t_1:1\to T$ is a subobject with characteristic map $\chi_1:T\to\Omega$. Consider the two composites $\chi_1\circ t_i$ , $i=0,1$:

For $i=1$ this simply yields $\mathsf{true}$ by the definition of $\chi_1$.

For $i=0$ we claim that $\chi_1\circ t_0=\mathsf{false}$ since we have the following diagram:

$$
\array{
0 &\to & 1 &\to & 1 
\\
\downarrow & &t_1\downarrow& & \downarrow \mathsf{true}
\\
1&\underset{t_0}{\to} &T&\underset{\chi_1}{\to}&\Omega
}
$$

Here the left square is a pullback since $t_o,t_1$ have empty equaliser by assumption. The right square is a pullback since it classifies $t_1$ whence the outer square is a pullback too. Therefore $\chi_1\circ t_0$ classifies $0\to 1$ which is exactly the definition of $\mathsf{false}$. 

Since $p_!(T)$ is terminal $p_!(t_0)=p_!(t_1)$. Whence
$$p_!(\mathsf{true})=p_!(\chi_1\circ t_1)=p_!(\chi_1)\circ p_!(t_1)=p_!(\chi_1)\circ p_!(t_0)=p_!(\chi_1\circ t_0)=p_!(\mathsf{false})\quad$$

This says that $\mathsf{true}$ and $\mathsf{false}$ are in the same connected component but a lattice whose top and bottom elements are in the same component is necessarily connected. $\qed$

One can use connectors to define a (generalized) homotopy relation between maps that behaves well under taking connected components.

+-- {: .num_defn #I-homotopy}
###### Definition 
Let $I$ be a connector. Two parallel maps $f,g:A\to B$ are called _I-homotopic_, in signs: $f\sim_I g$, if there exists a map $h:A\times I\to B$ with the property that
$$f=h\circ\langle id_A, t_0\circ !_A\rangle\quad and\quad g=h\circ\langle id_A, t_1\circ !_A\rangle\quad.$$
(In this case, $h$ is also called an (I-)homotopy between $f$ and $g$.)
=--

The following result brings together the two crucial ingredients for the equivalence between contractability and connectedness of $\Omega$, namely, the preservation of finit products by $p_!$ and $p_!(\Omega)=1$.

+-- {: .num_prop #homotopy_components}
###### Proposition
Let $f=h\circ\langle i, k_1\rangle$ and $g=h\circ\langle i, k_2\rangle$ be a pair of parallel maps in a weakly cohesive topos with the property that $p_!(k_1)=p_!(k_2)$. Then $p_!(f)=p_!(g)$. In particular, $f\sim_I g$ implies $p_!(f)=p_!(g)$.
=--

**Proof**. Since $p_!$ preserves finite products it maps product diagrams to product diagrams whence
$$p_!(h\circ\langle i, k_j\rangle)=p_!(h)\circ p_!(\langle i, k_j\rangle)=p_!(h)\circ \langle p_!( i), p_!(k_j)\rangle\quad,\quad j\in\{1,2\}$$
but these two maps coincide since $p_!(k_1)=p_!(k_2)$ by assumption.

Since for an I-homotopy $k_j=t_j\circ !_A:A\to I$ and, $p_!(I)=1$ by assumption, $p_!(k_j):p_!(A)\to 1$, $j\in\{1,2\}$, and these maps necessarily coincide since $1$ is terminal whence $p_!(t_0\circ !_A)=p_!(t_1\circ !_A)$ whence $p_!(f)=p_!(g)$ as claimed. $\qed$

For the following the monoid structure of $\Omega$ will become important. So let us briefly review the basics:

In a general topos, the Heyting algebra structure endows the subobject classifier with the structure of an [[internal monoid]]: The multiplication is given by conjunction

$$\Omega\times\Omega\overset{\wedge}{\to}\Omega\quad ,
\text{ and the unit by }\quad 1\overset{\mathsf{true}}{\to}\Omega\quad .
$$
The conjunction $\wedge$ is defined as the characteristic map of $1\xrightarrow{\langle\mathsf{true},\mathsf{true}\rangle}\Omega\times\Omega$.

Importantly, the other truth value $1\xrightarrow{\mathsf{false}}\Omega$ plays the role of a (multiplicative) _zero_ with respect to this multiplication.

For the following we need

+-- {: .num_prop #omega_homotopy}
###### Proposition
Let $\mathcal{E}$ be a weakly cohesive topos whose subobject classifier is a connector i.e. $p_!(\Omega)=1$. Then the conjunction $\wedge :\Omega\times\Omega{\to}\Omega$ is an $\Omega$-homotopy from $id_{\Omega}$ to the constant map $\mathsf{false}\circ !_\Omega$.
=--

**Proof**.
We have to show that $\wedge\circ\langle id_\Omega, \mathsf{true}\circ !_\Omega\rangle=id_\Omega$ and $\wedge\circ\langle id_\Omega, \mathsf{false}\circ !_\Omega\rangle=\mathsf{false}\circ !_\Omega$. This is more or less clear from the propositional structure of $\Omega$ but let us spell out the details diagrammtically:

For the first equation, consider the commutative diagram:
$$
\array{
1 &\to & 1
\\
{}_\mathsf{true}\downarrow & &\downarrow_{\langle\mathsf{true},\mathsf{true}\rangle}
\\
\Omega &\xrightarrow{\langle id_\Omega,\mathsf{true}\circ !_\Omega\rangle}&\Omega\times\Omega
}
$$
This pullback pasted to the classifying pullback diagram for $\langle\mathsf{true},\mathsf{true}\rangle$ displays $\wedge\circ\langle id_\Omega, \mathsf{true}\circ !_\Omega\rangle$ as the characteristic map of $\mathsf{true}$ which of course is none other than $id_\Omega$.

For the second, consider the following pullback:
$$
\array{
X &\xrightarrow{!_X} & 1
\\
{}_{\mathsf{true}\circ !_X}\downarrow & &\downarrow_{\langle\mathsf{true},\mathsf{true}\rangle}
\\
\Omega &\xrightarrow{\langle id_\Omega,\mathsf{false}\circ !_\Omega\rangle }&\Omega\times\Omega
}
$$
Chasing the arrows around in the second component yields the equation
$$\mathsf{true}\circ !_X=\mathsf{false}\circ !_\Omega\circ\mathsf{true}\circ !_X=\mathsf{false}\circ !_X$$
but this implies $X=0$ since it corresponds to  the pullback of $\mathsf{true}$ and $\mathsf{false}$. Hence the pasted

$$
\array{
0 &\xrightarrow{!_0} & 1 &\to & 1
\\
\downarrow & &\downarrow_{\langle\mathsf{true},\mathsf{true}\rangle}& &\downarrow _\mathsf{true}
\\
\Omega &\xrightarrow{\langle id_\Omega,\mathsf{false}\circ !_\Omega\rangle }&\Omega\times\Omega&\xrightarrow{\wedge}&\Omega
}
$$

is the classifying pullback of $0\rightarrowtail\Omega$. Since it is easily seen that $\mathsf{false}\circ !_\Omega$ is also the characteristic map of $0\rightarrowtail\Omega$ the claim follows. $\qed$

+-- {: .query}
The rest of this section is intended to provide a proof of theorem \ref{connected_truth} below. The claims and proofs in it should be taken with caution by the reader (at least) until they have reached a final form!
=--

In order to show that the connectedness of $\Omega$ implies its contractibility we will now lift this $\Omega$-homotopy between $id_\Omega$ and a constant map $\Omega\to\Omega$ to a $\Omega$-homotopy between $id_{\Omega^X}$ and a constant map $\Omega^X\to\Omega^X$.

+-- {: .num_prop #homotopy_lifting}
###### Proposition
Let $\mathcal{E}$ be a weakly cohesive topos with connector $1\overset{t_0}{\underset{t_1}{\rightrightarrows}} T$. Suppose that $m:X\times T\to X$ is a $T$-homotopy between $id_X$ and a constant map $c:X\to X\,$.Then there exists for every object $Y$ a $T$-homotopy $\mu:X^Y\times T\to X^Y$ from $id_{X^Y}$ to a constant endomap $X^Y\to X^Y$.
=--
**Proof**.
 We get $\mu$ from $X\times T \overset{m}{\to}  X$ as follows
$$
\begin{aligned}
X& \to X^{T}\quad\text{by transposal}
\\ 
X^Y&\to (X^{T})^{Y}\quad\text{by application of the endofunctor (-)}^Y
\\
X^Y &\to (X^Y)^{T}\quad\text{by using rules for powers}
\\
X^Y\times T&\overset{\mu}{\to}X^Y\quad \text{by reversing transposal .}
\end{aligned}
$$
In order to see that $\mu$ satisfies the two homotopy boundary conditions at $t_0,t_1$
$$\mu\circ\langle id_{X^Y},t_0\circ !_{X^Y}\rangle = id_{X^Y}\quad\text{and} 
\quad \mu\circ\langle id_{X^Y},t_1\circ !_{X^Y}\rangle =\text{const.}$$

consider the following commutative diagram:
$$
\array{
X &\xleftarrow{ev_{T{}X}}&X^T\times T &\xrightarrow{ev_{T{}X}} &X
\\
{}_{id_X}\negmedspace\uparrow &\underset{m}{\nwarrow}&\uparrow_{\lceil{m}\rceil\times id_T}& \underset{m}\nearrow&\uparrow_c
\\
X&\xrightarrow[\langle id_X,t_0\circ !_X\rangle]{}&X\times T&\xleftarrow[\langle id_X,t_1\circ !_X\rangle]{}&X
}
$$
This encapsulates all the information before the application of $(-)^Y$: the transpose of the second step occurs as $\lceil{m}\rceil$ and the homotopy information is expressed via $\lceil{m}\rceil$ by using $ev_{T{}X}\circ(\lceil{m}\rceil\times id_T)=m$ at $t_0,t_1$.

Now we exponentiate the diagram. Importantly, $(-)^Y$ as a right adjoint preserves all limits and therefore it maps the constant map $c:X\to X$ to a _constant_ map $c^Y:X^Y\to X^Y$ which has the form $c^Y=\lceil{c\cdot ev_{Y{}X}}\rceil$ !

This yields a map $\lceil{m}\rceil^Y:X^Y\to (X^T)^Y$ such that $\lceil{m}\rceil^Y=\lceil{\lceil{m}\rceil\cdot ev_{Y{}X}}\rceil$ whence $ev_{Y{}X^T}(\lceil{m}\rceil^Y\times id_Y)=\lceil{m}\rceil\cdot ev_{Y{}X}$.

Now we want to prolongate $\lceil{m}\rceil^Y:X^Y\to (X^T)^Y$ by an isomorphism $(X^T)^Y\xrightarrow{\simeq} (X^Y)^T$.

We get this isomorphism from the following sequence of maps

$$
\begin{aligned}
 ((X^T)^Y\times T)\times Y&\xrightarrow{\langle \pi_1\pi_1,\langle \pi_2\pi_1,\pi_2\rangle\rangle}& (X^T)^Y\times (T\times Y)
\\
 (X^T)^Y\times (T\times Y)&\xrightarrow{id_{(X^T)^Y}\times \tau_{T{}Y}}&(X^T)^Y\times(Y\times T) 
\\
 (X^T)^Y\times (Y\times T)&\xrightarrow{\langle\langle\pi_1,\pi_1\pi_2\rangle,\pi_2\pi_2\rangle}& ((X^T)^Y)\times Y)\times T
\\
((X^T)^Y)\times T&\xrightarrow{ev_{Y{}X^T}\times id_T}& X^T\times T
\\
X^T\times T &\xrightarrow{
ev_{T{}X}} & X
\end{aligned}
$$

....

$$
\array{
X^Y &\xleftarrow{ev^Y}&(X^T)^Y\times T^Y &\xrightarrow{ev^Y} &X^Y
\\
{}_{id_{X^Y}}\negmedspace\uparrow &\underset{m^Y}{\nwarrow}&\uparrow_{\hat{m}^Y\times id_{T^Y}}& \underset{m^Y}\nearrow&\uparrow_{c^Y}
\\
X^Y&\xrightarrow[\langle id_{X^Y},t_0^Y\circ !_{X^Y}\rangle]{}&X^Y\times T^Y&\xleftarrow[\langle id_{X^Y},t_1^Y\circ !_{X^Y}\rangle]{}&X^Y
}
$$


...

$\qed$

By prop. \ref{omega_homotopy} and the preceding the next is immediate:

+-- {: .num_prop #omega_action}
###### Corollary
Let $\mathcal{E}$ be a weakly cohesive topos whose subobject classifier is a connector. The $\Omega$-homotopy $\wedge :\Omega\times\Omega{\to}\Omega$ lifts to a $\Omega$-homotopy between $id_{\Omega^X}$ and a constant map $\Omega^X\to\Omega^X$. $\qed$
=--

+-- {: .num_remark}
###### Remark

In classical [[topology]], a space $X$ with the property that $id_X$ is homotopic to a constant map is called a [[contractible space]]. Hence  proposition \ref{homotopy_lifting} can be viewed as a synthetic internal avatar of the classical fact, that any two parallel maps into a contractible space $X$ are homotopic.

Pursuing this analogy, the preceding result shows that in a weakly cohesive topos with connected subobject classifier, the power object $\Omega^X$ of an object $X$ is akin to the [[cone]] $\mathbf{C}X$ of a topological space $X$ in providing a contractible object to embed into. In this perspective, one can think of a sufficiently cohesive topos as being equipped with a generalized cone construction.
=--

+-- {: .num_prop #connected_truth}
###### Theorem
Let $\mathcal{E}$ be a weakly cohesive topos. Then the subobject classifier $\Omega$ is connected iff $\Omega$ is contractible. In other words,  $\mathcal{E}$ is sufficiently cohesive iff $p_!(\Omega)=1$.
=--

**Proof**.
"$\Rightarrow$": The propositions \ref{omega_action} and \ref{homotopy_components} imply that for all $X$ $p_!(id_{\Omega^X})=id_{p_!(\Omega^X)}$ is a constant map. By observation \ref{constant_homotopy} it then follows that $p_!(\Omega^X)=1$ for all $X$ which is just the definition of $\Omega$ being contractible.
$\qed$

For convenience and summary let us collect all the equivalent formulations of sufficient cohesion in one place:

....

## Related entries

* [[cohesive topos]]

* [[Nullstellensatz]]

* [[quality type]]

* [[connected object]]

* [[injective object]]

## Link

* [nForum discussion thread](https://nforum.ncatlab.org/discussion/7562/sufficiently-cohesive-topos/#Item_0)

## References

* {#JS96}[[Peter Johnstone|P. Johnstone]], _Remarks on Quintessential and Persistent Localizations_ , TAC **2** no.8 (1996) pp.90-99. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf))

* {#J02} [[Peter Johnstone|P. Johnstone]], _Sketches of an Elephant vol. 1_ , Cambridge UP 2002. 

* {#JS11} [[Peter Johnstone|P. Johnstone]], _Remarks on Punctual Local Connectedness_ , TAC **25** no.3 (2011) pp.51-63. ([pdf](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* {#Law86} [[F. W. Lawvere]], _Categories of Spaces may not be Generalized Spaces as Exemplified by Directed Graphs_, Revista Colombiana de Matem&#225;ticas **XX** (1986) pp.179-186. Reprinted with commentary as TAC Reprint **9** (2005) pp.1-7. ([pdf](ftp://ftp.tac.mta.ca/tac/html/tac/reprints/articles/9/tr9.pdf))

* {#Law91a} [[F. W. Lawvere]], _Some Thoughts on the Future of Category Theory_ , pp.1-13 in Springer LNM **1488** (1991).

* {#Law92} [[F. W. Lawvere]], _Categories of Space and Quantity_, pp.14-30 in: J. Echeverria et al. (eds.), _The Space of Mathematics_ , de Gruyter Berlin 1992.

* {#Law99} [[F. W. Lawvere]], _Kinship and Mathematical Categories_ , pp.411-425 in: R. Jackendoff, P. Bloom, K. Wynn (eds.), _Language, Logic, and Concepts - Essays in Memory of John Macnamara_, MIT Press 1999.

* {#Law07} [[F. W. Lawvere]], _Axiomatic cohesion_ , TAC **19** no.3 (2007) pp.41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

* {#LawvereMenni15} [[F. W. Lawvere]], [[Matías Menni|M. Menni]], _Internal choice holds in the discrete part of any cohesive topos satisfying stable connected codiscreteness_, TAC **30** no. 26 (2015) pp.909-932. ([abstract](http://www.tac.mta.ca/tac/volumes/30/26/30-26abs.html))

* {#MarmoMenni16}F. Marmolejo, [[Matías Menni|M. Menni]], _On the relation between continuous and combinatorial_ , arXiv:1602.02826 (2016). ([abstract](http://arxiv.org/abs/1602.02826))

* {#Menni14a} [[Matías Menni|M. Menni]], _Sufficient Cohesion over Atomic Toposes_ , Cah. Top. G&#233;om. Diff. Cat. **LV** (2014). ([preprint](https://sites.google.com/site/matiasmenni/SufCohesion12.pdf?attredirects=0))

* {#Menni14b} [[Matías Menni|M. Menni]], _Continuous Cohesion over Sets_ , TAC **29** no.20 (2014) pp.542-568. ([pdf](http://www.tac.mta.ca/tac/volumes/29/20/29-20.pdf))

* {#Shulman15} [[Mike Shulman|M. Shulman]], _Brouwer's Fixed Point Theorem in Real-Cohesive Homotopy Type Theory_ , arXiv:1509.07584 (2015). ([abstract](http://arxiv.org/abs/1509.07584)) 


[[!redirects sufficiently cohesive topos]]
[[!redirects Sufficiently cohesive topos]]
[[!redirects sufficiently cohesive toposes]]
[[!redirects sufficiently cohesive topoi]]
[[!redirects sufficiently cohesive]]
[[!redirects sufficient cohesion]]
[[!redirects Sufficient Cohesion]]