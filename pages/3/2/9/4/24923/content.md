
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[quantum information theory]] a *bit flip code* is a [[quantum error correcting code]] to correct for [[quantum noise]] caused by [[bit flip channels]].

## Details

### 3-qbit flip code


The following basic example of a bit flip code encodes single [[logical qbits]] in [[triples]] of [[physical qbits]]. 


#### Idea


Here the [[Hilbert space]] 

$$
  LogicalQBit
  \;\coloneqq\;
  QBit \otimes QBit \otimes QBit
$$ 

of a single logical qbit has [[complex number|complex]] [[dimension of a vector space|dimension]] $2^3 \,=\, 8$. Inside this is the space of undisturbed logical qbits

\[
  \label{PureLogicalQBit}
  \begin{array}{ccccc}
    QBit
    \xrightarrow[\sim]{encode}
    DisturbedQBit_{0}
    &\overset{\phantom{---}}{\hookrightarrow}&
    LogicalQBit
    &\xrightarrow{
      P_{s = 0}
      \;\coloneqq\;
      \left\vert 0,0,0 \right\rangle
      \left\langle 0,0,0 \right\vert
      +
      \left\vert 1,1,1 \right\rangle
      \left\langle 1,1,1 \right\vert
    }&
    DisturbedQBit_0
    \\
    q_0 \left\vert 0 \right\rangle
    +
    q_1 \left\vert 1 \right\rangle
      &\mapsto&
    q_0 \left\vert 0, 0, 0 \right\rangle
    +
    q_1 \left\vert 1, 1, 1 \right\rangle    
  \end{array}
\]

as well as three further orthogonal subspaces which are the images of this one under one of the three *single* bit flips, respectively:

$$
  \begin{array}{ccc}
    DisturbedQBit_{1}
    &\overset{\phantom{---}}{\hookrightarrow}&
    LogicalQBit
    &\xrightarrow{
      P_{s=1}
      \;\coloneqq\;
      \left\vert 1,0,0 \right\rangle
      \left\langle 1,0,0 \right\vert
      +
      \left\vert 0,1,1 \right\rangle
      \left\langle 0,1,1 \right\vert
    }&
    DisturbedQBit_1
    \\
    q_0 \left\vert 0 \right\rangle
    +
    q_1 \left\vert 1 \right\rangle
    &\mapsto&
    q_0 \left\vert 1, 0, 0 \right\rangle
    +
    q_1 \left\vert 0, 1, 1 \right\rangle   
    \\
    {\phantom{A}}
    \\ 
    DisturbedQBit_{2}
    &\overset{\phantom{---}}{\hookrightarrow}&
    LogicalQBit
    &\xrightarrow{
      P_{s=2}
      \;\coloneqq\;
      \left\vert 0,1,0 \right\rangle
      \left\langle 0,1,0 \right\vert
      +
      \left\vert 1,0,1 \right\rangle
      \left\langle 1,0,1 \right\vert
    }&
    DisturbedQBit_2
    \\
    q_0 \left\vert 0 \right\rangle
    +
    q_1 \left\vert 1 \right\rangle
    &\mapsto&
    q_0 \left\vert 0, 1, 0 \right\rangle
    +
    q_1 \left\vert 1, 0, 1 \right\rangle   
    \\
    {\phantom{A}}
    \\ 
    DisturbedQBit_{3}
    &\overset{\phantom{---}}{\hookrightarrow}&
    LogicalQBit
    &\xrightarrow{
      P_{s=3}
      \;\coloneqq\;
      \left\vert 0,0,1 \right\rangle
      \left\langle 0,0,1 \right\vert
      +
      \left\vert 1,1,0 \right\rangle
      \left\langle 1,1,0 \right\vert
    }&
    DisturbedQBit_3
    \\
    q_0 \left\vert 0 \right\rangle
    +
    q_1 \left\vert 1 \right\rangle
    &\mapsto&
    q_0 \left\vert 0, 0, 1 \right\rangle
    +
    q_1 \left\vert 1, 1, 0 \right\rangle   
  \end{array}
$$

The 4 labels of these three subspaces are called the "error syndrome", which we collect in the 4-element set

$$
  Synd \;\coloneqq\; \{0,1,2,3\}
$$

to express the logical q-bit space alternatively in this linear basis:

