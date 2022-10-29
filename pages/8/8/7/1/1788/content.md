
## Idea

In [[quantum computing]] and [[quantum information theory]], the notion of *quantum random access memory* (QRAM, due to [Giovanettiy, Lloyd & Maccone 2008](#GiovanettiyLloydMaccone08)) is meant to be the [[quantum physics|quantum]]-analog of the [[classical physics|classical]] notion of [[random access memory]]; the key point being that QRAM may be addressed by *[[quantum superpositions]]* of address values and then reads/writes the corresponding [[quantum superposition]] of quantum data ([GLM08, (1)](#GiovanettiyLloydMaccone08)).

The original references on QRAM are soemwhat vague on the precise intended operational definition. But recall that a classical random access memory of [[data type]] $Mem$ is modeled (in terms of [[monads in computer science]]) by the [[state monad]] induced from the *[[cartesian monoidal category|cartesian]]* [[internal hom]]-[[adjoint functor|adjunction]] 

* [[product]]$\;$ $Mem \times (-) \;\;\dashv\;\; Maps(Mem, -)$ $\;$[[function set]]

namely:

$$
  RAM(Mem,A)
  \;\coloneqq\;
  Maps
  \big(
    Mem
    ,\,
    Mem 
    \times 
    A
  \big)
  \,.
$$

(Notice that in concrete applications people often insist that  $Mem =$ [[Bool]]${}^{\times^n}$, but the conceptual nature of RAM is indifferent to this choice.)

Now, with classical data types (such as [[bits]]) replaced by quantum data types (such as [[qbits]]), namely by *[[linear types]]*, the analogous [[internal hom]]-[[adjoint functor|adjunction]] is 

* [[tensor product]]$\;$ $ QMem \otimes (-) \;\;\dashv\;\; LinMaps(QMem, - )$ $\;$[[linear space]]-of-[[linear maps]]

and the corresponding [[monad]] is

$$
  QRAM(Mem,A)
  \;\coloneqq\;
  LinMaps
  \big(
    QMem
    ,\,
    QMem 
    \otimes
    A
  \big)
$$

and it seems clear that this does correspond to the intended behaviour of QRAM (where we are free to set $QMem \coloneqq $ [[QBit]]${}^{\otimes^n}$, if desired, which is typically the case in the literature).

In particular, the intended equivalence between the "QRAM model" and the "[[quantum circuit]]-model" of [[quantum computation]] is just the [hom-isomorphsim](adjoint+functor#InTermsOfHomIsomorphism) of the linear [[internal hom]]-[[adjunction]]

$$
  \Big\{
  In 
  \longrightarrow
  LinMaps
  \big(
    QMem
    ,\,
    QMem 
    \otimes
    Out
  \big)
  \Big\}
  \;\;\;\;\;\;\;
  \leftrightarrow
  \;\;\;\;\;\;\;  
  \Big\{
  In \otimes QMem
  \longrightarrow
  Out \otimes QMem
  \Big\}
  \,.
$$

## References

The terminology "quantum random access memory" is due to

* {#GiovanettiyLloydMaccone08} [[Vittorio Giovannetti]], [[Seth Lloyd]], [[Lorenzo Maccone]], *Quantum random access memory*, Phys. Rev. Lett. **100** 160501 (2008) &lbrack;[doi:10.1103/PhysRevLett.100.160501](https://doi.org/10.1103/PhysRevLett.100.160501), [arXiv:0708.1879](https://arxiv.org/abs/0708.1879)&rbrack;

but it could be argued (?) that the notion is implicit already in [Knill (1996)](quantum+programming+language#Knill96).

Further development:

* {#GiovanettiyLloydMaccone08b} [[Vittorio Giovannetti]], [[Seth Lloyd]], [[Lorenzo Maccone]], *Architectures for a quantum random access memory*, Phys. Rev. A **78** 052310 (2008) &lbrack;[doi:10.1103/PhysRevA.78.052310](https://doi.org/10.1103/PhysRevA.78.052310)&rbrack;



[[MeasurementViaWriterComonad-221027.jpg:file]]

[[MeasurementViaRandomMonad-221028.jpg:file]]

##  Idea

In [[quantum information theory]], a *controlled* [[quantum gate]] is a quantum gate whose operation on a given [[space of states]] is conditioned on the data in another space of "control states".

### The conceptual problem

The analogous situation for classical [[logic gates]] is without subtlety: Here the parameterization of a [[logic]] gate on $(n_{in}, n_{out})$-[[bits]] by $n_{ctrl}$ control bits is a choice of function

$$
  Bool^{n_{ctrl}}
  \xrightarrow{\;\;\; F_{\bullet} \;\;\;}
  Map
  \big(
    Bool^{n_{in}}
    ,\,
    Bool^{n_{out}}
  \big)
$$

from the intended set of controls to the [[set of functions]] between the intended input/output; and by the [[internal hom]]-[[adjoint functor|adjunction]] in the [[cartesian monoidal category]] of [[Sets]]  this is in [bijective correspondence ](adjoint+functor#InTermsOfHomIsomorphism) with a single function out of the [[Cartesian product]] set of the control bits with the input bits:
$$
  \array{
    Bool^{ n_{ctrl} + n_{in} }
    &\simeq&
    Bool^{ n_{ctrl} }
    \times
    Bool^{ n_{in} }
    &\xrightarrow{\;\;\;}&
    Bool^{ n_{out} }
    \\
    &&
    ( b_{ctrl}, b_in )
    &\mapsto&
    F_{b_{ctrl}}\big( b_{in} \big)
  }
  \,.
$$

This function would/could be called the "controlled logic gate". Notice that the control bits in the above function are "discarded after use", in that they cannot in general be recovered from the output of the above function.

The subtleties with generalizing this situation to [[quantum logic gates]] is:

1. The control of quantum gates may be either by quantum data or by classical data, which is not quite the same.

   \linebreak

   (In a *quantum-controlled* quantum logic gate, the control itself may be in a [[quantum superposition]], while a *classically-controlled* quantum gate is effectively an [[indexed set]] of quantum gates, indexed by classical data.)

1. A quantum-controlled quantum gate should, like any pure [[quantum logic gate]], be [[unitary]], in particular [[invertible]], hence it "must not discard" its control qbits.

   \linebreak

   This *rules out* the otherwise evident non-cartesian analog of the above classical situation (with the product operation replaced by the non-cartesian [[tensor product]] of [[finite dimensional vector space|finite-dimensional]] [[Hilbert spaces]], typically, and hence with the [[internal hom]] now being the corresponding linear space of linear maps)):

   $$
     \frac{
       QBit^{n_{ctrl}}
       \xrightarrow{\;\;\; F_\bullet \;\;\;}
       Map
       \big(
         QBit^{ n }   
         ,\,
         QBit^{ n }   
       \big)
     }{
       QBit^{n_{ctrl}}
       \otimes
       QBit^{n}
       \xrightarrow{\phantom{----}}
       QBit^{ n }
     }
   $$

   While the linear map at the bottom always exists, it cannot be invertible (unless the control is trivial, with $n_{ctrl} = 0$, or the state space is trivial, with $n = 0$) and hence does not qualify as a [[quantum logic gate]].


### The traditional notion
 {#IdeaTraditionalNotion}

A general and precise definition of controlled quantum gates is hard to find in traditional literature.

What traditional texbooks state (e.g. [Nielsen & Chuang (2000) §4.3](#NielsenChuang00)) is that for 
$$
  G \;\colon\; \mathscr{K} \longrightarrow \mathscr{K}
$$ 
a given [[quantum logic gate]], its version controlled by a single [[qbit]] is its [[direct sum]] with the [[identity map]], which may be thought of as the block-[[diagonal matrix|diagonal]]  [[matrix]]-notation with diagonal blocks being $G$ and the [[identity function]]:

$$
  \underset{
    QBit
  }{
    \underbrace{
      (\mathbb{C} \oplus \mathbb{C})
    }
  }
  \otimes 
  \mathscr{K}
  \;\simeq\;
  \mathscr{K} \oplus \mathscr{K}
  \xrightarrow{
    \;
    id \oplus G
    \,=\,
    \left[
    \begin{array}{cc}
      id & 0
      \\
      0 & G
    \end{array}
    \right]
    \;
  }
  \mathscr{K} \oplus \mathscr{K}
  \;\simeq\;
  \underset{
    QBit
  }{
    \underbrace{
      (\mathbb{C} \oplus \mathbb{C})
    }
  }
  \otimes 
  \mathscr{K}
$$

If we understand, as usual, that 

$$
  QBit
  \;\;\simeq\;\;
  \mathbb{C}\cdot \vert 0 \rangle
  \;\oplus\;
  \mathbb{C}\cdot \vert 1 \rangle
$$

then this gives a (invertible!) quantum gate on the tensor product space $QBit \otimes \mathscr{K}$, with the property that

1. $\vert 0 \rangle \,\otimes\, \vert \psi \rangle \;\;\mapsto\;\; \vert 0 \rangle \,\otimes\, \phantom{G}\vert \psi \rangle$

1. $\vert 1 \rangle \,\otimes\, \vert \psi \rangle \;\;\mapsto\;\; \vert 0 \rangle \,\otimes\, G\vert \psi \rangle$

In words: "*If the control Qbit is definitely set, then we operate with the $G$, if it is definitely not set then we operate trivially, and in general we operate with the respective superposition of these two actions.*"

A basic example of this construction is the [[controlled quantum NOT gate]].

### A formal definition

Given a ([[finite set|finite]]) [[set]] $B$ of "control parameter values" (typically $B =$ [[Bool]] = $\{0, 1\}$), a $B$-[[indexed set]] of [[quantum logic gates]] is a [[morphism]]

$$
  \begin{array}{rccc}
    &
    \mathscr{H}_\bullet
    &
    \xrightarrow{\;\;\; G_\bullet \;\;\;}
    &
    \mathscr{H}_\bullet
    \\
    b \colon B \;\; \vdash \;
    &
    \mathscr{H}_b
    &
    \xrightarrow{\;\;\; G_b \;\;\;}
    &
    \mathscr{H}_b
  \end{array}
$$

in a [[category]] $LinType_B$ of $B$-[[dependent linear types]] (typically: [[complex vector bundles]] over $B$), which is [[fiber]]-wise a [[linear map]] $G_b$ with given desired properties ([[invertible]], [[unitary]], ...).

As such, we may call this the **classically controlled quantum gate**, whose classical control parameter is $b \in B$ and whose quantum gate action for a given such parameter is $G_b$.

Typically the state spaces $\mathscr{H}_\bullet$ are independent of $b \colon B$, say equal to some $\mathscr{K},$ and only the quantum gates operating on a fixed state space $\mathscr{H}$ varies with the control parameter.

In this case, if we denote by

$$
  \mathscr{B}_\bullet
  \;\coloneqq\;
  (p_B)^\ast \mathbb{1}
  \,,\;\;\;
  \mathscr{B} 
  \;\coloneqq\;
  \Box_B \mathscr{B}_\bullet
$$

the quantum state space(s) of the control parameter,
then a classically $B$-controlled quantum gate is equivalently a morphism in $LinType_B$ between the [[external tensor products]] of $\mathscr{B}_\bullet$ with $\mathscr{K}$: 

$$
  \array{
    &
    \mathscr{B}_\bullet 
    \boxtimes
    \mathscr{K}
    &
    \xrightarrow{\phantom{----}}
    &
    \mathscr{B}_\bullet 
    \boxtimes
    \mathscr{K}
    \\
    b \colon B \;\; \vdash
    &
    \mathscr{K}
    &
    \xrightarrow{\phantom{--}G_b\phantom{--}}
    &
    \mathscr{K}
  }
$$

On the other hand, the corresponding **quantumly-controlled** quantum gate is the image of this under the [[necessity]]-[[comonad]] (in terms of *quantum modal logic*, see [here](necessity+and+possibility#ModalQuantumLogic)), hence under [[direct sum]]:

\[
  \label{QuantumlyControlledQuantumGate}
  \Box_B G_\bullet 
  \;\colon\;
  \Box_B \mathscr{H}_\bullet
  \;\simeq\;
  \underset{b \colon B}{\bigoplus}
  \mathscr{H}_b
  \xrightarrow{
    \;\;\;   
    \underset{b \colon B}{\oplus}
    G_b
    \;\;\;
  }
  \underset{b \colon B}{\bigoplus}
  \mathscr{H}_b
  \;\simeq\;
  \Box_B \mathscr{H}_\bullet
\]

\begin{imagefromfile}
    "file_name": "ParameterizedQuantumGates-221027.jpg",
    "width": "750",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


## Examples

* [[controlled NOT gate]] 

## Properties

* The *[[deferred measurement principle]]* interchanges classically-controlled with quantumly-controlled quantum gates.

## References

Traditional textbook accounts:

* {#NielsenChuang00} [[Michael A. Nielsen]], [[Isaac L. Chuang]], §4.3 *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;


