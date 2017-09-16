The Chu construction is a method for constructing a [[star-autonomous category]] from a [[closed monoidal category|closed symmetric monoidal category]]. It is named after Po-Hsiang Chu, a student of Michael Barr, who gave the construction in his master's thesis at McGill University. 

In outline, given a closed symmetric monoidal category $C$ with [[pullback]]s and an object $d$ of $C$, there is a star-autonomous category $Chu(C, d)$ and a strong symmetric monoidal functor 

$$i: C \to Chu(C, d)$$

which realizes $C$ as a [[coreflective subcategory]] of $Chu(C, d)$. Being star-autonomous, $Chu(C, d)$ is self-dual, hence $C^{op}$ also embeds as a full subcategory of $Chu(C, d)$, this time [[reflective subcategory|reflectively]]. 

Many concrete dualities in mathematics can be seen as embedded in a larger ambient self-duality on a Chu construction. This applies in particular to the category of _Chu spaces_, $Chu(Set, 2)$ (see below). 


## Definition ## 

The objects of $Chu(C, d)$ are triples $(a, b; r: a \otimes b \to d)$ (called _$d$-valued pairings_ between $a$ and $b$), where $a$ and $b$ are objects of $C$ and $r$ is a morphism of $C$. The special triple $(d, I; \rho: d \otimes I \cong d)$, where $rho$ is an instance of the canonical isomorphism (the right unitor) for the monoidal unit $I$, will play the role of dualizing object in $Chu(C, d)$. 

The morphisms of $Chu(C, d)$, 

$$(a, b; r: a \otimes b \to d) \to (x, y; s: x \otimes y \to d),$$

are pairs of morphisms $f: a \to x$, $g: y \to b$ which are adjoint with respect to the pairings, that is, making the diagram 

$$\array{
 & a \otimes y & \overset{1_a \otimes g}{\to} & a \otimes b\\
f \otimes 1_x & \downarrow & & \downarrow r\\
& x \otimes y & \overset{s}{\to} & d
}$$

commute. There is an evident self-duality 

$$Chu(C, d)^{op} \to Chu(C, d)$$ 

which takes an object $(a, b; r: a \otimes b \to d)$ to 

$$(b, a; r^\dagger = [b \otimes a \overset{s}{\cong} a \otimes b \overset{r}{\to} d])$$ 

where $\sigma$ is an instance of the symmetry isomorphism, so that $r^\dagger$ is the evident transpose. On morphisms, it takes a pair $(f, g)$ to $(g, f)$; note well that the directions of the arrows make the functor contravariant on $Chu(C, d)$. 

Armed with just this much knowledge, and knowledge of how star-autonomous categories behave (as categorified versions of [[Boolean algebra]]s, or perhaps better [[Boolean rig]]s), the star-autonomous structure on $Chu(C, D)$ can pretty much be deduced (or strongly guessed) by the diligent reader, and this is actually a very good exercise. One could sketch this as follows: 

* The monoidal unit of $Chu(C, d)$ should be the dual of the dualizer, and so is $(I, d; \lambda: I \otimes d \cong d)$ where $\lambda$, the transpose of $\rho$, is a canonical isomorphism for the unit $I$. 

* The internal hom $A \multimap X$ in $Chu(C, d)$ should internalize the external hom, i.e., the set of maps from the monoidal unit to $A \multimap X$ should be in natural bijection with the set of maps $A \to X$ in $Chu(C, d)$. 

This suggests the first component $(A \multimap X)_0$ of the triple 

$$A \multimap X = ((A \multimap X)_0, (A \multimap X)_1; pairing)$$ 

should be the object of adjoint pairs of maps: given 

$$A = (a, b; r: a \otimes b \to d), \qquad X = (x, y; s: x \otimes y \to d)$$ 

define the first component as pullback: 

$$\array{
(A \multimap X)_0 & \to & x^a \\
\downarrow & & \downarrow \tilde{s} \\
b^y & \overset{\tilde{r}}{\to} & d^{a \otimes y}
}$$

where exponentials are used to denote internal homs in $C$, $\tilde{r}$ is the result of currying $r$ to $b \to d^a$ and exponentiating, and similarly for $\tilde{s}$. 

The pullback is paired with $a \otimes y$, i.e., there is a map 

$$(A \multimap X)_0 \otimes (a \otimes y) \to d$$ 

obtained by decurrying either leg of the pullback, so one defines (with fingers crossed) $(A \multimap X)_1$ to be $a \otimes y$, and the pairing to be this map into $d$. 

