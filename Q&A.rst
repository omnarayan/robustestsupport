Q&A
----

**General**



Q: What technologies are used in RITE?

A: RITE is a `Chrome extension <http://code.google.com/chrome/extensions/getstarted.html>`_ and everything is Javascript.


Q: How does RITE handle logic controls like if/else, and while loop?

A: For simplicity reason, RITE doesn't handle logic controls/loops anymore. Users are welcomed to export the tests in Java code and edit it themselves.


Q: How can I add a custom function?

A: You could either write your own Javascript function or pick one from store. You can also submit yours to the store under certain category, so others could leverage it.

Q: How should I validate my site?

A: Go and take a look at our sample code site or browse through the handy methods store to learn what other users are validating.


Q: Who are the potential users?

A: Use cases:

- A tester with some existing automation using Webdriver.
	- RITE could be used to generate webdriver code.
	- RITE could be used to maintain the locators.
- A dev who just wants to have some simple regression tests.
	- RITE could be used to generate tests, saved to the cloud, and playback later.
- A user who wants to repeat some actions, like goes to a website, does a query and checks for the camera price.
	- RITE could generate such a script.
- A fresh tester who wants to learn how to test his/her websites.
	- From code samples and methods store, he/she could learn how other people are testing their websites.
- A dev who is investigating a bug.
	- RITE provides screenshots for a bug to show how the bug was found.
	- If the environment has not changed, RITE could replay step by step for further investigation.
- A Chrome OS member.
	- RITE is a pure Chrome Extension in Javascript, so it’s compatible with Chrome OS.
- A lead who wants to monitor his project.
	- From the backend server, the results of each run should be displayed, which could be used to monitor the project.

.. image:: image/trends.png



**Recording**


Q: Why it doesn't record the text I typed in a text box?

A: RITE records the onchange event in page, and usually the event occurs when the text box loses focus, which in other words, might mean clicking on somewhere else. For example, when you perform a search, usually you might type in some key words, and click the submit button, at which point that both of the type and click commands are generated. Another possible reason is that the box is inside a dynamically generated iframe, for example, Gmail or the Google+ sharebox. In this case, we could write JS functions to simulate the steps. 


Q: How to wait until an expected element shows up?

A: Sometimes you might need to wait until certain new UI shows up before continue. In this case, we could add a verify command for an element in the new UI. During playback, it will wait until the element shows up as long as it's within the valid interval. 

Q: Why didn't my recorded script perform correctly?

A: This could be caused by many reasons. 

- One of the common scenarios is that, you might have clicked a link to do some xhr request and show up a new UI and then continue interact with elements within it. In this case, it's likely sometimes RITE tries to execute the following commands without waiting until the UI shows up, you could add a verify command for an element in the new UI during recording to solve the waiting issue.

- Another common issue is that for some reason the generated script has a bug, for example, it might miss generating a command if recording was too fast or some cases that RITE couldn't record like flash, etc.

- The process you've recorded is not reproducible. For example, you might have clicked a link to delete an item in your script. Unfortunately, in this case, it wouldn't be able to playback because the link no longer exists.

Q: How do I update a recorded script?

A: After recording a script, you might want to inject new recorded steps in the original one, update an xpath, or move the step up and down. These could be achieved within the details dialog by double clicking a generated line in editor.


 
Q: Why can't I record the page?

A: There could be several causes:

1. The tab was opened before installing the RITE extension. This is very likely to happen for first time users. You could simply 
refresh the tab under record and then it should work.

2. The tab under record was accidentally closed. The solution is to select a new tab to record.

3. The URL doesn't allow recording. For example: Blank page (about:blank),  




https://chrome.google.com/webstore/category/home, and a few more.



Q: How do I select a new tab to record?
A: You could switch to a new tab and continue recording at any time by 1. Go to the target URL in the new tab. 2. Click the RITE extension icon in the top right corner on Chrome. 3. Select the Record/Playback option again in the popup dialog. Now the RITE main console should be in the front, and the new tab has been successfully selected to record.

**Playback**

Q: Why can't I playback my script?

If you couldn't playback a script, for example, a new tab is not automatically opened for playback, or it's stuck at certain point which is not expected, you could always try the stop button in the playback runtime dialog, which will clear the playback status. Now you could try playback again.

Q: Why did it click the wrong video/item when playback?

By default, RITE locates elements by matching the attributes, and whichever element matches the most succeeds. This works well in dealing with the dynamic attributes, but on the other side, it's possible to choose an element that's not original at all. What you could do is to set some attributes to "Must", and this will force to find either the exact element or fail.


**Save and Load**

Q: Why do I see errors when I load/save a script?
	- The server is on top of appengine, which occasionally has hiccups to store/load projects and scripts. This should be very rare, and you have to wait until it goes back.
	- Since a limit on appengine storage, the script length can not be too long, otherwise it will return a 500 error while saving.


**Limitation**


Q: What limitation does RITE have?

A: 
	- RITE is a Chrome extension and mostly can only work with Chrome. 
	- RITE only supports recording one tab at a time and doesn't record flash. 
	- It doesn't handle conditions or loops unless you manually write up custom JS functions. 
	- There isn't a way to reuse a script from another script at this point.
	- Doesn't record keyboard commands. 
	- Doesn't support recording native dialogs like uploading stuff.


**Comments**

You do not have permission to add comments
