<template>
  <section>
    <h1 class="heading">About Me</h1>
    <div class="profile-container">
      <div class="text-container">
        <p class="profile-text">
          I am a student at the University of Maryland, College Park, currently pursuing my Master's in Cybersecurity. I completed my Bachelor’s in Computer Science at SRM Institute of Science and Technology, where I built a strong foundation in network security, vulnerability assessment, and cyber defense.

Over time, I’ve developed a keen interest in Governance, Risk, and Compliance (GRC) and am actively working on projects to strengthen both my technical skills and risk management capabilities. I enjoy solving complex security challenges and bring strong analytical and problem-solving abilities to every task. Through my graduate studies, I aim to deepen my expertise in cybersecurity governance and threat mitigation, ultimately contributing to secure and resilient enterprise environments.
        </p>
        <div class="profile-icons">
          <img src="../assets/github.png" class="profile-icon" alt="GitHub" role="button" tabindex="0" @click="openLink('https://github.com/Jasaniharita')">
          <img src="../assets/linkedin.png" class="profile-icon" alt="LinkedIn" role="button" tabindex="0" @click="openLink('https://www.linkedin.com/in/harita-jasani-8b8b17218/')">
          <button @click="downloadPDF" class="resume-button" aria-label="Download resume">Resume</button>
        </div>
      </div>
      <div class="image-container" aria-hidden="false">
        <img src="../assets/harita.jpeg" alt="Profile Picture of Harita Jasani" class="profile-image" />
      </div>
    </div>
  </section>

  <section>
    <h1 class="heading">News</h1>
    <div class="news-container">
      <ul>
        <li class="news-item"><b>09-2025</b>:  Started Master's in Cybersecurity at University of Maryland - College Park.</li>
        <li class="news-item"><b>05-2025</b>:  Completed Bachelor's in Computer Science with Specialization in Cybersecurity at SRM Institute of Technology</li>
      </ul>
    </div>
  </section>

  <section class="tech-skills-section">
      <h1 class="heading">Tech Skills</h1>
      <div class="skills-container">
          <div class="skills-column">
              <div class="skill-category">
                  <h3 class="category-title">Cybersecurity Tools:</h3>
                  <div class="skills-grid">
                      <span class="skill-tag">Wireshark</span>
                      <span class="skill-tag">Metasploit</span>
                      <span class="skill-tag">Kali Linux</span>
                      <span class="skill-tag">Burp Suite</span>
                      <span class="skill-tag">Snort</span>
                      <span class="skill-tag">Nmap</span>
                      <span class="skill-tag">Nessus</span>
                      <span class="skill-tag">OpenVAS</span>
                  </div>
              </div>

              <div class="skill-category">
                  <h3 class="category-title">Networking Protocols</h3>
                  <div class="skills-grid">
                      <span class="skill-tag">TCP/IP</span>
                      <span class="skill-tag">DNS</span>
                      <span class="skill-tag">HTTP</span>
                      <span class="skill-tag">SSL/TLS</span>
                  </div>
              </div>

              <div class="skill-category">
                  <h3 class="category-title">Operating Systems</h3>
                  <div class="skills-grid">
                      <span class="skill-tag">Linux (Ubuntu, Kali)</span>
                  </div>
              </div>
          </div>

          <div class="skills-column">
              <div class="skill-category">
                  <h3 class="category-title">Security Concepts</h3>
                  <div class="skills-grid">
                      <span class="skill-tag">Ethical Hacking</span>
                      <span class="skill-tag">Vulnerability Assessment</span>
                      <span class="skill-tag">Incident Response</span>
                      <span class="skill-tag">Threat Hunting</span>
                      <span class="skill-tag">Digital Forensics</span>
                      <span class="skill-tag">Malware Analysis</span>
                      <span class="skill-tag">Risk Management</span>
                  </div>
              </div>

              <div class="skill-category">
                  <h3 class="category-title">Protocols & Standards</h3>
                  <div class="skills-grid">
                      <span class="skill-tag">MITRE ATT&CK</span>
                      <span class="skill-tag">ISO 27001</span>
                      <span class="skill-tag">Zero Trust</span>
                      <span class="skill-tag">NIST Framework</span>
                  </div>
              </div>
          </div>
      </div>
  </section>
</template>

<script setup>
function downloadPDF() {
  const link = document.createElement("a");
  link.href = "/Resume__Harita.pdf"; // from public folder
  link.download = "Resume__Harita.pdf";
  link.click();
}
function openLink(url){
  window.open(url, '_blank');
}
</script>

<style scoped>
:root{
  /* tweak these to change the theme quickly */
  --primary: #1B3C53;
  --muted: #f5f5f5;
  --card-bg: #fbfaf9;
  --accent: #D2C1B6;
}

