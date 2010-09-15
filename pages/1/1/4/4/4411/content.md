#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **valuation ring** is a commutative [[integral domain]] $O$ such that, for every nonzero element $x$ in its [[field of fractions]] $K$, either $x \in O$ or $x^{-1} \in O$. 

+-- {: .un_prop}
######Proposition 
A valuation ring $O$ is a [[local ring]]. 
=-- 

+-- {: .proof} 
######Proof 
Suppose $x$, $y$ are nonzero non-invertible elements of $O$. Either $x/y$ or $y/x$ belongs to $O$, say $x/y$. Then $(x+y)/y$ belongs to $O$ as well. If $x+y$ were a unit of $O$, it would follow that $1/y$ belongs to $O$, i.e., both $y$ and $1/y$ belong to $O$, so that $y$ is a unit of $O$, contradiction. It follows that non-unit elements of $O$ are closed under addition. It is also clear that if $x$ is a non-unit element of $O$ and $y$ is any element of $O$, then $x y$ is a non-unit element of $O$. Therefore the non-units form an ideal of $O$, clearly the unique maximal ideal of $O$. 
=--

+-- {: .un_prop}
######Proposition
A valuation ring $O$ is integrally closed in its field of fractions $F$. 
=-- 

+-- {: .proof} 
######Proof 
Suppose $x \in F$ satisfies an equation $x^n + a_{n-1}x^{n-1} + \ldots + a_0 = 0$ where the $a_i$ belong to $O$. Either $x$ or $1/x$ belongs to $O$, and if $1/x$ belongs to $O$, then so does $x$ because 
$$x = a_{n-1}x^{-1} + a_{n-1}x^{-2} + \ldots + a_0 x^{-n}$$ 
and this completes the proof. 
=--

### Example: germs of definable functions

Local rings often arise as stalks of sheaves of real or complex-valued functions, and similarly, some of the more interesting examples of valuation rings arise by considering germs of functions at an "ideal" point, for example at an ultrafilter or infinite point where the functions are not formally defined. Examples such as these are often rich sources of rings and fields with _infinitesimal elements_. The following example should give the flavor of this phenomenon. 

Consider the class of all functions $\mathbb{R} \to \mathbb{R}$ which can be defined by a first-order formula, starting with the basic operations 
$+, -, \cdot, \exp$, any constant $a \in \mathbb{R}$, and the relations $\lt$ and $=$. This is an enormous class of functions: it includes the [[logarithm]] function and any function which can be built from [[polynomials]], [[exponential map|exponentials]], and logarithms using the four basic arithmetic operations and composition, and also implicitly defined functions such as: 

$$f(x) = max \{y: y^5 - (e^{e^x - (\log x)^2 + 1/x})y^2 + \log(1 + x^{\sqrt{2}}))y - 17 = 0\}$$ 

and many, many more. Of interest are _rates of growth_ (cf. [[O notation]]) of these functions, or, at an even more refined level, the precise ordering of these functions $f(x) \leq g(x)$ when $x$ is large. A quite remarkable and deep fact is the following: 

+-- {: .un_thm} 
######Theorem 
Any such definable function $f(x)$ is either positive for all sufficiently large $x$, $0$ for all sufficiently large $x$, or negative for all sufficiently large $x$. 
=-- 

This theorem implies that the germs at infinity of such functions ($\sim$-equivalence classes of functions where $f \sim g$ if $f(x) = g(x)$ for all sufficiently large $x$) form a totally [[ordered field]], in fact a [[real closed field]]. The real numbers are embedded in this field as germs of constant functions, but lying between ordinary real numbers are other "numbers" infinitesimally close to reals, such as $2 - [1/x]$, $1 + [1/\log \log(x)]$, as well as infinite numbers such as $[e^x]$. 

Sitting inside this field $Germ(\mathbb{R}_{exp})$ is the valuation ring of germs of bounded definable functions, in other words the ring of finite "numbers", which contains infinitesimals of incredibly rich variety.  

