# Class Diagram

Class diagram offers a bird's eye view of the structural and static components of the entire system. And at the same time it represents a blueprint of the code, being a very near view of the code of the system.

It describes the classes of application being modeled along with their relationships. It’s a powerful tool that can help gain a comprehensive understanding of an application's inner workings, whether focused on a specific subset of classes or an entire class system.

## Fundamental Concepts

Class diagram fundamental concepts are:

- [Class](#class)
- [Visibility](#visibility)
- [Relationships](#relationships)
- Multiplicity

### Class

Classes are building blocks of the class diagram. They represent objects or entities\* in the system and define their attributes and behaviors.

_\*Classes refer as entities in software lingo._

Class can be identified by 3 compartments:

1. Class name - first box in class diagram.
2. Attributes (properties or characteristics of a class) - they take the second box in the class diagram.
3. Methods (actions that a class can perform, e.g. updating an attribute) - third compartment of a class box.

Here is a sample visual notation of an Employee class along with class code:

[Class diagram example](https://ntonbala.github.io/uml-diagrams/Structural/Class/img/class-concept.drawio.html)

```
class Employee {
  private _firstName: string;
  private _lastName: string;

  calculateSalary(): void {}
  getAddress(): void {}
}
```

### Visibility

Every _class member_ (attributes and methods) has a specific visibility assigned to it. To represent it in UML next notations are used:

- _public_ attributes and methods are represented with the plus sign (**+**). They are accessible anywhere in the program.
- _private_ attributes and methods are represented with minus or negative sign (**-**), and those are accessible in the class that defines them.
- _protected_ attributes and methods are represented with hash symbol (**#**) and they are accessible in the class that defines them and a subclass of that class.
- _package level_ attributes and methods are represented with the tilde symbol (**~**), and these members are accessible in the instances of the other classes within the same package.

### Relationships

There can be next types of relationships in class diagram:

- [Association](#association)
- [Inheritance](#inheritance)
- [Aggregation](#aggregation)
- [Composition](#composition)
- Realization

#### Association

Association shows how objects of one class interact with the objects of another class and defines the multiplicity of the relationship. This can be one to one, one to many, many to one or many to many relationships.

Relationship associations are depicted as a line connecting two class objects with endpoints that can be labeled to show the multiplicity.

E.g. Student and Course - a student can take multiple courses and a course can be taken by multiple students. So, they are bound with association which represents a many to many relationship: [Association diagram example](https://ntonbala.github.io/uml-diagrams/Structural/Class/img/relationships-concept-association.drawio.html).

#### Inheritance

Inheritance represents hierarchical relationships between classes, whereas a subclass inherits attributes and methods from its parent class and may add or override some of its own attributes and behavior.

This relationship is represented by an arrow, pointing from the subclass to the superclass with a field triangle as an arrowhead. E.g. a _Dog_ is a specific form of _Animal_ and inherits characteristics from _Animal_ class: [Inheritance diagram example](https://ntonbala.github.io/uml-diagrams/Structural/Class/img/relationships-concept-inheritance.drawio.html).

#### Aggregation

This is a type of association that represents a whole-part relationship between two classes. Aggregation indicates that an object of one class contains the object of another class.

In this [Aggregation diagram example](https://ntonbala.github.io/uml-diagrams/Structural/Class/img/relationships-concept-aggregation-1.drawio.html), the _Part_ class has its own lifecycle and it can exist independently of the _WholeClass_,

Aggregation can be thought of as a has a or a is part of a relationship.

Let's consider a real-world example of a _Wallet_ and _Money_: [Wallet-Money aggregation diagram example](https://ntonbala.github.io/uml-diagrams/Structural/Class/img/wallet-money.drawio.html). A wallet has money, but money does not necessarily need to have a wallet. So it's a one directional relationship and money can exist without a wallet as well.

Another real-world example is Car and Wheel. A car can not move without a wheel, but the wheel can be independently used with the bike scooter cycle or other vehicles: [Car-Wheel aggregation diagram example](https://ntonbala.github.io/uml-diagrams/Structural/Class/img/car-wheel.drawio.html). The Wheel object can exist without a Car object, which proves to be an aggregation relationship.

_Aggregation relationship_ is represented with the line joining the whole and part class with a hollow diamond pointing to the whole class.

#### Composition

_Composition_ type of relationship is a special type of aggregation that represents a strong whole part relationship between two classes. In composition relationship, the _Part class_ has a much tighter coupling with the _Whole class_ and it can not exist independently of the _Whole class_.

E.g. a human needs a heart to live and the heart needs a human body to function - both can not exist independently of each other, so they are tightly coupled: [Human-Heart composition diagram example](https://ntonbala.github.io/uml-diagrams/Structural/Class/img/human-heart.drawio.html).
