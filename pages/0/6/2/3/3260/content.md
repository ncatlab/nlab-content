

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Equivariant homotopy theory is [[homotopy theory]] for the case that a [[group]] $G$ acts on all the [[topological space]]s  or other objects involved.

## In topological spaces

Let $G$ be a discrete [[group]].

A **$G$-space** is a [[topological space]] equipped with a $G$-[[action]].

Let $I = \mathbb{R}$ be the [[interval object]] $({*} \stackrel{0}{\to} I \stackrel{1}{\leftarrow} {*})$ regarded as a $G$-space by equipping it with the trivial $G$-[[action]].

A **$G$-[[homotopy]]**  $\eta$ between $G$-maps $f,g  X \to Y$ is a [[left homotopy]] with respect to this $I$

$$
  \array{
    X \times {*} = X
    \\
    {}^{\mathllap{Id \times 0}}\downarrow & \searrow^{f}
    \\
    X \times I &\stackrel{\eta}{\to}& Y
    \\
    {}^{\mathllap{1}}\uparrow & \nearrow_{g}
    \\
    X\times {*} = X
  }
  \,.
$$ 

### Homotopical categories of $G$-equivariant spaces

+-- {: .un_defn}
###### Definition
**(models for $G$-equivariant spaces)**

Consider the following three [[homotopical category|homotopical categories]] that model $G$-spaces:

1. Write

   $$
     G Top_{cof} \subset G Top
   $$ 

   for the full [[subcategory]] of $G$-[[CW-complex]]es, regarded as equipped with the structure of a [[category with weak equivalences]] by taking the weak equivalences to be the $G$- [[homotopy equivalence]]s with the above definition. 

1. Write

   $$
     G Top_{loc}
   $$

   for all of $G Top$ equipped with weak equivalences given by those morphisms $(f : X \to Y) \in G Top$ that induce on for all subgroups $H \subset G$ weak equivalences $f^H : X^H \to Y^H$ on the $H$-fixed point spaces, in the standard [[model structure on topological spaces]] (i.e. inducing isomorphism on homotopy groups).

1. Write

   $$
     [O_G^{op}, Top]_{proj}
   $$ 

   for the projective [[global model structure on functors]] 
   from the [[opposite category]] of the [[orbit category]] $O_G$ of $G$ to [[model structure on topological spaces|Top]]. 


=--

