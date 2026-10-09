<!-- ANIMATED BACKGROUND -->
<style>
  @keyframes gradient-shift {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }
  
  @keyframes float-in {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }
  
  @keyframes pulse-glow {
    0%, 100% { box-shadow: 0 0 20px rgba(0, 212, 255, 0.3); }
    50% { box-shadow: 0 0 30px rgba(255, 111, 97, 0.5); }
  }
  
  @keyframes slide-up {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }
  
  @keyframes shimmer {
    0% { background-position: -1000px 0; }
    100% { background-position: 1000px 0; }
  }
  
  @keyframes border-glow {
    0%, 100% { border-left-color: currentColor; box-shadow: 0 0 10px rgba(0, 212, 255, 0.2); }
    50% { box-shadow: 0 0 20px rgba(255, 111, 97, 0.4); }
  }
  
  @keyframes rotate-gradient {
    0% { background-position: 0% 0%; }
    50% { background-position: 100% 100%; }
    100% { background-position: 0% 0%; }
  }
  
  body {
    background: #0D1117;
  }
  
  .profile-header {
    animation: float-in 1s ease-out;
  }
  
  .animated-section-bg {
    background: linear-gradient(-45deg, 
      rgba(102, 126, 234, 0.08), 
      rgba(255, 111, 97, 0.08), 
      rgba(42, 82, 152, 0.08), 
      rgba(116, 75, 162, 0.08),
      rgba(0, 212, 255, 0.08));
    background-size: 400% 400%;
    animation: gradient-shift 15s ease infinite;
    position: relative;
    overflow: hidden;
  }
  
  .animated-section-bg::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(circle at 20% 50%, rgba(0, 212, 255, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 50%, rgba(255, 111, 97, 0.1) 0%, transparent 50%);
    animation: rotate-gradient 20s ease infinite;
    pointer-events: none;
  }
  
  .projects-grid-container {
    padding: 40px 20px;
    border-radius: 15px;
    margin: 25px 0;
  }
  
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 24px;
    max-width: 1200px;
    margin: 0 auto;
    position: relative;
    z-index: 1;
  }
  
  .project-card {
    background: rgba(15, 23, 42, 0.8);
    backdrop-filter: blur(20px);
    padding: 24px;
    border-radius: 12px;
    border-left: 4px solid #00D4FF;
    animation: slide-up 0.6s ease-out backwards;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    border: 1px solid rgba(0, 212, 255, 0.1);
    position: relative;
    overflow: hidden;
  }
  
  .project-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
    animation: shimmer 3s infinite;
  }
  
  .project-card:nth-child(1) { 
    animation-delay: 0.1s; 
    border-left-color: #00D4FF;
    --glow-color: rgba(0, 212, 255, 0.2);
  }
  .project-card:nth-child(2) { 
    animation-delay: 0.2s; 
    border-left-color: #FF6F61;
    --glow-color: rgba(255, 111, 97, 0.2);
  }
  .project-card:nth-child(3) { 
    animation-delay: 0.3s; 
    border-left-color: #2A5298;
    --glow-color: rgba(42, 82, 152, 0.2);
  }
  .project-card:nth-child(4) { 
    animation-delay: 0.4s; 
    border-left-color: #764BA2;
    --glow-color: rgba(116, 75, 162, 0.2);
  }
  .project-card:nth-child(5) { 
    animation-delay: 0.5s; 
    border-left-color: #00D4FF;
    --glow-color: rgba(0, 212, 255, 0.2);
  }
  .project-card:nth-child(6) { 
    animation-delay: 0.6s; 
    border-left-color: #F7DF1E;
    --glow-color: rgba(247, 223, 30, 0.2);
  }
  
  .project-card:hover {
    transform: translateY(-12px);
    border-left-width: 6px;
    background: rgba(15, 23, 42, 0.95);
    border: 1px solid rgba(0, 212, 255, 0.3);
    box-shadow: 
      0 20px 40px rgba(0, 212, 255, 0.15),
      inset 0 1px 0 rgba(255, 255, 255, 0.1);
  }
  
  .project-card:hover::before {
    animation: shimmer 1.5s infinite;
  }
  
  .project-title {
    font-size: 1.2em;
    font-weight: 700;
    margin-bottom: 8px;
    color: #fff;
    letter-spacing: 0.5px;
  }
  
  .project-description {
    color: #b1bcc9;
    font-size: 0.9em;
    margin: 8px 0;
  }
  
  .project-badges {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin: 12px 0;
  }
  
  .project-links {
    display: flex;
    gap: 8px;
    margin-top: 12px;
    flex-wrap: wrap;
  }
  
  .project-links a {
    color: #00D4FF;
    text-decoration: none;
    font-size: 0.9em;
    padding: 4px 12px;
    border: 1px solid rgba(0, 212, 255, 0.3);
    border-radius: 6px;
    transition: all 0.2s ease;
  }
  
  .project-links a:hover {
    background: rgba(0, 212, 255, 0.1);
    border-color: rgba(0, 212, 255, 0.6);
  }
  
  .section-header {
    animation: float-in 0.8s ease-out;
  }
  
  .tech-stack-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 12px;
    margin: 20px 0;
  }
  
  .badge-glow {
    animation: pulse-glow 3s ease-in-out infinite;
  }
