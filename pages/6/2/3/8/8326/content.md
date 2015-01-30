
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
 [German hyperlinked version](http://hegel.logik.2.abcphil.de), [German html raw text version](http://www.gutenberg.org/cache/epub/6729/pg6729.html), [full text pdf-s](http://hegel.net/hegelwerke/), [Wikipedia entry](http://en.wikipedia.org/wiki/Science_of_Logic))

The English translation is by A. V. Miller in 1969. More recently George di Giovanni has published a new translation, Cambridge University Press, 2010.

Note that Hegel included an abbreviated version of _The Science of Logic_ as the first part of _The Encyclopedia of the Philosophical Sciences_, followed there by _[The Philosophy of Nature](#PhilosophyOfNature)_ and _[The Philosophy of Spirit](#PhilosophyOfSpirit)_. This first part is often referred to as the _Shorter Logic_. Similarly the _[The Philosophy of Spirit](#PhilosophyOfSpirit)_ subsumes, in condensed outline, the main parts of the _Phenomenology of the Spirit_.

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





## Formalization of the process

Hegel famously invokes a process or movement of opposing moments that via their synthesis lead to new phenomena, which then may again participte as opposing moments in a further synthesis. Accordingly the whole text is structured by triads of chapters each with triads of sections, etc. see [Inwood 83, p. 263](#Inwood1983) for a diagram.

Hegel wrote (according to [this](http://en.wikipedia.org/wiki/Georg_Wilhelm_Friedrich_Hegel#Heraclitus)):

"[[Heraclitus]] is the one who first declared the nature of the infinite and first grasped nature as in itself infinite, that is, its essence as process. The origin of [[philosophy]] is to be dated from Heraclitus. His is the persistent Idea that is the same in all philosophers up to the present day, as it was the Idea of Plato and Aristotle."

"... there is no proposition of Heraclitus which I have not adopted in my logic."


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
we have, as discussed at _[[differential cohomology hexagon]]_, that the dualities generate for each type a hexagonal web of which the above unifying tripl is the bottom stage.

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

This appears below in two stages, first in the Seinslogik at around [&#167;714](#714), and then ("reflected") in the Wesenslogik around [&#167;989](#989).

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
| [[Dasein]]   | [Aufhebung of becoming via sharp modality](Aufhebung#ExamplesBecomingFormalization) $\left(\array{\flat &\dashv&\sharp \\ \vee && \vee \\ \emptyset &\dashv& \ast}\right)$ | [&#167;182](#182),  [&#167;183](#183), [&#167;187](#187), [&#167;191](#191), [&#167;194](#194) |
| moment of repulsion | [[flat modality]] $\flat$ | [&#167;342](#342), [[Cohesive Toposes and Cantor's "lauter Einsen"|Law94]] |
| moment of attraction | [[cohesion]], [[shape modality]] $&#643;$ | [&#167;395](#395) |
| quality | [[adjoint modality]] (attraction $\dashv$ repulsion) = ($&#643; \dashv \flat$) |  [&#167;342](#342) |
| $\to$ Etwas  |   |  [&#167;1056](#1056)  |
| moment of discreteness | [[flat modality]] $\flat$ |  |
| moment of continuity | [[sharp modality]] $\sharp$ |  |
| quantity | [[adjoint modality]] (discreteness $\dashv$ continuity)  = ($\flat \dashv \sharp$) | [&#167;398](#398), [[Cohesive Toposes and Cantor's "lauter Einsen"|Law94]] |
| measure (= [[gauge]]), unity of quantity and quality | [[cohesion]] [[adjoint triple]] [[adjoint modality]] $\left(\array{ attraction &\stackrel{quality}{\dashv}& repulsion \\ \bot && \bot \\ discreteness &\stackrel{quantity}{\dashv}& continuity } \right) = \left(\array{ &#643; &\dashv& \flat \\ \bot && \bot \\ \flat &\dashv& \sharp }\right) $ | [&#167;699](#699), [&#167;708](#708), [&#167;714](#714), [&#167;725](#725) |
| vanishing of infinitesimals | [[reduction modality]] $\Re$ | [&#167;174](#174), [&#167;404](#304)   |
| being-for-one | [[infinitesimal flat modality]] $\Im$ | [&#167;322](#322) |
| being-for-self | [[infinitesimal shape modality]] $\& $ | [&#167;305](#305) |
| ideality (inf. quality) | [[unity of opposites]] ($ \& \dashv \Im$ ) | [&#167;305](#305), [&#167;322](#322)   |
| Aufhebung of finiteness | $\left(\array{\& &\dashv& \Im \\ \vee && \vee \\ &#643; &\dashv& \flat }\right)$ | [&#167;304](#304) , [&#167;305](#305) |
| reality | [[adjoint modality]] ($\Re \dashv  \&$) | [&#167;304](#304) , [&#167;305](#305) |
| idea, unity of ideality and reality | [[differential cohesion]] [[adjoint triple]] [[adjoint modality]] $\left( \array{ \Re &\dashv& \& \\ \bot&\stackrel{idea}{}& \bot && \\  \& &\dashv&  \Im} \right)$ | [&#167;304](#304), [&#167;324](#324), [EL&#167;214](#EL214), [&#167;1636](#1636) |
| absolute indifference  | [[adjoint modality]] ($id \dashv id$) | [&#167;803](#803), [&#167;808](#808), [&#167;812](#812) |
| **Wesenslogik** | **[[homotopy type theory]]** |   |
| Wesen, essence | the ambient [[category]]  | [&#167;803](#803), [&#167;812](#812)  |
| possibility | [possibility monad](necessity+and+possibility#InFirstOrderLogicAndTypeTheory) $\lozenge$ = [[dependent sum]] followed by [[context extension]] |  |
| necessity | [necessity comonad](necessity+and+possibility#InFirstOrderLogicAndTypeTheory) $\Box$ = [[dependent product]] followed by [[context extension]] |  |
| absolute actuality/Wirklichkeit, unity of [[possibility]] and [[necessity]] | [[adjoint pair]] of (co-)[[monads]] $(\lozenge \dashv \Box)$, hence [[locally cartesian closed category|local cartesian closure]] | [&#167;1160](#1160) (with [&#167;1159](#1159)), [&#167;1190](#1190), [&#167;1192](#1192) |
| essence appears as reflected in itself | [[object classifier]] = [[type of types]] = [[universe]] $Type$ | [&#167;816](#816), [&#167;834](#834), [&#167;850](#850), [&#167;1037](#1037) |
| essence as infinite return-into-self | [[universe enlargement|cumulative hierarchy]] of universe levels $Type_1 \lt Type_2 \lt Type_3 \lt \cdots $ | [&#167;860](#860) |
| everything is identical with itself | [[term introduction]] for [[identity types]] | [&#167;863](#863), [&#167;875](#875) |
| all things are different | [[intensional identity]] | [&#167;903](#903) |
| absoluter Widerspruch / absolute contradiction  |  [[adjoint modality]] ([[false]] $\dashv$ [[true]]) = ($\emptyset \dashv \ast$) | [&#167;931](#931)  [&#167;934](#934) |
| Aufhebung des Widerspruchs | [Aufhebung of absolute contradiction via sharp modality](Aufhebung#ExamplesBecomingFormalization) $\left(\array{\flat &\dashv& \sharp \\ \vee && \vee \\ \emptyset &\dashv& \ast}\right)$ | [&#167;943](#943), [&#167;944](#944), [&#167;945](#945) |
| abs. Grund | [[base topos]] of [[sharp modality|sharp]]-[[modal types]] | [&#167;945](#945) |
| Form | [[shape modality]] $&#643;$ | [&#167;973](#973) | 
| Inhalt | [[flat modality]] $\flat$ | [&#167;989](#989) | 
| Matter/([[gauge]]-)Fields | $(&#643; \dashv \flat)$ | [&#167;989](#989), [&#167;1068](#1068)  |
| $\to$ Ding |   |  [&#167;1048](#1048)  |
| **Natur**      | [[model]] (representation) of the above [[modal type theory]] | [PN&#167;192](#PN192) [#PN193b](PN&#167;193b) |

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
    Geist &&  && && 
    \\
    \\
    && &&  &&  && \rho(id) & \dashv & \rho(id)
    \\ 
    && &&  &&  && \vee & & \vee
    \\ 
    && &&  &&  && \rho(\Re) & & \rho(\&)
    \\ 
    && &&  &&  && \bot & Raum & \bot
    \\ 
    && &&  &&  && \rho(\&) &\dashv & \rho(\Im)
    \\ 
    && &&  &&  && \vee && \vee
    \\
    Natur &&   &&  && 
    & & \rho(&#643;) &\dashv& \rho(\flat) &
    \\
    && && && && \bot && \bot
    \\
    && && &&  && \rho(\flat) &\dashv& \rho(\sharp) & 
    \\
    && && &&&& \vee && \vee 
    \\
    && &&&&\stackrel{}{}&& \rho(\emptyset) &\dashv& \rho(\ast) & 
    \\
    \\
    {Subjektive \atop Logik}{}&&\stackrel{Begriffe}{}
    \\
    \\
    \\
    && && &&  && \vdots && \vdots
    \\
    && && && 
    \stackrel{Existenz}{}
    &\stackrel{Form}{} & &#643; 
    &\stackrel{Ding}{\stackrel{Materie/Eichfelder}{\dashv}}& \flat &
     \stackrel{Inhalt}{}
    \\
    && && && && \bot && \bot
    \\
    && && &&  && \flat &\dashv& \sharp & \stackrel{abs.\,Grund}{}
    \\
    && && &&&& \vee &\stackrel{Aufhebung \atop {des\;Widerspruchs}}{}& \vee 
    \\
    && &&&&\stackrel{}{}&\stackrel{falsch}{}& \emptyset &\stackrel{abs.\,Widerspruch}{\dashv}& \ast & \stackrel{wahr}{}
    \\
    \\
    && && \stackrel{Wesen}{} && &\stackrel{Moeglichkeit}{}& \lozenge &\stackrel{abs. Wirklichkeit}{\dashv}& \Box & \stackrel{Notwendigkeit}{}
    \\
    &&\stackrel{best.\; Reflexionen}{}&& &&  &\stackrel{setzende \atop Reflexion}{} &  &\stackrel{\stackrel{\stackrel{\vdots}{Type_2}}{Type_1}}{Type_0}&  & \stackrel{auessere \atop Reflexion}{} 
    \\
    \\
    && && &&\stackrel{An\& Fuersichsein}{}&& id &\stackrel{}{\dashv}& id
    \\
    {Objektive \atop Logik}{} && && &&&& \vee &\stackrel{{Aufhebung \atop {der\;Differenzen}}}{}& \vee 
    \\
    && && &&& \stackrel{{Verschwinden\;der}\atop Infinitesimalen}{}& \Re &\stackrel{Realitaet}{\dashv}& \&
    \\
    && && \stackrel{Unendlichkeit}{} &&&& \bot &\stackrel{Idee}{}& \bot 
    \\
    && && &&\stackrel{Fuersichsein}{} && \& 
    &\stackrel{Idealitaet /}{\stackrel{inf.\,Qualitaet}{\dashv}}& \Im &&\stackrel{Fuer-eines-sein}{}
    \\
    && \stackrel{Die\;Kategorien}{}&& &&&& \vee &\stackrel{{Aufhebung \atop {der\;Endlichkeit}}}{}& \vee 
    \\
    && && &&\stackrel{Ansichsein}{}&\stackrel{Attraktion}{}& 
    &#643; 
    &\stackrel{Etwas}{\stackrel{Qualitaet}{\dashv}}& 
   \flat & \stackrel{Repulsion}{} & 
    \stackrel{Sein-fuer-Anderes}{}
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



## **Introduction**

### Allgemeiner Begriff der Logik


> {#53} &#167;53 Die reine Wissenschaft setzt somit die Befreiung von dem Gegensatze des Bewu&#223;tseyns voraus. Sie enth&#228;lt den Gedanken, insofern er eben so sehr die Sache an sich selbst ist, oder die Sache an sich selbst, insofern sie ebenso sehr der reine Gedanke ist. Als Wissenschaft ist die Wahrheit das reine sich entwicklende Selbstbewu&#223;tseyn, und hat die Gestalt des Selbst, da&#223; das an und f&#252;r sich seyende gewu&#223;ter Begriff, der Begriff als solcher aber das an und f&#252;r sich seyende ist. Dieses objektive Denken ist denn der Inhalt der reinen Wissenschaft. Sie ist daher so wenig formell, sie entbehrt so wenig der Materie zu einer wirklichen und wahren Erkenntni&#223;, da&#223; ihr Inhalt vielmehr allein das absolute Wahre, oder wenn man sich noch des Worts Materie bedienen wollte, die wahrhafte Materie ist,&#8212;eine Materie aber, der die Form nicht ein &#196;u&#223;erliches ist, da diese Materie vielmehr der reine Gedanke, somit die absolute Form selbst ist. Die Logik ist sonach als das System der reinen Vernunft, als das Reich des reinen Gedankens zu fassen. Dieses Reich ist die Wahrheit, wie sie ohne H&#252;lle an und f&#252;r sich selbst ist. Man kann sich deswegen ausdr&#252;cken, da&#223; dieser Inhalt die Darstellung Gottes ist, wie er in seinem ewigen Wesen vor der Erschaffung der Natur und des endlichen Geistes ist.

> &#167;53 Accordingly, logic is to be understood as the system of pure reason, as the realm of pure thought. This realm is truth as it is without veil and in its own absolute nature. It can therefore be said that this content is the exposition of God as he is in his eternal essence before the creation of nature and a finite mind.

To wit, the _Logic_ ends with the appearance of _the idea_ in [&#167;1636](#1636) and then nature appears from that in [PN&#167;192](#PN192) "as the idea in the form of otherness".

> {#54} &#167;54 Anaxagoras wird als derjenige gepriesen, der zuerst den Gedanken ausgesprochen habe, da&#223; der Nus, der Gedanke, das Princip der Welt, da&#223; das Wesen der Welt als der Gedanke bestimmt ist. Er hat damit den Grund zu einer Intellektualansicht des Universums gelegt, deren reine Gestalt die Logik seyn mu&#223;. Es ist in ihr nicht um ein Denken &#252;ber etwas, das f&#252;r sich au&#223;er dem Denken zu Grunde l&#228;ge, zu thun, um Formen, welche blo&#223;e Merkmale der Wahrheit abgeben sollten; sondern die nothwendigen Formen und eigenen Bestimmungen des Denkens sind der Inhalt und die h&#246;chste Wahrheit selbst.

> &#167;54 Anaxagoras is praised as the man who first declared that Nous, thought, is the principle of the world, that the essence of the world is to be defined as thought. In so doing he laid the foundation for an intellectual view of the universe, the pure form of which must be logic. What we are dealing with in logic is not a thinking about something which exists independently as a base for our thinking and apart from it, nor forms which are supposed to provide mere signs or distinguishing marks of truth; on the contrary, the necessary forms and self-consciousness of thought are the content and the ultimate truth itself.


### Allgemeine Einteilung der Logik

> {#85} &#167;85 Die objektive Logik tritt damit vielmehr an die Stelle der vormaligen Metaphysik, als welche das wissenschaftliche Geb&#228;ude &#252;ber die Welt war, das nur durch Gedanken aufgef&#252;hrt seyn sollte.&#8212;Wenn wir auf die letzte Gestalt der Ausbildung dieser Wissenschaft R&#252;cksicht nehmen, so ist erstens unmittelbar die Ontologie, an deren Stelle die objektive Logik tritt,&#8212;der Theil jener Metaphysik, der die Natur des Ens &#252;berhaupt erforschen sollte;&#8212;das Ens begreift sowohl Seyn als Wesen in sich, f&#252;r welchen Unterschied unsere Sprache gl&#252;cklicherweise den verschiedenen Ausdruck gerettet hat.&#8212;Alsdann aber begreift die objektive Logik auch die &#252;brige Metaphysik insofern in sich, als diese mit den reinen Denkformen die besondern, zun&#228;chst aus der Vorstellung genommenen Substrate, die Seele, die Welt, Gott, zu fassen suchte, und die Bestimmungen des Denkens das Wesentliche der Betrachtungsweise ausmachten. 



> &#167;85 The objective logic, then, takes the place rather of the former metaphysics which was intended to be the scientific construction of the world in terms of thoughts alone. If we have regard to the final shape of this science, then it is first and immediately ontology whose place is taken by objective logic &#8212; that part of this metaphysics which was supposed to investigate the nature of ens in general; ens comprises both being and essence, a distinction for which the German language has fortunately preserved different terms. But further, objective logic also comprises the rest of metaphysics in so far as this attempted to comprehend with the forms of pure thought particular substrata taken primarily from figurate conception, namely the soul, the world and God; and the determinations of thought constituted what was essential in the mode of consideration. 


## **Die Lehre vom Sein** / **The Doctrine of Being**


### $\;\;$ Womit muss der Anfang der Wissenschaft gemacht werden?


> {#121} &#167;121 Was somit &#252;ber das Seyn ausgesprochen oder enthalten seyn soll, in den reicheren Formen des Vorstellens von Absolutem oder Gott, die&#223; ist im Anfange nur leeres Wort, und nur Seyn; die&#223; Einfache, das sonst keine weitere Bedeutung hat, die&#223; Leere ist also schlechthin der Anfang der Philosophie.

> &#167;121 Consequently, whatever is intended to be expressed or implied beyond being, in the richer forms of representing the absolute or God, this is in the beginning only an empty word and only being; this simple determination which has no other meaning of any kind, this emptiness, is therefore simply as such the beginning of philosophy.

> &#167;122 Diese Einsicht ist selbst so einfach, da&#223; dieser Anfang als solcher, keiner Vorbereitung noch weiteren Einleitung bedarf; und diese Vorl&#228;ufigkeit von Raisonnement &#252;ber ihn konnte nicht die Absicht haben, ihn herbeizuf&#252;hren, als vielmehr alle Vorl&#228;ufigkeit zu entfernen.

> &#167;122 This insight is itself so simple that this beginning as such requires no preparation or further introduction; and, indeed, these preliminary, external reflections about it were not so much intended to lead up to it as rather to eliminate all preliminaries.



### $\;\;$ Allgemeine Einteilung des Seins


### First section. Bestimmtheit (Qualit&#228;t) / Determinateness (Quality)

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


##### C. Werden / Becoming
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

which points to the [[Aufhebung]] of this duality via the [[sharp modality]].

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





###### 3. Aufheben des Werdens / Sublating of Becoming
 {#AufhebenDesWerdens}

> {#180} &#167;180 Das Gleichgewicht, worein sich Entstehen und Vergehen setzen, ist zun&#228;chst das Werden selbst. Aber dieses geht eben so in ruhige Einheit zusammen. Seyn und Nichts sind in ihm nur als verschwindende; aber das Werden als solches ist nur durch die Unterschiedenheit derselben. Ihr Verschwinden ist daher das Verschwinden des Werdens, oder Verschwinden des Verschwindens selbst. Das Werden ist eine haltungslose Unruhe, die in ein ruhiges Resultat zusammensinkt.

> &#167;180 The resultant equilibrium of coming-to-be and ceasing-to-be is in the first place becoming itself. But this equally settles into a stable unity. Being and nothing are in this unity only as vanishing moments; yet becoming as such is only through their distinguishedness. Their vanishing, therefore, is the vanishing of becoming or the vanishing of the vanishing itself. Becoming is an unstable unrest which settles into a stable result.

> {#181} &#167;181 Die&#223; k&#246;nnte auch so ausgedr&#252;ckt werden: Das Werden ist das Verschwinden von Seyn in Nichts, und von Nichts in Seyn, und das Verschwinden von Seyn und Nichts &#252;berhaupt; aber es beruht zugleich auf dem Unterschiede derselben. Es widerspricht sich also in sich selbst, weil es solches in sich vereint, das sich entgegengesetzt ist; eine solche Vereinigung aber zerst&#246;rt sich.

> &#167;181 This could also be expressed thus: becoming is the vanishing of being in nothing and of nothing in being and the vanishing of being and nothing generally; but at the same time it rests on the distinction between them. It is therefore inherently self-contradictory, because the determinations it unites within itself are opposed to each other; but such a union destroys itself.

> {#182} &#167;182 Die&#223; Resultat ist das Verschwundenseyn, aber nicht als Nichts; so w&#228;re es nur ein R&#252;ckfall in die eine der schon aufgehobenen Bestimmungen, nicht Resultat des Nichts und des Seyns. Es ist die zur ruhigen Einfachheit gewordene Einheit des Seyns und Nichts. Die ruhige Einfachheit aber ist Seyn, jedoch ebenso, nicht mehr f&#252;r sich, sondern als Bestimmung des Ganzen.

> &#167;182 This result is the vanishedness of becoming, but it is not nothing; as such it would only be a relapse into one of the already sublated determinations, not the resultant of nothing and being. It is the unity of being and nothing which has settled into a stable oneness. But this stable oneness is being, yet no longer as a determination on its own but as a determination of the whole.

> {#183} &#167;183 Das Werden so &#220;bergehen in die Einheit des Seyns und Nichts, welche als seyend ist, oder die Gestalt der einseitigen unmittelbaren Einheit dieser Momente hat, ist das Daseyn.

> &#167;183 Becoming, as this transition into the unity of being and nothing, a unity which is in the form of being or has the form of the onesided immediate unity of these moments, is determinate being.

By the discussion around [&#167;177](#177) the [[unity of opposites]] of [[nothing]] and [[being]] is to be expressed by the [[adjunction]]

$$
  \emptyset \dashv \ast
$$

between the [[modalities]] which are constant on the [[empty type]]/[[initial object]] and on the [[unit type]]/[[terminal object]], respectively.

To exhibit [[Aufhebung]] of this duality we are now to produce another such [[adjunction]] of the form $(\flat \dashv \sharp)$ which characterizes a higher [[level of a topos]], and such that both $\emptyset$ and $\ast$ are $\sharp$-[[modal types]]. 

This is the case for $\flat$ the [[flat modality]] and $\sharp$ the [[sharp modality]] over a [[cohesive site]], this is discussed at _[Aufhebung -- over cohesive sites](Aufhebung#ExamplesBecomingFormalization)_.

So the first step to further determination in the [Proce&#223;](#Process) is this:

$$
  \array{
    && && &&\stackrel{Dasein}{}&& \flat &\stackrel{}{\dashv}& \sharp & 
    \\
    && && &&&& \vee &\stackrel{Aufhebung \atop {des\;Werdens}}{}& \vee 
    \\
    && &&&&\stackrel{reines\;Sein}{}&\stackrel{Nichts}{}& \emptyset &\stackrel{Werden}{\dashv}& \ast & \stackrel{Sein}{}
 }
$$


| |  | [[Dasein]] | |  |
|--|--|--|--|--|
| [[Werden]] : | [[Nichts]] | $\;\;\;\dashv$ | [[Sein]] | : [[Vergehen]] |

$\,$

| |  | [[Dasein]] | |  |
|--|--|--|--|--|
| [[becoming]] : | [[nothing]] | $\;\;\;\dashv$ | [[being]] | : [[ceasing]] |


> {#187} &#167;187 Der n&#228;here Sinn und Ausdruck, den Seyn und Nichts, indem sie nunmehr Momente sind, erhalten, hat sich bei der Betrachtung des Daseyns, als der Einheit, in der sie aufbewahrt sind, zu ergeben. Seyn ist Seyn, und Nichts ist Nichts nur in ihrer Unterschiedenheit von einander; in ihrer Wahrheit aber, in ihrer Einheit, sind sie als diese Bestimmungen verschwunden, und sind nun etwas anderes. Seyn und Nichts sind dasselbe; darum weil sie dasselbe sind, sind sie nicht mehr Seyn und Nichts, und haben eine verschiedene Bestimmung; im Werden waren sie Entstehen und Vergehen; im Daseyn als einer anders bestimmten Einheit sind sie wieder anders bestimmte Momente. Diese Einheit bleibt nun ihre Grundlage, aus der sie nicht mehr zur abstrakten Bedeutung von Seyn und Nichts heraustreten.

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


> {#209} &#167;209 Die&#223; Aufgehobenseyn des Unterschieds ist die eigne Bestimmtheit des Daseyns; so ist es Insichseyn; das Daseyn ist Daseyendes, Etwas.

>  &#167;209 This sublating of the distinction is more than a mere taking back and external omission of it again, or than a simple return to the simple beginning, to determinate being as such. The distinction cannot be omitted, for it is. What is, therefore, in fact present is determinate being in general, distinction in it, and sublation of this distinction; determinate being, not as devoid of distinction as at first, but as again equal to itself through sublation of the distinction, the simple oneness of determinate being resulting from this sublation. This sublatedness of the distinction is determinate being's own determinateness; it is thus being-within-self: determinate being is a determinate being, a something.


> {#210} &#167;210 Something is the first negation of negation, as simple self-relation in the form of being.

> {#211} &#167;211 Something is the negation of the negation in the form of being;

> {#212} &#167;212 This mediation with itself which something is in itself, taken only as negation of the negation, has no concrete determinations for its sides; it thus collapses into the simple oneness which is being.


Here "double negation" is plausibly matched with the [[double negation modality]].

Concerning "something": if $X$ is a [[type]], then by [[propositions-as-types]] there is _something_ of this type if the type is [[inhabited]]. But [[classical logic|classically]] this is expressed by by its [[double negation modality]]. Hence: there is something of some quality/type if that is a double-negation [[modal type]].



##### B. Die Endlichkeit / Finitude.

###### a. Etwas und ein Anderes. / Something and an Other
 {#SomethingAndAnOther}

> {#221} &#167;221 Seyn-f&#252;r-Anderes und Ansichseyn machen die zwei Momente des Etwas aus.

> &#167;221  Being-for-other and being-in-itself constitute the two moments of the something.


Hence a [[unity of opposites]]:

$$
  \array{
    Ansichsein &\stackrel{Etwas}{\dashv}& Sein-fuer-Anderes
  }
  \,.
$$

This will repeat in the Wesenslogik with _Etwas_ replaced by _Ding_,
see [&#167;1048](#1048). 

|  | moment  |  unity   | comoment |
|--|---|-----|--| 
| **Seinslogik** | Ansichseyn | Etwas | Sein-fuer-Anderes |
| **Wesenslogik**  | Existenz   | Ding |   |


Notice that there in the discussion of _Ding_ is a comment hidden that concerns the _Etwas_ here:

> [&#167;1056](#1056) Die Qualit&#228;t ist die unmittelbare Bestimmtheit des Etwas; das Negative selbst, wodurch das Seyn Etwas ist.

> &#167;1056 Quality is the immediate determinateness of something, the negative itself through which being is something. 

This says that the the "immediate determinateness" of the adjunction in [&#167;221](#221)
is the adjunction [[shape modality]]$\dashv$[[flat modality]] that we identify with _quality_. We display this in the _[Process](#Process)_.


> &#167;222 Being and nothing in their unity, which is determinate being

This is the [[Aufhebung]] discussed around [&#167;182](#182), [&#167;183](#183)

> Die&#223; f&#252;hrt zu einer weitern Bestimmung. Ansichseyn und Seyn-f&#252;r-Anderes sind zun&#228;chst verschieden; aber da&#223; Etwas dasselbe, was es an sich ist, auch an ihm hat, und umgekehrt, was es als Seyn-f&#252;r-Anderes ist, auch an sich ist,&#8212;die&#223; ist die Identit&#228;t des Ansichseyns und Seyns-f&#252;r-Anderes, nach der Bestimmung, da&#223; das Etwas selbst ein und dasselbe beider Momente ist, sie also ungetrennt in ihm sind.&#8212;Es ergiebt sich formell diese Identit&#228;t schon in der Sph&#228;re des Daseyns, aber ausdr&#252;cklicher in der Betrachtung des Wesens und dann des Verh&#228;ltnisses der Innerlichkeit und &#196;u&#223;erlichkeit, und am bestimmtesten in der Betrachtung der Idee, als der Einheit des Begriffs und der Wirklichkeit.

For the last one, see below [&#167;1636](#1636).



##### C. Die Unendlichkeit


###### a. Das Unendliche &#220;berhaupt

###### b. Wechselwirkung des Endlichen und Unendlichen

###### c. Die affirmative Unendlichkeit




> {#304} &#167;304 In Beziehung auf Realit&#228;t und Idealit&#228;t wird aber der Gegensatz des Endlichen und Unendlichen so gefa&#223;t, da&#223; das Endliche f&#252;r das Reale gilt, das Unendliche aber f&#252;r das Ideelle gilt; wie auch weiterhin der Begriff als ein Ideelles und zwar als ein nur Ideelles, das Daseyn &#252;berhaupt dagegen als das Reale betrachtet wird.

> With reference to reality and ideality, however, the opposition of finite and infinite is grasped in such a manner that the finite ranks as the real but the infinite as the 'ideal' [das Ideelle]; in the same way that further on the Notion, too, is regarded as an 'ideal', that is, as a mere 'ideal', in contrast to determinate being as such which is regarded as the real.

Notice here from _[Der quantitative unendliche Progress](#DerQuantitativeUnendlicheProgress)_ that "infinite" refers much to the _infinite progression_ that in mathematics is referred to as _[[sequences]]_ and _[[series]]_, and that what "ideal" ( _ideell_ ) about them is that they need not converge to any finite value, but be regarded as sequences --- such as [[formal power series]]. 
Hence if we take the "infinite" and the "infinitesimal" to go together -- as also in [&#167;502](#502) -- then [&#167;304](#304) gives that  "the [[infinitesimal]] ranks as the ideal", whereas "the [[reduced object|reduced]] ranks as the real". See also the discussion below [&#167;305](#305).

This way we may think of the "ideal" here as related to the idealization involved in the concept of [[infinitesimals]], which are "not real" in an evident sense and of the "real" hence of the _finite_, the non-infinitesimal. 

Now the [[reduction modality]] $\Re$ is the operation that makes all infinitesimal vanish, i.e. it expresses precisely the "vanishing of infinitesimals" in [&#167;174](#174). Hence its [[modal types]] are precisely those without infinitesimal extension. It is perfectly plausible to think of these as the _real types_.

Moreover, the $\Re$-[[anti-modal types]] are indeed precisely those that consist entirely only of [[infinitesimals]] (the [[infinitesimally thickened points]]), hence those which are "ideel" but not "real" in the sense of [&#167;304](#304).

We discuss below [&#167;305](#305) the [[adjunction]] that $\Re$-participates in and the [[unity of opposites]] that this may be thought to express.

###### Der &#220;bergang

> {#305} &#167;305 Die Idealit&#228;t kann die Qualit&#228;t der Unendlichkeit genannt werden; aber sie ist wesentlich der Proce&#223; des Werdens und damit ein &#220;bergang, wie des Werdens in Daseyn, der nun anzugeben ist. Als [[Aufhebung|Aufheben]] der Endlichkeit, d. i. der Endlichkeit als solcher und ebenso sehr der ihr nur gegen&#252;berstehenden, nur negativen Unendlichkeit ist diese R&#252;ckkehr in sich, Beziehung auf sich selbst, Seyn. Da in diesem Seyn Negation ist, ist es Daseyn, aber da sie ferner wesentlich Negation der Negation, die sich auf sich beziehende Negation ist, ist sie das Daseyn, welches F&#252;rsichseyn genannt wird.

> &#167;305 Ideality can be called the _quality_ of infinity; but it is essentially the process of _becoming_, and hence a transition &#8212; like that of becoming in determinate being &#8212; which is now to be indicated. As a sublating of finitude, that is, of finitude as such, and equally of the infinity which is merely its opposite, merely negative, this return into self is _self-relation_, _being_. As this being contains negation it is _determinate_, but as this negation further is essentially negation of the negation, the self-related negation, it is that determinate being which is called _being-for-self_.


If here we take the "infinite" and the "infinitesimal" to go together -- as in [&#167;502](#502) -- then the above would give also that _ideality is the quality of the infinitesimal_. 

Now we have from [&#167;699](#699) that _quality_, being the oppisite moment of quantity, is the [[duality of opposites]] formalized by [[shape modality]] and [[flat modality]]


$$
  \array{
    quality \colon &#643; \dashv \flat
  }
$$

This indeed has a direct infinitesimal analog, namely the [[adjunction]] between the [[infinitesimal shape modality]] $\& $ and [[infinitesimal flat modality]] $\Im$. 

This clearly suggests to translate "ideality is the quality of the infinite"
in [&#167;305](#305)  as the [[unity of opposites]] which is expressed by the [[adjunction]] $ \& \dashv \Im$


$$
  \array{
    & &  \& &\stackrel{ideality}{\stackrel{inf\, quality}{\dashv}}& \Im
    \\
    && \vee && \vee
    \\
    &&  &#643; &\stackrel{quality}{\dashv}& \flat
  }
$$

as part of the [Proce&#223;](#Process). From [&#167;322](#322) we see what the moments here are to be called:

$$
  \array{
    & \text{being-for-self} &  \& &\stackrel{ideality /}{\stackrel{inf.\, quality}{\dashv}}& \Im & \text{being-for-one}
    \\
    && \vee && \vee
    \\
    & attraction &  &#643; &\stackrel{quality}{\dashv}& \flat & repulsion
  }
$$



In fact, this provides [[Aufhebung]] for quality, as indicated, which we may read as the Aufhebung of the finite as it passes into the infinite (which we read as expressed via the infinitesimal). 


Moreover, this extends to an [[adjoint triple]] $\Re \dashv \& \dashv \Im$, with the [[reduction modality]] $\Re$ (from the discussion below [&#167;304](#304)) on the left

This hence gives a second order unity of opposites

$$
  \array{
    && \Re &\dashv& \&
    \\
    && \bot && \bot
    \\
    && \& &\stackrel{{ideality/ \atop {inf.\,quality}}}{\dashv}& \Im
  }
$$

and hence exibits a dual moment of ideality, which, by the discussion below [&#167;304](#304), is related to reality.

Now by [&#167;324](#324) the opposite moment of ideality is indeed supposed to be _reality_. So we should write

$$
  \array{
    && \Re &\stackrel{reality}{\dashv}& \&
    \\
    && \bot && \bot
    \\
    && \& &\stackrel{{ideality/ \atop {inf.\,quality}}}{\dashv}& \Im
  }
$$

and interpret not just the [[reduction modality]] alone as being about reality, but as being just one moment of it, the other moment being expresed by the [[infinitesimal shape modality]] $\& $. 

This happens to make good sense: the [[modal types]] of $\& $ in [[context]] $X$ are the [[étale spaces]] over $X$, exhibiting [[étale groupoids]] (see the discussion at _[[differential cohesion]]_ for details). In terms of [[geometry]] this is what characterizes among all generalized geometric objects those that are _[[manifolds]]_, _[[orbifolds]]_ and generally, _[[geometric stacks]]_. These are indeed "the real spaces" as opposed to non-&#233;tale spaces such as generic [[moduli stacks]], in that a "real space" such as a [[spacetime]] is an [[geometric stack]], while some "abstract", hence maybe "ideal" space such as that of "all electromagnetic field configurations" (a [[moduli stack]]) of not an &#233;tale groupoid. (See also the discussion of this point at _[[higher geometry]]_).

Therefore the [[infinitesimal shape modality|infinitesimal shape]]-[[modal types]] certainly qualify as one "aspect of reality" in any mathematical description of [[physics]] (see also at _[[geometry of physics]]_), and so we conclude that reading the adjunction as

$$
  reality \colon \Re \dashv \&
$$

makes good sense. 

Notice that -- and this is of course precisely what the second-order duality with $ideality \colon \& \dashv \Im $ expresses -- while this is all about reality, in the above sense, it is so only _via_ ideal (ideelle) infinitesimals. This is of course in a way just the big insight of [[Leibniz]] when formulating [[differential calculus]] in terms of infinitesimals (today: [[synthetic differential geometry]]): in order to express the physical _reality_ that is described, notably, by [[differential equations]], it is most useful to consider the idealized concept of infinitesimals, itself without reality, but nevertheless serving to characterize reality. 

The view that the concept of [[infinitesimals]] are closely related to reality is also expressed in [Cohen83, secion 19](#Cohen83):

> F&#252;r diesen H&#246;hepunkt kritischer Naturerkenntnis bildet die Charakteristik der infinitesimalen Gr&#246;&#223;e als intensiver die notwendige Vermittlung;  denn die kritische Bedeutung der Realit&#228;t wird  vorzugsweise  an der  infinitesimalen Intensit&#228;t  durchgef&#252;hrt.

In conclusion, we add to the [Proce&#223;](#Process) the following piece


$$
  \array{
     & \stackrel{vanishing \atop {of\, infinitesimals}}{} & \Re &\stackrel{reality}{\dashv}&  \&
    \\    
    && \bot && \bot
    \\
    & &  \& &\stackrel{ideality/ \atop {inf.\, quality} }{\dashv}& \Im
    \\
    && \vee && \vee
    \\
    &&  &#643; &\stackrel{quality}{\dashv}& \flat
  }
$$


Moreover, here the bottom step upward is an [[Aufhebung]] in the mathematical sense that $\Im \circ &#643; \simeq &#643;$. In view of this, we learn from [&#167;305](#305) 
"Die Idealit&#228;t ... Als [[Aufhebung|Aufheben]] der Endlichkeit" that we might label this as

$$
  \array{
     & \stackrel{vanishing \atop {of\, infinitesimals}}{} & \Re &\stackrel{reality}{\dashv}&  \&
    \\    
    && \bot &\stackrel{Idee}{}& \bot
    \\
    & &  \& &\stackrel{ideality/ \atop {inf.\, quality} }{\dashv}&   
    \Im
    \\
    && \vee &\stackrel{Aufhebung \atop {der.\, Endlichkeit}}{}& \vee
    \\
    &&  &#643; &\stackrel{quality}{\dashv}& \flat
  }
$$



> {#316} &#167;316 Anmerkung 2. Der Satz, da&#223; das Endliche ideell ist, macht den Idealismus aus. Der Idealismus der Philosophie besteht in nichts anderem, als darin, das Endliche nicht als ein wahrhaft Seyendes anzuerkennen. Jede Philosophie ist wesentlich Idealismus, oder hat denselben wenigstens zu ihrem Princip, und die Frage ist dann nur, inwiefern dasselbe wirklich durchgef&#252;hrt ist. Die Philosophie ist es so sehr als die Religion; denn die Religion anerkennt die Endlichkeit ebenso wenig als ein wahrhaftes Seyn, als ein Letztes, Absolutes, oder als ein Nicht-Gesetztes, Unerschaffenes, Ewiges. Der Gegensatz von idealistischer und realistischer Philosophie ist daher ohne Bedeutung. Eine Philosophie, welche dem endlichen Daseyn als solchem wahrhaftes, letztes, absolutes Seyn zuschriebe, verdiente den Namen Philosophie nicht; Principien &#228;lterer oder neuerer Philosophien, das Wasser, oder die Materie oder die Atome sind Gedanken, Allgemeine, Ideelle, nicht Dinge, wie sie sich unmittelbar vorfinden, d. h. in sinnlicher Einzelnheit, selbst jenes thaletische Wasser nicht; denn, obgleich auch das empirische Wasser, ist es au&#223;erdem zugleich das Ansich oder Wesen aller anderen Dinge; und diese sind nicht selbstst&#228;ndige, in sich gegr&#252;ndete, sondern aus einem Anderen, dem Wasser, gesetzte, d. i. ideelle. Indem vorhin das Princip, das Allgemeine, das Ideelle genannt worden, wie noch mehr der Begriff, die Idee, der Geist, Ideelles zu nennen ist, und dann wiederum die einzelnen sinnlichen Dinge als ideell im Princip, im Begriffe, noch mehr im Geiste, als aufgehoben sind, so ist dabei auf dieselbe Doppelseite vorl&#228;ufig aufmerksam zu machen, die bei dem Unendlichen sich gezeigt hat, n&#228;mlich da&#223; das eine Mal das Ideelle das Konkrete, Wahrhaftseyende ist, das andere Mal aber ebenso sehr seine Momente das Ideelle, in ihm Aufgehobene sind, in der That aber nur das Eine konkrete Ganze ist, von dem die Momente untrennbar sind.



#### Third chapter. Das F&#252;rsichsein / Being for self

> {#318} &#167;318 Im F&#252;rsichseyn ist das qualitative Seyn vollendet;

> &#167;318 In being-for-self, qualitative being finds its consummation;

> &#167;319 Being-for-self is first, immediately a being-for-self &#8212; the One.

> Secondly, the One passes into a plurality of ones &#8212; repulsion &#8212; and this otherness of the ones is sublated in their ideality &#8212; attraction.

> Thirdly, we have the alternating determination of repulsion and attraction in which they collapse into equilibrium, and quality, which in being-for-self reached its climax, passes over into quantity.

Here we have a second-order unity of opposites: quantity itself is


quantity : discreteness $\dashv$ continuity

and by the above we take the 


continuum :  attraction $\dashv$  repulsion

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

###### b. Seyn-f&#252;r-eines / Being-for-one

> {#322} &#167;322  Seyn-f&#252;r-eines -- Die&#223; Moment dr&#252;ckt aus, wie das Endliche in seiner Einheit mit dem Unendlichen oder als Ideelles ist.

> F&#252;r-sich-seyn und F&#252;r-Eines-seyn sind also nicht verschiedene Bedeutungen der Idealit&#228;t, sondern sind wesentliche, untrennbare Momente derselben.

> &#167;322 Being-for-one -- This moment expresses the manner in which the finite is present in its unity with the infinite, or is an ideal being [Ideelles].

> &#167;322 To be 'for self' and to be 'for one' are therefore not different meanings of ideality, but are essential, inseparable moments of it.

By the discussion below [&#167;305](#305) the inclusion of [[flat modality|flat modal]] types into [[infinitesimal flat modality|infinitesimal flat modality]] [[modal types]]

$$
  \array{
    \Im
    \\
    \vee
    \\
    \flat
  }
$$

reflects the [[Aufhebung]] which is the passage from the finite to the infinitesimal.

So we may pronounce, in the [Proce&#223;](#Process) the [[infinitesimal flat modality]] as _Seyn-fuer-eines_, _being-for-one_.



Below [&#167;305](#305) we find the [[adjunction]] which plausibly captures the [[unity of opposites]] called ideality, and hence by [&#167;322](#322) what its moments are to be called. 

$$
  \array{
    Fuersichsein & \& &\stackrel{Idealitaet}{\dashv}& \Im & Fuereinssein
  }
$$

See also the discussion below [&#167;348](#348) 


###### Anmerkung
 {#RemarkOnRealityAsOppositeToDuality}

> {#324} &#167;324 Die Idealit&#228;t kommt zun&#228;chst den aufgehobenen Bestimmungen zu, als unterschieden von dem, worin sie aufgehoben sind, das dagegen als das Reelle genommen werden kann. So aber ist das Ideelle wieder eins der Momente und das Reale das andere; 

> &#167;324 But thus the ideal is again one of the moments, and the real the other;

Hence we have another [[unity of opposites]] is $ideality \dashv reality$. See also at _[The One and the Many](#EinsUndVieles)_.

It seems that in _Science of Logic_ there is no _name_ given to this unity. But in the [shorter logic](#EPSBOI) there is: 

> {#EL214} EL&#167;214 Die Idee kann als die Vernunft, (dies ist die eigentliche philosophische Bedeutung der Vernunft), ferner als das Subjekt-Objekt, als die Einheit des Ideellen und Reellen, des Endlichen und Unendlichen, der Seele und des Leibs, als die M&#246;glichkeit, die ihre Wirklichkeit an ihr selbst hat, als das, dessen Natur nur als existierend begriffen werden kann, u.s.f gefa&#223;t werden; weil in ihr alle Verh&#228;ltnisse des Verstandes, aber in ihrer unendlichen R&#252;ckkher, und Identit&#228;t in sich enthalten sind.

> EL&#167;214 The Idea may be described in many ways. It may be called reason; (and this is the proper philosophical signification of reason); subject-object; the unity of the ideal and the real, of the finite and the infinite, of soul and body; the possibility which has its actuality in its own self; that of which the nature can be thought only as existent, etc. 

|      |       |
|------|-------|       
| real | ideal |
| finite | infinitesimal |
| body | soul |

(Regarding "soul and body" see also the comments at _[The monad of Leibniz](#TheMonadOfLeibniz)_, where the similarity to the standard terminology "soul" and "body" for (super-)infinitesimals is pointed out.)


But see below _[The idea](#TheIdea)_, where the idea is given as the unity of the _notion_ and the real. See the discussion below [&#167;1683](#1638).



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

> {#340} &#167;340 The one and the void constitute the first stage of the determinate being of being-for-self. Each of these moments has negation for its determination and is at the same time posited as a determinate being; according to the former determination the one and the void are the relation of negation to negation as of an other to its other: the one is negation in the determination of being, and the void is negation in the determination of non-being.

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

> {#348} &#167;348 We have previously referred to the [[Gottfried Leibniz|Leibnizian]] idealism. We may add here that this idealism which started from the ideating [[monad (disambiguation)|monad]], which is determined as being for itself, advanced only as far as the repulsion just considered, and indeed only to plurality as such, in which each of the ones is only for its own self and is indifferent to the determinate being and being-for-self of the others; or, in general, for the one, there are no others at all. The monad is, by itself, the entire closed universe; it requires none of the others. But this inner manifoldness which it possesses in its ideational activity in no way affects its character as a being-for-self. The Leibnizian idealism takes up the plurality immediately as something given and does not grasp it as a repulsion of the monads. Consequently, it possesses plurality only on the side of its abstract externality. 

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

Notice that in [PN&#167;202b](#PN202b) it says 

> The truly philosophical science of mathematics as theory of magnitude would be the science of measures, but this already presupposes the real particularity of things, which is only at hand in concrete nature.

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

Moreover, below after transition from the Seinslogik to the Wesenslogik, find gauge fields again, with the above structure repeated in the Wesenslogik, see the discussion around [&#167;714](#714).

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


## **Die Lehre vom Wesen** / **The doctrine of essence**
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

There is of course not just one [[object classifier]]/[[type of types]] but a [[universe enlargement|cumulative hierarchy]] of them (see also at _[[universe polymorphism]]_)

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

##### C Der Widerspruch / Contradiction

###### 1. Der Unterschied ueberhaupt

> {#931} &#167;931 Der Unterschied &#252;berhaupt enth&#228;lt seine beiden Seiten als Momente; in der Verschiedenheit fallen sie gleichg&#252;ltig auseinander; im Gegensatze als solchem sind sie Seiten des Unterschiedes, eines nur durchs andere bestimmt, somit nur Momente; aber sie sind ebenso sehr bestimmt an ihnen selbst, gleichg&#252;ltig gegen einander und sich gegenseitig ausschlie&#223;end; die selbstst&#228;ndigen Reflexions-Bestimmungen.

> &#167;931 Difference as such contains its two sides as moments; in diversity they fall indifferently apart; in opposition as such, they are sides of the difference, one being determined only by the other, and therefore only moments; but they are no less determined within themselves, mutually indifferent and mutually exclusive: the self-subsistent determinations of reflection.

> {#934} &#167;934 Der Unterschied &#252;berhaupt ist schon der Widerspruch an sich; denn er ist die Einheit von solchen, die nur sind, insofern sie nicht eins sind,&#8212;und die Trennung solcher, die nur sind als in derselben Beziehung getrennte. Das Positive und Negative aber sind der gesetzte Widerspruch, weil sie als negative Einheiten, selbst das Setzen ihrer, und darin jedes das Aufheben seiner und das Setzen seines Gegentheils ist.&#8212;Sie machen die bestimmende Reflexion als ausschlie&#223;ende aus; weil das Ausschlie&#223;en Ein Unterscheiden, und jedes der Unterschiedenen als Ausschlie&#223;endes selbst das ganze Ausschlie&#223;en ist, so schlie&#223;t jedes in ihm selbst sich aus.

> &#167;934 Difference as such is already implicitly contradiction; for it is the unity of sides which are, only in so far as they are not one-and it is the separation of sides which are, only as separated in the same relation. But the positive and negative are the posited contradiction because, as negative unities, they are themselves the positing of themselves, and in this positing each is the sublating of itself and the positing of its opposite. They constitute the determining reflection as exclusive; and because the excluding of the sides is a single act of distinguishing and each of the distinguished sides in excluding the other is itself the whole act of exclusion, each side in its own self excludes itself.

Here we need a [[unity of opposites]] that expresses "difference as such". The obvious candidate is the opposition between [[false]] and [[true]]. And indeed, in [[type theory]]/[[categorical logic]] these are again given by [[empty type]] $\emptyset$ and [[unit type]] $\ast$ which form an [[adjunction]]

$$
  Abs.\,Contradiction 
  \colon 
  \array{
     false & \emptyset &\dashv& \ast & true
  }
$$

Technically this is the same adjunction as that between [[nothing]] and [[being]] as around [&#167;134](#134) in the Seinslogik. Indeed that makes sense: the tower of determination of the Seinslokig should repeat in the Wesenslogik, but reflected, and hence with different meaning.

###### 2. Der Widerspruch l&#246;st sich auf

> {#943} &#167;943 Nach dieser positiven Seite, da&#223; die Selbstst&#228;ndigkeit im Gegensatze, als ausschlie&#223;ende Reflexion sich zum Gesetztseyn macht, und es ebenso sehr aufhebt, Gesetztseyn zu seyn, ist der Gegensatz nicht nur zu Grunde, sondern in seinen Grund zur&#252;ckgegangen.&#8212; Die ausschlie&#223;ende Reflexion des selbstst&#228;ndigen Gegensatzes macht ihn zu einem Negativen, nur Gesetzten; sie setzt dadurch ihre zun&#228;chst selbstst&#228;ndigen Bestimmungen, das Positive und Negative, zu solchen herab, welche nur Bestimmungen sind; und indem so das Gesetztseyn zum Gesetztseyn gemacht wird, ist es &#252;berhaupt in seine Einheit mit sich zur&#252;ckgekehrt; es ist das einfache Wesen, aber das Wesen als Grund. Durch das Aufheben der sich an sich selbst widersprechenden Bestimmungen des Wesens, ist dieses wiederhergestellt, jedoch mit der Bestimmung, ausschlie&#223;ende Reflexionseinheit zu seyn,&#8212;einfache Einheit, welche sich selbst als Negatives bestimmt, aber in diesem Gesetztseyn unmittelbar sich selbst gleich und mit sich zusammen-gegangen ist.

> &#167; 943 According to this positive side, in which the self-subsistence in opposition, as the excluding reflection, converts itself into a positedness which it no less sublates, opposition is not only destroyed [zugrunde gegangen] but has withdrawn into its ground. The excluding reflection of the self-subsistent opposition converts this into a negative, into something posited; it thereby reduces its primarily self-subsistent determinations, the positive and negative, to the status of mere determinations; and the positedness, being thus made into a positedness, has simply returned into its unity with itself; it is simple essence, but essence as ground. Through the sublating of its inherently self-contradictory determinations, essence has been restored, but with this determination, that it is the excluding unity of reflection-a simple unity that determines itself as a negative, but in this positedness is immediately like itself and united with itself.


> {#944} &#167;944 Zun&#228;chst geht also der selbstst&#228;ndige Gegensatz durch seinen Widerspruch in den Grund zur&#252;ck; jener ist das Erste, Unmittelbare, von dem angefangen wird, und der aufgehobene Gegensatz oder das aufgehobene Gesetztseyn ist selbst ein Gesetztseyn. Somit ist das Wesen als Grund ein Gesetztseyn, ein Gewordenes. Aber umgekehrt hat sich nur die&#223; gesetzt, da&#223; der Gegensatz oder das Gesetztseyn ein Aufgehobenes, nur als Gesetztseyn ist. Das Wesen ist also als Grund so ausschlie&#223;ende Reflexion, da&#223; es sich selbst zum Gesetztseyn macht, da&#223; der Gegensatz, von dem vorhin der Anfang gemacht wurde und der das Unmittelbare war, die nur gesetzte, bestimmte Selbstst&#228;ndigkeit des Wesens ist, und da&#223; er nur das sich an ihm selbst Aufhebende, das Wesen aber das in seiner Bestimmtheit in sich Reflektirte ist. Das Wesen schlie&#223;t als Grund sich von sich selbst aus, es setzt sich; sein Gesetztseyn,&#8212;welches das Ausgeschlossene ist,&#8212;ist nur als Gesetztseyn, als Identit&#228;t des Negativen mit sich selbst. Die&#223; Selbstst&#228;ndige ist das Negative, gesetzt als Negatives; ein sich selbst Widersprechendes, das daher unmittelbar im Wesen als seinem Grunde bleibt.

> &#167;944 In the first place, therefore, the self-subsistent opposition through its contradiction withdraws into ground; this opposition is the prius, the immediate, that forms the starting point, and the sublated opposition or the sublated positedness is itself a positedness. Thus essence as ground is a positedness, something that has become. But conversely, what has been posited is only this, that opposition or positedness is a sublated positedness, only is as positedness. Therefore essence as ground is the excluding reflection in such wise that it makes its own self into a positedness, that the opposition from which we started and which was the immediate, is the merely posited, determinate self-subsistence of essence, and that opposition is merely that which sublates itself within itself, whereas essence is that which, in its determinateness, is reflected into itself. Essence as ground excludes itself from itself, it posits itself; its positedness &#8212; which is what is excluded &#8212; is only as positedness, as identity, of the negative with itself. This self-subsistent is the negative posited as negative; it is self-contradictory and therefore remains immediately in essence as-init ground.


> {#945} &#167;945 Der aufgel&#246;ste Widerspruch ist also der Grund,

> &#167;945 The resolved contradiction is therefore ground, essence as unity of the positive and negative.

By the discussion at [&#167;931](#931) the contradiction in question is given by the adjunction between [[false]]=[[empty type]] and [[true]]=[[unit type]]. The [[Aufhebung]] of that proceeds via the [[sharp modality]] exactly as for [[becoming]] as discussed around [&#167;183](#183) following the technical discussion at _[Aufhebung -- over cohesive sites](Aufhebung#ExamplesBecomingFormalization)_.


$$
  \array{
    && \vdots && \vdots
    \\
    && \bot && \bot
    \\
    && \flat &\dashv& \sharp
    \\
    &&\vee &\stackrel{Aufhebung \atop {des\;Widerspruchs}}{}& \vee
    \\
    &&\emptyset &\stackrel{abs.\,Widerspruch}{\dashv}& \ast
    \\
    Wesen
  }
$$

The question then remains which part of this diagram is to carry the name "Grund".
From [&#167;945](#945) Grund might be the Aufhebung itself, that would make it the analog in the Wesenslogik of the Dasein in the Seinslogik, which was the Aufhebung of [[becoming]].

However, the analog of Dasein in the Wesen should be another determination of being, and "Grund" seems not to be the right word for a determination of being. It seems rather that Grund is to go along with "Existenz" which is a decent name for a determination of being.

So if Grund is not the process of the above Aufhebung, then maybe it is that wherein which we have Aufhebung. By the above these are the [[sharp modality|sharp]]-[[modal types]].

This now has a certain charm to it, because these of course form the [[base topos]]/[[base (infinity,1)-topos|base infinity topos]] of the topos which is the Wesen, and for _that_ the term "Grund" is rather fitting.

So in the [Proce&#223;](#Process) we tentatively label the fragment as

$$
  \array{
    && \vdots && \vdots
    \\
    && \bot && \bot
    \\
    && \flat &\dashv& \sharp & \stackrel{Grund}{}
    \\
    &&\vee &\stackrel{Aufhebung \atop {des\;Widerspruchs}}{}& \vee
    \\
    &&\emptyset &\stackrel{abs.\;Widerspruch}{\dashv}& \ast
    \\
    Wesen
  }
$$




#### Chapter 3. Der Grund

> {#964} &#167;964 Das Wesen bestimmt sich selbst als Grund.

> Wie das Nichts zuerst mit dem Seyn in einfacher unmittelbarer Einheit, so ist auch hier zuerst die einfache Identit&#228;t des Wesens mit seiner absoluten Negativit&#228;t in unmittelbarer Einheit. Das Wesen ist nur diese seine Negativit&#228;t, welche die reine Reflexion ist. Es ist diese reine Negativit&#228;t als die R&#252;ckkehr des Seyns in sich; so ist es an sich oder f&#252;r uns bestimmt, als der Grund, in dem sich das Seyn aufl&#246;st. Aber diese Bestimmtheit ist nicht durch es selbst gesetzt; oder es ist nicht Grund, eben insofern es diese seine Bestimmtheit nicht selbst gesetzt hat. Seine Reflexion aber besteht darin, sich als das, was es an sich ist, als Negatives zu setzen und sich zu bestimmen. Das Positive und Negative machen die wesenhafte Bestimmung aus, in die es als in seine Negation verloren ist. Diese selbstst&#228;ndigen Reflexions-Bestimmungen heben sich auf, und die zu Grunde gegangene Bestimmung ist die wahrhafte Bestimmung des Wesens.

> {#964} &#167;964 Essence determines itself as ground.

> &#167;964 Just as nothing is at first in simple immediate unity with being, so here too the simple identity of essence is at first in immediate unity with its absolute negativity. Essence is only this its negativity, which is pure reflection. It is this pure negativity as the return of being into itself; as such, it is determined in itself, or for us, as ground in which being is dissolved. But this determinateness is not posited by essence itself; in other words, essence is not ground except in so far as it has itself posited this its determinateness. Its reflection, however, consists in its positing and determining itself as that which it is in itself, as a negative. The positive and negative constitute that determination of essence in which essence is lost in its negation. These self-subsistent determinations of reflection sublate themselves, and the determination that has fallen to the ground [zugrunde gegangene] is the true determination of essence.

On this see the discussion around [&#167;945](#945)


> &#167;964 Essence determines itself as ground.

> {#968} &#167;968 Der Grund ist zuerst absoluter Grund, in dem das Wesen zun&#228;chst als Grundlage &#252;berhaupt f&#252;r die Grundbeziehung ist; n&#228;her bestimmt er sich aber als Form und Materie, und giebt sich einen Inhalt.

> Zweitens ist er bestimmter Grund, als Grund von einem bestimmten Inhalt; indem die Grundbeziehung sich in ihrer Realisirung &#252;berhaupt &#228;u&#223;erlich wird, geht sie in die bedingende Vermittelung &#252;ber.

> Drittens, der Grund setzt eine Bedingung voraus; aber die Bedingung setzt ebenso sehr den Grund voraus; das Unbedingte ist ihre Einheit, die Sache an sich, die durch die Vermittelung der bedingenden Beziehung in die Existenz &#252;bergeht.

> Ground is first, absolute ground, in which essence is, in the first instance, a substrate for the ground relation; but it further determines itself as form and matter and gives itself a content.

> Secondly, it is a determinate ground as ground of a determinate content; in that the ground relation in its realisation as such becomes external to itself, it passes over into conditioning mediation.

> Thirdly, ground presupposes a condition; but the condition no less presupposes the ground; the unconditioned is their unity, the fact in itself, which through the mediation of the conditioning relation passes over into Existence.

##### A. Der absolute Grund

###### a. Form und Wesen

> {#970} &#167;970 der Grund ist als das aufgehobene Bestimmtseyn nicht das Unbestimmte, sondern das durch sich selbst bestimmte Wesen, aber als unbestimmt oder als aufgehobenes Gesetztseyn Bestimmtes. Er ist das Wesen, das in seiner Negativit&#228;t mit sich identisch ist.

> &#167;970 The determination of reflection, in so far as it withdraws into ground, is a first, an immediate determinate being in general, which forms the starting point. But determinate being still has only the meaning of positedness and essentially presupposes a ground-in the sense that it does not really posit a ground, that this positing is a sublating of itself, that really it is the immediate that is the posited, and ground the not-posited. As we have seen, this presupposing is positing that recoils on that which posits: ground, as the determination that has been sublated, is not indeterminate; it is essence determined through itself, but determined as undetermined, or as a sublated positedness. Ground is essence that in its negativity is identical with itself.

> Der Form geh&#246;rt &#252;berhaupt alles Bestimmte an; es ist Formbestimmung, insofern es ein Gesetztes, hiermit von einem solchen, dessen Form es ist, Unterschiedenes ist; die Bestimmtheit als Qualit&#228;t ist eins mit ihrem Substrat, dem Seyn; das Seyn ist das unmittelbar Bestimmte, das von seiner Bestimmtheit noch nicht unterschieden,&#8212;oder das in ihr noch nicht in sich reflektirt, so wie diese daher eine seyende, noch nicht eine Gesetzte ist.&#8212;Die Formbestimmungen des Wesens sind ferner als die Reflexions-Bestimmtheiten, ihrer n&#228;hern Bestimmtheit nach, die oben betrachteten Momente der Reflexion. Die Identit&#228;t, und der Unterschied, dieser Theils als Verschiedenheit, Theils als Gegensatz. Ferner aber geh&#246;rt auch die Grundbeziehung dazu, insofern sie zwar die aufgehobene Reflexions-Bestimmung aber dadurch das Wesen zugleich als Gesetztes ist. Dagegen geh&#246;rt zur Form nicht die Identit&#228;t, welche der Grund in sich hat, n&#228;mlich da&#223; das Gesetztseyn als aufgehobenes und das Gesetztseyn als solches,&#8212;der Grund und das Begr&#252;ndete,&#8212;Eine Reflexion ist, welche das Wesen als einfache Grundlage ausmacht, die das Bestehen der Form ist. Allein die&#223; Bestehen ist im Grunde gesetzt; oder die&#223; Wesen ist selbst wesentlich als bestimmtes; somit ist es auch wieder das Moment der Grundbeziehung und Form.&#8212;Die&#223; ist die absolute Wechselbeziehung der Form und des Wesens, da&#223; dieses einfache Einheit des Grundes und des Begr&#252;ndeten, darin aber eben selbst bestimmt oder Negatives ist, und sich als Grundlage von der Form unterscheidet, aber so zugleich selbst Grund und Moment der Form wird.

> {#973} &#167;973 Das Wesen hat eine Form,

> &#167;973 Essence has a form

Notice that "Form" also means _shape_. By the discussion at [&#167;812](#812),[&#167;816](#816),  the Essence  is formalized as the ambient [[(infinity,1)-topos|topos]]. In view of this [&#167;973](#973) translates to "The topos has a shape", and indeed there is the concept of [[shape of an (infinity,1)-topos|shape of an infinity-topos]].
This is just what is reflected by the [[shape modality]] $&#643;$.

Morover, given a [[type]] $X$ in the Wesen, hence in [[cohesive homotopy type theory]], it makes good sense to refer to $&#643; X$ as the  _shape_ of that [[homotopy type]] -- which is in the established traditional sense of _[[shape theory]]_ . This is indeed what the name "shape modality" is alluding to.

See the discussion below [&#167;989](#989) for the dual moment.



###### b. Form und Materie
 {#FormUndMaterie}

> {#978} &#167;978 Das Wesen wird zur Materie, indem seine Reflexion sich bestimmt, zu demselben als zu dem formlosen Unbestimmten sich zu verhalten. 

> &#167;978 Essence becomes matter in that its reflection is determined as relating itself to essence as to the formless indeterminate.

> {#980} &#167;980 Die Materie mu&#223; daher formirt werden, und die Form mu&#223; sich materialisiren,

> {#981} &#167;981 2. Die Form bestimmt daher die Materie, und die Materie wird von der Form bestimmt.

> &#167;981 2. Hence form determines matter, and matter is determined by form.

Notice by [&#167;1068](#1068) that here indeed _Materie_ refers to the physical world (even if physical _nature_ only appears much further down in [PN&#167;192](#PN192)) and explicitly refers also to [[physical fields]].

###### c. Form und Inhalt.
 {#FormUndInhalt}

> {#989} &#167;989 Die Form steht zuerst dem Wesen gegen&#252;ber; so ist sie Grundbeziehung &#252;berhaupt, und ihre Bestimmungen, der Grund und das Begr&#252;ndete. Alsdenn steht sie der Materie gegen&#252;ber; so ist sie bestimmende Reflexion und ihre Bestimmungen sind die Reflexionsbestimmung selbst und das Bestehen derselben. Endlich steht sie dem Inhalte gegen&#252;ber,

> &#167;989 At first, form stands opposed to essence; it is then the simple ground relation, and its determinations are the ground and the grounded. Secondly, it stands opposed to matter; it is then determining reflection, and its determinations are the reflected determination itself and the subsistence of the determination. Lastly, it stands opposed to content;

Above in the discussion at [&#167;973](#973) we identified the moment of "form" with the shape modality at the reflected level of the Wesen, since for $X$ a [[type]] in [[cohesive homotopy type theory]], then $&#643; X$ is indeed naturally pronounced as the "shape of the homotopy type" in the traditional sense of [[shape theory]]. 

In this vein, the collection of all global points $\ast \to X$ in $X$, hence its [[flat modality]] $\flat X$ is naturally pronounced as the "content" of that type. It is literally the collection of unit types ( _ones_ [&#167;340](#340))-- that it _contains_ .

Indeed, if one thinks of $X$ as a [[cohesive homotopy type]], then $\flat X$ is the _underlying bare homotopy type_ with its cohesion forgotten. 

This terminology is motivated from and well adapted to the picture in chemistry (see at _[[motivation for cohesive toposes]]_): imagine a chunk of chemical substance, then its plain content of substance is the collection of all the separate molecules -- quantified by the number of moles of the substance -- whereas in remembering just this number  all memory of the shape and cohesion of the substance has been forgotten. Indeed, by [&#167;1068](#1068), this reference to chemistry seems to be entirely intended.

Therefore it is natural to pronounce the [[flat modality]] $\flat$, as the _content_, _Inhalt_. And so then by [&#167;973](#973) its [[adjunction]] with the [[shape modality]] yields a [[unity of opposites]]

$$
  \array{
     form & &#643; & \dashv & \flat & content
  }
$$

which is naturally identified with what the text in [&#167;989](#989) alludes to.

It remains to find the name of this [[unity of opposites]]:


> {#990} &#167;990 Der Inhalt hat erstlich eine Form und eine Materie, die ihm angeh&#246;ren und wesentlich sind; er ist ihre Einheit.

> &#167;990 The content is, first, a form and a matter which belong to it and are essential; it is their unity

So form-content-matter form a [[unity of opposites]].  The exact form of [&#167;990](#990) suggests to take $(form \stackrel{content}{\dashv} matter)$, which however seems a bit awkward. But by [&#167;989](#989) there seems to be some flexibility in these three terms opposing each other, and if we appeal to that and declare that we should put

$$
  \array{
     form & &#643; & \stackrel{matter}{\dashv} & \flat & content
  }
$$

then it works out nicely:  Notice by [&#167;1068](#1068) that "matter" here includes _[[physical fields]]_ such as explicitly the [[electromagnetic field]], hence _[[gauge fields]]_. Now this matches: by the discussion at _[[differential cohomology hexagon]]_ the adjunction $&#643; \dashv \flat$ is precisely what axiomatizes [[higher gauge fields]] in the form of [[cocycles]] in [[differential cohomology]].

This fits indeed rather well, as it means that we recover at the stage of the Wesenslogik what we already had at the stage of the Seinslogik (where the appearance of [[gauge fields]] via the above adjunction is discussed around [&#167;714](#714)).

But we should maybe make notationally more explicit (than would have been possibl in 1812) that, by [&#167;1068](#1068), "matter" here means "[[physical fields]] and matter" and specifically [[gauge fields]]. Therefore in the [Proce&#223;](#Process) we add the stage:

$$
  \array{
     form & &#643; & \stackrel{(gauge)\,fields}{\dashv} & \flat & content
  }
  \,.
$$




##### B. Der bestimmte Grund

###### a. Der formelle Grund

###### b. Der reale Grund

###### c. Der vollstaendige Grund

##### C. Die Bedingung

###### a. Das relativ Unbedingte

> {#1021} &#167;1021 Der Grund ist das Unmittelbare und das Begr&#252;ndete das Vermittelte.

> &#167;1021 Ground is the immediate, and the grounded the mediated.

|  | Begriffslogik | [[natural deduction]] |
|--|---------------|-----------------------|
| unmittlebar | Grund         | [[antecedent]]       |
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

#### Chapter 1. Die Existenz / Existence. 

> {#1040} &#167;1040 Just as the proposition of ground states that whatever is has a ground, or is something posited or mediated, so too we must formulate a proposition of Existence, and in these terms: whatever is, exists. The truth of being is to be, not a first immediate, but essence that has emerged into immediacy.

##### A. Das Ding und seine Eigenschaften.

> {#1048} &#167;1048 Das Ding wird von seiner Existenz unterschieden, wie das Etwas von seinem Seyn unterschieden werden kann.

> &#167;1048 The thing is distinct from its Existence just as something can be distinguished from its being.

This means that the _Ding_ repeats (reflected) the _Etwas_ from the Seinslogik in [&#167;221](#221):

|  | moment  |  unity   | comoment |
|--|---|-----|--| 
| **Seinslogik** | Ansichseyn | Etwas | Sein-fuer-Anderes |
| **Wesenslogik**  | Existenz   | Ding |   |

Hence we locate these terms at matching positions in the _[Proce&#223;](#Process)_.


###### a. Ding an sich und Existenz.

###### b. Die Eigenschaft.

> {#1056} &#167;1056 Die Qualit&#228;t ist die unmittelbare Bestimmtheit des Etwas; das Negative selbst, wodurch das Seyn Etwas ist.

> &#167;1056 Quality is the immediate determinateness of something, the negative itself through which being is something. 

###### c. Die Wechselwirkung der Dinge.

##### B. Das Bestehen des Dings aus Materien.
 {#BestehenDesDingsAusMaterien}

> {#1068} &#167;1068 Der &#220;bergang der Eigenschaft in eine Materie oder in einen selbstst&#228;ndigen Stoff ist der bekannte &#220;bergang, den an der sinnlichen Materie die Chemie macht, indem sie die Eigenschaften der Farbe, des Geruchs, des Geschmacks u.s.f. als Lichtstoff, F&#228;rbestoff, Riechstoff, sauren, bittern u.s.f. Stoff darzustellen sucht oder andere wie den W&#228;rmestoff, die elektrische, magnetische Materie geradezu nur annimmt, und damit die Eigenschaften in ihrer Wahrhaftigkeit zu handhaben &#252;berzeugt ist.&#8212;Ebenso gel&#228;ufig ist der Ausdruck, da&#223; die Dinge aus verschiedenen Materien oder Stoffen bestehen. Man h&#252;tet sich, diese Materien oder Stoffe Dinge zu nennen; ob man wohl auch einr&#228;umen wird, da&#223; z.B. ein Pigment, ein Ding ist; ich wei&#223; aber nicht, ob z.B. auch der Lichtstoff, der W&#228;rmestoff, oder die elektrische Materie u.s.f. Dinge genannt werden. Man unterscheidet die Dinge und ihre Bestandtheile, ohne genau anzugeben, ob diese und in wie weit sie auch Dinge, oder etwa nur Halbdinge seyen; aber Existirende &#252;berhaupt sind sie wenigstens.

> &#167;1068 The transition of property into a matter or into a self-subsistent stuff is the familiar transition performed on sensible matter by chemistry when it seeks to represent the properties of colour, smell, taste and so on, as luminous matter, colouring matter, odorific matter, sour, bitter matter and so on, or merely straightway postulates others like heat matter or caloric, electrical and magnetic matter, in the conviction that it has got hold of properties in their truth. Equally current is the expression that things consist of various matters. One is careful not to call these matters things; although it would certainly be admitted that, e.g. a pigment is a thing; but I do not know whether e.g. luminous matter, heat matter or electrical matter and so on, are also called things. Things and their constituents are distinguished without it being exactly stated whether and to what extent the latter are also things or perhaps only half things; but they are at least existents in general.

Despite -- and in fact via -- this cautioning remark, this says that the word _Materie_ as used before in _[Form und Materie](#FormUndMaterie)_ and _[Form und Inhalt](#FormUndInhalt)_ is indeed meant what the physical world is made of. Notice 

1. how the reference to chemical substances harmonizes with the chemical imagery going with [[cohesion]] in the discussion below [&#167;989](#989);

1. that not just genuine matter but also what in modern parlance is called _[[physical fields]]_, notably  _[[gauge fields]]_ ("Lichtstoff" = [[light]], "elektrische Materie" =[[electromagnetic field]]), is explicitly included.

To highlight this we should maybe write  _Materiefelder_ or just _Felder_ or even _Eichfelder_ instead, which is what we do in the [Proce&#223;](#Process)-diagram.

It is maybe noteworthy that some physics appears here in the Wesenslogik, even though _nature_ will not appear before [PN&#167;192](#PN192).



> Die Nothwendigkeit, von den Eigenschaften zu Materien &#252;berzugehen, oder da&#223; die Eigenschaften in Wahrheit Materien sind, hat sich daraus ergeben, da&#223; sie das Wesentliche und damit das wahrhaft Selbstst&#228;ndige der Dinge sind.



##### C. Die Aufl&#246;sung des Dinges.

> Die Existenz hat in diesem Dinge ihre Vollst&#228;ndigkeit erreicht, n&#228;mlich in Einem an sich seyendes Seyn oder selbstst&#228;ndiges Bestehen, und unwesentliche Existenz zu seyn; die Wahrheit der Existenz ist daher, ihr Ansichseyn in der Unwesentlichkeit, oder ihr Bestehen in einem Andern und zwar dem absolut Andern, oder zu ihrer Grundlage ihre Nichtigkeit zu haben. Sie ist daher Erscheinung.

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


## **Die Lehre vom Begriff** / **The doctrine of the notion**

> {#B160} &#167;B160 Der Begriff ist das Freie, als die f&#252;r sich seiende Macht der Substanz; -- und als die Totalit&#228;t dieser Negativit&#228;t, in welcher jedes der Momente das Ganze ist, das er ist, und als ungetrennte Einheit mit ihm gesetzt ist, ist er in seiner Identit&#228;t mit sich das an und f&#252;r sich bestimmte.  


### Section 1. Der subjektive Begriff / Subjectivity.

#### a. Begriff als solcher

#### b. Urtheil

#### c. Schluss

### Section 2. Das Objekt / Objectivity

#### a. Mechanismus

#### b. Chemismus

#### c. Teleologie

### Section 3. Die Idee / The Idea
 {#TheIdea}

> {#1663} &#167;1636 The Idea being the unity of Notion and reality, being has attained the significance of truth;

In [[categorical logic]]/[[type theory]], _[[true]]_ is given by the [[unit type]] $\ast$ as discussed around [&#167;934](#934), which is exactly what was identified as formalizing _being_ above at [&#167;132](#132).


> {#1634} &#167;1634 But having reached the result that the Idea is the unity of the Notion and objectivity,

> {#1636} &#167;1636 Die Idee ist die Einheit des Begriffs und der Realit&#228;t

> &#167;1636 The Idea being the unity of Notion and reality, 

> {#1638} &#167;1638 However, the Idea has not merely the more general meaning of the true being, of the unity of Notion and reality, but the more specific one of the unity of subjective Notion and objectivity.

So 

* Idee = Begriff & Realit&#228;t 

See also [EL&#167;214](#EL214), which instead has

* Idee = das Ideelle & das Reelle .

But of course the Notion is _ideell_, by [&#167;304](#304) "wie auch weiterhin der Begriff als ein Ideelles und zwar als ein nur Ideelles" and [&#167;316](#316) "wie noch mehr der Begriff, die Idee, der Geist, Ideelles zu nennen ist".

(Notice that it is _Realit&#228;t_ [&#167;304](#304), [&#167;305](#305) which appears here, not _Wirklichkeit_ (_actuality_) as in [&#167;1160](#1160).)

Now that the Idea has appeared in the _Logic_, nature springs out of it (as announced in [&#167;53](#53)). The _[shorter Logic](#EPSBOI)_ ends with [EL&#167;244](#EL244).



#### a. Leben

> {#EL2126} EL&#167;216  Die unmittelbare Idee ist das Leben. Der Begriff ist als Seele in einem Leibe realisiert.


#### b. Erkennen

#### c. Absolute Idee

> {#EL244} EL&#167;244 Die Idee, welche f&#252;r sich ist, nach dieser ihrer Einheit mit sich betrachtet, ist sie Anschauen, und die anschauende Idee Natur. Als Anschauen aber ist die Idee in einseitiger Bestimmung der Unmittelbarkeit oder Negation durch &#228;u&#223;erliche Reflexion gesetzt. Die absolute Freiheit der Idee aber ist, da&#223; sie nicht blo&#223; ins Leben &#252;bergeht, noch als endliches Erkennen dasselbe in sich scheinen l&#228;&#223;t, sondern in der absoluten Wahrheit ihrer selbst sich entschlie&#223;t, das Moment ihrer Besonderheit oder des ersten Bestimmens und Andersseins, die unmittelbare Idee als ihren Widerschein, sich als Natur frei aus sich zu entlassen.

The theme of the idea expressing itself via the spirit in nature is summarized well [here](#PSEJul14).

## **Die Philosophie der Natur** / **Philosophy of Nature**
 {#PhilosophyOfNature}

The next book in the system, after the _Science of Logic_, is the _[[Philosophy of Nature]]_. It starts continuing from [EL&#167;244](#EL244) in [PN&#167;192](#PN192).
(Notice however that "matter" and in fact "[[physical fields]]" were already in the Wesenslogik, around [&#167;1068](#1068).)

### Betrachtungsweisen der Natur

### Begriff der Natur



> {#PN192} PN&#167;192.  Die Natur hat sich als die Idee in der Form des Andersseins ergeben. Da die Idee so als das Negative ihrer selbst oder sich &#228;u&#223;erlich ist, so ist die Natur nicht &#228;u&#223;erlich nur relativ gegen diese Idee (und gegen die subjektive Existenz derselben, den Geist), sondern die &#196;u&#223;erlichkeit macht die Bestimmung aus, in welcher sie als Natur ist.

> PN&#167;192 Nature has come into being as the idea in the form of otherness".

Hence Nature is the externalization of the Idea, and, by [PN&#167;193b](#PN193b) is _representation_ of the Idea. By the above, the Idea is the last stage in the system of modalities. Possible technical terminology for a [[model]] of the [[modal type theory]] is essentially verbatim "representation" and "externalization".


> PN&#167;193a Die Natur zeigt daher in ihrem Dasein keine Freiheit, sondern Notwendigkeit und Zuf&#228;lligkeit.

> PN&#167;193a Hence nature exhibits no freedom in its existence, but only necessity and contingency.

> {#PN193b} PN&#167;193b Weil sie jedoch, $[$ ... $]$ Darstellung der Idee ist, 

> PN&#167;193b $[$ ... $]$ nature is a representation of the idea, 

Darstellung/representation: [[model]] of the [[theory]]


> PN&#167;195. Nature is, in itself a living whole. The movement of its idea through its sequence of stages is more precisely this: the idea posits itself as that which it is in itself; or, what is the same thing, it goes into itself out of that immediacy and externality which is death in order to go into itself; yet further, it suspends this determinacy of the idea, in which it is only life, and becomes spirit, which is its truth.


> {#PN202a} PN&#167;202a Other mathematical determinations, such as infinity and its relationships, the infinitesimal, factors, powers, and so on, have their true concepts in philosophy itself. It is awkward to want to take and derive these from mathematics, where they are employed in a nonconceptual, often meaningless way; rather, they must await their justification and significance from philosophy. 

### Einteilung

> Die Idee als Natur ist:

> I. in der Bestimmung des Au&#223;ereinander, der unendlichen Vereinzelung, au&#223;erhalb welcher die Einheit der Form, diese daher als eine ideelle, nur an sich seiende und daher nur gesuchte ist, die Materie und deren ideelles System, &#8211; Mechanik;

> II. in der Bestimmung der Besonderheit, so da&#223; die Realit&#228;t mit immanenter Formbestimmtheit und an ihr existierender Differenz gesetzt ist, ein Reflexionsverh&#228;ltnis, dessen Insichsein die nat&#252;rliche Individualit&#228;t ist, &#8211; Physik;

> III. in der Bestimmung der Subjektivit&#228;t, in welcher die realen Unterschiede der Form ebenso zur ideellen Einheit, die sich selbst gefunden und f&#252;r sich ist, zur&#252;ckgebracht sind, &#8211; Organik

On the importance of the discussion of _Measure_ [above](#TheMeasure) in the passage to nature:

> {#PN202b} PN&#167;202b The truly philosophical science of mathematics as theory of magnitude would be the science of measures, but this already presupposes the real particularity of things, which is only at hand in concrete nature.

> {#PN250} PN&#167;250 Der Widerspruch der Idee, indem sie als Natur sich selbst &#228;u&#223;erlich ist

### Die Mechanik

#### Mathematische Mechanik -- Raum und Zeit

##### Der Raum
 {#DerRaum}

> {#PN254a} PN&#167;254a Die erste oder unmittelbare Bestimmung der Natur ist die abstrakte Allgemeinheit ihres Au&#223;ersichseins, &#8211; dessen vermittlungslose Gleichg&#252;ltigkeit, der Raum. Er ist das ganz ideelle Nebeneinander, weil er das Au&#223;ersichsein ist, und schlechthin kontinuierlich, weil dies Au&#223;ereinander noch ganz. abstrakt ist und keinen bestimmten Unterschied in sich hat.

> {#PN254b} PN&#167;254b Von Raumpunkten zu sprechen, als ob sie das positive Element des Raums ausmachten, ist unstatthaft,

> PN&#167;254b To speak of points of space, as if they constituted the positive element of space, is inadmissible

[[synthetic geometry]], see also [PN&#167;256b](#PN256b)

> {#PN256a} PN&#167;256a Aber der Unterschied ist wesentlich bestimmter, qualitativer Unterschied. Als solcher ist er $\alpha$) zun&#228;chst Negation des Raumes selbst, weil dieser das unmittelbar unterschiedlose Au&#223;ersichsein ist, -- der Punkt. $\beta$) Die Negation ist aber Negation des Raumes, d. i. sie ist selbst r&#228;umlich; der Punkt als wesentlich diese Beziehung, d.i. als sich aufhebend, ist die Line, das erste anders-, d.i. R&#228;umlich-sein des Punktes. $\gamma$) Die Wahrheit des Andersseins ist aber die Negation der Negation. Die Linie geht daher in die Fl&#228;che &#252;ber, welche einerseits eine Bestimmtheit gegen Linie und Punkt, und so Fl&#228;che &#252;berhaupt, andererseits aber die aufgehobene Negation des Raumes ist, somit Wiederherstellung der  r&#228;umlichen Totalit&#228;t, welche nunmehr das negative Moment an ihr hat; -- umschlie&#223;ende Oberfl&#228;che, die einen einzelnen ganzen Raum absondert.


[[schreiber:The brane bouquet|the brane bouquet]]: form the (super-)point $\mathbb{R}^{0|N}$ emanate the $\mathbb{R}^{d|N}$ by central extension via the $(-\Gamma-)$.

> {#PN256b} PN&#167;256b Da&#223; die Linie nicht aus Punkten, die Fl&#228;che nicht aus Linien besteht, geht aus ihrem Begriffe hervor, da die Linie vielmehr der Punkt als au&#223;er sich seiend, n&#228;mlich sich auf den Raum beziehend und sich aufhebend, die Fl&#228;che ebenso die aufgehobene, au&#223;er sich seiende Linie ist. &#8211;

> PN&#167;256b That the line does not consist of points, nor the plane of lines, follows from their concepts

[[synthetic geometry]], see also [PN&#167;254b](#PN254b)

##### Die Zeit

##### Einheit von Raum und Zeit

###### Ort und Bewegung

> {#PN260} PN&#167;260 Der Raum ist in sich selbst der Widerspruch des gleichg&#252;ltigen Auseinanderseins und der unterschiedlosen Kontinuit&#228;t, die reine Negativit&#228;t seiner selbst und das &#220;bergehen zun&#228;chst in die Zeit. Ebenso ist die Zeit, da deren in Eins zusammengehaltene entgegengesetzte Momente sich unmittelbar aufheben, das unmittelbare Zusammenfallen in die Indifferenz, in das ununterschiedene Au&#223;ereinander oder den Raum. So ist an diesem die negative Bestimmung, der ausschlie&#223;ende Punkt, nicht mehr nur an sich dem Begriffe nach, sondern gesetzt und in sich concret durch die totale Negativit&#228;t welche die Zeit ist; -- der so konkrete Punkt ist der Ort. 

modern terminology here would be: [[spacetime]] [[event]]

###### Materie und Bewegung

> {#PN261} PN&#167;261 Dies Vergehen und Sich-wiedererzeugen des Raumes in der Zeit und der Zeit im Raum, $[$...$]$ ist die Bewegung. Dies Werden ist aber selbst eben so sehr das in sich Zusammenfallen seines Widerspruchs, die unmittelbar identische daseiende Einheit beider, die Materie.

> This disappearance and regeneration of space in time and of time in space is motion;-- a becoming, which, however, is itself just as much immediately the identically existing unity of both, or matter.

> $[$ dies $]$ ist f&#252;r den Verstand unbegreiflich.

So [[space]] and [[time]] transmute into each other, forming a unity. The appropriate modern word for this is clearly _[[spacetime]]_. That Hegel's perspective fits well with modern [[general relativity]] has been argued in ([Wandschneider82](#Wandschneider82)).

Moreover, this unity of space and time in spacetime is [[matter]]. This is indeed the perspective of the modern concept of [[KK-compactification]] in which theories of pure ([[supergravity]]-)[[gravity]] give rise to matter and forces depending on how parts of spacetime take certain shape. For instance [[model (physics)|models]] such as the [[G2-MSSM]] are pure gravity (in this case [[11d supergravity]]) taking shape in the form of a [[KK-compactification]] on a [[G2-manifold]] [[fiber bundle]], and all the [[matter]] (and [[force]] field) content of the [[standard model of particle physics]] arises from just this (super-)geometry.

A vaguely similar synthethis had been suggested in ([Weyl 1919](#Weyl19)). In the 1960s [[John Wheeler]] highlighted this idea of producing matter from pure spacetime geometry, coining the term [[geometrodynamics]] for it. His slogan "mass without mass" referred to mass arising from pure spacetime geometry. At this level of detail, this is rather close to [PN&#167;261](#PN261).

#### Endliche Mechanik -- Materie und Bewegung. 


#### Absolute Mechanik -- Astronomie

##### Die allgemeine Gravitation

> {#PN269} PN&#167;269 Die Gravitation ist der wahrhafte und bestimmte Begriff der materiellen K&#246;rperlichkeit, der zur Idee realisiert ist

##### Die Kepplerschen Gesetze

##### Die Totalit&#228;t des Sonnen-Systems


### Die Physik

### Die Organik

#### A. Die geologische Natur

#### B. Die vegetabilische Natur

#### C. Der tierische Organismus


The last paragraph is

> {#PN298} PN&#167;298. In this way nature has passed over into its truth, into the subjectivity of the concept, whose objectivity is itself the suspended immediacy of individuality, the concrete generality, the concept which has the concept as its existence &#8212; into the spirit.



## **Die Philosophie des Geistes** / **Philosophy of Spirit**
 {#PhilosophyOfSpirit}



### Einleitung

### Begriff des Geistes

> PG&#167;381 Der Geist hat f&#252;r uns die Natur zu seiner Voraussetzung, deren Wahrheit und damit deren absolut Erstes er ist. In dieser Wahrheit ist die Natur verschwunden, und der Geist hat sich als die zu ihrem F&#252;rsichsein gelangte Idee ergeben, deren Objekt ebensowohl als das Subjekt der Begriff ist. Diese Identit&#228;t ist absolute Negativit&#228;t, weil in der Natur der Begriff seine vollkommene &#228;u&#223;erliche Objektivit&#228;t hat, diese seine Ent&#228;u&#223;erung aber aufgehoben und er in dieser identisch mit sich geworden ist. Er ist diese Identit&#228;t somit zugleich nur als Zur&#252;ckkommen aus der Natur.

> PS&#167;381 Spirit has for us nature as its presupposition, of which it is truth. In this truth, its concept, nature has disappeared; spirit has therefore produced itself as idea, of which the concept is both the object and the subject. This identity is absolute negativity, because in nature the concept has its completely external objectivity. But it has suspended its articulation, and in this it has become identical with itself. It is this identity only insofar as it is a return from nature.

The theme of the idea expressing itself via the spirit in nature is summarized well [here](#PSEJul14).

> PG&#167;381 Das Wesen des Geistes ist deswegen formell die Freiheit

> &#167; 384 Das Offenbaren, welches als das Offenbaren der abstrakten Idee unmittelbarer &#220;bergang, Werden der Natur ist, ist als Offenbaren des Geistes, der frei ist, Setzen der Natur als seiner Welt; ein Setzen, das als Reflexion zugleich Voraussetzen der Welt als selbst&#228;ndiger Natur ist. Das Offenbaren im Begriffe ist Erschaffen derselben als seines Seins, in welchem er die Affirmation und Wahrheit seiner Freiheit sich gibt. 

> Das Absolute ist der Geist, dies ist die h&#246;chste Definition des Absoluten. &#8211; Diese Definition zu finden und ihren Sinn und Inhalt zu begreifen, dies, kann man sagen, war die absolute Tendenz aller Bildung und Philosophie, auf diesen Punkt hat sich alle Religion und Wissenschaft gedr&#228;ngt; aus diesem Drang allein ist die Weltgeschichte zu begreifen. &#8211; Das Wort und die Vorstellung des Geistes ist fr&#252;h gefunden, und der Inhalt der christlichen Religion[29] ist, Gott als Geist zu erkennen zu geben. Dies, was hier der Vorstellung gegeben und was an sich das Wesen ist, in seinem eigenen Elemente, dem Begriffe, zu fassen, ist die Aufgabe der Philosophie, welche so lange nicht wahrhaft und immanent gel&#246;st ist, als der Begriff und die Freiheit nicht ihr Gegenstand und ihre Seele ist.[30]
 

### Erste Abteilung. Der subjektive Geist

#### A. Anthropologie

##### a. Nat&#252;rliche Seele

##### b. tr&#228;umende Seele

##### c. Wirkliche Seele

#### B. Ph&#228;nomenologie

##### a. Bewu&#223;tsein als solches

##### b. Selbstbewu&#223;tsein

##### c. Vernunft

#### B. Psychologie

##### a. Theoretischer Geist

##### b. Praktischer Geist

###### $\alpha$. Praktisches Gef&#252;hl

###### $\beta$. Trieb

###### $\gamma$. Willk&#252;r und Gl&#252;ckseligkeit

### Zweite Abteilung. Der objektive Geist

#### A. Das Recht

#### B. Die Moralit&#228;t

#### C. Die Sittlichkeit

### Dritte Abteilung. Der absolute Geist


#### A. Die Kunst

#### B. Die geoffenbarte Religion

#### C. Die Philosophie
 


> PG&#167;574 Dieser Begriff der Philosophie ist die sich denkende Idee, die wissende Wahrheit (&#167; 236), das Logische mit der Bedeutung, da&#223; es die im konkreten Inhalte als in seiner Wirklichkeit bew&#228;hrte Allgemeinheit ist. Die Wissenschaft ist auf diese Weise in ihren Anfang zur&#252;ckgegangen und das Logische so ihr Resultat als das Geistige, da&#223; es aus dem voraussetzenden Urteilen, worin der Begriff nur an sich und der Anfang ein Unmittelbares war, hiermit aus der Erscheinung, die es darin an ihm hatte, in sein reines Prinzip zugleich als in sein Element sich erhoben hat.

return to the beginning

The second edition of the _Enzyklop&#228;die der philos. Wiss._ from 1827 ends here. Later the following three paragraphs are added, concerning three kinds of _Schlu&#223;_.

> PG&#167;575 Es ist dieses Erscheinen, welches zun&#228;chst die weitere Entwicklung begr&#252;ndet. Die erste Erscheinung macht der Schlu&#223; aus, welcher das Logische zum Grunde als Ausgangspunkt und die Natur zur Mitte hat, die den Geist mit demselben zusammenschlie&#223;t. Das Logische wird zur Natur und die Natur zum Geiste. Die Natur, die zwischen dem Geiste und seinem Wesen steht, trennt sie zwar nicht zu Extremen endlicher Abstraktion, noch sich von ihnen zu einem Selbst&#228;ndigen, das als Anderes nur Andere zusammenschl&#246;sse; denn der Schlu&#223; ist in der Idee und die Natur wesentlich nur als Durchgangspunkt und negatives Moment bestimmt und an sich die Idee; aber die Vermittlung des Begriffs hat die &#228;u&#223;erliche Form des &#220;bergehens und die Wissenschaft die des Ganges der Notwendigkeit, so da&#223; nur in dem einen Extreme die Freiheit des Begriffs als sein Zusammenschlie&#223;en mit sich selbst gesetzt ist.

$$
  Logik \stackrel{Natur}{\longrightarrow} Geist
$$

> PG&#167;576 Diese Erscheinung ist im zweiten Schl&#252;sse insoweit aufgehoben, als dieser bereits der Standpunkt des Geistes selbst ist, welcher das Vermittelnde des Prozesses ist, die Natur voraussetzt und sie mit dem Logischen zusammenschlie&#223;t. Es ist der Schlu&#223; der geistigen Reflexion in der Idee; die Wissenschaft erscheint als ein subjektives Erkennen, dessen Zwecks die Freiheit und es selbst der Weg ist, sich dieselbe hervorzubringen.

> &#167;577 Der dritte Schlu&#223; ist die Idee der Philosophie, welche die sich wissende Vernunft, das Absolut-Allgemeine zu ihrer Mitte hat, die sich in Geist und Natur entzweit, jenen zur Voraussetzung als den Proze&#223; der subjektiven T&#228;tigkeit der Idee und diese zum allgemeinen Extreme macht, als den Proze&#223; der an sich, objektiv, seienden Idee. Das Sich-Urteilen der Idee in die beiden Erscheinungen (&#167; 575/6) bestimmt dieselben als ihre (der sich wissenden Vernunft) Manifestationen, und es vereinigt sich in ihr, da&#223; die Natur der Sache, der Begriff, es ist, die sich fortbewegt und entwickelt, und diese Bewegung ebensosehr die T&#228;tigkeit des Erkennens ist, die ewige an und f&#252;r sich seiende Idee sich ewig als absoluter Geist bet&#228;tigt, erzeugt und genie&#223;t.[394]


## **References**

Text with background, introduction and survey include

* [[Paul Redding]],  [section 3.2](http://plato.stanford.edu/entries/hegel/#SciLog) of _Georg Wilhelm Friedrich Hegel_, The Stanford Encyclopedia of Philosophy (Winter 2013 Edition), Edward N. Zalta (ed.) ([web](http://plato.stanford.edu/archives/win2013/entries/hegel/))

* {#Houlgate06} [[Stephen Houlgate]], _The opening of Hegel's Logic_, Purdue University Press, 2006 ([pdf](http://www.magonzalezvalerio.com/Houlgate,%20Stephen%20%20-%20The%20Opening%20of%20Hegel%27s%20Logic_From%20Being%20to%20Infinity%20-%20Purdue%20University%20Press.pdf))

* {#CarlsonMeasure} [[David Carlson]], _Hegel's theory of measure_ ([web](http://papers.ssrn.com/sol3/papers.cfm?abstract_id=413602))

* {#CarlsonActual} [[David Carlson]], _Hegel and what is actual_ ([pdf](http://www.hegel.net/carlson/Carlson2005-Hegel%20and%20What%20is%20Actual.pdf))

* [[Richard Dien Winfield]], _Lecture Course in Hegel's Science of Logic_ ([web](https://archive.org/details/LectureCourseInHegelsScienceOfLogic-RichardDienWinfield))

A quick survey of the theme of the idea expressing itself via the spirit in nature is in

* {#PSEJul14} musingsofacigarettesmokingman, _[P.SE comment](http://philosophy.stackexchange.com/a/14554/5473)_, July 2014

Hegel himself expands on the relation of the _Science of Logic_ to the [[Tao Te Ching]] in

* {#Hegel27} [[Georg Hegel]], Lectures on the Philosophy of Religion. Volume II: Determinate Religion. Edited by Peter C. Hodgson; translated by R.F. Brown, P.C. Hodgson, and J.M. Stewart, with the assistance of J.P. Fitzer and H.S. Harris. Berkeley: University of California Press, 1995 (orig. 1987). (Translation of: Vorlesungen &#252;ber die Philosophie der Religion.)  This extract (pp. 556-561) is from the Lectures of 1827; A. Immediate Religion, or Nature Religion; 1. The Religion of Magic; c. The State Religion of the Chinese Empire and the Dao. ([web](http://www.autodidactproject.org/quote/hegel-tao1.html))

Further comments on Hegel's text include

* {#Heidegger58} [[Martin Heidegger]], _Hegel and the Greeks_, Conference of the Academy of Sciences at Heidelberg, July 26, 1958 ([web](http://www.morec.com/hegelgre.htm))
  

* {#Inwood1983} Inwood, _Hegel_, 1983

* {#Lambek82} [[Joachim Lambek]], _The Influence of Heraclitus on Modern Mathematics_, In _Scientific Philosophy Today: Essays in Honor of Mario Bunge_, edited by Joseph Agassi and Robert S Cohen, 111&#8211;21. Boston: D. Reidel Publishing Co.

Comments on the general aim of a fundamental logic based on [[dialectic]] are in

* {#Wandschneider99} [[Dieter Wandschneider]], _Dialektik als Letztbegr&#252;ndung der Logik_, in Koreanische Hegelgesellschaft (ed.), _Festschrift f&#252;r Sok-Zin Lim_ Seoul 1999, 255&#8211;278 ([pdf](http://www.philosophie.rwth-aachen.de/global/show_document.asp?id=aaaaaaaaaabpltw))

Comments on the similarity of Hegel's physics to aspects of [[general relativity]] are in 

* {#Wandschneider82} [[Dieter Wandschneider]], _Raum, Zeit, Relativit&#228;t_m 1982 [web](http://www.klostermann.de/Wandschneider-Raum-Zeit-Relativitaet)

and the idea of matter emerging from space and time has apparently influenced

* {#Weyl19} [[Hermann Weyl]], _Raum, Zeit,Materie_, 1919 ([web](https://archive.org/details/raumzeitmateriev00weyl))

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