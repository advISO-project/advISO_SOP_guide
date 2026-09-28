Cross-References
================

.. important::
   This section is a fundamental building block of any SOP

The 'Cross-References' section of an SOP should list other controlled documents that support or relate to the procedure. Cross-references ensure that users can easily identify associated SOPs, validation documents, and equipment instructions necessary for performing the procedure correctly.

Depending on the procedure, cross-references may include:

- **Associated SOPs:** Related procedures that describe upstream or downstream processes, such as wet-lab procedures or reporting workflows.

- **Validation and verification documents:** References to documents establishing the analytical performance, accuracy, and reproducibility of the pipeline or procedure.  

- **Equipment or instrument SOPs:** Instructions for using specific laboratory instruments or software platforms required for the procedure.

- **Guidelines and standards:** Relevant internal or external guidelines, such as laboratory standards, regulatory requirements, or best practice documents.

.. attention::
   If the organisation does not have an electronic document management system (eQMS), cross-references should include version numbers and revision dates to ensure users access the correct version.


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
