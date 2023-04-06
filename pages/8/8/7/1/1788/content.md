But in the spirit of [[dependent linear type theory]] we may embed the situation along the [[reflective subcategory]]-inclusion

$$
  Vect 
  \underoverset
    {\hookrightarrow}
    {\overset{\mathrm{Q}}{\longleftarrow}}
    {\bot}
  Vect_{Set}
$$

into the category [[VectBund|$Vect_{Set}$]] of [[indexed sets]] $ (s \colon S) \mapsto \mathscr{V}_s$ of [[vector spaces]], which is a [[cartesian closed category]].

In the plain [[internal logic]] of [[VectBund|$Vect_{Set}$]] the above [[logical disjunction]] is quite different, in fact it coincides with the above conjunction (we abbreviate the [[singleton set|singleton]]-indexed vector space $(\cdot \colon \ast) \mapsto \mathscr{V}$ by $\mathscr{V}$):

<center>
<img src="/nlab/files/InternalLogicIninearSlicesOfVectSet-230406.jpg" width="600">
</center>

> wrong, of course

But under passage to the [slice adjunction](#adjoint+functor#OnSlices)

$$
  Vect_{/\mathcal{H}}
  \underoverset
    {\hookrightarrow}
    {\overset{\mathrm{Q}_{\!\!/\mathscr{H}}}{\longleftarrow}}
    {\;\;\; \bot \;\;\;}
  \big(
    Vect_{Set}
  \big)_{/\mathcal{H}}
$$

we recover in the internal $\mathrm{Q}$-logic of [[VectBund|$Vect_{Set}$]] the BvN disjunction as 

$$
  p_1 \vee_{BvN} p_2
  \;\;\;
  =
  \;\;\;
  \Big[
  \mathrm{Q}_{\!\!/\mathcal{H}}
  \big(
    \mathcal{P}_1 \sqcup \mathcal{P}_2
  \big)
  \Big]_{-1}
$$

<center>
<img src="/nlab/files/InternalQLogicInLinearSlicesOfVectSet-230406.jpg" width="600">
</center>
