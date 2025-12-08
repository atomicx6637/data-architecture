# Data Governance Maturity Plan: Data Classification & Labeling Program
## Electric & Natural Gas Utility Implementation Guide

---

## Current State Assessment

### Existing Capabilities
The organization has foundational classification framework and technology infrastructure in place:

| Asset | Status | Coverage | Critical Gap |
|-------|--------|----------|--------------|
| **Data Classification Framework** | **DEFINED** | Enterprise taxonomy exists | **NOT APPLIED - labels exist but data remains unlabeled** |
| **PII Definitions** | **DEFINED** | Core systems (CIS, HR) | **Limited to structured data; unstructured data unclassified** |
| **Microsoft Purview** | **DEPLOYED** | Infrastructure exists | **NOT CONFIGURED - auto-labeling policies not active, scanners not deployed** |
| **M365 Environment** | Partial | ~30-40% of data | **Most content unclassified; users not trained on labeling** |
| **Legacy File Shares** | Unmanaged | 60-70% of enterprise data | **Completely unclassified and ungoverned** |

### The Critical "Definition vs. Execution" Gap

**Current Reality**: The utility has invested in classification taxonomy design and Purview deployment, but **90%+ of actual data remains unclassified and ungoverned.** This is a classic "framework exists but execution doesn't" situation.

