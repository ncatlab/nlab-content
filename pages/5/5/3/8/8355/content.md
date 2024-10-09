
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Elementary function arithmetic
* table of contents
{: toc}

## Idea

Elementary function arithmetic (EFA), also known as $I\Delta_0 + \exp$, is a [[first-order theory]] of [[natural numbers]], one of the weakest fragments of [[arithmetic]] strong enough to do nontrivial mathematics. It is strictly weaker than [[Peano arithmetic]].

Regarding the strength of EFA, [[Harvey Friedman]] has put forth the following "grand conjecture": 

+-- {: .standout} 
"Every theorem published in the Annals of Mathematics whose statement involves only finitary mathematical objects (i.e., what logicians call an arithmetical statement) can be proved in EFA. EFA is the weak fragment of Peano Arithmetic based on the usual quantifier-free axioms for 0, 1, +, &#215;, exp, together with the scheme of induction for all formulas in the language all of whose quantifiers are bounded."
=-- 

Here "bounded quantifier" refers to a [[quantifier]] of shape $\forall_{m \lt n}$; more formally, if a [[variable]] $n$ does not occur in a formula $\phi$, then $\forall_{m \lt n} \phi(m)$ means $\forall_m (m \lt n) \Rightarrow \phi(m)$. 

## Definition 

The [[theory|language]] of EFA is one-sorted with 

* Two constants $0, 1$ 

* Three binary function symbols $+, \cdot, \exp$ (where $\exp(x, y)$ is usually written $x^y$). 

The [[axioms]] of EFA are 

* Those of [Robinson arithmetic](http://ncatlab.org/nlab/show/second+order+arithmetic#firstorder_axioms_10) (where $s$ is translated as $1 + (-)$, i.e., as $+(1, -)$); 

* Exponentiation axioms, viz. $x^0 = 1$ and $x^y \cdot x = x^{y+1}$; 

* The [induction axiom](http://ncatlab.org/nlab/show/second+order+arithmetic#secondorder_axioms_11) for formulas all of whose quantifiers are bounded. 

## Example

For example, in order to prove in EFA that addition is [[commutative]], one can prove $(\forall a)(\forall b)(a \leq b \vee b \leq a)$ on the one hand, and, on the other hand, prove by induction over a $\Delta_0$ formula that $(\forall a)(\forall b \leq a)(a+b=b+a)$ holds.

## Related concepts

* [[Peano arithmetic]]

* [[second-order arithmetic]]


## References

* Wikipedia, _[Elementary function arithmetic](http://en.wikipedia.org/wiki/Elementary_function_arithmetic)_. 

"Grand conjectures" by Harvey Friedman may be found here: 

* Post from [[Harvey Friedman]] to FOM, April 16, 1999. ([web](http://cs.nyu.edu/pipermail/fom/1999-April/003014.html)) 

A MathOverflow discussion on Friedman's grand conjecture about EFA may be found here, 

* [Charles](http://mathoverflow.net/users/6043), _Status of Harvey Friedman's grand conjecture?_, [http://mathoverflow.net/questions/39452](http://mathoverflow.net/questions/39452) (version: 2011-03-24), ([link](http://mathoverflow.net/questions/39452/status-of-harvey-friedmans-grand-conjecture)) 

[[!redirects grand conjecture]] 
[[!redirects elementary function arithmetic]] 
[[!redirects Elementary Function Arithmetic]] 
[[!redirects EFA]] 
