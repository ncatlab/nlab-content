
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn}
###### Definition

A [[category]] $D$ is called __sifted__ if [[colimits]] of [[diagrams]] of shape $D$ [[commutativity of limits and colimits|commute]] with [[finite products]] in [[Set]]: for every [[diagram]]

$$
  F : D \times S \to Set
  \,,
$$

where $S$ is a [[finite category|finite]] [[discrete category]] the canonical morphism

$$
  ( \underset{\underset{d \in D}{\longrightarrow}}{\lim} \prod_{s \in S} F(d,s))
   \to
  \prod_{s \in S} \underset{\underset{d \in D}{\longrightarrow}}{\lim} F(d,s)
$$

is an [[isomorphism]].

[[formal dual|Dually]], $D$ is called **cosifted** if the [[opposite category]] $D^{op}$ is sifted.


=--

A colimit over a sifted diagram is called a [[sifted colimit]].




## Properties

### Characterizations

+-- {: .num_prop}
###### Proposition

An [[inhabited set|inhabited]] [[small category]] $D$ is sifted precisely if the [[diagonal]] functor 
  
$$
  D \to D \times D
$$

is a [[final functor]].

=--

This is due to ([GabrielUlmer](#GabrielUlmer))

More explicitly this means that:

+-- {: .num_prop}
###### Proposition

An [[inhabited set|inhabited]] [[small category]] is sifted if for every pair of objects $d_1,d_2\in D$, the category $Cospan_D(d_1,d_2)$ of [[cospans]] from $d_1$ to $d_2$ is [[connected category|connected]].

=--

+-- {: .num_cor}
###### Corollary

Every category with finite [[coproducts]] is sifted.

=--

+-- {: .proof}
###### Proof

Since a category with finite coproducts is nonempty (it has an [[initial object]]) and each category of cospans has an initial object (the coproduct).

=--

We make this special case more explicit below in Example \ref{CategoriesWithFiniteProductsAreCosifted}.

## Examples

+-- {: .num_example #ReflexiveCoequalizerDiagram}
###### Example

The [[diagram]] category for [[reflexive coequalizers]], $\{ 0 \stackrel{\overset{d_0}{\to}}{\stackrel{\overset{s_0}{\leftarrow}}{\underset{d_1}{\to}}} 1\}^{op}$ with $ s_0 \circ d_0 = s_0 \circ d_1 = id$, is sifted.

=--

+-- {: .num_example #BareParallelPairIsNotSifted}
###### Example 

The presence of the degeneracy map $s_0 \colon 1 \to 0$ in example \ref{ReflexiveCoequalizerDiagram} is crucial for the statement to work: the category $\{0 \stackrel{\overset{d_0}{\to}}{\underset{d_1}{\to}} 1\}^{op}$ is _not_ sifted; there is no way to connect the cospan $(d_0,d_0)$ to the cospan $(d_1,d_1)$.

=--

Example \ref{ReflexiveCoequalizerDiagram} may be thought of as a truncation of:

+-- {: .num_example}
###### Example

The [[opposite category]] of the [[simplex category]] is sifted.

=--

+-- {: .num_example}
###### Example

Every [[filtered category]] is sifted.

=--

+-- {: .proof}
###### Proof

Since [[filtered colimits]] commute even with all [[finite limits]] in Set, they in particular commute with [[finite products]].

=--

+-- {: .num_example #CategoriesWithFiniteProductsAreCosifted}
###### Example
**([[categories with finite products are cosifted]])**

Let $\mathcal{C}$ be a [[small category]] which has [[finite products]]. Then $\mathcal{C}$ is a _[[cosifted category]]_, equivalently its [[opposite category]] $\mathcal{C}^{op}$ is a _[[sifted category]]_, equivalently [[colimits]] over $\mathcal{C}^{op}$ with values in [[Set]] are _[[sifted colimits]]_, equivalently [[colimits]] over $\mathcal{C}^{op}$ with values in [[Set]] _[[limits commuting with colimits|commute]] with [[finite products]]_, as follows:

For $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ to [[functors]] on the [[opposite category]] of $\mathcal{C}$ (hence two [[presheaves]] on $\mathcal{C}$) we have a [[natural isomorphism]]

$$
  \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
  \left(
    \mathbf{X} \times \mathbf{Y}
  \right)
  \;\simeq\;
  \left(
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \mathbf{X}
  \right)
  \times
  \left(
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \mathbf{Y}
  \right)
  \,.
$$ 

=--


## Related concepts

* [[distributivity of products and colimits]]

* **sifted category**, [[sifted (∞,1)-category]]

* [[filtered category]], [[filtered (∞,1)-category]]

* [[direct category]]



## References

*  [[Pierre Gabriel]], Fritz Ulmer, _Lokal pr&#228;sentierbare Kategorien_ , LNM
**221**, Springer Heidelberg 1971.
{#GabrielUlmer}

*  [[Jiri Adamek]], [[Jiri Rosicky]], _On sifted colimits and generalized varieties_, TAC **8** (2001) pp.33-53. ([tac](http://www.tac.mta.ca/tac/volumes/8/n3/8-03abs.html))

*  [[Jiri Adamek]], [[Jiri Rosicky]], [[Enrico Vitale]], _What are sifted colimits?_, TAC __23__ (2010) pp. 251--260. ([tac](http://www.tac.mta.ca/tac/volumes/23/13/23-13abs.html))

* [[Jiri Adamek]], [[Jiri Rosicky]], [[Enrico Vitale]], _Algebraic Theories - a Categorical Introduction to General Algebra_ , Cambrige UP 2010. (ch. 2) ([draft](http://www.iti.cs.tu-bs.de/~adamek/algebraic_theories.pdf)) 


[[!redirects sifted categories]]
[[!redirects cosifted category]]
[[!redirects cosifted categories]]