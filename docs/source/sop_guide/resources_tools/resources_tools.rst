.. _sop_guide_resources_tools:

Resources & Tools
=================

.. important::

  Use **either** the *Resources & Tools* section (for desk-based procedures) **or** the :ref:`Equipment & Reagents <sop_guide_equipment_reagents>` section (for laboratory procedures).

This section should list all resources and tools required to carry out the procedure. It ensures that users have access to the necessary infrastructure, information, and permissions before starting.

Depending on the procedure, this may include:

- **Software:** Applications, platforms, or tools required (e.g., computer software, analysis platforms, training systems etc).

- **Data & Information Sources:** Databases, datasets, records, or reference materials needed to complete the task.

- **Access Requirements:** Permissions, accounts, or network access necessary to use the resources.

- **Documentation & Guidance:** Manuals, policies, guidelines, or online references that support correct use of tools.

- **Hardware:** Computers, servers, workstations, or other devices required for the procedure.

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
