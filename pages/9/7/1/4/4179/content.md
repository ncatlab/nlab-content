In the setting of [[partial function]]s and operations, saying that an equality between [[term|terms]] such as 
$$ s = t $$
is a **Kleene equality** means that it asserts that if either side of the equality is defined, then so is the other, and they are equal.  Sometimes another symbol is used for Kleene equality, such as
$$ s \simeq t .$$


## Elementary examples

For example, in elementary algebra (or more generally, the first-order theory of a [[field]]),
\[ \label{correct} \frac x {x^2} = \frac 1 x \]
is always true as  Kleene equality, even when $x = 0$, because then *both* sides are undefined.  In contrast,
\[ \label{wrong} \frac {x^2} x = x \]
is not always true, even though the two sides are equal whenever both are defined, because the right-hand side is defined when $x = 0$ but the left-hand side is not.

The example (eq:wrong) can be fixed in either of two ways.  First, we can make its statement contingent on some condition under which the equality holds, as follows:
\[ \label{weak} \frac {x^2} x = x, \text{ if } x \ne 0 .\]
This states that (eq:wrong) holds whenever $x \ne 0$, which is correct.  Alternatively, we can add a clause to the term on the right-hand side that forces it to be undefined when $x = 0$, as follows:
\[ \label{strong} \frac {x^2} x = (x, x \ne 0) .\]
The idea here is that $x, x \ne 0$ is a term (like a [[piecewise-defined function|piecewise-defined]] expression with only one piece) that is defined only when $x \ne 0$.  Note that (eq:strong) is a *stronger* statement than (eq:weak); while (eq:weak) states only that (eq:wrong) holds when $x \ne 0$, (eq:strong) states additionally that the left-hand side of (eq:wrong) is defined only when $x \ne 0$.

The version usually seen in elementary algebra textbooks,
\[ \label{ambiguous} \frac {x^2} x = x,\; x \ne 0 ,\]
is ambiguous and could mean either (eq:weak) or (eq:strong).  In any case, there is *no* need to add anything to (eq:correct); some textbooks do and some don\'t.