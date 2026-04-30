# Master Spreadsheet Procedure

_By: Alexa Accuardi_

The goal of this procedure is to present the proposed structure for the master spreadsheet for TAs, admins, and instructors that will be responsible for its upkeep moving forward. This spreadsheet is structured like a lightweight relational database inside Excel.
Instead of storing duplicated or pre-aggregated data, it uses normalized tables and formulas to dynamically generate views and dashboards.

The goal of this approach is to help with data consistency, support flexibility for reporting needs, and scale better as HAAG grows.

### Core Design Principles

#### 1. Single Source of Truth

All relationships between people, projects, and roles are stored in `ProjectAssignments`. This information should not be duplicated elsewhere.

#### 2. Normalized Data Structure

Each table has a clear responsibility:

| Table              | Description                                                                                                                                                                                                                                                    |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| People             | One row per person. Stores name, email, and notes.                                                                                                                                                                                                             |
| Projects           | One row per project. Stores project name, faculty, unit, status, and other logistics information like channel link and meeting time.                                                                                                                           |
| Roles              | Static list of the valid roles to keep naming consistent.                                                                                                                                                                                                      |
| Units              | Static list of the units the research teams are assigned to.                                                                                                                                                                                                   |
| ProjectAssignments | Each row represents a person's assignment to a project and their given role. This enables a person to have multiple roles across different teams and for a project to have variable numbers of managers, researchers, volunteers, computational advisors, etc. |
| Enrollments        | Enrollments tracks additional groupings (such as which students are enrolled in various courses). This is to help validate active enrollments and any discrepancies semester to semester.                                                                      |

### Patterns and Features

#### Sheet Relationships

Instead of IDs, this system currently uses names (Person Name, Project Name, Role Name, etc.) as the "keys" to link tables together. This was done for simplicity and readability.

#### Data Validation (Dropdowns)

Where possible, data validation is used to enforce consistency across tables and prevent typos.

#### Validation page

A \_validation sheet was created as an easy way to view filtered sets from the list (for example, active projects). These columns can be used to drive dashboards.

#### Dashboard

Since the previous spreadsheet was sorted into tabs by faculty member, the Faculty Dashboard provides an easy way to see all teams and their participants for a particular faculty member.

### How to Add or Update Data

Right now all data is added to this sheet manually. Finding a more intelligent way to power this information was out of scope for this project, but would be an excellent enhancement moving forward.

#### Adding a Person

1. Add to **People** table
2. Ensure name is consistent

#### Adding a Project

1. Add to **Projects** table
2. Set:
   - Faculty
   - Unit
   - Status

#### Assigning Someone to a Project

1. Go to **ProjectAssignments**
2. Add a new row:
   - Person
   - Project
   - Role
   - Notes (optional)
