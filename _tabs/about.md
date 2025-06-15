---
# the default layout is 'page'
icon: fas fa-info-circle
order: 4
---

<style>
:root {
  --primary-color: #2c3e50;
  --secondary-color: #3498db;
  --accent-color: #e74c3c;
  --success-color: #27ae60;
  --warning-color: #f39c12;
  --light-bg: #f8f9fa;
  --dark-text: #2c3e50;
  --muted-text: #6c757d;
  --border-color: #dee2e6;
}

.professional-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.hero-banner {
  background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
  border-radius: 12px;
  padding: 60px 40px;
  color: white;
  text-align: center;
  margin-bottom: 40px;
  box-shadow: 0 8px 32px rgba(0,0,0,0.1);
  position: relative;
  overflow: hidden;
}

.hero-banner::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="25" cy="25" r="1" fill="rgba(255,255,255,0.03)"/><circle cx="75" cy="75" r="1" fill="rgba(255,255,255,0.03)"/><circle cx="25" cy="75" r="1" fill="rgba(255,255,255,0.03)"/><circle cx="75" cy="25" r="1" fill="rgba(255,255,255,0.03)"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
  opacity: 0.1;
}

.profile-image-container {
  position: relative;
  display: inline-block;
  margin-bottom: 30px;
}

.profile-image {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  object-fit: cover;
  border: 6px solid rgba(255,255,255,0.2);
  box-shadow: 0 12px 40px rgba(0,0,0,0.2);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.profile-image:hover {
  transform: translateY(-5px);
  box-shadow: 0 20px 60px rgba(0,0,0,0.3);
}

.hero-title {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 10px;
  position: relative;
  z-index: 1;
}

.hero-subtitle {
  font-size: 1.3rem;
  font-weight: 300;
  margin-bottom: 20px;
  opacity: 0.9;
  position: relative;
  z-index: 1;
}

.hero-description {
  font-size: 1.1rem;
  line-height: 1.6;
  max-width: 800px;
  margin: 0 auto 30px;
  opacity: 0.95;
  position: relative;
  z-index: 1;
}

.contact-bar {
  display: flex;
  justify-content: center;
  gap: 30px;
  flex-wrap: wrap;
  margin-top: 30px;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 12px 20px;
  background: rgba(255,255,255,0.15);
  border-radius: 30px;
  font-size: 0.95rem;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255,255,255,0.1);
  transition: all 0.3s ease;
}

.contact-item:hover {
  background: rgba(255,255,255,0.25);
  transform: translateY(-2px);
}

.section-card {
  background: white;
  border-radius: 12px;
  padding: 40px;
  margin-bottom: 30px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.08);
  border: 1px solid var(--border-color);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.section-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 30px rgba(0,0,0,0.12);
}

.section-title {
  color: var(--primary-color);
  font-size: 1.8rem;
  font-weight: 600;
  margin-bottom: 30px;
  padding-bottom: 15px;
  border-bottom: 3px solid var(--secondary-color);
  display: flex;
  align-items: center;
  gap: 12px;
}

.achievement-highlight {
  background: linear-gradient(135deg, #ffd700 0%, #ffed4e 100%);
  color: var(--dark-text);
  padding: 30px;
  border-radius: 12px;
  text-align: center;
  font-size: 1.2rem;
  font-weight: 600;
  margin: 20px 0;
  box-shadow: 0 6px 25px rgba(255,215,0,0.3);
}

.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 25px;
  margin-top: 25px;
}

.info-item {
  background: var(--light-bg);
  padding: 25px;
  border-radius: 8px;
  border-left: 4px solid var(--secondary-color);
  transition: all 0.3s ease;
}

.info-item:hover {
  background: #f1f3f4;
  transform: translateX(5px);
}

.info-item h4 {
  color: var(--primary-color);
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 8px;
  display: flex;
  align-items: center;
  gap: 8px;
}

.info-item p {
  color: var(--muted-text);
  line-height: 1.5;
  margin: 0;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  margin-top: 25px;
}

