
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
By the [[computation rule]] of [[function types]], the term $\big(\lambda(t:T).t\big)(x)$ reduces down to $x$, and the fiber type becomes
$$
  \sum_{y \colon T} y 
  \;=_T\; 
  x
$$
This is always a [[contractible type]]:

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