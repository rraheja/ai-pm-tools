# Industry Examples and Use Case Patterns

This reference provides detailed industry-specific examples and real-world use case patterns. Load this file when you need deeper context or industry-specific guidance beyond the core framework in SKILL.md.

---

## Detailed Quadrant Examples by Industry

### Financial Services

**Q1: Know-how + Human Intervention (BI/Diagnostic AI)**
- **Credit Risk Assessment Dashboards**: AI analyzes credit applications and assigns risk scores, but loan officers make final approval decisions. The AI provides insights on default probability, income stability, and debt ratios, but humans interpret results considering qualitative factors like industry trends and personal circumstances.
- **Anti-Money Laundering Detection**: AI flags suspicious transaction patterns and assigns risk levels, but compliance analysts investigate and determine whether to file Suspicious Activity Reports (SARs). Human expertise is critical for understanding context and regulatory nuances.
- **Investment Research Tools**: AI analyzes market data, company financials, and news sentiment to generate investment recommendations, but portfolio managers make final trading decisions considering client goals, risk tolerance, and market conditions.

**Q2: Know-how + Automation (In-context AI)**
- **Fraud Detection Alerts**: Real-time AI system automatically flags and blocks potentially fraudulent transactions based on spending patterns, location, and merchant risk. Customers only intervene if legitimate transactions are blocked.
- **Personalized Financial Advice**: Banking app automatically provides tailored savings recommendations, spending insights, and goal tracking based on transaction history. Users consume insights without validating each recommendation.
- **Dynamic Credit Limits**: AI continuously adjusts credit limits based on payment history, income changes, and credit utilization patterns without human review for each adjustment.

**Q3: Actionable + Human Intervention (Fixed Step Workflows)**
- **Loan Application Pre-Approval**: AI generates loan pre-approval letters with recommended terms based on applicant data, but underwriters review and approve before sending. The AI can't independently commit the institution to lending terms.
- **Compliance Report Generation**: AI drafts regulatory reports by analyzing transactions and flagging potential issues, but compliance officers review, edit, and submit reports. Human validation ensures regulatory accuracy.
- **Customer Communication Drafts**: AI creates personalized email responses to customer inquiries based on account history and issue type, but relationship managers review and approve before sending.

**Q4: Actionable + Automation (Fully Autonomous Agents)**
- **Automated Fraud Prevention**: AI independently blocks transactions identified as fraudulent, issues new cards, and notifies customers—all without human intervention. Operates 24/7 protecting millions of accounts.
- **Robo-Advisors**: Autonomous investment platforms that automatically rebalance portfolios, execute trades, and adjust asset allocation based on market conditions and client goals without advisor approval.
- **Trading Algorithms**: High-frequency trading systems that analyze market data and execute thousands of trades per second based on predefined strategies without human oversight.

---

### Healthcare

**Q1: Know-how + Human Intervention (BI/Diagnostic AI)**
- **Medical Image Analysis**: AI analyzes X-rays, MRIs, and CT scans to detect abnormalities and assign diagnostic probabilities, but radiologists validate findings and make final diagnoses. Combines AI pattern recognition with clinical expertise.
- **Clinical Decision Support**: AI reviews patient symptoms, medical history, and lab results to suggest diagnoses and treatment options, but physicians make final care decisions considering patient preferences and contraindications.
- **Patient Risk Stratification**: AI predicts readmission risk, deterioration likelihood, and complication probability, but care coordinators decide intervention strategies and resource allocation.

**Q2: Know-how + Automation (In-context AI)**
- **Patient Monitoring Systems**: Real-time AI continuously monitors vital signs, automatically alerts nurses when abnormalities detected, and predicts patient deterioration. Operates autonomously in ICUs and step-down units.
- **Chronic Disease Management**: AI tracks glucose levels, medication adherence, and symptom patterns for diabetic or cardiac patients, automatically providing personalized lifestyle recommendations and early warning alerts.
- **Clinical Research Matching**: AI continuously scans clinical trial databases and automatically identifies patients who match eligibility criteria, notifying research coordinators of potential candidates.

**Q3: Actionable + Human Intervention (Fixed Step Workflows)**
- **Clinical Documentation Assistance**: AI listens to patient encounters and generates draft clinical notes including diagnoses, treatments, and billing codes, but physicians review and approve before submitting to EHR.
- **Treatment Plan Generation**: AI creates draft care plans with medication recommendations, therapy schedules, and follow-up timelines based on evidence-based protocols, but clinicians review and customize before implementation.
- **Prior Authorization Drafting**: AI generates insurance prior authorization requests with supporting medical documentation, but billing specialists review and submit to ensure accuracy and completeness.

