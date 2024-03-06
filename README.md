# code__part

# Direct Redirect to Thank You Page if Someone filled out the form already.....
---
---
<script>
document.addEventListener('DOMContentLoaded', function() {
    if (document.cookie.indexOf('form_filled=true') !== -1) {
        window.location.href = 'URL_of_Thank_You_Page';
    } else {
        // If cookie doesn't exist, set it and proceed
        document.cookie = 'form_filled=true; expires=Fri, 31 Dec 9999 23:59:59 GMT; path=/';
    }
});
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
