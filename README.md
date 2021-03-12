# Zigbe_SS600ZB_automation
![alt text](https://github.com/alesoft73/Zigbee_SS600ZB_automation/blob/main/push_button.png)



My SS600ZB Wireless switch with 3 buttons (white-label of TuYa TS0043)

In my home i use push button for turn_on and turn_off my domestic appliances.

In the packages there is a script for managing the notification of the status of the appliance.
I also inserted an input_boolen in case you need an example.
The script is called with the following syntax:


            - service: script.notifica_elettrodomestico_acceso
              data_template:
                elettrodomestico: >-
                  switch.lavastoviglie #insert the name of switch to controlled in the TTS notify 


What is entered "switch.tutti" is for the notification of shutdown of all entities to be controlled.


Finally, two automations.

One for each Zigbee Device.
Each press is associated with an action which sends the notification of switching on and off to the media_plyaer.
You will notice that the notifications are directed to an internal script that I use in my Hub for managing notifications.
Package name is Notify

Italian

Nel packages è presente uno script per la gestione notifica dello stato dell'elettrodomestico.
Ho inserto anche un input_boolen nel caso servisse un esempio.
Lo script viene richiamato con la seguente sintassi:

            - service: script.notifica_elettrodomestico_acceso
              data_template:
                elettrodomestico: >-
                  switch.lavastoviglie # Va inserito l'eventuale elettrodomestico da far controllare nella notifica TTS per accension/spegnimento
                    
Quanto viene inserito "switch.tutti" e' per la notifica spegnimento di tutte le entità da controllare.

Infine due automazioni.
Una per ogni Device Zigbee.
Ad ogni pressione viene abbinata un'azione la quale invia al media_plyaer la notifica di accensione e spegnimento.
Noterete che le notifche vengono direzione ad uno script interno che uso nel mio Hub per la gestione delle notifiche.
Package denominato Notify.
