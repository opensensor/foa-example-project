# OpenSensor foa-example-project

This is OpenSensor Engineering's independently maintained fork of
[esp32-open-mac/foa-example-project](https://github.com/esp32-open-mac/foa-example-project). The canonical repository
is [opensensor/foa-example-project](https://github.com/opensensor/foa-example-project).

**AI-assisted and AI-generated contributions are welcome.** See
[Contributing](CONTRIBUTING.md) for review and validation expectations. Submit
[issues](https://github.com/opensensor/foa-example-project/issues) and [pull requests](https://github.com/opensensor/foa-example-project/pulls) here.

The [OpenSensor ESP repository index](https://github.com/opensensor/esp-wifi-hal/blob/main/FORKS.md)
links the related driver, stack, register definitions and reverse-engineering tools.
Original history, credits and licenses are retained.

This fork initially preserves upstream code. The S3 results in the repository
index apply to the Rust driver's recorded dependencies; they do not establish
hardware validation of this repository's current default branch.

## Upstream documentation

The original documentation follows; its badges, release links and project status
refer to upstream unless explicitly identified as OpenSensor results.

# FoA example project

This is a very basic Rust project that uses our open source Wi-Fi driver & stack
for the ESP32. It only connects to an access point (specified in the `SSID` env var)
and makes a parrot dance on your screen over HTTP.

If your AP uses WPA2-Personal, you can specify the password in the `PASSWORD` env
var. Note, that if it's an open network the variable must not be defined, as
otherwise the code will expect it to be a WPA2 network. (This is just because I
was to lazy to write something more complex for this example.)
