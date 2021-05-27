
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# The Continuum Hypothesis
* table of contents
{: toc}

## Idea

> Cantor's continuum problem is simply the question: How many points are there on a straight line in Euclidean space? In other terms, the question is: How many different sets of integers do there exist?  K. G&#246;del ([1947](#Goedel47), p.515)

The **continuum hypothesis** is a famous problem of [[set theory]] concerning the cardinality of the&#160;[[Dedekind real numbers|Dedekind]] [[real numbers]] (the "[[continuum]]"). The hypothesis in its classical form goes back to [[Georg Cantor|G. Cantor]] and was on top of [[Hilbert's problems|Hilbert's list]] of open problems in mathematics in 1900.

In concise form the continuum hypothesis ($CH$) reads: $\quad 2^{\aleph_0}=\aleph _1\quad$; which roughly says that every [[subset]] of the Dedekind real numbers is either [[countable set|countable]] or has the same [[cardinality]] as the set of all Dedekind real numbers.

The *generalized continuum hypothesis* ($GCH$) states more generally: $\quad 2^{\aleph_k}=\aleph _{k+1}\quad$. (But see also Remark \ref{GCHinZF} below.) 

The **independence of the continuum hypothesis** from the [[ZFC]] axioms of set theory has been established in landmark papers by [[Kurt Gödel|K. Gödel]] and [[Paul J. Cohen|P. J. Cohen]], the former proving the consistency of $ZFC+CH$ relative to $ZFC$ in 1938, and the latter proving the consistency of $ZFC+\neg CH$ relative to $ZFC$ in 1963. For fully [[formal proof]] see [Han 18](#Han18).

The broader implications of the independence results for set theory in general and $ZFC$ in particular are somewhat controversial. They are widely taken as a pointer towards the deficiency of $ZFC$ and the need for _new axioms_ of set theory. This position has been voiced famously in [G&#246;del (1947)](#Goedel47) from a [[platonism|platonist perspective]].

[[William Lawvere|W. Lawvere]] in [2003](#Lawvere03) interpreted Cantor's original point of view as saying that $CH$ holds for 'sufficiently structureless' sets and, accordingly, viewed G&#246;del's 1938 result as a proof of $CH$, whereas in [[Patrick Dehornoy|P. Dehornoy]]'s 2003 reinterpretation based on work of _Woodin_, $CH$ is actually conjectured to be false. [[Solomon Feferman|S. Feferman]] has argued more recently that $CH$ is essentially _mathematically indefinite_ and has made notions of 'indefiniteness' explicit that indeed enable to back this point of view with technical results (cf. [Feferman (2011)](#Feferman11)).  Similarly, [[Joel David Hamkins]] has argued (cf. [Hamkins 2012](#Hamkins12)) that under the [[set-theoretic multiverse|multiverse]] view of set theory, $CH$ is settled by our extensive knowledge of models of set theory satisfying both $CH$ and $\neg CH$ which all seem fully set-theoretic, so that no principle implying either one can possibly be considered 'obviously true'.

The attempt to give categorical accounts of the [[forcing]] methods introduced by Cohen provided a strong impetus in the development of (elementary) [[topos theory]] in the work of [[Peter Freyd|Freyd]], [[Miles Tierney|Tierney]], Lawvere and later Scedrov. The following exposition follows this categorical  approach.


## Statement

+-- {: .num_defn}
###### Definition

Let $E$ be an [[elementary topos]] with [[subobject classifier]] $\Omega$ and [[natural numbers object]] $N$.  The (external) **continuum hypothesis** in $E$ asserts that if there is a sequence of [[monomorphisms]]

$$N \hookrightarrow A\hookrightarrow \Omega^N$$

then either there exists a monomorphism $A \hookrightarrow N$ or a monomorphism $\Omega^N \hookrightarrow A$.
=--

When the topos is Boolean, so the [[Cantor-Schroeder-Bernstein theorem]] holds, this implies the existence of an isomorphism $A \simeq N$ or $\Omega^N \simeq A$. Note, however, that neither of the original monomorphisms is necessarily an isomorphism (one of them could be the successor map on $N$, for example).

In the classical case (that is, in the topos [[Set]] with the [[axiom of choice]]), this equivalently asserts that there is no strict inequality of [[cardinal numbers]]

$${|\mathbb{N}|} \lt \alpha\lt {|\Omega^\mathbb{N}|}$$

which it is more common to write as

$$ \aleph_0 \lt \alpha \lt 2^{\aleph_0} $$

In the formal proof outlined in ([Han–van Doorn 20](#HanvanDoorn20)), the statement is fomulated in [[Lean]] as:

$$\forall x, Ord(x)\Rightarrow x \leq \omega \vee P(\Omega) \leq x$$

where $x\leq y$ means $x$ is a [[subquotient]] of $y$, and $Ord(x)$ is a predicate that returns True if and only if $x$ is an [[ordinal]]. This says that no ordinal can be between $\omega$ and $P(\omega)$ in size. 
In the presence of classical logic and the well-ordering principle, this then implies that no set can have cardinality between $\omega$ and $P(\omega)$.


### In weakly predicative mathematics

[[predicative mathematics|Predicatively]], the power set $\Omega^N$ does not exist, but if function sets exist, then the mathematics is only weakly predicative. Assuming $E$ is a [[Heyting category|Heyting]] [[ΠW-pretopos]], one replaces the subset classifier $\Omega$ in the definition of the [[Dedekind real numbers]] with a [[Sierpinski space|Sierpinski space object]] $S$ in $Set$, defined as a $\omega$-[[small]] ([[countable set|countable]]) [[frame]] in $Set$, an initial $\sigma$-frame in $Set$. The continuum hypothesis then becomes that if there is a series of monomorphisms such that

$$N \hookrightarrow A\hookrightarrow S^N$$

then either there exists a monomorphism $A \hookrightarrow N$ or a monomorphism $S^N \hookrightarrow A$.

If the $\Pi W$-pretopos $E$ is [[Boolean category|Boolean]], then it is an elementary topos, the principle of excluded middle is true, and $S$ has two elements and is isomorphic to $\Omega$, so the pretopos is no longer predicative, and this definition reduces to the classical definition. 

Since $S$ as defined above for Dedekind reals is a countable set, one could replace $S$ with $N$ itself, as $N$ is also countable. The continuum hypothesis then becomes that if there is a series of monomorphisms such that 

$$N \hookrightarrow A\hookrightarrow N^N$$

then there exists a monomorphism $A \hookrightarrow N$ or a monomorphism $N^N \hookrightarrow A$.

The set $N^N$ is typically called the [[Baire space of sequences]], and sometimes called the Baire real numbers in [[descriptive set theory]] and denoted as $B$. In constructive mathematics, there is an [[homeomorphism]] between $N^N$ and the set of positive [[irrational numbers]] $J$ through infinite [[continued fractions]]. 

Finally, one could construct the [[unit interval]] [[continuum]] as the [[terminal coalgebra of the endofunctor]] $F(X) = X \times 2 + 1$ on [[Set]], the [[stream]] $2_*$. Since the [[initial algebra]] of the endofunctor $F(X) = X \times 2 + 1$ is the [[free monoid]] $2^*$ and has countable cardinality, the continuum hypothesis then be written as that if there is a series of monomorphisms such that 

$$2^* \hookrightarrow A\hookrightarrow 2_*$$

then there exists a monomorphism $A \hookrightarrow 2^*$ or a monomorphism $2_* \hookrightarrow A$. This last definition is important in situations where [[internal hom-objects]] do not exist in the ambient category, such as in the pretopos [[Set]] of strongly predicative mathematics. 

### In strongly predicative mathematics
If neither power sets nor function sets exist, such as in a Boolean or Heyting [[pretopos|W-pretopos]], the mathematics is strongly predicative and the cardinality of the continuum is an [[inaccessible cardinal]]. Then, classically, the continuum hypothesis becomes the question of whether there is a cardinal between the inaccessible cardinal $\aleph_0$ and the inaccessible cardinal $\mathfrak{c}$. 

While the set of real numbers could be defined by fiat as the [[terminal object|terminal]] [[archimedean field]] object $R$ in $Set$, its existence has to be included as an axiom of the set theory, after which the continuum hypothesis becomes if there is a series of monomorphisms such that 

$$N \hookrightarrow A\hookrightarrow R$$

then either there exists a monomorphism $A \hookrightarrow N$ or a monomorphism $R \hookrightarrow A$. One could likewise assert by fiat the existence of free monoids and streams on a finite set, whereby the continuum hypothesis follows from above. 

## Unprovability

+-- {: .num_theorem}
###### Theorem

There exists a [[boolean topos]] in which the [[axiom of choice]] holds and the continuum hypothesis fails.

=--

One topos for which the theorem holds is called the *Cohen topos*; it is the topos of sheaves with respect to the [[dense topology]] (also called the $\neg\neg$-topology) on the Cohen [[poset]].  Thus, in this topos, there exist monomorphisms $\mathbb{N} \hookrightarrow A\hookrightarrow 2^{\mathbb{N}}$ but no monomorphism $A \hookrightarrow N$ or $\Omega^N \hookrightarrow A$..

The Cohen topos will be constructed from the topos [[Set]] of sets.  For this, recall that the subobject classifier of $Set$ is $2\coloneqq \{0,1\}$. The technique of constructing such a topos is called [[forcing]].
 
+-- {: .num_defn}
###### Definition
**(Cohen poset)**

Let $\mathbb{N}$ be the set of natural numbers; i.e. the [[natural numbers object]] in $Set$. Let $A$ be a set with strictly larger cardinality ${|A|}\gt {|\mathbb{N}|}$; e.g. $A\coloneqq 2^{2^{\mathbb{N}}}$ will do because of the [[diagonal argument]].  Then the *Cohen poset* $P$ is defined to be the set of morphisms

$$p:F_p\to 2$$

where $F_p\subseteq A\times \mathbb{N}$ is any [[finite set|finite]] subset.
The order relation on $P$ is defined by

$$q\le p\; iff\; F_q\supseteq F_p\;and\;q|_{F_p}=p$$

where the right-hand condition means that $q$ restricted to $F_p$ must coincide with $p$.
=--

We think of each element of $P$ as an approximation to the function $F:A\times\mathbb{N}$ that is the [[exponential|transpose]] of the putative monomorphism

$$f:A\to 2^\mathbb{N}$$

with "smaller" elements considered as better approximations. The very rough intuition is that $p\to q\to \dots$ (if $p\ge q \ge \dots$) forms a [[codirected diagram]] of monomorphisms with domains of increasing size whose colimit is $f$, and that by [[free cocompletion]] (i.e. forming (pre)sheaves) we obtain a topos in which this colimit exists.


+-- {: .num_lemma}
###### Lemma
The [[dense topology|dense]] [[Grothendieck topology]] on $P$ is [[subcanonical topology|subcanonical]].  In other words: For any $p\in P$ we have $y(p)=hom(-,p)\in\Sh(P,\neg\neg)$ 
=--

+-- {: .num_lemma}
###### Lemma
Let $k_{A\times\mathbb{N}}:\begin{cases}P\to Set \\ p \mapsto A\times\mathbb{N}\end{cases}$ denote the functor constant on $A\times\mathbb{N}$. Let

$$C:\begin{cases}
P\to Set
\\
p\mapsto \{(b,n)|p(b,n)=0\}\subseteq A\times \mathbb{N}
\end{cases}$$

Then we have ${\neg}{\neg} C=C$ in $Sub(k_{A\times\mathbb{N}})$; i.e. $C$ is a closed subobject with respect to the dense topology ${\neg}{\neg}$ in the [[algebra of subobjects]] of $k_{A\times\mathbb{N}}$.
=--

Let $\Omega$ denote the [[subobject classifier]] of $Psh(P)$. Let $\Omega_{{\neg}{\neg}}$ denote the subobject classifier of $Sh(P,\neg\neg)$. Recall that $\Omega_{{\neg}{\neg}}$ is given by the equalizer $\Omega_{{\neg}{\neg}}=eq(id_\Omega,{\neg}{\neg})$.

By the preceding lemma, the [[characteristic morphism]] $\chi_a$ of the subobject $a \colon C\hookrightarrow k_{A\times\mathbb{N}}=k_A\times\k_\mathbb{N}$ factors through some $f \colon k_{A\times\mathbb{N}}\to \Omega_{\neg\neg}$.

+-- {: .num_lemma}
###### Lemma 
The adjoint $g:k_A\to \Omega_{{\neg}{\neg}}^{k_{\mathbb{N}}}$ of $f$ is a monomorphism.
=--

+-- {: .num_corollary}
###### Corollary
The associated-sheaf functor sends $g$ to a monomorphism in the Cohen topos.
=--

## Unrefutability

If $V$ is a model of [[ZF]], then the continuum hypothesis and the [[axiom of choice]] both hold in G&#246;del's [[constructible universe]] $L$ built from $V$. Actually, the GCH holds in $L$ as well. 

+-- {: .num_remark #GCHinZF} 
###### Remark 
Regarding the statement of the *generalized* continuum hypothesis in *ZF* (not ZFC), one should distinguish various possibilities. One might leave the statement $2^{\aleph_n} = \aleph_{n+1}$ unchanged, so that the GCH becomes a statement just about ordinals or well-ordered sets. But then one could argue such a generalized continuum hypothesis is not as general or strong as it might be, since not all sets can be well-ordered using ZF alone. The more general statement would say that if there are monomorphisms $X \to Y$ and $Y \to P(X)$ for infinite sets $X$ and $Y$, then $Y$ is bijective with one of $X, P(X)$. 

For example, Sierpi&#324;ski proved that over ZF, the generalized continuum hypothesis implies AC. (See [[Hartogs number]].) For this result, he certainly used the stronger formulation. 

In weakly predicative mathematics, power sets do not exist, so the stronger version of the continuum hypothesis for Dedekind real numbers would have to be rephrased in terms of the Sierpinski space $\mathbb{S}$ and function sets: if there are monomorphisms $X \to Y$ and $Y \to \mathbb{S}^X$ for infinite sets $X$ and $Y$, then $Y$ is bijective with one of $X, \mathbb{S}^X$, or equivalently the version involving natural numbers and function sets: if there are monomorphisms $X \to Y$ and $Y \to \mathbb{N}^X$ for infinite sets $X$ and $Y$, then $Y$ is bijective with one of $X, \mathbb{N}^X$. 
=-- 

## Generalization: Easton's theorem 
 {#EastonTheorem}

Just how flexible can the power [[operation]] $\kappa \mapsto 2^\kappa$ be? There are of course some constraints. Obvious ones are that $\kappa \lt 2^\kappa$ and $2^\kappa \leq 2^\lambda$ whenever $\kappa \leq \lambda$. A more refined one is a consequence of [[König's theorem]], namely that 

* $\kappa \lt cof(2^\kappa)$ 

where the right side is the [[cofinality]] of $2^\kappa$. 

A remarkable illustration of the power of the forcing method is [[Easton's theorem]], which says that as far as [[regular cardinals]] go, these are really the *only* constraints. 

+-- {: .num_theorem} 
###### Theorem 
**([Easton 70](#Easton70))** 

Suppose $\mathcal{M}$ is a [[model]] of [[ZFC]] in which the generalized continuum hypothesis (GCH) holds. Let $F$ be a [[partial function]] from the class of infinite [[regular cardinals]] to the class of [[cardinals]] such that 

* $F$ is strictly increasing and preserves the order $\leq$; 

* $\kappa$ is less than the cofinality of $F(\kappa)$ for all $\kappa \in dom(F)$. 

Then there is a generic extension $\mathcal{M}[G]$ of $\mathcal{M}$ with the same cardinals and cofinalities, such that $\mathcal{M}[G] \models 2^\kappa = F(\kappa)$ for all $\kappa \in dom(F)$. 
=-- 

On the other hand, the behavior of the power operation on [[regular cardinal|singular cardinals]] is not so unconstrained. For example, in a model of ZFC, the smallest cardinal for which GCH fails can never be singular. The so-called "[[pcf theory]]" (or "possible cofinalities theory"), due to [[Saharon Shelah]], gives some information on possible bounds for the power operation on singular cardinals (among other things). 

## Links

* Stanford Encyclopedia of Philosophy, _[The Continuum Hypothesis](http://plato.stanford.edu/entries/continuum-hypothesis/)_

* MO _Solutions to the Continuum Hypothesis_ . ([link](http://mathoverflow.net/questions/23829/solutions-to-the-continuum-hypothesis))

## References

* [[John Bell|J. L. Bell]], _Set Theory - Boolean-Valued Models and Independence Proofs_ , Oxford Logic Guides **47** 3rd ed. Oxford UP 2005.

* [[Alonzo Church|A. Church]], _Paul J. Cohen and the Continuum Problem_, pp.15-20 in Proceedings ICM Moscow 1966. ([pdf](http://www.mathunion.org/ICM/ICM1966.1/Main/icm1966.1.0015.0020.ocr.pdf))

* [[Paul J. Cohen|P. J. Cohen]], _The independence of the continuum hypothesis I_, Proc. Nat. Acad. Sci. **50** (1963) pp.1143-1148. ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC221287/pdf/pnas00240-0135.pdf))

* [[Paul J. Cohen|P. J. Cohen]], _The independence of the continuum hypothesis II_, Proc. Nat. Acad. Sci. **51** (1963) pp.105-110. ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC300611/pdf/pnas00175-0117.pdf))

* [[Paul J. Cohen|P. J. Cohen]], _Set Theory and the Continuum Hypothesis_ , Benjamin New York 1966. (Dover reprint 2008)

* [[Patrick Dehornoy|P. Dehornoy]], _Progr&#232;s r&#233;cents sur l'hypoth&#232;se du continu (d'apr&#232;s Woodin)_ , S&#233;minaire Bourbaki expos&#233; **915** (2003). ([English version](http://www.math.unicaen.fr/~dehornoy/Surveys/DgtUS.pdf))

* {#Feferman11}[[Solomon Feferman]], _The Continuum Hypothesis is neither a definite mathematical problem nor a definite logical problem_ , Harvard lectures 2011. ([pdf](http://math.stanford.edu/~feferman/papers/CH_is_Indefinite.pdf))

* {#Hamkins12} [[Joel David Hamkins]], *The set-theoretic multiverse*, Review of Symbolic Logic 5:416-449 (2012), [arxiv](https://arxiv.org/abs/1108.4223)

* M.C. Fitting, _Intuitionistic Logic, Model Theory and Forcing_, North-Holland Amsterdam 1969. 

* {#Goedel47}[[K. Gödel]], _What is Cantor's continuum problem?_ , Am. Math. Monthly **54** no. 9 (1947) pp.515-25. ([pdf](http://www.personal.psu.edu/ecb5/Courses/M475W/Readings/Week06-Sep30-IntoTheTwentiethCentury/01-WhatisCantorsContinuumProblembyKurtGodel.pdf))

* {#Lawvere03} [[William Lawvere|F. W. Lawvere]], _Foundations and Applications: Axiomatization and Education_, Bulletin of Symbolic Logic **9** no.2 (2003) pp.213-224. ([ps-preprint](https://www.math.ucla.edu/~asl/bsl/0902/0902-006.ps))

* [[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994. (sections VI.2, VI.3)

* [[W. Hugh Woodin]], _The Continuum Hypothesis, Part I_ , Notices AMS **48** no.6 (2001) pp.567-576. ([pdf](http://www.ams.org/notices/200106/fea-woodin.pdf))

* [[W. Hugh Woodin]], _The Continuum Hypothesis, Part II_ , Notices AMS **48** no.7 (2001) pp.681-690. ([pdf](http://www.ams.org/notices/200107/fea-woodin.pdf))

* {#Easton70} W. Easton, _Powers of regular cardinals_, Ann. Math. Logic, 1 (2): 139&#8211;178, (1970) [doi:10.1016/0003-4843(70)90012-4](https://dx.doi.org/10.1016%2F0003-4843%2870%2990012-4) 

A [[formal proof]] of the independence of the continuum hypothesis from [[ZFC]] is in 

* {#Han18} [[Jesse Han]], _Flypitch project -- Formal proof of the independence of CH_ ([github:flypitch](https://github.com/flypitch), [pdf](https://github.com/flypitch/flypitch-notes/blob/master/forcing-notes.pdf))

published as

* {#HanvanDoorn20} [[Jesse Han|Jesse Michael Han]] and [[Floris van Doorn]],  _A Formal Proof of the Independence of the Continuum Hypothesis_, Proceedings of the 9th ACM SIGPLAN International Conference on Certified Programs and Proofs (2020) pp 353–366, doi:[https://doi.org/10.1145/3372885.3373826](https://doi.org/10.1145/3372885.3373826), arXiv:[2102.02901](https://arxiv.org/abs/2102.02901).

[[!redirects CH]]
[[!redirects Continuum hypothesis]]
[[!redirects GCH]]
[[!redirects generalized continuum hypothesis]]

[[!redirects Easton's theorem]]
[[!redirects Easton theorem]]
