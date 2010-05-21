#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##
The **Kerr spacetime**(s) is a (family of) certain [[Lorentzian manifold]]s / [[spacetime]]s. 
The Kerr spacetime describes the ambient vacuum spacetime of a spherically symmetric rotating mass density, it can be extended in a way that this mass density degenerates to a singularity of spatial radius zero. This mathematical idealization is often said to describe a rotating black hole.

The Kerr spacetimes are parametrized by two parameters m and a that have the physical interpretation of mass and angular momentum per unit mass respectively, of the rotating object they describe. In the degenerate case of a = 0 the Kerr spacetimes reduce to the [[Schwartzschild spacetime]]s.

## Abstract ##
...

## Definition ##
The simplest description of the Kerr metric is by using spherical coordinates $r, \phi, \theta$ on the "space" $\mathbb{R}^3$ and a time coordinate $t \in \mathbb{R}$. In the context of the Kerr metric these coordinates are called **Boyer-Lindquist coordinates**.

The Kerr metric has two real parameters $m, a \ge 0$.

We define two functions mainly as an abbreviation:
$$
\rho^2 = r^2 + a^2 \cos^2(\theta )
$$ 

$$
\triangle = r^2 - 2 m r + a^2
$$ 

The following table lists the components of the metric of Minkowski, Schwartzschild and Kerr spacetimes respectivly using the canonical coordinates and the Boyer-Lindquist coordinates for the Kerr spacetime:

<table markdown="1" border="1">

<tr>
<th> metric</th>
<th> Minkowski </th>
<th> Schwartzschild </th>
<th> Kerr </th>
</tr>
<tr>
<td>$g_{tt}$</td>
<td>-1</td>
<td>$-1 + 2 \frac{m}{r}$</td>
<td>$-1 + 2 \frac{mr}{\rho^2}$</td>
</tr>

<tr>
<td>$g_{rr}$</td>
<td>+1</td>
<td>$\frac{r}{r - 2m}$</td>
<td>$\frac{\rho^2}{\triangle}$</td>
</tr>

<tr>
<td>$g_{\theta\theta}$</td>
<td>$r^2$</td>
<td>$r^2$</td>
<td>$\rho^2$</td>
</tr>

<tr>
<td>$g_{\phi\phi}$ </td>
<td>$r^2 \sin^2(\theta)$</td>
<td>$r^2 \sin^2(\theta)$</td>
<td>$(r^2 + a^2 + \frac{2 m r a^2 \sin^2(\theta)}{\rho^2}) \sin^2{\theta}$</td>
</tr>

<tr>
<td>$g_{ij}$ $i \neq j$</td>
<td>all zero</td>
<td>all zero</td>
<td>all zero except $g_{t \phi} = g_{\phi t} = - \frac{2 m r a \sin^2(\theta)}{\rho^2}$</td>
</tr>

</table>

## Properties ##
...

## Examples ##
...

## References ##

* Wikipedia on the [Kerr spacetime] (http://en.wikipedia.org/wiki/Kerr_spacetime).

Most textbooks about [[General Relativity]] have chapter about the Kerr spacetime, here is a monograph that specializes on the topic:

* Barrett O'Neill, _The geometry of Kerr black holes._ ([ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0828.53078&format=complete))

[[!redirects Kerr spacetimes]]
[[!redirects Kerr solution]]
[[!redirects Kerr metric]]
[[!redirects Boyer-Lindquist coordinates]]
[[!redirects Boyer-Lindquist]]