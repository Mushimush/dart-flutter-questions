# Dart & Flutter Questions

A collection of Dart and Flutter questions to test your knowledge. From basic syntax to tricky edge cases!

---

###### 1. What's the output?

```dart
void main() {
  var name = 'Flutter';
  print(name);
}
```

- A: `Flutter`
- B: `name`
- C: `var`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

`var name = 'Flutter'` assigns the string `'Flutter'` to the variable `name`. When we call `print(name)`, it outputs the value stored in `name`, which is `Flutter`.

</p>
</details>

---

###### 2. What's the output?

```dart
void main() {
  int x = 10;
  int y = 5;
  print(x + y);
}
```

- A: `10`
- B: `5`
- C: `15`
- D: `xy`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The `+` operator performs arithmetic addition on integers. `x + y` equals `10 + 5`, which is `15`.

</p>
</details>

---

###### 3. What's the output?

```dart
void main() {
  String name = 'John';
  print('Hello $name');
}
```

- A: `Hello $name`
- B: `Hello John`
- C: `Hello name`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `$` symbol is used for string interpolation in Dart. When you write `$name` inside a string, Dart replaces it with the value of the variable `name`. So `'Hello $name'` becomes `'Hello John'`.

</p>
</details>

---

###### 4. What's the output?

```dart
void main() {
  var numbers = [10, 20, 30];
  print(numbers[0]);
}
```

- A: `10`
- B: `20`
- C: `30`
- D: `0`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

List indices in Dart start at 0. So `numbers[0]` returns the first element of the list, which is `10`.

</p>
</details>

---

###### 5. What's the output?

```dart
void main() {
  var fruits = ['apple', 'banana', 'cherry'];
  print(fruits.length);
}
```

- A: `0`
- B: `2`
- C: `3`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The `.length` property returns the number of elements in a list. The list contains 3 elements: `'apple'`, `'banana'`, and `'cherry'`.

</p>
</details>

---

###### 6. What's the output?

```dart
void main() {
  double price = 9.99;
  print(price);
}
```

- A: `9`
- B: `9.99`
- C: `10`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `double` type in Dart preserves decimal values. The value `9.99` is printed as-is.

</p>
</details>

---

###### 7. What's the output?

```dart
void main() {
  bool isActive = true;
  print(isActive);
}
```

- A: `1`
- B: `true`
- C: `True`
- D: `yes`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

Dart prints boolean values as lowercase `true` or `false`. Unlike some languages, it doesn't convert booleans to `1`/`0` or capitalize them.

</p>
</details>

---

###### 8. What's the output?

```dart
void main() {
  var scores = {'John': 90, 'Jane': 85};
  print(scores['John']);
}
```

- A: `John`
- B: `90`
- C: `85`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

This is a Map with String keys and int values. `scores['John']` retrieves the value associated with the key `'John'`, which is `90`.

</p>
</details>

---

###### 9. What should fill the blank to make this code compile?

```dart
void main() {
  ______ PI = 3.14159;
  print(PI);
}
```

- A: `var` only
- B: `final` only
- C: `const` only
- D: `var`, `final`, or `const`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

All three keywords (`var`, `final`, and `const`) can be used to declare a variable with an initial value. They differ in mutability:
- `var`: Can be reassigned
- `final`: Cannot be reassigned (runtime constant)
- `const`: Cannot be reassigned and must be a compile-time constant

</p>
</details>

---

###### 10. What's the output?

```dart
void main() {
  final x = 10;
  x = 20;
  print(x);
}
```

- A: `10`
- B: `20`
- C: `30`
- D: `Error (cannot reassign final)`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

Variables declared with `final` cannot be reassigned after initialization. The line `x = 20` causes a compile-time error because `x` was already assigned the value `10`.

</p>
</details>

---

###### 11. What's the output?

```dart
void main() {
  String? name = null;
  print(name);
}
```

- A: `name`
- B: `null`
- C: `""`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`String?` is a nullable type that can hold either a String value or `null`. When you print a `null` value, Dart outputs the word `null`.

</p>
</details>

---

###### 12. What's the output?

```dart
void main() {
  int age = 25;
  print('Age: ${age + 5}');
}
```

- A: `Age: 25`
- B: `Age: 30`
- C: `Age: ${age + 5}`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

