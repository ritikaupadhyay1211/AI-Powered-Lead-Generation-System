<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI-Powered Lead Management & Security Infrastructure</title>
    <style>
        :root {
            --primary: #0176D3; /* Salesforce Blue */
            --primary-dark: #014486;
            --accent: #00A1E0; /* Einstein/Agentforce Cyan */
            --bg-dark: #0B192C; /* Deep Tech Blue */
            --bg-card: #1E3E62; /* Card Blue */
            --text-light: #F5F7F8;
            --text-muted: #B0C4DE;
            --success: #2E7D32;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-light);
            line-height: 1.6;
            padding-bottom: 60px;
        }

        /* Hero Section */
        header {
            background: linear-gradient(135deg, rgba(1, 118, 211, 0.95), rgba(11, 25, 44, 0.95)), 
                        radial-gradient(circle at 80% 20%, var(--accent), transparent 40%);
            padding: 80px 20px;
            text-align: center;
            border-bottom: 4px solid var(--accent);
            position: relative;
            overflow: hidden;
        }

        .badge {
            background: rgba(255, 255, 255, 0.15);
            border: 1px solid rgba(255, 255, 255, 0.3);
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            display: inline-block;
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        header h1 {
            font-size: 2.8rem;
            margin-bottom: 15px;
            font-weight: 700;
            letter-spacing: -0.5px;
        }

        header p {
            font-size: 1.2rem;
            color: var(--text-muted);
            max-width: 800px;
            margin: 0 auto 30px;
        }

        .author-tag {
            font-weight: 600;
            color: #FFF;
            background: var(--accent);
            padding: 4px 12px;
            border-radius: 4px;
        }

        /* Container Layout */
        .container {
            max-width: 1100px;
            margin: 40px auto;
            padding: 0 20px;
        }

        h2 {
            font-size: 1.8rem;
            margin: 40px 0 20px;
            padding-bottom: 8px;
            border-bottom: 2px solid rgba(255, 255, 255, 0.1);
            color: var(--accent);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* Grid Framework */
        .grid-2 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }

        .grid-3 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        /* Cards & Interactive Elements */
        .card {
            background-color: var(--bg-card);
            border-radius: 8px;
            padding: 25px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .card:hover {
            transform: translateY(-4px);
            box-shadow: 0 8px 25px rgba(0, 161, 224, 0.2);
            border-color: rgba(0, 161, 224, 0.4);
        }

        .card h3 {
            margin-bottom: 15px;
            color: #FFF;
            font-size: 1.25rem;
        }

        /* Lists */
        ul {
            list-style: none;
        }

        ul li {
            position: relative;
            padding-left: 25px;
            margin-bottom: 10px;
            color: var(--text-muted);
        }

        ul li::before {
            content: "✓";
            position: absolute;
            left: 0;
            color: var(--accent);
            font-weight: bold;
        }

        /* Interactive Hierarchy Chart */
        .hierarchy-box {
            background: rgba(0,0,0,0.2);
            border-radius: 8px;
            padding: 30px;
            text-align: center;
            margin: 20px 0;
        }

        .node {
            background: var(--primary);
            padding: 12px 25px;
            border-radius: 6px;
            display: inline-block;
            font-weight: bold;
            box-shadow: 0 2px 8px rgba(0,0,0,0.3);
            min-width: 180px;
        }
        
        .node.manager { background: var(--bg-card); border: 2px solid var(--primary); }
        .node.agent { background: rgba(255,255,255,0.05); border: 1px dashed var(--text-muted); }

        .connector {
            width: 2px;
            height: 30px;
            background: var(--accent);
            margin: 0 auto;
        }

        /* Table Design */
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: var(--bg-card);
            border-radius: 8px;
            overflow: hidden;
        }

        th, td {
            padding: 15px;
            text-align: left;
        }

        th {
            background-color: var(--primary);
            color: white;
            font-weight: 600;
        }

        tr {
            border-bottom: 1px solid rgba(255,255,255,0.05);
        }

        tr:last-child {
            border-bottom: none;
        }

        /* Repo Folders Visualizer */
        .folder-structure {
            background: #050C14;
            padding: 20px;
            border-radius: 8px;
            font-family: 'Courier New', Courier, monospace;
            color: #39FF14; /* Neon Green tech vibe */
            overflow-x: auto;
        }

        /* Tag Pill Badges */
        .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }

        .tag {
            background: rgba(255,255,255,0.08);
            padding: 6px 12px;
            border-radius: 4px;
            font-size: 0.85rem;
            color: var(--text-muted);
            border: 1px solid rgba(255,255,255,0.1);
        }

        /* Responsive Fixes */
        @media (max-width: 768px) {
            header h1 { font-size: 2rem; }
            .grid-2, .grid-3 { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

    <header>
        <div class="badge">Virtual Internship Submission</div>
        <h1>AI-Powered Lead Management & Security Infrastructure</h1>
        <p>Developed during the Salesforce Certified Administrator with AI Agentforce Specialization Virtual Internship using Salesforce Developer Edition.</p>
        <div>
            <span>Architected by: </span><span class="author-tag">Ritika Upadhyay</span>
        </div>
    </header>

    <div class="container">

        <!-- Project Overview -->
        <section>
            <h2>🚀 Project Overview</h2>
            <div class="card" style="background: linear-gradient(to right, var(--bg-card), rgba(1, 118, 211, 0.1));">
                <p>The core objective of this project was to build a highly secure, automated, and AI-powered Lead Management System. By customizing the standard Salesforce Lead object, enforcing tight role-based security configurations, and deploying <strong>Salesforce Prompt Builder</strong>, this ecosystem dynamically delivers Einstein AI-generated Lead summaries directly into Lightning record pages to supercharge sales productivity.</p>
            </div>
        </section>

        <!-- Project Objectives & Outcomes -->
        <div class="grid-2">
            <section>
                <h2>🎯 Project Objectives</h2>
                <div class="card" style="height: calc(100% - 60px);">
                    <ul>
                        <li>Configure Salesforce Developer Environment.</li>
                        <li>Deeply customize the Standard Lead Object layout.</li>
                        <li>Create operational Profiles, Users, and Roles.</li>
                        <li>Enforce multi-layered Role-Based Security.</li>
                        <li>Deploy Prompt Builder for generative AI workflows.</li>
                        <li>Build high-utility Lightning Record Pages.</li>
                    </ul>
                </div>
            </section>

            <section>
                <h2>📚 Key Learning Outcomes</h2>
                <div class="card" style="height: calc(100% - 60px);">
                    <ul>
                        <li>CRM Architecture & Object Customization</li>
                        <li>Advanced User & Access Management</li>
                        <li>Granular Permission Sets & Security Layers</li>
                        <li>Salesforce Einstein AI & Generative Workflows</li>
                        <li>Prompt Template Engineering & Activation</li>
                        <li>Lightning App Builder UX Orchestration</li>
                    </ul>
                </div>
            </section>
        </div>

        <!-- Features Implemented -->
        <section>
            <h2>🛠️ Features Implemented</h2>
            <div class="grid-3">
                <div class="card">
                    <h3>Lead Management</h3>
                    <ul>
                        <li>Custom Lead fields architecture</li>
                        <li>Tailored Page Layout designs</li>
                        <li>Optimized record management flows</li>
                    </ul>
                </div>
                <div class="card">
                    <h3>Security Ecosystem</h3>
                    <ul>
                        <li>Custom Profiles assignment</li>
                        <li>Granular Field-Level Security</li>
                        <li>Advanced Role Hierarchy mapping</li>
                    </ul>
                </div>
                <div class="card">
                    <h3>AI & Automation</h3>
                    <ul>
                        <li>Einstein Generative AI activation</li>
                        <li>Field Generation Prompt Templates</li>
                        <li>One-click Lightning UI summary engine</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Security Profile Matrix -->
        <section>
            <h2>🔒 Security Configuration Matrix</h2>
            <table>
                <thead>
                    <tr>
                        <th>Profile / Role</th>
                        <th>Object Permissions (Lead, Task, Contact, Event)</th>
                        <th>Functional Scope</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <strong><td>Lead Manager</td></strong>
                        <td>Read, Create, Edit, Delete (Full Access)</td>
                        <td>Complete record lifecycles oversight and operational pipeline audits.</td>
                    </tr>
                    <tr>
                        <strong><td>Sales Agent</td></strong>
                        <td>Read, Create, Edit (Restricted Deletion)</td>
                        <td>Active prospecting, day-to-day lead processing, task execution.</td>
                    </tr>
                </tbody>
            </table>

            <!-- Interactive Role Hierarchy Visualization -->
            <div class="hierarchy-box">
                <div class="node">VP of Sales</div>
                <div class="connector"></div>
                <div class="node manager">Lead Manager</div>
                <div class="connector"></div>
                <div class="node agent">Sales Agent</div>
            </div>
        </section>

        <!-- Business Value -->
        <section>
            <h2>📈 Quantifiable Business Value</h2>
            <div class="grid-2">
                <div class="card">
                    <h3>Data Protection</h3>
                    <p>Secures sensitive customer pipeline data using precision-engineered Object-Level security policies, guaranteeing zero data leakage across functional roles.</p>
                </div>
                <div class="card">
                    <h3>AI Productivity Injection</h3>
                    <p>Eliminates manual file synthesis by letting Einstein automatically aggregate customer context into clean summaries, shifting administrative burden off active agents.</p>
                </div>
            </div>
        </section>

        <!-- Tools and Repos -->
        <div class="grid-2">
            <section>
                <h2>🛠️ Tools & Technologies Used</h2>
                <div class="card" style="height: calc(100% - 60px);">
                    <div class="tech-tags">
                        <span class="tag">Salesforce Developer Edition</span>
                        <span class="tag">Salesforce Lightning Experience</span>
                        <span class="tag">Salesforce Prompt Builder</span>
                        <span class="tag">Salesforce Einstein AI</span>
                        <span class="tag">Lightning App Builder</span>
                        <span class="tag">GitHub Version Control</span>
                        <span class="tag">Microsoft Word</span>
                    </div>
                </div>
            </section>

            <section>
                <h2>📂 Repository Structure</h2>
                <div class="folder-structure" style="height: calc(100% - 60px);">
AI-Powered-Lead-Management-System/
├── README.md
├── Documentation.pdf
├── Screenshots/
│   ├── Home_Page_&_Launcher.png
│   ├── Profiles_&_Users_List.png
│   ├── Role_Hierarchy.png
│   ├── Lead_Object_Customization.png
│   └── Prompt_Builder_&_AI_Summary.png
└── Demo_Video_Link.txt
                </div>
            </section>
        </div>

    </div>
</body>
</html>
