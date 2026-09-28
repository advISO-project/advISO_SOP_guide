Scope
=====

.. important::
   This section is a fundamental building block of any SOP

The 'Scope' section of an SOP should define the boundaries of the :ref:`procedure <procedure>` i.e. what it covers, what it excludes, and who it applies to. It ensures that users understand the exact context and applicability of the procedure, helping to prevent misuse or misinterpretation.

Depending on the type of procedure being documented, the scope may include:

- **Types of data or samples:** The specific data formats, sample types, equipment, or materials the procedure is designed for.

- **Technologies and methods:** The platforms, tools, or methodologies the procedure applies to.

- **Personnel:** The roles or individuals authorised to perform or oversee the procedure.

- **Limitations:** Any exclusions, constraints, or unsupported scenarios users should be aware of.

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
