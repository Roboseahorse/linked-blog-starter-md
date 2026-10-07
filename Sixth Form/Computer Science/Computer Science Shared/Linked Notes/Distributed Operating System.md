A [[Distributed Operating System]] coordinates work across **multiple computers**. A single job can be divided between different machines, while the OS manages communication with their hardware.

Resources available across the computers can include:

- **Processor time**
- **Memory**
- **Input/output facilities**

The OS coordinates the distribution of tasks by passing instructions between computers.

> [!IMPORTANT] Key Point
> To the user, the system can appear to behave like a single powerful computer even though processing is being distributed across several machines.

### Advantages and limitation

| Advantage                                                                         | Limitation                                                             |
| --------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Access to greater computational power                                             | The programmer has little or no control over how tasks are distributed |
| The user can work as though using one processor                                   | Task distribution is handled by the OS                                 |
| Programs do not need to be written differently just to use the distributed system | The underlying distribution is hidden from the user                    |