When you use `${}` in string interpolation, Dart evaluates the expression inside the braces. `${age + 5}` evaluates to `25 + 5 = 30`, so the output is `Age: 30`.

</p>
</details>

---

###### 13. What should fill the blank for this to print "Guest"?

```dart
void main() {
  String? name = null;
  print(name ______ 'Guest');
}
```

- A: `+`
- B: `||`
- C: `??`
- D: `?`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The `??` operator is called the null coalescing operator. It returns the left operand if it's not null, otherwise it returns the right operand. Since `name` is `null`, it returns `'Guest'`.

</p>
</details>

---

###### 14. What's the output?

```dart
void main() {
  var list = [1, 2, 3];
  list.add(4);
  print(list);
}
```

- A: `[1, 2, 3]`
- B: `[1, 2, 3, 4]`
- C: `4`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `.add()` method appends an element to the end of the list. After `list.add(4)`, the list becomes `[1, 2, 3, 4]`.

</p>
</details>

---

###### 15. What's the output?

```dart
int double(int x) {
  return x * 2;
}

void main() {
  print(double(5));
}
```

- A: `5`
- B: `10`
- C: `2`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The function `double` takes an integer and returns it multiplied by 2. `double(5)` returns `5 * 2 = 10`.

</p>
</details>

---

###### 16. What's the output?

```dart
void main() {
  var set = {1, 2, 2, 3, 3, 3};
  print(set.length);
}
```

- A: `6`
- B: `3`
- C: `1`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

Sets in Dart only store unique values. Duplicate values are automatically removed. The set `{1, 2, 2, 3, 3, 3}` becomes `{1, 2, 3}`, which has a length of `3`.

</p>
</details>

---

###### 17. What should fill the blanks for the output to be -100?

```dart
void main() {
  __(i)__ x = -10;
  __(ii)__ y;
  y = x;
  const z = 10;
  print(z * y);
}
```

- A: (i) `const` (ii) `final`
- B: (i) `final` (ii) `final`
- C: (i) `const` (ii) `const`
- D: (i) `final` (ii) `const`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

- `x` needs `final` because its value (`-10`) is known at runtime
- `y` needs `final` because it's assigned after declaration (`y = x`)
- `const` variables must be assigned at declaration with compile-time constants
- `z * y = 10 * (-10) = -100`

You can't use `const` for `x` when its value will be assigned to another variable (`y`) that's also used in a computation.

</p>
</details>

---

###### 18. What's the output?

```dart
void main() {
  int a = 7;
  int b = 3;
  print(a ~/ b);
}
```

- A: `2.33`
- B: `2`
- C: `3`
- D: `2.0`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `~/` operator performs integer division in Dart. It divides and truncates the result to an integer. `7 ~/ 3 = 2` (the decimal `.33` is discarded).

</p>
</details>

---

###### 19. What's the output?

```dart
void main() {
  String? text = 'Hello';
  print(text?.length);
}
```

- A: `Hello`
- B: `5`
- C: `null`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `?.` operator is the null-aware access operator. It safely accesses the property if the value is not null. Since `text` is `'Hello'` (not null), `text?.length` returns `5`.

</p>
</details>

---

###### 20. What's the output?

```dart
int multiply(int a, int b) => a * b;

void main() {
  print(multiply(4, 5));
}
```

- A: `4`
- B: `5`
- C: `9`
- D: `20`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

The `=>` syntax is an arrow function (shorthand for single-expression functions). `multiply(4, 5)` returns `4 * 5 = 20`.

</p>
</details>

---

###### 21. What's the output?

```dart
void main() {
  var map = {'a': 1, 'b': 2};
  map['c'] = 3;
  print(map.length);
}
```

- A: `2`
- B: `3`
- C: `4`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The original map has 2 key-value pairs. `map['c'] = 3` adds a new entry with key `'c'` and value `3`. The final length is `3`.

</p>
</details>

---

###### 22. What's the output?

```dart
void main() {
  List<int> numbers = [5, 10, 15];
  numbers.removeAt(1);
  print(numbers);
}
```

- A: `[5, 10, 15]`
- B: `[10, 15]`
- C: `[5, 15]`
- D: `[5, 10]`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The `.removeAt(index)` method removes the element at the specified index. Index `1` is the second element (`10`). After removal, the list is `[5, 15]`.

