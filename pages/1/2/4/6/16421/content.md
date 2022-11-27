
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A recursive function is any [[function]] defined by [[recursion]] (i.e. non-dependent [[induction]]). 

Recursive functions could be contrasted with inductively defined dependent functions, where one uses terms of a general [[dependent product type]] rather than a [[function type]]. Alternatively, they could be considered as a special case of an inductively defined dependent function where the target type family does not actually depend upon the source. 

Similar to the case with induction, recursive functions could be generalized to *higher recursive functions*, where functions are recursively defined not only on the [[term]] constructors, but also the [[identity]] constructors of an [[higher inductive type]]. 

Recursive functions defined on the [[natural numbers]] are particularly important for [[computability]]. For more see also at *[[partial recursive function]]*.

## Example 


\begin{example}
The [[negation]] function 

$$
  \neg \colon \mathrm{Bool} \to \mathrm{Bool}
$$ 

on the [[booleans type]] is recursively defined by sending  [[true|$\top$]] to [[false|$\bot$]] and [[false|$\bot$]] to [[true|$\top$]]:

$$
  \begin{array}{l}
    \neg \top =_{\mathrm{Bool}} \bot
    \\
    \neg \bot =_{\mathrm{Bool}} \top
  \end{array}
$$

\end{example}

\begin{example}
The double function 

$$
  \mathrm{double} \colon \mathbb{N} \to \mathbb{N}
$$ 

on the [[natural numbers type]] is recursively defined by sending $0$ to $0$ and $s(n)$ to $s(s(\mathrm{double}(n)))$:

$$
  \begin{array}{l}
    \mathrm{double}(0) =_{\mathbb{N}} 0
    \\
    n:\mathbb{N} \vdash \mathrm{double}(s(n)) =_{\mathbb{N}} s(s(\mathrm{double}(n)))
  \end{array}
$$

\end{example}

\begin{example}
This last example is an example of a *higher recursive function*. Given a type $A$, elements $a:A$ and $b:A$, and identity $q:a =_A b$, there is a higher recursive function $f:\mathbb{I} \to A$ from an [[interval type]] $\mathbb{I}$ to $A$, recursively defined by 

$$
  \begin{array}{l}
    \beta_f^0:f(0) =_A a
    \\
    \beta_f^1:f(1) =_A b
    \\
    \beta_f^p:\mathrm{ap}_f(p) =_{f(0) =_A f(1)} \mathrm{trans}_{f(0), b, f(1)}(\mathrm{trans}_{f(0), a, b}(\beta_f^0, q), \mathrm{sym}_{f(1), b}(\beta_f^1)) 
  \end{array}
$$

where $\mathrm{ap}_f:(0 =_\mathbb{I} 1) \to (f(0) =_A f(1))$ is the [[action on identities]], $\mathrm{trans}_{a, b, c}:(a =_A b) \times (b =_A c) \to (a =_A c)$ is [[transitivity]], and $\mathrm{sym}_{a, b}:(a =_A b) \to (b =_A a)$ is [[symmetry]] of identities. 
\end{example}

## Related concepts

* [[function]]

* [[recursion]]

* [[partial recursive function]]

* [[proof theory]]


## References

See also:

* Wikipedia, *[Recursive function](https://en.m.wikipedia.org/wiki/Recursive_function)

[[!redirects recursive functions]]