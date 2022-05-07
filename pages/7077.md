
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

A _locally cartesian closed model category_ is a [[locally cartesian closed category]] which is equipped with the structure of a [[model category]] in a compatible way.

## Definition

A [[model category]] $\mathcal{C}$ which is additionally a [[locally cartesian closed category]] is called a **locally cartesian closed model category** if for any [[fibration]] $g\colon A\to B$ between [[fibrant objects]], the [[dependent product]]/[[base change]] [[adjunction]]
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

Concretely, this means that both [[cofibrations]] and [[trivial cofibrations]] are [[pullback-stability|stable]] under [[pullback]] along fibrations between fibrant objects.

Equivalently this means that for all $A \to B$ as above the [[internal hom]] [[adjunction]] in the [[slice category]] over $B$

$$
  (-) \times_{\mathcal{C}/_B} A 
  \;:\;
  \mathcal{C}/_B
  \rightleftarrows
  \mathcal{C}/_B
  \;:\;
  [A, -]_{\mathcal{C}/_B}
$$

is a [[Quillen adjunction]].


## Examples
 {#Examples}

\begin{example}\label{RightProperModelCategoriesWithCofibsTheMonosAreLcc}
Any [[right proper model category]] whose underlying category is [[locally cartesian closed category|locally cartesian closed]] and in which the [[cofibrations]] are the [[monomorphisms]] is a locally cartesian closed model category.  
\end{example}
\begin{proof}
The [[fiber product]]/[[pullback]] functor $g^\ast$
  
  * is a left adjoint by local cartesian closure of the underlying category,

  * preserves cofibrations because these are the monomorphisms and hence are preserved by pullback (by [this prop.](monomorphism#MonomorphismsArePreservedByPullback)),

  * preserves weak equivalences, and hence acyclic cofibrations by the provious item, due to right properness.

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

It is easy to see that the $(\infty,1)$-category presented by a locally cartesian closed model category is itself [[locally cartesian closed (infinity,1)-category|locally cartesian closed]].  Conversely, any [[locally presentable (infinity,1)-category|locally presentable]] locally cartesian closed $(\infty,1)$-category can be presented by some right proper Cisinski model category, which is therefore a locally cartesian closed model category; see [[locally cartesian closed (infinity,1)-category#Presentations|there]] for the proof.

## Applications

* Modulo questions of strictness and [[coherence]] (see [[identity type]] for details), locally cartesian closed model categories provide [[categorical semantics]] for [[homotopy type theory]] with [[function extensionality]].

## Related concepts

* [[cartesian closed category]], [[locally cartesian closed category]]

* [[cartesian closed functor]], [[locally cartesian closed functor]]


* [[cartesian closed model category]], **locally cartesian closed model category**


* [[cartesian closed (∞,1)-category]] [[locally cartesian closed (∞,1)-category]]

[[!redirects locally cartesian closed model categories]]

