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
- The third type of assessment, and the one we will focus on throughout this module, is a **Red Team Assessment**. This describes an advanced, adversarial simulation where security experts, often called the **red team**, mimic real-world attackers' tactics, techniques, and procedures (TTPs) to test an organization's defenses. The red team's goal is to exploit technical vulnerabilities and challenge every aspect of security, including people and processes, by employing social engineering, phishing, and physical intrusions. Red team assessments focus on stealth and persistence, working to evade detection by the defensive **blue team** while seeking ways to achieve specific objectives, such as accessing sensitive data or critical systems. This exercise often spans weeks to months, providing an in-depth analysis of an organization's overall resilience against sophisticated threats.

##### Red Teaming ML-based System
- Unlike traditional systems, ML-based systems face unique vulnerabilities because they rely on large datasets, statistical inference, and complex model architectures. Thus, red team assessments are often the way to go when assessing the security of ML-based systems, as many advanced attack techniques require more time than a typical penetration test would last. Furthermore, ML-based systems are comprised of various components that interact with each other. Often, security vulnerabilities arise at these interaction points. As such, including all these components in the security assessment is beneficial. Determining the scope of a penetration test for an ML-based system can be difficult. It may inadvertently exclude specific components or interaction points, potentially making particular security vulnerabilities impossible to reveal.'

## Red Teaming ML

