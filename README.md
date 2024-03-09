# code__part

# Direct Redirect to Thank You Page if Someone filled out the form already.....
---
---
<script>
    // Function to set a cookie
    function setCookie(cname, cvalue, exdays) {
        var d = new Date();
        d.setTime(d.getTime() + (exdays * 24 * 60 * 60 * 1000));
        var expires = "expires=" + d.toUTCString();
        document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
    }

    // Function to get a cookie by name
    function getCookie(cname) {
        var name = cname + "=";
        var decodedCookie = decodeURIComponent(document.cookie);
        var ca = decodedCookie.split(';');
        for (var i = 0; i < ca.length; i++) {
            var c = ca[i];
            while (c.charAt(0) == ' ') {
                c = c.substring(1);
            }
            if (c.indexOf(name) == 0) {
                return c.substring(name.length, c.length);
            }
        }
        return "";
    }

    // Function to check if the form has been submitted
    function checkFormSubmitted() {
        var formSubmitted = getCookie("formSubmitted");
        if (formSubmitted) {
            // Check if the URL parameter is_test=true is present
            var urlParams = new URLSearchParams(window.location.search);
            if (urlParams.has('is_test') && urlParams.get('is_test') === 'true') {
                // If the is_test parameter is true, do not redirect
                return;
            }
            // Redirect to the Thank You page
            window.location.href = "https://contact.consumersafe.com/paragard/ty/a.html";
        }
    }

    // Event listener for form submission
    document.getElementById("lp-pom-form-345").addEventListener("submit", function (event) {
        // Set a cookie to indicate that the form has been submitted
        setCookie("formSubmitted", "true", 1);
    });

    // Check if the form has been submitted when the page loads
    window.onload = function () {
        checkFormSubmitted();
    };
</script>

---
---

#Library for scroll Library
---
---
<script src="https://unpkg.com/scrollreveal"></script>
---
---
********HEIGHT Slick slider of same height *********
.slick-track
{
    display: flex !important;
}

.slick-slide
{
    height: inherit !important;
}
---
---

# Setting Up Tailwind
---
---
SETTING UP TAILWIND
• To setup tailwind ess, run these commands
I. npm init -y // This initializes the directory as a NodeJs project
2. npm install -D tailwindess postess autoprefixer vite // installs required packages
3. np tailwindess init -p
4. Create a css file "input.css", add it to your html and edit it with this content:
@tailwind base;
@tailwind components;
@tailwind utilities;
5. In your tailwind.config.js file replace content: [], with content: ["*"],
6. Add "start": Vite" to your scripts in package.json
7. Run npm run start command to start a dev server
---
---
When you you closed the editor and reopen at anu time then run command ---
1.run npm i or npm i
2. Run npm run start command to start a dev server
