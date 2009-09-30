This entry collects material on the June 2009 workshop on [[string theory|strings]], [[quantum field theory|fields]], and [[topology]] at [[Oberwolfach]].

* Title:      Strings, Fields and Topology
* Organisers: 
  * Dennis Sullivan, New York
  * Stephan Stolz, Notre Dame
  * Peter Teichner, Berkeley
* Date:       June 7th - June 13th, 2009
* ID:         0924

Writeups of most of the talks have appeared as 

* _Strings, Field, Topology_,  Oberwolfach report No 28, 2009, [pdf](http://www.mfo.de/programme/schedule/2009/24/OWR_2009_28.pdf)


# Talks 

* **Thomas Schick**, [_Smooth cohomology theories_](#schick).

* **Ullrich Bunke**, [_Smooth K-theory_](#bunke).

* **Christoph Schweigert and Ingo Runkel** , [_CFT and algebra in braided tensor categories I and II_](#schweigert). 

* **Kevin Costello**, [_Factorization algebras in perturbative QFT_](#costello). 

* **[[Gabriel C. Drummond-Cole]]**, [_$\infty$-Operads, $BU_\infty$ and $Hypercomm_\infty$_](#drummond-cole). 

* **Alex Kahle**, [_Superconnections and index theory_](#kahle).

* **[[Chris Schommer-Pries]]**, [_Topological defects, $D$-branes, and the classifications of TFTs in low dimensions_](#schommer-pries). 

* **Dan Freed**, [_Geometry and topology of orientifolds_](#freed).

* **Dan Freed**, [Evening informal session on RR fields and all that](#freed_extra).

* **Scott Wilson**, [_Some algebra related to mapping spaces and applications_](#wilson).

* **[[Urs Schreiber]]**, [_Background fields in twisted differential nonabelian cohomology_](#schreiber).

* **Andr&#233; Henriques**, [_Invertible conformal nets_](#henriques).

* **Andr&#233; Henriques**, [Evening informal session more details about conformal nets](#henriques_extra).

* **[[Konrad Waldorf]]**, [_String connections and Chern-Simons 2-gerbes_](#waldorf). 

* **Kevin Walker**, [_Blob homology_](#walker)

* **Ralph Cohen**, [_String topology, field theories and Fukaya categories_](#cohen).
 
* **Corbett Redden**, [_String structures, 3-forms, and tmf classes_](#redden).

* **Mike Hopkins**, [_The Kervaire invariant_](#hopkins).

* **Mike Hopkins**, [Evening informal session on technical details of the solution of the Kervaire invariant problem](#hopkins_extra).

* **David Chataur**, [Evening informal session explaining recent results in opeards](#chataur_extra)

* **Kishore Marathe**, [Evening informal session on the gauge theory to string theory correspondence](#marathe_extra)



# Talks in more detail


#### Thomas Schick, _Smooth cohomology theories_ {#schick}

The basic idea of [[differential cohomology]] (also called _smooth cohomology_ ) is to combine generalized [[cohomology]] (e.g. ordinary integral cohomology, or K-theory, or tmf, or ...) and differential forms. Hopkins and Singer showed that a smooth refinement exists for any generalized cohomology theory, but didn't provide an (easy for mere mortals to understand) explicit construction. In this talk, Thomas Schick advertised geometric models for multiplicative smooth cohomology with $S^1$-integration for $K$-theory (joint with Ulrich Bunke) and MU-bordism (joint with Ulrich Bunke, Schr&#246;der? and Wethamp?). They have proved a uniqueness theorem, stating that under certain assumptions any two smooth refinements of a generalized cohomology theory are naturally isomorphic. 

##### Resources

* [[oberwolfach_june2009_schick.pdf|Notes by Bruce Bartlett:file]]
* [Notes by Gabriel Drummond-Cole](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_9.pdf)
* [[Oberwolfach Workshop, June 2009 -- Tuesday, June 9|Notes by Urs Schreiber]]
* [[oberwolfach_june2009_pavlov_schick.pdf|Notes by Dmitry Pavlov:file]]



#### Ulrich Bunke, _Smooth K-theory_. {#bunke}

In this talk, which led on from the previous one by Thomas Schick, Ulrich Bunke gave an explicit description of their smooth $K$-theory model in terms of geometric cocycles. Basically a cocycle consists of a pair $(\mathcal{E}, \rho)$ where $\mathcal{E}$ is a 'geometric family', namely a smooth proper submersion $E \rightarrow B$ with a fiberwise metric, a Clifford bundle $W$ and some connection of some sort. The object $\rho$ is an element of $\Omega(B, K) = C^\infty(B, \Lambda^*T^* B \otimes K^*)$. He also described smooth $K$-orientatiosn and the push-forward map, with an application to the $e$-invariant of Adams. There is also a Riemann-Roch theorem. 

##### Resources

* [[oberwolfach_june2009_bunke.pdf|Notes by Bruce Bartlett:file]]
* [Notes by Gabriel Drummond-Cole](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_9.pdf)
* [[Oberwolfach Workshop, June 2009 -- Tuesday, June 9|Notes by Urs Schreiber]]

#### Christoph Schweigert and Ingo Runkel,_CFT and algebra in braided tensor categories I and II_. {#schweigert} 

This talk explains how correlators for a rational two-dimensional [[conformal field theory]] can be constructed in the [[FQFT|functorial TFT]] formalism. Based on a [[modular tensor category]] $C$, decoration data have been introduced in terms of special symmetric Frobenius algebras in $C$ and the correlator, as an element of $tft_C (\hat{X})$ with $\hat{X}$ a double cover of the surface $X$, has been expressed in terms ofthe invariant of a decorated 3-manifold $M_X$ with $\partial M_X = \hat{X}$. The correlators are invariant under the [[mapping class group]]s and obey the [[sewing constraint]].

[[Morita equivalence|Morita equivalent]] special symemtric Frobenius algebras lead to an equivalent description of the correlators. A Morita invariant formulation is provided by the notion of a module category $M$ over the module tensor category $C$. The [[world sheet]] is now decorated by categories, functors between module categories and natural transformations.

##### Resources

* Notes by Bruce Bartlett [[oberwolfach_june2009_schweigert.pdf|1:file]] and [[oberwolfach_june2009_runkel.pdf|2:file]]

* [Notes by Gabriel Drummond-Cole](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_8.pdf)

* [[Oberwolfach Workshop, June 2009 -- Monday, June 8|Notes by Urs Schreiber]]

* [[oberwolfach_june2009_pavlov_schweigert_runkel.pdf|Notes by Dmitry Pavlov:file]]



#### Kevin Costello, _Factorization algebras in perturbative QFT_. {#costello}

A [[factorization algebra]] on a manifold $M$ is an object which associates to every ball $B \subseteq M$ a vector space (or cochain complex) $F(B)$; and to every collection $B_1 \coprod \cdots \coprod B_n \subset B_{n+1}$ of disjoint balls in a larger ball, a map $F(B_1) \otimes \cdots \otimes F(B_n) \rightarrow F(B_{n+1})$. These structures are the $C^\infty$ analogues of chiral algebras, as introduced by Beilinson and Drinfeld; they are closely related to [[algebra over an operad|algebras]] for the [[little n-disk operad]] $E_n$.

In this series of lectures, Kevin Costello set up a framework to construct [[factorization algebra|factorization algebras]] from [[perturbative quantum field theory|perturbative]] [[quantum field theory]]. The set up is analagous to the [[deformation quantization]] picture of [[quantum mechanics]]. Just as the [[observable]]s of [[quantum mechanics]] are encoded in an associative algebra, Costello argues that the observables of a QFT on $M$ are encoded in a factorization algebra on $M$, similar to but slightly different from the waqy it works in (euclidean) [[AQFT]]. This factorization algebra arises by quantizing a commutative factorization algebra associated to classical field theory. 

This series of lectures finished with the statement of a theorem allowing one to quantize the commutative factorization algebra associated to a classical field theory in a range of situations, including situations of physical interest.  This is joint work with Owen Gwilliam. 

##### Resources

* Notes by Bruce Bartlett [[oberwolfach_june2009_costello1.pdf|1:file]], [[oberwolfach_june2009_costello2.pdf|2:file]], [[oberwolfach_june2009_costello2.pdf|3:file]]

* [Notes by Gabriel Drummond-Cole 1](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_8.pdf) and [2](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_9.pdf) 

* [[Oberwolfach Workshop, June 2009 -- Monday, June 8|Notes by Urs Schreiber 1]] and [[Oberwolfach Workshop, June 2009 -- Tuesday, June 9|2]]

* [[oberwolfach_june2009_pavlov_costello.pdf|Notes by Dmitry Pavlov:file]]

#### [[Gabriel C. Drummond-Cole]], _$\infty$-Operads, $BU_\infty$ and $Hypercomm_\infty$_. {#drummond-cole}

Gabriel Drummond-Cole applies the machinery of the [[model category]] of [[operad]]s to extend and explain the Barannikov-Kontsevich passage from differential BV algebras satisfying the $\partial-\overbar{\partial}$ lemma to hypercommutative algebras (Frobenius manifolds). This is joint work with Bruno Valette. The following theorem was proved:

+-- {: .un_thm}
###### Theorem

Let $V$ be a differential BV-algebra over a field of characteristic zero. Let $H$ be its homology. Then:
1. If $V$ satisfies the noncommutative Hodge to de Rham degeneration condition, then there exists a hypercommutative $\infty$-structure on $H$.
2. If $V$ satisfies Park's semiclassical condition then this structure is unique up to $Hypercomm_\infty$ quasi-isomorphism.
=--


##### Resources

* [[oberwolfach_june2009_pavlov.pdf|Notes by Dmitry Pavlov:file]]

*  Gabriel Drummond-Cole's [website](http://www.math.sunysb.edu/~blafard/)


#### Alex Kahle, _Superconnections and index theory_. {#kahle}

In this talk, Alex Kahle described results from his thesis work (his supervisor was Dan Freed) about [superconnections and index theory](http://arxiv.org/abs/0810.0820). The idea is to prove a local index theorem using [[superconnection]]s via direct geometric-analytical methods (i.e. not stochastic) for use with family index problems, determinant line bundles, etc. Just like [[connection on a bundle|ordinary connection]]s on spinor buundles, a superconnection gives rise to a [[Dirac operator]] on a [[spinor bundle]]. The usual local index theorem (that the trace of the heat kernel converges as $t \rightarrow 0$ to a certain differential form) needs to be modified though, because forms of different degrees have different scaling behaviour (recall that a [[superconnection]] involves forms of different degrees). Alex worked out how to scale everything correctly so that one indeed gets a local index theorem for superconnections, leading to many potential applications. 


##### Resources

* [[oberwolfach_june2009_kahle.pdf|Notes by Bruce Bartlett:file]]

* [Notes by Gabriel Drummond-Cole](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_10.pdf)

* [[Oberwolfach Workshop, June 2009 -- Wednesday, June 10|Notes by Urs Schreiber]]

* [[oberwolfach_june2009_pavlov_kahle.pdf|Notes by Dmitry Pavlov:file]]




#### [[Chris Schommer-Pries]], _Topological defects, $D$-branes, and the classifications of TFTs in low dimensions_. {#schommer-pries}

Chris explained his classification result mentioned at [[(infinity,n)-category of cobordisms]] from his thesis of extended (he suggested calling them _local_) 2d TQFT's via the explicit generators and relations he obtained on $2Cob$. He also showed how the [[higher category theory|higher-categorical viewpoint]] unites the following two ideas: the 'open-closed' theories and the 'field theories with defects' from Ingo Runkel and Christoph Schweigert's talk. He showed how both these concepts are particular examples of a single notion, namely that of a collection of natural transformations between a restriction of [[FTQFt]] $n$-functors (called "unnatural" or "supernatural" transformations to indicate that it is a transformation not of the entire functor, but just of its restriction to the 2-category of 2-manifolds with only inverttible 2-morphisms). 

This is precisely the kind of viewpoint that Urs Schreiber and Jens Fjelstad [suggested](http://golem.ph.utexas.edu/category/2007/08/dbranes_from_tin_cans_part_x.html) at the [n-category cafe](http://golem.ph.utexas.edu/category/) under the slogal [D-branes from tin-cans](http://golem.ph.utexas.edu/category/2006/10/dbranes_from_tin_cans_arrow_th.html) (a D-[[brane]] is a boundary condition ordefect, a "tin-can diagram" is the naturality diagram for a higher natural transformation).

By the way, there's much more to come from Chris, he is working on the 3d theory and much besides!

##### Resources

*  [Slides on webpage](http://sites.google.com/site/chrisschommerpriesmath/Home/Slides-MFO-6-11-09.pdf?attredirects=0)

#### Dan Freed, _Geometry and topology of orientifolds_. {#freed}

Freed described recent work with [[Jacques Distler]] and Greg Moore on a certain background structure in [[string theory|superstring theory]] called an [[orientifold], which is a [[bundle gerbe]] on a $\mathbb{Z}_2$ [[orbifold]] with a peculiar "twisted" [[equivariance]] condition. There is apparantly a beautiful string theory formula to calculate the '[[RR charge]]', namely something like
\[
 RR charge = \pm 2^{something} i_* \sqrt\left( \frac{L'(F)}{L'(\nu)} \right)
\]
involving a certain normal bundle and the 'Bott element in K-theory', which looks similar to the Hirzebruch formula for the L-genus. This uses some kind of twisted [[differential cohomology]] version of KR theory. The whole thing can be viewed as a new sort of anomaly, having to do with an exotic orientation of some kind.


##### Resources

* [[oberwolfach_june2009_freed.pdf|Notes by Bruce Bartlett:file]]

* [Notes by Gabriel Drummond-Cole](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_08.pdf)

* [[Oberwolfach Workshop, June 2009 -- Monday, June 8|Notes by Urs Schreiber]])

* [[oberwolfach_june2009_pavlov_freed.pdf|Notes by Dmitry Pavlov:file]]


#### Dan Freed, Evening informal session on RR fields and all that.

Summary appearing soon...

##### Resources

*  [[oberwolfach_june2009_freed_extra.pdf|Notes by Bruce Bartlett:file]]


#### Scott Wilson, _Some algebra relat4ed to mapping spaces and applications_. {#wilson}

Wilson defined a _partial algebra_ as a lax [[monoidal functor]] from the category of finite sets to [[chain complex|chain complexes]], such that the map $A(j \coprod k) \rightarrow A(j) \otimes A(k)$ is a quasi-isomorphism. He showed how these pop up in [[homotopy theory]] all the time. 

(Remark: this formula is the basis for [[Jacob Lurie]]'s discussion of [[commutative algebra in an (infinity,1)-category]] in general and of [[symmetric monoidal (infinity,1)-category]] in particular).

For instance, if $Y$ is any space and $A$ a partial algebra, the resulting total complex can be seen as a generalization of [[Hochschild cohomology]]. One really interesting example (for [[Bruce Bartlett|Bruce]]) was where $Y$ is the interval, and $A$ is the partial algebra of forms on a Riemannian manifold $M$. It turns out that a certain canonical equation which pops out is precisely the Navier-Stokes equation. Gulp!


##### Resources

* [[oberwolfach_june2009_wilson.pdf|Notes by Bruce Bartlett:file]]

* [Notes by Gabriel Drummond-Cole](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_10.pdf)

* [[Oberwolfach Workshop, June 2009 -- Wednesday, June 10|Notes by Urs Scheriber]]

* [[oberwolfach_june2009_pavlov_wilson.pdf|Notes by Dmitry Pavlov:file]]


#### [[Urs Schreiber]], _Background fields in twisted differential nonabelian cohomology_. {#schreiber}

What can I ([[Bruce Bartlett|Bruce]]) say about Urs's talk? Many mere mortals might think it impressive to pass from ordinary cohomology to twisted cohomology, or to differential cohomology, or to nonabelian cohomology. Urs does this all in one step! Yes, we're talking about _twisted differential nonabelian cohomology_. As we all know and love, Urs has developed some $\infty$-machinery based on all sorts of work which enables him to 'turn the crank' and output all the cohomology theories which mathematicians and physicists currently are bumping into. A great application of his machinery is an understanding of the 'Green-Schwarz anomaly cancellation' mechanism in terms of twisted nonabelian String-gerbes with connection and the Chern-Simons 2-gerbe. Unfortunately Urs didn't have time to quite get to that point, but he did at least mention other examples like how his machinery naturally produces the 'twisted Bianchi identities' in twisted flat differential cohomology, as well as nonabelian gerbes. Urs ended his talk by explaining how nonabelian cohomology on $X$ is related to _twisted_ abelian cohomology on $X$. This ties in with Konrad's talk, where the abelian viewpoint is taken, but the nonabelian viewpoint is essential for some applications.

##### Resources

* [[oberwolfach_june2009_schreiber.pdf|Notes by Bruce Bartlett:file]]

* [Notes by Gabriel Drummond-Cole](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_11.pdf)

* Urs's personal nLab write-up on [[schreiber:Background fields in twisted differential nonabelian cohomol|Background fields in twisted differential nonabelian cohomology]]


#### Andr&#233; Henriques, _Invertible conformal nets_. {#henriques}

In this talk, Henriques described joint work with Chris Douglas and Arthur Bartels on the program of establishing an equivalence between full conformal field theories and 'conformal nets'. Preliminary write-ups of this work is available on his [webpage](http://www.math.uu.nl/people/henrique/). A conformal net is something like a [[factorization algebra]] (in the sense of Costello's talk) on 1-dimensional manifolds taking values in the bicategory of Von Neumann algebras with [[bimodule]]s as 1-morphisms. The $\mu$_index $\mu(A)$ of a conformal net $A$ is defined to be the statistical dimension of the vacuum sector $H_0$, viewed as some kind of bimodule involving things which $A$ assigns to arcs on the unit circle. He stated the following result.

+-- {: .un_theorem}
###### Theorem

A [[conformal net]] is invertible if and only if $\mu(A)=1$, and it is fully dualizable (in the sense of Lurie) if and only if $\mu(A) \lt \infty$.
=--

##### Resources

* [Notes by Gabriel Drummond-Cole](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_11.pdf)

*  [[Oberwolfach Workshop, June 2009 -- Thursday, June 11|Notes by Urs Schreiber]]

* [[oberwolfach_june2009_pavlov_henriques.pdf|Notes by Dmitry Pavlov:file]]


#### Andr&#233; Henriques, Evening informal session on more details on conformal nets.

Andr&#233; responded to questions from the audience about further details regarding the 'conformal nets' programme. 

##### Resources
* [[oberwolfach_june2009_henriques_extra.pdf|Notes by Bruce Bartlett:file]]

* Write-up about conformal nets on Andr&#233; Henriques' [webpage](http://www.math.uu.nl/people/henrique/). 



#### [[Konrad Waldorf]], _String connections and Chern-Simons 2-gerbes_. {#waldorf}

Konrad described the [[Chern-Simons 2-gerbe]] $CS_P$ which is a geometric object living on any manifold $M$ which is equipped with a Spin-bundle $P$. Its definition involves some kind of [[pullback]] of the basic bundle gerbe over the Spin group. He demonstrates that a [[string structure]] $S$ on $P$ is a _trivialization_ of this 2-gerbe, in the sense of a morphism from the trivial 2-gerbe living over $M$ to $CS_P$. Such a trivialization only exists precisely if the first fractional Pontryagin class of the bundle vanishes, $\frac{1}{2} p_1(P) = 0$, otherwise the Chern-Simons 2-gerbe is globally nontrivial and a string structure doesn't exist. He defined a  _string connection_ on a string structure $S$ (a connection on $P$ is needed here) on $P$ as a connection on this trivialization $S$ which is compatible with various things.

Basically, the data of a string structure together with a string connection on $P$ is a class in the _$[CS_P]$-twisted_ differential cohomology of $M$ in Urs's sense, for vanishing twist (the twist is the nontriviality of the String structure). Konrad described various results about string connections, such as the fact that they form a contractible space, confirming a conjecture by Stolz and Teichner. See his recent [arXiv article](http://arxiv.org/abs/0906.0117).

##### Resources

* [[oberwolfach_june2009_waldorf.pdf|Notes by Bruce Bartlett:file]]

* [Notes by Gabriel Drummond-Cole](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_11.pdf)

*  [[Oberwolfach Workshop, June 2009 -- Thursday, June 11|Notes by Urs Schreiber]]


#### Kevin Walker, _Blob homology_. {#walker}

Kevin Walker described a new way to think about [[FQFT|extended TQFTs]]. Namely to an n-manifold $M$ and an [[n-category]] $C$ he defined a '[[blob complex]]' $B_*(M, C)$. The construction produces a kind of 'derived version' of an extended TQFT. The idea is that the usual quantum invariants $Z(M)$ to manifolds of dimension $\leq n$ are produced out of this chain complex, with the Atiyah-Segal axioms following as corollaries of the setup. He listed a number of examples of the TQFT's he has in mind in the beginning, such as the finite group model, one based on a *-algebra, one based on a [[pivotal category]], one based on a [[braided monoidal category|braided]] [[ribbon category]], and even one based on contact structures.

##### Resources

*  Slides available on [webpage](http://canyon23.net/math)


#### Ralph Cohen, _String topology, field theories and Fukaya categories. {#cohen}

This talk was about relating the subject of [[string topology]], which is now 10 years old, with other field theories, especially in the light of recent work by Costello, Hopkins and Lurie. [[string theory|String theory]] was described as a 'homological [[conformal field theory]]'. The slogan was that string topology simplifies when one applies Poincar&#233; duality. A relation was sketched between string topology and [[Gromov-Witten theory|Gromov-Witten symplectic field theory]]. Ultimately it was conjectured that the symplectic field theory of $T^*M$ is equivalent to string topology of $M$. 

##### Resources

* [[oberwolfach_june2009_waldorf.pdf|Notes by Bruce Bartlett:file]]

* [Notes by Gabriel Drummond-Cole](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_12.pdf)


#### Corbett Redden, _String structures, 3-forms, and tmf classes_. {#redden}

Corbett began my defining a [[string structure]] on a manifold $M$ as a certain lift of a classifying map; string structures up to homotopy are canonically isomorphic with things called 'string classes' on $M$ - namely, elements in the third integral cohomology of the total space of the bundle which behave on the fibers as the generator of the third cohomology of the Spin group. The point about string structures is that they transgress to give a spin structure on the loop space of the manifold, which is what one wants to study things like the Witten genus. He showed a beautiful way to obtain string structures from a metric on $M$, using Hodge representatives for the forms, and then passing to the 'adiabatic limit', to obtain a certain 3-form $H$. A theorem of Mazzeo-Melrose, Dai and Forman then says that the kernel of the Hodge laplacian extends smoothly in the adiabatic limit, and comes from a filtration in the Serre spectral sequence (something like that). He gave a hypothesis that if a manifold $M^n$ admits a spin and a string structure and a Riemannian metric $g$ such that the Ricci curvature of $g$ is positive and that $H=0$, then a certain invariant $\sigma(M, S)=0$ inside $tmf^{-n}(pt)$. He showed that all these conditions are necessary!

##### Resources

* [[oberwolfach_june2009_redden.pdf|Notes by Bruce Bartlett:file]]

* [Notes by Gabriel Drummond-Cole](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_11.pdf)

* [[Oberwolfach Workshop, June 2009 -- Thursday, June 11|Notes by Urs Schreiber]]


#### Mike Hopkins, _The Kervaire invariant_. {#hopkins}

Mike Hopkins gave a nice story of the history and origins of the [[Kervaire invariant]] in the classification of [[manifold]]s. He spoke about Pontryagin's work about the cobordism groups of stably framed manifolds in the 1930's, and the mistake he made in dimension $n=2$! Basically he thought a certain function was linear, when in fact it was quadratic. This led to the Kervaire invariant being introduced. The problem about when the Kervaire invariant vanishes has been solved in dramatic fashion by Hopkins, Hill and Ravenel very recently... if a manifold has Kervaire invariant $1$, then its dimension must be either 2, 6, 14, 30, 62 or 126, with the final of these remaining open! See the notes for the great story. Hopkins ended with a nice geometric description of the Kervaire invariant on spheres in dimension 2 and 6, relating it to complex structures and exceptional Lie groups. He wondered if these things feature in dimension 126? 

##### Resources

* [[oberwolfach_june2009_hopkins.pdf|Notes by Bruce Bartlett:file]]

* [Notes by Gabriel Drummond-Cole](http://www.math.sunysb.edu/~blafard/tex/sum09/ow_june_12.pdf)

* Andrew Ranicki's [http://www.maths.ed.ac.uk/~aar/exotic.htm](webpage) on exotic spheres 

* Douglas Ravenel's [webpage](http://www.math.rochester.edu/u/faculty/doug/).

#### Mike Hopkins, _Evening informal session on technical details of the solution of the Kervaire invariant problem_. {#hopkins_extra}.

Notes needed... help...


##### Resources
* [[oberwolfach_june2009_freed_extra.pdf|Notes by Bruce Bartlett:file]]

#### David Chataur, _Evening informal session explaining recent results in operads_ {#chataur_extra}.

Notes needed... help...

#### Kishore Marathe, _Evening informal session on the gauge theory to string theory correspondence_ {#marathe_extra}.

Notes needed... help...



# Pictures

* &lt;http://www.mfo.de/cgi-bin/tagung_espe?type=21&tnr=0924>


See also [[Oberwolfach Workshop, June 2009 -- Abstracts|talk summaries]].