.skill-item {
  background: var(--light-bg);
  padding: 25px;
  border-radius: 8px;
  text-align: center;
  border: 1px solid var(--border-color);
  transition: all 0.3s ease;
}

.skill-item:hover {
  background: white;
  box-shadow: 0 4px 15px rgba(0,0,0,0.1);
  transform: translateY(-3px);
}

.skill-icon {
  font-size: 2rem;
  margin-bottom: 15px;
  color: var(--secondary-color);
}

.badge-container {
  display: flex;
  justify-content: center;
  gap: 15px;
  flex-wrap: wrap;
  margin-top: 20px;
}

.professional-badge {
  background: var(--secondary-color);
  color: white;
  padding: 8px 16px;
  border-radius: 20px;
  font-size: 0.9rem;
  font-weight: 500;
  display: flex;
  align-items: center;
  gap: 6px;
  transition: all 0.3s ease;
}

.professional-badge:hover {
  background: var(--primary-color);
  transform: translateY(-1px);
}

.experience-timeline {
  position: relative;
  padding-left: 30px;
}

.experience-timeline::before {
  content: '';
  position: absolute;
  left: 15px;
  top: 0;
  bottom: 0;
  width: 2px;
  background: var(--secondary-color);
}

.timeline-item {
  position: relative;
  margin-bottom: 30px;
  background: var(--light-bg);
  padding: 20px;
  border-radius: 8px;
  margin-left: 20px;
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: -35px;
  top: 25px;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: var(--secondary-color);
  border: 3px solid white;
  box-shadow: 0 0 0 3px var(--secondary-color);
}

.timeline-item h4 {
  color: var(--primary-color);
  font-weight: 600;
  margin-bottom: 5px;
}

.timeline-item .date {
  color: var(--muted-text);
  font-size: 0.9rem;
  font-weight: 500;
}

.professional-quote {
  background: var(--primary-color);
  color: white;
  padding: 40px;
  border-radius: 12px;
  text-align: center;
  font-size: 1.2rem;
  font-style: italic;
  line-height: 1.6;
  margin-top: 40px;
  position: relative;
  overflow: hidden;
}

.professional-quote::before {
  content: '"';
  position: absolute;
  top: 10px;
  left: 20px;
  font-size: 4rem;
  opacity: 0.1;
  font-family: serif;
}

.professional-quote::after {
  content: '"';
  position: absolute;
  bottom: 10px;
  right: 20px;
  font-size: 4rem;
  opacity: 0.1;
  font-family: serif;
}

@media (max-width: 768px) {
  .hero-banner {
    padding: 40px 20px;
  }
  
  .hero-title {
    font-size: 2rem;
  }
  
  .section-card {
    padding: 25px;
  }
  
  .contact-bar {
    gap: 15px;
  }
  
  .contact-item {
    padding: 10px 16px;
    font-size: 0.9rem;
  }
}
</style>

