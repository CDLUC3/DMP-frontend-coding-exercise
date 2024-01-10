# DMP-coding-exercise
Provides the requirements for the coding exercise for the 2023 Senior Frontend Web Developer position.

Guide for Hiring Committee
For the programming exercise, candidates will use the DMPTool API to create a dashboard to illustrate and be assessed on the following:
Assess the structure of their project and what libraries/packages used
Demonstrate how to fetch data from an external API
Demonstrate error handling (an invalid DMP ID will returns a 404)
Demonstrate how to process an API response (Arrays, nested Objects, etc.)
Demonstrate how to build a React component and bind form fields
Demonstrate software development best practices
Test Driven Development 
Clear and substantial Documentation 

All candidates will receive the coding exercise on Friday afternoon 1/12 with a request to submit their solution by Wednesday 1/17 at 9am.  This will allow some time for the interview team to review the solution before their interview.  The candidate should complete the requirements as stated.  If the candidate cannot complete the exercise within the time provided, he/she should be prepared to discuss the solution that was to be implemented. 


DMP Dashboard Coding Exercise

Using React, build a single-page web application.  The application will display a list of Data Management Plans (DMPs).  A user should be able to perform the following actions on the Dashboard:

Sort the DMPs by ‘title’ or ‘modified’ date
Edit certain fields (see field list below)
Save any changes

Data Source:
Retrieve a list of DMP records by DMP ID using the DMP Tool API (e.g. https://api.dmphub.uc3stg.cdlib.net/dmps/10.48321/D1J31B):

List of DMP IDs:
['10.48321/D1J31B','10.48321/D1R316','10.48321/D10601','10.48321/D1CW23','10.48321/D1930S','10.48321/D1DW5J','10.48321/D1ERROR']



Processing the response:
A DMP record can be quite large. You only need to present the following fields to the user. We have included the HTML element we expect you to use along with the source (the field’s location within the JSON response from the API). The blue fields should be editable.

DMP ID (display type: hyperlink, source: dmp.dmp_id.identifier)
Last Updated (display type: text, source: dmp.modified)
Title (required: true, display type: input - text, source: dmp.title)
Contact Email (required: true, display type: input - email, source: dmp.contact.mbox)
Contributor Count (display type: text, source: dmp.contributor)
Abstract (required: false, display type: textarea, source: dmp.description)
Funder (display type: text, source: dmp.project[0].funding[0].name)
Opportunity ID (required: false, display type: input - text, source: dmp.project[0].funding[0].dmproadmap_funding_oppotunity_id)

The save button should supply the user with a confirmation message, but the call to the API to save the changes should just be stubbed out for now.

Code Exercise Requirements:
Use React components to organize your code
Provide some basic styling to the web application
Provide error handling
Provide inline documentation 
Provide a README file with instructions on how to build and run the app
Post your solution to Github to share with the hiring committee


Presentation and Discussion of Solution:
During the interview, we ask that you please walk us through your approach and implementation, highlighting areas of best practices utilized, why you chose those practices, any challenges you may have encountered, decisions you made and why you made them, and any other considerations you would like to highlight.  

The hiring committee will ask questions about your solution.  

This web application is intended to run in a desktop browser.  Be prepared to discuss what needs to be considered to make the application responsive and accessible.  What might you consider to make this application production-ready?

