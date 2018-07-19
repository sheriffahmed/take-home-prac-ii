# Take-Home Practical II Exam

## Overview

This exam should be completed solo. No Slack or other chat platforms, no email, and no asking questions on StackOverflow. You are welcome to utilize the full extent of your resources otherwise - Google is fair game, looking at existing threads on SO is okay, and MDN is encouraged.

Your task today is to create a shared notetaking app. This app should be similar to Google Keep or Evernote, but without a login, and with notes accessible to all users.

There is no .sql file provided for this. It is up to you to conceptualize a database structure and create a seed file for your Postgres database. Notes and their content should be saved on the backend, but beyond that, the division of labor between frontend and backend is up to you.

## Frontend Schema

Your frontend should have the following routes and functionalities:

**'/'** - Homepage. Should include a header with the text 'Forevernote" and two buttons: "About" and "View Notes".

*Memo for all subsequent routes:*
Every other page on the site, other than the homepage, should have a navbar with 'Forevernote' in the upper-left corner of the screen. That should link to '/'. It should also have links to 'About' and 'View Notes' on the right-hand side, evenly spaced. These should link to '/about' and '/notes', respectively.

**'/about'** - About page. Nothing here but a centered header ('About') and underneath that, [lorem ipsum](https://loremipsum.io/) text.

**'/notes'** - Notes page. Should include a (justified left) header ('All Notes'). Underneath that, there should be an evenly-spaced grid of note previews. Note previews should include the title and first couple sentences of the note, and they should be about 150 by 150 pixels (include more or less space to accommodate text). Note previews should populate from left to right, and from top to bottom. Therefore, the first note preview should occupy the upper-left space, and the second should go to the right, and so on. If there is not enough horizontal space, note previews should wrap to a new line. Clicking on any note preview should take you to the '/notes/:id' route for that note's ID. Underneath the note previews, there should be a button, 'New Note', that should take you to the route '/notes/new'.

**'/notes/new'** - New Note page. Should include a (justified left) header ('New Note'). Underneath that, there should be a form with two labeled fields: a small text input for the title and a larger text input for the note's body. Finally, there should be a button ('Submit') to finalize the creation of the new note. Once the new note is created, the user should be redirected to the route '/notes'.

**'/notes/:id'** - Single Note page. Should include a (justified left) header with the note's title. Underneath, should include a (justified left) text area with the note's text. The text for these notes can be lorem ipsum or any other stand-in text (we recommend [corporate ipsum](http://www.cipsum.com/)). Underneath that, there should be a button that reads 'Edit Note'. This should redirect the user to '/notes/:id/edit' for that note's ID. There should also be a button that reads 'Delete Note'. This should delete the note and redirect the user to the '/notes' route.

**'/notes/:id/edit'** - Edit Note page. Should look identical to the New Note page, except instead of blank input fields, inputs should populate with the previous text of the note. The 'Submit' button, instead of creating a new note, should edit the current one. It should still redirect the user to the '/notes' route.

## Wireframes and Styling

In this folder, you should find several .png images that should give you a sense of what this app should look like, structurally. However, beyond this template, we'd like you to express some creativity with how this app looks. You should use at least two colors and at least two fonts imported from Google Fonts. Spacing does not have to be pixel-perfect with the wireframes. Background images and the like are acceptable, as long as they don't distract from the core functionality of the application. If you have any questions, feel free to reach out.
