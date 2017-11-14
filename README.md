# IMega Keyboard for Linux

The cz-prg layout of IMega keyboard.

## Installation
1. `sudo cp cz-prg /usr/share/X11/xkb/symbols/`
2. `sudo vim /usr/share/X11/xkb/rules/base.lst`
   * Add into the section `! layout`:
     ```text
     cz-prg  Czech programming
     ```
   * Add into the section `! variant`:
     ```text
     qwertz      cz-prg: qwertz
     bracketu    cz-prg: Bracket uu
     bracketuzy  cz-prg: Bracket uu, qwertz
     ```
3. `sudo vim /usr/share/X11/xkb/rules/base.xml`
   * Add into the section `<layoutList>`:
     ```text
     <layout>
       <configItem>
         <name>cz-prg</name>
         <shortDescription>CzePrg</shortDescription>
         <description>Czech programming</description>
         <languageList><iso639Id>cze</iso639Id></languageList>
       </configItem>
       <variantList>
         <variant>
           <configItem>
             <name>qwertz</name>
             <description>qwertz</description>
           </configItem>
         </variant>
         <variant>
           <configItem>
             <name>bracketu</name>
             <description>Bracket-úů</description>
           </configItem>
         </variant>
         <variant>
           <configItem>
             <name>bracketuzy</name>
             <description>Bracket-úů, qwertz</description>
           </configItem>
         </variant>
       </variantList>
     </layout>
     ```
4. `sudo ln -s /usr/share/X11/xkb/rules/base.lst /usr/share/X11/xkb/rules/evdev.lst`
5. `sudo ln -s /usr/share/X11/xkb/rules/base.xml /usr/share/X11/xkb/rules/evdev.xml`

## Version
IMega keyboard version: 0.12

## Credit
The keyboard is taken from [http://www.imega.cz/keyboard/linux/for-linux-distribution.php](http://www.imega.cz/keyboard/linux/for-linux-distribution.php).
