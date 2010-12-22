
# Contents
* automatic table of contents goes here
{:toc}

## Idea

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

Linear logic was introduced in [Girard (1987)](#Girard).  Although it is
usually presented in terms of inference rules, it was
apparently discovered by Girard while studying [[coherent
space|coherent
spaces]] (see [Wikipedia](http://en.wikipedia.org/wiki/Coherent_space)) (not
the topological kind).


## Definition

Linear logic is usually given in terms of [[sequent calculus]].  There is a set of __[[propositions]]__ (although as remarked above, to be thought of more as resources to be acquired than as statements to be proved) which we construct through [[recursion]].  Each pair of [[lists]] of propositions is a __sequent__ (written as usual with '$\vdash$' between the lists), some of which are __valid__; we determine which are valid also through recursion.  Technically, the [[propositional calculus]] of linear logic also requires a set of __propositional variables__ from which to start; this is usually identified with the set of [[natural numbers]] (so the variables are $p_0$, $p_1$, etc), although one can also consider the linear logic $LL(V)$ where $V$ is any initial [[set]] of propositional variables.

Here we define the set of propositions:

*  Every propositional variable is a proposition.
*  For each proposition $A$, there is a proposition $A^\perp$, the __[[negation]]__ of $A$.
*  For each proposition $A$ and proposition $B$, there are four additional propositions:
   *  $A \& B$ (read 'with'), the __additive [[conjunction]]__ of $A$ and $B$;
   *  $A \oplus B$ (read 'plus'), the __additive [[disjunction]]__ of $A$ and $B$;
   *  $A \otimes B$ (read 'times'), the __multiplicative conjunction__ of $A$ and $B$;
   *  $A \parr B$ (read 'par' and sometimes written $A \mid B$), the __multiplicative disjunction__ of $A$ and $B$.
*  There are also four constants to go with the four binary operations above:
   *  $\top$ (read 'top'), the __additive [[truth]]__;
   *  $\mathbf{0}$ (read 'zero'), the __additive [[falsity]]__;
   *  $\mathbf{1}$ (read 'one'), the __multiplicative truth__;
   *  $\bot$ (read 'bottom'), the __multiplicative falsity__.
*  For each proposition $A$, there are two additional propositions:
   *  $!{A}$ (read 'of course'), the __exponential conjunction__ of $A$;
   *  $?{A}$ (read 'why not'), the __exponential disjunction__ of $A$.

Sometimes one does not define the operation of negation, defining only $p^\perp$ for a propositional variable $p$.  It is a theorem that every proposition above is equivalent (in the sense defined below) to a proposition in which negation is applied only to propositional variables.

Here we define the valid sequents, where we write $A : B : C \vdash D : E : F$ to state the validity of the sequent consisting of the list $(A,B,C)$ and the list $(D,E,F)$ and use Greek letters for sublists:

*  The [[structural rule]]s:
   *  The [[exchange rule]]:  If a sequent is valid, then any [[permutation]] of it (created by permuting its left and right sides independently) is valid.
   *  The [[identity rule]]:  $\Gamma \vdash \Gamma$ is valid, where $\Gamma$ is any list of propositions;
   *  The [[cut rule]]:  If $\Gamma \vdash \Delta$ and $\Delta \vdash \Theta$, then $\Gamma \vdash \Theta$.
   *  The restricted [[weakening rule]]:  If $\Gamma : \Delta \vdash \Theta$, then $\Gamma : !{A} : \Delta \vdash \Theta$, where $A$ is any proposition; conversely and dually, if $\Gamma \vdash \Delta : \Theta$, then $\Gamma \vdash \Delta : ?{A} : \Theta$.
   *  The restricted [[contraction rule]]:  If $\Gamma : !{A} : !{A} : \Delta \vdash \Theta$, then $\Gamma : !{A} : \Delta \vdash \Theta$; conversely and dually, if $\Gamma \vdash \Delta : ?{A} : ?{A} : \Theta$, then $\Gamma \vdash \Delta : ?{A} : \Theta$.
*  The logical rules for each operation:
   *  If $\Gamma \vdash A : \Delta$, then $\Gamma : A^\perp \vdash \Delta$; conversely and dually, if $\Gamma : A \vdash \Delta$, then $\Gamma \vdash A^\perp : \Delta$.
   *  If $\Gamma : A : \Delta \vdash \Theta$ or $\Gamma : B : \Delta \vdash \Theta$, then $\Gamma : A \& B : \Delta \vdash \Theta$; conversely, if $\Gamma \vdash \Delta : A : \Theta$ and $\Gamma \vdash \Delta : B : \Theta$, then $\Gamma \vdash \Delta : A \& B : \Theta$.
   *  Dually, if $\Gamma \vdash \Delta : A : \Theta$ or $\Gamma \vdash \Delta : B : \Theta$, then $\Gamma \vdash \Delta : A \oplus B : \Theta$; conversely, if $\Gamma : A : \Delta \vdash \Theta$ and $\Gamma : B : \Delta \vdash \Theta$, then $\Gamma : A \oplus B : \Delta \vdash \Theta$.
   *  If $\Gamma : A : B \Delta \vdash \Theta$, then $\Gamma : A \otimes B : \Delta \vdash \Theta$; conversely, if $\Gamma \vdash \Delta : A $ and $\vdash B : \Theta$, then $\Gamma \vdash \Delta : A \otimes B : \Theta$.
   *  Dually, if $\Gamma \vdash \Delta : A : B : \Theta$, then $\Gamma \vdash \Delta : A \parr B : \Theta$; conversely, if $A : \Gamma \vdash \Delta$ and $\Theta : B \vdash$, then $\Theta : A \parr B : \Gamma \vdash \Delta$.
   *  Always $\Gamma \vdash \Delta : \top : \Theta$; dually (there is no converse), $\Gamma : \mathbf{0} : \Delta \vdash \Theta$.
   *  If $\Gamma : \Delta \vdash \Theta$, then $\Gamma : \mathbf{1} : \Delta \vdash \Theta$; conversely, $\vdash \mathbf{1}$.
   *  Dually, if $\Gamma \vdash \Delta : \Theta$, then $\Gamma \vdash \Delta : \bot : \Theta$; conversely, $\bot \vdash$.
   *  If $\Gamma : A : \Delta \vdash \Theta$, then $\Gamma : !{A} : \Delta \vdash \Theta$; conversely, if $\Gamma \vdash \Delta : A : \Theta$, then $\Gamma \vdash \Delta : !{A} : \Theta$ *if* $\Gamma$ consists entirely of propositions of the form $!{-}$ while $\Delta$ and $\Theta$ consist entirely of propositions of the form $?{-}$.
   *  Dually, if $\Gamma \vdash \Delta : A : \Theta$, then $\Gamma \vdash \Delta : ?{A} : \Theta$; conversely, if $\Gamma : A : \Delta \vdash \Theta$, then $\Gamma : ?{A} : \Delta \vdash \Theta$ *if* $\Gamma$ and $\Delta$ consist entirely of propositions of the form $!{-}$ while $\Theta$ consists entirely of propositions of the form $?{-}$.

The main point of linear logic is the restricted use of the weakening and contraction rules; if these were universally valid (applying to any $A$ rather than only to $!{A}$ or $?{A}$), then the additive and multiplicative operations would be equivalent (in the sense defined below) and similarly $!{A}$ and $?{A}$ would be equivalent to $A$, which would give us [[classical logic]].  On the other hand, one can also remove the exchange rule to get a variety of [[noncommutative logic]]; one must then be careful about how to write the other rules (which we have been above).

As usual, there is a theorem of [[cut elimination]] showing that the cut rule and identity rule follow from all other rules and the special cases of the identity rule of the form $p \vdash p$ for a propositional variable $p$.

The propositions $A$ and $B$ are __equivalent__ if $A \vdash B$ and $B \vdash A$ are both valid.  It is then a theorem that either may be swapped for the other anywhere in a sequent without affecting its validity.  Up to equivalence, negation is an [[involution]], and the operations $\&$, $\oplus$, $\otimes$, and $\parr$ are all [[associative]], with respective [[identity elements]] $\top$, $\mathbf{0}$, $\mathbf{1}$, and $\bot$.  These operations are also [[commutative operation|commutative]] (although this fails for $\otimes$ and $\parr$ if we drop the exchange rule).  We also have [[distributive law|distributive laws]] that explain the adjectives 'additive', 'multiplicative', and 'exponential':

*  $A \otimes (B \oplus C) \equiv (A \otimes B) \oplus (A \otimes C)$ (and on the other side);
*  dually, $A \parr (B \& C) \equiv (A \parr B) \& (A \parr C)$ (and on the other side);
*  $!{(A \& B)} \equiv !{A} \otimes !{B}$;
*  dually, $?{(A \oplus B)} \equiv ?{A} \parr ?{B}$.

It is also a theorem that negation (except for the negations of propositional variables) can be defined (up to equivalence) recursively as follows:

*  $(A^\perp)^\perp \equiv A$;
*  $(A \& B)^\perp \equiv A^\perp \oplus B^\perp$ and vice versa;
*  $(A \otimes B)^\perp \equiv A^\perp \parr B^\perp$ and vice versa;
*  $\top^\perp \equiv \mathbf{0}$ and vice versa;
*  $\mathbf{1}^\perp \equiv \bot$ and vice versa;
*  $(!{A})^\perp \equiv ?{A^\perp}$ and vice versa.

(In this way, linear logic has a perfect [[de Morgan duality]].)  The logical rules for negation can then be proved.

We can also restrict attention to sequents with one term on either side as follows:  $\Gamma \vdash \Delta$ is valid if and only if $\bigotimes \Gamma \vdash \parr \Delta$ is valid, where $\bigotimes(A : B : C) \coloneqq A \otimes B \otimes C$, etc, and similarly for $\parr$ (using implicitly that these are associative, with identity elements to handle the [[empty sequence]]).

We can even restrict attention to sequents with no term on the left side and one term on the right; $A \vdash B$ is valid if and only if $\vdash A \multimap B$ is valid, where $A \multimap B \coloneqq A^\perp \parr B$.  In this way, it\'s possible to ignore sequents entirely and speak only of propositions and valid propositions, eliminating half of the logical rules in the process.  However, this approach is not as beautifully symmetric as the full sequent calculus.


## Categorial formulation

Probably the best way to explain linear logic to a category theorist
is to say that its models are
[[*-autonomous categories]] with extra
structure (see [Seely, 1989](#Seely)).

Firstly, there is a monoidal '[[tensor product|tensor]]' connective
$A \otimes B$.  [[negation|Negation]] $A^\bot$ is modelled by the duality
involution $(-)^*$, while linear implication $A\multimap B$
corresponds to the [[internal hom]], which can be defined as
$(A\otimes B^\bot)^\bot$.  There is a [[de Morgan dual]] of the
tensor called 'par', with $A \parr B = (A^\bot\otimes B^\bot)^\bot$.  Tensor and par are the
'multiplicative' connectives, which roughly speaking represent the
parallel availability of resources. 

The 'additive' connectives $\&$ and $\oplus$, which
correspond in another way to traditional [[conjunction]] and
[[disjunction]], are modelled as usual by [[product]]s and
[[coproduct]]s.  [Seely (1989)](#Seely) notes that products are sufficient, as $*$-autonomy then guarantees the existence of coproducts; that is, they are also linked by [[de Morgan duality]].

LL recaptures the notion of a resource that can be discarded
or copied arbitrarily by the use of the [[modal logic|modal]] operator $!$:
$!A$ denotes an '$A$-factory', a resource that can produce
zero or more $A$s on demand.  It is modelled using a [[comonad]]
$!$ on the underlying $*$-autonomous category that is
([[symmetric monoidal category|symmetric]]) [[monoidal category|monoidal]], in the sense that there is an
isomorphism $!A\otimes!B \cong !(A\& B)$.  Since every
$A$ is canonically a symmetric $\&$-[[comonoid]] (remembering that $\&$ is the product), $!A$ is
then a symmetric $\otimes$-comonoid.

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


## References

*  Girard, Jean-Yves, 'Linear logic'.  _Theoretical Computer
   Science_ 50:1, 1987.
{#Girard}

*  Seely, R. A. G., 'Linear logic, $*$-autonomous categories
   and cofree coalgebras', _Contemporary Mathematics_ 92,
   1989.  Available in [PostScript](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz).
{#Seely}

*  The [article](https://secure.wikimedia.org/wikipedia/en/wiki/Linear_logic) on the English Wikipedia has good summaries of the meanings of the logical operators and of the commonly studied fragments.


[[!redirects linear logic]]
[[!redirects linear logics]]
