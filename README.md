# ubuntu
some scripts


# Logitech , mouse speed faster
```xset mouse 10 1```

# Logitech , mouse speed slower
```xset mouse 1 1```

# Logitech man
```xset mouse <acceleration> <threshold>```

# Mouse wheel  
```sudo apt install imwheel (replace apt with apt-get depending on your system)```

```pico ~/.imwheelrc```

  and paste

```
".*"
None,      Up,   Button4, 3
None,      Down, Button5, 3
Control_L, Up,   Control_L|Button4
Control_L, Down, Control_L|Button5
Shift_L,   Up,   Shift_L|Button4
Shift_L,   Down, Shift_L|Button5
where you should try different values for # in the lines
```

  
To test the settings use the command 
```killall imwheel && imwheel -b "4 5"```

Open Startup Applications and add 
```imwheel -b "4 5"```


# Brightness
```echo 10000 | sudo tee /sys/class/backlight/intel_backlight/brightness```

# tweaker
sudo apt install gnome-tweak-tool

