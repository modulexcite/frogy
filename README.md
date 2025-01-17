<h1 align="center">
  <a href="https://github.com/iamthefrogy/frogy"><img src="https://user-images.githubusercontent.com/8291014/111029632-a1d13280-83f5-11eb-943a-002f71680d90.png" alt="frogy" height=230px></a>
  </h1>
  
Using the combination of different subdomain enumeration tools and logic this script tries to identify more subdomains and root domains in recon. <br/><br/>
![](https://visitor-badge.glitch.me/badge?page_id=iamthefrogy.frogy)<a href="https://twitter.com/iamthefrogy"> </a>

**Logic**<br/>
<img src="https://user-images.githubusercontent.com/8291014/139606306-6d9618f6-b0bb-43ac-8d48-af64f62d2d9b.jpg" alt="Frogy" title="Frogy" />

+ **Requirements:** Go Language, Python 3.+, jq<br/>
+ **Tools used - You must need to install these tools and place them into /usr/bin folder to use this script**<br/>

  + [SubFinder](https://github.com/projectdiscovery/subfinder)
  + [Find-domain](https://github.com/Findomain/Findomain) (Ensure the binary name is findomain-linux in the /usr/bin folder)
  + [httpx](https://github.com/projectdiscovery/httpx)
  + [anew](https://github.com/tomnomnom/anew)
    
  You might require to install WHOIS and JQ depending upon your enviroment. You can install them using the following commands:
   ```sh
    apt install jq
    apt install whois
    ```
  
+ **Installation**
    ```sh
    git clone https://github.com/iamthefrogy/frogy.git
    cd frogy
    chmod +x frogy.sh
    git clone https://github.com/aboul3la/Sublist3r.git
    git clone https://github.com/rbsec/dnscan.git
    ```
+ **Usage**
    ```sh
    ./frogy.sh
    ```
+ **Output**
    ```
    Output will be saved within output/ORG/ORG.master file. 
    If telsa.com is your target then output file Of all the subdomains will be output/telsa/tesla.master and all the root domains will be recorded in the output/tesla/rootdomains.txtls file.
    ```
    
**TODO**
- ✅  Efficient folder structure management
- Resolving subdomains using Massdns
- ✅  Add dnscan for extened subdomain enum scope
- ✅  Eliminate false positives. Currently around 2% to 4% false positives are there.
- ✅  Bug Fixed, for false positive reporting of domains and subdomains.
- ✅  Searching domains through crt.sh via registered organization name from WHOIS instead of domain name created some garbage data. Filtered result to only grab domains and nothing else.
- ✅  Now finds live websites on all standard/non-standard ports.
- ✅  Now finds all websites with login portals. It also checks websites home page that redirects to login page automatically upon opening.
- Find live subdomains and domains only independent to whether a website was found or not.

#### Thanks to the authors of the tools used in this script.
Initial repo created - A few weeks back below date.<br/>
Date - 4 March 2019, Open-sourced<br/>
Date - 19 March 2021, Major changes<br/>

Warning/Disclaimer: Read the detailed disclaimer at my blog - https://github.com/iamthefrogy/Disclaimer-Warning/blob/main/README.md <br/>
Logo credit - www.designevo.com