</p>
</details>

---

###### 23. What's the output?

```dart
void main() {
  String greet(String name) => 'Hello, $name!';
  print(greet('Dart'));
}
```

- A: `Hello, name!`
- B: `Hello, Dart!`
- C: `greet('Dart')`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

This is a local function using arrow syntax with string interpolation. When called with `'Dart'`, the function returns `'Hello, Dart!'`.

</p>
</details>

---

###### 24. What's the output?

```dart
void main() {
  int? value;
  print(value ?? 0);
}
```

- A: `value`
- B: `null`
- C: `0`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

Nullable variables without initialization default to `null`. The `??` operator returns the right operand when the left is null. Since `value` is `null`, it returns `0`.

</p>
</details>

---

###### 25. Which code will cause a runtime error?

**Option A:**
```dart
void main() {
  String? name = null;
  print(name?.length);
}
```

**Option B:**
```dart
void main() {
  String? name = null;
  print(name!.length);
}
```

**Option C:**
```dart
void main() {
  String? name = 'Hello';
  print(name.length);
}
```

**Option D:**
```dart
void main() {
  String name = 'Hello';
  print(name.length);
}
```

- A: Option A
- B: Option B
- C: Option C
- D: Option D

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `!` operator is called the null assertion operator. It tells Dart "I promise this value is not null." But in Option B, `name` IS null, so using `name!.length` causes a runtime error: `Null check operator used on a null value`.

Option A is safe because `?.` returns `null` instead of crashing when the value is null.

</p>
</details>

---

###### 26. What's the output?

```dart
void main() {
  final items = [1, 2, 3];
  items.add(4);
  print(items);
}
```

- A: `[1, 2, 3]`
- B: `[1, 2, 3, 4]`
- C: `Error (cannot modify final)`
- D: `Error (cannot add to list)`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

**This is a common misconception!** `final` prevents reassigning the variable to a new object, but it does NOT prevent modifying the object's contents.

- You CANNOT do: `items = [5, 6, 7]` (reassignment)
- You CAN do: `items.add(4)` (modifying contents)

The list becomes `[1, 2, 3, 4]`.

</p>
</details>

---

###### 27. Which code will NOT compile?

**Option A:**
```dart
void main() {
  final name = 'John';
  print(name);
}
```

**Option B:**
```dart
void main() {
  const items = [1, 2, 3];
  items.add(4);
  print(items);
}
```

**Option C:**
```dart
void main() {
  final items = [1, 2, 3];
  items.add(4);
  print(items);
}
```

**Option D:**
```dart
void main() {
  var items = [1, 2, 3];
  items.add(4);
  print(items);
}
```

- A: Option A
- B: Option B
- C: Option C
- D: Option D

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`const` makes the entire collection immutable - you cannot add, remove, or modify any elements. Attempting to call `.add()` on a `const` list causes a compile-time error.

Compare this to `final` (Option C), which only prevents reassignment but allows content modification.

</p>
</details>

---

###### 28. What's the output?

```dart
void main() {
  String? a = null;
  String? b = null;
  String? c = 'World';
  print(a ?? b ?? c ?? 'Default');
}
```

- A: `null`
- B: `Default`
- C: `World`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

Chained `??` operators evaluate from left to right:
1. `a` is `null`, so check `b`
2. `b` is `null`, so check `c`
3. `c` is `'World'` (not null), so return `'World'`

The chain stops at the first non-null value.

</p>
</details>

---

###### 29. What should fill the blanks for the output to be 25?

```dart
void main() {
  __(i)__ calculate = (int x) => x * x;
  __(ii)__ result = calculate(5);
  print(result);
}
```

- A: (i) `var` (ii) `var`
- B: (i) `final` (ii) `const`
- C: (i) `const` (ii) `final`
- D: (i) `Function` (ii) `int`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

- `calculate` holds a lambda/anonymous function
- `result` holds the return value of `calculate(5)`, which is `25`
- `var` allows type inference for both

Note: `const` won't work for `result` because the function is called at runtime, not compile-time.

</p>
</details>

---

###### 30. What's the output?

```dart
void main() {
  var list = [1, 2, 3, 4, 5];
  print(list.where((x) => x > 2).toList());
}
```

