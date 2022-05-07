
> For the use of "categorical"/"categorial" below, see at _[[categorical semantics]]_ the section on [Terminology](categorical+semantics#Terminology).

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

Linear logic is sometimes thought of as being a logic for arguing about resource sensitive issues, but it can also be thought of categorically, or interpreted using Game Semantics, or as being related to Petri nets, or as a particular form of [[quantum logic]]. A bit more formally: 

**Linear logic** is a [[substructural logic]] in which the [[contraction rule]] and the [[weakening rule]] are omitted, or at least have their applicability restricted.  

In the original definition of ([Girard 87](#Girard)) linear logic is the [[internal logic]] of/has [[categorical semantics]] in [[star-autonomous categories]] ([Seely 89, prop. 1.5](#Seely)). But more generally _linear logic_ came to refer to the [[internal logic]] of any possibly-non-[[cartesian monoidal category|cartesian]] [[symmetric monoidal category|symmetric]] [[closed monoidal category]] (then usually called _multiplicative intuitionistic linear logic_ -- _MILL_) or even [[polycategory]] ([Szabo 78](#Szabo78) see the [history section](linear%20type%20theory#HistoryCategoricalSemantics) and see also [de Paiva 89](#dePaiva89), [Blute 91](#Blute91), [Benton--Bierman--de Paiva--Hyland 92](#BentonBiermanPaivaHyland92), [Hyland--de Paiva 93](#HylandPaiva93), [Bierman 95](#Bierman95), [Barber 97](#Barber97), [Schalk 04](#Schalk04), [Melli&#232;s 09](#Mellies09)). Under this interpretation, _[[proof nets]]_ (or the associated [[Kelly–Mac Lane graphs]]) of linear logic are similar to [[string diagrams]] for monoidal categories.  

Indeed, these more general senses of linear logic still faithfully follow the original motivation for the term "linear" as connoting "resource availability" explained below (and in [Girard 87](#Girard87)), since the non-cartesianness of the [[tensor product]] means the absence of a [[diagonal]] map and hence the impossibility of [[functions]] to depend on more than a single (linear) copy of their [[variables]].

In addition to these usual "denotational" categorical semantics, linear logic also has an "operational" categorical semantics, called the _[[Geometry of Interaction]]_, in [[traced monoidal categories]].

Although linear logic is traditionally presented in terms of inference rules, it was apparently discovered by Girard while studying [[coherence
spaces]].

### Quantum logic

Linear logic and [[linear type theory]] can be argued to be the proper incarnation of _[[quantum logic]]_ (see there for references). In this context the linearity of the logic, hence the absence of [[diagonal]] maps in its [[categorical semantics]] (in non-[[cartesian monoidal category|cartesian]] [[symmetric monoidal categories]]) reflects the _[[no-cloning theorem]]_ of [[quantum physics]].

### Resource availability

Unlike traditional [[logics]], which deal with the _[[truth]]_ of
_[[propositions]]_, linear logic is often described as dealing
with the _availability_ of _resources_.  A proposition, if it is
true, remains true no matter how we use that fact in proving
other propositions.  By contrast, in using a resource $A$ to
make available a resource $B$, $A$ itself may be consumed or
otherwise modified.  Linear logic deals with this by
restricting our ability to duplicate or discard resources
freely.  For example, we have

$$\text{have cake} \vdash \text{eat cake}$$

from which we can prove

$$\text{have cake},\; \text{have cake} \vdash \text{have cake}
\wedge \text{eat cake}$$

which by left [[contraction rule|contraction]] (duplication of inputs) in [[classical logic]] yields

$$\text{have cake} \vdash \text{have cake} \wedge \text{eat cake}$$

Linear logic would disallow the contraction step and treat
$\text{have cake},\; \text{have cake} \vdash A$ as explicitly
meaning that _two_ slices of cake yield $A$.  Disallowing contraction then corresponds to the fact that we can't turn one slice of cake into two (more's the pity), so you can\'t have your cake and eat it too.


### Game semantics

Linear logic can also be interpreted using a semantics of "games" or "interactions".  Under this interpretation, each proposition in a sequent represents a game being played or a transaction protocol being executed.  An assertion of, for instance,

$$ P, Q \vdash R $$

means roughly that if I am playing three simultaneous games of $P$, $Q$, and $R$, in which I am the left player in $P$ and $Q$ and the right player in $R$, then I have a strategy which will enable me to win at least one of them.  Now the above statements about "resources" translate into saying that I have to play in all the games I am given and can't invent new ones on the fly.

For example, $P \vdash P$ can be won by using the copycat strategy where one makes the two games identical except with left and right players reversed.

### As a relevant logic

Linear logic is closely related to notions of [[relevant logic]], which have been studied for much longer.  The goal of relevant logic is to disallow statements like "if pigs can fly, then grass is green" which are true, under the usual logical interpretation of [[implication]], but in which the hypothesis has nothing to do with the conclusion.  Clearly there is a relationship with the "resource semantics": if we want to require that all hypotheses are "used" in a proof then we need to disallow weakening.




## Definition

Linear logic is usually given in terms of [[sequent calculus]].  There is a set of __[[propositions]]__ (although as remarked above, to be thought of more as resources to be acquired than as statements to be proved) which we construct through [[recursion]].  Each pair of [[lists]] of propositions is a __sequent__ (written as usual with '$\vdash$' between the lists), some of which are __valid__; we determine which are valid also through recursion.  Technically, the [[propositional calculus]] of linear logic also requires a set of __propositional variables__ from which to start; this is usually identified with the set of [[natural numbers]] (so the variables are $p_0$, $p_1$, etc), although one can also consider the linear logic $LL(V)$ where $V$ is any initial [[set]] of propositional variables.

Here we define the set of propositions:


*  Every propositional variable is a proposition.
*  For each proposition $A$, there is a proposition $A^\perp$, the __[[negation]]__ of $A$.
*  For each proposition $A$ and proposition $B$, there are four additional propositions:
   *  $A \& B$ (read 'with'), the __additive [[logical conjunction|conjunction]]__ of $A$ and $B$;
   *  $A \oplus B$ (read 'plus'), the __additive [[disjunction]]__ of $A$ and $B$;
   *  $A \otimes B$ (read 'times'), the __[[multiplicative conjunction]]__ of $A$ and $B$;
   *  $A \parr B$ (read 'par' and sometimes written $A \mid B$), the __[[multiplicative disjunction]]__ of $A$ and $B$.
*  There are also four constants to go with the four binary operations above:
   *  $\top$ (read 'top'), the __additive [[truth]]__;
   *  $\mathbf{0}$ (read 'zero'), the __additive [[falsity]]__;
   *  $\mathbf{1}$ (read 'one'), the __multiplicative truth__;
   *  $\bot$ (read 'bottom'), the __multiplicative falsity__.
*  For each proposition $A$, there are two additional propositions:
   *  $!{A}$ (read '[[of course]]'), the __[[exponential conjunction]]__ of $A$;
   *  $?{A}$ (read 'why not'), the __exponential disjunction__ of $A$.

The terms "exponential", "multiplicative", and "additive" come from the fact that "exponentiation converts addition to multiplication": we have $!{(A \& B)}\equiv !{A} \otimes !{B}$ and so on (see below).

However, the connectives and constants can also be grouped in different ways.  For instance, the multiplicative conjunction $\otimes$ and additive disjunction $\oplus$ are both [[positive types]], while the additive conjunction $\&$ and multiplicative disjunction $\parr$ are [[negative types]].  Similarly, the multiplicative truth $\mathbf{1}$ and the additive falsity $\mathbf{0}$ are positive, while the additive truth $\top$ and multiplicative falsity $\bot$ are negative.  This grouping has the advantage that the similarity of symbols matches the adjective used.

But conversely, the natural grouping by multiplicative/additive, or equivalently by de Morgan dual pairs, has led many authors to alter Girard's notation, in particular reverting to the category-theoretic $\times$ and $+$ for the additives $\&$ and $\oplus$, and introducing a different symbol such as $\odot$, $\bullet$ or (confusingly) $\oplus$ for Girard's $\parr$.  But on this page we will stick to Girard's conventions for consistency.

In [[relevant logic]], the terms "conjunction" and "disjunction" are often reserved for the additive versions $\&$ and $\oplus$, which are written with the traditional notations $\wedge$ and $\vee$.  In this case, the multiplicative conjunction $A\otimes B$ is called **fusion** and denoted $A\circ B$, while the multiplicative disjunction $A\parr B$ is called **fission** and denoted $A+B$ (or sometimes, confusingly, $A\oplus B$).  In relevant logic the symbol $\bot$ may also be used for the *additive* falsity, here denoted $\mathbf{0}$.  Also, sometimes the additive connectives are called **extensional** and the multiplicatives **intensional**.

Sometimes one does not define the operation of negation, defining only $p^\perp$ for a propositional variable $p$.  It is a theorem that every proposition above is equivalent (in the sense defined below) to a proposition in which negation is applied only to propositional variables.

We now define the valid sequents, where we write $A, B, C \vdash D, E, F$ to state the validity of the sequent consisting of the list $(A,B,C)$ and the list $(D,E,F)$ and use Greek letters for sublists:

*  The [[structural rule]]s:
   *  The [[exchange rule]]:  If a sequent is valid, then any [[permutation]] of it (created by permuting its left and right sides independently) is valid.
   *  The restricted [[weakening rule]]:  If $\Gamma, \Delta \vdash \Theta$, then $\Gamma, !{A}, \Delta \vdash \Theta$, for any $A$; conversely and dually, if $\Gamma \vdash \Delta, \Theta$, then $\Gamma \vdash \Delta, ?{A}, \Theta$ for any $A$.
   *  The restricted [[contraction rule]]:  If $\Gamma, !{A}, !{A}, \Delta \vdash \Theta$, then $\Gamma, !{A}, \Delta \vdash \Theta$; conversely and dually, if $\Gamma \vdash \Delta, ?{A}, ?{A}, \Theta$, then $\Gamma \vdash \Delta, ?{A}, \Theta$.
   *  The [[identity rule]]:  Always, $A \vdash A$;
   *  The [[cut rule]]:  If $\Gamma \vdash A, \Phi$ and $\Psi,A \vdash \Delta$, then $\Psi,\Gamma \vdash \Delta,\Phi$.
*  The logical rules for each operation:
   *  If $\Gamma \vdash A, \Delta$, then $\Gamma, A^\perp \vdash \Delta$; conversely and dually, if $\Gamma, A \vdash \Delta$, then $\Gamma \vdash A^\perp, \Delta$.
   *  If $\Gamma, A, \Delta \vdash \Theta$ or $\Gamma, B, \Delta \vdash \Theta$, then $\Gamma, A \& B, \Delta \vdash \Theta$; conversely, if $\Gamma \vdash \Delta, A, \Theta$ and $\Gamma \vdash \Delta, B, \Theta$, then $\Gamma \vdash \Delta, A \& B, \Theta$.
   *  Dually, if $\Gamma \vdash \Delta, A, \Theta$ or $\Gamma \vdash \Delta, B, \Theta$, then $\Gamma \vdash \Delta, A \oplus B, \Theta$; conversely, if $\Gamma, A, \Delta \vdash \Theta$ and $\Gamma, B, \Delta \vdash \Theta$, then $\Gamma, A \oplus B, \Delta \vdash \Theta$.
   *  If $\Gamma, A, B, \Delta \vdash \Theta$, then $\Gamma, A \otimes B, \Delta \vdash \Theta$; conversely, if $\Gamma \vdash \Delta, A$ and $\Lambda \vdash B, \Theta$, then $\Gamma, \Lambda \vdash \Delta, A \otimes B, \Theta$.
   *  Dually, if $\Gamma \vdash \Delta, A, B, \Theta$, then $\Gamma \vdash \Delta, A \parr B, \Theta$; conversely, if $\Gamma, A \vdash \Delta$ and $B, \Theta \vdash \Lambda$, then $\Gamma, A \parr B, \Theta \vdash \Delta, \Lambda$.
   *  Always $\Gamma \vdash \Delta, \top, \Theta$; dually (there is no converse), $\Gamma, \mathbf{0}, \Delta \vdash \Theta$.
   *  If $\Gamma, \Delta \vdash \Theta$, then $\Gamma, \mathbf{1}, \Delta \vdash \Theta$; conversely, $\vdash \mathbf{1}$.
   *  Dually, if $\Gamma \vdash \Delta, \Theta$, then $\Gamma \vdash \Delta, \bot, \Theta$; conversely, $\bot \vdash$.
   *  If $\Gamma, A, \Delta \vdash \Theta$, then $\Gamma, !{A}, \Delta \vdash \Theta$; conversely, if $\Gamma \vdash \Delta, A, \Theta$, then $\Gamma \vdash \Delta, !{A}, \Theta$, whenever $\Gamma$ consists entirely of propositions of the form $!{-}$ while $\Delta$ and $\Theta$ consist entirely of propositions of the form $?{-}$.
   *  Dually, if $\Gamma \vdash \Delta, A, \Theta$, then $\Gamma \vdash \Delta, ?{A}, \Theta$; conversely, if $\Gamma, A, \Delta \vdash \Theta$, then $\Gamma, ?{A}, \Delta \vdash \Theta$, whenever $\Gamma$ and $\Delta$ consist entirely of propositions of the form $!{-}$ while $\Theta$ consists entirely of propositions of the form $?{-}$.

The main point of linear logic is the restricted use of the weakening and contraction rules; if these were universally valid (applying to any $A$ rather than only to $!{A}$ or $?{A}$), then the additive and multiplicative operations would be equivalent (in the sense defined below) and similarly $!{A}$ and $?{A}$ would be equivalent to $A$, which would give us [[classical logic]].  On the other hand, one can also remove the exchange rule to get a variety of [[noncommutative logic]]; one must then be careful about how to write the other rules (which we have been above).

As usual, there is a theorem of [[cut elimination]] showing that the cut rule and identity rule follow from all other rules and the special cases of the identity rule of the form $p \vdash p$ for a propositional variable $p$.

The propositions $A$ and $B$ are (propositionally) __equivalent__ if $A \vdash B$ and $B \vdash A$ are both valid, which we express by writing $A \equiv B$.  It is then a theorem that either may be swapped for the other anywhere in a sequent without affecting its validity.  Up to equivalence, negation is an [[involution]], and the operations $\&$, $\oplus$, $\otimes$, and $\parr$ are all [[associative]], with respective [[identity elements]] $\top$, $\mathbf{0}$, $\mathbf{1}$, and $\bot$.  These operations are also [[commutative operation|commutative]] (although this fails for the multiplicative connectives if we drop the exchange rule).  The additive connectives are also [[idempotent]] (but the multiplicative ones are not). 

+-- {: .num_remark} 
###### Remark 
There is a more refined notion of equivalence, where we pay attention to specific derivations $\pi: A \vdash B$ of sequents, and deem two derivations $\pi, \pi'$ of $A \vdash B$ _Lambek-equivalent_ if they map to the same morphism under any categorical semantics $S$; see below. Given a pair of derivations $\pi: A \vdash B$ and $\rho: B \vdash A$, it then makes sense to ask whether they are Lambek-inverse to one another (i.e., whether $S(\rho) = S(\pi)^{-1}$ under any semantics), so that the derivations exhibit an isomorphism $S(A) \cong S(B)$ under any semantics $S$. This equivalence relation $A \equiv_{Lambek} B$ is strictly stronger than propositional equivalence. It should be observed that all equivalences $A \equiv B$ listed below are in fact Lambek equivalences. 
=-- 

We also have [[distributive law|distributive laws]] that explain the adjectives 'additive', 'multiplicative', and 'exponential':

*  Multiplication distributes over addition if one is a conjunction and one is a disjunction:
   *  $A \otimes (B \oplus C) \equiv (A \otimes B) \oplus (A \otimes C)$ (and on the other side);
   *  $A \parr (B \& C) \equiv (A \parr B) \& (A \parr C)$ (and on the other side);
   *  $A \otimes \mathbf{0} \equiv \mathbf{0}$ (and on the other side);
   *  $A \parr \top \equiv \top$ (and on the other side).
*  Exponentiation converts addition into multiplication if all are conjunctions or all are disjunctions:
   *  $!{(A \& B)} \equiv !{A} \otimes !{B}$;
   *  $?{(A \oplus B)} \equiv ?{A} \parr ?{B}$;
   *  $!{\top} \equiv \mathbf{1}$;
   *  $?{\mathbf{0}} \equiv \bot$.

It is also a theorem that negation (except for the negations of propositional variables) can be defined (up to equivalence) recursively as follows:

*  $(A^\perp)^\perp \equiv A$;
*  $(A \& B)^\perp \equiv A^\perp \oplus B^\perp$ and vice versa;
*  $(A \otimes B)^\perp \equiv A^\perp \parr B^\perp$ and vice versa;
*  $\top^\perp \equiv \mathbf{0}$ and vice versa;
*  $\mathbf{1}^\perp \equiv \bot$ and vice versa;
*  $(!{A})^\perp \equiv ?{A^\perp}$ and vice versa.

The logical rules for [[negation]] can then be proved.

In this way, linear logic in the original sense (interpreted in [[star-autonomous categories]])  has a perfect [[de Morgan duality]]. But observe that more general variants (interpreted in more general [[symmetric monoidal categories]]) need not, see for instance ([Hyland--de Paiva 93](#HylandPaiva93)).  

We can also restrict attention to sequents with one term on either side as follows:  $\Gamma \vdash \Delta$ is valid if and only if $\bigotimes \Gamma \vdash \parr \Delta$ is valid, where $\bigotimes(A, B, C) \coloneqq A \otimes B \otimes C$, etc, and similarly for $\parr$ (using implicitly that these are associative, with identity elements to handle the [[empty sequence]]).

We can even restrict attention to sequents with no term on the left side and one term on the right; $A \vdash B$ is valid if and only if $\vdash A \multimap B$ is valid, where $A \multimap B \coloneqq A^\perp \parr B$.  In this way, it\'s possible to ignore sequents entirely and speak only of propositions and valid propositions, eliminating half of the logical rules in the process.  However, this approach is not as beautifully symmetric as the full sequent calculus.


## Variants

The logic described above is full classical linear logic.  There are many important [[fragments]] and variants of linear logic, such as:

* [[multiplicative linear logic]] (MLL), which contains only $\otimes,\parr$ and their units $\mathbf{1},\bot$ as well as the negation $(-)^\perp$.

* multiplicative-exponential linear logic (MELL), which contains only $\otimes,\parr,\mathbf{1},\bot,(-)^\perp$ and the exponential modalities $!,?$.

* multiplicative-additive linear logic (MALL), which contains everything *except* the exponential modalities $!,?$.

* multiplicative intuitionistic linear logic (MILL), which contains only $\otimes,\mathbf{1},\multimap$ (the latter now as a primitive operation); in particular there is no longer the involutive negation $(-)^\perp$.  The sequents are also restricted to have only one formula on the right.

* intuitionistic linear logic (ILL), which contains all the additive connectives $\&,\oplus,\mathbf{0},\top$ as well as the intutionistic multiplicatives $\otimes,\mathbf{1},\multimap$ and the exponential $!$, with one formula on the right as above.  In this case all connectives are all independent of each other.

* full intuitionistic linear logic (FILL), which in addition to ILL contains the multiplicative disjunction $\parr$, and perhaps the exponential $?$.  (Sometimes ILL without $\parr,?$ is also called "full" intuitionistic linear logic.)

* non-commutative linear logics (braided or not)

* "light" and "soft" linear logics, which limit the use of ! to constrain the computational complexity of proofs

* first-order linear logic, which adds quantifiers $\exists$ and $\forall$ (sometimes denoted $\bigvee$ and $\bigwedge$), either over a fixed domain or over varying types.  These quantifiers are usually considered "additive"; for a theory that has a certain kind of "multiplicative quantifier" see [[bunched implication]].

One can also consider adding additional rules to linear logic.  For instance, by adding the [[weakening rule]] (but not the [[contraction rule]]) one obtains [[affine logic]], whereas by adding contraction but not weakening one obtains [[relevance logic]].  Another rule that is sometimes considered is the [[mix rule]].

[[linear-non-linear logic |Linear-non-linear logic]] is an equivalent presentation of intuitionistic linear logic that decomposes the $!$ modality into an adjunction between a cartesian logic and a linear one in which cartesian variables can also appear.

Some models of linear logic allow for a _codereliction_ operation, which allows for one to take the "linear approximation" of a proof $!(A) \to B$. These models lead to the development of _differential linear logic_, the categorical semantics of which was laid out in ([Blute--Cockett--Seely](#Blute-Cockett-Seely06)).

## Categorical semantics

We discuss the [[categorical semantics]] of linear logic. See also at _[[relation between type theory and category theory]]_.

### $*$-autonomous categories

One way to explain linear logic to a category theorist is to say that its models are [[*-autonomous categories]] with extra structure ([Seely, 1989, prop. 1.5](#Seely)). (If the underlying category is a [[suplattice]] then these are commutative [[quantales]], ([Yetter 90](#Yetter90)))

Firstly, there is a monoidal '[[tensor product|tensor]]' connective
$A \otimes B$.  [[negation|Negation]] $A^\bot$ is modelled by the [[dual object]]
involution $(-)^*$, while [[linear implication]] $A\multimap B$
corresponds to the [[internal hom]], which can be defined as
$(A\otimes B^\bot)^\bot$.  There is a [[de Morgan dual]] of the
tensor called 'par', with $A \parr B = (A^\bot\otimes B^\bot)^\bot$.  Tensor and par are the
'multiplicative' connectives, which roughly speaking represent the
parallel availability of resources. 

The 'additive' connectives $\&$ and $\oplus$, which
correspond in another way to traditional [[conjunction]] and
[[disjunction]], are modelled as usual by [[products]] and
[[coproducts]].  [Seely (1989)](#Seely) notes that products are sufficient, as $*$-autonomy then guarantees the existence of coproducts; that is, they are also linked by [[de Morgan duality]].

Recall also that linear logic recaptures the notion of a resource that can be discarded
or copied arbitrarily by the use of the [[modal logic|modal]] operator $!$ the [[exponential modality]]:
$!A$ denotes an '$A$-factory', a resource that can produce
zero or more $A$s on demand.  It is modelled using a suitably monoidal [[comonad]]
$!$ on the underlying $*$-autonomous category.  There are various inequivalent ways to make this precise, however; see [!-modality](https://ncatlab.org/nlab/show/!-modality) for discussion.

An LL sequent
$$A_1,\ldots,A_n \vdash B_1,\ldots,B_m$$
is interpreted as a morphism
$$ \otimes_i A_i \to \parr_j B_j $$
The comonoid structure on $!A$ then yields the weakening
$$ \Gamma\otimes !A \to \Gamma \otimes I \to \Gamma$$
and contraction
$$ \Gamma\otimes !A \to \Gamma \otimes !A \otimes !A $$
maps.  The corresponding rules are interpreted by
precomposing the interpretation of a sequent with one of
these maps.

The (co)-[[Kleisli category]] of $!$ is [[cartesian closed category|cartesian closed]], and
the product there coincides with the product in the base
category.  The [[exponential object|exponential]] (unsurprisingly for a Kleisli
category) is $B^A \cong !A\multimap B$.

Particular monoidal and $*$-autonomous [[posets]] for modeling linear logic can be obtained by [[Day convolution]] from [[ternary frames]].  This includes Girard's *phase spaces* as a particular example.

First-order linear logic is correspondingly modeled in a [[linear hyperdoctrine]].


### Polycategories

A different way to explain linear logic categorically (though equivalent, in the end) is to start with a categorical structure which lacks any of the connectives, but has sufficient structure to enable us to characterize them with universal properties.  If we ignore the exponentials for now, such a structure is given by a [[polycategory]].  The polymorphisms

$$(A,B,C) \to (D,E,F)$$

in a polycategory correspond to sequents $A,B,C \vdash D,E,F$ in linear logic.  The multiplicative connectives are then characterized by representability and corepresentability properties:

$$\frac{(A,B) \to C}{A\otimes B \to C}$$

and

$$\frac{A \to (B,C)}{A \to B\parr C}$$

(Actually, we should allow arbitrarily many unrelated objects to carry through in both cases.)  The additives are similarly characterized as categorical products and coproducts, in a polycategorically suitable sense.

Finally, dual objects can be recovered as a sort of "adjoint":

$$\frac{(A,B) \to C}{A \to (B^*,C)}$$

If all these representing objects exist, then we recover a $*$-autonomous category.

One merit of the polycategory approach is that it makes the role of the structural rules clearer, and also helps explain why $\parr$ sometimes seems like a disjunction and sometimes like a conjunction.  Allowing contraction and weakening on the left corresponds to our polycategory being "left [[cartesian multicategory|cartesian]]"; that is, we have "diagonal" and "projection" operations such as $Hom(A,A; B) \to Hom(A;B)$ and $Hom(;B) \to Hom(A,B)$.  In the presence of these operations, a representing object is automatically a cartesian product; thus $\otimes$ coincides with $\&$.  Similarly, allowing contraction and weakening on the right makes the polycategory "right cocartesian", which causes corepresenting objects to be coproducts and thus $\parr$ to coincide with $\oplus$.

On the other hand, if we allow "multi-composition" in our polycategory, i.e. we can compose a morphism $A \to (B,C)$ with one $(B,C)\to D$ to obtain a morphism $A\to D$, then our polycategory becomes a [[PROP]], and representing and corepresenting objects must coincide; thus $\otimes$ and $\parr$ become the same.  This explains why $\parr$ has both a disjunctive and a conjunctive aspect.  Of course, if in addition to multi-composition we have the left and right cartesian properties, then all four connectives coincide (including the categorical product and coproduct) and we have an [[additive category]].


## Game semantics

We can interpret any proposition in linear logic as a game between two players: we and they. The overall rules are perfectly symmetric between us and them, although no individual game is. At any given moment in a game, exactly one of these four situations obtains: it is our turn, it is their turn, we have won, or they have won; the last two states continue forever afterwards (and the game is over).  If it is our turn (or if they have won), then they are winning; if it is their turn (or if we have won), then we are winning.  So there are two ways to win: because the game is over (and a winner has been decided), or because it is forever the other players' turn (either because the other players have no move or because every move results in the other players' turn again).

This is a little complicated, but it\'s important in order to be able to distinguish the four constants:

*  In $\top$, it is their turn, but they have no moves; the game never ends, but we win.
*  Dually, in $\mathbf{0}$, it is our turn, but we have no moves; the game never ends, but they win.
*  In contrast, in $\mathbf{1}$, the game ends immediately, and we have won.
*  Dually, in $\bot$, the game ends immediately, and they have won.

The binary operators show how to combine two games into a larger game:

*  In $A \& B$, it is their turn, and they must choose to play either $A$ or $B$.  Once they make their choice, play continues in the chosen game, with ending and winning conditions as in that game.
*  Dually, in $A \oplus B$, it is our turn, and we must choose to play either $A$ or $B$.  Once we make our choice, play continues in the chosen game, with ending and winning conditions as in that game.
*  In $A \otimes B$, play continues with both games in parallel.  If it is our turn in either game, then it is our turn overall; if it is their turn in both games, then it is their turn overall.  If either game ends, then play continues in the other game; if both games end, then the overall game ends.  If we have won both games, then we have won overall; if they have won either game, then they have won overall.
*  Dually, in $A \parr B$, play continues with both games in parallel.  If it is their turn in either game, then it is their turn overall; if it is our turn in both games, then it is our turn overall.  If either game ends, then play continues in the other game; if both games end, then the overall game ends.  If they have won both games, then they have won overall; if we have won either game, then we have won overall.

So we can classify things as follows:

*  In a conjunction, they choose what game to play; in a disjunction, we have control.  Whoever has control must win at least one game to win overall.
*  In an addition, one game must be played; in a multiplication, all games must be played.

To further clarify the difference between $\top$ and $\mathbf{1}$ (the additive and multiplicative versions of truth, both of which we win); consider $A \parr \top$ and $A \parr \mathbf{1}$.  In $A \parr \top$, it is always their move (since it is their move in $\top$, hence their move in at least one game), so we win just as we win $\top$.  (In fact, $A \parr \top \equiv \top$.)  However, in $A \parr \mathbf{1}$, the game $\mathbf{1}$ ends immediately, so play continues as in $A$.  We have won $\mathbf{1}$, so we only have to end the game to win overall, but there is no guarantee that this will happen.  Indeed, in $\mathbf{0} \parr \mathbf{1}$, the game never ends and it is always our turn, so they win.  (In $\bot \parr \mathbf{1}$, both games end immediately, and we win.  In $A \otimes \mathbf{1}$, we must win both games to win overall, so this reduces to $A$; indeed, $A \otimes \mathbf{1} \equiv A$.)

Negation is easy:

*  To play $A^\perp$, simply swap roles and play $A$.

There are several ways to think of the exponentials.  As before, they have control in a conjunction, while we have control in a disjunction.  Whoever has control of $!{A}$ or $?{A}$ chooses how many copies of $A$ to play and must win them all to win overall.  There are many variations on whether the player in control can spawn new copies of $A$ or close old copies of $A$ prematurely, and whether the other player can play different moves in different copies (whenever the player in control plays the same moves).

Other than the decisions made by the player in control of a game, all moves are made by transmitting resources.  Ultimately, these come down to the propositional variables; in the game $p$, we must transmit a $p$ to them, while they must transmit a $p$ to us in $p^\perp$.

A game is __valid__ if we have a strategy to win (whether by putting the game in a state where we have won or by guaranteeing that it is forever their turn).  The soundness and completeness of this interpretation is the theorem that $A$ is a valid game if and only if $\vdash A$ is a valid sequent.  (Recall that all questions of validity of sequents can be reduced to the validity of single propositions.)

Game semantics for linear logic was first proposed by [[Andreas Blass]], in [Blass (1992)](#Blass1992).  The semantics here is essentially the same as that proposed by Blass.


## Multiple exponential operators

Much as there are many [[exponential functions]] (say from $\mathbb{R}$ to $\mathbb{R}$), even though there is only one addition operation and one multiplication operation, so there can be many versions of the exponential operators $!$ and $?$.  (However, there doesn\'t seem to be any analogue of the [[logarithm]] to convert between them.)

More precisely, if we add to the language of linear logic two more operators, $!'$ and $?'$, and postulate of them the same rules as for $!$ and $?$, we cannot prove that $!{A} \equiv !'{A}$ and $?{A} \equiv ?'{A}$.  In contrast, if we introduce $\&'$, $\bot'$, etc, we *can* prove that the new operators are equivalent to the old ones.

In terms of the categorial interpretation above, there may be many comonads $!$; it is not determined by the underlying $*$-autonomous category.  In terms of game/resource semantics, there are several slightly different interpretations of the exponentials.

One sometimes thinks of the exponentials as coming from infinitary applications of the other operations.  For example:

*  $!{A} \coloneqq 1 \& A \& (A \otimes A) \& (A \otimes A \otimes A) \& \cdots$,
*  $!{A} \coloneqq (1 \& A) \otimes (1 \& A) \otimes (1 \& A) \otimes \cdots$,
*  $!{A} \coloneqq 1 \& k A \& (k^2/2) (A \otimes A) \& (k^3/6) (A \otimes A \otimes A) \& \cdots$ (which is $\mathrm{e}^{k A}$ in an appropriate sense), where $n A$ means an $n$-fold additive conjunction $A \& \cdots \& A$ for $n$ a [[natural number]], and we pretend that $k$ is a positive number such that $k^n/{n!}$ is always a natural number (which of course is impossible).

All of these justify the rules for the exponentials, so again we see that there may be many ways to satisfy these rules.


## Interpretation in constructive mathematics {#antithesis}

[[Mike Shulman]] ([Shulman 2018](#Shulman2018)) has proposed an interpretation of linear logic for use in [[constructive mathematics]], called the _antithesis interpretation_.

The motivation here is that in much of constructive mathematics, especially (but not only) in [[constructive analysis]], statements of interest seem to come in pairs, a statement $P^+$ that amounts to a constructive version of a well-known statement $P^{\mathrm{C}}$ from [[classical mathematics]], and a statement $P^-$ that amounts to a constructive version of $\neg{P^{\mathrm{C}}}$, and which is equivalent to $\neg{P^+}$ in [[classical logic]], but which is not the same as $\neg{P^+}$ in [[intuitionistic logic]] (being sometimes stronger, sometimes weaker, sometimes neither, and similarly for $P^+$ vis-a-vis $\neg{P^-}$).  For example, if $P^{\mathrm{C}}$ is the claim that some [[real number]] $x$ is [[rational number|rational]], then $P^+$ is

$$ \exists\, q \in \mathbb{Q},\; x = q $$

(the conventional meaning of &lsquo;$x$ is rational&rsquo; in constructive analysis), while $P^-$ is

$$ \forall\, q \in \mathbb{Q},\; x \# q $$

(the conventional meaning of &lsquo;$x$ is [[irrational number|irrational]]&rsquo; in constructive analysis); here, $\#$ is the standard [[apartness relation]] between real numbers, whose [[negation]] is the [[equality relation]] $=$.  As you can see, the two statements are [[de Morgan duality|de Morgan dual]] to one another, and so are negations of each other in classical logic, but neither is the negation of the other in intuitionistic logic.

That such pairs of statements commonly arise is a truism in constructive mathematics.  The point of the antithesis interpretation is that the pair $(P^+, P^-)$ may be derived systematically from a single statement $P^{\mathrm{L}}$ in linear logic.  And this is a [[sound interpretation]], in that any reasoning valid in linear logic (or even [[affine logic]]) will be constructively valid for both statements; that is, if $P^{\mathrm{L}} \vdash Q^{\mathrm{L}}$ in linear (or even affine) logic, then $P^+ \vdash Q^+$ and $Q^- \vdash P^-$ in intuitionistic logic.  Therefore, as long as the reasoning is linear (or at least affine), one can prove intuitionistic theorems about both at once.

The antithesis interpretation also explains why there are often both weak and strong versions of $P^-$ (or even $P^+$ sometimes), having especially to do with the interpretation of [[disjunction]].  This comes up already in defining what a [[set]] is, because of the nature of the [[equality relation]] on a set $S$.  As in the example about about rational and irrational real numbers, every set should also be equipped with an antithesis [[inequality relation]] $\#$, and the axioms for this may be derived from the axioms for an equality relation.  The [[transitive relation|transitivity]] axiom for equality has two obvious interpretations in linear logic, which lead to two different interpretations in intuitionistic logic as axioms for $\#$: a weak version (intepreting $\parr$) stating (for elements $x, y, z$ of $S$) that if $x \# z$, then $y \# z$ if $x = y$, and $x \# y$ if $y = z$; and a strong version (interpreting $\oplus$) stating that if $x \# z$, then $x \# y$ or $y \# z$.  (The weak version really does follow from the strong version because we also automatically have that $x = y$ and $x \# y$ can never both be true.)  Ultimately, the weak version says only that $\#$ is an [[inequality relation]] on the set $S$, while the strong version says that $\#$ is an [[apartness relation]].

Since every proposition comes with an antithesis proposition in the antithesis interpretation, the natural notion of a [[subset]] is actually a pair of [[disjoint subsets]], leading to a potentially far-reaching reinterpretation of the role of [[higher-order logic]] in constructive mathematics, with concepts like a family of collections of subsets becoming a disjoint pair of families of disjoint pairs of collections of disjoint subsets.


## Related concepts

* [[bounded linear logic]]

* [[game semantics]]

* [[linear type theory]]

* [[light logic]]

  * [[light linear logic]]
  * [[soft linear logic]]

* [[proof net]]

* [[linearly distributive category]]

* [[transcendental syntax]]

* [[propositions as projections]]

* [[substructural logic]]
  * [[structural rule]]
  * [[affine logic]]
  * [[relevance logic]]
  * [[bunched logic]]
  * [[separation logic]]


## References

The original article is

*  [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science 50:1, 1987.  ([pdf](http://iml.univ-mrs.fr/~girard/linear.pdf))
 {#Girard}

Reviews include

* [[Jean-Yves Girard]], _Linear logic, its syntax and semantics_ ([pdf](http://www.cs.brandeis.edu/~cs112/2006-cs112/docs/girard-intro.pdf))

* {#Girard11} [[Jean-Yves Girard]], part III of _[[Lectures on Logic]]_, European Mathematical Society 2011
 

* {#Murfet14} [[Daniel Murfet]], _Logic and linear algebra: an introduction_ ([arXiv:1407.2650](http://arxiv.org/abs/1407.2650))

The [[categorical semantics]] of linear logic in [[star-autonomous categories]] originally appeared in

*  [[R. A. G. Seely]],  _Linear logic, $\ast$-autonomous categories and cofree coalgebras_, _Contemporary Mathematics_ 92, 1989.  ([[SeelyLinearLogic.pdf:file]], [ps.gz](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz))
 {#Seely}

and for the special case of [[quantales]] in 

* [[David Yetter]], _Quantales and (noncommutative) linear logic_, Journal of Symbolic Logic 55 (1990), 41--64.
 {#Yetter90}

The more general case of of multiplicative intuitionistic linear logic interpreted more generally in [[symmetric monoidal categories]] was systematically developed in

* M.E. Szabo, _Algebra of Proofs_, Studies in Logic and the Foundations of Mathematics, vol. 88 (1978), North-Holland. 
 {#Szabo78}

(that was before Girard introduced the "linear" terminology).

More recent articles exploring this include

* [[Valeria de Paiva]], _The Dialectica Categories_, _Contemporary Mathematics_ 92, 1989. ([web] (http://www.cs.bham.ac.uk/~vdp/publications/dial87.pdf)) 
 {#dePaiva89}

* [[Richard Blute]], _Linear logic, coherence, and dinaturality_, Dissertation, University of Pennsylvania 1991, published in Theoretical Computer Science archive
Volume 115 Issue 1, July 5, 1993  Pages 3--41 
 {#Blute91}

* Nick Benton, Gavin Bierman, [[Valeria de Paiva]], [[Martin Hyland]], _Term assignments for intuitionistic linear logic_. Technical report 262, Cambridge 1992 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.31.8666), [ps](http://www.cs.bham.ac.uk/~vdp/publications/tr262.ps))
 {#BentonBiermanPaivaHyland92}

* [[Martin Hyland]], [[Valeria de Paiva]], _Full Intuitionistic Linear Logic_ (extended abstract). Annals of Pure and Applied Logic, 64(3), pp. 273--291, 1993. ([pdf](http://www.cs.bham.ac.uk/~vdp/publications/fill.pdf))
 {#HylandPaiva93}

* G. Bierman, _On Intuitionistic Linear Logic_ PhD thesis, Computing
Laboratory, University of Cambridge, 1995 ([pdf](http://research.microsoft.com/~gmb/papers/thesis.pdf))
 {#Bierman95}


* {#Barber97} Andrew Graham Barber, _Linear Type Theories, Semantics and Action Calculi_, PhD thesis, Edinburgh 1997 ([web](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/&#8206;), [pdf](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/ECS-LFCS-97-371.pdf))



This is reviewed/further discussed in

* Andrea Schalk, _What is a categorical model for linear logic?_ ([pdf](http://www.cs.man.ac.uk/~schalk/notes/llmodel.pdf))
 {#Schalk04}

* [[Richard Blute]], Philip Scott, _Category theory for linear logicians_, 2004 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.83.6250))

* [[Paul-André Melliès]] , _Categorial Semantics of Linear Logic_, in _Interactive models of computation and program behaviour_, Panoramas et synth&#232;ses 27, 2009 ([pdf](http://www.pps.univ-paris-diderot.fr/~mellies/papers/panorama.pdf))
 {#Mellies09}

The relation of dual intuitionistic linear logic and $\pi$-calculus is given in

* Luis Caires, Frank Pfenning. _Session Types as Intuitionistic Linear Propositions_.

Noncommutative linear logic is discussed for instance in

* [[Richard Blute]], F. Lamarche, Paul Ruet, _Entropic Hopf algebras and models of non-commutative logic_, Theory and Applications of Categories, Vol. 10, No. 17, 2002, pp. 424&#8211;460. ([pdf](http://www.emis.ams.org/journals/TAC/volumes/10/17/10-17.pdf))


Further discussion of [[linear type theory]] is for instance in

* _Chapter 7, Linear type theory_ [pdf](http://www.cs.cmu.edu/~fp/courses/linear/handouts/lintt.pdf)


* Anders Schack-Nielsen, Carsten Sch&#252;rmann, _Linear contextual modal type theory_ [pdf](http://www.itu.dk/~carsten/papers/lcmtt.pdf)


See also

* [[Andreas Blass]], 1992. _A game semantics for linear logic_. _Annals of Pure and Applied Logic_ 56: 183--220. 1992.
  {#Blass1992}

*  The [article](https://secure.wikimedia.org/wikipedia/en/wiki/Linear_logic) on the English Wikipedia has good summaries of the meanings of the logical operators and of the commonly studied [[fragments]].

Discussion of application of linear logic to [[quantum logic]], [[quantum computing]] and generally to [[quantum physics]] includes

* [[Vaughan Pratt]], _Linear logic for generalized quantum mechanics_, in Proc. of _Workshop on Physics and Computation (PhysComp'92)_ ([pdf](http://boole.stanford.edu/pub/ql.pdf), [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.137.7817))

* [[Ross Duncan]], _Types for quantum computation_, 2006 ([pdf](http://www.cs.ox.ac.uk/files/2425/Types%20for%20Quantum%20Computation.pdf))

* {#CCGP09} Gianpiero Cattaneo, Maria Luisa Dalla Chiara, Roberto
Giuntini and Francesco Paoli, section 9 of _Quantum Logic and Nonclassical Logics_, p. 127 in  Kurt Engesser, Dov M. Gabbay, Daniel Lehmann (eds.) _Handbook of Quantum Logic and Quantum Structures: Quantum Logic_, 2009 North Holland
  
* [[Ugo Dal Lago]], [[Claudia Faggian]], _On Multiplicative Linear Logic, Modality and Quantum Circuits_ ([arXiv:1210.0613](http://arxiv.org/abs/1210.0613))

See also at *[[quantum programming languages]]*

Discussion for [[matrix factorization]] in [[Landau–Ginzburg models]] is in

* {#Murfet14} [[Daniel Murfet]], _Computing with cut systems_ ([arXiv:1402.4541](http://arxiv.org/abs/1402.4541))


Discussion of [[linear type theory]] without [[units]] is in 

* [[Robin Houston]], _Linear Logic without Units_ ([arXiv:1305.2231](http://arxiv.org/abs/1305.2231))


Discussion of [[inductive types]] in the context of [[linear type theory]] is in 

* St&#233;phane Gimenez, _Towards Generic Inductive Constructions in
Systems of Nets_ ([pdf](http://www.imn.htwk-leipzig.de/WST2013/papers/paper_16.pdf))


The categorical semantics of differential linear logic is introduced in:

* [[Richard Blute]], [[Robin Cockett]], [[Robert Seely]], _Differential Categories_, Mathematical structures in computer science 16.6 (2006): 1049--1083. ([pdf](https://pdfs.semanticscholar.org/82b0/f9533b451d174f407b35e1c39e2376138ac2.pdf)) 
{#Blute-Cockett-Seely06}


The antithesis interpretation is

* [[Michael Shulman]], 2018. _Linear logic for constructive mathematics_. [arXiv:1805.07518](https://arxiv.org/abs/1805.07518).
{#Shulman2018}

(This is a prepublication version that does not yet include the name 'antithesis interpretation', which was suggested by a referee.  We must link to the published version when available.)



[[!redirects linear logic]]
[[!redirects linear logics]]

[[!redirects classical linear logic]]
[[!redirects classical linear logics]]
[[!redirects CLL]]
[[!redirects intuitionistic linear logic]]
[[!redirects ILL]]
[[!redirects multiplicative intuitionistic linear logic]]
[[!redirects MILL]]
[[!redirects multiplicative linear logic]]
[[!redirects MLL]]
[[!redirects multiplicative-additive linear logic]]
[[!redirects MALL]]

[[!redirects antithesis interpretation]]