Useful tips
-----------

**Main console**

- Double click on a generated command like click(...), verify(...) will open the Details   dialog.
- Ctrl + Alt +s to switch the generated script to readable mode and switch back.

**Record**

- To change the tab under record, click the RITE option in extension popup again. To check if the new tab is selected correctly, you could enter record mode and see if the new tab is popped up to the front and ready to record.
- To record an action like verify, verify not, and mouseover, try right clicking on the target element. In the popped up dialog in console, select the correct action and save the command.
- Always keep an eye on the generated code during recording. Most of the time, it should be obvious to understand the syntax. When there is a URL redirection happens, it should generate a redirectTo command following the original action command. 
- Make sure the page is properly loaded and the dom element is yellow highlighted before performing actions, otherwise, it might miss recording the step.
- To turn the Xpath finder on, you'll need to check the option "Use Xpath" in the settings dialog which could be opened by clicking the settings button in the RITE menu bar.
- During recording, if a new tab is opened after clicking a link, you are still able to record in the original tab but the new tab. 
- Due to an `extension bug`_, RITE couldn't perform well in case of dynamically created iframes. For example, Gmail or the Google+ sharebox. As a workaround, it's possible to write up JS functions to simulate the behaviors.

.. _extension bug: https://code.google.com/p/chromium/issues/detail?id=76429

**Playback**

- To run a whole project or any number of scripts within a project, you'll need to load the project first, and select the script names in the playback runtime dialog and play. In the end, it will show the links to view the results.
- You could cancel the whole run of multiple tests by clicking the X button in the playback runtime dialog. It only appears when you are running multiple tests.
- Try the stop button in playback runtime dialog to clear any playback status in case anything gets stuck.

**Code**

- The commonly generated commands are the followings:
   - click(Element)  / dblclick(Element) / ...
   - type(Element, Variable) / select(Element, Variable) / verify(Element, Variable) /...
   - redirectTo(URL)
   - call(Custom Function)
   - changeUrl(URL), which could be manually typed in editor to perform a redirection.

**Xpath finder**

- "Shift" to pause/resume the content changing in Xpath finder.
- Turn on/off the checkboxes to customize the xpath.

**Comments**

   You do not have permission to add comments.
