Load
=======================

I denna studie ska jag välja ut tre webbsidor och från dem ta fram deras prestanda och laddningstid, samt analysera och jämföra resultaten.

Urval
-----------------------

Jag har valt hemsidorna arbetsförmedlingen.se, amazon.se och dn.se. Jag har försökt att välja lite olika typer av hemsidor, olika typer av ändamål och innehåll. Det är intressant att se hur olika typer av innehåll kan påverka olika faktorer.

Metod
-----------------------

Jag har använt mig av pagespeed.web.dev/ som tar fram betyg på prestanda, tillgänglighet, bästa metoder och SEO samt data om hur laddningstider och liknade har upplevts av faktiska användare. Jag har även använt mig av chromes devtools för att ta fram sidans laddningstid, hur många resurser som laddas in och hur mycket plats resurserna tar.

Resultat
-----------------------

### Arbetsförmedlingen.se

![arbetsformedlingen](../image/load-analysis/arbetsformedlingen-example.webp "Arbetsförmedlingen") {.websiteImg}

_Data_

<iframe class="sheet"  overflow="hidden" scrolling="no" frameBorder="0" width="100%" style="overflow:hidden;border:0;" border="0" height="100%" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRa-irgYWhsTE2lyHPhyPaUhsnbxqZMscWrQIHuXnTv1_1984nYFGcDH5Wj42IfaB3tEvOvNWg9UEkb/pubhtml?gid=0&amp;single=true&amp;widget=false&amp;headers=false&amp;chrome=false&amp;rm=minimal;frameborder=0"></iframe>

_Sammanfattning_

Enligt resultatet så ser man att sidans startsida och om sida fungerar bra på de flesta punkter men skulle dock behövas förbättras med den mobila prestandan. Förslag som ges av pagespeed är bland annat att modernisera bilder, reducera oanvänd css och skjuta up inläsningar av resurser som inte behövs vid första renderingen.

Platsbanken verkar ha mer problem, sämre mobil prestanda där det även ges förslag att undvika större layoutförskjutningar och även problem med Core Test Vitals; INP och CLS. Dessa hade förbättrats med att öka prestandan genom de givna förslagen samt återigen undvika större layoutförskjutningar.


### Amazon.se

![amazon](../image/load-analysis/amazon-example.webp "Amazon") {.websiteImg}

_Data_

<iframe class="sheet"  overflow="hidden" scrolling="no" frameBorder="0" width="100%" style="overflow:hidden;border:0;" border="0" height="100%" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRa-irgYWhsTE2lyHPhyPaUhsnbxqZMscWrQIHuXnTv1_1984nYFGcDH5Wj42IfaB3tEvOvNWg9UEkb/pubhtml?gid=1145729094&amp;single=true&amp;widget=false&amp;headers=false&amp;chrome=false&amp;rm=minimal;frameborder=0"></iframe>

_Sammanfattning_

Sidans startsidan har även här problem med den mobila prestandan med några förslag som reducera oanvänd css, skjuta up inläsningar av resurser som inte behövs vid första renderingen och skjuta upp inläsning av bilder som inte visas på skärmen. De kan även förbättra den mobila tillgängligheten genom att förbättra länkbeskrivningarna och alt beskrivningen till bilder för att underlätta och minska förvirring för personer som använder skärmuppläsare. Även de mobila Bästa Metoder kan bli bättre genom att göra bildernas faktiska mått proportionerliga mot skärmstorleken och pixelmåttet samt matcha bildens visningsformat med det naturliga bildformatet. 

Sidan bestsellers har likande problem med den mobila och dator prestandan och den mobila och dator tillgängligheten. De kan även förbättra SEO:n genom att se till att alla bild-element har ett alt attribut och se till att länkarna är genomsökningsbara.

