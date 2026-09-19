# NETWORKWALKS-RUTUJA-B083-WK2-PM4-PM5-FOOTPRINTING-WITH-HARVESTER-NETWORK-SCANNING-WITH-ZENMAP
NetworkWalks Week 2 cybersecurity lab covering footprinting with theHarvester and authorized network scanning with Zenmap.





Field	Details

Pentester Name	Rutuja Medhekar
Batch	B083
Program	NetworkWalks Cybersecurity Internship
Week	Week 2
Modules	W2-PM4 & W2-PM5
Project	Footprinting & Network Scanning
Tools	theHarvester & Zenmap
Operating Systems	Kali Linux & Windows
Skills	Reconnaissance & Network Mapping
Purpose	Educational Cybersecurity Lab
Environment	Authorized Lab / Own Network
GitHub	Rutuja Medhekar




⚠️ Liability Disclaimer

This project is created strictly for educational and cybersecurity learning purposes as part of the NetworkWalks Cybersecurity Internship.

All reconnaissance, footprinting, and network-scanning activities documented in this repository are performed only on authorized systems, networks, or lab environments where permission has been granted.

The tools and techniques demonstrated, including theHarvester and Zenmap, should not be used against systems or networks without proper authorization.

The author is not responsible for any misuse, unauthorized access, damage, or legal consequences resulting from the information presented in this project.

Always obtain proper permission before conducting cybersecurity testing or network scanning.



 📌 2. Introduction & Overview

This repository documents practical cybersecurity lab work completed as part of the NetworkWalks Cybersecurity Internship program. The project focuses on two core phases of cybersecurity reconnaissance and network discovery:

1. **Footprinting & Reconnaissance with theHarvester:** Gathering publicly available intelligence, including emails, subdomains, and host information from authorized target domains using theHarvester on Kali Linux.

2. **Network Scanning with Zenmap:** Performing local network configuration checks using Windows `ipconfig`, discovering active hosts through authorized network scanning, and visualizing the network topology using Zenmap.

The project provides hands-on experience with reconnaissance, OSINT collection, network discovery, and topology mapping while emphasizing proper authorization and responsible cybersecurity practices.





 🛠️ 3. Tools & Technologies Used

| Tool / Technology | Purpose / Function |
|---|---|
| Kali Linux | Operating system environment utilized for running theHarvester command-line operations. |
| Windows OS | Local platform hosting Zenmap, command prompt (`cmd`), and local interface settings. |
| theHarvester | Open Source Intelligence (OSINT) reconnaissance tool used to gather emails, subdomains, and host data from public sources. |
| Zenmap (Nmap GUI) | Graphical user interface for Nmap used to execute ping sweeps, discover hosts, and map network topologies. |





⚙️ 4. Methodology & Execution

### Phase 1: Footprinting & Reconnaissance with theHARVESTER

* **Help & Usage Verification:** Inspected tool parameters and guidelines using command-line options (`theHarvester -h`) to understand syntax flags like domain selection (`-d`), result limits (`-l`), and data sources (`-b`).

* **Task 1 (Baidu Source Query):** Executed targeted search against `microsoft.com` using the Baidu module with a result limit of 1000 and saving the text file as evidence using `cat task1.txt`:

  * **Execution Command:**

        theHarvester -d microsoft.com -l 1000 -b baidu

  * **Output Evidence:**

        cat task1.txt

  * **Analysis & Objective:**
    * **What we are trying to prove:** Assesses how much organization-specific infrastructure is publicly discoverable via an eastern search engine module (`baidu`) without interacting directly with the target network.
    * **What is shown:** The output displays raw OSINT data harvested from Baidu, including discovered subdomains and associated IP addresses tied to `microsoft.com`.

