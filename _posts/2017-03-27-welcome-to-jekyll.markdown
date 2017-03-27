---
layout: post
title:  "First Post"
date:   2017-03-27 20:00:03 +0000
categories: jekyll update
---
This blog will be used to provide updates on projects and developments in my dissertation.

Here is my solution to Google's introductory Python list exercise:

{% highlight python %}
#Function takes a list of words as input and sorts all words that begin with 'x' to the front of the list.
def front_x(words):
#Generate a placeholder array.
	xwords = []
	for word in words:
#Only append words that begin with x.  
		if word[0] == 'x':
			xwords.append(word)
			words.remove(word)
#Edge case if the list ends with an 'x'-word, append to the temporary list.
	if words[-1][0] == 'x':
		xwords.append(words[-1])
		words.remove(words[-1])
#Sort both lists separately to ensure the 'x'-words are listed alphabetically, but placed at the front.
	xwords.sort()
	words.sort()
	xwords.extend(words)
	return xwords
{% endhighlight %}
