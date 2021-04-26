
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The extra structure of a [[model category]] over a [[category with weak equivalences]] induces concrete constructions for expressing [[homotopy]] between [[morphisms]]. These lead in particular to an explicit construction of the [[homotopy category of a model category]].


## Definition

+-- {: .num_defn #PathAndCylinderObjectsInAModelCategory}
###### Definition

Let $\mathcal{C}$ be a [[model category]] and $X \in \mathcal{C}$ an [[object]].

* A **[[path object]]** $Path(X)$ for $X$ is a factorization of the [[diagonal]] $\nabla_X \colon X \to X \times X$ as

$$
  \nabla_X 
  \;\colon\;
   X \underoverset{\in W}{i}{\longrightarrow} Path(X) \overset{(p_0,p_1)}{\longrightarrow} X \times X
  \,.
$$

where $X\to Path(X)$ is a weak equivalence. This is called a **good path object** if in addition $Path(X) \to X \times X$ is a fibration.

* A **[[cylinder object]]** $Cyl(X)$ for $X$ is a factorization of the [[codiagonal]] (or "fold map") $\Delta_X X \sqcup X \to X$ as

$$
  \Delta_X
  \;\colon\;
  X \sqcup X \overset{(i_0,i_1)}{\longrightarrow} Cyl(X) \underoverset{p}{\in W}{\longrightarrow} X
  \,.
$$

where $Cyl(X) \to X$ is a weak equivalence. This is called a **good cylinder object** if in addition $X \sqcup X \to Cyl(X)$ is a cofibration.

=--

+-- {: .num_remark #RemarkOnChoicesOfNonGoodPathAndCylinderObjects}
###### Remark

By the factorization axioms every object in a model category has both a good path object and as well as a good cylinder object according to def. \ref{PathAndCylinderObjectsInAModelCategory}. But in some situations one is genuinely interested in using non-good such objects.  

For instance in the [[classical model structure on topological spaces]], the obvious object $X\times [0,1]$ is a cylinder object, but not a good cylinder unless $X$ itself is cofibrant (a [[cell complex]] in this case).

More generally, the path object $Path(X)$ of def. \ref{PathAndCylinderObjectsInAModelCategory} is analogous to the [[powering]] $\pitchfork(I,X)$ with an [[interval object]] and the cyclinder object $Cyl(X)$ is analogous to the [[tensoring]]  with a cylinder object $I\odot X$.  In fact, if $\mathcal{C}$ is a $V$-[[enriched model category]] and $X$ is fibrant/cofibrant, then these powers and copowers  are in fact examples of (good) path and cylinder objects if the [[interval object]] is sufficiently good. 

=--

+-- {: .num_defn #LeftAndRightHomotopyInAModelCategory}
###### Definition

Let $f,g \colon X \longrightarrow Y$ be two [[parallel morphisms]] in a [[model category]].

* A **left homotopy** $\eta \colon f \Rightarrow_L g$ is a morphism $\eta \colon Cyl(X) \longrightarrow Y$ from a [[cylinder object]] of $X$,  def. \ref{PathAndCylinderObjectsInAModelCategory}, such that it makes this [[commuting diagram|diagram commute]]: 

$$
  \array{
    X &\longrightarrow& Cyl(X) &\longleftarrow& X
    \\
    & {}_{\mathllap{f}}\searrow &\downarrow^{\mathrlap{\eta}}& \swarrow_{\mathrlap{g}}
    \\
    && 
    Y
  }
  \,.
$$

* A **right homotopy** $\eta \colon f \Rightarrow_R g$ is a morphism $\eta \colon X \to Path(Y)$ to some [[path object]] of $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}, such that this [[commuting diagram|diagram commutes]]:

$$
  \array{
    && X
    \\
    & {}^{\mathllap{f}}\swarrow & \downarrow^{\mathrlap{\eta}} & \searrow^{\mathrlap{g}} 
    \\
    Y &\longleftarrow& Path(Y) &\longrightarrow& Y
  }
  \,.
$$

=--



## Properties

### Basic lemmas

+-- {: .num_lemma #ComponentsOfGoodCylinderOfCofibrantAreAcyclicCofibrationsAndDually}
###### Lemma

If 
$
  X \sqcup X \overset{(i_0,i_1)}{\longrightarrow} Cyl(X) \underoverset{p}{\in W}{\longrightarrow} X
$
is a good [[cylinder object]] for a cofibrant object $X$ def. \ref{PathAndCylinderObjectsInAModelCategory}, then both components $i_0, i_1 \colon X \to Cyl(X)$ are acyclic cofibrations.

Dually, if 
$
   X \underoverset{\in W}{i}{\longrightarrow} Path(X) \overset{(p_0,p_1)}{\longrightarrow} X \times X
$

is a good path object for a fibrant object $X$, then both component $p_0,p_1 \colon Path(X)\to X$ are acyclic fibrations.

=--

+-- {: .proof}
###### Proof

We discuss the first case, the second is [[formal dual|formally dual]]. First observe that the two inclusions $X \to X \sqcup X$ are cofibrations, since they are the [[pushout]] of the cofibration $\emptyset \to X$. This implies that $i_0$ and $i_1$ are composites of two cofibrations

$$
  i_0, i_1 
   \;\colon\;
  X \overset{\in Cof}{\longrightarrow} X\sqcup X  
  \overset{\in Cof}{\longrightarrow}
$$

and hence are themselves cofibrations. That they are in addition weak equivalences follows from [[two-out-of-three]] applied to the identity

$$
  id_X \;\colon\;
  X \overset{\in W}{\longrightarrow}
  Cyl(X)
  \overset{i_0}{\longrightarrow}
  X
  \,.
$$

implied by the fact that the cylinder by definition factors the [[codiagonal]].

=--

The following says that the choice of cylinder/path objects in def. \ref{LeftAndRightHomotopyInAModelCategory} is irrelevant as long it is "good".

+-- {: .num_lemma #GoodCylinderObjectsSupportEveryLeftHomotopyAndDually}
###### Lemma

For $\eta \colon f \Rightarrow_L g \colon X \to Y$ a [[left homotopy]] in some [[model category]], def. \ref{LeftAndRightHomotopyInAModelCategory}, such that $Y$ is a fibrant object, then for $Cyl(X)$ any choice of _good_ [[cylinder object]] for $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}, there is a [[commuting diagram]] of the form

$$
  \array{
    X &\longrightarrow& Cyl(X) &\longleftarrow& X
    \\
    & {}_{\mathllap{f}}\searrow &\downarrow^{\mathrlap{\tilde \eta}}& \swarrow_{\mathrlap{g}}
    \\
    && 
    Y
  }
  \,.
$$

Dually, for $\eta \colon f \Rightarrow_R g \colon X \to Y$ a [[right homotopy]], def. \ref{LeftAndRightHomotopyInAModelCategory}, such that $X$ is cofibrant, then for $Path(X)$ any choice of _good_ [[path object]] for $X$, def. \ref{PathAndCylinderObjectsInAModelCategory}, there is a [[commuting diagram]] of the form


$$
  \array{
    && X
    \\
    & {}^{\mathllap{f}}\swarrow & \downarrow^{\mathrlap{\tilde \eta}} & \searrow^{\mathrlap{g}} 
    \\
    Y &\longleftarrow& Path(Y) &\longrightarrow& Y
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

We discuss the first statement, the second is [[formal dual|formally dual]].
Let $\eta \colon \hat X \longrightarrow Y$ be the given left homotopy with respect to a given cylinder object $\hat X$ of $X$. Factor it as 

$$
  \eta 
    \;\colon\; 
  \hat X \overset{\in Cof}{\longrightarrow} Z \overset{\in W \cap Fib}{\longrightarrow} 
  Y
  \,.
$$

Then find liftings $\ell$ and $k$ in the following two [[commuting diagrams]]

$$
  \array{
    X \sqcup X &\overset{}{\longrightarrow}& \hat X &\longrightarrow& Z
    \\
    \downarrow && & {}^{\mathllap{\ell}}\nearrow & \downarrow
    \\
    Cyl(X) &\longrightarrow& &\longrightarrow& Y 
  }
  \;\;\;\;\;
  \,,
  \;\;\;\;\;
  \array{
    \hat X &\overset{\eta}{\longrightarrow}& Y
    \\
    \downarrow &{}^{\mathllap{k}}\nearrow& \downarrow
    \\
    Z &\longrightarrow& \ast 
  }
  \,.
$$

Now the composite $\eta \coloneqq k \circ \ell$ is of the required kind, 

$$
  \array{
    X \sqcup X &\overset{}{\longrightarrow}& \hat X &\longrightarrow& Z &\overset{k}{\longrightarrow}& Y
    \\
    \downarrow &&&  {}^{\mathllap{\ell}}\nearrow &
    \\
    Cyl(X) &\longrightarrow& 
  }
  \,.
$$

=--

+-- {: .num_lemma #LeftHomotopyWithCofibrantDomainImpliesRightHomotopyAndDually}
###### Lemma

Let $f,g \colon X \to Y$ be two [[parallel morphisms]] in a [[model category]]. 

* Let $X$ be cofibrant. If there is a [[left homotopy]] $f \Rightarrow_L g$ then there is also a [[right homotopy]] $f \Rightarrow_R g$ (def. \ref{LeftAndRightHomotopyInAModelCategory}) with respect to any chosen good path object.

* Let $Y$ be fibrant. If there is a [[right homotopy]] $f \Rightarrow_R g$ then there is also a [[left homotopy]] $f \Rightarrow_L g$ with respect to any chosen good cylinder object. 

=--

+-- {: .proof}
###### Proof

We discuss the first case, the second is [[formal dual|formally dual]].
Let $\eta \colon Cyl(X) \longrightarrow Y$ be the given left homotopy. By lemma \ref{GoodCylinderObjectsSupportEveryLeftHomotopyAndDually} we may assume without restriction that $Cyl(X)$ is _good_ in the sense of def. \ref{PathAndCylinderObjectsInAModelCategory}, for otherwise replace it by one that is. With this, lemma \ref{ComponentsOfGoodCylinderOfCofibrantAreAcyclicCofibrationsAndDually} implies that we have a lift $h$ in the following [[commuting diagram]]

$$
  \array{
    X &\overset{i \circ f}{\longrightarrow}& Path(Y)
    \\
    {}^{\mathllap{i_0}}_{\mathllap{\in W \cap Cof}}\downarrow 
    &{}^{\mathllap{h}}\nearrow& 
    \downarrow^{\mathrlap{p_0,p_1}}_{\mathrlap{\in Fib}}
    \\
    Cyl(X)
    &\underset{(f \circ p,\eta)}{\longrightarrow}& Y \times Y
  }
  \,,
$$

where on the right we have the chosen path space object. Now the composite $\tilde \eta \coloneqq h \circ i_1$ is a right homotopy as required.

$$
  \array{
    && && Path(Y)
    \\
    && &{}^{\mathllap{h}}\nearrow& 
    \downarrow^{\mathrlap{p_0,p_1}}_{\mathrlap{\in Fib}}
    \\
    X &\overset{i_1}{\longrightarrow}& Cyl(X)
    &\underset{(f \circ p,\eta)}{\longrightarrow}&
    Y \times Y
  }
  \,.
$$

=--

### Equivalence relation

+-- {: .num_prop }
###### Proposition

For $X$ a cofibrant object in a [[model category]] and $Y$ a [[fibrant object]], then the [[relations]] of [[left homotopy]] $f \Rightarrow_L g$ and of [[right homotopy]] $f \Rightarrow_R g$ (def. \ref{LeftAndRightHomotopyInAModelCategory}) on the [[hom set]] $Hom(X,Y)$ coincide and are both [[equivalence relations]].

=--


+-- {: .proof}
###### Proof

That both relations coincide under the (co-)fibrancy assumption follows directly from lemma \ref{LeftHomotopyWithCofibrantDomainImpliesRightHomotopyAndDually}.

To see that left homotopy with domain $X$ is a [[transitive relation]] first use lemma \ref{GoodCylinderObjectsSupportEveryLeftHomotopyAndDually} to obtain that every left homotopy is exhibited by a _good_ cylinder object $Cyl(X)$ and then lemma \ref{ComponentsOfGoodCylinderOfCofibrantAreAcyclicCofibrationsAndDually} to see that the cofiber coproduct $Cyl(X)\underset{X}{\sqcup} Cyl(X)$ in 

$$
  \array{
     && && X
     \\
     && && \downarrow^{\mathrlap{i_0}}
     \\
     && X &\underoverset{\in W}{i_1}{\longrightarrow}& Cyl(X)
     \\
     && {}^{\mathllap{i_0}}\downarrow &(po)& \downarrow
     \\
     X &\underset{i_1}{\longrightarrow}& 
    Cyl(X) &\underset{\in W}{\longrightarrow}& Cyl(X) \underset{X}{\sqcup} Cyl(X)
     \\
     && &{}_{\mathllap{}}\searrow& & \searrow
     \\
     && && \underset{\in W}{\longrightarrow} &\longrightarrow& X
  }
$$

is again a [[cylinder object]], def. \ref{PathAndCylinderObjectsInAModelCategory}. The [[symmetric relation|symmetry]] and [[reflexive relation|reflexivity]] of the relation is obvious.

=--

## References

See the references at _[[model category]]_.