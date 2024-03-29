
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Quite generally, one says that an [[object]] $A$ in a [[category]] or [[higher category theory|higher category]] $\mathcal{C}$ satisfies _[[descent]]_ along a given [[morphism]] $p : \hat X \to X$ in $\mathcal{C}$ if it is a _$p$-[[local object]]_, hence if the induced map -- the _[[descent morphism]]_

$$
  \mathcal{C}(X, A) \to \mathcal{C}(\hat X, A)
$$

is an [[equivalence]]. We may read this as saying that every collection of $A$-data on $\hat X$ "[[descent|descends]]" down along $p$ to $X$.

In the context the [[hom object]] $\mathcal{C}(\hat X, A)$ is also called the **descent object**.

While roughly synonyms, typically one speaks of "descent" instead of [[local objects|locality]] when $\mathcal{C}$ is a category of [[presheaves]] or higher presheaves ([[(2,1)-presheaves]], [[(∞,1)-presheaves]], [[(∞,n)-presheaves]]).

In this case, in turn, the objects $X$ above are typically [[representables]] of a given [[site]] (or higher site) and $\hat X$ is either the [[Cech nerve]]  of a [[covering]] family with respect to a chosen [[coverage]]/[[Grothendieck topology]], or is the [[colimit]] of this &#268;ech nerve: the corresponding [[sieve]] (the _[[codescent object]]_). 

The [[descent]] condition then says that the presheaf $X$ satisfies the [[sheaf]]-condition ([[stack]]-condition, [[(∞,1)-sheaf]]/[[∞-stack]]-condition, etc.) for this given covering family.

Whether one takes $\hat X$ to be the [[Cech nerve]] or the corresponding [[sieve]] depends on [[homotopy theory|homotopical]] details of the setup. If $\mathcal{C}$ is taken to be an [[(∞,1)-category]], then it typically does not matter. But if $\mathcal{C}$ is instead just a [[homotopical category]] presenting the desired higher category, then $\hat X$ needs to satisfy some extra conditions (such as [[cofibrant object|cofibrancy]]) to ensure that $\mathcal{C}(\hat X, A)$ is indeed the correct descent object, and not too small.

For instance when working with the [[model structure on functors|injective]] [[model structure on simplicial presheaves]], every object is cofibrant and we can take $\hat X$ to be the [[sieve]]. But when working with the projective model structure then (as discussed there) $\hat X$ needs to be [[split hypercover|split]], which means that we need to use the [[Cech nerve]] and even ensure that the corresponding [[covering family]] behaves like a [[good cover]] (or, more generally, form a [[split hypercover]]).



## Details

