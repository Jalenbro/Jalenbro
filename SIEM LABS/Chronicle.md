
## Overview 

In Chronicle, you can search for events using the Search field, while Procedural Filtering refines your search by applying specific filters. This allows you to include or exclude results based on criteria like event type or log source. Additionally, YARA-L is a specialized language used to create rules for searching through ingested log data.

Chronicle offers two types of searches: Unified Data Mode (UDM) and Raw Log Search.

Unified Data Mode (UDM) is the default search method in Chronicle. It searches through security data that has been ingested, parsed, and normalized. Because UDM uses indexed and structured data, it delivers faster search results compared to Raw Log Search.

Raw Log Search examines raw, unparsed logs, making it slower than UDM. This method allows you to search for specific details like usernames, filenames, and hashes. It also supports regular expressions for matching specific patterns, offering more granular search capabilities.

## Scenario 

You are a security analyst at a financial services company. You receive an alert that an employee received a phishing email in their inbox. You review the alert and identify a suspicious domain name contained in the email's body: `signin.office365x24.com`. You need to determine whether any other employees have received phishing emails containing this domain and whether they have visited the domain. You will use [Chronicle](https://demo.backstory.chronicle.security/?warstory=) to investigate this domain.

## Expectation 
* Access threat intelligence reports on the domain
* Identify the assets that accessed the domain
* Evaluate the HTTP events associated with the domain
* Identify which assets submitted login information to the domain
* Identify additional domains

## Step-by-step 

1. Launch Chronicle.
2. Perform a domain search.
* In the search bar, type `signin.office365x24.com` and click Search. Under `DOMAINS`, click signin.office365x24.com to complete the search. Below are the screenshots of the legacy view, VT, and IP address `40.100.174.34`.
    
  Legacy View
    
 ![Screenshot 2024-08-19 235910](https://github.com/user-attachments/assets/92b8b717-5948-45ef-a31b-cfb783b48dd8)


  VT 
  ![Screenshot 2024-08-19 235947](https://github.com/user-attachments/assets/a918fe65-8ab7-4962-8e96-115d05327256)

 

 IP address `40.100.174.34`
  ![Screenshot 2024-08-20 000033](https://github.com/user-attachments/assets/b7453b63-befc-4ed6-b1f1-37e0c15cbd37)


  
* Evaluate the search result (Legacy view).
   
  | Observe | Description | Note |
  | :----: | :----: | :----: |
  | VT context | Provides  `VirusTotal` information available for the domain. | Chronicle found 7 security vendors flagged this domain as malicious.  | 
  | WHOIS | Summary of information about the domain using WHOIS which includes domain names, contact information of the domain owner. This may help determining the origin of malicious websites. | Reference time can be found and first/last seen is 7 months ago, as of February 10th, 2024. |
  | Prevalence | A graph which outlines historical prevalence of the domain. | The domain has been accessed on July 9th, 2023 and February 10th, 2024. |
  | Resolved IP | This provides additional context about the domain such as the IP address to `signin.office365x24.com`. This can be helpful for further investigation to determine whether there is a broader compromise. | We found 2 IP addresses that map to `signin.office365x24.com`: `104.215.148.63` & `40.100.174.34`. |
  | Sibling Domains | This provides additional context about the domain, such as the top or parent domain. | We found one sibling domain: `login.office365x24.com`.
  | ET Intelligence Rep List | This includes additional context on the domain, such as known threats using ProofPoint's Emerging Threats (ET) Intelligence Rep List | Category: Drop site for logs or stolen credentials. Confidence (Min: 20, Max 127): 22, Severity: Medium, Active from: 2018-12-31 T00:00:00Z, Active until: 2019-0-8T00:00:00Z. More information can be found [here](https://tools.emergingthreats.net/docs/ET%20Intelligence%20Rep%20List%20Tech%20Description.pdf).|
  | Timeline | This provides information about the events and interactions made with the domain. | It reveals the details about the HTTP requests made including `GET` and `POST`. `GET` retrieves the data from a server while a `POST` request submits data to a server`.|
  | ASSETS | This provides a list of the assets that have been assessed the domain. | There are 6 assets that have accessed the domain. |

3. Launch an Investigation. 
  * According to ET Intelligence Rep List, `signin.office365x24.com` is categorized as "Drop site for logs or stolen credentials".
  * The following assets are those who accessed the domain:
      * `ashton-davidson-pc`
      * `bruce-monroe-pc`
      * `coral-alvarez-pc`
      * `emil-palmer-pc`
      * `jude-reyes-pc`
      * `roger-spence-pc`
  * We found 2 IP addresses that map to `signin.office365x24.com`: `104.215.148.63` & `40.100.174.34`.
  * The IP address `40.100.174.34` resolves to `signin.office365x24.com` and `signin.accounts-google.com`.
  * As we can see from image 2 above, there are three `POST` requets made to `40.100.174.34`.
  * Some `POST` requests were made to `signin.office365x24.com`. Their target URL of the web page were sent to `http://signin.office365x24.com/login.php`. 
