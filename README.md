# Local-MQTT-Broker
Setup a Local MQTT broker on ESP compatible boards

# Step 1:
     Download uMQTT-Broker Library from here: https://github.com/martin-ger/uMQTTBroker and place
     it in Documents/Arduino/Libraries folder
# Step 2: 
     Upload Code on ESP Compatible Board. 

Once uploaded , ESP will start its own hotspot and Broker's Ip address will be displayed on Serial Monitor. 
You can test MQTT publish and subscribe by connecting to the hotspot and then using the
displayed IP address as Broker's address with port as 1883. 

# In order to Test:
    Download MQTT.fx from here: https://mqttfx.jensd.de/ and install. 
  
  After connecting to hotspot named as 'MQTTBroker' , Open MQTTFx and Click on Settings icon, 
  Write Broker's IP address, which you copied from Serial Minitor and write 1883 in Port, Click Apply/Ok 
  
 Once connection is established, go to Subscribe Tab, Write 'broker/counter' as topic , click Subscribe. 
 You will see the Stream of data coming which our Code is publishing continously. 
 
 You can also test the Publish functionality by going to 'Publish' tab, write a topic name, say 'Test', write a short
 message e.g 'Hello ESP' and click Publish. 
 Published message will be displayed in Serial Monitor. 
 
 ESP is by default listening to all the published data on any topics. 
 # You can change the line
                myBroker.subscribe("#"); Replace # with a specific topic name, so only the data published to
                that specific topic will be displayed.  
