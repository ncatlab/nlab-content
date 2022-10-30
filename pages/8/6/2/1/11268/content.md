
#Contents#
* table of contents
{:toc}

## Idea



Various [[diagonal arguments]] such as the [[halting theorem]], [[Cantor's theorem]], and [[Gödel]]'s [[incompleteness theorem]] are all instances of the _Lawvere fixed point theorem_, which says that for any [[cartesian closed category]], if there is a suitable notion of [[epimorphism]] from some [[object]] $A$ to the [[exponential object]]/[[internal hom]] from $A$ into some other object $B$

$$
  A \longrightarrow B^A
$$

then every [[endomorphism]] $f \colon B \to B$ of $B$ has a [[fixed point]].

## Precise statement 

Let us say that a map $\phi: X \to Y$ is _point-surjective_ if for every point $q: 1 \to Y$ there exists a point $p: 1 \to X$ that lifts $q$, i.e., $f p = q$. 

+-- {: .num_prop} 
###### Proposition 
In a cartesian closed category, if there is a point-surjective map $\phi: A \to B^A$, then every morphism $f: B \to B$ has a fixed point $s: 1 \to B$ (so that $f s = s$). 
=-- 

+-- {: .proof} 
###### Proof 
Given $f: B \to B$, let $q: 1 \to B^A$ name the composite map 

$$A \stackrel{\delta}{\to} A \times A \stackrel{\phi \times 1_A}{\to} B^A \times A \stackrel{eval}{\to} B \stackrel{f}{\to} B$$ 

from $A$ to $B$. In [[lambda calculus]] notation, $q = \lambda a: A. f \phi(a)(a)$. Let $p: 1 \to A$ lift $q$. Then calculate 

$$\phi(p)(p) = q(p) = (\lambda a: A. f \phi(a)(a))(p) = f \phi(p)(p)$$ 

where the last equation is a [[beta-reduction]]. Hence $s \coloneqq \phi(p)(p)$ is a fixed point of $f$. 
=-- 

+-- {: .num_remark} 
###### Remark 
As pointed out by Lawvere, a hypothesis even weaker than point-surjectivity will do. Namely, $g: X \to Y^A$ is called _weakly point-surjective_ iff for every $f: A \to Y$ there is $x: 1 \to X$ such that for every $a: 1 \to A$, we have $g(x)(a) = f(a)$. (This is weaker because $g(x) = f$ cannot be inferred from $g(x)(a) = f(a)$ for all _[[global elements]]_ $a$.) 
=-- 

+-- {: .num_remark} 
###### Remark 
The statement need not hold if "(weakly) point-surjective" is replaced by "epimorphism". For example, in the cartesian closed category of compactly generated Hausdorff spaces and continuous maps, with $S = S^1$ the circle, the [[Polish space]] $S^\mathbb{N}$ is compactly generated under the product topology; this is the exponential where $\mathbb{N}$ is given the discrete topology. There is a countable dense subspace $i: \mathbb{N} \to S^\mathbb{N}$, but recall that for any full subcategory of the category of Hausdorff spaces, a map $f: X \to Y$ is an epimorphism iff it has a dense [[image]]. On the other hand, there are obvious rotations of $S$ that have no fixed points. 
=-- 

Thus epimorphisms need not be (weakly) point-surjective. Nor are point-surjective maps necessarily epimorphisms; for example, if $U \hookrightarrow V$ is a proper inclusion between proper subobjects of the terminal object $1$ (as may happen in a [[sheaf topos]]), then this is vacuously point-surjective but only rarely an epimorphism. 



## References

The original article is

* [[William Lawvere]], _Diagonal Arguments and Cartesian Closed Categories_, Lecture Notes in Mathematics, 92 (1969), 134-145 ([TAC](http://tac.mta.ca/tac/reprints/articles/15/tr15abs.html))

A review and further development is in

* {#Yanofsky03} [[Noson Yanofsky]], _A Universal Approach to Self-Referential Paradoxes, Incompleteness and Fixed Points_, ([arXiv:math/0305282](http://arxiv.org/abs/math/0305282))


Expositions include

* [[Andrej Bauer]], _On a proof of Cantor's theorem_ ([web](http://math.andrej.com/2007/04/08/on-a-proof-of-cantors-theorem/))

[[!redirects Lawvere fixed point theorem]]
