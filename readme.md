# Student Management using ABAP Cloud RAP

A beginner learning project built in Eclipse ADT using managed RAP,
ABAP CDS, OData V4, and the SAP Fiori elements preview.

## Features

- Create, view, update, and delete student records
- Maintain Student ID, Student Name, Course, and Age
- Store unfinished changes as drafts
- Automatically maintain the last change timestamp
- Require Student ID during creation and prevent changes afterward

## Technologies

- ABAP Cloud
- ABAP RESTful Application Programming Model (RAP)
- CDS root view entity
- OData V4 UI service binding
- SAP Fiori elements preview
- Eclipse ABAP Development Tools (ADT)

## Project Objects

| Object | Name | Purpose |
|---|---|---|
| Database table | ZSTUDENT_2982 | Stores active student records |
| Draft table | ZSTUDENT_D2982 | Stores unfinished changes |
| CDS view | ZCSTUDENT2982 | Defines the data model and UI annotations |
| Behavior definition | ZCSTUDENT2982 | Declares operations, drafts, locks, and field controls |
| Behavior class | ZBP_CSTUDENT2982 | Contains custom behavior implementation |
| Service definition | ZUI_STUDENT2982 | Exposes the student entity |
| Service binding | ZUI_STUDENT2982_O4 | Exposes the service through OData V4 UI |

## How It Works

The Fiori elements preview communicates with the backend through OData V4.
RAP processes the operations and persists student data in the database.

Managed RAP handles the standard create, update, and delete logic.
CDS UI annotations define the table columns and Student Details form.

## Repository Contents

- Database: Active and draft table definitions
- CDS: CDS view source
- Behavior: Behavior definition and class source
- Service Definition: Service definition and binding settings
- Screenshots SMR: Application screenshots

## Running the Project

An SAP system supporting the project's ABAP Cloud and RAP features,
Eclipse ADT, and suitable development permissions are required.

1. Create a development package in Eclipse ADT.
2. Recreate the database table and CDS view using the supplied sources.
3. Recreate the behavior definition, draft table, and behavior class.
4. Activate the related objects after resolving their dependencies.
5. Create the service definition.
6. Create an OData V4 - UI service binding linked to that definition.
7. Activate and publish the binding.
8. Select the student entity and open Preview.

The repository contains manually copied source files and service settings.
It is not an automated installation package.
GitHub hosts the code and documentation; the application runs in SAP.

## Testing Completed

- Created students through the Fiori preview and verified database rows
- Read saved students in the list
- Updated a course and verified the database change
- Deleted a student and verified its removal from the database
- Observed the last change timestamp in database Data Preview

## Learning Scope and Limitations

This was a guided practice project for learning the RAP development flow.

- Student IDs are entered manually.
- Create authorization currently returns Allowed without a role check.
- Business validations and production authorization need further work.
- The interface is demonstrated through the Fiori elements preview.

## Author

Anshul Thakur
