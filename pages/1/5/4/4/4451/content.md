# G-norms
* table of contents
{: toc}

## Idea

A G-norm is like a [[normed vector space|norm]] (or better, an [[F-norm]]) on a [[vector space]], but on an [[abelian group]] instead.  Just as the [[topological structure]] of any [[topological vector space]] may be specified by a family of F-pseudonorms, so the topological structure of any [[topological abelian group]] may be specified by a family of G-pseudonorms.  A G-norm on an abelian group is equivalent to a translation-invariant [[metric space|metric]] on it.


## Definitions

Let $G$ be an [[abelian group]].

A __G-pseudonorm__, or __G-seminorm__, on $G$ is a [[function]] $\rho\colon G \to \mathbb{R}$ that satisfies the following conditions:

*  $\rho(0) \leq 0$, where $0$ is the [[identity element]] of $G$;
*  $\rho(x + y) \leq \rho(x) + \rho(y)$ for all $x, y$ in $G$; and
*  $\rho(-x) \leq \rho(x)$ for all $x$ in $G$.

From these axioms, the following simple conditions (sometimes included in the definition) follow:

*  $\rho(x) \geq 0$ for all $x$ in $G$
*  $\rho(0) = 0$;
*  $\rho(-x) = \rho(x)$; and
*  $\rho(n x) \leq {|n|} \rho(x)$ for every [[integer]] $n$ and all $x$ in $G$.


A G-pseudonorm is __definite__ (or __postive-definite__, but we have positivity anyway) if in addition:

*  $\rho(x) \ne 0$ for all $x \ne 0$ in $G$.

And of course, from that follows:

*  $\rho(x) \gt 0$ for all $x \ne 0$ in $G$.

A __G-norm__ is a definite G-pseudonorm.


A G-(pseudo)norm is __homogeneous__ (or $\mathbb{Z}$-homogeneous) if we have:

*  $\rho(n x) \geq {|n|} \rho (x)$ for infinitely many integers $n$, for all $x$ in $G$.

It then follows that

*  $\rho(n x) = {|n|} \rho (x)$ for every integer $n$ and all $x$ in $G$.

While homogeneous G-norms are particularly nice, we need general G-pseudonorms if we wish to describe arbitrary [[topological abelian groups]].


## Examples

Given any translation-invariant [[metric space|(pseudo)metric]] $d$ on $G$, we get a G-(pseudo)norm $\rho$ on $G$ by $\rho(x) \coloneqq d(0,x)$.  Conversely, given any G-(pseudo)norm $\rho$, we get a translation-invariant (pseudo)metric $d$ by $d(x,y) \coloneqq \rho(y - x)$.  These operations are [[inverses]].  (We could add a 'quasi-' in here if we drop the rule that $\rho(-x) = \rho(x)$.  But note that G-quasinorms and translation-invariant quasimetrics on an [[abelian monoid]] do *not* correspond.)

If $G$ happens to be the underlying abelian group of a real (or complex) [[vector space]] $V$, then any [[F-norm|F-(pseudo)norm]] on $V$ is a G-(pseudo)norm on $G$, but not conversely.  Similarly, any [[normed vector space|(pseudo)norm]] on $V$ is a homogeneous G-(pseudo)norm on $G$, but not conversely.

The obvious norms on $\mathbb{Z}^n$, seen as a subset of $\mathbb{R}^n$ with one of its usual structures as a [[Banach space]], is a homogeneous G-norm.

Any abelian group has a G-norm given by $\rho(x) = 1$ whenever $x \ne 0$ (and of course $\rho(x) = 0$ otherwise).  Except on the [[trivial group]], this is not homogeneous.  It corresponds to the [[discrete metric]] on $G$.

Given any [[topological abelian group]] $G$ and any [[neighbourhood]] $N$ of $0$, let $B \coloneqq N \cap -N = \{ x \;|\; x \in N,\; -x \in N \}$; then $B$ is also a neighbourhood of $0$.  Let $B_0 \coloneqq G$, let $B_1 \coloneqq B$, and recursively choose $B_{n^+}$ so that $x + y + z \in B_n$ whenever $x, y, z \in B_{n^+}$ (which is possible since addition is continuous).  Then
$$ \rho (x) \coloneqq \inf \Big\{ \sum_{i = 1}^m \inf \{ 2^{-n} \;|\; x_i \in B_n \} \;\Big|\; x = \sum_{i = 1}^m x_i \Big\} $$
defines a G-pseudonorm on $G$ such that, given any [[net]] $(x_\nu)$ in $G$, we have that $\rho(x_\nu)$ converges to $0$ if and only if $x_\nu \in N$ holds eventually.


