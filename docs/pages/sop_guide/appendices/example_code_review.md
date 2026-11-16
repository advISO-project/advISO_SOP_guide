*Example content from an SOP outlining the procedure for updating and reviewing code within the Luma Genomics Unit (LGU).*

```{raw} html
<hr />
```

**Appendices**

**Appendix 1:** Gitlab Merge Request - Developer template

```none
# Merge Request Assignee Overview

All lines ending in :to_remove_emoji: should be edited/removed. There should be no aliens in the final comment :to_remove_emoji:
If you make an important edit to this overview comment after the review process has started, please include [INITIAL DD/MM/YY] at the line end or in the section
Title. :to_remove_emoji:

# Context
Short paragraph to describe any context for the change. Answering: :to_remove_emoji:
- What was changed/created? :to_remove_emoji:
- Rationale for the change :to_remove_emoji:
- How does the change integrate into the existing ecosystem? Will this have any upstream or downstream consequences, and have they been considered? :to_remove_emoji:

# Critical checks
As the developer, I believe these are critical checks for the reviewer to consider.
1. Item one :to_remove_emoji:

# Testing
As the developer I have completed the following tests:
1. Tests X showing X functioning as expected and producing reliable results. ​:to_remove_emoji:
2. There are Y edge cases that haven’t been tested :to_remove_emoji:
3. The testing dataset Z is comprehensive and provides sufficient coverage for XX issues. :to_remove_emoji:

## Requirements for testing
For the others to carry out testing as agreed the following is required:
- **Environment** I used (local or VM, Windows or Linux, conda? containers? venv?) and X additional software. :to_remove_emoji:
- **Locations** you need to access the X, Y, Z location as datasets :to_remove_emoji:
- **How to run the code** These are the details need to run test addition to the README (the Nextflow -profile variable used, any additional arguments required for testing, changing paths to point to test data or test locations) :to_remove_emoji:

## Tests for reviewer
As assignee I have requested the reviewer completes the following tests:
1. Test one with details of how to complete it and expected results :to_remove_emoji:

# General Checks
As the Developer I have checked:
- [ ] **Fit for purpose**. Fulfils the requirements as described in the issue
- [ ] **Style**. Meets the standards of the appropriate house style guide for the language(s) used in the project. It is readable.
- [ ] **Code duplication**. The code is free of unnecessary duplication. Standard libraries/packages or house code are being re-used.
- [ ] **Maintainability**. The code is modular and expandable.
- [ ] **Scalability**. No major computational bottlenecks are in the code that could be adjusted to improve performance with larger datasets.
- [ ] **Reliability**. The code is stable and efficient (relative to project). Errors are handled correctly.
- [ ] The version of the repo has been incremented.
- [ ] The dependencies are listed with version numbers listed appropriately
- [ ] There are no hardcoded paths for data input and output (should be passed as arguments or read from a config YAML file).
- [ ] There are no hardcoded secrets or variables that make testing difficult (should be passed as arguments or read from a config YAML file).

# Documentation:
As the Developer I have checked:
- [ ] The README is useful, descriptive and includes installation instructions.
- [ ] Functions are sufficiently documented and understandable.
```

**Appendix 2:** Gitlab Merge Request - Reviewer template

```none
# Review Overview :to_remove_emoji:
All lines ending in :to_remove_emoji: should be edited/removed. There should be no aliens in the final comment :to_remove_emoji:

Provide 2-3 overview comments that you would like to highlight to the Developer.These might include any meaningful praise about the code you would like to give.:to_remove_emoji:

# Code Improvements Summary
All proposed improvements have a separate comment, either in-line or on the merge request. They are all indexed at the start of the comment using the mandatory scheme [RS][0-9] e.g. R1.
## Required (R)
- [ ] **(R1)** - link or short description if needed :to_remove_emoji:
- [ ] **(R2)** - link or short description if needed :to_remove_emoji:
## Suggestion (S)
- [ ] **(S1)** - link or short description if needed :to_remove_emoji:
- [ ] **(S2)** - link or short description if needed :to_remove_emoji:

Give concise details of how the testing was performed that would be useful for the assignee to be aware of. These might include locations where test outputs have been saved, the date the test was performed, what version of a metadata file was used (e.g. SARS metadata file) :to_remove_emoji:
1. Test one with details and if results were as expected :to_remove_emoji:

# Reviewer Critical checks
I performed the following checks suggested by the Developer. :to_remove_emoji:
1. Item one :to_remove_emoji:

# Reviewer General Checks
As reviewer you have highlighted improvements for items on the general check list you do not think are satisfactory. :to_remove_emoji:
As reviewer I have checked the following are satisfactory: :to_remove_emoji:
- **Fit for purpose**. Fulfils the requirements as described in the issue description :to_remove_emoji:
- **Style**. Meets the standards of the appropriate house style guide for the language(s) used in the project. It is readable. :to_remove_emoji:
- **Code duplication**. The code is free of unnecessary duplication. Standard libraries/packages or house code are being re-used. :to_remove_emoji:
- **Maintainability**. The code is modular and expandable. :to_remove_emoji:
- **Scalability**. No major computational bottlenecks are in the code that could be adjusted to improve performance with larger datasets. :to_remove_emoji:
- **Reliability**. The code is stable and fast (relative to project). Errors are handled correctly. :to_remove_emoji:
- Plots are readable, axes reasonable and labels clear :to_remove_emoji:
- Tables are logical, readable and understandable. :to_remove_emoji:
- There are no hardcoded paths for data input and output (should be passed as arguments or read from a config YAML file). :to_remove_emoji:
- There are no hardcoded secrets or variables that make testing difficult (should be passed as arguments or read from a config YAML file). :to_remove_emoji:
```
