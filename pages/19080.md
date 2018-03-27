# Internal tensor product of Hilbert C$^*$-modules
* table of contents
{: toc}

## Definition ##

The internal tensor product of Hilbert $C^*$-[[Hilbert C*-module|modules]] is a generalisation of the algebraic notion of a [[tensor product of modules]].

Let $A$ and $B$ be $C^*$-[[C*-algebra|algebras]], and let $E$ be a right Hilbert $A$-[[Hilbert C*-module|module]] and $F$ be a right Hilbert $B$-[[Hilbert C*-module|module]], and finally let $\varphi \colon A\to \mathcal{L}_B(F)$ be a $*$-homomorphism.

Form the algebraic tensor product $E \otimes_A F$ which is the quotient of the vector space tensor product $E\otimes F$ by the subspace $N$ spanned by elements of the form $ x a \otimes y - x \otimes \varphi(a)(y) $ for $a\in A, x\in E, y\in F$.  We define a $B$-valued inner product by
$$ \langle x_1\otimes y_1, x_2\otimes y_2 \rangle
= \langle y_1, \varphi(\langle x_1,x_2\rangle) y_2 \rangle. $$
It is easy to check that this respects the quotient by $N$.  Less obvious is:

+-- {: .num_lemma }
###### Lemma

If $z\in E\otimes F$ is such that $\langle z,z \rangle=0$ then $z\in N$.
=--

+-- {: .proof}
###### Proof

To do.
=--

It follows that we have a $B$-valued inner product on $E \otimes_A F$ which turns $E \otimes_A F$ into a Hilbert C$^*$-module over $B$, which is denoted by $E \otimes_\varphi F$.  This is the internal tensor product of $E$ and $F$ (using $\varphi$).


## Properties ##

### As a right $B$ module ###


### Action of adjointable operators on $E$ ###

To do.

## References ##

Lance's book, Chapter 4.