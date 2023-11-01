
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

\tableofcontents

\section{Idea}

The notion of a *sketch* ([Bastiani & Ehresmann 1972](#BastianiEhresmann72)) is one formalisation of the notion of a *[[theory]]*. It is [[diagram|diagrammatic]], and has the advantage of being very close to [[category theory]], allowing it to very naturally express the category theoretic structure which is required to construct a [[model]] of the theory ([[finite products]], say). On the other hand, it is not a very concise notion: as Example \ref{ExampleSketchUnitalMagmas} illustrates, writing down the full details of a sketch even in the simplest examples takes time!

There is a precise correspondence between categories of models of sketches and [[accessible category|accessible categories]] and [[locally presentable category|locally presentable categories]], discussed below.

The notion of a sketch generalises that of a [[Lawvere theory]]. See Example \ref{ExampleLawvereTheory}.

\section{Details}

\subsection{Sketches}

\begin{defn} A _sketch_ is a [[small category|small]] [[category]] $T$ equipped with a set $L$ of [[cones]] and a set $C$ of [[cocones]]. Alternatively, it is a [[directed graph]] equipped with a set $D$ of [[diagram|diagrams]], a set $L$ of [[cones]], and a set $C$ of [[cocones]]. \end{defn}

\begin{defn} A _realized sketch_ is one where all the cones in $L$ are [[limit]] cones and all the cocones in $C$ are [[colimit]] cocones. \end{defn}

\begin{defn} A _limit sketch_ is a sketch with $C = \emptyset$. \end{defn}

\begin{defn} A _colimit sketch_ is a sketch with $L = \emptyset$. \end{defn}

\begin{defn} A _finite product sketch_ is a limit sketch in which the only cones are those of [[finite product]] diagrams. \end{defn}

\begin{defn} A _finite limit sketch_ is a limit sketch in which the only cones are those of [[finite limit]] diagrams. \end{defn}

\subsection{Models of sketches}

\begin{defn} A _model of a sketch_ in a category $\mathcal{C}$ is a [[functor]] $T\to \mathcal{C}$ taking each cone in $L$ to a limit cone and each cocone in $C$ to a colimit cocone. \end{defn}

In particular, $T$ is realized if and only if its identity functor is a model.  

\begin{defn} If one takes the definition of a sketch to be that involving directed graphs, a _model of a sketch_ in a category $\mathcal{C}$ is a morphism of directed graphs from the directed graph of the sketch to the underlying directed graph of $\mathcal{C}$, so that diagrams are taken to commutative diagrams, cones are taken to limit cones, and co-cones are taken to colimit cones.\end{defn}

Frequently the notion of model is restricted to the case $\mathcal{C}=Set$.

\begin{defn} A [[category]] is _sketchable_ if it is the category of models (in $Set$) of a sketch. \end{defn}

\section{Examples}

\begin{example} A sketch, more precisely a finite product sketch, for the theory of pointed sets can be constructed as follows. The directed graph can be taken to be the following.

\begin{centre} 
  \begin{tikzpicture}
    \fill (0,0) circle[radius=0.1];
    \node at (0,-0.3) {$v_{1}$};
    \fill (3,0) circle[radius=0.1];
    \node at (3,-0.3) {$v_{2}$};
    \draw[shorten <= 0.5em, shorten >= 0.5em, ->] (0,0) -- (3,0);
  \end{tikzpicture}
\end{centre}

The set of diagrams can be taken to be empty. The set of cones can be taken to be the set with the single cone given by the vertex $v_{1}$, i.e. a cone of the empty diagram. The set of co-cones can be taken to be empty.

A model of this sketch necessarily sends the vertex $v_{1}$ to a product of the empty diagram, hence to a one element set $1$; sends the vertex $v_{2}$ to any set $X$; and sends the arrow from $v_{1}$ to $v_{2}$ to an arrow from $1$ to $X$, that is, to an element of $X$, as required. 
\end{example}

\begin{example} \label{ExampleSketchUnitalMagmas} A sketch, more precisely a finite product sketch, for the theory of unital magmas (sets with a binary operation which has a two sided unit) can be constructed as follows. The directed graph can be taken to be the following.

\begin{centre}
  \begin{tikzpicture}
    \fill (0,0) circle[radius=0.1];
    \fill (3,0) circle[radius=0.1];
    \fill (6,0) circle[radius=0.1];
    \fill (3,3) circle[radius=0.1];
    \fill (3,-3) circle[radius=0.1];
    \draw[shorten <= 0.5em, shorten >= 0.5em, ->] (0,0) to node[auto] {$e$} (3,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, <-, bend right=60] (3, 0) to node[auto, swap] {$p_{1}$} (6,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, <-, transform canvas={yshift=-0.1em}, bend left=60] (3, 0) to node[auto] {$p_{2}$} (6,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, <-] (3, 0) to node[auto] {$m$} (6,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=0.1em}, bend right] (3, 3) to node[auto, swap] {$p_{1}$} (0,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, ->] (3, 3) to node[auto] {$p_{2}$} (3,0);
   \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=-0.1em}, bend left] (3, 3) to node[auto] {$e, -$} (6,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=0.1em}, bend left] (3, -3) to node[auto] {$p_{2}$} (0,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, ->] (3, -3) to node[auto, swap] {$p_{1}$} (3,0);
   \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=-0.1em}, bend right] (3, -3) to node[auto, swap] {$-, e$} (6,0);
  \end{tikzpicture}
