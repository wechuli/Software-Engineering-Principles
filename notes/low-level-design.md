# Low-Level Design

High-level design paints an application's structure in broad strokes. It identifies the system's general environment(hardware, operating system, network and so on) and architecture(such as monolithic, client/server and service-oriented). It identifies the system's major components such as reporting modules, databases and top-level classes. It should also sketch out how the pieces of the system will interact.

Low-level design fills in some of the gaps to provide extra detail that's necessary before developers can start writing code. It gives more specific guidance for how the parts of the system will work and how they will work together. It refines the definitions of the database, the major classes, and the internal and external interfaces.

High-level design focuses on what. Low-level design begins to focus on how. The border between high-level and low-level design is ofen rather fuzzy. In a way, you can describe low‐level design as high‐level design for micro‐managers. You extend the high‐level design by providing more and more detail until everything is specifi ed precisely enough to
start implementation.

## OO Design

The high-level design should have identified the major types of classes that the application will use. Now it's time to refine that design to identify the specific classes that the program will need. The new classes should include definitions of the properties, methods, and events they will provide for the application to use.

### Identifying Classes

One way to pick classes is to look for nouns in a description of the application's features. When you're studying possible classes, think about what sorts of information the class needs(properties), what sorts of things it needs to do(methods), and whether it needs to notify the program of changing circumstances(events).

### Building Inheritence Hierarchies

After you define the application's main classes, you need to add more detail to represent variations of those classes. You can capture the differences between related classes by deriving a child class from a parent class. Child classes automatically inherit the properties, methods and events defined by the pareent class.

This is one important way object-oriented programming languages achieve code resuse. You write code once in the parent class and any child classes use that same code without you rewriting it.

Because an instance of a child class also belongs to the parent class, the program should be able to treat the object as if it were of the parent class if that would be helpful.In this example, that means a program should be able to treat a Corvette object as either a Corvette or as a more generic Car . For instance, t r he program could create an array of Car objects and fi ll it with instances of the Corvette , Yaris , VolkswagenBeatle , or DeLorean classes. The program should be able to treat all those objects as if they were Car s without knowing their true classes. The capability to treat objects as if they were actually from a different class is called polymorphism .

Conversely, most object-oriented programming languages do not allow multiple inheritence, so a class can have at most a single parent class. Because classes can have at most one parent but any number of children, the realtionship between classes for a tree-like inheritence hierarchy.

There are a lot of ways you can modify basic inheritence relationships. For example, a child class can add properties, methods and events(which together are called memebers) that are not available in the parent class. A child can also replace a parent class member with a new version.

### Refinement

Refinement is the process of breaking a parent class into multiple subclasses to capture some difference between objects in the class. One danger to refinement is overrefinement, which happens when you refine a class hierarchy unnecessarily, making too many classes that make programming more complicated and confusing. Even if the program cares about certain differences between objects, that doesn't mean those differences would make a good inheritence hierarchy.

The second problem with this hierarchy is that the differences between the classes could easily be represented by properties instead of by different classes. You can avoid these kinds of hierarchy problems if you focus on behavioral differences between the different kinds of objects instead of looking at differences in properties.

### Generalization

Refinement starts with a single class and creates child classes to represent differences between objects. Generalization does the opposite: It starts with several classes and creates a parent for them to represent common features.

Just as you can go overboard with refinement to build an inheritence hierarchy, you can also get carried away with generalization.

### Hierarchy Warning Signs

The following list gives some questions you can ask yourself when trying to decide if you have an effective inheritence hierarchy.

- Is it tall and thin? In general, tall, thin inheritence hierarchies are more confusing than shorter ones . Tall hierarchies make it hard for developers to remember which class to use under different circumstances. How tall an inheritence hierarchy can be depends on your application but if it contains more than three or fours levels, you should make sure you really need them all.
- Do you have a huge number of classes? If you have more than a dozen or so classes, se if you can replace some with simple properties.
- Does a class have only a single subclass? If so, then you can probably remove it and move whatever it was trying to represent into the subclass.
- Is there a class at the bottom of the hierarchy that is never instantiated? If so, you probably don't need it.
- Do the classes all make common sense?
- Do classes represent differences in a property's value rather than in behavior or the presence of properties?

### Object Composition

Inheritence is one way you can reuse code. A child class inherits all of the code defined by its parent class, so you don't need to write it again. Another way to reuse code is _object composition_, a technique that uses existing classes to build more complex classes.

For example, suppose you define a `Person` class that has `FirstName`, `LastName`,`Address` and `Phone` properties. Now you want to make a `Company` class that should include information about a contact person.

You could make the `Company` class inherit from the `Person` class so it would inherit the `FirstName`,`LastName`,`Address`, and `Phone` properties. That would give you places to store the contact person's information but it doesn't make intuitive sense. A company is not a kind of person, so `Company` should not inherit from Person.

A better approach is to give the `Company` class a new property of type `Person` called `ContactPerson`. Now the `Company` class gets the benefit of the code defined by the `Person` class without the illogic and possible consfusion of inheriting from `Person`.

This approach also lets you place more than one `Person` object inside the Company class. For example, if you decide the `Company` class also needs to store information about a billing contact and a shipping contact, you can add more `Person` objects to the class. You couldn’t do that with inheritance.


## Database Design

There are many different kinds od databases that you can use to build an application. The most popular being relational.
Relational database are simple,easy to use and provide a good set of tools for searching, combining data from different tables, sorting results and otherwise rearranging data.

A relational database stores related data in tables. Each table holds records that contain pieces of data that are related. The pieces of data in each record are called fields. Each field has a name and a data type. All the values in different records for a particular field have the data type.

One particular usefule kind of relationship is a foreign key relationship. A foreign key is a set of one or more fields in one table with values that uniquely define a record in another table.

The table containing the foreign key is often called the child table, and the table that contains the uniquely identified record is often called the parent table.

A *lookup* table is a table that contains values just to use as foreign keys. In addition to validating user inputs, lookup tables allow the users to configure the application.

Building a relational database is easy, but unless you design the database properly, you may encounter unexpected problems. Those problems may be that:
- Duplicate data can watse space and make updating values slow
- You may be unable to delete one piece of data without also deleting another unrelated piece of data
- An otherwise unnecessary piece of data may need to exists so that you can represent some other data.
- The database may not allow multiple values when you need them.

These kind of problems are known as anomalies.

Database normalization is a process of rearranginng a database to put it into a standard(normal) form that prevents these kinds of anomalies

### First Normal Form
*First normal form(1NF)* basically says the table can be placed meaninglfully in a relational database. It means the table has a sensible, down-to-earth structure.

Relational database products tend to enforce most of the 1NF rules automatically, so if you don't do anything too weird, your database will be in 1NF with little extra work.

The official requirements for a table to be in 1NF are:
1. Each column must have a unique name
2. The order of the rows and columns doesn't matter
3. each column must have a single data type
4. No two rows can contain identical values
5. Each column must contain a single value
6. Columns cannot contain repeating groups-That means that you can't have two columns that represent the same thing. This means a bit more than two columns don't have the same data type. Tables often have mutliple columns with the same data types but with different meanings.

In general, adding a number to field names to differentiate them is a bad idea. If the program doesn't need to differentiate between the two values, then adding a number to their names just creates a repeating group.

The way to fix this problem is to pull the repeated data out into a new table.

### Second Normal Form
