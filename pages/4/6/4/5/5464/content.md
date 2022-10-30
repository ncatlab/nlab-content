
<a id="DocStart"></a>

# An informal introduction to topos theory # {: #title}

This is a changing, editable document.  You can also read a [peer-reviewed, unchanging, non-editable version](http://ncatlab.org/publications/published/Leinster2011).  

##### Tom Leinster ##### {: #author}

+-- {: .thanks }
School of Mathematics and Statistics, University of Glasgow, Glasgow G12 8QW, UK; Tom.Leinster@glasgow.ac.uk. Supported by an EPSRC Advanced Research Fellowship.
=--




* tic
{: toc}




## Introduction ##

This short text is for readers who are confident in basic [[nlab:category theory]] but know little or nothing about [[nlab:toposes]]. It is based on some impromptu talks given to a small group of [[nlab:category]] theorists. I am no expert on [[nlab:topos theory]]. These notes are for people even less expert than me.

In keeping with the spirit of the talks, what follows is light on both detail and references. For the reader wishing for more, almost everything here is presented in respectable form in Mac Lane and Moerdijk's very pleasant introduction to [[nlab:topos theory]] ([1994](#citeMaMo)). Nothing here is new, not even the expository viewpoint (very loosely inspired by [Johnstone](#citeJohSE) ([2003](#citeJohSE))).

As a rough indication of the level of knowledge assumed, I will take it that you are totally comfortable with the [[nlab:Yoneda Lemma]] and the concept of [[nlab:cartesian closed category]], but I will not assume that you know the definition of [[nlab:subobject classifier]] or of [[nlab:topos]].

Section&nbsp;[1](#sectiona) explains the definition of [[nlab:topos]]. The remaining three sections discuss some of the connections between [[nlab:topos theory]] and other subjects. There are many more such connections than I will mention; I hope it is abundantly clear that these notes are, by design, a quick sketch of a large subject.

Section&nbsp;[2](#sectionb) is on connections between [[nlab:topos theory]] and [[nlab:set theory]]. There are two themes here. One is that, using the language of [[nlab:toposes]], we can write down an axiomatization of [[nlab:sets]] that sticks closely to how [[nlab:sets]] are actually used in mathematics. This provides an appealing alternative to [[nlab:ZFC]]. The other, related, theme is that

+-- {: style="text-align: center" }
*a [[nlab:topos]] is a generalized [[nlab:category of sets]].*
=--

Section&nbsp;[3](#sectionc) is on connections with [[nlab:geometry]] (in a broad sense); there the thought is that

+-- {: style="text-align: center" }
*a [[nlab:topos]] is a generalized [[nlab:space]].*
=--

Section&nbsp;[4](#sectiond) is on connections with [[nlab:universal algebra]]:

+-- {: style="text-align: center" }
*a [[nlab:topos]] is a generalized [[nlab:theory]].*
=--

What this means is that there is one [[nlab:topos]] embodying the concept of '[[nlab:ring]]', another embodying the concept of '[[nlab:field]]', and so on. This is the story of [[nlab:classifying toposes]].
+--
Sections&nbsp;[2](#sectionb)--[4](#sectiond) can be read in any order, except that ideally&nbsp;&#167;[3](#sectionc) ([[nlab:geometry]]) should come before&#160;&#167;[4](#sectiond) ([[nlab:universal algebra]]). You *can* read&#160;&#167;[4](#sectiond) without having read&#160;&#167;[3](#sectionc), but the price to pay is that the notion of '[[nlab:geometric morphism]]'---defined in&nbsp;&#167;[3](#sectionc) and used in&nbsp;&#167;[4](#sectiond)---might seem rather mysterious.
=--
+--
=--
Algebraic geometers beware: the word '[[nlab:topos]]' is used by mathematicians in two slightly different senses, according to circumstance and culture. There are [[nlab:elementary toposes]] and [[nlab:Grothendieck toposes]]. [[nlab:Category]] theorists tend to use '[[nlab:topos]]' to mean '[[nlab:elementary topos]]' by default, although [[nlab:Grothendieck toposes]] are also important in [[nlab:category theory]]. But when an [[nlab:algebraic geometer]] says '[[nlab:topos]]', they almost certainly mean '[[nlab:Grothendieck topos]]' (what else?).

[[nlab:Grothendieck toposes]] are [[nlab:categories of sheaves]]. Elementary [[nlab:toposes]] are slightly more general, and the definition is simpler. They are what I will emphasize here. [[nlab:Grothendieck toposes]] are the subject of Section&nbsp;[3](#sectionc), and appear fleetingly elsewhere; but if you only want to learn about [[nlab:categories of sheaves]], this is probably not the text for you.

##### Acknowledgements #####

I thank Andrei Akhvlediani, [[nlab:Eugenia Cheng]], [[nlab:Richard Garner]], [[nlab:Nick Gurski]], Ignacio Lopez Franco and [[nlab:Emily Riehl]] for their participation and encouragement. Aspects of Section&#160;[4](#sectiond) draw on a vaguely similar presentation of vaguely similar material by [[nlab:Richard Garner]]. I thank the organizers of Category Theory 2010 for making the talks possible, even though they did not mean to: Francesca Cagliari, Eugenio Moggi, [[nlab:Marco Grandis]], Sandra Mantovani, Pino Rosolini, and Bob Walters. I thank Filip B&#225;r, Jon Phillips, [[nlab:Urs Schreiber]], [[nlab:Mike Shulman]], Alex Simpson, [[nlab:Danny Stevenson]] and Todd Wilson for suggestions and corrections. I am especially grateful to [[nlab:Todd Trimble]] for carefully reading an earlier version and suggesting many improvements.

+-- {: .num_section #sectiona }
=--
## The definition of topos ## {: .num_section}

The hardest part of the definition of [[nlab:topos]] is the concept of [[nlab:subobject classifier]], so I will begin there. For motivation, I will speak of '[[nlab:the category of sets]]' (and [[nlab:functions]]). What exactly this means will be discussed in Section&nbsp;[2](#sectionb), but for now we proceed informally.

In [[nlab:the category of sets]], [[nlab:inverse images]] are a special case of [[nlab:pullbacks]]. That is, given a map $f\colon X \to Y$ of [[nlab:sets]] and a [[nlab:subset]] $B \subseteq Y$, we have a [[nlab:pullback square]]
$$
\begin{matrix} \mathllap{f^{-1}} B & \begin{svg} [[!include SVG rightarrow]]\end{svg} & B \\ \begin{svg} [[!include SVG hookdownarrow]]\end{svg} \mathrlap{\array{\arrayopts{\align{bottom}}\; \begin{svg} [[!include SVG pullback]]\end{svg}\\ \space{30}{10}{1}}} && \begin{svg} [[!include SVG hookdownarrow]]\end{svg} \\ X & \underset{\scriptsize f}{\begin{svg} [[!include SVG rightarrow]]\end{svg}} & Y. \end{matrix}
$$
In particular, this holds when $B$ is a 1-[[nlab:element]] [[nlab:subset]] $\{ y\} $ of $Y$:
$$
\begin{matrix} \mathllap{f^{-1}} \{ y\} & \begin{svg} [[!include SVG rightarrow]]\end{svg} & \{ y\} \\ \begin{svg} [[!include SVG hookdownarrow]]\end{svg} \mathrlap{\array{\arrayopts{\align{bottom}}\;\begin{svg} [[!include SVG pullback]]\end{svg}\\ \space{30}{10}{1}}} && \begin{svg} [[!include SVG hookdownarrow]]\end{svg} \\ X & \underset{\scriptsize f}{\begin{svg} [[!include SVG rightarrow]]\end{svg}} & Y. \end{matrix}
$$
There is no virtue in distinguishing between [[nlab:one-element sets]], so we might as well write $1$ instead of $\{ y\} $; then the inclusion $\{ y\} \hookrightarrow Y$ becomes the map $1 \to Y$ picking out $y \in Y$, and we have a [[nlab:pullback square]]
$$
\begin{matrix} \mathllap{f^{-1}} \{ y\} & \overset{\scriptsize !}{\begin{svg} [[!include SVG rightarrow]]\end{svg}} & 1 \\ \array{\begin{svg} [[!include SVG hookdownarrow]]\end{svg}} \mathrlap{\array{\arrayopts{\align{bottom}}\space{0}{30}{10}\begin{svg} [[!include SVG pullback]]\end{svg}}} && \array{\begin{svg} [[!include SVG downarrow]]\end{svg}} \mathrlap{y} \\ X & \underset{\scriptsize f}{\begin{svg} [[!include SVG rightarrow]]\end{svg}} & Y. \end{matrix}
$$
Next consider [[nlab:characteristic functions]] of [[nlab:subsets]]. Fix a two-[[nlab:element]] [[nlab:set]] $2 = \{ &#x1D5CD;, &#x1D5BF;\} $ ('[[nlab:true]]' and '[[nlab:false]]'). Then for any [[nlab:set]] $X$, the [[nlab:subsets]] of $X$ are in [[nlab:bijective]] [[nlab:correspondence]] with the [[nlab:functions]] $X \to 2$. In one direction, given a [[nlab:subset]] $A \subseteq X$, the corresponding [[nlab:function]] $\chi _{A}\colon X \to 2$ is defined by
$$
\chi _{A}(x) = \begin{cases} &#x1D5CD;&\text{if}\; x \in A \\ &#x1D5BF;&\text{if}\; x \notin A \end{cases}
$$
($x \in X$). In the other, given a [[nlab:function]] $\chi \colon X \to 2$, the corresponding [[nlab:subset]] of $X$ is $\chi ^{-1}\{ &#x1D5CD;\} $. To say that this latter process $\chi \mapsto \chi ^{-1}\{ &#x1D5CD;\} $ is a [[nlab:bijection]] is to say that for all $A \subseteq X$, there is a unique [[nlab:function]] $\chi \colon X \to 2$ such that $A = \chi ^{-1}\{ &#x1D5CD;\} $. In other words: for all $A \subseteq X$, there is a unique [[nlab:function]] $\chi \colon X \to 2$ such that
$$
\begin{matrix} A & \overset{\scriptsize !}{\begin{svg} [[!include SVG rightarrow]]\end{svg}} & 1 \\ \array{\begin{svg} [[!include SVG hookdownarrow]]\end{svg}} && \array{\begin{svg} [[!include SVG downarrow]]\end{svg}} \mathrlap{&#x1D5CD;} \\ X & \underset{\scriptsize \chi }{\begin{svg} [[!include SVG rightarrow]]\end{svg}} & 2 \end{matrix}
$$
is a [[nlab:pullback square]].

This property of [[nlab:sets]] can now be stated in purely categorical terms. We use $\rightarrowtail $ to indicate a [[nlab:mono]] ($=$ [[nlab:monomorphism]] $=$ [[nlab:monic]]).

+-- {: .num_defn #defna .thdefn }
###### Definition ######
Let $\mathcal{E}$ be a [[nlab:category]] with [[nlab:finite limits]]. A **_[[nlab:subobject classifier]]_{: style="font-style: normal"}** in $\mathcal{E}$ is an [[nlab:object]] $\Omega $ together with a map $&#x1D5CD;\colon 1 \to \Omega $ such that for every [[nlab:mono]] $A \stackrel{m}{\rightarrowtail } X$ in $\mathcal{E}$, there exists a unique map $\chi \colon X \to \Omega $ such that
$$
\begin{matrix} A & \overset{\scriptsize !}{\begin{svg} [[!include SVG rightarrow]]\end{svg}} & 1 \\ \mathllap{m}\array{\begin{svg} [[!include SVG downarrowtail]]\end{svg}} && \array{\begin{svg} [[!include SVG downarrow]]\end{svg}} \mathrlap{&#x1D5CD;} \\ X & \underset{\scriptsize \chi }{\begin{svg} [[!include SVG rightarrow]]\end{svg}} & \Omega \end{matrix}
$$
is a [[nlab:pullback square]].
=--

So, we have just observed that $\mathbf{Set}$ has a [[nlab:subobject classifier]], namely, the two-[[nlab:element]] [[nlab:set]]. In the general setting, we may write $\chi $ as $\chi _{A}$ (or properly, $\chi _{m}$) and call it the **_[[nlab:characteristic function]]_{: style="font-style: normal"}** of $A$ (or $m$).

To understand this further, we need two lemmas.

+-- {: .num_defn #defnb .thplain }
###### Lemma ######
In any [[nlab:category]], the [[nlab:pullback]] of a [[nlab:mono]] is a [[nlab:mono]]. That is, if
$$
\begin{matrix} \cdot & \begin{svg} [[!include SVG rightarrow]]\end{svg} & \cdot \\ \mathllap{m'}\array{\begin{svg} [[!include SVG downarrow]]\end{svg}} && \array{\begin{svg} [[!include SVG downarrow]]\end{svg}} \mathrlap{m} \\ \cdot & \begin{svg} [[!include SVG rightarrow]]\end{svg} & \cdot \end{matrix}
$$
is a [[nlab:pullback square]] and $m$ is a [[nlab:mono]], then so is $m'$.
=--

+-- {: .num_defn #defnc .thplain }
###### Lemma ######
In any [[nlab:category]] with a [[nlab:terminal object]] $1$, every map out of $1$ is a mono.
=--

So, pulling $&#x1D5CD;\colon 1 \to \Omega $ back along *any* map $X \to \Omega $ gives a mono into $X$.

It will also help to know the result of the following little exercise ([Johnstone](#citeJohSE) ([2003](#citeJohSE)), A1.6.1). It says, roughly, that in the definition of [[nlab:subobject classifier]], the fact that $1$ is [[nlab:terminal]] comes for free.

+-- {: .num_defn #defnd .thplain }
###### Fact ######
Let $\mathcal{E}$ be a [[nlab:category]] and let $T \stackrel{&#x1D5CD;}{\rightarrowtail } \Omega $ be a mono in $\mathcal{E}$. Suppose that for every mono $A \stackrel{m}{\rightarrowtail } X$ in $\mathcal{E}$, there is a unique map $\chi \colon X \to \Omega $ such that there is a [[nlab:pullback square]]
$$
\begin{matrix} A & \begin{svg} [[!include SVG rightarrow]]\end{svg} & T \\ \mathllap{m}\array{\begin{svg} [[!include SVG downarrowtail]]\end{svg}} && \array{\begin{svg} [[!include SVG downarrowtail]]\end{svg}} \mathrlap{&#x1D5CD;} \\ X & \underset{\scriptsize \chi }{\begin{svg} [[!include SVG rightarrow]]\end{svg}} & \Omega . \end{matrix}
$$
Then $T$ is [[nlab:terminal]] in $\mathcal{E}$.
=--

This leads to a second description of [[nlab:subobject classifiers]]. Let $\mathbf{Mono}(\mathcal{E})$ be the [[nlab:category]] whose [[nlab:objects]] are monos in $\mathcal{E}$ and whose maps are [[nlab:pullback]] squares. Then a [[nlab:subobject classifier]] is exactly a [[nlab:terminal object]] of $\mathbf{Mono}(\mathcal{E})$.

Here is a third way of looking at [[nlab:subobject classifiers]]. Given a [[nlab:category]] $\mathcal{E}$ and an [[nlab:object]] $X$, a **_[[nlab:subobject]]_{: style="font-style: normal"}** of $X$ is officially an [[nlab:isomorphism class]] of monos $A \stackrel{m}{\rightarrowtail } X$ (where [[nlab:isomorphism]] is taken in the [[nlab:slice category]] $\mathcal{E}/X$). For example, when $\mathcal{E}= \mathbf{Set}$, two monos
$$
A \stackrel{m}{\rightarrowtail } X, \quad A' \stackrel{m'}{\rightarrowtail } X
$$
are [[nlab:isomorphic]] if and only if they have the same [[nlab:image]]; so [[nlab:subobjects]] of $X$ correspond one-to-one with [[nlab:subsets]] of $X$. I say 'officially' because half the time people use '[[nlab:subobject]] of $X$' to mean simply 'mono into $X$', or slip between the two meanings without warning. It is a harmless abuse of language, which I will adopt.

For $X \in \mathcal{E}$, let $\mathrm{Sub}(X)$ be the [[nlab:class]] of [[nlab:subobjects]] (in the official sense) of $X$. Assume that $\mathcal{E}$ is [[nlab:well-powered category|well-powered]], that is, each $\mathrm{Sub}(X)$ is a [[nlab:set]] rather than a [[nlab:proper class]]. Assume also that $\mathcal{E}$ has [[nlab:pullbacks]]. By Lemma&nbsp;[2](#defnb), every map $X \stackrel{f}{\to } Y$ in $\mathcal{E}$ induces a map $\mathrm{Sub}(Y) \stackrel{f^{*}}{\to } \mathrm{Sub}(X)$ of [[nlab:sets]], by [[nlab:pullback]]. This defines a [[nlab:functor]] $\mathrm{Sub}\colon \mathcal{E}^{\mathrm{op}}\to \mathbf{Set}$.

Third description: a [[nlab:subobject classifier]] is a [[nlab:representable functor|representation]] of this [[nlab:functor]] $\mathrm{Sub}$.

This makes intuitive sense, since for $\mathrm{Sub}$ to be [[nlab:representable]] means that there is an [[nlab:object]] $\Omega \in \mathcal{E}$ satisfying
$$
\mathrm{Sub}(X) \cong \mathcal{E}(X, \Omega )
$$
naturally in $X \in \mathcal{E}$. In the motivating case of [[nlab:the category of sets]], this directly captures the thought that [[nlab:subsets]] of a [[nlab:set]] $X$ correspond naturally to maps $X \to \{ &#x1D5CD;, &#x1D5BF;\} $.

Now we show that this is [[nlab:equivalent]] to the original definition. By the Yoneda Lemma, a [[nlab:representable functor|representation]] of $\mathrm{Sub}\colon \mathcal{E}^{\mathrm{op}}\to \mathbf{Set}$ amounts to an [[nlab:object]] $\Omega \in \mathcal{E}$ together with an [[nlab:element]] $&#x1D5CD;\in \mathrm{Sub}(\Omega )$ that is 'generic' in the following sense:

> for every [[nlab:object]] $X \in \mathcal{E}$ and [[nlab:element]] $m \in \mathrm{Sub}(X)$, there is a unique map $\chi \colon X \to \Omega $ such that $\chi ^{*}(&#x1D5CD;) = m$.

In other words, a [[nlab:representable functor|representation]] of $\mathrm{Sub}$ is a mono $T \stackrel{&#x1D5CD;}{\rightarrowtail } \Omega $ in $\mathcal{E}$ satisfying the condition in Fact&nbsp;[4](#defnd). In other words, it is a [[nlab:subobject classifier]].

+-- {: .num_defn #defne .thdefn }
###### Definition ######
A **_[[nlab:topos]]_{: style="font-style: normal"}** (or **_[[nlab:elementary topos]]_{: style="font-style: normal"}**) is a [[nlab:cartesian closed category]] with [[nlab:finite limits]] and a [[nlab:subobject classifier]].
=--

+-- {: .num_defn #defnf .thdefn }
###### Examples ######
&nbsp;

1. <p></p>
   +-- {: .num_enuma #enumiAa }
   =--
   The primordial [[nlab:topos]] is $\mathbf{Set}$. It has special properties not shared by most other [[nlab:toposes]]. This is the subject of Section&nbsp;[2](#sectionb).

1. <p></p>
   +-- {: .num_enuma #enumiAb }
   =--
   For any [[nlab:set]] $I$, the [[nlab:category]] $\mathbf{Set}^{I}$ of $I$-indexed [[nlab:families of sets]] is a [[nlab:topos]]. Its [[nlab:subobject classifier]] is the constant [[nlab:family]] $(2)_{i \in I}$, where $2$ is a two-[[nlab:element]] [[nlab:set]].

1. <p></p>
   +-- {: .num_enuma #enumiAc }
   =--
   For any [[nlab:group]] $G$, the [[nlab:category]] $\mathbf{Set}^{G}$ of left $G$-[[nlab:sets]] is a [[nlab:topos]]. Its [[nlab:subobject classifier]] is the [[nlab:set]] $2$ with trivial $G$-[[nlab:action]].

1. <p></p>
   +-- {: .num_enuma #enumiAd }
   =--
   Encompassing all the previous examples, if $\mathbb{A}$ is any [[nlab:small category]] then the [[nlab:category]] $\widehat{\mathbb{A}} = \mathbf{Set}^{\mathbb{A}^{\mathrm{op}}}$ of [[nlab:presheaves]] on $\mathbb{A}$ is a [[nlab:topos]]. We can discover what its [[nlab:subobject classifier]] must be by a thought experiment: *if* $\Omega $ is a [[nlab:subobject classifier]] then by the [[nlab:Yoneda Lemma]],
   $$
   \Omega (a) \cong \widehat{\mathbb{A}}( \mathbb{A}(-, a), \Omega ) \cong \mathrm{Sub}(\mathbb{A}(-, a))
   $$
   for all $a \in \mathbb{A}$. So $\Omega (a)$ must be the [[nlab:set]] of [[nlab:subfunctors]] of $\mathbb{A}(-, a)$; and one can check that defining $\Omega (a)$ in this way does indeed give a [[nlab:subobject classifier]]. A [[nlab:subfunctor]] of $\mathbb{A}(-, a)$ is called a **_[[nlab:sieve]]_{: style="font-style: normal"}** on $a$; it is a [[nlab:collection]] of maps into $a$ satisfying a certain condition.

1. <p></p>
   +-- {: .num_enuma #enumiAe }
   =--
   For any [[nlab:topological space]] $S$, the [[nlab:category]] $\mathbf{Sh}(S)$ of [[nlab:sheaves]] on $S$ is a [[nlab:topos]]. This is the subject of Section&nbsp;[3](#sectionc). Modulo a small lie that I will come back to there, the [[nlab:space]] $S$ can be recovered from the [[nlab:topos]] $\mathbf{Sh}(S)$. Hence the [[nlab:class]] of [[nlab:spaces]] embeds into the [[nlab:class]] of [[nlab:toposes]], and this is why [[nlab:toposes]] can be viewed as generalized [[nlab:spaces]].

   Sheaves will be defined and explained in Section&nbsp;[3](#sectionc). To give a brief sketch: denote by $\mathbf{Open}(S)$ the [[nlab:poset]] of [[nlab:open subsets]] of $S$; then a **_[[nlab:presheaf]]_{: style="font-style: normal"}** on the [[nlab:space]] $S$ is a [[nlab:presheaf]] on the [[nlab:category]] $\mathbf{Open}(S)$, and a [[nlab:sheaf]] on $S$ is a [[nlab:presheaf]] with a further property. I will consistently use '[[nlab:sheaf]]' to mean what some would call '[[nlab:sheaf]] of [[nlab:sets]]'. A [[nlab:sheaf]] of [[nlab:groups]], [[nlab:rings]], etc. is the same as an [[nlab:internal group]], [[nlab:ring]] etc. in $\mathbf{Sh}(S)$.

1. <p></p>
   +-- {: .num_enuma #enumiAf }
   =--
   The [[nlab:category]] $\mathbf{FinSet}$ of [[nlab:finite sets]] is a [[nlab:topos]]. Similarly, $\mathbf{Set}$ can be replaced by $\mathbf{FinSet}$ in all of the previous examples, giving [[nlab:toposes]] of [[nlab:finite]] $G$-sets, [[nlab:finite]] [[nlab:sheaves]], etc.
=--

You might ask 'why is the definition of [[nlab:topos]] what it is? Why that *particular* collection of [[nlab:axioms]]? What's the motivation?' I will not attempt to answer, except by explaining several ways in which the definition has been found useful. It is also worth noting that the [[nlab:topos]] [[nlab:axioms]] have many non-obvious consequences, giving [[nlab:toposes]] a far richer [[nlab:structure]] than most [[nlab:categories]]. For example, every map in a [[nlab:topos]] factorizes, essentially uniquely, as an [[nlab:epi]] followed by a [[nlab:mono]]. More spectacularly, the [[nlab:axioms]] imply that every [[nlab:topos]] has [[nlab:finite]] *co*limits. This can be proved by the following very elegant strategy, due to [Par&#233;](#citePare) ([1974](#citePare)). For every [[nlab:topos]] $\mathcal{E}$, we have the contravariant [[nlab:power set]] [[nlab:functor]] $P = \Omega ^{(-)}\colon \mathcal{E}^{\mathrm{op}}\to \mathcal{E}$. It can be shown that $P$ is [[nlab:monadic]]. But [[nlab:monadic functors]] [[nlab:created limit|create limits]], and $\mathcal{E}$ has [[nlab:finite limits]]. Hence $\mathcal{E}^{\mathrm{op}}$ has [[nlab:finite limits]]; that is, $\mathcal{E}$ has [[nlab:finite colimits]].

+-- {: .num_section #sectionb }
=--
## Toposes and set theory ## {: .num_section}

Here I will describe what makes 'the' [[nlab:category of sets]] special among all [[nlab:toposes]], and explain why I just put 'the' in quotation marks. This is the stuff of revolution: it can completely change your view of [[nlab:set theory]]. It also provides an invaluable insight into [[nlab:topos theory]] as a whole.

We begin by listing some special properties of the [[nlab:topos]] $\mathbf{Set}$, using only the most commonplace assumptions about how [[nlab:sets]] and [[nlab:functions]] behave.

+-- {: .bflist }
1. <p></p>
   +-- {: .num_enumb #enumiBa }
   =--
   The [[nlab:terminal object]] $1$ is a separator ([[nlab:generator]]). That is, given maps $X \underoverset{\quad g \quad }{f}{\rightrightarrows } Y$ in $\mathbf{Set}$, if $f \circ x = g \circ x$ for all $x\colon 1 \to X$ then $f = g$.

   It is worth dwelling on what this says. Maps $1 \to X$ correspond to [[nlab:elements]] of $X$, and we make no notational distinction between the two. Moreover, given an [[nlab:element]] $x \in X$ and a map $f\colon X \to Y$, we can compose the maps
   $$
   1 \stackrel{x}{\to } X \stackrel{f}{\to } Y
   $$
   to obtain a map $f \circ x\colon 1 \to Y$, and this is the map corresponding to the [[nlab:element]] $f(x) \in Y$. (We might harmlessly write both $f \circ x$ and $f(x)$ as $f x$.) Thus, [[nlab:elements]] are a special case of [[nlab:functions]], and [[nlab:evaluation]] is a special case of [[nlab:composition]].

   The property above says that if $f(x) = g(x)$ for all $x \in X$ then $f = g$. In other words, a [[nlab:function]] is determined by its effect on [[nlab:elements]].

1. <p></p>
   +-- {: .num_enumb #enumiBb }
   =--
   Write $0$ for the [[nlab:initial object]] of $\mathbf{Set}$ (the [[nlab:empty set]]). Then $0 \ncong 1$. Equivalently, $\mathbf{Set}$ is not [[nlab:equivalent]] to the [[nlab:terminal category]] $\mathbb{1}$.

   A [[nlab:topos]] satisfying properties&nbsp;[1](#enumiBa) and&nbsp;[2](#enumiBb) is called **_[[nlab:well-pointed topos|well-pointed]]_{: style="font-style: normal"}**.

1. <p></p>
   +-- {: .num_enumb #enumiBc }
   =--
   This property says, informally, that there is a [[nlab:set]] consisting of the [[nlab:natural numbers]].

   What are the 'the [[nlab:natural numbers]]', though? One way to get at an answer is to use the principle that [[nlab:sequences]] can be defined recursively. That is, given a [[nlab:set]] $X$, an [[nlab:element]] $x \in X$, and a map $r\colon X \to X$, there is a unique [[nlab:sequence]] $(x_{n})_{n = 0}^{\infty }$ in $X$ such that
   \begin{equation}
   \label{eqrecursion} x_{0} = x, \quad x_{n + 1} = r(x_{n}) \quad (n \in \mathbb{N}).
   \end{equation}
   A [[nlab:sequence]] $(x_{n})_{n = 0}^{\infty }$ in $X$ is just a map $f\colon \mathbb{N}\to X$, and if we write $s\colon \mathbb{N}\to \mathbb{N}$ for the [[nlab:function]] $n \mapsto n + 1$ ('[[nlab:successor]]'), then&nbsp;\eqref{eqrecursion} says exactly that the diagram
   \begin{equation}
   \label{eqnat} \begin{matrix} 1 & \overset{0}{\begin{svg} [[!include SVG rightarrow]]\end{svg}} & \mathbb{N} & \stackrel{s}{\begin{svg} [[!include SVG rightarrow]]\end{svg}} & \mathbb{N} \\ & \mathrlap{\quad x} \array{\begin{svg} [[!include SVG searrow]]\end{svg}} &\array{\begin{svg} [[!include SVG downarrow]]\end{svg}}\mathrlap{f} & &\array{\begin{svg} [[!include SVG downarrow]]\end{svg}}\mathrlap{f} \\ &&X &\stackrel{r}{\begin{svg} [[!include SVG rightarrow]]\end{svg}} &X \end{matrix}
   \end{equation}
   commutes.

   +-- {: .num_defn #defng .thdefn }
   ###### Definition ######
   Let $\mathcal{E}$ be a [[nlab:category]] with a [[nlab:terminal object]], $1$. A **_[[nlab:natural numbers object]]_{: style="font-style: normal"}** in $\mathcal{E}$ is a triple $(N, 0, s)$, with $N \in \mathcal{E}$, $0\colon 1 \to N$, and $s\colon N \to N$, that is [[nlab:initial]] as such: for any triple $(X, x, r)$ of the same type, there is a unique map $f\colon N \to X$ such that&nbsp;\eqref{eqnat} commutes (with $N$ in place of $\mathbb{N}$).
   =--

   Property&nbsp;[3](#enumiBc) is, then, that $\mathbf{Set}$ has a [[nlab:natural numbers object]].

1. <p></p>
   +-- {: .num_enumb #enumiBd }
   =--
   [[nlab:Epis]] split. That is, for any [[nlab:epimorphism]] ([[nlab:surjection]]) $e\colon X \to Y$ in $\mathbf{Set}$, there exists a map $m\colon Y \to X$ such that $e \circ m = 1_{Y}$. The [[nlab:splitting]] $m$ chooses for each $y \in Y$ an [[nlab:element]] of the [[nlab:nonempty set]] $e^{-1}\{ y\} $. The existence of such [[nlab:splittings]] is precisely the Axiom of [[nlab:Choice]]. Generally, a [[nlab:category]] is said to satisfy the **_Axiom of [[nlab:Choice]]_{: style="font-style: normal"}** (or to 'have [[nlab:Choice]]') if [[nlab:epis]] split.
=--

In summary,

+-- {: style="text-align: center" }
*[[nlab:sets]] and [[nlab:functions]] form a [[nlab:well-pointed topos]]
with [[nlab:natural numbers object]] and [[nlab:Choice]].*
=--

The [[nlab:category of sets]] has many other elementary properties (such as the fact that the [[nlab:subobject classifier]] has exactly two [[nlab:elements]]), but they are all consequences of the properties just mentioned.

But what is this thing called '[[nlab:the category of sets]]'? What do we have to assume about [[nlab:sets]] in order to prove that these properties hold?

Many mathematicians do not like to be bothered with such questions, because they know that the standard answer will be something like '[[nlab:sets]] are anything satisfying the [[nlab:axioms]] of [[nlab:ZFC]]'---and they feel that [[nlab:ZFC]] is irrelevant to what they do, and prefer not to hear about it.

The standard answer is *valid*, in the sense that for every [[nlab:model]] of [[nlab:ZFC]], there is a resulting [[nlab:category of sets]] satisfying the properties above. But it may seem *irrelevant*, because at no point in establishing the properties did it feel necessary to call on an [[nlab:axiom]] system: all the properties are suggested directly by the naive imagery of a [[nlab:set]] as a bag of dots.

There is, however, another type of answer---and this was [[nlab:Lawvere]]'s radical idea. It is this:

+-- {: style="text-align: center" }
*we take the properties above as our [[nlab:axioms]] on [[nlab:sets]].*
=--

In other words, we do away with [[nlab:ZFC]] entirely, and ask instead that [[nlab:sets]] and [[nlab:functions]] form a [[nlab:well-pointed topos]] with [[nlab:natural numbers object]] and [[nlab:Choice]]. 'The' [[nlab:category of sets]] is any [[nlab:category]] satisfying these [[nlab:axioms]]. In fact we should say *a* [[nlab:category of sets]], since there may be many different such [[nlab:categories]], as we shall see.

This is [[nlab:Lawvere]]'s Elementary Theory of the [[nlab:Category]] of Sets ([[nlab:ETCS]]), stated in modern language. (See [Lawvere](#citeLawETCS) ([1964](#citeLawETCS)), or [Lawvere and Rosebrugh](#citeLaRo) ([2003](#citeLaRo)) for a good expository account.) It is nearly fifty years old, but still has not gained the currency it deserves, for reasons on which one can speculate.

+-- {: style="margin-left: 2em" }
##### Digression #####

You might be thinking that this is circular: that this axiomatization of [[nlab:sets]] depends on the notion of [[nlab:category]], and the notion of [[nlab:category]] depends on some notion of [[nlab:collection]] or [[nlab:set]]. But in fact, [[nlab:ETCS]] does not depend on the general notion of [[nlab:category]]. It can be stated without using the word '[[nlab:category]]' once.

To see this, we need to back up a bit. The [[nlab:ZFC]] axiomatization of [[nlab:sets]] looks, informally, like this:

* there are some things called '[[nlab:sets]]'

* there is a [[nlab:binary relation]] '$\in $' on [[nlab:sets]]

* some [[nlab:axioms]] hold.

People seeing this (or the formal version) often ask certain questions. What does 'some things' mean? Do you mean that there is a *[[nlab:set]]* of [[nlab:sets]]? (No.) What exactly is meant by '[[nlab:binary relation]]'? (It means that for each [[nlab:set]] $X$ and [[nlab:set]] $Y$, the statement '$X \in Y$' is deemed to be either [[nlab:true]] or [[nlab:false]].) What do you mean, 'deemed'? Etc. This is not a [[nlab:logic]] course, and I will not attempt to answer the questions except to say that there is an assumed common understanding of these terms. To hide behind jargon, [[nlab:ZFC]] is a [[nlab:predicate logic|first-order theory]].

The [[nlab:ETCS]] axiomatization of [[nlab:sets]] looks like this:

* there are some things called '[[nlab:sets]]'

* for each [[nlab:set]] $X$ and [[nlab:set]] $Y$, there are some things called '[[nlab:functions]] from $X$ to $Y$'

* for each [[nlab:set]] $X$, [[nlab:set]] $Y$ and [[nlab:set]] $Z$, there is a [[nlab:binary operation]] assigning to each pair of [[nlab:functions]]
  $$
  f\colon X \to Y, \quad g\colon Y \to Z
  $$
  a [[nlab:function]] $g \circ f\colon X \to Z$

* some [[nlab:axioms]] hold.

You can ask the same kind of logical questions as for [[nlab:ZFC]]---what exactly is meant by '[[nlab:binary operation]]'? etc.---which again I will not attempt to answer. The difficulties are no worse than for [[nlab:ZFC]], and again, in the jargon, [[nlab:ETCS]] is a [[nlab:predicate logic|first-order theory]].

Stated in this way, the [[nlab:ETCS]] [[nlab:axioms]] begin by saying that [[nlab:composition]] is [[nlab:associative]] and has [[nlab:identities]] (so that [[nlab:sets]], [[nlab:functions]] and [[nlab:composition]] of [[nlab:functions]] define a [[nlab:category]]); then they say that binary [[nlab:products]] and [[nlab:equalizers]] of [[nlab:sets]] exist, and there is a [[nlab:terminal]] [[nlab:set]] (so that [[nlab:the category of sets]] has [[nlab:finite limits]]); and so on, until we have said that [[nlab:sets]] and [[nlab:functions]] form a [[nlab:well-pointed topos]] with [[nlab:natural numbers object]] and [[nlab:Choice]]. You can do it in about ten [[nlab:axioms]].

Here ends the digression.
=--

[[nlab:ZFC]] axiomatizes [[nlab:sets]] and membership, whereas [[nlab:ETCS]] axiomatizes [[nlab:sets]] and [[nlab:functions]]. Anything that can be expressed in one language can be expressed in the other: in the usual implementation of [[nlab:ZFC]], a [[nlab:function]] $X \to Y$ is defined as a suitable [[nlab:subset]] of $X \times Y$, and in [[nlab:ETCS]], an [[nlab:element]] of $X$ is defined as a [[nlab:function]] from the [[nlab:terminal]] [[nlab:set]] to $X$. But an advantage of the categorical approach is that it avoids the chains of [[nlab:elements]] of [[nlab:elements]] of [[nlab:elements]] that are so important in traditional [[nlab:set theory]], yet seem so distant from most of mathematics.

[[nlab:ZFC]] is slightly stronger than [[nlab:ETCS]]. 'Stronger' means that everything that can be deduced about [[nlab:sets]] from the [[nlab:ETCS]] [[nlab:axioms]] can also be deduced in [[nlab:ZFC]], but not vice versa. 'Slightly' is meant in a sociological sense. I believe it has been said that the mathematics in an ordinary undergraduate syllabus (excluding, naturally, any course in [[nlab:ZFC]]) makes no more assumptions about [[nlab:sets]] than are made by [[nlab:ETCS]]. If that is so, it must also be the case that for many mathematicians, nothing in their entire research career requires more than [[nlab:ETCS]].

The technical relationship between [[nlab:ZFC]] and [[nlab:ETCS]] is well understood. It is known exactly which fragment of [[nlab:ZFC]] is [[nlab:equivalent]] to [[nlab:ETCS]] (namely, 'bounded' or 'restricted' Zermelo with [[nlab:Choice]]; see [Mac&nbsp;Lane and Moerdijk](#citeMaMo) ([1994](#citeMaMo))). It is also known what needs to be added to [[nlab:ETCS]] in order to obtain a system of [[nlab:equal]] strength to [[nlab:ZFC]]. This extra ingredient is an [[nlab:axiom]] scheme (a countably infinite [[nlab:family]] of [[nlab:axioms]]) that [[nlab:set]] theorists in the traditional mould would call Replacement, and [[nlab:category]] theorists would call a form of [[nlab:cocomplete category|cocompleteness]]. It says, informally, that given any [[nlab:set]] $I$ and [[nlab:family]] $(X_{i})_{i \in I}$ of [[nlab:sets]] specified by a first-order formula, the [[nlab:coproduct]] $\sum _{i \in I} X_{i}$ exists. The existence of this [[nlab:coproduct]] is expressed by saying that there exist a [[nlab:set]] $X$ and a map $p\colon X \to I$ (to be thought of as the [[nlab:projection]] $\sum _{i \in I} X_{i} \to I$) such that for each $i \in I$, the [[nlab:inverse image]] $p^{-1}\{ i\} $ is [[nlab:isomorphic]] to $X_{i}$. See Section&nbsp;8 of [McLarty](#citeMcLECS) ([2004](#citeMcLECS)) for details.

[[nlab:Topos]] theory therefore provides a different viewpoint on [[nlab:set theory]]. Let us take a brief look from this new viewpoint at a famous theorem of [[nlab:set theory]]: that the Continuum Hypothesis is independent of the usual [[nlab:set]]-theoretic [[nlab:axioms]], as proved by G&#246;del and Cohen.

Temporarily, let us say that a '[[nlab:category of sets]]' is a [[nlab:well-pointed topos]] with [[nlab:natural numbers object]] and [[nlab:Choice]], satisfying the [[nlab:axiom]] scheme of Replacement. A [[nlab:category of sets]] is said to **_satisfy the Continuum Hypothesis_{: style="font-style: normal"}** if for all [[nlab:objects]] $X$,
$$
\begin{aligned}
&\text{there exist monos}\; N \rightarrowtail X \rightarrowtail 2^{N} \\ \implies &X \cong N \;\text{or}\; X \cong 2^{N}.
\end{aligned}
$$
(As usual, $N$ denotes the [[nlab:natural numbers object]]; $2$ is the [[nlab:subobject classifier]].) Stated categorically, the theorem is this: given any [[nlab:category of sets]], you can build one that satisfies the Continuum Hypothesis and one that does not. This is only a rephrasing of the standard statement, but if you are more at home with the term '[[nlab:category]]' than with '[[nlab:model]] of a first-order [[nlab:theory]]', you might find it less mysterious.

So far we have seen the benefits of viewing the/a [[nlab:category of sets]] as a special [[nlab:topos]]. But the other way round, there are great benefits to viewing a [[nlab:topos]] as a generalized [[nlab:category of sets]]. For example, we might view $\mathbf{Set}^{\mathbb{N}}$ as [[nlab:the category of sets]] varying through (discrete) time. The [[nlab:set]] of human beings alive today is an [[nlab:object]] of $\mathbf{Set}^{\mathbb{N}}$: as the meaning of 'today' changes, the [[nlab:set]] changes. A [[nlab:sheaf]] can similarly be understood as a [[nlab:set]] varying through [[nlab:space]].

People (especially [[nlab:Lawvere]]) sometimes refer to [[nlab:the category of sets]] as the (or a) [[nlab:topos]] of *constant* [[nlab:sets]], to contrast it with [[nlab:toposes]] of variable [[nlab:sets]]. There are also [[nlab:toposes]] whose [[nlab:objects]] can informally be thought of as '[[nlab:cohesive topos|cohesive]]' [[nlab:sets]], which means the following. In an ordinary [[nlab:set]], the points have no relation or attachment to each other: they do not 'cohere'. But a [[nlab:cohesive topos|cohesive]] [[nlab:set]] carries something like a [[nlab:topology]] or [[nlab:smooth structure]], so that the points are in some sense stuck together. For example, there are [[nlab:toposes]] of [[nlab:smooth spaces]], which are the setting for [[nlab:synthetic differential geometry]]. From this point of view, the [[nlab:category]] of ordinary [[nlab:sets]] is extreme among all [[nlab:toposes]]: its [[nlab:objects]] are [[nlab:sets]] with no variation or cohesion at all.

Viewing the [[nlab:objects]] of a [[nlab:topos]] as generalized [[nlab:sets]] is much more than a useful mental technique. In fact, it is valid to use [[nlab:set]]-like language and reasoning in *any* [[nlab:topos]], provided that we stick to certain rules. This language is called the '[[nlab:internal language]]' of the [[nlab:topos]].

Many of the central ideas of [[nlab:topos theory]] are simple, but that simplicity can easily be obscured by the richness of structure available in a [[nlab:topos]]. Such is the case for the [[nlab:internal language]]. I will therefore describe the idea in a much more basic setting.

First let $\mathcal{E}$ be any [[nlab:category]] whatsoever, and let $X$ be an [[nlab:object]] of $\mathcal{E}$. A **_[[nlab:generalized element]]_{: style="font-style: normal"}** of $X$ is simply a map in $\mathcal{E}$ with [[nlab:codomain]] $X$. A [[nlab:generalized element]] $x\colon S \to X$ may be said to be of **_shape_{: style="font-style: normal"}** $S$, or to be an **_$S$-[[nlab:element]]_{: style="font-style: normal"}** of $X$. In the special case that $S$ is [[nlab:terminal]], $S$-[[nlab:elements]] are called **_[[nlab:global elements]]_{: style="font-style: normal"}**. (See Example&nbsp;[9](#defni)([3](#enumiDc)) for a hint on the reason for the name.) In [[nlab:the category of sets]], the [[nlab:global elements]] are the ordinary [[nlab:elements]], but in other [[nlab:categories]], the [[nlab:global elements]] might be very uninteresting: consider the [[nlab:category]] of [[nlab:groups]], for instance.

Given a map $f\colon X \to Y$ in $\mathcal{E}$, any [[nlab:generalized element]] $x$ of $X$ gives rise to a [[nlab:generalized element]] $f x$ of $Y$. This is the [[nlab:composite]] $f \circ x$, but can also be thought of as '$f(x)$': see the remarks on property&nbsp;[1](#enumiBa) at the beginning of this section. For maps $X \underoverset{\quad g \quad }{f}{\rightrightarrows } Y$, we have
$$
f = g \iff f x = g x \;\text{for all generalized elements}\; x \;\text{of}\; X.
$$
(Proof of $\Leftarrow $: take $x = 1_{X}$.) This is emphatically not true if we replace 'generalized' by 'global': again, consider [[nlab:groups]].

This language of [[nlab:generalized elements]] is the **_[[nlab:internal language]]_{: style="font-style: normal"}** of the [[nlab:category]]. It fits well with ordinary categorical terminology and [[nlab:notation]]. For example, let $\mathcal{E}$ be a [[nlab:category]] with [[nlab:finite]] [[nlab:products]]. In the [[nlab:internal language]], the definition of [[nlab:product]] reads, informally: an $S$-[[nlab:element]] of $X \times Y$ consists of an $S$-[[nlab:element]] of $X$ together with an $S$-[[nlab:element]] of $Y$. Apart from the '$S$-' prefixes, this is identical to the ordinary description of the [[nlab:cartesian product]] of [[nlab:sets]] $X$ and $Y$. And in standard categorical [[nlab:notation]], the map $S \to X \times Y$ with components $x\colon S \to X$ and $y\colon S \to Y$ is denoted by $(x, y)$, thus extending the [[nlab:set]]-theoretic [[nlab:notation]] for a (global) [[nlab:element]] of a [[nlab:cartesian product]].

To see why the [[nlab:internal language]] is useful, consider, for instance, [[nlab:internal groups]] in a [[nlab:finite]] [[nlab:product category]] $\mathcal{E}$. A [[nlab:group]] in $\mathcal{E}$ is an [[nlab:object]] $X$ together with maps
$$
m\colon X \times X \to X, \quad i\colon X \to X, \quad e\colon 1 \to X
$$
satisfying some [[nlab:axioms]]. Those [[nlab:axioms]] are usually expressed as [[nlab:commutative diagrams]], which have been obtained by translating the classical [[nlab:axioms]] into diagrammatic form. But there is no need to translate them: the classical [[nlab:axioms]] can simply be repeated verbatim and interpreted as statements about *generalized* [[nlab:elements]]. This is [[nlab:equivalent]]. For example, it is easy to show that the [[nlab:commutative diagram]] for [[nlab:associativity]] is [[nlab:equivalent]] to the statement that
\begin{equation}
\label{eqassoc} m(m(x, y), z) = m(x, m(y, z))
\end{equation}
for all [[nlab:generalized elements]] $x, y, z$ of $X$ of the same shape. (They have to be the same shape in order for expressions such as $(x, y)$ to make sense.) And just as for ordinary [[nlab:elements]] in $\mathbf{Set}$, there is no harm in writing $xy$ instead of $m(x, y)$, and similarly $x^{-1}$ instead of $i(x)$.

More valuably still, *proofs* written down in the classical [[nlab:set]]-theoretic scenario will actually be valid in an arbitrary [[nlab:finite]] [[nlab:product category]] $\mathcal{E}$, as long as whatever was said about [[nlab:elements]] in $\mathbf{Set}$ is also true for [[nlab:generalized elements]] in $\mathcal{E}$. For example, whenever $X$ is a [[nlab:group]] in $\mathbf{Set}$ and $x, y, a \in X$, we have
\begin{equation}
\label{eqcancellation} x a = y a \implies x = y.
\end{equation}
Proof:
$$
\begin{aligned}
x a = y a & \implies (x a)a^{-1} = (y a)a^{-1} \implies x(a a^{-1}) = y(a a^{-1}) \\ & \implies x e = y e \implies x = y.
\end{aligned}
$$
We can immediately conclude that the [[nlab:implication]]&nbsp;\eqref{eqcancellation} holds whenever $X$ is a [[nlab:group]] in an arbitrary [[nlab:finite]] [[nlab:product category]] $\mathcal{E}$ and $x, y, a$ are [[nlab:generalized elements]] of $X$ of the same shape. Indeed, each step in the proof is an application of an [[nlab:axiom]] such as&nbsp;\eqref{eqassoc} valid in the general setting.

The [[nlab:internal language]] is a massively labour-saving device. To prove that an equation valid in ordinary [[nlab:groups]] is also valid for [[nlab:internal groups]], you merely need to cast an eye over the proof and convince yourself that it holds for [[nlab:generalized elements]] too. In contrast, try proving the internal version of the equation
\begin{equation}
\label{eqinverse} y^{-1} x^{-1} = (x y)^{-1}
\end{equation}
by diagrammatic methods. First it has to be *stated* diagrammatically. It says that the diagram
$$
\begin{matrix} X \times X & \overset{\text{sym}}{\begin{svg} [[!include SVG rightarrow]]\end{svg}}\; X \times X\; \overset{i \times i}{\begin{svg} [[!include SVG rightarrow]]\end{svg}} & X \times X \\ \mathllap{\quad m} \array{\begin{svg} [[!include SVG downarrow]]\end{svg}} && \array{\begin{svg} [[!include SVG downarrow]]\end{svg}} \mathrlap{m} \\ X & \underset{i}{\begin{svg} [[!include SVG triplelengthrightarrow]]\end{svg}} & X \end{matrix}
$$
commutes. Then it has to be *proved*, by filling the inside of this diagram with instances of the diagrams encoding the [[nlab:group]] [[nlab:axioms]]. (It seems to need at least ten or so inner diagrams.) But once you have an elementwise proof, all this effort is unnecessary. And the example&nbsp;\eqref{eqinverse} chosen was very simple: for more complex statements, the benefits of the [[nlab:internal language]] become clearer still.

The [[nlab:internal language]] of [[nlab:toposes]] is similar to that of [[nlab:finite product]] [[nlab:categories]], but much richer. As well as being able to form pairs $(x, y)$ of [[nlab:generalized elements]], we can take [[nlab:generalized elements]] of exponentials $Y^{X}$ (to be thought of as [[nlab:families]] of maps $X \to Y$), form [[nlab:subobjects]] such as
$$
\{ x \in X \:|\:f x = g x \}
$$
(the [[nlab:equalizer]] of $X \underoverset{\quad g \quad }{f}{\rightrightarrows } Y$), and so on. Almost anything that can be expressed or proved in [[nlab:the category of sets]] can be reproduced in an arbitrary [[nlab:topos]]. The only sticking points are the law of the [[nlab:excluded middle]] and the [[nlab:axiom of choice]]. Any proof that avoids those---any [[nlab:constructive]] proof, in a sense that can be made precise---generalizes to an arbitrary [[nlab:topos]].

Phrases with more or less the same meaning as '[[nlab:internal language]]' are '[[nlab:Mitchell--Bénabou language]]' and '[[nlab:internal logic]]'. See, for instance, [Mac&#160;Lane and Moerdijk](#citeMaMo) ([1994](#citeMaMo)) or [Johnstone](#citeJohSE) ([2003](#citeJohSE)). There you can also find more spectacular applications of [[nlab:topos theory]] to [[nlab:set theory]], including topics such as [[nlab:forcing]].

+-- {: .num_section #sectionc }
=--
## Toposes and geometry ## {: .num_section}

This section covers concepts such as [[nlab:sheaf]], [[nlab:geometric morphism]] (map of [[nlab:toposes]]), [[nlab:Grothendieck topos]], and [[nlab:locale]]. But the most important thing I want to explain is how and why [[nlab:geometry]] has inspired so much of [[nlab:topos theory]].

### Sheaves ###

Let $X$ be a [[nlab:topological space]]. (Following tradition, I will switch from my previous convention of using $X$ to denote an [[nlab:object]] of a [[nlab:topos]].) Write $\mathbf{Open}(X)$ for its [[nlab:poset]] of [[nlab:open subsets]]. A [[nlab:presheaf]] on $X$ is a [[nlab:functor]] $F\colon \mathbf{Open}(X)^{\mathrm{op}}\to \mathbf{Set}$. It assigns to each [[nlab:open subset]] $U$ a [[nlab:set]] $F(U)$, whose [[nlab:elements]] are called **_[[nlab:sections]] over $U$_{: style="font-style: normal"}** (for reasons to be explained). It also assigns to each open $V \subseteq U$ a [[nlab:function]] $F(U) \to F(V)$, called **_[[nlab:restriction]]_{: style="font-style: normal"}** from $U$ to $V$ and denoted by $s \mapsto s\vert _{V}$. I will write $\mathbf{Psh}(X)$ for the [[nlab:category of presheaves]] on $X$.

+-- {: .num_defn #defnh .thdefn }
###### Examples ######
&nbsp;

1. <p></p>
   +-- {: .num_enumc #enumiCa }
   =--
   Let $F(U) = \{ \text{[[nlab:continuous functions]]}\; U \to \mathbb{R}\} $; [[nlab:restriction]] is [[nlab:restriction]].

1. <p></p>
   +-- {: .num_enumc #enumiCb }
   =--
   The same, but with 'bounded' in place of '[[nlab:continuous function|continuous]]'.
=--

Examples&nbsp;[1](#enumiCa) and&nbsp;[2](#enumiCb) are qualitatively different: continuity is a local [[nlab:property]], but boundedness is not. This difference can be captured by asking the following question. Let $(U_{i})_{i \in I}$ be a [[nlab:family]] of [[nlab:open subsets]] of $X$, and take, for each $i \in I$, a [[nlab:section]] $s_{i} \in F(U_{i})$. Might there be some $s \in F(\bigcup _{i \in I} U_{i})$ such that $s\vert _{U_{i}} = s_{i}$ for all $i$?

For this to stand a chance of being true, functoriality demands that the [[nlab:sections]] $s_{i}$ must satisfy a 'matching condition': $s_{i}\vert _{U_{i} \cap U_{j}} = s_{j}\vert _{U_{i} \cap U_{j}}$ for all $i$ and $j$. A **_[[nlab:sheaf]]_{: style="font-style: normal"}** is a [[nlab:presheaf]] such that for every [[nlab:family]] $(U_{i})_{i \in I}$ of [[nlab:open sets]] and every [[nlab:matching family]] $(s_{i})_{i \in I}$, there is a unique $s \in F(\bigcup _{i \in I} U_{i})$ such that $s\vert _{U_{i}} = s_{i}$ for all $i \in I$.

+-- {: .num_defn #defni .thdefn }
###### Examples ######
&nbsp;

1. <p></p>
   +-- {: .num_enumd #enumiDa }
   =--
   The first example above, with [[nlab:continuous functions]], is a [[nlab:sheaf]]. The proof can be split into two parts. Given $(U_{i})$ and $(s_{i})$, there is certainly a unique *[[nlab:function]]* $s\colon \bigcup U_{i} \to \mathbb{R}$ ([[nlab:continuous function|continuous]] or not) such that $s\vert _{U_{i}} = s_{i}$ for all $i$. The question now is whether $s$ is [[nlab:continuous function|continuous]]; and because continuity is a local property, it is.

1. <p></p>
   +-- {: .num_enumd #enumiDb }
   =--
   The second example above, with bounded [[nlab:functions]], is not a [[nlab:sheaf]] (for a general [[nlab:space]] $X$). This is because boundedness is *not* a local property.

1. <p></p>
   +-- {: .num_enumd #enumiDc }
   =--
   The [[nlab:sheaf]] of [[nlab:continuous function|continuous]] real-valued [[nlab:functions]] is rather floppy, in the sense that there are usually many ways to extend a [[nlab:continuous function]] from a smaller [[nlab:set]] to a larger one. Often people consider [[nlab:sheaves]] made up of [[nlab:holomorphic function|holomorphic]] or [[nlab:rational functions]], which are much more rigid: there are typically few or no ways to extend. It is quite normal for there to be no [[nlab:global sections]] ([[nlab:sections]] over $X$) at all.

1. <p></p>
   +-- {: .num_enumd #enumiDd }
   =--
   Take any [[nlab:continuous map]] $Y \stackrel{p}{\to } X$ of [[nlab:topological spaces]] (which can be thought of as a kind of [[nlab:bundle]] over $X$). Then there arises a [[nlab:sheaf]] $F$ on $X$, in which $F(U)$ is the [[nlab:set]] of [[nlab:continuous maps]] $s\colon U \to Y$ such that the triangle on the left commutes:
   $$
   \array{ \arrayopts{\rowalign{bottom}} \begin{matrix} && Y \\ &\mathllap{\quad s} \array{\begin{svg} [[!include SVG nearrow]]\end{svg}} & \array{\begin{svg} [[!include SVG downarrow]]\end{svg}}\mathrlap{p} \\ U & \begin{svg} [[!include SVG hookrightarrow]]\end{svg} & X \end{matrix}& \qquad \qquad \qquad &\begin{svg}
   <svg width="454" height="323" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="61448">
   <g>
   <title>Layer 1</title>
   <rect id="svg_{6}1448_{1}" height="100" width="150" y="101" x="301" stroke-width="2" stroke="#000000" fill="#ffaa56"/>
   <rect id="svg_{6}1448_{2}" height="0" width="0" y="192" x="435" opacity="0.5" stroke-width="2" stroke="#000000" fill="#FF0000"/>
   <line id="svg_{6}1448_{3}" y2="301" x2="451" y1="301" x1="301" stroke-width="2" stroke="#000000" fill="none"/>
   <line id="svg_{6}1448_{4}" y2="301" x2="151" y1="301" x1="101" stroke-width="2" stroke="#000000" fill="none"/>
   <line id="svg_{6}1448_{5}" y2="301" x2="381" y1="301" x1="331" stroke-width="5" stroke="#000000" fill="none"/>
   <rect opacity="0.5" id="svg_{6}1448_{6}" height="100" width="50" y="101" x="331" stroke-width="2" stroke="#000000" fill="#7f0000"/>
   <path id="svg_{6}1448_{7}" d="m330.5,165c33.666687,12.333344 28.333313,-43.333336 50,-44" stroke-width="3" stroke="#000000" fill="none"/>
   <line id="svg_{6}1448_{8}" y2="156.484044" x2="276.515956" y1="274" x1="159" stroke="#000000" fill="none"/>
   <line id="svg_{6}1448_{9}" y2="288.344236" x2="361" y1="217" x1="361" stroke="#000000" fill="none"/>
   <line id="svg_{6}1448_{1}0" y2="288" x2="368" y1="288" x1="368" opacity="0.5" stroke="#000000" fill="none"/>
   <line id="svg_{6}1448_{1}1" y2="299" x2="170" y1="299" x1="170" opacity="0.5" stroke="#000000" fill="none"/>
   <path id="svg_{6}1448_{1}2" d="m182.222504,290.555328c-2.499664,-0.322754 -5.507187,2.338531 -5.165527,5.222229c-0.314697,2.735504 1.386536,5.264587 5.05603,5.444427l99.891998,-0.221985" stroke="#000000" fill="none"/>
   <line id="svg_{6}1448_{1}3" y2="300" x2="280" y1="300" x1="280" opacity="0.5" stroke="#000000" fill="none"/>
   <foreignObject height="20" width="48" font-size="16" id="svg_{6}1448_{1}4" y="302" x="103">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
   <semantics>
   <mrow>
   <mi>U</mi>
   </mrow>
   <annotation encoding="application/x-tex">U</annotation>
   </semantics>
   </math>
   </foreignObject>
   <foreignObject height="20" width="48" font-size="16" id="svg_{6}1448_{1}5" y="302" x="400">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
   <semantics>
   <mrow>
   <mi>X</mi>
   </mrow>
   <annotation encoding="application/x-tex">X</annotation>
   </semantics>
   </math>
   </foreignObject>
   <foreignObject height="20" width="48" font-size="16" id="svg_{6}1448_{1}6" y="237" x="347">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
   <semantics>
   <mrow>
   <mi>p</mi>
   </mrow>
   <annotation encoding="application/x-tex">p</annotation>
   </semantics>
   </math>
   </foreignObject>
   <foreignObject height="20" width="48" font-size="16" id="svg_{6}1448_{1}7" y="176" x="406">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
   <semantics>
   <mrow>
   <mi>Y</mi>
   </mrow>
   <annotation encoding="application/x-tex">Y</annotation>
   </semantics>
   </math>
   </foreignObject>
   <foreignObject height="20" width="48" font-size="16" id="svg_{6}1448_{1}8" y="193" x="178">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
   <semantics>
   <mrow>
   <mi>s</mi>
   </mrow>
   <annotation encoding="application/x-tex">s</annotation>
   </semantics>
   </math>
   </foreignObject>
   <foreignObject id="svg_{6}1448_{1}9" height="20" width="48" font-size="16" y="303" x="332">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
   <semantics>
   <mrow>
   <mi>U</mi>
   </mrow>
   <annotation encoding="application/x-tex">U</annotation>
   </semantics>
   </math>
   </foreignObject>
   <path id="svg_{6}1448_{2}5" d="m351,276c3.22226,1.814819 7.666687,5.407318 10,13c2.111084,-7.296417 6.333344,-12.148071 10,-13" stroke="#000000" fill="none"/>
   <path transform="rotate(-90, 276.11, 300.944)" id="svg_{6}1448_{2}6" d="m266.111115,294.444458c3.221985,1.815002 7.666992,5.407013 10,13c2.110992,-7.29599 6.333008,-12.14801 10,-13" stroke="#000000" fill="none"/>
   <path id="svg_{6}1448_{2}7" transform="rotate(-135, 273.001, 160.056)" d="m263.000031,153.555588c3.221985,1.815002 7.666992,5.407013 10,13c2.110992,-7.29599 6.333008,-12.14801 10,-13" stroke="#000000" fill="none"/>
   </g>
   </svg>

   \end{svg}}
   $$
   Such an $s$ is precisely a [[nlab:right inverse]], or '[[nlab:section]]', of the map $p^{-1}U \to U$ induced by $p$.
=--

There is also an abstract categorical explanation of where the concept of [[nlab:sheaf]] comes from. Fix a [[nlab:space]] $X$. We have a [[nlab:functor]]
$$
I\colon \mathbf{Open}(X) \to \mathbf{TopSp}/X
$$
where $\mathbf{TopSp}$ is the [[nlab:category]] of [[nlab:topological spaces]], $\mathbf{TopSp}/X$ is the [[nlab:slice category]], and $I(U) = (U \hookrightarrow X)$. This [[nlab:functor]] $I$ embodies the simple thought that an [[nlab:open subset]] of a [[nlab:topological space]] can be treated as a [[nlab:space]] in its own right. We now apply to $I$ two very general categorical constructions, from which the [[nlab:sheaf]] concept will appear automatically.

First, purely because the [[nlab:domain]] of $I$ is small and the [[nlab:codomain]] has small [[nlab:colimits]], there is an induced [[nlab:adjunction]]
$$
\mathbf{Psh}(X) = \mathbf{Set}^{\mathbf{Open}(X)^{\mathrm{op}}} \underoverset{Hom(I,-)}{-\otimes I}{\underoverset{\leftarrow }{\rightarrow }{\quad \perp \quad }} \mathbf{TopSp}/X.
$$
The [[nlab:right adjoint]] is given by
$$
(\mathrm{Hom}(I, Y))(U) = \mathbf{TopSp}/X \, (I(U), Y)
$$
where $Y = \left ( \begin{matrix} Y\\ \downarrow \mathrlap{p}\\ X\end{matrix}\;\right ) \in \mathbf{TopSp}/X$ and $U \in \mathbf{Open}(X)$. This is, in fact, the process described in Example&nbsp;[9](#defni)([4](#enumiDd)): the [[nlab:sheaf]] $F$ defined there is $\mathrm{Hom}(I, Y)$. The [[nlab:left adjoint]] can be described as a [[nlab:coend]] or [[nlab:colimit]]: for $F \in \mathbf{Psh}(X)$,
$$
F \otimes I = \int ^{U} F(U) \times I(U) = \Bigl ( \bigl ( \displaystyle \lim _{\rightarrow U, s}\, U \bigr ) \to X \Bigr )
$$
where the [[nlab:colimit]] is over all $U \in \mathbf{Open}(X)$ and $s \in F(U)$, and the map from the [[nlab:colimit]] to $X$ is the canonical one.

<div id="padjneqv"></div>
Second, every [[nlab:adjunction]] restricts canonically to an [[nlab:equivalence]] between [[nlab:full subcategories]]: one consists of the [[nlab:objects]] at which the [[nlab:unit of the adjunction]] is an [[nlab:isomorphism]], and the other of the [[nlab:objects]] at which the [[nlab:counit]] is an [[nlab:isomorphism]]. Write the [[nlab:equivalence]] obtained from the [[nlab:adjunction]] above as
$$
\mathbf{Sh}(X) \underoverset{\leftarrow }{\rightarrow }{\quad \simeq \quad } \mathbf{Et}(X).
$$
It can be shown that this $\mathbf{Sh}(X)$ is the same [[nlab:category of sheaves]] as before. In this way, the notion of [[nlab:sheaf]] arises canonically from the very simple [[nlab:functor]] $I\colon \mathbf{Open}(X) \to \mathbf{TopSp}/X$. The notion of [[nlab:étale space|étale bundle]] also arises canonically: [[nlab:étale space|étale bundles]] over $X$ are (by definition, if you like) the [[nlab:objects]] of $\mathbf{Et}(X)$. Among other things, this [[nlab:equivalence]] shows that every [[nlab:sheaf]] is of the form described in Example&nbsp;[9](#defni)([4](#enumiDd)). See [Mac&nbsp;Lane and Moerdijk](#citeMaMo) ([1994](#citeMaMo)) for details.

One way or another, we have the [[nlab:category]] $\mathbf{Sh}(X)$ of [[nlab:sheaves]] on $X$. It is a [[nlab:topos]]. Its [[nlab:subobject classifier]] $\Omega $ is given by
$$
\Omega (U) = \{ \text{open subsets of } U \} .
$$
The crucial fact about $\mathbf{Sh}(X)$ is that---modulo a small lie that I will repair later---

+-- {: style="text-align: center" }
*$X$ can be recovered from $\mathbf{Sh}(X)$.*
=--

So the [[nlab:class]] of [[nlab:topological spaces]] embeds into the [[nlab:class]] of [[nlab:toposes]]. We can think of [[nlab:toposes]] as generalized [[nlab:spaces]].

A common technique in [[nlab:topos theory]] is to take a concept from [[nlab:topology]] or [[nlab:geometry]] and extend it to [[nlab:toposes]]. For example, suppose you hear someone talking about '[[nlab:connected toposes]]'. You may have no idea what one is, but you can bet that the definition has been obtained by determining what [[nlab:property]] of the [[nlab:topos]] $\mathbf{Sh}(X)$ corresponds to connectedness of the [[nlab:space]] $X$, then taking that as the definition of connectedness for all [[nlab:toposes]].

The next few subsections are all examples of this generalization process.

### Geometric morphisms ###

So far I have said nothing about maps between [[nlab:toposes]]. There is an obvious candidate for what a map of [[nlab:toposes]] should be: a [[nlab:functor]] preserving [[nlab:finite limits]], [[nlab:exponential object|exponentials]], and [[nlab:subobject classifiers]]. Such a [[nlab:functor]] is called a **_[[nlab:logical morphism]]_{: style="font-style: normal"}**. They have a part to play, but there is another notion of map of [[nlab:toposes]] that has been found much more useful. It can be derived by generalizing from [[nlab:topology]].

Every map $f\colon X \to Y$ in $\mathbf{TopSp}$ induces an [[nlab:adjunction]]
\begin{equation}
\label{eqShGM} \mathbf{Sh}(X) \underoverset{f_{*}}{f^{*}}{\underoverset{\rightarrow }{\leftarrow }{\quad \scriptsize \scriptsize \bot \quad }} \mathbf{Sh}(Y).
\end{equation}
This is not obvious. The [[nlab:right adjoint]] $f_{*}$ is easy to construct---
$$
(f_{*} F)(V) = F(f^{-1} V)
$$
($F \in \mathbf{Sh}(X)$, $V \in \mathbf{Open}(Y)$)---but the [[nlab:left adjoint]] $f^{*}$ is harder. It can be made easy by invoking the [[nlab:equivalence]] between [[nlab:sheaves]] and [[nlab:étale space|étale bundles]]; but I will not go into that, or give any other description of $f^{*}$.

It is a fact that $f^{*}$ preserves [[nlab:finite limits]]. It is also a fact (modulo the usual small lie) that there is a natural [[nlab:correspondence]] between [[nlab:continuous maps]] $X \to Y$ and [[nlab:adjunctions]]&nbsp;\eqref{eqShGM} in which the [[nlab:left adjoint]] preserves [[nlab:finite limits]]. So now we know what [[nlab:continuous maps]] look like in [[nlab:topos]]-theoretic terms. We duly generalize:

+-- {: .num_defn #defnj .thdefn }
###### Definition ######
Let $\mathcal{E}$ and $\mathcal{F}$ be [[nlab:toposes]]. A **_[[nlab:geometric morphism]]_{: style="font-style: normal"}** $f\colon \mathcal{E}\to \mathcal{F}$ is an [[nlab:adjunction]]
$$
\mathcal{E} \underoverset{f_{*}}{f^{*}}{\underoverset{\rightarrow }{\leftarrow }{\quad \scriptsize \scriptsize \bot \quad }} \mathcal{F}
$$
in which the [[nlab:left adjoint]] $f^{*}$ preserves [[nlab:finite limits]]. (People often say '[[nlab:left exact]] [[nlab:left adjoint]]'.) The [[nlab:right adjoint]] $f_{*}$ is called the **_[[nlab:direct image]]_{: style="font-style: normal"}** part of $f$, and $f^{*}$ is the **_[[nlab:inverse image]]_{: style="font-style: normal"}** part.
=--

I will write $\mathbf{Topos}$ for the [[nlab:category]] of [[nlab:toposes]] and [[nlab:geometric morphisms]]. (Really it's a [[nlab:2-category]], in an obvious way.) By construction, we have a [[nlab:functor]]
$$
\mathbf{Sh}\colon \mathbf{TopSp}\to \mathbf{Topos}
$$
which is (2-categorically) [[nlab:full]] and [[nlab:faithful]], modulo the usual small lie.


+-- {: .num_defn #defnk .thdefn }
###### Examples ######
&nbsp;

1. <p></p>
   +-- {: .num_enume #enumiEa }
   =--
   Every [[nlab:functor]] $f\colon \mathbb{C} \to \mathbb{D}$ induces a string of [[nlab:adjoint functors]]
   $$
   \widehat{\mathbb{C}} \, \underoverset{\underoverset{f_{*}}{\perp }{\rightarrow }}{ \underoverset{\perp }{f_{!}}{\rightarrow }}{ \longleftarrow {\scriptsize f^{*}} - } \, \widehat{\mathbb{D}}
   $$
   between [[nlab:presheaf categories]]. Here $f^{*} = -\circ f$, and $f_{!}$ and $f_{*}$ are left and [[nlab:right Kan extension]] along $f$, respectively. Since $f^{*}$ has a [[nlab:left adjoint]], it [[nlab:preserves limits]]. Hence $(f^{*}, f_{*})$ is a [[nlab:geometric morphism]] $\widehat{\mathbb{C}} \to \widehat{\mathbb{D}}$.

1. <p></p>
   +-- {: .num_enume #enumiEb }
   =--
   It turns out that, for any [[nlab:topological space]] $X$, the inclusion $\mathbf{Sh}(X) \hookrightarrow \mathbf{Psh}(X)$ has a [[nlab:finite limit|finite-limit]]-preserving [[nlab:left adjoint]]. It is called **_[[nlab:sheafification]]_{: style="font-style: normal"}** or the **_associated [[nlab:sheaf]]_{: style="font-style: normal"}** [[nlab:functor]]. So the inclusion of [[nlab:sheaves]] into [[nlab:presheaves]] is a [[nlab:geometric morphism]].

   Since $\mathbf{Sh}(X)$ is a *[[nlab:full]]* [[nlab:subcategory]], the inclusion is [[nlab:full]] and [[nlab:faithful]]; and for totally general reasons, this is [[nlab:equivalent]] to the [[nlab:counit of the adjunction]] being an [[nlab:isomorphism]]. In other words, sheafifying a [[nlab:sheaf]] does not change it.
=--

### Points ###

Let us generalize another concept of [[nlab:topology]]. The points of a [[nlab:topological space]] $X$ correspond to the maps $1 \to X$ (where $1$ is the one-[[nlab:point]] [[nlab:space]]), which correspond to the [[nlab:geometric morphisms]] $\mathbf{Sh}(1) \to \mathbf{Sh}(X)$. But $\mathbf{Sh}(1) = \mathbf{Psh}(1) = \mathbf{Set}$, so we make the following definition.

+-- {: .num_defn #defnl .thdefn }
###### Definition ######
A **_[[nlab:point]]_{: style="font-style: normal"}** of a [[nlab:topos]] $\mathcal{E}$ is a [[nlab:geometric morphism]] $\mathbf{Set}\to \mathcal{E}$.
=--

### Embeddings and Grothendieck toposes ###

For any [[nlab:subspace]] $Y$ of a [[nlab:space]] $X$, the inclusion $Y \hookrightarrow X$ is an **_[[nlab:embedding]]_{: style="font-style: normal"}**, that is, a [[nlab:homeomorphism]] to its [[nlab:image]]. It can be shown that a map $f\colon Y \to X$ of [[nlab:spaces]] is an [[nlab:embedding]] if and only if the [[nlab:direct image]] part $f_{*}$ of the corresponding [[nlab:geometric morphism]] $f\colon \mathbf{Sh}(Y) \to \mathbf{Sh}(X)$ is [[nlab:full]] and [[nlab:faithful]]. So, as usual, we generalize:

+-- {: .num_defn #defnm .thdefn }
###### Definition ######
A [[nlab:geometric morphism]] $f\colon \mathcal{F}\to \mathcal{E}$ is an **_[[nlab:embedding]]_{: style="font-style: normal"}** (or **_inclusion_{: style="font-style: normal"}**) if the [[nlab:direct image functor]] $f_{*}$ is [[nlab:full]] and [[nlab:faithful]].
=--

We then say that $\mathcal{F}$ is a **_[[nlab:subtopos]]_{: style="font-style: normal"}** of $\mathcal{E}$. At least, this is the right thing to say up to [[nlab:equivalence]]. Perhaps we should reserve that word for when $\mathcal{F}$ is actually a ([[nlab:full]]) [[nlab:subcategory]] of $\mathcal{E}$ and $f_{*}$ is the inclusion $\mathcal{F}\hookrightarrow \mathcal{E}$, rather than allowing $f_{*}$ to be any old [[nlab:full and faithful functor]]. But a [[nlab:full and faithful functor]] induces an [[nlab:equivalence]] to its [[nlab:image]], so it makes no real difference.

Probably the easiest [[nlab:toposes]] are the **_[[nlab:presheaf toposes]]_{: style="font-style: normal"}**: those [[nlab:equivalent]] to $\widehat{\mathbb{C}} = \mathbf{Set}^{\mathbb{C}^{\mathrm{op}}}$ for some [[nlab:small category]] $\mathbb{C}$. So maybe subtoposes of [[nlab:presheaf toposes]] are relatively easy too. They have a special name:

+-- {: .num_defn #defnn .thdefn }
###### Definition ######
A [[nlab:topos]] is **_[[nlab:Grothendieck]]_{: style="font-style: normal"}** if it is ([[nlab:equivalent]] to) a [[nlab:subtopos]] of some [[nlab:presheaf topos]].
=--

For instance, we saw in Example&nbsp;[11](#defnk)([2](#enumiEb)) that $\mathbf{Sh}(X)$ is a [[nlab:subtopos]] of $\mathbf{Psh}(X) = \widehat{\mathbf{Open}(X)}$, for any [[nlab:topological space]] $X$. Hence $\mathbf{Sh}(X)$ is a [[nlab:Grothendieck topos]].

Being [[nlab:Grothendieck]] is generally thought of as a mild condition on a [[nlab:topos]]. A [[nlab:Grothendieck topos]] has all small [[nlab:limits]], which immediately disqualifies [[nlab:toposes]] such as $\mathbf{FinSet}$, $\mathbf{FinSet}^{\mathbb{C}^{\mathrm{op}}}$, etc. But other than [[nlab:toposes]] arising from [[nlab:finite sets]] (or [[nlab:sets]] subject to some other [[nlab:cardinality]] bound), most of the [[nlab:toposes]] that people have worked with are [[nlab:Grothendieck]]. A notable exception is the [[nlab:effective topos]], the maps in which can be thought of as computable [[nlab:functions]]. Other non-[[nlab:Grothendieck toposes]] occur in the [[nlab:topos]]-theoretic approach to non-standard [[nlab:analysis]].

There is a theorem of Giraud giving a list of conditions on a [[nlab:category]] [[nlab:equivalent]] to it being a [[nlab:Grothendieck topos]]. It includes non-elementary [[nlab:axioms]] such as 'there is a small [[nlab:generating set]]'. ('Non-elementary' means that it refers to a pre-existing notion of [[nlab:set]].) The [[nlab:Grothendieck toposes]] are sometimes regarded as the nice [[nlab:toposes]], but perhaps the definition of [[nlab:Grothendieck topos]] is not as nice as the definition of [[nlab:elementary topos]].

Definition&nbsp;[14](#defnn) is not the definition of [[nlab:Grothendieck topos]] that you will find in most books. I will now give a brief indication of what the standard definition is and why it is equivalent to the one above.

Fix a [[nlab:small category]] $\mathbb{C}$. There is a one-to-one correspondence between the subtoposes of $\widehat{\mathbb{C}}$ and the **_[[nlab:Grothendieck topologies]]_{: style="font-style: normal"}** on $\mathbb{C}$. A [[nlab:Grothendieck topology]] is a kind of explicit, [[nlab:combinatorial]] structure; it specifies which diagrams

+-- {: style="text-align: center" }

<svg width="125" height="252" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="74344">
<g>
<title>Layer 1</title>
<foreignObject height="20" width="25" font-size="16" id="svg_74344_1" y="60" x="0">
<math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
<semantics>
<mrow>
<msub>
<mi>c</mi>
<mi>i</mi>
</msub>
</mrow>
<annotation encoding="application/x-tex">c_i</annotation>
</semantics>
</math>
</foreignObject>
<foreignObject height="24.666666" width="25" font-size="16" id="svg_74344_2" y="159.999998" x="0">
<math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
<semantics>
<mrow>
<msub>
<mi>c</mi>
<mi>j</mi>
</msub>
</mrow>
<annotation encoding="application/x-tex">c_j</annotation>
</semantics>
</math>
</foreignObject>
<foreignObject height="20" width="25" font-size="16" id="svg_74344_3" y="110" x="100">
<math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
<semantics>
<mrow>
<mi>c</mi>
</mrow>
<annotation encoding="application/x-tex">c</annotation>
</semantics>
</math>
</foreignObject>
<foreignObject height="20" width="20" font-size="16" id="svg_74344_4" y="110" x="0">
<math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
<semantics>
<mrow>
<mi>&#8942;</mi>
</mrow>
<annotation encoding="application/x-tex">\vdots </annotation>
</semantics>
</math>
</foreignObject>
<foreignObject id="svg_74344_5" height="20" width="20" font-size="16" y="10" x="0">
<math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
<semantics>
<mrow>
<mi>&#8942;</mi>
</mrow>
<annotation encoding="application/x-tex">\vdots </annotation>
</semantics>
</math>
</foreignObject>
<foreignObject id="svg_74344_11" height="20" width="20" font-size="16" y="210" x="0">
<math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
<semantics>
<mrow>
<mi>&#8942;</mi>
</mrow>
<annotation encoding="application/x-tex">\vdots </annotation>
</semantics>
</math>
</foreignObject>
<g id="svg_74344_21">
<line id="svg_74344_17" y2="120" x2="100" y1="80" x1="25" stroke-width="2" stroke="#000000" fill="none"/>
<path transform="rotate(27, 92.833, 116.335)" id="svg_74344_18" d="m85.333328,106.333328c4.000015,4.333328 8.666733,8 15,10c-5.999985,2.333344 -10.333328,5.333313 -15,10" stroke-width="2" stroke="#000000" fill="none"/>
<line id="svg_74344_19" y2="105" x2="105" y1="0" x1="20" stroke-width="2" stroke="#000000" fill="none"/>
<path id="svg_74344_20" transform="rotate(49.6164, 100.833, 99.667)" d="m93.333328,89.666672c4.000015,4.333328 8.666733,8 15,10c-5.999985,2.333344 -10.333328,5.333313 -15,10" stroke-width="2" stroke="#000000" fill="none"/>
</g>
<g transform="rotate(180, 63.0137, 191.252)" id="svg_74344_27">
<line id="svg_74344_28" y2="250.331747" x2="25.735653" y1="210.331747" x1="100.984138" stroke-width="2" stroke="#000000" fill="none"/>
<path id="svg_74344_29" d="m35.075073,234.350403c-1.60202,5.677002 -4.103745,11.062683 -8.854408,15.71991c6.426552,-0.644897 11.666832,0.060791 17.964302,2.10022" stroke-width="2" stroke="#000000" fill="none"/>
<line id="svg_74344_30" y2="235.331747" x2="20.719087" y1="130.331747" x1="106.000704" stroke-width="2" stroke="#000000" fill="none"/>
<path id="svg_74344_31" d="m22.132309,217.806854c0.711533,5.854462 0.480171,11.784882 -2.108261,17.904877c5.683556,-3.058563 10.793121,-4.415649 17.393204,-4.946838" stroke-width="2" stroke="#000000" fill="none"/>
</g>
</g>
</svg>
=--

in $\mathbb{C}$ are to be thought of as '[[nlab:covering families]]' and which are not. (There are [[nlab:axioms]].) The motivating example is that given a [[nlab:topological space]] $X$, there is a canonical [[nlab:Grothendieck topology]] on $\mathbf{Open}(X)$: a [[nlab:family]] $(U_{i} \hookrightarrow U)_{i \in I}$ of [[nlab:subsets]] of $U \in \mathbf{Open}(X)$ is [[nlab:covering]] if and only if $U = \bigcup _{i \in I} U_{i}$.

The [[nlab:bijection]]
$$
\{ \text{Grothendieck topologies on}\; \mathbb{C} \} \cong \{ \text{[[nlab:subtoposes]] of}\; \widehat{\mathbb{C}} \}
$$
is written
$$
J \leftrightarrow \mathbf{Sh}(\mathbb{C}, J).
$$
A pair $(\mathbb{C}, J)$, consisting of a [[nlab:small category]] $\mathbb{C}$ equipped with a [[nlab:Grothendieck topology]] $J$, is called a **_[[nlab:site]]_{: style="font-style: normal"}**, and $\mathbf{Sh}(\mathbb{C}, J)$ is the [[nlab:category]] of **_[[nlab:sheaves]]_{: style="font-style: normal"}** on that [[nlab:site]]. For example, let $X$ be a [[nlab:topological space]], take $\mathbb{C} = \mathbf{Open}(X)$, and take $J$ to be the [[nlab:Grothendieck topology]] mentioned above; then $\mathbf{Sh}(\mathbb{C}, J) = \mathbf{Sh}(X)$. Most books proceed as follows: define [[nlab:Grothendieck topology]], define [[nlab:site]], define the [[nlab:category of sheaves]] on a [[nlab:site]], then define a [[nlab:Grothendieck topos]] to be a [[nlab:category]] [[nlab:equivalent]] to the [[nlab:category of sheaves]] on some [[nlab:site]].

I do not know a short way to explain why the [[nlab:subtoposes]] of $\widehat{\mathbb{C}}$ correspond to the [[nlab:Grothendieck topologies]] on $\mathbb{C}$. The following two paragraphs may make it seem easier, or harder.

First, there is an explicit classification of the [[nlab:subtoposes]] of *any* [[nlab:topos]] $\mathcal{E}$. Indeed, it can be shown that the [[nlab:subtoposes]] of $\mathcal{E}$ correspond to the maps $j\colon \Omega \to \Omega $ satisfying certain equations. (Such a $j$ is called a **_[[nlab:Lawvere--Tierney topology]]_{: style="font-style: normal"}** on $\mathcal{E}$, although this is so distant from the original usage of the word '[[nlab:topology]]' that some people [[nlab:object]]; [[nlab:Peter Johnstone]], for instance, uses **_local [[nlab:operator]]_{: style="font-style: normal"}** instead.) By definition of [[nlab:subobject classifier]], it is [[nlab:equivalent]] to say that a [[nlab:subtopos]] of $\mathcal{E}$ amounts to a [[nlab:subobject]] of $\Omega $ satisfying certain [[nlab:axioms]].

Second, take $\mathcal{E}= \widehat{\mathbb{C}}$. We know (Example&nbsp;[6](#defnf)([4](#enumiAd))) that $\Omega \in \widehat{\mathbb{C}}$ is given by $\Omega (c) = \{ \text{sieves on}\; c \} $. Hence a [[nlab:subtopos]] of $\widehat{\mathbb{C}}$ corresponds to a [[nlab:collection]] of [[nlab:sieves]] in $\mathbb{C}$, satisfying certain [[nlab:axioms]]. Calling these the '[[nlab:covering]] [[nlab:sieves]]' gives the notion of [[nlab:Grothendieck topology]].

### Locales ###

Here I will explain the 'small lie' mentioned several times above, and make amends. I will also explain why [[nlab:topos]] theorists are fond of jokes about pointless [[nlab:topology]].

The definition of [[nlab:sheaf]] on a [[nlab:topological space]] $X$ does not mention the points of $X$. It mentions only the [[nlab:open sets]] and inclusions between them, and uses the fact that it is possible to take arbitrary [[nlab:unions]] and [[nlab:finite]] [[nlab:intersections]] of [[nlab:open sets]]. Having observed this, you can see why the [[nlab:space]] $X$ cannot *always* be recovered from the [[nlab:topos]] $\mathbf{Sh}(X)$. For instance, if $X$ is indiscrete (has no [[nlab:open sets]] except $\emptyset $ and $X$) and [[nlab:nonempty]], then $\mathbf{Sh}(X)$ is the same no matter how many points $X$ has.

The idea now is to split the process $X \mapsto \mathbf{Sh}(X)$ into two steps. First, we forget the points of $X$, leaving just the [[nlab:set]] of [[nlab:open sets]], ordered by inclusion. Then, we form the [[nlab:category]] of '[[nlab:sheaves]]' on that ordered [[nlab:set]] (defined as for [[nlab:topological spaces]], almost verbatim).

+-- {: .num_defn #defno .thdefn }
###### Definition ######
A **_[[nlab:frame]]_{: style="font-style: normal"}** is a [[nlab:partially ordered set]] such that every [[nlab:subset]] has a [[nlab:join]] ($=$ least upper bound $=$ [[nlab:sup]]), every [[nlab:finite]] [[nlab:subset]] has a [[nlab:meet]] ($=$ greatest lower bound $=$ [[nlab:inf]]), and [[nlab:finite]] [[nlab:meets]] distribute over [[nlab:joins]]. A **_map of [[nlab:frames]]_{: style="font-style: normal"}** is a map preserving [[nlab:order]], [[nlab:joins]] and [[nlab:finite]] [[nlab:meets]].
=--

A [[nlab:topological space]] $X$ has a [[nlab:frame]] $\mathbf{Open}(X)$ of [[nlab:open subsets]], and a [[nlab:continuous map]] $f\colon X \to Y$ induces a map $f^{-1}\colon \mathbf{Open}(Y) \to \mathbf{Open}(X)$ of [[nlab:frames]]. This gives a [[nlab:functor]]
$$
\mathbf{Open}\colon \mathbf{TopSp}\to \mathbf{Frame}^{\mathrm{op}}.
$$
We now perform a linguistic manoeuvre. $\mathbf{Frame}^{\mathrm{op}}$ is the desired [[nlab:category]] of 'pointless [[nlab:spaces]]'. But we cannot wholeheartedly say that a [[nlab:frame]] is a pointless [[nlab:space]], because the *maps* of [[nlab:frames]] are the wrong way round. So we introduce a new word---**_[[nlab:locale]]_{: style="font-style: normal"}**---and define the [[nlab:category]] $\mathbf{Loc}$ of [[nlab:locales]] by $\mathbf{Loc}= \mathbf{Frame}^{\mathrm{op}}$. We can wholeheartedly say that a *[[nlab:locale]]* is a pointless [[nlab:space]].

There is a [[nlab:functor]] $\mathbf{Sh}\colon \mathbf{Loc}\to \mathbf{Topos}$, defined just as for [[nlab:topological spaces]] except that [[nlab:unions]] become [[nlab:joins]] and [[nlab:intersections]] become [[nlab:meets]]. The [[nlab:functor]] $\mathbf{Sh}\colon \mathbf{TopSp}\to \mathbf{Topos}$ factorizes as
$$
\mathbf{TopSp}\stackrel{\mathbf{Open}}{\to } \mathbf{Loc}\stackrel{\mathbf{Sh}}{\to } \mathbf{Topos}.
$$
This is the two-step process mentioned above.

Whenever I have said 'modulo a small lie', you can interpret that as 'use [[nlab:locales]] instead of [[nlab:topological spaces]]'. For example, $\mathbf{Sh}\colon \mathbf{Loc}\to \mathbf{Topos}$ really is [[nlab:full]] and [[nlab:faithful]], in a suitably up-to-[[nlab:isomorphism]] sense: [[nlab:locale]] maps $X \to Y$ correspond one-to-one with [[nlab:isomorphism]] classes of [[nlab:geometric morphisms]] $\mathbf{Sh}(X) \to \mathbf{Sh}(Y)$. This means that $\mathbf{Loc}$ is [[nlab:equivalent]] to a [[nlab:full subcategory]] of $\mathbf{Topos}$. (Actually it is an [[nlab:equivalence of 2-categories]], but I will gloss over that point.)

Every [[nlab:locale]] gives rise to a [[nlab:topos]]---but the converse is also true. Given a [[nlab:topos]] $\mathcal{E}$, the [[nlab:subobjects]] of $1$ form a [[nlab:poset]] $\mathrm{Sub}_{\mathcal{E}}(1)$. Assuming that $\mathcal{E}$ has enough [[nlab:colimits]], $\mathrm{Sub}_{\mathcal{E}}(1)$ is a [[nlab:frame]]. This process defines a [[nlab:functor]]
$$
\begin{array}{ccc} \mathbf{Topos}&\to &\mathbf{Loc}\\ \mathcal{E}&\mapsto &\mathrm{Sub}_{\mathcal{E}}(1). \end{array}
$$
I am now quietly changing $\mathbf{Topos}$ to mean the [[nlab:toposes]] with small [[nlab:colimits]]; this includes all [[nlab:Grothendieck toposes]].

You might think that $1$ could have no interesting [[nlab:subobjects]], since that is the case in the most obvious [[nlab:topos]], $\mathbf{Set}$. But there are [[nlab:toposes]] that are nearly as obvious in which $\mathrm{Sub}_{\mathcal{E}}(1)$ is not trivial. For instance, take $\mathcal{E}= \mathbf{Set}^{I}$ for any [[nlab:set]] $I$: then $\mathrm{Sub}_{\mathcal{E}}(1)$ is the [[nlab:power set]] of $I$.

Now a wonderful thing is true. The [[nlab:functor]] just defined is [[nlab:left adjoint]] to the inclusion $\mathbf{Sh}\colon \mathbf{Loc}\hookrightarrow \mathbf{Topos}$. This means that $\mathbf{Loc}$ is ([[nlab:equivalent]] to) a *reflective* [[nlab:reflective subcategory|subcategory]] of $\mathbf{Topos}$. Hence the [[nlab:counit]] is an [[nlab:isomorphism]]:
$$
X \cong \mathrm{Sub}_{\mathbf{Sh}(X)}(1)
$$
for any [[nlab:locale]] $X$. This is how you recover a [[nlab:locale]] from its [[nlab:topos of sheaves]].

So $\mathbf{Loc}$ sits inside $\mathbf{Topos}$ as a [[nlab:subcategory]] of the best kind: [[nlab:full]] and [[nlab:reflective subcategory|reflective]], like [[nlab:abelian groups]] in [[nlab:groups]]. It is reasonable to say that a [[nlab:locale]] is a special sort of [[nlab:topos]]. More formally, a [[nlab:topos]] is **_localic_{: style="font-style: normal"}** if it is of the form $\mathbf{Sh}(X)$ for some [[nlab:locale]] $X$. Localic [[nlab:toposes]] are easy to work with; if you were having trouble proving something for arbitrary [[nlab:toposes]], you might start by trying to prove it in this special case.

Since every [[nlab:locale]] is of the form $\mathrm{Sub}_{\mathcal{E}}(1)$ for some [[nlab:topos]] $\mathcal{E}$, [[nlab:locale]] theory can be regarded as the fragment of [[nlab:topos theory]] concerning [[nlab:subobjects]] of $1$. A [[nlab:subobject]] of $1$ is a map $1 \to \Omega $, which can reasonably called a [[nlab:truth value]]. In that sense, [[nlab:locale]] theory is the study of [[nlab:truth values]].

The notion of [[nlab:locale]] can also be seen as a [[nlab:decategorification]] of the notion of [[nlab:Grothendieck topos]]. A [[nlab:poset]] $P$ is a [[nlab:category enriched]] in the two-[[nlab:element]] [[nlab:totally ordered set]] $2$. There is a [[nlab:Yoneda embedding]] $P \to 2^{P^{\mathrm{op}}}$, which has a [[nlab:finite]]-[[nlab:meet]]-preserving [[nlab:left adjoint]] if and only if $P$ is a [[nlab:frame]]. Analogously, it is almost true that for a [[nlab:category]] $\mathcal{E}$, the [[nlab:Yoneda embedding]] $\mathcal{E}\to \mathbf{Set}^{\mathcal{E}^{\mathrm{op}}}$ has a [[nlab:finite]]-[[nlab:limit]]-preserving [[nlab:left adjoint]] if and only if $\mathcal{E}$ is a [[nlab:Grothendieck topos]]. (This result is due to [Street](#citeStrNT) ([1981](#citeStrNT)). 'Almost' refers to a [[nlab:set]]-theoretic size condition.) A map of [[nlab:frames]] is a [[nlab:function]] preserving [[nlab:joins]] and [[nlab:finite]] [[nlab:meets]], and the [[nlab:inverse image]] part of a [[nlab:geometric morphism]] is a [[nlab:functor]] preserving [[nlab:colimits]] and [[nlab:finite limits]]. Thus, [[nlab:locales]] play roughly the same role among 2-[[nlab:enriched categories]] as [[nlab:Grothendieck toposes]] play among $\mathbf{Set}$-[[nlab:enriched categories]].

How much has been lost by passing from [[nlab:topological spaces]] to [[nlab:locales]]? In most people's view, not much. For example, we observed that all [[nlab:nonempty]] [[nlab:indiscrete spaces]] give rise to the same [[nlab:locale]]; but many mathematicians regard [[nlab:indiscrete spaces]] with $\geq 2$ points as '[[nlab:nice topological space|pathological]]' and would be positively happy to see them go.

In fact, some things are gained. For example, a [[nlab:subgroup]] of a [[nlab:topological group]] need not be closed, and non-closed subgroups are often regarded as pathological (since the corresponding [[nlab:quotients]] are non-[[nlab:Hausdorff]]). But it is a theorem that every [[nlab:subgroup]] of a *localic* [[nlab:group]] is closed. See for instance Section&nbsp;C5.3 of [Johnstone](#citeJohSE) ([2003](#citeJohSE)).

The [[nlab:functor]] $\mathbf{Open}\colon \mathbf{TopSp}\to \mathbf{Loc}$ has a [[nlab:right adjoint]], which I will not describe. As mentioned [above](#padjneqv), every [[nlab:adjunction]] restricts canonically to an [[nlab:equivalence]] between [[nlab:full subcategories]]. In this case, this gives an [[nlab:equivalence]] between:

* a [[nlab:full subcategory]] of $\mathbf{TopSp}$, whose [[nlab:objects]] are called the **_[[nlab:sober]]_{: style="font-style: normal"}** [[nlab:spaces]]

* a [[nlab:full subcategory]] of $\mathbf{Loc}$, whose [[nlab:objects]] are called the **_[[nlab:topological locale|spatial]]_{: style="font-style: normal"}** [[nlab:locales]].

Another way of interpreting the phrase 'modulo a small lie' is 'true for [[nlab:sober spaces]]'. Sobriety amounts to a rather mild separation condition. For example, every [[nlab:Hausdorff space]] is [[nlab:sober]]. So in passing from a [[nlab:Hausdorff space]] to a [[nlab:locale]], or to a [[nlab:topos]], nothing whatsoever is lost.

There is a kind of attitudinal paradox here. Many algebraic topologists think *only* about [[nlab:Hausdorff spaces]], and regard non-[[nlab:Hausdorff spaces]] as pathological. But these are often the same people who feel strongly that [[nlab:topological spaces]] are not really about [[nlab:open sets]]; they think in terms of points and paths and [[nlab:homotopies]]. So it is perhaps paradoxical that the Hausdorff condition guarantees that a [[nlab:space]] can be understood in terms of its [[nlab:open sets]] alone: the [[nlab:topos of sheaves]] depends on nothing else, and contains all the information about the original [[nlab:space]].

+-- {: .num_section #sectiond }
=--
## Toposes and universal algebra ## {: .num_section}

The point of this section is to explain what people mean when they talk about the [[nlab:classifying topos]] of a [[nlab:theory]]. Another way to look at it is this: I will explain how [[nlab:toposes]] can be viewed as cousins of [[nlab:operads]] and [[nlab:Lawvere theories]].

In classical [[nlab:universal algebra]], an [[nlab:algebraic theory]] (or strictly, a presentation of an [[nlab:algebraic theory]]) consists of a bunch of operation symbols of specified [[nlab:signature (in logic)|arities]], together with a bunch of equations. To take the standard example, the (usual presentation of the) [[nlab:theory]] of [[nlab:groups]] consists of

* an operation symbol $1$ of [[nlab:signature (in logic)|arity]] $0$

* an operation symbol $(\:\:)^{-1}$ of [[nlab:signature (in logic)|arity]] $1$

* an operation symbol $\cdot $ of [[nlab:signature (in logic)|arity]] $2$

together with the usual equations. You can speak of '[[nlab:models]]' of an [[nlab:algebraic theory]] in any [[nlab:category]] $\mathcal{E}$ with [[nlab:finite]] [[nlab:products]]. In our example, they are the [[nlab:internal groups]] in $\mathcal{E}$.

But there are other ways of looking at such [[nlab:theories]].

Consider the [[nlab:free object|free]] [[nlab:finite]] [[nlab:product category]] $\mathcal{T}$ equipped with an [[nlab:internal group]]. (There are general reasons why such a thing must exist.) Its [[nlab:universal property]] is that for any [[nlab:finite]] [[nlab:product category]] $\mathcal{E}$, the [[nlab:finite]]-[[nlab:product]]-preserving [[nlab:functors]] $\mathcal{T}\to \mathcal{E}$ correspond to the [[nlab:internal groups]] in $\mathcal{E}$.

Concretely, $\mathcal{T}$ looks something like this. It must contain an [[nlab:object]] $X$, the underlying [[nlab:object]] of the [[nlab:internal group]]. Since $\mathcal{T}$ has [[nlab:finite]] [[nlab:products]], it must also contain an [[nlab:object]] $X^{n}$ for each $n \in \mathbb{N}$. There is no reason for it to have any other [[nlab:objects]], and since it is [[nlab:free object|free]], it does not. A map $X^{n} \to X^{m}$ is (by definition of [[nlab:product]]) an $m$-tuple of maps $X^{n} \to X$; and the maps $X^{n} \to X$ are (by [[nlab:free object|freeness]]) whatever maps $G^{n} \to G$ must exist for *any* [[nlab:internal group]] $G$ in *any* [[nlab:finite]] [[nlab:product category]]. That is, they are the $n$-ary operations in the [[nlab:theory]] of [[nlab:groups]]: the words in $n$ letters.

This [[nlab:category]] $\mathcal{T}$ is called the **_[[nlab:Lawvere theory]] of [[nlab:groups]]_{: style="font-style: normal"}**. The same goes for [[nlab:rings]], [[nlab:lattices]], etc. In all these cases, $\mathcal{T}$ is a [[nlab:product category|finite product category]] with the further [[nlab:property]] that the [[nlab:objects]] are in [[nlab:bijection]] with the [[nlab:natural numbers]], the [[nlab:product]] of [[nlab:objects]] corresponding to addition of numbers. This further [[nlab:property]] holds because the [[nlab:theories]] described so far have been single-sorted: a [[nlab:model]] is a *single* [[nlab:object]] equipped with some [[nlab:structure]].

But there are also many-sorted [[nlab:theories]], such as the two-sorted [[nlab:theory]] of pairs $(R, M)$ in which $R$ is a [[nlab:ring]] and $M$ an $R$-[[nlab:module]]. So we can widen the notion of [[nlab:algebraic theory]] to include all (small) [[nlab:finite product]] [[nlab:categories]]. Some people say that an [[nlab:algebraic theory]] *is* just a [[nlab:product category|finite product category]]. Others say that [[nlab:algebraic theories]] *correspond* to [[nlab:finite product]] [[nlab:categories]]. Others still, more traditionally, say that [[nlab:algebraic theories]] correspond to only *certain* [[nlab:product category|finite product categories]].

Terminology aside, we can play the same game for other classes of [[nlab:limit]]. For example, it makes no sense to talk about [[nlab:internal categories]] in an arbitrary [[nlab:product category|finite product category]], because the definition of [[nlab:internal category]] needs [[nlab:pullbacks]]. (Composition in an [[nlab:internal category]] $\mathbb{C}$ is a map $\mathbb{C}_{1} \times _{\mathbb{C}_{0}} \mathbb{C}_{1} \to \mathbb{C}_{1}$.) But we can talk about [[nlab:internal categories]] in a finite *[[nlab:limit]]* [[nlab:category]]; and as before, there is a free [[nlab:finite limit]] [[nlab:category]] $\mathcal{T}$ equipped with an [[nlab:internal category]]. This means that for any [[nlab:finite limit]] [[nlab:category]] $\mathcal{E}$, the finite-[[nlab:limit]]-preserving [[nlab:functors]] $\mathcal{T}\to \mathcal{E}$ correspond to the [[nlab:internal categories]] in $\mathcal{E}$. A small [[nlab:finite limit]] [[nlab:category]] is called (or corresponds to) an **_[[nlab:essentially algebraic theory]]_{: style="font-style: normal"}**.

In a [[nlab:category]] with [[nlab:finite]] [[nlab:products]] you can talk about [[nlab:internal groups]] but not, in general, [[nlab:internal categories]]. In a [[nlab:category]] with [[nlab:finite limits]] you can talk about both. By extending the list of [[nlab:properties]] that the [[nlab:category]] is assumed to satisfy, you can accommodate more and more sophisticated kinds of [[nlab:theory]]. (The [[nlab:theory]] of [[nlab:internal categories]] is more 'sophisticated' than that of [[nlab:groups]] in the sense that [[nlab:composition]] is only defined for *some* pairs of maps, whereas classical [[nlab:universal algebra]] can only handle operations defined on *all* pairs.) The properties need not be of the form '[[nlab:limits]] of such-and-such a type exist'. For example, it is sometimes useful to assume [[nlab:factorization system|epi-mono factorization]], as we shall see.

There is a trade-off here. As you allow more sophisticated language, you widen the [[nlab:class]] of [[nlab:theories]] that can be expressed, but you narrow the [[nlab:class]] of [[nlab:categories]] in which it makes sense to take [[nlab:models]]. (You also make more work for yourself.) In the same way, if you trade in your motorbike for a double-decker bus, you increase the number of passengers you can carry, but you restrict where you can carry them: no low bridges or tight alleyways. (You also increase your fuel costs.) It is sensible, then, to use the smallest class of [[nlab:theories]] containing the ones you are interested in. For example, you *could* treat [[nlab:groups]] as an [[nlab:essentially algebraic theory]], but that would mean you could only take [[nlab:models]] in [[nlab:categories]] with *all* [[nlab:finite limits]], when in fact just [[nlab:products]] would do.

Before I get onto [[nlab:toposes]], I want to point out a slightly different direction that you can take things in. Rather than just altering the *[[nlab:properties]]* that the [[nlab:categories]] are assumed to have, you can also alter the *[[nlab:structure]]* with which they are equipped.

Take [[nlab:monoidal categories]], for instance. We can speak of [[nlab:internal monoids]] in any [[nlab:monoidal category]]. Hence, the [[nlab:theory]] of [[nlab:monoids]] can be regarded as the free [[nlab:monoidal category]] containing an [[nlab:internal monoid]]. (This is in fact the [[nlab:category]] of [[nlab:finite]] [[nlab:ordinals]].) Similarly, it makes sense to speak of [[nlab:algebras for an operad]] $P$ in any [[nlab:monoidal category]], and we can associate to $P$ the free [[nlab:monoidal category]] $\mathcal{T}$ containing a $P$-[[nlab:algebra]]. Thus, for any [[nlab:monoidal category]] $\mathcal{E}$, [[nlab:monoidal functors]] $\mathcal{T}\to \mathcal{E}$ correspond to $P$-[[nlab:algebras]] in $\mathcal{E}$.

We might define a **_monoidal [[nlab:theory]]_{: style="font-style: normal"}** to be a small [[nlab:monoidal category]]. This gets us into the territory of [[nlab:PROPs]], where there are nontrivial theorems such as the classification of 2-[[nlab:dimensional]] [[nlab:topological quantum field theories]]: the symmetric monoidal [[nlab:theory]] of (or, '[[nlab:PROP]] for') commutative [[nlab:Frobenius algebras]] is the [[nlab:category]] of smooth 1-[[nlab:manifolds]] and [[nlab:diffeomorphism]] classes of [[nlab:cobordisms]].

All of this is to give an impression of how far-reaching these ideas are. It is a sketch of the context in which [[nlab:classifying toposes]] can be understood.

You will have guessed that the same kind of thing can be said for [[nlab:toposes]] as for [[nlab:categories]] with [[nlab:finite]] [[nlab:products]], [[nlab:finite limits]], etc. Since [[nlab:toposes]] have very rich structure (*much* more than just [[nlab:finite limits]]), they correspond to a very wide class of [[nlab:theories]] indeed.

An example of the kind of [[nlab:theory]] that can be interpreted in a [[nlab:topos]] is the [[nlab:theory]] of [[nlab:fields]]. (This is rather a feeble example, but I want to keep it simple.) A [[nlab:field]] is, of course, a [[nlab:commutative ring]] $R$ satisfying the [[nlab:axioms]]
\begin{equation}
\label{eqfieldnontriv} 0 \neq 1
\end{equation}
and
\begin{equation}
\label{eqfieldmain} \forall x \in R, \quad x = 0 \;\text{or}\; \exists y\colon x y = 1.
\end{equation}
By a mechanical process, this definition can be turned into a definition of 'internal [[nlab:field]] in a [[nlab:topos]]'. As compensation for the imprecision of the rest of this section, I will give the definition in detail; but if you want to skip it, the point to retain is that it *is* a mechanical process.

Let $\mathcal{E}$ be a [[nlab:topos]]. We certainly know how to define '[[nlab:commutative ring]] in $\mathcal{E}$': that makes sense in any [[nlab:category]] with [[nlab:finite]] [[nlab:products]]. Let $R$ be a [[nlab:commutative ring]] in $\mathcal{E}$. The nontriviality [[nlab:axiom]], $0 \neq 1$, is expressed by saying that the [[nlab:equalizer]] of
$$
1 \underoverset{\quad 1 \quad }{0}{\rightrightarrows } R
$$
is the [[nlab:initial object]] $0$. For the other [[nlab:axiom]], let us first define the [[nlab:subobject]] $U \rightarrowtail R$ consisting of the [[nlab:units]] ([[nlab:invertible elements]]). The '[[nlab:set]]' $P = \{ (x, y) \:|\:x y = 1 \} $ is the [[nlab:pullback]]
$$
\begin{matrix} P & \begin{svg} [[!include SVG rightarrow]]\end{svg} & 1 \\ \array{\begin{svg} [[!include SVG downarrowtail]]\end{svg}} \mathrlap{\array{\arrayopts{\align{bottom}}\space{0}{30}{10}\begin{svg} [[!include SVG pullback]]\end{svg}}} && \array{\begin{svg} [[!include SVG downarrowtail]]\end{svg}}\mathrlap{1} \\ R \times R & \begin{svg} [[!include SVG rightarrow]]\end{svg} & R. \end{matrix}
$$
Now we want to define the '[[nlab:set]]' $U$ of [[nlab:units]] as the [[nlab:image]] of the [[nlab:composite]] map
$$
f = \left ( P \rightarrowtail R \times R \stackrel{\mathrm{pr}_{1}}{\to } R \right ).
$$
We can talk about [[nlab:images]] in a [[nlab:topos]], since every map in a [[nlab:topos]] factorizes essentially uniquely as an [[nlab:epi]] followed by a mono. So, define $U \rightarrowtail R$ by the factorization
$$
f = \left ( P \twoheadrightarrow U \rightarrowtail R \right ).
$$
The second [[nlab:field]] [[nlab:axiom]] states that every [[nlab:element]] of $R$ lies in either the [[nlab:subobject]] $1 \stackrel{0}{\rightarrowtail } R$ or the [[nlab:subobject]] $U \rightarrowtail R$. In other words, it states that the map
$$
1 + U \to R
$$
is [[nlab:epi]]. Here we have used the fact that every [[nlab:topos]] has [[nlab:coproducts]], written $+$.

If you have read Section&nbsp;[2](#sectionb), you will recognize that the informal talk of '[[nlab:sets]]' (really, [[nlab:objects]] of $\mathcal{E}$) and the use of [[nlab:set]]-theoretic [[nlab:notation]] $\{ \ldots \:|\:\ldots \} $ are something to do with the [[nlab:internal language]] of a [[nlab:topos]]. This gives a hint of how the process can be mechanized.

(There are actually *several* possible [[nlab:theories]] of [[nlab:fields]], depending on exactly how you write down the [[nlab:axioms]]. They all have the same [[nlab:models]] in $\mathbf{Set}$---namely, [[nlab:fields]]---but they do not have the same [[nlab:models]] in other [[nlab:toposes]]. For example, a genuinely different [[nlab:theory]] is obtained by changing [[nlab:axiom]]&nbsp;\eqref{eqfieldmain} to '$\forall x \in R$, $(\not \!\exists y: x y = 1) \implies x = 0$'. But this does not affect the main point: given a list of formally-expressed [[nlab:axioms]] such as&nbsp;\eqref{eqfieldnontriv} and&nbsp;\eqref{eqfieldmain}, there is an automatic process converting it into a definition that makes sense in an arbitrary [[nlab:topos]].)

You now have the choice between a short story and a long story.

The short story is that what we did for [[nlab:finite product]] and [[nlab:finite limit]] [[nlab:categories]] can also be done for [[nlab:toposes]]. The [[nlab:theories]] corresponding to [[nlab:toposes]] are called the [[nlab:geometric theories]], and the [[nlab:topos]] corresponding to a particular [[nlab:geometric theory]] is called its [[nlab:classifying topos]].

The long story is longer because there are two different notions of map of [[nlab:toposes]]---and you need to decide what a map of [[nlab:toposes]] is in order to state the [[nlab:universal property]] of the [[nlab:topos]] resulting from a [[nlab:theory]].

The more obvious but less used notion of map of [[nlab:toposes]] is a [[nlab:functor]] preserving all the [[nlab:structure]] in sight: [[nlab:finite limits]], [[nlab:exponential object|exponentials]], and the [[nlab:subobject classifier]]. These are called **_[[nlab:logical morphisms]]_{: style="font-style: normal"}**. Now in a [[nlab:topos]], you can interpret a really vast range of [[nlab:theories]]: any '[[nlab:type theory|higher-order theory]]', in fact. (First order means that you can only quantify over *[[nlab:elements]]* of a [[nlab:set]]; in a second order [[nlab:theory]] you can also quantify over *[[nlab:subsets]]* of a [[nlab:set]]; and so on.) Models of any such [[nlab:theory]] get along well with [[nlab:logical morphisms]], because [[nlab:logical morphisms]] preserve everything. So you can tell a similar story for [[nlab:toposes]], [[nlab:logical morphisms]] and [[nlab:type theory|higher order theories]] as for [[nlab:finite product]] [[nlab:categories]], finite-[[nlab:product]]-preserving [[nlab:functors]] and [[nlab:algebraic theories]].

The more popular notion of map of [[nlab:toposes]] is that of [[nlab:geometric morphism]]. (Here it helps to have read Section&nbsp;[3](#sectionc), where the definition is motivated.) A **_[[nlab:geometric morphism]]_{: style="font-style: normal"}** between [[nlab:toposes]] is a [[nlab:functor]] with a [[nlab:finite]]-[[nlab:limit]]-preserving [[nlab:left adjoint]]. The corresponding [[nlab:theories]] are the **_[[nlab:geometric theories]]_{: style="font-style: normal"}**. I will not give the definition, but it is not too bad an approximation to say that they are the same as the first-order [[nlab:theories]]: every [[nlab:geometric theory]] is first-order, and almost every first-order [[nlab:theory]] that one encounters is geometric.

Given a [[nlab:geometric theory]], a **_[[nlab:classifying topos]]_{: style="font-style: normal"}** for the [[nlab:theory]] is a [[nlab:cocomplete category|cocomplete]] [[nlab:topos]] $\mathcal{T}$ with the property that for any [[nlab:cocomplete category|cocomplete]] [[nlab:topos]] $\mathcal{E}$, [[nlab:models]] of the [[nlab:theory]] in $\mathcal{E}$ correspond naturally to [[nlab:geometric morphisms]] $\mathcal{E}\to \mathcal{T}$. Every [[nlab:geometric theory]] has a [[nlab:classifying topos]].

There are two surprises here. One is the appearance of the word '[[nlab:cocomplete category|cocomplete]]', which I will not explain and will not bother inserting below. It is generally thought of as a mild condition (satisfied by any [[nlab:Grothendieck topos]], for instance).

The bigger surprise is the reversal of direction. The previous cases lead us to expect [[nlab:models]] in $\mathcal{E}$ to correspond to maps $\mathcal{T}\to \mathcal{E}$. However, since a [[nlab:geometric morphism]] is a pair of [[nlab:adjoint functors]], the choice of direction is a matter of convention. As the name suggests, the choice that society made was motivated by [[nlab:geometry]]. Perhaps if the motivation had been [[nlab:universal algebra]], it would have been the other way round. (This is an aspect of the thought that [[nlab:geometry]] is dual to [[nlab:algebra]].) A map of [[nlab:toposes]] would then have been a [[nlab:finite]]-[[nlab:limit]]-preserving [[nlab:functor]] with a [[nlab:right adjoint]], which is more or less the same thing as a [[nlab:functor]] preserving [[nlab:finite limits]] and small [[nlab:colimits]].

If a [[nlab:topos]] is thought of as a generalized [[nlab:space]] (as in Section&nbsp;[3](#sectionc)) then the [[nlab:classifying topos]] of a [[nlab:theory]] can be thought of as its [[nlab:space]] of [[nlab:models]]. Indeed, a point of the [[nlab:classifying topos]] $\mathcal{T}$ is (by Definition&nbsp;[12](#defnl)) a [[nlab:geometric morphism]] $\mathbf{Set}\to \mathcal{T}$, which is exactly a [[nlab:model]] of the [[nlab:theory]] in $\mathbf{Set}$. Some familiar [[nlab:topological spaces]] can be construed as [[nlab:classifying toposes]]. For example, there is a '[[nlab:theory]] of [[nlab:Dedekind cuts]]' whose [[nlab:classifying topos]] is $\mathbf{Sh}(\mathbb{R})$, that is, $\mathbb{R}$ regarded as a [[nlab:topos]].

Given how much structure a [[nlab:topos]] contains, it is surprising how many [[nlab:classifying toposes]] can be described simply. I will now describe the [[nlab:classifying topos]] of any [[nlab:algebraic theory]], by the venerable expository device of doing it just for [[nlab:groups]].

We will need the notion of [[nlab:locally finitely presentable category|finite presentability]]. A [[nlab:group]] (in $\mathbf{Set}$) is **_[[nlab:locally finitely presentable category|finitely presentable]]_{: style="font-style: normal"}** if it admits a presentation by a [[nlab:finite set]] of [[nlab:generators]] subject to a [[nlab:finite set]] of [[nlab:relations]]. The [[nlab:category]] of finitely presentable [[nlab:groups]] and all [[nlab:homomorphisms]] between them will be written $\mathbf{Grp}_{\mathrm{fp}}$.

+-- {: style="margin-left: 2em" }
##### Aside #####

[[nlab:locally finitely presentable category|Finite presentability]] is a more categorical concept than it might seem. Writing $T\colon \mathbf{Set}\to \mathbf{Set}$ for the [[nlab:free group]] [[nlab:monad]], a relation (equation) in a [[nlab:set]] $X$ of [[nlab:generators]] is an [[nlab:element]] of $T X \times T X$. So, a [[nlab:family]] $(r_{i})_{i \in I}$ of relations is a map $I \to T X \times T X$, or equivalently a diagram
$$
I \rightrightarrows T X
$$
in $\mathbf{Set}$, or equivalently a diagram
$$
F I \rightrightarrows F X
$$
in $\mathbf{Grp}$, where $F\colon \mathbf{Set}\to \mathbf{Grp}$ is the [[nlab:free group]] [[nlab:functor]]. The [[nlab:group]] presented by these [[nlab:generators]] and relations is the [[nlab:coequalizer]] of this [[nlab:diagram]] in $\mathbf{Grp}$. Hence a [[nlab:group]] is finitely presentable precisely when it is the [[nlab:coequalizer]] of some diagram $F I \rightrightarrows F X$ in which $I$ and $X$ are [[nlab:finite sets]].

This formulation of [[nlab:finite]] presentability in $\mathbf{Grp}$ uses the [[nlab:free group]] [[nlab:functor]] $F$. But in fact, there is a general definition of [[nlab:finite]] presentability of an [[nlab:object]] of any [[nlab:category]]. I will not go into this.
=--

As promised, the [[nlab:classifying topos]] for [[nlab:groups]] is easy to describe:

+-- {: .num_defn #defnp .thplain }
###### Theorem ######
The [[nlab:classifying topos]] for [[nlab:groups]] is $\mathbf{Set}^{\mathbf{Grp}_{\mathrm{fp}}}$.
=--

In other words, for any [[nlab:topos]] $\mathcal{E}$, a [[nlab:group]] in $\mathcal{E}$ is the same thing as a [[nlab:geometric morphism]] $\mathcal{E}\to \mathbf{Set}^{\mathbf{Grp}_{\mathrm{fp}}}$.

The same goes for other [[nlab:algebraic theories]]. This yields something interesting even for very trivial [[nlab:theories]]. Take the [[nlab:theory of objects]], whose [[nlab:models]] in a [[nlab:category]] $\mathcal{E}$ are simply [[nlab:objects]] of $\mathcal{E}$. A finitely presentable [[nlab:set]] is just a [[nlab:finite set]]. Hence for any [[nlab:topos]] $\mathcal{E}$, [[nlab:objects]] of $\mathcal{E}$ correspond to [[nlab:geometric morphisms]] $\mathcal{E}\to \mathbf{Set}^{\mathbf{FinSet}}$. The [[nlab:topos]] $\mathbf{Set}^{\mathbf{FinSet}}$ is therefore called the **_[[nlab:object classifier]]_{: style="font-style: normal"}**.

We have been asking, for a given [[nlab:theory]], 'what [[nlab:topos]] classifies it?' But we can turn the question round and ask, for a given [[nlab:topos]] $\mathcal{T}$, 'what does $\mathcal{T}$ classify?' In other words, what are the [[nlab:geometric morphisms]] from an arbitrary [[nlab:topos]] $\mathcal{E}$ into $\mathcal{T}$? It is a fact that *every* [[nlab:topos]] $\mathcal{T}$ is the [[nlab:classifying topos]] of some [[nlab:geometric theory]]---although given how wide a class of [[nlab:theories]] that is, perhaps this does not say very much.

There are clean answers to this reversed question for many [[nlab:toposes]] $\mathcal{T}$. In particular, this is so when $\mathcal{T}$ is the [[nlab:topos]] $\mathbf{Sh}(\mathbb{C}, J)$ of [[nlab:sheaves]] on a [[nlab:site]] (Section&nbsp;[3](#sectionc)). Here I will just tell you the answer for a smaller class of [[nlab:toposes]].

+-- {: .num_defn #defnq .thplain }
###### Theorem ######
Let $\mathbb{C}$ be a [[nlab:category]] with [[nlab:finite limits]]. Then the [[nlab:presheaf topos]] $\widehat{\mathbb{C}}$ classifies [[nlab:finite limit|finite-limit]]-preserving [[nlab:functors]] out of $\mathbb{C}$.
=--

In other words, for any [[nlab:topos]] $\mathcal{E}$, a [[nlab:geometric morphism]] $\mathcal{E}\to \widehat{\mathbb{C}}$ is the same thing as a [[nlab:finite limit|finite-limit]]-preserving [[nlab:functor]] $\mathbb{C} \to \mathcal{E}$.

(If you know about [[nlab:flat functors]], you can drop the assumption that $\mathbb{C}$ has [[nlab:finite limits]]: for any [[nlab:small category]] $\mathbb{C}$, the [[nlab:presheaf topos]] $\widehat{\mathbb{C}}$ classifies [[nlab:flat functors]] out of $\mathbb{C}$. This is one version of [[nlab:Diaconescu's Theorem]].)

So there is a back-and-forth translation between [[nlab:geometric theories]] and the [[nlab:toposes]] that classify them. In many cases, this translation is surprisingly straightforward.

## References ##

* {: #citeJohSE }Johnstone, P.&nbsp;T., 2003. [[nlab:Sketches of an Elephant]]: A [[nlab:Topos]] Theory Compendium. Oxford Logic Guides. Oxford University Press.

* {: #citeLawETCS }[[nlab:Lawvere]], F.&nbsp;W., 1964. An elementary theory of [[nlab:the category of sets]]. *Proceedings of the National Academy of Sciences of the U.S.A.* **52**:1506--1511. Reprinted as *Reprints in [[nlab:Theory and Applications of Categories]]* 12:1--35, 2005.

* {: #citeLaRo }[[nlab:Lawvere]], F.&nbsp;W. and R.&nbsp;[[nlab:Rosebrugh]], 2003. Sets for Mathematics. Cambridge University Press, Cambridge.

* {: #citeMaMo }Mac&nbsp;Lane, S. and I.&nbsp;Moerdijk, 1994. [[nlab:Sheaves in Geometry and Logic]]. Springer, Berlin.

* {: #citeMcLECS }McLarty, C., 2004. Exploring categorical structuralism. *Philosophia Mathematica* **12**:37--53.

* {: #citePare }Par&#233;, R., 1974. Colimits in [[nlab:topoi]]. *Bulletin of the American Mathematical Society* **80**:556--561.

* {: #citeStrNT }Street, R., 1981. Notions of [[nlab:topos]]. *Bulletin of the Australian Mathematical Society* **23**:199--208.
<a href="http://www.seoweblog.net">Jasa SEO</a>
<a href="http://www.seoweblog.net">Jasa SEO Murah</a>
<a href="http://www.seoweblog.net">SEO Indonesia</a>
<a href="http://www.seoweblog.net">SEO</a>
<a href="http://www.bisnisukm.biz">Bisnis UKM</a>
<a href="http://www.tertinggal.com">Tertinggal</a>
<a href="http://www.bisnismodalkecil.org">Bisnis Modal Kecil</a>
<a href="http://www.cheapes.info">Cheapes</a>
<a href="http://www.hostgator-coupon.co">Hostgator Coupon</a>
<a href="http://www.linkbooking.info">Link Booking</a>
<a href="http://www.televisoriofferte.info">Televisori offerte</a>
<a href="http://www.notebook-offerte.info">Notebook Offerte</a>
<a href="http://www.govr.info">Govr</a>
<a href="http://www.ezido.info">Edo Ziedo</a>
<a href="http://www.portatileapple.info">Portatile Apple</a>
<a href="http://www.rdanet.info">RDAnet</a>
<a href="http://www.lorks.info">Lorks</a>
<a href="http://www.karikaturmurah.com">Karikatur</a>
<a href="http://www.pusatsepatuonline.com">Sepatu Online</a>
<a href="http://www.pusatsepatuonline.com">Toko Sepatu Online</a>
<a href="http://www.pusatsepatuonline.com">Sepatu</a>
<a href="http://www.pusatsepatuonline.com">Sepatu Safety</a>