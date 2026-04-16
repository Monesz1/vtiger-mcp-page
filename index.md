---
layout: default
---

<main style="display: grid; grid-template-columns: 1fr 1.2fr; gap: 48px; padding: 48px; align-items: center; max-width: 1200px; margin: 0 auto;">
  <section class="hero-content">
    <h1 style="font-size: 56px; line-height: 1.1; font-weight: 800; margin-bottom: 24px; letter-spacing: -2px;">{{ site.data.site.hero.headline }}</h1>
    <p style="font-size: 18px; color: var(--color-muted); margin-bottom: 32px; max-width: 440px;">{{ site.data.site.hero.subheadline }}</p>
    <div class="cta-group" style="display: flex; gap: 16px;">
      <a href="{{ '/setup/' | relative_url }}" class="btn btn-primary">{{ site.data.site.hero.cta_primary }}</a>
      <a href="{{ '/connection-test/' | relative_url }}" class="btn btn-secondary">{{ site.data.site.hero.cta_secondary }}</a>
    </div>
  </section>

  <section class="widgets-container" style="display: flex; flex-direction: column; gap: 24px;">
    <div class="widget connection-tester" style="background: #1A1A2E; color: white; border: none; border-radius: var(--border-radius); padding: 24px;">
      <div class="widget-title" style="font-size: 12px; text-transform: uppercase; letter-spacing: 1px; font-weight: 700; margin-bottom: 16px; opacity: 0.8;">Kapcsolat tesztelése (Live Sandbox)</div>
      <div class="form-group" style="margin-bottom: 12px;">
        <label style="display: block; font-size: 11px; margin-bottom: 4px; opacity: 0.6;">vtigerCRM URL</label>
        <div class="input-mock" style="width: 100%; padding: 10px; background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1); border-radius: 6px; color: white; font-size: 13px; font-family: monospace;">https://crm.cegem.hu</div>
      </div>
      <div class="form-group" style="margin-bottom: 12px;">
        <label style="display: block; font-size: 11px; margin-bottom: 4px; opacity: 0.6;">Felhasználónév</label>
        <div class="input-mock" style="width: 100%; padding: 10px; background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1); border-radius: 6px; color: white; font-size: 13px; font-family: monospace;">admin</div>
      </div>
      <div class="form-group" style="margin-bottom: 12px;">
        <label style="display: block; font-size: 11px; margin-bottom: 4px; opacity: 0.6;">AccessKey</label>
        <div class="input-mock" style="width: 100%; padding: 10px; background: rgba(255,255,255,0.05); border: 1px solid rgba(255,255,255,0.1); border-radius: 6px; color: white; font-size: 13px; font-family: monospace;">••••••••••••••••</div>
      </div>
      <div class="status-panel" style="margin-top: 20px; padding: 12px; background: rgba(16, 185, 129, 0.1); border: 1px solid var(--color-success); border-radius: 8px; color: var(--color-success); font-size: 13px; display: flex; align-items: center; gap: 8px;">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg>
        Sikeres csatlakozás: 34 elérhető modul.
      </div>
    </div>

    <div class="setup-steps" style="display: grid; grid-template-columns: 1fr 1fr; gap: 16px;">
      <div class="step-mini" style="background: white; padding: 16px; border-radius: 8px; border: 1px solid var(--color-border);">
        <div class="step-number" style="width: 24px; height: 24px; background: var(--color-primary); color: white; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 12px; font-weight: bold; margin-bottom: 12px;">1</div>
        <div class="step-text" style="font-size: 13px; font-weight: 600;">Másold ki az MCP szerver URL-t</div>
      </div>
      <div class="step-mini" style="background: white; padding: 16px; border-radius: 8px; border: 1px solid var(--color-border);">
        <div class="step-number" style="width: 24px; height: 24px; background: var(--color-primary); color: white; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 12px; font-weight: bold; margin-bottom: 12px;">2</div>
        <div class="step-text" style="font-size: 13px; font-weight: 600;">Add hozzá a Claude Custom Connectort</div>
      </div>
      <div class="step-mini" style="background: white; padding: 16px; border-radius: 8px; border: 1px solid var(--color-border);">
        <div class="step-number" style="width: 24px; height: 24px; background: var(--color-primary); color: white; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 12px; font-weight: bold; margin-bottom: 12px;">3</div>
        <div class="step-text" style="font-size: 13px; font-weight: 600;">Add meg a CRM hitelesítő adataidat</div>
      </div>
      <div class="step-mini" style="background: white; padding: 16px; border-radius: 8px; border: 1px solid var(--color-border);">
        <div class="step-number" style="width: 24px; height: 24px; background: var(--color-primary); color: white; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 12px; font-weight: bold; margin-bottom: 12px;">4</div>
        <div class="step-text" style="font-size: 13px; font-weight: 600;">Kezdj el beszélgetni az adataiddal</div>
      </div>
    </div>
  </section>
</main>

<section class="features">
  <div class="container">
    <div class="features-grid">
      {% for feature in site.data.site.features %}
      <div class="feature-card">
        <div class="feature-icon">{{ feature.icon }}</div>
        <h3>{{ feature.title }}</h3>
        <p>{{ feature.body }}</p>
      </div>
      {% endfor %}
    </div>
  </div>
</section>
