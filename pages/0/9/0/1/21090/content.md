+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The formalism of *Markov categories* and *copy-discard categories* is a [[categorical approach to probability theory]] introduced by [Cho & Jacobs 2019](#cd_categories) and [Fritz 2020](#fritzmarkov) (and by other authors independently, see the [History](#history) section).

Intuitively, a Markov category is a category where morphisms behave like "random functions", for example, [[Markov kernels]] form such a category (hence the name). Canonical examples are [[Kleisli categories]] of [[probability monads]]. The formalism is however far more general. 

Markov categories have a graphical formalism, based on [[string diagrams]], that allows one to easily keep track of stochastic dependencies, as well as of randomness and determinism. 
Using this formalism one can interpret, prove and even *generalize* several results of probability and related fields (see [[categorical probability#main_results|Categorical probability -- results]] for more details).



## Definitions

A concise definition, which we interpret below, can be given as follows: A **Markov category** is a [[semicartesian monoidal category|semicartesian]] [[symmetric monoidal category]] $(C,\otimes,1)$ which [[supply in a monoidal category|supplies]] [[cocommutative comonoids]], i.e. in which every [[object]] $X$ is equipped with the [[structure]] of a [[commutative]] [[internal monoid|internal comonoid]] compatible with the tensor product.

The [[comultiplication]] and [[counit]] maps are usually denoted by $copy: X \to X \otimes X$ and $del: X\to 1$. 

Let's now restate the definition in a more intuitive, mathematically equivalent way, by making use of [[string diagrams]].

### String diagrams for monoidal categories

It is useful to introduce a [[string diagram]] notation for Markov categories, which is used throughout the literature, and which makes stochastic interactions particularly intuitive. 

First of all, we represent a [[morphism]] $f:X\to Y$ in a [[monoidal category]] as follows, which we read *from bottom to top*:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=none] (0) at (0, -1) {};
		\node [style=none] (1) at (0, 1) {};
		\node [style=none] (2) at (0, -1.5) {$X$};
		\node [style=none] (3) at (0, 1.5) {$Y$};

		\draw (0.center) to (1.center);

        \node [style=morphism] (4) at (0, 0) {$f$};
\end{tikzpicture}

Notice that, across the literature, convention vary (for example, also left-to-right is used.)
When domain and codomain are clear, we will omit them:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=none] (0) at (0, -1) {};
		\node [style=none] (1) at (0, 1) {};

		\draw (0.center) to (1.center);

        \node [style=morphism] (4) at (0, 0) {$f$};
\end{tikzpicture}

We represent the object $X$, as well as its [[identity]] morphism, simply as a wire:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=none] (0) at (0, -1) {};
		\node [style=none] (1) at (0, 1) {};
		\node [style=none] (2) at (0, -1.5) {$X$};
		\node [style=none] (3) at (0, 1.5) {$X$};

		\draw (0.center) to (1.center);

                \node [style=none] (4) at (2, 0) {or};

		\node [style=none] (5) at (4, -1) {};
		\node [style=none] (6) at (4, 1) {};
		\node [style=none] (7) at (4.5, 0) {$X$};

		\draw (5.center) to (6.center);
\end{tikzpicture}

The (sequential) [[composition]] of morphisms $f:X\to Y$ and $g:Y\to Z$ is drawn as follows:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]
	
		\node [style=none] (0) at (-2, -2.5) {};
		\node [style=none] (1) at (-2, 2.5) {};
		\node [style=none] (2) at (-2, -3) {$X$};
		\node [style=none] (3) at (-2, 3) {$Z$};
		\node [style=none] (6) at (2, -1.75) {};
		\node [style=none] (7) at (2, 1.75) {};
		\node [style=none] (8) at (2, -2.25) {$X$};
		\node [style=none] (9) at (2, 2.25) {$Z$};
		\node [style=none] (12) at (0, 0) {or};
		\node [style=none] (13) at (-2.5, 0) {$Y$};

		\draw (0.center) to (1.center);
		\draw (6.center) to (7.center);

		\node [style=morphism] (4) at (-2, -1.5) {$f$};
		\node [style=morphism] (5) at (-2, 1.5) {$g$};
		\node [style=morphism] (10) at (2, -0.75) {$f$};
		\node [style=morphism] (11) at (2, 0.75) {$g$};
\end{tikzpicture}

The [[tensor product]] of the monoidal category, or parallel composition, is represented as follows. 
First of all, given objects $A$, $B$, $X$ and $Y$, a morphism $h:A\otimes B\to X\otimes Y$ is depicted as a box with multiple input and output wires: 

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=none] (0) at (-0.75, -1) {};
		\node [style=none] (1) at (0.75, -1) {};
		\node [style=none] (2) at (-0.75, 1) {};
		\node [style=none] (3) at (0.75, 1) {};
		\node [style=none] (4) at (-0.75, -1.5) {$A$};
		\node [style=none] (5) at (0.75, -1.5) {$B$};
		\node [style=none] (6) at (-0.75, 1.5) {$X$};
		\node [style=none] (7) at (0.75, 1.5) {$Y$};

		\draw (2.center) to (0.center);
		\draw (3.center) to (1.center);

		\node [style=morphism] (8) at (0, 0) {$\quad h\quad$};
\end{tikzpicture}

Now given $f:A\to X$ and $g:B\to Y$, the parallel composition $f\otimes g:A\otimes B\to X\otimes Y$ is represented by juxtaposition:
\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]
\node [style=none] (0) at (-0.75, -1) {};
		\node [style=none] (1) at (0.75, -1) {};
		\node [style=none] (2) at (-0.75, 1) {};
		\node [style=none] (3) at (0.75, 1) {};
		\node [style=none] (4) at (-0.75, -1.5) {$A$};
		\node [style=none] (5) at (0.75, -1.5) {$B$};
		\node [style=none] (6) at (-0.75, 1.5) {$X$};
		\node [style=none] (7) at (0.75, 1.5) {$Y$};

		\draw (2.center) to (0.center);
		\draw (3.center) to (1.center);

		\node [style=morphism] (8) at (-0.75, 0) {$f$};
                \node [style=morphism] (9) at (0.75, 0) {$g$};
\end{tikzpicture}

This highlights that this situation is *non-signalling*: here, $X$ depends on $A$ only, and not on $B$, while in the generic case of $h$ above, $X$ may depend both on $A$ and $B$. This will be particularly relevant when we discuss stochastic interactions (see below).

Similarly, one can form the product of three or more objects and morphisms. Note that in the diagrams, the product is strictly associative: string diagrams technically represent, rather than the original category, a [[strict monoidal category]] which is [[monoidal equivalence|monoidally equivalent]] to the original one; such a category always exists thanks to the [[coherence theorem for monoidal categories|coherence theorem]].

In a similar vein, the monoidal unit usually does not appear explicitly in string diagrams, providing this elision does not cause confusion. This way, for example, the diagram

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=none] (5) at (4, -1) {};
		\node [style=none] (6) at (4, 1) {};
		\node [style=none] (7) at (4.5, 0) {$X$};

		\draw (5.center) to (6.center);
\end{tikzpicture}
 
represents the object $X$, but also $X\otimes I$, $I\otimes X$, and so on. 

Particular importance is given to *morphisms from the monoidal unit*, in the form $p:I\to X$, and which here we call **states**, and represent as follows.
\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=none] (0) at (0, -0.5) {};
		\node [style=none] (1) at (0, 1) {};
                \node [style=none] (2) at (0, 1.5) {$X$};

		\draw (0.center) to (1.center);

        \node [style=morphism] (4) at (0, -0.5) {$p$};
\end{tikzpicture}

These will model probabilistic states, such as probability measures (see below).
In the literature, states are also depicted as triangles.

To conclude this section, the [[braiding]] of the monoidal category is represented as follows:

\begin{tikzpicture}[%
thick,%
scale=0.5,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-5, 2) {};
		\node [style=none] (1) at (-2, 2) {};
		\node [style=none] (2) at (-5, -2) {};
		\node [style=none] (3) at (-2, -2) {};
		\node [style=none] (4) at (-5, -2.5) {$X$};
		\node [style=none] (5) at (-2, -2.5) {$Y$};
		\node [style=none] (6) at (-5, 2.5) {$Y$};
		\node [style=none] (7) at (-2, 2.5) {$X$};

		\draw [style=over arrow, in=90, out=-90] (1.center) to (2.center);
		\draw [style=over arrow, in=90, out=-90] (0.center) to (3.center);
\end{tikzpicture}

The [[unitors]] and [[associators]] are similarly omitted from the diagrams, except when it causes ambiguity.

Since we work in a [[symmetric monoidal category]], the braiding is its own inverse.

\begin{tikzpicture}[%
thick,%
scale=0.5,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-5, 2) {};
		\node [style=none] (1) at (-2, 2) {};
		\node [style=none] (2) at (-5, -2) {};
		\node [style=none] (3) at (-2, -2) {};
		\node [style=none] (4) at (-5, -2.5) {$X$};
		\node [style=none] (5) at (-2, -2.5) {$Y$};
		\node [style=none] (6) at (-5, 2.5) {$Y$};
		\node [style=none] (7) at (-2, 2.5) {$X$};
		\node [style=none] (8) at (0, 0) {$=$};
		\node [style=none] (9) at (2, 2) {};
		\node [style=none] (10) at (5, 2) {};
		\node [style=none] (11) at (2, -2) {};
		\node [style=none] (12) at (5, -2) {};
		\node [style=none] (13) at (2, -2.5) {$X$};
		\node [style=none] (14) at (5, -2.5) {$Y$};
		\node [style=none] (15) at (2, 2.5) {$Y$};
		\node [style=none] (16) at (5, 2.5) {$X$};

		\draw [style=over arrow, in=90, out=-90] (1.center) to (2.center);
		\draw [style=over arrow, in=90, out=-90] (0.center) to (3.center);
		\draw [style=over arrow, in=90, out=-90] (9.center) to (12.center);
		\draw [style=over arrow, in=90, out=-90] (10.center) to (11.center);
\end{tikzpicture}


### Commutative comonoids

Let $X$ be an [[object]] of a [[symmetric monoidal category]]. A [[commutative]] [[internal monoid|comonoid]] structure on $X$ consists first of all of maps $X\mapsto X\otimes X$ and $X\to I$, called the *comultiplication* and *counit*, or *copy* and *discard*. 
For the purposes of Markov categories, we denote them by $copy: X \to X \otimes X$ and $del: X\to 1$

In terms of string diagrams, we represent these maps as follows:
\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
]

		\node [style=bn] (0) at (-4, 0) {};
		\node [style=none] (1) at (-4.75, 0.75) {};
		\node [style=none] (2) at (-4, -0.75) {};
		\node [style=none] (3) at (-3.25, 0.75) {};
		\node [style=none] (4) at (-4.75, 1.25) {$X$};
		\node [style=none] (6) at (-3.25, 1.25) {$X$};
		\node [style=none] (7) at (-4, -1.25) {$X$};
		\node [style=none] (8) at (-9.5, 0) {$\mathrm{copy}$};
		\node [style=bn] (9) at (7, 0.5) {};
		\node [style=none] (10) at (7, -0.75) {};
		\node [style=none] (11) at (7, -1.25) {$X$};
		\node [style=none] (12) at (3, 0) {$\mathrm{del}$};
		\node [style=none] (13) at (-7, 0) {$=$};
		\node [style=none] (14) at (5, 0) {$=$};

		\draw [in=165, out=-90] (1.center) to (0);
		\draw [in=270, out=15] (0) to (3.center);
		\draw (0) to (2.center);
		\draw (9) to (10.center);

\end{tikzpicture}
which we can think of as "copying the state of $X$" and "discarding it".

These maps need to satisfy the following conditions (*commutativity*, *counitality*, *coassociativity*):

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=none] (1) at (-7.25, -0.75) {};
		\node [style=bn] (2) at (-7.25, 0) {};
		\node [style=none] (3) at (-8, 0.75) {};
		\node [style=none] (4) at (-6.5, 0.75) {};
		\node [style=none] (5) at (-9, 0.5) {$=$};
		\node [style=none] (7) at (0, -0.75) {};
		\node [style=none] (9) at (-1, 0.5) {$=$};
		\node [style=none] (14) at (-10.75, -0.75) {};
		\node [style=bn] (15) at (-10.75, 0) {};
		\node [style=none] (16) at (-11.5, 0.75) {};
		\node [style=none] (17) at (-10, 0.75) {};
		\node [style=none] (19) at (-2.75, -0.75) {};
		\node [style=bn] (20) at (-2.75, 0) {};
		\node [style=none] (21) at (-3.5, 0.75) {};
		\node [style=none] (22) at (-2, 0.75) {};
		\node [style=none] (24) at (-10, 2) {};
		\node [style=none] (25) at (-11.5, 2) {};
		\node [style=bn] (26) at (-3.5, 1) {};
		\node [style=none] (30) at (11.75, -0.75) {};
		\node [style=bn] (31) at (11.75, 0) {};
		\node [style=none] (32) at (11, 0.75) {};
		\node [style=none] (33) at (12.75, 1) {};
		\node [style=none] (34) at (12, 1.75) {};
		\node [style=none] (35) at (13.5, 1.75) {};
		\node [style=bn] (36) at (12.75, 1) {};
		\node [style=none] (38) at (8.25, -0.75) {};
		\node [style=bn] (39) at (8.25, 0) {};
		\node [style=none] (41) at (9, 0.75) {};
		\node [style=none] (46) at (10, 0.5) {$=$};
		\node [style=none] (47) at (7.25, 1) {};
		\node [style=none] (48) at (6.5, 1.75) {};
		\node [style=none] (49) at (8, 1.75) {};
		\node [style=bn] (50) at (7.25, 1) {};
		\node [style=none] (51) at (-8, 2) {};
		\node [style=none] (52) at (-6.5, 2) {};
		\node [style=none] (53) at (-2, 2) {};
		\node [style=none] (54) at (0, 2) {};
		\node [style=none] (55) at (11, 0.75) {};
		\node [style=none] (56) at (11, 2) {};
		\node [style=none] (57) at (9, 2) {};
		\node [style=none] (58) at (12, 2) {};
		\node [style=none] (59) at (13.5, 2) {};
		\node [style=none] (60) at (6.5, 2) {};
		\node [style=none] (61) at (8, 2) {};
		\node [style=none] (62) at (1, 0.5) {$=$};
		\node [style=none] (63) at (2.75, -0.75) {};
		\node [style=bn] (64) at (2.75, 0) {};
		\node [style=none] (65) at (2, 0.75) {};
		\node [style=none] (66) at (3.5, 0.75) {};
		\node [style=none] (69) at (2, 2) {};
		\node [style=bn] (70) at (3.5, 1) {};

		\draw (2) to (1.center);
		\draw [in=165, out=-90] (3.center) to (2);
		\draw [in=270, out=15] (2) to (4.center);
		\draw (15) to (14.center);
		\draw [in=165, out=-90] (16.center) to (15);
		\draw [in=270, out=15] (15) to (17.center);
		\draw (20) to (19.center);
		\draw [in=165, out=-90] (21.center) to (20);
		\draw [in=270, out=15] (20) to (22.center);
		\draw (31) to (30.center);
		\draw [in=165, out=-90] (32.center) to (31);
		\draw [in=270, out=15] (31) to (33.center);
		\draw [in=165, out=-90] (34.center) to (36);
		\draw [in=-90, out=15] (36) to (35.center);
		\draw (39) to (38.center);
		\draw [in=-90, out=15] (39) to (41.center);
		\draw [in=165, out=-90] (48.center) to (50);
		\draw [in=-90, out=15] (50) to (49.center);
		\draw [in=270, out=165] (39) to (50);
		\draw (52.center) to (4.center);
		\draw (51.center) to (3.center);
		\draw (53.center) to (22.center);
		\draw (54.center) to (7.center);
		\draw (56.center) to (55.center);
		\draw (57.center) to (41.center);
		\draw [style=over arrow, in=90, out=-90] (25.center) to (17.center);
		\draw [style=over arrow, in=90, out=-90] (24.center) to (16.center);
		\draw (58.center) to (34.center);
		\draw (59.center) to (35.center);
		\draw (60.center) to (48.center);
		\draw (61.center) to (49.center);
		\draw (26) to (21.center);
		\draw (64) to (63.center);
		\draw [in=165, out=-90] (65.center) to (64);
		\draw [in=270, out=15] (64) to (66.center);
		\draw (69.center) to (65.center);
		\draw (70) to (66.center);
