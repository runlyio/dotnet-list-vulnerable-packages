# dotnet-list-vulnerable-packages

This action uses `dotnet list package` to list vulnerable packages.

| Input | Description | Default | Permission |
| :- | :- | :- | :- |
| add_to_pr | Adds the results to the PR | false | pull-requests: write |
| add_to_job_summary | Adds the results to the workflow job summary | true | |
| fail_on_low | Fails the workflow if low, moderate, or high severity vulnerabilities are found | false | |
| fail_on_moderate | Fails the workflow if moderate or high severity vulnerabilities are found | false | |
| fail_on_high | Fails the workflow if high severity vulnerabilities are found | false | |
| output_file | Saves the results to specified file | "vuln.md" | |
| root_folder | Folder that contains the solution file | "." | |

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