# Demo Generation Workflow Skill

A GitHub-ready skill package for turning raw enterprise-system requirements into either:

- App / PDA interactive demos
- Web back-office / admin interactive demos

## What this skill does

This skill enforces a 3-stage workflow:

1. Request raw requirements
2. Normalize and structure them into a requirement brief
3. Generate the demo only after confirmation

It is designed for scenarios such as:

- MES / WMS / ERP demos
- Instrument management systems
- Internal enterprise admin systems
- Warehouse handheld / PDA operation flows
- Pre-sales client demo preparation

## Supported demo types

### 1. App / PDA Demo
Best for:
- Receiving
- Putaway
- Inventory counting
- Shipping
- Production reporting
- Inspection / patrol workflows

Typical output:
- React single-file interactive demo

### 2. Web Demo
Best for:
- Master data maintenance
- Parameter setup
- Instrument management
- Query + table + modal form systems
- Desktop enterprise admin systems

Typical output:
- Single HTML file using native HTML + CSS + JavaScript

## Package structure

```text
demo_generation_workflow_skill/
├── SKILL.md
├── README.md
├── skill.json
├── manifest.json
└── examples/
    ├── raw_requirement_example_app.md
    ├── raw_requirement_example_web.md
    ├── normalized_requirement_example_app.md
    ├── normalized_requirement_example_web.md
    └── generated_output_notes.md
```

## Recommended usage flow

### Step 1
Ask the user for raw requirements.

### Step 2
Return a structured requirement brief containing:
- Recommended demo type
- User role
- Usage scenario
- Core flow
- Main functions
- Page suggestions
- Search conditions
- Display fields
- Input fields
- Validation rules
- Exception handling
- Default assumptions
- Items pending confirmation

### Step 3
Wait for explicit confirmation before generating the demo.

## Guardrails

- Do not generate code before confirmation
- Use Traditional Chinese
- Use enterprise / factory terminology
- Fill reasonable defaults where requirements are incomplete
- Match UI style to the selected route:
  - App / PDA → mobile workflow UI
  - Web → desktop admin UI

## Files

- `SKILL.md`: full machine/human-readable skill definition
- `skill.json`: compact metadata and routing config
- `manifest.json`: package file manifest
- `examples/`: examples of raw input, normalized briefs, and output expectations

## Version

Current package version: `2.1.0`
