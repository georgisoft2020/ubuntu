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
```sudo apt install gnome-tweak-tool```

# Screenshot
flameshot

# Copy clipboard manager
CopyQ

# Paths, to be always displayed (Ctrl+L)
```gsettings set org.gnome.nautilus.preferences always-use-location-entry true```

# Setup L2TP over IPsec VPN client on Ubuntu 
```sudo apt-get update```
```sudo apt-get install network-manager-l2tp```
```sudo apt-get install network-manager-l2tp-gnome```

Set VPN properties via GUI
Navigate to Settings > Network > VPN > +

# Count lines of code, excluding ./vendor/* dir
```find . -name '*.php' ! -path './vendor/*' | xargs wc -l```

# Make an .sh script viewed as app in software searches


    In Terminal
    
    
    gedit ~/.local/share/applications/<Your App Name>.desktop
    
    
    
    In gedit
    
    Here you should edit:  
    _You can find more details and more keys in  [the freedesktop.org docs](https://specifications.freedesktop.org/desktop-entry-spec/desktop-entry-spec-latest.html#recognized-keys)_
    
    
    [Desktop Entry]
    # Define which specification version this entry is using 
    Version=1.0
    # The application name (eg. "Gnome Terminal", "Firefox")
    Name=My Awesome App
    # The generic app name (eg. "Terminal", "Web Browser")
    GenericName=Awesome App
    # The Tooltip
    Comment=This app is awesome!
    # The command you want to execute
    Exec=/path/to/sh/file/file.sh
    # Whether the app should run in a terminal window
    Terminal=false
    # The pretty picture :D
    Icon=/opt/PhpStorm-103.243/bin/webide.png
    # The type of the desktop entry (Application, Link, or Directory)
    Type=Application
    # Categoies the app should be in
    Categories=Network;WebBrowser;
    # Mime types this launcher can open
    MimeType=text/html;
    # Localized version of the above info
    Name[en_NZ]=My Awesome App
    GenericName[en_NZ]=Awesome App
    Comment[en_NZ]=This app is awesome!
    

