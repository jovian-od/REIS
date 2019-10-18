#REIS  
>Ridiculously Elemental IoT Spec  

  

---    

##In short: A *thingy[1]* that implements REIS can be configured to do simple[2] IoT tasks by supplying it a simple JSON configuration file.

[1] Thingy can be an end user software application, physical device, or hybrid of the two.  

[2] Tasks are REST actions that have a REST verb, URL, and optional output

From the perspective of this specification an *endpoint* can be anything that implements input and/or output to an end user. 

The endpoints are specifically such devices, applications or services that communicate with a data source or other server applications. These are accessed from a very simple end user interface that this specification is wholly agnostic to.

* Endpoint may have input - text for class 2 application, binary button for class 1, or 0 for completely passive.  


* Endpoint may have output - text for class 2 app, a LED or other binary indicator for class 1, or 0 for no output device.

* Endpoint accesses an configured URL with the REST verb specified in the reisConfig.json file when end user performs the input task, like pressing a button or when programmed to do so otherwise. 

* Endpoint outputs the results of the input (with app specific formatting) on the output device. Binary class endpoints simply output a simple acknowledgement or optional pattern of light/sound/haptics. 