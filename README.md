/* ===== Global Reset & Base ===== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --ivory: #FFFBF7;
  --cream: #F6EEE4;
  --deep-beige: #C8BFAF;
  --bronze-light: #D4B996;
  --bronze: #B8986C;
  --dark-nude: #5C5448;
  --soft-charcoal: #3A362F;
  --fresh: #2F4238;
  --sweet: #7B6694;
  --confident: #4A5568;
  --romance: #A86464;
}

html, body {
  min-height: 100vh;
  font-family: 'Segoe UI', Georgia, 'Times New Roman', serif;
  background-color: var(--ivory);
  color: var(--soft-charcoal);
  line-height: 1.6;
}

h1, h2, h3, h4 {
  font-family: Georgia, 'Times New Roman', Times, serif;
  font-weight: 400;
  color: var(--soft-charcoal);
}

a {
  text-decoration: none;
  color: inherit;
}

.container {
  width: 90%;
  max-width: 1200px;
  margin: 0 auto;
}

/* ===== Navigation ===== */
nav {
  padding: 1.5rem 0;
  border-bottom: 1px solid rgba(184, 152, 108, 0.15);
}

nav .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

nav .logo {
  font-family: Georgia, serif;
  font-size: 1.6rem;
  color: var(--soft-charcoal);
  letter-spacing: 2px;
}

nav .nav-links a {
  margin-left: 2rem;
  font-size: 0.95rem;
  color: var(--dark-nude);
  transition: color 0.3s ease;
}

nav .nav-links a:hover {
  color: var(--bronze);
}

/* ===== Hero Section ===== */
.hero {
  min-height: 85vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 4rem 2rem;
}

.hero-content h1 {
  font-size: clamp(1.8rem, 4vw, 3rem);
  line-height: 1.4;
  margin-bottom: 1.2rem;
  color: var(--soft-charcoal);
}

.hero-content p {
  font-size: 1.1rem;
  color: var(--dark-nude);
  margin-bottom: 2.5rem;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.hero-line {
  width: 60px;
  height: 2px;
  background-color: var(--bronze-light);
  margin: 0 auto 2rem;
}

/* ===== Buttons ===== */
.btn-outline {
  display: inline-block;
  border: 1px solid var(--bronze);
  color: var(--bronze);
  padding: 0.8rem 2.2rem;
  font-size: 0.95rem;
  letter-spacing: 1px;
  transition: all 0.3s ease;
  background: transparent;
  cursor: pointer;
  font-family: inherit;
}

.btn-outline:hover {
  background-color: var(--bronze);
  color: #fff;
}

.btn-solid {
  display: inline-block;
  background-color: var(--bronze);
  color: #fff;
  border: 1px solid var(--bronze);
  padding: 0.8rem 2.2rem;
  font-size: 0.95rem;
  letter-spacing: 1px;
  transition: all 0.3s ease;
  cursor: pointer;
  font-family: inherit;
}

.btn-solid:hover {
  background-color: var(--bronze-light);
  border-color: var(--bronze-light);
  color: var(--soft-charcoal);
}

/* ===== Moods Section ===== */
.moods-section {
  padding: 5rem 0 6rem;
}

.section-heading {
  text-align: center;
  font-size: 1.8rem;
  margin-bottom: 0.8rem;
}

.section-underline {
  width: 40px;
  height: 2px;
  background-color: var(--bronze-light);
  margin: 0 auto 3rem;
}

.moods-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 2rem;
}

.mood-card {
  background-color: #fff;
  border: 1px solid var(--deep-beige);
  padding: 2.5rem 1.5rem;
  text-align: center;
  transition: all 0.35s ease;
}

.mood-card:hover {
  transform: translateY(-5px);
  border-color: var(--bronze-light);
}

.mood-icon-dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  margin: 0 auto 1.2rem;
}

.mood-card h3 {
  font-size: 1.15rem;
  margin-bottom: 0.5rem;
}

.mood-card p {
  font-size: 0.9rem;
  color: var(--dark-nude);
}

.dot-fresh { background-color: var(--fresh); }
.dot-sweet { background-color: var(--sweet); }
.dot-confident { background-color: var(--confident); }
.dot-romance { background-color: var(--romance); }

/* ===== Products Page ===== */
.products-header {
  text-align: center;
  padding: 3rem 0 1rem;
}

.products-header h2 {
  font-size: 1.8rem;
  margin-bottom: 0.5rem;
}

#filter-bar {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 0.8rem;
  margin-bottom: 3rem;
}

