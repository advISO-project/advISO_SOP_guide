Result Reporting & Authorisation
================================

.. important::
  This section should be included in SOPs where results are reported to internal or external stakeholders.

The *'Result Reporting & Authorisation'* section of an SOP should detail the process for authorising and the subsequent release of results generated during the procedure.

This section may include:

- **Reporting procedure:** Outline the steps for preparing, verifying, and releasing results, including required documentation, approval processes, and communication channels.

- **Responsibilities:** Define who is responsible for each step of the reporting procedure.

- **Reporting format:** Define the standard format for reporting.

- **Authorisation:** Define how reports are authorised prior to release, specify: 
    - when authorisation is required (e.g. all results or only when a specific result is generated such as the identification of a resistance or pathogenetic mutation);
    - how authorisation is documented;
    - what conditions must be met before authorisation can be granted.

- **Recipients:** Define who the intended recipients of the report are e.g. the requesting clinician, outbreak analyst etc.

- **Laboratory clinical interpretation:** Describe how results are interpreted in a clinical or analytical context, including guidance on providing explanatory notes, limitations, or recommendations provided alongside the result(s).

- **Alert/critical Values:** Specify how critical or alert values are identified, documented, and communicated promptly to responsible clinicians or stakeholders. Include escalation pathways and timeframes.

- **Potential sources of variation:** Highlight factors that may influence reported results (e.g. sample quality, instrument calibration, software version, operator variability) and how these are communicated within the report.

-----

**Example content:**

.. dropdown:: 🧬 Bioinformatics QC Procedure
   
   .. include:: example_bioinformatics.rst


.. dropdown:: 👩‍🔬 Staff Training Procedure
   
   .. include:: example_training.rst


.. dropdown:: 🌌 Galaxy Training Procedure
   
   .. include:: example_galaxy.rst


.. dropdown:: 🧪 Laboratory Procedure
   
   .. include:: example_lab.rst


.. dropdown:: 💻 Code Update & Review Procedure
   
   .. include:: example_code_review.rst


.. raw:: html

   <script>
     // Auto-close other dropdowns when one opens
     document.querySelectorAll('details').forEach((el) => {
       el.addEventListener('toggle', function () {
         if (el.open) {
           document.querySelectorAll('details').forEach((other) => {
             if (other !== el) {
               other.removeAttribute('open');
             }
           });
         }
       });
     });
   </script>