## Families of G-pseudonorms

Any family of G-pseudonorms on an abelian group $G$ makes $G$ into a [[topological abelian group]] (TAG), and every TAG structure on $G$ arises in this way.  However, different collections of G-pseudonorms may determine the same topological structure.

In one direction, let $G$ be an abelian group, and suppose that we equip $G$ with an arbitrary collection $D$ of G-pseudonorms.  Every G-pseudonorm determines a pseudometric, and these pseudometrics generate a [[gauge space]] structure on $G$ and thence a [[topological structure]].  Because the pseudometrics involved are translation-invariant, we have in fact made $G$ into a TAG. In more detail:  A [[subset]] $U$ of $G$ is [[open subset|open]] if and only if, for every $x$ in $U$, for some [[list]] $\rho_1,\ldots,\rho_n$ from $D$ and some [[real number]] $\epsilon \gt 0$, for every $y$ in $G$, if $\rho_i(y - x) \lt \epsilon$ for every $i$, then $y \in U$.  Then you can check that these subsets form a topology relative to which the group operations are continuous.

It may also be nice to look at the [[uniform space]] structure on $G$; the gauge and the TAG structure determine the same uniform structure.  Explicitly, a [[binary relation]] $\sim$ on $G$ is an [[entourage]] if and only if, for some list $\rho_1,\ldots,\rho_n$ from $D$ and some real number $\epsilon \gt 0$, for every $x$ and $y$ in $G$, if $\rho_i(y - x) \lt \epsilon$ for every $i$, then $x \sim y$.  Then these entourages form the uniform structure on $G$ which is compatible with the group structure and whose underlying topological structure is the one above.

Conversely, let $G$ be a TAG.  Then the collection of all [[continuous map|continuous]] G-pseudonorms $\rho\colon G \to \mathbb{R}$ generates the topological structure on $G$.  The proof is complicated, but essentially it amounts to this: applying the final example from the Examples section above to each neighbourhood of $0$ (or at least to each neighbourhood in a neighbourhood base), check that the G-pseudonorms defined are continuous, and check that there are enough of them to generate a topology at least as strong as the actual topology on $G$; the converse is immediate.  In other words, the hard thing that has to be checked is that there are enough continuous G-pseudonorms.


## In weak foundations

The only really tricky part is the proof that there are enough continuous G-pseudonorms to generate the topology on any TAG $G$.  The development seems to be [[predicative mathematics|predicative]] over $\mathbb{R}$; you can\'t speak of the collection of *all* continuous G-pseudonorms if you are being strongly predicative, but you really only need one for each neighbourhood in a neighbourhood base of $G$.  However, it is not [[constructive mathematics|constructive]] or predicative over $\mathbb{N}$, because the infima may not exist.  Also, we use [[dependent choice]]. 

The same problems arise in proving that every [[topological vector space]] structure is generated by some family of [[F-norm|F-pseudonorms]]; on the other hand, [[locally convex spaces]] (which are generated by [[pseudonormed space|pseudonorms]]) are better behaved.  There may be a similar theory of locally convex TAGs based on homogeneous G-pseudonorms, but I haven\'t looked into this.

It would be natural, in constructive mathematics, to attempt the development with [[locale|localic]] groups.  Even in [[classical mathematics]], however, there may be (and are) [[sober space|sober]] TAGs which cannot be interpreted as localic groups, such as the additive group of [[rational numbers]] with its topology as a [[subspace]] of the [[real line]].  Probably we have to start by requiring a G-pseudonorm to be a [[continuous map]] from the localic group $G$ to the [[locale of real numbers]], rather than starting with a discrete abelian group, but I haven\'t looked into this further.


## References

_[[HAF]]_, Chapters 22 and 26.  See especially Section 26.29 for the last Example.


[[!redirects G-norm]]
[[!redirects G-norms]]
[[!redirects G-pseudonorm]]
[[!redirects G-pseudonorms]]
[[!redirects G-seminorm]]
[[!redirects G-seminorms]]
