

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Definition

The __limited principle of omniscience__ ($LPO$) states that the [[existential quantification]] of any [[decidable proposition]] is again decidable.  That is,
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x, P(x)) \vee \neg(\exists x, P(x)) ,$$
or equivalently
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x, P(x)) \vee (\forall x, \neg{P(x)}) .$$

We have not stated the domain of quantification of the variable $x$.  If you take it to be the [[subsingleton]] corresponding to a given [[truth value]] and apply this principle to the constantly [[true]] proposition, then $EM$ follows; conversely, $EM$ implies $LPO$ (over any domain).  However, Bishop\'s $LPO$ takes the domain to be the set of [[natural numbers]], giving a weaker principle than $EM$.  (It appears that a [[realizability topos]] based on infinite-time [[Turing machine]]s validates $LPO$ but not $EM$; see [Bauer (2011)](#Bauer11).)  Note that propositions of the form $\exists x, P(x)$ when $P$ is decidable are the [[open truth values]] in the [[Rosolini dominance]].

We can also state the principle set-theoretically, with explicit reference to the domain of quantification.  Given a [[set]] $A$, the __limited principle of omniscience for $A$__ ($LPO_A$) states that, given any [[function]] $f$ from $A$ to the [[boolean domain]] $\{0,1\}$, either $f$ is the [[constant map]] to $0$ or $1$ belongs to the [[image]] of $f$.  Then Bishop\'s $LPO$ is $LPO_{\mathbb{N}}$, which applies to any [[infinite sequence]] of [[bits]].

