# Email-IPaddress-Startup
#We will go through setting up raspberry pi to email you everytime it starts. This is very helpful when the IP address can change.

#Create a folder on the pi where you will store your programs.
#  I like /home/pi/Mystuff
#In that folder save StartupIP.py
#Modify StartupIP.py and enter your information in the email settings
#Note: this program is sending out though gmail. You will need to change a few things if you are using different email host.
#Note: Using gmail - Go into gmail account settings/security and turn on less secure apps. This will prevent google from blocking emails being sent from devices like Rpi.

#Type
sudo nano /etc/rc.local 
#You will find #Print the IP address right below that and before the other code enter the following
python /home/pi/Mystuff/StartupIP.py $
# This will run the program everytime the raspberry pi is started.
