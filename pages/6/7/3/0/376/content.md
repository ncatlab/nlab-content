
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A **locally cartesian closed category** is a [[category]] $C$ whose [[slice categories]] $C/x$ are all [[cartesian closed category|cartesian closed]]. 

If a locally cartesian closed category $C$ has a [[terminal object]], then $C$ is itself cartesian closed and in fact [[finitely complete category|has all finite limit]]s; often this requirement is included in the definition.

Equivalently, a locally cartesian category $C$ is a category with [[pullbacks]] (and a [[terminal object]], if required) such that each [[base change]] functor $f^*: C/y \to C/x$ has a [[right adjoint]] $\Pi_f$, called the _[[dependent product]]_. (This equivalence is discussed in detail [below](EquivalentCharacterizations).)

In particular, such pullbacks preserve all [[colimits]]. Therefore, if a locally cartesian closed category [[finitely cocomplete category|has finite colimits]], it is automatically a [[coherent category]] and in fact a [[Heyting category]].


## Properties

### Equivalent characterizations
 {#EquivalentCharacterizations}

We show how the [[dependent product]] and the [[internal hom]] in the [[slice categories]] may be used to express each other.

+-- {: .num_prop #DependentProductImpliesLocalCartesinClosure}
###### Proposition

Let $\mathcal{C}$ be a [[category]] with [[pullbacks]] that has all [[dependent products]] $\prod_\bullet$,  equivalently that every morphism $f : E \to X$ in $\mathcal{C}$ induces an [[adjoint triple]]

$$
  \mathcal{C}_{/E}
    \stackrel{\overset{\sum_f}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{\prod_f}{\to}}}
  \mathcal{C}_{/X}
  \,.
$$

Then the [[internal hom]] in a slice $\mathcal{C}_{/X}$ exists and is given by 

$$
  [\langle E \stackrel{f}{\to} X\rangle \; ,\;  -]_{\mathcal{C}_{/X}}
  \simeq
  \prod_f \circ f^* 
  \,.
$$


=--

+-- {: .proof}
###### Proof

By the discusson at _[[overcategory]]-[Limits and colimits](overcategory#LimitsAndColimits)_ the product in the slice $\mathcal{C}_{/X}$ of two objects $\langle E_1 \stackrel{f_1}{\to} X\rangle$ and $\langle E_1 \stackrel{f_2}{\to} X\rangle$ is given by the [[pullback]] $f_1^* E_2 = f_2^* E_1$ in $\mathcal{C}$, regarded again as a morphism over $X$. More formally this means that the product with $\langle E \stackrel{f}{\to} X\rangle $ is given by the composite

$$ 
  (-) \times_{\mathcal{C}_{/X}} \langle E \stackrel{f}{\to} X\rangle
  \;\;\;:\;\;\; 
  \mathcal{C}_{/X}
    \stackrel{f^*}{\to}
  \mathcal{C}_{/E}
    \stackrel{\sum_f}{\to}
  \mathcal{C}_{/X}
$$

of the pullback long $f$ with the [[dependent sum]] along $f$. By the above [[adjoint triple]] both these morphisms have [[right adjoints]] and so the composite of the right adjoints is the right adjoint of the composite, hence is the [[internal hom]]:

$$
  \mathcal{C}_{/X}
    \stackrel{\prod_f}{\leftarrow}
  \mathcal{C}_{/E} 
    \stackrel{f^* }{\leftarrow} \mathcal{C}_{/X}
  \;\;\;:\;\;\;
  [\langle E\stackrel{f}{\to} X \rangle, -]_{\mathcal{C}_{/X}}
  \,.
$$


=--

+-- {: .num_prop}
###### Proposition

If for a [[category]] $\mathcal{C}$ every [[slice category]] is a [[cartesian closed category]], then for every morphism $f : X \to Y$ in $\mathcal{C}$ the [[dependent product]] $\prod_f$ exists and is given on an object $E \stackrel{p}{\to} X$ by the [[pullback]]

$$
  \array{
    \prod_f \langle E \stackrel{p}{\to} X\rangle &\to& [\langle X \stackrel{f}{\to}Y\rangle, \langle E \stackrel{p}{\to}X \stackrel{f}{\to} Y\rangle]_{\mathcal{C}_{/Y}}
    \\
    \downarrow && \downarrow
    \\
    Y &\stackrel{\bar id}{\to}& [\langle X \stackrel{f}{\to}Y \rangle,\langle X \stackrel{f}{\to}Y \rangle]_{\mathcal{C}_{/Y}}
  }
$$

in $\mathcal{C}_{/Y}$, where the bottom morphism is the [[adjunct]] of

$$
  Y \times_{\mathcal{C}_{/Y}} \langle X \stackrel{f}{\to} Y\rangle \simeq \langle X \stackrel{f}{\to}Y\rangle \stackrel{id}{\to} \langle X \stackrel{f}{\to}Y\rangle
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is sufficient to check the $(f^* \dashv \prod_f)$-[[adjunction]] [[hom set]]-[[natural isomorphism]]

$$
  \mathcal{C}_{/Y}( \langle F \stackrel{}{\to} Y\rangle , \prod_f \langle E \stackrel{p}{\to} X\rangle)
  \simeq
  \mathcal{C}_{/X}(f^* \langle F \stackrel{}{\to} Y\rangle, \langle E \stackrel{p}{\to} X\rangle)
  \,,
$$

natural in $\langle F \stackrel{}{\to}Y \rangle$.

Since the [[hom functor]] $\mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle, -)$ preserves [[limits]] and hence [[pullbacks]], the expression on the left is exhibited as the pullback

$$
  \array{
    \mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle, \prod_f \langle E \stackrel{p}{\to} X\rangle &\to& 
  \mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle, [\langle X \stackrel{f}{\to}Y \rangle,\langle E \stackrel{p}{\to}X \stackrel{f}{\to} Y\rangle]_{\mathcal{C}_{/Y}})
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{}{\to}& \mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle,[\langle X \stackrel{f}{\to}Y \rangle,\langle X \stackrel{f}{\to}Y \rangle]_{\mathcal{C}_{/Y}})
  }
  \,.
