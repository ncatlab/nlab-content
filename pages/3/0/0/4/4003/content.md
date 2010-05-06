Let $C$ be a [[locally cartesian closed category]].  A **polynomial functor** (or **polynomial endofunctor**) is specified by the data
$$ W \overset{f}{\leftarrow} X \overset{g}{\to} Y \overset{h}{\to} Z $$
in $C$.  The resulting functor is the composite
$$ C/W \overset{f^*}{\to} C/X \overset{\Pi_g}{\to} C/Y \overset{\Sigma_h}{\to} C/Z. $$
where $\Pi_g$ and $\Sigma_h$ are the [[dependent product]] and [[dependent sum]] operations, right and left adjoint respectively to [[pullback]] functors $g^*$ and $h^*$.

Sometimes this general notion is called a **dependent polynomial functor**, with "polynomial functor" reserved for the special case when $W=Z=1$ is the [[terminal object]].

## Related pages

* Polynomial endofunctors are important in the definition of [[W-types]] in categories.

* Polynomial functors are a special case of [[parametric right adjoint|parametric right adjoints]].

[[!redirects polynomial functors]]
[[!redirects polynomial endofunctor]]
[[!redirects polynomial endofunctors]]
[[!redirects dependent polynomial functor]]
[[!redirects dependent polynomial functors]]
