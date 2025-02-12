
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **Čech model structure on simplicial presheaves** on a [[site]] $C$ is a model for the [[topological localization]] of the [[(∞,1)-category of (∞,1)-presheaves]] on $C$ to the [[(∞,1)-category of (∞,1)-sheaves]]. 

It is obtained from the [[global model structure on simplicial presheaves]] on $C$ by the [[Bousfield localization of model categories|left Bousfield localization]] at [[Čech cover]]s:  its fibrant objects are [[∞-stack]]s that satisfy [[descent]] over [[Čech cover]]s but not necessarily over [[hypercover]]s.


Further [[Bousfield localization of model categories|left Bousfield localization]] at [[hypercover]]s leads from the Čech model structure to the Joyal-Jardine [[local model structure on simplicial presheaves]] that presents the [[hypercomplete (∞,1)-topos]] which is the [[hypercompletion]] of that presented by the Čech model structure.


## Definition

Let $C$ be a small [[site]] and write $[C^{op}, sSet]_{proj}$ and $[C^{op}, sSet]_{inj}$ for the projective and injective [[global model structure on simplicial presheaves]], respectively. 

For $\{U_i \to V\}_i$ a covering family in the [[site]] $C$, let

$$
  C(\{U_i\})
  :=
  \left(
    \cdots\stackrel{\to}{\stackrel{\to}{\to}}\coprod_{i j} U_{i j}\stackrel{\to}{\to}\coprod_i U_i
  \right)
$$

be the corresponding [[Cech nerve]], regarded as a [[simplicial presheaf]] on $C$. This comes canonically with a morphism

$$
  C(\{U_i\}) \to V
$$

of simplicial presheaves, the corresponding _&#268;ech cover morphism_ .

Notice that by the discussion at [model structure on simplicial presheaves - fibrant and cofibrant objects](http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#FibAndCofibObjects) this is a morphism between cofibrant objects.

+-- {: .un_defn}
###### Definition

The injective (projective) **Čech model structure on simplicial presheaves** $[C^{op},sSet]_{Cech}$ on $C$ is the [[Bousfield localization of model categories|left Bousfield localization]] of $[C^{op}, sSet]_{inj}$ ($[C^{op}, sSet]_{proj}$) at the set of &#268;ech cover morphisms.

=--

By the general properties of [[Bousfield localization of model categories|Bousfield localization]] this means that the fibrant-cofibrant objects $A$ of $[C^{op},sSet]_{Cech}$ are precisely those that are fibrant-cofibrant in the global model structure and in addition satisfy the [[descent]] condition that for all covers $\{U_i \to V\}$ the morphism of simplicial sets
$$
  A(V) \cong [C^op,sSet](V,A) \to [C^{op},sSet](C(\{U_i\}), A)
$$
is a weak equivalence in the standard [[model structure on simplicial sets]].

This is the model for the $\infty$-analog of the [[sheaf]] condition, modelling the [[topological localization]] of an $(\infty,1)$-presheaf $(\infty,1)$-topos.

## Model structures on simplicial sheaves

We may form the [[transferred model structure]] on simplicial _[[sheaf|sheaves]]_ by transferring along the degreewise [[sheafification]] [[adjunction]]
$$
  Sh(C) \stackrel{\overset{sh}{\leftarrow}}{\underset{}{\hookrightarrow}}
  PSh(C)
  \,.
$$

This defines fibrations and weak equivalences in $sSh(C)$ to be those morphisms that are fibrations or weak equivalences, respectively, as morphism in  $sPSh(C)_{Cech} = [C^{op},sSet]_{Cech}$.


As discussed there, a necessary and sufficient condition for this to be a model structure is that

* [[transfinite compositions]] of [[cobase changes]] of generating [[acyclic cofibrations]] are weak equivalences in $Sh(C)$.

Here the generating (acyclic) cofibrations in $Sh(C)$ are obtained by applying the associated sheaf functor to generating (acyclic) cofibrations in $PSh(C)$.

In the category $Sh(C)$, [[colimits]] like [[transfinite compositions]] and [[cobase changes]] are computed by applying the [[associated sheaf]] functor to the corresponding [[colimit]] in $PSh(C)$.

The latter [[colimit]] in $PSh(C)$ does yield a [[weak equivalence]] in $PSh(C)$ because $PSh(C)$ admits a [[model structure]].  By the 2-out-of-3 property, applying the [[associated sheaf]] functor yields a weak equivalence again.

## References

A detailed though unfinished account of the Čech model structure is given in

* Daniel Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

But beware of this document is unfinished. Some aspects of this appeared in 

* [[Daniel Dugger]], _[[DuggerUniv.pdf:file]]_  


[[!redirects Cech model structure on simplicial presheaves]]