# DRK Blutspende

This component has been created to be used with Home Assistant.

DRK Blutspende allows you to get upcoming dates for blood donation into Home Assistant.

### Data source

The data is fetched from https://www.spenderservice.net/.

**Warning:**
As this is no official API this component can break at any time if they decide to change their website structure.

### Installation:

#### HACS

- Ensure that HACS is installed.
- Search for and install the "DRK Blutspende" integration.
- Restart Home Assistant.

#### Manual installation

- Download the latest release.
- Unpack the release and copy the custom_components/drkblutspende directory into the custom_components directory of your Home Assistant installation.
- Restart Home Assistant.

### Example entry for configuration.yaml

```
- platform: drkblutspende
  zipcode: 79790
  radius: 10
  countyid: "08337"
  lookahead: 14
  timeformat: "%A, %d.%m.%Y"
  zipfilter: 
    - 79790
    - 79801
```

 - `zipcode` is required, this defines the center of the search
 - `radius` is optional, this defines the radius to search within in kilometers
 - `countyid` is optional, limits the results to the selected county (see list below)
 - `lookahead` is optional, defines how far into the future the rsults can be
 - `timeformat` is optional, lets you define how the date and time is formated
 - `zipfilter` is optional, a list of zipcodes that allows you to limit the results to the zipcodes in the list

