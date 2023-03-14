
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[computer science]], an *exception* is a nominal failure of a program which however is *handled* in some manner, so that the failing computation still terminates in a controlled way. 

In the simplest case this may mean that the program outputs an error message instead of continuing with the intended computation.

In terms of [[monads in computer science]], the *effect* of (possibly) throwing an exception is modeled by the [[monad]]:

1. which turns a given output [[data type]] into the [[coproduct type]] 

   $$ 
     D \;\mapsto\; D \sqcup Msg 
   $$ 
  
   with the intended type of handling/messages (typically $Msg = $ [[String (computer science)|string]]);

1. whose bind-operation on any $prog \colon D_1 \to D_2 \sqcup Msg$ is given by the [[codiagonal map]] $\nabla \;\colon\; Msg \sqcup Msg \;\to\; Msg$ as

   $$
     \phantom{\mathclap{\vert^{\vert^{\vert^{\vert^{\vert}}}}}}
     prog\big[-\big] 
     \;\coloneqq\; 
     D_2 \sqcup Msg 
     \xrightarrow{\; prog \sqcup Id_{Msg} \;} 
     D_3 \sqcup Msg \sqcup Msg 
     \xrightarrow{\; id_{D_3} \sqcup \nabla \;} 
     D_3 \sqcup Msg
     \,,
   $$

   meaning that whatever exception message has already been thrown gets carried further along.

If here $Msg = \ast$ is the [[unit type]], then the exception monad is also known as the *[[maybe monad]]*, modelling the effect that a program *may* fail, without however transmitting any further information about the failure.

## Related entries

* [[maybe monad]]

* [[writer monad]]

## References

Exception handling as a [[monad in computer science]]:

* [[Jiří Adámek]], Stefan Milius, Nathan Bowler, Paul B. Levy, *Coproducts of Monads on Set*, 27th Annual IEEE Symposium on Logic in Computer Science (2012) &lbrack;[arXiv:1409.3804](https://arxiv.org/abs/1409.3804), [doi:10.1109/LICS.2012.16](https://doi.org/10.1109/LICS.2012.16)&rbrack;


Lecture notes:

* {#Uustalu21} [[Tarmo Uustalu]], p. 11 in: *Monads and Interaction Lecture 1* lecture notes for [MGS 2021](https://staffwww.dcs.shef.ac.uk/people/G.Struth/mgs21.html) (2021) &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs1.pdf), [[Uustalu-Monads1.pdf:file]]&rbrack;


See also:

* Wikipedia, *[Exception handling](https://en.wikipedia.org/wiki/Exception_handling)*


[[!redirects exception monads]]

[[!redirects exception]]
[[!redirects exceptions]]

[[!redirects exception handler]]
[[!redirects exception handlers]]

[[!redirects exception handling]]
[[!redirects exception handlings]]



