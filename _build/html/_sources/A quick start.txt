A quick start
-------------

Before moving to each individual section, let's take a look at a real example and get hands on RITE.

**1.Prerequisites**

Please make sure you've got Chrome_ , and the latest `RITE extension`_ installed.

.. _Chrome: https://www.google.com/chrome/browser/

.. _RITE extension: https://chrome.google.com/

**2.Open example site and RITE console**

In this tutorial, we'll play with the dom elements in our `example site`_. Let's open the link in a new Chrome tab, and then click RITE icon (which is around the top right corner of Chrome), choose the RITE option in popup, and now we should see the RITE main console.

.. _example site: http://rpfserver.appspot.com/examples

**3.Start recording**

To start recording, let's click the round record button. Some changes you will notice are: The button set in menu bar changes, A project/script loading/saving area shows up, the URL of the selected page is recorded, some doc string appears in editor and if you move cursor in the tab under record, you should see elements get yellow highlighted on mouse over.

Now let's perform the following (or any number) actions:

	* Click the "change color" button

	* Click one of the radio buttons

	* Click the checkbox

	* Select an option say Chrome

	* Type in some text in the input box and click show

	* Type in some text in the text area and click show


.. image:: /image/image2.png


In the RPF editor, we will see the following scripts generated:


`click(getElem("click-input-changecolor-869"));`

`click(getElem("click-input-2-497"));`

`click(getElem("click-input-950"));`

`select(getElem("select-select-GoogleChromeAndroid-367"), ContentMap["SELECT0-488"]);`

`click(getElem("click-input-text-226"));`

`type(getElem("type-input-text-362"), ContentMap["INPUT4-206"]);`

`click(getElem("click-input-show-262"));`

`click(getElem("click-textarea-textarea-87"));`

`input(getElem("change-textarea-textarea-889"), ContentMap["TEXTAREA0-651"]);`

`click(getElem("click-input-show-652"));`

**4.Play it back**

Let's first click the stop button in the menu bar to stop recording. Now you'll have more buttons appear, and let's click the play button next to the record button. At this point we should see a playback runtime dialog shows up.

.. image:: /image/image3.png

Once we click the play button in the dialog, we'll see RPF automatically opens a new Chrome browser and executes the recorded script step by step.

**5.Save it to cloud**

Let's close the playback runtime dialog, type in the project and script name, and hit the save button in menu bar. If it's successful, the script should have been saved to the server.

**6.Load it back**

Let's click the refresh button (the last one in menu bar) to refresh the main console. Now let's click the load button to turn on the project/script area, and type in both names which you just created. Now we should see the script gets loaded back to editor. You could also try to click the camera look button on menu bar to view the screenshots of the steps to remind you of the scenario. A quick trick here is that you could try Ctrl+Alt+s to switch the view back and forth between the script and readable modes.

   **Comments**

      You do not have permission to add comments.
