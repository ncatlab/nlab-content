
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[electromagnetism]] the _Hall effect_ ([Hall 1879](#Hall1879)) is essentially the manifestation of the [[Lorentz force]] in [[conductors]]: 

It is the phenomenon that an [[electric current]] flowing [[perpendicular]] to a [[magnetic field]] induces an [[electric field]] perpendicular to both of these, sourced from the separation of positive and magnetic charge carriers in the current, which are driven apart by the [[Lorentz force]].

## Details

Write

* $B$ for the [[absolute value]] of the ambient [[magnetic field]];

* $E_{Hall}$ for the [[absolute value]] of the [[electric field]] induced by charge separation;

* $e$ for the [[electron]]'s [[electric charge]];

* $v$ for the [[absolute value]] of the drift [[velocity]] of the electrons in the material;

* $\rho$ for the [[number]] [[density]] of electrons;

* $j = \rho e v$ for the [[absolute value]] of the electric [[current]] [[density]].

Now, assuming, for simplicity and as usual, that the magnetic field and the electric current are both (as [[vector fields]]) constant in space and time as well as [[perpendicular]] to each other:

* the [[absolute value]] of the [[Lorentz force]] on the [[electrons]] is

  $$
    F_L = e v B
  $$

* the [[absolute value]] of the [[electrostatic force]] on the [[electrons]] is

  $$
    F_S = e E_{Hall}
  $$

* and hence in equilibrium $F_S = F_L$ we have

  $$
    E_{Hall} \;=\; v B 
    \,.
  $$

  This is called the _Hall electric field_.

In a [[conductor]] of extension $d$ perpendicular to both the current and the magnetic field (hence: along the electric field), this produces a [[voltage]]

$$
  V_{Hall} \;=\; d E_{Hall} \;=\; d v  B
  \,,
$$

called the _Hall voltage_.

In practice one typically refers to the _Hall resistance_ $R_{Hall}$, defined to be the ratio of Hall voltage over the electron current $J = A j$ through the cross-section [[area]] $A$ of the [[conductor]]:

$$
  R_{Hall}
  \;\coloneqq\;
  \frac{
    V_{Hall}
  }{
    J
  }
  \;=\;
  \frac{
    d
  }{
    A
  }
  \cdot
  \frac{
    v 
  }{
    \rho
  }
  \cdot
  \frac{
    B 
  }{
    e
  }
  \,.
$$

Here 

* the first factor on the right encodes the geometry of the [[conductor]];

* the second factor encodes the charge transport properties of its material;

* the third factor encodes the external magnetic field.


Since the first term is typicall known by construction,  knowledge of either of the remaining two terms makes the Hall effect applicable for _Hall sensors_ measuring the remaining term:

* when the material properties (second term) are known, the Hall effect serves in magnetometers (measuring the last term);

* when the external magentic field is known (the third term) the Hall effect provides information about the current and/or its conducting material (the second term).


## Related concepts

* [[quantum Hall effect]]

* [[spin Hall effect]], [[quantum spin Hall effect]]

## References

The original article:

* {#Hall1879} [[Edwin Hall]], _On a New Action of the Magnet on Electric Currents_, American Journal of Mathematics Vol. 2, No. 3 (Sep., 1879), pp. 287-292 ([doi:10.2307/2369245](https://doi.org/10.2307/2369245))

See also:

* Wikipedia, _[Hall effect](https://en.wikipedia.org/wiki/Hall_effect)_

[[!redirects Hall effects]]

[[!redirects Hall field]]
[[!redirects Hall fields]]

[[!redirects Hall voltage]]
[[!redirects Hall voltages]]

[[!redirects Hall resistance]]