- A: `[1, 2]`
- B: `[3, 4, 5]`
- C: `[2, 3, 4, 5]`
- D: `3`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `.where()` method filters elements based on a condition. It returns an Iterable containing elements that satisfy the predicate `x > 2`.

Elements greater than 2 are: `3, 4, 5`. Converting to a list gives `[3, 4, 5]`.

</p>
</details>

---

###### 31. What's the output?

```dart
void main() {
  int x = 5;
  int y = 3;
  print(x % y);
}
```

- A: `1`
- B: `2`
- C: `1.67`
- D: `0`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `%` operator is the modulo operator, which returns the remainder of division. `5 % 3 = 2` because 5 divided by 3 is 1 with a remainder of 2.

</p>
</details>

---

###### 32. What's the output?

```dart
void main() {
  var nums = [1, 2, 3];
  var doubled = nums.map((n) => n * 2).toList();
  print(doubled[1]);
}
```

- A: `2`
- B: `4`
- C: `6`
- D: `[2, 4, 6]`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `.map()` method transforms each element using the provided function:
- `1 * 2 = 2`
- `2 * 2 = 4`
- `3 * 2 = 6`

So `doubled` is `[2, 4, 6]`. Accessing `doubled[1]` returns the element at index 1, which is `4`.

</p>
</details>

---

###### 33. What's the output?

```dart
void main() {
  var x = 10;
  var y = x++;
  print('$x $y');
}
```

- A: `10 10`
- B: `11 10`
- C: `11 11`
- D: `10 11`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `x++` is a post-increment operator. It returns the current value of `x` (10), then increments `x` to 11.

So `y` gets the value `10`, while `x` becomes `11`. The output is `11 10`.

</p>
</details>

---

###### 34. What's the output?

```dart
void main() {
  var x = 10;
  var y = ++x;
  print('$x $y');
}
```

- A: `10 10`
- B: `11 10`
- C: `11 11`
- D: `10 11`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The `++x` is a pre-increment operator. It increments `x` first (to 11), then returns the new value.

So both `x` and `y` are `11`. The output is `11 11`.

</p>
</details>

---

###### 35. What's the output?

```dart
void main() {
  List<int> numbers = [1, 2, 3];
  numbers[1] = 10;
  print(numbers);
}
```

- A: `[1, 10, 3]`
- B: `[10, 2, 3]`
- C: `[1, 2, 10]`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

`numbers[1] = 10` replaces the element at index 1 (which is `2`) with `10`. The list becomes `[1, 10, 3]`.

</p>
</details>

---

###### 36. What's the output?

```dart
void main() {
  String text = 'Dart';
  print(text.toUpperCase());
}
```

- A: `dart`
- B: `Dart`
- C: `DART`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The `.toUpperCase()` method returns a new string with all characters converted to uppercase. `'Dart'.toUpperCase()` returns `'DART'`.

</p>
</details>

---

###### 37. What's the output?

```dart
void main() {
  var list = [1, 2, 3];
  print(list.reversed.toList());
}
```

- A: `[1, 2, 3]`
- B: `[3, 2, 1]`
- C: `3`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `.reversed` property returns an Iterable with elements in reverse order. Converting to a list gives `[3, 2, 1]`.

</p>
</details>

---

###### 38. What's the output?

```dart
void main() {
  var a = 5;
  var b = 2;
  print(a / b);
}
```

- A: `2`
- B: `2.5`
- C: `2.0`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `/` operator in Dart always returns a `double`, even when dividing integers. `5 / 2 = 2.5`.

If you want integer division, use `~/` instead.

</p>
</details>

---

###### 39. What's the output?

```dart
void main() {
  String? name;
  print(name?.toUpperCase() ?? 'NO NAME');
}
```

- A: `null`
- B: `NO NAME`
- C: `name`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`name` is `null` (uninitialized nullable variable). `name?.toUpperCase()` safely returns `null` because `name` is null. Then `?? 'NO NAME'` provides the fallback value, so the output is `NO NAME`.

</p>
</details>

---

###### 40. What's the output?

```dart
void main() {
  var list = [1, 2, 3, 4, 5];
  print(list.take(3).toList());
}
```

- A: `[1, 2, 3]`
- B: `[3, 4, 5]`
- C: `[1, 2, 3, 4, 5]`
- D: `3`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

