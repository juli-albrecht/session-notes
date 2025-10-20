# 🟢 JS Basics & Variablen

Variablen speichern Daten, die du später wiederverwenden kannst. Es gibt drei Arten: var, let (änderbar) und const (nicht änderbar).

```js
const name = "Anna";
const name = "Juli"; ❌
name = "Juli"; ❌


let age = 25;
let age = 26; ❌
age = 26  ✅

const city = "Berlin";

console.log(name, age, city);
```

# 🧩 JS Datentypen

JavaScript kennt verschiedene Datentypen, z. B. String, Number, Boolean, Object, Array, undefined, null.

```js
let text = "Hallo"; // String
let number = 42; // Number
let isHappy = true; // Boolean
let nothing = null; // Null
let notDefined; // Undefined
```

# Datentypen kombinieren

```js
const age = 23;
const year = 2025;
// Arithmetic operators: +, -, /, *, %, **
const birthyear = age - year;

// Text concatination:
const message = "You are" + age + "years old";
// Modern alternative:
const message2 = `You are born in ${birthyear}`;

// Logical operators: &&, ||, !
const isTeenager = age < 18 && age >= 13;
const isNotTeenager = age >= 18 || age < 13;
// or
const isNotTeenager2 = !isTeenager;
```

# 🧱 If-Else Statements

- Mit if, else if und else kannst du Bedingungen prüfen und Code abhängig davon ausführen.
- Evaluiert zu true oder false
- Solange false: wird weiter durchgeführt bis true- oder else-Block getroffen wird

```js
let score = 80;

if (score > 90) {
  console.log("Sehr gut!");
} else if (score >= 60) {
  console.log("Bestanden");
} else {
  console.log("Nicht bestanden");
}
```

# 🧮 JS Objects

- Objekte speichern Daten als Schlüssel-Wert-Paare (key-value-pairs).

```js
let person = {
  name: "Anna",
  age: 25,
  city: "Berlin",
};

console.log(person.name);
// Zugriff auf Eigenschaft
person.job = "Designer";
// Neue Eigenschaft hinzufügen
```

# 📦 JS Arrays

- Arrays speichern mehrere Werte in einer geordneten Liste.

```js
const fruits = ["Apfel", "Banane", "Kirsche"];
fruits[0] = "Birne" ✅
const fruits = ["Apfel", "Banane", "Kirsche"]; ❌
fruits = ["Apfel", "Banane", "Kirsche"]; ❌

console.log(fruits[0]); // "Apfel"
fruits.push("Orange"); // Element hinzufügen
fruits.pop(); // Letztes Element entfernen
```

# 🔁 JS Loops

- Schleifen wiederholen Codeblöcke – z. B. um Arrays zu durchlaufen.
- Start: let i wird ausgeführt; Bedingung wird geprüft (Am Anfang: 0 < 5 => true), Code in {} wird ausgeführt; i++ (variable i wird um 1 erhöht), Bedingung wird geprüft (Jetzt: 1 < 5 => true), Code wird ausgeführt, ...
- Sobald i >= 5 ist die Bedingung falsch, und die Schleife wird nicht mehr ausgeführt

```js
// Allgemein:
for (initialization; condition; afterthought) {
  statement;
  statement;
}
// For-Loop
for (let i = 0; i < 5; i++) {
  console.log("Zahl:", i);
}

const fruits = ["Apfel", "Banane", "Kirsche"];

for (let index = 0; index < fruits.length; index++) {
  const fruit = fruits[index];
  console.log(index, fruit);
  // gibt aus :
  // 0, "Apfel"
  // 1, "Banane"
  // 2, "Kirsche"
}

// While-Loop
let index = 0;
while (index < fruits.length) {
  console.log(index, fruits[index]);
  index++;
}

let i = 0;
while (i < 5) {
  console.log("Zahl:", i);
  i++;
}
// For-of-Loop
for (let fruit of fruits) {
  console.log(fruit);
}

// For-in-Loop
const user = {
  name: "Alex",
  age: 28,
  email: "alex@mail.com",
};

for (const key in user) {
  console.log(user[key]);
}

// 'Alex'
// 28
// 'alex@mail.com'
```

# ⚙️ JS Functions

Funktionen bündeln Code, den du mehrfach ausführen kannst.

