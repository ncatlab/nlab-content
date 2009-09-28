The goal of this page is to prove that a non-extensional [[choice operator]] is conservative over a theory without AC.  I'll take the theory without AC to be [[SEAR]], for definiteness and since that's where [[Mike Shulman|I'm]] most comfortable.


# Defining SEAR+$\epsilon$

For the theory with a non-extensional choice operator, consider the following theory, which is a variant of the version of SEAR without fundamental equality described at [[SEAR]].  There are four basic sorts: *pre-sets*, *pre-relations*, *elements*, and *operations* (or *pre-functions*).  Each element belongs to a pre-set, and each pre-relation and operation has a source and target which are pre-sets.  For a prerelation $\phi:A\looparrowright B$ and $x\in A$, $y\in B$, we have the assertion $\phi(x,y)$, and for an operation $f:A\rightsquigarrow B$ and $x\in A$ we have an element $f(x)\in B$.  There is no predefined notion of equality of anything.   Axioms 0 and 1 of SEAR are unmodified, except that the uniqueness clause of the latter is interpreted as a *definition* of when two parallel pre-relations are called "equal".  We also impose

**Axiom $1+\epsilon$ (Choice operator):** _If $\varphi:A\looparrowright B$ is a pre-relation such that for every $x\in A$ there exists a $y\in B$ with $\varphi(x,y)$, then there exists an operation $\epsilon_\varphi :A\rightsquigarrow B$ such that $\varphi(x,\epsilon_\varphi(x))$ for all $x\in A$._

A *set* is defined to be a pre-set $A$ equipped with an equivalence pre-relation $=_A$.  A *relation* between sets is a pre-relation which is *extensional*, i.e. if $\varphi(x,y)$, $x'=_A x$, and $y'=_B y$, then $\varphi(x',y')$.  Likewise, a *function* $f:A\to B$ between sets is an operation $f:A\rightsquigarrow B$ which is extensional, i.e. if $x' =_A x$ then $f(x')=_B f(x)$.  We define two functions $f,g:A\to B$ to be *equal* if $f(x)=_B g(x)$ for all $x\in A$.  Note that we have no notion of equality for arbitrary operations between pre-sets.

For any operation $f:A\rightsquigarrow B$ between *sets*, we have a pre-relation (its *graph*) defined by $\Gamma_f(x,y) \Leftrightarrow (f(x)=_B y)$, which is *[[entire relation|entire]]* in the sense that for any $x\in A$, there is a $y\in B$ with $\Gamma_f(x,y)$.  This pre-relation is extensional in $y$, but not in $x$ unless $f$ is actually a function (in which case $\Gamma_f$ is a *[[functional relation]]* in the usual sense).  Conversely, Axiom $1+\epsilon$ says that any entire pre-relation induces an operation, and for an entire and functional relation between sets, this induced operation is a function (and is unique, in the sense of equality of functions defined above).

Now Axiom 2 can be taken to read: For any sets $A,B$ and any relation $\varphi:A\looparrowright B$, there exists a pre-set $|\varphi|$ and operations $p:{|\varphi|}\rightsquigarrow A$ and $q:{|\varphi|}\rightsquigarrow B$ such that $\varphi(x,y)$ iff there exists $z\in {|\varphi|}$ with $p(z)=_A x$ and $q(z)=_B y$.  We can then define $z=_{|\varphi|} z'$ iff $p(z)=_A p(z')$ and $q(z)=_B q(z')$ to make $|\varphi|$ into a set and $p,q$ into functions that are jointly injective.  Axioms 3, 4, and 5 are easy to translate.

We call this theory $SEAR+\epsilon$.  Clearly the sets, elements (with defined equality), and relations in any model of $SEAR+\epsilon$ satisfy the axioms of SEAR.  Conversely, from any model of SEAR-C we can construct a model of $SEAR+\epsilon$ by taking the pre-sets, pre-relations, and operations to be the SEAR-C sets, relations, and functions respectively.  With this interpretation axiom $1+\epsilon$ is precisely the SEAR-C [[axiom of choice]].  The question is whether we can get $SEAR+\epsilon$ without assuming or implying choice.


# Conservativity over COSHEP

Our goal is to prove that $SEAR+\epsilon$ is conservative over SEAR. 
But since I haven't quite figured out how to do that (or, to be fair, even whether it's true), as a warm-up let's prove that the same thing is true when we add [[COSHEP]], a choice-like axiom notably weaker than full AC, to both sides.

Suppose we have a model of SEAR satisfying COSHEP, call it $V$. Recall that COSHEP means that in $V$, every set admits a surjection from a [[projective object|projective]] one.  We define a model of $SEAR+\epsilon$ as follows.

