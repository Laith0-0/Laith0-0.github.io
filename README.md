# Laith's Portfolio
## About this page
This github page is used to showcase my personal growth and progress throughout my cybersecurity journey, in which i'll be documenting my progress and steps taken to complete these projects.
# Projects:

## Network Monitoring System
#### Summary
The Network Monitoring System (NMS) project was my graduation project for my final year at the university in which I was able to excel and develop valuebale skills in both technical and interpersonal skills, in which the projects group consisted of 3 other members, in which this project was only made possible through our collabrative efforts and applying our theoretical knowledge into practical work. 
#### Description
Developed a network monitoring system with Splunk SIEM, Snort IDS/IPS, and PfSense Firewall. Enabling real-time traffic analysis and intrusion detection.
#### Tools & Technologies used

   * Vmware
     
   * GNS3
     
   * PfSense (Firewall)
     
   * Splunk (SIEM)
     
   * Snort (IPS & IDS)

#### Process
[Download the document](https://github.com/Laith0-0/Laith0-0.github.io/raw/main/NMS.pdf)
#### Conclusion
## Python keylogger
#### Description
This project includes a Python keylogger that tracks keyboard inputs and sends them to a server every 10 seconds. The Python script uses pynput to capture keystrokes and requests to send them to a server. The server is built with JavaScript using the express framework and saves the data to a file. It also provides a web page where you can view the captured keyboard data.
#### Tools & Technologies Used
1. Python: The language used for the keylogger.
   
   * pynput: To capture keyboard events.
    
   * requests: To send data to the server.
    
   * threading: To handle timed tasks.
     
2. JavaScript: The language used for the server.
   
   * express: For setting up the web server.
    
   * body-parser: To handle JSON data.
    
   * fs (File System): For saving data to a file.
    
#### Process
* Python Keylogger:
  
   * Setup: Initializes variables for storing keystrokes and defines the server’s address.
     
   * Capture Keystrokes: Uses pynput to record key presses.
     
   * Send Data: Posts the captured data to the server every 10 seconds.
     
   * Error Handling: Prints a message if sending data fails.
     
   * Stop Logging: Stops when the Esc key is pressed.
  
* Server:
  
   * Initialize: Sets up the server and configures it to read JSON data.
     
   * Handle GET Requests: Serves a web page showing the contents of keyboard_capture.txt.
     
   * Handle POST Requests: Receives data from the Python script and writes it to keyboard_capture.txt.
     
   * Error Handling: Shows a default message if no data has been logged yet.
     
#### Testing & Results

* Python Code: Run the script to ensure it captures keystrokes and sends them to the server correctly.
  
* Server: Start the server and check that it listens on port 8080. Visit http://localhost:8080 to see if the data is displayed correctly and confirm that POST requests are being handled properly.
  
#### Conclusion
This project demonstrates how to capture and display keyboard input using a Python keylogger and a server. The Python script handles capturing and sending data, while the server manages data storage and display.
#### Resources
David Bombal’s YouTube Tutorial: <https://www.youtube.com/watch?v=LBM3EzBXhdY&t=302s>
## Access Control List (Time-based, Dynamic, Reflexive & MAC-based)
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
## Arduino (Automatic Sliding Door)
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
