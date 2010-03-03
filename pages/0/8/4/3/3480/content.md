
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

[[Tannaka]] duality or _Tannaka [[reconstruction theorem]]s_ are statements of the form:

for $A$ some algebraic structure, [[representation|represented]] on objects in a category $D$, one may _reconstruct_ $A$ from knowledge of the [[endomorphism]]s of the forgetful functor -- the **fiber functor** --

$$
  F : Rep_D(A) \to D
$$

from the [[category]] $Rep_D(A)$ of [[representation]]s of $A$ on objects of $D$ that remembers these underlying objects.

## For permutation representations 

A simple case of Tannaka duality is that of [[permutation representation]]s of a [[group]], i.e. representations on a [[set]]. In this case, Tannaka duality follows entirely from repeated application of the [[Yoneda lemma]].


+-- {: .un_theorem}
###### Theorem
**(Tannaka duality for permutation representations)**

Let $G$ be a [[group]], $Rep_{Set}(G)$ the category of its [[permutation representation]]s and $F : Rep_{Set}(G) \to Set$ the forgetful functor that sends a representation to its underlying set.

Then there is a canonical [[isomorphism]] of [[group]]s

$$
  Aut(F) \simeq G
  \,.
$$

Here $Aut(F)$ denotes the group of invertbile [[natural transformation]]s from $F$ to itself.

=--

+-- {: .proof}
###### Quick Proof


With a bit of evident abuse of notation, the proof is a one-line sequence of applications of the [[Yoneda lemma]]: we show $End(F) \cong G$, i.e., each endomorphism on $F$ is invertible, so $End(F) = Aut(F) \cong G$.  

Write $C := Set^G = Rep_{Set}(G)$.
Observe that the functor $F : C \to Set$ is the [[representable functor|representable]] $F = C(G, -)$. Then the argument is 

$$
  End(F)
  =
  Set^C(F, F) 
    \cong 
  Set^C(C(G, -), C(G, -)) 
    \cong 
  C(G, G) 
   \cong 
  G.
$$

The "$G$" here is used in multiple senses, but each sense is deducible from context.

=--

+-- {: .proof}
###### Long-winded Proof

 
Let $\mathbf{B}G$ be the [[delooping]] [[groupoid]]. Then 

$$
  Rep_{Set}(G) := Func(\mathbf{B}G^{op}, Set)
  \,.
$$

The canonical inclusion $i : {*} \to \mathbf{B}G$ induces the fiber functor

$$
  Func(i,Set) : Rep_{Set}(G) \to Set
$$

which evaluates a functor $\rho : \mathbf{B}G^{op} \to Set$ on the unique object of $\mathbf{B}G$. By the [[Yoneda lemma]] this is the same as homming out of the functor [[representable functor|represented by]] that unique object

$$
  Func(i,Set) = Hom_{PSh(\mathbf{B}G)}(Y_{\mathbf{B}G}) {*}, -)
  \,,
$$

where $Y_{\mathbf{B}G} : \mathbf{B}G \to PSh(\mathbf{B}G)$ is the [[Yoneda embedding]].

But this way we see that $Func(i,Set) : PSh(\mathbf{B}G) \to Set$  is itself a representable functor in the presheaf category $PSh(PSh(\mathbf{B}G)^{op})$

$$
  Func(i,Set) = Y_{\mathbf{PSh(\mathbf{B}G)^{op}}} Y_{\mathbf{B}G} *
  \,.
$$

So applying the [[Yoneda lemma]] twice, we find that

$$
  \begin{aligned}
    Aut_{PSh(PSh(\mathbf{B}G)^{op})} Func(i,Set)
    & =
    Aut_{PSh(PSh(\mathbf{B}G)^{op})} Y_{\mathbf{PSh(\mathbf{B}G)^{op}}} Y_{\mathbf{B}G} *
    \\
    & \simeq
    Aut_{PSh(\mathbf{B}G)^{op})} Y_{\mathbf{B}G} *
    \\
    & \simeq
    Aut_{\mathbf{B}G} *
    \\
    & \simeq G
    \,.
  \end{aligned}
$$

=--
## References

* [[André Joyal]], [[Ross Street]], _An introduction to Tannaka duality and quantum groups_, [pdf](http://www.math.mq.edu.au/~street/CT90Como.pdf)

* Pierre Deligne, [[Catégories Tannakiennes]]

The following paper shortens the Deligne's proof 

* [[Alexander Rosenberg|Alexander L. Rosenberg]],  _The existence of fiber functors_,  The Gelfand Mathematical Seminars, 1996--1999,  145--154, Birkh&#228;user, Boston 2000.

Ulbrich made a major contribution at the coalgebra and Hopf algebra level

* K-H. Ulbrich, _On Hopf algebras and rigid monoidal categories_, in special volume, Hopf algebras, Israel J. Math. 72 (1990), no. 1-2, 252--256. 

A generalization of several classical reconstruction theorems with nontrivial [[functional analysis]] is in 

* [[Alexander Rosenberg|Alexander L. Rosenberg]],  _Reconstruction of groups_, Selecta Math. (N.S.) __9__, 1 (2003), 101--118, [doi](http://dx.doi.org/10.1007/s00029-003-0322-x).

Categorically oriented notes were written also by Pareigis, emphasising on using [[coend|Coend]] in dual picture. His works can be found [here](http://www.mathematik.uni-muenchen.de/~pareigis/pa_schft.html) but the most important is the chapter 3 of his online book

* Bodo Pareigis, _Quantum groups and noncommutative geometry_, Chapter 3: Representation theory, reconstruction and Tannaka duality, [pdf](http://www.mathematik.uni-muenchen.de/~pareigis/Vorlesungen/98SS/Quantum_Groups/LN3.PDF)

A very neat Tannaka theorem for stacks is proved in

* [[Jacob Lurie]], _Tannaka duality for geometric stacks_, [math.AG/0412266](http://arxiv.org/abs/math/0412266)

See also talk 

* B. Toen, [Higher Tannaka duality](http://www.msri.org/publications/ln/msri/2002/hodgetheory/toen/2/index.html), MSRI 2002 (video)

[[!redirects Tannaka reconstruction]]