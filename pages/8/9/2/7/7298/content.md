
> This entry is about what in [[nonstandard analysis]] are called *monads*. For disambiguation see at *[[monad (disambiguation)]]*.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Infinitesimal neighbourhoods
* table of contents
{: toc}

## Idea

> *Der unendlich kleinste Theil des Raumes ist immer ein Raum, etwas, das Continuität hat, nicht aber ein blosser Punct* ([Fichte 1795, Grundriss &#167;4.IV](Grundriss+des+Eigenth&#252;mlichen+der+Wissenschaftslehre#4IVUnendlichKleinsterTeilDesRaumes))

> ("An infinitesimally small part of space is always a space, something with continuity, but not a bare point.")


An infinitesimal neighbourhood is a "[[neighbourhood]] with [[infinitesimal]] diameter". This can be made precise in several formalisms, including [[nonstandard analysis]], [[ringed spaces]], [[synthetic differential geometry]], [[differential cohesion]], ....

{#MonadTerminology} **"Monads".** In [[nonstandard analysis]]   the infinitesimal neighbourhood of a point is traditionally called (see [below](#InNonstandardAnalysis)) its *[[monad (disambiguation)|monad]]*, apparently following the [ancient terminology going back to Euclid](monad+disambiguation#HistoricalOrigins), for more see [there](monad+disambiguation#HistoricalOrigins).

Curiously, in [[differential cohesion]] the construction of all infinitesimal neighbourhoods (the [[infinitesimal disk bundle]]) is indeed a [[monad]] in the sense of [[category theory]] (see [there](infinitesimal+disk+bundle#MonadicityAdjointToJetBundles), namely the [[left adjoint|left]] [[adjoint monad]] to the [[jet comonad]]). Whether this confluence of the terms "monads" is just a happy coincidence seems to be lost to history, see at *[[monad]]* the section *[Etymology](monad#Etymology)*.




## Definition


### In nonstandard analysis
 {#InNonstandardAnalysis}

In [[nonstandard analysis]], the 

* "*[[monad (disambiguation)|monad]]*"  ([Robinson 1966, p. 57](#Robinson66) following , see also [Luxemburg 1966](#Luxemburg66), [Keisler 1976, Def. 1.2](#Keisler76), [Kutateladze 2011](#Kutateladze11)) 

or 

* "*halo*" (eg. [Rayo 2015, Def. 4.11](#Rayo15))

of a standard point $p$ in a [[topological space]] (or even in a [[Choquet space]]) is the hyperset of all [[hyperpoints]] infinitely close to $p$. It is  the (external) set constructed as the [[intersection]] of all of the standard [[neighbourhoods]] of $p$, the _infinitesimal neighbourhood_ of $p$.

Some

### In differential cohesion
 {#DifferentialCohesion}

For $\mathbf{H}$ a context of [[differential cohesion]] with [[infinitesimal shape modality]] $\Im$, then for $x\colon \ast \to X$ a [[global point]] in any object $X \in \mathbf{H}$ the infinitesimal disk $\mathbb{D}^X_x \to X$ around that point is the ([[homotopy pullback|homotopy]]) [[pullback]] of the [[unit of a monad|unit]] $i \colon X \to \Im(X)$ of the $\Im$-monad

$$
  \array{
    \mathbb{D}^X_x &\longrightarrow& X
    \\
    \downarrow && \downarrow^{\mathrlap{i}}
    \\
    \ast &\stackrel{x}{\longrightarrow}& \Im(X)
  }
  \,.
$$

The collection of all infinitesimal disks forms the *[[infinitesimal disk bundle]]* over $X$, see there for more.


### For ringed spaces

Consider a morphism $(f,f^\sharp):(Y,\mathcal{O}_Y)\to(X,\mathcal{O}_X)$ of [[ringed space]]s for which the corresponding map $f^\sharp:f^*\mathcal{O}_X\to\mathcal{O}_Y$ of sheaves on $Y$ is surjective. Let $\mathcal{I} = \mathcal{I}_f = Ker\,f^\sharp$, then $\mathcal{O}_Y = f^\sharp(\mathcal{O}_X)/\mathcal{I}_f$. The ring $f^*(\mathcal{O}_Y)$ has the $\mathcal{I}$-preadic filtration which has the associated graded ring $Gr_\bullet =\oplus_{n} \mathcal{I}_f^n/\mathcal{I}^{n+1}_f$ which in degree $1$ gives the [[conormal sheaf]] $Gr_1 = \mathcal{I}_f/\mathcal{I}^2_f$ of $f$. The $\mathcal{O}_Y$-augmented ringed space $(Y,f^\sharp(\mathcal{O}_X)/\mathcal{I}^{n+1})$ is called the $n$-th __infinitesimal neighborhood__ of $Y$ along morphism $f$. Its structure sheaf is called the $n$-th normal invariant of $f$. 



## Related concepts

* [[jet groupoid]]


[[!include infinitesimal and local - table]]


## References

In [[algebraic geometry]] (via [[infinitesimal shape modality]]):

* [[A. Grothendieck]], _&#201;l&#233;ments de g&#233;om&#233;trie alg&#233;brique (r&#233;dig&#233;s avec la collaboration de Jean Dieudonn&#233;) : IV. &#201;tude locale des sch&#233;mas et des morphismes de sch&#233;mas, Quatri&#232;me partie_, Publications Math&#233;matiques de l'IH&#201;S __32__ (1967), p. 5-361, [numdam](http://www.numdam.org/item?id=PMIHES_1967__32__5_0)

Discussion of infinitesimal neighbourhoods in [[nonstandard analysis]] and use of the "[[monad (disambiguation)|monad-terminology]]":

* {#Robinson66} [[Abraham Robinson]], p. 57 of: *Non-standard analysis*, Studies in Logic and the Foundations of Mathematics **42**, North-Holland (1966), Princeton University Press (1996) &lbrack;[ISBN:9780691044903](https://press.princeton.edu/books/paperback/9780691044903/non-standard-analysis)&rbrack;

* {#Luxemburg66} [[Wilhemus A. J. Luxemburg]], *A General Theory of Monads*, in: *Applications of Model Theory to Algebra, Analysis and Probability*, Holt, Rinehart and Minston (1966) 18–86 &lbrack;[ark](https://archive.org/stream/in.ernet.dli.2015.141486/2015.141486.Applications-Of-Model-Theory-To-Algebra-analysis-And-Probability_djvu.txt)&rbrack;

* E. I. Gordon, A. G. Kusraev, [[Semën S. Kutateladze]], Chapter 4 in: *Infinitesimal Analysis*, Mathematics and its Applications **544**, Springer (2002) &lbrack;[doi:10.1007/978-94-017-0063-4](https://doi.org/10.1007/978-94-017-0063-4)&rbrack;

* {#Keisler76} [[Jerome Keisler]], Def. 1.2 in: *Foundations of Infinitesimal Calculus*, Prindle Weber & Schmidt (1976, 2022) &lbrack;[pdf](https://people.math.wisc.edu/~hkeisler/foundations.pdf)&rbrack;

* {#Kutateladze11} [[Semën S. Kutateladze]], *Leibnizian, Robinsonian, and Boolean valued monads*, Journal of Applied and Industrial Mathematics **5** 3 (2011) 365-373 &lbrack;[arxiv/1106.2755](http://arxiv.org/abs/1106.2755), [doi:10.1134/S1990478911030082](https://doi.org/10.1134/S1990478911030082)&rbrack;

* [[Sergio Albeverio]], Jens Erik Fenstad, Raphael Hoegh-Krohn, *Nonstandard methods in stochastic analysis and mathematical physics*, Academic Press 1986

and using the "*halo*"-terminology:

* Robert Lutz, Michel Goze; p. 5 of: *Nonstandard Analysis -- A Practical Guide with Applications*, Lecture Notes in Mathematics **881**, Springer (1981) &lbrack;[doi:10.1007/BFb0093397](https://doi.org/10.1007/BFb0093397)&rbrack;


* Francine Diener, Marc Diener, p. 6, 11 of: *Tutorial*, chapter 1 of: *Nonstandard analysis in practice*, Universitext, Springer (1995) &lbrack;[doi:10.1007/978-3-642-57758-1](https://doi.org/10.1007/978-3-642-57758-1)&rbrack;


* {#Rayo15} Diego Rayo, Def. 4.11 in: *Introduction to non-standard analysis* (2015) &lbrack;[pdf](http://math.uchicago.edu/~may/REUDOCS/Rayo.pdf)&rbrack;

See also:

 * Wikipedia, *[Monad (non-standard analysis)](http://en.wikipedia.org/wiki/Monad_%28non-standard_analysis%29)*

More historical commentary on the [[monad (disambiguation)|monad-terminology]]

* {#Kutateladze06} [[Semën S. Kutateladze]], *Leibniz's Definition of Monad*, NeuroQuantology **4** 3 (2006) 249-241 &lbrack;[arXiv:math/0608298](https://arxiv.org/abs/math/0608298), [pdf](https://www.researchgate.net/profile/Semen-Kutateladze/publication/2130297_Leibniz%27s_Definition_of_Monad/links/0912f5058405405dbb000000/Leibnizs-Definition-of-Monad.pdf)&rbrack;


Discussion in [[synthetic differential geometry]], also using the "monad"-terminology:

* {#Kock80} [[Anders Kock]], _Formal manifolds and synthetic theory of jet bundles_, Cahiers de Topologie et Géométrie Différentielle Catégoriques **21** 3 (1980)  &lbrack;[numdam:CTGDC_1980__21_3_227_0](http://www.numdam.org/item?id=CTGDC_1980__21_3_227_0)&rbrack;


Discussion in [[differential cohesion]] (see at *[[infinitesimal disk bundle]]*):

* [[Igor Khavkine]], [[Urs Schreiber]], _[[schreiber:Synthetic variational calculus|Synthetic geometry of differential equations: I. Jets and comonad structure]]_ ([arXiv:1701.06238](https://arxiv.org/abs/1701.06238))

and its formalization in differentially [[cohesive homotopy type theory]]:

* {#Wellen17} [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_ (2017)



[[!redirects infinitesimal neighborhood]]
[[!redirects infinitesimal neighborhoods]]
[[!redirects infinitesimal neighbourhood]]
[[!redirects infinitesimal neighbourhoods]]

[[!redirects monad in nonstandard analysis]]
[[!redirects monads in nonstandard analysis]]
[[!redirects monad in non-standard analysis]]
[[!redirects monads in non-standard analysis]]

[[!redirects halo]]
[[!redirects halos]]
[[!redirects haloes]]

[[!redirects infinitesimal halo]]
[[!redirects infinitesimal halos]]
[[!redirects infinitesimal haloes]]


[[!redirects infinitesimal disk]]
[[!redirects infinitesimal disks]]

