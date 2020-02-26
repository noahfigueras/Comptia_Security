# Dealing with Incidents 
## Incident Response 
**Incident response process**  
1. Preparation.
  * The Big plan.
  * Who's doing what? 
  * Organize the types of incidents that might happen. 
  * Practice scenarios.
2. Reporting.
  * What reports go to whom ?
  * Escalation. 
3. Identification.
  * Recognize what incident has ocurred.
  * Reports from users.
  * Check the monitoring tools you use. 
  * Watch alerts and logs.
  * Asses the impact.
  * Define who's involved.
4. Containment. 
  * Mitigate the damage.
  * Stop the attack. 
  * Segregate the network. 
  * Shutdown the system. 
  * Turn off a service. 
5. Eradication.
  * Remove the malware.
  * Close off vulnerabilities.
  * Add new controls. 
6. Recovery.
  * Restore from backups.
  * Pull from snapshots.
  * Hire replacement personnel.
  * Monitor to ensure good operations. 
7. Documentation.
  * Document the incident.
  * What failed? 
  * What worked? 
  * Generate a final report. 

**Incident Response Plan**  
1. CIRT - Cyber incident response team.  
* A group of people whose job is to respond to all incident.
* Full time or part time.
* IT security team.
* IT department.
* Human Resources.
* Legal.
* Public Relations. 
2. Document incident types/category definitions.
* Physical access.
* Malware.
* Phishing.
* Social engineering.
* Data access.
3. Roles and responsabilities.
* Users.
* Help Desk.
* Human Resources.
* Database Manager.
* Incident hotline.
* Incident Response manager / IR officer.
* IR team. 
4. Reporting requirements/escalation.
* Determine severity.
* Based on severity have a clear chain of escalation. 
* Informing law enforcement. 

**Most importantly practice is the only way we are going to be able to achieve everything on the list successfully**  

## Digital Forensics
Digital forensics is the art, the science of collecting, storing and quantifying digital evidence to be used as the result of some action that takes place.  
**Chain of Custody**  
The whole idea of chain of custody is to show good integrity of the evidence itself.  
**Chain of custody process**  
1. Define the evidence.
2. Document collection methods.
3. Date/time collected.
4. Person(s) handling the evidence.
5. Function of person handling evidence.
6. All locations of the evidence.  

**Order of Volatility**  
Our job is to get as much data of the computer as we can and the order of volatility is basically a checklist that says what to do first and what to keep doing next after that.  
1. Memory.
  * Caches.
  * Routing table.
  * ARP table.
2. Data on the disk.
  * Optical, flash drives.
  * Cache files, temp files.
  * Write blocker enabled tools.
3. Remotely logged data.
  * Web site data.
  * Remote file server logs.
4. Backups.
  * Trends.
  * Low volatility takes time to gather data.  

**Forensic Data Acquisition**  
1. Capture the system image.
2. Network traffic and logs.
3. Capture video.
  * Security cameras.
  * Record time offset.
4. Take hashes.
5. Take screenshots.
6. Interview witnesses.
7. Track man hours.  

## Contingency Planning
Sometimes, every once in a while really bad incidents take place. We're talking hurricanes or acts of war or some type of really bad thing that's going to take place that is going to massively disrupt your infrastrucutre.  

**Evacuation Plan / Backup or Recovery Site**  
1. Cold Site.
  * It takes weeks to bring online. 
  * Basic office space: buildings, chairs, AC. 
  * No operational equipment.
  * Cheapest recovery site.
2. Warm Site. 
  * It takes days to bring online.
  * Operational equipment but little or no data. 
3. Hot site.
  * It takes hours to bring online.
  * Real-time synchronization.
  * Almost all data ready to go - often just a quick update. 

**Order of Restoration** 
1. Power 
2. Wired LAN.
3. ISP link.
4. Active directory/DNS/DHCP servers
5. Accounting servers.
6. Sales and accounting workstations.
7. Video production servers.
8. Video production workstations.
9. Wireless.
10. Peripherals(Printers, cameras, scanners, faxes).

## Backups
We can do Full Backups every day in order to save all the information in your system bu it is very time consuming and it takes a lot of memory as well.  
Instead, what we can do is do a backup of the system first and then every time there's a change update it to the backup.  

**Differential Backup:** Backup of all changes since the last full backup.  
**Incremental Backup:** Only backs up changes made from last backup.  
**Snapshots:** A very good way of making a copy of something that happened in the past.  
**Local Backups:** tapes, external drives.
**Offsite Backup:** 
**Cloud Backup:** very powerful to keep your data save. 






  
  
