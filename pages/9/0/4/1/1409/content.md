
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

Thus, the identity function is the function for which every element $x$ of $S$ is a [[fixed point]]. 

The identity functions are the [[identity morphisms]] in the category [[Set]] of sets.

More generally, in any [[concrete category]], the identity morphism of each object is given by the identity function on its [[underlying set]].

\begin{definition}
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
\end{definition}

## Properties

\begin{definition}
In [[dependent type theory]], the type of identity functions on a type $A$ is the type

$$\sum_{f:A \to A} \prod_{x:A} f(x) =_A x$$

of functions with a witness that every element $x:A$ is a [[fixed point]] of the function.
\end{definition}

In general, an identity function is an element of this type. However, any element of the type of identity functions is unique up to identification:

\begin{theorem}
For all types $A$, the type 

$$\sum_{f:A \to A} \prod_{x:A} f(x) =_A x$$

is a proposition. 
\end{theorem}

\begin{proof}
Suppose we have $i:A \to A$ with $I:\prod_{x:A} i(x) =_A x$ and $j:A \to A$ with $J:\prod_{x:A} j(x) =_A x$. Then we have a [[homotopy]]

$$\lambda x:A.I(x) \bullet J(x)^{-1}:\prod_{x:A} i(x) =_A j(x)$$

and by [[function extensionality]], an [[identification]]

$$\mathrm{homToId}(i, j, \lambda x:A.I(x) \bullet J(x)^{-1}):i =_{A \to A} j$$

and by dependent function application on this identification, a dependent identification

$$\mathrm{apd}(i, j, \mathrm{homToId}(i, j, \lambda x:A.I(x) \bullet J(x)^{-1}, I, J):I =_{f:A \to A.\prod_{x:A} f(x) =_A j(x)}^{i, j, \lambda x:A.I(x) \bullet J(x)^{-1}} J$$

Then by the extensionality principle for dependent pair types, we have 

$$\mathrm{pairIdsToId}(i, j, I, J)(\mathrm{homToId}(i, j, \lambda x:A.I(x) \bullet J(x)^{-1}), \mathrm{apd}(i, j, \mathrm{homToId}(i, j, \lambda x:A.I(x) \bullet J(x)^{-1}, I, J))$$

in the identity type

$$(i, I) =_{\sum_{f:A \to A} \prod_{x:A} f(x) =_A x} (j, J)$$

By induction on dependent pair types, this implies that for all elements 
$$F:\sum_{f:A \to A} \prod_{x:A} f(x) =_A x \; \mathrm{and} \; G:\sum_{f:A \to A} \prod_{x:A} f(x) =_A x \; ,$$
$$F =_{\sum_{f:A \to A} \prod_{x:A} f(x) =_A x} G$$

Thus, the type 

$$\sum_{f:A \to A} \prod_{x:A} f(x) =_A x$$

is a proposition. 
\end{proof}

\begin{theorem}
For all types $A$, the type 

$$\sum_{f:A \to A} \prod_{x:A} f(x) =_A x$$

is contractible. 
\end{theorem}

\begin{proof}
Since the type 

$$\sum_{f:A \to A} \prod_{x:A} f(x) =_A x$$

is a proposition, it suffices to construct an element of the above type. Given a type $A$, by the weakening rules and the generic variable rule in dependent type theory, one gets the identity family of elements $x:A \vdash x:A$. Then by lambda abstraction, one gets a function $\lambda x:A.x:A \to A$, and by the typal computation rule for [[weak function types]] one gets the dependent function $\beta_{A \to A}^{x:A.x}:\prod_{x:A} (\lambda x:A.x)(x) =_A x$. For [[strict function types]], we have $\beta_{A \to A}^{x:A.x} \equiv \mathrm{refl}_A$. Thus, one has the identity function
$$(\lambda x:A.x, \beta_{A \to A}^{x:A.x}):\sum_{f:A \to A} \prod_{x:A} f(x) =_A x$$ 

Since the type 
$$\sum_{f:A \to A} \prod_{x:A} f(x) =_A x$$
is a proposition and has element $(\lambda x:A.x, \beta_{A \to A}^{x:A.x})$, the type is contractible.
\end{proof}

Thus, it makes sense to refer to the canonical identity function $\lambda x:A.x$ as *[[generalized the|the]]* identity function on type $A$. 

Now, we show that the identity function is an [[equivalence of types]]:

\begin{theorem}
Any identity function is a (non-coherent) [[involution]]. 
\end{theorem}

\begin{proof}
Given a function $i:A \to A$ and a dependent function $I:\prod_{x:A} i(x) =_A x$, by function application on $i$, we have the family of identifications
$$x:A \vdash \mathrm{ap}(i, i(x), x, I(x)):i(i(x)) =_A i(x)$$
Thus by concatenation of identifications and lambda abstraction, we have the dependent function 
$$\lambda x:A.\mathrm{ap}(i, i(x), x, I(x)) \bullet I(x):\prod_{x:A} i(i(x)) =_A x$$
which indicates that the identity function $i:A \to A$ is a non-coherent involution. 
\end{proof}

By definition of [[involution]], it follows that:

\begin{corollary}
The [[inverse function]] of the identity function is the identity function itself. 
\end{corollary}

\begin{theorem}
Any identity function is bi-invertible.
\end{theorem}

\begin{proof}
Given a function $i:A \to A$ and a dependent function $I:\prod_{x:A} i(x) =_A x$, we have an element 
$$((i, \lambda x:A.\mathrm{ap}(i, i(x), x, I(x)) \bullet I(x)), (i, \lambda x:A.\mathrm{ap}(i, i(x), x, I(x)) \bullet I(x)))$$

of type 

$$\left(\sum_{j:A \to A} \prod_{x:A} i(j(x)) =_A x\right) \times \left(\sum_{k:A \to A} \prod_{x:A} k(i(x)) =_A x\right)$$

indicating that $i:A \to A$ is bi-invertible.
\end{proof}

By definition, it follows that:

\begin{corollary}
Any [[identity function]] on a type $A$ is an [[equivalence of types]]. 
\end{corollary}

Hence, in [[dependent type theory]], the identity function is also called the **identity equivalence**.

There are other ways to prove that the identity function is an equivalence of types. One of them is given below:

\begin{theorem}
Suppose that [[function types]] are defined using judgmental [[computation rules]]. Then for all [[terms]] $x \colon T$, the [[fiber]] of the identity function $\lambda(t \colon T).t \,\colon\, T \to T$ (eq:IdentityFunctionInTypeTheory) at $x$ is a [[contractible type]].
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
By the judgmental [[computation rule]] of [[function types]], the term $\big(\lambda(t:T).t\big)(x)$ reduces down to $x$, and the fiber type becomes
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

## Related concepts

* [[neutral element]]

* [[identity morphism]]

* [[identity functor]]

* [[identity natural transformation]]

* [[identity type]]

* [[transport]]

* [[fixed point]]

[[!redirects identity function]]
[[!redirects identity functions]]
[[!redirects identity map]]
[[!redirects identity maps]]

[[!redirects identity equivalence]]
[[!redirects identity equivalences]]

[[!redirects type of identity functions]]
[[!redirects types of identity functions]]
[[!redirects type of identity maps]]
[[!redirects types of identity maps]]

[[!redirects type of identity equivalences]]
[[!redirects types of identity equivalences]]