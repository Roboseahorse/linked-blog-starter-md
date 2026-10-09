# Thinking Procedurally

## Lesson Objectives

- Identify the components of a problem
- Identify the components of a solution
- Determine the order of the steps needed to solve a problem
- Identify sub-procedures necessary to solve a problem

> [!IMPORTANT] Core Idea
> Most problems are easier to solve when they are broken down into smaller parts.

## Decomposition

> [!NOTE] Definition
> Procedural decomposition means breaking a problem into smaller sub-problems where each sub-problem performs a specific task.

### Key Points

- Large problems are divided into manageable tasks.
- Sub-problems can be broken down further.
- Decomposition makes complex systems easier to design and understand.

## Structured Programming

Structured programming aims to improve the clarity and quality of programs.

| Technique | Purpose |
|------------|---------|
| Modularisation | Break a program into subroutines |
| Sequence | Instructions executed in order |
| Selection | Make decisions using conditions |
| Iteration | Repeat instructions using loops |
| Recursion | A procedure calls itself |

## Top-Down Design

1. Start with the overall problem.
2. Split it into major tasks.
3. Split tasks into smaller subtasks.
4. Continue until each procedure performs a single function.

> [!IMPORTANT]
> A hierarchy chart is often used to show the structure of a program.

```text
Exam Results Report
├── Initialise Variables
├── Process File
│   ├── Open File
│   ├── Process All Records
│   │   ├── Read Record
│   │   └── Process Record
│   └── Close File
└── Print Report
    └── Calculate Averages
```

## Benefits of Modularisation

### Development

- Programs are easier to write.
- Modules can be tested individually.
- Code can be reused.
- Multiple programmers can work on different modules.

### Maintenance

- Errors are easier to locate.
- Debugging takes less time.
- Programs are easier to maintain.
- New features can be added through new modules.

## Good Programming Practice

- Use meaningful identifiers.
- Document inputs, outputs and preconditions.
- Write useful comments.
- Ensure each sub-procedure performs one task.
- Use parameters and local variables appropriately.

## Procedures, Functions and Parameters

Once a problem has been decomposed, the solution can be built using procedures and functions that communicate through parameters.

## Exam Summary

> [!IMPORTANT] Key Facts
> - Problems should be decomposed into smaller components.
> - Solutions should be broken into procedures and functions.
> - Structured programming uses sequence, selection and iteration.
> - Modularisation improves testing, maintenance and reuse.
> - Top-down design breaks large problems into manageable subtasks.

> [!QUESTION]- Self-Check Questions
> 1. What is procedural decomposition?
> 2. Why is modularisation useful?
> 3. What is top-down design?
> 4. What does a hierarchy chart show?
> 5. Give three benefits of modular programming.

## Related Notes

- [[Structured Programming]]
- [[Modular Programming]]
- [[Procedures and Functions]]
- [[Parameters]]
- [[Thinking Logically]]
- [[Thinking Concurrently]]
