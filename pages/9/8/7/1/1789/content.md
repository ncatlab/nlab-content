A _&#268;ech cover_ is a [[Cech nerve|Čech nerve]] $C(U)$ that comes from a [[cover]] $U \to X$.

# Definition #

Let $C$ be a [[site]] and $\{U_i \to X\}$ a covering [[sieve]]. Write $U = \sqcup_i Y(U_i)$ for the [[coproduct]] of the patches in the [[presheaf]] category $PSh(C)$ ($Y$ is the [[Yoneda embedding]]). 

Write $X$ for $Y(X)$, for short.

Then the [[Cech nerve|Čech nerve]] $C(U)$ of $U \to X$ in $PSh(C)$, i.e. the [[simplicial presheaf]]

$$
  \cdots
  U \times_X U \times_X U
  \stackrel{\stackrel{\to}{\to}}{\to}
  U \times_X U \stackrel{\to}{\to} U
$$

is called a **&#268;ech cover**.

#Properties#

Consider the [[local model structure on simplicial presheaves]] on $C$. If the [[sheaf]] [[topos]] $Sh(C)$ has [[point of a topos|enough points]], then the weak equivalences (called local weak equivalences for emphasis) are the [[stalk]]-wise weak equivalences of [[simplicial set ]] (with respect to the standard [[model structure on simplicial sets]]).

+-- {: .un_defn}
###### Definition

Write

$$
  \pi_0(C(U)) = colim_{[n] \in \Delta^{op}} C(U)_n
$$

for the presheaf of connected components (see [[simplicial homotopy group]]) of $C(U)$. Regard this as a simplicially constant [[simplicial presheaf]].

=--

**Remark**. By the discussion in the section "Interpretation in terms of descent and codescent" at [[sieve]] this $\pi_0(C(U))$, regarded as an ordinary presheaf, is precisely the subfunctor of $Y(X)$ that corresponds to the [[sieve]] $\{U_i \to X\}$.

+-- {: .un_lemma }
###### Lemma

For every &#268;ech cover $C(U)$ the morphism of simplicial presheaves

$$
  C(U) \to \pi_0(C(U))
$$

is a local weak equivalence.

=--

+-- {: .proof}
###### Proof

Being a simplicially discrete simplicial sheaf, for every test object $V$ $\pi_0(C(U))(V)$ has all [[simplicial homotopy group]]s trivial except possibly the set of connected components.
But by the very definition of $\pi_0(C(U))$ the morphism 
$C(U) \to \pi_0(C(U))$ is a bijection on $\pi_0$.

Over each test domain $V$ the [[simplicial set]]
$C(U)(V)$ is just the [[nerve]] of the [[Cech groupoid]]
$$
   \left(
     C(V,U)\times_{C(V,U \times_X U)}
     \stackrel{\to}{\to}
     C(V,U)
   \right)
  \,.
$$
The nerve of that groupoid is readily seen to have vanishing first [[simplicial homotopy group]]. Being the [[nerve]] of a 1-[[groupoid]], also all higher [[simplicial homotopy group]]s vanish. 

So $C(U) \to \pi_0(C(U))$ induces for each object $V \in C$ an isomorphism of [[simplicial homotopy group]]s. It therefore is an objectwise weak equivalence of simplicial sets.

See also for instance lemma 3.3.5 in

* Daniel Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))


=--


+-- {: .un_prop}
###### Proposition

Every Cech cover 

$$
  C(U) \to X
$$

is a stalkwise weak equivalence.

=--
 
+-- {: .proof}
###### Proof

From the above we know that $C(U) \to X$ factors as

$$
  C(U) \to \pi_0(C(U)) \to X
$$

and that the first morphism is an objectwise, hence also a [[stalk]]wise weak equivalence. It therefore suffices to show that $\pi_0(C(U)) \to X$ is a stalkwise weak equivalence.

But by the remark above, $\pi_0(C(U)) \to X$ is actually the [[local isomorphism]] corresponding to the [[cover]] $U$. It is therefore even a [[stalk]]wise [[isomorphism]].

See also for instance lemma 3.4.9 in

* Daniel Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

=--

**Remark**. So this says that every &#268;ech cover is a [[hypercover]]. But not conversely. [[localization|Localization]] of [[simplicial presheaf|simplicial presheaves]] at &#268;ech covers yieds [[Čech cohomology]]. 


[[!redirects Čech cover]]
[[!redirects Čech covers]]
[[!redirects Cech covers]]