$$

Using the $((-) \times_{\mathcal{C}_{/Y}} \langle X \stackrel{f}{\to}Y\rangle \dashv [\langle X \stackrel{f}{\to}Y\rangle, -]_{\mathcal{C}_{/Y}})$-adjunction  this is equivalently

$$
  \array{
    \mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle, \prod_f \langle E \stackrel{p}{\to} X\rangle 
    &\to& 
  \mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle \times_{\mathcal{C}_{/Y}} \langle X \stackrel{f}{\to}Y \rangle, \langle E \stackrel{p}{\to}X \stackrel{f}{\to} Y\rangle)
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{}{\to}& 
    \mathcal{C}_{/Y}(\langle F \stackrel{}{\to} Y\rangle \times_{\mathcal{C}_{/Y} }\langle X \stackrel{f}{\to}Y \rangle ,
   \langle X \stackrel{f}{\to}Y \rangle)
  }
  \,.
$$

This pullback now manifestly computes 
$\mathcal{C}_{/X}(f^* \langle F \to Y\rangle, \langle E \stackrel{p}{\to} X\rangle)$.

=--


### Internal logic

The [[internal logic]] of locally cartesian closed categories is an [[extensional type theory|extensional]] form of [[dependent type theory]].  In particular, the [[dependent product]] $\Pi_f$ represents an extensional [[dependent product type]] in the internal logic.

### Almost local cartesian closure

There are categories which are cartesian closed and not locally cartesian closed, but in which for some $f$ the  base change functor $f^*: C/y \to C/x$ has a right adjoint. This includes $Cat$, $Gpd$, and the category of [[crossed complex]]es; in the latter two cases, it is necessary and sufficient for $f$ to be a [[fibration]], while in $Cat$ it is sufficient for $f$ to be a fibration or an opfibration.

## Examples

+-- {: .num_prop}
###### Proposition

Every [[sheaf topos]] is locally cartesian closed.

=--

+-- {: .proof}
###### Proof

By [[Giraud's theorem]], in a sheaf topos [[pullbacks]] preserve [[colimits]].
With the [[adjoint functor theorem]] this implies that for every morphism $f : X \to Y$, the pullback functor $f^* : \mathcal{C}_{/Y} \to \mathcal{C}_{/X}$ has a [[right adjoint]] $\prod_f$. By prop. \ref{DependentProductImpliesLocalCartesinClosure} this yields the local cartesian closure.
 
=--

## Related concepts

* [[cartesian closed category]], **locally cartesian closed category**

* [[cartesian closed functor]], [[locally cartesian closed functor]]

* [[cartesian closed model category]], [[locally cartesian closed model category]]

* [[cartesian closed (∞,1)-category]] [[locally cartesian closed (∞,1)-category]]


## References

A standard textbook account is around corollary A1.5.3 in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

A discussion of [[dependent type theory]] as the [[internal language]] of locally cartesian closed categories is in 

* R. A. G. Seely, _Locally cartesian closed categories and type theory_, Math. Proc. Camb. Phil. Soc. (1984) 95 ([pdf](http://www.math.mcgill.ca/rags/LCCC/LCCC.pdf))

Related literature includes

* [[Marta Bunge]],  and Susan Niefield,   _Exponentiability and single universes_ J. Pure Appl. Algebra 148 (2000) 217--250.

* [[François Conduché]],   _Au sujet de l'existence d'adjoints &#224; droite aux foncteurs "image r&#233;ciproque" dans la cat&#233;gorie des cat&#233;gories_ (French)  C. R. Acad. Sci. Paris S&#233;r. A-B  275  (1972), A891--A894.

* J. Howie, _Pullback functors and crossed complexes_ , Cahiers Topologie G&#233;om. Diff&#233;rentielle, 20 (1979) 281--296.



[[!redirects locally cartesian closed categories]]
[[!redirects LCCC]]

[[!redirects locally Cartesian closed category]]
[[!redirects locally Cartesian closed categories]]
