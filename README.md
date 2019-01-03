# SQL-CRUD-DINOS

This lab will be similar to the app we built in the [REST/CRUD lessons](https://gawdiseattle.gitbooks.io/wdi/05-node-express/express-REST-crud/00readme.html), but instead of CRUDding on a json file, we'll use sequelize to make transactions with our postgres database.

## Overview
* Start with the `seedy-dinosaurs` Node/Postgres project from the seeding lesson.
* Add `express`, `ejs`, and `express-ejs-layouts` to set up your views
* Use `method-override` to make the `PUT` and `DELETE` route work properly
* Don't forget the `body-parser` middleware to make the form data come through properly
* Since there aren't too many routes, you may opt to put them all in your main server file (as opposed to a controller)

---

## Views

### Home: 
* landing page that has a link to the _index_ view

### Index: 
* Pulls all dinos from the database and displays them in a list. 
* Each dino in the list should have an "edit" button that takes the user to the _edit_ view
* Each dino in the list should have a "delete" button that deletes the dinosaur from the database and redirects back to the list of dinosaurs.
* Somewhere on this page, include a form for creating a new dinosaur.

### Edit:
* Form should prepopulate the existing data about the dinosaur that the user wants to edit.
* Submit button updates this dinosaur in the database and redirects back to the _index_ view.

---

## Routes

Your app should include the following routes

| VERB | URL | Action (CRUD) | Description |
|------|-----|---------------|-------------|
| GET | / | Read | landing page |
| GET | /dinosaurs | Read | lists all dinosaurs |
| POST | /dinosaurs | Create | post new dinosaur to database |
| GET | /dinosaurs/edit/:id | Read | form for editting a specific dinosaur |
| PUT | /dinosaurs/:id | Update | updates the data for a specific dinosaur (id = 1) |
| DELETE | /dinosaurs/:id | Delete | deletes the dinosaur with the specified id (1) |
