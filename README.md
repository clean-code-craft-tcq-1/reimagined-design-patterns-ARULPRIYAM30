# reimagined-design-patterns

Give a summary description of Four design patterns that you choose from the following design patterns: **Adapter,  Builder, Composite, Decorator, Observer, Interpreter, State, Mediator, Memento, Prototype, Proxy**. In your summaries say:

- what kind of problem(s) you can solve with that pattern and when you use it, maybe with a short example
- how the pattern works, what the basic idea of the pattern is
- what the main advantage and what the the main disadvantage is of using this pattern
- Write a short summary for each of the four patterns, about half a page for each pattern (rather less than more). 

> Do not add diagrams, and do not try to give a complete description of the patterns as found in the books. Rather think of how you would explain the essential ideas of these patterns in a few sentences to a colleague while drinking coffee.

#Composite Design Pattern

The **basic idea** is where there is a need to create objects which represent a tree structure. this pattern allows to treat individual object (leaf object) and composite object uniformly (equally). 

**Example :**, An organization have organization represented in a tree structure, suppose, on first level we have General Manager then under this we have 4-6 Sub Managers then under each manager we have several Developers/Technicians/Test. This represents a hierarchy (tree structure).
Here “General Manager” and “Sub Manager” are Composite objects because they have child objects/elements under them and they made by composing two or more objects under them. And Developer object do not have any child under them so these objects are called leaf objects.
As we know that this design pattern allows to treat leaf and composite objects equally hence we can perform one operation to get display their information(General and Sub Managers) and leaf object (Developers). Such approach for considered in Composite Design Patterns.

**Advantage:** No need to take care for concrete object. if we have an operation it applies to all objects down the tree.

**Main disadvantage:** Complexity of making objects and implementing the tree data structure.

**Decorator Design Pattern**
**Basic idea**
It allows user to add new functionality to an existing object without altering its already existing structure. Also called Wrapper Design Pattern and comes under structural design patterns. In simple words it attach additional responsibilities to an object dynamically without altering the existing structure. It act as wrapper as it wraps the original object and allows us to add additional functionality at runtime.

 **Example :** ‘Wearing Clothes’ is a good example to understand this design pattern. So in winters, if you are feeling too cold you simply wrap yourself using a sweater. Even after wearing a sweater you are feeling cold, so you can wrap jacket around you. Now suppose it starts raining so you can put raincoat on. So usually we don’t wear these clothes, if we don’t need them we can easily remove them.
So basically you are wrapping yourself with clothes according to weather requirement similarly decorator design pattern allows to add new functionality at runtime without disturbing the existing structure of the object.It solves the problem to add behavior or state to individual object at runtime. Inheritance is not feasible because it is static and applies to an entire class.
**Advantage:** It is flexible than inheritance because inheritance adds responsibility at compile time but decorator pattern adds at run time.

**Disadvantage:** High complexity of software (especially decorator interface)

**Prototype Design Pattern**
**Basic Idea** is to create a new object from the existing object that means it clone the existing object into a new object with its data in it. It avoids the expensive operation of the creation of a new object. This pattern mostly used when object creation is an expensive operation. It is also a creational design pattern.
By shallow copy & deep copy allows to achieve Prototype or cloning.
**Example:** In the organization we need to build a salary structure according to education degree and from college tier so we have different parameters to define salary structure. Creating separate objects for the individual degree will lead to a lot of object creation which we can avoid using this pattern.

**Advantage**
Eliminates the potential expensive overhead of initializing an object.
Optimizing the code where multiple objects are having similar data.

**Disadvantages**
Difficult to implement in already existing projects as a class must have an implementation of clone() methods.Chances of using different objects internally.

**State Design Pattern**
**Basic Idea** State design pattern allows an object to alter its behaviour when its internal state is changing so in a nutshell it allows an object to change its complete behaviour depending on its internal state.
So if you consider some object and maybe there are 2 states called state A & state B now which operation object is going to perform is completely decided based on the states over here.
**Example:** Consider an employee portal where you have different services like Employee Services Site, HR Service Site, Alumni Portal & Separation Request Site. This visibility of sites are managed via state of employee i.e(Active & InActive). Active employees having access to Employee Service,HR Service and Separation request and InActive Employees are having access to only alumni portal. All these changes are handled on state change when an active user raises a separation request.

**Advantages**
This pattern minimizes the conditional complexity i.e. eliminates the need of if/else or switch cases for objects that have different behaviour requirements.

**Disadvantages**
Lot of code is required depending on how many states a possible object can be and how many state transitions are required.