### County ID lookup table

 - 07131: Ahrweiler
 - 09771: Aichach-Friedberg
 - 08425: Alb-Donau-Kreis
 - 16077: Altenburger Land
 - 07132: Altenkirchen (Westerwald)
 - 15081: Altmarkkreis Salzwedel
 - 09171: Altötting
 - 07331: Alzey-Worms
 - 09361: Amberg (Kreisfreie Stadt)
 - 09371: Amberg-Sulzbach
 - 03451: Ammerland
 - 15082: Anhalt-Bitterfeld
 - 09571: Ansbach
 - 09561: Ansbach (Kreisfreie Stadt)
 - 09671: Aschaffenburg
 - 09661: Aschaffenburg (Kreisfreie Stadt)
 - 09772: Augsburg
 - 09761: Augsburg (Kreisfreie Stadt)
 - 03452: Aurich
 - 07332: Bad Dürkheim
 - 09672: Bad Kissingen
 - 07133: Bad Kreuznach
 - 09173: Bad Tölz-Wolfratshausen
 - 08211: Baden-Baden (Stadtkreis)
 - 09471: Bamberg
 - 09461: Bamberg (Kreisfreie Stadt)
 - 12060: Barnim
 - 14625: Bautzen
 - 09472: Bayreuth
 - 09462: Bayreuth (Kreisfreie Stadt)
 - 09172: Berchtesgadener Land
 - 06431: Bergstraße
 - 11000: Berlin (Kreisfreie Stadt)
 - 07231: Bernkastel-Wittlich
 - 08426: Biberach
 - 05711: Bielefeld (Kreisfreie Stadt)
 - 07134: Birkenfeld
 - 08115: Böblingen
 - 05911: Bochum (Kreisfreie Stadt)
 - 08435: Bodenseekreis
 - 05314: Bonn (Kreisfreie Stadt)
 - 15083: Börde
 - 05554: Borken
 - 05512: Bottrop (Kreisfreie Stadt)
 - 12051: Brandenburg an der Havel (Kreisfreie Stadt)
 - 03101: Braunschweig (Kreisfreie Stadt)
 - 08315: Breisgau-Hochschwarzwald
 - 04011: Bremen (Kreisfreie Stadt)
 - 04012: Bremerhaven (Kreisfreie Stadt)
 - 15084: Burgenlandkreis
 - 08235: Calw
 - 03351: Celle
 - 09372: Cham
 - 14511: Chemnitz (Kreisfreie Stadt)
 - 03453: Cloppenburg
 - 09473: Coburg
 - 09463: Coburg (Kreisfreie Stadt)
 - 07135: Cochem-Zell
 - 05558: Coesfeld
 - 12052: Cottbus (Kreisfreie Stadt)
 - 03352: Cuxhaven
 - 09174: Dachau
 - 12061: Dahme-Spreewald
 - 06411: Darmstadt (Kreisfreie Stadt)
 - 06432: Darmstadt-Dieburg
 - 09271: Deggendorf
 - 03401: Delmenhorst (Kreisfreie Stadt)
 - 15001: Dessau-Roßlau (Kreisfreie Stadt)
 - 03251: Diepholz
 - 09773: Dillingen a.d. Donau
 - 09279: Dingolfing-Landau
 - 01051: Dithmarschen
 - 09779: Donau-Ries
 - 07333: Donnersbergkreis
 - 05913: Dortmund (Kreisfreie Stadt)
 - 14612: Dresden (Kreisfreie Stadt)
 - 05112: Duisburg (Kreisfreie Stadt)
 - 05358: Düren
 - 05111: Düsseldorf (Kreisfreie Stadt)
 - 09175: Ebersberg
 - 16061: Eichsfeld
 - 09176: Eichstätt
 - 07232: Eifelkreis Bitburg-Prüm
 - 16056: Eisenach (Kreisfreie Stadt)
 - 12062: Elbe-Elster
 - 03402: Emden (Kreisfreie Stadt)
 - 08316: Emmendingen
 - 03454: Emsland
 - 05954: Ennepe-Ruhr-Kreis
 - 08236: Enzkreis
 - 09177: Erding
 - 16051: Erfurt (Kreisfreie Stadt)
 - 09562: Erlangen (Kreisfreie Stadt)
 - 09572: Erlangen-Höchstadt
 - 14521: Erzgebirgskreis
 - 05113: Essen (Kreisfreie Stadt)
 - 08116: Esslingen
 - 05366: Euskirchen
 - 01001: Flensburg (Kreisfreie Stadt)
 - 09474: Forchheim
 - 07311: Frankenthal (Pfalz) (Kreisfreie Stadt)
 - 12053: Frankfurt (Oder) (Kreisfreie Stadt)
 - 06412: Frankfurt am Main (Kreisfreie Stadt)
 - 08311: Freiburg im Breisgau (Stadtkreis)
 - 09178: Freising
 - 08237: Freudenstadt
 - 09272: Freyung-Grafenau
 - 03455: Friesland
 - 06631: Fulda
 - 09179: Fürstenfeldbruck
 - 09573: Fürth
 - 09563: Fürth (Kreisfreie Stadt)
 - 09180: Garmisch-Partenkirchen
 - 05513: Gelsenkirchen (Kreisfreie Stadt)
 - 16052: Gera (Kreisfreie Stadt)
 - 07334: Germersheim
 - 06531: Gießen
 - 03151: Gifhorn
 - 08117: Göppingen
 - 14626: Görlitz
 - 03153: Goslar
 - 16067: Gotha
 - 03159: Göttingen
 - 03456: Grafschaft Bentheim
 - 16076: Greiz
 - 06433: Groß-Gerau
 - 09774: Günzburg
 - 05754: Gütersloh
 - 05914: Hagen (Kreisfreie Stadt)
 - 15002: Halle (Saale) (Kreisfreie Stadt)
 - 02000: Hamburg (Kreisfreie Stadt)
 - 03252: Hameln-Pyrmont
 - 05915: Hamm (Kreisfreie Stadt)
 - 03353: Harburg
 - 15085: Harz
 - 09674: Haßberge
 - 12063: Havelland
 - 03358: Heidekreis
 - 08221: Heidelberg (Stadtkreis)
 - 08135: Heidenheim
 - 08125: Heilbronn
 - 08121: Heilbronn (Stadtkreis)
 - 05370: Heinsberg
 - 03154: Helmstedt
 - 05758: Herford
 - 05916: Herne (Kreisfreie Stadt)
 - 06632: Hersfeld-Rotenburg
 - 01053: Herzogtum Lauenburg
 - 16069: Hildburghausen
 - 03254: Hildesheim
 - 05958: Hochsauerlandkreis
 - 06434: Hochtaunuskreis
 - 09475: Hof
 - 09464: Hof (Kreisfreie Stadt)
 - 08126: Hohenlohekreis
 - 03255: Holzminden
 - 05762: Höxter
 - 16070: Ilm-Kreis
 - 09161: Ingolstadt (Kreisfreie Stadt)
 - 16053: Jena (Kreisfreie Stadt)
 - 15086: Jerichower Land
 - 07335: Kaiserslautern
 - 07312: Kaiserslautern (Kreisfreie Stadt)
 - 08215: Karlsruhe
 - 08212: Karlsruhe (Stadtkreis)
 - 06633: Kassel
 - 06611: Kassel (Kreisfreie Stadt)
 - 09762: Kaufbeuren (Kreisfreie Stadt)
 - 09273: Kelheim
 - 09763: Kempten (Allgäu) (Kreisfreie Stadt)
 - 01002: Kiel (Kreisfreie Stadt)
 - 09675: Kitzingen
 - 05154: Kleve
 - 07111: Koblenz (Kreisfreie Stadt)
 - 05315: Köln (Kreisfreie Stadt)
 - 08335: Konstanz
 - 05114: Krefeld (Kreisfreie Stadt)
 - 09476: Kronach
 - 09477: Kulmbach
 - 07336: Kusel
 - 16065: Kyffhäuserkreis
 - 06532: Lahn-Dill-Kreis
 - 07313: Landau in der Pfalz (Kreisfreie Stadt)
 - 09181: Landsberg am Lech
 - 09274: Landshut
 - 09261: Landshut (Kreisfreie Stadt)
 - 03457: Leer
 - 14729: Leipzig
 - 14713: Leipzig (Kreisfreie Stadt)
 - 05316: Leverkusen (Kreisfreie Stadt)
 - 09478: Lichtenfels
 - 06533: Limburg-Weilburg
 - 09776: Lindau (Bodensee)
 - 05766: Lippe
 - 08336: Lörrach
 - 01003: Lübeck (Kreisfreie Stadt)
 - 03354: Lüchow-Dannenberg
 - 08118: Ludwigsburg
 - 07314: Ludwigshafen am Rhein (Kreisfreie Stadt)
 - 13076: Ludwigslust-Parchim
 - 03355: Lüneburg
 - 15003: Magdeburg (Kreisfreie Stadt)
 - 06435: Main-Kinzig-Kreis
 - 09677: Main-Spessart
 - 08128: Main-Tauber-Kreis
 - 06436: Main-Taunus-Kreis
 - 07315: Mainz (Kreisfreie Stadt)
 - 07339: Mainz-Bingen
 - 08222: Mannheim (Stadtkreis)
 - 15087: Mansfeld-Südharz
 - 06534: Marburg-Biedenkopf
 - 12064: Märkisch-Oderland
 - 05962: Märkischer Kreis
 - 07137: Mayen-Koblenz
 - 13071: Mecklenburgische Seenplatte
 - 14627: Meißen
 - 09764: Memmingen (Kreisfreie Stadt)
 - 10042: Merzig-Wadern
 - 05158: Mettmann
 - 09182: Miesbach
 - 09676: Miltenberg
 - 05770: Minden-Lübbecke
 - 14522: Mittelsachsen
 - 05116: Mönchengladbach (Kreisfreie Stadt)
 - 09183: Mühldorf a. Inn
 - 05117: Mülheim an der Ruhr (Kreisfreie Stadt)
 - 09184: München
 - 09162: München (Kreisfreie Stadt)
 - 05515: Münster (Kreisfreie Stadt)
 - 08225: Neckar-Odenwald-Kreis
 - 09775: Neu-Ulm
 - 09185: Neuburg-Schrobenhausen
 - 09373: Neumarkt i.d. OPf.
 - 01004: Neumünster (Kreisfreie Stadt)
 - 10043: Neunkirchen
 - 09575: Neustadt a.d. Aisch-Bad Windsheim
 - 09374: Neustadt a.d. Waldnaab
 - 07316: Neustadt an der Weinstraße (Kreisfreie Stadt)
 - 07138: Neuwied
 - 03256: Nienburg (Weser)
 - 01054: Nordfriesland
 - 16062: Nordhausen
 - 14730: Nordsachsen
 - 13074: Nordwestmecklenburg
 - 03155: Northeim
 - 09564: Nürnberg (Kreisfreie Stadt)
 - 09574: Nürnberger Land
 - 09780: Oberallgäu
 - 05374: Oberbergischer Kreis
 - 05119: Oberhausen (Kreisfreie Stadt)
 - 12065: Oberhavel
 - 12066: Oberspreewald-Lausitz
 - 06437: Odenwaldkreis
 - 12067: Oder-Spree
 - 06438: Offenbach
 - 06413: Offenbach am Main (Kreisfreie Stadt)
 - 03458: Oldenburg
 - 03403: Oldenburg (Oldb) (Kreisfreie Stadt)
 - 05966: Olpe
 - 08317: Ortenaukreis
 - 03459: Osnabrück
 - 03404: Osnabrück (Kreisfreie Stadt)
 - 08136: Ostalbkreis
 - 09777: Ostallgäu
 - 03356: Osterholz
 - 01055: Ostholstein
 - 12068: Ostprignitz-Ruppin
 - 05774: Paderborn
 - 09275: Passau
 - 09262: Passau (Kreisfreie Stadt)
 - 03157: Peine
 - 09186: Pfaffenhofen a.d. Ilm
 - 08231: Pforzheim (Stadtkreis)
 - 01056: Pinneberg
 - 07317: Pirmasens (Kreisfreie Stadt)
 - 01057: Plön
 - 12054: Potsdam (Kreisfreie Stadt)
 - 12069: Potsdam-Mittelmark
 - 12070: Prignitz
 - 08216: Rastatt
 - 08436: Ravensburg
 - 05562: Recklinghausen
 - 09276: Regen
 - 09375: Regensburg
 - 09362: Regensburg (Kreisfreie Stadt)
 - 03241: Region Hannover
 - 10041: Regionalverband Saarbrücken
 - 08119: Rems-Murr-Kreis
 - 05120: Remscheid (Kreisfreie Stadt)
 - 01058: Rendsburg-Eckernförde
 - 08415: Reutlingen
 - 05362: Rhein-Erft-Kreis
 - 07140: Rhein-Hunsrück-Kreis
 - 05162: Rhein-Kreis Neuss
 - 07141: Rhein-Lahn-Kreis
 - 08226: Rhein-Neckar-Kreis
 - 07338: Rhein-Pfalz-Kreis
 - 05382: Rhein-Sieg-Kreis
 - 06439: Rheingau-Taunus-Kreis
 - 05378: Rheinisch-Bergischer Kreis
 - 09673: Rhön-Grabfeld
 - 09187: Rosenheim
 - 09163: Rosenheim (Kreisfreie Stadt)
 - 13072: Rostock
 - 13003: Rostock (Kreisfreie Stadt)
 - 03357: Rotenburg (Wümme)
 - 09576: Roth
 - 09277: Rottal-Inn
 - 08325: Rottweil
 - 16074: Saale-Holzland-Kreis
 - 16075: Saale-Orla-Kreis
 - 15088: Saalekreis
 - 16073: Saalfeld-Rudolstadt
 - 10044: Saarlouis
 - 10045: Saarpfalz-Kreis
 - 14628: Sächsische Schweiz-Osterzgebirge
 - 03102: Salzgitter (Kreisfreie Stadt)
 - 15089: Salzlandkreis
 - 03257: Schaumburg
 - 01059: Schleswig-Flensburg
 - 16066: Schmalkalden-Meiningen
 - 09565: Schwabach (Kreisfreie Stadt)
 - 08127: Schwäbisch Hall
 - 06634: Schwalm-Eder-Kreis
 - 09376: Schwandorf
 - 08326: Schwarzwald-Baar-Kreis
 - 09678: Schweinfurt
 - 09662: Schweinfurt (Kreisfreie Stadt)
 - 13004: Schwerin (Kreisfreie Stadt)
 - 01060: Segeberg
 - 05970: Siegen-Wittgenstein
 - 08437: Sigmaringen
 - 05974: Soest
 - 05122: Solingen (Kreisfreie Stadt)
 - 16068: Sömmerda
 - 16072: Sonneberg
 - 07318: Speyer (Kreisfreie Stadt)
 - 12071: Spree-Neiße
 - 10046: St. Wendel
 - 03359: Stade
 - 05334: Städteregion Aachen
 - 09188: Starnberg
 - 01061: Steinburg
 - 05566: Steinfurt
 - 15090: Stendal
 - 01062: Stormarn
 - 09263: Straubing (Kreisfreie Stadt)
 - 09278: Straubing-Bogen
 - 08111: Stuttgart (Stadtkreis)
 - 07337: Südliche Weinstraße
 - 07340: Südwestpfalz
 - 16054: Suhl (Kreisfreie Stadt)
 - 12072: Teltow-Fläming
 - 09377: Tirschenreuth
 - 09189: Traunstein
 - 07211: Trier (Kreisfreie Stadt)
 - 07235: Trier-Saarburg
 - 08416: Tübingen
 - 08327: Tuttlingen
 - 12073: Uckermark
 - 03360: Uelzen
 - 08421: Ulm (Stadtkreis)
 - 05978: Unna
 - 16064: Unstrut-Hainich-Kreis
 - 09778: Unterallgäu
 - 03460: Vechta
 - 03361: Verden
 - 05166: Viersen
 - 06535: Vogelsbergkreis
 - 14523: Vogtlandkreis
 - 13075: Vorpommern-Greifswald
 - 13073: Vorpommern-Rügen
 - 07233: Vulkaneifel
 - 06635: Waldeck-Frankenberg
 - 08337: Waldshut
 - 05570: Warendorf
 - 16063: Wartburgkreis
 - 09363: Weiden i.d. OPf. (Kreisfreie Stadt)
 - 09190: Weilheim-Schongau
 - 16055: Weimar (Kreisfreie Stadt)
 - 16071: Weimarer Land
 - 09577: Weißenburg-Gunzenhausen
 - 06636: Werra-Meißner-Kreis
 - 05170: Wesel
 - 03461: Wesermarsch
 - 07143: Westerwaldkreis
 - 06440: Wetteraukreis
 - 06414: Wiesbaden (Kreisfreie Stadt)
 - 03405: Wilhelmshaven (Kreisfreie Stadt)
 - 15091: Wittenberg
 - 03462: Wittmund
 - 03158: Wolfenbüttel
 - 03103: Wolfsburg (Kreisfreie Stadt)
 - 07319: Worms (Kreisfreie Stadt)
 - 09479: Wunsiedel i. Fichtelgebirge
 - 05124: Wuppertal (Kreisfreie Stadt)
 - 09679: Würzburg
 - 09663: Würzburg (Kreisfreie Stadt)
 - 08417: Zollernalbkreis
 - 07320: Zweibrücken (Kreisfreie Stadt)
 - 14524: Zwickau

