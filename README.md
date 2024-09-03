# Laith's Portfolio
## About this page
This github page is used to showcase my personal growth and progress throughout my cybersecurity journey, in which i'll be documenting my progress and the steps taken to complete these projects.

---

# Projects:

## Network Monitoring System
#### Summary
For my final year graduation project, I worked on a Network Monitoring System (NMS), which allowed me to enhance both my technical and interpersonal skills. Leading a team of three other members, I contributed significantly to the project’s success. Our collaborative efforts and application of theoretical knowledge in a practical setting were key to achieving our goals.
#### Description (Overview)
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

#### Documentation
Download the Project's documentation: [Here.](https://github.com/Laith0-0/Laith0-0.github.io/raw/main/NMS.pdf)
#### Conclusion
The Network Monitoring System (NMS) project effectively demonstrated our ability to design and implement a complex network environment using modern simulation tools and technologies. By integrating Cisco devices, pfSense, Snort, and Splunk, we created a robust system capable of real-time intrusion detection and response. The successful simulation of a TCP and UDP scan attack highlighted the system's effectiveness in detecting and notifying administrators of security threats. This project not only showcased our technical skills but also emphasized the importance of collaborative efforts and practical application of theoretical knowledge in addressing real-world cybersecurity challenges.

---

## Windows Active Directory in a Home lab environment
#### Description

In this project, I set up Windows Active Directory in a home lab using Windows Server 2019 and Windows 10, both running on VirtualBox. The main goal was to create an Active Directory (AD) domain, implement Group Policies, and see how these policies affected client machines within the domain. I specifically focused on configuring a policy to disable the Recycle Bin and making sure it was properly applied to users in the domain.

#### Tools & Technologies used

  * Windows Server 2019: Used as the Domain Controller.
    
  * Windows 10: Used as the client machine.
    
  * VirtualBox: Virtualization software for creating and managing virtual machines.
    
  * Static IP Addresses: Assigned to both the domain controller and client machine to ensure stable network communication.
    
#### Process

1. Prepare the Environment:

     * I started by installing VirtualBox and setting up two virtual machines: one for Windows Server 2019 and one for Windows 10.

     * allocated 2 CPUs, 4 GB of RAM, and 40 GB of HDD space for each VM.
       
     * Configured the virtual network to ensure the VMs could communicate with each other.
       
2. Install Windows Server 2019:
   
      * Installed Windows Server 2019 on the VM designated as the Domain Controller.
        
      * Assigned a static IP address (e.g., 192.168.1.10) and configured the network settings.

3. Configure the Domain Controller:

      * Renamed the server to DC01 and updated Windows Server 2019 to the latest patches.
        
      * Opened Server Manager, added the "Active Directory Domain Services" role, and promoted the server to a Domain Controller.
        
      * Created a new forest with the domain name home.lab during the promotion process.
        
      * Set the Directory Services Restore Mode (DSRM) password and completed the setup.

4. Set Up Windows 10 Client:

    * Installed Windows 10 on the second VM.
      
    * Assigned a static IP address (e.g., 192.168.1.20) and joined it to the home.lab domain.
      
    * Logged in with domain credentials to verify that the domain join was successful.

5. Implement Group Policies:

    * Opened the Group Policy Management Console (GPMC) on the Domain Controller.
      
    * Created a new Group Policy Object (GPO) called "Disable Recycle Bin."
      
    * Edited the GPO to navigate to User Configuration > Administrative Templates > Windows Components > File Explorer, and enabled the policy to disable the Recycle Bin.
      
    * Linked the GPO to the default domain policy.
      
6. Apply and Test Policies:

    * On the Windows 10 client, I ran the command gpupdate /force to apply the new Group Policy settings immediately.
      
    * Checked the client machine to confirm that the Recycle Bin icon was no longer visible on the desktop.
      
#### Testing & results

1. Domain Join Verification:

    * The Windows 10 machine joined the home.lab domain without any issues.
      
    * Domain user accounts were able to log in and access resources as expected.
      
