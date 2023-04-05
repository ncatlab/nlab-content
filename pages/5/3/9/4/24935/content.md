
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

Consider now the [[symmetric monoidal structure]] on $VectBund$ given by the [[external tensor product]] [[external tensor product of vector bundles|of vector bundles]]

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

### Distributive monoidal structure
 {#
}

With respect to the [[coproduct]] and the [[external tensor product]] [[external tensor product of vector bundles|of vector bundles]], $VectBund$ is a [[distributive monoidal category]]. We spell this out in detail for the case of [[discrete topological space|discrete]] base spaces (sets):

\begin{definition}
  For any [[ground field]], write [[VectBund|$Vect_{Set}$]] for the [[category]] of [[indexed sets]] of [[vector spaces]].
\end{definition}
\begin{remark}
We may and will present [[objects]] $\mathcal{V}$ of [[VectBund|$Vect_{Set}$]] as [[pairs]] consisting of a [[set]] $S$ and a [[function]] $\mathcal{V}_{(-)}$ (really a [[functor]] on the [[discrete category]] on $S$) to [[Vect]]:
$$
  \left(
    \array{
      S &\longrightarrow& Vect
      \\
      s &\mapsto& \mathcal{V}_s
    }
  \right)
  \;\;
  \in
  \;\;
  Vect_{Set}
  \mathrlap{\,.}
$$
\end{remark}

\begin{definition}
\label{ExternalTensorProductInVectSet}
The "[[external tensor product|external]]" [[tensor product]]  on [[VectBund|$Vect_{Set}$]] is the [[functor]] 
$$
  \boxtimes
  \,\colon\,
  Vect_{Set} \times VectSet 
    \longrightarrow
  Vect_{Set}
$$
given by
$$
  \big(
    \mathcal{V}_{(-)} \,\colon\, S \to \Vect
  \big)
  \,\boxtimes\,
  \big(
    \mathcal{V}'_{(-)} \,\colon\, S' \to \Vect
  \big)
  \;\;
  \coloneqq
  \;\;
  \left(
    \array{
      S \times S' &\longrightarrow& \Vect
      \\
      (s, s') 
        &\mapsto& 
      \mathcal{V}_s \otimes \mathcal{V}'_{s'}
    }
  \right)
  \mathrlap{\,.}
$$
\end{definition}

\begin{proposition}
\label{CoproductInVectSet}
  The [[coproduct]] in [[VectBund|$Vect_{Set}$]] is given by [[disjoint union]] of [[bundles]]:
$$
  \big(
    \mathcal{V}^{(1)}_{(-)} \,\colon\, S_1 \to \Vect
  \big)
  \;
  \sqcup
  \;
  \big(
    \mathcal{V}^{(1)}_{(-)} \,\colon\, S_2 \to \Vect
  \big)
  \;\;
  \simeq
  \;\;
  \left(
    \array{
      S_1 \sqcup S_2 &\longrightarrow& \Vect
      \\
      s_i &\mapsto& \mathcal{V}^{(i)}_{s_i}
    }
  \right)
$$
\end{proposition}
\begin{proof}
  It is immediate to check the [[universal property]] characterizing the coproduct.
\end{proof}

\begin{proposition}
The [[external tensor product]] $\boxtimes$ 
(Def. \ref{ExternalTensorProductInVectSet})
[[distributive monoidal category|distributes]] over the coproduct (Prop. \ref{CoproductInVectSet}):
$$
  \mathcal{E} \boxtimes ( \mathcal{V}^{(1)} \sqcup  \mathcal{V}^{(2)}) 
  \;\simeq\;
  \big(  
    \mathcal{E} \boxtimes \mathcal{V}^{(1)}
  \big)
  \,\sqcup\,
  \big(
    \mathcal{E} \boxtimes \mathcal{V}^{(2)}
  \big)
$$
and hence gives a [[distributive monoidal category]]:
$$
  \big(
    Vect_{Set}
    ,
    \sqcup
    ,
    \boxtimes
  \big)
  \;\in\;
  DistMonCat
  \mathrlap{\,.}
