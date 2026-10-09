<!-- ANIMATED BACKGROUND -->
<style>
  @keyframes gradient-shift {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }

  @keyframes float-in {
    from { opacity: 0; transform: translateY(18px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes pulse-glow {
    0%, 100% { box-shadow: 0 0 18px rgba(0, 212, 255, 0.22); }
    50% { box-shadow: 0 0 28px rgba(255, 111, 97, 0.42); }
  }

  @keyframes shimmer {
    from { transform: translateX(-120%); }
    to { transform: translateX(120%); }
  }

  .hero-shell {
    position: relative;
    overflow: hidden;
    border-radius: 26px;
    padding: 28px 18px 20px;
    margin: 18px 0 26px;
    background: linear-gradient(135deg, rgba(15, 23, 42, 0.95), rgba(16, 30, 54, 0.9));
    border: 1px solid rgba(0, 212, 255, 0.25);
    box-shadow: 0 18px 40px rgba(0, 0, 0, 0.28);
    background-size: 200% 200%;
    animation: gradient-shift 12s ease infinite;
  }

  .hero-shell::before {
    content: "";
    position: absolute;
    inset: 0;
    background: radial-gradient(circle at 20% 20%, rgba(0, 212, 255, 0.18), transparent 30%),
                radial-gradient(circle at 80% 30%, rgba(255, 111, 97, 0.18), transparent 30%),
                radial-gradient(circle at 50% 80%, rgba(118, 75, 162, 0.18), transparent 35%);
    animation: gradient-shift 15s ease infinite;
    pointer-events: none;
  }

  .profile-header {
    position: relative;
    z-index: 1;
    animation: float-in 1s ease-out;
  }

  .hero-shell img {
    max-width: 100%;
    height: auto;
    display: block;
    margin: 0 auto;
  }

  .quick-links {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 12px;
    margin: 18px 0 10px;
    position: relative;
    z-index: 1;
  }

  .quick-links a {
    text-decoration: none;
    transition: transform 0.2s ease;
  }

  .quick-links a:hover {
    transform: translateY(-2px);
  }

  .stats-row {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 8px;
    position: relative;
    z-index: 1;
  }

  .badge-glow {
    animation: pulse-glow 2.8s ease-in-out infinite;
  }

  .project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
    margin: 24px 0 10px;
  }

  .project-card {
    position: relative;
    overflow: hidden;
    padding: 22px 20px;
    border-radius: 18px;
    border: 1px solid rgba(255, 255, 255, 0.08);
    background: rgba(17, 24, 39, 0.86);
    box-shadow: 0 12px 28px rgba(0, 0, 0, 0.18);
    transition: transform 0.25s ease, box-shadow 0.25s ease, border-color 0.25s ease;
  }

  .project-card::before {
    content: "";
    position: absolute;
    inset: 0 auto 0 -100%;
    width: 60%;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.12), transparent);
    transform: skewX(-22deg);
    animation: shimmer 2.8s ease-in-out infinite;
  }

  .project-card:hover {
    transform: translateY(-6px);
    box-shadow: 0 18px 34px rgba(0, 212, 255, 0.12);
    border-color: rgba(0, 212, 255, 0.35);
  }

  .project-card h4 {
    margin: 0 0 8px;
    font-size: 1.12rem;
    color: #ffffff;
  }

  .project-card p {
    margin: 8px 0;
    font-size: 0.92rem;
    color: #d0d8e4;
  }

  .project-card .meta {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin: 12px 0;
  }

  .project-card .links {
    margin-top: 12px;
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .project-card a {
    color: #7dd3fc;
    text-decoration: none;
    border: 1px solid rgba(125, 211, 252, 0.35);
    border-radius: 999px;
    padding: 6px 10px;
    font-size: 0.8rem;
    background: rgba(125, 211, 252, 0.04);
  }

  .project-card a:hover {
    background: rgba(125, 211, 252, 0.10);
  }

  .projects-section {
    background: linear-gradient(135deg, rgba(11, 18, 32, 0.75), rgba(20, 33, 54, 0.7));
    border: 1px solid rgba(0, 212, 255, 0.14);
    border-radius: 20px;
    padding: 18px 18px 6px;
    margin: 4px 0 16px;
  }

  .projects-title {
    margin: 0 0 10px;
    color: #7dd3fc;
    text-align: center;
  }

  @media (max-width: 600px) {
    .hero-shell {
      padding: 20px 8px 12px;
    }
    .project-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<div align="center">
  <div class="hero-shell">
    <div class="profile-header">
      <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=28&duration=4000&pause=1000&color=00D4FF&center=true&vCenter=true&width=900&lines=Hi+👋+I'm+Sathish+Sivakumar;Technical+Leader+%26+Full-Stack+Architect" alt="Typing Animation" />

      <div class="stats-row">
        <img class="badge-glow" src="https://img.shields.io/badge/Focus-Mobile%20%26%20Web%20Architecture-00D4FF?style=flat-square&logo=target" />
        <img class="badge-glow" src="https://img.shields.io/badge/Experience-8%2B%20Years-FF6F61?style=flat-square&logo=calendar" />
        <img class="badge-glow" src="https://img.shields.io/badge/Based%20In-India-%F74C1C?style=flat-square&logo=mapbox" />
      </div>

      <div class="quick-links">
        <a href="https://sathish-portfolio-website.onrender.com/" target="_blank"><img alt="Portfolio" src="https://img.shields.io/badge/🌐_Portfolio-Visit-00D4FF?style=for-the-badge&logoColor=white" /></a>
        <a href="https://linkedin.com/in/sathish-sivakumar-99a462143" target="_blank"><img alt="LinkedIn" src="https://img.shields.io/badge/💼_LinkedIn-Connect-0A66C2?style=for-the-badge" /></a>
        <a href="mailto:sathish.sivakumar2706@gmail.com" target="_blank"><img alt="Email" src="https://img.shields.io/badge/📧_Email-Contact-D14836?style=for-the-badge" /></a>
      </div>
    </div>
  </div>
</div>

---

## 👨‍💻 About Me

- 🏢 **Technical Lead** at Impiger Technologies Pvt. Ltd.
- 🚀 **8+ Years** architecting high-performance mobile ecosystems and enterprise platforms
- 📱 **Specialization**: Flutter, React JS, Native Android (Java & Kotlin)
- 🤖 **AI Enthusiast**: Leveraging GitHub Copilot, Claude, and Gemini for accelerated delivery
- 🌐 **Full-Stack Expert**: Mobile → Web → Backend → Cloud → AI
- ✨ **Passion**: Building practical, scalable, and impactful digital solutions

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

<div class="projects-section">
  <h3 class="projects-title">🚀 Full-Stack Applications</h3>

  <div class="project-grid">
    <div class="project-card">
      <h4>🏨 BookNowGo</h4>
      <p>Hotel room booking platform with scalable backend and modern UX.</p>
      <div class="meta">
        <img src="https://img.shields.io/badge/Frontend-TypeScript-3178C6?style=flat-square" />
        <img src="https://img.shields.io/badge/Backend-Java-ED8B00?style=flat-square" />
      </div>
      <div class="links">
        <a href="https://github.com/sathishkhan27/BookNowGo-FrontEnd">Frontend</a>
        <a href="https://github.com/sathishkhan27/BookNowGo-BackEnd">Backend</a>
      </div>
    </div>

    <div class="project-card">
      <h4>🍽️ PingZo Ecosystem</h4>
      <p>End-to-end grocery and food delivery platform across customer, delivery, and admin flows.</p>
      <div class="meta">
        <img src="https://img.shields.io/badge/Mobile-Dart-00B4AB?style=flat-square" />
        <img src="https://img.shields.io/badge/Admin-TypeScript-3178C6?style=flat-square" />
      </div>
      <div class="links">
        <a href="https://github.com/sathishkhan27/PingZo-Customer-Mobile-App">Customer</a>
        <a href="https://github.com/sathishkhan27/PingZO-Delivery-App">Delivery</a>
        <a href="https://github.com/sathishkhan27/Food-Grocery-Admin-Pannel">Admin</a>
      </div>
    </div>

    <div class="project-card">
      <h4>📱 AI Calendar</h4>
      <p>AI-enhanced scheduling and productivity system with intelligent workflow automation.</p>
      <div class="meta">
        <img src="https://img.shields.io/badge/Framework-Dart-00B4AB?style=flat-square" />
        <img src="https://img.shields.io/badge/AI-Integrated-FF6F61?style=flat-square" />
      </div>
      <div class="links">
        <a href="https://github.com/sathishkhan27/AI-Calendar">Repository</a>
      </div>
    </div>

    <div class="project-card">
      <h4>💼 Billing Software</h4>
      <p>Desktop ERP-like billing and inventory platform for enterprise operations.</p>
      <div class="meta">
        <img src="https://img.shields.io/badge/Tech-Flutter-00B4AB?style=flat-square" />
        <img src="https://img.shields.io/badge/System-ERP-00D4FF?style=flat-square" />
      </div>
      <div class="links">
        <a href="https://github.com/sathishkhan27/Billing-Software-Desktop-Application">Repository</a>
      </div>
    </div>

    <div class="project-card">
      <h4>🌐 Portfolio Builder</h4>
      <p>Dynamic portfolio platform with configurable templates and real-time content rendering.</p>
      <div class="meta">
        <img src="https://img.shields.io/badge/Tech-TypeScript-3178C6?style=flat-square" />
        <img src="https://img.shields.io/badge/CMS-Dynamic-00D4FF?style=flat-square" />
      </div>
      <div class="links">
        <a href="https://github.com/sathishkhan27/Portfolio-Website-Builder">Repository</a>
      </div>
    </div>

    <div class="project-card">
      <h4>🤖 Genisus AI OS</h4>
      <p>Personal AI operating system for focused workflows, automation, and decision support.</p>
      <div class="meta">
        <img src="https://img.shields.io/badge/Tech-JavaScript-F7DF1E?style=flat-square" />
        <img src="https://img.shields.io/badge/AI-Powered-FF6F61?style=flat-square" />
      </div>
      <div class="links">
        <a href="https://github.com/sathishkhan27/Genisus-Personal-AI-Operating-System">Repository</a>
      </div>
    </div>
  </div>
</div>

---

<details open>
<summary><h3>📱 Mobile Applications</h3></summary>

- **PingZo Customer Mobile App** - Dart/Flutter, user-friendly grocery & food ordering with real-time tracking
- **PingZo Delivery App** - Dart/Flutter, live delivery tracking, route optimization & earnings management
- **Shreeja Ulagam Mobile App** - Dart/Flutter, domain-specific mobile solution with rich features

</details>

---

<details open>
<summary><h3>🌐 Web & Other Projects</h3></summary>

- **gstechnology** - HTML-based portfolio showcase
- **Portfolio Website** - Personal portfolio and professional presence

</details>

---

## 📊 GitHub Analytics & Activity

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=sathishkhan27&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D4FF&icon_color=FF6F61&text_color=ffffff" alt="GitHub Stats" />

<img src="https://github-readme-streak-stats.herokuapp.com/?user=sathishkhan27&theme=tokyonight&hide_border=true&background=0D1117&stroke=00D4FF&ring=FF6F61&fire=FF6F61" alt="GitHub Streak" />

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=sathishkhan27&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D4FF&text_color=ffffff" alt="Top Languages" />

</div>

---

## 💡 Professional Highlights

- ✅ **Architected & Delivered** large-scale mobile and enterprise applications serving millions
- ✅ **Platform Scale**: Built systems across FinTech, Insurance, B2B, Trading, and Social domains
- ✅ **End-to-End Solutions**: Mobile → Web → Backend → Cloud → AI integration
- ✅ **Team Leadership**: Technical lead guiding cross-functional teams for high-impact delivery
- ✅ **Performance First**: Scalable architecture, clean code, and product excellence
- ✅ **Innovation Driven**: Leveraging AI tools for accelerated development and delivery

---

## 🎯 Open to Opportunities

I'm actively seeking roles in:

🚀 **Senior Engineering** | Technical Leadership

🏗️ **Architecture & Design** | Platform Development

📱 **Mobile Ecosystem** | Full-Stack Engineering

🤖 **AI Integration** | Innovative Solutions

💼 **Enterprise Products** | Startup Ventures

---

## 📫 Let's Connect

<div align="center">

[LinkedIn](https://linkedin.com/in/sathish-sivakumar-99a462143) • [Email](mailto:sathish.sivakumar2706@gmail.com) • [Portfolio](https://sathish-portfolio-website.onrender.com/) • [GitHub](https://github.com/sathishkhan27)

</div>

---

<div align="center">

**Building the future with code and innovation** ✨

<img src="https://img.shields.io/badge/Last%20Updated-Oct%202026-00D4FF?style=flat-square" />
<img src="https://img.shields.io/github/followers/sathishkhan27?style=flat-square&label=Followers&logo=github" />
<img src="https://img.shields.io/github/stars/sathishkhan27?style=flat-square&label=Stars&logo=github" />

</div>
