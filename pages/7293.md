
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[algebraic topology]], what are called the _Steenrod squares_ is the system of [[cohomology operations]] on [[ordinary cohomology]] with [[coefficients]] in $\mathbb{Z}_2$ (the [[cyclic group of order 2]]) which is compatible with [[suspension]] (the "stable cohomology operations").  They are special examples of [[power operations]].

The collection of Steenrod squares for all degrees forms the _[[Steenrod algebra]]_, see there for more.

## Definition

### Construction in terms of extended squares
 {#DefinitionInTermsOfExtendedSquares}

We discuss the explicit construction of the Steenrod-operations in terms of [[chain maps]] of [[chain complexes]] of $\mathbb{F}_2$-[[vector spaces]] equipped with a suitable product. We follow ([Lurie 07, lecture 2](#Lurie07)).

Write $\mathbb{F}_2 \coloneqq \mathbb{Z}/2\mathbb{Z}$ for the [[field]] with two elements.

For $V$ an $\mathbb{F}_2$-[[module]], hence an $\mathbb{F}_2$-[[vector space]], and for $n \in \mathbb{N}$, write

$$
  V^{\otimes n}_{h \Sigma_n} \in \mathbb{F}_2 Mod
$$

for the [[homotopy quotient]] of the $n$-fold [[tensor product]] of $V$ with itself by the [[action]] of the [[symmetric group]]. Explicitly this is presented, up to [[quasi-isomorphism]] by the ordinary [[coinvariants]] $D_n(V)$ of the tensor product of $V^{\otimes n}$ with a [[free resolution]] $E \Sigma_n^\bullet$ of $\mathbb{F}_2$:

$$
  V^{\otimes n}_{h \Sigma_n}
  \simeq
  D_n(V)
  \coloneqq
  (V^{\otimes n} \otimes E\Sigma_n)_{\Sigma_n}
  \,.
$$

This is called the $n$th _[[extended power]]_ of $V$.

For instance

$$
  D_2(  \mathbb{F}_2[-n])
  \simeq
  \mathbb{F}_2[-2n] \otimes C^\bullet(B \Sigma_2)
  \,,
$$

where on the right we have the, say, [[singular cohomology]] [[cochain complex]] of the [[homotopy quotient]] $\ast //\Sigma_2 \simeq B \Sigma_2 \simeq \mathbb{R}P^\infty$, which is the [[homotopy type]] of the [[classifying space]] for $\Sigma_2$.

A [[chain map]]

$$
  D_2(V) \longrightarrow V
$$

is called a _symmetric multiplication_ on $V$ (a shadow of an [[E-infinity algebra]] structure). The archetypical class of examples of these are given by the [[singular cohomology]] $V = C^\bullet(X, \mathbb{F}_2)$ of any [[topological space]] $X$,  for instance of $B \Sigma_2$.

Therefore there is a canonical [[isomorphism]]

$$
  H^k(D_2(\mathbb{F}_2[-n]))
  \simeq
  H_{2n - k}(B \Sigma_2, \mathbb{F}_2) e_{2n}
$$

of the [[cochain cohomology]] of the extended square of the chain compplex concentrated on $\mathbb{F}_2$ in degree $n$ with the [[singular homology]] of this classifying space shifted by $2 n$.

Using this one gets for general $V$ and for each $i \leq n$ a map that sends an element in the $n$th [[cochain cohomology]]

$$
  [v] \in H^n(V)
$$

represented  by a morphism of [[chain complexes]]

$$
  v \;\colon\; \mathbb{F}_2[-n] \longrightarrow V
$$

to the element

$$
  \overline{Sq}^i(v) \in H^{n+1}(D_2(V))
$$

represented by the [[chain map]]

$$
  \mathbb{F}_2[-n-i]
  \stackrel{1}{\longrightarrow}
  C^\bullet(B \Sigma_2, \mathbb{F}_2)
  \stackrel{\simeq}{\longrightarrow}
  D_2(\mathbb{F}_2[-n])
   \stackrel{D_2(v)}{\longrightarrow}
  D_2(V)
  \,.
$$

If moreover $V$ is equipped with a _symmetric product_ $D_2(V) \longrightarrow V$ as above, then one can further compose and form the element

$$
  {Sq}^i(v) \in H^{n+1}(V)
$$

represented by the [[chain map]]

$$
  \mathbb{F}_2[-n-i]
  \stackrel{1}{\longrightarrow}
  C^\bullet(B \Sigma_2, \mathbb{F}_2)
  \stackrel{\simeq}{\longrightarrow}
  D_2(\mathbb{F}_2[-n])
   \stackrel{D_2(v)}{\longrightarrow}
  D_2(V)
   \longrightarrow
  V
  \,.
$$

This [[linear map]]

$$
  Sq^i \;\colon\; H^\bullet(V) \longrightarrow H^{\bullet + i}(V)
$$

is called the $i$th _Steenrod operation_ or the $i$th _Steenrod square_ on $V$. By default this is understood for $V = C^\bullet(X,\mathbb{F}_2)$ the $\mathbb{F}_2$-[[singular homology|singular cochain complex]] of some [[topological space]] $X$, as in the above examples, in which case it has the form

$$
  Sq^i \;\colon\; H^\bullet(X, \mathbb{F}_2) \longrightarrow H^{\bullet+i}(X,\mathbb{F}_2)
  \,.
$$


### Axiomatic characterization

For $n \in \mathbb{N}$ write $B^n \mathbb{Z}_2$ for the [[classifying space]] of [[ordinary cohomology]] in degree $n$ with [[coefficients]] in the [[group of order 2]] $\mathbb{Z}_2$ (the [[Eilenberg-MacLane space]] $K(\mathbb{Z}_2,n)$), regarded as an [[object]] in the [[homotopy category]] $H$ [[model structure on topological spaces|of topological spaces]]).

Notice that for $X$ any topological space ([[CW-complex]]), 

$$
  H^n(X, \mathbb{Z}_2) \coloneqq H(X, B^n \mathbb{Z}_2) 
$$

is the [[ordinary cohomology]] of $X$ in degree $n$ with [[coefficients]] in $\mathbb{Z}_2$. Therefore, by the [[Yoneda lemma]], [[natural transformations]]

$$
  H^{k}(-, \mathbb{Z}_2) \to H^l(-, \mathbb{Z}_2)
$$

correspond bijectively to morphisms $B^k \mathbb{Z}_2 \to B^l \mathbb{Z}_2$.

The following characterization is due to ([SteenrodEpstein](#SteenrodEpstein)).

+-- {: .num_defn}
###### Definition

The **Steenrod squares** are a collection of [[cohomology operations]]

$$
  Sq^n \;\colon\; H^k(-, \mathbb{Z}_2) \longrightarrow H^{k+n}(-, \mathbb{Z}_2)
  \,,
$$

hence of [[morphisms]] in the [[homotopy category]]

$$
  Sq^n \;\colon\; B^k \mathbb{Z}_2 \longrightarrow B^{k + n} \mathbb{Z}_2
$$

for all $n,k \in \mathbb{N}$ satisfying the following conditions:

1. for $n = 0$ it is the [[identity]];

1. if $n \gt deg(x)$ then $Sq^n(x) = 0$;

1. for $k = n$ the morphism $Sq^n : B^n \mathbb{Z}_2 \to B^{2n} \mathbb{Z}_2$ is the [[cup product]] $x \mapsto x \cup x$;

1. $Sq^n(x \cup y) = \sum_{i + j = n} (Sq^i x) \cup (Sq^j y)$;


=--

An analogous definition works for [[coefficients]] in $\mathbb{Z}_p$ for any [[prime number]] $p \gt 2$. The corresponding operations are then usually denoted

$$
  P^n \;\colon\; B^k \mathbb{Z}_p \longrightarrow B^{k+n} \mathbb{Z}_{p}
  \,.
$$

Under [[composition]], the Steenrod squares form an [[associative algebra]] over $\mathbb{F}_2$, called the _[[Steenrod algebra]]_. See there for more.

## Properties

### Relation to Bockstein homomorphism

$Sq^1$ is the [[Bockstein homomorphism]] of the [[short exact sequence]] $\mathbb{Z}_2 \to \mathbb{Z}_4 \to \mathbb{Z}_2$.


### Compatibility with suspension

The Steenrod squares are compatible with the [[suspension isomorphism]].

Therefore the Steenrod squares are often also referred to as the _[[stabilization|stable]] [[cohomology operations]]_

### Relation to Massey products

See at _[[Massey product]]_, _[Relation to Steenrod squares](Massey+product#RelationToSteenrodSquares)_


### Adem relations


+-- {: .num_prop #AdemRelations}
###### Proposition
**([[Adem relations]])**

The [[composition]] of Steenrod square operations satisfies the following relations

$$
  Sq^i \circ Sq^j 
   = 
  \sum_{0 \leq k \leq i/2}
  \left(
    {
      { j - k - 1 }
      \atop 
      { i - 2k }
    }
  \right)_{mod 2}
  Sq^{i + j -k} \circ Sq^k
$$

for all $0 \lt i \lt 2 j$.

Here $\left( a \atop b \right) \coloneqq 0$ if $a \lt b$.

=--


+-- {: .num_example #CompositionWithSq1}
###### Example
**([[Adem relation]] for [[postcomposition]] with the [[Bockstein homomorphism]] $Sq^1 = \beta$)**

For $j \geq 2$ and $i =1$, the [[Adem relations]] (prop. \ref{AdemRelations}) say that:

$$
  \begin{aligned}
    Sq^1 \circ Sq^j 
    & = 
    \underset{
      (j-1)_{mod 2}
    }{
    \underbrace{
    \left(
      {
        {j - 1 }
        \atop
        1
      }     
    \right)_{mod 2}
    }}
    Sq^{j + 1} 
    \\   
    & =
    \left\{
      \array{
        Sq^{j+1} &\vert& j \, \text{even}
        \\
        0 &\vert& j \, \text{odd}
      }
    \right.
  \end{aligned}
$$

=--

This gives rise to:

+-- {: .num_example #IntegralSteenrodSquares}
###### Example
**([[integral Steenrod squares]])**

For [[odd natural numbers|odd]] $2n + 1 \in \mathbb{N}$ defines the [[integral Steenrod squares]] to be

$$
  Sq^{2n + 1}_{\mathbb{Z}}
  \;\coloneqq\;
  \beta \circ Sq^{2n}
  \,.
$$

By example \ref{CompositionWithSq1} and by [this example](Bockstein+homomorphism#Mod2BocksteinIntoMod2Cohomology) these indeed are lifts of the odd [[Steenrod squares]]:

$$
  (mod\, 2) \circ Sq^{2n + 1}_{\mathbb{Z}}
  \;=\;
  Sq^{2n+1}
  \,,
$$

in that we have

$$
  \array{
    Sq^{2n+1}_{\mathbb{Z}}
    &\colon&
    B^{\bullet} (\mathbb{Z}/2\mathbb{Z})
      &\overset{Sq^{2n}}{\longrightarrow}&      
    B^{\bullet + 2n} (\mathbb{Z}/2\mathbb{Z})
      &\overset{ \beta }{\longrightarrow}&
    B^{\bullet + 2n + 1} \mathbb{Z}
    \\
    &&
    \downarrow^{ id }  
    &&
    \downarrow^{ id }
      &&
    \downarrow^{\mathrlap{B^{k + 2 n + 1}(mod\, 2)}}
    \\
    Sq^{2n+1}
    &\colon&
    B^{\bullet} (\mathbb{Z}/2\mathbb{Z})
      &\underset{Sq^{2n}}{\longrightarrow}&   
    B^{\bullet + 2n} (\mathbb{Z}/2\mathbb{Z})
       &\underset{  Sq^1 }{\longrightarrow}&
    B^{\bullet + 2n + 1} (\mathbb{Z}/2\mathbb{Z})
  }
$$

=--


## Examples

### Hopf invariant
 {#HopfInvariant}

+-- {: .num_prop}
###### Proposition

For $\phi \colon S^{k+n-1} \to S^k$, a map of [[spheres]], the Steenrod square 

$$
  Sq^n 
    \colon 
   H^k(cofib(\phi), \mathbb{F}_2) 
    \longrightarrow 
   H^{k+n}(cofib(\phi),\mathbb{F}_2)
$$

(on the [[homotopy cofiber]] $cofib(\phi)\simeq S^k \underset{S^{k+n-1}}{\cup} D^{k+n}$)

is non-vanishing exactly for $n \in \{1,2,4,8\}$.

=--

([Adams 60, theorem 1.1.1](Hopf+invariant+one#Adams60)).

See at _[[Hopf invariant one theorem]]_.


## Related concepts

* [[cohomology operation]]

* [[Bockstein homomorphism]],

* [[Wu class]]

* [[Steenrod algebra]]

## References

The operations were first defined in 

* [[Norman Steenrod]], _Products of cocycles and extensions of mappings_, Annals of Mathematics Second Series, Vol. 48, No. 2 (Apr., 1947), pp. 290-320 ([jstor:1969172](https://www.jstor.org/stable/1969172))

The axiomatic definition appears in

* {#SteenrodEpstein} [[Norman Steenrod]], [[David Epstein]], _Cohomology operations_, Annals of Mathematics Studies, Princeton University Press (1962) ([jstor:j.ctt1b7x52h](https://www.jstor.org/stable/j.ctt1b7x52h))
 

Lecture notes on Steenrod squares and the [[Steenrod algebra]] include

* {#Lurie07} [[Jacob Lurie]], 18.917 _[Topics in Algebraic Topology: The Sullivan Conjecture, Fall 2007](http://ocw.mit.edu/courses/mathematics/18-917-topics-in-algebraic-topology-the-sullivan-conjecture-fall-2007)_. (MIT OpenCourseWare: Massachusetts Institute of Technology), _[Lecture notes](http://ocw.mit.edu/courses/mathematics/18-917-topics-in-algebraic-topology-the-sullivan-conjecture-fall-2007/lecture-notes/)_

  Lecture 2 _Steenrod operations_ ([pdf](http://ocw.mit.edu/courses/mathematics/18-917-topics-in-algebraic-topology-the-sullivan-conjecture-fall-2007/lecture-notes/lecture2.pdf))

  Lecture 3 _Basic properties of Steenrod operations_ ([pdf](http://ocw.mit.edu/courses/mathematics/18-917-topics-in-algebraic-topology-the-sullivan-conjecture-fall-2007/lecture-notes/lecture3.pdf))

  Lecture 4 _The Adem relations_ ([pdf](http://ocw.mit.edu/courses/mathematics/18-917-topics-in-algebraic-topology-the-sullivan-conjecture-fall-2007/lecture-notes/lecture4.pdf))

  Lecture 5 _The Adem relations (cont.)_ ([pdf](http://ocw.mit.edu/courses/mathematics/18-917-topics-in-algebraic-topology-the-sullivan-conjecture-fall-2007/lecture-notes/lecture5.pdf))
  

See also

* [[Wen-Tsun Wu]], _Sur les puissances de Steenrod_, Colloque de Topologie de Strasbourg, IX, La Biblioth&#232;que Nationale et Universitaire de Strasbourg, (1952)


[[!redirects Steenrod squares]]

[[!redirects Steenrod operation]]
[[!redirects Steenrod operations]]


[[!redirects stable cohomology operation]]
[[!redirects stable cohomology operations]]