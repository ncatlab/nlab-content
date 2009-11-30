[[!redirects Green–Schwarz mechanism]]

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Recall from the discussion at [[quantum anomaly]] the following situation:

* An action functional in [[path integral|path integral quantization]] is said to be [[quantum anomaly|anomalous]] if it is only locally identified with a function on the configuration space of fields, but is globally instead a section of a line [[bundle]] (usually equipped with [[connection on a bundle|connection]]).

* Given two anomalous action functionals in this sense, it may happen that while the two corresponding line bundles on configuration space are each nontrivial, their [[tensor product]] becomes trivializable. In this case one can consider the non-anomalous action function given by the sum of the two anomalous action functionals. This is what is called **anomaly cancellation** of one piece of an action functional against another. 

* The two main sources of examples for action functionals that are anomalous are

  * the standard action functional for chiral fermions 

    * this is a section of the Pfaffian line bundle for the Dirac operator

  * the action functional for [[differential cohomology|differential cocycles]] (higher connection, higher [[gauge theory]]) in the presence of [[electric charge|electric]] and [[magnetic charge]]s: 

    * this is a section of the transgression of the line bundle arising as the cup product of the electric and magnetic differential cocycles


A **Green--Schwarz mechanism** is the addition of an action functional for higher differential cocycles with [[magnetic charge]]s such that their anomaly cancels a given Pfaffian line bundle: so its a choice of by itself ill-defined action functional for higher gauge theory that cancels the ill-definedness of an action functional for chiral fermions.

More strictly speaking, _the_ Green--Schwarz mechanism is the application of this procedure in the theory called heterotic supergravity: there it so happens that the Pfaffian line bundle of the fermionic action has as Chern class the transgression of a 12 class that factorizes as $I_8 \wedge I_4$. Since heterotic supergravity contains a higher gauge field that couples to [[string theory|strings]], this is precisely of the form $J_{electric} \wedge J_{magnetic}$ that the anomaly for the corresponding higher gauge theory in the presence of magnetic charges gives rise to. So the original Green--Schwarz anomaly cancellation mechanism consist of modifying the "naive" action functional for heterotic supergravity by adding the contribution that corresponds to adding a magnetic current of the form

$$
  j_B := I_4
  \,.
$$

Further details for the moment at

* [Charges and Twisted Bundles, IV: Anomaly Cancellation](http://golem.ph.utexas.edu/category/2008/04/charges_and_twisted_bundles_iv.html)

