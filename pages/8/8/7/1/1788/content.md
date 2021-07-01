
### Generalization to simplicial presheaves
 {#GeneralizationToSimplicialPresheaves}

Since the [[simplicial classifying space|universal simplicial principal complex]]-construction is [[functor|functorial]]

$$
  SimplicialGroups
  \xrightarrow{\;\; W \;\;}
  SimplicialSets
$$

with [[natural transformations]]

$$
  \mathcal{G}
  \xrightarrow{\;\; i \;\;}
  W\mathcal{G}
  \xrightarrow{\;\; p \;\;}  
  \overline{W}\mathcal{G}
$$

the pair of [[adjoint functors]] (eq:QuillenAdjunctionWithSliceOverSimplicialClassifyingSpace) extends to [[presheaves]]:


\begin{prop}
For $\mathcal{C}$ a [[small category|small]] [[sSet-category]] with

$$
  sPSh(\mathcal{C})
  \;\coloneqq\;
  sSetCat( \mathcal{C}^{op}, \, sSet )
$$

denoting its category of [[simplicial presheaves]], and for

$$
  \underline{\mathcal{G}}
  \;\in\;
  Groups
  \big(
    sPSh(\mathcal{C})
  \big)
$$

a [[group object]] [[internalization|internal to]] [[SimplicialPresheaves]] with

$$
  \underline{\mathcal{G}}
  Acts
  \big(
    sPSh(\mathcal{C})
  \big)  
$$

denoting its category of [[action objects]] [[internalization|internal to]] [[SimplicialPresheaves]]

we have an [[adjoint functor|adjoint pair]]

$$
  \underline{\mathcal{G}}
  Acts
  \big(
    sPSh(\mathcal{C})
  \big)  
  \underoverset
    {
      \underset{ 
        \big(
          (-) \times W\underline{\mathcal{G}} 
        \big) 
        \big/
        \underline{\mathcal{G}}
      }
      {\longrightarrow}}
    {
      \overset{
        (-) 
          \times_{\overline{W}\underline{\mathcal{G}}}
        W\underline{\mathcal{G}}
      }{\longleftarrow}
    }
    {\bot}
    sPSh(\mathcal{C})_{/\overline{W}\underline{\mathcal{G}}}
$$

\end{prop}
\begin{proof}

The required [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) is the composite of the following sequence of [[natural bijections]]:

$$
  \begin{aligned}
    Hom
    \Big(
      (\underline{X},p),
      \,
      \big(
        \underline{Y} \times W\underline{\mathcal{G}}  
      \big) / \underline{\mathcal{G}}
    \Big)
    & 
    \;\simeq\;
    Hom
    \Big(
      \underline{X},
      \,
      \big(
        \underline{Y} \times W\underline{\mathcal{G}}  
      \big) / \underline{\mathcal{G}}
    \Big)
    \underset{
    Hom
    \Big(
      \underline{X},
      \,
      \overline{W} \underline{\mathcal{G}}
    \Big)
    }{\times}
    \{p\}
    \\
    & \;\simeq\;
    \int^c
    Hom
    \Big(
      \underline{X}(c),
      \,
      \big(
        \underline{Y}(c) \times W\underline{\mathcal{G}(c)}  
      \big) / \underline{\mathcal{G}}(c)
    \Big)
    \underset{
    \int^c
    Hom
    \Big(
      \underline{X}(c),
      \,
      \overline{W} \underline{\mathcal{G}}(c)
    \Big)
    }{\times}
    \{p\}
    \\
    & \;\simeq\;
    \int^c
    \left(
    Hom
    \Big(
      \underline{X}(c),
      \,
      \big(
        \underline{Y}(c) \times W\underline{\mathcal{G}(c)}  
      \big) / \underline{\mathcal{G}}(c)
    \Big)
    \underset{
    Hom
    \Big(
      \underline{X}(c),
      \,
      \overline{W} \underline{\mathcal{G}}(c)
    \Big)
    }{\times}
    \{p(c)\}
    \right)
    \\
    & \;\simeq\;
    \int^c 
    Hom_{/\overline{W}\underline{\mathcal{G}}(c)}
    \Big(
      \big(X(c), p(c)\big),
      \,
      \big(
        Y(c) \times \overline{W} \mathcal{G}(c)
      \big)\big/ \mathcal{G}(c)
    \Big)
    \\ 
    & \;\simeq\;
    \int^c
    \left(
      \underline{\mathcal{G}}(c)
      Acts(sSet)
      \big(
        X(c) 
          \underset{ \overline{W}\underline{\mathcal{G}}(c) }{\times}
        W \underline{\mathcal{G}}(c),
        \,
        Y(c)
      \big)
    \right)
    \\
    & \;\simeq\;
    \mathcal{G}Acts(sPSh(\mathcal{C}))
    \big(
      X 
        \underset{\overline{W}\underline{\mathcal{G}}}{\times}
      W \underline{\mathcal{G}},
      \,
      Y
    \big)
  \end{aligned}
$$

Here:

* the first step is the characterization of hom-sets of a [[slice category]] as a [[fiber]] of the [[hom-sets]] of the underlying category;

* the second step is the description of the hom-set of a [[functor category]] as an [[end]] of object-wise hom-sets;

* the third step uses that [[ends]] are [[limits]] and [[limits commute with limits|hence commute]] the the [[fiber product]];

* the fourth step recognizes again, now object-wise, the hom-set in a [[slice category]];

* the fifth step is objectwise the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of (eq:QuillenAdjunctionWithSliceOverSimplicialClassifyingSpace);

* the sixth step recognizes again the [[end]] as computing the hom-set in (a subcategory of) a functor category:

$$
  \array{
    \underline{\mathcal{G}}Acts
    \big(
      A, \, B
    \big)
    &\longrightarrow&
    \mathcal{G}(c_1)Acts
    \big(
       A(c_1), \, B(c_1)
    \big)
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    \mathcal{G}(c_2)Acts
    \big(
      A(c_2), \, B(c_2)
    \big)
    &\longrightarrow&
    Hom
    \big(
      A(c_1), \, B(c_2)
    \big)
  }
$$

\end{proof}

\linebreak

\linebreak


added the observation ([here](https://ncatlab.org/nlab/show/Borel+model+structure#GeneralizationToSimplicialPresheaves)) that the adjunction for simplicial groups 

$$
    \mathcal{G} Acts(sSet)
      \underoverset
        {\underset{ \big((-) \times W \mathcal{G}\big)/\mathcal{G} }{\longrightarrow}}
        {\overset{ (-) \times_{\overline{W}\mathcal{G}} W \mathcal{G}  }{\longleftarrow}}
        {\bot}
    sSet_{/\overline{W}\mathcal{G}}
$$

generalizes to one for presheaves of simplicial groups

$$
  \underline{\mathcal{G}}
  Acts
  \big(
    sPSh(\mathcal{C})
  \big)  
  \underoverset
    {
      \underset{ 
        \big(
          (-) \times W\underline{\mathcal{G}} 
        \big) 
        \big/
        \underline{\mathcal{G}}
      }
      {\longrightarrow}}
    {
      \overset{
        (-) 
          \times_{\overline{W}\underline{\mathcal{G}}}
        W\underline{\mathcal{G}}
      }{\longleftarrow}
    }
    {\bot}
    sPSh(\mathcal{C})_{/\overline{W}\underline{\mathcal{G}}}
$$


