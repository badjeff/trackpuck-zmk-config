# ZMK Config for Trackpuck

This is the ZMK firmware config repository for [trackpuck](https://github.com/badjeff/trackpuck).

The peripheral will present itself as a mixture of keyboard and joystick with ZMK module [zmk-hid-joystick](https://github.com/badjeff/zmk-hid-joystick). The sensors are handled by ZMK module [zmk-mlx90393-driver](https://github.com/badjeff/zmk-mlx90393-driver). 3D space convertion is handled in an embedded input-processor [zmk,input-processor-trixer](https://github.com/badjeff/trackpuck-zmk-config/blob/main/boards/shields/trackpuck/input_processor_trixer.c) in this config repo.

**Important**: This firmware do **NOT** spoof to be one specific peripheral and complies with the software terms and conditions of other vendors.

**Sidetrack for trackballs:**
When you looking at this. You are probably not only read the readme in Trackpuck repo. And you have interested to dig how the things work. So, you might want to know that all ZMK trackball with dual-sensor (e.g. [mochibella](https://github.com/badjeff/mochibella), or [Efog's Endgame with opt-out some features due to flash size](https://github.com/efogtech/endgame-trackball-firmware)) would take this config as reference, to setup the `zmk-hid-joystick`, converting 3DoF trackball to feature free orbit mode with `TrackpuckTools` in Fusion360 and Blender. And, the free orbit mode config example was not be provided in [mochibella](https://github.com/badjeff/mochibella), i think it is not the best to toggle mode via switches but somebody likes to have the feature for free.

### Related Projects

- [TrackpuckTools-Fusion360](https://github.com/badjeff/TrackpuckTools-Fusion360) is a Fusion 360 add-in that connects HID-based 6DoF input peripheral devices as navigation input for Fusion 360, providing fluid control over camera orbit, pan, zoom, and rotation.

- [TrackpuckTools-Blender](https://github.com/badjeff/TrackpuckTools-Blender) is a Blender add-in that connects HID-based 6DoF input peripheral devices as navigation input for Fusion 360, providing fluid control over camera orbit, pan, zoom, and rotation.

- [Magnetometers tracking simulator web app](https://sim7dof4ve.vercel.app/) will show how this all thigs works.

- [A example web app](https://trackpuck-threejs-examples.vercel.app/). Used to test HID Joystick outputs via web gamepad api.

## License

Available under the [MIT](/LICENSE) license.
