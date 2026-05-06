**AEGIS** is a predictive phishing URL detection system designed to protect users from malicious web vulnerabilities. By analyzing 21 unique features of a web address, the system provides a real-time risk score and human-readable explanations of why a site is flagged as dangerous or safe.

## 👥 The Team
* **Developers:** Namitha Anna Koshy & Rithika
* **Mentor:** Guided by Mr. Jithin Sir
* **Institution:** St. Joseph's College of Engineering and Technology (SJCET), Palai

## 🚀 Key Features
* **Hybrid Analysis:** Combines global threat intelligence with a local Machine Learning engine.
* **Explainable AI (XAI):** Uses SHAP (SHapley Additive exPlanations) to translate complex model decisions into human-readable security indicators.
* **Modern UI:** A high-performance, glass-morphism interface built with HTML5, Tailwind CSS, and a custom particle engine.
* **Dockerized Microservices:** Fully containerized architecture for easy deployment and scaling.

## 🛠️ Tech Stack
* **Frontend:** HTML5, CSS3 (Tailwind), JavaScript
* **Backend:** FastAPI (Python)
* **ML Engine:** LightGBM, SHAP
* **DevOps:** Docker, Docker Compose, Nginx

## 📊 Feature Analysis
The system evaluates 21 distinct features, categorized as follows:

### **General URL Characteristics**
* **URLLength**: Excess length often hides true destinations.
* **URLSimilarityIndex**: Detects resemblance to known brand names (spoofing).
* **CharContinuationRate**: Identifies repetitive patterns typical of scam links.
* **TLDLegitimateProb**: Measures trust levels of the website ending (e.g., .com vs .xyz).
* **URLCharProb**: Analyzes if character sequences are standard or random.
* **TLDLength**: Flags non-standard website extensions.
* **NoOfSubDomain**: Identifies confusing website sub-sections used to mimic domains.
* **DomainLength**: Flags unusual lengths of the main site name.

### **Deception & Obfuscation**
* **HasObfuscation**: Detects encoded or scrambled text in the address.
* **NoOfObfuscatedChar**: Counts hidden characters within the link.
* **ObfuscationRatio**: Measures the percentage of the link that is obscured.

### **Character Composition**
* **LetterRatioInURL**: Flags an atypical balance of letters vs. symbols.
* **NoOfDegitsInURL**: Identifies high digit counts, common in bot-generated links.
* **DegitRatioInURL**: Measures the density of numbers in the link.
* **NoOfOtherSpecialCharsInURL**: Counts unusual symbols like hyphens or underscores.
* **SpacialCharRatioInURL**: Identifies "messy" URLs with high symbol density.

### **Technical Red Flags**
* **NoOfEqualsInURL (=)**: Identifies tracking markers used to capture data.
* **NoOfQMarkInURL (?)**: Flags hidden data-transfer commands.
* **NoOfAmpersandInURL (&)**: Detects chained background actions in the link.
* **IsHTTPS**: Flags the absence of standard security encryption.
* **IsDomainIP**: Detects raw numeric addresses instead of names.

## 💻 Installation & Setup

### Prerequisites
* Docker and Docker Desktop installed.
* Git installed.

### Steps to Run
1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/Phishy.git
    cd Phishy
    ```

2.  **Build and launch the containers:**
    ```bash
    docker-compose up --build
    ```

3.  **Access the application:**
    * **Frontend:** Open `http://localhost` in your browser.
    * **API Docs:** Open `http://localhost:8000/docs` to view the FastAPI documentation.

## 📜 Research & Publication
This project builds upon our research in applied Artificial Intelligence and Cybersecurity, focusing on making complex security data understandable for non-technical users.
