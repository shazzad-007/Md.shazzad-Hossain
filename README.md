<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Md. Shazzad Hossain | Executive Operations & Tech Portfolio</title>
    <style>
        :root {
            --bg-dark: #0f172a;
            --bg-card: #1e293b;
            --accent-blue: #38bdf8;
            --accent-green: #4ade80;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --border: #334155;
        }
        
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { 
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; 
            color: var(--text-main); 
            background-color: var(--bg-dark);
            line-height: 1.6;
        }
        
        /* Smooth Animation Framework */
        @keyframes glowEntrance {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        @keyframes borderPulse {
            0% { border-color: var(--border); }
            50% { border-color: var(--accent-blue); }
            100% { border-color: var(--border); }
        }
        
        /* Cyber/Tech Inspired Header */
        header { 
            background: linear-gradient(180deg, #1e293b 0%, var(--bg-dark) 100%);
            border-bottom: 1px solid var(--border);
            padding: 80px 20px; 
            text-align: center;
            position: relative;
        }
        header h1 { 
            font-size: 3rem; 
            color: #ffffff;
            margin-bottom: 15px; 
            letter-spacing: -0.5px;
            font-weight: 800;
        }
        header p { 
            font-size: 1.25rem; 
            color: var(--accent-blue); 
            font-weight: 400;
            max-width: 600px;
            margin: 0 auto 30px auto;
        }

        /* Dashboard Global Print & Action Button */
        .action-container {
            margin-top: 10px;
        }
        .btn-action {
            display: inline-block;
            background: linear-gradient(135deg, #0284c7, #0369a1);
            color: white;
            padding: 14px 28px;
            font-size: 0.95rem;
            font-weight: 600;
            text-decoration: none;
            border-radius: 8px;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 12px rgba(56, 189, 248, 0.2);
        }
        .btn-action:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(56, 189, 248, 0.4);
            background: linear-gradient(135deg, #0369a1, #0284c7);
        }
        
        .container { max-width: 1000px; margin: 0 auto; padding: 50px 20px; }
        
        h2 { 
            color: #ffffff; 
            font-size: 1.75rem; 
            margin-bottom: 25px; 
            display: flex;
            align-items: center;
            gap: 10px;
        }
        h2::after {
            content: '';
            flex-grow: 1;
            height: 1px;
            background: var(--border);
        }
        
        section { 
            margin-bottom: 60px;
            animation: glowEntrance 0.8s ease-out forwards;
        }
        
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 25px; }
        
        /* Modernized Interactive Glass-style Cards */
        .card { 
            background: var(--bg-card); 
            padding: 30px; 
            border-radius: 12px; 
            border: 1px solid var(--border);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .card:hover { 
            transform: translateY(-6px);
            border-color: var(--accent-blue);
            box-shadow: 0 12px 24px rgba(0, 0, 0, 0.3);
        }
        .card h3 { color: #ffffff; margin-bottom: 12px; font-size: 1.25rem; }
        .card p { color: var(--text-muted); font-size: 0.95rem; }
        
        /* Job Timeline Nodes */
        .job-node { 
            background: var(--bg-card);
            border: 1px solid var(--border);
            padding: 30px;
            border-radius: 12px;
            margin-bottom: 25px;
            position: relative;
        }
        .job-node:hover {
            animation: borderPulse 2s infinite;
        }
        .job-header { display: flex; justify-content: space-between; flex-wrap: wrap; margin-bottom: 15px; }
        .job-title { font-weight: 700; color: #ffffff; font-size: 1.2rem; }
        .job-date { color: var(--accent-blue); font-weight: 600; font-size: 0.95rem; }
        .job-company { color: var(--text-muted); font-style: italic; margin-bottom: 15px; font-size: 1rem; }
        .job-node ul { margin-left: 20px; color: var(--text-muted); }
        .job-node li { margin-bottom: 10px; font-size: 0.95rem; }

        /* Dynamic Tech Badges */
        .badge-hub { display: flex; flex-wrap: wrap; gap: 10px; }
        .tech-tag { 
            background: #1e293b; 
            color: var(--text-main); 
            padding: 8px 16px; 
            border-radius: 20px; 
            font-size: 0.85rem; 
            font-weight: 600;
            border: 1px solid var(--border);
            transition: all 0.2s ease;
        }
        .tech-tag:hover {
            background: rgba(56, 189, 248, 0.1);
            color: var(--accent-blue);
            border-color: var(--accent-blue);
        }
        
        .status-chip {
            background: rgba(74, 222, 128, 0.1);
            color: var(--accent-green);
            border: 1px solid rgba(74, 222, 128, 0.2);
            padding: 4px 10px;
            font-size: 0.75rem;
            border-radius: 6px;
            font-weight: 700;
            display: inline-block;
            margin-bottom: 12px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .footer { text-align: center; padding: 60px 20px; border-top: 1px solid var(--border); font-size: 0.9rem; color: var(--text-muted); }
        .footer a { color: var(--accent-blue); text-decoration: none; margin: 0 15px; font-weight: 600; }
        .footer a:hover { color: #ffffff; }

        /* Native Browser to High-Fidelity PDF Engine */
        @media print {
            body { background: #ffffff !important; color: #000000 !important; }
            header { background: none !important; border-bottom: 2px solid #000000 !important; padding: 20px 0 !important; }
            header h1 { color: #000000 !important; }
            header p { color: #333333 !important; }
            .action-container, .footer { display: none !important; }
            .container { max-width: 100% !important; padding: 0 !important; }
            .card, .job-node { background: none !important; border: 1px solid #000000 !important; color: #000000 !important; page-break-inside: avoid; }
            h2 { color: #000000 !important; border-bottom: 1px solid #000000 !important; }
            .tech-tag { background: none !important; border: 1px solid #000000 !important; color: #000000 !important; }
            .status-chip { border: 1px solid #000000 !important; color: #000000 !important; }
        }
    </style>
</head>
<body>

<header>
    <h1>Md. Shazzad Hossain</h1>
    <p>Strategic Operations Leader & Remote Project Governance Consultant</p>
    <div class="action-container">
        <button class="btn-action" onclick="window.print()">📥 Export Official Verified CV (PDF)</button>
    </div>
</header>

<div class="container">
    <!-- Executive Blueprint -->
    <section>
        <h2>Executive Focus</h2>
        <p style="color: var(--text-muted); font-size: 1.05rem;">১২ বছরেরও বেশি সময় ধরে উচ্চ-শিক্ষা এবং প্রাতিষ্ঠানিক প্রশাসনিক কার্যক্রমে সফল নেতৃত্বের অভিজ্ঞতা সম্পন্ন একজন পেশাদার ম্যানেজার। মাল্টি-মিলিয়ন টাকার বাজেট পরিকল্পনা, সরকারি বা বৈশ্বিক কমপ্লায়েন্স ট্র্যাকিং এবং রিমোট-ফার্স্ট ডিজিটাল টুলসের (Git/GitHub, Generative AI Platforms) সমন্বয়ে প্রজেক্ট ম্যানেজমেন্টে পারদর্শী।</p>
    </section>

    <!-- Global Technical Core Systems -->
    <section>
        <h2>Operational Toolkit & Core Ecosystem</h2>
        <div class="badge-hub">
            <span class="tech-tag">Technical Project Management (Agile/Scrum)</span>
            <span class="tech-tag">Ecosystem Architecture (Git / GitHub Workflow)</span>
            <span class="tech-tag">AI Productivity Systems (Gemini, Grok Data Diagnostics)</span>
            <span class="tech-badge tech-tag">Financial Oversight & Cost Controls (Multi-Tier Auditing)</span>
            <span class="tech-tag">Peer Review Standards & Technical Workspace Editing</span>
            <span class="tech-tag">Vendor Contract Metrics & SLA Enforcement</span>
        </div>
    </section>

    <!-- Professional Timeline Display -->
    <section>
        <h2>Corporate Trajectory</h2>
        <div class="job-node">
            <div class="job-header">
                <span class="job-title">Senior Manager – Administration & Student Life</span>
                <span class="job-date">Nov 2012 – Nov 2024 (12 years)</span>
            </div>
            <div class="job-company">BRAC University, Dhaka</div>
            <ul>
                <li>বিশ্ববিদ্যালয়ের সরকারি ইউজিসি (UGC) কমপ্লায়েন্স নীতি এবং প্রাতিষ্ঠানিক প্রশাসনিক কার্যাবলী সরাসরি পরিচালনা করেছেন।</li>
                <li>বিভাগীয় বার্ষিক বাজেট সফলভাবে প্রণয়ন, পর্যবেক্ষণ এবং সম্পূর্ণ আর্থিক অডিট পরিচালনা করেছেন।</li>
                <li>যুগান্তকারী আন্তর্জাতিক এবং জাতীয় প্রোগ্রামগুলোর সম্পূর্ণ ভেন্ডর লজিস্টিকস এবং টিম ম্যানেজমেন্ট পরিচালনা করেছেন।</li>
            </ul>
        </div>
    </section>

    <!-- Scholarly & Remote Consulting Grid -->
    <section>
        <h2>Global Endorsements & Thought Leadership</h2>
        <div class="grid">
            <div class="card">
                <span class="status-chip">Global Appointment</span>
