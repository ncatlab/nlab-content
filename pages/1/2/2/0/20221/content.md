
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The [[spin group]] in [[dimension]] 6.

## Properties

### Exceptional isomorphism
 {#ExceptionalIsomorphism}

+-- {: .num_prop #IsomorphismBetweenSpin6AndSU4}
###### Proposition

There is an [[exceptional isomorphism]] 

\begin{tikzpicture}

  \node (Spin6) at (0,1.4)  {$\mathrm{Spin}(6)$};
  \node (SU4) at (3.4,1.4)  {$\mathrm{SU}(4)$};

  \node at (1.7,1.4) {$\simeq$};

  \node (center) at (0,0) {};
  \node (topright) at (30:1) {};
  \node (left) at (180-30:1) {};
  \node (botright) at (0,-1) {};
  
  \draw[fill=black] (center) circle (.1);
  \draw[fill=black] (topright) circle (.1);
  \draw[draw=lightgray, fill=lightgray] (botright) circle (.1);
  \draw[fill=black] (left) circle (.1);


  \draw (center) to (topright);
  \draw[lightgray] (center) to (botright);
  \draw (center) to (left);
    
  \begin{scope}[shift={(3.4,0)}]
  \node (center) at (0,0) {};
  \node (left) at (-1,0) {};
  \node (right) at (+1,0) {};

  \draw[fill=black] (center) circle (.1);
  \draw[fill=black] (left) circle (.1);
  \draw[fill=black] (right) circle (.1);

  \draw (center) to (left);
  \draw (center) to (right);
  \end{scope}
\end{tikzpicture}

between [[Spin(6)]] and [[SU(4)]], reflecting, under the [[classification of simple Lie groups]], the coicidence of [[Dynkin diagram]] of "[[D3]]" with [[A3]].

=--

(e.g. [Figueroa-O'Farrill 10, Lemma 8.1](#FigueroaFarrill10))


### Coset spaces

[[!include coset space structure on n-spheres -- table]]


### $G$-Structure and exceptional geometry


[[!include Spin(8)-subgroups and reductions -- table]]


\linebreak

## Related concepts

[[!include low dimensional rotation groups -- table]]

* [[SU(2)]], [[SU(3)]]

\linebreak

## References

* {#FigueroaFarrill10} [[José Figueroa-O'Farrill]], _[PG course on Spin Geometry](https://empg.maths.ed.ac.uk/Activities/Spin/)_ lecture 8: _Parallel and Killing spinors_, 2010 ([pdf](https://empg.maths.ed.ac.uk/Activities/Spin/Lecture8.pdf))

[[!redirects SU(4)]]
