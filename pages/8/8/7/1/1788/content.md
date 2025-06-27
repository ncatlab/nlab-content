
The [[Pin(2)]]-group is

$$
  S(\mathbb{C}) \cup \mathbf{j} S(\mathbb{C})
  \,.
$$


Identify the plane with the [[linear span]] of $\mathbf{j}$ and $\mathbf{k}$

$$
  \mathbb{R}^2 
  \;\simeq\;
  \langle \mathbf{j}, \mathbf{k}\rangle
  \;\subset\;
  \mathbb{H}_{\mathrm{im}}
  \,.
$$

Then an element 

$$
  R_{\alpha}
  \;\coloneqq\; 
  Ad_{
    \cos(\alpha/2) 
    +
    \sin(\alpha/2)
    \mathbf{i} 
  }
  \;\in\;
  S(\mathbb{C}) \subset S(\mathbb{H})
$$

acts on $\mathbb{R}^2$ as

$$
  \begin{array}{rcl}
    R_\alpha(\mathbf{j})
    &\equiv&
    \big(
      \cos(\alpha/2) + \sin(\alpha/2)\mathbf{i}
    \big)
    \,
    \mathbf{j}
    \,
    \big(
      \cos(\alpha/2) - \sin(\alpha/2)\mathbf{i}
    \big)
    \\
    &=&
    \big(
      \cos(\alpha/2)^2 - \sin(\alpha/2)^2
    \big)
    \,
    \mathbf{j}
    +
    \big( 
      2 \sin(\alpha/2) \cos(\alpha/2)
    \big)
    \,
    \mathbf{k} 
    \\
    &=&
    \cos(\alpha) \, \mathbf{j}
    +
    \sin(\alpha) \, \mathbf{k}
  \end{array}
$$

(in the last line we used the [sum-of-angles](trigonometric+identity#eq:SumOfAnglesFormulas) [[trigonometric identities]])

while the element $I_y \coloneqq Ad_{\mathbf{j}}$ acts as

$$
  I_y \mathbf{j}
  \;=\;
  \mathbf{j} \, \mathbf{j} \, (- \mathbf{j})
  \;=\;
  \mathbf{j}
$$

$$
  I_y \mathbf{k}
  \;=\;
  \mathbf{j} \, \mathbf{k} \, (- \mathbf{j})
  \;=\;
  -
  \mathbf{k}
$$



