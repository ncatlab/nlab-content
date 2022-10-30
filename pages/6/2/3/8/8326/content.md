
{:formalization: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


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

Here the _objective logic_ is not quite _[[logic]]_ in the usual sense, but rather something like _[[logos]]_ in the old sense of [[Heraclitus]] (e.g. ([Heidegger 58](#Heidegger58))) or the _[[Nous]]_ in the sense of [[Anaxagoras]] ([&#167;54](#54)) or _[[metaphysics]]_ ([&#167;85](#85)). Something closer to the usual notion of logic is what Hegel calls the "subjective logic", though of course he also talks about both being the same.

Note that Hegel included an abbreviated version of _The Science of Logic_ as the first part of _The Encyclopedia of the Philosophical Sciences_, followed there by _The Philosophy of Nature_ and _The Philosophy of Mind_. This first part is often referred to as the _Shorter Logic_. 

* _Enzyklop&#228;die der philosophischen Wissenschaften im Grundrisse_ (1830) W. Bonsiepen und H.-C. Lucas (eds.) in _Gesammelte Werke_, Rheinisch-Westf&#228;lischen Akademie der Wissenschaften, and xx. Hamburg: Felix Meiner, 1992 ( Bonsiepen/Lucas 1992).

  [Encyclopedia of the Philosophical Sciences in Basic Outline, Part I: Science of Logic](http://ndpr.nd.edu/news/24778-encyclopedia-of-the-philosophical-sciences-in-basic-outline-part-i-science-of-logic/)
 {#EPSBOI}

> With Hegel you're getting what seems to us today a curious package. The whole dynamic (or '[[dialectic]]') of the unfolding of the [[logos|Logik]] is prior to any actual thinking, realised in concrete humans. In fact, the world, and that part of it which is human thought, is the Idea (or Spirit) realising itself. I say 'curious', but in a way I'm hearing echoes of this in things Urs is suggesting, as though the universe worked itself out according to [[type theory]]. For Hegel one isn't to be a Kantian, where what one theorises about the universe is just how the universe is taken up by the human understanding, with the further idea that this will be limited in certain ways, e.g., no access to the thing-in-itself. For Hegel, the human mind itself is part of the universe and as such part of the unfolding of the Idea/Spirit. $[\cdots]$ It's a dizzying picture which tends either to delight or revolt people. $[$ See at _[[absolute idealism]]_ $]$ ([Corfield](http://nforum.mathforge.org/discussion/4117/the-wiki-history-of-the-universe/?Focus=34343#Comment_34343))


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

For instance for the [points-to-pieces transform](cohesive%20topos#CanonicalComparison) induced by the [[shape modality]] $\dashv$ [[flat modality]] dichotomy $\int \dashv \flat$,
we have, as discussed at [tangent cohesion -- Cohesive and differential refinement](#tangent+cohesive+%28∞%2C1%29-topos#CohesiveAndDifferentialRefinement)

$$
  \array{
    &&  \int_{dR} \Omega A && \longrightarrow && \flat_{dR}\Sigma A
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{\theta_A}} && \searrow
    \\
    \flat \int_{dR} \Omega A  && && A && && \int \flat_{dR}\Sigma A
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow_{\mathrlap{\int \theta_A}}
    \\
    && \flat A && \longrightarrow && \int A
  }
  \,,
$$

### Formalization dictionary

[[Hegel]]'s "Science of Logic" may seem rather mysterious. Over the decades, [[William Lawvere]] had suggested, more or less explicitly, that parts of it are usefully understood as being about -- or conversely as being formalized and hence interpreted by -- aspects of [[categorical logic]]. For instance Lawvere suggested that the recurring notion of "unity and identity of opposites" is usefully thought of in terms of certain [[adjunctions]], as discussed in _[Formalization of Unity of Opposites](#OppositesAndUnity)_.

In view of this one may notice that modern [[foundations]] of [[constructive mathematics]] via [[type theory]] and in particular via [[homotopy type theory]] may offer more opportunities like this to give Hegel's intuitions a formalized home or incarnation in a useful way. 

The following table lists proposals for possible such identifications. The content below means to provide for each keyword commented passages in _Science of Logic_ to support this identification and illuminate it. But of course this remains just a proposal and subject at least to debate.

| Hegel's logic |  [[modal type theory|modal]] [[homotopy type theory]] |
|-----|------|
| moment | [[modality]] |
| unity of opposites |  [[adjoint modality]] |
| ground | [[antecedent]] |
| entering into existence | [[term introduction]] |
| immediacy of reflection | reflector term in [[identity type]] |
| all things are different | [[intensional identity]] |
| [[being]], One  | ([[context]] of) [[unit type]] |
| [[nothing]] | [[empty type]] |
| [[becoming]] | [[adjoint modality]]  $\emptyset \dashv \ast$ |
| moment of repulsion | [[flat modality]] $\flat$ |
| moment of attraction | [[cohesion]], [[shape modality]] $\int$ |
| quality/dasein | [[adjoint modality]] attraction $\dashv$ repulsion = $\int \dashv \flat$ | 
| moment of discreteness | [[flat modality]] $\flat$ |
| moment of continuity | [[sharp modality]] $\sharp$ |
| quantity | [[adjoint modality]] $\flat \dashv \sharp$ |
| vanishing of infinitesimals | [[reduction modality]] |
| being-for-self | [[reduction modality]] $Red$ |
| being-for-one | [[infinitesimal shape modality]] $\int_{inf}$ |
| ideality | [[adjoint modality]] $Red \dashv \int_{inf}$ | 
| reality | [[adjoint modality]] $\int_{inf} \dashv \flat_{inf}$ | 
| moment of two negations | [[double negation modality]] $\not \not$, more generally: [[bracket type]]/[[n-truncation modality|(-1)-truncation modality]] |
| something | [[n-truncation modality|(-1)-truncation modality]], classically [[double negation modality]] |
| measure (= [[gauge field|gauge]]) | quality $\dashv$ quantity |

Notice that the above involves the first two stages in the tower
of [[n-truncation modalities]]:

| $n$ | [[n-truncation modality]] |
|--|--|
| -2 | [[unit type]] modality |
| -1 | [[n-truncation modality|(-1)-truncation modality]], [[classical logic|classically]] [[double negation modality]] |

### On the translation of the terms

The orginal German is at times maybe more evocative than the established English translations 

* "f&#252;r sich sein", which standard sources translate as "being-for-self", really means to be alone and undisturbed. One says: "Ich gehe jetzt in mein B&#252;ro, ich muss mal f&#252;r mich sein um mich zu konzentrieren." (I'll retreat to my office to be alone and undisturbed.)

* "f&#252;r eins sein" which Hegel uses, is not proper German and probably wasn't even at his time, but it is clearly meant to rhyme with "f&#252;r sich sein", and the similar phrase that does exist is "f&#252;r einander sein", which means: to be available for others.

* "Dasein", which in the standard translations appears as "determinate being" is really much more immediate "being there", "existing". "Wann sollen wir da sein?" means "When are we supposed to be there?" In more formal speach "das Dasein" means "existence" as in "Ach, das Dasein ist doch zwecklos."

(...)


## **Introduction**

### Allgemeiner Begriff der Logik


* {#53} &#167;53 Die Logik ist sonach als das System der reinen Vernunft, als das Reich des reinen Gedankens zu fassen. Dieses Reich ist die Wahrheit, wie sie ohne H&#252;lle an und f&#252;r sich selbst ist. Man kann sich deswegen ausdr&#252;cken, da&#223; dieser Inhalt die Darstellung Gottes ist, wie er in seinem ewigen Wesen vor der Erschaffung der Natur und des endlichen Geistes ist.


* &#167;53 Accordingly, logic is to be understood as the system of pure reason, as the realm of pure thought. This realm is truth as it is without veil and in its own absolute nature. It can therefore be said that this content is the exposition of God as he is in his eternal essence before the creation of nature and a finite mind.

* {#54} &#167;54 Anaxagoras wird als derjenige gepriesen, der zuerst den Gedanken ausgesprochen habe, da&#223; der Nus, der Gedanke, das Princip der Welt, da&#223; das Wesen der Welt als der Gedanke bestimmt ist. Er hat damit den Grund zu einer Intellektualansicht des Universums gelegt, deren reine Gestalt die Logik seyn mu&#223;. Es ist in ihr nicht um ein Denken &#252;ber etwas, das f&#252;r sich au&#223;er dem Denken zu Grunde l&#228;ge, zu thun, um Formen, welche blo&#223;e Merkmale der Wahrheit abgeben sollten; sondern die nothwendigen Formen und eigenen Bestimmungen des Denkens sind der Inhalt und die h&#246;chste Wahrheit selbst.

* &#167;54 Anaxagoras is praised as the man who first declared that Nous, thought, is the principle of the world, that the essence of the world is to be defined as thought. In so doing he laid the foundation for an intellectual view of the universe, the pure form of which must be logic. What we are dealing with in logic is not a thinking about something which exists independently as a base for our thinking and apart from it, nor forms which are supposed to provide mere signs or distinguishing marks of truth; on the contrary, the necessary forms and self-consciousness of thought are the content and the ultimate truth itself.


### Allgemeine Einteilung der Logik

* {#85} &#167;85 Die objektive Logik tritt damit vielmehr an die Stelle der vormaligen Metaphysik, als welche das wissenschaftliche Geb&#228;ude &#252;ber die Welt war, das nur durch Gedanken aufgef&#252;hrt seyn sollte.&#8212;Wenn wir auf die letzte Gestalt der Ausbildung dieser Wissenschaft R&#252;cksicht nehmen, so ist erstens unmittelbar die Ontologie, an deren Stelle die objektive Logik tritt,&#8212;der Theil jener Metaphysik, der die Natur des Ens &#252;berhaupt erforschen sollte;&#8212;das Ens begreift sowohl Seyn als Wesen in sich, f&#252;r welchen Unterschied unsere Sprache gl&#252;cklicherweise den verschiedenen Ausdruck gerettet hat.&#8212;Alsdann aber begreift die objektive Logik auch die &#252;brige Metaphysik insofern in sich, als diese mit den reinen Denkformen die besondern, zun&#228;chst aus der Vorstellung genommenen Substrate, die Seele, die Welt, Gott, zu fassen suchte, und die Bestimmungen des Denkens das Wesentliche der Betrachtungsweise ausmachten. 

* &#167;85 The objective logic, then, takes the place rather of the former metaphysics which was intended to be the scientific construction of the world in terms of thoughts alone. If we have regard to the final shape of this science, then it is first and immediately ontology whose place is taken by objective logic &#8212; that part of this metaphysics which was supposed to investigate the nature of ens in general; ens comprises both being and essence, a distinction for which the German language has fortunately preserved different terms. But further, objective logic also comprises the rest of metaphysics in so far as this attempted to comprehend with the forms of pure thought particular substrata taken primarily from figurate conception, namely the soul, the world and God; and the determinations of thought constituted what was essential in the mode of consideration. 

## **Book one** Die Lehre vom Sein / The Doctrine of Being

### $\;\;$ Womit muss der Anfang der Wissenschaft gemacht werden?


* {#121} &#167;121 Was somit &#252;ber das Seyn ausgesprochen oder enthalten seyn soll, in den reicheren Formen des Vorstellens von Absolutem oder Gott, die&#223; ist im Anfange nur leeres Wort, und nur Seyn; die&#223; Einfache, das sonst keine weitere Bedeutung hat, die&#223; Leere ist also schlechthin der Anfang der Philosophie.

* &#167;121 Consequently, whatever is intended to be expressed or implied beyond being, in the richer forms of representing the absolute or God, this is in the beginning only an empty word and only being; this simple determination which has no other meaning of any kind, this emptiness, is therefore simply as such the beginning of philosophy.

* &#167;122 Diese Einsicht ist selbst so einfach, da&#223; dieser Anfang als solcher, keiner Vorbereitung noch weiteren Einleitung bedarf; und diese Vorl&#228;ufigkeit von Raisonnement &#252;ber ihn konnte nicht die Absicht haben, ihn herbeizuf&#252;hren, als vielmehr alle Vorl&#228;ufigkeit zu entfernen.

* &#167;122 This insight is itself so simple that this beginning as such requires no preparation or further introduction; and, indeed, these preliminary, external reflections about it were not so much intended to lead up to it as rather to eliminate all preliminaries.



### $\;\;$ Allgemeine Einteilung des Seins


### First section: Determinateness (Quality)

#### First chapter

From The Shorter Logic:
* &#167;86 Pure [[being]] constitutes the beginning, because it is pure thought as well as the undetermined, simple immediate, and the first beginning cannot be anything mediated and further determined.

* &#167;87 Now this pure being is a pure abstraction and thus the absolutely negative which, when likewise taken immediately, is nothing.

* &#167;88 Conversely, nothing, as this immediate, self-same category, is likewise the same as being. The truth of being as well as of nothing is therefore the unity of both; this unity is [[becoming]].


##### A. Being
 {#OnBeingAndBecoming}

* &#167;132 Being, pure being, [...] it has no diversity within itself nor any with a reference outwards.



This is the _[[unit type]]_ $\ast$. 


Indeed, later this is called "Das Eins"  which is maybe indeed better translated as "The Unit" instead of as "The One" as commonly done.


##### B. Nothing

* &#167;133 Nothing, pure nothing: it is simply equality with itself, complete emptiness,

The [[empty type]] $\emptyset$.


##### C. Becoming
 {#Becoming}

* &#167;134 Pure Being and pure nothing are, therefore, the same. What is the truth is neither being nor nothing, but that being &#8212; does not pass over but has passed over &#8212; into nothing, and nothing into being. But it is equally true that they are not undistinguished from each other, that, on the contrary, they are not the same, that they are absolutely distinct, and yet that they are unseparated and inseparable and that each immediately vanishes in its opposite. Their truth is therefore, this movement of the immediate vanishing of the one into the other: becoming, a movement in which both are distinguished, but by a difference which has equally immediately resolved itself.

According to the formalization of such [[unity of opposites]] as
[above](#OppositesAndUnity) we might think of this as the
universal factorization

$$
  \array{
    \emptyset &\longrightarrow& X &\longrightarrow& \ast 
    \\
    \\
    nothing && becoming && being
  }
$$

of the factorization of the unique [[function]] from the [[empty type]] to the [[unit type]] through any other [[type]] $X$.


Indeed, later it says:

* &#167;174 there is nothing which is not an intermediate state between being and nothing.

Also, [below](#SomethingAndAnOther) it says

* &#167;222 Being and nothing in their unity, which is determinate being

and "determinate being" / Dasein seems to be well interpreted with types expressed as

$$
  \vdash X \colon Type
  \,.
$$


###### 1. Unity of Being and Nothing

###### $\;\;$ Remark 1 The opposition  of being and nothing in ordinary thinking

###### $\;\;$ Remark 2: Defectiveness of the Expression "Unity, Identity of Being and Nothing"

* &#167;152  But the third in which being and nothing subsist must also present itself here, and it has done so; it is becoming. In this being and nothing are distinct moments; becoming only is, in so far as they are distinguished.

In view of the above it seems that "moment" is well translated with _[[modality]]_.

###### $\;\;$ Remark 3 The isolating of these abstractions

###### $\;\;$ Remark 4 Incomprehensibility of the beginning

* &#167;171 It is impossible for anything to begin, either in so far as it is, or in so far as it is not; for in so far as it is, it is not just beginning, and in so far as it is not, then also it does not begin. If the world, or anything, is supposed to have begun, then it must have begun in nothing, but in nothing &#8212; or nothing &#8212; is no beginning; for a beginning includes within itself a being, but nothing does not contain any being. Nothing is only nothing. In a ground, a cause, and so on, if nothing is so determined, there is contained an affirmation, a being. For the same reason, too, something cannot cease to be; for then being would have to contain nothing, but being is only being, not the contrary of itself.

* &#167;174 The foregoing dialectic is the same, too, as that which understanding employs the notion of infinitesimal magnitudes, given by higher analysis. A more detailed treatment of this notion will be given later. These magnitudes have been defined as such that they are in their vanishing, not before their vanishing, for then they are finite magnitudes, or after their vanishing, for then they are nothing. 

Vanishing of [[infinitesimal objects]] is expressed by the [[reduction modality]] $Red$.

* &#167;174 there is nothing which is not an intermediate state between being and nothing.

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

* {#176} &#167;176 Das Werden, Entstehen und Vergehen, ist die Ungetrenntheit des Seyns und Nichts; nicht die Einheit, welche vom Seyn und Nichts abstrahirt; sondern als Einheit des Seyns und Nichts ist es diese bestimmte Einheit, oder in welcher sowohl Seyn als Nichts ist. Aber indem Seyn und Nichts, jedes ungetrennt von seinem Anderen ist, ist es nicht. Sie sind also in dieser Einheit, aber als verschwindende, nur als Aufgehobene. Sie sinken von ihrer zun&#228;chst vorgestellten Selbstst&#228;ndigkeit zu Momenten herab, noch unterschiedenen, aber zugleich aufgehobenen.

* {#176} &#167;176 Becoming is the unseparatedness of being and nothing, not the unity which abstracts from being and nothing; but as the unity of being and nothing it is this determinate unity in which there is both being and nothing. But in so far as being and nothing, each unseparated from its other, is, each is not. They are therefore in this unity but only as vanishing, sublated moments. They sink from their initially imagined self-subsistence to the status of moments, which are still distinct but at the same time are sublated.

* {#177} &#167;177 Nach dieser ihrer Unterschiedenheit sie aufgefa&#223;t, ist jedes in derselben als Einheit mit dem Anderen. Das Werden enth&#228;lt also Seyn und Nichts als zwei solche Einheiten, deren jede selbst Einheit des Seyns und Nichts ist; die eine das Seyn als unmittelbar und als Beziehung auf das Nichts; die andere das Nichts als unmittelbar und als Beziehung auf das Seyn; die Bestimmungen sind in ungleichem Werthe in diesen Einheiten.

* {#177} &#167;177 Grasped as thus distinguished, each moment is in this distinguishedness as a unity with the other. Becoming therefore contains being and nothing as two such unities, each of which is itself a unity of being and nothing; the one is being as immediate and as relation to nothing, and the other is nothing as immediate and as relation to being; the determinations are of unequal values in these unities.


An archetypical description of the [[unity of opposites]]. Here:

[[becoming]]/Werden : [[nothing]] $\dashv$ [[being]] 

$\;\;\;$ [[empty type]] $\dashv$ [[unit type]]

$\;\;\;$ $\emptyset \dashv \ast$


$$
  \emptyset \longrightarrow X \longrightarrow \ast
$$

* {#178} &#167;178 Das Werden ist auf diese Weise in gedoppelter Bestimmung; in der einen ist das Nichts als unmittelbar, d. i. sie ist anfangend vom Nichts, das sich auf das Seyn bezieht, das hei&#223;t, in dasselbe &#252;bergeht, in der anderen ist das Seyn als unmittelbar d. i. sie ist anfangend vom Seyn, das in das Nichts &#252;bergeht,&#8212;Entstehen und Vergehen.

* {#178} &#167;178 Becoming is in this way in a double determination. In one of them, nothing is immediate, that is, the determination starts from nothing which relates itself to being, or in other words changes into it; in the other, being is immediate, that is, the determination starts from being which changes into nothing: the former is coming-to-be and the latter is ceasing-to-be.
 
$\;\;$ [[nothing]] $\dashv$ [[being]]  $\;\colon\;$ [[ceasing]]/




###### 3. Sublating of Becoming

* &#167;180 The resultant equilibrium of coming-to-be and ceasing-to-be is in the first place becoming itself. But this equally settles into a stable unity. Being and nothing are in this unity only as vanishing moments; yet becoming as such is only through their distinguishedness. Their vanishing, therefore, is the vanishing of becoming or the vanishing of the vanishing itself. Becoming is an unstable unrest which settles into a stable result.

* &#167;181 This could also be expressed thus: becoming is the vanishing of being in nothing and of nothing in being and the vanishing of being and nothing generally; but at the same time it rests on the distinction between them. It is therefore inherently self-contradictory, because the determinations it unites within itself are opposed to each other; but such a union destroys itself.

* &#167;182 This result is the vanishedness of becoming, but it is not nothing; as such it would only be a relapse into one of the already sublated determinations, not the resultant of nothing and being. It is the unity of being and nothing which has settled into a stable oneness. But this stable oneness is being, yet no longer as a determination on its own but as a determination of the whole.

* &#167;183 Becoming, as this transition into the unity of being and nothing, a unity which is in the form of being or has the form of the onesided immediate unity of these moments, is determinate being.

| |  | [[Dasein]] | |  |
|--|--|--|--|--|
| [[Werden]] : | [[Nichts]] | $\;\;\;\dashv$ | [[Sein]] | : [[Vergehen]] |

$\,$

| |  | [[Dasein]] | |  |
|--|--|--|--|--|
| [[becoming]] : | [[nothing]] | $\;\;\;\dashv$ | [[being]] | : [[ceasing]] |



* &#167;187 The more precise meaning and expression which being and nothing receive, now that they are moments, is to be ascertained from the consideration of determinate being as the unity in which they are preserved. Being is being, and nothing is nothing, only in their contradistinction from each other; but in their truth, in their unity, they have vanished as these determinations and are now something else. Being and nothing are the same; but just because they are the same they are no longer being and nothing, but now have a different significance. In becoming they were coming-to-be and ceasing-to-be; in determinate being, a differently determined unity, they are again differently determined moments. This unity now remains their base from which they do not again emerge in the abstract significance of being and nothing.

moment $\leftrightarrow$ [[modality]]

#### Second chapter. Deasein / Determinate Being 

* {#188} &#167;188 Daseyn ist bestimmtes Seyn; seine Bestimmtheit ist seyende Bestimmtheit, Qualit&#228;t.

* &#167;188 In considering determinate being the emphasis falls on its determinate character; the determinateness is in the form of being, and as such it is quality.


* &#167;188 In considering determinate being the emphasis falls on its determinate character; the determinateness is in the form of being, and as such it is quality.

##### A. Dasein as such / Determinate being as such

*  &#167;188 In considering determinate being the emphasis falls on its determinate character; the determinateness is in the form of being, and as such it is quality. Through its quality, something is determined as opposed to an other, as alterable and finite; and as negatively determined not only against an other but also in its own self. This its negation as at first opposed to the finite something is the infinite; the abstract opposition in which these determinations appear resolves itself into the infinity which is free from the opposition, into being-for-self.

The first sentence here is made up by the translator, in the original it says:

* Daseyn ist bestimmtes Seyn;



###### a. Dasein &#252;berhaupt / Determinant being in general


* &#167;191 From becoming there issues determinate being, which is the simple oneness of being and nothing.

Above we saw that _becoming_ is formalized by the universal [[unity of opposites]] of $\emptyset \dashv \ast$, exhibiting any [[type]] $X$

$$
  \emptyset \longrightarrow X \longrightarrow \ast
  \,.
$$

So determinate being/Dasein is that of [[types]].

&#167; 191 From becoming there issues determinate being, which is the simple oneness of being and nothing. Because of this oneness it has the form of immediacy. Its mediation, becoming, lies behind it; it has sublated itself and determinate being appears, therefore, as a first, as a starting-point for the ensuing development. It is first of all in the one-sided determination of being; the other determination, nothing, will likewise display itself and in contrast to it.


###### b. Qualit&#228;t / Quality

* &#167;196 Determinateness thus isolated by itself in the form of being is quality 

[[type]]

###### c. Etwas / Something
 {#Etwas}

* &#167;208 In determinate being its determinateness has been distinguished as quality; in quality as determinately present, there is distinction &#8212; of reality and negation. Now although these distinctions are present in determinate being, they are no less equally void and sublated. Reality itself contains negation, is determinate being, not indeterminate, abstract being. Similarly, negation is determinate being, not the supposedly abstract nothing but posited here as it is in itself, as affirmatively present [als seiend], belonging to the sphere of determinate being. 

  Thus quality is completely unseparated from determinate being, which is simply determinate, qualitative being.

[[Dasein]], quality, [[type]], something

* &#167;209 This sublating of the distinction is more than a mere taking back and external omission of it again, or than a simple return to the simple beginning, to determinate being as such. The distinction cannot be omitted, for it is. What is, therefore, in fact present is determinate being in general, distinction in it, and sublation of this distinction; determinate being, not as devoid of distinction as at first, but as again equal to itself through sublation of the distinction, the simple oneness of determinate being resulting from this sublation. This sublatedness of the distinction is determinate being's own determinateness; it is thus being-within-self: determinate being is a determinate being, a something.

* &#167;209 Die&#223; Aufgehobenseyn des Unterschieds ist die eigne Bestimmtheit des Daseyns; so ist es Insichseyn; das Daseyn ist Daseyendes, Etwas.

* &#167;210 Something is the first negation of negation, as simple self-relation in the form of being.

* &#167;211 Something is the negation of the negation in the form of being;

* &#167; 212 This mediation with itself which something is in itself, taken only as negation of the negation, has no concrete determinations for its sides; it thus collapses into the simple oneness which is being.


Here "double negation" is plausibly matched with the [[double negation modality]].

Concerning "something": if $X$ is a [[type]], then by [[propositions-as-types]] there is _something_ of this type if the type is [[inhabited]]. But [[classical logic|classically]] this is expressed by by its [[double negation modality]]. Hence: there is something of some quality/type if that is a double-negation [[modal type]].


##### B. Die Endlichkeit / Finitude.

###### a. Etwas und ein Anderes. / Something and an Other
 {#SomethingAndAnOther}

* &#167;221  Being-for-other and being-in-itself constitute the two moments of the something.

something : Being-for-other $\dashv$ being-in-itself

* &#167;222 Being and nothing in their unity, which is determinate being

Notice that [above](#Becoming) this [[unity of opposites|unity]] is called _[[becoming]]_.

* Die&#223; f&#252;hrt zu einer weitern Bestimmung. Ansichseyn und Seyn-f&#252;r-Anderes sind zun&#228;chst verschieden; aber da&#223; Etwas dasselbe, was es an sich ist, auch an ihm hat, und umgekehrt, was es als Seyn-f&#252;r-Anderes ist, auch an sich ist,&#8212;die&#223; ist die Identit&#228;t des Ansichseyns und Seyns-f&#252;r-Anderes, nach der Bestimmung, da&#223; das Etwas selbst ein und dasselbe beider Momente ist, sie also ungetrennt in ihm sind.&#8212;Es ergiebt sich formell diese Identit&#228;t schon in der Sph&#228;re des Daseyns, aber ausdr&#252;cklicher in der Betrachtung des Wesens und dann des Verh&#228;ltnisses der Innerlichkeit und &#196;u&#223;erlichkeit, und am bestimmtesten in der Betrachtung der Idee, als der Einheit des Begriffs und der Wirklichkeit.

##### C. Die Unendlichkeit

###### a. Das Unendliche &#220;berhaupt

###### b. Wechselwirkung des Endlichen und Unendlichen

###### c. Die affirmative Unendlichkeit

###### Der &#220;bergang

* Die Idealit&#228;t kann die Qualit&#228;t der Unendlichkeit genannt werden; aber sie ist wesentlich der Proce&#223; des Werdens und damit ein &#220;bergang, wie des Werdens in Daseyn, der nun anzugeben ist. Als Aufheben der Endlichkeit, d. i. der Endlichkeit als solcher und ebenso sehr der ihr nur gegen&#252;berstehenden, nur negativen Unendlichkeit ist diese R&#252;ckkehr in sich, Beziehung auf sich selbst, Seyn. Da in diesem Seyn Negation ist, ist es Daseyn, aber da sie ferner wesentlich Negation der Negation, die sich auf sich beziehende Negation ist, ist sie das Daseyn, welches F&#252;rsichseyn genannt wird.

Compare "ideality is quality of the infinite" with


$$
  \array{
    quality \colon \int \dashv \flat
    \\
    ideality \colon Red \dashv \int_{inf}
  }
$$


#### Third chapter. Das F&#252;rsichsein / Being for self

* {#318} &#167;318 Im F&#252;rsichseyn ist das qualitative Seyn vollendet;

* &#167;318 In being-for-self, qualitative being finds its consummation;

* &#167;319 Being-for-self is first, immediately a being-for-self &#8212; the One.

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
    quality : & \int &\dashv& \flat
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

* {#321} &#167;321 Das F&#252;rsichseyn ist, wie schon erinnert ist, die in das einfache Seyn zusammengesunkene Unendlichkeit; es ist Daseyn, insofern die negative Natur der Unendlichkeit, welche Negation der Negation ist, in der nunmehr gesetzten Form der Unmittelbarkeit des Seyns, nur als Negation &#252;berhaupt, als einfache qualitative Bestimmtheit ist.

* &#167;321 But being, which in such determinateness is determinate being, is also at once distinct from being-for-self, which is only being-for-self in so far as its determinateness is the infinite one above-mentioned; nevertheless, determinate being is at the same time also a moment of being-for-self; for this latter, of course, also contains being charged with negation. Thus the determinateness which in determinate being as such is an other, and a being-for-other, is bent back into the infinite unity of being-for-self, and the moment of determinate being is present in being-for-self as a being-for-one.

###### b. Sein-f&#252;r-Eines / Being-for-one

* &#167;322 To be 'for self' and to be 'for one' are therefore not different meanings of ideality, but are essential, inseparable moments of it.


###### Anmerkung

* &#167;324 Die Idealit&#228;t kommt zun&#228;chst den aufgehobenen Bestimmungen zu, als unterschieden von dem, worin sie aufgehoben sind, das dagegen als das Reelle genommen werden kann. So aber ist das Ideelle wieder eins der Momente und das Reale das andere; 

* &#167;324 But thus the ideal is again one of the moments, and the real the other;

hence another [[unity of opposites]] is $ideality \dashv reality$.

$$
  \array{
    & \text{f&#252;r sich sein} && \text{f&#252;r eins sein}
    \\
    ideality & Red &\dashv& \int_{inf}
    \\
    & \bot && \bot
    \\
    reality & \int_{inf} &\dashv& \flat_{inf}
  }
$$

See also at _[The One and the Many](#EinsUndVieles)_.

###### c. Eins

* &#167;328 Being-for-self is the simple unity of itself and its moment, being-for-one.

* &#167;329 The moments which constitute the Notion of the one as a being-for-self fall asunder in the development. They are: (1) negation in general, (2) two negations, (3) two that are therefore the same, (4) sheer opposites, (5) self-relation, identity as such, (6) relation which is negative and yet to its own self.

If we translate "moment" as [[modality]] then here the 
[[double negation modality]] comes to mind.

Notice that the [[empty type]] and the [[unit type]] are the [[modal types]] for the [[double negation modality]].

##### B. Eins und Vieles. / The One and the Many
 {#EinsUndVieles}

* Die Idealit&#228;t des F&#252;rsichseyns als Totalit&#228;t schl&#228;gt so f&#252;rs erste in die Realit&#228;t um, und zwar in die festeste, abstrakteste, als Eins.

###### a. Das Eins an ihm selbst

###### b. Das Eins und das Leere / The One and the Void

* &#167;335 The one is the void as the abstract relation of the negation to itself. 

###### $\;\;$ Remark: Atomism
 {#Atomism}

* &#167;337 The one in this form of determinate being is the stage of the category which made its appearance with the ancients as the atomistic principle, according to which the essence of things is the atom and the void.

Eins: [[atom]], [[infinitesimally thickened point]]

###### c. Viele Eins. Repulsion. / Many ones. Repulsion.

* &#167;340 The one and the void constitute the first stage of the determinate being of being-for-self. Each of these moments has negation for its determination and is at the same time posited as a determinate being; according to the former determination the one and the void are the relation of negation to negation as of an other to its other: the one is negation in the determination of being, and the void is negation in the determination of non-being.

Das Eins (the One): $\ast$ [[unit type]]

Das Leere (the void): $\emptyset$ [[empty type]] ( _leere Menge_ !)

Negation $(\not X) \coloneqq (X \to \emptyset)$

$\ast \simeq \not \emptyset$.

* &#167;342 the one repels itself from itself. The negative relation of the one to itself is repulsion.

* &#167;343 This repulsion as thus the positing of many ones but through the one itself, is the one's own coming-forth-from-itself but to such outside it as are themselves only ones. This is repulsion according to its Notion, repulsion in itself. The second repulsion is different from it, it is what is immediately suggested to external reflection: repulsion not as the generation of ones, but only as the mutual repelling of ones presupposed as already present. 


To see a formalization of "the one repels itself from itself",
suppose we have a [[shape modality]] $\int$ but without the assumption that it preserves finite product types. (This is what the term "[[shape of an (infinity,1)-topos|shape]]" really refers to).

Then given just the [[empty type]] $\emptyset$ and the [[unit type]] $\ast$, there is one new [[type]] to be formed (since necessarily $\int \emptyset \simeq \emptyset$) and this is

$$
  \int \ast 
$$

Below we see that this, being a [[discrete type]], is what Hegel describes with "repulsion": The points in $\int \ast$ do not attract/cohese, they are different and repel.

At the same time, being a [[discrete type]] it is necessarily a [[homotopy colimit]] of copies of the [[unit type]] (see [here](limit+in+a+quasi-category#Tensoring))

$$
  \int \ast \simeq \underset{\longrightarrow}{\lim}_I \ast
$$

where the [[diagram]] $I$ that the colimit is over is $I = &#643; \ast$ itself.

For a similar argument see Lawvere's  _[Cohesive toposes and Cantor's Lauter Einsen ](#LawvereLauterEinsen))_. On p. 6 there is suggested that the [[unity of opposites]] "all elements of a set are indistinguishable and yet distinct" is captured by the fact that both

$\flat X$ as well as $\sharp X$ have the same image under $\flat$.

###### $\;\;$ Remark: The Monad of Leibniz
 {#TheMonadOfLeibniz}

* &#167;348 We have previously referred to the [[Gottfried Leibniz|Leibnizian]] idealism. We may add here that this idealism which started from the ideating [[monad (disambiguation)|monad]], which is determined as being for itself, advanced only as far as the repulsion just considered, and indeed only to plurality as such, in which each of the ones is only for its own self and is indifferent to the determinate being and being-for-self of the others; or, in general, for the one, there are no others at all. The monad is, by itself, the entire closed universe; it requires none of the others. But this inner manifoldness which it possesses in its ideational activity in no way affects its character as a being-for-self. The Leibnizian idealism takes up the plurality immediately as something given and does not grasp it as a repulsion of the monads. Consequently, it possesses plurality only on the side of its abstract externality. 

  The atomistic philosophy does not possess the Notion of ideality; it does not grasp the one as an ideal being, that is, as containing within itself the two moments of being-forself and being-for-it, but only as a simple, dry, real being-for-self. 

  It does, however, go beyond mere indifferent plurality; the atoms become further determined in regard to one another even though, strictly speaking, this involves an inconsistency; whereas, on the contrary, in that indifferent independence of the monads, plurality remains as a fixed fundamental determination, so that the connection between them falls only in the monad of monads, or in the philosopher who contemplates them.

To summarize, in &#167;322 we get a clear prescription:

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

Notice that in [[superalgebra]] one says "[[soul]]" for these "antennas" and "[[body]]" for what remains. Therefore it seems plausible to conclude that the formalization of the [[unity of opposites]]

$$
  Ideality \;\colon\; BeingForSelf \dashv BeingForOne
$$

is the [[adjoint modality]] given by [[reduction modality]] $\dashv$ [[infinitesimal shape modality]]. The "Ideality" of infinitesimal extension gives the Eins, the atom-of-space, its dual character of containing a reduced point for-itself and at the same time an infinitesimal thickening that extends beyond that.



##### C. Repulsion und Attraktion

###### a. Ausschli&#223;en des Eins.

###### b. Das Eine Eins der Attraktion

###### c. Die Beziehung der Repulsion und der Attraktion


* &#167;369 Die Repulsion daseyender Eins ist die Selbsterhaltung des Eins durch die gegenseitige Abhaltung der andern, so da&#223; 1) die anderen Eins an ihm negirt werden, die&#223; ist die Seite seines Daseyns oder seines Seyns-f&#252;r-Anderes; diese ist aber somit Attraktion, als die Idealit&#228;t der Eins;&#8212;und da&#223; 2) das Eins an sich sey, ohne die Beziehung auf die andere; aber nicht nur ist das Ansich &#252;berhaupt l&#228;ngst in das F&#252;rsichseyn &#252;bergegangen, sondern an sich, seiner Bestimmung nach, ist das Eins jenes Werden zu Vielen.&#8212;Die Attraktion daseyender Eins ist die Idealit&#228;t derselben, und das Setzen des Eins, worin sie somit als Negiren und Hervorbringen des Eins sich selbst aufhebt, als Setzen des Eins das Negative ihrer selbst an ihr, Repulsion ist.

* &#167;369 The repulsion of the determinately existent ones is the self-preservation of the one through the mutual repulsion of the others, so that (1) the other ones are negated in it-this is the side of its determinate being or of its being-for-other; but this is thus attraction as the ideality of the ones; and (2) the one is in itself, without relation to the others; but not only has being-in-itself as such long since passed over into being-for-self, but the one in itself, by its determination, is the aforesaid becoming of many ones. The attraction of the determinately existent ones is their ideality and the positing of the one, in which, accordingly, attraction as a negating and a generating of the one sublates itself, and as a positing of the one is in its own self the negative of itself, repulsion.


* &#167;370 Damit ist die Entwickelung des F&#252;rsichseyns vollendet und zu ihrem Resultate gekommenen.

* &#167;370 With this, the development of being-for-self is completed and has reached its conclusion.

Since _Dasein_ and _F&#252;rsichsein_ both are qualitative being/are quality ([188](#188), [318](#318), [321](#321))  the above gives us the [[unity of opposites]]

$$
  quality \;\colon\; attraction \dashv repulsion
$$

###### Remark: The Kantian Construction of Matter from the Forces of Attraction and Repulsion


* &#167;374 Kant, as we know, constructed matter from the forces of attraction and repulsion, or at least he has, to use his own words, set up the metaphysical elements of this construction.

Not about actual [[forces]] in [[matter]] so much as about what makes the points in the [[continuum]] both stay apart (repulsion) and at the same time hang together (attraction/cohesion).




### Second section. The magnitude

#### First chapter. Die Quantit&#228;t / The quantity

##### A. Die reine Quantit&#228;t / Pure quantity
 {#PureQuantity}


* &#167;398 Quantity is the unity of these moments of continuity and discreteness

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

* &#167;395 Attraction is in this way the moment of continuity in quantity.

attraction is what holds stuff together, hence this is the idea of [[cohesion]]

if $X$ has continuity then the [[shape modality]] $\int X$ is the result of letting things collaps under their cohesion/attraction


###### On discreteness and repulsion
 {#OnDiscretenessAndRepulsion}

* &#167;397 In continuity, therefore, magnitude immediately possesses the moment of discreteness &#8212; repulsion, as now a moment in quantity. 

continuous object $X$ possesses moment 
of [[discrete object|discreteness]]= [[flat modality]] $\flat X$

* &#167;398 Quantity is the unity of these moments of continuity and discreteness,


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
    \flat X &\longrightarrow& X &\longrightarrow& \int X
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

* &#167;432 Space, time, matter, and so forth are continuous magnitudes 




##### C. Begrenzung der Quantit&#228;t 


#### Second chapter. Quantum


### Third section. The measure.
 {#TheMeasure}

* {#699} &#167;699 Im Maa&#223;e sind, abstrakt ausgedr&#252;ckt, Qualit&#228;t und Quantit&#228;t vereinigt.

* &#167;699 Abstractly expressed, in measure quality and quantity are united

[[unity of opposites]]

$$
  measure \colon quantity \dashv quality
$$

* &#167;703 The observation here made extends generally to those systems of pantheism which have been partially developed by thought. The first is being, the one, substance, the infinite, essence; in contrast to this abstraction the second, namely, all determinateness in general, what is only finite, accidental, perishable, non-essential, etc. can equally abstractly be grouped together; and this is what usually happens as the next step in quite formal thinking. But the connection of this second with the first is so evident that one cannot avoid grasping it as also in a unity with the latter;

#### A. The Specific Quantum

* {#714} &#167;714 Ein Maa&#223;, als Maa&#223;stab im gew&#246;hnlichen Sinne, ist ein Quantum, das als die an sich bestimmte Einheit gegen &#228;u&#223;erliche Anzahl willk&#252;rlich angenommen wird. Eine solche Einheit kann zwar auch in der That an sich bestimmte Einheit seyn, wie Fu&#223; und dergleichen urspr&#252;ngliche Maa&#223;e; insofern sie aber als Maa&#223;stab zugleich f&#252;r andere Dinge gebraucht wird, ist sie f&#252;r diese nur &#228;u&#223;erliches, nicht ihr urspr&#252;ngliches Maa&#223;.&#8212;So mag der Erddurchmesser, oder die Pendell&#228;nge, als specifisches Quantum f&#252;r sich genommen werden. Aber es ist willk&#252;rlich, den wievielsten Theil des Erddurchmessers oder der Pendell&#228;nge und unter welchem Breitengrade man diese nehmen wolle, um sie als Maa&#223;stab zu gebrauchen. Noch mehr aber ist f&#252;r andere Dinge ein solcher Maa&#223;stab etwas &#196;u&#223;erliches. Diese haben das allgemeine specifische Quantum wieder auf besondere Art specificirt, und sind dadurch zu besondern Dingen gemacht. Es ist daher th&#246;richt, von einem nat&#252;rlichen Maa&#223;stab der Dinge zu sprechen. Ohnehin soll ein allgemeiner Maa&#223;stab nur f&#252;r die &#228;u&#223;erliche Vergleichung dienen; in diesem oberfl&#228;chlichsten Sinne, in welchem er als allgemeines Maa&#223; genommen wird, ist es v&#246;llig gleichg&#252;ltig, was daf&#252;r gebraucht wird. Es soll nicht ein Grundmaa&#223; in dem Sinne seyn, da&#223; die Naturmaa&#223;e der besondern Dinge daran dargestellt und daraus nach einer Regel, als Specifikationen Eines allgemeinen Maa&#223;es, des Maa&#223;es ihres allgemeinen K&#246;rpers, erkannt w&#252;rden. Ohne diesen Sinn aber hat ein absoluter Maa&#223;stab nur das Interesse und die Bedeutung eines Gemeinschaftlichen, und ein solches ist nicht an sich, sondern durch &#220;bereinkommen ein Allgemeines.

* &#167;714 A measure taken as a standard in the usual meaning of the word is a quantum which is arbitrarily assumed as the intrinsically determinate unit relatively to an external amount. Such a unit can, it is true, also be in fact an intrinsically determinate unit, like a foot and suchlike original measures; but in so far as it is also used as a standard for other things it is in regard to them only an external measure, not their original measure. Thus the diameter of the earth or the length of a pendulum may be taken, each on its own account, as a specific quantum; but the selection of a particular fraction of the earth's diameter or of the length of the pendulum, as well as the degree of latitude under which the latter is to be taken for use as a standard, is a matter of choice. But for other things such a standard is still more something external. These have further specified the general specific quantum in a particular way and have thereby become particular things. It is therefore foolish to speak of a natural standard of things. Moreover, a universal standard ought only to serve for external comparison; in this most superficial sense in which it is taken as a universal measure it is a matter of complete indifference what is used for this purpose. It ought not to be a fundamental measure in the sense that it forms a scale on which the natural measures of particular things could be represented and from which, by means of a rule, they could be grasped as specifications of a universal measure, i.e. of the measure of their universal body. Without this meaning, however, an absolute measure is interesting and significant only as a common element, and as such is a universal not in itself but only by agreement.

Here _Ma&#223;stab_ is translated as "standard". It can also, maybe better, be translated as "[[gauge]]". Therefore by ([699](#699)) we have 

$$
  \array{
    & & attraction && repulsion
    \\
    & quality : & \int &\dashv& \flat
    \\
    gauge & \bot & \bot && \bot
    \\
    & quantity : & \flat &\dashv& \sharp
    \\
    & & discreteness && continuity
  }
$$

#### B. Specifying measure

##### (a) The Rule

* {725} &#167;725 Die Regel oder der Maa&#223;stab, von dem schon gesprochen worden, ist zun&#228;chst als eine an sich bestimmte Gr&#246;&#223;e, welche Einheit gegen ein Quantum ist, das eine besondere Existenz ist, an einem andern Etwas, als das Etwas der Regel ist, existirt,&#8212;an ihr gemessen, d. i. als Anzahl jener Einheit bestimmt wird. Diese Vergleichung ist ein &#228;u&#223;erliches Thun, jene Einheit selbst eine willk&#252;rliche Gr&#246;&#223;e, die ebenso wieder als Anzahl (der Fu&#223; als eine Anzahl von Zollen) gesetzt werden kann. Aber das Maa&#223; ist nicht nur &#228;u&#223;erliche Regel, sondern als specifisches ist es die&#223;, sich an sich selbst zu seinem Andern zu verhalten, das ein Quantum ist.

* &#167;725 The rule or standard $[$ gauge $]$, which has already been mentioned, is in the first place an intrinsically determinate magnitude which is a unit with reference to a quantum having a particular existence in a something other than the something of the rule; this other something is measured by the rule, i.e. is determined as an amount of the said unit. This comparison is an external act, the unit itself being an arbitrary magnitude which in turn can equally be treated as an amount (the foot as an amount of inches). But measure is not only an external rule; as a specifying measure its nature is to be related in its own self to an other which is a quantum.

##### (b) Specifying Measure

##### (c) Relation of the two Sides as Qualities

## **Book two** Die Lehre vom Wesen / The doctrine of essence 

### Reflection

#### Section 1. Essence as Reflection within Itself

##### Chapter 1 Illusory Being
 
###### A The essential and the unessential

###### B Illusory being

###### C Reflection

##### Chapter 2 The Essentialities or Determination of Reflection

###### $\;\;$ Remark $A = A$

* &#167;863 Thus the essential category of identity is enunciated in the proposition: everything is identical with itself, A = A.

The reflector(!) [[term constructor]] in an [[identity type]]. This is more explicit below at _[Identity](#Identity)_.

###### A Identity
 {#Identity}

* &#167;869 Essence is therefore simple identity with self.

* &#167;869 This identity-with-self is the immediacy of reflection.

The reflector(!) [[term constructor]] in an [[identity type]].  Below this is called te _[First original law of thought](#FirstOriginalLawOfThought)_.

###### $\;\;$ Remark 1: Abstract identity

###### $\;\;$ Remark 2: First original law of thought
 {#FirstOriginalLawOfThought}

* &#167;875 In this remark, I will consider in more detail identity as the law of identity which is usually adduced as the first law of thought.

  This proposition in its positive expression $A = A$ is, in the first instance, nothing more than the expression of an empty tautology. 

The reflector [[term constructor]] in an [[identity type]].

###### B Difference

###### $\;\;$ (a) Absolute difference

###### $\;\;$ (b) Diversity

###### $\;\;$ Remark: The Law of Diversity


* &#167;903 All things are different; or: there are no two things like each other.

Reminiscent of [[identity types]] in [[intensional type theory]].

###### C Contradiction

* &#167;903 When all the conditions of a fact are present, it enters into Existence.


* &#167;1035 The fact emerges from the ground. It is not grounded or posited by it in such a manner that ground remains as a substrate; on the contrary, the positing is the movement of the ground outwards to itself and its simple vanishing.

  $[..]$

  This immediacy that is mediated by ground and condition and is self-identical through the sublating of mediation, is Existence.

[[term introduction]] in [[natural deduction]]


(...)

* Die Wirklichkeit als selbst unmittelbare Formeinheit des Innern und &#196;u&#223;ern ist damit in der Bestimmung der Unmittelbarkeit gegen die Bestimmung der Reflexion in sich; oder sie ist eine Wirklichkeit gegen eine M&#246;glichkeit. Die Beziehung beider auf einander ist das Dritte, das Wirkliche bestimmt ebenso sehr als in sich reflektirtes Seyn, und dieses zugleich als unmittelbar existirendes. Dieses Dritte ist die Nothwendigkeit.

(..)

* Die Wirklichikeit ist formell, insofern sie als erste Wirklichkeit nur unmittelbare, unreflektirte Wirklichkeit, somit nur in dieser Formbestimmung, aber nicht als Totalit&#228;t der Form ist. Sie ist so weiter nichts als ein Seyn oder Existenz &#252;berhaupt. Aber weil sie wesentlich nicht blo&#223;e unmittelbare Existenz, sondern, als Formeinheit des Ansichseyns oder der Innerlichkeit, und der &#196;u&#223;erlichkeit ist, so enth&#228;lt sie unmittelbar das Ansichseyn oder die M&#246;glichkeit. Was wirklich ist, ist m&#246;glich.

so 

$$
  Wirklichkeit \colon Ansichsein/inner \dashv outer
$$

## **Book three** Die Lehre vom Begriff / The doctrine of the notion




## Related entries

* [[being]], [[becoming]]

## References


Comments on Hegel's text are for instance in 

* [[Martin Heidegger]], _Hegel and the Greeks_, Conference of the Academy of Sciences at Heidelberg, July 26, 1958 ([web](http://www.morec.com/hegelgre.htm))
  {#Heidegger58}

* Inwood, _Hegel_, 1983
 {#Inwood1983}

Proposals for formalizing some of Hegel's thoughts in [[categorical logic]] have been put forward by [[William Lawvere]] in several places, for instance in

* [[William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_
 {#LawvereComo}

* [[William Lawvere]], _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_
  {#LawvereLauterEinsen}

* _Toposes of laws of motion_ , transcript of a talk in Montreal, Sept. 1997 ([pdf](http://www.acsu.buffalo.edu/~wlawvere/ToposMotion.pdf))
 {#LawvereMotion}