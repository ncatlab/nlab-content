#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In [[type theory]] under the [[propositions as types]] paradigm, an **identity type** is the incarnation of [[equality]].  That is, for any type $A$ and any terms $x,y:A$, the type $Id_A(x,y)$ is "the type of proofs that $x=y$" or "the type of reasons why $x=y$".

In *extensional* type theory, such as that modeled in the [[internal logic]] of a 1-category, equality is simply a [[proposition]], and hence each $Id_A(x,y)$ is a [[subsingleton]].  However, in the internal type theory of [[higher category theory|higher categories]], such as the [[internal logic of an (∞,1)-topos]], identity types represent [[path objects]] and are highly nontrivial.  In these cases, one may write for instance $Path_A(x,y)$ instead of $Id_A(x,y)$.


## Definition

The rules for forming identity types and terms are as follows.  First the rule that defines the identity type itself, as a [[dependent type]], in some [[context]] $\Gamma$.

$$\frac{\Gamma \vdash A:Type}
{\Gamma, x:A, y:A \vdash Id_A(x,y):Type}$$


Now the basic "introduction" rule, which says that everything is equal to itself in a canonical way.

$$\frac{\Gamma \vdash A:Type}
{\Gamma, x:A \vdash r(x) : Id_A(x,x)}$$

To a category theorist, it might be more natural to call this $1_X$.  The traditional notation $r(x)$ indicates that this is a canonical proof of the *reflexivity* of equality.

Then we have the "elimination" rule, which is easily the most subtle and powerful.

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \qquad
\Gamma, x:A, \Delta(x,x,r(x)) \vdash t : C(x,x,r(x))}
{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash J(t;x,y,p) : C(x,y,p)}$$

Ignore the presence of the additional context $\Delta$ for now; it is unnecessary if we also have [[dependent product type]]s.  The elimination rule then says that if:

1. for any $x,y:A$ and any reason $p:Id_A(x,y)$ why they are the same, we have a type $C(x,y,p)$, and
1. if $x$ and $y$ are actually identical and $p:Id_A(x,x)$ is the reflexivity proof $r(x)$, then we have a specified term $t:C(x,x,r(x))$,

then we can construct a canonically defined term $J(t;x,y,p):C(x,y,p)$ for *any* $x$, $y$, and $p:Id_A(x,y)$, by "transporting" the term $t$ along the proof of equality $p$.  In homotopical or categorical models, this can be viewed as a "path-lifting" property, i.e. that the [[display map]]s are some sort of [[fibration]].  This can be made precise with the [[identity type weak factorization system]].

A particular case is when $C$ is a term representing a proposition according to the propositions-as-types philosophy.  In this case, the elimination rule says that in order to prove a statement is true about all $x,y,p$, it suffices to prove it in the special case for $x,x,r(x)$.

Finally, we have the "computation" rule, which says that if we substitute along a reflexivity proof, nothing happens.

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \qquad
\Gamma, x:A, \Delta(x,x,r(x)) \vdash t : C(x,x,r(x))}
{\Gamma, x:A, \Delta(x,x,r(x)) \vdash J(t;x,x,r(x)) = t}$$

These rules may seem a little ad-hoc, but they are actually a particular case of the general notion of [[inductive type]].


## Types are weak $\omega$-groupoids

...

References:

* Benno van den Berg, [[Richard Garner]], *Types are weak $\omega$-groupoids*, [arXiv:0812.0298](http://arxiv.org/abs/0812.0298)

* Peter Lumsdaine, *Weak $\omega$-categories from intensional type theory*, [arXiv:0812.0409](http://arxiv.org/abs/0812.0409)


[[!redirects identity types]]
[[!redirects equality type]]
[[!redirects equality types]]