The `.take(n)` method returns an Iterable with the first `n` elements. `.take(3)` gets the first 3 elements: `[1, 2, 3]`.

</p>
</details>

---

###### 41. What's the output?

```dart
void main() {
  var list = [1, 2, 3, 4, 5];
  print(list.skip(2).toList());
}
```

- A: `[1, 2]`
- B: `[3, 4, 5]`
- C: `[1, 2, 3]`
- D: `2`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `.skip(n)` method returns an Iterable that skips the first `n` elements. `.skip(2)` skips `1` and `2`, leaving `[3, 4, 5]`.

</p>
</details>

---

###### 42. What's the output?

```dart
void main() {
  var text = 'hello world';
  print(text.split(' ').length);
}
```

- A: `1`
- B: `2`
- C: `11`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `.split(' ')` method splits the string at each space, returning a list: `['hello', 'world']`. The length of this list is `2`.

</p>
</details>

---

###### 43. What's the output?

```dart
void main() {
  var numbers = [3, 1, 4, 1, 5, 9, 2, 6];
  numbers.sort();
  print(numbers.first);
}
```

- A: `3`
- B: `1`
- C: `9`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `.sort()` method sorts the list in ascending order: `[1, 1, 2, 3, 4, 5, 6, 9]`. The `.first` property returns the first element, which is `1`.

</p>
</details>

---

###### 44. What's the output?

```dart
void main() {
  var numbers = [3, 1, 4, 1, 5, 9, 2, 6];
  numbers.sort();
  print(numbers.last);
}
```

- A: `6`
- B: `1`
- C: `9`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

After sorting in ascending order: `[1, 1, 2, 3, 4, 5, 6, 9]`. The `.last` property returns the last element, which is `9`.

</p>
</details>

---

###### 45. What's the output?

```dart
void main() {
  var list = [1, 2, 3];
  print(list.contains(2));
}
```

- A: `true`
- B: `false`
- C: `2`
- D: `1`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

The `.contains()` method checks if an element exists in the list. Since `2` is in the list, it returns `true`.

</p>
</details>

---

###### 46. What's the output?

```dart
void main() {
  var list = [1, 2, 3, 4, 5];
  print(list.reduce((a, b) => a + b));
}
```

- A: `1`
- B: `5`
- C: `15`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The `.reduce()` method combines all elements using the provided function:
- Start: `a=1, b=2` → `3`
- Next: `a=3, b=3` → `6`
- Next: `a=6, b=4` → `10`
- Next: `a=10, b=5` → `15`

The sum of all elements is `15`.

</p>
</details>

---

###### 47. What's the output?

```dart
void main() {
  var text = '  hello  ';
  print('${text.trim()}!');
}
```

- A: `  hello  !`
- B: `hello!`
- C: `hello  !`
- D: `  hello!`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `.trim()` method removes leading and trailing whitespace from a string. `'  hello  '.trim()` returns `'hello'`, so the output is `hello!`.

</p>
</details>

---

###### 48. What's the output?

```dart
void main() {
  var list = [1, 2, 3];
  var copy = [...list, 4, 5];
  print(copy);
}
```

- A: `[1, 2, 3]`
- B: `[[1, 2, 3], 4, 5]`
- C: `[1, 2, 3, 4, 5]`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The `...` (spread operator) unpacks the elements of `list` into the new list. So `[...list, 4, 5]` becomes `[1, 2, 3, 4, 5]`.

</p>
</details>

---

###### 49. What's the output?

```dart
void main() {
  var a = true;
  var b = false;
  print(a && b);
}
```

- A: `true`
- B: `false`
- C: `1`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `&&` operator is logical AND. It returns `true` only if both operands are `true`. Since `b` is `false`, the result is `false`.

</p>
</details>

---

###### 50. What's the output?

```dart
void main() {
  var a = true;
  var b = false;
  print(a || b);
}
```

- A: `true`
- B: `false`
- C: `1`
- D: `Error`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

The `||` operator is logical OR. It returns `true` if at least one operand is `true`. Since `a` is `true`, the result is `true`.

</p>
</details>

---

## Flutter Questions

---

###### 51. What widget should you use to display a simple text on the screen?

- A: `Container`
- B: `Text`
- C: `Label`
- D: `TextView`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