```js
function greet(name) {
  return "Hallo " + name + "!";
}

console.log(greet("Anna"));

// Arrow Function
const add = (a, b) => a + b;
console.log(add(3, 5));
```

# 🧍‍♀️ JS Inputs & Strings

Mit prompt() kannst du Benutzereingaben abfragen. Strings lassen sich leicht bearbeiten.

```js
let name = prompt("Wie heißt du?");
console.log("Hallo " + name.toUpperCase() + "!");
// In Großbuchstaben
```

# 📝 JS Forms

Formulare kannst du über das DOM ansprechen und auswerten.

```js
<form id="myForm">
  <input id="username" type="text" />
  <button type="submit">Absenden</button>
</form>

<script>
document.getElementById("myForm").addEventListener("submit", function(e) {
  e.preventDefault();
  // verhindert Neuladen
  let user = document.getElementById("username").value;
  console.log("Benutzername:", user);
});
</script>

```

# 🌐 JS DOM & Events

Mit dem DOM greifst du auf HTML-Elemente zu und reagierst auf Ereignisse.

```js
let button = document.querySelector("button");

button.addEventListener("click", () => {
  alert("Button wurde geklickt!");
});
```

# 🧩 HTML hinzufügen und verändern

## InnerHTML

Mit innerHTML kannst du den Inhalt von Elementen ändern oder neue hinzufügen.

```js
let title = document.getElementById("title");
title.innerHTML = "<h2>Willkommen!</h2>";
```

## 🧱 createElement

Mit document.createElement() kannst du neue HTML-Elemente programmatisch erzeugen.

```js
let newDiv = document.createElement("div");
newDiv.textContent = "Ich bin neu hier!";
document.body.appendChild(newDiv);
```

# 🧮 JS Array Methods

## Allgemein

Mit Array-Methoden kannst du Daten filtern, sortieren oder transformieren.

```js
let numbers = [1, 2, 3, 4, 5];

numbers.forEach((n) => console.log(n)); // Ausgabe jedes Elements
let doubled = numbers.map((n) => n * 2); // Neues Array mit verdoppelten Werten
let evens = numbers.filter((n) => n % 2 === 0); // Nur gerade Zahlen
```

## includes

- Die Array-Methode includes() wird verwendet, um zu prüfen, ob ein bestimmtes Element in einem Array enthalten ist.
- includes() gibt true zurück, wenn das gesuchte Element im Array vorhanden ist,
  und false, wenn nicht.

```js
const strings = [
  "HTML",
  "React",
  "CSS",
  "Next.js",
  "MongoDB",
  "styled components",
  "mongoose",
  "next-auth",
  "Visual Studio Code",
];

const includeResult = strings.includes("CSS");
console.log(includeResult);
```

## For Each

- Name the paramter (here: game) ALWAYS in singular
- forEach() ist eine Methode, um über alle Elemente eines Arrays zu iterieren (also sie nacheinander zu durchlaufen) und dabei eine Funktion auf jedes Element auszuführen.

