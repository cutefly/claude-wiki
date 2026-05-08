---
title: "VoltAgent/awesome-claude-code-subagents: A collection of 100+ specialized Claude Code subagents covering a wide range of development use cases"
source: "https://github.com/VoltAgent/awesome-claude-code-subagents"
author:
published:
created: 2026-05-08
description: "A collection of 100+ specialized Claude Code subagents covering a wide range of development use cases - VoltAgent/awesome-claude-code-subagents"
tags:
  - "clippings"
---
[![Group 32](https://private-user-images.githubusercontent.com/18739364/532228493-55b97c47-8506-4be0-b18f-f5384d063cbb.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NzgyMzIzMzYsIm5iZiI6MTc3ODIzMjAzNiwicGF0aCI6Ii8xODczOTM2NC81MzIyMjg0OTMtNTViOTdjNDctODUwNi00YmUwLWIxOGYtZjUzODRkMDYzY2JiLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA1MDglMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwNTA4VDA5MjAzNlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTA2YWM3OGY2MDVjMDU2MTZkN2YwMGQzMWY3MDY4YTEzY2VlNDIwM2YyMjU4ZmNlMjFjMTRkZjAxMWZiMmZlMmYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.kUdTLRA1V2Os3Cr13g3JgY3NV8T-WGjpsVw7oX-L1Zc)](https://github.com/VoltAgent/voltagent)  
  

**The awesome collection of Claude Code subagents.**  

**More awesome collections for developers**  

## Awesome Claude Code Subagents

This repository serves as the definitive collection of Claude Code subagents, specialized AI assitants designed for specific development tasks.

## Installation

```
claude plugin marketplace add VoltAgent/awesome-claude-code-subagents
claude plugin install <plugin-name>
```

Examples:

```
claude plugin install voltagent-lang    # Language specialists
claude plugin install voltagent-infra   # Infrastructure & DevOps
```

See [Categories](#-categories) below for all available plugins.

> **Note**: The `voltagent-meta` orchestration agents work best when other categories installed.

### Option 1: Manual Installation

1. Clone this repository
2. Copy desired agent files to:
	- `~/.claude/agents/` for global access
		- `.claude/agents/` for project-specific use
3. Customize based on your project requirements

### Option 2: Interactive Installer

```
git clone https://github.com/VoltAgent/awesome-claude-code-subagents.git
cd awesome-claude-code-subagents
./install-agents.sh
```

This interactive script lets you browse categories, select agents, and install/uninstall them with a single command.

### Option 3: Standalone Installer (no clone required)

```
curl -sO https://raw.githubusercontent.com/VoltAgent/awesome-claude-code-subagents/main/install-agents.sh
chmod +x install-agents.sh
./install-agents.sh
```

Downloads agents directly from GitHub without cloning the repository. Requires `curl`.

### Option 4: Agent Installer (use Claude Code to install agents)

```
curl -s https://raw.githubusercontent.com/VoltAgent/awesome-claude-code-subagents/main/categories/09-meta-orchestration/agent-installer.md -o ~/.claude/agents/agent-installer.md
```

Then in Claude Code: "Use the agent-installer to show me available categories" or "Find PHP agents and install php-pro globally".

## 📚 Categories

### 01\. Core Development

**Plugin:** `voltagent-core-dev`

Essential development subagents for everyday coding tasks.

- [**api-designer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/01-core-development/api-designer.md) - REST and GraphQL API architect
- [**backend-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/01-core-development/backend-developer.md) - Server-side expert for scalable APIs
- [**design-bridge**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/01-core-development/design-bridge.md) - Design-to-agent translator
- [**electron-pro**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/01-core-development/electron-pro.md) - Desktop application expert
- [**frontend-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/01-core-development/frontend-developer.md) - UI/UX specialist for React, Vue, and Angular
- [**fullstack-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/01-core-development/fullstack-developer.md) - End-to-end feature development
- [**graphql-architect**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/01-core-development/graphql-architect.md) - GraphQL schema and federation expert
- [**microservices-architect**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/01-core-development/microservices-architect.md) - Distributed systems designer
- [**mobile-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/01-core-development/mobile-developer.md) - Cross-platform mobile specialist
- [**ui-designer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/01-core-development/ui-designer.md) - Visual design and interaction specialist
- [**websocket-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/01-core-development/websocket-engineer.md) - Real-time communication specialist

### 02\. Language Specialists

**Plugin:** `voltagent-lang`

Language-specific experts with deep framework knowledge.

- [**typescript-pro**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/typescript-pro.md) - TypeScript specialist
- [**sql-pro**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/sql-pro.md) - Database query expert
- [**swift-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/swift-expert.md) - iOS and macOS specialist
- [**vue-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/vue-expert.md) - Vue 3 Composition API expert
- [**angular-architect**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/angular-architect.md) - Angular 15+ enterprise patterns expert
- [**cpp-pro**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/cpp-pro.md) - C++ performance expert
- [**csharp-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/csharp-developer.md) -.NET ecosystem specialist
- [**django-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/django-developer.md) - Django 4+ web development expert
- [**dotnet-core-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/dotnet-core-expert.md) -.NET 8 cross-platform specialist
- [**dotnet-framework-4.8-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/dotnet-framework-4.8-expert.md) -.NET Framework legacy enterprise specialist
- [**elixir-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/elixir-expert.md) - Elixir and OTP fault-tolerant systems expert
- [**expo-react-native-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/expo-react-native-expert.md) - Expo and React Native mobile development expert
- [**fastapi-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/fastapi-developer.md) - Modern async Python API framework expert
- [**flutter-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/flutter-expert.md) - Flutter 3+ cross-platform mobile expert
- [**golang-pro**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/golang-pro.md) - Go concurrency specialist
- [**java-architect**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/java-architect.md) - Enterprise Java expert
- [**javascript-pro**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/javascript-pro.md) - JavaScript development expert
- [**powershell-5.1-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/powershell-5.1-expert.md) - Windows PowerShell 5.1 and full.NET Framework automation specialist
- [**powershell-7-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/powershell-7-expert.md) - Cross-platform PowerShell 7+ automation and modern.NET specialist
- [**kotlin-specialist**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/kotlin-specialist.md) - Modern JVM language expert
- [**laravel-specialist**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/laravel-specialist.md) - Laravel 10+ PHP framework expert
- [**nextjs-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/nextjs-developer.md) - Next.js 14+ full-stack specialist
- [**node-specialist**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/node-specialist.md) - Node.js specialist
- [**php-pro**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/php-pro.md) - PHP web development expert
- [**python-pro**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/python-pro.md) - Python ecosystem master
- [**rails-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/rails-expert.md) - Rails 8.1 rapid development expert
- [**react-specialist**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/react-specialist.md) - React 18+ modern patterns expert
- [**rust-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/rust-engineer.md) - Systems programming expert
- [**spring-boot-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/spring-boot-engineer.md) - Spring Boot 3+ microservices expert
- [**symfony-specialist**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/02-language-specialists/symfony-specialist.md) - Symfony 6+/7+/8+ PHP framework and Doctrine ORM expert

### 03\. Infrastructure

**Plugin:** `voltagent-infra`

DevOps, cloud, and deployment specialists.

- [**azure-infra-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/azure-infra-engineer.md) - Azure infrastructure and Az PowerShell automation expert
- [**cloud-architect**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/cloud-architect.md) - AWS/GCP/Azure specialist
- [**database-administrator**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/database-administrator.md) - Database management expert
- [**docker-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/docker-expert.md) - Docker containerization and optimization expert
- [**deployment-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/deployment-engineer.md) - Deployment automation specialist
- [**devops-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/devops-engineer.md) - CI/CD and automation expert
- [**devops-incident-responder**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/devops-incident-responder.md) - DevOps incident management
- [**incident-responder**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/incident-responder.md) - System incident response expert
- [**kubernetes-specialist**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/kubernetes-specialist.md) - Container orchestration master
- [**network-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/network-engineer.md) - Network infrastructure specialist
- [**platform-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/platform-engineer.md) - Platform architecture expert
- [**security-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/security-engineer.md) - Infrastructure security specialist
- [**sre-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/sre-engineer.md) - Site reliability engineering expert
- [**terraform-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/terraform-engineer.md) - Infrastructure as Code expert
- [**terragrunt-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/terragrunt-expert.md) - Terragrunt orchestration and DRY IaC specialist
- [**windows-infra-admin**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/03-infrastructure/windows-infra-admin.md) - Active Directory, DNS, DHCP, and GPO automation specialist

### 04\. Quality & Security

**Plugin:** `voltagent-qa-sec`

Testing, security, and code quality experts.

- [**accessibility-tester**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/accessibility-tester.md) - A11y compliance expert
- [**ad-security-reviewer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/ad-security-reviewer.md) - Active Directory security and GPO audit specialist
- [**ai-writing-auditor**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/ai-writing-auditor.md) - AI writing pattern detector and rewriter
- [**architect-reviewer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/architect-reviewer.md) - Architecture review specialist
- [**chaos-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/chaos-engineer.md) - System resilience testing expert
- [**code-reviewer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/code-reviewer.md) - Code quality guardian
- [**compliance-auditor**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/compliance-auditor.md) - Regulatory compliance expert
- [**debugger**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/debugger.md) - Advanced debugging specialist
- [**error-detective**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/error-detective.md) - Error analysis and resolution expert
- [**penetration-tester**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/penetration-tester.md) - Ethical hacking specialist
- [**performance-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/performance-engineer.md) - Performance optimization expert
- [**powershell-security-hardening**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/powershell-security-hardening.md) - PowerShell security hardening and compliance specialist
- [**qa-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/qa-expert.md) - Test automation specialist
- [**security-auditor**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/security-auditor.md) - Security vulnerability expert
- [**test-automator**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/test-automator.md) - Test automation framework expert
- [**ui-ux-tester**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/04-quality-security/ui-ux-tester.md) - Exhaustive documented-flow UI tester

### 05\. Data & AI

**Plugin:** `voltagent-data-ai`

Data engineering, ML, and AI specialists.

- [**ai-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/ai-engineer.md) - AI system design and deployment expert
- [**data-analyst**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/data-analyst.md) - Data insights and visualization specialist
- [**data-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/data-engineer.md) - Data pipeline architect
- [**data-scientist**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/data-scientist.md) - Analytics and insights expert
- [**database-optimizer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/database-optimizer.md) - Database performance specialist
- [**llm-architect**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/llm-architect.md) - Large language model architect
- [**machine-learning-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/machine-learning-engineer.md) - Machine learning systems expert
- [**ml-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/ml-engineer.md) - Machine learning specialist
- [**mlops-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/mlops-engineer.md) - MLOps and model deployment expert
- [**nlp-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/nlp-engineer.md) - Natural language processing expert
- [**postgres-pro**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/postgres-pro.md) - PostgreSQL database expert
- [**prompt-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/prompt-engineer.md) - Prompt optimization specialist
- [**reinforcement-learning-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/05-data-ai/reinforcement-learning-engineer.md) - Reinforcement learning and agent training expert

### 06\. Developer Experience

**Plugin:** `voltagent-dev-exp`

Tooling and developer productivity experts.

- [**build-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/build-engineer.md) - Build system specialist
- [**cli-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/cli-developer.md) - Command-line tool creator
- [**dependency-manager**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/dependency-manager.md) - Package and dependency specialist
- [**documentation-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/documentation-engineer.md) - Technical documentation expert
- [**dx-optimizer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/dx-optimizer.md) - Developer experience optimization specialist
- [**git-workflow-manager**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/git-workflow-manager.md) - Git workflow and branching expert
- [**legacy-modernizer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/legacy-modernizer.md) - Legacy code modernization specialist
- [**mcp-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/mcp-developer.md) - Model Context Protocol specialist
- [**powershell-ui-architect**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/powershell-ui-architect.md) - PowerShell UI/UX specialist for WinForms, WPF, Metro frameworks, and TUIs
- [**powershell-module-architect**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/powershell-module-architect.md) - PowerShell module and profile architecture specialist
- [**readme-generator**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/readme-generator.md) - Repository README generation specialist
- [**refactoring-specialist**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/refactoring-specialist.md) - Code refactoring expert
- [**slack-expert**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/slack-expert.md) - Slack platform and @slack/bolt specialist
- [**tooling-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/06-developer-experience/tooling-engineer.md) - Developer tooling specialist

### 07\. Specialized Domains

**Plugin:** `voltagent-domains`

Domain-specific technology experts.

- [**api-documenter**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/api-documenter.md) - API documentation specialist
- [**blockchain-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/blockchain-developer.md) - Web3 and crypto specialist
- [**embedded-systems**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/embedded-systems.md) - Embedded and real-time systems expert
- [**fintech-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/fintech-engineer.md) - Financial technology specialist
- [**game-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/game-developer.md) - Game development expert
- [**healthcare-admin**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/healthcare-admin.md) - Healthcare administration specialist with 51 sub-agents covering revenue cycle, compliance, quality, clinical ops, health IT, and payer relations
- [**iot-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/iot-engineer.md) - IoT systems developer
- [**m365-admin**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/m365-admin.md) - Microsoft 365, Exchange Online, Teams, and SharePoint administration specialist
- [**mobile-app-developer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/mobile-app-developer.md) - Mobile application specialist
- [**payment-integration**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/payment-integration.md) - Payment systems expert
- [**quant-analyst**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/quant-analyst.md) - Quantitative analysis specialist
- [**risk-manager**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/risk-manager.md) - Risk assessment and management expert
- [**seo-specialist**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/07-specialized-domains/seo-specialist.md) - Search engine optimization expert

### 08\. Business & Product

**Plugin:** `voltagent-biz`

Product management and business analysis.

- [**business-analyst**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/08-business-product/business-analyst.md) - Requirements specialist
- [**content-marketer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/08-business-product/content-marketer.md) - Content marketing specialist
- [**customer-success-manager**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/08-business-product/customer-success-manager.md) - Customer success expert
- [**legal-advisor**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/08-business-product/legal-advisor.md) - Legal and compliance specialist
- [**license-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/08-business-product/license-engineer.md) - Software licensing and compliance systems specialist
- [**product-manager**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/08-business-product/product-manager.md) - Product strategy expert
- [**project-manager**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/08-business-product/project-manager.md) - Project management specialist
- [**sales-engineer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/08-business-product/sales-engineer.md) - Technical sales expert
- [**scrum-master**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/08-business-product/scrum-master.md) - Agile methodology expert
- [**technical-writer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/08-business-product/technical-writer.md) - Technical documentation specialist
- [**ux-researcher**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/08-business-product/ux-researcher.md) - User research expert
- [**wordpress-master**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/08-business-product/wordpress-master.md) - WordPress development and optimization expert

### 09\. Meta & Orchestration

**Plugin:** `voltagent-meta`

Agent coordination and meta-programming.

- [**airis-mcp-gateway**](https://github.com/agiletec-inc/airis-mcp-gateway) - Docker-based MCP multiplexer that aggregates 60+ tools behind 7 meta-tools, reducing context token usage by 97%. One command to start, auto-enables servers on demand
- [**agent-installer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/09-meta-orchestration/agent-installer.md) - Browse and install agents from this repository via GitHub
- [**agent-organizer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/09-meta-orchestration/agent-organizer.md) - Multi-agent coordinator
- [**codebase-orchestrator**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/09-meta-orchestration/codebase-orchestrator.md) - Safe refactor governance orchestrator
- [**context-manager**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/09-meta-orchestration/context-manager.md) - Context optimization expert
- [**error-coordinator**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/09-meta-orchestration/error-coordinator.md) - Error handling and recovery specialist
- [**it-ops-orchestrator**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/09-meta-orchestration/it-ops-orchestrator.md) - IT operations workflow orchestration specialist
- [**knowledge-synthesizer**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/09-meta-orchestration/knowledge-synthesizer.md) - Knowledge aggregation expert
- [**multi-agent-coordinator**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/09-meta-orchestration/multi-agent-coordinator.md) - Advanced multi-agent orchestration
- [**performance-monitor**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/09-meta-orchestration/performance-monitor.md) - Agent performance optimization
- [**pied-piper**](https://github.com/sathish316/pied-piper/) - Orchestrate Team of AI Subagents for repetitive SDLC workflows
- [**task-distributor**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/09-meta-orchestration/task-distributor.md) - Task allocation specialist
- [**taskade**](https://github.com/taskade/mcp) - AI-powered workspace with autonomous agents, real-time collaboration, and workflow automation with MCP integration
- [**workflow-orchestrator**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/09-meta-orchestration/workflow-orchestrator.md) - Complex workflow automation

### 10\. Research & Analysis

**Plugin:** `voltagent-research`

Research, search, and analysis specialists.

- [**research-analyst**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/10-research-analysis/research-analyst.md) - Comprehensive research specialist
- [**search-specialist**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/10-research-analysis/search-specialist.md) - Advanced information retrieval expert
- [**trend-analyst**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/10-research-analysis/trend-analyst.md) - Emerging trends and forecasting expert
- [**competitive-analyst**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/10-research-analysis/competitive-analyst.md) - Competitive intelligence specialist
- [**market-researcher**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/10-research-analysis/market-researcher.md) - Market analysis and consumer insights
- [**project-idea-validator**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/10-research-analysis/project-idea-validator.md) - Brutal go/no-go product idea validator
- [**data-researcher**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/10-research-analysis/data-researcher.md) - Data discovery and analysis expert
- [**scientific-literature-researcher**](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/categories/10-research-analysis/scientific-literature-researcher.md) - Scientific paper search and evidence synthesis via [BGPT MCP](https://github.com/connerlambden/bgpt-mcp)

## 🤖 Understanding Subagents

Subagents are specialized AI assistants that enhance Claude Code's capabilities by providing task-specific expertise. They act as dedicated helpers that Claude Code can call upon when encountering particular types of work.

### What Makes Subagents Special?

**Independent Context Windows**  
Every subagent operates within its own isolated context space, preventing cross-contamination between different tasks and maintaining clarity in the primary conversation thread.

**Domain-Specific Intelligence**  
Subagents come equipped with carefully crafted instructions tailored to their area of expertise, resulting in superior performance on specialized tasks.

**Shared Across Projects**  
After creating a subagent, you can utilize it throughout various projects and distribute it among team members to ensure consistent development practices.

**Granular Tool Permissions**  
You can configure each subagent with specific tool access rights, enabling fine-grained control over which capabilities are available for different task types.

### Core Advantages

- **Memory Efficiency**: Isolated contexts prevent the main conversation from becoming cluttered with task-specific details
- **Enhanced Accuracy**: Specialized prompts and configurations lead to better results in specific domains
- **Workflow Consistency**: Team-wide subagent sharing ensures uniform approaches to common tasks
- **Security Control**: Tool access can be restricted based on subagent type and purpose

### Getting Started with Subagents

**1\. Access the Subagent Manager**

```
/agents
```

**2\. Create Your Subagent**

- Choose between project-specific or global subagents
- Let Claude generate an initial version, then refine it to your needs
- Provide detailed descriptions of the subagent's purpose and activation triggers
- Configure tool access (leave empty to inherit all available tools)
- Customize the system prompt using the built-in editor (press `e`)

**3\. Deploy and Utilize** Your subagent becomes immediately available. Claude Code will automatically engage it when suitable, or you can explicitly request its help:

```
> Have the code-reviewer subagent analyze my latest commits
```

### Subagent Storage Locations

| Type | Path | Availability | Precedence |
| --- | --- | --- | --- |
| Project Subagents | `.claude/agents/` | Current project only | Higher |
| Global Subagents | `~/.claude/agents/` | All projects | Lower |

Note: When naming conflicts occur, project-specific subagents override global ones.

## 📖 Subagent Structure

Each subagent follows a standardized template:

```
---
name: subagent-name
description: When this agent should be invoked
tools: Read, Write, Edit, Bash, Glob, Grep
model: sonnet
---

You are a [role description and expertise areas]...

[Agent-specific checklists, patterns, and guidelines]...

## Communication Protocol
Inter-agent communication specifications...

## Development Workflow
Structured implementation phases...
```

### Tool Assignment Philosophy

### Smart Model Routing

Each subagent includes a `model` field that automatically routes it to the right Claude model — balancing quality and cost:

| Model | When It's Used | Examples |
| --- | --- | --- |
| `opus` | Deep reasoning — architecture reviews, security audits, financial logic | `security-auditor`, `architect-reviewer`, `fintech-engineer` |
| `sonnet` | Everyday coding — writing, debugging, refactoring | `python-pro`, `backend-developer`, `devops-engineer` |
| `haiku` | Quick tasks — docs, search, dependency checks | `documentation-engineer`, `seo-specialist`, `build-engineer` |

You can override any agent's model by editing the `model` field in its frontmatter. Set `model: inherit` to use whatever model your main conversation is using.

### Tool Assignment Philosophy

Each subagent's `tools` field specifies Claude Code built-in tools, optimized for their role:

- **Read-only agents** (reviewers, auditors): `Read, Grep, Glob` - analyze without modifying
- **Research agents** (analysts, researchers): `Read, Grep, Glob, WebFetch, WebSearch` - gather information
- **Code writers** (developers, engineers): `Read, Write, Edit, Bash, Glob, Grep` - create and execute
- **Documentation agents** (writers, documenters): `Read, Write, Edit, Glob, Grep, WebFetch, WebSearch` - document with research

Each agent has minimal necessary permissions. You can extend agents by adding MCP servers or external tools to the `tools` field.

## 🧰 Tools

### subagent-catalog

Claude Code skill for browsing and fetching subagents from this catalog.

| Command | Description |
| --- | --- |
| `/subagent-catalog:search <query>` | Find agents by name, description, or category |
| `/subagent-catalog:fetch <name>` | Get full agent definition |
| `/subagent-catalog:list` | Browse all categories |
| `/subagent-catalog:invalidate` | Refresh cache |

**Installation:**

```
cp -r tools/subagent-catalog ~/.claude/commands/
```

## 🤝 Contributing

We welcome contributions! See [CONTRIBUTING.md](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/CONTRIBUTING.md) for guidelines.

- Submit new subagents via PR
- Improve existing definitions
- Report issues and bugs

## Contributor ♥️ Thanks

[![Contributors](https://camo.githubusercontent.com/2c12497f14f684d2e6f4332f36600d4fea59a1bb0330b63b17ce4b30d57659cd/68747470733a2f2f636f6e747269622e726f636b732f696d6167653f7265706f3d766f6c746167656e742f617765736f6d652d636c617564652d636f64652d7375626167656e7473266d61783d35303026636f6c756d6e733d323026616e6f6e3d31)](https://camo.githubusercontent.com/2c12497f14f684d2e6f4332f36600d4fea59a1bb0330b63b17ce4b30d57659cd/68747470733a2f2f636f6e747269622e726f636b732f696d6167653f7265706f3d766f6c746167656e742f617765736f6d652d636c617564652d636f64652d7375626167656e7473266d61783d35303026636f6c756d6e733d323026616e6f6e3d31)

## 📄 License

MIT License - see [LICENSE](https://github.com/VoltAgent/awesome-claude-code-subagents/blob/main/LICENSE)

This repository is a curated collection of subagent definitions contributed by both the maintainers and the community. All subagents are provided "as is" without warranty. We do not audit or guarantee the security or correctness of any subagent. Review before use, the maintainers accept no liability for any issues arising from their use.

If you find an issue with a listed subagent or want your contribution removed, please [open an issue](https://github.com/VoltAgent/awesome-claude-code-subagents/issues) and we'll address it promptly.