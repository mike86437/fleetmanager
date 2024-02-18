Standalone Fleet-Manager for style development.
I modified fleetmanager.py to support off-device flask server deployment in debug mode.

Works fine for me when deployed on a simple hyper-v ubuntu 22.04 server image
Steps I used to install required dependencies
sudo apt update 
sudo apt install python3 python3-pip ffmpeg
pip3 install Flask
git clone https://github.com/mike86437/fleetmanager
cd fleetmanager
python3 fleet_manager.py
Connect to local_ip:8082 as indicated in console

Which pages work:
Main landing 
Dashcam Footage index 
Dashcam Footage viewer
Screen Recordings viewer
Error Log index
Error Log viewer
About Fleet Manager
Navigation Landing

Which pages don't work:
Preserved Footage index
Nav address confirmation
Nav driving directions
