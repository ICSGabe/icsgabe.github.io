---

title: "Has OT Been Compromised? (The Problem)"

date: 2023-12-20

categories: [Incident Response]

tags: [IR, OT, DFIR]

image:
    path: /assets/images/industrial_incident_image.png

---

🌐✨

### **Part 1: The Problem**

When I’ve performed incident response services for customers, one of the first questions during the triage call is “Has OT been compromised?”. **Determining if an OT compromise has occured is not easy**. It is not always so simple to pinpoint the answer to that questions because of several reasons that i've encountered and that you might've as well:

  
1. **Lack of** **EDR tools in OT**: EDR tools can give a strong indication of the presence of malware due to modern alerting and integration into SIEM solutions. The problem is that EDR tools are rarely if ever deployed across the entirety of OT assets. As a result, there is a limited view of endpoint security alerts and indicators during a full out incident.

2. **Rarity of IDS and lack of tuning**: There is rarely an intrusion detection capability within OT environments. Customers are starting to adopt some of the popular vendor products for network security monitoring like Nozomi Guardian, Claroty CTD, and the Dragos Platform but for organizations without the investment and internal resources for tool tuning, the solutions aren't very usable during an actual incident.

3. **OT security organizational knowledge and skill gaps**: OT system owners, engineers, and technicians are not typically cybersecurity-aware. This is changing but even today, the awareness of their environment's attack surfaces and asset vulnerabilities of OT systems are rarely understood by OT staff who daily manage the systems. This results in incidents going unnoticed and undetected until it affects production system operations and critical business processes.

4. **No security-related logs or telemetry data has been collected**: The primary goal of most OT environments is to safely keep business-critical systems running and not necessarily keeping them secure from today's cybersecurity threats. As a result, monitoring telemetry and collecting logs for security-related purposes are rarely maintained.