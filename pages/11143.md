
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _Dubuc topos_ is a model in which one may apply [[synthetic differential geometry]] to attain results in classical [[differential geometry]]. It is constructed as the [[topos]] of [[sheaves]] for the [[open covering]] [[Grothendieck topology|topology]] on the dual of the [[category]] of [[smooth algebra|C-infinity rings]] presented by a [[germ determined ideal]].


## Definition

+-- {: .num_defn #GermDeterminedCInfinityRing}  
###### Definition
**([[germ-determined C-infinity ring]])**

A finitely generated [[C-infinity ring]] of the form $C^\infty(M)/I$ for some [[smooth manifold]] $M$ and [[ideal]] $I$ is __germ-determined__ if the [[ideal]] $I$ is a [[germ-determined ideal]], which means that for any $f\in I$, if the [[germ]] of $f$ at any point $x$ in the [[zero locus]] of $I$ in $M$ coincides with the [[germ]] of some element of $I$ at $x$, then $f$ itself belongs to $I$. 

Equivalently, germ-determined [[ideals]] are precisely those [[ideals]]
that are closed under (possibly infinite) sums of [[locally finite]] families. One can also take sums with coefficients in a [[partition of unity]].

=--


+-- {: .num_defn #DubucTopos}  
###### Definition
**(Dubuc topos)**

The _Dubuc topos_ is the [[sheaf topos]] on the [[site]] $G$, whose underlying [[category]] is the [[opposite category]] of the [[category]] of [[germ-determined C-infinity ring|germ-determined]] finitely generated [[C-infinity rings]] (Def. \ref{GermDeterminedCInfinityRing}).

The resulting [[opposite category]] is equipped with a [[Grothendieck topology]] as follows. A collection of morphisms $\{A_i\to B\}_{i\in I}$ in this category is a [[covering family]] if for any $i\in I$, the corresponding homomorphism of [[C-infinity rings]] $B \to A_i$ is isomorphic to a [[localization]] map at some element $b_i\in B$.

Here [[localization]] is defined using a universal property formulated in the category of [[C-infinity rings]] and need not  coincide with the usual [[localization of commutative rings]]. Furthermore, we require that applying the functor $\gamma$ to the family $\{A_i\to B\}_{i\in I}$
produces a jointly surjective family of [[continuous maps]] of [[topological spaces]].

Here the functor $\gamma$ is the [[right adjoint functor]] of the [[opposite functor]] of the inclusion of finitely generated point-determined [[C-infinity rings]] into finitely generated germ-determined [[C-infinity rings]]. Concretely, $\gamma(C^\infty(M)/I)$ for a germ-determined [[ideal]] $I$ can be described as the [[zero locus]] of $I$ in $M$,
converted into a finitely generated point-determined [[C-infinity ring]]
using its [[C-infinity ring]] of smooth functions.

Here a finitely generated [[C-infinity ring]] of the form $C^\infty(M)/I$ for some [[smooth manifold]] $M$ and [[ideal]] $I$ is __point-determined__ if the [[ideal]] $I$ is point-determined, which means that for any $f\in I$, if $f(x)=0$ for any point $x$ in the [[zero locus]] of $I$ in $M$, then $f$ itself belongs to $I$.

=--

## Some history
 {#SomeHistory}

_This section is written by [[Eduardo Dubuc]]_.

In papers on [[synthetic differential geometry|SDG]] one can find phrases of the type "We build our model after the standard manner of Moerdijk & Reyes" ([MR] "[[Models for Smooth Infinitesimal Analysis]]", Moerdijk and Reyes, Springer Verlag 1991). Now, this "standard manner" of building models was  developed by Dubuc, and not by Moerdijk-Reyes. Of course, I understand that when a monograph is available, the proper reference is that, and not the original papers. But, phrases as the one quoted above are ambiguous, and the fault is not of the authors.

I resume the history of the subject: In a series of papers and many lectures given specially in Montreal, Sydney, Oberwolfach and elsewhere, I created and started the development of the subject of models of SDG adapted  for the applications to classical [[differential geometry]].
            
1. _Sur les Modeles de la Geometrie Differentielle 
Sinthetyque_, [[Cahiers|Cahiers de Topologie et Geometrie Differentielle]] Vol. XX-3 
(1979).

1. _Schemas C-inf (amplified version of [3], with detailed proofs and many examples)_, "Prepublications de la Universite de Montreal" 80-81 edited by  G. Reyes (1980).

1. _C-inf Schemes_, American Journal of Mathematics, John Hopkins University, Vol. 103-4 (1981).

1. _Open Covers and Infinitary Operations in C-inf-rings_, Cahiers de Topologie et Geometrie Differentielle Vol. XXII-3 (1981).

1. _Integracion de campos vectoriales y Geometria Diferencial Sintetica_, Proceedings of the VII Sem. Nac. de Mat., FAMAF, Univ. Nac. de Cordoba (1984). 

1. _Germ representability and Local integration of vector fields in a well adapted model of SDG_, Aarhus Univ. Math. Inst. preprint series (1985/1986),
(Journal of Pure and Applied Algebra Vol. 64, 1990).

1. _Archimedian Local C-inf-rings and Models of SDG_ (with [[Marta Bunge]]), Cahiers de Topologie et Geometrie Differentielle Vol. XXVII-3 (1986).

1. _Local concepts in SDG and germ representability_ (with Marta Bunge), in  D. Kueker et al. (ads), Mathematical Logic and Theoretical Computer Science, Lecture Notes in Pure and Applied Mathematics 106, Marcel Dekker (1987)
 
            
A) I introduced the concept, coined the name "[[well-adapted model]]", and constructed the first ones. I considered the two essential properties:

i) preservation of all [[open covers]].

ii) preservation of [[transversal maps|transversal]] [[pullbacks]].

