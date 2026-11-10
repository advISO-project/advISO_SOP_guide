# Purpose of the Procedure

:::{important}
This section is a fundamental building block of any SOP
:::

The 'Purpose' section of an SOP should provide a clear and concise statement of why the procedure exists and its intended role within the organisation/laboratory. It should outline the specific goals the procedure aims to achieve, and explain how it contributes to broader workflows, services, or regulatory requirements. This helps users understand the value and relevance of the procedure in context.

Depending on the type of procedure, the purpose may describe:

- The operational or clinical need the procedure addresses.
- The outcomes or deliverables it is designed to produce.
- Its position within a larger workflow or diagnostic service.

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
