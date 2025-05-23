# IDS-HTTP-Log-Analysis-and-Visualization-of-Common-Host-Traffic
o analyze a pre-processed HTTP traffic log file generated by an Intrusion Detection System (IDS) to identify the most frequently accessed external hosts and visualize their activity patterns over time.

Context:
IDS logs contain critical information about network traffic, which can be valuable for security monitoring, understanding network usage, and identifying potential anomalies or security incidents. This project focuses on extracting, analyzing, and visualizing specific aspects of the HTTP traffic recorded in such a log – specifically, the destinations (hosts) that are most frequently accessed from the monitored network. This type of analysis helps in understanding typical network behavior and highlighting prominent external communication points.

Data Source:
The project will utilize the provided log file part2.log. This file contains pre-processed records of HTTP requests, including timestamp, unique transaction ID, originating IP and port, destination IP and port, transaction depth, HTTP method, the requested host domain, and the requested URI path.

Methodology and Tasks:

Efficient Log Reading: Implement a method to read the part2.log file line by line to manage memory usage effectively, especially for potentially large log files.
Data Parsing: Parse each line of the log file to extract the ten specified fields: ts, uid, id.orig_h, id.orig_p, id.resp_h, id.resp_p, trans_dep, th, method, host, and uri.
Timestamp Conversion: Convert the timestamp string from each log entry into a structured datetime object to enable chronological analysis and plotting.
Host Frequency Analysis: Analyze the extracted host field across all log entries to determine the frequency of occurrence for each unique host domain requested.
Identification of Top Hosts: Identify the top three most commonly seen host domains based on the frequency analysis.
Host Description: Provide a brief, descriptive explanation (1-2 sentences) for each of the top three identified hosts, commenting on their likely nature (e.g., major website, service provider, known tracker, etc.).
Temporal Visualization: Create a plot that visualizes the distribution and frequency of requests for the top three most common hosts over the entire time period covered by the log file.
Deliverables:

A script or notebook containing the code to perform the log reading, parsing, analysis, and visualization steps.
The output displaying the names of the top three most common hosts.
Brief descriptions of the top three hosts.
A plot illustrating the timeline of requests directed towards the top three hosts.
Tools/Technologies:
Python programming language is suitable for this task, leveraging libraries such as:

Standard file I/O for reading the log.
String manipulation methods for parsing each line.
datetime module for timestamp conversion.
collections.Counter or similar methods for frequency counting.
pandas (optional but highly recommended for data handling and time-series plotting).
matplotlib or seaborn for creating the visualization.
