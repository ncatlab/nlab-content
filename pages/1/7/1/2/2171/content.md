
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

By a *braid group* &lbrack;[Artin (1925)](#Artin25)&rbrack; one means the [[group]] of joint continuous *motions* &lbrack;cf. [Goldsmith (1981)](#Goldsmith81)&rbrack; of a fixed number $n+1$ of non-coincident points in the [[plane]], from any fixed [[configuration space of points|configuration]] back to that fixed configuration. The  "[[worldlines]]" traced out by such points in space-time under such an operation look like a braid with $n+1$ strands, whence the name. 


<img src="/nlab/files/GenericBraidGroupElement-230205.jpg" width="280">


As with actual braids, here it is understood that two such operations are identified if they differ only by continuous deformations of the "strands" without breaking or intersecting these, hence that one identifies those such systems of [[worldlines]] which are [[isotopy|isotopic]] in $\mathbb{R}^3$. (This is just the kind of invariance considered for [[link diagrams]] --- such as under [[Reidemeister moves]] --- and in fact every link diagram may be obtained by "closing up" a braid diagram, in the evident sense.)


A quick way of saying this with  precision is to observe that 
a braid group is thus the *[[fundamental group]]* $\pi_1$ of a [[configuration space of points]] in the plane (see [below](#AsFundamentalGroupOfConfigurationSpace) for more). 

Here it makes a key difference whether:

* one considers the points in a configuration as *ordered* (labeled by numbers $1, \cdots, n+1$) in which case one speaks of the *[[pure braid group]]*, 

* or as indistinguishable (albeit in any case with distinct positions!) in which case one speaks of the *braid group* proper.

Namely, after traveling along a general braid $b$ the order of the given points may come out permuted by a [[permutation]] $\mathrm{perm}(b)$, and the braid is called *pure* precisely if this permutation is trivial:  

<img src="/nlab/files/BraidGroupFibration-230205.jpg" width="600">

More explicitly, braid groups admit [[finitely presented group|finite presentations]] by [[generators and relations]]. To these we now turn first:

\linebreak

## Definitions and characterizations
 {#DefinitionsAndCharacterizations}

* *[Via generators and relations](#ByGeneratorsAndRelations)*

* *[As the fundamental group of a configuration space of points](#AsFundamentalGroupOfConfigurationSpace)*

* *[As mapping class group of punctured surfaces](#BraidGroupsAsMappingClassGroupsOfPuncturedSurfaces)*

* *[As automorphisms of a free group](#AsAutomorphismsOfAFreeGroup)*


### Via generators and relations
 {#ByGeneratorsAndRelations}


#### Presentation of general braids
 {#PresentationOfGeneralBraids}

We discuss the braid group as  a [[finitely generated group]]
([Artin 1925, (5)-(6)](#Artin25); [Artin 1947, (18)-(19)](#Artin47);
review in, e.g.:  [Fox & Neuwirth 1962, §7](#FoxNeuwirth62)):

\begin{definition}\label{ArtinPresentation}
**(Artin presentation)**

The **Artin braid group**, $Br({n+1})$, on $n+1$ strands is the [[finitely generated group]] given via [[generators and relations]] by (this and the following graphics are taken from [[schreiber:Topological Quantum Gates in Homotopy Type Theory|Myers et al. (2023)]]):

* {#ArtinGenerators} generators: 

  \[
    \label{ArtinGenerators}
    b_i\;\; i = 1, \ldots, n
  \]

\begin{tikzcd}
b_i
\;:=\;
\color{orange}
\left[
\color{black}
\raisebox{6pt}{
\begin{tikzpicture}

\begin{scope}[shift={(-1.6,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\draw[line width=1.4]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);

\draw[line width=4.5, white]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\draw[line width=1.4]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);

\begin{scope}[shift={(+1.6,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\draw 
  (-2.1, -1.3) node {\color{blue}\scalebox{.5}{$1$}};

\draw 
  (-1.1, -1.3) node {\color{blue}\scalebox{.5}{$i\!-\!1$}};

\draw 
  (-.4, -1.3) node {\color{blue}\scalebox{.5}{$i$}};

\draw 
  (+.35, -1.3) node {\color{blue}\scalebox{.5}{$i\!+\!1$}};

\draw 
  (+1.1, -1.3) node {\color{blue}\scalebox{.5}{$i\!+\!2$}};

\draw 
  (+2.1, -1.3) node {\color{blue}\scalebox{.5}{$n+1$}};

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}


\begin{tikzcd}
b_i^{-1}
\;:=\;
\color{orange}
\left[
\color{black}
\raisebox{6pt}{
\begin{tikzpicture}

\begin{scope}[shift={(-1.6,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\draw[line width=1.4]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);

\draw[line width=4.5, white]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);
\draw[line width=1.4]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);

\begin{scope}[shift={(+1.6,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\draw 
  (-2.1, -1.3) node {\color{blue}\scalebox{.5}{$1$}};

\draw 
  (-1.1, -1.3) node {\color{blue}\scalebox{.5}{$i\!-\!1$}};

\draw 
  (-.4, -1.3) node {\color{blue}\scalebox{.5}{$i$}};

\draw 
  (+.35, -1.3) node {\color{blue}\scalebox{.5}{$i\!+\!1$}};

\draw 
  (+1.1, -1.3) node {\color{blue}\scalebox{.5}{$i\!+\!2$}};

\draw 
  (+2.1, -1.3) node {\color{blue}\scalebox{.5}{$n+1$}};

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}




* relations I: 

  \[
    \label{ArtinRelations}
    \underset{
      i+1 \lt j    
    }{\forall}
    \;\;\;
     b_i \cdot b_j 
     \;=\;  
     b_j \cdot b_i
  \]

\begin{tikzcd}
\color{orange}
\left[
\color{black}
\raisebox{-20pt}{
\begin{tikzpicture}

\begin{scope}

\begin{scope}[shift={(-1.6,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\draw[line width=1.4]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);

\draw[line width=4.5, white]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\draw[line width=1.4]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);

\begin{scope}[shift={(+1.6,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}


\begin{scope}[shift={(3.2,0)}]
\draw[line width=1.4]
  (-.35,-1)
  -- 
  (-.35,1);

\draw[line width=1.4]
  (+.35,-1) 
  --
  (+.35,1);
\end{scope}

\begin{scope}[shift={(+4.8,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}


\draw 
  (-2.1, -1.3) node {\color{blue}\scalebox{.5}{$1$}};

\draw 
  (-1.1, -1.3) node {\color{blue}\scalebox{.5}{$i\!-\!1$}};

\draw 
  (-.4, -1.3) node {\color{blue}\scalebox{.5}{$i$}};

\draw 
  (+.35, -1.3) node {\color{blue}\scalebox{.5}{$i\!+\!1$}};

\draw 
  (+1.1, -1.3) node {\color{blue}\scalebox{.5}{$i\!+\!2$}};

\draw 
  (+2.1, -1.3) node {\color{blue}\scalebox{.5}{$j\!-\!1$}};

\draw 
  (+2.8, -1.3) node {\color{blue}\scalebox{.5}{$j$}};

\draw 
  (+3.5, -1.3) node {\color{blue}\scalebox{.5}{$j\!+\!1$}};

\draw 
  (+4.3, -1.3) node {\color{blue}\scalebox{.5}{$j\!+\!2$}};

\draw 
  (+5.3, -1.3) node {\color{blue}\scalebox{.5}{$n\!+\!1$}};

\end{scope}



\begin{scope}[shift={(0,2)}]

\begin{scope}[shift={(-1.6,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\begin{scope}
\draw[line width=1.4]
  (-.35,-1)
  -- 
  (-.35,1);

\draw[line width=1.4]
  (+.35,-1) 
  --
  (+.35,1);
\end{scope}

\begin{scope}[shift={(+1.6,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}


\begin{scope}[shift={(3.2,0)}]
\draw[line width=1.4]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);
\draw[line width=4.5, white]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\draw[line width=1.4]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\end{scope}

\begin{scope}[shift={(+4.8,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\end{scope}

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\;\;\;\;\; 
  =
\;\;\;\;\;
\color{orange}
\left[
\color{black}
\raisebox{-20pt}{
\begin{tikzpicture}


\begin{scope}[shift={(0,2)}]

\begin{scope}

\begin{scope}[shift={(-1.6,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\draw[line width=1.4]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);

\draw[line width=4.5, white]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\draw[line width=1.4]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);

\begin{scope}[shift={(+1.6,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}


\begin{scope}[shift={(3.2,0)}]
\draw[line width=1.4]
  (-.35,-1)
  -- 
  (-.35,1);

\draw[line width=1.4]
  (+.35,-1) 
  --
  (+.35,1);
\end{scope}

\begin{scope}[shift={(+4.8,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\end{scope}

\end{scope}


\begin{scope}[shift={(0,0)}]

\begin{scope}[shift={(-1.6,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\begin{scope}
\draw[line width=1.4]
  (-.35,-1)
  -- 
  (-.35,1);

\draw[line width=1.4]
  (+.35,-1) 
  --
  (+.35,1);
\end{scope}

\begin{scope}[shift={(+1.6,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}


\begin{scope}[shift={(3.2,0)}]
\draw[line width=1.4]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);
\draw[line width=4.5, white]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\draw[line width=1.4]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\end{scope}

\begin{scope}[shift={(+4.8,0)}]
\draw[line width=1.4]
  (-.5,1) to (-.5,-1);
\draw[line width=1.2]
  (+.5,1) to (+.5,-1);
\draw
  (-0,-.1) node {$\mathclap{\cdots}$};
\end{scope}


\draw 
  (-2.1, -1.3) node {\color{blue}\scalebox{.5}{$1$}};

\draw 
  (-1.1, -1.3) node {\color{blue}\scalebox{.5}{$i\!-\!1$}};

\draw 
  (-.4, -1.3) node {\color{blue}\scalebox{.5}{$i$}};

\draw 
  (+.35, -1.3) node {\color{blue}\scalebox{.5}{$i\!+\!1$}};

\draw 
  (+1.1, -1.3) node {\color{blue}\scalebox{.5}{$i\!+\!2$}};

\draw 
  (+2.1, -1.3) node {\color{blue}\scalebox{.5}{$j\!-\!1$}};

\draw 
  (+2.8, -1.3) node {\color{blue}\scalebox{.5}{$j$}};

\draw 
  (+3.5, -1.3) node {\color{blue}\scalebox{.5}{$j\!+\!1$}};

\draw 
  (+4.3, -1.3) node {\color{blue}\scalebox{.5}{$j\!+\!2$}};

\draw 
  (+5.3, -1.3) node {\color{blue}\scalebox{.5}{$n\!+\!1$}};


\end{scope}

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}

\linebreak

* {#2ndArtinRelation} relations II ([[Yang-Baxter equation]])

  \[
    \underset{
      1 \leq i \lt n    
    }{\forall}
    \;\;\;
    b_i \cdot b_{i+1} \cdot b_i 
    \;=\;
    b_{i+1} \cdot b_i \cdot b_{i+1}
  \]

\begin{tikzcd}
\color{orange}
\left[
\color{black}
\raisebox{-24pt}{
\begin{tikzpicture}[yscale=.5]

\begin{scope}[shift={(-1.6,0)}]
\draw[line width=1.4]
  (-.5,5) to (-.5,-1);
\draw[line width=1.2]
  (+.5,5) to (+.5,-1);
\draw
  (-0,2.2) node {$\mathclap{\cdots}$};
\end{scope}

\begin{scope}[shift={(0,4)}]
\draw[line width=1.4]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);

\draw[line width=4.5, white]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\draw[line width=1.4]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\end{scope}

\draw[line width=1.4]
  (-.35,3) 
  --
  (-.35,1);

\draw[line width=1.4]
  (+1.05,5) 
  --
  (+1.05,3);


\begin{scope}[shift={(.7,2)}]
\draw[line width=1.4]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);

\draw[line width=4.5, white]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\draw[line width=1.4]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\end{scope}


\begin{scope}
\draw[line width=1.4]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);

\draw[line width=4.5, white]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\draw[line width=1.4]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\end{scope}

 \draw[line width=1.4]
   (1.05,1) to (1.05,-1);

\begin{scope}[shift={(+2.4,0)}]
\draw[line width=1.4]
  (-.5,5) to (-.5,-1);
\draw[line width=1.2]
  (+.5,5) to (+.5,-1);
\draw
  (-0,2.2) node {$\mathclap{\cdots}$};
\end{scope}

\draw 
  (-2.1, -1.4) node {\color{blue}\scalebox{.5}{$1$}};

\draw 
  (-1.1, -1.4) node {\color{blue}\scalebox{.5}{$i\!-\!1$}};

\draw 
  (-.4, -1.4) node {\color{blue}\scalebox{.5}{$i$}};

\draw 
  (+.35, -1.4) node {\color{blue}\scalebox{.5}{$i\!+\!1$}};

\draw 
  (+1.1, -1.4) node {\color{blue}\scalebox{.5}{$i\!+\!2$}};

\draw 
  (+1.9, -1.4) node {\color{blue}\scalebox{.5}{$i\!+\!3$}};

\draw 
  (+2.9, -1.4) node {\color{blue}\scalebox{.5}{$n\!+\!1$}};
\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\;\;\;\;\;
=
\;\;\;\;
\color{orange}
\left[
\color{black}
\raisebox{-24pt}{
\begin{tikzpicture}[yscale=.5]

\begin{scope}[shift={(-1.6,0)}]
\draw[line width=1.4]
  (-.5,5) to (-.5,-1);
\draw[line width=1.2]
  (+.5,5) to (+.5,-1);
\draw
  (-0,2.2) node {$\mathclap{\cdots}$};
\end{scope}

\begin{scope}[shift={(.7,4)}]
\draw[line width=1.4]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);

\draw[line width=4.5, white]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\draw[line width=1.4]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\end{scope}


\draw[line width=1.4]
  (1.05,3) 
  --
  (1.05,1);

\draw[line width=1.4]
  (-.35,5) 
  --
  (-.35,3);


\draw[line width=1.4]
  (-.35,1) 
  -- 
  (-.35,-1);


\begin{scope}[shift={(0,2)}]
\draw[line width=1.4]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);

\draw[line width=4.5, white]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\draw[line width=1.4]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\end{scope}


\begin{scope}[shift={(.7,0)}]
\draw[line width=1.4]
  (-.35,-1) 
  .. controls (-.35,0) and (+.35,0)  .. 
  (+.35,1);

\draw[line width=4.5, white]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\draw[line width=1.4]
  (+.35,-1) 
  .. controls (+.35,0) and (-.35,0)  .. 
  (-.35,1);
\end{scope}


\begin{scope}[shift={(+2.4,0)}]
\draw[line width=1.4]
  (-.5,5) to (-.5,-1);
\draw[line width=1.2]
  (+.5,5) to (+.5,-1);
\draw
  (-0,2.2) node {$\mathclap{\cdots}$};
\end{scope}

\draw 
  (-2.1, -1.4) node {\color{blue}\scalebox{.5}{$1$}};

\draw 
  (-1.1, -1.4) node {\color{blue}\scalebox{.5}{$i\!-\!1$}};

\draw 
  (-.4, -1.4) node {\color{blue}\scalebox{.5}{$i$}};

\draw 
  (+.35, -1.4) node {\color{blue}\scalebox{.5}{$i\!+\!1$}};

\draw 
  (+1.1, -1.4) node {\color{blue}\scalebox{.5}{$i\!+\!2$}};

\draw 
  (+1.9, -1.4) node {\color{blue}\scalebox{.5}{$i\!+\!3$}};

\draw 
  (+2.9, -1.4) node {\color{blue}\scalebox{.5}{$n\!+\!1$}};
\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}


\end{definition}


#### Presentation of pure braids
 {#PresentationOfPureBraids}

Similarly, the [[pure braid group]] has a [[finitely presented group|finite presentation]].

One possible set of generators (also originally considered by Artin) are the "weave" braids where one strands lassos exactly one other strand:


\begin{tikzcd}
b_{ij}
\;\;
  :=
\;\;
\color{orange}
\left[
\color{black}
\raisebox{5pt}{
\begin{tikzpicture}[yscale=1, xscale=1.3]

\draw[line width=1.4]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);


\begin{scope}[shift={(-1.4,0)}]
\draw[line width=1.4]
  (-.3,1) to (-.3,-1);
\draw[line width=1.4]
  (+.4,1) to (+.4,-1);
\draw
  (+.05,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\begin{scope}[shift={(-0,0)}]
\draw[line width=1.4]
  (-.6,1) to (-.6,-1);
\draw[line width=1.4]
  (-.4,1) to (-.4,-1);
\draw[line width=4, white]
  (+.4,1) to (+.4,-1);
\draw[line width=1.4]
  (+.4,1) to (+.4,-1);
\draw[line width=4, white]
  (+.2,1) to (+.2,-1);
\draw[line width=1.4]
  (+.2,1) to (+.2,-1);
\draw
  (-.1,-.1) node {$\mathclap{\cdots}$};
\end{scope}


\begin{scope}[shift={(+.8,0)}]
\draw[line width=1.4]
  (-.4,1) to (-.4,-1);
\draw[line width=1.2]
  (+.3,1) to (+.3,-1);
\draw
  (-.01,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\draw[line width=4, white]
  (-.8,-1)
  .. controls   (-.8, -.5)  and (.55, -.5)  ..
  (.55,0);
\draw[line width=1.4]
  (-.8,-1)
  .. controls   (-.8, -.5)  and (.55, -.5)  ..
  (.55,0);

\begin{scope}
\clip
  (-.9,0) rectangle (+.3,1.2); 
\draw[line width=4, white]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);
\draw[line width=1.4]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);
\end{scope}

\draw
  (-.8,-1.3) node {
    \scalebox{.7}{
      \color{blue}
      $i$
    }
  };

\draw
  (+.4,-1.3) node {
    \scalebox{.7}{
      \color{blue}
      $j$
    }
  };

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\;\;
=
\;\;
\color{orange}
\left[
\color{black}
\raisebox{5pt}{
\begin{tikzpicture}[yscale=-1, xscale=-1.3]

\draw[line width=1.4]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);


\begin{scope}[shift={(-1.4,0)}]
\draw[line width=1.4]
  (-.3,1) to (-.3,-1);
\draw[line width=1.4]
  (+.4,1) to (+.4,-1);
\draw
  (+.05,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\begin{scope}[shift={(-0,0)}]
\draw[line width=1.4]
  (-.6,1) to (-.6,-1);
\draw[line width=1.4]
  (-.4,1) to (-.4,-1);
\draw[line width=4, white]
  (+.4,1) to (+.4,-1);
\draw[line width=1.4]
  (+.4,1) to (+.4,-1);
\draw[line width=4, white]
  (+.2,1) to (+.2,-1);
\draw[line width=1.4]
  (+.2,1) to (+.2,-1);
\draw
  (-.1,-.1) node {$\mathclap{\cdots}$};
\end{scope}


\begin{scope}[shift={(+.8,0)}]
\draw[line width=1.4]
  (-.4,1) to (-.4,-1);
\draw[line width=1.2]
  (+.3,1) to (+.3,-1);
\draw
  (-.01,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\draw[line width=4, white]
  (-.8,-1)
  .. controls   (-.8, -.5)  and (.55, -.5)  ..
  (.55,0);
\draw[line width=1.4]
  (-.8,-1)
  .. controls   (-.8, -.5)  and (.55, -.5)  ..
  (.55,0);

\begin{scope}
\clip
  (-.9,0) rectangle (+.3,1.2); 
\draw[line width=4, white]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);
\draw[line width=1.4]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);
\end{scope}

\draw
  (-.8,+1.3) node {
    \scalebox{-.7}{
      \color{blue}
      $j$
    }
  };

\draw
  (+.4,+1.3) node {
    \scalebox{-.7}{
      \color{blue}
      $i$
    }
  };

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}


{#LeeRelationsForPureBraidGroup} In terms of these generators, the [[pure braid group]] is obained by quotienting out the following relations --- an optimization of Artin's original pure braid relations, due to [Lee (2010, Thm. 1.1, Rem. 3.1)](#Lee10):


<img src="/nlab/files/PureBraidGroupPresentation-230205b.jpg" width="830">






\begin{tikzcd}
\color{orange}
\left[
\color{black}
\raisebox{7pt}{
\begin{tikzpicture}[line width=1.2]

\begin{scope}[shift={(0,+1)}]

\begin{scope}[shift={(-2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-2,-1) to (-2,1);


\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,-1) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,1);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(2,0)}]
\draw[line width=4, white]
  (-2,-1)
    --
  (-2,-.8)
    .. controls (-2,-.4) and (-.85, -.4) ..
  (-.85, 0)
    .. controls (-.85, +.4) and (-2, +.4) ..
  (-2,+.8)
    --
  (-2, 1);
\draw
  (-2,-1)
    --
  (-2,-.8)
    .. controls (-2,-.4) and (-.85, -.4) ..
  (-.85, 0)
    .. controls (-.85, +.4) and (-2, +.4) ..
  (-2,+.8)
    --
  (-2, 1);
\end{scope}

\draw[line width=4, white]
  (+1,0) to (+1,1);
\draw 
  (+1,0) to (+1,1);

\end{scope}



\begin{scope}[shift={(0,-1)}]

\begin{scope}[shift={(-2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,-1) to (-1,0);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,1);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (-2,-1)
    --
  (-2,-.8)
    .. controls (-2,-.4) and (-.85, -.4) ..
  (-.85, 0)
    .. controls (-.85, +.4) and (-2, +.4) ..
  (-2,+.8)
    --
  (-2, 1);
\draw
  (-2,-1)
    --
  (-2,-.8)
    .. controls (-2,-.4) and (-.85, -.4) ..
  (-.85, 0)
    .. controls (-.85, +.4) and (-2, +.4) ..
  (-2,+.8)
    --
  (-2, 1);

\draw[line width=4, white]
  (-1,0) to (-1,1);
\draw 
  (-1,0) to (-1,1);

\end{scope}

\node
  at (-2,-2.4) {
    \color{blue}
    $i$
  }; 

\node
  at (-1,-2.4) {
    \color{blue}
    $j$
  }; 

\node
  at (0,-2.4) {
    \color{blue}
    $k$
  }; 

\node
  at (+1,-2.4) {
    \color{blue}
    $l$
  }; 


\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\;\;\;
=
\;\;\;
\color{orange}
\left[
\color{black}
\raisebox{7pt}{
\begin{tikzpicture}[line width=1.2]

\begin{scope}[shift={(0,-1)}]

\begin{scope}[shift={(-2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-2,-1) to (-2,1);


\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,-1) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,1);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(2,0)}]
\draw[line width=4, white]
  (-2,-1)
    --
  (-2,-.8)
    .. controls (-2,-.4) and (-.85, -.4) ..
  (-.85, 0)
    .. controls (-.85, +.4) and (-2, +.4) ..
  (-2,+.8)
    --
  (-2, 1);
\draw
  (-2,-1)
    --
  (-2,-.8)
    .. controls (-2,-.4) and (-.85, -.4) ..
  (-.85, 0)
    .. controls (-.85, +.4) and (-2, +.4) ..
  (-2,+.8)
    --
  (-2, 1);
\end{scope}

\draw[line width=4, white]
  (+1,0) to (+1,1);
\draw 
  (+1,0) to (+1,1);

\end{scope}



\begin{scope}[shift={(0,+1)}]

\begin{scope}[shift={(-2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,-1) to (-1,0);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,1);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (-2,-1)
    --
  (-2,-.8)
    .. controls (-2,-.4) and (-.85, -.4) ..
  (-.85, 0)
    .. controls (-.85, +.4) and (-2, +.4) ..
  (-2,+.8)
    --
  (-2, 1);
\draw
  (-2,-1)
    --
  (-2,-.8)
    .. controls (-2,-.4) and (-.85, -.4) ..
  (-.85, 0)
    .. controls (-.85, +.4) and (-2, +.4) ..
  (-2,+.8)
    --
  (-2, 1);

\draw[line width=4, white]
  (-1,0) to (-1,1);
\draw 
  (-1,0) to (-1,1);

\end{scope}

\node
  at (-2,-2.4) {
    \color{blue}
    $i$
  }; 

\node
  at (-1,-2.4) {
    \color{blue}
    $j$
  }; 

\node
  at (0,-2.4) {
    \color{blue}
    $k$
  }; 

\node
  at (+1,-2.4) {
    \color{blue}
    $l$
  }; 


\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}






\begin{tikzcd}
\color{orange}
\left[
\color{black}
\raisebox{5pt}{
\begin{tikzpicture}[line width=1.2]

\begin{scope}[shift={(0,-1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,-1) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,0) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (+1,-1) 
  -- 
  (+1,-.8)
   .. controls (+1, -.4) and (-.15, -.4) ..
  (-.15, 0)
   .. controls (-.15, +.4) and (+1, +.4) ..
  (+1,+.8)
  -- 
  (+1,+1);
\draw 
  (+1,-1) 
  -- 
  (+1,-.8)
   .. controls (+1, -.4) and (-.15, -.4) ..
  (-.15, 0)
   .. controls (-.15, +.4) and (+1, +.4) ..
  (+1,+.8)
  -- 
  (+1,+1);

\draw[line width=4, white]
  (0,-1) to (0,0);
\draw 
  (0,-1) to (0,0);


\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\end{scope}


\begin{scope}[shift={(0,1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,0);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,0);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (-1,-1) 
    --
  (-1, -.8)
    .. controls (-1, -.4) and (1.15, -.4) ..
  (+1.15,0)
    .. controls (1.15, .4) and (-1, .4) ..
  (-1, +.8)
    --
  (-1,+1);
\draw 
  (-1,-1) 
    --
  (-1, -.8)
    .. controls (-1, -.4) and (1.15, -.4) ..
  (+1.15,0)
    .. controls (1.15, .4) and (-1, .4) ..
  (-1, +.8)
    --
  (-1,+1);

\draw[line width=4, white]
  (0,0) to (0,1);
\draw
  (0,0) to (0,1);

\draw[line width=4, white]
  (+1,0) to (+1,1);
\draw
  (+1,0) to (+1,1);

\end{scope}

\node
  at (-1,-2.4) 
  {
    \scalebox{.9}{
      \color{blue}
      $r$
    }
  };

\node
  at (-0,-2.4) 
  {
    \scalebox{.9}{
      \color{blue}
      $i$
    }
  };

\node
  at (+1,-2.4) 
  {
    \scalebox{.9}{
      \color{blue}
      $j$
    }
  };

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\;\;
=
\;\;
\color{orange}
\left[
\color{black}
\raisebox{5pt}{
\begin{tikzpicture}[line width=1.2]

\begin{scope}[shift={(0,+1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,-1) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,0) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (+1,-1) 
  -- 
  (+1,-.8)
   .. controls (+1, -.4) and (-.15, -.4) ..
  (-.15, 0)
   .. controls (-.15, +.4) and (+1, +.4) ..
  (+1,+.8)
  -- 
  (+1,+1);
\draw 
  (+1,-1) 
  -- 
  (+1,-.8)
   .. controls (+1, -.4) and (-.15, -.4) ..
  (-.15, 0)
   .. controls (-.15, +.4) and (+1, +.4) ..
  (+1,+.8)
  -- 
  (+1,+1);

\draw[line width=4, white]
  (0,-1) to (0,0);
\draw 
  (0,-1) to (0,0);


\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\end{scope}


\begin{scope}[shift={(0,-1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,0);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,0);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (-1,-1) 
    --
  (-1, -.8)
    .. controls (-1, -.4) and (1.15, -.4) ..
  (+1.15,0)
    .. controls (1.15, .4) and (-1, .4) ..
  (-1, +.8)
    --
  (-1,+1);
\draw 
  (-1,-1) 
    --
  (-1, -.8)
    .. controls (-1, -.4) and (1.15, -.4) ..
  (+1.15,0)
    .. controls (1.15, .4) and (-1, .4) ..
  (-1, +.8)
    --
  (-1,+1);

\draw[line width=4, white]
  (0,0) to (0,1);
\draw
  (0,0) to (0,1);

\draw[line width=4, white]
  (+1,0) to (+1,1);
\draw
  (+1,0) to (+1,1);

\end{scope}

\node
  at (-1,-2.4) 
  {
    \scalebox{.9}{
      \color{blue}
      $r$
    }
  };

\node
  at (-0,-2.4) 
  {
    \scalebox{.9}{
      \color{blue}
      $i$
    }
  };

\node
  at (+1,-2.4) 
  {
    \scalebox{.9}{
      \color{blue}
      $j$
    }
  };

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}







\begin{tikzcd}
\color{orange}
\left[
\color{black}
\raisebox{5pt}{
\begin{tikzpicture}[line width=1.2]

\begin{scope}[shift={(0,-1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,0) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (1,-1) to (1,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(-1,0)}]
\draw[line width=4, white]
  (+1,-1) 
  -- 
  (+1,-.8)
   .. controls (+1, -.4) and (-.15, -.4) ..
  (-.15, 0)
   .. controls (-.15, +.4) and (+1, +.4) ..
  (+1,+.8)
  -- 
  (+1,+1);
\draw
  (+1,-1) 
  -- 
  (+1,-.8)
   .. controls (+1, -.4) and (-.15, -.4) ..
  (-.15, 0)
   .. controls (-.15, +.4) and (+1, +.4) ..
  (+1,+.8)
  -- 
  (+1,+1);

\draw[line width=4, white]
  (0,-1) to (0,0);
\draw 
  (0,-1) to (0,0);


\end{scope}

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\end{scope}


\begin{scope}[shift={(0,1)}, scale=-1]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,0);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,0);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (-1,-1) 
    --
  (-1, -.8)
    .. controls (-1, -.4) and (1.15, -.4) ..
  (+1.15,0)
    .. controls (1.15, .4) and (-1, .4) ..
  (-1, +.8)
    --
  (-1,+1);
\draw 
  (-1,-1) 
    --
  (-1, -.8)
    .. controls (-1, -.4) and (1.15, -.4) ..
  (+1.15,0)
    .. controls (1.15, .4) and (-1, .4) ..
  (-1, +.8)
    --
  (-1,+1);

\draw[line width=4, white]
  (0,0) to (0,1);
\draw
  (0,0) to (0,1);

\draw[line width=4, white]
  (+1,0) to (+1,1);
\draw
  (+1,0) to (+1,1);

\end{scope}

\node
  at (-1,-2.4) 
  {
    \scalebox{.9}{
      \color{blue}
      $r$
    }
  };

\node
  at (-0,-2.4) 
  {
    \scalebox{.9}{
      \color{blue}
      $i$
    }
  };

\node
  at (+1,-2.4) 
  {
    \scalebox{.9}{
      \color{blue}
      $j$
    }
  };

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\;\;
=
\;\;
\color{orange}
\left[
\color{black}
\raisebox{5pt}{
\begin{tikzpicture}[line width=1.2]

\begin{scope}[shift={(0,+1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,0) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (1,-1) to (1,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(-1,0)}]
\draw[line width=4, white]
  (+1,-1) 
  -- 
  (+1,-.8)
   .. controls (+1, -.4) and (-.15, -.4) ..
  (-.15, 0)
   .. controls (-.15, +.4) and (+1, +.4) ..
  (+1,+.8)
  -- 
  (+1,+1);
\draw
  (+1,-1) 
  -- 
  (+1,-.8)
   .. controls (+1, -.4) and (-.15, -.4) ..
  (-.15, 0)
   .. controls (-.15, +.4) and (+1, +.4) ..
  (+1,+.8)
  -- 
  (+1,+1);

\draw[line width=4, white]
  (0,-1) to (0,0);
\draw 
  (0,-1) to (0,0);


\end{scope}

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\end{scope}


\begin{scope}[shift={(0,-1)}, scale=-1]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,0);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,0);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (-1,-1) 
    --
  (-1, -.8)
    .. controls (-1, -.4) and (1.15, -.4) ..
  (+1.15,0)
    .. controls (1.15, .4) and (-1, .4) ..
  (-1, +.8)
    --
  (-1,+1);
\draw 
  (-1,-1) 
    --
  (-1, -.8)
    .. controls (-1, -.4) and (1.15, -.4) ..
  (+1.15,0)
    .. controls (1.15, .4) and (-1, .4) ..
  (-1, +.8)
    --
  (-1,+1);

\draw[line width=4, white]
  (0,0) to (0,1);
\draw
  (0,0) to (0,1);

\draw[line width=4, white]
  (+1,0) to (+1,1);
\draw
  (+1,0) to (+1,1);

\end{scope}

\node
  at (-1,-2.4) 
  {
    \scalebox{.9}{
      \color{blue}
      $r$
    }
  };

\node
  at (-0,-2.4) 
  {
    \scalebox{.9}{
      \color{blue}
      $i$
    }
  };

\node
  at (+1,-2.4) 
  {
    \scalebox{.9}{
      \color{blue}
      $j$
    }
  };

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}











\begin{tikzcd}
\color{orange}
\left[
\color{black}
\raisebox{8pt}{
\begin{tikzpicture}[line width=1.2]

\begin{scope}[shift={(0,+1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,0) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (+1, -1)
    --
  (+1, -.8)
    .. controls (+1, -.4) and (-1.14, -.4) ..
  (-1.15, 0)
    .. controls (-1.15, .4) and (+1, .4) ..
  (+1, .8)
    --
  (+1, 1);
\draw
  (+1, -1)
    --
  (+1, -.8)
    .. controls (+1, -.4) and (-1.14, -.4) ..
  (-1.15, 0)
    .. controls (-1.15, .4) and (+1, .4) ..
  (+1, .8)
    --
  (+1, 1);

\draw[line width=4, white]
  (-1,-1) to (-1,0);
\draw 
  (-1,-1) to (-1,0);


\end{scope}


\begin{scope}[shift={(0,-1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,-.35) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,.4);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (0,-1)
    --
  (0,-.8)
    .. controls (0,-.6) and (-1.15, -.6) ..
  (-1.15, -.4)
    .. controls (-1.15, 0) and (+1.15, 0) ..
  (+1.15, +.4)
    .. controls (+1.15, .6) and (0, .6) ..
  (0, +.8)
    --
  (0,1);
\draw
  (0,-1)
    --
  (0,-.8)
    .. controls (0,-.6) and (-1.15, -.6) ..
  (-1.15, -.4)
    .. controls (-1.15, 0) and (+1.15, 0) ..
  (+1.15, +.4)
    .. controls (+1.15, .6) and (0, .6) ..
  (0, +.8)
    --
  (0,1);

\draw[line width=4, white]
  (-1,-1) to (-1,-.35);
\draw 
  (-1,-1) to (-1,-.35);

\draw[line width=4, white]
  (+1, .4) to (+1, 1);
\draw 
  (+1, .4) to (+1, 1);

\end{scope}

\node
  at (-1, -2.4) {
    \color{blue}
    $r$
  };

\node
  at (0, -2.4) {
    \color{blue}
    $i$
  };

\node
  at (+1, -2.4) {
    \color{blue}
    $j$
  };


\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\;\;\;
=
\;\;\;
\color{orange}
\left[
\color{black}
\raisebox{8pt}{
\begin{tikzpicture}[line width=1.2]

\begin{scope}[shift={(0,-1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,0) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (+1, -1)
    --
  (+1, -.8)
    .. controls (+1, -.4) and (-1.14, -.4) ..
  (-1.15, 0)
    .. controls (-1.15, .4) and (+1, .4) ..
  (+1, .8)
    --
  (+1, 1);
\draw
  (+1, -1)
    --
  (+1, -.8)
    .. controls (+1, -.4) and (-1.14, -.4) ..
  (-1.15, 0)
    .. controls (-1.15, .4) and (+1, .4) ..
  (+1, .8)
    --
  (+1, 1);

\draw[line width=4, white]
  (-1,-1) to (-1,0);
\draw 
  (-1,-1) to (-1,0);

\end{scope}


\begin{scope}[shift={(0,+1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,-.35) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,.4);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (0,-1)
    --
  (0,-.8)
    .. controls (0,-.6) and (-1.15, -.6) ..
  (-1.15, -.4)
    .. controls (-1.15, 0) and (+1.15, 0) ..
  (+1.15, +.4)
    .. controls (+1.15, .6) and (0, .6) ..
  (0, +.8)
    --
  (0,1);
\draw
  (0,-1)
    --
  (0,-.8)
    .. controls (0,-.6) and (-1.15, -.6) ..
  (-1.15, -.4)
    .. controls (-1.15, 0) and (+1.15, 0) ..
  (+1.15, +.4)
    .. controls (+1.15, .6) and (0, .6) ..
  (0, +.8)
    --
  (0,1);

\draw[line width=4, white]
  (-1,-1) to (-1,-.35);
\draw 
  (-1,-1) to (-1,-.35);

\draw[line width=4, white]
  (+1, .4) to (+1, 1);
\draw 
  (+1, .4) to (+1, 1);

\end{scope}

\node
  at (-1, -2.4) {
    \color{blue}
    $r$
  };

\node
  at (0, -2.4) {
    \color{blue}
    $i$
  };

\node
  at (+1, -2.4) {
    \color{blue}
    $j$
  };


\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}








\begin{tikzcd}
\color{orange}
\left[
\color{black}
\raisebox{8pt}{

\begin{tikzpicture}[line width=1.2]

\begin{scope}[shift={(0,+1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,0) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+2,-1) to (+2,1);

\begin{scope}[shift={(+3,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}



\draw[line width=4, white]
  (+1, -1)
    --
  (+1, -.8)
    .. controls (+1, -.4) and (-1.14, -.4) ..
  (-1.15, 0)
    .. controls (-1.15, .4) and (+1, .4) ..
  (+1, .8)
    --
  (+1, 1);
\draw
  (+1, -1)
    --
  (+1, -.8)
    .. controls (+1, -.4) and (-1.14, -.4) ..
  (-1.15, 0)
    .. controls (-1.15, .4) and (+1, .4) ..
  (+1, .8)
    --
  (+1, 1);

\draw[line width=4, white]
  (-1,-1) to (-1,0);
\draw 
  (-1,-1) to (-1,0);

\end{scope}

\begin{scope}[shift={(0,-1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,-1) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,1);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(+3,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (+2, -1)
    --
  (+2, -.8)
    .. controls (2, -.4) and (-1.15, -.4) ..
  (-1.15, 0)
    .. controls (-1.15, +.4) and (2, +.4) ..
  (+2, +.8)
    --
  (+2, 1);
\draw
  (+2, -1)
    --
  (+2, -.8)
    .. controls (2, -.4) and (-1.15, -.4) ..
  (-1.15, 0)
    .. controls (-1.15, +.4) and (2, +.4) ..
  (+2, +.8)
    --
  (+2, 1);

\draw[line width=4, white]
  (-1,-1) to (-1,0);
\draw 
  (-1,-1) to (-1,0);

\draw[line width=4, white]
  (0,-1) to (0,0);
\draw 
  (0,-1) to (0,0);

\draw[line width=4, white]
  (1,-1) to (1,0);
\draw 
  (1,-1) to (1,0);

\end{scope}

\node
  at (-1, -2.4) {
    \color{blue}
    $r$
  };

\node
  at (0, -2.4) {
    \color{blue}
    $i$
  };

\node
  at (+1, -2.4) {
    \color{blue}
    $s$
  };

\node
  at (+2, -2.4) {
    \color{blue}
    $j$
  };


\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\;\;\;
=
\;\;\;
\color{orange}
\left[
\color{black}
\raisebox{8pt}{

\begin{tikzpicture}[line width=1.2]

\begin{scope}[shift={(0,-1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,0) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+2,-1) to (+2,1);

\begin{scope}[shift={(+3,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}



\draw[line width=4, white]
  (+1, -1)
    --
  (+1, -.8)
    .. controls (+1, -.4) and (-1.14, -.4) ..
  (-1.15, 0)
    .. controls (-1.15, .4) and (+1, .4) ..
  (+1, .8)
    --
  (+1, 1);
\draw
  (+1, -1)
    --
  (+1, -.8)
    .. controls (+1, -.4) and (-1.14, -.4) ..
  (-1.15, 0)
    .. controls (-1.15, .4) and (+1, .4) ..
  (+1, .8)
    --
  (+1, 1);

\draw[line width=4, white]
  (-1,-1) to (-1,0);
\draw 
  (-1,-1) to (-1,0);

\end{scope}

\begin{scope}[shift={(0,+1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (-1,-1) to (-1,1);

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,1);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(+3,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4, white]
  (+2, -1)
    --
  (+2, -.8)
    .. controls (2, -.4) and (-1.15, -.4) ..
  (-1.15, 0)
    .. controls (-1.15, +.4) and (2, +.4) ..
  (+2, +.8)
    --
  (+2, 1);
\draw
  (+2, -1)
    --
  (+2, -.8)
    .. controls (2, -.4) and (-1.15, -.4) ..
  (-1.15, 0)
    .. controls (-1.15, +.4) and (2, +.4) ..
  (+2, +.8)
    --
  (+2, 1);

\draw[line width=4, white]
  (-1,-1) to (-1,0);
\draw 
  (-1,-1) to (-1,0);

\draw[line width=4, white]
  (0,-1) to (0,0);
\draw 
  (0,-1) to (0,0);

\draw[line width=4, white]
  (1,-1) to (1,0);
\draw 
  (1,-1) to (1,0);

\end{scope}

\node
  at (-1, -2.4) {
    \color{blue}
    $r$
  };

\node
  at (0, -2.4) {
    \color{blue}
    $i$
  };

\node
  at (+1, -2.4) {
    \color{blue}
    $s$
  };

\node
  at (+2, -2.4) {
    \color{blue}
    $j$
  };


\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}

Here we repeatedly used products of pure braid generators of the following form:

\begin{tikzcd}
\color{orange}
\left[
\color{black}
\raisebox{30pt}{
\begin{tikzpicture}[line width=1.2]


\begin{scope}[shift={(0,-3)}]


\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,1);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+2,-1) to (+2,1);

\begin{scope}[shift={(+3,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4pt, white]
  (-1,-1)
    --
  (-1, -.8)
    .. controls (-1, -.4) and (2.15, -.4) ..
  (2.15, 0)
    .. controls (2.15, .4) and (-1, .4) ..
  (-1, .8)
    --
  (-1,1);
\draw
  (-1,-1)
    --
  (-1, -.8)
    .. controls (-1, -.4) and (2.15, -.4) ..
  (2.15, 0)
    .. controls (2.15, .4) and (-1, .4) ..
  (-1, .8)
    --
  (-1,1);

\draw[line width=4pt, white]
  (2, 0) to (2,1);
\draw
  (2, 0) to (2,1);

\end{scope}




\begin{scope}[shift={(0,-1)}]


\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,1);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+2,-1) to (+2,1);

\begin{scope}[shift={(+3,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4pt, white]
  (-1,-1)
    --
  (-1, -.8)
    .. controls (-1, -.4) and (1.15, -.4) ..
  (1.15, 0)
    .. controls (1.15, .4) and (-1, .4) ..
  (-1, .8)
    --
  (-1,1);
\draw
  (-1,-1)
    --
  (-1, -.8)
    .. controls (-1, -.4) and (1.15, -.4) ..
  (1.15, 0)
    .. controls (1.15, .4) and (-1, .4) ..
  (-1, .8)
    --
  (-1,1);

\draw[line width=4pt, white]
  (1, 0) to (1,1);
\draw
  (1, 0) to (1,1);

\end{scope}


\begin{scope}[shift={(0,+1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,1);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+2,-1) to (+2,1);

\begin{scope}[shift={(+3,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\draw[line width=4, white]
  (-1,-1)
    --
  (-1,-.8)
    .. controls (-1, -.4) and (.15, -.4) ..
  (.15, 0)
    .. controls (.15, .4) and (-1, .4) ..
  (-1, .8)
    --
  (-1, 1);
\draw
  (-1,-1)
    --
  (-1,-.8)
    .. controls (-1, -.4) and (.15, -.4) ..
  (.15, 0)
    .. controls (.15, .4) and (-1, .4) ..
  (-1, .8)
    --
  (-1, 1);
  
\draw[line width=4, white]
  (0, 0) to (0,1);
\draw 
  (0, 0) to (0,1);
  
\end{scope}


\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\;\;\;
=
\;\;\;
\color{orange}
\left[
\color{black}
\raisebox{30pt}{
\begin{tikzpicture}[line width=1.2]


\begin{scope}[shift={(0,-2)}, yscale=2]


\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,1);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+2,-1) to (+2,1);

\begin{scope}[shift={(+3,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4pt, white]
  (-1,-1)
    --
  (-1, -.8)
    .. controls (-1, -.4) and (2.15, -.4) ..
  (2.15, 0)
    .. controls (2.15, .4) and (-1, .4) ..
  (-1, .8)
    --
  (-1,1);
\draw
  (-1,-1)
    --
  (-1, -.8)
    .. controls (-1, -.4) and (2.15, -.4) ..
  (2.15, 0)
    .. controls (2.15, .4) and (-1, .4) ..
  (-1, .8)
    --
  (-1,1);

\draw[line width=4pt, white]
  (2, 0) to (2,1);
\draw
  (2, 0) to (2,1);

\draw[line width=4pt, white]
  (1, 0) to (1,1);
\draw
  (1, 0) to (1,1);


\end{scope}




\begin{scope}[shift={(0,+1)}]

\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,1);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+2,-1) to (+2,1);

\begin{scope}[shift={(+3,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}


\draw[line width=4, white]
  (-1,-1)
    --
  (-1,-.8)
    .. controls (-1, -.4) and (.15, -.4) ..
  (.15, 0)
    .. controls (.15, .4) and (-1, .4) ..
  (-1, .8)
    --
  (-1, 1);
\draw
  (-1,-1)
    --
  (-1,-.8)
    .. controls (-1, -.4) and (.15, -.4) ..
  (.15, 0)
    .. controls (.15, .4) and (-1, .4) ..
  (-1, .8)
    --
  (-1, 1);
  
\draw[line width=4, white]
  (0, 0) to (0,1);
\draw 
  (0, 0) to (0,1);
  
\end{scope}


\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\;\;\;
=
\;\;\;
\color{orange}
\left[
\color{black}
\raisebox{30pt}{
\begin{tikzpicture}[line width=1.2]


\begin{scope}[shift={(0,-1)}, yscale=3]


\begin{scope}[shift={(-1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\begin{scope}[shift={(0,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (0,-1) to (0,1);

\begin{scope}[shift={(+1,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+1,-1) to (+1,1);

\begin{scope}[shift={(+2,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw (+2,-1) to (+2,1);

\begin{scope}[shift={(+3,0)}, gray]
\draw (-.75,-1) to (-.75,1);
\draw (-.25,-1) to (-.25,1);
\draw (-.5,-.6) node {\scalebox{.7}{$\cdots$}};
\end{scope}

\draw[line width=4pt, white]
  (-1,-1)
    --
  (-1, -.8)
    .. controls (-1, -.4) and (2.15, -.4) ..
  (2.15, 0)
    .. controls (2.15, .4) and (-1, .4) ..
  (-1, .8)
    --
  (-1,1);
\draw
  (-1,-1)
    --
  (-1, -.8)
    .. controls (-1, -.4) and (2.15, -.4) ..
  (2.15, 0)
    .. controls (2.15, .4) and (-1, .4) ..
  (-1, .8)
    --
  (-1,1);

\draw[line width=4pt, white]
  (2, 0) to (2,1);
\draw
  (2, 0) to (2,1);

\draw[line width=4pt, white]
  (1, 0) to (1,1);
\draw
  (1, 0) to (1,1);

\draw[line width=4pt, white]
  (0, 0) to (0,1);
\draw
  (0, 0) to (0,1);

\end{scope}


\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}






### As fundamental group of a configuration space of points
 {#AsFundamentalGroupOfConfigurationSpace}

Geometrically, one may understand the group of braids in $\mathbb{R}^3$ as the [[fundamental group]] of the [[configuration space of points]] in the [[plane]] $\mathbb{R}^2$ (traditionally regarded as the [[complex plane]] $\mathbb{C}$ in this context, though the [[complex structure]] plays no role in the definition of the braid group as such).

(originally due to [Hurwitz 1891, §II](#Hurwitz1891), then re-discovered/re-vived in [Fadell & Neuwirth 1962, p. 118](#FadellNeuwirth62), [Fox & Neuwirth 1962, §7](#FoxNeuwirth62), review includes [Birman 1975, §1](#Birman75), [Williams 2020, pp. 9](#Williams20))


\linebreak


**In the plane**

We say this in more detail:

Let $C_n \hookrightarrow \mathbb{C}^n$ denote the space of [[configuration space of points|configurations of n ordered  points]] in the [[complex plane]], whose elements are those [[n-tuples]] $(z_1, \ldots, z_n)$ such that $z_i \neq z_j$ whenever $i \neq j$. In other words, $C_n$ is the [[complement]] of the [[fat diagonal]]:

$$
  C_n 
    \;\coloneqq\; 
  \mathbb{C}^n \setminus \mathbf{\Delta}^n_{\mathbb{C}}
  \,.
$$


The [[symmetric group]] $S_n$ [[group action|acts]] on $C_n$ by [[permutation|permuting]] coordinates. Let:

* $C_n/S_n$  denote the [[quotient]] by this group action, hence the [[orbit]] space (the space of $n$-element subsets of $\mathbb{C}$ if one likes), 

* $[z_1, \ldots, z_n]$ denote the image of $(z_1, \ldots, z_n)$ under the quotient [[coprojection]] $\pi \colon C_n \to C_n/S_n$ (i.e. its the [[equivalence class]]). 

We understand $p = (1, 2, \ldots, n)$ as the basepoint for $C_n$, and $[p] = [1, 2, \ldots n]$ as the basepoint for the [[configuration space of unordered points]] $C_n/S_n$, making it a [[pointed topological space]].



\begin{definition}

The _braid group_ is the [[fundamental group]] of the [[configuration space of unordered points|configuration space of n unordered points]]:

$$
  Br(n) 
    \;\coloneqq\; 
  \pi_1
  \big(
    C_n/S_n, [p]
  \big)
$$

The _pure braid group_  is the [[fundamental group]] of the [[configuration space of ordered points|configuration space of n ordered points]]: 

$$
  PBr(n)
    \;\coloneqq\;
  \pi_1
  \big(
    C_n, p 
  \big)
  \,.
$$

\end{definition}


Evidently a braid $\beta$ is represented by a path $\alpha: I \to C_n/S_n$ with $\alpha(0) = [p] = \alpha(1)$. Such a path may be uniquely lifted through the [[covering]] projection $\pi: C_n \to C_n/S_n$ to a path $\tilde{\alpha}$ such that $\tilde{\alpha}(0) = p$. The end of the path $\tilde{\alpha}(1)$ has the same underlying subset as $p$ but with coordinates permuted: $\tilde{\alpha}(1) = (\sigma(1), \sigma(2), \ldots, \sigma(n))$. Thus the braid $\beta$ is exhibited by $n$ non-intersecting strands, each one connecting an $i$ to $\sigma(i)$, and we have a map $\beta \mapsto \sigma$ appearing as the quotient map of an exact sequence 

$$1 \to PBr(n) \to Br(n) \to Sym(n) \to 1$$ 

which is part of a [[long exact sequence of homotopy groups|long exact homotopy sequence]] corresponding to the [[fibration]] $\pi \colon C_n \to C_n/S_n$. 

\linebreak

**In general surfaces or graphs**
 {#ForMoreGeneralTopologicalSpaces}

Since the notion of a [[configuration space of points]] makes sense for points in any [[topological space]], not necessarily the [[plane]] $\mathbb{R}^2$, the [above](#GeometricDefinition) geometric definition has an immediate generalization:

For $\Sigma$ any [[surface]], the [[fundamental group]] of the (ordered) [[configuration space of points]] in $\Sigma$ may be regarded as generalized (pure) braid group, called a *surface braid group*. (See the *[[spherical braid group]]* for the case that the surface in question is the [[2-sphere]].)

These surface braid groups are of interest in [[3d topological field theory]] and in particular in [[topological quantum computation]] where it models [[non-abelian anyons]].


Yet more generally, one may consider the fundamental group of the configuration space of points of any topological space $X$.

For example for $X$ a 1-dimensional [[CW-complex]], hence an ([[undirected graph|undirected]]) [[graph]], one speaks of *graph braid groups* (e.g. [Farley & Sabalka 2009](#FarleySabalka2009)).

> The following should maybe not be here in the Definition-section, but in some Properties- or Examples-section, or maybe in a dedicated entry on *[[graph braid groups]]*:

It has been shown ([An & Maciazek 2006](#AnMaciazek2006), using discrete [[Morse theory]] and combinatorial analysis of small graphs) that graph braid groups are generated by particular particle moves with the following description:

1. Star-type generators: exchanges of particle pairs on vertices of the particular graph

2. loop type generators: circular moves of a single particle around a simple cycle of the graph

\linebreak



### Braid groups as mapping class groups of punctured surfaces
 {#BraidGroupsAsMappingClassGroupsOfPuncturedSurfaces}


The [[braid groups]] are equivalently given by [[mapping class groups]] of [[punctured]] [[surfaces]]. &lbrack;[Birman 1969](#Birman69)&rbrack;



#### For plain braid groups
 {#AsMappingClassGroupOfAPuncturedDisk}


The braid group $Br(n)$ may be alternatively described as the [[mapping class group]] of a 2-disk $D^2$ with $n$ punctures. &lbrack;[Birman 1969](#Birman69)&rbrack; 

(review includes [Birman 1975 §4](#Birman75), [González-Meneses 2011 §1.4](#González-Meneses11), [Massuyeau 2021 §3.3](#Massuyeau21), [Abadie 2022 §1.3](#Abadie22))

Concretely, consider 

1. $D^2 \setminus \{z_1, \cdots, z_n\}$ 

   denoting the [[complement]] of $n$ distinct points in the [[closed disk]] (with [[boundary]] the [[circle]]);

1. $Homeo^{\partial}\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)$ 

   denoting the [[mapping space]] of [[automorphism|auto]]-[[homeomorphisms]] which restrict to the [[identity]] on the [[boundary]] [[circle]], regarded with its canonical [[group]] [[structure]] under [[composition]];

1. $Homeo^{\partial}_id\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)$ 

   denoting the [[subgroup]] which is the [[connected component]] of the [[identity]] (which is readily seen to be a [[normal subgroup]]).

Then the [[mapping class group]] is the [[quotient group]]:

$$
  MCG
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\}
  \big)
  \;\coloneqq\;
  Homeo^{\partial}\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)
  \Big/
  Homeo^{\partial}_{id}\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)
  \,.
$$

Now observe that 

1. for the case that $n = 0$ this group is [[trivial group|trivial]], by *[[Alexander's trick]]*. 

1. continuous extension yields an [[injection]]

   $$
     Homeo^{\partial}\big(D^2 \setminus \{z_1, \cdots, z_n\} \big)
     \xhookrightarrow{\phantom{-}\iota\phantom{-}}
     Homeo^{\partial}\big(D^2\big)
     \,.
   $$

Combining this implies that for every $[\phi] \,\in\, MCG\big(D^2 \setminus \{z_1, \cdots, z_n\}\big)$ there is an [[isotopy]] to the [[identity]], $\iota[\phi] \to id$, under which the locations of the [[punctures]] trace out a [[braid]] (in the sense of a [[loop]] in the symmetrized [[configuration space of points]]). This construction constitutes a [[group homomorphism]] from the [[mapping class group]] to the [[braid group]]
$$
  MCG
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\}
  \big)
  \xrightarrow{\;\;\sim\;\;}
  Br(n) 
  \,.
$$
and this is an [[isomorphism]].


\begin{remark}\label{ActionOfBraidGroupOnFundamentalGroupOfPuncturedDisk}
**(action of braid group on fundamental group of $n$-punctured disk)**
\linebreak
It follows in particular that the braid group $Br(n)$ has a canonical [[group action]] on the [[fundamental group]] of the $n$-punctured disk. Since the latter is [[isomorphism|isomorphic]] to the [[free group]] on $n$ [[generators and relations|generators]], this leads to the purely algebraic characterization of the braid group [below](#AsAutomorphismsOfAFreeGroup).

See also eg. [Margalit & Winarski (2021), §7](#MargalitWinarski21), [Amram, Lawrence & Vishne (2012), §7](#AmramLawrenceVishne12).
\end{remark}


#### For surface braid groups
 {#SurfaceBraidGroupsViaMappingClassGroups}

More generally, let $\Sigma$ be a ([[connected topological space|connected]]) [[closed manifold|closed]], [[orientation|oriented]] [[surface]], possibly with [[boundary of a manifold|boundary]] and let $x_1, \cdots, x_n \in \Sigma$ a [[finite set]] of [[interior]] points.

Then: 

\begin{proposition}
\label{SurfaceBraidGroupsAsFibersOfForgettingPuncturesInMCG}
The [[mapping class groups]] ($MCG(-) \coloneqq \pi_0 Homeo^{+,\partial}(-)$)

* $MCG(\Sigma)$ (of $\Sigma$ itself, presering orientation and the boundary pointwise)

* $MCG(\Sigma, \{x_1, \cdots, x_n\})$ (of $\Sigma$ with "indistinguishable" punctures)

* $MCG(\Sigma, \{x_1\}, \cdots, \{x_n\})$ (of $\Sigma$ with "distinguishable" punctures)

relate to the [[surface braid groups]]

* $Br_n(\Sigma)$ (ordinary braid group)

* $PBr_n(\Sigma)$ (pure braid group)

* $Sym_n$ (the [[symmetric group]])

by forming the following [[commuting diagram]] of [[group homomorphisms]] where all rows and all columns are [[exact sequences]]:

\begin{tikzcd}
  & 
  1 \ar[d]
  & 
  1 \ar[d]
  \\
  \pi_1\big(
    \mathrm{Homeo}^{+,\partial}(\Sigma)
  \big)
  \ar[r]
  \ar[d, equals]
  &
  \mathrm{PBr}_n(\Sigma)
  \ar[r]
  \ar[d]
  &
  \mathrm{MCG}\big(\Sigma, \{x_1\}, \cdots, \{x_n\}\big)
  \ar[r]
  \ar[d]
  &
  \mathrm{MCG}\big(\Sigma\big)
  \ar[r]
  \ar[d, equals]
  &
  1
  \\
  \pi_1\big(
    \mathrm{Homeo}^{+,\partial}(\Sigma)
  \big)
  \ar[r]
  &
  \mathrm{Br}_n(\Sigma)
  \ar[r]
  \ar[d]
  &
  \mathrm{MCG}\big(
    \Sigma, \{x_1, \cdots, x_n\}
  \big)
  \ar[r]
  \ar[d]
  & 
  \mathrm{MCG}(\Sigma)
  \ar[r]
  &
  1
  \\
  & \mathrm{Sym}_n 
  \ar[d]
  \ar[r, equals]
  & \mathrm{Sym}_n
  \ar[d]
  \\
  & 1 & 1
\end{tikzcd}

\end{proposition}
(Going back to [Birman 1969](#Birman69), cf. [Massuyeau 2021 Thm. 3.13](#Massuyeau21)).


In fact:

\begin{proposition}
  \label{TrivialityOfHigherHomeomorphismGroups}
  Let $\Sigma$ be the result of equipping a [[compact topological space|compact]] [[surface]] with a [[finite number]] of [[interior]] [[punctures]], then 

$$
  \pi_{n \geq 1} Homeo_0(\Sigma)
  \;=\;
  trivial
$$ 

**unless** $\Sigma$ is [[homeomorphism|homeomorphic]] to any one of 

* the [[2-sphere]] $S^2$,

* the [[plane]] $\mathbb{R}^2$,

* the [[closed disk]] $D^2$,

* the [[torus]] $Y^2$,

* the [[closed annulus]],

* the 1-[[punctured surface|punctured]] [[disk]] $D^2 \setminus \{0\}$,

* the 1-[[punctured surface|punctured]] [[plane]] $\mathbb{R}^2 \setminus \{0\}$.

\end{proposition}

([Farb & Margalit 2012, Thm. 1.14](#FarbMargalit12), due to a series of results by Hamstrom)

\begin{corollary}
  In the situation of Prop. \ref{TrivialityOfHigherHomeomorphismGroups}
  the [[long exact sequences]] of Prop. \ref{SurfaceBraidGroupsAsFibersOfForgettingPuncturesInMCG} become [[short exact sequences]]:

\begin{tikzcd}
  & 
  1 \ar[d]
  & 
  1 \ar[d]
  \\
  1
  \ar[r]
  \ar[d, equals]
  &
  \mathrm{PBr}_n(\Sigma)
  \ar[r]
  \ar[d]
  &
  \mathrm{MCG}\big(\Sigma, \{x_1\}, \cdots, \{x_n\}\big)
  \ar[r]
  \ar[d]
  &
  \mathrm{MCG}\big(\Sigma\big)
  \ar[r]
  \ar[d, equals]
  &
  1
  \\
  1
  \ar[r]
  &
  \mathrm{Br}_n(\Sigma)
  \ar[r]
  \ar[d]
  &
  \mathrm{MCG}\big(
    \Sigma, \{x_1, \cdots, x_n\}
  \big)
  \ar[r]
  \ar[d]
  & 
  \mathrm{MCG}(\Sigma)
  \ar[r]
  &
  1
  \\
  & \mathrm{Sym}_n 
  \ar[d]
  \ar[r, equals]
  & \mathrm{Sym}_n
  \ar[d]
  \\
  & 1 & 1
\end{tikzcd}

\end{corollary}

([Farb & Margalit 2012, Thm. 9.1](#FarbMargalit12))




In words: *The [[mapping class group]] of a [[punctured]] [[surface]] is a [[group extension]] of the [[mapping class group]] of the plain surface by the surface braid group on the set of punctures.*


### As automorphisms of a free group
 {#AsAutomorphismsOfAFreeGroup}

Since the [[fundamental group]] of $D^2 \setminus \{z_1, \cdots, z_n\}$ is [[generalized the|the]]  [[free group]] of $n$ generators, the MCG-presentation of the braid group ([above](#InTermsOfAutomorphismsOfFreeGroups)) induces a [[group homomorphism]] of the braid group into the [[automorphism group]] of a [[free group]], which turns out to be [[faithful representation|faithful]].

This presentation is due to [Artin 1925, §6](#Artin25), review includes [González-Meneses 2011, §1.6](#González-Meneses11), see also pointer in [Bardakov 2005, p.  2](#Bardakov05).


More in detail, since the [[homotopy type]] of this punctured disk is, evidently, that of the the [[wedge sum]] of $n$ [[circles]], it follows that its [[fundamental group]] is is the [[free group]] $F_n$ on $n$ generators:

$$
  \pi_1
  \big(
    D^2 \setminus \{z_1, \cdots, z_ n\}
  \big)
  \;\simeq\;
  \pi_1
  \big(
    \vee_n S^1
  \big)
  \;\simeq\;
  F_n
  \,.
$$ 

Now the [[functor|functoriality]] of $\pi_1 \,\colon\, Top^{\ast/} \longrightarrow Grp$ implies we have an induced homomorphism 

$$
  Aut
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\} 
  \big)
  \longrightarrow 
  Aut
  \Big(
    \pi_1\big(
      D^2 \setminus \{z_1, \cdots, z_n\} 
    \big)
  \Big) 
  \,\simeq\, 
  Aut(F_n)
  \,.
$$ 

If such an automorphism $\phi$ of $D^2 \setminus \{z_1, \cdots, z_n\} $ is [[isotopy|isotopic]] to the [[identity]], then of course $\pi_1(\phi)$ is trivial, which means that the above homomorphism factors through the [[quotient group]] known as the [[mapping class group]]:

$$
  MCG
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\}
  \big) 
  \,=\, 
  Aut
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\}
  \big)/Aut_0
  \big(
     D^2 \setminus \{z_1, \cdots, z_n\}  
  \big)
$$ 

Therefore, the above gives a homomorphism of the following form, which turns out to be a [[monomorphism]]:

$$
  Br(n) 
    \,=\, 
  MCG
  \big(
    D^2 \setminus \{z_1, \cdots, z_n\}
  \big) 
  \xhookrightarrow{\phantom{--}} 
  Aut(F_n)
$$ 

\begin{imagefromfile}
    "file_name": "BraidActingOnFundamentalGroup-Artin1925.jpg",
    "width": 440,
    "float": "right",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [Artin 1925](#Artin25)"
\end{imagefromfile}



Explicitly, the generator $yb_i$ (eq:ArtinGenerators) in the Artin presentation(Def. \ref{ArtinPresentation}) is mapped to the automorphism $\sigma_i$ on the free group on $n$ generators $t_1, \ldots, t_n$ which is given as follows:

$$
  \sigma_i(t_j)
  \,=\,
  \left\{
  \begin{array}{lcl}
    t_{i+1} & \vert & j = i
    \\  
    t_{i+1}^{-1} \cdot t_i \cdot t_{i+1}
    & \vert & 
    j = i + 1
    \\
    t_j &\vert& \text{otherwise.}
  \end{array}
  \right.
$$

([Artin 1925, (24)](#Artin25))

\begin{imagefromfile}
    "file_name": "BraidActingOnFundamentalGroup-Gonzalez2011.jpg",
    "width": 540,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [González-Meneses 2011](#González-Meneses11)"
\end{imagefromfile}




\linebreak

## Properties

### Relation to moduli space of monopoles

+-- {: .num_prop #ModuliSpaceOfkMonopolesStablyWeakHomotopyEquivbalentToClassifyingSpaceOfBraids}
###### Proposition
**([[moduli space of monopoles]] is [[stable weak homotopy equivalence|stably weak homotopy equivalent]] to [[classifying space]] of [[braid group]])**

For $k \in \mathbb{N}$ there is a [[stable weak homotopy equivalence]] between the [[moduli space of k monopoles]] (eq:ModuliSpaceOfkInstantons) and the [[classifying space]] of the [[braid group]] $Br({2k})$ on $2 k$ strands:

$$
  \Sigma^\infty \mathcal{M}_k
  \;\simeq\;
  \Sigma^\infty Br({2k})
$$

=--

([Cohen-Cohen-Mann-Milgram 91](#CohenCohenMannMilgram91))


## Examples
 {#Examples}

The first few examples of the braid group $Br(n)$ for low values of $n$:

\begin{example}
The group $Br(1)$ has no generators and no relations, so is the [[trivial group]]:
$$
  Br(1) \;\simeq\; 1  
  \,.
$$

\end{example}

\begin{example}
The group $Br(2)$ has one generator and no relations, so is the infinite cyclic group of [[integers]]:
$$
  Br(2) \;\simeq\; \mathbb{Z}
  \,.
$$
\end{example}


\begin{example}\label{TheBraidgroupBr3}
The group $Br(3)$ (we will simplify notation writing $u = y_1$, $v = y_2$)
has presentation 

$$
  Br(3)
  \;\simeq\;
  \mathcal{P} 
  \coloneqq 
  \big( 
     u,v : r \equiv u v u v^{-1} u^{-1} v^{-1}
  \big).
$$

This is also known as the "trefoil [[knot group]]", i.e., the [[fundamental group]] of the [[complement]] of a [[trefoil knot]]. 
\end{example}

\begin{example}
The group $Br(4)$ (simplifying notation as [before](#TheBraidgroupBr3)) has generators $u,v,w$ and relations:

 *  $r_u \equiv  v w v w^{-1} v^{-1} w^{-1}$,

 *  $r_v \equiv  u w u^{-1} w^{-1}$,

 *  $r_w \equiv  u v u v^{-1} u^{-1} v^{-1}$.

\end{example}

\begin{example}\label{HurwitzBraidGroup}
The **Hurwitz braid group** (or **sphere braid group**) is the [surface braid group](#ForMoreGeneralTopologicalSpaces) for $\Sigma$ the [[2-sphere]] $S^2$.  Algebraically, the Hurwitz braid group $H_{n+1}$ has all of the generators and relations of the Artin braid group $Br({n+1})$, plus one additional relation:

$$ 
  y_1 y_2 \dots y_{n-1} y_n^2 y_{n-1}\dots y_2 y_1
$$
\end{example}


## Related concepts

* [[spherical braid group]]

* [[annular braid group]]

* [[braid representation]]

* [[braid group statistics]]

  [[anyons]], [[quantum Hall effect]]

  [[topological quantum computation]]

* [braid group cryptography](cryptography#BraidGroupCryptographyReferences)

* [[braid category]]

* [[infinitesimal braid relation]]

* [[loop braid group]]

* [[parenthesized braid operad]]

* [[braid cobordism]]

* [[vine monoid]]

* [[tangle]]

[[!include chord diagrams and weight systems -- table]]


## References

### General

The braid group regarded as the [[fundamental group]] of a [[configuration space of points]] is considered (neither of them under these names, though) already in:

* {#Hurwitz1891} [[Adolf Hurwitz]], §II of: *&Uuml;ber Riemann'sche Flächen mit gegebenen Verzweigungspunkten*, Mathematische Annalen **39** (1891) 1–60 &lbrack;[doi:10.1007/BF01199469](https://doi.org/10.1007/BF01199469)&rbrack;

there regarded as [[group action|acting]] on [[Riemann surfaces]] forming [[branched covers]], by movement of the branch points.

The original articles dedicated to analysis of the braid group:

* {#Artin25} [[Emil Artin]], *Theorie der Zöpfe*, Abh. Math. Semin. Univ. Hambg. **4**  (1925) 47–72 &lbrack;[doi;10.1007/BF02950718](https://doi.org/10.1007/BF02950718)&rbrack;

  >(the braid group via generators & relations and via automorphisms of free groups)

* [[Wilhelm Magnus]], *Über Automorphismen von Fundamentalgruppen berandeter Flächen*, Mathematische Annalen **109** (1934) 617–646 &lbrack;[doi:10.1007/BF01449158](https://doi.org/10.1007/BF01449158)&rbrack;
  > (the braid group as a [[mapping class group]])
    
* {#Artin47} [[Emil Artin]], *Theory of Braids*, Annals of Mathematics, Second Series, **48** 1 (1947) 101-126 &lbrack;[doi:10.2307/1969218](https://doi.org/10.2307/1969218)&rbrack;

* [[Frederic Bohnenblust]], *The Algebraical Braid Group*, Annals of Mathematics Second Series **48** 1 (1947) 127-136 &lbrack;[doi:10.2307/1969219](https://doi.org/10.2307/1969219)&rbrack;

* [[Wei-Liang Chow]], *On the Algebraical Braid Group*, Annals of Mathematics Second Series, **49** 3 (1948) 654-658 &lbrack;[doi:10.2307/1969050](https://doi.org/10.2307/1969050)&rbrack;

Identifying the [[center]] of the braid group as the [[subgroup]] generated by the square of the "fundamental braid" or "half-twist":

* F. A. Garside: *The braid group and other groups*,  The Quarterly Journal of Mathematics **20** 1 (1969) 235–254 &lbrack;[doi:10.1093/qmath/20.1.235](https://doi.org/10.1093/qmath/20.1.235), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/garside.pdf), [pdf](https://nsalter.science.nd.edu/teaching/braidsspring2024/garside.pdf)&rbrack; 



Survey of the early history:

* [[Michael Friedman (historian)]], *Mathematical formalization and diagrammatic reasoning: the case study of the braid group between 1925 and 1950*, British Journal for the History of Mathematics **34** 1 (2019) 43-59 &lbrack;[doi:10.1080/17498430.2018.1533298](https://doi.org/10.1080/17498430.2018.1533298)&rbrack;


The understanding of the braid group as the [[fundamental group]] of a [[configuration space of points]] was re-discovered/re-vived (after [Hurwitz 1891](#Hurwitz1891)) in:

* {#FoxNeuwirth62} [[Ralph H. Fox]], [[Lee Neuwirth]], *The braid groups*, Math. Scand. **10** (1962) 119-126 $[$[doi:10.7146/math.scand.a-10518](https://doi.org/10.7146/math.scand.a-10518), [pdf](https://www.mscand.dk/article/view/10518/8539), [MR150755](http://www.ams.org/mathscinet-getitem?mr=150755)$]$

* {#FadellNeuwirth62} [[Edward Fadell]], [[Lee Neuwirth]], *Configuration spaces*, Math. Scand. __10__ (1962) 111-118 $[$[doi:10.7146/math.scand.a-10517](https://doi.org/10.7146/math.scand.a-10517), [MR141126](http://www.ams.org/mathscinet-getitem?mr=141126)$]$

The understanding of the braid group as the [[mapping class group]] of the punctured disk, etc., is due to:

* {#Birman69} [[Joan S. Birman]]: *Mapping class groups and their relationship to braid groups*, Communications on Pure and Applied Mathematics **22** 2 (1969) 213-238 &lbrack;[doi:10.1002/cpa.3160220206](https://doi.org/10.1002/cpa.3160220206)&rbrack;

Textbook accounts:

* {#Birman75} [[Joan S. Birman]], _Braids, links, and mapping class groups_, Princeton Univ Press (1975) &lbrack;[ISBN:9780691081496](https://press.princeton.edu/books/paperback/9780691081496/braids-links-and-mapping-class-groups-am-82-volume-82), [preview pdf](https://api.pageplace.de/preview/DT0400.9781400881420_A26691398/preview-9781400881420_A26691398.pdf)&rbrack;

* [[Saunders MacLane]], §XI.4 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* [[Tomotada Ohtsuki]] ch 2 of: *Quantum Invariants -- A Study of Knots, 3-Manifolds, and Their Sets*, World Scientific (2001) &lbrack;[doi:10.1142/4746](https://doi.org/10.1142/4746)&rbrack;

* [[Christian Kassel]], [[Vladimir Turaev]], _Braid Groups_, GTM **247** Springer Heidelberg 2008 ([doi:10.1007/978-0-387-68548-9](https://link.springer.com/book/10.1007/978-0-387-68548-9), [webpage](http://irma.math.unistra.fr/~kassel/Braids-bk.html))

In relation to [[mapping class groups]]:

* {#FarbMargalit12} [[Benson Farb]], [[Dan Margalit]]: *Braid groups*, chapter 9 of: *A primer on mapping class groups*, Princeton Mathematical Series, Princeton University Press (2012) &lbrack;[ISBN:9780691147949](https://press.princeton.edu/books/hardcover/9780691147949/a-primer-on-mapping-class-groups), [jstor:j.ctt7rkjw](https://www.jstor.org/stable/j.ctt7rkjw), [pdf](http://euclid.nmu.edu/~joshthom/Teaching/MA589/farbmarg.pdf)&rbrack;


Further introduction and review:

* [[Joan S. Birman]], [[Anatoly Libgober]] (eds.) *Braids*, Contemporary Mathematics **78** (1988) &lbrack;[doi:10.1090/conm/078](http://dx.doi.org/10.1090/conm/078)&rbrack;

* [[Chen Ning Yang]], M. L. Ge (eds.), *Braid Group, Knot Theory and Statistical Mechanics*, Advanced Series in Mathematical Physics **9**, World Scientific (1991) &lbrack;[doi:10.1142/0796](https://doi.org/10.1142/0796)&rbrack;

* [[Dale Rolfsen]]: *Tutorial on the braid groups*, lecture notes (2007) &lbrack;[arXiv:1010.4051](https://arxiv.org/abs/1010.4051)&rbrack;

* Joshua Lieber, *Introduction to Braid Groups*, 2011 ([pdf](https://math.uchicago.edu/~may/VIGRE/VIGRE2011/REUPapers/Lieber.pdf))

* {#González-Meneses11} [[Juan González-Meneses]], *Basic results on braid groups*, Annales Mathématiques Blaise Pascal, **18** 1 (2011) 15-59 &lbrack;[ambp:AMBP_2011__18_1_15_0](https://ambp.centre-mersenne.org/item/?id=AMBP_2011__18_1_15_0), [numdam:AMBP_2011__18_1_15_0](http://www.numdam.org/item/AMBP_2011__18_1_15_0)&rbrack;

* Alexander I. Suciu, He Wang, *The pure braid groups and their relatives*,  Perspectives in Lie theory, INdAM series, **19** Springer (2017) 403-426 &lbrack;[arXiv:1602.05291](https://arxiv.org/abs/1602.05291)&rbrack;

* [[Dale Rolfsen]]: *New developments in the theory of Artin’s braid groups*, Topology and its Applications **127** 1–2 (2003) 77-90 &lbrack;<a href="https://doi.org/10.1016/S0166-8641(02)00054-8">doi:10.1016/S0166-8641(02)00054-8</a>, [pdf](https://personal.math.ubc.ca/~rolfsen/papers/newbraid/newbraid2.pdf)&rbrack;

* John Guaschi, Daniel Juan-Pineda: *A survey of surface braid groups and the lower algebraic K-theory of their group rings* &lbrack;[arXiv:1302.6536](https://arxiv.org/abs/1302.6536)&rbrack;

* [[Jennifer C. H. Wilson]], *The geometry and topology of braid groups*, lecture at *[2018 Summer School on Geometry and Topology](https://www.pims.math.ca/scientific-event/180611-ssgt)*, Chicago (2018) &lbrack;[pdf](http://www.math.lsa.umich.edu/~jchw/RTG-Braids.pdf), [[Wilson-BraidGroups.pdf:file]]&rbrack;

* {#Williams20} [[Lucas Williams]], *Configuration Spaces for the Working Undergraduate*,  Rose-Hulman Undergraduate Mathematics Journal, **21** 1 (2020) Article 8 &lbrack;[arXiv:1911.11186](https://arxiv.org/abs/1911.11186), [rhumj:vol21/iss1/8](https://scholar.rose-hulman.edu/rhumj/vol21/iss1/8)&rbrack;

* {#Massuyeau21} [[Gwénaël Massuyeau]]: *Lectures on Mapping Class Groups, Braid Groups and Formality* (2021) &lbrack;[pdf](https://massuyea.perso.math.cnrs.fr/notes/formality.pdf)&rbrack;

* [[Jennifer C. H. Wilson]], *Representation stability and the braid groups*, talk at *[ICERM -- Braids](https://icerm.brown.edu/programs/sp-s22/)* (Feb 2022) &lbrack;[pdf](https://app.icerm.brown.edu/assets/362/3661/3661_3250_021720221430_Slides.pdf)&rbrack;

* {#Abadie22} Marie Abadie, §1 in: *A journey around mapping class groups and their presentations* (2022) &lbrack;[pdf](https://christianurech.github.io/Semester_Project.pdf), [[Abadie-MCG.pdf:file]]&rbrack;

See also:

* Wikipedia: _[Braid group](http://en.wikipedia.org/wiki/Braid_group)_

As an example of motion general "motion groups" (such as [[loop braid groups]]):

* {#Goldsmith81} [[Deborah L. Goldsmith]], *The theory of motion groups*, Michigan Math. J. **28** 1 (1981) 3-17 &lbrack;[doi:10.1307/mmj/1029002454](https://projecteuclid.org/journals/michigan-mathematical-journal/volume-28/issue-1/The-theory-of-motion-groups/10.1307/mmj/1029002454.full)&rbrack;



Algebraic presentation of braid groups:

* [[Warren Dicks]], Edward Formanek, around Ex. 15.2 of: *Algebraic Mapping-Class Groups of Orientable Surfaces with Boundaries*, in: *Infinite Groups: Geometric, Combinatorial and Dynamical Aspects*, Progress in Mathematics **248** Birkhäuser (2005) &lbrack;[doi :10.1007/3-7643-7447-0_4](https://doi.org/10.1007/3-7643-7447-0_4)&rbrack;

* [Bacardit & Dicks 2009](#BacarditDicks09)

More [[finitely presented group|finite presentations]] of the *pure* braid group:

* [[Dan Margalit]], [[Jon McCammond]], *Geometric presentations for the pure braid group*,  Journal of Knot Theory and Its Ramifications **18** 01 (2009) 1-20 &lbrack;[arXiv:math/0603204](https://arxiv.org/abs/math/0603204), [doi:10.1142/S0218216509006859](https://doi.org/10.1142/S0218216509006859)&rbrack;

* {#Lee10} [[Eon-Kyung Lee]], *A positive presentation of the pure braid group*, Journal of the Chungcheong Mathematical Society **23** 3 (2010) 555-561 &lbrack;[JAKO201007648745187](https://koreascience.kr/article/JAKO201007648745187.view?orgId=anpor), [pdf](http://www.ccms.or.kr/data/pdfpaper/jcms23_3/23_3_555.pdf)&rbrack;

More on the relation of braid groups to [[mapping class groups]]:

* {#AmramLawrenceVishne12} M. Amram, R. Lawrence, U. Vishne, *Artin Covers of the Braid Group*,  Journal of Knot Theory and Its Ramifications **21** 07 (2012) 1250061 &lbrack;[doi:10.1142/S0218216512500617](https://doi.org/10.1142/S0218216512500617), [pdf](http://www.ma.huji.ac.il/~ruthel/papers/12artin.pdf)&rbrack; 

* {#MargalitWinarski21} [[Dan Margalit]], [[Rebecca R. Winarski]], *Braid groups and mapping class groups: The Birman–Hilden theory*, Bull. London Math. Soc. **53** 3 (2021) 643-659 &lbrack;[arXiv:1703.03448](https://arxiv.org/abs/1703.03448), [doi:10.1112/blms.12456](https://doi.org/10.1112/blms.12456)&rbrack;

More on the braid representation on [[automorphism group|automorphisms]] of [[free groups]]:

* {#BacarditDicks09} [[Lluís Bacardit]], [[Warren Dicks]], *Actions of the braid group, and new algebraic proofs of results of Dehornoy and Larue*, Groups Complexity Cryptology **1** (2009) 77-129 &lbrack;[arXiv:0705.0587](https://arxiv.org/abs/0705.0587), [doi;10.1515/GCC.2009.77](https://doi.org/10.1515/GCC.2009.77)&rbrack;

* {#Bardakov05} [[Valerij G. Bardakov]], *Extending representations of braid groups to the automorphism groups of free groups*, Journal of Knot Theory and Its Ramifications **14** 08 (2005) 1087-1098 &lbrack;[arXiv:math/0408330](https://arxiv.org/abs/math/0408330), [doi:10.1142/S0218216505004251](https://doi.org/10.1142/S0218216505004251)&rbrack;

* Tetsuya Ito, *Actions of the $n$-strand braid groups on the free group of rank n which are similar to the Artin representation*, Quart. J. Math **66** (2015) 563-581 &lbrack;[arXiv;1406.2411](https://arxiv.org/abs/1406.2411), [doi:10.1093/qmath/hau033](https://doi.org/10.1093/qmath/hau033)&rbrack;



On the [[group homology]] and [[group cohomology]] of braid groups:

* [[Vladimir Vershinin]], *Homology of Braid Groups and their Generalizations*, Banach Center Publications (1998) **42** 1 421-446 ([pdf](https://hopf.math.purdue.edu/Vershinin/hobr.pdf), [dml:208821](https://eudml.org/doc/208821))

Relation of [[automorphism groups]] of the [[profinite completion]] of braid groups to the [[Grothendieck-Teichmüller group]]:

* [[Pierre Lochak]], [[Leila Schneps]], *The Grothendieck-Teichmüller group and automorphisms of braid groups*, in: *The Grothendieck Theory of Dessins d’Enfant*, Cambridge University Press (1994, 2011) &lbrack;[pdf](https://webusers.imj-prg.fr/~leila.schneps/Fls.pdf), [doi:10.1017/CBO9780511569302](https://doi.org/10.1017/CBO9780511569302)&rbrack;


On braid [[subgroups]]:

* [[Dale Rolfsen]]: *Braid subgroup normalisers, commensurators and induced representations*, Invent Math **130** (1997) 575–587 &lbrack;[doi:10.1007/s002220050194](https://doi.org/10.1007/s002220050194), [pdf](https://personal.math.ubc.ca/~rolfsen/papers/braidnorm/B_nFinal2.pdf)&rbrack;

* D. B. McReynolds: *The congruence subgroup problem for braid groups: Thurston's proof*, New York Jour. Math. **18** (2012) 925-942 &lbrack;[arXiv:0901.4663](https://arxiv.org/abs/0901.4663)&rbrack;

* Charalampos Stylianakis: *Congruence subgroups of braid groups*,  International Journal of Algebra and Computation **28** 02 (2018) 345-364 &lbrack;[doi:10.1142/S0218196718500169](https://doi.org/10.1142/S0218196718500169)&rbrack;



On orderings of the braid group:

* [[Patrick Dehornoy]]: *Braid groups and left distributive operations*, Transactions AMS **345** 1 (1994) 115150 &lbrack;[doi:10.1090/S0002-9947-1994-1214782-4](https://doi.org/10.1090/S0002-9947-1994-1214782-4), [pdf](https://dehornoy.lmno.cnrs.fr/Papers/Dfb.pdf)&rbrack;

* H. Langmaack, _Verbandstheoretische Einbettung von Klassen unwesentlich verschiedener Ableitungen in die Zopfgruppe_ , Computing **7** no.3-4 (1971) pp.293-310.



On geometric presentations of braid groups:

* Byung Hee An, Tomasz Maciazek, *Geometric Presentations of Braid Groups for Particles on a Graph*, Communications in Mathematical Physics **384** (2021) 1109-1140 &lbrack;[doi:10.1007/s00220-021-04095-x](http://dx.doi.org/10.1007/s00220-021-04095-x)&rbrack;  

On [[G-structure]] for $G = Br_\infty$ the infinite braid group:

* [[Frederick R. Cohen]], *Braid orientations and bundles with flat connections*, Inventiones mathematicae **46** (1978) 99–110 &lbrack;[doi:10.1007/BF01393249](https://doi.org/10.1007/BF01393249)&rbrack;

* [[Jonathan Beardsley]], *On Braids and Cobordism Theories*, Glasgow (2022) &lbrack;notes: [pdf](https://www.jonathanbeardsley.com/GlasgowNotes2022.pdf), [[Beardsley-BraidsAndCobordism.pdf:file]]&rbrack;


[[!include braid group representations -- references]]



### Graph braid groups
  {#ReferencesGraphBraidGroups}

* {#FarleySabalka2009} Daniel Farley, Lucas Sabalka, *Presentations of Graph Braid Groups* ([arXiv:0907.2730](https://arxiv.org/abs/0907.2730))

* Ki Hyoung Ko, Hyo Won Park,  *Characteristics of graph braid groups* ([arXiv:1101.2648](https://arxiv.org/abs/1101.2648))

* {#AnMaciazek2006} Byung Hee An, Tomasz Maciazek, *Geometric presentations of braid groups for particles on a graph* ([arXiv:2006.15256](https://arxiv.org/abs/2006.15256))



### Relation to moduli space of monopoles

On [[moduli spaces of monopoles]] related to [[braid groups]]:

* [[Fred Cohen]], [[Ralph Cohen]], B. M. Mann, R. J. Milgram, _The topology of rational functions and divisors of surfaces_, Acta Math (1991) 166: 163 ([doi:10.1007/BF02398886](https://doi.org/10.1007/BF02398886))

* [[Ralph Cohen]], John D. S. Jones  _Monopoles, braid groups, and the Dirac operator_, Comm. Math. Phys. Volume 158, Number 2 (1993), 241-266 ([euclid:cmp/1104254240](https://projecteuclid.org/euclid.cmp/1104254240))




[[!include braid group cryptography -- references]]




category: knot theory

[[!redirects braid groups]]

[[!redirects braid]]
[[!redirects braids]]

[[!redirects pure braid]]
[[!redirects pure braids]]

[[!redirects pure braid group]]
[[!redirects pure braid groups]]


[[!redirects Artin braid group]]
[[!redirects Hurwitz braid group]]

[[!redirects surface braid group]]
[[!redirects surface braid groups]]

