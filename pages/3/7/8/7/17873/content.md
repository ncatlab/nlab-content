
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Cohesion
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}
[[!redirects Sufficiently cohesive topos]]
[[!redirects contractible object]]
[[!redirects sufficient cohesion]]
[[!redirects sufficiently cohesive toposes]]
[[!redirects Sufficient Cohesion]]

## Idea

A **sufficiently cohesive topos** is a [[topos]] that has enough connected objects in the sense that every object embeds into a [[connected object]]. This can be viewed as a strong form of [[cohesive topos|cohesiveness]] in the context of [[William Lawvere|Lawvere's]] axiomatic approach to [[gros toposes]].

## Terminological preliminaries

Sufficient cohesion is a relative concept and requires minimally the presence of an [[essential geometric morphism]] $p:\mathcal{E}\to\mathcal{S}$. Here we state it for an [[adjoint quadruple]] $p_!\dashv p^* \dashv p_* \dashv p^!:\mathcal{S}\to\mathcal{E}$ such that $p^!$ (and hence $p^\ast$) is [[fully faithful]] and $p_!$ preserves [[finite products]].

This (and $\mathcal{E}$ in particular) is called a 'cohesive topos' (over $\mathcal{S}$) at _[[cohesive topos]]_, and will be referred to as a _'weakly cohesive topos'_ in the present entry - a sufficiently cohesive topos in this context corresponds to the three axioms (0-2) for a 'gros topos' in Lawvere ([1986](#Law86)) where the concept of sufficient cohesion was considered for the first time. 

A weakly cohesive topos is called _pre-cohesive_ if $p$ furthermore satisfies the [[Nullstellensatz]] i.e. the canonical map $\theta:p_\ast\to p_!$ is an epimorphism. This is the situation explored in Menni ([2014a](#Menni14a), [2014b](#Menni14b)).

A pre-cohesive topos that furthermore satisfies the _continuity principle_ that $p_!(X^{p^\ast(Y)})\simeq p_!(X)^{Y}$ natural in $X\in\mathcal{E}$, $Y\in\mathcal{S}$, is called _'cohesive'_ in Lawvere ([2007](#Law07)) where the term 'sufficently cohesive' occurs for the first time although the notion is defined in a more restricted environment than the earlier papers (cf. Lawvere [1986](#Law86), [1992](#Law92), [1999](#Law99)).

## Definitions

+-- {: .num_defn #Contractible_object}
###### Definition 
An object $X$ in a weakly cohesive topos $p:\mathcal{E}\to\mathcal{S}$ is called _contractible_ if for every object $Y\in\mathcal{E}$: $p_!(X^Y)=1$. 
=--

+-- {: .num_remark}
###### Remark
In particular, a contractible object is connected: $p_!(X)=p_!(X^1)=1$.
=--

+-- {: .num_defn #Sufficient_Cohesion}
###### Definition 
A weakly cohesive topos $p:\mathcal{E}\to\mathcal{S}$ is called _sufficiently cohesive_ if the [[subobject classifier]] $\Omega\in\mathcal{E}$ is contractible i.e. $p_!(\Omega^X)=1$ for every object $X\in\mathcal{E}$ or, in other words, if all [[power object|power objects]] are connected. 
=--

+-- {: .num_remark}
###### Remark
Since in general, every object $X$ embeds into its power object via the singleton map $\{\}:X\rightarrowtail\Omega^X$ it follows that in a sufficiently cohesive topos $\mathcal{E}$ every object embeds into a [[connected object]] i.e. $\mathcal{E}$ has _enough connected objects_.

Furthermore, since in a [[Cartesian closed category]] $X^{(Y\times Z)}\simeq(X^Y)^Z$ one sees that in a sufficiently cohesive topos power objects $\Omega^X$ are not only connected but even contractible: $p_!((\Omega^X)^Z)=p_!(\Omega^{X\times Z})=1$ and hence it follows that in a sufficiently cohesive topos every object embeds into a contractible object.

Conversely, if every power object $\Omega^X$ embeds into a connected object then the power objects $\Omega^X$ will be connected themselves by proposition \ref{connected_retract} below since power objects are injective in general. Whence a topos is sufficiently cohesive iff every object embeds into a connected object iff every object embeds into a contractible object. The last formulation is taken as the definition of sufficient cohesion in Lawvere ([2007](#Law07)).
=--

## Properties

+-- {: .num_prop #connected_retract}
###### Proposition
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

In a sufficiently cohesive topos the subobject classifier is obviuosly connected since $\Omega=\Omega^1$. It is the aim of this section to prove that in a weakly cohesive topos the converse holds as well: $\Omega$ is connected iff $\Omega$ is contractible.

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

On the other hand, the topos of [[quiver|quivers]] $Set^\rightrightarrows$ has a connected subobject classifier but lacks the right adjoint $B$ nor does its connected components functor $\Pi$ preserve finite products.
=--

[^bouquet]: (Theorem 12.2.3 in La Palme Reyes et al. ([2004](#RRZ04), p.221)). Of course, this can also easily be proved directly or read off the concrete objects and properties worked out in La Palme Reyes et al (2004) where the Sierpinski topos is called the category of bouquets.

Recall that in any topos, the subobject classifier $\Omega$ has two points $\bot,\top$ fitting into the following pullback diagram (which is an equaliser diagram as well) due to the classifying property of $\Omega$:

$$
\array{
0 &\to & 1 
\\
\downarrow & &\downarrow\mathsf{T}
\\
1 &\underset{\bot}{\to} &\Omega
}
$$

In a sufficiently cohesive topos $\Omega$ is furthermore connected whence together with its [[Heyting algebra|Heyting algebra structure]] we can view it as a generalized (non linear) "interval" object:

+-- {: .num_defn #connector}
###### Definition 
An object $I$ in a weakly cohesive topos is called a _(cohesive) connector_ if $p_!(I)=1$ and $I$ has two points $t_0,t_1:1\to I$ with empty [[equaliser]]: $0\overset{e}{\to} 1\overset{t_0}{\underset{t_1}{\rightrightarrows}} I$.
=--

One can use connectors to define a (generalized) homotopy relation between maps that behaves well under taking connected components.

+-- {: .num_defn #I-homotopy}
###### Definition 
Let $I$ be a connector. Two parallel maps $f,g:A\to B$ are called _I-homotopical_, in signs: $f\sim_I g$, if there exists a map $h:A\times I\to B$ with the property that
$$f=h\circ\langle id_A, t_0\circ !_A\rangle\quad and\quad g=h\circ\langle id_A, t_1\circ !_A\rangle\quad.$$
(In this case, $h$ is also called an (I-)homotopy between $f$ and $g$.)
=--



(...
+-- {: .num_prop #homotopy_components}
###### Proposition
Let $f=h\circ\langle i, k_1\rangle$ and $g=h\circ\langle i, k_2\rangle$ be a pair of parallel maps in a weakly cohesive topos with the property that $p_!(k_1)=p_!(k_2)$. Then $p_!(f)=p_!(g)$ and this holds in particular if $h$ is a homotopy from $f$ to $g$.
=--
...)
...

## Related entries

* [[cohesive topos]]

* [[Nullstellensatz]]

* [[quality type]]

* [[connected object]]

* [[injective object]]

## References

* {#JS96}[[Peter Johnstone|P. Johnstone]], _Remarks on Quintessential and Persistent Localizations_ , TAC **2** no.8 (1996) pp.90-99. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf))

* {#JS11} [[Peter Johnstone|P. Johnstone]], _Remarks on Punctual Local Connectedness_ , TAC **25** no.3 (2011) pp.51-63. ([pdf](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))

* {#J02} [[Peter Johnstone|P. Johnstone]], _Sketches of an Elephant vol. 1_ , Cambridge UP 2002. 

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

* {#Shulman15} [[Mike Shulman|M. Shulman]], _Brouwer's Fixed Point Theorem in real-cohesive Homotopy Type Theory_ , arXiv:1509.07584 (2015). ([abstract](http://arxiv.org/abs/1509.07584)) 

[[!redirects empty 162]]
[[!redirects sufficiently cohesive toposes]]
[[!redirects sufficiently cohesive topoi]]
[[!redirects sufficiently cohesive]]
[[!redirects sufficient cohesion]]