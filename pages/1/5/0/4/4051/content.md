+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Introduction 

This page addresses a frequently voiced but easily corrected misconception about [categorial](http://ncatlab.org/nlab/show/foundation+of+mathematics#CFM) approaches to [[foundations of mathematics]], namely that there is a logical circularity in using [[category theory]] to give an axiomatic [[set theory]] (such as [[ETCS]]), since categories themselves are [[sets]] (or collections) with extra [[structure]]. 

The most straightforward response is a formalist one: category theory and various elaborations like [[ETCS]] are [[first-order theories]], just as [[ZFC]] is. One doesn't need a theory of sets prior to a theory of categories, any more than one needs a theory of sets prior to a theory of sets. Fully formalized, ETCS makes no mention of sets, only a [[signature]] and a list of [[axioms]]; the only background is [[predicate logic|first-order logic]] (which gives the rules for deducing theorems). All of these remarks are perfectly obvious, but the misunderstanding above is common enough that working out the details of full formalization and recording them might be a useful exercise, and that is what we carry out here. 

### Choices in presentation 

While we're at it, however, we should also point out features of categorical set theory which distinguish it from traditional forms of set theory such as ZFC. Conceptually and philosophically, there is a big difference in that ZFC emphasizes membership between sets as the basic relation (founded on the idea that elements can themselves have elements), whereas in ETCS elements of sets are intuited as essentially featureless (sets being "bags of dots" so to speak, where elements are distinguishable but have no internal structure), and the emphasis is rather on mappings and patterns of mappings where mathematically relevant structure resides. 

These conceptual distinctions are discussed more fully elsewhere in the nLab; see for example [[structural set theory]] and pages and references linked therein. Our focus in this page will be on more formalist concerns, but even after disengaging from possibly contentious philosophical issues, experience has shown that logicians not familiar with the categorical background might easily misunderstand what we are doing and why we make the choices we do, and worse, deride those choices from lack of understanding. We thus feel some advance explanation might be of some benefit. 

#### Choosing sequent calculus 

Even if we restrict focus to formal aspects, there are notable differences between axioms of ETCS and axioms of ZFC in terms of the strength of the underlying logic needed to express them, or in terms of what [internal logical](http://ncatlab.org/nlab/show/internal+logic#kinds_of_internal_logics_in_different_categories_20) assumptions are needed on a background environment in which to interpret them. The relevant distinctions between different types of internal theories (e.g., finite limit theories, coherent theories, etc.) is often conveniently expressed via a [[sequent calculus]]-style presentation of first-order logic that is common currency among categorical logicians, and that is the mode we will adopt here. 

When we write a sequent $\varphi \vdash \psi$, it is understood that predicates $\varphi$, $\psi$ have the same type (we could write $\varphi \vdash_X \psi$ to indicate that $\varphi$ and $\psi$ are both of type $X$). Roughly speaking, this means they have the same free variables, although if we see a sequent of the form 

$$\varphi(x, y) \vdash \psi(x)$$ 

where a free variable $y$ does not appear explicitly, then we can match up the types by adding it in freely, replacing $\psi(x)$ by $\psi(x) \wedge [y = y]$. This replacement process corresponds to a "substitution" operation in a [[hyperdoctrine]], a way of doing categorical logic. In fact, a sequent calculus gives rise to a functor 

$$Pred: Types^{op} \to Preord$$ 

taking each type $X$ to the set of predicates of that type, preordered by the entailment relation $\vdash_X$, and where $Pred(f)$ is a substitution map of preorders for each map $f: X \to Y$ between types. Composing with the posetal reflection $Preord \to Pos$ gives a hyperdoctrine 

$$Types^{op} \to \Pos$$ 

which plays the role of a Lindenbaum algebra. Thus the close connection between sequent calculus presentations and the sorts of hyperdoctrine presentations that have proved effective in categorical logic. 

In a categorical semantics of a sequent calculus, we have a category of types 
$C$ and a hyperdoctrine $Sub: C^{op} \to Pos$ that assigns to each object $c$ its subobject lattice, and a map between hyperdoctrines $Pred \to Sub$. Thus each formula represents a subobject (of an object represented by the formula's type), and a sequent represents an inclusion between subobjects. Logical operations represent categorical operations on subobject lattices in a natural way in the semantics of sequent calculus, e.g., $\exists$ represents taking the image of a subobject along a map, and $\wedge$ represents intersections of subobjects. 

#### Choosing the multiplicity of predicates 

In addition, there are different choices of signature in which one might present a theory. Our own choices of signature are driven by the desire to have the model theorist's notion of homomorphism match the category theorist's notion of morphism appropriate for a given situation. For example: it is possible to define a monoid as a structure consisting of a associative binary operation $m$ for which a two-sided identity element _exists_ (so the signature of the theory of monoids consists of just a binary function symbol $m$); one can then prove the identity is unique. However, homomorphisms of models of this theory, under this signature, need not preserve the identity; if we want identities to be preserved, then a constant for the identity needs to be explicitly added to the signature. In the same way, one _could_ define a category by recourse to a single ternary relation $c(f, g, h)$ whose intended interpretation is that $f$ and $g$ are composable morphisms such that $f \circ g = h$, and add axioms stipulating existence of identities, but then homomorphisms fail to be functors. 

Likewise, if we are presenting a theory of finitely complete categories, then it is not enough to say they are categories for which finite limits exist: if we want the relevant homomorphisms of models of the theory to be functors that preserve finite limits, then appropriate predicates for finite limits (e.g., for pullbacks and terminal objects) need to be adjoined to the signature. And so on. Note that such requirements add (slightly) to the length of the presentation, but we regard that as a superficial consideration -- it is more important to have the signature and axioms reflect the correct notion of homomorphism for each layer of structure. 

#### Whether on-the-nose or up to isomorphism? 

A final consideration is whether we want a categorical set theory to have _chosen_ products, _chosen_ power objects, etc. or we want such structures to be uniquely given only up to isomorphism. The prevailing tendency among category theorists is to go with the latter; if we want to reflect that practice, then the signature ought to be relational; for example, we might have a ternary predicate $prod(a, b, c)$ which says $c$ is _a_ product of objects $a$ and $b$, rather than have a binary function $a \times b$ which specifies _the_ product. 

The present author (Todd Trimble) feels the difference isn't such a big deal; while choosing particular products, pullbacks, power objects, etc. as part of the structure might not seem "natural", such strict or rigid structure is basically harmless. This observation can be formalized in terms of suitable equivalences (in much the same way that while monoidal categories and monoidal functors occur more often in nature, there are strictification 2-functors which allow for them to be formally and equivalently replaced by strict monoidal categories and strict monoidal functors). There are in fact benefits to working with strict structures because they can be expressed in very weak fragments of logic. For example, the theory of strict toposes is a finite limit theory (it is finitary-algebraic over the category of directed graphs), meaning the notion of strict topos object can be internalized within any finitely complete category. 

Thus, we will present fragments of the theory ETCS along two parallel tracks, one being with structure considered only up to isomorphism (expressed in a coherent theory), and the other involving specific choices of structure (expressed in a finite limit theory). That will bring us up to the theory of toposes with a natural numbers object. This in itself is a reasonable notion of category of sets; to use words of Lawvere, we can view it as a categorical theory of "variable sets". 

Two further axioms are adjoined to the theory of toposes with NNO to get ETCS (bringing one closer to a category of Zermelo sets; to use words of Lawvere, ETCS is a categorical theory of "constant sets"): the axiom of choice and the axiom of well-pointedness. These axioms are non-algebraic axioms that take us outside of finite limit logic: the axiom of choice is manifestly written in coherent logic, and the well-pointedness axiom is not even coherent (although ETCS can, via "Morleyization", be rewritten in coherent logic if excluded middle is assumed in the meta-logic). 

### Layering ETCS 

ETCS as presented here is built up in stages: 

* The theory of categories, as a one-sorted theory. (The usual presentation involves two sorts, objects and  morphisms. Our excuse is that many introductions to logic do not discuss any except one-sorted theories -- thus these are more familiar to logical novices, the very ones subject to the misconceptions recounted above.) In a morphisms-only approach, we have "source" and "target" operations and a ternary predicate $c(f, g, h)$, meaning "$f$ and $g$ are composable and their composite is $h$". 

* The theory of categories with finite limits. This builds on the previous theory and adds some new predicates, namely an unary predicate $1$ where $1(x)$ means "$x$ is terminal", and a quaternary predicate $p$ where $p(f, g, h, k)$ means "$f$, $g$, $h$, $k$ are the arrows of a pullback square". 

* The theory of toposes with a [[natural numbers object]] (NNO). Here we add in still more predicates to capture the notion of power object up to isomorphism. 

* The theory of toposes with NNO that are well-pointed (terminal objects are generators) and satisfy AC (every epi has a section).  

The sections below reflect this multi-stage approach. 

## Preliminaries 

We assume familiarity with the standard notion of a [[algebraic theory|(finitary) first-order theory]] with equality; this includes the standard rules of deduction in the Gentzen [[sequent calculus]] for first-order logic[^note2]. 

First-order [[theory|theories]] are typically presented in terms of a [[signature]] consisting of function and predicate symbols, together with axioms each of which is a closed formula in the first-order language generated by the signature. That mode of presentation will be followed here. Standard logical conventions are followed; for example, it is common to state axioms as formulas $P(x_1, \ldots, x_n)$ in which some of the variables $x_i$ may appear freely, with the implicit understanding that such variables are bound by unwritten [[universal quantifiers]] at the heads of formulas, to make the formulas closed. 

To make the exposition more readable, we add some explanations (in parentheses) which do not belong to the formal theory, but which may aid comprehension. We also employ the standard device of abbreviating formulas, by declaring at various junctures definitions and notational conventions. 

In formalizing universal properties, one very helpful purely logical abbreviation is the "exists-unique" quantifier $\exists !$. Namely, if $Q(x)$ is a formula in which a variable $x$ appears freely, then $\exists ! x: Q(x)$ is shorthand for the conjunction of 

$$(\exists_x Q(x))$$ \wedge 

$$\,$$

$$Q(x) = Q(y) \vdash x = y$$

## The theory of categories 

+-- {: .un_def}
###### Definition

We define the [[theory]] $Th(Cat)$ of [[categories]].

The [[signature]] of $Th(Cat)$ consists of 

* Unary function symbols $s$, $t$; 

* A ternary predicate $c$. 

(The [[theory]] of [[categories]] is commonly presented as a two-sorted theory, with an object sort and a morphism sort. Here we instead use [[single-sorted definition of a category|the single-sorted theory]], whose terms are to be interpreted as _morphisms_ of a category. We generally use letters $f, g, h, \ldots$ for variable terms. If $e$ is any term, then the intended interpretation of $s(e)$ is: the identity morphism of the domain of $e$. Similarly, $t(e)$ means the identity morphism of the codomain of $e$. The intended interpretation of $c(f, g, h)$ is that $h = f \circ g$.) 

The axioms of $Th(Cat)$ are as follows:  

1. $\vdash (s s(f) = s(f) = t s (f)) \wedge (t t(f) = t(f) = s t(f))$. 

1. $c(f, g, h) \vdash (s(f) = t(g) \wedge t(f) = t(h) \wedge s(g) = s(h))$

1. $s(f) = t(g) \vdash \exists !_h c(f, g, h)$

1. ([[identity|Identity]] laws) $\vdash c(f, s(f), f) \wedge c(t(f), f, f)$

1. ([[associativity|Associativity]]) $(c(f, g, j) \wedge c(g, h, k)) \vdash (c(j, h, m) \Leftrightarrow c(f, k, m))$

(Notice that an **object-term** may be defined as a term $e$ for which either of the following equivalent equations holds: $e = s(e)$, $e = t(e)$.) 


=--


## The theory of finitely complete categories

+-- {: .un_def}
###### Definition

We define the [[theory]] $Th(Lex)$ of [[finitely complete categories]].

(The axioms say there is a [[terminal object]] $1$, and a [[pullback]] for each pair $f, g$ with common target.) 

The axioms of $Th(Lex)$ are the axioms of $Th(Cat)$ plus the following: 

1. $\exists_1 (1 = s(1)) \wedge (\forall_f (f = s(f)) \Rightarrow 
(\exists ! g: (s(g) = f \wedge t(g) = 1))$

1. (Pullbacks exist) Define $p(f, g, h, k)$ to be the conjunction of the formulas  
$$(\exists_j c(f, h, j) \wedge c(g, k, j))$$
$$\,$$
$$(\exists_{j'} (c(f, h', j') \wedge c(g, k', j')) \Rightarrow (\exists ! i: (c(h, i, h') \wedge c(k, i, k')))$$ 
Then   
$$t(f) = t(g) \vdash \exists_h \exists_k p(f, g, h, k)$$

=-- 

## The theory of elementary toposes 

+-- {: .un_def}
###### Definition

We define the [[theory]] $Th(Topos)$ of [[elementary toposes]].

The signature of $Th(Topos)$ is obtained by adding to the signature of $Th(Lex)$ unary function symbols $P, \lambda, \rho$. 

(The intended interpretation is that $P(f: X \to Y)$ is the [[power object]] of $Y$, and $\langle \lambda(Y), \rho(Y) \rangle: E(Y) \hookrightarrow P(Y) \times Y$ is the elementhood relation, which we rewrite as a jointly [[monomorphism|monic]] [[span]], and consider as a [[universal property|universal]] relation from $P(Y)$ to $Y$.) 

The axioms of $Th(Topos)$ are obtained by adjoining to $Th(Lex)$ the following further axioms. In what follows, $M(f, g)$ denote the following formula in $Th(Cat)$:

$$s(f) = s(g) \wedge (\forall_{h, i, j, k} (c(f, h, j) \wedge c(f, i, j) \wedge c(g, h, k) \wedge c(g, i, k)) \Rightarrow h = i)$$

($M(f, g)$ means that the pair $(f, g)$ is a jointly monic span, aka a relation. In other words, that $\langle f, g \rangle \colon s(f) \to t(f) \times t(g)$ is monic, and $(f, g)$ form a relation between $t(f)$ and $t(g)$.) 

1. ($P(f: X \to Y) = P(Y)$ is an object that depends only on the codomain of $f$, and $\lambda(f), \rho$ are morphisms that span between $P(Y)$ and $Y$, comprising a local elementhood relation) 
$$\vdash (P(f) = P(t(f)) = t(P(f)) = t(\lambda(f))) \wedge (t(\rho(f)) = t(f))$$ 

1. $\vdash M(\lambda(f), \rho(f))$

1. (Universal property of power objects) 
$$M(f, g) \vdash \exists ! h: \exists_k p(h, \lambda(f), g, k) \wedge c(\rho(f), k, f)$$ 

=--

## The theory ETCS 

+-- {: .un_def}
###### Definition

Finally, we define the [[theory]] $Th(ETCS)$: [[ETCS]].

The signature of $Th(ETCS)$ is obtained by adjoining to the signature of $Th(Topos)$ the following 

* Nullary function symbols (i.e., constants) $\mathbb{N}, 0, \sigma$. 

The axioms of $Th(ETCS)$ are obtained by adjoining to the axioms of $Th(Topos)$ the following further axioms: 

1. ([[well-pointed topos|Well-pointedness]]: equality of maps $x \to y$ is detected by points $1 \to x$) 
$$(s(f) = s(g) \wedge t(f) = t(g)) \vdash \forall_h (s(h) = 1 \wedge t(h) = s(f) \Rightarrow f \circ h = g \circ h) \Rightarrow f = g$$ 

1. ([[axiom of choice|Axiom of Choice]]: every epi $f$ admits a section $i$) 
$$(\forall_{g, h} (t(f) = s(g) = s(h) \;\wedge\; t(g) = t(h) \;\wedge\; g \circ f = h \circ f) \;\Rightarrow\; g = h) \vdash \exists_i (s(i) = t(f) \;\wedge\; t(i) = s(f) \;\wedge\; f \circ i = t(f))$$

1. ([[natural numbers object|Zero and successor]])
$$\vdash s(0) = 1 \wedge t(0) = \mathbb{N} = s(\sigma) = t(\sigma)$$

1. ([[natural numbers object|Recursion: existence]]) 
$$s(f) = 1 \wedge t(f) = s(g) = t(g) \vdash \exists_h (s(h) = \mathbb{N} \wedge t(h) = t(f) \wedge f = h \circ 0 \wedge h \circ \sigma = g \circ h)$$ 

1. (Recursion: uniqueness) 
$$(s(f) = \mathbb{N} = s(g) \wedge t(f) = t(g) \wedge f \circ 0 = g \circ 0 \wedge f \circ \sigma = g \circ \sigma) \vdash f = g$$


This completes the formal specification of $Th(ETCS)$. 

=--

## Remarks 

### On $Th(Cat)$ 

The theory of categories is usually presented as a two-sorted theory, where the sorts $O$ and $M$ are for objects and morphisms. 

Despite the length of the list of axioms, it should be noted that they generally have an extremely simple logical structure. Indeed, with some slight modification, the theory $Th(Topos)$ may be rewritten so that it becomes an [[essentially algebraic theory]], at least in the sense that the models of $Th(Topos)$ are categorially equivalent (as categories = models of $Th(Cat)$) to models of an essentially algebraic theory. That is to say, the notion of "topos" can be [[internalization|internalized]] in any category with finite limits; this is even true of toposes with natural numbers object. 

Hence, the only "irremovable" existential clauses (that necessitate passing from essentially algebraic logic to a larger fragment of first-order logic) are well-pointedness and the axiom of choice. The axiom of choice belongs to [[geometric logic]]. 

This is in marked contrast to ZFC, whose axiom list is superficially shorter (ignoring the fact that axiom schemas are technically infinite lists of axioms!) but whose logical complexity is much greater.

It must be added that this fully formal presentation masks much of the conceptual clarity afforded by the underlying categorical and structural insights that are actually at work, particularly the systematic use of universal mapping properties. To put it more sharply: the traditional syntactic machinery used to present first-order theories is not really a natural or well-adapted 'home' for presenting categorical theories such as ETCS. The natural mode of presentation would use diagrams of arrows from the outset, as formalized say by Freyd's [[Q-sequence]]s, and that is as fully formal as the more traditional mode adopted here, which after all goes back to Frege and hasn't changed in a century.


## References

Over the years various people at

* _Foundations of Mathematics_ [mailing list](http://www.math.psu.edu/simpson/fom/) (around 1998)
{#FOM}

have challenged [[category theory|category theorists]] to write down a fully formal presentation of ETCS.

note1: Note how cumbersome are the traditional "machine-level" logical scripts for expressing this theory, as opposed to the more visual and easily apprehended arrow-theoretic notations (which are just as rigorous). No doubt this was anticipated by those in the FOM debate who wished to portray categorical foundations in the worst possible light: traditional 1-dimensional logical notations tend to make the theory look as clumsy as possible!

note2: We use $\vdash$ to denote an entailment between formulas; axioms of our theory are written in the form $\Gamma \vdash P$ where $\Gamma$ is a finite, possibly empty list of formulas which provide the _context_ in which $P$ is asserted. Obviously one could eschew this symbol entirely, and instead give each axiom in the form of a single formula with appropriately embedded implication symbols $\Rightarrow$. But, as explained in this article, this would obscure the later point that large fragments of ETCS, in fact all axioms except well-pointedness, are manifestly expressible in _coherent logic_.

[[!redirects fully formal ETCS]]
[[!redirects fully formal definition of ETCS]]
