---
layout: page
title: "{{ site.data.site.setup.page_title }}"
description: "{{ site.data.site.setup.intro }}"
---

<div style="margin-bottom: 40px; display: inline-block; background: var(--color-surface); padding: 5px 15px; border-radius: 20px; font-size: 0.9rem; font-weight: 500; color: var(--color-primary);">
  ⏱️ {{ site.data.site.setup.time_estimate }}
</div>

## Előfeltételek

<div class="prereq-grid">
  <div class="prereq-card">
    <div class="prereq-icon">🤖</div>
    <div class="prereq-content">
      <h4>Claude AI fiók</h4>
      <p>Pro vagy Team előfizetés ajánlott a Custom Connectors használatához.</p>
    </div>
  </div>
  <div class="prereq-card">
    <div class="prereq-icon">👤</div>
    <div class="prereq-content">
      <h4>vtigerCRM hozzáférés</h4>
      <p>Adminisztrátori vagy API-hozzáféréssel rendelkező felhasználói fiók.</p>
    </div>
  </div>
  <div class="prereq-card">
    <div class="prereq-icon">🌐</div>
    <div class="prereq-content">
      <h4>vtigerCRM URL</h4>
      <p>A webcím, ahol a CRM elérhető (pl. https://crm.cegem.hu).</p>
    </div>
  </div>
  <div class="prereq-card">
    <div class="prereq-icon">🔑</div>
    <div class="prereq-content">
      <h4>AccessKey</h4>
      <p>A vtigerCRM felhasználói beállításaiban (My Preferences) található kulcs.</p>
    </div>
  </div>
</div>

## Lépésről lépésre

{% capture step1_body %}
Másold ki az alábbi MCP szerver URL-t. Ezt kell majd megadnod a Claude AI-ban.
{% endcapture %}
{% include step.html number="1" title="MCP szerver URL másolása" body=step1_body code=site.product.mcp_server_url %}

{% capture step2_body %}
Nyisd meg a Claude AI beállításait, és adj hozzá egy új Custom Connectort. Használd a "vtigerCRM" nevet, és illeszd be az előbb kimásolt URL-t.
<br><br>
<a href="{{ site.product.claude_connector_url }}" target="_blank" class="btn btn-secondary">Claude Connector megnyitása ↗</a>
{% endcapture %}
{% include step.html number="2" title="Connector hozzáadása Claude AI-ban" body=step2_body %}

{% capture step3_body %}
Kattints a Connect gombra a Claude-ban, és add meg a hitelesítő adataidat:
<ul>
  <li><strong>vtigerCRM URL:</strong> A rendszered elérhetősége (pl. <code>https://crm.cegem.hu</code>).</li>
  <li><strong>Felhasználónév (Username):</strong> Amivel be szoktál jelentkezni.</li>
  <li><strong>AccessKey:</strong> Lépj be a vtigerCRM-be &rarr; Jobb felső sarok (Profil ikon) &rarr; My Preferences &rarr; Görgess le az Access Key mezőhöz és másold ki.</li>
</ul>
{% endcapture %}
{% include step.html number="3" title="Connect gomb és adatok megadása" body=step3_body %}

{% capture step4_body %}
Sikeres csatlakozás után azonnal elkezdhetsz parancsokat adni a Claude-nak. Próbáld ki ezeket:
<ul>
  <li><em>"Listázd ki a legutóbbi 5 nyitott jegyet (Tickets)."</em></li>
  <li><em>"Készíts egy új kontaktot: Kovács János, info@kovacs.hu, +36301234567."</em></li>
  <li><em>"Keresd meg a 'Nagy Projekt' nevű ügyletet (Deals) és írd le az állapotát."</em></li>
  <li><em>"Módosítsd a 12x45 azonosítójú rekord státuszát 'Closed'-ra."</em></li>
  <li><em>"Futtass egy VQL lekérdezést: SELECT * FROM Contacts LIMIT 3;"</em></li>
</ul>
{% endcapture %}
{% include step.html number="4" title="Kész! Kezdj el parancsokat írni" body=step4_body %}

---

<div class="faq">
  <h2>Gyakori kérdések (FAQ)</h2>
  {% for item in site.data.site.faq %}
  <details>
    <summary>{{ item.q }}</summary>
    <div class="faq-answer">{{ item.a }}</div>
  </details>
  {% endfor %}
</div>

<div style="margin-top: 60px; text-align: center; background: var(--color-surface); padding: 40px; border-radius: var(--border-radius);">
  <h3>Elakadtál?</h3>
  <p style="color: var(--color-muted); margin-bottom: 20px;">Írj nekünk, és segítünk a beállításban.</p>
  <a href="mailto:{{ site.provider.email }}" class="btn btn-primary">Kapcsolatfelvétel</a>
</div>
