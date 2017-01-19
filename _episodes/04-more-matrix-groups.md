---
title: Matrix Groups
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---

Matrix groups involves $A1^3$, $A3$, $H3$.

with Episode 5 - order of group, order of elements, inverses, traces, determinants
A1^3 here: sub in simple roots into the general reflection formula above, then generate the group

$A_1^3$: $\alpha_1=(1,0,0)^T, \alpha_2=(0,1,0)^T, \alpha_3=(0,0,1)^T$



~~~
g=[]
count=3
g.append(reflection_matrix([1, 0, 0]))
g.append(reflection_matrix([0, 1, 0]))
g.append(reflection_matrix([0, 0, 1]))

g

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


I3 = identity_matrix(3)

g_inverse = []

for i in range(count):
    for j in range(count):
        if (I3-g[i]*g[j])<0.01:
            g_inverse.append(g[j])

I3 = identity_matrix(3)        
tmp = identity_matrix(3)
for i in range(count):
    for j in range(10):
        tmp = tmp * g[i]
        if (tmp - I3).norm().abs() < 0.01:
            break
    print(g[i].determinant(), g[i].trace(), j)




~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-1-8c25b261fd22> in <module>()
  1 g=[]
  2 count=Integer(3)
----> 3 g.append(reflection_matrix([Integer(1), Integer(0), Integer(0)]))
  4 g.append(reflection_matrix([Integer(0), Integer(1), Integer(0)]))
  5 g.append(reflection_matrix([Integer(0), Integer(0), Integer(1)]))

NameError: name 'reflection_matrix' is not defined
~~~
{: .error}


~~~
# bit of conjugacy classes if you fancy - tidy up and do set of sets here?

for i in range(4):
    for j in range(4):
        print("coset", i, j)
        print(g[i] * g[j] * g_inverse[i])
        print(g[j])


~~~
{: .source .python}

~~~
('coset', 0, 0)

~~~
{: .output}

~~~
---------------------------------------------------------------------------
IndexErrorTraceback (most recent call last)
<ipython-input-2-9bb3d9711914> in <module>()
  4 for j in range(Integer(4)):
  5 print("coset", i, j)
----> 6 print(g[i] * g[j] * g_inverse[i])
  7 print(g[j])
  8 

IndexError: list index out of range
~~~
{: .error}
Do A3 next: sub in simple roots into the general reflection formula above, then generate the group

$A_3$:  $\alpha_1=\frac{1}{\sqrt{2}}(-1,1,0)^T, \alpha_2=\frac{1}{\sqrt{2}}(0,-1,1)^T, \alpha_3=\frac{1}{\sqrt{2}}(1,1,0)^T$


~~~
K.<r> = NumberField(x^2 - 2, embedding=1.4)
g=[]
count=3
g.append(reflection_matrix([-1/r, 1/r, 0]))
g.append(reflection_matrix([0, -1/r, 1/r]))
g.append(reflection_matrix([1/r, 1/r, 0]))

g

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


I3 = identity_matrix(3)

g_inverse = []

for i in range(count):
    for j in range(count):
        if (I3-g[i]*g[j])<0.01:
            g_inverse.append(g[j])

I3 = identity_matrix(3)        
tmp = identity_matrix(3)
for i in range(count):
    for j in range(10):
        tmp = tmp * g[i]
        if (tmp - I3).norm().abs() < 0.01:
            break
    print(i, g[i].determinant(), g[i].trace(), j)



~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-3-11be0aba83ae> in <module>()
  2 g=[]
  3 count=Integer(3)
----> 4 g.append(reflection_matrix([-Integer(1)/r, Integer(1)/r, Integer(0)]))
  5 g.append(reflection_matrix([Integer(0), -Integer(1)/r, Integer(1)/r]))
  6 g.append(reflection_matrix([Integer(1)/r, Integer(1)/r, Integer(0)]))

NameError: name 'reflection_matrix' is not defined
~~~
{: .error}


~~~
# bit of conjugacy classes if you fancy

for i in range(4):
    for j in range(4):
        print("coset", i, j)
        print(g[i] * g[j] * g_inverse[i])
        print(g[j])

~~~
{: .source .python}

~~~
('coset', 0, 0)

~~~
{: .output}

~~~
---------------------------------------------------------------------------
IndexErrorTraceback (most recent call last)
<ipython-input-4-e24cf675b289> in <module>()
  4 for j in range(Integer(4)):
  5 print("coset", i, j)
----> 6 print(g[i] * g[j] * g_inverse[i])
  7 print(g[j])

IndexError: list index out of range
~~~
{: .error}
Do H3 next: sub in simple roots into the general reflection formula above, then generate the group