\end{centre}

The set of diagrams can be taken to have six elements, the first consisting of  

\begin{centre}
  \begin{tikzpicture}
    \fill (3,0) circle[radius=0.1];
    \fill (6,0) circle[radius=0.1];
    \fill (3,3) circle[radius=0.1];
    \draw[shorten <= 0.5em, shorten >=0.5em, <-] (3, 0) to node[auto] {$m$} (6,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, ->] (3, 3) to node[auto] {$p_{2}$} (3,0);
   \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=-0.1em}, bend left] (3, 3) to node[auto] {$e, -$} (6,0);
  \end{tikzpicture}
\end{centre}

the second consisting of the following

\begin{centre}
  \begin{tikzpicture}
    \fill (3,0) circle[radius=0.1];
    \fill (6,0) circle[radius=0.1];
    \fill (3,-3) circle[radius=0.1];
    \draw[shorten <= 0.5em, shorten >=0.5em, <-] (3, 0) to node[auto] {$m$} (6,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, ->] (3, -3) to node[auto, swap] {$p_{1}$} (3,0);
   \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=-0.1em}, bend right] (3, -3) to node[auto, swap] {$-, e$} (6,0);
  \end{tikzpicture}
\end{centre}

the third consisting of the following 

\begin{centre}
  \begin{tikzpicture}
    \fill (0,0) circle[radius=0.1];
    \fill (3,0) circle[radius=0.1];
    \fill (6,0) circle[radius=0.1];
    \fill (3,3) circle[radius=0.1];
    \draw[shorten <= 0.5em, shorten >= 0.5em, ->] (0,0) to node[auto] {$e$} (3,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, <-, bend right=60] (3, 0) to node[auto, swap] {$p_{1}$} (6,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=0.1em}, bend right] (3, 3) to node[auto, swap] {$p_{1}$} (0,0);
   \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=-0.1em}, bend left] (3, 3) to node[auto] {$e, -$} (6,0);
  \end{tikzpicture}
\end{centre}

the fourth consisting of the following

\begin{centre}
  \begin{tikzpicture}
    \fill (3,0) circle[radius=0.1];
    \fill (6,0) circle[radius=0.1];
    \fill (3,3) circle[radius=0.1];
    \draw[shorten <= 0.5em, shorten >=0.5em, <-, bend left=60] (3, 0) to node[auto] {$p_{2}$} (6,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, ->] (3, 3) to node[auto] {$p_{2}$} (3,0);
   \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=-0.1em}, bend left] (3, 3) to node[auto] {$e, -$} (6,0);
  \end{tikzpicture}
