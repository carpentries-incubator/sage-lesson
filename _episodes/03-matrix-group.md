---
title: Matrix Group Closure
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---

Multiply together till you achieve closure (of the group)


~~~
count = 1

g = [A]

for i in range(count):
    for j in range(count):
        new = True
        tmp = g[i] * g[j]
        for k in range(count):
            if (tmp - g[k]).norm().abs() < 0.01:
                new = False
        if new:
            count += 1
            g.append(tmp)
            print(g[-1], count)
        
# don't do this till later
I3 = identity_matrix(3)        
tmp = identity_matrix(3)
for i in range(count):
    for j in range(10):
        tmp = tmp * g[i]
        if (tmp - I3).norm().abs() < 0.01:
            print(i,j+1)
            print(g[i]^(j+1))   # comment out or assert        
            break


~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-1-034c9970490c> in <module>()
  1 count = Integer(1)
  2 
----> 3 g = [A]
  4 
  5 for i in range(count):

NameError: name 'A' is not defined
~~~
{: .error}
Find the inverses to the group elements


~~~
I3 = identity_matrix(3)

g_inverse = []

for i in range(count):
    for j in range(count):
        if (I3-g[i]*g[j])<0.01:
            g_inverse.append(g[j])

for i in range(count):
    print (g[i])
    print (g_inverse[i])
    print (g[i]*g_inverse[i])


~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-2-cac1c24ed306> in <module>()
  5 for i in range(count):
  6 for j in range(count):
----> 7 if (I3-g[i]*g[j])<RealNumber('0.01'):
  8 g_inverse.append(g[j])
  9 

NameError: name 'g' is not defined
~~~
{: .error}
## From reflection formula find matrix?

for x'=x-2x_parallel=x-2(x.n)n/(n.n), resolve for components x=(x1, x2, x3) and n=(n1, n2, n3) find 3x3 matrix


~~~
# TODO: n-dimensional case


~~~
{: .source .python}


~~~
def reflection_matrix(v, normalize=True):
    """
    Return the reflection matrix to the plane with normal vector v
    
    INPUT:
    
      - ``v`` -- vector or any iterable that can be turned into a vector
      - ``normalize`` -- boolean (default: True)
      
    If ``normalize`` is ``False``, assume the vector is a unit vector and avoid normalizing.

    EXAMPLE:
    
        sage: a, b, c = SR.var("a b c")
        sage: A = reflection_matrix((a, b, c))
        sage: A
        [-a^2 + b^2 + c^2           -2*a*b           -2*a*c]
        [          -2*a*b  a^2 - b^2 + c^2           -2*b*c]
        [          -2*a*c           -2*b*c  a^2 + b^2 - c^2]
    """
    v = vector(v)
    m = matrix(v)
    n = len(v)
    R = v.base_ring()
    if normalize:
        return (identity_matrix(n) - 2/v.dot_product(v) * m.transpose() * m)
    return (v.dot_product(v) * identity_matrix(n) - 2 * m.transpose() * m)
~~~
{: .source .python}


~~~
n1, n2, n3 = SR.var("n1 n2 n3")

A=reflection_matrix([n1, n2, n3])

A
~~~
{: .source .python}



~~~
[-2*n1^2/(n1^2 + n2^2 + n3^2) + 1    -2*n1*n2/(n1^2 + n2^2 + n3^2)    -2*n1*n3/(n1^2 + n2^2 + n3^2)]
[   -2*n1*n2/(n1^2 + n2^2 + n3^2) -2*n2^2/(n1^2 + n2^2 + n3^2) + 1    -2*n2*n3/(n1^2 + n2^2 + n3^2)]
[   -2*n1*n3/(n1^2 + n2^2 + n3^2)    -2*n2*n3/(n1^2 + n2^2 + n3^2) -2*n3^2/(n1^2 + n2^2 + n3^2) + 1]
~~~
{: .output}




~~~
r = reflection_matrix
a, b, c = r((1, 0, 0)), r((-1/4*(1+sqrt(5)), -1/2, -1/4*(1-sqrt(5)))), r((0, 0, 1))
~~~
{: .source .python}
