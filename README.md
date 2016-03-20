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
  ber             dz: Berber (Algeria, Tifinagh caracters)
  la              dz: Latin (Algeria, Latin caracters)
  ar              dz: Arabic (Algeria)
```
after `! variant` in `/usr/share/X11/xkb/rules/base.lst` and `/usr/share/X11/xkb/rules/evdev.lst`.
3.  Add the folowing lines inside `<layoutList> ... </layoutList>` in `/usr/share/X11/xkb/rules/base.xml` and `/usr/share/X11/xkb/rules/evdev.xml`:

    ```
    <layout>
      <configItem>
        <name>dz</name>
        <shortDescription>la</shortDescription>
        <description>Berber (Algeria, Latin caracters)</description>
      </configItem>
      <variantList>
        <variant>
          <configItem>
            <name>ber</name>
            <shortDescription>ber</shortDescription>
            <description>Berber (Algeria, Tifinagh caracters)</description>
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
5.  Now you can finde the layout in the keyboard settings of your disktop manager: 
Berber (Algeria, Tifinagh caracters), Latin (Algeria, Latin caracters) or Arabic (Algeria).

To Do:
------
Create an installation script, or contribute it to XOrg at [freedesktop.org](https://www.freedesktop.org/wiki/Software/XKeyboardConfig)
