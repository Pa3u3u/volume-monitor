# Volume Monitor

Show notifications when PulseAudio volume changes.

This is *not* another volume control.
All this script does is that it listens for PulseAudio events for sinks and cards.
A notification is shown when a change in volume (increase, decrease, mute, unmute) is observed, or when a sound card is added, changed or removed.

It works with both PulseAudio and PipeWire, which provides the PulseAudio protocol through `pipewire-pulse`.

## Dependencies

* PulseAudio, or PipeWire with `pipewire-pulse`.
* A notification daemon implementing `org.freedesktop.Notifications`.
* `python3` and the following libraries:
	* `pulsectl`
	* `pulsectl_asyncio`
	* `dbus_next`

## Usage

Run `./volume-monitor` in the background.
Alternatively, install the script as `/usr/bin/volume-monitor`, then install and enable `volume-monitor.service` as a user service.
