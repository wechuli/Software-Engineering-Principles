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
