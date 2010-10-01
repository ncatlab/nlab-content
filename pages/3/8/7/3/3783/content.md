
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea ##

The **Kerr spacetime**(s) is a (family of) certain [[Lorentzian manifold]]s / [[spacetime]]s. 
The Kerr spacetime describes the ambient vacuum spacetime of a spherically symmetric rotating mass density, it can be extended in a way that this mass density degenerates to a singularity of spatial radius zero. This mathematical idealization is often said to describe a rotating black hole.

The Kerr spacetimes are parametrized by two parameters $m$ and $a$ that have the physical interpretation of mass and angular momentum per unit mass respectively, of the rotating object they describe. In the degenerate case of a = 0 the Kerr spacetimes reduce to the [[Schwartzschild spacetime]]s.

## Abstract ##
The definition states the components of the metric tensor in a specific coordinate system, the Boyer-Lindquist coordinates, and compares those to the Minkowski and Schwartzschild metrics. Some properties can be read off directly from the metric tensor, this is done in the properties paragraph.

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

One gets the [[Kerr-Newman metric]] for an electrically charged source with charge $e$ by replacing the definition of $\triangle$ with 

$$
\triangle = r^2 - 2 m r + a^2 + e^2
$$ 

The family of Kerr spacetimes is classified by the relation of the parameters $a$ and $m$:

* $0 = a$ gives Schwartzschild spacetime

* $0 \lt a^2 \lt m^2$ gives slowly rotating Kerr spacetime (**slow Kerr**)

* $a^2 = m^2$ gives **extreme Kerr spacetime** and

* $m^2 \lt a^2$ gives rapidly rotating Kerr spacetime (**fast Kerr**) 
 
## Properties ##
### Direct Consequences from the Definition ###
There are several coordinate singularities, inlcuding the z-axis (where $\sin(\theta) = 0$) and where $\rho = 0$ and $\triangle = 0$. Points where $\triangle = 0$ define the horizons of Kerr spacetime.

Both $\partial_t$ and $\partial_{\phi}$ are [[Killing vector field]]s, expressing the time invariance and the axial symmetry of the model respectively. Combining the sign changes $t \to -t, \phi \to -\phi$ gives an isometry: Letting time running backwards reverses the rotation.

Kerr spacetime is **asymptotically flat**, that is the Kerr metric approximates the Minkowski metric for large $r$.

### Boyer-Lindquist Blocks ###
The Boyer-Lindquist coordinates are defined on a subset of $\mathbb{R}^2 \times \mathcal{S}^2$ with $t, r$ defined on a copy of $\mathbb{R}$ respectively (actually $r$ is not supposed to take negative values, this definition is for convenience only). There are three subsets where the coordinates fail:

1. The **horizon H** where $\triangle = 0$.

2. The **ring singularity $\Sigma$** where $\rho^2 = 0$

3. The **axis A** where $\sin(\theta) = 0$.



+-- {: .un_def}
###### Definition
The **Boyer-Lindquist blocks I, II, III** are the following open subsets of $\mathbb{R}^2 \times \mathcal{S}^2 - \Sigma$:

1. For slow Kerr, there are two horizons at $r_{\pm}$,
$$
I: r \gt r_+ 
$$

$$
II: r_- \lt r \lt r_+ 
$$

$$
III: r \lt r_- 
$$

2. For extreme Kerr, there is a single horizon at $r = m$,
$$
I: r \gt m
$$

$$
III: r \lt m
$$
3. For fast Kerr, there is no horizon and $\mathbb{R}^2 \times \mathcal{S}^2 - \Sigma$ can be considered as one block I = III.
=--

Block I is also called the **Kerr exterior** and can be visualized as close to the Newtonian concept of space and time with a central force field.

+-- {: .un_theorem}
###### Theorem
**Causality of I and II**
The Boyer-Lindquist blocks I and II are causal.
=--

For a definition of causality see [[spacetime]].

+-- {: .un_theorem}
###### Theorem
**Noncausality of III**
The Boyer-Lindquist block III is vicious, that is for any two events $p, q$ in III there is a timelike future-pointing curve in III from p to q.
=--

## Examples ##
...

## References ##

* Wikipedia on the [Kerr spacetime] (http://en.wikipedia.org/wiki/Kerr_spacetime).

Most textbooks about [[General Relativity]] have chapter about the Kerr spacetime, here is a monograph that specializes on the topic:

* Barrett O'Neill, _The geometry of Kerr black holes._ ([ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0828.53078&format=complete))

[[!redirects Kerr spacetimes]]
[[!redirects Kerr solution]]
[[!redirects Kerr metric]]
[[!redirects Kerr black hole]]
[[!redirects Kerr-Newman black hole]]
[[!redirects Boyer-Lindquist coordinates]]
[[!redirects Boyer-Lindquist]]