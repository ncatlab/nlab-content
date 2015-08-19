
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

_Higher Klein geometry_ is the generalization of [[Klein geometry]] from traditional ([[differential geometry|differential]]) [[geometry]] to [[higher geometry]]:

where Klein geometry is about ([[Lie group|Lie]]) [[groups]] and their [[quotient]]s, higher Klein geometry is about ([[smooth infinity-group|smooth]]) [[∞-groups]] and their [[groupoid object in an (∞,1)-category|∞-quotients]].

The way that the generalization proceeds is clear after the following observation.

+-- {: .num_prop}
###### Observation

Let $G$ be a [[discrete group]] and $H \hookrightarrow G$ a subgroup. Write $\mathbf{B}G$ and $\mathbf{B}H$ for the corresponding [[delooping]] [[groupoid]]s with a single object. Then the [[action groupoid]] $G//H$ is the [[homotopy fiber]] of the inclusion [[functor]]

$$
  \mathbf{B}H \to \mathbf{B}G
$$

in the [[(2,1)-category]] [[Grpd]]: we have a [[fiber sequence]]

$$
  G//H \to \mathbf{B}H \to \mathbf{B}G
$$

that exhibits $G//H$ as the $G$-[[principal bundle]] over $\mathbf{B}H$ which is classified by the [[cocycle]] $\mathbf{B}H \to \mathbf{B}G$.

Moreover, the [[decategorification]] of the [[action groupoid]] (its [[0-truncated|0-truncation]]) is the ordinary [[quotient]]

$$
  \tau_0 (G//H) = G/H
  \,.
$$ 

=--

+-- {: .proof}
###### Proof

This should all be explained in detail at [[action groupoid]]. 

The fact that a [[quotient]] is given by a [[homotopy fiber]] is a special case of the general theorem discussed at [∞-colimits with values in ∞Grpd](http://ncatlab.org/nlab/show/limit+in+a+quasi-category#WithValInooGrpd)

=--

+-- {: .num_remark}
###### Remark

That fiber sequence continues to the left as

$$
  H \to G \to G//H \to \mathbf{B}H \to \mathbf{B}G
  \,.
$$

=--

+-- {: .num_prop}
###### Observation

The above statement remains true _verbatim_ if [[discrete group]]s are generalized to [[Lie group]]s -- or other [cohesive groups](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#InfinGroups) --  if only we pass from the [[(2,1)-topos]] [[Grpd]] of [[discrete groupoid]]s to the [[(2,1)-topos]] [[Smooth∞Grpd|SmoothGrpd]] of _smooth groupoids_ . 

=--

This follows with the discussion at [[smooth ∞-groupoid -- structures]].

Since the quotient $G/H$ _is_ what is called a _[[Klein geometry]]_ and since by the above observations we have analogs of these quotients for [higher cohesive groups](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+structures#InfinGroups), there is then an evident definition of _higher Klein geometry_  :

## Definition

Let $\mathbf{H}$ be a choice of [[cohesive (∞,1)-topos|cohesive structure]]. For instance choose

* $\mathbf{H} = $ [[Disc∞Grpd]] for discrete higher Klein geometry (no actual geometric structure);

* $\mathbf{H} = $ [[ETop∞Grpd]] for continuous higher Klein geometry (with [[topological structure]]);

* $\mathbf{H} = $ [[Smooth∞Grpd]] for higher Klein geometry based on [[differential geometry]];

* $\mathbf{H} = $ [[SuperSmooth∞Grpd]] for the [[supergeometry]] version of higher Klein geometry

* and so on.

+-- {: .num_defn}
###### Definition

An **$\infty$-Klein geometry** in $\mathbf{H}$ is a [[fiber sequence]] in $\mathbf{H}$ 

$$
  G//H \to \mathbf{B}H \stackrel{i}{\to} \mathbf{B}G
$$

for $i$ any morphism between two [[connected]] objects, as indicated, hence $\Omega i : H \to G$ any morphism of [[∞-group]] objects.

=--

+-- {: .num_remark}
###### Remark

For $X$ an object equipped with a $G$-[[action]] and $f : Y \to X$ any morphism, the higher Klein geometry induced by "the shape $Y$ in $X$" is given by taking $i : H \to G$ be the [[stabilizer ∞-group]] $Stab(f) \to G$ of $f$ in $X$. See there at _[Examples -- Stabilizers of shapes / Klein geometry](stabilizer+group#KleinGeometry)_.

=--

+-- {: .num_remark}
###### Remarks


* By the discussion at [[looping and delooping]], and using that a [[cohesive (∞,1)-topos]] has [[homotopy dimension]] 0 it follows that  every connected object indeed is the delooping of an [[∞-group]] object.

* The above says that $G//H$ is the [[principal ∞-bundle]] over $\mathbf{B}H$ that is classified by the [[cocycle]] $i$.

  Continuing this [[fiber sequence]] further to the left yields the long fiber sequence

  $$
    H \to G \to G//H \to \mathbf{B}H \stackrel{i}{\to} \mathbf{B}G
  $$

  This exhibits $G$ indeed as the [[fiber]] of $G//H \to \mathbf{B}H$.

=--

## Examples

### Higher super Poincar&#233; Klein geometry

Let $\mathbf{H} = $ [[SuperSmooth∞Grpd]] be the context for [[SynthDiff∞Grpd|synthetic]] [[higher geometry|higher]] [[supergeometry]]. 

Write $\mathfrak{sugra}_11$ for the [[super L-∞ algebra]] called the [[supergravity Lie 6-algebra]]. This has a sub-super $L_\infty$-algebra of the form

$$
  \mathbf{B}(\mathfrak{so}(10,1) \oplus b \mathbb{R} \oplus b^{5}\mathbb{R})
  \hookrightarrow
  \mathbf{B}\mathfrak{sugra}_11
  \,,
$$

where 

* $\mathfrak{so}(d,1)$ is the [[special orthogonal Lie algebra]];

* $b^{n-1} \mathbb{R}$ is the [[line Lie n-algebra]].

The quotient

$$
  \mathfrak{sugra}_11 / 
  ((\mathfrak{so}(10,1) \oplus b \mathbb{R} \oplus b^{5}\mathbb{R}))
$$

is the [[super translation Lie algebra]] in 11-dimensions.

This higher Klein geometry is the local model for the [[higher Cartan geometry]] that describes [[11-dimensional supergravity]]. See [[D'Auria-Fre formulation of supergravity]] for more on this.



## Related concepts

[[!include local and global geometry - table]]

## References

That there ought to be a systematic study of higher Klein geometry and [[higher Cartan geometry]] has been amplified by [[David Corfield]] since 2006.

Such a formalization is offered in 

* [[schreiber:differential cohomology in a cohesive topos]]

For more on this see at _[[higher Cartan geometry]]_ and _[[schreiber:Higher Cartan Geometry]]_.

[[!redirects higher Klein geometries]]