Mest problem har sidan aboutamazon.eu. Både på mobilen och datorn har den problem med prestandan och tillgänglighet, mest prestanda problem har den på mobilen där förslagen bland annat är att minska LCP, alltså inläsningen av det största elementet, och använda bilder med rätt storlek. För att förbättra tillgängligheten så kan de bland annat förbättra hur listorna läses upp genom att endast ha li element i listor. Om de förbättrar prestanda borde även FCP och TTFB förbättras.


### Dn.se

![dn](../image/load-analysis/dn-example.webp "DN") {.websiteImg}

_Data_

<iframe class="sheet"  overflow="hidden" scrolling="no" frameBorder="0" width="100%" style="overflow:hidden;border:0;" border="0" height="100%" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRa-irgYWhsTE2lyHPhyPaUhsnbxqZMscWrQIHuXnTv1_1984nYFGcDH5Wj42IfaB3tEvOvNWg9UEkb/pubhtml?gid=932734691&amp;single=true&amp;widget=false&amp;headers=false&amp;chrome=false&amp;rm=minimal;frameborder=0"></iframe>

_Sammanfattning_

Denna hemsidan har inte så mycket problem, den mobila prestandan hade kunnat förbättras på alla undersökta sidor. För startsidan ges bland annat förslagen förbättra det största elementets inläsningstid och reducera JavaScript osm inte används. Kultur och korsordssidorna får även förslagen att minska påverkan från tredjepartskod och reducera css som inte används. Alla sidor, speciellt korsordssidan, bör förbättra datorns prestanda genom att undvika större layoutförskjutningar.


Analys
-----------------------

Enligt resultatet jag har fått fram verkar det vara mest saker att åtgärder med prestandan samt att det verkar vara mer problem med mobilversionen än datorversionen. Förslag som många sidor fick var bland annat att förbättra det största elementets inläsningstid, förbättra moderniteten av bilder och skjuta up inläsningar av resurser som inte behövs vid första renderingen. För de sidor som hade problem emd tillgängligheten var ofta förslagen att alla länkar ska ha passande beskrivningar som inte är upprepande av tidigare text och att alla bilder ska ha ett beskrivande alt-attribut.

De sidor jag har valt har mycket data i sig, speciellt Amazon. De sidor som har mer resurser kan man se generellt tar mer laddningstid. 

Min ragnordig av sidorna ser ut såhär:

1. dn.se
2. arbetsformedlingen.se
3. amazon.se

Av alla tre sidorna har dn.se best betyg av prestanda, tillgänglighet, bästa metoder och SEO och snabbast inläsningstid jämfört med resursernas storlek. Även om de flesta av sidornas Core Web Vitals testerna inte blev godkända så var det inte mycket över gränsen fel. De andra sidorna var mer lika men resultaten visar att arbetsförmedlingen var snäppet bättre i testerna samt att amazons startsida hade den långsammaste inläsningstiden.

Jag tycker att runt tre sekunders inläsningstid max verkar rimligt för att vara en snabb webbsida, dock är nog det viktigaste hur det upplevs av användaren. Om man ser till att allt som visas above the fold laddas in snabbt så kanske det inte gör jättemycket för användaren att saker längst ner på sidan läses in några sekunder senare. Men jag tror det är viktigt att tänka på de som kanske har lite sämre uppkoppling då någon sekund extra kan bli flera sekunder extra, och det finns nog en hel del användare i den kategorin som man vill ska stanna på hemsidan.

Enligt resultatet så är det endast två av alla hemsidornas sidor som är under tre sekunder. Jag tror dock att på de hemsidor som användaren vet har mycket att läsa in, som till exempel amazon, kan användarna nog ha lite mer förståelse för än sidor som känns om att det ska kunna läsas in på direkten. Jag upplevde själv inte att sidorna kändes sega när jag gick in på dem, men några av sidorna kan absolut förbättras för att optimera användarutlevelsen. 

Referenser
-----------------------

[arbetsformedlingen.se](https://arbetsformedlingen.se/)

[amazon.se](https://amazon.se)

[dn.se](https://dn.se)

[pagespeed.web.dev](https://pagespeed.web.dev/)

Övrigt
-----------------------

Skriven av Rebecka Corell.