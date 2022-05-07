
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

__Borel\'s Theorem__ (also called _Borel\'s Lemma_) says that every [[power series]] is the [[Taylor series]] of some [[smooth function]]. In other words: for every collection of prescribed [[partial derivatives]] at some point, there is a smooth function having these as its actual derivatives.


## Statements

+-- {: .num_theorem #basic}
###### Theorem

The canonical map from the ring of germs of $C^\infty$ function at $0 \in \mathbb{R}^n$ to the ring of formal power series obtained by taking the Taylor series at $0$ is surjective.
=--

There are many extensions and variants. 


For $\mathbb{R}^{n+m}$ a [[Cartesian space]] of [[dimension]] $n+m \in \mathbb{N}$, write $C^\infty(\mathbb{R}^{n+m})$ for the $\mathbb{R}$-[[associative algebra|algebra]] of [[smooth function]]s with values in $\mathbb{R}$.

Write $m^\infty_{\mathbb{R}^n \times \{0\}} \subset C^\infty(\mathbb{R}^{n+m})$ for the ideal of functions all whose [[partial derivatives]] along $\mathbb{R}^m$ vanish.

+-- {: .num_theorem #general}
###### Theorem

Forming the [[Taylor series]] constitutes an [[isomorphism]]

$$
  C^\infty(\mathbb{R}^{n+m})/m^\infty_{\mathbb{R}^n \times \{0\}}
  \stackrel{\simeq}{\longrightarrow}
  C^\infty(\mathbb{R}^n) [ [ Y_1, \cdots, Y_m] ]
$$

between smooth functions modulo those whose derivatives along $\mathbb{R}^m$ vanish and the ring of [[power series]] in $m$-variables over $C^\infty(\mathbb{R}^n)$.
=--

This appears for instance as ([Moerdijk-Reyes, theorem I.1.3](#MoerdijkReyes)).


## Proof

There is a full proof in Moerdijk--Reyes, cited above.  Here we prove Theorem \ref{basic} to indicate the method; the general version is not substantially different.  (This is based on the proof in [the English Wikipedia article](https://en.wikipedia.org/wiki/Borel%27s_lemma) at the time of writing, but with more details.)

+-- {: .proof}
###### Proof (of Theorem \ref{basic})

A real [[power series]] at $0$ is given simply by an [[infinite sequence]] $c = (c_n)_{n\geq{0}}$ of [[real numbers]].  Given such a sequence, we would ideally use
$$ f(x) = \sum_{n=0}^\infty c_n x^n ,$$
but this is only correct if the sum [[convergence|converges]] on at least some [[neighbourhood]] of $0$ (in other words if the power series has a positive [[radius of convergence]]).

To ensure this, let $\psi$ be a [[smooth function|smooth]] [[bump function]] chosen so that $\psi(x) = 1$ for ${|x|} \leq 1$ and $\psi(x) = 0$ for ${|x|} \geq 2$.  (For example, $\psi(x) = \frac{\phi(x + 2)} {\phi(x + 2) + \phi(-x - 1)} \frac{\phi(-x + 2)} {\phi(-x + 2) + \phi(x - 1)}$, where $\phi(x)$ is $\exp(-1/x)$ when $x \gt 0$ and otherwise vanishes.)  Next, choose an infinite sequence $H = (H_n)_{n\geq{1}}$ of positive finite numbers:
$$ 
  H_n 
    = 
  \max_{0\leq{k}\lt{n}} 
  \,
  \max_{0\leq{i}\leq{k}} 
  \,
  \root{n-k}{
    2^{2n-i}
    \, 
    (k + 1)
    \, 
    n^{\underline{k}} 
    \,
    k^{\underline{i}} 
    \,
    i!^{-1} 
    \,
    {|c_n|} 
    \,
    {\|\psi^{(k-i)}\|_\infty}
   }
  $$
(where $m^{\underline{j}}$ is the [[falling power]] $\prod_{0\leq{h}\lt{j}} (m - h)$, including the special case $m! = m^{\underline{m}}$); also, let $H_0 = 0$ (the [[bottom element]] of $[0,\infty]$, since $0 \leq k \lt 0$ never occurs).  Finally, define
$$ f(x) = \sum_{n=0}^\infty c_n \psi(H_n x) x^n .$$

If things go well, the [[derivatives]] of $f$ will be
$$ f^{(k)}(x) = \sum_{n=k}^\infty \sum_{i=0}^k i!^{-1} k^{\underline{i}} n^{\underline{i}} c_n H_n^{k-i} \psi^{(k-i)}(H_n x) x^{n-i} ,$$
and I claim that this is so.  Since $\psi^{(k-i)}(H_n x) = 0$ for ${|x|} \geq 2/H_n$, we have

$$ 
  \begin{aligned}
     {\|f^{(k)}\|_\infty} 
     & \leq 
    \sum_{n=k}^\infty \sum_{i=0}^k i!^{-1} k^{\underline{i}} n^{\underline{i}} {|c_n|} H_n^{k-i} {\|\psi^{(k-i)}\|_\infty} (2/H_n)^{n-i} 
     \\
     & \leq \sum_{n=k}^\infty (k + 1) \max_{0\leq{i}\leq{k}} i!^{-1} k^{\underline{i}} n^{\underline{i}} {|c_n|} {\|\psi^{(k-i)}\|_\infty} 2^{n-i}/H_n^{n-k} 
     \\
     & \leq (k + 1) \max_{0\leq{i}\leq{k}} i!^{-1} k^{\underline{i}} k^{\underline{i}} {|c_n|} {\|\psi^{(k-i)}\|_\infty} 2^{k-i} + \sum_{n=k+1}^\infty 2^{-n} 
  \end{aligned}
  \,,
$$
which is finite.  This proves [[uniform convergence]] of each claimed derivative (although not equiconvergence of all at once), and so each series not only converges but also may be antidifferentiated term by term, proving that $f^{(k)}$ is as claimed.

Finally (because $\psi^{(m)}(0) = 0$ for $m \gt 0$ but $\psi(0) = 1$, and the same goes for $0^m$),
$$ f^{(k)}(0) = \sum_{n=k}^\infty \sum_{i=0}^k i!^{-1} k^{\underline{i}} n^{\underline{i}} c_n H_n^{k-i} \psi^{(k-i)}(0) 0^{n-i} = k!^{-1} k! k! c_k H_k^0 \psi(0) 0^0 = k! c_k ,$$
making $c_k$ the $k$th coefficient of the Taylor series of $f$ at $0$, as desired.
=--


## Related theorems

* the [[Hadamard lemma]]

* the [[Tietze extension theorem]]

* the [[Whitney extension theorem]]

* the [[Steenrod-Wockel approximation theorem]]

* [[embedding of smooth manifolds into formal duals of R-algebras]]

* [[smooth Serre-Swan theorem]]

* [[derivations of smooth functions are vector fields]]

## Related concepts

* [[asymptotic expansion]]

## References

The original reference is

* [[Émile Borel]], _Sur quelques points de la th&#233;orie des fonctions_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 3, 12 (1895), 
p. 9--55 [numdam](http://www.numdam.org/item?id=ASENS_1895_3_12__9_0)

It had been actually proved by [[Giuseppe Peano]] before Borel

* &#193;d&#225;m Besenyei, _Peano's unnoticed proof of Borel's theorem_ ([pdf](http://www.cs.elte.hu/~badam/publications/borel.pdf))

Textbook discussion includes

* {#MoerdijkReyes} [[Ieke Moerdijk]], [[Gonzalo Reyes]], chapter I of _[[Models for Smooth Infinitesimal Analysis]]_

A generalization to [[Banach spaces]] is in 

* John C. Wells, _Differentiable functions on Banach spaces with Lipschitz derivatives_, J. Differential Geom. 8:1 (1973), 135-152 [euclid](http://projecteuclid.org/euclid.jdg/1214431488)

and is cited (along with extensive discussion and (counter)examples) also as (Ch.III) 15.4 in 

* [[Andreas Kriegl]], [[Peter Michor]], _[[The Convenient Setting of Global Analysis]]_, Mathematical Surveys and Monographs, 53 AMS (1997) [pdf](http://www.mat.univie.ac.at/~michor/apbookh-ams.pdf)
 

[[!redirects Borel's theorem]]
[[!redirects Borel\'s theorem]]
[[!redirects Borel/'s theorem]]
[[!redirects Borel's theorem]]
[[!redirects Borel's Theorem]]
[[!redirects Borel\'s Theorem]]
[[!redirects Borel/'s Theorem]]
[[!redirects Borel's Theorem]]

[[!redirects Borel theorem]]
[[!redirects Borel Theorem]]

[[!redirects Borel's theorem on power series]]


[[!redirects Borel's lemma]]
[[!redirects Borel\'s lemma]]
[[!redirects Borel/'s lemma]]
[[!redirects Borel's lemma]]
[[!redirects Borel's Lemma]]
[[!redirects Borel\'s Lemma]]
[[!redirects Borel/'s Lemma]]
[[!redirects Borel's Lemma]]

[[!redirects Borel lemma]]
[[!redirects Borel Lemma]]
