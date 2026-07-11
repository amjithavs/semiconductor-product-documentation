# CLI Reference

## Overview

The Enterprise Test Platform Command Line Interface (CLI) enables administrators and engineers to automate platform operations, manage projects, execute validation workflows, and retrieve system information.

---

# CLI Syntax

```bash
platform <command> [options]
```

---

# Global Options

| Option | Description |
|--------|-------------|
| --help | Displays command help |
| --version | Displays the platform version |
| --verbose | Enables verbose output |
| --config | Specifies the configuration file |
| --log | Enables command logging |

---

# Common Commands

## Display Platform Version

```bash
platform --version
```

Example Output

```text
Enterprise Test Platform
Version 1.0.0
```

---

## Display Help

```bash
platform --help
```

Displays all available commands and options.

---

## Create a Project

```bash
platform project create --name Validation_Project_01
```

Example Output

```text
Project created successfully.
Project ID: P10045
```

---

## List Projects

```bash
platform project list
```

Example Output

```text
Project ID     Status

P10045         Active

P10046         Completed
```

---

## Run Validation

```bash
platform validation run --project P10045
```

Example Output

```text
Validation Started

Job ID: JOB2026

Status: Running
```

---

## Check Validation Status

```bash
platform validation status --job JOB2026
```

Example Output

```text
Status : Completed

Result : Passed
```

---

## Generate Report

```bash
platform report generate --project P10045
```

Example Output

```text
Report generated successfully.

Location:

reports/P10045/report.pdf
```

---

## View Logs

```bash
platform logs view
```

Example Output

```text
Displaying latest application logs...
```

---

## Configuration Commands

### View Configuration

```bash
platform config show
```

### Update Configuration

```bash
platform config update
```

---

# Exit Codes

| Exit Code | Description |
|-----------|-------------|
| 0 | Success |
| 1 | Invalid Command |
| 2 | Invalid Arguments |
| 3 | Authentication Failed |
| 4 | Configuration Error |
| 5 | Internal Error |

---

# Best Practices

- Validate command syntax before execution.
- Run commands with the appropriate user permissions.
- Use configuration files for repeatable workflows.
- Review logs after failed executions.
- Use the `--help` option for command-specific guidance.

---

# Related Documentation

- User Guide
- Administrator Guide
- API Reference
- Troubleshooting Guide
