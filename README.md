# GSoC'24 Final Report - Arnab Ghosh
##### Organization: Internet Health Report (IHR)
##### Project: Real Time BGP Monitor
##### Project Link: https://summerofcode.withgoogle.com/programs/2024/projects/YOteUEcC
##### Student: Arnab Ghosh
##### Mentors: Romain Fontugne, Dimitrios Panteleimon Giakatos, Emile Aben

## Project Demo
Here is a demo of the tool I developed from scratch in this GSoC'24 project:

## About the Project
Network operators need to monitor the global reachability of their IP prefixes every time they update their routing policies or make BGP announcements.

This project addresses this need by providing a monitoring dashboard on the IHR website that allows network operators, policymakers, and other
stakeholders to easily track how a prefix propagates across the Internet. The tool takes a prefix from the user, along with a RIS collector and the maximum number of hops from the monitored prefix to display. Once the user presses the 'play' button, the tool connects to RIS Live with the specified parameters and visualizes the AS paths received in a Sankey diagram. The data is continuously updated with new BGP information, ensuring real-time monitoring.

## My Work
* Created a monitoring dashboard using Vue.js, JavaScript, Quasar UI, and Plotly.js.
* Integrated the RIS Live WebSocket API for primary data collection.
* Wrote optimized JavaScript logic to generate visualization data for AS paths and line charts for BGP announcements and withdrawals.
* Integrated the GitHub API to fetch additional BGP community information from a third-party repository, automatically retrieving and processing .txt files with CSV data. This includes filtering out invalid or inconsistent data and extracting valid BGP community descriptions.
* Developed four custom wildcard patterns and regular expressions to identify BGP communities from the fetched data.
* Wrote filtering logic to automatically update BGP peer messages when new data is received or when viewing past BGP messages.
* Added a feature that allows users to view past BGP messages by implementing a timestamp slider or by clicking on a specific timestamp in the line chart, which updates the Sankey diagram and messages table to reflect the data at that particular time.

## Screenshorts
![GSoC'24 SS](assets/GSoC'24%20SS.jpg)