Such examples are close in spirit to [[hyperreal number]]s, which form a considerably larger real closed field. In this case, the procedure is similar, except that one takes germs of _all_ functions $\mathbb{N} \to \mathbb{R}$ in the neighborhood of a non-principal ultrafilter on $\mathbb{N}$, which can be considered an ideal point at "infinity". This is called an [[ultrapower]] of the standard real numbers. Again the finite hyperreals form a valuation ring sitting inside. 

## The valuation function 

The nonzero elements of $K$ may be partially ordered as follows: write $x \leq y$ if $x/y$ belongs to $O$. For any two nonzero elements $x$, $y$ of $K$, exactly one of the following conditions holds: 

* $x/y$ is a non-unit of $O$; 

* $x/y$ is a unit of $O$: $x/y$ and $y/x$ belong to $O$; 

* $y/x$ is a non-unit of $O$. 

We call this the _trichotomy law_. Thus, if we write $O^*$ for the units of $R$, it follows from trichotomy that the partial order on $K^*$ descends to a [[total order]] on the quotient group $G = K^*/O^*$. This totally ordered group is called the **value group** of the valuation ring $O$. When the value group is isomorphic to $\mathbb{Z}$, the ring $O$ is called a **discrete valuation ring**. Many local rings which arise in practice, for example localizations of rings of [[algebraic integer]]s $O$ with respect to a prime ideal $\mathcal{p}$, or their completions as rings of $\mathcal{p}$-adic integers $O_{(\mathcal{p})}$, are discrete valuation rings. 

We may then define a **valuation** function 

$$v: K \to K^*/O^* \cup \{0\}$$ 

where $v(x)$ is the coset $x O^*$ if $x \in K^*$, and $v(0) = 0$. The codomain becomes a totally ordered monoid if $0$ is regarded as the bottom element and is _absorbent_ ($0 x = 0$ for all $x$). This function satisfies the following conditions: 

1. $v(x) = 0$ if and only if $x = 0$; 

1. $v(x y) = v(x)v(y)$; 

1. $v(x + y) \leq \max \{v(x), v(y)\}$ 

1. $v$ is surjective. 

### Example: rates of growth

Let us return to our earlier example of a valuation ring $O$, consisting of germs of bounded functions which are first-order definable in the theory of the reals as ordered field with exponentiation. Two "numbers" $[f]$, $[g]$ have the same coset, $[f]O^* = [g]O^*$, if both $[f/g]$ and $[g/f]$ are bounded. But this is precisely to say $f$ is $O(g)$ and $g$ is $O(f)$. 

Thus, the elements of the value group in this case can be described as the various "rates of growth" of definable functions. The order relation is that $[f]O^* \leq [g]O^*$ if $f$ is $O(g)$. Thus the classical analysis notion of 'O notation' fits within the theory of valuation rings. 

Rates of growth, as elements of the value group $K^*/O^*$, can also be regarded as "numbers" containing infinitesimal and infinite quantities. Thus, ordinary real numbers $a$ would correspond to rates of growth of power functions $x^a$, whereas the rate of growth $\log x$ is infinitesimal and the rate of growth of $e^x$ is infinite. The fact that rates of growth of definable functions are totally ordered is essentially due to G.H. Hardy, and in his honor, fields of germs of definable functions are frequently called "Hardy fields". 

* Hardy actually studied the class of functions definable from polynomials, exponential, and logarithmic functions using the four arithmetic operations and composition. This of course is a small subclass of the definable functions considered above, but contains all functions likely to be of interest in analytic number theory (for example). 

## Valuation rings from valuation functions 

Quite generally, we may define a **valuation** on a field $K$ to be a function 

$$v: K \to G \cup \{0\}$$ 

(where $G$ is a totally ordered group, extended to a totally ordered monoid $G \cup \{0\}$ as above), satisfying conditions 1 - 4 listed above. Two valuations $v$, $v'$ are **equivalent** if there is an isomorphism 

$$\phi: G \cup \{0\} \to G' \cup \{0}$$ 

of totally ordered monoids such that $v' = \phi \circ v$. In fact, valuations $v$ may be [[preorder|preordered]]: if we regard $v$ as a special sort of group homomorphism $v: K^* \to G$, then define $v \leq v'$ if there is a surjective homomorphism of ordered groups $\phi: G \to G'$ such that $v' = \phi \circ v$. 