While $LPO$ for $\mathbb{N}$ is a classic example of the difference between constructive and classical mathematics, $LPO$ holds for the set $\overline{\mathbb{N}}$ of [[extended natural number]]s; this is related to the fact that $\overline{\mathbb{N}}$ may constructively be given a [[compact space|compact]] topology.  See [Escard&#243; (2011)](#Escardo11) for this and much more.


## In the internal logic

In [[set theory]], there are actually two different notions of logic: there is the external predicate logic used to define the set theory itself, and there is the internal predicate logic induced by the set operations on [[subsingletons]] and [[injections]]. In particular, 

* An internal *[[proposition]]* is a set $P$ such that for all elements $x \in A$ and $y \in A$, $x = y$. 

* The internal proposition *[[true]]* is a [[singleton]] $\top$. 

* The internal proposition *[[false]]* is the [[empty set]]

* The internal conjunction of two internal propositions $P$ and $Q$ is the [[cartesian product]] $P \times Q$ of $P$ and $Q$. 

* The internal disjunction of two internal propositions $P$ and $Q$ is the [[image]] of the [[uniqueness quantifier|unique]] function $!_{P \uplus Q}:P \uplus Q \to 1$ from the [[disjoint union]] of $P$ and $Q$ to the [[singleton]] $\top$. 

$$P \vee Q = \mathrm{im}(!_{P \uplus Q})$$

* The internal implication of two internal propositions $P$ and $Q$ is the [[function set]] $P \to Q$ between $P$ and $Q$. 

* The internal negation of an internal proposition $P$ is the function set from $P$ to the [[empty set]]

$$\neg P = P \to \emptyset$$

* An internal proposition $P$ is a [[decidable proposition]] if it comes with a function $\chi_P:P \to 2$ from $P$ to the [[boolean domain]] $2$. 

* An *internal predicate* on a set $A$ is a [[set]] $P$ with [[injection]] $i:P \hookrightarrow A$, whose family of propositions indexed by $x \in A$ is represented by the [[preimages]] $i^*(x)$.

* The internal [[existential quantifier]] of an internal predicate $i:P \hookrightarrow A$ is the [[image]] of the [[uniqueness quantifier|unique]] function $!_P:P \to \top$ into the singleton $\top$.

$$\exists_A P = \im(!_P)$$

* The internal [[universal quantifier]] of an internal predicate $i:P \hookrightarrow A$ is the [[dependent product]] of the preimages
 
$$\forall_A P = \{f \in P^A \vert \forall x \in A, f(x) \in i^*(x) \}$$

* An internal predicate $i:P \hookrightarrow A$ is a [[decidable proposition]] if it comes with a function $\chi_P(x):i^*(x) \to 2$ into the [[boolean domain]] for all elements $x \in A$, or equivalently if it comes with a function $\chi_P:A \to 2$ from $A$ to the [[boolean domain]] $2$. 

Then the **internal LPO** for a [[family of sets]] $(A_z)_{z \in I}$ is the LPO for each $A_z$ stated in the internal logic of the set theory:

* For any internal predicate $i:P \hookrightarrow A_z$, if there is a function $\chi_P:A_z \to 2$, then the internal existential quantification of $P$, $\exists_{A_z} P = \im(!_P)$ has a function $(\exists_{A_z} P) \to 2$ into the boolean domain. 

or equivalently, as

* For any function $a:A_z \to 2$, the internal existential quantification of $P = \{x \in A_z \vert a(x) = 1\}$, $\exists_{A_z} P = \im(!_P)$ has a function $(\exists_{A_z} P) \to 2$ into the boolean domain. 

In particular, the internal LPO for the family of all [[subsingletons]] is internal excluded middle. Similarly, given a [[universe]] $U$, the internal LPO for the family of all sets in $U$ is excluded middle in $U$. 

The internal versions of the limited principles of omniscience, like all internal versions of axioms, are weaker than the external version of the limited principle of omniscience, since while [[bounded separation]] implies that one can convert any external predicate $x \in A \vdash P(x)$ on a set $A$ to an internal predicate $\{x \in A \vert P(x)\} \hookrightarrow A$, it is generally not possible to convert an internal predicate to an external predicate without a reflection rule which turns subsingletons in the set theory into propositions in the external logic. 

## Equivalent statements

There are various other results that are equivalent to the principles of omniscience. Here are a few:

* Every [[semi-decidable proposition]] is a [[decidable proposition]] iff $\mathrm{LPO}_\mathbb{N}$ holds. 

* [[sequentially compact space|Sequential compactness]] of the [[unit interval]] holds if and only if $\mathrm{LPO}_\mathbb{N}$ holds. 

* The [[boolean domain]] is the [[initial object|initial]] $\sigma$-frame if and only if $\mathrm{LPO}_\mathbb{N}$ holds. 

* The [[Cauchy real numbers]] are isomorphic to the [[radix notation|radix expansion]] in any base (e.g., a decimal expansion or binary expansion) iff $\mathrm{LPO}_\mathbb{N}$ holds. See [Feldman (2010)](#Mehkeri10). 

* The [[analytic LPO]] for the following sets of real numbers are equivalent to the LPO for the [[natural numbers]]: the [[Cauchy real numbers]] $\mathbb{R}_C$, the [[Escardo-Simpson real numbers]]/[[HoTT book real numbers]] $\mathbb{R}_E$/$\mathbb{R}_H$, and the subfield of [[Dedekind real numbers]] $\mathbb{R}_\Sigma \subseteq \mathbb{R}_D$ which are constructed out of [[Dedekind cuts]] valued in the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]] $\Sigma \subseteq \Omega$. 

## Truncated and untruncated versions in dependent type theory

