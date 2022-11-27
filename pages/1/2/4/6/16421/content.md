
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A recursive function is any [[function]] defined by [[recursion]] (i.e. non-dependent [[induction]]). 

For more see also at *[[partial recursive function]]*.

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

## Related concepts

* [[function]]

* [[recursion]]

* [[partial recursive function]]

* [[proof theory]]


## References

See also:

* Wikipedia, *[Recursive function](https://en.m.wikipedia.org/wiki/Recursive_function)

[[!redirects recursive functions]]