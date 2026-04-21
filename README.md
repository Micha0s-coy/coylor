Вот два блока, которые можно скопировать целиком.

### 📄 `README.md`

```markdown
# Coylor Programming Language

![Coylor Logo](https://via.placeholder.com/150x150?text=Coylor)  
*The explicit, readable, and modular language.*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-0.1.0-blue)](https://github.com/Micha0s_coy/coylor/releases/latest)
[![Windows](https://img.shields.io/badge/platform-Windows-brightgreen)]()

**Coylor** is a modern programming language designed for clarity and self-documentation. Every statement begins with `--init`, making code predictable and easy to read.

## ✨ Features

- 🔹 **Explicit syntax** – keywords start with `--`
- 🔹 **Strict static typing** – all variables are declared with a type
- 🔹 **Modularity** – import components with `--import`
- 🔹 **Modern constructs** – `if/elsif/else`, `while`, `foreach`, `try/catch`
- 🔹 **Easily extensible** – create your own components

## 🚀 Quick Start

### Installation

1. Download the latest installer: **[CoylorSetup.exe](https://github.com/Micha0s_coy/coylor/releases/latest/download/CoylorSetup.exe)**
2. Run the installer (administrator rights may be required).
3. After installation, Coylor is added to your `PATH` and `.coy` files are associated with the interpreter.

### First Program

Create a file `hello.coy`:

```coylor
--init message [{string}, {'Hello, Coylor!'}] --type var
--call print(message);
```

Run it:

```bash
coylor hello.coy
```

Output:

```
Hello, Coylor!
```

### VSCode Extension

For syntax highlighting, install the bundled VSCode extension:
- Open VSCode, go to Extensions (`Ctrl+Shift+X`)
- Click `...` → **Install from VSIX...**
- Select `coylor-language-0.0.1.vsix` from the `vscode-extension/` folder

## 📖 Examples

### Variables & Conditions

```coylor
--init age [{int}, {20}] --type var

--if age >= 18 {
    --call print('Adult');
} --elsif age >= 13 {
    --call print('Teenager');
} --else {
    --call print('Child');
}
```

### While Loop

```coylor
--init i [{int}, {0}] --type var
--while i < 5 {
    --call print(i);
    --init i [{int}, {i + 1}] --type var
}
```

### Functions

```coylor
--init add [{func}, {
    --params [{int} a, {int} b]
    --body {
        --return a + b;
    }
}] --type func

--call print(add(5, 3));  ## 8
```

### Importing Modules

```coylor
--import 'math.coy' as math;

--init pi [{float}, {math.PI}] --type var
--call print(pi);
```

## 🧩 Components

Coylor supports reusable modules called **Components**. The standard library includes:
- `math` – mathematical constants and functions
- `string` – string utilities *(coming soon)*
- `file` – file I/O *(coming soon)*