

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The original "Peano (space-filling) curve" is a _[[surjective]]_ [[continuous function]] $I \to I^2$, from the [[closed interval]] $I = [0, 1]$ to the [[product space|product]] with itself, the [[square]]. The existence of such an entity (due to Peano) came as a surprise. 

One may characterize exactly which [[Hausdorff spaces]] arise as the continuous [[images]] of a unit interval. These are called *Peano spaces*. 

One can similarly show that there is a continuous surjection $\mathbb{R}^1 \to \mathbb{R}^2$ from the [[real line]] to the [[plane]] (both regarded as [[Euclidean spaces]] equipped with their [[metric topology]]), and similarly characterize which spaces arise as continuous images of the real line. These are sometimes called *$\sigma$-Peano spaces*. 

Notice that, while of course there is also an injection $\mathbb{R} \to \mathbb{R}^2$, there is _no_ [[homeomorphism]] between these two spaces, or generally between [[Euclidean spaces]] of differing [[dimension]]. This is the statement of _[[topological invariance of dimension]]_.

## Construction 

There are many constructions of space-filling curves, but one of the quickest is due to Lebesgue and is closely connected with the Cantor-Lebesgue function. 

[[Cantor space]] (following the "middle thirds" construction) can be described as the subspace $C$ of $[0, 1]$ consisting of points whose base-$3$ representation $.a_1 a_2 a_3 \ldots = \sum_{i=1}^{\infty} \frac{a_i}{3^i}$ has $a_i \in \{0, 2\}$ for all $i$ (no $1$\'s). Define a function $\phi: C \to I$ by 

$$\phi\left(\sum_{i=1}^\infty \frac{a_i}{3^i}\right) = \sum_{i=1}^\infty \frac{a_i/2}{2^i}$$ 

(i.e., replace $2$'s in the base $3$ representation by $1$'s and reinterpret the sequence as representing a number in base $2$). Notice that $\phi$ maps the two endpoints of any one of the open intervals removed during the middle-thirds construction to the same point, e.g., for the first middle third $(\frac1{3}, \frac{2}{3})$ we have 

$$\phi(.02222222\ldots_3) = .01111111\ldots_2 = 10000000\ldots_2 = \phi(.20000000\ldots_3).$$ 

In any case, it is very easy to see that $\phi: C \to I$ is a continuous surjective map. 

Now: $C$ is homeomorphic to the [[product space]] $2^\mathbb{N}$, a countable product of copies of the [[discrete space]] $2 = \{0, 1\}$. Of course we also have a bijection $\mathbb{N} \cong \mathbb{N} + \mathbb{N}$, inducing a homeomorphism 

$$2^\mathbb{N} \cong 2^{\mathbb{N} + \mathbb{N}} \cong 2^\mathbb{N} \times 2^\mathbb{N}$$ 

and hence a "pairing function" $pair: C \cong C \times C$ that is a homeomorphism (see [[Jonsson-Tarski algebra]]). We use this to construct a continuous surjection 

$$C \stackrel{pair}{\to} C \times C \stackrel{\phi \times \phi}{\to} I \times I,$$ 

denoted say $g: C \to I \times I$, and Lebesgue's idea is to extend $g$ to a continuous function $f: I \to I \times I$ by linear interpolation: if $x \in I$ belongs to one of the open intervals $(a, b)$ removed during the middle thirds construction, say $x = t a + (1 - t)b$ for some $t \in (0, 1)$, then define 

$$f(x) = t g(a) + (1 - t)g(b).$$ 

+-- {: .num_prop} 
###### Proposition 
The function $f: I \to I \times I$ thus defined is surjective and continuous. 
=-- 

+-- {: .proof} 
###### Proof 
Surjectivity follows from the fact that its restriction $g: C \to I \times I$ is surjective. 

Obviously for each open interval removed in the middle thirds construction, $f$ is continuous at each [[interior point]] $x$ (being locally an [[affine map]] there), and so it remains to check that $f$ is continuous at each point of $C$. So let $a \in C$, and let us prove that $f(x)$ approaches $f(a)$ as $x$ approaches $a$ from the right; a similar argument will prove continuity from the left. This is obvious if $a$ is the left endpoint of one of the removed open intervals, again because $f$ is affine to the immediate right of $a$. If not, then $a$ is a limit from the right of points of $C$. Now $g: C \to I \times I$ is continuous, so given $\epsilon \gt 0$ there exists $\delta \gt 0$ such that ${|g(x) - g(a)|} \lt \epsilon$ whenever $x \in [a, a + \delta)$ and $x \in C$. What if $x \notin C$? Shrink $\delta$ a little more, and assume $a + \delta$ is a right-hand endpoint of a removed open interval, and consider the case where $x \in [a, a + \delta)$ and $x \notin C$, say $x \in (b, c)$ where $(b, c)$ is a removed open interval and $b, c \in (a, a + \delta]$. Then we get the same $\epsilon$-bound as before: putting $x = t b + (1 - t)c$, we have 

$$\array{
{|f(x) - f(a)|} & = & {\left|[t g(b) + (1 - t)g(c)] - g(a)\right|} \\ 
 & = & {\left|t(g(b) - g(a)) + (1 - t)(g(c) - g(a))\right|} \\ 
 & \leq & t{\left|g(b) - g(a)\right|} + (1 - t){\left|g(c) - g(a)\right|} \\ 
 & \lt & t\epsilon + (1 - t)\epsilon = \epsilon
}$$ 

which completes the demonstration. 
=-- 

The same method can be used to exhibit a space-filling curve $I \to I^S$ for any set $S$ of finite or countable [[cardinality]]. Note that in the case where $S$ is a singleton, where we extend the surjection $C \to I$ to $I \to I$ by linear interpolation, we get the [Cantor-Lebesgue function](https://en.wikipedia.org/wiki/Cantor_function). 


## Hahn-Mazurkiewicz theorem 

The eponymous theorem may be stated as follows: 

+-- {: .num_theorem} 
###### Theorem 
A [[Hausdorff space]] $X$ admits a [[continuous function|continuous]] [[surjection]] $f: I \to X$ from the [[closed interval]] $I$ if and only if it is a [[connected space|connected, locally connected]] [[compact space|compact]] [[metrizable space]]. 
=-- 

(N.B. According to the nLab, connected spaces are [[inhabited set|nonempty]]!) 

The "only if" half is relatively easy; see [here](https://ncatlab.org/nlab/show/connected+space#arcconnectedness) for some details. The "if" half is rather more involved, but [Willard's General Topology](https://www.amazon.com/dp/0486434796/?tag=stackoverfl08-20) contains a proof. A space $X$ satisfying the stated conditions is called a **Peano space**. 

Given this characterization, it is not difficult to characterize which spaces are continuous images of $\mathbb{R}$: 

+-- {: .num_theorem} 
###### Theorem 
A [[path-connected space|path-connected]] Hausdorff space $X$ admits a continuous surjection $\mathbb{R} \to X$ if and only if it is a $\sigma$-Peano space, i.e., a countable union $\bigcup_{n: \mathbb{N}} A_n$ of Peano spaces. 
=-- 

+-- {: .proof} 
###### Proof 
The "only if" half being fairly obvious, the "if" part may be proved as follows. Since there are continuous surjections $[0, \infty) \to \mathbb{R}$ and $\mathbb{R} \to [0, \infty)$, it suffices to show that a $\sigma$-Peano space admits a continuous surjection from $[0, \infty)$. For each $n \in \mathbb{N}$ choose a continuous surjection $f_n: [2 n, 2 n + 1] \to A_n$. Then for each $n$ choose a path $g_n: [2 n + 1, 2 n + 2] \to X$ such that $g_n(2 n + 1) = f_n(2 n + 1)$ and $g_n(2 n + 2) = f_{n+1}(2 n + 2)$. Then the $f_n$ and $g_n$ paste together to form a continuous surjection $[0, \infty) \to X$. 
=-- 

An example of such a space is the [[Warsaw circle]]. 

## Related concepts

* [[topological invariance of dimension]] 

* [[connected space]] 

## References

Named after [[Giuseppe Peano]].

* Wikipedia, _[Peano curve](https://en.wikipedia.org/wiki/Peano_curve)_

* [[Guiseppe Peano]], *Sur une courbe, qui remplit toute une aire plane*, Mathematische Annalen, **36** 1 (1890) 157–160 &#x5B;[doi:10.1007/BF01199438](https://doi.org/10.1007/BF01199438)]

The proof of the Hahn-Mazurkiewicz theorem is given in section 31 (page 219ff) within chapter 8 of Willard's classic text: 

* Stephen Willard, *General Topology* (Dover Edition 2004). Originally published by Addison-Wesley, 1970. ([link to vendor](https://www.amazon.com/dp/0486434796/?tag=stackoverfl08-20))  

The question of which spaces are continuous images of the real line was asked (and answered with dispatch by Jeff Strom) at MathOverflow: 

* [[Todd Trimble]] (https://mathoverflow.net/users/2926/todd-trimble), continuous images of open intervals, URL (version: 2014-05-25): [https://mathoverflow.net/q/168084](https://mathoverflow.net/questions/168084/continuous-images-of-open-intervals) 

[[!redirects Peano curves]]
[[!redirects Peano space-filling curve]] 
[[!redirects Peano space-filling curves]] 
[[!redirects Peano space]] 
[[!redirects Peano spaces]] 
[[!redirects Hahn-Mazurkiewicz theorem]] 