* The pre-sets are the projective $V$-sets.
* The elements are the $V$-elements.
* The pre-relations are the $V$-relations.
* The operations are the $V$-functions.

We will continue to qualify the notions in the old model $V$, using unqualified words such as "set" for the new notions defined above.

Axiom 0 of $SEAR+\epsilon$ is obviously true.  For Axiom 1, we need to translate a first-order formula in the language of $SEAR+\epsilon$ into a formula in the language of SEAR in order to apply Axiom 1 of $V$, but the above dictionary tells us exactly how to do that.  Axiom $1+\epsilon$ is true because we have chosen the pre-sets to be the *projective* sets in $V$, so any entire $V$-relation between them contains a $V$-function.

Now a *set* $A$ in our putative model of $SEAR+\epsilon$ is a $V$-set equipped with an equivalence relation $=_A$, so in particular it has a quotient $A/{=_A}$.  Now any *relation* $A\looparrowright B$, meaning extensional relation, induces a $V$-relation $(A/{=_A}) \looparrowright (B/{=_B})$, and conversely any such $V$-relation induces a relation $A\looparrowright B$, setting up a meta-bijection.  The same is true of functions $A\to B$ and $V$-functions $(A/{=_A}) \to (B/{=_B})$.  It follows that we have meta-functors $Set\to Set_V$ and $Rel\to Rel_V$ given by "take quotients" that are [[full and faithful functor|fully faithful]].

I claim that in fact these functors are [[essentially surjective functor|essentially surjective]] as well.  For given any $V$-set $A$, by COSHEP there is a projective set $P$ and a surjection $e:P\to A$. Since $Set_V$ is a [[regular category]], it follows that $A$ is the [[quotient set]] of the [[kernel pair]] of $e$.  But that means that if we call this kernel pair $=_P$, then $P$ becomes a new-style set which maps onto $A$ under the quotient functor; hence this functor is essentially surjective.

It follows that the meta-categories $Set$ and $Rel$ (in the new sense) are [[equivalence of categories|equivalent]] to the old meta-categories $Set_V$ and $Rel_V$.  Since the remaining axioms of SEAR are essentially just statements about these categories, their truth in the "new world" follows immediately from their truth in $V$.  (There's no need to worry about a meta-axiom-of-choice, since these axioms are just statements about finite numbers of objects and morphisms, so "fully faithful and essentially surjective" is a perfectly sufficient notion of "equivalence.")

Thus, we have constructed a model of $SEAR+\epsilon$.  Furthermore, its underlying SEAR-model is equivalent to $V$.  (The notion of "equivalence" here means "(weak) equivalence of categories of sets," as above.  But since SEAR speaks no [[evil]], this suffices to show that exactly the same first-order statements are true in both.)  It follows that the statements *in the language of SEAR* which are true in this new model of $SEAR+\epsilon$ are precisely those which are true in $V$.

Therefore, any statement in the language of SEAR which is true in all models of SEAR that underlie models of $SEAR+\epsilon$ is, in fact, true in *all* models of SEAR+COSHEP.  This is the conservativity result we were looking for.  Its practical upshot is that if you want to work in SEAR+COSHEP, you might as well work in $SEAR+\epsilon$ if it's more convenient to have a choice operator, since the theorems you can prove in either case will be exactly the same.

Note that the model of $SEAR+\epsilon$ we've just constructed also satisfies COSHEP (as it must, given its equivalence to $V$).  In fact, if a model of $SEAR+\epsilon$ admits an "identity" equivalence pre-relation $\equiv_A$ on every pre-set, and relative to which all pre-relations and operations are extensional, then it must satisfy COSHEP---for then every set $(A,{=_A})$ is the surjective image of the set $(A,{\equiv_A})$, which is projective by Axiom $1+\epsilon$.


# Without COSHEP

Now [[Toby Bartels|I]] step in to say: $\mathbf{SEAR} + \epsilon \vDash COSHEP$.

The reason is that every preset *does* admit an identity prerelation as in the last paragraph above; let $x \equiv_A y$ if $x \sim_R y$ for every reflexive prerelation $R: A \looparrowright A$ (or even for every equivalence prerelation).  This will work also in $\mathbf{ETCS} + \epsilon$ by quantifying over prefunctions $f: A \to \mathcal{P}1$ and using the kernel of $f$ (relative to the standard equality on truth values) as the equivalence relation.  (Of course, $\mathbf{SEAR}$ is capable of using this method too.)  It will still work in versions with intuitionistic logic, but not (as far as I can see) in $\mathbf{CETCS} + \epsilon$ (following [Palmgren](http://www.math.uu.se/~palmgren/cetcs.pdf)), where one cannot take power sets or quantify over subsets.


[[!redirects SEAR+ε]]
[[!redirects SEAR+ϵ]]
