# Fan speed script use
To use this script, in i3status config (.config/i3status/config) add 
cpu_temperature 41 {
        format = "❄%degrees RPM"
        path = "/etc/fanspeed/left"
        max_threshold=4000
}
cpu_temperature 42 {
        format = "❄%degrees RPM"
        path = "/etc/fanspeed/right"
        max_threshold=4000
}
cpu_temperature 43 {
        format = "☀%degrees"
        path = "/etc/backlight/i3status"
	      max_threshold=1000000
}
Use whatever max threshold, anything works really. Depends on what software youre using. Backlight isn't neccesarily needed but I use it.

Run $ fanspeeddaemon &
on boot and it will update fan speed readings accordingly. i3bar will do the rest.
If you have any questions feel free to contact me. Thank you!