$$
\end{proposition}
\begin{proof}
Unwinding the above definitions and using that [[Set]] is a [[distributive category]], we have the following sequence of [[natural isomorphisms]]:
$$
  \begin{array}{l}
    \mathcal{E} 
    \,\boxtimes\,
    \big(
      \mathcal{V}^{(1)}
      \,\sqcup\,
      \mathcal{V}^{(2)}
    \big)
    \\
    \;\equiv\;
    \big(
      \mathcal{E}_{(-)} \,\colon\, S_E \to Vect
    \big)
    \,\boxtimes\,
    \Big(
      \big(
        \mathcal{V}^{(1)}_{(-)} \,\colon\, S_1 \to Vect
      \big)
      \,\sqcup\,
      \big(
        \mathcal{V}^{(2)}_{(-)} \,\colon\, S_2 \to Vect
      \big)
    \Big)
    \\
    \;\simeq\;
    \big(
      \mathcal{E}_{(-)} \,\colon\, S_E \to Vect
    \big)
    \,\boxtimes\,
    \left(
      \array{
        S_1 \sqcup S_2 &\longrightarrow& Vect
        \\
        s_i &\mapsto& \mathcal{V}^{(i)}_{s_i}
      }
    \right)
    \\
    \;\simeq\;
    \left(
      \array{
        S_E \times (S_1 \sqcup S_2)
        &\longrightarrow& Vect
        \\
        (s_E , s_i) &\mapsto&
        \mathcal{E}_{s_E} \otimes \mathcal{V}^{(i)}_{s_i}
      }
    \right)
    \\
    \;\simeq\;
    \left(
      \array{
        (S_E \times S_1) \,\sqcup\, (S_2 \times S_2)
        &\longrightarrow& Vect
        \\
        (s_E , s_i) &\mapsto&
        \mathcal{E}_{s_E} \otimes \mathcal{V}^{(i)}_{s_i}
      }
    \right)
    \\
    \;\simeq\;
    \left(
      \array{
        S_E \times S_1 
        &\longrightarrow& Vect
        \\
        (s_E , s_1) 
         &\mapsto&
        \mathcal{E}_{s_E} \otimes \mathcal{V}^{(1)}_{s_1}
      }
    \right)
    \,\sqcup\,
    \left(
      \array{
        S_E \times S_2 
        &\longrightarrow& Vect
        \\
        (s_E , s_2) 
         &\mapsto&
        \mathcal{E}_{s_E} \otimes \mathcal{V}^{(2)}_{s_2}
      }
    \right)
    \\
    \;\equiv\;
    \mathcal{E} \boxtimes \mathcal{V}^{(1)}
    \,\sqcup\,
    \mathcal{E} \boxtimes \mathcal{V}^{(2)}
  \end{array}
$$
\end{proof}



