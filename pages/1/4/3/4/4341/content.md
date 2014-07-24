
# Walking structures
* tables of contents
{: toc}

## Idea 

Around the nLab and elsewhere, one occasionally sees an expression "the walking _____" where the blank is some mathematical concept. This is a colloquial way of referring to an archetypal model of the concept or type, and usually refers to a free or initial context in which such a type can be interpreted. The term is believed to have been introduced by [[James Dolan]] (see the reference below). 

## Definition

The idea is probably easier to apprehend through examples rather than through a formal definition, but for the record: 

If X is a type of structure that can be defined in a [[category]], [[higher category]], or category with some sort of [[stuff, structure, property|structure]], then the **walking X** is an informal term for the *free category (resp. higher category, category with suitable structure) containing an X*.

More precisely, if $StructCat$ denotes some (higher) category of categories with an appropriate type of structure, then the **walking X** is an object $[X] \in StructCat$ together with a [[natural transformation|natural]] [[equivalence]]
$$ StructCat([X],C) \simeq \{Xs \; in \; C\}$$
between the hom-set/category/space from $[X]$ to $C$, for any $C\in StructCat$, and the set/category/space of all Xs in $C$. 

+-- {: .num_remark} 
###### Remark 
In other words, the structured category $[X]$ equipped with its canonical type $X$ is initial among such structured categories that come equipped with such types $X$. A fancier expression is that $[X]$ 'coclassifies' such types: this is analogous to how a [[classifying space]] $B G$ for a [[topological group]] $G$ classifies $G$-[[bundles]], in that every $G$-bundle $p: E \to X$ over a suitable space $X$ has a classifying map $\chi_p: X \to B G$ (unique up to homotopy) such that pulling back the canonical $G$-bundle type $\pi: E G \to B G$ along $\chi_p$ reproduces the type $p$. Only here we say 'coclassifies' (as for example in this [comment](http://nforum.mathforge.org/discussion/1529/walking-structures/#Item_5)), since here we instead "push forward" the canonical type $X$ of $[X]$ along a structured-category morphism $[X] \to C$ to obtain a given type of $C$. 
=-- 

Pronunciation is just as in 'John is a walking almanac' or 'Eugene Levy is a walking pair of eyebrows'.


## Examples

* The [[interval category]] is the *walking arrow*.

* The augmented/algebraist's [[simplex category]] is "the *walking [[monoid]]*" (in a [[monoidal category]]). That is to say: the simplex category is initial (in a 2-categorical sense) among monoidal categories equipped with a monoid object. Intuitively, it is [[the]] monoidal category that results if all one need be told about it is that it has a monoid object -- all the morphisms of the category are obtainable from the monoid structure by applying the operations of a monoidal category, and they are subject to no further relations beyond those implied by the monoid axioms. 

* Similarly, the [[Lawvere theory]] of groups can be described as "the *walking [[group object|group]]*" (qua [[cartesian monoidal categories]]). This gives a good intuitive description: this Lawvere theory can be understood as the category (with finite products) that results if all one need be told about it is that it has a [[group object]]; the rest of the structure of this category can be deduced from this one fact. 

The last two examples indicate the need for a little care: the [[doctrine]] or type of structured category in which the '$X$' of "the walking $X$" lives should either be specified or clear from context. For example, if one simply says "the 
walking monoid", this means the simplex category if the surrounding context is the doctrine of monoidal categories -- but means something else (the Lawvere theory of monoids) if the ambient context is the doctrine of categories with finite products, and it means the category opposite to that of finitely presentable monoids if we are in the doctrine of [[finitely complete categories]]. 

If the doctrine is not specified, then a reasonable default is a 'minimal' doctrine in which the concept makes sense; for example, to make sense of monoids, one doesn't need more than monoidal categories. See also [[microcosm principle]]. 

Thus, more generally, 

* The [[syntactic category]] of a [[theory]] $T$ in some [[doctrine]] $D$ is the "walking $T$-model" (in a $D$-category).  In particular, the [[classifying topos]] of a [[geometric theory]] $T$ is "the *walking $T$-model*" *qua* [[Grothendieck toposes]] (where the morphisms are the left-adjoint parts of [[geometric morphisms]]).


## References

* A [Caf&#233; post](http://golem.ph.utexas.edu/category/2010/01/f_and_the_shibboleth.html) essentially about walking objects (among other things), including a [comment](http://golem.ph.utexas.edu/category/2010/01/f_and_the_shibboleth.html#c031066) that explains the terminology.


[[!redirects walking]]
[[!redirects walking structure]]
[[!redirects walking structures]]
[[!redirects walking object]]
[[!redirects walking objects]]