$H_3$:  $\alpha_1=(0,1,0)^T, \alpha_2=-\frac{1}{2}(\tau,1,(\tau-1))^T, \alpha_3=(0,0,1)^T$

$\tau$ is the golden ratio $\tau = \frac{1}{2}(1+\sqrt{5})\sim 1.618$ and satisfies the relation $\tau^2=\tau+1$.


You will need to modify the two earlier examples to either deal with $\tau$ numerically (i.e. to within a certain error) or via the recursion relation. 


~~~

g = []
count = 3

g.append(reflection_matrix([1, 0, 0]))
g.append(reflection_matrix([-1/4*(1+sqrt(5)), -1/2, -1/4*(1-sqrt(5))]))
g.append(reflection_matrix([0, 0, 1]))

# Build g

for i in range(count):
    for j in range(count):
        new = True
        tmp = (g[i] * g[j]).apply_map(expand)
        for k in range(count):
            if (tmp - g[k]).norm().abs() < 0.01:
                new = False
        if new:
            count += 1
            g.append(tmp)
            print(g[-1], count)


for i in range(count):
    for j in range(count):
        new = True
        tmp = (g[i] * g[j]).apply_map(expand)
        for k in range(count):
            if (tmp - g[k]).norm().abs() < 0.01:
                new = False
        if new:
            count += 1
            g.append(tmp)
            print(g[-1], count)


I3 = identity_matrix(3)

g_inverse = []

for i in range(count):
    for j in range(count):
        if (I3-g[i]*g[j])<0.01:
            g_inverse.append(g[j])

I3 = identity_matrix(3)        
tmp = identity_matrix(3)
for i in range(count):
    for j in range(10):
        tmp = tmp * g[i]
        if (tmp - I3).norm().abs() < 0.01:
            break
    print(i, g[i].determinant(), g[i].trace(), j)



~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-5-41818393244c> in <module>()
  3 count = Integer(3)
  4 
----> 5 g.append(reflection_matrix([Integer(1), Integer(0), Integer(0)]))
  6 g.append(reflection_matrix([-Integer(1)/Integer(4)*(Integer(1)+sqrt(Integer(5))), -Integer(1)/Integer(2), -Integer(1)/Integer(4)*(Integer(1)-sqrt(Integer(5)))]))
  7 g.append(reflection_matrix([Integer(0), Integer(0), Integer(1)]))

NameError: name 'reflection_matrix' is not defined
~~~
{: .error}


~~~
K5.<a> = NumberField(x^2 - x - 1, embedding=1.6)

g=[]
count=3
g.append(reflection_matrix((1, 0, 0)))
g.append(reflection_matrix((-1/2*a, -1/2, -1/2*(1-a)))
g.append(reflection_matrix((0, 0, 1)))

g

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


I3 = identity_matrix(3)

g_inverse = []

for i in range(count):
    for j in range(count):
        if (I3-g[i]*g[j])<0.01:
            g_inverse.append(g[j])

I3 = identity_matrix(3)        
tmp = identity_matrix(3)
for i in range(count):
    for j in range(10):
        tmp = tmp * g[i]
        if (tmp - I3).norm().abs() < 0.01:
            break
    print(i, g[i].determinant(), g[i].trace(), j+1)

~~~
{: .source .python}

~~~
  File "<ipython-input-6-cb71787085bb>", line 7
g.append(reflection_matrix((Integer(0), Integer(0), Integer(1))))
^
SyntaxError: invalid syntax
~~~
{: .error}


~~~
K.<a> = NumberField(x^2-5)

g=[]
count=3
g.append(reflection_matrix((1, 0, 0))
g.append(reflection_matrix((-1/4*(1+a), -1/2, -1/4*(1-a)))
g.append(reflection_matrix((0, 0, 1))

g

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


I3 = identity_matrix(3)

g_inverse = []

for i in range(count):
    for j in range(count):
        if (I3-g[i]*g[j])<0.01:
            g_inverse.append(g[j])

I3 = identity_matrix(3)        
tmp = identity_matrix(3)
for i in range(count):
    for j in range(10):
        tmp = tmp * g[i]
        if (tmp - I3).norm().abs() < 0.01:
            break
    print(i, g[i].determinant(), g[i].trace(), j+1)

~~~
{: .source .python}

~~~
  File "<ipython-input-7-38f40c98dc56>", line 6
g.append(reflection_matrix((-Integer(1)/Integer(4)*(Integer(1)+a), -Integer(1)/Integer(2), -Integer(1)/Integer(4)*(Integer(1)-a)))
^
SyntaxError: invalid syntax
~~~
{: .error}
