<script lang="ts">
    import FlashCard from "./lib/FlashCard.svelte";

    // Define flash cards data structure
    const flashCards = [
        // Kapitel 2
        //// Lektion 1
        //{ id:  1, question: "das Abitur", answer: "het vwo-eindexamen"},
        //{ id:  2, question: "anfangen", answer: "beginnen"},
        //{ id:  3, question: "aufstehen", answer: "opstaan"},
        //{ id:  4, question: "aufwachen", answer: "wakker worden"},
        //{ id:  5, question: "der Buchstabe", answer: "de letter"},
        //{ id:  6, question: "das Bundesland", answer: "de deelstaat"},
        //{ id:  7, question: "dunkel", answer: "donker"},
        //{ id:  8, question: "entfernt", answer: "vandaan"},
        //{ id:  9, question: "erzählen", answer: "vertellen"},
        //{ id: 10, question: "es gibt", answer: "er is"},
        //{ id: 11, question: "fahren", answer: "rijden"},
        //{ id: 12, question: "fast", answer: "bijna"},
        //{ id: 13, question: "früh", answer: "vroeg"},
        //{ id: 14, question: "hell", answer: "licht"},
        //{ id: 15, question: "meistens", answer: "meestal"},
        //{ id: 16, question: "müde", answer: "moe"},
        //{ id: 17, question: "spät", answer: "laat"},
        //{ id: 18, question: "die Sprache", answer: "de taal"},
        //{ id: 19, question: "trotzdem", answer: "toch"},
        //{ id: 20, question: "die Unterrichtsstunde", answer: "het lesuur"},
        //{ id: 21, question: "wach", answer: "wakker"},
        //{ id: 22, question: "das Zeugnis", answer: "het rapport" },
        //{ id: 23, question: "zum Beispiel", answer: "bijvoorbeeld" },
        //// Lektion 2
        //{ id: 24, question: "ab", answer: "vanaf" },
        //{ id: 25, question: "außer", answer: "behalve" },
        //{ id: 26, question: "danach", answer: "daarna" },
        //{ id: 27, question: "dauern", answer: "duren" },
        //{ id: 28, question: "die Doppelstunde", answer: "het blokuur" },
        //{ id: 29, question: "einmal", answer: "eens" },
        //{ id: 30, question: "endlich", answer: "eindelijk" },
        //{ id: 31, question: "sich freuen auf", answer: "zich verheugen op" },
        //{ id: 32, question: "die Grundschule", answer: "de basisschool" },
        //{ id: 33, question: "das Gymnasium", answer: "het gymnasium" },
        //{ id: 34, question: "die Hauptschule", answer: "het vmbo" },
        //{ id: 35, question: "immer", answer: "altijd" },
        //{ id: 36, question: "der Kalender", answer: "de agenda" },
        //{ id: 37, question: "nervös", answer: "zenuwachtig" },
        //{ id: 38, question: "die Note", answer: "het cijfer" },
        //{ id: 39, question: "die Realschule", answer: "de havo" },
        //{ id: 40, question: "der Stundenplan", answer: "het lesrooster" },
        //{ id: 41, question: "das Thema", answer: "het onderwerp" },
        //{ id: 42, question: "verstehen", answer: "begrijpen" },
        //{ id: 43, question: "die Wirtschaft", answer: "de economie" },
        //{ id: 44, question: "die Zeitung", answer: "de krant" },
        //{ id: 45, question: "zuerst", answer: "eerst" },
        //// Lektion 3
        //{ id: 46, question: "der Klassenlehrer", answer: "de mentor" },
        //{ id: 47, question: "die Klassenlehrerin", answer: "de mentrix" },
        //{ id: 48, question: "das Lieblingsfach", answer: "het lievelingsvak" },
        //// Schoolvakken
        //{ id: 49, question: "Chemie", answer: "scheikunde" },
        //{ id: 50, question: "Deutsch", answer: "Duits" },
        //{ id: 51, question: "Englisch", answer: "Engels" },
        //{ id: 52, question: "Erdkunde", answer: "aardrijkskunde" },
        //{ id: 53, question: "Französisch", answer: "Frans" },
        //{ id: 54, question: "Geschichte", answer: "geschiedenis" },
        //{ id: 55, question: "Griechisch", answer: "Grieks" },
        //{ id: 56, question: "Latein", answer: "Latijn" },
        //{ id: 57, question: "Mathematik", answer: "wiskunde" },
        //{ id: 58, question: "Physik", answer: "natuurkunde" },
        //{ id: 59, question: "Religion", answer: "godsdienst" },
        //{ id: 60, question: "Sport", answer: "lichamelijke opvoeding" },
        //// Schoolspullen
        //{ id: 61, question: "der Bleistift", answer: "het potlood" },
        //{ id: 62, question: "das Buch", answer: "het boek" },
        //{ id: 63, question: "das Etui", answer: "de etui" },
        //{ id: 64, question: "das Heft", answer: "het schrift" },
        //{ id: 65, question: "der Kugelschreiber", answer: "de balpen" },
        //{ id: 66, question: "der Rucksack", answer: "de rugzak" },
        //{ id: 67, question: "die Schere", answer: "de schaar" },
        //{ id: 68, question: "die Tasche", answer: "de tas" },
        //// Eigenschappen
        //{ id: 69, question: "anstrengend", answer: "vermoeiend" },
        //{ id: 70, question: "blöd", answer: "stom" },
        //{ id: 71, question: "einfach", answer: "makkelijk" },
        //{ id: 72, question: "freundlich", answer: "vriendelijk" },
        //{ id: 73, question: "langweilig", answer: "saai" },
        // Die Farben
        //{ id: 99, question: "blau", answer: "blauw" },
        //{ id: 100, question: "bunt", answer: "veelkleurig" },
        //{ id: 101, question: "dunkelblau", answer: "donkerblauw" },
        //{ id: 102, question: "gelb", answer: "geel" },
        //{ id: 103, question: "grau", answer: "grijs" },
        //{ id: 104, question: "grün", answer: "groen" },
        //{ id: 105, question: "hellgrün", answer: "lichtgroen" },
        //{ id: 106, question: "orange", answer: "oranje" },
        //{ id: 107, question: "rosa", answer: "roze" },
        //{ id: 108, question: "rot", answer: "rood" },
        //{ id: 109, question: "schwarz", answer: "zwart" },
        //{ id: 110, question: "türkis", answer: "turquoise" },
        //{ id: 111, question: "violett", answer: "paars" },
        //{ id: 112, question: "weiß", answer: "wit" },
        //// Die Wochentage
        //{ id: 113, question: "der Montag", answer: "maandag" },
        //{ id: 114, question: "der Dienstag", answer: "dinsdag" },
        //{ id: 115, question: "der Mittwoch", answer: "woensdag" },
        //{ id: 116, question: "der Donnerstag", answer: "donderdag" },
        //{ id: 117, question: "der Freitag", answer: "vrijdag" },
        //{ id: 118, question: "der Samstag", answer: "zaterdag" },
        //{ id: 119, question: "der Sonntag", answer: "zondag" },
        //{ id: 120, question: "das Wochenende", answer: "het weekeinde" },
        //// Die Ordinalzahlen
        //{ id: 121, question: "erste", answer: "eerste" },
        //{ id: 122, question: "zweite", answer: "tweede" },
        //{ id: 123, question: "dritte", answer: "derde" },
        //{ id: 124, question: "vierte", answer: "vierde" },
        //{ id: 125, question: "fünfte", answer: "vijfde" },
        //{ id: 126, question: "sechste", answer: "zesde" },
        //{ id: 127, question: "siebte", answer: "zevende" },
        //{ id: 128, question: "achte", answer: "achtste" },
        //{ id: 129, question: "neunte", answer: "negende" },
        //{ id: 130, question: "zehnte", answer: "tiende" },
        //{ id: 131, question: "elfte", answer: "elfde" },
        //{ id: 132, question: "zwölfte", answer: "twaalfde" },
        //{ id: 133, question: "dreizehnte", answer: "dertiende" },
        //{ id: 134, question: "vierzehnte", answer: "veertiende" },
        //{ id: 135, question: "fünfzehnte", answer: "vijftiende" },
        //{ id: 136, question: "siebzehnte", answer: "zeventiende" },
        //{ id: 137, question: "achtzehnte", answer: "achttiende" },
        //{ id: 138, question: "neunzehnte", answer: "negentiende" },
        //{ id: 139, question: "zwanzigste", answer: "twintigste" },
        //// Lektion 4
        //{ id: 140, question: "abhängig", answer: "afhankelijk" },
        //{ id: 141, question: "bekommen", answer: "krijgen" },
        //{ id: 142, question: "besitzen", answer: "bezitten" },
        //{ id: 143, question: "die Brücke", answer: "de brug" },
        //{ id: 144, question: "denn", answer: "want" },
        //{ id: 145, question: "das Dorf", answer: "het dorp" },
        //{ id: 146, question: "der Einwohner", answer: "de inwoner" },
        //{ id: 147, question: "die Einwohnerin", answer: "de inwoonster" },
        //{ id: 148, question: "der Fluss", answer: "de rivier" },
        //{ id: 149, question: "früher", answer: "vroeger" },
        //{ id: 150, question: "die Großstadt", answer: "de grote stad" },
        //{ id: 151, question: "das Holz", answer: "het hout" },
        //{ id: 152, question: "die Kleinstadt", answer: "de kleine stad" },
        //{ id: 153, question: "mieten", answer: "huren" },
        //{ id: 154, question: "oft", answer: "vaak" },
        //{ id: 155, question: "der Ort", answer: "de plaats" },
        //{ id: 156, question: "der Raum", answer: "de ruimte" },
        //{ id: 157, question: "seit", answer: "sinds" },
        //{ id: 158, question: "das Tor", answer: "de poort" },
        //{ id: 159, question: "träumen", answer: "dromen" },
        //{ id: 160, question: "der Turm", answer: "de toren" },
        //{ id: 161, question: "die Umgebung", answer: "de omgeving" },
        //{ id: 162, question: "unter", answer: "onder" },
        //{ id: 163, question: "verschieden", answer: "verschillend" },
        //{ id: 164, question: "verwenden", answer: "gebruiken" },
        // Lektion 5
        //{ id: 165, question: "auch", answer: "ook" },
        //{ id: 166, question: "der Aufzug", answer: "de lift" },
        //{ id: 167, question: "brauchen", answer: "nodig hebben" },
        //{ id: 168, question: "dürfen", answer: "mogen" },
        //{ id: 169, question: "die Entschuldigung", answer: "het excuus" },
        //{ id: 170, question: "die Farbe", answer: "de kleur" },
        //{ id: 171, question: "das Fenster", answer: "het raam" },
        //{ id: 172, question: "das Geschäft", answer: "de winkel" },
        //{ id: 173, question: "gleich", answer: "zo" },
        //{ id: 174, question: "man", answer: "men" },
        //{ id: 175, question: "mögen", answer: "houden van" },
        //{ id: 176, question: "der Nachbar", answer: "de buurman" },
        //{ id: 177, question: "die Nachbarin", answer: "de buurvrouw" },
        //{ id: 178, question: "schlau", answer: "slim" },
        //{ id: 179, question: "schrecklich", answer: "verschrikkelijk" },
        //{ id: 180, question: "der Schreibtisch", answer: "het bureau" },
        //{ id: 181, question: "später", answer: "later" },
        //{ id: 182, question: "stolz", answer: "trots" },
        //{ id: 183, question: "süß", answer: "lief" },
        //{ id: 184, question: "vielleicht", answer: "misschien" },
        //{ id: 185, question: "die Wand", answer: "de wand" },
        //{ id: 186, question: "weit", answer: "ver" },
        //{ id: 187, question: "das Wohnviertel", answer: "de woonwijk" },
        // Kapitel 3
        // Lektion 3
        //{ id: 188, question: "badmintonnen", answer: "Badminton spielen" },
        //{ id: 189, question: "schaatsen", answer: "eislaufen" },
        //{ id: 190, question: "fietsen", answer: "Fahrrad fahren" },
        //{ id: 191, question: "voetballen", answer: "Fußball spielen" },
        //{ id: 192, question: "hockeyen", answer: "Hockey spielen" },
        //{ id: 193, question: "naar de sportschool gaan", answer: "ins Fitnessstudio gehen" },
        //{ id: 194, question: "hardlopen", answer: "joggen" },
        //{ id: 195, question: "judoën", answer: "Judo machen" },
        //{ id: 196, question: "klimmen", answer: "klettern" },
        //{ id: 197, question: "aan atletiek doen", answer: "Leichtathletik machen" },
        //{ id: 198, question: "aan scouting doen", answer: "Pfadfinder sein" },
        //{ id: 199, question: "paardrijden", answer: "reiten" },
        //{ id: 200, question: "roeien", answer: "rudern" },
        //{ id: 201, question: "schaken", answer: "Schach spielen" },
        //{ id: 202, question: "zwemmen", answer: "schwimmen" },
        //{ id: 203, question: "zeilen", answer: "segeln" },
        //{ id: 204, question: "skaten", answer: "skaten" },
        //{ id: 205, question: "skiën", answer: "Ski fahren" },
        //{ id: 206, question: "dansen", answer: "tanzen" },
        //{ id: 207, question: "tennissen", answer: "Tennis spielen" },
        //{ id: 208, question: "de wedstrijd", answer: "der Wettbewerb" },
        //{ id: 209, question: "de wedstrijd (balsporten)", answer: "das Spiel" },
        // Frequentie
        //{ id: 210, question: "drie keer per week", answer: "dreimal pro Woche" },
        //{ id: 211, question: "één keer per dag", answer: "einmal pro Tag" },
        //{ id: 212, question: "dagelijks", answer: "täglich" },
        //{ id: 213, question: "meestal", answer: "meistens" },
        //{ id: 214, question: "nooit", answer: "nie" },
        //{ id: 215, question: "vaak", answer: "oft" },
        //{ id: 216, question: "sinds één jaar", answer: "seit einem Jahr" },
        //{ id: 217, question: "sinds twee jaar", answer: "seit zwei Jahren" },
        //{ id: 218, question: "twee keer per maand", answer: "zweimal pro Monat" },
        // Kapitel 5
        // duits - nederlands
        //{ id: 219, question: "der Aufzug | die Aufzüge", answer: "de lift" },
        //{ id: 220, question: "die Badewanne | die Badewannen", answer: "de badkuip" },
        //{ id: 221, question: "barrierefrei", answer: "rolstoeltoegankelijk" },
        //{ id: 222, question: "die Couch | die Couchen", answer: "de bank" },
        //{ id: 223, question: "das Doppelbett | die Doppelbetten", answer: "het tweepersoonsbed" },
        //{ id: 224, question: "draußen", answer: "buiten" },
        //{ id: 225, question: "einladen", answer: "uitnodigen" },
        //{ id: 226, question: "das Erdgeschoss | die Erdgeschosse", answer: "de begane grond" },
        //{ id: 227, question: "das Etagenbett | die Etagenbetten", answer: "het stapelbed" },
        //{ id: 228, question: "die Ferienwohnung | die Ferienwohnungen", answer: "de vakantiewoning" },
        //{ id: 229, question: "geräumig", answer: "ruim" },
        //{ id: 230, question: "die Geschwister", answer: "broers en zussen" },
        //{ id: 231, question: "klar", answer: "natuurlijk" },
        //{ id: 232, question: "der Krach", answer: "de ruzie" },
        //{ id: 233, question: "das Mehrfamilienhaus | die Mehrfamilienhäuser", answer: "het appartementencomplex" },
        //{ id: 234, question: "das Obergeschoss | die Obergeschosse", answer: "de bovenverdieping" },
        //{ id: 235, question: "plaudern", answer: "kletsen" },
        //{ id: 236, question: "der Quadratmeter | die Quadratmeter", answer: "de vierkante meter" },
        //{ id: 237, question: "riesig", answer: "reusachtig" },
        //{ id: 238, question: "der Stock", answer: "de verdieping" },
        //{ id: 239, question: "tauschen", answer: "ruilen" },
        //{ id: 240, question: "verfügen über", answer: "beschikken over" },
        //{ id: 241, question: "sich verstehen", answer: "met elkaar overweg kunnen" },
        //// nederlands - duits
        //{ id: 242, question: "de lift", answer: "der Aufzug" },
        //{ id: 243, question: "de badkuip", answer: "die Badewanne" },
        //{ id: 244, question: "rolstoeltoegankelijk", answer: "barrierefrei" },
        //{ id: 245, question: "de bank", answer: "die Couch | die Couchen" },
        //{ id: 246, question: "het tweepersoonsbed", answer: "das Doppelbett" },
        //{ id: 247, question: "buiten", answer: "draussen" },
        //{ id: 248, question: "uitnodigen", answer: "einladen" },
        //{ id: 249, question: "de begane grond", answer: "das Erdgeschoss" },
        //{ id: 250, question: "het stapelbed", answer: "das Etagenbett" },
        //{ id: 251, question: "de vakantiewoning", answer: "die Ferienwohnung" },
        //{ id: 252, question: "ruim", answer: "geraumig" },
        //{ id: 253, question: "broers en zussen", answer: "die Geschwister" },
        //{ id: 254, question: "natuurlijk", answer: "klar" },
        //{ id: 255, question: "de ruzie", answer: "der Krach" },
        //{ id: 256, question: "het appartementencomplex", answer: "das Mehrfamilienhaus" },
        //{ id: 257, question: "de bovenverdieping", answer: "das Obergeschoss" },
        //{ id: 258, question: "kletsen", answer: "plaudern" },
        //{ id: 259, question: "de vierkante meter", answer: "der Quadratmeter" },
        //{ id: 260, question: "reusachtig", answer: "riesig" },
        //{ id: 261, question: "de verdieping", answer: "der Stock" },
        //{ id: 262, question: "ruilen", answer: "tauschen" },
        //{ id: 263, question: "beschikken over", answer: "verfugen uber" },
        //{ id: 264, question: "met elkaar overweg kunnen", answer: "sich verstehen" },

        // Kaptiel 4
        // Lektion 6
        { id: 265, question: "der Becher Joghurt", answer: "de beker yoghurt" },
        { id: 266, question: "das Brot", answer: "het brood" },
        { id: 267, question: "das Brötchen", answer: "het broodje" },
        { id: 268, question: "die Butter", answer: "de boter" },
        { id: 269, question: "das Ei", answer: "het ei" },
        { id: 270, question: "die Erdnussbutter", answer: "de pindakaas" },
        { id: 271, question: "frühstücken", answer: "ontbijten" },
        { id: 272, question: "das Glas Saft", answer: "het glas sap" },
        { id: 273, question: "der Honig", answer: "de honing" },
        { id: 274, question: "der Käse", answer: "de kaas" },
        { id: 275, question: "die Marmelade", answer: "de jam" },
        { id: 276, question: "die Milch", answer: "de melk" },
        { id: 277, question: "der Pfannkuchen", answer: "de pannenkoek" },
        { id: 278, question: "das Schälchen Müsli", answer: "het kommetje muesli" },
        { id: 279, question: "der Schinken", answer: "de ham" },
        { id: 280, question: "die Schokoladencreme", answer: "de chocoladepasta" },
        { id: 281, question: "die Schokostreusel", answer: "de hagelslag" },
        { id: 282, question: "die Tasse Kakao", answer: "de kop chocolademelk" },
        { id: 283, question: "der Tee", answer: "de thee" },
        { id: 284, question: "die Wurst", answer: "de worst" },
        //// Nederlands - Duits
        //{ id: 285, question: "de beker yoghurt", answer: "der Becher Joghurt" },
        //{ id: 286, question: "het brood", answer: "das Brot" },
        //{ id: 287, question: "het broodje", answer: "das Brötchen" },
        //{ id: 288, question: "de boter", answer: "die Butter" },
        //{ id: 289, question: "het ei", answer: "das Ei" },
        //{ id: 290, question: "de pindakaas", answer: "die Erdnussbutter" },
        //{ id: 291, question: "ontbijten", answer: "frühstücken" },
        //{ id: 292, question: "het glas sap", answer: "das Glas Saft" },
        //{ id: 293, question: "de honing", answer: "der Honig" },
        //{ id: 294, question: "de kaas", answer: "der Käse" },
        //{ id: 295, question: "de jam", answer: "die Marmelade" },
        //{ id: 296, question: "de melk", answer: "die Milch" },
        //{ id: 297, question: "de pannenkoek", answer: "der Pfannkuchen" },
        //{ id: 298, question: "het kommetje muesli", answer: "das Schälchen Müsli" },
        //{ id: 299, question: "de ham", answer: "der Schinken" },
        //{ id: 300, question: "de chocoladepasta", answer: "die Schokoladencreme" },
        //{ id: 301, question: "de hagelslag", answer: "die Schokostreusel" },
        //{ id: 302, question: "de kop chocolademelk", answer: "die Tasse Kakao" },
        //{ id: 303, question: "de thee", answer: "der Tee" },
        //{ id: 304, question: "de worst", answer: "die Wurst" },

        //// Lektion 5
        //{ id: 305, question: "beliebt", answer: "populair" },
        //{ id: 306, question: "die Birne", answer: "de peer" },
        //{ id: 307, question: "brauchen", answer: "nodig hebben" },
        //{ id: 308, question: "daheim", answer: "thuis" },
        //{ id: 309, question: "die Ernährung", answer: "de voeding" },
        //{ id: 310, question: "erwarten", answer: "verwachten" },
        //{ id: 311, question: "der Garten", answer: "de tuin" },
        //{ id: 312, question: "das Geheimnis", answer: "het geheim" },
        //{ id: 313, question: "der Geschmack", answer: "de smaak" },
        //{ id: 314, question: "die Kirsche", answer: "de kers" },
        //{ id: 315, question: "leer", answer: "leeg" },
        //{ id: 316, question: "leicht", answer: "makkelijk" },
        //{ id: 317, question: "manchmal", answer: "soms" },
        //{ id: 318, question: "die Mandarine", answer: "de mandarijn" },
        //{ id: 319, question: "das Mehl", answer: "de bloem" },
        //{ id: 320, question: "niemals", answer: "nooit" },
        //{ id: 321, question: "die Pflanze", answer: "de plant" },
        //{ id: 322, question: "die Pflaume", answer: "de pruim" },
        //{ id: 323, question: "das Salz", answer: "het zout" },
        //{ id: 324, question: "die Stunde", answer: "het uur" },
        //{ id: 325, question: "der Zucker", answer: "de suiker" },
        //{ id: 326, question: "zunächst", answer: "eerst" },
        //{ id: 327, question: "die Zutat", answer: "het ingrediënt" },
        //// Nederlands - Duits
        //{ id: 328, question: "populair", answer: "beliebt" },
        //{ id: 329, question: "de peer", answer: "die Birne" },
        //{ id: 330, question: "nodig hebben", answer: "brauchen" },
        //{ id: 331, question: "thuis", answer: "daheim" },
        //{ id: 332, question: "de voeding", answer: "die Ernährung" },
        //{ id: 333, question: "verwachten", answer: "erwarten" },
        //{ id: 334, question: "de tuin", answer: "der Garten" },
        //{ id: 335, question: "het geheim", answer: "das Geheimnis" },
        //{ id: 336, question: "de smaak", answer: "der Geschmack" },
        //{ id: 337, question: "de kers", answer: "die Kirsche" },
        //{ id: 338, question: "leeg", answer: "leer" },
        //{ id: 339, question: "makkelijk", answer: "leicht" },
        //{ id: 340, question: "soms", answer: "manchmal" },
        //{ id: 341, question: "de mandarijn", answer: "die Mandarine" },
        //{ id: 342, question: "de bloem", answer: "das Mehl" },
        //{ id: 343, question: "nooit", answer: "niemals" },
        //{ id: 344, question: "de plant", answer: "die Pflanze" },
        //{ id: 345, question: "de pruim", answer: "die Pflaume" },
        //{ id: 346, question: "het zout", answer: "das Salz" },
        //{ id: 347, question: "het uur", answer: "die Stunde" },
        //{ id: 348, question: "de suiker", answer: "der Zucker" },
        //{ id: 349, question: "eerst", answer: "zunächst" },
        //{ id: 350, question: "het ingrediënt", answer: "die Zutat" },

        //// Lektion 4
        //{ id: 351, question: "die Auswahl", answer: "de keuze" },
        //{ id: 352, question: "benutzen", answer: "gebruiken" },
        //{ id: 353, question: "deshalb", answer: "daarom" },
        //{ id: 354, question: "das Ergebnis", answer: "het resultaat" },
        //{ id: 355, question: "gegen", answer: "tegen" },
        //{ id: 356, question: "das Gemüse", answer: "de groente" },
        //{ id: 357, question: "genau", answer: "precies" },
        //{ id: 358, question: "gespannt sein auf", answer: "nieuwsgierig zijn naar" },
        //{ id: 359, question: "günstig", answer: "voordelig" },
        //{ id: 360, question: "haltbar", answer: "houdbaar" },
        //{ id: 361, question: "irgendwann", answer: "ergens" },
        //{ id: 362, question: "die Karotte", answer: "de wortel" },
        //{ id: 363, question: "die Kräuter", answer: "de kruiden" },
        //{ id: 364, question: "der Laden", answer: "de winkel" },
        //{ id: 365, question: "der Mülleimer", answer: "de vuilnisbak" },
        //{ id: 366, question: "die Nuss", answer: "de noot" },
        //{ id: 367, question: "das Obst", answer: "het fruit" },
        //{ id: 368, question: "sondern", answer: "maar" },
        //{ id: 369, question: "überrascht sein", answer: "verrast zijn" },
        //{ id: 370, question: "die Umwelt", answer: "het milieu" },
        //{ id: 371, question: "verschwenden", answer: "verspillen" },
        //{ id: 372, question: "wegwerfen", answer: "weggooien" },
        //{ id: 373, question: "zubereiten", answer: "bereiden" },
        //// Nederlands - Duits
        //{ id: 374, question: "de keuze", answer: "die Auswahl" },
        //{ id: 375, question: "gebruiken", answer: "benutzen" },
        //{ id: 376, question: "daarom", answer: "deshalb" },
        //{ id: 377, question: "het resultaat", answer: "das Ergebnis" },
        //{ id: 378, question: "tegen", answer: "gegen" },
        //{ id: 379, question: "de groente", answer: "das Gemüse" },
        //{ id: 380, question: "precies", answer: "genau" },
        //{ id: 381, question: "nieuwsgierig zijn naar", answer: "gespannt sein auf" },
        //{ id: 382, question: "voordelig", answer: "günstig" },
        //{ id: 383, question: "houdbaar", answer: "haltbar" },
        //{ id: 384, question: "ergens", answer: "irgendwann" },
        //{ id: 385, question: "de wortel", answer: "die Karotte" },
        //{ id: 386, question: "de kruiden", answer: "die Kräuter" },
        //{ id: 387, question: "de winkel", answer: "der Laden" },
        //{ id: 388, question: "de vuilnisbak", answer: "der Mülleimer" },
        //{ id: 389, question: "de noot", answer: "die Nuss" },
        //{ id: 390, question: "het fruit", answer: "das Obst" },
        //{ id: 391, question: "maar", answer: "sondern" },
        //{ id: 392, question: "verrast zijn", answer: "überrascht sein" },
        //{ id: 393, question: "het milieu", answer: "die Umwelt" },
        //{ id: 394, question: "verspillen", answer: "verschwenden" },
        //{ id: 395, question: "weggooien", answer: "wegwerfen" },
        //{ id: 396, question: "bereiden", answer: "zubereiten" },

        ];


    // Create a shuffled version of the flashcards
    let shuffledCards = [];

    // Fisher-Yates shuffle algorithm function
    function shuffleArray(array: any) {
        // Create a copy of the original array to avoid modifying it
        const arrayCopy = [...array];
        // Start from the last element and swap it with a randomly selected element
        for (let i = arrayCopy.length - 1; i > 0; i--) {
            // Pick a random index from 0 to i
            const j = Math.floor(Math.random() * (i + 1));
            // Swap elements at i and j
            [arrayCopy[i], arrayCopy[j]] = [arrayCopy[j], arrayCopy[i]];
        }
        return arrayCopy;
    }

    // Initialize shuffled cards when component loads
    shuffledCards = shuffleArray(flashCards);

    // Keep track of the current card index
    let currentCardIndex = 0;

    // State for tracking points system
    let points = 0;
    let attempted = 0;

    // Function to go to the next card
    // Function to go to the next card
    function nextCard() {
        if (currentCardIndex < shuffledCards.length - 1) {
            currentCardIndex++;
        }
    }

    // Function to go to the previous card
    function prevCard() {
        if (currentCardIndex > 0) {
            currentCardIndex--;
        }
    }
    // Function to update points when an answer is submitted
    function handleAnswerSubmit(event: any) {
        const isCorrect = event.detail.isCorrect;
        attempted++;

        if (isCorrect) {
            points++; // Add 1 point for correct answer

            // Set a 2-second delay for correct answers before moving to the next card
            if (currentCardIndex < shuffledCards.length - 1) {
                setTimeout(() => {
                    nextCard();
                }, 2000);
            }
        } else {
            // No point deduction for incorrect answers

            // Set a 5-second delay for incorrect answers before moving to the next card
            if (currentCardIndex < shuffledCards.length - 1) {
                setTimeout(() => {
                    nextCard();
                }, 5000);
            }
        }
    }