.filter-btn {
  border: 1px solid var(--deep-beige);
  background: transparent;
  color: var(--dark-nude);
  padding: 0.55rem 1.2rem;
  font-size: 0.9rem;
  cursor: pointer;
  transition: all 0.3s ease;
}

.filter-btn:hover,
.filter-btn.active {
  border-color: var(--bronze);
  color: var(--bronze);
}

#product-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 2.5rem;
  padding-bottom: 5rem;
}

.product-card {
  background-color: #fff;
  border: 1px solid rgba(184, 152, 108, 0.15);
  overflow: hidden;
  transition: box-shadow 0.3s ease;
}

.product-card:hover {
  box-shadow: 0 8px 25px rgba(92, 84, 72, 0.06);
}

.product-image {
  width: 100%;
  height: 240px;
  object-fit: cover;
  background-color: var(--cream);
}

.product-info {
  padding: 1.5rem;
}

.product-info h3 {
  font-size: 1.05rem;
  margin-bottom: 0.3rem;
}

.product-size {
  font-size: 0.85rem;
  color: var(--dark-nude);
  margin-bottom: 0.8rem;
}

.product-desc {
  font-size: 0.9rem;
  color: var(--dark-nude);
  line-height: 1.5;
  margin-bottom: 1rem;
}

.product-price {
  font-size: 1.1rem;
  color: var(--bronze);
  font-family: Georgia, serif;
  margin-bottom: 1rem;
}

.product-info .btn-outline {
  width: 100%;
  text-align: center;
  padding: 0.6rem;
  font-size: 0.9rem;
}

/* ===== Form & Order Page ===== */
.form-section {
  padding: 4rem 0;
  max-width: 520px;
  margin: 0 auto;
}

.form-section h2 {
  text-align: center;
  font-size: 1.6rem;
  margin-bottom: 0.5rem;
}

.form-underline {
  width: 40px;
  height: 2px;
  background-color: var(--bronze-light);
  margin: 0 auto 2.5rem;
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group label {
  display: block;
  font-size: 0.95rem;
  color: var(--dark-nude);
  margin-bottom: 0.5rem;
}

.form-group input,
.form-group textarea,
.form-group input:disabled {
  width: 100%;
  padding: 0.9rem 1rem;
  border: 1px solid var(--deep-beige);
  background-color: #fff;
  color: var(--soft-charcoal);
  font-size: 0.95rem;
  font-family: inherit;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--bronze);
}

.form-group input:disabled {
  background-color: var(--cream);
  color: var(--dark-nude);
}

.form-group textarea {
  resize: vertical;
  min-height: 100px;
}

.form-submit {
  text-align: center;
  margin-top: 2rem;
}

/* ===== Thank You Page ===== */
.thankyou-section {
  min-height: 70vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 4rem 2rem;
}

.thankyou-section h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
}

.thankyou-section p {
  color: var(--dark-nude);
  margin-bottom: 2rem;
  max-width: 450px;
}

/* ===== Admin / Orders Table ===== */
.admin-section {
  padding: 3rem 0 5rem;
}

.admin-section h2 {
  text-align: center;
  font-size: 1.6rem;
  margin-bottom: 0.5rem;
}

.table-wrapper {
  overflow-x: auto;
  border: 1px solid var(--deep-beige);
  background-color: #fff;
}

#ordersTable {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.9rem;
}

#ordersTable th,
#ordersTable td {
  padding: 0.9rem 1rem;
  text-align: left;
  border-bottom: 1px solid rgba(184, 152, 108, 0.15);
  vertical-align: top;
}

#ordersTable th {
  background-color: var(--cream);
  font-family: Georgia, serif;
  font-weight: 400;
  color: var(--soft-charcoal);
  font-size: 0.85rem;
  letter-spacing: 0.5px;
}

#ordersTable td {
  color: var(--dark-nude);
}

.empty-row td {
  text-align: center;
  padding: 3rem;
  color: var(--deep-beige);
}

/* ===== Footer ===== */
footer {
  border-top: 1px solid rgba(184, 152, 108, 0.15);
  text-align: center;
  padding: 2rem;
  font-size: 0.85rem;
  color: var(--deep-beige);
  margin-top: auto;
}

/* ===== Responsive ===== */
@media (max-width: 768px) {
  nav .nav-links {
    display: flex;
    gap: 1rem;
  }

  nav .nav-links a {
    margin-left: 0;
    font-size: 0.85rem;
  }

  .moods-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
  }

  #product-list {
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 1.5rem;
  }

  #ordersTable th,
  #ordersTable td {
    padding: 0.6rem 0.5rem;
    font-size: 0.8rem;
  }
}

@media (max-width: 480px) {
  .moods-grid {
    grid-template-columns: 1fr;
  }
}
