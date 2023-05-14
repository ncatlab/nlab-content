

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _model structure on simplicial groups_ is a presentation of the 
[[(∞,1)-category]] of [[∞-groups]] in [[∞Grpd]] $\simeq$ [[Top]]. See [[group object in an (∞,1)-category]].

## Definition

+-- {: .num_prop #ModelStructureOnSimplicialGroups} 
###### Proposition

There is a "projective" [[model category]] structure on the [[category]] $sGrp$ of [[simplicial groups]] where a morphism is

* a [[weak equivalence]] if the [[underlying]] morphism is a weak equivalence in the [[classical model structure on simplicial sets]], hence a [[simplicial weak homotopy equivalence]];

* a [[fibration]] if the underlying morphism is a fibration in the [[classical model structure on simplicial sets]], hence a  [[Kan fibration]];

* a [[cofibration]] if it has the [[left lifting property]] with respect to all [[acyclic fibrations]].

=--

([Quillen 67, II 3.7](#Quillen67), see also [Goerss-Jardine 99, V](#GoerssJardine99))


## Properties

### Further model category properties
 {#FurtherModelCategoryProperties}

\begin{proposition}\label{EveryObjectIsFibrant}
  Every object in the projective model structure (Prop. \ref{ModelStructureOnSimplicialGroups}) is [[fibrant object|fibrant]].
\end{proposition}
\begin{proof}
  This statement amounts to saying that the underlying simplicial set of any simplicial group is a [[Kan complex]], which is case by Moore's theorem ([here](simplicial+group#EverySimplicialGroupIsAKanComplex)).
\end{proof}

\begin{definition}\label{AlmostFreeMaps}
**(almost free maps)** \linebreak
A homomorphims of simplicial groups is called *almost free* if it is degreewise the inclusion into the [[amalgamation of groups|amalgamation]] with a [[free group]]

$$
  f_n 
    \,\colon\, 
  \mathcal{G}_n 
    \xhookrightarrow{\phantom{---}}
  \mathcal{G}_n \star F(S_n)
$$
in a compatible way.
\end{definition}
([Goerss & Jardine (1999), p. 270](#GoerssJardine99); [Speirs (2015), §A.4](#Speirs15))

\begin{proposition}\label{CharacterizationOfCofibrations}
In the model structure on simplicial groups (Prop. \ref{ModelStructureOnSimplicialGroups}):  

1. Every *almost free* homomorphism (Def. \ref{AlmostFreeMaps}) is a cofibration.

1. Every cofibration is a [[retract]] of an almost free map

In particular, since [[injections]] are closed under [[retracts]], every cofibration of simplicial groups has[[underlying]] it a [[monomorphism]] of [[simplicial sets]] and hence a [[cofibration]] in the [[classical model structure on simplicial sets]].
\end{proposition}
The first statement is proven in [Goerss & Jardine (1999) Cor. 1.10](#GoerssJardine99).

See also [Baues (1999), eq. (6)](#Baues99).


### Relation to reduced simplicial sets

+-- {: .num_prop #QuillenEquivalenceWithReducedSimplicialSets} 
###### Proposition
**([[Quillen equivalence between simplicial groups and reduced simplicial sets]])**

Forming [[simplicial loop space]] objects and [[simplicial classifying spaces]] gives a [[Quillen equivalence]]

$$
  \big(
    \Omega \dashv \overline{W}
  \big) 
  \;\colon\; 
  sGrp 
   \stackrel{\overset{}{\longleftarrow}}{\longrightarrow}
  sSet_0
$$

with the [[model structure on reduced simplicial sets]].

=--

([Goerss-Jardine 99, Chapter V, Prop. 6.3](#GoerssJardine99))


### Relation to simplicial groupoids

\begin{remark}
Forming simplicial [[delooping groupoids]] constitutes a [[fully faithful functor]] of [[1-categories]] from [[simplicial groups]] to [[sSet]]-[[enriched groupoids]] (DK-[[simplicial groupoids]]):

$$
  \array{
    sGrp &\hookrightarrow& sSet\text{-}Grpd
    \\
    \mathcal{G} &\mapsto& \mathbf{B}\mathcal{G}
    \mathrlap{\,.}
  }
$$

With respect to the above model structure (Prop. \ref{ModelStructureOnSimplicialGroups}) and the [[model structure on simplicial groupoids]], this functor clearly preserves the [[weak equivalences]] and [[fibrations]]. However, it does not have a [[left adjoint]] and thus fails to be a [[right Quillen functor]].
\end{remark}



## Related concepts

* [[model structure on simplicial groupoids]]

* [[Borel model structure]] (presenting [[infinity-actions]] of simplicial groups)

## References

The model structure on simplicial groups is due to:

* {#Quillen67} [[Daniel Quillen]], II §3.7 of: *[[Homotopical Algebra]]*, Lecture Notes in Mathematics **43**, Springer (1967) &lbrack;[doi:10.1007/BFb0097438](https://doi.org/10.1007/BFb0097438)&rbrack;

Further detailed discussion:

* {#GoerssJardine99} [[Paul Goerss]], [[J. F. Jardine]], chapter V of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))

Review:

* {#Speirs15} [[Martin Speirs]], *Model Categories with a view towards rational homotopy theory*, MSc thesis, Copenhagen (2015) &lbrack;[pdf](https://speirs.sites.ku.dk/files/2017/10/Master.pdf), [[Speirs-ModelCategories.pdf:file]]&rbrack;

See also:

* {#Baues99} [[Hans-Joachim Baues]], *Quadratic Homology*, Transactions of the American Mathematical Society **351** 2 (1999) &lbrack;[jstor:117809](https://www.jstor.org/stable/117809), [pdf](https://www.ams.org/journals/tran/1999-351-02/S0002-9947-99-02335-1/S0002-9947-99-02335-1.pdf)&rbrack;