<div class="professional-container">
  <div class="hero-banner">
    <div class="profile-image-container">
      <img src="/assets/img/profile.jpg" alt="Preethu Mohanan KK" class="profile-image">
    </div>
    
    <h1 class="hero-title">Preethu Mohanan KK</h1>
    <h2 class="hero-subtitle">Physiotherapist & Healthcare Educator</h2>
    
    <p class="hero-description">
      Dedicated healthcare professional with expertise in clinical assessment, diagnosis, and personalized treatment for musculoskeletal and neuromuscular conditions. Committed to integrating evidence-based practices into teaching and patient care while fostering collaboration and mentoring future healthcare professionals.
    </p>
    
    <div class="contact-bar">
      <div class="contact-item">
        <i class="fas fa-envelope"></i>
        preethu088@gmail.com
      </div>
      <div class="contact-item">
        <i class="fas fa-map-marker-alt"></i>
        Bangalore, Karnataka
      </div>
      <div class="contact-item">
        <i class="fas fa-hospital"></i>
        Akash Institute of Physiotherapy
      </div>
    </div>
  </div>

  <div class="section-card">
    <h2 class="section-title">
      <i class="fas fa-graduation-cap"></i>
      Educational Excellence
    </h2>
    
    <div class="info-grid">
      <div class="info-item">
        <h4><i class="fas fa-medal"></i> Master of Physiotherapy (MPT)</h4>
        <p><strong>Specialization:</strong> Musculoskeletal and Sports</p>
        <p><strong>Institution:</strong> Kerala University of Health and Science - Thrissur</p>
        <p><strong>Graduation:</strong> December 2023</p>
      </div>
      
      <div class="info-item">
        <h4><i class="fas fa-book"></i> Bachelor of Physiotherapy (BPT)</h4>
        <p><strong>Institution:</strong> Kerala University of Health and Science - Thrissur</p>
        <p><strong>Graduation:</strong> September 2019</p>
      </div>
    </div>
    
    <div class="achievement-highlight">
      <i class="fas fa-trophy"></i> 1st Rank Holder in MPT-Musculoskeletal and Sports
      <br>Kerala University of Health Sciences
    </div>
  </div>

  <div class="section-card">
    <h2 class="section-title">
      <i class="fas fa-briefcase"></i>
      Professional Experience
    </h2>
    
    <div class="experience-timeline">
      <div class="timeline-item">
        <h4><i class="fas fa-star"></i> Current Position</h4>
        <p><strong>Akash Institute of Physiotherapy</strong> - Devanahalli, Bangalore</p>
        <div class="date">Present</div>
      </div>
      
      <div class="timeline-item">
        <h4>Physiotherapist</h4>
        <p><strong>Vatakara Physiotherapy Clinic</strong> - Calicut</p>
        <div class="date">April 2024 - July 2024</div>
      </div>
      
      <div class="timeline-item">
        <h4>Physiotherapist</h4>
        <p><strong>Spectrum Physio</strong> - Bangalore</p>
        <div class="date">March 2023 - March 2024</div>
      </div>
      
      <div class="timeline-item">
        <h4>Physiotherapist</h4>
        <p><strong>Vatakara Physiotherapy Clinic</strong> - Calicut</p>
        <div class="date">August 2020 - May 2021</div>
      </div>
    </div>
  </div>

  <div class="section-card">
    <h2 class="section-title">
      <i class="fas fa-hospital"></i>
      Clinical Excellence
    </h2>
    
    <div class="info-grid">
      <div class="info-item">
        <h4><i class="fas fa-stethoscope"></i> Fortis Hospital</h4>
        <p>Bangalore - 84 Days Clinical Exposure</p>
      </div>
      
      <div class="info-item">
        <h4><i class="fas fa-hospital-alt"></i> Government Hospital</h4>
        <p>Kottayam - 84 Days Clinical Exposure</p>
      </div>
      
      <div class="info-item">
        <h4><i class="fas fa-clinic-medical"></i> Rajagiri Hospital</h4>
        <p>Ernakulam - 1 Month Clinical Exposure</p>
      </div>
      
      <div class="info-item">
        <h4><i class="fas fa-hospital-user"></i> Lourdes Hospital</h4>
        <p>Ernakulam - 1 Month Clinical Exposure</p>
      </div>
    </div>
  </div>

  <div class="section-card">
    <h2 class="section-title">
      <i class="fas fa-cogs"></i>
      Core Competencies
    </h2>
    
    <div class="skills-grid">
      <div class="skill-item">
        <div class="skill-icon"><i class="fas fa-user-md"></i></div>
        <h4>Clinical Excellence</h4>
        <p>Expert in rehabilitation techniques, hydrotherapy, and electrotherapy</p>
      </div>
      
      <div class="skill-item">
        <div class="skill-icon"><i class="fas fa-comments"></i></div>
        <h4>Communication</h4>
        <p>Excellent written and oral communication skills</p>
      </div>
      
      <div class="skill-item">
        <div class="skill-icon"><i class="fas fa-brain"></i></div>
        <h4>Problem-Solving</h4>
        <p>Strong analytical and practical problem-solving abilities</p>
      </div>
      
      <div class="skill-item">
        <div class="skill-icon"><i class="fas fa-laptop-medical"></i></div>
        <h4>Technology</h4>
        <p>Broad knowledge of medical equipment and new technologies</p>
      </div>
      
      <div class="skill-item">
        <div class="skill-icon"><i class="fas fa-users"></i></div>
        <h4>Leadership</h4>
        <p>Effective team collaboration and task management</p>
      </div>
      
      <div class="skill-item">
        <div class="skill-icon"><i class="fas fa-clock"></i></div>
        <h4>Professional</h4>
        <p>Strong adaptability, punctuality, and time management</p>
      </div>
    </div>
  </div>

  <div class="section-card">
    <h2 class="section-title">
      <i class="fas fa-language"></i>
      Languages
    </h2>
    
    <div class="badge-container">
      <div class="professional-badge">
        <i class="fas fa-globe"></i>
        English
      </div>
      <div class="professional-badge">
        <i class="fas fa-flag"></i>
        Malayalam
      </div>
      <div class="professional-badge">
        <i class="fas fa-flag"></i>
        Tamil
      </div>
    </div>
  </div>

  <div class="section-card">
    <h2 class="section-title">
      <i class="fas fa-certificate"></i>
      Professional Development
    </h2>
    
    <div class="info-grid">
      <div class="info-item">
        <h4><i class="fas fa-dumbbell"></i> Current Certification</h4>
        <p>Pursuing Strength and Conditioning Specialist certification</p>
      </div>
      
      <div class="info-item">
        <h4><i class="fas fa-research"></i> Research Project</h4>
        <p><strong>MPT Thesis:</strong> "Efficacy of muscle energy technique on Iliopsoas muscle to reduce tightness and to improve hip extension range of motion among desktop workers"</p>
      </div>
      
      <div class="info-item">
        <h4><i class="fas fa-hands-helping"></i> Specialized Training</h4>
        <p>Musculofacial Release Therapy - Basic and Advanced</p>
      </div>
      
      <div class="info-item">
        <h4><i class="fas fa-syringe"></i> Advanced Techniques</h4>
        <p>Dry Needling Course - International Institute of Healing Science</p>
      </div>
      
      <div class="info-item">
        <h4><i class="fas fa-heartbeat"></i> Emergency Care</h4>
        <p>Basic Life Support Course - American Heart Association</p>
      </div>
      
      <div class="info-item">
        <h4><i class="fas fa-globe-americas"></i> Conferences</h4>
        <p>PHYSIO-CON 2020 & PHYSIO-2020 International Conferences</p>
      </div>
    </div>
  </div>

  <div class="section-card">
    <h2 class="section-title">
      <i class="fas fa-bullseye"></i>
      Specialization Focus
    </h2>
    
    <div class="info-item">
      <h4><i class="fas fa-running"></i> Musculoskeletal & Sports Physiotherapy</h4>
      <div class="info-grid" style="margin-top: 15px;">
        <div class="info-item">
          <p><i class="fas fa-check-circle"></i> Evidence-based rehabilitation practices</p>
        </div>
        <div class="info-item">
          <p><i class="fas fa-check-circle"></i> Clinical assessment and diagnosis</p>
        </div>
        <div class="info-item">
          <p><i class="fas fa-check-circle"></i> Personalized treatment approaches</p>
        </div>
        <div class="info-item">
          <p><i class="fas fa-check-circle"></i> Healthcare education and mentoring</p>
        </div>
      </div>
    </div>
  </div>

  <div class="professional-quote">
    Committed to excellence in physiotherapy practice, education, and advancing healthcare through evidence-based treatment approaches. Dedicated to empowering patients and inspiring future healthcare professionals.
  </div>
</div>
