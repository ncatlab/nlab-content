
# Contents
* table of contents
{:toc}

## Idea

**Temporal logics**, as their name suggests, are logics that involve time.  They form a very large and important class of [[modal logics]], but here we will, to start with, only look at some simple cases. An important early example of a temporal logic is given by [[Arthur Prior]]'s **tense** logic.


## Basic temporal language, (BTL)

First the basic temporal language is built with two binary model operators, which instead of being denoted 'box' and 'diamond', are written $F$ and $P$.  The intended interpretation of these are:

* $F\phi$ is _$\phi$ will be true at some **future** time_;

* $P\phi$ is _$\phi$ was true at some **past** time.

The reason for the notation $F$ and $P$ should be clear.

* The dual of $F$ is $G$, so $G\phi = \neg F\neg \phi$. This means that we read $G\phi$ as 'at no future time is $\phi$ not true', i.e., $\phi$ is always **going** to be true. ($G$ for 'going'.)

* The dual of $P$ is written $H$, whence $H\phi = \neg P\neg \phi$ and $H\phi$ interprets as '$\phi$ **has** always been true'. ($H$ is for 'has' - which is a bit weak, but that is life!)

+-- {: . un_example}
###### Examples

*  If for all $\phi$ we have $P\phi \to G P\phi$, then _whatever has happened will always have happened_, which seems reasonable so this might be a suitable 'general truth' we might want a temporal logic to contain.

*  If we had in our logic that $F\phi \to F F\phi$, then this would means that if $\phi$ is true at some future time, then at some future time it will be true that $\phi$ will be true at some future time, so _between any two instants there must be a third_, and the general truth of this would say something about the 'internal structure' of time as modelled by such a logic. 
=--

This basic temporal language does not yet really constitute a sensible logic that could model important features of 'time'. but we can still look at models so as to see what properties of the models can be identified as corresponding to seemingly feasible formulae in the language.


## Frames and models for BTL

A _frame_ for BTL will be a set, $T$, with two binary relations $R_F$ and $R_P$.  We have $R_F x y$ reads that 'at $x$, $y$ is in the future'  - but, in the ordinary common sense meaning of words, this should mean $R_P y x$ and conversely.  In other words $R_P$ should be the _converse_ or [[opposite relation]] of $R_F$. 

(In general, if $R$ is a binary relation on a set $X$, then its [[opposite relation]] is defined by 

$$(y,x) \in R^{op} \Leftrightarrow (x,y)\in R.)$$

+-- {: .un_defn}
###### Definition

A frame of the form $(T,R,R^{op})$ is called a _bidirectional frame_.
=--

If we have **any** model $\mathfrak{M} = (T,R,V)$ with a valuation, $V$, then we can interpret BTL in terms of it by specifying  the interpretation of $P$ in terms that of $R$.  explicitly we define 

*  $\mathfrak{M}, t\models F\phi$ if and only if $\exists s (R t s \wedge \mathfrak{M}, s\models \phi);$

*  $\mathfrak{M}, t\models P\phi$ if and only if $\exists s (R s t \wedge \mathfrak{M}, s\models \phi)$,

but, of course, this is still a long way from having a logic that looks as if it captures 'time-like' behaviour. We could have models with 'circular time', and 'branching time'.  Both of these correspond to various situations in computational applications so should be kept in mind, both to be able to identify their occurrence and to build them in or to avoid them in the logics.

## (4)

One condition it would be natural to impose is transitivity of $R_F$, since if $F\phi$ is true at some future time, then clearly, $\phi$ itself must also be true at some future time, i.e., later on still!  This leads one to ask that 

$$(4) \quad\quad    F F\phi \to F\phi$$

should be in our logic,  (and similarly for $P$, but that will hold in the bidirectional models since if $R$ is transitive then so will be $R^{op}$).

## Temporal type theory in terms of adjoints

It is possible to specify a temporal type theory in the context of [[adjoint logic]]. Consider a category $\mathcal{C}$, and an [[internal category]] given by $b, e: Time_1 \rightrightarrows Time_0$. Here we understand elements of $Time_1$ as time intervals, and $b$ and $e$ as marking their beginning and end points. We may choose to impose additional structure on $Time$, e.g., that it be an internal [[poset]], or a [[linear order]].

