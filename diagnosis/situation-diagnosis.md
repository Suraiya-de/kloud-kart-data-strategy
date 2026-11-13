
# Kloud Kart – Situation Diagnosis

## 1. Executive Summary

Kloud Kart's primary challenge is not the absence of advanced analytics capabilities, but the absence of a trusted, reliable, and governed reporting environment.

The company's current data practices expose it to operational inefficiency, compliance risks, and potential business losses. These challenges are becoming increasingly significant as the company grows and prepares to expand into Nigeria.

Four root causes have been identified:

1. **Reporting workloads compete with customer transactions:** Reporting queries and large data exports run against the same production database that supports the live e-commerce platform.
2. **Lack of trusted reporting and metric governance:** Finance and Operations work with inconsistent figures because key business metrics lack agreed definitions and a shared reporting source.
3. **Weak governance of customer data copies:** Customer information is exported and distributed without reliable tracking of where copies are stored or who has access to them.
4. **Dependence on manual spreadsheet reporting processes:** Reporting relies heavily on manual preparation and reconciliation, making the process time-consuming and difficult to repeat consistently.

These challenges affect website performance, management decision-making, staff productivity, and the company's ability to demonstrate appropriate control over customer information.

The immediate priority should be to protect the live platform, establish a trusted reporting process, improve customer data governance, and reduce dependence on manual reporting before investing in advanced analytics capabilities.

## 2. Root Cause Analysis

### Root Cause 1: Reporting and Customer Transactions Share the Same Production Database

**Evidence**
- Kloud Kart processes approximately 4,000 orders daily.
- Orders, inventory, and customer account information are stored in a MySQL database running on the same server as the live website.
- Large Monday reporting exports slowed the live website twice within the previous month.

**Why It Matters**

Reporting queries compete for database resources with the transactions that keep the e-commerce platform running. As order volumes grow, this creates a greater risk that reporting activities will affect website responsiveness and the customer purchasing experience.

**Affected Data Quality Dimensions**
- Availability
- Timeliness

**Cost Category:** Direct business and operational loss.

**Estimated Impact**

Slow website performance can interrupt customer transactions, increase abandoned purchases, and reduce customer confidence. It also creates a risk of lost sales. However, the actual revenue impact of the reported incidents has not been quantified.

**Priority:** Critical – immediate attention required.

---

### Root Cause 2: Lack of a Trusted Reporting Source and Metric Governance

**Evidence**
- Nana, the Head of Operations, manually rebuilds the company's Monday reports.
- Finance's spreadsheet consistently produces figures that do not match Nana's report.
- There is no established shared source of reporting figures or agreed definition of key business metrics.

**Why It Matters**

Different departments may calculate or interpret the same business metrics differently. Without agreed definitions and a trusted reporting source, management cannot confidently determine which figures should guide operational and financial decisions.

This also creates difficulties when comparing reports across departments or reporting periods.

**Affected Data Quality Dimensions**
- Consistency
- Accuracy

**Cost Category:** Wasted labour and management decision-making risk.

**Estimated Impact**

Management decisions may be based on conflicting information. Staff also spend time checking, correcting, and reconciling reports instead of focusing on analysis and operational decisions.

The number of staff hours lost to this process has not been measured and should be established as a baseline before calculating the actual labour cost.

**Priority:** High – requires attention to improve reporting reliability.

---

### Root Cause 3: Weak Governance of Customer Data Copies

**Evidence**
- Marketing exports customer lists containing approximately 300,000 records.
- There is no reliable tracking of how many copies of these lists exist or where they are stored.
- Kloud Kart has an ongoing Data Protection Commission complaint involving a customer's deletion request.

**Why It Matters**

When customer information is copied across departments and stored in different locations without proper oversight, the company may struggle to identify all locations containing a customer's personal data.

This makes it difficult to demonstrate appropriate control over access, retention, deletion, and the handling of customer information.

**Governance and Compliance Areas Affected**
- Customer data traceability
- Access control
- Data retention and deletion
- Accountability and compliance

**Cost Category:** Regulatory, legal, and reputational exposure.

**Estimated Impact**

Untracked customer data copies increase the company's exposure under Ghana's Data Protection Act, 2012 (Act 843).

The existing Data Protection Commission complaint makes this an immediate governance concern. The company may also face reputational damage and additional operational work if it cannot identify and account for customer data copies.

