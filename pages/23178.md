
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is called *singular cohesion* in [SaSc 2020](#SaSc20), following observations in [Rezk 2014](#Rezk14), is a form of [[cohesion]] [[cohesive (infinity,1)-toposes|on $\infty$-toposes]] which enhances any [[base (infinity,1)-topos|base]] notion of "smooth" cohesive geometry to a "singular-smooth" cohesive geometry which reflects the possible presence of [[orbi-singularities]].

For example, where [[smooth manifolds]] are faithfully embedded among the [[cohesive (infinity,1)-topos|cohesive $\infty$-topos]] of [[smooth infinity-groupoids]], so their [[orbifolds]] are faithfully embedded among [[singular-smooth infinity-groupoid|singular-smooth $\infty$-groupoids]].

For the [[base (infinity,1)-topos|base $\infty$-topos]] [[Infinity-Grpd|$Grpd_\infty$]], embodying plain [[homotopy theory]], its singular-cohesive enhancement is [[global equivariant homotopy theory]] and hence every singular-cohesive $\infty$-topos is cohesive over (in particular) [[global equivariant homotopy theory]], hence may be thought of as embodying a "globally equivariant and cohesive" homotopy theory.

In fact, every [[slice (infinity,1)-topos|slice]] of a singular-cohesive $\infty$-topos over the canonical $G$-[[orbi-singularity]] $\boxed{\prec}\mathbf{B}G$ [[cohesion of global- over G-equivariant homotopy theory|is cohesive over]] the $G$-[[equivariant homotopy theory]] over the given smooth cohesive base, with the [[inverse image]] of the cohesive [[geometric morphism]] being the embedding of cohesive $G$-[[orbispaces]].


### Globally equivariant geometric homotopy theory

Consider the [[full sub-(infinity,1)-category|full sub-$\infty$-category]] of [[Infinity-Grpd|$Grp_\infty$]] on the [[connected object in an (infinity,1)-topos|connected]], [[truncated object in an (infinity,1)-category|1-truncated]] [[pi-finite homotopy types|$\pi$-finite homotopy types]] 

\[
  \label{CategoryOfSingularities}
  \array{
    Singularities
    &\coloneqq&
    Grpd^{fin}_{1, \geq 1}
    &\xhookrightarrow{\;}&
    Grp_\infty
    \\
    \boxed{\prec}\mathbf{B}G
    &
    \mapsto
    &
    B G
  }
\]

(sometimes called the "[[global orbit category]]"), hence the [[full sub-(infinity,1)-category|full sub]] [[(2,1)-category]] of [[groupoids]] on the [[delooping groupoids]] of [[finite groups]] $G$, 


Then for $\mathbf{H}_{\subset}$ any [[base (infinity,1)-topos|base $\infty$-topos]] 
the [[(infinity,1)-category of (infinity,1)-presheaves|$\infty$-category of $\infty$-presheaves]] over $Singularities$ (eq:CategoryOfSingularities)

$$
  \mathbf{H}
  \,\coloneqq\,
  Glo \mathbf{H}_{\subset}
  \;\coloneqq\;
  PSh_\infty
  \big(
    Singularities
    \,,
    \mathbf{H}_{\subset}
  \big)
  \,,
$$

which may be called the *[[globally equivariant homotopy theory]]* over the [[geometric homotopy theory]] $\mathbf{H}_{\subset}$,
is [[cohesive (infinity,1)-topos|cohesive]] over $\mathbf{H}_{\subset}$ (as is any $\infty$-presheaf $\infty$-topos over an [[(infinity,1)-site|$\infty$-site]] with a [[terminal object]], see e.g. at *[[adjoint quadruple]]* the section *[Cohesion](adjoint+quadruple#CohesiveToposes)*).

In fact, for any $\boxed{\prec}\mathbf{B}G \,\in\, Singularities$, the [[slice (infinity,1)-topos|slice $\infty$-topos]] $Glo(\mathbf{H}_{\subset})_{/\boxed{\prec}\mathbf{B}G}$ is [[cohesive (infinity,1)-topos|cohesive]] over the $G$-[[equivariant homotopy theory]], hence over the [[(infinity,1)-category of (infinity,1)-presheaves|$\infty$-topos of $\infty$-presheaves]] over the actual [[orbit category]] of $G$:

$$
  G \mathbf{H}_{\subset}
  \;\coloneqq\;
  Psh_\infty
  \big(
    G Orbits
    ,\,
    \mathbf{H}_{\subset}
  \big)
  \,.
$$

\begin{tikzcd}
  \mathllap{
    \mathbf{H}_{/\boxed{\prec}\mathbf{B}G}
    \;\coloneqq\;
  } 
  (\mathrm{Glo} \mathbf{H}_{\subset})_{/\boxed{\prec}\mathbf{B}G}
      \ar[
        rr,
        "{ G \mathrm{Smth}    }"{description}
      ]
      \ar[
        rr,
        shift left=40pt,
        "{ G \mathrm{Cncl} }"{description, pos=.5},
        "\mathclap{\times}"{description, pos=0}
      ]
      &&
     G \mathbf{H}_{\subset}
      \ar[
        ll,
        hook',
        shift right=20pt,
        "{ G \mathrm{Spc} }"{description}
      ]
      \ar[
        ll,
        hook',
        shift right=-20pt,
        "{ G \mathrm{Snglrt} }"{description, pos=.5}
      ]
      \ar[
        ll,
        phantom,
        shift right=10pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=30pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
      \ar[
        ll,
        phantom,
        shift right=-10pt,
        "{\scalebox{.6}{$\bot$}}"
      ]
\end{tikzcd}

This follows formally from the [[full sub-(infinity,1)-category|full sub]] [[(2,1)-category]] inclusion

$$
  \Singularities_{/\boxed{\prec}\mathbf{B}G}
  \underoverset
{\hookleftarrow}
    {\overset{\tau_0}{\longrightarrow}}
    
    {\;\;\; \bot \;\;\;}
  G Orbits
  \,,
$$

as discussed at *[[cohesion of global- over G-equivariant homotopy theory]]*.


### Globally equivariant cohesive homotopy theory

Now if $\mathbf{H}_{\subset}$ is itself [[cohesive (infinity,1)-topos|cohesive]] over [[Infinity-Grpd|$Grpd_\infty$]] then $\mathbf{H} = Glo(\mathbf{H}_{\subset})$ carries the following system of [[adjoint triples]] of [[adjoint modalities]]:


\begin{imagefromfile}
    "file_name": "SingularCohesionAdjoints_20211026.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [SaSc 21](https://ncatlab.org/schreiber/show/Equivariant+principal+infinity-bundles)"
\end{imagefromfile}

### Singular cohesion

From this is obtained a pair of [[adjoint triples]] of [[adjoint modalities]] on $\mathbf{H} \,\coloneqq\, Glo(\mathbf{H}_{\smooth})$ which jointly reflect that its objects are [[geometric homotopy types]] whose geometric nature is "cohesive with [[orbi-singularities]]".

(...)

For example, when $\mathbf{H}_{\subset} \,=\,$ [[smooth infinity-groupoids|$SmthGrpd_\infty$]] containing [[diffeological spaces]] as the [[full sub-(infinity,1)-category|full sub-$\infty$-category]] of [[n-truncated object of an (infinity,1)-category|0-truncated]] [[concrete objects]]

$$
  DiffSpc
  \xhookrightarrow{ i_{\tau_0, \sharp_1} }
  SmthGrpd_\infty
$$

then $\mathbf{H} \,\coloneqq\, Glo(SmthGrpd_\infty)$ contains diffeological [[orbifolds]] as a [[full sub-(infinity,1)-category|full sub-$\infty$-category]] of orbi-singular- hence $\box{\prec}$-[[modal objects]]

$$
  \array{
    DiffOrbfld
    &\xhookrightarrow{\;}&
    LieGrpd
    &\xhookrightarrow{ \;}&
    Glo(SmthGrpd_\infty)
    \\
    &&
    X \sslash G
    &\mapsto&
    \boxed{\prec}(X \sslash G)
  }
$$

in such a way that their [[shape modality|shape]] 

$$
  \esh 
  \,
  \prec
  \,
  (X \!\sslash\! G)
  \;\;\in\;\;
  G Grpd_\infty
   \xhookrightarrow{ Dsc }
  (G SmthGrpd_\infty)_{/\boxed{\prec}\mathbf{B}G}
    \xhookrightarrow{ G Spc }
  \mathbf{H}_{/\boxed{\prec}\mathbf{B}G}
$$

is the incarnation of the [[D-topological space]] underlying $X$ as a [[G-space]] in $G$-[[equivariant homotopy theory]] (via [[Elmendorf's theorem]]):





(...)


## References

The [[cohesion of global- over G-equivariant homotopy theory]] was first observed in

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_, 2014  ([pdf](http://www.math.uiuc.edu/~rezk/global-cohesion.pdf), [[Rezk14.pdf:file]])

with emphasis on characterization of the full image under $G Spc$ of [[orbispaces]] in sliced [[global homotopy theory]].

The above combination with smooth cohesion to singular cohesion was considered in

* {#SaSc20} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))

in discussion of [[orbifold cohomology]], where the above notation is taken from,

and in 

* {#SaSc20} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Equivariant principal infinity-bundles|Equivariant principal $\infty$-bundles]]*

in discussion of [[equivariant bundle|equivariant]] [[principal infinity-bundle|principal $\infty$-bundles]], where the above diagrams are taken from.

