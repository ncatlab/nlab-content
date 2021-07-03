
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[simplicial homotopy theory]], *décalage* refers to a well-behaved model of [[path space objects]] for [[simplicial sets]]:

If you take a [[simplicial set]] and 'throw away' the last face and degeneracy, and relabel, shifting everything down one 'notch', you get a new simplicial set.  This is what is called the _d&#233;calage_ of a [[simplicial set]]. 

It is a model for the [[path space object]] of $X$, -- or rather: the union of all based path space objects for all basepoints $x \in X_0$ -- similar to, but a little smaller than, the model $X^I \times_X X_0$, which is discussed for instance at _[[factorization lemma]]_:

In the latter case an $n$-cell in the path space is a morphism to $X$ from the simplicial cone over the $n$-simplex modeled as the [[pushout]] $(\Delta[n] \times \Delta[1]) \coprod_{\Delta[n]} \Delta[0]$.
This is the simplicial set obtained by forming the simplicial [[cylinder]] over $\Delta[n]$ and then contracting one end to the point. 

Contrary to that, an $n$-simplex in the d&#233;calage of $X$ is a morphism to $X$ from the cone over $\Delta[n]$ modeled simply by the [[join of simplicial sets]] $\Delta[n] \star \Delta[0]$. 

This is a much smaller model for the cone. In fact $\Delta[n]\star \Delta[0] = \Delta[n+1]$ is just the $(n+1)$-simplex. On the other hand, the above pushout-construction produces simplicial sets with many $(n+1)$-simplices, the one that one "expects", but glued to others with some degenerate edges. Accordingly, there is, for $n \geq 1$, a proper inclusion

$$
  \Delta[n] \star \Delta[1] \hookrightarrow
  (\Delta[n] \times \Delta[1]) \coprod_{\Delta[n]} \Delta[0]
  \,.
$$

As a result, the d&#233;calage construction is often more convenient than forming $X^I \times_X X_0$.


## Definition 

The plain definition of the d&#233;calage of a simplicial set is very simple, stated below in 

