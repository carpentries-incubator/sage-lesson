---
title: Polynomials and linear algebra
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---
Next we demonstrate indeterminates and polynomials.
This is an indeteminate `x`. It is defined automatically when SageMath starts (however, it is not read-only and may be easily overwritten):


~~~
x
~~~
{: .source .python}



~~~
x
~~~
{: .output}


One can construct polynomials and find their roots as follows:


~~~
f=x^2-x-1
~~~
{: .source .python}


~~~
f
~~~
{: .source .python}



~~~
x^2 - x - 1
~~~
{: .output}




~~~
solve([f==0],x)
~~~
{: .source .python}



~~~
[x == -1/2*sqrt(5) + 1/2, x == 1/2*sqrt(5) + 1/2]
~~~
{: .output}


Convert this these to a floating point variable:


~~~
float(1/2*sqrt(5) + 1/2)
~~~
{: .source .python}



~~~
1.618033988749895
~~~
{: .output}


Other symbolic variables are not defined. For example, if we try to define `v` to be the vector with symbolic coordinates `x`, `y`, `z`, we will have an error, because only `x` is defined by default when you launch Sage!


~~~
v = vector([x, y, z])
~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-6-41c893d7dada> in <module>()
----> 1 v = vector([x, y, z])

NameError: name 'y' is not defined
~~~
{: .error}
To fix this, we need to define `y` (and `z`) as symbolic variables, using `SR.var` (where "SR" stands for "symbolic ring"):


~~~
x, y, z = SR.var("x y z")
~~~
{: .source .python}


~~~
v = vector([x, y, z])
v
~~~
{: .source .python}



~~~
(x, y, z)
~~~
{: .output}


Such vectors can be operated with in the same way like vectors with numeric coordinates. To demonstrate this, we want to create an additive inverse of a 3x3 indentity matrix over integers. One could certainly enter it with `matrix([[-1,0,0], [0,-1,0], [0,0,-1]])`, but actually SageMath has a function `identity_matrix` that can be used instead. Below we demonstrate how to use SageMath help system to get its documentation:


~~~
?identity_matrix
~~~
{: .source .python}
Hence, we will define `A` using this special function.


~~~
A = -identity_matrix(3)
A
~~~
{: .source .python}



~~~
[-1  0  0]
[ 0 -1  0]
[ 0  0 -1]
~~~
{: .output}


Now we multiply this matrix and symbolic vector using `*`


~~~
A * v
~~~
{: .source .python}



~~~
(-x, -y, -z)
~~~
{: .output}


We can substitute values of variables as follows:


~~~
v.subs(x=1, y=0, z=3)
~~~
{: .source .python}



~~~
(1, 0, 3)
~~~
{: .output}




~~~
A * v.subs(x=1, y=0, z=3)
~~~
{: .source .python}



~~~
(-1, 0, -3)
~~~
{: .output}




~~~
A * v
~~~
{: .source .python}



~~~
(-x, -y, -z)
~~~
{: .output}




~~~
_.subs(x=1, y=0, z=3)
~~~
{: .source .python}



~~~
(-1, 0, -3)
~~~
{: .output}


In the cell above, the underscore `_` refers to the result of the last executed command, that is of `A*v`.
