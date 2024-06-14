---
simulation:
    title: 'Explore the capabilities of Copilot in Microsoft Defender XDR'
    module: 'Explore use cases of Microsoft Copilot for Security'
---

# Explore the capabilities of Copilot in Microsoft Defender XDR

In this exercise, you investigate an incident in Microsoft Defender XDR. As part of the investigation, you explore the key features of Microsoft Copilot in Microsoft Defender XDR, including incident summary, device summary, script analysis, and more. You also pivot your investigation to the standalone experience and use the pin board as a way to share details of your investigation with your colleagues.

- You're logged in as Avery Howard and have the Copilot owner role. 
- For most of the tasks in this exercise, you work in the Microsoft Defender portal and access the embedded Copilot capabilities of Defender XDR. Towards the end of the exercise, you pivot to the standalone experience.
- You'll work in Microsoft Defender, using the new unified security operations platform, to access the embedded Copilot capabilities in Microsoft Defender XDR. Towards the end of the exercise, you pivot to the standalone experience of Microsoft Copilot for Security.

> [!NOTE]
> The environment for this exercise is based on a simulation, generated from pre-determined screen captures of the actual product. As a limited simulation, links on a page may not be enabled and text-based inputs that fall outside of the specified script are not be supported.

> [!NOTE]
> When a lab instruction calls for opening a link to the simulated environment, it is generally recommended that you open the link in a new browser window so that you can simultaneously view the instructions and the exercise environment. To do so, select the right mouse key and select the option.

### Task: Explore Incident summary and guided responses

1. Open the simulated environment by selecting this link: **Microsoft Defender portal**.

1. From the Microsoft Defender portal, expand **Incidents & alerts** then select **Incidents**.
1. In the search field, enter incident ID **30342**, named Human-operated ransomware attack was launched from a compromised asset (attack disruption). then select it to open the incident, and open it. 

1. This is a complex incident. Defender XDR provides a great deal of information, but with 72 alerts it can be a challenge to know where to focus. On the right side of the incident page, Copilot automatically generates an **Incident summary** that helps guide your focus and response.
    1. Copilot's summary describes how this incident has evolved, from initial access to lateral movement, and exfiltration. It identifies specific devices, and indicates that the PsExec tool was used to launch executable files. Copilot also names the threat actor involved in the incident.
    1. These are all items you can leverage for further investigation. You explore some of these in subsequent tasks.

1. Scroll down on the Copilot panel and just beneath the summary are **Guided responses**. Guided responses recommend actions in support of triage, containment, investigation, and remediation.
    1. The first item in the triage category it to Classify this incident. Select **Classify** to view the options. Review the guided responses in the other categories.
    1. Select the **Status** button and filter on **Completed**. Two completed activities show labeled as Attack Disruption. Automatic attack disruption is designed to contain attacks in progress, limit the impact on an organization's assets, and provide more time for security teams to remediate the attack fully. To learn more, visit [Automatic attack disruption in Microsoft Defender XDR](/defender-xdr/automatic-attack-disruption).

1. Keep the incident page open, you'll use it in the next task.

### Task:  Explore device and identity summary

1. From the incident page, select the first alert **Suspicious URL clicked**.

1. Copilot  automatically generates an alert summary, which provides a wealth of information for further analysis. For example, the summary identifies a malicious file Rubeus.exe, it identifies data collection activities, reconnaissance and discovery activities, and more.

1. There's a lot of information on the page, so to get a better view of this alert, select **Open alert page**. It's on the third panel of the page, next to the incident graph and below the alert title.

1. On the top of the page, is card for the device parkcity-win10v. Select the ellipses and note the options. Select **Summarize**. Copilot generates a device summary. It's worth nothing that there are many ways you can access device summary and this is just one convenient method. The summary shows the device is a VM, identifies the owner of the device, it shows its compliance status against Intune policies, and more.

1. Next to the device card is a card for the owner of the device. Select **parkcity\jonaw**. The third panel on the page updates from showing details of the alert to providing information about the user Jonathan Wolcott, an account executive, whose Entra ID risk and Insider risk severity are classified as high. These aren't surprising given what you've learned from the Copilot incident and alert summaries. Select **Summarize**, displayed underneath the user's name to obtain an identity summary generated by Copilot.

