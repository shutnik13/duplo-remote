# LEGO DUPLO 10427 — Train Remote

A child-friendly, browser-based Bluetooth remote control for the **LEGO DUPLO Interactive Adventure Train (10427)**.

The project includes a colorful, portrait-oriented **driver's cab** with a combined direction/speed lever, an emergency stop button, headlight controls, and a horn. It is designed for use on a small iPhone screen, including older iPhone SE devices.

> [!IMPORTANT]
> **Compatibility and testing:** This project has been tested **only with my own LEGO DUPLO 10427 train**. It has **not** been tested with other LEGO DUPLO train models, other train hardware revisions, or other Bluetooth devices. Compatibility with any other model or revision is **not guaranteed**.

## Live demo

- [Train remote — GitHub Pages](https://shutnik13.github.io/duplo-remote/)
- [Driver's cab](https://shutnik13.github.io/duplo-remote/cab.html)

The driver's cab URL assumes that the latest cab version is published as `cab.html`.

## Features

- Direct Bluetooth Low Energy (BLE) control from a supported web browser
- Portrait-oriented, toy-like driver's cab interface
- One lever for **forward / neutral / reverse** and speed control
- **10 speed steps in each direction**, from 10% to 100%
- Large **STOP** button that sends a motor stop command and resets the lever to neutral
- Headlight color cycling and horn control
- Train-shaped Bluetooth connection control with a connection indicator
- **Press and hold for 2 seconds** to connect or disconnect, helping prevent accidental taps
- Single HTML file; no framework, build process, or backend required

## Tested setup

- **Train:** LEGO DUPLO 10427 (my own unit only)
- **Phone:** an older iPhone running **iOS 15.8**
- **Browser:** **Bluefy**, which provides Web Bluetooth support on iOS
- **Hosting:** GitHub Pages over HTTPS

Other iOS versions, browsers, devices, and train models have not been verified as part of this project.

## How to use

1. Turn on the LEGO DUPLO 10427 train.
2. Open the [driver's cab](https://shutnik13.github.io/duplo-remote/cab.html) in **Bluefy** on your iPhone.
3. **Hold the train icon for 2 seconds** to start Bluetooth pairing/connection.
4. Select the train when the browser prompts you.
5. Move the lever **up** to drive forward or **down** to reverse. The center position is neutral.
6. Use the **STOP** button to stop the motor and return the on-screen lever to neutral.
7. Use the headlight and horn controls as desired.

The train icon also indicates the Bluetooth connection state. To disconnect, hold it again for 2 seconds.

## Hosting your own copy

1. Download the HTML file and name it `cab.html`.
2. Add it to a GitHub repository.
3. Enable **Settings → Pages → Deploy from a branch**, selecting `main` and `/ (root)`.
4. Open `https://YOUR_USERNAME.github.io/YOUR_REPOSITORY/cab.html` in Bluefy.

Web Bluetooth generally requires a secure context such as **HTTPS**. Opening the file directly from the iOS Files app may not provide Bluetooth access.

## Safety and limitations

- This is an **unofficial hobby project**, not affiliated with or endorsed by the LEGO Group.
- The 2-second Bluetooth hold is an **accidental-tap safeguard**, not a security mechanism.
- The STOP button sends a Bluetooth command; it is **not a physical emergency brake**.
- If the phone, browser, or Bluetooth connection fails, **the train may not stop immediately**. Supervise use and keep the train within reach.
- Switching apps or locking the phone may interrupt Bluetooth control.
- The 100% setting represents the remote's commanded speed level, not a measured physical train speed.

## Technology

The remote uses the browser's **Web Bluetooth API** and sends BLE GATT commands directly to the train. The interface is implemented in plain HTML, CSS, and JavaScript.

## License

No license has been specified. Please add a `LICENSE` file if you intend to grant reuse or redistribution rights.

---

**LEGO** and **DUPLO** are trademarks of the LEGO Group, which does not sponsor, authorize, or endorse this project.
