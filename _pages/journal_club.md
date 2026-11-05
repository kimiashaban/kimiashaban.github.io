---
layout: page
permalink: /journal-club/
title: journal club
description: The Computer Vision Journal Club at the University of Toronto, KITE, and the Vector Institute. Edited at <a href="https://taatiteam.github.io/journal-club/">taatiteam.github.io/journal-club</a>.
nav: true
nav_order: 4
---

<!-- The page content lives in the TaatiTeam/journal-club repo and is shown
     here live. ?embed=1 hides that site's own header and footer; the frame
     follows this site's light/dark setting and grows to fit the content. -->

<div class="jc-embed">
  <iframe id="jc-frame" title="Computer Vision Journal Club" src="https://taatiteam.github.io/journal-club/?embed=1" loading="eager" scrolling="no"></iframe>
  <noscript><p><a href="https://taatiteam.github.io/journal-club/">Open the journal club page.</a></p></noscript>
</div>

<style>
  .jc-embed iframe { display: block; width: 100%; min-height: 70vh; border: 0; }
</style>
<script>
  (function () {
    var ORIGIN = "https://taatiteam.github.io";
    var frame = document.getElementById("jc-frame");
    var html = document.documentElement;
    var theme = function () { return html.getAttribute("data-theme") === "dark" ? "dark" : "light"; };
    frame.src = ORIGIN + "/journal-club/?embed=1&theme=" + theme();
    window.addEventListener("message", function (e) {
      if (e.origin !== ORIGIN || !e.data || !e.data.journalClubHeight) return;
      frame.style.height = e.data.journalClubHeight + "px";
    });
    new MutationObserver(function () {
      frame.contentWindow && frame.contentWindow.postMessage({ journalClubTheme: theme() }, ORIGIN);
    }).observe(html, { attributes: true, attributeFilter: ["data-theme"] });
  })();
</script>
