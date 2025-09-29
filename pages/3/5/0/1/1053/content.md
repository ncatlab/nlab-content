

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
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

**Linear logic** is a [[substructural logic]] in which the [[contraction rule]] and the [[weakening rule]] are omitted, or at least have their applicability restricted.  

### Absence of weakening and contraction
 {#AbsenceOfWeakeningAndContraction}

Notice that [[contraction rule|contraction]] and [[weakening rule|weakening]] are the two [[structural rule|structural]] [[inference rules]] which exhibit [[context extensions]] $\Gamma \,\mapsto\, \Gamma, P$ as admitting [[natural transformation|natural]] [[diagonal map|diagonal]] and [[projection]] [[maps]], respectively, hence as admitting [[categorical semantics|interpretation]] as *[[cartesian products]]* $\Gamma \times P$ (cf. [Jacobs 1994](structural+rule#Jacobs94)):


\begin{imagefromfile}
    "file_name": "WeakeningContractionRules-230330d.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


Therefore, when these [[inference rules]] are dropped then the resulting [[multiplicative conjunction]] $\otimes$ of contexts may still have [[categorical semantics|interpretation]] as a [[symmetric monoidal category|symmetric monoidal]] [[tensor product]] (such as known from the [[tensor product of vector spaces]]) but not necessarily as a [[cartesian monoidal category|cartesian monoidal]] [[product]] (such as known from the [[topological product space|product of topological spaces]]).

Accordingly, if [[implication]] still follows the usual [[inference rule]] of [[function types]] but now with respect to a non-cartesian [[multiplicative conjunction]] $\otimes$

$$
  \frac{
    \Gamma \otimes P 
      \;\;\vdash\;\; 
    t_p \,\colon\, T
  }
  {
    \Gamma 
      \;\;\vdash\;\; 
    (p \mapsto t_p) 
      \,\colon\, 
    P \multimap T
  }
$$

etc., then the [[function type]] $P \multimap T$ may be [[categorical semantics|interpreted]] as an [[internal hom]]
in a non-[[cartesian closed category|cartesian]] [[closed monoidal category]] with [[symmetric monoidal category|symmetric monoidal]] *[[tensor product]]* $\otimes$ --- such as the category  of [[finite-dimensional vector spaces]], in which case the [[terms]] $\Gamma \vdash f \colon P \multimap T$ [[categorical semantics|interpret]] as *[[linear functions]]* --- whence the [[logical connective]] "$\multimap$" is also called *[[linear implication]]*.

Which exact flavour of [[monoidal category]] provides [[categorical semantics]] for linear logic depends on exactly which further [[inference rules]] are considered (see also at *[[bunched logic]]*):
In the original definition of [Girard (1987)](#Girard1987), linear logic is the [[internal logic]] of/has [[categorical semantics]] in [[star-autonomous categories]] ([Seely 89, prop. 1.5](#Seely)). But more generally _linear logic_ came to refer to the [[internal logic]] of any possibly-non-[[cartesian monoidal category|cartesian]] [[symmetric monoidal category|symmetric]] [[closed monoidal category]] (then usually called _multiplicative intuitionistic linear logic_ -- _MILL_) or even [[polycategory]] ([Szabo 78](#Szabo78) see the [history section](linear%20type%20theory#HistoryCategoricalSemantics) and see also [de Paiva 89](#dePaiva89), [Blute 91](#Blute91), [Benton--Bierman--de Paiva--Hyland 92](#BentonBiermanPaivaHyland92), [Hyland--de Paiva 93](#HylandPaiva93), [Bierman 95](#Bierman95), [Barber 97](#Barber97), [Schalk 04](#Schalk04), [Melli&#232;s 09](#Mellies09)). Under this interpretation, _[[proof nets]]_ (or the associated [[Kelly–Mac Lane graphs]]) of linear logic are similar to [[string diagrams]] for monoidal categories.  

Indeed, these more general senses of linear logic still faithfully follow the original motivation for the term "linear" as connoting "resource availability" explained [below](#ResourceAvailability), since the non-cartesianness of the [[tensor product]] means the absence of a [[diagonal]] map and hence the impossibility of [[functions]] to depend on more than a single (linear) copy of their [[variables]].

In addition to these usual "[[denotational semantics|denotational]]" categorical semantics, linear logic also has an "[[operational semantics|operational]]" categorical semantics, called the _[[Geometry of Interaction]]_, in [[traced monoidal categories]].

Although linear logic is traditionally presented in terms of [[inference rules]], it was apparently discovered by Girard while studying [[coherence spaces]].



### As a quantum logic
 {#AsAQuantumLogic}

With the archetypical [[categorical semantics]] of linear logic in the [[compact closed category]] of [[finite dimensional vector spaces]] in mind, which is the habitat of [[quantum information theory]] (see [[quantum information theory via dagger-compact categories|there]] for more), one may naturally understand linear logic as a form of [[quantum logic]] &lbrack;[Pratt (1992)](#Pratt92)&rbrack; and in its natural [[propositions as types|enhancement]] to [[linear type theory]] also as a [[quantum circuit]]-[[quantum programming language|language]] &lbrack;[Abramsky & Duncan (2006)](#AbramskyDuncan06); [Duncan (2006)](#Duncan06)&rbrack;.

> {#DalLagoFaggianQuote} &lbrack;[Dal Lago & Faggian (2012)](#DalLagoFaggian12)&rbrack;: "It’s more and more clear that strong relationships exist between [[linear logic]] and [[quantum computation]]. This seems to go well beyond the easy observation that the intrinsic resource-consciousness of
linear logic copes well with the [[no-cloning theorem|impossibility of cloning and erasing]] qubits."

> &lbrack;[Staton (2015), p. 1](#Staton15)&rbrack;: "A [[quantum programming language]] captures the ideas of [[quantum computation]] in a [[linear type theory]]." 

Indeed:

1. the absence of the [[contraction rule]] [above](#AbsenceOfWeakeningAndContraction), whose [[categorical semantics]] is the *duplication* of [[data]], exactly reflects the *[[no-cloning theorem]]* of [[quantum physics]]

1. the absence of the [[weakening rule]] [above](#AbsenceOfWeakeningAndContraction), whose [[categorical semantics]] is the *erasure* of [[data]], exactly reflects the [[no-deleting theorem]], 

1. the non-cartesian [[multiplicative conjunction]] $\otimes$, whose [[categorical semantics]] is given by [[tensor products]] (such as [[tensor product of Hilbert spaces|of Hilbert spaces]]), reflects the existence of [[quantum entanglement|entangled]] [[terms]] &lbrack;[Baez (2004)](#Baez04)&rbrack;. 

Historically, linear logic was not explicitly motivated as a  [[quantum logic]] this way, but as a logic keeping track of "*resource availability*" (see [below](#ResourceAvailability)), where (again due to the absence of the [[contraction rule]]) a [[variable]] could, a priori, be "only used once" and in fact (due to the absence of the [[weakening rule]]) "exacty once". However, meanwhile the resource concept has also (independently) penetrated [[quantum information theory]] (for example, the [[quantum teleportation]]-protocol uses [[Bell states]] as a resource that allow for and are consumed by  the intended "teleportation" operation), see the references [there](quantum+information#ReferencesQuantumResources).



### As a logic of resource availability
 {#ResourceAvailability}

Unlike many traditional formal systems of [[logic]], which deal with the _[[truth]]_ of _[[propositions]]_, linear logic is often described and was originally motivated &lbrack;[Girard (1987)](#Girard1987)&rbrack; as dealing with the _availability_ of _resources_.  

A proposition, if it is true, remains true no matter how we use that fact in proving other propositions.  By contrast, in using a resource $A$ to make available a resource $B$, $A$ itself may be consumed or
otherwise modified.  Linear logic deals with this by
restricting our ability to duplicate or discard resources
freely.  



For example:

> Let's please add a better example!

We have

$$\text{have cake} \vdash \text{eat cake}$$

from which we can prove

$$\text{have cake},\; \text{have cake} \vdash \text{have cake}
\wedge \text{eat cake}$$

which by left [[contraction rule|contraction]] (duplication of inputs) in [[classical logic]] yields

$$\text{have cake} \vdash \text{have cake} \wedge \text{eat cake}$$

Linear logic would disallow the [[contraction rule|contraction]] step and treat $\text{have cake},\; \text{have cake} \vdash A$ as explicitly meaning that _two_ slices of cake yield $A$.  Disallowing contraction then corresponds to the fact that we can't turn one slice of cake into two (more's the pity), so you can\'t have your cake and eat it too.


### Game semantics

Linear logic can also be interpreted using a semantics of "games" or "interactions".  Under this interpretation, each proposition in a sequent represents a game being played or a transaction protocol being executed.  An assertion of, for instance,

$$ P, Q \vdash R $$

means roughly that if I am playing three simultaneous games of $P$, $Q$, and $R$, in which I am the left player in $P$ and $Q$ and the right player in $R$, then I have a strategy which will enable me to win at least one of them.  Now the above statements about "resources" translate into saying that I have to play in all the games I am given and can't invent new ones on the fly.

For example, $P \vdash P$ can be won by using the copycat strategy where one makes the two games identical except with left and right players reversed.


### As a relevance logic

Linear logic is closely related to notions of [[relevance logic]], which have been studied for much longer.  The goal of relevance logic is to disallow statements like "if pigs can fly, then grass is green" which are true, under the usual logical interpretation of [[implication]], but in which the hypothesis has nothing to do with the conclusion.  Clearly there is a relationship with the "resource semantics": if we want to require that all hypotheses are "used" in a proof then we need to disallow weakening. In linear logic, all hypotheses must be used *exactly once*, whereas in relevance logic(s), all hypotheses must be used *at least* once.  


## Definition

Linear logic is usually given in terms of [[sequent calculus]].  There is a set of __[[propositions]]__ (although as remarked above, to be thought of more as resources to be acquired than as statements to be proved) which we construct through [[recursion]].  Each pair of [[lists]] of propositions is a __sequent__ (written as usual with '$\vdash$' between the lists), some of which are __valid__; we determine which are valid also through recursion.  Technically, the [[propositional calculus]] of linear logic also requires a set of __propositional variables__ from which to start; this is usually identified with the set of [[natural numbers]] (so the variables are $p_0$, $p_1$, etc), although one can also consider the linear logic $LL(V)$ where $V$ is any initial [[set]] of propositional variables.

Here we define the set of propositions:


*  Every propositional variable is a proposition.

*  For each proposition $A$, there is a proposition $A^\perp$, the __[[negation]]__ of $A$.

*  For each proposition $A$ and proposition $B$, there are four additional propositions:

   *  $A \& B$ (read 'with'), the __[[additive conjunction]]__ of $A$ and $B$;

   *  $A \oplus B$ (read 'plus'), the __[[additive disjunction]]__ of $A$ and $B$;

   *  $A \otimes B$ (read 'times'), the __[[multiplicative conjunction]]__ of $A$ and $B$;

   *  $A \parr B$ (read 'par'), the __[[multiplicative disjunction]]__ of $A$ and $B$ (sometimes written $A \mid B$).

*  There are also four constants to go with the four binary operations above:

   *  $\top$ (read 'top'), the __additive [[truth]]__;

   *  $\mathbf{0}$ (read 'zero'), the __additive [[falsity]]__;

   *  $\mathbf{1}$ (read 'one'), the __multiplicative truth__;

   *  $\bot$ (read 'bottom'), the __multiplicative falsity__.

*  For each proposition $A$, there are two additional propositions:

   *  $!{A}$ (read '[[of course]]'), the __[[exponential conjunction]]__ of $A$;

   *  $?{A}$ (read '[[why not]]'), the __[[exponential disjunction]]__ of $A$.

The terms "exponential", "multiplicative", and "additive" come from the fact that "exponentiation converts addition to multiplication": we have $!{(A \& B)}\equiv !{A} \otimes !{B}$ and so on (see below).

However, the connectives and constants can also be grouped in different ways.  For instance, the multiplicative conjunction $\otimes$ and additive disjunction $\oplus$ are both [[positive types]], while the additive conjunction $\&$ and multiplicative disjunction $\parr$ are [[negative types]].  Similarly, the multiplicative truth $\mathbf{1}$ and the additive falsity $\mathbf{0}$ are positive, while the additive truth $\top$ and multiplicative falsity $\bot$ are negative.  This grouping has the advantage that the similarity of symbols matches the adjective used (because the symbols were chosen with this grouping in mind).

But conversely, the natural grouping by multiplicative/additive, or equivalently by de Morgan dual pairs, has led many authors to alter Girard's notation, in particular reverting to the category-theoretic $\times$ and $+$ for the additives $\&$ and $\oplus$, and introducing a different symbol such as $\odot$, $\bullet$ or (confusingly) $\oplus$ for Girard's $\parr$.  But on this page we will stick to Girard's conventions for consistency.

In [[relevance logic]], the terms "conjunction" and "disjunction" are often reserved for the additive versions $\&$ and $\oplus$, which are written with the traditional notations $\wedge$ and $\vee$.  In this case, the multiplicative conjunction $A\otimes B$ is called **fusion** and denoted $A\circ B$, while the multiplicative disjunction $A\parr B$ is called **fission** and denoted $A+B$ (or sometimes, confusingly, $A\oplus B$).  In relevance logic the symbol $\bot$ may also be used for the *additive* falsity, here denoted $\mathbf{0}$.  Also, sometimes the additive connectives are called **extensional** and the multiplicatives **intensional**.

Sometimes one does not define the operation of negation, defining only $p^\perp$ for a propositional variable $p$.  It is a theorem that every proposition above is equivalent (in the sense defined below) to a proposition in which negation is applied only to propositional variables.

We now define the valid sequents, where we write $A, B, C \vdash D, E, F$ to state the validity of the sequent consisting of the list $(A,B,C)$ and the list $(D,E,F)$ and use Greek letters for sublists:

*  The [[structural rules]]:

   *  The [[exchange rule]]:  If a sequent is valid, then any [[permutation]] of it (created by permuting its left and right sides independently) is valid.

   *  The restricted [[weakening rule]]:  If $\Gamma, \Delta \vdash \Theta$, then $\Gamma, !{A}, \Delta \vdash \Theta$, for any $A$; conversely and dually, if $\Gamma \vdash \Delta, \Theta$, then $\Gamma \vdash \Delta, ?{A}, \Theta$ for any $A$.

   *  The restricted [[contraction rule]]:  If $\Gamma, !{A}, !{A}, \Delta \vdash \Theta$, then $\Gamma, !{A}, \Delta \vdash \Theta$; conversely and dually, if $\Gamma \vdash \Delta, ?{A}, ?{A}, \Theta$, then $\Gamma \vdash \Delta, ?{A}, \Theta$.

   *  The [[variable rule]]:  Always, $A \vdash A$;

   *  The [[cut rule]]:  If $\Gamma \vdash A, \Phi$ and $\Psi,A \vdash \Delta$, then $\Psi,\Gamma \vdash \Delta,\Phi$.

*  The [[inference rules]] for each operation:

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

## Related concepts

* [[bounded linear logic]]

* [[affine logic]]

* [[coherence space]]

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

* [[scale]]
  * [[Heyting scale]]
  * [[minor scale]]

* [[linear lambda-calculus]]

* [[antithesis interpretation]]

[[!include logic symbols -- table]]


## References

### General

The original article:

* {#Girard1987} [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science **50** 1 (1987)  &lbrack;<a href="https://doi.org/10.1016/0304-3975(87)90045-4">doi:10.1016/0304-3975(87)90045-4</a>, [pdf](http://iml.univ-mrs.fr/~girard/linear.pdf)&rbrack;
 

Review:

* [[Anne Sjerp Troelstra]], *Lectures on Linear Logic*, CSLI Lectures notes **29** (1992) &lbrack;[ISBN:0937073776](https://web.stanford.edu/group/cslipublications/cslipublications/site/0937073776.shtml)&rbrack;

* [[Frank Pfenning]], *Linear Logic*, CSLI Lecture Notes **29** (1998) &lbrack;[pdf](https://www.cs.cmu.edu/~fp/courses/98-linear/handouts/notes.pdf), [webpage](https://www.cs.cmu.edu/~fp/courses/98-linear/handouts.html), [[Pfenning-LinearLogic98.pdf:file]]&rbrack;

* [[Jean-Yves Girard]], _Linear logic, its syntax and semantics_ (2006) &lbrack;[pdf](http://www.cs.brandeis.edu/~cs112/2006-cs112/docs/girard-intro.pdf)&rbrack;

* {#Girard11} [[Jean-Yves Girard]], part III of _[[Lectures on Logic]]_, European Mathematical Society 2011

* {#MihályiNovitzká13} Daniel Mihályi, Valerie Novitzká, *What about Linear Logic in Computer Science?*, Acta Polytechnica Hungarica **10** 4 (2013) 147-160 &lbrack;[pdf](http://acta.uni-obuda.hu/Mihalyi_Novitzka_42.pdf), [[MihalyiNovitzka-LinearLogic.pdf:file]]&rbrack;

and making explicit the [[categorical semantics]] of linear logic in the category [[FinDimVect]] of [[finite-dimensional vector spaces]]:

* {#Pratt93} [[Vaughan Pratt]], *The second calculus of binary relations*, Mathematical Foundations of Computer Science 1993. MFCS 1993, Lecture Notes in Computer Science **711**, Springer (1993) &lbrack;[doi:10.1007/3-540-57182-5_9](https://doi.org/10.1007/3-540-57182-5_9)&rbrack;
  > "Linear logic is seen in its best light as the realization of the [[Curry-Howard isomorphism]] for [[linear algebra]]"

* {#ValironZdancewic14} [[Benoît Valiron]], [[Steve Zdancewic]], *Finite Vector Spaces as Model of Simply-Typed Lambda-Calculi*, in: *Proc. of ICTAC'14*, Lecture Notes in Computer Science **8687**, Springer (2014) 442-459 &lbrack;[arXiv:1406.1310](https://arxiv.org/abs/1406.1310), [doi:10.1007/978-3-319-10882-7_26](https://doi.org/10.1007/978-3-319-10882-7_26), slides:[pdf](https://www.cs.bham.ac.uk/~drg/bll/steve.pdf), [[Zdancewic-LinearLogicAlgebra.pdf:file]]&rbrack;
 
* {#Murfet14} [[Daniel Murfet]], *Logic and linear algebra: an introduction* &lbrack;[arXiv:1407.2650](http://arxiv.org/abs/1407.2650)&rbrack;

following a remark in section 2.4.2 of [Hyland & Schalk (2003)](#HylandSchalk03).


* {#HylandSchalk03} [[Martin Hyland]], Andrea Schalk, *Glueing and orthogonality for models of linear logic*, Theoretical Computer Science **294** 1–2 (2003) 183-231 \[<a href="https://doi.org/10.1016/S0304-3975(01)00241-9">doi:10.1016/S0304-3975(01)00241-9</a>\]

* Wikipedia: *[Linear Logic](https://secure.wikimedia.org/wikipedia/en/wiki/Linear_logic)*


The [[categorical semantics]] of linear logic in general [[star-autonomous categories]] originally appeared in

* {#Seely} [[R. A. G. Seely]],  *Linear logic, $\ast$-autonomous categories and cofree coalgebras*, in *Categories in Computer Science and Logic*, Contemporary Mathematics **92** (1989)  &lbrack;[[SeelyLinearLogic.pdf:file]], [ps.gz](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz), [ISBN:978-0-8218-5100-5](https://bookstore.ams.org/conm-92)&rbrack;
 
* [[Michael Barr]], *$\ast$-Autonomous categories and linear logic*, Math. Structures Comp. Sci. **1** 2 (1991) 159–178 &lbrack;[doi:10.1017/S0960129500001274](https://doi.org/10.1017/S0960129500001274), [pdf](https://www.math.mcgill.ca/barr/papers/scatll.pdf), [[Barr-AutomomousCatAndLinLogic.pdf:file]]&rbrack;

and for the special case of [[quantales]] in 

* {#Yetter90} [[David Yetter]], _Quantales and (noncommutative) linear logic_, Journal of Symbolic Logic 55 (1990), 41--64.

and further in view of the [[Chu construction]]:

* {#Pratt93} [[Vaughan Pratt]], *The second calculus of binary relations*, Mathematical Foundations of Computer Science 1993. MFCS 1993, Lecture Notes in Computer Science **711**, Springer (1993) &lbrack;[doi:10.1007/3-540-57182-5_9](https://doi.org/10.1007/3-540-57182-5_9)&rbrack;

* {#Pratt99} [[Vaughan Pratt]], *Chu Spaces* (1999) &lbrack;[pdf](http://boole.stanford.edu/pub/coimbra.pdf), [[Pratt-ChuSpaces.pdf:file]]&rbrack;

 

The more general case of of multiplicative intuitionistic linear logic interpreted more generally in [[symmetric monoidal categories]] was systematically developed in

* {#Szabo78} M.E. Szabo, _Algebra of Proofs_, Studies in Logic and the Foundations of Mathematics, vol. 88 (1978), North-Holland. 
 
> (that was before Girard introduced the "linear" terminology).


More recent articles exploring this:

* {#dePaiva89} [[Valeria de Paiva]], _The Dialectica Categories_, _Contemporary Mathematics_ 92, 1989. ([web] (http://www.cs.bham.ac.uk/~vdp/publications/dial87.pdf)) 
 

* {#Blute91} [[Richard Blute]], _Linear logic, coherence, and dinaturality_, Dissertation, University of Pennsylvania 1991, published in Theoretical Computer Science archive
Volume 115 Issue 1, July 5, 1993  Pages 3--41 
 

* {#BentonBiermanPaivaHyland92} [[Nick Benton]], [[Gavin Bierman]], [[Valeria de Paiva]], [[Martin Hyland]], _Term assignments for intuitionistic linear logic_. Technical report 262, Cambridge 1992 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.31.8666), [ps](http://www.cs.bham.ac.uk/~vdp/publications/tr262.ps))
 

* {#HylandPaiva93} [[Martin Hyland]], [[Valeria de Paiva]], _Full Intuitionistic Linear Logic_ (extended abstract). Annals of Pure and Applied Logic, 64(3), pp. 273--291, 1993. ([pdf](http://www.cs.bham.ac.uk/~vdp/publications/fill.pdf))
 

* {#Bierman95} G. Bierman, _On Intuitionistic Linear Logic_ PhD thesis, Computing Laboratory, University of Cambridge, 1995 ([pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.114.588&rep=rep1&type=pdf))

* {#Barber97} Andrew Graham Barber, _Linear Type Theories, Semantics and Action Calculi_, PhD thesis, Edinburgh 1997 ([web](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/&#8206;), [pdf](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/ECS-LFCS-97-371.pdf))



This is reviewed/further discussed in

* {#Schalk04} Andrea Schalk, _What is a categorical model for linear logic?_ ([pdf](http://www.cs.man.ac.uk/~schalk/notes/llmodel.pdf))

* [[Richard Blute]], Philip Scott, _Category theory for linear logicians_, 2004 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.83.6250))

* {#Melliès02} [[Paul-André Melliès]], *Categorical models of linear logic revisited* (2002) &lbrack;[hal:00154229](https://hal.science/hal-00154229)&rbrack;

* {#Melliès09} [[Paul-André Melliès]], *Categorical semantics of linear logic*, in *[Interactive models of computation and program behaviour](https://smf.emath.fr/publications/modeles-interactifs-de-calcul-et-de-comportement-de-programme)*, Panoramas et synthèses **27** (2009) 1-196 &lbrack;[web](https://smf.emath.fr/publications/semantique-categorielle-de-la-logique-lineaire), [pdf](https://www.irif.fr/~mellies/papers/panorama.pdf), [[Mellies-CategoricalSemanticsLinear.pdf:file]]&rbrack;
 

* [[Paul-André Melliès]], *A Functorial Excursion Between Algebraic Geometry and Linear Logic*, in 37th Annual ACM/IEEE Symposium on Logic in Computer Science (LICS '22), Haifa, Israel  (2022). ACM, New York &lbrack;[doi:10.1145/3531130.3532488](https://doi.org/10.1145/3531130.3532488), [pdf](https://www.irif.fr/~mellies//papers/functorial-excursion.pdf)&rbrack;


The relation of dual intuitionistic linear logic and $\pi$-calculus is given in

* Luis Caires, [[Frank Pfenning]]. _Session Types as Intuitionistic Linear Propositions_.

Noncommutative linear logic is discussed for instance in

* [[Richard Blute]], F. Lamarche, Paul Ruet, _Entropic Hopf algebras and models of non-commutative logic_, Theory and Applications of Categories, Vol. 10, No. 17, 2002, pp. 424&#8211;460. ([pdf](http://www.emis.ams.org/journals/TAC/volumes/10/17/10-17.pdf))


Further discussion of [[linear type theory]] is for instance in

* _Chapter 7, Linear type theory_ [pdf](http://www.cs.cmu.edu/~fp/courses/linear/handouts/lintt.pdf)


* Anders Schack-Nielsen, Carsten Sch&#252;rmann, _Linear contextual modal type theory_ [pdf](http://www.itu.dk/~carsten/papers/lcmtt.pdf)


See also:

* {#Blass1992} [[Andreas Blass]]: _A game semantics for linear logic_ Annals of Pure and Applied Logic **56** (1992) 183-220

* [[Richard Garner]]: *Three investigations into linear logic*, MSc thesis, Macquarie (2005) &lbrack;[pdf](https://web.science.mq.edu.au/~rgarner/Thesis/Smith-Knight-Essay.pdf), [[Garner-LinearLogic.pdf:file]]&rbrack;


Discussion of [[linear type theory]] without [[units]]: 

* [[Robin Houston]], _Linear Logic without Units_ ([arXiv:1305.2231](http://arxiv.org/abs/1305.2231))


Discussion of [[inductive types]] in the context of [[linear type theory]]:

* St&#233;phane Gimenez, _Towards Generic Inductive Constructions inSystems of Nets_ &lbrack;[pdf](http://www.imn.htwk-leipzig.de/WST2013/papers/paper_16.pdf)&rbrack;


The [[categorical semantics ]]of differential linear logic is introduced in:

* {#Blute-Cockett-Seely06} [[Richard Blute]], [[Robin Cockett]], [[Robert Seely]], _Differential Categories_, Mathematical structures in computer science 16.6 (2006): 1049--1083. ([pdf](https://pdfs.semanticscholar.org/82b0/f9533b451d174f407b35e1c39e2376138ac2.pdf)) 



The antithesis interpretation is

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518).

### In relation to quantum computing

Discussion of application of linear logic to [[quantum logic]], [[quantum computing]] and generally to [[quantum physics]] (See also at *[[quantum programming languages]]*):

* {#Pratt92} [[Vaughan Pratt]], _Linear logic for generalized quantum mechanics_, in Proc. of _Workshop on Physics and Computation (PhysComp'92)_ ([pdf](http://boole.stanford.edu/pub/ql.pdf), [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.137.7817))

* [[Benoît Valiron]], *A functional programming language for quantum computation with classical control*, MSc thesis, University of Ottawa (2004) &lbrack;[doi:10.20381/ruor-18372](http://dx.doi.org/10.20381/ruor-18372), [pdf](https://ruor.uottawa.ca/bitstream/10393/26790/1/MR01625.PDF)&rbrack;

* {#SelingerValiron04} [[Peter Selinger]], [[Benoît Valiron]], *A lambda calculus for quantum computation with classical control*, Proc. of TLCA 2005 &lbrack;[arXiv:cs/0404056](https://arxiv.org/abs/cs/0404056), [doi:10.1007/11417170_26](https://doi.org/10.1007/11417170_26)&rbrack;

* {#SelingerValiron09} [[Peter Selinger]], [[Benoît Valiron]], *Quantum Lambda Calculus*, in: *Semantic Techniques in Quantum Computation*, Cambridge University Press (2009) 135-172 &lbrack;[doi:10.1017/CBO9781139193313.005](https://doi.org/10.1017/CBO9781139193313.005), [pdf](https://www.mscs.dal.ca/~selinger/papers/qlambdabook.pdf)&rbrack;

  > (cf. *[[quantum lambda-calculus]]*)


* {#Baez04} [[John Baez]], *Quantum Quandaries: a Category-Theoretic Perspective*, in D. Rickles et al. (ed.) *The structural foundations of quantum gravity*, Clarendon Press (2006) 240-265 &lbrack;[arXiv:quant-ph/0404040](https://arxiv.org/abs/quant-ph/0404040), [ISBN:9780199269693](https://global.oup.com/academic/product/the-structural-foundations-of-quantum-gravity-9780199269693)&rbrack;


* {#AbramskyDuncan06} [[Samson Abramsky]], [[Ross Duncan]], *A Categorical Quantum Logic*, Mathematical Structures in Computer Science **16** 3 (2006) &lbrack;[arXiv:quant-ph/0512114](http://arxiv.org/abs/quant-ph/0512114), [doi:10.1017/S0960129506005275](https://doi.org/10.1017/S0960129506005275)&rbrack;

* {#Duncan06} [[Ross Duncan]], _Types for quantum computation_, 2006 ([pdf](http://www.cs.ox.ac.uk/files/2425/Types%20for%20Quantum%20Computation.pdf))


* {#DalLagoFaggian12} [[Ugo Dal Lago]], [[Claudia Faggian]], *On Multiplicative Linear Logic, Modality and Quantum Circuits*, EPTCS 95 (2012) 55-66 &lbrack;[arXiv:1210.0613](http://arxiv.org/abs/1210.0613), [doi:10.4204/EPTCS.95.6](https://doi.org/10.4204/EPTCS.95.6)&rbrack;

* {#Staton15} [[Sam Staton]], *Algebraic Effects, Linearity, and Quantum Programming Languages*, POPL '15: Proceedings of the 42nd Annual ACM SIGPLAN-SIGACT Symposium on Principles of Programming Languages (2015) $[$[doi:10.1145/2676726.2676999](https://doi.org/10.1145/2676726.2676999), [pdf](http://www.cs.ox.ac.uk/people/samuel.staton/papers/popl2015.pdf)$]$

* {#CCGP09} Gianpiero Cattaneo, Maria Luisa Dalla Chiara, Roberto Giuntini and Francesco Paoli, section 9 of _Quantum Logic and Nonclassical Logics_, p. 127 in  Kurt Engesser, Dov M. Gabbay, Daniel Lehmann (eds.) _Handbook of Quantum Logic and Quantum Structures: Quantum Logic_, 2009 North Holland
  


Application of linear logic to [[matrix factorization]] in [[Landau–Ginzburg models]]:

* [[Daniel Murfet]], _The cut operation on matrix factorisations_, Journal of Pure and Applied Algebra
**222** 7 (2018) 1911-1955 &lbrack;[arXiv:1402.4541](https://arxiv.org/abs/1402.4541), [doi:10.1016/j.jpaa.2017.08.014](https://doi.org/10.1016/j.jpaa.2017.08.014)&rbrack;

Relating linear logic to [[quantum error correction]]:

* [[Daniel Murfet]], William Troiani, *Linear Logic and Quantum Error Correcting Codes* &lbrack;[arXiv:2405.19051](https://arxiv.org/abs/2405.19051)&rbrack;



[[!redirects linear logic]]
[[!redirects linear logics]]

[[!redirects classical linear logic]]
[[!redirects classical linear logics]]
[[!redirects CLL]]
[[!redirects intuitionistic linear logic]]
[[!redirects ILL]]
[[!redirects multiplicative intuitionistic linear logic]]
[[!redirects multiplicative classical linear logic]]
[[!redirects MILL]]
[[!redirects multiplicative linear logic]]
[[!redirects MLL]]
[[!redirects multiplicative-additive linear logic]]
[[!redirects MALL]]
