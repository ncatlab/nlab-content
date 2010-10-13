

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}
 
## Idea

The definition of _cohesive topos_ or _category of cohesion_ aims to axiomatize properties of a [[topos]] that make it a [[gros topos]] of [[space]]s inside of which [[geometry]] may take place.

The idea behind the term is that a _geometric space_ is roughly something consisting of points or pieces that are _held together_ by some cohesion - for instance by [[topology]], by [[smooth structure]], etc.

The canonical [[global section]] geometric morphism $\Gamma : E \to Set$ of a cohesive topos over [[Set]] may be thought of as sending a space $X$ to its underlying set of points $\Gamma(X)$. Here $\Gamma(X)$ is $X$ with all _cohesion forgotten_ (for instance with the topology or the smooth structure forgotten)

Conversely, the [[left adjoint]] and [[right adjoint]] of $\Gamma$

$$
  E 
    \stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
  S
$$

send a set $S$ either to the [[discrete space]] $Disc(S)$ with _discrete_ cohesive structure (for instance with [[discrete topology]]) or to the [[codiscrete space]] $Codisc(S)$ with the _codiscrete_ cohesive structure (for instance with [[codiscrete topology]]) .

Moreover, the idea is that cohesion makes points lump together to _connected pieces_ . This is modeled by one more functor $\Pi : E \to S$ [[left adjoint]] to $Disc$. In the context of 1-[[topos theory]] this sends a cohesive space to its [[connected topos|connected componets]] $(\Pi = \pi_0)$. More generally in an [[(n,1)-topos]]-theory context, $\Pi$ sends a cohesive space $X$ to the $n$-[[truncated|truncation]] of its [[geometric homotopy groups in an (∞,1)-topos|geometric fundamental ∞-groupoid]] $\Pi(X)$.

