
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Operator algebra and AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Theorems observed by Harding, D&#246;ring and Hamhalter say that under some conditions the [[Jordan algebra]] structure of a [[C*-algebra]] is effectively captured by its [[poset of commutative subalgebras]].

Via the [[Alfsen-Shultz theorem]], which states that two [[C*-algebra]] have the same [[states]] precisely if they are isomorphic as [[Jordan algebras]], this is related to [[Gleason's theorem]], which says that states on an [[algebra of bounded operators]] are determined by their restriction to commutative subalgebras (if the underlying Hilbert space has dimenion $\gt 2$).

## Statements

For $A$ an [[associative algebra]] write $A_J$ for its corresponding [[Jordan algebra]], where the commutative product $\circ : A_J \otimes A_J \to A_J$ is the symmetrization of the product in $A$: $a \circ b = \frac{1}{2}(a b + b a)$.

+-- {: .num_lemma}
###### Observation

There exist [[von Neumann algebras]] $A$, $B$ such that there exists a [[Jordan algebra]] isomorphism $A_J \to B_J$ but not an algebra isomorphism $A \to B$.

=--

+-- {: .proof}
###### Proof

By 

* [[Alain Connes]], _A factor not anti-isomorphic to itself_, Annals of Mathematics, 101 (1975), no. 3, 536&#8211;554. ([JSTOR](http://www.jstor.org/stable/1970940))

there is a [[von Neumann algebra factor]] $A$ with no algebra isomorphism to its opposite algebra $A^{op}$. But clearly $A_J \simeq (A^{op})_J$.

=--

+-- {: .num_prop}
###### Proposition

Let $A, B$ be [[von Neumann algebra]]s without a type $I_2$-[[von Neumann algebra factor]]-summand and let $ComSub(A)$, $ComSub(B)$ be their posets of [[commutative C-star-algebra|commutative]] sub-von Neumann algebras. 

Then every [[isomorphism]] $ComSub(A) \to ComSub(B)$ of [[poset]]s comes from a unique [[Jordan algebra]] isomorphism $A_J \to B_J$. 

=--

This is the theorem in ([Harding-D&#246;ring 10](#HardingDoering)).

There is a generalization of this theorem to more general [[C-star algebras]] in ([Hamhalter 11](#Hamhalter)).


+-- {: .num_remark}
###### Remark

This is related to the [[Alfsen-Shultz theorem]], which says that two $C^*$-algebras have the 
same [[state on an operator algebra|states]] precisely if they are Jordan-isomorphic.

=--




## Related theorems


Other theorems about the foundations and [[interpretation of quantum mechanics]] include:

* [[order-theoretic structure in quantum mechanics]]

  * [[Kochen-Specker theorem]]

  * [[Alfsen-Shultz theorem]]

* [[Fell's theorem]]

* [[Gleason's theorem]]

* [[Wigner theorem]]

* [[Bell's theorem]]

* [[Bub-Clifton theorem]]

* [[Kadison-Singer problem]]

## References

The relation to Jordan algebras of $ComSub(A)$ is discussed in

* {#HardingDoering} [[Andreas Döring]], [[John Harding]],  *Abelian subalgebras and the Jordan structure of a von Neumann algebra*, Houston Journal of Mathematics **42** 2 (2016) &lbrack;[arXiv:1009.4945](http://arxiv.org/abs/1009.4945), [issue](https://www.math.uh.edu/~hjm/Vol42-2.html), [pdf](https://wordpress.nmsu.edu/hardingj/files/2019/10/2010-Abelian-subalgebras-and-the-Jordan-structure-of-von-Neumann-algebras.pdf)&rbrack;


for $A$ a [[von Neumann algebra]] and more generally for $A$ a [[C*-algebra]] in 

* {#Hamhalter} [[Jan Hamhalter]], _Isomorphisms of ordered structures of abelian $C^\ast$-subalgebras of $C^\ast$-algebras_, J. Math. Anal. Appl. 383 (2011) 391&#8211;399 ([journal](http://dx.doi.org/10.1016/j.jmaa.2011.05.035))
 

* [[Jan Hamhalter]], E. Turilova, _Structure of associative subalgebras of Jordan operator algebras_ ([arXiv:1111.7240](http://arxiv.org/abs/1111.7240))


[[!redirects Harding-Döring-Hamhalter theorem]]

