##Idea##

A [[coalgebra]] is half of the structure of a [[bialgebra]]. A bialgebra with antipode is a [[Hopf algebra]], and morally a "Hopf algebra without counit" is essentially a [[quantum heap]]. 
So a cop should be "half way toward a quantum heap".


##Definitions##

Let $(A,\otimes,1)$, or $A$ for short,
be a [[strict monoidal category]] with unit object $1$.
A __cop__ $C$ in $(A,\otimes, 1)$ is a pair
$(C,\tau)$, where $C$ is an object in $A$
and $\tau : C \rightarrow C \otimes C \otimes C$
is a morphism in $A$ satisfying the law
\begin{equation} \label{law}
(\id \otimes \id \otimes \tau) \circ \tau =
  (\tau \otimes \id \otimes \id) \circ \tau.
\end{equation}
Let $(A,\otimes,1,\sigma)$ be a strict [[symmetric monoidal
category]] and $C$ a [[monoid object|monoid (= algebra) object]] in that category, i.e.
$C$ is equipped with a product $\mu : C \otimes C \rightarrow C$
and a unit morphism $\eta : 1 \rightarrow C$ satisfying the
standard axioms.
Then an _opposite monoid_ $C_{op}$ (lower index as it is on the monoid side and upper index is for the comonoid-side duality here) is the same object $C$
equipped with product $\sigma_{C,C} \circ \mu$ and
with the same unit map $\eta$.

A __symmetric cop monoid__ $C$ in
a strict symmetric monoidal category $(A,\otimes,1,\sigma)$
is a _monoid_ object $C$ with a _morphism of monoids_
$\tau : C \rightarrow C \otimes C_{op} \otimes C$
satisfying the law (eqref:law). Notice the passage to the opposite monoid in the second tensor factor (which does not make sense for usual cops in nonsymmetric monoidal categories). 
Here the tensor product has the usual tensor product
structure of a monoid in a strict symmetric monoidal category (for two monoids $C$ and $D$ one takes $(\mu \otimes \mu) \circ (\id \otimes \sigma_{D,C} \otimes \id)$ as a product on $C \otimes D$).

A __counit__ of a cop $C$ in $A$ is a morphism
$\epsilon : C \rightarrow 1$ such that
\begin{equation}
 (\id \otimes \epsilon \otimes \epsilon) \circ \tau = \id = (\epsilon
\otimes \epsilon \otimes \id) \circ \tau ,
\end{equation}
where the identification morphism
$1 \otimes 1 \otimes C \equiv C
\equiv C \otimes 1 \otimes 1$ is used.

A typical interest is in the cops in the (symmetric) monoidal category of [[vector space]]s $Vec_k$ or [[supervector space]]s $SVec_k$ over some fixed field $k$.

A __coheap monoid__ in a symmetric monoidal category is a
symmetric cop monoid such that
$(\id \otimes \mu)\circ \tau = (\mu\otimes \id)\circ\tau = \id$,
where the identification $C\otimes 1 = C = 1\otimes C$
is implicitly used. A __character__ of a monoid $(C,\mu,\eta)$ in a strict monoidal category
is a morphism $\epsilon : C \rightarrow {\bf 1}$ such that
$\epsilon \circ \eta = \id_1$ and
$(\epsilon \otimes \epsilon) = \epsilon \circ\mu$.

A __character of a symmetric cop monoid__ $C$
is any character of $(C,\eta,\mu)$ in $A$.

+-- {: .un_prop}
###### Proposition

A _character_ of a coheap monoid
is a automatically a counit of the underlying cop.
=--

+-- {: .proof}
###### Proof

This is straightforward:
$$\array{
(\id \otimes \epsilon\otimes \epsilon)\tau =
(\id\otimes (\epsilon\circ\mu))\tau =
(\id\otimes\epsilon)(\id\otimes\mu)\tau =
(\id\otimes\epsilon)(\id\otimes\eta) = \id,
\\
(\epsilon\otimes\epsilon\otimes\id)\tau =
((\epsilon\circ\mu)\circ\id)\tau = (\id\otimes\epsilon)(\mu\otimes\id)\tau =
(\epsilon\otimes\id)(\eta\otimes\id) = \id,
}$$
where obvious identifications are implicitly
used.
=--

A __copointed cop__ is a pair $(C,\epsilon)$
of a cop $C$ and a counit $\epsilon$ of $C$.
A __copointed coheap monoid__ is a coheap monoid with
a _character_ $\epsilon$ of $C$. Warning: a copointed cop which is also a coheap is not necessarily a copointed coheap, as the counit does not
need to be a character of a coheap. 


##Remarks##

* Clearly all this may be generalized to nonstrict [[monoidal categories]].

* About the language: the 'co' in 'cop' mimics the 'co' in 'coalgebra';
furthermore, in the dialect of Kent, according to the OED,
'cop' means _a small heap of hay or straw_. This way it is kind of coalgebra-like entity half way toward a (quantum) heap as in the idea section above.


##Literature##

* Zoran &#352;koda, _Quantum heaps, cops and heapy categories_, Mathematical Communications 12, No. 1, pp. 1-9 (2007); [math.QA/0701749](http://www.arxiv.org/abs/math.QA/0701749) 