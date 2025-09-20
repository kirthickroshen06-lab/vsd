End-to-End Design and Verification Flow

1. Software Baseline (C Program)

We begin with the design specification written in C.

The program is compiled using GCC, and the generated output is labeled as O0.

The same specification is also executed directly in C to produce O1.

At this point, we check functional equivalence:

O0 == O1



2. Hardware Modeling (RTL Level)

To represent the hardware, we use a high-level hardware description language such as Bluespec or Chisel.

The application runs on this RTL model, producing an output called O2.

Verification requires equivalence with the software result:

O2 == O1



3. Physical Design and Tapeout

The RTL design is synthesized and passed through the physical design flow to generate GDSII files.

The layout is checked for DRC (Design Rule Check) and LVS (Layout vs. Schematic) compliance.

Once validated, the design is sent to the foundry (tapeout).



4. Fabrication and Tapein

After manufacturing, the fabricated chip is received from the foundry (tapein).

The chip is packaged and mounted on a test board along with essential components:

USB controller

External memory

Voltage regulator

Crystal oscillator




5. System Bring-Up and Execution

The application is loaded onto the chip through the USB interface.

Running the application on silicon generates the final output, O4.



6. Equivalence Across All Stages

The correctness of the design flow is ensured by maintaining functional equivalence across all staghe portal for further assistance.
