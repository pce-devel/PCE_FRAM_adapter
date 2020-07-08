# FRAM-DIP converter board

The PC Engine series of systems has a different game-save storage system than most people
these days have gotten used to.  It used a 2KB static RAM.  This wasn't in the cartridges
themselves; initially, it was sold as pat of an add-on to the system: The Tennokoe 2,
"Voice from Heaven".  In later systems like the Duo series, it would be integrated into
the system unit, yet still be limited to 2KB static RAM.

You're probably thinking, "Static RAM is volatile - it loses its contents when the power
is shut off", and you'd be right.  There really weren't any non-volatiole options at the
time.  Instead, they used batteries or large capacitors to apply continuous power to the
memory, so that it would not lose its contents.  In the case of the Tennokoe 2, 2 "AA"
cells were used; in the case of the Duo, a large capacitor was used.

I have lost a few game saves on my Duo because I failed to turn the system on for a period
of time long enough to lose its contents... probably about 1 to 2 weeks.

Because of this, I was inspired to replace the SRAM with modern FeRAM to make it
non-volatile.  But the Duo is a tighter-packed PC board with surface-mount chips, so I felt it
was easier to first test the idea on the Tennokoe 2, which uses a DIP SRAM chip.  Later, I
plan to come back with a design for a surface-mount version suitable for my Duo.

I have chosen to use the Cypress FM16W08 chip, which can handle 5V, has timing which is
equal to or better than the SRAM it is replacing, and has a similar pinout.  But I still
needed to make an adapter board (which is what this repository is all about).

As the FeRAM is rated for 100 trillion read/write cycles, there is no
concern about lifetime under the usage in this application.

I designed the boards using the free version of EAGLE (2-layer, less than 100mm
on both X- and Y-axes).  The gerbers are included in this repository, in case you
want to get your own set made.


Assembly/installation instructions for the FRAM-DIP board:

https://github.com/dshadoff/PCE_FRAM_adapter/FRAM-DIP-assembly.md


