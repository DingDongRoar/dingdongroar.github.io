---
layout: post
title: "Random Markdown"
date: 2016-07-07
author: 'by D.D.Rawr!'
---
Here is some code I wrote in *Python*{: style="color: green"}.

~~~ python

def status(item, action, cart):
    statusMessage = 'An item ({0}) was {1} the {2} cart.'
    print statusMessage.format(item, action, cart)


class store:

    def __init__(self, storeName):
        self.storeName = storeName
        self.cart = {}

    def addItem(self, item, price):
        self.item = item
        self.price = price
        self.cart[item] = self.price
        status(self.item, 'added to', self.storeName)

    def removeItem(self, item):
        self.item = item
        self.cart.pop(self.item)
        status(self.item, 'removed from', self.storeName)
     
    def printReceipt(self):
        print
        print '=' * 25
        print ' ' * 5 + self.storeName + ' RECEIPT' + ' ' * 5
        print '=' * 25
        for item in self.cart:
            print '{:>12} {:>12}'.format(item, str(self.cart[item]))
        print '=' * 25
        print '{:>12} {:>12}'.format('TOTAL:', str(sum(self.cart.values())))
        print
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
![alt text]({{ site.url }}/download-folder/file-name){: style="width: size-in-pixels"}
~~~

![avatar]({{ site.url }}/assets/myAvatar.svg){: style="width: 200px"}

I hold the following certifications:

* CompTIA A+
* CompTIA Net+
* Electronic Technology

...and, I am studying for CCNA certification.

*[CCNA]: Cisco Certified Network Associate