Now each arrow, $b$ and $e$, generates an adjoint triple, e.g., $\sum_b \dashv  b^{\ast} \dashv \prod_b$, formed of [[dependent sum]], [[base change]], [[dependent product]], going between the slices $\mathcal{C}/Time_0$ and $\mathcal{C}/Time_1$. 

Then we find two adjunctions $\sum_b e^{\ast} \dashv \prod_e b^{\ast}$ and $\sum_e b^{\ast} \dashv \prod_b e^{\ast}$, e.g.,

$$
Hom(\sum_b e^{\ast} C(t), D(t)) = Hom(e^{\ast} C(t), b^{\ast} D(t)) = Hom(C(t), \prod_e b^{\ast} D(t)).
$$

Now consider for the moment that $C$ and $D$ are propositions. Then $\sum_b e^*C$ means "there is some interval beginning now and such that $C$ is true at its end", i.e. $F C$; while $\prod_e b^*D$ means "for all intervals ending now, $D$ is true at their beginning", i.e. $H D$. Hence our adjunction is $F \dashv H$. Similarly, interchanging $b$ and $e$, we find $P \dashv G$. Note that we don't have to assume the classical principle $G\phi = \neg F\neg \phi$ and $H\phi = \neg P\neg \phi$.

In the setting of dependent type theory, we do not need to restrict to propositions, but can treat the temporal operators on general time-dependent types. So if $People(t)$ is the type of people alive at $t$, $F People(t)$ is the type of people alive at a point in the future of $t$, and $G People(t)$ is a function from future times to people alive at that time, e.g., an element of this is 'The oldest person alive(t)'.

Since $Time$ is a category, we have in addition to the two projections $p,q:Time_1\times_{Time_0} Time_1 \to Time_1$, composition $c:Time_1\times_{Time_0} Time_1 \to Time_1$. This allows us to express more subtle temporal expressions, such as '$\phi$ has been true since a time when $\psi$ was true', denoted $\phi S \psi$.

$$\phi S \psi := \Sigma_e (b^* \psi \times \Pi_c (e p)^* \phi) $$

(note $e p = b q$).  That is, there is a subinterval ending now such that $\psi$ was true at its beginning and $\phi$ was true at all points inside it. Similarly, '$\phi$ will be true until a time when $\psi$ is true' is

$$\phi U \psi := \Sigma_b (e^* \psi \times \Pi_c (e p)^* \phi).$$

