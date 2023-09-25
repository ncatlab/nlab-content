
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A *linear isometry* is a [[linear map]] 

$$
  \phi
  \,\colon\,
  \mathscr{H}_1
  \longrightarrow
  \mathscr{H}_2
$$

between [[vector spaces]] equipped with ([[Hermitian form|Hermitian]]) [[inner products]] ${\langle \cdot \vert \cdot \rangle}_{i}$ (often: [[Hilbert spaces]]) which is also an [[isometry]] in that it preserves these inner products:

$$
  \left\langle \phi(-) \vert \phi(-) \right\rangle_2
  \;=\;
  \left\langle - \vert - \right\rangle_1
$$

or equivalently, in terms of [[adjoint operators]]:

$$
  \phi^\dagger \cdot \phi \,=\, Id_{\mathscr{H}_1}
  \,.
$$

If also the reverse condition $\phi \cdot \phi^\dagger \,=\, Id_{\mathscr{H}_2}$ holds, then $\phi$ is called a *[[unitary operator]]*, which is the case iff $\phi$ is [[surjective map]]. 

## Related concepts

* [[isometry]]

* [[linear isomorphism]]

* [[unitary operator]]

## References

See also: 

* Wikipedia, *[Linear isometry](https://en.wikipedia.org/wiki/Isometry#Linear_isometry)*

[[!redirects linear isometries]]
