# Hi, I'm KyuuRzy 👋🏼

```javascript
class Person {
  #quote = "Among a thousand stars, only one I like ✨";

  constructor(info) {
    Object.assign(this, info);
  }

  introduce() {
    return `
      Name: ${this.name}
      Age: ${this.age}
      Origin: ${this.origin}
      Hobbies: ${this.hobbies}
      Waifu: ${this.waifu}
      Partner: ${this.partner}
      Quote: ${this.#quote}
    `;
  }
}

const kyuuRzy = new Person({
  name: "Ikyy",
  age: 18,
  origin: "Makassar",
  hobbies: "Makan Burassa/Pallubasa",
  waifu: "Gada bjirr",
  partner: "my child's🤍‼️"
});

console.log(kyuuRzy.introduce());
