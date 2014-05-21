Content Map
------------

.. image:: image/image10.png

**What's Content Map?**

ContentMap is used as the global variable storage. For example, if you've recorded a script which types in an "hello" to a search box, you might get a generated line as "type(getElem("type-button-Search-123"), ContentMap["INPUT-109"])". In the mean time, you'll see some additional code generated in the way similar to the above image, which assigns a variable with value "hello". Of course you could define your own global variable like ContentMAp['myVar'] and replace the ContentMap["INPUT4-109"] in your script. 

Another example is when you have a custom JS method defined, say::

 function sayHello(words) {
  alert(words);
 }

you could invoke it by `call(sayHello, ContentMap["myVar"]);` As a result, it will alert an "hi" during playback.

   **Comments**

      You do not have permission to add comments.
