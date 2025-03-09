# Volume Monitor

Show notifications when PulseAudio volume changes.

This is *not* another volume control. All this script does is that is
listens for D-Bus events for PulseAudio sinks, and shows a notification when
a change in volume (increase, decrease, mute, unmute) is observed.

## Dependencies

* `pulseaudio` with D-Bus support
* `libnotify`
* `python3` and the following libraries:
	* `asyncio`
	* `pulsectl`
	* `pulsectl_asyncio`
	* `dbus_next`

## Usage

Run `./volume-monitor` in the background. Alternatively, install and enable
`volume-monitor.service` as a user service.
