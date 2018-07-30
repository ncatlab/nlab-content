# Functorial analysis
* table of contents
{: toc}

## Idea

One can base [[analysis]] on _[[functional analysis]]_, i.e.,  on the use of
[[topological vector spaces]] of (generalized) functions.
Completeness hypotheses give theorems like the [[fixed point
theorem]] and the [[implicit function theorem]], which are fundamental tools to prove the existence and unicity of perturbatively small (small parameter) solutions of non-linear problems (e.g., [[partial differential equation]]s). One also sometimes (more rarely) uses related methods (compactness, etc) to extend the local solutions to global ones. However, functional analytic methods sometimes introduce too many technical restrictions on the allowed
functionals, which makes it hard the present to mathematicians the physicists' methods in [[quantum field theory]].

Another approach to analysis is given by _functorial analysis_, that is
based on the [[functor of points]] approach to [[differential geometry]] on functional spaces. The basic idea of this approach is to use a very general class
of [[partially defined functions]] on functional spaces. It has the advantage of
being adaptable to any non-linear (also [[fermion]]ic) situation and seems particularly well suited to the study of non-perturbative quantum field theories.

The flexibility of this approach does not mean that one can avoid
writing down inequalities and [[estimate]]s, like in standard analysis:
these are exactly the necessary steps to compute the definition [[domain]]s
of the objects in play.

A lot of the work of physicists uses a yoga of the type of categorical analysis, without computing the definition domains of the functionals in play: they just write down the formulas and compute with them. This could be a reason why mathematicians often think that (perturbative) quantum field theory is not well grounded mathematically.


## Example

Consider [[smooth spaces]] modeled on [[open subsets]] of [[cartesian spaces]], $U\subset \R^n$ for varying $n$, given by [[sheaves]] $U\mapsto X(U)$.
Let $\pi\colon C=\R^3\times [0,1]\to [0,1]=M$ be a [[trivial bundle]] with coordinates $(t,x)$ corresponding to euclidean time and space coordinates. Let $L(t,x_\alpha)$ be a [[lagrangian density]].
The formula
$$S(x_u)=\int_M L(t,x_{\alpha,u}(t))dt$$
defines a partially defined functional
$$S\colon \Gamma(M,C)\to \R$$
whose definition domain $D\subset \Gamma(M,C)$ is given by Lebesgue's dominated derivation theorem
$$D(U):=\{x_u\in \Gamma(M,C)(U),\;locally on U, there exists g\in L^1(M),\;|L(t,x_{\alpha,u}(t))|\leq g(t)\}$$
that is imposed to make
$u\mapsto S(x_u)$
a smooth function of the parameter $u\in U$.


## Related concepts

* [[functor of points]]

## References

* [[Frédéric Paugam]]: see the related chapter of
[Towards the mathematics of quantum field theory](http://people.math.jussieu.fr/~fpaugam/documents/enseignement/master-mathematical-physics.pdf).
