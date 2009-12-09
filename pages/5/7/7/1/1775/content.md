<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

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

being **effective** means that it is the [[Cech nerve]] 

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


## Details


In section 6.1.2 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

a notion of [[groupoid]] object [[internalization|internal]] to an [[(∞,1)-category]] $\mathbf{C}$ is defined
as [[homotopy]]-[[simplicial object]] in $\mathbf{C}$ given by an [[(∞,1)-functor]]

$$
  C : \Delta^{op} \to \mathbf{C}
$$

satisfying some conditions that make it look like the [[nerve]] of an [[internal category|internal]] [[groupoid]] (proposition 6.2.2.6 in [[Higher Topos Theory|HTT]]).

Such a groupoid object with $C_0 = {*}$ is a group object.


If $C$ is the [[Cech nerve]] of a morphism $C_0 \to C_{-1}$  
then the groupoid object is [[delooping|deloopable]] in the groupoid sense.

If furthermore the morphism $C_0 \to C_{-1}$ is the colimit $C_{-1} = colim_i C_i$ 
over the groupoid object diagram (the $(\infty,1)$-analog of a [[quotient object]]), then the groupoid object is **effective** or: $C_0 \to C_{-1}$ is an **effective quotient**.

In an [[(∞,1)-topos]] every groupoid object has an effective quotient.

[[!redirects groupoid object in an (∞,1)-category]]