* _[In components](#DefinitionInComponents)_

However, in order to appreciate and handle this definition, it is useful
to understand it as a special case of total d&#233;calage, stated below in 

* _[As a restriction of total d&#233;calage](#AsARestrictionOfTotalDecalage)_ .

From this one sees more manifestly that the d&#233;calage of a simplicial set
is built from cones in the original simplicial set. This we discuss below in

* _[In terms of cones](#DefinitionInTermsOfCones)_.

In this last formulation it is clearest what the two canonical morphisms out of the d&#233;calage of a simplicial set mean. These we define in

* _[Morphisms out of d&#233;calage](#MorphismsOutOfIt)_.

### In components
 {#DefinitionInComponents}

Concretely, the d&#233;calage construction is the following.

+-- {: .num_defn #DecalageInComponents}
###### Definition

For $X$ a [[simplicial set]],
the **d&#233;calage** $Dec_0\, X \in sSet$ of $X$, is the simplicial set obtained by shifting every dimension down by one, 'forgetting' the last face and degeneracy  of $X$ in each dimension:

* $(Dec_0 \, X)_n \coloneqq X_{n+1}$;

* $d_k^{n,Dec_0 X}  \coloneqq d^{n+1,X}_{k}$;

* $s_k^{n,Dec_0 X}  \coloneqq s^{n+1,X}_{k}$.

=--

Analogously:

* $(Dec^0 \, X)_n \coloneqq X_{n+1}$;

* $d_k^{n,Dec^0 X}  \coloneqq d^{n+1,X}_{k+1}$;

* $s_k^{n,Dec^0 X}  \coloneqq s^{n+1,X}_{k+1}$.

([Illusie 72](#Illusie72), review in [Stevenson 11, Def. 2](#Stevenson11)) 

### As a restriction of total d&#233;calage
 {#AsARestrictionOfTotalDecalage}

It is often useful to understand this as a special case of the _[[total décalage]]_ construction:

+-- {: .num_defn}
###### Definition

Write $\sigma \colon \Delta_a \times \Delta_a \to \Delta_a$ for the [[ordinal sum]] operation on the [[asSet|augmented simplex category]]. The [[total décalage]] functor is precompositon with this

$$
  \sigma^* \colon sSet_a \to ssSet_a
$$

or rather its restriction from [[augmented simplicial sets]] to just [[simplicial sets]]/[[bisimplicial sets]].

$$
  \sigma^* : sSet \to ssSet
  \,.
$$

In terms of this the plain [[décalage]] is the functor induced from the restriction $\sigma(-,[0]) : \Delta \to \Delta$, of [[ordinal sum]] with $0$, i.e.

$$
  Dec_0 X := (\sigma(-,[0]))^* X
  \,.
$$

=--

### In terms of cones
 {#DefinitionInTermsOfCones}

The perspective from total d&#233;calage makes fairly manifest that d&#233;calage forms [[cones]] in $X$, as we discuss now. To this end, notice the relation of [[total décalage]] to [[join of simplicial sets]]:

+-- {: .num_defn}
###### Definition


Write

$$
  \Box : sSet \times sSet \to ssSet 
$$

for the _box product functor_ that takes $X,Y \in sSet$ to the [[bisimplicial set]]

$$
  (X \Box Y) : ([k],[l]) \mapsto X_k \times X_l
  \,.
$$

=--

+-- {: .num_lemma}
###### Lemma

If $X, Y \in $ [[sSet]] are connected, then  their [[join of simplicial sets]] $X \star Y$ is expressed by the [[left adjoint]] to [[total décalage]] as

$$
  \sigma_!(X \Box Y) = X \star Y
  \,.
$$

=--

This appears as ([Stevenson 12, lemma 2.1](#Stevenson12)).

It follows that the left adjoint of plain d&#233;calage forms joins with the 0-simplex:

+-- {: .num_cor}
###### Corollary

The [[left adjoint]] to $Dec_0 : sSet \to sSet$ is

$$
  C := \sigma_!((-) \Box \Delta[0])
  \,.
$$

In particular for $S \in sSet$ connected we have

$$
  C(S) = S \star \Delta[0]
  \,.
$$

=--

This appears as ([Stevenson 12, cor. 2.1](#Stevenson12)).

+-- {: .num_remark}
###### Remark

The [[join of simplicial sets]] with the 0-simplex $X \star \Delta[0]$ forms a simplicial model for the [[cone]] over $X$.

=--

+-- {: .num_cor #InTermsOfCones}
###### Corollary

By [[adjunction]] we have for all $n \in \mathbb{N}$

$$
  (Dec_0 X)_n = Hom_{sSet}( \Delta[n] \star \Delta[0], X)
  \,.
$$

=--

So this exhibits the $n$-cells of $Dec_0 X$ as being the cones of $n$-simplices in $X$.

### Morphisms out of the d&#233;calage
 {#MorphismsOutOfIt}



+-- {: .num_prop #TheCanonicalMorphisms}
###### Proposition


For $X \in sSet$ its d&#233;calage $Dec_0 X$ comes with two canonical [[morphisms]] out of it

$$
  \array{
    Dec_0 X &\overset{\in Fib}{\longrightarrow}& X
    \\
    \big\downarrow {}^{\mathrlap{\in \mathrm{W}}}
    \\
    const X_0
    \mathrlap{\,.}
  }
$$

Here, in terms of the description [above](#DefinitionInTermsOfCones) of d&#233;calage by cones:

* the horizontal morphism is induced from the canonical inclusion 
  $\Delta[n] \hookrightarrow \Delta[n]\star \Delta[0]$;

* the vertical morphism is given by the canonical inclusion
  $\Delta[0] \hookrightarrow \Delta[n]\star \Delta[0]$.

Or in terms of components, as discussed 
[above](#DefinitionInComponents), 

* the horizontal morphism is given by
  $d_{last} \colon Dec_0 Y \to Y$,
  hence in degree $n$ by the remaining face map 
  $d_{n+1} \colon X_{n+1} \to X_n$;

* the vertical morphism is given in degree 0 by $s_0 \colon X_1 \to X_0$ and in every higher degree similarly by $s_0 \circ s_0 \circ \cdots \circ s_0$.

=--

(review in [Stevenson 11, Def. 2](#Stevenson11))

These morphisms are a [[Kan fibration]] and a [[simplicial weak equivalence]], respectively, by the [following](#FibrationResolution) discussion.



## Properties

### Fibration resolution
 {#FibrationResolution}

We discuss here how $Dec_0 X \to X$ is a [[resolution]] of $const X_0 \to X$ by a [[Kan fibration]].

+-- {: .num_prop}
###### Proposition

For $X$ a simplicial set, the two morphisms from prop. \ref{TheCanonicalMorphisms} have the following properties.

* the morphism $d_0 : Dec_0 X \to const X_0$ is a [[weak homotopy equivalence]], in fact a [[deformation retract]]; a weak inverse is given by the morphism which in degree 0 is the degeneracy $s_0 : X_0 \to X_1$, and so on.

If $X$ is a [[Kan complex]], then

* the morphism $d_{last} : Dec_0 X \to X$ is a [[Kan fibration]];

=--

+-- {: .proof}
###### Proof

The first statement is classical, it appears for instance as ([Stevenson 11, lemma 5](#Stevenson11)).

For the second, notice that by remark \ref{InTermsOfCones} the lifting problem

$$
  \array{
    \Lambda^n[n] &\to& Dec_0 X
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] &\to& X
  }
$$

is equivalent to the lifting problem  

$$
  \array{
    (\Lambda^n[n] \star \Delta[0]) \coprod_{\Lambda^i[n]} \Delta[n] &\to& X
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] \star \Delta[0] &\to& *
  }
  \,.
$$

Here the left morphism is an [[anodyne morphism]], in fact is an  $(n+1)$-[[horn]] inclusion $\Lambda[n+1] \to \Delta[n+1]$. So a lift exists if $X$ is a [[Kan complex]].

=--

+-- {: .num_remark}
###### Remark

By the above, $Dec_0 X$ is the [[disjoint union]] of [[over quasi-categories]] 

$$
  Dec_0 X  = \coprod_{x \in X_0} X_{/x}
  \,.
$$

For each of these the statement that the projection $X_{/x} \to X$ is a [[Kan fibration]] if $X$ is a [[Kan complex]], and moreover that it is a a [[right fibration]] if $X$ is a [[quasi-category]], is ([Joyal, theorem 3.19](#Joyal)), reproduced also as ([[Higher Topos Theory|HTT, prop. 2.1.2.1]]). Notice that left/right fibrations into a Kan complex are automatically Kan fibrations (by the discussion at _[Left fibration in ∞-groupoids](right%2Fleft+Kan+fibration#AsFibrationsInInfinityGroupoids)_).


=--


+-- {: .num_cor}
###### Corollary

For $X$ a [[Kan complex]], the d&#233;calage morphism $Dec_0 X \to X$ is a [[Kan fibration]] [[resolution]] of the inclusion $const X_0 \to X$ of the set of 0-cells of $X$, regarded as a [[discrete object|discrete]] simplicial set:

there is a [[commuting diagram]]

$$
  \array{
    const X_0 &\stackrel{\simeq}{\to}& Dec_0 X
    \\
    \downarrow && \downarrow
    \\
    X &\to& X
  }
  \,,
$$

where

* the top morphism 

  * is given in degree $n$ by the $n$-fold degeneracy map $s_0 \circ s_0 \circ \cdots s_0$;

  * is a [[weak homotopy equivalence]];

* the right vertical morphism 

  * is given in degree $n$ by $d_{n+1} : X_{n+1} \to X_n$ 

  * is a [[Kan fibration]].

=--

+-- {: .num_remark}
###### Remark

The inclusion $const X_0 \to X$ presents a canonical [[effective epimorphism in an (∞,1)-category]] in [[∞Grpd]] into $X$, out of a [[0-truncated]] object. By the above, the d&#233;calage is a natural fibration resolution of this canonical "[[atlas]]".

This is useful for instance in the discussion of [[homotopy pullbacks]] of this effective epimorphism: by the discussion there the homotopy pullback of $const X_0 \to X$ along any morphism $f : A \to X$ is presented by the ordinary pullback of any Kan fibration resolution, hence in particular of the d&#233;calage projection:

$$
  f^* Dec_0 X \simeq A \times_X^{h} const X_0
  \,.
$$

=--


 



### D&#233;calage comonad 
 {#DecalageComonad}

D&#233;calage also has an abstract [[category theory|category theoretic]] description as follows. The [[augmented simplex category]] with the ordinal sum operation is a [[monoidal category]] $(\Delta_a, + = \sigma, 0 = [-1])$. This monoidal category carries a canonical [[monoid]], namely the terminal object $1 = [0]$ with its unique monoid structure. By duality, the monoidal category $\Delta_a^{op}$ has a comonoid, also denoted $[0]$. 

As is the case for any comonoid in a monoidal category, the comonoid $[0]$ induces a comonad $D_0 = (-) + [0] = \sigma(-, [0])$ on $\Delta_a^{op}$. And, as is the case for any $2$-functor, exponentiation $Set^{-}$ as a $2$-functor (say of the form $cat^{op} \to Cat$, from small categories to locally small categories) takes the comonad $D_0: \Delta_a^{op} \to \Delta_a^{op}$ in $cat^{op}$ to a comonad $Set^{D_0}: Set^{\Delta_a^{op}} \to Set^{\Delta_a^{op}}$ in $Cat$. This comonad, mapping $F: \Delta_a^{op} \to Set$ to $F \circ D_0: \Delta_a^{op} \to Set$, is precisely the d&eacute;calage comonad $Dec_0: SSet \to SSet$. 

(By similar reasoning, there is a second comonad $D^0 = [0] + (-) = \sigma([0], -)$ on $\Delta_a^{op}$, which in turn induces a second comonad $Set^{D^0}: Set^{\Delta_a^{op}} \to Set^{\Delta_a^{op}}$. This second d&eacute;calage comonad is denoted by [Stevenson](#Stevenson11) as $Dec^0: SSet \to SSet$.) 

There are tautologically equivalent formulations. One formulation invokes the fact that $\Delta_a$ together with the terminal monoid $[0]$ constitute the "[[walking structure|walking]] [[monoid]]", i.e., $\Delta_a$ is initial among monoidal categories equipped with a monoid. Similarly, $\Delta_a^{op}$ is the walking [[comonoid]]: by initiality, strict monoidal functors $\Delta_a^{op}\to [C, C]$ are precisely in correspondence with comonoids in the endofunctor category $[C, C]$ (as a monoidal category under endofunctor composition), that is to say, with comonads on $C$. 

Consider then the monoidal product
$$ \sigma : \Delta_a^{op} \times \Delta_a^{op} \to \Delta_a^{op}$$
Analogous to Cayley embeddings of monoids into endofunction monoids, either way of currying this product produces a strict monoidal functor $\Delta_a^{op}\to [\Delta_a^{op},\Delta_a^op]$ into an endofunctor category. By applying 2-functoriality as above, there is additionally a strict monoidal functor 

$$[\Delta_a^{op}, \Delta_a^{op}] \to [\mathbf{SSet},\mathbf{SSet}]$$ 

given by precomposition. Composing these two strict monoidal functors, there is a strict monoidal functor 

$$\Delta_a^{op}\to [\mathbf{SSet}, \mathbf{SSet}].$$ 
 
Hence by the "walking" correspondence, the value of $[0]$ under this monoidal functor is a comonad on simplicial sets whose underlying functor is d&#233;calage: 

$$
  Dec_0 \colon Set^{\Delta_a^{op}} \to Set^{\Delta_a^{op}}
$$

(Tautologically, though, this is merely an elaborate way to rephrase the earlier description of this comonad.) 

The map $d_{last} \colon Dec_0 \to Id$ is the counit of the comonad. The comonad itself is analogous to a kind of unbased [[path space object]] comonad $P$ on $Top$ whose value at a space $X$ is a pullback 

$$
  \array{
    P X & \to & X^I 
    \\
    \downarrow & & \downarrow \mathrlap{eval_0} 
    \\
    |X| & \stackrel{i}{\to} & X  
  }
$$

where $i$ is the set-theoretic identity inclusion of $X$ equipped with the discrete topology. Thus we have 

$$
  P X 
  \;=\; 
  \sum_{x_0 \in X} P(X, x_0),

$$ 

the sum over all possible basepoints $x_0$ of path spaces based at $x_0$. The analogy is made precise by a canonical isomorphism 

$$
  Dec_0 \circ Sing 
  \;\cong\; 
  Sing \circ P
  \,,
$$ 

where $Sing \;\colo\; Top \to Set^{\Delta^{op}}$ is the [[singular simplicial complex]]-[[functor]]. 

A $P$-coalgebra partitions $X$ into path components and exhibits contractibility of each component. Similarly, a coalgebra of the d&eacute;calage comonad exhibits the acyclicity of the underlying simplicial set. 

####Total D&#233;calage####

 Using either the simplicial [[comonadic resolution]] generated by the above comonad or directly using [[ordinal sum]], we get a [[bisimplicial set]] known as the [[total decalage|total décalage]] of $Y$. See there for more details.

## Examples

### For simplicial classifying spaces
 {#ExampleForSimplicialClassifyingSpaces}

A central application is the special case where $X = \overline{W} G$ is the [[simplicial classifying space]] of a [[simplicial group]] $G$ (see at _[[simplicial principal bundle]]_). In this case $Dec_0 \overline{W} G$, called $W G$, is a standard model for the _[universal simplicial principal bundle](simplicial%20principal%20bundle#UniversalSimplicialBundle)_.

Or rather, with the conventions used at *[[simplicial classifying spaces]]* (which are those of [Goerss & Jardine, p. 269](simplicial+classifying+space#GoerssJardine09)) we have $W G \,=\, Dec^0(\overline{W}G)$ (Def. \ref{DecalageInComponents}).


### For simplicial groups
 {#ExampleForSimplicialGroups}

The case of $Dec_0 G$ for $G$ a [[simplicial group]] is important in the simplicial theory of algebraic models for [[homotopy n-types]].

In this case the morphism $d_{last} : Dec_0\, G \to G$, is an [[epimorphism]].  Taking the [[kernel]] of this and then applying $\pi_0$, yields a [[crossed module]] constructed from the [[Moore complex]] of $G$

$$N G_1/d_2(NG_2)\to N G_0,$$

which has kernel $\pi_1(G)$ and cokernel $\pi_0(G)$. This crossed module represents the [[homotopy 2-type]] of $G$. Applying the d&#233;calage  twice  leads to a [[crossed square]] which represents the 3-type of $G$, ... and so on.

## Related concepts

* [[bar construction]]

## References

Original sources are 

* {#Illusie72} [[Luc Illusie]], _Complexe cotangent et d&#233;formations I_, volume 239 of Lecture Notes in Maths ,  Springer-Verlag. and  1972, _Complexe cotangent et d&#233;formations II_, volume 283 of Lecture Notes in Maths , Springer-Verlag (1971)

and

* [[John Duskin]], _Simplicial methods and the interpretation of "triple" cohomology_, number  163 in Mem. Amer. Math. Soc., 3, Amer. Math. Soc (1975)

The notion of d&#233;calage has been widely used since the paper introducing the method of [[cohomological descent]] in [[Hodge theory]]:

* [[Pierre Deligne]], _Th&#233;orie de Hodge. III_, Inst. Hautes &#201;tudes Sci. Publ. Math. __44__ (1974), 5--77. 

Reviews are in

* [[Phil Ehlers]], _Algebraic Homotopy in Simplicially Enriched Groupoids_, 1993,  University of Wales Bangor, (pdf [[Ehlers-thesis.pdf|here:file]]) 

A detailed account of various technical aspects:
 
* {#Stevenson11} [[Danny Stevenson]], around Lemma 15 of: *Décalage and Kan's simplicial loop group functor*, Theory and Applications of Categories, Vol. 26, 2012, No. 28, pp 768-787 ([arXiv:1112.0474](https://arxiv.org/abs/1112.0474), [tac:26-28](http://www.tac.mta.ca/tac/volumes/26/28/26-28abs.html)) 

and 

* {#Stevenson12} [[Danny Stevenson]], Section 2.2 of _Classifying theory for simplicial parametrized groups_ ([arXiv:1203.2461](http://arxiv.org/abs/1203.2461))
 

Closely related technical results are in section 3 of 

* {#Joyal}  [[André Joyal]], _The theory of quasi-categories and its applications_ , lectures at CRM Barcelona (2008)

The link with simplicial groups and algebraic models of homotopy $n$-types is given in 

* [[Tim Porter]], _n-types of simplicial groups and crossed n-cubes_, Topology, 32, (1993), 5--24.

* [[Tim Porter]], _[[Menagerie|The crossed menagerie]]_
 

An application in the theory of [[stacks]] is discussed in

* [[Anders Kock]], _The stack quotient of a groupoid_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, __44__ no. 2 (2003), p. 85--104 [numdam](http://www.numdam.org/item?id=CTGDC_2003__44_2_85_0)


[[!redirects decalage]]
[[!redirects décalage]]

[[!redirects total decalage]]
[[!redirects total décalage]]