In the context of [[dependent type theory]], the various principles of omniscience can be translated in two ways, by interpreting "or" as [[propositional truncation|propositionally truncated]] ("merely or") or untruncated ("purely or"). Truncated LPO and untruncated LPO are equivalent (due to [[Martin Escardo]], see [UFP](#UFP)). 

## Related statements

There are various other results that are related to the principles of omniscience. Here are a few:

* The [[full bar theorem]] implies the $\mathrm{LPO}_\mathbb{N}$. 

* The existence of various [[classical mathematics|classical]] [[universes]] or models of [[foundations of mathematics]] implies the $\mathrm{LPO}_\mathbb{N}$: 

  * Any model $\mathcal{V}$ of bounded Zermelo set theory contains a [[pure set]] of [[real numbers]] $\mathbb{R}$. One can collect all the pure sets of $\mathcal{V}$ which are in $\mathbb{R}$ and show that the resulting set is a subset of $\mathcal{V}$ and a sequentially Cauchy complete Archimedean ordered field which satisfies the [[analytic LPO]], thus implying $\mathrm{LPO}_\mathbb{N}$ for the entire foundations. Thus, the existence of stronger models of [[material set theory]] such as [[ZFC]] also imply $\mathrm{LPO}_\mathbb{N}$ for the entire foundations. 

  * For a similar reason, the existence of a constructively [[well-pointed topos|well-pointed]] [[Boolean topos|Boolean]] [[W-topos]] $\mathcal{E}$ implies the $\mathrm{LPO}_\mathbb{N}$, since the hom-set $\mathrm{Hom}_\mathcal{E}(1, \mathbb{R})$, where $1 \in \mathcal{E}$ is the [[terminal object|terminal]] [[generator]] and  $\mathbb{R} \in \mathcal{E}$ is the [[real numbers object]] in $\mathcal{E}$, yields a sequentially Cauchy complete Archimedean ordered field which satisfies the [[analytic LPO]], thus implying $\mathrm{LPO}_\mathbb{N}$ for the entire foundations. Thus, the existence of any constructive model of [[ETCS]] also implies $\mathrm{LPO}_\mathbb{N}$ for the entire foundations. 

  * Finally, in [[dependent type theory]], there being a [[univalent Tarski universe]] $(U, T)$ closed under dependent product types, dependent sum types, and identity types and satisfying the axiom of infinity and [[excluded middle]] implies the $\mathrm{LPO}_\mathbb{N}$, since one can construct an element $\mathbb{R}:U$ representing the $U$-small type of real numbers, whose type reflection $T(\mathbb{R})$ is a sequentially Cauchy complete Archimedean ordered field which satisfies the [[analytic LPO]], thus implying $\mathrm{LPO}_\mathbb{N}$ for the entire type theory. Thus, any univalent Tarski universe which has [[axiom of choice]] or a [[choice operator]] for the types in the universe also implies $\mathrm{LPO}_\mathbb{N}$ for the entire type theory. 

  * Note that in all these cases, the real numbers $\mathbb{R}$ constructed from these universes or classical models of foundations of mathematics, while equivalent to the internal Dedekind real numbers constructed in the universe or model, are not necessarily equivalent to the external [[Dedekind real numbers]] in the foundations. 

* $WLPO$ follows from [[LPO]], but not conversely. If $P(x)$ is a decidable proposition, then so is $\neg{P(x)}$, and so $LPO$ gives
$$(\exists x, \neg{P(x)}) \vee (\forall x, \neg{\neg{P(x)}}), $$
which implies
$$\neg(\forall x, P(x)) \vee (\forall x, P(x))$$
as $P$ is decidable.

* The [[LLPO]] follows from [[LPO]], [[WLPO]] is equivalent to untruncated LLPO, which implies truncated LLPO, and [[WLPO]] follows from [[LPO]]. However, the converse does not necessarily hold, since in <http://www1.maths.leeds.ac.uk/~rathjen/Lifschitz.pdf> is a model by Michael Rathjen that separates WLPO from LLPO. Similarly, [Grossack 24](#Grossack24) shows that Johnstone's topological topos separates WLPO from LLPO. Thus LLPO is separated from LPO.  

## Models

* Assuming that [[Set]] is a [[Boolean topos]], then $LPO_{\mathbb{N}}$ (the LPO for natural numbers) holds in any [[presheaf topos]] over $Set$ and indeed in any [[locally connected topos]] over $Set$, essentially since then $2^N$ is a constant object.

* The LPO for natural numbers fails in Johnstone's [[topological topos]], due to its internal continuity principle.  Hence, the analytic LPO also fails, since the modulated Cauchy reals and Dedekind reals coincide in this topos. 

## Related concepts

* [[principle of omniscience]]

* [[weak limited principle of omniscience]]

* [[lesser limited principle of omniscience]]

* [[Markov's principle]]

* [[excluded middle]]

## References

* {#Bishop67} [[Errett Bishop]]: _[[Foundations of Constructive Analysis]]_, McGraw-Hill (1967)
 
  > (in the introduction or chapter 1, I forget)

* {#Ishihara06} [[Hajime Ishihara]], _Reverse Mathematics in Bishop's Constructive Mathematics_, Philosophia Scienti&#230;, CS 6 (2006) ([doi:10.4000/philosophiascientiae.406](https://doi.org/10.4000/philosophiascientiae.406),  [pdf](https://philosophiascientiae.revues.org/pdf/406))

* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* {#Rathjen13} [[Michael Rathjen]], *Constructive Zermelo-Fraenkel set theory and the limited principle of omniscience*. &lbrack;[arXiv:1302.3037](https://arxiv.org/abs/1302.3037)&rbrack;

* {#Shulman18} [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Booij20} [[Auke Booij]], *Analysis in univalent type theory* (2020) &lbrack;[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)&rbrack;

* {#Ciraulo22} Francesco Ciraulo, *$\sigma$-locales in Formal Topology*, Logical Methods in Computer Science, Volume 18, Issue 1 (January 12, 2022) ([doi:10.46298/lmcs-18%281%3A7%292022](https://doi.org/10.46298/lmcs-18%281%3A7%292022), [arXiv:1801.09644](https://arxiv.org/abs/1801.09644))

* {#BirchfieldSwan24} Madeleine Birchfield, Andrew Swan (2024) on Category Theory Zulip, [LPO and sigma-frame structure on booleans](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/LPO.20and.20sigma-frame.20structure.20on.20booleans)

* {#Grossack24} [[Chris Grossack]], *Life in Johnstone's Topological Topos 3 -- Bonus Axioms* ([web](https://grossack.site/2024/07/03/topological-topos-3-bonus-axioms))

* {#LombardiMahboubi24} [[Henri Lombardi]], [[Assia Mahboubi]], *Théories géométriques pour l'algèbre des nombres réels sans test de signe ni axiome de choix dépendant* ([arXiv:2406.15218](https://arxiv.org/abs/2406.15218))

These two references call the limited principle of omniscience simply by the term "principle of omniscience" or "omniscience principle". However, [[principle of omniscience]] can refer to multiple possible axioms. 

* {#Bauer11}  [[Andrej Bauer]] (2011) via constructivenews, [An Injection from $\mathbb{N}^{\mathbb{N}}$ to $\mathbb{N}$](http://math.andrej.com/wp-content/uploads/2011/06/injection.pdf) (pdf)

* {#Escardo11} [[Martín Escardó]] (2011) via constructivenews, [Infinite sets that satisfy the principle of omniscience in all varieties of constructive mathematics](http://www.cs.bham.ac.uk/~mhe/papers/omniscient-2011-07-06.pdf) (pdf)

[[!redirects LPO]]
[[!redirects limited principle of omniscience]]
[[!redirects limited principles of omniscience]]

[[!redirects internal LPO]]
[[!redirects internal limited principle of omniscience]]
[[!redirects internal limited principles of omniscience]]

[[!redirects truncated LPO]]
[[!redirects truncated limited principle of omniscience]]
[[!redirects truncated limited principles of omniscience]]

[[!redirects untruncated LPO]]
[[!redirects untruncated limited principle of omniscience]]
[[!redirects untruncated limited principles of omniscience]]