$$
  QBit
  \xhookrightarrow{ encode }
  \underset{
    LogicalQBit
  }{
    \underbrace{
      QBit \otimes QBit \otimes QBit
    }
  }
  \xrightarrow[\sim]{
    (P_s)_{s \colon Synd}
  }
  \underset{  
    s \colon Synd
  }{\bigoplus}
  DisturbedQBit_{s}
$$

\begin{remark}
Beware that there is no room to record the further possible errors of 2 qbits flipping at once. Instead, this error process takes pure qbits to one of the subspaces reserved for single bit flips. Similarly, if all three bits flip at once, the initial pure state remains in the subspace reserved for pure states, but now with its phases mixed up. Therefore, the following error correction code fails on flips of more than one of the 3-qbits and will reduce the overall error probability only if single bit flips are sufficiently more likely than double and triple spin flips.
\end{remark}

The error correction now proceeds by:

1. Performing a [[quantum measurement]] of the above error syndrome $s$ on the logical Qbit space. While this measurement [[quantum state collapse|collapses]] the quantum state onto the subspace $DisturbedQBit_s$ the particular logical qbit states of the pure form (eq:PureLogicalQBit) lose no information under this collapse, in that there is a [[unitary operator]] on $DisturbedQBit_s$ which turns any such collapse state back into the original qbit state. 

1. applying this correcting unitary $X_s$, which is evidently the "[[Pauli matrix|Pauli X]]-" (or "[[NOT]]-")[[quantum gate]] $X \,\colon\, QBit \to QBit$ acting on the $s$-th qbit:

   $$
     \begin{array}{cccc}
       X_0 &\coloneqq& id \otimes id \otimes id
       \\
       X_1 &\coloneqq& X \otimes id \otimes id   
       \\
       X_2 &\coloneqq& id \otimes X \otimes id   
       \\
       X_3 &\coloneqq& id \otimes id \otimes X
     \end{array} 
     \;\;\;\colon\;\;\;
     \underset{
       LogicalQBit
     }{
       \underbrace{
         QBit \otimes QBit \otimes QBit
       }
     }
     \multimap
     \underset{
       LogicalQBit
     }{
       \underbrace{
         QBit \otimes QBit \otimes QBit
       }
     }
   $$

1. re-preparing a logical QBit from the recovered Qbit.


#### Circuit diagram and pseudo-code
 {#ThreeBitFlipCodeCircuitDiagramsAndPseudoCode}

In terms of [[quantum circuit diagrams]] and the [[schreiber:QS]]-[[pseudo-code]], the 3-bit flip error correcting code looks as follows (following the notation from *[[quantum circuits via dependent linear types]]*):

\begin{imagefromfile}
    "file_name": "QS_3BitFlipCodeIngredients-221125.jpg",
    "width": "720",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\linebreak

\begin{imagefromfile}
    "file_name": "QS_3BitFlipCode-221125.jpg",
    "width": "700",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


## Related concepts

* [[Æ code]]

* [[bit flip code]]

* [[stabilizer code]]

* [[HaPPY code]]

* [[Majorana dimer code]]

* [[surface code]] [[toric code]]



## References

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], §10.1.1 in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

* {#DevittNemotoMunro09} [[Simon J. Devitt]], Kae Nemoto, William J. Munro, §IV of: *Quantum Error Correction for Beginners*, Rep. Prog. Phys. **76** (2013) 076001 &lbrack;[arXiv:0905.2794](https://arxiv.org/abs/0905.2794), [doi:10.1088/0034-4885/76/7/076001](https://iopscience.iop.org/article/10.1088/0034-4885/76/7/076001)&rbrack;


[[!redirects bit flip codes]]

[[!redirects bit-flip code]]
[[!redirects bit-flip codes]]

[[!redirects quantum bit flip code]]
[[!redirects quantum bit flip codes]]

[[!redirects quantum bit-flip code]]
[[!redirects quantum bit-flip codes]]


[[!redirects 3 bit flip code]]
[[!redirects 3 bit flip codes]]

[[!redirects 3 bit-flip code]]
[[!redirects 3 bit-flip codes]]

[[!redirects three bit flip code]]
[[!redirects three bit flip codes]]

[[!redirects three bit-flip code]]
[[!redirects three bit-flip codes]]



