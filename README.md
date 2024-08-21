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
The Python code implements a keylogger that captures keyboard input and sends it to a server at regular intervals. It uses the pynput library to monitor keyboard events and requests to send HTTP POST requests containing the captured text. The JavaScript code sets up a server using the express framework, which listens for HTTP POST requests and logs the keyboard data to a file. It also serves a simple HTML page to display the logged data.
#### Tools & Technologies Used
Python: A high-level programming language used for the keylogger script.

pynput: A library for capturing keyboard events.
requests: A library for making HTTP requests.
threading: A Python module for running tasks concurrently.
JavaScript: A programming language used for the server-side script.

express: A web framework for Node.js to create the HTTP server.
body-parser: Middleware for parsing JSON bodies of incoming requests.
fs (File System): Node.js module for file operations.
Process
Python Keylogger:

Initialization: Sets up a text variable to store captured keystrokes and defines the server’s IP address and port number.
Key Capture: Uses pynput's keyboard.Listener to capture key presses and update the text variable accordingly.
Data Posting: Sends the captured text to the server via a POST request every 10 seconds using the requests library.
Exception Handling: Prints an error message if the POST request fails.
Termination: Stops capturing when the Esc key is pressed.
JavaScript Server:

Setup: Initializes an Express application and configures it to parse JSON request bodies.
HTTP GET: Serves an HTML page that displays the contents of keyboard_capture.txt if it exists.
HTTP POST: Receives keyboard data from the Python script and writes it to keyboard_capture.txt.
Error Handling: Responds with a default message if no data is logged yet.
#### Testing & Results
##### Testing:

Python Code: Run the Python script to ensure it starts capturing keystrokes and sending data to the server. Verify that the data is correctly sent every 10 seconds.
JavaScript Server: Start the server and make sure it listens on port 8080. Test the GET request by navigating to http://localhost:8080 to ensure it displays the logged data. Test the POST request by running the Python script to check if the data is properly received and saved.
##### Results:

The Python script successfully captures keystrokes and posts them to the server.
The JavaScript server correctly logs the data to a file and serves it via HTTP GET requests.
The HTML page displays the logged keyboard data as expected.
#### Conclusion
The integration of the Python keylogger and JavaScript server demonstrates a basic setup for capturing and displaying keyboard input. The Python script handles the keylogging and data transmission, while the JavaScript server manages data storage and presentation. This setup provides a clear example of how to capture user input and communicate between a client-side application and a server. However, this implementation should be used with caution and only in environments where you have explicit permission, as keylogging can be sensitive and potentially harmful if misused.
#### Resources
[David Bombal] (https://www.youtube.com/watch?v=LBM3EzBXhdY&t=302s)
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
