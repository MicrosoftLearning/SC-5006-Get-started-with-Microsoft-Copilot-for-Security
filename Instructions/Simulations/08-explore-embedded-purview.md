---
simulation:
    title: 'Explore the capabilities of Copilot in Microsoft Purview'
    module: 'Explore use cases of Microsoft Copilot for Security'
---

# Explore the capabilities of Copilot in Microsoft Purview

In this exercise, you explore the Copilot summarization capabilities available from within Microsoft Purview data security and compliance solutions, including Data Loss Prevention (DLP), Insider Risk Management, Communication Compliance, and eDiscovery (Premium).  You start by verifying that the Microsoft Purview plugin is enabled.

- You're logged in as Avery Howard. You have the Copilot owner role and you have specific role permissions required for access to each of the afore mentioned Microsoft Purview solutions.
- You'll work with specific Microsoft Purview solutions, using the new Microsoft Purview portal and access the embedded Copilot capabilities of those solutions.

This exercise should take approximately **25** minutes to complete.

> [!NOTE]
> The environment for this exercise is based on a simulation, generated from pre-determined screen captures of the actual product. As a limited simulation, links on a page may not be enabled and text-based inputs that fall outside of the specified script are not be supported.

> [!NOTE]
> When a lab instruction calls for opening a link to the simulated environment, it is generally recommended that you open the link in a new browser window so that you can simultaneously view the instructions and the exercise environment. To do so, select the right mouse key and select the option.

### Task: Enable the Microsoft Purview plugin

In this task, you enable the Microsoft Purview plugin. For this task, you work in the standalone experience.

1. Open the simulated environment by selecting this link: **Microsoft Copilot for Security**.

1. From the Microsoft Copilot for Security landing page, select the sources icon in the prompt bar.
    1. Expand the Microsoft plugins
    1. Scroll down so that the Microsoft Purview plugin is visible.
    1. Select the information icon. Note the instructions then close the plugins page.

1. Select the home menu (hamburger icon)
    1. Select owner settings.
    1. Enable the toggle for “Allow Copilot for Security to access data from your Microsoft 365 services.”

1. Now that you’ve enabled Copilot to access data from your Microsoft 365 services, return to the plugins page and enable the Microsoft Purview plugin.

### Task: Gain comprehensive summary of Insider Risk Management alerts

For this and all subsequent tasks, you explore the Copilot functionality embedded in Microsoft Purview.

In this task, you explore the value Copilot provides in summarizing an Insider Risk Management alert. You start by first reviewing an alert, without Copilot for Security. It can be challenging to know where to start your investigation when risky activities are detected over a long period of time. You'll then see how Copilot can address this same task with the click of a button.

Microsoft Copilot assumes the permissions of the user when it tries to access the data to answer queries. To access data associated with the Microsoft Purview Insider Risk Management solution, users should have previously been assigned an appropriate role.

1. Open the environment by selecting this link (use the right mouse key and select,'Open link in split screen window'): **Microsoft Purview Portal.**

1. From the Microsoft Purview portal, select Insider Risk Management.

1. Select Alerts

1. In the search bar, enter **86e52569**. Select this alert.
    1. This alert deals with Potential data theft - Employee Departure. Under User details, you can gain more context on why the user was identified as a high impact user by selecting **View all details**. Review the user details then select the **X** to close the User details window.
    1. The page is currently displaying all risk factors. If you scroll down, there are even more details to consume! Including all of the risk factors for this user’s activity and the content detected in the alert.
    1. Select the **Activity explorer** tab, to quickly review a timeline of potentially risky activity and filter for specific risk activities associated with the alert. Select, the first activity on the list, labeled **Email sent to external recipient**. Review the information provided then select **X** to close the window.
    1. Select the **User activity tab**. Here you view a scatter plot, over a 1 month, 3 month, or 6 month timeline; alongside details of each event – such as the user exfiltrated data one day before submitting their resignation.
    1. Clearly, there're many insightful details to analyze!