</style>

<div align="center" class="profile-header">
  
  <!-- Animated greeting -->
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=28&duration=4000&pause=1000&color=00D4FF&center=true&vCenter=true&width=600&lines=Hi+👋+I'm+Sathish+Sivakumar;Technical+Leader+%26+Full-Stack+Architect" alt="Typing Animation" />
  
  <p style="margin: 15px 0;">
    <img src="https://img.shields.io/badge/Focus-Mobile%20%26%20Web%20Architecture-00D4FF?style=flat-square&logo=target" class="badge-glow" />
    <img src="https://img.shields.io/badge/Experience-8%2B%20Years-FF6F61?style=flat-square&logo=calendar" class="badge-glow" />
    <img src="https://img.shields.io/badge/Based%20In-India-%F74C1C?style=flat-square&logo=mapbox" class="badge-glow" />
  </p>

  <!-- Quick Links -->
  <div style="margin: 20px 0; display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
    <a href="https://sathish-portfolio-website.onrender.com/" target="_blank" style="text-decoration: none;">
      <img alt="Portfolio" src="https://img.shields.io/badge/🌐_Portfolio-Visit-00D4FF?style=for-the-badge&logoColor=white" />
    </a>
    <a href="https://linkedin.com/in/sathish-sivakumar-99a462143" target="_blank" style="text-decoration: none;">
      <img alt="LinkedIn" src="https://img.shields.io/badge/💼_LinkedIn-Connect-0A66C2?style=for-the-badge" />
    </a>
    <a href="mailto:sathish.sivakumar2706@gmail.com" target="_blank" style="text-decoration: none;">
      <img alt="Email" src="https://img.shields.io/badge/📧_Email-Contact-D14836?style=for-the-badge" />
    </a>
  </div>

</div>

---

## 👨‍💻 About Me

<div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); padding: 20px 25px; border-radius: 12px; margin: 20px 0; text-align: left; box-shadow: 0 4px 15px rgba(102, 126, 234, 0.2);">

- 🏢 **Technical Lead** at Impiger Technologies Pvt. Ltd.
- 🚀 **8+ Years** architecting high-performance mobile ecosystems and enterprise platforms
- 📱 **Specialization**: Flutter, React JS, Native Android (Java & Kotlin)
- 🤖 **AI Enthusiast**: Leveraging GitHub Copilot, Claude, and Gemini for accelerated delivery
- 🌐 **Full-Stack Expert**: Mobile → Web → Backend → Cloud → AI
- ✨ **Passion**: Building practical, scalable, and impactful digital solutions

</div>

---

## 🛠️ Tech Stack & Architecture

<div align="center">

### 📱 Mobile & Web Development
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=Flutter&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)

### 🔧 Backend, Cloud & Databases
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-039BE5?style=for-the-badge&logo=firebase&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)

