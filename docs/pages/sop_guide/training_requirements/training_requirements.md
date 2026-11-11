(sop-guide-training-requirements)=

# Training requirements

The Training Requirements section of an SOP outlines what knowledge, skills, qualifications, or resources a person must have before they are allowed to perform the procedure. Its purpose is to ensure that only properly prepared individuals carry out the task, which protects quality, safety, and consistency. It can be separated into sections, for example; prerequisites, and training materials needed.

---

**Example content:**

:::{dropdown} 🧬 Bioinformatics QC Procedure

```{include} example_bioinformatics.md
```

:::

:::{dropdown} 👩‍🔬 Staff Training Procedure

```{include} example_training.md
```

:::

:::{dropdown} 🌌 Galaxy Training Procedure

```{include} example_galaxy.md
```

:::

:::{dropdown} 🧪 Laboratory Procedure

```{include} example_lab.md
```

:::

:::{dropdown} 💻 Code Update & Review Procedure

```{include} example_code_review.md
```

:::

```{raw} html
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
```
