---
layout: default
title: Cybersecurity Articles & Walkthroughs
---

<style>
  * { margin: 0; padding: 0; }
  
  .hero {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 50px 20px;
    text-align: center;
    border-radius: 8px;
    margin-bottom: 40px;
  }
  
  .hero h1 { font-size: 2.5em; margin-bottom: 10px; }
  .hero p { font-size: 1.1em; opacity: 0.95; }
  
  .stats {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    margin: 30px 0;
  }
  
  .stat { text-align: center; padding: 20px; }
  .stat-number { font-size: 32px; font-weight: bold; }
  .stat-label { font-size: 14px; opacity: 0.9; }
  
  .cta-buttons {
    margin-top: 25px;
    display: flex;
    justify-content: center;
    gap: 10px;
    flex-wrap: wrap;
  }
  
  .btn {
    padding: 10px 20px;
    border-radius: 25px;
    text-decoration: none;
    font-weight: bold;
    transition: all 0.3s;
    display: inline-block;
  }
  
  .btn-white { background: white; color: #667eea; }
  .btn-white:hover { transform: scale(1.05); }
  
  .section-title {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 20px;
    border-radius: 6px;
    margin: 40px 0 25px 0;
    font-size: 1.8em;
  }
  
  .content-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
    margin-bottom: 30px;
  }
  
  .card {
    background: white;
    border-left: 4px solid #667eea;
    padding: 20px;
    border-radius: 6px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    transition: all 0.3s;
    text-decoration: none;
    color: inherit;
    display: block;
  }
  
  .card:hover {
    transform: translateY(-5px);
    box-shadow: 0 6px 12px rgba(0,0,0,0.15);
    border-left-color: #764ba2;
  }
  
  .card h3 { color: #667eea; margin-bottom: 10px; font-size: 1.1em; }
  .card p { color: #666; font-size: 0.95em; line-height: 1.5; }
  
  .badge {
    display: inline-block;
    background: #667eea;
    color: white;
    padding: 4px 10px;
    border-radius: 12px;
    font-size: 0.8em;
    margin: 8px 5px 0 0;
  }
  
  .badge-articles { background: #f5576c; }
  .badge-walkthrough { background: #ff9a56; }
  .badge-track { background: #2ecc71; }
  .badge-beginner { background: #667eea; }
  .badge-intermediate { background: #764ba2; }
  .badge-advanced { background: #d63031; }
  .badge-coming { background: #bbb; }
  
  .subsection {
    margin: 20px 0;
    padding: 20px;
    background: #f8f9fa;
    border-radius: 6px;
  }
  
  .subsection h4 { color: #667eea; margin-bottom: 15px; font-size: 1.1em; }
  
  .week-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 15px;
  }
  
  .week-card {
    background: white;
    border-left: 4px solid #2ecc71;
    padding: 15px;
    border-radius: 6px;
    box-shadow: 0 2px 6px rgba(0,0,0,0.08);
    transition: all 0.3s;
  }
  
  .week-card.coming-soon {
    border-left-color: #bbb;
    opacity: 0.7;
  }
  
  .week-card a {
    color: #667eea;
    text-decoration: none;
    font-weight: 500;
    display: block;
    margin: 8px 0;
    transition: all 0.2s;
  }
  
  .week-card a:hover { color: #764ba2; padding-left: 5px; }
  
  .week-card strong { display: block; margin-bottom: 8px; color: #333; }
  
  .coming-soon-text {
    color: #999;
    font-size: 0.9em;
    font-style: italic;
  }
  
  .footer {
    margin-top: 60px;
    padding: 30px 0;
    border-top: 2px solid #ddd;
    text-align: center;
    color: #666;
  }
  
  @media (max-width: 768px) {
    .hero h1 { font-size: 1.8em; }
    .content-grid { grid-template-columns: 1fr; }
    .stats { flex-direction: column; }
  }
</style>

<div class="hero">
  <h1>🛡️ Cybersecurity Learning Hub</h1>
  <p>Comprehensive notes, walkthroughs, and hands-on labs for security professionals in training</p>
  
  <div class="stats">
    <div class="stat">
      <div class="stat-number">15+</div>
      <div class="stat-label">Learning Modules</div>
    </div>
    <div class="stat">
      <div class="stat-number">3</div>
      <div class="stat-label">Lab Guides</div>
    </div>
    <div class="stat">
      <div class="stat-number">100+</div>
      <div class="stat-label">Q&A + Walkthroughs</div>
    </div>
  </div>
  
  <div class="cta-buttons">
    <a href="https://github.com/josephkilatya/Cybersecurity-Articles" class="btn btn-white">🔗 GitHub Repository</a>
    <a href="https://tryhackme.com/p/kl45h" class="btn btn-white">🎯 TryHackMe Profile</a>
  </div>
</div>

---

# 📚 Complete Content Directory

## 🏗️ Lab Building Guides

These comprehensive guides help you set up professional-grade cybersecurity labs for hands-on learning.

<div class="content-grid">
  <a href="Articles/FLARE-VM%20-%20Building%20A%20Malware%20Analysis%20Lab.md" class="card">
    <h3>🔬 FLARE-VM Malware Analysis Lab</h3>
    <p>Set up Mandiant's FLARE-VM (Forward-Looking Adversary Resistance Engineering) on VirtualBox. Learn reverse engineering and malware analysis in a sandboxed Windows environment with professional-grade tools.</p>
    <span class="badge badge-articles">Lab Guide</span>
    <span class="badge badge-advanced">Advanced</span>
  </a>
  
  <a href="Articles/Building%20a%20SIEM-EDR%20Lab%20with%20Wazuh.md" class="card">
    <h3>🔐 SIEM-EDR Lab with Wazuh</h3>
    <p>Build an enterprise-grade security monitoring lab using Wazuh. Covers virtual network setup, Windows endpoint configuration, and security event collection.</p>
    <span class="badge badge-articles">Lab Guide</span>
    <span class="badge badge-advanced">Advanced</span>
  </a>
  
  <a href="Articles/Building%20A%20Basic%20Penetration%20Testing%20Lab:%20Parrot%20OS%20and%20Metasploitable.md" class="card">
    <h3>🔨 Penetration Testing Lab</h3>
    <p>Create a beginner-friendly penetration testing environment using Parrot OS and Metasploitable. Complete setup instructions for your first pentest lab.</p>
    <span class="badge badge-articles">Lab Guide</span>
    <span class="badge badge-beginner">Beginner</span>
  </a>
</div>

---

## 🔍 Walkthroughs & Writeups

Step-by-step solutions and explanations for hands-on security challenges.

<div class="content-grid">
  <a href="Walkthroughs/TryHackMe/CyberChef:%20The%20Basics.md" class="card">
    <h3>🍳 CyberChef: The Basics</h3>
    <p>Master CyberChef, the Swiss Army knife for data analysis and encoding. Learn encoding/decoding, hashing, encryption, and data manipulation techniques with practical examples.</p>
    <span class="badge badge-walkthrough">TryHackMe Walkthrough</span>
    <span class="badge badge-beginner">Beginner</span>
  </a>
</div>

---

## 🎓 Cyber Shujaa Security Analyst Track

A comprehensive 12-week program covering cybersecurity fundamentals from Python scripting to malware analysis.

**Track Progress:** Weeks 1-12 | **TryHackMe Profile:** [kl45h](https://tryhackme.com/p/kl45h)

<div class="subsection">
  <h4>📖 Week 1: Computing Essentials</h4>
  <p style="color: #666; margin-bottom: 15px;">Foundation of IT concepts and computer operations</p>
  
  <div class="week-grid">
    <div class="week-card coming-soon">
      <strong>💻 Computing Fundamentals</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
  </div>
</div>

<div class="subsection">
  <h4>🔐 Week 2: Cyber Security Essentials</h4>
  <p style="color: #666; margin-bottom: 15px;">Introduction to core cybersecurity concepts, threats, and defenses</p>
  
  <div class="week-grid">
    <div class="week-card coming-soon">
      <strong>🛡️ Security Fundamentals</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
  </div>
</div>

<div class="subsection">
  <h4>📖 Week 3: Reconnaissance and OSINT</h4>
  <p style="color: #666; margin-bottom: 15px;">Master reconnaissance techniques and open-source intelligence gathering</p>
  
  <div class="week-grid">
    <div class="week-card">
      <strong>🐍 Python Basics</strong>
      <a href="Cyber%20Shujaa%20-%20Security%20Analyst%20Track/Week%203%20-%20Reconnaissance%20and%20OSINT/Assignment%201%20-%20Python%20Scripting/Python%20Basics.md">
        Variables, data types, loops, functions, file I/O
      </a>
      <span class="badge badge-beginner">Beginner</span>
    </div>
    
    <div class="week-card">
      <strong>🔍 Red Team Recon</strong>
      <a href="Cyber%20Shujaa%20-%20Security%20Analyst%20Track/Week%203%20-%20Reconnaissance%20and%20OSINT/Assignment%202%20-%20Red%20Team%20Recon/Red%20Team%20Recon%20-%20THM.md">
        Google dorking, Shodan, Censys, recon-ng, Maltego
      </a>
      <span class="badge badge-intermediate">Intermediate</span>
    </div>
  </div>
</div>

<div class="subsection">
  <h4>🌐 Week 4: Scanning and Enumeration</h4>
  <p style="color: #666; margin-bottom: 15px;">Understand networking and enumeration techniques</p>
  
  <div class="week-grid">
    <div class="week-card">
      <strong>🌍 Introduction to Networking</strong>
      <a href="Cyber%20Shujaa%20-%20Security%20Analyst%20Track/Week%204%20-%20Scanning%20and%20Enumeration/Assignemt%201%20-%20Introduction%20to%20Networking/Introduction%20to%20Networking%20Module%20-%20HTB.md">
        Network types, topologies, OSI model, TCP/IP, subnetting
      </a>
      <span class="badge badge-beginner">Beginner</span>
    </div>
    
    <div class="week-card">
      <strong>🔗 DNS in Detail</strong>
      <a href="Cyber%20Shujaa%20-%20Security%20Analyst%20Track/Week%204%20-%20Scanning%20and%20Enumeration/Assignemt%202%20-%20DNS%20in%20details/DNS%20in%20detail%20Room%20-%20THM.md">
        DNS hierarchy, record types, DNS enumeration
      </a>
      <span class="badge badge-intermediate">Intermediate</span>
    </div>
  </div>
</div>

<div class="subsection">
  <h4>🔐 Week 5: Vulnerability Assessment</h4>
  <p style="color: #666; margin-bottom: 15px;">Learn vulnerability scanning and assessment methodologies</p>
  
  <div class="week-grid">
    <div class="week-card">
      <strong>🛠️ Vulnerability Assessment</strong>
      <a href="Cyber%20Shujaa%20-%20Security%20Analyst%20Track/Week%205%20-%20Vulnerablity%20Assessment/Assignment%202%20-%20Vulnerability%20Assessment/Vulnerability%20Assessment%20Module%20-%20HTB.md">
        Nessus, OpenVAS, CVSS scoring, vulnerability reporting
      </a>
      <span class="badge badge-intermediate">Intermediate</span>
    </div>
    
    <div class="week-card coming-soon">
      <strong>🎯 Threat Intelligence Tools</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
  </div>
</div>

<div class="subsection">
  <h4>🔐 Week 6: Access Control Security</h4>
  <p style="color: #666; margin-bottom: 15px;">Authentication, authorization, and identity management</p>
  
  <div class="week-grid">
    <div class="week-card coming-soon">
      <strong>🔑 IAM & Authentication</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
    
    <div class="week-card coming-soon">
      <strong>👥 Access Control Models</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
  </div>
</div>

<div class="subsection">
  <h4>🌐 Week 7: Web Application Security</h4>
  <p style="color: #666; margin-bottom: 15px;">OWASP Top 10, web vulnerabilities, secure coding</p>
  
  <div class="week-grid">
    <div class="week-card coming-soon">
      <strong>🔓 Web Vulnerabilities</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
    
    <div class="week-card coming-soon">
      <strong>🛡️ OWASP Top 10</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
  </div>
</div>

<div class="subsection">
  <h4>💾 Week 8: Database Security</h4>
  <p style="color: #666; margin-bottom: 15px;">Database security principles and SQL injection prevention</p>
  
  <div class="week-grid">
    <div class="week-card coming-soon">
      <strong>🗄️ Database Protection</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
    
    <div class="week-card coming-soon">
      <strong>💉 SQL Injection Prevention</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
  </div>
</div>

<div class="subsection">
  <h4>📶 Week 9: Wireless Network Security</h4>
  <p style="color: #666; margin-bottom: 15px;">WiFi security, encryption, and wireless attacks</p>
  
  <div class="week-grid">
    <div class="week-card coming-soon">
      <strong>📡 WiFi Security</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
    
    <div class="week-card coming-soon">
      <strong>🔐 Wireless Encryption</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
  </div>
</div>

<div class="subsection">
  <h4>🛡️ Week 10: Security Operations and Monitoring</h4>
  <p style="color: #666; margin-bottom: 15px;">SIEM, logging, event analysis, and incident response</p>
  
  <div class="week-grid">
    <div class="week-card coming-soon">
      <strong>📊 SIEM Fundamentals</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
    
    <div class="week-card coming-soon">
      <strong>🚨 Incident Response</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
  </div>
</div>

<div class="subsection">
  <h4>🔎 Week 11: Digital Forensics</h4>
  <p style="color: #666; margin-bottom: 15px;">Evidence collection, analysis, and chain of custody</p>
  
  <div class="week-grid">
    <div class="week-card coming-soon">
      <strong>🔍 Evidence Collection</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
    
    <div class="week-card coming-soon">
      <strong>⛓️ Chain of Custody</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
  </div>
</div>

<div class="subsection">
  <h4>🦠 Week 12: Malware Analysis</h4>
  <p style="color: #666; margin-bottom: 15px;">Static and dynamic malware analysis techniques</p>
  
  <div class="week-grid">
    <div class="week-card coming-soon">
      <strong>🔬 Static Analysis</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
    
    <div class="week-card coming-soon">
      <strong>⚙️ Dynamic Analysis</strong>
      <p class="coming-soon-text">📝 Content Coming Soon</p>
      <span class="badge badge-coming">In Development</span>
    </div>
  </div>
</div>

---

<div class="footer">
  <h3>📖 How to Use This Site</h3>
  <p style="margin: 15px 0;">Click on any article or lab guide above to access the full content with detailed walkthroughs, screenshots, and practical examples.</p>
  
  <p style="margin: 20px 0;">Each resource includes:</p>
  <ul style="text-align: left; display: inline-block; margin: 10px 0; list-style: none;">
    <li>✅ Complete theory and explanations</li>
    <li>✅ Step-by-step instructions</li>
    <li>✅ Screenshots and visual aids</li>
    <li>✅ Answers and solutions</li>
    <li>✅ Key takeaways</li>
  </ul>
  
  <hr style="margin: 30px 0; border: none; border-top: 1px solid #ddd;">
  
  <p>
    <strong>Want to learn more?</strong><br>
    <a href="https://github.com/josephkilatya/Cybersecurity-Articles">View on GitHub</a> • 
    <a href="https://tryhackme.com/p/kl45h">Follow on TryHackMe</a>
  </p>
  
  <p style="margin-top: 20px; font-size: 0.9em; color: #999;">
    Built with 🔐 for the cybersecurity community | Last updated: June 2026
  </p>
</div>
