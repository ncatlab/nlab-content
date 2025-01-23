

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


\tableofcontents


## Definition

The __Vandermonde determinant__ or *Vandermonde polynomial* $\Delta(x_1,\ldots,x_n)$ is the [[determinant]] of the *[[Vandermonde matrix]]*:

\[
  \label{VandermondeMatrix}
  V(x_1,\ldots,x_n) 
  \;\coloneqq\; 
  \left( 
     \array{
        1 & x_1 & \cdots & x_1^{n-1}
        \\ 
        1 & x_2 &\cdots & x_2^{n-1}
        \\ 
        \cdot &\cdot &\cdot &\cdots
        \\ 
        1 & x_n &\cdots &x_n^{n-1}
    }
  \right) 
  \mathrlap{\,.}
\]

\begin{proposition}
$$
  \Delta(x_1,\ldots,x_n) 
  \;=\; 
  \prod_{1\leq i\lt j\leq n} (x_j - x_i)
  \,.
$$
\end{proposition}

\begin{proof}
We argue by [[induction]]. Without loss of generality, assume $x_1, \ldots, x_{n-1}$ are distinct (else the value is zero as claimed), and treat these as constants. Write 

$$\det \left( \array{1 & x_1 & \cdots & x_1^{n-1}\\ 1 & x_2 &\cdots & x_2^{n-1}\\ \cdot &\cdot &\cdot &\cdots\\ 1 & x &\cdots &x^{n-1}}\right) = f(x) = \sum_{i=1}^{n-1} a_i x^i.$$ 

Then the leading coefficient $a_{n-1}$ is $\prod_{1\leq i\lt j\leq n-1} (x_j - x_i)$ by inductive hypothesis, and $f(x)$ has simple roots at $x = x_1, \ldots, x_{n-1}$ since each of those values makes two rows equal (hence with zero determinant). It follows that 

$$
  \begin{array}{ccl}
  f(x) 
  &=&
  a_{n-1}
  \,
  \textstyle{\prod_{i=1}^{n-1}} 
  (x - x_i) 
  \\
  &=&
  \left(
    \textstyle{\prod_{1\leq i\lt j\leq n-1}} 
    (x_j - x_i)
  \right)
    \textstyle{\prod_{i=1}^{n-1}} 
    (x - x_i)
  \,.
  \end{array}
$$ 

and the inductive step follows by setting $x = x_n$. 
\end{proof}


## Properties

\begin{remark}
  \label{SkewSymemtryUnderSwappingVariables}
  If follows for instance that 
  the product $\prod_{1\leq i\lt j\leq n} (x_j - x_i)$
  changes sign when any [[pair]] $(x_r, x_s)$ of the [[variables]] are interchanged, because this corresponds to swapping the corresponding rows of the Vandermonde matrix (eq:VandermondeMatrix), and because the [[determinant]] is [[alternating multilinear map|alternating multilinear]].

This property is important, for instance, when understanding the Vandermonde determinant as a factor in the [[Laughlin wavefunction]] [[ground states]] of [[fractional quantum Hall systems]] at odd filling-fraction, where it reflects the skew-symmetry required of [[quantum many-body physics|many-]][[fermion]] (spin-polarized [[electron]]) wavefunctions.
\end{remark}


## Applications

The Vandermonde determinant appears in many important situations, as a square root of a [[discriminant]], sometimes as a [[Wronskian]], and also in Lagrange interpolation (see wikipedia [Lagrange polynomial](http://en.wikipedia.org/wiki/Lagrange_polynomial)), [[Selberg integral]] etc. 

## Related concepts

* [[Laughlin wavefunction]]

## Literature

* Wikipedia: *[Vandermonde matrix](http://en.wikipedia.org/wiki/Vandermonde_matrix)*

* [[Alexander Varchenko]]: *Multidimensional Vandermonde Determinant*, Uspekhi Mat. Nauk **43** 4 (1988) 190. 

* [[Alexander Varchenko]], _Beta-function of Euler, *Vandermonde determinant, Legendre equation and critical values of linear functions of configuration of hyperplanes*, I. Izv. Akademii Nauk USSR, Seriya Mat. **53** 6 (1989) 1206-1235. 

[[!redirects Vandermonde matrix]]