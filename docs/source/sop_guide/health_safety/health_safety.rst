Health & Safety
===============

.. important::
   This section is a fundamental building block of any SOP

This section should outline any health and safety requirements relevant to the procedure. It ensures compliance with institutional policies, legal regulations, and best practices for safe working environments.

Depending on the procedure being documented, this may include:

- **Chemical or Biological Hazards:** Risks associated with handling hazardous substances, biological materials, or infectious agents.

- **Physical Hazards:** Risks from equipment use, manual handling, noise, or temperature extremes.

- **Ergonomic Considerations:** Safe workstation setup, posture, and repetitive strain prevention (particularly relevant for computer-based procedures).

- **Training Requirements:** Any mandatory safety training or certifications required before performing the procedure.

- **Emergency Protocols:** Steps to follow in case of accidents, spills, or exposure incidents.

- **Risk Assessments:** References to relevant institutional risk assessments and applicable national regulations (e.g., COSHH in the UK, OSHA in the US, REACH in the EU etc).

.. note::

   Even procedures that appear low-risk (e.g. administrative or computational tasks) will at a minimum still need to consider the safe use of display screen equipment and desk ergonomics.

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
