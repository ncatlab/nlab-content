+-- {: .num_prop #Symplectomorphism}
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

be a [[Quillen adjunction]] which exhibits a Bousfield localization of model categories, and assume that $\mathcal{C}_{loc}$ admits [[functorial factorization]] (for instance if $\mathcal{C}$ is a [[combinatorial model category]], then via the [[small object argument]]), hence in particular a fibrant replacement [[natural transformation]]

$$
  (-) \longrightarrow (-)^{fib}
  \,.
$$

Then the derived adjunction unit, i.e. the [[adjunction unit]] $\eta^{der}$ of [[adjoint pair]] of the [[derived functors]] on the [[homotopy category]]

$$
  Ho(\mathcal{C}_{loc})
    \underoverset
      {\underset{}{\hookrigtharrow}}
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

where $\ell \;\mathcal{C}_{loc} \to Ho(\mathcal{C}_{loc})\;$ is the [[localization]]


=--

Let

$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

be a [[Quillen adjunction]] betwen [[model categories]] which admit [[functorial factorization]].

We consider the derived [[adjunction unit]].


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
       &\overset{R (j \in W \cap Cof)}{\longrightarrow}&
     R (L X_{cof})^{fib}
     \\
     \downarrow^{\mathrlap{\in W \cap Fib}}
       &&
     \downarrow
     \\
     R L X &\underset{}{\longrightarrow}& R((L X)^{fib})
  }
$$

The derived unit is now modeled by the top composite morphism in 

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
$$
.
Now in the special case that $(L \dashv R)$ is a left Bousfield localization of model categories, then as functors $L = id$ and $R = id$ and so in this case the derived adjunction unit is modeled simply by the top morphism in

$$
  \array{
    X_{cof} 
      &\overset{\in W \cap Cof}{\longrihtarrow}&
    (X_{cof})^{fib}
     \\
    {}^{\mathllap{\in W \cap Fib}}\downarrow
    \\
    X 
      \underset{\in W \cap Cof}{\longrightarrow}
    \\
    X^{fib}
  }
$$

But now since the vertical morphisms are weak equivalences,
this means that already the fibrant replacement $X \to X^{fib}$
is isomorphic, in the homotopy category, to the derived unit.
