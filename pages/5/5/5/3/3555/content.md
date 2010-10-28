
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

If an [[(∞,1)-topos]] $\mathbf{H}$ is that of [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaves]] on (the [[site]] of [[category of open subsets|open subsets]] of) a [[paracompact space|paracompact]] [[topological space]] -- $\mathbf{H} = Sh_{(\infty,1)}(X)$ --  then its **shape** is the _strong shape_ of $X$ in the sense of [[shape theory]]: a [[pro-object]] $Shape(X)$ in the category of [[CW-complex]]es.

It turns out that $Shape(X)$ may be extracted in a canonical fashion from just the [[(∞,1)-topos]] $Sh_{(\infty,1)}(X)$, and in a way that makes sense for any [[(∞,1)-topos]]. This then gives a definition of shape of general $(\infty,1)$-toposes.

## Definition


+-- {: .un_def}
###### Definition

The composite [[(∞,1)-functor]]

$$
  \Pi : (\infty,1)Topos 
     \stackrel{Y}{\to}  Func((\infty,1)Topos, \infty Grpd)^{op}
      \stackrel{Lex(PSh(-), \infty Grpd)}{\to}
      Lex(\infty Grpd, \infty Grpd)^{op}
     \simeq
       Pro \infty Grpd
$$

is the **shape functor** . Its value 

$$
  \Pi(\mathbf{H}) = 
  (\infty,1)Topos(\mathbf{H}, PSh(-))
$$ 

on an $(\infty,1)$-topos $\mathbf{H}$ is the **shape** of $\mathbf{H}$.

=--

Here

* [[(∞,1)Topos]] is the [[(∞,1)-category]] of [[(∞,1)-topos]]es;

* [[∞Grpd]] is the $(\infty,1)$-category of [[∞-groupoid]]s;

* $Y$ is the [[(∞,1)-Yoneda embedding]];

* $Func(-,-)$ is the [[(∞,1)-category of (∞,1)-functors]];

* $Lex(-,-) \subset (\infty,1)Func(-,-)$ is the full [[sub-(∞,1)-category]]
  of the [[(∞,1)-category of (∞,1)-functors]] on those which are left [[exact functor]]s (preserve finite [[(∞,1)-limit]]s);

* $PSh(-) : \infty Grpd \to (\infty,1)Topos$ is the functor that 
  produces the [[(∞,1)-category of (∞,1)-presheaves]] $Func(X^{op}, \infty Grpd)$ on $X$ (equivalently on the equivalent [[opposite (∞,1)-category|opposite ∞-groupoid]] $X^{op}$);

* $Pro \infty Grpd$ is the [[pro-object in an (∞,1)-category|(∞,1)-category of pro-objects]] in $\infty Grpd$.

That this does indeed land in left exact functors is shown below.

## Properties


Notice that for every [[(∞,1)-topos]] $\mathbf{H}$ there is a unique [[geometric morphism]]

$$
  (LConst \dashv \Gamma) : \mathbf{H} \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

where [[∞Grpd]] is the $(\infty,1)$-topos of [[∞-groupoids]],  $\Gamma$ is the [[global section]]s [[(∞,1)-functor]] and $LConst$ is the [[constant ∞-stack]] functor.




+-- {: .un_prop}
###### Proposition

The **shape** of $\mathbf{H}$ is the composite functor

$$
  \Pi(\mathbf{H}) := \Gamma \circ LConst
  \;\;:\;\;
  \infty Grpd \stackrel{LConst}{\to}
  \mathbf{H}
  \stackrel{\;\;\Gamma\;\;}{\to}
  \infty Grpd
$$

regarded as an object 

$$
  \Pi(\mathbf{H})
  \in
  Pro(\infty Grpd)
  =
  Lex(\infty Grpd, \infty Grpd)^{op}
  \,.
$$

=--

+-- {: .proof}
###### Proof

For $X \in $ [[∞Grpd]] we have by the [[(∞,1)-Grothendieck construction]]-theorem and using that up to equivalence every morphism of $\infty$-groupoids is a [[Cartesian fibration]] (see there) that 

