# rockpis-systemd
systemd manager for rockpis

I servizi attivati tramite `systemd` sono programmati per essere eseguiti all'avvio del sistema, o periodicamente, o in base al verificarsi di determinate condizioni. Un esempio tipico è rappresentato da un servizio che all'avvio del sistema esegue uno script che gestisce il cambio di stato di un pin della scheda.

I servizi sono dei pezzi di software che eseguono compiti automatizzati. Nel sistema `systemd` di Linux i servizi vengono gestiti da un file con estensione `.service` che ne definisce i tempi e le modalità di esecuzione. Tali file di gestione sono posizionati nella directory `/usr/lib/systemd/system/`.

In questo progetto usiamo servizi per gestire quasi tutte le periferiche (GPIO, Serial e I2C), a cui sono connessi i led, il display oled, i pulsanti e la scheda ESP32.Analogamente, un servizio è attivo per eseguire all'avvio un'istanza di Puredata.

## Installazione dei servizi

Posizionare i file con estensione `.service` nella directory `/usr/lib/systemd/system/` e gli script che rappresentano i servizi estessi (generalmente con estensione `.py` o `.sh`) nella directory `/home/neum/services`
