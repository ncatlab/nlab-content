
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

In [[logic]], a variable is a symbol that stands for an arbitrary instantiation of some given [[type]] (although in single-typed theories the type is trivial).  Thus, every variable of type $T$ is a [[term]] of type $T$ (although typically there are other terms).

Logicians have developed several ways to precisely specify what variables are and how to keep track of them, and the only thing more annoyingly pedantic than learning one of these is translating between different ones.


## Free and bound variables

If we keep track of [[context]], every [[context extension|introduction of a variable]] changes the context.  Thus, whatever [[terms]] of [[type]] $T$ there may (or may not) be in a given context $\Gamma$, in the context $(\Gamma, x\colon T)$ ---which is $\Gamma$ extended by a __free variable__ $x$ of type $T$--- there is (at least) one more term of type $T$, and that term is $x$ itself.

Conversely, we may be able to take a term $a$ in the context $(\Gamma, x\colon T)$ and apply some operation $f$ to it to create a term $f(a)$ (possibly of a different type) in the context $\Gamma$; then any appearances of the variable $x$ in the term $a$ have become __bound variables__ in the term $f(a)$.  That is, the appearances of $x$ are bound by the operator $f$, and $x$ has no meaning outside of its scope.

So for example, if (say in something simple like [[Peano arithmetic]], supplemented with the abbreviations used in practice) I write $2x$, this is a term (for a natural number) in a context with a free variable $x$, whereas if I write $3 \sum_{x=0}^4 2x + 5$, this is a term (also for a natural number) in a context with no free variables; here, $x$ is bound.  The variable $x$ has a meaning after the operator $\sum_{x=0}^4$ (whose notation also specifies the variable that will have a meaning inside it) and before the plus sign (which, following the standard order of operations, marks the end of the scope of $\sum_{x=0}^4$) but has no meaning outside of that (where the $3$ and $5$ are, or even where the $0$ and $4$ are).  And indeed, the ultimate meaning of $2x$ depends on what $x$ is, but the ultimate meaning of $3 \sum_{x=0}^4 2x + 5$ is simply $65$.


## In categorical semantics

In the [[internal language]] of a [[category]] $\mathcal{C}$ a [[morphism]]

$$
  f\colon B \to A
$$


is a _[[term]]_ $f(x)$ of _[[type]]_ $A$ where $x$ is 
a **free variable** of _type_ $B$, which in symbols is given by

$$ 
  x\colon B \vdash f(x)\colon A
  \,. 
$$

We may think of the _free variables_ here as being placeholders for all the [[generalized elements]] 
$U \stackrel{x}{\to} B$ of $B$. 



Then the assertion 

$$
  x\colon B \vdash f(x)\colon A
$$ 

indicates that with $B \stackrel{f}{\to} A$ given we may send $U \stackrel{x}{\to} B$ to the [[composition]] 

$$
  (U \stackrel{x}{\to} B \stackrel{f}{\to}A ) = (U \stackrel{f(x)}{\to} A)
  \,.
$$

A free variable becomes a **bound variable** after application of a [[quantifier]]: for instance the image of $f\colon P \to X$ under [[base change]]

$$
  \mathcal{C}_{/X} \stackrel{\to}{\stackrel{\leftarrow}{\to}}
  \mathcal{C}
$$

represents, for the [[left adjoint]] the [[type]] 

$$
  \exists x\colon X , P(x)
$$

([[existential quantifier]]), and the the [[right adjoint]] the type

$$
  \forall x\colon X , P(x)
$$

([[universal quantifier]]) in which now $x$ is a _bound variable_.

## Related concepts

* [[quantification]]

* [[context extension]]

* [[proposition]]

## References
 {#References}

A textbook account with an eye towards applications in [[computer science]] is in section 1.2 of

*  [[Robert Harper]], _Practical Foundations for Programming Languages_ ([web](http://www.cs.cmu.edu/~rwh/plbook/book.pdf))
{#Harper}

An exposition on the relation between free variables and [[universal quantification]] is in

* [[Andrej Bauer]], _Free variables are not "implicitly universally quantified"!_ ([web](http://math.andrej.com/2012/12/25/free-variables-are-not-implicitly-universally-quantified/))

[[!redirects variable]]
[[!redirects variables]]

[[!redirects free variable]]
[[!redirects free variables]]

[[!redirects bound variable]]
[[!redirects bound variables]]

[[!redirects dependent variable]]
[[!redirects dependent variables]]

[[!redirects metavariable]]
[[!redirects metavariables]]