**Q4: Actionable + Automation (Fully Autonomous Agents)**
- **Appointment Scheduling and Reminders**: AI chatbot independently handles appointment booking, rescheduling, cancellations, and sends automated reminders via SMS/email. Operates 24/7 without staff involvement.
- **Prescription Refill Automation**: AI automatically processes routine prescription refill requests, verifies eligibility, submits to pharmacy, and notifies patients—no pharmacist review needed for non-controlled medications.
- **Supply Chain Restocking**: AI monitors medical supply usage, predicts demand, and automatically orders replenishments from vendors when inventory reaches reorder points.

---

### Retail & E-commerce

**Q1: Know-how + Human Intervention (BI/Diagnostic AI)**
- **Customer Segmentation Analysis**: AI analyzes purchase history, browsing behavior, and demographics to create customer segments and predict lifetime value, but marketing managers design campaigns and targeting strategies.
- **Assortment Planning Recommendations**: AI suggests optimal product mix for each store location based on local demographics, sales history, and trends, but merchandisers make final assortment decisions.
- **Price Optimization Analysis**: AI analyzes competitor pricing, demand elasticity, and margin targets to recommend pricing strategies, but pricing managers approve and implement changes.

**Q2: Know-how + Automation (In-context AI)**
- **Product Recommendations**: E-commerce platform automatically displays personalized product suggestions based on browsing history, past purchases, and similar customer behavior. No human review of each recommendation.
- **Inventory Optimization**: AI continuously predicts demand and automatically adjusts safety stock levels, reorder points, and allocation across warehouses without requiring planner approval.
- **Dynamic Content Personalization**: Website automatically adapts homepage layout, featured products, and promotional banners based on individual user preferences and behavior patterns.

**Q3: Actionable + Human Intervention (Fixed Step Workflows)**
- **Product Description Generation**: AI creates product descriptions, SEO-optimized content, and marketing copy from product specifications, but content editors review and approve before publishing.
- **Visual Merchandising Mockups**: AI generates store layout designs and product placement recommendations, but visual merchandisers review and finalize before implementation.
- **Promotional Campaign Drafts**: AI designs promotional email campaigns with personalized offers and timing, but marketing managers review, adjust, and schedule for deployment.

**Q4: Actionable + Automation (Fully Autonomous Agents)**
- **Customer Service Chatbots**: AI independently handles product questions, order status inquiries, returns processing, and issue resolution without agent escalation for majority of interactions.
- **Automated Order Fulfillment**: AI routes orders to optimal warehouse, generates pick lists, directs robotic systems, and updates tracking information—all without human intervention.
- **Dynamic Pricing Engines**: AI automatically adjusts prices in real-time based on demand, inventory levels, competitor pricing, and customer segments across thousands of SKUs.

---

### Manufacturing

**Q1: Know-how + Human Intervention (BI/Diagnostic AI)**
- **Predictive Maintenance Dashboards**: AI analyzes sensor data from equipment to predict failure probability and recommend maintenance schedules, but maintenance managers decide timing and resource allocation.
- **Quality Root Cause Analysis**: AI identifies patterns in defect data to suggest root causes and quality improvement opportunities, but quality engineers validate hypotheses and implement corrective actions.
- **Production Planning Optimization**: AI simulates production schedules considering demand forecasts, capacity constraints, and material availability, but production planners make final scheduling decisions.

**Q2: Know-how + Automation (In-context AI)**
- **Real-Time Quality Monitoring**: Computer vision AI continuously inspects products on production line, automatically categorizes defects, and generates real-time quality dashboards without inspector validation.
- **Energy Consumption Optimization**: AI monitors equipment energy usage, predicts consumption patterns, and automatically provides recommendations for efficiency improvements without requiring approval.
- **Supply Chain Visibility**: AI tracks shipments, predicts delays, and automatically alerts stakeholders of potential disruptions across the entire supply chain in real-time.

**Q3: Actionable + Human Intervention (Fixed Step Workflows)**
- **Production Schedule Generation**: AI creates optimized production schedules balancing demand, capacity, and changeover costs, but production managers review and approve before implementation.
- **Work Order Creation**: AI generates work orders with routing, materials list, and time estimates based on production requirements, but planners review and release to shop floor.
- **Maintenance Work Instructions**: AI drafts step-by-step maintenance procedures with safety protocols and parts requirements, but maintenance supervisors review and approve.

**Q4: Actionable + Automation (Fully Autonomous Agents)**
- **Autonomous Mobile Robots**: Self-driving robots transport materials between production stations, adapt routes based on obstacles, and charge themselves without human direction.
- **Automated Material Ordering**: AI monitors production schedules and inventory, automatically places purchase orders with suppliers when materials reach reorder points.
- **Self-Adjusting Production Systems**: AI automatically adjusts machine parameters (speed, temperature, pressure) in real-time to maintain quality specifications and maximize throughput.

