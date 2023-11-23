# E39steerModule

This project was created to solve the need for a MY99 BMW 540i (E39) to be able to steer using the semi-autonomous driving software openpilot.

Openpilot is an open source driver assistance system that offers Automated Lane Centering and Adaptive Cruise Control for over 200 supported car makes and models. To function properly, openpilot needs to be able to control the longitudinal (gas and brake) and lateral (steering) movements of the car using the CAN bus. For more information, see https://comma.ai/ and https://github.com/commaai/openpilot.

[![](https://i3.ytimg.com/vi/NmBfgOanCyk/maxresdefault.jpg)](https://youtu.be/NmBfgOanCyk)

My system is based on openpilot v0.8.2 and features stop-and-go capability achieved through the [BrakeModule](https://github.com/killinen/BrakeModule), which controls braking, and a device similar to the [Comma](https://youtu.be/3z-Izl-ve5o?si=7oRMfNvz600YJCA-) [Pedal](https://github.com/commaai/openpilot/wiki/comma-pedal), which manages acceleration. The E39steerModule is connected to same CAN network that these devices and receives steering torque values from openpilot, which determine the rotation of the steering wheel. I also track the Nema rotation (angle) relation to the steering shaft rotation and if there is too big of a difference get a warning to check the module assembly.

As the actuator motor I use [this](https://www.aliexpress.com/item/4001349087963.html) NEMA17 motor with 5.18 gear ratio. With the motor/steering shaft gear ratio of 2 the end torque applied to the steershaft is approx 12 Nm.

---

### Credit

The NEMA [control logic board](https://github.com/dzid26/StepperServo-hardware) and [firmware](https://github.com/dzid26/StepperServoCAN) that I use, is created by dzid26, and this project probably would't come to fruition without his work.

---

### Disclaimer

The E39steerModule is created by fellow that have no knowledge of any kind on automotive, material, mechanical or elecrical engineering, nor I am a 3D-designer. I just like do stuff and get things done. If someone ever tries to implement this, keep in mind that it is designed to intentionally kill you.

The designs in different pictures may vary and is confusing as f. This is just me being lazy, but at least it gives the impression that some development have been done.

The E39steerModuleCase v1.f3d design might be broken because I deleted a lot of stuff from it to be more clean and haven't tested it.

---

### Case design

The key concept behind this project involves placing the primary support point of the module case not within the car frame but, instead, bearing-mounting it around the steering shaft. This configuration is supported by the control arm, with the steering shaft being driven by a NEMA17 stepper motor.

Animation of the E39steerModule assembly:

https://github.com/killinen/E39steerModule/assets/37126045/f650a476-6907-45d7-89ee-340f917e1412

<br />

The design has been parametrized so that the shaft diameter and the bearing size can in some extetend be changed, along with some other things. This gives the ability to tune the design and maybe be used in some other car/system.

![User_parameters](https://github.com/killinen/E39steerModule/assets/37126045/4bd57aa8-7b20-4dc0-b0dc-f16660cb3d7c)



The shaft diameter and distance between steering shaft and Nema gearbox shaft (distance between gears) is engraved onto side of the case. This was made to help with prototyping to keep on track which parts you have in hand, because with 3D-printing you have to adjust these values to get the fit really right or make those variables too tight and then use shim plates to adjust to correct tolerances.

![Case_engravings](https://github.com/killinen/E39steerModule/assets/37126045/ab277f7c-30d0-4e6d-868f-dddd649c0cf2)

This module is built from 110 mm M5 double end threaded rods, 606ZZ bearings, 58x6 mm steel rods (cut to length), and a 3D-printed case made of PETG with a layer height of 0.2 mm, a wall thickness of 1.2 mm, and top and bottom 'layers' with 20% infill. Additionally, there are 2 mm steel plates at the ends of the case, and the control arm is constructed from 4 mm flat bar. I have used also 3D-printed shim plates betweeen case segments to get the bearing and gear distance tolerances right. The gear shim plate can be seen in the pictures as red line between the segments.

The module is installed to the E39 steering shaft between the steering column and firewall. The steering shaft luckily has an teething in one part of the shaft where the shaft gear is installed. The E39steerModule is placed under the teething and is resting on a sleeve that is coming out of the firewall and is aroud the steering shaft.

![20231117_133440](https://github.com/killinen/E39steerModule/assets/37126045/018b6c33-1576-464d-9bac-939dba0a3a1a)

![20231117_133419](https://github.com/killinen/E39steerModule/assets/37126045/5e90a912-a3aa-40ce-ae47-9608fc4c10f8)

![20231117_133303](https://github.com/killinen/E39steerModule/assets/37126045/84801272-1761-44de-afa7-7b1305489efd)



The E39steerModule control arm goes up to cars chassis where is steering columns bolted joint. This keeps the module in place, so it won't start rotating when the shaft or motor is driven.

![20231117_133318](https://github.com/killinen/E39steerModule/assets/37126045/468aacc6-0ba5-450c-ae55-ecc205583f62)


---

### Outro

I haven't done enough testing to say that this module is good for a million miles, but for a short drive, it works ok.

https://github.com/killinen/E39steerModule/assets/37126045/6e7ec804-1adb-46d0-a014-d352c33e2bd3



