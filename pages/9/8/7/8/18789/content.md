
# Contents
* table of contents
{: toc}

## Idea

The _sign function_ on the [[real numbers]].


## Definition

$$
  \array{
    \mathbb{R} &\overset{sgn}{\longrightarrow}& \mathbb{R}
    \\
    x &\mapsto& \left\{ \array{ 1 &\vert& x \gt 0 \\ 0 &\vert& x = 0 \\ -1 &\vert& x \lt 0 }\right.
  }
$$

Some definitions will modify the value at $0$, usually to make it $1$, $-1$, or undefined.  In many applications, the sign function is essentially treated as a [[measurable function]] on the real line with [[Lebesgue measure]], and then these are all essentially the same since they are all [[almost equal]].    But some applications require the function to be [[left-continuous function|left-]] or [[right-continuous function|right-continuous]], and then the value of $0$ must be chosen appropriately, while the handy formula $x/{|x|}$ naturally makes the value at $0$ undefined.


# Related concepts

* [[positive real number]]

* [[negative real number]]

* [[real absolute value]]

* [[step function]]


## References

See also 

* Wikipedia, _[Sign function](https://en.wikipedia.org/wiki/Sign_function)_


[[!redirects sign]]
[[!redirects sign function]]
[[!redirects sgn]]
