# Laith's Portfolio
## About this page
This github page is used to showcase my personal growth and progress throughout my cybersecurity journey, in which i'll be documenting my progress and the steps taken to complete these projects.
# Projects:

## Network Monitoring System
#### Summary
For my final year graduation project, I worked on a Network Monitoring System (NMS), which allowed me to enhance both my technical and interpersonal skills. Leading a team of three other members, I contributed significantly to the project’s success. Our collaborative efforts and application of theoretical knowledge in a practical setting were key to achieving our goals.
#### Description
The Network Monitoring System (NMS) project was a comprehensive final year graduation project that involved designing and implementing a simulated network environment using GNS3 and VMware. The simulation featured a network topology consisting of an HQ branch and a second branch, with intermediary devices including Cisco routers, multilayer switches, and switches.

We integrated various virtual appliances into our setup, including a pfSense router/firewall for managing firewall rules and Snort for intrusion detection and prevention. Snort was configured to detect intrusion attempts in real-time by comparing network activities against a predefined ruleset. When an intrusion was detected, Snort compiled the event data and sent it to a Security Information and Event Management (SIEM) system, Splunk.

Splunk played a crucial role in notifying administrators through mobile alerts that detailed the severity of the intrusion attempt. Additionally, it provided a comprehensive dashboard for reviewing and analyzing intrusion events.

As part of the project, we simulated an attack using a Kali Linux device connected to a compromised branch. This device conducted TCP and UDP scans, which were detected by both pfSense and Snort. The successful detection led to a mobile notification being sent to the administrator, demonstrating the effectiveness of our monitoring and alerting system.
#### Tools & Technologies used

   * Vmware
     
   * GNS3
     
   * PfSense (Firewall)
     
   * Splunk (SIEM)
     
   * Snort (IPS & IDS)
     
   * Site-to-site VPN
     
   * OSPFv2
     
   * PAT (Port Address Translation)

   * VLAN (Virual Local Area Network) 
     
   * Etherchannel with LACP

   * VRRP (Virtual Router Redundancy Protocol)

#### Process
Download the Project's documentation, [Here.](https://github.com/Laith0-0/Laith0-0.github.io/raw/main/NMS.pdf)
#### Conclusion
The Network Monitoring System (NMS) project effectively demonstrated our ability to design and implement a complex network environment using modern simulation tools and technologies. By integrating Cisco devices, pfSense, Snort, and Splunk, we created a robust system capable of real-time intrusion detection and response. The successful simulation of a TCP and UDP scan attack highlighted the system's effectiveness in detecting and notifying administrators of security threats. This project not only showcased our technical skills but also emphasized the importance of collaborative efforts and practical application of theoretical knowledge in addressing real-world cybersecurity challenges.
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
## Access Control List (Time-based)
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
