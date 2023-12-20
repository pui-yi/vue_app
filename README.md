# Working with Vue JS
Here is the <a href="https://exuberant-stretch.surge.sh/">URL</a> to my web application.
<br><br>

## Objective:
Simple application to use the basic features of Vue JS. Users should be able to use this application to check information about an event that will happen in December.
<br><br>

## Tasks:
There will be at least 4 seminars read from a JSON file and here are more details for the pages and JSON file:
- The seminars, in the JSON file should have:
  - ID - it should be a unique value;
  - Title - title of the event;
  - Location - it can be the room where the event will happen;
  - Start Time - it should be in string format such as 9:00AM or 2:00PM, etc.;
  - Short Description - a sentence that summarizes what the seminar is about

- All pages (Home, Seminars, Details, Contact)should have the same navigation bar using Vue Router – the navigation bar should have a small logo for the Event Organizer – this image should be positioned to the right or left of the menu – this will be all part of the root component of the application as it will be shown in all pages!

- The Home page should present the name of the Event Organizer and some details about the whole Event (such as price, promotions, what the event is about) – create a nice content to invite the users to explore the Seminars using the menu and even to use the Contact of the menu in case they need to contact the Event Organizer.

- The Seminars page should present the list of seminars as hyperlinks (using the route parameter - it will bring the title of the seminars from the JSON file).

- The Details page will exist for each seminar that will present a heading with the title of the seminar, a paragraph with the short description, location, and start time.

- A Contact page that will have a form with the following fields: 
  - Input text box for the full name of the user (the full name should have at least 10 characters and should be required) 
  - Input email box for the email of the user (it should be required) 
  - Textarea so the user can type a question or any comments (this should be required and should have at least 3 characters) 
  - The submit button – when clicked, if there is no error,  the application will only display in an area outside the form what the user typed as a confirmation for the user
  - Create error messages that will be shown for each of the fields that have a minimum of characters
<br><br>

## Feedback:
From Claudia Ferreira Da Silva: "Great work - my advice is to avoid centralizing content on the page as it causes eye strain as it's not the normal movement of the eye (it's left to right) Nice passing of props to the Details page of the seminar when clicking on the desired seminar."
<br><br>

## Screenshot:
