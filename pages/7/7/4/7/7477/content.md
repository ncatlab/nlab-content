
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **completely distributive lattice** is a [[complete lattice]] $L$ in which arbitrary [[joins]] and arbitrary meets [[distributive lattice|distribute]] over each other. 

More formally: given a complete lattice $L$ and functions $p: J \to I$ and $f: J \to L$, we have 

$$\bigwedge_{i \in I} \bigvee_{j \in p^{-1}(i)} f(j) \geq \bigvee_{sections\; s: I \to J} \bigwedge_{i \in I} f(s(i))$$ 

where "section" means [[section]] of $p$. Complete distributivity states that this inequality is an equality, for all $f, p$. The same statement then holds upon switching $\bigwedge$ and $\bigvee$, i.e., complete distributivity is a [[duality|self-dual]] property. 

## Properties

### Algebraic lattices

+-- {: .num_prop}
###### Proposition

The category of [[Alexandroff locales]] is equivalent to that of completely distributive [[algebraic lattice|algebraic lattices]]. 
=--

This appears as remark 4.3 in ([Caramello 2011](#Caramello11)).

### Completely distributive Boolean algebras 

+-- {: .num_lemma} 
###### Lemma 
A complete totally ordered poset is completely distributive. 
=-- 

+-- {: .proof} 
###### Proof 
(Note: this uses the [[axiom of choice]].) Suppose we had a strict inequality 

$$\bigwedge_{i \in I} \bigvee_{j \in p^{-1}(i)} f(j) \gt \bigvee_{sections\; s: I \to J} \bigwedge_{i \in I} f(s(i)).$$ 

Denote the left side by $x$ and the right by $y$. Either there is no element $z$ strictly between $x$ and $y$, or there is. In the former case, we have for each $i$ that $\bigvee_{j \in p^{-1}(i)} f(j) \geq x$, and so (using trichotomy) we have $f(j) \gt y$ for some $j \in p^{-1}(i)$. Choosing such a $j$ for each $i$, we obtain a section $s$ with $f(s(i)) \gt y$ for all $y$, whence $f(s(i)) \geq x$ for this case, so that $\bigvee_{sections\; s: I \to J} \bigwedge_{i \in I} f(s(i)) \geq x \gt y$, contradiction. If there is $z$ with $x \gt z \gt y$, we argue similarly to obtain a section $s$ with $f(s(i)) \gt z$ for all $i$, whence $\bigwedge_{i \in I} f(s(i)) \geq z$, and we obtain a contradiction as before with $z$ replacing $x$. 
=-- 

+-- {: .num_prop} 
###### Proposition 
A complete Boolean algebra $B$ is completely distributive iff it is atomic (a [[CABA]]), i.e., is a [[power set]] as a Boolean algebra. 
=-- 

+-- {: .proof} 
###### Proof 
For a complete atomic Boolean algebra $B$, it is classical that the canonical map $B \to P(atoms(B))$, sending each $b \in B$ to the set of [[atoms]] below it, is an isomorphism. Such [[power sets]] are products of copies of $\mathbf{2} = \{0 \leq 1\}$, which is completely distributive by the lemma, and [[products]] of completely distributive lattices are completely distributive. 

In the other direction, suppose $B$ is completely distributive. Take $p = \pi_2: \mathbf{2} \times B \to B$, and $\alpha: \mathbf{2} \times B \to B$ by $\alpha(0, b) \coloneqq \neg b$ and $\alpha(1, b) \coloneqq b$. Sections of $p$ correspond to functions $g: B \to \mathbf{2}$, and so complete distributivity gives 

$$1 = \bigwedge_{b \in B} (b \vee \neg b) = \bigvee_{g: B \to \mathbf{2}} \bigwedge_{b \in B} \alpha(g(b), b).$$ 

Write $a(g)$ as abbreviation for $\bigwedge_{b \in B} \alpha(g(b), b)$, we have 

$$b = b \wedge 1 = b \wedge \bigvee_{g: B \to \mathbf{2}} a(g) = \bigvee_{g: B \to \mathbf{2}} b \wedge a(g)$$ 

so $b \wedge a(g) \neq 0$ for some $g$ if $b \neq 0$. Notice that $b \wedge a(g) \neq 0$ implies $g(b) = 1$, from which we infer two things: 

* Whenever $b \leq a(g)$ with $b \neq 0$, then $a(g) \leq \alpha(g(b), b) = \alpha(1, b) = b$; therefore $a(g)$ is an atom whenever $a(g) \neq 0$; 

* Provided that $b \wedge a(g) \neq 0$, the preceding point gives that $a(g)$ is an atom below $b \wedge a(g) \leq b$. 

The last point shows every element $b$ has an atom $a(g)$ below it, so that $B$ is atomic, as was to be shown. 
=-- 


### Constructive complete distributivity

A complete lattice $A$ is called **constructively completely distributive** (CCD) if the join-assigning morphism $D A \to A$ has a left adjoint, with $D A$ the poset of [[downsets]]. 

_Constructive complete distributivity is equivalent to complete distributivity if and only if the [[axiom of choice]] holds_ ([Wood&Fawcett (1990)](#WoodFawcett)).

Constructively completely distributive lattices are an example of [[continuous algebras]] for a [[lax-idempotent 2-monad]].

### Remark

Completely distributive lattices correspond to tight [[Galois connections]] (Raney 1953). This generalizes to a correspondence between totally distributive toposes and [[essential geometric morphism|essential localizations]] (Lucyshyn-Wright 2011).

CCD lattices are precisely the [[nuclear objects]] in the category of complete lattices. 

The (bi-) category $\mathfrak{CCD}$ with CCD lattices and sup-preserving maps is the [[Karoubi envelope|idempotent splitting]] of the (bi-) category of relations $\mathfrak{Rel}$. This plays an important role in _[[domain]]-theoretical_ approaches to the semantics of [[linear logic]].

## Related concepts

* [[continuous lattice]]

* [[totally distributive category]]

## Links

* wikipedia-entry: [completely distributive lattice](http://en.wikipedia.org/wiki/Completely_distributive_lattice)

## References

* [[Olivia Caramello]], _A topos-theoretic approach to Stone-type dualities_  , ms. 2011. ([arXiv:1103.3493](http://arxiv.org/abs/1103.3493))
 {#Caramello11}

* {#WoodFawcett} [[Barry Fawcett]], [[Richard J. Wood]], *Constructive complete distributivity I* , Math. Proc. Camb. Phil. Soc. **107** (1990) 81-89 &lbrack;[doi:10.1017/S0305004100068377](https://doi.org/10.1017/S0305004100068377)&rbrack;
 

* R. Guitart, J. Riguet, _Enveloppe Karoubienne de Cat&#233;gories de Kleisli_ , Cah. Top. Geom. Diff. Cat. **XXXIII** no.3 (1992) pp.261-266. ([pdf](http://archive.numdam.org/article/CTGDC_1992__33_3_261_0.pdf))

* {#LW11}[[Rory Lucyshyn-Wright|R. Lucyshyn-Wright]], _Totally Distributive Toposes_ , arXiv.1108.4032 (2011). ([pdf](http://arxiv.org/pdf/1108.4032v3))

* G. N. Raney, _Tight Galois Connections and Complete Distributivity_ , Trans.Amer.Math.Soc **97** (1960) pp.418-426. ([pdf](http://www.ams.org/journals/tran/1960-097-03/S0002-9947-1960-0120171-3/S0002-9947-1960-0120171-3.pdf))

* R. Rosebrugh, R. J. Wood, _Constructive complete distributivity IV_ , App. Cat. Struc. **2** (1994) pp.119-144. ([preprint](http://www.mta.ca/~rrosebru/articles/ccd4.pdf))

* [[Isar Stubbe|I. Stubbe]], _Towards "Dynamic Domains": Totally Continuous Complete Q-Categories_ , Theo. Comp. Sci. **373** no.1-2 (2007) pp.142-160.

[[!redirects completely distributive lattices]]
[[!redirects constructive completely distributive lattice]]
[[!redirects constructively completely distributive lattice]]
[[!redirects constructively completely distributive lattices]]
[[!redirects constructive completely distributive lattices]]
[[!redirects CCD lattice]]