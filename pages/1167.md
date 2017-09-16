#Idea#

The _coYoneda lemma_ is a [[natural transformation|natural isomorphism]] whose left hand side is some sort of [[duality|dual]] of the left hand side in the ordinary [[Yoneda lemma]], but whose right hand side is different.

The following states the coYoneda lemma and then proposes an interpretation that is supposed to put it in perspective with the [[Yoneda lemma]].

#Definition#

For $D$ a [[category]], [[Set]] the [[category]] of [[set]]s, $K : D \to Set$ a [[functor]], let $(* \darr K)$ be the [[comma category]] of elements $x \in K d$, let $Q: (* \darr K) \to D$ be the projection $(x \in K d) \mapsto d$ and let for each $a \in D$  the functor $\Delta_a: (* \darr K) \to D$ be the diagonal functor sending everything to the constant value $a$. 

The **coYoneda lemma** is the statement that there is a natural isomorphism of [[functor category|functor categories]]

$$
[D,Set](K, D(a, -)) \cong [(*\darr K), D](\Delta_a, Q).
$$


# Interpretation #

The following is an interpretation of the meaning of the coYoneda lemma in line with the interetation of the ordinary [[Yoneda lemma]] as described at [[heuristic introduction to sheaves, cohomology and higher stacks]].

## ordinary Yoneda recalled (long-winded) ##

Recall from that that for $S$ a [[category]] of test objects (possibly a [[site]], but will be ignored for the following argument), a [[presheaf]] (possibly a [[sheaf]]) $X(-) : S^{op} \to Set$ on $S$ may be interpreted as a rule which assigns to each test space $U$ the collection $X(U)$ of probes of some generalized space $X$ by $U$.

Since every test space $U$ may itself be regarded as a special kind of generalized space in this sense, by the [[Yoneda embedding]] which regards the test space $U$ as the generalized space $Y(U)(-) : V \mapsto S(V,U)$, there ar _a priori_ then two different definitions of what the collection of probes of the generalized space $X$ by the test space $U$ should be:

on the one hand the set $X(U)$ was supposed to be the collection of such probes by definition, but now there is also the set $Hom_{prsheaves}(Y(U), X)$ of maps of $U$ regarded as a generalized space into $X$. If these two sets would not have a natural identification, then the whole interpretation of presheaves as generalized spaces were infected by inconsistencies.

The Yoneda lemma says precisely that this kind of inconsistency is not present, that it is consistent to think of presheaves as probe-assignments to generalized spaces, since there is a natural bijection 
$$
  X(U) \simeq Hom_{presheaves}(Y(U),X)
  \,.
$$


## now same for coYoneda (and also long-winded) ##

Following further the spirit of [[space and quantity]], we may think of a co-presheaf $A(-) : D \to Set$ as a generalized quantity: namely a generalized collection of functions:

for each co-test space $d \in D$, we think of $A(d)$ as the collection of functions (maps) from some hypothetical generalized space _into_ $d$. For every morphism $f: d \to d'$ in $D$ we think of the induced map 
$A(d) \stackrel{A(f)}{\to} A(d')$ as the map which sends each $d$-valued function to the corresponding $d'$-valued function obtained by post-composing it with $f$.

Again via the [[Yoneda embedding]] mechanism, the co-test spaces $d \in D$ themselves form special examples of generalized collections of functions $Y(d) : e \mapsto D(d,e)$: namely the functions on the space $d$.

This suggests that the [[hom-set]] of co-presheaves 

$$
  Hom_{co-presheaves}(A, Y(d))
$$

from a generalized function collection $A(-)$ to an ordinary function collection $Y(d)$ on co-test space $d$ should admit an interpretation as a map which sends each generalized function in $A$ (for all possible co-domains) to a function on $d$ (for all possible co-domains).

The _coYoneda lemma_ may be read as asserting that precisely this is the case. 

To see this, unwrap the nature of the set 
$[(*\downarrow A), D](\Delta_a, Q)$
appearing on the right hand side of the lemma. First notice that the [[comma category]] has as objects 

$$
   (\phi : * \to A(d))  \leftrightarrow (\phi \in A(d))
$$

the generalized functions in the collection $A$ for given codomain $d$, and as morphisms the way these transform as one changes the codomain from $d$ to $d'$ along a map $f$:

$$
  \array{
     && *
     \\
     & {}^\phi\swarrow && \searrow^{f \circ \phi}
     \\
     A(d) && \stackrel{A(f)}{\to} && A(d')
  }
  \,.
$$

This means that an element $k$ in the [[functor category]]

$$
  [(*\downarrow A), D](\Delta_a, Q)
$$

is a natural assignment

$$
  \array{
      (\phi \in A(d)) &\mapsto& (k(\phi) : a \to d)
  }
$$

which sends each $d$-valued generalized function in $A$ to a $d$-valued function on the test space $a$, where naturality means that this assignment respects transformations of codomains.

So the right hand side of the coYoneda lemma, the one which superficially looks a bit opaque, has in fact a manifest interpretation as a map of one collection of generalized functions to another. The statement of the coYoneda lemma therefore is that the [[hom-set]] of co-[[presheaf|presheaves]] between the collection of generalized functions $A$ and the oridnary function on $a$ does reproduce this.

Which is what one would hope, if the interpretation of co-presheaves as generalized [[space and quantity|quantities]] is to be consistent.


#References#

The coYoneda lemma appears as a brief uncommented exercise on p. 63 of 

* MacLane, [[Categories Work|Categories for the Working Mathematician]],

where it is atributed to Kan.

A blog discussion which led to the creation of this entry is [here](http://golem.ph.utexas.edu/category/2009/01/nlab_general_discussion.html#c023106).