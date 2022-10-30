
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### $(\infty,1)$-topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

A [[group object]] in an ordinary [[category]] $C$ with [[pullback]]s is an [[internalization|internal]] [[group]]. More generally, there is the notion of an [[internal groupoid]] in a category $C$.

By the logic of [[vertical categorification]], an **internal $\infty$-group** or **[[internal ∞-groupoid]]** may be defined as a group(oid) object internal to an [[(∞,1)-category]] $C$ with pullbacks. As described there, in full generality this involves not only a weakening of the usual associativity and unit laws up to [[homotopy]], but requires specification of coherence laws of these homotopies up to higher homotopy, and so on.


A _group object_ in an [[(∞,1)-category]] generalizes and unifies two familiar concepts:

* it is the generalization of [[Jim Stasheff|Stasheff]] $A_\infty$-[[A-infinity-space|space]] from [[Top]] to more general [[∞-stack]] [[(∞,1)-topoi]]: an object that comes equipped with an associative and invertible [[monoid]] structure, up to coherent [[homotopy]];

* it generalizes the notion of [[equivalence relation]] from [[category|categories]] to [[(∞,1)-categories]].

Of particular relevance are such group objects that define [[quotient object|effective quotients]]

* these are [[delooping|deloopable]]

* these generalize the notion of [[regular epimorphism]]

* these serve to characterize [[regular category|regular (∞,1)-categories]] -- such as [[∞-stack]] [[(∞,1)-topoi]] -- as those where every such object is an [[quotient object|effective quotient]].

A _groupoid object_ is then accordingly the many-object version of a group object. 

A groupoid object 

$$
 \cdots C_2 \stackrel{\to}{\stackrel{\to}{\to}} C_1 \stackrel{\to}{\to} C_0
$$

being **effective** means that it is the [[?ech nerve]] 

