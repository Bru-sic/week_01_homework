# Ripple Labs - Case Study

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

  
  Table 2 provides a further comparison of XRP's technology with other prominent cryptocurrencies, highlighting that XRP has been designed with payments, speed, throughput and efficiency in mind. 

  | Cryptocurrency / Blockchain | Bitcoin / Bitcoin | Ether / Ethereum |	XRP / XRP&nbsp;Ledger|
  |:---| :---| :--- | :--- |
  |Key Use  | Store of Value   |Smart Contracts  |  Payments |
  |Speed to Transact (seconds) | 409.98  | 300.00 |  3.83 |
  |Cost per Transaction (US$)  | $0.465 | $9.00 | $0.0002 |
  |Transactions Per Second | 5 | 10 | 1,500 (max)|

  ***Table 2:*** Approximative Comparison of Different Cryptocurrencies[^RippleCryptoIntro]
  
  Kohli et al[^Kohli-2023] suggest XRP is significantly more energy efficient than other major cryptocurrencies - in the case of BitCoin, up to 100,000 times more efficient, although there are other cryptocurrencies such as Hedera which are even more efficient than XRP.

		
   ![Figure 2: Energy consumption per transaction for various cryptocurrencies (and their consensus mechanisms)](./assets/crypto-energy-consumption.jpg)   
   ***Figure 2:*** Energy consumption per transaction for various cryptocurrencies (and their consensus mechanisms). Source: Kohli et al (2023)[^Kohli-2023]


* *Which technologies are they currently using, and how are they implementing them? (This may take a little bit of sleuthing–– you may want to search the company’s engineering blog or use sites like Stackshare to find this information.)*
  
  [Stackshare](https://stackshare.io/ripple/ripple)[^StackShare] indicates Ripple uses the following technologies:

  <details open>
    <summary>Application and Data</summary>

    * [Amazon S3](https://aws.amazon.com/s3/): AWS' Simple Storage Service where data is stored as objects within resources called “buckets”, and a single object can be up to 5 terabytes in size.
    * [Amazon EC2](https://aws.amazon.com/ec2/): AWS' Elastic Compute Cloud which offers (virtual) cloud compute as a service allowing customer like Ripple to rent rather than buy physical computing systems.  
    * [ES6 (Standard ECMA-262 6th Edition)](https://262.ecma-international.org/6.0/): A new version of the Javascript programming language.
    * [HTML5](https://www.w3.org/TR/2011/WD-html5-20110405/): HyperText Markup Language version 5, used for coding web pages.    
    * Google Drive   
    * Java: programming language.   
    * JavaScript: programming language.   
    * [jQuery](https://jquery.com/): JavaScript library that simplifies   HTML document traversal and manipulation, event handling, animation, and Ajax.   
    * [Kafka](https://kafka.apache.org/): open-source distributed event streaming platform   
    * [NGINX](https://www.nginx.com/): web server that can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache.   
    * [PostgreSQL](https://www.postgresql.org/): open source object-relational database system.   
    * [RabbitMQ](https://www.rabbitmq.com/): open source message broker.   
    * [React](https://react.dev/): open-source front-end JavaScript library for building web and native user interfaces.   
    * [Redis](https://redis.io/): open source, in-memory data store used by  developers as a database, cache, streaming engine, and message broker.    
    * [TypeScript](https://www.typescriptlang.org/): a programming language based on Javascript.    
  </details>

    <details open>
    <summary>Utilities</summary>

    * [Google Analytics](https://marketingplatform.google.com/about/analytics/): service offered by Google that tracks and reports website traffic and also the mobile app traffic &amp; events.   
    </details>


    <details open>
    <summary>Utilities</summary>

    * [Babel](https://babeljs.io/): JavaScript compliler.   
    * [Docker](https://www.docker.com/): a platform designed to help developers build, share, and run container applications.   
    * [GitHub](https://github.com/): a platform and cloud-based service for software development and version control using Git.
    * [Jenkins](https://www.jenkins.io/): open source automation server which helps automate parts of software development related to building, testing, and deploying, facilitating continuous integration and continuous delivery.
    </details>


    <details open>
    <summary>Utilities</summary>

    * [Confluence](https://www.atlassian.com/software/confluence): web-based corporate wiki.   
    * [G Suite (now known as Workspace)](https://workspace.google.com/intl/en_au/): a collection of cloud computing, productivity and collaboration tools, software and products.   
    * [Jira](https://www.atlassian.com/software/jira): issue tracking.
    * [Slack](https://slack.com/intl/en-au) instant messaging.  
    * [WordPress](https://wordpress.com/):  website builder and content management system.
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
   * An action filed in 2022 by the <a title="U.S. Securities and Exchange Commission" href="#sec">SEC</a> charging Ripple and two executives with conducting a $1.3b unregistered securities offering.[^SECPR]  Although a landmark ruling in favor of Ripple was made in July 2023[^Torres]<sup>,</sup>[^HKLaw-1] for three of the four transaction types at issue, the <a title="U.S. Securities and Exchange Commission" href="#sec">SEC</a> plans to appeal the court's ruling .[^Reuters]


* *What are some of the core metrics that companies in this domain use to measure success? How is your company performing, based on these metrics?*    

<p style="color:red; font-size:40px">---HERE BRU---</p>

Uptime 99.99%


* *How is your company performing relative to competitors in the same domain?*   



## Recommendations

* If you were to advise the company, what products or services would you suggest they offer? (This could be something that a competitor offers, or use your imagination!)

* Why do you think that offering this product or service would benefit the company?

* What technologies would this additional product or service utilize?

* Why are these technologies appropriate for your solution?


# Appendix

## Glossary

### B2B
Business to Business.

---

### B2C
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

### ODL
On Demand Liquidity.

---

### SEC
Securities and Exchange Commission.

---

### XRP
XRP is the cryptocurrency that is native to the XRP Ledger (<a title="The XRP Ledger is an open-source, public, decentralized blockchain" href="#xrpl">XRPL</a>).

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
