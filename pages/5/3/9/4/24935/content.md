
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

This entry is concerned with [[categories]] $VectBund$ of [[vector bundles]] whose [[morphisms]] are allowed to cover non-trivial [[maps]] between their base spaces.

This means that after choosing a [[ground field]] and an ambient category of [[spaces]] (e.g. [[Sets]] [[TopologicalSpaces]], [[SmoothManifolds]], etc.):

* the [[objects]] of $VectBund$ are [[vector bundles]] over any base space $B$ in the ambient category, which we shall denote like this:

  $$
    \left[  
      \array{
        E
        \\
        \big\downarrow
        \\
        B
      }
    \right]
  $$

* the [[morphisms]] of $VectBund$ are [[commuting squares]] (in the ambient category of spaces) of the form

  $$
      \array{
        E &\overset{\phi}{\longrightarrow}& E'
        \\
        \big\downarrow && \big\downarrow
        \\
        B &\underset{f}{\longrightarrow}& B'
      }
  $$

  which are [[fiber]]-wise [[linear maps]]. 

  Notice here that given the base map $f$, such a diagram is equivalent to a homomorphism of vector bundles over $B$ from $E$ into the [[pullback vector bundle]] $f^\ast E'$, which we may denote by the same symbol $\phi$:

  $$
    \array{
      E && \overset{\phi}{\longrightarrow} && f^\ast E'
      \\
      & \searrow && \swarrow
      \\
      && B
    }
  $$

Accordingly, for each base space $B$ there is a [[full subcategory]]-inclusion

$$
  VectBund(B) 
    \xhookrightarrow{\phantom{--}}
  VectBund
$$


of the category [[VectBund(X)|VectBund(B)]] of vector bundles over $B$,


