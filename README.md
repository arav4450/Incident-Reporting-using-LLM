<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Incident Reporting System</title>
</head>
<body>

<h1>Incident Reporting System</h1>

<p>An advanced incident reporting system built with Streamlit, SQLAlchemy, and a machine learning model from Hugging Face's transformers library. This system allows users to log incidents, classify their severity, suggest root causes, and automatically generate corrective actions. Additionally, it generates incident reports in Word format and provides a user-friendly interface for reviewing and managing incidents.</p>

<h2>Features</h2>
<ul>
    <li><strong>Incident Logging</strong>: Users can log new incidents with detailed descriptions and assign reviewers.</li>
    <li><strong>Severity Classification</strong>: Automatically classify the severity of incidents using a pre-trained transformer model.</li>
    <li><strong>Root Cause Suggestion</strong>: Suggest the most likely root cause of incidents based on their descriptions.</li>
    <li><strong>Corrective Action Suggestion</strong>: Generate detailed corrective action plans based on incident severity.</li>
    <li><strong>Incident Report Generation</strong>: Create and download incident reports in Word format.</li>
    <li><strong>Incident Review and Management</strong>: Review open incidents, assign follow-up tasks, and track the status of corrective actions.</li>
</ul>

<h2>Technologies Used</h2>
<ul>
    <li><strong>Streamlit</strong>: For creating the user interface.</li>
    <li><strong>SQLAlchemy</strong>: For database ORM and handling data operations.</li>
    <li><strong>Hugging Face Transformers</strong>: For integrating pre-trained transformer models to classify severity and suggest root causes.</li>
    <li><strong>Python-Docx</strong>: For generating Word documents for incident reports.</li>
    <li><strong>SQLite</strong>: For storing incident reports in a local database.</li>
</ul>

<h2>Installation</h2>
<ol>
    <li><strong>Clone the Repository</strong>:
        <pre><code>git clone https://github.com/yourusername/incident-reporting-system.git
cd incident-reporting-system</code></pre>
    </li>
    <li><strong>Set Up the Environment</strong>: Create and activate a virtual environment:
        <pre><code>python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`</code></pre>
    </li>
    <li><strong>Install pip-tools</strong>: Install `pip-tools` for dependency management:
        <pre><code>pip install pip-tools</code></pre>
    </li>
    <li><strong>Create dev.in File</strong>: List your project dependencies in a `dev.in` file:
        <pre><code>streamlit
pandas
datetime
transformers
SQLAlchemy
python-docx</code></pre>
    </li>
    <li><strong>Compile Dependencies</strong>: Use `pip-compile` to generate the `requirements.txt` file:
        <pre><code>pip-compile dev.in</code></pre>
    </li>
    <li><strong>Install Dependencies</strong>: Install the compiled dependencies:
        <pre><code>pip install -r requirements.txt</code></pre>
    </li>
    <li><strong>Set Up the Database</strong>: Initialize the SQLite database:
        <pre><code>python -c "from main import Base, engine; Base.metadata.create_all(engine)"</code></pre>
    </li>
</ol>

<h2>Usage</h2>
<p>Run the Streamlit application:</p>
<pre><code>streamlit run main.py</code></pre>

<h2>Future Enhancements</h2>
<ul>
    <li><strong>More Advanced Root Cause Analysis</strong>: Integrate more advanced models for detecting specific categories (e.g., machinery-related issues, human errors, environmental hazards).</li>
    <li><strong>Better Workflow for Corrective Actions</strong>: Implement a more detailed corrective action tracking system involving follow-ups, task assignments, deadlines, and notifications.</li>
    <li><strong>Advanced Incident Analytics</strong>: Add detailed analytics, like charts and graphs, to analyze incident trends, types, and severity distributions over time.</li>
    <li><strong>User Authentication</strong>: Implement user authentication to ensure that only authorized personnel can submit and review incidents.</li>
    <li><strong>Email Notifications</strong>: Set up email or SMS notifications to alert reviewers when incidents are assigned or when corrective actions are overdue.</li>
</ul>

<h2>License</h2>
<p>This project is licensed under the MIT License. See the <a href="LICENSE">LICENSE</a> file for details.</p>

<h2>Contributing</h2>
<p>Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.</p>

<h2>Acknowledgements</h2>
<ul>
    <li><strong>Streamlit</strong> for the UI framework.</li>
    <li><strong>SQLAlchemy</strong> for ORM.</li>
    <li><strong>Hugging Face</strong> for the pre-trained transformer models.</li>
    <li><strong>Python-Docx</strong> for generating Word documents.</li>
</ul>

</body>
</html>
