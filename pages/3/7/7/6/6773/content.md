The __Vandermonde determinant__ or Vandermonde polynomial $\Delta(x_1,\ldots,x_n)$ is the determinant of the Vandermonde matrix 

$$
V(x_1,\ldots,x_n) = \left( \array{1 & x_1 & \cdots & x_1^{n-1}\\ 1 & x_2 &\cdots & x_2^{n-1}\\ \cdot &\cdot &\cdot &\cdots\\ 1 & x_n &\cdots &x_n^{n-1}}\right) 
$$

+-- {: .num_prop} 
###### Proposition 
$\Delta(x_1,\ldots,x_n)= \prod_{1\leq i\lt j\leq n} (x_j - x_i)$. 
=-- 

+-- {: .proof} 
###### Proof 
We argue by induction. WLOG, assume $x_1, \ldots, x_{n-1}$ are distinct (else the value is zero as claimed), and treat these as constants. Write 

$$\det \left( \array{1 & x_1 & \cdots & x_1^{n-1}\\ 1 & x_2 &\cdots & x_2^{n-1}\\ \cdot &\cdot &\cdot &\cdots\\ 1 & x &\cdots &x^{n-1}}\right) = f(x) = \sum_{i=1}^{n-1} a_i x^i.$$ 

Then the leading coefficient $a_{n-1}$ is $\prod_{1\leq i\lt j\leq n-1} (x_j - x_i)$ by inductive hypothesis, and $f(x)$ has simple roots at $x = x_1, \ldots, x_{n-1}$ since each of those values makes two rows equal (hence with zero determinant). It follows that 

$$f(x) = a_{n-1}\prod_{i=1}^{n-1} (x - x_i) = (\prod_{1\leq i\lt j\leq n-1} (x_j - x_i))\prod_{i=1}^{n-1} (x - x_i)$$ 

and the inductive step follows by setting $x = x_n$. 
=-- 

The Vandermonde determinant appears in many important situations, as a square root of a [[discriminant]], sometimes as a [[Wronskian]], and also in Lagrange interpolation (see wikipedia [Lagrange polynomial](http://en.wikipedia.org/wiki/Lagrange_polynomial)), [[Selberg integral]] etc. 

* wikipedia [Vandermonde matrix](http://en.wikipedia.org/wiki/Vandermonde_matrix)
* A. Varchenko, Multidimensional Vandermonde Determinant, Uspekhi Mat. Nauk 43:4 (1988), p. 190. 
* A. Varchenko, _Beta-function of Euler, Vandermonde determinant, Legendre equation and critical values of linear functions of configuration of hyperplanes_, I. Izv. Akademii Nauk USSR, Seriya Mat., 53:6 (1989), 1206-1235. 
[[!redirects Vandermonde matrix]]