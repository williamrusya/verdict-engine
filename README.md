# Verdict Engine

**Verdict Engine** is a lightweight, deterministic rules and policy engine designed for backend systems.

It evaluates a set of predefined rules against input facts and produces a clear, predictable **verdict** (e.g. `ALLOW`, `DENY`, `SKIP`).

The project is focused on:
- deterministic decision-making
- transparency and explainability
- clean domain-driven design
- easy embedding into existing backend systems

---

## 🚀 Use cases

Verdict Engine can be used for:

- access control and authorization rules
- loan / credit approval logic
- business policy enforcement
- feature gating and eligibility checks
- replacing hard-coded `if-else` logic with declarative rules

---

## 🧠 Core concept

At its core, the engine evaluates **policies** against **facts** and produces a **verdict**.

**Input:**
```json
{
  "policy": "loan-approval",
  "facts": {
    "age": 25,
    "income": 5000,
    "country": "KZ"
  }
}
```

**Output:**
```json
{
  "verdict": "ALLOW",
  "matchedRule": "AGE_AND_INCOME_OK"
}
```

The result is always deterministic:  
the same input will always produce the same output.

---

## 🧩 Architecture principles

- **Core-first design**  
  The rules engine is implemented as a pure Java module, independent of Spring or any framework.

- **Thin infrastructure layer**  
  Spring Boot (REST API, serialization, etc.) is only a wrapper around the core engine.

- **Test-driven rules**  
  Business rules are validated through unit tests, which act as executable specifications.

---

## 🛠 Tech stack

- Java 17+
- Spring Boot (REST layer only)
- Maven
- JUnit 5 / AssertJ

---

## 📦 Project status

🚧 **Work in progress**

Current focus:
- core domain model
- rule evaluation engine
- deterministic verdict logic

Planned next steps:
- REST API (`/evaluate`)
- rule priority and conflict resolution
- explainable verdicts (why a rule matched)

---

## 📜 License

This project is licensed under the **Apache License 2.0**.  
See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributing

Contributions, ideas, and discussions are welcome.  
Please open an issue or a pull request if you'd like to collaborate.
