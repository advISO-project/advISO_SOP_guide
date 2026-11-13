# Underlying Principles

The underlying principles section of an SOP can be used to provide background information of relevance to the procedure being documented.

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
