## JavaScript Questions Solved

### 1. Write a program to take a string and remove a character as desired by the user

```javascript
const removeCharacter = (inputString, removingCharacter) => {
  const uniqueChar = [];
  let strLength = inputString.length;
  console.log(strLength);

  for (let i = 0; i < strLength; i++) {
    if (inputString[i] !== removingCharacter) {
      uniqueChar.push(inputString[i]);
    }
  }

  console.log(
    `After removing '${removingCharacter}', The final string is '${uniqueChar.join(
      ""
    )}'.`
  );
};

removeCharacter("development", "e");
```

### 2. Write a program to take 10 numbers in an array and count the number of positive, negative numbers and zeros

```javascript
const countPositiveNegativeZero = (arr) => {
  let positive = 0;
  let negative = 0;
  let zero = 0;

  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === 0) zero++;
    else if (arr[i] > 0) positive++;
    else negative++;
  }

  console.log(
    `Positive Count: ${positive}, Negative Count: ${negative} and Zero Count: ${zero}`
  );
};

countPositiveNegativeZero([
  21,
  -25,
  7250,
  0,
  -982,
  0,
  472,
  -87,
  07,
  81284,
  -950,
]);
```

### 3. Write a program to take a string and count the occurence of each character in the string.

```javascript
const occurrenceOfChar = (str) => {
  str = str.toLowerCase();

  const countEach = {};

  const strLength = str.length;

  let getChar, count;

  for (let i = 0; i < strLength; ++i) {
    getChar = str[i];

    count = countEach[getChar];
    countEach[getChar] = count ? count + 1 : 1;
  }

  for (getChar in countEach) {
    if (getChar != " ")
      console.log(`Occurrence of ${getChar} is ${countEach[getChar]}`);
  }
};

occurrenceOfChar("A smooth sea never made a skillful sailor");
```