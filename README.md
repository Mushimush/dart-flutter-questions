# Dart & Flutter Questions

A collection of Dart and Flutter questions to test your knowledge. From basic syntax to tricky edge cases!

---

###### 1. What's the output?

```dart
void main() {
  String s = "Mediterranean Sea";
  int pos = s.indexOf('r');
  print(s.substring(pos - 2, pos + 3));
}
```

- A: `terra`
- B: `iterr`
- C: `diter`
- D: `error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

Let's break it down:
- `s = "Mediterranean Sea"` (indices: M=0, e=1, d=2, i=3, t=4, e=5, r=6, r=7, a=8, n=9, e=10, a=11, n=12...)
- `s.indexOf('r')` returns `6` (the first 'r')
- `pos - 2` = `6 - 2` = `4`
- `pos + 3` = `6 + 3` = `9`
- `substring(4, 9)` extracts indices 4, 5, 6, 7, 8
- Characters: `i`, `t`, `e`, `r`, `r`

Result: `iterr`

</p>
</details>

---

###### 2. What's the output?

```dart
void main() {
  String text = "Flutter is awesome";
  print(text.substring(text.indexOf('is') - 1));
}
```

- A: `is awesome`
- B: ` is awesome`
- C: `r is awesome`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

- `text.indexOf('is')` returns `8` (position of "is")
- `8 - 1` = `7`
- `substring(7)` with one argument extracts from index 7 to the end
- Character at index 7 is a space: `" is awesome"`

The output includes the leading space!

</p>
</details>

---

###### 3. What's the output?

```dart
void main() {
  String s = "DartLang";
  print(s.substring(0, s.indexOf('L')));
}
```

- A: `Dart`
- B: `DartL`
- C: `DartLang`
- D: `L`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

- `s.indexOf('L')` returns `4`
- `s.substring(0, 4)` extracts characters from index 0 to 3
- Characters: `D`, `a`, `r`, `t`

Result: `Dart`

</p>
</details>

---

###### 4. What's the output?

```dart
void main() {
  String word = "programming";
  int start = word.indexOf('gram');
  print(word.substring(start, start + 4));
}
```

- A: `prog`
- B: `gram`
- C: `ramm`
- D: `ammi`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

- `word.indexOf('gram')` returns `3` (where "gram" starts in "pro**gram**ming")
- `start = 3`
- `substring(3, 7)` extracts characters at indices 3, 4, 5, 6
- Characters: `g`, `r`, `a`, `m`

Result: `gram`

</p>
</details>

---

###### 5. What's the output?

```dart
void main() {
  String s = "abcdefghij";
  print(s.substring(s.length - 3));
}
```

- A: `abc`
- B: `hij`
- C: `ghi`
- D: `ij`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

- `s.length` = `10`
- `s.length - 3` = `7`
- `substring(7)` extracts from index 7 to the end
- Characters at indices 7, 8, 9: `h`, `i`, `j`

Result: `hij`

</p>
</details>

---

###### 6. What's the output?

```dart
void main() {
  String text = "Hello World";
  int pos = text.indexOf('o');
  print(text.substring(pos, text.lastIndexOf('o') + 1));
}
```

- A: `o Wo`
- B: `o Wor`
- C: `o Worl`
- D: `o World`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

- `text.indexOf('o')` returns `4` (first 'o' in "Hell**o**")
- `text.lastIndexOf('o')` returns `7` (last 'o' in "W**o**rld")
- `substring(4, 8)` extracts indices 4, 5, 6, 7
- Characters: `o`, ` `, `W`, `o`

Result: `o Wo`

</p>
</details>

---

###### 7. What's the output?

```dart
void main() {
  String s = "ABCABC";
  print(s.substring(s.indexOf('B'), s.lastIndexOf('B') + 1));
}
```

- A: `B`
- B: `BCA`
- C: `BCAB`
- D: `CAB`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

- `s.indexOf('B')` returns `1` (first B)
- `s.lastIndexOf('B')` returns `4` (last B)
- `s.lastIndexOf('B') + 1` = `5`
- `substring(1, 5)` extracts indices 1, 2, 3, 4
- Characters: `B`, `C`, `A`, `B`

Result: `BCAB`

</p>
</details>

---

###### 8. What's the output?

```dart
void main() {
  String code = "A1B2C3D4";
  print(code.substring(code.indexOf('2') + 1, code.indexOf('4')));
}
```

- A: `C3`
- B: `C3D`
- C: `B2C3`
- D: `2C3D`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

- `code.indexOf('2')` returns `3`
- `code.indexOf('2') + 1` = `4`
- `code.indexOf('4')` returns `7`
- `substring(4, 7)` extracts indices 4, 5, 6
- Characters: `C`, `3`, `D`

Result: `C3D`

</p>
</details>

---

###### 9. What's the output?

```dart
void main() {
  String s = "racecar";
  int mid = s.length ~/ 2;
  print(s.substring(0, mid) + s.substring(mid + 1));
}
```

- A: `racecar`
- B: `raccar`
- C: `racear`
- D: `acecar`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

- `s.length` = `7`
- `mid = 7 ~/ 2` = `3`
- `s.substring(0, 3)` = `rac`
- `s.substring(4)` = `car`
- Concatenated: `rac` + `car` = `raccar`

This removes the middle character 'e' at index 3!

</p>
</details>

---

###### 10. What's the output?

```dart
void main() {
  String text = "one two three";
  int first = text.indexOf(' ');
  int second = text.indexOf(' ', first + 1);
  print(text.substring(first + 1, second));
}
```

- A: `one`
- B: `two`
- C: ` two`
- D: `two `

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

- `text.indexOf(' ')` returns `3` (first space)
- `text.indexOf(' ', first + 1)` = `indexOf(' ', 4)` returns `7` (second space, searching from index 4)
- `substring(4, 7)` extracts indices 4, 5, 6
- Characters: `t`, `w`, `o`

Result: `two`

This is a common pattern to extract the second word from a sentence!

</p>
</details>

---

###### 11. What's the output?

```dart
void main() {
  String s = "abcdef";
  print(s.substring(2, 2));
}
```

- A: `c`
- B: `""`  (empty string)
- C: `cd`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

When the start and end indices are the same, `substring()` returns an empty string. There are no characters between index 2 and index 2.

`substring(2, 2)` = `""`

</p>
</details>

---

###### 12. What's the output?

```dart
void main() {
  String email = "user@example.com";
  print(email.substring(0, email.indexOf('@')));
}
```

- A: `user@`
- B: `@example.com`
- C: `user`
- D: `example.com`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

- `email.indexOf('@')` returns `4`
- `substring(0, 4)` extracts indices 0, 1, 2, 3
- Characters: `u`, `s`, `e`, `r`

Result: `user`

This is a common pattern to extract the username from an email address!

</p>
</details>

---

###### 13. What's the output?

```dart
void main() {
  String email = "user@example.com";
  print(email.substring(email.indexOf('@') + 1));
}
```

- A: `user`
- B: `@example.com`
- C: `example.com`
- D: `example`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

- `email.indexOf('@')` returns `4`
- `email.indexOf('@') + 1` = `5`
- `substring(5)` extracts from index 5 to the end

Result: `example.com`

This extracts the domain from an email address!

</p>
</details>

---

###### 14. What's the output?

```dart
void main() {
  String path = "/home/user/documents/file.txt";
  print(path.substring(path.lastIndexOf('/') + 1));
}
```

- A: `/file.txt`
- B: `file.txt`
- C: `file`
- D: `documents/file.txt`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

- `path.lastIndexOf('/')` returns `20` (the last '/')
- `lastIndexOf('/') + 1` = `21`
- `substring(21)` extracts from index 21 to the end

Result: `file.txt`

This is a common pattern to extract the filename from a file path!

</p>
</details>

---

###### 15. What's the output?

```dart
void main() {
  String s = "mississippi";
  int first = s.indexOf('ss');
  int last = s.lastIndexOf('ss');
  print('$first $last');
}
```

- A: `2 2`
- B: `2 5`
- C: `5 5`
- D: `2 6`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

- `s = "mississippi"` (indices: m=0, i=1, s=2, s=3, i=4, s=5, s=6, i=7, p=8, p=9, i=10)
- `s.indexOf('ss')` returns `2` (first "ss" starts at index 2)
- `s.lastIndexOf('ss')` returns `5` (last "ss" starts at index 5)

Result: `2 5`

</p>
</details>

---

###### 16. What's the output?

```dart
void main() {
  String s = "Flutter";
  print(s.substring(s.indexOf('x')));
}
```

- A: `Flutter`
- B: `""`  (empty string)
- C: `Error: RangeError`
- D: `null`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

- `s.indexOf('x')` returns `-1` because 'x' is not found
- `substring(-1)` throws a `RangeError` because -1 is not a valid index

Always check if `indexOf` returns -1 before using it with `substring`!

</p>
</details>

---

###### 17. What's the output?

```dart
void main() {
  String s = "0123456789";
  print(s.substring(3, 3 + 4));
}
```

- A: `3456`
- B: `34567`
- C: `2345`
- D: `456`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

- `substring(3, 7)` extracts indices 3, 4, 5, 6
- In the string "0123456789", characters at those indices are: `3`, `4`, `5`, `6`

Result: `3456`

</p>
</details>

---

###### 18. What's the output?

```dart
void main() {
  String url = "https://dart.dev/guides";
  int start = url.indexOf('://') + 3;
  int end = url.indexOf('/', start);
  print(url.substring(start, end));
}
```

- A: `https`
- B: `dart.dev`
- C: `://dart.dev`
- D: `dart.dev/guides`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

