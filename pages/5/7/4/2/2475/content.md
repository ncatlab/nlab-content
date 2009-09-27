The goal of this page is to prove that a non-extensional choice operator is conservative over a theory without AC.  I'll take the theory without AC to be [[SEAR]], for definiteness and since that's where [[Mike Shulman|I'm]] most comfortable.

# Defining SEAR+$\epsilon$

For the theory with a non-extensional choice operator, consider the following theory, which is a variant of the version of SEAR without fundamental equality described at [[SEAR]].  There are four basic sorts: *pre-sets*, *pre-relations*, *elements*, and *operations* (or *pre-functions*).  Each element belongs to a pre-set, and each pre-relation and operation has a source and target which are pre-sets.  For a prerelation $\phi:A\looparrowright B$ and $x\in A$, $y\in B$, we have the assertion $\phi(x,y)$, and for an operation $f:A\rightsquigarrow B$ and $x\in A$ we have an element $f(x)\in B$.  There is no predefined notion of equality of anything.   Axioms 0 and 1 of SEAR are unmodified, except that the uniqueness clause of the latter is interpreted as a *definition* of when two parallel pre-relations are called "equal".  We also impose

**Axiom $1+\epsilon$ (Choice operator):** _If $\varphi:A\looparrowright B$ is a pre-relation such that for every $x\in A$ there exists a $y\in B$ with $\varphi(x,y)$, then there exists an operation $\epsilon_\varphi :A\rightsquigarrow B$ such that $\varphi(x,\epsilon_\varphi(x))$ for all $x\in A$._

A *set* is defined to be a pre-set $A$ equipped with an equivalence pre-relation $=_A$.  A *relation* between sets is a pre-relation which is *extensional*, i.e. if $\varphi(x,y)$, $x'=_A x$, and $y'=_B y$, then $\varphi(x',y')$.  Likewise, a *function* $f:A\to B$ between sets is an operation $f:A\rightsquigarrow B$ which is extensional, i.e. if $x' =_A x$ then $f(x')=_B f(x)$.  We define two functions $f,g:A\to B$ to be *equal* if $f(x)=_B g(x)$ for all $x\in A$.  Note that we have no notion of equality for arbitrary operations between pre-sets.

Note that for any operation $f:A\rightsquigarrow B$ between *sets*, we have a pre-relation (its *graph*) defined by $\Gamma_f(x,y) \Leftrightarrow (f(x)=_B y)$, which is *[[entire relation|entire]]* in the sense that for any $x\in A$, there is a $y\in B$ with $\Gamma_f(x,y)$.  This pre-relation is extensional in $y$, but not in $x$ unless $f$ is actually a function (in which case $\Gamma_f$ is a *[[functional relation]]* in the usual sense).  Conversely, Axiom $1\frac12$ says that any entire pre-relation induces an operation, and for an entire and functional relation between sets, this induced operation is a function (and is unique, in the sense of equality of functions defined above).

Now Axiom 2 can be taken to read: For any sets $A,B$ and any relation $\varphi:A\looparrowright B$, there exists a pre-set $|\varphi|$ and operations $p:{|\varphi|}\rightsquigarrow A$ and $q:{|\varphi|}\rightsquigarrow B$ such that $\varphi(x,y)$ iff there exists $z\in {|\varphi|}$ with $p(z)=_A x$ and $q(z)=_B y$.  We can then define $z=_{|\varphi|} z'$ iff $p(z)=_A p(z')$ and $q(z)=_B q(z')$ to make $|\varphi|$ into a set and $p,q$ into functions that are jointly injective.  Axioms 3, 4, and 5 are easy to translate.

We call this theory $SEAR+\epsilon$.  Clearly the sets, elements (with defined equality), and relations in any model of $SEAR+\epsilon$ satisfy the axioms of SEAR.  Conversely, from any model of SEAR-C we can construct a model of $SEAR+\epsilon$ by taking the pre-sets, pre-relations, and operations to be the SEAR-C sets, relations, and functions respectively.  The question is whether we can get $SEAR+\epsilon$ without assuming or implying choice.


# Conservativity over COSHEP

Our goal is to prove that $SEAR+\epsilon$ is conservative over SEAR. 
But since I haven't quite figured out how to do that (or, to be fair, even whether it's true), as a warm-up let's prove that the same thing is true when we add [[COSHEP]], a choice-like axiom notably weaker than full AC, to both sides.

(to be continued...)

[[!redirects SEAR+ε]]