</script>

<main>
    <div class="container">
        <h1>Flash Cards Duits</h1>

        <div class="score-container">
            <p>Points: {points} (Attempted: {attempted})</p>
        </div>

        <div class="card-container">
            <FlashCard
                flashCard={shuffledCards[currentCardIndex]}
                on:answerSubmitted={handleAnswerSubmit}
            />
        </div>

        <div class="navigation">
            <button on:click={prevCard} disabled={currentCardIndex === 0}
                >Previous</button
            >
            <span class="card-counter"
                >{currentCardIndex + 1} / {shuffledCards.length}</span
            >
            <button
                on:click={nextCard}
                disabled={currentCardIndex === shuffledCards.length - 1}
                >Next</button
            >
        </div>
    </div>
</main>

<style>
    :global(body) {
        background-color: #10abb4;
        color: #004c50;
        margin: 0;
        padding: 0;
        font-family:
            -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen-Sans,
            Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
    }

    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
        max-width: 800px;
        margin: 0 auto;
        padding: 20px;
        background-color: white;
        border-radius: 12px;
        box-shadow: 0 4px 12px rgba(0, 76, 80, 0.1);
    }

    h1 {
        color: #004c50;
        margin-bottom: 20px;
        font-weight: 700;
        text-align: center;
    }

    .score-container {
        margin-bottom: 20px;
        font-size: 1.2rem;
        font-weight: bold;
        color: #004c50;
        background-color: rgba(16, 171, 180, 0.1);
        padding: 8px 16px;
        border-radius: 8px;
    }

    .card-container {
        width: 100%;
        margin-bottom: 20px;
    }

    .navigation {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        max-width: 400px;
        padding: 10px;
        background-color: rgba(0, 147, 156, 0.05);
        border-radius: 8px;
    }

    button {
        background-color: #00939c;
        color: white;
        border: none;
        padding: 10px 20px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 4px 2px;
        cursor: pointer;
        border-radius: 4px;
        transition: all 0.3s ease;
        font-weight: 500;
        box-shadow: 0 2px 4px rgba(0, 76, 80, 0.2);
    }

    button:hover {
        background-color: #10abb4;
        transform: translateY(-2px);
        box-shadow: 0 4px 8px rgba(0, 76, 80, 0.3);
    }

    button:disabled {
        background-color: rgba(0, 147, 156, 0.3);
        cursor: not-allowed;
        box-shadow: none;
        transform: none;
    }

    .card-counter {
        font-size: 1rem;
        color: #502000;
        font-weight: 600;
        background-color: rgba(156, 62, 0, 0.1);
        padding: 4px 10px;
        border-radius: 4px;
    }
</style>