B) I started a systematic study of [[smooth algebra|C-infinity rings]] as such. Of course, they were already there, but nothing had been done with them. I even had to state and prove such simple facts as that the algebraic quotient of a C-infinity ring by an R-algebra ideal had a canonical structure of C-infinity ring, and was then the quotient in this category. 

I introduced the key notion of Germ Determined Ideal (or ideal of local nature), which was, as such, nowhere to be found in the literature, and stated and proved their basic properties. This, I think, is the most important concept in the subject. It is the basic definition to start to build upon. It is just the right concept needed. Among other things, I first proved it contains all finitely generated ideals, and defines the largest possible class of C-infinity rings consistent with the [[Nullstellensatz]]. This means that the ring can be seen as the ring of global sections of a C-infinity [[scheme]]. The notion of germ determined ideal also determines the right notion of C-infinity local ring (notice that I do not say local C-infinity ring), that I then developed. I also developed the relative C-infinity version of inverting elements universally, and proved the essential fact that the ring of C-infinity functions defined in an open set $U$ inverts universally a function which is non-zero exactly on $U$ (every Euclidean open is C-infinity  Zariski). 


_When incorporating this work in their monograph Moerdijk and Reyes say (I quote): "Although this general notion of C-infinity  ring does not occur as such in classical analysis and differential geometry, the main examples do ...  Given the role of these examples of C-infinity rings in the classical literature, it is not surprising that although the statements of several of the results in this chapter seem new, most of their proofs are either known or easily derivable from known ones". This is, at the least, misleading, and  I see a clear intention to disqualify my work.  Of course, when the new concepts are introduced, the examples are already there, and the proof of the basic properties is easy. The important thing is to identify explicitly the concept, and to identify the right statements and properties, and this does not come easily. And I repeat, even if C-infinity rings may have been there, the concept of germ determined ideal was not, neither the concept of $C^\infty$-local ring, and several derived concepts and the statements of their basic essential properties neither)._

            
C) With this in hand, I introduced the [[topos]] $G$ of [[sheaves]] for the open covering topology on the dual of the category of C-infinity rings presented by a germ determined ideal, and proved all the basic important properties, which many times are the correct relative C-infinity versions of corresponding properties in [[algebraic geometry]]. This is the analogue in SDG of the [[Zariski topos]] of algebraic geometry (here we should notice that the Zariski topos is defined by the topology of all open covers, this is essential. Moerdijk-Reyes, misunderstanding Zariski, call Smooth-Zariski, the topos determined by the finite covers).

The topos $G$ is the best known model in order to do applications of SDG to classical differential geometry, and as such, it is the most utilized in practice. Many early workers in the subject ([[Jacques Penon|J. Penon]], O. Bruno, M. Bunge, F. Gago, [[David Yetter|Yetter]], among others) called this topos "The Dubuc Topos". Even Moerdijk and Reyes did so in some preprints, although they changed this in the published versions. 

_In their monograph they say (I quote): "As far as terminology is concerned, we have tried to avoid descriptions of the type "the [[Ieke Moerdijk|Moerdijk]] envelop of the Reyes topos", in favor of more informative ones". But the true fact was that the only name that was involved was "Dubuc", since no other new name was being utilized at the time (of course, things as [[Kock-Lawvere axiom]] or [[Weil algebras]] were not aimed by this philosophy, and "Moerdijk envelop of the Reyes topos" was an invention to reduce to the ridiculous, the fact of naming things after "Dubuc"._
            
D)  I should mention here that I do not ignore the fact that my work is  acknowledged and referenced in the monograph, but the matter is much more subtle, and nobody can deny the evidence of the following consequence of their maneuvering:
 
