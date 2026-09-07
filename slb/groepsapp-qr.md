---
marp: true
size: 16:9
paginate: false
title: WhatsApp-groep
description: QR-sheet met korte groepsinformatie en afspraken
---

<style>
section {
  box-sizing: border-box;
  width: 1280px;
  height: 720px;
  padding: 52px 64px;
  overflow: hidden;
  position: relative;
  background: #f6f1e7;
  color: #151515;
  font-family: "Aptos", "Inter", "Segoe UI", Arial, sans-serif;
  letter-spacing: 0;
}

section::before {
  content: "";
  position: absolute;
  inset: 0;
  z-index: 0;
  background:
    linear-gradient(90deg, transparent 0 58px, #151515 58px 68px, transparent 68px 100%),
    linear-gradient(90deg, transparent 0 286px, #151515 286px 296px, transparent 296px 100%),
    linear-gradient(90deg, transparent 0 905px, #151515 905px 915px, transparent 915px 100%),
    linear-gradient(0deg, transparent 0 92px, #151515 92px 102px, transparent 102px 100%),
    linear-gradient(0deg, transparent 0 604px, #151515 604px 614px, transparent 614px 100%);
  opacity: 0.13;
}

.sheet {
  position: relative;
  z-index: 1;
  display: grid;
  grid-template-columns: 1fr 360px;
  gap: 56px;
  height: 100%;
  align-items: center;
}

.content {
  padding: 18px 0 34px 38px;
}

.label {
  display: inline-block;
  margin-bottom: 28px;
  padding: 8px 12px;
  border: 3px solid #151515;
  background: #ffffff;
  font-size: 17px;
  font-weight: 800;
  text-transform: uppercase;
}

h1 {
  margin: 0 0 18px;
  max-width: 650px;
  font-size: 66px;
  font-weight: 850;
  line-height: 0.96;
}

.intro {
  max-width: 610px;
  margin: 0 0 28px;
  font-size: 27px;
  font-weight: 600;
  line-height: 1.28;
}

.rules {
  display: grid;
  gap: 11px;
  max-width: 665px;
  margin: 0;
  padding: 0;
  list-style: none;
}

.rule {
  display: grid;
  grid-template-columns: 44px 1fr;
  align-items: center;
  min-height: 50px;
  border: 3px solid #151515;
  background: #ffffff;
  box-shadow: 6px 6px 0 #151515;
  font-size: 21px;
  font-weight: 720;
}

.rule span {
  display: grid;
  height: 100%;
  place-items: center;
  border-right: 3px solid #151515;
  font-weight: 900;
}

.rule strong {
  color: #245aa8;
}

.rule div {
  padding: 10px 17px;
}

.qr-panel {
  display: grid;
  justify-items: center;
  gap: 18px;
  padding: 26px 24px 22px;
  border: 5px solid #151515;
  background: #ffffff;
  box-shadow: 12px 12px 0 #151515;
}

.qr-panel img {
  width: 288px;
  height: 288px;
  object-fit: contain;
  image-rendering: pixelated;
}

.qr-title {
  font-size: 23px;
  font-weight: 850;
}

.qr-note {
  max-width: 260px;
  margin: 0;
  color: #424242;
  font-size: 17px;
  font-weight: 600;
  line-height: 1.25;
  text-align: center;
}

.footer {
  position: absolute;
  right: 64px;
  bottom: 24px;
  z-index: 2;
  color: #151515;
  font-size: 13px;
  font-weight: 800;
  text-transform: uppercase;
}

.block {
  position: absolute;
  z-index: 0;
  border: 5px solid #151515;
}

.block-red-top {
  top: 0;
  left: 0;
  width: 255px;
  height: 82px;
  background: #e23d2f;
}

.block-yellow-left {
  left: 0;
  bottom: 0;
  width: 92px;
  height: 240px;
  background: #f2c335;
}

.block-blue-bottom {
  left: 92px;
  bottom: 0;
  width: 205px;
  height: 88px;
  background: #245aa8;
}

.block-yellow-top {
  top: 0;
  right: 0;
  width: 350px;
  height: 92px;
  background: #f2c335;
}

.block-red-bottom {
  right: 0;
  bottom: 0;
  width: 365px;
  height: 106px;
  background: #e23d2f;
}
</style>

<div class="block block-red-top"></div>
<div class="block block-yellow-left"></div>
<div class="block block-blue-bottom"></div>
<div class="block block-yellow-top"></div>
<div class="block block-red-bottom"></div>
<div class="sheet"><div class="content"><div class="label">WhatsApp-groep</div><h1>Samen op de hoogte.</h1><p class="intro">Deze groep is bedoeld om belangrijke informatie, updates en korte vragen met elkaar te delen.</p><div class="rules"><div class="rule"><span>1</span><div><strong>Informatie delen</strong> staat centraal.</div></div><div class="rule"><span>2</span><div>Houd berichten kort, duidelijk en relevant.</div></div><div class="rule"><span>3</span><div>Geen uitbundig chatten of losse gesprekken.</div></div><div class="rule"><span>4</span><div>Reageer alleen als het nuttig is voor de groep.</div></div></div></div><div class="qr-panel"><img src="../assets/wa QR.png" alt="QR-code voor de WhatsApp-groep"><div class="qr-title">Scan om mee te doen</div><p class="qr-note">Gebruik de groep rustig en praktisch.</p></div></div>
<div class="footer">ROC Mondriaan / informatiegroep</div>
