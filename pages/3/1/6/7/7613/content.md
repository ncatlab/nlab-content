
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

There are various hints (originally observed in [Witten 95](#Witten95)) that all [[perturbation theory|perturbative]] [[superstring theories]] ([[type II string theory|type II]] (A and B), [[type I string theory|type I]], [[heterotic string theory|heterotic]] ($SO(32)$ and $E_8 \times E_8$)) have a joint [[coupling constant|strong coupling]] [[non-perturbative quantum field theory|non-perturbative]] limit whose low energy [[effective field theory]] description is [[11-dimensional supergravity]] and which reduces to the various string theories by [[Kaluza-Klein compactification]] on an [[orientifold]] torus bundle, followed by various [[duality in string theory|string dualities]]. Since the string itself is thought to arise from a [[membrane]]/[[M2-brane]] in 11-dimensions after [[double dimensional reduction]] this hypothetical theory has been called "M-theory" short for "membrane theory"; e.g. in [Horava-Witten 95](#HoravaWitten95):

> As it has been proposed that the eleven-dimensional theory is a supermembrane theory but there are some reasons to doubt that interpretation, we will non-committally call it the _M-theory_, leaving to the future the relation of M to membranes.

The "reasons to doubt" that interpretation is that the [[M2-brane]] does not support a [[perturbation theory]] the way that the [[superstring]] does. This is part of the reason why the actual nature of "M-theory" remains mysterious. On the other hand, later it was argued that there is a regularization of the M2-brane worldvolume theory, which makes it becomes the [[BFSS matrix model]] ([Nicolai-Helling 98](#NicolaiHelling98), [Dasgupta-Nicolai-Plefka 02](#DasguptaNicolaiPlefka02)). In reaction to these developments it was suggested that "M-theory" could be read as "matrix theory".

> Later, the membranes were interpreted in terms of matrices. Purely by chance, the word "matrix" also starts with "m", so for a while I would say that the M stands for magic, mystery, or matrix. ([Witten 14, last paragraph](#Witten14))

The defining characteristic of M-theory is that it exhibits [[duality between M-theory and type IIA string theory|duality with type IIA string theory]] in the following way:


$$
  \array{
      M-Theory(?) &\stackrel{low\;energy\;limit}{\to}& 11d Supergravity
      \\
      {}^{\mathllap{ \array{ small \\ coupling \\ limit}}}\downarrow && \downarrow^{\mathrlap{ \array{KK\;reduction \\ on S^1 }}}
      \\
      type IIA string theory 
        &\stackrel{low\;energy\;effective\;QFT}{\to}&  
      10d Supergravity
  }
$$

(see also e.g. ([Obers-Pioline 98, p. 12](#ObersPioline98))). The unknown top left corner here has optimistically been given a name, and that is "M-theory". But even the rough global structure of the top left corner has remained elusive. 

> We still have no fundamental formulation of "[[M-theory]]" - the hypothetical theory of which [[11-dimensional supergravity]] and the five [[string theories]] are all special limiting cases. Work on formulating the fundamental principles underlying M-theory has noticeably waned. $[...]$. If history is a good guide, then we should expect that anything as profound and far-reaching as a fully satisfactory formulation of M-theory is surely going to lead to new and novel mathematics. Regrettably, it is a problem the community seems to have put aside - temporarily. But, ultimately, Physical Mathematics must return to this grand issue.

> ([Moore 14, section 12](Physical+Mathematics+and+the+Future#Moore14))


## Hints

The available evidence that there is something of interest consists of various facets of the bottom left and the top right entry of the above diagram, that seem to have a common origin in the top left corner.

### Membranes

Notably, from the [[black brane]]-solution structure in [[11-dimensional supergravity]] and from the [[brane scan]] one finds that it contains a 2-[[brane]], called the _[[M2-brane]]_, and to the extent that one has this under control one can show that under "double dimensional reduction" this becomes the [[string]]. However, it is clear that this cannot quite give a definition of the top left corner by [[perturbation theory]] as the [[superstring]] [[sigma-model]] does for the bottom left corner. At the bottom of it,  this is simply because, by the very nature of the conjecture, the top left corner is supposed to be given by a non-perturbative strong-coupling limit of the bottom left corner. But one may also see that the evident guess for a would-be membrane analog of the [[string perturbation series]] fails

> {#WittenOnProblemsOfMembraneTheory2014} [[Mike Duff]], [[Paul Townsend]], and other physicists working on [[supermembranes]] had spent a couple of years in the mid-1980s saying that there should be a theory of fundamental membranes analogous to the theory of fundamental strings. That wasn't convincing for a large number of reasons. For one thing, a three-manifold doesn't have an [[Euler characteristic]], so there isn't a topological expansion as there is in string theory. Moreover, in three dimensions there is no [[conformal invariance]] to help us make sense of membrane theory; membrane theory is [[renormalization|nonrenormalizable]] just like [[general relativity]]. 

> ([[Edward Witten]] in interview by [[Hirosi Ooguri]], Notices
Amer. Math. Soc, May 2015 p491 ([pdf](http://www.ams.org/notices/201505/rnoti-p491.pdf)))

This issue is the very root of the abbreviation "M-theory":

> As it has been proposed that the eleven-dimensional theory is a supermembrane theory but there are some reasons to doubt that interpretation, we will non-committally call it the _M-theory_, leaving to the future the relation of M to membranes. ([Horava-Witten 95](#HoravaWitten95))

> {#Witten14LastParagraph} M-theory was meant as a temporary name pending a better understanding. Some colleagues thought that the theory should be understood as a membrane theory. Though I was skeptical, I decided to keep the letter "m" from "membrane" and call the theory M--theory, with time to tell whether the M stands for magic, mystery, or membrane. Later, the membranes were interpreted in terms of matrices. Purely by chance, the word "matrix" also starts with "m", so for a while I would say that the M stands for magic, mystery, or matrix. ([Witten 14, last paragraph](#Witten14))


### Strongly coupled type IIA strings and D$0$-branes
 {#StronglyCoupledTypeIIAAndD0Branes}

There is a bunch of consistency checks on the statement that the [[KK-compactification]] of [[11-dimensional supergravity]] on a circle gives the [[non-perturbative quantum field theory|strong coupling]] refinement of [[type IIA string theory]]. See at _[[duality between M-theory and type IIA string theory]]_.

One aspect of this is that [[type IIA string theory]] with a [[condensate]] of [[D0-branes]] behaves like a 10-dimensional theory that develops a further circular dimension of [[radius]] scaling with the density of [[D0-branes]].  ([Banks-Fischler-Shenker-Susskind 97](#BanksFischlerShenkerSusskind97), [Polchinski 99](#Polchinski99)). See also ([FSS 13, section 4.2](#FSS13)).

Discussion of the relation of [[gauge enhancement]] of M-theory at [[ADE singularities]] and the corresponding coincident [[D-brane]] geometries in type IIA string theory is in ([Sen 97](#Sen97)).

More on the decomposition of the [[nLab:supergravity C-field]] in 11d to the [[RR-fields]] and the NS-fields in type IIA is in ([Mathai-Sati 03, section 4](#MathaiSati03)).

For survey of how the components maps see also the table at _[Relation to F-theory](#RelationToFTheory)_.

### U-duality

Another hint comes from the fact that the [[U-duality]]-structure of [[supergravity]] theories forms a clear pattern in those dimensions where one understands it well, giving rise to a description of higher dimensional supergravity theories by [[exceptional generalized geometry]]. Now, this pattern, as a mathematical pattern, can be continued to the case that would correspond to the top left corner above, by passing to [[exceptional generalized geometry]] over _hyperbolic_ [[Kac-Moody Lie algebras]] such as first [[E10]] and then, ultimately [[E11]]. The references there show that these are huge algebraic structures inside which people incrementally find all kinds of relations that are naturally identified with various aspects of M-theory. This leads to the conjecture that M-theory somehow _is_ $E_{11}$ in some way. But it all remains rather mysterious at the moment.

### Relation to F-theory
 {#RelationToFTheory}

The [[KK-compactification|compactification]] of M-theory on a torus yields [[type II string theory]] -- directly type IIA, and then type IIB after [[T-duality|T-dualizing]]. It turns out that the [[axio-dilaton]] of the resulting type II-B string theory is equivalently the [[complex structure]]-[[moduli|modulus]] of this [[elliptic fibration]] by the compactification torus. This gives a description of [[non-perturbative quantum field theory|non-perturbative]] aspects of type II which has come to be known as _[[F-theory]]_ (see e.g. [Johnson 97](#Johnson97)).
 
In slightly more detail, write, topologically, $T^2 = S^1_A\times S^1_B$ for the compactification torus of M-theory, where contracting the first $S^1_A$-factor means passing to type IIA. To obtain type IIB in noncompact 10 dimensions from M-theory,  also the second $S^1_B$ is to be compactified (since [[T-duality]] sends the radius $r_A$ of $S^1_A$ to the inverse radius $r_B = \ell_s^2 / R_A$ of $S^1_B$).
Therefore type IIB sugra in $d = 10$ is obtained from 11d sugra compactified on the [[torus]] $S^1_A \times S^1_B$. More generally, this torus may be taken to be an [[elliptic curve]] and this may vary over the 9d base space as an [[elliptic fibration]]. 

Applying T-duality to one of the compact direction yields a 10-dimensional theory which may now be thought of as encoded by a 12-dimensional elliptic fibration. This 12d elliptic fibration encoding a 10d type II supergravity [[vacuum]] is the input data that [[F-theory]] is concerned with.

A schematic depiction of this story is the following:

|  |  |  |
|--|--|--|
| [[11d supergravity|M-theory]] in $d = 11$ | | F-theory in $d = 12$ |
| $\downarrow$ [[Kaluza-Klein mechanism|KK-reduction]] along [[elliptic fibration]] | | $\downarrow$ [[axio-dilaton]] is modulus of [[elliptic fibration]] |
| [[type IIA string theory|IIA string theory]] in $d = 9$ | $\leftarrow$[[T-duality]]$\rightarrow$ | [[type IIB string theory|IIB string theory]] in $d = 10$ |

In the simple case where the elliptic fiber is indeed just $S^1_A \times S^1_B$, the [[imaginary part]] of its complex modulus is

$$
  Im(\tau) = \frac{R_A}{R_B}
  \,.
$$

By following through the above diagram, one finds how this determines the [[coupling constant]] in the [[type II string theory]]:

First, the [[KK-compactification]] of M-theory on $S^1_A$ yields a type IIA [[string coupling constant]]

$$
  g_{IIA} = \frac{R_A}{\ell_s}
  \,.
$$

Then the T-duality operation along $S^1_B$ divides this by $R_B$:

$$
  \begin{aligned}
    g_{IIB} & = g_{IIA} \frac{\ell_s}{R_B} 
    \\
    & = \frac{R_A}{R_B}
    \\
    & = Im(\tau)
   \end{aligned}
   \,.
$$

[[!include F-branes -- table]]

### Cohomological properties

A derivation of [[D-brane charge]], [[RR-fields]] and other [[K-theory]] structure in [[type II superstring theory]] from M-theory was argued in ([FMW 00](#FMW00)).

See also at _[[cubical structure in M-theory]]_.

### Kaluza-Klein compactifications

[[!include KK-compactifications of M-theory -- table]]


### Via AdS/CFT

The [[AdS-CFT duality]] for the [[black brane|black]][[M5-brane]] may be turned around to deduce from the [[6d (2,0)-superconformal QFT]] on the [[M5-brane]] [[scattering amplitudes]] in the 11-dimensional [[bulk]]-spacetime, hence in putative M-theory. While the [[6d (2,0)-superconformal QFT]] is not completely known, [[conformal invariance]] and [[supersymmetry]] tightly constrains it ("[[conformal bootstrap]]") and does allow to extract results.

This approach to computing putative M-theory scattering amplitudes is due to  ([ChesterPerlmutter18](#ChesterPerlmutter18)).


### More

(...)

## The open problem of formulating M-theory
 {#TheOpenProblem}

The tight web of hints and plausiblity checks notwithstanding, an actual formulation of M-theory as an actual [[theory (physics)|theory]] remains an open problem. 

This is not outrageous in itself: In [[mathematics]] there are good examples of cases where a collection of situations was or is suspected to be limiting cases of a single unified theory, without that theory itself having been or being known. 

One example of this is the putative theory "absolute geometry over the [[field with one element]]". In this [[analogy]], the various [[perturbative string theories]] ([[heterotic string theory|HET]], [[type I string theory|I]], [[type IIA string theory|IIA]], [[type IIB string theory|IIB]] and their [[KK-compactifications]]) correspond to [[arithmetic geometry|arithmetic geometries]] over [[ground field|base]] [[prime field]] $\mathbb{F}_p$ for $p \geq 2$, and the would-be M-theory corresponds to a  theory of a "[[field with one element]]" that unifies all this, by describing it at a deeper level (literally: a deeper base). 

On the other hand, parts of the physics-minded literature tends to forget or downplay the [[conjecture|conjectural]] nature of many assumptions or leaps of faiths that are being made when it comes to discussion of [[D-brane]]/[[M-brane]] dynamics and generally of [[non-perturbative effects]] in string theory. 

The following is a collection of quotes from authors that highlight the open problem:

### General
 {#OpenProblemGeneral}


[Duff 96, totality of Section 6](#Duff96):

> The overriding problem in superunification in the coming years will be to take the Mystery out of M-theory, while keeping the Magic and the Membranes.

\linebreak

[Howe-Lambert-West 97, p. 2](DpDp2-brane+bound+state#HoweLambertWest97):

> the still rather mysterious M theory governs many aspects of the lower dimensional string theories.  What little is known of M theory is powerful enough to lead us to new phenomena in string theory and indeed new string theories.  In particular the M theory fivebrane is strongly believed hold a new kind of self-dual string theory on its worldvolume. This new and somewhat elusive theory has also appeared in other contexts such as the compactification of type IIB string theory on K3 , M(atrix) theory on $\mathbb{T}^5$ and the S-duality of $N = 4$, $D = 4$ super-Yang-Mills. Thus one may hope that a greater understanding of this self-dual string may lead directly to a greater understanding of duality, string theory and M theory.

\linebreak

[Duff 98a, last paragraph (p. 6)](#Duff98):

> Despite all these successes, physicists are glimpsing only small corners of M-theory; the big picture is still lacking.

> $[...]$

> Indeed future historians may judge the late 20th century as a time when theorists were like  children  playing  on  the  seashore, diverting themselves with the smoother pebbles or prettier shells of superstrings while the great ocean of M-theory lay undiscovered before them.

\linebreak

[Duff 98b, p. 6](#Duff98b):

> we are only just beginning to scratch the surface of the ultimate meaning of M-theory, and for the time being therefore, M stands for Magic and Mystery too.

\linebreak

[Nicolai-Helling 98, p. 2](BFSS+matrix+model#NicolaiHelling98):

> Despite the recent excitement, however, we do not think that [[BFSS matrix model|M(atrix) theory]] and the [[M2-brane|d= 11 supermembrane]] in their present incarnation are already the final answer in the search for [[M-theory|M-Theory]], even though they probably are important pieces of the puzzle. There are still too many ingredients missing that we would expect the final theory to possess. For one thing, we would expect a true theory of quantum gravity to exhibit certain pregeometrical features corresponding to a “dissolution” of space-time and the emergence of some kind of non-commutative geometry at short distances; although the matrix model does achieve that to some extent by replacing commuting coordinates by non-commuting matrices, it seems to us that a still more radical departure from conventional ideas about space and time may be required in order to arrive at a truly background independent formulation (the matrix model “lives” in nine _flat_ transverse dimensions only). Furthermore, there should exist some huge and so far completely hidden symmetries generalizing not only the duality symmetries of extended supergravity and string theory, but also the principles underlying general relativity.

\linebreak

[Duff 99, p.330](#Duff99):

> future historians may judge the period 1984-95 as a time when theorists were like boys playing by the sea shore, and diverting themselves with the smoother pebbles or prettier shells of perturbative ten-dimensiorial superstrings while the great ocean of non-perturbative eleven-dimensional M-theory lay all undiscovered before them. 

\linebreak

{#CGNT04} [Cederwall-Gran-Nilsson-Tsimpis 04](higher+curvature+correction#CGNT04):

> Our understanding of M-theory is still very limited, mainly due to the lack of powerful methods to probe it at the microscopic level. One approach to encoding information about M-theory is through its low energy [[effective field theory]]. $[...]$ The ultimate goal is to be able to derive the [[higher curvature corrections|higher derivative corrections]], e.g. by means of a microscopic version of M-theory. Since this is not yet possible, our aim here is instead to solve the [[superspace]] [[Bianchi identities]] in order to obtain the most general form such correction terms can take restricted only by [[supersymmetry]] and [[Lorentz group|Lorentz invariance]] in eleven dimensions. To what extent such an approach can capture main features of M-theory is an interesting question to which we have no answer at this point.

\linebreak

{#Moore14} [[Physical Mathematics and the Future|Moore 14, pages 43-44]]:

>  We still have no fundamental formulation of "[[M-theory]]" - the hypothetical theory of which [[11-dimensional supergravity]] and the five [[string theories]] are all special limiting cases. Work on formulating the fundamental principles underlying M-theory has noticeably waned. 

> {#AGoodStartWasGivenByTheMatrixTheory} A good start was given by the [[BFSS matrix model|Matrix theory]] approach of [[Tom Banks|Banks]], [[Willy Fischler|Fischler]], [[Stephen Shenker|Shenker]] and [[Leonard Susskind|Susskind]]. We have every reason to expect that this theory produces the correct [[scattering amplitudes]] of modes in the [[11-dimensional supergravity]] multiplet in 11-dimensional [[Minkowski space]] - even at energies sufficiently large that [[black holes]] should be created. (This latter phenomenon has never been explicitly demonstrated). But [[BFSS matrix model|Matrix theory]] is only a beginning and does not give us the whole picture of [[M-theory]]. The program ran into increasing technical difficulties when more complicated [[KK-compactification|compactifications]] were investigated. (For example, compactification on a six-dimensional torus is not very well understood at all. $[...]$). Moreover, to my mind, as it has thus far been practiced it has an important flaw: It has not led to much significant new mathematics. 

\linebreak

[Chester-Perlmutter 18, p. 2](conformal+bootstrap#ChesterPerlmutter18):

> given our utter lack of a complete description of [[M-theory]], the [[bulk]] is  not terribly useful for determining finite aspects of the [[AdS/CFT|dual CFT]]. However, we can turn this problem around using the modern perspective of the [[conformal bootstrap]], which gives an a priori independent formulation of the (local sector of the) CFT. This provides an independent tool for constructing M-theory at the non-perturbative level, a philosophy that we will substantiate in this work.

\linebreak

{#Witten19} [Witten 19, USN Interview](Edward+Witten#WhatIsMissing):

> I actually believe that string/M-theory is on the right track toward a deeper explanation.  But at a very fundamental level it’s not well understood. And I’m not even confident that we have a good concept of what sort of thing is  missing or where to find it. The reason I am not is that in hindsight it is clear the view given in the 1980s of what is missing was too narrow. Instead of discovering what we thought was missing, we broadened the picture in the 90s, in unexpected directions.


\linebreak

{#Duff19} [Duff 19, USN interview](Michael+Duff#WeDontKnowWhatItIs):


> The problem we face is that we have a patchwork understanding of M-theory, like a quilt. We understand this corner and that corner, but what's lacking is the overarching big picture. So directly or indirectly, my research hopes to explain what M-theory really is. We don't know what it is. 

> In a certain sense, and this is not a popular statement, I think it's premature to be asking: "What are the empirical consequences", because it's not yet in a mature enough state, where we can sensibly make falsifiable prediction.

\linebreak

{#Duff20} [[Duff interview at M-Theory-Mathematics 2020]]:

> (06:59) But the matrix model itself was not all of M-theory; it was a corner of M-theory, and it told us certain interesting things, but there were interesting things about M-theory that it didn't tell us. 

> (07:13) I think we are still looking, in fact, for what M-theory really is.  

> (07:19) We have a patchwork picture. We understand various corners. But the overarching big picture of M-theory is still waiting to be discovered, in my view. 

> (08:12) M-theory in 1995 was very promising, and it's taught us a lot about the fundamental interactions; but the final theory is still not with us. 

> (12:46) I wouldn't like to predict what the ultimate picture of M-theory will be; I imagine it will be something quite different from what we can imagine now. 

> (16:36) That's why I think M-theory is not yet in a mature enough stage for us to make falsifiable predictions.

> (16:44) We don't understand the theory sufficiently well yet to do so.


### Non-abelian DBI-action
 {#OpenProblemNonabelianDBI}

A key ingredient of [[M-theory]] is supposedly the physics of [[intersecting branes]] with [[gauge enhancement]] in their [[worldvolume]] [[super Yang-Mills theory]]/[[DBI field theory]]. But the actual derivation or even formulation of the expected [[non-abelian DBI action]] remains open:

\linebreak


[Taylor-VanRaamsdonk 99, p. 1](Dirac-Born-Infeld+action#TaylorVanRaamsdonk99):

> For a system of multiple D$p$-branes, the world-volume action is much less well understood than for a single brane. The extension of $[$  the [[super Yang-Mills theory|super Yang-Mills action]] $]$ to a full super-symmetric or [[kappa-symmetry|κ-symmetric]] [[nonabelian Born-Infeld action]] is not known. 

> $[$the proposal by [Tseytlin 97](Dirac-Born-Infeld+action#Tseytlin97)$]$ has not yet been derived from any more fundamental principles

\linebreak

[Schwarz 01, Section 2](Dirac-Born-Infeld+action#Schwarz01):

> The explicit construction of such an action is a difficult problem that has been studied extensively (starting with [17]), but is not yet completely settled.

\linebreak

[Chemissany 04, p. 5 (7 of 84)](Dirac-Born-Infeld+action#Chemissany04)

> Several attempts to generalize the Born-Infeld action describing one D-brane to non-Abelian action describing a stack of them have been made. The proper (perhaps closed) form of it is however not known up to date.

### M5-Brane anomaly cancellation
 {#OpenProblemM5BraneAnomalyCancellation}

Another key ingredient of M-theory is the [[M5-brane]]. The argument for [[anomaly cancellation]] has a convoluted history (see [there](M5-brane#AnomalyCancellation)). 

[Harvey 05, p. 46](#Harvey05):

> $[$...$]$ the solution is not so clear. $[$The established procedure$]$ will not work for the M5-brane. $[$...$]$ something new is required. What this something new is, is not a priori obvious. $[$...$]$ $[$This is$]$ a daunting task. To my knowledge no serious attempts have been made
to study the problem.

> $[$The proposal of [FHMM 98](M5-brane#FreedHarveyMinasianMoore98)$]$ probably should not be viewed as a final understanding of the
problem. One would eventually hope for a microscopic formulation of M-theory which makes some of the manipulations $[$proposed in [FHMM 98](M5-brane#FreedHarveyMinasianMoore98)$]$ appear more natural.

\linebreak

### Coincident M5-branes
 {#OpenProblemCoincidentM5Branes}

Formulating the [[D=6 N=(2,0) SCFT]] expected on [[coincident brane|coincident]] [[M5-branes]] (and thus the [[gauge enhancement]] on [[coincident brane|coincident]] [[D4-branes]] under [[duality between M-theory and type IIA string theory]]) remains an open problem:


[Moore 12, p. 77](6dN20SCFT#Moore12):

> The IR dynamics of $N$ coincident M5 branes $[...]$ remains largely mysterious.


[Lambert 12, p. 49](BLG+model#Lambert12):

> The M5-brane theory remains an important open problem.



[Hu 13, p. 1](6dN20SCFT#Hu13):

> The low energy effective theory on multiple M2 branes has been well understood in recent years.  However, the low energy effective theory on multiple M5 branes is still an open problem.

[Lambert 19, Section 3.6](6dN20SCFT#Lambert19):

> 3.6  Open problems and wishes

> Let me close this discussion of M5-branes with some open problems and wish list of results:

> i) Provide a field definition/construction of the (2,0) theory $[$...$]$

> ii) Find the mathematical structures that best capture aspects of the (2,0) theory $[$...$]$

\linebreak

## Related entries

* [[large 1/N limit]]

* [[supergravity C-field]]

  * [[shifted C-field flux quantization]]

  * [[C-field tadpole cancellation]]

* [[F-theory]]

* [[topological M-theory]], [[bosonic M-theory]]

* [[M2-brane]], [[M5-brane]]

* [[supergravity Lie 3-algebra]], [[supergravity Lie 6-algebra]], [[M-theory super Lie algebra]]

* [[Horava-Witten theory]], [[M9-brane]]

* [[Diaconescu-Moore-Witten anomaly]]

* [[BFSS matrix model]], [[IKKT matrix model]], [[membrane matrix model]]

## References
 {#References}

### General

First indications for M-theory came from the [[supermembrane]] [[Green-Schwarz sigma-model]] now called the [[M2-brane]]. A comprehensive collection of early articles is in 

* {#Duff99} [[Mike Duff]], _[[The World in Eleven Dimensions]]: Supergravity, Supermembranes and M-theory_, IoP 1999 ([publisher](https://www.crcpress.com/The-World-in-Eleven-Dimensions-Supergravity-supermembranes-and-M-theory/Duff/9780750306720))

For some time though the success of [[string theory]] in 10-dimensions caused resistence to the idea of a theory of [[membranes]] in 11-dimensions, an account is in ([Duff 99](#Duff99)) and in brevity on the first pages of

* [[Mike Duff]], _M-history without the M_ ([arXiv:1501.04098](http://arxiv.org/abs/1501.04098))

The article that convinced the community of M-theory was

* {#Witten95} [[Edward Witten]], _[[String Theory Dynamics In Various Dimensions]]_, Nucl. Phys. B443:85-126 (1995) ([arXiv:hep-th/9503124](http://arxiv.org/abs/hep-th/9503124), <a href="https://doi.org/10.1016/0550-3213(95)00158-O">doi:10.1016/0550-3213(95)00158-O</a>)

A public talk announcing the conjecture that the [[non-perturbative field theory|strong-coupling limit]] of [[type IIA string theory]] is [[11-dimensional supergravity]] [[KK-compactification|KK-compactified]] on a circle is at 15:12 in

* {#Witten95Talk} [[Edward Witten]], talk at University of Southern California, 1995 ([video](https://youtu.be/1HYa4wxqe8Y))

   19:33: "Ten years ago we had the embarrassment that there were five consistent string theories plus a close cousin, which was 11-dimensional supergravity." (19:40): "I promise you that by the end of the talk we have just one big theory."

The term "M-theory" originates in 

* {#HoravaWitten95} [[Petr Hořava]], [[Edward Witten]], _Heterotic and Type I string dynamics from eleven dimensions_, Nucl. Phys. B460 (1996) 506 ([arXiv:hep-th/9510209](http://arxiv.org/abs/hep-th/9510209))

as a "non-committed" shorthand for "membrane theory"

> {#NonCommittal} As it has been proposed that the eleven-dimensional theory is a supermembrane theory but there are some reasons to doubt that interpretation, we will non-committally call it the M-theory, leaving to the future the relation of M to membranes. ([Ho&#345;ava-Witten 95, p. 2](#HoravaWitten95))

and

* {#Witten95} [[Edward Witten]], _Five-branes And M-Theory On An Orbifold_, Nucl.Phys.B463:383-397,1996 ([arXiv:hep-th/9512219](http://arxiv.org/abs/hep-th/9512219))

which coined the association

> the eleven-dimensional "M-theory" (where M stands for magic, mystery, or membrane, according to taste) ([Witten 95, p. 1](#Witten95))

that later gained much publicity:

* {#Witten98} [[Edward Witten]], _Magic, Mystery, and Matrix_, Notices of the AMS, volume 45, number 9 (1998) ([pdf](http://www.ams.org/notices/199809/witten.pdf))

The argument that the regularized [[M2-brane]] [[worldvolume]] theory is the [[BFSS matrix model]] is discussed in

* {#NicolaiHelling98} [[Hermann Nicolai]], Robert Helling, _Supermembranes and M(atrix) Theory_,  Lectures given by H. Nicolai at the Trieste Spring School on Non-Perturbative Aspects of String Theory and Supersymmetric Gauge Theories, 23 - 31 March 1998 ([arXiv:hep-th/9809103](http://arxiv.org/abs/hep-th/9809103))

* {#DasguptaNicolaiPlefka02} Arundhati Dasgupta, [[Hermann Nicolai]], [[Jan Plefka]], _An Introduction to the Quantum Supermembrane_, Grav.Cosmol.8:1,2002; Rev.Mex.Fis.49S1:1-10, 2003 ([arXiv:hep-th/0201182](http://arxiv.org/abs/hep-th/0201182))

Recollections include the last paragraph of 

* {#Witten14} [[Edward Witten]], _Adventures in Physics and Math_, [Kyoto Prize lecture](http://www.kyotoprize.org/en/laureates/commemorative_lectures/)  2014 ([pdf](http://www.kyotoprize.org/wp/wp-content/uploads/2016/02/30kB_lct_EN.pdf), [[WittenKyotoPrizeLecture.pdf:file]])



The term became fully established with surveys including

* {#Duff96} [[Michael Duff]], _M-Theory (the Theory Formerly Known as Strings)_,  Int. J. Mod. Phys. A11 (1996) 5623-5642 ([arXiv:hep-th/9608117](http://arxiv.org/abs/hep-th/9608117))

* {#Duff98} [[Michael Duff]], _The Theory Formerly Known as Strings_, Scientific American 1998 ([pdf](https://www.nikhef.nl/pub/services/biblio/bib_KR/sciam14395569.pdf), [[DuffFormerlyStrings98.pdf:file]])

* {#Duff98b} [[Michael Duff]], _A Layman's Guide to M-theory_, 	Abdus Salam Memorial Meeting, Trieste, Italy, 19 - 22 Nov 1997, pp.184-213 ([arXiv:hep-th/9805177](https://arxiv.org/abs/hep-th/9805177), [cds:355721](https://cds.cern.ch/record/355721))


Despite the magic and mystery, the relation to the original abbreviation for _membrane-theory_ was highlighted again for instance in 

* [[Paul Townsend]], _M(embrane) theory on $T^0$_, Nucl. Phys. Proc. Suppl. 68:11-16, 1998 ([arXiv:hep-th/9708034](http://arxiv.org/abs/hep-th/9708034))


More recent review includes

* {#ObersPioline98} N.A. Obers, B. Pioline, _U-duality and M-Theory_, Phys.Rept.318:113-225,1999 ([arXiv:hep-th/9809039](http://arxiv.org/abs/hep-th/9809039))

Early articles clarifying the relation to [[type II string theory]] now known as [[F-theory]] include

* {#Schwarz95} [[John Schwarz]], _The Power of M Theory_, Phys.Lett. B367 (1996) 97-103 ([arXiv:hep-th/9510086](http://arxiv.org/abs/hep-th/9510086))

* {#Johnson97} [[Clifford Johnson]], _From M-theory to F-theory, with Branes_, Nucl.Phys. B507 (1997) 227-244 ([arXiv:hep-th/9706155](http://arxiv.org/abs/hep-th/9706155))

The relation also to the [[heterotic string]] was understood in ([Horava-Witten 95](#HoravaWitten95))&#10075; see at _[[Horava-Witten theory]]_.

More technical surveys include

* [[Paul Townsend]], _Four Lectures on M-theory_,  procs. of the ICTP summer school on High Energy Physics and Cosmology, Trieste, June 1996. ([arXiv:hep-th/9612121](http://arxiv.org/abs/hep-th/9612121))

Surveys of the discussion of E-series [[Kac-Moody algebras]]/[[Kac-Moody groups]] in the context of M-theory include 

* Sophie de Buyl, _Kac-Moody Algebras in M-theory_, PhD thesis ([pdf](http://theses.ulb.ac.be/ETD-db/collection/available/ULBetd-06072006-153117/unrestricted/kmalgebrasinmth.pdf))

* [[Paul Cook]], _Connections between Kac-Moody algebras and M-theory_ PhD thesis ([arXiv:0711.3498](http://arxiv.org/abs/0711.3498))

### Relation to AdS/CFT

Relation to [[AdS/CFT]] and [[conformal bootstrap]]:

* {#ChesterPerlmutter18} Shai M. Chester, [[Eric Perlmutter]], _M-Theory Reconstruction from $(2,0)$ CFT and the Chiral Algebra Conjecture_ ([arXiv:1805.00892](https://arxiv.org/abs/1805.00892))


### Cohomological considerations

Discussion of the [[cohomology|cohomological]] charge quantization in type II ([[RR-fields]] as cocycles in [[KR-theory]]) in relation to the M-theory [[supergravity C-field]] is in

* {#FMW00} D. Diaconescu, [[Gregory Moore]], [[Edward Witten]], _$E_8$ Gauge Theory, and a Derivation of K-Theory from M-Theory_, Adv.Theor.Math.Phys.6:1031-1134,2003 ([arXiv:hep-th/0005090](http://arxiv.org/abs/hep-th/0005090)), summarised in _A Derivation of K-Theory from M-Theory_ ([arXiv:hep-th/0005091](http://arxiv.org/abs/hep-th/0005091))

See also

* {#GarciaUranga05} Inaki Garcia-Etxebarria, [[Angel Uranga]], _From F/M-theory to K-theory and back_, JHEP 0602:008,2006 ([arXiv:hep-th/0510073](https://arxiv.org/abs/hep-th/0510073))

For more on this perspective as 10d type II as a [[self-dual higher gauge theory]] in the boudnary of a kind of [[higher dimensional Chern-Simons theory|11-d Chern-Simons theory]] is in

* {#BelovMooreII} Dmitriy Belov, [[Greg Moore]], _Type II Actions from 11-Dimensional Chern-Simons Theories_ ([arXiv:hep-th/0611020](http://arxiv.org/abs/hep-th/0611020))

More complete discussion of the decomposition of the [[supergravity C-field]] as one passes from 11d to 10d is in 

* {#MathaiSati03} [[Varghese Mathai]], [[Hisham Sati]], _Some Relations between Twisted K-theory and E8 Gauge Theory_, JHEP0403:016,2004 ([arXiv:hep-th/0312033](http://arxiv.org/abs/hep-th/0312033))


### Relation to D$0$-brane mechanics

Discussion of M-theory as arising from [[type II string theory]] via the effect of [[D0-branes]] is in 

* [[Tom Banks]], W. Fischler, S.H. Shenker, [[Leonard Susskind]], _M Theory As A Matrix Model: A Conjecture_, Phys.Rev.D55:5112-5128,1997 ([arXiv:hep-th/9610043](http://arxiv.org/abs/hep-th/9610043))
 {#BanksFischlerShenkerSusskind97}

* [[Joseph Polchinski]], _M-Theory and the Light Cone_,  	Prog.Theor.Phys.Suppl.134:158-170,1999 ([arXiv:hep-th/9903165](http://arxiv.org/abs/hep-th/9903165))
 {#Polchinski99}

### More on the relation to type IIA string theory

* {#Sen97} [[Ashoke Sen]], _A Note on Enhanced Gauge Symmetries in M- and String Theory_, JHEP 9709:001,1997 ([arXiv:hep-th/9707123](http://arxiv.org/abs/hep-th/9707123))



### In terms of higher geometry

Discussion of phenomena of M-theory in [[higher geometry]] and [[generalized cohomology]] is in 

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]]_ (2010)

See also the references at _[[exceptional generalized geometry]]_. 

In fact, much of the broad structure of M-theory and its relation to the various [[string theory]] limits can be seen from the classification of exceptional [[super L-∞ algebras]] (such as the [[supergravity Lie 3-algebra]] and the [[supergravity Lie 6-algebra]]), as discussed in 

* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))
 
Review:

* [[Branislav Jurčo]], [[Christian Saemann]], [[Urs Schreiber]], [[Martin Wolf]] (eds.)

  **Proceedings of the LMS/EPSRC Durham Symposium on 

  [[Higher Structures in M‐Theory 2018]]

  Fortschritte der Physik Special Issue

  Volume 67, Issue 8-9

  [doi:10.1002/prop.201870081](https://www.onlinelibrary.wiley.com/toc/15213978/2019/67/8-9)

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:The rational higher structure of M-theory|The Rational Higher Structure of M‐theory]]**

  in: Proceedings of _[[Higher Structures in M-Theory 2018]]_

  Fortschritte der Physik, Special Issue Volume 67, Issue 8-9

  [arXiv:1903.02834](https://arxiv.org/abs/1903.02834), [doi:10.1002/prop.201910017](https://doi.org/10.1002/prop.201910017)



### Activity

* Conference series _[[M-Theory and Mathematics]]_

[[!redirects non-perturbative string theory]]