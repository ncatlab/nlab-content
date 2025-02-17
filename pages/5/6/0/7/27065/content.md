+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

The notion of *restrictions* in a [[double category]] abstracts that of the classical operation of [[restriction of scalars]] of [[bimodules]].
Indeed, they are usually available in [[framed bicategories]], which are formal analogoues to double categories of bimodules; and indeed restrictions in a double category of bimodules correspond to restrictions of scalars.

The dual notion is that of **[[extension (double category theory)|extension]]**.

## Definition
In a [[double category]] $\mathbb{D}$, the **restriction** of a [[loose arrow]] $p:A \nrightarrow B$ along [[tight morphisms]] $f:X\to A$, $g:Y \to B$ is a universal filling of the niche: 
\begin{tikzcd}
	X & Y \\
	A & B
	\arrow["f"', from=1-1, to=2-1]
	\arrow["g", from=1-2, to=2-2]
	\arrow["p"', "\shortmid"{marking}, from=2-1, to=2-2]
\end{tikzcd}
That is, a 2-cell:
\begin{tikzcd}
	X & Y \\
	A & B
	\arrow[""{name=0, anchor=center, inner sep=0}, "{p(f,g)}", "\shortmid"{marking}, from=1-1, to=1-2]
	\arrow["f"', from=1-1, to=2-1]
	\arrow["g", from=1-2, to=2-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "p"', "\shortmid"{marking}, from=2-1, to=2-2]
	\arrow["{\mathrm{cart}}", shorten <=4pt, shorten >=4pt, Rightarrow, from=0, to=1]
\end{tikzcd}
such that every other 2-cell as below left factors as below right:
\begin{tikzcd}
	R & S & R & S \\
	X & Y & X & Y \\
	A & B & A & B
	\arrow[""{name=0, anchor=center, inner sep=0}, "q", "\shortmid"{marking}, from=1-1, to=1-2]
	\arrow["h"', from=1-1, to=2-1]
	\arrow["k", from=1-2, to=2-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "q", "\shortmid"{marking}, from=1-3, to=1-4]
	\arrow["h"', from=1-3, to=2-3]
	\arrow["k", from=1-4, to=2-4]
	\arrow["f"', from=2-1, to=3-1]
	\arrow["{=}"{marking, allow upside down}, draw=none, from=2-2, to=2-3]
	\arrow["g", from=2-2, to=3-2]
	\arrow[""{name=2, anchor=center, inner sep=0}, "{p(f,g)}", "\shortmid"{marking}, from=2-3, to=2-4]
	\arrow["f"', from=2-3, to=3-3]
	\arrow["g", from=2-4, to=3-4]
	\arrow[""{name=3, anchor=center, inner sep=0}, "p"', "\shortmid"{marking}, from=3-1, to=3-2]
	\arrow[""{name=4, anchor=center, inner sep=0}, "p"', "\shortmid"{marking}, from=3-3, to=3-4]
	\arrow["\phi", shorten <=9pt, shorten >=9pt, Rightarrow, from=0, to=3]
	\arrow["{\exists! \hat\phi}"{pos=0.4}, shorten <=4pt, shorten >=11pt, Rightarrow, from=1, to=2]
	\arrow["{\mathrm{cart}}", shorten <=4pt, shorten >=4pt, Rightarrow, from=2, to=4]
\end{tikzcd}

## Properties
Admitting all restrictions is sufficient for a double category to be a [[framed bicategory]]. In fact, restrictions are given by cartesian maps for the functor $(L,R):\mathbb{D}_1 \to \mathbb{D}_0 \times \mathbb{D}_0$, thus admitting all restrictions means to admit all cartesian lifts, making $(L,R)$ into a fibration.

As proven in [Shulman '08](#Shulman08), restrictions can be constructed out of [[companions]] and [[conjoints]] alone.
Indeed, notice first that a companion of $f$ is equivalently given as the restriction $A(f,1)$, where $A$ denotes the unit loose arrow at $A$; and dually a conjoint of $f$ is the restriction $B(1,f)$.
Moreover, it's easy to see that (denoting by $\odot$ looseward composition):
$$
(p \odot q)(f,g) = p(f,1) \odot q(1,g)
$$
Thus we conclude
$$
p(f,g) = (A \odot p \odot B)(f,g) = A(f,1) \odot p \odot B(1,g).
$$
This can be used to see that admitting all restrictions is equivalent to admitting all [[extension (double category theory)|extensions]], since extensions can also be obtained by composing with companions and conjoints, and companions and conjoints are also special instances of extensions.

## See also

* [[framed bicategory]]
* [[extension (double category theory)]]

## References

* {#Shulman08} [[Mike Shulman]], *Framed bicategories and monoidal fibrations*, Theory and Applications of Categories **20** 18 (2008) 650–738 &lbrack;[tac:2018](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html), [arXiv:0706.1286](https://arxiv.org/abs/0706.1286)&rbrack;