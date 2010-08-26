## Definition 

Let $K$ be a field. A **Puiseux series** with coefficients in $K$ is a formal Laurent series 

$$f(t) = \sum_{k \geq m} a_k t^{k/r} \qquad (1)$$ 

where $r$ is a positive integer, $m$ is an integer, and each $a_k$ belongs to $K$. Somewhat more abstractly but also more meaningfully, if $\mathbb{N}_{\cdot}$ is the poset of positive integers ordered by divisibility (so that $1$ is the least element), then the field of Puiseux series is the filtered colimit of the diagram of fields 

$$F: \mathbb{N}_{\cdot} \to Field$$ 

where each $F(n)$ is the field of [[Laurent series]] $K((t))$, but where $F(m) \to F(n)$ (in case $m|n$) is the field homomorphism taking $f(t)$ to $f(t^{n/m})$. 

The field of Puiseux series carries a [[valuation ring|valuation]] whose values are in the ordered group of rationals $(\mathbb{Q}, +)$: for $f(t)$ as in (1), $v(f)$ is the least exponent $k/r$ for which $a_k \neq 0$. 

## Puiseux-Newton expansions

Puiseux series were in essence considered by [[Isaac Newton]], who developed a method of expanding algebraic functions as Puiseux series, based on an analogue of Newton's method of approximating roots. Here is a sample theorem: 

+-- {: .un_thm} 
######Theorem 
If $K$ is [[algebraically closed field|algebraically closed]] and has characteristic 0, then the field of Puiseux series over $K$ is the algebraic closure of the field of Laurent series over $K$. 
=-- 

(Proof or suitable reference to be inserted later.) 
