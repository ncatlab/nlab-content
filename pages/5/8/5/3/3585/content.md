#Contents#
* automatic table of contents goes here
{:toc}

#Idea
The theory of hyperfunctions, created by the Japanese school of [[Mikio Sato]], [[Masaki Kashiwara]] et al. is one of the many variants of the theory of [[generalized functions]]. Unlike the earlier theory of distributions of Schwarz et alt. it is not based on duals of some spaces of smooth functions but rather on boundary values of holomorphic functions. This allows usage of sheaf theory and includes Schwartz distributions as a special case. For example in Schwarz's theory apart from measures one has functions with discrete support which are linear combinations of finite derivatives of delta functions. Here one can allow things like the exponential of a differential operator applied to a delta function. So in a sense one has distributions of infinite order. 

Hyperfunctions are a very useful tool in the study of [[D-modules]], holonomic systems of differential equations, and especially some aspects of [[symplectic geometry]] and [[harmonic analysis]] that are part of [[microlocal analysis]], especially [[algebraic microlocalization]]. 

#Definition

##hyperfunctions of one variable
Let $I = (a, b) \subseteq \mathbb{R}$ be an open interval, a complex neighbourhood of $I$ is an open set $U \subset \mathbb{C}$ such that $U \bigcap \mathbb{R} = I$. For $V \subset \mathbb{C}$ open let $\mathcal{O}(V)$ be the [[sheaf]] of holomorphic functions on $V$.

The set of hyperfunctions on $I$ for a complex neighbourhood $U$ of $I$ is defined to be the quotient
$$
\mathcal{B}(I) := \frac{ \mathcal{O}(U/I) }{\mathcal{O}(U)}
$$

The set $\mathcal{B}(I)$ does not depend on the chosen complex neighbourhood $U$, which is a consequence of [[Mittag-Leffler's theorem]] in the one-dimensional case. The definition easily generalizes to open subsets of $\mathbb{R}$.

Let $U^+ := \{u \in U : \operatorname{Im}(u) \gt 0 \}$ and $U^- := \{u \in U : \operatorname{Im}(u) \lt 0 \}$, then a nontrivial hyperfunction can be described by two functions $F^+$ holomorphic on $U^+$ and $F^-$ holomorphic on $U^-$ such that there is no function $F$ holomorphic on $U$ that restricts to $F^+$ and $F^-$. In this sense hyperfunctions are "differences" of holomorphic functions on a "boundary" (we did not specify an algebraic object that contains both $F^+$ and $F^-$, so strictly speaking we cannot subtract them). 

#basic properties

##basic properties of hyperfunctions of one variable

Let $U \subseteq \mathbb{R}$ be open.

*  Let $\mathcal{A}(U)$ be the vector space of real analytic functions on $U$, then $\mathcal{B}(U)$ is a module over $\mathcal{A}(U)$.

* The sets of hyperfunctions of open subsets of $U$ form a [[flabby sheaf]] of [[vector spaces]] over $U$.

* There is a linear injection from the space of distributions $\mathcal{D}'(U)$ to the space of hyperfunctions $\mathcal{B}(U)$. The sheaf of germs of distributions is therefore a subsheaf of the sheaf of germs of hyperfunctions.

#References

* Springer Online Enc. of Math.: [hyperfunction](http://eom.springer.de/h/h048420.htm)

A gentle introduction with examples is the booklet

* K. Yosida, _Operational calculus. A theory of hyperfunctions_, Applied Mathematical Sciences, 55. Springer-Verlag, New York, 1984. x+170 pp.

* [[Mikio Sato]], _Theory of hyperfunctions I_, [pdf scan](http://repository.dl.itc.u-tokyo.ac.jp/dspace/bitstream/2261/6027/1/jfs080104.pdf)

* M. [[Kashiwara]],   T. Kawai,   T. Kimura,   "Foundation of algebraic analysis" , Princeton Univ. Press  (1986)  ((translated from the Japanese))

* Mitsuo Morimoto: _An introduction to Sato's hyperfunctions._ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0811.46034&format=complete)) 


[[!redirects hyperfunctions]]
[[!redirects Sato's hyperfunction]]
[[!redirects Sato's hyperfunctions]]