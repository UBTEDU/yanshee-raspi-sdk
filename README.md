# Yanshee-Raspi-SDK(not use now)

## TO ALL

This old version Yanshee-Raspi-SDK is no longer used and maintained. Please use the new SDK URL address as follows:
http://yandev.ubtrobot.com/ 

Have fun!



### Overview of the Yanshee-Raspi-SDK(Yanshee-SDK)

The Yanshee-sdk provides arm-linux based c and python library that allows developers to control YanShee robot


### Hardware
 
1. Yanshee robot(Ex. Raspberry Pi 3 Main board)
2. Monitor
3. Output cable (Ex. HDMI-DVI/HDMI-VGA/HDMI-HDMI)
4. USB cable/wireless(Recommond)  mouse
5. Stick sensors(Ex. infrared sensor) 


### Software

1. Ex. NOOBS developing system
[Go to official website] (https://www.raspberrypi.org/downloads/noobs/) 


### Get started


1. Prepare your workspace and download the SDK <br>
We recommend running these commands from the home directory (~/) or Desktop; however, you can run the script anywhere.

```bash
sudo apt-get -y install doxygen swig
git clone https://github.com/UBTEDU/Yanshee-Raspi-SDK.git
```


2. Compile the files <br>
After compile the SDK, the doc, libs and python example are installed to "output" directory.
This guide presumes that the SDK is in {YANSHEE_SDK}, which we will presume is your home directory. If you choose to use different folder names, please update the commands throughout this guide accoringly:


```bash
export YANSHEE_SDK=/home/pi/Yanshee-Raspi-SDK
cd $YANSHEE_SDK
make
```


3. Set up dynamic library path <br>
Please make sure your application can find these LIBs.


```bash
export LD_LIBRARY_PATH=$YANSHEE_SDK/output/libs/:$LD_LIBRARY_PATH
```


4. Install python module and library <br>

```bash
cd $YANSHEE_SDK/output/python/
sudo python setup.py install
```
PS:MAKE SURE RobotApi.py AND _RobotApi.so ARE IN THE FOLDER /usr/local/lib/python2.7/dist-packages  

5. Execute and learn the example <br>
This is an example of how to control the robot to hit left. There are some other examples in "$YANSHEE_SDK/output/python/example", you can try them if you want.

```bash
cd $YANSHEE_SDK/output/python/example
python ubtStartRobotAction.py
```


6. Build your own project <br>
Befor you build your own project, you can find the SDK APIs in the below directory. After you enter the doc directory, please use your web browser to open "index.html". The documentation is generated by doxygen.

```bash
cd $YANSHEE_SDK/output/doc/
```
