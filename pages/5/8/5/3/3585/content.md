#Contents#
* automatic table of contents goes here
{:toc}

##Idea
The theory of hyperfunctions, created by the Japanese school of [[Mikio Sato]], [[Masaki Kashiwara]] et al. is one of the many variants of the theory of [[generalized functions]]. Unlike the earlier theory of distributions of Schwarz et alt. it is not based on duals of some spaces of smooth functions but rather on boundary values of holomorphic functions. This allows usage of sheaf theory and includes Schwartz distributions as a special case. For example in Schwarz's theory apart from measures one has functions with discrete support which are linear combinations of finite derivatives of delta functions. Here one can allow things like the exponential of a differential operator applied to a delta function. So in a sense one has distributions of infinite order. 

Hyperfunctions are a very useful tool in the study of [[D-modules]], holonomic systems of differential equations, and especially some aspects of [[symplectic geometry]] and [[harmonic analysis]] that are part of [[microlocal analysis]], especially [[algebraic microlocalization]]. 

The theory of hyperfunctions of one variable is considerably easier than the one for multiple variables, for this reason we will split the exposition to handle the one dimensional case first, and then generalize to multiple dimensions.

##Definition

###Hyperfunctions of One Variable
Let $I = (a, b) \subseteq \mathbb{R}$ be an open interval, a complex neighbourhood of $I$ is an open set $U \subset \mathbb{C}$ such that $U \bigcap \mathbb{R} = I$. For $V \subset \mathbb{C}$ open let $\mathcal{O}(V)$ be the [[sheaf]] of holomorphic functions on $V$.

+-- {: .un_def}
###### Definition
The set of hyperfunctions on $I$ for a complex neighbourhood $U$ of $I$ is defined to be the quotient
$$
\mathcal{B}(I) := \frac{ \mathcal{O}(U/I) }{\mathcal{O}(U)}
$$
=--

