
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Definition 

Let $K$ be a [[field]]. A **Puiseux series** with [[coefficients]] in $K$ is a formal [[Laurent series]] 

$$f(t) = \sum_{k \geq m} a_k t^{k/r} \qquad (1)$$ 

where $r$ is a positive [[integer]], $m$ is an integer, and each $a_k$ belongs to $K$. Somewhat more abstractly but also more meaningfully, if $\mathbb{N}_{\cdot}$ is the [[poset]] of positive integers ordered by divisibility (so that $1$ is the least element), then the field of Puiseux series is the [[filtered colimit]] of the diagram of fields 

$$F: \mathbb{N}_{\cdot} \to Field$$ 

where each $F(n)$ is the field of [[Laurent series]] $K((t))$, but where $F(m) \to F(n)$ (in case $m|n$) is the field [[homomorphism]] taking $f(t)$ to $f(t^{n/m})$. 

The field of Puiseux series carries a [[valuation ring|valuation]] whose values are in the ordered group of [[rational number|rationals]] $(\mathbb{Q}, +)$: for $f(t)$ as in (1), $v(f)$ is the least exponent $k/r$ for which $a_k \neq 0$. 

## Puiseux-Newton expansions

Puiseux series were in essence considered by [[Isaac Newton]], who developed a method of expanding algebraic functions as Puiseux series, based on an analogue of [[Newton's method]] of approximating roots. Here is a sample theorem: 

+-- {: .num_theorem #Puiseux} 
###### Theorem 
If $K$ is [[algebraically closed field|algebraically closed]] and has [[characteristic]] 0, then the field of Puiseux series over $K$ is the algebraic closure of the field of Laurent series over $K$. 
=-- 

+-- {: .proof} 
###### Proof (sketch) 
It is enough to show that every degree $n$ extension $E$ of the field of Laurent series $K((x))$ is of the form $K((x^{1/n}))$. For this, it suffices that the integral closure $B$ of $K[ [x] ]$ in $E$ be of the form $K[ [x^{1/n}] ]$. 

Generally speaking, let $A$ be a complete DVR ([[valuation ring|discrete valuation ring]]) with maximal ideal $\mathfrak{m}_A$ and residue class field $k_A$, and let $F$ be its field of fractions. Let $E$ be a degree $n$ extension of $F$, and let $B$ be the integral closure of $A$ in $E$. Then $B$ is also a complete DVR. We may write the ideal $\mathfrak{m}_A B$ of $B$ as $\mathfrak{m}_B^e$ where $e$ is the _ramification index_, and we have  

$$n = deg_F E = rank_A B = rank_{A/\mathfrak{m}_A} B/\mathfrak{m}_A B = dim_{k_A} B/\mathfrak{m}_B^e = e \cdot dim_{k_A} k_B$$ 

where the last equation holds because $\mathfrak{m}_B^i/\mathfrak{m}_B^{i+1} \cong k_B$ as $k_B$-modules and therefore also as $k_A$-modules. In the case $A = K[ [x] ]$ where $k_A = K$, we have that $dim_{k_A} k_B = 1$ since $K$ is algebraically closed, and therefore $e = n$. In other words, $(x)B = \mathfrak{m}_B^n$, so we can write $x = u \pi^n$ where $\pi$ generates the maximal ideal of $B$ and $u$ is a unit of $B$. 

The residue class $\bar{u} \in K$ has an $n^{th}$ root (again by algebraic closure); in fact a simple root since $char(K) = 0$. By [[Hensel's lemma]], this lifts to an $n^{th}$ root of $u$ in $B$. The element $u^{1/n} \pi$ is thus an $n^{th}$ root of $x$, and is a generator of the maximal ideal of $B$. Writing this element as $y = x^{1/n}$, the ring $K[ [y] ] = A[x^{1/n}] \hookrightarrow B$ is an $A$-submodule of full rank $n$ and integrally closed (being abstractly isomorphic to $A$, which is [[integral closure|integrally closed]] because it's a [[principal ideal domain]] and therefore a [[unique factorization domain]]), so that $K[ [y] ] = B$, as was to be shown. 
=-- 

+-- {: .un_example} 
###### Example 
(Intend to solve for $y$ in $y^3 - x y + 1 = 0$ as a Puiseux series in $x$.) 
=-- 

## Related pages

Other rings of generalized power series include:

* [[Novikov field]]
* [[Hahn series]]
* [[Ribenboim power series]]

Hahn series are a special kind of Ribenboim power series, but Puiseux and Novikov series are not.  However, they are all instances of the linearization of a [[finiteness space]].

## References

* wikipedia [Puiseux series](http://en.wikipedia.org/wiki/Puiseux_series)

The sketched proof of theorem \ref{Puiseux} was extracted from notes on a seminar by Boyarchenko on local class field theory: 

* Mitya Boyarchenko, Kottwitz Seminar Lectures, (U. Michigan, Winter 2011). ([pdf](http://www.math.lsa.umich.edu/seminars/kottwitz/HieuNgoLocalCFT.pdf)) 

and the reader may refer to the classic text by Serre for a fuller treatment: 

* Jean-Pierre Serre, _Local Fields_ (trans. Marvin J. Greenberg), Graduate Texts in Math. 67, Springer 1980. 

For a noncommutative generalization see

* D. Grigoriev, _Analogue of Newton-Puiseux series for non-holonomic D-modules and factoring_, Moscow Math. J. __9__, 2009, 775--800, [pdf](http://logic.pdmi.ras.ru/~grigorev/pub/puiseux_journal.pdf); MPIM2008-6, [pdf](http://www.mpim-bonn.mpg.de/preblob/3537)

Other references

* Jan Kiwi, _Puiseux series dynamics of Quadratic rational maps_,  [arxiv/1106.0059](http://arxiv.org/abs/1106.0059)
* Luis Felipe Tabera, _On real tropical bases and real tropical discriminants_, [arxiv/1311.2211](http://arxiv.org/abs/1311.2211)

> We explore the concept of real tropical basis of an ideal in the field of real Puiseux series. We show explicit tropical bases of zero-dimensional real radical ideals, linear ideals and hypersurfaces coming from combinatorial patchworking. But we also show that there exist real radical ideals that do not admit a tropical basis. As an application, we show how to compute the set of singular points of a real tropical hypersurface. i.e. we compute the real tropical discriminant. 

* Evelia Garc&#237;a Barroso, Pedro Daniel Gonz&#225;lez P&#233;rez, Patrick Popescu-Pampu, _Variations on inversion theorems for Newton-Puiseux series_, [arxiv/1606.08029](http://arxiv.org/abs/1606.08029)

[[!redirects Newton-Puiseux series]]
