
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contents
* table of contents 
{:toc}

## Idea 

Consider a [[category]] $C$ whose [[objects]] are thought of as _[[spaces]]_ of sorts ("test spaces"), and whose [[morphisms]] are regarded as [[homomorphisms]] between these spaces. 

There is then a general notion of

* **spaces** modeled on $C$ that are _testable_ or _probe-able_ by objects of $C$;

* **quantities** with values in $C$.

Very generally, following [Lawvere 86](#Lawvere86):

* a generalized [[space]] modeled on the objects of $C$ is a [[presheaf]] on $C$, i.e. a [[functor]] of the form

  $X \;\colon\; C^{op} \to $ [[Set]]:

  we think of each such presheaf as being a rule that assigns to each test space $U \in C$ the set $X(U)$ of allowed maps from $U$ _into_ the would-be space $X$ (this is really the perspective of [[functorial geometry]], originally due to [Grothendieck 65](functorial+geometry#Grothendieck65)); 

* a generalized [[quantity]] modeled on $C$ is a [[copresheaf]] on $C$, i.e. a [[functor]] of the form 

  $A \;\colon\; C \to Set$:

  we think of each such copresheaf $A$ as a rule that assigns to each test space $U \in C$ the set $A(U)$ of allowed maps _from_ the would-be space $A$ into $U$, hence as the collection of $U$-valued _functions_ on $A$. Since a function on a point is a "quantity", these are generalized quantities.

One may view the _[[Yoneda lemma]]_ and the resulting _[[Yoneda embedding]]_ as expressing consistency conditions on this perspective: The [[Yoneda lemma]] says that the prescribed rule for how to test a generalized space $X$ by a test space $U$ turns out to coincide with the actual maps from $U$ to $X$, when $U$ is itself regarded as a generalized space, and the [[Yoneda embedding]] says that, as a result, the nature of maps between test spaces does not depend on whether we regard these as test spaces or as generalized spaces.

Beyond this _automatic_ consistency condition, guaranteed by [[category theory]] itself, typically the admissible (co)presheaves that are regarded as generalized spaces and quantities are required to respect one more consistency condition:

* If $C$ carries the structure of a [[site]], one asks a generalized space to be a presheaf $X = PSh(C) = [C^{op},Set]$ that respects the way objects in $C$ are [[covering|covered]] by other objects. These are the _[[sheaves]]_. The [[category of sheaves]]

  $Sh(C) \hookrightarrow PSh(C)$

  is the [[topos]] of spaces modeled on objects in $C$. More details on how to think of sheaves as generalized spaces is at [[motivation for sheaves, cohomology and higher stacks]].


* Given any generalized spaces, functions out of it are expected to respect [[product]]s of coefficient objects, in that a function with values in $U \times V$ is the same as a pair of functions, one with values in $U$, one with values in $V$. Hence one is typically interested in copresheaves that preserve at least [[product]]

  $CoSh(C) \hookrightarrow CoPSh(C)$.


### Details

As indicated in [Lawvere 86, from p. 17 on](#Lawvere86)

* (generalized) spaces;

* (generalized) quantities (e.g. [[algebras of functions]]);

* the [[duality]] between the two;

which underlies much of mathematics is at its heart controlled by the following elementary [[category theory|category theoretic]] reasoning:

Let $S$ be some category whose objects we want to think of as certain simple spaces on which we want to model more general kinds of spaces. For instance $S = \Delta$, the [[simplicial category]], or $S = $ [[CartSp]], the category of $\mathbb{R}^n$ and smooth maps between them. 

An ordinary [[manifold]], for instance, is a space required to be _locally isomorphic_ to an object in $S = CartSp$. But more generally, a space $X$ modeled on $S$ need only be _probeable_ by objects of $S$, giving a rule with which, to each test object $U \in S$, we assign the set of probing maps from $U$ to $X$,  such that this assignment is well-behaved with respect to morphisms in $S$. Such an assignment is nothing but a [[presheaf]] on $S$, i.e. a contravariant functor
$$
  X : S^{op} \to Set
  \,.
$$
Therefore general spaces modeled on $S$ are nothing but presheaves on $S$:
$$
  Spaces_S := PSh(S)
  \,.
$$
Of course this is an extremely general notion of spaces modeled on $S$. 

For example, any smooth manifold $M$ is a presheaf on CartSp by $F_M:= Hom_{Man}(-, M): CartSp^{op} \to Set$, where we consider CartSp as a full subcategory of Man, the category of [[smooth manifold|smooth manifolds]] and smooth maps between them. $F_M$ maps each $\mathbb{R}^n$ to the set of all the smooth ways that $\mathbb{R}^n$ can probe $M$.

In particular, every object in $S$ is a space modeled on $S$, by the [[Yoneda lemma|Yoneda embedding]] $S \hookrightarrow Spaces_S$, whereby every object $X$ in $S$ is embedded as $Hom_S(-, X)$. That is, any object in $S$ is nothing but a consistent way to be probed by all the objects in $S$. 

Now take a space $X$ modeled on $S$, and consider the set of _quantities_ on $X$ with values in $U \in S$. It should be
$$
  C(X,U) := Hom_{Spaces_S}(X,U)
  \,.
$$
This defines a covariant functor $C(X) := Hom_{Spaces_S}(X,-): S \to Sets$. More generally, we can consider the S-valued quantities on $X$ to be a copresheaf on $S$, namely a covariant functor
$$
  C(X): S \to Sets
  \,.
$$
One can think of $C(X)$ as a generalized quantity which may be _co-probed_ by objects of $S$.

In this vein, one can say, generally, that copresheaves on $S$ are generalized quantities modeled on $S$, and we write
$$
  Quantities_S := CoPSh(S)
  \,.
$$

Given any such generalized quantity $A \in Quantities_S$, we can ask which generalized space it behaves like the algebra of functions on. This generalized space should be called $Spec(A)$ and can be defined as a presheaf by the assignment
$$
  Spec(A) 
  :
  U \mapsto Hom_{Quantities_S}(A, C(U))
  \,.
$$

In  total this yields an adjoint pair of contravariant functors between generalized spaces and generalized quantities:

$$
  Spaces_S^{op}
\stackrel{\stackrel{C(-)}{\to}}{\stackrel{Spec(-)}{\leftarrow}}
  Quantities_S
  \,.
$$

(That this is an adjunction can be understood as a special case of [[abstract Stone duality]] induced by a [[dualizing object]].)

Lawvere refers to this [[adjoint pair]] as **[[Isbell conjugation]]**.

In conclusion, the grand [[duality]] between spaces and quantities is a consequence of the [[formal duality]] which reverses the arrows in the category $S$ of test spaces.

This story generalizes straightforwardly from [[presheaf|presheaves]] with values in [[Set]] to presheaves with values in other categories. Of relevance are in particular presheaves with values in the category [[Top]] of [[topological space]]s and presheaves with values in the category of [[spectrum|spectra]]. See the examples below. 


## Isbell duality: global functions and spectrum {#Isbell}

we describe the [[duality]] between space and quantity induced by forming

* functions on spaces;

* spectra of function algebras.

Let $V$ be a [[symmetric monoidal category]] and $C$ a $V$-[[enriched category]]. Write $[C^{op},V]$ for the [[enriched functor category]] and $j : C \to [C^{op},V]$ for the [[Yoneda embedding]].

There is canonically a $V$-[[adjunction]]

$$
  (\mathcal{O} \dashv Spec)  \;\;: \;\; [C, V]^{op}
  \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
  [C^{op},V]
$$

the **[[Isbell adjunction]]**. Here

* $\mathcal{O} := [C^{op},V](j(-), -)$ sends a presheaf $X$ to the copresheaf $U \mapsto [C^{op},V](X,j(U))$;

* $Spec := [C,V]^{op}(j(-),-)$ sends a copresheaf $A$ to the presheaf $U \mapsto [C,V](A, j^{op}(U))$.

If we assume that $C$ is [[copower|tensored]] over $V$, then that this is an adjunction may be seen in [[end]]/[[coend]]-calculus to express the [[hom-object]]s in the [[enriched functor category]] as follows. We compute

$$
  \begin{aligned}
    [C,V]^{op}(\mathcal{O}(X),A)
    & =
    \int_{u \in C} V(A(u), [C^{op},V](X,j(u)))
    \\
    & \simeq
    \int_{u \in C} V(A(u), [C^{op},V](\int^{v \in C} j(v) \cdot X(v),j(u)))   
    \\
    & \simeq
    \int_{u, v \in C} V(A(u) \cdot X(v), [C^{op},V](j(v),j(u)))    
    \\
    & \simeq
    \int_{u, v \in C} V(A(u) \cdot X(v), V(v,u))    
  \end{aligned}
  \,,
$$

where we used the [[Yoneda lemma]] $[C^{op},V](j(v),j(u)) \simeq V(v,u)$ and the [[co-Yoneda lemma]] $X \simeq \int^{v \in V} j(v) \cdot X(v)$ and the fact that the $V$-enriched hom sends colimits and coends in the first argument to limits and ends.

Analogously we find

$$
  \begin{aligned}
    [C^{op},V](X,Spec A)
    & =
    \int_{v \in C} V(X(v),[C,V](A, j^{op}(v)))
    \\
    & \simeq
    \int_{v \in C} V(X(v), [C,V](\int^{u \in C} j^{op}(u) \cdot X(v),j^{op}(u)))   
    \\
    & \simeq
    \int_{u, v \in C} V(A(u) \cdot X(v), [C,V](j^{op}(v),j^{op}(u)))    
    \\
    & \simeq
    \int_{u, v \in C} V(A(u) \cdot X(v), V(v,u))    
  \end{aligned}
  \,,
$$


## Examples

### Cartesian test spaces: diffeological spaces and smooth algebras

Consider the category of test spaces $C = $ [[CartSp]].

Then 

* spaces modeled on $C$ are [[generalized smooth space]]s such as [[diffeological space]]s;

* quantities modeled on $C$ are [[smooth algebra]]s ($C^\infty$-rings).

The adjunction $(\mathcal{O} \dashv Spec)$ sends a smooth space to its smooth algebra of functions and a smooth algebra of functions to its "spectrum".


## Higher space and higher quantity

There are various specializations of interest on this

* [[higher category theory|higher categorical]] version

  * [[∞-space]] modeled on $C$ is a [[simplicial presheaf]] on $C$, i.e. a functor $X : C^{op} \to $ [[SSet]].

  * [[∞-quantity]] modeled on $C$ is a cosimplicial copresheaf on $C$, i.e. a functor $X : C \to CoSSet$ .

With the advent of [[Higher Topos Theory]] abstract concepts of _space and quantity_ have been realized fully in the context of [[(∞,1)-topos]]es in terms of [[structured (∞,1)-topos]]es and [[generalized scheme]]s. For a summary see the tables at [notions of space](http://ncatlab.org/nlab/show/A+Survey+of+Elliptic+Cohomology+-+the+derived+moduli+stack+of+derived+elliptic+curves#NotionsOfSpace).


## Related entries

* [[Isbell duality]]

* [[space]]

* [[generalized smooth space]]

* [[geometry of physics -- categories and toposes]]



## References

The general perspective is due to 

* {#Lawvere86} [[William Lawvere]], _Taking categories seriously_, Revista Colombiana de Matematicas, XX (1986) 147-178, reprinted in: Reprints in Theory and Applications of Categories, No. 8 (2005) pp. 1-24 ([TAC](http://www.tac.mta.ca/tac/reprints/articles/8/tr8abs.html))

* {#Lawvere92} [[William Lawvere]], _Categories of space and quantity_, in: J. Echeverria et al (eds.), _The Space of mathematics_, de Gruyter, Berlin, New York (1992) ([pdf](https://github.com/mattearnshaw/lawvere/blob/master/pdfs/1992-categories-of-space-and-quantity.pdf))

See also

* [[William Lawvere]], _John Isbell's Adequate Subcategories_, TopCom **11** no.1 2006. ([link](http://at.yorku.ca/t/o/p/d/65.htm)) 

[[!redirects quantity]]
[[!redirects quantities]]

[[!redirects space and quantity]]
[[!redirects duality between space and quantity]]

[[!redirects generalized space]]
[[!redirects generalized spaces]]
