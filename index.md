---
layout: home
title: Home
---

<style>
  /* 1. Animation Keyframes */
  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* 2. Global Styles for the Home Page */
  .profile-section {
    text-align: center;
    padding: 40px 0;
    animation: fadeInUp 0.8s ease-out;
  }
  
  .profile-img {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    margin-bottom: 20px;
  }

  .bio-text {
    font-size: 1.2rem;
    color: #555;
    max-width: 600px;
    margin: 0 auto;
  }

  /* 3. Post List Styling */
  .post-list li {
    transition: transform 0.2s ease, box-shadow 0.2s ease;
    padding: 15px;
    border-radius: 8px;
    margin-bottom: 20px;
    border: 1px solid #eee;
    background: white;
    animation: fadeInUp 0.5s ease-out backwards;
  }

  /* Stagger animations for list items */
  .post-list li:nth-child(1) { animation-delay: 0.1s; }
  .post-list li:nth-child(2) { animation-delay: 0.2s; }
  .post-list li:nth-child(3) { animation-delay: 0.3s; }
  .post-list li:nth-child(4) { animation-delay: 0.4s; }

  .post-list li:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 20px rgba(0,0,0,0.1);
    border-color: #ddd;
  }

  .post-meta {
    font-size: 0.9rem;
    color: #888;
  }
</style>

<div class="profile-section">
  <img src="https://github.com/guptaaditya746.png" alt="Aditya Profile" class="profile-img">
  <h1>Aditya's Research Lab</h1>
  <p class="bio-text">
    Exploring the boundaries of <strong>Machine Learning</strong>, <strong>Anomaly Detection</strong>, and <strong>Explainable AI</strong>. 
    <br> Researcher @ DLR Jena, Germany.
  </p>
</div>

<h2>Latest Research & Thoughts</h2>

<ul class="post-list">
  {% for post in site.posts limit:5 %}
    <li>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h3>
      <span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</span>
      <p>{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
    </li>
  {% endfor %}
</ul>
