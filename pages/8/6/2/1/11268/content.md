
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Logic
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


Various [[diagonal arguments]], such as those found in the proofs of the [[halting theorem]], [[Cantor's theorem]], and [[Gödel]]'s [[incompleteness theorem]], are all instances of the _Lawvere fixed point theorem_ ([Lawvere 69](#Lawvere69)), which says that for any [[cartesian closed category]], if there is a suitable notion of [[epimorphism]] from some [[object]] $A$ to the [[exponential object]]/[[internal hom]] from $A$ into some other object $B$

$$
  A \longrightarrow B^A
$$

then every [[endomorphism]] $f \colon B \to B$ of $B$ has a [[fixed point]].

## Precise statement 

Let us say that a map $\phi: X \to Y$ is _point-surjective_ if for every point $q: 1 \to Y$ there exists a point $p: 1 \to X$ that lifts $q$, i.e., $\phi p = q$. 

+-- {: .num_theorem} 
###### Theorem 
**(Lawvere's fixed-point theorem)** 
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

Thus epimorphisms need not be (weakly) point-surjective. Nor are point-surjective maps necessarily epimorphisms; for example, if $U \hookrightarrow V$ is a proper inclusion between proper subobjects of the terminal object $1$ (as may happen in a [[sheaf topos]]), then this is vacuously point-surjective but not an epimorphism. 

Point-surjectivity may seem like an inadequate notion of "epimorphism", but it suffices for many purposes. For example, 

+-- {: .num_prop} 
###### Proposition 
**(Cantor's theorem in a topos)** 
For any object $X$, there is an epimorphism $f: X \to \Omega^X$ only if the topos is degenerate. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose there existed such an epi. In a topos, a map $f: X \to Y$ is epi iff the [[image|direct image]] map $\exists_f: \Omega^X \to \Omega^Y$ retracts the [[preimage|inverse image]] map $\Omega^f: \Omega^Y \to \Omega^X$, i.e., $\exists_f \circ \Omega^f = 1_{\Omega^Y}$. Putting $Y = \Omega^X$, the supposition implies that $\exists_f: Y \to \Omega^Y$ is a retraction. But retractions are automatically point-surjective. 

We then conclude from Lawvere's fixed point theorem that every endomorphism on $\Omega$, in particular the negation $\neg: \Omega \to \Omega$, has a fixed point $p: 1 \to \Omega$. Then $0 = p \wedge \neg p = p \wedge p = p$, whence $\neg 0 = 0$, or "true = false": the topos is degenerate.
=--

Once we have a proposition $p$ with $p = \neg p$, another way to conclude the proof is to apply Lawvere's fixed-point theorem again to the surjection $p \to 0^p$, where $p$ is regarded as a [[subsingleton]] and $0$ is the initial object, so that $0^p = \neg p$.  This gives a fixed point $1\to 0$ of the identity map $0\to 0$, which again makes the topos degenerate.  (The shorter version above is a [[beta-reduction]] of this.)  For a formalization of this argument and a generalization thereof to [[universe types]], see [Escardo18](#Escardo18).


+-- {: .num_remark} 
###### Remark 
Another version of Lawvere's fixed-point theorem requires only finite products for its statement. Namely, in a category with finite products, suppose $\Phi: A \times A \to B$ is a morphism with the property that for each $g: A \to B$ there exists $a: 1 \to A$ such that $g \lambda = \Phi \circ (a \times 1_A)$, where $\lambda: 1 \times A \stackrel{\sim}{\to} A$ is the projection. Then every map $f: B \to B$ has a fixed point. This version of the theorem is emphasized by [Yanofsky](#Yanofsky03). 
=-- 

+-- {: .num_remark} 
###### Remark 
Many applications of Lawvere's fixed point theorem are in the form of negated propositions, e.g., there is no epimorphism from a set to its power set, or [[Peano arithmetic]] cannot prove its own [[consistency]]. However, there are positive applications as well, e.g., it implies the existence of [[fixed-point combinators]] in [[untyped lambda calculus]]. 
=-- 

## History
 {#History}

In an interview ([Lawvere 07](William+Lawvere#Interview07)) not long after G&#246;del's 100th birthday, [[William Lawvere]] answered the question

> We have recently celebrated Kurt G&#246;del's 100th birthday. What do you think about the extra-mathematical publicity around his incompleteness theorem?

by saying (reproduced in [Lawvere 69 reprint, p. 2](#Lawvere69)):

> In 'Diagonal arguments and Cartesian closed categories' ([Lawvere 69](#Lawvere69)) we demystified the incompleteness theorem of G&#246;del and the truth-definition theory of Tarski by showing that both are consequences of some very simple algebra in the Cartesian-closed setting. It was always hard for many to comprehend how Cantor's mathematical theorem could be re-christened as a "paradox" by Russell and how G&#246;del's theorem could be so often declared to be the most significant result of the 20th century. There was always the suspicion among scientists that such extra-mathematical publicity movements concealed an agenda for re-establishing belief as a substitute for science. Now, one hundred years after G&#246;del's birth, the organized attempts to harness his great mathematical work to such an agenda have become explicit.

## Related pages 

* [[fixed point]]

* [[Kleene's fixed point theorem]]

* [[Brouwer's fixed point theorem]]

* [[Lefschetz fixed point theorem]]

* [[Cantor's theorem]] 

* [[fixed-point combinator]] 

* [[incompleteness theorem]] 

* [[Löb's theorem]]


## References
 {#References}

The original article:

* {#Lawvere69} [[William Lawvere]], _Diagonal Arguments and Cartesian Closed Categories_, Lecture Notes in Mathematics, **92** (1969) 134-145 &lbrack;[tac:15](http://tac.mta.ca/tac/reprints/articles/15/tr15abs.html)&rbrack;

Review and further development:

* {#Yanofsky03} [[Noson Yanofsky]], *A Universal Approach to Self-Referential Paradoxes, Incompleteness and Fixed Points*, The Bulletin of Symbolic Logic **9** 3 (2003) 362-386 &lbrack;[arXiv:math/0305282](http://arxiv.org/abs/math/0305282), [jstor:3109884](https://www.jstor.org/stable/3109884)&rbrack;


Exposition:

* [[Andrej Bauer]], _On a proof of Cantor's theorem_ ([web](http://math.andrej.com/2007/04/08/on-a-proof-of-cantors-theorem/))

Formalization in [[Agda]]

* {#Escardo18} [[Martin Escardo]], _On Lawvere's Fixed Point Theorem_ (2018) &lbrack;[agda development](https://www.cs.bham.ac.uk/~mhe/agda-new/LawvereFPT.html)&rbrack;
 


The necessary assumptions for Lawvere's account are reduced in various ways in

* {#Roberts} [[David Michael Roberts]], _Substructural fixed-point theorems and the diagonal argument: theme and variations_,  Compositionality **5** issue 8 (2023) doi:[10.32408/compositionality-5-8](https://doi.org/10.32408/compositionality-5-8),
([arXiv:2110.00239](https://arxiv.org/abs/2110.00239)).


[[!redirects Lawvere fixed point theorem]]
