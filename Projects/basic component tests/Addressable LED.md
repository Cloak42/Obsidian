---
tags:
  - code-project
  - electronics-project
  - pcb
---
---
GitHub Repository:https://github.com/Cloak42/Addressable-LED

---
## Intro/Concept:
an exploration of addressable LEDs, using the [FastLED](https://fastled.io) library and an Arduino

---
## Code Phase 1: Understanding the Library
### 1. basic necessary things
```
#include <FastLED.h>

#define LED_PIN 2
#define NUM_LEDS 5  // Set precisely to your 2 LEDs
#define BRIGHTNESS 25
#define LED_TYPE WS2812B
#define COLOR_ORDER RGB

CRGB leds[NUM_LEDS];   // definesd an array that represents your led stip
```
### 2. changing/manipulating LEDs
```
leds[i]=CRGB(0,0,0);
```
sets the color in to be of the i led to be what ever RGB values you want 
```
FastLED.show();
```
actually compiles and sends the signal to update the leds to match the leds[] array

---
## ~~Code Phase 2: Basic Functions~~

**this code is likely unnecessary and redundant scroll down to phase 2.1 to see amended code**
### 1. update Function

```
void update(LED arr[5]) {

  // requires the LED structure and array of said structure based on the number of LEDs
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(arr[i].R, arr[i].G, arr[i].B);
    FastLED.show();
    delay(500);
  }
  return;
}
```

- updates a string of LEDs based on an array containing the RGB values for each LED
- data for each LED is stored in the struct bellow 
```
struct LED {
  int index;
  int brightness;
  int R;
  int G;
  int B;
};
```

**Dependencies**
- **fastLED library must be included**
- **LED struct must be defined**
- **must define and pass an array of the LED struct into the function**
-  **NUM_LEDS must be defined**

### 2. allOff Function

```
void allOff(LED arr[NUM_LEDS]) {
  for (int i = 0; i < NUM_LEDS; i++) {
    arr[i].R = 0;
    arr[i].G = 0;
    arr[i].B = 0;
    leds[i] = CRGB(arr[i].R,arr[i].G,arr[i].B);
    FastLED.show();
  }
  return;
}
```

- sets all RGB values in the array to 0
- and update all the LEDs to the new value

**Dependencies**
- **fastLED library must be included**
- **LED struct must be defined**
- **must define and pass an array of the LED struct into the function**
-  **NUM_LEDS must be defined**

### 3. allColor Function

```
void allColor(LED arr[NUM_LEDS],int R,int G, int B) {
  for (int i = 0; i < NUM_LEDS; i++) {
    arr[i].R = R;
    arr[i].G = G;
    arr[i].B = B;
    leds[i] = CRGB(arr[i].R,arr[i].G,arr[i].B);
    FastLED.show();
  }
  return;
}
```

- sets all LEDs to the color passed through the function
- updates all the LEDs to the new color value

**Dependencies**
- **fastLED library must be included**
- **LED struct must be defined**
- **must define and pass an array of the LED struct into the function**
-  **NUM_LEDS must be defined**
---
## Code Phase 2.1: Basic Functions reworked
### 1. allOff:

```
void allOff() {
  for (int i = 0; i < NUM_LEDS; i++) {
    leds[i] = CRGB(0,0,0);
    FastLED.show();
  }
  return;
}
```

### 2. allColor:

```

```

---
## Code Phase 2: Animations

---
## Physical Setups:
- Basic breadboard
![[Pasted image 20260817193714.png|260]]
(ignore the purple IMU, used for different project)
a string of LEDs connected to 5v GND and to a digital pin of an Arduino nano through a 470 ohm resistor 

- PCB matrix ([[LED Sand Matrix]])

- Full PCB matrix ([[LED Sand Matrix]])

---
## File ledged

| File Name                      . | File Description                 .                   |
| -------------------------------- | ---------------------------------------------------- |
| buttonTest.ino                   |                                                      |
| allOffFunc.ino                   | the program showing the use of the allOff Function   |
| updateFunc.ino                   | the program showing the use of the update Function   |
| allColorFunc.ino                 | the program showing the use of the allColor Function |

---
## Component Guide

| Component name/number | Component type | Component use/assosiated part |
| --------------------- | -------------- | ----------------------------- |
| 5mm diffused WS2812   | Adressable LED |                               |
| 470 ohm ressistor     | Resistor       | voltage spike protection      |

---
## References

- WS2812 pinout:
![[Pasted image 20260817194135.png]]

---
## Results/ updates

---