- `url.indexOf('://')` returns `5`
- `start = 5 + 3` = `8`
- `url.indexOf('/', 8)` searches for '/' starting from index 8, returns `16`
- `substring(8, 16)` extracts the characters between indices 8-15

Result: `dart.dev`

This is a common pattern to extract the domain from a URL!

</p>
</details>

---

###### 19. What's the output?

```dart
void main() {
  String s = "abcdefg";
  String reversed = "";
  for (int i = s.length - 1; i >= 0; i--) {
    reversed += s.substring(i, i + 1);
  }
  print(reversed);
}
```

- A: `abcdefg`
- B: `gfedcba`
- C: `fedcba`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

This loop reverses the string by extracting one character at a time from the end:
- `i=6`: `substring(6,7)` = `g`
- `i=5`: `substring(5,6)` = `f`
- `i=4`: `substring(4,5)` = `e`
- ... and so on

Result: `gfedcba`

Note: In real code, you'd use `s.split('').reversed.join()` instead!

</p>
</details>

---

###### 20. What's the output?

```dart
void main() {
  String s = "hello world";
  String result = s.substring(0, 1).toUpperCase() + s.substring(1);
  print(result);
}
```

- A: `Hello World`
- B: `Hello world`
- C: `HELLO WORLD`
- D: `hello world`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

