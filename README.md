# Hi, I'm KyuuRzy 👋🏼

<img src="https://pomf2.lain.la/f/zp8as3kp.jpg" alt="Banner Image" width="100%" style="border-radius: 10px; margin: 20px 0;">

## 🎵 Featured Song: Line Without a Hook

### Lyrics Translation:
```Oh, baby, I am a wreck when I'm without you``` 

```I need you here to stay```

These lyrics beautifully capture the essence of deep emotional attachment and vulnerability. The singer expresses how incomplete and broken they feel without their loved one, reflecting the universal human experience of profound connection and dependency in love.

## 🧑‍💻 Self-Introduction (in JavaScript)

```javascript
const crypto = require('crypto');

class EnigmaticPerson {
  #secretKey;
  #favoriteQuote = "Among a thousand stars, only one I like";
  
  constructor(data) {
    this.#secretKey = crypto.randomBytes(32);
    this.encryptedData = this.#encrypt(JSON.stringify(data));
  }

  #encrypt(text) {
    const iv = crypto.randomBytes(16);
    const cipher = crypto.createCipheriv('aes-256-cbc', this.#secretKey, iv);
    let encrypted = cipher.update(text, 'utf8', 'hex');
    encrypted += cipher.final('hex');
    return iv.toString('hex') + ':' + encrypted;
  }

  #decrypt(text) {
    const [ivHex, encryptedHex] = text.split(':');
    const iv = Buffer.from(ivHex, 'hex');
    const decipher = crypto.createDecipheriv('aes-256-cbc', this.#secretKey, iv);
    let decrypted = decipher.update(encryptedHex, 'hex', 'utf8');
    decrypted += decipher.final('utf8');
    return JSON.parse(decrypted);
  }

  revealIdentity() {
    const data = this.#decrypt(this.encryptedData);
    console.log(`
      🌟 Decrypted Identity 🌟
      Name: ${data.name}
      Age: ${data.age}
      Origin: ${data.origin}
      Hobbies: ${data.hobbies.join(', ')}
      Waifu: ${data.waifu}
      Partner: ${data.partner}
      
      Quote: ${this.#favoriteQuote} ✨
    `);
  }
}

const kyuuRzy = new EnigmaticPerson({
  name: "Ikyy",
  age: 18,
  origin: "makassar",
  hobbies: ["Makan Burassa/Pallubasa"],
  waifu: "Gada bjirr",
  partner: "my child's🤍‼️"
});

kyuuRzy.revealIdentity();
