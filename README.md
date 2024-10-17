<h1>Email Personalization Project</h1>
<p>This project aims to automate the generation of personalized email messages based on a list of email addresses provided in a CSV file. The emails are grouped by domain, and each user receives a customized message.</p>

<h2>Table of Contents</h2>
<ul>
    <li><a href="#features">Features</a></li>
    <li><a href="#technologies">Technologies</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#file-structure">File Structure</a></li>
    <li><a href="#setup">Setup</a></li>
    <li><a href="#running-the-project">Running the Project</a></li>
    <li><a href="#license">License</a></li>
</ul>

<h2 id="features">Features</h2>
<ul>
    <li><strong>Group emails by domain</strong>: Emails are automatically grouped by their domain (e.g., gmail.com, yahoo.com) for easy management.</li>
    <li><strong>Personalized messages</strong>: Automatically generate and customize email messages with user-specific data, such as names and providers.</li>
    <li><strong>Flexible domain handling</strong>: The system supports any email provider and dynamically adapts to new domains found in the provided list.</li>
    <li><strong>Custom message template</strong>: Allows you to define custom templates for the messages, replacing placeholders with the actual user information.</li>
</ul>

<h2 id="technologies">Technologies</h2>
<ul>
    <li><strong>Python 3.x</strong></li>
    <li><strong>Regular expressions (re)</strong> for domain and user extraction.</li>
    <li><strong>pandas</strong> for reading and processing the CSV file.</li>
    <li><strong>re</strong> for text substitution and template customization.</li>
</ul>

<h2 id="usage">Usage</h2>
<p>1. <strong>Email List Processing</strong>: The project takes a CSV file with email addresses, splits them by domain, and creates a dictionary of users organized by their email providers.</p>
<p>2. <strong>Message Personalization</strong>: The system replaces placeholders like <code>{nombre}</code> and <code>{proveedor}</code> in the message template with the actual user names and providers.</p>
<p>3. <strong>Output</strong>: A custom message is generated for each user and saved to individual <code>.txt</code> files.</p>

<h3>Example</h3>
<p>Given the following email list:</p>

<pre>
<code>
email
john.doe@gmail.com
jane.smith@yahoo.com
admin@customdomain.com
</code>
</pre>

<p>The system will generate personalized messages for each user like:</p>

<pre>
<code>
Buenos dias John,

Gracias por elegir Gmail como tu proveedor de mensajes.
Un cordial saludo
</code>
</pre>

<h2 id="file-structure">File Structure</h2>
<pre>
<code>
├── email_personalization.py   # Main script with the Email class
├── emails.csv                 # Input file containing the list of emails
├── mensaje_generico.txt       # Template for the custom email message
└── README.md                  # This file
</code>
</pre>

<h2 id="setup">Setup</h2>
<ol>
    <li>Clone this repository to your local machine:
        <pre><code>git clone https://github.com/yourusername/email-personalization.git
cd email-personalization
</code></pre>
    </li>
    <li>Install necessary dependencies (if any):
        <pre><code>pip install pandas</code></pre>
    </li>
    <li>Prepare your CSV file with the list of emails. For example, <code>emails.csv</code> should look like:
        <pre><code>email
john.doe@gmail.com
jane.smith@yahoo.com
admin@customdomain.com
</code></pre>
    </li>
    <li>Customize the <code>mensaje_generico.txt</code> file to include your desired message format, using placeholders like <code>{nombre}</code> and <code>{proveedor}</code>.</li>
</ol>

<h2 id="running-the-project">Running the Project</h2>
<p>To run the project:</p>
<ol>
    <li>Ensure the <code>emails.csv</code> file is properly formatted.</li>
    <li>Execute the Python script:
        <pre><code>python email_personalization.py</code></pre>
    </li>
</ol>
<p>This will generate personalized email messages for each user and save them to <code>.txt</code> files.</p>

<h2 id="license">License</h2>
<p>This project is licensed under the MIT License.</p>
