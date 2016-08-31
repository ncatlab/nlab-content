+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In the [[category of sets]], we have a bijective correspondence (up to isomorphism) between surjective functions on $X$ and equivalence relations on $X$, where a surjective function $\pi : X \to Y$ is taken to the equivalence relation $E_{\pi}$ gotten by pulling back the diagonal of $Y$, and an equivalence relation $E$ is taken to the function $f_E$ which projects $X$ onto the set of $E$-classes. If we replace [[Set]] with the category of definable sets $\mathbf{Def}(T)$ of a first-order theory $T$, this correspondence generally fails, because when $E$ is a definable equivalence relation, there may not be a corresponding definable $f_E$. That is to say, internal congruences in $\mathbf{Def}(T)$ are not generally effective.

## Definition ##

We say that:

1. $T$ has _uniform elimination of imaginaries_ if the above correspondence does hold, that is, if internal congruences in $\mathbf{Def}(T)$ are effective.

2. $T$ has _elimination of imaginaries_ if for every definable set $X = \{m \in \mathbb{M} \operatorname{ | } \varphi(m,b)\}$, there exists a formula $\psi(x,y)$ and a tuple $c$ with the same sort as $y$ such that $c$ uniquely satisfies $X = \{m \in M \operatorname{ | } \psi(m,c)\}.$

Inside a saturated model $\mathbb{M} \models T$, elimination of imaginaries is equivalent to the following statement: for every definable set $X$, there exists a tuple $c$ such that for all $\sigma \in \operatorname{Aut}(\mathbb{M})$, $\sigma(X) = X$ setwise if and only if $\sigma(c) = c$ pointwise. This is sometimes called the _coding of definable sets_.

Poizat noticed that $T$ having elimination of imaginaries allows one to develop a classical Galois theory classifying definably-closed extensions of small parameter sets in terms of the closed subgroups of a profinite automorphism group in any sufficiently saturated model of $T$.

The *imaginary elements* of a theory $T$ are precisely $E$-classes, where $E$ is a $0$-definable equivalence relation on $T$.

## The $(-)^{\operatorname{eq}}$ construction ##
In the process of inventing [[stability theory]], i.e. classifying theories according to the number of isomorphism classes of their models in each cardinality, Shelah found he needed to eliminate imaginaries in a universal way, so he found a way to conservatively interpret each theory $T$ in a theory $T^{\operatorname{eq}}$ which eliminated all the imaginaries of $T$. The process just involves throwing in for each congruence $E$ on $X$ a new sort ([[type]] in type theory) for $X/E$ and a projection map $X \twoheadrightarrow X/E$.

$T^{\operatorname{eq}}$ satisfies the following universal property: any theory which interprets $T$ and eliminates imaginaries must uniquely interpret $T^{\operatorname{eq}}$ as theories under $T$ (in the $2$-category of theories and interpretations.)

Makkai realized not long after that the $(-)^{\operatorname{eq}}$ construction corresponded to the [[pretopos completion]] of the [[syntactic category]] of $T$.

(Indeed, pretoposes are just toposes that might be missing some power objects. According to the next section, inside a Boolean pretopos these power objects will still be there, just generally only formally.)

## Relation to ind-representable power objects ##
If a first-order theory eliminates imaginaries, it interprets infinitely many constants. This is because it interprets at least two constants: a code for the diagonal relation and its complement. Taking binary sequences of these two constants in higher and higher Cartesian products of the model with itself produces infinitely many constants.

In particular, when $T$ eliminates imaginaries, its [[syntactic category]] has finite [[coproducts]]. In particular, $\mathbf{2}$ exists, and all definable subsets have definable classifying maps.

The following characterization is due to Moshe Kamensky, and can be found in his categorical internality paper.

**Proposition.** Let \(T\) be a first-order theory which interprets two constants. Then $T$ eliminates imaginaries if and only if for all $X$ and $Y$ in $\mathbf{Def}(T)$, the presheaf $Z \mapsto \operatorname{Hom}_{\mathbf{Def}(T)}(Z \times X, Y)$ is ind-representable.

_Proof._ Suppose first that the presheaves $Y^X \overset{\operatorname{df}}{=}Z \mapsto \operatorname{Hom}_{\mathbf{Def}(T)}(Z \times X,Y)$ are ind-representable. Let $E \overset{s}{\underset{t}{\rightrightarrows}} X$ be a definable equivalence relation on $X$. Let $\phi_E : X \times X \to 2$ classify $E \overset{(s,t)}{\hookrightarrow} X \times X$. Let $\mathbf{y} : \mathbf{Def}(T) \hookrightarrow \widehat{\mathbf{Def}(T)}$ be the Yoneda embedding. Then $\mathbf{y} \phi_E$ has a product-exponential transpose $\overline{\mathbf{y} \phi_E} : \mathbf{y}X \to 2^X$. The Yoneda lemma says that $\operatorname{Hom}_{\widehat{\mathbf{Def}(T)}}(\mathbf{y}X, 2^X) \simeq 2^X(X)$, and by assumption $2^X(X) \simeq \underset{\longrightarrow}{\lim}\operatorname{Hom}(X,J(i))$ for some $J : I \to \mathbf{Def}(T)$ a filtered diagram of definable sets. Since this is filtered, the colimit as a set can be computed as

$$\bigsqcup_{i \in I} J(i) / \sim,$$

