<div align="center">

## Different Ways of a Windows 9x Shutdown


</div>

### Description

Explains an interesting way to shutdown a Windows 9x PC in only 1 Line of Source Code. But not only to shutdown... have a look for details
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Agent White](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/agent-white.md)
**Level**          |Beginner
**User Rating**    |4.4 (22 globes from 5 users)
**Compatibility**  |Microsoft Visual C\+\+
**Category**       |[System Services/ Functions](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/system-services-functions__3-23.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/agent-white-different-ways-of-a-windows-9x-shutdown__3-833/archive/master.zip)





### Source Code

<P>Another way to handle Windows-Shutdowns...
You can run many Windows Function direct with the RunDLL32 program.
Now I will explain you how this will works for a shutdown ... it's very simple !!!
Just put these line in your Project:</P>
<P>system(</P>
<P>"rundll32 shell32.dll,SHExitWindows VALUE");</P>
<P>Here are the different VALUES you can put in:</P>
<P>0	Logoff User</P>
<P>1	Shutdown Windows</P>
<P>2	Restart Windows</P>
<P>4	Force Applications to be killed</P>
<P>8	Poweroff (if supported by your PC)</P>
<P>-1	restart the GUI without a shutdown</P>
<br>
<P>You can also add values together (but the -1 value must be called alone)...</P>
<P>The value of 13 consists of value 1 + 4 + 8 and will force the kill of all applications and
shutdown Windows with poweroff...</P>
<P>There is also a function called ExitWindowsEx() in Microsofts Visual C++ which does
exactly the same... but can't handle the -1 value !!!</P>
cu Agent_White