\end{tikzpicture}

which we can interpret as the facts that 

* The two copies are interchangeable;
* Copying once and discarding one of the two copies is the same as doing nothing;
* Copying once and then copying one of the copies is the same as copying the other copy.

In other words, these conditions assure that the interpretation as "copying and discarding information" is consistent. 


### Markov and CD categories

A **copy-discard (CD) category** or **garbage-share (GS) monoidal category** is a symmetric monoidal category where 

* Every object is equipped with a distinguished commutative comonoid structure;

* The comonoid structures are compatible with the tensor products in the following ways. 

First for all, for all objects $X$ and $Y$, 
$$
copy_{X\otimes Y} \; =\; (id_X\otimes b_{Y,X} \otimes id_Y) ( copy_X \otimes copy_Y ),
$$
where $b$ denotes the [[braiding]]. In terms of string diagrams:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=none] (1) at (3, 2) {};
		\node [style=none] (2) at (-3.75, -1.5) {};
		\node [style=none] (3) at (4.5, 0.5) {};
		\node [style=none] (4) at (3, 2.5) {$Y$};
		\node [style=none] (6) at (4.5, 2.5) {$X$};
		\node [style=none] (7) at (-3.75, -2) {$X\otimes Y$};
		\node [style=none] (14) at (-0.25, 0) {$=$};
		\node [style=none] (15) at (4.5, 2) {};
		\node [style=none] (32) at (3, 0.5) {};
		\node [style=none] (33) at (-3.75, -0.5) {};
		\node [style=none] (34) at (-3.75, -1.5) {};
		\node [style=none] (35) at (2.25, -1.25) {};
		\node [style=none] (37) at (2.25, -1.75) {$X$};
		\node [style=none] (38) at (5.25, -1.75) {$Y$};
		\node [style=none] (39) at (2.25, -0.25) {};
		\node [style=none] (40) at (5.25, -0.25) {};
		\node [style=none] (41) at (5.25, -1.25) {};
		\node [style=bn] (42) at (2.25, -0.25) {};
		\node [style=bn] (43) at (5.25, -0.25) {};
		\node [style=none] (44) at (1.5, 0.5) {};
		\node [style=none] (45) at (3, 0.5) {};
		\node [style=none] (46) at (6, 0.5) {};
		\node [style=none] (47) at (1.5, 2) {};
		\node [style=none] (48) at (6, 2) {};
		\node [style=none] (49) at (1.5, 2.5) {$X$};
		\node [style=none] (50) at (6, 2.5) {$Y$};
		\node [style=none] (51) at (-2, 2.5) {$X\otimes Y$};
		\node [style=none] (52) at (-5.5, 2.5) {$X\otimes Y$};
		\node [style=bn] (53) at (-3.75, -0.5) {};
		\node [style=none] (54) at (-5.5, 1.25) {};
		\node [style=none] (55) at (-2, 1.25) {};
		\node [style=none] (56) at (-5.5, 2) {};
		\node [style=none] (57) at (-2, 2) {};

		\draw (34.center) to (33.center);
		\draw (39.center) to (35.center);
		\draw (40.center) to (41.center);
		\draw [in=165, out=-90] (44.center) to (42);
		\draw [in=15, out=-90] (45.center) to (42);
		\draw [in=165, out=-90] (3.center) to (43);
		\draw [in=15, out=-90] (46.center) to (43);
		\draw (47.center) to (44.center);
		\draw (48.center) to (46.center);
		\draw [in=165, out=-90] (54.center) to (53);
		\draw [in=15, out=-90] (55.center) to (53);
		\draw (56.center) to (54.center);
		\draw (57.center) to (55.center);
		\draw [style=over arrow, in=-90, out=90] (45.center) to (15.center);
		\draw [style=over arrow, in=90, out=-90] (1.center) to (3.center);
\end{tikzpicture}

Similarly, we also have the following conditions (recall that the monoidal unit, unitors and associators are not depicted):

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
 
		\node [style=none] (0) at (-6, -1) {};
		\node [style=none] (1) at (-5, -1) {};
		\node [style=none] (2) at (-6, -1.5) {$X$};
		\node [style=none] (3) at (-5, -1.5) {$Y$};
		\node [style=bn] (4) at (-6, 1) {};
		\node [style=bn] (5) at (-5, 1) {};
		\node [style=bn] (6) at (-10, 1) {};
		\node [style=none] (7) at (-8, 0) {$=$};
		\node [style=none] (8) at (-10, -1) {};
		\node [style=none] (9) at (-10, -1.5) {$X\otimes Y$};
		\node [style=none] (10) at (1, -1) {};
		\node [style=bn] (11) at (1, 1) {};
		\node [style=none] (12) at (1, -1.5) {$I$};
		\node [style=none] (13) at (3, 0) {$=$};
		\node [style=none] (14) at (5, 2) {};
		\node [style=none] (15) at (5, -2) {};
		\node [style=none] (16) at (9, 2) {};
		\node [style=none] (17) at (9, -2) {};
		\node [style=none] (18) at (11, 0) {$=$};
		\node [style=none] (19) at (14, -1) {};
		\node [style=none] (20) at (14, -1.5) {$I$};
		\node [style=bn] (21) at (14, 0) {};
		\node [style=none] (22) at (13, 1) {};
		\node [style=none] (23) at (15, 1) {};
		\node [style=none] (24) at (13, 1.5) {$I$};
		\node [style=none] (25) at (15, 1.5) {$I$};
 
		\draw (4) to (0.center);
		\draw (5) to (1.center);
		\draw (6) to (8.center);
		\draw (11) to (10.center);
		\draw [dashed] (14.center) to (16.center);
		\draw [dashed] (16.center) to (17.center);
		\draw [dashed] (17.center) to (15.center);
		\draw [dashed] (15.center) to (14.center);
		\draw [in=165, out=-90] (22.center) to (21);
		\draw (21) to (19.center);
		\draw [bend left] (23.center) to (21);
 
\end{tikzpicture}

A **Markov category** or **affine CD category** is a CD category where any of these equivalent conditions hold:

* The monoidal unit $I$ is a [[terminal object]] (i.e. the category is [[semicartesian monoidal category|semicartesian monoidal]]);
* The discard (counit) maps $del:X\to I$ are part of a [[natural transformation]] $id\Rightarrow I$;
* For every morphism $f:X\to Y$, we have that $del_Y \circ f = \del_X$.

The last equation can be written in terms of string diagrams as follows:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-2, -1) {};
		\node [style=bn] (1) at (-2, 1) {};
		\node [style=bn] (2) at (1.75, 0.5) {};
		\node [style=none] (3) at (1.75, -1) {};
		\node [style=none] (5) at (0, 0) {$=$};

		\draw (1) to (0.center);
		\draw (2) to (3.center);

		\node [style=morphism] (4) at (-2, 0) {$f$};
\end{tikzpicture}

This condition can be interpreted as follows:

* From the point of view of [[information theory]], it says that processing any information and discarding the result is the same as discarding the input altogether.
* From the point of view of [[probability theory]], it says that probabilities are normalized to one. (More on that below.)

Notice also that if we assume that the monoidal unit is terminal, all compatibility conditions between the comonoid structures and the tensor product except the first one are satisfied.



## Examples 

Let's start with a simple example where randommess is not involved, the category of sets.
We then look at more interesting cases where randomness is involved, [[FinStoch]] and [[Stoch]].

