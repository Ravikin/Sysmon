# SPLUNK UNIVERSAL FORWARDER

Forwardera można skonfigurować edytując pliki konfiguracyjne (zalecane i dobrze opisane w [dokumentacji](https://docs.splunk.com/Documentation/Splunk/6.5.2/Admin/Howtousethismanual))
- [inputs.conf](https://docs.splunk.com/Documentation/Splunk/6.5.2/Admin/Inputsconf)
- [outputs.conf](https://docs.splunk.com/Documentation/Splunk/6.5.2/Admin/Outputsconf)

Domyślne dane do logowania -> `admin:changeme`

Lub poprzed komendy wydawane z konsoli
```
C:\Program Files\SplunkUniversalForwarder\bin>splunk

Data forwarding configuration management tools.
  Commands:
      enable local-index [-parameter <value>] ...
      disable local-index [-parameter <value>] ...
      display local-index
      add forward-server server
      remove forward-server server
      list forward-server
  Objects:
      forward-server       a Splunk forwarder to forward data to be indexed
      local-index          a local search index on the Splunk server
```
Jest też oczywiście help:

```
C:\Program Files\SplunkUniversalForwarder\bin>splunk /?



Welcome to Splunk's Command Line Interface (CLI).

    Type these commands for more help:

        help [command]             type a command name to access its help page
        help [object]              type an object name to access its help page
        help [topic]               type a topic keyword to get help on a topic
        help commands              display a full list of CLI commands
        help clustering            commands that can be used to configure the clustering setup
        help shclustering          commands that can be used to configure the Search Head Cluster setup
        help control, controls     tools to start, stop, manage Splunk processes
        help datastore             manage Splunk's local filesystem use
        help distributed           manage distributed configurations such as
                                   data cloning, routing, and distributed search
        help forwarding            manage deployments
        help input, inputs         manage data inputs
        help licensing             manage licenses for your Splunk server
        help settings              manage settings for your Splunk server
        help simple, cheatsheet    display a list of common commands with syntax
        help tools                 tools to help your Splunk server
        help search                help with Splunk searches

    Universal Parameters:

        The following parameters are usable by any command. For more details on each parameter, type "help [parameter]".

Syntax:

        [command] [object] [-parameter <value> | <value>]... [-uri][-auth]

      app        specify the app or namespace to run the command; for search, defaults to
                 the Search app

      auth       specify login credentials to execute commands that require you to be logged in

      owner      specify the owner/user context associated with an object; if not specified,
                 defaults to the currently logged in user

      uri        execute a command on any specified Splunk server. Use the
                 format: <ip>:<port>

      Note: Both IPv4 and IPv6 formats are supported for specifying an IP address, for example:
      127.0.0.1:80 or "[2001:db8::1]:80". By default, splunkd listens on IPv4 only. To enable
      IPv6 support, refer to the instructions in:
      http://docs.splunk.com/Documentation/Splunk/latest/Admin/ConfigureSplunkforIPv6


Objects:

        None

Required Parameters:

        None

Optional Parameters:

        None

Examples:

        None

Type "help [command]" to get help with parameters for a specific command.

Complete documentation is available online at: http://docs.splunk.com/Documentation
```

## Przykładowe dodanie forwardu do serwera docelowego
`splunk add forward-server <address_ip>:<port>`
