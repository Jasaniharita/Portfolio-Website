<template>
  <h2 class="heading">Projects</h2>

  <div class="projects">
    <ul class="projects-list">
      <li>
        <div class="project">
          <div class="image-container">
            <img src="../assets/ahs.png" class="project-image" alt="Project-Image" />
          
          </div>

          <div class="project-description-container">
            <h2>Generative AI Malware Classification, Detection, and Monitoring</h2>
            <div class="project-stack">
              <p class="stack-component">Python Libraries</p>
              <p class="stack-component">Ghidra</p>
              <p class="stack-component">VS Code</p>
              <p class="stack-component">Linux & Windows</p>
              
            </div>
            <ul class="project-description">
              <li> <b>Objective:</b> 
              
Designed a software solution that generates new types of malware using an existing malware dataset, leveraging the 
capabilities of Generative AI. The project involved categorizing the output based on the threat level of the malware 
and integrating cybersecurity tools and protocols to address these threats. t.
              </li>
              <li> <b>Key Responsibilities:</b>
                I designed and implemented a system that generates new malware samples by training a Generative AI model on an existing malware dataset. After generating these samples, I categorized them according to their threat levels using advanced classification algorithms. To understand their behavior and potential risks, I tested the generated malware against standard cybersecurity tools and monitoring environments. Based on the classified threat levels, I also developed targeted cybersecurity controls to ensure effective mitigation and prevention strategies were applied.
              </li>
              <li><b>Outcome:</b> 
                I produced a comprehensive tabulated report documenting each malware sample generated, tested, and classified according to its threat level. From this analysis, I generated actionable insights to help implement the necessary cybersecurity controls required to prevent potential malware outflow. Additionally, I stored all generated data in a structured database to support future analysis, tracking, and research..
              </li>
              
          
            </ul>
          </div>
        </div>

        <div class="project">
          <div class="image-container">
            <img
              src="../assets/person_reidentification.png"
              class="project-image"
              alt="Project-Image"
            
          </div>

          <div class="project-description-container">
            <h2>
              Compiled Expense Tracker using Supervised Learning Algorithm 
            </h2>
            <div class="project-stack">
              <p class="stack-component">Python Libraries</p>
              <p class="stack-component">VS Code</p>
              <p class="stack-component">MongoDB</p>
              <p class="stack-component">Google Colab</p>
            </div>
            <ul class="project-description">
              <li> <b>Objective :</b> 
Developed a system that automatically detects and organizes subscriptions and recurring bills, providing users with 
a clear and comprehensive view of their regular financial commitments.
                
              </li>
              <li><b>Key Responsibilities:</b>
                I designed and implemented a machine learning model to process payment bill data and identify subscriptions and recurring payments. Using supervised learning algorithms, the model classifies transactions into categories based on spending patterns and frequency. I integrated MongoDB to store the categorized data, enabling tracking of spending over time. Additionally, I created a user-friendly output interface that displays categorized expenditures and highlights the highest spending categories. The system is also capable of distinguishing between periodic payments and new or unique transactions, allowing for more accurate and insightful financial tracking.
              </li>
              <li><b>Outcome:</b> 
                I developed a system that generates real-time outputs showing the categories with the highest spending and the amounts spent in each. This enables users to easily track and manage recurring financial commitments, identify spending patterns, and optimize their budget. The system provides clear insights into monthly expenses and streamlines the process of managing subscriptions and bills effectively.
              </li>
              
            </ul>
          </div>
        </div>

       

        <div class="project">
          <div class="image-container">
            <img src="../assets/meAccounts.png" class="project-image" alt="Project-Image" />
            
          </div>

          <div class="project-description-container">
            <h2>MEAccounts - An accounting application for Mangala Enterprises</h2>
            <div class="project-stack">
              <p class="stack-component">Python</p>
              <p class="stack-component">Flask</p>
              <p class="stack-component">MongoDB</p>
              <p class="stack-component">Javascript</p>
              <p class="stack-component">HTML</p>
              <p class="stack-component">CSS</p>
            </div>
            <ul class="project-description">
              <li>It is an accounting application developed for Mangala Enterprises, according to the specifications requested by the company.
              </li>
              <li>
                User could analyze the data in the form of dashboards, charts and graphs.
              </li>
              <li>
                Google-based authentication system was used in the application for a secure-login process.
              </li>
              <li>
                Enables users to filter transactions by date range for generating reports and summaries.
              </li>
              <li>
                Offers administrative control for managing users and data integrity.
              </li>
            </ul>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script setup></script>

<style scoped>
.heading {
  text-align: center;
  font-size: 2rem;
  /* margin-bottom: 2rem; */
  color: #1B3C53;
  font-weight: bold;
}

.projects {
  display: flex;
  justify-content: center;
}

.project {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: flex-start;
  margin-top: 2em;
  padding: 2em;
  border-radius: 10px;
  width: 100%;
  background-color: #fbfaf9;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
  max-width: 1000px;
}

.project:hover {
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.25);
  /* transform: translateY(-8px);   */
}

.image-container {
  margin-right: 2em;
}

.project-image {
  height: 250px;
  width: 250px;
}

h2{
  color: #1B3C53;
}

.projects-list {
  list-style: none;
  padding: 0;
  margin: 0;
  width: 100%;
  max-width: 1100px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
}

.project-stack {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5em;
  /* margin-top: 1em; */
}

.stack-component {
  background-color: #1B3C53;
  color: #fbfaf9;
  padding: 6px 8px;
  border-radius: 20px;
  font-size: 0.9rem;
  font-weight: 500;
  border: none;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  white-space: nowrap;
}

.project-description p {
  text-align: justify;

}

.project-description li{
  text-align: justify;
  margin-top: 5px;
}

.github-buttons-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.github-buttons {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 5px;
  width: 100%;
}

.github-button {
  font-size: 16px;
  background-color: #ffffff;
  border-radius: 5px;
  padding: 5px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 10px;
  padding: 5px;
  font-family: 'Times New Roman', Times, serif;
  margin-top: 10px;
  width: 100%;
}
.github-button:hover {
  cursor: pointer;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.25);
}

.github-image {
  height: 20px;
  width: 20px;
}
</style>
