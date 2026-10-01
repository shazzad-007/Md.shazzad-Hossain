    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { 
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; 
        color: var(--text-main); 
        background-color: var(--bg-dark);
        line-height: 1.6;
    }
    
    @keyframes glowEntrance {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }
    
    header { 
        background: linear-gradient(180deg, #1e293b 0%, var(--bg-dark) 100%);
        border-bottom: 1px solid var(--border);
        padding: 60px 20px; 
        text-align: center;
    }
    header h1 { font-size: 2.5rem; color: #ffffff; margin-bottom: 10px; font-weight: 800; }
    header p { color: var(--accent-blue); font-size: 1.15rem; margin-bottom: 20px; }

    .action-container { margin: 15px 0; }
    .btn-action {
        display: inline-block;
        background: linear-gradient(135deg, #27ae60, #219653);
        color: white;
        padding: 14px 28px;
        font-size: 1rem;
        font-weight: 600;
        text-decoration: none;
        border-radius: 8px;
        border: none;
        cursor: pointer;
        transition: all 0.3s ease;
        box-shadow: 0 4px 12px rgba(74, 222, 128, 0.2);
    }
    .btn-action:hover { transform: translateY(-2px); box-shadow: 0 6px 18px rgba(74, 222, 128, 0.4); }
    
    .container { max-width: 1000px; margin: 0 auto; padding: 40px 20px; }
    
    h2 { color: #ffffff; font-size: 1.6rem; margin-bottom: 20px; display: flex; align-items: center; gap: 10px; }
    h2::after { content: ''; flex-grow: 1; height: 1px; background: var(--border); }
    
    section { margin-bottom: 50px; animation: glowEntrance 0.6s ease-out forwards; }
    
    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }
    
    .card { 
        background: var(--bg-card); 
        padding: 25px; 
        border-radius: 12px; 
        border: 1px solid var(--border);
        transition: all 0.3s ease;
    }
    .card:hover { transform: translateY(-4px); border-color: var(--accent-blue); }
    .card h3 { color: #ffffff; margin-bottom: 8px; font-size: 1.2rem; }
    .card p { color: var(--text-muted); font-size: 0.9rem; }
    
    .job-node { background: var(--bg-card); border: 1px solid var(--border); padding: 25px; border-radius: 12px; margin-bottom: 20px; }
    .job-header { display: flex; justify-content: space-between; flex-wrap: wrap; margin-bottom: 10px; }
    .job-title { font-weight: 700; color: #ffffff; font-size: 1.15rem; }
    .job-date { color: var(--accent-blue); font-weight: 600; font-size: 0.9rem; }
    .job-company { color: var(--text-muted); font-style: italic; margin-bottom: 10px; }
    .job-node ul, .section-list { margin-left: 20px; color: var(--text-muted); }
    .job-node li, .section-list li { margin-bottom: 8px; font-size: 0.95rem; }

    .tech-tag { 
        display: inline-block; background: #1e293b; color: var(--text-main); padding: 6px 14px; 
        border-radius: 20px; font-size: 0.85rem; border: 1px solid var(--border); margin: 4px;
    }
    .status-chip {
        background: rgba(56, 189, 248, 0.1); color: var(--accent-blue); border: 1px solid rgba(56, 189, 248, 0.2);
        padding: 4px 10px; font-size: 0.75rem; border-radius: 6px; font-weight: 700; display: inline-block; margin-bottom: 10px; text-transform: uppercase;
    }
    
    /* Private Note Box */
    .private-note-box {
        background: rgba(3, 105, 161, 0.15);
        border: 1px dashed var(--accent-blue);
        padding: 25px;
        border-radius: 12px;
        margin-top: 30px;
    }
    .private-note-box h4 { color: var(--accent-blue); margin-bottom: 10px; font-size: 1.1rem; }
    .private-note-box p { color: var(--text-main); font-size: 0.95rem; font-style: italic; }

    .footer { text-align: center; padding: 40px 20px; border-top: 1px solid var(--border); font-size: 0.9rem; color: var(--text-muted); }
    .footer a { color: var(--accent-blue); text-decoration: none; margin: 0 15px; }

    @media print {
        body { background: #ffffff !important; color: #000000 !important; }
        header { background: none !important; border-bottom: 2px solid #000000 !important; padding: 20px 0 !important; }
        header h1 { color: #000000 !important; }
        .action-container, .footer { display: none !important; }
        .container { max-width: 100% !important; padding: 0 !important; }
        .card, .job-node, .private-note-box { background: none !important; border: 1px solid #000000 !important; color: #000000 !important; page-break-inside: avoid; }
        .private-note-box h4 { color: #000000 !important; font-weight: bold; }
        h2 { color: #000000 !important; border-bottom: 1px solid #000000 !important; }
        .tech-tag, .status-chip { background: none !important; border: 1px solid #000000 !important; color: #000000 !important; }
    }
</style>
