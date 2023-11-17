# E39steerModule
---

This project was created to solve the need for a MY99 BMW 540i (E39) to be able to steer using the semi-autonomous driving software OPENPILOT.

---

### Disclaimer

The E39steerModule is created by fellow that have no knowledge of any kind on automotive, material, mechanical or elecrical engineering, nor I am a 3D-designer of anykind. I just like do stuff and get things done. If ever someone tries to implement this, keep in mind that it is designed to intentionally kill you.

The designs in different pictures may vary and confusing as f. This is just me being lazy, but it seems there has been some development done.

---

### Credit

The NEMA [control logic board](https://github.com/dzid26/StepperServo-hardware) and [firmware](https://github.com/dzid26/StepperServoCAN) that I use, is created by dzid26.

---

### Design

The central idea of this project was the concept that the support point of the module is not in the car frame but is instead bearing-mounted around the steering shaft itself, supported by the control arm, with the steering shaft being driven by a NEMA17 stepper motor.

Animation of the E39steerModule assembly:

https://github.com/killinen/E39steerModule/assets/37126045/f650a476-6907-45d7-89ee-340f917e1412



The design has been parametirized so that the shaft diamemter and the bearing size can in some extetend be changed, and some other things.
--> Picture


The shaft diameter and module length will be engraved onto side of the module. This made to help with prototyping.
-->  Picture

The module is built from 110 mm M5 threaded rods, 686ZZ bearings, 58x6 mm steel rods, and a 3D-printed case made of PETG with a layer height of 0.2 mm, a wall thickness of 1.2 mm, and top and bottom 'layers'. Additionally, there are 2 mm steel plates at the ends of the case, and the control arm is constructed from 4 mm flat bar.

---

### Outro

There is no really enough testing done to say that this is any good, but for a short drive, it drives works quite well.

--> Video
