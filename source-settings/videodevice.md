---
description: Pre-configures the selected video device
---

# \&videodevice

## Aliases

* `&vdevice`
* `&vd`

## Options

| Value          | Description                                                                                                                                |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 0              | disable the video camera automatically. No option to change it during setup is provided.                                                   |
| 1              | auto-select the default video camera. No option to change it will be allowed.                                                              |
| (string value) | auto-select a video device that has a label containing that same string / deviceID. Whitespaces in names can be replaced with underscores. |

## Details

It can be changed after the connection has been established.\
Useful for helping a remote guest skip-past the complex setup of their camera/audio.

You can use this option to also disable a guest's camera, potentially allowing for guest connections that have no video or audio.  This is a great option if you want to use midi-only transport, add some hidden IFRAME control, or just wanted to text chat.

For a device like an iPhone, you can pass a string value such as `&vd=back` to specify the back camera by default. For Android, you might try `rear` instead of `back`, but it will depend on the name the manufacture gave the camera.

When combined with `&webcam` and `&autostart`, you can have the camera start publishing instantly, often without any user interaction at all. Keep in mind that some browsers will still need to ask for permissions or require a user-gesture for things to function correctly though.

{% hint style="info" %}
See [vdo.ninja/devices](https://vdo.ninja/devices) to see the device IDs and device names. DeviceIDs are specific to VDO.Ninja's domain, while device names are not. The page will also auto-create links for  you, just by clicking on the respective device.
{% endhint %}

## Related

{% content-ref url="audiodevice.md" %}
[audiodevice.md](audiodevice.md)
{% endcontent-ref %}

{% content-ref url="and-nosettings.md" %}
[and-nosettings.md](and-nosettings.md)
{% endcontent-ref %}

{% content-ref url="and-webcam.md" %}
[and-webcam.md](and-webcam.md)
{% endcontent-ref %}

{% content-ref url="and-autostart.md" %}
[and-autostart.md](and-autostart.md)
{% endcontent-ref %}
