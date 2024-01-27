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

The formalism of Markov categories is one of the most recent [[categorical approaches to probability theory]]. 

Intuitively, a Markov category can be seen as a category where morphisms behave like "random functions", for example, [[Markov kernels]] form such a category (hence the name). Canonical examples are [[Kleisli categories]] of [[probability monads]]. The formalism is however far more general. 

**Caveat**: some of the content of this page reflects work in progress. Content may change.



## Definitions

A formal, concise definition can be given as follows: A **Markov category** is a [[semicartesian monoidal category|semicartesian]] [[symmetric monoidal category]] $(C,\otimes,1)$ in which every object $X$ is equipped with the structure of a [[commutative]] [[internal monoid|internal comonoid]].
Equivalently, it is a semicartesian symmetric monoidal category that [[supply in a monoidal category|supplies]] commutative comonoids.

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

Similarly, one can form the product of three or more objects and morphisms. Note that in the diagrams, the product is strictly associative: string diagrams, rather than the original category, technically represent a [[strict monoidal category]] which is [[monoidal equivalence|monoidally equivalent]] to the original one. (Such a category always exists thanks to the [[coherence theorem for monoidal categories|coherence theorem]].)

In a similar vein, the monoidal unit is usually not appearing in string diagrams, whenever this does not cause confusion. This way, for example, the diagram
imply as a wire:

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
 
represent the object $X$ but also $X\otimes I$, $I\otimes X$, and so on. 

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

These will model probabilistic states, such as information sources or probability measures (see below).
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
		\node [style=none] (14) at (0, 0) {$=$};
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

* The monoidal unit $I$ is a [[terminal object]] (i.e. the category is [[semicartesian]] monoidal);
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
		\node [style=bn] (2) at (2, 0.5) {};
		\node [style=none] (3) at (2, -1) {};
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


### The Markov structure of *Set*

Consider the category [[Set]] of sets and functions, with its usual cartesian monoidal structure (given by the cartesian product of sets). 

