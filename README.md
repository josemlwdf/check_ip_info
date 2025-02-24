# Whois IP Lookup Script

This Python script performs WHOIS lookups for a list of IP addresses and displays relevant information such as the organization name, country, and a link to check the IP on external platforms (AbuseIPDB and VirusTotal). It also supports whitelisting organizations like Google, Amazon, and others, with the ability to mark their organizations with a special color.

## Features
- **WHOIS Lookup**: Retrieves WHOIS data for IP addresses.
- **Whitelist Organizations**: Displays specific organizations (e.g., Google, Amazon) in a special color.
- **Country Mapping**: Converts country codes into full country names.
- **Check IP**: Provides links to external platforms like [AbuseIPDB](https://abuseipdb.com) and [VirusTotal](https://virustotal.com) for each IP.

## Requirements
- Python 3.x
- `tabulate` library (for pretty table output)
- `whois` command-line tool installed

You can install the required Python package by running:

    pip install tabulate
    
## How to Use

``Prepare a file with a list of IP addresses. Each IP address should be on a new line (e.g., ip_list.txt).``

Run the script with the path to your wordlist file as an argument:
    
    ./get_ip_info ip_list.txt

View the results: The script will display the following information for each IP in the list:

`` IP: The IP address``
``Organization: The organization associated with the IP (if available)``
``Country: The country associated with the IP (if available)``
``Check IP: Links to external platforms (AbuseIPDB and VirusTotal) for further investigation``

##Example Output:
![image](https://github.com/user-attachments/assets/62bf381c-ec27-4c94-8987-74efb3528a32)

## How It Works
``The script uses the system's whois command to fetch WHOIS information for each IP.
It identifies the organization and country from the WHOIS data and checks against a list of whitelisted organizations. If the organization is whitelisted (like Google or Amazon), the organization name is highlighted in a soft yellow color.
The country code (e.g., "US" for United States) is mapped to a country name using a dictionary.``

## Whitelisted Organizations

This script includes the following organizations by default:

    Google
    Amazon
    Microsoft
    Facebook
    Apple
    Cloudflare
    GitHub
    GitLab
    Akamai

Feel free to add or remove organizations by editing the whitelisted list in the script.

## License

This script is open source and available under the MIT License.

For more information about the WHOIS command, visit: https://en.wikipedia.org/wiki/Whois

For external platforms:
    AbuseIPDB: https://www.abuseipdb.com/
    VirusTotal: https://www.virustotal.com/