---

### Technology & SaaS

**Q1: Know-how + Human Intervention (BI/Diagnostic AI)**
- **Code Quality Analysis**: AI reviews code commits, identifies potential bugs, security vulnerabilities, and technical debt, but developers decide what to fix and how to refactor.
- **Customer Health Scoring**: AI analyzes usage patterns, support tickets, and engagement to predict churn risk, but customer success managers design retention strategies.
- **Infrastructure Cost Analysis**: AI examines cloud resource usage and recommends optimization opportunities, but DevOps engineers approve and implement changes.

**Q2: Know-how + Automation (In-context AI)**
- **Anomaly Detection and Alerting**: AI continuously monitors application performance, automatically detects anomalies, and alerts on-call engineers without human validation of each alert.
- **User Behavior Analytics**: AI automatically tracks feature usage, identifies adoption patterns, and surfaces insights to product teams without requiring analyst review.
- **Automated Threat Intelligence**: AI continuously scans for security threats, updates threat databases, and adapts defense mechanisms autonomously.

**Q3: Actionable + Human Intervention (Fixed Step Workflows)**
- **Code Generation Assistants**: AI generates code functions, tests, and documentation from natural language descriptions, but developers review and approve before merging.
- **Automated Test Generation**: AI creates test cases covering edge cases and potential failure modes, but QA engineers review test coverage and approve test suites.
- **Documentation Drafting**: AI generates API documentation, user guides, and release notes from code changes, but technical writers review and publish.

**Q4: Actionable + Automation (Fully Autonomous Agents)**
- **Customer Support Chatbots**: AI independently resolves technical issues, password resets, billing questions, and feature guidance without agent escalation.
- **Auto-Scaling Infrastructure**: AI automatically provisions and de-provisions cloud resources based on traffic patterns and performance requirements.
- **Continuous Integration/Deployment**: AI runs automated tests, identifies issues, and automatically deploys code to production when all checks pass.

---

## Real-World Use Case Examples with Details

### Example 1: Healthcare - Ambient Clinical Documentation (Q3)

**Company**: Kaiser Permanente (real implementation)

**Problem**: Physicians spend 2+ hours daily on clinical documentation, reducing patient face time and causing burnout.

**AI Solution**: Ambient AI listens to patient encounters, understands context, and generates structured clinical notes including:
- Chief complaint and history of present illness
- Review of systems and physical examination
- Assessment and diagnosis codes
- Treatment plan and medication orders

**Why Q3 (Actionable + Human Intervention)**:
- **Actionable**: AI creates tangible outputs (complete clinical notes)
- **Human Intervention**: Physician MUST review and approve before submitting to EHR. AI cannot independently create medical records.

**Results**: 50% reduction in documentation time, improved physician satisfaction, maintained clinical accuracy with human oversight.

**Key Learning**: High-stakes outputs (medical records) require human validation even when AI quality is high. Regulatory and liability considerations keep this in Q3, not Q4.

---

### Example 2: Retail - Netflix Recommendations (Q2)

**Company**: Netflix

**Problem**: Users overwhelmed by content library, struggle to find relevant shows/movies, leading to reduced engagement.

**AI Solution**: Recommendation engine analyzes viewing history, ratings, browsing behavior, and similar user patterns to automatically suggest personalized content.

**Why Q2 (Know-how + Autonomous)**:
- **Know-how**: AI provides recommendations and predictions (what to watch)
- **Autonomous**: System operates independently; users simply consume suggestions without validating accuracy

**Results**: 80% of viewing comes from recommendations, increased engagement, reduced churn.

**Key Learning**: Low-stakes insights (content suggestions) can operate autonomously. Users naturally self-correct by simply choosing different content.

---

### Example 3: Financial Services - Robo-Advisors (Q4)

**Company**: Betterment, Wealthfront

**Problem**: Traditional wealth management expensive and inaccessible for smaller accounts; manual portfolio management time-consuming.

**AI Solution**: Fully autonomous investment platform that:
- Collects client goals and risk tolerance
- Selects asset allocation automatically
- Executes trades and rebalances portfolio
- Manages tax-loss harvesting
- Adjusts strategy based on market conditions

**Why Q4 (Actionable + Autonomous)**:
- **Actionable**: AI executes actual financial transactions
- **Autonomous**: Operates independently without advisor approval for each trade

**Results**: $50B+ assets under management, 0.25% fees vs. 1%+ for traditional advisors, democratized wealth management.

