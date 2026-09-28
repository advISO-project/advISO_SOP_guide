Data Type & Analysis Selection
==============================

.. important::
   This section should be included in SOPs where data is analysed or passes through a computational pipeline.

This section of an SOP should define the types of input the procedure is validated to process and explain how data characteristics determine the choice of analysis methods, tools, and parameters.

This section may include:

- **Data Format:** Specify the format(s) of input data (e.g. FASTQ, BAM, VCF), sequencing technology (e.g. Illumina, Oxford Nanopore, PacBio), and any relevant characteristics (e.g. read length, paired-end vs single-end).

- **Sample suitability:** Describe the types of samples or organisms the data is expected to represent (e.g. human clinical samples, bacterial isolates, viral genomes).

- **Analysis Selection:** Describe how the data type influences the selection of analysis tools, algorithms, and parameters. For example, certain variant callers may be optimised for short reads versus long reads.


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