### Amalgamation of monoidal and parameter structures
 {#AmalgamationOfMonoidalAndParameterStructures}

> under construction

We want to point out a way in which $VectBund$ with its [[external tensor product]]-structure is the canonical "amalgamation" of 

1. vector spaces equipped with theiry tensor product 

1. vector spaces equipped with parametrization, namely vector bundles

at least in the case that the base space is discrete.

In order to formalize this idea, we need to work inside a [[2-category]] which suitably subsumes all of the following

[[very large category|very large]] [[(2,1)-categories]]:

* $Cat$ of [[categories]] 

* $MonCat$ of [[monoidal categories]];

* $CoCartCart$ of [[cocartesian monoidal categories]];

* $DistMonCat$ of [[distributive monoidal categories]] (with [[underlying]] [[cocartesian monoidal categories]]).

Here we understand that 

* the [[1-morphisms]] in these [[2-categories]] are [[functors]] which respect all given [[tensor products]] up to [[isomorphism]], i.e. [[strong monoidal functors]]

* the [[2-morphisms]] are [[natural isomorphisms]] between these functors.

The system of [[forgetful functor|forgetful]] [[2-functors]] between these [[(2,1)-categories]] forms a square [[diagram]] which we may regard as the [[image]] of a corresponding [[contravariant functor|contravariant]] [[pseudofunctor]] from the [[commuting square]]-[[diagram category]] to [[2Cat]]:


$$
  \mathbf{C}
  \;\;
    \colon
  \;\;
  \array{
    (1,0) &\longrightarrow& (1,1)
    \\
    \big\downarrow && \big\downarrow
    \\
    (0,0) &\longrightarrow& (1,0)
  }
  \;\;\;\;
    \mapsto
  \;\;\;\;
  \array{
     MonCat &\longleftarrow& DistMonCat
     \\
     \big\downarrow && \big\downarrow
     \\
     Cat &\longleftarrow& CoCartCat
  }
$$

The 2-categorical context which we are after is then the [[(infinity,1)-Grothendieck construction|(2,1)-]][[Grothendieck construction]] $\int \mathbf{C}$ on this [[pseudofunctor]]: Here [[1-morphisms]] are functors which strictly preserve the [[tensor products]] present on their [[domain]] category, but whose [[codomain]] may be equipped with further [[tensor products]] (though not with fewer tensor products).

**Claim.** In $\int \mathbf{C}$ the following [[diagram]] is a ([[homotopy pushout|homotopy]]) [[pushout]]

\begin{tikzcd}
  \big(
    \mathrm{Vect}
    , 
    \otimes
  \big)
  \ar[rr]
  &&
  \big(
    \mathrm{Vect}_{\mathrm{Set}}
    ,
    \sqcup
    , 
    \boxtimes
  \big)
  \\
  \mathrm{Vect}
  \ar[u]
  \ar[
    rr
  ]
  &&
  \big(
    \mathrm{Vect}_{\mathrm{Set}}
    ,
    \sqcup
  \big)
  \ar[u]
\end{tikzcd}


\begin{proof}
We check the [[universal property]]. To this end, observe that any [[cocone]] under the diagram must have as tip a [[distributive monoidal category]], since only these can receive morphisms in $\int \mathbf{C}$ both from a monoidal and from a cocartesian category.

This means that a general [[cocone]] looks like the following solid diagram:

\begin{tikzcd}
  && 
  &[-10pt]
  \big(
    \mathcal{C}
    ,
    \sqcup
    ,
    \otimes
  \big)
  \\[-10pt]
  \big(
    \mathrm{Vect}
    , 
    \otimes
  \big)
  \ar[rr]
  \ar[urrr]
  &&
  \big(
    \mathrm{Vect}_{\mathrm{Set}}
    ,
    \sqcup
    , 
    \boxtimes
  \big)
  \ar[
    ur,
    dashed
  ]
  \\
  \mathrm{Vect}
  \ar[u]
  \ar[
    rr
  ]
  &&
  \big(
    \mathrm{Vect}_{\mathrm{Set}}
    ,
    \sqcup
  \big)
  \ar[u]
  \ar[uur]
\end{tikzcd}

We need to see that this uniquely admits the dashed arrow. Unwinding the definitions, the existence of the dashed arrow means that any functor $F \,\colon\, Vect_{Set} \to \mathcal{C}$ which preserves both the coproduct of vector bundles as well as the tensor product on fibers already respects the [[external tensor product]]. But this follows by the [[distributive monoidal category|distributivity]] and using that any [[set]] is the [[coproduct]] of its elements:

$$
  \begin{array}{l}
    F\big( \mathcal{E} \boxtimes \mathcal{E}' \big)
    \\
    \;\simeq\;
    F
    \Bigg(
      \underset{s \in S}{\coprod} 
      \left(
        \array{
          \{s\} &\longrightarrow& Vect
          \\
          s &\mapsto& \mathcal{E}_s 
        }
      \right)
      \;\;
      \boxtimes
      \;\;
      \underset{s' \in S'}{\coprod} 
      \left(
        \array{
          \{s'\} &\longrightarrow& Vect
          \\
          s' &\mapsto& \mathcal{E}'_{s'} 
        }
      \right)
    \Bigg)
    \\
    \;\simeq\;
    F
    \Bigg(
      \underset{(s, s') \in S \times S'}{\coprod}
      \Big(
        \big(
          (s \colon \{s\}) \mapsto \mathcal{E}_s
        \big)
        \boxtimes
        \big(
          (s' \colon \{s'\}) \mapsto \mathcal{E}_{s'}
        \big)
      \Big)
    \Bigg)
    \\
    \;\simeq\;
    \underset{(s, s') \in S \times S'}{\coprod}
    \bigg(
      \Big(
        F
        \big(
          (s \colon \{s\}) \mapsto \mathcal{E}_s
        \big)
       \Big)
        \otimes
       \Big(
        F
        \big(
          (s' \colon \{s'\}) \mapsto \mathcal{E}_{s'}
        \big)
      \Big)
    \bigg)
    \\
    \;\simeq\;
      \Big(
        F
        \big(
          \underset{s \in S}{\coprod}
          (s \colon \{s\}) \mapsto \mathcal{E}_s
        \big)
       \Big)
        \otimes
       \Big(
        F
        \big(
          \underset{s' \in S'}{\coprod}
          (s' \colon \{s'\}) \mapsto \mathcal{E}_{s'}
        \big)
      \Big)
    \\
    \;\simeq\;
    F(\mathcal{E}) \otimes F(\mathcal{E}')
    \,.
  \end{array} 
$$

\end{proof}








## Related concepts

* [[Mod]]

* [[VectBund(B)]]

* [[tangent (infinity,1)-category|tangent $\infty$-category]]

* [[parameterized spectra]]

* [[doubly closed monoidal category]]


[[!redirects VectorBundles]]
