# LogStash Config File

<h2> Below is the breakdown of LogStash Config File to ingest, standardize, and output a standard Syslog <h2>

<p1> This Logstash configuration file is designed to ingest a syslog message from the console using the stdin input plugin, parse it using the grok and kv filter plugins, and then transform the data using the mutate filter plugin before outputting it to the console using the stdout output plugin. The grok filter plugin is used to parse the syslog message into various fields like timestamp, host, source, pid, and body, while the kv filter plugin is used to split the body field into key-value pairs. The mutate filter plugin is then used to rename and transform various fields like alertname, computername, computerip, and severity before removing unnecessary fields like timestamp, host, alertname, computername, and computerip. Finally, the stdout output plugin is used to print the transformed data to the console in a Ruby debug format. <p1>
