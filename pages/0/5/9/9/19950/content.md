

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The [[Bredon cohomology]]-[[equivariant cohomology|equivariant]] enhancement of [[cohomotopy]]-theory is _equivariant cohomotopy_: 

For $G$ a [[group]], $V$ a [[finite dimensional vector space|finite-dimensional]] [[real vector space|real]]  $G$-[[representation]] $G \to O(V)$ and writing $S^V$ for the corresponding [[representation sphere]], the _equivariant cohomotopy_ in [[RO(G)-degree]] $V$ of a [[G-space]] $X$ is the set of $G$-[[equivariant homotopy theory|equivariant]] [[homotopy classes]] of maps from $X$ to $S^V$:

$$
  \pi_G^V\big( X \big)
  \;\coloneqq\;
  \left[
    X, S^V
  \right]^G
  \,.
$$

For $V = \mathbb{R}^n$ the [[trivial representation]] of [[dimension]] $n$, this reduces to the definition of plain [[cohomotopy]]-sets

$$
  \pi^{\mathbb{R}^n}(X)
  \;=\;
  \pi^n(X)
  \;=\;
  \left[ X, S^n\right]
  \,.
$$


The [[stabilization]] of this construction, in the sense of [[equivariant stable homotopy theory]], yields the concept of _[[equivariant stable cohomotopy]]_.


## Properties

### Equivariant Hopf degree theorem

* [[equivariant Hopf degree theorem]]


## Examples

### Equivariant Cohomotopy of $S^V$ in RO-degree $V$

As a special case of the [[equivariant Hopf degree theorem]] , we obtain the following:


