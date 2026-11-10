*Example content from a training SOP detailing the standardised procedure for training on the Galaxy platform*

```{raw} html
<hr />
```

**Procedure**

This section describes the step-by-step process for delivering training on developing and executing analysis workflows using the Galaxy platform. Training is delivered using the **Show → Do → Apply** instructional model to ensure progressive skill acquisition and demonstrable competency.

```{raw} html
<hr />
```

**1. Preperation (Training Coordinator + Trainer)**

**1.1 Training Coordinator Responsibilities**

> - Schedule training session(s), confirm venue or virtual setup.
> - Ensure all trainees have active Galaxy accounts (institutional instance or TIaaS).
> - Confirm resource availability (internet access, classroom laptops, temporary accounts if needed).
> - Upload or prepare training materials:
>   : - Example datasets (FASTQ/tabular files or equivalent),
>     - Training slides/handouts,
>     - Quick-reference sheet for Galaxy tool categories and parameters,
>     - Competency checklist and feedback forms.
> - Ensure prerequisites are met (see {ref}`Training Requirements <sop-guide-training-requirements>` section).

**1.2 Trainer Responsibilities**

> - Perform a "dry run" of the training workflow to confirm all tools are available and functional.
> - Test the Galaxy instance for:
>   : - Tool panel availability
>     - Workflow editor functionality
>     - Dataset upload limits
>     - Job execution responsiveness
> - Prepare a clean example history and optional template workflow for demonstration.

**1.3 Outputs**

> - Training session plan
> - Verified toolset availability
> - Example history/workflow ready for demonstration
> - Dataset folder prepared and accessible

```{raw} html
<hr />
```

**2. SHOW - Trainer Demonstration (Observation)**

The trainer performs a live demonstration, first introducing the trainee to Galaxy’s core components and essential platform operations, including navigation, dataset handling, and tool execution. The demonstration then progresses to the workflow-development process, illustrating how to build, edit, run, and manage reproducible analysis workflows. The trainer performs all relevant steps while the trainee observes and verbally explains the process from beginning to end, using the operational SOP as a training guide.

**2.1 Introduction to the Galaxy Environment**

Trainer demonstrates:

> - Registering and logging in to the Galaxy instance
> - Navigating:
>   : - Tool panel
>     - History panel
>     - Main analysis workspace
>     - Workflow menu
> - Basic Galaxy concepts:
>   : - Histories: creating and renaming a new history, uploading files to a history
>     - Datasets
>     - Tools
>     - Inputs/outputs
>     - Job execution and monitoring

**2.2 Uploading and Inspecting Data**

Trainer demonstrates how to:

> - Upload example datasets using the Upload Data tool
> - Verify and adjust dataset datatype
> - View dataset metadata and preview content
> - Apply dataset tags, annotations, and good naming conventions

**2.3 Running Tools in Galaxy**

Trainer demonstrates a minimal analysis chain using existing tools (dataset-neutral), such as:

> - Running a QC tool
> - Performing a simple filtering or mapping step (as appropriate for the dataset used)
> - Reviewing tool parameters
> - Inspecting outputs and metadata
> - Monitoring job progress and identifying failed jobs

**2.4 Building a Workflow by Connecting Tools (Manual Construction)**

The trainer demonstrates how to manually construct a workflow using the Galaxy Workflow Editor. This introduces trainees to the logic of assembling analysis steps into a reproducible sequence before learning automated extraction.

Trainer demonstrates:

> - Navigating to Workflows → Create New workflow
> - Assigning a meaningful workflow name
> - Opening the Workflow Editor
> - Searching for tools in the tool panel
> - Adding tools into the editor canvas
> - Connecting tool outputs to subsequent tool inputs
> - Adjusting tool parameters (e.g., datatype expectations, filters, reference selections)
> - Reordering modules to improve readability
> - Adding annotations describing the purpose of each step
> - Saving the workflow

Key teaching points:

> - Why connecting tools manually improves understanding of workflow logi
> - How tool outputs influence downstream inputs
> - How parameter defaults affect reproducibility
> - Common mistakes (wrong connection types, missing inputs, incompatible datatypes)

**2.5 Extracting a Workflow from a History**

Trainer shows how to:

