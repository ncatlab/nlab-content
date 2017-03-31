

{:principle: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


> this page is the German language version of (parts of) the page _[[topology]]_

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topologie
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


Diese Seite behandelt _Topologie_ als **Untergebiet der [[mathematics|Mathemaik]]**.  Zu "Topologie" im Sinne von **[[structured set|Struktur]]** auf einer [[set|Menge]], siehe _[[topological space|topologischer Raum]]_.

***

$\,$

$\,$

$\,$

#Inhalt#
* table of contents
{:toc}

## Einf&#252;hrung
 {#Introduction}

Im Folgenden geben wir eine kurze Einf&#252;hrung zu den zentralen Konzepten und Werkzeugen der Topologie.

* _[Stetigkeit](#Continuity)_

* _[Topologische R&#228;ume](#TopologicalSpaces)_

* _[Homeomorphismen](#Homeomorphisms)_

* _[Homotopie](#Homotopy)_

* _[Zusammenhangskomponenten](#ConnectedComponents)_

* _[Fundamentalgruppe](#FundamentalGroup)_

* _[&#220;berlagerungsr&#228;ume](#CoveringSpaces)_

### Stetigkeit
 {#Continuity}

Die zentrale Idee der Topologie ist es, [[spaces|Räume]] mit "[[continuous maps|stetigen Abbildungen]]" zwischen ihnen zu betrachten. 

Historisch wurde das Konzept der Stetigkeit zuerst in der [[analysis|Analysis]] pr&#228;zise gemacht, durch "[[epsilontic analysis|epsilontische Analysis]]" von [[open balls|offenen Bällen]], an diese wird unten in def. \ref{EpsilonDeltaDefinitionOfContinuity} erinnert. Dann realisierte man dass dies eine elegantere Formulierung durch den Begriffe der _[[open sets|offenen Mengen]]_ hat, dies ist unten Prop. \ref{ContinuityBetweenMetricSpacesInTermsOfOpenSets}. Der Begriff des  _[[topological spaces|topologischen Raumes]]_ ergibt sich wenn man von diesem allgemeinen Begriff der offenen Mengen ausgeht, dies ist Def. \ref{TopologicalSpace} unten.


Sei daher zun&#228;chst an folgende elementare Begriffe der [[analysis|Analysis]] erinnert:

+-- {: .num_defn #MetricSpace}
###### Definition

Ein _[[metric space|metrischer Raum]]_ ist

1. eine [[set|Menge]] $X$ (die "zugrunde liegende Menge");

1. eine [[function|Funktion]] $d \;\colon\; X \times X \to [0,\infty)$ (die "Distanzfunktion") aus dem  [[Cartesian product|kartesischen Produkt]] der Menge mit sich selbst in die [[nonnegative number|nicht-negativen]] [[real number|reellen Zahlen]]

so dass f&#252;r alle $x,y,z \in X$ gilt:

1. $d(x,y) = 0 \;\;\Leftrightarrow\;\; x = y$

1. (Symmetrie) $d(x,y) = d(y,x)$

1. ([[triangle inequality|Dreiecksungleichung]]) $d(x,y)+ d(y,z) \geq d(x,z)$.

=--


+-- {: .num_example}
###### Beispiel

Jeder [[normed vector space|normierte Vektorraum]] $(V, {\Vert -\Vert})$
wird ein [[metric space|metrischer Raum]] im Sinne von Definition \ref{MetricSpace} indem man setzt:

$$
  d(x,y) \coloneqq {\Vert x-y\Vert}
  \,.
$$

=--


+-- {: .num_defn #OpenBalls}
###### Definition

Sei $(X,d)$, ein [[metric space|metrischer Raum]]. Dann heisst f&#252;r jedes Element $x \in X$ und jede [[positive number|positive]] [[real number|reelle Zahl]] $\epsilon \in \mathbb{R}_+$ die Menge

$$
  B^\circ_x(\epsilon)
    \;\coloneqq\;
  \left\{
    y \in X \;\vert\; d(x,y) \lt \epsilon
  \right\}
$$

der _[[open ball|offene Ball]] von [[radius|Radius]] $\epsilon$ um $x$_.

=--


+-- {: .num_defn #EpsilonDeltaDefinitionOfContinuity}
###### Definition
**(epsilontische Definition von Stetigkeit)**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/EpsilonDeltaBalls.png" width="250">
</div>

Seien $(X,d_X)$ und $(Y,d_Y)$ zwei [[metric spaces|metrische Räume]] (def. \ref{MetricSpace}), dann heisst eine [[function|Funktion]]

$$
  f \;\colon\; X \longrightarrow Y
$$

_stetig am Punkt $x \in X$_ wenn f&#252;r jedes $\epsilon \gt 0$ ein $\delta\gt 0$ existiert, so dass

$$
  d_X(x,y) \lt \delta \;\;\Rightarrow\;\; d_Y(f(x), f(y)) \lt \epsilon
$$

oder &#228;quivalent dazu, so dass

$$
  f(\;B_x^\circ(\delta)\;) \;\subset\; B^\circ_{f(x)}(\epsilon)
$$

wobei $B^\circ$ den [[open ball|offenen Ball]] bezeichnet (Definition \ref{OpenBalls}).

Die Funktion $f$ heisst _stetig_ wenn sie an jedem Punkt $x \in X$ stetig ist.

=--

Wir formulieren diese analytische Begriffsbildung nun um, durch den einfachen aber wichtigen Begriff der [[open set|offenen Menge]]:

+-- {: .num_defn #OpenSubsetsOfAMetricSpace}
###### Definition
**(Umgebung und offene Menge)**

Sei $(X,d)$ ein [[metric space|metrischer Raum]] (def. \ref{MetricSpace}). Dann sagt man

1. Eine _[[neighbourhood|Umgebung]]_ eines Punktes $x \in X$ ist eine  [[subset|Untermenge]] $x \in U \subset X$, welche mindestens einen [[open ball|offen Ball]] $B_x^\circ(\epsilon)$ um $x$ enth&#228;lt (def. \ref{OpenBalls}).

1. Eine _[[open subset|offene Menge]]_ von $X$ ist eine [[subset|Untermenge]] $U \subset X$ die f&#252;r jedes $x \in U$ auch noch eine [[neighbourhood|Umgebung]] von $x$ enth&#228;lt.

=--

Das folgende Bild zeigt einen Punkt $x$, einige [[open balls|offene Bälle]] $B_i$ die $x$ enthalten, und zwei seiner [[neighbourhoods|Umgebungen]] $U_i$:

<img src="https://ncatlab.org/nlab/files/NeighbourhoodsAndOpenBalls.png" width="500">

> Illustration aus [Munkres 75](#Munkres75)



+-- {: .num_prop #ContinuityBetweenMetricSpacesInTermsOfOpenSets}
###### Proposition
**(Stetigkeit durch offene Mengen ausgedr&#252;ckt)**

Eine [[function|Funktion]] $f \colon X \to Y$ zwischen [[metric spaces|metrischen Räumen]] (def. \ref{MetricSpace}) ist stetig in dem  [[epsilontic analysis|epsilontischen]] Sinne von def. \ref{EpsilonDeltaDefinitionOfContinuity} genau dann wenn sie die Eigenschaft hat dass:

* ihre [[pre-images|Urbilder]] von [[open subsets|offenen Mengen]] in $Y$ (im Sinne von def. \ref{OpenSubsetsOfAMetricSpace}) sind auch offene Mengen von $X$.

=--

+-- {: principle}
**Prinzip der Stetigkeit**

$\,$ $\,$ _Urbilder offener Mengen sind offen._

=--


$\,$


### Topologische R&#228;ume
 {#TopologicalSpaces}

Daher sollten wir uns also gut das Konzept von [[open subset|offenen Mengen]] ansehen. Es stellt sich heraus dass die folgende Abschlusseigenschaft das Konzept von offenen Mengen bereits sinnvoll _charakterisiert_.

+-- {: .num_prop }
###### Proposition
**(Abschlusseigenschaft offener Mengen eines metrischen Raumes)**

Die Menge aller [[open subsets|offenen Mengen]] eines [[metric space|metrischen Raumes]] $(X,d)$ wie in def. \ref{OpenSubsetsOfAMetricSpace} hat die folgenden Eigenschaften:

1. Der [[intersection|Durchschnitt]] einer [[finite number|endlichen Zahl]] von offenen Mengen ist wieder eine offene Menge.

1. Die [[union|Vereinigung]] einer beliebigen [[set|Menge]] von offenen Mengen ist wieder eine offene Menge.

Insbesondere 

* die [[empty set|leere Menge]] ist offen (als die Vereinigung keiner Untermenge) 

und

* die ganze Menge $X$ selbst ist offen (als Durchschnitt keiner Untermenge).

=--

Dies motiviert die folgende allgemeinere Definition:

+-- {: .num_defn #TopologicalSpace}
###### Definition
**(topologische R&#228;ume)**

Gegeben eine [[set|Menge]] $X$, dann ist eine _Topologie_ $\tau$ auf $X$ eine Menge von [[subsets|Untermengen]] von $X$ -- die dann _[[open subsets|offene Mengen]]_ genannt werden -- also eine [[subset|Untermenge]] der [[power set|Potenzmenge]]

$$
  \tau \subset P(X)
$$

so dass diese unter folgenden Operatione abgeschlossen ist:

1. endliche [[intersections|Durchschnitte]];

1. beliebige [[unions|Vereinigungen]].

Ein _[[topological space|topologischer Raum]]_ ist eine Menge $X$ ausgestattet mit einer solchen [[topology|Toplogie]].

=--

Die folgende Illustration zeigt alle Topologien auf der 3-Element Menge (bis auf Permutation der Elemente):

<img src="https://ncatlab.org/nlab/files/TopologiesOn3ElementSet.png" width="400">

> Illustration aus [Munkres 75](#Munkres75)

Jetzt ist klar wie das Stetigkeitprinzip formalisiert wird.

+-- {: principle}
**Prinzip der Stetigkeit**

$\,$ $\,$ _Urbilder offener Mengen sind offen._

=--

+-- {: .num_defn #ContinuousMaps}
###### Definition
**(stetige Abbildungen)**

Eine _[[continuous function|stetige Abbildung]]_ zwischen [[topological spaces|topologsichen Räumen]]

$$
  f \colon (X, \tau_X) \to (Y, \tau_Y)
$$

ist eine [[function|Funktion]] zwischen den unterliegenden Mengen,

$$
  f \colon X \longrightarrow Y
$$

so dass [[pre-images|Urbilder]] unter $f$ von offenen Mengen in $Y$ wieder offene Mengen in $X$ sind.


=--


Diese einfach Definition von [[open subsets|offenen Untermengen]] und das einfache _Stetigkeitprinzip_
geben der Topologie ihr fundamentales und universelles Gepr&#228;ge. 
Die kombinatoischen Natur dieser Definition macht dass Topologie
enge Bez&#252;ge zur [[formal logic|formalen Logik]] hat (mehr dazu siehe _[[locale]]_).


+-- {: .num_remark}
###### Bemerkung
**(die Kategorie der topologischen R&#228;ume)**

Die  [[composition|Komposition]] von [[continuous functions|stetigen Abbildungen]] ist offensichtlich [[associativity|assoziativ]] und [[unitality|unital]].

Man sagt dass

1. [[topological spaces|topologische Räume]] sind die [[objects|Objekte]] 

1. [[continuous maps|stetige Abbildungen]] sind die [[morphisms|Morphismen]] ([[homomorphisms|Homomorphismen]])

einer _[[category|Kategorie]]_. Die _[[category of topological spaces|Kategorie der topologischen Räume]]_ (kurz: _[[Top]]_ ).

Es ist n&#252;tzliche eine Ansammlung von [[objects|Objekten]] mit [[morphisms|Morphismen]] dazwischen durch [[diagrams|Diagramme]] darzustellen, wie dieses:


<img src="https://ncatlab.org/nlab/files/AssociativityDiagram.png" width="400">

> Illustration aus [Lawvere-Schanuel 09](#category+theory#LawvereSchanuel09).

=--



Unser motivierendes Beispiel ist also folgendes

+-- {: .num_example #MetricTopology}
###### Beispiel
**(metrische Topologie)**

Sei $(X,d)$ ein [[metric space|metrischer Raum]]. Dann ist seine Menge von offenen Mengen im Sinne von def. \ref{OpenSubsetsOfAMetricSpace} eine _[[topological space|Topologie]]_ auf $X$, macht also $X$ zu einem _[[topological space|topologischen Raum]]_ im Sinne von def. \ref{TopologicalSpace}. Dies wird die _[[metric topology|metrische topologie]]_ genannt. 

Kurz gesagt, die [[open balls|offenen Bälle]] in einem metrischen Raum sind die "[[basis of a topology|Basis]]" f&#252;r die [[metric topology|metrische Topologie]].

=--


Ein wichtiger Punkt der allgemeinen Definition von "[[topological space|topologischem Raum]]" ist dass sie Konstruktionen zul&#228;sst die intuitiv auf "stetigen R&#228;umen" existieren sollten, aber dies sonst, zum Beispiel in metrischen R&#228;umen, nicht tun:

+-- {: .num_example #DiscreteTopologicalSpace}
###### Beispiel
**(diskrete topologische R&#228;ume)**

Sei $S$ eine [[set|Menge]], dann betrachtet die _[[discrete topology|diskrete Topologie]]_ auf $S$ _jede_ Untermenge von $S$ als [[open subset|offene Untermenge]].

=--

+-- {: .num_example #SubspaceTopology}
###### Beispiel
**(Unterraum Topologie)**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/OpenSubsetsOfSquareInsidePlane.png" width="200">
</div>

Sei $(X, \tau_X)$ ein [[topological space|topologischer Raum]], und sei $X_0 \hookrightarrow X$ eine [[subset|Untermenge]] der zugrunde liegenden Menge. Die zugeh&#246;rige  _[[topological subspace|Unterraumtopologie]]_ hat dann 

* $X_0$ als ihre zugunde liegende Menge, 

* die offenen Untermengen sind die Untermengen von $X_0$, welche Einschr&#228;nkungen von offenen Untermengen in $X$ sind.

(Dies wird auch die _[[initial topology|initiale Topologie]]_ der Injektionsabbildung genannt.)

Die Illustration rechts zeigt zwei offene Untermengen in dem [[square|Quadrat]], betrachtet als [[topological subspace|topologischer Unterraum]] der [[plane|Ebene]] $\mathbb{R}^2$:


> Illustration aus [Munkres 75](#Munkres75)

=--


+-- {: .num_example #QuotientTopologicalSpace}
###### Beispiel
**(topologischer Quotientenraum)**

Sei $(X,\tau_X)$ ein [[topological space|topologischer Raum]] (def. \ref{TopologicalSpace}) und sei 

$$
  R_\sim \subset X \times X
$$ 

eine [[equivalence relation|Äquivalenzrelation]] auf der zugrunde liegenden Menge. Dann hat der _[[quotient topological space|topologische Quotientenraum]]_ 

* als zugrunde liegende Menge die [[quotient set|quotientenmenge]] $X_{\sim}$, also die Menge von [[equivalence classes|Äquivalenzklassen]], 

und

* eine Untermenge $O \subset X_{\sim}$ wird als [[open subset|offene Untermenge]] betrachtet genau dann wenn ihr [[preimage|Urbild]] $\pi^{-1}(O)$ under der kanonischen [[projection map|Projektionsabbildung]]

  $$
    \pi \colon X \to X_\sim
  $$

  eine offene Untermenge von $X$ ist.

(Dies wird auch die _[[final topology|finale Topologie]]_ der Projektion $\pi$ genannt.)

=--

<img src="https://ncatlab.org/nlab/files/QuotientOfSquareIsCylinderAndTorus.png" width="660">


Die obige Illustration zeigt links das [[square|Quadrat]] (ein [[topological subspace|topologischer Unterraum]] der  [[plane|Ebene]]),
dann in der Mitte den resultierenden [[quotient topological space|topologischen Quotientenraum]] erhalten durch Identifizierung zweier gegen&#252;berliegender eiten (der _[[cylinder|Zylinder]]_), und rechts den weiteren Quotientenraum erhalten durch identifizierung auch der verbleibenden beiden Seiten (der _[[torus|Torus]]_).


> Illustration aus [Munkres 75](#Munkres75)

+-- {: .num_example #ProductTopologicalSpace}
###### Beispiel
**(topologischer Produktraum)**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/ProductTopology.png" width="300">
</div>

Seien $X$ und $Y$ zwei [[topological spaces|topologische Räume]], dann hat der [[product topological space|topologische Produktraum]] $X \times Y$ 

*  als zugrunde liegende Menge das [[Cartesian product|kartesische Produkt]] der unterliegenden Mengen $X$ and $Y$, 

und

* seine [[open sets|offenen Mengen]] sind die Untermengen $O \subset X \times Y$ des kartesischen Produktes f&#252;r die gilt dass f&#252;r alle Punkte $(x,y) \in O$ offene Mengen $x \in O_x \subset X$ und $y \in O_Y \subset Y$ existieren, so dass  $O_x \times O_y \subset O$.

> Illustration aus [Munkres 75](#Munkres75)

=--





Diese Konstruktionen von[[discrete topological spaces|disketen topologischen Räumen]], [[quotient topological spaces|topologischen Quotientenräumen]], [[topological subspaces|topologischen Unterräumen]] und von [[product topological spaces|topologischen Produkträumen]] snd einfache Beispiele f&#252;r **[[limits|Limiten]]** und **[[colimits|Kolimiten]]** von topologischen R&#228;umen. Die [[category|Kategorie]] [[Top]] von topologischen R&#228;umen hat die n&#252;tzliche Eigenschaft dass _alle_ [[limits|Limiten]] und [[colimits|Kolimiten]] (&#252;ber [[small diagrams|kleine Diagramme]]) in ihr existieren (mehr dazu siehe _[Top -- Universelle Konstruktionen](Top#UniversalConstructions)_.)



### Homeomorphismen
 {#Homeomorphisms}

Mit den [[objects|Objekten]] ([[topological spaces|topologischen Räumen]]) und den [[morphisms|Morphismen]] ([[continuous maps|stetige Abbildungen]]) der [[category|Kategorie]] [[Top]] der Topologie also definiert, erhalten wir den Begriff der "Gleichheit" in der Topologie.

Um dies pr&#228;zise zu machen sagt man dass ein [[morphism|Morphismus]] 

$$
  X \overset{f}{\to} Y
$$ 

in einer [[category|Kategorie]] ein _[[isomorphism|Isomorphismus]]_ ist wenn ein weiterer Morphismus in die andere Richtung existiert

$$
  X \overset{f^{-1}}{\longleftarrow} Y 
  \,,
$$

welcher [[inverse|invers]] zu $f$ ist in dem Sinne dass

$$
  f \circ f^{-1} = id_Y \;\;\;\;\; and \;\;\;\;\; f^{-1} \circ f = id_X
  \,.
$$



+-- {: .num_defn #Homeomorphism}
###### Definition
**(Homeomorphismen)**

Ein [[isomorphism|Isomorphismus]] in der [[category|Kategorie]] [[Top]] von [[topological spaces|topologischen Räumen]] mit [[continuous functions|stetigen Abbildungen]] zwischen ihnen heisst _[[homeomorphism|Homeomorphismus]]_. 


Das ist also eine [[continuous function|stetige Abbildung]]

$$
  f \;\colon\; X \longrightarrow Y
$$

so dass ein dazu [[inverse|inverser]] [[morphism|Morphismus]] existiert, n&#228;mich eine [[continuous function|stetige Funktion]] in der anderen Richtung

$$
  X \longleftarrow Y \;\colon\; f^{-1}
$$

so dass

$$
  f \circ f^{-1} = id_{Y} \;\;\;and\;\;\; f^{-1} \circ f = id_{X}
  \,.
$$

=--


<img src="https://ncatlab.org/nlab/files/Homeomorphism.png" width="560">

> Illustration aus [Munkres 75](#Munkres75)

+-- {: .num_example #OpenBallsHomeomorphicToRn}
###### Beispiel
**(offenes Intervall hom&#246;omorph zur reellen Geraden)**

Das offene [[interval|Intervall]] $(-1,1)$ ist [[homeomorphic|homöomorph]] zu der gesamten [[real line|reellen Geraden]]

$$
  (0,1) \underset{homeo}{\simeq} \mathbb{R}^1
  \,.
$$

Ein [[inverse|inverses]] Paar von [[continuous functions|stetigen Funktionen]] ist zum Beispiel gegeben durch

$$
  \array{
    f &\colon&  \mathbb{R}^1 &\longrightarrow& (-1,+1)
    \\
    && x &\mapsto& \frac{x}{\sqrt{1+ x^2}}
  }
$$

and

$$
  \array{
    f^{-1} &\colon&  (-1,+1) &\longrightarrow& \mathbb{R}^1
    \\
    && x &\mapsto& \frac{x}{\sqrt{1 - x^2}}
  }
  \,.
$$

Allgemein ist jeder [[open ball|offene Ball]] in $\mathbb{R}^n$ (def. \ref{OpenBalls}) [[homeomorphic|homöomorph]] zum ganzen $\mathbb{R}^n$.

=--


+-- {: .num_example #HomeomorphismBetweenTopologicalAndCombinatorialCircle}
###### Beispiel
**(Intervall an den Endpunkten verklebt ist hom&#246;omorph zum Kreis)**

Als topologische R&#228;ume ist das [[interval|Intervall]] mit identifizierten Endpunkten [[homeomorphic|homöomorph]] (def. \ref{Homeomorphism}) zum [[circle|Einheitskreis]]:

$$
  [0,1]_{/(0 \sim 1)} \;\; \underset{homeo}{\simeq} \;\; S^1
  \,.
$$

Mehr im Detail: Sei

$$
  S^1 \hookrightarrow \mathbb{R}^2
$$

der [[circle|Einheitskreis]] in der  [[plane|Ebene]] 

$$
  S^1 = \{(x,y) \in \mathbb{R}^2, x^2 + y^2 = 1\}
$$

ausgestattet mit der [[subspace topology|Unterraumtopologie]] (Beispiel \ref{SubspaceTopology}) der Ebene $\mathbb{R}^2$, welche selbst mit ihrer standard [[metric topology|metrischen Topologie]] (Beispiel \ref{MetricTopology}) ausgestattet ist.

Dar&#252;berhinaus, sei

$$
  [0,1]_{/(0 \sim 1)}
$$

der [[quotient topological space|topologische Quotientenraum]] (Beispiel \ref{QuotientTopologicalSpace}) der aus dem [[interval|Intervall]] $[0,1] \subset \mathbb{R}^1$ mit seine [[subspace topology|Unterraumtopologie]] erhalten wird durch Anwendung der [[equivalence relation|Äquivalenzrelation]], welche die beiden Endpunkte identifiziert (und sonst nichts).

Betrachte dann die Funktion

$$
  f \;\colon\; [0,1] \longrightarrow S^1
$$

gegeben durch

$$
  t \mapsto (cos(t), sin(t))
  \,.
$$

Diese hat die Eigenschaft dass $f(0) = f(1)$, so dass die also absteigt zu einer Funktion auf dem [[quotient topological space|topologischen Quotientenraum]]

$$
  \array{
    [0,1] &\overset{}{\longrightarrow}& [0,1]_{/(0 \sim 1)}
    \\
    & {}_{\mathllap{f}}\searrow & \downarrow^{\mathrlap{\tilde f}}
    \\
    && S^1
  }
  \,.
$$

Wir behaupten dann $\tilde f$ ein [[homeomorphism|Homöomorphismus]] ist (Definition \ref{Homeomorphism}).

Zun&#228;chst ist es klar dass $\tilde f$ eine [[continuous function|stetige Funktion]] ist. Das folgt direkt aus der tatsache dass $f$ eine [[continuous function|stetige Funktion]] ist und per Definition der [[quotient topology|Quotiententopologie]] (Beispiel \ref{QuotientTopologicalSpace}).

Wir m&#252;ssen also pr&#252;fen dass $\tilde f$ eine stetige inverse Funtion hat. Offensichtlich hat die Einschr&#228;nkung von $f$ selbst auf das offene Intervall $(0,1)$ ein stetiges Inverses. Es hat kein stetiges Inverses auf $[0,1)$ und auf $(0,1]$ und hat &#252;berhaupt kein Inverses auf [0,1], weil $f(0) = f(1)$. Aber die Relation $[0,1]_{/(0 \sim 1)}$ hat genau die Eigenschaft dass sie diese Probleme herausteilt.

=--

Analog gilt:

Das [[square|Quadrat]] $[0,1]^2$ mit zwei seiner Seiten identifiziert ist der [[cylinder|Zylinder]], und mit zwei weiteren Seiten identifiziert der [[torus|Torus]]:

<img src="https://ncatlab.org/nlab/files/TorusAsQuotientOfSquare.png" width="500">

Wenn die Seiten hingegen mit umgekehrter Orientierung identifiziert werden, dann ist das Resultat das _[[Möbius strip|Möbiusband]]_:

<img src="https://ncatlab.org/nlab/files/MoebiusStripAsQuotientOfSquare.png" width="400">

> Illustration aus [Lawson 03](#Lawson03)


$\,$

Wichtige Beispiele von topologischen R&#228;umen die _nicht_ hom&#246;omorph sind, enthalten die folgenden:


+-- {: .num_theorem #TopologicalInvarianceOfDimension}
###### Theorem
**([[topological invariance of dimension|topologische Invarianz der Dimension]])**

Seien $n_1, n_2 \in \mathbb{N}$ aber $n_1 \neq n_2$, dann sind die [[Cartesian space|kartesischen Räume]] $\mathbb{R}^{n_1}$ und $\mathbb{R}^{n_2}$ _nicht_ [[homeomorphic|homöomorph]].

Allgemeiner, eine [[open set|offene Menge]] in $\mathbb{R}^{n_1}$ ist nie hom&#246;omorph zu einer offenen Menge in $\mathbb{R}^{n_2}$ wenn $n_1 \neq n_2$.

=--

Der beweis des Theorems \ref{TopologicalInvarianceOfDimension} ist &#252;berraschend anspruchsvoll, angesichts wie offensichtlich die Aussage intuitiv erscheint. Man ben&#246;tigt Werkzeuge der _[[algebraic topology|algebraischen Topologie]]_ (insbesondere [[Brouwer's fixed point theorem|den Fixpunktsatz von Brouwer]]).

Wir illustrieren nun die Werkzeuge der [[algebraic topology|algebraischen Topologie]] und demonstrieren die Natur ihrer Anwednung durch den Beweis zweier sehr einfacher Spezialf&#228;lle  der [[topological invariance of dimension|topologischen Invarianz der Dimension]] (prop. \ref{TopologicalInvarianceOfDimensionFirstSimpleCase} und prop. \ref{topologicalInvarianceOfDimensionSecondSimpleCase} unten).


+-- {: .num_example }
###### Beispiel
**(Homeomorphismusklassen von Fl&#228;chen)**

Die [[2-sphere]] $S^2 = \{(x,y,z) \in \mathbb{R}^3 \vert x^2 + y^2 + z^2 = 1\}$ ist _nicht_ [[homeomorphic|homöomorph]] zu dem [[torus|Torus]] $T^2 = S^1 \times S^1$.

Allgemein ist die Homeomorphismusklasse einer [[closed manifold|geschlossenen]] [[orientable|orientierbaren]] [[surface|Fläche]] durch die Anzahl der "L&#246;cher" determiniert die die Fl&#228;che hat: ihr _[[genus of a surface|Geschlecht]]_.

=--

$\,$


### Homotopie
  {#Homotopy}

Wir haben oben gesehen dass f&#252;r $n \geq 1$  der [[open ball|offene Ball]] $B_0^\circ(1)$ in $\mathbb{R}^n$ _nicht_ [[homeomorphic|homöomorph]] zu, insbesondere,  dem Punkt $\ast = \mathbb{R}^0$ ist (Beispiel \ref{OpenBallsHomeomorphicToRn}, Theorem \ref{TopologicalInvarianceOfDimension}). Dennoch ist intuitiv der $n$-Ball eine "stetige Deformierung" des Punktes, den man erh&#228;lt wenn der Radius des $n$-Balles nach null geht.

Diese Intuition wird durch die Beobachtung pr&#228;zisiert 
dass ein [[continuous function|stetige Funktion]] existiert auf dem  [[product topological space|topologischen Produktraum]]
(Beispiel \ref{ProductTopologicalSpace}) des offenen Balles mit dem geschlossenen [[interval|Intervall]]

$$
  \eta \colon [0,1] \times B_0^\circ(1)  \longrightarrow \mathbb{R}^n
$$

gegeben durch Reskalierung:

$$
  (t,x) \mapsto t \cdot x
  \,.
$$

Dies interpoliert stetig zwischen dem offenen Ball und dem Punkt, in dem Sinne dass f&#252;r $t = 1$ die Abbildung sich auf die definierende Einbettung einschr&#228;nkt $B_0^\circ(1)$, w&#228;hrende sie f&#252;r $t = 0$ konstant ist.

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/ShrinkingBalls.png" width="200">
</div>

Wir k&#246;nnen diese Siutation zusammenfassen durch ein [[diagram|Diagramm]] von [[continuous function|stetigen Abbildungen]] der folgenden Form:

$$
  \array{
    B_0^\circ(1) \times \{0\}
    \\
    \downarrow & \searrow^{\mathrlap{x \mapsto 0}}
    \\
    [0,1] \times B_0^\circ(1)
    &\overset{(t,x) \mapsto t \cdot x}{\longrightarrow}&
    \mathbb{R}^n
    \\
    \uparrow & \nearrow_{\mathrlap{inclusion}}
    \\
    B_0^\circ(1) \times \{1\}
  }
$$

Solche "stetigen Deformationen" heissen _[[homotopies|Homotopien]]_:

+-- {: .num_defn #LeftHomotopy}
###### Definition
**(Homotopie)**

Seien $f,g\colon X \longrightarrow Y$ zwei [[continuous functions|stetige Funktionen]] zwischen [[topological spaces|topologischen Räumen]] $X,Y$, dann ist eine _[[left homotopy|(linke) Homotopie]]_

$$
  \eta \colon f \,\Rightarrow_L\, g
$$

eine [[continuous function|stetige Funktion]]

$$
  \eta \;\colon\; X \times I \longrightarrow Y
$$


aus dem [[product topological space|topologischen Produktraum]] (Beispiel \ref{ProductTopologicalSpace}) des offenen Balles mit 
dem standard Intervall, so dass dies in ein [[commuting diagram|kommutierendes Diagramm]] der folgenden Form passt:

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://www.ncatlab.org/nlab/files/AHomotopy.jpg" width="400">
</div>


$$
  \array{
     {0} \times X
     \\
     {}^{\mathllap{(id,\delta_0)}}\downarrow & \searrow^{\mathrlap{f}}
     \\
     [0,1] \times X  &\stackrel{\eta}{\longrightarrow}& Y
     \\
     {}^{\mathllap{(id,\delta_1)}}\uparrow & \nearrow_{\mathrlap{g}}
     \\
     \{1\} \times X
  }
  \,.
$$

> Illustration von J. Tauber [here](http://jtauber.com/blog/2005/07/01/path_homotopy/)

=--


+-- {: .num_defn #HomotopyEquivalence}
###### Definition
**(Homotopie&#228;quivalenz)**

Eine [[continuous function|stetige Funktion]] $f \;\colon\; X \longrightarrow Y$
heisst _[[homotopy equivalence|Homotopieäquivalenz]]_ wenn 

1. es eine stetige Abbildung in der anderen Richtung gibt,
$g \;\colon\; Y \longrightarrow X$, 

1. sowie [[left homotopies]], def. \ref{LeftHomotopy}, from the two composites to the identity:

  $$
    \eta_1 \;\colon\; f\circ g \Rightarrow_L id_Y
  $$

  and

  $$
    \eta_2 \;\colon\; g\circ f \Rightarrow_L id_X
    \,.
  $$

=--


+-- {: .num_example}
###### Beispiel
**(der offene Ball ist kontrahierbar)**

Jeder [[open ball|offene Ball]] (oder geschlossene Ball) also 
(nach Beispiel \ref{OpenBallsHomeomorphicToRn}) auch jeder [[Cartesian space|kartesische Raum]] ist [[homotopy equivalence|homotopieäquivalent]] zum Punkt

$$
  \mathbb{R}^n \underset{homotopy}{\simeq} \ast
  \,.
$$


=--

+-- {: .num_example}
###### Beispiel


Die folgenden drei [[graphs|Graphen]]

<img src="https://ncatlab.org/nlab/files/ThreeNonHomeoButHomotopyEquivGraphs.png" width="400">

(also die offensichtlichen [[topological subspaces|topologischen Unterräume]] der [[plane|Ebene]] $\mathbb{R}^2$ die diese Bilder anzeigen) sind nicht [[homeomorphic|homöomorph]]. Aber sie sind [[homotopy equivalence|homotopieäquivalent]], tats&#228;chlich sind sie alle homotopie&#228;quivalent zur [[disk|Scheibe]] aus der zwei Punkte entnommen sind, kraft der Homotopien die in folgenden Bildern angedeutet sind:

<img src="https://ncatlab.org/nlab/files/HomotopyEquivalentsToBiAnnulus.png" width="400">


> Illustration aus [Hatcher](homotopy+equivalence#Hatcher)

=--


$\,$


### Zusammenhangskomponenten
 {#ConnectedComponents}

Unter Verwendung des Begriffs der [[homotopy|Homotopie]] erh&#228;lt man die grundlegnden Werkzeuge der [[algebraic topology|algebraischen Topologie]], n&#228;mlich die Konstruktion algebraischer [[homotopy invariants|Homotopieinvarianten]] von topologischen R&#228;umen. Wir f&#252;hren hier die einfachsten dieser Werkzuge ein und illustrieren deren Anwendung.


+-- {: .num_example}
###### Bespiel

Eine [[homotopy|Homotopie]] zwischen zwei Punkten

$x,y \;\colon\; \ast \to X$

ist einfach ein stetiger [[path|Pfad]] zwischen diesen Punkten.

=--

+-- {: .num_defn #pi0}
###### Definition
**(Zusammenhangskomponenten)**

Die Megen der [[homotopy classes|Homotopieklassen]] von Punkten in einem topologischen Raum $X$ heisst die Menge der _[[connected components|Pfadzusammenhangskomponenten]]_, bezeichnet durch

$$
  \pi_0(X) \in Set
  \,.
$$

Wen $\pi_0(X) \simeq \ast$ ein einzelnes Element enth&#228;lt, dann heisst $X$ ein _[[path-connected topological space|pfad-zusammenhängender topologischer Raum]]_.

Wenn $f \colon X \to Y$ eine [[continuous map|stetige Abbildung]] zwischen [[topological spaces|topologischen Räumen ist]], dann indizuiert sie auf [[homotopy classes|Homotopieklassen]] von Punkten eine  [[function|Funktion]] zwischen den Zusammenhangskomponenten. Diese bezeichnen wir durch:

$$
  \pi_0(f) \;\colon\; \pi_0(X) \longrightarrow \pi_0(Y)
  \,.
$$

=--

Diese Konstruktion ist offenbar mit [[composition|Komposition]] vertr&#228;glich, in dem Sinne dass

$$
  \pi_0(g \circ f) = \pi_0(g) \circ \pi_0(f)
$$

und ist offensichtlich [[unitality|unital]], in dem Sinne dass

$$
  \pi_0(id_X) = id_{\pi_{0}(X)}
  \,.
$$

Man fasst diesen sachverhalt zusammen indem man sagt dass $\pi_0$  _[[functor|Funktor]]_ ist von der [[category|Kategorie]] [[Top]] von [[topological spaces|topologischen Räumen]] zu der [[category|Kategorie]] [[Set]] der [[sets|Mengen]]:

$$
  \pi_0 \;\colon\; Top \longrightarrow Set
  \,.
$$

Eine offensichtliche aber wichtige Konsequen ist dies:

+-- {: .num_prop #ConnectedComponentsDistinctImpliesHeomeClassesDistinct}
###### Proposition

Wenn die Mengen von [[connected components|Zusammenhangskomponenten]] zweier [[topological spaces|topologischer Räume]] nicht [[bijection|bijektiv]] sind, dann k&#246;nnen die beiden R&#228;ume nicht [[homeomorphism|homöomorph]] zueinander sein:

$$
  \pi_0(X) \neq \pi_0(Y)
  \;\;\;
    \Rightarrow
  \;\;\,
  X \underset{homeo}{\neq} Y
$$

=--

+-- {: .proof}
###### Beweis

Da $\pi_0$ [[functor|funktoriell]] ist, folgt sofort das es  [[isomorphisms|Isomorphismen]] auf [[isomorphisms|Isomorphismen]] schickt, also [[homeomorphisms|Homöomorphismen]] auf [[bijections|Bijektionen]]:

$$
  \begin{aligned}
     & f \circ g = id \;\;and\;\; g \circ f = id
    \\
    \Rightarrow \;\;\;\;\;\;&
    \pi_0(f \circ g) = \pi_0(id) \;\;und \;\; \pi_0(g \circ f) = \pi_0(id)
    \\
    \Leftrightarrow \;\;\;\;\;\;
    &
    \pi_0(f) \circ \pi_0(g) = id \;\;und \;\; \pi_0(g) \circ \pi_0(f) = id
  \end{aligned}
  \,.
$$

=--

Dies bedeutet dass wir dir Zuammenhangskomponenten als eine erste  "topologische Invariante" betrachten k&#246;nnen, welche uns erlaubt manche topologischen R&#228;ume zu unterscheiden. 

+-- {: principle}
**Prinzip der algebraischen Topologie**

$\,\,$ _Verwende topologische Invarianten um topologische R&#228;ume zu unterscheiden._

=--


Als Anwendungsbeispiel haben wir den folgenden Beweis eines Spezialfalls der [[topological invariance of dimension|topologischen Invarianz der Dimension]] (Theorem \ref{TopologicalInvarianceOfDimension}):


+-- {: .num_prop #TopologicalInvarianceOfDimensionFirstSimpleCase}
###### Proposition
**([[topological invariance of dimension|topologische Invarianz der Dimension]] -- erster einfacher Fall)**

Die [[Cartesian spaces|kartesische Räume]] $\mathbb{R}^1$ und $\mathbb{R}^2$ sind nicht [[homeomorphic|homöomorph]] (def. \ref{Homeomorphism}).

=--

+-- {: .proof}
###### Beweis

Wir nehmenn an e g&#228;be einen [[homeomorphism|Homöomorphismus]]

$$
  f \colon \mathbb{R}^1 \longrightarrow \mathbb{R}^2
$$

und werden einen Widerspruch erhalte. Sei also $f$ ein Homeomorphismus, dann ist offensichtlich auch seine Einschr&#228;nkung auf den [[topological subspaces|topologischen Unterraum]] (Beispiel \ref{SubspaceTopology}) den man durch Entfernen des Ursprunges $0 \in \mathbb{R}^1$ and $f(0) \in \mathbb{R}^2$ erh&#228;lt ein Homeomorphismus:

$$
  f 
    \;\colon\; 
  (\mathbb{R}^1-\{0\})
    \longrightarrow
  (\mathbb{R}^2 - \{f(0)\})
  \,.
$$

Es folgt also dass wir ein Bijektion zwischen den [[connected components|Zusammenhangskomponenten]] $\pi_0(\mathbb{R}^1 - \{0\})$ und $\pi_0(\mathbb{R}^2  - \{f(0)\})$ erhalten w&#252;rden. Aber eine solche existiert offensichtlich nicht, da letztere Menge nur ein Element enth&#228;lt, aber erstere Menge zwei Elemente enh&#228;lt (die negativen und die positiven Zahlen )

$$
  \pi_0(\mathbb{R}^1-\{0\})
    \;\neq\;
  \pi_0(\mathbb{R}^2 - \{f(0)\})  
  \,.
$$

=--

Die Lehre aus dem beweis von prop. \ref{TopologicalInvarianceOfDimensionFirstSimpleCase} ist seine Strategie:


+-- {: principle}
**Prinzip der algebraischen Topologie**

$\,\,$ _Verwende topologische Invarianten um topologische R&#228;ume zu unterscheiden._

=--


Nat&#252;rlich verwendet man in der Praxis st&#228;rkere Invarianten als nur $\pi_0$.

Die en&#228;chset topologische Invariante nach den [[connected components|Zusammenhangskomponenten]] ist die _[[fundamental group|Fundamentalgruppe]]:


### Fundamentalgruppe
 {#FundamentalGroup}


+-- {: .num_defn #FundamentalGroup}
###### Definition
**(Fundamentalgruppe)**

Sei $X$ ein [[topological space|topologischer Raum]] und sein $x \in X$ ein gegebener Punkt. Dann schreiben wir 

$$
  \pi_1(X,x)
    \;\in\; 
  Grp
$$ 

f&#252;r, zun&#228;chst, die Menge von [[homotopy classes|Homotopieklassen]] von [[paths|Pfaden]] in $X$ die bei $x$ starten und enden. Solche Pfade heissen stetige [[loops|Schleifen]] in $X$ basiert bei $x$.

1. Unter Aneinanderh&#228;ngen von Schleifen wird $\pi_1(X,x)$ zu einer [[semi-group|Semigruppe]];

1. die konstante Schleife ist [[neutral element|neutrales Element]] und macht $\pi_1(X,x)$ zu einem "[[monoid|Monoiden]]". 

1. Umkehrung von Schleifen schickt sie auf ihr [[inverse|Inverses]], und macht $\pi_1(X,x)$ zu einer [[group|Gruppe]]. 

Diese heisst die _[[fundamental group|Fundamentalgrupp]]_ $\pi_1(X,x)$ von $X$ bei $x$.

=--


Das folgende Bild deutet die vier nicht-trivialen Generatoren der [[fundamental group|Fundamentalgruppe]] der orientierten [[surface|Fläche]] vom [[genus of a surface|Geschlecht]] 2:

<img src="https://ncatlab.org/nlab/files/FundamentalGroupOfGenus2Surface.png" width="500">

> Illustration aus [Lawson 03](#Lawson03)




Auch diese Konstruktion ist [[functor|funktoriell]], nun auf der  [[category]] $Top^{\ast/}$ von [[pointed topological spaces|punktierten topologischen Räumen]]:

$$
  \pi_1 \;\colon\; Top^{\ast/} \longrightarrow Grp
  \,.
$$

As $\pi_0$, so also $\pi_1$ is a topological invariant. As before, we may use this to prove a simple case of the theorem of the [[topological invariance of dimension]]:

+-- {: .num_defn #SimplyConnected}
###### Definition

Ein topologischer Raum $X$ f&#252;r den 

1. $\pi_0(X) \simeq \ast$ ([[path-connected topological space|pfad-zusammenhängend]], def. \ref{pi0}) 

1. $\pi_1(X,x) \simeq 1$ (die Fundamentalgruppe ist [[trivial group|trivial]], def. \ref{FundamentalGroup}), 

heisst _[[simply connected topological space|einfach zusammenhängend]]_.

=--

+-- {: .num_prop #topologicalInvarianceOfDimensionSecondSimpleCase}
###### Proposition
**([[topological invariance of dimension|topologische Invarianz der Dimension]] -- zweites einfaches Beispiel)**

Es gibt  _keinen_ [[homeomorphism|Homöomorphismus]] zwischen $\mathbb{R}^2$ und $\mathbb{R}^3$.

=--

+-- {: .proof}
###### Beweis

Wir nehmen an es g&#228;be einen Homeomorphismus $f$ und werden einen Widerspruch herleiten.

Sei also $f$ ein Homeomorphismus, dann ist auch seine Einschr&#228;nkung auf das Komplement eines Punktes einer 

$$
  (\mathbb{R}^2 - \{0\})
    \longrightarrow
  (\mathbb{R}^3 - \{f(0)\})
  \,.
$$


Diese R&#228;ume sind beide zusammenh&#228;ngend, lassen sich also durch $\pi_0$ nicht unterscheiden. 

Aber ihre [[fundamental groups|Fundamentalgruppen]] $\pi_1$ sind unterschiedlich:

1. Die Fundamentalgruppe von $\mathbb{R}^{2} - \{0\}$ ist $\mathbb{Z}$ (die Windungszahl von Schleifen um den entfernten Punkt).
Wir diskutieren dies n&#228;her unten in Beispiel \ref{FundamentalGroupOfTheCircle}.

1. Die Fundamentalgruppe von  $\mathbb{R}^3 - \{f(0)\}$ its trivial: der einzelne fehlende Punkt hindert nicht daran Schleifen beliebig zusammenzuziehen.

Aber weil die Konstrution der Fundamentalgruppe[[functor|funktiell]] sit, so folgt, mit de gleichen Argument wie in dem Beweis von Prop. \ref{ConnectedComponentsDistinctImpliesHeomeClassesDistinct},
dass also $f$ kein [[isomorphism|Isomorphismus]] sein kein, also kein [[homeomorphism|Homöomorphismus]].

=--


$\,$

### &#220;berlagerungsraum
 {#CoveringSpaces}

Wir diskutieren nun eine "duale Erscheinungsform" der Fundamentalgruppe $\pi_1$, welche oft hilft sie zu berechnen.

+-- {: .num_defn #CoveringSpace}
###### Definition
**(&#220;berlagerungsraum)**

Ein _[[covering space|Überlagerungsraum]]_ &#252;ber einem [[topological space|topologischer Raum]] $X$ ist eine [[continuous map|stetige Abbildung]]

$$
  p \;\colon\; E \longrightarrow X
$$

so dass eine [[open cover|offene Überdeckung]] existiert

$$
  \underset{i}{\sqcup}U_i \longrightarrow X
$$

so dass die Einschr&#228;nkung von $E \overset{p}{\to} X$ auf jedes der  [[homeomorphic|homöomorph]] ist zu dem [[product topological space|topologischen Produktraum]] (Beispiel \ref{ProductTopologicalSpace}) von $U_i$
mit dem [[discrete topological space|diskreten topologischen Raum]] (Beispiel \ref{DiscreteTopologicalSpace}) auf einer [[set|Menge]] $F_i$:

$$
  \array{
    \underset{i}{\sqcup} U_i \times F_i &\longrightarrow&  E
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{p}}
    \\
    \underset{i}{\sqcup} U_i &\underset{}{\longrightarrow}& X
  }
  \,.
$$

F&#252;r $x \in U_i \subset X$ ein Punkt heissen die Element von $F_x  = F_i$ die _[[leaf|Blätter]]_ der &#220;berlagerung an diesem Punkt.

=--

+-- {: .num_example #kForlCovringOfCircle}
###### Beispiel
**(&#220;berdeckung des Kreises durch den Kreis)**

<div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/pFoldCoveringOfCircleB.png" width="180">
</div>

Betrachte den [[circle|Kreis]] $S^1 = \{ z \in \mathbb{C}  \;\vert\; {\vert z\vert} = 1 \}$ als den [[topological subspace|topologischen Unterraum]] von Elementen mit [[absolute value|Betrag]] 1 in der  [[complex plane|komplexen Ebene]].
F&#252;r $k \in \mathbb{N}$, betrachte die stetige Funktion

$$
  p \coloneqq (-)^k \;\colon\; S^1 \longrightarrow S^1
$$

die eine komplexe Zahl auf ihr $k$-te Potenz schickt. 

Man denk sich dies als "der Kreis windet sich $k$ mal um sich selbst".
Pr&#228;zise: f&#252;r $k \geq 1$ ist dies ein [[covering space|Überlagerungsraum]]
(Def. \ref{CoveringSpace}) mit $k$ Bl&#228;ttern an jedem Punkt.

> Illustration aus [Hatcher](homotopy+equivalence#Hatcher)


=--

+-- {: .num_example #CoveringOfCircleByRealLine}
###### Beispiel
**(&#220;berlagerung des Kreises durch die reelle Gerade)**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/UniversalCoveringOfCircle.png" width="150">
</div>

Betrachte die [[continuous function|stetige Funktion]]

$$
  \exp(2 \pi i(-)) \;\colon\; \mathbb{R}^1 \longrightarrow S^1
$$

von der [[real line|reellen Geraden]] zum [[circle|Kreis]],
welche

1. mit the Kreis betrachtet als der Einheitskreis in der [[complex plane|komplexen Ebene]] $\mathbb{C}$ durch 

   $$
     t \mapsto \exp(2\pi i t)
   $$

   gegeben ist

1. mit dem Kreis betrachtet als Einheitskreis in $\mathbb{R}^2$ durch

   $$
     t \mapsto ( cos(2\pi t), sin(2\pi t) )
   $$

   gegeben ist.

Man darf sich dies vorstellen als  "das unendliche Umwickeln des Kreises durch die reelle Achse".

Pr&#228;zise: dies ist ein [[covering space|Überlagerungsraum]] (def. \ref{CoveringSpace}) mit  [[leaves|Blattmenge]] an jedem Punkt isomorph zur Menge $\mathbb{Z}$ der [[natural numbers|ganzen Zahlen]].

=--


+-- {: .num_defn #ActionOfFundamentalGroupOnFibersOfCovering}
###### Definition
**(Wirkung der Fundamentalgruppe auf Bl&#228;tter einer &#220;berlagerung)**

Sei $E \overset{\pi}{\longrightarrow} X$ ein [[covering space|Überlagerungsraum]] (def. \ref{CoveringSpace}).

Dann gilt f&#252;r jeden Punkt $x \in X$ und jede Wahl von Element $e \in F_x$ aus der [[leaf space|Blattmenge]] &#252;ber $x$,
es existiert, bis auf  [[homotopy|Homotopie]], eine eindeutige Hebung 

* eines Pfades in $X$ der ein Element $\gamma$ der [[fundamental group|Fundamentalgruppe]] $\pi_1(X,x)$ (def. \ref{FundamentalGroup})  repr&#228;sentiert 

* zu einem stetigen Pfad in $E$ der bei $e$ beginnt. 

Dieser Pfad endet notwendigerwise and einem (anderen) Punkt 

$$
  \rho_\gama(e) \in F_x
$$

in derselben [[fiber|Faser]]. 

Diese Kontruktion gibt eine [[function|Funktion]]

$$
  \array{
    \rho &\colon& F_x \times \pi_1(X,x) &\longrightarrow& F_x
    \\
    && (e,\gamma) &\mapsto& \rho_\gamma(e)
  }
$$

aus dem [[Cartesian product|kartesischen Produk]] des [[leaf space|Blattraumes]] mit der [[fundamental group|Fundamentalgruppe]]. Diese Funtion ist kompatibel mit der [[group|Gruppen]]-Struktur auf $\pi_1(X,x)$, in dem Sinne dass die folgenden [[commuting diagram|Diagramme kommutieren]]:

$$
  \array{
    F_x \times \{const_x\} && \longrightarrow && F_x \times \pi_1(X,x)
    \\
    & {}_{\mathllap{id}}\searrow && \swarrow_{\mathrlap{\rho}}
    \\
    && F_x
  }
  \;\;\;\;\;\;
  \left(
  \array{
    \text{das neutrale Element,}
    \\
    \text{also die konstante Schleife}
    \\
    \text{wirkt trivial}
  }
  \right)
$$

and

$$
  \array{
    F_x \times \pi_1(X,x) \times \pi_1(X,x)
      &\overset{\rho \times id}{\longrightarrow}&
    F_x \times \pi_1(X,x)
    \\
    {}^{\mathllap{id \times ((-)\cdot(-))}}\downarrow && \downarrow^{\mathrlap{\rho}}
    \\
    F_x \times \pi_1(X,x)
      &\underset{\rho}{\longrightarrow}&
    F_x
  }
  \;\;\;\;\;\;
  \left(
  \array{
    \text{die Wirkung von zwei Gruppenelementen }
    \\
    \text{ist die gleiche wie}
    \\
    \text{erst beide Elemente zu verkn&#252;pfen}
    \\
    \text{und dann mit dem Produkt zu wirken}
  }
  \right)
  \,.
$$

Man sagt auch dass $\rho$ eine _[[action|Wirkung]]_ oder _[[permutation representation|Permutationsdarstellung]]_ von $\pi_1(X,x)$ auf $F_x$ ist.

For $G$ irgend eine [[group|Gruppe]], dann gibt es eine [[category|kategorie]] $G Set$ deren [[objects|Objekte]] die [[sets|Mengen]]
mit  $G$-[[action|Wirkung]] sind, und deren [[morphisms|Morphismen]] solche [[function|Funktionen]] sind die diese $G$-Wirkung respektieren. 

Die obige Konstruktion ist dann ein [[functor|Funktor]] der Form

$$
  Cov(X) \longrightarrow \pi_1(X,x) Set
  \,.
$$

=--

+-- {: .num_example }
###### Beispiel
**(drei-bl&#228;ttrige &#220;berdeckung des Kreises)**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/The3SheetedCoveringsOfTheCircle.png" width="150">
</div>

Es gibt, bis auf [[isomorphism|Isomorphismus]], drei uterschiedliche 3-bl&#228;ttrige [[covering spaces|Überlagerungen]] des [[circle|Kreises]] $S^1$.

Die von Beeispiel \ref{kForlCovringOfCircle} f&#252;r $k = 3$. Und eine andere. Und die triviale. Die zugeh&#246;rigen [[permutation actions|Permutationswirkungen]] sind in dem bild rechts angedeutet.

> graphics grabbed from [Hatcher](homotopy+equivalence#Hatcher)

=--

Wir sind jetzt bereit den Hauptsatz &#252;ber die [[fundamental group|Fundamentalgruppe]] zu nennen. 

Wir bn&#246;tigen nur noch die folgende technische Bdingung. Diese ist f&#252;r alle "sinnvollen" topologischen R&#228;ume erf&#252;llt:

+-- {: .num_defn #SemiLocallySimplyConnected}
###### Definition
**(semi-lokal einfach zusammenh&#228;ngend)**

Ein [[topological space|topologischer Raum]] $X$ heisst

1. _[[locally path-connected|lokal pfad-zusammenhängend]]_ wenn f&#252;r jeden Punkt $x \in X$ und f&#252;r jede [[neighbourhoodUmgebung]] $x \in U \subset X$ gilt dass 
eine Umgebung $x \in V \subset U$ existiert so dass $V$  [[path-connected topological space|pfad-zusammenhängend]] ist (def. \ref{pi0});

1. _[[semi-locally simply connected topological space|semi-lokal einfach zusammenhängend]]_ wenn jeder Punkt $x \in X$ eine  [[neighbourhood|Umgebung]] $x \in U \subset X$ hat so dass der induzierte Morphismus von [[fundamental groups|Fundamentalgruppen]] $\pi_1(U,x) \to \pi_1(X,x)$ trivial ist (also jedes Element auf das [[neutral element|neutrale Element]] schickt).

=--



+-- {: .num_theorem #FundamentalTheoremOfCoveringSpaces}
###### Theorem
**([[fundamental theorem of covering spaces|Fundamentalsatz der Überlagerungstheorie]])**

Sei $X$ ein [[topological space|topologischer Raum]] der [[connected topological space|pfad-zusammenhängend]] (def. \ref{pi0}),
[[locally path-connected topological space|lokal pfad-zusammenhängend]] (def. \ref{SemiLocallySimplyConnected})
und [[semi-locally simply connected topological space|semi-lokal einfach zusammenhängend]] ist (def. \ref{SemiLocallySimplyConnected}). 

Dann ist f&#252;r jedes $x \in X$ der Funktor
$$
  Fib_x \;\colon\; Cov(X) \overset{}{\longrightarrow} \pi_1(X,x) Set
  \,.
$$

von def. \ref{ActionOfFundamentalGroupOnFibersOfCovering} der die [[action|Wirkung]] der [[fundamental group|Fundamentalgruppe]] von $X$ auf die Menge der [[leaves|Blätter]] &#252;ber $x$ konstruiert
hat die folgenden Eigenschaften:

1. jede [[isomorphism class|Isomorphieklasse]] von $\pi_1(X,x)$-[[actions|Wirkungen]] ist im Bild des Funktors (man sagt: der Funktor ist _[[essentially surjective functor|essentiell surjectiv]]_);

1. f&#252;r je zwei &#220;berlagerungsr&#228;ume $E_1, E_2$ of $X$ ist die Abbildung au [[hom-sets|Morphismen-Mengen]]

   $$
     Fib_x \;\colon\; Hom_{Cov(X)}(E_1, E_2) \longrightarrow Hom( Fib_x(E_1), Fib_x(E_2) )
   $$

   eine [[bijection|Bijektion]] (man sagt der Funktor ist _[[fully faithful functor|voll true]]_ ).


Ein Funktor mit diesen Eigenschaften heisst _[[equivalence of categories|Äquivalenz von Kategorien]]_:

$$
  Cov(X) \overset{\simeq}{\longrightarrow} \pi_1(X,x) Set
  \,.
$$

=--

Dies hat einige interessante Konsequenzen...

$\,$


$\,$

Every sufficiently nice topological space $X$ as above has a covering which is [[simply connected topological space|simply connected]]
(def. \ref{SimplyConnected}). This is the covering corresponding, under the [[fundamental theorem of covering spaces]]
(theorem \ref{FundamentalTheoremOfCoveringSpaces}) to the action of $\pi_1(X)$ on itself.
This is called the _[[universal covering space]]_ $\hat X \to X$. The above theorem implies that the
[[fundamental group]] itself may be recovered as the [[automorphisms]] of the universal covering space:

$$
  \pi_1(X) \simeq Aut_{Cov_{/X}}(\hat X, \hat X)
  \,.
$$


+-- {: .num_example #FundamentalGroupOfTheCircle}
###### Example
**(computing the fundamental group of the circle)**

The covering $\exp(2\pi i(-)) \;\colon\; \mathbb{R}^1 \to S^1$ from example \ref{CoveringOfCircleByRealLine}
is [[simply connected topological space|simply connected]] (def. \ref{SimplyConnected}), hence must be the [[universal covering space]],
up to [[homeomorphism]].

It is fairly straightforward to see that the only [[homeomorphisms]] from $\mathbb{R}^1$ to itself
over $S^1$ are given by [[integer]] translations by $n \in \mathbb{N} \hookrightarrow \mathbb{R}$:

$$
  \array{
    \mathbb{R}^1
      &&
        \underoverset{\simeq}{t \mapsto t + n}{\longrightarrow}
      &&
    \mathbb{R}^1
    \\
    & {}_{\mathllap{\exp(2 \pi i(-))}}\searrow && \swarrow_{\mathrlap{\exp(2 \pi i(-))}}
    \\
    && S^1
  }
  \,.
$$

Hence

$$
  Aut_{Cov_{/S^1}}(\hat S^1, \hat S^1) \simeq \mathbb{Z}
$$

and hence the [[fundamental group]] of the [[circle]] is the additive group of [[integers]]:

$$
  \pi_1(S^1) \simeq \mathbb{Z}
  \,.
$$

=--

$\,$

***

$\,$


## Literatur

Einf&#252;hrende Lehrb&#252;cher:

* {#Munkres75} [[James Munkres]], _Topology_, Prentice Hall 1975 (2000)

* {#Lawson03} Terry Lawson, _Topology: A Geometric Approach_, Oxford University Press (2003) ([pdf](http://users.metu.edu.tr/serge/courses/422-2014/supplementary/TGeometric.pdf))

Siehe auch die Literatur unter _[[algebraic topology|algebraische Topologie]]_.

Kurzeinf&#252;hrungen:

* [[Friedhelm Waldhausen]], _Topologie_ ([pdf](https://www.math.uni-bielefeld.de/~fw/ein.pdf))

* Alex Kuronya, _Introduction to topology_, 2010 ([pdf](https://www.uni-
frankfurt.de/64271720/TopNotes_Spring10.pdf))

* Anatole Katok, Alexey Sossinsky, _Introduction to modern topology and geometry_ ([pdf](http://www.personal.psu.edu/axk29/MASS-07/Background-forMASS.pdf))

Siehe auch

* [[Topospaces]], ein Wiki mit Grundlagen zur Topologie.
