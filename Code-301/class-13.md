# Class 13

## More CRUD

### CRUD Basics

CRUD is an acronym that stands for Create, Read, Update, and Delete. It's a simple concept that represents the four basic elements of the HTTP avatar. They are the four basic operations you can do on any data.

- Create: Creating data. Once created, a POST request is sent to store the data in the database.
- Read: Read data. A GET request is made in order to get the data to read.
- Update: Update data. A PUT or PATCH request is made to update the data.
  - Requires an id in the route to target specific data.
- Delete: Delete data. A DELETE request is made to remove the target data from the database.
  - Requires an id in the route to target specific data.

### Speed-running a CRUD API

1. Use an express app starter kit.
2. Create module.
3. Require express/ create express.Router()l;
4. Add in CRUD
    1. Get one
    2. Get all
    3. Create one
    4. Update one
    5. Delete one
5. Export module.
6. Scream when npm run dev doesn't work.
7. Check ports and change .env file.
8. Use extension or page to test all routes.
9. Have 13 minutes left.
10. Do some math.
11. Install monk or mongoose to talk to mongoDb (database), and joy (schema validation).
12. Add Mongo URI to .env
13. Require monk, link db.
14. Update GET to await .find.
15. Add schema. Specify what data types will be handled through this schema.
16. Update POST. Validate data through schema that comes from req.body.
17. Test schema.
18. Update GET one. Find by id and await .findOne().
19. Make sure to handle errors and make await functions async.
20. Update PUT. Validate req.body through schema, findOne and check if exists, then update.
21. Scream when you realize there's only 18 seconds left.
22. Update DELETE. Find by id and await .findOne().
23. Be over time and say good enough.
24. Claim you made a CRUD API in 'about' 20 minutes.

Amazing.

## Things I want to know more about