### For ordinary presheaves
 {#ForPresheaves}

For ordinary [[presheaves]], a descent object is a set of _[[matching families]]_

More in detail, let $C$ be a [[site]], let $X \in C$ be an object, $\{U_i \to X\}$ a [[covering]] family and $S(\{U_i\}) \hookrightarrow X$ the corresponding [[sieve]]. 

Then for $A : C^{op} \to Set$ any [[presheaf]] on $C$, the descent object with respect to this covering is the [[hom set]]

$$
  Desc(\{U_i\}, A) = PSh(S(\{U_i\}), A)
  \,.
$$

This is discussed in detail at [[sheaf]], so just briefly: 

the [[sieve]] may be realized as the [[coequalizer]]

$$
  \coprod_{i, j} U_i \cap U_j \stackrel{\to}{\to}
  \coprod_i U_i \to S(\{U_i\})
  \,.
$$

Accordingly the hom out of this realizes the descent object as the [[equalizer]]

$$
  Desc(\{U_i\}, A) \to 
  \prod_{i} A(U_i)
  \stackrel{\to}{\to}
  \prod_{i, j} A(U_i \cap U_j)
  \,.
$$

Writing this out in components shows that this is the set of [[matching families]].

If the [[descent morphism]]

$$
  [C^{op}, Set](X, A) \to Desc(\{U_i\}, A)
$$

is an [[isomorphism]] one says that $A$ satisfies the [[sheaf]]-condition with respect to the [[cover]] $\{U_i \to X\}$. If this morphism is only a [[monomorphism]] one says that $A$ satisfies the [[separated presheaf]]-condition.


### For groupoid valued presheaves / pseudofunctors
 {#ForGroupoidValuedPresheaves}

For $A : C^{op} \to $ [[Grpd]] a [[2-functor]] (hence a "[[pseudofunctor]]" if $C$ is an ordinary [[category]] regarded as a [[2-category]]) and for $\hat X \to X$ a [[covering]] morphism in $C$, the descent object now is a [[groupoid]] 

$$
  Desc(\hat X, A) := [C^{op}, Grpd](\hat X, A) \in Grpd
  \,.
$$ 

If the [[descent morphism]]

$$
  [C^{op}, Grpd](X, A) \to Desc(\hat X, A)
$$ 

is an [[equivalence of groupoids]], one says that $A$ satisfies the _[[(2,1)-sheaf]]_- or _[[stack]]_-condition with respect to the [[cover]] $\hat X \to X$. If it is just a [[full and faithful functor]], one says (sometimes) that $A$ satisfies the condition for a _[[separated prestack]]_ with respect to this cover.

Similar statements hold for the case of 2-functors with values in [[Cat]]. Here one also often talks about a _[[stack]]-condition_, though less ambiguous would be to speak of _[[2-sheaf]]-conditions_.

By the [[Grothendieck construction]] one may identify pseudofunctors $C^{op} \to Cat$ equivalently with [[fibered categories]] (or just [[categories fibered in groupoids]] for $C^{op} \to Grpd$) over $C$, and all of the above has analogs in this dual description.


### For simplicial presheaves

See _[[descent]]_.

### For strict $\omega$-category-valued presheaves

In ([Street](#Street)) a proposal for a definition of descent objects for presehaves with values in [[strict ∞-categories]] was proposed. Additional homotopical conditions to ensure that this gives the right answer were discussed in ([Verity](#Verity)).

+-- {: .num_defn}
###### Definition
Let $C$ be a category, let $E_1\stackrel{\stackrel{d_1}{\to}}{\stackrel{d_0}{\to}}E_0\xrightarrow{p}B$ be morphisms where the parallel arrows $\mathcal{E}:=\{d_0,d_1:E_1\to E_0\}$ are seen as _a_ diagram, let $X\in C_0$ be an object.

Applying the functor $C(-,X)$ to this sequence gives

$$C(E_1,X)\xleftarrow{C(d_0,X),C(d_1,X)}C(E_0,X)\xleftarrow{C(p,X)}C(B,X)$$

If this diagram is for all $X\in C_0$ an equalizer diagram $B$ is called **codescent object for** the diagram $\mathcal{E}$. 

=--

+-- {: .num_defn}
###### Definition
Let $E_0\to\E_1\to E_2$ be a diagram where $E_0\xrightarrow{\partial_0}E_1\xrightarrow{\partial_0}E_2$, $E_0\xleftarrow{\iota_0}E_1\xrightarrow{\partial_1}E_2$, $E_0\xrightarrow{\partial_1}E_1\xrightarrow{\partial_2}E_2$ satisfying $\partial_s\partial_r=\partial_r\partial_{s-1}$ for $r\lt s$ and $\iota_0\partial_0=\iota_0\partial_1$ (these are the identities characterizing a truncated cosimplicial category).

Then the **descent category** $\Desc E$ of $E$ has as objects pairs $(F,f)$ where $F\in E_0$, $f:\partial_1 F\to \partial_0 F$ such that $\iota_0 f=\id_F$ and $\partial_0 f=\partial_2( f)\circ \partial_0 (f)$ and a morphism $(F,f)\to (G,g)$ consists of a morphism $(u:F\to G)\in E_1$ such that $\partial_0 u\circ f=g\circ \partial_1 u$.
=--

+-- {: .num_instance}
###### Instance
Let $A$, $X$ be categories.

Then $\Desc [N(A),X]\cong[A,X]$
=--

## Related concepts

See also _[[descent]]_ and [[category of descent data]]. 

Discussion related to the computation of descent objects is also at _[[model structure on cosimplicial simplicial sets]]_.

## References

See also the references at [[descent]].

A definition of descent objects for presheaves with values in strict $\omega$-categories was proposed in 

* [[Ross Street]], [Categorical and combinatorial aspects of descent theory](http://arxiv.org/pdf/math/0303175)
  {#Street}

A discussion of a missing condition on this definition is in 

* [[Dominic Verity]], _Relating descent notions_ ([pdf](http://ncatlab.org/nlab/files/VerityDescent.pdf) [[Verity on descent for strict omega-groupoid valued presheaves|nLab]])
  {#Verity} 

[[!redirects descent objects]]

[[!redirects descent data]]