$$
 \cdots 
  C_0 \times_{C_0//C_1} C_0 \times_{C_0//C_1} C_0 
  \stackrel{\to}{\stackrel{\to}{\to}} 
  C_0 \times_{C_0//C_1} C_0  
 \stackrel{\to}{\to} C_0
$$

of its [[action groupoid]] $C_0//C_1$ (the  [[(∞,1)-colimit]] over its diagram)

$$
 \cdots C_2 \stackrel{\to}{\stackrel{\to}{\to}} C_1 \stackrel{\to}{\to} C_0
  \to
  C_0//C_1 := colim_i C_i
  \,.
$$

Therefore groupoid objects in an $(\infty,1)$-category play a central role in the theory of [[principal ∞-bundles]].

Notice that one of the four characterizing properties of an [[(∞,1)-topos]] is that every groupoid object is effective. 


## Definition (complete Segal-space style)


### Groupoid object

The following definition follows in style the definition of a [[complete Segal space]] object.


+-- {: .un_defn}
###### Definition

For $C$ an [[(∞,1)-category]], a **groupoid object** in $C$ is a [[simplicial object|simplicial]] [[diagram]]

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

is a [[(∞,1)-pullback]] diagram in $C$. 

The $(\infty,1)$-category of groupoid objects in $C$ is the full [[sub-(∞,1)-category]] 

$$
  Grpd(C) \hookrightarrow Func(\Delta^{op}, C)
$$

of the [[(∞,1)-category of (∞,1)-functors]] on those objects that are groupoid objects.

=--

This is [[Higher Topos Theory|HTT, prop. 6.1.2.6, item 4'']] with [[Higher Topos Theory|HTT, def. 6.1.2.7]].


+-- {: .un_def}
###### Definition 

A groupoid object $A : \Delta^{op} \to C$ is the **[[Cech nerve]]** of a morphism $A_0 \to B$ if 

* $A$ is the restriction of an augmented simplicial object $A^+ : \Delta^{op}_a \to A$ with $A^*([-1] \to [0]) = A_0 \to B$;

* the sub-[[diagram]]

  $$
    \array{
      A_1 &\to& A_0
      \\
      \downarrow && \downarrow
      \\
      A_0 &\to& A_{-1}
    }
  $$
  
  of $A^+$ is a [[(∞,1)-pullback]] diagram in $C$.

=--

This is [[Higher Topos Theory|HTT, below prop. 6.1.2.11]].

If $A$ is the [[?ech nerve]] of a morphism $A_0 \to A_{-1}$  
then the groupoid object is [[delooping|deloopable]] in the groupoid sense.

+-- {: .un_def}
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

+-- {: .un_remark}
###### Remark

A groupoid object in an $(\infty,1)$-category 

$$
\left(  \cdots  A_2  \stackrel{\to}{\stackrel{\to}{\to}}
   A_1 \stackrel{\to}{\to} A_0
  \right)
$$

is the [[(∞,1)-category]] analog of an internal [[equivalence relation]] on $CA_0$, which is just a pair of morphisms

$$
   R \stackrel{\to}{\to} A_0
   \,.
$$

The [[colimit]] ([[coequalizer]]) of the latter diagram is the [[quotient]] of $C_0$ by the relation $R$.

Accordingly, the [[(∞,1)-colimit]] 

$$
  \lim_\to (\Delta^{op} \stackrel{A}{\to} C)
$$

over the simplicial diagram $A : \Delta^{op} \to C$ is the corresponding **$(\infty,1)$-quotient**.

If we are given a [[model category]] [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-category]] $C$, then this [[(∞,1)-colimit]] is presented by a [[homotopy colimit]] over the corresponding simplicial diagraM a **homotopy quotient** .

=--


## Properties

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

between the $(\infty,1)$-category of groupoid objects in $\mathbf{H}$ and the full [[sub-(∞,1)-category]] of the [[arrow category]] of $\mathbf{H}$ (the [[(∞,1)-functor (∞,1)-category]] $Func(\Delta[1], \mathb{H})$) on the [[effective epimorphism in an (∞,1)-category|effective epimorphisms]].

=--

This appears below [[Higher Topos Theory|HTT, cor. 6.3.2.5]].

### Cech nerves

Write $\Delta_a$ for the augmented [[simplex category]] (including the object $[-1]$).

+-- {: .un_prop}
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


### Effective quotients {#Effective}
 

+-- {: .un_prop}
###### Proposition

In $C = $ [[∞Grpd]] every groupoid object is an effective quotient. 

=--

This is [[Higher Topos Theory|HTT, below remark 6.1.2.15]] and [[Higher Topos Theory|HTT, cor. 6.1.3.20]].

More generally, this is true for every [[(∞,1)-topos]].

+-- {: .un_prop}
###### Proposition

In $C$ is an [[(∞,1)-topos]], then every groupoid object in $C$ is an effective quotient. 

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

+-- {: .un_prop}
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

There exists the [[transferred model structure]] on the category $sGrp$ of [[simplicial group]]s allong the [[forgetful functor]]

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

* [[monoid]]. [[monoid object]], [[monoid object in an (∞,1)-category]]

* [[group]], [[group object]]

* [[ring]], [[ring object]]

* [[looping and delooping]]

## References

Groupoid objects in $(\infty,1)$-categories are the topic of section 6.1.2 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 
{#Lurie}

A standard textbook reference on the model categories presentation of $\infty$-groups in $sSet$ is chapter V of

* [[Paul Goerss]], [[Rick Jardine]], _Simplicial homotopy theory_ [chapter V](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-5.dvi). 
{#GoerssJardine}



[[!redirects groupoid object in an (∞,1)-category]]
[[!redirects groupoid objects in an (∞,1)-category]]
[[!redirects groupoid objects in an (infinity,1)-category]]
[[!redirects group object in an (infinity,1)-category]]
[[!redirects group object in an (∞,1)-category]]
[[!redirects group objects in an (infinity,1)-category]]
[[!redirects group objects in an (∞,1)-category]]