\end{centre}

the fifth consisting of the following

\begin{centre}
  \begin{tikzpicture}
    \fill (3,0) circle[radius=0.1];
    \fill (6,0) circle[radius=0.1];
    \fill (3,-3) circle[radius=0.1];
    \draw[shorten <= 0.5em, shorten >=0.5em, <-, bend right=60] (3, 0) to node[auto, swap] {$p_{1}$} (6,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, ->] (3, -3) to node[auto, swap] {$p_{1}$} (3,0);
   \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=-0.1em}, bend right] (3, -3) to node[auto, swap] {$-, e$} (6,0);
  \end{tikzpicture}
\end{centre}

and the sixth consisting of the following.

\begin{centre}
  \begin{tikzpicture}
    \fill (0,0) circle[radius=0.1];
    \fill (3,0) circle[radius=0.1];
    \fill (6,0) circle[radius=0.1];
    \fill (3,-3) circle[radius=0.1];
    \draw[shorten <= 0.5em, shorten >= 0.5em, ->] (0,0) to node[auto] {$e$} (3,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, <-, bend left=60] (3, 0) to node[auto, swap] {$p_{2}$} (6,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=0.1em}, bend left] (3, -3) to node[auto] {$p_{2}$} (0,0);
   \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=-0.1em}, bend right] (3, -3) to node[auto, swap] {$-, e$} (6,0);
  \end{tikzpicture}
\end{centre}

The set of cones can be taken to have four elements, the first being the leftmost vertex (cone of the empty set), the second consisting of 

\begin{centre}
  \begin{tikzpicture}
    \fill (0,0) circle[radius=0.1];
    \fill (3,0) circle[radius=0.1];
    \fill (3,3) circle[radius=0.1];

    \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=0.1em}, bend right] (3, 3) to node[auto, swap] {$p_{1}$} (0,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, ->] (3, 3) to node[auto] {$p_{2}$} (3,0);
  \end{tikzpicture}
\end{centre}

the third consisting of 

\begin{centre}
  \begin{tikzpicture}
    \fill (0,0) circle[radius=0.1];
    \fill (3,0) circle[radius=0.1];
    \fill (3,-3) circle[radius=0.1];
    \draw[shorten <= 0.5em, shorten >=0.5em, ->, transform canvas={yshift=0.1em}, bend left] (3, -3) to node[auto] {$p_{2}$} (0,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, ->] (3, -3) to node[auto, swap] {$p_{1}$} (3,0);
  \end{tikzpicture}
\end{centre}

and the fourth consisting of the following.

\begin{centre}
  \begin{tikzpicture}
    \fill (3,0) circle[radius=0.1];
    \fill (6,0) circle[radius=0.1];
    \draw[shorten <= 0.5em, shorten >=0.5em, <-, bend right=60] (3, 0) to node[auto, swap] {$p_{1}$} (6,0);
    \draw[shorten <= 0.5em, shorten >=0.5em, <-, transform canvas={yshift=-0.1em}, bend left=60] (3, 0) to node[auto] {$p_{2}$} (6,0);
  \end{tikzpicture}
\end{centre}

The set of co-cones can be taken to be empty.

In a model of this sketch, the leftmost vertex is sent to a one element set $1$, the middle vertex is sent to an arbitrary set $X$, the top vertex is sent to the product $1 \times X$, the bottom vertex is sent to the product $X \times 1$, and the right vertex is sent to the product $X \times X$. The arrow $e$ picks out an element $e_{X}$ of $X$. 

The arrow $e,-$ is sent to an arrow $e_{X} \times id: 1 \times X \rightarrow X \times X$, which is forced by the universal property of $X \times X$ and the fact that the diagrams 

\begin{centre}
  \begin{tikzcd}
    1 \times X \ar[r, "e_{X} \times id"] \ar[d, "p_{1}", swap] & X \times X \ar[d, "p_{1}"] \\
    1 \ar[r, "e_{X}", swap] & X 
  \end{tikzcd}
