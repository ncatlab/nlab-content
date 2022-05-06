
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A __perplex number__ (also known as a __split-complex number__ or a __hyperbolic number__ or a __Lorentz number__ or myriad other such synonyms varying from author to author) is an expression of the form $a + \mathrm{I} b$, where $a$ and $b$ are [[real numbers]] and $\mathrm{I}^2 = 1$ (but $\mathrm{I} \ne \pm{1}$).  The set of perplex numbers (in fact a [[topological vector space]] and [[commutative algebra]] over the real numbers) may be denoted $\mathbf{P}$ or $\mathbb{P}$.

## Definition

This can be thought of as:

*  the vector space $\mathbb{R}^2$ made into an [[associative algebra|algebra]] by the rule
   $$ (a, b) \cdot (c, d) = (a c + b d, a d + b c) ;$$
*  $\mathbb{R}^2$ as a direct product $\mathbb{R} \times \mathbb{R}$ of [[ring|rings]];
*  the subalgebra of those $2$-by-$2$ real [[matrix|matrices]] of the form
   $$ \left(\array { a & b \\ b & a } \right);$$
*  the [[polynomial]] ring $\mathbb{R}[\mathrm{x}]$ modulo $\mathrm{x}^2 - 1$;
*  the hyperbolic $2$-dimensional algebra of [[hypercomplex number]]s.


We think of $\mathbb{R}$ as a [[subset]] of $\mathbb{P}$ by identifying $a$ with $a + 0 \mathrm{I}$.  $\mathbb{P}$ is equipped with an [[involution]] that maps $\mathrm{I}$ to $\bar{\mathrm{I}} = -\mathrm{I}$:
$$ \overline{a + \mathrm{I} b} = a - \mathrm{I} b .$$
$\mathbb{P}$ also has an [[absolute value]]:
$$ {|a + \mathrm{I} b|} = \sqrt{a^2 - b^2} ;$$
notice that the absolute value of a perplex number is a [[complex number]], with
$$ {|z|^2} = z \bar{z}. $$
But this absolute value is degenerate, in that ${|z|} = 0$ need not imply that $z = 0$.

## Properties

Some concepts in [[analysis]] can be extended from $\mathbb{R}$ to $\mathbb{P}$, but not as many as work for the [[complex numbers]].  Even algebraically, the perplex numbers are not as nice as the real or complex numbers, as they do not form a [[field]].


[[!redirects hyperbolic complex number]]
[[!redirects hyperbolic complex numbers]]
[[!redirects perplex number]]
[[!redirects perplex numbers]]
[[!redirects perplex number system]]
[[!redirects perplex number systems]]
