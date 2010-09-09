Not to be confused with the unit of an [[adjunction]].

****

# Units
* table of contents
{: toc}

## Idea

A unit is a [[quantity]] $u$ such that every other quantity (of a certain type) is a multiple of $u$.


## Definitions

Exactly what this means depends on context.


### Units in rings

In a [[commutative ring]] (or [[rig]]) $R$, a __unit__ is an [[element]] of $R$ that has an [[inverse element|inverse]].  Of course, a commutative ring $R$ is a [[field]] just when every non-[[zero]] element is a unit.  In a noncommutative [[ring]], we distinguish _left_ and _right_ units.

If $u$ is a left unit in a ring, then any other element $x$ is a left multiple of $u$:
$$ x = (x u^{-1}) u .$$
Similarly, if $u$ is a right unit, then $x$ is a right multiple of $u$:
$$ x = u (u^{-1} x) .$$

### Units in modules

If $R$ is a commutative ring (or a rig) and $M$ an $R$-[[module]], then a __unit__ in $M$ is an element $m\in M$ such that every other $n\in M$ can be written as $n = r \cdot m$ for some $r\in R$.  This is the same as a [[generator]] of $M$ as an $R$-module.  If $R$ is noncommutative, we distinguish left and right units (or generators).  Note that a unit in $R$ _qua_ ring is the same as a unit in $R$ _qua_ $R$-module.

### Units of measurement

In [[physics]], the quantities of a given dimension generally form an $\mathbb{R}$-[[line]], a $1$-dimensional [[vector space]] over the [[real numbers]].  Since $\mathbb{R}$ is a field, any non-[[zero]] quantity is a unit, called in this context a __unit of measurement__.

Often (but not always) these quantities form an [[orientation|oriented]] line, so that nonzero quantities are either positive or negative.  Then we usually also require a unit of measurement to be positive.  In fact, for some dimensions, such as temperature, there is no meaning to a negative quantity, in which case the quantities actually form a module over the rig $\mathbb{R}_{\ge 0}$ and every nonzero element is "positive."

For example, the [[kilogramme]] is a unit of mass, because any mass may be expressed as a real multiple of the kilogramme.  Further, it is a positive unit; the mass of any physical object is a nonnegative quantity (so that mass quantities actually form an $\mathbb{R}_{\ge 0}$-module) and may be expressed as a nonnegative real multiple of the kilogramme.


[[!redirects unit]]
[[!redirects units]]

[[!redirects unit of measurement]]
[[!redirects unit of measurements]]
