FlowScript: Formal Language Specification


---

Overview

FlowScript is a human-centric, declarative programming language designed to express logic in a form close to natural thought and conversation. It is designed to be event-driven, readable, and expressive, focusing on simplicity, time-awareness, and safety. FlowScript is domain-flexible, allowing for custom extensions to match specific use cases such as health monitoring, home automation, and educational logic.


---

Core Principles

1. Human-Centric Expression

Prioritize readability and clarity.

Avoid traditional syntax noise: no semicolons, brackets, or strict indentation rules.

Syntax reads like logical instructions or dialogue.


2. Declarative First

Describe desired outcomes and behaviors rather than explicit step-by-step control.


3. Time-Awareness

Built-in understanding of time intervals and delays.

Native constructs: after, every, until, for, etc.


4. Event-Driven Logic

Reactions to changes or events are first-class citizens.

Keywords: when, on, if, trigger, etc.


5. Domain Simplicity & Flexibility

Domain-specific keywords are allowed through "definition" statements.

Keywords and concepts can be overridden or extended.


6. Minimal Setup, Instant Feedback

Designed for REPLs, interactive interpreters, or lightweight runtimes.


7. Safe by Design

Eliminate undefined behavior.

Strong error reporting with human-readable messages.


8. Extendable Grammar

Custom keywords and aliases supported using define.



---

Syntax Overview

Keywords:

Event Triggers: when, on, every, after, before, until

Conditions: if, else, unless

Actions: do, start, stop, alert, set, toggle

Timing: seconds, minutes, hours, days

Definitions: define, as


Example Snippets:

when door.opened:
    turn on hallway.light

after 5 minutes:
    turn off heater

define nurse_button as emergency.button
when nurse_button.pressed:
    alert "Nurse called"


---

Types

FlowScript implicitly handles the following types:

Number (e.g., 1, 3.14)

Boolean (true, false)

String ("text")

Time (5.seconds, 10.minutes)

Identifier (room.light, sensor.value)

List and Record (planned for future extension)



---

Scoping and Structure

Blocks are defined using indentation (similar to Python).

Each block follows a trigger: and an indented sequence of actions.



---

Control Flow

when condition:
    do something
else:
    do alternative

if temperature > 38:
    alert "High fever"


---

Execution Model

FlowScript is reactive.

There is no main function — execution begins based on events and schedules.

Events are monitored and matched to triggers.



---

Extensibility

define kitchen_lamp as kitchen.light

define alert_staff(message):
    alert "Staff: " + message


---

Roadmap (v0.1)

Core interpreter in Rust

REPL environment

Event simulation engine

Domain packs: home, health, education



---

License & Contribution

FlowScript is open for educational and experimental purposes. Contributions welcome under the MIT license.