where the equivalence relation $\sim$ identifies elements that are eventually sent to the same element by transition maps in the diagram. Hence, we can identify $\overline{\mathbf{y}\phi_E}$ with its equivalence class of maps $\{\phi_i : X \to J(i)\}_{i \in I}$. Now, $\mathbf{y}E$ is the kernel pair of $\overline{\mathbf{y} \phi_E}$ in $\widehat{\mathbf{Def}(T)}$, so $E = \bigvee_{i \in I} \ker(\phi_i)$. By compactness, we can replace $I$ with a finite subset $I_0 \subseteq I$. Since $I$ is filtered, there exists a weak coproduct $j$ to $I_0$. Since the $\{\phi_i\}_{i \in I}$ turn $X$ into a cone to $J$, for each $i \in I_0$ there is a transition map $h_{ij} : J(i) \to J(j)$, so $\ker(\phi_j) = \ker(h_{ij} \circ \phi_i) \supseteq \ker(\phi_i)$. Replacing each $\ker(\phi_i)$ with $\ker(\phi_j)$, we see $E = \ker(\phi_j)$, and $\phi_j$ is definable.

On the other hand, suppose we have elimination of imaginaries. Fix $X$ and $Y$. For each $Z$ and $f : Z \times X \to Y$, we may form the equivalence relation $E_f$ on $Z$ which says $z_1 \sim_{E_f} z_2$ if and only if they define the same fiber of $\Gamma(f)$. The projection map induces a map

$$(-/E_f) \times X : Z \times X \to Z/E_f \times X$$ 

which is also a map $f \to f/E_f$ of objects over $Y$. 

Now, the [[category of elements]] $\operatorname{Pt}(1, Y^X)$ of the presheaf $\operatorname{Hom}(- \times X, Y)$ has objects maps $f : Z \times X \to Y$ for $Z$ ranging over $\mathbf{Def}(T)$, and morphisms from $f_1 : Z_1 \times X \to Y$ to $f_2 : Z_2 \times X \to Y$ the maps $g \times X : Z_1 \times X \to Z_2 \times X$ for $g : Z_1 \to Z_2$ such that $f_1 = f_2 \circ g$. For each object $f \in \operatorname{Pt}(1, Y^X)$, $-/ E_f \times X$ as above coequalizes all pairs of maps in $\operatorname{Pt}(1, Y^X)$ into $f$. Furthermore, the natural projection $p$ from $\operatorname{Pt}(1, Y^X) \to \mathbf{Def}(T)$ by sending $f : Z \times X \to Y \mapsto Z$ creates colimits, in particular finite coproducts, which by assumption exist in $\mathbf{Def}(T)$. So $\operatorname{Pt}(1, Y^X)$ is filtered, and since for any presheaf $P$, we have that

$$P \simeq \underset{\longrightarrow}{\lim}\left(\operatorname{Pt}(1,P) \overset{p}{\to} \mathbf{Def}(T) \overset{\mathbf{y}}{\hookrightarrow} \widehat{\mathbf{Def}(T)}\right),$$

so $Y^X$ is ind-representable. $\square$

**Remark.** In the above proof, complementation is required to characterize compactness as "every covering of a definable set by an infinite family of definable sets is finitely supported." The same proof works if we replace inner homs with power objects.

* Bruno Poizat, _Une th&#233;orie de Galois imaginaire_, J. Symbolic Logic __48__ (1984), no.4, 1151-1170, [MR85e:03083](http://www.ams.org/mathscinet-getitem?mr=727805), [doi](http://dx.doi.org/10.2307/2273680)
* wikipedia [imaginary element](http://en.wikipedia.org/wiki/Imaginary_element)
* Anand Pillay, _Some remarks on definable equivalence relations in O-minimal structures_, J. Symbolic Logic __51__ (1986), 709-714, [MR87h:03046](http://www.ams.org/mathscinet-getitem?mr=853850), [doi](http://dx.doi.org/10.2307/2274024)
* Jan Holly, _Definable operations on sets and elimination of imaginaries_, Proc. Amer. Math. Soc. __117__ (1993), no. 4, 1149&#8211;1157, [MR93e:03052](http://www.ams.org/mathscinet-getitem?mr=1116261), [doi](http://dx.doi.org/10.2307/2159546), [pdf](http://www.ams.org/journals/proc/1993-117-04/S0002-9939-1993-1116261-6/S0002-9939-1993-1116261-6.pdf)
* [[Ehud Hrushovski]], _Groupoids, imaginaries and internal covers_, [arxiv/math.LO/0603413](http://arxiv.org/abs/math/0603413); _On finite imaginaries_, [arxiv/0902.0842](http://arxiv.org/abs/0902.0842)
* D. Haskell, E. Hrushovski, H.D.Macpherson, _Definable sets in algebraically closed valued fields: elimination of imaginaries_, J. reine und angewandte Mathematik __597__ (2006)
* [[Saharon Shelah]], _Classification theory and the number of non-isomorphic models_, Studies in Logic and the Foundations of Mathematics __92__, North Holland, Amsterdam 1978
[[!redirects elimination of imaginaries]]
* Moshe Kamensky, [_A categorical approach to internality_](http://arxiv.org/abs/1012.3185)

[[!redirects elimination of imaginaries]]
[[!redirects imaginaries]]