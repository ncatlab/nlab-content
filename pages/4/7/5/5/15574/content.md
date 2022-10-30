
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

[[!redirects aufhebung]]
[[!redirects Aufhebungs relation]]
[[!redirects jump operator]]
[[!redirects sublation]]

## Idea

> I am not a "Hegelian". F. W. Lawvere [^LQ]

**Aufhebung** (sublation) is a central concept[^ref] in the [[dialectic|dialectical]] logic of the German philosopher [[Georg Hegel|G. W. F. Hegel]]. The German expression has several meanings for which _tollere, elevare, conservare_ would be Latin equivalents.[^fine] 

[^ref]:  A pertinent passage is e.g. [SoL &#167;209](Science+of+Logic#209).

[^fine]: As this polysemy is important for the concept and difficult to preserve in translation we prefer to use the German term in the following.

In his quest to [[axiom|axiomatize]] the concepts of [[space]] and [[cohesion]], [[F. W. Lawvere]], inspired by [[homotopy theory]] proposed a mathematical rendering of the _Aufhebungs_ relation within [[topos theory]] or [[category theory]] more generally. It is the mathematical concept that will constitute the primary subject in the following.

##_Aufhebung_ in Hegel's 'Wissenschaft der Logik'

Although the two volumes of _'[[Science of Logic|Wissenschaft der Logik]]'_  (1st ed. 1812-1816) can be considered as one of the main texts of [[Hegel]]'s philosophy they fell into disfavour in the second half of the 19th century and most of the 20th century, and accordingly received much less attention than the 'Ph&#228;nomenologie des Geistes' or the 'Rechtsphilosophie'. They shared this fate with Hegelian philosophy as a whole which apart from the philological interest it generated, was continued only through the political wing of Lefthegelianism which in either its existentialist interpretation by A. Koj&#232;ve or its Marxist interpretation by G. Luk&#225;cs openly rejected the concept of objective dialectics in nature thereby cutting the social thought from its broad foundation in [[ontology]] and [[logic]], whereas the [[natural philosophy|natural philosophical]] tradition in the vein of F. Engels petrified to the doctrines of dialectical materialism. 

The 'Wissenschaft der Logik' has to be viewed against the background of philosophy in the early 19th century: **Kant** had embarked on a project of 'refoundation', or rather demolition, of [[metaphysics]] from an epistemological perspective and this project had been pushed further by his followers especially Fichte in his _Wissensschaftslehre_. However critical these [[idealism|idealist]] systems had been to the claims of traditional metaphysics and epistemology they all left the traditional logic untouched and in this respect fell behind Leibniz. It is at this point where Hegel starts: he sets out to extend the critical examination of the foundations of knowledge to logic itself.

Heavily influenced by the transcendental deductions and the chapters on dialectical paralogisms in Kant's 'Kritik der reinen Vernunft' he intends to start from indeterminate, immediate [[being]] and justify the autonomous development of the system of categories. Here dialectics and Aufhebung enter the picture as Hegel conceives the categories not only as not given apriorily but as actually [[becoming]]: _logic ceases to be an inventory of categories but becomes a system of transformations of categories!_ (Had Eilenberg and MacLane in 1945 intended their terminological loans from philosophy as a kind of joke, Lawvere would 25 years later take this terminological proximity at face value.)

Hegel parts with the traditional conception mainly in two points: the foundations of his logic coalesce with [[ontology]] into an **objective logic** as the first part is titled (a 'logic of things' as [[Charles Sanders Peirce|C.S. Peirce]] would later put it), i.e. he rejects the subject as a possible ground for logic, and he reassesses the status of **negativity** or conflict-contradiction in logic. The cornerstone of the edifice is the anti-eleatic unity of [[being]] and [[nothing|nothingness]] in the idea of [[becoming]]. It is precisely this 'positively being negative' that finds its expression in the concept of 'Aufhebung'. 

A key passage on Aufhebung in 'Wissenschaft der Logik' comes at the end of the first chapter ([I.1.1Cc, p.113](#WdL)): after a deduction of the categories of '[[being]]', '[[nothing|nothingness]]', and their unity in '[[becoming]]' Hegel determines **[[dialectics]]** as 'the higher rational movement... in which the precondition of the separatedness (of the seemingly separated) is lifted ( _sich aufhebt_ )' ([p.111](#WdL)).

He goes on ([p.113](#WdL)) to explicate _Aufheben_ as one of the most important concepts in all of philosophy that constantly recurs everywhere. The sublated - _das Aufgehobene_ is not nothing which is an _unmediated_, but is a mediated - _ein Vermitteltes_; it is nothing - _das Nichtseiende_, but as a result that originated from a being and therefore still carries with it the determination from which it derives. This is inspired by Spinoza's 'omnis determinatio est negatio': **Aufhebung** is the mode of this coexistence of negation-affirmation.

Hegel draws his logic from a rich tradition of dialectic going back to Plato in general and to its renewal in Fichte and Schelling's attempts to transcendental philosophy in the 1790s for which in turn Kant's attitude was of capital importance: the latter had established in a short paper _'Versuch den Begriff der negativen Gr&#246;&#223;en in die Weltweisheit einzuf&#252;hren'_ (1763) a distinction between contradictions and real oppositions anticipating the later analytic-synthetic division - here originates the term 'Aufhebung' and gets tied to synthesis of oppositions which is terminologically present in Schelling's use of the terms 'thesis', 'anti-thesis' and 'synthesis' for the dialectical triad[^triad]. Secondly, Kant had partly arranged the table of categories in triadic fashion and thereby invited the deduction of the categories by dialectical steps as undertaken by Fichte and Schelling. Kant's view that reason gets necessarily entangled in the contradictions of transcendental dialectic by its own nature was interpreted by Hegel as an indication of the positive role of contradictions as the driving force of thought.

[^triad]: Hegel apparently didn't use these terms though, probably through their use by F. Engels who was a student of Schelling, the terms stick to Hegelian dialectic today.

Clearly, these remarks can not do justice to the richness and subtlety of Hegel's logic and should only serve as canvas against which to get a better grasp of Lawvere's conceptual translation. The points to keep in mind from this view are:

* Aufhebung is a _pervasive_ concept: although Lawvere proposes only mathematical definitions for two terms of Hegel's logic, namely _[[unity of opposites]]_ and _Aufhebung_, these are in fact the key terms and go already far in a reconstruction of the whole edifice!

* Aufhebung unites _determinateness_ with annihilation of being. These recur at the mathematical level as the correspondance between being-being a sheaf, annihilation -being the adjoint opposite of sheaf (anti-sheaf), and the determination of Aufhebung as being the least (=the Leibnizian best) level of being simultaneously a sheaf and an anti-sheaf.

This is the original text on _Aufhebung_ from [Hegel 1812, book 1, section 1, chapter 1, C, 3. ](Science+of+Logic#AufhebenDesWerdens):

> Aufheben und das Aufgehobene (das Ideelle) ist einer der wichtigsten Begriffe der Philosophie, eine Grundbestimmung, die schlechthin allenthalben wiederkehrt, deren Sinn bestimmt aufzufassen und besonders vom Nichts zu unterscheiden ist.&#8212;Was sich aufhebt, wird dadurch nicht zu Nichts. Nichts ist das Unmittelbare; ein Aufgehobenes dagegen ist ein Vermitteltes, es ist das Nichtseyende, aber als Resultat, das von einem Seyn ausgegangen ist; es hat daher die Bestimmtheit aus der es herkommt, noch an sich.

> Aufheben hat in der Sprache den gedoppelten Sinn, da&#223; es so viel als aufbewahren, erhalten bedeutet, und zugleich so viel als aufh&#246;ren lassen, ein Ende machen. Das Aufbewahren selbst schlie&#223;t schon das Negative in sich, da&#223; etwas seiner Unmittelbarkeit und damit einem den &#228;u&#223;erlichen Einwirkungen offenen Daseyn entnommen wird, um es zu erhalten.&#8212;So ist das Aufgehobene ein zugleich Aufbewahrtes, das nur seine Unmittelbarkeit verloren hat, aber darum nicht vernichtet ist. &#8212;Die angegebenen zwei Bestimmungen des Aufhebens k&#246;nnen lexikalisch als zwei Bedeutungen dieses Wortes aufgef&#252;hrt werden. Auffallend m&#252;&#223;te es aber dabei seyn, da&#223; eine Sprache dazu gekommen ist, ein und dasselbe Wort f&#252;r zwei entgegengesetzte Bestimmungen zu gebrauchen. F&#252;r das spekulative Denken ist es erfreulich, in der Sprache W&#246;rter zu finden welche eine spekulative Bedeutung an ihnen selbst haben; die deutsche Sprache hat mehrere dergleichen. Der Doppelsinn des lateinischen: tollere (der durch den ciceronianischen Witz tollendum esse Octavium, ber&#252;hmt geworden) geht nicht so weit, die affirmative Bestimmung geht nur bis zum Emporheben. Etwas ist nur insofern aufgehoben, als es in die Einheit mit seinem Entgegengesetzten getreten ist; in dieser n&#228;hern Bestimmung als ein reflektirtes kann es passend Moment genannt werden. Gewicht und Entfernung von einem Punkt hei&#223;en beim Hebel, dessen mechanische Momente, um der Dieselbigkeit ihrer Wirkung willen bei aller sonstigen Verschiedenheit eines Reellen, wie das ein Gewicht ist, und eines Ideellen, der blo&#223;en r&#228;umlichen Bestimmung, der Linie; s. Encykl. der philos. Wissenschaft 3te Ausg. _ 261. Anm.&#8212;Noch &#246;fter wird die Bemerkung sich aufdringen, da&#223; die philosophische Kunstsprache f&#252;r reflektirte Bestimmungen lateinische Ausdr&#252;cke gebraucht, entweder weil die Muttersprache keine Ausdr&#252;cke daf&#252;r hat, oder wenn sie deren hat, wie hier, weil ihr Ausdruck mehr an das Unmittelbare, die fremde Sprache aber mehr an das Reflektirte erinnert.

## Lawvere's path to _Aufhebung_

> In early 1985, while I was studying the foundations of homotopy theory, it occurred to me that the explicit use of a certain simple categorical structure might serve as a link between mathematics and philosophy. ([Lawvere 1996](#Law96), p.167)

## Extracting the rational kernel 

So now let's get down to business and do some mathematics!

### The mathematics of Yin and Yang

In ([Lawvere 2000](#Law00)) a particularly simple example of the [[adjoint cylinder]] was suggested that we use here as a warm up. Note that the categories involved are not toposes and even lack a terminal object!

Let $N$ be the [[natural numbers]] $\{0, 1,\dots\}$ viewed as a [[category]] via their usual [[poset|ordering]]. Let $L,R:N\to N$ be the two parallel [[functors]] '_even_' and '_odd_' defined by $L(n) \coloneqq 2n$ and $R(n) \coloneqq 2n+1$.

Both are [[fully faithful functor|full and faithful]], hence candidates for an [[adjoint cylinder]], and so we look now for a third functor $N\to N$ which with a clin d'oeil to [[Charles Sanders Peirce|C. S. Peirce's]] concept of _thirdness_ we will call $T$ , such that its forms an [[adjoint triple]] $L\dashv T\dashv R$.

For our simple [[poset]] example these [[adjunctions]] amount to $L(n)\leq m$ iff $n\leq T(m)$ and $n\leq R(m)$ iff $T(n)\leq m$. When such a $T$ exists it must satisfy $T\circ L \cong id\cong T\circ R$ which in our case just gives $T\circ L = id = T\circ R$ - the thirdness $T$ mediates the _identity_ of $L$ and $R$. Spelled out this says $T(2n)=n$ and $T(2n+1)=n$ which we simply take as the definition for $T$.

We also see here how $T$ mediates the _opposition_ between $L$ and $R$ because in order for such a $T$ to exist the functors $L$ and $R$ must (in this example) actually correspond to inclusions of _disjoint_ subcategories e.g. for $L(n)=2n$ and $G(n) \coloneqq 3n\quad$ $T$ would have to invert e.g. 6 to 2 and to 3 at the same time, which a function of course cannot do.

The _unity_ of the opposites is finally provided by the encompassing $N$ where they sit as subcategories $E$ and $O$ of even and odd numbers, respectively.

Whereas $T$$L$ and $T$$R$ are each the identity, the reverse compositions $L$$T$ and $R$$T$ yield an [[idempotent comonad]] $sk:N\to N$ and an [[idempotent monad]] $cosk:N\to N$, respectively, where $sk(2n)=2n$ and $sk(2n+1)=2n$ and $cosk(2n)=2n+1$ and $cosk(2n+1)=2n+1$: in new guises $L$ and $R$ resurface again but this time with an _unmediated opposition_ $sk\dashv cosk$ which expresses the conflict between $E$ and $O$, even and odd.
 
### The mathematics of _Aufhebung_
 {#TheMathematicsOfAufhebung}

For convenience let us briefly recall the following

+-- {: .num_defn #EssentialLocalization}
###### Definition

A [[localization of a category]] $\mathcal{B}$ with [[finite limits]] is a [[reflective subcategory]] $\mathcal{A}$ whose reflection preserves finite limits. The localization is called _[[essential geometric morphism|essential]]_ when the reflection has furthermore a [[left adjoint]].

=--

If $l\dashv r\dashv i$ is an essential localization then $l$ is also [[fully faithful functor|full and faithful]]. If $\mathcal{B}$ is a [[topos]], $\mathcal{A}$ is called an _[[essential geometric morphism|essential]] [[subtopos]]_ and we write $i_!\dashv i^*\dashv i_*$ in this case and call $i_!$ the _essentiality_.

It is a result in ([Kelly-Lawvere 89](#KL89)) that the [[essential geometric morphism|essential]] [[subtoposes]] of a topos form a [[complete lattice]]. Therefore we say:

+-- {: .num_defn #Level}
###### Definition 

An [[essential geometric morphism|essential]] [[subtopos]] of $\mathcal{B}$ is referred to as a _[[level of a topos|level]]_ of $\mathcal{B}$ and levels are denoted by small letters $i,j,\dots$ .

=--

An [[adjoint triple|adjoint string]] $i_!\dashv i^*\dashv i_*$ yields two [[adjoint modalities]] $\Box _i\dashv\bigcirc _i$ on $\mathcal{B}$, namely $\Box _i \coloneqq i_!i^*$ and $\bigcirc _i \coloneqq i_*i^*$.

The [[modalities]] yield notions of _[[modal types]]_, which may be called

* the _i-sheaves_ : $X\in\mathcal{B}$ with $\bigcirc _i X\simeq X$ (following the terminology at _[[Lawvere-Tierney operator]]_);

* the _i-skeleta_ : $X\in\mathcal{B}$ with $\Box _i X\simeq X$ (following the example of [[simplicial skeleta]] discussed [below](#SimplicialAndCubicalSets)).

+-- {: .num_defn #Aufhebung}
###### Definition 
([Lawvere 1989b](#Law89b))

Let $i,j$ be [[level of a topos|levels]], def. \ref{Level}, of a topos $\mathcal{A}$ we say that the level $i$ is _lower_ than level $j$, written 

$$
  \array{
    \Box_i &\prec & \Box_j
    \\
    \bot && \bot
    \\
    \bigcirc_i &\prec & \bigcirc_j 
  }
$$

(or $i\prec j$ for short) when every i-sheaf ($\bigcirc_i$-[[modal type]]) is also a j-sheaf and every i-skeleton ($\Box_i$-[[modal type]]) is a j-skeleton. This is equivalent to say that both $\bigcirc_j \bigcirc_i =\bigcirc_i$ and $\Box_j \Box_i =\Box_i$.

Let $i\prec j$, we say that the level $j$ _resolves the opposite_ of level $i$, written

$$
  \array{
    \Box_i &\ll& \Box_j
    \\
    \bot && \bot
    \\
    \bigcirc_i &\ll& \bigcirc_j 
  }
$$


(or just $i\ll j$ for short[^wayb]) if $\bigcirc _j\Box_i=\Box _i$. 

Finally a [[level of a topos|level]] $\bar{i}$ is called the _Aufhebung_ of level $i$ 

$$
  \array{
    \Box_i &\ll& \Box_{\bar i}
    \\
    \bot &\searrow& \bot
    \\
    \bigcirc_i &\ll& \bigcirc_{\bar i} 
  }
$$


iff it is a minimal level which resolves the opposites of level $i$, i.e. iff $i\ll\bar{i}$ and for any $k$ with $i\ll k$ then it holds that $\bar{i}\leq k$ in the order relation (by subtopos inclusion) between levels.

=--

[^wayb]: $\ll$ is called the _way below_ relation in ([KRRZ11](#KRRZ11)).

+-- {: .num_remark}
###### Remark

The condition $\bigcirc_j \Box_i=\Box_i$ amounts to saying that every $i$-skeleton is a $j$-sheaf:

Suppose the condition holds and $X$ is an $i$-skeleton ($\Box_i X= X$) then $\bigcirc_j \Box_i X =\bigcirc_j X=\Box_i X =X$ i.e. $X$ is a $j$-sheaf. Conversely, if every $i$-skeleton is a $j$-sheaf then, since by the idempotency of $\Box_i$ $i$-skeleta are precisely the objects of form $\Box_i X$ for some $X$, $\Box_i X$ is by assumption a $j$-sheaf and that's precisely what $\bigcirc_j \Box_i X=\Box_i X$ asserts.

The resolution condition $\bigcirc_j \Box_i=\Box_i$ ensures that $i$-skeleta are in the intersection of the $j$-skeleta and $j$-sheaves at the resolving level.

Thinking of $\bigcirc_i\Box_i=\bigcirc_i$ as an expression of the negation of $\Box_i$ by $\bigcirc_i$ one could think of $\bigcirc_j \Box_i=\Box_i$ as dialogical refinement of the opposition through a _negation of the negation_: 'Proponent' $\bigcirc_i$ gets updated - _sublated_ to $\bigcirc_j$ in order to absorb the 'opponent' $\Box_i$.

Note that $\bigcirc_j \Box_i=\Box_i$ does not imply $\Box_j \bigcirc_i =\bigcirc_i$ , e.g. in the [[Sierpinski topos]] $Set^\to$ the level $\emptyset\dashv\ast$ is resolved by $\nabla\dashv &#643;$ but $(\nabla\circ\ast)\neq\ast$ (see [below](#SierpExample)).

We say that $j$ _co-resolves_ $i$ if $\Box_j \bigcirc_i =\bigcirc_i$. If $j$ resolves and co-resolves $i$ we say that $j$ bi-resolves $i$. In the latter case, all $i$-sheaves and $i$-skeleta are simultaneously $j$-sheaves and $j$-skeleta at the higher level $j$.

=--

+-- {: .num_remark}
###### Remark

The Aufhebung of a level is the smallest level that resolves its opposites or contradictions. Such a level need not exist in general for every level but in certain cases like [[presheaf toposes]] over [[graphic category|graphic categories]] or, more generally,  over [[von Neumann regular categories]] ([Lawvere 2002](#Law02)), it does. The Aufhebungs relation is also called the _jump operator_ in [Lawvere (2009)](#Law09).


=--

+-- {: .num_remark}
###### Remark

Comparing with [[Science of Logic|WdL]] under Lawvere's translation and identifing the [[level of a topos|levels]]  with logical categories of thinking in the ordinary sense (thought determinations - _Gedankenbestimmungen_), one sees that $\emptyset\dashv\ast$ corresponds to Hegel's logical category of _indeterminate being_ whereas the higher levels correspond to logical  categories of _determinate being_ - _Bestimmtheit_.

Furthermore one sees that the subtoposes corresponding to the levels trace out as _mathematical_ categories the _logical_ categories of thought as envisioned by Hegel thereby corroborating the terminological choices of Eilenberg and Mac Lane made in their 1945 paper!

=--

## Examples

### Aufhebung of Becoming -- Determinate being
 {#AufhebungOfBecoming}

#### From Faust's study

In the context of a **[[category of being]]**, aka a (sufficiently) [[cohesive topos]], which has a connected [[subobject classifier]] $\Omega$ and product preserving components functor $\Pi _0$,  there is an opposition 

$$
  \empty\dashv \ast
$$ 

between _[[nothing|non being]]_ (the [[idempotent comonad]] constant on the [[initial object]]) and _[[being|pure being]]_ (the idempotent comonad constant in the [[terminal object]]) whose Aufhebung is (at least in suitable cases, see [below](#ExamplesBecomingFormalization)) the [[unity of opposites|opposition]] of [[becoming]]

$$ 
  \flat\dashv \sharp
$$ 

given by [[flat modality]] $\dashv$ [[sharp modality]], between _non-becoming_ vs. _pure becoming_ (cf. Lawvere 1989a, 1989b, [1991a](#Law91a))[^Pure]. This is what in [SoL &#167; 191](Science+of+Logic#DaseinUberhaupt) is called _[[determinate being]]_ as it corresponds to localization at $\neg\neg$ and the double negation creates the determinateness of the 'Etwasse'.

[^Pure]: Lawvere suggests more generally to read $\Box_ i\dashv\bigcirc_i$ as an opposition _non-F_ vs. _pure-F_ where $F$ is a property descriptively appropriate for the level.

In terms of [[topos theory]] the Aufhebungs-condition $\sharp \emptyset \simeq \emptyset$ says equivalently that the [[subtopos]] of $\sharp$-[[modal objects]] is a [[dense subtopos]].

This lowest essential subtopos arises more generally for categories $\mathcal{A}$ with [[initial object|initial]] and [[terminal objects]], via the adjoints to $\mathcal{A}\to \{*\}$ that map $*$ to $0$ and $1$. Especially, the imposition of conditions that ensure the existence of $\flat\dashv \sharp$ can be viewed as intended to provide a specific resolution of the 'identity' $0=1$, the indeterminate confluence of truth and falsity at the lowest level which [[syntax|syntactically]] corresponds to the inconsistent [[geometric theory]].

Following Lawvere's suggestive terminology and identifying a level with its sheaf part, we could somewhat more loosely say that [[becoming]] is the Aufhebung of the opposition between [[nothing]] and [[being]], or more shortly, that _becoming is the Aufhebung of being_.

The Aufhebungs relation expresses precisely that the (positive) sheaf part of the higher level $j$ subsumes (the opposition between) the skeleton and the sheaf part of the lower level in a universal way - it is the smallest context in which negative and positive poles of the lower level can positively coexist. To elaborate this intuition somewhat, it is the minimal way to turn the negative part into a positive part yet retaining the positivity of its positive opposite.

For more on the relevant _metaphysical_ modalities see at [[adjoint modality]].

#### Over cohesive sites
 {#ExamplesBecomingFormalization}

We discuss Aufhebung of [[becoming]] in the above sense in [[cohesive toposes]] ([[cohesive (∞,1)-toposes]]) with a [[cohesive site]] ([[∞-cohesive site]]) of definition.

(More general discussion is now also in [Lawvere-Menni 15, lemma 4.1, 4.2](#LawvereMenni15), see at [pieces-to-points-transform -- Relation to Aufhebung](points-to-pieces+transform#RelationToAufhebung)).

+-- {: .num_prop #AufhebungOfBecomingMeansOnlyInitialObjectHasNoGlobalPoints}
###### Proposition

Given a [[topos]] equipped with a [[level of a topos]] given by an [[adjoint modality]] $(\Box\dashv \bigcirc) \coloneqq (\flat \dashv \sharp)$, then the condition $\sharp \emptyset \simeq \emptyset$ is equivalent to $(\flat X \simeq \emptyset) \Leftrightarrow (X \simeq \emptyset)$.

=--

+-- {: .proof}
###### Proof

In a topos the [[initial object]] $\emptyset$ is a [[strict initial object]], and hence $(X \simeq \emptyset) \simeq (X \to \emptyset)$.

In one direction, assuming $\sharp \emptyset \simeq \emptyset$ then

$$
  \begin{aligned}
    (X \simeq \emptyset)
    & \simeq
    (X \to \emptyset)
    \\
    & \simeq (X \to \sharp \emptyset)
    \\
    & \simeq (\flat X \to \emptyset)
    \\
    & \simeq (\flat X \simeq \emptyset)
  \end{aligned}
  \,.
$$

Conversely, assume that $(\flat X \simeq \emptyset) \Leftrightarrow (X \simeq \emptyset)$. Then for all $X$

$$
  \begin{aligned}
    (X\to \emptyset)
    & \simeq
    (X\simeq \emptyset)
   \\
    & \simeq (\flat X \simeq \emptyset)
    \\
    & \simeq (\flat X \to \emptyset)
    \\
    & \simeq (X\to \sharp \emptyset)
  \end{aligned}
$$

and hence by the [[Yoneda lemma]] $\emptyset \simeq \sharp \emptyset$.

=--

+-- {: .num_example}
###### Example
In the [[Sierpinski topos]] $Set^{\to}$ with objects maps $X\to Y$ between sets $X,Y$, the initial object is $\emptyset\to\emptyset$ and the respective adjoint modalities are given by $\sharp(X\to Y)=X\to 1$ and $\flat(X\to Y)=X\overset{id}{\to} X$. Since not only $\flat(\emptyset\to\emptyset)=\emptyset\to\emptyset$ but also $\flat(\emptyset\to Y)=\emptyset\to\emptyset$,  we find that $\flat\dashv \sharp$ does not resolve $\emptyset\dashv\ast$ (we expand on this example [below](#SierpExample)).

=--

+-- {: .num_cor}
###### Corollary

An [[(∞,1)-topos]] with Aufhebung $(\flat \dashv \sharp)$ of [[being]] has [[homotopy dimension]] $\leq 0$ with respect to the $\flat$-[[modal types|modal]] [[base (∞,1)-topos]].

=--

+-- {: .num_prop #OverCohesiveSiteBecomingIsResolved}
###### Proposition

Let $\mathcal{S}$ be a [[cohesive site]] (or [[∞-cohesive site]]) and $\mathbf{H} = Sh(\mathcal{S})$ its [[cohesive topos|cohesive]] [[sheaf topos]] (or $\mathbf{H} = Sh_\infty(S)$ its [[cohesive (∞,1)-topos]] ). 

Then in $\mathbf{H}$ we have $\sharp \emptyset \simeq \emptyset$, hence that $(\flat \dashv \sharp)$ resolves, def. \ref{Aufhebung},  the [[unity of opposites]] $(\emptyset \dashv \ast)$ which is [[becoming]].

=--

+-- {: .proof}
###### Proof

The [[flat modality]] $\flat$ in this case is given by forming [[global sections]] and re-embedding the resulting [[set]] as a [[constant sheaf]].

Since by assumption $\mathcal{S}$ has a [[terminal object]] $\ast$, it follows that for $X\in \mathbf{H}$ any sheaf $X \colon \mathcal{S}^{op}\to Set$ then

$$
  \flat X \simeq X(\ast)
$$ 

(where we may leave the constant re-embedding implicit, due to it being [[fully faithful functor|fully faithful]]).

Moreover by assumption, for every object $U\in \mathcal{S}$ there exists a morphism $i \colon \ast \to U$ hence for every $X\in \mathbf{H}$ and every $U$ there exists a morphism $i^\ast \colon X(U)\to \flat X$. This means that if $\flat X \simeq \emptyset$ then $X(U) \simeq \emptyset$ for all $U \in \mathcal{S}$ and hence $X\simeq \emptyset$. From this the claim follows with prop. \ref{AufhebungOfBecomingMeansOnlyInitialObjectHasNoGlobalPoints}.

=--

+-- {: .num_prop #OverCohesiveSiteBecomingIsAufgehoben} 
###### Proposition

Let $\mathcal{S}$ be a [[cohesive site]] (or [[∞-cohesive site]]) and $\mathbf{H} = Sh(\mathcal{S})$ its [[cohesive topos|cohesive]] [[sheaf topos]] with values in [[Set]] (or $\mathbf{H} = Sh_\infty(S)$ its [[cohesive (∞,1)-topos]] ). 

Then in $\mathbf{H}$ we have Aufhebung, def. \ref{Aufhebung}, of the [[duality of opposites]] of [[becoming]] $\emptyset \dashv \ast$ ("[[Dasein]]").

$$
  \array{
     \flat &\dashv& \sharp
     \\
     \vee &\nearrow& \vee
     \\
     \emptyset &\dashv& \ast
  }
$$


=--

+-- {: .proof}
###### Proof

By prop. \ref{OverCohesiveSiteBecomingIsResolved} we have that $(\flat\dashv \sharp)$ resolves $(\emptyset \dashv \ast)$ and so it remains to see that it is the minimal [[level of a topos|level]] with this property. But the [[subtopos]] of [[sharp modality|sharp]]-[[modal types]] is $\simeq$ [[Set]] which is clearly a 2-valued [[Boolean topos]]. By [this proposition](subtopos#BooleantoposesAreAtoms) these are the [[atoms]] in the [[subtopos lattice]] hence are minimal as non-trivial subtoposes and hence also as non-trivial [[level of a topos|levels]].

=--

+-- {: .num_remark #OnDoubleNegation}
###### Remark
As mentioned above, the Aufhebung of $\emptyset\dashv \ast$ is necessarily given by a _dense_ subtopos $\mathcal{E}_j$. Since $\neg\neg$ is the unique largest dense topology (cf.
[[double negation topology]] or the references cited there) it follows in general that $\mathcal{E}_{\neg\neg}\subseteq\mathcal{E}_j$ , in particular in the case that $\mathcal{E}_{\neg\neg}$ happens to be [[essential geometric morphism|essential]] and hence happens to be a [[level of a topos|level]], the minimality condition on Aufhebung means that $\mathcal{E}_{\neg\neg}=\mathcal{E}_j$.

A special case of this are toposes $\mathcal{E}$ such that $\mathcal{E}_{\neg\neg}$ is [[open subtopos|open]] whence essential in particular; these are called $\bot$-scattered toposes. For the record we state:

**Proposition.**
Let $\mathcal{E}$ be a $\bot$-[[scattered topos]]. The Aufhebung of $\emptyset\dashv\ast$ is given by $\mathcal{E}_{\neg\neg}$.  $\qed$

Another consequence is that the Aufhebung $\mathcal{E}_j$ of $\emptyset\dashv\ast$ is [[Boolean topos|Boolean]] precisely when $\mathcal{E}_{\neg\neg}$ is essential e.g. for Boolean $\mathcal{E}$ this happens trivially and accordingly the Aufhebung of $\emptyset\dashv \ast$ is $\mathcal{E}$ in this case. 

It also follows from the [above proposition](#OverCohesiveSiteBecomingIsAufgehoben) that for [[cohesive sites]] over [[Set]]: $\mathbf{H}_{\neg\neg}=Set$ i.e. the double negation topos coincides  with the base.
=--


+-- {: .num_example}
###### Example

Examples of $\infty$-toposes satisfying the assumptions of prop. \ref{OverCohesiveSiteBecomingIsAufgehoben} and hence exhibiting Aufhebung of becoming include

* [[∞-groupoids]]

* [[Euclidean-topological ∞-groupoids]]

* [[smooth ∞-groupoids]]

* [[formal smooth ∞-groupoids]]

* [[super ∞-groupoids]]

* [[smooth super ∞-groupoids]]

Here [[formal smooth ∞-groupoid]] has its [[cohesion]] further refined to [[differential cohesion]], yielding

$$
  \array{
     id & \dashv & id
     \\
     \vee && \vee
     \\
     \Re &\dashv& &#643;_{inf} &\dashv& \flat_{inf}
     \\
      && \vee && \vee
     \\
     && &#643; &\dashv& \flat &\dashv& \sharp
     \\
     && && \vee &\nearrow& \vee
     \\
     && && \emptyset &\dashv& \ast
  }
$$

=--

### Absolute identity and _Selbstaufhebung_

Given a topos $\mathcal{E}$ the highest level is always given by $id_\mathcal{E}$ yielding the trivial adjoint string $id_\mathcal{E}\dashv id_\mathcal{E}\dashv id_\mathcal{E}$ with no less trivial adjoint modalities $id_\mathcal{E}\dashv id_\mathcal{E}$. Obviously, the sheaves and skeleta for this level coincide. Since the corresponding subtopos is simply $\mathcal{E}$, this level _resolves every other level_ and suggests to view the ascension from $\emptyset\dashv\ast$ to $id_\mathcal{E}\dashv id_\mathcal{E}$ as a process of increasing stepwise the number of objects that are sheaves as well as skeleta at a given level. The definition of resolution ensures that a level inherits the objects in the intersection from lower levels but also that all non-sheaves from the lower levels will be henceforth in the intersection.

Note that though $id_\mathcal{E}$ resolves every level it need not be the Aufhebung of any strictly lower level. This situation occurs e.g. in the examples from combinatorial topology discussed [below](#SimplicialAndCubicalSets): Here the levels correspond to the geometrical dimension of the 'triangulated spaces' involved plus the highest level 'at infinity' and the Aufhebung is a simple numerical relation between finite levels e.g. in the topos of Ball complexes the Aufhebung of level $n$ is $n+1$. Of course, $id_\mathcal{E}$ is always its own Aufhebung and we see, incidentally, that a level might be the Aufhebung of more than one level, namely e.g. itself and perhaps several other levels - this might happen with $id_\mathcal{E}$ when the lattice of levels is finite e.g. in the [[Sierpinski topos]] $Set^{\to}$ (see [below](#SierpExample)).

Though $id_\mathcal{E}$ is trivial from a mathematical point of view, paradoxically it nevertheless captures on the philosophical side one of the most enigmatic concepts of the early _identity philosophy_ of Hegel and Schelling, namely the **absolute** as the identity of identity and non-identity:

>Das Absolute selbst aber ist darum die Identit&#228;t der Identit&#228;t und der Nichtidentit&#228;t; Entgegensetzen und Einssein ist zugleich in ihm. (Hegel [1801](#Diff), p.96)

We might call a topos $\mathcal{E}$ with the property that $id_\mathcal{E}$ is the Aufhebung of no other level than itself _absolute_ and $id_\mathcal{E}$ the absolute level. Note that these toposes will occasionally have infinitely many levels and are then from the perspective of the mature Hegel vulnerable to the charge of being a _'bad infinity'_.

The discussion so far might suggest that being self-sublating is a property peculiar to $id_\mathcal{E}$ but this is not the case. In fact $id_\mathcal{E}$ is only an instance of a whole class of essential localizations enjoying this property:

+-- {: .num_defn #quintessentialloc}
###### Definition 
Let $\mathcal{C}$ be a finitely complete category. An [[level|essential localization]] $l\dashv r\dashv i:\mathcal{L}\to\mathcal{C}$ is called **quintessential** if $l$ is naturally isomorphic to $i$.
=--

To say that $l\dashv r\dashv i:\mathcal{L}\to\mathcal{C}$ is a quintessential localization amounts to say in Lawvere's terminology ([2007](#07)) that $i:\mathcal{L}\to\mathcal{C}$ exhibits $\mathcal{C}$ as a [[quality type]] over $\mathcal{L}$ with $r$ providing the right adjoint to $i\simeq l$ (provided $\mathcal{L}$, $\mathcal{C}$ are [[extensive category|extensive]]).

The following is immediate:

+-- {: .num_prop #quintAuf} 
###### Proposition

Let $l\dashv r\dashv i:\mathcal{L}\to\mathcal{C}$ be a quintessential localization. Then the corresponding [[adjoint modality]] $l\cdot r\dashv i\cdot r$ coincides up to natural isomorphism and provides its own Aufhebung.  $\qed$
=--  

A simple _example_ of a non-trivial quintessential localization is given by the category $\mathcal{C}$ with objects pairs $(X, e)$ where $X$ is a set and $e=e^2$ an idempotent map $X\to X$. A morphism $f:(X_1, e_1)\to (X_2, e_2)$ is a function $f:X_1\to X_2$ with $f\cdot e_1=e_2\cdot f$. These equivariant morphisms are bound to preserve fixpoints: when $e_1(x)=x$ then $f(e_1(x))=f(x)=e_2(f(x))$. Then the fixpoint set functor $r:\mathcal{C}\to Set$ with $r(X, e)=\{x\in X | e(x)=x \}$ is left as well as right adjoint to $i(X)=(X, id_X)$ since an equivariant morphism $f:(X,e)\to (Y,id_Y)$ is uniquely determined by its restriction to the fixpoints of $e$ and its values are given by $f(e(x))$. The [[adjoint modality]] $i\cdot r\dashv i\cdot r:\mathcal{C}\to\mathcal{C}$ corresponding to $i\dashv r\dashv i:Set\to\mathcal{C}$ maps $(X,e)$ to $(r(X),id_{r(X)})$. The corresponding level sublates $\emptyset\dashv\ast$ as well as itself whereas $id_\mathcal{E}$ only sublates itself.

For further properties of quintessential localizations see at [[quality type]].

### The example of the Sierpinski topos{#SierpExample}

(...)

### Simplicial and cubical sets
 {#SimplicialAndCubicalSets}

(...) [[simplicial set]] (...)


[[simplicial skeleton]] $\dashv$ [[simplicial coskeleton]]

(...) [[cubical set]] (...)

([Kennett-Riehl-Roy-Zaks (2011)](#KRRZ11))

### An open problem: the presheaf topos over non-empty finite sets

## Related pages

* [[Hegelian taco]]

* [[Science of Logic]]

* [[adjoint modality]]

* [[adjoint logic]]

* [[level of a topos]]

* [[quality type]]

* [[graphic category]]

* [[generic interval]]

* [[Pursuing stacks]]

* [[co-Heyting boundary]]

* [[homotopy dimension]]

##A guide to the literature

The book by [La Palme-Reyes-Zolfaghari (2004)](#RRZ04) provides a good entry to the mathematics of Lawvere from an elementary point of view and contains even a page on the adjoint cylinder.

Lawvere introduced the Hegelian concepts in Lawvere ([1989b](#Law89b)). They get some attention in Lawvere ([1991a](#Law91a),[1992](#Law92)) with the latter containing his 'philosophical program'. By all means have a look at [Lawvere (1996)](#Law96), this together with Lawvere ([1989a](#Law89a),[1999](#Law99)) exposes his ideas on homotopy theory. The  work on graphic toposes ([1989b](#Law89b),[1991b](#Law91b),[2002](#Law02)) concerns the _Aufhebungs_ relation with the latter containing a discussion of the relevant concepts. [Kelly-Lawvere (1989)](#KL89) provides the technical prerequisites on essential localizations for _Aufhebung_.

The known mathematical results on the Aufhebungs relation are contained in the paper by [Kennett-Riehl-Roy-Zaks (2011)](#KRRZ11) which is based on older phd-works by some of the authors.

Further results on essential localizations can be found in the papers by [Borceux-Korotenski (1991)](#BK91), [Johnstone (1996)](#JS96), [Vitale (2001)](#VT01) and [Lucyshyn-Wright (2011)](#LW11) or in [SGA 4](#SGA4).

***

<img src="http://ncatlab.org/nlab/files/AufhebungDetail.jpg" width="900"> 
([full pdf](http://www.in-situ-art-society.com/docs/2015-09-18+19_aufhebung_flyer.pdf) by [In Situ Art Society](http://www.in-situ-art-society.com/aufhebung.html))

***

##References

* {#SGA4} [[Michael Artin|M.Artin]], [[Alexander Grothendieck|A.Grothendieck]], [[J. L. Verdier]] (eds.), _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas - SGA 4_ , Springer LNM **269** Heidelberg 1972. (sec. IV 7.6., pp.414-416)

* [[John Baez|J.C. Baez]], [[Mike Shulman|M. Shulman]], _Lectures on n-categories and cohomology_ , pp.1-68 in: J.C. Baez, P. May (eds.), _Towards Higher Categories_, Springer Heidelberg 2010. ([preprint](http://math.ucr.edu/home/baez/cohomology.pdf))
&#8206;
* {#BK91}[[Francis Borceux|F. Borceux]], M. Korostenski, _Open Localizations_ , JPAA **74** (1991) pp.229-238.

* J. Climent Vidal, J. Soliveres Tur, _Functors of Lindenbaum-Tarski, Schematic Interpretations, and Adjoint Cylinders between Sentential Logics_ , Notre Dame Journal of Formal Logic **49** no.2 (2008) pp.185-202. ([pdf](https://projecteuclid.org/download/pdfview_1/euclid.ndjfl/1210859927))
&#8206;
* H. F. Fulda, _Aufheben_ , pp.318-320 in Ritter (ed.), _Historisches W&#246;rterbuch der Philosophie_ , Schwabe Basel 1971.  ([Heidi](http://archiv.ub.uni-heidelberg.de/volltextserver/16307/))

* {#Diff} [[G. W. F. Hegel]], _Differenz des Fichte'schen und Schelling'schen Systems der Philosophie_ , pp.7-138 in Moldenhauer, Michel (eds.), _Werke 2_ , Suhrkamp Frankfurt 1986[1801].

* {#WdL} [[G. W. F. Hegel]], _[[Science of Logic|Wissenschaft der Logik]] I_ , Suhrkamp Frankfurt 1986[1812/13; revised 1831].

* {#JS96}[[Peter Johnstone|P. Johnstone]], _Remarks on Quintessential and Persistent Localizations_ , TAC **2** no.8 (1996) pp.90-99. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf))

* {#KL89}[[G. M. Kelly]], [[F. W. Lawvere]], _On the Complete Lattice of Essential Localizations_ , Bull.Soc.Math. de Belgique **XLI** (1989) pp.289-319.

* {#KRRZ11} C. Kennett, [[Emily Riehl|E. Riehl]], M. Roy, M. Zaks, _Levels in the toposes of simplicial sets and cubical sets_ , JPAA **215** no.5 (2011) pp.949-961. ([preprint](http://arxiv.org/abs/1003.5944))

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* {#Law89a} [[F. W. Lawvere]], _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* {#Law89b} [[F. W. Lawvere]], _Display of graphics and their applications, as exemplified by 2-categories and the Hegelian "taco"_ , Proceedings of the first international conference on algebraic methodology and software technology University of Ioowa, May 22-24 1989, Iowa City, pp.51-74. 

* {#Law91a} [[F. W. Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_ , pp.1-13 in Springer LNM **1488** (1991).

* {#Law91b} [[F. W. Lawvere]], _More on Graphic Toposes_ , Cah.Top.G&#233;om.Diff.Cat. **XXXII** no.1 (1991) pp.5-10. ([pdf](archive.numdam.org/article/CTGDC_1991__32_1_5_0.pdf))
&#8206;
* {#Law92} [[F. W. Lawvere]], _Categories of Space and Quantity_, pp.14-30 in: J. Echeverria et al (eds.), _The Space of mathematics_ , de Gruyter Berlin 1992.

* {#Law94a} [[F. W. Lawvere]], _Cohesive Toposes and Cantor's 'lauter Einsen'_ , Phil. Math. **2** no.3 (1994) pp.5-15.

* {#Law94b} [[F. W. Lawvere]], _Tools for the Advancement of Objective Logic: Closed Categories and Toposes_, pp.43-56 in: J. Macnamara, G. E. Reyes (eds.), _The Logical Foundations of Cognition_ , Oxford UP 1994.

* {#Law96} [[F. W. Lawvere]], _[[Unity and Identity of Opposites in Calculus and Physics]]_ , App. Cat. Struc **4** (1996) pp.167-174.

* {#Law99} [[F. W. Lawvere]], _Kinship and Mathematical Categories_ , pp.411-425 in: R. Jackendoff, P. Bloom, K. Wynn (eds), _Language, Logic, and Concepts - Essays in Memory of John Macnamara_, MIT Press 1999.

* {#Law00} [[F. W. Lawvere]], _Adjoint Cylinders_, message to catlist November 2000. ([link](http://permalink.gmane.org/gmane.science.mathematics.categories/1683))

* {#Law02} [[F. W. Lawvere]], _Linearization of graphic toposes via Coxeter groups_ , JPAA **168** (2002) pp.425-436.

* {#Law07} [[F. W. Lawvere]], _Axiomatic cohesion_ , TAC **19** no.3 (2007) pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

* {#Law09} [[F. W. Lawvere]], _Open Problems in Topos Theory_ , ms. (2009). ([pdf](http://cheng.staff.shef.ac.uk/pssl88/lawvere.pdf)) {#Law09}

* {#Law13} [[F. W. Lawvere]], _Combinatorial Topology_, message to catlist November 2013. ([link](http://comments.gmane.org/gmane.science.mathematics.categories/7920))

* {#LW11}[[Rory Lucyshyn-Wright|R. Lucyshyn-Wright]], _Totally Distributive Toposes_ , arXiv.1108.4032 (2011). ([pdf](http://arxiv.org/pdf/1108.4032v3))

* {#Menni09} [[Matías Menni|M. Menni]], _Algebraic Categories whose Projectives are Explicitly Free_ , TAC **22** no.29 (2009) pp.509-541. ([pdf](http://www.tac.mta.ca/tac/volumes/22/20/22-20.pdf))

* {#Menni12} [[Matías Menni|M. Menni]], _Bimonadicity and the Explicit Base Property_ , TAC **26** no.22 (2012) pp.554-581. ([pdf](http://www.tac.mta.ca/tac/volumes/26/22/26-22.pdf))

* J. Petitot, _La Neige est Blanche ssi... Pr&#233;dication et Perception_ , Math.Inf.Sci.Hum **35** no.140 (1997) pp.35-50. ([pdf](http://archive.numdam.org/article/MSH_197_140_35_0.pdf))

* [[Bob Rosebrugh|R. Rosebrugh]], R. J. Wood, _Distributive Adjoint Strings_ , TAC **1** no.6 (1995) pp.119-145. ([pdf](http://www.tac.mta.ca/tac/volumes/1995/n6/v1n6.pdf))

* [[R. Street]], _The petit topos of globular sets_ , JPAA **154** (2000) pp.299-315.

* {#VT01}[[Enrico Vitale|E. M. Vitale]], _Essential Localizations and Infinitary Exact Completions_ , TAC **8** no.17 (2001) pp.465-480. ([pdf](http://www.tac.mta.ca/tac/volumes/8/n17/n17.pdf))

* {#WR93}[[Gavin C. Wraith]], _Using the Generic Interval_ , Cah.Top.G&#233;om.Diff.Cat. **XXXIV** 4 (1993) pp.259-266. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1993__34_4/CTGDC_1993__34_4_259_0/CTGDC_1993__34_4_259_0.pdf))

* {#LawvereMenni15} [[William Lawvere]], [[Matías Menni]], _Internal choice holds in the discrete part of any cohesive topos satisfying stable connected codiscreteness_, Theory and Applications of Categories, Vol. 30, 2015, No. 26, pp 909-932. ([TAC](http://www.tac.mta.ca/tac/volumes/30/26/30-26abs.html))

[^LQ]: ([Lawvere 1989](#Law89b), p.74).