Temporal logicians have debated the relevant advantages of instant-based and interval-based approaches. Some have also considered hybrid approaches ([Balb11](#Balb11)). The analysis of this section suggests that working with intervals and instants together in the form of an internal category allows for a natural treatment via [[adjoint logic]].

An important construction in interval-based temporal logics is the **chop operator**, $C$ ([Venema 1991](#Venema91)). This applies to two interval properties, $\alpha$, $\beta$, so that $\alpha C \beta$ denotes the property of an interval that it may be divided into two sub-intervals such that $\alpha$ holds of the first and $\beta$ of the second. In our current framework we have $\alpha C \beta : \equiv \Sigma_c(p^{\ast}\alpha \times q^{\ast} \beta)$.

One of the consequences of taking $Time$ as an internal category is that the future includes the present, so that $\phi$ could be true now and at no other instant but we would have that $F \phi$ is true when it is supposed to say "$\phi$ will be true at some Future time". Similarly, we would have that $\phi U \psi$ holds now if $\psi$ and $\phi$ both hold now (in general, as defined above it requires $\phi$ to still hold at the instant when $\psi$ becomes true).  

If we wish to change these consequences, we could let $Time_1$ be the $\lt$-intervals instead of the $\le$-ones. In other words, we could take $Time$ to be a [[semicategory]]. While this accords with standard practice, the original alternative has been proposed:

>The most common practice in temporal logic is to regard time as an irreflexive ordering, so that "henceforth", meaning "at all future times", does not refer to the present moment. On the other hand, the Greek philosopher Diodorus proposed that the necessary be identified with that which is now and will always be the case. This suggests a temporal interpretation of $\Box$ that is naturally formalised by using reflexive orderings. The same interpretation is adopted in the logic of concurrent programs to be discussed. ([Gold92, p. 44](#Gold92))

On the other hand, some temporal logicians look to represent both forms of 'henceforth'.

For an related approach to temporal type theory, see ([Schultz-Spivak 17](#SchSpi17)).

## Computation tree logic

In [[computer science]], logics have been devised for dealing with the behaviours of entities undergoing transitions between its states. Where in a linear temporal logic, operators are provided for describing events along a single computation path, in a branching-time logic the temporal operators quantify over the paths that are possible from a given state. The **computation tree logic** $CTL^{\ast}$ (pronounced "CTL star") combines both the branching-time operators of $CTL$ and the linear-time operators of $LTL$.

Starting from a [[transition system|finite-state system]], where a finite collection of states represented by the nodes of a graph are connected by labelled edges representing transitions, the path tree of the system can be generated. This presents as a [[tree]] all possible paths that the system may undergo from an initial state.

The Computation tree logic $CTL^{\ast}$ is then deployed to reason about the behaviour of the system. This allows for quantification, both universal and existential, over paths. It is also possible to express that a certain state will occur at some point in the future or always in the future. 

Now beyond the $F$ and $G$ operators above, we can express new operators such as 'necessarily in the future' to convey that along every path emanating from the current state that some property will hold at some point, and 'possibly henceforth' to convey that there is at least one path along which some property holds at every point.

There is a [[Curry-Howard correspondence]] between linear-time temporal logic (LTL) and functional reactive programming (FRP) ([Jeffrey 12](#Jeffrey12), [Jeltsch 12](#Jeltsch12)).



## References

Generally this entry is based on

* P. Blackburn, M. de Rijke and Y. Vedema, _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001, 

but see also:

*  A. Galton, [Temporal Logic, (Stanford Encyclopedia of Philosophy)] (http://plato.stanford.edu/entries/logic-temporal/)

* [[Patrick Blackburn]], _Tense, Temporal Reference and Tense Logic_, Journal of Semantics, 1994,11,
    pages 83--101, [on-line version](http://hylo.loria.fr/content/papers/files/tense.pdf)

* [[Arthur Prior]], 1957, _Time and Modality_, Oxford: Clarendon Press.

* [[Arthur Prior]], 1967, _Past, Present and Future_, Oxford: Clarendon Press.

* {#Balb11} Balbiani, P., Goranko, V. and Sciavicco, G., 2011, 'Two-sorted Point-Interval Temporal logics', in _Proc. of the 7th International Workshop on Methods for Modalities (M4M7)_ (Electronic Notes in Theoretical Computer Science: Volume 278), pp. 31&#8211;45.

* {#Gold92} [[Robert Goldblatt]],  _Logics of time and computation_, 1992, ([pdf](http://sul-derivatives.stanford.edu/derivative?CSNID=00003782&mediaType=application/pdf))

For the relationship between linear-time temporal logic and functional reactive programming, see

* {#Jeffrey12} Alan Jeffrey _LTL types FRP: Linear-time temporal logic propositions as types, proofs as functional reactive programs_, in: Proceedings of the Sixth Workshop on Programming Languages Meets Program Verification (PLPV ’12)(2012), pp. 49–60. ([pdf](http://ect.bell-labs.com/who/ajeffrey/papers/plpv12.pdf))

* {#Jeltsch12} Wolfgang Jeltsch, _Towards a Common Categorical Semantics for Linear-Time Temporal Logic and Functional Reactive Programming_, Electronic Notes in Theoretical Computer Science 286, pp. 229-242, ([doi](https://doi.org/10.1016/j.entcs.2012.08.015))

For an interval-based approach see

* {#Venema91} Yde Venema, _A modal logic for chopping intervals_. Journal of Logic and Computation, 1(4), pp. 453–476, 1991.

For versions of temporal type theory see

* {#SchSpi17} Patrick Schultz, David Spivak, _Temporal Type Theory: A topos-theoretic approach to systems and behavior_, ([arXiv:1710.10258](https://arxiv.org/abs/1710.10258))


* {#Corfield20} [[David Corfield]], _Modal homotopy type theory_, Oxford University Press 2020, Sec. 4.3 ([ISBN: 9780198853404](https://global.oup.com/academic/product/modal-homotopy-type-theory-9780198853404))


[[!redirects temporal logic]]
[[!redirects temporal logics]]