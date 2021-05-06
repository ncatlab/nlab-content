
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+--{: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents#
* table of contents
{: toc}

## Idea

In [[logic]], a **signature** is a collection of data which prescribes the 'alphabet' of non-logical symbols of a logical [[theory]], saying which operations and [[predicates]] are taken to be primitive. 



## Definition

### Types

Formally, a **signature** $\Sigma$ consists of 

* A set $S$ whose elements are called **sorts** or **[[types]]** of $\Sigma$, 

* A set $Rel(\Sigma)$ whose elements are called **relation symbols**, equipped with a function $ar: Rel(\Sigma) \to S^*$ to the [[free monoid]] on $S$ which prescribes an [[arity]] for each relation symbol, 

* A set $Func(\Sigma)$ whose elements are called **function symbols**, equipped with a function 
$$\langle dom, cod \rangle: Func(\Sigma) \to S^* \times S$$ 
which prescribes an arity or type for each function symbol. A function symbol $f$ may be written as $dom(f) \to cod(f)$, or as $d_0(f) \to d_1(f)$, to indicate its arity. 

The majority of (but far from all) mathematical concepts are described by means of a **single-sorted** signature, where $S$ consists of a single element $X$. Examples where multisorted signatures are used is the theory of [[categories]] (with an [[object]] sort and a [[morphism]] sort) and [[quiver|(multi)directed graphs]] (with a vertex sort and an edge sort). But in the single-sorted or one-sorted case, the free monoid on the one-sort set is isomorphic to $\mathbb{N}$, and the arity of a relation is a number $n$. Hence we speak of an $n$-ary relation (unary, binary, etc.). Similarly, the arity of a function symbol or operation $f$ is the number $n$ which indexes $dom(f)$ (hence we speak of unary operations, binary operations, etc.) In either the single-sorted or multisorted case, a 0-ary operation (where the domain empty) is usually called a **constant**. 

A **relational** signature is where $Func(\Sigma)$ is empty, and an **equational** or **algebraic** signature is where $Rel(\Sigma)$ is empty. (In the latter case, the only relation symbol is the equality symbol, but this is typically considered a logical symbol.) Occasionally one allows a relational signature to have constants. 

### Models

A ([[set theory|set-theoretic]]) **model** or **interpretation** $M$ of a signature consists of functions which assign

* To each sort $s$ a [[set]] $M(s)$, 

* To each relation symbol $R$ of arity $\langle s_1, \ldots, s_n \rangle$ a [[subset]] $M(R) \hookrightarrow M(s_1) \times \ldots \times M(s_n)$, 

* To each function symbol $f$ of type $\langle s_1, \ldots, s_n \rangle \to s$ a [[function]] $M(f): M(s_1) \times \ldots \times M(s_n) \to M(s)$. Such a function is called an **operation** (that interprets $f$). In the case of constants of type $s$, the empty product on the left is taken to be a terminal or 1-element set $1$, whose element needs no name but is often given a generic name like '$*$'. 

More generally a signature may be interpreted in other [[category|categories]] $C$ besides [[Set]]; for this it is reasonable to suppose that $C$ is at least a [[regular category]]. See also 

* [[categorical semantics]].


### Theories

In terms of a signature one may formulate [[proposition]]s, [[sequents]] and then [[theories]]. See there for more details.


## Examples 

An important point to bear in mind is that _essentially_ the same theories (where 'same' means that the categories of models are equivalent or even isomorphic) may have very different signatures. For example, 

* The theory of [[group]]s is usually described as a single-sorted theory whose signature has one binary operation (called 'multiplication') $m$, one constant $e$ (called 'identity'), and one unary operation (called 'inversion') $i$. But it can also be described using a signature with just one (binary) operation $m$; there one adds in extra axioms which posit the existence of an identity and of inverse elements. Or, it can be described using a signature with a single (binary) operation $d$ (for 'division'). All these are examples of equational signatures. 

* A [[Boolean ring]] is usually described as a commutative ring with identity in which multiplication is idempotent, hence the theory of Boolean rings is usually presented using the signature normally reserved for rings (with identity). A [[Boolean algebra]] may be described using a variety of signatures, for example non-equationally, involving a binary relation $\leq$ and function symbols $\wedge$, $\neg$, $\top$. 

* The theory ZFC is usually described using a single-sorted relational signature with one binary relation $\in$. However, other approaches are possible: one can also describe ZFC with a relational symbol $\subseteq$ together with a unary function symbol $sing$ (to be interpreted as taking a 'set' $S$, i.e., an element of a ZFC structure, to a singleton 'set' $\{S\}$). 


## Remarks 

The multiplicity of ways in which one can describe essentially the same class of objects is a phenomenon which in higher category theory is often referred to as [[bias]]. Often one desires to use an 'unbiased' approach which includes different signatures under one roof and on the same footing. In the case of algebraic (equational) theories, this can be done using the device of [[clone]]s or [[Lawvere theory|Lawvere theories]], which does not single out certain non-logical operations as 'privileged'. 

There are several reasons though why one might prefer to retain some bias, for example: 

* Tradition, familiarity, thus ease of reference. For example, a group _is_ a set equipped with a binary $m$, an unary $i$, and a constant $e$, rather than a set equipped with a single division operation, or a finite product-preserving functor for that matter. 

* Mathematical intuition. That is, different signatures may invoke different intuitions or attitudes toward a subject; for example, "Boolean rings" may invoke a more algebraic or algebro-geometric attitude (as in [[Stone duality]]) whereas "Boolean algebras" may invoke a more logical attitude (propositional logic). 

* Differences in logical strength. That is, first-order logic should be thought of as coming in layers, ranging from equational logic up to [[pretopos]] logic, and different signatures may need differing levels of logical strength for them to be interpreted as intended. Equational logic may be preferred on occasion because it is a very weak logic, whereas relational signatures often require at least the strength of regular categories for them to be interpreted correctly. 


## The language of a signature

Each signature $\Sigma$ generates a language whose elements are first-order predicates: expressions formed by using an alphabet of logical symbols together with $\Sigma$, considered as an alphabet of non-logical symbols, according to certain rules. For an account of the traditional logical syntax, see [Wikipedia](https://en.wikipedia.org/wiki/First-order_logic#Syntax). 

First-order languages can also be structured categorically through the notion of [[hyperdoctrine]]. The base of the hyperdoctrine is a [[cartesian monoidal category]] $\mathbf{Term}(\Sigma)$ consisting of sorts and terms, or rather, the objects are formal (cartesian) products of sorts, written as finite lists, and the morphisms are tuples of terms generated by the function symbols of the signature. A detailed categorical description of $\mathbf{Term}(\Sigma)$ may be found [here](https://ncatlab.org/nlab/show/free%20cartesian%20category#free_cartesian_category_on_a_signature). 

Given the base $\mathbf{Term}(\Sigma)$, the language itself is structured as a certain Boolean hyperdoctrine, i.e., a functor 

$$Lang(\Sigma): \mathbf{Term}(\Sigma)^{op} \to Bool$$ 

where for each morphism $f$ in the base, the morphism $f^\ast = Lang(\Sigma)(f)$ has a left adjoint $\exists_f$ and a right adjoint $\forall_f$, subject to a Beck-Chevalley condition for each pullback square in the base. To describe it with more traditional logical terminology: the functor takes each object (i.e., product of sorts) $w = s_1 s_2 \ldots s_n$ to the Boolean algebra $Pred(w)$ of predicates of arity $w$ that built up from the formal relations of the signature using first-order logic operations. The sorts $s_i$ appearing in the arity are matched bijectively with the free variables of the predicate, and are the types of those variables. Then, the functor takes each morphism $f: v \to w$, given by an $n$-tuple of terms $\tau_i: v \to s_i$, to the Boolean algebra map $f^\ast: Pred(w) \to Pred(v)$ obtained by substituting, in predicates of arity $w$, the term $\tau_i$ for the free variable $x_i$ that is matched with $s_i$, resulting in a predicate of arity $v$. 

A more precise categorical description of $Lang(\Sigma)$, in terms of a universal property, is as follows. Let $S^\ast$ denote the underlying set of free monoid generated by the set of sorts $S$; regard $S^\ast$ as a discrete category. The formal relations of the signature give a functor 

$$i: S^\ast \to Set$$ 

sending each product $w = s_1 \ldots s_n$ to the set of relations $R \in Rel(\Sigma)$ that have arity $w$. Let $j: S^\ast \to \mathbf{Term}(\Sigma)$ be the obvious inclusion functor (the identity on objects). Define an *interpretation* of $\Sigma$ to be a pair consisting of a Boolean hyperdoctrine $M: \mathbf{Term}(\Sigma)^{op} \to Bool$ together with a natural transformation $\phi: i \to U M j$: 

$$\array{
S^\ast & \stackrel{i}{\to} & Set \\ 
\mathllap{j} \downarrow & \Downarrow \mathrlap{\phi} & \uparrow \mathrlap{U} \\ 
\mathbf{Term}(\Sigma)^{op} & \underset{M}{\to} & Bool
}$$ 

where $U: Bool \to Set$ is the underlying set functor. There is an obvious notion of morphism between interpretations $(M, \phi) \to (M', \phi')$, given by a natural transformation $M \Rightarrow M'$ compatible with the data $\phi, \phi'$. 

+-- {: .num_defn} 
###### Definition 
The *language* $Lang(\Sigma)$ is the initial object in the category of interpretations of $\Sigma$. 
=-- 


## References

* Categorical Logic and Type Theory, Bart Jacobs


[[!redirects signatures in logic]]
[[!redirects signature in logic]]

[[!redirects relation symbol]]
[[!redirects function symbol]]
[[!redirects relation symbols]]
[[!redirects function symbols]]
