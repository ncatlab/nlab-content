
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Diagram chasing lemmas
+-- {: .hide}
[[!include diagram chasing lemmas - contents]]
=--
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The **five lemma** is one of the basic lemmas of [[homological algebra]], useful for example in the construction of the [[connecting homomorphism]] in the  [[homology long exact sequence]]. 

## Statement

Let $\mathcal{A}$ be an [[abelian category]].
Consider a [[commutative diagram]] in $\mathcal{A}$  of the form 

$$\array{
A_1 & \to & A_2 & \to & A_3 & \to & A_4 &\to & A_5\\
\downarrow f_1 &&\downarrow f_2 &&\downarrow f_3 &&\downarrow f_4 &&\downarrow f_5 \\
B_1 & \to & B_2 & \to & B_3 & \to & B_4 &\to & B_5
}$$

where the top and bottom rows are [[exact sequences]]. For simplicity we denote all the differentials in both exact sequences by $d$.

+-- {: .num_prop #FiveLemma}
###### Proposition (the lemma on five homomorphisms or the **five lemma**)

1. sharp five lemma (essentially the weak **[[four lemma]]**)

   1. If $f_2$ and $f_4$ are [[epimorphism|epi]] and $f_5$ is [[monomorphism|mono]], then $f_3$ is epi. 

   1. If $f_2$ and $f_4$ are [[monomorphism|mono]] and $f_1$ is [[epimorphism|epi]], then $f_3$ is mono. 

1. (weak) five lemma (conjunction of the two statements above)

   If $f_2$ and $f_4$ are [[isomorphism|isos]], $f_1$ is epi, and $f_5$ is mono, then $f_3$ is iso.

=--

+-- {: .num_remark}
###### Remark
**on terminology**

The _weak four lemma_ is another terminology (cf. MacLane, _Homology_) for the same as 1.1 and 1.2 except that in 1.1 $f_1$ is not required to exist, and in 1.2 $f_5$ is not required to exist
(see [[four lemma]]), where the dropped requirements are inessential as not used in the proof. 

=--

+-- {: .proof}
###### Proof

The [[four lemma]] follows immediately from the [[salamander lemma]], as discussed at _[salamander lemma - impliciations - four lemma](salamander%20lemma#FourLemma)_. Here is a direct proof.

By the [[Freyd-Mitchell embedding theorem]]
we can always assume that the abelian category is $R$[[Mod]] (though this requires the category to be [[small category|small]], one can always take a smaller abelian subcategory containing the morphism in the diagram which is small). Then we can do the [[diagram chasing]] using elements in that setup. We prove only 1) as 2) is dual. 

Suppose $b\in B_3$. Since $f_4$ is epi, one can choose an element $a_4\in A_4$ such that $f_4(a_4) = d(b)$. Now $0 = d^2 b = d f_4 (a_4) = f_5 d (a_4)$. Since $f_5$ is a monomorphism that means that $d a_4 = 0$ as well. By the exactness of the upper row, that means there is $a_3\in A_3$ such that 
$d a_3 = a_4$, hence also $d f_3 (a_3) = f_4 d (a_3) = f_4(a_4) = d
b$. We would like that $f_3(a_3)$ be equal to $b$ but this is not so, we just see that $d (b-f_3(a_3)) = 0$ and hence by exactness  of the lower row there is $b'\in B_2$ such that $d b' = b-f_3(a_3)$. Since $f_2$ is also epi, there is $a_2\in A_2$ such that $f_2(a_2) = b'$. Now $d a_2+a_3\in A_3$ is such that 
$$f_3 (d a_2 + a_3) = d f_2(a_2) + f_3(a_3) = d b' + f_3(a_3) = b - f_3(a_3) + f_3(a_3) = b$$ 
demonstrating that $b$ is in the image of $f_3$.

Hence $f_3$ is an epimorphism.
=--

+-- {: .num_remark}
###### Remark 

The five lemma also holds in the category [[Grp]] of [[groups]], by essentially the same diagram-chasing proof. 

=-- 

+-- {: .num_remark}
###### Remark
One can avoid appealing to the [[Freyd-Mitchell embedding theorem]] if one works with [[element in an abelian category|generalized elements]] or uses the device of [[internal logic|interpreting]] [[regular logic]] in the given abelian category. The former requires a bit of manual reformulation, while the latter is almost automatic, as the element-based proof given above only uses (constructive) regular reasoning.
=--

