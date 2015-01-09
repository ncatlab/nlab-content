
{:formalization: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

{:bluebox: .un_remark }

> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
=--
=--

This page collects resources related to


* [[Georg Hegel]]

  _Wissenschaft der Logik_ ( _Science of Logic_)

  Volume 1, _The Objective Logic_, Part I: The Doctrine of Being; Part II: The Doctrine of Essence.

  Volume 2, _The Subjective Logic_, The Doctrine of the Notion

  1812, 1831

  ([English hyperlinked version](http://www.marxists.org/reference/archive/hegel/works/hl/),
 [German hyperlinked version](http://hegel.logik.2.abcphil.de), [German raw text version](http://www.gutenberg.org/cache/epub/6729/pg6729.html), [Wikipedia entry](http://en.wikipedia.org/wiki/Science_of_Logic))

The English translation is by A. V. Miller in 1969. More recently George di Giovanni has published a new translation, Cambridge University Press, 2010.

Note that Hegel included an abbreviated version of _The Science of Logic_ as the first part of _The Encyclopedia of the Philosophical Sciences_, followed there by _The Philosophy of Nature_ and _The Philosophy of Mind_. This first part is often referred to as the _Shorter Logic_. 

* {#EPSBOI} _Enzyklop&#228;die der philosophischen Wissenschaften im Grundrisse_ (1830) W. Bonsiepen und H.-C. Lucas (eds.) in _Gesammelte Werke_, Rheinisch-Westf&#228;lischen Akademie der Wissenschaften, and xx. Hamburg: Felix Meiner, 1992 ( Bonsiepen/Lucas 1992) ([English hyperlinked version](http://www.marxists.org/reference/archive/hegel/sl_index.htm)) 

Here the _objective logic_ is not quite _[[logic]]_ in the usual sense, but rather something like _[[logos]]_ in the old sense of [[Heraclitus]] (e.g. ([Heidegger 58](#Heidegger58), [Lambek 82](#Lambek82))) or the _[[Nous]]_ in the sense of [[Anaxagoras]] ([&#167;54](#54), [PoS pref. &#167;55](Phenomenology%20of%20Spirit#Vorrede55)) or _[[metaphysics]]_ ([&#167;85](#85)). Something closer to the usual notion of logic is what Hegel calls the "subjective logic", though of course he also talks about both being the same.


> With Hegel you're getting what seems to us today a curious package. The whole dynamic (or '[[dialectic]]') of the unfolding of the [[logos|Logik]] is prior to any actual thinking, realised in concrete humans. In fact, the world, and that part of it which is human thought, is the Idea (or Spirit) realising itself. I say 'curious', but in a way I'm hearing echoes of this in things Urs is suggesting, as though the universe worked itself out according to [[type theory]]. For Hegel one isn't to be a Kantian, where what one theorises about the universe is just how the universe is taken up by the human understanding, with the further idea that this will be limited in certain ways, e.g., no access to the thing-in-itself. For Hegel, the human mind itself is part of the universe and as such part of the unfolding of the Idea/Spirit. $[\cdots]$ It's a dizzying picture which tends either to delight or revolt people. $[$ See at _[[absolute idealism]]_ $]$ ([Corfield](http://nforum.mathforge.org/discussion/4117/the-wiki-history-of-the-universe/?Focus=34343#Comment_34343))

+-- {: bluebox #nPOVRemark}
###### nPOV

While going through Hegel's text, this page here attempts to spell out as much as seems possible the translation of the "objective logic" to a [[category theory|category-theoretic]] or [[modal type theory|modal]] [[type theory|type-theoretic]] formalization, following various suggestions by [[William Lawvere]] (an [[nPOV]]). The way this formalization dictionary works is discussed below in _[The formalization dictionary](#FormalizationDictionary)_.

=--


#Contents#
* table of contents
{:toc}



## Topics of Volume One: The objective logic

The following extracts some paragraphs from the text, with comments on how to possibly think about this in terms of [[homotopy type theory]], along the lines that [[William Lawvere]] has been suggesting over the decades. 

The paragraph numbers refer to the numbers as given in the English translation at _[Hegel-by-hypertext](http://www.marxists.org/reference/archive/hegel/index.htm)_ _[Hegel's science of logic](http://www.marxists.org/reference/archive/hegel/works/hl/)_.

Before we get to the content, here some remarks.

### Heraclitus and the Logos of Becoming
 {#Heraclitus}

Hegel wrote (according to [this](http://en.wikipedia.org/wiki/Georg_Wilhelm_Friedrich_Hegel#Heraclitus)):

"[[Heraclitus]] is the one who first declared the nature of the infinite and first grasped nature as in itself infinite, that is, its essence as process. The origin of [[philosophy]] is to be dated from Heraclitus. His is the persistent Idea that is the same in all philosophers up to the present day, as it was the Idea of Plato and Aristotle."

"... there is no proposition of Heraclitus which I have not adopted in my logic."

### Triads of Opposites and their Unity

Hegel famously invokes opposite to the extent of [[paradoxes]], as sources for new phenomena via their synthesis. The whole text is structured by triads of chapters each with triads of sections, etc. see [Inwood 83, p. 263](#Inwood1983) for a diagram.


### Formalization of Unity of Opposites
 {#OppositesAndUnity}

On p. 11 of _[Cohesive toposes and Cantor's Lauter Einsen](#LawvereLauterEinsen)_ [[William Lawvere]] proposes that these _triads_ of [[unity of opposites]] are captured by [[adjoint pairs]] of [[idempotent]] [[monads]]/[[comonads]] ("[[adjoint cylinders]]"), such as

$\flat \dashv \sharp$

[[flat modality]] $\dashv$ [[sharp modality]]

This gives unifying triples of the form

$$
  \array{
    \flat X &\longrightarrow& X &\longrightarrow& \sharp X
    \\
    \\
    opposite\;1 && unity && opposite\;2
  }
  \,.
$$

for any [[type]] $X$.


Several examples of this appear below.

Notice that indeed a fair bit of structure follows from maps of this form.

For instance for the [points-to-pieces transform](cohesive%20topos#CanonicalComparison) induced by the [[shape modality]] $\dashv$ [[flat modality]] dichotomy $&#643; \dashv \flat$,
we have, as discussed at [tangent cohesion -- Cohesive and differential refinement](#tangent+cohesive+%28?%2C1%29-topos#CohesiveAndDifferentialRefinement)

$$
  \array{
    &&  &#643;_{dR} \Omega A && \longrightarrow && \flat_{dR}\Sigma A
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{\theta_A}} && \searrow
    \\
    \flat &#643;_{dR} \Omega A  && && A && && &#643; \flat_{dR}\Sigma A
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow_{\mathrlap{&#643; \theta_A}}
    \\
    && \flat A && \longrightarrow && &#643; A
  }
  \,,
$$

### Formalization dictionary
 {#FormalizationDictionary}

[[Hegel]]'s "Science of Logic" may seem rather mysterious. Over the decades, [[William Lawvere]] had suggested, more or less explicitly, that parts of it are usefully understood as being about -- or conversely as being formalized and hence interpreted by -- aspects of [[categorical logic]]. For instance Lawvere suggested that the recurring notion of "unity and identity of opposites" is usefully thought of in terms of certain [[adjunctions]], as discussed in _[Formalization of Unity of Opposites](#OppositesAndUnity)_ and _[[Aufhebung]]_.

In view of this one may notice that modern [[foundations]] of [[constructive mathematics]] via [[type theory]] and in particular via [[homotopy type theory]] may offer more opportunities like this to give Hegel's intuitions a formalized home or incarnation in a useful way. 

The following table lists proposals for possible such identifications. The content to follow below means to provide for each keyword a commented passages in the _Science of Logic_ to support this identification and illuminate it. But of course this remains just a proposal and subject to debate. It is however noteworthy that the formalization arrived at is of genuine mathematical interest in itself.

+-- {: bluebox #Dictionary}
###### The formalization dictionary

| Hegel's logic |  [[modal type theory|modal]] [[homotopy type theory]] |  |
|-----|------|---|
| **Subjektive Logic** |    |   |
| **Begriffslogik** | **[[type theory]]/[[natural deduction]]** |  |
| Begriff, concept, notion | [[type]] | [MaL&#246;73](#MartinLoef73), [Sale 77](#Sale77), [Se94](#Sergeraert94) [LaPr14](#LadymanPresnel14) |
| Urteil | [[judgement]] | [MaL&#246;96](#MartinLoef96) |
| Schluss | [[natural deduction]] | [Ge35](#Gentzen35) |
| Grund (unvermittelt) | [[antecedent]] | [&#167;1021](#1021) |
| das Begr&#252;ndete (vermittelt) | [[succedent]]/[[consequent]] | [&#167;1021](#1021), [&#167;1035](#1035) |
| entering into existence | [[term introduction]] | [&#167;1033](#1033), [&#167;1035](#1035) |
| moment | [[modality]], [[modal operator]] |  |
| unity of opposites |  [[adjoint modality]] (moment $\dashv$ co-moment) | [[Some Thoughts on the Future of Category Theory|Law91]], [[Cohesive Toposes and Cantor's "lauter Einsen"|Law94]], [[Unity and Identity of Opposites in Calculus and Physics|Law96]] |
| unity of opposite unities of opposites | [[adjoint triple]] [[adjoint modality]] $\left(\array{moment &\dashv& comoment \\ \bot && \bot \\ comoment &\dashv& cocomoment }\right)$  |  |
| sphere | [[level of a topos|level]] | [&#167;194](#194) |
| Aufhebung | [[Aufhebung]], inclusion of adjoint modality in higher [[level of a topos|level]] | [Law89](Aufhebung#Law89b) |
| **Objektive Logik** |    |  |
| **Seinslogik** | **[[modal type theory]]** |  |
| moment of two negations, something | [[double negation modality]] $\not \not$, more generally: [[bracket type]]/[[n-truncation modality|(-1)-truncation modality]] | [&#167;210](#210) |
| [[being]], One  | [[unit type]] $\ast$ | [&#167;86](#86), [&#167;132](#132), [&#167;1663](#1663) |
| [[nothing]] | [[empty type]] $\emptyset$ | [&#167;133](#133) |
| [[becoming]] | [[adjoint modality]]  $(\emptyset \dashv \ast)$ | [&#167;134](#134), [&#167;152](#152), [&#167;176](#176), [&#167;177](#177), [&#167;180](#180), [[Some Thoughts on the Future of Category Theory|Law91]] |
| everything is an intermediate stage between nothing and being | [[points-to-pieces transform|comparison map]] via [[counit of a comonad|counit]]/[[unit of a monad|uni]]-factorization $(\emptyset \to X \to \ast)$,  | [&#167;174](#174) |
| [[Dasein]]   | [[Aufhebung]] of [[becoming]] by [[sharp modality]] $\sharp$ | [&#167;182](#182),  [&#167;183](#183), [&#167;187](#187), [&#167;191](#191), [&#167;209](#209) [&#167;222](#222) |
| moment of repulsion | [[flat modality]] $\flat$ |  |
| moment of attraction | [[cohesion]], [[shape modality]] $&#643;$ | [&#167;395](#395) |
| quality | [[adjoint modality]] (attraction $\dashv$ repulsion) = ($&#643; \dashv \flat$) |  [&#167;342](#342) |
| moment of discreteness | [[flat modality]] $\flat$ |  |
| moment of continuity | [[sharp modality]] $\sharp$ |  |
| quantity | [[adjoint modality]] (discreteness $\dashv$ continuity)  = ($\flat \dashv \sharp$) | [&#167;398](#398), [[Cohesive Toposes and Cantor's "lauter Einsen"|Law94]] |
| measure (= [[gauge]]), unity of quantity and quality | [[cohesion]] [[adjoint triple]] [[adjoint modality]] $\left(\array{ attraction &\stackrel{quality}{\dashv}& repulsion \\ \bot && \bot \\ discreteness &\stackrel{quantity}{\dashv}& continuity } \right) = \left(\array{ &#643; &\dashv& \flat \\ \bot && \bot \\ \flat &\dashv& \sharp }\right) $ | [&#167;699](#699), [&#167;708](#708), [&#167;714](#714), [&#167;725](#725) |
| vanishing of infinitesimals | [[reduction modality]] $\Re$ | [&#167;174](#174)  |
| being-for-self | [[reduction modality]] $\Re$ |  |
| being-for-one | [[infinitesimal shape modality]] $&#643;_{inf}$ |  |
| ideality | [[adjoint modality]] ($\Re \dashv &#643;_{inf}$) | [&#167;305](#305), [&#167;322](#322)   |
| reality | [[adjoint modality]] ($&#643;_{inf} \dashv \flat_{inf}$) |   |
| idea, unity of ideality and reality | [[differential cohesion]] [[adjoint triple]] [[adjoint modality]] $\left( \array{ \Re &\dashv& &#643;_{inf} \\ \bot&\stackrel{idea}{}& \bot && \\ &#643;_{inf} &\dashv&  \flat_{inf}} \right)$ | [&#167;304](#304), [&#167;324](324#), [EL&#167;214](#EL214), [&#167;1636](#1636) |
| absolute indifference  | [[adjoint modality]] ($id \dashv id$) | [&#167;803](#803), [&#167;808](#808), [&#167;812](#812) |
| **Wesenslogik** | **[[homotopy type theory]]** |   |
| Wesen, essence | the ambient [[category]]  | [&#167;803](#803), [&#167;812](#812)  |
| possibility | [possibility monad](necessity+and+possibility#InFirstOrderLogicAndTypeTheory) $\lozenge$ = [[dependent sum]] followed by [[context extension]] |  |
| necessity | [necessity comonad](necessity+and+possibility#InFirstOrderLogicAndTypeTheory) $\Box$ = [[dependent product]] followed by [[context extension]] |  |
| absolute reality, unity of [[possibility]] and [[necessity]] | [[adjoint pair]] of (co-)[[monads]] $(\lozenge \dashv \Box)$, hence [[locally cartesian closed category|local cartesian closure]] | [&#167;1160](#1160) (with [&#167;1159](#1159)), [&#167;1190](#1190), [&#167;1192](#1192) |
| essence appears as reflected in itself | [[object classifier]] = [[type of types]] = [[universe]] $Type$ | [&#167;816](#816), [&#167;834](#834), [&#167;850](#850), [&#167;1037](#1037) |
| essence as infinite return-into-self | hierarchy of universe levels $Type_1 \lt Type_2 \lt Type_3 \lt \cdots $ | [&#167;860](#860) |
| everything is identical with itself | [[term introduction]] for [[identity types]] | [&#167;863](#863), [&#167;875](#875) |
| all things are different | [[intensional identity]] | [&#167;903](#903) |

=--

Notice that the [above dictionary](#Dictionary) involves the first two stages in the tower of [[n-truncation modalities]]:

| $n$ | [[n-truncation modality]] |
|--|--|
| -2 | [[unit type]] modality |
| -1 | [[n-truncation modality|(-1)-truncation modality]], [[classical logic|classically]] [[double negation modality]] |
| $\vdots$ | $\vdots$ |

$\,$

$\,$

The following shows that system of _[[unity of opposites]]_ and _[[Aufhebung]]_ which the formalization of the Seinslogik forms. This is the adjoint pair of adjoint triples of [[cohesion]] and [[differential cohesion]] arranged such as to match, it seems, Hegel's text. Below this is discussed with pointers to the relevant passages.


+-- {: bluebox #Process}
###### Weg des Wissens,  Bewegung des Seyns 
([&#167;808](#808), [&#167;809](#809))


$$
  \array{
    {Subjektive \atop Logik}{}&&\stackrel{Begriffe}{}
    \\
    \\
    && && && \stackrel{Grund}{} && \vdots && \vdots
    \\
    && && &&&& \vee &\stackrel{Aufhebung \atop {des\;Widerspruchs}}{}& \vee 
    \\
    && &&&&\stackrel{}{}&\stackrel{falsch}{}& \emptyset &\stackrel{Widerspruch}{\dashv}& \ast & \stackrel{wahr}{}
    \\
    \\
    && && && &\stackrel{Moeglichkeit}{}& \lozenge &\stackrel{abs. Wirklichkeit}{\dashv}& \Box & \stackrel{Notwendigkeit}{}
    \\
    &&\stackrel{best.\; Reflexionen}{}&& && \stackrel{Wesen}{} &\stackrel{setzende \atop Reflexion}{} &  &\stackrel{\stackrel{\stackrel{\vdots}{Type_2}}{Type_1}}{Type_0}&  & \stackrel{auessere \atop Reflexion}{} 
    \\
    \\
    && && &&\stackrel{An\& Fuersichsein}{}&& id &\stackrel{}{\dashv}& id
    \\
    {Objektive \atop Logik}{} && && &&&& \vee &\stackrel{{Aufhebung \atop {der\;Differenzen}}}{}& \vee 
    \\
    && && &&& \stackrel{{Verschwinden\;der}\atop Infinitesimalen}{}& \Re &\stackrel{Idealitaet}{\dashv}& &#643;_{inf}
    \\
    && && \stackrel{Unendlichkeit}{} &&&& \bot &\stackrel{Idee}{}& \bot 
    \\
    && && &&\stackrel{Fuersichsein}{}&& &#643;_{inf} &\stackrel{Realitaet}{\dashv}& \flat_{inf}
    \\
    && \stackrel{Die\;Kategorien}{}&& &&&& \vee &\stackrel{{Aufhebung \atop {der\;Endlichkeit}}}{}& \vee 
    \\
    && && &&\stackrel{Ansichsein}{}&\stackrel{Attraktion}{}& &#643; &\stackrel{Qualitaet}{\dashv}& \flat & \stackrel{Repulsion}{}
    \\
    && && &&&& \bot &\stackrel{Eichmass}{}& \bot 
    \\
    && && \stackrel{Endlichkeit}{} &&\stackrel{Dasein}{}&\stackrel{Diskretion}{}& \flat &\stackrel{Quantitaet}{\dashv}& \sharp & \stackrel{Kontinuitaet}{}
    \\
    && && &&&& \vee &\stackrel{Aufhebung \atop {des\;Werdens}}{}& \vee 
    \\
    && &&&&\stackrel{reines\;Sein}{}&\stackrel{Nichts}{}& \emptyset &\stackrel{Werden}{\dashv}& \ast & \stackrel{Sein}{}
    \\
  }
$$

=--


### On the translation of the terms

The orginal German is at times maybe more evocative than the established English translations 

* "f&#252;r sich sein", which standard sources translate as "being-for-self", really means to be alone and undisturbed. One says: "Ich gehe jetzt in mein B&#252;ro, ich muss mal f&#252;r mich sein um mich zu konzentrieren." (I'll retreat to my office to be alone and undisturbed.)

* "f&#252;r eins sein" which Hegel uses, is not proper German and probably wasn't even at his time, but it is clearly meant to rhyme with "f&#252;r sich sein", and the similar phrase that does exist is "f&#252;r einander sein", which means: to be available for others.

* "Dasein", which in the standard translations appears as "determinate being" is really much more immediate "being there", "existing". "Wann sollen wir da sein?" means "When are we supposed to be there?" In more formal speech "das Dasein" means "existence" as in "Ach, das Dasein ist doch zwecklos." (Note that di Giovanni has 'existence' here.)

(...)


## **Introduction**

### Allgemeiner Begriff der Logik


> {#53} &#167;53 Die reine Wissenschaft setzt somit die Befreiung von dem Gegensatze des Bewu&#223;tseyns voraus. Sie enth&#228;lt den Gedanken, insofern er eben so sehr die Sache an sich selbst ist, oder die Sache an sich selbst, insofern sie ebenso sehr der reine Gedanke ist. Als Wissenschaft ist die Wahrheit das reine sich entwicklende Selbstbewu&#223;tseyn, und hat die Gestalt des Selbst, da&#223; das an und f&#252;r sich seyende gewu&#223;ter Begriff, der Begriff als solcher aber das an und f&#252;r sich seyende ist. Dieses objektive Denken ist denn der Inhalt der reinen Wissenschaft. Sie ist daher so wenig formell, sie entbehrt so wenig der Materie zu einer wirklichen und wahren Erkenntni&#223;, da&#223; ihr Inhalt vielmehr allein das absolute Wahre, oder wenn man sich noch des Worts Materie bedienen wollte, die wahrhafte Materie ist,&#8212;eine Materie aber, der die Form nicht ein &#196;u&#223;erliches ist, da diese Materie vielmehr der reine Gedanke, somit die absolute Form selbst ist. Die Logik ist sonach als das System der reinen Vernunft, als das Reich des reinen Gedankens zu fassen. Dieses Reich ist die Wahrheit, wie sie ohne H&#252;lle an und f&#252;r sich selbst ist. Man kann sich deswegen ausdr&#252;cken, da&#223; dieser Inhalt die Darstellung Gottes ist, wie er in seinem ewigen Wesen vor der Erschaffung der Natur und des endlichen Geistes ist.

> &#167;53 Accordingly, logic is to be understood as the system of pure reason, as the realm of pure thought. This realm is truth as it is without veil and in its own absolute nature. It can therefore be said that this content is the exposition of God as he is in his eternal essence before the creation of nature and a finite mind.

> {#54} &#167;54 Anaxagoras wird als derjenige gepriesen, der zuerst den Gedanken ausgesprochen habe, da&#223; der Nus, der Gedanke, das Princip der Welt, da&#223; das Wesen der Welt als der Gedanke bestimmt ist. Er hat damit den Grund zu einer Intellektualansicht des Universums gelegt, deren reine Gestalt die Logik seyn mu&#223;. Es ist in ihr nicht um ein Denken &#252;ber etwas, das f&#252;r sich au&#223;er dem Denken zu Grunde l&#228;ge, zu thun, um Formen, welche blo&#223;e Merkmale der Wahrheit abgeben sollten; sondern die nothwendigen Formen und eigenen Bestimmungen des Denkens sind der Inhalt und die h&#246;chste Wahrheit selbst.

> &#167;54 Anaxagoras is praised as the man who first declared that Nous, thought, is the principle of the world, that the essence of the world is to be defined as thought. In so doing he laid the foundation for an intellectual view of the universe, the pure form of which must be logic. What we are dealing with in logic is not a thinking about something which exists independently as a base for our thinking and apart from it, nor forms which are supposed to provide mere signs or distinguishing marks of truth; on the contrary, the necessary forms and self-consciousness of thought are the content and the ultimate truth itself.


### Allgemeine Einteilung der Logik

> {#85} &#167;85 Die objektive Logik tritt damit vielmehr an die Stelle der vormaligen Metaphysik, als welche das wissenschaftliche Geb&#228;ude &#252;ber die Welt war, das nur durch Gedanken aufgef&#252;hrt seyn sollte.&#8212;Wenn wir auf die letzte Gestalt der Ausbildung dieser Wissenschaft R&#252;cksicht nehmen, so ist erstens unmittelbar die Ontologie, an deren Stelle die objektive Logik tritt,&#8212;der Theil jener Metaphysik, der die Natur des Ens &#252;berhaupt erforschen sollte;&#8212;das Ens begreift sowohl Seyn als Wesen in sich, f&#252;r welchen Unterschied unsere Sprache gl&#252;cklicherweise den verschiedenen Ausdruck gerettet hat.&#8212;Alsdann aber begreift die objektive Logik auch die &#252;brige Metaphysik insofern in sich, als diese mit den reinen Denkformen die besondern, zun&#228;chst aus der Vorstellung genommenen Substrate, die Seele, die Welt, Gott, zu fassen suchte, und die Bestimmungen des Denkens das Wesentliche der Betrachtungsweise ausmachten. 



> &#167;85 The objective logic, then, takes the place rather of the former metaphysics which was intended to be the scientific construction of the world in terms of thoughts alone. If we have regard to the final shape of this science, then it is first and immediately ontology whose place is taken by objective logic &#8212; that part of this metaphysics which was supposed to investigate the nature of ens in general; ens comprises both being and essence, a distinction for which the German language has fortunately preserved different terms. But further, objective logic also comprises the rest of metaphysics in so far as this attempted to comprehend with the forms of pure thought particular substrata taken primarily from figurate conception, namely the soul, the world and God; and the determinations of thought constituted what was essential in the mode of consideration. 

## **Book one** Die Lehre vom Sein / The Doctrine of Being


### $\;\;$ Womit muss der Anfang der Wissenschaft gemacht werden?


> {#121} &#167;121 Was somit &#252;ber das Seyn ausgesprochen oder enthalten seyn soll, in den reicheren Formen des Vorstellens von Absolutem oder Gott, die&#223; ist im Anfange nur leeres Wort, und nur Seyn; die&#223; Einfache, das sonst keine weitere Bedeutung hat, die&#223; Leere ist also schlechthin der Anfang der Philosophie.

> &#167;121 Consequently, whatever is intended to be expressed or implied beyond being, in the richer forms of representing the absolute or God, this is in the beginning only an empty word and only being; this simple determination which has no other meaning of any kind, this emptiness, is therefore simply as such the beginning of philosophy.

> &#167;122 Diese Einsicht ist selbst so einfach, da&#223; dieser Anfang als solcher, keiner Vorbereitung noch weiteren Einleitung bedarf; und diese Vorl&#228;ufigkeit von Raisonnement &#252;ber ihn konnte nicht die Absicht haben, ihn herbeizuf&#252;hren, als vielmehr alle Vorl&#228;ufigkeit zu entfernen.

> &#167;122 This insight is itself so simple that this beginning as such requires no preparation or further introduction; and, indeed, these preliminary, external reflections about it were not so much intended to lead up to it as rather to eliminate all preliminaries.



### $\;\;$ Allgemeine Einteilung des Seins


### First section: Determinateness (Quality)

#### First chapter

From  the [shorter Logic](#EPSBOI):

> EL&#167;86 Pure [[being]] constitutes the beginning, because it is pure thought as well as the undetermined, simple immediate, and the first beginning cannot be anything mediated and further determined.

> EL&#167;87 Now this pure being is a pure abstraction and thus the absolutely negative which, when likewise taken immediately, is nothing.

> {EL#88} EL&#167;88 Conversely, nothing, as this immediate, self-same category, is likewise the same as being. The truth of being as well as of nothing is therefore the unity of both; this unity is [[becoming]].


##### A. Sein / Being
 {#OnBeingAndBecoming}

> {#132} &#167;132 Being, pure being, [...] it has no diversity within itself nor any with a reference outwards.


This is the _[[unit type]]_ $\ast$. See also [&#167;1663](#1663).


Indeed, later this is called "Das Eins"  which is maybe indeed better translated as "The Unit" instead of as "The One" as commonly done.


##### B. Nichts / Nothing

> &#167;133 Nothing, pure nothing: it is simply equality with itself, complete emptiness,

The [[empty type]] $\emptyset$.


##### C. Werden Becoming
 {#Becoming}


> {#134} &#167;134 Pure Being and pure nothing are, therefore, the same. What is the truth is neither being nor nothing, but that being &#8212; does not pass over but has passed over &#8212; into nothing, and nothing into being. But it is equally true that they are not undistinguished from each other, that, on the contrary, they are not the same, that they are absolutely distinct, and yet that they are unseparated and inseparable and that each immediately vanishes in its opposite. Their truth is therefore, this movement of the immediate vanishing of the one into the other: becoming, a movement in which both are distinguished, but by a difference which has equally immediately resolved itself.

According to the formalization of such [[unity of opposites]] as
[above](#OppositesAndUnity) we identify this [[becoming]] (following [Lawvere 91]({#LawvereComo})) as the universal factorization

$$
  \array{
    \emptyset &\longrightarrow& X &\longrightarrow& \ast 
    \\
    \\
    nothing && becoming && being
  }
$$

of the factorization of the unique [[function]] from the [[empty type]] to the [[unit type]] through any other [[type]] $X$.


Indeed, later in [&#167;174](#174) it says:

> there is nothing which is not an intermediate state between being and nothing.

Also, [below](#SomethingAndAnOther) it says

> {#222} &#167;222 Being and nothing in their unity, which is determinate being



###### 1. Unity of Being and Nothing

###### $\;\;$ Remark 1 The opposition  of being and nothing in ordinary thinking

###### $\;\;$ Remark 2: Defectiveness of the Expression "Unity, Identity of Being and Nothing"

> {#152} &#167;152  But the third in which being and nothing subsist must also present itself here, and it has done so; it is becoming. In this being and nothing are distinct moments; becoming only is, in so far as they are distinguished.

In view of the above it seems that "moment" is well translated with _[[modality]]_.

###### $\;\;$ Remark 3 The isolating of these abstractions

###### $\;\;$ Remark 4 Incomprehensibility of the beginning

> &#167;171 It is impossible for anything to begin, either in so far as it is, or in so far as it is not; for in so far as it is, it is not just beginning, and in so far as it is not, then also it does not begin. If the world, or anything, is supposed to have begun, then it must have begun in nothing, but in nothing &#8212; or nothing &#8212; is no beginning; for a beginning includes within itself a being, but nothing does not contain any being. Nothing is only nothing. In a ground, a cause, and so on, if nothing is so determined, there is contained an affirmation, a being. For the same reason, too, something cannot cease to be; for then being would have to contain nothing, but being is only being, not the contrary of itself.

> {#174} &#167;174 Das Angef&#252;hrte ist auch dieselbe Dialektik, die der Verstand gegen den Begriff braucht, den die h&#246;here Analysis von den unendlich-kleinen Gr&#246;&#223;en giebt. Von diesem Begriffe wird weiter unten ausf&#252;hrlicher gehandelt.&#8212;Diese Gr&#246;&#223;en sind als solche, bestimmt worden, die in ihrem Verschwinden sind, nicht vor ihrem Verschwinden, denn als dann sind sie endliche Gr&#246;&#223;en;&#8212;nicht nach ihrem Verschwinden, denn alsdann sind sie nichts. Gegen diesen reinen Begriff ist eingewendet und immer wiederholt worden, da&#223; solche Gr&#246;&#223;en entweder Etwas seyen, oder Nichts; da&#223; es keinen Mittelzustand (Zustand ist hier ein unpassender, barbarischer Ausdruck) zwischen Seyn und Nichtseyn gebe.&#8212;Es ist hierbei gleichfalls die absolute Trennung des Seyns und Nichts angenommen. Dagegen ist aber gezeigt worden, da&#223; Seyn und Nichts in der That dasselbe sind, oder um in jener Sprache zu sprechen, da&#223; es gar nichts giebt, das nicht ein Mittelzustand zwischen Seyn und Nichts ist. Die Mathematik hat ihre gl&#228;nzendsten Erfolge der Annahme jener Bestimmung, welcher der Verstand widerspricht, zu danken.

> {#174} &#167;174 The foregoing dialectic is the same, too, as that which understanding employs the notion of infinitesimal magnitudes, given by higher analysis. A more detailed treatment of this notion will be given later. These magnitudes have been defined as such that they are in their vanishing, not before their vanishing, for then they are finite magnitudes, or after their vanishing, for then they are nothing. 

Mathematically, the vanishing of [[infinitesimal objects]] is exactly what is expressed by the [[reduction modality]] $\Re$.

> &#167;174 there is nothing which is not an intermediate state between being and nothing.

The universal factorization for [[unity of opposites]] of the [[empty type]] $\dashv$ [[unit type]] [[adjoint modality]]

$$
  \array{
    \emptyset &\longrightarrow& X &\longrightarrow& \ast 
    \\
    \\
    nothing && becoming && being
  }
$$

of the factorization of the unique [[function]] from the [[empty type]] to the [[unit type]] through any other [[type]] $X$.



###### 2. Momente des Werdens / Moments of Becoming

> {#176} &#167;176 Das Werden, Entstehen und Vergehen, ist die Ungetrenntheit des Seyns und Nichts; nicht die Einheit, welche vom Seyn und Nichts abstrahirt; sondern als Einheit des Seyns und Nichts ist es diese bestimmte Einheit, oder in welcher sowohl Seyn als Nichts ist. Aber indem Seyn und Nichts, jedes ungetrennt von seinem Anderen ist, ist es nicht. Sie sind also in dieser Einheit, aber als verschwindende, nur als Aufgehobene. Sie sinken von ihrer zun&#228;chst vorgestellten Selbstst&#228;ndigkeit zu Momenten herab, noch unterschiedenen, aber zugleich aufgehobenen.

> {#176} &#167;176 Becoming is the unseparatedness of being and nothing, not the unity which abstracts from being and nothing; but as the unity of being and nothing it is this determinate unity in which there is both being and nothing. But in so far as being and nothing, each unseparated from its other, is, each is not. They are therefore in this unity but only as vanishing, sublated moments. They sink from their initially imagined self-subsistence to the status of moments, which are still distinct but at the same time are sublated.

> {#177} &#167;177 Nach dieser ihrer Unterschiedenheit sie aufgefa&#223;t, ist jedes in derselben als Einheit mit dem Anderen. Das Werden enth&#228;lt also Seyn und Nichts als zwei solche Einheiten, deren jede selbst Einheit des Seyns und Nichts ist; die eine das Seyn als unmittelbar und als Beziehung auf das Nichts; die andere das Nichts als unmittelbar und als Beziehung auf das Seyn; die Bestimmungen sind in ungleichem Werthe in diesen Einheiten.

> {#177} &#167;177 Grasped as thus distinguished, each moment is in this distinguishedness as a unity with the other. Becoming therefore contains being and nothing as two such unities, each of which is itself a unity of being and nothing; the one is being as immediate and as relation to nothing, and the other is nothing as immediate and as relation to being; the determinations are of unequal values in these unities.


An archetypical description of the [[unity of opposites]]. Here:

[[becoming]]/Werden : [[nothing]] $\dashv$ [[being]] 

$\;\;\;$ [[empty type]] $\dashv$ [[unit type]]

$\;\;\;$ $\emptyset \dashv \ast$

This is also the interpretation in ([LawvereComo, p. 11](#LawvereComo)).
$$
  \emptyset \longrightarrow X \longrightarrow \ast
$$



> {#178} &#167;178 Das Werden ist auf diese Weise in gedoppelter Bestimmung; in der einen ist das Nichts als unmittelbar, d. i. sie ist anfangend vom Nichts, das sich auf das Seyn bezieht, das hei&#223;t, in dasselbe &#252;bergeht, in der anderen ist das Seyn als unmittelbar d. i. sie ist anfangend vom Seyn, das in das Nichts &#252;bergeht,&#8212;Entstehen und Vergehen.

> {#178} &#167;178 Becoming is in this way in a double determination. In one of them, nothing is immediate, that is, the determination starts from nothing which relates itself to being, or in other words changes into it; in the other, being is immediate, that is, the determination starts from being which changes into nothing: the former is coming-to-be and the latter is ceasing-to-be.
 
$\;\;$ [[nothing]] $\dashv$ [[being]]  $\;\colon\;$ [[ceasing]]





###### 3. Sublating of Becoming


> &#167;180 The resultant equilibrium of coming-to-be and ceasing-to-be is in the first place becoming itself. But this equally settles into a stable unity. Being and nothing are in this unity only as vanishing moments; yet becoming as such is only through their distinguishedness. Their vanishing, therefore, is the vanishing of becoming or the vanishing of the vanishing itself. Becoming is an unstable unrest which settles into a stable result.

> &#167;181 This could also be expressed thus: becoming is the vanishing of being in nothing and of nothing in being and the vanishing of being and nothing generally; but at the same time it rests on the distinction between them. It is therefore inherently self-contradictory, because the determinations it unites within itself are opposed to each other; but such a union destroys itself.


> &#167;182 This result is the vanishedness of becoming, but it is not nothing; as such it would only be a relapse into one of the already sublated determinations, not the resultant of nothing and being. It is the unity of being and nothing which has settled into a stable oneness. But this stable oneness is being, yet no longer as a determination on its own but as a determination of the whole.

> &#167;183 Becoming, as this transition into the unity of being and nothing, a unity which is in the form of being or has the form of the onesided immediate unity of these moments, is determinate being.

| |  | [[Dasein]] | |  |
|--|--|--|--|--|
| [[Werden]] : | [[Nichts]] | $\;\;\;\dashv$ | [[Sein]] | : [[Vergehen]] |

$\,$

| |  | [[Dasein]] | |  |
|--|--|--|--|--|
| [[becoming]] : | [[nothing]] | $\;\;\;\dashv$ | [[being]] | : [[ceasing]] |



> &#167;187 The more precise meaning and expression which being and nothing receive, now that they are moments, is to be ascertained from the consideration of determinate being as the unity in which they are preserved. Being is being, and nothing is nothing, only in their contradistinction from each other; but in their truth, in their unity, they have vanished as these determinations and are now something else. Being and nothing are the same; but just because they are the same they are no longer being and nothing, but now have a different significance. In becoming they were coming-to-be and ceasing-to-be; in determinate being, a differently determined unity, they are again differently determined moments. This unity now remains their base from which they do not again emerge in the abstract significance of being and nothing.

moment $\leftrightarrow$ [[modality]]

Notice that all this has a striking resemblance to the following lines from the [[Tao Te Ching]] (English translation following [[Xiao-Gang Wen]] [here](http://physics.stackexchange.com/a/94612/5603)):

> The nameless nonbeing is the origin of universe;

> The named being is the mother of all observed things.

> Within nonbeing, we enjoy the mystery of the universe.

> Among being, we observe the richness of the world.

> Nonbeing and being are two aspects of the same mystery.

> From nonbeing to being and from being to nonbeing is the gateway to all understanding.

#### Second chapter. Dasein / Determinate Being 

##### A. Dasein als solches / Determinate being as such
 {#ExistenceAsSuch}

> {#188} &#167;188 Daseyn ist bestimmtes Seyn; seine Bestimmtheit ist seyende Bestimmtheit, Qualit&#228;t.

>  &#167;188 In considering determinate being the emphasis falls on its determinate character; the determinateness is in the form of being, and as such it is quality. Through its quality, something is determined as opposed to an other, as alterable and finite; and as negatively determined not only against an other but also in its own self. This its negation as at first opposed to the finite something is the infinite; the abstract opposition in which these determinations appear resolves itself into the infinity which is free from the opposition, into being-for-self.

The first sentence here is made up by the translator, in the original it says:

> Daseyn ist bestimmtes Seyn;

Di Giovanni has

> Existence is _determinate_ being;

In any case, by the discussion at _[Becoming](#Becoming)_ we have that "being" is a moment of the adjunction $(\emptyset \dashv \ast)$ and the discussion at _[Relation between repulsion and attraction](#RelationBetweenRepulsionAndAttraction)_ we have that "quality" is the adjunction $(&#643; \dashv \flat)$. Therefore it seems that

* types have "being" in the presence of $(\emptyset \dashv \ast)$

  * types moreover have "existence"/Dasein in the further presence of $(&#643; \dashv \flat)$.

For more on this see at _[Remark on reality as opposite to ideality](#RemarkOnRealityAsOppositeToDuality)_.

###### a. Dasein &#252;berhaupt / Determinant being in general
 {#DaseinUberhaupt}

> {#191} &#167; 191 From becoming there issues determinate being, which is the simple oneness of being and nothing. Because of this oneness it has the form of immediacy. Its mediation, becoming, lies behind it; it has sublated itself and determinate being appears

Above we saw that _[[becoming]]_ is formalized by the universal [[unity of opposites]] of [[nothing]] $\dashv$ [[being]], i.e. $\emptyset \dashv \ast$, exhibiting any [[type]] $X$ as intermediate (via $\emptyset$-[[unit of a monad|unit]] and $\ast$-[[counit of a comonad]])

$$
  \emptyset \longrightarrow X \longrightarrow \ast
  \,.
$$

Now by [&#167; 191](#191) [[determinate being]] is the [[sublation]] of this [[unity of opposites]]. By the discussion at _[Aufhebung -- Examples -- Aufhebung of Becoming](Aufhebung#AufhebungOfBecoming)_ this is given by the [[level of a topos|level]] of the  [[flat modality]] $\dashv$ [[sharp modality]]-opposition $(\flat \dashv \sharp)$, [[Dasein]]:

$$
  \array{
     \flat \; &\dashv& \;\;\sharp
     \\
     \vee \; &\nearrow_{\mathrlap{Dasein}}& \;\;\vee
     \\
     \emptyset \; &\dashv& \;\;\ast
  }
  \,.
$$

> {#194} &#167; 194 Determinate being corresponds to being in the previous sphere

Here "sphere" is [[level of a topos|level]].

So $\sharp$ is the version of $\ast$ ([[being]]) in the next level, which indeed it is by the above.

###### b. Qualit&#228;t / Quality

> &#167;196 Determinateness thus isolated by itself in the form of being is quality 


###### c. Etwas / Something
 {#Etwas}

> {#208} &#167;208 In determinate being its determinateness has been distinguished as quality; in quality as determinately present, there is distinction &#8212; of reality and negation. Now although these distinctions are present in determinate being, they are no less equally void and sublated. Reality itself contains negation, is determinate being, not indeterminate, abstract being. Similarly, negation is determinate being, not the supposedly abstract nothing but posited here as it is in itself, as affirmatively present [als seiend], belonging to the sphere of determinate being. 

  Thus quality is completely unseparated from determinate being, which is simply determinate, qualitative being.


[[Dasein]], quality, [[type]], something


> {#209} &#167;209 This sublating of the distinction is more than a mere taking back and external omission of it again, or than a simple return to the simple beginning, to determinate being as such. The distinction cannot be omitted, for it is. What is, therefore, in fact present is determinate being in general, distinction in it, and sublation of this distinction; determinate being, not as devoid of distinction as at first, but as again equal to itself through sublation of the distinction, the simple oneness of determinate being resulting from this sublation. This sublatedness of the distinction is determinate being's own determinateness; it is thus being-within-self: determinate being is a determinate being, a something.

> {#209} &#167;209 Die&#223; Aufgehobenseyn des Unterschieds ist die eigne Bestimmtheit des Daseyns; so ist es Insichseyn; das Daseyn ist Daseyendes, Etwas.

> {#210} &#167;210 Something is the first negation of negation, as simple self-relation in the form of being.

> {#211} &#167;211 Something is the negation of the negation in the form of being;

> {#212} &#167;212 This mediation with itself which something is in itself, taken only as negation of the negation, has no concrete determinations for its sides; it thus collapses into the simple oneness which is being.


Here "double negation" is plausibly matched with the [[double negation modality]].

Concerning "something": if $X$ is a [[type]], then by [[propositions-as-types]] there is _something_ of this type if the type is [[inhabited]]. But [[classical logic|classically]] this is expressed by by its [[double negation modality]]. Hence: there is something of some quality/type if that is a double-negation [[modal type]].



##### B. Die Endlichkeit / Finitude.

###### a. Etwas und ein Anderes. / Something and an Other
 {#SomethingAndAnOther}

> &#167;221  Being-for-other and being-in-itself constitute the two moments of the something.

something : Being-for-other $\dashv$ being-in-itself

> &#167;222 Being and nothing in their unity, which is determinate being

Notice that [above](#Becoming) this [[unity of opposites|unity]] is called _[[becoming]]_.

> Die&#223; f&#252;hrt zu einer weitern Bestimmung. Ansichseyn und Seyn-f&#252;r-Anderes sind zun&#228;chst verschieden; aber da&#223; Etwas dasselbe, was es an sich ist, auch an ihm hat, und umgekehrt, was es als Seyn-f&#252;r-Anderes ist, auch an sich ist,&#8212;die&#223; ist die Identit&#228;t des Ansichseyns und Seyns-f&#252;r-Anderes, nach der Bestimmung, da&#223; das Etwas selbst ein und dasselbe beider Momente ist, sie also ungetrennt in ihm sind.&#8212;Es ergiebt sich formell diese Identit&#228;t schon in der Sph&#228;re des Daseyns, aber ausdr&#252;cklicher in der Betrachtung des Wesens und dann des Verh&#228;ltnisses der Innerlichkeit und &#196;u&#223;erlichkeit, und am bestimmtesten in der Betrachtung der Idee, als der Einheit des Begriffs und der Wirklichkeit.



##### C. Die Unendlichkeit


###### a. Das Unendliche &#220;berhaupt

###### b. Wechselwirkung des Endlichen und Unendlichen

###### c. Die affirmative Unendlichkeit



> {#303} &#167;303 Das Endliche ist nicht das Reale, sondern das Unendliche.

> It is not the finite which is the real, but the infinite

> {#304} &#167;304 In Beziehung auf Realit&#228;t und Idealit&#228;t wird aber der Gegensatz des Endlichen und Unendlichen so gefa&#223;t, da&#223; das Endliche f&#252;r das Reale gilt, das Unendliche aber f&#252;r das Ideelle gilt; wie auch weiterhin der Begriff als ein Ideelles und zwar als ein nur Ideelles, das Daseyn &#252;berhaupt dagegen als das Reale betrachtet wird.

> With reference to reality and ideality, however, the opposition of finite and infinite is grasped in such a manner that the finite ranks as the real but the infinite as the 'ideal' [das Ideelle]; in the same way that further on the Notion, too, is regarded as an 'ideal', that is, as a mere 'ideal', in contrast to determinate being as such which is regarded as the real.

Notice here from _[Der quantitative unendliche Progress](#DerQuantitativeUnendlicheProgress)_ that "infinite" refers much to the _infinite progression_ that in mathematics is referred to as _[[sequences]]_ and _[[series]]_, and that what "ideal" ( _ideell_ ) about them is that they need not converge to any finite value, but be regarded as sequences--- such as [[formal power series]]. 
Hence if we take the "infinite" and the "infinitesimal" to go together -- as also in [&#167;502](#502) -- then [&#167;304](#304) gives that  "the [[infinitesimal]] ranks as the ideal", whereas "the [[reduced object|reduced]] ranks as the real". See also the discussion below [&#167;305](#305)


###### Der &#220;bergang

> {#305} &#167;305 Die Idealit&#228;t kann die Qualit&#228;t der Unendlichkeit genannt werden; aber sie ist wesentlich der Proce&#223; des Werdens und damit ein &#220;bergang, wie des Werdens in Daseyn, der nun anzugeben ist. Als [[Aufhebung|Aufheben]] der Endlichkeit, d. i. der Endlichkeit als solcher und ebenso sehr der ihr nur gegen&#252;berstehenden, nur negativen Unendlichkeit ist diese R&#252;ckkehr in sich, Beziehung auf sich selbst, Seyn. Da in diesem Seyn Negation ist, ist es Daseyn, aber da sie ferner wesentlich Negation der Negation, die sich auf sich beziehende Negation ist, ist sie das Daseyn, welches F&#252;rsichseyn genannt wird.

> &#167;305 Ideality can be called the _quality_ of infinity; but it is essentially the process of _becoming_, and hence a transition &#8212; like that of becoming in determinate being &#8212; which is now to be indicated. As a sublating of finitude, that is, of finitude as such, and equally of the infinity which is merely its opposite, merely negative, this return into self is _self-relation_, _being_. As this being contains negation it is _determinate_, but as this negation further is essentially negation of the negation, the self-related negation, it is that determinate being which is called _being-for-self_.


If we take the "infinite" and the "infinitesimal" to go together -- as in [&#167;502](#502) -- then the above would give also that _ideality is the quality of the infinitesimal_. 

Now we had already that quality is the [[duality of opposites]] expressed by [[shape modality]] and [[flat modality]]

$$
  \array{
    quality \colon &#643; \dashv \flat
  }
$$

and moreover, mathematically, the infinitesimal is expressed by the infinitesimal analog of this, namely the [[adjunction]] between the [[infinitesimal shape modality]] $&#643;_{inf}$ and [[infinitesimal shape modality]] $\flat_{inf}$.

This would suggest to translate "ideality is the quality of the infinite" by the part 

$$
  \array{
    ideality & \colon&  &#643;_{inf} &\dashv& \flat_{inf}
    \\
    && \vee && \vee
    \\
    quality &\colon&  &#643; &\dashv& \flat
  }
$$

in the [Proce&#223;](#Process).

On the other hand, mathematically we actually have an [[adjoint triple]] $\Re \dashv &#643;_{inf} \dashv \flat_{inf}$, with the [[reduction modality]] on the  left. Recall that the reduction modality expresses precisely the "disappearance of infinitesimal quantity" in [&#167;174](#174).

This may be rearranged as a second order unity of opposites

$$
  \array{
    && \Re &\dashv& &#643;_{inf}
    \\
    && \bot && \bot
    \\
    && &#643;_{inf} &\dashv& \flat_{inf}
  }
$$

and so "ideality" could also be translated to $\Re \dashv &#643;_{inf}$. 

Now by [&#167;324](#324) the opposite moment of ideality is _reality_. Noticing that the adjoint pair $&#643;_{inf} \dashv \flat_{inf}$ is what axiomatizes [[étale toposes]], [[manifolds]], and [[étale groupoids]] (as discussed at [[differential cohesion]]), it does make sense to think of this in terms of "reality": among all the objects in a differentially cohesive $\infty$-topos, those, that are "geometric" in the sense of [[geometric stack]], hence those that would actually model, for instance, a [[spacetime]], but not those that model more "non-real" spaces such as moduli spaces, are precisely the &#233;tale objects (see also the discussion at _[[higher geometry]]_). This may also fit with [&#167;304](#304) above.

The view that the concept of [[infinitesimals]] are closely related to reality is also expressed in [Cohen83, secion 19](#Cohen83):

> F&#252;r diesen H&#246;hepunkt kritischer Naturerkenntnis bildet die Charakteristik der infinitesimalen Gr&#246;&#223;e als intensiver die notwendige Vermittlung;  denn die kritische Bedeutung der Realit&#228;t wird  vorzugsweise  an der  infinitesimalen Intensit&#228;t  durchgef&#252;hrt.

In view of all this, it makes sense to translate as follows:

$$
  \array{
    ideality & \colon& \Re &\dashv&  &#643;_{inf}
    \\    
    && \bot && \bot
    \\
    reality & \colon&  &#643;_{inf} &\dashv& \flat_{inf}
    \\
    && \vee && \vee
    \\
    quality &\colon&  &#643; &\dashv& \flat
  }
$$

as part of the [Proce&#223;](#Process).

Notice that here the bottom step upward is an [[Aufhebung]] in the mathematical sense that $\flat_{inf} \circ &#643; \simeq &#643;$. In view of this, we learn from [&#167;305](#305) 
"Die Idealit&#228;t ... Als [[Aufhebung|Aufheben]] der Endlichkeit" that we might label this as

$$
  \array{
    ideality & \colon& \Re &\dashv&  &#643;_{inf}
    \\    
    && \bot && \bot
    \\
    reality & \colon&  &#643;_{inf} &\dashv& \flat_{inf}
    \\
    Aufhebung\;der\;Endlichkeit & & \vee && \vee
    \\
    quality &\colon&  &#643; &\dashv& \flat
  }
$$



> {#316} &#167;316 Anmerkung 2. Der Satz, da&#223; das Endliche ideell ist, macht den Idealismus aus. Der Idealismus der Philosophie besteht in nichts anderem, als darin, das Endliche nicht als ein wahrhaft Seyendes anzuerkennen. Jede Philosophie ist wesentlich Idealismus, oder hat denselben wenigstens zu ihrem Princip, und die Frage ist dann nur, inwiefern dasselbe wirklich durchgef&#252;hrt ist. Die Philosophie ist es so sehr als die Religion; denn die Religion anerkennt die Endlichkeit ebenso wenig als ein wahrhaftes Seyn, als ein Letztes, Absolutes, oder als ein Nicht-Gesetztes, Unerschaffenes, Ewiges. Der Gegensatz von idealistischer und realistischer Philosophie ist daher ohne Bedeutung. Eine Philosophie, welche dem endlichen Daseyn als solchem wahrhaftes, letztes, absolutes Seyn zuschriebe, verdiente den Namen Philosophie nicht; Principien &#228;lterer oder neuerer Philosophien, das Wasser, oder die Materie oder die Atome sind Gedanken, Allgemeine, Ideelle, nicht Dinge, wie sie sich unmittelbar vorfinden, d. h. in sinnlicher Einzelnheit, selbst jenes thaletische Wasser nicht; denn, obgleich auch das empirische Wasser, ist es au&#223;erdem zugleich das Ansich oder Wesen aller anderen Dinge; und diese sind nicht selbstst&#228;ndige, in sich gegr&#252;ndete, sondern aus einem Anderen, dem Wasser, gesetzte, d. i. ideelle. Indem vorhin das Princip, das Allgemeine, das Ideelle genannt worden, wie noch mehr der Begriff, die Idee, der Geist, Ideelles zu nennen ist, und dann wiederum die einzelnen sinnlichen Dinge als ideell im Princip, im Begriffe, noch mehr im Geiste, als aufgehoben sind, so ist dabei auf dieselbe Doppelseite vorl&#228;ufig aufmerksam zu machen, die bei dem Unendlichen sich gezeigt hat, n&#228;mlich da&#223; das eine Mal das Ideelle das Konkrete, Wahrhaftseyende ist, das andere Mal aber ebenso sehr seine Momente das Ideelle, in ihm Aufgehobene sind, in der That aber nur das Eine konkrete Ganze ist, von dem die Momente untrennbar sind.



#### Third chapter. Das F&#252;rsichsein / Being for self

> {#318} &#167;318 Im F&#252;rsichseyn ist das qualitative Seyn vollendet;

> &#167;318 In being-for-self, qualitative being finds its consummation;

> &#167;319 Being-for-self is first, immediately a being-for-self &#8212; the One.

  Secondly, the One passes into a plurality of ones &#8212; repulsion &#8212; and this otherness of the ones is sublated in their ideality &#8212; attraction.

  Thirdly, we have the alternating determination of repulsion and attraction in which they collapse into equilibrium, and quality, which in being-for-self reached its climax, passes over into quantity.

Here we have a second-order unity of opposites: quantity itself is


quantity : discreteness $\dashv$ continuity

and by the above we take the 

continuum : repulsion $\dashv$ attraction 

to be quality, then we get from the [[adjoint triple]] 

[[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]]

the duality of dualities

$$
  \array{
    & attraction && repulsion
    \\
    quality : & &#643; &\dashv& \flat
    \\
    & \bot && \bot
    \\
    quantity : & \flat &\dashv& \sharp
    \\
    & discreteness && continuity
  }
$$




##### A. Das F&#252;rsichsein als solches / Being-for-self as such



###### a. Dasein und F&#252;rsichsein / Determinate being and Being-for-self

> {#321} &#167;321 Das F&#252;rsichseyn ist, wie schon erinnert ist, die in das einfache Seyn zusammengesunkene Unendlichkeit; es ist Daseyn, insofern die negative Natur der Unendlichkeit, welche Negation der Negation ist, in der nunmehr gesetzten Form der Unmittelbarkeit des Seyns, nur als Negation &#252;berhaupt, als einfache qualitative Bestimmtheit ist.

> &#167;321 But being, which in such determinateness is determinate being, is also at once distinct from being-for-self, which is only being-for-self in so far as its determinateness is the infinite one above-mentioned; nevertheless, determinate being is at the same time also a moment of being-for-self; for this latter, of course, also contains being charged with negation. Thus the determinateness which in determinate being as such is an other, and a being-for-other, is bent back into the infinite unity of being-for-self, and the moment of determinate being is present in being-for-self as a being-for-one.

###### b. Sein-f&#252;r-Eines / Being-for-one

> {#322} &#167;322 To be 'for self' and to be 'for one' are therefore not different meanings of ideality, but are essential, inseparable moments of it.


###### Anmerkung
 {#RemarkOnRealityAsOppositeToDuality}

> {#324} &#167;324 Die Idealit&#228;t kommt zun&#228;chst den aufgehobenen Bestimmungen zu, als unterschieden von dem, worin sie aufgehoben sind, das dagegen als das Reelle genommen werden kann. So aber ist das Ideelle wieder eins der Momente und das Reale das andere; 

> &#167;324 But thus the ideal is again one of the moments, and the real the other;

Hence we have another [[unity of opposites]] is $ideality \dashv reality$. See also at _[The One and the Many](#EinsUndVieles)_.

It seems that in _Science of Logic_ there is no _name_ given to this unity. But in the [shorter logic](#EPSBOI) there is: 

> {#EL214} EL&#167;214 The Idea may be described in many ways. It may be called reason; (and this is the proper philosophical signification of reason); subject-object; the unity of the ideal and the real, of the finite and the infinite, of soul and body; the possibility which has its actuality in its own self; that of which the nature can be thought only as existent, etc. 

(Regarding "soul and body" see also the comments at _[The monad of Leibniz](#TheMonadOfLeibniz)_, where the similarity to the standard terminology "soul" and "body" for (super-)infinitesimals is pointed out.)


So in the [Dictionary](#Dictionary) we add

$$
  \array{
    & \text{f&#252;r sich sein} && \text{f&#252;r eins sein}
    \\
    ideality & \Re &\dashv& &#643;_{inf}
    \\
    & \bot &Idea& \bot
    \\
    reality & &#643;_{inf} &\dashv& \flat_{inf}
  }
$$

(See below _[The idea](#TheIdea)_ and notice [PN&#167;192](#PN192).)

We might interpret this as follows: the $(&#643;_{inf} \dashv \flat_{inf})$-adjunction is that which, by the discussion at _[[differential cohesion]]_, makes all types $X$ have an associated [[structured (infinity,1)-topos|structured]] [[étale topos]] $(Sh(X), \mathcal{O}_X)$. In a sense this gives the type $X$ a "reality" as a topos.

Hence in view of the previous disucssion at _[Existence As Such](#ExistenceAsSuch)_ it seems we have the following

* types have "being" in the presence of $(\emptyset \dashv \ast)$

  * types moreover have "existence"/Dasein in the further presence of $(&#643; \dashv \flat)$.

    * types moreover have "reality" in the further presence of $(&#643;_{inf} \dashv \flat_{inf})$

in other words we have the following situation, in view of p. 7 of _[[Some Thoughts on the Future of Category Theory]]_:

$$
   \array{
      reines\;Sein && Dasein && Realitaet
      \\
      being && existence && reality
      \\
       pure\,being && determinate\,being 
      \\
      \\
      && && \Re & \subset & id
      \\
     && && \bot && \bot
      \\
      && &#643; & \subset & &#643;_{inf} & \subset & id
      \\
      && \bot && \bot 
      \\
      \emptyset &\subset& \flat & \subset & \flat_{inf}
      \\
      \bot & & \bot && 
      \\
      \ast & \subset& \sharp      
   }
$$

where "$\subset$" denotes inclusion of modal types

Equivalently we may arrange this as follows

$$
  \array{
    id &\dashv& id
    \\
    \vee && \vee 
    \\
    \Re &\dashv& &#643;_{inf}
    \\
    \bot && \bot 
    \\
    &#643;_{inf} &\dashv& \flat_{inf}
    \\
    \vee && \vee 
    \\
    &#643; &\dashv& \flat
    \\
    \bot && \bot 
    \\
    \flat &\dashv& \sharp
    \\
    \vee && \vee 
    \\
    \emptyset &\dashv& \ast 
    \\
  }
$$

to exhibit a Proce&#223; (Bewegung) of oppositions and their Aufhebung.

See the labeled diagram _[Proce&#223;](#Process)_ below.

See also the commented diagram for _[gauge](#gauge)_ below.

###### c. Eins

> &#167;328 Being-for-self is the simple unity of itself and its moment, being-for-one.

> &#167;329 The moments which constitute the Notion of the one as a being-for-self fall asunder in the development. They are: (1) negation in general, (2) two negations, (3) two that are therefore the same, (4) sheer opposites, (5) self-relation, identity as such, (6) relation which is negative and yet to its own self.

If we translate "moment" as [[modality]] then here the 
[[double negation modality]] comes to mind.

Notice that the [[empty type]] and the [[unit type]] are the [[modal types]] for the [[double negation modality]].

##### B. Eins und Vieles. / The One and the Many
 {#EinsUndVieles}

> Die Idealit&#228;t des F&#252;rsichseyns als Totalit&#228;t schl&#228;gt so f&#252;rs erste in die Realit&#228;t um, und zwar in die festeste, abstrakteste, als Eins.

###### a. Das Eins an ihm selbst

###### b. Das Eins und das Leere / The One and the Void

> &#167;335 The one is the void as the abstract relation of the negation to itself. 

###### $\;\;$ Remark: Atomism
 {#Atomism}

> &#167;337 The one in this form of determinate being is the stage of the category which made its appearance with the ancients as the atomistic principle, according to which the essence of things is the atom and the void.

Eins: [[atom]], [[infinitesimally thickened point]]

###### c. Viele Eins. Repulsion. / Many ones. Repulsion.

> &#167;340 The one and the void constitute the first stage of the determinate being of being-for-self. Each of these moments has negation for its determination and is at the same time posited as a determinate being; according to the former determination the one and the void are the relation of negation to negation as of an other to its other: the one is negation in the determination of being, and the void is negation in the determination of non-being.

Das Eins (the One): $\ast$ [[unit type]]

Das Leere (the void): $\emptyset$ [[empty type]] ( _leere Menge_ !)

Negation $(\not X) \coloneqq (X \to \emptyset)$

$\ast \simeq \not \emptyset$.

> {#342} &#167;342 the one repels itself from itself. The negative relation of the one to itself is repulsion.

> &#167;343 This repulsion as thus the positing of many ones but through the one itself, is the one's own coming-forth-from-itself but to such outside it as are themselves only ones. This is repulsion according to its Notion, repulsion in itself. The second repulsion is different from it, it is what is immediately suggested to external reflection: repulsion not as the generation of ones, but only as the mutual repelling of ones presupposed as already present. 


To see a formalization of "the one repels itself from itself",
suppose we have a [[shape modality]] $&#643;$ but without the assumption that it preserves finite product types. (This is what the term "[[shape of an (infinity,1)-topos|shape]]" really refers to).

Then given just the [[empty type]] $\emptyset$ and the [[unit type]] $\ast$, there is one new [[type]] to be formed (since necessarily $&#643; \emptyset \simeq \emptyset$) and this is

$$
  &#643; \ast 
$$

Below we see that this, being a [[discrete type]], is what Hegel describes with "repulsion": The points in $&#643; \ast$ do not attract/cohese, they are different and repel.

At the same time, being a [[discrete type]] it is necessarily a [[homotopy colimit]] of copies of the [[unit type]] (see [here](limit+in+a+quasi-category#Tensoring))

$$
  &#643; \ast \simeq \underset{\longrightarrow}{\lim}_I \ast
$$

where the [[diagram]] $I$ that the colimit is over is $I = &#643; \ast$ itself.

For a similar argument see Lawvere's  _[Cohesive toposes and Cantor's Lauter Einsen ](#LawvereLauterEinsen))_. On p. 6 there is suggested that the [[unity of opposites]] "all elements of a set are indistinguishable and yet distinct" is captured by the fact that both

$\flat X$ as well as $\sharp X$ have the same image under $\flat$.

###### $\;\;$ Remark: The Monad of Leibniz
 {#TheMonadOfLeibniz}

> &#167;348 We have previously referred to the [[Gottfried Leibniz|Leibnizian]] idealism. We may add here that this idealism which started from the ideating [[monad (disambiguation)|monad]], which is determined as being for itself, advanced only as far as the repulsion just considered, and indeed only to plurality as such, in which each of the ones is only for its own self and is indifferent to the determinate being and being-for-self of the others; or, in general, for the one, there are no others at all. The monad is, by itself, the entire closed universe; it requires none of the others. But this inner manifoldness which it possesses in its ideational activity in no way affects its character as a being-for-self. The Leibnizian idealism takes up the plurality immediately as something given and does not grasp it as a repulsion of the monads. Consequently, it possesses plurality only on the side of its abstract externality. 

  The atomistic philosophy does not possess the Notion of ideality; it does not grasp the one as an ideal being, that is, as containing within itself the two moments of being-forself and being-for-it, but only as a simple, dry, real being-for-self. 

  It does, however, go beyond mere indifferent plurality; the atoms become further determined in regard to one another even though, strictly speaking, this involves an inconsistency; whereas, on the contrary, in that indifferent independence of the monads, plurality remains as a fixed fundamental determination, so that the connection between them falls only in the monad of monads, or in the philosopher who contemplates them.

To summarize, in [&#167;322](#322) we get a clear prescription:

> To be 'for self' and to be 'for one' are therefore not different meanings of ideality, but are essential, inseparable moments of it.

So we are to find an [[adjoint modality]] that expresses 

$$
  Ideality \;\colon\; BeingForSelf \dashv BeingForOne
$$

(or possibly the other way around).

The complaint about Leibniz in &#167;348, makes pretty clear what this is about:

> The atomistic philosophy does not possess the Notion of ideality; it does not grasp the one as an ideal being, that is, as containing within itself the two moments of being-forself and being-for-it, but only as a simple, dry, real being-for-self.

Here "atoms" really refers to the decomposition of the continuum into points (atoms of space, as in [[monad in nonstandard analysis]]) because in &#167;337 it says:

> The one in this form of determinate being is the stage of the category which made its appearance with the ancients as the atomistic principle, according to which the essence of things is the atom and the void.

But "The one" (The unit) with its repulsion of many we claimed before is well modeled by what $\flat$ produces, the underlying points, the atoms of space.

So in conclusion the statement here is that it is a defect of both the ancients as well as of Leibniz to consider atoms/monads/points which have no way to look outside of themselves into interaction with others, that instead one needs to characterized atoms/monads/points by the above adjoint modality which expresses _Ideality_.

In conclusion, _Eins_ ("The One"/"The Unit") is a notion of atom which is similar to what the ancients and Leibniz called atom/monad, only that it improves on that by keeping an additional "moment" which the ancients and Leibniz forgot to retain. 

Now in [[William Lawvere]]'s _[Toposes of Laws of Motion](#LawvereMotion)_  "atom" is proposed to refer to, essentially, [[infinitesimally thickened points]]. Indeed, the "infinitesimal thickening" of the point has  something to do with the point "coming out of itself"and interacting with other points. 

So possibly the [[adjoint modality]] given by [[reduction modality]] $\dashv$ [[infinitesimal shape modality]] captures some of this well.

Here is a cartoon of an [[infinitesimally thickened point]] with its infinitesimal antennas reaching out to test what's going on around

$$
  \array{
      -- \bullet -- 
  }
$$

and here is the [[reduced object|reduced point]], all by itself/for itself

$$
  \array{
      \bullet
  }
  \,.
$$

Notice that in [[superalgebra]] one says "[[soul]]" for these "antennas" and "[[body]]" for what remains. (This happens to fit well with [EL&#167;214](#EL214)) Therefore it seems plausible to conclude that the formalization of the [[unity of opposites]]

$$
  Ideality \;\colon\; BeingForSelf \dashv BeingForOne
$$

is the [[adjoint modality]] given by [[reduction modality]] $\dashv$ [[infinitesimal shape modality]]. The "Ideality" of infinitesimal extension gives the Eins, the atom-of-space, its dual character of containing a reduced point for-itself and at the same time an infinitesimal thickening that extends beyond that.



##### C. Repulsion und Attraktion

###### a. Ausschli&#223;en des Eins.

###### b. Das Eine Eins der Attraktion

###### c. Die Beziehung der Repulsion und der Attraktion
 {#RelationBetweenRepulsionAndAttraction}


> {#369} &#167;369 Die Repulsion daseyender Eins ist die Selbsterhaltung des Eins durch die gegenseitige Abhaltung der andern, so da&#223; 1) die anderen Eins an ihm negirt werden, die&#223; ist die Seite seines Daseyns oder seines Seyns-f&#252;r-Anderes; diese ist aber somit Attraktion, als die Idealit&#228;t der Eins;&#8212;und da&#223; 2) das Eins an sich sey, ohne die Beziehung auf die andere; aber nicht nur ist das Ansich &#252;berhaupt l&#228;ngst in das F&#252;rsichseyn &#252;bergegangen, sondern an sich, seiner Bestimmung nach, ist das Eins jenes Werden zu Vielen.&#8212;Die Attraktion daseyender Eins ist die Idealit&#228;t derselben, und das Setzen des Eins, worin sie somit als Negiren und Hervorbringen des Eins sich selbst aufhebt, als Setzen des Eins das Negative ihrer selbst an ihr, Repulsion ist.

> &#167;369 The repulsion of the determinately existent ones is the self-preservation of the one through the mutual repulsion of the others, so that (1) the other ones are negated in it-this is the side of its determinate being or of its being-for-other; but this is thus attraction as the ideality of the ones; and (2) the one is in itself, without relation to the others; but not only has being-in-itself as such long since passed over into being-for-self, but the one in itself, by its determination, is the aforesaid becoming of many ones. The attraction of the determinately existent ones is their ideality and the positing of the one, in which, accordingly, attraction as a negating and a generating of the one sublates itself, and as a positing of the one is in its own self the negative of itself, repulsion.



> &#167;370 Damit ist die Entwickelung des F&#252;rsichseyns vollendet und zu ihrem Resultate gekommenen.

> &#167;370 With this, the development of being-for-self is completed and has reached its conclusion.

Since _Dasein_ and _F&#252;rsichsein_ both are qualitative being/are quality ([&#167;188](#188), [&#167;318](#318), [&#167;321](#321))  the above gives us the [[unity of opposites]]

$$
  quality \;\colon\; attraction \dashv repulsion
$$

###### Remark: The Kantian Construction of Matter from the Forces of Attraction and Repulsion


> &#167;374 Kant, as we know, constructed matter from the forces of attraction and repulsion, or at least he has, to use his own words, set up the metaphysical elements of this construction.

Not about actual [[forces]] in [[matter]] so much as about what makes the points in the [[continuum]] both stay apart (repulsion) and at the same time hang together (attraction/cohesion).




### Second section. The magnitude

#### First chapter. Die Quantit&#228;t / The quantity

##### A. Die reine Quantit&#228;t / Pure quantity
 {#PureQuantity}

> [&#167;398](#398) Die Quantit&#228;t ist die Einheit dieser Momente, der Kontinuit&#228;t und Diskretion

> &#167;398 Quantity is the unity of these moments of continuity and discreteness

By [[unity of opposites]] and since the [[flat modality]] matches the "moment of discreteness" this is the duality with the [[sharp modality]]

$$
  \array{
    \flat X &\longrightarrow& X &\longrightarrow& \sharp X
    \\
    {moment\;of \atop discreteness}
    && 
    &&
    {moment\;of \atop continuity}
  }
$$

###### On attraction / cohesion 

> &#167;395 Attraction is in this way the moment of continuity in quantity.

attraction is what holds stuff together, hence this is the idea of [[cohesion]]

if $X$ has continuity then the [[shape modality]] $&#643; X$ is the result of letting things collaps under their cohesion/attraction


###### On discreteness and repulsion
 {#OnDiscretenessAndRepulsion}

> &#167;397 In continuity, therefore, magnitude immediately possesses the moment of discreteness &#8212; repulsion, as now a moment in quantity. 

continuous object $X$ possesses moment 
of [[discrete object|discreteness]]= [[flat modality]] $\flat X$

> &#167;398 Quantity is the unity of these moments of continuity and discreteness,


By the formalization of [[unity of opposites]] this must mean that 
"moment of continuity" is the [[right adjoint]] [[modality]] to the [[flat modality]].  This is the [[sharp modality]] $\sharp$. Therefore their [[unity of opposites]] is

$$
  quantity
    \;\colon\;
  \array{ 
     \flat X &\longrightarrow& X &\longrightarrow& \sharp X
      \\
      \\
      {moment\;of \atop discreteness}
      &&
      &&
      {moment\;of \atop continuity}  
  } 
$$

Notice that by[[Lawvere]]'s _[Cohesive Toposes and Cantor's "lauter Einsen"](#LawvereLauterEinsen)_ precisely this [[unity of opposites]] is that characteristic of [[cardinality]] (Mengen/Kardinalen).

we also have

$$
  \array{
    \flat X &\longrightarrow& X &\longrightarrow& &#643; X
    \\
    repulsion &&  && { attraction/ \atop cohesion } 
  }
$$


##### B. Kontinuirliche und diskrete Gr&#246;&#223;e.

###### On the continuum

* &#167;400 Mathematics, on the other hand, rejects a metaphysics which would make time consist of points of time; space in general &#8212; or in the first place the line &#8212; consist of points of space; the plane, of lines; and total space of planes. It allows no validity to such discontinuous ones. Even though, for instance, in determining the magnitude of a plane, it represents it as the sum of infinitely many lines, this discreteness counts only as a momentary representation, and the sublation of the discreteness is already implied in the infinite plurality of the lines, since the space which they are supposed to constitute is after all bounded.

The [[continuum]].


> Diese Antinomie besteht allein, darin da&#223; die Diskretion eben so sehr als die Kontinuit&#228;t behauptet werden mu&#223;. Die einseitige Behauptung der Diskretion giebt das unendliche oder absolute Getheiltseyn, somit ein Untheilbares zum Princip; die einseitige Behauptung der Kontinuit&#228;t dagegen die unendliche Theilbarkeit.


###### On space, time, matter


> &#167;432 Space, time, matter, and so forth are continuous magnitudes 




##### C. Begrenzung der Quantit&#228;t 


#### Second chapter. Quantum

##### A. Die Zahl

##### B. Extensives und Intensives Quantum

##### C. Die quantitative Unendlichkeit

###### a. Begriff derselben

###### b. Der quantitative unendliche Progre&#223;
 {#DerQuantitativeUnendlicheProgress}

> &#167;500 The progress to infinity is in general the expression of contradiction, here, of that which is implicit in the quantitative finite, or quantum as such. It is the reciprocal determining of the finite and infinite which was considered in the sphere of quality, with the difference that, as just remarked, in the sphere of quantity the limit in its own self dispatches and continues itself into its beyond and hence, conversely, the quantitative infinite too is posited as having quantum within it; for quantum in its self-externality is also its own self, its externality belongs to its determination.

> &#167;501 Now the infinite progress is only the expression of this contradiction, not its resolution; but because the one determinateness is continued into its other, the progress gives rise to the show of a solution in a union of both. As at first posed, it is the problem of attaining the infinite, not the actual reaching of it; it is the perpetual generation of the infinite, but it does not get beyond quantum, nor does the infinite become positively present. It belongs to the Notion of quantum to have a beyond of itself. This beyond is first, the abstract moment of the non-being of quantum: the vanishing of quantum is its own act; it is thus related to its beyond as to its infinity, in accordance with the qualitative moment of the opposition. Secondly, however, quantum is continuous with its beyond; quantum consists precisely in being the other of itself, in being external to itself; this externality is, therefore, no more an other than quantum itself; the beyond or the infinite is, therefore, itself a quantum. In this way, the beyond is recalled from its flight and the infinite is attained. But because the infinite now affirmatively present is again a quantum, what has been posited is only a fresh limit; this, too, as a quantum, has again fled from itself, is as such beyond itself and has repelled itself into its non-being, into its own beyond, and as it thus repels itself into the beyond, so equally does the beyond perpetually become a quantum.

> [&#167;502](#502) Die Kontinuit&#228;t des Quantums in sein Anderes bringt die Verbindung beider in dem Ausdruck eines Unendlich-Gro&#223;en oder Unendlich-Kleinen hervor. Da beide die Bestimmung des Quantums noch an ihnen haben, bleiben sie ver&#228;nderliche und die absolute Bestimmtheit, die ein F&#252;r-sichseyn w&#228;re, ist also nicht erreicht. Die&#223; Au&#223;ersichseyn der Bestimmung ist in dem gedoppelten Unendlichen, das sich nach dem Mehr und Weniger entgegengesetzt ist, dem Unendlich-gro&#223;en und Kleinen, gesetzt. An jedem selbst ist das Quantum im perennirenden Gegensatze gegen sein Jenseits erhalten. Das Gro&#223;e noch so sehr erweitert, schwindet zur Unbetr&#228;chtlichkeit zusammen; indem es sich auf das Unendliche als auf sein Nichtseyn bezieht, ist der Gegensatz qualitativ; das erweiterte Quantum hat daher dem Unendlichen nichts abgewonnen; dieses ist vor wie nach das Nichtseyn desselben. Oder, die Vergr&#246;&#223;erung des Quantums ist keine N&#228;herung zum Unendlichen, denn der Unterschied des Quantums und seiner Unendlichkeit hat wesentlich auch das Moment ein nicht quantitativer Unterschied zu seyn. Es ist nur der ins Engere gebrachte Ausdruck des Widerspruchs; es soll ein Gro&#223;es d. i. ein Quantum, und unendlich, d. i. kein Quantum seyn.&#8212;Eben so das Unendlichkleine ist als Kleines ein Quantum und bleibt daher absolut d. h. qualitativ zu gro&#223; f&#252;r das Unendliche, und ist diesem entgegengesetzt. Es bleibt in beiden der Widerspruch des unendlichen Progresses erhalten der in ihnen sein Ziel gefunden haben sollte.


> &#167;502 The continuity of quantum with its other produces the conjunction of both in the expression of an infinitely great or infinitely small. Since both still bear the character of quantum they remain alterable, and the absolute determinateness which would be a being-for-self is, therefore, not attained. This self-externality of the determination is posited in the dual infinite &#8212; which is opposed to itself as a 'more' and a 'less' &#8212; in the infinitely great and infinitely small. In each, the quantum is maintained in perpetual opposition to its beyond. No matter how much the quantum is increased, it shrinks to insignificance; because quantum is related to the infinite as to its non-being, the opposition is qualitative; the increased quantum has therefore gained nothing from the infinite, which is now, as before, the non-being of quantum. In other words, the increase of quantum brings it no nearer to the infinite; for the difference between quantum and its infinity is essentially not a quantitative difference. The expression 'the infinitely great' only throws the contradiction into sharper relief; it is supposed to be great, that is, a quantum, and infinite, that is, not a quantum. Similarly, the infinitely small is, as small, a quantum, and therefore remains absolutely, that is, qualitatively, too great for the infinite and is opposed to it. In both, there remains the contradiction of the infinite progress which in them should have reached its goal.


####### Anmerkung 1


####### Anmerkung 2



###### c. Die Unendlichkeit des Quantums

####### Anmerkung 1

> In R&#252;cksicht der Erhaltung des Verh&#228;ltnisses im Verschwinden der Quantorum findet sich (anderw&#228;rts, wie bei Carnot, R&#233;flexions sur la M&#233;taphysique du Calcul Infinit&#233;simal.) der Ausdruck, da&#223; verm&#246;ge des Gesetzes der St&#228;tigkeit die verschwindenden Gr&#246;&#223;en noch das Verh&#228;ltni&#223;, aus dem sie herkommen, ehe sie verschwinden, behalten. &#8212;Diese Vorstellung dr&#252;ckt die wahre Natur der Sache aus, insofern nicht die St&#228;tigkeit des Quantums verstanden wird, die es im unendlichen Progre&#223; hat, sich in sein Verschwinden so zu kontinuiren, da&#223; im Jenseits seiner wieder nur ein endliches Quantum, ein neues Glied der Reihe entsteht; ein st&#228;tiger Fortgang wird aber immer so vorgestellt, da&#223; die Werthe durchloffen werden, welche noch endliche Quanta sind.

> In demjenigen &#220;bergange dagegen, welcher in das wahrhafte Unendliche gemacht wird, ist das Verh&#228;ltni&#223; das st&#228;tige; es ist so sehr st&#228;tig und sich erhaltend, da&#223; er vielmehr allein darin besteht, das Verh&#228;ltni&#223; rein herauszuheben, und die verh&#228;ltni&#223;lose Bestimmung, d. i. da&#223; ein Quantum, welches Seite des Verh&#228;ltnisses ist, auch au&#223;er dieser Beziehung gesetzt, noch Quantum ist, verschwinden zu machen. &#8212;Diese Reinigung des quantitativen Verh&#228;ltnisses ist insofern nichts anders, als wenn ein empirisches Daseyn begriffen wird. Die&#223; wird hierdurch so &#252;ber sich selbst erhoben, da&#223; sein Begriff dieselben Bestimmungen enth&#228;lt, als es selbst, aber in ihrer Wesentlichkeit und in die Einheit des Begriffes gefa&#223;t, worin sie ihr gleichg&#252;ltiges, begriffloses Bestehen verloren haben.
















### Third section. The measure.
 {#TheMeasure}

> {#699} &#167;699 Im Maa&#223;e sind, abstrakt ausgedr&#252;ckt, Qualit&#228;t und Quantit&#228;t vereinigt.

> &#167;699 Abstractly expressed, in measure quality and quantity are united

(Repeated in [&#167;708](#708), below.)

So by the formalization of [[unity of opposites]] we have 

$$
  measure \colon quantity \dashv quality
$$

and since quantity and quality are already themselves unities of opposites, we find that Ma&#223; (Eichma&#223;) is the second-order adjunction

$$

  \array{
    Qualitaet && \int &\dashv& \flat
    \\
    Eichmass && \bot && \bot
    \\
    Quantitaet y && \flat &\dashv& \sharp
  }
$$

See the _[Proce&#223;](#Process)_ diagram.


> {##703} &#167;703 The observation here made extends generally to those systems of pantheism which have been partially developed by thought. The first is being, the one, substance, the infinite, essence; in contrast to this abstraction the second, namely, all determinateness in general, what is only finite, accidental, perishable, non-essential, etc. can equally abstractly be grouped together; and this is what usually happens as the next step in quite formal thinking. But the connection of this second with the first is so evident that one cannot avoid grasping it as also in a unity with the latter;

> {#708} &#167;708 Das Maa&#223; ist zun&#228;chst unmittelbare Einheit des Qualitativen und
Quantitativen, so da&#223; (1) erstens ein Quantum ist, das qualitative Bedeutung hat, und als Maa&#223; ist. Dessen Fortbestimmung ist, da&#223; an ihm, dem an sich bestimmten, &#8212;der Unterschied seiner Momente, des qualitativen und quantitativen Bestimmtseyns, hervortritt. Diese Momente bestimmen sich weiter selbst zu Ganzen des Maa&#223;es, welche insofern als Selbstst&#228;ndige sind; indem sie sich wesentlich aufeinander beziehen, wird das Maa&#223; (2) zweitens Verh&#228;ltni&#223; von specifischen Quantis, als selbstst&#228;ndigen Maa&#223;en. Ihre Selbstst&#228;ndigkeit beruht aber wesentlich zugleich auf dem quantitativen Verh&#228;ltnisse und dem Gr&#246;&#223;enunterschiede; so wird ihre Selbstst&#228;ndigkeit ein &#220;bergehen in einander. Das Maa&#223; geht damit im Maa&#223;losen zu Grunde.&#8212;Die&#223; Jenseits des Maa&#223;es ist aber die Negativit&#228;t desselben nur an sich selbst; es ist dadurch (3) drittens die Indifferenz der Maa&#223;bestimmungen, und als reell mit der in ihr enthaltenen Negativit&#228;t das Maa&#223; gesetzt, als umgekehrtes Verh&#228;ltni&#223; von Maa&#223;en, welche als selbstst&#228;ndige Qualit&#228;ten wesentlich nur auf ihrer Quantit&#228;t und auf ihrer negativen Beziehung aufeinander beruhen, und damit sich erweisen, nur Momente ihrer wahrhaft selbstst&#228;ndigen Einheit zu seyn, welche ihre Reflexion-in-sich und das Setzen derselben, das Wesen, ist.

> &#167;708 At first, measure is only an immediate unity of quality and quantity, so that: (1), we have a quantum with a qualitative significance, a measure. The progressive determining of this consists in explicating what is only implicit in it, namely, the difference of its moments, of its qualitatively and quantitatively determined being. These moments further develop themselves into wholes of measure which as such are self-subsistent. These are essentially in relationship with each other, and so measure becomes (2), a ratio of specific quanta having the form of self-subsistent measures. But their self-subsistence also rests essentially on quantitative relation and quantitative difference; and so their self-subsistence becomes a transition of each into the other, with the result that measure perishes in the measureless. But this beyond of measure is the negativity of measure only in principle; this results (3), in the positing of the indifference of the determinations of measure, and the positing of real measure &#8212; real through the negativity contained in the indifference &#8212; as an inverse ratio of measures which, as self-subsistent qualities, are essentially based only on their quantity and on their negative relation to one another, thereby demonstrating themselves to be only moments of their truly self-subsistent unity which is their reflection-into-self and the positing thereof, essence.

> {#709} &#167;709 Die Entwickelung des Maa&#223;es, die im Folgenden versucht worden, ist eine der schwierigsten Materien; indem sie von dem unmittelbaren, &#228;u&#223;erlichen Maa&#223;e anf&#228;ngt, h&#228;tte sie einer Seits zu der abstrakten Fortbestimmung des Quantitativen (einer Mathematik der Natur) fortzugehen, anderer Seits den Zusammenhang dieser Maa&#223;bestimmung mit den Qualit&#228;ten der nat&#252;rlichen Dinge anzuzeigen, wenigstens im Allgemeinen; denn die bestimmte Nachweisung des aus dem Begriffe des konkreten Gegenstandes hervorgehenden Zusammenhangs des Qualitativen und Quantitativen geh&#246;rt in die besondere Wissenschaft des Konkreten; wovon Beispiele in der Encykl. der philos. Wissensch. 3te Aufl. _. 267 u. 270 Anm. das Gesetz des Falles und das der freien himmlischen Bewegung betreffend, nachzusehen sind. Es mag hierbei die&#223; &#252;berhaupt bemerkt werden, da&#223; die verschiedenen Formen, in welchen sich das Maa&#223; realisirt, auch verschiedenen Sph&#228;ren der nat&#252;rlichen Realit&#228;t angeh&#246;ren. Die vollst&#228;ndige, abstrakte Gleichg&#252;ltigkeit des entwickelten Maa&#223;es d. i. der Gesetze desselben kann nur in der Sph&#228;re des Mechanismus Statt haben, als in welchem das konkrete K&#246;rperliche nur die selbst abstrakte Materie ist; die qualitativen Unterschiede derselben haben wesentlich das Quantitative zu ihrer Bestimmtheit; Raum und Zeit sind die reinen &#196;u&#223;erlichkeiten selbst, und die Menge der Materien, Massen, Intensit&#228;t des Gewichts, sind ebenso &#228;u&#223;erliche Bestimmungen, die an dem Quantitativen ihre eigenth&#252;mliche Bestimmtheit haben.

> &#167;709 The development of measure which has been attempted in the following chapters is extremely difficult. Starting from immediate, external measure it should, on the one hand, go on to develop the abstract determination of the quantitative aspects of natural objects (a mathematics of nature), and on the other hand, to indicate the connection between this determination of measure and the qualities of natural objects, at least in general; for the specific proof, derived from the Notion of the concrete object, of the connection between its qualitative and quantitative aspects, belongs to the special science of the concrete. Examples of this kind concerning the law of falling bodies and free, celestial motion will be found in the Encyclopedia. of the Phil. Sciences, 3rd ed., Sections 267 and 270, Remark. In this connection the general observation may be made that the different forms in which measure is realised belong also to different spheres of natural reality. The complete, abstract indifference of developed measure, i.e. the laws of measure, can only be manifested in the sphere of mechanics in which the concrete bodily factor is itself only abstract matter; the qualitative differences of such matter are essentially quantitatively determined; space and time are the purest forms of externality, and the multitude of matters, masses, intensity of weight, are similarly external determinations which have their characteristic determinateness in the quantitative element.

Regarding this, see also below [&#167;714](#714).

#### First chapter. Die specifische Quantit&#228;t.
 {#TheMeasureFirstChapter}

##### A. Das specifische Quantum / The Specific Quantum

> {#714} &#167;714 Ein Maa&#223;, als Maa&#223;stab im gew&#246;hnlichen Sinne, ist ein Quantum, das als die an sich bestimmte Einheit gegen &#228;u&#223;erliche Anzahl willk&#252;rlich angenommen wird. Eine solche Einheit kann zwar auch in der That an sich bestimmte Einheit seyn, wie Fu&#223; und dergleichen urspr&#252;ngliche Maa&#223;e; insofern sie aber als Maa&#223;stab zugleich f&#252;r andere Dinge gebraucht wird, ist sie f&#252;r diese nur &#228;u&#223;erliches, nicht ihr urspr&#252;ngliches Maa&#223;.&#8212;So mag der Erddurchmesser, oder die Pendell&#228;nge, als specifisches Quantum f&#252;r sich genommen werden. Aber es ist willk&#252;rlich, den wievielsten Theil des Erddurchmessers oder der Pendell&#228;nge und unter welchem Breitengrade man diese nehmen wolle, um sie als Maa&#223;stab zu gebrauchen. Noch mehr aber ist f&#252;r andere Dinge ein solcher Maa&#223;stab etwas &#196;u&#223;erliches. Diese haben das allgemeine specifische Quantum wieder auf besondere Art specificirt, und sind dadurch zu besondern Dingen gemacht. Es ist daher th&#246;richt, von einem nat&#252;rlichen Maa&#223;stab der Dinge zu sprechen. Ohnehin soll ein allgemeiner Maa&#223;stab nur f&#252;r die &#228;u&#223;erliche Vergleichung dienen; in diesem oberfl&#228;chlichsten Sinne, in welchem er als allgemeines Maa&#223; genommen wird, ist es v&#246;llig gleichg&#252;ltig, was daf&#252;r gebraucht wird. Es soll nicht ein Grundmaa&#223; in dem Sinne seyn, da&#223; die Naturmaa&#223;e der besondern Dinge daran dargestellt und daraus nach einer Regel, als Specifikationen Eines allgemeinen Maa&#223;es, des Maa&#223;es ihres allgemeinen K&#246;rpers, erkannt w&#252;rden. Ohne diesen Sinn aber hat ein absoluter Maa&#223;stab nur das Interesse und die Bedeutung eines Gemeinschaftlichen, und ein solches ist nicht an sich, sondern durch &#220;bereinkommen ein Allgemeines.

> &#167;714 A measure taken as a standard in the usual meaning of the word is a quantum which is arbitrarily assumed as the intrinsically determinate unit relatively to an external amount. Such a unit can, it is true, also be in fact an intrinsically determinate unit, like a foot and suchlike original measures; but in so far as it is also used as a standard for other things it is in regard to them only an external measure, not their original measure. Thus the diameter of the earth or the length of a pendulum may be taken, each on its own account, as a specific quantum; but the selection of a particular fraction of the earth's diameter or of the length of the pendulum, as well as the degree of latitude under which the latter is to be taken for use as a standard, is a matter of choice. But for other things such a standard is still more something external. These have further specified the general specific quantum in a particular way and have thereby become particular things. It is therefore foolish to speak of a natural standard of things. Moreover, a universal standard ought only to serve for external comparison; in this most superficial sense in which it is taken as a universal measure it is a matter of complete indifference what is used for this purpose. It ought not to be a fundamental measure in the sense that it forms a scale on which the natural measures of particular things could be represented and from which, by means of a rule, they could be grasped as specifications of a universal measure, i.e. of the measure of their universal body. Without this meaning, however, an absolute measure is interesting and significant only as a common element, and as such is a universal not in itself but only by agreement.

This concept of _Ma&#223;stab_ in [&#167;714](#714) is very explicitly that of _Eichma&#223;_, a _choice_ that is made (durch &#220;bereinkommen). The English translation that captures this maybe more properly than "standard" is "[[gauge]]".

This aspect is further amplified below in [&#167;725](#725), which states that this choice is the choice of _Einheit_ (unit), i.e. Ma&#223;einheit. Mathematically, indeed, the choice of units is precisely a choice of [[gauge]] as in [[gauge theory]]. See at _[[physical unit]]_ for more on this. By the discussion there (see also at _[[torsor]]_), this is indeed all about ratios, just as stated in [&#167;708](#708) above. 

(Observe also that [&#167;709](#709) above said that to develop a theory of measure, hence a theory of gauge, is to develop a "mathematics of nature". Moreover, by [Philosophy of Nature &#167;202](Philosophy+of+Nature#202) "The truly philosophical science of mathematics as theory of magnitude would be the science of measures".)

Therefore by ([&#167;699](#699)) we may label this part of the [Proce&#223;](#Process) as follows:

+-- {: bluebox #gauge}
###### .


$$
  \array{
    & & attraction && repulsion
    \\
    & quality : & &#643; &\dashv& \flat
    \\
    gauge & \bot & \bot && \bot
    \\
    & quantity : & \flat &\dashv& \sharp
    \\
    & & discreteness && continuity
  }
$$

=--

This is striking, as at the same time precisely this [[adjoint triple]] is also an abstract axiomatization of ([[higher gauge theory|higher]]) [[gauge theory]] in [[physics]] via [[cohesion]]. This is discussed further at _[[differential cohomology hexagon]]_.


##### B. Specificirendes Ma&#223; / Specifying measure


###### (a) Die Regel / The Rule

> {#725} &#167;725 Die Regel oder der Maa&#223;stab, von dem schon gesprochen worden, ist zun&#228;chst als eine an sich bestimmte Gr&#246;&#223;e, welche Einheit gegen ein Quantum ist, das eine besondere Existenz ist, an einem andern Etwas, als das Etwas der Regel ist, existirt,&#8212;an ihr gemessen, d. i. als Anzahl jener Einheit bestimmt wird. Diese Vergleichung ist ein &#228;u&#223;erliches Thun, jene Einheit selbst eine willk&#252;rliche Gr&#246;&#223;e, die ebenso wieder als Anzahl (der Fu&#223; als eine Anzahl von Zollen) gesetzt werden kann. Aber das Maa&#223; ist nicht nur &#228;u&#223;erliche Regel, sondern als specifisches ist es die&#223;, sich an sich selbst zu seinem Andern zu verhalten, das ein Quantum ist.


> &#167;725 The rule or standard $[$ gauge $]$, which has already been mentioned, is in the first place an intrinsically determinate magnitude which is a unit with reference to a quantum having a particular existence in a something other than the something of the rule; this other something is measured by the rule, i.e. is determined as an amount of the said unit. This comparison is an external act, the unit itself being an arbitrary magnitude which in turn can equally be treated as an amount (the foot as an amount of inches). But measure is not only an external rule; as a specifying measure its nature is to be related in its own self to an other which is a quantum.

Choice of _Einheit_ unit is choice of gauge, as in _[[gauge theory]]_. See at _[[physical unit]]_ for more on this.

###### (b) Das specificirende Ma&#223; / Specifying Measure


###### (c) Verh&#228;ltnis beider Seiten als Qualit&#228;ten / Relation of the two Sides as Qualities

##### C. Das F&#252;rsichseyn im Maa&#223;e

#### Chapter two. Das reale Maa&#223;

#### Chapter three. Das Werden des Wesens.

##### A. Die absolute Indifferenz


##### B. Die Indifferenz als umgekehrtes Verh&#228;ltni&#223; ihrer Faktoren.

##### C. &#220;bergang in das Wesen.
 {#UeberGangInDasWesen}

> {#803} &#167;803 Die absolute Indifferenz ist die letzte Bestimmung des Seyns, ehe dieses zum Wesen wird; 

> &#167;803 Absolute indifference is the final determination of being before it becomes essence; but it does not attain to essence.

Under the formalization of [[unity of opposites]], "absolute indifference" is plausibly the name of the trivial adjunction $id\dashv id$ which describes a difference that is none, hence an indifference.

$$
  Wesen \colon id \dashv id
  \,.
$$

This fits well with the idea in [&#167;803](#803) that the process of determination comes to an end in the Wesen, because indeed $(id \dashv id)$ is the topmost [[level of a topos|level]] in the mathematical sense.

$$
  \array{
     Wesen &\colon& id &\dashv& id
     \\
     && \vee && \vee
     \\
     && \vdots && \vdots
  }
$$

See also [&#167;812](#812)


## **Book two** Die Lehre vom Wesen / The doctrine of essence 
 {#LehreVomWesen}


> {#807} &#167;807 Die Wahrheit des Seins is das Wesen.

> &#167;807 The truth of being is essence.

> {#808} &#167;808 Diese Bewegung, als Weg des Wissens vorgestellt, so erscheint dieser Anfang vom Seyn und der Fortgang, der es aufhebt und beim Wesen als einem Vermittelten anlangt, eine Th&#228;tigkeit des Erkennens zu seyn, die dem Seyn &#228;u&#223;erlich sey und dessen eigene Natur nichts angehe.

> {#809} &#167;809 Aber dieser Gang ist die Bewegung des Seyns selbst. Es zeigte sich an diesem, da&#223; es durch seine Natur sich erinnert, und durch die&#223; Insichgehen zum Wesen wird.

Bewegung des Seins from pure being to essence. The [Proce&#223;](#Process).

> {#812} &#167;812 Das Wesen aber, wie es hier geworden ist, ist das, was es ist, nicht durch eine ihm fremde Negativit&#228;t, sondern durch seine eigne, die unendliche Bewegung des Seyns. Es ist An-und-F&#252;rsichseyn; absolutes Ansichseyn, indem es gleichg&#252;ltig gegen alle Bestimmtheit des Seyns ist, das Andersseyn und die Beziehung auf anderes schlechthin aufgehoben worden ist. 

> &#167;812 But essence as it has here come to be, is what it is, through a negativity which is not alien to it but is its very own, the infinite movement of being. It is being that is in itself and for itself; it is absolute being-in-itself in that it is indifferent to every determinateness of being, and otherness and relation-to-other have been completely sublated.

So Essence is the ultimate [[Aufhebung]], hence the topmost [[level of a topos|level]] 

$$
  \array{
     Wesen &\colon& id &\dashv& id
     \\
     && \vee && \vee
     \\
     && \vdots && \vdots
  }
$$

See the [Proce&#223;](#Process).


> {#816} &#167;816 Das Wesen scheint zuerst in sich selbst, oder ist Reflexion

> &#167;816 At first, essence shines or shows within itself, or is reflection

With the translation from [&#167;803](#803),[&#167;812](#812) of "Das Wesen" = terminal [[Aufhebung]] = "the ambient category", the original German here translates really to: 

> The ambient category appears within itslef

See also [&#167;834](#834), [&#167;1036](#1036), [&#167;1037](#1037) below. 

The [Rezk-Lurie theorem](infinity-topos#CharacterizationByObjectClassifier) states that the very characterization of an [[(infinity,1)-topos|infinity-topos]] is that it (is presentable with universal colimits and) has a [[type of types]] = [[object classifier]] = [[universe]] (in the mathematical sense!). This [[type of types]] is indeed nothing but the small reflection of the full $\infty$-topos inside it self.

(Indeed, [&#167;850](#850) below highlights that "Reflexion" here does _not_ mean the usual "to reflect on a topic" (but means "Reflexion &#252;berhaupt", for what it's worth).)

There is of course not just one [[object classifier]]/[[type of types]] but a hierarchy of them (see also at _[[universe polymorphism]]_)

$$
  Type_1 \subset Type_2 \subset Type_3 \subset Type_4 \subset \cdots
$$

By the above this should correspond to an infinite Reflexion of the Wesen inside itself, and sure enough, this is what [&#167;860](#860) below says.



Notice the following characteristic properties of [[(infinity,1)-topos|infinity-topos]] in relation to WdL:

1. [[identity types]], characterized by their [[term introduction rule]] via the reflector $refl: (A = A)$, w

   This matches neatly with section 1, chapter 2 [&#167;863](#863), [&#167;903](#903).

1. [[object classifier]]=[[type of types]]=[[universe]]=self-relfecton

   This matches neatly with section 2 [&#167;1037](#1037), also [&#167;834](#834) etc.

1. [[locally Cartesian closed (∞,1)-category|local cartesian closure]],  equivalently incarnated in the [[base change]] [[adjoint triples]] whose associated [[monad]]/[[comonad]] [[adjoint pairs]] are nothing but the [[possibility]]$\dashv$[[necessity]]-[[adjunction]] as discussed at _[Possible worlds via homotopy type theory](necessity+and+possibility#InFirstOrderLogicAndTypeTheory)_

   This matches neatly with section 3 [&#167;1160](#1160).


In summary the formalization dictionary gives fairly accurately that in _Das Wegen_ Hegel speak about [[locally Cartesian closed (∞,1)-categories]] with [[object classifier]].

This is pretty close to being the proposed definition of _[[elementary (∞,1)-topos]]_, as in ([Shulman 12](elementary+infinity-topos#Shulman12)).


### Section 1.Das Wesen als Reflexion in ihm selbst. /  Essence as Reflection within Itself {#WesenAlsReflexionInIhmSelbst}

> {#817} &#167;817 Das Wesen ist erstens Reflexion. Die Reflexion bestimmt sich; ihre Bestimmungen sind ein Gesetztseyn, das zugleich Reflexion in sich ist; es sind

> zweitens diese Reflexions-Bestimmungen oder die Wesenheiten zu betrachten.

> Drittens macht sich das Wesen als die Reflexion des Bestimmens in sich selbst, zum Grunde, und geht in die Existenz und Erscheinung &#252;ber.


#### Chapter 1 Der Schein / Illusory Being
 
##### A Das Wesentliche und das Unwesentliche / The essential and the unessential


##### B Der Schein / Illusory being

##### C Die Reflexion / Reflection


> {#834} &#167;834 Das Wesen ist Reflexion;

> &#167;834 Essence is reflection

See discussion at _[Wesen als Reflexion in Ihm Selbst](#WesenAlsReflexionInIhmSelbst)_

(1) Die setzende Reflexion

(2) Die &#228;u&#223;ere Reflexion

Anmerkung

> {#850} &#167;850 Es ist aber hier nicht, weder von der Reflexion des Bewu&#223;tseyns, noch von der bestimmteren Reflexion des Verstandes, die das Besondere und Allgemeine zu ihren Bestimmungen hat, sondern von der Reflexion &#252;berhaupt die Rede. Jene Reflexion, der Kant das Aufsuchen des Allgemeinen zum gegebenen Besondern zuschreibt, ist, wie erhellt, gleichfalls nur die &#228;u&#223;ere Reflexion, die sich auf das Unmittelbare als auf ein gegebenes bezieht.

> Reflection is usually taken in a subjective sense as the movement of the faculty of judgement that goes beyond a given immediate conception and seeks universal determinations for it or compares such determinations with it. Kant opposes reflective judgement to determining judgement. He defines the faculty of judgement in general as the ability to think the particular as subsumed under the universal.

(3) Bestimmende Reflexion

> {#845} &#167;853 Die bestimmende Reflexion ist &#252;berhaupt die Einheit der setzenden und der &#228;u&#223;eren Reflexion. Die&#223; ist n&#228;her zu betrachten. Die &#228;u&#223;ere Reflexion f&#228;ngt vom unmittelbaren Seyn all, die setzende vom Nichts.

> &#167;853 Determining reflection is in general the unity of positing and external reflection. This is to be considered in more detail. 1. External reflection starts from immediate being, positing reflection from nothing.

#### Chapter 2. Die Wesenheiten oder die Reflexions-Bestimmungen / The Essentialities or Determination of Reflection

> {#860} &#167;860 Die Reflexion ist das Scheinen des Wesens in sich selbst. Das Wesen als unendliche R&#252;ckkehr in sich ist nicht unmittelbare, sondern negative Einfachheit; es ist eine Bewegung durch unterschiedene Momente, absolute Vermittelung mit sich. Aber es scheint in diese seine Momente; sie sind daher selbst in sich reflektirte Bestimmungen.

> &#167;860 Reflection is the showing of the illusory being of essence within essence itself. Essence, as infinite return-into-self, is not immediate but negative simplicity; it is a movement through distinct moments, absolute self-mediation. But it reflects itself into these its moments which consequently are themselves determinations reflected into themselves.

$$
  Type_1 \subset Type_2 \subset Type_3 \subset Type_4 \subset \cdots 
$$

See above at [&#167;816](#816)

##### $\;\;$ Remark $A = A$

> {#863} &#167;863 Thus the essential category of identity is enunciated in the proposition: everything is identical with itself, A = A.

The reflector(!) [[term constructor]] in an [[identity type]]. This is more explicit below at _[Identity](#Identity)_.

##### A Identity
 {#Identity}

> &#167;869 Essence is therefore simple identity with self.

> &#167;869 This identity-with-self is the immediacy of reflection.

Below this is called te _[First original law of thought](#FirstOriginalLawOfThought)_.

##### $\;\;$ Remark 1: Abstract identity

##### $\;\;$ Remark 2: First original law of thought
 {#FirstOriginalLawOfThought}

> {#875} &#167;875 In this remark, I will consider in more detail identity as the law of identity which is usually adduced as the first law of thought.

> This proposition in its positive expression $A = A$ is, in the first instance, nothing more than the expression of an empty tautology. 

The reflector [[term constructor]] in an [[identity type]].

##### B Difference

##### $\;\;$ (a) Absolute difference

##### $\;\;$ (b) Diversity

##### $\;\;$ Remark: The Law of Diversity
 {#LawOfDiversity}


> {#903} &#167;903 All things are different; or: there are no two things like each other.

Reminiscent of [[identity types]] in [[intensional type theory]].

##### C Contradiction



> Der aufgel&#246;ste Widerspruch ist also der Grund,

[[Aufhebung]] des Widerspruchs ist der Grund

$$
  \array{
    Grund &&\vdots && \vdots
    \\
    &&\vee && \vee
    \\
    &&\emptyset &\stackrel{Widersoruch}{\dashv}& \ast
    \\
    Wesen
  }
$$





#### Chapter 3. Der Grund

> {#964} &#167;964 Das Wesen bestimmt sich selbst als Grund.

> &#167;964 Essence determines itself as ground.

##### A. Der absolute Grund

###### a. Form und Wesen

###### b. Form und Materie

> {#978} &#167;978 Das Wesen wird zur Materie, indem seine Reflexion sich bestimmt, zu demselben als zu dem formlosen Unbestimmten sich zu verhalten. 

> &#167;978 Essence becomes matter in that its reflection is determined as relating itself to essence as to the formless indeterminate.

> {#981} &#167;981 2. Die Form bestimmt daher die Materie, und die Materie wird von der Form bestimmt.

> &#167;981 2. Hence form determines matter, and matter is determined by form.

###### c. Form und Inhalt.


##### B. Der bestimmte Grund

###### a. Der formelle Grund

###### b. Der reale Grund

###### c. Der vollstaendige Grund

##### C. Die Bedingung

###### a. Das relativ Unbedingte

> {#1021} &#167;1021 Der Grund ist das Unmittelbare und das Begr&#252;ndete das Vermittelte.

> &#167;1021 Ground is the immediate, and the grounded the mediated.

|  | Begriffslogik | [[natural deduction]] |
|  |---------------|-----------------------|
| unmittlebar | Grund         | [[antecedent]]        |
| vermittelt  | das Begr&#252;ndete | [[succedent]]/[[consequent]] |


###### b. Das absolute Unbedingte

###### c. Hervorgang der Sache in die Existenz

> {#1033} &#167;1033 Wenn alle Bedingungen einer Sache vorhanden sind, so tritt sie in die Existenz.

> &#167;1033 When all the conditions of a fact are present, it enters into Existence. 

This is [[term introduction]] via the [[natural deduction]] from the [[antecedent]] of the term introduction rule. More of this in [&#167;1035](#1035)

> {#1035} &#167;1035 Die Sache geht aus dem Grunde hervor. Sie wird nicht durch ihn so begr&#252;ndet oder gesetzt, da&#223; er noch unten bliebe, sondern das Setzen ist die Herausbewegung des Grundes zu sich selbst, und das einfache Verschwinden desselben. Er erh&#228;lt durch die Vereinigung mit den Bedingungen die &#228;u&#223;erliche Unmittelbarkeit und das Moment des Seyns.

> &#167;1035 The fact emerges from the ground. It is not grounded or posited by it in such a manner that ground remains as a substrate; on the contrary, the positing is the movement of the ground outwards to itself and its simple vanishing.

>  This immediacy that is mediated by ground and condition and is self-identical through the sublating of mediation, is Existence.

### Section 2. Die Erscheinung

> {#1036} &#167;1036 Das Wesen mu&#223; erscheinen.

> &#167;1036 Essence must appear

Notice that by [&#167;816](#816) this "appear" is short for "appear in itself". 

> {#1037} &#167;1037 So erscheint das Wesen. Die Reflexion ist das Scheinen des Wesens in ihm selbst.

> Thus appears essence . Reflection is the appearance of essence within itself.

This nicely explicitly re-iterates [&#167;816](#816). See the discussion there about translating this to "The ambient category appears reflected within itself".


### Section 3. Die Wirklichkeit
 {#DieWirklichkeit}

> {#1158} &#167;1158 Die Wirklichkeit ist die Einheit des Wesens und der Existenz;

> &#167;1158 Actuality is the unity of essence and Existence

> {#1159} &#167;1159 Diese Einheit des Innern und &#196;u&#223;ern ist die absolute Wirklichkeit. Diese Wirklichkeit aber ist zun&#228;chst das Absolute als solches;

> &#167;1159 This unity of inner and outer is absolute actuality. But this actuality is, in the first instance, the absolute as such &#8212; in so far as it is posited as a unity in which form has sublated itself and made itself into the empty or outer difference of an outer and inner.

> {#1160} &#167;1160 Zweitens die eigentliche Wirklichkeit.  Wirklichkeit, M&#246;glichkeit und Nothwendigkeit machen die formellen Momente des Absoluten, oder die Reflexion desselben aus.

> &#167;1160 Secondly, we have actuality proper. Actuality, possibility and necessity constitute the formal moments of the absolute, or its reflection.

This is a [[unity of opposites]]:

* The Absolute : [[possibility]] $\dashv$ [[necessity]]

Notice by [&#167;1159](#1159) that the Absolute is the absolute reality

* absolute reality : [[possibility]] $\dashv$ [[necessity]]

(beware that the [[possibility]] [[monad]] and [[necessity]] [[comonad]] are not in general [[idempotent monad|idempotent]]).

Also beware that by [&#167;1190](#1190), [&#167;1192](#1192) below there is also plain (not absolute) reality which goes along with possibility at the same level, so that maybe one should write something like

* absolute reality : reality/[[possibility]] $\dashv$ [[necessity]]


In any case, by the discussion at _[necessity and possibility -- As modality in dependent type theory](necessity+and+possibility#InFirstOrderLogicAndTypeTheory)_ the adjunction ([[possibility]] $\dashv$ [[necessity]]) characterizes [[locally cartesian closed category]]. So with the "Wesen" ("Essence") translating to the ambient category by [&#167;812](#812), the _absolute reality_ here translates to this ambient category being a [[locally Cartesian closed category]].
 

> {#1161} &#167;1161 Drittens die Einheit des Absoluten und seiner Reflexion ist das absolute Verh&#228;ltni&#223;, oder vielmehr das Absolute als Verh&#228;ltni&#223; zu sich selbst; Substanz.

> Thirdly, the unity of the absolute and its reflection is the absolute relation, or rather the absolute as relation to itself &#8212; substance.

So by [&#167;1159](#1159) "the absolute (absolute reality)" here translates to the locally Cartesian closed ambient category and by [&#167;816](#816) etc. the reflection here translates to the [[type of types]], so the above would then translate to 

* Substance = ambient locally Cartesian closed category equipped with type universe.



#### Chapter 1. Das Absolute

#### Chapter 2. Die Wirklichkeit {#DieWirklichkeitKapitel2}

> {#1190} &#167;1190 Die Wirklichkeit als selbst unmittelbare Formeinheit des Innern und &#196;u&#223;ern ist damit in der Bestimmung der Unmittelbarkeit gegen die Bestimmung der Reflexion in sich; oder sie ist eine Wirklichkeit gegen eine M&#246;glichkeit. Die Beziehung beider auf einander ist das Dritte, das Wirkliche bestimmt ebenso sehr als in sich reflektirtes Seyn, und dieses zugleich als unmittelbar existirendes. Dieses Dritte ist die Nothwendigkeit.

> &#167;1190 Actuality as itself the _immediate form_ &#8212; unity of inner and outer is thus in the determination of _immediacy_ over against the determination of reflection-into-self; or it is an _actuality as against a possibility_. Their _relation_ to each other is the _third_ term, the actual determined equally as a being reflected into itself, and this at the same time as a being existing immediately. This third term is _necessity_.


again: (Wirklichkeit-[[possibility]])-[[necessity]], see [&#167;1160](#1160) above.




##### A Zuf&#228;lligkeit oder formelle Wirklichkeit, M&#246;glichkeit und Nothwendigkeit/ Formal Actuality, Possibility and Necessity
 {#PossibilityAndNecessity}

> {#1192} &#167;1192 1. Die Wirklichikeit ist formell, insofern sie als erste Wirklichkeit nur unmittelbare, unreflektirte Wirklichkeit, somit nur in dieser Formbestimmung, aber nicht als Totalit&#228;t der Form ist. Sie ist so weiter nichts als ein Seyn oder Existenz &#252;berhaupt. Aber weil sie wesentlich nicht blo&#223;e unmittelbare Existenz, sondern, als Formeinheit des Ansichseyns oder der Innerlichkeit, und der &#196;u&#223;erlichkeit ist, so enth&#228;lt sie unmittelbar das Ansichseyn oder die M&#246;glichkeit. Was wirklich ist, ist m&#246;glich.

> &#167;1192 1. Actuality is formal in so far as, being primary actuality, it is only immediate, unreflected actuality, and hence is only in this form-determination but not as the totality of form. As such it is nothing more than a being or Existence in general. But because it is essentially not a mere immediate Existence but exists as form-unity of being-within-self or inwardness and outwardness, it immediately contains the in-itself or possibility. What is actual is possible.

again: Wirklichkeit $\rightarrow$ [[possibility]]


##### B. Relative Nothwendigkeit oder reale Wirklichkeit, M&#246;glichkeit und Nothwendigkeit / Relative Necessity, or Real Actuality, Possibility and Necessity


##### C. Absolute Nothwendigkeit / Absolute Necessity



#### Chapter 3. Das absolute Verh&#228;ltni&#223;


## **Book three** Die Lehre vom Begriff / The doctrine of the notion

### Section 1. Subjectivity.

### Section 2. Objectivity

### Section 3. The Idea
 {#TheIdea}

> {#1663} &#167;1636 The Idea being the unity of Notion and reality, being has attained the significance of truth;

Indeed, in [[categorical logic]]/[[type theory]], _[[true]]_ is given by the [[unit type]] $\ast$, which is exactly what was identified as formalizing _being_ above at [&#167;132](#132).


> {#1634} &#167;1634 But having reached the result that the Idea is the unity of the Notion and objectivity,

> {#1636} &#167;1636 Die Idee ist die Einheit des Bregiffs und der Realit&#228;t

> &#167;1636 The Idea being the unity of Notion and reality, 

> {#1638} &#167;1638 However, the Idea has not merely the more general meaning of the true being, of the unity of Notion and reality, but the more specific one of the unity of subjective Notion and objectivity.

So 

* Idee = Begriff & Realit&#228;t

See also [EL&#167;214](#EL214), which instead has

* Idee = das Ideelle & das Reelle .

But of course the the Notion is _ideell_, by [&#167;316](#316) "wie noch mehr der Begriff, die Idee, der Geist, Ideelles zu nennen ist".

## **Philosophy of nature**
 {#PhilosophyOfNature}

> {#PN192} PN&#167;192. Die Natur has sich als die Idee in der Form des Andersseins ergeben.

> PN&#167;192 Nature has come into being as the idea in the form of otherness".


## References


A good survey is in 

* [[Paul Redding]],  [section 3.2](http://plato.stanford.edu/entries/hegel/#SciLog) of _Georg Wilhelm Friedrich Hegel_, The Stanford Encyclopedia of Philosophy (Winter 2013 Edition), Edward N. Zalta (ed.) ([web](http://plato.stanford.edu/archives/win2013/entries/hegel/))

detailed background, introduction and survey includes

* {#Houlgate06} [[Stephen Houlgate]], _The opening of Hegel's Logic_, Purdue University Press, 2006 ([pdf](http://www.magonzalezvalerio.com/Houlgate,%20Stephen%20%20-%20The%20Opening%20of%20Hegel%27s%20Logic_From%20Being%20to%20Infinity%20-%20Purdue%20University%20Press.pdf))

* {#CarlsonMeasure} [[David Carlson]], _Hegel's theory of measure_ ([web](http://papers.ssrn.com/sol3/papers.cfm?abstract_id=413602))

* {#CarlsonActual} [[David Carlson]], _Hegel and what is actual_ ([pdf](http://www.hegel.net/carlson/Carlson2005-Hegel%20and%20What%20is%20Actual.pdf))


* [[Richard Dien Winfield]], _Lecture Course in Hegel's Science of Logic_ ([web](https://archive.org/details/LectureCourseInHegelsScienceOfLogic-RichardDienWinfield))

Hegel himself expands on the relation of the _Science of Logic_ to the [[Tao Te Ching]] in

* {#Hegel27} [[Georg Hegel]], Lectures on the Philosophy of Religion. Volume II: Determinate Religion. Edited by Peter C. Hodgson; translated by R.F. Brown, P.C. Hodgson, and J.M. Stewart, with the assistance of J.P. Fitzer and H.S. Harris. Berkeley: University of California Press, 1995 (orig. 1987). (Translation of: Vorlesungen &#252;ber die Philosophie der Religion.)  This extract (pp. 556-561) is from the Lectures of 1827; A. Immediate Religion, or Nature Religion; 1. The Religion of Magic; c. The State Religion of the Chinese Empire and the Dao. ([web](http://www.autodidactproject.org/quote/hegel-tao1.html))

Further comments on Hegel's text include

* {#Heidegger58} [[Martin Heidegger]], _Hegel and the Greeks_, Conference of the Academy of Sciences at Heidelberg, July 26, 1958 ([web](http://www.morec.com/hegelgre.htm))
  

* {#Inwood1983} Inwood, _Hegel_, 1983

* {#Lambek82} [[Joachim Lambek]], _The Influence of Heraclitus on Modern Mathematics_, In _Scientific Philosophy Today: Essays in Honor of Mario Bunge_, edited by Joseph Agassi and Robert S Cohen, 111&#8211;21. Boston: D. Reidel Publishing Co.

Comments on the general aim of a fundamental logic based on [[dialectic]] are in

* {#Wandschneider99} [[Dieter Wandschneider]], _Dialektik als Letztbegr&#252;ndung der Logik_, in Koreanische Hegelgesellschaft (ed.), _Festschrift f&#252;r Sok-Zin Lim_ Seoul 1999, 255&#8211;278 ([pdf](http://www.philosophie.rwth-aachen.de/global/show_document.asp?id=aaaaaaaaaabpltw))

Related discussion in view of [[infinitesimals]] is in

* {#Cohen83} [[Hermann Cohen]], _Das Prinzip der Infinitesimal-Methode und seine Geschichte_ , Berlin 1883. ([html](http://www.gleichsatz.de/b-u-t/archiv/Cohen/hc-infinit1.html))


Proposals for formalizing some of Hegel's thoughts in [[categorical logic]] have been put forward by [[William Lawvere]] in several places, for instance in

* {#LawvereComo} [[William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_, 1991
 

* [[William Lawvere]], _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_
  {#LawvereLauterEinsen}

* [[William Lawvere]] _[[Toposes of laws of motion]]_ , transcript of a talk in Montreal, Sept. 1997 ([pdf](http://www.acsu.buffalo.edu/~wlawvere/ToposMotion.pdf))
 {#LawvereMotion}

Related commentary is in 

* [[Andrei Rodin]], section 4.8 of _Axiomatic Method and Category Theory_ ([arXiv:1210.1478](http://arxiv.org/abs/1210.1478))

Discussion of formalization of the topics of the "subjective logic" within [[type theory]] include

* {#MartinLoef96} [[Per Martin-Löf]], _On the Meanings of the Logical Constants and the Justifications of the Logical Laws_, Nordic Journal of Philosophical Logic, 1(1): 11&#8211;60, 1996, ([pdf](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf))

which gives a detailed discussion of the term [[judgement]] as used  in the history  [[philosophy]] and then in [[type theory]].

The formalization of _Schluss_ by [[natural deduction]] originates in

* {#Gentzen35} [[Gerhard Gentzen]], _Untersuchungen &#252;ber das logische Schlie&#223;en_, _Mathematische Zeitschrift_ 39(1), Springer-Verlag 1935. &lt;http://dx.doi.org/10.1007/BF01201353> (English translation _Investigations into Logical Deduction_ in Szabo)  

The idea that the [[types]] in [[type theory]] are (mathematical) _concepts_/_notions_ (i.e. "Begriffe", as in the [formalization dictionary](#Dictionary) above ) is arguably implicit in the original 

* {#MartinLoef73} [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, In Logic Colloquium (1973), ed. H. E. Rose and J. C. Shepherdson (North-Holland, 1974), 73-118. ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926))

where it says in section 1.1:

> Every mathematical object is of a certain type [...] a type is well defined if we understand (or _grasp_ to use a word favoured by Kreisel 1970) what it means to be an object of that type.

The explicit statement "a type is a concept"  appears for instance (referring both to types of mathematical objects as well as to [[data types]] in [[computer science]]) in:

* {#Sale77} [[Arhtur Sale]], _Primitive data types_, The Australian Computer Journal, Vol. 9, No. 2, July 1977 ([pdf](http://eprints.utas.edu.au/139/1/PrimitiveData.pdf))

The explicit statement "a type is a 'mathematical' concept" appears on p. 6 of

* {#Sergeraert94} [[Francis Sergeraert]], _The computability problem in algebraic topology_, Advances in mathematics 104, 1-29, 1994 [pdf](http://www-fourier.ujf-grenoble.fr/~sergerar/Papers/Advances.pdf)

An explicit suggestion that "[[type]]" in [[homotopy type theory]] should be read as a "concept"  is in

* {#LadymanPresnel14} [[James Ladyman]], [[Stuart Presnell]], _Does Homotopy Type Theory Provide a Foundation for Mathematics?_, 2014 ([web](http://philsci-archive.pitt.edu/11143/))