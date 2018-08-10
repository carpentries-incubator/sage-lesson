---
title: First session with SageMath
teaching: 30
exercises: 0
questions:
- "..."
objectives:
- "..."
---

In this episode, we demonstrate how to use SageMath for simple calculations in order to became familiar with the SageMath Jupyter interface.

You can use SageMath as a calculator:


~~~
1+1
~~~
{: .source .python}



~~~
2
~~~
{: .output}


Lists cab be entered as follows:


~~~
[[1,2], [3,4]]
~~~
{: .source .python}



~~~
[[1, 2], [3, 4]]
~~~
{: .output}


A list does not automatically become a matrix. This has to be specified explicitly:


~~~
m=matrix([[1,2], [3,4]])
~~~
{: .source .python}
In this case, we assigned the result to a _variable_ called `m`. Sage performs the command but does not display its result. If you want to inspect `m`, you need to do the following:


~~~
m
~~~
{: .source .python}



~~~
[1 2]
[3 4]
~~~
{: .output}


You can combine several commands in the same cell as well:


~~~
m=matrix([[1,2], [3,4]])
m
~~~
{: .source .python}



~~~
[1 2]
[3 4]
~~~
{: .output}


The fact that `m` is a matrix will allow to perform further operations (try to perform them with a list and you will get an error)


~~~
m^-1
~~~
{: .source .python}



~~~
[  -2    1]
[ 3/2 -1/2]
~~~
{: .output}




~~~
m*m^-1
~~~
{: .source .python}



~~~
[1 0]
[0 1]
~~~
{: .output}


But:


~~~
[[1,2], [3,4]]^-1
~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
TypeError Traceback (most recent call last)
<ipython-input-8-8755d237bf1c> in <module>()
----> 1 [[Integer(1),Integer(2)], [Integer(3),Integer(4)]]**-Integer(1)

/Applications/SageMath/local/lib/python2.7/site-packages/sage/rings/integer.pyx in sage.rings.integer.Integer.__pow__ (build/cythonized/sage/rings/integer.c:14174)()
   2087 return left * int(right)
   2088 # left is a non-Element: do the powering with a Python int
-> 2089 return left ** int(right)
   2090 
   2091 cpdef _pow_(self, other):

TypeError: unsupported operand type(s) for ** or pow(): 'list' and 'int'
~~~
{: .error}
Another common type of error is when one tries to use a variable name that does not exist in the current SageMath session will lead to an error:


~~~
y
~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
NameError Traceback (most recent call last)
<ipython-input-9-9063a9f0e032> in <module>()
----> 1 y

NameError: name 'y' is not defined
~~~
{: .error}
SageMath is able to convert operands to a suitable type in many scenarios, for example


~~~
1/2+1.5
~~~
{: .source .python}



~~~
2.00000000000000
~~~
{: .output}


It also allows to _overload_ operations - for example, `+` may be use to add numbers and also to concatenate strings and lists:


~~~
"ab" + "c"
~~~
{: .source .python}



~~~
'abc'
~~~
{: .output}




~~~
[1,2]+[3,4]
~~~
{: .source .python}



~~~
[1, 2, 3, 4]
~~~
{: .output}


On the other hand, when operations is not possible, an error will happen, for example


~~~
"a" * "b"
~~~
{: .source .python}

~~~
---------------------------------------------------------------------------
TypeError Traceback (most recent call last)
<ipython-input-13-546e1eb79f21> in <module>()
----> 1 "a" * "b"

TypeError: can't multiply sequence by non-int of type 'str'
~~~
{: .error}
Finally, SageMath also have graphical capabilities. An easy 2D graphics example is shown below. In the next episodes you will see 3D examples.


~~~
plot(sin, (0,10))
~~~
{: .source .python}



![png](../01-introduction_files/01-introduction_26_0.png)


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
