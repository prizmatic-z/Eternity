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


            rgba(0,255,100,0.035) 4px


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


        50% { opacity: 0; }


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


        min-height: 80px;


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



        <div id="codeResult"></div>



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



            let delay = typingSpeed +


                Math.random() * 100;



            setTimeout(typeNextCharacter, delay);



        } else {



            finishTransmission();



        }


    }



    function finishTransmission() {



        output.innerHTML +=


            '<span class="cursor">_</span>';



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



        const hashBuffer = await crypto.subtle.digest(


            "SHA-256",


            data


        );



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



                result.className = "success";



                result.textContent = "";



                await revealFinalMessage(result);



            } else {



                result.className = "error";



                result.textContent =


                    "ACCESS DENIED.\n" +


                    "INVALID CODE. TRY AGAIN.";



            }



        } catch (error) {



            result.className = "error";



            result.textContent =


                "SYSTEM ERROR: CRYPTOGRAPHIC MODULE UNAVAILABLE.";



        }



    }



    // HIDDEN FINAL MESSAGE


    // Encoded using repeating-key XOR and Base64.



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



    async function revealFinalMessage(element) {



        const hiddenCode = decodeMessage(


            encodedMessage,


            decodingKey


        );



        const message =


            "CONGRATS, TRAVELER.\n\n" +


            "YOU HAVE COME FAR.\n\n" +


            "YOUR FINAL CHALLENGE AWAITS WHERE YOU STARTED.\n\n" +


            "THE CODE IS: " + hiddenCode + ".";



        element.textContent = "";



        for (const character of message) {



            element.textContent += character;



            await new Promise(resolve =>


                setTimeout(resolve, 25)


            );



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



</body>


</html>
