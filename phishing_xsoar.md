**Introduction**

Phishing emails are one of the most frequent, easily executable, and harmful security attacks that organizations, regardless of size, face today. High-volume, persistent phishing alerts are a time sink for the security team, with incident response requiring coordination between multiple security products and communications with end users. Phishing is involved in almost 40% of security incidents, according to the [2022 Unit 42 Incident Response Threat Report](https://www.paloaltonetworks.com/unit42/2022-incident-response-report).

_“Attackers are looking for easy ways in. Phishing is a low-cost method with high results for attackers.”_

**Phishing Content Pack - New 2023 Features**

The [Phishing content pack](https://cortex.marketplace.pan.dev/marketplace/details/Phishing/) is the main pack for all phishing purposes. If you need to respond to phishing incidents based on user reports, this is the content pack for you. With this content pack, you can significantly reduce the time your security analysts spend on phishing alerts and standardize the way you manage phishing incidents.

We’ve added new features to our most popular Cortex Marketplace content pack to help you better respond to phishing campaigns in 2023.

### **Phishing - Generic v3 Playbook**

**Semi-Automated Remediation**

When detecting phishing attempts, immediate action is essential to mitigate potential harm. By blocking indicators associated with the phishing attempt, we limit the attackers' ability to execute their malicious operations successfully and prevent further spread of the phishing campaign.

However, automatically blocking indicators runs the risk of inadvertently blocking legitimate indicators, thereby potentially disrupting the organization's regular activities and workflow.

By setting the “AutoBlockIndicators” playbook input to “false” (the default value) and using the enhanced version of the [Block Indicators - Generic v3](https://xsoar.pan.dev/docs/reference/playbooks/block-indicators---generic-v3) playbook available in the Cortex Marketplace, the analyst can choose the indicators that will be blocked automatically. Once the phishing incident is classified as malicious, the playbook will stop at a data collection task that asks the analyst to select the indicators to block.

**Threat Intelligence Analysis**

Cybersecurity threat intelligence provides valuable insights into the latest and emerging threats, attack techniques, and malicious actors. By staying informed about evolving cyberthreats, investigators can better comprehend the tactics, techniques, and procedures used by attackers, enabling them to respond more effectively to incidents.

The " [TIM - Indicator Relationships Analysis'](https://xsoar.pan.dev/docs/reference/playbooks/tim---indicator-relationships-analysis)' playbook aims to identify connections between indicators of compromise (IOCs) and reported campaigns sourced from feeds linked to Cortex XSOAR Threat Intelligence Management (TIM). When phishing incident-related IOCs are associated with a particular campaign, this information will be presented in the phishing incident layout within the "Investigation" tab of the incident.


**Spear Phishing - Keywords Analysis**

Phishing attacks have become increasingly sophisticated, with cybercriminals customizing their tactics to target specific organizations. This tailored approach, known as spear phishing, poses a significant threat to businesses and individuals alike. According to the [Recent Trends in Internet Threats](https://unit42.paloaltonetworks.com/internet-threats-late-2022/) report by Unit 42, we observed an increase in phishing attacks disguising themselves as online document and storage platforms in Q3 and Q4 2022, up from 27.8% to over 38.1% in Q2. During the same time period, fake online shopping and marketplace sites became more popular as sources of phishing campaigns.

Using the “ [Spear Phishing Investigation](https://xsoar.pan.dev/docs/reference/playbooks/spear-phishing-investigation)” sub-playbook, analysts can select a list of keywords associated with the organization, like names of stakeholders or systems and applications that are being used, and detect whether they exist in the phishing mail content.

The keywords can be provided via the playbook input “KeyWordsToSearch” as a comma-separated list or as XSOAR list object.


When a keyword is found in the email body, it will be displayed in the layout “Investigation” tab in a tag field, under the “Spear Phishing Investigation” section.

Since it's a tag type field, the analyst can search and filter incidents and identify phishing mails containing the same keywords.


**Determine phishing mail sender verdict as malicious**

Once a phishing incident verdict is determined as malicious, the email sender address verdict will be set as malicious as well.

When the Cortex XSOAR TIM module classifies the sender's email address in a phishing email as malicious, it triggers the marking of that email address as malicious in any subsequent phishing incidents linked to it. This ensures that analysts and playbooks will consider this classification when making their final determination about the incident verdict.


**Conclusion**

These enhancements to our Cortex phishing playbooks represent a significant leap forward in the battle against phishing attempts. With powerful automation, intelligent analysis, and a seamless integration into threat intelligence data, security teams can now bolster their defenses and respond with unparalleled speed and accuracy.