<template>
  <h2 class="heading">Certifications</h2>

  <div class="experience-section">
    <div class="experience" @click="downloadFile('axis.pdf')">
      <div class="image-container">
        <img src="../assets/infineon.png" alt="infineon-technologies" />
      </div>
      <div>
        <h2>Javascript with HTML</h2>
        <h3>SRM Axis Intellects</h3>
        <div class="location">
          <p>04/2022</p>
        </div>
        <div>
          During my participation in the “JavaScript with HTML” program by SRM Axis Intellects, I
          gained a strong foundation in how JavaScript interacts with HTML to build dynamic and
          interactive web pages. I learned key JavaScript concepts such as variables, functions,
          events, loops, and DOM manipulation, and understood how these work together with HTML
          structure to create responsive user experiences. This training helped me strengthen my
          problem-solving skills and boosted my confidence in front-end development.
        </div>
      </div>
    </div>

    <div class="experience" @click="downloadFile('level 1.pdf')">
      <div class="image-container">
        <img src="../assets/infineon.png" alt="infineon-technologies" />
      </div>
      <div>
        <h2>Cybersecurity Learner Level-1</h2>
        <h3>Mosse Cyber Security Institute</h3>
        <div class="location">
          <p>10/2024</p>
        </div>
        <div>
          Through the Level 1 Cybersecurity Learner program at Mossé Cyber Security Institute, I
          gained a solid introduction to the fundamentals of cybersecurity. I learned about core
          security concepts such as threats, vulnerabilities, and attack surfaces, and developed an
          understanding of how cyberattacks occur and how they can be prevented. The program also
          helped me build essential skills in safe online practices, basic security analysis, and
          recognizing common security risks. This milestone strengthened my foundation for
          progressing further in the cybersecurity domain.
        </div>
      </div>
    </div>

    <div class="experience" @click="downloadFile('level 2.pdf')">
      <div class="image-container">
        <img src="../assets/infineon.png" alt="infineon-technologies" />
      </div>
      <div>
        <h2>Cybersecurity Learner Level-2</h2>
        <h3>Mosse Cyber Security Institute</h3>
        <div class="location">
          <p>12/2024</p>
        </div>
        <div>
          In the Cybersecurity Learner Level 2 program at Mossé Cyber Security Institute, I deepened
          my understanding of cybersecurity principles and built hands-on skills through more
          advanced practical exercises. I learned how to identify and analyze real-world security
          threats, understand attacker techniques, and apply defensive strategies to mitigate risks.
          This level strengthened my abilities in basic security operations, vulnerability
          awareness, and safe system practices, helping me progress toward more technical
          cybersecurity challenges.
        </div>
      </div>
    </div>

    <div class="experience" @click="downloadFile('COMPTIA SCORE REPORT__.pdf')">
      <div class="image-container">
        <img src="../assets/infineon.png" alt="infineon-technologies" />
      </div>
      <div>
        <h2>CompTIA Security+</h2>
        <h3>CompTIA</h3>
        <div class="location">
          <p>06/2025</p>
        </div>
        <div>
          By achieving the CompTIA Security+ certification, I developed a strong understanding of
          essential cybersecurity principles and hands-on security practices. I learned how
          different security controls work, the fundamentals of risk management, and how to identify
          various threat actors, vulnerabilities, and indicators of malicious activity. I gained
          skills in securing enterprise infrastructure, applying security techniques to systems,
          managing identities and access, and understanding vulnerability management processes. This
          certification strengthened my ability to evaluate risks, respond to security incidents,
          and support secure operations in real-world environments.
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
async function downloadFile(fileName) {
  try {
    const response = await fetch(`/${fileName}`, { method: 'GET' });

    if (!response.ok) {
      throw new Error(`HTTP error ${response.status}`);
    }

    const blob = await response.blob();

    if (!blob || blob.size === 0) {
      throw new Error('Downloaded file is empty');
    }

    const url = URL.createObjectURL(blob);
    const link = document.createElement('a');
    link.href = url;
    link.download = fileName;

    document.body.appendChild(link);
    link.click();
    link.remove();

    setTimeout(() => URL.revokeObjectURL(url), 1000);
  } catch (error) {
    console.error('Download failed:', error);
    alert(`Unable to download ${fileName}. Make sure it exists in /public.`);
  }
}
</script>

<style scoped>
.heading {
  text-align: center;
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #1b3c53;
  font-weight: bold;
}

.experience {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.experience:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 28px rgba(0, 0, 0, 0.12);
  cursor: pointer;
}

.heading {
  text-align: center;
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #1b3c53;
  font-weight: bold;
}

.experience-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
}

.experience {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: flex-start;
  background-color: #fbfaf9;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
  width: 100%;
  max-width: 1000px;
  gap: 2rem;
}

.image-container img {
  width: 100px;
  height: auto;
  object-fit: contain;
}

.experience h2 {
  margin: 0;
  font-size: 1.25rem;
  color: #1b3c53;
}

.experience h3 {
  margin: 0.25rem 0 0 0;
  font-size: 1rem;
  font-weight: normal;
  color: #555;
}

.location {
  display: flex;
  gap: 2rem;
  font-size: 0.9rem;
  color: #777;
  /* margin-bottom: 1rem; */
}

.experience div:last-child {
  font-size: 0.95rem;
  text-align: justify;
  color: #333;
  line-height: 1.5;
}
</style>
