# Ripple Labs - Case Study
<!-- Implementation notes
The following features have been used in this markdown document:
  1. Basic Markdown: # Headings, unordered lists, ordered lists, hyperlinks, text styling (bold, italic etc), backslash escaping of special symbols, images (from this repository and external sources eg YouTube), line breaks, quotes, source comments
  2. Enhanced / Advanced Markdown / HTML (note: some features only work on GitHub User Interface not Visual Studio Code): Footnotes, Accordion (HTML summary/details tags), Mouse-over for defined terms (see aHTML anchor tag), use of HTML entities (eg &nbsp; ), tables
  3. User features: a disclaimer, a table of contents, a glossary of defined terms and acronyms, mouse-over for abbreviations.

Acknowledgement goes to Brian Childress at https://brianchildress.co/variables-in-markdown/ and  John Gruber on https://daringfireball.net/projects/markdown/syntax#link for demonstrating the technique of variables in markdown through use of links. This approach stays more true to pure markdown versus the inital approach that had been taken using HTML anchor tags, eg: '<a href="#glossary-title">Glossary definition</a>', which also meant duplication of the definition text at each reference.

TO DO:
* technology stack include XRPL and its associated stacks
* Last section
* references as per Purdue quotation style
* Table of contents

-->

Author: Bruno Ivasic   
Date: 29 August 2023  

**Disclaimer:** This case study is ***NOT*** intended to provide legal, financial or investment advice of any kind.


