+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Operator algebra
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea
 {#Idea}


A _Bohr topos_ is a [[topos]] associated with any [[quantum mechanical system]], which is such that 

* the [[quantum observables]] and [[quantum states]] of the [[quantum mechanical system]], hence its [[quantum probability theory]], 

are equivalently 

* the [[classical physics|classical]] [[observables]] and classical [[states]], hence its classical [[probability theory]], 

  _[[internalization|internal]]_ to the Bohr topos, hence in the _[[internal logic]]_ of the Bohr topos. 

A detailed motivation/derivation of this from classical theorems on the foundations of standard [[quantum mechanics]] is at _[[order-theoretic structure in quantum mechanics]]_.

One might think of a Bohr topos as (part of) a formalization of the "[[coordination]]" of the [[physical theory]] of [[quantum mechanics]], providing a formalized prescription of how to map the theory to [[propositions]] about ([[experiment|experimental]]) [[observables]] of the system. The [[internal logic]] of Bohr toposes has been argued (e.g. [Heunen-Landsman-Spitters 09](#HeunenLandsmanSpitters09)) to be a better formal context for such considerations than the old [[quantum logic]] going back to [[von Neumann]].

The idea of Bohr toposes goes back to  [Butterfield-Hamilton-Isham](#ButterfieldHamiltonIsham), [Isham-D&#246;ring 07](#IshamDoering07)) and [Heunen-Landsman-Spitters 09](#HeunenLandsmanSpitters09). The concept is named after [[Niels Bohr]], whose informal ideas about the nature of quantum mechanics ([Bohr 1949](#interpretation+of+quantum+mechanics#Bohr49), cf. [Scheibe 1973, p. 24](#Scheibe73)) it is supposed to formalize, see at _[interpretation of quantum mechanics -- Bohr's standpoint](interpretation+of+quantum+mechanics#BohrStandpoint)_.

Sometimes in the literature the discussion of Bohr toposes is referred to as "the topos-theoretic formulation of physics". But actually Bohr toposes currently formalize but one aspect of [[quantum mechanics]], namely "the quantum mechanical [[phase space]]" in the form of the [[quantum observables]] and the [[quantum states]]. The plain Bohr topos does not even encode any [[dynamics]], though in the spirit of [[AQFT]] a certain presheaf of Bohr toposes on [[spacetime]] does encode dynamics ([Nuiten 11](#Nuiten11)). For other and more comprehensive usages of [[topos theory]] in the formalization of [[physics]] see at _[[geometry of physics]]_ and at _[[higher category theory and physics]]_.

### Brief
 {#IdeaInBrief}

To every [[quantum mechanical system]] is associated its _Bohr topos_: a [[ringed topos]] which plays the role of the quantum [[phase space]]. The idea of this construction -- _Bohrification_ -- is that it naturally captures the [[geometry|geometric]] and [[logic|logical]] aspects of [[quantum physics]] in terms of [[higher geometry]]/[[topos theory]].

One way to understand Bohrification is as a generalization of the construction of the [[Gelfand spectrum]] of commutative [[C-star algebra]]s to a context of _noncommutative_ $C^*$-algebras. It assigns to a noncommutative $C^*$-algebra $A$ essentially a system of Gelfand dual spaces to each of its [[commutative C*-algebra|commutative]] subalgebras.
Together, this system yields a generalized [[Gelfand spectrum]] in the form of a [[locale]] $\underline{\Sigma}_A$ [[internalization|internal]] to the [[sheaf topos]] $\mathcal{T}_A$ over the [[poset of commutative subalgebras]] of $A$, or  equivalently its externalization $\Sigma_A \to \mathcal{C}(A)$ regarded as a [[locale]] [[over category|over]] the locale of open subalgebras.

As a [[topos]], the Bohr topos is just a [[presheaf topos]], the topos of presheaves on this [[poset of commutative subalgebras]] of $A$, but the point is that it is naturally a [[ringed topos]] with the original non-commutative algebra $A$ appearing as a commutative $C^\ast$-algebra [[internalization|internal]] to the Bohr topos. This allows to talk about [[quantum states]] on $A$ much like classical states, but internal to the Bohr topos. 

In fact, under mild assumptions on $A$, its [[poset of commutative subalgebras]], and hence the Bohr topos over it, encodes precisely the [[Jordan algebra]] underlying $A$. As discussed at _[[Jordan algebra]]_, this is precisely that part of $A$ which knows about the [[quantum observables]] themselves. In order to have the Bohr topos remember the full non-commutative algebra structure of $A$, it needs to be equipped with the information about [[Hamiltonian vector field|Hamiltonian]] [[flows]] induced on $A$ by automorphisms of the form $\exp(i [H,-])$, where $[-,-]$ is the [[commutator]] (that gets discarded as one passes to the [[Jordan algebra]]). According to [[Andreas Döring]] (private communication at MPI Bonn, April 2013), this can be formulated nicely in topos theory.


### More detailed

The formalization of the notion _[[quantum mechanical system]]_ (see there for details) with its _[[states]]_ and _[[observables]]_ is the following.

* The system as such is encoded by a [[C-star algebra]] $A$;

* a [[self-adjoint operator]] $a \in A$ is thought of as being an [[observable]] of the system: a kind of observation that one can make about it;

* a $\mathbb{C}$-[[linear map]] $\rho : A \to \mathbb{C}$ (which is "positive" and "normalized") is thought of as being a _[[state]]_ that the system can be in -- a physical configuration (or rather: a [[probability distribution]] of such);

* the pairing $(a, \rho) \mapsto \rho(a) \in \mathbb{C}$ is thought of as being the value of the observable $a$ made on the system in state $\rho$: for instance the total _[[energy]]_ of the system as measured in some chosen [[unit]];

* a one-parameter [[group]] of [[automorphism]]s $\mathbb{R} \to Aut(A)$ ([[inner automorphisms]] for "localized" systems, see below) is thought of as being an _evolution_ of the system, for instance in [[time]] or more general in [[spacetime]].

(Often in the literature quantum mechanical systems are instead dually conceived of in terms of [[Hilbert space|Hilbert]] [[spaces of states|spaces of]] [[pure states]]. The relation between these two descriptions is established by the [[GNS-construction]] which allows to pass from one to the other.)

Notice that these axioms are naturally thought of as exhibiting the $C^\ast$-algebra $A$ as a [[Isbell duality|formal dual]] of the would-be _quantum [[phase space]]_ of the physical system -- not quite an ordinary [[topological space]] (which by [[Gelfand duality]] it would be if $A$ were commutative) but still a kind of generalized space. Traditionally it is common to regard this as a space in [[noncommutative geometry]]. Notice that if we do so -- hence if we regard the object $Spec A \in C^\ast Alg^{op}$ that is the incarnation of $A \in C^\ast Alg$ in the [[opposite category]] -- then the definition of [[observable]] above reduces to the evident notion of real-valued functions on quantum phase space: such a function is a [[morphism]] $Spec A \to \mathbb{R}$ in $C^\ast Alg^{op}$, which dually is a $C^\ast$-algebra [[homomorphism]] $C(\mathbb{R})_0 \to A$ (where on the left we have the [[unitization]] of functions with [[compact support]]). That such correspond to [[self-adjoint operator]]s of $A$ is the statement of [[functional calculus]] for $C^\ast$-algebras.

More subtle is the interpretation of the axiom for [[state]]s. Historically this had been been subject to some discussion: by the [[spectral theorem]] two different [[observable]]s $a_1, a_2 \in A$ have a compatible set of observable values if and only if these elements commute with each other in $A$. Generally, a set $\{a_i\}_i$ of observables has a jointly consistent set of observable values if and only if the sub-$C^\ast$-algebra $\langle \{a_i\}_i\rangle \subset A$ generated by them is commutative. Therefore for the phenomenological interpretation of the axioms it seems to make no sense to demand that a [[state]] $\rho : A \to \mathbb{C}$ be linear on non-commuting observables: if $a_1$ and $a_2$ do not commute, it is not a-priori clear that it makes sense to require that $\rho(a_1 + a_2) = \rho(a_1) + \rho(a_2)$. This might experimentally fail, and hold only for commuting $a_1, a_2$.

Therefore the notion of _[[quasi-state]]_ was introduced: a quasi-state on $A$ is defined to be a (positive and normalized) [[function]] $\rho : A \to \mathbb{C}$ which is required to be $\mathbb{C}$-[[linear function|linear]] only on all commutative subalgebras of $A$. Operationally, quasi-states should be the genuine states!

One would therefore tend to think that the terminology has been chosen in an unfortunate way. While maybe true, it turns out -- non-trivially -- that in a major class of cases of interest the distinction does not matter: namely _[[Gleason's theorem]]_ states that for $H$ a separable complex [[Hilbert space]] with $dim H \gt 2$ and $A = B(H)$ the $C^\ast$-algebra of [[bounded operators]] on $\H$, all quasi-states on $A$ are automatically states: a function that is linear on all commutative subalgebras is automatically also linear on all of $A$.

While this means that the distinction between states and quasi-states disappears in a major case of interest, it does not disappear in all cases of interest. In particular, other foundational theorems about quantum mechanics concern the collection of commutative subalgebras, too.

Notably, one may wonder about the evident strengthening of the notion of quasi-states to that of a map $\rho : A \to \mathbb{C}$ which is not just linear but also an [[associative algebra|algebra]] [[homomorphism]] on each commuting subalgebra. Notice that by [[Gelfand duality]] every commutative $C^\ast$-algebra $C$ is the algebra of continuous functions on some [[topological space]] $sp(C)$. Under this duality a [[state]] on $C$ is a [[probability distribution]] on $sp(C)$, while an algebra homomorphism $C \to \mathbb{C}$ is a [[point]] of $X_C$. Therefore a quasi-state which is commutative-subalgebra-wise an algebra [[homomorphism]] may be thought of as encoding a collection of precise numerical values (as opposed to just expectation values) of _all_ possible observables. Such a hypothetical quasi-state is sometimes called a collection of _[[hidden variable]]s_ of the [[quantum mechanical system]]: its existence would mean that despite the apparent probabilistic nature of [[quantum mechanics]], there are "hidden" non-probabilistic states. But there are not. This is the statement of the [[Kochen-Specker theorem]]: under precisely the assumptions that make [[Gleason's theorem]] work, there is _no_ quasi-state which is commutative-subalgebra-wise an algebra homomorphism.

In summary, this means:

+-- {: .standout}

The foundational characteristics of [[quantum physics]] are encoded in notions of [[functions]] on the [[algebra of observables]] $A$ which are linear and positive only _commutative-subalgebra-wise_ .

=--

Since the notion of **commutative-subalgebra-wise homomorphism** is at the heart of quantum physics, it seems worthwhile to consider natural formalizations of this notion. There is indeed a very natural and [[category theory|general abstract]] one: whenever any notion of [[function]] is defined only _locally_ it is natural to consider the [[sheaf]] of such functions over all possible local patches. 

The historically motivating example, and possibly still the most widely familiar one, is that of [[holomorphic function]]s on a [[complex manifold]]: there are in general very few holomorphic functions defined over all of a complex manifold, but plenty of them defined over any small enough subset. And it is of fundamental interest to consider the collections of holomorphic functions over each such subset, and how these restrict to each other under restriction of subsets. This collection of local data is a [[sheaf]] of functions on the complex manifold.

There is an evident analog setup of this situation that applies in the present case of interest, that of functions defined on commutative subalgebras:

For $A$ any [[C-star algebra]], write $\mathcal{C}(A)$ for the set of all its commutative $C^\ast$-subalgebras. This is naturally a [[poset]] under inclusion of subalgebras. A (co)[[presheaf]] of this set is a [[functor]] $\mathcal{C}(A) \to Set$. Any such functor we may think of as a collection of commutative-subalgebra-wise data on $A$, consistent with restriction of subalgebras. The collection of all such functors -- which we write $[\mathcal{C}(A), Set]$ -- is a [[category]] called a [[presheaf topos]]. 

[[internal logic|Inside]] this [[topos]], all the above discussion of foundations of quantum mechanics finds a natural simple equivalent reformulation:

First of all, the non-commutative $C^\ast$-algebra $A$ naturally induces a _commutative_ [[C-star algebra]] object $\underline{A}$ [[internalization|internal to]] $[\mathcal{C}(A), Set]$: namely the [[copresheaf]] defined by the tautological assignment

$$
  \underline{A} : (C \in \mathcal{C}(A)) \mapsto C
  \,.
$$

In words this means nothing but that the collection of all commutative subalgebras of $A$ may naturally be regarded as a _single_ commutative $C^\ast$-algebra [[internalization|internal to]] the [[topos]] $[\mathcal{C}(A), Set]$.

Below we shall discuss ([here](...)) that in a precise sense this commutative internal $\underline{A}$ captures precisely all the [[kinematics|kinematical]] information encoded in the [[quantum mechanical system]] of $A$ -- everything related to [[states]] and [[observables]] but not information about (time) evolution. So everything we have discussed so far.

The pair of these two ingredients

$$
  Bohr(A) := ([\mathcal{C}(A), Set], \underline{A})
$$  

constitutes what is called a _[[ringed topos]]_ -- a special case of the notion of a [[locally ringed topos]]. This notion is a fundamental notion for generalized [[space]]s in [[higher geometry]]. The most advanced general theory of [[higher geometry]] ([[Structured Spaces|Lurie09]]) is based on modelling spaces as ringed toposes.

We shall call this ringed topos the **Bohr topos** of $A$. 

This terminology is meant to indicate that one may think of this construction as formalizing faithfully and usefully a heuristic that has been emphasized by [[Niels Bohr]] -- one of the founding fathers of [[quantum mechanics]] -- and is known as the _doctrine of classical concepts_ ([Scheibe 1973](#Scheibe73)) in [[quantum mechanics]]. This states that  nonclassical/noncommutative as the [[logic]]/[[geometry]] of quantum mechanics may be, it is to be probed and detected by classical/commutative logic/geometry. 

Namely in terms of the Bohr topos we have the following equivalent reformulations of the foundational facts about quantum physics discussed above, now internally in $Bohr(A)$.

+-- {: .standout}


**Consistent quantum mechanical states.** A [[quasi-state]] on $A$ is precisely an ordinary [[classical state]] on $\underline{A}$, [[internalization|internal]] to $Bohr(A)$.

In particular ([[Gleason's theorem]]): if $A = B(H)$ for $dim H \gt 2$ then a [[quantum state]] on the external $A$ is precisely a [[classical state]] on the internal $\underline{A}$.

=--

and 

+-- {: .standout}

**Non-existence of hidden quantum variables.** The [[Gelfand spectrum]] $sp(\underline{A})$ of $\underline{A}$ internal to the Bohr topos has no [[global element|global point]]. ([[Kochen-Specker theorem|Kochen-Specker]]).

=--

These two statements might be taken as suggesting that a quantum mechanical system $A$ is naturally regarded in terms of its Bohr topos $Bohr(A)$ -- somewhat more naturally than as a $C^\ast$-algebra $A$. (The second, in a slightly different setup, was emphasized in [IshamHamiltonButterfield](#ButterfieldHamiltonIsham), which inspired all of the following discussion, the first in [Spitters]()). In fact, thinking of [[ringed topos]]es as generalized [[space]]s in [[higher geometry]], it suggests that the Bohr topos $Bohr(A)$ itself _is_ the _quantum [[phase space]]_ of the quantum mechanical system in question.

To which extent this perspective is genuinely useful is maybe still to be established. For pointers to the literature see the [references](#References) below. Discussion along the above lines may suggest that this perspective is indeed useful, but what is probably still missing is a statement about [[quantum physics]] that can be formulated and proven in terms of Bohr toposes, while being hardly conceivable or at least more unnatural without. It is probably currently not clear if such statements have been found.

One potential such statement has been suggested in ([Nuiten 11](#Nuiten11)) after discussion with [[Bas Spitters|Spitters]]: 

In the formalization of [[quantum field theory]] by the [[Haag-Kastler axioms]] -- called [[AQFT]] -- every quantum field theory is entirely encoded in terms of its [[local net of observables]] over [[spacetime]] $X$. This is a [[copresheaf]] of [[C-star algebra]]s

$$
  A : Op(X) \to C^\ast Alg
$$

which assigns to every [[open subset]] $U \subset X$ of [[spacetime]] the quantum [[subsystem]] $A_U$ of quantum fields supported in that region. By the above, we may consider for each of these quantum systems their associated quantum [[phase space]]s given by the correspondong Bohr toposes $Bohr(A_U)$. This yields a presheaf

$$
  Bohr(A) : Op(X)^{op} \to C^\ast_{com} TopSpace \hookrightarrow C^\ast_{com}Topos
$$

of ringed toposes whose internal ring object has the structure of a commutative $C^\ast$-algebra. With the [[copresheaf]] thus turned into a [[presheaf]] it is natural to ask under which conditions this is a [[sheaf]]: under which conditions this presheaf satisfies [[descent]].

In ([Nuiten 11](#Nuiten11)) the following is observed: if $A$ satisfies what is called the _split property_ (a strong form of the [[time slice axiom]]) then  the Bohr-presheaf of quantum phase spaces satisfies spatial descent by [[local geometric morphism]]s precisely if the original copresheaf of observables $A : Op(X) \to C^\ast Alg$ is indeed _[[local net of observables|local]]_ -- spatially and causally. So this means that a natural property of quantum physics -- spatial and [[causal locality]] -- corresponds from the perspective of Bohr toposes to a natural property of presheaves of quantum phase spaces: [[descent]].

One can probably view this as further suggestive evidence that indeed quantum physics is naturally regarded from the point of view of the Bohr topos. But for seeing where this perspective is headed, it seems that more insights along these lines would be useful.




## Outline

The discussion below proceeds in the following steps (following ([Nuiten 11](#Nuiten11)))

1. [Bohr topos of a quantum mechanics system](#BohrToposOfQMSystem)

   This discusses the Bohr topos incarnation of a [[quantum mechanical system]] -- the topos-theoretic quantum [[phase space]] -- and its [[functor|functoriality]].

1. [Kinematics in a Bohr topos](#KinematicsOnBohrTopos)

   This discusses how the classical [[kinematics]] [[internalization|internal to]] a Bohr topos is the external quantum kinematics of the underlying quantum mechanical system.

1. [(Pre-)Sheaf of Bohr toposes of a quantum field theory](#SheafOfBohrToposesOfQFT)

   This discusses how the [[presheaves]] of Bohr toposes obtained by applying Bohrification to a [[local net of observables]] of a [[quantum field theory]].


## Bohr topos of a quantum mechanical system
 {#BohrToposOfQMSystem}


We discuss the definitions and some basic properties of Bohr toposes: certain [[ringed topos]]es -- in fact [[ringed spaces]] -- associated with any (possibly non-commutative) algebra. We formulate the construction for [[C-star algebra]]s, since this is the standard model for [[quantum mechanical system]]s, but actually much of it does not depend on either the [[topology]] or the [[star-algebra]] structure until we come to the discussion of the [kinematics in a Bohr topos](KinematicsOnBohrTopos) below.

### $C^*$-algebras

+-- {: .num_defn}
###### Definition

A [[C-star algebra]] is (...)

=--

+-- {: .num_defn}
###### Definition

For $A$ a [[star-algebra]], an element $a \in A$ is called a **[[normal operator|normal element]]** if $a^* a = a a^*$.

=--

+-- {: .num_remark}
###### Remark

Every element of a $C^*$-algebra is the sum of two normal elements, because

$$
  a = \frac{1}{2} \left( \left( a + a^* \right) + \left( a - a^*  \right) \right)
  \,.
$$

This means whenever a linear morphism between the vector spaces underlying two  $C^*$-algebras is defined on normal elements, it is already defined on all elements. This will be used in several of the arguments below.

=--

+-- {: .num_defn #PartialCStar}
###### Definition

A **partial $C^\ast$-algebra is a [[set]] $A$ equipped with

* a symmetric and reflexive binary [[relation]] $C \subset A \times A$;

* elements $0,1 \in A$;

* an [[involution]] $\ast : A \to A$;

* a [[function]] $(-)\cdot (-) : \mathbb{C} \times A \to A$;

* a [[function]] $\Vert-\Vert : A \to \mathbb{R}$;

* (partial) binary operations $+, \times : C \to A$

such that every set $S \subset A$ of elements that are pairwise in $C$ is contained in a set $T \subset A$ whose elements are also pairwise in $C$ and on which the above operations yield the structure of a commutative [[C-star algebra]].

A [[homomorphism]] of partial $C^\ast$-algebra is a function preserving this structure. This defines a [[category]] $PCstar$ of partial $C^\ast$ algebras.

=--


This appears as ([vdBergHeunen, def. 11,12](#vdBergHeunen)).


+-- {: .num_defn #PartialAlgebraOfNormalOperators}
###### Definition

For $A$ a [[C-star algebra]], write 

$$
  N(A) := \{a \in A | a a^* = a^* a\}
$$

for its set of [[normal operator]]s. This is naturally a [partial C-star algebra](#PartialCStar) with $C \subset N(A) \times N(A)$ the set of pairs of elements that commute in $A$.

=--


### The Bohr site
 {#BohrSite}

+-- {: .num_defn #PosetOfCommutativeSubalgebras}
###### Definition

For $A$ a [partial C-star algebra](#PartialCStar) write $\mathcal{C}(A)$ for the [[poset]] of total (not partial) commutative sub [[C-star algebra]]s. We call this the [[poset of commutative subalgebras]].

=--


+-- {: .num_prop }
###### Proposition

This construction extends to a functor

$$
  \mathcal{C} : C^* Alg \to Poset
  \,.
$$

to the [[category]] [[Poset]] of [[posets]]: for $f : A \to B$ a homomorphism we let $\mathcal{C}(f)$ be over any $C \in \mathcal{C}(A)$ be the [[image]] $im(f|_C) \in C^\ast Alg$ of the restriction of $f$ to $C$.

=--

+-- {: .num_remark }
###### Remark

By standard properties of [[C-star algebra]]s (see [here](http://ncatlab.org/nlab/show/C-star-algebra#General)), this 
image $im(f|_C)$ is simply the set-theoretic image $f(C)$.

=--

Notice the following fact about [[Alexandroff space]]s:

+-- {: .num_prop }
###### Proposition

The functor

$$
  Alex : Poset \to Top
$$

from [[posets]] to [[topological spaces]] that sends a poset $P$ to the topological space whose underlying set is the underlying set of $P$ and whose [[open subsets]] are the upward closed subsets $Up(P)$ exhibits an [[equivalence of categories]]

$$
  Poset 
    \underoverset{\simeq}{Alex}{\to}
  AlexTop
  \hookrightarrow
  Top
$$

of [[Poset]] with the [[full subcategory]] of [[Alexandroff space]]s.

=--

+-- {: .num_defn }
###### Definition

For $A \in C^* Alg$ we call $Alex \mathcal{C}(A)$ the **Bohr [[site]]** of $A$.

=--

+-- {: .num_defn }
###### Definition

A morphism $f : A \to B$ in $C^* Alg$ is called **commutativity reflecting** if for all $a_1, a_2 \in A$ we have that if $f(a_1)$ commutes with $f(a_2)$ in $B$ then already $a_1$ commutes with $a_2$ in $A$.

Write

$$
  C^* Alg_{cr} \subset C^* Alg
$$

for the [[subcategory]] of [[C-star algebra]]s on the commutativity-reflecting morphisms.

=--

+-- {: .num_remark }
###### Remark

Every [[monomorphism]] $A \hookrightarrow B$ in $C^* Alg$ is commutativity reflecting.

=--

+-- {: .num_prop #CommutativityReflectionByAdjoints}
###### Proposition

A morphism $f : A \to B$ in $C^* Alg$ is commutativity reflecting precisely if the morphism $\mathcal{C}(f)$ has a [[right adjoint]]

$$
  (\mathcal{C}(f) \dashv R_f)
  \;\colon\;
  \mathcal{C}(A)
   \stackrel{\overset{R_f}{\leftarrow}}{\underset{\mathcal{C}(f)}{\to}}
  \mathcal{C}(B)
  \,.
$$

=--

This appears as ([Nuiten 11, lemma 2.6](#Nuiten11)).

+-- {: .num_defn }
###### Definition

Write 

$$
  C^* Alg_{inc}
  \subset 
  C^* Alg_{cr}
  \subset
  C^* Alg
$$

for the subcategories of $C^* Alg$ on the monomorphisms and on the commutativity-reflecting morphisms, respectively.

=--



### The Bohr topos
 {#BohrTopos}


+-- {: .num_defn #CStarTopos}
###### Definition

Write

$$
  C^*_{com} Top \hookrightarrow C^*_{com} Topos
$$

for the categories of [[ringed spaces]] and [[ringed toposes]], where the [[internalization|internal]] ring object is equipped with the structure of an internal _commutative_ [[C-star algebra]] and the morphisms respect the $C^*$-algebra structure.

Hence a [[morphism]] $(\mathcal{E}, \underline{A}) \to (\mathcal{F}, \underline{B})$ in $C^\ast_{com} Topos$ is 

1. a [[geometric morphism]] $f : \mathcal{E} \to \mathcal{F}$ such that the [[inverse image]] $f^* \underline{B}$ is still an internal $C^\ast$-algebra in $\mathcal{E}$;

1. and a morphism of internal $C^\ast$-algebras

   $$
     f^\ast \underline{B} \to \underline{A}
   $$

   in $\mathcal{E}$.

=--

+-- {: .num_defn #TheSheafTopos}
###### Definition

For $A \in C^* Alg$ the **Bohr topos** of $A$ is the $C^\ast$-space/topos

$$
  Bohr(A) := ( Sh(Alex(\mathcal{C}(A))), \underline{A}) \in
  C^\ast_{com} Top \hookrightarrow C^\ast_{com} Topos
$$

whose underlying [[topological space]] is (that corresponding to) the [Bohr site](#BohrSite), and whose internal $C^\ast$-algebra is the tautological [[copresheaf]]

$$
  \underline{A} : (C \in \mathcal{C}(A)) \mapsto C
$$

in $[\mathcal{C}(A), Set] \simeq Sh(Alex(\mathcal{C}(A)))$ equipped with the evident objectwise commutative $C^\ast$-algebra structure.


Moreover, write

$$
  Bohr_{\not \not}(A)
  :=
  (Sh_{\not \not}(Alex \mathcal{C}(A)), \underline{A})
$$

for the $C^*$-topos whose underlying [[sheaf topos]] is that for the [[double negation topology]] on the plain Bohr topos.

=--

The general notion of [[morphism]]s between [[topos]]es are [[geometric morphism]]s. But those that remember the morphisms of Bohr sites are [[essential geometric morphism]]s. 

+-- {: .num_remark}
###### Remark

Every [[functor]] $f : \mathcal{C}(A) \to \mathcal{C}(B)$ induces an [[essential geometric morphism]] 

$$
  (f_! \dashv f^* \dashv f_*) : 
  [\mathcal{C}(A), Set]
    \stackrel{\overset{f_! := Lan_f}{\longrightarrow}}{\stackrel{\overset{f^* := (-) \circ f}{\leftarrow}}{\underset{f_* := Ran_f }{\longrightarrow}}}
  [\mathcal{C}(B), Set]   
$$

where $Lan_f$ and $Ran_f$ are left and right [[Kan extension]] along $f$, respectively.

We also write $[f,Set] : [\mathcal{C}(A), Set] \to [\mathcal{C}(B), Set]$ for this. Notice that by the equivalence of [[copresheaves]] on [[posets]] and [[sheaves]] on the corresponding [[Alexandroff locales]] (see there for details) this is equivalently

$$
  Sh (Alex(f))) : Sh(Alex \mathcal{C}(A)) \to Sh(Alex \mathcal{C}(B))
  \,.
$$

=--

The next proposition asserts that all essential geometric morphisms between Bohr toposes arise this way:

+-- {: .num_prop #EssentialGeomMorphismsAndPosetMorphisms}
###### Proposition

The [[2-functor]]

$$
  [-,Set] : Poset \hookrightarrow Topos_{ess}
$$

is a [[full and faithful 2-functor]].

Analogously, [[essential geometric morphism]]s of the underlying toposes $Bohr(A) \to Bohr(B)$ are precisely those in image under the functor $Sh \circ Alex$ of functors $\mathcal{C}(A) \to \mathcal{C}(B)$.

=--

+-- {: .proof}
###### Proof

By the discussion in the section _[In terms of essential geometric morphisms](http://ncatlab.org/nlab/show/Cauchy+complete+category#InOrdinaryCatTheoryByEssGeomMorphisms)_ at _[[Cauchy complete category]]_ we have a full and faithful embedding of Cauchy-complete catgeories $[-,Set] : Cat_{Cauchy} \hookrightarrow Topos_{ess}$. But posets are trivially Cauchy, complete, hence this restricts to an embedding $[-,Set] : Poset \hookrightarrow Cat_{Cauchy} \hookrightarrow Topos_{ess}$. 

In terms of Alexandroff topologies: by the discussion of [Alexandroff locales](http://ncatlab.org/nlab/show/specialization+topology#AlexandrovLocales) (in the entry _[[Alexandroff space]]_) we have that the functor $Alex\colon Poset \to Locale$ takes values precisely on those morphisms of locales whose inverse image has a [[left adjoint]]. The statement then follows using the properties of [[localic reflection]], which says that the [[2-functor]] $Sh : Locale \to Topos$ is a [[full and faithful 2-functor]].

=--

For such essential geometric morphisms to be parts of morphisms in 
$C^\ast Topos$, def. \ref{CStarTopos} we need that their [[inverse image]]s 
respect internal $C^\ast$-algebras:

+-- {: .num_prop }
###### Proposition

For $f : Bohr(A) \to Bohr(B)$ an essential geometric morphism, 
the [[inverse image]] $f^\ast \underline{B}$ is naturally a $C^\ast$-algebra in $[\mathcal{C}(A), Set]$.

=--

+-- {: .proof}
###### Proof

According to ([HLS09, 4.8](#HLSDeep)) every functor $\mathcal{C}(A) \to C^\ast Alg$ is an $C^\ast$-algebra [[internalization|internal to]] $[\mathcal{C}(A), Set]$. Here $f^* \underline{B}$ is such a functor, sending $(C \in \mathcal{C}(A)) \mapsto im_f(C)$.

=--

Using this we now discuss morphisms of Bohr toposes in $C^\ast Topos$.

+-- {: .num_prop #BohrFunctoriality}
###### Proposition

The construction of Bohr toposes from 
def. \ref{TheSheafTopos} extends to a [[functor]] of the form

$$
  Bohr 
  : 
  C^\ast Alg_{cr}^{op} 
    \to 
  C^\ast_{com} TopSpace 
    \hookrightarrow 
  C^\ast_{com} Topos
$$

with the special property that any $f : A \to B$ is sent to

* an [[essential geometric morphisms]] $(f^* \dashv f_*) : Bohr(B) \to Bohr(A)$ with an extra [[right adjoint]]

  $$
    Bohr(B)
     \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\stackrel{\overset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}}
    Bohr(A)
  $$

* such that the corresponding internal [[homomorphism]] of internal algebras $\underline{A} \to f_* \underline{B}$ is an [[epimorphism]].

=--

This is ([Nuiten 11, lemma 2.7](#Nuiten11)). (Essentially this argument also appears as ([vdBergHeunen, prop. 33](#vdBergHeunen)), where however the extra right adjoint is not made use of and instead the variances of the morphisms involved in the definition of $C^\ast Topos$ are redefined in order to make the statement come out.)

+-- {: .proof}
###### Proof

To a morphism $f : A \to B$ in $C^\ast Alg_{cr}$ which by prop. \ref{CommutativityReflectionByAdjoints} corresponds to an [[adjoint pair]]

$$
  ( \mathcal{C}(f) \dashv R_f) : 
  \mathcal{C}(A)
   \stackrel{\overset{R_f}{\leftarrow}}{\underset{\mathcal{C}(f)}{\to}}
  \mathcal{C}(B)
$$

we assign the [[essential geometric morphism]]

$$
  (f_! \dashv f^* \dashv f_* \dashv f^!)
  :=
  [\mathcal{C}(B), Set]
   \stackrel{\overset{f_! := Lan_{R_f}}{\longrightarrow}}{\stackrel{\overset{f^* := (-)\circ R_f}{\leftarrow}}{\stackrel{\overset{f_* := (-)\circ \mathcal{C}(f)}{\longrightarrow}}{\underset{f^! := Ran_{\mathcal{C}(f)}}{\leftarrow}}}}
  [\mathcal{C}(A), Set]
$$

(wher $Lan$ and $Ran$ denote left and right [[Kan extension]], respectively) equipped with the morphism of internal $C^*$-algebras

$$
  \eta_f : \underline{A} \to f_* \underline{B}
$$

which over $C \in \mathcal{C}(A)$ is the restriction of $f$ to $C$ and [[corestriction]] to $\mathcal{C}(f)(C)$

$$
  f|_C : C \to \mathcal{C}(f)(C)
$$

(to the $C^\ast$-completion of the algebraic image of $f|_C$).

=--


Using prop. \ref{EssentialGeomMorphismsAndPosetMorphisms} the above prop. \ref{BohrFunctoriality} has the following partial converse.

+-- {: .num_prop #ToposCharacterizationOfAlgebraHomomorphisms}
###### Proposition

For $A, B \in C^\ast Alg$,  morphisms $f : Bohr(B) \to Bohr(A)$ in $C^\ast Top$ for which 

1. the underlying geometric morphism has an extra right adjoint 

1. the morphism of internal algebras $\underline{A} \to f_* \underline{B}$ is an [[epimorphism]]

are in bijection with [[function]]s

$$
  f : A \to B
$$

that are [[homomorphism]]s on all commutative subalgebras and reflect commutativity.

In particular when $A$ is already commutative, morphisms $Bohr(B) \to Bohr(A)$ with an extra right adjoint and epi ring homomorphism are in bijection with algebra homomorphisms $A \to B$.

=--

+-- {: .proof}
###### Proof

By prop \ref{EssentialGeomMorphismsAndPosetMorphisms} every [[essential geometric morphism]] $Sh(Alex \mathcal{C}(A)) \to Sh(Alex \mathcal{C}(B))$ comes from a morphism of locales $Alex \mathcal{C}A \to Alex \mathcal{C}A$, which by the discussion at [[Alexandroff space]] is equivalently a morphism of posets $\mathcal{C}(f) : \mathcal{C}(A) \to \mathcal{C}(B)$. By the assumption of the extra right adjoint we also have a geometric morphism the other way round, and hence, again by prop. \ref{EssentialGeomMorphismsAndPosetMorphisms}, an [[adjoint pair]]

$$
  (\mathcal{C}(f) \dashv R_f) : \mathcal{C}(A) \leftrightarrow \mathcal{C}(B)
$$

that induces functors between toposes as in prop. \ref{BohrFunctoriality}.
Then the fact that $f$ is a morphism of $C^\ast$-toposes implies 
algebra homomorphisms

$$
  f_C : C \to f(C)
$$

[[natural transformation|natural]] in $C \in \mathcal{C}(A)$.

By the assumption that this are the components of an [[epimorphism]] 
of [[copresheaves]] all these component morphisms are themselves epimorphisms and hence we have that indeed $f(C) = image_{f_C}(C)$.

=--





## Kinematics in a Bohr topos
 {#KinematicsOnBohrTopos}


A key aspect of the Bohr topos $Bohr(A)$ of a [[quantum mechanical system]] (as defined [above](#BohrToposOfQMSystem)) is that that _classical_ [[kinematics]] and classical [[probability theory]] of the commutative _internal_ $C^*$-algebra $\underline{A} \in Bohr(A)$ is the _quantum_ [[kinematics]] and [[quantum probability theory]] of $A$. 

In fact, the very definition of $Bohr(A)$ provides a formal context in which [[Gleason's theorem]] has a natural formulation:

+-- {: .num_theorem }
###### Theorem 
**(Gleason's theorem)**

For $H$ a [[Hilbert space]] of [[dimension]] $dim H \gt 2$, and $A = B(H) \in C^\ast Alg$ its algebra of [[bounded operators]], a [[state]] on $A$ is a [[function]]

$$
  \rho : A \to \mathbb{C}
$$

which is a $\mathbb{C}$-[[linear map]] when restricted to each commutative subalgebra $C \subset A$.

=--

A function that preserves certain [[structure]] locally -- here: over each commutative subalgebra -- is precisely an [[internalization|internal]] fully structure preserving [[homomorphism]] in the [[presheaf topos]] over these local objects -- here: over commutative subalgebras. Hence we have the following direct topos-theoretic equivalent reformulation of Gleason's theorem.

+-- {: .num_cor }
###### Corollary

For $A = B(H) \in C^\ast Alg$ as above, we have a natural bijection between the quantum [[state]]s on $A$ and the  (classical) states of $\underline{A}$ [[internalization|internal to]] $Bohr(H)$.

=--


### The phase space
 {#ThePhaseSpace}

The idea is that for $A \in C^* Alg$, the Bohr topos 
$Bohr(A) = (Sh(Alex(\mathcal{C}(A))), \underline{A}) \in C^* TopSpace \subset C^* Topos$ _is_ the corresponding quantum [[phase space]].  More precisely, we may think of the internal commutative $C^*$-algebra $\underline{A} \in Bohr(A)$ as the [[Isbell duality|formal dual]] to the quantum phase space.

The following discussion makes this precise by exhibiting this formal dual as an [[internal locale]]. Since $Bohr(A)$ is a [[spatial topos]], this internal locale is in fact an ordinary [[topological space]] [[bundle]] $\Sigma \to Alex \mathcal{C}(A)$ over the [[Alexandroff space]] $Alex \mathcal{C}(A)$.

+-- {: .num_defn #TheInternalLocale}
###### Definition


Write $\underline{\Sigma}_A$ and $\Sigma_A^{\not \not}$, respectively for the corresponding [[internal locale]]s associated to $\underline{A}$ by internal [[constructive Gelfand duality]]. Write 

$$
  \Sigma_A \to \mathcal{C}(A)
$$ 

and

$$
  \Sigma^{\not \not}_A \to \mathcal{C}(A)
$$ 

for the corresponding external locale, given under the [[equivalence of categories]]

$$
  Loc(Sh(\mathcal{C}(A))) \simeq Loc/\mathcal{C}(A)
$$

discussed at [[internal locale]].

=--

+-- {: .num_defn #Bohrification}
###### Definition

For $A$ a (noncommutative) [[C-star algebra]], the assignment

$$
  A \mapsto \Sigma_{A}
$$

or 

$$
  A \mapsto \Sigma^{\not \not}_{A}
$$

is called the **Bohrification** of $A$.

=--


+-- {: .num_prop #TheInternalLocale}
###### Proposition

Let $\underline{\Sigma}(\underline(A))$ be the [[internal locale]] from def. \ref{TheInternalLocale}.

Regarded as an object 

$$
  (\Sigma_A \to \mathcal{C}(A))
  \in
  Loc/\mathcal{C}(A)
$$ 

of external locales over $\mathcal{C}(A)$, this is the [[topological space]] whose underlying set is given by the disjoint union

$$
  \Sigma_A = \coprod_{C \in \mathcal{C}(A)} \Sigma(C)
$$

over all commutative $C^*$-subalgebras of $A$ of the ordinary [[Gelfand spectrum|Gelfand spectra]] $\Sigma(C)$ of these commutative $C^*$-algebras, and whose [[open subset]]s are defined to be those $\mathcal{U} \subset \Sigma_A$ for which

1. $\mathcal{U}|_C \in \mathcal{O}(\Sigma(C))$ for all commutative subalgebras $C$;

1. For all $C \hookrightarrow D$, if $\lambda \in \mathcal{U}|_C$ and $\lambda' \in \Sigma(D)$ such that   $\lambda'|_C = \lambda$, then $\lambda' \in \mathcal{U}|_D$.

Regarded equivalently as an [[internal locale]] in $Sh(\mathcal{C}(A))$ this  

As a [[presheaf]] on the poset $\mathcal{C}(A)$ this is given by

$$
  \underline{\Sigma}(\underline{A})
  :
  U \mapsto \Sigma_U
  \,,
$$

where for $U \in \mathcal{O}(\mathcal{C}(A))$ we set

$$
  \Sigma_U := \coprod_{C \in U} \Sigma(C)
$$

with the relative topology inherited from $\Sigma_A$.


=--

This appears as ([HLSW, theorem 1](#HLSW)).


+-- {: .num_prop #BohrificationDependsOnNormalElementsOnly}
###### Proposition

The Bohrification of $A \in ncCStar$ only depends on its [partial C-star algebra](#PartialCStar) $N(A)$ of normal elements

$$
  \Sigma_A \simeq \Sigma_{N(A)}
  \,.
$$

=--

This is highlighted in ([vdBergHeunen](#vdBergHeunen)).

+-- {: .num_prop #ReproducingOrdinaryGelfandDuality}
###### Proposition

For $A$ a commutative $C^\ast$-algebra and $\Sigma_A^{Gelf} \in $ [[Loc]] its ordinary [[Gelfand spectrum]], we have that Bohrification in the double negation topology reproduces this ordinary Gelfand spectrum:

$$
  \Sigma^{\not \not}_A \simeq \Sigma_A^{Gel}
  \,.
$$

=--

This is ([Spitters06, theorem 9, corollary 10](#Spitters06)).

+-- {: .num_prop #FunctorToRingedToposes}
###### Proposition

Then the construction of the [[ringed topos]] over the [[poset of commutative subalgebras]]

$$
  A \mapsto ([\mathcal{C}(A), Set], \underline{A})
$$

extends to a functor

$$
  C^* Alg_{incl} \to C^*TopSpace \hookrightarrow C^* Topos
  \,,
$$


where on the right the morphisms of internal rings are even morphisms of internal [[C* algebras]].

=--

+-- {: .proof}
###### Proof

With the components of the morphism of internal rings the evident objectwise inclusions, this is directly checked.

=--

+-- {: .num_prop #BohrificationFunctorToLoc}
###### Proposition

Let $Cstar_{inc}$ be the [[category]] of [[C-star algebra]]s and inclusions. Then [Bohrification](#Bohrification) extends to a [[functor]]

$$
  \Sigma_{(-)} : CStar_{inc}^{op} \to Loc
  \,.
$$

=--

This is effectively the functoriality of the internal [[constructive Gelfand duality]] applied to the [above observation](#FunctorToRingedToposes). The statement appears as ([vdBergHeunen, theorem 35](#vdBergHeunen)). 


### The observables
 {#TheObservables}

For $A \in C^\ast Alg$ a [[C*-algebra]], then in [[quantum physics]] a [[self-adjoint operator]] $a \in A$ is a _quantum [[observable]]_. The following statement asserts that quantum observables on $A$ are in a precise sense the $\mathbb{R}$-valued "functions" on the Bohr topos of $A$.

Write $C(\mathbb{R})$ for the $C^\ast$-algebra of continuous complex functions on the [[real line]]. We think of $Bohr(C(\mathbb{R}))$ as the incarnation of $\mathbb{R}$ in the context of Bohr toposes.


+-- {: .num_prop }
###### Proposition

Morphisms $f : Bohr(A) \to Bohr(C(\mathbb{R})_0)$ with an extra right adjoint and $C(\mathbb{R})_0 \to f_*\underline{A}$ epi are in bijection to the observables on $A$.

=--

+-- {: .proof}
###### Proof

By prop. \ref{ToposCharacterizationOfAlgebraHomomorphisms}
such morphisms are in bijection to algebra homomorphisms

$$
  C(\mathbb{R})_0 \to A
  \,.
$$

By [[functional calculus]]: every [[self-adjoint operator]] $a \in A$ provides such a homomorphism by $f \mapsto f(a)$. Conversely, given such an algebra homomorphism, its image of $i : x \mapsto x$ is a self-adjoint operator in $A$, and these two constructions are clearly inverses of each other.

=--

+-- {: .num_remark }
###### Remark

In the different but related context of the [[spectral presheaf]] ([Isham-D&#246;ring 07](#IshamDoering07)) the identification of [[quantum observables]] with a topos-theoretic construction, as far as possible, has been called "[[daseinisation]]". This is a bit more involved than the above direct characterization in terms of maps of [[ringed toposes]].

=--

+-- {: .num_remark }
###### Remark

Let $x_{t_1} \in A$ be an observable and write $\langle x_{t_1} \rangle$ for the subalgebra generated by it. Then (by general properties of [presheaf over-toposes](#http://ncatlab.org/nlab/show/over-topos#PresheafOverTopos)) the [[slice topos]] $Bohr(A)_{/\langle x_{t_1}\rangle}$ is [[equivalence of categories|equivalent]] to

$$
  Bohr(A)_{/\langle x_{t_1}\rangle}
  \simeq
  [\langle x_{t_1}\rangle_{/\mathcal{C}(A)}, Set]
  \,,
$$

where on the right we have the [[copresheaves]] over the [[under-category]] $\langle x_{t_1}\rangle_{/\mathcal{C}(A)}$. This is precisely the sub-[[poset of commutative subalgebras]] on those commutative subalgebras that contain $x_{t}$. This means that a classically consistent observation in the slice topos is one that is consistent with the observation of $x_{t_1}$.

=--

### The states


+-- {: .num_defn }
###### Definition

For $A \in C^\ast Alg$ write 
$(Sh(Alex \mathcal{C}(A)), \mathbb{R})$ for the [[ringed topos]] as indicated, where $\mathbb{R}$ denotes the copresheaf constant on $\mathbb{R}$.

The internal $C^\ast$-algebra $\underline{A} \in Bohr(A)$ is an internal $\mathbb{R}$-module. Forgetting the algebra structure and only remembering the $\mathbb{R}$-module structure, we get a category of "$\mathbb{R}$-module toposes".

=--

+-- {: .num_prop }
###### Observation

There is a canonical morphism of ringed toposes

$$
  \pi : Bohr(A) \to (Sh(Alex \mathcal{C}(A)), \mathbb{R})
$$

whose underlying geometric morphism is the identity (and whose morphism of internal ring objects is the unique one).

=--

+-- {: .num_remark }
###### Remark

This [[bundle]] is the $C^\ast$-topos incarnation of the morphism $\Sigma \to Alex \mathcal{C}(A)$ of locales discussed [above](ThePhaseSpace).

=--


+-- {: .num_prop }
###### Observation

A [[state]] $\rho$ on $A$ is a [[section]] of $\pi$ in the category
of $\mathbb{R}$-moduled toposes that is positive and normalized.

=--

(...)

## (Pre-)Sheaf of Bohr toposes of a quantum field theory
 {#SheafOfBohrToposesOfQFT}


Notice that in the context of [[AQFT]] a [[quantum field theory]] is encoded by a [[local net]] of [[C-star algebra]]s on [[spacetime]].

+-- {: .num_note #PresheavesFromLocalNets}
###### Note

Let $X$ be a [[Lorentzian manifold]] and 

$$
  A : \mathcal{O}(X) \to C^* Alg_{inc}
$$

be a [[local net]] of algebras. Notice that by definition this indeed takes values in $C^\ast$-algebras and _inclusions_ . Then postcomposition with the [Bohr topos](#BohrTopos)-functor yields a presheaf of ringed spaces

$$
  Bohr(A) : \mathcal{O}(X)^{op} 
    \to 
  C^* Alg_{inc}^{op}
   \hookrightarrow 
  C^* Alg_{cr}^{op}
   \stackrel{Bohr}{\to}
  C^* TopSpace
   \hookrightarrow
  C^* Topos
  \,.
$$

=--

This appears as ([Nuiten 11, def. 17](#Nuiten11)).


Assume that a net of observables $A : Op(X) \to C^\ast Alg_{inc}$
satisfies the [[split property]]. Then it is []() precisely if the corresponding presheaf of Bohr toposes
$Bohr(A) : Op(X)^{op} \stackrel{A}{\to} C^\ast Alg_{inc} \stackrel{Bohr}{\to} C^\ast Top$ satisfies _spatial_ [[descent]] by [[local geometric morphism]]s (meaning that for every spatial hyperslice $\Sigma \subset X$ the induced presheaf $Bohr(A)|_\Sigma : Op(\Sigma)^{op} \to C^\ast Top$ satisfies [[descent]] by [[local geometric morphism]]s.)

(...)

This appears as ([Nuiten 11, theorem 4.2](#Nuiten11)).


## Contravariant functors on open subsets

Above is discussed the notion of Bohr topos given by [[covariant functors]] on the [[poset of commutative subalgebras]] of a [[C*-algebra]]. The fact that the functors here are covariant is related to the fact that the algebra itself naturally exists inside the presheaf topos.

Alternatively one can explore the situation for [[contravariant functors]] on the [[poset of commutative subalgebras]] ([Isham-D&#246;ring 07](#IshamDoering07)).  The resulting [[presheaf topos]] then does not directly contain the given $C^\ast$-algebra, but by [[Gelfand duality]], does directly contain an internal [[locale]] which is its [[Gelfand spectrum]]. This is called the "[[spectral presheaf]]". 



## Related concepts

* [[quantum logic]]

[[!include states and observables -- content]]




## References
 {#References}

The assertion by Bohr that all experiments in quantum mechanics must be possible to describe in "classical terms" is in

* {#Bohr49} [[Niels Bohr]],  *Discussion with Einstein on Epistemological Problems in Atomic Physics*, in: P. A. Schilpp (ed.) *Albert Einstein, Philosopher-Scientist* (Evanston: Library of Living Philosophers) (1949) 201-241 &lbrack;<a href="https://doi.org/10.1016/S1876-0503(08)70379-7">doi:10.1016/S1876-0503(08)70379-7</a>&rbrack;

  > "however far the phenomena transcend the scope of classical physical explanation, the account of all evidence must be expressed in classical terms."

[[Niels Bohr]]'s views on quantum mechanics that give the construction of _Bohrification_ its name are reviewed further in

* {#Scheibe73} [[Erhard Scheibe]], *Bohr's interpretation of quantum mechanics*, Chapter I in: _The logical analysis of quantum mechanics_, Oxford: Pergamon Press (1973)


For more see at _[[interpretation of quantum mechanics]]_ the section _[Bohr's standpoint](interpretation+of+quantum+mechanics#BohrStandpoint)_.

Maybe the first article to propose to use [[intuitionistic logic]]/[[topos theory]] for the description of quantum physics is

* Murray Adelman, John Corbett, *A Sheaf Model for Intuitionistic Quantum Mechanics*, Appl. Cat. Struct. **3**  (1995) 79-104 &lbrack;[doi:10.1007/BF00872949](https://doi.org/10.1007/BF00872949)&rbrack;

The term _Bohrification_ and the investigations associated with it were initiated in

* {#HeunenLandsmanSpitters09} [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], *Bohrification of operator algebras and quantum logic*, Synthese **186** 3 (2012) 719-752 &lbrack;[arXiv:0905.2275](http://arxiv.org/abs/0905.2275), [doi;10.1007/s11229-011-9918-4](https://doi.org/10.1007/s11229-011-9918-4)&rbrack;
  
see also related comments in disucssion of the [[Born rule]] here:

* [[Klaas Landsman]], *The Born rule and its interpretation*, in: *Compendium of Quantum Physics*, Springer (2009) 64-70 &lbrack;[doi:10.1007/978-3-540-70626-7_20](https://doi.org/10.1007/978-3-540-70626-7_20), [pdf](https://www.math.ru.nl/~landsman/Born.pdf), [[Landsman-BornRule.pdf:file]]&rbrack;


See also:

* {#HLSDeep} [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], _Bohrification_, in: *Deep Beauty -- Understanding the Quantum World through Mathematical Innovation*, Cambridge University Press (2009) 271-314 &lbrack;[arXiv:0909.3468](http://arxiv.org/abs/0909.3468), [doi:10.1017/CBO9780511976971.008](https://doi.org/10.1017/CBO9780511976971.008)&rbrack;
 


The computation of the internal Gelfand spectrum $\underline{\Sigma}$ was initiated in 

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]] _A topos for algebraic quantum theory_, Comm. Math. Phys. **291**  (2009) 63-110 &lbrack;[arXiv:0709.4364](http://arxiv.org/abs/0709.4364), [doi:10.1007/s00220-009-0865-6](http://dx.doi.org/10.1007/s00220-009-0865-6)&rbrack;

with some results in section 5 and 6 of 

* Martijn Caspers, _Gelfand spectra of $C^*$-algebras in topos theory_, MSc thesis, Nijmegen (2008) &lbrack;[pdf](http://www.math.ru.nl/~landsman/scriptieMartijn.pdf), [[Caspers-GelfandSpectra.pdf:file]]&rbrack;

and completed in 

* Sander Wolters, _Contravariant vs covariant quantum logic: A comparison of two topos-theoretic approaches to quantum theory_, Comm. Math. Phys. **317** (2013) 3–53 &lbrack;[arXiv:1010.2031](http://arxiv.org/abs/1010.2031), [doi:10.1007/s00220-012-1652-3](https://doi.org/10.1007/s00220-012-1652-3)&rbrack;

An outline of the full proof is given in 

* {#HLSW} [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], Sander Wolters, _The Gelfand spectrum of a noncommutative $C^\ast$-algebra: a topos-theoretic approach_, Journal of the Australian Mathematical Society **90** (2011) 39-52 &lbrack;[arxiv:1010.2050](http://arxiv.org/abs/1010.2050), [doi:10.1017/S1446788711001157](https://doi.org/10.1017/S1446788711001157)&rbrack;
 

Applications and examples for $A$ a [[matrix]] algebra are discussed in 

* Martijn Caspers, [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], _Intuitionistic Quantum Logic of an $n$-level System_, Foundations of Physics **39** 7 (2009) 731-759 &lbrack;[arXiv:0902.3201](https://arxiv.org/abs/0902.3201), [doi:10.1007/s10701-009-9308-7](https://doi.org/10.1007/s10701-009-9308-7)&rbrack;

The [[functor|functoriality]] of Bohrification is observed in 

* {#vdBergHeunen} [[Benno van den Berg]], [[Chris Heunen]], _Noncommutativity as a colimit_, Applied Categorical Structures **20** 4 (2012) 393-414 &lbrack;[arXiv:1003.3618](http://arxiv.org/abs/1003.3618), [doi:10.1007/s10485-011-9246-3](https://doi.org/10.1007/s10485-011-9246-3)&rbrack;
 

The application of the [[double negation topology]] to make Bohrification coincide with ordinary [[Gelfand duality]] on commutative $C^*$-algebras is discussed in 

* {#Spitters06} [[Bas Spitters]], _The space of measurement outcomes as a spectrum for non-commutative algebras_, EPTCS **26** (2010) 127-133 &lbrack;[arXiv:1006.1432](http://arxiv.org/abs/1006.1432), [doi:10.4204/EPTCS.26.12](https://doi.org/10.4204/EPTCS.26.12)&rbrack;


The generalization of Bohrification from [[quantum mechanics]] to [[quantum field theory]] ([[AQFT]]):

* {#Nuiten11} [[Joost Nuiten]], _[[schreiber:bachelor thesis Nuiten|Bohrification of local nets of observables]]_, in: *Proceedings of [QPL 2011](http://qpl.science.ru.nl/)*, [EPTCS 95, 2012](http://rvg.web.cse.unsw.edu.au/eptcs/content.cgi?QPL2011) (2012) 211-218 &lbrack;[arXiv:1109.1397](http://arxiv.org/abs/1109.1397),   [doi:10.4204/EPTCS.95.15](https://dx.doi.org/10.4204/EPTCS.95.15)&rbrack;

Review: 

* {#Landsman17} [[Klaas Landsman]], *Topos theory and quantum logic*, Section 12 of: _Foundations of quantum theory -- From classical concepts to Operator algebras_, Springer Open (2017) &lbrack;[doi:10.1007/978-3-319-51777-3](https://link.springer.com/book/10.1007/978-3-319-51777-3), [pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-51777-3.pdf)&rbrack;



The original suggestion to interpret the [[Kochen-Specker theorem]] in the topos over the [[poset of commutative subalgebras]] (there taken to be [[presheaves]] instead of [[copresheaves]]) is due to

* {#ButterfieldHamiltonIsham} [[Jeremy Butterfield]],  John Hamilton, [[Chris Isham]], _A topos perspective on the Kochen-Specker theorem_, _I. quantum states as generalized valuations_, Internat. J. Theoret. Phys. **37** 11 (1998) 2669-2733 &lbrack;[doi:10.1023/A:1026680806775](http://dx.doi.org/10.1023/A:1026680806775), [arXiv:quant-ph/9803055](https://arxiv.org/abs/quant-ph/9803055), [MR2000c:81027](http://www.ams.org/mathscinet-getitem?mr=1669557)&rbrack; 

  _II. conceptual aspects and classical analogues_ Int. J. of Theor. Phys. **38**  3 (1999) 827-859 &lbrack;[MR2000f:81012](http://www.ams.org/mathscinet-getitem?mr=1697983), [doi:10.1023/A:1026652817988](http://dx.doi.org/10.1023/A:1026652817988)&rbrack;

  _III. Von Neumann algebras as the base category_, Int. J. of Theor. Phys. **39** 6 (2000) 1413-1436 &lbrack;[arXiv:quant-ph/9911020](http://arxiv.org/abs/quant-ph/9911020), [MR2001k:81016](http://www.ams.org/mathscinet-getitem?mr=1788498),[doi:10.1023/A:1003667607842](http://dx.doi.org/10.1023/A:1003667607842)&rbrack; 

  _IV. Interval valuations_, Internat. J. Theoret. Phys. __41__ 4 (2002) 613-639 &lbrack;[MR2003g:81009](http://www.ams.org/mathscinet-getitem?mr=1902067), [doi](http://dx.doi.org/10.1023/A:1015276209768)&rbrack; 

with some review and outlook in

* [[Chris Isham]], [[Jeremy Butterfield]], *Some Possible Roles for Topos Theory in Quantum Theory and Quantum Gravity*, Found. Phys. **30** (2000) 1707-1735 &lbrack;[arXiv:gr-qc/9910005](https://arxiv.org/abs/gr-qc/9910005), [doi:10.1023/A:1026406502316](https://doi.org/10.1023/A:1026406502316)&rbrack;

and then

* {#IshamDoering07} [[Andreas Döring]], [[Chris Isham]], _A Topos Foundation for Theories of Physics_  

  *I. Formal Languages for Physics*, J. Math. Phys. **49** (2008) 053515 &lbrack;[arXiv:quant-ph/0703060](http://arxiv.org/abs/quant-ph/0703060), [doi:10.1063/1.2883740](https://doi.org/10.1063/1.2883740)&rbrack;


  *II. Daseinisation and the Liberation of Quantum Theory*, J. Math. Phys. **49** (2008) 053516
  &lbrack;[arXiv:quant-ph/0703062](http://arxiv.org/abs/quant-ph/0703062), [doi:10.1063/1.2883742](https://doi.org/10.1063/1.2883742)&rbrack;

  *III. The Representation of Physical Quantities With Arrows*, J. Math. Phys. **49** (2008) 053517 &lbrack;[arXiv:quant-ph/0703064](https://arxiv.org/abs/quant-ph/0703064), [doi:10.1063/1.2883777](https://doi.org/10.1063/1.2883777)&rbrack;

  *IV. Categories of Systems*, J. Math. Phys. **49** (2008) 053518 &lbrack;[arXiv:quant-ph/0703066](http://arxiv.org/abs/quant-ph/0703066), [doi:10.1063/1.2883826](https://doi.org/10.1063/1.2883826)&rbrack;
  
Further development in:

* [[John Harding]], [[Chris Heunen]], *Topos quantum theory with short posets*, Order **38** 111–125 (2021) &lbrack;[arXiv:1903.01897](https://arxiv.org/abs/1903.01897), [doi:10.1007/s11083-020-09531-6](https://doi.org/10.1007/s11083-020-09531-6)&rbrack;



Discussion of aspects of the process of [[quantization]] in terms of Bohr toposes is in 

* Kunji Nakayama, _Sheaves in Quantum Topos Induced by Quantization_ &lbrack;[arXiv:1109.1192](http://arxiv.org/abs/1109.1192)&rbrack;

A variant of the Bohr topos construction meant to take more of the topology of the underlying $C^\ast$-algebra into account has been suggested for finite-dimensional $C^\ast$-algebra in 

* Guillaume Raynaud, _Fibred contextual quantum physics_, PhD thesis, University of Birmingham, 2014. &lbrack;[web](http://www.cs.bham.ac.uk/~sjv/grpage.php)&rbrack;

and generalized to arbitrary $C^\ast$-algebras in 

* [[Simon Henry]], _A Geometric Bohr topos_ &lbrack;[arXiv:1502.01896](https://arxiv.org/abs/1502.01896)&rbrack;

[[!redirects Bohr topos]]
[[!redirects Bohr toposes]]
[[!redirects Bohrification]]

[[!redirects Nuiten's lemma]]
