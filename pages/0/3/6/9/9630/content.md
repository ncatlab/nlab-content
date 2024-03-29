
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}


## Statement 

+-- {: .num_theorem}
######Theorem 
**(Tarski-Seidenberg)**

The [[image]] of a [[semialgebraic set]] in $R^{n+1}$ under the [[projection]] [[map]] 

$$
 \pi \colon 
  R^{n+1} \to R^n: (x_1, \ldots, x_{n+1}) \mapsto (x_1, \ldots, x_n)
$$  

is also a semi-algebraic set. 

=-- 

## Commentary 

This powerful theorem is usually understood in the context of [[formal logic]] and [[model theory]], where one considers subsets of [[Euclidean space]] $\mathbb{R}^n$ that are definable by [[first-order logic|first-order logical]] [[formulas]] in the [[language]] of ordered rings. It says that the [[definable set|definable]] subsets are precisely semi-algebraic sets, i.e., sets defined by taking Boolean combinations of sets of the form 

$$\{(x_1, \ldots, x_n) \in \mathbb{R}^n: p(x_1, \ldots, x_n) \geq 0\}$$ 

where $p$ is a [[polynomial]]. 

In logic, the result is understood as connected to a [[quantifier elimination]] result. By definition, semi-algebraic sets $X$ are definable by formulas $P$ without any quantifiers. Taking an image under a projection amounts to applying an existential quantifier: 

$$\pi(X) = \pi(\{(x_1, \ldots, x_{n+1}) \in \mathbb{R}^{n+1}: P(x_1, \ldots, x_n, x_{n+1})\} = \{(x_1, \ldots, x_n) \in \mathbb{R}^n: \exists_{x_{n+1}} P(x_1, \ldots, x_n, x_{n+1})\}$$ 

and Tarski-Seidenberg allows us to replace $\exists_{x_{n+1}} P$ by some quantifier-free formula. By induction, it follows that any quantified formula may be replaced by a quantifier-free one. 

There is a host of consequences of this result, including the fact that the theory $Th(\mathbb{R})$ in this language is decidable (in particular, [[Euclidean geometry]] is decidable), and that all [[models]] of the theory of [[real-closed field]]s are [[elementary equivalence|elementarily equivalent]]. 

## Extensions 

The entire theory of [[o-minimal structure]]s can be viewed as a vast extrapolation stemming from the Tarski-Seidenberg theorem and its consequences. 

Not all the extrapolations are based on quantifier elimination, but practically all do involve some reduction of logical complexity of formulas. An example is Wilkie's theorem on the structure of the ordered exponential field $\mathbb{R}$ (in the language $(0, 1, +, \cdot, \exp, \lt)$ where $\exp$ is interpreted as the usual [[exponential function]] $\exp(x) = e^x$): 

+-- {: .num_theorem} 
###### Theorem 
**(Wilkie)** 
Any subset of $\mathbb{R}^m$ definable in the language of ordered exponential fields can be defined by means of an existential formula 

$$\exists x_{m+1}\ldots\exists x_n \, f_1(x_1,\ldots,x_n,e^{x_1},\ldots,e^{x_n})=\cdots= f_r(x_1,\ldots,x_n,e^{x_1},\ldots,e^{x_n})=0$$ 

where the $f_i$ are polynomials. 
=-- 

Here the critical point is that the _complement_ of a set defined by such an existential formula is definable by another such existential formula. This is called a [[model completeness]] result, and it implies that an alternating string of quantifiers $\forall = \neg \exists \neg, \exists$ can be eliminated in favor of just existential quantifiers at the head of a defining formula. 

+-- {: .num_remark} 
###### Remark 
It is not known whether the theory of ordered exponential fields is decidable, but it is known that such decidability follows if one assumes [[Schanuel's conjecture]]. 
=-- 