* **Task 2 (Multi-Source Enumeration):** Executed broader searches against `microsoft.com` using all available sources (`all`) with a result limit of 50 and saving the text file as evidence using `cat task2.txt`:

  * **Execution Command:**

        theHarvester -d microsoft.com -l 50 -b all

  * **Output Evidence:**

        cat task2.txt

  * **Analysis & Objective:**
    * **What we are trying to prove:** Demonstrates the capabilities and limitations of automated multi-source enumeration (`all`), showing how the tool attempts to aggregate intelligence across a wide spectrum of public and proprietary OSINT feeds simultaneously.
    * **What is shown:** The output displays harvested asset data alongside warning messages for services that require API credentials. This demonstrates the limitations of restricted or registration-bound OSINT sources when API credentials are not configured.

### Phase 2: Network Scanning with Zenmap

* Opened Windows Command Prompt and executed `ipconfig` to determine the local interface configuration, including the active IPv4 address, subnet mask, and default gateway.

* Entered the **actual authorized local subnet range obtained from `ipconfig`** into Zenmap, selected the **Ping scan** profile, and executed the corresponding Nmap command.

* **Zenmap Host Discovery Results:**
  * Executed the ping sweep against the authorized local subnet.
  * Identified active hosts within the scanned local network.
  * Recorded the scan results for documentation.

* **Network Topology Generation:**
  * Switched to the **Topology** tab in Zenmap to visually map the discovered nodes.
  * Reviewed the topology generated from the authorized local network scan.
  * Captured the topology as evidence for the project documentation.
 





 
 ⚙️ 4. Methodology & Execution

### Phase 1: Footprinting & Reconnaissance with theHARVESTER

* **Help & Usage Verification:** Inspected tool parameters and guidelines using command-line options (`theHarvester -h`) to understand syntax flags like domain selection (`-d`), result limits (`-l`), and data sources (`-b`).

* **Task 1 (Baidu Source Query):** Executed targeted search against `microsoft.com` using the Baidu module with a result limit of 1000 and saving the text file as evidence using `cat task1.txt`:

  * **Execution Command:**

        theHarvester -d microsoft.com -l 1000 -b baidu

  * **Output Evidence:**

        cat task1.txt

  * **Analysis & Objective:**
    * **What we are trying to prove:** Assesses how much organization-specific infrastructure is publicly discoverable via an eastern search engine module (`baidu`) without interacting directly with the target network.
    * **What is shown:** The output displays raw OSINT data harvested from Baidu, including discovered subdomains and associated IP addresses tied to `microsoft.com`.

* **Task 2 (Multi-Source Enumeration):** Executed broader searches against `microsoft.com` using all available sources (`all`) with a result limit of 50 and saving the text file as evidence using `cat task2.txt`:

  * **Execution Command:**

        theHarvester -d microsoft.com -l 50 -b all

  * **Output Evidence:**

        cat task2.txt

  * **Analysis & Objective:**
    * **What we are trying to prove:** Demonstrates the capabilities and limitations of automated multi-source enumeration (`all`), showing how the tool attempts to aggregate intelligence across a wide spectrum of public and proprietary OSINT feeds simultaneously.
    * **What is shown:** The output displays harvested asset data alongside warning messages for services that require API credentials. This demonstrates the limitations of restricted or registration-bound OSINT sources when API credentials are not configured.

### Phase 2: Network Scanning with Zenmap

* Opened Windows Command Prompt and executed `ipconfig` to determine the local interface configuration, including the active IPv4 address, subnet mask, and default gateway.

* Entered the **actual authorized local subnet range obtained from `ipconfig`** into Zenmap, selected the **Ping scan** profile, and executed the corresponding Nmap command.

* **Zenmap Host Discovery Results:**
  * Executed the ping sweep against the authorized local subnet.
  * Identified active hosts within the scanned local network.
  * Recorded the scan results for documentation.

* **Network Topology Generation:**
  * Switched to the **Topology** tab in Zenmap to visually map the discovered nodes.
  * Reviewed the topology generated from the authorized local network scan.
  * Captured the topology as evidence for the project documentation.
 






 🛡️ Consolidated Security Assessment & Risk Matrix

