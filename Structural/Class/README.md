# Class Diagram

Class diagram offers a bird's eye view of the structural and static components of the entire system. And at the same time it represents a blueprint of the code, being a very near view of the code of the system.

It describes the classes of application being modeled along with their relationships. It’s a powerful tool that can help gain a comprehensive understanding of an application's inner workings, whether focused on a specific subset of classes or an entire class system.

## Fundamental Concepts

Class diagram fundamental concepts are:

- Class
- Visibility
- Relationships
- Multiplicity

### Class

Classes are building blocks of the class diagram. They represent objects or entities\* in the system and define their attributes and behaviors.

\* Classes refer as entities in software lingo.

Class can be identified by 3 compartments:

1. Class name - first box in class diagram.
2. Attributes (properties or characteristics of a class) - they take the second box in the class diagram.
3. Methods (actions that a class can perform, e.g. updating an attribute) - third compartment of a class box.

Here is a sample visual notation of an Employee class along with class code: [Class diagram](./img/class-concept.drawio.html),

```
class Employee {
  private _firstName: string;
  private _lastName: string;

  calculateSalary(): void {}
  getAddress(): void {}
}
```

### Visibility

Every class member (attributes and methods) has a specific visibility assigned to it. To represent it in UML next notations are used:

- Public attributes and methods are represented with the plus sign (+). They are accessible anywhere in the program.
- Private attributes and methods are represented with minus or negative sign (-), and those are accessible in the class that defines them.
- Protected attributes and methods are represented with hash symbol (#) and they are accessible in the class that defines them and a subclass of that class.
- Package level attributes and methods are represented with the tilde symbol (~), and these members are accessible in the instances of the other classes within the same package.

### Relationships

There can be next types of relationships in class diagram:

- Association
- Inheritance
- Aggregation
- Composition
- Realization
