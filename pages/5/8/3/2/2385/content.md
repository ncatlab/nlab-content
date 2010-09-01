

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

In a context of [[synthetic differential geometry]], the _de Rham space_ $dR(X)$ of a [[space]] $X$ is the quotient of $X$ that identifies [[infinitesimal object|infinitesimally close points]].

> [[nPOV]] claim:

The deRham space $dR(X)$ of a [[space]] $X$ is a [[decategorification]] of its [[schreiber:infinitesimal path ∞-groupoid]] $\Pi^{inf}(X)$.

## Definition 

### General definition

In [[synthetic differential geometry]] to every 
[[space]] $X$ is associated its [[infinitesimal singular simplicial complex]] $X^{(\Delta^\bullet_{inf})}$ -- which may be thought of as modelling the [[schreiber:infinitesimal path ∞-groupoid]]
$\Pi^{inf}(X)$. 

The **deRham space** $dR(X)$ of $X$ is the [[decategorification]] of this [[Lie ∞-groupoid]]: the space of its equivalence classes i.e. the space of which $\Pi^{inf}(X)$ is a [[simplicial resolution]].

Typically the [[space]]s $X$ here are modeled as [[sheaf|sheaves]], an object in the [[category of sheaves]] $\Sh(C)$ for some suitable [[site]] and the 
[[Lie ∞-groupoid]] $\Pi^{inf}(X)$ [[models for ∞-stack (∞,1)-toposes|is modeled]] as a [[simplicial presheaf|simplicial sheaf]] $\Pi^{inf}(X) \in [\Delta^{op}, Sh(C)]$. In that case the deRham space is the [[coequalizer]]
 
$$
  colim(
  \Pi^{inf}(X)_1 \rightrightarrows
  \Pi^{inf}(X)_0 )
  = 
  colim(
   X^{(\Delta^1_{inf})} \rightrightarrows
   X)
  )
  =
  dR(X)
$$

(where $D$ is the [[infinitesimal space|infinitesimal interval]]).

### On $Rings^{op}$

In a context where the spaces in question are modeled as [[sheaf|sheaves]] on
the [[opposite category|opposite]] of a category of [[ring]]s, i.e. notably in the context 
of [[scheme]]s, there is another definition of $dR(X)$:

in this case there is an evident functor $Red : Spaces \to Spaces$ that sends each space to its _reduced_ subspace, dually characterized by sending each ring to the quotient by its nilpotent elements.

Then $dR' : Spaces \to Spaces$ may be defined as the [[right adjoint]] to $Red$. 

This definition coincides with the previous one on 
those spaces that are [[formally smooth scheme]]s. In fact, a [[scheme]] $X$ is [[formally smooth scheme|formally smooth]] precisely if the [[right adjoint]] of $Red$ applied to $X$ coincides with the coequalizer of $(X^{(\Delta^1_{inf})} \rightrightarrows X)$.

## Related concepts 

### Grothendieck connection

Morphisms out of the [[schreiber:infinitesimal path ∞-groupoid]] encode flat higher [[connection on a bundle|connections]]: [[local system]]s.

Accordingly, [[descent]] for deRham spaces -- sometimes called **deRham descent** encodes flat 1-connections. This is described at [[Grothendieck connection]], 

### D-modules

The category of [[D-module]]s on a [[space]] is equivalent to that of [[quasicoherent sheaf|quasicoherent sheaves]] on the corresponding deRham space. 

Accordingly, quasicoherent $\infty$-stacks on the full $\Pi^{inf}(X)$ encode a higher categorical version of this, as discussed at [[schreiber:∞-vector bundle]].

## References

The deRham space construction on spaces ([[scheme]]s) is described in [section 3, p. 7](http://math.berkeley.edu/~teleman/math/simpson.pdf#page=7)

* [[Carlos Simpson]], [[Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))

which goes on to assert the existence of its [[derived functor]] on the [[homotopy category]] $Ho Sh_\infty(C)$ of [[∞-stack]]s in proposition 3.3. on the same page.

The characterization of [[formally smooth scheme]] as above is also on that page.

>Notice that as of the time of this writing this is an unfinished document. See the remark on [[Constantin Teleman]]'s website [here](http://math.berkeley.edu/~teleman/lectures.html). One of the $n$Lab contributors ([[Urs Schreiber]]) is grateful to [[David Ben-Zvi]] for pointing out this work in blog discussion [here](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit.html#c023287) -- mentioning also the relation to [[D-module]]s --  and [here](http://golem.ph.utexas.edu/category/2009/08/question_on_synthetic_differen.html#c026218). See also some remarks and warnings at MO, [the answer by Ben-Zvi](http://mathoverflow.net/questions/10556/d-modules-derham-spaces-and-microlocalization).



[[!redirects deRham space]]
