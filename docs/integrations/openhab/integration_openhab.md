# Installation and Example

<h2>Page Layout</h2>

![Screenshot](../../assets/images/screenshots/demo_jaffa1.png)
![Screenshot](../../assets/images/screenshots/demo_jaffa2.png)
![Screenshot](../../assets/images/screenshots/demo_jaffa3.png)

We call _plate_ any device running openHASP in your system.

## Installation

The openHAB configuration files to have this demo load automatically can be found [here](https://github.com/HASwitchPlate/openHASP-demo){target=_blank}.

Update the IP-address for your MQTT-broker in the `haspLVGL_demo.things` file. 

Make sure you have your plate connected to the network and to your MQTT boker, and your topic is set to `demo_plate`.

## Code

To add an openhasp plate to your installation with Jaffa Sunrise sample configuration, upload a `pages.jsonl` file with the folowing content to your plate:

- in the plate's web UI select `Mono` UI theme and reboot,
- upload a `pages.jsonl` file with the folowing content to your plate and reboot:

```json
{"page":1,"comment":"---------- Page 1 ----------"}
{"obj":"btn","id":4,"x":5,"y":5,"w":230,"h":58,"bg_color":"#000000","border_color":"#FFAC00","border_width":2,"radius":10,"radius1":10,"radius2":10,"text":"Lights On","value_ofs_x":-85,"value_font":32,"value_str":"\uE6E8","value_color":"#B6B6B6","text_color":"#B6B6B6","text_font":24}
{"obj":"btn","id":5,"x":5,"y":68,"w":230,"h":58,"bg_color":"#000000","border_color":"#FFAC00","border_width":2,"radius":10,"radius1":10,"radius2":10,"text":"Daylight","value_ofs_x":-85,"value_font":32,"value_str":"\uE599","value_color":"#B6B6B6","text_color":"#B6B6B6","text_font":24}
{"obj":"btn","id":6,"x":5,"y":131,"w":230,"h":58,"bg_color":"#000000","border_color":"#FFAC00","border_width":2,"radius":10,"radius1":10,"radius2":10,"text":"Night","value_ofs_x":-85,"value_font":32,"value_str":"\uE594","value_color":"#B6B6B6","text_color":"#B6B6B6","text_font":24}
{"obj":"btn","id":7,"x":5,"y":194,"w":230,"h":58,"bg_color":"#000000","border_color":"#FFAC00","border_width":2,"radius":10,"radius1":10,"radius2":10,"text":"Lights Off","value_ofs_x":-85,"value_font":32,"value_str":"\uE335","value_color":"#B6B6B6","text_color":"#B6B6B6","text_font":24}

{"page":2,"comment":"---------- Page 2 ----------"}
{"obj":"label","id":8,"x":5,"y":5,"w":230,"h":30,"bg_color":"#000000","border_color":"#C7BAA7","border_width":0,"radius":10,"radius1":10,"radius2":10,"text":"Kitchen Dimmer","text_color":"#B6B6B6","text_font":24}
{"obj":"label","id":9,"x":5,"y":80,"w":230,"h":30,"bg_color":"#000000","border_color":"#C7BAA7","border_width":0,"radius":10,"radius1":10,"radius2":10,"text":"Dining Dimmer","text_color":"#B6B6B6","text_font":24}
{"obj":"label","id":10,"x":5,"y":165,"w":230,"h":30,"bg_color":"#000000","border_color":"#C7BAA7","border_width":0,"radius":10,"radius1":10,"radius2":10,"text":"Front Blinds","text_color":"#B6B6B6","text_font":24}
{"obj":"slider","id":11,"x":20,"y":40,"w":200,"h":30,"bg_color":"#C7BAA7","border_color":"#C7BAA7","border_width":0,"radius":15,"radius1":15,"radius2":20,"text_font":1,"val":80,"bg_color1":"#FFAC00","bg_color2":"#DC5C05"}
{"obj":"slider","id":12,"x":20,"y":120,"w":200,"h":30,"bg_color":"#C7BAA7","border_color":"#C7BAA7","border_width":0,"radius":15,"radius1":15,"radius2":20,"text_font":1,"val":65,"bg_color1":"#FFAC00","bg_color2":"#DC5C05"}
{"obj":"slider","id":13,"x":20,"y":205,"w":200,"h":30,"bg_color":"#C7BAA7","border_color":"#C7BAA7","border_width":0,"radius":15,"radius1":15,"radius2":20,"text_font":1,"val":25,"bg_color1":"#FFAC00","bg_color2":"#DC5C05"}

{"page":3,"comment":"---------- Page 3 ----------"}
{"obj":"label","id":14,"x":42,"y":10,"w":236,"h":30,"bg_color":"#000000","border_color":"#C7BAA7","border_width":0,"text":"Gold","text_color":"#C7BAA7","text_font":24}
{"obj":"label","id":15,"x":42,"y":60,"mode":"scroll","w":236,"h":30,"bg_color":"#000000","border_color":"#C7BAA7","border_width":0,"text":"Chet Faker","text_color":"#C7BAA7","text_font":24}
{"obj":"btn","id":16,"x":2,"y":140,"w":76,"h":61,"bg_color":"#000000","border_color":"#FFAC00","border_width":2,"radius":10,"radius1":10,"radius2":10,"text":"\uE4AE","text_color":"#C7BAA7","text_font":32}
{"obj":"btn","id":17,"x":82,"y":140,"w":76,"h":61,"bg_color":"#000000","border_color":"#FFAC00","border_width":2,"radius":10,"radius1":10,"radius2":10,"text":"\uE3E4","text_color":"#C7BAA7","text_font":32}
{"obj":"btn","id":18,"x":162,"y":140,"w":76,"h":61,"bg_color":"#000000","border_color":"#FFAC00","border_width":2,"radius":10,"radius1":10,"radius2":10,"text":"\uE4AD","text_color":"#C7BAA7","text_font":32}
{"obj":"bar","id":19,"x":2,"y":105,"w":236,"h":20,"bg_color":"#C7BAA7","border_color":"#C7BAA7","border_width":0,"radius":15,"radius1":15,"radius2":15,"text_font":1,"val":65,"bg_color1":"#FFAC00"}
{"obj":"slider","id":20,"x":35,"y":220,"w":170,"h":30,"bg_color":"#C7BAA7","border_color":"#C7BAA7","border_width":0,"radius":15,"radius1":15,"radius2":20,"text_font":1,"val":30,"bg_color1":"#FFAC00","bg_color2":"#DC5C05"}
{"obj":"label","id":21,"x":2,"y":10,"w":40,"h":61,"bg_color":"#000000","border_color":"#C7BAA7","border_width":0,"text":"\uE75A","text_color":"#C7BAA7","text_font":24}
{"obj":"label","id":22,"x":2,"y":60,"w":36,"h":61,"bg_color":"#000000","border_color":"#C7BAA7","border_width":0,"text":"\uE004","text_color":"#C7BAA7","text_font":24}
{"obj":"label","id":23,"x":5,"y":224,"w":25,"h":40,"bg_color":"#000000","border_color":"#C7BAA7","border_width":0,"text":"\uE75F","text_color":"#C7BAA7","text_font":24}
{"obj":"label","id":24,"x":210,"y":224,"w":25,"h":40,"bg_color":"#000000","border_color":"#C7BAA7","border_width":0,"text":"\uE57E","text_color":"#C7BAA7","text_font":24}

{"page":0,"comment":"---------- All pages ----------"}
{"obj":"btn","id":1,"x":5,"y":257,"w":73,"h":58,"bg_color":"#000000","border_color":"#C7BAA7","border_width":0,"radius":10,"radius1":10,"radius2":10,"text":"\uE04D","text_color":"#978B7D","text_font":32}
{"obj":"btn","id":2,"x":83,"y":257,"w":73,"h":58,"bg_color":"#000000","border_color":"#C7BAA7","border_width":0,"radius":10,"radius1":10,"radius2":10,"text":"\uE2DC","text_color":"#978B7D","text_font":32}
{"obj":"btn","id":3,"x":161,"y":257,"w":73,"h":58,"bg_color":"#000000","border_color":"#C7BAA7","border_width":0,"radius":10,"radius1":10,"radius2":10,"text":"\uE054","text_color":"#978B7D","text_font":32}
```

Restart the plate and the demo page should load automatically to your device.

# More Example Rules
```javascript
/* BACKLIGHT DIM ON IDLE */
rule "openHASP Display Backlight DIM on idle, return to Page 1 and Screensaver"
    when
        Item openHASP_Plate_Idle received update short
    then
        var idleday = '{"state":"on","brightness":10}'
        var idlenight = '{"page":0,"id":99,"obj":"obj","x":0,"y":0,"w":240,"h":320,"radius":0,"hidden":0,"bg_grad_dir":0,"bg_color":"black"}'
        var Number hour = now.getHour	
            if ((hour >= 0)  || (hour <= 6)) {
                openHASP_Plate_Page_Current.sendCommand("1")   
                openHASP_Plate_Command_JSON.sendCommand("['backlight " + idleday +"']")
            }
            else    {
                openHASP_Plate_Page_Current.sendCommand("1")       
                openHASP_Plate_Command_JSON.sendCommand("['" + idlenight +"']")
                openHASP_Plate_Command_JSON.sendCommand("['backlight off']")
            }
end

rule "openHASP Display Backlight DIM off"
    when
        Item openHASP_Plate_Idle received update off
    then
        var idleoff = '{"state":"on","brightness":255}'
        var Number hour = now.getHour
            if ((hour >= 0)  || (hour <= 6)) {
                openHASP_Plate_Command_JSON.sendCommand("['backlight " + idleoff +"']")
            }
            else    {
                openHASP_Plate_Command_JSON.sendCommand("['p0b99.hidden=1','p0b99.delete=']")
                openHASP_Plate_Command_JSON.sendCommand("['backlight " + idleoff +"']")
            }
end

/* TEMPERATURE UPDATE */
rule "openHASP Temperature Update"
when
    Item localCurrentTemperature received update or
    Item openHASP_Plate_Page_Current received update 1 or
    Item openHASP_Plate_LWT received update
then
    if (openHASP_Plate_Page_Current.state == 1)   //Only update page if you're on page 1 (avoid sending too many MQTT messages)
    {
        openHASP_Plate_Command_JSON.sendCommand("['p1b2.value_str=" + localCurrentTemperature.state.format("%.1f") + "']")
    }
end

/* MOODLIGHT VIA COLORPICKER */
rule "openHASP CHANNEL TRIGGERED"
    when
        Channel "mqtt:broker:openHASPBroker:openHASP_Plate_State_Event" triggered
    then
        logInfo("openHASP_channel.rules", " Channel triggered: {} ",  receivedEvent)

        var topic = receivedEvent.toString.split("#").get(0)
        var payload = receivedEvent.substring(topic.length+1,receivedEvent.length)
        var topicvalue = topic.split("/").get(topic.split("/").size -1)
        var jsonkey = transform("JS","json_demo_key.js",payload)
        var jsonvalue = transform("JSONPATH", "$." + jsonkey, payload).toString.toUpperCase

        logInfo("openHASP_channel.rules", " Topic: {} [{}] Payload: {}",  topic, topicvalue , payload)

        switch (topicvalue)
        {
            case 'idle':
            {
                logInfo("openHASP_channel.rules", " Idle event: {}",  payload)
            }
            case 'statusupdate':
            {
                logInfo("openHASP_channel.rules", " Statusupdate: {}",  payload)
            }
            case 'dim':
            {
                logInfo("openHASP_channel.rules", " Dim: {}",  payload)
            }
            case 'page':
            {
                logInfo("openHASP_channel.rules", " Page: {}",  payload)
                postUpdate(openHASP_Plate_Page_Current, payload)
            }
            case 'input':
            {
                logInfo("openHASP_channel.rules", " Input: {}",  payload)
            }
            case 'sensors':
            {
                logInfo("openHASP_channel.rules", " Sensors: {}",  payload)
            }
            case 'backlight':
            {
                logInfo("openHASP_channel.rules", " Backlight: {}",  payload)
            }
            case 'moodlight':
            {
                logInfo("openHASP_channel.rules", " Moodlight: {}",  payload)
            }
            default:
            {
                var eventpage = topicvalue.split("b").get(0).split("p").get(1)
                var eventbutton = topicvalue.split("b").get(1)

                logInfo("openHASP_channel.rules", " Page: {} Button: {} Key: {} Value: {}",  eventpage, eventbutton, jsonkey, jsonvalue)

                switch(eventpage)
                {
                    case '1':
                    {
                        switch(eventbutton)
                        {
                            case '2':
                            {
                                if(jsonkey == "event" && jsonvalue == "UP")
                                {
                                    var String stat
                                    if (switch1.state == null || switch1.state == OFF){
                                        switch1.sendCommand(ON)
                                        stat = "ON"
                                    } else {
                                        switch1.sendCommand(OFF)
                                        stat = "OFF"
                                    }
                                    openHASP_Plate_Command_JSON.sendCommand("[''p1b2.value_str=" + stat + "']")
                                }
                            }
                        }
                    }
/* MOODLIGHT VIA COLORPICKER */
                    case '2':   // Colorpicker Page ID
                        switch(eventbutton)
                        {
                            case '2':   // Colorpicker Button ID
                            {
                                if(jsonkey == "event" && jsonvalue == "UP")
                                {
                                    var colorpicker = receivedEvent.toString.split('"').get(7)
                                    var moodlight = '{"state":"on","brightness":255,"color":"' + colorpicker + '"}'
                                    openHASP_Plate_Command_JSON.sendCommand("['moodlight " + moodlight + "']")
                                }
                            }
                            case '3':
                            {
                                if(jsonkey == "event" && jsonvalue == "UP")
                                {
                                    openHASP_Plate_Moodlight_OFF.sendCommand(ON)
                                }
                            }
                        }
                }
                
            }
        }
    end
```