My name, as time passes, and as young people appear, is less and less credited with a subject that I created and developed, namely, models of SDG adapted to classical differential geometry. People talk as if the well adapted models were always there, or start referring to them in a way that lead inexperienced (in the subject)  readers  to believe that these constructions are "M-R way of doing models", as I quoted at the  beginning of this note. 

E) This does not do justice to my work, and does not corresponds to the true history of the subject.  As an starting point to remedy it, I request all workers that need to use the topos $G$, to refer to it as "Dubuc Topos". After all, it is a long tradition in mathematics to associate proper names to important concepts or constructions when it is justified, as I believe it is the case here. 

                              
**REMARK.**  Proposition 18 and Theorem 22 of 6. cited above establish that postulate WA2 (II, 3.2, 3.3) of 8. holds in the Dubuc Topos. However, there is a mistake (discovered by [[Michael Makkai|M. Makkai]]) in Lemma 21 of 6. which invalidates the proof. I believe that the result is true but I am not working to fix the proof now. The external statement holds, it is easy and it proved in 5. cited above.


## Related entries

* [[Cahiers topos]]

## References

* [[Eduardo Dubuc]], _Sur les mod&#232;les de la g&#233;om&#233;trie diff&#233;rentielle synth&#233;tique_, [[Cahiers|Cahiers de Topologie et Geometrie Differentielle]] Vol. XX-3 
(1979) ([numdam:CTGDC_1979__20_3_231_0](http://www.numdam.org/item?id=CTGDC_1979__20_3_231_0))

* [[Eduardo Dubuc]], _Schemas $C^\infty$_, "Prepublications de la Universite de Montreal" 80-81 edited by  G. Reyes (1980).

This preprint is an amplified version of the following article, with detailed proofs and many examples:

* [[Eduardo Dubuc]], _$C^\infty$ Schemes_, American Journal of Mathematics, John Hopkins University, Vol. 103-4 (1981) ([jstor:2374046](http://www.jstor.org/stable/2374046))

* [[Eduardo Dubuc]], _Open Covers and Infinitary Operations in C-inf-rings_, [[Cahiers|Cahiers de Topologie et Geometrie Differentielle]] Vol. XXII-3 (1981) ([numdam:CTGDC_1981__22_3_287_0](http://www.numdam.org/item?id=CTGDC_1981__22_3_287_0))

* [[Eduardo Dubuc]], _Integracion de campos vectoriales y Geometria Diferencial Sintetica_, Proceedings of the VII Sem. Nac. de Mat., FAMAF, Univ. Nac. de Cordoba (1984). [journal volume](http://inmabb.criba.edu.ar/revuma/revuma.php?p=toc/vol35), [pdf](http://inmabb.criba.edu.ar/revuma/pdf/v35/p151-162.pdf)

* [[Eduardo Dubuc]], _Germ representability and Local integration of vector fields in a well adapted model of SDG_, Aarhus Univ. Math. Inst. preprint series (1985/1986), published in Journal of Pure and Applied Algebra Vol. 64, (1990) (<a href="https://doi.org/10.1016/0022-4049(90)90152-8">doi:10.1016/0022-4049(90)90152-8</a>)

* [[Marta Bunge]], [[Eduardo Dubuc]], _Archimedian Local C-inf-rings and Models of SDG_, [[Cahiers|Cahiers de Topologie et Geometrie Differentielle]] Vol. XXVII-3 (1986) ([numdam:CTGDC_1986__27_3_3_0](http://www.numdam.org/item?id=CTGDC_1986__27_3_3_0))

* [[Marta Bunge]], [[Eduardo Dubuc]], _Local concepts in SDG and germ representability_, in  D. Kueker et al. (ads), Mathematical Logic and Theoretical Computer Science, Lecture Notes in Pure and Applied Mathematics 106, Marcel Dekker (1987)

Penon's thesis has an appendix on the Dubuc topos:

* [[Jacques Penon]], _De l'infinit&#233;simal au local_ (Th&#232;se de Doctorat d'&#201;tat). [[Diagrammes]], S13 (1985), p. 1-191 ([numdam:DIA_1985__S13__1_0](http://www.numdam.org/item?id=DIA_1985__S13__1_0))


