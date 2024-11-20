# Hi, I'm KyuuRzy 👋🏼

<div style="display: flex; align-items: flex-start; gap: 20px; margin-bottom: 20px;">
  <img src="https://pomf2.lain.la/f/zp8as3kp.jpg" alt="Song Image" width="200" style="border-radius: 50px;">
  <div>
    <h2>🎵 Line Without a Hook - Ricky Montgomery</h2>
    <p>"Oh, baby, I am a wreck when I'm without you<br>
    I need you here to stay"</p>
    <p><i>A poignant indie pop song capturing the essence of emotional dependency and vulnerability in love.</i></p>
  </div>
</div>

## 🧑‍💻 Self-Introduction

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
