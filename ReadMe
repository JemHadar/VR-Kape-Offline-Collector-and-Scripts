This is an excellent presentation by Eric Capuano detailing the capabilities of Velociraptor in a full fledged live environment. I was just blown away how we can have the client give us access to the compromised environment, launch our VR server, have clients push out VR client agent to all endpoints and begin our DFIR investigation from the VR server.

https://www.youtube.com/watch?v=Q1IoGX--814

His demo has 55 systems and how fast IR can be done. Velocirator is definitely scalable for enterprise environments. 

He shows how we can look for persistence, scan memory using Yara, running process hash check vith V/T, all binaries hash check with V/T. Once compromised systems have been found via various artifacts we can quarantine all via the VR server. VR will apply fw rules to block all nework communication on all the tagged systems except back to VR server.

Before obliterating the infected systems, we can pull triage acquisitions from all the infected systems using Kape to collect files from an endpoint


Black Hills presentation by Patterson Cake shows how we can leverage VR and use Kape for an offline collector. 

https://www.youtube.com/watch?v=rqEjxZph96c


Using Patterson's techinique, I decided to test it and the results were fast and quick. We can leverage an expander script that unpacks all Kape artifacts and mounts the VHD files and then run a second script to parse through all the mounted volumes and extract the artifacts courtesy of Swisscom (https://github.com/swisscom/Invoke-Forensics).

Finally, we can use Hayabusa's Windows event log fast forensics timeline generator to create a forensic timeline from the event logs. Hayabusa uses Sigma as well as built-in rules to assess Windows Event Logs for known threats. Hayabusa can be run either on single running systems for live analysis, by gathering logs from single or multiple systems for offline analysis, or by running the Hayabusa artifact with Velociraptor for enterprise-wide threat hunting and incident response. 


Below is a video of Velociraptor with Kape Offline Collector and the scripts in action as well as the event log timeline.

[![Video Walkthrough](https://img.youtube.com/vi/0nzyJ7mJHAI/0.jpg)](https://www.youtube.com/watch?v=0nzyJ7mJHAI/ "Walkthrough") 

Hayabusa was run on a sample of EVTX logs that displayed malicious activity.
https://github.com/sbousseaden/EVTX-ATTACK-SAMPLES


Command that was run:

./hayabusa-2.11.0-mac-arm csv-timeline -d ~/Downloads/tools/evtx_files/ -o results.csv -p super-verbose


I have placed Kape and modules as well as expander script for extractng and/or mounting multiple VHD files and Swisscom's Invoke-Forensics script for processing in one zip file for download:

https://drive.google.com/file/d/1G7MQqgLuaYXiASisIHNA5ZV5LV7a-XZG/view?usp=sharing




