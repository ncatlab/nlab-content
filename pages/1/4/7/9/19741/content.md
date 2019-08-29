
> This entry is about items in the [[ADE-classification]] labeled by $D4$. For the [[D4-brane]], see there.

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

In the [[ADE-classification]], the items labeled $D4$ include the following:

1. as [[finite subgroups of SO(3)]]:

   the [[Klein four-group]]  (the smallest [[dihedral group]])

   $\mathbb{Z}/2 \times \mathbb{Z}/2$

1. as [[finite subgroups of SU(2)]]:

   the [[quaternion group]] of [[order of a group|order]] 8 (the smallest [[binary dihedral group]]):

   $Q_8 \simeq 2 D_4$ 

1. as [[simple Lie groups]]: the [[special orthogonal group]] in 8 dimensions

   [[SO(8)]], [[Spin(8)]]

1. as a [[Dynkin diagram]]/[[Dynkin quiver]]: 

\begin{tikzpicture}
  \node (center) at (0,0) {};
  \node (topright) at (60:1) {};
  \node (botright) at (-60:1) {};
  \node (left) at (180:1) {};

  \draw[fill=black] (center) circle (.1);
  \draw[fill=black] (topright) circle (.1);
  \draw[fill=black] (botright) circle (.1);
  \draw[fill=black] (left) circle (.1);

  \draw (center) to (topright);
  \draw (center) to (botright);
  \draw (center) to (left);
\end{tikzpicture}


## Properties

### Triality

The [[symmetric group|S3]]-[[symmetry group]] of the D4-diagram translates into interesting 3-fold symmetries of structures associated with the corresponding objects in the above list. This is known as _[[triality]]_.

## Related concepts


[[!include ADE -- table]]
