weak_classdump
==============
A Cycript script that generates a header file for the class passed to the function.

Most useful when you cannot classdump , when binaries are encrypted etc.

-------------------------------
Usage examples : 

	root# cycript -p Skype weak_classdump.cy; cycript -p Skype
	cy# UIApp
	"<HellcatApplication: 0x1734e0>"

	cy# weak_classdump(HellcatApplication);
	"Wrote file to /tmp/HellcatApplication.h"
	
	cy# UIApp.delegate
	"<SkypeAppDelegate: 0x194db0>"
	
	cy# weak_classdump(SkypeAppDelegate,"/someDirWithWriteAccess/");
	"Wrote file to /someDirWithWriteAccess/SkypeAppDelegate.h"
	
	


	
by Elias Limneos
----------------
web: limneos.net

email: iphone (at) limneos (dot) net

twitter: @limneos

Issues
-----------
It currently assumes every variable as (id), since I cannot get types from cycript class.messages approach.

Licence
-----------

weak_classdump is open source. Feel free to help improving it if you like.

Licence
-----------
weak_classdump works under Cycript. Visit cycript.org for more info.




