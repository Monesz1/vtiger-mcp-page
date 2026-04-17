---
layout: default
---

<main class="hero-layout">
  <section class="hero-content">
    <h1 style="font-size: 56px; line-height: 1.1; font-weight: 800; margin-bottom: 24px; letter-spacing: -2px;" class="animate-fade-in-up">{{ site.hero.headline }}</h1>
    <p style="font-size: 18px; color: var(--color-muted); margin-bottom: 32px; max-width: 440px;" class="animate-fade-in-up delay-1">{{ site.hero.subheadline }}</p>
    <div class="cta-group animate-fade-in-up delay-2">
      <button id="api-trigger-btn" class="btn btn-primary" onclick="testApiCall()">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
        {{ site.hero.cta_primary }}
      </button>
    </div>
    <div id="api-result" style="margin-top: 16px; font-size: 14px; display: none; padding: 12px; border-radius: 6px; font-weight: 500;" class="animate-fade-in-up"></div>
  </section>

  <section class="widgets-container animate-fade-in-up delay-3">
    <div class="widget connection-tester">
      <div style="padding-bottom: 24px;">
        <h2 style="font-size: 22px; font-weight: 700; margin-bottom: 8px; color: #0F172A;">Ingyenes bemutató és teszt igénylése</h2>
        <p style="font-size: 13px; color: #475569; margin: 0; line-height: 1.5;">Töltse ki az adatokat és azonnal megkapja a 14 napos próba licenckulcsot e-mailben.</p>
      </div>

      <div class="form-group" style="margin-bottom: 16px;">
        <label style="display: block; font-size: 12px; margin-bottom: 6px; font-weight: 600; color: #334155;">Cégnév</label>
        <input type="text" id="company_name" class="form-control" style="width: 100%; padding: 10px 14px; background: #FFFFFF; border: 1px solid #CBD5E1; border-radius: 6px; color: #0F172A; font-size: 14px; transition: all 0.2s;" placeholder="Cég neve">
      </div>
      
      <div class="form-group" style="margin-bottom: 16px;">
        <label style="display: block; font-size: 12px; margin-bottom: 6px; font-weight: 600; color: #334155;">Kapcsolattartó neve</label>
        <input type="text" class="form-control" style="width: 100%; padding: 10px 14px; background: #FFFFFF; border: 1px solid #CBD5E1; border-radius: 6px; color: #0F172A; font-size: 14px; transition: all 0.2s;" placeholder="Teljes név">
      </div>

      <div class="form-group" style="margin-bottom: 16px;">
        <label style="display: block; font-size: 12px; margin-bottom: 6px; font-weight: 600; color: #334155;">Mobiltelefon</label>
        <input type="tel" class="form-control" style="width: 100%; padding: 10px 14px; background: #FFFFFF; border: 1px solid #CBD5E1; border-radius: 6px; color: #0F172A; font-size: 14px; transition: all 0.2s;" placeholder="+36 ...">
      </div>

      <div class="form-group" style="margin-bottom: 16px;">
        <label style="display: block; font-size: 12px; margin-bottom: 6px; font-weight: 600; color: #334155;">E-mail</label>
        <input type="email" class="form-control" style="width: 100%; padding: 10px 14px; background: #FFFFFF; border: 1px solid #CBD5E1; border-radius: 6px; color: #0F172A; font-size: 14px; transition: all 0.2s;" placeholder="email@ceg.hu">
      </div>

      <div class="form-group" style="margin-bottom: 24px;">
        <label style="display: block; font-size: 12px; margin-bottom: 6px; font-weight: 600; color: #334155;">Felhasználók száma</label>
        <input type="number" class="form-control" style="width: 100%; padding: 10px 14px; background: #FFFFFF; border: 1px solid #CBD5E1; border-radius: 6px; color: #0F172A; font-size: 14px; transition: all 0.2s;" placeholder="1" value="1">
      </div>

      <button id="trial-request-btn" class="btn btn-primary" style="width: 100%; justify-content: center; font-weight: 700; padding: 14px; border-radius: 6px; font-size: 15px;" onclick="runConnectionTest()">Próba licenc igénylése</button>
      
      <div style="text-align: center; margin-top: 16px; font-size: 12px; color: #64748B;">
        14 napos ingyenes próba. Nincs elköteleződés.
      </div>
      
      <div id="test-result-wrapper" style="margin-top: 24px; display: none;"></div>
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
