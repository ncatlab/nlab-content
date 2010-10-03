#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

A __dual number__ is given by an expression of the form $a + \epsilon b$, where $a$ and $b$ are [[real numbers]] in $\mathbb{R}$ or more generally elements in any [[ring]] -- and $\epsilon^2 = 0$ (but $\epsilon \ne 0$).  The set of dual numbers is a [[topological vector space]] and a [[commutative algebra]] over the real numbers.


## Interpretations ##

This can be thought of as:

*  the vector space $\mathbb{R}^2$ made into an [[associative algebra|algebra]] by the rule
   $$ (a, b) \cdot (c, d) = (a c, a d + b c) ;$$
*  the subalgebra of those $2$-by-$2$ real [[matrix|matrices]] of the form
   $$ \left(\array { a & b \\ 0 & a } \right);$$
*  the [[polynomial]] ring $\mathbb{R}[\mathrm{x}]$ modulo $\mathrm{x}^2$;
*  the parabolic $2$-dimensional algebra of [[hypercomplex number]]s;
*  the algebra of functions on the [[infinitesimal object|infinitesimal interval]] (the smallest of the [[infinitesimally thickened points]]) in [[synthetic differential geometry]].
* if $\epsilon$ is regarded as being of degree 1 and $\mathbb{R} \oplus \epsilon \mathbb{R}$ is regarded accordingly as a [[superalgebra]] then this is the algebra of functions on the [[odd line]] $\mathbb{R}^{0|1}$.
* the square-0-extension corresponding to the $\mathbb{R}$-[[module]] (see there) given by $\mathbb{R}$ itself.

We think of $\mathbb{R}$ as a [[subset]] of $\mathbb{D}$ by identifying $a$ with $a + 0 \epsilon$.


## Properties

$\mathbb{D}$ is equipped with an [[involution]] that maps $\epsilon$ to $\bar{\epsilon} = -\epsilon$:
$$ \overline{a + \epsilon b} = a - \epsilon b .$$
$\mathbb{D}$ also has an [[absolute value]]:
$$ |{a + \epsilon b}| = |a| ;$$
notice that the absolute value of a dual number is a non-negative real number, with
$$ |z|^2 = z \bar{z}. $$
But this absolute value is degenerate, in that $|z| = 0$ need not imply that $z = 0$.

Some concepts in analysis can be extended from $\mathbb{R}$ to $\mathbb{D}$, but not as many as work for the [[complex numbers]].  Even algebraically, the dual numbers are not as nice as the real or complex numbers, as they do not form a [[field]].


[[!redirects dual numbers]]
[[!redirects dual number system]]
[[!redirects parabolic complex number]]
[[!redirects ring of dual numbers]]