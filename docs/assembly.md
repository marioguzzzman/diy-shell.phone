# Assembly guide

How to build a Shellphone from the kit, step by step. It takes about an hour,
most of it soldering.

When it's built, continue with **[Wi-Fi setup](wifi-setup.md)**.

---

## What's in the kit

- Raspberry Pi Zero W **or** Zero 2 W (both work), with its 40-pin header
- Pre-flashed microSD card (the software is already on it)
- Snail audio board (the blue PCB)
- 2×20 female socket (for the Pi) and 1×7 female socket (for the amplifier)
- MAX98357A amplifier, with a 7-pin male header and a 2-pin screw terminal
- 2 × 470 Ω resistors
- 2 × 5 mm LEDs (the snail's antennas)
- Bone-conduction transducer, speaker cable with a white 2-pin plug
- 5 V micro-USB power supply

**You also need:** a soldering iron and solder, side cutters, a small
screwdriver, a hot glue gun, and a shell. Any shell works.

The full parts list is in the [Bill of Materials](../hardware/bom.md).

## The two sides of the board

The snail board has two sides, and it matters which part goes where:

- **Top**: the snail drawing and the text **SHETELLS.STREAM**. Resistors and
  LEDs go on this side.
- **Bottom**: the text **STAY SALTY!**. The two sockets go on this side, and
  the Raspberry Pi plugs in from here.

Every part is pushed through from one side and **soldered on the other side**.

---

## Step 1: Check the Raspberry Pi

![Raspberry Pi Zero W with its pin header](../images/01-raspberry-pi-zero-w.jpg)

The Pi needs its 40-pin header (the double row of pins). If your Pi came
without one, solder the 2×20 **male** header onto it first, with the pins
pointing up on the side with the chips.

## Step 2: Solder the Pi socket

![Board (top) and the 2×20 female socket](../images/02-board-and-pi-socket.jpg)

![The socket placed on the bottom side](../images/03-pi-socket-on-back.jpg)

1. Push the long **2×20 female socket** into its holes from the **bottom**
   (STAY SALTY!) side. It goes on the outline labelled
   *Raspberry Pi zero 2w*.
2. Turn the board over and solder all 40 pins on the **top** side.

> **Tip:** solder one pin at each end first, check that the socket sits flat
> and straight, then solder the rest.

## Step 3: Solder the amplifier socket

![The 1×7 female socket for the amplifier](../images/04-amp-socket.jpg)

![Both sockets in place on the bottom side](../images/05-both-sockets-placed.jpg)

1. Push the short **1×7 female socket** into the holes labelled **MAX98357A**,
   also from the **bottom** side.
2. Solder its 7 pins on the **top** side.

![Sockets soldered, seen from the top, with the two resistors](../images/06-sockets-soldered-resistors.jpg)

## Step 4: Solder the resistors

![Resistors soldered on the top side](../images/07-resistors-soldered.jpg)

1. Bend the legs of the two **470 Ω resistors** and push them into the two
   rectangles on the **top** side (marked R1 and R2 on the bottom).
   Resistors have no direction, so either way round is fine.
2. Solder them on the bottom side and cut off the extra legs.

## Step 5: Solder the LEDs (the antennas)

![The two LEDs](../images/08-leds.jpg)

![LEDs soldered as the snail's antennas](../images/09-leds-soldered.jpg)

LEDs **only work one way round**:

- The **long leg (+)** goes into the **round** hole.
- The **short leg (−)** goes into the **square** hole. The flat edge on the
  LED's rim is on this side too.

1. Push both LEDs into the two antenna positions at the snail's head, on the **top** side.
2. Solder them on the bottom side and cut off the extra legs.

The antennas are wired straight to the power, so they light up whenever the
Shellphone is switched on.

## Step 6: Prepare the amplifier

![MAX98357A amplifier and its 7-pin header](../images/10-amp-and-header.jpg)

1. Push the **short ends** of the 7-pin male header into the amplifier's row of
   holes (Vin, GND, SD, GAIN, DIN, BCLK, LRC), with the long pins pointing
   **down**, away from the printed side. Solder all 7 pins.
2. **Solder the 2-pin screw terminal** into the two big holes marked
   **+** and **−** on the amplifier, with the screw openings facing outwards.
   *(No photo of this step; you can see the blue terminal in step 7.)*

## Step 7: Plug in the amplifier and connect the transducer

![Amplifier plugged into its socket](../images/11-amp-plugged-in.jpg)

1. Plug the amplifier into its socket on the **bottom** side. Match the pin
   names on the amplifier with the names printed next to the socket
   (**Vin GND … DIN BCLK LRC**). If they don't line up, turn it round.
2. Screw the two wires of the **speaker cable** into the screw terminal
   (**+** and **−**).
3. Connect the white plug of the cable to the **transducer**.

![The bone-conduction transducer](../images/12-transducer.jpg)

![Amplifier with the speaker cable, and the transducer](../images/13-amp-cable-transducer.jpg)

![Board with the transducer connected](../images/14-board-with-transducer.jpg)

![Close-up of the finished board](../images/15-board-closeup.jpg)

## Step 8: Insert the SD card and plug in the Pi

![Raspberry Pi and the pre-flashed SD card](../images/16-pi-and-sd-card.jpg)

1. **Insert the pre-flashed SD card into the Raspberry Pi**: the card slot is
   at one end of the Pi, and the card goes in with its label facing up.
2. Plug the Pi's pins into the **2×20 socket** on the **bottom** of the snail
   board. The Pi's chips face the snail board. Check that **all 40 pins** go
   into the socket and that it isn't shifted by one row.

![Pi plugged onto the board, seen from the bottom](../images/17-pi-plugged-in.jpg)

![The assembled electronics, seen from the top](../images/18-assembled-front.jpg)

## Step 9: Glue the transducer into the shell

![The electronics next to the shell, with the transducer inside it](../images/19-with-shell.jpg)

![The transducer glued inside the shell](../images/21-transducer-in-shell.jpg)

The transducer doesn't make sound on its own: it makes **the shell** vibrate,
and the shell becomes the speaker.

1. Find a smooth, solid spot inside the shell, where the transducer can lie
   flat with good contact.
2. **Glue it in place with hot glue.** Press the flat face of the transducer
   against the shell while the glue sets, so it touches the shell directly.
3. Lead the cable out of the shell's opening so it doesn't rattle.

## Step 10: Power it on

![Complete, with the USB power supply](../images/20-complete-with-power.jpg)

1. Plug the 5 V power supply into the Pi's micro-USB port marked **PWR IN**:
   the port at the corner of the Pi, not the one in the middle.
2. The snail's antennas light up straight away.
3. **Wait about 2 minutes.** The Pi starts up, joins the Wi-Fi and starts
   playing. Hold the shell to your ear.

No sound after a few minutes? It probably isn't on a Wi-Fi it knows yet.
Go to **[Wi-Fi setup](wifi-setup.md)**.

---

## Troubleshooting

| What you see | What to check |
|---|---|
| Antennas don't light up | Power supply plugged into **PWR IN**? Board pushed fully onto the Pi? LEDs the right way round (long leg in the round hole)? |
| Antennas light up, but no sound after 3 minutes | Wi-Fi: see [Wi-Fi setup](wifi-setup.md). |
| Connected to Wi-Fi, but no sound | Amplifier plugged in the right way round (pin names matching)? Speaker cable tight in the screw terminal? White plug pushed into the transducer? |
| Sound is very quiet | Is the transducer glued flat against the shell? Turn up the volume on the [control page](wifi-setup.md#volume-and-control-page). |
