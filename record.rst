Record
--------

Terms

Tab under record: The tab which will be/is recorded.

Select a tab to record

1. Navigate to the URL you'd like to record.

2. Click the RITE browser icon on Chrome.

3. Click the RITE option in the popup dialog.

This will open the RITE main console, and also sets the selected tab as the tab under record. Note that it's allowed to change the tab under record while the main console is opened.

Start recording the tab

Click the record button in the RITE main console. By design, the tab under record should be popped up to front and ready to record now. To check if it's properly working, you could move your cursor in page, and find whether the dom elements are yellow highlighted. 

If not, there are several potential causes:

1. The tab was opened before installing the RITE extension. This is very likely to happen to the first time users. You could simply refresh the tab under record and check it again.

2. The tab under record was accidentally closed. The solution is to select a new tab to be recorded.

3. The URL doesn't allow recording. For example:
   chrome://extensions/, 

https://chrome.google.com/webstore/category/home, and a few more.

**How RITE recording works**

RITE injects a content script in the tab under record which

* Adds event listeners to dom events including mousedown, mouseover, mouseout, change, submit, keydown, dlbclick, and mouseup.
  All of the listeners are registered on document object in capturing phase, which guarantees we could intercept the events on most of the sites.
 
* When an event is caught, the content script will send info back to the background page including action, element locating related info,  iframe info etc.

**What are recorded?**

* The common actions while users are interacting with page, for example the clicks, types, selects, etc.
 
* The dom element's information which is used to locate it while playback.

* The data inputs like a query.

* Other important actions like `verification`_.

.. _verification: verification.html

**What are NOT recorded?**

* RITE can only record Dom level events/elements, that said, anything outside the target page can not be recorded. For example, the browser back button, address bar etc.

* Flash can not be recorded.

* The keyboard strokes are not recorded, for example, "Enter" key. This excludes the typings in input boxes.

* Mouse wheel, right mouse click can not be recorded.

* Complex scenarios, for example, elements within dynamically created iframes can not be recorded.


**Limitation**

 RITE currently only supports recording one Chrome tab at a time.

   **Comments**

      You do not have permission to add commen
