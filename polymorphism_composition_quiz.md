# Polymorphism & Composition Homework - Quiz

## Polymorphism - Answers;

Q1. What does the ___word___ 'polymorphism' mean?
 - The term comes from Greek etimology 'Ploymorpho (πολύμορφο)' meaning multiform. In coding the term is used to denote an object that can take on many forms.


Q2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.
 - In OOP polymorphism relates to the application and re-use of code to extend functionality.

```bash
public class Wallet implements IScan {
    private String name;
    private ArrayList<IScan> cards;

    public Wallet(String name) {
        this.name = name;
        this.cards = new ArrayList();
    }

    public String getName() {
        return this.name;
    }

    public int getNumberOfItems() {
        return this.cards.size();
    }

    public String scan(String data) {
        return null;
    }

    public void addItem(IScan card) {
        this.cards.add(card);
    }
}
```

Q3. What can we use to implement polymorphism in Java?
 - Through implementation of intefaces and abstract classes.

Q4. How many 'forms' can an object take when using polymorphism?

 -  2; Static and Dynamic. Method overloading and method overriding respectively.

Q5. Give an example of when you could use polymorphism.

```bash
public class Desktop implements IConnect {
    private String name;
    private String make;
    private String model;

    public Desktop(String name, String make, String model) {
        this.name = name;
        this.make = make;
        this.model = model;
    }

    public String getName() {
        return name;
    }

    public String getMake() {
        return make;
    }

    public String getModel() {
        return model;
    }

    public String connect(String data) {
        return "connecting to network: " + data;
    }
}

```

## Composition and Aggregation - Answers:

Q6. What do we mean by 'composition' in reference to object-oriented programming?

 - It describes a class that one or more objects references. It is the deepest/strongest form of encapsulation.

Q7. When would you use composition? Provide a simple example in Java.

- To associate the relationship between a car and its engine.

``` bash
public class Car {

    private Engine engine;  
       
    public Car(){
       engine  = new Engine();
    }
}

class Engine {
    private String type;
}
```

Q8. Give a difference between composition and aggregation?

- Composition owns objects and relationships within, Aggregation uses objects and can contain sub-part objects without main objects.

Q9. What is/are the advantage(s) of using composition/aggregation?
 - Efficient code re-use without havening to directly use inheritance and make encapsulation of code easier to maintain.

Q10. When using composition, when an object is destroyed, what happens to all the objects it is composed of?
- The objects are destroyed as well.

Q11. When using aggregation, when an object is destroyed, what happens to all the objects it is composed of?
 - The objects can be destroyed independently.