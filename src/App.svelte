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
        // Lektion 3
        { id: 46, question: "der Klassenlehrer", answer: "de mentor" },
        { id: 47, question: "die Klassenlehrerin", answer: "de mentrix" },
        { id: 48, question: "das Lieblingsfach", answer: "het lievelingsvak" },
        // Schoolvakken
        { id: 49, question: "Chemie", answer: "scheikunde" },
        { id: 50, question: "Deutsch", answer: "Duits" },
        { id: 51, question: "Englisch", answer: "Engels" },
        { id: 52, question: "Erdkunde", answer: "aardrijkskunde" },
        { id: 53, question: "Französisch", answer: "Frans" },
        { id: 54, question: "Geschichte", answer: "geschiedenis" },
        { id: 55, question: "Griechisch", answer: "Grieks" },
        { id: 56, question: "Latein", answer: "Latijn" },
        { id: 57, question: "Mathematik", answer: "wiskunde" },
        { id: 58, question: "Physik", answer: "natuurkunde" },
        { id: 59, question: "Religion", answer: "godsdienst" },
        { id: 60, question: "Sport", answer: "lichamelijke opvoeding" },
        // Schoolspullen
        { id: 61, question: "der Bleistift", answer: "het potlood" },
        { id: 62, question: "das Buch", answer: "het boek" },
        { id: 63, question: "das Etui", answer: "de etui" },
        { id: 64, question: "das Heft", answer: "het schrift" },
        { id: 65, question: "der Kugelschreiber", answer: "de balpen" },
        { id: 66, question: "der Rucksack", answer: "de rugzak" },
        { id: 67, question: "die Schere", answer: "de schaar" },
        { id: 68, question: "die Tasche", answer: "de tas" },
        // Eigenschappen
        { id: 69, question: "anstrengend", answer: "vermoeiend" },
        { id: 70, question: "blöd", answer: "stom" },
        { id: 71, question: "einfach", answer: "makkelijk" },
        { id: 72, question: "freundlich", answer: "vriendelijk" },
        { id: 73, question: "langweilig", answer: "saai" },
        //// Lektion 4
        //{ id: 74, question: "abhängig", answer: "afhankelijk" },
        //{ id: 75, question: "bekommen", answer: "krijgen" },
        //{ id: 76, question: "besitzen", answer: "bezitten" },
        //{ id: 77, question: "die Brücke", answer: "de brug" },
        //{ id: 78, question: "denn", answer: "want" },
        //{ id: 79, question: "das Dorf", answer: "het dorp" },
        //{ id: 80, question: "der Einwohner", answer: "de inwoner" },
        //{ id: 81, question: "die Einwohnerin", answer: "de inwoonster" },
        //{ id: 82, question: "der Fluss", answer: "de rivier" },
        //{ id: 83, question: "früher", answer: "vroeger" },
        //{ id: 84, question: "die Großstadt", answer: "de grote stad" },
        //{ id: 85, question: "das Holz", answer: "het hout" },
        //{ id: 86, question: "die Kleinstadt", answer: "de kleine stad" },
        //{ id: 87, question: "mieten", answer: "huren" },
        //{ id: 88, question: "oft", answer: "vaak" },
        //{ id: 89, question: "der Ort", answer: "de plaats" },
        //{ id: 90, question: "der Raum", answer: "de ruimte" },
        //{ id: 91, question: "seit", answer: "sinds" },
        //{ id: 92, question: "das Tor", answer: "de poort" },
        //{ id: 93, question: "träumen", answer: "dromen" },
        //{ id: 94, question: "der Turm", answer: "de toren" },
        //{ id: 95, question: "die Umgebung", answer: "de omgeving" },
        //{ id: 96, question: "unter", answer: "onder" },
        //{ id: 97, question: "verschieden", answer: "verschillend" },
        //{ id: 98, question: "verwenden", answer: "gebruiken" },
        //// Die Farben
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
