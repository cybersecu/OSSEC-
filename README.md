# ossec.github.io
These are the files for the official OSSEC Project website. They are built automatically from the ossec/ossec-docs repo by Travis when pull requests are made for that repo after the website source files are updated. DO NOT MAKE CHANGES TO FILES IN THIS REPO. If you want to update the website, edit the files in ossec/ossec-docs and let Travis do the rest.

Requirements
The source website files in ossec/ossec-docs consist of Sphinx and HTML template files, so you require Python and sphinx-build to update the website. In most cases you will need to modify the website when a new OSSEC release has been created or a blog entry is added.

Updating the Downloads page
Fork the ossec/ossec-docs repo
cd into the ossec-docs directory
Edit the downloads.rst file
Run make html.
Open the _build/html/index.html file in a browser.
Check to see the test wbesite looks OK.
Repeat steps 3-6 until you have it the way you want.
Push you changes to your fork of ossec-docs.
Create a pull request for your changes.
Adding a blog entry
Fork the ossec/ossec-docs repo
cd into the ossec-docs directory
Add your blog entry to the blog/posts directory. The naming convention is YYYY-MM-DD-title.rst.
Add the following code to your blank file:
.. post:: MMM DD, YYYY
  :tags: 'your tags'
  :category: 'your categories'
  :author: 'your name'
  
======================
'your title goes here'
======================

'your content goes here'
Put your date, tags, categories, and name in the corresponding fields.
Add a title below this section that has a row of '=' before and after the title that are the same charter length as the title.
Add and edit your content below the title.
When you are done writing, run make html.
Open the _build/html/index.html file in a browser.
Check to see the test wbesite looks OK.
Repeat steps 7-10 until you have it the way you want.
Push your changes to your fork of ossec-docs.
Create a pull request for your changes.
