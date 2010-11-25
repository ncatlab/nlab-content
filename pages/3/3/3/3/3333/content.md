

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Stabe homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}


## Idea

In an [[(∞,1)-category]] $C$ with $(\infty,1)$-[[pullback]]s, the _free loop space object_ $\mathcal{L}X$ of any object $X$ is an object that behaves as if its [[generalized element]]s are loops in $X$, morphisms between generalized elements [[homotopy|homotopies]] of loops, and so on.

For the case that $C = $ [[Top]] this reproduces the ordinary notion of free [[loop space]] objects of [[topological space]]s.

Over each fixed element $x \in X$, the free loop space object $\mathcal{L}X$ looks like the based [[loop space object]] $\Omega_x X$ of $X$.

Free loop space objects come naturally equipped with various structures of interest, such as a categorical circle action. The [[cohomology]] of $\mathcal{L}X$ is [[Hochschild cohomology]] or [[cyclic cohomology]] of function algebras $C(X)$ on $X$. The categorical circle action induces [[differential]]s on these cohomolgies, identifying them, in suitable cases, with algebras of [[Kähler differential|Kähler]] [[differential form]]s on $X$.


## Definition

+-- {: .un_defn}
###### Definition

In an [[(∞,1)-category]] $C$ with [[(∞,1)-pullback]]s, for $X \in C$ an [[object]], its **free loop space object** $\mathcal{L}X$ is the $(\infty,1)$-pullback

$$
  \array{
    \mathcal{L} X &\to& X
    \\
    \downarrow && \downarrow^{\mathrlap{(Id,Id)}}
    \\
    X &\stackrel{(Id,Id)}{\to}& X \times X
  }
  \,.
$$

=--

+-- {: .un_remark}
###### Remark


This is the $(\infty,1)$-categorical [[span trace]] of the identity-[[span]]

$$
  \mathcal{L}X =
  Tr
  \left(
    \array{
       && X
       \\
       & {}^{\mathllap{Id}}\swarrow && \searrow^{\mathrlap{Id}}
       \\
       X &&&& X
    }
  \right)
  \,.
$$

=--

## Properties


### Models by homotopy pullbacks {#HomPullModel}

To see what the definition of a free loop space objectamounts to in more detail, assume that the [[(∞,1)-category]] is modeled by a [[homotopical category]], say for simplicity a [[category of fibrant objects]], for instance the full subcategory on fibrant objects of a [[model category]]. 

Then following the discussion at [[homotopy pullback]] and [[generalized universal bundle]] we can compute the about $(\infty,1)$-pullback as the ordinary [[limit]] 

$$
  \array{
    \mathcal{L}X &\to& &\to& X
     \\
    \downarrow && && \downarrow^{\mathrlap{(Id,Id)}}
    \\
    && (X \times X)^I &\stackrel{(d_0,d_0)}{\to}& X \times X
    \\
    \downarrow &&  {}^{\mathllap{(d_1,d_1)}}\downarrow
    \\
    X &\stackrel{(Id,Id)}{\to} &  X \times X
    \,,
  }
$$

where $(X\times X)^I$ is a [[path space object]] for $X \times X$.  At least if we have the structure of a [[model category]] we may take $(X \times X)^I = X^I \times X^I$ for a [[path space object]] $X^I$ of $X$. 

From this description one sees that $\mathcal{L}X$ is built from _pairs of paths_ in $X$ with coinciding endpoints, that are _glued at their coinciding endpoint_ . So the loops here are all built from two semi-ciricle paths.



### Relation to based loop space object

The fiber of $\mathcal{L}X$ over a [[point]] $x : {*} \to X$ is the corresponding (based) [[loop space object]] $\Omega_x X$ of $X$: we have an $(\infty,1)$-[[pullback]] diagram

