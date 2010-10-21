
<div class="rightHandSide toc">
[[!include topos theory - contents]]
</div>

This page is about **direct images of sheaves** and related subjects.  For the set-theoretic operation, see [[image]].

***

#Contents#
* automatic table of contents goes here
{:toc}


## Idea 

The [[right adjoint]] part $f_*$ of any [[geometric morphism]] 

$$  
  (f^* \dashv f_*) \;\; : E_1  \leftrightarrows E_2
$$

of [[topos]]es is called a **direct image**.

Moe generally, pairs of [[adjoint functor]]s between the [[categories of sheaves]] appear in various other setups apart from [[geometric morphism]]s of [[topoi]], for instance on [[abelian categories]] of [[quasicoherent sheaves]], bounded [[derived categories]] of [[coherent sheaves]] and the term _direct image_ is used for the right adjoint part of these, too.


Specifically for [[Grothendieck topos]]es:
a [[site|morphism of sites]] $f : X \to Y$ induces a [[geometric morphism]] of [[Grothendieck topos]]es


$$
  (p^* \dashv p_*)
  \;\;\;
  :
  \;\;\;
  Sh(X) \stackrel{}{\stackrel{\overset{p_*}{\to}}{\overset{p^*}{\leftarrow}}}
  Sh(Y)
$$

between the [[category of sheaves|categories of sheaves]] on the sites, with 

* $p_*$ the **direct image**

* and $p^*$ its [[left adjoint]]: the [[inverse image]].




## Definition

Given a [[site|morphism of sites]] $f : X \to Y$ coming from a [[functor]] $f^t : S_Y \to S_X$, the **direct image** operation on [[presheaf|presheaves]] is the functor

$$
  f_* : PSh(X) \to PSh(Y)
$$
$$
  f_* F : S_Y^{op} \stackrel{f^t}{\to} S_X^{op} \stackrel{F}{\to} Set
  \,.
$$

The restriction of this operation to [[sheaf|sheaves]], which respects sheaves, is the **direct image of sheaves**

$$
  f_* : Sh(X) \to Sh(Y)
  \,.
$$



## Examples


### Global sections

For $X$ a [[site]] with a [[terminal object]], let the morphism of [[site]]s be the canonical morphism $p : X \to {*}$.

* The direct image $p_*$ is the [[global section]]s functor;

* the inverse image $p^*$ is the [[constant sheaf]] functor;

* the left adjoint to $p^*$  is $\Pi_0$, the functor of geometric connected components (see [[homotopy group of an ∞-stack]]).




### Restriction and extension of sheaves

See 

* [[restriction and extension of sheaves]] 

for the moment.

[[!redirects direct images]]
[[!redirects direct image functor]]