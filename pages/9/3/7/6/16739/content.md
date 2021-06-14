
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Idea

A [[Heyting algebra]] is called a **De Morgan Heyting algebra** if it satisfies the [[De Morgan laws]], which may be considered a weak form of the [[law of excluded middle]].  The corresponding [[logic]] is an interesting intermediate logic between [[intuitionistic logic]] and [[classical logic]].

De Morgan Heyting algebras are also known as **Stone algebras** or **Stone lattices**.  They are also often called simply **de Morgan algebras**, although that clashes with a different notion; see [[De Morgan algebra]].


## Definition

A [[Heyting algebra]] $M$ that satisfies the following equivalent conditions is called a _De Morgan Heyting algebra_:

1. For all $a,b \in M$: $\not(a\wedge b) =\not a\vee\not b$. (second **[[De Morgan law]]**)

2. For all $a\in M$: $\not a\vee\not\not a=\top$.

3. For all $a,b\in M$: $\not\not (a\vee b) =\not\not a\vee \not\not b$.

+-- {: .proof} 
###### Proof of equivalence 
(2. implies 1.) First, it is automatic that $\neg a \vee \neg b \leq \neg(a \wedge b)$. Now, in a distributive lattice such as a Heyting algebra, if $x \wedge y = \bot$ and $x \vee z = \top$, then $y \leq z$. Putting $x = \neg \neg a \wedge \neg \neg b$ and $y = \neg(a \wedge b)$ and $z = \neg a \vee \neg b$, we check 
$$\neg\neg a \wedge \neg\neg b \wedge \neg(a \wedge b) = \neg\neg (a \wedge b) \wedge \neg(a \wedge b) = \bot$$ 
(since $\neg\neg$ preserves meets; see [[Heyting algebra]]) and 
$$(\neg\neg a \wedge \neg\neg b) \vee \neg a \vee \neg b = (\neg \neg a \vee \neg a \vee \neg b) \wedge (\neg\neg b \vee \neg a \vee \neg b) = (\top \vee \neg b) \wedge (\neg a \vee \top) = \top \wedge \top = \top$$ 
whence $\neg(a \wedge b) \leq \neg a \vee \neg b$ follows. 

(1. implies 3.) Given that $\neg(x \wedge y) = \neg x \vee \neg y$ for all $x, y$, put $x = \neg a$ and $y = \neg b$. Then 
$$\neg\neg(a \vee b) = \neg(\neg a \wedge \neg b) = \neg(x \wedge y) = \neg x \vee \neg y = \neg\neg a \vee \neg\neg b$$ 
as desired. 

(3. implies 2.) We have $\neg a = \neg\neg\neg a$, and so we may calculate 
$$\neg a \vee \neg\neg a = \neg\neg\neg a \vee \neg\neg a = \neg\neg(\neg a \vee a) = \neg(\neg \neg a \wedge \neg a) = \neg(\bot) = \top$$ 
as desired. 
=-- 


### Remark

The dual _first_ De Morgan law $\not (a\vee b) = \not a\wedge\not b$ is valid in every Heyting algebra.


## Examples

* Every [[Boolean algebra]] is a De Morgan Heyting algebra.
* The [[lattice of open subsets]] of the [[Sierpinski space]] is a De Morgan Heyting algebra (assuming a classical metalogic).
* The [[subobject classifier]] in any [[topos]] satisfying the [[ultrafilter principle]] is a De Morgan Heyting algebra. 

## Related entries

* [[De Morgan topos]]
* [[De Morganization]]
* [[Ore condition]]
* [[Heyting algebra]]
* [[co-Heyting algebra]]
* [[Boolean algebra]]
* [[ultrafilter principle]]

## References

* [[Francis Borceux]], _Handbook of Categorical Algebra vol.3_ , Cambridge UP 1994. (sections 1.2, 7.3)

* K. B. Lee, _Equational Classes of Distributed Pseudo-Complemented Lattices_ , Can. J. Math. **22** (1970) pp.881-891. ([pdf](http://cms.math.ca/openaccess/cjm/v22/cjm1970v22.0881-0891.pdf))

* M. E. Szabo, _Categorical De Morgan Laws_ , Alg. Universalis **12** (1981) pp.93-102.


[[!redirects De Morgan Heyting algebra]]
[[!redirects de Morgan Heyting algebra]]
[[!redirects de morgan Heyting algebra]]
[[!redirects De Morgan Heyting algebras]]
[[!redirects de Morgan Heyting algebras]]
[[!redirects de morgan Heyting algebras]]

[[!redirects Stone lattice]]
[[!redirects Stone lattices]]
[[!redirects Stone algebra]]
[[!redirects Stone algebras]]
