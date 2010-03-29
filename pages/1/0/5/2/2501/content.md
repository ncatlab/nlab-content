#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

Ordinary [[classical mechanics]] of point particles may be regarded as the theory of [[action functional]]s on [[mapping space]]s of maps from the real line to some space.

In _classical [[field theory]]_ one instead studies functionals on [[mapping space]]s on higher dimensional domains.


## classical gauge theory ##

Of particular interest are classical field theories that are [[gauge theory|gauge theories]]. A powerful formalism for handling these is provided by [[BV theory]], which effectively realizes spaces of classical fields as [[Lie infinity-algebroid|∞-Lie algebroid]]s. BV-formalism can be understood as a means to capture a classical gauge field theory in such a way that it lends itself to [[quantization]]. (See below)


## examples ##

Important examples of classical field theories are

* [[electromagnetism]]

* [[gravity]], [[supergravity]]

+--{: .query}
[[Ian Durham]]: I've never heard of supergravity as being considered a _classical_ theory before.  Isn't the spin structure it is imbued with inherently quantum mechanical in nature?  I've never even seen it in anything other than a quantum field theory book (i.e. I've never seen it in a GR or GR-related book)?

Zoran: criterium on which book is irrelevant. It is easy to see in any treatment, that one has a classical version first and then quantization. 

Tim van Beek: There may be some confusion because spin in physics is a quantum phenomenon, and "supertheories" try to unify the treatment of fermions and bosons, who are again pure quantum terms. But that does not imply that e.g. a spin structure on a manifold would be considered to be a "quantum structure": Take a smooth mainifold and put a bundle structure on it: That is still a "classical object" for mainstream physics. Same thing with supergravity. Both become "quantum objects" if you build a Hilbert space of states and turn your observables into operators on this space, for example (see [[geometric quantization]]).

[[Ian Durham]]: Well, true, but in my personal experience it doesn't take on any physical meaning until it is quantized (in this case).  In other words, while I'm not necessarily disputing what you're saying, I'm saying it's a little misleading to list it under "classical field theory" without some accompanying caveat.
=--

## quantizaton of classical field theory ##

When it was realized that fundamental physics is governed by [[quantum field theory]] it became clear that classical field theory of fundamental fields can only be an approximation to the corresponginf [[quantum field theory]]. If we think of quantum field theory in terms of [[FQFT|functorial quantum field theory]], then the domains of the mapping spaces mentionmed above are the [[cobordism]]s that this [[FQFT]] is a functor on. The [[quantization]] of classical field theories to [[quantum field theories]] is a major issue in theoretical and mathematical [[physics]] (see also [[renormalization]]).