* To form the tensor product $A \otimes X$, use the formula $ A \otimes X \cong (A \multimap X^*)^* $ which holds true in any star-autonomous category (as a categorified analogue of the Boolean algebra equation $a \wedge x = \neg (a \Rightarrow \neg x)$). 

With notation as above, this works out to 

$$(a \otimes x, y^a \times_{d^{a \otimes x}} b^x)$$ 

where the second component is a pullback, and the pairing omitted but obvious. The main thing to check is the presence of a canonical isomorphism 

$$Chu(C, d)(A \otimes X, Y) \cong Chu(C, d)(X, A \multimap)$$ 

but this is left as an exercise. 

Also one should check that if $D$ is the dualizing object, that $ A^* \cong A \multimap D $, but this is straightforward. 

* There is a strong symmetric monoidal functor 
$$i: C \to Chu(C, d)$$ 
taking $c$ to $(c, d^c; eval: c \otimes d^c \to d)$. (This does **not** take $d$ to the dualizing object in $Chu(C, d)$, unless of course the canonical map $I \to d^d$ is an isomorphism.) This embedding admits a right adjoint 
$$p: Chu(C, d) \to C$$ 
given by the obvious projection, that is also strong symmetric monoidal. The unit of the adjunction is an isomorphism, hence $C$ is a coreflective (full) subcategory of $Chu(C, d)$. 

* If $C$ is complete and cocomplete, then so is $Chu(C, d)$. The formula for colimits is the obvious expected one: 
$$colim_i (a_i, b_i; r_i: a_i \otimes b_i \to d) = (colim_i a_i, lim_i b_i; r)$$ 
where $r$ is the decurrying of 
$$lim_i (b_i \to d^{a_i}) \cong lim_i b_i \to d^{colim_i a_i}$$ 
and the formula for limits is obtained by dualizing the formula for colimits in $Chu(C, d)$.  


## Chu spaces ## 

While the Chu construction is worthy of exploration for many types symmetric monoidal categories $C$, a great deal of attention has been focused just on the particular case $Chu(Set, 2)$ (or $Chu(Set,TV)$, where $TV$ is the set of [[truth value]]s, to be [[constructive mathematics|constructive]]), called the category of **Chu spaces**, and relatives like $Chu(E, \Omega)$ where $E$ is a [[topos]] and $\Omega$ its [[subobject classifier]]. The reason is that a great many concrete categories of interest are fully embedded in Chu spaces. Moreover, the 2-element set $TV$ carries a panoply of [[ambimorphic object|ambimorphic]] (formerly, schizophrenic) object structures which induce concrete dualities between these categories, and nearly all of these dualities are embedded in (i.e., are restrictions of) the one overarching duality that obtains on Chu spaces. 

The way this works is invariably the same: if $U: C \to Set$ is a [[concrete category]] and $\mathbf{2}$ is an object of $C$ over the 2-element set $TV$, then there is a functor 

$$C \to Chu(Set, 2): c \mapsto (U c, hom(c, \mathbf{2}); U c \times hom(c, \mathbf{2}) \to U\mathbf{2} = 2)$$ 

which is faithful by the notion of concrete category. What is striking is that this functor is also *full* in many cases of interest. Some examples follow: 

* As explained above, $Set$ fully embeds in $Chu(Set, 2)$ by $X \mapsto (X, 2^X; eval: X \times 2^X \to 2)$. 

* For $C = Top$, taking $\mathbf{2}$ to be [[Sierpinski space]], we have for each [[topological space]] $c$ an identification $Open(c) = hom(c, \mathbf{2})$. The adjointness condition on a morphism $(f, g)$ between the corresponding Chu space expresses precisely the continuity condition that $g = f^*$, the [[preimage]], taking opens to opens. Thus the functor $Top \to Chu(Set, 2)$ is full. 

More examples to be added later...

+--{.query}
Hi Toby; could I get you to explain the aside about Boolean rigs above? I'm thinking Boolean algebras is appropriate, as we have $ I \to x^* \wp x $, $ x \otimes x^* \to D $ [where $\wp$ denotes Girard's "par" and $D$ denotes the dualizer], together with appropriate triangular equations, categorifying the inequalities $1 \leq (\neg x) \vee v$ and $x \wedge (\neg x) \leq 0$ in a Boolean algebra. --*Todd*

Now that I go to write [[Boolean rig]], I\'m not so sure.  I just know that $Chu(P X,\empty)$ at [[measurable space]] is *not* (even classically) a Boolean algebra.  I\'ll get back to you in a day or less.  ---Toby
=--
