
Let $\mathcal{C}$ be a [[model category]]. Then every [[commuting square]] in its [[homotopy category]] $Ho(C)$ is, up to [[isomorphism]], in the image of the [[localization]] functor $\mathcal{C} \longrightarrow Ho(\mathcal{C})$ of a commuting square in $\mathcal{C}$ (i.e.: not just commuting up to homotopy).

Let

$$
  \array{
    A &\overset{f}{\longrightarrow}& B
    \\
    {}^{\mathllap{a}}\downarrow
      &&
    \downarrow^{\mathrlap{b}}
    \\
    A' &\underset{f'}{\longrightarrow}& B'
  }
  \;\;\;\;\;
  \in Ho(\mathcal{C})
$$

be a commuting square in the homotopy category. Writing the same symbols for fibrant-cofibrant objects in $\mathcal{C}$ and for morphisms in $\mathcal{C}$ representing these, then this means that in $\mathcal{C}$ there is a [[left homotopy]] of the form

$$
  \array{
    A &\overset{f}{\longrightarrow}& B
    \\
    {}^{\mathllap{i_1}}\downarrow && \downarrow^{\mathrlap{b}}
    \\
    Cyl(A) &\underset{\eta}{\longrightarrow}& B'
    \\
    {}^{\mathllap{i_0}}\uparrow && \uparrow^{\mathrlap{f'}}
    \\
    A &\underset{a}{\longrightarrow}& A'
  }
  \,.
$$

Consider the factorization of the top square here through the [[mapping cylinder]] of $f$

$$
  \array{
    A &\overset{f}{\longrightarrow}& B
    \\
    {}^{\mathllap{i_1}}\downarrow &(po)& \downarrow^{\mathrlap{\in W}}
    \\
    Cyl(A) &\underset{}{\longrightarrow}& Cyl(f)
    \\
    {}^{\mathllap{i_0}}\uparrow &{}_{\mathllap{\eta}}\searrow& \downarrow^{\mathrlap{}}
    \\
    A && B'
    \\
    & {}_{\mathllap{a}}\searrow & \uparrow_{\mathrlap{f'}}
    \\
    && A'
  }
$$

This exhibits the composite $A \overset{i_0}{\to} Cyl(A) \to Cyl(f)$ as an alternative representative of $f$ in $Ho(\mathcal{C})$, and $Cyl(f) \to B'$ as an alternative representative for $b$, and the commuting square 

$$
  \array{
    A &\overset{}{\longrightarrow}& Cyl(f)
    \\
    {}^{\mathllap{a}}\downarrow
      &&
    \downarrow
    \\
    A' &\underset{f'}{\longrightarrow}& B'
  }
$$

as an alternative representative of the given commuting square in $Ho(\mathcal{C})$.

