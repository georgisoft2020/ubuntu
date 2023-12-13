# Sound problems
pulseaudio --kill

pulseaudio --start

systemctl --user restart pipewire.service
