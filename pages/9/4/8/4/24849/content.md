
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The "ZX-calculus" is an elaboration for the purpose of [[qbit]]-based [[quantum computation]] of the [[string diagram]]-calculus used in [[quantum information theory via dagger-compact categories]].

The basic idea is to formalize the co-existence of the ubiquitous pair of [[quantum measurement|measurement]] [[linear basis|bases]] of [[qbits]] $QBit \simeq \mathbb{C}^2$, namely

1. the "computational basis" 

   $$
    \big\{ 
      \left\vert 0 \right\rangle
      ,\, 
      \left\vert 1 \right\rangle 
    \big\}
   $$ 

   which consists (by common convention) of the [[eigenstates]] of the [[Pauli-Z gate]];

1. the [[Hadamard gate|Hadamard]] basis 

   $$
     \Big\{ 
       \tfrac{1}{\sqrt{2}} 
       \big(
         \left\vert 0 \right\rangle 
         \pm 
         \left\vert 1 \right\rangle  
       \big) 
     \Big\}
   $$ 

   which consists of the [[eigenstates]] of the [[Pauli-X gate]];

by observing &lbrack;[Coecke & Duncan, p. 1](#CoeckeDuncan)&rbrack; that:

1. either equips $QBit = \mathbb{C}^2$ with a [[Frobenius algebra]]-[[structure]] (associated to the [[Frobenius monad]]-[[structure]] of the corresponding [[quantum reader monad]] as originally observed by &lbrack;[Coecke & Pavlović (2008)](quantum+measurement#CoeckePavlović08)&rbrack;);

1. jointly these make a certain [[bialgebra]]-strucuture, algebraically reflecting the fact that they are [[mutually unbiased bases]].

It is this bi-algebraic formalizaton of the interaction between the "Pauli-Z basis" and the "Pauli-X basis" for [[qbits]] which gives the ZX-calculus its name.

Graphically, the ZX-calculus proceeds to declare that: 

1. the [[comultiplication|(co-)]][[multiplication]] and [[counit|(co)-]][[unit]] [[string diagrams]] of these two [[Frobenius algebra]]-structures are to be denoted

   1. in green for the Z-basis

   1. in red for the X-basis

1. [[connected topological spaces|connected]] sub-[[string diagrams]] formed from (co-)multiplications and (co-)units  all of the same color are shown as a single box/circle with the given number of in/outputs -- then called *spiders*

   (since the [[Frobenius algebra]]-property ensures --- recalled as [Coecke & Duncan (2011), Theorem 1](#CoeckeDuncan11) --- that any connected diagrams are equal iff they have the same number of in/outputs).


* ...

(...)

## References

Landing page:

* [zxcalculus.com](https://zxcalculus.com/)

The ZX-calculus has its origin as a tool for organizing [[measurement-based quantum computation]]-protocols, following [Danos, Kahsefi & Panangaden (2007)](measurement-based+quantum+computation#DanosKahsefiPanangaden07):

* [[Ross Duncan]], [[Simon Perdrix]], *Rewriting Measurement-Based Quantum Computations with Generalised Flow*, in: *Automata, Languages and Programming. ICALP 2010*, Lecture Notes in Computer Science **6199**, Springer (2010) &lbrack;[doi:10.1007/978-3-642-14162-1_24](https://doi.org/10.1007/978-3-642-14162-1_24)&rbrack;

The official introduction of the ZX-calculus:

* {#CoeckeDuncan} [[Bob Coecke]], [[Ross Duncan]], *A graphical calculus for quantum observables* &lbrack;[pdf](https://www.cs.ox.ac.uk/people/bob.coecke/GreenRed.pdf)&rbrack;

* {#CoeckeDuncan08} [[Bob Coecke]], [[Ross Duncan]], *Interacting Quantum Observables*, in *Automata, Languages and Programming. ICALP 2008*, Lecture Notes in Computer Science **5126**, Springer (2008) &lbrack;[doi:10.1007/978-3-540-70583-3_25](https://doi.org/10.1007/978-3-540-70583-3_25)&rbrack;

* {#CoeckeDuncan11} [[Bob Coecke]], [[Ross Duncan]], *Interacting Quantum Observables: Categorical Algebra and Diagrammatics*, New J. Phys. **13** (2011) 043016 &lbrack;[arXiv:0906.4725](http://arxiv.org/abs/0906.4725), [doi:10.1088/1367-2630/13/4/043016](https://doi.org/10.1088/1367-2630/13/4/043016)&rbrack;

Textbook account:

* [[Bob Coecke]], [[Stefano Gogioso]], *Quantum in Pictures*, [Quantinuum Publications](https://www.quantinuum.com/publications) (2023) &lbrack;[ISBN 978-1739214715](https://www.amazon.co.uk/dp/1739214714), [Quantinuum blog](https://www.quantinuum.com/news/quantum-in-pictures)&rbrack;

Relation to [[braided fusion categories]] for [[anyon]] [[braiding]]:

* [[Fatimah Rita Ahmadi]], [[Aleks Kissinger]], *Topological Quantum Computation Through the Lens of Categorical Quantum Mechanics* $[$[arXiv:2211.03855](https://arxiv.org/abs/2211.03855)$]$

See also:

* Razin A. Shaikh, Quanlong Wang, Richie Yeung, *How to sum and exponentiate Hamiltonians in ZXW calculus* &lbrack;[arXiv:2212.04462](https://arxiv.org/abs/2212.04462)&rbrack;


(...)

[[!redirects ZX calculus]]

[[!redirects zx-calculus]]
