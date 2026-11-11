*Example content from a wet-lab SOP outlining the procedure for preparing sequencing libraries using the Illumina DNA Prep kit.*

```{raw} html
<hr />
```

**Procedure**

**1. Run Setup & Documentation**

**1.1 Run ID Formatting**

When preparing a sequencing run, a unique Run ID must be generated to ensure proper tracking and documentation.

Format:

`<Date>-<Workstream>-N<Number of samples>`

Example:

If a library is prepared for 32 HIV samples, including a no-template control (NTC), on the 8th of March 2025, the Run ID is: `2025-03-08-HIV-N32`.

**1.2 Index Set Selection**

Consult the UDI Indexing Log (SOP 084F2) to determine which index set (1–16) is required. Record the Run ID on the chosen index set within the index log.

```{raw} html
<hr>
```

**2. Plate Map & Sample Organisation**

For each sequencing run, a plate map must be generated to document sample placement.

**Requirements:**

> - Record the Run ID clearly at the top of the plate map.
> - Assign each sample to a specific well position.
> - Order samples sequentially, starting from A1 and continuing acoss each row.
> - Place controls (including NTCs) in designated wells, typically at the end of the plate, to ensure consistent placement across runs.

**File storage:**

Save a copy of the completed plate map in \<<LOCATION>>, using the **Run ID** as the filename.

```{raw} html
<hr>
```

**3. Reagent Preperation**

Referring to Table 1 and BenchAid 085, prepare the following reagents:

> - BLT
> - TWB
> - TB1
> - TSB
> - EPM

Record reagent lot numbers and expiration dates of all reagents in the NGS reagent database [REF].```{list-table}
:header-rows: 1

* - Item
  - Storage temperature
  - Instructions
* - BLT
  - 2°C to 8°C
  - Bring to room temperature.
* - TWB
  - 2°C to 8°C
  - Bring to room temperature. Once kit is in use, leave at room temperature.Once kit is in use, leave at room temperature.
* - TB1
  - -25°C to -15°C
  - Bring to room temperature.
* - TSB
  - 2°C to 8°C
  - Bring to room temperature. If precipitates occur, vortex and heat to 37°C until dissolved. One kit is in use, leave at room temperature.
* - EPM
  - -25°C to -15°C
  - Thaw in the fridge. Leave in the fridge until use.
```

```{raw} html
<hr>
```

**4. Tagmentation (FLEXTAG)**

**4.1 Programme Setup**

> - Load the FLEXTAG programme on the Veriti thermocycler.
> - Leave the programme on hold until all samples and reagents are ready for processing.

**4.2 TAG mix preperation**

Vortex BLT (30s) and TB1 (pulse spin). Prepare the Tagmentation (TAG) Mix in a reservoir as follows, mixing well with a pipette:

> - BLT: 7 µl per sample
> - TB1: 7 µl per sample

**4.3 Sample Loading**

> - Label a semi-skirted plate with the run ID followed by “-TAG”.
> - **For viral amplicons (HIV, Flu):** Shake PCR product plate at 1800 rpm for 2 minutes using the plate shaker. Centrifuge at 3000 rpm for 30 seconds. Dilute sample 1:3 by adding 10 µl sample to 20 µl nuclease‑free water to the labelled semi-skirted plate. Mix by pipetting 10 times or shake at 1600 rpm for 1 minute.
> - **For COVID samples:** Shake PCR plates A and B at 1800rpm for 2 minutes on using the plate shaker. Centrifuge at 3000 rpm for 30 seconds. Add 10 µl of sample from PCR Plate A, 10 µl of sample from PCR Plate B, and 10 µl nuclease‑free water to the labelled semi-skirted plate. Mix by pipetting 10 times or shake at 1600 rpm for 1 minute.
> - **For bacterial samples:** Shake extract plate at 1800rpm for 2 minutes using the plate shaker. Centrifuge at 3000rpm for 30 seconds. Place plat on magnet for 5 minutes to remove silica from the extraction. Add 30µl of neat sample to the labelled semi-skirted plate.
> - Add 10 µl TAG Mix to each sample. Pipette once to dispense, shake (1600 rpm, 1 min), then seal plate.

**4.4 FLEXTAG programme execution**

> - Load plate onto the Veriti thermocycler.
> - Skip hold top initiate FLEXTAG.
> - **Runtime:** 15 minutes.
> - Once FLEXTAG programme has completed, remove plate from the Veriti thermocycler and centrifuge at 3000rpm for 30 seconds.

```{raw} html
<hr>
```

**5. Stop Reaction (FLEXSTOP)**

**5.1 TSB Preperation**

> - Vortex and pulse spin TSB.
> - Aliquot required volume (at least 7 µl per sample) into a reservoir.

**5.2 FLEXSTOP Execution**

> - Start FLEXSTOP programme on the Veriti thermocycler and leave on hold.
> - Add 5 µl of TSB to each sample.
> - Seal plate and shake at 1600rpm for 1 minute.
> - Load plate into the thermocycler and skip hold to initiate FLEXSTOP.
> - **Runtime:** 15 minutes.

**5.3 Index Plate Handling**

:::{Note}
This is a parellel task
:::

While FLEXSTOP is running:

> - Remove required index plate from freezer.
> - Thaw at room temperature.
> - Shake at 1600rpm for 1 minute.
> - Centrifuge at 3000rpm for 30 seconds.
> - Record Index lot number and expiry date on the DNA Prep Worksheet.

```{raw} html
<hr>
```

**6. Pre-Amplification Cleanup**

**6.1 Post-FLEXSTOP Handling**

> - Remove plate from thermocycler.
> - Centrifuge at 3000 rpm for 30 seconds.
> - Start FLEXPCR programme and leave on hold.

**6.2 Bead Binding & Wash**

> - Mix TWB and aliquot required volume (at least 210 µl per sample) into a reservoir.
> - Place plate on magnet for 3 minutes.
> - Remove and discard the supernatant with a multichannel pipette without disturbing the beads.
> - Remove from magnet.
> - Commence first wash as follows:
>   : 1. Add 100 µl of TWB, then pipette (10x) to gently mix.
>     2. Place on magnet for a further 3 minutes.
>     3. Remove and discard the supernatant as before.
> - Commence second wash as follows:
>   : 1. Add 100 µl of TWB, then pipette (10x) to gently mix.
>     2. Place on magnet for a further 3 minutes.

:::{Important}
After the second wash, keep plate on magnet with supernatant on until the PCR mix is ready.
:::

```{raw} html
<hr>
```

**7. PCR-Amplification (FLEXPCR)**

> - Start FLEXPCR programme on the Veriti thermocycler and leave on hold.
> - Remove EPM from fridge. Invert to mix and pulse spin.
> - Make up PCR mix as follows:
>
> ```{list-table}
> :header-rows: 1
>
> * -
>   - Volume per sample
> * - EPM
>   - 14 µl
> * - Nuclease-free water
>   - 14 µl
> ```
>
> - Using a 20 µl multichannel pipette, remove all the supernatant being careful to not disturb the beads.
> - Remove plate from magnet and add 20 µl of PCR mix to each sample.
> - Add 5 µl of index to each sample.
> - Seal plate and place on shaker at 1600rpm for 1 minute.
> - Load plate into the thermocycler and skip hold to initiate FLEXPCR.
> - **Runtime:** 15 minutes.

:::{Note}
**Safe Stopping Point!**
The plate can be left on the thermocycler overnight or the plate can be sealed and stored at 2-8°C. Do not freeze.
:::
