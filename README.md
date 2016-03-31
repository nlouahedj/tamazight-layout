# tamazight-layout
Linux tamazight keyboard layout (bouth Tifinagh and Latin)

### Latin layout: ###
![latin layout](https://raw.githubusercontent.com/menoureddine/tamazight-layout/master/talatinit.png)
### Tifinagh layout: ###
![latin layout](https://raw.githubusercontent.com/menoureddine/tamazight-layout/master/tifinagh.png)

Installation:
-------------
Be aware that this installation process has been tested on ArchLinux and Ubuntu14.04 for the OSs and Gnome3 and Unity for the DE, so please if you are testing it on other distro and it did work perfectly tell us to update this list, but basically this is the default installation process for any Linux based distro.

All operations will be done as **root**.

1.  Copy the file `symbols/dz` to `/usr/share/X11/xkb/symbols/dz`.
2.  Add `dz              Amazigh (Tamazgha)` after `!layout` and 
```
  ber             dz: Berber (Algeria, Tifinagh characters)
  la              dz: Latin (Algeria, Latin characters)
  ar              dz: Arabic (Algeria)
```
after `! variant` in `/usr/share/X11/xkb/rules/base.lst` and `/usr/share/X11/xkb/rules/evdev.lst`.

3.  Add the following lines inside `<layoutList> ... </layoutList>` in `/usr/share/X11/xkb/rules/base.xml` and `/usr/share/X11/xkb/rules/evdev.xml`:

    ```
    <layout>
      <configItem>
        <name>dz</name>
        <shortDescription>la</shortDescription>
        <description>Berber (Algeria, Latin characters)</description>
      </configItem>
      <variantList>
        <variant>
          <configItem>
            <name>ber</name>
            <shortDescription>ber</shortDescription>
            <description>Berber (Algeria, Tifinagh characters)</description>
            <languageList>
              <iso639Id>ber</iso639Id>
            </languageList>
          </configItem>
        </variant>
        <variant>
          <configItem>
            <name>ar</name>
            <shortDescription>ar</shortDescription>
            <description>Arabic (Algeria)</description>
            <languageList>
              <iso639Id>ara</iso639Id>
            </languageList>
          </configItem>
        </variant>
      </variantList>
    </layout>
    ```
4.  Restart the Xorg server or your computer.
5.  Now you can find the layout in the keyboard settings of your desktop manager: 
Berber (Algeria, Tifinagh characters), Latin (Algeria, Latin characters) or Arabic (Algeria).

To Do:
------
Create an installation script, or contribute it to XOrg at [freedesktop.org](https://www.freedesktop.org/wiki/Software/XKeyboardConfig)
