Specimen Type & Test Selection
==============================

.. important::
   This section is relevant to SOPs involving the direct use of specimens, which will predominately consist of laboratory procedures or sample reception/triage.

The *'Specimen Type & Test Selection'* section of an SOP should describe the types of specimens for which the procedure has been validated. It must also outline the acceptance criteria that determine whether the specimen is suitable for analysis. In cases where multiple workflows or test options are available, this section should also provide clear criteria for selecting the appropriate test option.

Key points to cover include:

- **Validate specimen types:** List the specimen types that have been approved for use with the procedure (e.g. blood, urine, tissue, swabs, serum etc).

- **Acceptance criteria:** Define the minimum requirements for specimen quality, volume, labelling, and storage conditions to ensure sample integrity and confirm sample origin.

- **Test Selection:** Provide clear guidance on how to choose between different testing workflows or assays based on specimen type received or clinical indications. 


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
