# A. Cybersecurity & Digital Safety

## 1. X-Sentinel AI — Explainable AI-Based Cyber Threat Detection System

### Problem Statement

Traditional Intrusion Detection Systems (IDS) may generate many false alarms and provide limited explanations for why network traffic is classified as malicious. This makes it difficult for security analysts to understand and investigate detected threats.

### Proposed Approach

Develop a machine-learning-based intrusion detection system that classifies network traffic as benign or malicious and uses Explainable AI (XAI), such as SHAP, to explain its predictions.

The system could compare multiple machine learning models and evaluate whether their explanations remain consistent across different datasets or traffic conditions.

### Research Questions

- How do different machine learning models compare in detecting malicious network traffic?
- Does adding explainability affect detection performance?
- Are feature explanations consistent across different models and datasets?
- Can explanation-based analysis help identify false alarms or unreliable predictions?

### Potential Research Gap to Investigate

Do existing explainable intrusion detection methods provide sufficiently accurate, stable, and useful explanations when network traffic distributions change?

### Candidate Datasets

- [CIC-IDS2017 — Official dataset](https://www.unb.ca/cic/datasets/ids-2017.html)
- [CSE-CIC-IDS2018 — Official dataset](https://www.unb.ca/cic/datasets/ids-2018.html)

### Starter Research Papers

- [Toward Generating a New Intrusion Detection Dataset and Intrusion Traffic Characterization (2018)](https://doi.org/10.5220/0006639801080116)
- [BCCC-CIC-IDS2017 — Research dataset information](https://www.yorku.ca/research/bccc/ucs-ids/)
- [Explainable AI for Intrusion Detection — Google Scholar](https://scholar.google.com/scholar?q=explainable+AI+intrusion+detection+SHAP+cross+dataset+stability)

### Evaluation Plan

- Compare Logistic Regression, Random Forest, and XGBoost.
- Measure precision, recall, F1-score, and false-positive rate.
- Measure inference time and explanation stability.
- Evaluate cross-dataset performance where the feature sets and labels are compatible.
- Check for duplicate records, class imbalance, and data leakage before training.

---

## 2. AI-Based Scam & Fraud Detection for Bangla/Banglish

### Problem Statement

Users may struggle to identify scam messages and suspicious links, particularly when messages use Bangla, Banglish, informal spelling, or mixed-language expressions. Many existing datasets and detection approaches focus on English-language content.

### Proposed Approach

Develop an AI-based system that analyzes message text and URL features to identify potentially fraudulent content. The system could highlight suspicious phrases, links, requests for money, or attempts to obtain personal information.

A multilingual transformer could be compared with traditional machine learning models.

### Research Questions

- How do traditional machine learning models compare with multilingual transformer models?
- How does performance change between Bangla, Banglish, and mixed-language messages?
- Can combining message text and URL features improve detection?
- How robust is the system to spelling variations, transliteration, and previously unseen scam patterns?

### Potential Research Gap to Investigate

Are existing scam detection methods sufficiently robust to informal Bangla/Banglish language, spelling variation, and code-switching?

### Candidate Datasets

- [BanglaPhish-2026 — Synthetic Bangla scam benchmark](https://github.com/Xrenes/BanglaPhish-2026)
- [Hugging Face — Bangla SMS spam dataset search](https://huggingface.co/datasets?search=Bangla%20SMS%20spam)
- [Kaggle — Phishing URL datasets](https://www.kaggle.com/search?q=phishing+URL+dataset)
- [GitHub — Bangla spam detection datasets](https://github.com/search?q=Bangla+spam+detection+dataset&type=repositories)

### Starter Research Papers

- [Bangla SMS spam detection — Google Scholar](https://scholar.google.com/scholar?q=Bangla+SMS+spam+detection+machine+learning)
- [Bangla-English code-mixed text classification — Google Scholar](https://scholar.google.com/scholar?q=Bangla+English+code-mixed+text+classification+dataset)
- [Phishing message detection using NLP — Google Scholar](https://scholar.google.com/scholar?q=phishing+message+detection+NLP+multilingual+transformer)

### Evaluation Plan

- Compare TF-IDF with Logistic Regression or SVM against a multilingual transformer.
- Measure precision, recall, macro-F1, and false-positive rate.
- Evaluate performance separately on Bangla, Banglish, and mixed-language messages.
- Test robustness against spelling variation and unseen message templates.
- Inspect synthetic dataset limitations before treating benchmark performance as evidence of real-world effectiveness.

---

## 3. AI-Based Secret Leak Detection

### Problem Statement

Developers may accidentally expose API keys, access tokens, passwords, and other credentials in source code, configuration files, or version-control repositories.

Traditional pattern-matching tools can identify known formats but may also flag harmless strings or miss unfamiliar secret formats.

### Proposed Approach

Develop a secret detection tool that combines regular expressions, entropy-based analysis, and contextual machine learning. The system could analyze surrounding code to determine whether a string is likely to be a real credential.

### Research Questions

- Does contextual analysis reduce false positives compared with regular expressions alone?
- Which types of secrets are most difficult to detect?
- Can the system detect previously unseen secret formats?
- How does performance vary across programming languages and repository types?

### Potential Research Gap to Investigate

Can context-aware detection improve the balance between detecting real secrets and avoiding false alarms across different programming languages and repositories?

### Candidate Datasets and Tools

- [GitHub — Gitleaks secret scanner](https://github.com/gitleaks/gitleaks)
- [GitHub — TruffleHog secret scanner](https://github.com/trufflesecurity/trufflehog)
- [GitHub — Secret detection dataset search](https://github.com/search?q=secret+detection+dataset&type=repositories)

### Starter Research Papers

- [Secret leakage detection in source code — Google Scholar](https://scholar.google.com/scholar?q=secret+leak+detection+source+code+GitHub+research+paper)
- [Machine learning for API key and credential detection — Google Scholar](https://scholar.google.com/scholar?q=machine+learning+secret+detection+API+keys+source+code)
- [GitHub secret scanning research — Google Scholar](https://scholar.google.com/scholar?q=GitHub+secret+scanning+false+positive+research)

### Evaluation Plan

- Compare regular-expression detection, entropy-based detection, and a context-aware model.
- Measure precision, recall, F1-score, and false-positive rate.
- Measure detection coverage for different secret types.
- Test on secret formats and repositories excluded from training.
- Use sanitized or synthetic credentials; never expose real credentials in a dataset or report.

---

## 4. SmartShield — AI-Assisted Smartphone Theft Protection

### Problem Statement

Existing phone security features may not always distinguish suspicious device activity from normal usage. Detecting theft-related behavior without generating excessive false alarms is challenging.

### Proposed Approach

Explore an Android-based prototype that analyzes selected device events and identifies unusual patterns. The system could trigger configurable safety actions when a risk threshold is reached.

The research should focus on a clearly defined, measurable detection task rather than claiming that all smartphone theft can be predicted from device behavior.

### Research Questions

- Can event-based anomaly detection distinguish simulated theft scenarios from normal usage?
- How does detection performance change across different user behavior patterns?
- What is the trade-off between detection delay, false alarms, and battery consumption?
- Can a lightweight model run within practical Android background-execution constraints?

### Potential Research Gap to Investigate

Can lightweight on-device anomaly detection improve theft-risk identification without excessive battery use or intrusive data collection?

### Candidate Datasets and Data Sources

- [Drebin — Android malware dataset](https://drebin.mlsec.org/)
- [Android device theft detection — Google Scholar](https://scholar.google.com/scholar?q=Android+device+theft+detection+behavior+dataset)
- Controlled, consent-based device-event data collected for the experiment.

### Starter Research Papers

- [Drebin: Effective and Explainable Detection of Android Malware in Your Pocket](https://www.ndss-symposium.org/ndss2014/ndss-2014-programme/drebin-effective-and-explainable-detection-android-malware-your-pocket/)
- [Android device anomaly detection — Google Scholar](https://scholar.google.com/scholar?q=Android+device+anomaly+detection+security+research)

### Evaluation Plan

- Define specific simulated scenarios and a normal-use baseline.
- Measure detection rate, false-alarm rate, and detection delay.
- Measure battery consumption, memory use, and processing overhead.
- Evaluate usability and Android permission restrictions.
- Clearly distinguish controlled experimental results from real-world theft detection.

---

## 5. AI-Based Fake Job & Online Recruitment Scam Detection

### Problem Statement

Fake job advertisements may deceive job seekers through misleading descriptions, unrealistic salaries, fraudulent application fees, or requests for sensitive information.

### Proposed Approach

Develop a classifier that analyzes job descriptions and available contextual features to estimate whether a listing may be fraudulent. An explainable model could highlight suspicious features for further review.

### Research Questions

- Which job-advertisement features contribute most to fraud detection?
- Do contextual features improve performance over text-only classification?
- How well does the model generalize to newer listings and different job categories?
- Can explainability help reviewers prioritize suspicious advertisements?

### Potential Research Gap to Investigate

Do existing models generalize reliably to changing recruitment scams and job advertisements from different regions?

### Candidate Datasets

- [Employment Scam Aegean Dataset (EMSCAD)](http://emscad.samos.aegean.gr/)
- [Kaggle — Real or Fake Job Posting Prediction](https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction)

### Starter Research Papers

- [Automatic Detection of Online Recruitment Frauds: Characteristics, Methods, and a Public Dataset (2017)](https://www.mdpi.com/1999-5903/9/1/6)
- [Fraud-BERT: Transformer-Based Context-Aware Online Recruitment Fraud Detection](https://doi.org/10.1007/s10791-025-09502-8)
- [An Explainable, Cost-Aware Hybrid Framework for Fraudulent Online Job Posting Detection (2026)](https://doi.org/10.1016/j.array.2026.101191)

### Evaluation Plan

- Compare text-only models with models using contextual features.
- Measure precision, recall, macro-F1, and false-positive rate.
- Account for class imbalance; accuracy alone is not sufficient.
- Use time-aware or grouped validation where possible.
- Examine whether the model generalizes to newer scam patterns.

---

## 6. AI-Based Android App Privacy Risk Analyzer

### Problem Statement

App permissions and other available metadata can make it difficult for users to understand potential privacy risks before installing an Android application.

Permission-based rules may also generate misleading warnings because some legitimate applications require sensitive permissions for valid purposes.

### Proposed Approach

Build a tool that analyzes app permissions and available metadata to identify potentially risky permission combinations and provide understandable explanations.

### Research Questions

- How accurately can permission-based features identify potentially risky applications?
- Does adding contextual metadata improve performance?
- Can explanations help users understand why an application receives a particular risk assessment?
- How well does the model generalize to applications not represented in the training data?

### Potential Research Gap to Investigate

Can a lightweight, explainable permission-based model provide useful risk assessments without relying on excessive or inaccessible app data?

### Candidate Datasets

- [Drebin — Android malware dataset](https://drebin.mlsec.org/)
- [Android malware and permission datasets — Google Scholar](https://scholar.google.com/scholar?q=Android+app+permissions+privacy+risk+dataset)

### Starter Research Papers

- [Drebin: Effective and Explainable Detection of Android Malware in Your Pocket](https://www.ndss-symposium.org/ndss2014/ndss-2014-programme/drebin-effective-and-explainable-detection-android-malware-your-pocket/)
- [Android permission-based malware detection — Google Scholar](https://scholar.google.com/scholar?q=Android+permission+based+malware+detection+machine+learning)
- [Android privacy risk assessment — Google Scholar](https://scholar.google.com/scholar?q=Android+application+privacy+risk+assessment+permissions)

### Evaluation Plan

- Compare permission-only features with models that use additional metadata.
- Measure precision, recall, F1-score, and false-positive rate.
- Evaluate explanation usefulness.
- Validate on separate applications where feasible.
- Avoid treating malware classification as equivalent to measuring privacy risk.

