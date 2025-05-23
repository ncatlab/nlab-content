
# Contents
* automatic table of contents goes here
{: toc}

## Statement

The _Cantor--Schroeder--Bernstein_ theorem says that the usual [[order relation]] on [[cardinalities]] of [[set]]s is [[antisymmetric relation|antisymmetric]]. In other words, define an order on sets by $X \leq Y$ if there exists a [[monomorphism]] $f\colon X \to Y$. Then, if both $X \leq Y$ and $Y \leq X$, there exists an [[isomorphism]] of sets $X \cong Y$.

The result is really only interesting in the absence of the [[axiom of choice]] ($AC$).  With $AC$, it is a trivial corollary of the [[well-ordering theorem]].  However, the theorem actually requires only [[excluded middle]], although it does not hold in [[constructive mathematics]] --- indeed, it is actually *equivalent* to excluded middle (at least assuming the [[axiom of infinity]]).

## Proof 

We prove that the Cantor--Schroeder--Bernstein theorem holds in a [[Boolean topos]]. The theorem is not however [[intuitionistic logic|intuitionistically]] valid, in that it fails in some [[topos]]es, such as the topos $Set^{\bullet \to \bullet}$ (the [[arrow category]] of $Set$); see Example \ref{counterexample} below. 

Throughout we use ordinary [[set theory|set-theoretic]] reasoning which can be translated into the formal theory of toposes. (This can be formalized via the [[Mitchell–Benabou language]], for instance.) 

First, let's try a little pedagogy. Somehow functions $h: X \to Y, h^{-1}: Y \to X$ are to be cooked up from injections $f: X \to Y$ and $g: Y \to X$, so we might guess $h$ is to be defined as $f$ at least part of the time, and $h^{-1}$ as $g$ another part of the time. An ideal situation would be to have a set-up 

$$f: A \stackrel{\sim}{\longrightarrow} B$$ 

$$\,$$ 

$$C \stackrel{\sim}{\longleftarrow} D: g$$ 

where $A, C$ are complementary subsets in $X$ and $B, D$ are complementary subsets in $Y$; then $h$ could be defined as $f$ on $A$ and as $g^{-1}$ on $C$, and everything works out fine. How can we achieve this? 

If we have this situation, then apparently $B = f(A)$ (the direct image of $A$), and $D = \neg B = \neg f(A)$ (the complement of $f(A)$), and then $C = g(D) = g(\neg f(A))$, and finally $A, C$ are required to be complementary, so we would need 

$$A = \neg g(\neg f(A)).$$ 

In other words, $A$ would be a [[fixed point]] of a suitable operation built from direct image and complementation operators. In fact, if we find such a fixed point $A$, then the plan above would work without a hitch. 

Perhaps the simplest fixed-point theorem for this purpose on the market is 

+-- {: .num_lemma}
###### Lemma (Knaster--Tarski fixed-point theorem) 
Let $\phi\colon P X \to P X$ be an order-preserving map. Then there exists $A$ in $P X$ for which $\phi(A) = A$. 
=-- 

+-- {: .proof}
###### Proof 
Let $A$ be the (internal) [[intersection]] of $U = \{T \in P X : \phi(T) \leq T\}$. Since $A \leq T$ for every $T$ in $U$, we have $\phi(A) \leq \phi(T) \leq T$ for every $T$ in $U$. Hence $\phi(A) \leq A$ by definition of $A$. Applying $\phi$ again, we get $\phi \phi(A) \leq \phi(A)$. Hence $\phi(A)$ belongs to $U$. But then $A \leq \phi(A)$ by definition of $A$.
=--

