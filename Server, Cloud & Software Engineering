# C. Server, Cloud & Software Engineering

## 1. ScaleWise AI — Predictive Server Load Optimization and Auto-Scaling

### Problem Statement

Reactive auto-scaling systems often respond after server demand has increased, which can cause delayed responses or unnecessary resource allocation. Predicting upcoming workload may help systems allocate resources more efficiently.

### Proposed Approach

Develop a workload forecasting model that predicts upcoming resource demand and evaluates whether proactive scaling can improve on reactive scaling policies.
The prototype could forecast workload and simulate scaling decisions without requiring deployment on a production cloud service.

### Research Questions

- Can workload forecasting improve scaling decisions compared with reactive threshold-based policies?
- Which forecasting models perform best under sudden workload changes?
- What is the trade-off between response time, resource utilization, and infrastructure cost?
- How does prediction accuracy change when workload patterns shift?

### Potential Research Gap to Investigate

Do predictive scaling approaches remain effective during workload spikes and distribution changes while avoiding excessive resource allocation?

### Candidate Datasets

- [Google Borg Cluster Traces — Official repository](https://github.com/google/cluster-data)
- [Alibaba Cluster Trace Program — Official repository](https://github.com/alibaba/clusterdata)

### Starter Research Papers

- [Large-Scale Cluster Management at Google with Borg (2015)](https://doi.org/10.1145/2741948.2741964)
- [Borg: The Next Generation (2020)](https://research.google/pubs/borg-the-next-generation/)
- [Workload prediction and predictive auto-scaling — Google Scholar](https://scholar.google.com/scholar?q=cloud+workload+prediction+predictive+auto+scaling+machine+learning)

### Evaluation Plan

- Compare moving-average and threshold-based baselines with forecasting models such as XGBoost or LSTM.
- Measure forecast error using MAE and RMSE.
- Measure response latency, SLA violations, resource utilization, and simulated cost.
- Test performance during sudden workload spikes and changing traffic patterns.
- Document the simulation assumptions and avoid claiming production-level savings from simulation alone.

---

## 2. AI-Based Server Bottleneck Detection

### Problem Statement

Server slowdowns can result from CPU, memory, disk I/O, network, or application-level bottlenecks. Identifying the likely cause from monitoring data can require substantial manual investigation.

### Proposed Approach

Build a monitoring and diagnosis prototype that analyzes time-series metrics and detects unusual behavior. Investigate whether the system can classify or rank possible bottleneck causes.

Possible techniques include Isolation Forest, time-series anomaly detection, and supervised classification when reliable fault labels are available.

### Research Questions

- Can anomaly detection identify bottleneck-related behavior before severe service degradation?
- Which metrics provide the most useful diagnostic information?
- Can combining multiple metrics improve diagnosis compared with single-metric thresholds?
- How well does the model identify bottlenecks under noisy workloads or previously unseen conditions?

### Potential Research Gap to Investigate

Can a lightweight diagnostic model distinguish between different bottleneck causes under noisy workloads and previously unseen operating conditions?

### Candidate Datasets

- [LogHub — Public system log datasets](https://github.com/logpai/loghub)
- [Google Borg Cluster Traces](https://github.com/google/cluster-data)
- [Alibaba Cluster Traces](https://github.com/alibaba/clusterdata)

### Starter Research Papers

- [LogHub: A Large Collection of System Log Datasets for AI-driven Log Analytics (2020)](https://arxiv.org/abs/2008.06448)
- [Server bottleneck detection and root-cause analysis — Google Scholar](https://scholar.google.com/scholar?q=server+bottleneck+detection+root+cause+analysis+AIOps+machine+learning)
- [AIOps and system performance diagnosis — Google Scholar](https://scholar.google.com/scholar?q=AIOps+system+performance+diagnosis+CPU+memory+network+bottleneck)

### Evaluation Plan

- Compare the model with simple threshold-based monitoring.
- Measure detection precision, recall, F1-score, and false-alarm rate.
- Measure detection delay and diagnosis accuracy.
- Measure monitoring overhead.
- Consider controlled CPU, memory, disk, and network fault injection to obtain reliable ground-truth labels.

---

## 3. AI-Based Software Bug Prediction

### Problem Statement

Software teams have limited time to test and review every component equally. Predicting which files or modules are more likely to contain defects may help prioritize testing and code review.

### Proposed Approach

Train a machine learning model using software metrics, code-change history, or repository features to estimate defect risk for a file or module.

The system could rank components by estimated risk and help developers prioritize testing effort.

### Research Questions

- Which feature groups provide the most useful defect predictions?
- Do historical change features improve predictions beyond static code metrics?
- How well do models trained on earlier versions generalize to later versions or other projects?
- Can risk-based prioritization reduce testing effort without missing too many defective components?

### Potential Research Gap to Investigate

Do bug prediction models remain reliable under realistic temporal evaluation and across different software projects, rather than only under random train-test splits?

### Candidate Datasets

- [PROMISE software defect datasets — Repository](https://github.com/jalaxy33/PROMISE-dataset)
- [PROMISE 2021 Defect Prediction Challenge](https://github.com/smartshark/promise-challenge)
- [PROMISE Software Engineering Repository — Dataset information](http://promise.site.uottawa.ca/SERepository/datasets-page.html)

### Starter Research Papers

- [A Systematic Literature Review on Software Defect Prediction Using AI: Datasets, Data Validation Methods, Approaches, and Tools (2022)](https://doi.org/10.1016/j.engappai.2022.104773)
- [Application of Deep Learning in Software Defect Prediction: Systematic Literature Review and Meta-analysis (2023)](https://doi.org/10.1016/j.infsof.2023.107175)
- [Software defect prediction research — Google Scholar](https://scholar.google.com/scholar?q=software+defect+prediction+temporal+validation+cross+project)

### Evaluation Plan

- Compare Logistic Regression, Random Forest, and gradient-boosting models.
- Measure precision, recall, F1-score, and PR-AUC where appropriate.
- Evaluate effort-aware metrics if the goal is to prioritize code review or testing.
- Use temporal validation to train on earlier versions and test on later versions.
- Check for duplicate records, label leakage, and differences between projects.

---

## 4. AI-Based API Anomaly Detection

### Problem Statement

APIs may experience unusual request patterns, latency spikes, elevated error rates, or unexpected traffic behavior. Static thresholds can struggle when normal traffic changes over time.

### Proposed Approach

Develop an anomaly detection system using API request metadata and operational metrics. The system could flag unusual behavior and provide supporting indicators for investigation.

Possible input features include request frequency, response status codes, latency, endpoint, and time-based traffic patterns, depending on dataset availability.

### Research Questions

- Can machine learning detect API anomalies more accurately than static threshold rules?
- How does performance change when normal traffic patterns shift?
- Which features are most useful for distinguishing genuine anomalies from normal traffic bursts?
- Can adaptive detection reduce false alarms without increasing detection delay?

### Potential Research Gap to Investigate

Can adaptive anomaly detection reduce false alarms under changing API traffic while maintaining timely detection?

### Candidate Datasets

- [LogHub — Public system logs](https://github.com/logpai/loghub)
- [Alibaba Cluster Trace Program](https://github.com/alibaba/clusterdata)
- [API anomaly detection datasets — Google Scholar](https://scholar.google.com/scholar?q=API+anomaly+detection+dataset+HTTP+requests+latency+errors)

### Starter Research Papers

- [LogHub: A Large Collection of System Log Datasets for AI-driven Log Analytics (2020)](https://arxiv.org/abs/2008.06448)
- [API anomaly detection and service monitoring — Google Scholar](https://scholar.google.com/scholar?q=API+anomaly+detection+machine+learning+service+monitoring)
- [Time-series anomaly detection in cloud services — Google Scholar](https://scholar.google.com/scholar?q=time+series+anomaly+detection+cloud+service+metrics+research)

### Evaluation Plan

- Compare threshold-based rules with Isolation Forest, One-Class SVM, or an autoencoder.
- Measure precision, recall, F1-score, and false-positive rate.
- Measure detection delay and computational overhead.
- Test the system under changing traffic patterns and simulated anomalies.
- Verify that the chosen dataset contains API-level information and reliable anomaly labels; general system logs may not be sufficient.

