
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The effective topos $Eff$ is an example of an [[elementary topos]] with a [[natural numbers object]] which is not a [[Grothendieck topos]] (and doesn't even have a [[geometric morphism]] to [[Set]]).

It is an environment for [[higher-order logic|higher order]] [[recursion]] theory, where, in the [[internal logic]], it is provable that every [[total function]] from [[natural numbers]] to natural numbers is [[computable function|recursive]] (furthermore, the functor $Hom(1, -)$ from the effective topos into [[Set]], the inverse image part of a geometric morphism $Set \to Eff$ preserves the natural numbers object, giving a suitable version of this result in the external logic as well). 

It can be specified as the [[realizability topos]] for [[Kleene's first algebra]]. 

The effective topos construction alluded in the above paragraph can be performed more generally, in every topos $E$ with a natural numbers object, replacing [[Set]]. To every such topos one constructs the corresponding "external" effective topos $e E$ and the correspondence $E \mapsto e E$ extends to a functor admitting a [[full and faithful functor|fully faithful]] [[right adjoint]].  Kleene's first algebra can also be replaced by any [[partial combinatory algebra]], or even some more general types of gadgets; toposes obtained in this way are called [[realizability topos]]es.

The effective topos is the category obtained from the category of sets by first freely adjoining recursively-indexed coproducts (but being careful to preserve the empty set), and then adding quotients of (pseudo-)equivalence relations. ([RobinsonRosolini](#RobinsonRosolini)).

## Definition

An object of the effective topos is a set $X$ along with an effective PER $E_X \subseteq \mathbb{N} \times X \times X$. This means that $(p_{2,3})_*(E_X) \subseteq X \times X$ is a [[partial equivalence relation]] on $X$, with "computational proofs" of the symmetry and transitivity properties. In particular, let us use notation $n \Vdash x \equiv y$ for $(n, x, y) \in E_X$. What we require is:

* (Symmetry tracker) There exists a [[partial recursive function]] $s_X : \mathbb{N} \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash x \equiv y,$$
then $s_X(n)$ is defined and
$$s_X(n) \Vdash y \equiv x.$$

* (Transitivity tracker) There exists a partial recursive function $t_X : \mathbb{N}^2 \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash x \equiv y$$
and
$$m \Vdash y \equiv z,$$
then $t_X(n, m)$ is defined and
$$t_X(n, m) \Vdash x \equiv z.$$

As for morphisms, they will be defined by equivalence classes of effective functional relations under a certain equivalence relation. In particular, an effective functional relation between objects $(X, E_X)$ and $(Y, E_Y)$ will be a subset $f \subseteq \mathbb{N} \times X \times Y$ such that using notation $n \Vdash x \xmapsto{f} y$ for $(n, x, y) \in f$, we have:

* (Domain tracker) There exists a partial recursive function $d_f : \mathbb{N} \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash x \xmapsto{f} y,$$
then $d_f(n)$ is defined and
$$d_f(n) \Vdash x \equiv x.$$

* (Codomain tracker) There exists a partial recursive function $c_f : \mathbb{N} \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash x \xmapsto{f} y,$$
then $c_f(n)$ is defined and
$$c_f(n) \Vdash y \equiv y.$$

* (Image uniqueness tracker) There exists a partial recursive function $u_f : \mathbb{N}^2 \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash x \xmapsto{f} y_1$$
and
$$m \Vdash x \xmapsto{f} y_2,$$
then $u_f(n, m)$ is defined and
$$u_f(n, m) \Vdash y_1 \equiv y_2.$$

* (Totality tracker) There exists a partial recursive function $t_f : \mathbb{N} \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash x \equiv x,$$
then $t_f(n)$ is defined, and there exists $y\in Y$ such that
$$t_f(n) \Vdash x \xmapsto{f} y.$$

* (Respectfulness tracker) There exists a partial recursive function $r_f : \mathbb{N}^3 \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash x_1 \xmapsto{f} y_1,$$
$$m \Vdash x_1 \equiv x_2,$$
and
$$p \Vdash y_1 \equiv y_2,$$
then $r_f(n, m, p)$ is defined and
$$r_f(n, m, p) \Vdash x_2 \xmapsto{f} y_2.$$

As for the equivalence relation, we will say that effective functional relations $f, g \subseteq \mathbb{N} \times X \times Y$ are equivalent if there exists an equivalence tracker, i.e. a partial recursive function $e_{f,g} : \mathbb{N} \dashrightarrow \mathbb{N}$ such that whenever
$$n \Vdash x \xmapsto{f} y,$$
then $e_{f,g}(n)$ is defined, and
$$e_{f,g}(n) \Vdash x \xmapsto{g} y.$$

For the other pieces of data required to make this a category, first define the identity morphism on $X$ to be the equivalence class of $E_X$, i.e. the equivalence class of the effective functional relation $\operatorname{id}_X$ where $n \Vdash x \xmapsto{\operatorname{id}_X} y$ if and only if $n \Vdash x \equiv y$.

As for compositions, this will be induced by the following composition operation on effective functional relations: suppose $g$ is an effective functional relation between $(X, E_X)$ and $(Y, E_Y)$, and $f$ is an effective functional relation between $(Y, E_Y)$ and $(Z, E_Z)$. Also, fix a full recursive pairing bijection $\langle {-}, {-} \rangle : \mathbb{N}^2 \to \mathbb{N}$ with full recursive projections $p_1, p_2 : \mathbb{N} \rightrightarrows \mathbb{N}$ such that $(p_1, p_2) : \mathbb{N} \to \mathbb{N}^2$ is the inverse of $\langle {-}, {-} \rangle$. Then $f \circ g \subseteq \mathbb{N} \times X \times Z$ will be the effective functional relation consisting of triples $(n, x, z)$ such that there exists $y\in Y$ with
$$p_1(n) \Vdash x \xmapsto{g} y$$
and
$$p_2(n) \Vdash y \xmapsto{f} z.$$

For proofs that this does indeed define a category, see [[effective topos proofs|here]].

## Related concepts

* [[realizability]]

* [[topos of recursive sets|recursive topos]]

* [[effective 2-topos]]

## References

Reviews include 

* {#Vermeeren09} [[Stijn Vermeeren]], section 3 of _Realizability Toposes_, 2009 ([pdf](http://stijnvermeeren.be/download/mathematics/essay.pdf))

* J.M.E. [[Martin Hyland|Hyland]], _The effective topos_ in  A. S. Troelstra (ed.)  D. van Dalen (ed.) , _The L.E.J. Brouwer Centenary Symposium_, North-Holland  (1982)  pp. 165--216.

* [[Bart Jacobs]], Chapter 6 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;


In the context of [[triposes]]:

* Andy Pitts, _The theory of triposes_, thesis, [pdf](http://www.cl.cam.ac.uk/~amp12/papers/thet/thet.pdf)

Then

* Sori Lee, [[Jaap van Oosten]], _Basic subtoposes of the effective topos_, [arxiv/1201.2571](http://arxiv.org/abs/1201.2571)

* {#RobinsonRosolini} Edmund Robinson, Giuseppe Rosolini, _Colimit completions and the effective topos_, The Journal of symbolic logic, 55, no 2 (1990) ([JSTOR](http://www.jstor.org/discover/10.2307/2274658?uid=3738736&uid=2129&uid=2134&uid=2&uid=70&uid=4&sid=47698789906927))
 

* [[Aurelio Carboni]], _Some free constructions in realizability and proof theory_, J. Pure App. Alg., Vol. 103 Issue 2 (1995), 117-233. ([web](http://www.sciencedirect.com/science/journal/00224049/103/2)) 

On [[categorification]] of the effective topos to an effective [[2-topos]]:

* [[Steve Awodey]], [[Jacopo Emmenegger]], _Toward the effective 2-topos_ (2025) &lbrack;[arXiv:2503.24279](http://arxiv.org/abs/2503.24279)&rbrack;



[[!redirects effective toposes]]