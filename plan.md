### Goal

The final goal of The Floor Ate It (TFAI) project is to make a web app that serves as a personal inventory system. It should be able to host multiple users, and each user should (only) be able to create and manage their own inventories.

 

### Structure

Each user should have a list of locations and a list of items. Each item would contain information about the item including the location it's stored at, and possibly the category, the quantity, a description, etc.

The following tables are definitely needed:

**User**
- id: primary key; required; automanically created unique id
- username: requried; unique id chosen by user, used to identify user

**Location**
- id: primary key; required; automanically created unique id
- user: foreign key; required; identify which user the location belongs to
- name: required; name of the location
- description: a description of the location

**Item**
- id: primary key; required; automanically created unique id
- user: foreign key; required; identify which user the item belongs to
- location: foreign key; the location where the item is stored
- name: required; name of the item, or a primary description
- description: a more detailed desctiption of the item
- category (maybe): the catecory in which the item belongs


The following tables are good to have but not absolutely necessary. Still deciding if add.

**Category**
- id: primary key; required; automanically created unique id
- user: foreign key; required; identify which user the category belongs to
- name: required; name of the category
- description: a description of the category



### Endpoints

##### `/`, `/login`
- Homepage and login page

##### `/locations`, `/items`
- display a list of locations/items

##### `/locations/<location_id>`
- display items at a specific location

##### `/locations/add`, `/items/add`
- add locations/items

##### `/locations/<location_id>/edit`, `/item/<item_id>/edit`
- edit specific location/item

##### `/locations/<location_id>/delete`, `/item/<item_id>/delete`
- delete specific location/item
