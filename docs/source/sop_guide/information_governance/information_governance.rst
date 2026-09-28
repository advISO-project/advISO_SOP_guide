Information Governance
======================

.. important::
  This section must be included in SOPs where data containing personally identifiable information (PII), or other sensitive information is accessed, generated, or stored.

The *'Information Governance'* section of an SOP should describe how information generated, accessed, or stored during a procedure is managed in compliance with institutional policies, legal requirements, and ethical standards. Depending on the procedure, this may include:

- **Data Protection & Privacy:** Specify how personal or sensitive data is handled in line with relevant regulations (e.g. GDPR in the UK/EU, HIPAA in the US etc).
- **Genetic Data Governance:** Define how genomic sequences, variant data, and metadata are stored, anonymised, and shared.
- **Confidentiality:** Define who has access to the information and how confidentiality is maintained.
- **Access Control:** State what permissions, accounts, or authentication are required to access data or systems.
- **Retention & Disposal:** Outline how long data must be retained and the approved methods for secure disposal.
- **Audit & Traceability:** Describe how information use is logged, monitored, and traceable for compliance purposes.
- **Ethical Use:** Ensure information is used only for its intended purpose (e.g. surveillance, diagnostics, research) and in accordance with institutional policies.
- **Third-Party Systems:** Identify any external platforms or services used (e.g. NCBI).

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
