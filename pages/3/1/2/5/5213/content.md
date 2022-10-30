
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

There is a sense in which a [[sheaf]] $F$ is like a [[categorification]] of a [[function]]: the [[stalk]]-map from [[point of a topos|topos point]]s to [[set]]s $(x^* \dashv x_*) \mapsto F(x) := x^* F \in Set$ we may think of under [[decategorification]] as a [[cardinality]]-valued [[function]].

Under this interpretation, many constructions in [[category theory]] have analogs in [[linear algebra]]: for instance products of numbers correspond to categorical [[product]]s (more generally to [[limit]]s) and addition of numbers to [[coproduct]]s (more generally to [[colimit])s. Accordingly a [[colimit]]-preserving [[functor]] between [[sheaf topos]]es is analogous to a [[linear map]] or to a [[distribution]]: one also speaks of [[Lawvere distribution]]s.

This [[categorification]] of [[linear algebra]] becomes even better behaved if we pass all the way to [[(∞,1)-sheaf (∞,1)-topos]]es. Under [[∞-groupoid cardinality]] their [[stalk]]s take values also in [[integer]]s, in [[rational number]]s, and in [[real number]]s. See also the discussion at [[Goodwillie calculus]].

A [[span]] of [[base change geometric morphism]]s between toposes behaves under this interpretation like the [[linear map]] given by a [[matrix]]. Such categorified [[integral transform]]s turn out to be of considerable interest in their own right: they include operations such as the [[Fourier-Mukai transform]] which categorifies the [[Fourier transform]].


These analogies have been noticed and exploited at various places in the literature. See for instance the entries [[groupoidification]] or [[geometric ∞-function theory]]. Here we try to give a general abstract [[(∞,1)-topos theory|(∞,1)-topos theoretic]] description with examples from ordinary [[topos theory]] to motivate  the constructions. 

## Linear bases 

Every [[(∞,1)-topos]] is a [[locally presentable (∞,1)-category]]. More generally we may think of arbitrary locally presentable [[(∞,1)-categories]] as being analogous to [[vector space]]s of [[linear functional]]s. 

+-- {: .un_prop}
###### Proposition

Every [[locally presentable (∞,1)-category]] is a [[reflective sub-(∞,1)-category]] of an [[(∞,1)-category of (∞,1)-presheaves]].

=--

See [[locally presentable (∞,1)-category]] for details.

+-- {: .un_remark}
###### Remark


For $C$ a small [[(∞,1)-category]] the [[(∞,1)-category of (∞,1)-presheaves]] 

$$
  \hat C := Func(C^{op}, \infty Grpd)
$$ 

is the [[free cocompletion|free (∞,1)-cocompletion]] of $X$, hence the free completion under [[(∞,1)-colimit]]s. Under the interpretation of colimits as sums, this means that it is analogous to the vector spaces _spanned_ by the [[basis]] $C$.

Accordingly an arbitrary locally presentable $(\infty,1)$-category is analogous in this sense to a sub-space of a vector space spanned by a basis.

=--

+-- {: .un_prop}
###### Proposition

For $\hat C, \hat D$ two [[(∞,1)-categories of (∞,1)-presheaves]], a morphism $\hat C \to \hat D$ in [[Pr(∞,1)Cat]] is equivalently a [[profunctor]] $C  &#8696; D$.

=--

See [[profunctor]] for details.


## Hom-spaces

+-- {: .un_prop}
###### Proposition

For $C, D \in $ [[Pr(∞,1)Cat]] we have that $Func^L(C,D)$ is itself locally prsesentable.

=--

See [[Pr(∞,1)Cat]] for details.

+-- {: .un_remark}
###### Remark

This means that to the extent that we may think of $C, D$ as analogous to vector spaces, also the space of linear maps between them is analogous to a vector space.
=--

## Tensor products

+-- {: .un_prop}
###### Fact

For $C$ and $D$ two [[locally presentable (∞,1)-categories]] there is locally presentable $(\infty,1)$-category $C \otimes D$ and an [[(∞,1)-functor]] 

$$
  C \times D \to C \otimes D
$$

which is [[universal property|universal]] with respect to the property that it preserves [[(∞,1)-colimit]]s in both arguments.

=--

+-- {: .un_remark}
###### Remark

This means that in as far as $C, D \in $ [[Pr(∞,1)Cat]] are analogous to vector spaces, $C \otimes D$ is analogous to their [[tensor product]].

=--

## Function spaces {#FunctionSpaces}

We consider from now on some fixed ambient [[(∞,1)-topos]] $\mathbf{H}$. 

Notice that for each [[object]] $X \in \mathbf{H}$ the [[over-(∞,1)-topos]] $\mathbf{H}/X$ is the [[little topos]] of $(\infty,1)$-sheaves on $X$. So to the extent that we think of these as **function objects** , and of locally presentable $(\infty,1)$-categories as linear spaces, we may think of $\mathbf{H}/X$ as the $\infty$-vector space of $\infty$-functions on $X$

+-- {: .un_remark #EtaleIdentificationRemark}
###### Remark

The [[over-(∞,1)-topos]]es $\mathbf{H}/X$ sit by an [[etale geometric morphism]] over $\mathbf{H}$ and are characterized up to equivalence by this property. 

Moreover, we have an equivalence of the ambient $(\infty,1)$-topos $\mathbf{H}$ with the $(\infty,1)$-category of [[etale geometric morphism]]s into it.

$$
  ((\infty,1)Topos/\mathbf{H})_{et} \simeq
  \mathbf{H}
  \,.
$$

=--



+-- {: .un_example}
###### Example

Let $\mathbf{H} =$ [[FinSet]] be the ordinary [[topos]] of [[finite set]]s. Then for $X \in FinSet$ a finite set, a _function object_ on $X$ is a morphism
$\psi : \Psi \to X$ of sets. Under the [[cardinality]] [[decategorification]]

$$
  |-| : FinSet \to \mathbb{N}
$$

we think of this as the [[function]]

$$
  |\psi| : X \to \mathbb{N}
$$

given by

$$
  x \mapsto |\Psi_x|
  \,,
$$

where $\Psi_x \in FinSet$ is the [[fiber]] of $\psi$ over $X$.

=--


+-- {: .un_example #PresheavesOnGroupoids}
###### Example

Let $\mathbf{H} = $ [[∞Grpd]]. By the [[(∞,1)-Grothendieck construction]] we have for $X \in \infty Grpd$ an [[∞-groupoid]] an [[equivalence of (∞,1)-categories]]

$$
  \infty Grpd/X \simeq PSh_{(\infty,1)}(X) \simeq  Func_{(\infty,1)}(X,\infty Grpd) 
$$

of the [[over-(∞,1)-category]] of all $\infty$-groupoids over $X$  with the [[(∞,1)-category of (∞,1)-presheaves]] on $X$. And since the $\infty$-groupoid $C$ is equivalent to its [[opposite (∞,1)-category]] this is also equivalent to the [[(∞,1)-category of (∞,1)-functors]] from $C$ to [[∞Grpd]].



=--

## Products of function objects

For $\psi : \Psi \to X$ and $\phi : \Phi \to X$ in $\mathbf{H}/X$ two function objects on $X$, their [[product]] $\psi \times \phi$ in $\mathbf{H}/X$ we call the **product of function objects**.

This is computed in $\mathbf{H}$ as the [[fiber product]]

$$
 \psi \times^{\mathbf{H}/X} \phi = \Psi \times^{\mathbf{H}}_X \Phi  
$$

and the morphism down to $X$ is the evident projection

$$
  \array{
    && \Psi \times_{X}^{\mathbf{H}} \Phi
    \\
    & \swarrow && \searrow
    \\
    \Psi &&\downarrow^{\psi \times^{\mathbf{H}/X} \phi}&& \Phi
    \\
    & {}_{\mathllap{\psi}}\searrow && \swarrow_{\mathrlap{\phi}}
    \\
    && X
  }
  \,.
$$


+-- {: .un_example}
###### Example

In $\mathbf{H} = $ [[FinSet]] we have that the $\mathbb{N}$-valued function underlying the product function object is the usual pointwise product of functions

$$
  |\psi \cdot \phi| : x \mapsto |\psi|(x) \cdot |\phi|(x)
  \,.
$$

=--

## Fiber integration


For every [[morphism]] $v : X \to Y$ in the ambient [[(∞,1)-topos]] $\mathbf{H}$ there is the corresponding [[base change geometric morphism]]

$$
  (v_! \dashv v^* \dashv v_*) 
    : 
  \mathbf{H}/X
   \stackrel{\overset{v_!}{\to}}{\stackrel{\overset{v^*}{\leftarrow}}{\underset{v_*}{\to}}}
   \mathbf{H}/Y
$$

between the corresponding [[over-(∞,1)-topos]]es. Here $v_!$ acts simply by postcomposition with $v$:

$$
  v_! : (\Psi \stackrel{\psi}{\to} X) \mapsto (\Psi \stackrel{\psi}{\to} X \stackrel{v}{\to} Y)
$$

while $v^*$ acts by [[(∞,1)-pullback]] along $v$:

$$
  v^* : (\Phi \stackrel{\phi}{\to} Y) \mapsto (X \times_Y \Phi)
  \,.
$$

There is a further [[right adjoint]] $v_*$. For the present purpose the relevance of its existence is that it implies that both $v_!$ as well as $v^*$ are [[left adjoint]]s and hence both preserve [[(∞,1)-colimit]]s. Therefore these are morphism in [[Pr(∞,1)Cat]] and hence behave like linear maps on our function spaces $\mathbf{H}/X$ and $\mathbf{H}/Y$.

When we think of [[base change]] in the context of linear algebra on sheaves, we shall write $\int_{X/Y}  := v_!$

$$
  (\int_{X/Y} \dashv v^*) : 
  \mathbf{H}/X
  \stackrel{\overset{\int_{X/Y}}{\to}}{\underset{v^*}{\leftarrow}}
  \mathbf{H}/Y
$$

and call $\int_{X/Y} \psi$ the **[[fiber integration]]** of $F$ over the fibers of $v$. In particular when $Y = *$ is the [[terminal object]] we write simply

$$
  \int_X \psi \in \mathbf{H}
$$

for the **integral** of $\psi$ with values in the ambient $(\infty,1)$-topos. (See also the notation for [[Lawvere distribution]]s).


+-- {: .un_example}
###### Example

Consider the ordinary [[topos]] $\mathbf{H} = $  [[FinSet]] and for $X \in \mathbf{H}$ any set the unique [[morphism]] $v : X \to *$ to the [[terminal object]].

For $\psi : \Psi \to X$ a function object with underlying function $\psi : x \mapsto |\Psi_x|$ we have that the integral

$$
  \int_X \psi : \Psi \to *
$$

has as underlying function the constant

$$
  |\int_X \psi| = \sum_{x \in X} |\psi|(x)
  \,.
$$

=--


## Integral transforms

If we are given an oriented [[span]] or [[correspondence]]

$$
  \left(
  \array{  
     && A
     \\
     & {}^{\mathllap{i}}\swarrow && \searrow^{\mathrlap{o}}
     \\
     X &&&& Y
  }
  \right)
$$

in $\mathbf{H}$ it induces by composition of pullback and fiber integration operations a colimit-preserving $(\infty,1)$-functor

$$
  \underline{A}
  :
  \mathbf{H}/X
   \stackrel{i^*}{\to}
  \mathbf{H}/A
   \stackrel{\int_{A/Y}}{\to}
  \mathbf{H}/Y
  \,.
$$

We may always factor $(i,o)$ through the [[(∞,1)-limit|(∞,1)-product]]

$$
  \left(
  \array{
     && A
     \\
     && \downarrow^{\mathrlap{(i,o)}}
     \\
     && X \times Y
     \\
     & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
     \\
     X &&&& Y
  }
  \right)
  \,.
$$

We call the function object

$$
  ((i,o) : A \to X \times Y) \in \mathbf{H}/(X\times Y)
$$

on $X \times Y$ the **integral kernel** of $\underline{A}$.

+-- {: .un_lemma}
###### Observation

We have the **pull-tensor-push formula** for $\underline{A}$:

$$
  \underline{A} F = \int_{A/Y} i^* F =  (p_2)_!(A \times (p_1^* F) )
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows from the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#PushoutPasting">pasting law</a> for pullbacks in $\mathbf{H}$:

$$
  \array{
    i^* \Psi &\to& p_1^* \Psi &\to& \Psi
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{\psi}}
    \\
    A &\stackrel{(i,o)}{\to}& X \times Y &\stackrel{p_1}{\to}& X
  }
  \,.
$$


=--


+-- {: .un_remark }
###### Remark

By the [above remark](#EtaleIdentificationRemark) on [[etale geometric morphism]]s we have that we can recover the span $X \stackrel{i}{\leftarrow} A \stackrel{o}{\to} Y$ in $\mathbf{H}$ from the span

$$
  \array{
     \mathbf{H}/X 
    &\stackrel{\overset{i^*}{\to}}{\underset{i_*}{\leftarrow}}&
      \mathbf{H}/A
    &\stackrel{\overset{o^*}{\leftarrow}}{\underset{o_*}{\to}}&
    \mathbf{H}/Y
    \\
    & \searrow\nwarrow & \downarrow\uparrow & \swarrow\nearrow
    \\
    && \mathbf{H}
  }
$$

in $((\infty,1)Topos/\mathbf{H})_{et}$.
=--


+-- {: .un_example}
###### Example

In $\mathbf{H} = $ [[FinSet]] we have that 
$(|A_{x,y}|)$ is a $|X|$-by-$ |Y|$-[[matrix]] with entries in [[natural number]]s and the function

$$
  |A \psi | : y \mapsto | (i^* \Psi)_y | = \sum_{x \in X} |A_{x,y}| \cdot |\psi|(x)
$$ 

is the result of applying the familiar [[linear map]] given by usual [[matrix calculus]] on $|\psi|$.

=--


+-- {: .un_example}
###### Example

In the case $\mathbf{H} = $ [[∞Grpd]] we have -- as in the [above example](#PresheavesOnGroupoids) -- by the [[(∞,1)-Grothendieck construction]] an equivalence

$$
  \infty Grpd / (X \times Y) \simeq PSh_{(\infty,1)}(X \times Y)
  \,.
$$

Since the $\infty$-groupoid $Y$ is equivalent to its [[opposite (∞,1)-category]] this may also be written as

$$
  \infty Grpd / (X \times Y) Func_{(\infty,1)}(X \times Y^{op}, \infty Grpd)
  \,.
$$

The objects on the right we may again think of as $(\infty,1)$-[[profunctor]]s $X &#x21F8; Y$. So in particular the kernel $(A \to X \times Y) \in \infty Grpd/(X \times Y)$ is under this equivalence on the right hand identified with an $(\infty,1)$-profunctor

$$
  \tilde A : X &#x21F8; Y
  \,.
$$

=--