In Flutter, the `Text` widget is used to display text. Unlike Android (which uses `TextView`) or web (which uses labels), Flutter uses `Text`.

```dart
Text('Hello, Flutter!')
```

</p>
</details>

---

###### 52. What's the output?

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(
    MaterialApp(
      home: Scaffold(
        body: Center(
          child: Text('Hello'),
        ),
      ),
    ),
  );
}
```

- A: Error - missing StatelessWidget
- B: A blank screen
- C: "Hello" centered on the screen
- D: Error - runApp requires a Widget class

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

This is a valid minimal Flutter app. `runApp()` accepts any Widget, not just StatelessWidget or StatefulWidget classes. The code displays "Hello" centered on the screen.

</p>
</details>

---

###### 53. Which widget arranges children vertically?

- A: `Row`
- B: `Column`
- C: `Stack`
- D: `Flex`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`Column` arranges its children vertically (top to bottom). `Row` arranges horizontally. `Stack` overlays children on top of each other. `Flex` is the base class for both Row and Column.

</p>
</details>

---

###### 54. Which widget arranges children horizontally?

- A: `Row`
- B: `Column`
- C: `Stack`
- D: `Wrap`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

`Row` arranges its children horizontally (left to right by default). Use `Row` when you want widgets side by side.

</p>
</details>

---

###### 55. What's wrong with this code?

```dart
class MyWidget extends StatelessWidget {
  String title = 'Hello';

