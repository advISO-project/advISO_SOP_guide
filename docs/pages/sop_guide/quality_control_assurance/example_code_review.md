*Example content from an SOP outlining the procedure for updating and reviewing code within the Luma Genomics Unit (LGU).*

```{raw} html
<hr />
```

**Verification & Quality Control**

To ensure accuracy, reproducibility, and compliance with coding standards, the following quality control measures are implemented during the code review process:

> - **Peer Review:** All merge requests must be reviewed by at least one qualified team member who is not the original developer. Reviewers assess correctness, adherence to coding standards, and potential security vulnerabilities.
> - **Testing Verification:** Developers are required to run unit tests and integration tests prior to submitting a merge request. Reviewers confirm that appropriate tests have been executed and may request additional tests if gaps are identified.
> - **Version Control & Audit Trail:** All changes are tracked in GitLab. Branch protection rules enforce that code cannot be merged without passing review and automated tests. Version tags are assigned to ensure reproducibility.
> - **Documentation Check:** Reviewers verify that any new or modified functionality is documented in accordance with LGU guidelines, ensuring clarity for future users.
> - **Continuous Improvement:** Required improvements (R) must be implemented before merging. Suggested improvements (S) are logged for future updates, supporting ongoing enhancement of code quality.
