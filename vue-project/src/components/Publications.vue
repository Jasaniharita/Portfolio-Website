<template>
  <h2 class="heading">Volunteering</h2>

  <div class="publications-container">
    <div
      class="publication"
    >
      <h2>
        Google Developer Student Club
      </h2>

      <p class="abstract">
        <b>Description: </b>
        Led initiatives to promote Google's development tools and technologies (e.g., Firebase, Flutter), enhancing 
        technical knowledge and advocacy skills. Organized coding sessions, workshops, and tech talks for fellow students, 
        fostering a collaborative learning environment. Contributed to community development by organizing Google Cloud 
        Study Jams, assisting peers in learning cloud technologies. Strengthened leadership skills by managing teams for 
        club activities and supporting tech-related events and hackathons.
      </p>
    </div>

    <div
      class="publication"
    >
      <h2>
        Eleet Club (Cybersecurity)
      </h2>

      <p class="abstract">
        <b>Description: </b>
        Collaborated with a team to organize and manage technical workshops and events, enhancing 
        cybersecurity knowledge. Coordinated technical discussions and speaker sessions on emerging technologies, improving 
        communication and networking abilities. Facilitated hands-on coding and tech development workshops, gaining practical 
        experience in using cybersecurity tools.
      </p>
    </div>

    <div
      class="publication"
    >
      <h2>Cyberthon</h2>

      <p class="abstract">
        <b>Description: </b>
        Provided guidance and support to participants by helping them brainstorm and develop innovative 
        solutions to real-world cybersecurity problems. Facilitated communication between teams, ensuring smooth 
        collaboration and effective problem-solving throughout the project. Gained insights into current cybersecurity 
        issues while contributing to the development of actionable solutions for real-world problems. Enhanced teamwork, 
        leadership, and organizational skills by managing participant engagement and helping to coordinate project deliverables.
      </p>
    </div>

    <div
      class="publication"
    >
      <h2>College Orientations</h2>

      <p class="abstract">
        <b>Description: </b>
        Assisted in organizing orientation programs for new students, developing strong organizational and event 
        management skills. Provided mentorship and guidance to incoming students, fostering communication and leadership skills. 
        Coordinated logistics, including registration and resource management, ensuring smooth execution of the 
        orientation events. Built strong interpersonal and teamwork skills by working with faculty and student volunteers to enhance 
        the overall orientation experience.
      </p>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>

.heading {
  text-align: center;
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #1B3C53;
  font-weight: bold;
}

.publications-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
  padding: 0 1rem 2rem;
}

.publication {
  width: 100%;
  max-width: 800px;
  background-color: #fbfaf9;
  border-radius: 16px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
  padding: 2rem;
  transition:
    transform 0.3s ease,
    box-shadow 0.3s ease;
}

.publication:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 28px rgba(0, 0, 0, 0.12);
  cursor: pointer;
}

.publication h2 {
  font-size: 1.3rem;
  margin-bottom: 1rem;
  color: #34495e;
}

.abstract {
  display: -webkit-box;
  -webkit-line-clamp: 5;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  text-align: justify;
  color: #555;
  font-size: 0.95rem;
  margin-bottom: 1rem;
}

.abstract b {
  color: #1B3C53;
}

.publication div p {
  font-size: 0.9rem;
  margin: 0.3rem 0;
  color: #555;
}


.publication b {
  color: #1B3C53;
}

.pub-info-line {
  display: flex;
  gap: 2rem; /* Adjust spacing between the two spans */
  flex-wrap: wrap; /* Allow wrapping on small screens */
  font-size: 0.9rem;
  color: #555;
  margin-bottom: 0.8rem;
}

@media (max-width: 768px) {
  .publication {
    padding: 1.5rem;
  }

  .publication h2 {
    font-size: 1.1rem;
  }

  .abstract {
    font-size: 0.9rem;
  }
}
</style>
