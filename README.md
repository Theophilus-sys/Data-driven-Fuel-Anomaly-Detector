# Detection of Operational Leakage in Telecom Infrastructure
*Anomaly Detection for Fuel Consumption across 1000 tower sites*
>1. Executive Summary

In the Nigerian telecommunication landscape, fuel precisely diesel accounts for over 60% of site operational costs and with MTN's recent acquisition of IHS, there is an increasing need for focus on the data internalization that is using data to find effiencies. This notebook aims to develop an **Anomaly Detection** for identifying "Fuel Leakage" by comparing actual consumption against expected benchmarks. 
>2. Problem Statement

Manual auditing of 29,000+ tower is impossible but with an automatic way of flaging sites that deviates from the norm with this field teams can be dispatched only where leakage is significantly likely. 

>3. Data Simulation

Note that in real-world scenerio this information comes from the Remote Monitoring Systems (RMS) like those of the IHS Towers.
We will simulate a dataset containing:
* *Tower_ID:* Unique identifier
* *Region:* Five states in Nigeria
* *Expected_Daily_Usage:* Based on the power load and generator age
* *Actual_Daily_Usage:* The recorded consumption
* *Variance:* The difference between the two.

>4. Technical Implementation
* Library: Scikit-Learn (Isolation Forest)
* Logic: Isolation-Forest is an unsupervised learning algorithm that is effective for identifying outliers in high-dimensional datasets. Through the identification of anomalies by randomly selecting a feature and then randomly selecting a split value. 

>5. Business Recommendation

The model recommends that the Operation Team:
* Automation of alerting 10% for immediate inspection
* Performance of Regional Auditing as areas with higher anomaly densities are considered systemic security risky

>6. The Financial impact of this project:

Without this model, Minor Fuel leakages can go unnoticed across her 29,000 sites.
* Assumed leakage: If 5% of sites (approx 1,450 towers) experience a 20-liter daily loss due to theft or faulty sensors.
* Daily Loss: 1,450 * 20 liters = 29,000 liters/day.
* Annual cost: At an average diesel price of #1,400/liter, this represents an annual loss of over #14.8 Billion.
## Strategic Field Directives
The primary objective of implementing this **Anomaly Detection Model** is to internalizes costs. This model utilizes a *representative sample of 1,000 towers* to validate the algorithms, the system is architected for the full **MTN_IHS 29,000 tower fleet**. Without this model, "minor" fuel theft often goes unnoticed across tower sites and even a seemingly small daily loss per site scales into a massive financial drain for an telecom group
* **Statistical Significance:** A 1,000-site sample provides a **95% confidence level** with a small margin of error, allowing us to prove the "Leakage Pattern" before deploying model company-wide.
* **Algorithm Efficiency:** **Isolation Forest** is an O(n\logn) algorithm and this means that doubling the data can be done without significantly increasing computing power or processing time. 

### Strategic Alignment with MTN's Ambition 2025
This project directly supports MTN's goal of Operational Efficiencies. By moving from manual ovesight to Automated Anomaly Detection. It supports the transition from a reactive infrastructure company to a proactive digital platform.

### Implementation Roadmap
* Direct Database Integration: Replace the 1000 random simulation with a live SQL connection to the **Remote Monitoring System (RMS)**.
* Daily Batch Processsing: Run the model every 24 hours to generate a "Top 100" list of anomalies for the **National Operations Center (NOC)**.
* Threshold Tuning: The model contamination parameter can be adjusted as it current value is based on historical theft data from the Nigerian Communication Commission.
* Refined ROI: At full scale, the **14.8Billion** annual loss identified in our 20-liter scenerio becomes a core target for **OPEX reduction**.

### ROI Analysis
* Tageted Auditing: The model directs security and maintenance teams only to the top 5% flagged anomalies and not an expensive physical audits of 29,000 sites thereby reducing Field Operation costs by an estimated 30% - 40%.
* Deterrence Effect: Acts as a psychological deterrent for third party contractors or vendors as they know "Digital Eyes" are monitoring consumptions in real-time.
* Proactive maintenance: As anomalies aren't always due to theft and with this model, generators losing efficency are spotted. this ensures early prevention efforts for total site blackout which costs the company significant "Service Level Agreement" penalties from mobile operators.
![Sensitivity Analysis](sensitivity_analysis (1).png)
## Strategic Interpretation: Sensitivity Analysis 
The Chart above illustrates the financial risk exposure based on two volatile market conditions that is diesel prices and leakage rate (Anomaly Frequency). 
* Price Floor & Ceilling: With diesel price at #1,000/L, a 5% leakage results in a #10.5Billion annual loss. As Prices fluctuate towards #2,000/L the same leakage escalated to #21 Billion.
* Operational Control: The vertical spread between the lines represents *Value of Intervention*. Moving the organization from a 10% leakage rate to 3% leakage rate through this detection model saving the business #15 - 20 Billion regardless of fuel price volatility.
* Conclusion for management: By reducing the rate of anomalies through real-time detection and deterence, we can significantly lower the company's vulnerability to external fuel price shocks so therefore directly protecting the Earnings Before Interest Taxes Depreciation and Amortization margin.
