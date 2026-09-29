# Awesome-Data-Clean-Room-For-Advertising

## Top Data Clean Room for Advertising Platforms Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Privacy-Preserving Data Collaboration, Audience Overlap, Campaign Measurement & Lookalike Modeling*  

**Last updated: September 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Data Clean Rooms in Advertising**. These tools help advertisers, publishers, and data providers match first-party data, measure campaign effectiveness, and build audiences without exposing raw user-level data.



**Examples** include Habu (LiveRamp), InfoSum, LiveRamp Safe Haven, Snowflake Clean Rooms, AWS Clean Rooms, Google Ads Data Hub, Decentriq, Datavant, Anonos, Salesforce Data Cloud, and Optable (the category leaders).



**Open-source emphasis**: Data clean rooms are a **commercially dominated category**, but a significant open-source foundation exists through **TikTok's PrivacyGo Data Clean Room** (released June 2024) and **ManaTEE** (Confidential Computing Consortium project). Both use **Trusted Execution Environments (TEEs)** to enable secure multi-party data collaboration without exposing underlying data . This section documents these self-hostable solutions and the broader open-source TEE ecosystem.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents



- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Habu (LiveRamp)](https://habu.com/)**  

  Data clean room platform acquired by LiveRamp, now integrated as **LiveRamp MAP Clean Room**. Built on **Azure Confidential Computing (ACC)** platform with hardware-based TEEs ensuring data remains private and secure. Supports custom queries for measurement use cases, actionable insights generation, and custom audience creation. Uploaded advertiser signals remain in the advertiser's dedicated LiveRamp instance and are inaccessible to Microsoft. Currently supports **exact joins on hashed emails (HEM)** only .



- **[InfoSum](https://www.infosum.com/)**  

  **True multi-party data clean room with zero data movement.** Patented "non-movement" technology using **Private Set Intersection (PSI)** scaled to billions of rows in seconds. Supports unlimited datasets, cloud-agnostic decentralized processing, and end-to-end privacy protection. Platform Sigma (2024) added **Cloud Vault** (computation directly on cloud storage without copying), **Transformations** (on-demand reshaping of any dataset), and **Full SQL Compatibility**. Drag-and-drop interface for marketers, not just data scientists .



- **[LiveRamp Safe Haven](https://liveramp.com/)**  

  Neutral connectivity infrastructure for secure data management, activation, measurement, and collaboration between publishers, brands, and partners. **Two environments**: Customer Profiles (marketer workspace for audience building, insights, lookalike modeling, activation) and Analytics Environment (data scientist workspace for advanced modeling, analysis, visualization). Data pseudonymized via **RampID matching** with virtual desktop lockdown — data cannot leave the environment. Granular permissioning at taxonomy, audience, and data view levels .



- **[Snowflake Data Clean Rooms](https://www.snowflake.com/)**  

  Native clean rooms within the Snowflake Data Cloud. **2026 updates** introduce **symmetric multiparty collaboration** (multiple organizations contribute, analyze, activate data in shared controlled environment), **Snowsight native experience**, **Cortex Code** for accelerated setup, and **Snowflake Intelligence** for natural language interaction. Moves beyond rigid provider-consumer roles to support real-world partner networks .



- **[AWS Clean Rooms](https://aws.amazon.com/clean-rooms/)**  

  Fully managed data collaboration service. **AWS Clean Rooms ML** provides lookalike modeling trained on the collaboration with up to **36% accuracy improvement** over industry baselines. **Differential privacy** controls require no prior expertise. **Synthetic datasets** generate statistically representative data for training models without exposing original data. Supports SQL, PySpark, Spark SQL, and bring-your-own ML models. Zero-ETL collaboration across Snowflake and AWS data .



- **[Google Ads Data Hub](https://developers.google.com/ads-data-hub)**  

  Privacy-safe data warehouse solution for analyzing Google Ads campaign data. Built on **BigQuery** with aggregation requirements (minimum 10 users for click/conversion queries, 50 for others) and differential privacy. Supports data linking from YouTube, Search, and other Google products. **Analyst, Relationship Manager, and Superuser** access roles. All analytic functions are blocked for privacy reasons .



- **[Decentriq](https://www.decentriq.com/)**  

  Swiss data clean room platform using **confidential computing** for privacy-preserving data collaboration. NIQ (NielsenIQ) joined the Decentriq Network in September 2025 to enable secure data collaboration for marketers and agencies across Europe, with NIQ's Digital Purchase data available for audience profiling and closed-loop measurement .



- **[Datavant](https://www.datavant.com/)**  

  Healthcare-focused data collaboration platform. **Datavant Connect powered by AWS Clean Rooms** (November 2025) enables life sciences organizations to discover and assess fit-for-purpose real-world data. Uses **no-underlying-data-movement** approach for secure, cloud-first collaboration. Validated by four top 20 pharma companies and 15 leading RWD sources .



- **[Salesforce Data Cloud Clean Room](https://help.salesforce.com/)**  

  Clean room within Salesforce Data 360. Provides **zero-copy** data sharing between Data 360 orgs. Providers and consumers collaborate through **collaboration templates** defining required/optional data fields, allowed queries, query-running parties, and result recipients. Query results aggregated for privacy and stored in **Data Model Objects (DMOs)** for reporting .



- **[Optable](https://www.optable.co/)**  

  Data collaboration network with **Insights Clean Rooms** for privacy-preserving audience overlap analysis. Uses **differential privacy** with thresholding and calibrated noise. Supports **participant reports** (overlap distribution across traits) and **summary reports** (aggregated union of all participants). Privacy budget system tracks and limits privacy cost per partner .



## Open-Source GitHub Projects



- **[PrivacyGo Data Clean Room (TikTok)](https://github.com/tiktok-privacy-innovation/PrivacyGo-DataCleanRoom)**  

  **The leading open-source TEE-based data clean room for advertising.** Released by TikTok in June 2024 and now part of the **Confidential Computing Consortium** as **ManaTEE** . **Two-stage architecture**: **Programming Stage** (data consumers explore low-risk data with PETs like pseudonymization or differentially private synthetic data) and **Secure Execution Stage** (workloads run in TEE with attestable integrity and confidentiality guarantees) . **Features**: Jupyter Notebook integration (Python), multiparty collaboration, flexible PET selection per stage, cloud-ready deployment to Google Confidential Space, JWT-based attestation reports for public verification . **Use cases**: Trusted Research Environments, **advertising lookalike segment analysis**, private ad tracking, private model training . **Open source** (Apache-2.0). Current version supports one-way collaboration, Google Cloud Platform backend, CPU computation .



- **[ManaTEE](https://github.com/)**  

  The Confidential Computing Consortium project name for TikTok's PrivacyGo Data Clean Room. Designed to enable secure data collaboration without compromising individual privacy. Addresses the challenge that **existing solutions (differential privacy, commercial clean rooms) often fail to balance privacy, accuracy, and usability, particularly at large scale** . Led by TikTok's founding developers with plans to expand leadership through a Technical Steering Committee .



- **[PrivacyGo (Broader Ecosystem)](https://github.com/tiktok-privacy-innovation)**  

  TikTok's broader privacy innovation ecosystem includes PrivacyGo Data Clean Room as its core advertising use case, alongside other privacy-enhancing technologies. The project encourages open collaboration and community contribution within the Confidential Computing Consortium .



### Additional Strong Open-Source Options



- **TEE-Based Clean Rooms**: **PrivacyGo/ManaTEE** (leading open-source advertising clean room), **Open Enclave** (Microsoft, TEE framework), **Google Confidential Space** (TEE backend for ManaTEE).

- **Privacy-Enhancing Technologies**: **OpenMined** (differential privacy, federated learning), **OpenDP** (differential privacy library), **Private Set Intersection** libraries for data linkage without exposure.

- **Related Open-Source**: **Karlsgate** (distributed cryptographic exchange — "clean stream" not clean room, data stays behind firewall) , **Anonos** (patented data privacy via "Variant Twins" and functional separation) .



**Frameworks for building custom systems**: Combine **PrivacyGo/ManaTEE** for the core TEE-based clean room with two-stage programming/execution model, **Google Confidential Space** as the TEE backend, and **Jupyter Notebook** for the interactive programming stage. For non-TEE approaches, consider **differential privacy libraries** (OpenDP, OpenMined) and **Private Set Intersection** for secure data linkage. Add **JWT attestation** for verifiable execution integrity .



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Data clean rooms handle sensitive consumer and advertising data; ensure compliance with GDPR, CCPA, and relevant privacy regulations.

- **Open-source reality**: The open-source ecosystem for advertising data clean rooms is **emerging but limited**. **PrivacyGo/ManaTEE** is the leading open-source TEE-based clean room, released by TikTok in 2024 and governed by the Confidential Computing Consortium . However, it currently supports **one-way collaboration only**, requires **Google Cloud Platform**, and uses **CPU computation** (GPU support planned) . For **multi-party symmetric collaboration**, **production-scale marketing use cases**, and **enterprise support**, commercial platforms (InfoSum, Snowflake, AWS Clean Rooms, LiveRamp Safe Haven) remain the primary choice. The TEE approach is promising but requires significant engineering investment to match commercial clean room capabilities.



---



**Made for advertising technologists, data collaboration engineers, privacy engineers, and marketing measurement teams.**

Let's make advertising data clean rooms more open, transparent, and privacy-preserving.
