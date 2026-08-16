---
tags:
  - code-project
  - electronics-project
  - pcb
---
---
GitHub Repository:(NOT CREATED YET)

---
## Intro/Concept:
an exploration of addressable LEDs, using the [FastLED](https://fastled.io) library and an Arduino

---
## Phase 1: Basic Functions
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

---
## Phase 2: Animations

---
## Time Line:
- [ ] 
---
## Concept Drawings/Notes:

---
## File ledged

| File Name                      . | File Description                 . |
| -------------------------------- | ---------------------------------- |
| buttonTest.ino                   |                                    |
| allOffFunc.ino                   | a file to test the                 |
| updateFunc.ino                   |                                    |

---
## Component Guide

| Component name/number | Component type | Component use/assosiated part |
| --------------------- | -------------- | ----------------------------- |
|                       |                |                               |
|                       |                |                               |

---
## Results/ updates

---