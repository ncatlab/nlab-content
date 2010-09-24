
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

A [[group object]] in an ordinary [[category]] $C$ with [[pullback]]s is [[internalization|internal]] [[group]]. More generally, there is the notion of an [[internal groupoid]] in a category $C$.

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

of its [[action groupoid]] $C_0//C_1$ (the ($(\infty,1)$-categorical) [[colimit]] over its diagram)

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

is a [[limit in a quasi-category|pullback diagram]] in $C$. 

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
  
  of $A^+$ is a [[limit in a quasi-category|pullback]] diagram in $C$.

=--

This is [[Higher Topos Theory|HTT, below prop. 6.1.2.11]].

If $A$ is the [[?ech nerve]] of a morphism $A_0 \to A_{-1}$  
then the groupoid object is [[delooping|deloopable]] in the groupoid sense.

+-- {: .un_def}
###### Definition 

A groupoid object $A : \Delta^{op} \to C$ is an **effective [[quotient object]]** if the [[limit in a quasi-category|colimit]] diagram $A^+ : \Delta_a^{op} \to C$ exists, such that $A$ is the [[Cech nerve]] of $A^+_0 \to A^+_{-1}$, i.e. of $A_0 \to \lim_\to A_\bullet$.

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

## Properties

+-- {: .un_prop}
###### Proposition

The $(\infty,1)$-category of groupoid objects in $C$ is a [[reflective sub-(∞,1)-category]]

$$
  Grpd(C)
  \stackrel{\overset{}{\leftarrow}}{\hookrightarrow}
  Func(\Delta^{op}, C)
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, prop. 6.1.2.9]].

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

is a [[limit in a quasi-category|pullback]] in $C$.

=--

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



## Examples

### Group objects in an $(\infty,1)$-topos

When the ambient [[(∞,1)-category]] is an [[(∞,1)-topos]] then -- by the $\infty$-Giraud axioms -- all groupoid objects are [[quotient object|effective]], meaning that for

$$
  \mathbf{B}G = \lim_{\leftarrow} U_\bullet
$$

we have

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

This is for instance in 

* Goerss, Jardine, _Simplicial homotopy theory_ [chapter V](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-5.dvi). 

The Quillen equivalence itself is in section 6 there.


[[!redirects groupoid object in an (∞,1)-category]]
[[!redirects groupoid objects in an (∞,1)-category]]
[[!redirects groupoid objects in an (infinity,1)-category]]
[[!redirects group object in an (infinity,1)-category]]
[[!redirects group object in an (∞,1)-category]]
[[!redirects group objects in an (infinity,1)-category]]
[[!redirects group objects in an (∞,1)-category]]
