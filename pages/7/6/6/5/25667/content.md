# Contents
* this block creates the table of contents, leave as is
{: toc}

## Idea

A _pseudoform_ is a [[differential form]] that has been [[differential form|twisted]] by the [[pseudoscalar]] bundle.

Concretely, this means that when written in two (local) systems of
coordinates, the form transforms by an additional factor of $-1$
when the coordinate systems have opposite [[orientations]].
For a top-dimension pseudoform, this has the effect that at any given point,
the form has a consistent sign regardless of the [[orientation]] of the coordinates.

An $n$-pseudoform is the fundamental object of
[[integration of differential forms|integration on an $n$-manifold]].
In particular the [[volume]] (or area, or length) is a pseudoform.


## Definition

\begin{definition}
A __pseudoform__ on a [[manifold]] $X$ is a [[section]] of the
[[tensor product]] $\Lambda \otimes \Psi$, where

* $\Lambda$ is the [[exterior algebra]] of the [[cotangent bundle]] on $X$, and

* $\Psi$ is the [[pseudoscalar]] bundle on $X$.

\end{definition}

By comparison, an untwisted [[differential form]] is a [[section]] of
the [[exterior algebra]] $\Lambda$ itself.


## Properties

See also discussion under ["Twisted and vector-valued forms"](https://ncatlab.org/nlab/show/differential+form#twisted) at
[[differential form]].


### Correspondence to untwisted forms given orientation

For a pseudoform $\omega$ on an [[oriented manifold]] with orientation $o$, multiplying $\omega$ by the [[pseudoscalar field]] $1_o$ whose value at orientation $o$ is everywhere $1$ gives an untwisted form $\omega_o = 1_o \wedge \omega$. Similarly an untwisted form $\alpha$ corresponds to a pseudoform $1_o \wedge \alpha$.

As a result, on an [[orientable]] manifold, any pseudoform $\omega$ corresponds to two untwisted forms, one for each orientation, which differ only in sign. Conversely, on an orientable manifold any untwisted form corresponds to two pseudoforms differing only in sign.
Even when the manifold is [[nonorientable]], this correspondence holds locally because each point has an orientable neighborhood.

When working on a manifold with a chosen orientation, many authors conflate a pseudoform $\omega$ with the corresponding untwisted form $\omega_o$ and vice versa.


### Integration

When [[integration of differential forms|integrating differential forms]]
on an $n$-manifold, the most fundamental is the integration of $n$-pseudoforms.

This corresponds to how in multivariable calculus, the formula for
change of variables has a factor of the [[absolute value]] of the
[[determinant]] (just like for an $n$-pseudoform), and not of the
determinant itself (as one would have for an untwisted $n$-form).

With an orientation, one can of course also integrate (untwisted) $n$-forms;
this can be seen as using the orientation to convert the
$n$-form to an $n$-pseudoform and integrating that.

More generally one can integrate a $p$-pseudoform on an $n$-manifold $X$
if one has a $p$-[[submanifold]] $U$ to integrate over
and a [[pseudoorientation]] of $U$ in $X$.  See [[integration of
differential forms]].


## Examples

### Top-dimensional examples

The [[volume form|volume]] (or area, or length) on an $n$-manifold is an $n$-pseudoform.  On an [[oriented manifold]] one often speaks of a [[volume form]] as an untwisted $n$-form.

The [[absolute value of a form|absolute value]] of an untwisted $n$-form (on an $n$-manifold) is an $n$-pseudoform,
as is the [[absolute value of a pseudoform|absolute value]] of an $n$-pseudoform.

Alternatively, both of these examples can be thought of as [[absolute differential forms]]. On an $n$-manifold, an absolute $n$-form is equivalent to an $n$-pseudoform.


### Electromagnetism

In [[electromagnetism]], the current form $j$, measuring flux of [[electric charge|charge]],
is a 2-pseudoform.  This can be seen by considering how one integrates
it: you need a 2-surface together with a notion of which way _through_
the surface is forward and which is backward, or in other words
a [[pseudooriented]] surface.

By contrast the magnetic field strength $B$ is an untwisted 2-form.
To integrate $B$ over a surface $U$, one needs not a [[pseudoorientation]]
but an [[orientation]] of $U$ itself, identifying a direction
of circulation within the surface rather than a transverse direction
through the surface.

Traditionally in electromagnetism these look very similar because one
freely converts an orientation to a pseudoorientation and vice versa.
The tell when one does so is that it relies on an arbitrary choice of
orientation of the ambient 3-dimensional space, namely the [[right-hand rule]].
Comparing the right-hand rule to a left-hand rule, one gets the same physical meaning by integrating $j$ over the same surface with the same [[pseudoorientation]] (hence opposite [[orientations]]), confirming that the pseudoorientation is primary and $j$ is properly a pseudoform.
With $B$, one needs the same orientation on the surface (hence opposite pseudoorientations), confirming that the orientation is primary and $B$ is an untwisted form.


## References

Many useful explanations by [[Toby Bartels]] and [[John Baez]] in
[this long Usenet
thread](https://groups.google.com/g/sci.physics.research/c/aiMUJrOjE8A/m/0361hct91VsJ). In
particular:

* [Toby on absolute values, and getting a volume from a metric, 2001-12-23](https://groups.google.com/g/sci.physics.research/c/aiMUJrOjE8A/m/DiAumLzLdCcJ)

* [Toby on examples of pseudo- and untwisted forms in electromagnetism, 2002-02-08](https://groups.google.com/g/sci.physics.research/c/aiMUJrOjE8A/m/0361hct91VsJ)


[[!redirects differential pseudoform]]
[[!redirects differential pseudoforms]]
[[!redirects differential pseudo-form]]
[[!redirects differential pseudo-forms]]
[[!redirects differential pseudo form]]
[[!redirects differential pseudo forms]]
[[!redirects pseudoforms]]
[[!redirects pseudo-form]]
[[!redirects pseudo-forms]]
[[!redirects pseudo form]]
[[!redirects pseudo forms]]
[[!redirects p-pseudoform]]
[[!redirects p-pseudoforms]]
[[!redirects n-pseudoform]]
[[!redirects n-pseudoforms]]
[[!redirects pseudo-p-form]]
[[!redirects pseudo-p-forms]]
[[!redirects pseudo-n-form]]
[[!redirects pseudo-n-forms]]
[[!redirects pseudo p-form]]
[[!redirects pseudo p-forms]]
[[!redirects pseudo n-form]]
[[!redirects pseudo n-forms]]
