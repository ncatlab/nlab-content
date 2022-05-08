
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Terminology

In [[field]] theory, what we call an 'absolute value' here is often called a 'valuation'.  However, there is also a more general notion of [[valuation]] used in field theory, which is what we call 'valuation'.  The notion of absolute value is also used in [[functional analysis]], where it may be called a 'multiplicative norm' (rather than merely submultiplicative, as norms on [[Banach algebras]] are required to be).


## Definition

For $k$ a [[rig]] (typically either a [[field]] or at least an [[integral domain]], or else an [[associative algebra]] over such), an **absolute value** on $k$ is a (non-trivial) multiplicative [[seminorm]], or equivalently a finite real-valued [[valuation]].

This means it is a [[function]] 

$$
  {\vert {-} \vert}\colon k \to \mathbb{R}
$$ 

to the [[real numbers]] such that for all $x, y \in k$

1. ${\vert x \vert} \geq 0$;

2. ${\vert x \vert} = 0$ precisely if $x = 0$;

3. ${\vert x \cdot y \vert} = {\vert x \vert} {\vert y \vert}$;

4. ${\vert x + y \vert} \leq {\vert x \vert} + {\vert y \vert}$ (the [[triangle inequality]]).


If the last triangle inequality is strengthened to

* ${\vert x + y \vert} \leq max({\vert x \vert}, {\vert y \vert})$ 

then ${\vert {-} \vert}$ is called an [[ultrametric]] or **non-archimedean** absolute value, since then for any $x, y \in k$ with $\vert x \vert \lt \vert y \vert$ then for all natural numbers $n$, $\vert n x \vert \leq \vert x \vert \lt \vert y \vert$.  If the opposite holds, that whenever $\vert x \vert \lt \vert y \vert$ (and $x\neq 0$) there exists a natural number $n$ with $\vert n x \vert \gt \vert y \vert$, then it is called **archimedean**.

Two absolute values ${\vert {-} \vert}_1$ and ${\vert {-} \vert}_2$ are called _equivalent_ if for all $x \in k$

$$
  ({\vert x \vert}_1 \lt 1)
   \Leftrightarrow
  ({\vert x \vert}_2 \lt 1)
  \,.
$$  

An [[equivalence class]] of absolute values is also called a **[[place]]**. 

A [[field]] equipped with an absolute value which is a [[complete metric space]] with respect to the corresponding [[metric]] is called a [[complete field]].


## Examples

### Trivial absolute value

Every field admits the trivial absolute value ${\vert {-} \vert}_0$ defined by

$$
  {\vert x \vert}_0 = 
  \left\{
    \array{
       0 & if\; x = 0
       \\
       1 & otherwise
    }
  \right.
  \,.
$$

This is non-archimedean.


### On the real and complex numbers
 {#OnTheRealAndComplexNumbers}


Since the [[real numbers]] are a [[totally ordered abelian group]], the standard absolute value ${\vert {-} \vert_\infty}$ on the [[real numbers]] is

$$
  {\vert x \vert_\infty} = \max(x, -x)
$$

The standard absolute value on the [[complex numbers]] is 

$$
  {\vert x + i y \vert_\infty}
  = 
  \sqrt{x^2 + y^2}
  \,.
$$

These standard absolute values are archimedean, and with respect to these standard absolute values, both $\mathbb{R}$ and $\mathbb{C}$ are [[complete field|complete]] and hence are complete [[archimedean valued fields]]. Notice that $\mathbb{R}$ is in addition an [[ordered field]] and as such also an [[archimedean field]].

Similar norms exist on the [[quaternions]] and [[octonions]], showing that absolute values can be of interest on noncommutative and even nonassociative [[division rings]].


### On the rational numbers

The standard absolute value [above](#OnTheRealAndComplexNumbers) restricts to the standard absolute value on the [[rational numbers]]

$$
  {\vert {-} \vert_\infty}\colon \mathbb{Q} \to \mathbb{R}
  \,.
$$

Moreover, for any [[prime number]] $p$ and [[positive number]] $\epsilon \lt 1$, there is an absolute value ${\vert {-} \vert_{p,\epsilon}}$ on $\mathbb{Q}$ defined by

$$
  \left\vert \frac{k}{l} p^n\right\vert_{p,\epsilon}
  = 
  \epsilon^n
$$

whenever $n$ is an [[integer]] and $k$ and $l$ are nonzero [[integers]] not divisible by $p$ (and ${\vert 0 \vert_{p,\epsilon}} = 0$).

These are called the **$p$-adic absolute values**.  Given $p$, they are all equivalent (the open unit ball consists of all rational numbers whose denominator in lowest terms is not divisible by $p$), so there is a unique **$p$-adic [[place]]**.  For most purposes, only the place matters, and one may write simply $|q|_p$; however, if one wants a specific absolute value, then the usual choice is to use $\epsilon = 1/p$ (so that ${|p^n|_p} = p^{-n}$ whenever $n$ is an integer).

The $p$-adic absolute value is non-archimedean. The [[complete field|completion]] $\mathbb{Q}_p$ of $\mathbb{Q}$ under this absolute value is called the field of [[p-adic numbers]], which is therefore a [[non-archimedean field]].

[[Ostrowski's theorem]] says that these examples exhaust the non-trivial absolute values on the [[rational numbers]]. Therefore the [[real numbers]] and the [[p-adic numbers]] are the only possible field completions of $\mathbb{Q}$.


### On Laurent power series

The field of [[Laurent series]] $k[ [ T] ]$ over a [[field]] $k$ is a [[complete field]] with respect to the absolute value that sends a series to $\epsilon^n$ for a fixed $0 \lt \epsilon \lt 1$ and with $n$ the lowest integer such that the $n$th coefficient of the series is not $0$.

## See also 

* [[real square root]]

* [[sign function]]

## References

Section 1.5, 1.6 of

* {#BoschGuntzerRemmert84} [[Siegfried Bosch]], [[Ulrich Güntzer]], [[Reinhold Remmert]], _[[Non-Archimedean Analysis]] -- A systematic approach to rigid analytic geometry_, 1984 ([pdf](http://math.arizona.edu/~cais/scans/BGR-Non_Archimedean_Analysis.pdf))


[[!redirects absolute value]]
[[!redirects absolute values]]

[[!redirects archimedean absolute value]]
[[!redirects Archimedean absolute value]]
[[!redirects archimedean absolute values]]
[[!redirects Archimedean absolute values]]

[[!redirects archimedean]]
[[!redirects non-archimedean]]

[[!redirects non-archimedean valuation]]
[[!redirects non-archimedean valuations]]

[[!redirects real absolute value]]
[[!redirects real absolute values]]