See also the [detailed list below](#DetailedList).


### The copy-discard structure of *Set*

Consider the category [[Set]] of sets and functions, with its usual cartesian monoidal structure (given by the cartesian product of sets). 

Every set $X$ is equipped with canonical maps
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
 X \ar{r}{\mathrm{diag}} & X\times X && X \ar{r}{!} & 1 \\
x \ar[mapsto]{r} & (x,x) && x \ar[mapsto]{r} & *
\end{tikzcd}

which can be interpreted as "copying the value of $x$" and "discarding it" (we denote by $*$ the unique element of the terminal set $1$). 
It can be easily checked that these maps make $X$ a commutative comonoid, and that these maps are compatible with the tensor product.
Since the monoidal unit is terminal, we have a Markov category.

The same can be done in every cartesian monoidal category:

\begin{proposition}\label{cartmon1}
In a cartesian monoidal category every object is equipped with a unique commutative comonoid structure, defined in terms of the universal property of the product.
\end{proposition}

In cartesian monoidal categories, no randomness is present (as defined below), and so the Markov structure is purely about manipulating information deterministically: information can be copied, discarded, and processed deterministically (through arbitrary morphisms). 

\begin{remark}
Note that, while the copy-discard structure of *Set* and of other cartesian monoidal categories may seem trivial, it is not.
The copy map is implicitly used whenever we are *reusing* a variable in an expression. For example, every function $f:X\times X\to Y$ also defines a function $f':X\to Y$ by just "pluggin in $x$ twice": 
$$
f'(x) = f(x,x) .
$$
What happened under the hood is the following composition:
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
X \ar{r}{\mathrm{diag}} \ar[bend left=35]{rr}{f'} & X\times X \ar{r}{f} & Y \\
x \ar[mapsto]{r} & (x,x) \ar[mapsto]{r} & f(x,x)
\end{tikzcd}
In string diagrams, we write this as follows.

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=bn] (0) at (2.75, -1) {};
		\node [style=none] (1) at (2, -0.25) {};
		\node [style=none] (2) at (3.5, -0.25) {};
		\node [style=none] (3) at (2, 0.25) {};
		\node [style=none] (4) at (3.5, 0.25) {};
		\node [style=none] (5) at (2.75, 0.25) {};
		\node [style=none] (6) at (2.75, 1.5) {};
		\node [style=none] (7) at (2.75, 2) {$Y$};
		\node [style=none] (8) at (2.75, -1.75) {};
		\node [style=none] (9) at (2.75, -2.25) {$X$};
		\node [style=none] (10) at (-2, 1.5) {};
		\node [style=none] (11) at (-2, -1.75) {};
		\node [style=none] (12) at (-2, -2.25) {$X$};
		\node [style=none] (13) at (-2, 2) {$Y$};
		\node [style=none] (16) at (0, 0) {$=$};

		\draw [in=165, out=-90] (1.center) to (0);
		\draw [in=15, out=-90] (2.center) to (0);
		\draw (3.center) to (1.center);
		\draw (4.center) to (2.center);
		\draw (6.center) to (5.center);
		\draw (0) to (8.center);
		\draw (10.center) to (11.center);

		\node [style=morphism] (14) at (-2, 0) {$f'$};
		\node [style=morphism] (15) at (2.75, 0.25) {$\quad f \quad$};
\end{tikzpicture}

Similarly, the discard map is used whenever we are *not using* a variable in an expression. For example, every function $g:X\to Y$ also defines a function $g':X\times A\to Y$ which "does not really depend on $A$":
$$
g'(x,a) = g(x) .
$$
What happened under the hood is the following composition,
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
X\times A \ar[bend left=35]{rr}{g'} \ar{r}{\mathrm{id}\times !} & X\times 1\cong X \ar{r}{g} & Y \\
(x,a) \ar[mapsto]{r} & x \ar[mapsto]{r} & g(x)
\end{tikzcd}
which in string diagrams we write as follows.

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]
	
		\node [style=none] (0) at (-3.75, -1.5) {};
		\node [style=none] (1) at (-3, 1.5) {};
		\node [style=none] (2) at (-3.75, -2) {$X$};
		\node [style=none] (3) at (-3, 2) {$Y$};
		\node [style=none] (4) at (-2.25, -1.5) {};
		\node [style=none] (5) at (-2.25, -2) {$A$};
		\node [style=none] (6) at (-3, 0) {};
		\node [style=none] (7) at (-3, 0) {};
		\node [style=none] (8) at (-3.75, 0) {};
		\node [style=none] (9) at (-2.25, 0) {};
		\node [style=none] (10) at (0, 0) {$=$};
		\node [style=none] (11) at (2.25, -1.5) {};
		\node [style=none] (13) at (2.25, -2) {$X$};
		\node [style=none] (14) at (2.25, 2) {$Y$};
		\node [style=none] (15) at (3.75, -1.5) {};
		\node [style=none] (16) at (3.75, -2) {$A$};
		\node [style=none] (19) at (2.25, 1.5) {};
		\node [style=bn] (21) at (3.75, 0) {};

		\draw (7.center) to (1.center);
		\draw (8.center) to (0.center);
		\draw (9.center) to (4.center);
		\draw (19.center) to (11.center);
		\draw (21) to (15.center);

		\node [style=morphism] (22) at (-3, 0) {$\quad g' \quad$};
		\node [style=morphism] (23) at (2.25, 0) {$g$};
\end{tikzpicture}

In particular, every element $y\in Y$ can be seen as a *constant* function $X\to Y$ which does not really depend on $X$. 

As we will see, once probabilities are involved, copying and discarding will require particular care, due to the presence of possible correlation.
Markov and CD categories allow us to keep track of these operations graphically, avoiding many possible pitfalls, and even using them to our advantage.
\end{remark}


### The category *FinStoch* of stochastic matrices

Let's now look at a category where randomness is involved.
Let $X$ and $Y$ be [[finite sets]]. 
Recall that a [[stochastic matrix]], or *stochastic map*, between them is a function 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
 X\times Y \ar{r} & {[0,1]} \\
(x,y) \ar[mapsto]{r} & f(y|x)
\end{tikzcd}
such that 
\begin{equation}\label{norm}
\sum_{y\in Y} f(y|x)  = 1
\end{equation}
for every $x\in X$.

We can interpret the number $f(y|x)$ as the probability of transitioning from $x$ to $y$, in a stochastic way.
Note that in particular, [[stochastic map#stochastic_maps_from_deterministic_functions|every deterministic function defines a stochastic matrix]]: if $f:X\to Y$ is an ordinary function, we can write a stochastic matrix $\delta_f$ from $X$ to $Y$ by saying that $\delta_f(y|x)=1$ if $y=f(x)$, and $0$ otherwise. Therefore these random transitions include the deterministic ones as a special case.

See [[stochastic map]] for more information, and for how they compose.

Similarly to what we did for [[Set]], we can assign copy and discard maps to our object, which intuitively copy and discard information deterministically. 
First of all, as monoidal structure we again take the cartesian product of sets. (In this category, it is not a [[cartesian product|categorical product]], but it's still a [[monoidal category|monoidal]] one.)

The tensor product of morphisms $f:A\to X$ and $g:B\to Y$
\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]
\node [style=none] (0) at (-0.75, -1) {};
		\node [style=none] (1) at (0.75, -1) {};
		\node [style=none] (2) at (-0.75, 1) {};
		\node [style=none] (3) at (0.75, 1) {};
		\node [style=none] (4) at (-0.75, -1.5) {$A$};
		\node [style=none] (5) at (0.75, -1.5) {$B$};
		\node [style=none] (6) at (-0.75, 1.5) {$X$};
		\node [style=none] (7) at (0.75, 1.5) {$Y$};

		\draw (2.center) to (0.center);
		\draw (3.center) to (1.center);

		\node [style=morphism] (8) at (-0.75, 0) {$f$};
                \node [style=morphism] (9) at (0.75, 0) {$g$};
\end{tikzpicture}

is the stochastic matrix $A\otimes B\to X\otimes Y$ of entries
$$
(f\otimes g) (x,y|a,b) = f(x|a) \, g(y|b) ,
$$
which says that the two transitions are happening independently.
In particular, for the case of states, the product of $p:1\to X$ and $q:1\to X$,

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-0.75, -0.75) {};
		\node [style=none] (1) at (-0.75, 0.75) {};
		\node [style=none] (2) at (0.75, 0.75) {};
		\node [style=none] (3) at (0.75, -0.75) {};
		\node [style=none] (4) at (-0.75, 1.25) {$X$};
		\node [style=none] (5) at (0.75, 1.25) {$Y$};

		\draw (1.center) to (0.center);
		\draw (2.center) to (3.center);

		\node [style=morphism] (6) at (-0.75, -0.75) {$p$};
		\node [style=morphism] (7) at (0.75, -0.75) {$q$};
\end{tikzpicture}

is the _product probability_ 
$$
(p\otimes q)(x,y) = p(x)\,q(y) ,
$$
which as usual denotes independent events. 


We define the copy and discard maps as the maps $\delta_copy$ and $\delta_del$ induced by the ones of *Set* (see the example above). 
Explicitly, the stochastic map $copy:X\to X\otimes X$ is defined by 
$$
copy(x',x''|x) = \begin{cases}
1 & x'=x''=x ; \\
0 & otherwise.
\end{cases}
$$
The stochastic map $del:X\to 1$ satisfies
$$
del(*|x) = 1 ,
$$
where $*$ is the unique element of the terminal set $1$.

Again, one can check that these maps make $X$ a commutative comonoid, and that these maps are compatible with the tensor product.

The reason why we have a *Markov* category and not just a CD category is exactly the normalization condition \eqref{norm}: given a stochastic map $f:X\to Y$, the condition $del_Y\circ f = del_X$ reads exactly as 
$$
(del_Y\circ f) (*|x) = \sum_{y\in Y} del_Y(*|y) \, f(y|x) = \sum_{y\in Y} 1\, f(y|x) = 1 = \del_X(*|x)
$$
for every $x\in X$.


### The category *Stoch* of Markov kernels

Recall that given [[measurable spaces]] $(X,\mathcal{A})$ and $(Y,\mathcal{B})$, a [[Markov kernel]] between them is a function 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
X \times \mathcal{B} \ar{r} & {[0,1]} \\
(x,B) \ar[mapsto]{r} & k(B|x)
\end{tikzcd}
which is measurable in $x$ and which is a probability measure in $B$. We can view it as a generalization of a stochastic matrix outside the discrete case, where the number $k(B|x)$ is the probability of transitioning into $B$ if we are in $x$. (See [[Markov kernel]] for more on this.)

The category [[Stoch]] of measurable spaces and Markov kernels has a Markov category structure similar to the one of *FinStoch*.
As for *FinStoch*, as monoidal structure we take the one induced by the cartesian product of measurable spaces. Given measurable spaces $(X,\mathcal{A})$ and $(Y,\mathcal{B})$ (or more briefly, $X$ and $Y$), we take $X\otimes Y$ to be the cartesian product of sets $X\times Y$, equipped with the tensor product [[sigma-algebra]] $\mathcal{A}\otimes\mathcal{B}$, the one generated by the sets $A\times B\subseteq X\times Y$ for $A\in\mathcal{A}$ and $B\in\mathcal{B}$.
Just as in *FinStoch*, on morphisms we have the product of kernels, and the same is true for probability measures.

The copy and discard maps $X\to X\otimes X$ and $X\to 1$, just as for *FinStoch* (see above), are inherited from the ones of *Set*. Explicitly, for each object $(X,\mathcal{A})$, we have that for all $x\in X$ and for all $A,A'\in\mathcal{A}$,
$$
copy(A\times A'|x) = \delta(A\cap A'|x) = \begin{cases}
1 & x\in A\cap A' ; \\
0 & x\notin A\cap A' 
\end{cases}
$$
and 
$$
del(\{*\}|x) = 1 ,
$$
where $*$ is the unique element of the terminal measurable space $1$, the one-point space.

These again equip each object with a commutative comonoid structure compatible with the tensor product.

Just as for *FinStoch*, the fact that $1$ is terminal in [[Stoch]] reflects the fact that Markov kernels are normalized: for every kernel $f:X\to Y$ and for every $x\in X$,
$$
(del_Y\circ f) (\{*\}|x) = \int_Y del_Y(\{*\}|y) \, f(dy|x) = \int_Y 1\, f(dy|x) = 1 = \del_X(\{*\}|x) .
$$


### Kleisli categories of probability monads

As explained in [[probability monad]], often [[monads]] can be used to "add extra morphisms" to a category, to model behaviors that were not present in the original category. These new morphisms form the [[Kleisli category]], and are used, for example, [[monad (in computer science)|in computer science]] to model computational effects.
In particular, monads can be used to add *stochastic* maps to deterministic ones (more at [[probability monad]]), and very often, the resulting Kleisli category is a Markov category.


Let $C$ be a [[cartesian monoidal category]], which we can interpret as encoding "no randomness" (more on that below). For example, [[Set]].
As we have seen [above](#the_copydiscard_structure_of_set), $C$ has a canonical copy and discard structure. 

The [[Kleisli category]] of a [[commutative monad]] (or monoidal monad) $P$ on $C$, for example of most [[probability monads]], has a canonical copy-discard structure inherited from the one of $C$.
First of all, for every monoidal monad, [[monoidal monad#monoidal_structure_on_the_kleisli_category|the Kleisli category is canonically monoidal again]]. To define a copy-discard structure, we can use the one of $C$ and the unit of the monad: 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=small,%
]
X \ar{r}{\mathrm{diag}} & X\times X \ar{r}{\eta} & P(X\times X) \\
X \ar{r}{\mathrm{!}} & 1 \ar{r}{\eta} & P1
\end{tikzcd}

If moreover we have that $P$ preserves the monoidal unit ($P1\cong 1$, i.e. the monad is [[affine monad|affine]]), we have that $1$ is terminal in the Kleisli category as well, and so we have a Markov category.

Several Markov categories are obtained in this way, where the randomness is, in some sense, generated by the monad.
For example, [[Stoch]] is the Kleisli category of the [[Giry monad]].



## Core concepts

### States, channels, joints, marginals

The Markov category structures can be interpreted in terms of probability, statistics, and information theory in these ways. 

First of all, a state on $X$

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=none] (0) at (0, -0.5) {};
		\node [style=none] (1) at (0, 1) {};
                \node [style=none] (2) at (0, 1.5) {$X$};

		\draw (0.center) to (1.center);

        \node [style=morphism] (4) at (0, -0.5) {$p$};
\end{tikzpicture}

has the interpretation of a _probability measure_ on $X$, or in terms of information theory, a _noisy source_ with alphabet $X$. 

This reflect the intuition in our main examples:

* In [[FinStoch]], a state is exactly a $n\times 1$ stochastic matrix, i.e. a column vector whose entries sum to one. In other words, it is exactly a (discrete) probability distribution on $X$, of entries $p(x)$.
* In [[Stoch]], a state es exactly a probability measure on a measurable space $(X,\mathcal{A})$, of values $p(A)$ for $A\in\mathcal{A}$. 
* In [[Set]] (no randomness!), a state is exactly a function $1\to X$, i.e. a point $x$ of $X$. 

Let's now turn to morphisms:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=none] (0) at (0, -1) {};
		\node [style=none] (1) at (0, 1) {};
		\node [style=none] (2) at (0, -1.5) {$X$};
		\node [style=none] (3) at (0, 1.5) {$Y$};

		\draw (0.center) to (1.center);

        \node [style=morphism] (4) at (0, 0) {$f$};
\end{tikzpicture}

As we have already remarked, these can be thought of as _functions with possibly random outcomes_, or, from the point of view of information theory _potentially noisy channels_. 
In our basic examples:

* Morphisms of *FinStoch* are [[stochastic maps]];
* Morphisms of *Stoch* are [[Markov kernels]];
* Morphisms of *Set* (no randomness!) are [[functions]].

Morphisms in a Markov category have an additional useful interpretation: a morphism $f:X\to Y$ can also be seen as a _state on $Y$ which depends by a parameter $X$_. Indeed:

* In *FinStoch*, a stochastic map $f:X\to Y$, of entries $f(y|x)$, can be seen as a probability distribution on $Y$ which depends by a parameter $x\in X$;
* In *Stoch*, a Markov kernel $f:(X,\mathcal{A})\to (Y,\mathcal{B})$ of values $f(B|x)$ can be seen as a probability measure on $Y$ which depends *measurably* on $x\in X$, sometimes called a [[Markov kernel#regular_conditional_distributions|regular conditional distribution]].
* In *Set* (no randomness!), a function $f:X\to Y$ can be seen as a point of $Y$ parametrized by $X$. 

This idea can be seen as a stochastic version of [[generalized elements]].

Let's now turn to slightly more complex objects.
States in the form $p:I\to X\otimes Y$ are called **joint states**. 

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (10) at (-3, 0) {};
		\node [style=none] (11) at (-2, 0) {};
		\node [style=none] (12) at (-2, 1.25) {};
		\node [style=none] (13) at (-3, 1.25) {};
		\node [style=none] (14) at (-3, 1.75) {$X$};
		\node [style=none] (15) at (-2, 1.75) {$Y$};
		\node [style=none] (20) at (-2.5, 0) {};

		\draw (10.center) to (13.center);
		\draw (11.center) to (12.center);
        
                \node [style=morphism] (27) at (-2.5, 0) {$\;\, p \;\,$};
\end{tikzpicture}

This has the interpretation of "shared randomness between $X$ and $Y$, possibly with correlation or other interactions".

* In *FinStoch*, a joint state on $X\otimes Y$ is a [[joint probability distribution]] on $X\times Y$, of entries $p(x,y)$.
* In *Stoch*, a joint state on $X\otimes Y$ is a [[joint probability measure]] on $(X\times Y,\mathcal{A}\otimes\mathcal{B})$, specified uniquely by its values $p(A\times B)$ for $A\in\mathcal{A}$ and $B\in\mathcal{B}$.
* In *Set*, a joint state on $X\otimes Y$ is an ordered pair $(x,y)$.

Given a joint state $p$ on $X\otimes Y$, its **marginals** are the states $p_X$ and $p_Y$, on $X$ and $Y$ respectively, given by discarding the unobserved variable:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-3.5, -0.75) {};
		\node [style=none] (2) at (-4, 1) {};
		\node [style=none] (3) at (-4, 1.5) {$X$};
		\node [style=none] (4) at (-4, -0.5) {};
		\node [style=none] (5) at (-3, -0.5) {};
		\node [style=bn] (6) at (-3, 0.5) {};
		\node [style=none] (9) at (-8.25, 1) {};
		\node [style=none] (10) at (-8.25, 1.5) {$X$};
		\node [style=none] (11) at (-8.25, -0.5) {};
		\node [style=none] (12) at (-6, 0) {$=$};
		\node [style=none] (13) at (7.75, -0.75) {};
		\node [style=none] (15) at (8.25, 1) {};
		\node [style=none] (16) at (8.25, 1.5) {$Y$};
		\node [style=none] (17) at (8.25, -0.5) {};
		\node [style=none] (18) at (7.25, -0.5) {};
		\node [style=bn] (19) at (7.25, 0.5) {};
		\node [style=none] (21) at (3, 1) {};
		\node [style=none] (22) at (3, 1.5) {$Y$};
		\node [style=none] (23) at (3, -0.5) {};
		\node [style=none] (24) at (5.25, 0) {$=$};

		\draw (2.center) to (4.center);
		\draw (5.center) to (6);
		\draw (9.center) to (11.center);
		\draw (15.center) to (17.center);
		\draw (18.center) to (19);
		\draw (21.center) to (23.center);

		\node [style=morphism] (1) at (-3.5, -0.75) {$\;\, p \;\,$};
		\node [style=morphism] (8) at (-8.25, -0.75) {$p_X$};
		\node [style=morphism] (14) at (7.75, -0.75) {$\;\, p \;\,$};
		\node [style=morphism] (20) at (3, -0.75) {$p_Y$};
\end{tikzpicture}

This formalizes both the idea of "not observing" as well as the one of *averaging* or *integrating* over something:

* In *FinStoch*, the [[marginal distribution]] $p_X$ on $X$ formed by the [[joint distribution]] $p$ on $X\times Y$ is given by summing over $Y$:
$$
p_X(x) = \sum_{y\in Y} p(x,y)
$$
* In *Stoch*, the [[marginal distribution]] $p_X$ on $(X,\mathcal{A})$ formed by the [[joint distribution]] $p$ on $X\times Y$ is given by *integrating* over $Y$:
$$
p_X(A) = p(A\times Y) = \int_Y 1_A(x)\,p(d x\,d y)
$$
for all $A\in\mathcal{A}$.
* In *Set*, the marginal state $x\in X$ formed by the joint state $(x,y)\in X\otimes Y$ is simply given by discarding the second component.


Similarly, we call a **joint morphism** a morphism in the form $p:A\to X\otimes Y$.

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]

		\node [style=none] (9) at (-2.5, -1.25) {};
		\node [style=none] (10) at (-3, 0) {};
		\node [style=none] (11) at (-2, 0) {};
		\node [style=none] (12) at (-2, 1.25) {};
		\node [style=none] (13) at (-3, 1.25) {};
		\node [style=none] (14) at (-3, 1.75) {$X$};
		\node [style=none] (15) at (-2, 1.75) {$Y$};
		\node [style=none] (19) at (-2.5, -1.75) {$A$};
                \node [style=none] (20) at (-2.5, 0) {};

		\draw (9.center) to (20);
		\draw (10.center) to (13.center);
		\draw (11.center) to (12.center);

		\node [style=morphism] (27) at (-2.5, 0) {$\;\, p \;\,$};
\end{tikzpicture}

We can view this equivalently as a joint state which depends on a parameter $A$.
We form its **marginal morphisms** $p_X:A\to X$ and $p_X:A\to Y$ by discarding the unobserved variables:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]

		\node [style=none] (0) at (-3.5, -0.75) {};
		\node [style=none] (2) at (-4, 1) {};
		\node [style=none] (3) at (-4, 1.5) {$X$};
		\node [style=none] (4) at (-4, -0.5) {};
		\node [style=none] (5) at (-3, -0.5) {};
		\node [style=bn] (6) at (-3, 0.5) {};
		\node [style=none] (9) at (-8.25, 1) {};
		\node [style=none] (10) at (-8.25, 1.5) {$X$};
		\node [style=none] (11) at (-8.25, -0.5) {};
		\node [style=none] (12) at (-6, -0.5) {$=$};
		\node [style=none] (13) at (7.75, -0.75) {};
		\node [style=none] (15) at (8.25, 1) {};
		\node [style=none] (16) at (8.25, 1.5) {$Y$};
		\node [style=none] (17) at (8.25, -0.5) {};
		\node [style=none] (18) at (7.25, -0.5) {};
		\node [style=bn] (19) at (7.25, 0.5) {};
		\node [style=none] (21) at (3, 1) {};
		\node [style=none] (22) at (3, 1.5) {$Y$};
		\node [style=none] (23) at (3, -0.5) {};
		\node [style=none] (24) at (5.25, -0.5) {$=$};
		\node [style=none] (25) at (-8.25, -1.75) {};
		\node [style=none] (26) at (-3.5, -1.75) {};
		\node [style=none] (27) at (3, -1.75) {};
		\node [style=none] (28) at (7.75, -1.75) {};
		\node [style=none] (29) at (-3.5, -0.5) {};
		\node [style=none] (30) at (7.75, -0.5) {};
		\node [style=none] (31) at (-8.25, -2.25) {$A$};
		\node [style=none] (32) at (-3.5, -2.25) {$A$};
		\node [style=none] (33) at (3, -2.25) {$A$};
		\node [style=none] (34) at (7.75, -2.25) {$A$};

		\draw (2.center) to (4.center);
		\draw (5.center) to (6);
		\draw (9.center) to (11.center);
		\draw (15.center) to (17.center);
		\draw (18.center) to (19);
		\draw (21.center) to (23.center);
		\draw (11.center) to (25.center);
		\draw (29.center) to (26.center);
		\draw (23.center) to (27.center);
		\draw (30.center) to (28.center);

		\node [style=morphism] (1) at (-3.5, -0.5) {$\;\, p \;\,$};
		\node [style=morphism] (8) at (-8.25, -0.5) {$p_X$};
		\node [style=morphism] (14) at (7.75, -0.5) {$\;\, p \;\,$};
		\node [style=morphism] (20) at (3, -0.5) {$p_Y$};
\end{tikzpicture}

This way, also the marginals will depend on the parameter $A$.


### Stochastic independence

A joint state $p$ on $X\otimes Y$ is said to exhibit **independence** of $X$ and $Y$ if and only if the following equation holds.

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (1) at (2.5, -0.25) {};
		\node [style=none] (2) at (4.5, -0.25) {};

		\node [style=none] (5) at (2, 1.25) {};
		\node [style=none] (6) at (5, 1.25) {};
		\node [style=none] (8) at (0, 0.5) {$=$};
		\node [style=none] (10) at (-3, 0) {};
		\node [style=none] (11) at (-2, 0) {};
		\node [style=none] (12) at (-2, 1.25) {};
		\node [style=none] (13) at (-3, 1.25) {};
		\node [style=none] (14) at (-3, 1.75) {$X$};
		\node [style=none] (15) at (-2, 1.75) {$Y$};
		\node [style=none] (16) at (2, 1.75) {$X$};
		\node [style=none] (17) at (5, 1.75) {$Y$};
		\node [style=none] (20) at (-2.5, 0) {};
		\node [style=none] (21) at (2, 0) {};
		\node [style=none] (22) at (3, 0) {};
		\node [style=none] (23) at (5, 0) {};
		\node [style=none] (24) at (4, 0) {};
		\node [style=bn] (25) at (3, 1) {};
		\node [style=bn] (26) at (4, 1) {};

		\draw (23.center) to (6.center);
		\draw (5.center) to (21.center);
		\draw (10.center) to (13.center);
		\draw (11.center) to (12.center);
		\draw (22.center) to (25);
		\draw (24.center) to (26);
        
                \node [style=morphism] (3) at (2.5, 0) {$\;\, p \;\,$};
		\node [style=morphism] (4) at (4.5, 0) {$\;\, p \;\,$};
                \node [style=morphism] (27) at (-2.5, 0) {$\;\, p \;\,$};
\end{tikzpicture}

In other words, $p$ denotes independendence if and only if it is the product of its marginals. 
In particular:

* In _FinStoch_, the joint distribution $p(x,y)$ denotes independence if it is in the form $p_X(x)\,p_Y(y)$ ;
* In _Stoch_, $p$ on $(X\times Y, \mathcal{A}\otimes\mathcal{B})$ denotes independence if for every $A\in\mathcal{A}$ and $B\in\mathcal{B}$, $p(A\times B) = p_X(A)\,p_Y(B)$;
* In _Set_, every joint state $(x,y)$ is trivially the product of its marginals $x$ and $y$: _no nontrivial correlation can happen when there is no randomness_ (see Proposition \ref{eqdet} below).

We can interpret the string diagram as follows: when $p$ denotes independence of $X$ and $Y$, then $p$ "splits" and leaves them disconnected. This denotes the fact that _no information flow from $X$ to $Y$ is possible_, i.e. observing the value of $X$ does not increase our knowledge over $Y$. 
For example, knowing the last name of a person does not tell us anything about their age (approximately).
Instead, in case of correlation (including nonlinear), knowing $X$ can tell us something about $Y$: for example, knowing the _height_ of a person can tell us something (not everything) about their age. In that case, the diagram remains connected. 
This correspondence between inferential information flow and topological connectedness of the string diagram is not a coincidence, it holds in general and is very deep: Markov categories have been proven to be [[probabilistic graphical models]] ([Fritz-Klingler'23](fritz_klingler23)).

More generally, a joint morphism $p:W\to X\otimes Y$ is said to exhibit **conditional independence** of $X$ and $Y$ **given** $W$ if and only if the following holds.

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]

		\node [style=bn] (0) at (3.5, -1.25) {};
		\node [style=none] (1) at (2.5, -0.25) {};
		\node [style=none] (2) at (4.5, -0.25) {};
		\node [style=none] (5) at (2, 1.25) {};
		\node [style=none] (6) at (5, 1.25) {};
		\node [style=none] (7) at (3.5, -2) {};
		\node [style=none] (8) at (0, 0) {$=$};
		\node [style=none] (9) at (-2.5, -2) {};
		\node [style=none] (10) at (-3, 0) {};
		\node [style=none] (11) at (-2, 0) {};
		\node [style=none] (12) at (-2, 1.25) {};
		\node [style=none] (13) at (-3, 1.25) {};
		\node [style=none] (14) at (-3, 1.75) {$X$};
		\node [style=none] (15) at (-2, 1.75) {$Y$};
		\node [style=none] (16) at (2, 1.75) {$X$};
		\node [style=none] (17) at (5, 1.75) {$Y$};
		\node [style=none] (18) at (3.5, -2.5) {$W$};
		\node [style=none] (19) at (-2.5, -2.5) {$W$};
        \node [style=none] (20) at (-2.5, 0) {};
		\node [style=none] (21) at (2, 0) {};
		\node [style=none] (22) at (3, 0) {};
		\node [style=none] (23) at (5, 0) {};
		\node [style=none] (24) at (4, 0) {};
		\node [style=bn] (25) at (3, 1) {};
		\node [style=bn] (26) at (4, 1) {};

		\draw (7.center) to (0);
		\draw (23.center) to (6.center);
		\draw (5.center) to (21.center);
		\draw (9.center) to (20);
		\draw (10.center) to (13.center);
		\draw (11.center) to (12.center);
		\draw (22.center) to (25);
		\draw (24.center) to (26);
		\draw [in=165, out=-90] (1.center) to (0);
		\draw [in=270, out=15] (0) to (2.center);

		\node [style=morphism] (3) at (2.5, 0) {$\;\, p \;\,$};
		\node [style=morphism] (4) at (4.5, 0) {$\;\, p \;\,$};
		\node [style=morphism] (27) at (-2.5, 0) {$\;\, p \;\,$};
\end{tikzpicture}

This can be interpreted as the fact that _$X$ and $Y$ are independent for each choice of fixed input $W$_. 
For example, 

* In *FinStoch*, this says exactly that $p$ is in the form 
$$
p(x,y|w) = p_X(x|w)\,p_Y(y|w) ,
$$
which recovers the usual conditional independence in the discrete case.

* In *Stoch*, this says exactly that for all measurable sets $A\subseteq X$ and $B\subseteq Y$,
$$
p(A\times B|w) = p_X(A|w)\,p_Y(B|w) ,
$$
which recovers the usual conditional independence in the measure-theoretic case.

* In *Set*, once again conditional independence always holds. 

We can interpret the string diagram as follows. In the case of conditional independence, it is not true anymore, in general, that $X$ and $Y$ are fully disconnected. However, they are connected *only through $W$*. That is, observing $X$ may tell us something about $Y$, but *none of that information is new to us if we already know $W$*.

For example, $X$ could be the number of mathematicians in a random city, and $Y$ could be annual consumption of coffee in the same city. 
We might observe a correlation between the two. 
However, both the amount of mathematicians and the consumption of coffee correlate with the population size of the city, $W$. It could be that *given $W$*, that is, *only looking at cities with similar population size*, we see no real correlation between the amount of coffee consumed and the number of mathematicians. 
In this case, 

* If we don't know the population size, knowing the coffee consumption may help us estimating the number of mathematicians;
* If we already know the population size, knowing the coffee consumption does not give us a more accurate estimate about the number of mathematicians. One says that the knowledge of $W$ _explains away_ the correlation between $X$ and $Y$. 

(This is just an example, real data about mathematicians and coffee may differ.)

Once again, the inferential information flow is perfectly reflected by the topological properties of the string diagram. 
This is one of the main assets of Markov categories: no matter how complex the model is, there always a perfect correspondence between the diagram topology and the interaction structure.

Let's now consider the case of *Set*: why is every morphism displaying conditional independence? The reason is that if $p:W\to X\times Y$ is a (deterministic) function, then knowing $W$ will already tell us everything about $Y$ (and $X$). Therefore there is no additional knowledge than observing $X$ can give us, if we know $W$.
(See also Proposition \ref{eqdet} below.)

Let's now make precise the idea of determinism.



### Deterministic morphisms

We have said that Markov categories are about describing morphisms which we can think of as "behaving randomly".
Let's make this precise, or rather, let's define precisely what it means to have *no randomness*.

A state $p:I\to X$ in a Markov category is called **deterministic** if and only if $\mathrm{copy}\circ p = p\otimes p$, i.e. if the following holds.

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (2) at (-3, -0.5) {};
		\node [style=none] (5) at (-3, -1.5) {};
		\node [style=bn] (7) at (-3, -0.5) {};
		\node [style=none] (8) at (-4, 0.5) {};
		\node [style=none] (9) at (-2, 0.5) {};
		\node [style=none] (10) at (-2, 0.5) {};
		\node [style=none] (11) at (-4, 1) {};
		\node [style=none] (12) at (-2, 1) {};
		\node [style=none] (14) at (-4, 1.5) {$X$};
		\node [style=none] (15) at (-2, 1.5) {$X$};
		\node [style=none] (16) at (-0.125, -0.25) {$=$};
		\node [style=none] (20) at (2, -1.5) {};
		\node [style=none] (21) at (4, 0.5) {};
		\node [style=none] (22) at (4, -1.5) {};
		\node [style=none] (23) at (2, 1) {};
		\node [style=none] (24) at (4, 1) {};
		\node [style=none] (25) at (2, 1.5) {$X$};
		\node [style=none] (26) at (4, 1.5) {$X$};

		\draw (5) to (2.center);
		\draw [in=270, out=165] (7) to (8.center);
		\draw [in=270, out=15] (7) to (9.center);
		\draw (11.center) to (8.center);
		\draw (12.center) to (10.center);
		\draw (23.center) to (20.center);
		\draw (24.center) to (22.center);

		\node [style=morphism] (28) at (-3, -1.5) {$p$};
		\node [style=morphism] (18) at (2, -1.5) {$p$};
		\node [style=morphism] (27) at (4, -1.5) {$p$};
\end{tikzpicture}

This reflect the traditional idea of probability theory of a [[zero-one measure]], a random variable which is independent of itself. In particular:

* In *FinStoch*, a distribution $p$ is deterministic if and only if for all $x,x'\in X$,
$$
p(x)\,\delta_{x,x'} = p(x)\,p(x') ,
$$
i.e. if and only if for all $x\in X$,
$$
p(x) = p(x)^2 .
$$
This means precisely that for all $x$, either $p(x)=0$ or $p(x)=1$, i.e. that the probability is concentrated on a single point. 

* In *Stoch*, a similar calculation shows that $p$ is deterministic if and only if for every measurable subset $A\subseteq X$, $p(A)=0$ or $p(A)=1$ ([[zero-one measure]]). That is, we are (almost) certain about which events happen and which do not. On well-behaved measurable spaces, such as [[standard Borel spaces]], this means exactly that $p$ is a [[Dirac measure|Dirac delta]], a measure concentrated at a single point.

* In *Set*, every state (i.e. single point) is deterministic.

More generally, a morphism $f:X\to Y$ in a Markov category is called **deterministic** if it commutes with the copy map,
$$
copy \circ f \;=\; (f\otimes f) \circ copy .
$$

In terms of string diagrams:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=none] (0) at (3, -1.75) {};
		\node [style=bn] (1) at (3, -0.75) {};
		\node [style=none] (2) at (2, 0.25) {};
		\node [style=none] (3) at (4, 0.25) {};
		\node [style=none] (4) at (4, 0.25) {};
		\node [style=none] (7) at (-3, -1.75) {};
		\node [style=bn] (8) at (-3, 0.25) {};
		\node [style=none] (9) at (-4, 1.25) {};
		\node [style=none] (10) at (-2, 1.25) {};
		\node [style=none] (11) at (-2, 1.25) {};
		\node [style=none] (12) at (2, 1.75) {};
		\node [style=none] (13) at (4, 1.75) {};
		\node [style=none] (14) at (-4, 1.75) {};
		\node [style=none] (15) at (-2, 1.75) {};
		\node [style=none] (16) at (-0.25, 0) {$=$};		
		\node [style=none] (18) at (2, 2.25) {$Y$};
		\node [style=none] (19) at (4, 2.25) {$Y$};
		\node [style=none] (20) at (-4, 2.25) {$Y$};
		\node [style=none] (21) at (-2, 2.25) {$Y$};
		\node [style=none] (22) at (3, -2.25) {$X$};
		\node [style=none] (23) at (-3, -2.25) {$X$};

		\draw (0.center) to (1);
		\draw [in=270, out=165] (1) to (2.center);
		\draw [in=270, out=15] (1) to (3.center);
		\draw (7.center) to (8);
		\draw [in=270, out=165] (8) to (9.center);
		\draw [in=270, out=15] (8) to (10.center);
		\draw (14.center) to (9.center);
		\draw (15.center) to (11.center);
		\draw (12.center) to (2.center);
		\draw (13.center) to (4.center);

        \node [style=morphism] (5) at (2, 0.75) {$f$};
		\node [style=morphism] (6) at (4, 0.75) {$f$};
		\node [style=morphism] (17) at (-3, -0.75) {$f$};
\end{tikzpicture}

This formalizes the idea of a deterministic transition, or function. In particular:

* In *FinStoch*, by means of a similar calculation as above, a stochastic matrix $k:X\to Y$ is deterministic if and only if for all $x,y\in X$, $k(y|x)=0$ or $k(y|x)=1$. This means precisely that $k$ is in the form $\delta_f$ for a set-theoretic function $f$ (see [[stochastic map#stochastic_maps_from_deterministic_functions|here]]).

* In *Stoch*, a Markov kernel $k:X\to Y$ is deterministic if and only if for every $x\in X$ and every measurable $B\subseteq Y$, $k(B|x)=0$ or $k(B|x)=1$ ([[zero-one kernels]]). On well-behaved measurable spaces, such as [[standard Borel spaces]], this means exactly that $k$ is in the form $\delta_f$ for a measurable function $f$ (see [[Markov kernel#kernels_from_deterministic_functions|here]]).

* In *Set*, every morphism is deterministic: for every $x\in X$ both side of the equations yield 
$$
\big(f(x),f(x)\big) = \big(f(x),f(x)\big) , 
$$
where on the left we have applied $f$ to $x$ and copied the result, while on the right we have copied $x$ and applied $f$ to both copies. 

Let's now see where the generic case differs from *Set*, and further motivate this definition. Suppose that $f$ is a "random" function between real numbers, which adds to the input the result of the roll of a die. Given a number $x$, we can roll a die, add the resulting value (say, $n$) to $x$, and then copy the result, to get $(x+n,x+n)$. Or, we could copy the value $x$, roll two dice (or roll the die twice), and add the two resulting values (say, $m$ and $n$) to the two copies of $x$, obtaining $(x+m,x+n)$. The two results are likely to differ, and in particular will follow different distributions: one perfectly correlated, one with conditional independence of the outputs given the inputs. 
One can take this as a _definition_ of randomness: it's a process that may give a different result if you do it twice. Or equivalently, that copying the information before or after the process has taken place gives different results.

A _deterministic_ morphism is one that does _not_ exhibit this behavior, i.e. that commutes with the copy map.

Deterministic morphisms are closed under composition. One usually denotes the [[wide subcategory]] of deterministic morphisms of a Markov category $C$ by $C_det$.

We have seen that in a Markov category, every morphism commutes with the discard map. Therefore, from the category-theoretic perspective, we can equivalently see deterministic morphisms exactly as the morphisms of comonoids. 

The following statement makes precise the idea, sketched in the previous sections, that *no inference is possible without randomness*:

\begin{proposition}\label{eqdet}
For a Markov category, the following conditions are equivalent.

1. Every morphism is deterministic;
2. The copy maps are natural;
3. The category is [[cartesian monoidal category|cartesian monoidal]];
4. Every morphism displays conditional independence of its outputs given its inputs.

\end{proposition}

Therefore, we can consider Markov categories as a generalization of cartesian monoidal categories to the case where "randomness is present".

(However, using Markov categories to study cartesian categories, while technically possible, usually yields trivial results, since all the correlations are trivial and no inference is possible.)




### Almost sure equality 

Another concept of probability and measure theory that Markov categories formalize is *almost sure equality*. 
The fact that certain propositions, in probability theory, are only true *up to a null set*, is sometimes considered an unavoidable but confusing technicality of the theory.
In Markov categories this concept is equally inevitable, but it acquires a precise conceptual meaning, and has very deep-reaching consequences.

Let $f,g:X\to Y$ be morphisms in a Markov category, and let $p$ be a state on $X$. We say that $f$ and $g$ are **$p$-almost surely equal** if and only if the following equation holds. 

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-3, -2) {};
		\node [style=bn] (1) at (-3, -1) {};
		\node [style=none] (2) at (3, -2) {};
		\node [style=bn] (3) at (3, -1) {};
		\node [style=none] (4) at (-4, 0) {};
		\node [style=none] (5) at (-2, 0) {};
		\node [style=none] (6) at (2, 0) {};
		\node [style=none] (7) at (4, 0) {};
		\node [style=none] (8) at (-4, 1.5) {};
		\node [style=none] (9) at (-2, 1.5) {};
		\node [style=none] (10) at (2, 1.5) {};
		\node [style=none] (11) at (4, 1.5) {};
		\node [style=none] (12) at (-4, 2) {$X$};
		\node [style=none] (13) at (-2, 2) {$Y$};
		\node [style=none] (14) at (2, 2) {$X$};
		\node [style=none] (15) at (4, 2) {$Y$};

        \node [style=none] (20) at (0.125, -0.25) {$=$};

		\draw (8.center) to (4.center);
		\draw (9.center) to (5.center);
		\draw (10.center) to (6.center);
		\draw (11.center) to (7.center);
		\draw (0.center) to (1);
		\draw (2.center) to (3);
		\draw [in=165, out=-90] (4.center) to (1);
		\draw [in=15, out=-90] (5.center) to (1);
		\draw [in=165, out=-90] (6.center) to (3);
		\draw [in=15, out=-90] (7.center) to (3);

		\node [style=morphism] (16) at (-2, 0.5) {$f$};
		\node [style=morphism] (17) at (4, 0.5) {$g$};
		\node [style=morphism] (18) at (-3, -2) {$p$};
		\node [style=morphism] (19) at (3, -2) {$p$};
\end{tikzpicture}

Similar definitions can be given even if $f$ and $p$ depend on additional parameters, see ([Fritz et al'23](#supports_idemp)) for the details.

In *Stoch* and *FinStoch*, this definition recovers the traditional notions of almost sure equality:

* In *FinStoch*, the equation reads 
$$
p(x)\,f(y|x) = p(x)\,g(y|x)
$$
for all $x\in X$ and $y\in Y$. This means exactly that for all $y\in Y$, and for all those $x\in X$ with $p(x) \ne 0$, $f(y|x)=g(y|x)$. That is, $f$ and $g$ agree on the support of $p$. 

* In *Stoch*, the equation reads
$$
\int_A f(B|x)\,p(d x) = \int_A g(B|x)\,p(d x)
$$
for all measurable $A\subseteq X$ and $B\subseteq Y$.
That is, for all $B$, the quantities $f(B|x)$ and $g(B|x)$ agree on a measure-one subset of $X$ (which may depend on $B$ in general). This recovers the [[Markov kernel#almost_sure_equality|notion of almost sure equality for Markov kernels]].

In the same vein, given a morphism $f:X\to Y$ and a state $p$ on $X$ we say that $f$ is **$p$-almost surely deterministic** if and only if the determinism equation for $f$ holds $p$-almost surely. In string diagrams:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=bn] (0) at (-4, -1.75) {};
		\node [style=bn] (1) at (-2.5, 1.25) {};
		\node [style=bn] (2) at (4, -1.75) {};
		\node [style=bn] (3) at (5.5, 0) {};
		\node [style=none] (4) at (-4, -2.75) {};
		\node [style=none] (5) at (4, -2.75) {};
		\node [style=none] (6) at (-5.5, -0.25) {};
		\node [style=none] (7) at (-2.5, -0.25) {};
		\node [style=none] (8) at (2.5, -0.25) {};
		\node [style=none] (9) at (5.5, -0.25) {};
		\node [style=none] (10) at (-5.5, 2.25) {};
		\node [style=none] (11) at (2.5, 2.25) {};
		\node [style=none] (12) at (-5.5, 2.75) {$X$};
		\node [style=none] (13) at (2.5, 2.75) {$X$};
		\node [style=none] (14) at (-1.5, 2.25) {};
		\node [style=none] (15) at (-3.5, 2.25) {};
		\node [style=none] (16) at (-3.5, 2.75) {$Y$};
		\node [style=none] (17) at (-1.5, 2.75) {$Y$};
		\node [style=none] (18) at (4.5, 1) {};
		\node [style=none] (19) at (6.5, 1) {};
		\node [style=none] (20) at (4.5, 2.25) {};
		\node [style=none] (21) at (6.5, 2.25) {};
		\node [style=none] (22) at (4.5, 2.75) {$Y$};
		\node [style=none] (23) at (6.5, 2.75) {$Y$};
		\node [style=none] (24) at (0.125, 0) {$=$};

		\draw (0) to (4.center);
		\draw (2) to (5.center);
		\draw [in=165, out=-90] (6.center) to (0);
		\draw [in=15, out=-90] (7.center) to (0);
		\draw [in=165, out=-90] (8.center) to (2);
		\draw [in=270, out=15] (2) to (9.center);
		\draw (10.center) to (6.center);
		\draw (11.center) to (8.center);
		\draw (1) to (7.center);
		\draw [in=165, out=-90] (15.center) to (1);
		\draw [in=270, out=15] (1) to (14.center);
		\draw [in=165, out=-90] (18.center) to (3);
		\draw (3) to (9.center);
		\draw [in=-90, out=15] (3) to (19.center);
		\draw (20.center) to (18.center);
		\draw (21.center) to (19.center);

		\node [style=morphism] (25) at (-4, -2.75) {$p$};
		\node [style=morphism] (26) at (4, -2.75) {$p$};
		\node [style=morphism] (27) at (-2.5, 0.25) {$f$};
		\node [style=morphism] (28) at (4.5, 1.25) {$f$};
		\node [style=morphism] (29) at (6.5, 1.25) {$f$};

\end{tikzpicture}

* In *FinStoch*, this says exactly that $f(y|x)$ is either zero or one for all $x$ such that $p(x) \ne 0$;

* In *Stoch*, this says that for all measurable $B\subseteq Y$, for $x$ on a measure-one set, $f(B|x)$ is either zero or one.


### Conditionals

One of the most powerful concepts in the theory of Markov categories is the idea of *conditioning*.
We saw, when talking about [stochastic independence](#stochastic_independence), that given a joint state on $X\times Y$,

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-3.5, -1) {};
		\node [style=none] (1) at (-3.5, 1) {};
		\node [style=none] (2) at (-2, 1) {};
		\node [style=none] (3) at (-2, -1) {};
		\node [style=none] (4) at (-3.5, 1.5) {$X$};
		\node [style=none] (5) at (-2, 1.5) {$Y$};

                \draw (1.center) to (0.center);
		\draw (2.center) to (3.center);
		
		\node [style=morphism] (6) at (-2.75, -1) {$\quad p \quad$};
\end{tikzpicture}
one can try, from observing $X$, to *infer* something about $Y$. This idea of information flowing from $X$ to $Y$, often, can be modelled as a *morphism* $X\to Y$, in general not deterministic, since $X$ may not determine $Y$ completely. Let's define this precisely.

Let $p$ be a joint state on $X\otimes Y$. A **conditional distribution** on $Y$ **given** $X$ is a morphism $p|_X:X\to Y$ such that the following equation holds:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-3.5, -1) {};
		\node [style=none] (1) at (-3.5, 1) {};
		\node [style=none] (2) at (-2, 1) {};
		\node [style=none] (3) at (-2, -1) {};
		\node [style=none] (4) at (-3.5, 1.5) {$X$};
		\node [style=none] (5) at (-2, 1.5) {$Y$};
		\node [style=none] (7) at (0.125, 0) {$=$};
		\node [style=none] (8) at (3, -2) {};
		\node [style=none] (11) at (4.5, -2) {};
		\node [style=none] (12) at (2, 2.5) {$X$};
		\node [style=none] (13) at (4, 2.5) {$Y$};
		\node [style=bn] (15) at (3, -0.5) {};
		\node [style=bn] (16) at (4.5, -1) {};
		\node [style=none] (17) at (2, 0.5) {};
		\node [style=none] (18) at (4, 0.5) {};
		\node [style=none] (19) at (4, 2) {};
		\node [style=none] (20) at (2, 2) {};

		\draw (1.center) to (0.center);
		\draw (2.center) to (3.center);
		\draw (16) to (11.center);
		\draw (15) to (8.center);
		\draw [in=15, out=-90] (18.center) to (15);
		\draw [in=165, out=-90] (17.center) to (15);
		\draw (20.center) to (17.center);
		\draw (19.center) to (18.center);

		\node [style=morphism] (6) at (-2.75, -1) {$\quad p \quad$};
		\node [style=morphism] (14) at (3.75, -2) {$\quad p \quad$};
		\node [style=morphism] (21) at (4, 1) {$p|_X$};
\end{tikzpicture}

* In *FinStoch*, this means a [[stochastic map]] of entries $p|_X(y|x)$ such that for all $x\in X$ and $y\in Y$,
$$
p(x,y) = p_X(x)\,p|_X(y|x) .
$$
(Note the difference between the *marginal*, $p_X$, and the *conditional*, $p|_X$.)
This is the usual notion of conditional distribution in the discrete case, usually obtained by 
$$
p|_X(y|x) = \frac{p(x,y)}{p(x)}
$$
when $p(x)\ne 0$, and arbitrary otherwise.

* In *Stoch*, this means a [[Markov kernel]] $p|_X:X\to Y$ such that for all measurable $A\subseteq X$ and $B\subseteq Y$,
$$
p(A\otimes B) = \int_A p|_X(B|x)\,p_X(d x) .
$$
This is known in probability theory as a [[Markov kernel#regular_conditional_distributions|regular conditional distribution]].

Note that, if a conditional distribution exists, it is unique only up to $p_X$-almost sure equality. Moreover,

* In *FinStoch* all conditional distributions exist;
* In *Stoch*, they may fail to exist in general, but they always exist for [[standard Borel spaces]], i.e. in the subcategory [[BorelStoch]]. More on that in [[Markov kernel#regular_conditional_distributions|regular conditional distribution]].

It is helpful to think of a conditional distribution as of turning the output $X$ into an input. In terms of string diagram, it is sometimes helpful to represent this as follows, 

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-2, -1) {};
		\node [style=none] (1) at (-2, 2.5) {};
		\node [style=none] (2) at (-2, -1.5) {$X$};
		\node [style=none] (3) at (-2, 3) {$Y$};
		\node [style=none] (4) at (0.125, 0.75) {$=$};
		\node [style=none] (5) at (3.5, 1) {};
		\node [style=none] (6) at (5, 2.5) {};
		\node [style=none] (7) at (3.5, 0.75) {};
		\node [style=none] (8) at (5, 0.75) {};
		\node [style=none] (9) at (5, 3) {$Y$};
		\node [style=none] (10) at (2.25, 1) {};
		\node [style=none] (11) at (2.25, -1) {};
		\node [style=none] (12) at (2.25, -1.5) {$X$};
		\node [style=none] (15) at (1.75, 1.75) {};
		\node [style=none] (16) at (1.75, -0.25) {};
		\node [style=none] (17) at (5.75, -0.25) {};
		\node [style=none] (18) at (5.75, 1.75) {};

		\draw (1.center) to (0.center);
		\draw (5.center) to (7.center);
		\draw (6.center) to (8.center);
		\draw [bend left=90, looseness=1.25] (10.center) to (5.center);
		\draw (10.center) to (11.center);
		\draw [dashed] (15.center) to (18.center);
		\draw [dashed] (18.center) to (17.center);
		\draw [dashed] (17.center) to (16.center);
		\draw [dashed] (16.center) to (15.center);

		\node [style=morphism] (13) at (-2, 0.75) {$p|_X$};
		\node [style=morphism] (14) at (4.25, 0.75) {$\quad p \quad$};
\end{tikzpicture}

which says that "in the inside of $p|_X$, a wire has been bent to turn an output into an input".

A particularly important conditional distribution is given by [[Bayesian inverses]].

Let $p$ be a state on $X$ and let $f:X\to Y$ be a morphisms. A **[[Bayesian inverse]]** of $f$ with respect to $p$ is a morphism $f^\dagger:Y\to X$ such that the following equation holds, where $q=f\circ p$.

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=bn] (0) at (-3, -1) {};
		\node [style=bn] (1) at (3, -1) {};
		\node [style=none] (2) at (-3, -2) {};
		\node [style=none] (3) at (3, -2) {};
		\node [style=none] (4) at (-4, 0) {};
		\node [style=none] (5) at (-2, 0) {};
		\node [style=none] (6) at (2, 0) {};
		\node [style=none] (7) at (4, 0) {};
		\node [style=none] (8) at (-4, 1.5) {};
		\node [style=none] (9) at (-2, 1.5) {};
		\node [style=none] (10) at (2, 1.5) {};
		\node [style=none] (11) at (4, 1.5) {};
		\node [style=none] (16) at (-4, 2) {$X$};
		\node [style=none] (17) at (-2, 2) {$Y$};
		\node [style=none] (18) at (2, 2) {$X$};
		\node [style=none] (19) at (4, 2) {$Y$};
		\node [style=none] (20) at (0, -0.25) {$=$};

		\draw [in=165, out=-90] (4.center) to (0);
		\draw [in=15, out=-90] (5.center) to (0);
		\draw (0) to (2.center);
		\draw [in=165, out=-90] (6.center) to (1);
		\draw [in=15, out=-90] (7.center) to (1);
		\draw (1) to (3.center);
		\draw (8.center) to (4.center);
		\draw (9.center) to (5.center);
		\draw (10.center) to (6.center);
		\draw (11.center) to (7.center);

		\node [style=morphism] (12) at (-4, 0.25) {$f^\dagger_p$};
		\node [style=morphism] (13) at (4, 0.25) {$f$};
		\node [style=morphism] (14) at (-3, -2) {$q$};
		\node [style=morphism] (15) at (3, -2) {$p$};
\end{tikzpicture}

Note that this is the same as a conditional given $Y$ for the joint on the right-hand side. 
The equation can be seen as a version of [[Bayes' formula]]:

* In *FinStoch*, it says that 
$$
q(y) \,f^\dagger_p(x|y) = p(x) \,f(y|x) ,
$$
which is in the usual form 
$$
P(y) \, P(x|y) = P(x) \, P(y|x) ,
$$
which recovers the usual [[Bayesian inversion#discrete_case|Bayesian version for stochastic maps]].

* In *Stoch*, similarly, it says that for all measurable $A\subseteq X$ and $B\subseteq Y$,
$$
\int_B f^\dagger_p(A|y) \, q(d y) = \int_A f(B|x)\,p(d x) .
$$
This recovers the [[Bayesian inversion#measuretheoretic_case|Bayesian inversion of Markov kernels]].

Once again, Bayesian inversions exist for all [[standard Borel spaces]], and in general, if they exist, they are unique $q$-almost surely.

To conclude this section, let's give the most general definition of conditional. 
Let $h:A\to X\otimes Y$ be a joint morphism. A **conditional** of $h$ **given** $X$ is a morphism $h|_X:X\otimes A\to Y$ such that the following equation holds.

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-3.5, 0) {};
		\node [style=none] (1) at (-2, 0) {};
		\node [style=none] (2) at (-3.5, 1.5) {};
		\node [style=none] (3) at (-2, 1.5) {};
		\node [style=none] (4) at (-2.75, 0) {};
		\node [style=none] (5) at (-2.75, 0) {};
		\node [style=none] (6) at (-2.75, -1.5) {};
		\node [style=none] (7) at (-2.75, -2) {$A$};
		\node [style=none] (8) at (-3.5, 2) {$X$};
		\node [style=none] (9) at (-2, 2) {$Y$};
		\node [style=none] (10) at (0.125, 0) {$=$};
		\node [style=none] (11) at (2.5, -0.5) {};
		\node [style=none] (12) at (4, -0.5) {};
		\node [style=none] (17) at (3.25, -0.75) {};
		\node [style=none] (18) at (4.25, -3.25) {$A$};
		\node [style=none] (19) at (1.5, 3.25) {$X$};
		\node [style=none] (20) at (4.25, 3.25) {$Y$};
		\node [style=bn] (21) at (2.5, 0.5) {};
		\node [style=bn] (22) at (4, 0.5) {};
		\node [style=none] (23) at (1.5, 1.5) {};
		\node [style=none] (24) at (3.5, 1.5) {};
		\node [style=bn] (25) at (4.25, -1.75) {};
		\node [style=none] (26) at (5.25, -0.75) {};
		\node [style=none] (27) at (4.25, -2.75) {};
		\node [style=none] (28) at (5, 1.5) {};
		\node [style=none] (29) at (4.25, 1.5) {};
		\node [style=none] (30) at (4.25, 2.75) {};
		\node [style=none] (31) at (1.5, 2.75) {};

		\draw (0.center) to (2.center);
		\draw (3.center) to (1.center);
		\draw (5.center) to (6.center);
		\draw (21) to (11.center);
		\draw (12.center) to (22);
		\draw [in=165, out=-90] (23.center) to (21);
		\draw [in=15, out=-90] (24.center) to (21);
		\draw [in=15, out=-90] (26.center) to (25);
		\draw [in=165, out=-90] (17.center) to (25);
		\draw (25) to (27.center);
		\draw [in=90, out=-90] (28.center) to (26.center);
		\draw (31.center) to (23.center);
		\draw (30.center) to (29.center);

		\node [style=morphism] (32) at (-2.75, 0) {$\quad h \quad$};
		\node [style=morphism] (33) at (3.25, -0.5) {$\quad h \quad$};
		\node [style=morphism] (34) at (4.25, 1.75) {$\;\, h|_X \;\,$};
\end{tikzpicture}

A Markov category is said to **have conditionals** if every conditional in the form above exists. 

Both *FinStoch* and *BorelStoch* have conditionals.


## Further structures and properties


### Representable Markov categories

[As we explained above](#kleisli_categories_of_probability_monads), a [[probability monad]] often gives rise to a Markov category. 

Conversely, consider a Markov category $C$. 

* The category $C_det$ of deterministic morphisms has no randomness; 
* There may be have a [[monad]] on $C_\det$ which encodes randomness (see [[probability monad]]);
* The Markov category $C$ may be the [[Kleisli category]] of this monad.

Let's make this precise in terms of a [[universal property]].

Let $X$ be an object in a Markov category $C$. A **distribution object for $X$** is an object, which we denote by $P X$, together with a bijection
$$
C_det(A,P X) \cong C(A,X)
$$
for all objects $A$, natural in $A$ against deterministic morphisms.

The object $P X$ has the interpretation of being a *space of probability measures over $X$*. Setting $A=I$ in the definition, we see in particular that the deterministic states (or "points") of $P X$ are exactly the (generic, random) states on $X$. 
For [[Stoch]], this says that the points of $P X$ should be exactly the probability measures on $X$. 
Indeed, in [[Stoch]] every object has a distribution object, given by the [[Giry monad]]. 

More generally:

\begin{theorem}
For a Markov category $C$, the following conditions are equivalent. 

1. Every object of $C$ has a distribution object.
2. The inclusion functor $C_det\to C$ has a right adjoint (which we denote by $P$). 
3. $C$ is isomorphic to the Kleisli category of a commutative affine monad on $C_det$.

\end{theorem}

A Markov category $C$ is called **representable** if any of the conditions of the theorem above holds.

The category *FinStoch* is not representable, since the objects are finite sets, and the set of distribution $P X$ over a finite set $X$ (with more than two elements) would be infinite. 
It is however a subcategory of the Kleisli category of the [[distribution monad]], of *all sets* and all [[stochastic maps]] between them. 

By means of the [[Yoneda lemma]], we can equivalently define a distribution object as an object $P X$ together with a distinguished morphism $P X\to X$, which we denote by "$samp$" and call the [[sampling map]], such that the assignment
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
C_\mathrm{det}(A,PX) \ar{r} & C(A,X) \\
f \ar[mapsto]{r} & \mathrm{samp}\circ f
\end{tikzcd}
is a bijection for all objects $A$.

The map $samp$ can be thought of as being the *universal* random map, in the sense that by the bijection above, every Kleisli morphism can be seen as the composition of $samp$ with a deterministic map.

From the point of view of probability theory, in [[Stoch]], we can view this map $P X\to X$ as taking a distribution $p\in P X$, and returning a random point of $X$ distributed according to $p$. In other words, it is [[sampling map|sampling]] from $p$.

This also corresponds to the idea of sampling in [[probabilistic programming]], (see [[monad (in computer science)]]).


### Kolmogorov products

Kolmogorov products are a way to equip a Markov category with an [[infinitary tensor product]].
The idea can be seen as an abstraction of the [[Kolmogorov extension theorem]] for [[probability measures]].

Let $C$ be a Markov category, and let $(X_j)_{j\in J}$ be a family of objects. A **Kolmogorov product** of them is an [[infinite tensor product]] 
$$
X_J=\bigotimes_{j\in J} X_j
$$
such that all finite projections (marginalizations) $X_J\to X_F$, with $F\subseteq J$ finite, are deterministic morphisms.

Using the universal property of limits, this says that a joint distribution on $X_J$ is equivalently given by a family of joint distributions on all finite subsets of $J$, compatible with the restrictions.

* *BorelStoch* has all countable Kolmogorov products by means of the [[Kolmogorov extension theorem]].

* In *Set*, and in every [[cartesian monoidal category]], Kolmogorov products coincide with ordinary products (when they exist for those cardinality). 

Because of this, a Kolmogorov product on $C$ restricts to a [[cartesian product]] in the category $C_det$ of deterministic morphisms.


### Positivity and causality

Positivity and causality are two additional axioms for Markov categories, introduced in [Fritz'20](#fritzmarkov), which hold in categories of kernels such as [[Stoch]].

A Markov category is called **positive** if and only if whenever two morphisms $f:X\to Y$ and $g:Y\to Z$ are such that $g\circ f:X\to Z$ is deterministic, then the following holds,

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-3, -2) {};
		\node [style=bn] (1) at (-3, 0) {};
		\node [style=bn] (2) at (3.25, -1) {};
		\node [style=none] (3) at (3.25, -2) {};
		\node [style=none] (4) at (3.25, -2) {};
		\node [style=none] (5) at (-4, 1) {};
		\node [style=none] (6) at (-2, 1) {};
		\node [style=none] (7) at (2.25, 0) {};
		\node [style=none] (8) at (4.25, 0) {};
		\node [style=none] (9) at (3.25, -2.5) {$X$};
		\node [style=none] (10) at (-3, -2.5) {$X$};
		\node [style=none] (11) at (-4, 2.5) {};
		\node [style=none] (12) at (-2, 2.5) {};
		\node [style=none] (13) at (2.25, 2.5) {};
		\node [style=none] (14) at (4.25, 2.5) {};
		\node [style=none] (15) at (0, 0) {$=$};
		\node [style=none] (16) at (-4, 3) {$Y$};
		\node [style=none] (17) at (-2, 3) {$Z$};
		\node [style=none] (18) at (2.25, 3) {$Y$};
		\node [style=none] (19) at (4.25, 3) {$Z$};
		
		\draw (1) to (0.center);
		\draw (4.center) to (2);
		\draw [in=165, out=-90] (5.center) to (1);
		\draw [in=270, out=15] (1) to (6.center);
		\draw [in=165, out=-90] (7.center) to (2);
		\draw [in=270, out=15] (2) to (8.center);
		\draw (11.center) to (5.center);
		\draw (12.center) to (6.center);
		\draw (13.center) to (7.center);
		\draw (14.center) to (8.center);

        \node [style=morphism] (20) at (-3, -1) {$f$};
		\node [style=morphism] (21) at (-2, 1.25) {$g$};
		\node [style=morphism] (22) at (2.25, 1) {$f$};
		\node [style=morphism] (23) at (4.25, 0.25) {$f$};
		\node [style=morphism] (24) at (4.25, 1.5) {$g$};
\end{tikzpicture}

i.e. the resulting joint morphism on the left makes $Y$ and $Z$ conditionally independent given $X$.

Equivalently, a Markov category is positive if and only if  for every joint morphism $h:A\to X\otimes Y$ such that one of its marginals is deterministic, $h$ exhibits conditional independents of its outputs given its input.

In a positive Markov category, every isomorphism is deterministic ([Fritz'20](#fritzmarkov), Remark 11.28).


A Markov category is called **causal** if, whenever the following equation holds,

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-1.75, 2.5) {};
		\node [style=none] (1) at (0, 0) {$=$};
		\node [style=none] (2) at (-2.5, -3) {$A$};
		\node [style=none] (4) at (-3.25, 2.5) {};
		\node [style=none] (5) at (-1.75, 3) {$X$};
		\node [style=none] (6) at (-2.5, -2.5) {};
		\node [style=none] (7) at (-3.25, 1.75) {};
		\node [style=none] (8) at (-1.75, 1.75) {};
		\node [style=bn] (9) at (-2.5, 0.75) {};
		\node [style=none] (12) at (-3.25, 3) {$Y$};
		\node [style=none] (13) at (2.5, -2.5) {};
		\node [style=none] (14) at (2.5, -3) {$A$};
		\node [style=none] (15) at (3.25, 2.5) {};
		\node [style=none] (16) at (3.25, 1.75) {};
		\node [style=none] (17) at (1.75, 1.75) {};
		\node [style=bn] (18) at (2.5, 0.75) {};
		\node [style=none] (19) at (1.75, 2.5) {};
		\node [style=none] (22) at (1.75, 3) {$Y$};
		\node [style=none] (24) at (3.25, 3) {$X$};

		\draw [style=morphism] (6.center) to (9);
		\draw [style=morphism, in=-90, out=15] (9) to (8.center);
		\draw [style=morphism, in=-90, out=165] (9) to (7.center);
		\draw [style=morphism] (8.center) to (0.center);
		\draw [style=morphism] (7.center) to (4.center);
		\draw [style=morphism] (16.center) to (15.center);
		\draw [style=morphism, in=-90, out=165] (18) to (17.center);
		\draw [style=morphism, in=-90, out=15] (18) to (16.center);
		\draw [style=morphism] (17.center) to (19.center);
		\draw [style=morphism] (13.center) to (18);

		\node [style=morphism] (3) at (-2.5, -1.5) {$f$};
		\node [style=morphism] (10) at (-2.5, -0.25) {$g$};
		\node [style=morphism] (11) at (-3.25, 1.75) {$h_1$};
		\node [style=morphism] (20) at (2.5, -0.25) {$g$};
		\node [style=morphism] (21) at (1.75, 1.75) {$h_2$};
		\node [style=morphism] (23) at (2.5, -1.5) {$f$};
\end{tikzpicture}

then the following, stronger condition also holds.

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-3, 3) {};
		\node [style=none] (1) at (0, 0) {$=$};
		\node [style=none] (2) at (-3.75, -3.5) {$A$};
		\node [style=none] (4) at (-4.5, 3) {};
		\node [style=none] (5) at (-3, 3.5) {$X$};
		\node [style=none] (7) at (-4.5, 2) {};
		\node [style=none] (8) at (-3, 2) {};
		\node [style=bn] (9) at (-3.75, 1) {};
		\node [style=none] (12) at (-4.5, 3.5) {$Y$};
		\node [style=none] (13) at (-3.75, -3) {};
		\node [style=bn] (15) at (-3.75, -1) {};
		\node [style=none] (16) at (-2, 0.5) {};
		\node [style=none] (18) at (-2, 3) {};
		\node [style=none] (19) at (-2, 3.5) {$W$};
		\node [style=none] (20) at (3.5, 3) {};
		\node [style=none] (21) at (2.75, -3.5) {$A$};
		\node [style=none] (23) at (2, 3) {};
		\node [style=none] (24) at (3.5, 3.5) {$X$};
		\node [style=none] (25) at (2, 2) {};
		\node [style=none] (26) at (3.5, 2) {};
		\node [style=bn] (27) at (2.75, 1) {};
		\node [style=none] (30) at (2, 3.5) {$Y$};
		\node [style=none] (31) at (2.75, -3) {};
		\node [style=bn] (32) at (2.75, -1) {};
		\node [style=none] (33) at (4.5, 0.5) {};
		\node [style=none] (34) at (4.5, 3) {};
		\node [style=none] (35) at (4.5, 3.5) {$W$};
		\node [style=none] (10) at (-3.75, 0) {};
		\node [style=none] (28) at (2.75, 0) {};
	
		\draw [style=morphism, in=-90, out=15] (9) to (8.center);
		\draw [style=morphism, in=-90, out=165] (9) to (7.center);
		\draw [style=morphism] (8.center) to (0.center);
		\draw [style=morphism] (7.center) to (4.center);
		\draw [style=morphism] (13.center) to (15);
		\draw [style=morphism, in=-90, out=0] (15) to (16.center);
		\draw (16.center) to (18.center);
		\draw (15) to (10);
		\draw (10) to (9);
		\draw [style=morphism, in=-90, out=15] (27) to (26.center);
		\draw [style=morphism, in=-90, out=165] (27) to (25.center);
		\draw [style=morphism] (26.center) to (20.center);
		\draw [style=morphism] (25.center) to (23.center);
		\draw [style=morphism] (31.center) to (32);
		\draw [style=morphism, in=-90, out=0] (32) to (33.center);
		\draw (33.center) to (34.center);
		\draw (32) to (28);
		\draw (28) to (27);
	
		\node [style=morphism] (3) at (-3.75, -2) {$f$};
		\node [style=morphism] (40) at (-3.75, 0) {$g$};
		\node [style=morphism] (11) at (-4.5, 2) {$h_1$};
		\node [style=morphism] (22) at (2.75, -2) {$f$};
		\node [style=morphism] (48) at (2.75, 0) {$g$};
		\node [style=morphism] (29) at (2, 2) {$h_2$};
\end{tikzpicture}

\begin{theorem}
Every Markov category with all conditionals is causal ([Fritz'20](#fritzmarkov), Proposition 11.34), and every causal Markov category is positive ([Fritz et al'23](#dilations), Theorem 2.24). Both converses are false.
\end{theorem}

The category [[Stoch]] is causal (but it doesn't have all conditionals).


### The _ProbStoch_ construction

The _ProbStoch_ construction on a Markov category formalizes the idea of a category of [[probability spaces]]. Morphisms are identified when they agree almost surely, so that universal properties in that category tend to encode universal properties that hold "up to probability zero".
Moreover, if conditionals exist, the _ProbStoch_ construction gives an abstraction of the [[category of couplings]].

Let $C$ be a causal Markov category. The category **$ProbStoch(C)$** is defined as follows.

* Its [[objects]] are pairs $(X,p)$ where $X$ is an object of $C$, and $p:I\to X$ is a state on $X$. 
* Its [[morphisms]] $(X,p)\to(Y,q)$ are equivalence classes of morphisms $f:X\to Y$ of $C$ under $p$-almost sure equality, and such that $f\circ p=q$. 

The causality condition is required in order for composition to be well defined on the equivalence classes.

In general $ProbStoch(C)$ is not a Markov category, but only a [[semicartesian monoidal category]].

\begin{proposition}
If a Markov category $C$ has all conditionals, $ProbStoch(C)$ is a [[dagger category]], with the daggers given by [[Bayesian inversion|Bayesian inverses]]. 
\end{proposition}

For example, [[BorelStoch]] has all conditionals, and $ProbStoch(BorelStoch)$ is the category [[Krn]].


## Quantum versions 

(For now, see the references.)


## History
 {#History}

In the history of Markov categories, and of [[categorical probability]] in general, it happened very often that a number of independent researchers developed similar ideas unaware of each other's work.

The first study of a category of [[Markov kernels]] (here called [[Stoch]]) seems to be due to [[Lawvere]], and recorded in unpublished notes ([Lawvere'62](#Lawvere62), see also the explanation by Lawvere himself in [this video](https://www.youtube.com/watch?v=BhKaHAY8Ec8&t=3621s), time 1:00:21.)
The same category was studied independently by Chentsov ([Chentsov'65](#Chentsov65)), who wrote in Russian. It is likely that Lawvere and Chentsov remained unaware of each other's work for several decades. 



Giry ([Giry'82](#giry82)) first described [[Stoch]] as the Kleisli category of the [[Giry monad|monad which brings her name]].
Shortly after, computer scientists such as [[Eugenio Moggi|Moggi]] and [[Gordon Plotkin|Plotkin]] started considering monads in the context of effectful programming ([Moggi'89](#moggi89)), with probabilistic computation as a special case ([Jones-Plotkin'89](#jones_plotkin89)). (More details in [[monad (in computer science)]].)
This is also the time when a number of [[probability monads]] were introduced, see there for more. 

The first definition of a _garbage-share_ (a.k.a. _copy-discard_) category seems to be due to [[Fabio Gadducci|Gadducci]] ([Gadducci'96](#gadducci96)), who in his PhD thesis introduced such a structure (for strict monoidal categories), with in mind applications to formal languages (in particular graph term rewriting). In subsequent papers together with Corradini some further properties of these construction were studied, including higher-categorical ones ([Corradini-Gadducci'97](#corradini_gadducci97), [Corradini-Gadducci'99a](#corradini_gadducci99a), [Corradini-Gadducci'99b](#corradini_gadducci99b), [Corradini-Gadducci'02](#corradini_gadducci02)).

The first mention of Markov and CD-categories used for the purpose of probability seems to have first appeared in the work of Golubtsov ([Golubtsov'99](#golubtsov99)), who named the structure "category of information converters" or "information transformers", likely unaware of Gadducci's work, and first writing in Russian. In subsequent work ([Golubtsov'02](#golubtsov02), [Golubtsov-Mosaliuk'02](#golubtsov_mosaliuk02), [Golubtsov'04](#golubtsov04)) these structures were connected to [[Kleisli categories]], introducing what now we call a [representable Markov category](#representable_markov_categories).

In parallel, and seemingly unaware of Golubtsov's work, [[Bob Coecke|Coecke]] and Spekkens developed a string-diagrammatic framework for Bayesian inference, for the purpose of generalizing these concept from classical to quantum ([Coecke-Spekkens'11](#coecke_spekkens11)). The resulting framework is somewhat different from the one of Markov categories, but very similar in aims and philosophy.

Once again seemingly unaware of Golubtsov's work, [[Brendan Fong|Fong]] studied categorical structures to model Bayesian networks in his master's thesis ([Fong'12](#fong12)), in particular by means of equipping the objects of a category with comonoid structures.

Finally, the current form of Markov and copy-discard categories, which is also the one presented in this article, was developed in the works of Cho and [[Bart Jacobs|Jacobs]] ([Cho-Jacobs'19](#cd_categories)) and of [[Tobias Fritz|Fritz]] ([Fritz'20](#fritzmarkov)).



## Detailed list
 {#DetailedList}

[[!include table of Markov categories]]



## See also

* [[probability theory]], [[categorical probability]]

* [[Markov kernel]], [[stochastic map]], [[Stoch]]

* [[conditional independence]], [[joint and marginal probability]]

* [[probability monad]], [[affine monad]], [[commutative monad]]

* [[doctrine]], [[supply in a monoidal category]]



## References


### Main sources

The main definitions and results in this article can be found in

* {#cd_categories} [[Kenta Cho]], [[Bart Jacobs]]: _Disintegration and Bayesian Inversion via String Diagrams_, Mathematical Structures of Computer Science **29** (2019) &lbrack;[arXiv:1709.00322](https://arxiv.org/abs/1709.00322), [doi:10.1017/S0960129518000488](https://doi.org/10.1017/S0960129518000488)&rbrack;
  > (where Markov categories are called *affine CD categories*)

* {#fritzmarkov} [[Tobias Fritz]]: _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, Advances of Mathematics **370** (2020) &lbrack;[arXiv:1908.07021](http://arxiv.org/abs/1908.07021), [doi:10.1016/j.aim.2020.107239](https://doi.org/10.1016/j.aim.2020.107239)&rbrack;


The graphical model (separation and d-separation) aspects of conditional independence for Markov categories have been studied in

* {#d-sep} [[Tobias Fritz]] and Andreas Klingler, _The d-separation criterion in Categorical Probability_, Journal of Machine Learning Research 24(46), 2023. ([arXiv](https://arxiv.org/abs/2207.05740))

Representable Markov categories have been studied in 

* [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], Eigil Fjeldgren Rischel, _Representable Markov categories and comparison of statistical experiments in categorical probability_, Theoretical Computer Science 961, 2023. ([arXiv:2010.07416](https://arxiv.org/abs/2010.07416))

as well as in the following work, together with an in-depth treatment of positivity and causality:

* {#dilations} [[Tobias Fritz]], Tomáš Gonda, Nicholas Gauguin Houghton-Larsen, [[Paolo Perrone]] and Dario Stein, _Dilations and information flow axioms in categorical probability_. Mathematical Structures in Computer Science, 2023. ([arXiv:2211.02507](https://arxiv.org/abs/2211.02507)).

Kolmogorov products have been studied in 

* {#fritzrischel} [[Tobias Fritz]] and Eigil Fjeldgren Rischel, _Infinite products and zero-one laws in categorical probability_, Compositionality 2(3) 2020. ([arXiv:1912.02769](http://arxiv.org/abs/1912.02769))


### Introductory material

Some of the introductory content on this page is taken from the following reference:

* {#markov_entropy} [[Paolo Perrone]], _Markov Categories and Entropy_, IEEE Transactions on Information Theory 70(3), 2024. ([arXiv](https://arxiv.org/abs/2212.11719))

Video lectures suitable for beginners:

* [[Paolo Perrone]], _Tutorial on Markov categories_, Applied Category Theory 2023, University of Maryland, USA. ([YouTube](https://www.youtube.com/watch?v=9U5w3EMHio8))

* [[Paolo Perrone]], _Universal properties in probability theory_, Category Theory 2023, Louvain-la-Neuve, Belgium. ([YouTube](https://www.youtube.com/watch?v=gmSlbgmLyVQ))

* (in Spanish) [[Paolo Perrone]], _Categorical Probability and Information Theory_, Universidad Carlos III Madrid, Spain ([video here](http://www.q-math.es/Videos/PaoloPerrone2023.mp4))

* Eigil Fjeldgren Rischel, _Introduction to Markov categories_, Categorical Probability and Statistics Workshop, 2020. ([YouTube](https://www.youtube.com/watch?v=534f-9Qx2Lg))

Slides from talks:

* [[Tobias Fritz]], _Categorical Probability and the de Finetti theorem_, New York City Category Seminar, 2021. ([pdf](http://tobiasfritz.science/2021/markov_cats_nyc.pdf))

* [[Tobias Fritz]], _Probability and Statistics as a Theory of Information Flow_, 2020 ([pdf](http://tobiasfritz.science/2020/markov_cats.pdf))

* [[Tobias Fritz]], _A synthetic introduction to probability and statistics_, 2019 ([pdf](http://tobiasfritz.science/2019/markov_cats.pdf))




### Historical references

> (see *[History](#History)*)

* {#Lawvere62} [[W. Lawvere]], _The category of probabilistic mappings_, ms. 12 pages, 1962 
([[lawvereprobability1962.pdf:file]])

* {#Chentsov65} N. N. Chentsov, _The categories of mathematical statistics_, Dokl. Akad. SSSR 164, 1965.

* {#giry82} Michèle Giry, _A categorical approach to probability theory_, Categorical aspects of topology and analysis, Lecture notes in Mathematics 915, Springer, 1982.

* {#moggi89} [[Eugenio Moggi]], *Computational lambda-calculus and monads*, Proceedings of LICS, 1989. ([doi](https://doi.org/10.1109/LICS.1989.39155))

* {#jones_plotkin89} Claire Jones and [[Gordon Plotkin]], _A probabilistic powerdomain of evaluations_, Proceedings of LICS, 1989. ([doi](https://doi.org/10.1109/LICS.1989.39173))

* {#gadducci96} [[Fabio Gadducci]], _On the Algebraic Approach to Concurrent Term Rewriting_, PhD thesis, University of Pisa, 1996. ([available here](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.57.5651))

* {#corradini_gadducci97} Andrea Corradini and [[Fabio Gadducci]], _A 2-categorical presentation of term graph rewriting_. In CTCS, LNCS 1290, 1997.

* {#corradini_gadducci99a} Andrea Corradini and [[Fabio Gadducci]], _An algebraic presentation of term graphs, via gs-monoidal categories_, Applied Categorical Structures 7(4), 1999

* {#corradini_gadducci99b} Andrea Corradini and [[Fabio Gadducci]], _Rewriting on cyclic structures: equivalence between the operational and the categorical description_, RAIRO Theoretical Informatics and Applications 33(4-5), 1999.

* {#corradini_gadducci02} Andrea Corradini and [[Fabio Gadducci]], _A functorial semantics for multi-algebras and partial algebras, with applications to syntax_, Theoretical Computer Science 286(2), 2002.

* {#golubtsov99} Peter V. Golubtsov, _Axiomatic description of categories of information converters_, Problemy Peredachi Informatsii (Problems in Information Transmission) 35(3), 1999. 

* {#golubtsov02} Peter V. Golubtsov, _Monoidal Kleisli category as a background for information transformers theory_. Information Theory and Information Processing 2, 2002.

* {#golubtsov_mosaliuk02} Peter V. Golubtsov and Stepan S. Moskaliuk, _Method of additional structures on the objects of a monoidal Kleisli category as a background for information transformers theory_, Hadronic Journal 25(2), 2002.

* {#golubtsov04} Peter V. Golubtsov, _Information transformers: category-theoretical structure, informativeness, decision-making problems_, Hadronic Journal Supplements 19(3), 2004.

* {#coecke_spekkens11} [[Bob Coecke]] and Robert W. Spekkens, _Picturing classical and quantum Bayesian inference_, Synthese, 186(3), 2012. ([arXiv](https://arxiv.org/abs/1102.2368))

* {#fong12} [[Brendan Fong]], _Causal theories: A categorical perspective on Bayesian networks_, master thesis, University of Oxford, 2012. ([arXiv](https://arxiv.org/abs/1301.6201))


### Further references

* [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], _De Finetti's theorem in categorical probability_. Journal of Stochastic Analysis, 2021. ([arXiv:2105.02639](https://arxiv.org/abs/2105.02639))

* [[Tobias Fritz]], [[Wendong Liang]], _Free gs-monoidal categories and free Markov categories_, Applied Categorical Structures 31, 21, 2023. ([arXiv:2204.02284](https://arxiv.org/abs/2204.02284))

* Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, Proceedings of LICS, 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* Sean Moss and [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* {#name_gen} Marcin Sabok, Sam Staton, Dario Stein, Michael Wolman, _Probabilistic Programming Semantics for Name Generation_, Proceedings POPL, 2021. ([arXiv](https://arxiv.org/abs/2007.08638))

* Elena Di Lavore and Mario Román, _Evidential Decision Theory via Partial Markov Categories_, Proceedings of LICS, 2023. ([arXiv](https://arxiv.org/abs/2301.12989))

* [[Bart Jacobs]], _Multinomial and Hypergeometric Distributions in Markov Categories_, Proceedings of MFPS 2021. ([arXiv](https://arxiv.org/abs/2112.14044))

* [[Tobias Fritz]], [[Fabio Gadducci]], Davide Trotta, Andrea Corradini, _From gs-monoidal to oplax-cartesian categories: constructions and functorial completeness_, Applied Categorical Structures 31, 42, 2023. ([arXiv](https://arxiv.org/abs/2205.06892))

* [[Tobias Fritz]], [[Fabio Gadducci]], [[Paolo Perrone]] and Davide Trotta, _Weakly Markov categories and weakly affine monads_, Proceedings of CALCO, LIPIcs 10, 2023. ([arXiv](https://arxiv.org/abs/2303.14049))

* {#gauss} Dario Stein and Richard Samuelson, _A Category for unifying Gaussian Probability and Nondeterminism_, Proceedings of CALCO, LIPIcs 10, 2023. ([arXiv](https://arxiv.org/abs/2204.14024))

* Dario Stein and [[Sam Staton]], _Probabilistic Programming with Exact Conditions_, JACM, 2023. ([arXiv](https://arxiv.org/abs/2312.17141))

* {#supports_idemp} [[Tobias Fritz]], Tomáš Gonda, Antonio Lorenzin, [[Paolo Perrone]] and Dario Stein, _Absolute continuity, supports and idempotent splitting in categorical probability_, 2023. ([arXiv:2308.00651](https://arxiv.org/abs/2308.00651))

* Dario Stein and Richard Samuelson, _Towards a Compositional Framework for Convex Analysis (with Applications to Probability Theory)_, 2023. ([arXiv](https://arxiv.org/abs/2312.02291))

* Nathaniel Virgo, _Unifilar Machines and the Adjoint Structure of Bayesian Filtering_, Proceedings of ACT, 2023. ([arXiv](https://arxiv.org/abs/2305.02826))

* Noé Ensarguet and [[Paolo Perrone]], _Categorical probability spaces, ergodic decompositions_, and transitions to equilibrium, 2023. ([arXiv:2310.04267](https://arxiv.org/abs/2310.04267))

* [[Tobias Fritz]] and Antonio Lorenzin, _Involutive Markov categories and the quantum de Finetti theorem_, 2023. ([arXiv](https://arxiv.org/abs/2312.09666))

* [[Tobias Fritz]], Andreas Klingler, Drew McNeely, Areeb Shah-Mohammed and Yuwen Wang, _Hidden Markov models and the Bayes filter in categorical probability_, 2024. ([arXiv](https://arxiv.org/abs/2401.14669))

In the context of [[Bayesian inversion]]:

* {#quantum_markov} [[Arthur J. Parzygnat]]: _Inverses, disintegrations, and Bayesian inversion in quantum Markov categories_ &lbrack;[arXiv:2001.08375](https://arxiv.org/abs/2001.08375)&rbrack;

* {#noncommutative_bayes} [[Arthur J. Parzygnat]], [[Benjamin P. Russo]]: _A noncommutative Bayes theorem_, Linear Algebra Applications **644** (2022) &lbrack;[doi:10.1016/j.laa.2022.02.030](https://doi.org/10.1016/j.laa.2022.02.030), [arXiv:2005.03886](https://arxiv.org/abs/2005.03886)&rbrack;

* {#conditional_quantum} [[Arthur J. Parzygnat]]: *Conditional distributions for quantum systems*, EPTCS **343** (2021) 1-13 &lbrack;[arXiv:2102.01529](https://arxiv.org/abs/2102.01529), [doi:10.4204/EPTCS.343.1](https://doi.org/10.4204/EPTCS.343.1)&rbrack;

* {#quantum_states_time} [[James Fullwood]], [[Arthur J. Parzygnat]]: _On quantum states over time_, Proceedings of the Royal Society A **478** (2022) &lbrack;[arXiv:2202.03607](https://arxiv.org/abs/2202.03607), [doi:10.1098/rspa.2022.0104](https://doi.org/10.1098/rspa.2022.0104)&rbrack;

* {#retrodiction} [[Arthur J. Parzygnat]], Francesco Buscemi, _Axioms for retrodiction: achieving time-reversal symmetry with a prior_, Quantum **7** (2023) 1013 &lbrack;[arXiv:2210.13531](https://arxiv.org/abs/2210.13531), [doi:10.22331/q-2023-05-23-1013](https://doi.org/10.22331/q-2023-05-23-1013)&rbrack;

* {#quantum_bayes} [[James Fullwood]], [[Arthur J. Parzygnat]]: _From time-reversal symmetry to quantum Bayes rules_, PRX Quantum **4** (2023) &lbrack;[arXiv:2212.08088](https://arxiv.org/abs/2212.08088), [doi:10.1103/PRXQuantum.4.020334](https://doi.org/10.1103/PRXQuantum.4.020334)&rbrack;




### References about Markov kernels

* {#Kallenberg17} Olaf Kallenberg: *Random Measures, Theory and Applications* Springer (2017)

* {#BM19} Vladimir Bogachev and Il’ya Malofeev, Kantorovich problems and conditional measures depending on a parameter. ([arXiv](https://arxiv.org/abs/1904.03642))

See also the references at [[Markov kernel]].


category: probability

[[!redirects Markov categories]]
[[!redirects markov category]]
[[!redirects markov categories]]
[[!redirects copy-discard category]]
[[!redirects copy-discard categories]]
[[!redirects copy discard category]]
[[!redirects copy discard categories]]
[[!redirects cd category]]
[[!redirects cd categories]]
[[!redirects cd-category]]
[[!redirects cd-categories]]
[[!redirects CD category]]
[[!redirects CD categories]]
[[!redirects CD-category]]
[[!redirects CD-categories]]