# create-rune CLI Tool

`create-rune` is a Node.js CLI tool designed for creating rune projects. Currently in early development as a placeholder stub.

Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Working Effectively

- **Bootstrap and validate the repository:**
  - `npm install` -- completes in <1 second, no dependencies. NEVER CANCEL.
  - `./bin/create-rune` -- should output "create rune: coming soon..."
  - `npm link` -- installs globally, takes <2 seconds. NEVER CANCEL.
  - `create-rune` -- test global command, should output "create rune: coming soon..."

- **No build process required:** The main executable is a simple bash script at `bin/create-rune`. No compilation or bundling is needed.

- **Testing:**
  - `npm test` -- currently fails with "Error: no test specified" as no test framework is configured.
  - Manual validation: Run `./bin/create-rune` and verify it outputs the expected message.

## Critical Information

- **Current State:** This is a placeholder/stub project with minimal functionality.
- **Main Executable:** `bin/create-rune` is a bash script that only prints "create rune: coming soon..."
- **No Dependencies:** The project has no runtime or development dependencies.
- **No Build Step:** No compilation, transpilation, or bundling required.
- **No Test Framework:** Tests are not currently configured.

## Validation

- **ALWAYS run these validation steps after making changes:**
  1. `npm install` -- verify no errors
  2. `./bin/create-rune` -- verify expected output
  3. `npm link` -- verify global installation works
  4. `create-rune` -- verify global command works
  5. Check that the script is executable: `ls -la bin/create-rune`

- **Manual Testing Scenarios:**
  - Test local execution: `./bin/create-rune`
  - Test global execution after `npm link`: `create-rune`
  - Verify both produce: "create rune: coming soon..."

## Common Tasks

The following are outputs from frequently run commands. Reference them instead of viewing, searching, or running bash commands to save time.

### Repository Structure
```
ls -la
total 32
drwxr-xr-x  1 runner docker  4096 [timestamp] .
drwxr-xr-x  1 runner docker  4096 [timestamp] ..
drwxr-xr-x  1 runner docker  4096 [timestamp] .git
drwxr-xr-x  1 runner docker  4096 [timestamp] .github
-rw-r--r--  1 runner docker  3906 [timestamp] .gitignore
-rw-r--r--  1 runner docker    20 [timestamp] README.md
drwxr-xr-x  1 runner docker  4096 [timestamp] bin
-rw-r--r--  1 runner docker   730 [timestamp] package-lock.json
-rw-r--r--  1 runner docker   562 [timestamp] package.json
```

### Package.json Contents
```json
{
  "name": "create-rune",
  "version": "0.0.2",
  "description": "create an rune",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "bin": {
    "create-rune": "bin/create-rune"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/melvincarvalho/create-rune.git"
  },
  "author": "Melvin Carvalho",
  "bugs": {
    "url": "https://github.com/melvincarvalho/create-rune/issues"
  },
  "homepage": "https://github.com/melvincarvalho/create-rune#readme",
  "keywords": [
    "aam",
    "create-rune",
    "rune"
  ]
}
```

### Main Executable
```bash
#!/usr/bin/env bash

echo "create rune: coming soon..."
```

### README.md Contents
```markdown
# create-rune
create rune
```

## Development Guidelines

- **When adding functionality:** You'll likely need to add dependencies, tests, and proper CLI argument handling.
- **Future build process:** If TypeScript or other transpilation is added, update these instructions with build commands.
- **Testing:** When adding tests, configure a proper test runner (Jest, Mocha, etc.) and update the npm test script.
- **Linting:** No linting is currently configured. Consider adding ESLint when real code is added.

## Timing Expectations

- `npm install`: <1 second (no dependencies)
- `npm link`: <2 seconds  
- `./bin/create-rune`: Instant
- `create-rune`: Instant

## File Permissions

The `bin/create-rune` file must be executable. If you modify it, ensure it retains execute permissions:
```bash
chmod +x bin/create-rune
```

## Common Pitfalls

- **Don't expect complex functionality:** This is currently just a placeholder that prints a message.
- **No error handling:** The current script has no error handling or argument parsing.
- **Global installation required for testing:** Use `npm link` to test the global command behavior.
- **Shebang line required:** The `#!/usr/bin/env bash` line is critical for the script to execute properly.