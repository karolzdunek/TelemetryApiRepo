# **Travelport Telemetry API**

With Travelport Telemetry API, you can easily monitor your application for usage, availability and performance. You can also quickly identify and diagnose errors in your application without waiting for a user to report them.

This quickstart guides you through adding the Travelport Telemetry API SDK to an existing ASP.Net applications (like Smartpoint App Plugin/Web App/Desctop App).

# Prerequisites

- .NET 4.6.2
- Visual Studio
- Reference to Newtonsoft.Json up to 6.0.0.0

# Enable Telemetry API

API can gather telemetry data from any internet-connected application, regardless of whether it's running on-premises or in the cloud. Use the following steps to start:

- Take product ID (int) you wish to log your telemetry.
- If your product not exists provision a new product to be added (contact Travelport Product Owner)
- Add SDK dll reference (together with config file) to your project
- Initialize telemetry engine object by creating new Telemetry object

![image.png](.attachments/image-d5835384-d70e-41bb-b781-00fc358e8736.png)
- Start using your telemetry API :)

![image.png](.attachments/image-f27465b1-180d-4b11-b44a-18c7ba68f43b.png)

# Examples:

<P class=MsoNormal><B>Log custom object &nbsp;example 1:</B></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">TelemetryHelper</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">.Instance.LogCustomObject(</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:blue">new</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"></SPAN></P>

<H2><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">{</SPAN></H2>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&nbsp;&nbsp;&nbsp; Prop1 = </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#A31515">&quot;value1&quot;</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">,</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&nbsp;&nbsp;&nbsp; Prop2 = 333 </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:green">//, ...</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"></SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">}, </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#A31515">&quot;optional label as data type&quot;</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">);</SPAN></P>

<P class=MsoNormal><B>Log custom object example 2:</B></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">TelemetryHelper</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">.Instance.LogCustomObject(</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:blue">new</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"> </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">ButtonsConfigClass</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"></SPAN></P>

<P class=MsoNormal><SPAN lang=PL style="font-size:
9.5pt;font-family:Consolas;color:black">{</SPAN></P>

<P class=MsoNormal><SPAN lang=PL style="font-size:
9.5pt;font-family:Consolas;color:black">&nbsp;&nbsp;&nbsp;
Url = </SPAN><SPAN lang=PL style="font-size:9.5pt;font-family:Consolas;color:#A31515">&quot;<A href="https://travelportee.visualstudio.com/Telemetry">https://travelportee.visualstudio.com/Telemetry</A>&quot;</SPAN><SPAN lang=PL style="font-size:9.5pt;font-family:Consolas;color:black">,</SPAN></P>

<P class=MsoNormal><SPAN lang=PL style="font-size:
9.5pt;font-family:Consolas;color:black">&nbsp;&nbsp;&nbsp;
</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">PersonalButtonsConfigFilePath
= </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#A31515">&quot;C:</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#FF007F">\\</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#A31515">config1.xml&quot; </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:green">//, ....</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"></SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">});</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&nbsp;</SPAN></P>

<P class=MsoNormal><B><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">Log launch event example:</SPAN></B></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">TelemetryHelper</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">.Instance.LogLaunchEvent();</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&nbsp;</SPAN></P>

<P class=MsoNormal><B><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">Log exception message example:</SPAN></B></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">TelemetryHelper</SPAN><SPAN style="font-size:9.5pt;font-family:
Consolas;color:black">.Instance.LogException(</SPAN><SPAN style="font-size:
9.5pt;font-family:Consolas;color:#A31515">&quot;Some self-explanatory error
message :)&quot;</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">);</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&nbsp;</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&nbsp;</SPAN></P>

<P class=MsoNormal><B><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">Initialization (add to first line at Plugin.cs):</SPAN></B></P>

<P class=MsoNormal>&nbsp;</P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:blue">var</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"> logAction = </SPAN><SPAN style="font-size:
9.5pt;font-family:Consolas;color:blue">new</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"> </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">Action</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&lt;</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">Exception</SPAN><SPAN style="font-size:
9.5pt;font-family:Consolas;color:black">&gt;(ex =&gt;</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">{</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&nbsp;&nbsp;&nbsp; </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:green">//use your logger
here:)</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"></SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">});</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&nbsp;</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:blue">var</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"> getCurrentPccFunc = </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:blue">new</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"> </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">Func</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&lt;</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:blue">string</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&gt;(() =&gt;</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">{</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&nbsp;&nbsp;&nbsp; </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:blue">return</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"> </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">UIHelper</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">.Instance.CurrentTEControl.Connection.CommunicationFactory.GetCurrentPcc();</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">});</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">&nbsp;</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:blue">var</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"> assemblyPath = </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:blue">new</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"> </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">Uri</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">(</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">Assembly</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">.GetExecutingAssembly().CodeBase).LocalPath;</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:blue">var</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"> version = System.Reflection.</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">AssemblyName</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">.GetAssemblyName(assemblyPath).Version;</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:blue">var</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"> telemetry = </SPAN><SPAN style="font-size:
9.5pt;font-family:Consolas;color:blue">new</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black"> </SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF;background:lime">TelemetryEngine</SPAN><SPAN style="font-size:9.5pt;font-family:Consolas;color:black">(1,
version.ToString(), 10, 30, logAction);</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">CoreHelper</SPAN><SPAN style="font-size:
9.5pt;font-family:Consolas;color:black">.Instance.OnSmartpointClose += (s, o)
=&gt; telemetry.SaveAllAndClose();</SPAN></P>

