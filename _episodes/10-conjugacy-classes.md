---
title: Conjugacy Classes
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---


~~~
cc = []



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
NameError Traceback (most recent call last)
<ipython-input-1-de1a82d64aa5> in <module>()
  6 for j in range(Integer(4)):
  7 print("coset", i, j)
----> 8 print(g[i] * g[j] * g_inverse[i])
  9 print(g[j])

NameError: name 'g' is not defined
~~~
{: .error}
