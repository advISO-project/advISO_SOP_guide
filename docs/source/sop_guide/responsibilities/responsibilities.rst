Roles & Responsibilities
-----------------------

.. important::
   This section is a fundamental building block of any SOP

The 'Roles & Responsibilities' section of an SOP outlines the specific duties and accountability of individuals or teams involved in the execution, oversight, and authorisation of the procedure. Role titles (e.g. Bioinformatician, Lab Technician, Quality Manager, Head of Laboratory etc) should be used rather than individual names to ensure the SOP remains current even when staff change.

Depending on the procedure, this section should describe:

- **Roles involved:** Identify all personnel or teams responsible for performing, reviewing, or approving steps within the procedure.

- **Responsibilities:** Describe the specific duties for each role (e.g., performing laboratory procedures, data processing, quality control, result authorisation, report authorisation etc).

-----

.. rubric:: Example content:

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
