# Technicolor Process Emulator (2 and 3 Strips)

Revive the aesthetic of cinema's golden age with this **DCTL (DaVinci Color Transform Language)** for DaVinci Resolve. It emulates the iconic **2-strip and 3-strip Technicolor processes**, offering detailed control over the intensity of each color and the characteristic "color bleeding" to achieve an authentic vintage film look.


# Detailed Description and Philosophy

Technicolorama is a DCTL designed to simulate the Technicolor filming and printing processes. Unlike a static LUT, it provides **dynamic parameters** to fully customize the effect.

It allows colorists and editors to precisely recreate the vibrant, saturated world of classic cinema. It's ideal for giving a unique character to **music videos, short films, or any piece** seeking a nostalgic, color-rich aesthetic.

The tool is based on the two most famous Technicolor processes:

  2-Strip Process: An earlier version that created a distinctive image from red and cyan components.
  3-Strip Process: Which recorded light onto three distinct negatives (red, green, and blue) to later combine them.


# Parameters and Controls

This DCTL offers the following controls in the DaVinci Resolve interface:

Technicolor Process: A dropdown menu to choose between the two simulation modes.

  3 strips (RGB): Emulates the most advanced Technicolor process, working with the Red, Green, and Blue channels.
  2 strips (Red and Cyan): Emulates the older process, generating an image based on a red and a cyan component.

Red Strip Intensity: Controls the strength of the red channel in both modes.

Green/Cyan Strip Intensity:

  3 strips mode, this adjusts the intensity of the green channel.
  2 strips mode, this adjusts the intensity of the cyan component, which is generated from the original green and blue channel information.

Blue Strip Intensity: In 3 strips mode, this adjusts the intensity of the blue channel.
  This slider is ignored and has no effect in 2 strips mode.

Color Bleeding: This slider simulates the imperfection of the tinting process, where colors "bleed" into one another.
  It mixes each color channel with an average of the other two. This effect is only active in 3 strips mode.

Print Contrast: Applies a final contrast curve to the entire image to emulate the dense appearance of a physical film print. This adjustment is applied to the... (The original text cuts off here, but this is the translation of what was provided.)
