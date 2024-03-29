# jQuery Accordion Section
Collapsible Accordion Section designed to be added to SharePoint page using a CEWP (Content Editor Web Part) in order to display list data in accordion format

&nbsp;
## SPFx Collapsible Accordion Section web part

* Adds a collapsible accordion to a page.
* Populate the accordion structure from a List on your site. 
* The list used to populate the accordion section must have a Title column and Content column & its name specified in the REST API in the code before deploying.
&nbsp;

![jQuery Accordion Example](./assets/jQueryAccordion.png)

&nbsp;
## Applies to

* SharePoint 2013
* SharePoint 2016
* Office 365 SharePoint (Classic Sites only) - not recommended, however.  Please see [my SharePoint Framework solution](https://github.com/ejbenke/SPFx-React-Accordion-Section)


&nbsp;
## Solution

Solution|Author(s)
--------|---------
jQuery Collapsible Accordion Section|Erik Benke


&nbsp;
## Version history

Version|Date|Comments
-------|----|--------
1.0|June 27, 2018|Initial release
1.1|September 19, 2019|Minor updates, adding to Github


&nbsp;
## Using the code
&nbsp; &nbsp;
**1) Create or use a list with a Title and a Content column:**
* The value in the Title column for each item will appear in the heading bars of the Accordion.  
* The value in the Content column for each item will appear in the collapsible content section of the Accordion    


&nbsp; &nbsp;
![Create list for use with the Accordion](./assets/ListForAccordion.png)

&nbsp; &nbsp;
**2) Add the .html file, jQuery library, jQueryUI library and css to your Site Assets folder on your site**  
* Edit the following line of code (line 28) in ClassicAccordion,html to replace "ListName" with the actual name of your list that you want to use to populate the Accordion Section:
`sEndPoint += "/_api/web/lists/getbytitle('ListName')/items";`
* In ClassicAccordion.html, either edit the paths in the first 3 lines or make sure you mirror the folder structure specified within your Site Assets folder on your site.
* Add your modified ClassicAccordion.html file to your Site Assets  
* Add jQuery library, jquery.min.js (not included in this repo) to your Site Assets. [Download jQuery](https://jquery.com/download/)
* Add my custom jQueryUI library and associated css (or generate your own and use those instead: [jQueryUI download builder](https://jqueryui.com/download/)) to your Site Assets

&nbsp; &nbsp;
![Add your code to Site Assets](./assets/FilesInSiteAssets.png)

&nbsp; &nbsp;
**3) Add a Content Editor Web Part (CEWP) to your page:**


&nbsp; &nbsp;
![Add a Content Editor Web Part](./assets/AddCEWP.png)

&nbsp; &nbsp;
**4) Configure the Content Editor Web Part (CEWP) to point to the code entry file:**
* Choose Edit Web Part and then within the Content Link field add the path of your entry file for your code:
Example of a full path: */sites/ClassicAccordion/SiteAssets/ClassicAccordion.html*

&nbsp; &nbsp;
![Configure Content Editor Web Part](./assets/EditCEWP.png)
