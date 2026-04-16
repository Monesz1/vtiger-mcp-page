---
layout: page
title: "Általános Szerződési Feltételek"
description: "Hatályos: {{ 'now' | date: '%Y. %m. %d.' }}"
---

## 1. Általános rendelkezések

Jelen Általános Szerződési Feltételek (a továbbiakban: **ÁSZF**) tartalmazzák a **{{ site.provider.name }}** (a továbbiakban: **Szolgáltató**) által üzemeltetett **{{ site.product.name }}** (a továbbiakban: **Szolgáltatás**) használatára vonatkozó feltételeket.

**Szolgáltató adatai:**
*   Név: {{ site.provider.name }}
*   Székhely: {{ site.provider.address }}
*   Adószám: {{ site.provider.tax_id }}
*   E-mail: [{{ site.provider.email }}](mailto:{{ site.provider.email }})
*   Weboldal: [{{ site.provider.website }}]({{ site.provider.website }})

A Szolgáltatás használatával a Felhasználó elfogadja a jelen ÁSZF-ben foglaltakat.

## 2. A szolgáltatás leírása

A {{ site.product.name }} egy Model Context Protocol (MCP) szerver, amely lehetővé teszi a vtigerCRM rendszer összekapcsolását a Claude AI (Anthropic) szolgáltatással. A Szolgáltatás közvetítőként működik a Felhasználó vtigerCRM példánya és a Claude AI között, lehetővé téve a természetes nyelvű adatlekérdezést és módosítást.

A Szolgáltatás használatához a Felhasználónak rendelkeznie kell:
1.  Érvényes vtigerCRM hozzáféréssel (URL, Username, AccessKey).
2.  Claude AI fiókkal (amely támogatja az MCP Custom Connectorokat).

## 3. Regisztráció és hitelesítés

A Szolgáltatás használatához nincs szükség külön regisztrációra a Szolgáltató rendszerében. A hitelesítés közvetlenül a Felhasználó vtigerCRM rendszerével történik a megadott AccessKey használatával.

A Felhasználó felelős a hitelesítő adatai (vtigerCRM URL, Username, AccessKey) biztonságos kezeléséért. A Szolgáltató nem tárolja ezeket az adatokat tartósan; azok kizárólag a memóriában, az adott kérés feldolgozásának idejéig léteznek.

## 4. Díjszabás és fizetés

A Szolgáltatás jelenlegi verziója ingyenesen használható. A Szolgáltató fenntartja a jogot, hogy a jövőben prémium funkciókat vezessen be, amelyek használatát díjfizetéshez kötheti. Erről a Felhasználókat előzetesen tájékoztatja.

## 5. A felhasználó jogai és kötelezettségei

*   A Felhasználó jogosult a Szolgáltatást a jelen ÁSZF-nek megfelelően használni.
*   A Felhasználó köteles gondoskodni arról, hogy a Szolgáltatás használata során ne sértse meg harmadik felek jogait (pl. adatvédelmi előírások).
*   A Felhasználó tudomásul veszi, hogy a Szolgáltatáson keresztül végrehajtott műveletek (pl. adatok módosítása, törlése a vtigerCRM-ben) az ő felelősségére történnek. A Szolgáltató nem vállal felelősséget a Felhasználó által kiadott utasítások következményeiért.
*   Tilos a Szolgáltatás rendeltetésellenes használata, a rendszer túlterhelése, vagy a biztonsági intézkedések megkerülése.

## 6. A szolgáltató jogai és kötelezettségei

*   A Szolgáltató törekszik a Szolgáltatás folyamatos és hibamentes működésének biztosítására, de nem garantálja a 100%-os rendelkezésre állást.
*   A Szolgáltató jogosult a Szolgáltatás karbantartása, frissítése vagy biztonsági okok miatt a Szolgáltatást átmenetileg szüneteltetni.
*   A Szolgáltató fenntartja a jogot a Szolgáltatás funkcióinak módosítására, bővítésére vagy megszüntetésére.

## 7. Felelősségkorlátozás

A Szolgáltató nem vállal felelősséget az alábbiakért:
*   A vtigerCRM API elérhetetlensége, hibái vagy változásai.
*   A Claude AI (Anthropic) szolgáltatás elérhetetlensége, hibái vagy a Custom Connector funkció változásai.
*   A Felhasználó által a Claude AI-nak adott utasítások helyessége és azok következményei a vtigerCRM adatokra nézve.
*   Közvetett, következményes károk, elmaradt haszon, vagy adatvesztés.

A Szolgáltató felelőssége a Szolgáltatás használatával kapcsolatban felmerülő károkért legfeljebb a Felhasználó által a Szolgáltatásért az elmúlt 12 hónapban fizetett díj összegéig terjed (ingyenes használat esetén 0 Ft).

## 8. Adatvédelem

A Szolgáltató a személyes adatokat a vonatkozó jogszabályoknak (GDPR) megfelelően kezeli. A részletes adatkezelési szabályokat az [Adatkezelési Tájékoztató]({{ '/adatkezeles/' | relative_url }}) tartalmazza.

## 9. Szerződés megszüntetése

A Felhasználó bármikor megszüntetheti a Szolgáltatás használatát a Custom Connector eltávolításával a Claude AI beállításaiból.

A Szolgáltató jogosult a Szolgáltatás nyújtását azonnali hatállyal megszüntetni, ha a Felhasználó súlyosan megsérti a jelen ÁSZF rendelkezéseit.

## 10. Vegyes rendelkezések

A jelen ÁSZF-re a magyar jog az irányadó. A felek a vitás kérdéseket elsősorban békés úton kísérlik meg rendezni. Ennek eredménytelensége esetén a jogvita elbírálására a Szolgáltató székhelye szerinti hatáskörrel rendelkező bíróság az illetékes.

A Szolgáltató fenntartja a jogot az ÁSZF egyoldalú módosítására. A módosítások a weboldalon történő közzététellel lépnek hatályba.
