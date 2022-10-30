
# Contents
* automatic table of contents goes here
{:toc}

## Idea

**Linear logic** is a [[substructural logic]] in which the [[contraction rule]] and the [[weakening rule]] are omitted, or at least have their applicability restricted.  It has a number of interpretations, of which we discuss several below.

Linear logic was introduced in [Girard (1987)](#Girard).  Although it is
usually presented in terms of inference rules, it was
apparently discovered by Girard while studying [[coherence
space|coherent
spaces]] (see [Wikipedia](http://en.wikipedia.org/wiki/Coherent_space)) (not
the [[coherent topological space|topological kind]]).


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


### As a relevant logic

Linear logic is closely related to notions of [[relevant logic]], which have been studied for much longer.  The goal of relevant logic is to disallow statements like "if pigs can fly, then grass is green" which are true, under the usual logical interpretation of [[implication]], but in which the hypothesis has nothing to do with the conclusion.  Clearly there is a relationship with the "resource semantics": if we want to require that all hypotheses are "used" in a proof then we need to disallow weakening.


### Categorical interpretations

To a category theorist, it may be easiest to think of linear logic in terms of [[*-autonomous categories]] or [[polycategories]]; see below.


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

The terms "exponential", "multiplicative", and "additive" come from the fact that "exponentiation converts addition to multiplication": we have $!{(A \& B)}\equiv !{A} \otimes !{B}$ and so on (see below).

However, the connectives and constants can also be grouped in different ways.  For instance, the multiplicative conjunction $\otimes$ and addditive disjunction $\oplus$ are both [[positive types]], while the additive conjunction $\&$ and multiplicative disjunction $\parr$ are [[negative types]].  Similarly, the multiplicative truth $\mathbf{1}$ and the additive falsity $\mathbf{0}$ are positive, while the additive truth $\top$ and multiplicative falsity $\bot$ are negative.  This grouping has the advantage that the similarity of symbols matches the adjective used.

In [[relevant logic]], the terms "conjunction" and "disjunction" are often reserved for the additive versions $\&$ and $\oplus$, which are written with the traditional notations $\wedge$ and $\vee$.  In this case, the multiplicative conjunction $A\otimes B$ is called **fusion** and denoted $A\circ B$, while the multiplicative disjunction $A\parr B$ is called **fission** and denoted $A+B$ (or sometimes, confusingly, $A\oplus B$).  In relevant logic the symbol $\bot$ may also be used for the *additive* falsity, here denoted $\mathbf{0}$.  Also, sometimes the additive connectives are called **extensional** and the multiplicatives **intensional**.

Sometimes one does not define the operation of negation, defining only $p^\perp$ for a propositional variable $p$.  It is a theorem that every proposition above is equivalent (in the sense defined below) to a proposition in which negation is applied only to propositional variables.

We now define the valid sequents, where we write $A : B : C \vdash D : E : F$ to state the validity of the sequent consisting of the list $(A,B,C)$ and the list $(D,E,F)$ and use Greek letters for sublists:

*  The [[structural rule]]s:
   *  The [[exchange rule]]:  If a sequent is valid, then any [[permutation]] of it (created by permuting its left and right sides independently) is valid.
   *  The restricted [[weakening rule]]:  If $\Gamma : \Delta \vdash \Theta$, then $\Gamma : !{A} : \Delta \vdash \Theta$, for any $A$; conversely and dually, if $\Gamma \vdash \Delta : \Theta$, then $\Gamma \vdash \Delta : ?{A} : \Theta$ for any $A$.
   *  The restricted [[contraction rule]]:  If $\Gamma : !{A} : !{A} : \Delta \vdash \Theta$, then $\Gamma : !{A} : \Delta \vdash \Theta$; conversely and dually, if $\Gamma \vdash \Delta : ?{A} : ?{A} : \Theta$, then $\Gamma \vdash \Delta : ?{A} : \Theta$.
   *  The [[identity rule]]:  Always, $A \vdash A$;
   *  The [[cut rule]]:  If $\Gamma \vdash A$ and $A \vdash \Delta$, then $\Gamma \vdash \Delta$.
*  The logical rules for each operation:
   *  If $\Gamma \vdash A : \Delta$, then $\Gamma : A^\perp \vdash \Delta$; conversely and dually, if $\Gamma : A \vdash \Delta$, then $\Gamma \vdash A^\perp : \Delta$.
   *  If $\Gamma : A : \Delta \vdash \Theta$ or $\Gamma : B : \Delta \vdash \Theta$, then $\Gamma : A \& B : \Delta \vdash \Theta$; conversely, if $\Gamma \vdash \Delta : A : \Theta$ and $\Gamma \vdash \Delta : B : \Theta$, then $\Gamma \vdash \Delta : A \& B : \Theta$.
   *  Dually, if $\Gamma \vdash \Delta : A : \Theta$ or $\Gamma \vdash \Delta : B : \Theta$, then $\Gamma \vdash \Delta : A \oplus B : \Theta$; conversely, if $\Gamma : A : \Delta \vdash \Theta$ and $\Gamma : B : \Delta \vdash \Theta$, then $\Gamma : A \oplus B : \Delta \vdash \Theta$.
   *  If $\Gamma : A : B \Delta \vdash \Theta$, then $\Gamma : A \otimes B : \Delta \vdash \Theta$; conversely, if $\Gamma \vdash \Delta : A $ and $\vdash B : \Theta$, then $\Gamma \vdash \Delta : A \otimes B : \Theta$.
   *  Dually, if $\Gamma \vdash \Delta : A : B : \Theta$, then $\Gamma \vdash \Delta : A \parr B : \Theta$; conversely, if $A : \Gamma \vdash \Delta$ and $\Theta : B \vdash$, then $\Theta : A \parr B : \Gamma \vdash \Delta$.
   *  Always $\Gamma \vdash \Delta : \top : \Theta$; dually (there is no converse), $\Gamma : \mathbf{0} : \Delta \vdash \Theta$.
   *  If $\Gamma : \Delta \vdash \Theta$, then $\Gamma : \mathbf{1} : \Delta \vdash \Theta$; conversely, $\vdash \mathbf{1}$.
   *  Dually, if $\Gamma \vdash \Delta : \Theta$, then $\Gamma \vdash \Delta : \bot : \Theta$; conversely, $\bot \vdash$.
   *  If $\Gamma : A : \Delta \vdash \Theta$, then $\Gamma : !{A} : \Delta \vdash \Theta$; conversely, if $\Gamma \vdash \Delta : A : \Theta$, then $\Gamma \vdash \Delta : !{A} : \Theta$, whenever $\Gamma$ consists entirely of propositions of the form $!{-}$ while $\Delta$ and $\Theta$ consist entirely of propositions of the form $?{-}$.
   *  Dually, if $\Gamma \vdash \Delta : A : \Theta$, then $\Gamma \vdash \Delta : ?{A} : \Theta$; conversely, if $\Gamma : A : \Delta \vdash \Theta$, then $\Gamma : ?{A} : \Delta \vdash \Theta$, whenever $\Gamma$ and $\Delta$ consist entirely of propositions of the form $!{-}$ while $\Theta$ consists entirely of propositions of the form $?{-}$.

The main point of linear logic is the restricted use of the weakening and contraction rules; if these were universally valid (applying to any $A$ rather than only to $!{A}$ or $?{A}$), then the additive and multiplicative operations would be equivalent (in the sense defined below) and similarly $!{A}$ and $?{A}$ would be equivalent to $A$, which would give us [[classical logic]].  On the other hand, one can also remove the exchange rule to get a variety of [[noncommutative logic]]; one must then be careful about how to write the other rules (which we have been above).

As usual, there is a theorem of [[cut elimination]] showing that the cut rule and identity rule follow from all other rules and the special cases of the identity rule of the form $p \vdash p$ for a propositional variable $p$.

The propositions $A$ and $B$ are __equivalent__ if $A \vdash B$ and $B \vdash A$ are both valid.  It is then a theorem that either may be swapped for the other anywhere in a sequent without affecting its validity.  Up to equivalence, negation is an [[involution]], and the operations $\&$, $\oplus$, $\otimes$, and $\parr$ are all [[associative]], with respective [[identity elements]] $\top$, $\mathbf{0}$, $\mathbf{1}$, and $\bot$.  These operations are also [[commutative operation|commutative]] (although this fails for the multiplicative connectives if we drop the exchange rule).  The additive connectives are also [[idempotent]] (but the multiplicative ones are not).

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

(In this way, linear logic has a perfect [[de Morgan duality]].)  The logical rules for negation can then be proved.

We can also restrict attention to sequents with one term on either side as follows:  $\Gamma \vdash \Delta$ is valid if and only if $\bigotimes \Gamma \vdash \parr \Delta$ is valid, where $\bigotimes(A : B : C) \coloneqq A \otimes B \otimes C$, etc, and similarly for $\parr$ (using implicitly that these are associative, with identity elements to handle the [[empty sequence]]).

We can even restrict attention to sequents with no term on the left side and one term on the right; $A \vdash B$ is valid if and only if $\vdash A \multimap B$ is valid, where $A \multimap B \coloneqq A^\perp \parr B$.  In this way, it\'s possible to ignore sequents entirely and speak only of propositions and valid propositions, eliminating half of the logical rules in the process.  However, this approach is not as beautifully symmetric as the full sequent calculus.


## Fragments

The logic described above is full classical linear logic.  There are many important fragments of linear logic, such as multiplicative linear logic, intuitionistic linear logic (in which $\multimap$ is a primitive operation), etc.


## Categorial formulation

### $*$-autonomous categories

One way to explain linear logic to a category theorist is to say that its models are [[*-autonomous categories]] with extra structure (see [Seely, 1989](#Seely)).

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

One merit of the polycategory approach is that it makes the role of the structural rules clearer, and also helps explain why $\parr$ sometimes seems like a disjunction and sometimes like a conjunction.  Allowing contraction and weakening on the left corresponds to our polycategory being "left cartesian"; that is, we have "diagonal" and "projection" operations such as $Hom(A,A; B) \to Hom(A;B)$ and $Hom(;B) \to Hom(A,B)$.  In the presence of these operations, a representing object is automatically a cartesian product; thus $\otimes$ coincides with $\&$.  Similarly, allowing contraction and weakening on the right makes the polycategory "right cocartesian", which causes corepresenting objects to be coproducts and thus $\parr$ to coincide with $\oplus$.

On the other hand, if we allow "multi-composition" in our polycategory, i.e. we can compose a morphism $A \to (B,C)$ with one $(B,C)\to D$ to obtain a morphism $A\to D$, then our polycategory becomes a [[PROP]], and representing and corepresenting objects must coincide; thus $\otimes$ and $\parr$ become the same.  This explains why $\parr$ has both a disjunctive and a conjunctive aspect.  Of course, if in addition to multi-composition we have the left and right cartesian properties, then all four connectives coincide (including the categorical product and coproduct) and we have an [[additive category]].


## Game semantics

We can interpret any proposition in linear logic as a game between two players: we and they. The overall rules are perfectly symmetric between us and them, although no individual game is. At any given moment in a game, exactly one of these four situations obtains: it is our turn, it is their turn, we have won, or they have won; the last two states continue forever afterwards (and the game is over).  If it is our turn, then they are winning; if it is their turn, then we are winning.  So there are two ways to win: because the game is over (and a winner has been decided), or because it is forever the other players turn (either because they have no move or because every move results in its still being their turn).

This is a little complicated, but it\'s important in order to be able to distinguish the four constants:

*  In $\top$, it is their turn, but they have no moves; the game never ends, but we win.
*  Dually, in $\mathbf{0}$, it is our turn, but we have no moves; the game never ends, but they win.
*  In contrast, in $\mathbf{1}$, the game ends immediately, and we have won.
*  Dually, in $\bot$, the game ends immediately, and they have won.

The binary operators show how to combine two games into a larger game:

*  In $A \& B$, is is their turn, and they must choose to play either $A$ or $B$.  Once they make their choice, play continues in the chosen game, with ending and winning conditions as in that game.
*  Dually, in $A \oplus B$, is is our turn, and we must choose to play either $A$ or $B$.  Once we make our choice, play continues in the chosen game, with ending and winning conditions as in that game.
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

Game semantics for linear logic was first proposed by [[Andreas Blass]], I believe in [Blass (1992)](#Blass).  The semantics here may or may not be the same as proposed by Blass.


## Multiple exponential operators

Much as there are many [[exponential functions]] (say from $\mathbb{R}$ to $\mathbb{R}$), even though there is only one addition operation and one multiplication operation, so there can be many versions of the exponential operators $!$ and $?$.  (However, there doesn\'t seem to be any analogue of the [[logarithm]] to convert between them.)

More precisely, if we add to the language of linear logic two more operators, $!'$ and $?'$, and postulate of them the same rules as for $!$ and $?$, we cannot prove that $!{A} \equiv !'{A}$ and $?{A} \equiv ?'{A}$.  In contrast, if we introduce $\&'$, $\bot'$, etc, we *can* prove that the new operators are equivalent to the old ones.

In terms of the categorial interpretation above, there may be many comonads $!$; it is not determined by the underlying $*$-autonomous category.  In terms of game/resource semantics, there are several slightly different interpretations of the exponentials.

One sometimes thinks of the exponentials as coming from infinitary applications of the other operations.  For example:

*  $!{A} \coloneqq 1 \& A \& (A \otimes A) \& (A \otimes A \otimes A) \& \cdots$,
*  $!{A} \coloneqq (1 \& A) \otimes (1 \& A) \otimes (1 \& A) \otimes \cdots$,
*  $!{A} \coloneqq 1 \& k A \& (k^2/2) (A \otimes A) \& (k^3/6) (A \otimes A \otimes A) \& \cdots$ (which is $\mathrm{e}^{k A}$ in an appropriate sense), where $n A$ means an $n$-fold additive conjunction $A \& \cdots \& A$ for $n$ a [[natural number]], and we pretend that $k$ is a positive number such that $k^n/{n!}$ is always a natural number (which of course is impossible).

All of these justify the rules for the exponentials, so again we see that there may be many ways to satisfy these rules.


## References

*  Blass, Andreas, 'A game semantics for linear logic'.  _Annals of Pure and Applied Logic_ 56: 183--220, 1992.
{#Blass}

*  Girard, Jean-Yves, 'Linear logic'.  _Theoretical Computer
   Science_ 50:1, 1987.  Available in [PDF](http://iml.univ-mrs.fr/~girard/linear.pdf).
{#Girard}

*  Seely, R. A. G., 'Linear logic, $*$-autonomous categories
   and cofree coalgebras', _Contemporary Mathematics_ 92,
   1989.  Available in [PostScript](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz).
{#Seely}

*  The [article](https://secure.wikimedia.org/wikipedia/en/wiki/Linear_logic) on the English Wikipedia has good summaries of the meanings of the logical operators and of the commonly studied fragments.


[[!redirects linear logic]]
[[!redirects linear logics]]
