+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea

A linear-non-linear adjunction is an [[adjunction]] between a cartesian and a non-cartesian [[monoidal categories]]:

\begin{tikzcd}
	{(\mathbf{L}, \otimes, 1)} && {(\mathbf{M}, \times, \top)}
	\arrow["{!}", from=1-1, to=1-1, loop, in=145, out=215, distance=20mm]
	\arrow[""{name=0, anchor=center, inner sep=0}, "M"', shift right=2, from=1-1, to=1-3]
	\arrow[""{name=0p, anchor=center, inner sep=0}, phantom, from=1-1, to=1-3, start anchor=center, end anchor=center, shift right=2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "L"', shift right=2, from=1-3, to=1-1]
	\arrow[""{name=1p, anchor=center, inner sep=0}, phantom, from=1-3, to=1-1, start anchor=center, end anchor=center, shift right=2]
	\arrow["\dashv"{anchor=center, rotate=-90}, draw=none, from=1p, to=0p]
\end{tikzcd}

Here $\mathbf{L}$ is [[symmetric monoidal category|symmetric monoidal]], $\mathbf{M}$ is [[cartesian monoidal category|cartesian monoidal]].
The adjunction takes place in the [[2-category]] of symmetric monoidal categories and [[lax monoidal functors]], thus by [[doctrinal adjunction]] $L$ is in fact [[strong monoidal functor|strong monoidal]].

Such a situation forms the ground on which practically all categorical semantics of linear logic (of various kinds) are built. Specifically, the comonad $!=L M$ on $\mathbf{L}$ is the [[exponential modality]] of [[linear logic]]. A survey can be found in ([Mellies '09](#PAM09), Chapter 7).

## Related

* [[linear-non-linear logic]]

* [[LNL polycategory]]

## References

* {#PAM09} [[Paul-André Melliès]], _Categorical semantics of linear logic_. Panoramas et syntheses, 27:15–215, 2009, ([citeseerx](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=4a5b1bf3c04343055dd00f0a60862b44b6dfc9a3))
