---
title: Multiply a matrix and a vector
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---
Let us define the 3 x 3 minus-identity matrix


~~~
A = matrix([[-1,0,0], [0,-1,0], [0,0,-1]])
A
~~~
{: .source .python}



~~~
[-1  0  0]
[ 0 -1  0]
[ 0  0 -1]
~~~
{: .output}


Or simply


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


Define vector `v` to be the vector with coordinates `x`, `y`, `z`


~~~
v = vector([x, y, z])
~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-3-41c893d7dada> in <module>()
----> 1 v = vector([x, y, z])

NameError: name 'y' is not defined
~~~
{: .error}
Didn't work... We need to define `y` (and `z`) as symbolic variables. Only `x` is defined by default when you launch Sage!


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


Multiply matrix and vector using `*`


~~~
A * v
~~~
{: .source .python}



~~~
(-x, -y, -z)
~~~
{: .output}




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


