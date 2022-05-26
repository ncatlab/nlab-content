
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

### General
 {#IdeaGeneral}

*Persistent cohomotopy* (not yet an established term) would be the study of [[cohomotopy]] in situations where the [[domain]] [[topological space|space]] and/or its [[continuous function|map]] to an [[n-sphere]] may depend on a parameter, to yield not just a single [[cohomotopy set]], but a [[filtered object|filtered]] set (a filtered [[group]] when the [[dimension of a cell complex|dimension]] of the domain space is large enough). One concrete implementation of this general notion is considered in [Franek & Krčál 2017](#FranekKrcal17), see [below](#Definition). 

Generally, one may understand persistent cohomotopy both as the [[duality|dual]] of *[[persistent homotopy]]* as well as a [[non-abelian cohomology]]-version of the more widely considered notion of [[persistent homology]]:


| | coarse |  intermediate | fine  |
|--|--|--|--|
| **[[homology]]** | [[ordinary homology]] | [[generalized homology]] | [[homotopy groups|homotopy]] |
| **[[cohomology]]** | [[ordinary cohomology]] | [[Whitehead-generalized cohomology|generalized cohomology]] | [[cohomotopy]] |
|  |  |  |  | 
| **persistent homology** | [[persistent homology|persistent ordinary homology]] | persistent generalized homology | [[persistent homotopy]] |
| **persistent cohomology** | persistent ordinary cohomology | persistent generalized cohomology | [[persistent cohomotopy]] |


### Detecting data meeting targets
 {#DetectingDataMeetingTargets}

While [[persistent homology]], as a tool in [[topological data analysis]], is traditionally meant to discover [[persistence diagram|persistent]] [[cycles]] in a given data set, it is typically unclear what a persistent cycle actually *means* for the practical interpretation of the data -- certainly this information is not provided by the mathematics.


\begin{imagefromfile}
    "file_name": "IndicatorFunctionOnData-220523.jpg",
    "float": "right",
    "width": 420,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 0,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

In contrast, [[persistent cohomotopy]] in [[TDA]] is the effective answer to a concrete and common question in [[data analysis]]: 

Given a large-[[dimension of a CW-complex|dimensional]] [[topological space|space]] of data, and a small [[natural number|number]] $n$ of ([[real number|real]]) indicator values assigned to each data point with given precision $1/r$, *does _any_ data meet a prescribed target indication precisely?*


A fundamental theorem of persistent Cohomotopy ([Franek, Krčál & Wagner 2018](persistent+cohomotopy#FranekKrcal18), [Franek & Krčál 2017, p. 5](persistent+cohomotopy#FranekKrcal17), see Thm. \ref{GuaranteeThatSolutionsExist} below) shows that (1.) the answer to this question is detected by a certain [[Cohomotopy]]-class and (2.) in a fair range of dimensions, this Cohomotopy class is provably [[computability|computable]], hence the above question is effectively [[decidability|decidable]]. $\phantom{----}$ (figure from [[schreiber:New Foundations for TDA -- Cohomotopy|SS22]])


Alternatively, with tools from [[persistent homology theory]] an answer to this question is given by the method of *[[well groups]]* -- but (1.) it is known that well groups are in general too coarse to provide a complete answer and (2.) despite effort it remains unknown if well groups are actually [[computability|computable]] in relevant cases, see [Franek & Krčál 2016](persistent+cohomotopy#FranekKrcal16).

In this concrete sense (and generally by the [above](#IdeaGeneral) discussion), persistent cohomotopy may be understood as an enhancement or refinement of ([[well groups]] in) [[persistent homology]]:

<center>
<img src="https://ncatlab.org/nlab/files/EnhancePersFromHolomogyToCohomotopy-220522.jpg" width="600">
</center>
> (graphics from [[schreiber:New Foundations for TDA -- Cohomotopy|SS 22]])


### Use of cobordism theory
 {#UseOfCobordismTheory}

If the [[topological space]] $X$ of data may be assumed to be a [[smooth manifold]] (indeed, in typical examples $X$ is itself a large-dimensional [[Cartesian space]]) then persistent cohomotopy may be understood dually via [[Pontryagin's theorem]] as characterizing [[iso-hypersurfaces]] of data (close to a given target indicator) by [[framed cobordism|framed]] *[[cobordism theory]]* ([Franek & Krčál 2017, p. 8-9](persistent+cohomotopy#FranekKrcal17)). The full implications of this relation for topological data analysis remain to be explored.
  

## Definition
 {#Definition}

We spell out the definition considered in [Franek & Krčál 2017](#FranekKrcal17).

For 

* $X$ a [[topological space]],

* $n \in \mathbb{N}$ a [[natural number]],

* $r \in \mathbb{R}_{\gt 0}$ a [[positive number|positive]] [[real number]],

* $f \,\colon\, X \xrightarrow{\;\;\;\;\;\;} \mathbb{R}^n$ a [[continuous map]],

such that with

* $A_r \,\coloneqq\, f^{-1}\big( \mathbb{R}^n \setminus B_r \big) \;\xhookrightarrow{i_r}\; X\;$

  (the [[preimage]] under $f$ of the [[complement]] of the [[open ball]] of [[radius]] $r$ around the origin in the [[Cartesian space]])

we have that 

* $(X,A_r)$ is a [[CW-pair]] of [[dimension of a cell complex|dimension]] $dim(X) \leq 2n - 3$,

consider the following induced [[exact sequence]] of [[cohomotopy]]-groups (where square brackets $[X,Y]$ denote the [[hom-set]] $Ho(X,Y)$ in the [[classical homotopy category]], hence [[homotopy classes]] of [[continuous functions]] $X \to Y$):

\begin{tikzcd}[row sep=small]
  \pi^{n-1}
  \big(
    X
  \big)
  \ar[r, "{ \iota_r^\ast}"]
  \ar[d, phantom, "{\coloneqq}"{rotate=-90}]
  &
  \pi^{n-1}
  \big(
    A 
  \big)
  \ar[d, phantom, "{\coloneqq}"{rotate=-90}]
  \ar[r, "{ \delta_r }"]
  &
  \pi^{n}
  \big(
    X
  \big)
  \ar[d, phantom, "{\coloneqq}"{rotate=-90}]
  \\
  \big[
    X
    ,\,
    S^{n-1}
  \big]
  \ar[r, "{ [\iota_r. S^{n-1}] }"]
  &
  \big[
    A
    ,\,
    S^{n-1}
  \big]
  \ar[r]
  &
  \big[
    X
    ,\,
    S^n
  \big]
  \mathrlap{\,.}
\end{tikzcd}


Now define what we may call **the $n$-cohomotopy of $X$ at resolution $1/r$ relative to $f$**, to be (this is [FK17 (2)](#FranekKrcal17)):

\begin{equation}
  \label{CohomotopyAtSomeResolution}
  \pi^n_{(f,r)}
  \;\coloneqq\;
  image(\delta_r)
  \;\simeq\;
  \Big\{
    [g/A_r]
    \,\in\,
    \pi^n(X/A_r)
    \,\big\vert\,
    (X, A_r) \xrightarrow{ \exists \, g } (\mathbb{R}^n,\, \mathbb{R}^n \setminus B_r)
  \Big\}
  \,,
\end{equation}

hence that subgroup of the $n$-cohomotopy group of the [[quotient topological space]] $X/A_r$ whose elements may be represented by [[continuous maps]] defined on all of $X$.

Notice that the function $f$ itself canonically represents an element

\[
  \label{FunctionAsClassInThePersistenceCohomotopyRelativeToIt}
  [f]_r 
    \;\in\;
  \pi^n_{(f,r)}(X)
\]

which provides a base point, making this a [[pointed object|pointed]] group.

Moreover, for $r_1 \leq r_2$ we have the evident inclusion

$$
  A_{r_2} \xhookrightarrow{\; i_{r_1, r_2} \;}  A_{r_1}
$$

and thus a canonical comparison [[homomorphisms]] of pointed groups:

\begin{tikzcd}[row sep=small]
  \pi^n_{(f,r_1)}(X)
  \ar[d, hook]
  \ar[rr]
  &&
  \pi^n_{(f,r_2)}(X)
  \ar[d, hook]
  \\
  \big[
    X/A_{r_1}
    ,\,
    S^n
  \big]
  \ar[rr, "{ \big[ X/{i_{r_1,r_2}}, S^n\big] }"]
  &&
  \big[
    X/A_{r_2}
    ,\,
    S^n
  \big]
  \,.
\end{tikzcd}

Therefore, regarding the [[positive number|positive]] [[real numbers]] [[ordering|ordered]] by $\leq$ as a [[poset]] and thus as a [[category]], the resulting [[direction|directed]] [[diagram]] of [[pointed objects|pointed]] [[groups]]

\[
  \label{TheCohomotopyPersistenceModule}
  \pi^n_{(f,\bullet)}
  (X)
  \;\colon\;
  (\mathbb{R}, \leq)
  \xrightarrow{\;\;\;}
  Grp^{\mathbb{Z}/}
\]

is the **cohomotopy persistence module** ([FK17, p. 5](#FranekKrcal17), rhyming on *[[persistence module]]* as used in [[persistent homology theory]]) of $X$ relative to $f$.

\linebreak

## Properties

For $r \in \mathbb{R}_{\gt 0}$, say that a continuous function 

$$
  g\;\colon\; X \xrightarrow{\;\;} \mathbb{R}^n
$$

is an *$r$-deformation* of the given $f$ if its values are pointwise within a radius $r$ of those of $f$, i.e. if

\[
  \label{rDeformation}
  \vert g-f\vert_\infty
  \;\coloneqq\;
  \underset{x \in X}{max}
  \vert g(x) - r(x)\vert
  \;\lt\;
  r
  \,.
\]


\begin{theorem}\label{GuaranteeThatSolutionsExist}
**([Franek & Krčál 2017](#FranekKrcal17), following [2016, p. 5](#FranekKrcal16))**
\linebreak
Under the above assumptions, the following are equivalent:

* there exists an $r$-deformation (eq:rDeformation) of $f$ with *no* zeros on $X \setminus A_r$;

* the Cohomotopy class $[f]_r \in \pi_n^{(f,r)}(X)$ (eq:FunctionAsClassInThePersistenceCohomotopyRelativeToIt) is trivial.

Moreover, both questions are effectively [[computability|computable]]/[[decidability|decidable]] in the given dimension range.
\end{theorem}

The proof of the computability statement in Thm. \ref{GuaranteeThatSolutionsExist} uses a general result about computability of [[cohomotopy]]-sets from [CKMSVW14](computational+topology#CKMSVW14).



\linebreak

## Examples
 {#Examples}

Consider the simplest instructive example, where $X \subset \mathbb{R}$ is an [[interval]] (closed or open, such as the [[real line]] itself) and $n = 1$. 

Notice that $X$ is [[contractible topological space|contractible]], so that its plain [[cohomotopy]] in [[positive number|positive]] degree is necessarily trivial, $\pi^{n \geq 1}(X) = \ast$. 

Now consider a [[continuous function]] 

$$
  f
  \;\colon\; 
  X 
  \xrightarrow{\;\;} 
  \mathbb{R}^1
$$

to the [[real numbers]], and consider the question whether any continuous map that might differ from $f$ by up to $\pm r$ ever takes the value $0 \in \mathbb{R}$.

In this simple case one can decide this immediately by appeal to the [[intermediate value theorem]]: Any such function $r$-close to $f$ will have to pass through zero at least once if the values of $f$ ever pass between $(-\infty, -r)$ and $(r, \infty)$. But precisely this is also detected by the 1-cohomotopy class of $f$  at resolution $1/r$ (relative to itself) in the sense of (eq:CohomotopyAtSomeResolution), as illustrated in the following figure: 

\begin{tikzpicture}


\begin{scope}

\draw[line width=1pt]
  (-4, 0)
  to
  (4,0);

\draw
  (-4.3,0)
  node
  {
    \colorbox{white}{$X$}
  };

\begin{scope}

\draw[gray, densely dashed]
  (-4, .5)
  to
  (4,.5);
  
\draw[gray, densely dashed]
  (-4, 1)
  to
  (4,1);
  
\draw[gray, densely dashed]
  (-4, 1.5)
  to
  (4,1.5);  

\draw[gray, densely dashed]
  (-4, 2)
  to
  (4,2);   
  
\draw[gray, densely dashed]
  (-4, 2.5)
  to
  (4,2.5);    
  
\draw[red, line width=2pt, densely dashed]
  (-4, 3)
  to
  (4,3);    

\draw[fill=red, fill opacity=.3, draw opacity=0]
  (4,3)
  rectangle
  (-4,4);
  
\draw[gray, densely dashed]
  (-4, 3.5)
  to
  (4,3.5);      
 
\draw[gray, densely dashed]
  (-4, 4)
  to
  (4,4);      
  
\end{scope}  
 
 
\begin{scope}[yscale=-1]

\draw[gray, densely dashed]
  (-4, .5)
  to
  (4,.5);
  
\draw[gray, densely dashed]
  (-4, 1)
  to
  (4,1);
  
\draw[gray, densely dashed]
  (-4, 1.5)
  to
  (4,1.5);  

\draw[gray, densely dashed]
  (-4, 2)
  to
  (4,2);   
  
\draw[gray, densely dashed]
  (-4, 2.5)
  to
  (4,2.5);    
  
\draw[red, line width=2pt, densely dashed]
  (-4, 3)
  to
  (4,3);  
  
\draw[fill=red, fill opacity=.3, draw opacity=0]
  (4,3)
  rectangle
  (-4,4);
  
  
\draw[gray, densely dashed]
  (-4, 3.5)
  to
  (4,3.5);      
 
\draw[gray, densely dashed]
  (-4, 4)
  to
  (4,4);      
  
\end{scope}   

\draw[white, line width=7pt] 
  plot[smooth]
  coordinates
  {
    (-4,-3.9)
    (-3.5, -3.7)
    (-3.1, -3)
    (-2.5, -2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  
  
\draw plot[smooth]
  coordinates
  {
    (-4,-3.9)
    (-3.5, -3.7)
    (-3.1, -3)
    (-2.5, -2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  
\draw[gray, densely dashed]
 (2.7,-.1) to (2.7,1);

\draw
  (2.7,-.3)
  node
  {\scalebox{1}{$x$}};

\draw (4.4, 1)
 node
 {\scalebox{1}{$f(x)$}};

\draw (4.3, 3)
 node
 {\scalebox{1}{$r$}};

\draw (4.3, -3)
 node
 {\scalebox{1}{$-r$}};
 

\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (-4,-4) 
    rectangle
  (-3.05, 4);
  
\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (+4,-4) 
    rectangle
  (+3.7, 4);
  
\end{scope}



%%%%%%%%%%%%%%%


\begin{scope}[yshift=-9cm]


\begin{scope}
\clip
  (-3.05,3)
  rectangle
  (3.7, -2.98);






\draw[white, line width=7pt] 
  plot[smooth]
  coordinates
  {
    (-4,-3.9)
    (-3.5, -3.7)
    (-3.1, -3)
    (-2.5, -2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  
  
\draw plot[smooth]
  coordinates
  {
    (-4,-3.9)
    (-3.5, -3.7)
    (-3.1, -3)
    (-2.5, -2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  


\draw (4.4, 1)
 node
 {\scalebox{1}{$f(x)$}};

\draw (4.3, 3)
 node
 {\scalebox{1}{$r$}};

\draw (4.3, -3)
 node
 {\scalebox{1}{$-r$}};
 

\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (-4,-4) 
    rectangle
  (-3.05, 4);
  
\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (+4,-4) 
    rectangle
  (+3.7, 4);

\end{scope}  

\draw
  (.4, 3.5)
  node
  {$ 
    \color{black}
    X/\mathrm{gray} \;=\; S^1
  $};

\draw
  (.4, -3.5)
  node
  {$ 
    \color{black}
    X/\mathrm{gray} \;=\; S^1
  $};
  
\draw
  (4.2, .1)
  node[rotate=90]
  {$ 
    \color{black}
    \mathbb{R}/\mathrm{red}
    \;=\; S^1
  $};  
  
\draw
  (-3.6, .1)
  node[rotate=90]
  {$ 
    \color{black}
    \mathbb{R}/\mathrm{red}
    \;=\; S^1
  $};    

\draw[red, line width=2pt, draw opacity=.5]
  (-3.05,3)
  to
  (3.7, 3);

\draw[red, line width=2pt, draw opacity=.5]
  (-3.05,-2.98)
  to
  (3.7, -2.98);

\draw[line width=2pt]
  (-3.05, 3) to (-3.05, -2.98);

\draw[line width=2pt]
  (3.7, 3) to (3.7, -2.98);


\draw[red, ->, line width=2pt, draw opacity=.5]
  (.4-.1,3)
  to
  (.4+.1, 3);

\draw[red, ->, line width=2pt, draw opacity=.5]
  (.4-.1,-2.98)
  to
  (.4+.1, -2.98);

\draw[->, line width=2pt]
  (3.7,.3-.1)
  to
  (3.7,.3+.1);
  
\draw[->, line width=2pt]
  (-3.05,.3-.1)
  to
  (-3.05,.3+.1);
  
\draw
  (1.1,-1.3)
  node
  {$
    \underset{
      \raisebox{-2pt}{
        \small
        \color{black}
        unit winding
      }
    }{
    [f] = {\color{purple}+1} \in \pi^1(X/\mathrm{gray})
    }
  $};

\draw[fill=gray, draw=gray]
  (-3.05,3)
  circle (.08);

\draw[fill=gray, draw=gray]
  (-3.05,-2.98)
  circle (.08);
  
\draw[fill=gray, draw=gray]
  (3.7,3)
  circle (.08);  

\draw[fill=gray, draw=gray]
  (3.7,-2.98)
  circle (.08);
  


\end{scope}


\begin{scope}[xshift=10cm]

\draw[line width=1pt]
  (-4, 0)
  to
  (4,0);

\draw
  (-4.3,0)
  node
  {
    \colorbox{white}{$X$}
  };

\begin{scope}

\draw[gray, densely dashed]
  (-4, .5)
  to
  (4,.5);
  
\draw[gray, densely dashed]
  (-4, 1)
  to
  (4,1);
  
\draw[gray, densely dashed]
  (-4, 1.5)
  to
  (4,1.5);  

\draw[gray, densely dashed]
  (-4, 2)
  to
  (4,2);   
  
\draw[gray, densely dashed]
  (-4, 2.5)
  to
  (4,2.5);    
  
\draw[red, line width=2pt, densely dashed]
  (-4, 3)
  to
  (4,3);    

\draw[fill=red, fill opacity=.3, draw opacity=0]
  (4,3)
  rectangle
  (-4,4);
  
\draw[gray, densely dashed]
  (-4, 3.5)
  to
  (4,3.5);      
 
\draw[gray, densely dashed]
  (-4, 4)
  to
  (4,4);      
  
\end{scope}  
 
 
\begin{scope}[yscale=-1]

\draw[gray, densely dashed]
  (-4, .5)
  to
  (4,.5);
  
\draw[gray, densely dashed]
  (-4, 1)
  to
  (4,1);
  
\draw[gray, densely dashed]
  (-4, 1.5)
  to
  (4,1.5);  

\draw[gray, densely dashed]
  (-4, 2)
  to
  (4,2);   
  
\draw[gray, densely dashed]
  (-4, 2.5)
  to
  (4,2.5);    
  
\draw[red, line width=2pt, densely dashed]
  (-4, 3)
  to
  (4,3);  
  
\draw[fill=red, fill opacity=.3, draw opacity=0]
  (4,3)
  rectangle
  (-4,4);
  
  
\draw[gray, densely dashed]
  (-4, 3.5)
  to
  (4,3.5);      
 
\draw[gray, densely dashed]
  (-4, 4)
  to
  (4,4);      
  
\end{scope}   

\draw[white, line width=7pt] 
  plot[smooth]
  coordinates
  {
    (-4,+3.9)
    (-3.5, +3.7)
    (-3.1, +3)
    (-2.5, +2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  
  
\draw plot[smooth]
  coordinates
  {
    (-4,+3.9)
    (-3.5, +3.7)
    (-3.1, +3)
    (-2.5, +2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  
\draw[gray, densely dashed]
 (2.7,-.1) to (2.7,1);

\draw
  (2.7,-.3)
  node
  {\scalebox{1}{$x$}};

\draw (4.4, 1)
 node
 {\scalebox{1}{$f(x)$}};

\draw (4.3, 3)
 node
 {\scalebox{1}{$r$}};

\draw (4.3, -3)
 node
 {\scalebox{1}{$-r$}};
 

\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (-4,-4) 
    rectangle
  (-3.05, 4);
  
\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (+4,-4) 
    rectangle
  (+3.7, 4);
  
\end{scope}



%%%%%%%%%%%%%%%


\begin{scope}[xshift=10cm, yshift=-9cm]


\begin{scope}
\clip
  (-3.05,3)
  rectangle
  (3.7, -2.98);






\draw[white, line width=7pt] 
  plot[smooth]
  coordinates
  {
    (-4,+3.9)
    (-3.5, +3.7)
    (-3.1, +3)
    (-2.5, +2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  
  
\draw plot[smooth]
  coordinates
  {
    (-4,+3.9)
    (-3.5, +3.7)
    (-3.1, +3)
    (-2.5, +2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  


\draw (4.4, 1)
 node
 {\scalebox{1}{$f(x)$}};

\draw (4.3, 3)
 node
 {\scalebox{1}{$r$}};

\draw (4.3, -3)
 node
 {\scalebox{1}{$-r$}};
 

\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (-4,-4) 
    rectangle
  (-3.05, 4);
  
\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (+4,-4) 
    rectangle
  (+3.7, 4);

\end{scope}  

\draw
  (.4, 3.5)
  node
  {$ 
    \color{black}
    X/\mathrm{gray} \;=\; S^1
  $};

\draw
  (.4, -3.5)
  node
  {$ 
    \color{black}
    X/\mathrm{gray} \;=\; S^1
  $};
  
\draw
  (4.2, .1)
  node[rotate=90]
  {$ 
    \color{black}
    \mathbb{R}/\mathrm{red}
    \;=\; S^1
  $};  
  
\draw
  (-3.5, .1)
  node[rotate=90]
  {$ 
    \color{black}
    \mathbb{R}/\mathrm{red}
    \;=\; S^1
  $};    

\draw[red, line width=2pt, draw opacity=.5]
  (-3.05,3)
  to
  (3.7, 3);

\draw[red, line width=2pt, draw opacity=.5]
  (-3.05,-2.98)
  to
  (3.7, -2.98);

\draw[line width=2pt]
  (-3.05, 3) to (-3.05, -2.98);

\draw[line width=2pt]
  (3.7, 3) to (3.7, -2.98);


\draw[red, ->, line width=2pt, draw opacity=.5]
  (.4-.1,3)
  to
  (.4+.1, 3);

\draw[red, ->, line width=2pt, draw opacity=.5]
  (.4-.1,-2.98)
  to
  (.4+.1, -2.98);

\draw[->, line width=2pt]
  (3.7,.3-.1)
  to
  (3.7,.3+.1);
  
\draw[->, line width=2pt]
  (-3.05,.3-.1)
  to
  (-3.05,.3+.1);
  
\draw
  (1.1,-1.3)
  node
  {$
    \underset{
      \raisebox{-2pt}{
        \small
        \color{black}
        trivial winding
      }
    }{
    [f] = {\color{purple}0} \in \pi^1(X/\mathrm{gray})
    }
  $};


\draw[fill=gray, draw=gray]
  (-3.05,3)
  circle (.08);

\draw[fill=gray, draw=gray]
  (-3.05,-2.98)
  circle (.08);
  
\draw[fill=gray, draw=gray]
  (3.7,3)
  circle (.08);  

\draw[fill=gray, draw=gray]
  (3.7,-2.98)
  circle (.08);


\end{scope}

\end{tikzpicture}

> (graphics adapted from [[schreiber:New Foundations for TDA -- Cohomotopy|SS 22]])

Here the [[curve]] indicates the [[graph of a function|graph]] of $f$ and "gray" stands for the region $A_r \,\subset\, X$, while "red" stands for $\mathbb{R}^1 \setminus B_r$.

One sees on the left that if the cohomotopy class of $f$ at resolution $1/r$ is non-trivial, then there is at least one zero. 

{#IntuitivelyClear} In the situation on the right it is intuitively clear that a deformation of $f$ with magnitude smaller than $r$ may move the curve/[[graph of a function|graph]] away from the horizontal 0-line. In terms of [[homotopy theory]] this is the statement that in this case the [[quotient]]-map  $X/gray \to \mathbb{R}^1/red$ of $f$ admits a [[homotopy]] to the [[constant function]], which shows that its [[homotopy class]] (here: a [[cohomotopy]]-class) is trivial:

<center>
<img src="https://ncatlab.org/nlab/files/PersistentCohomotopy-TheIdea-220524b.gif" width="600">
</center>

> (graphics from [[schreiber:New Foundations for TDA -- Cohomotopy|SS22]])


\linebreak

## References

* {#FranekKrcal16} [[Peter Franek]], [[Marek Krčál]], _On Computability and Triviality of Well Groups_, Discrete Comput Geom **56** (2016) 126 ([arXiv:1501.03641](https://arxiv.org/abs/1501.03641), [doi:10.1007/s00454-016-9794-2](https://doi.org/10.1007/s00454-016-9794-2))

* {#FranekKrcal17} [[Peter Franek]], [[Marek Krčál]], _Persistence of Zero Sets_, Homology, Homotopy and Applications, **19** 2 (2017)  ([arXiv:1507.04310](https://arxiv.org/abs/1507.04310), [doi:10.4310/HHA.2017.v19.n2.a16](http://dx.doi.org/10.4310/HHA.2017.v19.n2.a16))


* {#FranekKrcal18} [[Peter Franek]], [[Marek Krčál]], [[Hubert Wagner]], _Solving equations and optimization problems with uncertainty_, J Appl. and Comput. Topology **1** (2018) 297 ([arxiv:1607.06344](https://arxiv.org/abs/1607.06344), [doi:10.1007/s41468-017-0009-6](https://doi.org/10.1007/s41468-017-0009-6))

Review:

* [[Peter Franek]], [[Marek Krčál]], _Cohomotopy groups capture robust Properties of Zero Sets via Homotopy Theory_, talk at [ACAT meeting 2015](https://www2.ist.ac.at/acat) ([pdf slides](https://www2.ist.ac.at/fileadmin/user_upload/events_pages/acat/ACAT2015_Marek_Krcal.pdf))

* {#SS22} [[Urs Schreiber]] on joint work with [[Hisham Sati]]: *[[schreiber:New Foundations for TDA -- Cohomotopy]]*, (May 2022)


[[!redirects persistent cohomotopy theory]]

[[!redirects persistent Cohomotopy]]
[[!redirects persistent Cohomotopy theory]]
