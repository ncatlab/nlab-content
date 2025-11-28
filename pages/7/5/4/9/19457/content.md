
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of _enriched adjoint functors_ is the generalization of that of [[adjoint functors]] ([[adjunctions]] in [[Cat]]) from [[category theory]] to [[enriched category theory]] ([[adjunctions]] in [[VCat]]).

## Definition

\begin{definition}\label{EnrichedAdjunction}
**(enriched adjoint functors)**
\linebreak
For $\mathcal{V}$ a [[closed monoidal category|closed]] [[symmetric monoidal category]] with all [[limits]] and [[colimits]] (a [[cosmos for enrichment]]), let $\mathcal{C}$, $\mathcal{D}$ be a [[pair]] of $\mathcal{V}$-[[enriched categories]]. 

Then an _enriched [[adjoint pair]] of $\mathcal{V}$-[[enriched functors]]_ or _$\mathcal{V}$-enriched adjunction_ between them 

$$
  \mathbf{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\;\; \bot \;\;}
  \mathbf{D}
$$

is a [[pair]] of $\mathcal{V}$-[[enriched functors]] as shown, such that the following equivalent conditions hold ([Kelly, §1.11](#Kelly))

* there exists an [[adjunction]] between them when regarded as [[1-morphisms]] in the [[2-category]] [[VCat|$\mathcal{V}Cat$]], namely $V$-[[enriched natural transformations]] 

  $\eta \,\colon\, Id_{\mathbf{D}} \longrightarrow R \circ L$ (the [[adjunction unit]])
  and
  $\epsilon \,\colon\, R \circ L \longrightarrow id_{\mathbf{C}}$ (the [[adjunction counit]])

  such that the following *[[zig-zag law]]* holds in [[VCat|$\mathcal{V}Cat$]]:
 
\begin{tikzcd}[row sep=10pt]
  \mathbf{D}
  \ar[rr, bend left=40, "{\mathrm{id}}", 
      "{\ }"{name=s1, swap}
  ]
  \ar[r, "L"{description}, "{\ }"{name=t1, pos=.9}]
  \ar[
    from=s1,
    to=t1,
    Rightarrow,
    "{ \eta }"{swap}
  ]
  &
  \mathbf{C}
  \ar[rr, bend right=40, "{\mathrm{id}}"{swap},
    "{\ }"{name=t2}
  ]
  \ar[r, "R"{description}]
  &
  \mathbf{D}
  \ar[r, "L"{description}, "{\ }"{swap, name=s2, pos=.1}]
  \ar[
    from=s2,
    to=t2,
    Rightarrow,
    "{ \epsilon }"
  ]  
  &
  \mathbf{C}
  &=&
  \mathbf{D}
  \ar[r, bend left=40, "{L}", "{\ }"{name=s3, swap}]
  \ar[r, bend right=40, "{\mathrm{id}}"{swap}, "{\ }"{name=t3}]
  \ar[from=s3, to=t3, Rightarrow, "{\mathrm{id}}"]
  &
 \mathbf{C}
\end{tikzcd}

\begin{tikzcd}[row sep=10pt]
  \mathbf{C}
  \ar[rr, bend right=40, "{\mathrm{id}}"{swap}, 
      "{\ }"{name=s1}
  ]
  \ar[r, "R"{description}, "{\ }"{name=t1, pos=.9, swap}]
  \ar[
    from=t1,
    to=s1,
    Rightarrow,
    "{ \epsilon }"{swap, pos=.3}
  ]
  &
  \mathbf{D}
  \ar[rr, bend left=40, "{\mathrm{id}}",
    "{\ }"{name=t2, swap}
  ]
  \ar[r, "L"{description}]
  &
  \mathbf{C}
  \ar[r, "R"{description}, "{\ }"{name=s2, pos=.1}]
  \ar[
    from=t2,
    to=s2,
    Rightarrow,
    "{ \eta }"{pos=.8}
  ]  
  &
  \mathbf{D}
  &=&
  \mathbf{C}
  \ar[r, bend left=40, "{R}", "{\ }"{name=s3, swap}]
  \ar[r, bend right=40, "{R}"{swap}, "{\ }"{name=t3}]
  \ar[from=s3, to=t3, Rightarrow, "{\mathrm{id}}"]
  &
 \mathbf{D}
\end{tikzcd}

* {#ViaHomIsomorphism} there is a $\mathcal{V}$-[[enriched natural isomorphism|enriched natural]] [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) between [[enriched hom-functors]], of the form

$$
  \mathbf{C}\big(L(-),-\big)
  \;\simeq\;
  \mathbf{D}\big(-,R(-)\big)
  \,.
$$
\end{definition}
If the [[adjunction unit]] and [[adjunction counit]] are (enriched natural) *[[isomorphisms]]* then this is called an *enriched adjoint equivalence*.

(e.g. [Kelly, §1.11](#Kelly), [Borceux 94, Def. 6.7.1](#Borceux94))

The [[2-functor]] $\mathcal{V}$-$Cat \rightarrow {Cat}$ that sends an enriched category to its underlying ordinary category (i.e. the [[change of enrichment]] to [[Set]] along $V : \mathcal{V} \to Set$) sends a pair of enriched adjoint functor to an ordinary pair of [[adjoint functors]] and sends an enriched adjoint equivalence to an [[adjoint equivalence]].


## Examples

\begin{example}
  A pair of [[Set]]-enriched adjoint functors is an ordinary pair of [[adjoint functors]].
\end{example}

\begin{example}
 A pair of [[truth values]]-enriched adjoint functors is equivalently known as a *[[Galois connection]]*.
\end{example}

\begin{example}
\label{StrictAdjointTwoFunctors}
  With *[[Cat]]* denoting the [[1-category]] of [[small category|small]] [[strict categories]] equipped with its [[cartesian monoidal category|cartesian monoidal]] [[structure]] (via forming [[product categories]]), a pair of [[Cat]]-enriched adjoint functors is also known as a pair *[[strict adjoint 2-functors]]*.
\end{example}

\begin{example}
  Assuming the [[axiom of choice]] in the underlying [[set theory]], every Dwyer-Kan [[simplicial groupoid]] (i.e. [[sSet]]-[[enriched groupoid]]) is [[sSet]]-enriched equivalent to a [[disjoint union]] of simplicial [[delooping groupoids]] of [[simplicial groups]] --- see the discussion [there](simplicial+groupoid#RelationToSimplicialGroups)
\end{example}

## Related concepts

* [[enriched Quillen adjunction]]

  * [[simplicial Quillen adjunction]]

* [[monoidal adjunction]]


## References

The notion is due to

* [[Max Kelly]], §3 in: *Adjunction for enriched categories*, in: *Reports of the Midwest Category Seminar III*, Lecture Notes in Mathematics **106**, Springer (1969) &lbrack;[doi:10.1007/BFb0059145](https://doi.org/10.1007/BFb0059145)&rbrack;

Review:

* {#Kelly} [[Max Kelly]], section 1.11 of: _Basic Concepts of Enriched Category Theory_, Cambridge University Press, Lecture Notes in Mathematics **64** (1982),  Republished in: Reprints in Theory and Applications of Categories, **10** (2005) 1-136 &lbrack;[tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;


* {#Borceux94} [[Francis Borceux]], Def. 6.7.1 of: _[[Handbook of Categorical Algebra]] Vol 2_, Cambridge University Press (1994)

[[!redirects enriched adjoint functors]]

[[!redirects enriched adjunction]]
[[!redirects enriched adjunctions]]

[[!redirects enriched adjoint]]
[[!redirects enriched adjoints]]

[[!redirects enriched adjoint equivalence]]
[[!redirects enriched adjoint equivalences]]

