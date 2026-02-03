# labwc-tasklist

Overview/Exposé-like script tested on labwc 0.93+ to add a cool blurred layer under the native labwc task switcher.

- make sure to install: wlrctl and wtype
- make sure to install the required python dependencies
- chmod +x labwc-tasklist
- bind it to a convenient key combo / mouse button (rc.xml on labwc)
- enjoy!

To prevent this script from showing up in the tasks add this to your rc.xml
```xml
<windowRules>
  <windowRule title="labwc-tasklist">
    <skipWindowSwitcher>yes</skipWindowSwitcher>
  </windowRule>
</windowRules>
```

If you want to invoke this script on a mouse wheel/middle button press just like on mac os, make sure to add the following to your rc.xml
```xml
<mouse>
<default />
<!-- exposee on mouse wheel click -->
<context name="All">
  <mousebind button="Middle" action="Press">
    <action name="Execute" command="labwc-tasklist" />
  </mousebind>
</context>
</mouse>
```
