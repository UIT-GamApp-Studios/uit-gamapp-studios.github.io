---
layout: default

---

# About

Gen 1

<section>
  <div class="members-grid">
    {% for member in site.data.about %}
    <div class="member-card">
      <img src="{{ member.image | relative_url }}" alt="{{ member.name }}">
      <h2>{{ member.name }}</h2>
      <p class="status">{{ member.status }}</p>
    </div>
    {% endfor %}
  </div>
</section>

<style>

.members-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 10px;
  margin-top: 10px;
}
.member-card {
  border-radius: 1rem;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  padding: 10px;
  transition: transform 0.2s ease;
}
.member-card:hover {
  transform: translateY(-5px);
}
.member-card img {
  max-width: 100%;
  aspect-ratio: 1 / 1;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 10px;
}
.member-card h2 {
  margin: 0.5rem 0;
  font-size: 1.2rem;
}
.member-card .status {
  color: #666;
  font-style: italic;
}
</style>