\end{centre}

and

\begin{centre}
  \begin{tikzcd}
    1 \times X \ar[r, "e_{X} \times id"] \ar[dr, "p_{2}", swap] & X \times X \ar[d, "p_{2}"] \\
      & X 
  \end{tikzcd}
\end{centre}

commute to really be the product of the arrows $e_{X}$ and $id$. Similarly, the arrow $-,e$ is sent to an arrow $id \times e_{X}: X \times 1 \rightarrow X \times X$, which is forced by the fact that the diagrams 

\begin{centre}
  \begin{tikzcd}
    X \times 1 \ar[r, "id \times e_{X}"] \ar[dr, "p_{1}", swap] & X \times X \ar[d, "p_{1}"] \\
      & X 
  \end{tikzcd}
\end{centre}

and

\begin{centre}
  \begin{tikzcd}
    X \times 1 \ar[r, "id \times e_{X}"] \ar[d, "p_{2}", swap] & X \times X \ar[d, "p_{2}"] \\
    1 \ar[r, "e_{X}", swap] & X 
  \end{tikzcd}
\end{centre}

commute to really be the product of the arrows $e_{X}$ and $id$.

The arrow $m$ is sent to a map $m: X \times X \rightarrow X$ which is arbitrary except that the diagrams 

\begin{centre}
  \begin{tikzcd}
    1 \times X \ar[r, "e_{X} \times id"] \ar[dr, "p_{2}", swap] & X \times X \ar[d, "m"] \\
      & X
  \end{tikzcd}
\end{centre}

and 

\begin{centre}
  \begin{tikzcd}
    X \times 1 \ar[r, "id \times e_{X}"] \ar[dr, "p_{1}", swap] & X \times X \ar[d, "m"] \\
      & X
  \end{tikzcd}
\end{centre}

are forced to commute. 

Putting all of this together, we see that we exactly have a unital magma. 

\end{example}

\begin{example} \label{ExampleLawvereTheory} A [[Lawvere theory]] is a special case of a (limit) sketch, where the category is one with a distinguished object $X$ such that all objects are ([[isomorphic]] to) powers of $X$, and $C = \emptyset$ and $L$ is the set of all product cones. \end{example}

## Properties

