how to run source code 1
On a Local Computer
Verify Python Installation

Ensure Python 3.x is installed on your system:
bash
Copy code
python3 --version
Save the Code

Rename and save the uploaded file as simple_car.py or use the current file name Sorce Code-1.py.py.
Run the Code

Open a terminal or command prompt.
Navigate to the directory containing the file:
bash
Copy code
cd /path/to/file
Execute the script:
bash
Copy code
python3 Sorce\ Code-1.py.py
On an ARM Cortex IoT Device
Set Up the Device

Install Python 3 if it is not already installed:
bash
Copy code
sudo apt-get update
sudo apt-get install python3
Transfer the File

Transfer the file to the device using scp, USB, or SFTP:
bash
Copy code
scp Sorce\ Code-1.py.py user@iot-device-ip:/home/user/
Run the File

SSH into the IoT device or use a local terminal.
Navigate to the directory where the file was copied:
bash
Copy code
cd /home/user/
Run the script:
bash
Copy code
python3 Sorce\ Code-1.py.py
Expected Output
Upon running the script, the car's movements will be simulated, and the following results will print to the terminal:

css
Copy code
Moved forward to (0, 1)
Turned right. Now facing East
Moved forward to (1, 1)
Turned left. Now facing North
Moved forward to (1, 2)

how to run source code 2:
1. Prepare the IoT Device
Ensure the IoT device has an ARM Cortex processor (e.g., Raspberry Pi, BeagleBone, or other similar boards).
Install an operating system on the device that supports Python, such as Raspbian (for Raspberry Pi) or an equivalent Linux-based OS.
2. Install Python and Required Libraries
Install Python if not pre-installed:
bash
Copy code
sudo apt-get install python3
Install the required libraries from the code:
bash
Copy code
pip3 install opencv-python mediapipe pyautogui pynput numpy
3. Transfer the Code
Copy the script (Source Code-2.py) to the IoT device using SCP, SFTP, or a USB drive:
bash
Copy code
scp Source\ Code-2.py user@iot-device-ip:/home/user/
4. Connect Necessary Peripherals
Attach a USB camera if the IoT device doesn't have a built-in one.
Connect any display device if needed for testing.
5. Run the Code
Open a terminal on the IoT device.
Navigate to the directory where the script is stored:
bash
Copy code
cd /path/to/script
Run the script:
bash
Copy code
python3 Source\ Code-2.py
6. Testing
The script uses a webcam to track hand gestures and perform actions such as mouse movement, clicks, and screenshots.
Test the gestures to ensure functionality.
7. Optimize for IoT
If running on a constrained IoT device:
Optimize the code for performance (e.g., reduce video resolution to lower CPU usage).
Minimize the number of libraries or modules loaded.
If the device lacks GPU support, consider lightening the Mediapipe models.
Debugging Tips
If you encounter issues:
Ensure the camera is detected (ls /dev/video*).
Check for missing libraries or Python errors.
Adjust the device’s hardware capabilities (e.g., swap space) for better performance
