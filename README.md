# Laith's Portfolio
## About this page
This github page is used to showcase my personal growth and progress throughout my cybersecurity journey, in which i'll be documenting my progress and steps taken to complete these projects.
# Projects
## Network Monitoring System
#### Description
Developed a network monitoring system with Splunk SIEM, Snort IDS/IPS, and PfSense Firewall. Enabling real-time traffic analysis and intrusion detection.
#### Tools & Technologies used
#### Process
#### Testing & results
#### Conclusion
#### Resources
## Python keylogger
#### Description
This project includes a Python keylogger that tracks keyboard inputs and sends them to a server every 10 seconds. The Python script uses pynput to capture keystrokes and requests to send them to a server. The server is built with JavaScript using the express framework and saves the data to a file. It also provides a web page where you can view the captured keyboard data.
#### Tools & Technologies Used
Python: The language used for the keylogger.
pynput: To capture keyboard events.
requests: To send data to the server.
threading: To handle timed tasks.
JavaScript: The language used for the server.
express: For setting up the web server.
body-parser: To handle JSON data.
fs (File System): For saving data to a file.
Process
Python Keylogger:
Setup: Initializes variables for storing keystrokes and defines the server’s address.
Capture Keystrokes: Uses pynput to record key presses.
Send Data: Posts the captured data to the server every 10 seconds.
Error Handling: Prints a message if sending data fails.
Stop Logging: Stops when the Esc key is pressed.
JavaScript Server:
Initialize: Sets up the server and configures it to read JSON data.
Handle GET Requests: Serves a web page showing the contents of keyboard_capture.txt.
Handle POST Requests: Receives data from the Python script and writes it to keyboard_capture.txt.
Error Handling: Shows a default message if no data has been logged yet.
#### Testing & Results
##### Testing:
Python Code: Run the script to ensure it captures keystrokes and sends them to the server correctly.
JavaScript Server: Start the server and check that it listens on port 8080. Visit http://localhost:8080 to see if the data is displayed correctly and confirm that POST requests are being handled properly.
##### Results:
The Python script successfully sends keystrokes to the server.
The JavaScript server correctly logs the data and displays it on the web page.
#### Conclusion
This project demonstrates how to capture and display keyboard input using a Python keylogger and a JavaScript server. The Python script handles capturing and sending data, while the JavaScript server manages data storage and display. Use this setup responsibly, as keylogging involves sensitive data.
#### Resources
David Bombal’s YouTube Tutorial: https://www.youtube.com/watch?v=LBM3EzBXhdY&t=302s
## Access Control List (Time-based, Dynamic, Reflexive & MAC-based)
#### Description
#### Tools & Technologies used
#### Process
#### Testing & results
#### Conclusion
#### Resources
## Web application deployment with Microsoft Azure
#### Description
#### Tools & Technologies used
#### Process
#### Testing & results
#### Conclusion
#### Resources
## Windows Active Directory in a Home lab environment
#### Description
#### Tools & Technologies used
#### Process
#### Testing & results
#### Conclusion
#### Resources
## Digital Forensics
#### Description
#### Tools & Technologies used
#### Process
#### Testing & results
#### Conclusion
#### Resources
## Kali linux powerful tools
Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh.
## Capture the flag (CTF)
Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh.