$$
  Func(X,\infty Grpd) \simeq \infty Grpd/X
$$ 

is the [[over-(∞,1)-category]].  Moreover, by the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#WithValInooGrpd">theorem about limits in ∞Grpd</a> we have that the terminal geometric morphism $Hom(*,-): [X, \infty Grpd] \to \infty Grpd$ is the canonical projection $\infty Grpd/ X \to \infty Grpd$. This means that it is an [[etale geometric morphism]]. So for any [[geometric morphism]] $f : \mathbf{H} \to [X, \infty Grpd]$  we have a system of [[adjoint (∞,1)-functor]]s

$$
  (LConst \dashv \Gamma)
   :
  \mathbf{H}
    \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
   \infty Grpd/X
    \stackrel{\overset{\pi^*}{\leftarrow}}{\underset{\pi_*}{\to}}    
   \infty Grpd
  \,.
$$

whose composite is the [[global section]] geometric morphism as indicated, because that is terminal.

Notice that in $\infty Grpd/X$ there is a canonical morphism

$$
  (* \to  \pi^* X) := (X \stackrel{(Id,Id)}{\to} X \times X)
  \,.
$$

The image of this under $f^*$ is (using that this preserves the terminal object) a morphism

$$
  * \to f^* \pi^* X = LConst X
$$

in $\mathbf{H}$.

Conversely, given a morphism of the form $* \to LConst X$ in $\mathbf{H}$ we obtain the [[base change geometric morphism]]

