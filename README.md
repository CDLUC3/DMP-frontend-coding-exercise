# DMP Dashboard Coding Exercise

Using React, build a single-page web application.  The application will display a list of Data Management Plans (DMPs).   This web application is intended to run in a desktop browser.  A user should be able to perform the following actions on the Dashboard:

- Sort the DMPs by ‘title’ or ‘modified’ date
- Edit certain fields (see field list below)
- Save any changes

**Data Source:**
Retrieve a list of DMP records by DMP ID using the [DMP Tool API ](https://github.com/CDLUC3/dmsp_aws_prototype/wiki/api-overview#data-management-plans)\
(e.g. https://api.dmphub.uc3stg.cdlib.net/dmps/10.48321/D1J31B):

**List of DMP IDs:**
['10.48321/D1J31B','10.48321/D1R316','10.48321/D10601','10.48321/D1CW23','10.48321/D1930S','10.48321/D1DW5J','10.48321/D1ERROR']


**Processing the response:**\
A DMP record can be quite large. You only need to present the following fields to the user. We have included the HTML element we expect you to use along with the source (the field’s location within the JSON response from the API). The **bolded** fields should be editable.

- DMP ID (display type: hyperlink, source: dmp.dmp_id.identifier)
- Last Updated (display type: text, source: dmp.modified)
- **Title** (required: true, display type: input - text, source: dmp.title)
- **Contact Email** (required: true, display type: input - email, source: dmp.contact.mbox)
- Contributor Count (display type: text, source: dmp.contributor)
- **Abstract** (required: false, display type: textarea, source: dmp.description)
- Funder (display type: text, source: dmp.project[0].funding[0].name)
- **Opportunity ID** (required: false, display type: input - text, source: dmp.project[0].funding[0].dmproadmap_funding_oppotunity_id)

The save button should supply the user with a confirmation message, but the call to the API to save the changes should just be stubbed out for now.

**Code Exercise Requirements:**
- Use React components to organize your code
- Provide some basic styling to the web application
- Provide error handling
- Provide inline documentation 
- Provide a README file with instructions on how to build and run the app
- Post your solution to Github in a manner that can be shared with the hiring committee

**Presentation and Discussion of Solution:**
During the interview, we ask that you please walk us through your approach and implementation, highlighting areas of best practices utilized, why you chose those practices, any challenges you may have encountered, decisions you made and why you made them, and any other considerations you would like to highlight.  

The hiring committee will ask questions about your solution.  

**Be prepared to discuss:**
- What are some frontend design patterns you could apply to this dashboard to provide more enhanced features?
- How might or did you approach component-based UI design, following React component best practices?
- What would you consider to make the application responsive and accessible?  
- What might you consider to make this application production-ready?