## Immediate consequences

### Short five lemma

A special case of the five lemma is the _short five lemma_ where the objects $A_1,B_1,A_5,B_5$ above are all [[zero objects]]. It may hold in more general setups, sometimes with additional assumptions. 

+-- {: .num_cor #ShortFiveLemma}
###### Corollary 
**(short five lemma)**

Let $A \to B \to C$ and $A \to \tilde B \to C$ be two [[exact sequences]]. If a [[homomorphism]] $f \colon B \to \tilde B$ makes the [[diagram]]


$$
  \array{
     && B
     \\
     & \nearrow && \searrow
     \\
     A &&\downarrow^{\mathrlap{f}}&& C
     \\
     & \searrow && \nearrow
     \\
     && \tilde B
  }
$$

[[commuting diagram|commute]], then $f$ is an [[isomorphism]].

=--

+-- {: .proof}
###### Proof

Apply prop. \ref{FiveLemma} to the diagram

$$
  \array{
    0 &\to& A &\to& B &\to& C &\to& 0
    \\
    \downarrow^{\mathrlap{=}}
    &&
    \downarrow^{\mathrlap{=}}
    &&
    \downarrow^{\mathrlap{f}}
    &&
    \downarrow^{\mathrlap{=}}
    &&
    \downarrow^{\mathrlap{=}}
    \\
    0 &\to& A &\to& \tilde B &\to& C &\to& 0
  }
$$

=--



### Short split five lemma

The **short split five lemma** is a statement usually stated in the setup of [[semiabelian categories]]:

+-- {: .num_cor}
###### Corollary 
**(short split five lemma)**

Given a commutative diagram
$$\array{L & \overset{l}{\to} & H & \overset{q}{\to} & C\\
  ^u\downarrow && \downarrow^w && \downarrow^v \\
  K & \underset{k}{\to} & G& \underset{p}{\to} & B}$$
where $p$ and $q$ are [[split epimorphism]]s and $l$ and $k$ are their [[kernel]]s, if $u$ and $v$ are [[isomorphism]]s then so is $w$.
=--

+-- {: .num_remark}
###### Remark 
The short five lemma holds in the category of [[abelian group|abelian]] [[topological groups]], even though that category is not semi-abelian. For a proof, see this [paper](#BorClem) by Borceux and Clementino. 
=--

## Related concepts

* [[connecting homomorphism]]

* [[salamander lemma]]

* [[3x3 lemma]], [[snake lemma]]

* [[horseshoe lemma]]

## References

Early references of the 5-lemma 

* (lemma (5,9) in) D. A. Buchsbaum, _Exact categories and duality_, Transactions of the American Mathematical Society Vol. 80, No. 1 (1955), pp. 1-34 ([JSTOR](http://www.jstor.org/stable/1993003))
* (prop.1.1, page 5) Henri Cartan, Samuel Eilenberg, _Homological algebra_, Princeton Univ. Press 1956
* (lemma 3.3 in chapter I) S. MacLane, _Homology_, Springer 1963, 1975

Modern

* (exercise 1.3.3 in) [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_ 
* Nicolas Bourbaki, _Homological algebra_ (Algebra ch. X) 1980

In nonabelian context

* [[Francis Borceux]], [[Dominique Bourn]], _[[Borceux-Bourn|Mal'cev, protomodular, homological and semi-abelian categories]]_, Mathematics and Its Applications __566__, Kluwer 2004

The short 5-lemma also appears in various topological algebra contexts; see for example 

* Francis Borceux, Maria Manuel Clementino, _Topological semi-abelian categories_, Adv. Math. __190__ (2005), 425-453 ([web](https://estudogeral.sib.uc.pt/simple-search?query=clementino&x=0&y=0))
{#BorClem} 


[[!redirects five-lemma]]
[[!redirects five lemma]]
[[!redirects 5-lemma]]
[[!redirects 5 lemma]]

[[!redirects short five-lemma]]
[[!redirects short five lemma]]
[[!redirects short 5-lemma]]
[[!redirects short 5 lemma]]

[[!redirects split short five-lemma]]
[[!redirects split short five lemma]]
[[!redirects split short 5-lemma]]
[[!redirects split short 5 lemma]]

