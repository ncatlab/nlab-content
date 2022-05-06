
Suppose that $ u $ is a function of $ x $.  Then
$$ \mathrm { d } u = \frac { \partial u } { \partial x } \, \mathrm { d } x ,$$
so
$$ \frac { \partial u } { \partial x } = \frac { \mathrm { d } u } { \mathrm { d } x } .$$
Thus,
$$ \frac { \partial ^ 2 u } { \partial x ^ 2 } = \frac { \partial \left ( \frac { \partial u } { \partial x } \right ) } { \partial x } = \frac { \mathrm { d } \left ( \frac { \mathrm { d } u } { \mathrm { d } x } \right ) } { \mathrm { d } x } = \frac { \mathrm { d } x \, \mathrm { d } ^ 2 u - \mathrm { d } u \, \mathrm { d } ^ 2 x } { \mathrm { d } x ^ 3 } .$$

On the other hand,
$$ \mathrm { d } ^ 2 u = \frac { \partial ^ 2 u } { \partial x ^ 2 } \, \mathrm { d } x + \frac { \partial u } { \partial x } \, \mathrm { d } ^ 2 x ,$$
so
$$ \mathrm { d } ^ 2 u \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } ^ 2 x = \frac { \partial ^ 2 u } { \partial x ^ 2 } \, \mathrm { d } x \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } ^ 2 x ,$$
so
$$ \frac { \partial ^ 2 u } { \partial x ^ 2 } = \frac { \mathrm { d } ^ 2 u \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } ^ 2 x } { \mathrm { d } x \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } ^ 2 x } .$$

Now suppose that $ u $ is a function of $ x $ and $ y $.  Then
$$ \mathrm { d } u = \left ( \frac { \partial u } { \partial x } \right ) _ y \, \mathrm { d } x + \left ( \frac { \partial u } { \partial y } \right ) _ x \, \mathrm { d } y ,$$
so
$$ \mathrm { d } u \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } y = \left ( \frac { \partial u } { \partial x } \right ) _ y \, \mathrm { d } x \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } y ,$$
so
$$ \left ( \frac { \partial u } { \partial x } \right ) _ y = \frac { \mathrm { d } u \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } y } { \mathrm { d } x \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } y } .$$
Thus,
$$ \left ( \frac { \partial ^ 2 u } { \partial x ^ 2 } \right ) _ y = \left ( \frac { \partial \left ( \frac { \partial u } { \partial x } \right ) _ y } { \partial x } \right ) _ y = \frac { \mathrm { d } \left ( \frac { \mathrm { d } u \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } y } { \mathrm { d } x \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } y } \right ) \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } y } { \mathrm { d } x \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } y } $$.

On the other hand,
$$ \mathrm { d } ^ 2 u = \left ( \frac { \partial ^ 2 u } { \partial x ^ 2 } \right ) _ y \, \mathrm { d } x ^ 2 + 2 \frac { \partial ^ 2 u } { \partial x \partial y } \, \mathrm { d } x \, \mathrm { d } y + \left ( \frac { \partial ^ 2 u } { \partial y ^ 2 } \right ) _ x \, \mathrm { d } y ^ 2 + \left ( \frac { \partial u } { \partial x } \right ) _ y \, \mathrm { d } ^ 2 x + \left ( \frac { \partial u } { \partial y } \right ) _ x \, \mathrm { d } ^ 2 y ,$$
so
$$ \mathrm { d } ^ 2 u \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } x \mathrm { d } y \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } y ^ 2 \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } ^ 2 x \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } ^ 2 y = \left ( \frac { \partial ^ 2 u } { \partial x ^ 2 } \right ) _ y \, \mathrm { d } x ^ 2 \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } x \mathrm { d } y \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } y ^ 2 \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } ^ 2 x \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } ^ 2 y ,$$
so
$$ \left ( \frac { \partial ^ 2 u } { \partial x ^ 2 } \right ) _ y = = \frac { \mathrm { d } ^ 2 u \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } x \mathrm { d } y \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } y ^ 2 \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } ^ 2 x \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } ^ 2 y } { \mathrm { d } x ^ 2 \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } x \mathrm { d } y \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } y ^ 2 \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } ^ 2 x \multiscripts { _ 1 } \wedge { _ 1 } \mathrm { d } ^ 2 y } .$$
