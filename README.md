# information-security-h1
Second homework task for Information Security ICI002AS2AE-3007

# Table of contents
1. [Threat modeling](#threat-modeling---summaries)  
    1.1 [Braiterman](#braiterman)  
    1.2 [Shostack](#shostack)  
    1.3 [OWASP](#owasp)  
2. [Infosec Scene](#infosec-scene)  
    2.1 [Summary](#small-summary)  
    2.2 [Description](#summary-per-topic)
3. [Security Hygiene](#security-hygiene)
4. [Make-belief boogie-man](#make-belief-boogie-man)
5. [References](#references)

# Threat Modeling - summaries
## Braiterman
- Threat modeling highlights security and privacy concerns of a system  
-> recognize what can go wrong and allows you to pinpoint design and implementation issues  
-> output = threats
- 4 questions: 
  - What are we working on?
  - What can go wrong?
  - What are we going to do about it?
  - Did we do a good enough job?
- Values & principles
  - values: importance of something *over* something else
  - principle: fundamental thruths of threat modeling
    - fundamental, general thruths (succesful threat modeling)
      - e.g. best use is to improve security & privacy through frequent analysis
    - recommended patterns
      - e.g. systemic approach
    - anti-patterns (don't do this)
      - e.g. think you alone can do it

## Shostack
- Why Threat model? 
  - Think about security before it becomes expensive
  - Make application as secure as possible
- Four questions
  - What are we doing?
  - What can go wrong?
  - What can we do about it?
  - Is it enough?
- Collaboration
  - Multiple views on one concept is good
- Sketching
  - Translate thoughts to other people and refine them
- Keeping records
  - Business reasons for proof of security
- Data Flow Diagrams (DFD3)
  - External entities: Sharp corners (no control)
  - Processes: round corners (your control)
  - Data flows: connect external entities to processes
  - Data stores: drums
  - Trust boundary: different elements are operated by different entities (different trust)
- What can go wrong?
  - Keep consistency by going over these treats:  
    -> STRIDE
      - Spoofing
      - Tampering
      - Repudiation
      - Information Disclosure
      - DoS (Denial of Service)
      - Elevation of Privileges
- What can we do about it?
  - Track the work/problems and do something about it
    - Risk management
      - Quantify impact of problems
    - Fix it
- Did we do a good job in threat modeling?
  - Would you recommend threat modeling to a colleague?  
  => If no, you haven't done a good enough job.

  ## OWASP 
    ### Intro
    Threat modeling is structured and repeatable. It gives insights in security of a system. 
    - Best performed during design fase
    - Best integrated in development proces, not an add-on

    ###  Benefits of threat modeling:
    - Identify risks early (efficient)
    - Increase awareness (think creatively and critically)
    - Improved visibility of Target of Evalution
    - Everyone understands the system better
    
    ###  Address each question:  
    No standard for threat modeling process, but most approaches include the following:
    - System Modeling (what are we building )
        - with Data Flow Diagram (DFD)
    - Threat identification (what can go wrong)
        - STRIDE
        - ranking threats based on likelihood and impact
    - Risk response (what can we do about it?)
        - mitigate (reduce chance of threat)
        - must be documented
        - eliminate (remove feature causing threat)
        - transfer (shift responsibility)
        - accept (neither of the above given business requirements/constraints)
    - Review & validation (Did we do a good enough job)
        - threat model must be reviewed by all stakeholders
        - includes, but not limited to:
        - is DFD accurate?
        - have all threats been identified, discussed and documented?
        - can mitigations be tested?

    ### Difficulties
    - Most devs don't know vulnerabilities
    - Threat modeling can be **complex and time-consuming**
    - Communication and collaboration between departments

    ### How to solve difficulties?
    - Invite specialists (members of security team)
    - Company can invest in IT security training for dev teams
    - Promote importance of security

# Infosec scene
[Episode 132: Sam the Vendor - A Darknet Market Vendor](https://darknetdiaries.com/episode/132/)

## Small summary

Sam, a libertarian (supporter of absolute freedom) got into drugs as a teen and later became a seller on the darknet. He built trust in the community by calling out scammers and after some time, started selling weed and moonshine. He took very strong security measures (Tails Linux, PGP keys, no phones, rotating post offices, USPS shipments, gloves, fake return addresses) and eventually involved his cousin to help ship packages.

Even though revenue was growing (and his cousin got paid by the percentage), she broke security protocols which led to federal suspicion. The cops illegally opened on of the packages to get a warrant but still lacked real evidence. Sam hoped something like this would invalidate his case, but his cousin testified against him to reduce her own sentence. In the end, he took a plea deal and was sentenced to five years. 

Just before going to prison, he got married. He was in prison for 18 months, after which he got released for compasssionate release and later earned a law degree. Currently, he helps other people fight legal battles.


If you want to read a more detailed description of the episode, please read the summary below. If not, go to the [next topic](#security-hygiene)

## Description
  
  Silk Road = Online, anonymous market for illegal drugs  

  Sam got in jail as a teen, fell into a drug habit and started selling cocaine.  
  
  After break-up with girlfriend of 10 years, he educated himself on darknet marketplaces and made a name with calling out scammers on there.  
    
  After the marketplace got posting restrictions, he had to become either a buyer or a vendor. Another vendor gave him the bitcoin for buying a stolen credit card so he could keep on posting but didn't jump right into it.
    
  He made friends and connections without even buying or selling and noticed the following:  
  1. Everyone tried to be as anonymous as possible
  2. Assume everyone is a criminal or federal agent
  3. The feds are trying to catch the criminals. Their misteps became Sam's guidance.  
    
  It started with selling weed and moonshine and he had a lot of connections already. After doing some business, he wanted to cut down on business costs (e.g. shipping supplies). This also anonymized him further (no credit card purchase).  
    
  He never used his home internet connection to do illegal things and also used Tails Linux. It resets each time when you reboot. Even though it resetted, he needed his PGP and bitcoin key to authenticate himself. Those keys prove that he was a vendor though, so he kept a flash drive on himself at all times.  
    
  He lived on a hill so could see everything coming at his house, so did a regular surveillance tour. He didn't have a cellphone and no cellphones got in his house. 
  
  He used only USPS, because they require a warant to open packages. They need reasonable suspicion and cause to do this. Sam wanted to know what they classified as too suspicious. 
  
  It became a big operation so he needed help, so he asked his cousin. She got very well compensated and could get all drugs she'd want. She would handle posting the packages.  
    
  Her cousin was worried that her fingerprints were on the box, which was not really a problem (plaussible deniability, e.g. touch a box in a post office). Sam did have to wear gloves, to make sure the *inside* of the package didn't have any fingerprints.  
    
  Vacuum-seal the drugs and make a vissual barrier. With the label, he'd print that it was organic, dried fruit as the package feels the same. A dog could smell through the package if it stayed out long enough, yet this wasn't a problem. 
  
  Each package would have a different return address, but it couldn't be an invalid one. It also couldn't be a random return address because he didn't want to subject good people to this. Instead, he used the addresses of sex offenders if they *would* get raided. 
  
  He had one big rule for the cousin:  
  - Each post office could have max three packages going out so he could rotate the post offices and also not visit them for six months. 
    
  He only sold 'party' drugs, drugs that wouldn't ruin people's lives, so he considered himself not a big target. 

  Sam believes that people should have the right to do with their body as they want, including drugs. This is a typical way of thinking for libertarians.

  The maker of Silk Road was also a libertarian. He didn't want any nefarious things on the market place though - nothing that could hurt other people (guns, child porn etc.)

  It's strange that even though they are criminals, they follow 'unnecessary' ethical rules. Sam was actually proud of his product, and wanted to provide his clients the best product he could. 
  
  His goal was to make about 200k, to buy a house and live off of it for some time. While this goal continued on, he invested most of it back in the business. Towards the end, the money started to come in exponentially. Even though he had quite some revenue at some point, bitcoin dropped often, which means he had to hold for some time.

  His famous words were "Don't drink and **type**". When they were chatting, the anonimosity dissapeared sometimes, where he got to know people's names. 

  He could whitewash the bitcoin by buying the drugs online and selling it to people he knew in real life. He sold it for about half the price of the 'street price'. 

  He started working for a darknet company that gives refunds. Additionally, he got an offer for some PR for another darknet marketplace. On reddit, he saw a post for that marketplace for a specific bug on the website, leaking IP addresses. He tried to calm the user by gaslighting him. He got to know that user and started chatting often with him. 

  They moved the darknet subreddit to the darknet itself (reddit banned people trying to **sell** products), so the user started developing it. After some time, reddit shut down the subreddit so a lot of people migrated to the new site.  

  He woke up some day and opened the door to a federal agent with a warrant, with lots of other people with guns behind them. He notified the agent that there were kids and two women living there, just to not alarm anyone. 

  Some time before, his cousin asked him what they'd do if they raided them, to which he answered that he would've fucked up, as he did most of the work. 

  He was completely honest when the agent asked if there were any drugs in the house, to which he calmly replied "They're in a safe; I'm a darknet drug dealer". The cops were not prepared for this, but he got an indictment that they were going to arrest him. After that, he moved to an appartment, so when the cops were coming to get him, he wasn't there. His ex, who he still lived with, told them the address, but Sam was already on his way to turn himself in. 

  The cops had some questions. They mostly asked him informative questions, how he could get to know so much about the darknet in such a short time, to which he replied that he just made himself useful to the community. They offered him a job to just get more information - not sell any drugs - but he declined, seeing as how he worked with multiple cartels.  

  Sam's cousin introduced him to a new woman, with whom he only chatted online - never with face. When he got raided, he lost her number. He was again completely honest when she asked him why he hadn't responded in four days. She obviously didn't believe it at first, but did sometime after. They only knew each other mentally, yet after the raid they sent each other selfies - who was going to raid him now? 

  He was honest in that he'd go into prison, and told her to forget him. She still didn't go away, since she loved him too. They moved in together, while they waited for his court date. 

  He was still very curious how the feds got him. Going through the evidence, he found "Operation Dark Gold". It as a guy that exchanged bitcoin for cash in the mail. Gold got arrested though, and worked for the feds. Sam fighted this, because transferring bitcoin to cash is not illegal at all. If he could prove that the feds were inventing ways to get a warrant, the case might get thrown out.

  At one point, his cousin was coming in with multiple packages with different return addresses - which is suspicious, but is not a probable cause for a warant. What the cops did, was cut open a package illegally, find cocaine and get the warrant. The cops followed the cousin home, after which they got a warrant. 

  Sam was angry at his cousin for quite some time, seeing as how she didn't follow the security protocols, which could end up costing him years and years in prison. He realised after some time, that he was still at fault - he should have supervised her better. 

  The feds bought drugs off of him 20 times, yet they couldn't prove a thing. 

  One of his back-up plans was that if he would get caught, he'd admit everything because he *knew* that to get him, they would have to break the law. If evidence is illegally obtained, the whole case must be thrown out. And if all the evidence is gone, then there can be no case. His lawyer did fight them on this to get a 'Frank's hearing'. 

  The lawyer of the opposition told Sam's lawyer they didn't want to go to that hearing, and offered the following: If he'd admit he was guilty, he would only get 9 years in prison. Otherwise, all other charges *would* be dropped, except for the conspirancy charge. Sam didn't know about this, so went to look at the documents. 

  His cousin told the cops "she didn't know what was in the packages" and told them everything about Sam, even though she was in on the whole operation to get a reduced sentence (or not any in his case). Why she changed the plan was not clear, yet this meant that Sam would still get convicted even if all the other charges would be thrown out. 

  Because of this, Sam decided to take the plea deal. During the sentencing, the judge sentenced him to five years in prison. He got married during this time and his wife visited him a lot during the prison, giving him hope. 

  In prison, he decided to educate himself on the law. He applied for compassionate release, which he was granted. After just 18 months, he was released. 

  Sam got his degree in law and now helps other people fight the law. 


  # Security Hygiene
  What basic security practices should everyone follow?
  - Check the sender of the email. 
  - Don't open any links if you don't have to. 
  - If you do have to open links, thoroughly check the urls.
  - Never put in usb-sticks that you don't know the origin of. 
  - Always lock your computer when you go away. 
  - Use a password manager, or at least use different passwords for different purposes.
  - It's always better to double check with someone in person if they ask sensitive information through a digital channel. (e.g. IT asks for your password)

  # Make-belief boogie-man
  ## What are we working on?
  ### Company
  TechStore, an online webshop selling consumer electronics (computer components, laptops, etc.).  
  Customers can browse products on the website. To order, they should be logged in. Orders are then processed through an e-commerce back-end. The products are then shipped from a warehouse. 

  ### Key assets
  - Customer data (names, addresses, emails, passwords, payment details)
  - Webshop (website, shopping cart, products)
  - Payment gateways (credit card, PayPal, ...)
  - Order database
  - Warehouse management system
  - Employee data & admin dashboard (manage products, orders, refunds)
  - Reputation

  ## Customer interactions
  - Customer interacts with webshop to browse and purchase products, and to interact with support.
  - Payment page
  - Order confirmation & shipping (email)

  ### Crown jewels
  - Secure payment and customer data
  - Website uptime
  - Order database **integrity** (nothing can be tampered with)
  - Employee dashboard (controls most of the operations)

  ### Sketch
  <img src=./images/ThreatModel.drawio.png>

  ## What can go wrong?
  ### STRIDE
  - **S**poofing
    - Employee account can be hijacked
    - Customer account can be hijacked
  - **T**ampering
    - Product catalog can be changed
    - Products can be given a discount when it's not the intention
    - Orders can be created when they haven't paid
    - Orders from customers can be removed
    - Customer data can be stolen
    - Customer passwords can be stolen
    - Employee data can be stolen
    - Employee passwords can be stolen
  - **R**epudiation
    - There's no proof which employee changed what
  - **D**oS
    - The website is inaccessible due to an attack
    - Payment processors are not working
  - **E**levation of Priveleges
    - Customer can access employee dashboard
  
  ### Biggest risks
  - Leaking customer and employee data/passwords
  - Employees accounts get compromised
  - Order database gets corrupted
  - Webshop is not working

  ### Specific threat actors
  This area is not high risk. The only reason to hack this company is because of monetary reasons.

  ## What are we going to do about it?
  1. Regular training for employees **mitigates** risk of loss of account.
  2. Databases can't be accessed directly and every change is logged. This **transfers** responsibility to the employee changing orders or products. 
  3. Employees can only access the customers account they are currently working on, which **mitigates** the risk of all customer data being leaked. 
  4. HR will be moved to a seperate application to **eliminate** the risk of employee's data being leaked through our application.
  5. We keep backups of the databases to **mitigate** the risk of all data being lost or corrupted.
  6. Customers are solely responsible for the protection of their account. This **transfers** the responsibility to the customer.
  7. Databases are seperated to **mitigate** the risk of all data being leaked at once. We **accept** that the data might get leaked at some point, but will **mitigate** the consequences.

  ## Did we do a good enough job?
  Cybersecurity gets a dedicated budget to make sure all operations are as secure as they can be. Security audits will be held regularly. All employees get trained.
  



# References
- Conklin, L. (2022). *Threat Modeling Process | OWASP*. Owasp.org. https://owasp.org/www-community/Threat_Modeling_Process

- *Information Security - 2025 early autumn - ICI002AS2AE-3007.* (2025). Terokarvinen.com. https://terokarvinen.com/information-security/

- MyBib Contributors. (2019, May 26). *APA Citation Generator – FREE & Fast – (7th Edition, 2019)*. MyBib. https://www.mybib.com/tools/apa-citation-generator

- OWASP. (2024). *Threat Modeling*. Cheatsheetseries.owasp.org. https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html

- *Sam the Vendor – Darknet Diaries*. (2023). Darknetdiaries.com. https://darknetdiaries.com/episode/132/

- *Threat modeling manifesto* (n.d.). www.threatmodelingmanifesto.org. https://www.threatmodelingmanifesto.org/.

- *World’s Shortest Threat Modeling Course*. (n.d.). YouTube. Retrieved June 12, 2025, from http://www.youtube.com/playlist?list=PLCVhBqLDKoOOZqKt74QI4pbDUnXSQo0nf
