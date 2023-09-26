
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

between [[normed space|normed]] [[vector spaces]] which preserves the norm:

$$
  \big\Vert \psi(-) \big\Vert_2
  \;=\;
  \big\Vert - \big\Vert_1
  \,.
$$

In particular, when the norm is induced by ([[Hermitian form|Hermitian]]) [[inner products]] ${\langle \cdot \vert \cdot \rangle}_{i}$ (as on [[Hilbert spaces]]) 

$$
  {\big\Vert \psi \big\Vert}_i
  \,\equiv\,
  \sqrt{
     \left\langle \psi \vert \psi \right\rangle_i
  }
$$

then a linear isometry is an [[isometry]] in that it preserves these inner products:

$$
  \big\langle \phi(-) \vert \phi(-) \big\rangle_2
  \;=\;
  \left\langle - \vert - \right\rangle_1
$$

or equivalently, in terms of [[adjoint operators]]:

\[
  \label{InTermsOfAdjointOperators}
  \phi^\dagger \cdot \phi \,=\, Id_{\mathscr{H}_1}
  \,.
\]

\begin{remark}
**(relation to unitary operators)**
\linebreak
If in addition to (eq:InTermsOfAdjointOperators) also the reverse condition $\phi \cdot \phi^\dagger \,=\, Id_{\mathscr{H}_2}$ holds, then $\phi$ is called a *[[unitary operator]]*, which is the case iff $\phi$ is [[surjective map]]. 
\end{remark}


## Properties

\begin{proposition}
  \label{LinearIsometriesAreInjective}
  Linear isometries are [[injective maps]].
\end{proposition}
\begin{proof}
  For
  $\left\vert \psi \right\rangle, \left\vert \psi' \right\rangle \,\colon\, \mathscr{H}$ we need to show that
$$
  \phi\left\vert \psi \right\rangle
  \;=\;
  \phi\left\vert \psi' \right\rangle
  \;\;\;\;
  \Rightarrow
  \;\;\;\;
  \left\vert \psi \right\rangle
  \;=\;
  \left\vert \psi' \right\rangle
  \mathrlap{\,.}
$$
But by non-degeneracy of the norm this is equivalent to showing
$$
  {
  \Big\Vert
  \phi
  \big(
    \left\vert \psi \right\rangle
    -
    \left\vert \psi' \right\rangle
  \big)
  \Big\Vert
  }
  \,=\,
  0
  \;\;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;\;
  {
  \Big\Vert
    \left\vert \psi \right\rangle
    -
    \left\vert \psi' \right\rangle
  \Big\Vert
  }
  \,=\,
  0
  \mathrlap{\,.}
$$
But since $\phi$ is an isometry, here the left hand side already coincides with the right hand side and hence certainly implies it.
\end{proof}


## Related concepts

* [[isometry]]

* [[linear isomorphism]]

* [[unitary operator]]

## References

See also: 

* ProofWiki, *[Linear Isometry](https://proofwiki.org/wiki/Definition:Linear_Isometry)*

* Wikipedia, *[Linear isometry](https://en.wikipedia.org/wiki/Isometry#Linear_isometry)*

[[!redirects linear isometries]]