$$
  \array{
    \Omega_x X &\to& \mathcal{L}X &\to& X
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{(Id,Id)}} 
    \\
    {*} &\stackrel{x}{\to} & X &\stackrel{(Id,Id)}{\to}& X\times X
  }
  \,.
$$

To see this, use that [[homotopy pullback]]s paste to homotopy pullbacks, so that the outer pullback is modeled by the ordinary [[limit]]

$$
  \array{
    \Omega_x^{I \vee I}X &\to& &\to& X
     \\
    \downarrow && && \downarrow^{\mathrlap{(Id,Id)}}
    \\
    && (X \times X)^I &\stackrel{(d_0,d_0)}{\to}& X \times X
    \\
    \downarrow &&  {}^{\mathllap{(d_1,d_1)}}\downarrow
    \\
    {*} &\stackrel{(x,x))}{\to} &  X \times X
    \,,
  }
$$

which builds based loops on $X$ from two consecutive paths, the first starting at the basepoint $x$, the second ending there. This is weakly equivalent $\Omega_x X = \Omega^I_x X \stackrel{\simeq}{\to} \Omega^{I \vee I} X$ to the based [[loop space object]] $\Omega_x X$ built from just the path space object $X^I$ with a single copy of $I$, by standard arguments as for instance form page 12 on in 