  @override
  Widget build(BuildContext context) {
    return Text(title);
  }
}
```

- A: Nothing is wrong
- B: StatelessWidget cannot have non-final fields
- C: Missing const constructor
- D: build() should return a Container

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`StatelessWidget` is immutable, so all instance fields must be `final`. The analyzer will show a warning: "This class inherits from a class marked as @immutable, and therefore should be immutable (all instance fields must be final)."

Fix: `final String title = 'Hello';`

</p>
</details>

---

###### 56. What does `setState()` do?

- A: Sets the state of the entire app
- B: Triggers a rebuild of the widget
- C: Saves data to local storage
- D: Sends state to the server

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`setState()` is used in StatefulWidget to notify Flutter that the internal state has changed. This triggers a rebuild of the widget, updating the UI to reflect the new state.

```dart
setState(() {
  counter++;
});
```

</p>
</details>

---

###### 57. Which widget adds padding around its child?

- A: `Margin`
- B: `Padding`
- C: `Spacing`
- D: `Inset`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `Padding` widget adds empty space around its child. Use `EdgeInsets` to specify the padding values.

```dart
Padding(
  padding: EdgeInsets.all(16.0),
  child: Text('Hello'),
)
```

</p>
</details>

---

###### 58. What widget makes its child scrollable?

- A: `Scroll`
- B: `Scrollable`
- C: `SingleChildScrollView`
- D: `ScrollWidget`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

`SingleChildScrollView` is a widget that scrolls a single child. Use it when you have content that might overflow the screen.

```dart
SingleChildScrollView(
  child: Column(
    children: [...],
  ),
)
```

</p>
</details>

---

###### 59. What's the purpose of the `key` property in widgets?

- A: To encrypt the widget data
- B: To help Flutter identify widgets for efficient rebuilding
- C: To store widget preferences
- D: To name the widget for debugging

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

Keys help Flutter's widget reconciliation algorithm identify which widgets have changed, moved, or been removed. They're especially important in lists where items can be reordered or removed.

```dart
ListTile(
  key: ValueKey(item.id),
  title: Text(item.name),
)
```

</p>
</details>

---

###### 60. Which widget displays a clickable button with text?

- A: `Button`
- B: `TextButton`
- C: `ClickableText`
- D: `Touchable`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`TextButton` (formerly `FlatButton`) displays a clickable text button. Other button types include `ElevatedButton`, `OutlinedButton`, and `IconButton`.

```dart
TextButton(
  onPressed: () { },
  child: Text('Click me'),
)
```

</p>
</details>

---

###### 61. What's the difference between `mainAxisAlignment` and `crossAxisAlignment`?

- A: They're the same thing
- B: `mainAxisAlignment` is for Row, `crossAxisAlignment` is for Column
- C: `mainAxisAlignment` aligns along the primary direction, `crossAxisAlignment` aligns perpendicular to it
- D: `mainAxisAlignment` is deprecated

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

In a `Row`:
- `mainAxisAlignment`: Horizontal alignment (left/center/right)
- `crossAxisAlignment`: Vertical alignment (top/center/bottom)

In a `Column`:
- `mainAxisAlignment`: Vertical alignment (top/center/bottom)
- `crossAxisAlignment`: Horizontal alignment (left/center/right)

</p>
</details>

---

###### 62. What widget displays an image from the network?

- A: `Image.network('url')`
- B: `NetworkImage('url')`
- C: `Image.url('url')`
- D: `WebImage('url')`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

`Image.network()` is the constructor for displaying images from a URL.

```dart
Image.network('https://example.com/image.png')
```

Note: `NetworkImage` is an `ImageProvider`, not a widget itself.

</p>
</details>

---

###### 63. What does `Expanded` widget do?

- A: Animates the child to expand
- B: Makes the child fill available space in a Row/Column
- C: Increases the child's font size
- D: Adds padding around the child

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`Expanded` widget expands its child to fill the available space along the main axis of a Row, Column, or Flex.

```dart
Row(
  children: [
    Text('Start'),
    Expanded(child: Container(color: Colors.blue)), // Fills remaining space
    Text('End'),
  ],
)
```

</p>
</details>

---

###### 64. What's wrong with this code?

```dart
Column(
  children: [
    Expanded(child: Text('Hello')),
  ],
)
```

- A: Nothing is wrong
- B: Column cannot have Expanded children
- C: Expanded requires multiple siblings
- D: Column needs a fixed height or to be inside another Flex widget

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

`Expanded` tries to fill available space, but a standalone `Column` has infinite height. This causes a layout error. The Column needs to be constrained, either by a fixed height or by being inside a widget that provides constraints (like `Scaffold`'s body).

</p>
</details>

---

###### 65. What does `Navigator.push()` do?

- A: Sends a push notification
- B: Adds a new route/screen to the navigation stack
- C: Pushes data to the server
- D: Updates the current screen

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`Navigator.push()` adds a new route to the navigation stack, displaying a new screen on top of the current one.

```dart
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => SecondScreen()),
);
```

</p>
</details>

---

###### 66. What does `Navigator.pop()` do?

- A: Shows a popup dialog
- B: Removes the current route from the navigation stack
- C: Pops up a snackbar
- D: Closes the app

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`Navigator.pop()` removes the current route from the stack, returning to the previous screen.

```dart
Navigator.pop(context);
```

</p>
</details>

---

###### 67. What's the purpose of `BuildContext`?

- A: To build widgets faster
- B: To store user preferences
- C: To locate the widget's position in the widget tree and access inherited widgets
- D: To compile the Flutter code

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

`BuildContext` represents the location of a widget in the widget tree. It's used to:
- Access theme data: `Theme.of(context)`
- Navigate: `Navigator.of(context)`
- Access inherited widgets: `MediaQuery.of(context)`

</p>
</details>

---

###### 68. What widget wraps a child to detect gestures?

- A: `TouchDetector`
- B: `GestureDetector`
- C: `ClickHandler`
- D: `TapWidget`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`GestureDetector` detects various gestures like tap, double tap, long press, pan, and scale.

```dart
GestureDetector(
  onTap: () { print('Tapped!'); },
  child: Container(color: Colors.blue),
)
```

</p>
</details>

---

###### 69. What's the output of `MediaQuery.of(context).size.width`?

- A: The width of the current widget
- B: The width of the screen/window
- C: The width of the parent widget
- D: Always returns 0

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`MediaQuery.of(context).size` returns the size of the media (screen/window). `.width` gives you the screen width in logical pixels.

</p>
</details>

---

###### 70. Which lifecycle method is called when a StatefulWidget is inserted into the tree?

- A: `initState()`
- B: `build()`
- C: `createState()`
- D: `didChangeDependencies()`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

`initState()` is called once when the State object is created and inserted into the tree. It's the place to do one-time initialization like setting up controllers or subscriptions.

```dart
@override
void initState() {
  super.initState();
  // Initialize here
}
```

</p>
</details>

---

###### 71. Which lifecycle method is called when a StatefulWidget is removed from the tree?

- A: `dispose()`
- B: `destroy()`
- C: `remove()`
- D: `deactivate()`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

`dispose()` is called when the State object is permanently removed. Use it to clean up resources like controllers, subscriptions, or streams.

```dart
@override
void dispose() {
  _controller.dispose();
  super.dispose();
}
```

Note: `deactivate()` is called when the widget is temporarily removed but may be reinserted.

</p>
</details>

---

###### 72. What's the difference between `const` and `final` for widgets?

- A: No difference
- B: `const` widgets are compile-time constants and can be reused, `final` prevents reassignment
- C: `final` is faster than `const`
- D: `const` only works with Text widgets

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`const` widgets are created at compile-time and can be reused across the widget tree, improving performance. `final` just prevents the variable from being reassigned.

```dart
// const - same instance reused
const Text('Hello')

