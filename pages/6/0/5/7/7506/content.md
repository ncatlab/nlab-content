
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# $\beta$-reduction
* table of contents
{: toc}

## Idea

In [[type theory]], $\beta$-reduction is a process of "computation", which generally replaces more complicated terms with simpler ones.  It was originally identified in the [[lambda-calculus]], where it contrasts with $\alpha$-[[alpha-equivalence|equivalence]] and $\eta$-[[eta expansion|expansion]]; this is the version described below for [[function types]].  The analogous reduction for [[inductive types]] may also be known as $\iota$-reduction.


## "Definition"

In its most general form, $\beta$-reduction consists of rules which specify, for any given [[type]] $T$, if we apply an "eliminator" for $T$ to the result of a "constructor" for $T$, how to "evaluate" the result.  We write

$$s \to_\beta t$$

if the term $s$ beta-reduces to the term $t$.  Sometimes we write $s \to_\beta^* t$ if this reduction takes $n$ steps (leaving off the $*$ to denote $n=1$).  The relation "reduces to" generates an [[equivalence relation]] on the set of terms called **beta equivalence** and often denoted $s =_\beta t$ or $s \equiv_\beta t$.


### Function types

The most common (and original) example is when $T$ is a [[function type]] $A \to B$.

In this case, the constructor of $A \to B$ is a *$\lambda$-expression*: given a term $b$ of type $B$ containing a free variable $x$ of type $A$, then $\lambda x.\, b$ is a term of type $A \to B$.

The eliminator of $A \to B$ says that given a term $f$ of type $A \to B$ and a term $a$ of type $A$, we can [[function application|apply]] $f$ to $a$ to obtain a term $f(a)$ of type $B$.

Now if we first construct a term $\lambda x.\, b\colon A \to B$, and then apply *this term* to $a\colon A$, we obtain a term $(\lambda x.\, b)(a)\colon B$.  The rule of $\beta$-reduction then tells us that this term *evaluates* or *computes* or *reduces* to $b[a/x]$, the result of [[substitution|substituting]] the term $a$ for the variable $x$ in the term $b$.

See [[lambda calculus]] for more.


### Product types

Although function types are the most publicized notion of $\beta$-reduction, basically all types in type theory have a form of it.  For instance, in the negative presentation of a [[product type]] $A \times B$, the constructor is an ordered pair $(a,b)\colon A \times B$, while the eliminators are projections $\pi_1$ and $\pi_2$ which yield elements of $A$ or $B$.

The beta reduction rules then say that if we first apply a constructor $(a,b)$, then apply an eliminator to this, the resulting terms $\pi_1(a,b)$ and $\pi_2(a,b)$ compute to $a$ and $b$ respectively.


## Related concepts

* [[lambda-calculus]]

* [[eta-reduction]]

* [[confluent category]] / [[diamond]] / [[Church-Rosser theorem]]


[[!redirects beta reduction]]
[[!redirects beta-reduction]]
[[!redirects ∞-reduction]]

[[!redirects beta conversion]]
[[!redirects beta-conversion]]
[[!redirects ∞-conversion]]

[[!redirects beta rule]]
[[!redirects beta-rule]]
[[!redirects ∞-rule]]

[[!redirects beta equivalent]]
[[!redirects beta-equivalent]]
[[!redirects ∞-equivalent]]
[[!redirects beta equivalence]]
[[!redirects beta-equivalence]]
[[!redirects ∞-equivalence]]

[[!redirects iota reduction]]
[[!redirects iota-reduction]]
[[!redirects ∞-reduction]]

[[!redirects iota equivalent]]
[[!redirects iota-equivalent]]
[[!redirects ∞-equivalent]]
[[!redirects iota equivalence]]
[[!redirects iota-equivalence]]
[[!redirects ∞-equivalence]]
