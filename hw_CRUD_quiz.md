# CRUD Quiz

Use the solution to this afternoon's Property Tracker lab to answer the following questions. Please write your answers under each question, push the file to GitHub, and submit in the usual way.

## MVP Questions

In our Property Tracker application:

Q1. Where are we instantiating instances of the `Property` class?
```
in console.rb file the property.new is called which uses this. this also happens in property.rb file with the methods .find, .all, .find_by_address.

```

Q2. Where are we defining the SQL that enables us to save the ruby `Property` object into the database?
```
this is defined in the save method.
```

Q3. In `console.rb`, which lines modify the database?

```
delete_all at 4, in lines 13, 22, 31 in save, and in 33 with delete
```

Q4. Why do we not define the id of a `Property` object at the point we instantiate it (‘new it up’)?

Q5. Where and how do we assign the id (that is generated by the database) to the ruby `Property` object?

```
@id = db.exec_prepared("save", values)[0]["id"].to_i
```

Q6. Why do we put a guard (an `if` clause) on the `@id` attribute in the constructor?

Q7. Why are some of the CRUD actions represented by instance methods, and others by class methods?

Q8. What type of data structure is returned by calls to `db.exec_prepared()`? In the `save` method, how do we access the id from the returned data structure?

Q9. Why do we use prepared statements when performing database operations?

```
SQL injection attacks can happen so this is used to sanitise input and defend against an attack
```

## Extension Questions

Look at the `find_by_id` and `find_by_address` methods in the `Property` class.

Q10. What do they take in as their arguments?

Q11. What are their return values?
