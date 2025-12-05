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

###### 2. What should fill the blanks for the output to be 100?

```dart
void main() {
  __(i)__ x = 5;
  __(ii)__ y;
  y = x;
  const z = x;
  print(z * y + 75);
}
```

- A: (i) `final` (ii) `final`
- B: (i) `const` (ii) `const`
- C: (i) `const` (ii) `final`
- D: (i) `final` (ii) `const`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

Let's break it down:
- `const z = x` requires `x` to be a compile-time constant, so `x` must be `const`
- `y` is **declared first, then assigned later** (`y = x` on a separate line) → **must use `final`**
- With `const x = 5` and `final y = x`:
  - `z = x = 5`
  - `y = x = 5`
  - `z * y + 75 = 5 * 5 + 75 = 25 + 75 = 100` ✓

**Key Rule:**
| Pattern | Use |
|---------|-----|
| Declare AND assign on same line (compile-time value) | `const` |
| Declare AND assign on same line (runtime value) | `final` |
| Declare first, assign later | **`final` only** (never `const`) |

`const` variables **MUST** be assigned at declaration. If you see a variable declared on one line and assigned on another, it can only be `final`.

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
