
> This entry is about items in the [[ADE-classification]] labeled by $D6$. For the [[D6-brane]], see there.

***


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the [[ADE-classification]], the items labeled $D6$ include the following:

1. as [[finite subgroups of SO(3)]]:

   the [[dihedral group of order 8]]

   $\mathbb{D}_8$

1. as [[finite subgroups of SU(2)]]:

   the [[binary dihedral group of order 16]]

   $2 D_8$ 

1. as [[simple Lie groups]]: the [[special orthogonal group]]/[[spin group]] in 12 dimensions

   [[SO(12)]], [[Spin(12)]]

1. as a [[Dynkin diagram]]/[[Dynkin quiver]]: 

\begin{tikzpicture}
  \node (center) at (0,0) {};
  \node (topright) at (60:1) {};
  \node (botright) at (-60:1) {};
  \node (left) at (-1,0) {};
  \node (D5) at (-2,0) {};
  \node (D6) at (-3,0) {};
  
  \draw[fill=black] (center) circle (.1);
  \draw[fill=black] (topright) circle (.1);
  \draw[fill=black] (botright) circle (.1);
  \draw[fill=black] (left) circle (.1);

  \draw[fill=black] (D5) circle (.1);
  \draw[fill=black] (D6) circle (.1);

  \draw (center) to (topright);
  \draw (center) to (botright);
  \draw (center) to (left);
  
  \draw (D5) to (left);
  \draw (D6) to (D5);
\end{tikzpicture}


## Related concepts


[[!include ADE -- table]]


