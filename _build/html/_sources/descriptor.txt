Descriptor
-----------



**What's descriptor?**

It's well known that one of the biggest pain of web UI automation is to maintain all of the dom element locators. In RITE, we provide two ways of locating an element. The traditional way is by xpath, which will be talked in the `Xpath finder`_ section. The other way is by descriptor, which is actually an object containing all of the useful information of the dom element, for example the attributes, location, iframe info, etc. 

.. _Xpath finder: Xpath-finder.html

**How does descriptor work?**

RITE uses a scoring algorithm to give all of the potential candidate elements scores based on how they match the information recorded in descriptor.  The element which gets the top score succeeds. Because of the fuzziness, the recorded automation becomes less fragile than before. For example, some element might have a random id, or some of the minor attributes have been changed, etc. In those cases, descriptor can do a very good job to continue getting the elements.

By default, RITE uses descriptor to locate elements. If you feel more comfortable with xpaths, you could turn the "Use Xpath" option on in the settings dialog.

  **Comments**

  You do not have permission to add comments.