+-- {: .num_example #EquivariantHomotopyOfSVInRODegreeV}
###### Proposition
**([[equivariant cohomotopy]] of [[representation sphere]] $S^V$ in [[RO(G)-degree]] $V$)**


  Let $G \in \mathrm{Grp}_{\mathrm{fin}}$
  and $V \in \mathrm{RO}(G)$ with $V^G = 0$.
  Then the bipointed [[equivariant cohomotopy]] 
  of the [[representation sphere]] $S^V$ 
  in [[RO(G)-degree]] $V$ is
  the [[Cartesian product]] of one copy of the [[integers]] for
  each [[isotropy group|isotropy]] subgroup (eq:IsotropySubgroups) of $G$ in $S^V$
  except the full subgroup $G \subset G$

$$
  \array{
      \pi^V\left( S^V\right)^{\{0,\infty\}/}
      &
        \overset{\simeq}{\longrightarrow}
      &
      \underset{
        {
          {
              {H \in \mathrm{Isotr}_{S^V}(G)}
              \atop
              {H \neq G}
          }
        }
      }{\prod}
      \;\;
      {\vert W_G(H)\vert } \cdot \mathbb{Z}
      \\
      \big[
        S^V
          \overset{c}{\longrightarrow}
        S^V
      \big]
      &\mapsto&
      \Big(
        H 
          \mapsto
        \mathrm{deg}
        \big(
          c^H
        \big)
        -
        \mathrm{offs}(c,H)
      \Big)
  }
$$
  where on the right 
  $$
    \mathrm{deg}
    \Big(
      \big(
        S^V
      \big)^H
      \overset{
        c^H
      }{\longrightarrow}
      \big(
        S^V
      \big)^H
    \Big)
    \in \mathbb{Z}
  $$
  is the [[integer]] [[winding number]] of the underlying [[continuous function]]
  of $c$ ([[corestriction|co]])[[restriction|restricted]] to $H$-[[fixed points]], and part of the claim is  that this is an integer multiple of the order of the [[Weyl group]] $W_G(H)$ up to an offset

$$
  \mathrm{offs}(f,H) 
  \;\in\; 
  \big\{
    0,1, \cdots,  \left\vert W_G(H)\right\vert
  \big\}
  \;\subset\;
  \mathbb{Z}
$$

which depends in a definite way on the degrees of $c^K$ for  all isotropy groups $K \gt H$.

=--

For **[[proof]]** see [here](Hopf+degree+theorem#EquivariantHomotopyOfSVInRODegreeV) at _[[equivariant Hopf degree theorem]]_.


+-- {: .num_example #EquivariantCohomotopyOfRepresentationSphereOfSignRepresentationInThatDegree}
###### Example
**([[equivariant cohomotopy]] of $S^{\mathbb{R}_{sgn}}$ in [[RO(G)-degree]] the [[sign representation]] $\mathbb{R}_{sgn}$)**

Let $G = \mathbb{Z}_2$ the [[cyclic group of order 2]] and $\mathbb{R}_{sgn} \in RO(\mathbb{Z}_2)$ its 1-dimensional [[sign representation]]. 

Under equivariant [[stereographic projection]] ([here](representation\+sphere#Construction)) the corresponding [[representation sphere]] $S^{\mathbb{R}_{sgn}}$ is equivalently the [[unit circle]]

$$
  S^1 
  \simeq 
  S(\mathbb{R}^2)
$$ 

equipped with the $\mathbb{Z}_2$-[[action]] whose [[involution]] element $\sigma$ [[reflection|reflects]] one of the two [[coordinate functions|coordinates]] of the ambient [[Cartesian space]] 

$$
  \sigma \;\colon\; (x_1,x_2) \mapsto (x_1, -x_2)
  \,.
$$

Equivalently, if we identify 

\[
  \label{CircleAsQuaotientOfRByZ}
  S^1
  \;\simeq\;
  \mathbb{R}/\mathbb{Z}
\]

then the involution action is

$$
  \begin{aligned}
    \sigma
    \;\colon\;
    t 
    \mapsto
    &
    \phantom{\sim}
    1 - t 
    \\
    & \sim
    \phantom{1} - t
  \end{aligned} 
  \,.
$$

This means that the [[fixed point space]] is the [[0-sphere]]

$$
  \big( S^1\big)^{\mathbb{Z}_2}
  \;\simeq\;
  S^0
$$

being two antipodal points on the circle, which in the presentation (eq:CircleAsQuaotientOfRByZ) are labeled $\{0,1/2\} \simeq S^0$.

Notice that the map

\[
  \label{ConstantParameterFunctionFromSignRepresentationSphereToItself}
  \array{
    S^1 &\overset{n}{\longrightarrow}& S^1
    \\
    t &\mapsto& n\cdot t
  }
\]

of constant parameter speed and [[winding number]] $n \in \mathbb{N}$ is equivariant for this $\mathbb{Z}_2$-[[action]] on both sides:

\begin{center}
\begin{xymatrix}
  t 
    \ar@{|->}[r] 
    \ar@{|->}[d]_{\sigma}
    & 
  n\cdot t
    \ar@{|->}[d]^{\sigma}
  \\
  -t 
    \ar@{|->}[r] 
    & 
  -n \cdot t
\end{xymatrix}
\end{center}

Now the restriction of the map $n \cdot (-)\in \mathbb{Z}$ from (eq:ConstantParameterFunctionFromSignRepresentationSphereToItself) to the [[fixed points]] 

$$
  \array{
    S^0 = \left( S^{\mathbb{R}_{sgn}}\right) 
    &\hookrightarrow&
    S^{\mathbb{R}_{sgn}}
    \\
    {}^{ \mathllap{  \left( \cdot n\right)^{\mathbb{Z}_2} } }
    \big\downarrow 
      && 
    \big\downarrow^{\mathrlap{\cdot n}}
    \\
    S^0 = \left( S^{\mathbb{R}_{sgn}}\right) 
    &\hookrightarrow&
    S^{\mathbb{R}_{sgn}}
  }
$$

sends (0 to 0 and) $1/2$ to either $1/2$ or to $0$, depending on whether the [[winding number]] is [[odd number|odd]] or [[even number|even]]:

$$
  \array{
     S^0 
       &\overset{ \left(\cdot n\right)^{\mathbb{Z}_2} }{\longrightarrow}&
     S^0
     \\
     1/2 &\mapsto&
     \left\{
       \array{
         1/2 &\vert& n \;\text{is odd}
         \\
         0 &\vert& n \text{is even}
       }
     \right.
  }
$$

Hence if the restriction to the [[fixed locus]] is taken to be the [[identity function|identity]] (bipointed [[equivariant cohomotopy]]) then, in accord with Prop. \ref{EquivariantHomotopyOfSVInRODegreeV} there remains the [[integers]] worth of equivariant [[homotopy classes]], where each integer $k \in \mathbb{Z}$ corresponds to the odd winding integer $1 + 2k$

$$
  \array{
    \pi^{\mathbb{R}_{sgn}}
    \left(
      S^{\mathbb{R}_{sgn}}
    \right)^{\{0,\infty\}/}
    &\simeq&
    2 \cdot \mathbb{Z} + 1 
    &\simeq& 
   \mathbb{Z}
    \\
    \left[
      \mathbb{R}/\mathbb{Z} \overset{c}{\to} \mathbb{R}/\mathbb{Z}
    \right]_{{0 \mapsto 0} \atop {1/2 \mapsto 1/2}}
    &\mapsto&
    deg(c)
    &\mapsto&
    \big( deg(c) - 1\big)/2
  }
$$

=--


+-- {: .num_example #EquivariantCohomotopyOfRepresentationSphereOfQuaternionsInThatDegree}
###### Example
**([[equivariant cohomotopy]] of $S^{\mathbb{H}}$ in [[RO(G)-degree]] the [[quaternions]] $\mathbb{H}$)**

Let $G \subset SU(2) \simeq S(\mathbb{H})$ be a non-[[trivial group|trivial]] [[finite subgroup of SU(2)]] and let $\mathbb{H} \in RO(G)$ be the [[real vector space]] of [[quaternions]] regarded as a [[linear representation]] of $G$ by left multiplication with unit [[quaternions]].

Then the bi-pointed [[equivariant cohomotopy]] of the [[representation sphere]] $S^{\mathbb{H}}$ in [[RO(G)-degree]] $\mathbb{H}$ is

$$
  \array{
    \pi^{\mathbb{H}}
    \left(
      S^{\mathbb{H}} 
    \right)^{\{0,\infty\}/}
    &\simeq&
    {\left\vert G\right\vert} \cdot \mathbb{Z} + 1
    &\simeq& 
    {\left\vert G\right\vert} \cdot \mathbb{Z}
    &\simeq& 
    \mathbb{Z}    
    \\
    \left[   
      S^{\mathbb{H}}
      \overset{c}{\longrightarrow}
       S^{\mathbb{H}}
    \right]
    &\mapsto&
    deg\left( c^{ \{e\}  }\right)
    &\mapsto&
    deg\left( c^{ \{e\}  }\right) - 1
    &\mapsto&
    \big( 
      deg\left( c^{ \{e\}  }\right) - 1
    \big)/ {\left\vert G\right\vert}
  }
$$


=--

+-- {: .proof}
###### Proof

The only [[isotropy groups|isotropy]] [[subgroups]] of the left action of $G$ on $\mathbb{H}$ are the two extreme cases $Isotr_{\mathbb{H}}(G) = \{1, G\} \in Sub(G)$. Hence the only multiplicity that appears in Prop. \ref{EquivariantHomotopyOfSVInRODegreeV} is 

$$
  \left\vert W_G(1)\right\vert 
  \;=\;
  \left\vert G \right\vert   
  \,.
$$

and all degrees  must differ from that of the class of the [[identity function]] by a multiple of this multiplicity. Finally, the offset of the identity function is clearly $offs\left(id_{S^{\mathbb{H}}},1\right) = deg\left( id_{S^{\mathbb{H}}}\right) = 1$.

=--


## Related concepts

[[!include flavours of cohomotopy -- table]]

* [[equivariant Hopf degree theorem]]

* [[equivariant Pontrjagin theorem]]

<br/>

## References

### General

* {#Wasserman69} [[Arthur Wasserman]], section 3 of _Equivariant differential topology_, Topology Vol. 8, pp. 127-150, 1969 ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/wasserman.pdf))


* {#tomDieck79} [[Tammo tom Dieck]], section 8.4 of _[[Transformation Groups and Representation Theory]]_, Lecture Notes in Mathematics 766 Springer 1979

* {#Peschke94} [[George Peschke]], _Degree of certain equivariant maps into a representation sphere_, Topology and its Applications Volume 59, Issue 2, 30 September 1994, Pages 137-156 (<a href="https://doi.org/10.1016/0166-8641(94)90091-4">doi:10.1016/0166-8641(94)90091-4</a>)

* Zalman Balanov, _Equivariant hopf theorem_, Nonlinear Analysis: Theory, Methods & Applications Volume 30, Issue 6, December 1997, Pages 3463-3474 (<a href="https://doi.org/10.1016/S0362-546X(97)00020-5">doi:10.1016/S0362-546X(97)00020-5</a>)

* {#Cruickshank03} [[James Cruickshank]], _Twisted homotopy theory and the geometric equivariant 1-stem_, Topology and its Applications Volume 129, Issue 3, 1 April 2003, Pages 251-271 (<a href="https://doi.org/10.1016/S0166-8641(02)00183-9">doi:10.1016/S0166-8641(02)00183-9</a>)

* Davide L. Ferrario, _On the equivariant Hopf theorem_, _Topology
Volume 42, Issue 2, March 2003, Pages 447-465_ (<a href="https://doi.org/10.1016/S0040-9383(02)00015-0">doi:10.1016/S0040-9383(02)00015-0</a>)


### Cocycle spaces

Discussion of [[cocycle spaces]] in equivariant Cohomotopy:

* [[Victor Vassiliev]], _Twisted homology of configuration spaces, homology of spaces of equivariant maps, and stable homology of spaces of non-resultant systems of real homogeneous polynomials_ ([arXiv:1809.05632](https://arxiv.org/abs/1809.05632))


### For M-brane charge quantization

Discussion of [[M-brane]] [[charge quantization]] in [[equivariant cohomotopy]]:

* [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_, Comm. Math. Phys. 371: 425. (2019) ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987))

  ([[equivariant rational homotopy theory|equivariant]] [[rational Cohomotopy]])

* {#SatiSchreiber19} [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]], _[[schreiber:Equivariant Cohomotopy implies orientifold tadpole cancellation]]_ ([arXiv:1909.12277](https://arxiv.org/abs/1909.12277))

  (implying [[RR-field tadpole cancellation]])

[[!redirects equivariant Cohomotopy]]

[[!redirects equivariant cohomotopy theory]]
[[!redirects equivariant Cohomotopy theory]]