2. Group Policy Application:

    * The "Disable Recycle Bin" policy was successfully applied. After running gpupdate /force, the Recycle Bin icon disappeared from the Windows 10 desktop.
      
    * Verified the policy application using the rsop.msc command and confirmed it was listed correctly under User Configuration > Administrative Templates > Windows Components > File Explorer.
      
#### Conclusion

Setting up Active Directory with Windows Server 2019 and Windows 10 on VirtualBox was a great hands-on experience with directory services and Group Policy management. By configuring a policy to disable the Recycle Bin and applying it to domain users, I effectively managed and enforced policies across a networked environment. This project provided a solid foundation for further exploring Active Directory features and administration.

---

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

#### Github Link

Python keylogger: [Here.](https://github.com/Laith0-0/Python-Remote-Keylogger)

Keylogger Server: [Here.](https://github.com/Laith0-0/Keylogger-Server)
  
#### Conclusion
This project demonstrates how to capture and display keyboard input using a Python keylogger and a server. The Python script handles capturing and sending data, while the server manages data storage and display.
#### Resources
David Bombal’s YouTube Tutorial: <https://www.youtube.com/watch?v=LBM3EzBXhdY&t=302s>

---

## Access Control List (Time-based)
#### Summary
For my Access Control List Project, I developed a Time-Based Access Control List (ACL) system designed to enhance network security and manage access dynamically based on specific time periods. The core objective was to implement an advanced ACL mechanism that extends traditional packet filtering capabilities by incorporating time-based conditions.
#### Description (Overview)
An ACL, or Access Control List, is fundamental in network security for controlling traffic flow by defining rules to permit or deny packets. My project took this concept further by creating a Time-Based ACL, which allows network administrators to apply access rules based on specified time periods. This added layer of control enables more granular management of network access, aligning security measures with operational needs.

#### Key Features and Functionality
* Time-Based ACL Types:

  * Periodic ACL: I implemented a system where access restrictions are enforced based on a recurring schedule. For example, employees' internet access can be denied during business hours (e.g., Monday to       Friday, 9 am to 5 pm) and automatically allowed outside these hours and on weekends. This ensures that network resources are used appropriately according to organizational policies.
    
  * Absolute ACL: This feature allows for precise control over network access during specific time windows. For instance, internet access can be permitted during lunch breaks (e.g., 12 pm to 1 pm) and          automatically restricted outside this period. The absolute ACL provides flexibility for one-time or ad-hoc scenarios.
    
#### Practical Scenarios
Periodic Use Case: In a corporate environment, the Time-Based ACL system could be used to automatically restrict internet access during business hours while allowing it during off-hours and weekends. This setup helps maintain productivity and security by ensuring that access policies are enforced according to the company's operational schedule.

Absolute Use Case: For scenarios like scheduled maintenance or special events, the system allows for precise control by permitting access only during the specified time frame. For example, granting internet access during a planned lunch break and then automatically revoking it after the break ends.

#### Challenges and Solutions
Local Clock Limitations: Initially, relying on the local clock posed challenges, including the potential for users to manipulate device time settings to bypass restrictions. To address this, I utilized NTP to provide a unified and accurate time source across all network devices. This approach ensures that ACL rules are enforced consistently, even if a device's local clock is altered or the router is restarted.
#### Documentation
Download the project's documentation: [Here.](https://github.com/Laith0-0/Laith0-0.github.io/raw/main/Time-based-ACL.pdf)
#### Conclusion
The Time-Based ACL project successfully demonstrates the application of advanced network security principles through dynamic time-based access control. By incorporating periodic and absolute time-based rules, along with integrating NTP for accurate time synchronization, the project enhances network management and security. This approach not only improves operational efficiency but also provides a more flexible and reliable solution for managing network access.

---

## Arduino (Automatic Sliding Door)
#### Description (Overview)
This Arduino project simulates an automatic sliding door system using a PIR (Passive Infrared) motion sensor, a micro servo, and a piezo buzzer. The system automatically opens the door when motion is detected and closes it after a period of inactivity. The piezo buzzer adds a realistic touch by playing different sounds when the door opens and closes.
#### components used

  * Arduino Uno: The central microcontroller to handle the logic and control the components.
    
  * PIR Motion Sensor: Detects motion in the vicinity.
    
  * Micro Servo Motor: Simulates the sliding door's movement.
    
  * Piezo Buzzer: Produces sound effects for opening and closing actions.
    
  * Breadboard and Jumper Wires: For connecting the components.

#### Circuit Diagram

  * PIR Sensor: Connect the VCC pin to 5V on the Arduino, GND pin to GND, and the OUT pin to a digital input pin (pin 7).
    
  * Piezo Buzzer: Connect one pin to a digital output pin (pin 8) and the other pin to GND.
    
  * Micro Servo: Connect the power pin to the 5V on the Arduino, ground pin (black or brown) to GND, and the signal pin to a PWM-enabled digital pin (pin 9).

#### Source Code
Code used for the arduino project [Here.](https://github.com/Laith0-0/Laith0-0.github.io/raw/main/Arduino-sliding-door.pdf)
#### Code explaination

  * Initialization: Set up pins for the PIR sensor, servo, and piezo buzzer.
    
  * Motion Detection: Continuously check the PIR sensor’s output. If motion is detected, initiate the door opening sequence.
    
  * Servo Control: Move the servo to the horizontal position (90 degrees) to simulate the door opening and to the vertical position (0 degrees) to simulate      the door closing.
    
  * Sound Effects: Play different sounds using the piezo buzzer when the door opens and closes.
    
#### How it works

  * Motion Detection: When the PIR sensor detects motion, the Arduino triggers the servo to move to the horizontal position, simulating the door opening,        and plays a distinct sound via the piezo buzzer.
    
  * Door Movement: The servo motor’s position changes from vertical (closed) to horizontal (open) to visually simulate the sliding action.
    
  * Sound Effects: The piezo buzzer emits a tone when the door opens and another tone when it closes, enhancing the realism of the simulation.
    
#### Link to project
To view project on Tinkercad: [Here.](https://www.tinkercad.com/things/kansXmJt5NQ-automatic-door-with-sound?sharecode=MAR2DK-Sxukust6AfAhQ0AVWgpkg0U1nfTXoc7esreY)
#### Conclusion
This project provides a functional and interactive demonstration of automated systems, combining motion detection, mechanical actuation, and sound effects for a realistic sliding door simulation.

---

# Digital Forensics Projects

## Hashing

#### Description
This project focused on verifying the integrity of digital files by calculating and comparing their hash values. Hashing ensures that files have not been altered or tampered with, which is crucial for maintaining the integrity of digital evidence in forensic investigations.

#### Tools & Technologies Used
- **Hash Calculation Software**: HashCalc for generating hash values.
- **File Hash Database**: To compare and validate hash values against known good values.

#### Process
1. **Generate Hash Values**: Utilized hashing algorithm MD5 to compute the hash values for each file. This provides a unique fingerprint for the files.
2. **Compare Hashes**: Compared the generated hash values with previously known good values to ensure that the files have not been altered.
3. **Document Results**: Recorded the hash values and compared them with expected results. Noted any discrepancies if the values did not match.

#### Testing & Results
- **Integrity Check**: All calculated hash values matched their corresponding known good values, confirming that the files were intact and unaltered.
- **Outcome**: Verified that no changes had been made to the files, ensuring their integrity.

#### Conclusion
Hashing is a fundamental method for verifying file integrity. This project demonstrated the effectiveness of hashing algorithms in ensuring that digital evidence remains unchanged throughout an investigation.

## File Signature Analysis

#### Description
This project involved analyzing file signatures to verify file authenticity and detect any anomalies or tampering. File signatures, found in the header and footer of files, help to identify file types and validate their integrity.

#### Tools & Technologies Used
- **WinHex**: A hex editor used to inspect file signatures.
- **File Signature Database**: For cross-referencing file signatures with known values.

#### Process
1. **Open Files in WinHex**: Loaded each file into WinHex to view its raw hex data.
2. **Inspect File Signatures**: Analyzed the header and footer sections of each file to identify its signature.
3. **Compare Signatures**: Compared the identified signatures with known signatures to verify file authenticity and detect any discrepancies.

#### Testing & Results
- **Signature Verification**: Successfully matched file signatures with their expected values, confirming the authenticity of the files.
- **Outcome**: Ensured that the files were genuine and had not been tampered with.

#### Conclusion
File signature analysis is essential for verifying the authenticity and type of files. This project successfully demonstrated how to use signature analysis to ensure file integrity.

## Software Write Blocking

#### Description
The aim of this project was to prevent any modifications to digital evidence by disabling write access to USB devices through Windows Registry settings. This is crucial for preserving the integrity of evidence during forensic investigations.

#### Tools & Technologies Used
- **Windows Registry Editor**: For configuring write-blocking settings.
- **USB Write Blocker Settings**: Registry keys that control write access to USB devices.

#### Process
1. **Access Windows Registry**: Opened the Registry Editor (`regedit`) on the Windows system.
2. **Modify Registry Keys**: Edited specific registry keys to disable write access to USB devices. This prevents any data from being written to USB drives connected to the system.
3. **Verify Write Blocking**: Tested the configuration by connecting a USB device and verifying that no data could be written.

#### Testing & Results
- **Write Blocking Verification**: Successfully prevented modifications to data on USB devices, ensuring that no changes could be made.
- **Outcome**: Maintained the integrity of digital evidence by effectively blocking write operations.

#### Conclusion
Using Windows Registry settings to disable write access is an effective method for protecting digital evidence from being altered. This project demonstrated how to implement and verify write-blocking measures.

## Creating Forensic Images

#### Description
This project involved creating exact copies of digital evidence using FTK Imager, which is essential for preserving the integrity of the data. Forensic imaging creates a bit-by-bit copy of the data, ensuring that the original evidence remains unaltered.

#### Tools & Technologies Used
- **FTK Imager**: Software used for creating forensic images.
- **E01 Format**: A widely used format for forensic imaging.

#### Process
1. **Launch FTK Imager**: Started FTK Imager and selected the option to create a forensic image.
2. **Select Source**: Chose the files or drives to be imaged.
3. **Create Image**: Configured imaging options and created an E01 forensic image. This image is an exact replica of the original data.
4. **Verify Image**: Checked the integrity of the created image by comparing hash values to ensure it was an exact copy of the original data.

#### Testing & Results
- **Image Verification**: Successfully created and verified forensic images with no discrepancies between the original data and the image.
- **Outcome**: Produced reliable forensic images for further analysis.

#### Conclusion
Creating forensic images with FTK Imager is critical for preserving digital evidence. This project demonstrated successful imaging and verification of data integrity.

## File Carving (Manually)

#### Description
This project focused on manually searching for and recovering hidden or deleted files within forensic images using FTK Imager. File carving can help recover data that is not immediately visible or accessible.

#### Tools & Technologies Used
- **FTK Imager**: For manual file carving and data extraction.
- **File Carving Techniques**: Methods used to locate hidden files within a forensic image.

#### Process
1. **Open FTK Imager**: Loaded the forensic image into FTK Imager.
2. **Manually Search for Hidden Files**: Performed a detailed manual search for hidden or deleted files by examining file structures and data blocks.
3. **Extract Files**: Successfully recovered a hidden image and a PDF document by identifying data patterns and file signatures.

#### Testing & Results
- **Hidden File Discovery**: Successfully located and extracted hidden files, including an image and a PDF document.
- **Outcome**: Demonstrated the ability to manually recover hidden data from forensic images.

#### Conclusion
Manual file carving is an effective technique for recovering hidden or deleted files. This project showcased the process and success of manually locating and extracting concealed data.

## File Carving (Automatically)

#### Description
In this project, I used Carver Recovery for automatic file carving, which simplifies the process of recovering hidden or deleted files from forensic images. Automatic carving tools can quickly identify and recover files without manual intervention.

#### Tools & Technologies Used
- **Carver Recovery**: Tool for automatic file carving and recovery.
- **Carver Audit Reports**: Provides detailed reports on recovered files.

#### Process
1. **Run Carver Recovery**: Loaded the forensic image into Carver Recovery.
2. **Automatic File Carving**: Utilized the tool’s automatic file carving features to search for and recover hidden or deleted files.
3. **Generate Audit Report**: Produced an audit report detailing the recovered files and their attributes.

#### Testing & Results
- **File Carving and Reporting**: Successfully recovered hidden files and generated a comprehensive audit report.
- **Outcome**: Provided detailed information on the recovered files, demonstrating the efficiency of automatic file carving.

#### Conclusion
Automatic file carving with tools like Carver Recovery streamlines the process of recovering hidden files. This project effectively showcased the tool’s capability to recover data and produce detailed reports.

## File System Identification

#### Description
This project involved identifying and analyzing the file system used in a forensic image using SleuthKit. Understanding the file system is essential for interpreting file structures and conducting thorough forensic analysis.

#### Tools & Technologies Used
- **SleuthKit**: For file system identification and analysis.
- **File System Analysis**: Techniques for understanding file system structures and contents.

#### Process
1. **Open Forensic Image in SleuthKit**: Loaded the forensic image into SleuthKit.
2. **Identify File System**: Analyzed the file system’s structure to determine its type (e.g., NTFS, FAT32).
3. **Investigate File System**: Conducted a detailed analysis of the file system to understand its layout and contents.

#### Testing & Results
- **File System Identification**: Successfully identified the file system type and structure.
- **Outcome**: Gained valuable insights into the file system used, facilitating further analysis.

#### Conclusion
File system identification with SleuthKit is crucial for forensic investigations. This project demonstrated successful identification and analysis of file systems within forensic images.

## File Analysis

#### Description
This project involved analyzing file metadata to gather information about files and their origin. Metadata analysis can reveal details such as file creation, modification dates, and location information.

#### Tools & Technologies Used
- **Exif Reader**: Tool for analyzing image metadata.
- **Google Maps**: For cross-referencing geographical location data.

#### Process
1. **Analyze Image Metadata with Exif Reader**: Loaded the image into Exif Reader to extract metadata, including GPS coordinates.
2. **Determine Location**: Used the extracted GPS data to find the geographical location on Google Maps.
3. **Verify Information**: Cross-referenced the location data to ensure accuracy.

#### Testing & Results
- **Location Determination**: Successfully identified the geographical location where the image was taken.
- **Outcome**: Provided additional context for the image, useful for understanding its origin.

#### Conclusion
Exif Reader and Google Maps are effective tools for analyzing image metadata and determining location. This project demonstrated how to use these tools to gain valuable contextual information.

## Artifacts in the Registry

#### Description
This project involved using Regripper to analyze Windows registry artifacts to uncover hidden user activities and system events. Registry artifacts can provide detailed information about user actions and system changes.

#### Tools & Technologies Used
- **Regripper**: Tool for extracting and analyzing Windows registry data.
- **Windows 10 Virtual Machine**: Platform used for analyzing registry artifacts.

#### Process
1. **Run Regripper**: Loaded the Windows registry hive into Regripper.
2. **Extract Artifacts**: Used Regripper to extract and analyze registry data related to user activities and system events.
3. **Review Findings**: Examined the output for evidence of hidden or deleted activities.

#### Testing & Results
- **Artifact Extraction**: Successfully extracted and analyzed registry artifacts to reveal hidden user activities.
- **Outcome**: Provided insights into user behavior and system changes, aiding forensic investigations.

#### Conclusion
Regripper is a powerful tool for analyzing Windows registry artifacts. This project demonstrated its effectiveness in uncovering hidden user activities and system events.

## Resource
Digital Forensics Workbook Data Sets: [Here.](https://www.digitalforensicsworkbook.com/data-sets)

---

# Certificates
## Google Cybersecurity Certificate: Foundations of cybersecurity
Googles certificate: [Here.](https://github.com/Laith0-0/Laith0-0.github.io/raw/main/Google-Foundations-of-cybersecurity-cert.pdf)
## Cisco Networking Academy: Network Security
Cisco's certificate: [Here.](https://github.com/Laith0-0/Laith0-0.github.io/raw/main/Network-Security-certificate.pdf)
## Capture the flag (CTF)
CTF certificate: [Here.](https://github.com/Laith0-0/Laith0-0.github.io/raw/main/CTF-certificate.pdf)
