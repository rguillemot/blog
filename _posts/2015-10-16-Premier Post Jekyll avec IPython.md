---
layout: post
title: "Premier Post Jekyll avec IPython"
tags:
    - python
    - notebook
---
Bonjour je m'appelle Richard Guillemot.

**In [1]:**

{% highlight python %}
a=1
{% endhighlight %}

**In [3]:**

{% highlight python %}
print(a)
{% endhighlight %}

    1


**In [4]:**

{% highlight python %}
%pylab inline
{% endhighlight %}

    Populating the interactive namespace from numpy and matplotlib


**In [5]:**

{% highlight python %}
from pylab import figure, show
from numpy import arange, sin, pi

t = arange(0.0, 1.0, 0.01)

fig = figure(1)

ax1 = fig.add_subplot(211)
ax1.plot(t, sin(2*pi*t))
ax1.grid(True)
ax1.set_ylim( (-2,2) )
ax1.set_ylabel('1 Hz')
ax1.set_title('A sine wave or two')

for label in ax1.get_xticklabels():
    label.set_color('r')


ax2 = fig.add_subplot(212)
ax2.plot(t, sin(2*2*pi*t))
ax2.grid(True)
ax2.set_ylim( (-2,2) )
l = ax2.set_xlabel('Hi mom')
l.set_color('g')
l.set_fontsize('large')

show()
{% endhighlight %}


![png]({{ site.baseurl }}/notebooks/Premier%20Post%20Jekyll%20avec%20IPython_files/Premier%20Post%20Jekyll%20avec%20IPython_4_0.png)

