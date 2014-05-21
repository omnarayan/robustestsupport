Code generation
---------------

.. image:: image/image9.png

In this page, we'll use the following scenario: A user clicks the video link on Google home page, and the page redirects to the Google videos page. The user then clicks the news link on Google videos page, and it redirects to Google news page afterwards.

The above image shows the snippet of generated code whose syntax is relatively self-explanatory. 

**How to read the generated code**::

 /**
  *@fileoverview
  
  *@author
  
 */

The top doc string documents the site that the script starts on is Google home page, as well as the author info.

`click(getElem("click-span-Videos-345"));`

From this line, we know that it's talking about a click action is performed on an element which has Videos as text. 

`redirectTo("http://www.google.com/videohp?hl=en");`

This line doesn't do anything and only acts like a comment.


**Under the cover**

RITE generates click(getElem("click-span-Videos-345")); when user clicks on the video link. The syntax is composed of three parts:

1. Action. In this case, it's a click action. It could also be a type, verify, select, or move, etc.

2. getElem. This is an internal defined function which reads a step id and returns the associated dom element.

3. Step id. During recording, RITE actually collects much more information like screenshot, the dom element's attributes, location, xpath, etc. and hide them from users. The information is associated with the step id, which in this case is "click-span-Videos-345". The step id is generated on the fly which is composed of step action, dom element's tagname, text/value, and a random number.

In short,  the generated command syntax is simply ACTION(STEP ID, DATA VAR), which represents you've done some actions and maybe with some inputs to a particular dom element. We might get rid of the "getElem" syntax at some point since it's not recommended to manually modify the script any more. 

   **Comments**

      You do not have permission to add comments.
