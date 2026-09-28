Quality Control & Verification
==============================

This section should outline the quality control (QC) measures and verification steps implemented to ensure the accuracy, reliability, and reproducibility of the procedure described in the SOP. Clear documentation of QC practices helps maintain confidence in results and supports compliance with regulatory and accreditation standards.

This section may include:

- **Control Samples:** Use positive and negative controls, as well as samples of known characteristics (e.g. variant types, resistance markers, reference strains) to verify that the procedure consistently produces expected results.

- **Internal Quality Assurance (IQA) and External Quality Assurance (EQA):** Document participation in internal QC programs (e.g. repeatability checks, peer review of results) and external proficiency testing schemes to benchmark performance against other laboratories or organisations.

- **Software and Code Verification:** For computational workflows, include measures such as code review, unit testing, and continuous integration (CI) testing to ensure reproducibility, detect errors early, and maintain compatibility across versions.

- **Verification Procedures:** Outline the steps taken to verify the pipeline's performance.

-------

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
