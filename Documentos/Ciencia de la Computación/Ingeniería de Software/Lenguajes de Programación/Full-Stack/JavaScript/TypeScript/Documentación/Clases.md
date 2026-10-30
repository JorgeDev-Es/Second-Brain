Una clase puede cumplir una interfaz sin necesidad de la clausula `implements` explícita:
```TypeScript
interface Person {
  firstName: string;
  lastName: string;
}

class Student {
  fullName: string;
  constructor(
    public firstName: string,
    public middleInitial: string,
    public lastName: string,
  ) {
    this.fullName = firstName + " " + middleInitial + " " + lastName;
  }
}

function greeter(person: Person) {
  return "Hello, " + person.firstName + " " + person.lastName;
}

const user = new Student("Jane", "M.", "user");

console.log(greeter(user));
```