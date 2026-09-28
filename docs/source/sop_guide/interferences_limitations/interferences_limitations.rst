Interferences & Limitations
===========================

This section should outline any factors that may affect the reliability, accuracy, or applicability of the procedure. Identifying interferences and limitations helps ensure that results are interpreted correctly and that the procedure is used within its validated scope.

This section may include:

  - **Detection or Performance Limits:** Define the boundaries of the procedure’s capability (e.g. sensitivity, specificity, minimum/maximum measurable values, or operational thresholds).

  - **Interfering Factors:** List any substances, conditions, or external influences that may compromise performance. Examples include contaminants, environmental conditions, equipment variability, or data quality issues.

  - **Dependencies:** Note any reliance on tools, equipment, software, reagents, or personnel expertise that could introduce limitations or compatibility concerns.

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
