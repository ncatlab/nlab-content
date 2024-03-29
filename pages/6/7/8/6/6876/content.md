
# The geometric origin of inhomogeneous media
* table of contents
{: toc}

## Summary

Just as ([[Riemannian geometry|Riemannian]]) [[geometry]] is encoded in the [[metric tensor]] and manifests itself via the [[Hodge star operator]], so too do the [[constitutive equations]] of [[electromagnetism]] (cf. the discussion at *[[pre-metric electromagnetism]]*). 


For example, in linear media we have the simple constitutive relations

$$
  E = \frac{1}{\epsilon} D \quad\text{and}\quad B = \mu H.
$$

between the [[electric field]] $E$ and the [[magnetic field]] $B$.

In 4d, we have

$$
  F = B + E\wedge d t
$$

The 4d constitutive relation is 

$$
  G = \star F
  \,,
$$

which under assumptions of linearity gives

$$
  \star F = -\eta(D-H\wedge d t)
  \,,
$$

where $\eta = \sqrt{\frac{\mu}{\epsilon}}$. This may be written in a form that more closely mimics the tradition relations via

$$
  \star(v d t\wedge E) = \frac{1}{\epsilon} D\quad\text{and}\quad\star B = \mu H\wedge v d t
  \,,
$$

where $v = \frac{1}{\sqrt{\mu\epsilon}}$ (Note: $v = c$ in vacuum). 

What this means is the the electromagnetic properties of matter can be interpreted geometrically and are encoded in the 
[[Hodge star operator]]. Conversely, it means that geometrical properties of matter can be interpreted electromagnetically.

## Related entries

* [[pre-metric electromagnetism]]


## References

For more details see page 111 of [[Eric Forgy]]\'s [dissertation](http://ncatlab.org/ericforgy/show/Dissertation).
