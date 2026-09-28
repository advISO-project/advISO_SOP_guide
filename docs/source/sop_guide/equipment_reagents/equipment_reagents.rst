.. _sop_guide_equipment_reagents:

Equipment & Reagents
====================

.. important::

   This section is suitable for laboratory procedures. For desk-based procedures use the :ref:`Resources & Tools <sop_guide_resources_tools>` section instead.

This section should list all physical items required to perform the procedure, ensuring compliance with safety standards and proper preparation before starting.

Depending on the procedure, this may include:

- **Equipment:** Instruments or devices required (e.g., centrifuges, pipettes, PCR thermocyclers, sequencing platforms, etc.).

- **Consumables:** Reagents, kits, or materials consumed during the procedure.

- **Personal Protective Equipment (PPE):** Gloves, lab coats, goggles, or other safety gear.

- **Calibration/Validation Requirements:** Any checks or certifications needed before equipment use.

- **Storage Conditions:** Requirements for reagents or materials (e.g., refrigeration, light protection).

- **Waste Disposal:** Procedures for safe disposal of reagents, consumables, or contaminated materials.

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
