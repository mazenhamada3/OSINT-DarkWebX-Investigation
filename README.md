# OSINT Investigation: DarkWebX

This repository contains the findings of an OSINT (Open Source Intelligence) investigation into the alias "DarkWebX." The investigation used publicly available sources and tools to trace the digital footprint of the cybercriminal, including social media accounts, email addresses, potential data breaches, and IP addresses.

## Objectives

The main objectives of this investigation were to:
- Enumerate social media accounts associated with the alias.
- Identify linked email addresses.
- Check for leaked credentials using breach databases.
- Gather potential IP addresses from forum data and logs.
- Compile a structured intelligence report.

## Tools Used

The following tools were utilized during the investigation:
- **Sherlock**: Used for discovering social media accounts associated with the alias.
- **theHarvester**: Used for discovering email addresses linked to the alias.
- **Have I Been Pwned**: Used to check for any breaches associated with the discovered email addresses.
- **Google Dorking**: Used for uncovering additional indexed information about the alias.
- **WHOIS lookups**: Used to trace IP addresses to hosting services or VPNs.

## File Structure

- **OSINT_Report_DarkWebX.pdf**: The comprehensive OSINT investigation report.
- **DarkWebX.txt**: A list of 32 websites associated with "DarkWebX" (including GitHub, Reddit, and more).
- **hackerforums_results.json**: A JSON file containing results of IP and hostnames discovered on hackerforums.net.
- **hackerforums_results.xml**: An XML version of the same results from hackerforums.net.

## How to Run the Tools

1. **Sherlock** - To search for social media accounts linked to "DarkWebX":
    ```bash
    python3 -m sherlock DarkWebX -o output.txt
    ```
2. **theHarvester** - To search for email addresses linked to "DarkWebX":
    ```bash
    theHarvester -d hackerforums.net -l 100 -b all -f harvester_results
    ```
3. **Have I Been Pwned (HIBP)** - To check email addresses for breaches:
    ```bash
    haveibeenpwned.py -e darkwebx@yahoo.com
    ```
4. **Google Dorking** - To search for additional indexed information:
    Use queries such as:
    ```
    "DarkWebX" site:pastebin.com
    "DarkWebX" filetype:log
    ```

## Findings

- **Social Media Accounts**: Identified across multiple platforms including GitHub, Reddit, and YouTube.
- **Email Addresses**: Several email addresses linked to the alias, such as `darkwebx@yahoo.com` and `darkwebx@outlook.com`.
- **Breach Check**: No breaches or leaked credentials found.
- **IP Addresses**: Several IP addresses traced back to global hosting services, suggesting the use of VPNs/proxies.

## MITRE ATT&CK Mapping

The activities related to "DarkWebX" were mapped to the MITRE ATT&CK framework:
- **Reconnaissance**: Active scanning and information gathering from forums and leaks.
- **Resource Development**: Creation of multiple accounts across social and technical platforms.
- **Defense Evasion**: Use of VPNs and secure email services to obscure identity and location.
