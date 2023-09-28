# Configuring a Custom Keyboard Shortcut for Partial Screen Capture and Clipboard Saving in Ubuntu
Open a terminal in Ubuntu.

Make sure you have gnome-screenshot and xclip installed. If they are not installed, you can do so with the following command:

```shell
sudo apt-get install gnome-screenshot xclip
```

Now, create a custom script to capture and copy to the clipboard. Open a text editor in the terminal:

```shell
nano screenshot-script.sh
```

Inside the text editor, copy and paste the following script:

```bash
#!/bin/bash
gnome-screenshot -a -f /tmp/screenshot.png
xclip -selection clipboard -t image/png -i /tmp/screenshot.png
```

This script captures a partial screenshot and temporarily saves it as /tmp/screenshot.png, then copies it to the clipboard using xclip.

Save the file and exit the text editor (in nano, you can do this by pressing Ctrl + O, then Enter to save, and Ctrl + X to exit).

Make the script executable with the following command:

```shell
chmod +x screenshot-script.sh
```

Now, you can assign a custom key combination to execute this script. Follow the steps in my previous response to set up a custom shortcut, but in the "Command" field, enter the full path to the script you just created, for example:

```shell
/full/path/to/script/screenshot-script.sh
```

Assign a key combination for the shortcut and click "Apply" to save the configuration.

Once you have configured the custom shortcut, you can press the assigned key combination to capture a part of the screen and copy it to the clipboard.
# screen-cut
