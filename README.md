# dotnet-list-vulnerable-packages

This action uses `dotnet list package` to list vulnerable packages.

- `add_to_pr`: If true, adds the results to the PR. Default: false
- `add_to_job_summary`: If true, adds the results to the job summary. Default: true
- `fail_on_low`: Fail step if low, moderate, or high severity vulnerabilities found. Default: false
- `fail_on_moderate`: Fail step if moderate or high severity vulnerabilities found. Default: false
- `fail_on_high`: Fail step if high severity vulnerabilities are found. Default: false
- `output_file`: File that results will be saved to. Default: "vuln.md"
- `root_folder`: Folder that contains the solution file. Default: "."

# Usage
```
- name: Check for Vulnerabilities
  uses: runlyio/dotnet-list-vulnerable-packages@v1
```
```
- name: Check for Vulnerabilities
  uses: runlyio/dotnet-list-vulnerable-packages@v1
  with:
    fail_on_high: true
```
```
- name: Check for Vulnerabilities
  uses: runlyio/dotnet-list-vulnerable-packages@v1
  with:
    fail_on_high: true
    add_to_pr: true
```