1. With Copilot for Security, you can gain a comprehensive summary of an alert – in the single click of a button! Select **Summarize**.
    1. This comprehensive summary provides key details, including alert severity, user details like their HR offboarding event and much more! 
    1. These summaries help accelerate investigations by helping you quickly gain context into user intent and timing of risky activities, enabling you to tailor your investigation with specific dates in mind and quickly pinpoint sensitive files at risk.

1. From the left navigation panel, select **Home** to return the Microsoft Purview portal. You'll return to this page in the next task.

### Task: Gain comprehensive summary of Data Loss Prevention alerts.

In this task, you explore the value Copilot provides in summarizing a Data loss prevention alert. As in the previous task, you start by first reviewing an alert, without Copilot for Security. You then discover how Copilot can address this same task with the click of a button.

Microsoft Copilot assumes the permissions of the user when it tries to access the data to answer queries. To access data associated with the Microsoft Purview Data Loss Prevention solution, users should have previously been assigned an appropriate role.

1. Select **Data loss prevention**, then select **Alerts**

1. Investigating DLP alerts can be overwhelming due to the large number of sources to analyze, including apps, cloud services, email, endpoints and chat, and the varying rules and conditions of a policy.

1. Select the alert labeled, **DLP policy match for document cardholder transaction Log.xlsx in OneDrive**.
    1. The alert page opens to the **Details** page The details tab provides additional details, such as name of alert, location, and user involved. You can expand this view by selecting **View details**.
    1. Select the **Events** tab. For the selected event, you can view event details, impacted entities and more.
    1. Select the **Classifiers** tab. Under classifiers, you can view the specific sensitive information types or trainable classifiers that were matched.
    1. You can also select File Activity. There is lots of information to analyze.

1. Now view the information that Copilot can generate with the click of a button.
    1. Return to the Alerts page and select the same alert. **DLP policy match for document cardholder transaction Log.xlsx in OneDrive**.
    1. Select **Get a summary from Security Copilot**.
    1. This comprehensive summary provides key details, including policy rules, source, files involved and more. Additionally, the summary pulls the user risk levels from Insider Risk Management, providing integrated insights across data security solutions. These summaries provide you with a better starting point for further investigation.

1. From the left navigation panel, select **Home** to return the Microsoft Purview portal. You'll return to this page in the next task.

### Task: Gain contextual summary of Communication Compliance policy matches

In this task, you explore the capability of Copilot in Microsoft Purview Communication Compliance. Reviewing communication violations can be time-consuming, especially when reviewing lengthy content like meeting transcripts, email attachments, Teams attachments, or extensive text. Copilot can address this, and more, with the click of a button.

Microsoft Copilot assumes the permissions of the user when it tries to access the data to answer queries. To access data associated with the Microsoft Purview Communication Compliance solution, users should have previously been assigned an appropriate role.

1. From the New Microsoft Purview portal, select **View all solutions**, then select **Communication Compliance**, listed under Risk & Compliance.

1. Select **Policies**.

1. Select **Regulatory compliance** policy to identify potential regulatory compliance violations.

1. From the list of violations triggered by the policy, select the Teams communication with the subject **Happy new year valued customers!** to expand the list. Select the first item from the expanded view.

1. Communication Compliance is able to pinpoint the timestamps when a potential violation has occurred and highlight conditions matched, but there's still a good bit of text to read through.
    1. With Copilot for Security, you can gain a comprehensive summary of an alert in the single click of a button! Select **Summarize**.
    1. You can also ask follow-up questions. Use copy/paste to enter **Does this violation indicate unauthorized disclosure?**

1. From the left navigation panel, select **Home** to return the Microsoft Purview portal. You'll return to this page in the next task.

### Task: Gain contextual summary of evidence collected in eDiscovery review sets (Preview)

In this task, you explore the capability of Copilot to Microsoft Purview to gain a contextual summary of evidence collected in an eDiscovery review set.

Microsoft Copilot assumes the permissions of the user when it tries to access the data to answer queries. To access data associated with the Microsoft Purview eDiscovery solution, users should have previously been assigned an appropriate role.

Let’s start by showing you how to review evidence collected in eDiscovery review sets, without Copilot for Security.

Legal investigations can take hours, days, even weeks to sift through the list of evidence collected in review sets, requiring costly resources like outside council to manually go through each document to determine the relevancy to the case.

