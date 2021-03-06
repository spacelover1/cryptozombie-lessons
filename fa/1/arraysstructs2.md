---
title: ساختارها و آرایه‌ها
actions: ['پاسخ', 'راهنمایی']
material:
  editor:
    language: sol
    startingCode: |
      pragma solidity ^0.4.25;

      contract ZombieFactory {

          uint dnaDigits = 16;
          uint dnaModulus = 10 ** dnaDigits;

          struct Zombie {
              string name;
              uint dna;
          }

          Zombie[] public zombies;

          function createZombie (string _name, uint _dna) {
              // start here
          }

      }
    answer: >
      pragma solidity ^0.4.25;


      contract ZombieFactory {

          uint dnaDigits = 16;
          uint dnaModulus = 10 ** dnaDigits;

          struct Zombie {
              string name;
              uint dna;
          }

          Zombie[] public zombies;

          function createZombie (string _name, uint _dna) {
              zombies.push(Zombie(_name, _dna));
          }

      }
---
<div dir="rtl">     
### ایجاد ساختار جدید

ساختار `Person` از مثال قبل رو یادتونه؟

```
struct Person {
  uint age;
  string name;
}

Person[] public people;
```

حالا می‌خوایم یاد بگیریم چطوری `Person`های جدید بسازیم و اونا رو به آرایه `people` (مردم) اضافه کنیم.

```
// create a New Person:
Person satoshi = Person(172, "Satoshi");

// Add that person to the Array:
people.push(satoshi);
```

همچنین می‌تونیم این دو مرحله رو با هم تو یه خط کد بنویسیم تا کدمون تمیزتر باشه:

```
people.push(Person(16, "Vitalik"));
```

توجه کنین که `array.push()` عنصر جدید رو به **انتها**ی آرایه اضافه می‌کنه، پس عناصر به ترتیبی که اضافه شدند در آرایه ذخیره می‌شن. مثال زیر رو ببینین:

```
uint[] numbers;
numbers.push(5);
numbers.push(10);
numbers.push(15);
// numbers is now equal to [5, 10, 15]
```

# دست به کد شو

بیاین کدی بنویسیم که تابع createZombie کاری انجام بده!


۱.داخل تابع یه زامبی جدید با عنوان `Zombie`بسازین و اونو به آرایه`zombies` اضافه کنین. اسم `name` و دی‌ان‌ای `dna` زامبی جدید از آرگومان‌های تابع‌مونه.
۲. بیایین کدمونو تو یه خط بنویسیم تا تمیزتر باشه.
</div>