## Table of Contents
* [Overview and Origin](#overview-and-origin)
* [Business Activities](#business-activities)
* [Landscape](#landscape)
* [Results](#results)
* [Recommendations](#recommendations)
* [Glossary](#glossary)
* [References](#references)


## Overview and Origin

* *Name of company*   
Ripple Labs Inc. ("Ripple").

* *When was the company incorporated?*   
In short, 2011. The entity was initially incorporated as "NewCoin Inc."[^SoS-NewCoin] on 19 September 2012, then renamed to "OpenCoin Inc."[^SoS-OpenCoin] on 3 October 2012, and finally renamed to "Ripple Labs Inc."[^SoS-Ripple] on 18 October 2013.

* *Who are the founders of the company?*   
Chris Larsen and Jed McCaleb co-founded the company[^tracxn].

* *How did the idea for the company (or project) come about?*   
 Chris attributes the idea for the company's key product, the XRP Ledger, originating in 2004 from the "Ripple Project" initially conceived by Ryan Fuger.

  In early 2011, three developers—David Schwartz, Jed McCaleb, and Arthur Britto—were fascinated with Bitcoin but observed the waste inherent in mining. They sought to create a more sustainable system for sending value (an idea outlined in a May 2011 forum post: [“Bitcoin without mining”](https://bitcointalk.org/index.php?topic=10193.0))[^Bitcoin_Talk].

  [![Video clip placeholder of How Ripple Got Started, featuring Chris Larsen](https://img.youtube.com/vi/3zW_DN9pkbM/0.jpg)](https://www.youtube.com/watch?v=3zW_DN9pkbM)


* *How is the company funded? How much funding have they received?*   
    Ripple has raised a total of $293.8M in funding over 14 rounds between May 2015 to August 2021 from 43 different investors.[^CrunchBase]

## Business Activities:

* *What specific financial problem is the company or project trying to solve?*   
Ripple's crypto and blockchain solutions are designed to "move, manage and tokenize value" predominantly for the following use cases:
   * Cross-Border Payments: Enable global money transfers
   * Crypto Liquidity: Source digital assets
   * Central Bank Digital Currency: Implement <a title="Central Bank Digital Currencies" href="#cbdc">CBDCs</a>

* *Who is the company's intended customer?*   
  Ripple is mainly targeting business customers[^RippleAbout] such as banks and financial institutions, that in turn use Ripple solutions for various types of consumers. Some examples of these include:  
  * [Siam Commercial Bank: Enabling better payouts](https://ripple.com/customer-case-study/scb/)  
  * [Nium: Eliminating prefunding](https://ripple.com/customer-case-study/nium/)
  * [MoneyMatch: Offering lower-cost remittances](https://ripple.com/customer-case-study/moneymatch/)


* *Is there any information about the market size of this set of customers?*   
  In 2021, Ernest &amp; Young[^EYFlows] estimated the total global cross-border payment flow to exceed US$156 trillion by 2022, with a <a title="Compound Annual Growth Rate" href="#cagr">CAGR</a> of 5%, segmented as follows:


    | Segment | Value | Notes |
    | :--- | :---: | :--- |
    |<a title="Business-to-Business" href="#b2b">B2B</a>| US$150t |Transactions make up the largest share by far.|
    |<a title="Consumer-to-Business" href="#c2b">C2B</a>| US$2.8t |Cross-border e-commerce and offline tourism spend.|
    |<a title="Business-to-Consumer" href="#b2c">B2C</a>| US$1.6t |Wage salaries or interest payments.|
    |<a title="Consumer-to-Consumer" href="#c2c">C2C</a>| US$0.8t | Remittance payments.|

    ***Table 1:*** Predicted global cross-border payment flow by segment.[^EYFlows]

    ![Figure 1: Global cross-border payments flows split by use case](./assets/EY-cross-boarder-payment-flows-predicted-growth.jpg)
    ***Figure 1:*** Global cross-border payments flows split by use case[^EYFlows]

* *What solution does this company offer that their competitors do not or cannot offer? (What is the unfair advantage they utilize?)*   
  Ripple aims to disrupt the status quo of cross-border payments. Through the use of blockchain and modern APIs, Ripple enables financial institutions who are part of the network "RippleNet" to send money globally, instantly, reliably and for fractions of a penny. Being part of RippleNet solves three key issues with payments:
  1. Speed and certainty
  1. Liquidity management
  1. Transparency

  With RippleNet, customers can quickly access new markets, expand their services and deliver the best customer experience in global payments today. With a single connection, customers can access the best blockchain technology for global payments, payout capabilities in over 40 currencies, On-Demand Liquidity as an alternative to pre-funding and operational consistency through a common rulebook.[^RippleFAQ]

  
* *Which technologies are they currently using, and how are they implementing them? (This may take a little bit of sleuthing–– you may want to search the company’s engineering blog or use sites like Stackshare to find this information.)*   
  
    [Stackshare](https://stackshare.io/ripple/ripple) users[^StackShare] indicate Ripple adopts  the following technologies:
      <details>
      <summary>Application and Data</summary>
    * [Amazon S3](https://aws.amazon.com/s3/): AWS' Simple Storage Service where data is stored as objects within resources called “buckets”, and a single object can be up to 5 terabytes in size.
    * [Amazon EC2](https://aws.amazon.com/ec2/): AWS' Elastic Compute Cloud which offers (virtual) cloud compute as a service allowing customer like Ripple to rent rather than buy physical computing systems.  
    * [ES6 (Standard ECMA-262 6th Edition)](https://262.ecma-international.org/6.0/): A new version of the Javascript programming language.
    * [HTML5](https://www.w3.org/TR/2011/WD-html5-20110405/): HyperText Markup Language version 5, used for coding web pages.    
    * [Google Drive](https://www.google.com/intl/en_au/drive/): Cloud storage.   
    * [Java](https://www.oracle.com/java/): programming language / development platform.   
    * [JavaScript](https://developer.oracle.com/languages/javascript.html): programming language.   
    * [jQuery](https://jquery.com/): JavaScript library that simplifies HTML document traversal and manipulation, event handling, animation, and Ajax.   
    * [Kafka](https://kafka.apache.org/): open-source distributed event streaming platform.   
    * [NGINX](https://www.nginx.com/): web server that can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache.   
    * [PostgreSQL](https://www.postgresql.org/): open source object-relational database system.   
    * [RabbitMQ](https://www.rabbitmq.com/): open source message broker.   
    * [React](https://react.dev/): open-source front-end JavaScript library for building web and native user interfaces.   
    * [Redis](https://redis.io/): open source, in-memory data store used by  developers as a database, cache, streaming engine, and message broker.    
    * [TypeScript](https://www.typescriptlang.org/): a programming language based on Javascript.    
      </details>

      <details>
      <summary>Utilities</summary>

      * [Google Analytics](https://marketingplatform.google.com/about/analytics/): service offered by Google that tracks and reports website traffic and also the mobile app traffic and events.
      </details>


      <details>
      <summary>Dev Ops</summary>

      * [Babel](https://babeljs.io/): JavaScript compliler.   
      * [Docker](https://www.docker.com/): platform designed to help developers build, share, and run container applications.   
      * [GitHub](https://github.com/): platform and cloud-based service for software development and version control using Git.
      * [Jenkins](https://www.jenkins.io/): open source automation server which helps automate parts of software development related to building, testing, and deploying, facilitating continuous integration and continuous delivery.
      </details>


      <details>
      <summary>Business Tools</summary>

      * [Confluence](https://www.atlassian.com/software/confluence): web-based corporate wiki.   
      * [G Suite (now known as Workspace)](https://workspace.google.com/intl/en_au/): a collection of cloud computing, productivity and collaboration tools, software and products.   
      * [Jira](https://www.atlassian.com/software/jira): issue tracking.
      * [Slack](https://slack.com/intl/en-au) instant messaging.  
      * [WordPress](https://wordpress.com/):  website builder and content management system.
      </details>


  
      <details>
      <summary>In addition, Ripple uses the XRP Ledger, which includes / uses the following technologies[^xrplrefs]:</summary>
      
      * [Python](https://www.python.org/)
      * [Java](https://www.oracle.com/java/): programming language / development platform.   
      * [JavaScript](https://developer.oracle.com/languages/javascript.html): programming language.   
      * [TypeScript](https://learn.microsoft.com/en-us/archive/msdn-magazine/2014/june/typescript-enhance-your-javascript-investment-with-typescript):  superset of the JavaScript programming language. 
      * [C++](https://isocpp.org/std/the-standard): programming language.
      * [Ruby](https://www.ruby-lang.org/en/): programming language.
      * [Tom's Obvious Minimal Language "TOML"](https://toml.io/en/): definition language for configuration files.    
      * [HTTP APIs](https://www.ietf.org/rfc/rfc2616.txt): Hypertext Transfer Protocol (HTTP) is an application-level protocol for distributed, collaborative, hypermedia information systems.   
      * [WebSocket APIs](https://www.rfc-editor.org/rfc/rfc6455): specification for two-way communication between a client running untrusted code in a controlled environment to a remote host that has opted-in to communications from that code. 
      * [Linux](https://www.linux.com/what-is-linux/): Operating System.
      
      </details>


## Landscape:

* *What domain of the financial industry is the company in?*  
  Ripple operates in the payments, crypto currency and blockchain domains.

* *What have been the major trends and innovations of this domain over the last 5-10 years?*  
    In the crypto and blockchain domains, interest has been growing for use of blockchain in applications besides cybercurrency since 2016. The trend continues as new use cases emerge, including voting, real estate, fitness tracking, intellectual rights, the internet of things and vaccine distribution. Multiple cloud providers began offering "blockchain as a service" during the period.[^TechTarget]

    Trends in payments[^RBA2020] over the last 5 to 10 years include:  
    * Faster domestic payments (NPP/Osko/PayID), which has facilitated straight through processing
    * Buy Now Pay Later
    * Mobile device tap and go
    * Crypto currencies
    * Blockchain (e.g. XRP) as digital currencies and expedited payments
    * A decline in cash transactions in favour of digital 

* *What are the other major companies in this domain?*  
   Other blockchain platform companies include[^Gartner]:
   * IBM Blockchain
   * Ethereum
   * Stellar
   * Oracle Blockchain Cloud Service
   * Swirlds
   * Tangle
   * Bitcoin
   * Quorum

  
## Results

* *What has been the business impact of this company so far?*   
  >RippleNet members and their customers — corporations and consumers alike — are increasingly reaping the benefits of instant, on-demand, certain and low-cost payments with Ripple solutions, ultimately sharpening their competitive edges. As more financial institutions join RippleNet, instant payments will reach more destinations and costs will further compress, enabling members to continuously improve their global payments services.[^RipplePR100]


  So far, Ripple's accomplishments include:
  * Ripple has processed nearly $30B worth of volume and 20M transactions since RippleNet was first launched. In 2022, approximately 60% of those payments were sent through <a title="On Demand Liquidity" href="#odl">ODL</a>.[^RippleInsightsQ42022]   
  * Ripple has over 300 business customers which continues to expand.
  * Ripple’s crypto-powered payment solution is available in nearly 40 payout markets, up from just three markets in 2020.  

  Benefits claimed by some of Ripple's customers include:
    * 40% reduction in cross-border payment costs since MoneyMatch joined RippleNet.   
    * US$25M saved by Sentbe customers on foreign exchange conversion and transaction fees.
    * Payments via Modulr in less than 10 seconds.
    * 98% savings on domestic transfer rates for NIUM customers.


  Despite its successes, Ripple has faced some significant legal challenges, which include:   
   * A US$700,000 civil money penalty in 2015, which was the first against a virtual currency for willful violation of several requirements of the Bank Secrecy Act \(BSA\)[^FinCEN]   
   * An action filed in 2022 by the <a title="U.S. Securities and Exchange Commission" href="#sec">SEC</a> charging Ripple and two executives with conducting a $1.3b unregistered securities offering.[^SECPR]  Although a landmark ruling in favor of Ripple was made in July 2023[^Torres]<sup>, </sup>[^HKLaw-1] for three of the four transaction types at issue, the <a title="[U.S. Securities and Exchange Commission" href="#sec">SEC</a> plans to appeal the court's ruling .[^Reuters]


* *What are some of the core metrics that companies in this domain use to measure success? How is your company performing, based on these metrics?*    

  Typical metrics include:
  * Processing throughput (in transactions per second),
  * Cost of processing
  * End to end Processing speed
  * Energy consumption
  * Buy / sell volume on exchanges
  * Price of the token


* *How is your company performing relative to competitors in the same domain?*   

  A comparison of Ripple's XRP against prominent cryptocurrencies is presented in Table 2 below, which highlights the extent of XRP's performance advantage.

  | Cryptocurrency / Blockchain | Bitcoin / Bitcoin | Ether / Ethereum&nbsp;1.0 |	XRP / XRP&nbsp;Ledger|
  |:---| :---| :--- | :--- |
  |Key Use  | Store of Value   |Smart Contracts  |  Payments |
  |Speed to Transact (seconds) | 409.98  | 300.00 |  3.83 |
  |Cost per Transaction (US$)  | $0.465 | $9.00 | $0.0002 |
  |Transactions Per Second | 5 | 10 | 1,500[^RippleCryptoIntro] - 3,400[^RippleXrp]|

  ***Table 2:*** Comparison of Prominent Cryptocurrencies [^RippleCryptoIntro]<sup>, </sup> [^RippleXrp]
  
  Further, Kohli et al[^Kohli-2023] suggest XRP is significantly more energy efficient than other major cryptocurrencies by an order of up to 100,000 times more efficient compared to BitCoin, although there are other cryptocurrencies, such as Hedera, which are even more efficient than XRP.

		
   ![Figure 2: Energy consumption per transaction for various cryptocurrencies (and their consensus mechanisms)](./assets/crypto-energy-consumption.jpg)   
   ***Figure 2:*** Energy consumption per transaction for various cryptocurrencies (and their consensus mechanisms). Source: Kohli et al (2023)[^Kohli-2023]



## Recommendations

* *If you were to advise the company, what products or services would you suggest they offer? (This could be something that a competitor offers, or use your imagination!)*   

  
  Some of the negative comments posted on [Gartner Peer Insights](https://www.gartner.com/reviews/market/blockchain-platforms/vendor/ripple/product/ripple) about Ripple's blockchain product suggest it doesn't really support [smart contracts][def-smart-contract] like other blockchain solutions.[^gpr-726158]<sup>, </sup>[^gpr-842917]  
  
  Upon further investigation using a search within [Ripple's website](https://www.ripple.com) for the term "smart contract" returned no results. A separate [Google Search restricted to the Ripple website](https://www.google.com/search?q=%22smart+contract%22+site%3Aripple.com) returned about 250 results, which of interest included:
  1. "Use an Escrow as a Smart Contract"[^xrplsc]; and
  1. "XRPL Hooks - Smart Contract proposal for the XRP Ledger"[^xrpl-hooks]
  
    Recently, coincidently, a whitepaper for the Xahau Ledger titled ["The Smart Contract Sidechain for the XRPL Ecosystem"](https://github.com/Xahau/Whitepaper/blob/main/Xahau-Whitepaper.pdf) was released.

  Reddit user "lj23ft" states[^reddit]:
  > *"There are several businesses that have been waiting for these features and instead of waiting for Ripple they built a sidechain so they could get these features sooner."*

  
* Why do you think that offering this product or service would benefit the company?

  [Zion Market Research](https://www.zionmarketresearch.com/report/smart-contracts-market) suggests:   
  > *in terms of revenue, the global smart contracts market size was valued at around USD 1750 million in 2022 and is projected to reach ***USD 9850 million***, by 2030*[^zion-sc]

  Although Ripple is mentioned as a technology, its statistics are not, perhaps implying it is not a dominant player due to their current technology. XLR Ledger is not mentioned as a platform either.


* What technologies would this additional product or service utilize?

  The service would use [XRPL Hooks](https://xrpl-hooks.readme.io/docs).

* *Why are these technologies appropriate for your solution?*   
Developed for the XRP Ledger, [hooks][def-hooks] work "on-chain" as opposed to other solutions which work "off-chain" or "side-chain", and depending on one's view, either the advantage or risk that "hooks have the ability to control, with atomicity and finality, the logical flow and execution of transactions on the accounts to which the hooks are configured".[^wietse-h2]

---


## Glossary

### B2B
[def-b2b]: #b2b "Business to Business."

Business to Business.

---

### B2C
[def-b2c]: #b2c "Business to Consumer."

Business to Consumer.

---

### C2B
Consumer to Business.

---

### C2C
Consumer to Consumer.

---

### CAGR
Compound Annual Growth Rate.

---

### CBDC
Central Bank Digital Currency.

---
### Hooks
[def-hooks]: #hooks "Small efficient web assembly modules that run on the XRP Ledger at Layer 1 (on-chain). This is distinct from Codius, Hot Pocket, Flare and other Layer 2 solutions (which are off-chain or side-chain)."

Small efficient web assembly modules that run on the XRP Ledger at Layer 1 (on-chain). This is distinct from Codius, Hot Pocket, Flare and other Layer 2 solutions (which are off-chain or side-chain).[^wietse-h2]

---

### ODL
On Demand Liquidity.

---

### SEC
Securities and Exchange Commission.

---

### Sidechain
[def-sidechain]: #sidechain "A separate, independent blockchain linked to the main blockchain (mainchain) using a two-way bridge. It enables tokens or other digital assets to be transferred between the mainchain and the sidechain."
A separate, independent blockchain linked to the main blockchain (mainchain) using a two-way bridge. It enables tokens or other digital assets to be transferred between the mainchain and the sidechain.[^cryptocom]

---

### Smart Contract
[def-smart-contract]: #smart-contract "A blockchain-based program that encodes the conditions and fulfillment of an agreement between two or more parties and automatically fulfills the terms of the agreement once conditions are met."
A blockchain-based program that encodes the conditions and fulfillment of an agreement between two or more parties and automatically fulfills the terms of the agreement once conditions are met.[^xrplsc]


---

### XRP
XRP is the cryptocurrency that is native to the XRP Ledger (<a title="The XRP Ledger is an open-source, public, decentralized blockchain" href="#xrpl">XRPL</a>).[^investopedia-xrp]

---

### XRPL
The <a title="XRP is the cryptocurrency that is native to the XRP Ledger" href="#xrp">XRP</a> Ledger is an open-source, public, decentralized blockchain.

---

## References
[^RippleAbout]: [Ripple Labs Inc. (2021) "Intro to Ripple Fact Sheet"](https://ripple.com/files/Intro-to-Ripple-Fact-Sheet.pdf)

[^RippleCryptoIntro]: [Ripple Labs Inc. (2021) "An introduction to Cryptocurrency"](https://ripple.com/files/Intro-to-Crypto-Fact-Sheet.pdf)

[^RippleFAQ]: [Ripple Labs Inc. Frequently Asked Questions](https://ripple.com/faq/)

[^RippleInsightsQ42022]: [Ripple Labs Inc. (30/1/2023) "Q4 2022 XRP Markets Report"](https://ripple.com/insights/q4-2022-xrp-markets-report/)


[^RipplePR100]: [Ripple Labs Inc. "Ripple’s Blockchain Network Is Now More Than 100 Strong"](10/10/2017)(https://ripple.com/ripple-press/ripples-blockchain-network-now-100-strong/)


[^RippleXrp]:[Ripple Labs Inc. "XRP Overview"](https://ripple.com/xrp/)

[^CrunchBase]: [Crunchbase Inc. - Ripple Financials](https://www.crunchbase.com/organization/ripple-labs/company_financials)


[^Bitcoin_Talk]: [“Bitcoin without mining”](https://bitcointalk.org/index.php?topic=10193.0)

[^EYFlows]: [Ernst &amp; Young Global Ltd. (2021) "How new entrants are redefining cross-border payments"](https://www.ey.com/en_au/banking-capital-markets/how-new-entrants-are-redefining-cross-border-payments)

[^FinCEN]: [U.S. Financial Crimes Enforcement Network (05/05/2015) "FinCEN Fines Ripple Labs Inc. in First Civil Enforcement Action Against a Virtual Currency Exchanger" ](https://www.fincen.gov/news/news-releases/fincen-fines-ripple-labs-inc-first-civil-enforcement-action-against-virtual)

[^SECPR]: [Securities Exchange Commission, (22/12/2020) "SEC Charges Ripple and Two Executives with Conducting $1.3 Billion Unregistered Securities Offering"](https://www.sec.gov/news/press-release/2020-338)

[^HKLaw-1]: [Mascianica S., Magee J., McCarron Turner J. (20/07/2023) "SEC v. Ripple: When a Security Is Not a Security - Summary Judgment Battle Results in Split Decision, Blow to SEC Enforcement"](https://www.hklaw.com/en/insights/publications/2023/07/sec-v-ripple-when-a-security-is-not-a-security) 

[^Torres]: [Torres A., United States District Court Southern District Of New York (13/07/2023) "Order on Case 1:20-cv-10832-AT-SN (SEC vs Ripple Labs et al) Document 874"](https://www.nysd.uscourts.gov/sites/default/files/2023-07/SEC%20vs%20Ripple%207-13-23.pdf)

[^Reuters]: [Stempel J., Reuters (12/08/2023) "US SEC seeks to appeal Ripple Labs crypto decision" ](https://www.reuters.com/legal/us-sec-appeal-ripple-labs-court-ruling-2023-08-09/)

[^SoS-NewCoin]: [Californian Secretary of State (19/09/2023) Articles of Incorporation #3505635 NewCoin Inc](https://bizfileonline.sos.ca.gov/api/report/GetImageByNum/187089170177186059061179244045225015102149150023)

[^SoS-OpenCoin]: [Californian Secretary of State (3/10/2023) Certificate of Amendment #A0732979 Renamed to OpenCoin Inc](https://bizfileonline.sos.ca.gov/api/report/GetImageByNum/116067222226235006001172039135168044050121032046)

[^SoS-Ripple]: [Californian Secretary of State (18/10/2023) Certificate of Amendment #A0747403 Renamed to Ripple Inc](https://bizfileonline.sos.ca.gov/api/report/GetImageByNum/076031074160242065134127075129213240171193013106)

[^tracxn]: [Tracxn \(n.d.\) Ripple Founders](https://tracxn.com/d/companies/ripple/__RI5NqNB2xmmrUkf5iftdStz97omfcqLLEWHh-AydmF8/founders-and-board-of-directors)

[^Kohli-2023]: [Kohli V. et al, (2023) "An analysis of energy consumption and carbon footprints of cryptocurrencies and possible solutions", Digital Communications and Networks, doi: 10.1016/j.dcan.2022.06.017](https://doi.org/10.1016/j.dcan.2022.06.017)

[^Stackshare]: [Ripple profile on stackshare.io (26/08/2023](https://stackshare.io/ripple/ripple)

[^RBA2020]: [Reserve Bank of Australia (2020) "Payments System Board Annual Report – 2020 Trends in Payments, Clearing and Settlement Systems"](https://www.rba.gov.au/publications/annual-reports/psb/2020/trends-in-payments-clearing-and-settlement-systems.html)

[^TechTarget]: [Sheldon R. "A timeline and history of blockchain technology" (9/09/2021)](https://www.techtarget.com/whatis/feature/A-timeline-and-history-of-blockchain-technology)

[^Gartner]: [Gartner "Ripple Alternatives" (2023)](https://www.gartner.com/reviews/market/blockchain-platforms/vendor/ripple/product/ripple/alternatives)

[^xrplrefs]: [XRP Ledger References and APIs](https://xrpl.org/references.html)

[^xrplsc]: [XRP Ledger Use an Escrow as a Smart Contract](https://xrpl.org/use-an-escrow-as-a-smart-contract.html)

[^xrpl-hooks]: ["XRPL Hooks - Smart Contract proposal for the XRP Ledger"](https://xrpl-hooks.readme.io/)

[^gpr-726158]: [Gartner Peer Review Forum, Anonymous, (20/01/2020)](https://www.gartner.com/reviews/market/blockchain-platforms/vendor/ripple/product/ripple/review/view/726158)



[^gpr-842917]: [Gartner Peer Review Forum, Anonymous, (24/04/2019)](https://www.gartner.com/reviews/market/blockchain-platforms/vendor/ripple/product/ripple/review/view/842917)


[^cryptocom]: [Crypto.com, "What Are Sidechains? Scaling Blockchain on the Side", (4/02/2021)](https://crypto.com/university/what-are-sidechains-scaling-blockchain#:~:text=A%20sidechain%20is%20a%20separate,the%20mainchain%20and%20the%20sidechain)

[^investopedia-xrp]: [Investopedia, "What is XRP?" (1/08/2021)](https://www.investopedia.com/what-is-xrp-6362550)

[^xrpl-xahau]: [XRP Ledger Foundation, "Hello Xahau" (28/08/2023)](https://foundation.xrpl.org/2023/08/28/hello-xahau/)


[^reddit]:[lj26ft, Reddit, "What does Xahau mean for XRP?", (29/08/2023)](https://www.reddit.com/r/XRP/comments/1648zh0/what_does_xahau_mean_for_xrp/jy7ljp9/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button)
<!-- Blog -->

[^zion-sc]: [Zion Market Research, "Global Smart Contracts Market to grow around USD 9850 million by 2030", (3/03/2023)](https://www.zionmarketresearch.com/news/global-smart-contracts-market)

[^wietse-h2]: [Wind W., DEV, "Hooked #2: Hooks & Security (Smart Contracts on the XRP ledger)", (14/11/2020)](https://dev.to/wietse/hooked-2-hooks-security-smart-contracts-on-the-xrp-ledger-83e)
