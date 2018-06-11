# EVE V rEFInd Theme

EVE V theme for the rEFInd boot manager

![Screenshot](https://eve.community/uploads/eve/original/2X/1/15fe28e480b1a7d73237c133c23387c241876613.jpg)

## Installation

1. Locate your rEFInd installation folder [Windows](https://www.rodsbooks.com/refind/installing.html#windows), [Linux](https://www.rodsbooks.com/refind/installing.html#linux), [Mac OSX](https://www.rodsbooks.com/refind/installing.html#osx)

2. Create a folder called `themes` inside it, if it doesn't already exist

3. Clone this repo into the `themes` folder

4. Add `include themes/refind-eve-v/theme.conf` to `refind.conf`

### Windows Installation on the V ([Source](https://www.rodsbooks.com/refind/installing.html#windows))

1. Locate Command Prompt in the Start menu, right-click it, and select Run as Administrator. This action opens a Command Prompt window with administrative privileges.

2. Type `mountvol S: /S` in the Administrator Command Prompt window. This makes the ESP accessible as drive `S:` from that window. (You can use a drive identifier other than `S:` if you like.)

3. Change into the folder you extracted the Theme to, so that the `refind-eve-v` directory is visible when you type dir.

4. Type `xcopy /E refind S:\EFI\refind\` to copy the refind directory tree to the ESP's EFI directory. If you omit the trailing backslash from this command, `xcopy` will ask if you want to create the refind directory. Tell it to do so.

5. Open `Notepad++` with Administrator rights. (notepad.exe will not work, since it is not able to edit Linux Linebreaks... 

6. Open `S:\EFI\refind\refind.conf` and add `include themes/refind-eve-v/theme.conf` to it.

7. Reboot and try it.

## Configuration
If you want to see the tools you had without the theme just uncomment (add `#` before) `showtools` and you will see the Tools Section like on my screenshot.

If you want to see the explanation text on the bottom just uncomment (add `#` before) `hideui singleuser,hints,arrows,label,badges` and you will see it again.

You need to do this in your `S:\EFI\refind\themes\refind-eve-v\theme.conf` file!

## Contribution

Pull requests for more OS icons are welcome. Please make sure the image is a 256x256 solid white png at 75% transparency. To keep alignment consistent the actual icon should be roughly 132x132 in the middle of the png. Depending on the shape of the icon, the size and position may vary to get better results.

## Credits

This theme is a fork of [rEFInd-ambience](https://github.com/lukechilds/refind-ambience) by lukechilds

## License

MIT © Luke Childs