The extent of the exposure cannot be determined from the available information and requires further investigation.

**Priority:** High – immediate governance action required.

---

### Root Cause 4: Dependence on Manual Spreadsheet Reporting Processes

**Evidence**
- Nana manually rebuilds Monday reporting using exported CSV files.
- Finance and Operations maintain separate spreadsheets that produce inconsistent figures.
- Reporting preparation depends on repeated manual activities rather than a standardised and automated process.

**Why It Matters**

Manual spreadsheet workflows make reporting time-consuming and increase the possibility of human error. They also create dependencies on individual employees who understand how the reports are prepared.

As the company grows, these processes may become increasingly difficult to maintain and may delay the availability of reliable management information.

**Affected Data Quality Dimensions**
- Accuracy
- Completeness
- Consistency

**Cost Category:** Wasted labour and operational inefficiency.

**Estimated Impact**

Staff spend valuable time extracting, organising, checking, and reconciling data. This reduces the time available for analysing business performance and responding to operational issues.

Manual processes also make it harder to reproduce reports consistently and establish a clear record of how reported figures were generated.

The actual time and labour cost associated with report preparation have not been quantified.

**Priority:** Medium to High – address through standardised and repeatable reporting processes.

---

## 3. Risk Ranking

The following risks are ranked according to their potential business impact, the evidence available, and the urgency of the required response.

| Priority | Risk | Reason for Ranking |
|---|---|---|
| 1st | Production database being used for reporting | Two reporting-related slowdowns have already affected the live website, creating a direct risk to customer transactions and revenue. |
| 2nd | Act 843 compliance exposure | An existing Data Protection Commission complaint and weak customer data tracking create immediate legal and governance concerns. |
| 3rd | Lack of a trusted reporting source | Finance and Operations produce conflicting figures, reducing management's confidence in reported business information. |
| 4th | Manual spreadsheet workflows | Repeated manual reporting activities create operational inefficiency, consume staff time, and increase the possibility of errors. |

**Priority Consideration:** Although the risks are ranked, the first two require immediate attention. Customer data governance should not be postponed while the company addresses its reporting infrastructure.

## 4. Cost and Impact Assessment

The case study does not provide sufficient financial information to calculate exact monetary losses. The assessment therefore identifies the known cost exposures and the information required to quantify them.

| Risk Area | Known Evidence | Cost Exposure | Information Needed for Quantification |
|---|---|---|---|
| Production database performance | Two reporting-related website slowdowns in the previous month. | Potential lost sales, interrupted transactions, and reduced customer confidence. | Incident duration, affected orders, website performance records, and conversion data. |
| Reporting inconsistencies | Finance and Operations produce conflicting figures. | Staff time spent rebuilding and reconciling reports; risk of poor management decisions. | Hours spent preparing reports, reconciliation time, and frequency of discrepancies. |
| Customer data governance | Approximately 300,000 customer records exported without reliable copy tracking. | Regulatory, legal, operational, and reputational exposure. | Number and location of copies, access records, retention practices, and complaint scope. |
| Manual reporting processes | Nana manually rebuilds Monday reports using CSV files. | Repeated administrative work and reduced staff productivity. | Time spent extracting, cleaning, checking, and preparing weekly reports. |

The absence of exact monetary estimates should not be interpreted as an absence of business impact. It highlights the need to establish measurable baselines as part of the proposed data strategy.

## 5. Overall Diagnosis

Kloud Kart's immediate challenge is establishing control over how its existing data is processed, reported, and governed.

The company does not need to begin with a complex data warehouse, lakehouse, or machine learning platform. It first needs to address the operational and governance weaknesses affecting its current data environment.

The key areas requiring attention are:

1. **Reporting infrastructure:** Separate routine reporting workloads from production transactions without compromising the availability of the live website.
2. **Reporting governance:** Establish agreed business metric definitions and a trusted reporting source for Finance and Operations.
3. **Customer data governance:** Improve visibility, accountability, and control over customer data copies and their handling.
4. **Reporting efficiency:** Reduce dependence on manual spreadsheet preparation through standardised and repeatable reporting processes.

Addressing these foundational issues will improve reporting reliability, protect day-to-day operations, support better management decisions, and prepare Kloud Kart for future growth and more advanced analytics capabilities.