1. From the left navigation panel in the new Microsoft Purview portal, select **Cases**

1. Select **Contoso stock manipulation**, then select the tab **Review sets**.

1. From the review sets page, open the review set listed **RS - Stock manipulation Teams conversation + cloud attachments**
    1. From the bottom of the Overview page, select **Open review set**.
    1. Using the filter, filter for Teams conversations:
        1. Filter - **File class**.
        1. Select an operator - **Equals any of**.
        1. Select Any -  **Conversation**.
    1. From the results, select item **#4**.
        1. Information about the conversation appears in the window to the right. **Scroll** to view the source history. There's quite a bit of text included in this teams conversation. It can be time-consuming to sift through the information.
        1. With Copilot for Security, you can gain a comprehensive summary of the conversation in the review set – in the single click of a button! Select **Summarize**. Copilot also provides prompt suggestions and the prompt bar for you to enter your own prompts in furtherance of the investigation. This helps you save time and conduct investigations more efficiently!

1. Refer back to the list of Teams conversations. This time, select item **#13** .
    1. The subject is displayed in a non-English language. This is common challenge with multi-national corporation whose employees speak various languages. The window with the source conversations shows a conversation history with non-English language. Select **Summarize** to view a summary in English, which is my default language for Copilot.
    1. Expand item 13 by selecting the **>**. Within Microsoft Teams, you can send cloud attachments, which are links to documents. The first item under the expanded view is an attached document. Select **Summarize** to. So you can see the attachment shared within the Teams chat is rather lengthy.

1. From the left navigation panel, select **Home** to return the Microsoft Purview portal. You'll return to this page in the next task.

### Task: Create Keyword Query Language (KeyQL) queries using natural language to search in eDiscovery (Premium)

In this task, you explore the capability of Copilot in Microsoft Purview eDiscovery (Premium) to create Keyword Query Language (KeyQL) queries using natural language. Users provide a prompt in natural language and Copilot generates a query in KeyQL language, making your search iterations faster and more accurate. This feature also enables analysts, at all levels, to conduct advanced investigations using KeyQL.

Microsoft Copilot assumes the permissions of the user when it tries to access the data to answer queries. To access data associated with the Microsoft Purview eDiscovery solution, users should have previously been assigned an appropriate role.

1. From the New Microsoft Purview portal, select **View all solutions**, then select **eDiscovery**, listed under Risk & Compliance.

1. Select **Cases**.
1. Select **Fabrikam vs Contoso**.
1. Select **Create a search**.
    1. Enter a search name.
    1. Enter a description.
    1. Select **Create**.
1. Add a data source – in this case, you want to search the group **Sales**.
1. From the box labeled natural language prompt:
    1. Select **View prompts**. This is a great starting point. You could look at suggested prompts to determine how to craft a natural language query for suggested prompts. For example, Find all emails containing the words budget and finance and have attachments. 
    1. For this example, however, you know what you are looking for. You’ve been told that you need to find all conversations related to a recent acquisition. Enter **Find all conversations that contain the keywords; acquisition, stock, Bitdefender, Frostvision, offshore**.
    1. When you enter your natural language prompt, Copilot may work to refine the query to ensure a more accurate query output. Select **Refine** then **Accept**.
    1. Select **Generate KeyQL**. Copilot for Security refines the prompt and then in a simple click, can generate the query within seconds!
    1. The resulting query is displayed in the Keyword Query Language  (KeyQL) result text box. Select **CopyKeyQL**, then paste it the KeyQL text box. From here, you can run the query. In this simulation, you won't run the query.

1. A query can be generated manually with the Condition builder, but it can be more time-consuming. Also, if you input an incorrect property or condition, it can mean the difference between a right or wrong result – meaning you have to start over and further delay the investigation.

### Review

With Microsoft Copilot in Microsoft Purview, data security and compliance admins can use the power of AI to assess risk exposure more quickly than is otherwise possible, directly from within Microsoft Purview solutions.

In this exercise, you explored the powerful functionality of Copilot to aid in your compliance investigations with DLP, Insider Risk Management, Communication Compliance, and eDiscovery.
