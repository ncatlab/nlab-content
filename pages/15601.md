
# Ricatti equations
* table of contents
{: toc}

## Idea

A (general) __Ricatti differential equation__ is any first-order [[ordinary differential equation]] for a function $y = y(t)$ which is of the form

$$
\frac{d y}{d t} = a_0(t) + a_1(t) y + a_2(t) y^2 
$$

with $a_0(t)\neq 0$ and $a_2(t)\neq 0$.  

## Connection to fractional linear transformations

Ricatti equations are to fractional linear transformations as first-order linear ordinary differential equations are to affine transformations, in the following sense.  A first-order linear ordinary differential equation

$$
\frac{d y}{d z} = a_0(t) + a_1(t) y
$$

has (under suitable regularity conditions on $a_0$ and $a_1$) solutions $y(t)$ depending in an affine manner on the initial data:

$$ y(t) = f(t) y(0) + g(t) $$

for functions $f,g$ independent of $y(0)$.   More generally, any Riccati equation 

$$
\frac{d y}{d t} = a_0(t) + a_1(t) y + a_2(t) y^2 
$$

has (under suitable regularity conditions, and at least for short times) solutions $y(t)$ depending on the initial data as follows:

$$ y(t) = \frac{f(t) y(0) + g(t)}{h(t) y(0) + i(t)} $$

for functions $f,g,h,i$ independent of $y(0)$.  

Unlike solutions  of first-order linear equations, solutions of Riccati equations can blow up in finite time; however, these solutions become defined for all time if we let $y$ take values in the [[projective line]] rather than the [[affine line]]: that is, $\mathbb{R}\mathrm{P}^1$ or $\mathbb{C}\mathrm{P}^1$ rather than $\mathbb{R}$ or $\mathbb{C}$.  

Indeed, the group of fractional linear transformations, the [[projective general linear group]] $\mathrm{PGL}(2,\mathbb{R})$ or $\mathrm{PGL}(2,\mathbb{C})$, acts naturally on the projective line, with the group of affine transformations being the subgroup that preserves the affine line.

The group of smooth $\mathrm{PGL}(2)$-valued functions on the real line acts on the space of Ricatti equations.  First, note that this group acts on $\mathbb{P}^1$-valued functions on the real line as follows:

$$ \left( \begin{array}{cc} f(t) & g(t) \\ h(t) & i(t) \end{array} \right) \colon y(t) \mapsto \tilde{y}(t) = \frac{f(t) y(t) + g(t)}{h(t) y(t) + i(t)} $$

Then, given any Ricatti equation 

$$
\frac{d y}{d t} = a_0(t) + a_1(t) y + a_2(t) y^2   \qquad \star
$$

there is another Ricatti equation such that $\tilde{y}$ is a solution of this new Ricatti equation iff $y$ is a solution of $\star$.  

## Correspondence with 2nd order linear ODEs

There is a correspondence between Ricatti equations and a wide class of
2nd order linear differential equations, namely Ricatti equation for $y$ gives a 2nd order linear ODE for $u$ which satisfies $a_2 u' = u y$, namely

$$
u'' + a_0 a_2 u' + \left( a_1 + \frac{a_2'}{a_2} \right) u = 0.
$$
Of course, the coefficients are non-constant.


## Reduction to a Bernoulli ODE in the presence of a particular solution

Unlike the [[Bernoulli differential equation]] which has $a_0(z) = 0$ and $a_2(z) \neq 0$, the Ricatti equation can not be solved in quadratures in general, unless a a particular solution $y_1$ is known. If so, then we can write $y = y_1 + u$ and
write down the equation for $u$ which appears to be an example of a Bernoulli differential equation, hence solvable in quadratures. Regarding that $w = 1/u$ is
the substitution for reducing Bernoulli to first order linear ODE, we can reduce
the original Ricatti to such ODE by substituting $y = y_1 + 1/w$.


## Matrix Ricatti equation

For a generalization, the matrix Ricatti equation, see [the eom article](#eom).


## Literature

* Springer [[eom]] [Ricatti equation](http://www.encyclopediaofmath.org/index.php?title=p/r081770)
  {#eom}

* Wikipedia: [Ricatti equation](http://en.wikipedia.org/wiki/Riccati_equation)


category: analysis

[[!redirects Ricatti equation]]
[[!redirects Ricatti equations]]
[[!redirects Ricatti differential equation]]
[[!redirects Ricatti differential equations]]
