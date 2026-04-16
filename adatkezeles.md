---
layout: page
title: "Adatkezelési Tájékoztató"
description: "Hatályos: {{ 'now' | date: '%Y. %m. %d.' }}"
---

A **{{ site.provider.name }}** (a továbbiakban: **Adatkezelő**) elkötelezett a felhasználók személyes adatainak védelme iránt. Jelen tájékoztató célja, hogy bemutassa, hogyan kezeljük a **{{ site.product.name }}** szolgáltatás használata során felmerülő adatokat, az Európai Unió Általános Adatvédelmi Rendeletének (GDPR) megfelelően.

## 1. Az Adatkezelő adatai

*   Név: {{ site.provider.name }}
*   Székhely: {{ site.provider.address }}
*   Adószám: {{ site.provider.tax_id }}
*   E-mail: [{{ site.provider.email }}](mailto:{{ site.provider.email }})

## 2. Milyen adatokat kezelünk?

A {{ site.product.name }} egy közvetítő (proxy) szolgáltatás a Claude AI és a Te vtigerCRM rendszered között. A szolgáltatás működéséhez az alábbi adatok áthaladnak a szerverünkön:

*   **vtigerCRM URL:** A rendszered elérhetősége.
*   **Felhasználónév (Username):** A vtigerCRM bejelentkezési neved.
*   **AccessKey:** A vtigerCRM API hozzáférési kulcsod.
*   **Kérések és válaszok tartalma:** A Claude AI által küldött lekérdezések (pl. VQL) és a vtigerCRM által visszaadott adatok (pl. kontaktok, ügyletek adatai).

**FONTOS:** Ezeket az adatokat **NEM TÁROLJUK** tartósan semmilyen adatbázisban vagy naplófájlban. Az adatok kizárólag a szerver memóriájában léteznek az adott kérés (request) feldolgozásának idejéig (általában néhány másodperc), majd azonnal törlődnek.

## 3. Az adatkezelés célja és jogalapja

*   **Cél:** A szolgáltatás (MCP protokollon keresztüli kommunikáció a Claude AI és a vtigerCRM között) biztosítása.
*   **Jogalap:** A szerződés teljesítése (GDPR 6. cikk (1) bekezdés b) pont), amelyet a szolgáltatás használatának megkezdésével (az ÁSZF elfogadásával) kötsz velünk.

## 4. Adattovábbítás

A szolgáltatás jellegéből adódóan az adatok az alábbi harmadik felek között áramlanak:
*   **Anthropic (Claude AI):** A Te kéréseid innen érkeznek, és a válaszokat ide továbbítjuk.
*   **A Te vtigerCRM rendszered:** A kéréseket ide továbbítjuk, és az adatokat innen kapjuk.

A szerverünk (amely az adatokat átmenetileg feldolgozza) az Európai Unió területén található (pl. Frankfurt, Németország).

## 5. Sütik (Cookies)

Ez a weboldal (a beállítási útmutató és a dokumentáció) egy statikus oldal (Jekyll). **Nem használunk semmilyen nyomkövető (tracking), analitikai vagy marketing sütit.**

A "Kapcsolat tesztelése" oldal kizárólag a böngésző memóriáját használja a teszt futtatásához, adatokat nem ment a gépedre.

## 6. Az érintettek jogai

Mivel nem tárolunk rólad személyes adatokat tartósan, a hagyományos adatvédelmi jogok (pl. törléshez való jog, adathordozhatóság) értelmezése korlátozott. Ennek ellenére a GDPR alapján az alábbi jogokkal rendelkezel:

*   **Tájékoztatáshoz és hozzáféréshez való jog:** Kérhetsz tájékoztatást arról, hogy kezelünk-e rólad adatot (a válaszunk az lesz, hogy tartósan nem).
*   **Panasztételhez való jog:** Ha úgy gondolod, hogy az adatkezelésünk sérti a GDPR-t, panaszt tehetsz a Nemzeti Adatvédelmi és Információszabadság Hatóságnál (NAIH) vagy a lakóhelyed szerinti adatvédelmi hatóságnál.

## 7. Kapcsolat

Ha bármilyen kérdésed van az adatkezeléssel kapcsolatban, kérjük, lépj kapcsolatba velünk a [{{ site.provider.email }}](mailto:{{ site.provider.email }}) e-mail címen.
