
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


This page is about **direct images of sheaves** and related subjects.  For the set-theoretic operation, see [[image]].

***

#Contents#
* table of contents
{:toc}


## Idea 

The [[right adjoint]] part $f_*$ of any [[geometric morphism]] 

$$  
  (f^* \dashv f_*) \;\; : E_1  \leftrightarrows E_2
$$

of [[topos]]es is called a **direct image**.

More generally, pairs of [[adjoint functor]]s between the [[categories of sheaves]] appear in various other setups apart from [[geometric morphism]]s of [[topoi]], for instance on [[abelian categories]] of [[quasicoherent sheaves]], bounded [[derived categories]] of [[coherent sheaves]] and the term _direct image_ is used for the right adjoint part of these, too.


Specifically for [[Grothendieck topos]]es:
a [[morphism of sites|morphism of sites]] $f : X \to Y$ induces a [[geometric morphism]] of [[Grothendieck topos]]es


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

### Direct image with compact supports
 {#DirectImageWithCompactSupport}

Let $f:X\to Y$ be a morphism of [[locally compact topological spaces]]. Then there exist a unique [[subfunctor]] $f_!: Sh(X)\to Sh(Y)$ of the direct image functor $f_*$ such that for any [[abelian sheaf]] $F$ over $X$ the sections of $f_!(F)$ over $U^{open}\subset X$ are those sections $s\in f_*(U)= \Gamma(f^{-1}(U),F)$ for which the restriction $supp(s)|f : supp(s)\hookrightarrow U$ is a [[proper map]]. 

This is called the [[direct image with compact support]].

It follows that $f_!$ is left exact. 

Let $p:X\to {*}$ be the map into the one point space. Then for any $F\in Sh(X)$ the [[abelian sheaf]] $p_!F$ is the [[abelian group]] consisting of sections $s\in \Gamma(X,F)$ such that $supp(s)$ is compact. One writes $\Gamma_c(X,F) \coloneqq p_! F$ and calls this group a group of sections of $F$ with compact support. If $y\in Y$, then the fiber $(f_! F)_y$ is isomorphic to $\Gamma_c(f^{-1}y,F|_{f^{-1}(y)})$. 

### Derived direct image


+-- {: .num_prop}
###### Proposition

Let $f^{-1} \colon Y \to X$ be a [[morphism of sites]].
Then the $q$th [[derived functor]] $R^q f_\ast$ of the induced [[direct image]] functor sends $\mathcal{F} \in Ab(Sh(X_{et}))$ to the [[sheafification]] of the [[presheaf]]

$$
  U_Y
  \mapsto
  H^q(f^{-1}(U_Y), \mathcal{F})
  \,,
$$

where on the right we have the degree $q$ [[abelian sheaf cohomology]] [[cohomology group|group]] with [[coefficients]] in the given $\mathcal{F}$.


=--

(e.g. [Tamme, I (3.7.1), II (1.3.4)](#Tamme), [Milne, 12.1](#Milne)).


+-- {: .proof}
###### Proof

We have a [[commuting diagram]]

$$
  \array{
    Ab(PSh(X)) &\stackrel{(-)\circ f^{-1}}{\longrightarrow}& Ab(PSh(Y))
    \\
    \uparrow^{\mathrlap{inc}} && \downarrow^{L}
    \\
    Ab(Sh(X)) &\stackrel{f_\ast}{\longrightarrow}& Ab(Sh(Y))
  }
  \,,
$$

where the right vertical morphism is [[sheafification]]. Because $(-) \circ f^{-1}$ and $L$ are both [[exact functors]] it follows that for $I^\bullet \to \mathcal{F}$ an [[injective resolution]] that

$$
  \begin{aligned}
     R^p f_\ast(\mathcal{F})
     & :\simeq
     H^p( f_\ast I)
     \\
     & = H^p(L I^\bullet(f^{-1}(-)))
     \\
     & = L (H^p(I^\bullet)(f^{-1}(-)))
  \end{aligned}
$$

=--


## Related concepts

* [[derived direct image]]

## References

e.g.

* [[Günter Tamme]], section II 1 of _[[Introduction to Étale Cohomology]]_
 {#Tamme}

* [[James Milne]], section 7 of _[[Lectures on Étale Cohomology]]_
 {#Milne}


[[!redirects direct images]]
[[!redirects direct image functor]]