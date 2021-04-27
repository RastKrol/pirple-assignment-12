# pirple-assignment-12
**What is object oriented programming, and why would you use it? As you may already know, many javascript projects are written using a functional, or event-driven design pattern. In which cases would an OOP pattern be a better choice?**
OOP is a way of programming where objects are used to store and modify the data. The advantage of such aproach are:
1)**Encapsulation**. This means that data is generally hidden from other parts of a language.
OOP encapsulates data by default; objects contain both the data and the methods that affect that data, and good OOP practice means you provide getter and setter methods to control access to that data. This protects mutable data from being changed, and makes application data safer. 
2)**Inheritance**. Because objects can be created as instances of other objects, they can inherit variables and methods from those objects. This allows objects to support operations defined by anterior types without having to provide their own definition. The goal is to not repeat yourself—multiple uses of the same code is hard to maintain. But functional programming can also achieve DRY through reusable functions. 
3)**Polymorphism**. Literally, shape-changing, this concept allows one object or method, whether it’s a generic, an interface, or a regular object, to serve as the template for other objects and methods. 
**Example**
{
  function Worker (firstName, lastName, rate, hours) {
    this.firstName = firstName;
    this.lastName = lastName;
    this.rate = rate;
    this.hours = hours;
}
  Worker.prototype.getSalary = function () {
    const salary = this.rate * this.hours;
    console.log(`${this.firstName} ${this.lastName}'s salary in this month is: ${salary}$`);
  }
//Encapsulation

  const worker1 = new Worker("Jimmy", "Doe", 12, 40);
  worker1.getSalary();
//Inheritance

  Worker.prototype.getSalary = function () {
    const fullName = `${this.firstName} ${this.lastName}`;
    const salary = this.rate * this.hours;
    console.log(`${fullName}'s salary in this month is: ${salary}$`);
  }
  //Polymorphism
  
  const worker2 = new Worker("Sally", "Smith", 10, 20);
  worker2.getSalary();
}

In other words OOP allows you to make some kind of generic template and then adopt it for your need, saving a lot of time and making it quite easy to handle data.
I will use it for storing users, products and other data that is just a "Thing".
This way I can always easily modify it and adjust for my needs.
