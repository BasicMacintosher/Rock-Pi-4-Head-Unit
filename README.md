# Rock-Pi-4-Head-Unit
Build an Rock Pi 4b powered car head unit

# !! This Project is Work in Progress!!

## To Do ##
- [ ] Microfon in calls currently not working 
- [ ] Build and test the second version of the media buttons
- [ ] integrate the display in my car (I cant build a mount for every car but will test it with my ford fiesta mk6)


I bought a Rock Pi 4 with the intention to build a Car head unit for my Car. 
Follow me on my journey through this project. 

I downloaded the official Android image for the Rock Pi 4. In my case, I bought the Rock Pi 4 model b as it was the only one available for purchase thanks to the chip shortage. 
[Download link](https://rock.sh/rockpi-android7-download)
The reason I went with Android 7 is that it runs faster on the Rock Pi and since it just serves as a base for the Project I didn't really care that it was outdated. From a security standpoint I'm not worried at all because it is not connected to the internet, so it doesn't matter. 

After the image was installed on the SD card I downloaded the Application that is needed to run the dongle I bought 
[Dongle](ttps://amzn.eu/d/6gC4eBJ)
App download: 121.40.123.198:8080/AutoKit/AutoKit.apk (the link is also on the box)

At this time, I could only test the setup on an 42-inch TV because my touch display didn't arrive jet. When i receive it, I will test it with the display and then 3D Print a box enclosure to test the setup in my Car and use it while I'm driving. 
For now, it works fine on the TV. 

The only thing to consider is, that if you have Wi-Fi somewhere, and you are planing to use it, the CarPlay dongle works over Wi-Fi so the connection to your home Wi-Fi will get disconnected. I don't think this is a huge bummer, but maybe a thing to note since I don't have Cellular data at my place. 

## - 10.09.2022  
The touch display did arrive and it worked flawlessly. 
I took two pictures how it looks right now. 
Im now designing a box to fit it all in and then test it in my car.

## - 11.09.2022
I installed the Display temporary in my car without the enclousure, because it fit somewhat and im only printig a small structure to support it while driving.  
Now im going to test it and get a few more things ready. 
[Car Mount](https://github.com/BasicMacintosher/Rock-Pi-4-Head-Unit/blob/main/Picutres/Car_Mount.jpeg)


## - 22.10.2022  
The Mount for the Display is not as I antisipated at the beginning. 
I found an old phone holder in my car and im going to use it to secure the Display. 
The file for the Mount is attached in the "Files" folder. 
I am currently testing it and eliminating a few issues like the Microfone of my car not beeing picked up. 
The Steering wheel control on my car arent working either. To solve this issue, I programmed an Raspberry pi pico to use buttons I soldered to it as media buttons and it workes. 
Because the design is not yet finished, I didnt include the cad files nor the code for the Pico because I want to alter it 

## - 01.11.2022  
I created an enclousure for the Rock Pi and an Battery Backup System which I bought of off amazon. [Battery Backup](https://www.amazon.de/-/en/gp/product/B07KXRZ779/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1)
The acrylic case the Battery Board comes with and the tall stand offs have no use for me because it is to bulky for me and I wanted an Integrated design. 
So I designed my own Case  for it. 
![Rock Pi 4 case](https://github.com/BasicMacintosher/Rock-Pi-4-Head-Unit/blob/main/Files/Rock_Pi_4_case_with_Battery.step.stl)  
To mount the components to the Case, I used the included mounting screws and the small standoffs along with some M2 nuts I had laying arround. For the Rock Pi I used some M3 screews and nuts.
After I drilled a few M3 or M2 holes in the case I could mount the components to the case. 
![Picutre of the Case](https://github.com/BasicMacintosher/Rock-Pi-4-Head-Unit/blob/main/Picutres/Case_with_Battery.jpeg)

## - 07.12.2022
By now I have two versions of the car media controler. Both are build around the Raspberry Pi Pico (witch is actually in stock at least in germany) and a few push buttons. The secend version I made als has an Joystick because the dispaly was a bit unconvortable to reach while diriving so I made the joystick control act as an mouse to control the display convortable. 
Sadly I'm not quiet finished jet so I can only write about the first version witch run without a problem. 
#### V1 Media Control #### 
It has three buttons (I used some mechanical buttons I had laying arround but these ones are similar [mechanical buttons](https://www.amazon.de/-/en/Cherry-Switches-Mechanical-Keyboard-Replacement/dp/B08SK47VDX/ref=dp_prsubs_1?pd_rd_w=9Dfkl&content-id=amzn1.sym.85e12063-5122-4149-bea0-850be1f2d6fb&pf_rd_p=85e12063-5122-4149-bea0-850be1f2d6fb&pf_rd_r=TXTQ65X3V23RKC0E6E2S&pd_rd_wg=DHPxH&pd_rd_r=97320573-eb64-4131-b339-d626eed951cf&pd_rd_i=B08SK47VDX&psc=1)) 
The files can be found here: [cad file](https://github.com/BasicMacintosher/Rock-Pi-4-Head-Unit/blob/main/Files/car_media_control%20v1.stl)
the Raspberry Pi pico has been mounted outside of the enclousure to keep the housing low profile. The RPI Pico and the buttons were connected with an old USB cable with I removed both end of and used the conductors to connect each button seperatly with a common ground. [wiring diagramm of the pi](https://github.com/BasicMacintosher/Rock-Pi-4-Head-Unit/blob/main/Files/Car_Controll_Schematic_Version_1.pdf)
Currently I am printing the housing for verion 2 and as soon as I get some time testing it I will post it here. 

## - 19.12.2022
Today I created the second verion of the media buttons. The Design can mount to the steering wheel (watch out for compatibility with you car). The design is split into the buttons, the joystick for mouse input and the raspberry pi pico which are all seperated. The buttons are located on the inner side of the steering wheel, the joystick will be mounted to the car handle (the case is not finished yet), and the rasperry pi is located where ever is space. [steering wheel control](https://github.com/BasicMacintosher/Rock-Pi-4-Head-Unit/blob/main/Files/steering_wheel_control.stl) (an .step file is also avaible in the "file" folder).
In the following days I will test the design and also work on the joystick. 