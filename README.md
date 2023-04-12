# LogStash Config File

<h2> 1. Please refer to the "Configs" Folder for the corresponding LogStash Config File: </h2>
<b> https://github.com/gitahn11/LogStash/Configs </b>

<h2> 2. Below is the breakdown of LogStash Config File to ingest, standardize, and output a standard Syslog event:</h1>

<p> This Logstash configuration file is designed to ingest a syslog message from the console using the "stdin input" plugin, parse it using the "grok" and "kv" filter plugins, and then transform the data using the "mutate" filter plugin before outputting it to the console using the "stdout output" plugin. The "grok" filter plugin is used to parse the syslog message into various fields like timestamp, host, source, pid, and body, while the "kv" filter plugin is used to split the body field into key-value pairs. The "mutate" filter plugin is then used to rename and transform various fields like alertname, computername, computerip, and severity before removing unnecessary fields like timestamp, host, alertname, computername, and computerip. Finally, the "stdout output" plugin is used to print the transformed data to the console in a Ruby debug format. </p>


<h2> 3. Below is an example of a SysLog event and a screen capture of the console output after LogStash has ingested, parsed, and outputted the data: </h2>

<p> SysLog Event: <14>1 2016-12-25T09:03:52.754646-06:00 contosohost1 antivirus 2496 -- alertname=”Virus Found” computername=”contosopc42” computerip=”216.58.194.142” severity=”1” </p> 

<img src = "https://github.com/gitahn11/Logstash/blob/main/Files/LogStash%20Output.png"> 