**Specific Gaps**:
1. **Labels Defined, Not Applied**: Sensitivity labels exist in Purview but are not actively applied to documents, emails, file shares, or databases
2. **Unknown Data Landscape**: No comprehensive inventory of where sensitive data actually resides across file shares, databases, and unstructured repositories
3. **Manual Labeling Only**: No auto-classification policies configured; relies on users to manually label (which isn't happening)
4. **Purview "Shelfware"**: Platform deployed but critical capabilities dormant: Data Map scanners not running, trainable classifiers not built, DLP policies not active
5. **No Discovery Process**: Cannot protect what you haven't found - need systematic data discovery and inventory before classification
6. **User Adoption Failure**: M365 users aren't labeling content because they lack training, enforcement, and integrated workflows

### Estimated Current Classification Coverage
- **M365 Content**: 10-15% labeled (mostly ad-hoc user labeling, inconsistent)
- **File Shares**: <5% classified (no automated scanning, occasional manual tagging)
- **Databases**: PII defined in core systems only (CIS customer data, HR employee data); other databases unclassified
- **Unstructured Data**: 90%+ completely unclassified and undiscovered

### Strategic Positioning
**This is a LABEL APPLICATION and DATA DISCOVERY program, NOT a framework design initiative.** The taxonomy exists; the challenge is systematically applying it to terabytes of unmanaged data while building sustainable classification workflows. The focus must be on:
- **Discovery First**: Systematically inventory and scan data sources to understand what exists and where sensitive data resides
- **Automated Classification at Scale**: Configure Purview auto-labeling, trainable classifiers, and scanning to classify millions of files
- **Crawl-Walk-Run Approach**: Start with automated discovery and high-risk "crown jewels," expand to enterprise coverage
- **Operationalize Purview**: Move from "deployed" to "configured with active policies" - activate scanners, auto-labeling rules, and DLP enforcement
- **User Adoption Program**: Train users, embed labeling in workflows, create enforcement mechanisms to sustain manual classification where automation can't reach

---

## Executive Summary

This maturity plan provides three pathways for **applying the existing classification framework to actual data at scale**. The utility has invested in taxonomy design and Purview deployment, but 90%+ of data remains unclassified. Each pathway focuses on systematic data discovery, automated label application, and building sustainable classification workflows to achieve measurable coverage targets while addressing regulatory compliance (NERC CIP, FERC, state privacy laws) and operational risk reduction.

**The Core Challenge**: Moving from "labels exist" to "data is labeled" requires:
1. **Data Discovery & Inventory**: Systematically scan file shares, databases, and M365 to understand where sensitive data resides
2. **Purview Configuration**: Activate auto-labeling policies, deploy Data Map scanners, configure trainable classifiers
3. **Automated Classification at Scale**: Use Purview automation to classify millions of files without manual effort
4. **Crown Jewels First**: Prioritize high-risk data (NERC CIP BCSI, customer PII, confidential financials) for immediate coverage
5. **User Adoption Program**: Train M365 users, embed labeling in workflows, create enforcement for manual classification where needed

**Coverage Targets by Option**:
- **Option 1 (6-12 months)**: 40-60% of priority data classified through automated discovery and targeted manual labeling
- **Option 2 (12-18 months)**: 70-85% of enterprise data classified with broader automation and expanded scope
- **Option 3 (24-36 months)**: 90%+ comprehensive coverage with full automation, IoT/OT integration, and mature governance

**Critical Success Factors**: Executive commitment to "finishing what we started," Purview specialist expertise, data discovery preceding policy enforcement, phased automation build-out, and realistic expectations about classification accuracy and manual remediation needs.

---

## Option 1: Data Discovery & Automated Classification Kickstart (6-12 Months)

### Overview & Objectives

This pathway focuses on **discovering and classifying priority data at scale** using Purview automation capabilities. Starting from 10-15% current classification coverage, the goal is to achieve 40-60% coverage on high-priority data sources through automated scanning, auto-labeling policies, and targeted manual classification of "crown jewels" data.

**Primary Objectives**:
- **Data Discovery**: Scan and inventory top 15-20 priority file shares and M365 environments to understand where sensitive data resides
- **Purview Configuration**: Activate auto-labeling policies, sensitivity label publishing, and Data Map scanners (moving from "deployed" to "operationalized")
- **Automated Classification**: Apply labels to 300K-500K files through Purview automation (sensitive info types, keyword matching, pattern detection)
- **Crown Jewels Priority**: Achieve 80%+ classification coverage on NERC CIP BCSI, customer PII, and confidential financial data
- **M365 User Enablement**: Train users and enable mandatory labeling for 60-70% of M365 population to sustain ongoing classification
- **Quick Wins**: Demonstrate measurable risk reduction and build business case for Option 2 expansion

**Target Coverage at 12 Months**: 40-60% of priority data classified (up from 10-15% baseline)

### Implementation Phases

| Phase | Timeline | Key Activities | Deliverables |
|-------|----------|----------------|--------------|
| **1. Data Discovery & Baseline** | Month 1-2 | Deploy Purview Data Map scanners to M365 (SharePoint, OneDrive, Teams) and top 15 priority file shares; run initial discovery scans to inventory data and identify sensitive content using built-in classifiers; establish current state baseline (estimated 10-15% classified); create data sensitivity heatmap | Complete data inventory (file counts, sizes, locations), sensitive data discovery report (PII, BCSI findings), current classification baseline metrics, priority data source risk scoring |
| **2. Purview Auto-Labeling Configuration** | Month 2-3 | Configure sensitivity labels in Purview (map to existing taxonomy); build auto-labeling policies using sensitive info types (SSN, credit cards, account numbers, employee IDs); configure keyword-based rules for BCSI, confidential contracts; test policies on pilot dataset (10K files); tune for accuracy (target 85%+) | 8-12 auto-labeling policies operational, sensitivity label schema published, initial accuracy assessment, tuning playbook |
| **3. Automated Classification Wave 1** | Month 3-5 | Execute auto-labeling on M365 content (SharePoint sites, OneDrive, Teams); run scanner-based auto-classification on priority file shares (targeting 200K-300K files); monitor classification results and false positive rates; remediate misclassifications; establish weekly scanning cadence | 200K-300K files auto-classified, classification accuracy report, false positive remediation log, scanning operations runbook |
| **4. Crown Jewels Manual Classification** | Month 4-6 | Identify critical unclassified data not caught by automation (SCADA procedures, substation diagrams, board materials, M&A documents); assign to business data stewards for manual labeling; implement mandatory labeling workflow; conduct targeted steward training; track completion | 15K-25K high-value files manually classified by stewards, mandatory labeling enabled in sensitive SharePoint sites, steward training completion (20-30 users) |
| **5. M365 User Adoption & Training** | Month 5-7 | Deploy sensitivity labels to 60-70% of M365 users (Outlook, Word, Excel, PowerPoint); deliver role-based training (compliance, engineering, customer service, finance); enable default labels and mandatory labeling in pilot departments; establish helpdesk support model | 60-70% user adoption (actively labeling new content), training completion (500-800 users), adoption metrics dashboard, helpdesk runbook |
| **6. DLP Policy Activation (Monitor Mode)** | Month 7-9 | Configure Purview DLP policies leveraging applied labels (block external sharing of Restricted/Confidential, detect PII in emails); implement in MONITOR mode (policy tips, no blocking) for 30 days; analyze violations and user feedback; tune policies; prepare for enforcement | DLP policies configured (5-8 policies), 30-day monitoring report, policy tuning decisions, enforcement readiness assessment |
| **7. Validation & Business Case** | Month 10-12 | Audit classification coverage (sample 2000+ files across sources); measure accuracy; calculate risk reduction (% of sensitive data now protected); assess Purview ROI; identify gaps for Option 2; develop expansion business case | Final coverage report (40-60% target validated), accuracy metrics (85%+ target), ROI analysis, Option 2 business case with lessons learned |

### Staffing Plan

| Role | FTE | Responsibilities | Duration |
|------|-----|------------------|----------|
| Program Manager | 1.0 | Overall classification program leadership, executive reporting, stakeholder alignment, ROI tracking | 12 months |
| **Purview Policy Analyst** (CRITICAL ROLE) | 1.5 | Configure auto-labeling policies, manage Data Map scanners, tune classifiers, optimize accuracy, troubleshoot scanning issues | 12 months |
| Data Discovery Specialist | 1.0 | Deploy and manage Purview scanners for file shares and M365, analyze discovery results, create sensitivity heatmaps, prioritize data sources | 10 months |
| Data Governance Coordinator | 0.5 | Align existing taxonomy to Purview labels, support stewards, manage manual classification workflows | 12 months |
| Classification Quality Analyst | 0.75 | Validate auto-classification accuracy, identify false positives/negatives, support policy tuning, conduct audits | 10 months |
| Business Analysts / Training Specialists | 1.5 | M365 user training delivery, steward enablement, helpdesk support, adoption measurement | 12 months |
| Data Stewards (Business) | 1.5 | Part-time stewards from 8-10 business units (0.15-0.2 FTE each) for manual "crown jewels" classification and validation | 12 months |
| Security/Compliance SME | 0.25 | DLP policy requirements, NERC CIP BCSI identification, regulatory alignment validation | 8 months |
| Change Management | 0.75 | User adoption campaign, communications, training coordination, adoption analytics | 12 months |
| **Total Core Team** | **8.75 FTE** | Emphasis on Purview configuration expertise, discovery/scanning operations, and classification quality | |

### Technology Requirements

**Existing Platform Utilization** (Months 1-6):
- **Microsoft Purview Information Protection**: Configure sensitivity labels, auto-labeling policies, mandatory labeling (ALREADY DEPLOYED)
- **Purview Data Loss Prevention**: Activate DLP policies using existing PII definitions (ALREADY DEPLOYED)
- **Purview Data Map**: Deploy scanners for on-premises file shares and databases (licensing ALREADY AVAILABLE)
- **Purview Compliance Portal**: Configure reporting, audit logs, compliance dashboards (ALREADY DEPLOYED)

**Incremental Additions** (Months 6-12):
- **File share scanning infrastructure**: On-premises scanner agents for Purview Data Map (no additional licensing, deployment only)
- **Azure Information Protection unified labeling client**: Deploy to end-user workstations for file share access (included in M365 E5)
- **Power BI templates**: Purview adoption and compliance reporting (utilize existing Power BI if available)
- **Migration tooling**: For prioritized file share to SharePoint/OneDrive migration (leverage Microsoft SharePoint Migration Tool or third-party accelerator)

**Integration Requirements**:
- Purview integration with Active Directory (for file share scanning and access reviews) - configuration only
- DLP integration with Exchange Online, SharePoint, OneDrive, Teams (native M365 integration) - activation only
- Connector to key operational databases (CIS, MDMS) if extending auto-classification beyond M365 (optional for Phase 1)

**Key Point**: This option requires NO new platform licenses. Investment is in configuration, deployment, and adoption of existing Purview capabilities.

### Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| **Overall Classification Coverage** | **40-60% of priority data sources classified** (up from 10-15% baseline) | Purview Data Map coverage reports across M365 + priority file shares (quarterly audit) |
| **Automated Classification Volume** | 300K-500K files auto-labeled through Purview policies and scanners | Purview Activity Explorer + Data Map classification reports |
| **Classification Accuracy** | 85%+ accuracy on auto-labeled content (reduce false positives to <15%) | Statistical sampling validation (2000+ files per quarter) |
| **Crown Jewels Coverage** | 80%+ of NERC CIP BCSI, customer PII, and confidential financial data classified | Targeted audit of high-risk data repositories |
| **M365 User Adoption** | 60-70% of M365 users actively applying labels to new content (emails, documents) | Purview Activity Explorer user engagement metrics |
| **Data Discovery Completion** | 100% of priority file shares (15-20 shares) and M365 environments scanned and inventoried | Data Map scan completion logs + inventory reports |
| **Manual Classification (Crown Jewels)** | 15K-25K high-value files manually labeled by business stewards | Steward workflow tracking + completion reports |
| **DLP Readiness** | 5-8 DLP policies configured and tested in monitor mode; <5% false positive rate | DLP policy testing reports + 30-day monitoring period analysis |
| **Unclassified Data Baseline** | Establish quantified inventory of remaining unclassified data (target for Option 2) | Data discovery reports identifying gaps and未covered sources |

### Budget Range Estimate

| Category | Low Estimate | High Estimate | Notes |
|----------|--------------|---------------|-------|
| **Software/Tools** | $0 | $50K | NO new licenses needed (Purview deployed); optional migration accelerator tools or enhanced Power BI reporting |
| **Professional Services** | $75K | $150K | Microsoft FastTrack or partner for Purview configuration, scanner setup, adoption best practices (4-6 weeks) |
| **Internal Labor** | $485K | $675K | 6.75 FTE blended rate ($75K-$100K average loaded cost) |
| **Training & Change Mgmt** | $60K | $120K | M365 user training materials, adoption campaign, helpdesk readiness |
| **File Share Infrastructure** | $25K | $50K | Scanner servers, network/security config for Purview connectivity to file shares |
| **Contingency (15%)** | $97K | $149K | User adoption challenges, file share complexity, data remediation scope expansion |
| **Total 12-Month Budget** | **$742K** | **$1.19M** | 25-35% cost reduction vs. greenfield due to existing platform investment |

**Ongoing Annual Costs (Year 2+)**: $150K-$250K (Purview licensing already covered in M365 E5; sustaining team 1.5-2.0 FTE for ongoing governance operations)

---

## Option 2: Enterprise Classification Scale-Up (12-18 Months)

### Overview & Objectives

This pathway **builds directly on Option 1's discovery and automation foundation** (or accelerates those activities in months 1-4) to achieve **70-85% enterprise-wide classification coverage** across all file shares, M365 environments, and operational databases. The focus shifts from priority data sources to comprehensive enterprise scanning, advanced automation through trainable classifiers, and systematic elimination of unclassified data.

**Primary Objectives**:
- **Complete Data Discovery**: Scan ALL file shares (50-100+ shares), full M365 tenant, and operational databases (CIS, MDMS, GIS)
- **Advanced Auto-Classification**: Build trainable classifiers for utility-specific content (SCADA procedures, engineering documents, regulatory filings); expand automation to cover 80%+ of data through ML-based classification
- **Comprehensive Coverage**: Classify 1M-2M files through combination of automated scanning and targeted manual steward workflows
- **Operational Systems Integration**: Extend classification to structured data in CIS customer records, MDMS meter data, GIS infrastructure data
- **Full M365 Adoption**: Achieve 85%+ user adoption with mandatory labeling across enterprise
- **DLP Enforcement**: Move from monitor mode to active blocking of policy violations with comprehensive coverage
- **Minimize Unclassified Data**: Reduce unclassified data to 15-30% (primarily edge cases, legacy archives, and data queued for retirement)

**Target Coverage at 18 Months**: 70-85% of enterprise data classified (up from 40-60% in Option 1)

### Implementation Phases

| Phase | Timeline | Key Activities | Deliverables |
|-------|----------|----------------|--------------|
| **1. Foundation Completion** | Month 1-4 | Complete Option 1 activities if not done (priority data discovery, auto-labeling setup, M365 adoption); establish 40-60% baseline coverage; analyze gaps and unclassified data patterns; plan enterprise expansion priorities | Option 1 deliverables complete, gap analysis report, enterprise classification expansion plan |
| **2. Enterprise Data Discovery** | Month 3-6 | Deploy Purview scanners to ALL remaining file shares (50-100+ shares, 2M-5M files); complete full M365 tenant scanning; inventory operational databases (CIS, MDMS, GIS); create comprehensive sensitivity map of entire data estate | Complete enterprise data inventory (all sources), comprehensive sensitivity heatmap, unclassified data quantification |
| **3. Trainable Classifiers Development** | Month 4-7 | Build custom ML classifiers for utility-specific content (SCADA procedures, engineering drawings, regulatory filings, board materials, incident reports); train models using labeled datasets; test accuracy (target 80-85%); deploy to production | 5-8 trainable classifiers operational for utility-specific content, accuracy validation reports, production deployment |
| **4. Automated Classification Wave 2** | Month 6-10 | Execute enterprise-wide auto-labeling using expanded policies and trainable classifiers; classify 800K-1.2M additional files; continuous monitoring and tuning; remediate misclassifications; weekly reporting | 800K-1.2M files auto-classified (cumulative 1M-1.5M total), classification accuracy optimization, weekly progress reports |
| **5. Operational Database Classification** | Month 7-11 | Deploy Purview Data Map connectors to CIS (customer PII, account data), MDMS (meter/interval data), GIS (infrastructure locations); configure column-level classification; apply labels to structured data; integrate with existing data catalog if present | CIS, MDMS, GIS databases scanned and classified (tables/columns), structured data governance established, catalog integration |
| **6. Steward-Led Gap Remediation** | Month 10-14 | Identify remaining unclassified high-value data (20-30% of estate); assign to expanded steward network (15-20 stewards); implement workflows for systematic manual classification; track completion; quality assurance | 100K-200K files manually classified by stewards, unclassified data reduced to 15-30%, steward performance metrics |
| **7. DLP Enforcement & Validation** | Month 14-18 | Activate DLP enforcement (move from monitor to block mode); extend DLP to endpoints and file shares; implement context-aware policies; conduct final coverage audit (target 70-85%); optimize for accuracy (90%+); business case for Option 3 | DLP enforcement operational, final coverage audit (70-85% validated), 90%+ classification accuracy, Option 3 business case |

### Staffing Plan

| Role | FTE | Responsibilities | Duration |
|------|-----|------------------|----------|
| Program Manager | 1.0 | Enterprise classification program leadership, executive reporting, budget/schedule management | 18 months |
| **Purview Policy Analysts** | 2.0 | Build/tune trainable classifiers, manage enterprise-wide auto-labeling policies, optimize ML models, troubleshoot scanning at scale | 18 months |
| Data Discovery & Scanning Lead | 1.0 | Deploy/manage scanners across all file shares and databases, analyze discovery results, prioritize classification waves | 18 months |
| Classification Quality Manager | 1.0 | Validate accuracy across 1M+ classified files, identify systematic errors, drive continuous improvement, audit reporting | 18 months |
| Database Scanning Specialists | 1.5 | Deploy Purview Data Map connectors to CIS, MDMS, GIS; configure column-level classification; structured data governance | 12 months |
| Business Analysts / Automation Specialists | 2.0 | Steward workflow automation, classification reporting, user training support, process optimization | 18 months |
| Data Stewards (Business) | 2.5 | Expanded network: 15-20 part-time stewards (0.15-0.25 FTE each) for manual classification and validation | 18 months |
| GIS/SCADA/OT SME | 0.75 | Operational system classification standards, BCSI identification, trainable classifier training for OT content | 12 months |
| Security/Compliance SME | 0.75 | DLP policy requirements, enforcement readiness, NERC CIP alignment, audit support | 16 months |
| Data Catalog Integration Lead | 0.5 | Purview-to-catalog integration, metadata synchronization (if separate catalog exists) | 10 months |
| Change Management / Training | 1.0 | Enterprise user adoption, advanced training, helpdesk support, adoption analytics | 18 months |
| **Total Core Team** | **14.0 FTE** | Scaled team for enterprise classification; emphasis on automation, quality, and steward network expansion | |

### Technology Requirements

**Purview Advanced Features Activation** (Months 1-12):
- **Purview Insider Risk Management**: Configure insider risk policies for data exfiltration, BCSI mishandling (module ALREADY LICENSED in M365 E5)
- **Purview Records Management**: Implement regulatory retention schedules, disposition workflows (module ALREADY LICENSED)
- **Purview eDiscovery**: Configure for regulatory inquiries, FERC requests, litigation holds (module ALREADY LICENSED)
- **Purview Communication Compliance**: Monitor customer service interactions for PII mishandling (module ALREADY LICENSED)
- **Purview Endpoint DLP**: Extend DLP to Windows endpoints, USB controls, print restrictions (ALREADY LICENSED, deployment needed)

**Enterprise Scanning & Classification** (Months 4-14):
- **Purview Data Map connectors**: Deploy to SQL Server, Oracle, PostgreSQL databases (CIS, MDMS, GIS, OMS) - included in licensing
- **Enhanced scanners**: Additional on-premises scanner capacity for 50-100 file shares (infrastructure scaling only)
- **Trainable classifiers**: Custom ML models for utility-specific content (SCADA procedures, engineering drawings) - included capability
- **Azure Information Protection (AIP)**: Enterprise deployment to all endpoints for label persistence (ALREADY LICENSED)

**Migration & Integration Tools** (Months 4-16):
- **SharePoint Migration Tool or third-party accelerator**: For large-scale file share migration (Microsoft tool free; accelerator $50K-$150K optional)
- **Data catalog integration**: If separate catalog exists (Collibra, Alation), API integration with Purview classification metadata (integration labor, no new licenses)
- **Power Automate**: Workflow automation for retention, access requests, incident response (ALREADY LICENSED in M365)
- **External sharing controls**: Azure RMS/AIP for label preservation outside organization (ALREADY LICENSED)

**Key Point**: Minimal new licensing required. Primary investment is activating underutilized Purview modules and scaling infrastructure for enterprise scanning.

### Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| **Enterprise Classification Coverage** | **70-85% of ALL data sources classified** (M365, file shares, databases) - up from 40-60% in Option 1 | Purview Data Map enterprise audit + comprehensive sampling (3000+ files quarterly) |
| **Total Files Classified** | 1M-2M files auto-labeled + manually labeled (cumulative from Option 1) | Purview classification volume reports across all data sources |
| **Trainable Classifier Performance** | 5-8 utility-specific classifiers operational with 80-85% accuracy | ML model validation testing + production monitoring |
| **Automated vs. Manual Classification Ratio** | 80% automated, 20% manual steward-led classification | Classification method attribution reporting |
| **Classification Accuracy (Enterprise)** | 90% accuracy across M365/file shares; 85% accuracy for databases | Statistical sampling validation (3000+ items per quarter across all sources) |
| **Operational Database Coverage** | 100% of CIS, MDMS, GIS databases scanned; column-level classification applied to sensitive tables | Data Map database scan completion + metadata reports |
| **Unclassified Data Reduction** | Reduce unclassified data from 40-50% (post-Option 1) to 15-30% | Gap analysis reports + unclassified data inventory |
| **M365 User Adoption** | 85% of users actively labeling new content; mandatory labeling enforced in high-risk areas | Purview Activity Explorer user engagement metrics |
| **DLP Enforcement Readiness** | DLP policies active in enforcement mode with <3% false positive rate; 95% user compliance | DLP policy effectiveness reports + incident tracking |
| **Steward Network Maturity** | 15-20 trained stewards completing 100K-200K manual classifications with 90%+ quality score | Steward performance metrics + quality audits |

### Budget Range Estimate

| Category | Low Estimate | High Estimate | Notes |
|----------|--------------|---------------|-------|
| **Software/Tools** | $50K | $150K | Migration accelerator tools (optional), Power BI premium (optional); Purview modules ALREADY LICENSED |
| **Infrastructure** | $75K | $125K | Additional scanner servers, network/security config, endpoint AIP deployment, database connector infrastructure |
| **Professional Services** | $200K | $350K | Microsoft partner for advanced Purview features (Insider Risk, Records Mgmt), trainable classifiers, optimization (10-14 weeks) |
| **Internal Labor** | $970K | $1.35M | 13.5 FTE blended rate over 18 months ($75K-$100K average loaded) |
| **Migration Program** | $100K | $200K | File share migration project costs (cleanup, testing, user cutover support) |
| **Training & Change Mgmt** | $125K | $200K | Enterprise-wide advanced training, ongoing adoption, helpdesk expansion |
| **Third-Party Consulting** | $50K | $100K | Legal review for vendor agreements, privacy impact assessments, compliance validation |
| **Contingency (15%)** | $232K | $368K | File share complexity, operational system integration challenges, migration delays |
| **Total 18-Month Budget** | **$1.8M** | **$2.84M** | 35-45% savings vs. greenfield; if building on completed Option 1, subtract $400K-$600K |

**Ongoing Annual Costs (Year 2+)**: $300K-$450K (Purview licensing already in M365 E5; sustaining team 2.5-3.0 FTE for operations and continuous improvement)

---

## Option 3: Comprehensive Coverage & Advanced Automation (24-36 Months)

### Overview & Objectives

This pathway **builds on Options 1 and 2's classification foundation** (or accelerates them) to achieve **90%+ comprehensive enterprise coverage** with advanced automation, IoT/OT data governance, and intelligent classification at the point of data creation. The focus shifts from "catch-up classification" to "classification-by-design" where new data is automatically labeled at ingestion across all systems.

**Primary Objectives**:
- **Near-Complete Coverage**: Achieve 90-95%+ classification across ALL data sources including M365, file shares, databases, IoT streams, and legacy archives
- **Advanced Automation**: Implement real-time classification at data creation/ingestion points; expand trainable classifiers to 15-20 models covering all utility content types
- **IoT/OT Data Classification**: Extend labels to AMI streaming data (10M-50M devices), SCADA historian time-series data, and DER device metadata
- **Legacy Data Remediation**: Systematically classify remaining 10-30% of edge cases, legacy archives, and complex unstructured content through dedicated steward campaigns
- **File Share Elimination**: Complete migration of 90%+ file share data to M365; decommission legacy infrastructure
- **Classification-by-Design**: Embed auto-labeling in all data workflows (document creation, email composition, database inserts, IoT ingestion)
- **Self-Sustaining Operations**: Transition from project to BAU operations with minimal ongoing manual classification (<5% of new data)

**Target Coverage at 36 Months**: 90-95%+ of enterprise data classified with sustained automation maintaining coverage as new data is created

### Implementation Phases

| Phase | Timeline | Key Activities | Deliverables |
|-------|----------|----------------|--------------|
| **1. Foundation Completion** | Month 1-6 | Complete Options 1-2 activities if not done (70-85% coverage achieved); establish comprehensive baseline of remaining unclassified data (10-30%); analyze gap patterns and remediation strategies; plan final coverage push | Options 1-2 deliverables complete, comprehensive unclassified data inventory, remediation strategy by data type |
| **2. Advanced Trainable Classifiers** | Month 4-10 | Expand ML models to 15-20 trainable classifiers covering ALL utility content types (substations, engineering drawings, regulatory filings, incident reports, customer correspondence, vendor contracts, board materials); achieve 85-90% accuracy | 15-20 production trainable classifiers, 85-90% accuracy validation, classification coverage for niche content types |
| **3. Legacy Archive Classification** | Month 6-14 | Systematically classify remaining unclassified data including legacy archives, retired systems exports, complex engineering documents, historical records; deploy dedicated steward teams; implement quality assurance workflows | 300K-500K legacy files classified, unclassified data reduced to 10-15%, archive classification playbook |
| **4. IoT/OT Data Classification** | Month 10-18 | Deploy Purview to AMI streaming data via Azure Stream Analytics/Event Hub; classify SCADA historian metadata (OSIsoft PI, GE Proficy); label DER device data; extend classification to time-series operational data | AMI data streams classified (10M-50M devices), SCADA historian governance, IoT/OT classification framework operational |
| **5. Real-Time Classification at Ingestion** | Month 14-22 | Implement auto-labeling at data creation points: M365 document creation, email composition, database record inserts, SharePoint uploads, IoT data ingestion; embed classification in all workflows | Real-time auto-labeling operational across all systems, 95%+ of new data auto-classified within minutes of creation |
| **6. File Share Decommissioning** | Month 16-26 | Complete final file share migration (remaining 10-30%); decommission legacy file servers; implement "no new file shares" architectural controls; redirect users to M365 SharePoint/OneDrive | 90-95% of data migrated to M365, legacy file servers decommissioned, architectural controls preventing new file shares |
| **7. Final Coverage Push & Optimization** | Month 24-32 | Execute final manual classification campaigns for edge cases (<10% unclassified data); optimize all ML models for 95%+ accuracy; audit entire data estate; achieve 90-95% comprehensive coverage | 90-95% enterprise coverage validated, 95%+ classification accuracy, final audit report |
| **8. BAU Transition & Sustaining Operations** | Month 30-36 | Transition from project to business-as-usual operations; establish sustaining team (6-8 FTE); implement continuous monitoring and optimization; create self-service steward tools; measure ongoing auto-classification rate (target 95%+ for new data) | BAU operations model, sustaining team operational, continuous improvement framework, center of excellence established |

### Staffing Plan

| Role | FTE | Responsibilities | Duration |
|------|-----|------------------|----------|
| **Executive Sponsor** | 0.1 | CDO or CISO providing strategic direction, board reporting, organizational alignment | 36 months |
| **Program Director** | 1.0 | Enterprise governance program leadership, strategic partnerships, industry engagement | 36 months |
| **Data Governance Managers** | 1.5 | Policy management, stewardship network expansion (2 managers for scale), process maturity | 36 months |
| **Purview Platform Lead** | 1.0 | Advanced Purview capabilities, custom ML models, platform optimization, innovation pilots | 36 months |
| **Technical Architects** | 2.0 | IoT/OT integrations, zero-trust architecture, AI/ML governance, multi-party data sharing infrastructure | 36 months |
| **Business Analysts** | 2.5 | Cross-functional workflow automation, use case enablement, analytics support, steward training | 36 months |
| **Data Stewards (Business)** | 3.5 | Mature embedded network: 25-30 part-time stewards (0.3-0.4 FTE each) across all business units | 36 months |
| **IoT/OT Integration Lead** | 1.0 | AMI/SCADA data governance, edge classification, OT/IT convergence, historian integration | 24 months |
| **AI/ML Governance Lead** | 0.75 | AI ethics framework, model governance, privacy-enhancing technologies, federated learning | 24 months (months 12-36) |
| **Security/Zero-Trust Lead** | 1.0 | Dynamic access controls, adaptive DLP, UEBA integration, insider risk management | 30 months |
| **Privacy/Legal SME** | 0.75 | Privacy program, regulatory compliance, data ethics, vendor agreements | 36 months |
| **Migration & Decommissioning Mgr** | 0.75 | Complete file share migration, legacy system decommissioning, M365 architectural standards | 20 months (months 1-20) |
| **Data Catalog/Lineage Lead** | 0.75 | Purview Data Map optimization, lineage with sensitivity propagation, metadata strategy | 30 months |
| **Change Management Team** | 1.5 | Culture transformation, continuous training, adoption measurement, center of excellence | 36 months |
| **Quality Assurance** | 0.5 | Audit, compliance validation, accuracy optimization, maturity assessment | 30 months |
| **Strategic Initiatives Lead** | 0.5 | Data monetization, multi-party sharing, industry partnerships, thought leadership | 18 months (months 18-36) |
| **Total Core Team** | **19.0 FTE** | Slightly larger than Option 2 due to advanced capabilities (IoT/OT, AI/ML, strategic initiatives) | |
| **Sustaining Team (Year 4+)** | **6-8 FTE** | Smaller sustaining team due to automation and self-service capabilities; platform operations, stewardship support, continuous improvement | Ongoing |

### Technology Requirements

**Purview Advanced Capabilities** (Fully Utilize ALL Licensed Modules):
- **Purview Information Protection**: Advanced trainable classifiers for utility-specific content, contextual classification policies (ALREADY LICENSED - optimize and expand)
- **Purview DLP**: Adaptive protection based on user risk score, device compliance, location; behavior-based policies (ALREADY LICENSED - advanced configuration)
- **Purview Insider Risk Management**: Comprehensive deployment with priority user groups, risky activity indicators (ALREADY LICENSED - full activation)
- **Purview Communication Compliance**: Regulatory communications monitoring, customer interaction compliance (ALREADY LICENSED - expand use cases)
- **Purview Records Management**: Complete lifecycle management, disposition workflows, regulatory retention automation (ALREADY LICENSED - full deployment)
- **Purview eDiscovery Premium**: Advanced analytics, machine learning, case management for regulatory inquiries (ALREADY LICENSED - operationalize)
- **Purview Audit Premium**: Long-term audit retention, advanced threat detection (ALREADY LICENSED - full configuration)

**IoT/OT Integration** (Months 12-24):
- **Azure Stream Analytics**: Classification of AMI streaming data at ingestion (included in Azure consumption pricing)
- **Azure Event Hub/IoT Hub**: Edge device integration with sensitivity labeling (Azure consumption pricing)
- **Purview Data Map for OSIsoft PI/Historian**: Custom connectors for SCADA time-series data (development effort, no licensing)
- **Azure Arc**: Hybrid/edge governance for distributed OT environments (included in Azure, configuration only)

**Zero-Trust & Advanced Security** (Months 16-28):
- **Azure AD Conditional Access**: Dynamic policies based on sensitivity labels (ALREADY LICENSED in M365 E5)
- **Microsoft Defender for Cloud Apps**: CASB with label-aware policies, shadow IT discovery (ALREADY LICENSED)
- **Azure Privileged Identity Management (PIM)**: Just-in-time access for Restricted data (ALREADY LICENSED)
- **Microsoft Sentinel**: UEBA integration with Purview security signals (Azure consumption pricing if not deployed; or existing SIEM integration)

**AI/ML & Advanced Analytics** (Months 20-32):
- **Azure Machine Learning**: Model training on classified datasets, privacy controls, bias monitoring (Azure consumption pricing)
- **Azure Synapse Analytics or Databricks**: Data clean rooms, secure multi-party computation, federated analytics with Purview integration (Azure/Databricks licensing)
- **Power BI Premium**: Sensitivity label propagation, automatic content classification, row-level security (upgrade from Pro if needed: ~$5K/user/year for key users)
- **Privacy-enhancing technologies**: Differential privacy libraries, synthetic data generation (open-source or third-party tools: $50K-$150K)

**Key Differentiator**: This option maximizes existing M365 E5/Purview investment. New costs are primarily Azure consumption for IoT/analytics use cases and specialized AI/ML tools.

### Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| **Comprehensive Coverage** | **90-95% of ALL data classified** across M365, file shares, databases, IoT/OT streams, legacy archives | Enterprise-wide Purview Data Map audit + comprehensive sampling (5000+ files quarterly across all sources) |
| **Total Classification Volume** | 2M-3M+ files/records classified (cumulative across all phases) | Purview classification volume tracking across all data sources and methods |
| **Advanced Trainable Classifiers** | 15-20 utility-specific ML models operational with 85-90% accuracy covering all content types | ML model performance monitoring + validation testing for each classifier |
| **Automated Classification Dominance** | 95%+ of NEW data auto-classified at creation/ingestion with <5% requiring manual intervention | Real-time classification monitoring + manual classification request tracking |
| **Classification Accuracy (Optimized)** | 95%+ for M365/file shares; 90%+ for databases; 85-90% for IoT/streaming data | Statistical sampling validation (5000+ items per quarter) with error analysis |
| **Legacy Archive Remediation** | 100% of legacy archives classified; zero critical unclassified data remaining | Legacy data inventory completion + audit of high-risk unclassified data |
| **IoT/OT Coverage** | 10M-50M AMI devices with classified data streams; SCADA historian metadata classified; DER device data labeled | IoT platform telemetry + historian scan reports + DER data governance validation |
| **File Share Elimination** | 90-95% of file share data migrated to M365; legacy file servers decommissioned | Infrastructure decommissioning tracking + M365 storage reports |
| **Unclassified Data Minimization** | Reduce unclassified data to <5-10% (edge cases, data queued for retirement, non-sensitive public data) | Quarterly unclassified data inventory + gap analysis |
| **Steward Network Scale** | 25-30 trained stewards operational; 300K-500K files manually classified with 95%+ quality | Steward performance dashboards + quality audit results |
| **BAU Transition** | Sustaining team operational (6-8 FTE); 95%+ of ongoing classification automated; <5% manual effort | BAU operations metrics + team resource tracking + auto-classification rate monitoring |
| **Regulatory Compliance** | Zero NERC CIP, FERC, or state privacy law findings related to data classification/protection | Annual regulatory audit results + compliance validation |

### Budget Range Estimate

| Category | Low Estimate | High Estimate | Notes |
|----------|--------------|---------------|-------|
| **Software/Tools (36 months)** | $100K | $300K | Minimal new licensing (Purview ALREADY LICENSED); Power BI Premium upgrades, PETs tools, specialized AI governance tools |
| **Azure Cloud Consumption** | $250K | $500K | IoT/AMI data processing, Azure ML compute, Stream Analytics, Synapse/Databricks for data clean rooms (consumption-based) |
| **Infrastructure** | $100K | $175K | Scanner scaling, IoT edge devices, SCADA connector infrastructure, network/security enhancements |
| **Professional Services** | $450K | $850K | Microsoft partner for advanced Purview (trainable classifiers, IoT integration, zero-trust), AI/ML governance design (20-30 weeks) |
| **Internal Labor** | $2.85M | $3.8M | 19.0 FTE blended rate over 36 months ($85K-$110K average loaded) |
| **Migration & Decommissioning** | $200K | $350K | Complete file share migration (final 30%), legacy system decommissioning, data cleanup |
| **Training & Change Mgmt** | $200K | $350K | Culture transformation, center of excellence, continuous training, advanced user enablement |
| **Consulting & Advisory** | $200K | $400K | AI ethics advisor, privacy counsel, multi-party data sharing legal, maturity assessments, industry benchmarking |
| **Innovation & Pilots** | $150K | $300K | Data marketplace pilot, secure multi-party computation POC, federated learning experiments, PETs evaluation |
| **Contingency (15%)** | $668K | $1.13M | IoT/OT integration complexity, AI/ML use case development, organizational change challenges |
| **Total 36-Month Budget** | **$5.2M** | **$8.2M** | 40-50% savings vs. greenfield; if building on Option 2, subtract $1.0M-$1.5M for completed work |

**Ongoing Annual Costs (Year 4+)**: $650K-$950K (Purview licensing in M365 E5; Azure consumption ~$150K/year; sustaining team 6-8 FTE; continuous innovation)

**Expected ROI Sources**:
- **Regulatory compliance & risk avoidance**: $3M-$6M over 3 years (NERC CIP audit findings avoidance, data breach prevention, privacy law compliance)
- **Operational efficiency**: $2M-$4M (file share decommissioning savings, reduced data storage costs, productivity from self-service access)
- **Cyber insurance premium reduction**: $300K-$600K annually (due to mature governance and zero-trust controls)
- **Strategic value creation**: $1M-$3M (AI/ML use cases enabled, DER integration revenue, multi-party data partnerships, customer analytics monetization)
- **Total Expected Value**: $6M-$13M over 3 years = **115-160% net ROI**

---

## Utility-Specific Implementation Considerations

### Current State Advantages
- **Existing Purview Deployment**: Platform already deployed reduces implementation risk and timeline; focus on configuration vs. installation
- **Defined Classification Framework**: Taxonomy already established eliminates design debates; immediate operationalization possible
- **PII Definitions in Place**: Existing PII definitions in core systems provide templates for extension to unmanaged data
- **Partial M365 Migration**: Some data already in managed environment; lessons learned inform expansion strategy
- **Regulatory Pressure as Catalyst**: NERC CIP, customer data protection requirements provide clear business case for operationalization

### Hybrid Environment Management
- **Dual-Mode Governance**: Must maintain governance across M365 (cloud) and legacy file shares (on-premises) during transition
- **Purview Strengths**: Native M365 integration (Information Protection, DLP) provides seamless governance; scanner-based approach extends to on-premises
- **Migration Prioritization**: Use Purview scanning to identify high-risk file shares (BCSI, PII) for priority migration
- **Decommissioning Strategy**: Establish clear criteria for file share retirement to prevent governance drift
- **Change Freeze Exceptions**: Plan for operational needs (storm restoration, emergency operations) where governance enforcement may be temporarily relaxed

### Regulatory Alignment
- **NERC CIP-011**: Purview capabilities directly support BCSI identification, labeling, and protection requirements
- **FERC**: Classification enables power market data confidentiality and proper handling of transmission planning data
- **State Privacy Laws**: Purview DLP and Information Protection address emerging state requirements (CPRA, VCDPA) for customer data
- **Critical Infrastructure**: Purview Restricted labels applied to substation locations, SCADA configurations, physical security data

### Operational Technology (OT) Considerations
- **Non-Intrusive Approach**: Purview scanning of SCADA documentation, engineering drawings, and procedures does NOT touch real-time operational systems
- **Database Connectors**: Purview Data Map can classify metadata in historians (OSIsoft PI, GE Proficy) without impacting OT performance
- **OT/IT Convergence**: Options 2-3 position for AMI/IoT governance as utility modernizes grid infrastructure
- **Safety-First Messaging**: Frame governance as risk reduction for critical infrastructure protection, not IT compliance burden

### Key Utility Systems Integration Priority (Adjusted for Current State)
1. **M365 Environment** (Month 1-4): Activate Purview Information Protection, DLP - HIGH PRIORITY, quick win
2. **Priority File Shares** (Month 2-6): Scan top 15 shares with BCSI, customer PII, confidential contracts - HIGH PRIORITY, risk reduction
3. **Customer Information System (CIS)** (Month 6-10): Extend existing PII definitions via Purview Data Map scanning
4. **Meter Data Management System (MDMS)** (Month 6-10): AMI data, interval usage classification
5. **GIS** (Month 8-12): Critical infrastructure location data, substation mapping (Restricted classification)
6. **Document Management / Engineering Systems** (Month 10-14): SCADA procedures, engineering drawings, regulatory filings
7. **SCADA Historians** (Option 3): Time-series operational data classification (non-intrusive metadata approach)

### Organizational Change Management (Current State Focus)
- **ROI Messaging**: Emphasize maximizing existing Purview investment vs. new spending; "use what we already paid for"
- **User Adoption Challenge**: Deployed technology with low adoption requires behavior change focus, not tool selection
- **M365 Migration Alignment**: Coordinate governance rollout with ongoing M365 migration efforts (joint communications, shared project governance)
- **Quick Win Strategy**: Early DLP policy successes (blocking PII in external emails) build credibility for expanded program
- **Executive Sponsorship**: CISO and IT leadership must champion "finishing what we started" narrative

### Risk Mitigation Strategies (Tailored to Expansion Initiative)
- **Phased File Share Scanning**: Start with 10-15 priority shares to prove value before enterprise-wide deployment
- **Policy Tuning Period**: Implement DLP in "monitor mode" (policy tips, no blocking) for 30-60 days before enforcement
- **Migration Before Enforcement**: Don't apply strict access controls to file shares slated for near-term M365 migration
- **Helpdesk Readiness**: Ensure IT support prepared for Purview-related user questions before broad rollout
- **Operational Exemptions**: Create process for temporary classification bypasses during emergencies (storm restoration, major outages)

---

## Decision Framework: Selecting the Right Option

### Choose Option 1 (Data Discovery & Automated Classification Kickstart, 6-12 Months) if:
- Starting from 10-15% classification coverage and need to demonstrate rapid improvement
- Budget constrained ($750K-$1.2M) but under regulatory pressure to show progress
- Need quick wins to build executive support for expanded classification program
- Want to prove value of automated classification before committing to enterprise-wide effort
- High-priority data (NERC CIP BCSI, customer PII) is well-known and can be targeted first
- **Best fit**: Utilities needing to move from "labels defined" to "priority data labeled" with measurable risk reduction in 12 months
- **Expected outcome**: 40-60% coverage on priority data; foundation for enterprise expansion

### Choose Option 2 (Enterprise Classification Scale-Up, 12-18 Months) if:
- Option 1 complete (40-60% coverage) OR can accelerate foundation work in months 1-4
- Budget availability $1.8M-$2.8M to tackle comprehensive enterprise classification
- Regulatory drivers (NERC CIP audits, state privacy law compliance) require broad coverage across all data sources
- Ready to invest in trainable classifiers for utility-specific content beyond generic PII/sensitive info types
- Operational databases (CIS, MDMS, GIS) are documented and ready for scanning
- **Best fit**: Utilities committed to systematic elimination of unclassified data across enterprise
- **Expected outcome**: 70-85% coverage; majority of data classified with advanced automation

### Choose Option 3 (Comprehensive Coverage & Advanced Automation, 24-36 Months) if:
- Options 1-2 complete (70-85% coverage) OR high organizational maturity to accelerate
- Budget availability $5.2M-$8.2M with multi-year executive commitment
- Strategic need for near-complete coverage (90-95%) including IoT/OT, legacy archives, edge cases
- Grid modernization initiatives (AMI deployment, DER integration) require IoT data classification
- Ready to transition from "classification project" to "classification-by-design" BAU operations
- **Best fit**: Utilities pursuing industry-leading maturity with automated classification embedded in all workflows
- **Expected outcome**: 90-95% coverage; self-sustaining operations with 95%+ of new data auto-classified

### Recommended Approach Given Current State

**The Critical Reality**: You have labels defined but 90%+ of data is unclassified. This is an EXECUTION challenge, not a design challenge.

**START WITH OPTION 1 (6-12 months)** to:
1. **Discover where sensitive data actually lives** through systematic scanning (you can't protect what you haven't found)
2. **Configure Purview automation** to classify 300K-500K files without manual effort
3. **Achieve 40-60% coverage on crown jewels** (NERC CIP BCSI, customer PII, confidential financials)
4. **Prove automation ROI** and build business case for enterprise expansion

**THEN PROGRESS TO OPTION 2 (months 12-30)** with:
- Classification coverage doubled from 40-60% to 70-85%
- Trainable classifiers handling utility-specific content (SCADA procedures, engineering documents)
- Operational databases classified (CIS, MDMS, GIS)
- Unclassified data reduced to manageable 15-30%

**CONSIDER OPTION 3 (months 24-48)** if:
- Strategic initiatives require near-complete coverage (IoT/OT governance, AI/ML, multi-party data sharing)
- Committed to achieving 90-95% coverage and eliminating classification backlog
- Ready to embed classification-by-design in all data workflows

**Key Message**: The gap is not technology or taxonomy - it's systematic application of labels to millions of files. Success requires Purview automation expertise, data discovery discipline, and realistic expectations about accuracy/manual remediation needs.

---

## Next Steps & Recommendations

### Immediate Actions (Weeks 1-4)

1. **Baseline Current Classification Coverage**:
   - Run Purview Data Map reports to quantify current classification coverage (likely 10-15%)
   - Identify what IS currently labeled (where, by whom, accuracy) vs. vast unclassified estate
   - Document existing auto-labeling policies (if any) and their effectiveness
   - Inventory file shares: how many shares, total file counts, estimated sensitive data volume
   - Assess M365 tenant: SharePoint sites, OneDrive accounts, Teams - what percentage has labels applied?

2. **Data Discovery Pilot**:
   - Deploy Purview Data Map scanner to 3-5 pilot file shares (high-risk: BCSI, customer PII, financials)
   - Run discovery scan using built-in sensitive info types to understand what's actually there
   - Generate sensitivity heatmap: which shares contain most PII, BCSI, confidential data?
   - Use results to validate (or challenge) assumptions about where sensitive data resides

3. **Executive Alignment**:
   - Present the "defined vs. applied" gap reality to CISO, CIO, and business unit leaders
   - Frame as execution challenge: "We have the taxonomy and tools; now we need to apply labels to millions of files"
   - Emphasize realistic coverage targets (Option 1: 40-60%, Option 2: 70-85%, Option 3: 90-95%)
   - Select option based on budget, urgency, and tolerance for remaining unclassified data
   - Secure executive sponsor who understands this is multi-year automation and stewardship effort

4. **Purview Expertise Assessment**:
   - Evaluate current team's Purview configuration skills (auto-labeling policies, trainable classifiers, Data Map scanners)
   - Identify need for Purview Policy Analyst role (CRITICAL for success)
   - Engage Microsoft FastTrack or partner for Purview automation best practices and configuration guidance

### Months 1-3 (Kickoff)

1. **Program Setup**:
   - Recruit CRITICAL ROLE: Purview Policy Analyst with auto-labeling and scanner configuration expertise
   - Form steering committee with IT, Security, Legal, Business Unit representatives
   - Draft project charter emphasizing LABEL APPLICATION at scale (not framework design)
   - Establish success metrics: % data classified, classification accuracy, auto vs. manual ratio

2. **Purview Auto-Labeling Configuration**:
   - Map existing classification taxonomy to Purview sensitivity labels (labels already defined, now configure in Purview)
   - Build 8-12 auto-labeling policies using sensitive info types (SSN, credit cards, employee IDs, account numbers)
   - Configure keyword and pattern-based rules for BCSI, confidential contracts, regulatory filings
   - Test policies on pilot dataset (10K files) and tune for 85%+ accuracy

3. **Data Discovery Expansion**:
   - Deploy Purview Data Map scanners to top 15-20 priority file shares and M365 environments
   - Execute discovery scans to inventory data and identify sensitive content
   - Create comprehensive sensitivity heatmap showing where PII, BCSI, confidential data resides
   - Quantify unclassified data challenge (file counts, GB, sensitivity levels)

4. **Change Management Foundation**:
   - Develop communication plan: "Applying our classification framework to protect our data"
   - Create M365 user training on manual labeling (for when automation can't reach)
   - Establish helpdesk support for classification questions and policy exceptions

### Ongoing Governance

- **Monthly**: Program team status reviews, adoption metrics tracking, issue resolution
- **Quarterly**: Steering committee reviews with go/no-go decisions for next phases; present ROI metrics (risk reduction, adoption progress)
- **Semi-Annual**: Maturity assessment; adjust roadmap based on lessons learned, regulatory changes, strategic shifts
- **Annual**: Executive reporting on program value; funding requests for next option phase

### Critical Success Factors (Tailored to Label Application Challenge)

1. **Discovery Before Classification**: Cannot apply labels to data you haven't found - systematic scanning and inventory is Phase 1
2. **Automation First, Manual Second**: Target 80-90% automated classification through Purview policies; reserve stewards for high-value edge cases
3. **Purview Configuration Expertise**: Success hinges on Purview Policy Analyst who can build/tune auto-labeling policies and trainable classifiers
4. **Realistic Coverage Expectations**: 40-60% in 12 months is success; 100% coverage is unrealistic - accept that some data will remain unclassified
5. **Accuracy Over Speed**: 85% classification accuracy with 15% false positives is acceptable; 95%+ accuracy takes longer but reduces manual remediation
6. **Crown Jewels Prioritization**: Focus first on NERC CIP BCSI, customer PII, confidential financials - don't try to classify everything at once
7. **User Adoption for Sustainability**: Automated classification handles backlog; user training ensures NEW data gets labeled going forward
8. **Business Value Framing**: Measure success by % of sensitive data NOW PROTECTED (not % of framework designed or tools deployed)

---

**Document Version**: 3.0 (CRITICAL REVISION: Label Application at Scale - "Taxonomy Exists But Execution Doesn't")
**Last Updated**: 2025-12-05
**Owner**: Data Governance Program Office
**Review Cycle**: Quarterly or upon significant regulatory/strategic changes

**Key Revisions in Version 3.0 (CRITICAL UPDATE)**:
- **Corrected Current State Assessment**: Clarified that labels are DEFINED but NOT APPLIED - 90%+ of data remains unclassified (not "low adoption" but "no execution")
- **Refocused All Three Options on Label Application**: Changed from "Purview activation" to "data discovery and automated classification at scale"
- **Discovery-First Approach**: Emphasized systematic data discovery and inventory as prerequisite to classification (can't label what you haven't found)
- **Realistic Coverage Targets**: Set honest expectations - Option 1: 40-60%, Option 2: 70-85%, Option 3: 90-95% (not 100%)
- **Purview Configuration Emphasis**: Highlighted need for Purview Policy Analyst expertise in auto-labeling policies, trainable classifiers, and Data Map scanners
- **Automation-Centric Staffing**: Revised staffing plans to prioritize automation specialists, classification quality analysts, and discovery specialists over migration managers
- **Crown Jewels Prioritization**: Structured phases to start with high-risk data (NERC CIP BCSI, customer PII) rather than enterprise-wide deployment
- **Success Metrics Overhaul**: Changed from "adoption %" to "classification coverage %", "files classified", "accuracy %", and "unclassified data reduction"
- **Crawl-Walk-Run Implementation**: Restructured phases to reflect: discover → configure automation → classify priority data → expand coverage → optimize accuracy
- **Execution Gap Messaging**: Reframed entire plan around "applying existing taxonomy to actual data" vs. "expanding platform adoption"
