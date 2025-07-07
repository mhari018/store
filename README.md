# 💎 Ruby Idiomatic Cheat Sheet for C# Developers

Welcome! This cheat sheet is designed to help C# developers transition into Ruby by showing idiomatic Ruby equivalents of familiar C# patterns.

---

## 📚 Basics

| Concept           | C#                            | Ruby                            | Notes                                  |
|-------------------|-------------------------------|----------------------------------|----------------------------------------|
| Hello World       | `Console.WriteLine("Hi")`     | `puts "Hi"`                     | `puts` = print with newline            |
| Variable Declare  | `int x = 5;`                  | `x = 5`                         | Ruby is dynamically typed              |
| String Interp     | `$"Hi {name}"`                | `"Hi #{name}"`                 | Use `#{}` inside double quotes         |
| Null              | `null`                        | `nil`                          | `nil` is falsy                         |
| Boolean check     | `if (x != null)`              | `if x`                         | Only `false` and `nil` are falsy       |

---

## 🔁 Loops & Iteration

| C#                                 | Ruby                              | Description                         |
|------------------------------------|-----------------------------------|-------------------------------------|
| `for (int i = 0; i < 5; i++)`      | `5.times do |i|` ... `end`        | Times loop                          |
| `foreach (var item in list)`       | `list.each do |item| ... end`     | Each iterator                       |
| LINQ: `list.Where(x => x > 1)`     | `list.select { |x| x > 1 }`        | Filter                              |
| LINQ: `list.Select(x => x * 2)`    | `list.map { |x| x * 2 }`           | Map / transform                     |

---

## 🔧 Conditions

| C#                           | Ruby                          | Notes                                 |
|-----------------------------|-------------------------------|----------------------------------------|
| `if (x == 1)`               | `if x == 1`                   | Same meaning                          |
| Ternary `x ? y : z`         | `x ? y : z`                   | Same syntax                           |
| Null coalesce: `x ?? y`     | `x || y`                      | Use `||` for fallback value            |
| Null safe: `x?.name`        | `x&.name`                     | Ruby 2.3+ supports safe navigation     |

---

## 🎒 Functions

| C#                                | Ruby                                  | Notes                          |
|-----------------------------------|----------------------------------------|--------------------------------|
| `void Say(string name)`           | `def say(name)` ... `end`             | No return type needed          |
| Default param `int x = 5`         | `def add(x = 5)`                      | Use `=` in parameter           |
| Multiple returns                  | `return a, b;`                        | `return [a, b]` or just `a, b` |
| Lambda: `x => x * 2`              | `->(x) { x * 2 }`                     | Also `proc { |x| ... }`        |

---

## 🧱 Classes & Modules

| C#                                   | Ruby                                 | Notes                          |
|--------------------------------------|--------------------------------------|--------------------------------|
| `class Person { }`                   | `class Person; end`                  | Same idea                      |
| `interface IFlyable`                 | `module Flyable` + `include`         | Mixin instead of interface     |
| Static class                         | `module Math`                        | Use modules                    |
| Extension method                     | Monkey patch (not recommended)       | Ruby allows reopening classes  |

---

## 🚨 Exception Handling

| C#                                     | Ruby                                     |
|----------------------------------------|------------------------------------------|
| `try { ... } catch (Ex e) { ... }`     | `begin ... rescue => e ... end`         |
| `finally { ... }`                      | `ensure`                                 |

---

## 🔁 Collections

| C#                            | Ruby                        |
|-------------------------------|-----------------------------|
| `List<int> list = new()`      | `list = []`                |
| `list.Add(x)`                 | `list << x`                |
| `Dictionary<string, int>`     | `hash = {}` or `{ key: val }` |

---

## 🧪 Testing (RSpec style)

```ruby
describe "Calculator" do
  it "adds numbers correctly" do
    expect(1 + 1).to eq(2)
  end
end