#### Attacking ML-based Systems (ML OWASP Top 10)
- Just like for [Web Applications](https://owasp.org/www-project-top-ten/), [Web APIs](https://owasp.org/www-project-api-security/), and [Mobile Applications](https://owasp.org/www-project-mobile-top-10/), OWASP has published a Top 10 list of security risks regarding the deployment and managment of ML-based Systems, the  [Top 10 for Machine Learning Security](https://owasp.org/www-project-machine-learning-security-top-10/). We will briefly discuss the ten risks to obtain an overview of security issues resulting from ML-based systems.

| ID | Description |
| :- | :- |
| ML01	| **Input Manipulation Attack**: Attackers modify input data to cause incorrect or malicious model outputs. |
| ML02	| **Data Poisoning Attack**: Attackers inject malicious or misleading data into training data, compromising model performance or creating backdoors. |
| ML03	| **Model Inversion Attack**: Attackers train a separate model to reconstruct inputs from model outputs, potentially revealing sensitive information. |
| ML04	| **Membership Inference Attack**: Attackers analyze model behavior to determine whether data was included in the model's training data set, potentially revealing sensitive information. |
| ML05	| **Model Theft**: Attackers train a separate model from interactions with the original model, thereby stealing intellectual property. |
| ML06	| **AI Supply Chain Attacks**: Attackers exploit vulnerabilities in any part of the ML supply chain. |
| ML07	| **Transfer Learning Attack**: Attackers manipulate the baseline model that is subsequently fine-tuned by a third-party. This can lead to biased or backdoored models. |
| ML08	| **Model Skewing**: Attackers skew the model's behavior for malicious purposes, for instance, by manipulating the training data set. |
| ML09	| **Output Integrity Attack**: Attackers manipulate a model's output before processing, making it look like the model produced a different output. |
| ML10	| **Model Poisoning**: Attackers manipulate the model's weights, compromising model performance or creating backdoors. |

##### ML 01 - Input Manipulation Attack
- Name suggests that involves attacker or bad guy can subtly altering the data fed to ML model, leading unexpected and potential harmful behaviour. These attacks, often using imperceptible changes, aim to decide the model into making incorrect decisions.
    - **Example**: Modifying the road signs with small stickers could trick self-driving car systems, highlighting serious risks to safty and reliability. 

![ML01-Input Manipulation Attack](/Images/ML01.png)

##### ML 02 - Data Poisoning Attack 
- Data Poisoning Attack compromises ML models by injecting malicious data into their training sets, resulting in flawed predictions and compromised security.
- **Example**: Poisoning an antivirus model's training data to make it classify the attacker's specific malware as safe, creating a dangerous 

##### ML 03 - Model Inversion Attack
- Model inversion attacks aim to reconstruct a target model's training data by analyzing its outputs. Attackers train a seperate model to reverse-engineer the input information from the predictions of the target model. These attacks are especially dangerous when the original training data contains sensitive information, such as medical records or personal details. 
- **Example**: The more detailed the model's output, the easier it is for an attacker to reconstruct the input data. Defenses include techniques like differential privacy, federated learning and secure multi-party computation, along with access control measure and output sanitization.

##### ML 04 - Membership Inference Attack
- Model inversion attacks aim to reconstruct a target model's training data by analyzing its outputs. Attackers train a separate model to reverse-engineer the input information from the predictions of the target model. These attacks are especially dangerous when the original training data contains sensitive information, such as medical records or personal details. The more detailed the model's output, the easier it is for an attacker to reconstruct the input data. Defenses include techniques like differential privacy, federated learning, and secure multi-party computation, along with access control measures and output sanitization.
- **Example**: The attacker wants to reconstruct information about the original data that was used to train a machine learning (ML) model. For example, they might want to know details about patients whose medical data was used to train a cancer detection system.

![ML04](/Images/ML04.png)

##### ML 05 - Model Theft
- This type of attack where an adversary recreates a copy of an ML model without direct access to its internal workings. This is achieved by repeatedly querying the target model with inputs and analyzing its outputs to replicate its functionality. Model theft poses a significant threat, potentially resulting in financial losses, intellectual property theft, competitive disadvantages, and reputational damage. For example, stealing a proprietary text generation model could enable a competitor to offer a similar service without incurring development costs.
- **Example**: Imagine a company that has developed a unique AI-powered text generation service. An attacker could repeatedly send carefully constructed text prompts to this service and collect the generated output. By analyzing enough of these input-output pairs, the attacker could train their own text generation model that produces similar results, effectively stealing the company's intellectual property.

![ML05](/Images/ML05.png)

##### ML 06 - AI Supply Chain Attacks
- AI supply chain attacks compromise machine learning models or their data by exploiting vulnerabilities in the interconnected components involved in the model's creation, deployment, or maintenance. Attackers can tamper with data sources, libraries, or pre-trained models to introduce malicious code or alter the model's behavior.
- **Example**: An attacker modifies a popular open-source library used to develop an AI-powered fraud detection system, embedding a backdoor that allows specific fraudulent transactions to bypass detection.

##### ML 07 - Transfer Learning Attack
- exploit vulnerabilities in pre-trained models by injecting malicious code or biases during the transfer learning process. These malicious elements can persist even when fine-tuning the model with clean data, potentially leading to security issues like backdoors or manipulated model behavior.
- **Example**: An attacker could poison a publicly available pre-trained facial recognition model. A company using this model for transfer learning in its facial recognition system might inherit a backdoor, allowing the attacker to bypass authentication with specific manipulated images

##### ML 08 - Model Skewing
- An attack where an adversary injects biased or incorrectly labeled data into an ML model's training set to deliberately influence its output in a direction that favors their objectives, potentially leading to incorrect predictions or malicious outcomes
- **Example**: An attacker could train an antivirus model to classify specific malware as benign by injecting the malware into the training data with a benign label, creating a backdoor to bypass detection.

##### ML 09 - Output Integrity Attack
- This  involves an attacker intercepting and altering the output generated by an ML model `before` it is processed by a downstream system or user. The ML model itself remains uncompromised, making detection challenging.
- **Example**: An attacker uploads malware to a system defended by an ML-based antivirus. When the ML model correctly identifies the file as malware, the attacker intercepts the output and changes the classification to `benign.` The antivirus then fails to delete the malware, leaving the system vulnerable.

##### ML 10 - Model Poisoning
- Attacks directly manipulate an ML model's internal parameters (weights and biases) to introduce malicious biases or behaviors. This requires direct access to the model's internal structure and sophisticated manipulation to achieve targeted malicious outcomes without overtly degrading overall performance.
- **Example**: An attacker gains access to an ML model used in military drones for target identification. They subtly modify the model's parameters to misclassify a specific friendly vehicle type as an enemy, potentially leading to friendly fire incidents in certain scenarios.