
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Trigonometry
+-- {: .hide}
[[!include trigonometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The sine function $\sin$ is one of the basic [[trigonometric functions]].

It may be thought of as assigning to any [[angle]] the [[distance]] to a chosen axis of the point on the [[unit circle]] with that angle to that axis.


## Definitions

The _sine function_ is the [[function]] $\sin \;\colon\; \mathbb{R} \to \mathbb{R}$ from the [[real numbers]] to themselves which is characterized by the following equivalent conditions:

1. $\sin$ is the unique [[solution]] among [[smooth functions]] to the [[differential equation]]/[[initial value problem]]

   $$ 
     sin'' = -sin 
   $$

   (where a prime indicates the [[derivative]]) subject to the initial conditions 

   $$ 
     \begin{aligned}
       sin(0) &= 0
       \\
       sin'(0) & = 1
       \,.
     \end{aligned}
   $$

1. ([[Euler's formula]]) $\sin$ is the [[imaginary part]] of the [[exponential function]] with imaginary argument

   $$
     \begin{aligned}
       \sin(x) & = Im\left( \exp(i x) \right)
       \\
       & = \frac{1}{2 i}\left( \exp(i x) - \exp(- i x)\right)
     \end{aligned}
     \,.
   $$

1. $\sin$ is the unique function which 

   1. is [[continuous function|continuous]] at $0$ 

   1. satisfies the [[inequality]]

      $$ 
        1 - x^2 \;\leq\; \frac{\sin(x)}{x} \;\leq\; 1 
      $$

      and the [[equation]]

      $$ 
        \sin(3 x) \;=\; 3 \sin(x) - 4 (\sin(x))^3 
      $$

   (see [Trimble](#Trimble): *[[toddtrimble:Characterization of sine]]*. Some additional discussion at the [nForum](https://nforum.ncatlab.org/discussion/5773/a-short-note-for-todd-trimble/).)

## Properties

### Relation to other functions

See at _[[trigonometric identity]]_.


### Roots

The [[roots]] of the sine function, hence the argument where its value is [[zero]], are the [[integer]] multiples of [[pi]] $\pi \in \mathbb{R}$.
 

## Related concepts

* [[cosine]]

* [[arcsine]]

* [[hyperbolic sine]], [[hyperbolic cosine]]

* [[exponential]], [[exponential ring]], [[Euler's formula]]

* [[trigonometric identity]] 

* [[pi]]

## References

* {#Trimble} [[Todd Trimble]], _[[toddtrimble:Characterization of sine]]_

See also

* Wikipedia, _[Sine](https://en.wikipedia.org/wiki/Sine)_

[[!redirects sin]]

[[!redirects sine function]]
[[!redirects sine functions]]