+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[group object]] in an ordinary [[category]] $C$ with [[pullback]]s is an [[internalization|internal]] [[group]]. More generally, there is the notion of an [[internal groupoid]] in a category $C$.

By the logic of [[vertical categorification]], an **internal $\infty$-group** or **[[internal ∞-groupoid]]** may be defined as a group(oid) object internal to an [[(∞,1)-category]] $C$ with [[(∞,1)-pullbacks]]. As described there, in full generality this involves not only a weakening of the usual [[associativity]] and [[unit laws]] up to [[homotopy]], but requires specification of [[coherence]] laws of these homotopies up to higher homotopy, and so on.


A _group object_ in an [[(∞,1)-category]] generalizes and unifies two familiar concepts:

* it is the generalization of the notion of groupal [[Jim Stasheff|Stasheff]] $A_\infty$-[[A-infinity-space|space]] from [[Top]] to more general [[(∞,1)-sheaf (∞,1)-toposes]]: an object that comes equipped with an associative and invertible [[monoid]] structure, up to [[coherence|coherent]] [[homotopy]], and possibly only [[horizontal categorification|partially defined]] (see also [[looping and delooping]] for more on this) ;

* it generalizes the notion of _[[equivalence relation]]_ -- or rather the [[internalization|internal]] notion of _[[congruence]]_  -- from [[category theory]] to [[(∞,1)-category theory]].

Of particular relevance are such group objects that define [[quotient object|effective quotients]]

* these are [[delooping|deloopable]];

* these generalize the notion of [[regular epimorphism]];

* these serve to characterize [[regular category|regular (∞,1)-categories]] -- such as [[∞-stack]] [[(∞,1)-topoi]] -- as those where every such object is an [[quotient object|effective quotient]].

A _groupoid object_ is then accordingly the [[horizontal categorification|many-object]] version of a [[group object]]. 

But notice the following. Since this is defined [[internalization|internal]] to an [[(∞,1)-category]], externally these look like genuine [[∞-groupoid]] and [[∞-group]] objects. For instance a [[group object]] in a [[(2,1)-category]] such as [[Grpd]] is, externally, a [[2-group]].

Also notice that if the ambient $(\infty,1)$-category is in fact an [[(∞,1)-topos]], then every object in there may already be thought of as an "∞-groupoid with geometric structure" (see for instance the discussion at [[cohesive (∞,1)-topos]], but this is true more generally).
The relation between the _internal groupoid objects_ then and the objects themselves is (an [[horizontal categorification|oid-ification]]) of that of [[looping and delooping]]. Notably for $G$ any internal group object (externally an [[∞-group]]) the corresponging ordinary object is its [[delooping]] object $\mathbf{B}G$, and every [[pointed object|pointed]] [[n-connected object in an (infinity,1)-topos|connected]] object in the $(\infty,1)$-topos arises this way from an internal group object.

A groupoid object

$$
 \cdots C_2 \stackrel{\to}{\stackrel{\to}{\to}} C_1 \stackrel{\to}{\to} C_0
$$

being **effective** means that it is the [[Cech nerve]] 

