# Poetry Machines (F23) 10/30 Class Prep: Python & Hardware

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
This tutorial is written by [Katherine Walden](https://github.com/kwaldenphd) and is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

# Python & Hardware

[Google Drive folder](https://drive.google.com/drive/folders/1PrI5VLy7jH9IXMMu9_d_7xLK_WHtyJUh?usp=drive_link) with Python explorations.

# GPIO Overview

*Information in this section is taken from the Raspberry Pi Foundation's "[Physical Computing With Python](https://projects.raspberrypi.org/en/projects/physical-computing/1)" lesson*

<blockquote>"One powerful feature of the Raspberry Pi is the row of GPIO pins along the top edge of the board. GPIO stands for General-Purpose Input/Output. These pins are a physical interface between the Raspberry Pi and the outside world. At the simplest level, you can think of them as switches that you can turn on or off (input) or that the Pi can turn on or off (output)."</blockquote>

<p align="center"><img src="https://circuitdigest.com/sites/default/files/inlineimages/raspberry-pi-GPIO-pins.jpg" width=65%></p>

<blockquote>"The GPIO pins allow the Raspberry Pi to control and monitor the outside world by being connected to electronic circuits. The Pi is able to control LEDs, turning them on or off, run motors, and many other things. It’s also able to detect whether a switch has been pressed, the temperature, and light. We refer to this as physical computing."</blockquote>

Many of the peripherals folks can work with are already set up to connect to the Raspberry Pi's 40 pins.

Let's look at an example, the [Voice Bonnet](https://www.adafruit.com/product/4757).

<table><tr>
<td><p align="center"><img src="https://cdn-shop.adafruit.com/970x728/4757-07.jpg" width=60%></p></td>
<td><p align="center"><img src="https://cdn-shop.adafruit.com/970x728/4757-05.jpg" width=60%</p></td>
<td><p align="center"><img src="https://cdn-shop.adafruit.com/970x728/4757-01.jpg" width=60%</p></td>
</tr></table>

Folks can see the bottom of the device includes spots for 40 pin connections- perfect to connect directly to our Raspberry Pi.

# Other Kinds of Connections

But we have a few components that don't readily connect to the Raspberry Pi's 40 GPIO pins, or require specific wiring setups.

<p align="center"><img src="https://www.raspberrypi.com/documentation/computers/images/GPIO-Pinout-Diagram-2.png" width=80%</p>

In these situations, we use jumper wires to connect the Raspberry Pi's pins to other devices.

<p align="center"><img src="https://blog.sparkfuneducation.com/hubfs/EDU/BLOG%20Images/Jan%202018/JumperWire-Male-01-L.jpg" width=40%</p>

<blockquote>"Jumper wires are simply wires that have connector pins at each end, allowing them to be used to connect two points to each other without soldering." (<a href="https://blog.sparkfuneducation.com/what-is-jumper-wire">SparkFun Education, "What is a Jumper Wire?"</a>)</blockquote>

We can use jumper wires to connect to things like...

<table><tr><td><p align="center"><img src="https://cdn-learn.adafruit.com/assets/assets/000/039/519/medium640/raspberry_pi_button5.jpg?1487634684" width=40%></p></td>
<td><p align="center"><img src="https://cdn-learn.adafruit.com/assets/assets/000/039/524/medium640/raspberry_pi_dc4.jpg?1487634853" width=40%></p></td>
<td><p align="center"><img src="https://cdn-learn.adafruit.com/assets/assets/000/117/133/medium640/components_small-connections.jpg?1671137114" width=40%></p></td>
<td><p align="center"><img src="https://cdn-learn.adafruit.com/assets/assets/000/117/152/medium640/components_pi_a___b___2__3_pi-printer-to-header.jpg?1671212621" width=40%></p></td></tr>
<tr><td><p align="center">Buttons</p></td>
<td><p align="center">Power adapters</p></td>
<td><p align="center">Thermal Printers</p></td>
<td><p align="center">Raspberry Pi pins</p></td></tr></table>

# How to Use This Guide

This section of the notebook attempts to break down some of the Raspberry Pi peripherals and related materials folks could explore in their projects.
- The full inventory list is available online: [AirTable](https://airtable.com/appiyAMpeY6Bia0dZ/shrEDVeQg81olv2dz)

These materials and resources are organized based on possible uses or functions in your project. Each section shows possible resources and, in most cases, links to documentation or tutorials.

## Input

User input can take a variety of forms, from push buttons and joysticks to motion and touch. We could also use speech-to-text programs or other kind of image galleries to provide avenues for user input.

In making sense of these possibilities, folks can think about how they imagine the user interacting with different components, as well as what function or purpose different components might play within the larger system.
- *For example, a user pushes a button....and then what? Or, in a scenario where the user scrolls through and selects images, what images? What does the selection trigger?*

### Buttons

We have two main options for buttons: stand-alone buttons or buttons that are part of other systems. All of these button examples are momentary pushbuttons- they don't register an on/off setting, but the push can trigger some other kind of action.

- Arcade buttons (includes an LED light, multiple colors)
- Metal LED push buttons (can support RGB colors or light patterns)

<br>
<br>

<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/arcade-blue.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/arcade-clear.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/arcade-green.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/arcade-red.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/arcade-yellow.jpg?raw=true"></p></td></tr>
<tr><td colspan=5><p align="center">Arcade Buttons</p></td></tr>
<tr><td colspan=5><p align="center"><a href="https://projects.raspberrypi.org/en/projects/rpi-gpio-wiring-a-button">Wiring Diagram</a><br><a href="https://gpiozero.readthedocs.io/en/stable/recipes.html#button">Documentation</a><br><a href="https://learn.adafruit.com/products/3491/guides">Sample Projects</a></p></td></tr></table>

<br>
<br>

<table>
<tr><td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-push-button.jpg?raw=true" width=40%></p></td></tr>
<tr><td><p align="center">LED Metal Pushbutton</p></td></tr>
<tr><td colspan=5><p align="center"><a href="https://github.com/evanwill/poemBot/blob/master/poembot_leaf.png">Wiring Diagram</a><br><a href="https://gpiozero.readthedocs.io/en/stable/recipes.html#button">Documentation</a><br><a href="https://learn.adafruit.com/products/3350/guides">Sample Projects</a></p></td></tr></table>

<br>
<br>

The [`GPIO Zero`](https://gpiozero.readthedocs.io/en/stable/recipes.html#button) library includes resource for setting up and accepting input from a button. We can use that underlying logic to make the button part of more complex tasks or workflows.

```Python
from gpiozero import Button # import

button = Button(2) # set button wiring

while True: # respond to button input
  if button.is_pressed: # if button is pressed
    print("Button is pressed.")
  else: # if button is not pressed
    print("Button is not pressed.")
```

The second group of buttons are part of other add-ons or workflows. For these buttons, the wiring and button use is often handled by the larger add-on.

- Voice bonnet (single button; 4757)
  * Includes a single joystick button along with a speaker & microphone
- 1.3" TFT bonnet (joystick, two buttons; 4506)
  * Includes two buttons along with a joystick and small TFT display
- Sense Hat (button; 2738)
  * Includes a single button along with an 8 x 8 LED display (and other sensors)
- Mini TFT bonnet (two buttons; 4393)
  * Includes two buttons along with a small TFT display
- Pirate Audio (four buttons, 4451)
  * Includes four buttons along with a small display and speaker
- Unicorn HAT mini (four buttons, 4637)
  * Include s17 X 7 grid

<br>
<br>

<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/voice-bonnet.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4393-03.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4506-04.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2738-05.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4451-05.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4637-01.jpg?raw=true"></p></td></tr>
<tr><td><p align="center">Voice<br>Bonnet</p></td>
<td><p align="center">Mini TFT<br>Bonnet</p></td>
<td><p align="center">1.3" TFT<br>Bonnet</p></td>
<td><p align="center">Sense<br>Hat</p></td>
<td><p align="center">Pirate<br>Audio</p></td>
<td><p align="center">Unicorn<br>Hat Mini</p></td>
</tr>
<tr><td><p align="center"><a href="https://learn.adafruit.com/adafruit-voice-bonnet">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-mini-pitft-135x240-color-tft-add-on-for-raspberry-pi">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-1-3-color-tft-bonnet-for-raspberry-pi">Tutorial</a></p></td>
<td><p align="center"><a href="https://projects.raspberrypi.org/en/projects/getting-started-with-the-sense-hat">Tutorial</a></p></td>
<td><p align="center"><a href="https://github.com/pimoroni/pirate-audio">Documentation</a></p></td>
<td><p align="center"><a href="https://github.com/pimoroni/unicornhatmini-python">Documentation</a></p></td></tr></table>

<br>
<br>

Most of these add-ons use the [`digitalio` module](ttps://docs.circuitpython.org/en/latest/shared-bindings/digitalio/index.html), part of [`CircuitPython`](https://docs.circuitpython.org/en/latest/docs/index.html), to control button function.

```Python
# example for the voice bonnet; https://learn.adafruit.com/adafruit-voice-bonnet/python-bonnet-usage

import time, board # import statements
from digitalio import DigitalInOut, Direction, Pull

button = DigitalInOut(board.D17) # set button wiring
button.direction = Direction.INPUT # set input direction
button.pull = Pull.UP # set button direction

while True:
  if not button.value: # check if button is pressed
    print("Button pressed")
  time.sleep(0.01)
```

```Python
# example for the 1.3" TFT Bonnet; https://learn.adafruit.com/adafruit-1-3-color-tft-bonnet-for-raspberry-pi/python-setup
# Once it is running, push the buttons. The corresponding buttons should light up on the display

import time, random, board # all the import statements
from colorsys import hsv_to_rgb
from digitalio import DigitalInOut, Direction
from PIL import Image, ImageDraw, ImageFont
from adafruit_rgb_display import st7789

cs_pin = DigitalInOut(board.CE0) # display configuration
dc_pin = DigitalInOut(board.D25)
reset_pin = DigitalInOut(board.D24)
BAUDRATE = 24000000
spi = board.SPI()
disp = st7789.ST7789(
    spi,
    height=240,
    y_offset=80,
    rotation=180,
    cs=cs_pin,
    dc=dc_pin,
    rst=reset_pin,
    baudrate=BAUDRATE,
)

button_A = DigitalInOut(board.D5) # set up buttons and joystick directions
button_A.direction = Direction.INPUT

button_B = DigitalInOut(board.D6)
button_B.direction = Direction.INPUT

button_L = DigitalInOut(board.D27)
button_L.direction = Direction.INPUT

button_R = DigitalInOut(board.D23)
button_R.direction = Direction.INPUT

button_U = DigitalInOut(board.D17)
button_U.direction = Direction.INPUT

button_D = DigitalInOut(board.D22)
button_D.direction = Direction.INPUT

button_C = DigitalInOut(board.D4)
button_C.direction = Direction.INPUT

backlight = DigitalInOut(board.D26) # set up blacklight
backlight.switch_to_output()
backlight.value = True

width = disp.width # blank image for drawing
height = disp.height
image = Image.new("RGB", (width, height))

draw = ImageDraw.Draw(image) # clear display & draw object
draw.rectangle((0, 0, width, height), outline=0, fill=(255, 0, 0))
disp.image(image)
draw = ImageDraw.Draw(image)
draw.rectangle((0, 0, width, height), outline=0, fill=0)

udlr_fill = "#00FF00" # set up color functions
udlr_outline = "#00FFFF"
button_fill = "#FF00FF"
button_outline = "#FFFFFF"

fnt = ImageFont.truetype("/usr/share/fonts/truetype/dejavu/DejaVuSans.ttf", 30) # get font info

while True: # initiate button program
    up_fill = 0
    if not button_U.value:  # up pressed
        up_fill = udlr_fill
    draw.polygon(
        [(40, 40), (60, 4), (80, 40)], outline=udlr_outline, fill=up_fill
    )  # Up

    down_fill = 0
    if not button_D.value:  # down pressed
        down_fill = udlr_fill
    draw.polygon(
        [(60, 120), (80, 84), (40, 84)], outline=udlr_outline, fill=down_fill
    )  # down

    left_fill = 0
    if not button_L.value:  # left pressed
        left_fill = udlr_fill
    draw.polygon(
        [(0, 60), (36, 42), (36, 81)], outline=udlr_outline, fill=left_fill
    )  # left

    right_fill = 0
    if not button_R.value:  # right pressed
        right_fill = udlr_fill
    draw.polygon(
        [(120, 60), (84, 42), (84, 82)], outline=udlr_outline, fill=right_fill
    )  # right

    center_fill = 0
    if not button_C.value:  # center pressed
        center_fill = button_fill
    draw.rectangle((40, 44, 80, 80), outline=button_outline, fill=center_fill)  # center

    A_fill = 0
    if not button_A.value:  # left pressed
        A_fill = button_fill
    draw.ellipse((140, 80, 180, 120), outline=button_outline, fill=A_fill)  # A button

    B_fill = 0
    if not button_B.value:  # left pressed
        B_fill = button_fill
    draw.ellipse((190, 40, 230, 80), outline=button_outline, fill=B_fill)  # B button

    rcolor = tuple(int(x * 255) for x in hsv_to_rgb(random.random(), 1, 1))     # make a random color and print text

    draw.text((20, 150), "Hello World", font=fnt, fill=rcolor)
    rcolor = tuple(int(x * 255) for x in hsv_to_rgb(random.random(), 1, 1))
    draw.text((20, 180), "Hello World", font=fnt, fill=rcolor)
    rcolor = tuple(int(x * 255) for x in hsv_to_rgb(random.random(), 1, 1))
    draw.text((20, 210), "Hello World", font=fnt, fill=rcolor)

    disp.image(image) # Display the Image

    time.sleep(0.01)
```

### Joysticks

Joysticks are similar to buttons, but have a directional component. All of the joysticks folks might use for their projects are part of other add-ons. That said, there are [many other types of joysticks](https://www.adafruit.com/search?q=joystick) that could connect with the Raspberry Pi.

- Voice bonnet (single button; 4757)
  * Includes a single joystick button along with a speaker & microphone
- 1.3" TFT bonnet (joystick, two buttons; 4506)
  * Includes two buttons along with a joystick and small TFT display
- Sense Hat (button; 2738)
  * Includes a single button along with an 8 x 8 LED display (and other sensors)

<br>
<br>

<table><tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/voice-bonnet.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4506-04.jpg?raw=true" width=80%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2738-05.jpg?raw=true" width=90%></p></td></tr>
<tr><td><p align="center">Voice Bonnet</p></td>
<td><p align="center">1.3" TFT Bonnet</p></td>
<td><p align="center">Sense HAT</p></td></tr>
<tr><tr><td><p align="center"><a href="https://learn.adafruit.com/adafruit-voice-bonnet">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-1-3-color-tft-bonnet-for-raspberry-pi">Tutorial</a></p></td>
<td><p align="center"><a href="https://projects.raspberrypi.org/en/projects/getting-started-with-the-sense-hat">Tutorial</a><br><a href="https://sense-hat.readthedocs.io/en/latest/">Documentation</a></p></td></tr></table>

<br>
<br>

The previous section included sample programs for two of these devices. A sample program that uses the Sense Hat's joystick is included below.
- [Link to full tutorial](https://projects.raspberrypi.org/en/projects/getting-started-with-the-sense-hat/9)
- [Full `SenseHat` documentation](https://sense-hat.readthedocs.io/en/latest/)

```Python
# sense hat joystick example; https://projects.raspberrypi.org/en/projects/getting-started-with-the-sense-hat/9

from sense_hat import SenseHat # import
sense = SenseHat() # set up sense hat object

while True: # wait for joystick motion
  for event in sense.stick.get_events(): # get possible directions/events
    print(event.direction, event.action) # if joystick is moved, show direction and action
```

```Python
# another sense hat joystick example- this time output a specific message based on joystick movement
# https://projects.raspberrypi.org/en/projects/getting-started-with-the-sense-hat/9

from sense_hat import SenseHat # import statements
from time import sleep
sense = SenseHat() # sense hat object

e = (0, 0, 0) # LED matrix
w = (255, 255, 255)

sense.clear() # clear display

while True: # wait for joystick movement
  for event in sense.stick.get_events(): # Check if the joystick was pressed
    if event.action == "pressed": # if button is pressed, check direction
      if event.direction == "up":
        sense.show_letter("U")      # Up arrow
      elif event.direction == "down":
        sense.show_letter("D")      # Down arrow
      elif event.direction == "left":
        sense.show_letter("L")      # Left arrow
      elif event.direction == "right":
        sense.show_letter("R")      # Right arrow
      elif event.direction == "middle":
        sense.show_letter("M")      # Enter key

      sleep(0.5) # wait and clear the screen
      sense.clear()
```

```Python
# third sense hat program that ties function calls to joystick movement
# https://projects.raspberrypi.org/en/projects/getting-started-with-the-sense-hat/9

from sense_hat import SenseHat # import
sense = SenseHat() # object

# function definitions
def red():
  sense.clear(255, 0, 0)

def blue():
  sense.clear(0, 0, 255)

def green():
  sense.clear(0, 255, 0)

def yellow():
  sense.clear(255, 255, 0)

# assign functions to joystick directions
sense.stick.direction_up = red
sense.stick.direction_down = blue
sense.stick.direction_left = green
sense.stick.direction_right = yellow
sense.stick.direction_middle = sense.clear # use Enter/Return key to clear screen

while True: # keeps program running to accept joystick events
  pass
```

### Touch

Touch as an input can take a variety of forms- the Raspberry Pi add-ons folks might use involve haptic touch. With the exception of the Capacitive Touch HAT, all of our touch input options are part of other add-ons.

- Capacitive Touch HAT (drive for touch sensor electrodes; 2340)
  * NOTE- this add-on requires some soldering before we can connect it with the Raspberry Pi, which we should be able to do!
  * We can connect up to 6 electrodes (any conductive material) to use as inputs
  * Uses the [Adafruit MPR121 Library](https://docs.circuitpython.org/projects/mpr121/en/latest/index.html)
- Pimoroni Piano HAT (piano keys, 2695)
  * Includes 16 touch-sensitive buttons
  * Options to use alternate (i.e. non-piano) sounds or other audio sources
  * Uses [`pianohat`](https://github.com/pimoroni/Piano-HAT/tree/master) library
- Pimoroni Touch pHAT (six touch sensors; 3472)
  * NOTE- this add-on requires some soldering before we can connect it with the Raspberry Pi, which we should be able to do!
  * Six capacitive touch buttons with LEDs
  * Uses the [`touch-phat`](https://github.com/pimoroni/touch-phat) library


<br>
<br>

<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/3472-01.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2695-00.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2340-01.jpg?raw=true"></p></td></tr>
<tr><td><p align="center">Pimoroni Touch pHAT</p></td>
<td><p align="center">Pimoroni Piano HAT</p></td>
<td><p align="center">Capacitive Touch HAT</p></td></tr>
<tr><td><p align="center"><a href="https://github.com/pimoroni/touch-phat">Documentation</a></p></td>
<td><p align="center"><a href="https://github.com/pimoroni/piano-hat">Documentation</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-mpr121-12-key-capacitive-touch-sensor-breakout-tutorial/python-circuitpython">Documentation</a></p></td></tr></table>

```Python
# capacitive touch example that prints out a message when a touch input is activated
# https://docs.circuitpython.org/projects/mpr121/en/latest/examples.html

import time, board, busio, adafruit_mpr121 # import statements

i2c = busio.I2C(board.SCL, board.SDA) # Create I2C bus
mpr121 = adafruit_mpr121.MPR121(i2c) # Create MPR121 object

while True: # testing each input and printing when they're touched
    for i in range(12): # loop thorugh each input
        if mpr121[i].value: # will return message it sensor is touched
            print("Input {} touched!".format(i))
    time.sleep(0.25)  # Small delay to keep from spamming output messages.
```

```Python
# pianohat example that provides a simple keyboard
# https://github.com/pimoroni/Piano-HAT/blob/master/examples/simple-piano.py

import glob, os, re, signal, pygame, pianohat # import statements
from sys import exit


BANK = os.path.join(os.path.dirname(__file__), "sounds") # set sound files

NOTE_OFFSET = 3 # keyboard settings
FILETYPES = ['*.wav', '*.ogg']
samples = []
files = []
octave = 0
octaves = 0

pygame.mixer.pre_init(44100, -16, 1, 512) # sound settings
pygame.mixer.init()
pygame.mixer.set_num_channels(32)

patches = glob.glob(os.path.join(BANK, '*')) # sound file settings
patch_index = 0

"""
# error message if files can't be found
if len(patches) == 0:
    exit("Couldn't find any .wav files in: {}".format(BANK))
"""

def natural_sort_key(s, _nsre=re.compile('([0-9]+)')): # function to order keys
    return [int(text) if text.isdigit() else text.lower() for text in re.split(_nsre, s)]


def load_samples(patch): # function to load audio files
    global samples, files, octaves, octave
    files = []
    print('Loading Samples from: {}'.format(patch))
    for filetype in FILETYPES:
        files.extend(glob.glob(os.path.join(patch, filetype)))
    files.sort(key=natural_sort_key)
    octaves = len(files) / 12
    samples = [pygame.mixer.Sound(sample) for sample in files]
    octave = int(octaves / 2)


pianohat.auto_leds(True) # LED light settings


def handle_note(channel, pressed): # function to handle key action
    channel = channel + (12 * octave)
    if len(samples) > 13:
        channel += NOTE_OFFSET
    if channel < len(samples) and pressed:
        print('Playing Sound: {}'.format(files[channel]))
        samples[channel].play(loops=0)


def handle_instrument(channel, pressed): # function to set instrument
    global patch_index
    if pressed:
        patch_index += 1
        patch_index %= len(patches)
        print('Selecting Patch: {}'.format(patches[patch_index]))
        load_samples(patches[patch_index])


def handle_octave_up(channel, pressed): # functions to handle octave changes
    global octave
    if pressed and octave < octaves:
        octave += 1
        print('Selected Octave: {}'.format(octave))


def handle_octave_down(channel, pressed):
    global octave
    if pressed and octave > 0:
        octave -= 1
        print('Selected Octave: {}'.format(octave))


pianohat.on_note(handle_note) # function calls when keys are pressed
pianohat.on_octave_up(handle_octave_up)
pianohat.on_octave_down(handle_octave_down)
pianohat.on_instrument(handle_instrument)

load_samples(patches[patch_index]) # load audio files

signal.pause() # pause audio input
```

```Python
# touch-phat example that lights up when a button is pressed and prints the button name
# https://github.com/pimoroni/touch-phat/blob/master/examples/buttons.py

import signal, time, touchphat # import statements

for pad in ['Back','A','B','C','D','Enter']: # for loop that sets buttons
    touchphat.set_led(pad, True)
    time.sleep(0.1)
    touchphat.set_led(pad, False)
    time.sleep(0.1)

@touchphat.on_touch(['Back','A','B','C','D','Enter']) # function to get touch inputs
def handle_touch(event):
    print(event.name)

signal.pause() # pause input signal
```

We also have two HDMI touch screen display that could take a variety of different touch inputs.

<br>
<br>
<table><tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2407-12.jpg?raw=true" width=90%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2232-07.jpg?raw=true" width=90%></p></td></tr>

<tr><td><p align="center">7" HDMI<br>Touch Screen</p></td>
<td><p align="center">5" HDMI<br>Touch Screen</p></td></tr>

<tr><td colspan=2><p align="center"><a href="https://learn.adafruit.com/hdmi-uberguide/2395-7-display-w-touchscreen-1024x600">Documentation</a></p></td>
</tr></table>  

### Motion

For our purposes, we're separating motion as an input from the kinds of tasks or workflows that might involve motors or movement (see the `Motion` subsection under `Output`).
- That said, we could connect the Sense HAT's gyroscope with the other kinds of motion/movement to trigger certain actions based on movement.

The lone Pi add-on we have that senses motion or movement is the Sense HAT, which includes a gyroscope, accelerometer, and magnetometer (2738).
- [For more on the Sense HAT's inertial measurement chip](https://projects.raspberrypi.org/en/projects/getting-started-with-the-sense-hat/8)
- A gyroscope detects momentum and rotation
- An accelerometer measures acceleration forces
- An magnometer works like a compas, detecting the earth's magnetic fields

<br>
<br>
<table><tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2738-05.jpg?raw=true" width=40%></p></td></tr>
<tr><td><p align="center">Sense HAT</p></td></tr>
<tr><td><p align="center"><a href="https://projects.raspberrypi.org/en/projects/getting-started-with-the-sense-hat">Tutorial</a></p></td></tr></table>

```Python
# sense hat example that uses the accelerometer to detect motion
# https://projects.raspberrypi.org/en/projects/getting-started-with-the-sense-hat/8

from sense_hat import SenseHat # import statement
sense = SenseHat() # object

sense.show_letter("J") # show letter J

while True: # determine acceleration values
	acceleration = sense.get_accelerometer_raw()
	x = acceleration['x']
	y = acceleration['y']
	z = acceleration['z']

	x=round(x, 0)
	y=round(y, 0)
	z=round(z, 0)

	print("x={0}, y={1}, z={2}".format(x, y, z)) # output message

	if x  == -1:   # Update the rotation of the display depending on which way up the Sense HAT is
	  sense.set_rotation(180)
	elif y == 1:
	  sense.set_rotation(90)
	elif y == -1:
	  sense.set_rotation(270)
	else:
	  sense.set_rotation(0)
```

```Python
# sense hat example that outputs a poem when the device is shaken
# based on: https://projects.raspberrypi.org/en/projects/getting-started-with-the-sense-hat/8

from sense_hat import SenseHat # import statement
import time, csv, textwrap, random
sense = SenseHat() # object

with open('filtered_subset.csv', encoding='utf-8') as csvPoems: # load poems
    allPoems = list(csv.reader(csvPoems, delimiter=','))

def poem(): # function to show random poem
    #get a random poem
    randPoem = random.choice(allPoems)
    s.show_message(randPoem[0])
    s.show_message(randPoem[2])
    for line in randPoem[1].splitlines():
        s.show_message(line)

while True: # detect acceleration level
    acceleration = sense.get_accelerometer_raw()
    x = acceleration['x']
    y = acceleration['y']
    z = acceleration['z']

    x = abs(x)
    y = abs(y)
    z = abs(z)

    if x > 1 or y > 1 or z > 1:
        poem()
    else:
        sense.clear()
```


### Text

The most straightforward option for text input is via a traditional keyboard. We have wired and wireless options of various sizes. In a scenario where the program involves some kind of text input, keyboards are a solid option.

- Keyboard
  * Regular keyboard (wireless/bluetooth connection)
  * Mini keyboard (bluetooth)

The next option for text input would be via a touchscreen- we have two touch screens available for folks to use as part of their program. In this scenario, we might need to incorporate a [virtual keyboard](https://github.com/AbhiK002/virtual-keyboard) as part of our program.

- HDMI touch screen
  * 5" and 7" touchscreens that could probably run some kind of app or interface with a keyboard

Another option for text input would be via the TFT screens, which we could probably rig up the TFT screens to have some kind of text selection or keyboard style interface (although it might not be super user friendly).

We could also use some of the touch sensors in the previous section as a keyboard input, possibly emulating an old cell phone keypad, or a rotary phone.

<br>
<br>
<table><tr>
<td><p align="center"><img src="https://m.media-amazon.com/images/I/61w09t-kNuL.jpg" width=80%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/rp-keyboard.jpg?raw=true" width=80%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2407-12.jpg?raw=true" width=90%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2232-07.jpg?raw=true" width=90%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4506-04.jpg?raw=true" width=90%></p></td></tr>

<tr><td><p align="center">Keyboard</p></td>
<td><p align="center">Mini Wireless<br> Keyboard</p></td>
<td><p align="center">7" HDMI<br>Touch Screen</p></td>
<td><p align="center">5" HDMI<br>Touch Screen</p></td>
<td><p align="center">1.3" TFT<br>Bonnet</p></td></tr>

<tr><td></td><td></td>
<td><p align="center"><a href="https://learn.adafruit.com/hdmi-uberguide/2395-7-display-w-touchscreen-1024x600">Documentation</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/hdmi-uberguide/2395-7-display-w-touchscreen-1024x600">Documentation</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-1-3-color-tft-bonnet-for-raspberry-pi">Documentation</a></p></td>
</tr></table>  

```Python
# example of Python's input function that could use a physical or virtual keyboard

# start program
print("We're going to create a mad lib love poem!")

# user inputs
verb1 = input("Enter a verb: ")
noun1 = input("Enter a noun: ")
adj1 = input("Enter an adjective: ")
noun2 = input("Enter another noun: ")
adj2 = input("Enter another adjective: ")
noun3 = input("Enter another noun: ")

# poem madlib
print("She " + verb1 + " in beauty, like the " + noun1 + "\n Of " + adj1 + " " + noun2 + " and " + adj2 + " " + noun3)
```

### Speech / Sound

While we only have one Pi-specific add-on that includes a microphone, we have othre microphone options and any device that includes a microphone would let us accept sound as an input, or run a speech-to-text program.

- Voice Bonnet (microphone, button, speaker; 4757)
  * Includes a single joystick button along with a speaker & microphone

<br>
<br>
<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/voice-bonnet.jpg?raw=true" width=60%></p></td></tr>
<tr><td><p align="center">Voice Bonnet</p></td>
</tr>
<tr><td><p align="center"><a href="https://github.com/pimoroni/pirate-audio">Documentation</a></p></td></tr></table>
<br>
<br>

We have other USB microphone options, through the [Navari Family Center for Digital Scholarship's tech lending collection](https://libcal.library.nd.edu/reserve/equipment/reservable-equipment):

<br>
<br>
<table>
<tr>
<td><p align="center"><img src="https://libapps.s3.amazonaws.com/customers/2463/images/nessie-microphone.jpg" width=80%></p></td>
<td><p align="center"><img src="https://libapps.s3.amazonaws.com/customers/2463/images/raspberry-microphone.jpg" width=40%></p></td>
<td><p align="center"><img src="https://libapps.s3.amazonaws.com/customers/2463/images/yeti-microphone.jpg"></p></td></tr>
<tr><td><p align="center">Blue Nessie</p></td>
<td><p align="center">Blue Raspberry</p></td>
<td><p align="center">Yeti Nano</p></td></tr></table>

<br>
<br>

First, we would need to make sure the Raspberry Pi detects our audio input device.
- [General tutorial on Raspberry Pi audio](https://projects.raspberrypi.org/en/projects/raspberry-pi-using/4)

The Adafruit Voice Bonnet includes a specialized program for this: 
- [`blinka` setup](https://learn.adafruit.com/adafruit-voice-bonnet/blinka-setup)
- [audio card setup](https://learn.adafruit.com/adafruit-voice-bonnet/audio-setup)

For other microphone inputs, we can use `alsamixer` to set audio levels and other audio settings.
- [More info on `alsamixer`](http://cagewebdev.com/raspberry-pi-getting-audio-working/)

We can work with audio in Python, a few key libraries:
- [`pyaudio`](https://pypi.org/project/PyAudio/) handles audio inputs
- [`SpeechRecognition`](https://pypi.org/project/SpeechRecognition/) handles speech-to-text conversion
- [`pyttsx3`](https://pyttsx3.readthedocs.io/en/latest/) handles text-to-speech conversion

Let's see some of those workflows in action: 

```Python
# speech recognition example

import speech_recognition as sr # import statements
import pyaudio

# settings
p = pyaudio.PyAudio()

"""
# get list of device microphones
for m in enumerate(sr.Microphone.list_microphone_names()): # get microphones
    print(m) 
"""

for m in enumerate(sr.Microphone.list_microphone_names()): # get microphones
    print(m) 
    
# initialize the recognizer
r = sr.Recognizer()

# use the microphone as source for input
with sr.Microphone(device_index=5) as source:
    print("Speak something...")
    r.energy_threshold = 4000  # adjust this value according to your environment
    r.pause_threshold = 1  # adjust this value depending on how long you want to wait for silence
    audio = r.listen(source, timeout=5)

    try:
        text = r.recognize_google(audio)
        print("You said: ", text)
    except sr.UnknownValueError:
        print("Google Speech Recognition could not understand audio")
    except sr.RequestError as e:
        print("Could not request results from Google Speech Recognition service; {0}".format(e))
```

We could use that text input, along with natural language processing workflows, to find or create a poem that includes a similar phrase or related terms.

### Image

We have a few options for using an image or visual information as an input.

#### Camera

One option would be to use Raspberry Pi's camera module (5659) to take a user image.

<br>
<br>
<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/rp-camera.jpg?raw=true" width=30%></p></td></tr>
<tr><td><p align="center">Camera</p></td></tr>
<tr><td><p align="center"><a href="https://www.raspberrypi.com/documentation/accessories/camera.html">Documentation</a><br><a href="https://projects.raspberrypi.org/en/projects/getting-started-with-picamera">Tutorial</a></p></td></tr></table>

```Python
# taking a picture
from picamera import PiCamera # import statements
from time import sleep

camera = PiCamera() # camera object
camera.start_preview() # preview camera image
sleep(5) # sleep interval
camera.capture("image.jpg") # take image and save to file
camera.stop_preview() # stop preview
```

We could run an emotion detection program on the image using Python's [`deepface` library](https://www.edlitera.com/en/blog/posts/emotion-detection-in-images) to select a poem that includes similar descriptive or affective language.
- NOTE: Part of `deepface`'s functionality includes race/ethnicity and gender detection, which is an application of these workflows that has been shown to be highly problematic and innacurate. Emotion detection is also fraught, and not immune to some of these same issues.

```Python
# emotion detection analysis

from deepface import DeepFace # import

face_analysis = DeepFace.analyze(img_path = "image.jpg") # analyze image

data = face_analysis[0]['emotion'] # isolate emotion data

emotions = [] # empty list for emotions

for key, value in data.items(): # iterate over emotions
  if value > 1: # test value to see if emotion is present
    emotions.append(key) # if emotion is present, add to list
  else:
    continue

emotions # show emotions
```

#### Other Displays

But we could also do something with scrolling images or image selection on one of the LCD, LED, or TFT displays, particularly the display options that include a button (or could integrate with a button).

##### TFTs

- 1.3" TFT bonnet (joystick, two buttons; 4506)
  * Includes two buttons along with a joystick and small TFT display)
- Mini TFT bonnet (two buttons; 4393)
  * Includes two buttons along with a small TFT display
- Mini TFT HAT (display, 2315)
  * Includes a 2.2" display

<br>
<br>

<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2315-04.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4393-03.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4506-04.jpg?raw=true"></p></td></tr>
<tr><td><p align="center">2.2" TFT HAT</p></td>
<td><p align="center">1.3" TFT Bonnet</p></td>
<td><p align="center">Mini TFT Bonnet</p></td></tr>
<tr><td><p align="center"><a href="https://learn.adafruit.com/adafruit-2-2-pitft-hat-320-240-primary-display-for-raspberry-pi">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-1-3-color-tft-bonnet-for-raspberry-pi">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-2-2-pitft-hat-320-240-primary-display-for-raspberry-pi">Tutorial</a></p></td><tr></table>
<br>
<br>

We've already seen some examples of the TFT buttons and joystick in action- we could modify those programs to interact with image selection.

##### LCDs
- Blue 16 x 2 LCD (1115)
- Purple 16 x 2 LCD (1109)
<br>
<br>
<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/1115-00.jpg?raw=true" width=80%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/1109-00.jpg?raw=true" width=80%></p></td></tr>
<tr><td><p align="center">Blue 16 x 2 LCD</p></td>
<td><p align="center">Purple 16 x 2 LCD</p></td></tr>
<tr><td colspan=2><p align="center"><a href="https://learn.adafruit.com/i31fl3731-16x9-charliplexed-pwm-led-driver">Tutorial</a></p></td></tr></table>

<br>
<br>

This kind of program would involve an external button that interacts with the LCD display.

##### CharliePlex LED Matrix

<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-charlieplex-blue.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-charlieplex-cool-white.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-charlieplex-green.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-charlieplex-red.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-charlieplex-warm-white.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-charlieplex-yellow.jpg?raw=true"></p></td></tr>
<tr><td><p align="center">Blue</p></td>
<td><p align="center">Cool <br>White</p></td>
<td><p align="center">Green</p></td>
<td><p align="center">Red</p></td>
<td><p align="center">Warm <br>White</p></td>
<td><p align="center">Yellow</p></td></tr>
<tr><td colspan=6><p align="center">9 x 16 CharliePlexed LED Matrix</p></td></tr>
<tr><td colspan=6><p align="center"><a href="https://learn.adafruit.com/adafruit-16x2-character-lcd-plus-keypad-for-raspberry-pi">Tutorial</a></p></td></tr></table>

##### Other LEDs
- Unicorn HAT (16 x 16 grid, 3580)
- Unicorn HAT mini (17 X 7 grid, 4637)
- Sense HAT (8 x 8 grid, 2738)

<br>
<br>

<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/3580-03.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4637-01.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2738-05.jpg?raw=true"></p></td></tr>
<tr><td><p align="center">16 x 16 Unicorn<br>HAT</p></td>
<td><p align="center">17 x 7 Unicorn<br>HAT Mini</p></td>
<td><p align="center">8 x 8 Sense HAT</p></td></tr>
<tr><td><p align="center"><a href="https://github.com/pimoroni/unicorn-hat-hd">Documentation</a></p></td>
<td><p align="center"><a href="https://github.com/pimoroni/unicornhatmini-python">Documentation</a></p></td>
<td><p align="center"><a href="https://projects.raspberrypi.org/en/projects/getting-started-with-the-sense-hat">Tutorial</a></p></td></tr></table>

<br>
<br>

This kind of program would involve a button that interacts with the LED displays. We could show pixel art images, rotate through solid-color displays, show color gradiants. Lots of options!

##### HDMI Displays

We could also maybe explore some kind of drawing or image interface with the HDMI touchscreens.
- 5" and 7" touchscreen displays

<br>
<br>
<table><tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2407-12.jpg?raw=true" width=90%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2232-07.jpg?raw=true" width=90%></p></td></tr>

<tr><td><p align="center">7" HDMI<br>Touch Screen</p></td>
<td><p align="center">5" HDMI<br>Touch Screen</p></td></tr>

<tr><td colspan=2><p align="center"><a href="https://learn.adafruit.com/hdmi-uberguide/2395-7-display-w-touchscreen-1024x600">Documentation</a></p></td>
</tr></table>  

## Output

User input can take a variety of forms, from push buttons and joysticks to motion and touch. We could also use speech-to-text programs or other kind of image galleries to provide avenues for user input.

In making sense of these possibilities, folks can think about how they imagine the user interacting with different components, as well as what function or purpose different components might play within the larger system.
- *For example, a user pushes a button....and then what? Or, in a scenario where the user scrolls through and selects images, what images? What does the selection trigger?*

### LCD

- Blue 16 x 2 LCD (1115)
- Purple 16 x 2 LCD (1109)

<br>
<br>
<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/1115-00.jpg?raw=true" width=80%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/1109-00.jpg?raw=true" width=80%></p></td></tr>
<tr><td><p align="center">Blue 16 x 2 LCD</p></td>
<td><p align="center">Purple 16 x 2 LCD</p></td></tr>
<tr><td colspan=2><p align="center"><a href="https://learn.adafruit.com/i31fl3731-16x9-charliplexed-pwm-led-driver">Tutorial</a></p></td></tr></table>

<br>
<br>

This kind of output could show text scrolling on the display, using the [`CharLCD` library](https://learn.adafruit.com/adafruit-16x2-character-lcd-plus-keypad-for-raspberry-pi/python-usage).

```Python
# LCD output example

import board, busio, adafruit_character_lcd.character_lcd_rgb_i2c as character_lcd # iport statements

lcd_columns = 16 # configure display
lcd_rows = 2
i2c = busio.I2C(board.SCL, board.SDA)
lcd = character_lcd.Character_LCD_RGB_I2C(i2c, lcd_columns, lcd_rows)

# poem text
frost = """
Two roads diverged in a yellow wood,
And sorry I could not travel both
And be one traveler, long I stood
And looked down one as far as I could
To where it bent in the undergrowth;

Then took the other, as just as fair,
And having perhaps the better claim,
Because it was grassy and wanted wear;
Though as for that the passing there
Had worn them really about the same,

And both that morning equally lay
In leaves no step had trodden black.
Oh, I kept the first for another day!
Yet knowing how way leads on to way,
I doubted if I should ever come back.

I shall be telling this with a sigh
Somewhere ages and ages hence:
Two roads diverged in a wood, and I—
I took the one less traveled by,
And that has made all the difference.
"""

"""
# other arguments we could use to specify rate and voice
rate = engine.getProperty('rate')
voice = engine.getProperty('voice')
engine.setProperty('voice', 'english_rp+f3')
engine.setProperty('rate', rate+100)
"""
lcd.color = [50, 0, 50] # set color

lcd.text_direction = lcd.LEFT_TO_RIGHT # set text direction

lcd.message = "Robert Frost" # show poet
lcd.clear() # clear screen
lcd.message = "The Road Less Traveled" # show title
lcd.clear() # clear screen

lcd.message = frost # set message
for i in range(len(frost)): # scroll poem message
  time.sleep(0.5)
  lcd.move_left() 

lcd.color = [0,0,0] # turn off lights
lcd.clear() # clear screen
```

### Charlieplex LED Matrix


<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-charlieplex-blue.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-charlieplex-cool-white.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-charlieplex-green.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-charlieplex-red.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-charlieplex-warm-white.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-charlieplex-yellow.jpg?raw=true"></p></td></tr>
<tr><td><p align="center">Blue</p></td>
<td><p align="center">Cool <br>White</p></td>
<td><p align="center">Green</p></td>
<td><p align="center">Red</p></td>
<td><p align="center">Warm <br>White</p></td>
<td><p align="center">Yellow</p></td></tr>
<tr><td colspan=6><p align="center">9 x 16 CharliePlexed LED Matrix</p></td></tr>
<tr><td colspan=6><p align="center"><a href="https://learn.adafruit.com/adafruit-16x2-character-lcd-plus-keypad-for-raspberry-pi">Tutorial</a></p></td></tr></table>

<br>
<br>

This kind of output could involve varying color intensity, lighting individual LEDs, or other kinds of single-color displays.

### Other LEDs

- Unicorn HAT (16 x 16 grid, 3580)
- Unicorn HAT mini (17 X 7 grid, 4637)
- Sense HAT (8 x 8 grid, 2738)
- LED strips (two versions; 3811, 2537)

<br>
<br>

<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/3580-03.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4637-01.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2738-05.jpg?raw=true"></p></td></tr>
<tr><td><p align="center">16 x 16 Unicorn<br>HAT</p></td>
<td><p align="center">17 x 7 Unicorn<br>HAT Mini</p></td>
<td><p align="center">8 x 8 Sense HAT</p></td></tr>
<tr><td><p align="center"><a href="https://github.com/pimoroni/unicorn-hat-hd">Documentation</a></p></td>
<td><p align="center"><a href="https://github.com/pimoroni/unicornhatmini-python">Documentation</a></p></td>
<td><p align="center"><a href="https://projects.raspberrypi.org/en/projects/getting-started-with-the-sense-hat">Tutorial</a></p></td></tr></table>

<br>
<br>

This kind of output could involve varying color intensity, lighting individual LEDs, or other kinds of multi-color RGB displays.

```Python
# an example that shows how the sense hat could display pixel art

from sense_hat import SenseHat # import statements
import os, time, random
from os import listdir

s = SenseHat() # sense hat object
s.clear() # clear display

colors = { # dict with colors
  'green': (0, 255, 0),
  'yellow': (255, 255, 0),
  'blue': (0, 0, 255),
  'red': (255, 0, 0),
  'orange': (255,140,0),
  'purple': (128,0,128),
  'brown': (139,69,19),
  'white': (255,255,255),
  'nothing': (0,0,0),
  'pink': (255,105, 180),
  'ndBlue': (12, 35, 64),
  'ndYellow': (174, 145, 66),
  'ndGreen': (10, 132, 61),
  }

# create list of images
def rHeart():
    P = colors['red']
    O = colors['nothing']
    terms = ["love", "affection", "adore", "yearn"]
    logo = [
    O, O, O, O, O, O, O, O,
    O, P, P, O, P, P, O, O,
    P, P, P, P, P, P, P, O,
    P, P, P, P, P, P, P, O,
    O, P, P, P, P, P, O, O,
    O, O, P, P, P, O, O, O,
    O, O, O, P, O, O, O, O,
    O, O, O, O, O, O, O, O,
    ]
    return logo
 
 
def yHeart():
    P = colors['yellow']
    O = colors['nothing']
    terms = ["friend", "friendship", "companion", "company"]
    logo = [
    O, O, O, O, O, O, O, O,
    O, P, P, O, P, P, O, O,
    P, P, P, P, P, P, P, O,
    P, P, P, P, P, P, P, O,
    O, P, P, P, P, P, O, O,
    O, O, P, P, P, O, O, O,
    O, O, O, P, O, O, O, O,
    O, O, O, O, O, O, O, O,
    ]
    return logo    

def pHeart():
    terms = ["loss", "grief", "sorrow", "mourn"]
    P = colors['purple']
    O = colors['nothing']
    logo = [
    O, O, O, O, O, O, O, O,
    O, P, P, O, P, P, O, O,
    P, P, P, P, P, P, P, O,
    P, P, P, P, P, P, P, O,
    O, P, P, P, P, P, O, O,
    O, O, P, P, P, O, O, O,
    O, O, O, P, O, O, O, O,
    O, O, O, O, O, O, O, O,
    ]
    return logo

def smile():
  terms = ["happy", "smile", "cheer"]
  y = colors['yellow']
  b = colors['nothing']
  logo = [
		y, y, y, y, y, y, y, y,
		y, y, y, y, y, y, y, y,
		y, b, b, y, y, b, b, y,
		y, b, b, y, y, b, b, y,
		y, y, y, y, y, y, y, y,
		y, b, b, y, y, b, b, y,
		y, y, y, b, b, y, y, y,
		y, y, y, y, y, y, y, y
		]
  return logo

def tree():
  terms = ["nature", "woods", "leaf", "leaves", "earth", "land"]
  b = colors['blue']
  r = colors['brown']
  g = colors['green']
  logo = [
	b, g, g, g, g, g, b, b,
	g, g, g, g, g, g, g, b,
	g, g, g, g, g, g, g, b,
	b, g, g, g, g, g, b, b,
	b, b, r, r, r, b, b, b,
	b, b, r, r, r, b, b, b,
	b, b, r, r, r, b, b, b,
	g, g, g, g, g, g, g, g
	]
  return logo

images = [rHeart, yHeart, pHeart, smile, tree] # gallery of images
count = 0 # initialize count

while True: # while statement to cycle through images
	s.set_pixels(images[count % len(images)]())
	time.sleep(1.2)
	count += 1
```

### TFT

- 1.3" TFT bonnet (joystick, two buttons; 4506)
  * Includes two buttons along with a joystick and small TFT display)
- Mini TFT bonnet (two buttons; 4393)
  * Includes two buttons along with a small TFT display
- Mini TFT HAT (display, 2315)
  * Includes a 2.2" display

<br>
<br>

<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2315-04.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4393-03.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4506-04.jpg?raw=true"></p></td></tr>
<tr><td><p align="center">2.2" TFT HAT</p></td>
<td><p align="center">1.3" TFT Bonnet</p></td>
<td><p align="center">Mini TFT Bonnet</p></td></tr>
<tr><td><p align="center"><a href="https://learn.adafruit.com/adafruit-2-2-pitft-hat-320-240-primary-display-for-raspberry-pi">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-1-3-color-tft-bonnet-for-raspberry-pi">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-2-2-pitft-hat-320-240-primary-display-for-raspberry-pi">Tutorial</a></p></td><tr></table>
<br>
<br>

This kind of program could involve text, images, or other kinds of displays. Our earlier TFT sample programs included examples of display functionality.

### Sound
- Voice bonnet (single button; 4757)
  * Includes a single joystick button along with a speaker & microphone
- Pirate Audio (four buttons, speaker, display; 4451)
  * Includes four buttons along with a display & speaker
  * No longer supports a Spotify integration, but can be used as an audio server through [Mopidy](https://mopidy.com/)
- Speaker bonnet (3346)
  * NOTE- this add-on requires some soldering before we can connect it with the Raspberry Pi, which we should be able to do!
  * We could connect this add-on to other speakers or audio output devices.
- Stereo enclosed speaker set (two sets available; 1669)
  * These speakers would require some wiring, but would plug right into the speaker bonnet.
- 3" speakers (two available, 1313)
  *   We'd have to do some wiring or soldering, but we could connect these speakers to a Raspberry Pi.

<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/voice-bonnet.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4451-05.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4757-01.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/1669-06.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/adafruit-1313.jpg?raw=true"></p></td></tr>
<tr><td><p align="center">Voice Bonnet</p></td>
<td><p align="center">Pirate Audio</p></td>
<td><p align="center">Speaker Bonnet</p></td>
<td><p align="center">Stereo Enclosed<br>Speaker Set</p></td>
<td><p align="center">3" Speakers</p></td>
</tr>
<tr><td><p align="center"><a href="https://learn.adafruit.com/adafruit-voice-bonnet">Tutorial</a></p></td>
<td><p align="center"><a href="https://github.com/pimoroni/pirate-audio">Documentation</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-speaker-bonnet-for-raspberry-pi">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-speaker-bonnet-for-raspberry-pi">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-speaker-bonnet-for-raspberry-pi">Tutorial</a></p></td>
</tr></table>

<br><br>

We hadn'considered headphones as an option for audio output, and a shared shet of headphones might present some hygene concerns. But there's no reason we couldn't explore this option!

The Raspberry Pi model folks are working with does support Bluetooth, so it's feasible folks could have a program that connects to someone's personal wireless headphones. A couple tutorials are linked below.
- [Bluetooth Headphones Raspberry Pi Connections](https://peppe8o.com/fixed-connect-bluetooth-headphones-with-your-raspberry-pi/)
- [Instructables' tutorial](https://www.instructables.com/Make-Bluetooth-Device-Work-With-Raspberry-Pi/)


<br>
<br>

In general, for audio workflows, we would need to make sure the Raspberry Pi detects our audio output device.
- [General tutorial on Raspberry Pi audio](https://projects.raspberrypi.org/en/projects/raspberry-pi-using/4)

The Adafruit Voice Bonnet includes a specialized program for this: 
- [`blinka` setup](https://learn.adafruit.com/adafruit-voice-bonnet/blinka-setup)
- [audio card setup](https://learn.adafruit.com/adafruit-voice-bonnet/audio-setup)

For other outputs, we can use `alsamixer` to set audio levels and other audio settings.
- [More info on `alsamixer`](http://cagewebdev.com/raspberry-pi-getting-audio-working/)

We can work with audio in Python, a few key libraries:
- [`pyaudio`](https://pypi.org/project/PyAudio/) handles audio inputs
- [`SpeechRecognition`](https://pypi.org/project/SpeechRecognition/) handles speech-to-text conversion
- [`pyttsx3`](https://pyttsx3.readthedocs.io/en/latest/) handles text-to-speech conversion

We've seen an example of the speech-to-text workflow. Let's look at the other direction (text-to-speech).

```Python
# text to speech example

import pyttsx3, pyaudio # import statements

engine = pyttsx3.init() # initialize engine

# poem text
frost = """
Two roads diverged in a yellow wood,
And sorry I could not travel both
And be one traveler, long I stood
And looked down one as far as I could
To where it bent in the undergrowth;

Then took the other, as just as fair,
And having perhaps the better claim,
Because it was grassy and wanted wear;
Though as for that the passing there
Had worn them really about the same,

And both that morning equally lay
In leaves no step had trodden black.
Oh, I kept the first for another day!
Yet knowing how way leads on to way,
I doubted if I should ever come back.

I shall be telling this with a sigh
Somewhere ages and ages hence:
Two roads diverged in a wood, and I—
I took the one less traveled by,
And that has made all the difference.
"""

"""
# other arguments we could use to specify rate and voice
rate = engine.getProperty('rate')
voice = engine.getProperty('voice')
engine.setProperty('voice', 'english_rp+f3')
engine.setProperty('rate', rate+100)
"""

engine.say(frost) # program to read text
engine.runAndWait()
```

### Screen

- 5" and 7" HDMI screens

We could use the HDMI screens in a few different ways- text or image output are good starting points.

<br>
<br>
<table><tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2407-12.jpg?raw=true" width=90%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2232-07.jpg?raw=true" width=90%></p></td></tr>

<tr><td><p align="center">7" HDMI<br>Touch Screen</p></td>
<td><p align="center">5" HDMI<br>Touch Screen</p></td></tr>

<tr><td colspan=2><p align="center"><a href="https://learn.adafruit.com/hdmi-uberguide/2395-7-display-w-touchscreen-1024x600">Documentation</a></p></td>
</tr></table>  

### Print

- Mini thermal receipt printers (3)
  * Prof. Kilbane has one
  * One's in the wood crate prototype
  * Third one is in the CDS
- Tiny thermal receipt printer (1 or 2?)
  * CDS

<br>
<br>
<table><tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/mini-printer.jpg?raw=true" width=80%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/tiny-printer.jpg?raw=true" width=60%></p></td></tr>

<tr><td><p align="center">Mini Thermal Printer</p></td>
<td><p align="center">Tiny Thermal Printer</p></td></tr>

<tr><td colspan=2><p align="center"><a href="https://learn.adafruit.com/networked-thermal-printer-using-cups-and-raspberry-pi/overview">Documentation</a></p></td>
</tr></table>  

The poemBot project that originally inspired this course used a thermal printer, which printed a Shakespeare sonnet when a button was pressed.

<br>
<p align="center"><img src="https://github.com/evanwill/poemBot/blob/master/images/poemBot_inside.JPG?raw=true" width=80%></p>
<br>
<br>

We have a few of those printers folks can work with as part of their designs. These printers can output images or text. A very basic example of how we can control the printer in Python.

```Python
from __future__ import print_function # import statements
import RPi.GPIO as GPIO
import subprocess, time, socket, csv, textwrap, random, board, busio, serial
from thermalPrinter import *
import adafruit_thermal_printer

# printer setup
ThermalPrinter = adafruit_thermal_printer.get_printer_class(1.00)
uart = serial.Serial("/dev/serial0", baudrate=19200, timeout=3000)
printer = ThermalPrinter(uart)
printer.warm_up()

# load poems from file
with open('filtered_subset.csv', encoding='utf-8') as csvPoems:
    allPoems = list(csv.reader(csvPoems, delimiter=','))

def printPoem(): # function to print a random poem
    randPoem = random.choice(allPoems) #get a random poem

    wrappedTitle = textwrap.fill(randPoem[0], width=32) # format printer output
    wrappedAuthor = textwrap.fill(randPoem[2], width=32)
    wrappedPoem = ""
    for line in randPoem[1].splitlines():
        wrappedLine = textwrap.fill(line, width=32, subsequent_indent="    ")
        wrappedPoem += wrappedLine +"\n"
    
    # print the poem
    printer.size = adafruit_thermal_printer.SIZE_MEDIUM
    printer.print(wrappedTitle)
    printer.justify = adafruit_thermal_printer.JUSTIFY_LEFT
    printer.size = adafruit_thermal_printer.SIZE_SMALL
    printer.print("\n")
    printer.print(wrappedPoem)
    printer.print(wrappedAuthor)
    printer.print(randPoem[3])
    printer.feed(3)

printPoem() # function call
```

### Motion

- Drivers / Hats
  * Servo HAT (DC/PWM 16 channel; 2327)
  * Servo Bonnet (PWM 16 channel; 3416)
  * Pimoroni Inventor HAT (motor, servo, audio driver connection options; 5736)
  * DC / Stepper Motor Bonnet (4 DC or 2 Stepper; 4280)
  * Cricket HAT (signal pins, PWM Output, capacitive touch; 3957)


<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2327-13.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/3416-03.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/5736-00.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4280-06.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/3957-00.jpg?raw=true"></p></td></tr>
<tr><td><p align="center">Servo HAT</p></td>
<td><p align="center">Servo Bonnet</p></td>
<td><p align="center">Inventor HAT</p></td>
<td><p align="center">Motor Bonnet</p></td>
<td><p align="center">Cricket HAT</p></td>
</tr>
<tr><td><p align="center"><a href="https://learn.adafruit.com/adafruit-16-channel-pwm-servo-hat-for-raspberry-pi/">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-16-channel-pwm-servo-hat-for-raspberry-pi/">Tutorial</a></p></td>
<td><p align="center"><a href="https://github.com/pimoroni/inventorhatmini-python">Documentation</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-dc-and-stepper-motor-hat-for-raspberry-pi">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-crickit-hat-for-raspberry-pi-linux-computers">Tutorial</a></p></td>
</tr></table>

<br><br>

- Motors / Chassis Kits
  *   Jetbots parts pack with motors (4225)
    * Looks like we'd need to build an enclosure, but it's open source ([GitHub](https://github.com/NVIDIA-AI-IOT/jetbot))
    * Includes FeatherWing board, OLED display, 2 DC motors, 2 wheels
  
  * Mini red round cassis kit (two motors; 3216)
    * Includes aluminum frame, 2 DC motors, 2 wheels, 1 caster ball

  * Mini red rectangle chassis kit (two motors; 2939)
    * Includes aluminum frame, 2 DC motors, 2 wheels, 1 caster ball

  * Mini black round chassis kit (two motors; 3244)
    * Includes aluminum frame, 2 DC motors, 2 wheels, 1 caster ball

<table>
<tr>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/4225-01.jpg?raw=true"></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/3216-09.jpg?raw=true" width=75%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/2939-08.jpg?raw=true" width=75%></p></td>
<td><p align="center"><img src="https://github.com/kwaldenphd/poemBot/blob/master/images/inventory/3244-02.jpg?raw=true" width=75%></p></td></tr>
<tr><td><p align="center">Jetbots</p></td>
<td><p align="center">Red Chassis Kit</p></td>
<td><p align="center">Red Chassis Kit</p></td>
<td><p align="center">Black Chassis Kit</p></td>
</tr>
<tr><td><p align="center"><a href="https://jetbot.org/master/getting_started.html">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/adafruit-dc-and-stepper-motor-hat-for-raspberry-pi">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/simple-raspberry-pi-robot">Tutorial</a></p></td>
<td><p align="center"><a href="https://learn.adafruit.com/simple-raspberry-pi-robot">Tutorial</a></p></td>
</tr></table>

<br><br>
