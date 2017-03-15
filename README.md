# Sysmon
Podstawowa konfiguracja i wdrożenie Syinternals [Sysmon](https://technet.microsoft.com/en-us/sysinternals/sysmon)

### Instalacja

Pobieramy [Sysmona](https://technet.microsoft.com/en-us/sysinternals/sysmon), umieszczamy poza ścieżką C:\Users i instalujemy poleceniem z konsoli:
```
sysmon -i -n -accepteula
```
lub jeśli posiadamy konfig i znajduje się on w tym samym folderze:

```
sysmon -i sysmon_config.xml -n -accepteula
```

## Splunk Universal Forwarder [KLIK](https://github.com/Ravikin/Sysmon/tree/master/SplunkUniversalForwarder)
Przykładowa konfiguracja forwardera Splunka na stacji monitorowanej.

## Splunk

## Sysmon Config