> - Extract a workflow from the history (History → Extract Workflow)
> - Name the workflow meaningfully
> - Remove unnecessary steps
> - Save the workflow

**2.6 Editing Workflows Manually**

Trainer demonstrates:

> - Opening the Workflow Editor
> - Adding tools from the tool panel
> - Connecting tool inputs and outputs
> - Modifying default parameters
> - Reordering modules for readability
> - Adding annotations (purpose, assumptions, expected outputs)
> - Saving workflow updates

**2.7 Running the Workflow**

Trainer runs the workflow to illustrate:

> - Selecting input datasets
> - Adjusting runtime parameters
> - Executing and monitoring workflow jobs
> - Inspecting final outputs
> - Interpreting whether results match expectations
> - Documenting deviations or errors

**2.8 Sharing, Exporting, and Versioning**

Trainer demonstrates:

> - Sharing workflows (links, permission settings)
> - Exporting workflows (.ga file)
> - Creating new workflow versions and documenting changes

**2.9 Data Management Hygiene**

Trainer emphasises:

> - Proper dataset naming
> - Tagging datasets and histories
> - Purging unnecessary intermediate files
> - Keeping one “gold” history
> - Adding README-style documentation within Galaxy

**2.10 Outputs of SHOW phase**

> - Trainer demo history
> - Trainer demo workflow
> - Trainee observation notes

```{raw} html
<hr />
```

**3. DO – Performance Under Supervision**

Trainees now replicate the steps demonstrated in the SHOW phase, with real-time guidance and troubleshooting by the trainer. The goal is to reinforce understanding, identify gaps early, and ensure trainees can follow the workflow logic.

**3.1 Trainee activities**

> - Upload example datasets independently
> - Run the same set of tools demonstrated in the SHOW phase
> - Check datatype assignment and correct if needed
> - Reproduce the analysis chain and inspect outputs
> - Extract a workflow from their history
> - Edit the workflow in the Workflow Editor
> - Apply dataset tags, annotations, and documentation

**3.2 Trainer responsibilities**

> - Monitor tool execution and support troubleshooting
> - Ensure trainees understand:
> - Purpose of each step
> - Why the tool order matters
> - What constitutes valid vs invalid outputs
> - Provide guidance on workflow structure, parameter defaults, and good documentation practices
> - Record trainee challenges in preparation for the APPLY phase

**3.3 Outputs of DO phase**

> - Draft trainee workflow
> - Trainee history containing tool runs
> - Trainer notes on competency gaps

```{raw} html
<hr />
```

**4. APPLY - Independent Application & Competency**

The trainee must now demonstrate independent proficiency using a dataset and workflow relevant to the training module.

**4.1 Trainee responsibilities**

Independently produce a complete, reproducible workflow by:

> - Designing the workflow logically
> - Adding tools in the correct order
> - Configuring parameters appropriately
> - Running the workflow end-to-end
> - Documenting parameter decisions within the workflow/editor
> - Exporting the final workflow (.ga)
> - Organising their history and tagging datasets
> - Submitting:
>   : - Final workflow file (.ga)
>     - Documented history
>     - Notes on workflow logic or parameter choices

**4.2 Trainer responsibilities**

> - Assess the submitted workflow according to the competency checklist:
>   : - Logical tool order
>     - Correct use of inputs/outputs
>     - Parameter correctness and documentation
>     - Reproducibility of outputs
>     - Clear annotations and naming conventions
> - Provide feedback and remediation if required
> - Record competency status in the training matrix

```{raw} html
<hr />
```

**5. Optional Advanced Modules (Trainer's Discretion)**

Depending on trainee progress, the trainer may introduce additional topics such as:

> - Conditional workflow steps
> - Dataset collections
> - Using subworkflows
> - Batch execution
> - Parameter sweeping
> - Basic troubleshooting strategies
> - Introduction to workflow version control using external repositories (e.g., Git)

```{raw} html
<hr />
```

**6. Feedback and Evaluation**

> - Trainees complete the post-training feedback form
> - Trainer reviews all trainee outputs and finalises competency records
> - Training Coordinator compiles session feedback summary
> - QA Officer reviews documentation for completeness and signs off training completion
> - Records stored in the designated QMS/SharePoint directory
