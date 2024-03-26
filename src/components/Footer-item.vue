<script setup></script>

<template>
  <footer>
    <div class="footer-name">
      <img class="footer-logo" src="/src/icons/AIrones_logo_white.png" alt="Company Logo" />
      <span class="footer-company-name">AIrones s.r.o</span>
    </div>
    <div class="footer-details">
      <div class="footer-details-item footer-main-text">
        <div class="footer-details-links-item">
          <img
            class="footer-details-socials-icon"
            src="/src/icons/Footer/linkedin.png"
            alt="LinkedIn"
          />
          <div>Docs</div>
        </div>
        <div class="footer-details-links-item">GitHub</div>
        <div class="footer-details-links-item">ContactUs</div>
      </div>
      <div class="footer-details-item footer-main-text">
        <b>Address</b>
        <div class="footer-details-adress-info">
          Mikovíniho 217/4<br />Trnava 917 01<br />Slovakia, European Union
        </div>
      </div>
      <div class="footer-details-item footer-main-text">
        <b>Socials</b>
        <div class="footer-details-socials-icons">
          <img
            class="footer-details-socials-icon"
            src="/src/icons/Footer/linkedin.png"
            alt="LinkedIn"
          />
          <img
            class="footer-details-socials-icon"
            src="/src/icons/Footer/youtube.png"
            alt="YouTube"
          />
        </div>
      </div>
      <div class="footer-details-item footer-main-text">
        <b>Email</b>
        <div class="footer-details-email-info">info@airvolute.com</div>
      </div>
      <div class="footer-details-item footer-main-text">
        <b>More information</b>
        <div class="footer-details-information-info">
          <b>Company ID</b> 53229649<br />
          <b>Tax ID</b> 2121308519<br />
          <b>VAT ID</b> SK2121308519<br />
          <b>IBAN</b> SK34 8330 0000 0020 0186 1813<br />
          <b>BIC/SWIFT</b> FIOZSKBAXXX<br />
          <b>Bank</b> Fio Banka
        </div>
      </div>
    </div>
  </footer>
</template>

<style>
footer {
  background: #121212;
  display: flex;
  align-items: start;
  flex-direction: column;
  padding-left: 7%;
  padding-right: 7%;
  padding-top: 65px;
  gap: 50px;
}
.footer-main-text {
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}
b {
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
}
.footer-name {
  display: inline-flex;
  justify-content: space-between;
  align-items: center;
  gap: 16px;
}
.footer-logo {
  min-width: 32px;
  width: 2.2%;
  height: auto;
  margin-left: 6.6%;
}
.footer-company-name {
  color: #000;
  font-family: 'Michroma', sans-serif;
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  width: auto;
  margin-right: 64px;
  white-space: nowrap;
  color: #ffffff;
}
.footer-details {
  display: flex;
  flex-direction: row;
  gap: 88px; /*chanche on %*/
  padding-right: 108px;
  padding-left: 144px;
}
.footer-details-item {
  display: flex;
  flex-direction: column;
  gap: 15px;
}
</style>
