

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