+-- {: .num_theorem }
###### Theorem
**(Elmendorf's theorem)**

The [[homotopy category|homotopy categories]] of all three models are [[equivalence of categories|equivalent]]:

$$
  Ho(G Top_{loc}) \simeq Ho(G Top_{cof}) \stackrel{\simeq}{\to} Ho([O_G^{op}, Top])
  \,,
$$

where the equivalence is induced by the functor that sends $G$-space to the presheaf that it represents is an [[equivalence of categories]].

=--

+-- {: .proof}
###### Proof


Stated as theorem VI.6.3 in [EqHoCo](http://www.math.rochester.edu/u/faculty/doug/otherpapers/alaska1.pdf).

=--


### $(\infty,1)$-category of $G$-equivariant spaces {#InfGTop}

At [[topological ∞-groupoid]] it is discussed that the category [[Top]] of [[topological space]]s may be understood as the [[localization of an (∞,1)-category]] $Sh_{(\infty,1)}(Top)$ [[(∞,1)-category of (∞,1)-sheaves|of (∞,1)-sheaves]] on $Top$, at the collection of morphisms of the form $\{X \times I \to X\}$ with $I$ the real line.

The analogous statement is true for $G$-spaces: the equivariant homotopy category is the [[homotopy localization]] of the category of $\infty$-stacks on $G Top$.  

More in detail: let $G Top$ be the [[site]] whose objects are $G$-spaces that admit $G$-equivariant open covers, morphisms are $G$-equivariant maps and morphism $Y \to X$ is in the [[coverage]] if it admits a $G$-equivariant splitting over such $G$-equivariant open covers.


Write

$$
  sSh(G Top)_{loc}
$$

for the corresponding [[hypercompletion|hypercomplete]] local [[model structure on simplicial sheaves]]. 

Let $I$ be the unit interval, the standard [[interval object]] in [[Top]], equipped with the trivial $G$-action, regarded as an object of $G Top$ and hence in $sSh(G Top)$.


Write 

$$
  sSh(G Top)_{loc}^I  \stackrel{\leftarrow}{\to}
  sSh(G Top)_{loc}
$$

for the left [[Bousfield localization of model categories|Bousfield localization]] at thecollection of morphisms $\{X \stackrel{Id \times 0}{\to} X \times I\}$.

Then the [[homotopy category]] of $sSh(G Top)_{loc}^I$ is the equivariant homotopy category described above

$$  
  Ho(sSh(G Top)_{loc}^{I}) \simeq G Top_{loc}
  \,.
$$

This is [exaple 3, page 50](http://www.math.uiuc.edu/K-theory/0305/nowmovo.pdf) of

* Morel, Voevosky, _$A^1$-homtopy theory of schemes_ ([pdf](http://www.math.uiuc.edu/K-theory/0305/nowmovo.pdf))


## In more general model categories

Let $G$ be a finite [[group]] as above. We describe the generalizaton of the above story as [[Top]] is replaced by a more general [[model category]] $C$.

+-- {: .un_defn}
###### Definition and proposition

1. Let $C$ be a [[cofibrantly generated model category]] with generating cofibrations $I$ and generating acyclic cofibrations $J$.

   There is a cofibrantly generated model category 

   $$
     [O_G^{op}, C]_{loc}
   $$

   on the [[functor category]] from the [[orbit category]] of $G$ to $C$ by taking the generating cofibratoins to be

   $$
     I_{O_G} := \{G/H \times i\}_{i \in I, H \subset G}
   $$

   and the generating acyclic cofibrations to be
  
   $$
     J_{O_G} := \{G/H \times j\}_{j \in I, H \subset G}
     \,.
   $$

1. Let $\mathbf{B}G$ be the [[delooping]] [[groupoid]] of $G$ and let

   $$
     [\mathbf{B}G^{op}, C]_{loc}
   $$

   be the [[functor category]] from $\mathbf{B}G$ to $C$ -- the category of objects in $C$ equipped with a $G$-[[action]] equipped with a set of generatinc (acyclic) cofibrations

   $$
     I_{\mathbf{B}G} := \{G/H \times i\}_{i \in I, H \subset G}
   $$

   and the generating acyclic cofibrations to be
  
   $$
     J_{\mathbf{B}G} := \{G/H \times j\}_{j \in I, H \subset G}
     \,.
   $$

   This defines a cofibrantly generated model category if $[\mathbf{B}G^{op}, C]$ has a _cellular fixed point functor_ (see...). 

=--

+-- {: .un_defn}
###### Definition and proposition
**(generalized Elmendorf's theorem)**


There is a [[Quillen adjunction]]

$$
  G/e \times (-) : C \stackrel{\leftarrow}{\to} [\mathbf{B}G^{op},C]_{loc} : (-)^e
$$

and a [[Quillen equivalence]]

$$
  \Theta : [O_G^{op}, C]_{loc} \stackrel{\leftarrow}{\to} [\mathbf{B}G^{op},C]_{loc}
  : \Phi
  \,.
$$

=--


+-- {: .proof}
###### Proof

This is proposition 3.1.5 in [Guillou](http://www.math.uiuc.edu/~bertg/EquivModels.pdf#page=6).

=--


### In $\infty$-stack $(\infty,1)$-toposes

The assumption on the [[model category]] $C$ entering the
generalized Elmendorf theorem above is satisfied in particular by every left [[Bousfield localization of model categories|Bousfield localization]] 

$$
  C := L_A SPSh(D)
$$ 

of the global projective [[model structure on simplicial presheaves]] onany [[small category]] $C$ at any [[set]] $A$ of morphisms, i.e. for every [[combinatorial model category]] $C$.
This is example 4.4 in [Guillou](http://www.math.uiuc.edu/~bertg/EquivModels.pdf#page=7).

For $A = \{C(\{U_i\}) \to X\}$ the collection of [[Cech cover]]s for all [[sieve|covering families]] of a [[Grothendieck topology]] on $D$, this are the standard [[models for ∞-stack (∞,1)-toposes]] $\mathbf{H}$.

This way the above theorem provides a model for $G$-equivariant refinements of [[∞-stack]] [[(∞,1)-topos]]es.

* For instance [[motivic cohomology]] is the cohomology of the [[∞-stack]] [[(∞,1)-topos]] on the [[Nisnevich site]], presented by $C := L_{Cech} SPSh(Nis)$ . Its $G$-equivariant version as above should be the right context for the [[Bredon cohomology|Bredon]] $G$-[[equivariant cohomology]] refinement of [[motivic cohomology]].

  This is example 4.5 in [Guillou](http://www.math.uiuc.edu/~bertg/EquivModels.pdf#page=8).

  (Actually here one localizes moreover at [[hypercover]]s and at [[A1-homotopy theory|A1-homotopies]].)





## Related concepts



Equivariant homotopy theory is to [[equivariant stable homotopy theory]] as [[homotopy theory]] is to [[stable homotopy theory]].

## References

* [[Peter May]], _Equivariant homotopy and cohomology theory_ CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. With contributions by M. Cole, G. Comeza&#732;na, S. Costenoble, A. D. Elmenddorf, J. P. C. Greenlees, L. G. Lewis, Jr., R. J. Piacenza, G.
Triantafillou, and S. Waner. ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/alaska1.pdf))

The generalization of the homotopy theory of $G$-spaces and of Elmendorf's theorem to that of $G$-objects in more general [[model category|model categories]] is in 

* [[Bert Guillou]], _A short note on models for equivariant homotopy theory_ ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf))