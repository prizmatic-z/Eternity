# Eternity
[System]: If you're here for Dynablocks Cloud, you are not worthy. Virus Noob knows that, he'll just give you what you need for the Cloud.


[A Mysterious Noob]: This is just the beginning.


[A Mysterious Noob]: Talk to Virus Noob to start.


[A Mysterious Noob]: However, to do so, you must prove thyself worthy.


[A Mysterious Noob]: Solve the puzzle...




<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>THE FINAL TRANSMISSION</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    min-height: 100vh;
    background: #080b12;
    color: #55ff99;
    font-family: "Courier New", monospace;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow-x: hidden;
    padding: 25px 0;
}

.screen {
    width: 90%;
    max-width: 850px;
    min-height: 470px;
    border: 2px solid #55ff99;
    padding: 35px;
    background: rgba(0, 15, 10, 0.95);
    box-shadow: 0 0 25px #00ff6650;
    position: relative;
}

.screen::before {
    content: "";
    position: absolute;
    inset: 0;
    pointer-events: none;
    background: repeating-linear-gradient(
        transparent 0px,
        transparent 3px,
        rgba(0, 255, 100, 0.035) 4px
    );
}

h1 {
    text-align: center;
    letter-spacing: 5px;
    font-size: 24px;
    text-shadow: 0 0 12px #55ff99;
}

.subtitle {
    text-align: center;
    color: #888;
    font-size: 12px;
    letter-spacing: 3px;
    margin-bottom: 45px;
}

.decoration {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 25px 0;
    letter-spacing: 3px;
    text-align: center;
}

.output-label {
    color: #aaffcc;
    font-size: 14px;
    margin-bottom: 15px;
}

#output {
    font-size: clamp(15px, 3vw, 25px);
    letter-spacing: 4px;
    word-break: break-all;
    min-height: 45px;
    text-shadow: 0 0 10px #55ff99;
}

.cursor {
    display: inline-block;
    animation: blink 0.8s infinite;
}

@keyframes blink {
    50% {
        opacity: 0;
    }
}

.status {
    margin-top: 35px;
    color: #668877;
    font-size: 12px;
    line-height: 2;
}

.footer {
    position: absolute;
    bottom: 15px;
    right: 20px;
    color: #446655;
    font-size: 10px;
}

button {
    display: block;
    margin: 25px auto 0;
    background: transparent;
    color: #55ff99;
    border: 1px solid #55ff99;
    padding: 12px 25px;
    font-family: inherit;
    cursor: pointer;
    letter-spacing: 3px;
}

button:hover {
    background: #55ff99;
    color: #080b12;
    box-shadow: 0 0 15px #55ff99;
}

button:disabled {
    opacity: 0.4;
    cursor: not-allowed;
}

.divider {
    border: none;
    border-top: 1px solid #28583d;
    margin: 40px 0;
}

.code-section {
    margin-top: 30px;
}

.code-label {
    color: #aaffcc;
    font-size: 14px;
    margin-bottom: 15px;
}

.code-input {
    display: block;
    width: 100%;
    background: #050b08;
    border: 1px solid #34784f;
    color: #55ff99;
    padding: 13px;
    font-family: inherit;
    font-size: 16px;
    letter-spacing: 3px;
    outline: none;
    text-align: center;
    text-transform: uppercase;
}

.code-input:focus {
    border-color: #55ff99;
    box-shadow: 0 0 10px #00ff6650;
}

#codeResult {
    margin-top: 25px;
    color: #aaffcc;
    font-size: 14px;
    line-height: 2;
    min-height: 30px;
    white-space: pre-wrap;
    overflow-wrap: anywhere;
    text-shadow: 0 0 8px #55ff99;
}

.success {
    color: #55ff99;
}

.error {
    color: #bb6655;
}

/* REFLEX PROTOCOL */

#gameSection {
    margin-top: 35px;
}

.game-title {
    text-align: center;
    font-size: 19px;
    letter-spacing: 4px;
    text-shadow: 0 0 10px #55ff99;
}

.game-description {
    color: #668877;
    text-align: center;
    font-size: 12px;
    line-height: 2;
    margin: 20px 0;
}

#gameStatus {
    text-align: center;
    color: #aaffcc;
    font-size: 14px;
    min-height: 45px;
    line-height: 2;
    margin-top: 20px;
}

#gameArena {
    width: 100%;
    max-width: 560px;
    height: 260px;
    margin: 20px auto;
    position: relative;
    border: 1px solid #34784f;
    background-color: #030906;
    background-image:
        linear-gradient(#163322 1px, transparent 1px),
        linear-gradient(90deg, #163322 1px, transparent 1px);
    background-size: 25px 25px;
    overflow: hidden;
    touch-action: manipulation;
    user-select: none;
}

#gameArena.active {
    box-shadow: inset 0 0 15px #00ff6630;
}

#target {
    position: absolute;
    width: 48px;
    height: 48px;
    margin: 0;
    padding: 0;
    border: 2px solid #aaffcc;
    background: #55ff99;
    box-shadow: 0 0 18px #55ff99;
    cursor: crosshair;
    display: none;
    touch-action: manipulation;
}

#target:hover {
    background: #aaffcc;
    box-shadow: 0 0 25px #55ff99;
}

#finalMessage {
    margin-top: 30px;
    color: #55ff99;
    font-size: 14px;
    line-height: 2;
    white-space: pre-wrap;
    overflow-wrap: anywhere;
    text-shadow: 0 0 8px #55ff99;
}

[hidden] {
    display: none !important;
}

@media (max-width: 600px) {
    .screen {
        padding: 20px;
    }

    h1 {
        font-size: 19px;
        letter-spacing: 3px;
    }

    #gameArena {
        height: 230px;
    }
}
</style>
</head>

<body>

<div class="screen">

    <h1>UNKNOWN TRANSMISSION</h1>

    <div class="subtitle">
        RETRO SYSTEM INTERFACE // VERSION 1.09
    </div>

    <div class="decoration">
        CONNECTION ESTABLISHED
    </div>

    <div class="output-label">
        &gt; DECRYPTION SEQUENCE INITIALIZED
    </div>

    <div id="output">
        <span class="cursor">_</span>
    </div>

    <button onclick="beginTransmission()">
        DECRYPT
    </button>

    <div class="status" id="status">
        SYSTEM STATUS: STANDBY<br>
        ENCRYPTED DATA: DETECTED<br>
        WAITING FOR INPUT...
    </div>

    <hr class="divider">

    <div class="code-section">

        <div id="accessEntry">

            <div class="code-label">
                &gt; ENTER ACCESS CODE
            </div>

            <input
                type="text"
                id="codeInput"
                class="code-input"
                placeholder="AWAITING INPUT..."
                autocomplete="off"
                spellcheck="false"
            >

            <button onclick="checkCode()">
                SUBMIT CODE
            </button>

        </div>

        <div id="codeResult"></div>

        <div id="gameSection" hidden>

            <div class="game-title">
                REFLEX PROTOCOL
            </div>

            <div class="game-description">
                SYSTEM TEST INITIATED.<br>
                WAIT FOR THE TARGET TO APPEAR.<br>
                CLICK IT AS QUICKLY AS POSSIBLE.<br><br>
                8 SUCCESSFUL HITS REQUIRED.<br>
                PREMATURE INPUT WILL RESULT IN FAILURE.
            </div>

            <div id="gameStatus">
                AWAITING INITIALIZATION...
            </div>

            <div id="gameArena">
                <button id="target" aria-label="Hit target"></button>
            </div>

            <button id="startGame" onclick="startChallenge()">
                START CHALLENGE
            </button>

            <div id="finalMessage"></div>

        </div>

    </div>

    <div class="footer">
        END OF TRANSMISSION // 199X
    </div>

</div>

<script>

// ORIGINAL DECRYPTION SYSTEM

const secretKey = "YXPXDHJQAKAMKKEKSDCQIB";
const typingSpeed = 180;

let currentIndex = 0;
let running = false;

const output = document.getElementById("output");
const status = document.getElementById("status");

function beginTransmission() {
    if (running) return;

    running = true;
    currentIndex = 0;
    output.innerHTML = "";

    status.innerHTML =
        "SYSTEM STATUS: PROCESSING<br>" +
        "DECRYPTION: IN PROGRESS<br>" +
        "PLEASE WAIT...";

    typeNextCharacter();
}

function typeNextCharacter() {
    if (currentIndex < secretKey.length) {
        output.textContent += secretKey[currentIndex];
        currentIndex++;

        const delay = typingSpeed + Math.random() * 100;
        setTimeout(typeNextCharacter, delay);
    } else {
        finishTransmission();
    }
}

function finishTransmission() {
    output.innerHTML += '<span class="cursor">_</span>';

    status.innerHTML =
        "SYSTEM STATUS: COMPLETE<br>" +
        "DECRYPTION: SUCCESSFUL<br>" +
        "TRANSMISSION RECEIVED.";

    running = false;
}


// ACCESS CODE VERIFICATION

const expectedHash =
    "0e3e4bc001b272e0fba13cbbd4d28408997834c0d3fc91e0ff37ac1ca15fe515";

async function hashCode(value) {
    const data = new TextEncoder().encode(value);
    const hashBuffer = await crypto.subtle.digest("SHA-256", data);

    return Array.from(new Uint8Array(hashBuffer))
        .map(byte => byte.toString(16).padStart(2, "0"))
        .join("");
}

async function checkCode() {
    const input = document.getElementById("codeInput");
    const result = document.getElementById("codeResult");
    const enteredCode = input.value.trim().toUpperCase();

    result.className = "";
    result.textContent = "VERIFYING ACCESS...";

    if (!enteredCode) {
        result.className = "error";
        result.textContent = "ERROR: NO INPUT DETECTED.";
        return;
    }

    try {
        const enteredHash = await hashCode(enteredCode);

        if (enteredHash === expectedHash) {
            document.getElementById("accessEntry").hidden = true;

            result.className = "success";
            result.textContent =
                "ACCESS GRANTED.\nINITIALIZING REFLEX PROTOCOL...";

            document.getElementById("gameSection").hidden = false;

            document.getElementById("gameStatus").textContent =
                "SYSTEM READY. AWAITING PLAYER.";
        } else {
            result.className = "error";
            result.textContent =
                "ACCESS DENIED.\nINVALID CODE. TRY AGAIN.";
        }
    } catch (error) {
        result.className = "error";
        result.textContent =
            "SYSTEM ERROR: CRYPTOGRAPHIC MODULE UNAVAILABLE.";
    }
}


// REFLEX PROTOCOL

const TOTAL_ROUNDS = 8;
const MOBILE_REACTION_LIMIT = 500;
const PC_REACTION_LIMIT = 750;
const MIN_WAIT = 1000;
const MAX_WAIT = 2600;

let currentRound = 0;
let gameRunning = false;
let targetVisible = false;
let targetStartTime = 0;
let activeReactionLimit = PC_REACTION_LIMIT;
let waitTimer = null;
let targetTimer = null;

const arena = document.getElementById("gameArena");
const target = document.getElementById("target");
const gameStatus = document.getElementById("gameStatus");
const startButton = document.getElementById("startGame");

function getReactionLimit() {
    return window.matchMedia("(pointer: coarse)").matches
        ? MOBILE_REACTION_LIMIT
        : PC_REACTION_LIMIT;
}

function startChallenge() {
    clearTimeout(waitTimer);
    clearTimeout(targetTimer);

    currentRound = 0;
    gameRunning = true;
    targetVisible = false;
    target.style.display = "none";
    startButton.hidden = true;
    arena.classList.add("active");
    document.getElementById("finalMessage").textContent = "";

    gameStatus.textContent =
        "ROUND 1 / " + TOTAL_ROUNDS + "\nWAIT FOR THE TARGET...";

    scheduleTarget();
}

function scheduleTarget() {
    if (!gameRunning) return;

    targetVisible = false;
    target.style.display = "none";

    const delay = MIN_WAIT + Math.random() * (MAX_WAIT - MIN_WAIT);
    waitTimer = setTimeout(showTarget, delay);
}

