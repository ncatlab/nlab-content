
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc} 

## Idea

The _group algebra_ of a [[group]] $G$ over a [[ring]] $R$ is the [[associative algebra]] whose elements are [[formal linear combinations]] over $R$ of the elements of $G$ and whose multiplication is given on these [[basis]] elements by the group operation in $G$. 



## Definition



### For discrete groups
 {#ForDiscreteGroups}

Let $G$ be a [[discrete group]]. Let $R$ be a [[commutative ring]]. 

+-- {: .num_defn }
###### Definition

The **group $R$-algebra** $R[G]$ is the [[associative algebra]] over $R$ 

1. whose underlying $R$-[[module]] is the the [[free module]] over $R$ on the underlying set of $G$;

1. whose multiplication is given on [[basis]] elements by the group operation.

=--

+-- {: .num_remark }
###### Remark

By the discussion at [[free module]] an element $r$ in $R[G]$ is a [[formal linear combination]] of [[basis]] elements in $G$ with [[coefficients]] in $R$, hence a formal sum

$$
  r = \sum_{g \in G} r_g \cdot g
$$

with $\forall_{g \in G} (r_g \in R)$ and only finitely many of the coefficients different from $0 \in R$.

The addition of algebra elements is given by the componentwise addition of coefficients

$$
  r + \tilde r = 
  \sum_{g \in G} (r_g + \tilde r_g) g
$$

and the multiplication is given by

$$
  \begin{aligned}
    r \tilde r 
    & =
    \sum_{g \in G} 
      \sum_{\tilde g \in G} (r_g \tilde r_{\tilde g}) g \cdot \tilde g
    \\
    & =
    \sum_{q \in G} 
    \left(
      \sum_{k \in G}  (r_{q\cdot k^{-1}} r_k) 
    \right) q
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

The [[formal linear combinations]] over $R$ of element in $G$ may equivalently be thought of as [[functions]]

$$
  r_{(-)} \colon U(G) \to U(R)
$$

from the underlying set of $G$ to the underlying set of $R$ which have _finite support_. Accordingly,  often the underlying set of the group $R$-algebra is written as

$$
  U(R[G]) = Hom_{Set}^{fin\;supp}(U(G), U(R))
$$

and for the [[basis elements]] one writes

$$
  \chi_g \colon U(G) \to U(R)
  \,,
$$

the **characteristic function** of an element $g \in G$, defined by

$$
  \chi_g \colon \tilde g \mapsto
  \left\{
    \array{
      1 & | g = \tilde g
      \\
      0 & | otherwise
    }
  \right.
  \,.
$$

In terms of this the product in the group algebra is called the **[[convolution product]]** on functions. 

=--

+-- {: .num_remark }
###### Remark

The notion of group algebra is a special case of that of a [[groupoid algebra]], hence of [[category algebra]].

=--


###For profinite groups

The completed group ring of a [[profinite group]] is a pseudocompact ring.
Let $\hat{\mathbb{Z}}$ be the [[profinite completion]] of the ring of integers, $\mathbb{Z}$, then $\hat{\mathbb{Z}}$  is itself a [[pseudocompact ring]] as it is the inverse limit of its _finite_ quotients.  Now let $G$ be a profinite group.


The _completed group algebra_, $\hat{\mathbb{Z}}[\![G]\!]$, of $G$ over $\hat{\mathbb{Z}}$ is the inverse limit of the ordinary group algebras, $\hat{\mathbb{Z}}[G/U] $, of the finite quotients, $G/U$ (for $U$ in the directed set, $\Omega(G)$, of open normal subgroups of $G$), over $\hat{\mathbb{Z}}$;

$$\hat{\mathbb{Z}}[\![G]\!] = lim_{U\in \Omega(G)} \hat{\mathbb{Z}}[G/U].$$

For $R$ a pseudocompact ring, it is then easy to construct the corresponding pseudo-compact group algebra of $G$ over $R$; see the paper by Brumer.

### For topological groups
 {#ForTopologicalGroups}

(...)

## Properties

+-- {: .num_prop }
###### Proposition

A group algebra is in particular a [[Hopf algebra]] and a $G$-[[graded algebra]].

=--

The following states a [[universal property]] of the construction of the group algebra.

+-- {: .num_remark}
###### Remark

There is an [[adjunction]]

$$
  (R[-]\dashv (-)^\times)
  \;\colon\; 
  Alg_R 
    \underoverset
      {
        \underset{
          \;\;\;
          (-)^\times
          \;\;\;
        }{
          \longrightarrow
        }
      } 
      {
        \overset{
          \;\;\;
          R[-]
          \;\;\;
        }{
          \leftarrow
        }
      }
      {}
  Grp
$$

between the [[category]] of [[Algebras]] ([[associative algebras]] over $R$) and that of [[Groups]], where $R[-]$ forms [[group rings]] and $(-)^\times$ assigns to an $R$-algebra its [[group of units]].

=--

+-- {: .num_remark}
###### Remark

Let $V$ be an [[abelian group]]. A [[homomorphism]] of rings $R[G] \to End(V)$ of the group ring to the [[endomorphism ring]] of $V$ is equivalently a $R[G]$-[[module]] structure on $V$. 

Any [[homomorphism]] of groups $p \colon G \to Aut(V)$ to the [[automorphism group]] of $V$ extends to to a morphism of rings. 

This observation is used extensively in the theory of [[group representation|group representations]]. See also at _[module -- Abelian groups with G-action as modules over a ring ](http://ncatlab.org/nlab/show/module#AbelianGroupsWithGAction)_.

=--

\begin{prop}\label{ComplexGroupAlgebraOfFiniteGroupAsDirectSumOfEndomorphismAlgebras}
  For $G$ a [[finite group]] with [[isomorphism classes]] of [[irreducible representations]] $[V] \in Irreps_{\mathbb{C}}(G)_{/\sim}$ over the [[complex numbers]], the complex [[group algebra]] of $G$ is [[isomorphism|isomorphic]] to the [[direct sum]] of the linear [[endomorphism algebras]] of the [[complex vector spaces]] underlying the [[irreps]]:
$$
  \mathbb{C}[G]
  \;\simeq\;
  \underset{
    [V] \in Irreps_{\mathbb{C}}(G)_{/\sim}
  }{ \oplus }
  End_{\mathbb{C}}(V)
$$ 
\end{prop}
(e.g. [Fulton-Harris 91, Prop. 3.29](#FultonHarris91))
\begin{proof}
  For every representation $V$, the defining [[group action]]
  $$
    G 
      \overset{}{\longrightarrow} 
    Aut_{\mathbb{C}}(V) 
      \hookrightarrow
    End_{\mathbb{C}}(V)
  $$
  [[extension|extends]] uniquely to an [[algebra homomorphism]]
  $$
    \mathbb{C}[G]
      \overset{ \phi_V }{\longrightarrow} 
    End_{\mathbb{C}}(V)
    \,.
  $$
  Observe that this is a [[surjection]], since if it were not then we could split off a  non-trivial [[cokernel]], contradicting the assumption that $V$ is irreducible.

  We claim that the resulting homomorphism to the [[direct sum]]
  $$
    \mathbb{C}[G]
      \overset{ (\phi_V)_{[V]} }{\longrightarrow} 
    \underset{
      [V] \in Irreps_{\mathbb{C}}(G)_{/\sim}
    }{\oplus} 
    End_{\mathbb{C}}(V)
  $$
  is an [[isomorphism]]: By the previous comment it is sujective, hence it is sufficient to observe that the [[dimension of a vector space|dimension]] of the group algebra equals that of the right hand side, hence that
$$
  dim\big( 
    \mathbb{C}[Sym(G)]
  \big)
  \;=\;
  \underset{[V]}{\sum} \big( dim(V)\big)^2
  \,.
$$ 
This is the case by [this property](regular+representation#RegularRepDecomposedIntoIrreps) of the [[regular representation]].
\end{proof}


+-- {: .num_theorem}
###### Theorem
([[Maschke's theorem]])

Let $G$ be a [[finite group]], let $R = k$ be a field.

Then $k[G]$ is a [[semi-simple algebra]] precisely if the [[order]] of $G$ is not divisible by the [[characteristic]] of k.

=--


## Related concepts

* [[Cohn localization]]

* [[groupoid algebra]], [[category algebra]]

* [[augmentation ideal]]

* [[pseudocompact ring]]

* [[Day convolution]]

* [[∞-group ∞-ring]]

## References

Textbook accounts:

* {#FultonHarris91} [[William Fulton]], [[Joe Harris]], Section 3.4 of: _Representation Theory: a First Course_, Springer, Berlin, 1991 ([doi:10.1007/978-1-4612-0979-9](https://link.springer.com/book/10.1007/978-1-4612-0979-9))

Lecture notes include

* [[Kiyoshi Igusa]], _Algebra II, part D: representations of groups_, ([pdf](http://people.brandeis.edu/~igusa/Math101bS07/Math101b_notesD1a.pdf))   

* Andrei Yafaev, _Group algebras_ ([pdf](http://www.ucl.ac.uk/~ucahaya/GroupAlgebras.pdf))

The [[universal localization]] of group rings (see also at _[[Snaith's theorem]]_) is discussed in

* [[M. Farber]], [[Pierre Vogel]], _The Cohn localization of the free group ring_, Math. Proc.  Camb. Phil. Soc. (1992) 111, 433  ([pdf](http://www.maths.ed.ac.uk/~aar/papers/fv.pdf))

* Davidson, Nicholas, _Modules Over Localized Group Rings for Groups Mapping Onto Free Groups_ (2011). Boise State University Theses and Dissertations. Paper 170. ([web](http://scholarworks.boisestate.edu/td/170/))

For the case of profinite groups, see

* A. Brumer, _Pseudocompact algebras, profinite groups and class formations_,  J. Algebra __4__ (1966) 442-470, [MR202790](http://www.ams.org/mathscinet-getitem?mr=202790), <a href="http://dx.doi.org/10.1016/0021-8693(66)90034-2">doi</a> [pdf](http://deepblue.lib.umich.edu/bitstream/handle/2027.42/33410/0000811.pdf?sequence=1)


[[!redirects group algebras]]

[[!redirects group ring]]
[[!redirects group rings]]



[[!redirects group convolution algebra]]
[[!redirects group convolution algebras]]

