
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc} 

## Idea

In [[type theory]] the _unit type_ is the [[type]] with a unique [[term]].  It is the special case of a [[product type]] with no factors. 

In a [[model]] by [[categorical semantics]], this is a [[terminal object]]. In [[set theory]], it is a [[singleton]].

## Definition

Like any type in type theory, the unit type is specified by rules saying when we can introduce it as a type, how to construct terms of that type, how to use or "eliminate" terms of that type, and how to compute when we combine the constructors with the eliminators.

The unit type, like the binary [[product type]], can be presented both as a [[positive type]] and a [[negative type]].  In both cases the rule for building the unit type is the same, namely "it exists":

$$ \frac{ }{1\colon Type} $$

### As a positive type

Regarded as a positive type, we give primacy to the constructors, of which there is exactly one, denoted $()$ or $tt$.

$$ \frac{ }{() \colon 1 } $$

The eliminator now says that to use something of type $1$, it suffices to say what to do in the case when that thing is $()$.

$$ \frac{\vdash c\colon C}{u\colon 1 \vdash let () = u in c \;\colon C}$$

Obviously this is not very interesting, but this is what we get from the general rules of type theory in this degenerate case.  In [[dependent type theory]], we should also allow $C$ to depend on the unit type $1$.

We then have the [[∞-reduction]] rule:

$$ let () = () in c \;\to_\beta\; c$$

and (if we wish) the [[∞-reduction]] rule:

$$ let () = u in c[()/z] \;\to_\eta\; c[u/z]. $$

The $\beta$-reduction rule is simple.  The $\eta$-reduction rule says that if $c$ is an expression involving a variable $z$ of type $1$, and we substitute $()$ for $z$ in $c$ and use that (with the eliminator) to define a term involving another term $u$ of type $1$, then the result is the same as what we would get by substituting $u$ for $z$ in $c$ directly.

The positive presentation of the unit type is naturally expressed as an [[inductive type]].  In [[Coq]] syntax:

    Inductive unit : Type :=
    | tt : unit.

(Coq then implements beta-reduction, but not eta-reduction. However, eta-equivalence is provable with the internally defined [[identity type]], using the dependent eliminator mentioned above.)

### As a negative type

A negative type is characterized by its eliminators, which is a little subtle for the unit type.  But by analogy with binary [[product types]], which have two eliminators $\pi_1$ and $\pi_2$ when presented negatively, the negative unit type (a [[zero|nullary]] product) should have *no eliminators at all*.

To derive the constructors from this, we follow the general rule for negative types that to construct an element of $1$, it should suffice to specify how that element behaves under all the eliminators.  Since there *are* no eliminators, this means we have nothing to do; thus we have exactly one way to construct an element of $1$, by doing nothing:

$$\frac{ }{()\colon 1}$$

There is no $\beta$-reduction rule, since there are no eliminators to compose with the constructor.  However, there *is* an $\eta$-conversion rule.  In general, an $\eta$-[[redex]] consists of a constructor whose inputs are all obtained from eliminators.  Here we have a constructor which has no inputs, so it is not a problem that we have no eliminators to fill them in with.  Thus, the term $()\colon 1$ is an "$\eta$-redex", and it "reduces" to *any* term of type $1$ at all:

$$ () \;\to_\eta\; u$$

This is obviously not a well-defined "operation", so in this case it is better to view $\eta$-conversion in terms of *expansion*:

$$ u \;\to_\eta\; ().$$

### Positive versus negative

In ordinary "nonlinear" type theory, the positive and negative unit types are equivalent.  They manifestly have the same constructor, while we can define the positive eliminator in a trivial way as

$$ let () = u in c  \quad \coloneqq\quad c $$

