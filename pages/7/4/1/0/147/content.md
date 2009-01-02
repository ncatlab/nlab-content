#Idea#

The structure of a **site** on a category $C$ is a structure that regards each object of $C$ as a space and determines which morphisms from collections of objects of $C$ to a given object of $C$ behave as _covers_ of spaces.  This in turn determines when a [[presheaf]] on $C$ is actually a [[sheaf]].

#Definition#

* A **sieve** (or in French, **crible**) on an object $c$ is a subfunctor of the [[representable functor]] $\hom_C(-, c): C^{op} \to Set$. 

Thus, a sieve on $c$, $i: F \hookrightarrow \hom(-, c)$, may be described as a function which assigns to each object $d$ a collection of morphisms $f: d \to c$ into $c$. Naturality of the inclusion $i$ means that whenever $f: d \to c$ belongs to the sieve and $g: e \to d$ is any morphism, then $f g: e \to c$ also belongs to the sieve. 

* A [[Grothendieck topology]] assigns to each object $c$ a collection of sieves on $c$ which are called **covering sieves**, satisfying the following axioms: 
: The maximal sieve $id: \hom(-, c) \hookrightarrow \hom(-, c)$ is always a covering sieve; 
: 

...