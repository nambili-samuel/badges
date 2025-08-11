Welcome to Nambili Samuel's Badge Repository! These badges represent collections awarded to Nambili Samuel by various entities and institutions as recognition of his work.  Howver, there is no single badge published by Nambili. Please take a moment to read the README file and the license for this repository


* Generate a ready-to-fill `badges.json` or Jekyll include file that renders the grid automatically.
* Convert your existing badge list into the exact card HTML (you can paste it here).

<style>
.badges-grid {
  display: grid;
  grid-template-columns: repeat(6, 1fr); /* 6 columns */
  gap: 1rem;
  align-items: start;
}

.badge-card {
  background: #ffffff;
  border: 1px solid rgba(15,23,42,0.06);
  border-radius: 10px;
  box-shadow: 0 6px 18px rgba(2,6,23,0.04);
  padding: 12px;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  min-height: 180px; /* ensures equal card heights */
  box-sizing: border-box;
}

.badge-image {
  width: 96px;
  height: 96px;
  object-fit: contain;
  margin-bottom: 10px;
}

.badge-meta {
  font-size: 12px;
  color: #334155;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.badge-title {
  font-weight: 700;
  font-size: 13px;
  color: #0f172a;
}

.badge-org {
  font-size: 12px;
  color: #475569;
}

.badge-date {
  font-size: 11px;
  color: #6b7280;
}

.badge-cta {
  margin-top: 8px;
  font-size: 12px;
}

/* Responsiveness */
@media (max-width: 1400px) { .badges-grid { grid-template-columns: repeat(4, 1fr); } }
@media (max-width: 900px)  { .badges-grid { grid-template-columns: repeat(3, 1fr); } }
@media (max-width: 700px)  { .badges-grid { grid-template-columns: repeat(2, 1fr); } }
@media (max-width: 420px)  { .badges-grid { grid-template-columns: repeat(1, 1fr); } }
</style>

<div class="badges-grid">

  <!-- Repeat this block for each badge -->
  <div class="badge-card">
    <img class="badge-image" src="https://placehold.co/96x96/EEE/000?text=Badge" alt="Badge: Example Certified" />
    <div class="badge-meta">
      <div class="badge-title">Example Certified — Level 1</div>
      <div class="badge-org">Issued by: Acme Institute</div>
      <div class="badge-date">Issued: 2024-08-01</div>
      <div class="badge-cta"><a href="#" rel="noopener">View credential</a></div>
    </div>
  </div>
  <!-- /badge block -->

  <!-- Add as many badge blocks as you need -->

</div>
