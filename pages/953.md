Waldhausen in his work in K-theory introduced the notion of a category with cofibration and weak equivalences, nowdays known as _Waldhausen category_. As the original name suggests, this is a category $C$ with zero object $0$, equipped with a choice of two classes of maps $\mathrm{cof}$ of the cofibrations and $w.e.$ of weak equivalences such that

(C1) all isomorphisms are cofibrations

(C2) there is a zero object $0$ and for any object $a$ the unique morphism $O\to a$ is a cofibration

(C3) if $a\hookrightarrow b$ is a cofibration and $d\to b$ any morphism than the pushout $d\to a\cup_b d$ is a cofibration

(W1) all isomorphisms are weak equivalences

(W2) weak equivalences are closed under composition (make a subcategory)

(W3) "glueing for weak equivalences": Given any commutative diagram of the form 
$$\array{
D &\leftarrow& A &\hookrightarrow &B\\
\downarrow^\sim&& \downarrow^\sim &&\downarrow^\sim\\
D' &\leftarrow &A' &\hookrightarrow &B'
}$$
in which the vertical arrows are weak equivalences and right horizontal maps cofibrations, the induced map
$B\cup_A D\hookrightarrow B'\cup_{A'} D'$
is a weak equivalence. 

The axioms imply that for any cofibration $A\hookrightarrow B$ there is a cofibration sequence $A\hookrightarrow B\to B/A$ where $B/A$ is the choice of the cokernel $B\cup_A 0$.

Given a Waldhausen category $C$ whose weak equivalence classes from a set, one defines $K_0(C)$ as an abelian group whose elements are the weak equivalence classes modulo the relation $[A]+[B/A]=[B]$ for any cofibraton sequence $A\hookrightarrow B\to B/A$.

Waldhausen then devises so called S-construction $C\mapsto S_\bullet C$ from Waldhausen categories to simplicial categories with cofibrations and weak equivalence (hence one can iterate the construction producing multisimplicial categories). 

The [[K-theory space]] of a Waldhausen construction is 
given by formula $\Omega\mathrm{hocolim}_{\Delta^{\mathrm{op}}}([n]\mapsto N_\bullet(w.e.(S_n C)))$, where $\Omega$ is the loop space functor, $N$ is the simplicial nerve, w.e. takes the (simplicial) subcategory of weak equivalence and $[n]\in\Delta$. This construction can be improved (using iterated $S$-construction) to the K-theory $\Omega$-spectrum of $C$; the K-theory space will be just the one-space of the K-theory spectrum. 

Then the K-groups are the homotopy groups of the K-theory space.

#Remarks#

* The axioms of a Waldhausen category $C$ are very similar to the axioms of a [[category of fibrant objects]] on the [[opposite category]] $C^{op}$ in which the initial object is also terminal. The difference is in axiom W3, whose analog in a [[category of fibrant objects]] is the axioms that every object has a [[path object]]. It still follows that one has fibration sequences in a [[category of fibrant objects]].