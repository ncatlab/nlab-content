
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

In the [[ADE-classification]], the items labeled $A3$ include the following:

1. as [[finite subgroups of SO(3)]]:

   the [[cyclic group]]  

   $\mathbb{Z}/4$

1. as [[finite subgroups of SU(2)]]:

   the [[dicyclic group]]  

   $Dic_1 \simeq \mathbb{Z}/4$

1. as [[simple Lie groups]]: the [[special unitary group]] in 4 complex dimensions

   [[SU(4)]]

1. as a [[Dynkin diagram]]/[[Dynkin quiver]]: 

\begin{tikzpicture}
  \node (center) at (0,0) {};
  \node (left) at (-1,0) {};
  \node (right) at (1,0) {};

  \draw[fill=black] (center) circle (.1);
  \draw[fill=black] (left) circle (.1);
  \draw[fill=black] (right) circle (.1);

  \draw (center) to (left);
  \draw (center) to (right);
\end{tikzpicture}

\linebreak

## Properties

### Exceptional isomorphism
  {#ExceptionalIsomorphism}

The A3 [[Dynkin diagram]] coincides with the [[D3]] diagram, hence with the result of removing one node from the [[D4]] diagram. In the [[classification of simple Lie groups]] this coincidence reflects the exceptional [[isomorphism]] between [[SU(4)]] and [[Spin(6)]]:


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



## Related concepts


[[!include ADE -- table]]

[[!redirects D3]]