/* fluid heading / base sizes */
.heading {
  text-align: center;
  font-size: clamp(1.4rem, 2.2vw + 1rem, 2rem);
  margin-bottom: 1rem;
  color: var(--primary);
}

/* spacing for sections */
section{
  margin-top: 2.5rem;
  margin-bottom: 2.5rem;
  padding: 0 1rem;
}

/* PROFILE layout */
.profile-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 2.5rem;
  padding: 0.5rem;
}

/* left column (text) */
.text-container {
  flex: 1 1 380px;
  max-width: 680px;
}

/* readable paragraph */
.profile-text{
  text-align: justify;
  line-height: 1.6;
  font-size: clamp(0.95rem, 1.2vw + 0.6rem, 1rem);
  color: var(--primary);
  margin: 0;
}

/* icons + resume */
.profile-icons {
  margin-top: 1rem;
  display: flex;
  gap: 1rem;
  align-items: center;
  flex-wrap:wrap;
}

/* touch targets bigger on mobile */
.profile-icon {
  height: 44px;
  width: 44px;
  transition: transform 0.18s;
  cursor: pointer;
  border-radius: 8px;
  padding: 6px;
  background: transparent;
}
.profile-icon:hover,
.profile-icon:focus {
  transform: scale(1.08);
  outline: none;
}

/* avatar - responsive circular container */
.image-container {
  width: 300px;
  height: 300px;
  border-radius: 50%;
  overflow: hidden;
  border: 3px solid var(--primary);
  display: flex;
  justify-content: center;
  align-items: center;
  flex: 0 0 auto;
}

/* make image scale nicely */
.profile-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center top;
  display:block;
}

/* NEWS */
.news-container{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.news-item{
  margin-bottom: 1rem;
  font-size: clamp(0.95rem, 1vw + 0.6rem, 1.05rem);
  color: var(--primary);
}

/* TECH SKILLS card */
.tech-skills-section {
  background-color: var(--card-bg);
  padding: 2.25rem 1.25rem;
  border-radius: 12px;
  margin: 1.5rem auto;
  max-width: 1100px;
  box-shadow: 0 6px 18px rgba(0,0,0,0.06);
}

/* grid for two-column layout on desktop */
.skills-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2.25rem;
  max-width: 1000px;
  margin: 0 auto;
}

.skills-column {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.skill-category {
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}

.category-title {
  color: var(--primary);
  font-size: 1.05rem;
  font-weight: 600;
  margin: 0;
  text-transform: uppercase;
  letter-spacing: 1px;
}

/* skills grid: allow content to wrap and be responsive */
.skills-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 0.6rem;
}

/* tags smaller and wrap better on mobile */
.skill-tag {
  background-color: var(--muted);
  color: var(--primary);
  padding: 0.45rem 0.8rem;
  border-radius: 6px;
  font-size: clamp(0.78rem, 0.6vw + 0.6rem, 0.95rem);
  font-weight: 400;
  white-space: nowrap;
  border: 1px solid #e0e0e0;
  transition: all 0.22s ease;
}
.skill-tag:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.08);
}

/* Resume button */
.resume-button {
  font-size: 1rem;
  color: var(--primary);
  background-color: var(--accent);
  border-radius: 8px;
  padding: 6px 12px;
  border: none;
  cursor: pointer;
  min-width: 96px;
}
.resume-button:hover,
.resume-button:focus {
  background-color: #456882;
  color: #fbfaf9;
  box-shadow: 0 6px 12px rgba(0,0,0,0.12);
  outline: none;
}

/* --- Responsive adjustments --- */
@media (max-width: 900px) {
  .image-container { width: 240px; height: 240px; }
  .profile-container { gap: 1.5rem; }
  .skills-container { gap: 1.5rem; }
}

@media (max-width: 700px) {
  /* stack profile text and image */
  .profile-container {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  .text-container { max-width: 95%; }
  .profile-text { text-align: left; } /* left aligned text reads better on narrow screens */
  .image-container { width: 180px; height: 180px; }
  .profile-icons { justify-content: center; }

  /* skills become single column */
  .skills-container {
    grid-template-columns: 1fr;
    gap: 1rem;
  }

  /* make skill tags wrap by allowing them to break */
  .skill-tag { white-space: normal; text-align:center; padding: 0.4rem 0.6rem; }

  /* reduce paddings */
  .tech-skills-section { padding: 1.5rem 1rem; }
  section { margin-top: 1.75rem; margin-bottom: 1.75rem; }
}

@media (max-width: 420px) {
  .image-container { width: 140px; height: 140px; border-width: 2px; }
  .profile-icon { height: 40px; width: 40px; padding:4px; }
  .heading { font-size: 1.4rem; }
  .profile-text { font-size: 0.95rem; }
}
</style>
