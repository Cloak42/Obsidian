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
an exploration of addressable LEDs, using the FastLED library and an Arduino

---
## Phase 1: Basic Functions
### Update function
- runs a for loop based on the number of LEDs specified by NUM_LED
- updates them t
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

---
## Time Line:
- [ ] 
---
## Concept Drawings/Notes:

---
## File ledged

| File Name                      . | File Description                 . |
| -------------------------------- | ---------------------------------- |
|                                  |                                    |

---
## Component Guide

| Component name/number | Component type | Component use/assosiated part |
| --------------------- | -------------- | ----------------------------- |
|                       |                |                               |
|                       |                |                               |

---
## Results/ updates

---