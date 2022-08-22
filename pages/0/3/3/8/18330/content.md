
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definitions

\begin{definition}
In set theory, an **identity-on-objects [[functor]]** $F: A\to B$ between [[categories]] $A$ and $B$ is a functor between categories with the same [[set]] of [[objects]], i.e. $Ob = ob(A) = ob(B)$, and has as its underlying object function $F_{ob}: Ob \to Ob$ the [[identity function]] on $Ob$. 
\end{definition}

This simple definition goes against the [[principle of equivalence]], since it mentions equality of objects, and indeed identity of *sets* of objects. One solution is to alter the definition of equality so that equality is no longer a proposition, such as in type theory.

\begin{definition}
In [[type theory]], an **identity-on-objects [[functor]]** $F: A\to B$ between [[categories]] $A$ and $B$ in a [[univalent universe]] $\mathcal{U}$ is a functor between categories with the same [[type]] of [[objects]], i.e. there exists a type $Obj:\mathcal{U}$ and [[identity types]] $a:Ob =_\mathcal{U} ob(A)$ and $b:Ob =_\mathcal{U} ob(B)$, and has as its underlying object function $F_{ob}: Ob \to Ob$ the [[identity function]] on $Ob$. 
\end{definition}

If we assume that the [[strict category|categories are strict]], in the sense that the objects of a category form an [[set]], the identity types above are [[set]]s as well. If we assume the categories are [[univalent categories]], then the identity types in the definition above are [[groupoids]]. This is in contrast to the situation in [[set theory]] where identity/equality is always a [[proposition]]. 

If the [[type universe]] $\mathcal{U}$ above is not univalent, then one has to replace the identity types with equivalences: i.e. there exists a type $Obj:\mathcal{U}$ and equivalences $a:Ob \simeq_\mathcal{U} ob(A)$ and $b:Ob \simeq_\mathcal{U} ob(B)$, and which its underlying object function $F_{ob}: ob(A) \to ob(B)$ comes with an identity type $p:F_{ob} \circ a =_\mathcal{U} b$, or equivalently, which satisfies the [[commutative square]]

$$\array{& Ob & \overset{a}\rightarrow & ob(A) & \\
          id_{Ob} & \downarrow &&\downarrow & F_{ob}\\
          &Ob & \underset{b}\rightarrow& ob(B) & \\
}$$

This is the same as saying that the underlying object function $F_{ob}: ob(A) \to ob(B)$ is an equivalence of types $F_{ob}: ob(A) \simeq ob(B)$. In the presence of [[axiom K]], all types become sets, and equivalences become set isomorphisms. 

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[categories]] $A$ and $B$ is a [[functor]] whose underlying object function $F_{ob}: ob(A) \simeq ob(B)$ is an equivalence of object types in [[type theory]] and a set isomorphism of object sets in [[set theory]]. 
\end{definition}

This definition reflects the [[principle of equivalence]] that the true notion of identity between sets is set isomorphism, rather than propositional equality. 

On the other hand, in category theory the notion of "two categories with an identity-on-objects functor between them" is much more commonly used than the notion of "an identity-on-objects functor between two previously given categories". Instead of postulating two categories with a functor whose object function is a set isomorphism/type equivalence, one instead postulates one set or type $Ob$ of objects, with two families of arrows $A(x,y)$ and $B(x,y)$ for $x,y\in Ob$, each with composition and identities making each of $(Ob, A)$ and $(Ob, B)$ into a category structure, plus a family of functions $A(x,y) \to B(x,y)$ commuting with these category structures. This is the approach used to define [[dagger categories]] on the nLab in a way which doesn't violate the [[principle of equivalence]]. 

More abstractly, this can be defined as a category [[enriched category|enriched]] over the [[arrow category]] $Set^\to$.  See also [[M-category]] and [[F-category]].

## Related pages

* [[Freyd category]]
* [[Freyd multicategory]]
* [[dagger category]]
* [[principle of equivalence]]

[[!redirects identity-on-objects functors]]
[[!redirects identity on objects functor]]
[[!redirects identity on objects functors]]
[[!redirects io functor]]
[[!redirects io functors]]
[[!redirects i.o. functor]]
[[!redirects i.o. functors]]