Note that just as for binary [[product types]], in order for this to be a well-typed definition of the *dependent* eliminator in dependent type theory, we need to assume the $\eta$-conversion rule for the assumed negative unit type (at least, [propositionally](/nlab/show/eta-conversion#Propositional)).

Of course, the positive $\beta$-reduction rule holds by definition for the above defined eliminator.

For the $\eta$-conversion rules, if we start from the negative presentation and define the positive eliminator as above, then $let () = u in c[()/z]$ is precisely $c[()/z]$, which is convertible to $c[u/z]$ by the negative $\eta$-conversion rule $() \;\leftrightarrow_\eta\; u$.

Conversely, if we start from the positive presentation, then we have

$$
  ()
  \;\leftrightarrow_\eta\; let () = u in ()
  \;\leftrightarrow_\eta\; u
$$

where in the first conversion we use $c \coloneqq ()$ and in the second we use $c\coloneqq z$.

As in the case of binary [[product types]], these translations require the [[contraction rule]] and the [[weakening rule]]; that is, they duplicate and discard terms.  In [[linear logic]] these rules are disallowed, and therefore the positive and negative unit types become different.  The positive product becomes "one" $\mathbf{1}$, while the negative product becomes "top" $\top$.

## Properties

\begin{theorem}
The unit type is a [[contractible type]].
\end{theorem}

\begin{proof}
For all elements $x:\mathbb{1}$, by induction on the unit type, there is an identity $\mathrm{ind}_\mathbb{1}^*(x):x =_\mathbb{1} *$. This means that $*$ is a [[center of contraction]] of $\mathbb{1}$, and thus that $\mathbb{1}$ is a [[contractible type]]. 
\end{proof}

\begin{theorem}
There is an [[equivalence of types]] between the [[unit type]] and every [[contractible type]] $T$. 
\end{theorem}

\begin{proof}
By the definition of [[contractible type]], there is an element $p_T:\sum_{a:T} \prod_{b:T} a =_T b$, and thus, an element $\pi_1(p_T)$ and a witness $\pi_2(p_T)$ that $\pi_1(p_T)$ is a [[center of contraction]] of $T$. By the induction principle of the unit type, it suffices to define a function $f:\mathbb{1} \to T$ at $*$. We define it as $f(*) \coloneqq \pi_1(p_T)$. Now, all that's left is to prove that the fiber of $f$ at all elements $a:T$ is contractible. But by [[singleton induction]], it suffices to prove it for the center of contraction $\pi_1(p_T)$. The canonical element $*$ is in the fiber of $f$ at $\pi_1(p_T)$, and since $*$ is the center of contraction of $\mathbb{1}$, the fiber of $f$ at $\pi_1(p_T)$ is contractible, and thus the fiber of $f$ at every element $a:T$ is contractible. Thus, $f$ is an equivalence of types between the unit type and the contractible type $T$. 
\end{proof}

\begin{theorem}
Given a contractible type $T$ and elements $x:T$ and $y:T$, the identity type $x =_T y$ is contractible. 
\end{theorem}

Then we could derive the extensionality principle for the unit type:

\begin{lemma}
Given elements $x:\mathbb{1}$ and $y:\mathbb{1}$, there is an [[equivalence of types]] $(x =_\mathbb{1} y) \simeq \mathbb{1}$ between the [[identity type]] $x =_\mathbb{1} y$ and $\mathbb{1}$ itself. 
\end{lemma}

\begin{proof}
This follows from the previous three theorems. 
\end{proof}

## Categorical semantics

Under [[categorical semantics]], a unit type satisfying both beta and eta conversions corresponds to a [[terminal object]] in a [[category]].  More precisely:

* A terminal object may be used to interpret a unit type that validates both beta and eta rules, while

* the syntactic category of a type theory with a unit type has a terminal object, as long as the unit type satisfies both beta and eta rules.

Of course, the categorical notion of terminal object matches the *negative* definition of a unit type most directly.  In [[linear logic]], therefore, the categorical terminal object interprets "top" $\top$, while the unit object of an additional [[monoidal category|monoidal structure]] interprets "one" $\mathbf{1}$.


## Related concepts

* [[product type]]
* [[empty type]]
* [[contractible type]]

[[!include homotopy n-types - table]]



[[!redirects unit type]]
[[!redirects unit types]]
[[!redirects trivial type]]
[[!redirects trivial types]]
