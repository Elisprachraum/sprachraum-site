<template lang="pug">
.bg-body.text-body.font-body.bg-white
  //- HEADER
  header.fixed.container.w-full.top-0.bg-white.border-b-2.border-gray-300.shadow-xs(style="max-width:100vw")
    .container.mx-auto.w-full.text-center
      nav(class="flex flex-wrap items-center justify-between bg-white w-full pb-4")
        div(class="flex flex-shrink-0 mr-6")
          g-link(to="/")
            g-image(src="~/assets/images/LogoAlphaLineDeKlein.png" class="hidden sm:block")
            g-image(src="~/assets/images/LogoAlphaLineDeKlein.png" width="320" class="visible sm:hidden")
        div(class="hidden lg:hidden")
            <button class="navbar-burger flex items-center py-2 px-3 text-black rounded border border-black"><svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"></path></svg></button>
        div(class="navbar-menu hidden lg:flex lg:flex-grow lg:items-center w-full lg:w-auto")
            div(class="lg:ml-auto")
              g-link(to="/Team/"  class="block lg:inline-block mt-4 lg:mt-0 mr-10 text-secondary-900 hover:text-secondary-700") Team
            //-     a(href="#" class="block lg:inline-block mt-4 lg:mt-0 mr-10 text-secondary-900 hover:text-secondary-700") Deutschkurse
            //-     a(href="#" class="block lg:inline-block mt-4 lg:mt-0 mr-10 text-secondary-900 hover:text-secondary-700") Italienschkurse
            div
              g-link(to="/Kursprogramm/" class="inline-block py-3 px-5 mr-4 leading-none text-center text-gray-700 bg-primary-100 hover:bg-primary-200 rounded shadow") Kursprogramm
              a(href="mailto:post@workitaut.at?subject=Kursanmeldung&body=KURSTITEL /  CORSO %0A %0A %0AVORNAME / NOME%0A  %0ANACHNAME / COGNOME%0A  %0AGEBURTSDATUM / DATA DI NASCITA%0A  %0ASTRASSE / VIA%0A   %0APLZ / CODICE POSTALE%0A %0AORT / CITÀ%0A %0ALAND / PAESE%0A  %0ATELEFON / TELEFONO%0A %0AE-MAIL%0A %0A%0ANACHRICHT / MESSAGO%0A%0A%0A%0A%0A%0A%0A%0A [X]  Ich bestätige, dass ich die Allgemeinen Geschäftsbedingungen WorkITAUT (AGB) zur Kenntnis genommen habe." class="inline-block py-3 px-6 mt-4 lg:mt-0 leading-none text-black bg-primary-500 hover:bg-primary-600 rounded shadow") Anmelden
                //- a(href="mailto:post@workitaut.at?subject=Kursanmeldung" class="inline-block py-3 px-6 mt-4 lg:mt-0 leading-none text-black bg-primary-500 hover:bg-primary-600 rounded shadow") Anmelden
  //- CONTENT
  section.mx-auto.border-none.shadow-none(class="container")
    div(class="mt-24 md:mt-32 mx-0 sm:mx-2 lg:mx-16")
      div(class="visible sm:hidden mx-2 ")
        g-link(to="/kursprogramm/" class="text-center inline-block mb-3 py-3 px-6 w-full leading-none text-black bg-primary-500 hover:bg-primary-600 rounded shadow") Kursprogramm
        g-link(to="/team/" class="text-center inline-block mb-3 py-3 px-6 w-full leading-none text-black bg-secondary-500 hover:bg-seondary-600 rounded shadow") Team
        g-link(to="/" class="text-center inline-block mb-3 py-3 px-6 w-full leading-none text-black bg-primary-500 hover:bg-primary-600 rounded shadow") Startseite
      slot
  //- FOOTER
  footer(class="flex flex-wrap items-center pb-4 px-4 mt-16 border-t")
    .container.w-full.bottom-0.py-4.bg-white(style="max-width:100vw")
      .container.mx-auto.w-full.text-center
        div(class="w-full lg:w-1/5 text-center lg:text-left")
            a(class="text-xl text-primary-500 font-semibold" href="#")
                g-image(src="~/assets/images/LogoAlphaFull.png" alt="SPRACHRAUM.workitaut.at" width="100")
        div(class="w-full lg:w-4/5 mt-4 lg:mt-0 text-center")
            a SPRACHRAUM.workitaut.at
            a(class="inline-block mx-4 mb-4 lg:mb-0  hover:text-primary-700" href="#") Kontakt
            a(class="inline-block mx-4 mb-4 lg:mb-0  hover:text-primary-700" href="#") Work IT AUT
            a(class="inline-block mx-4 hover:text-primary-700" href="#") Impressum
            a(class="inline-block mx-4 hover:text-primary-700" href="#") AGB

</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
@import url('https://fonts.googleapis.com/css2?family=Unica+One&display=swap');
.navigation-font {
  font-family: 'Unica One', Arial, Helvetica, sans-serif;
  font-weight: 400;
  font-size: 18px;
  letter-spacing: 2px;
  font-style: normal;
  line-height: 3.5em;
}
bodydebug {
  @apply bg-red-600;
}
.content-font {
  font-family: D-DIN, DIN, Arial, Helvetica, sans-serif;
  font-weight: 400;
  letter-spacing: 0px;
  font-style: normal;
}

h4 {
  font-family: 'Unica One', Arial, Helvetica, sans-serif;
  font-weight: 400;
  letter-spacing: 0px;
  font-style: normal;
  font-weight: bold;
}

body {
  margin: 0;
  padding: 0;
  line-height: 1.5;
}
</style>