The reconnaissance and network-scanning activities provided visibility into publicly available information and the authorized local network environment. The following risk matrix summarizes the security observations identified during the practical assessment.

| Finding / Observation | Risk Level | Impact | Recommendation |
|---|---|---|---|
| Publicly available domain information | Medium | Information may assist reconnaissance activities. | Regularly review publicly exposed organizational information and remove unnecessary disclosures. |
| Discoverable subdomains and hosts | Medium | Exposed assets may increase the organization's external attack surface. | Maintain an updated inventory of public-facing assets and secure unnecessary subdomains. |
| Publicly discoverable email addresses | Low | Addresses may be targeted by spam or phishing attempts. | Minimize unnecessary exposure of employee email addresses and strengthen email security controls. |
| Active hosts identified on the authorized local network | Medium | Network discovery can reveal available systems to an attacker with network access. | Use appropriate network segmentation, firewall rules, and access controls. |
| Network topology information | Medium | Network structure can provide useful information during reconnaissance. | Restrict unnecessary network visibility and monitor unauthorized scanning activity. |
| OSINT/API source limitations | Low | Incomplete information may result when sources require authentication or API keys. | Use authorized and properly configured intelligence sources during security assessments. |

### Risk Rating Summary

| Risk Level | Description |
|---|---|
| **High** | Could result in significant security impact and requires immediate attention. |
| **Medium** | Could assist reconnaissance or increase exposure and should be addressed. |
| **Low** | Limited security impact but should still be monitored and reviewed. |

### Overall Security Considerations

The assessment demonstrates that reconnaissance techniques can reveal information about publicly exposed assets and authorized internal network infrastructure. Organizations should regularly review their external attack surface, maintain accurate asset inventories, apply appropriate access controls, and monitor network activity.





## 🛠️ Challenges Encountered & Solutions

### Challenge 1: theHarvester Source Limitations

**Issue:**  
Some theHarvester data sources may require API keys, authentication, or may not return results.

**Solution:**  
Reviewed the available source options and used accessible sources within the authorized lab environment. Source/API limitations were documented instead of bypassed.

---

### Challenge 2: Understanding theHarvester Commands

**Issue:**  
TheHarvester includes multiple command-line options for domains, result limits, and data sources, which can initially be confusing.

**Solution:**  
Used the built-in help option:

```bash
theHarvester -h








## 🏁 Conclusion

This project successfully demonstrated the practical application of foundational reconnaissance and network discovery methodologies through structured cybersecurity lab exercises.

* **Footprinting & Reconnaissance:** Utilizing theHarvester on Kali Linux demonstrated how OSINT techniques can be used to gather publicly available information and identify potential attack-surface data from authorized target domains without directly interacting with the target infrastructure.

* **Network Scanning:** Using Zenmap and Windows interface diagnostics (`ipconfig`) provided hands-on experience in identifying local subnets, executing ping sweeps, discovering active hosts, and visualizing network topologies within an authorized environment.

* **Operational Awareness:** Documenting challenges such as network-interface selection, command-line syntax, and scan-scope configuration reinforced the importance of careful execution, accurate documentation, and proper authorization during professional security assessments.

Overall, the tasks completed under the NetworkWalks Cybersecurity Internship successfully bridged theoretical cybersecurity concepts with practical reconnaissance and network-discovery techniques.
All observations in this assessment are intended for educational purposes and should be interpreted within the scope of the authorized testing environmen








## 🛠️ Tools Used

* **Oracle VM VirtualBox 7.1.18** — (Download Link)
* **Kali Linux 2026.1** — (Download Link)
* **theHarvester** — Open-source intelligence (OSINT) and footprinting tool
* **Zenmap** — (Download Link)
* **7-Zip** — (Download Link)
* **GitHub** — (GitHub Platform)














