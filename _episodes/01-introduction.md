---
title: First session with SageMath
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---

Lesson text



~~~
1 + 1
~~~
{: .source .python}



~~~
2
~~~
{: .output}




~~~
matrix([[1,2], [3,4]])^(-1)
~~~
{: .source .python}



~~~
[  -2    1]
[ 3/2 -1/2]
~~~
{: .output}


Output with error message:


~~~
x[10]
~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
TypeError Traceback (most recent call last)
<ipython-input-3-084faa554d6d> in <module>()
----> 1 x[Integer(10)]

TypeError: 'sage.symbolic.expression.Expression' object does not support indexing
~~~
{: .error}
Output generating figures:


~~~
plot(sin, (0,10))
~~~
{: .source .python}



![png](../01-introduction_files/01-introduction_6_0.png)


For the challenges
you need to pay attention to include `<blockquote class="challenge">`
before it and `<\blockquote>` after it.
And for the solutions
you need to pay attention to include `<blockquote class="solution">`
before it and `<\blockquote>` after it.
**This hacks is necessary for allow include Jupyter cells on challenges and solutions.**
<blockquote class="challenge">
## Challenge: Can you do it?

What is the output of this command?

~~~
"a" + "b"
~~~
{: .source}

<blockquote class="solution">

## Solution


~~~
"a" + "b"
~~~
{: .source .python}



~~~
'ab'
~~~
{: .output}


</blockquote>
</blockquote>
