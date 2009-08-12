A [[morphism]] $f : A \to B$ of [[simplicial set]]s is called **anodyne** if it has the left [[lifting property]] with respect to all [[Kan fibration]]s.

So $f$ is anodyne if for every [[Kan fibration]] $X \to Y$ and every commuting diagram

$$
  \array{
    A &\to& X
    \\
    \downarrow^f && \downarrow
    \\
    B &\to& Y
  }
$$

there exists a lift

$$
  \array{
    A &\to& X
    \\
    \downarrow^f &\nearrow& \downarrow
    \\
    B &\to& Y
  }
  \,.
$$


Similarly a morphism is called

* **left anodyne** if it has the left [[lifting property]] with respect to all [[left Kan fibration]]s

* **right anodyne** if it has the left [[lifting property]] with respect to all [[right Kan fibration]]s

* **inner anodyne** if it has the left [[lifting property]] with respect to all [[inner Kan fibration]]s
