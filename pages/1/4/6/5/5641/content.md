+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _chain homotopy_ is a [[homotopy]] in a [[category of chain complexes]] with respect to the standard [[interval object in chain complexes]].

Sometimes a chain homotopy is called a _homotopy operator_. This is the terminology common for instance in the [standard proof](Poincare+lemma#Statement) of the [[Poincaré lemma]].

## Definition

Let $\mathcal{A} = $ [[Ab]] be the [[abelian category]] of [[abelian groups]]. Write $Ch_\bullet(\mathcal{A})$ for the [[category of chain complexes]] in $\mathcal{A}$.

A chain homotopy is a [[homotopy]] in $Ch_\bullet(\mathcal{A})$. We first give the explicit definition, the more abstract characterization is below in prop. \ref{AsALeftHomotopy}.

+-- {: .num_defn}
###### Definition

A _chain homotopy_ $\psi : f \Rightarrow g$ between two [[chain maps]] $f,g : C_\bullet \to D_\bullet$ in $Ch_\bullet(\mathcal{A})$ is a sequence of morphisms

$$
  \{ (\psi_n : C_n \to D_{n+1}) \in \mathcal{A} | n \in \mathbb{N} \}
$$

in $\mathcal{A}$ such that 

$$
  f_n - g_n = \partial^D \circ  \psi_n + \psi_{n-1} \circ \partial^C
  \,.
$$

=--


+-- {: .num_remark}
###### Remark

It may be useful to illustrate this with the following graphics, which however is _not_ a [[commuting diagram]]:

$$
  \array{
    \vdots && \vdots
    \\
    \downarrow && \downarrow
    \\
    C_{n+1} &\stackrel{f_{n+1} - g_{n+1}}{\to}& D_{n+1}
    \\
    \downarrow^{\mathrlap{\partial^C_{n}}} 
    &\nearrow_{\mathrlap{\psi_{n}}}& 
    \downarrow^{\mathrlap{\partial^D_{n}}}
    \\
    C_n &\stackrel{f_n - g_n}{\to}& D_n
    \\
    \downarrow^{\mathrlap{\partial^C_{n-1}}} 
    &\nearrow_{\mathrlap{\psi_{n-1}}}& 
    \downarrow^{\mathrlap{\partial^D_{n-1}}}
    \\
    C_{n-1} &\stackrel{f_{n-1} - g_{n-1}}{\to}& D_{n-1}
    \\
    \downarrow && \downarrow
    \\
    \vdots && \vdots
  }
  \,.
$$

=--

Instead, a way to encode chain homotopies by genuine diagrammatics is below in prop. \ref{AsALeftHomotopy}.


## Properties

### In terms of general homotopy
 {#RelationToLeft}

+-- {: .num_defn}
###### Definition

Let 

$$
  I_\bullet \coloneqq N_\bullet(C(\Delta[1]))
$$

be the [[normalized chain complex]] in $\mathcal{A}$ of the [[chain on a simplicial set|simplicial chains]] on the simplicial 1-[[simplex]]:

$$
  I_\bullet = 
  [
    \cdots \to 0 \to 0 \to \mathbb{1} \stackrel{(id,-id)}{\to}
   \mathbb{1} \oplus \mathbb{1}
  ]
  \,.
$$

=--

This is the standard [[interval in chain complexes]]. Indeed it is manifestly the "abelianization" of the standard interval object in [[sSet]]/[[Top]]. 


+-- {: .num_prop #AsALeftHomotopy}
###### Proposition

A chain homotopy $\psi : f \Rightarrow g$ is equivalently a [[commuting diagram]]

$$
  \array{
    C_\bullet
    \\
    \downarrow & \searrow^{\mathrlap{f}}
    \\
    I_\bullet\otimes C_\bullet  
    &\stackrel{(f,g,\psi)}{\to}&
    D_\bullet
    \\
    \uparrow & \nearrow_{\mathrlap{g}}
    \\
    C_\bullet
  }
$$

in $Ch_\bullet(\mathcal{A})$, hence a genuine [[left homotopy]] with respect to the [[interval object in chain complexes]].

=--

+-- {: .proof}
###### Proof

For notational simplicity we discuss this in $\mathcal{A} = $ [[Ab]].

Observe that $N_\bullet(\mathbb{Z}(\Delta[1]))$ is the chain complex

$$
  (  \cdots  \to 0   \to 0 \to \mathbb{Z} \stackrel{(id,-id)}{\to}  \mathbb{Z} \oplus \mathbb{Z} \to 0 \to 0 \to \cdots)
$$

where the term $\mathbb{Z} \oplus \mathbb{Z}$ is in degree 0: this is the [[free abelian group]] on the set $\{0,1\}$ of 0-simplices in $\Delta[1]$. The other copy of $\mathbb{Z}$ is the free abelian group on the single non-degenerate edge in $\Delta[1]$. All other cells of $\Delta[1]$ are degenerate and hence do not contribute to the [[normalized chain complex]]. The single nontrivial [[differential]] sends $1 \in \mathbb{Z}$ to $(1,-1) \in \mathbb{Z} \oplus \mathbb{Z}$, reflecting the fact that one of the vertices is the 0-[[boundary]] and the other is the 1-boundary of the single nontrivial edge.

It follows that the [[tensor product of chain complexes]] $I_\bullet \otimes C_\bullet$ is

$$
  \cdots
  \to 
  C_2 \oplus C_{2} \oplus C_1
  \to C_1 \oplus C_{1} \oplus C_0 \to  C_0 \oplus C_0 \oplus C_{-1} \to \cdots
 \,.
$$

Therefore a chain map $(f,g,\psi) :  C_\bullet \otimes I_\bullet \to D_\bullet$ that restricted to the two copies of $C_\bullet$ is $f$ and $g$, respectively,  is characterized by a collection of commuting diagrams

$$
  \array{
    C_{n+1}\oplus C_{n+1} \oplus C_{n} 
      &\stackrel{(f_{n+1},g_{n+1}, \psi_n)}{\to}& D_{n+1}
    \\
    {}^{\mathllap{}}\downarrow && \downarrow^{\mathrlap{\partial^D}}
    \\
     C_{n} \oplus C_{n} \oplus C_{n-1} &\stackrel{(f_n,g_n,\psi_{n-1})}{\to}
    & 
    D_n
  }
  \,.
$$

On the elements $(1,0,0)$ and $(0,1,0)$ in the top left this reduces to the chain map condition for $f$ and $g$, respectively. On the element $(0,0,1)$ this is the equation for the chain homotopy

$$
  f_n - g_n - \psi_{n-1} d_C = d_D \psi_{n}
  \,.
$$

=--

### Homotopy equivalence

Let $C_\bullet, D_\bullet \in Ch_\bullet(\mathcal{A})$
be two chain complexes.

+-- {: .num_defn }
###### Definition

Define the [[relation]] _chain homotopic_ on 
$Hom(C_\bullet, D_\bullet)$ by

$$
  (f \sim g)
    \Leftrightarrow
  \exists (\psi : f \Rightarrow g)
  \,.
$$


=--

+-- {: .num_prop }
###### Proposition

Chain homotopy is an [[equivalence relation]] on $Hom(C_\bullet,D_\bullet)$.

=--

+-- {: .num_prop }
###### Proposition

Write $Hom(C_\bullet,D_\bullet)_{\sim}$ for the [[quotient]] of the [[hom set]] $Hom(C_\bullet,D_\bullet)$ by chain homotopy.

=--

+-- {: .num_prop }
###### Proposition

This quotient is compatible with [[composition]] of [[chain maps]].

=--

Accordingly the following [[category]] exists:

+-- {: .num_defn }
###### Definition

Write $\mathcal{K}(\mathcal{A})$ for the category whose
[[objects]] are those of $Ch_\bullet(\mathcal{A})$, and whose [[morphisms]]
are chain homotopy classes of chain maps:

$$
  Hom_{\mathcal{K}(\mathcal{A})}(C_\bullet, D_\bullet)
  \coloneqq
  Hom_{Ch_\bullet(\mathcal{A})}(C_\bullet, D_\bullet)_\sim
  \,.
$$

This is usually called the **[[homotopy category of chain complexes]]**
in $\mathcal{A}$. 

=--

+-- {: .num_remark }
###### Remark

Beware, as discussed there, that another category that would deserve to 
carry this name instead is called the _[[derived category]]_ of $\mathcal{A}$.
In the derived category one also quotients out chain homotopy, but one allows that first the [[domain]] of the two chain maps $f$ and $g$ is refined along a [[quasi-isomorphism]]. 

=--


## Related concepts

* [[null homotopy]]

* [[category of chain complexes]]

  * [[chain complex]]

  * [[chain map]], [[quasi-isomorphism]]

  * **chain homotopy**

* [[homotopy category of chain complexes]]
  
## References

Historical articles:

* Tibor Rado , *A Remark on Chain-Homotopy*, Proceedings of the American Mathematical Society Vol. 2, No. 3 (Jun., 1951), pp. 458-463 ([jstor:2031776](https://www.jstor.org/stable/2031776), [doi:10.2307/2031776](https://doi.org/10.2307/2031776))


Review:

* [[Charles Weibel]], Section 1.4 of: _[[An Introduction to Homological Algebra]]_

[[!redirects cochain homotopy]]
[[!redirects chain homotopies]]
[[!redirects cochain homotopies]]

[[!redirects homotopy operator]]
[[!redirects homotopy operators]]
