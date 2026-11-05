             HTML

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Assignment 7.4 — Modern Landing Page Header & Hero</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <!-- ================= STEP 1 & 6: STICKY HEADER ================= -->
  <header class="header">
    <div class="nav-container">
      <a href="#" class="logo">Nexus<span>Flow</span></a>
      <nav class="nav-menu">
        <a href="#features">Features</a>
        <a href="#solutions">Solutions</a>
        <a href="#pricing">Pricing</a>
        <a href="#resources">Resources</a>
      </nav>
      <div class="nav-cta">
        <a href="#get-started" class="btn btn-primary">Start Free Trial</a>
      </div>
    </div>
  </header>

  <!-- ================= STEP 2, 3, 4, 5: HERO SECTION ================= -->
  <main>
    <section class="hero-section">
      <div class="hero-container">
        
        <!-- Step 2: Hero Text Content -->
        <div class="hero-content">
          <span class="badge">Next-Gen Analytics Platform</span>
          <h1 class="hero-heading">Scale your workflow with intelligent data automation</h1>
          <p class="hero-subtext">
            Streamline operational bottlenecks, automate recurring reports, and deliver real-time collaboration tools straight to your distributed engineering teams.
          </p>
          <div class="hero-actions">
            <a href="#signup" class="btn btn-primary btn-lg">Get Started Now</a>
            <a href="#demo" class="btn btn-secondary btn-lg">Watch 2-Min Demo</a>
          </div>
          <p class="hero-foot-note">Free 14-day trial • No credit card required</p>
        </div>

        <!-- Step 3: Hero Illustration / Image -->
        <div class="hero-visual">
          <img 
            src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?w=900&auto=format&fit=crop&q=80" 
            alt="Data analytics dashboard visualization showing metrics and charts"
            class="hero-image"
          >
        </div>

      </div>
    </section>
  </main>

  <!-- ================= STEP 6: STYLED FOOTER ================= -->
  <footer class="footer">
    <div class="footer-container">
      <p>&copy; 2026 NexusFlow Technologies, Inc. All rights reserved.</p>
      <div class="footer-links">
        <a href="#privacy">Privacy Policy</a>
        <a href="#terms">Terms of Service</a>
        <a href="#support">Support</a>
      </div>
    </div>
  </footer>

</body>
</html>



                     CSS


/* --- Global Reset & Design Tokens --- */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  color: #1e293b;
  background-color: #ffffff;
  line-height: 1.6;
}

/* --- Step 1 & 6: Sticky Navigation Header --- */
.header {
  position: sticky;                  /* Sticky positioning requirement */
  top: 0;
  z-index: 1000;
  background-color: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(8px);
  border-bottom: 1px solid #e2e8f0;
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 1.1rem 2rem;
}

.logo {
  font-size: 1.5rem;
  font-weight: 800;
  color: #0f172a;
  text-decoration: none;
  letter-spacing: -0.02em;
}

.logo span {
  color: #2563eb;
}

.nav-menu {
  display: flex;
  gap: 2rem;
}

.nav-menu a {
  text-decoration: none;
  font-weight: 500;
  font-size: 0.95rem;
  color: #475569;
  transition: color 0.2s ease;
}

.nav-menu a:hover {
  color: #2563eb;
}

/* --- Shared Button Components --- */
.btn {
  display: inline-block;
  text-decoration: none;
  font-weight: 600;
  border-radius: 8px;
  transition: all 0.2s ease;
  cursor: pointer;
}

.btn-primary {
  background-color: #2563eb;
  color: #ffffff;
  padding: 0.65rem 1.3rem;
  border: 1px solid #2563eb;
}

.btn-primary:hover {
  background-color: #1d4ed8;
  border-color: #1d4ed8;
}

.btn-secondary {
  background-color: #f1f5f9;
  color: #0f172a;
  padding: 0.65rem 1.3rem;
  border: 1px solid #cbd5e1;
}

.btn-secondary:hover {
  background-color: #e2e8f0;
}

.btn-lg {
  padding: 0.85rem 1.6rem;
  font-size: 1rem;
}

/* --- Step 2, 4 & 5: Flexbox Hero Layout --- */
.hero-section {
  padding: 5rem 2rem;
  background: linear-gradient(180deg, #f8fafc 0%, #ffffff 100%);
  display: flex;
  justify-content: center;
}

.hero-container {
  display: flex;                     /* Step 4: Flexbox side-by-side alignment */
  flex-direction: row;
  justify-content: space-between;
  align-items: center;               /* Step 5: Center-align content vertically */
  gap: 4rem;
  max-width: 1200px;
  width: 100%;
}

/* Text Content Area */
.hero-content {
  flex: 1 1 50%;                    /* Allocates 50% width baseline */
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.badge {
  display: inline-block;
  background-color: #dbeafe;
  color: #1e40af;
  font-size: 0.8rem;
  font-weight: 700;
  padding: 0.35rem 0.85rem;
  border-radius: 9999px;
  margin-bottom: 1.25rem;
  letter-spacing: 0.03em;
  text-transform: uppercase;
}

.hero-heading {
  font-size: 3rem;
  font-weight: 800;
  line-height: 1.15;
  color: #0f172a;
  letter-spacing: -0.03em;
  margin-bottom: 1.25rem;
}

.hero-subtext {
  font-size: 1.15rem;
  color: #64748b;
  margin-bottom: 2rem;
}

.hero-actions {
  display: flex;
  gap: 1rem;
  margin-bottom: 1rem;
}

.hero-foot-note {
  font-size: 0.85rem;
  color: #94a3b8;
}

/* Step 3: Hero Image Presentation */
.hero-visual {
  flex: 1 1 50%;                    /* Allocates 50% width baseline */
  display: flex;
  justify-content: center;
}

.hero-image {
  width: 100%;
  max-width: 540px;
  height: auto;
  border-radius: 16px;
  box-shadow: 0 20px 35px -10px rgba(15, 23, 42, 0.15);
  display: block;
}

/* --- Step 6: Styled Footer --- */
.footer {
  border-top: 1px solid #e2e8f0;
  background-color: #0f172a;
  color: #94a3b8;
  padding: 2.5rem 2rem;
}

.footer-container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.9rem;
}

.footer-links {
  display: flex;
  gap: 1.5rem;
}

.footer-links a {
  color: #94a3b8;
  text-decoration: none;
  transition: color 0.2s ease;
}

.footer-links a:hover {
  color: #ffffff;
}

/* --- Step 7: Responsive Media Queries --- */
@media (max-width: 900px) {
  .hero-container {
    flex-direction: column-reverse;  /* Stacks visual and text on tablet/mobile */
    text-align: center;
    gap: 2.5rem;
  }

  .hero-content {
    align-items: center;
  }

  .hero-heading {
    font-size: 2.25rem;
  }

  .hero-actions {
    flex-direction: column;
    width: 100%;
    max-width: 320px;
  }

  .nav-menu {
    display: none;                  /* Preserves layout cleanly on mobile viewports */
  }

  .footer-container {
    flex-direction: column;
    gap: 1.25rem;
    text-align: center;
  }
}