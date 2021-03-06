# Sysmon
Podstawowa konfiguracja i wdrożenie Syinternals [Sysmon](https://technet.microsoft.com/en-us/sysinternals/sysmon) oraz monitoring z wykorzystaniem [Splunk'a](https://splunk.com)

### Instalacja

Pobieramy [Sysmona](https://technet.microsoft.com/en-us/sysinternals/sysmon), umieszczamy **poza** ścieżką `C:\Users` i instalujemy poleceniem z konsoli:
```
sysmon -i -n -accepteula
```
lub jeśli posiadamy config i znajduje się on w tym samym folderze:

```
sysmon -i sysmon_config.xml -n -accepteula
```
i to by było na tyle. Serio :)

Możemy ewentualnie zmienić rozmiar bufa Windows Event Loga.

### Sysmon Config

1. Najpopularniejszy config [SwiftOnSecurity](https://github.com/SwitfOnSecurity/sysmon-conf)
2. Fork Swift'a wyedytowany pod serwery [ion-storm](https://github.com/ion-storm/sysmon-config/blob/master/sysmonconfig-export.xml)

## Splunk

### Konfiguracja źródła
Należy dodać jedynie odbieranie zdarzeń na wskazanym porcie. 
Ewentualnie można dodać nowy index pod zdarzenia Sysmona ale konfiguracja tego jest już wedle uznania :)

## Splunk Universal Forwarder [KLIK](https://github.com/Ravikin/Sysmon/tree/master/SplunkUniversalForwarder)
Przykładowa konfiguracja forwardera Splunka na stacji monitorowanej.

- [inputs.conf](https://github.com/Ravikin/Sysmon/blob/master/SplunkUniversalForwarder/inputs.conf)
- [outputs.conf](https://github.com/Ravikin/Sysmon/blob/master/SplunkUniversalForwarder/outputs.conf)