**Key Learning**: Heavily regulated actions (financial transactions) CAN be Q4 if proper guardrails, disclosure, and client consent are in place.

---

## Document Analysis Extraction Examples

### Example: Strategic Goal Extraction

**Source Document**: "We aim to achieve $500M in revenue by 2026 while maintaining 90% customer retention"

**Extraction Process**:
1. **Identify Goals**: Revenue growth (2.5x in 3 years), Customer retention (90%)
2. **Translate to AI Opportunities**:
   - Revenue: Sales automation, dynamic pricing, upsell recommendations
   - Retention: Churn prediction (Q1), personalized engagement (Q2), proactive support (Q4)

**Generated Use Cases**:
- "Predictive churn modeling with intervention playbooks" (Q1)
- "Automated personalized retention campaigns" (Q2)
- "AI-powered customer success chatbot" (Q4)

---

### Example: Pain Point Extraction

**Source Document**: "Support team handles 10,000 tickets/month, 60% are basic password resets taking 15 min each"

**Extraction Process**:
1. **Quantify Problem**: 6,000 password resets × 15 min = 1,500 hours/month
2. **Calculate Cost**: 1,500 hours × $30/hour = $45K/month in support costs
3. **Identify Automation Opportunity**: Self-service password reset

**Generated Use Case**:
- **Name**: "Self-Service Password Reset Assistant"
- **Quadrant**: Q4 (automates resolution without agent)
- **Value**: Save $45K/month (90% automation rate)
- **Cost**: Low (standard authentication APIs)

---

### Example: Capability Gap Analysis

**Source Document**: "We cannot provide real-time inventory visibility across 50 distribution centers"

**Extraction Process**:
1. **Gap Identified**: Lack of real-time data aggregation
2. **Consequence**: Stockouts, overstocking, poor customer experience
3. **AI Solution**: Real-time inventory optimization

**Generated Use Cases**:
- "Real-time inventory visibility dashboard" (Q1 - insights for planners)
- "Predictive restocking recommendations" (Q2 - autonomous predictions)
- "Automated transfer order generation" (Q3 - AI drafts, planners approve)

---

## Competitive Analysis Examples

### Example: Healthcare AI Competitive Intelligence

**Research Query**: "Kaiser Permanente AI investments"

**Findings**:
- Deployed ambient clinical documentation AI
- 50% reduction in physician documentation time
- Positive physician satisfaction scores

**Competitive Insights**:
- Q3 use case (assisted documentation with physician review) is proven
- Major health systems investing heavily in physician efficiency
- Ambient AI becoming table stakes for competitive physician recruitment

**Strategic Implications for User**:
- Clinical documentation is parity play, not differentiation
- Explore Q4 opportunities (autonomous) for competitive edge
- Consider patient-facing Q4 use cases instead of clinician-facing Q3

---

## Common Industry Patterns (Expanded)

### Pattern 1: High-Stakes Domains Start in Q1, Evolve to Q4

**Healthcare Journey**:
- **2015**: Diagnostic AI provides insights for physician review (Q1)
- **2018**: AI automatically flags anomalies in imaging (Q2)
- **2020**: AI drafts clinical notes for review (Q3)
- **2024**: AI autonomously handles appointment scheduling (Q4)

**Lesson**: Build trust through human-in-the-loop (Q1/Q3) before moving to autonomous (Q2/Q4).

---

### Pattern 2: Consumer-Facing Moves to Q4 Faster Than Enterprise

**Retail Evolution**:
- **Consumer**: Product recommendations (Q2) → Chatbots (Q4) in 5 years
- **Enterprise**: Inventory insights (Q1) → Automated ordering (Q4) in 10+ years

**Reason**: Consumer tolerance for AI errors higher; Enterprise stakes (financial, operational) require more validation.

---

### Pattern 3: Regulatory Constraints Lock Use Cases in Q1/Q3

**Financial Services**:
- Credit decisions legally require human accountability → Q1 (not Q2)
- Loan approvals need regulatory oversight → Q3 (not Q4)
- Fraud prevention can be autonomous → Q4 (customer protection)

**Lesson**: Regulatory environment determines quadrant, not just technical capability.

---

## When to Reference This File

Load this file when:
- User asks for **specific industry examples** beyond brief mentions in SKILL.md
- User needs **detailed use case patterns** for their industry
- User questions **why** a use case belongs in specific quadrant
- User wants **real-world validation** of approach
- User needs **competitive intelligence** examples
- User requests **document analysis walkthroughs**

**Do NOT load** for standard use case generation—SKILL.md contains sufficient guidance for 90% of scenarios.

---

*Reference Version: 1.0*
*Last Updated: October 2025*
