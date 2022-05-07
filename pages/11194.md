
> This entry is about dualizing objects in closed (monoidal) categories in the sense of [[homological algebra]] and [[stable homotopy theory]] (e.g. [[dualizing modules]]). For a more general concept see at _[[dualizing object]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _dualizing object_ $D$ in a [[closed category]] $\mathcal{C}$ is an [[object]] such that the [[internal hom]] $[-,D] \colon \mathcal{C} \to \mathcal{C}^{op}$ into it serves as an [[involution|involutive]] [[duality]] operation on $\mathcal{C}$, or at least on a suitable [[full subcategory]] $\mathcal{C}_D \hookrightarrow \mathcal{C}$, i.e. it induces an [[equivalence of categories]] $[-,D] \colon \mathcal{C}_D \to \mathcal{C}_D^{op}$.

## Definition

Let $\mathcal{C}$ be a [[closed category]], $D\in \mathcal{C}$ an object, and $\mathcal{C}_D \hookrightarrow \mathcal{C}$ a [[full subcategory]].  We say that $D$ is a **dualizing object on $\mathcal{C}_D$** if the induced functor

$$ [-,D] : \mathcal{C}_D \to \mathcal{C}_D^{op} $$

is an [[equivalence of categories]].  Note that this includes the assumption that $[-,D]$ maps $\mathcal{C}_D$ into itself, which is not automatic.

Note that we do not in general assume $D\in \mathcal{C}_D$.  In [[stable homotopy theory]] the subcategory in question is typically that of [[homotopy types with finite homotopy groups]] (e.g. for [[Anderson duality]]). Specifically in [[homological algebra]] one speaks also of _[[dualizing modules]]_. (See for instance ([Heard-Stojanoska 14, def. 3.1](#HeardStojanoska14) and [[Representability Theorems|Lurie, section 4.2]]).)  Notably in a [[Grothendieck-Verdier context]] $(f^\ast \dashv f_\ast)$, $(f_! \dashv f^!)$ of [[six operations]] the functor $f^!$ typically preserves dualizing objects in this sense, which is a crucial ingredient of [[Verdier duality]].

If $\mathcal{C} = \mathcal{C}_D$, we say that $D$ is a **global dualizing object**.  A biclosed monoidal category $\mathcal{C}$ with a global dualizing object is one definition of a [[star-autonomous category]].


### In closed monoidal categories

If $\mathcal{C}$ is a [[closed symmetric monoidal category]], then $[-,D]$ is adjoint to itself on the right, i.e. we have a natural isomorphism $\mathcal{C}(A,[B,D]) \cong \mathcal{C}(B,[A,D])$.  Thus, if $[-,D]$ maps $\mathcal{C}_D$ into itself, then its restriction to $\mathcal{C}_D$ is an equivalence of categories if and only if the unit and counit of this adjunction are isomorphisms.  But these unit and counit are both the "double-dualization" map

$$A \to [[A,D],D]$$

(the [[adjunct]] of the [[evaluation map]] $[A,D] \otimes A \to D$, which in turn is the adjunct of the identity map $[A,D] \to [A,D]$) for $A\in \mathcal{C}_D$; so $D$ is a dualizing object on $\mathcal{C}_D$ if and only if $[-,D]$ preserves $\mathcal{C}_D$ and these maps are isomorphisms for all $A\in \mathcal{C}_D$.

If $\mathcal{C}$ is a non-symmetric [[biclosed monoidal category]], with two internal-homs $(A\otimes -) \dashv [A,-]$ and $(-\otimes A) \dashv \langle A,-\rangle$, then $[-,D]$ is adjoint on the right not to itself but to $\langle-,D\rangle$.  A similar argument then shows that $D$ is dualizing if and only if $[-,D]$ and $\langle-,D\rangle$ both map $\mathcal{C}_D$ to itself, and both double-dualization maps

$$ A\to \langle [A,D],D\rangle\qquad and \qquad A \to [\langle A,D\rangle,D]$$

are isomorphisms.


## Examples

### In a cartesian closed category
 {#InACartesianClosedCategory}

A [[cartesian closed category]] that with a global dualizing object is necessarily just a [[preorder]].  This statement is often known as _[[Joyal]]'s lemma_, recalled for instance in [Abramsky 09](#Abramsky09).  It can be slightly strengthened as follows: 

+-- {: .num_prop} 
###### Proposition 
A cartesian closed category $C$ that is self-dual (carries an equivalence $N: C^{op} \to C$) is necessarily a preorder (whose posetal reflection is then a [[Heyting algebra]]). If the self-duality comes from a dualizing object, then the Heyting algebra is a Boolean algebra. 
=-- 

+-- {: .proof} 
###### Proof 
For the first statement, let $1$ be terminal; then $N(1)$ is an initial object $0$, and similarly $N$ takes finite products to finite coproducts (coproducts are necessary for a Heyting algebra). So it remains to show $C$ is a preorder. Let $x, y$ be any two objects. The number of morphisms $x \to y$ is the number of morphisms $1 \to [x, y]$, which is the number of morphisms $N([x, y]) \to N(1) = 0$. But this is at most one since the initial object is strict (if there is any $z \to 0$, then $z$ is a retract of $0 \times z \cong 0$, hence $z \cong 0$; thus there is at most one morphism $z \to 0$). 

The second statement is immediate: if $d$ is the dualizing object, then 

$$d \cong [1, d] = N(1) \cong 0$$ 

so that $N(x) = [x, 0]$ is the negation and the hypothesis becomes the condition that double negation on the Heyting algebra is the identity, i.e., the Heyting algebra is a Boolean algebra. 
=-- 

### In the category of spectra -- Anderson duality

In the [[stable (infinity,1)-category of spectra]], the [[sphere spectrum]] (which induces [[Spanier-Whitehead duality]] on spectra which are [[dualizable objects]] with respect to the [[smash product of spectra]]) is not a dualizing object.  However, the [[Anderson spectrum]] $I_{\mathbb{Z}}$ is a dualizing object on a suitable subcategory of finite spectra ([[Representability Theorems|Lurie, Example 4.3.9]]).  The [[duality]] operation $[-,I_{\mathbb{Z}}]$ that it induces is [[Anderson duality]].

For instance, the Anderson dual of [[KU]] is (complex conjugation-equivariantly) the 4-fold [[suspension spectrum]] $\Sigma^4 KU$ ([Heard-Stojanoska 14, theorem 8.2](#HeardStojanoska14)); and [[tmf]]$[1/2]$ is Anderson dual to its 21-fold suspension ([Stojanoska 12](#Stojanoska12))

### In the category of suplattices

In the category [[Sup]] of [[suplattices]], the opposite $\Omega^{op}$ of the poset $\Omega$ of [[truth values]] is a global dualizing object (and hence $Sup$ is [[star-autonomous category|star-autonomous]]).  The internal-hom $[A,B]$ is the suplattice of sup-preserving maps $A\to B$, hence $[A,\Omega^{op}]$ is the suplattice of contravariant maps $A \to \Omega^{op}$ that take suprema in $A$ to infima in $\Omega$.  But by the [[adjoint functor theorem]] for posets, any such map is representable by an element of $A$; thus $[A,\Omega^{op}] \cong A^{op}$.  The double-dualization is therefore isomorphic to the identity $A\cong (A^{op})^{op}$.

### Chu spaces

The [[Chu construction]] is a (co)universal way of "making any object into a dualizing object".


## Related concepts

* [[dual object in a closed category]]
* [[star-autonomous category]]
* [[Chu construction]]
* [[ambimorphic object]]

## References

General discussion is in 

* {#BoryachenkoDrinfeld11} [[Mitya Boryachenko]], [[Vladimir Drinfeld]], _A duality formalism  in the spirit of Grothendieck and Verdier_ ([arXiv:1108.6020](http://arxiv.org/abs/1108.6020))

* [[Jacob Lurie]], section 4.2 of _[[Representability Theorems]]_

Reviews of the general concept and then discussion of [[Anderson duality]] is in

* {#Stojanoska12} [[Vesna Stojanoska]], _Duality for Topological Modular Forms_, Doc. Math. 17 (2012) 271-311 ([arXiv:1105.3968](http://arxiv.org/abs/1105.3968))

* {#HeardStojanoska14} [[Drew Heard]], [[Vesna Stojanoska]], _K-theory, reality, and duality_ ([arXiv:1401.2581](http://arxiv.org/abs/1401.2581))

Discussion in the context of the [[linear logic]]/[[quantum logic]] of [[quantum physics]] is in 

* {#Abramsky09} [[Samson Abramsky]], _No-Cloning in categorical quantum mechanics_, (2008) in I. Mackie and S. Gay (eds), _Semantic Techniques for Quantum Computation_ , Cambridge University Press ([arXiv:0910.2401](http://arxiv.org/abs/0910.2401))


[[!redirects dualizing objects in a closed category]]
[[!redirects dualizing objects in closed categories]]
