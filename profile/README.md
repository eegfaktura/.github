# eegfaktura
Public repository providing all information required to run your own `eegfaktura` instance.

`eegfaktura` is an open source project initiated by [Verein zur Förderung von Erneuerbaren Energiegemeinschaften ](https://vfeeg.org) to provide a free management and invoicing system for Energiegemeinschaften (EEG; lit. "energy community")

```mermaid
flowchart TD
    web[eegfaktura-web]
    web --> backend[eegfaktura-backend]
    web --> energystore[eegfaktura-energystore]
    web --> filestore[eegfaktura-filestore]
    web --> billing[eegfaktura-billing]

    filestore --> db[(db_filestore)]

    billing --> db

    eda[eegfaktura-eda-comm] --> db

    backend --> db
    backend --> mqtt@{ shape: lean-l, label: "mqttbroker" }

    energystore --> mqtt

    click web "https://github.com/eegfaktura/eegfaktura-web" "Open eegfaktura-web repo"
    click backend "https://github.com/eegfaktura/eegfaktura-backend" "Open eegfaktura-backend repo"
    click filestore "https://github.com/eegfaktura/eegfaktura-filestore" "Open eegfaktura-filestore repo"
    click eda "https://github.com/eegfaktura/eegfaktura-eda-comm" "Open eegfaktura-eda-comm"
    click energystore "https://github.com/eegfaktura/eegfaktura-energystore" "Open eegfaktura-energystore"
```
