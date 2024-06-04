# smooth-scroll-browser-viewport  

open DEV-tools (F12)  
open console  

```
(function smoothScroll() {
    const scrollStep = 15; // Anzahl der Pixel pro Schritt
    const scrollInterval = 15; // Zeit in Millisekunden zwischen den Schritten

    function scrollDown() {
        window.scrollBy(0, scrollStep);
        if ((window.innerHeight + window.scrollY) >= document.body.scrollHeight) {
            clearInterval(scrollTimer);
        }
    }

    const scrollTimer = setInterval(scrollDown, scrollInterval);
})();
```