// final - new instance each time, but variable can't be reassigned
final widget = Text('Hello');
```

</p>
</details>

---

###### 73. What does `SafeArea` widget do?

- A: Encrypts the child widget
- B: Prevents the child from being covered by system UI (notch, status bar)
- C: Makes the child read-only
- D: Disables touch events

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`SafeArea` adds padding to avoid system UI elements like the notch, status bar, and home indicator.

```dart
SafeArea(
  child: Column(
    children: [...],
  ),
)
```

</p>
</details>

---

###### 74. What's the parent widget for Material Design apps?

- A: `App`
- B: `MaterialApp`
- C: `FlutterApp`
- D: `MainApp`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`MaterialApp` is the root widget for Material Design apps. It provides navigation, theming, and localization.

```dart
MaterialApp(
  title: 'My App',
  theme: ThemeData(primarySwatch: Colors.blue),
  home: MyHomePage(),
)
```

For Cupertino (iOS) style, use `CupertinoApp`.

</p>
</details>

---

###### 75. What widget provides the basic Material Design visual layout structure?

- A: `MaterialLayout`
- B: `Scaffold`
- C: `AppLayout`
- D: `Screen`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

`Scaffold` provides the basic Material Design structure including app bar, body, floating action button, drawer, and bottom navigation.

```dart
Scaffold(
  appBar: AppBar(title: Text('Title')),
  body: Center(child: Text('Hello')),
  floatingActionButton: FloatingActionButton(
    onPressed: () {},
    child: Icon(Icons.add),
  ),
)
```

</p>
</details>

---

## Quick Reference

### Null Safety Operators

| Operator | Name | Example | Behavior |
|----------|------|---------|----------|
| `?` | Nullable type | `String?` | Can hold null |
| `?.` | Null-aware access | `obj?.prop` | Returns null if obj is null |
| `??` | Null coalescing | `a ?? b` | Returns b if a is null |
| `!` | Null assertion | `obj!.prop` | Crashes if obj is null |
| `??=` | Null-aware assignment | `a ??= b` | Assigns b to a only if a is null |

### Variable Keywords

| Keyword | Reassign? | Contents Mutable? | When Set? |
|---------|-----------|-------------------|-----------|
| `var` | Yes | Yes | Runtime |
| `final` | No | Yes | Runtime |
| `const` | No | No | Compile-time |

### Common Operators

| Operator | Name | Example | Result |
|----------|------|---------|--------|
| `~/` | Integer division | `7 ~/ 3` | `2` |
| `%` | Modulo | `5 % 3` | `2` |
| `/` | Division (returns double) | `5 / 2` | `2.5` |
| `++x` | Pre-increment | `y = ++x` | Increment then assign |
| `x++` | Post-increment | `y = x++` | Assign then increment |

### Collection Methods

| Method | Description | Example |
|--------|-------------|---------|
| `.add()` | Add item | `list.add(4)` |
| `.removeAt()` | Remove at index | `list.removeAt(0)` |
| `.length` | Get size | `list.length` |
| `.where()` | Filter | `list.where((x) => x > 2)` |
| `.map()` | Transform | `list.map((x) => x * 2)` |
| `.reduce()` | Combine all | `list.reduce((a, b) => a + b)` |
| `.take()` | First n items | `list.take(3)` |
| `.skip()` | Skip n items | `list.skip(2)` |
| `.reversed` | Reverse order | `list.reversed` |
| `...` | Spread | `[...list, 4]` |

---

## Contributing

Feel free to submit a PR to add more questions!
