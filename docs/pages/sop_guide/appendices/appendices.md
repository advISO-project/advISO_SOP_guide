# Appendix

An optional *'Appendix'* section of an SOP can be used to provide supplementary information relevant to to the procedure. Such information may include example reports, schematics of bioinformatics pipelines, work flow diagrams etc.

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

::::::{dropdown} 💻 Code Update & Review Procedure
.. include:: example_code_review.md
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
