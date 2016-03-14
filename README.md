# tamazight-layout
Linux tamazight keyboard layout (bouth Tifinagh and Latin)

### Latin layout: ###
![latin layout](https://raw.githubusercontent.com/nouriph/tamazight-layout/master/talatinit.png)
### Tifinagh layout: ###
![latin layout](https://raw.githubusercontent.com/nouriph/tamazight-layout/master/tifinagh.png)

Installation:
-------------
All operations will be done as **root**.

1.  Copy the file `symbols/dz` to `/usr/share/X11/xkb/symbols/dz`.
2.  Add `dz              Amazigh (Tamazgha)` after `!layout` and 
```
  tif             dz: Tamazight (Tamazgha, Tifinagh caracters)
  lat             dz: Tamazight (Tamazgha, Latin caracters)
  ar              dz: Arabic (Tamazgha)
```
after `variant` in `/usr/share/X11/xkb/rules/base.lst` and `/usr/share/X11/xkb/rules/evdev.lst`.
3.  Add the folowing lines inside `<layoutList> ... </layoutList>` in `/usr/share/X11/xkb/rules/base.xml` and `/usr/share/X11/xkb/rules/evdev.xml`:

    ```
    <layout>
      <configItem>
        <name>dz</name>
        <shortDescription>lat</shortDescription>
        <description>Tamazight (Tamazgha, Latin caracters)</description>
      </configItem>
      <variantList>
        <variant>
          <configItem>
            <name>tif</name>
            <shortDescription>tif</shortDescription>
            <description>Tamazight (Tamazgha, Tifinagh caracters)</description>
          </configItem>
        </variant>
        <variant>
          <configItem>
            <name>ar</name>
            <shortDescription>ar</shortDescription>
            <description>Arabic (Tamazgha)</description>
          </configItem>
        </variant>
      </variantList>
    </layout>
  ```
4.  Restart the Xorg server or your computer.
5.  Now you can finde the layout in the keyboard settings of your disktop manager: 
Tamazight (Tamazgha, Latin caracters) and Tamazight (Tamazgha, Tifinagh caracters).

To Do:
------
Create an installation script.
