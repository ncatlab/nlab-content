
+-- {: .num_prop #SuperSmoothSetsSystemOfAdjunctions}
###### Proposition
**(system of [[adjoint functors]] on [[SuperFormalSmoothSet]])**

There exists an essentially unique system of [[functors]] between the categories of [[sets]],
[[smooth sets]] (def. \ref{SmoothSet}), [[formal smooth sets]] and [[super formal smooth sets]] (def. \ref{FormalSmoothSets})
as shown in the second and third row of the following diagram, such that

1. every [[pair]] of consecutive [[functors]] is an [[adjoint pair]] ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjointFunctorsInTermsOfNaturalBijectionOfHomSets)), with the functor above being [[left adjoint]] and the functor below being [[right adjoint]]

1. on [[representables]] the top two functors on the left, the top two functors in the middle, and the top three functors on the right coincide with the corresponding functors between [[sites]] shown in the first row (from prop. \ref{SystemOfSites}):

<center>
<img src="https://ncatlab.org/nlab/files/AjunctionsForSuperCohesion.png" width="600">
</center>

In such a situation we also say that in the third row

1. the bottom four functors exhibit [[SuperFormalSmoothSet]] as a  [[cohesive topos]] ([this Def.](geometry+of+physics+--+categories+and+toposes#CohesiveTopos))

1. the middle four functors exhibit [[SuperFormalSmoothSet]] as [[differentially cohesive topos]] (elastic topos) relative to [[SmoothSet]] ([this Def.](https://ncatlab.org/nlab/show/geometry+of+physics+--+categories+and+toposes#DifferentialCohesion));

1. the top four functors exhibit $SuperFormalSmoothSet$ as _solid topos_ relative to [[FormalSmoothSet]] (...)

=--

+-- {: .proof}
###### Proof

That we have [[adjoint quadruples]] between [[presheaf toposes]] in the second row is by [this Example](geometry+of+physics+--+categories+and+toposes#KanExtensionOfAdjointPairIsAdjointQuadruple) in the chapter _[[geometry of physics -- categories and toposes|on categories and toposes]]_. 

That the [[adjoint quadruple]] on the left ([[corestriction|co-]])[[restriction|restricts]] to [[sheaves]], exhibiting [[SmoothSet]] as a [[cohesive topos]], is [this Prop.](geometry+of+physics+--+smooth+sets#SmoothSetsFormACohesiveTopos) in the chapter [[geometry of physics -- smooth sets|on smooth sets]].

For the other two [[adjoint quadruples]] the ([[corestriction|co-]])[[restriction|restricts]] to [[sheaves]] is trivial, since this concerns only the [[coverages]] along the infinitsimal directions in [[FormalCartSp]] and [[SuperFormalCartSp]], which are [[trivial coverage|trivial]] ([this Example](geometry+of+physics+--+categories+and+toposes#TrivialCoverage)), by definition.

This establishes the system of [[adjoint quadruples]] between [[sheaf toposes]] in the second row.

The diagram in the third row states that two extra adjoints to _composites_ of the functors appear. Here 

1. the [[right adjoint]] functor

   $$
     SmoothSet \longleftarrow SuperFormalSmoothSet
   $$ 

   exists as part of the [[adjoint quadruple]] which is induced ([this Example](geometry+of+physics+--+categories+and+toposes#KanExtensionOfAdjointPairIsAdjointQuadruple)) from the _[[composition|composite]]_ [[coreflective subcategory|coreflective inclusion]]

   $$
     CartSp
     \array{
       \overset{\phantom{A}\iota_{formal}\phantom{A}}{\hookrightarrow}
       \\
       \overset{\phantom{AA} \Re \phantom{AA}}{\longleftarrow} 
       \\
       \phantom{\overset{\phantom{AA} \Re \phantom{AA}}{\longleftarrow}}     
     }
     FormalCartSp
     \array{
       \overset{\phantom{A}\iota_{super}\phantom{A}}{\hookrightarrow}
       \\
       \overset{\phantom{AA} \Re \phantom{AA}}{\longleftarrow} 
       \\
       \phantom{\overset{\phantom{AA} \overset{\rightrightarrows}{(-)} \phantom{AA}}{\longleftarrow}}     
     }
     SuperFormalCartSp
   $$

   and using that composites of adjoints are adjoint, and that adjoints are unique, when they exist ([this prop.](geometry+of+physics+--+categories+and+toposes#UniquenessOfAdjoints))

1. Notice that also [[SuperFormalCartSp]] is a [[cohesive site]]: since the [[coverage]] along the infinitesimal directions is [[trivial coverage|trivial]], while that along the finite directions is the same as that on [[CartSp]], this follows with the same [[proof]] as for [[CartSp]] ([this Prop.](geometry+of+physics+--+smooth+sets#SmoothSetsFormACohesiveTopos)). 

   Moreover, the [[composition|composite]] 

   $$
     Disc_{SuperFormalSmoothSet}
     \;\colon\;
     Set 
       \hookrightarrow 
     SmoothSet 
       \hookrightarrow 
     FormalSmoothSet
       \hookrightarrow 
     SuperFormalSmoothSet
   $$

   from the second row above equals the functor 

   $$
     \array{
        Set 
          &\overset{Disc_{SuperFormalSmoothSet}}{\longrightarrow}&
        SuperFormalSmoothSet
        \\
        S &\mapsto& const_S
     }
   $$

   which is part of the [[adjoint quadruple]] of the [[cohesion]] of $SuperFormalSmoothSet$ (via [that Prop.](geometry+of+physics+--+smooth+sets#SmoothSetsFormACohesiveTopos))): This is because all these inclusion functors are [[right adjoints]], and hence [[preserved limit|preserve]] the [[terminal object]] $\ast$ ([this Prop.](geometry+of+physics+--+categories+and+toposes#LeftAdjointFunctorPreservesEpi)), but also [[left adjoints]], and hence [[preserved limit]] [[coproducts]] ([this Prop.](geometry+of+physics+--+categories+and+toposes#AdjointsPreserveCoLimits)). This implies the claim because every [[set]] is a [[coproduct]] of [[generalized the|the]] [[singleton]], which is the [[terminal object]] in [[Set]]. 

   This implies, again by uniqueness of adjoints ([this Prop.](geometry+of+physics+--+categories+and+toposes#UniquenessOfAdjoints)) that the composite functor $Set\longleftarrow SuperFormalSmoothSet$ from the previous item is in fact the functor $\Gamma_{SuperFormalSmoothSet}$ from the [[cohesive topos]]-structure on [[SuperFormalSmoothSet]] and hence, finally, that there is the bottom right adjoint 

   $$
     coDisc_{SuperFormalSmoothSet} \;\colon\; Set \overset{\phantom{AA}}{\hookrightarrow} SuperFormalSmoothSet
   $$ 

   as claimed.

Finally, that every second functor is a [[full subcategory]]  inclusion (a [[fully faithful functor]]) as shown follows because

1. left Kan extension along [[fully faithful functors]] is itself fully faithful ([this prop.](Kan+extension#LeftKanExtensionBasicProp));

1. in an [[adjoint triple]] the leftmost adjoint is [[fully faithful functor|fully faithful]] precisely if the rightmost adjoint is ([this prop.](adjoint+triple#FullyFaithful)).

=--
