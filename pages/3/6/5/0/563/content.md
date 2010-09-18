
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Pseudofunctors
* table of contents
{: toc}

## Idea

A **pseudofunctor** is a specific algebraic notion of _weak $2$-[[2-functor|functor]]_ between [[bicategory|bicategories]] (including [[strict 2-category|strict 2-categories]]), i.e. a functor which preserves composition and identities only up to coherent specified isomorphism.

+--{: .query}
[[Tim]]: in specifying a pseudo functor $F$ you have to decide whether the isomorphism goes from $F(g f)$ to $F(g) F(f)$ or in the other direction. Of course they are equivalent as each will be inverse to the other. You might say that one is lax and pseudo the other op-lax and pseudo. When specifying the Grothendieck construction for such a functor, which is to be preferred? 

Both are about equally represented in the literature that I have seen which gets confusing. (In other words, I'm confused!)

_Toby_:  As you suggest, the two versions are equivalent, so in a way it doesn\'t make a difference.  But it might be nice to settle a convention in case we need it.


[[Tim]]: I have been using (for the Menagerie) the idea that there are pseudofunctors presented in two equivalent flavours lax pseudofunctor and oplax ones. 

[[Mike Shulman|Mike]]: Well, the natural comparison maps that you get in a [[Grothendieck fibration]] go in the "lax" direction $F(g) F(f) \to F(g f)$, since they are induced by the universal property of cartesian arrows.  In particular, if you have a functor with "weakly cartesian" liftings that don't compose, then it is a lax functor.  Not a very strong argument, but if we just want _some_ convention it might be a reason to pick lax.  I think that making too big a deal out of the difference would be misleading, though.
=--


In general, there is not much reason to say "pseudofunctor" instead of "functor," since the only relevant type of functor between arbitrary bicategories is weak.  However, if the domain and codomain are known to be [[strict 2-category|strict 2-categories]] (including ordinary $1$-[[1-category|categories]]), it can be helpful to say "pseudofunctor" or "weak functor" to emphasize that it is not a [[strict 2-functor]].  Note that if the codomain is a $1$-category, then there is no difference.

Pseudo or weak functors are also to be distinguished from [[lax functor]]s and [[lax functor|oplax functor]]s, which preserve identities and composition only up to a  transformation in one direction or the other, which may be non-invertible.

An older terminology, which should probably be avoided at all costs, uses "homomorphism of bicategories" for a weak functor and "morphism of bicategories" for a lax one.


## Definition

Given [[bicategories]] $C$ and $D$, a __pseudofunctor__ (or __weak $2$-functor__, or just __functor__) $P\colon C \to D$ consists of:

*  for each [[object]] $x$ of $C$, an object $P_x$ of $D$;
*  for each [[hom-category]] $C(x,y)$ in $C$, a [[functor]] $P_{x,y}\colon C(x,y) \rightarrow D(P_x,P_y)$;
*  for each object $x$ of $C$, an invertible [[2-morphism]] ($2$-cell) $P_{\id_x}\colon \id_{P_x} \Rightarrow P_{x,x}(\id_x)$;
*  for each triple $x,y,z$ of $C$-objects, a [[natural isomorphism|isomorphism]] (natural in $f\colon x \to y$ and $g\colon y \to z$) $P_{x,y,z}(f,g)\colon P_{x,y}(f) ; P_{y,z}(g) \Rightarrow P_{x,z}(f;g)$;
*  for each hom-category $C(x,y)$,
   $$ \array {
                                  &                                         & \id_{P_x} ; P_{x,y}(f) \\
                                  & {}^{P_{\id_x};\id_{P_{x,y}(f)}}\swArrow &                        & \seArrow^{\lambda_{P_{x,y}(f)}} \\
      P_{x,x}(\id_x) ; P_{x,y}(f) &                                         &                        &                                 & P_{x,y}(f) \\
                                  & {}_{P_{x,x,y}(\id_x,f)}\seArrow         &                        & \neArrow_{P_{x,y}(\lambda_f)} \\
                                  &                                         & P_{x,y}(\id_x;f) \\
   } $$
   and
   $$ \array {
                                  &                                         & P_{x,y}(f) ; \id_{P_y} \\
                                  & {}^{\id_{P_{x,y}(f)};P_{\id_y}}\swArrow &                        & \seArrow^{\rho_{P_{x,y}(f)}} \\
      P_{x,y}(f) ; P_{y,y}(\id_y) &                                         &                        &                              & P_{x,y}(f) \\
                                  & {}_{P_{x,y,y}(f,\id_y)}\seArrow         &                        & \neArrow_{P_{x,y}(\rho_f)} \\
                                  &                                         & P_{x,y}(f;\id_y) \\
   } $$
   commute; and
*  for each quadruple $w,x,y,z$ of $C$-objects,
   $$ \array {
      \big(P_{w,x}(f) ; P_{x,y}(g)\big) ; P_{y,z}(h)       & \overset{\alpha_{P_{w,x}(f),P_{x,y}(g),P_{y,z}(h)}}\Rightarrow & P_{w,x}(f) ; \big(P_{x,y}(g) ; P_{y,z}(h)\big) \\
      \mathllap{P_{w,x,y}(f,g);\id_{P_{y,z}(h)}}\Downarrow &                                                                & \Downarrow\mathrlap{\id_{P_{w,x}(f)};P_{x,y,z}(g,h)} \\
      P_{w,y}(f;g) ; P_{y,z}(h)                            &                                                                & P_{w,x}(f) ; P_{x,z}(g;h) \\
      \mathllap{P_{w,y,z}(f;g,h)}\Downarrow                &                                                                & \Downarrow\mathrlap{P_{w,x,z}(f,g;h)} \\
      P_{w,z}\big((f;g);h\big)                             & \underset{P_{w,z}(\alpha_{f,g,h})}\Rightarrow                  & P_{w,z}\big(f;(g;h)\big) \\
   } $$
   commutes.


## Lax functors

If we remove the requirement that $P_{\id_x}$ and $P_{x,y,z}(f,g)$ be invertible, then we have the definition of __[[lax functor]]__.  If we reverse the direction of these as well, then we have an __[[oplax functor]]__.


[[!redirects pseudofunctor]]
[[!redirects pseudofunctors]]
[[!redirects pseudo functor]]
[[!redirects pseudo functors]]
[[!redirects pseudo-functor]]
[[!redirects pseudo-functors]]