* [[Kenneth Brown]], _[[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]_ .

### In an $(\infty,1)$-topos {#InATopos}

We consider now the case that $C = \mathbf{H}$ is an  [[(∞,1)-topos]] (of [[(∞,1)-sheaves]]/[[∞-stack]]s). This comes canonically with its [[terminal object|terminal]] [[global section]]s [[(∞,1)-geometric morphism]]

$$
  (LConst \dashv \Gamma) : \mathbf{H} \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
  \,.
$$ 

#### As a mapping space object {#AsMappingSpaceObject}

+-- {: .un_defn}
###### Definition/Proposition

Write 

$$
  S^1 \in Top \simeq \infty Grpd \stackrel{LConst}{\hookrightarrow} \mathbf{H}
$$

for the [[circle]]. In [[Top]] this is the usual topological circle. In [[∞Grpd]] this is (the [[homotopy type]] of) the [[fundamental ∞-groupoid]] of the topological circle. We may think of this as the [[(∞,1)-pushout]]

$$
  S^1 \simeq * \coprod_{* \coprod *} *
$$

hence as the universal [[cocone]]

$$
  \array{
    * \coprod * &\to& *
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    * &\to& S^1
  }
$$

in $\infty Grpd$. 

In $\mathbf{H}$ we still write $S^1$ for the [[constant ∞-stack]] on this, the image of this under $LConst$. Since $LConst$ is a [[left adjoint]] and hence preserves this poushout, there is no risk of confusion.

=--

+-- {: .proof}
###### Proof

To see that the given $(\infty,1)$-pushout indeed produces the circle, we use the standard [[model structure on simplicial sets]] $sSet_{Quillen}$ to [[presentable (∞,1)-category|present]] [[∞Grpd]]. In $sSet_{Quillen}$ the $(\infty,1)$-pushout is computed by the [[homotopy pushout]]. By general facts about this, it may be computed as an ordinary [[pushout]] in [[sSet]] once we pass to an equivalent pushout diagram in which at least one morphism is a [[monomorphism]]. This is the case for

$$
  \array{
    * \coprod * &\to& *
    \\
    \downarrow && \downarrow
    \\
    \Delta[1] &\to& \Delta[1]/\partial \Delta[1]
  }
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

Informally the $(\infty,1)$-pushout $* \coprod_{* \coprod *} *$ may be thought of as 

* the disjoint union of two points $*_1$, $*_2$;

* equipped with _two_ non-equivalent abstract [[homotopies]] between them

  $$
    S^1 
    =
   \left\{
    \array{
       & \nearrow \searrow^{\mathrlap{\simeq}}
       \\
       *_1 && *_2
       \\
       & \searrow \nearrow_{\mathllap{\simeq}}
    }
    \right\}
    \,.
  $$ 

This equivalent way of modelling the circle not as a single point with an automorphism, but as two points with two isomorphisms is what connects directly to the definition of the free loop space object. This we now come to. It is also the fundamenal source of the basic structure of [[Hochschild cohomology|Hochschild (co)homology]] (as discussed there).

=--

+-- {: .un_lemma}
###### Observation


Every [[(∞,1)-topos]] is a [[cartesian closed (∞,1)-category]]: we have for every object $X \in \mathbf{H}$ an [[internal hom]]-[[(∞,1)-functor]]

$$
  [X,-] : \mathbf{H} \to \mathbf{H}
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is discussed at [[(∞,1)-topos]] in the section <a href="http://ncatlab.org/nlab/show/(infinity,1)-topos#ClosedMonoidalStructure">Closed monoidal structure</a>.

=--

+-- {: .un_prop}
###### Proposition

There is a natural [[equivalence in an (∞,1)-category|equivalence]]

$$
  \mathcal{L}X \simeq [S^1 , X]
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows from the above by the fact (see <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-topos#ClosedMonoidalStructure">closed monoidal structure on (∞,1)-toposes</a>) that the internal hom in an $(\infty,1)$-topos preserves finite colimits in its first argument and satisfies 

$$
  [*,X] \simeq X
  \,.
$$

This yields

$$
  \begin{aligned}
    [S^1 ,X] &\simeq [* \coprod_{* \coprod *} *, X]
    \\
      & \simeq
      [*,X] \times_{[* \coprod *, X]} [*,X]
     \\
      & \simeq X \times_{X \times X} X
     \\
     & \simeq \mathcal{L}X
     \,.
  \end{aligned}
$$

=--

+-- {: .un_prop}
###### Corollary

We have that the free loop space object of $X \in \mathbf{H}$ is equivalently the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#Tensoring">powering</a> of $X$ by the $\infty$-groupoid $S^1$:

$$  
  \mathcal{L} X \simeq X^{S^1}
$$

=--

+-- {: .proof}
###### Proof

Follows by the above from the equivalence $[LConst S^1 , X] \simeq X^{S^1}$ discussed at [[(∞,1)-topos]].

=--

#### Intrinsic circle action



By precomposition, the [[automorphism 2-group]] of the [[circle]] $S^1$ acts on free loop space of an object $X \in \mathbf{H}$

$$
  Aut(S^1) \times [S^1, X] 
  \to 
  [S^1, S^1] \times [S^1, X] \stackrel{\circ}{\to} [S^1, X]
  \,.
$$


+-- {: .un_prop}
###### Proposition

The connected component of $[S^1,S^1]$ on the identity is equivalent to $S^1$

$$
  [S^1 , S^1]_{Id} \simeq S^1
$$

=--

+-- {: .un_def}
###### Definition

We say that

$$
  S^1 \times [S^1, X] 
    \simeq
  [S^1, S^1]_{Id} \times [S^1, X]
  \stackrel{\circ}{\to} 
  [S^1, X]
$$

is the intrinsic **circle action** on the free loop space object.

=--

+-- {: .proof}
###### Proof

We spell out in detail what this action looks like.
The reader should thoughout keep the [[homotopy hypothesis]]-equivalence, $(|-| \dashv \Pi) : Top \simeq \infty Grpd$ in mind.

We may realize the [[circle]] $S^1 \in $ [[Top]] under $\Pi : Top \simeq \infty Grpd$ as the [delooping]] [[groupoid]] $\mathbf{B}\mathbb{Z}$ of the additive [[group]] $\mathbb{Z}$ of [[integer]]s 

The [[automorphism 2-group]] of this object is the [[functor category|functor groupoid]]

$$
  Aut_{Grpd}(\mathbf{B}\mathbb{Z})
$$

whose [[object]]s are invertible [[functor]]s $\mathbf{B}\mathbb{Z} \to \mathbf{B}\mathbb{Z}$ and whose [[morphism]]s are [[natural transformation]]s between these. 

The functors $\mathbf{B}\mathbb{Z} \to \mathbf{B}\mathbb{Z}$ correspond bijectively to group [[homomorphism]]s $\mathbb{Z} \to \mathbb{Z}$, hence to multiplication by $n\in\mathbb{Z}$

$$
  [n] : \mathbf{B}\mathbb{Z} \to \mathbf{B}\mathbb{Z}
$$

$$
  (\bullet \stackrel{k}{\to} \bullet) \mapsto (\bullet \stackrel{n\cdot k}{\to} \bullet).
$$

Natural transformations between two such endomorphisms are given by a component $\ell \in \mathbb{Z}$ such that all diagrams

$$
  \array{
    \bullet &\stackrel{\ell}{\to}& \bullet
    \\
    {}^{\mathllap{n\cdot k}}\downarrow && \downarrow^{\mathrlap{n' \cdot k}}
    \\
    \bullet &\stackrel{\ell}{\to}& \bullet    
  }
$$

commute in $\mathbf{B}\mathbb{Z}$. This can happen only for $n = n'$, but then it happens for arbitrary $\ell$. 

In other words we have

$$
  Aut(\mathbf{B}\mathbb{Z}) \simeq 
  \coprod_{[n] \in \mathbb{Z}^\times}\mathbf{B}\mathbb{Z}
  \,.
$$

and 

$$
Aut_{Id}(\mathbf{B}\mathbb{Z}) \simeq \mathbf{B}\mathbb{Z}
  \,.
$$

The object $[n]$ corresponds to the self-mapping of the circle that fixes the basepoint and has winding number $n\in\mathbb{Z}$. The transformation $\ell$ corresponds then to a rigid rotation of the loop by $\ell$ full circles

Notably for $n = 1$ and $k = 1$ we may think of the diagram

$$
  \array{
    \bullet &\stackrel{\ell}{\to}& \bullet
    \\
    {}^{\mathllap{1}}\downarrow && \downarrow^{\mathrlap{1}}
    \\
    \bullet &\stackrel{\ell}{\to}& \bullet    
  }
$$

as depicting the unit loop around the circle (on the left, say) and the result of translating its basepoint $\ell$-times around the circle (the rest of the diagram). Of course since we are using a model of $S^1$ with a single object here, every rotation of the loop is a full circle rotation, which is a bit hard to see.

=--

> Exercise: spell out the above discussion analogously for the equivalent model given by the [[fundamental groupoid]] $\Pi_1(S^1)$ of the standard circle. The is the groupoid with $S^1_{Top}$ as its set of objects homotopy classes of paths in the circle as morphisms. In this model things look more like one might expect from a circle action. Notice that $\mathbf{B}\mathbb{Z}$ is the [[skeleton]] of $\Pi_1(S^1)$.

+-- {: .un_example}
###### Example

Consider $\mathbf{H} = $ [[∞Grpd]], $G$ a [[group]] and  $X = \mathbf{B}G$ the [[delooping groupoid]]. Then $\mathcal{L}X = G//_{Ad}G$ (as discussed in detail [below](#LoopsInBG)). A morphism $(g \stackrel{h}{\to} Ad_h a)$ in $G//G$ corresponds to a natural transformation

$$
  \array{
    & \nearrow \searrow^{\mathrlap{g}}
    \\
    \mathbf{B}\mathbb{Z}
    &\Downarrow^{h}&
    \mathbf{B}G
    \\
    & \searrow \nearrow_{\mathrlap{Ad_h g}}
  }
  \,.
$$

Precomposing this with the automorphism $\ell$ of the object $[n]$ in $END(\mathbf{B}\mathbb{Z})$

$$
  \array{
    & \nearrow \searrow^{\mathrlap{n}}
    \\
    \mathbf{B}\mathbb{Z}
    &\Downarrow^{\ell}&
    \mathbf{B}\mathbb{Z}
    \\
    & \searrow \nearrow_{\mathrlap{n}}
  }
$$

produces the new transformation

$$
  \array{
    & \nearrow \searrow^{\mathrlap{n}} && \nearrow \searrow^{\mathrlap{g}}
    \\
    \mathbf{B}\mathbb{Z}
    &\Downarrow^{\ell}&
    \mathbf{B}\mathbb{Z}
    &\Downarrow^{h}&
    \mathbf{B}G
    \\
    & \searrow \nearrow_{\mathrlap{n}} && \searrow \nearrow_{\mathrlap{Ad_h g}}
  }
  \,.
$$

By the rules of horizontal composition of [[natural transformation]]s, this is the transformation whose component naturality square on $(\bullet \stackrel{1}{\to} \bullet)$ in $\mathbf{B}\mathbb{Z}$ is the diagram

$$
  \array{
    \bullet &\stackrel{g^\ell}{\to}& \bullet &\stackrel{h}{\to}&\bullet
    \\
    {}^{\mathllap{g^{n}}}\downarrow && {}^{g^n}\downarrow && \downarrow^{\mathrlap{Ad_h g^n}}
   \\
    \bullet &\underset{g^\ell}{\to}& \bullet &\underset{h}{\to}&\bullet
  }
$$

in $\mathbf{B}\mathbb{Z}$, hence the morphism $(g^n \stackrel{g^{\ell} h}{\to} Ad_h g^n)$ in $G//_{Ad}G$. In particular, the categorical circle action is 
$$
\ell:(g \stackrel{h}{\to} Ad_h g)\mapsto (g \stackrel{g^{\ell} h}{\to} Ad_h g).
$$ 

=--

### Hochschild cohomology and cyclic cohomology

[[quasicoherent ∞-stack]]s on $\mathcal{L}X$ form the [[Hochschild cohomology|Hochschild homology]] object of $X$ (if the axioms of [[geometric function theory]] are met) as described there. The circle acton on $\mathcal{L}X$ induces differentials on these.

> ... details to be written, but see [[Hochschild cohomology]] and [[cyclic cohomology]] for more.




## Examples 

### Free topological loop spaces

In [[Top]] the notion of free loop space objects reproduces the standard notion of topological [[free loop space]]s.

### Details for $\mathcal{L} \mathbf{B}G$ {#LoopsInBG}

Let the ambient [[(∞,1)-category]] be [[∞Grpd]], let $G$ be an ordinary [[group]] and $\mathbf{B}G$ its one-object [[delooping]] [[groupoid]]. 

+-- {: .un_prop}
###### Proposition

We have that the [[loop groupoid]]

$$
  \mathcal{L} \mathbf{B}G \simeq G//_{Ad} G
  \,,
$$

the [[action groupoid]] of the adjoint action of $G$ on itself.

=--


+-- {: .proof}
###### Proof

We spell this out in full pedestrian detail, as a little exercise in computing [[homotopy pullback]]s.

We have that the [[path space object]] is $\mathbf{B}G^I = [I,\mathbf{B}G]$ -- the [[functor category|functor groupoid]], where $I$ is the free groupoid $I = \{a \stackrel{\simeq}{\to} b\}$ on the standard [[interval object]] -- which is (by the definition of [[natural transformation]]) the [[action groupoid]]

$$
  \mathbf{B}G^I = G\backslash \backslash G // G
$$

for the action of $G$ on itself, by _inverse_ left and direct right multiplication separately: the naturality square of a [[natural transformation]] defining a morphism $g \stackrel{h_1,h_2}{\to} h_1^{-1} g h_2$ in this groupoid is the commuting square

$$
  \array{
    \bullet &\stackrel{g}{\to}& \bullet
    \\  
    {}^{\mathllap{h_1}}\downarrow && \downarrow^{\mathrlap{h_2}}
    \\
    \bullet &\stackrel{h_1^{-1}g h_2}{\to}& \bullet    
  }
$$

in $\mathbf{B}G = {*}//G$.

The [[pullback]] of the top right corner of the above defining limit diagram is

$$
  \array{
    (G\backslash\backslash G \times 
    G\backslash\backslash G)//G
    &\to& \mathbf{B}G
    \\
    \downarrow && \downarrow^{\mathrlap{(Id,Id)}} 
    \\
    (G\backslash\backslash G//G) \times
    (G\backslash\backslash G//G)
    &\to& \mathbf{B}G \times \mathbf{B}G
  }
$$

identifying the two actions from the right, and then the remaining pullback completing the limit diagram is

$$
  \array{
    G\backslash\backslash (G\times G)//G
    &\to& 
    (G\backslash\backslash G \times 
    G\backslash\backslash G)//G
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{(Id,Id)}{\to}&  
    \mathbf{B}G \times \mathbf{B}G
  }
$$

now identifying also the two actions from the left, so that  $G\backslash\backslash (G\times G)//G$ is the [[action groupoid]] of $G$ acting diagonally on $G \times G$ by multiplication from the left and from the right, separately.

To see better what this is, we pass to an equivalent smaller groupoid (the [[homotopy pullback]] is defined, of course, only up to weak equivalence). Notice that every morphism 
$(g_1,g_2) \stackrel{h_1,h_2}{\to} (g'_1, g'_2)$ 
in $G\backslash\backslash (G\times G)//G$ corresponding to a [[natural transformation]]

$$
  \array{
     \bullet &\stackrel{(g_1,g_2)}{\to}& \bullet
     \\
     {}^{\mathllap{(h_1,h_1)}}\downarrow && \downarrow^{\mathrlap{(h_2,h_2)}}
     \\
     \bullet &\stackrel{(h_1^{-1} g_1 h_2, h_1^{-1} g_2 h_2)}{\to}
     & \bullet
  }
$$

between functors $I\times I \to \mathbf{B}G \times \mathbf{B}G$
may always be decomposed as

$$
  \array{
     \bullet &\stackrel{(g_1,g_2)}{\to}& \bullet
     \\
     {}^{\mathllap{(e,e)}}\downarrow 
     && \downarrow^{\mathrlap{(g_2^{-1}, g_2^{-1})}}
     \\
     \bullet &\stackrel{(g_1 g_2^{-1}, e)}{\to}& \bullet
     \\
     {}^{\mathllap{(h_1,h_1)}}\downarrow 
     && \downarrow^{\mathrlap{(h_1,h_1)}}
     \\
     \bullet &\stackrel{(h_1^{-1}(g_1 g_2^{-1})h_1, e)}{\to}& \bullet
     \\
     {}^{\mathllap{(e,e)}}\downarrow 
     && \downarrow^{\mathrlap{(g'_2,g'_2)}}
     \\
     \bullet &\stackrel{(h_1^{-1}(g_1 g_2^{-1})h_1 g'_2, g'_2)}{\to}& \bullet
  }
  \,.
$$

Staring at this for a moment shows that this is a unique factorization of every morphism through one of the form

$$
  \array{
    \bullet & \stackrel{(g,e)}{\to} & \bullet
    \\
    {}^{\mathllap{k}}\downarrow && \downarrow^{\mathrlap{k}}
    \\
    \bullet & \stackrel{(Ad_k g,e)}{\to} & \bullet    
  }
  \,,
$$

which is naturally identified with a morphism in the [[action groupoid]] $G//_{Ad} G$ of the adjoint action of $G$ on itself.

This means that the inclusion

$$
  G//_{Ad} G 
  \stackrel{}{\hookrightarrow}
  G\backslash\backslash(G \times G)//G
$$

given by this identification
is [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|full and faithful]], and hence an [[equivalence of categories|equivalence of groupoids]].

So in conclusion we have that the free loop space object of the [[delooping]] $\mathbf{B}G$ of a group is

$$
  \mathcal{L} \mathbf{B}G \simeq G//_{Ad}G
  \,.
$$

=--

### Chern character

We describe how the [[Chern character]] of [[vector bundle]]s over $X$ may be realized in terms of the [[cohomology]] of the free loop space object $\mathcal{L}X$.

Assume now $C$ is a nice category of smooth spaces, and let $X$ be an object of $C$.

Consider a [[group object]] $G$ in $C$ and a [[representation]] of $G$ given my a group homomorphism to the [[general linear group]] (in $C$):  $\rho:G\to GL(n;\mathbb{C})$. For instance $G$ could be $GL(n)$ itself and this morphism the identity.

The [[trace]] of the representation $\rho$ is invariant under conjugation in the group and so defnes a map $Tr(\rho): G//_{Ad}G\to \mathbb {C}$ -- a [[class function]]. By the equivalence $\mathcal{L}\mathbf{B}G \simeq G//_{Ad} G$ discussed above, this may be regarded as a [[characteristic class]]

$$
  Tr(\rho(-)) : \mathcal{L}\mathbf{B}G\to \mathbb {C}
$$

on the free loop space of $\mathbf{B}G$.

The [[cocycle]] $g : X\to \mathbf{B}G$ of a $G$-[[principal bundle]] on $X$ transgresses to a cocycle 

$$
  \mathcal{L} g : \mathcal{L}X \to \mathcal{L}\mathbf{B}G
$$

on the free loop space, by the functoriality of the free loop space object construction.

The above [[characteristic class]] of this cocycle is the composite morphism

$$
  Tr(\rho(\mathcal{L}g)) : \mathcal{L}X \to \mathcal{L} \mathbf{B}G \to \mathbb{C}
  \,,
$$

which by the $Ad$-invariance of the [[trace]] is now $S^1$-invariant and hence defines an element in the [[cyclic cohomology]]
$C(\mathcal{L}X,\mathbb{C})^{S^1_C}$ of $X$. 

The Hom-space $C(\mathcal{L}X,\mathbb{C})$ is a model for the graded commutative algebra of complex-valued [[differential form]]s on $X$, with the categorical circle action corresponding to the [[de Rham complex|de Rham differential]]. Hence $C(\mathcal{L}X,\mathbb{C})^{S^1_C}$ is a model for closed forms and maps to [[de Rham cohomology]] $H_{dR}^\bullet(X)$ of $X$. If the [[de Rham theorem]] holds for $X$ in $C$, then this may be identified with the real cohomology $H^\bullet(X,\mathbb{R})$.



In the case that $G=GL(\infty;\mathbb{C})$, the compatibility of the trace with [[direct sum]]s and [[tensor product]]s of [[vector bundle]]s over $X$ makes the above construction a [[ring]] homomorphism $K(X)\to H_{dR}(X)$ from the [[topological K-theory]] of $X$ to [[de Rham cohomology]], hence a very good candidate to being the [[Chern character]] 

( _to be completed..._ )



## Related concepts

* [[loop space object]] / [[delooping]]

* **free loop space object** / [[derived loop space]]




## References

Free loop space objects in the [[(∞,1)-topos]] of [[derived stack]]s on the site of [[differential graded algebra]]s are discussed in

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Connections_ ([arXiv](http://arxiv.org/abs/1002.3636))

More information in the topological case is given in:

* [[Ronnie Brown]] _Crossed modules and the homotopy 2-type of a free loop space_, ([arXiv](http://arxiv.org/abs/1003.5617))

which gives complete information on the 2-type of $LX$ for a space $X$ which is the classifying space of a crossed module of groups. This generalises the above example of  $ \mathcal{L} \mathbf{B}G$. 

[[!redirects free loop space objects]]