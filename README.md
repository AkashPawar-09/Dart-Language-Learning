# Dart Language — Complete Learning Repository

A structured, from-scratch Dart curriculum built while preparing for Flutter
mobile app development. The repository is organized into five tiers, each
containing standalone, runnable `.dart` files that build in difficulty —
starting from language fundamentals and ending at the advanced patterns used
throughout production Flutter codebases.

## What This Repository Contains

Every file in this repository is written to be read, not just run. Each
concept file follows the same structure: a working example first, followed
by inline comments that explain *why* the code behaves the way it does, and
a closing block that connects the concept back to real Flutter usage.

**`TIER_2_OOP`** covers Dart's class system the way Flutter actually uses it
— mixins (`with`), abstract classes, and getters/setters are demonstrated
through examples like `SingleTickerProviderStateMixin`-style composition and
validated setters on a `BankAccount` class, so the pattern is recognizable
the first time it shows up in a real `State` class.

**`TIER_3_Async`** goes beyond textbook definitions of `Future`, `async`,
and `await` — the files simulate real API calls using `Future.delayed()`,
compare `.then()` chaining against `await`-based flow, and build up to a
full `try / catch / finally` pattern wrapped around a simulated network
request. This is the same shape of code used later for REST API and
Firebase calls in Flutter: `try { await fetchUser(); } catch (e) { }`.

**`TIER_4_Idiomatic_Dart`** focuses on the syntax that makes Dart code look
like *Dart* rather than a port from another language. Generics
(`List<T>`, `Map<K, V>`) are built up from simple examples to constrained
generic classes; cascade notation (`..`) is shown configuring objects the
same way Flutter widgets and controllers are configured in real projects;
enums are given properties and methods so they can directly model API/UI
states (`loading`, `success`, `error`) instead of relying on raw strings;
and extension methods show how to safely add reusable behavior to built-in
types like `String` and `List<int>` without modifying Dart's core classes.

**`TIER_5_Advanced_Dart`** covers the three patterns that appear constantly
once real apps are involved: factory constructors that parse JSON into
model objects (`User.fromJson()`), static members for singletons and
app-wide configuration, and typedefs that turn callback signatures like
`void Function()` into readable, reusable types — the same mechanism behind
Flutter's `onPressed`, `onTap`, and `onChanged` callbacks.

All code is written with readability as the first priority — function and
variable names are descriptive, logic is broken into small focused blocks,
and every non-obvious line carries a comment explaining what it does and,
where relevant, what output to expect.

## Repository Structure

```text
DART_Language_complete_folder/
│
├── TIER_1_Fundamentals/
│   ├── 1_Variables_data_types/
│   ├── 2_Null_safety/
│   ├── 3_Functions/
│   ├── 4_Control_flow/
│   └── 5_Collections/
│
├── TIER_2_OOP/
│   ├── 6_Classes_constructors/
│   ├── 7_Inheritance/
│   ├── 8_Abstract_classes_interfaces/
│   ├── 9_Mixins/
│   └── 10_Getters_setters/
│
├── TIER_3_Async/
│   ├── 11_Future_async_await/
│   ├── 12_Streams_StreamBuilder/
│   └── 13_Exception_handling/
│
├── TIER_4_Idiomatic_Dart/
│   ├── 14_Generics/
│   ├── 15_Cascade_notation/
│   ├── 16_Enums/
│   └── 17_Extension_methods/
│
└── TIER_5_Advanced_Dart/
    ├── 18_Factory_constructors/
    ├── 19_Static_members/
    └── 20_Typedefs/
```

Each topic folder contains 8–10 files, numbered in learning order, moving
from a basic isolated example through progressively more realistic use
cases, and ending with a `complete_*.dart` file that revises the entire
topic in one place.

## How to Run

Any file can be run independently with the Dart SDK:

```bash
dart run path/to/file.dart
```

Or pasted directly into [DartPad](https://dartpad.dev) for instant output.

## Learning Path

This repository follows a tier-based progression rather than a single long
tutorial, so each concept can be reviewed in isolation:

1. **Fundamentals** — variables, null safety, functions, control flow, collections
2. **OOP** — classes, inheritance, abstraction, mixins, getters/setters
3. **Async** — Future, async/await, Streams, exception handling
4. **Idiomatic Dart** — generics, cascades, enums, extension methods
5. **Advanced Dart** — factory constructors, static members, typedefs

The tiers are deliberately ordered to match what's needed to read and write
real Flutter code — by the end of Tier 5, the syntax patterns used in
`State` classes, API models, and widget callbacks should all be recognizable
rather than new.

## Next Steps

This repository represents the Dart foundation only. The next phase of this
learning path moves into Flutter itself: widget trees, `StatefulWidget`,
state management, REST API integration, and local/Firebase persistence.


--- 
### continue learning | happy coding 
