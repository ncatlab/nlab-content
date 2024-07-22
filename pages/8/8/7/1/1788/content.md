!include-command


* item

  * subitem?

    * sub sub item

      * sub sub sub item

\tableofcontents

[[geometrically connected scheme]]

### Group completed configuration spaces
 {#GroupCompletedConfigurationSpaces}

We discuss configuration-spaces of "charged objects" as models for [[group completions]] of plain [[configuration spaces of points]].

#### Charged particles and strings


Write $Conf(\mathbb{R}^n)$ for the "plain" configuration space of unlabeled and unordered points in the [[Cartesian space]] ([[Euclidean space]]) $\mathbb{R}^n$, hence the space of [[finite set|finite]] [[subsets]] of [[Cartesian space|$\mathbb{R}^n$]].
This is naturally a [[partial function|partial]] [[commutative monoid|abelian]] [[topological monoid]], where the addition of a pair of configurations is defined if they are [[disjoint]], in which case it is given by their (necessarily [[disjoint union|disjoint]]) [[union]] &lbrack;[Segal 1973, p. 215](#Segal73)&rbrack;.

Here we write
$$
  \mathbb{G}Conf(\mathbb{R}^n)
  \;\coloneqq\;
  \Omega B_{\sqcup} Conf(\mathbb{R}^n)
$$
for the [[group completion]] of the configuration space with respect to this partial operation of disjoint union. 

[Segal 1973, Thm. 1](#Segal73) says, in particular, that this group completed configuration space is [[weak homotopy equivalence|weak homotopy equivalent]] to the $n$-fold [[iterated loop space]] of the [[n-sphere|$n$-sphere]] $S^n$ (the $n$-[[Cohomotopy]] [[cocycle space]] of the [[one-point compactification]] $\mathbb{R}^n_{cpt}$ of [[Euclidean space]]):
\[
  \label{SegalTheorem1}
  \mathbb{G} Conf(\mathbb{R}^n)
  \;\simeq\;
  \Omega^n S^n
  \,,
\]

This motivates asking for more explicit descriptions of the group completed configuration space of points, itself as a configuration space, now of objects somewhat richer than plain points.

\begin{imagefromfile}
    "file_name": "OkuyamaRelations-240714.jpg",
    "float": "right",
    "width": 300,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}


Since the group completion must introduce the existence of a kind of "anti-points" much in the sense of [[antiparticles]], it is tempting to think that $\mathbb{G}Conf(\mathbb{R}^n)$ should be equivalent to the configuration space $Conf^{\pm}(\mathbb{R}^n)$ of *charged* points, where each point in a configuration carries a label in $\{\pm 1\}$ and where equal-charged points cannot coincide (they "repel") while pairs of oppositely charged points may coincide in which case they annihilate &lbrack;[McDuff 1975, p. 94](#McDuff75)&rbrack;.
However, this is *not* the case: $Conf^{\pm}(\mathbb{R}^n) \neq \mathbb{G}Conf(\mathbb{R}^n)$ &lbrack;[McDuff 1975, p. 96](#McDuff75)&rbrack;.

Still, the basic idea can be salvaged &lbrack;[Okuyama 2005](#Okuyama05)&rbrack; if only one allows charged points to be replaced by "strings" --- concretely: straight line segments of finite lenght in $\mathbb{R}^n$ each parallel to, say, the first coordinate axis --- with charged endpoints, where pair creation/annihilation of strings smoothens out the corresponding interaction of points, in the familiar way in which interactions in [[string theory]] smoothen out singular [[Feynman diagrams]] (only that here this is not postulated but emerges in order that the resulting moduli space models $\mathbb{G}Conf(\mathbb{R}^n)$):

On the right, if a filled circle is taken to indicate that the corresponding point is part of the interval, while an open circle indicates that it is not, then the curved arrows correspond to continuous paths in the configuration space of intervals, $Conf^I(\mathbb{R}^n)$, according to [Okuyama 2005, Def. 3.1-2](#Okuyama05) --- there denoted $I_n(S^0)_{\mathbb{R}}$.

With this stringy resolution of the charged points, the expected equivalence does hold &lbrack;[Okuyama 2005, Thm. 1](#Okuyama05)&rbrack;:

\[
  \label{OkuyamaTheorem}
  Conf^I(\mathbb{R}^n)
  \;\;
  \simeq
  \;\;
  \mathbb{G}Conf(\mathbb{R}^n)
  \,.
\]

#### Loop diagrams of charged string
 {#LoopsOfChargedStrings}

It follows that the [[fundamental group]] of the configuration space of charged strings in the [[plane]] $\mathbb{R}^2$ is

\[
  \label{Pi1OfOkuyamaConfigsInThePlane}
  \begin{array}{ll}
  \pi_1\big(
    Conf^I(\mathbb{R}^2)  
  \big)
  &
  \simeq\;\;
  \pi_1\big(
    \mathbb{G}Conf(\mathbb{R}^2)  
  \big)
  \;\;\simeq\;\;
  \pi_1\big(
    \Omega^2 S^2
  \big)
  \;\;\simeq\;\;
  \pi_0\big(
    \Omega(\Omega^2 S^2)
  \big)
  \;\;\simeq\;\;
  \pi_0\big(
    \Omega^3 S^2)
  \big)
  \;\;\simeq\;\;
  \pi^3(S^2)
  \\
  &\simeq\;\;
  \mathbb{Z}
  \,,
  \end{array}
\]

where the first [[isomorphism]] is by Okuyama's theorem (eq:OkuyamaTheorem), the second by Segal's theorem (eq:SegalTheorem1) and the last one is the statement that the 3d [[homotopy group of spheres|homotopy group of]] the [[2-sphere]] is the [[free group]] generated by the [[Hopf fibration]].

Hence we ask which loop diagram of charged strings corresponds to the Hopf fibration, under this sequences of isomorphisms.

{#Merger} In the following analysis we consider continuous paths *of* continuous paths of configurations of charged strings -- hence continuous maps $[0,1]^2 \to Conf^I(\mathbb{R}^2)$, the two main building blocks being the saddle

\begin{imagefromfile}
    "file_name": "ChargedStringyMerge-240716.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}

and the vanishing of the plain loop diagram.


\begin{imagefromfile}
    "file_name": "ChargedStringLoop-240715.jpg",
    "width": 560,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}

{#ChargedStringLoopWithTwist} The following based loop should have a non-trivial class in $\pi_1\big(Conf^I(\mathbb{R}^2)\big)$ and we will argue that all other based loops have classes which are integral multiples of this one:

\begin{imagefromfile}
    "file_name": "ChargedStringLoopWithTwist-240717b.jpg",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}



This example brings out the key difference between loops in McDuff's configuration space of charged points and loops in Okuyama's configuration spaces of charged strings: The former may essentially be regarded as [[oriented links]], while the latter carry the further [[structure]] of *[[framed links]]*.

As such, the above is the [[unknot]]-[[link]] but equipped with non-vanishing [[framing number]] $+1$ (say, the choice of the sign is a convention).

{#ChargedStringHopfLink} In view of this, we find that the charged stringy version of the [[Hopf link]] is equivalent, as an element of $\pi_1\big(Conf^I(\mathbb{R}^2)\big)$ and via the above saddle move, to the [[unknot]] equipped with [[framing number]] $+2$:


\begin{imagefromfile}
    "file_name": "ChargedStringHopfLink-240716.jpg",
    "width": 320,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}

In fact, by applying the same saddle move on the left, this shows that the Hopf link represents twice the class of the previous example in $\pi_1\big(Conf^I(\mathbb{R}^2)\big)$.

{#ChargedStringOppositeHopfLink} Analogously, the [[Hopf link]] with the opposite relative [[oriented link|orientation]] represents $-2$ times that unit class:

\begin{imagefromfile}
    "file_name": "ChargedStringOppositeHopfLink-240717.jpg",
    "width": 320,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}

#### Charged string loops as framed links

These examples should suffice to illustrate how [[framed links|framed]] [[oriented links|oriented]] [[link diagrams]] may be regarded as [[based loops]] in the Okuyama configuration space, and conversely how every based loop of Okuyama configurations -- possibly up to some slight continuous deformation  -- comes from a framed oriented link diagram in this way. Therefore, from now on we just draw [[framed link|framed]] [[oriented link|oriented]] [[link diagrams]], in fact we will draw just oriented link diagrams and declare the framing to be the blackboard framing (as implicit already in the above examples).

Our sign convention for crossing numbers shall be

\begin{imagefromfile}
    "file_name": "CrossingSignConvention-240722.jpg",
    "width": 310,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}

In this notation, the saddle-move looks as follows:

\begin{imagefromfile}
    "file_name": "SaddlePointMove-240718.jpg",
    "width": 420,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}

\begin{proposition}
\label{VacuumAndSaddleMoveImplyReidemeister}
The vacuum and saddle move imply the [1st Reidemeister move](framed+link#ReidemeisterMoves) for [[framed links]]:

\begin{imagefromfile}
    "file_name": "FramedReidemeisterFromSaddle-240722.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}


Therefore, regarding framed oriented link diagrams as loops in the Okuyama configuration space descends to a map 
\[
  \label{TheMap}
  FrmdOrntdLnk_{/\sim} \xrightarrow{\phantom{---}} 
  \pi_1\big(
    Conf^I(\mathbb{R}^2)
  \big)
\]
from [[isotopy classes]] of [[framed link|framed]] [[oriented link|oriented]] [[links]] to the [[fundamental group]] of the Okuyama configuration space.
\end{proposition}


\begin{proposition}
  Under the identitification (eq:Pi1OfOkuyamaConfigsInThePlane) this map (eq:TheMap)
$$
  FrmdOrntdLnkDgrms_{/\sim} \xrightarrow{\phantom{---}} 
  \pi_1\big(
    Conf^I(\mathbb{R}^2)
  \big)
  \;\simeq\;
  \mathbb{Z}
$$
is given by sending a [[framed link|framed]] [[oriented link|oriented]] [[link diagram]] to twice its total [[linking number]] including self-linking, namely to the sum of *all* the entries in its [[linking matrix]].

Moreover, this integer value may be realized as the [[framing number]] of any framed unlink which results from successively applying the saddle move to the original link.
\end{proposition}
\begin{proof}
  Since the saddle move manifestly leaves the crossing number invariant.
\end{proof}

\begin{remark}
  Besides the 1st Reidemeister move, the 2nd and 3rd also imply the following moves:

\begin{imagefromfile}
    "file_name": "CancellingLeftRightTwists-240722.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}

Jointly, these moves in particular make the [[framing number]] of a [[framed link|framed]] [[unknot]] a well-defined [[integer]], being the sum of the signs of the crossings in any representing [[link diagram]] with blackboard framing.
\end{remark}

\begin{example}
\label{HopfLink}
For the [[Hopf link]] we get $\pm 2$:

\begin{imagefromfile}
    "file_name": "HopfLinkToFramedUnknot-240722.jpg",
    "width": 520,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}


\end{example}

\begin{example}
\label{TrefoilKnot}
For the [[trefoil knot]] we get $\pm 3$:
\end{example}

\begin{imagefromfile}
    "file_name": "TrefoilKnotToFramedUnknot-240722.jpg",
    "width": 740,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}


\begin{example}
\label{FigureEightKnot}
For the [[figure eight knot]] we get $0$:
\end{example}

\begin{imagefromfile}
    "file_name": "FigureEightKnotToFramedUnknot-240722b.jpg",
    "width": 740,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 15
    }
\end{imagefromfile}


(...)


(...)


## References

* {#Segal73} [[Graeme Segal]], *Configuration-spaces and iterated loop-spaces*, Invent. Math. **21** (1973) 213-221  &lbrack;[doi:10.1007/BF01390197](https://doi.org/10.1007/BF01390197), [pdf](http://dodo.pdmi.ras.ru/~topology/books/segal.pdf), MR 0331377&rbrack;

* {#McDuff75} [[Dusa McDuff]], *Configuration spaces of positive and negative particles*, Topology **14** 1 (1975) 91-107 \[<a href="https://doi.org/10.1016/0040-9383(75)90038-5">doi:10.1016/0040-9383(75)90038-5</a>, [pdf](https://core.ac.uk/download/pdf/81183648.pdf)\]

* {#Okuyama05} [[Shingo Okuyama]]: *The space of intervals in a Euclidean space*, Algebr. Geom. Topol. **5** (2005) 1555-1572 &lbrack;[arXiv:math/0511645](https://arxiv.org/abs/math/0511645), [doi:10.2140/agt.2005.5.1555](https://doi.org/10.2140/agt.2005.5.1555)&rbrack;