Every set $X$ is equipped with canonical maps
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
 X \ar{r}{\mathrm{copy}} & X\times X && X \ar{r}{\mathrm{del}} & 1 \\
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
First of all, as monoidal structure we again take the cartesian product of sets. (In this category, it is not a [[categorical product]], but it's still a [[monoidal category|monoidal]] one.)
We now the copy and discard maps as the maps $\delta_copy$ and $\delta_del$ induced by the ones of *Set* (see the example above). 
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

- The category [[Stoch]] of [[measurable spaces]] and [[Markov kernels]]

(...)

### Kleisli categories of probability monads

- For any [[cartesian monoidal category]] $\mathsf{C}$ equipped with a [[monoidal monad]] $T$ preserving the monoidal unit, the [[Kleisli category]] $Kl(T)$ is a Markov category.

(...)



## Core concepts

### Conditional independence

(...)

### Deterministic morphisms

A morphism $f:X\to Y$ in a Markov category is called **deterministic** if it commutes with the copy map,
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
		\node [style=none] (16) at (0, 0) {$=$};		
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

A way to motivate the definition is the following. Suppose that $f$ is a "random" function between real numbers, which adds to the input the result of the roll of a die. Given a number $x$, we can roll a die, add the resulting value (say, $n$) to $x$, and then copy the result, to get $(x+n,x+n)$. Or, we could copy the value $x$, roll two dice (or roll the die twice), and add the two resulting values (say, $m$ and $n$) to the two copies of $x$, obtaining $(x+m,x+n)$. The two results are likely to differ. 
One can take this as a _definition_ of randomness: it's a process that may give a different result if you do it twice. Or equivalently, that copying the information before or after the process has taken place gives different results.

A _deterministic_ morphism is instead one that does _not_ exhibit this behavior, i.e. that commutes with the copy map.

(...)

## Further structures and properties

(...)

### Conditionals

### Kolmogorov products

### Positivity

(to be expanded)


### Representable Markov categories

For now, see [[probability monad]].


## History

(...)


## Detailed list
 {#DetailedList}

(...to be expanded...)

<table>
 <tr>
  <th markdown="1">Category</th>
  <th markdown="1">[[probability monad|Probability monad]]</th>
  <th markdown="1">[[Markov category#conditionals|Conditionals]]</th>
  <th markdown="1">[[Markov category#positivity|Positivity]]</th>
  <th markdown="1">[[Markov category#kolmogorov_products|Kolmogorov products]]</th>
  <th markdown="1">Further references</th>
 </tr>
 <tr>
  <th markdown="1">[[Stoch]]</th>
  <td markdown="1">[[Giry monad]] on [[Meas]]</td>
  <td markdown="1">No ([Fritz'19](#fritzmarkov), Example 11.3)</td>
  <td markdown="1">Yes ([Fritz'19](#fritzmarkov), Example 11.25)</td>
  <td markdown="1">Not in general</td>
  <td markdown="1">[Fritz'19](#fritzmarkov)</td>
 </tr>
<tr>
  <th markdown="1">[[Stoch#borelstoch|BorelStoch]]</th>
  <td markdown="1">[[Giry monad]] on [[Pol]]</td>
  <td markdown="1">Yes ([Kallenberg '17](#Kallenberg17), [B-M'19](#BM19))</td>
  <td markdown="1">Yes ([Fritz'19](#fritzmarkov), Section 11)</td>
  <td markdown="1">Countable ([Fritz-Rischel'19](#fritzrischel))</td>
  <td markdown="1">[Fritz'19](#fritzmarkov)</td>
 </tr>
<tr>
  <th markdown="1">[[Stoch#finstoch|FinStoch]]</th>
  <td markdown="1">Not representable (closely related to the [[distribution monad]])</td>
  <td markdown="1">Yes ([Fritz'19](#fritzmarkov), Example 11.6)</td>
  <td markdown="1">Yes ([Fritz'19](#fritzmarkov), Section 11)</td>
  <td markdown="1">No</td>
  <td markdown="1">[Fritz'19](#fritzmarkov)</td>
 </tr>
<tr>
  <th markdown="1">**TychStoch**</th>
  <td markdown="1">[[extended probabilistic powerdomain#the_probability_monad_on_top|probability monad on topological spaces]] (here, Tychonoff)</td>
  <td markdown="1"> No </td>
  <td markdown="1"> Yes ([Fritz et al'23](#supports_idemp)) </td>
  <td markdown="1"> ? </td>
  <td markdown="1">[Fritz et al'23](#supports_idemp)</td>
 </tr>
<tr>
  <th markdown="1">**QBStoch**</th>
  <td markdown="1">probability monad on [[quasi-Borel spaces]] (here, Tychonoff)</td>
  <td markdown="1"> No ([Sabok et al'20](#name_gen))</td>
  <td markdown="1"> No ([Sabok et al'20](#name_gen))</td>
  <td markdown="1"> ? </td>
  <td markdown="1">[Fritz et al'23](#dilations)</td>
 </tr>
</table>


## See also

* [[probability theory]], [[categorical probability]]

* [[Markov kernel]], [[stochastic map]]

* [[probability monad]]

* [[statistics]]

* [[zero-one law]]

* [[doctrine]]

* [[supply in a monoidal category]]


## References

Markov categories as defined here appear in:

* {#fritzmarkov} [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, 2019. ([arXiv:1908.07021](http://arxiv.org/abs/1908.07021))

* {#fritzrischel} [[Tobias Fritz]] and [[Eigil Fjeldgren Rischel]], _The zero-one laws of Kolmogorov and Hewitt--Savage in categorical probability_, 2019. ([arXiv:1912.02769](http://arxiv.org/abs/1912.02769))

* [[Tobias Fritz]], [[Tomáš Gonda]], [[Paolo Perrone]], [[Eigil Fjeldgren Rischel]], _Representable Markov categories and comparison of statistical experiments in categorical probability_. ([arXiv:2010.07416](https://arxiv.org/abs/2010.07416))

* [[Tobias Fritz]], [[Tomáš Gonda]], [[Paolo Perrone]], _De Finetti's theorem in categorical probability_. Journal of Stochastic Analysis, 2021. ([arXiv:2105.02639](https://arxiv.org/abs/2105.02639))

* [[Tobias Fritz]], [[Wendong Liang]], _Free gs-monoidal categories and free Markov categories_, 2022. ([arXiv:2204.02284](https://arxiv.org/abs/2204.02284))

* [[Sean Moss]], [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* [[Sean Moss]] and [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* {#dilations} [[Tobias Fritz]], [[Tomáš Gonda]], Nicholas Gauguin Houghton-Larsen, [[Paolo Perrone]] and [[Dario Stein]], _Dilations and information flow axioms in categorical probability_. Mathematical Structures in Computer Science, 2023. ([arXiv:2211.02507](https://arxiv.org/abs/2211.02507)).

* {#name_gen} Marcin Sabok, Sam Staton, Dario Stein, Michael Wolman, _Probabilistic Programming Semantics for Name Generation_, 2020. ([arXiv](https://arxiv.org/abs/2007.08638))

* [[Paolo Perrone]], _Markov Categories and Entropy_, IEEE Transactions on Information Theory, 2023. ([arXiv:2212.11719](https://arxiv.org/abs/2212.11719))

* {#supports_idemp} [[Tobias Fritz]], [[Tomáš Gonda]], [[Antonio Lorenzin]], [[Paolo Perrone]] and [[Dario Stein]], _Absolute continuity, supports and idempotent splitting in categorical probability_, 2023. ([arXiv:2308.00651](https://arxiv.org/abs/2308.00651))

* Noé Ensarguet and [[Paolo Perrone]], _Categorical probability spaces, ergodic decompositions_, and transitions to equilibrium, 2023. ([arXiv:2310.04267](https://arxiv.org/abs/2310.04267))

See also the references therein.

The first idea of defining a "category of probabilistic mappings" seems to be due to [[Lawvere]], in

*{#Lawvere62} [[W. Lawvere]], _The category of probabilistic mappings_, ms. 12 pages, 1962 
([[lawvereprobability1962.pdf:file]])

(...more to come...)


Further references:

* {#Kallenberg17} Olaf Kallenberg, _Random Measures, Theory and Applications_, Springer, 2017.

* {#BM19} Vladimir Bogachev and Il'ya Malofeev, _Kantorovich problems and conditional measures depending on a parameter_. ([arXiv:1904.03642](https://arxiv.org/abs/1904.03642))


[[!redirects Markov categories]]
[[!redirects markov category]]
[[!redirects markov categories]]