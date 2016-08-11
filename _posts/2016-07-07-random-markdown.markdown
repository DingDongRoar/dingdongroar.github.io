---
layout: post
title: "Random Markdown"
date: 2016-07-07
author: 'by Ding Dong Roar'
---
Just personal notes to myself regarding the use of *kramdown* markdown of which only the results can be seen here.

Here is some *Python*{: style="color: green"} code.

~~~ python

def status(item, action, cart):
    statusMessage = 'An item ({0}) was {1} the {2} cart.'
    print statusMessage.format(item, action, cart)


class Store:

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
            print '{:>12} {:12.2f}'.format(item, self.cart[item])
        print '=' * 25
        print '{:>12} {:12.2f}'.format('TOTAL:', sum(self.cart.values()))
        print
~~~

Sample use and output of above code:

~~~ python
>>> target = Store('Target')

>>> target.addItem('towel', 14.00)
An item (towel) has been added to the Target cart.

>>> target.addItem('soap', 8.50)
An item (soap) has been added to the Target cart.

>>> target.printReceipt()

=========================
     Target RECEIPT
=========================
        towel       14.00
         soap        8.50
=========================
       TOTAL:       22.50
~~~

More sample *Python*{: style="color: green"} code.

~~~ python
# Create a staircase of # stepping from the left side

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
![alt text](\{{ site.url }}/download-folder/file-name){: style="width: size-in-pixels"}
~~~

![avatar]({{ site.url }}/assets/myAvatar.svg){: style="width: 200px"}

I hold the following certifications:

* CompTIA A+
* CompTIA Net+
* Electronic Technology

...and, I am studying for Security+ and CCNA certification.

*[CCNA]: Cisco Certified Network Associate
