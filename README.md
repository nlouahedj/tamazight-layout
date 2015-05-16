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
2.  Open the file `/usr/share/X11/xkb/rules/base.lst` and add `dz              Amazigh (Tamazgha)` after `!layout`.
3.  Open the file `/usr/share/X11/xkb/rules/base.lst` and add the folowing lines inside `<layoutList> ... </layoutList>`:

    ```
    <layout>
      <configItem>
        <name>dz</name>
        <shortDescription>mz</shortDescription>
        <description>Amazigh (Tamazgha, Amazigh latin caracters)</description>
      </configItem>
      <variantList>
		<variant>
		  <configItem>
		        <name>amazigh-tifinagh</name>
		        <shortDescription>tif</shortDescription>
		        <description>Amazigh (Tamazgha, Amazigh tifinagh caracters)</description>
		        <languageList>
		        <iso639Id>fra</iso639Id>
		        </languageList>
		      </configItem>
		</variant>
      </variantList>
    </layout>
  ```
4.  Open the file `/usr/share/X11/xkb/rules/evdev.lst` and add `dz              Amazigh (Tamazgha)` after `!layout`.
5.  Open the file `/usr/share/X11/xkb/rules/evdev.lst` and add the folowing lines inside `<layoutList> ... </layoutList>`:

    ```
    <layout>
      <configItem>
        <name>dz</name>
        <shortDescription>mz</shortDescription>
        <description>Amazigh (Tamazgha, Amazigh latin caracters)</description>
      </configItem>
      <variantList>
		<variant>
		  <configItem>
		        <name>amazigh-tifinagh</name>
		        <shortDescription>tif</shortDescription>
		        <description>Amazigh (Tamazgha, Amazigh tifinagh caracters)</description>
		        <languageList>
		        <iso639Id>fra</iso639Id>
		        </languageList>
		      </configItem>
		</variant>
      </variantList>
    </layout>
  ```
6.  Restart the Xorg server or your computer.
7.  Now you can finde the layout in the keyboard settings of your disktop manager: 
Amazigh (Tamezgha, latin characters) end Amazigh (Tamezgha, tifinagh characters).

To Do:
------
Create an installation script.