$$
 \cdots 
  C_0 \times_{C_0//C_1} C_0 \times_{C_0//C_1} C_0 
  \stackrel{\to}{\stackrel{\to}{\to}} 
  C_0 \times_{C_0//C_1} C_0  
 \stackrel{\to}{\to} C_0
$$

of its [[quotient stack]] $C_0 \sslash C_1$ (the  [[(∞,1)-colimit]] over its diagram)

$$
 \cdots C_2 \stackrel{\to}{\stackrel{\to}{\to}} C_1 \stackrel{\to}{\to} C_0
  \to
  C_0//C_1 := colim_i C_i
  \,.
$$

Accordingly, groupoid objects in an $(\infty,1)$-category play a central role in the theory of [[principal ∞-bundles]].

Notice that one of the four characterizing properties of an [[(∞,1)-topos]] by the higher analog of the [[Giraud theorem]] is that all [[groupoid objects in an (infinity,1)-topos are effective]].


## Definition (complete Segal-space style)


### Groupoid object

The following definition follows in style the definition of a [[complete Segal space]] object.


+-- {: .num_defn}
###### Definition

For $C$ an [[(∞,1)-category]], a **groupoid object** in $C$ is a [[simplicial object in an (∞,1)-category]]

$$
  A : \Delta^{op} \to C
$$ 

such that for all partitions $S \cup S'$ of $[n]$ that share precisely one vertex $s$, we have that

$$
  \array{
    A([n]) &\to & A(S)
    \\
    \downarrow && \downarrow
    \\
    A(S') &\to& A(\{s\})
  }
$$

is a [[(∞,1)-pullback]] diagram in $C$. Here, by a partition $S \cup S'$ of $[n]$ that share precisely one vertex $s$, we mean two subsets $S$ and $S'$ of $\{0,1,\ldots,n\}$ whose union is $\{0,1,\ldots,n\}$ and whose intersection is the singleton $\{s\}$. The linear order on $[n]$ then restricts to the linear order on $S$ and $S'$. 

The $(\infty,1)$-category of groupoid objects in $C$ is the full [[sub-(∞,1)-category]] 

$$
  Grpd(C) \hookrightarrow Func(\Delta^{op}, C)
$$

of the [[(∞,1)-category of (∞,1)-functors]] on those objects that are groupoid objects.

=--

This is [[Higher Topos Theory|HTT, prop. 6.1.2.6, item 4'']] with [[Higher Topos Theory|HTT, def. 6.1.2.7]].

+-- {: .num_remark}
###### Remark

If one requires the above condition only for those partitions that are order-preserving, then this yields the definition of a (pre-)[[category object in an (∞,1)-category]].

=--


+-- {: .num_defn}
###### Definition 

A groupoid object $A : \Delta^{op} \to C$ is the **[[Cech nerve]]** of a morphism $A_0 \to B$ if $A$ is the restriction of an augmented simplicial object $A^+ : \Delta^{op}_a \to C$ with $A^+_0 \to A^+_{-1}$ as the morphism $A_0 \to B$, such that the sub-[[diagram]]

  $$
    \array{
      A^+_1 &\to& A^+_0
      \\
      \downarrow && \downarrow
      \\
      A^+_0 &\to& A^+_{-1}
    }
  $$
  
  of $A^+$ is a [[(∞,1)-pullback]] diagram in $C$.

=--

This is [[Higher Topos Theory|HTT, below prop. 6.1.2.11]].

If $A$ is the [[Cech nerve]] of a morphism $A_0 \to A_{-1}$  
then the groupoid object is [[delooping|deloopable]] in the groupoid sense.

+-- {: .num_defn #EffectiveGroupoid}
###### Definition 

A groupoid object $A : \Delta^{op} \to C$ is an **effective [[quotient object]]** if the [[(∞,1)-colimit]] diagram $A^+ : \Delta_a^{op} \to C$ exists, such that $A$ is the [[Cech nerve]] of $A^+_0 \to A^+_{-1}$, i.e. of $A_0 \to \lim_\to A_\bullet$.

=--

### Group object

A **group object** is a groupoid object $U : \Delta^{op} \to C$ for which $U_0 \simeq *$ is a [[terminal object in a quasi-category|terminal object]].

([[Higher Topos Theory|HTT, def. 7.2.2.1]]).

It follows ([[Higher Topos Theory|HTT, prop. 7.2.2.4]]) that a group object is of the form

$$
  U = \left(
      \cdots G \times G \stackrel{\to}{\stackrel{\to}{\to}} G \stackrel{\to}{\to} *
  \right)
  \,.
$$

### Relation to $(\infty,1)$-quotients {#RelationToQuotients}

+-- {: .num_remark}
###### Remark

A groupoid object in an $(\infty,1)$-category 

$$
\left(  \cdots  A_2  \stackrel{\to}{\stackrel{\to}{\to}}
   A_1 \stackrel{\to}{\to} A_0
  \right)
$$

is the [[(∞,1)-category]] analog of an internal [[equivalence relation]] on $A_0$, which is just a pair of morphisms

$$
   R \stackrel{\to}{\to} A_0
   \,.
$$

The [[colimit]] ([[coequalizer]]) of the latter diagram is the [[quotient]] of $A_0$ by the relation $R$.

Analogously, the [[(∞,1)-colimit]] 

$$
  \lim_\to (\Delta^{op} \stackrel{A}{\to} C)
$$

over the simplicial diagram $A : \Delta^{op} \to C$ is the corresponding **$(\infty,1)$-quotient**.

If we are given a [[model category]] [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-category]] $C$, then this [[(∞,1)-colimit]] is presented by a [[homotopy colimit]] over the corresponding simplicial diagraM a **homotopy quotient** .

=--


## Properties

### Equivalent characterizations
 {#EquivalentCharacterizations}

We state in prop. \ref{EquivalentCharacterizationsViaSlicesAndPowering} below a list of equivalent conditions that characterize a [[simplicial object in an (∞,1)-category]] as a groupoid object. This uses the following basic notions, which we review here for convenience.

+-- {: .num_defn}
###### Definition

For $K \in $ [[sSet]] a [[simplicial set]], write $\Delta_{/K}$ for its [[category of simplices]]. For $X_\bullet \in \mathcal{C}^{\Delta^{op}}$ a simplicial object, write

$$
  X[K] \colon \Delta^{op}_{/K} \to \Delta^{op} \stackrel{X}{\to} \mathcal{C}
$$

for the precomposition of $X_\bullet$ with the canonical projection. Moreover, write 

$$
  X(K) \coloneqq \underset{\leftarrow}{\lim} X[K]
$$

for the [[(∞,1)-limit]] over this composite [[(∞,1)-functor]] in $\mathcal{C}$ (if it exists). (Notice: square brackets for the composite functor, round brackets for its $(\infty,1)$-limit.)

=--

+-- {: .num_remark #EquivalenceOfConeCategoriesAndLimits}
###### Remark

For $X_\bullet \in \mathcal{C}^{\Delta^{op}}$ and $K \to K'$ the following are equivalent

1. the induced morphism of cone $(\infty,1)$-categories $\mathcal{C}_{X[K]} \to \mathcal{C}_{X[K']}$ is an [[equivalence of (∞,1)-categories]];

1. the induced morphism of [[(∞,1)-limits]] $X(K) \to X(K')$ is an [[equivalence in an (∞,1)-category|equivalence]].

=--

(The first perspective is used in ([Lurie](#Lurie)), the second in ([Lurie2](#Lurie2)).)

+-- {: .proof}
###### Proof

In one direction: the limit is the [[terminal object in an (∞,1)-category|terminal object]] in the cone category, and so is preserved by equivalences of cone categories. (This direction appears as ([Lurie, prop. 4.1.1.8](#Lurie))).  Conversely, the limits is the object representing cones, and hence an equivalence of limits induces an equivalence of cone categories.

=--

+-- {: .num_prop #EquivalentCharacterizationsViaSlicesAndPowering}
###### Proposition

Let $\mathcal{C}$ be an $(\infty,1)$-category incarnated explicitly as a [[quasi-category]]. Then a [[simplicial object in an (∞,1)-category|simplicial object in]] $\mathcal{C}$ is a groupoid object if the following equivalent conditions hold.

1. If $K \to K'$ is a morphism in [[sSet]] which is a [[weak homotopy equivalence]] and a [[bijection]] on [[vertices]], then the induced morphism on [[slice-(∞,1)-categories]]

   $$
     \mathcal{C}_{/X[K]}
     \to 
     \mathcal{C}_{/X[K']}
   $$

   is an [[equivalence of (∞,1)-categories]] (a [[weak equivalence]] in the [[model structure for quasi-categories]]).

1. For every $n \geq 2$ and every $0 \leq i \leq n$, the morphism $\mathcal{C}_{/X[\Delta^n]} \to \mathcal{C}_{/X[\Lambda^n_i]}$ is an weak equivalence in the [[model structure for quasi-categories]]

1. (...)

Using remark \ref{EquivalenceOfConeCategoriesAndLimits} this means equivalently that the simplicial object $X_\bullet$ is a groupoid precisely if the following 

1. $X_\bullet$ satisfies the ordinary [[Segal conditions]] and the morphism $X(\Delta^2) \to X(\Lambda^2_0)$ is an [[equivalence in an (∞,1)-category|equivalence]].

1. (...)

=--

The first items appear as ([Lurie, prop. 6.1.2.6](#Lurie)). The second ones appear in the proofs of ([Lurie2, prop. 1.1.8, lemma 1.2.25](#Lurie2)).



### The $(\infty,1)$-category of groupoid objects

+-- {: .num_prop}
###### Proposition

The $(\infty,1)$-category of groupoid objects in $C$ is a [[reflective sub-(∞,1)-category]]

$$
  Grpd(C)
  \stackrel{\overset{}{\leftarrow}}{\hookrightarrow}
  Func(\Delta^{op}, C)
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, prop. 6.1.2.9]]. In nice cases the image of this reflective subcategory are the effective epimorphisms:

+-- {: .num_prop}
###### Proposition

If $C = \mathbf{H}$ in an [[(∞,1)-semitopos]] there is a natural [[equivalence of (∞,1)-categories]]

$$
  Grpd(\mathbf{H})
  \simeq
  (\mathbf{H}^I)_{eff}
$$

between the $(\infty,1)$-category of groupoid objects in $\mathbf{H}$ and the full [[sub-(∞,1)-category]] of the [[arrow category]] of $\mathbf{H}$ (the [[(∞,1)-functor (∞,1)-category]] $Func(\Delta[1], \mathbf{H})$) on the [[effective epimorphism in an (∞,1)-category|effective epimorphisms]].

=--

This appears below [[Higher Topos Theory|HTT, cor. 6.2.3.5]].

### Cech nerves

Write $\Delta_a$ for the augmented [[simplex category]] (including the object $[-1]$).

+-- {: .num_prop}
###### Proposition

An augmented simplicial object $A^+ : \Delta_a^{op} \to C$ is the right [[Kan extension]] of its restriction to $[-1]$ and $[0]$

$$
  \array{
    \{[-1] \leftarrow [0]\} &\stackrel{A^+|_{\leq 0}}{\to}& C
    \\
    \downarrow & \nearrow_{\mathrlap{A^+}}
    \\
    \Delta_a^{op}
  }
$$

precisley if $A^+|_{\geq 0}$ is a groupoid object in $C$ and the [[diagram]]

$$
  \array{
    A_1 &\to& A_0
    \\
    \downarrow && \downarrow
    \\
    A_0 &\to& A_{-1}
  }
$$

is a [[(∞,1)-pullback]] in $C$.


=--

$A$ is called the **[[Cech nerve]]** of $A_0 \to A_{-1}$ if the equivalent conditions of this proposition are satisfied.


### Effective quotients 
  {#Effective}
 

+-- {: .num_prop}
###### Proposition

In $C = $ [[∞Grpd]] every groupoid object is an effective quotient, def. \ref{EffectiveGroupoid}. 

=--

This is [[Higher Topos Theory|HTT, below remark 6.1.2.15]] and [[Higher Topos Theory|HTT, cor. 6.1.3.20]].

More generally, this is true for every [[(∞,1)-topos]].

+-- {: .num_prop}
###### Proposition

In $C$ is an [[(∞,1)-topos]], then every groupoid object in $C$ is an effective quotient, def. \ref{EffectiveGroupoid}. 

=--

This is [[Higher Topos Theory|HTT, theorem 6.1.0.6 (4) iv)]].


### Delooping
  {#Delooping}  

For $\mathcal{X}$ an [[(∞,1)-category]] with [[(∞,1)-pullback]]s and for
$x : * \to X$ a [[pointed object|pointed]] object in $\mathcal{X}$, its [[loop space object]] at $x$ is the [[(∞,1)-pullback]]

$$
  \Omega_x X := {*} \prod_{X} {*}
$$

hence the object universally filling the diagram

$$
  \array{
    \Omega_x X &\to& *
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{x}}
    \\
    * &\stackrel{x}{\to}& X
  }
  \,.
$$

Since this is the beginning of the [[Cech nerve]] of $* \to X$, $\Omega_x X$ is naturally equipped with the structure of an $\infty$-group object in $\mathcal{X}$.

+-- {: .num_prop}
###### Proposition

Let $\mathcal{X}$ be an [[(∞,1)-topos]]. Then the operation of forming [[loop space]] objects constitutes an [[equivalence of (∞,1)-categories]]

$$
  \Omega : PointedConnected(\mathcal{X}) \stackrel{\simeq}{\to}
   Grp(\mathcal{X})
$$

from the full [[sub-(∞,1)-category]] of the [[over-(∞,1)-category|under-(∞,1)-category]] $*/\mathcal{X}$ of [[pointed object]]s on those that are also [[0-connected]] (hence those that have an essentially unique point) with the $(\infty,1)$-category of group objects in $\mathcal{X}$.

=--

This is [[Higher Topos Theory|HTT, lemma 7.2.2.11 (1)]]

The inverse to $\Omega$ we write 

$$
  \mathbf{B} : Grp(\mathcal{X}) \to PointedConnected(\mathcal{X})
  \,.
$$

For $G \in Grp(\mathcal{X})$ we call $\mathbf{B}G$ its [[delooping]].



## Examples

### Group objects in an $(\infty,1)$-topos

When the ambient [[(∞,1)-category]] is an [[(∞,1)-topos]] then -- by the $\infty$-Giraud axioms -- all groupoid objects are [[quotient object|effective]], meaning that for

$$
  \mathbf{B}G = \lim_{\to} U_\bullet
$$

the [[(∞,1)-colimit]] over the group object $U_\bullet$ we have that $U_\bullet$ is reproduced as the Cech nerve of $* \to \mathbf{B}G$

$$
  \left(
      \cdots G \times G \stackrel{\to}{\stackrel{\to}{\to}} G \stackrel{\to}{\to} *
  \right)
  \simeq
  \left(
      \cdots 
   {*}\times_{\mathbf{B}G}{*}\times_{\mathbf{B}G}{*} \stackrel{\to}{\stackrel{\to}{\to}} {*}\times_{\mathbf{B}G}{*} \stackrel{\to}{\to} *
  \right) 
  \,.
$$

The object $\mathbf{B}G$ is the [[delooping]] object of the group object $G$.

For more on this see also [[principal ∞-bundle]].

### Models for group objects in $\infty Grpd$ {#ModelsInInfGrpd}

There is a [[model category]] structure that presents the [[(∞,1)-category]] of group objects in [[∞Grpd]]: the [[∞-group]]s.

* The group objects $G$ themselves are modeled by a model structure on the category $sGrp$ of [[simplicial group]]s.

* Their delooping spaces $\mathbf{B}G$ are modeled by a model structure on the category $sSet_0$ of [[simplicial set]]s with a single vertex.

The operation of forming [[loop space object]]s constitutes a [[Quillen equivalence]] between these two model structures

$$
  \Omega : sSet_0 \stackrel{\simeq_{Quillen}}{\to} sGrp
  \,.
$$



The Quillen equivalence itself is in section 6 there.

+-- {: .num_prop }
###### Proposition

There exists the [[transferred model structure]] on the category $sGrp$ of [[simplicial group]]s along the [[forgetful functor]]

$$
  U : sGrp \to sSet_{Quillen}
$$

to the standard [[model structure on simplicial sets]].

This means that a morphism in $sGrp$ is a 

* weak equivalences 

* or fibration

precisely if it is so in $sSet_{Quillen}$.

=--

This appears as ([GoerssJardine, ch V, theorem. 2.3](GoerssJardine)).


+-- {: .num_prop }
###### Proposition

There is a [[model structure on reduced simplicial sets]] $sSet_0$ ([[simplicial sets]] with a single vertex) whose

* weak equivalences 

* and cofibrations

are those in the standard [[model structure on simplicial sets]].

=--

This appears as ([GoerssJardine, ch V, prop. 6.2](GoerssJardine)).


+-- {: .num_prop }
###### Proposition

The simplicial loop space functor $G$ and the delooping functor $\bar W(-)$ (discussed at [[simplicial group]]) constitute a [[Quillen equivalence]]

$$
  (G \dashv \bar W) : sGr \stackrel{\overset{G}{\leftarrow}}{\underset{\bar W}{\to}}
  sSet_0
  \,.
$$

The $(G \dashv \bar W)$-[[unit of an adjunction|unit]] and counit are weak equivalences:

$$
  X \stackrel{\simeq}{\to} \bar W G X
$$

$$
  G \bar W G \stackrel{\simeq}{\to} G
  \,.
$$


=--

This appears as ([GoerssJardine, ch. V prop. 6.3](#GoerssJardine)).


## Related concepts

* [[∞-group]]

* [[monoid]]. [[monoid object]], [[monoid object in an (∞,1)-category]]

* [[group]], [[group object]]

* [[ring]], [[ring object]]

* [[looping and delooping]]


## References

Groupoid objects in $(\infty,1)$-categories are the topic of section 6.1.2 in

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_ 


Model category presentations of groupoid objects in $\infty Grpd$ by groupoidal [[complete Segal spaces]] are discussed in 

* [[Julia Bergner]], 

  _Adding inverses to diagrams encoding algebraic structures_, Homology, Homotopy and Applications 10 (2008), no. 2, 149&#8211;174. ([arXiv:0610291](http://arxiv.org/abs/math/0610291))

  _Adding inverses to diagrams II: Invertible homotopy theories are spaces_, Homology, Homotopy and Applications, Vol. 10 (2008), No. 2, pp.175-193. ([web](http://www.intlpress.com/hha/v10/n2/a9/), [arXiv:0710.2254](http://arxiv.org/abs/0710.2254))

A standard textbook reference on $\infty$-groups in the [[classical model structure on simplicial sets]] is 

* {#GoerssJardine} [[Paul Goerss]], [[Rick Jardine]], chapter V of _[[Simplicial homotopy theory]]_ [chapter V](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-5.dvi). 


Discussion from the point of view of [[category objects in an (∞,1)-category]] is in 

* {#Lurie2} [[Jacob Lurie]], _[[(∞,2)-Categories and the Goodwillie Calculus]]_ ([arXiv:0905.0462](http://arxiv.org/abs/0905.0462))
 



[[!redirects groupoid object in an (∞,1)-category]]
[[!redirects groupoid objects in an (∞,1)-category]]
[[!redirects groupoid objects in an (infinity,1)-category]]
[[!redirects group object in an (infinity,1)-category]]
[[!redirects group object in an (∞,1)-category]]
[[!redirects group objects in an (infinity,1)-category]]
[[!redirects group objects in an (∞,1)-category]]
