# AI Security (AI Red Teamer - HTB)

## Fnndamentals of AI
- Artificial Intelligence (AI) is a broad field focused on developing intelligent systems capable of performing tasks that typically require human intelligence. These tasks include understanding natural language, recognizing objects, making decisions, solving problems, and learning from experience. AI systems exhibit cognitive abilities like reasoning, perception, and problem-solving across various domains. Some key areas of AI include:
    - Natural Language Processing (NLP): Enabling computers to understand, interpret, and generate human language.
    - Computer Vision: Allowing computers to "see" and interpret images and videos.
    - Robotics: Developing robots that can perform tasks autonomously or with human guidance.
    - Expert Systems: Creating systems that mimic the decision-making abilities of human experts.
    
![AI Tpyes](/Images/AI_Types.webp)

##### Machine Learning (ML)
Is a subfield of AI that focuses on enabling systems to learn from data and improve their performance on specific tasks without explicit programming. ML algorithms use statistical techniques to identify patterns, trends, and anomalies within datasets, allowing the system to make predictions, decisions, or classifications based on new input data.

- ML can be categorized into three main types:
- **Supervised Learning**: The algorithm learns from labeled data, where each data point is associated with a known outcome or label. 
    - Examples  include:
        - Image classification
        - Spam detection
        - Fraud prevention
- **Unsupervised Learning**: The algorithm learns from unlabeled data without providing an outcome or label. 
    - Examples include:
        - Customer segmentation
        - Anomaly detection
        - Dimensionality reduction
- **Reinforcement Learning**: The algorithm learns through trial and error by interacting with an environment and receiving feedback as rewards or penalties. 
    - Examples include:
        - Game playing
        - Robotics
        - Autonomous driving
- For instance, an ML algorithm can be trained on a dataset of images labeled as "cat" or "dog." By analyzing the features and patterns in these images, the algorithm learns to distinguish between cats and dogs. When presented with a new image, it can predict whether it depicts a cat or a dog based on its learned knowledge.

- ML has a wide range of applications across various industries, including:
    - Healthcare: Disease diagnosis, drug discovery, personalized medicine
    - Finance: Fraud detection, risk assessment, algorithmic trading
    - Marketing: Customer segmentation, targeted advertising, recommendation systems
    - Cybersecurity: Threat detection, intrusion prevention, malware analysis
    - Transportation: Traffic prediction, autonomous vehicles, route optimization

- The Relationship Between AI, ML, and DL
    - Machine Learning (ML) and Deep Learning (DL) are subfields of Artificial Intelligence (AI) that enable systems to learn from data and make intelligent decisions. They are crucial enablers of AI, providing the learning and adaptation capabilities that underpin many intelligent systems.
    - ML algorithms, including DL algorithms, allow machines to learn from data, recognize patterns, and make decisions. The various types of ML, such as supervised, unsupervised, and reinforcement learning, each contribute to achieving AI's broader goals. For instance:

## Introduction to Red Teaming ML-based Systems
> To assess the security of ML-based systems, it is essential to have a deep understanding of the underlying components and algorithms.

- Traditionally, when discussing security assessments of IT systems, the most common type of assessment is a **Penetration Test**. This type of assessment is typically a focused and time-bound exercise aimed at discovering and exploiting vulnerabilities in specific systems, applications, or network environments. Penetration testers follow a structured process, often using automated tools and manual testing techniques to identify security weaknesses within a defined scope. A penetration test aims to determine if vulnerabilities exist, whether they can be exploited, and to what extent. It is often carried out in isolated network segments or web application instances to avoid interference with regular users.

![Difference between Roles](/Images/Red%20VS%20vulnerabilitity%20vs%20pentest.png)

- **Vulnerability assessments** are generally more automated assessments that focus on identifying, cataloging, and prioritizing known vulnerabilities within an organization's infrastructure. These assessments typically do not involve exploitation but instead focus on the identification of security vulnerabilities. They provide a comprehensive scan of systems, applications, and networks to identify potential security gaps that could be exploited. These scans are often the result of automated scans using vulnerability scanners such as **Nessus** or **OpenVAS**. 
- The third type of assessment, and the one we will focus on throughout this module, is a **Red Team Assessment**. This describes an advanced, adversarial simulation where security experts, often called the red team, mimic real-world attackers' tactics, techniques, and procedures (TTPs) to test an organization's defenses. The red team's goal is to exploit technical vulnerabilities and challenge every aspect of security, including people and processes, by employing social engineering, phishing, and physical intrusions. Red team assessments focus on stealth and persistence, working to evade detection by the defensive blue team while seeking ways to achieve specific objectives, such as accessing sensitive data or critical systems. This exercise often spans weeks to months, providing an in-depth analysis of an organization's overall resilience against sophisticated threats.