### 🚀 Tools & DevOps
![Git](https://img.shields.io/badge/Git-F05033?style=for-the-badge&logo=git&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-2C5263?style=for-the-badge&logo=jenkins&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)

</div>

---

## 🌟 Featured Professional Projects

| 🎯 Project | 💼 Domain | 📊 Impact & Tech |
|:---|:---|:---|
| **ABCD Aditya Birla Capital** | FinTech | 10M+ users • UPI, Investments, Digital Gold • Flutter-powered |
| **TATA AIA Siddhi** | Insurance | Agent platform • Real-time policies & earnings • SSO + Biometrics |
| **BizcomAI** | B2B Automation | Conversational AI • Enterprise data access via chat interface |
| **Go4WorldBusiness** | Global Trading | Marketplace for buyers & sellers • Flutter + Java + Firebase |
| **Foodwall** | Social Platform | Food discovery & reviews • Interactive UI • Firebase integration |

---

## 📂 My Open Source & Personal Projects

<div class="animated-section-bg">
  <div class="projects-grid-container">
    <h3 class="section-header" style="text-align: center; margin-bottom: 30px; color: #00D4FF;">🚀 Full-Stack Applications</h3>
    
    <div class="projects-grid">
      
      <div class="project-card">
        <div class="project-title">🏨 BookNowGo</div>
        <div class="project-description">Hotel Room Booking Platform</div>
        <div class="project-badges">
          <img src="https://img.shields.io/badge/Frontend-TypeScript-3178C6?style=flat-square" />
          <img src="https://img.shields.io/badge/Backend-Java-ED8B00?style=flat-square" />
        </div>
        <p style="font-size: 0.85em; color: #b1bcc9; margin: 10px 0;">Full-stack hotel booking application with modern architecture</p>
        <div class="project-links">
          <a href="https://github.com/sathishkhan27/BookNowGo-FrontEnd">Frontend</a>
          <a href="https://github.com/sathishkhan27/BookNowGo-BackEnd">Backend</a>
        </div>
      </div>

      <div class="project-card">
        <div class="project-title">🍽️ PingZo Ecosystem</div>
        <div class="project-description">Grocery & Food Delivery</div>
        <div class="project-badges">
          <img src="https://img.shields.io/badge/Mobile-Dart-00B4AB?style=flat-square" />
          <img src="https://img.shields.io/badge/Admin-TypeScript-3178C6?style=flat-square" />
        </div>
        <p style="font-size: 0.85em; color: #b1bcc9; margin: 10px 0;">End-to-end delivery ecosystem with real-time tracking</p>
        <div class="project-links">
          <a href="https://github.com/sathishkhan27/PingZo-Customer-Mobile-App">Customer</a>
          <a href="https://github.com/sathishkhan27/PingZO-Delivery-App">Delivery</a>
          <a href="https://github.com/sathishkhan27/Food-Grocery-Admin-Pannel">Admin</a>
        </div>
      </div>

      <div class="project-card">
        <div class="project-title">📱 AI-Powered Solutions</div>
        <div class="project-description">Intelligent Applications</div>
        <div class="project-badges">
          <img src="https://img.shields.io/badge/Framework-Dart%20Flutter-00B4AB?style=flat-square" />
          <img src="https://img.shields.io/badge/AI-Integrated-FF6F61?style=flat-square" />
        </div>
        <p style="font-size: 0.85em; color: #b1bcc9; margin: 10px 0;">AI-enhanced calendar & smart scheduling management</p>
        <div class="project-links">
          <a href="https://github.com/sathishkhan27/AI-Calendar">AI Calendar</a>
        </div>
      </div>

      <div class="project-card">
        <div class="project-title">💼 Desktop & Billing</div>
        <div class="project-description">Enterprise Solutions</div>
        <div class="project-badges">
          <img src="https://img.shields.io/badge/Tech-Flutter-00B4AB?style=flat-square" />
          <img src="https://img.shields.io/badge/Focus-ERP-00D4FF?style=flat-square" />
        </div>
        <p style="font-size: 0.85em; color: #b1bcc9; margin: 10px 0;">Comprehensive billing, invoicing & inventory management</p>
        <div class="project-links">
          <a href="https://github.com/sathishkhan27/Billing-Software-Desktop-Application">Billing App</a>
        </div>
      </div>

      <div class="project-card">
        <div class="project-title">🌐 Portfolio Builder</div>
        <div class="project-description">Dynamic Portfolio Platform</div>
        <div class="project-badges">
          <img src="https://img.shields.io/badge/Tech-TypeScript-3178C6?style=flat-square" />
          <img src="https://img.shields.io/badge/CMS-Dynamic-00D4FF?style=flat-square" />
        </div>
        <p style="font-size: 0.85em; color: #b1bcc9; margin: 10px 0;">Dynamic portfolio websites with real-time rendering</p>
        <div class="project-links">
          <a href="https://github.com/sathishkhan27/Portfolio-Website-Builder">View Project</a>
        </div>
      </div>

      <div class="project-card">
        <div class="project-title">🤖 Genisus AI OS</div>
        <div class="project-description">Personal AI Operating System</div>
        <div class="project-badges">
          <img src="https://img.shields.io/badge/Tech-JavaScript-F7DF1E?style=flat-square" />
          <img src="https://img.shields.io/badge/AI-Powered-FF6F61?style=flat-square" />
        </div>
        <p style="font-size: 0.85em; color: #b1bcc9; margin: 10px 0;">Command center for AI-driven productivity & automation</p>
        <div class="project-links">
          <a href="https://github.com/sathishkhan27/Genisus-Personal-AI-Operating-System">Explore</a>
        </div>
      </div>

    </div>
  </div>
</div>

### 📱 Mobile Applications

- **PingZo Customer Mobile App** - Dart/Flutter, User-friendly grocery & food ordering
- **PingZo Delivery App** - Dart/Flutter, Real-time delivery tracking & management
- **Shreeja Ulagam Mobile App** - Dart/Flutter, Domain-specific mobile solution

### 🌐 Web & Other Projects

- **gstechnology** - HTML-based showcase
- **Portfolio Website** - Personal portfolio and professional presence

---

## 📊 GitHub Analytics & Activity

<div align="center" style="margin: 30px 0;">

  <img src="https://github-readme-stats.vercel.app/api?username=sathishkhan27&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D4FF&icon_color=FF6F61&text_color=ffffff" alt="GitHub Stats" width="100%" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=sathishkhan27&theme=tokyonight&hide_border=true&background=0D1117&stroke=00D4FF&ring=FF6F61&fire=FF6F61" alt="GitHub Streak" width="100%" />

  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=sathishkhan27&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D4FF&text_color=ffffff" alt="Top Languages" width="100%" />

</div>

---

## 💡 Professional Highlights

<div style="background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%); padding: 25px 30px; border-radius: 12px; margin: 20px 0; text-align: left; box-shadow: 0 4px 15px rgba(30, 60, 114, 0.2);">

- ✅ **Architected & Delivered** large-scale mobile and enterprise applications serving millions
- ✅ **Platform Scale**: Built systems across FinTech, Insurance, B2B, Trading, and Social domains
- ✅ **End-to-End Solutions**: Mobile → Web → Backend → Cloud → AI integration
- ✅ **Team Leadership**: Technical lead guiding cross-functional teams for high-impact delivery
- ✅ **Performance First**: Scalable architecture, clean code, and product excellence
- ✅ **Innovation Driven**: Leveraging AI tools for accelerated development and delivery

</div>

---

## 🎯 Open to Opportunities

<div style="background: linear-gradient(135deg, #00D4FF 0%, #FF6F61 100%); padding: 30px; border-radius: 12px; margin: 25px 0; box-shadow: 0 4px 20px rgba(0, 212, 255, 0.2);">

<div style="text-align: center; color: #0D1117;">

### I'm actively seeking roles in:

🚀 **Senior Engineering** | Technical Leadership

🏗️ **Architecture & Design** | Platform Development

📱 **Mobile Ecosystem** | Full-Stack Engineering

🤖 **AI Integration** | Innovative Solutions

💼 **Enterprise Products** | Startup Ventures

<p style="margin-top: 20px; font-size: 18px; font-weight: bold;">
  ✨ Let's build something amazing together! 🌟
</p>

</div>

</div>

---

## 📫 Let's Connect

<div align="center" style="margin: 30px 0;">

  <a href="https://linkedin.com/in/sathish-sivakumar-99a462143" target="_blank" style="text-decoration: none; margin: 0 8px;">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:sathish.sivakumar2706@gmail.com" target="_blank" style="text-decoration: none; margin: 0 8px;">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail" />
  </a>
  <a href="https://sathish-portfolio-website.onrender.com/" target="_blank" style="text-decoration: none; margin: 0 8px;">
    <img src="https://img.shields.io/badge/Portfolio-00D4FF?style=for-the-badge&logo=globe&logoColor=white" alt="Portfolio" />
  </a>
  <a href="https://github.com/sathishkhan27" target="_blank" style="text-decoration: none; margin: 0 8px;">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>

</div>

---

<div align="center" style="margin: 40px 0;">
  
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=16&duration=4000&pause=1000&color=00D4FF&center=true&vCenter=true&width=500&lines=Building+the+future+with+code+and+innovation" alt="Footer" />

  <p style="margin-top: 20px;">
    <img src="https://img.shields.io/badge/Last%20Updated-Oct%202026-00D4FF?style=flat-square" />
    <img src="https://img.shields.io/github/followers/sathishkhan27?style=flat-square&label=Followers&logo=github" />
    <img src="https://img.shields.io/github/stars/sathishkhan27?style=flat-square&label=Stars&logo=github" />
  </p>

</div>
