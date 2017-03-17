
+-- {: .num_prop #DerivedAdjunctionUnitOfLftBousfieldLoclization}
###### Proposition

Let 

$$
  \mathcal{C}_{loc}
    \underoverset
      {\underset{id}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\bot}
  \mathcal{C}
$$

be a [[Quillen adjunction]] which exhibits a left [[Bousfield localization of model categories]], and assume that $\mathcal{C}_{loc}$ admits [[functorial factorization]] (for instance if $\mathcal{C}$ is a [[combinatorial model category]], whence $\mathcal{C}_{loc}$ is, then via the [[small object argument]]), hence in particular a fibrant replacement [[natural transformation]]

$$
  (-) \longrightarrow (-)^{fib}
  \,.
$$

Then the derived adjunction unit, i.e. the [[adjunction unit]] $\eta^{der}$ of [[adjoint pair]] of the [[derived functors]] on the [[homotopy category of a model category|homotopy category]] (as discussed there)

$$
  Ho(\mathcal{C}_{loc})
    \underoverset
      {\underset{}{\hookrightarrow}}
      {\overset{}{\longleftarrow}}
      {\bot}
  Ho(\mathcal{C})
$$

is isomorphic to the image of the fibrant replacement morphism in $\mathcal{C}_{loc}$:

$$
  \eta^{der}_X
  \simeq
  \ell(X \to X^{fib})
  \,,
$$

where $\ell \;\colon\; \mathcal{C}_{loc} \to Ho(\mathcal{C}_{loc})\;$ is the [[localization]] functor (as discussed at _[[homotopy category of a model category]]_).

=--

+-- {: .proof}
###### Proof

First consider the general prescription (from _[[homotopy category of a model category]]_) of computing the right (left) [[derived functors]] by applying the Quillen functors to fibrant (cofibrant) replacements, where we apply the fibrant replacement functorially also to the non-cofibrantly replaced object:

Let

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

be a general [[Quillen adjunction]] betwen [[model categories]] which admit [[functorial factorization]].

Let $X \in \mathcal{D}$ be any [[object]]. First consider a cofibrant replacement

$$
  \array{
    X_{cof}
    \\
    \downarrow^{\mathrlap{\in \mathrm{W} \cap Fib}}
    \\
    X
  }
  \,.
$$

Then apply $L$ to this

$$
  \array{
    L(X_{cof})
    \\
    \downarrow^{}
    \\
    L(X)
  }
  \,.
$$

Then apply fibrant replacement functorially


$$
  \array{
    L(X_{cof})
     &\overset{\in W \cap Cof}{\longrightarrow}&
    (L(X_{cof}))^{fib}
    \\
    \downarrow^{}
      &&
    \downarrow
    \\
    L(X)
      &\underset{\in W \cap Cof}{\longrightarrow}&
    (L(X))^{fib}
  }
  \,.
$$

Then apply $R$

$$
  \array{
     R L (X_{cof})
       &\overset{}{\longrightarrow}&
     R (L X_{cof})^{fib}
     \\
     \downarrow^{\mathrlap{}}
       &&
     \downarrow
     \\
     R L X &\underset{}{\longrightarrow}& R((L X)^{fib})
  }
$$

Finally, precompose with the ordinary [[adjunction unit]].
The derived adjunction unit is now modeled by the top composite morphism in the following diagram:

$$
  \array{
     X_{cof}
      &\overset{\eta_{X_{cof}}}{\longrightarrow}&
     R L (X_{cof})
       &\overset{R (j \in W \cap Cof)}{\longrightarrow}&
     R (L X_{cof})^{fib}
     \\
     \downarrow
     &&
     \downarrow^{\mathrlap{\in W \cap Fib}}
       &&
     \downarrow
     \\
     X
      &\underset{\eta_X}{\longrightarrow}&
     R L X &\underset{}{\longrightarrow}& R((L X)^{fib})
  }
  \,.
$$

Now in the special case that $(L \dashv R)$ is a [[left Bousfield localization of model categories]], then as plain [[categories]] $\mathcal{D} = \mathcal{C} $ and as plain functors $L = id$ and $R = id$ are trivial and so in this special case the derived adjunction unit is modeled simply by the top morphism in the following diagram

$$
  \array{
    X_{cof} 
      &\overset{\in Cof}{\longrightarrow}&
    (X_{cof})^{fib}
     \\
    {}^{\mathllap{\in W \cap Fib}}\downarrow
      &&
    \downarrow^{\mathrlap{\in W \cap Fib}}
    \\
    X 
      &\underset{\in W Cof}{\longrightarrow}&
    X^{fib}
  }
  \,.
$$

But now since the vertical morphisms are weak equivalences,
this means that already the fibrant replacement $X \to X^{fib}$
is isomorphic, in the homotopy category, to the derived unit, i.e. applying the [[localization]] $\ell$ to the above diagram in $\mathcal{C}$ yields the diagram

$$
  \array{
    \mathcal{l}(X_{cof})
      &\overset{\eta^{der}_X}{\longrightarrow}&
    \mathcal{l}((X_{cof})^{fib})
     \\
    {}^{\simeq}\downarrow
    &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathcal{l}(X) 
      &\underset{}{\longrightarrow}&
    \mathcal{l}(X^{fib})
  }
  \,.
$$

=--