In total this gives a quadruple of [[adjoint functor]]s

   $$
    (\Pi \dashv Disc \dashv \Gamma \dashv Codisc) : 
    E
     \stackrel{\stackrel{\overset{\Pi}{\to}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
    S
    \;
   $$

A cohesive topos is a topos whose terminal [[geometric morphism]] admits an extenson to such a quadruple of adjoints, satisfying some further properties.

## Definition

+-- {: .un_defn}
###### Definition

A [[topos]] $E$ over some base topos $S$, i.e. equipped with a [[geometric morphism]]

$$
  (f^* \dashv f_*) E \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
  S
$$

is **cohesive** or  **a topos of cohesion** if it has the following [[stuff, structure, property|properties]]:

1. it is _local_ and _connected_ in the following sense:

   1. it is a [[locally connected topos]]: there exists a further [[left adjoint]] $(f_! \dashv f^*)$;

   1. it is a [[connected topos]]: the functor $f_!$ preserves the [[terminal object]];

   1. it is _strongly connected_ : $f_!$ preserves even all [[finite]] [[product]]s;

   1. it is a [[local topos]]: there exists a further [[right adjoint]] $(f_* \dashv f^!)$;

   1. this makes $S \stackrel{f^!}{\hookrightarrow} E$ a [[subtopos]]: $f^!$ is a [[full and faithful functor]];

   so that in total we have a quadruple of [[adjoint functor]]s
   
   $$
    (f_! \dashv f^* \dashv f_* \dashv f^!) : 
    E
     \stackrel{\stackrel{\overset{f_!}{\to}}{\overset{f^*}{\leftarrow}}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
    S
    \;
   $$

1. $f_!$ is continuous in that for all $s \in S$ and $e \in E$ the natural morphism

   $$
     f_! (e^{f^* s}) \stackrel{\simeq}{\to} (f_!(e))^s
   $$

   is an [[isomorphism]]

   (this morphism is the [[internal hom]]-[[adjunct]] of 
   $
     s \times f_!(e^{f^* s}) 
      \stackrel{\simeq}{\to}
     f_!f^*(s) \times f_!(e^{f^* s})
      \stackrel{\simeq}{\to}
     f_!(f^*(s) \times e^{f^* s})
     \to
     f_!(e)
   $
   where we use that by definition $f^*$ is full and faithful and then that $f_!$ preserves products); 

1. the [[natural transformation]]

   $$
     f_*  
       \stackrel{\simeq}{\to} 
     f_* ( f^*  f_* )
       \stackrel{}{\to}
     f_* ( Id ) 
       \stackrel{}{\to}
     f_*( f^* f_! )
       \stackrel{\simeq}{\to}
     f_!
   $$

   is an [[epimorphism]], equivalently the transformation

   $$
     f^* \to f^!
   $$

   is a [[monomorphism]].

=--

## Examples

* Every topos is cohesive over itself.

### Smooth sets


+-- {: .un_theorem}
###### Theorem

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is a cohesive topos over [[Set]].

=--

We first show that it is a [[locally connected topos]] in that the terminal [[global section]] [[geometric morphism]] to [[Set]] is an [[essential geometric morphism]]

$$
  Sh(CartSp)
  \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{L Const}{\leftarrow}}{\underset{\Gamma}{\to}}}
  Set
$$

and show that the extra [[left adjoint]] $\Pi_0 : Sh(CartSp) \to Set$ sends diffeological spaces to the set of path-[[connected]] components of their underlying [[topological space]]s.


+-- {: .un_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is a [[locally connected topos]].

=--

+-- {: .proof}
###### Proof

The following argument works for every [[site]] $C$ which is such that constant presheaves on $C$ are already sheaves.

Notice that this is the case for $C = CartSp$ because every Cartesian space is connected: for $S \in Set$ a compatible family of elements of $Const S$ on a cover $\{U_i \to \mathbb{R}^n\}$ of some $\mathbb{R}^n$ is an element of $S$ on each patch, such that their restriction maps to intersections of patches coincide. But the restriction maps are all identities, so this says that all these elements coincide. Therefore the set of compatible families is just the set $S$ itself, hence the presheaf $Const S$ is a sheaf.

So with $L : PSh(C) \to Sh(C)$ the [[sheafification]] functor we have that $L Const S \simeq Const S$.

Whenever this is the case the [[left adjoint]] to the constant presheaf functor, which always exists for presheaves and is given by the [[colimit]] functor, is also left adjoint on the level of sheaves, because for each $X \in Sh(C)$ and $S \in Set$ we have natural bijections

$$
  \begin{aligned}
    Hom_{Sh(C)}(X, L Const S)
    & =
    Hom_{PSh(C)}(X, L Const S)
    \\
    & \simeq
    Hom_{PSh(C)}(X, Const S)
    \\
    & \simeq
    Hom_{Set}(\lim_\to X, S)
  \end{aligned}
  \,.
$$

=--

+-- {: .un_def}
###### Definition

Write $\Pi_0 := \lim_\to : Sh(CartSp) \to Set$
for the [[left adjoint]] to $LConst : Set \stackrel{Const}{\to} PSh(C) \stackrel{L}{\to} Sh(C)$.

=--

+-- {: .un_prop}
###### Proposition

For $X \in Sh(C)$ a diffeological space, $\Pi_0(X)$ is the set of path-connected components of the topological space underlying $X$.

=--

+-- {: .proof}
###### Proof

By the [[co-Yoneda lemma]] we may write 

$$
  X = {\lim_\to}_{(U \to X) \in y/X} U
$$

and since $\Pi_0$ commutes with colimits we have

$$
  \Pi_0(X) \simeq 
  \Pi_0 {\lim_\to}_{(U \to X)} U
  \simeq
  {\lim_\to}_{(U \to X)} \Pi_0(U)
  \,.
$$

But also by the co-Yoneda lemma we have that the [[colimit]] over any [[representable functor|representable]] is the singleton set, hence our expression

$$
  \cdots \simeq 
  {\lim_\to}_{(U \to X)} *
$$

is the colimit over the category of plots of $X$ of the functor that is constant on the point. This colimit is the [[coproduct]] of points over the connected components of the [[diagram]] category.

The connected components of the category of plots $y/X$ are the path-connected (or "plot-connected") components of the underlying topological space of $X$.



=--


+-- {: .un_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is even a [[connected topos]].

=--

+-- {: .proof}
###### Proof

Since $CartSp$ is a [[connected category]] it is immediate that $Const : Set \to PSh(CartSp)$ is a [[full and faithful functor]]. By the above this equals $L Const$, which is hence also full and faithful.

By the discussion at [[connected topos]] we could equivalently convince ourselves that $\Pi_0$ preserves the terminal object. The terminal object of $Sh(CartSp)$ is $y(\mathbb{R}^0)$, hence representable. By the above, $\Pi_0$ sends all representable objects to the singleton set, which is the terminal object of $Set$. 

=--

#### Diffeological spaces

A _reflective localization_ at a collection of morphisms $W$ is a [[reflective subcategory]] on [[local object]]s, those $A$ for which for all $w \in W$ we have that $A^w$ is an isomorphism.

We say a **quasi-localization** is similarly a full subcategory on objects such that $A^w$ in a [[monomorphism]].



+-- {: .un_prop}
###### Proposition

The [[quasitopos]] of [[diffeological space]]s 

$$
  Diffeol \hookrightarrow Sh(CartSp)
$$

is the reflective quasi-localization at the counits  $Disc \Gamma U \to U$ for $U \in CartSp$.

=--

+-- {: .proof}
###### Proof

For $X \in Sh(CartSp)$ we have

$$
  Hom(Disc \Gamma U , X) 
    \simeq
  Hom_{Set}(\Gamma U , \Gamma X)
  \,.
$$

So we need to check for which $X$ we have for all $U\in CartSp$ that

$$
  Hom(U,X) \to Hom_{Set}(\Gamma(U), \Gamma(X))
$$

is a monomorphism.

The [[image]] of this morphism is $Hom(U, Conc(X))$, the plots of the [[concrete sheaf|concretization]] of $X$: the [[diffeological space]] underlying $X$. So we have a factorization of our morphism as

$$
   Hom(U,X) 
    \hookrightarrow
   Hom(U, Conc(X))
   \hookrightarrow
  Hom_{Set}(\Gamma U , \Gamma X)
  \,,
$$

where the second morphims is a monomorphism. So for the total morphism to be a monomorphism we need that the image-projection is. But since that is already an epimorphism, it follows that we need that the image projection is an isomorphism, hence that $X$ is already a [[concrete sheaf]].

So the concrete sheaves on $CartSp$, hence the [[diffeological space]]s, are precisely the quasi-localization at the morphisms $Disc \Gamma U \to U$.

=--

### $\infty$-Lie groupoids

* The [[(∞,1)-category of (∞,1)-sheaves]] $(\infty,1)Sh(CartSp) = $ [[?LieGrpd]] on [[CartSp]] is a cohesive $(\infty,1)$-topos over [[∞Grpd]]. (See there for the moment)


### Interpretation of cohesive $(\infty,1)$-toposes

We list the geometric meaning of the various morphisms and structures in
a cohesive [[(∞,1)-topos]] over [[∞Grpd]]. (We follow the entries [[schreiber:structures in an (∞,1)-topos]] and [[schreiber:differential cohomology in an (∞,1)-topos]] where more motivation and justification for these interpretations can be found.)

Write

$$
 (\Pi \dashv Disc \dashv \Gamma \dashv Codisc) : 
 \mathbf{H}
  \stackrel{\stackrel{\overset{\Pi}{\to}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
 \infty Grpd
$$

for the given cohesive $(\infty,1)$-topos. Its objects $X,A \in \mathbf{H}$ we ay think of as [[∞-groupoid]] with cohesive structure. For instance in the case of $\mathbf{H} = $ [[?LieGrpd]] they are $\infty$-groupoids with _smooth_ structure. Then

* $\Gamma(X)$ is the _underlying $\infty$-groupoid_ of the cohesive $\infty$-groupoid $X$ (for instance an $\infty$-Lie groupoid with its smooth structure forgotten);

* $\Pi(X)$ is the fundamental [[path ∞-groupoid]] of $X$: its [[k-morphism]]s are generated from $k$-dimensional smooth paths in $X$ and the $k$-morphisms of $X$ itself. Under the equivalence of $(\infty,1)$-toposes 

  $|-| :$  [[∞Grpd]] $\stackrel{\simeq}{\to}$ [[Top]] 


  we may think of $|\Pi(X)|$ as the _geometric realization_ of $X$. For instance if $X \in \infty LieGrpd$ is a [[paracompact manifold]], then $|\Pi(X)|$ is, up to [[weak homotopy equivalence]] its underlying topological space.

Write 

$$
  (\mathbf{\Pi} \dashv \mathbf{\flat})
  = 
  (Disc \Pi \dashv Disc \Gamma) : \mathbf{H} \to \mathbf{H}
  \,.
$$


Then unit and counit of the [[adjunction]]s give canonical natural morphisms

* $X \to \mathbf{\Pi}(X)$ -- this we may think of as the inclusion of $X$ as the constant paths in the [[path ∞-groupoid]] $\mathbf{\Pi}(X)$;

* $\mathbf{\flat}A \to A$ -- if we think of $A$ as the coefficient object for $A$-[[principal ∞-bundle]]s in $\mathbf{H}$, 

  $$  
    A Bund(X) := \mathbf{H}(X,A)
  $$

  then this is the map that takes principal $A$-bundles with [[schreiber:differential cohomology in an (∞,1)-topos|flat connection]] 

   $(X \to \mathbf{\flat}A) \leftrightarrow (\mathbf{\Pi}(X) \to A)$ to the underlying $A$-bundle.

  If $A = \mathbf{B}G$ is the [[delooping]] of an [[∞-group]] object, then we may think of $\mathbf{\flat} \mathbf{B}G$ or rather the corresponding  $Disc(\mathbf{B}G)$ as being $K(G,1)$: the classifying object for $G$-principal bundles where all cohesive structure on $G$ has been forgotten.

  Accordingly, the canonical map

  $$
    Disc(\mathbf{B}G) \to \Pi \mathbf{B}G
  $$

  that apppears in the second clause of the definition of cohesive topos is the inclusion of the topologist's $K(G,1)$ into the topological [[classifying space]] $\mathcal{B}G$. Again, on [[cocycle]]s this is the map from flat bundles to the underlying bundles.



## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

* [[connected topos]] / [[∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* **cohesive topos** / [[cohesive (∞,1)-topos]]




## References

The definition of a category of cohesion was proposed in

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))


The observation that $Sh(CartSp)$ is a [[local topos]] and that this serves to characterize [[diffeological space]]s was amplified by [[David Carchedi]].

[[!redirects cohesive toposes]]
[[!redirects cohesive topoi]]

[[!redirects category of cohesion]]
[[!redirects categories of cohesion]]

[[!redirects cohesive (∞,1)-topos]]