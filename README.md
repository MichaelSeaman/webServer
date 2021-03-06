# Toy Inventory Database

**Author:** Michael Seaman

**Due date:** 12/16/16

---

## Setup:

Running this application requires the node.js framework. Download it here:
https://nodejs.org/en/download/

Running the following command will install any dependencies not already included
`> npm install`

To run the application:
`> node server.js`

or to mount it on port 80:
`> sudo node server.js 80`

And that's it! Go to the link below to check it out!
http://localhost:3000

Also, you can view the Demo at
http://michael-seaman.com

## File Guide

* server.js - Backend of the server. Deals with database connections, handling AJAX requests, and generating reports
* /js/sqlMethods.js - Wrapper methods for the my-sql driver. Used by server.js.
* /js/generateFakeData.js - uses the faker module to generate and insert new data into the database, accounting for referential integrity
* /js/pageScript - Front end script that generates pop windows, links buttons, and sends AJAX requests to the server
* tableData.json - has all the SQL table information to be used by the application
* /public - The website/UI including index.html
* /sql - All DDL used on the database
* /node_modules - auto-generated by npm, not necessarily needed
* /electron - no longer needed, but the script to run this website as an electron app


## Proposal: Amazon Sales Database

#### Premise
The multi-billion dollar e-sales giant Amazon in 2015 alone had over 100 billion
dollars in online sales revenue, 304 million registered users, with another 1.9
billion unregistered site visitors. As the newest hire on Amazon’s US sales
research team, you’re likely scared to be extracting data from the 10 Petabyte flat
file that Amazon notoriously uses to store all of their sales information - but
fear not! The new database administrator Michael Seaman is in the process of
developing a database application to solve all your data needs and make all your
queries incomparably faster.

#### Details
The Amazon Sales Database Application will be an easy to use web applet
communicating with a MySQL database hosted on Microsoft’s Azure cloud. Because it
will be a web application, the UI will be scripted primarily in JavaScript with
windows designed in HTML/CSS.

The backend database will have tables keeping track of all listed items,
warehouses, which warehouses ship where, and the stock for each warehouse.
Additionally, separate tables will be kept for each customer with a registered
account and for their possibly multiple shipping addresses. Finally, a table
containing all transaction history in the US will be accessible.

A casual user will be able to print out and search the tables listed above, as well
as create, delete, and update records. In addition to in-app functionality, the
application will be able to export reports of the national most/least popular
items, the most/least popular items by state, and the customers that generate the
most revenue.

---
### Schema:

![Alt text](/inClassPresentation/finalProjectSchema.png?raw=true "Amazon Database Schema")

 - Indexes were placed on columns most likely to fill up and be searched the most

---

### Known Bugs:
* Update by Name menu displays 'Name' twice
* Modals for Create, Update and Delete do not completely encapsulate their contents.
* Need to remove 'ExtraData' attribute

### Overview:
The	UI	can	be	developed	in	the	framework	of	your	choosing	(i.e.	web,	.net,
java),	however	the	backend	database	must	obviously	be	MySQL.

The	final	project	must incorporate at a	minimum	the	following	requirements:

- [x]  Print	records	from	your	database/tables.
- [x]  Search	for	results	by	various	criteria	given	a	specific	identifier
- [x]  Create	a	new	record
- [x]  Delete	records	(soft	delete	function	would	be	ideal)
- [x]  Update	records
- [ ]  Make	use	of	transactions	(commit	&	rollback)
- [x]  Generate	reports	that	can	be	exported	(excel	or	csv	format)
  * One	query	must perform an aggregation	using	a	group-by clause
  * One	query	must be	implemented	with	a	prepared	statement (if	developing in	Java)
  * One	query	must	contain	a	sub-query.
  * Two	queries	must	involve	joins	across	at	least	3	tables
- [x]  Enforce	referential	integrality (Constraints)
- [x]  Include	Database	Views,	Indexes

---
## Honor Pledge

I pledge that all the work in this repository is my own!


Signed,

Michael Seaman