## Closed monoidal structures
 {#ClosedMonoidalStructures}

For a fixed base space $B$, the [[monoidal category]]-[[structures]] on [[VectBund(B)|$VectBund_B$]] are well known, given [[fiber]]-wise by the respective structures on [[VectorSpaces]]:

* the [[cartesian monoidal structure]] on $VectBund(B)$ is given by [[direct sum of vector bundles]], which in turn is [[fiber]]-wise the [[direct sum]] of [[vector spaces]];

* the other [[symmetric monoidal structure]] on $VectBund(B)$ is given by [[tensor product of vector bundles]], which in turn is [[fiber]]-wise the [[tensor product of vector spaces]].

But analogous -- if subtly different -- monoidal structures exist on the total category $VectBund$, discussed in the following:

* [Cartesian monoidal structure on VectBund](#TensorMonoidalStructur)


* [Tensor monoidal structure on VectBund](#TensorMonoidalStructur).

In discussing this now, we (have to and want to) assume that the ambient [[category]] of [[TopologicalSpaces]] is itself [[cartesian closed category|cartesian closed]] (a "[[convenient category of topological spaces]]"), such as that of [[compactly generated topological spaces]] or of [[D-topological spaces]]. 


### Cartesian monoidal structure
 {#CartesianMonoidalStructure}

The [[cartesian product]] in $VectBund$ is readily checked to be the "external direct sum", namely the result of [[pullback of vector bundles|pulling back]] the two vector bundles to the [[product space]] of their base spaces along the [[projection maps]] 

$$
  \array{
    && 
    B \times B'
    \\
    & \mathllap{ {}^{pr_{B}} }\swarrow 
    && 
    \searrow \mathrlap{  {}^{ pr_{B'} } }
    \\
    B && && B'
  }
$$

and then forming the [[direct sum of vector bundles]] there: 

\[
  \label{CartesianProduct}
  \left[
    \begin{array}{c}
      E
      \\
      \big\downarrow
      \\
      B
    \end{array}
  \right]
  \times
  \left[
    \begin{array}{c}
      E'
      \\
      \big\downarrow
      \\
      B'
    \end{array}
  \right]
  \;\;\simeq\;\;
  \left[
    \begin{array}{c}
      (pr_{B})^\ast E
      \oplus
      (pr_{B'})^\ast {E'}
      \\
      \big\downarrow
      \\
      B \times B'
    \end{array}
  \right]
\]

From this one finds that the cartesian [[mapping space]] ([[internal hom]]) 

$$
  Maps(-,-)
  \;\colon\;
  VectBund^{op}
  \times
  VectBund
  \longrightarrow
  VectBund
$$

is given by forming the vector bundle whose base is the space of vector bundle homomorphisms $\phi$ covering maps of base spaces $f$, and whose fiber over $(f,\phi)$ is (independent of $\phi$ and) given by the [[vector space|vector]]-[[space of sections]] $\Gamma_B(-)$ of the [[pullback vector bundle]] $f^\ast E'$ of the [[codomain]] bundle $E'$ along $f$:

$$
  Maps
  \left(
    \left[
      \begin{array}{c}
        E
        \\
        \big\downarrow
        \\
        B
      \end{array}
    \right]
    \;,\;\;
    \left[
      \begin{array}{c}
        E'
        \\
        \big\downarrow
        \\
        B'
      \end{array}
    \right]
  \right)
  \;\;\simeq\;\;
  \left[
    \begin{array}{c}
      (f,\phi) 
      \mapsto 
      \Gamma_B\big(f^\ast E'\big)
      \\
      \big\downarrow 
      \\
      \left\{
        \array{
          f \colon B \to B',
          \\
          \phi 
          \colon E \underset{lin/B}{\to} f^\ast E'
        }
        \;\;
      \right\}
    \end{array}
  \right]
$$

Namely, one checks the defining [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) 

$$
  Hom
  \big(
    -
    ,\,
    Map(-,-)  
  \big)
  \;\;\simeq\;\;
  Hom
  \big(
    - \times -
    ,\,   
    -
  \big)  
$$


by testing it on vector bundles over the [[point space]] (ignoring the topology for the moment)  and using (eq:CartesianProduct) on the right:

$$
  Hom
  \left(
  \left[
    \begin{array}{c}
      V
      \\
      \big\downarrow
      \\
      \ast
    \end{array}
  \right]
  \;,\;\;
  Maps
  \left(
    \left[
      \begin{array}{c}
        E
        \\
        \big\downarrow
        \\
        B
      \end{array}
    \right]
    \;,\;\;
    \left[
      \begin{array}{c}
        E'
        \\
        \big\downarrow
        \\
        B'
      \end{array}
    \right]
  \right)
  \right)
  \;\; 
  \underoverset
  {\sim}
  {
    \Big(
      v 
        \mapsto
      \big(
        (f,\phi)
        , 
        \sigma_v
      \big)
    \Big)
    \;\mapsto\;
    \big(f, (\phi + \sigma_{(-)}) \big)
  }{\longrightarrow}
  \;\;
  Hom
  \left(
  \left[
    \begin{array}{c}
      E \oplus V
      \\
      \big\downarrow
      \\
      B
    \end{array}
  \right]  
  \;,\;\;
  \left[
    \begin{array}{c}
      E'
      \\
      \big\downarrow
      \\
      B'
    \end{array}
  \right]  
  \right)
$$



### Tensor monoidal structure
 {#TensorMonoidalStructure}

Consider now the [[symmetric monoidal structure]] on $VectBund$ given by the [[external tensor product]]

$$
  \otimes
  \;\colon\;
  VectBund \times VectBund
  \longrightarrow
  VectBund
$$

which itself is constructed by first [[pullback vector bundle|pulling back]] both bundles to the [[product space]] of their base spaces, and then forming their [[tensor product of vector bundles]] there:

\[
  \label{TensorProduct}
  \left[
    \begin{array}{c}
      E
      \\
      \big\downarrow
      \\
      B
    \end{array}
  \right]
  \otimes
  \left[
    \begin{array}{c}
      E'
      \\
      \big\downarrow
      \\
      B'
    \end{array}
  \right]
  \;\;\coloneqq\;\;
  \left[
    \begin{array}{c}
      (pr_{B})^\ast E
      \otimes
      (pr_{B'})^\ast {E'}
      \\
      \big\downarrow
      \\
      B \times B'
    \end{array}
  \right]
\]

The corresponding [[internal hom]]

$$
  LMaps
  \;\colon\;
  VectBund^{op} \times VectBund
  \longrightarrow
  VectBund
$$

forms the vector bundle whose base space is the [[compact-open topology|mapping space]] of base spaces, and whose [[fiber]] over $f \colon B \to B'$ is the [[vector space]] $[E, f^\ast E']_B$ of vector bundle homomorphisms $E \to f^\ast E'$ over $B$:

$$
  LMaps
  \left(
    \left[
      \begin{array}{c}
        E
        \\
        \big\downarrow
        \\
        B
      \end{array}
    \right]
    \;,\;\;
    \left[
      \begin{array}{c}
        E'
        \\
        \big\downarrow
        \\
        B'
      \end{array}
    \right]
  \right)
  \;\;\coloneqq\;\;
  \left[
    \begin{array}{c}
      f
      \mapsto 
      \big[E,  f^\ast E'\big]_B
      \\
      \big\downarrow 
      \\
      \left\{
        \array{
          f \colon B \to B'
        }
        \;\;
      \right\}
    \end{array}
  \right]
$$

To see this, one checks the required hom-isomorphism

$$
  Hom
  \big(
    -
    ,\,
    LMap(-,-)  
  \big)
  \;\;\simeq\;\;
  Hom
  \big(
    - \otimes -
    ,\,   
    -
  \big)  
$$

over the point, now using (eq:TensorProduct) on the right: 

$$
  Hom
  \left(
  \left[
    \begin{array}{c}
      V
      \\
      \big\downarrow
      \\
      \ast
    \end{array}
  \right]
  \;,\;\;
  LMaps
  \left(
    \left[
      \begin{array}{c}
        E
        \\
        \big\downarrow
        \\
        B
      \end{array}
    \right]
    \;,\;\;
    \left[
      \begin{array}{c}
        E'
        \\
        \big\downarrow
        \\
        B'
      \end{array}
    \right]
  \right)
  \right)
  \;\; 
  \underoverset
  {\sim}
  {
    \Big(
      v 
        \mapsto
      \big(f, \sigma_v\big)
    \Big)
    \;\mapsto\;
    \big(f, \sigma_{(-)} \big)
  }{\longrightarrow}
  \;\;
  Hom
  \left(
  \left[
    \begin{array}{c}
      E \otimes V
      \\
      \big\downarrow
      \\
      B
    \end{array}
  \right]  
  \;,\;\;
  \left[
    \begin{array}{c}
      E'
      \\
      \big\downarrow
      \\
      B'
    \end{array}
  \right]  
  \right)
$$


## Related concepts

* [[Mod]]

* [[VectBund(B)]]

* [[tangent (infinity,1)-category|tangent $\infty$-category]]

* [[parameterized spectra]]

* [[doubly closed monoidal category]]


[[!redirects VectorBundles]]
