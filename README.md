# GitHub Actions Templates

This repository contains reusable GitHub Actions workflows designed for various use cases such as CI/CD pipelines and automation tasks.

## Usage

To use these workflows in your repository:

1. Reference the reusable workflow in your `.github/workflows/` YAML file.
2. Provide the required inputs (if any).

### Basic Syntax for Calling a Reusable Workflow

```yaml
jobs:
  job-name:
    uses: <owner>/<repository>/.github/workflows/<template-file-name>@<branch>
    with:
      # Specify the required inputs here
```

---

## Templates and How to Call Them

### **Bun CI Template**

A CI workflow for projects using Bun.

```yaml
jobs:
  bun-ci-job:
    uses: pHo9UBenaA/gh-action-templates/.github/workflows/bun-ci.yml@main
```

---

### **Chrome Extension Upload Template**

A workflow to automatically upload a Chrome extension.

```yaml
jobs:
  upload-chrome-extension:
    uses: pHo9UBenaA/gh-action-templates/.github/workflows/chrome-extension-upload.yml@main
    with:
      client-id: ${{ secrets.CHROME_CLIENT_ID }}
      client-secret: ${{ secrets.CHROME_CLIENT_SECRET }}
      refresh-token: ${{ secrets.CHROME_REFRESH_TOKEN }}
      extension-id: "your-extension-id"
      file-path: "./path/to/extension.zip"
      publish: "true" # Set to "false" if you don't want to publish immediately
```

---

### **Deno CI Template**

A CI workflow for projects using Deno.

```yaml
jobs:
  deno-ci-job:
    uses: pHo9UBenaA/gh-action-templates/.github/workflows/deno-ci.yml@main
```

---

## Prerequisites

- **Repository Permissions**: Verify that the repository has appropriate permissions for writing, publishing, or other necessary actions.

--

## License

This project is licensed under the [MIT License](LICENSE). See the license file for more details.
