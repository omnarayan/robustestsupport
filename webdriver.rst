Webdriver
---------

**How RITE and Webdriver are related**

RITE could translate a project - a group of scripts into the Java webdriver code, which brings in several benefits:

1. The RITE generated code could be potentially run across other browsers.

2. After being translated into Java page classes, users could easily write their own code to extend the classes and implement any complicate methods.

**How to translate a RITE project to Webdriver code**

Again, let's start with a real example. Suppose we have a RITE project which contains two scripts that both start on Google home page. In one script, it navigates to Videos page then News page, and in the other, it navigates to Images page and News page.
After we load the project, let's click the project details button, and we'll see:


.. image:: image/projectdetails.png

There are three tabs in this dialog: Export, Import, and Tests.

The Export tab handles translating the project to Webdriver code. Let's give it a package path say "com.google.testing", save it, and then hit the export button. Now you should see a zip has been downloaded which might be called "tests.zip".
Open the zip and we'll find a few Java files inside:

- BasePage.java.  This contains all of the fundamental methods for automation including click, select, verifyElement, type, move, etc.
- PageGoogle0.java and PageNewsGoogle1.java. By default, RITE creates a page class for each unique domain appears in the project. In this case, we have two different domains: www.google.com and news.google.com.
- Tests.java. For each script in the project, we'll have a corresponding unit test defined in this file. 

For more details of the generated code, feel free to try it out or take a look at the attached zip.

The Import tab requires the local server, which will be discussed later.

The Tests tab will list all of the scripts within the project, and you could select any number of them for deletes.

**Extending the generated Java page classes**

Though RITE could generate Java code, you might need more complicated logic or maybe some internal API calls. In this case, you could simply write your own extended Java page classes to implement those, and leave the tedious xpath finding/maintenance work to RITE.

**A diagram describing code generation**


.. image:: image/RITECodeGenerationDesignDoc_1.png







**Comments**

   You do not have permission to add comments.
