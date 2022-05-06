
> This entry is about items in the [[ADE-classification]] labeled by $D5$. For the [[D5-brane]], see there.

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

   the [[dihedral group of order 6]]

   $\mathbb{D}_6$

1. as [[finite subgroups of SU(2)]]:

   the [[binary dihedral group of order 12]]

   $2 D_6$ 

1. as [[simple Lie groups]]: the [[special orthogonal group]]/[[spin group]] in 10 dimensions

   [[SO(10)]], [[Spin(10)]]

1. as a [[Dynkin diagram]]/[[Dynkin quiver]]: 

\begin{tikzpicture}
  \node (center) at (0,0) {};
  \node (topright) at (60:1) {};
  \node (botright) at (-60:1) {};
  \node (left) at (-1,0) {};
  \node (D5) at (-2,0) {};
  
  \draw[fill=black] (center) circle (.1);
  \draw[fill=black] (topright) circle (.1);
  \draw[fill=black] (botright) circle (.1);
  \draw[fill=black] (left) circle (.1);

  \draw[fill=black] (D5) circle (.1);

  \draw (center) to (topright);
  \draw (center) to (botright);
  \draw (center) to (left);
  
  \draw (D5) to (left);
\end{tikzpicture}


## Related concepts


[[!include ADE -- table]]
