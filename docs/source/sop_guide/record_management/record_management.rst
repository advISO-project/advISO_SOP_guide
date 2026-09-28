Record Management
=================

.. important::
  This section should be included in SOPs where records are generated during the procedure.

The 'Record management' section of an SOP should detail the process for reviewing and authorising records produced as part of the procedure. Example records may include: audit logs, training logs, approval forms etc.

This section may include:

- **Record procedure:** Outline the steps for preparing and authorising new records, including required documentation, approval processes, and communication channels.

- **Reporting format:** Define the standard format for the record.

- **Responsibilities:** Define who is responsible for each step of record management.

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
