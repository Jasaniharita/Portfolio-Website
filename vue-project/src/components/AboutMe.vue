<template>
    <section>
      <h1 class="heading">About Me</h1>
      <div class="profile-container">
        <div class="text-container">
          <p class="profile-text">
            I am an MEng student at the University of Maryland, College Park, currently pursuing my Master’s in Cybersecurity. I completed my Bachelor’s in Computer Science at SRM Institute of Science and Technology, where I built a strong foundation in network security, vulnerability assessment, and cyber defense.

Over time, I’ve developed a keen interest in Governance, Risk, and Compliance (GRC) and am actively working on projects to strengthen both my technical skills and risk management capabilities. I enjoy solving complex security challenges and bring strong analytical and problem-solving abilities to every task. Through my graduate studies, I aim to deepen my expertise in cybersecurity governance and threat mitigation, ultimately contributing to secure and resilient enterprise environments.
          </p>
          <div class="profile-icons">
            <img src="../assets/github.png" class="profile-icon" alt="GitHub" onclick="window.open(`https://github.com/Jasaniharita`, '_blank')">
            <img src="../assets/linkedin.png" class="profile-icon" alt="LinkedIn" onclick="window.open(`https://www.linkedin.com/in/harita-jasani-8b8b17218/`, '_blank')">
            <!-- <button @click="download" >Resume</button> -->
             <!-- <a :href="pdfFile" download="Resume__Harita.pdf">
              <button>Resume</button>
             </a> -->
             <button @click="downloadPDF" class="resume-button">Resume</button>
          </div>
        </div>
        <div class="image-container">
          <img src="../assets/harita.jpeg" alt="Profile Picture" class="profile-image" />
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
  </script>
  
  <style scoped>
  .heading {
    text-align: center;
    font-size: 2rem;
    margin-bottom: 1rem;
    color: #1B3C53;
  }

  section{
    margin-top: 3em;
    margin-bottom: 3em;
  }
  
  .profile-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    gap: 4rem;
    padding: 1rem;
  }

  .profile-text{
    text-align: justify;
  }
  
  .text-container {
    flex: 1 1 400px;
    max-width: 600px;
  }
  
  .text-container p {
    line-height: 1.6;
    font-size: 1rem;
    color: #1B3C53;
  }
  
  .profile-icons {
    margin-top: 1rem;
    display: flex;
    gap: 2rem;
  }
  
  .profile-icon {
    height: 40px;
    width: 40px;
    transition: transform 0.3s;
    cursor: pointer;
  }
  
  .profile-icon:hover {
    transform: scale(1.1);
  }
  
  .image-container {
    width: 300px;
    height: 300px;
    border-radius: 50%;
    overflow: hidden;
    border: 3px solid #1B3C53; /* Tailwind's blue-500 */
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .profile-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center top;
  }

  .news-container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .news-item{
    margin-bottom: 1.5em;
    font-size: 18px;
    color: #1B3C53;
  }

  .tech-skills-section {
    background-color: #fbfaf9;
    padding: 3rem 2rem;
    border-radius: 12px;
    margin: 2rem auto;
    max-width: 1200px;
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
  }

  .tech-skills-section .heading {
    color: #1B3C53;
    margin-bottom: 2rem;
  }

  .skills-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 3rem;
    max-width: 1000px;
    margin: 0 auto;
  }

  .skills-column {
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }

  .skill-category {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .category-title {
    color: #1B3C53;
    font-size: 1.2rem;
    font-weight: 600;
    margin: 0;
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  .skills-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
  }

  .skill-tag {
    background-color: #f5f5f5;
    color: #1B3C53;
    padding: 0.5rem 1rem;
    border-radius: 6px;
    font-size: 0.9rem;
    font-weight: 400;
    white-space: nowrap;
    border: 1px solid #e0e0e0;
    transition: all 0.3s ease;
  }

  .skill-tag:hover {
    background-color: #e8e8e8;
    border-color: #1B3C53;
    transform: translateY(-2px);
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  }

  @media (max-width: 768px) {
    .skills-container {
      grid-template-columns: 1fr;
      gap: 2rem;
    }

    .tech-skills-section {
      padding: 2rem 1rem;
    }
  }

  .resume-button {
  font-size: 1rem;
  color: #1B3C53;
  background-color: #D2C1B6;
  border-radius: 8px;
  display: flex;  
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 10px;
  padding: 5px;
  font-family: 'Times New Roman', Times, serif;
  width: 100px;
  border: none;
}
.resume-button:hover {
  background-color: #456882;
  color: #fbfaf9;
  cursor: pointer;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}
  </style>
  