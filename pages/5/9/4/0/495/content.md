
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An [[object]] of a [[category]] (usually a [[topos]] or [[pretopos]]) is _internally projective_ if it satisfies the [[internalization]] of the condition on a [[projective object]].

## Definition

An object $E$ of a [[topos]] $\mathcal{T}$ is called **internally projective** if the [[internal hom]]/[[exponential object]] [[functor]] 

$$
  (-)^E \colon \mathcal{T} \to \mathcal{T}
$$ 

preserves [[epimorphisms]].

## Equivalent characterizations

Some of these facts, and more, can be found stated in Exercises 15 and 16 in Chapter IV of [[Sheaves in Geometry and Logic]].

+-- {: .num_theorem #DepProd}
###### Theorem
$E$ is internally projective if and only if the [[dependent product]] functor (the [[right adjoint]] to [[pullback]])
$$ \Pi_E \colon \mathcal{T}/E \to \mathcal{T}$$
preserves epimorphisms.
=--
+-- {: .proof}
###### Proof
The functor $(-)^E$ is the composite $\Pi_E \circ E^*$, and pullback $E^*\colon \mathcal{T} \to \mathcal{T}/E$ preserves epis, so if $\Pi_E$ preserves epis then so does $(-)^E$.

Conversely, for any $f:A\to B$ in $\mathcal{T}/E$, we have a pair of pullback squares:
$$\array{
  \Pi_E A & \to & A^E \\
  \downarrow & & \downarrow\\
  \Pi_E B & \to & B^E \\
  \downarrow & & \downarrow\\
  1 & \xrightarrow{id_E} & E^E
}$$
The lower square and outer rectangle are easily seen to be pullbacks, hence so is the upper square.  Since epimorphisms are closed under pullback, the other implication follows.
=--

+-- {: .num_lemma #Stable}
###### Lemma
If $E$ is internally projective in $\mathcal{T}$, then $I^* E$ is internally projective in $\mathcal{T}/I$.
=--
+-- {: .proof}
###### Proof
This proof was given by [[Alex Simpson]] [here](http://mathoverflow.net/a/140262/49).  Let $q:B\to A$ be an epimorphism from $v:B\to I$ to $u:A\to I$.  Then the exponential $u^{I^*E}$ in $\mathcal{T}/I$ is the equalizer of
$$ I\times A^E \xrightarrow{pr_2} A^E \xrightarrow{u} I^E$$
and
$$ I\times A^E \xrightarrow{pr_1} I \xrightarrow{const} I^E $$
equipped with the obvious projection to $I$.  Now we have a pullback square
$$\array{
  v^{I^*E} & \to & I\times B^E \\
  \downarrow & & \downarrow \\
  u^{I^*E} & \to & I\times A^E
}$$
in which the right-hand map is epi since $E$ is internally projective; hence so is the left-hand map.
=--

+-- {: .num_theorem #StackSem}
###### Theorem
$E$ is internally projective if and only if the statement "$E$ is projective" is true in the [[stack semantics]] of $\mathcal{T}$.
=--
+-- {: .proof}
###### Proof
By definition, truth of "$E$ is projective" in the stack semantics means that for any $I$ and any epimorphism $A\to I\times E$, there exists an epimorphism $p:J\to I$ and a [[section]] of $(p\times id)^*A \to J\times E$.  (We have used the characterization that an object $X$ is projective just when every epimorphism with codomain $X$ is split.)

If $E$ is internally projective, then given an epimorphism $A\to I\times E$ as above, let $J = \Pi_{pr_1}(A)$, where $pr_1:I\times E \to I$ is the projection.  Since $I\times E$ is internally projective in $\mathcal{T}/I$ by Lemma \ref{Stable}, $p:J\to I$ is an epimorphism.  And $(p\times id)^*A \to J\times E$ is split by the [[counit]] of the adjunction $(pr_1)^* \dashv \Pi_{pr_1}$.

Conversely, suppose the above condition holds, and let $e:B\to A$ be an epimorphism in $\mathcal{T}/E$.  Let $I = \Pi_E(A)$, and let $C$ be the pullback of $e$ along the counit $\Pi_E(A) \times E\to A$.  Then $\Pi_E(B)$ is equivalently $\Pi_{pr_1}(C)$, where $pr_1:I \times E \to I$ is the projection.

Morevoer, $C \to I\times E$ is epi, so by assumption there is an epi $p:J\to I$ such that $(p\times id)^*C \to J\times E$ is split.  Since pullback along epis reflects epis, it suffices to show that $p^* \Pi_{pr_1}(C)$ is split.  However, we have a pullback square
$$ \array{
  J\times E & \to & I\times E \\
  ^{pr_1}\downarrow & & \downarrow^{pr_1} \\
  J & \to & I
}$$
so by the [[Beck-Chevalley condition]], $p^* \Pi_{pr_1}(C)$ is equivalently $\Pi_{pr_1}(p\times id)^* C$.  But $(p\times id)^*C$ is split, and all functors preserve split epis.
=--

Note that Lemma 4.5.3(iii) of [[Sketches of an Elephant]] is the special case of the above stack-semantics version of internal projectivity when $I=1$.  This is insufficient for the implication (iii)$\Rightarrow$(ii) of that lemma to hold, since if so, then every projective object would be internally projective, which as we show below is not the case.


## Projectivity versus internal projectivity

If the [[terminal object]] in $\mathcal{T}$ is [[projective object|projective]], then every internally projective object is projective. In the converse direction, 

+-- {: .num_prop #enough} 
###### Proposition 
If $\mathcal{T}$ has [[projective object|enough projectives]] and projectives are closed under binary [[products]], then every projective object is internally projective. (In particular, if all objects of $\mathcal{T}$ are projective then all objects are internally projective.) 
=-- 

+-- {: .proof}
###### Proof 
Let $P$ be a projective object. To show that $e^P \colon E^P \to B^P$ is epic whenever $e \colon E \to B$ is epic, choose an epi $\phi \colon P' \to B^P$ where $P'$ is projective (using the assumption of enough projectives). Since $P \times P'$ is projective, there exists a lift through $e$ of the horizontal composite as shown: 

$$\array{
 & & & & E \\
 & & & & \downarrow ^\mathrlap{e} \\ 
P' \times P & \underset{\phi \times 1}{\to} & B^P \times P & \underset{eval}{\to} & B; 
}$$ 

this, by [[currying]], provides a lift of $\phi \colon P' \to B^P$ through $e^P$. Since $\phi$ is epic, this immediately implies $e^P$ is epic, as desired. 
=-- 

+-- {: .num_remark} 
###### Remark 
Proposition \ref{enough} may fail without the assumption that projective objects are closed under binary products. An example is given [here](/nlab/show/presentation+axiom#counter). 
=--  

+-- {: .num_remark}
###### Remark 
The _internal axiom of choice_ (that is, the [[axiom of choice]] interpreted in the [[internal logic]] of the topos) is equivalent to the statement that every object is internally projective.  This is strictly weaker than the "external" axiom of choice that every [[epimorphism]] in the topos is [[split epimorphism|split]]. 
=-- 

+-- {: .num_cor #presheaf} 
###### Corollary 
In a presheaf topos $Set^{C^{op}}$, if $C$ has binary products, then every projective presheaf is internally projective. 
=-- 

+-- {: .proof} 
###### Proof 
Representables, and arbitrary coproducts of representables, are projective, and every presheaf is covered by some coproduct of representables. This implies that projective presheaves are precisely retracts of coproducts of representables. Under the assumption that $C$ has binary products, coproducts of representables, and also their retracts, are also closed under binary products. Thus projective presheaves are closed under binary products. Now apply Proposition \ref{enough}. 
=-- 

## Discussion

* Forum discussions [one](http://nforum.ncatlab.org/discussion/3008/internally-projective-objects/), [two](http://nforum.ncatlab.org/discussion/4342/internally-projective-objects/).

## Related concepts

* [[projective object]], [[projective presentation]], [[projective cover]], [[projective resolution]]

  * [[projective module]]

  * [[internally projective object]]

* [[injective object]], [[injective presentation]], [[injective envelope]], [[injective resolution]]

  * [[injective module]]

* [[free object]], [[free resolution]]
 
  * [[free module]]

* flat object, [[flat resolution]]

  * [[flat module]]

[[!redirects internally projective objects]]