From the data of a valuation on $K$, we may construct a valuation ring $O_v$ inside $K$: 

$$O_v = \{x \in K: v(x) \leq 1\}$$ 

where $1$ is the identity element of $G$. (The fact that $O_v$ is a ring follows straightforwardly from the axioms 1 - 3, and that $O_v$ is a valuation ring follows from the fact that $G$ is totally ordered.) 

In summary, we have the following result whose proof is straightforward: 

+-- {: .un_prop}
######Proposition 
There is a natural bijective correspondence between equivalence classes of valuations on $K$ and valuation rings in $K$. 
=-- 

To express the naturality more precisely: there are two functors 

$$V: Field^{op} \to Pos, \qquad V': Field^{op} \to Pos$$ 

from fields to posets. Here $V$ assigns to a field $K$ the poset of equivalence classes of valuations on $K$, where the partial order is inherited from the preorder described above; $V'$ assigns to a field $K$ the poset of valuation rings inside $K$, ordered by inclusion. If $i: K \to K'$ is a field homomorphism, then $V'(i): V'(K') \to V'(K)$ takes a valuation ring $O' \subseteq K$ to the valuation ring $i^{-1}(O') \subseteq K$, and $V(i)$ is defined similarly. The proposition asserts that the functors $V$, $V'$ are naturally isomorphic. We freely conflate them, denoting either functor as $Val: Field^{op} \to Pos$. 

### Example: compact Riemann surfaces 

One of the first lessons from Mumford's famous Red Book is the "amazing" correspondence between 

* Fields which arise as finite algebraic extensions of the field of rational functions $\mathbb{C}(x)$; 

* Compact Riemann surfaces (compact complex manifolds of complex dimension 1, or "curves"). 

The correspondence goes roughly as follows: to each compact Riemann surface $C$, one may associate the field of meromorphic functions $Mer(C)$, or holomorphic functions $C \to \mathbb{P}^1(\mathbb{C})$. Moreover, for each such $C$, there exists a finite branched covering 

$$\phi: C \to \mathbb{P}^1(\mathbb{C})$$ 

which contravariantly induces a field homomorphism $\mathbb{C}(x) \to Mer(C)$. 

In the other direction, to each field $K$ of transcendence degree 1 over $\mathbb{C}$, there is a Riemann surface whose points may be identified with valuation rings in $K$. (More precisely, with the _discrete_ valuation rings in $K$. All valuation rings of $K$ are discrete except for $K$ itself, which plays the role of a "generic point".) 

Much more could be added here... 

## Generalized power series 

There is a very general construction which takes as input an arbitrary field $k$ and a totally ordered abelian group $G$, and produces as output a valuation ring whose value group is naturally identified with $G$. This is the ring of _Hahn series_. 

+-- {: .un_def}
######Definition 
The ring of **Hahn series** with value group $G$, denoted $k[x^G]$, is the ring of functions $f: G \to k$ such that $\{x \in G: f(x) \neq 0\}$ is a well-ordered subset of $G$. Addition is defined pointwise, and multiplication is defined by convolution product: 
$$(f \cdot g)(x) = \sum_{y+z = x in G} f(y)g(z)$$
The **valuation** $v(f)$ is the least $x \in G$ for which $f(x) \neq 0$. 
=-- 

We obtain a valuation ring from this construction since, as noted above, a valuation ring is essentially the same as a valuation on a field.

+-- {: .un_thm}
######Theorem 
The ring $k[x^G]$ is a field. If $k$ is algebraically closed, then $k[x^G]$ is algebraically closed provided that $G$ is [[divisible group|divisible]]. 
=-- 

As a corollary, if $G$ is divisible, $k[x^G]$ is real closed if $k$ is real closed. This is because the adjunction of a square root of $-1$ would make $k[x^G]$ algebraically closed, since this gives the same result as constructing the Hahn series over the algebraically closed field $k[\sqrt{-1}]$. 