```js
const gamesContainer = document.querySelector("[data-js='games-container']");
const games = [
  {
    id: 1,
    name: "Barbie Horse Adventure",
    publishingYear: 2003,
    devices: ["Xbox", "PS2"],
    description:
      "Barbie rides a horse, while looking for a flock of other horses that managed to get themselves lost.",
  },
  {
    id: 2,
    name: "If It Moves, Shoot It!",
    publishingYear: 1989,
    devices: ["Amiga", "DOS"],
    description:
      "A top-down shooter, in which killing creatures from the depths of the cosmos is far more appealing than asking them to explain the mysteries of pi.",
  },
  {
    id: 3,
    name: "Attack of the Mutant Camels",
    publishingYear: 1983,
    devices: ["Atari"],
    description:
      "A bunch of enormous yellow camels are making their way to your base. Since you're fond of your base, you must massacre them from a plane.",
  },
  {
    id: 4,
    name: "Frogger: Helmet Chaos",
    publishingYear: 2005,
    devices: ["Nintdendo DS", "PSP"],
    description:
      "You play a frog. Stop a bloke destroying your home by jumping around various landscapes. There's some chaos to be had, but disappointingly not in the anatomical region the title so coyly alludes to.",
  },
  {
    id: 5,
    name: "Billy the Wizard: Rocket Broomstick Racing",
    publishingYear: 2007,
    devices: ["Wii", "PC", "PS2"],
    description:
      "It's exactly as it sounds: you're a wizard that races on a fast broomstick. Extraordinary. Where did they get that idea?",
  },
  {
    id: 6,
    name: "Yes Prime Minister",
    publishingYear: 1987,
    devices: ["Commodore 64", "Amstrad CPC", "ZX Spectrum"],
    description:
      "Tie-in game from the popular BBC political comedy of the same name. You play as Prime Minister of the UK for a week.",
  },
  {
    id: 7,
    name: "How To Be A Complete Bastard",
    publishingYear: 1987,
    devices: ["ZX Spectrum", "Commodore 64", "Amstrad CPC"],
    description:
      "Invade a party for rich folks and demonstrate your boyish skills of being a complete and utter git, by for example loosening the screws on the handles of the disabled toilet.",
  },
  {
    id: 8,
    name: "Princess Tomato in Salad Kingdom",
    publishingYear: 1988,
    devices: ["NES"],
    description:
      "As one Sir Cucumber, you must win the hand of Princess Tomato -- daughter of King Broccoli -- by retrieving the stolen royal Turnip Emblem, in this first-person puzzle-solving adventure game.",
  },
  {
    id: 9,
    name: "Ninjabread Man",
    publishingYear: 2005,
    devices: ["PC", "PS2", "Wii"],
    description:
      "It's a ninja again, but this time it's a gingerbread man who needs to save the world from evil pastries. Oh goody.",
  },
  {
    id: 10,
    name: "Extreme Laser Cats From Jupiter",
    publishingYear: 2042,
    devices: ["DOS", "Mac"],
    description:
      "Have you heard of the Extreme Laser Cats From Jupiter? Of course you have! Unfortunately, they have decided to attack earth. The Apocalypse is upon us - and it's very cute.",
  },
];

games.forEach(function (game) {
  const li = document.createElement("li");
  li.textContent = game.name;
  gamesContainer.append(li);
});
```

## Map

- Ein neues Array auf Basis eines bestehenden Arrays erzeugen oder transformieren
- map() durchläuft jedes Element eines Arrays und führt eine Funktion darauf aus.
  Das Ergebnis dieser Funktion wird in ein neues Array geschrieben.

```js
const upperCaseStrings = strings.map(function (string) {
  return string.toUpperCase();
});

console.log(upperCaseStrings);

const firstLetters = upperCaseStrings.map(function (string) {
  return string[0];
});

console.log(firstLetters);

const publishingYears = games.map(function (game) {
  return game.publishingYear;
});

console.log(publishingYears);
```

## Filter

- Mit filter() kann man mehrere Elemente aus einem Array auswählen, die eine bestimmte Bedingung erfüllen.
- Das Ergebnis ist immer ein neues Array (auch wenn nur ein Element gefunden wurde).

```js
const longStrings = strings.filter(function (string) {
  const isLongerThan5 = string.length > 5;

  if (isLongerThan5) {
    return true;
    //yes, keep this in the new array
  } else {
    return false;
    //no, skip this element.
  }
});

console.log(longStrings);

// const retroGames = games.filter(function (game) {
//   return game.publishingYear < 2000;
// });

// const retroGames = games.filter((game) => {
//   return game.publishingYear < 2000;
// });

const retroGames = games.filter((game) => game.publishingYear < 2000);

console.log(retroGames);
```

## Find

- Mit find() sucht man das erste Element, das eine Bedingung erfüllt.
- Es gibt nur ein einzelnes Element (oder undefined) zurück – kein Array!

```js
const firstRetroGame = games.find((game) => game.id === 1);

console.log(firstRetroGame);
```

# APIs

- API steht für Application Programming Interface.
  Eine API ist eine Schnittstelle, über die zwei Programme miteinander kommunizieren können.
  👉 Beispiel:
- Du hast eine Wetter-App.
- Diese App ruft über eine Wetter-API Daten vom Wetterdienst ab.
- Der Server schickt als Antwort z. B. ein JSON-Objekt mit Temperatur, Stadt, Luftfeuchtigkeit usw.
  ➡️ Du kannst dir eine API also wie einen Kellner im Restaurant vorstellen:
- Du (Client) bestellst etwas (Request), der Kellner (API) bringt deine Bestellung zur Küche (Server), und liefert dir das Ergebnis zurück (Response).
