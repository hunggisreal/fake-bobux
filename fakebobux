(function () {
    'use strict';

    var userInput = prompt("Enter your robux:");
    if (!userInput) return;

    function updateRobuxDisplay() {
        const robuxAmount = document.querySelector('[data-robux-amount]') ||
                            document.querySelector('#nav-robux-amount') ||
                            document.querySelector('span[class*="robux"]');

        const robuxBalance = document.querySelector('#nav-robux-balance') ||
                             document.querySelector('[data-robux-balance]');

        if (robuxAmount) {
            robuxAmount.textContent = userInput;
            robuxAmount.style.visibility = "visible";
        }

        if (robuxBalance) {
            robuxBalance.textContent = userInput;
            robuxBalance.style.visibility = "visible";
        }
    }

    const observer = new MutationObserver(() => {
        updateRobuxDisplay();
    });

    observer.observe(document.body, {
        childList: true,
        subtree: true
    });

    const interval = setInterval(() => {
        updateRobuxDisplay();
    }, 1000);

    window.addEventListener("load", updateRobuxDisplay);
})();
