
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Given a [[set]] $S$, the __identity function__ on $S$ is the [[function]] $id_S\colon S \to S$ that maps any element $x$ of $S$ to itself:
$$ id_S = (x \mapsto x) = \lambda x.\; x ;$$
or equivalently,
$$ id_S(x) = x .$$

The identity functions are the [[identity morphisms]] in the category [[Set]] of sets.

More generally, in any [[concrete category]], the identity morphism of each object is given by the identity function on its [[underlying set]].

\begin{remark}
In ([[dependent type theory|dependent]]) [[type theory]], the identity function on a [[type]] $T$ may be declared as
\[
  \label{IdentityFunctionInTypeTheory}
  \mathrm{id}_T 
  \;\coloneqq\; 
  \big(\lambda(t \colon T).t \big) 
  \;\colon\; 
  T \to T
  \,.
\]
\end{remark}


## Properties

\begin{theorem}
For all [[terms]] $x \colon T$, the [[fiber]] of the identity function $\lambda(t \colon T).t \,\colon\, T \to T$ (eq:IdentityFunctionInTypeTheory) at $x$ is a [[contractible type]].
\end{theorem}

\begin{proof}
The [[fiber type]] in question is the [[dependent type]] 
$$
  \sum_{y \colon T} 
  \big(
    \lambda(t:T).t
  \big)(y) 
  =_T x
  \,.
$$
All [[function types]] satisfy the propositional [[computation rule]] for function types whether the inference rules for function types are given with judgmental or propositional computation rules. By the propositional computation rule for function types, for all $y:T$ there is an [[identification]] $\beta_{T \to T}(y):\big(\lambda(t:T).t\big)(y) =_{T} y$. 

This implies that for all elements $x:T$, the types $y =_T x$ and $\big(\lambda(t:T).t\big)(y) =_{T} x$ are equivalent to each other. If there is an identification $p:y =_T x$, by pre-composition with $\beta_{T \to T}(y)$, there is an identification $\beta_{T \to T}(y) \bullet p:\big(\lambda(t:T).t\big)(y) =_{T} x$, and if there is an identification $q:\big(\lambda(t:T).t\big)(y) =_{T} x$, then by pre-composition with the inverse identification of $\beta_{T \to T}(y)$, there is an identification $\beta_{T \to T}(y)^{-1} \bullet q:y =_T x$. Since the inverse identification is defined through induction on [[identity types]], $\beta_{T \to T}(y) \bullet \beta_{T \to T}(y)^{-1} \bullet q \equiv q:\big(\lambda(t:T).t\big)(y) =_{T} x$ and $\beta_{T \to T}(y)^{-1} \bullet \beta_{T \to T}(y) \bullet p \equiv p:y =_{T} x$, which implies that the types $y =_T x$ and $\big(\lambda(t:T).t\big)(y) =_{T} x$ are strictly equivalent to each other for all $y:T$, with strict equivalences 
$$\lambda q:(\lambda(t:T).t\big)(y) =_{T} x).\beta_{T \to T}(y)^{-1} \bullet q):(\big(\lambda(t:T).t\big)(y) =_{T} x) \simeq (y =_T x)$$
and
$$\lambda p:(y =_{T} x).\beta_{T \to T}(y) \bullet q):(y =_T x) \simeq (\big(\lambda(t:T).t\big)(y) =_{T} x)$$
that are [[strict inverse functions]] of each other.

This means that the following dependent sum types are equivalent to each other with equivalence
$$
  \mathrm{tot}(\lambda q:(\lambda(t:T).t\big)(y) =_{T} x).\beta_{T \to T}(y)^{-1} \bullet q):\left(\sum_{y \colon T} 
  \big(
    \lambda(t:T).t
  \big)(y) 
  =_T x\right) \simeq
  \left(\sum_{y \colon T} y 
  \;=_T\; 
  x\right)
$$
The type
$$
  \sum_{y \colon T} y 
  \;=_T\; 
  x
$$
is always a [[contractible type]]:

* the [[center of contraction]] is given by the [[dependent pair]] $(x, \mathrm{refl}_T(x))$,

* for any $z \colon \sum_{y \colon T} y \,=_T\, x$, there is an [[identification]] 

$$
  z \;=_{\sum_{y:T} y =_T x}\; 
  \big(
    x, \mathrm{refl}_T(x)
  \big)
  \,.
$$

By [[induction]] on [[dependent sum types]], it suffices to construct an identification 
$$
  (w, p) 
  \;=_{\sum_{y:T} y =_T x}\; 
  \big(
    x, \mathrm{refl}_T(x)
  \big)
$$
for any $w \colon T$ and $p \;\colon\; w =_T x$, and by [[induction]] on [[identity types]], it suffices to construct an identification 
$$
  \big(x, \mathrm{refl}_T(x)\big) 
  \;=_{\sum_{y:T} y =_T x}\; 
  \big(x, \mathrm{refl}_T(x)\big)
$$
but that's just reflexivity on $(x, \mathrm{refl}_T(x))$
$$
  \mathrm{refl}_{\sum_{y:T} y =_T x}
  \big(
    (x, \mathrm{refl}_T(x))
  \big)
  \;\colon\; 
  \big(x, \mathrm{refl}_T(x)\big) 
  \;=_{\sum_{y:T} y =_T x}\; 
  \big(x, \mathrm{refl}_T(x)\big)
  \,.
$$

Since 
$$
  \sum_{y \colon T} y 
  \;=_T\; 
  x
$$
is a contractible type, by the equivalence $\mathrm{tot}(\lambda q:(\lambda(t:T).t\big)(y) =_{T} x).\beta_{T \to T}(y)^{-1} \bullet q)$, the type
$$
  \sum_{y \colon T} 
  \big(
    \lambda(t:T).t
  \big)(y) 
  =_T x
  \,.
$$
is also contractible. 

Thus, for all $x \colon T$, the [[fiber type]] of the identity function $\lambda(t:T).t:T \to T$ at $x$ is [[contractible type|contractible]]. 
\end{proof}

By definition, it follows that:

\begin{corollary}
The [[identity function]] on a type $T$ is an [[equivalence of types]]. 
\end{corollary}

Hence, in [[dependent type theory]], the identity function is also called the **identity equivalence**. 

Since the identity function is an equivalence of types, it has an [[inverse function]]. 

\begin{theorem}
The [[inverse function]] of the identity function is the identity function itself. 
\end{theorem}

\begin{proof}
...
\end{proof}

## Related concepts

* [[neutral element]]

* [[identity morphism]]

* [[identity functor]]

* [[identity natural transformation]]

* [[identity type]]

[[!redirects identity function]]
[[!redirects identity functions]]
[[!redirects identity map]]
[[!redirects identity maps]]

[[!redirects identity equivalence]]
[[!redirects identity equivalences]]