---
title: Rotational Subgroup
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---


~~~
g
~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-1-f5302386464f> in <module>()
----> 1 g

NameError: name 'g' is not defined
~~~
{: .error}


~~~
counteven=0
g_even = []
for i in range(count):
    if (((g[i]).determinant()-1).abs() < 0.01):
        counteven += 1
        g_even.append(g[i])
        print(g_even[-1], counteven) #



~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-2-c36458ec36f6> in <module>()
  1 counteven=Integer(0)
  2 g_even = []
----> 3 for i in range(count):
  4 if (((g[i]).determinant()-Integer(1)).abs() < RealNumber('0.01')):
  5 counteven += Integer(1)

NameError: name 'count' is not defined
~~~
{: .error}


~~~
closed = false

for i in range(counteven):
    for j in range(counteven):

        tmp = g_even[i] * g_even[j]
        new = true

        #create a function that compares to group elements and returns label k if it is contained in the group?
        for k in range(counteven):
            if (tmp - g_even[k]).norm().abs() < 0.01:
                new = false
                break
            
        if new:  
            print("not closed")
            closed = false
            break

if closed: 
    print ("closed")

g_even_inverse = []

#create a function that makes inverses
for i in range(counteven):
    for j in range(counteven):
        if (I3-g_even[i] * g_even[j])<0.01:
            g_even_inverse.append(g[j])
            print(g_even_inverse[-1]) #

~~~
{: .source .python}
