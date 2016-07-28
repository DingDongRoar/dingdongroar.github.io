---
layout: post
title: "Random Markdown"
date: 2016-07-07
author: 'by D.D.Rawr!'
---
Here is some code I wrote in *Python*{: style="color: green"}.

~~~ python
class store:

	def __init__(self, storeName):
		self.storeName = storeName
		self.cart = {}

	def add_item(self, item, price):
		self.item = item
		self.price = price
		self.cart[item] = price
		print '{0} has been added to the {1} cart.'.format(self.item, self.storeName)

	def rem_item(self, item):
		self.cart.pop(item)
		print '{0} has been removed from the {1} cart.'.format(self.item, self.storeName)
~~~

~~~ python
"""
Create a staircase of # stepping from the left side
"""

def StairCase(n):
    for x in range(0, n):
        print str(' ') * (n - x), str('#') * x


OUTPUT:

       #
      ##
     ###
    ####
   #####
  ######
~~~

Here is an example of *kramdown* for adding an image to a page/post.

~~~ kramdown
![alt text](http://domain/download-folder/file-name){: style="width: size-in-pixels"}
~~~

![avatar](http://localhost:4000/assets/myAvatar.svg){: style="width: 200px"}

I hold the following certifications:

* CompTIA A+
* CompTIA Net+
* Electronic Technology

...and, I am studying for CCNA certification.

*[CCNA]: Cisco Certified Network Associate
