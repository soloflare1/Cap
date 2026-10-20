# B. AI, Programming & Education

## 1. AdaptiveAI Tutor — Personalized AI-Based Programming Tutor

### Problem Statement

Students have different levels of programming knowledge, but traditional learning platforms often provide similar exercises and learning sequences to everyone. Students may need different levels of explanation, practice, and guidance.

### Proposed Approach

Develop an adaptive programming tutor that estimates a learner's knowledge from previous answers and recommends suitable exercises, hints, or learning materials.

The system could use Bayesian Knowledge Tracing, Item Response Theory, or another learner-modeling approach to adapt the learning sequence.

### Research Questions

- Does adaptive exercise selection improve learning outcomes compared with a fixed sequence?
- Which learner features are useful for estimating programming knowledge?
- Can the system adapt effectively when only a small amount of learner data is available?
- Does personalized feedback improve performance on later independent exercises?

### Potential Research Gap to Investigate

Do existing adaptive learning methods effectively support programming beginners when learner interaction data is limited or irregular?

### Candidate Datasets

- [ASSISTments — Educational research datasets](https://sites.google.com/site/assistmentsdata/home)
- [PSLC DataShop — Educational datasets](https://pslcdatashop.web.cmu.edu/)
- [Project CodeNet — Programming submissions](https://github.com/IBM/Project_CodeNet)

### Starter Research Papers

- [Knowledge Tracing: A Survey (2023)](https://doi.org/10.1145/3569576)
- [Bayesian Knowledge Tracing and adaptive learning — Google Scholar](https://scholar.google.com/scholar?q=Bayesian+Knowledge+Tracing+adaptive+learning+programming+education)
- [Personalized programming education — Google Scholar](https://scholar.google.com/scholar?q=personalized+adaptive+programming+education+intelligent+tutoring+system)

### Evaluation Plan

- Compare adaptive learning with a fixed-sequence baseline.
- Measure learner-state prediction performance where suitable labels are available.
- Evaluate exercise completion, pre-test and post-test scores, and delayed retention if feasible.
- Conduct a consent-based user study if the project makes claims about actual learning improvement.
- Verify that the selected dataset contains the interaction features needed for the proposed model.

---

## 2. AI Over-Reliance Detection in Programming Education

### Problem Statement

AI coding assistants can help students solve programming problems, but excessive dependence may reduce independent problem-solving practice. However, frequent AI use does not automatically mean that a student is over-reliant.

A useful system must investigate learning behavior rather than simply counting AI requests.

### Proposed Approach

Investigate whether learning-process signals—such as independent attempts, hint requests, code changes, and performance on later independent tasks—can identify patterns associated with difficulty solving problems without AI assistance.

A prototype could provide reflective feedback that encourages independent reasoning without blocking legitimate AI support.

### Research Questions

- Which interaction signals are associated with reduced independent problem-solving performance?
- Can these signals predict difficulty solving a similar problem without AI assistance?
- Does the relationship between AI use and independent performance vary with task difficulty or prior experience?
- Can reflective feedback encourage independent reasoning without preventing useful AI support?

### Potential Research Gap to Investigate

Can over-reliance be measured reliably from learning interactions, rather than simply counting AI requests or assuming that frequent AI use is harmful?

### Candidate Datasets and Data Sources

- [CodeStream — Iterative programming submissions dataset (2026)](https://www.sciencedirect.com/science/article/pii/S2352340926003951)
- [Project CodeNet — IBM](https://github.com/IBM/Project_CodeNet)
- [AI coding assistants in programming education — Google Scholar](https://scholar.google.com/scholar?q=AI+coding+assistants+programming+education+student+behavior+dataset)

### Starter Research Papers

- [AI Code Assistants in Programming Education: A Narrative Literature Review (2026)](https://www.mdpi.com/2227-7102/16/6/961)
- [Evaluating Lab Assistant Chatbot on Student Learning and Behaviors in a Programming Short Course](https://doi.org/10.1016/j.caeai.2025.100527)
- [AI coding assistant use and independent problem-solving — Google Scholar](https://scholar.google.com/scholar?q=generative+AI+coding+assistant+independent+problem+solving+students+study)

### Evaluation Plan

- Define over-reliance operationally before collecting or labeling data.
- Compare performance on assisted tasks with performance on subsequent independent tasks.
- Measure prediction precision, recall, and F1-score where defensible labels are available.
- For a user study, compare clearly defined assistance conditions and evaluate learning outcomes.
- Obtain informed consent, protect student privacy, and avoid labeling students as over-reliant based only on usage frequency.

---

## 3. AI-Based Programming Error Diagnosis

### Problem Statement

Beginner programmers often struggle to understand compiler errors, logical mistakes, and runtime failures. Simply showing a corrected solution may not help them learn how to diagnose and fix similar problems independently.

### Proposed Approach

Build a system that classifies common programming errors and provides progressive hints explaining the likely cause and possible debugging steps.

For example, the system could first identify an error category, then offer a conceptual hint, followed by a more specific suggestion if the student remains stuck.

### Research Questions

- Can error classification improve the relevance of debugging hints?
- Do progressive hints support better learning than showing a complete correction immediately?
- How does performance vary across error types and programming experience levels?
- Can students apply the learned debugging strategy to new problems?

### Potential Research Gap to Investigate

Do current automated debugging approaches provide explanations that help beginners understand and fix errors, rather than merely producing a corrected program?

### Candidate Datasets

- [Project CodeNet — IBM](https://github.com/IBM/Project_CodeNet)
- [CodeStream — Dataset of iterative programming submissions](https://www.sciencedirect.com/science/article/pii/S2352340926003951)
- [Automated programming feedback datasets — Google Scholar](https://scholar.google.com/scholar?q=novice+programming+error+diagnosis+dataset+automated+feedback)

### Starter Research Papers

- [CodeStream: A Dataset of Iterative Programming Submissions with Sequential Verdict Traces and Attempt Histories (2026)](https://doi.org/10.1016/j.dib.2026.112843)
- [Automated programming error diagnosis — Google Scholar](https://scholar.google.com/scholar?q=automated+programming+error+diagnosis+intelligent+feedback+novice+programmers)
- [Automated feedback in programming education — Google Scholar](https://scholar.google.com/scholar?q=automated+feedback+programming+education+debugging+students)

### Evaluation Plan

- Measure error-classification precision, recall, and F1-score.
- Evaluate hint relevance using predefined criteria or expert ratings.
- Measure successful correction rate and time to fix.
- Compare progressive hints with direct correction.
- Assess learning transfer through follow-up problems, if a user study is feasible.

---

## 4. Human-in-the-Loop AI Learning Platform

### Problem Statement

Educational AI systems may produce explanations, recommendations, or answers that are not appropriate for every learner. User feedback is not always incorporated systematically into future recommendations.

### Proposed Approach

Develop a learning platform where users can rate or correct AI-generated educational content. Investigate whether this feedback can improve content ranking or recommendation quality.

The project should define a specific task, such as ranking programming hints, recommending exercises, or selecting explanations that learners find useful.

### Research Questions

- Does incorporating user feedback improve the relevance of educational recommendations?
- How much feedback is needed before measurable improvement occurs?
- How can the system handle inconsistent or low-quality feedback?
- Does feedback-informed ranking perform better for new users with limited interaction history?

### Potential Research Gap to Investigate

Under what conditions does feedback from learners improve educational AI outputs, and when can noisy or biased feedback reduce quality?

### Candidate Datasets

- [ASSISTments — Educational research datasets](https://sites.google.com/site/assistmentsdata/home)
- [PSLC DataShop](https://pslcdatashop.web.cmu.edu/)
- [Hugging Face — Educational question-answering datasets](https://huggingface.co/datasets?search=educational%20question%20answering)

### Starter Research Papers

- [Human-in-the-loop machine learning for education — Google Scholar](https://scholar.google.com/scholar?q=human-in-the-loop+machine+learning+education+student+feedback)
- [Feedback-based educational recommendation systems — Google Scholar](https://scholar.google.com/scholar?q=feedback+based+educational+recommendation+system+learning)
- [Human feedback for educational AI — Google Scholar](https://scholar.google.com/scholar?q=human+feedback+AI+tutoring+system+educational+content+quality)

### Evaluation Plan

- Compare a baseline system with a feedback-informed version.
- Measure ranking quality, user-rated relevance, and error rate.
- Evaluate performance as the amount of available feedback increases.
- Test the effect of noisy or conflicting feedback.
- Conduct a consent-based study if making claims about learner satisfaction or educational outcomes.