The set $\mathcal{B}(I)$ does not depend on the chosen complex neighbourhood $U$, which is a consequence of [[Mittag-Leffler's theorem]] in the one-dimensional case. The definition easily generalizes to open subsets of $\mathbb{R}$.

Let $U^+ := \{u \in U : \operatorname{Im}(u) \gt 0 \}$ and $U^- := \{u \in U : \operatorname{Im}(u) \lt 0 \}$, then a nontrivial hyperfunction can be described by two functions $F^+$ holomorphic on $U^+$ and $F^-$ holomorphic on $U^-$ such that there is no function $F$ holomorphic on $U$ that restricts to $F^+$ and $F^-$. In this sense hyperfunctions are "differences" of holomorphic functions on a "boundary" (we did not specify an algebraic object that contains both $F^+$ and $F^-$, so strictly speaking we cannot subtract them). 

In the following we will often write $F = (F^+, F^-)$ for a hyperfunction $F$, with $(F^+, F^-)$ being a representative of the equivalence class that is $F$ in $\mathcal{B}$ on some complex neighbourhood. If the algebraic expression of $F^+$ and $F^-$ coincides we can further simplify the notation and simply write $[F]$.

Example: The $\delta$ distribution can be represented by $\delta = [\frac{i}{2 \pi z}]$. We can prove that this equality is simply a restatement of Cauchy's integral formula after we define the concept of integration for a compactly supported hyperfunction below. 

##Basic Properties and Definitions

###Hyperfunctions of One Variable

Let $U \subseteq \mathbb{R}$ be open.

+-- {: .un_theorem}
###### Theorem
**(hyperfunctions are a module over analytic functions)**
Let $\mathcal{A}(U)$ be the algebra space of real analytic functions on $U$, then $\mathcal{B}(U)$ is a module over $\mathcal{A}(U)$.
=--

In fact every real analytic function $f$ is naturally an element of $\mathcal{B}(U)$ represented by (f, 0) or (0, -f) on a complex neighbourhood. Given any hyperfunction $F = (F^+, F^-)$ we can define the product by $f F := (f F^+, F^-) = (F^+, -f F^-)$ which can be shown to be independent of the various choices involved (representation of $F$, complex neighbourhood of $U$, domain of the extension of the domain of $f$).


+-- {: .un_theorem}
###### Theorem
**(hyperfunctions form a [[flabby sheaf]])**
The sets of hyperfunctions of open subsets of $U$ form a [[flabby sheaf]] of [[vector spaces]] over $U$.
=--

+-- {: .un_theorem}
###### Theorem
**(distributions are a subsheaf)**
There is a linear injection from the space of distributions $\mathcal{D}'(U)$ to the space of hyperfunctions $\mathcal{B}(U)$. The sheaf of germs of distributions is therefore a subsheaf of the sheaf of germs of hyperfunctions.
=--

####Support
In general we cannot speak of the value of a hyperfunction at a certain point, much like we cannot speak of the value of a distribution at a certain point. We say that a hyperfunction $F$ vanishes on an open subset $U'$ of $U$ if it coincides with the zero hyperfunction, which is of course equivalent to stating that there is a representation of $F = (F^+, F^-)$ such that the boundary values of $F^+$ and $F^-$ coincide on $U'$ and therefore define a real analytic function on $U'$. 

+-- {: .un_def}
###### Definition
The **support** of a hyperfunction $F$ is the complement of the largest open subset of $U$ on which $F$ vanishes in the sense described above.
=-- 

For any compact $K$ we will denote by $\mathcal{B}_K$ all hyperfunctions whose support is contained in $K$.

####Integration for Compactly Supported Hyperfunctions
Since we defined hyperfunctions for open subsets only, we do not yet know anything about hyperfunctions $\mathcal{B}_K$ with support in a compact subset $K$, but the following theorem tells us that there is no difference:

+-- {: .un_theorem}
###### Theorem
**(characterization of compactly supported hyperfunctions)**
Let $\mathcal{B}_K$ be all hyperfunctions with support contained in $K \subset \mathbb{R}$ compact and $V$ be any complex neighbourhood of $K$. Then we have the following isomorphism:
$$
\mathcal{B}_K \cong \frac{ \mathcal{O}(V/K) }{\mathcal{O}(V)}
$$
=--

Let $a, b \in \mathbb{R}$ with $a \leq b$ and suppose that $F$ is a hyperfunction that is analytical in $a$ and $b$. Then we can choose a complex neighbourhood $V$ of $[a, b]$, paths $\tau^+$ in $V^+$  and $\tau^-$ in $V^-$ from a to b and a representation of $F = (F^+, F^-)$ such that we can define the integral

$$
\int_a^b F(x) dx := \int_{\tau^+} F^+ (z) dz - \int_{\tau^-} F^- (z) dz
$$

independently of all the arbitrary choices we made, thanks to the holomorphy of the functions on the right side (and Cauchy's integral formula for holomorphic functions, of course).

####Example of a Hyperfunction that is not a Distribution
Warning: As of this moment this paragraph consists of some handwaving.

A well known structure theorem in the theory of distributions says that every distribution whose support consists of one single point $P$ is in fact a finite linear combination of distributional derivatives of the $\delta$ function at $P$.

As an example of a hyperfunction that is not a distribution we therefore have $F = [\exp{\frac{1}{z}}]$ with $\supp{F} = \{ 0 \}$. 

Using the representation of the $\delta$ distribution, we see that
$$
\delta^{(n)}(x) = [\frac{(-1)^{n+1} n!}{2 \pi i} \frac{1}{z^{n+1}}]
$$

Using this representation, for any real analytic test function $a$ we see that the following identity holds, which motivates the use of the $\delta$ as in distribution theory:
$$
\int a(x) \delta^{n}(x) dx = a^{(n)} (0)
$$

Comparing the Laurent series of $F$ with the representation of $\delta^{(n)}$ we get
$$
[\exp{\frac{1}{z}}] = [1 + 2 \pi i  \sum_{n=0}^{\infty}  \frac{1}{n! (n-1)!} \delta^{(n)}(z)]
$$
with $(-1)! := 1$.
Given the structure theorem about distributions cited above, we see that the hyperfunction $[\exp{\frac{1}{z}}]$ cannot be a distribution. There is an analog structure theorem for hyperfunctions, however:

+-- {: .un_theorem}
###### Theorem
**(structure of hyperfunctions supported at a single point)**
Let $F$ be a hyperfunction supported at the origin, then $F$ has a representation as
$$
       F(x) = [ \sum_{n=0}^{\infty} b_n \delta^{(n)} (x)]
$$
where the coefficients satisfy 
$$
\lim_{n \to \infty} \sqrt{|b_n n!|} = 0
$$
=--

####Topology and Duality for Compactly Supported Hyperfunctions
We can introduce a canonical topology on the space $\mathcal{B}_K$ of hyperfunctions with support in a compact $K$ and show that the topological dual is the space $\mathcal{A}_K$ of germs of real analytical functions, that is the inductive limit of the spaces of holomorphic functions on a cofinal set of complex neighbourhoods of $K$, and vice versa. 

The algebraic statement is known as **K&#246;the's theorem**. 

This will also hint at the fact that we will not be able to introduce a topology on $\mathcal{B}(\mathbb{R})$ that resembles the situation in the theory of distributions, since its dual space would be something like "the space of compactly supported real analytic functions".

...

###Hyperfunctions of Multiple Variables

##Main Theoretical Results
...

###Hyperfunctions of One Variable
One striking example of the use of hyperfunctions in the theory of differential equations with real analytic coefficients is this result due to Sato:

Let $U \subseteq \mathbb{R}$ be open and $P$ be a linear, finite order differential operator with real analytic coefficients defined on $U$:
$$
       P(x, \frac{d}{dx}) = \sum_{i=0}^n a(x) (\frac{d}{dx})^{i}
$$
with $a_n \neq 0$.

+-- {: .un_theorem}
###### Theorem
**(solvability of differential equations)**
For every $f \in \mathcal{B}(U)$ there is a solution $u \in \mathcal{B}(U)$ of the equation $P u = f$. Every such solution can be extended to an open set $V \supset U$ iff the coefficients $a_i$ and $f$ can be extended to $V$.
=--

Briefly: $P$ is surjective on hyperfunctions.

Two related results are:

+-- {: .un_theorem}
###### Theorem
$P$ is a sheaf endomorphismus, both of the sheaf of real analytic functions and of the sheaf of hyperfunctions.
=--

+-- {: .un_theorem}
###### Theorem
$P$ does not enlarge the support of hyperfunctions.
=--

###Hyperfunctions of Multiple Variables
...

##Singularities and Microfunctions
...

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