$$
  \mathbf{H} \simeq \mathbf{H}/* \to \mathbf{H}/LConst X
   \stackrel{\Gamma}{\to}
  \infty Grpd/X
  \,.
$$

One checks that these constructions establish an equivalence

$$
  (\infty,1)Topos(\mathbf{H}, \infty Grpd/X)
  \simeq
  \mathbf{H}(*, LConst X)
  \,.
$$

Using this, we see that 

$$
  \begin{aligned}
    \Pi (\mathbf{H}) : X \mapsto & (\infty,1)Topos(\mathbf{H}, X)
     \\
      & \simeq \mathbf{H}(*,LConst X)
     \\
      & \simeq \mathbf{H}(LConst *, LConst X)
     \\
      & \simeq \infty Grpd(*, \Gamma LConst X)
    \\
      & \simeq \Gamma LConst X
  \end{aligned}   
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

In particular this does show that $\Pi(\mathbf{H}) : \infty Grpd \to \infty Grpd$ does preserve finite $(\infty,1)$-limits, since $\Gamma$ preserves all limits and $LConst$ is a left [[exact functor]].

=--

## Examples

### Shape of a locally $\infty$-connected topos

Suppose that $\mathbf{H}$ is [[locally ∞-connected (∞,1)-topos|locally ∞-connected]], meaning that $\Gamma$ has a left adjoint $\Pi$ which constructs the [[geometric homotopy groups in an (∞,1)-topos|homotopy ∞-groupoids]] of objects of $\mathbf{H}$.  Then $\Shape(\mathbf{H})$ is [[representable functor|represented]] by $\Pi(*)\in \infty Grpd$, for we have

$$
\begin{aligned}
Shape(\mathbf{H})(A) &= \Gamma(LConst(A))\\
&= Hom_{\infty Grpd}(*, \Gamma(LConst(A)))\\
&= Hom_{\mathbf{H}}(LConst(*), LConst(A)) \\
&= Hom_{\mathbf{H}}(*, LConst(A)) \\
&= Hom_{\infty Grpd}(\Pi(*),A).
\end{aligned}
$$

Thus, if we regard $\Pi(*)$ as "the homotopy $\infty$-groupoid of $\mathbf{H}$" --- which is reasonable since when $\mathbf{H}=Sh(X)$ consists of sheaves on a locally contractible [[topological space]] $X$, $\Pi_{\mathbf{H}}(*)$ is equivalent to the usual [[fundamental ∞-groupoid]] of $X$ --- then we can regard the shape of an $(\infty,1)$-topos as a generalized version of the "homotopy $\infty$-groupoid" which nevertheless makes sense even for non-locally-contractible toposes, by taking values in the larger category of "pro-$\infty$-groupoids."


### Shape of a topological space

For a discussion of how the $(\infty,1)$-topos theoretic shape of $Sh_{(\infty,1)}(X)$ relates to the ordinary shape-theoretic _strong shape_ of the topological space $X$ see [[shape theory]].


### Shape of an essential retract {#Retract}

The following is trivial to observe, but may be useful to note.

+-- {: .un_lemma}
###### Observation

Let $(f_! \dashv f^* \dashv f_*) : \mathbf{H} \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}} \mathbf{B}$ be an [[essential geometric morphism]] of $(\infty,1)$-toposes that exhibits $\mathbf{B}$ as an essential [[retract]] of $\mathbf{H}$ in that 

$$
  (Id \dashv Id)
  \;\;
  \simeq
  \;\;
  \mathbf{B}
    \stackrel{\overset{f_!}{\leftarrow}}{\underset{f^*}{\to}} 
  \mathbf{H}
    \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}} 
  \mathbf{B}
  \,.
$$

Then the shape of $\mathbf{B}$ is equivalent to that of $\mathbf{H}$.

=--

+-- {: .proof}
###### Proof

Since $\infty Grpd$ is the [[terminal object]] in the category of Grothendieck $(\infty,1)$-toposes and [[geometric morphisms]], we have

$$
  \begin{aligned}
    (\infty Grpd \stackrel{LConst_{\mathbf{B}}}{\to} \mathbf{B} 
     \stackrel{\Gamma_\mathbf{B}}{\to} \infty Grpd)
    &\simeq
    (\infty Grpd 
      \stackrel{LConst_{\mathbf{B}}}{\to} 
      \mathbf{B} 
      \stackrel{f^*}{\to} \mathbf{H}   
     \stackrel{f_*}{\to} \mathbf{B}
     \stackrel{\Gamma_\mathbf{B}}{\to}
     \infty Grpd)
    \\
    &\simeq
    (\infty Grpd 
     \stackrel{LConst_\mathbf{H}}{\to} 
     \mathbf{H} 
      \stackrel{\Gamma_\mathbf{H}}{\to}
      \infty Grpd)    
  \end{aligned}
  \,.
$$

=--


+-- {: .un_example}
###### Example

Every 

* [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] or [[∞-connected (∞,1)-topos]] 

* and hence also every [[cohesive (∞,1)-topos]] 

over $\infty Grpd$ has the shape of the point.

=--


+-- {: .proof}
###### Proof

By definition $\mathbf{H}$ is $\infty$-connected if the [[constant ∞-stack]] [[inverse image]] $f^* = L Const$ is 

1. not only a left but also a [[right adjoint]];

1. is a [[full and faithful (∞,1)-functor]].

By standard properties of [[adjoint (∞,1)-functor]]s we have that a [[right adjoint]] $f^*$ is a [[full and faithful (∞,1)-functor]] precisely if the counit $f_! f^* \to Id$ is an [[equivalence in a quasi-category|equivalence]].

Equivalently, we can observe that a locally ∞-connected (∞,1)-topos is ∞-connected precisely when $\Pi$ preserves the terminal object, and apply the above observation that the shape of a locally ∞-connected (∞,1)-topos is represented by $\Pi(*)$.

=--


## References

The definition of shape of $(\infty,1)$-toposes as $\Gamma \circ LConst$ is due to

* [[Bertrand Toen]] and [[Gabriele Vezzosi]],  _Segal topoi and stacks over Segal categories_ , in Proceedings of the
Program _Stacks, Intersection theory and Non-abelian Hodge Theory_ , MSRI, Berkeley, January-May 2002 ([arXiv:math/0212330](http://arxiv1.library.cornell.edu/abs/math/0212330)).

This and the relation to [[shape theory]] of topological spaces is further discussed in section 7.1.6 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects shape of an (∞,1)-topos]]
