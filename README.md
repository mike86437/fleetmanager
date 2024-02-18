# Standalone Fleet-Manager for style development.
## I modified fleetmanager.py to support off-device flask server deployment in debug mode. Works fine for me when deployed on a simple hyper-v ubuntu 22.04 server image.

### Steps I used to install required dependencies:
1. ```sudo apt update ```
2. ```sudo apt install python3 python3-pip ffmpeg```
3. ```pip3 install Flask```
4. ```git clone https://github.com/mike86437/fleetmanager```
5. ```cd fleetmanager```
6. ```python3 fleet_manager.py```

### Connect to local_ip:8082 as indicated in console.
#### Which pages work:
1. Main landing
   - ```local_ip:8082```
   - jinja template -> layout.html + index.html
3. Dashcam Footage index
   - ```local_ip:8082/footage```
   - jinja template -> layout.html + footage.html
5. Dashcam Footage viewer
   - ```local_ip:8082/footage/<route>```
   - jinja template -> layout.html + route.html
7. Screen Recordings viewer
   - ```local_ip:8082/screenrecords```
   - jinja template -> layout.html + screenrecords.html
9. Error Log index
   - ```local_ip:8082/error_logs```
   - jinja template -> layout.html + error_logs.html
11. Error Log viewer
   - ```local_ip:8082/error_log/<file_name>```
   - jinja template -> layout.html + error_log.html
13. About Fleet Manager
   - ```local_ip:8082/about```
   - jinja template -> layout.html + about.html
14. Navigation Landing
   - ```local_ip:8082/addr_input```
   - jinja template -> layout.html + addr.html + addr_input.html
   
#### Which pages don't work:
1. Preserved Footage index
2. Nav address confirmation
3. Nav driving directions