- `s.substring(0, 1)` = `h`
- `.toUpperCase()` = `H`
- `s.substring(1)` = `ello world`
- Concatenated: `H` + `ello world` = `Hello world`

This is a common pattern to capitalize the first letter of a string! Note that only the first letter is capitalized, not the 'w' in 'world'.

</p>
</details>

---

## Quick Reference: String Methods

| Method | Description | Example | Result |
|--------|-------------|---------|--------|
| `substring(start)` | From start to end | `"hello".substring(2)` | `"llo"` |
| `substring(start, end)` | From start to end-1 | `"hello".substring(1, 4)` | `"ell"` |
| `indexOf(str)` | First occurrence | `"hello".indexOf('l')` | `2` |
| `indexOf(str, start)` | First occurrence from start | `"hello".indexOf('l', 3)` | `3` |
| `lastIndexOf(str)` | Last occurrence | `"hello".lastIndexOf('l')` | `3` |
| `length` | String length | `"hello".length` | `5` |

### Key Points

1. **`substring(start, end)`** extracts characters from `start` up to but **NOT including** `end`
2. **`indexOf()` returns `-1`** if the substring is not found
3. **Indices start at 0**, so the first character is at index 0
4. **`substring(n)`** with one argument extracts from index `n` to the end of the string

---

## Contributing

Feel free to submit a PR to add more questions!
