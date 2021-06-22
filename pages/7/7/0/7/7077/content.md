
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _locally cartesian closed model category_ is a [[locally cartesian closed category]] which is equipped with the structure of a [[model category]] in a compatible way, namely such that all right [[base change]]-[[adjunctions]] along [[fibrations]] are [[Quillen adjunctions]], hence such that all their [[dependent product]]-functors are [[right Quillen functors]].

\begin{remark}\label{RelationToCartesianClosedModelCategories}
**(relation to [[cartesian closed model categories]])** \linebreak
Beware that, despite the terminology, the axioms on a locally cartesian closed model category (Def. \ref{LocallyCartesianClosedModelCategory}) do *not* imply that the underlying [[model category]] (or any of its [[slice model categories]]) is a [[cartesian closed model category]] -- and in most examples this is not the case. Namely, the axioms here (eq:RightBaseChangeQuillenAdjunction) only require [[Quillen functors]] in one variable (the second variable for [[internal homs]], with the other variable a fixed [[fibrant object]]) where those of a [[cartesian closed model category]] require [[Quillen bifunctors]].
\end{remark}

## Definition

\begin{definition}\label{LocallyCartesianClosedModelCategory}
**(locally cartesian closed model category)** \linebreak
A **locally cartesian closed model category** is

* a [[model category]] $\mathcal{C}$,

* whose underlying category is a [[locally cartesian closed category]] 

* such that for every [[fibration]] between [[fibrant objects]]

  \[
    \label{FibrationBetweenFibrantObjects}
    \array{
      A &\underoverset{\;\;\;\;\;\in Fib\;\;\;\;\;}{g}{\longrightarrow}& B
      \\
      && \big\downarrow {}^{\mathrlap{\in Fib}}
      \\    
      && \ast
    }
  \]

  the [[dependent product]]/[[base change]] [[adjunction]]

  $$ 
    g^* 
    \;\colon\; 
    \mathcal{C}/B 
       \rightleftarrows 
    \mathcal{C}/A 
    \;\colon\; 
    \Pi_g 
  $$

  is a [[Quillen adjunction]] between the corresponding [[slice model structures]].

Concretely, this means that both [[cofibrations]] and [[trivial cofibrations]] are [[pullback-stability|stable]] under [[pullback]] along fibrations between [[fibrant objects]].

Equivalently this means that for all [[fibrations]] $A \to B$ the [[internal hom]] [[adjunction]] in the [[slice category]] over $B$

\[
  \label{RightBaseChangeQuillenAdjunction}
  (-) \times_{\mathcal{C}/_B} A 
  \;:\;
  \mathcal{C}/_B
  \rightleftarrows
  \mathcal{C}/_B
  \;:\;
  [A, -]_{\mathcal{C}/_B}
\]

is a [[Quillen adjunction]].
\end{definition}


## Examples
 {#Examples}

\begin{example}\label{RightProperModelCategoriesWithCofibsTheMonosAreLcc}
Any [[right proper model category]] whose underlying category is [[locally cartesian closed category|locally cartesian closed]] and in which the [[cofibrations]] are the [[monomorphisms]] is a locally cartesian closed model category.  
\end{example}
\begin{proof}
The [[fiber product]]/[[pullback]] functor $g^\ast$
  
  * is a left adjoint by local cartesian closure of the underlying category,

  * preserves cofibrations because these are the monomorphisms and hence are preserved by pullback (by [this prop.](monomorphism#MonomorphismsArePreservedByPullback)),

  * {#PullbackPreservesWeakEquivalences} preserves weak equivalences, and hence acyclic cofibrations by the previous item, due to right properness -- using here the assumption (eq:FibrationBetweenFibrantObjects) that $g$ is a fibration.

In summary this means that $g^\ast$ is a [[left Quillen functor]].
\end{proof}

\begin{example}
Example \ref{RightProperModelCategoriesWithCofibsTheMonosAreLcc} subsumes the following classes of examples, in increasing generality:

* the [[classical model structure on simplicial sets]], 

* any [[injective global model structure on simplicial presheaves]],

* any [[injective local model structure on simplicial presheaves]] whose weak equivalences are detected [[stalk]]-wise (by the discussion [there](model+structure+on+simplicial+presheaves#StalkwiseWeakEquivalencesImpliesRightProperness)),

* any right proper [[Cisinski model structure]].

\end{example}

## Versus locally cartesian closed $(\infty,1)$-categories
 {#VersusLCCInfinityCategories}

{#LCCInfinityCategoriesFromLCCModelCategories}
It is easy to see that the $(\infty,1)$-category [[simplicial localization|presented]] by a locally cartesian closed model category is itself [[locally cartesian closed (infinity,1)-category|locally cartesian closed]]: With the assumption (eq:FibrationBetweenFibrantObjects) that $g$ is a fibration between fibrant objects, it follows (by [this Prop](homotopy+pullback#HomotopyPullbackByOrdinaryPullback)) that pullback along $g$ models the correct [[homotopy pullback]].

{#LCCModelCategoriesFromLCCInfinityCategories}
Conversely, any [[locally presentable (infinity,1)-category|locally presentable]] locally cartesian closed $(\infty,1)$-category can be presented by some right proper Cisinski model category, which is therefore a locally cartesian closed model category; see [[locally cartesian closed (infinity,1)-category#Presentations|there]] for the proof.

### Versus homotopy type theories
 {#VersusHomotopyTypesTheories}

* Modulo questions of strictness and [[coherence]] (see at *[[initiality conjecture]]* for details), locally cartesian closed model categories provide [[categorical semantics]] for [[homotopy type theory]] with [[function extensionality]].

## Related concepts

* [[cartesian closed category]], [[locally cartesian closed category]]

* [[cartesian closed functor]], [[locally cartesian closed functor]]


* [[cartesian closed model category]], **locally cartesian closed model category**


* [[cartesian closed (∞,1)-category]] [[locally cartesian closed (∞,1)-category]]

[[!redirects locally cartesian closed model categories]]