function showTarget() {
    if (!gameRunning) return;

    /*
     * Keep a 20px margin inside the arena, then choose a random
     * position only within that smaller area.
     */
    const inset = 20;
    const targetSize = target.offsetWidth;

    const maxX = Math.max(
        inset,
        arena.clientWidth - targetSize - inset
    );

    const maxY = Math.max(
        inset,
        arena.clientHeight - targetSize - inset
    );

    const x = inset + Math.random() * Math.max(0, maxX - inset);
    const y = inset + Math.random() * Math.max(0, maxY - inset);

    target.style.left = x + "px";
    target.style.top = y + "px";
    target.style.display = "block";

    targetVisible = true;
    targetStartTime = performance.now();
    activeReactionLimit = getReactionLimit();

    gameStatus.textContent =
        "ROUND " + (currentRound + 1) + " / " + TOTAL_ROUNDS +
        "\nTARGET DETECTED. CLICK NOW!";

    targetTimer = setTimeout(() => {
        if (targetVisible && gameRunning) {
            failChallenge("REACTION TIME EXCEEDED.");
        }
    }, activeReactionLimit);
}


// Detect pointer input inside the arena.
// Clicking too early or missing the target causes failure.

arena.addEventListener("pointerdown", function(event) {
    if (!gameRunning) return;

    event.preventDefault();

    if (!targetVisible) {
        failChallenge("PREMATURE INPUT DETECTED.");
        return;
    }

    if (!event.target.closest("#target")) {
        failChallenge("TARGET MISSED.");
        return;
    }

    const reactionTime = performance.now() - targetStartTime;

    if (reactionTime > activeReactionLimit) {
        failChallenge("REACTION TIME EXCEEDED.");
        return;
    }

    clearTimeout(targetTimer);

    targetVisible = false;
    target.style.display = "none";
    currentRound++;

    if (currentRound >= TOTAL_ROUNDS) {
        completeChallenge();
        return;
    }

    gameStatus.textContent =
        "TARGET CONFIRMED.\nPREPARING ROUND " +
        (currentRound + 1) + " / " + TOTAL_ROUNDS + "...";

    waitTimer = setTimeout(scheduleTarget, 450);
});

function failChallenge(reason) {
    if (!gameRunning) return;

    gameRunning = false;
    targetVisible = false;

    clearTimeout(waitTimer);
    clearTimeout(targetTimer);

    target.style.display = "none";
    arena.classList.remove("active");

    gameStatus.textContent =
        "PROTOCOL FAILED.\n" + reason;

    startButton.textContent = "RETRY PROTOCOL";
    startButton.hidden = false;
}

function completeChallenge() {
    gameRunning = false;
    targetVisible = false;

    clearTimeout(waitTimer);
    clearTimeout(targetTimer);

    target.style.display = "none";
    arena.classList.remove("active");
    startButton.hidden = true;

    gameStatus.textContent =
        "ALL 8 TARGETS CONFIRMED.\nREFLEX PROTOCOL: COMPLETE.";

    revealFinalMessage();
}


// HIDDEN FINAL MESSAGE

const encodedMessage = "E3EnPSNoHzArE2c7ICZ0Bg==";
const decodingKey = "R3tro!Key";

function decodeMessage(encoded, key) {
    const binary = atob(encoded);
    const keyBytes = new TextEncoder().encode(key);
    const decodedBytes = new Uint8Array(binary.length);

    for (let i = 0; i < binary.length; i++) {
        decodedBytes[i] =
            binary.charCodeAt(i) ^
            keyBytes[i % keyBytes.length];
    }

    return new TextDecoder().decode(decodedBytes);
}


// FINAL MESSAGE REVEAL

async function revealFinalMessage() {
    const hiddenCode = decodeMessage(encodedMessage, decodingKey);
    const element = document.getElementById("finalMessage");

    const message =
        "CONGRATS, TRAVELER.\n\n" +
        "YOU HAVE COME FAR.\n\n" +
        "YOUR FINAL CHALLENGE AWAITS WHERE YOU STARTED.\n\n" +
        "THE CODE IS: " + hiddenCode + ".";

    element.textContent = "";

    for (const character of message) {
        element.textContent += character;
        await new Promise(resolve => setTimeout(resolve, 25));
    }
}


// ENTER KEY SUPPORT

document.getElementById("codeInput")
    .addEventListener("keydown", function(event) {
        if (event.key === "Enter") {
            checkCode();
        }
    });

</script>

</body>
</html>
