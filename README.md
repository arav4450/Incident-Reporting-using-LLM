<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

<h1>Incident Reporting System</h1>

<p>An incident reporting system built with Streamlit, SQLAlchemy, and LLM. This system allows users to log incidents, classify their severity, suggest root causes, and automatically generate corrective actions. Additionally, it generates incident reports in Word format.</p>

<h2>Features</h2>
<ul>
    <li><strong>Incident Logging</strong>: Users can log new incidents with detailed descriptions and assign reviewers.</li>
    <li><strong>Severity Classification</strong>: Automatically classify the severity of incidents.</li>
    <li><strong>Root Cause Suggestion</strong>: Suggest the most likely root cause of incidents based on their descriptions.</li>
    <li><strong>Corrective Action Suggestion</strong>: Generate detailed corrective action plans based on incident severity.</li>
    <li><strong>Incident Report Generation</strong>: Create and download incident reports in Word format.</li>
</ul>

<h2>Technologies Used</h2>
<ul>
    <li><strong>Streamlit</strong>: For creating the user interface.</li>
    <li><strong>SQLAlchemy</strong>: For database ORM and handling data operations.</li>
    <li><strong>Ollama</strong>: For integrating LLM to classify severity and suggest root causes.</li>
    <li><strong>Python-Docx</strong>: For generating Word documents for incident reports.</li>
    <li><strong>SQLite</strong>: For storing incident reports in a local database.</li>
</ul>

<h2>Installation</h2>
<ol>
    <li><strong>Clone the Repository</strong>:
        <pre><code>git clone https://github.com/arav4450/incident-reporting-system.git
cd incident-reporting-system</code></pre>
    </li>
    <li><strong>Set Up the Environment</strong>: Create and activate a virtual environment:
        <pre><code>python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`</code></pre>
    </li>
    <li><strong>Install pip-tools</strong>: Install `pip-tools` for dependency management:
        <pre><code>pip install pip-tools</code></pre>
    </li>
    <li><strong>Compile and Sync Dependencies</strong>: Use `pip-compile` to generate the `devs.txt` file and `pip-sync` to install the dependencies:
        <pre><code>pip-compile dev.in
pip-sync dev.txt</code></pre>
    </li>
    <li><strong>Download and Install Ollama</strong>: Download and install Ollama from <a href="https://ollama.com/">https://ollama.com/</a> and download the required model by running the following command:
        <pre><code>ollama pull starling-lm:7b-alpha-q5_K_M</code></pre>
    </li>
    
</ol>

<h2>Usage</h2>
<p>Run the Streamlit application:</p>
<pre><code>streamlit run app.py</code></pre>

<h2>Future Enhancements</h2>
<ul>
    <li><strong>More Advanced Root Cause Analysis</strong>: Integrate more advanced models for detecting specific categories (e.g., machinery-related issues, human errors, environmental hazards).</li>
    <li><strong>Better Workflow for Corrective Actions</strong>: Implement a more detailed corrective action tracking system involving follow-ups, task assignments, deadlines, and notifications.</li>
    <li><strong>User Authentication</strong>: Implement user authentication to ensure that only authorized personnel can submit and review incidents.</li>
    <li><strong>Email Notifications</strong>: Set up email or SMS notifications to alert reviewers when incidents are assigned or when corrective actions are overdue.</li>
</ul>



</body>
</html>