### Relation to accessible and locally representable categories
 {#RelationToLocallyRepresentableCategories}


\begin{proposition}
\label{LimitSketchableCategoriesAreAccessible}
The categories of models of sketches are equivalently the [[accessible categories]].
\end{proposition}

\begin{proposition}
\label{LimitSketchableCategoriesAreLocallyPresentable}
The categories of models of limit-sketches are the [[locally presentable categories]].
\end{proposition}

+-- {: .num_prop }
###### Remark

From the discussion there we have that

* an [[accessible category]] is equivalently:
  * a full subcategory of a presheaf category that's closed under $\kappa$-filtered colimits for some $\kappa$
  * the category of models of a sketch

* a [[locally presentable category]] is equivalently:
  * a *reflective* full subcategory of a presheaf category that's closed under $\kappa$-filtered colimits for some $\kappa$
  * the category of models of a *limit* sketch
  * an accessible category with all small limits
  * an accessible category with all small colimits

We can "break in half" the difference between the two and define

* a [[locally multipresentable category]] to be equivalently:
  * a *multireflective* full subcategory of a presheaf category that's closed under $\kappa$-filtered colimits for some $\kappa$
  * the category of models of a *limit and coproduct* sketch
  * an accessible category with all small *connected* limits
  * an accessible category with all small multicolimits

and

* a *weakly locally presentable category* to be equivalently:
  * a *weakly reflective* full subcategory of a presheaf category that's closed under $\kappa$-filtered colimits for some $\kappa$
  * the category of models of a *limit and epi* sketch
  * an accessible category with all small products
  * an accessible category with all small weak colimits

=--

### Monoidal Structures on the Category of Sketches

The category of sketches is well behaved: it is complete, cocomplete, cartesian closed and has a second symmetric monoidal closed structure.

+-- {: .num_prop }
###### Proposition 

The category of sketches is [[topological category|topological]] over the category of directed [pseudographs](https://ncatlab.org/nlab/show/pseudograph).

=--

The above proposition gives the category of sketches Cartesian products - however these are often not the sketches one would expect when thinking of the product of two theories. Instead consider the tensor product:
+-- {: .num_prop }
###### Proposition 

Let $S,T$ be sketches. We define the sketch $S \otimes T$ to be:

The vertices of $S \otimes T$ are the product of the set of vertices from $S$, $T$. The set of arrows is given as
$$
\{ (\alpha, b) | \alpha \in \mathsf{Edge}(S), b \in \mathsf{Vertex}(T)\}
\cup \{ (a, \beta) | a \in \mathsf{Vertex}(S), \beta \in \mathsf{Edge}(T)\}
$$
where the source of $(\alpha,b)$ is $(s_S(\alpha), b)$, and vice versa. $S$ is often called the _horizontal_ structure and $T$ as the _vertical_ structure.
The set of diagrams is the union of the following three sets:

* The horizontal diagrams are constant in the second parameter: $H = \{ (D, b) | D \in \mathsf{Diagrams}(S), b \in \mathsf{Vertex}(T) \}$

* The vertical diagrams are constant in the first parameter: $V =  \{ (a, D) |  a \in \mathsf{Vertex}(S), D \in \mathsf{Diagrams}(T) \}$

* Also add every square diagram: $C$ is the set of squares for each edge $\alpha$ in $S$, $\beta \in T$ 
 
\begin{center}
    \begin{tikzcd} 
        (a,b) \ar[r, "(\alpha{,}b)"] \ar[d, "(a{,}\beta)"] & (a',b) \ar[d, "(a'{,} \beta)"] \\ 
        (a, b') \ar[r, "(\alpha{,} b')"] & (a',b')
     \end{tikzcd}
\end{center}  

* The set of cones and cocones are define analogously to the set of commuting diagrams, except _only_ the vertical and horizontal cones are taken. 
     
This tensor product, along with the unit $(\ast, \emptyset, \emptyset, \emptyset)$, gives the category of sketches a monoidal structure.
=--

This monoidal structure is useful for considering structures like double categories (i.e. categories in the category of categories).
+-- {: .num_prop }

###### Proposition 

Let $S,T$ be sketches, and $X$ some category. Then the category of models of $S$ in the category of models of $T$ in $X$ is equivalent to the category of models of $S \otimes T$ in $X$.

=--

One can ask when $S \otimes T$ has the same models as $T \otimes S$, i.e. when $S$-models in the category of $T$-models are the same as $T$-models in the category of $S$-models.
This is the case, roughly, when the colimits and limits specified in the sketches commute. For example, since limits always commute, you can swap the sketches if both are limit sketches. And you can swap a finite product sketch with a sifted colimit sketch etc. For more precise statements see David Bensons article and the references therein.


In general one can not swap the order in the monoidal product.
For example take the (terminal object + coproduct)-sketch $S$ whose models are maps $X \to X \coprod 1$ and the finite product sketch $M$ whose models are monoids. Look at models of these in $Set$:
Since in the category of monoids the terminal object is also initial, the coproduct of a monoid with the terminal object is isomorphic to that monoid again. Therefore $S$-models in $M$-Mod are monoids with an endomorphism.
On the other hand $M$-models in $S$-Mod are pairs of monoids one of which has one element more, plus a homomorphism between them. These categories do not seem to be equivalent.

## Related concepts

* [[internalization]]


## References

### General

Original articles:

* {#BastianiEhresmann72} [[Andrée Bastiani]], [[Charles Ehresmann]], _Categories of sketched structures_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, Tome **13** no 2 (1972)  104-214 ([numdam:CTGDC_1972__13_2_104_0](http://www.numdam.org/item/?id=CTGDC_1972__13_2_104_0))

Overview in:

* [[Charles Wells]], *Sketches: Outline with references*, 1993 ([citeseer:10.1.1.217.3531](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.217.3531), [[Wells_Sketches.pdf:file]])

See also:

* [[Michael Barr]], *Notes on Sketches*, Technical report of the Electrotechnical Laboratory (computer language section), Tsukuba, Japan (1997) &lbrack;[pdf](https://www.math.mcgill.ca/barr/papers/sketch.pdf), [[Barr-NotesOnSketches.pdf:file]]&rbrack;


Textbook accounts:

* [[Michael Barr]], [[Charles Wells]], Section 4 of: *[[Toposes, Triples, and Theories]]*, Originally published by: Springer-Verlag, New York, 1985, republished in:
Reprints in [Theory and Applications of Categories, No. 12 (2005) pp. 1-287](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)

and with emphasis on the relation to [[locally presentable category|locally presentable]] and [[accessible categories]]:

* {#MakkaiPare} [[Michael Makkai]], [[Robert Paré]], Chapter 3 onwards in: _Accessible categories: The foundations of categorical model theory_,  Contemporary Mathematics 104. American Mathematical Society, Rhode Island, 1989 ([ISBN:978-0-8218-7692-3](https://bookstore.ams.org/conm-104))

* {#AdamekRosicky} [[Jiří Adámek]], [[Jiří Rosický]], Def. 1.49 onwards in: _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)



That not only every sketchable category is [[accessible category|accessible]] but that conversely every [[accessible category]] is sketchable is due to

* Christian Lair, _Cat&#233;gories modelables et cat&#233;gories esquissables_, [Diagrammes (1981)](http://www.numdam.org/article/DIA_1981__6__A5_0.pdf).

The tensor product of sketches is investigated here:

* David D. Benson, Multilinearity of sketches, [TAC, vol.11, nr. 3, pp.269-277](http://www.tac.mta.ca/tac/volumes/1997/n11/n11.pdf)

The category of sketches itself was studied as a [[categorical semantics]] for [[type theory]] in:

* {#Gray} [[John W. Gray]], _The Category of Sketches as a Model for Algebraic Semantics_, Categories in Computer Science and Logic: Proceedings of the AMS-IMS-SIAM Joint Summer Research Conference Held June 14-20, 1987 with Support from the National Science Foundation. Vol. 92. American Mathematical Soc., 1989.

See also

* [[Martin Brandenburg]], *Large limit sketches and topological space objects* ([arXiv:2106.11115](https://arxiv.org/abs/2106.11115))

### In enriched category theory

Discussion of sketches the generality of [[enriched category theory]]:

* {#Kelly82} [[G. Max Kelly]], *Structures defined by finite limits in the enriched context, I*, Cahiers de topologie et géométrie différentielle **23** 1 (1982)  3-42 &lbrack;[numdam:CTGDC_1982__23_1_3_0](http://archive.numdam.org/item/CTGDC_1982__23_1_3_0)&rbrack;


* [[Francis Borceux]], [[Carmen Quinteriro]], [[Jiří Rosický]], *A theory of enriched sketches*, Theory and Applications of Categories, **4** 3 (1998) 47-72 &lbrack;[tac:4-03](http://www.tac.mta.ca/tac/volumes/1998/n3/4-03abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/1998/n3/n3.pdf)&rbrack;

### Generalisations

A generalisation internal to a [[2-category]] is discussed in:

* Yoshiki Kinoshita, [[John Power]], and Makoto Takeyama. _Sketches_, Journal of Pure and Applied Algebra 143.1-3 (1999): 275-291.

* [[Ross Street]]. _Pointwise extensions and sketches in bicategories_ (2014), ([arXiv:1409.6427](https://arxiv.org/abs/1409.6427)).

* [[Ross Street]]. _Complete objects with respect to a theory_.



[[!redirects sketches]]

[[!redirects finite product sketch]]
[[!redirects finite product sketches]]

[[!redirects finite limit sketch]]
[[!redirects finite limit sketches]]

[[!redirects limit sketch]]
[[!redirects limit sketches]]
