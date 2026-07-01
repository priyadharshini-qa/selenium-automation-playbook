# Selenium Automation Playbook

A reference knowledge base documenting the architecture, design patterns,
and industry-standard practices for building a Selenium + Java test
automation framework — layer by layer.

📖 **[Read the full Framework Guide](docs/framework-guide.md)**

## What's Inside
- Framework design philosophies (POM, DDT, KDT, BDD)
- A 14-layer reference architecture (build → runner → reporting → CI/CD)
- Core design patterns used in production-grade frameworks
- Recommended project structure
- Golden rules & anti-patterns to avoid

## Architecture Snapshot

```
┌───────────────────────────────────────────┐
│  Test Layer (TestNG/JUnit)                 │  Test orchestration, assertions
├───────────────────────────────────────────┤
│  Page Object / Component Layer             │  UI abstraction (locators + actions)
├───────────────────────────────────────────┤
│  Business/Workflow Layer (optional)        │  Combines multiple page actions into flows
├───────────────────────────────────────────┤
│  Driver/Base Layer                         │  WebDriver lifecycle management
├───────────────────────────────────────────┤
│  Utility/Common Layer                      │  Waits, screenshots, file I/O, logging
├───────────────────────────────────────────┤
│  Test Data Layer                           │  External data sources (JSON/CSV/DB/Excel)
├───────────────────────────────────────────┤
│  Configuration Layer                       │  Environment, browser, timeout management
├───────────────────────────────────────────┤
│  Reporting & Logging Layer                 │  ExtentReports/Allure + Log4j/SLF4J
├───────────────────────────────────────────┤
│  CI/CD & Execution Layer                   │  Jenkins/GitHub Actions, parallel execution
└───────────────────────────────────────────┘
```

See [docs/framework-guide.md](docs/framework-guide.md) for the full 14-layer breakdown, design patterns, and golden rules.

## Who This Is For
QA engineers and SDETs looking for a structured reference when designing
or reviewing a Selenium test automation framework.

## Related
This playbook documents the standards applied in the companion
implementation repo: `selenium-automation` (SauceDemo, Java + Selenium +
TestNG + Maven, POM-based, GitHub Actions CI/CD).

## License
This project is licensed under the [MIT License](LICENSE).
