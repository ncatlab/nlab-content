
#Contents#
* table of contents
{:toc}


## Idea
The [[homotopy groups of spheres]] are a fundamental concept in [[algebraic topology]] and [[homotopy theory]]. They tell you about [[homotopy classes]] of maps from [[spheres]] to other spheres which can be rephrased as the collection of different ways to attach a sphere to another sphere. The [[homotopy type]] of a [[CW complex]] is completely determined by the homotopy types of the attaching maps.

Here's a quick reference for the state of the art on [[homotopy groups]] of spheres in HoTT. 

## Table

<table style="text-align:center">
  <tbody style="background:white">
    <tr>
      <th>n/k</th>
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
    </tr>
    <tr>
      <td>0</td>
      <td><a href="#pinsn">π<sub>0</sub>(S<sup>0</sup>)</a></td>
      <td><a href="#piksn">π<sub>0</sub>(S<sup>1</sup>)</a></td>
      <td><a href="#piksn">π<sub>0</sub>(S<sup>2</sup>)</a></td>
      <td><a href="#piksn">π<sub>0</sub>(S<sup>3</sup>)</a></td>
      <td><a href="#piksn">π<sub>0</sub>(S<sup>4</sup>)</a></td>
    </tr>
    <tr>
      <td>1</td>
      <td>π<sub>1</sub>(S<sup>0</sup>)</td>
      <td><a href="#pinsn">π<sub>1</sub>(S<sup>1</sup>)</a></td>
      <td style="background:#ffdddd"><a href="#piksn">π<sub>1</sub>(S<sup>2</sup>)</a></td>
      <td style="background:#ddffdd"><a href="#piksn">π<sub>1</sub>(S<sup>3</sup>)</a></td>
      <td style="background:#ddddff"><a href="#piksn">π<sub>1</sub>(S<sup>4</sup>)</a></td>
    </tr>
    <tr>
      <td>2</td>
      <td>π<sub>2</sub>(S<sup>0</sup>)</td>
      <td>π<sub>2</sub>(S<sup>1</sup>)</td>
      <td style="background:#ddddff"><a href="#pinsn">π<sub>2</sub>(S<sup>2</sup>)</a></td>
      <td style="background:#ffdddd"><a href="#piksn">π<sub>2</sub>(S<sup>3</sup>)</a></td>
      <td style="background:#ddffdd"><a href="#piksn">π<sub>2</sub>(S<sup>4</sup>)</a></td>
    </tr>
    <tr>
      <td>3</td>
      <td>π<sub>3</sub>(S<sup>0</sup>)</td>
      <td>π<sub>3</sub>(S<sup>1</sup>)</td>
      <td style="background:#ffffcc"><a href="#pi3s2">π<sub>3</sub>(S<sup>2</sup>)</a></td>
      <td style="background:#ddddff"><a href="#pinsn">π<sub>3</sub>(S<sup>3</sup>)</a></td>
      <td style="background:#ffdddd"><a href="#piksn">π<sub>3</sub>(S<sup>4</sup>)</a></td>
    </tr>
    <tr>
      <td>4</td>
      <td>π<sub>4</sub>(S<sup>0</sup>)</td>
      <td>π<sub>4</sub>(S<sup>1</sup>)</td>
      <td style="background:#ffdddd[pink]"><a href="#hopff">π<sub>4</sub>(S<sup>2</sup>)</a></td>
      <td style="background:#ddffdd"><a href="#pi4s3">π<sub>4</sub>(S<sup>3</sup>)</a></td>
      <td style="background:ddddff"><a href="#pinsn">π<sub>4</sub>(S<sup>4</sup>)</a></td>
    </tr>
  </tbody>
</table>


## At least one proof has been formalized

### Calculuation of $\pi_4(S^3)$ {#pi4s3}