+-- {: .num_remark #term}
###### Remark

The preceding proof is valid in _any_ topos (and so holds for $Set$ even intuitionistically). It can be seen as a specialization to posets of a result of Lambek on the [[initial algebra|initial]] [[algebra of an endofunctor]], saying that the structure maps of such initial algebras are necessarily isomorphisms. Here the initial algebra $A$ is (by construction) an initial fixed point. 

=--

+-- {: .proof}
###### Proof of Cantor--Schroeder--Bernstein

Suppose given two monos $f: X \to Y$, $g: Y \to X$. Let $\exists_f: P X \to P Y$ denote direct image or [[existential quantification]] along $f$, and let $\neg_X: P X \to P X$ denote [[negation]]. Then the composite 

$$\phi = \neg_X \exists_g \neg_Y \exists_f: P X \to P X$$ 

is order-preserving, and so has a fixed point $A$ by the Knaster-Tarski lemma. Now define $h: X \to Y$ by the rule 

$$\array{
h(x) & = & f(x) & \text{ if }\; x \in A \\
h(x) & = & g^{-1}(x) & \text{ if }\; x \notin A 
}$$ 

(the multi-line definition is where we use the Boolean condition). The second line makes sense because $\neg A$ is in the image of $g$. The inverse of $h$ is 

$$\array{
j(y) & = & f^{-1}(y) & \; \text{if} \; y \in \exists_f(A) \\
j(y) & = & g(y) & \; \text{if} \; y \notin \exists_f(A)
}$$

That $j$ is inverse to $h$ uses the fact that $\neg A = \exists_g \neg \exists_f(A)$. The rest is obvious. 
=--

This classic proof is substantially the proof given in Johnstone's [[Elephant]], D4.1.11. The Boolean condition is not *strictly speaking* necessary, i.e., the [[principle of excluded middle]] ($EM$) does not logically follow from the Cantor--Schroeder--Bernstein statement since, for example, using notation as above, monic endomorphisms like $f \circ g: Y \to Y$ and $g \circ f: X \to X$ are isomorphisms in 

$$FinSet^C,$$ 

but this is a non-Boolean, non-[[Grothendieck topos|Grothendieck]] topos provided that $C$ is any [[finite category]] that is not a [[groupoid]], e.g., $C = \mathbf{2}$. But that being said, $EM$ is certainly the most natural supposition to make. In fact EM does constructively follow from the Cantor-Schroeder-Bernstein statement provided that a [[natural numbers object]] exists (for instance in a Grothendieck topos); see [Pradic and Brown, 2019](#PB19).
A proof that in a topos CSB+NNO implies Booleanness is outlined in [Freyd  1994](#Freyd94), using the stronger hypothesis that the monomorphisms have retractions.

### Alternative construction of a fixed point {#alt}

In some schools of thought, the proof using the Knaster-Tarski lemma would be criticized because that lemma makes use of an [[impredicative]] construction. However, the application made of it in the proof of the CSB theorem is only to ensure that the operator $\neg_X \exists_g \neg_Y \exists_f: P X \to P X$ has a fixed point. This objection can be countered by shopping around for a different fixed-point theorem, one which is predicatively and constructively valid. 

A time-honored way of constructing a fixed point of an operator $\phi$ is by taking a limit of a sequence of iterates of $\phi$ that converges, provided that $\phi$ preserves the limit. To this end, we find that specializing Ad&#225;mek's theorem (see [[initial algebra of an endofunctor]]) suits our purposes perfectly.  

+-- {: .num_lemma #chain} 
###### Lemma 
If $g: Y \to X$ is monic, then the operator $\exists_g: P Y \to P X$ preserves limits of inverse chains $\omega^{op} \to P Y$ (i.e. intersections of decreasing sequences). 
=-- 

+-- {: .proof} 
###### Proof 
More generally, $\exists_g$ preserves [[connected limits]], because it lifts through the inclusion $i: P X \downarrow \exists_g(1) \hookrightarrow P X$ to an isomorphism $P Y \stackrel{\sim}{\to} P X \downarrow \exists_g(1)$ (here $1$ denotes the top element of $P Y$, aka $Y$), and $i$ preserves connected limits. 

In more detail: by [[Frobenius reciprocity]], we have $\exists_g T \wedge S = \exists_g(T \wedge g^\ast S)$ for elements $S$ of $P X$ and $T$ of $P Y$. Putting $T = 1$, we get $\exists_g 1 \wedge S = \exists_g g^\ast S$, and so the composite 

$$P X \downarrow \exists_g 1 \stackrel{g^\ast}{\to} P Y \stackrel{\exists_g}{\to} P X \downarrow \exists_g 1$$ 

is the identity. But since $g$ is monic, $g^\ast \exists_g: P Y \to P Y$ is also the identity, which completes the proof. 
=-- 

+-- {: .num_cor} 
###### Corollary 
$\forall_g = \neg_X \exists_g \neg_Y: P Y \to P X$ preserves colimits of $\omega$-chains. 
=-- 

Naturally the left adjoint $\exists_f$ also preserves such colimits. So by the corollary, the composite $\neg_X \exists_g \neg_Y \exists_f: P X \to P X$ preserves colimits of $\omega$-chains. 

Putting now $A_0 = 0$ (the bottom element of $P X$), $A_1 = \neg_X \exists_g \neg_Y \exists_f(0)$, and generally 

$$\label{An} A_n = (\neg_X \exists_g \neg_Y \exists_f)^n(0),$$ 

we have $A_n \subseteq A_{n+1}$ (apply the monotone operator $(\neg_X \exists_g \neg_Y \exists_f)^n$ to the inclusion $A_0 = 0 \subseteq A_1$), and so $\neg_X \exists_g \neg_Y \exists_f$ preserves the union of the chain $A_0 \subseteq A_1 \subseteq \ldots$,

$$\label{A} A = \bigcup_{n \geq 0} (\neg_X \exists_g \neg_Y \exists_f)^n(0),$$ 

which implies that $A$ is a fixed point of $\neg_X \exists_g \neg_Y \exists_f$, as desired. In fact this $A$ is the minimal fixed point, just as in the conclusion of the Knaster-Tarski lemma. (Cf. [[initial algebra of an endofunctor]], especially Ad&#225;mek's theorem.) 

### Beta reduced proof 

The preceding proofs are sometimes considered too abstract to easily visualize, but this is slightly misleading: the second proof, involving the construction of a minimal fixed point as a countable limit, can be "[[beta-reduced]]" to produce one of the standard "concrete" proofs. 

In a nutshell, the minimal fixed point of the operator $\neg \exists_g \neg \exists_f: P X \to P X$ can be expressed as an alternating series of iterated direct images: 

$$\label{series} X - g Y + g f X - g f g Y + \ldots$$ 

where $-$ stands for set-theoretic difference $\setminus$ and $+$ stands for the union $\cup$. The meaning of the infinite series is that we have a increasing sequence of those finite alternating sums with an even number of terms, starting with the empty sum (which is $0$, the empty set): 

$$0$$

$$\,$$

$$X - g Y,$$ 

$$\,$$ 

$$X - g Y + g f X - g f g Y,$$ 

etc., and the infinite series is interpreted as the countable union of this increasing sequence. Note that we have to be careful about the order of the appearance of $+$ and $-$, but alternatively, letting $\oplus$ be the addition in the Boolean *ring* $P X$ (symmetric difference), we could write also the series as $X \oplus g Y \oplus g f X \oplus \ldots$ in the ring, where we do not need to be fussy about order. 

Most of this is a routine calculation, which for the most part boils down to the following observation: 

+-- {: .num_lemma} 
###### Lemma 
If $B, D$ are elements of $P Y$, with $D \leq B$, then $\exists_g(B - D) = \exists_g B - \exists_g D$. (With a similar statement for $\exists_f$.) 
=-- 

The proof is left to the reader, but in brief, the injectivity of $g$ implies that $\exists_g$ preserves binary intersections and relative complements. 

From here, if we write 

$$\neg \exists_g \neg \exists_f(B) = X - g(Y - f B) = X - g Y + g f B = X \oplus g Y \oplus g f B,$$ 

then it is easily verified by induction that, referring to equation (eq:An), 

$$A_n = (\neg \exists_g \neg \exists_f)^n 0 = \bigoplus_{j=0}^n (g f)^j X \oplus \bigoplus_{j=0}^n g(f g)^j Y.$$ 

Thus, according to equation (eq:A), the minimal fixed point $A$ is the union of the $A_n$ which is how we are interpreting the series (eq:series). 

Now we set up a comparison with one of the standard proofs involving a [[back-and-forth argument]], say the one given in [Wikipedia](https://en.wikipedia.org/wiki/Schr%C3%B6der%E2%80%93Bernstein_theorem#Proof) that is attributed to Julius K&#246;nig. The minimal fixed point is a union of finitary approximations 

$$A_1 = X - g Y,$$ 

$$\,$$ 

$$A_2 = X - g Y + g f X - g f g Y,$$ 

etc. Elements in $A_1$ are those which have no inverse images under $g$. Elements in $A_2$ are elements in $X$ to which $(g f)^{-1}$ can be applied at most once before we hit an element of $X$ with no inverse image under $g^{-1}$. Elements in the union $A_1 \cup A_2 \cup \ldots$ are those which survive at most finitely many applications of $(g f)^{-1}$ before hitting an element of $X$ with no inverse image under $g$. In the terminology of the Wikipedia article, such elements $x$ in $X$ are called "$X$-stoppers", and these are exactly the elements for which $h(x)$ (where recall $h$ is the bijection under construction) is defined to be $f(x)$ in the Wikipedia article. For elements $x$ not in this fixed point $A$ (the non-$X$-stoppers), our proof of CSB (via a minimal fixed point) defined $h(x)$ to be $g^{-1}(x)$, the same prescription that is used in the Wikipedia article. 

Other prescriptions are possible. For example, one could dually construct a *maximal* fixed point of the operator $\neg \exists_g \neg \exists_f: P X \to P X$, using Lemma \ref{chain} to note that $\exists_f$ and the right adjoint $\forall_g = \neg \exists_g \neg$ preserve limits of inverse $\omega$-chains, so that the maximal fixed point or terminal algebra of the endofunctor $\neg \exists_g \neg \exists_f$ could be constructed as an intersection $\bigcap_{n \geq 1} (\neg \exists_g \neg \exists_f)^n(1)$. This could also be written as a series 

$$X - g Y + g f X - g f g Y + g f g f X - \ldots$$ 

except this time the series is interpreted as an *intersection* of a *decreasing* sequence whose partial sums have an *odd* number of terms: 

$$1 = X,$$ 

$$\,$$ 

$$\neg \exists_g \neg \exists_f(1) = X - g Y + g f X,$$ 

$$\,$$ 

$$(\neg \exists_g \neg \exists_f)^2(1) = X - g Y + g f X - g f g Y + g f g f X,$$ 

etc. The difference between this and the minimal fixed point is the set $\bigcap_{n \geq 1} (g f)^n(X)$, consisting of elements $x$ of $X$ that belong to a doubly infinite sequence or a cyclic sequence (in the terminology of the Wikipedia article). As remarked in that article, for such $x$ we have an option to define $h(x)$ as $f(x)$ or $g^{-1}(x)$; in the present article we defined $h(x) = f(x)$ for all $x$ belonging to whichever fixed point $A$ is used, which includes points in doubly infinite sequences or cyclic sequences if $A$ is the maximal fixed point. In that case the remaining $x$ (belonging to the complement of the maximal fixed point) are mapped to $g^{-1}(x)$. 

## Failure in toposes and constructive mathematics

+-- {: .num_example #Top}
###### Example

Counterexample \ref{counterexample2} below shows that the CSB theorem fails in Brouwer\'s [[intuitionistic mathematics]] even for $Set$ (since every function between the sets $[0, 1]$ and $\mathbb{R}$ must be continuous by Brouwer\'s continuity principle!). See also the discussion in [Mac Lane-Moerdijk](#MM), VI.9, on toposes that realize Brouwer's theorem. 
=--

+-- {: .num_example #counterexample} 
###### Example 

As mentioned above, the Cantor-Schroeder-Bernstein theorem fails in the arrow category $Set^\to$, whose objects are functions $X_0 \to X_1$ between sets and whose morphisms are commutative squares. For example, let $X$ be the object $f: \mathbb{N} \to \mathbb{N}$ that takes $n \in \mathbb{N}$ to $\mathrm{int}(n/2)$, where $\mathrm{int}(x)$ is the greatest integer less than or equal to $x$; let $Y$ be the object $g: \mathbb{N} \to \mathbb{N}$ that takes $n$ to $\mathrm{Int}((n+1)/2)$, where $\mathrm{Int}(x)$ is the least integer greater than or equal to $x$. Pretty clearly $X$ and $Y$ are non-isomorphic, because $g^{-1}(0)$ has cardinality $1$ whereas all fibers of $f$ have cardinality $2$. But, just by drawing pictures of these objects, it is easy to construct monomophisms $i: X \to Y$ and $j: Y \to X$ (e.g., define $i_0(n) = n+1$ and $i_1(n) = n+1$ for all $n$, and define $j_0(n) = n+1$ for $n \gt 0$, $j_0(0) = 0$, and $j_1(n) = n$ for all $n$). 
=-- 

Nor can one have internal existence of an isomorphism between $X$ and $Y$ in this last example, since internal existence implies external existence as soon as the terminal object is (externally) projective.

+-- {: .num_example #effectivetopos} 
###### Example 
There is an [[effective topos]] with an injection from the [[Baire space of sequences]] $\mathbb{N}^\mathbb{N}$ to the [[natural numbers]] $\mathbb{N}$. The constant functions on the natural numbers give an injection from $\mathbb{N}$ to $\mathbb{N}^\mathbb{N}$. However, due to [[Lawvere's fixed point theorem]], there is no bijection between $\mathbb{N}$ and $\mathbb{N}^\mathbb{N}$. 
=--

In fact, the CSB theorem is equivalent in [[constructive mathematics]] (with the [[axiom of infinity]]) to the [[law of excluded middle]].  This was shown in [Pradic and Brown, 2019](#PB19) using the [[principle of omniscience]] for the [[extended natural numbers]].


## In other categories

The CSB property holds in some other [[categories]] of interest (but arguably fails in many more). Some examples follow: 

+-- {: .num_example #archiemdean} 
###### Example 
The CSB property holds in the category of [[Archimedean ordered fields]] and [[ring homomorphisms]]. This is because every Archimedean ordered field is a [[subset]] of the [[real numbers]], and ring homomorphisms between Archimedean ordered fields are subset inclusions in the [[powerset]] of the real numbers; i.e. the category of [[Archimedean ordered fields]] is a [[full subcategory]] of the [[powerset]] of the real numbers. This remains true in [[constructive mathematics]] but one has to use the [[Dedekind real numbers]] as only the Dedekind real numbers are the [[terminal object]] in the category of [[Archimedean ordered fields]] and [[ring homomorphisms]]. 
=--

+-- {: .num_example #preorder} 
###### Example 
More generally, the CSB property holds in any [[partial order]] (i.e. [[thin category|thin]] [[gaunt category]]). 
=--

+-- {: .num_example #model} 
###### Example 
The CSB property holds in the category of [[vector spaces]] and in the category of [[algebraically closed field]]s. See also this [MO post](http://mathoverflow.net/questions/1058/when-does-cantor-bernstein-hold) by John Goodrick, where model-theoretic criteria come into play, sometimes under strengthenings of the notion of monomorphism (e.g., [[elementary embedding]], [[split monomorphism]]) Some slides by Goodrick [here](http://settheory.mathtalks.org/wp-content/uploads/2012/06/jonh_goodrick.pdf) go into more detail, giving connections between CSB and [[stability theory|stable theories]] in the sense of [[Shelah]]. 
=-- 

+-- {: .num_example #counterexample2} 
###### Counterexample 
On the other hand, the CSB property obviously fails in [[Top]], since we have [[embeddings]] $\mathbb{R} \cong (0,1) \to [0,1] \to \mathbb{R}$, yet $[0,1] \ncong \mathbb{R}$. It fails in [[Grp]] (e.g., the free group on countably many generators embeds in the free group on two generators). 
=-- 

More examples and discussion can be found at this Secret Blogging Seminar [post](http://sbseminar.wordpress.com/2007/10/30/theme-and-variations-schroeder-bernstein/). 

In a [celebrated work](#Gowers), [[Timothy Gowers]] gave a negative solution in the case of [[Banach spaces]].

Martin Escardó has announced a proof of CSB in the base theory of [[Martin-Löf dependent type theory]] with the added assumption of [[function extensionality]] and [[excluded middle]], and supplied an [[Agda]] proof ([Escardó 2020](#Escardo20)). There is a slight subtlety in that "injection" is replaced by "embedding", where the latter is defined to be a map whose fibres are [[subsingletons]]. This implies that CSB holds for [[homotopy types]]/$\infty$-groupoids.


## Name

The CSB theorem was first stated by [[Georg Cantor]], but his proof relied on the [[well-ordering theorem]].  The modern (choice-free) theorem was proved (independently) by [[Felix Bernstein]] and [[Ernst Schröder]].  It has been variously named after two or three of these in almost every possible combination, although Cantor (when mentioned at all) seems always to be mentioned first. 

[[Richard Dedekind]] wrote out a proof on 11th July 1887, and only later published in his Nachlass in 1932 ([Dedekind 1932](#Dedekind)), while working on a draft of _Was sind und was sollen die Zahlen?_, well before any announced proofs by Cantor, Schroeder, or Bernstein in 1895, 1896, 1897 respectively. 


## References 


* {#Dedekind} [[Richard Dedekind]] (1932), [[Robert Fricke]]; [[Emmy Noether]]; [[Øystein Ore]] (eds.), _Gesammelte mathematische Werke_, vol. 3, Braunschweig: Friedr. Vieweg & Sohn, pp. 447–449 (Ch.62) [Göttinger Digitalisierungszentrum ](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=PPN23569441X)


* [[Peter Johnstone]], _[[Sketches of an Elephant]]: A Topos Theory Conpendium_, Vol. I, Clarendon Press, Oxford (2002)

* {#Gowers} [[Timothy Gowers]], _A Solution to the Schroeder-Bernstein Problem for Banach Spaces_, Bulletin of the London Mathematical Society, Volume 28, Issue 3 (1996), 297-304 [(abstract)](http://blms.oxfordjournals.org/content/28/3/297.abstract)
 

* {#MM} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_, Springer-Verlag 1992. 

* {#Freyd94}[[Peter Freyd]], _Cantor-Bernstein - message to the category theory mailing list_, February 1994. ([link](https://www.mta.ca/~cat-dist/archive/1994/94-2))

* {#PB19} Pierre Pradic, Chad E. Brown, *Cantor-Bernstein implies Excluded Middle*, 2019 ([arxiv:1904.09193](https://arxiv.org/abs/1904.09193))

* {#Escardo20} Martín Hötzel Escardó, _The Cantor-Schröder-Bernstein Theorem for ∞-groupoids_, 2020 ([blog post](https://homotopytypetheory.org/2020/01/26/the-cantor-schroder-bernstein-theorem-for-%e2%88%9e-groupoids/), [Agda proof](https://www.cs.bham.ac.uk/~mhe/agda-new/CantorSchroederBernstein.html), [arXiv:2002.07079](https://arxiv.org/abs/2002.07079))


[[!redirects Cantor-Schroeder-Bernstein theorem]]
[[!redirects Cantor–Schroeder–Bernstein theorem]]
[[!redirects Cantor--Schroeder--Bernstein theorem]]
[[!redirects Cantor-Schroeder-Bernstein Theorem]]
[[!redirects Cantor–Schroeder–Bernstein Theorem]]
[[!redirects Cantor--Schroeder--Bernstein Theorem]]
[[!redirects Cantor-Schröder-Bernstein theorem]]
[[!redirects Cantor–Schröder–Bernstein theorem]]
[[!redirects Cantor--Schröder--Bernstein theorem]]
[[!redirects Cantor-Schröder-Bernstein Theorem]]
[[!redirects Cantor–Schröder–Bernstein Theorem]]
[[!redirects Cantor--Schröder--Bernstein Theorem]]
[[!redirects Schroeder-Bernstein theorem]]
[[!redirects Schroeder–Bernstein theorem]]
[[!redirects Schroeder--Bernstein theorem]]
[[!redirects Schroeder-Bernstein Theorem]]
[[!redirects Schroeder–Bernstein Theorem]]
[[!redirects Schroeder--Bernstein Theorem]]
[[!redirects Schröder-Bernstein theorem]]
[[!redirects Schröder–Bernstein theorem]]
[[!redirects Schröder--Bernstein theorem]]
[[!redirects Schröder-Bernstein Theorem]]
[[!redirects Schröder–Bernstein Theorem]]
[[!redirects Schröder--Bernstein Theorem]]
