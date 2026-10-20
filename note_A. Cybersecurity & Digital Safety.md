# A. Cybersecurity & Digital Safety
## Capstone Project Research Ideas

### 1. X-Sentinel AI — Explainable AI-Based Cyber Threat Detection System
**Problem Statement:** Traditional intrusion detection systems may generate many false alarms and provide limited explanations for why network traffic is classified as malicious.

**Proposed Approach:** Develop a machine-learning-based intrusion detection system that classifies network traffic and uses Explainable AI (XAI), such as SHAP, to explain its predictions.

**Research Questions:**
- How do different machine learning models compare in detecting malicious network traffic?
- Does adding explainability affect detection performance?
- Can explanations help users distinguish genuine threats from false alarms?

**Potential Research Gap to Investigate:** Do existing explainable intrusion detection methods provide sufficiently accurate, stable, and useful explanations under changing network conditions?

**Candidate Datasets:** CIC-IDS2017, CSE-CIC-IDS2018.

**Evaluation Plan:** Measure precision, recall, F1-score, false-positive rate, inference time, and explanation stability. Compare models such as Logistic Regression, Random Forest, and XGBoost.

### 2. AI-Based Scam & Fraud Detection for Bangla/Banglish
**Problem Statement:** Users may struggle to identify scam messages and suspicious links, particularly when messages use Bangla, Banglish, informal spelling, or mixed-language expressions.

**Proposed Approach:** Build an AI-based system that analyzes message text and URLs to classify potentially fraudulent content and explain suspicious indicators.

**Research Questions:**
- How well do traditional machine learning models compare with multilingual transformer models?
- How does performance change between Bangla, Banglish, and mixed-language messages?
- Can combining text and URL features improve scam detection?

**Potential Research Gap to Investigate:** Are existing scam detection methods sufficiently robust to informal Bangla/Banglish language, spelling variation, and code-switching?

**Candidate Datasets:** Public SMS spam and phishing URL datasets, supplemented by a carefully labeled Bangla/Banglish dataset if feasible.

**Evaluation Plan:** Use precision, recall, F1-score, false-positive rate, and cross-language testing. Compare TF-IDF with Logistic Regression or SVM against a multilingual transformer. Clearly document dataset collection and labeling.

### 3. AI-Based Secret Leak Detection
**Problem Statement:** Developers may accidentally expose API keys, access tokens, passwords, and other credentials in source code or version-control repositories.

**Proposed Approach:** Develop a secret detection tool that combines pattern matching, entropy-based analysis, and contextual machine learning to identify potential credential leaks.

**Research Questions:**
- Does contextual analysis reduce false positives compared with regular expressions alone?
- Which types of secrets are most difficult to detect?
- How well does the detector perform on previously unseen secret formats?

**Potential Research Gap to Investigate:** Can context-aware detection improve the balance between detecting real secrets and avoiding false alarms across different programming languages and repositories?

**Candidate Datasets:** Public secret-scanning benchmarks and appropriately sanitized repositories; synthetic examples may be used for controlled testing.

**Evaluation Plan:** Measure precision, recall, F1-score, false-positive rate, and detection coverage by secret type. Prevent real credentials from being exposed during dataset preparation.

### 4. SmartShield — AI-Assisted Smartphone Theft Protection
**Problem Statement:** Existing phone security features may not always detect suspicious device activity early or distinguish theft-related behavior from normal usage.

**Proposed Approach:** Explore an Android-based prototype that analyzes selected device events and identifies unusual patterns. The system could trigger configurable safety actions when a risk threshold is reached.

**Research Questions:**
- Can event-based anomaly detection distinguish simulated theft scenarios from normal usage?
- How does detection performance change across different user behavior patterns?
- What is the trade-off between early detection, false alarms, and battery consumption?

**Potential Research Gap to Investigate:** Can lightweight on-device anomaly detection improve theft-risk identification without excessive battery use or intrusive data collection?

**Candidate Datasets:** Controlled, consent-based device-event data and synthetic scenarios. Public datasets may be limited for realistic smartphone-theft behavior.

**Evaluation Plan:** Measure detection rate, false-alarm rate, detection delay, resource consumption, and usability. Clearly distinguish simulated results from real-world theft detection. Consider Android permission and background-execution restrictions.

### 5. AI-Based Fake Job & Online Recruitment Scam Detection
**Problem Statement:** Fake job advertisements may deceive job seekers through misleading descriptions, unrealistic salaries, fraudulent application fees, or requests for sensitive information.

**Proposed Approach:** Develop a classifier that analyzes job descriptions and available contextual features to estimate whether a listing may be fraudulent.

**Research Questions:**
- Which job-advertisement features contribute most to fraud detection?
- Do contextual features improve performance over text-only classification?
- How well does the model generalize to newer listings and different job categories?

**Potential Research Gap to Investigate:** Do existing models generalize reliably to changing recruitment scams and job advertisements from different regions?

**Candidate Datasets:** Employment Scam Aegean Dataset (EMSCAD), subject to checking availability, licensing, and suitability.

**Evaluation Plan:** Measure precision, recall, F1-score, and false-positive rate. Use time-aware or grouped validation where possible to reduce data leakage.

### 6. AI-Based Android App Privacy Risk Analyzer
**Problem Statement:** App permissions and other available metadata can make it difficult for users to understand potential privacy risks before installing an Android application.

**Proposed Approach:** Build a tool that analyzes app permissions and available metadata to identify potentially risky permission combinations and provide understandable explanations.

**Research Questions:**
- How accurately can permission-based features identify potentially risky applications?
- Does adding contextual metadata improve performance?
- Can explanations help users understand why an application receives a particular risk assessment?

**Potential Research Gap to Investigate:** Can a lightweight, explainable permission-based model provide useful risk assessments without relying on excessive or inaccessible app data?

**Candidate Datasets:** Public Android malware datasets and available app metadata or permission datasets, after checking their labels and licensing.

**Evaluation Plan:** Measure precision, recall, F1-score, false-positive rate, and explanation usefulness. Avoid treating every app requesting sensitive permissions as malicious.