* [[Guillaume Brunerie]] has proved that there exists an $n$ such that $\pi_4(S^3)$ is $\mathbb{Z}_n$.  Given a computational interpretation, we could run this proof and check that $n$ is 2. Added June 2016: Brunerie now has a proof that $n=2$, using cohomology calculations and a Gysin sequence argument.

### Calculuation of $\pi_3(S^2)$ {#pi3s2}

* [[Peter LeFanu Lumsdaine]] has constructed the Hopf fibration as a dependent type. Lots of people around know the construction, but I don't know anywhere it's written up. Here's some [Agda code](https://github.com/dlicata335/hott-agda/blob/master/homotopy/Hopf.agda) with it in it.
* [[Guillaume Brunerie]]'s proof that the total space of the Hopf fibration is $S^3$, together with $\pi_n(S^n)$, imply this by a long-exact-sequence argument.
* This was [formalized in Lean](https://github.com/leanprover/lean2/blob/master/hott/homotopy/sphere2.hlean) in 2016.

### $\pi_n(S^2)=\pi_n(S^3)$ for $n\geq 3$  {#hopff}

* This follows from the Hopf fibration and long exact sequence of homotopy groups.
* It was [formalized in Lean](https://github.com/leanprover/lean2/blob/master/hott/homotopy/sphere2.hlean) in 2016.

### Freudenthal Suspension Theorem  {#fsusp}

Implies $\pi_k(S^n) = \pi_{k+1}(S^{n+1})$ whenever $k \le 2n - 2$

* [[Peter LeFanu Lumsdaine]]'s encode/decode-style proof, [formalized](https://github.com/dlicata335/hott-agda/blob/master/homotopy/Freudenthal.agda) by [[Dan Licata]], using a clever lemma about maps out of two n-connected types.

### Calculuation of $\pi_n(S^n)$ {#pinsn}

* [[Dan Licata]] and [[Guillaume Brunerie]]'s [encode/decode-style proof using iterated loop spaces](https://github.com/dlicata335/hott-agda/blob/master/homotopy/PiNSN.agda) (for single-loop presentation).
* [[Guillaume Brunerie]]'s proof (for suspension definition).
* [[Dan Licata]]'s [proof from Freudenthal suspension theorem](https://github.com/dlicata335/hott-agda/blob/master/homotopy/PiSnSusp.agda) (for suspension definition).

### Calculuation of $\pi_k(S^n)$ for $k \lt n$ {#piksn}

* [[Guillaume Brunerie]]'s proof (see the book).
* [[Dan Licata]]'s encode/decode-style proof [for pi_1(S^2) only](https://github.com/dlicata335/hott-agda/blob/master/homotopy/Pi1S2.agda).
* [[Dan Licata]]'s encode/decode-style proof [for all k < n](https://github.com/dlicata335/hott-agda/blob/master/homotopy/PiKSNLess.agda) (for single-loop presentation).
* [[Dan Licata]]'s [proof from Freudenthal suspension theorem](https://github.com/dlicata335/hott-agda/blob/master/homotopy/PiSnSusp.agda) (for suspension definition).

### Calculuation of $\pi_2(S^2)$ {#pi2s2}

* [[Guillaume Brunerie]]'s proof using the total space the Hopf fibration.
* [[Dan Licata]]'s encode/decode-style [proof](https://github.com/dlicata335/hott-agda/tree/master/homotopy/pi2s2).

### Calculuation of $\pi_1(S^1)$ {#pi1s1}

* [[Mike Shulman]]'s proof by contractibility of total space of universal cover ([HoTT blog](http://uf-ias-2012.wikispaces.com/ofpost)).
* [[Dan Licata]]'s encode/decode-style proof ([HoTT blog](http://homotopytypetheory.org/2012/06/07/a-simpler-proof-that-%CF%80%E2%82%81s%C2%B9-is-z/)). A [paper](http://arxiv.org/abs/1301.3443) mostly about the encode/decode-style proof, but also describing the relationship between the two.
* [[Guillaume Brunerie]]'s proof using the flattening lemma.

category: homotopy theory
