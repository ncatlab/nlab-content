<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
</div>

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


## Definition


### Groupoid object

In section 6.1.2 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

a notion of [[groupoid]] object [[internalization|internal]] to an [[(∞,1)-category]] $\mathbf{C}$ is defined
as [[homotopy]]-[[simplicial object]] in $\mathbf{C}$ given by an [[(∞,1)-functor]]

$$
  C : \Delta^{op} \to \mathbf{C}
$$

satisfying some conditions that make it look like the [[nerve]] of an [[internal category|internal]] [[groupoid]] (proposition 6.2.2.6 in [[Higher Topos Theory|HTT]]).

Such a groupoid object with $C_0 = {*}$ is a group object.


If $C$ is the [[?ech nerve]] of a morphism $C_0 \to C_{-1}$  
then the groupoid object is [[delooping|deloopable]] in the groupoid sense.

If furthermore the morphism $C_0 \to C_{-1}$ is the colimit $C_{-1} = colim_i C_i$ 
over the groupoid object diagram (the $(\infty,1)$-analog of a [[quotient object]]), then the groupoid object is **effective** or: $C_0 \to C_{-1}$ is an **effective quotient**.

In an [[(∞,1)-topos]] every groupoid object has an effective quotient.

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

## Examples

### Group objects in an $(\infty,1)$-topos

When the ambient [[(∞,1)-category]] is an [[(∞,1)-topos]] then -- by the $\infty$-Giraud axioms -- all groupoid objects are [[quotient object|effective]], meaning that for

$$
  \mathbf{B}G = \lim_\to U_\bullet
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

### Models for group objects in $\infty Grpd$

There is a [[model category]] structure that presents the [[(∞,1)-category]] of group objects in [[∞Grpd]].

* The group objects $G$ themselves are modeled by a model structure on the category $sGrpd$ of [[simplicial group]]s.

* Their delooping spaces $\mathbf{B}G$ are modeled by a model structure on the category $sSet_0$ of [[simplicial set]]s with a single vertex.

The operation of forming [[loop space object]]s constitutes a [[Quillen equivalence]] between these two model structures

$$
  \Omega : sSet_0 \stackrel{\simeq_{Quillen}}{\to} sGrpd
  \,.
$$

This is for instance in 

* Goerss, Jardine, _Simplicial homotopy theory_ [chapter V](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-5.dvi). 

The Quillen equivalence itself is in section 6 there.


[[!redirects groupoid object in an (∞,1)-category]]