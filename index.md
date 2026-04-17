---
layout: default
---

<main class="hero-layout">
  <section class="hero-content">
    <h1 style="font-size: 56px; line-height: 1.1; font-weight: 800; margin-bottom: 24px; letter-spacing: -2px;" class="animate-fade-in-up">{{ site.hero.headline }}</h1>
    <p style="font-size: 18px; color: var(--color-muted); margin-bottom: 32px; max-width: 440px;" class="animate-fade-in-up delay-1">{{ site.hero.subheadline }}</p>
    <div class="cta-group animate-fade-in-up delay-2">
      <a href="{{ '/setup/' | relative_url }}" 
         id="api-trigger-btn" 
         class="btn btn-primary" 
         {% if site.hero.background_api_url and site.hero.background_api_url != empty %}
         onclick="triggerBackgroundApi(event, '{{ site.hero.background_api_url }}', '{{ site.hero.background_api_method | default: 'POST' }}', this.href)"
         {% endif %}
      >
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
        {{ site.hero.cta_primary }}
      </a>
    </div>
  </section>

  <section class="widgets-container animate-fade-in-up delay-3">
    <div class="widget connection-tester" style="pointer-events: none;">
      <div class="widget-title" style="font-size: 12px; text-transform: uppercase; letter-spacing: 1px; font-weight: 700; margin-bottom: 20px; color: #64748B;">Kapcsolat tesztelése (Live Sandbox)</div>
      <div class="form-group" style="margin-bottom: 16px;">
        <label style="display: block; font-size: 13px; margin-bottom: 8px; font-weight: 600; color: #334155;">vtigerCRM URL</label>
        <div class="input-mock" style="width: 100%; padding: 12px 14px; background: #F8FAFC; border: 1px solid #CBD5E1; border-radius: 6px; color: #334155; font-size: 14px; font-family: ui-monospace, monospace;">https://crm.cegem.hu</div>
      </div>
      <div class="form-group" style="margin-bottom: 16px;">
        <label style="display: block; font-size: 13px; margin-bottom: 8px; font-weight: 600; color: #334155;">Felhasználónév</label>
        <div class="input-mock" style="width: 100%; padding: 12px 14px; background: #F8FAFC; border: 1px solid #CBD5E1; border-radius: 6px; color: #334155; font-size: 14px; font-family: ui-monospace, monospace;">fnev.pelda</div>
      </div>
      <div class="form-group" style="margin-bottom: 16px;">
        <label style="display: block; font-size: 13px; margin-bottom: 8px; font-weight: 600; color: #334155;">AccessKey</label>
        <div class="input-mock" style="width: 100%; padding: 12px 14px; background: #F8FAFC; border: 1px solid #CBD5E1; border-radius: 6px; color: #334155; font-size: 14px; font-family: ui-monospace, monospace;">••••••••••••••••</div>
      </div>
      <div class="status-panel" style="margin-top: 24px; padding: 16px; background: #ECFDF5; border: 1px solid #A7F3D0; border-radius: 6px; color: #065F46; font-size: 14px; display: flex; align-items: center; gap: 8px; font-weight: 500;">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg>
        Sikeres csatlakozás: 34 elérhető modul.
      </div>
    </div>

    <div class="steps-grid">
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
      {% for feature in site.features %}
      <div class="feature-card">
        <div class="feature-icon">{{ feature.icon }}</div>
        <h3>{{ feature.title }}</h3>
        <p>{{ feature.body }}</p>
      </div>
      {% endfor %}
    </div>
  </div>
</section>