<P class=MsoNormal><SPAN style="font-size:9.5pt;font-family:Consolas;color:#2B91AF">TelemetryHelper</SPAN><SPAN style="font-size:9.5pt;font-family:
Consolas;color:black">.Instance.SetCurrentPcc = getCurrentPccFunc;</SPAN></P>

## **Store telemetry logs API endpoint:** 
https://travelportee.eu/telemetryapi/api/storelogs
(POST of array of telemetry object with schema described below)


## **Telemetry log object schema:**

<PRE style="margin: 10px 0px 0px;font-family: &amp;quot;padding: 10px;white-space: pre-wrap;font-size: 12.6px;line-height: 1.6;color: rgba(0, 0, 0, 0.87);font-style: normal;font-weight: normal;letter-spacing: normal;text-align: start;text-indent: 0px;text-transform: none;word-spacing: 0px;background-color: rgb(255, 255, 255)"><SPAN class="lineno">  1 </SPAN><SPAN class="p">{</SPAN>
<SPAN class="lineno">  2 </SPAN>   <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno">  3 </SPAN>   <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"array"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno">  4 </SPAN>   <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"definitions"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{},</SPAN> 
<SPAN class="lineno">  5 </SPAN>   <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$schema"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://json-schema.org/draft-07/schema#"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno">  6 </SPAN>   <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"items"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno">  7 </SPAN>      <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json/items"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno">  8 </SPAN>      <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"object"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno">  9 </SPAN>      <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"properties"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno"> 10 </SPAN>         <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"ActivityId"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno"> 11 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json/items/properties/ActivityId"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 12 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"integer"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 13 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"title"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"The Activityid Schema "</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 14 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"default"</SPAN><SPAN class="p">:</SPAN> <SPAN class="mi" style="color: rgb(180, 82, 205)">0</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 15 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"examples"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">[</SPAN>
<SPAN class="lineno"> 16 </SPAN>               <SPAN class="mi" style="color: rgb(180, 82, 205)">1</SPAN>
<SPAN class="lineno"> 17 </SPAN>            <SPAN class="p">]</SPAN>
<SPAN class="lineno"> 18 </SPAN>         <SPAN class="p">},</SPAN> 
<SPAN class="lineno"> 19 </SPAN>         <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"DateAddedUtc"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno"> 20 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json/items/properties/DateAddedUtc"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 21 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"string"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 22 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"title"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"The Dateaddedutc Schema "</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 23 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"default"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">""</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 24 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"examples"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">[</SPAN>
<SPAN class="lineno"> 25 </SPAN>               <SPAN class="s2" style="color: rgb(205, 85, 85)">"2018-03-01T08:34:25"</SPAN>
<SPAN class="lineno"> 26 </SPAN>            <SPAN class="p">]</SPAN>
<SPAN class="lineno"> 27 </SPAN>         <SPAN class="p">},</SPAN> 
<SPAN class="lineno"> 28 </SPAN>         <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"Version"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno"> 29 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json/items/properties/Version"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 30 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"string"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 31 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"title"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"The Version Schema "</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 32 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"default"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">""</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 33 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"examples"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">[</SPAN>
<SPAN class="lineno"> 34 </SPAN>               <SPAN class="s2" style="color: rgb(205, 85, 85)">"1.0.0.0"</SPAN>
<SPAN class="lineno"> 35 </SPAN>            <SPAN class="p">]</SPAN>
<SPAN class="lineno"> 36 </SPAN>         <SPAN class="p">},</SPAN> 
<SPAN class="lineno"> 37 </SPAN>         <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"ExceptionMessage"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno"> 38 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json/items/properties/ExceptionMessage"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 39 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"string"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 40 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"title"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"The Exceptionmessage Schema "</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 41 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"default"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">""</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 42 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"examples"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">[</SPAN>
<SPAN class="lineno"> 43 </SPAN>               <SPAN class="s2" style="color: rgb(205, 85, 85)">"some exception message"</SPAN>
<SPAN class="lineno"> 44 </SPAN>            <SPAN class="p">]</SPAN>
<SPAN class="lineno"> 45 </SPAN>         <SPAN class="p">},</SPAN> 
<SPAN class="lineno"> 46 </SPAN>         <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"ActivityType"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno"> 47 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json/items/properties/ActivityType"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 48 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"integer"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 49 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"title"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"The Activitytype Schema "</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 50 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"default"</SPAN><SPAN class="p">:</SPAN> <SPAN class="mi" style="color: rgb(180, 82, 205)">0</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 51 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"examples"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">[</SPAN>
<SPAN class="lineno"> 52 </SPAN>               <SPAN class="mi" style="color: rgb(180, 82, 205)">1</SPAN>
<SPAN class="lineno"> 53 </SPAN>            <SPAN class="p">]</SPAN>
<SPAN class="lineno"> 54 </SPAN>         <SPAN class="p">},</SPAN> 
<SPAN class="lineno"> 55 </SPAN>         <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"JsonCustomObject"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno"> 56 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json/items/properties/JsonCustomObject"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 57 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"string"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 58 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"title"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"The Jsoncustomobject Schema "</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 59 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"default"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">""</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 60 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"examples"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">[</SPAN>
<SPAN class="lineno"> 61 </SPAN>               <SPAN class="s2" style="color: rgb(205, 85, 85)">"{...}"</SPAN>
<SPAN class="lineno"> 62 </SPAN>            <SPAN class="p">]</SPAN>
<SPAN class="lineno"> 63 </SPAN>         <SPAN class="p">},</SPAN> 
<SPAN class="lineno"> 64 </SPAN>         <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"JsonCustomObjectType"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno"> 65 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json/items/properties/JsonCustomObjectType"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 66 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"string"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 67 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"title"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"The Jsoncustomobjecttype Schema "</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 68 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"default"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">""</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 69 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"examples"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">[</SPAN>
<SPAN class="lineno"> 70 </SPAN>               <SPAN class="s2" style="color: rgb(205, 85, 85)">"SbWarnMsg"</SPAN>
<SPAN class="lineno"> 71 </SPAN>            <SPAN class="p">]</SPAN>
<SPAN class="lineno"> 72 </SPAN>         <SPAN class="p">},</SPAN> 
<SPAN class="lineno"> 73 </SPAN>         <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"Pcc"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno"> 74 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json/items/properties/Pcc"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 75 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"string"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 76 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"title"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"The Pcc Schema "</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 77 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"default"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">""</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 78 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"examples"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">[</SPAN>
<SPAN class="lineno"> 79 </SPAN>               <SPAN class="s2" style="color: rgb(205, 85, 85)">"YYYY"</SPAN>
<SPAN class="lineno"> 80 </SPAN>            <SPAN class="p">]</SPAN>
<SPAN class="lineno"> 81 </SPAN>         <SPAN class="p">},</SPAN> 
<SPAN class="lineno"> 82 </SPAN>         <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"ClientId"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno"> 83 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json/items/properties/ClientId"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 84 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"string"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 85 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"title"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"The Clientid Schema "</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 86 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"default"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">""</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 87 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"examples"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">[</SPAN>
<SPAN class="lineno"> 88 </SPAN>               <SPAN class="s2" style="color: rgb(205, 85, 85)">"g1234567"</SPAN>
<SPAN class="lineno"> 89 </SPAN>            <SPAN class="p">]</SPAN>
<SPAN class="lineno"> 90 </SPAN>         <SPAN class="p">},</SPAN> 
<SPAN class="lineno"> 91 </SPAN>         <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"LaunchDate"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno"> 92 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json/items/properties/LaunchDate"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 93 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"string"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 94 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"title"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"The Launchdate Schema "</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 95 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"default"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">""</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno"> 96 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"examples"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">[</SPAN>
<SPAN class="lineno"> 97 </SPAN>               <SPAN class="s2" style="color: rgb(205, 85, 85)">"2018-03-01T08:34:23"</SPAN>
<SPAN class="lineno"> 98 </SPAN>            <SPAN class="p">]</SPAN>
<SPAN class="lineno"> 99 </SPAN>         <SPAN class="p">},</SPAN> 
<SPAN class="lineno">100 </SPAN>         <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"ProductRefId"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">{</SPAN>
<SPAN class="lineno">101 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"$id"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"http://example.com/example.json/items/properties/ProductRefId"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno">102 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"type"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"integer"</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno">103 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"title"</SPAN><SPAN class="p">:</SPAN> <SPAN class="s2" style="color: rgb(205, 85, 85)">"The Productrefid Schema "</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno">104 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"default"</SPAN><SPAN class="p">:</SPAN> <SPAN class="mi" style="color: rgb(180, 82, 205)">0</SPAN><SPAN class="p">,</SPAN> 
<SPAN class="lineno">105 </SPAN>            <SPAN class="nt" style="color: rgb(139, 0, 139);font-weight: 700">"examples"</SPAN><SPAN class="p">:</SPAN> <SPAN class="p">[</SPAN>
<SPAN class="lineno">106 </SPAN>               <SPAN class="mi" style="color: rgb(180, 82, 205)">1</SPAN>
<SPAN class="lineno">107 </SPAN>            <SPAN class="p">]</SPAN>
<SPAN class="lineno">108 </SPAN>         <SPAN class="p">}</SPAN>
<SPAN class="lineno">109 </SPAN>      <SPAN class="p">}</SPAN>
<SPAN class="lineno">110 </SPAN>   <SPAN class="p">}</SPAN>
<SPAN class="lineno">111 </SPAN><SPAN class="p">}</SPAN></PRE>