1. Keep the alert page open, you'll use it in the next task.

### Task:  Explore script analysis

1. Let's Focus on the alert story. Select **Maximize** to get a better view of the process tree. Optionally, select **Expand all**. From maximized view, you begin to get a clearer view of how this incident came to be. Many line items indicate that powershell.exe executed a script. Since the user Jonathan Wolcott is an account executive, it's reasonable to assume that executing PowerShell scripts isn't something this user is likely to be doing regularly.

1. Expand the first instance of **powershell.exe execute a script**, it's the one showing the timestamp of 4:57:11 AM. Copilot has the capability to analyze scripts. Select **Analyze**.
    1. Copilot generates an analysis of the script and suggests it could be a phishing attempt or used to deliver a web-based exploit.
    1. Select **Show code**. The code shows a defanged URL.
    1. Expand the line item that follows, labeled **powershell.exe opened the HTTP link...**. Defender XDR provides a link to the Mitre technique employed. Select **T1204.001: Malicious Link** to review information about this Mitre technique.

1. There are several other items that indicate powershell.exe executed a script. Expand the one labeled **powershell.exe -EncodedCommand...** with the timestamp 5:00:47 AM. The original script was base 64 encoded, but Defender has decoded that for you. For the decoded version, select **Analyze**. The analysis highlights the sophistication of the script used in this attack.

1. Close the alert story page by selecting the **X** (the X that is to the left of Copilot panel). Now use the breadcrumb to return to the incident. Select **Human-operated ransomware attack was launched from a compromised asset (attack disruption)**.

### Task:  Explore file analysis

1. You're back at the incident page. In the alert summary, Copilot identified the file Rubeus.exe, which is associated with the 'Kekeo' malware. You can use the file analysis capability in Defender XDR to see what other insights you can get. There are several ways to access files. From the top of the page, select the **Evidence and Response** tab.

1. From the left side of the screen select **Files**.
1. Scroll down until you see **Rubeus.exe**, then select it. 
1. From the windows opens, select **Analyze**. Copilot generates a summary.

### Task: Pivot to the standalone experience

This task is complex and requires the involvement of more senior analysts. In this task, you pivot your investigation and run the Defender incident promptbook so the other analysts have a running start on the investigation. You pin responses to the pin board and generate a link to this investigation that you can share with more advanced members of the team to help investigate.

1. Return to the incident page by selecting the **Attack story** tab from the top of the page.

1. Select the ellipses next to Copilot's Incident summary and select **Open in Copilot for Security**.

1. Copilot opens in the standalone experience and shows the incident summary. You can also run more prompts. In this case, you run the promptbook for an incident. Select the **prompt icon** ![prompt icon](media/prompt-icon.png). 
    1. Select **See all promptbooks**.
    1. Select **Microsoft 365 Defender incident investigation**.
    1. The promptbook page opens and asks for the Defender Incident ID. Enter **30342** then select **Run**.
    1. Review the information provided. By pivoting to the standalone experience and running the promptbook, the investigation is able to invoke capabilities from a broader set security solution, beyond just Defender XDR, based on the plugins enabled.

1. Select the **box icon ![box icon](media/box-icon.png)** next to the pin icon to copy all the responses to the pin board, then select the **Pin icon ![pin icon](media/pin-icon.png)** to save those responses to the pin board.

1. Select the **pin board icon ![pin board icon](media/pinboard-icon.png)** to open the pin board. The pin board holds your saved prompts and responses, along with a summary of each one.

1. From the top of the page, select **Share** to view your options. By sharing the incident via a link or email, people in your organization with Copilot access can view this session. Close the window by selecting the **X**.

1. You can now close the browser tab to exit the simulation.

### Review

This incident is complex. There's a great deal of information to digest and Copilot helps summarize the incident, individual alerts, scripts, devices, identities, and files. Complex investigations like this may require the involvement of several analysts. Copilot facilitates this by easily sharing details of an investigation.
