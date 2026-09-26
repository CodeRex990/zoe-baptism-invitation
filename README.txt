Zoe Llaine Simeon's Baptism - Jollibee FairyTale Land invitation website
(Sunday, October 4, 2026 - Guiguinto, Bulacan)
==========================================================================

Files
  index.html                 the whole site (HTML + CSS + JS + Lottie data in one file)
  images/                    WebP images and the 1200x630 link-preview thumbnail
                             (zoe-llaine-simeon-baptism-invitation-og.jpg)
  audio/fairytale-lullaby.mp3   background music (original music-box waltz, ~76 s loop)
  animations/celebration-confetti.json   the Lottie sparkle animation (also embedded in index.html)
  robots.txt, sitemap.xml    search-engine files

This site is already live at https://zoe-baptism-invitation.vercel.app/ - the canonical
links, Open Graph tags, and JSON-LD in index.html point there. If you ever move it to a
different address, update those (search for the domain) plus robots.txt and sitemap.xml.

Sections on the page, top to bottom
  Hero - "You are invited! Zoe Llaine's Baptism" with Zoe's photo and countdown button
  Royal feast ticker - a looping strip of food icons (fried chicken, spaghetti, fries, sundaes)
  Countdown - live countdown to the baptism mass, with an "Add to Google Calendar" button
  Schedule - the two stops with times, addresses and "View map" links
  Gift idea - monetary gift only
  Dress code - attire for Ninong/Ninang, guests (pastel colors), and general rules
  Godparents - two columns, GodFathers and GodMothers, each with a highlighted principal
               sponsor (Wilmor Bello / Ellaine Simeon) at the top
  See you! - a closing photo of Zoe in a gold frame

Event details (edit in index.html - search for the words)
  10:30 am  Baptism mass - San Ildefonso Parish Church, Poblacion, Guiguinto, Bulacan (Diocese of Malolos)
  12:00 noon  Celebration - Jollibee Sta. Cruz, Guiguinto
  Assumed end times (not given): the countdown's "thank you" message and the Google Calendar entry
  assume the day wraps up around 3:00 pm / 2:30 pm. Change END in the <script> near the bottom of
  index.html and the dates=... part of the "Add to Google Calendar" link if that is wrong.
  "View map" links search by venue name; swap in exact Google Maps share links if you have them.

Editing the Godparents list
  Each name is a plain <li> inside <ul class="god-list"> - search for "GodFathers" or "GodMothers"
  in index.html to find the two lists. To highlight a different name the way Wilmor Bello and
  Ellaine Simeon are highlighted, wrap it as:
    <li class="principal"><span class="tag">Principal Ninong</span>Name Here</li>
  Only one name per column has that treatment; every other name is a plain <li>Name</li>.

Background music
  Browsers block sound autoplay until a visitor interacts with the page, so the page tries to autoplay
  and, if the browser says no, starts the music on the first tap / click / key press (a small hint and a
  pulsing music button at the bottom left tell people). The music button toggles it; the choice is remembered.
  To use your own track, replace audio/fairytale-lullaby.mp3 (keep the file name, or update the <audio> tag).

Celebration animation (Lottie)
  Plays on page load, on "Enter FairyTale Land", at "See you!", and whenever the wand button (bottom right)
  is tapped. Skipped automatically for visitors with "reduce motion" on (the button still works for them).
  To use a different Lottie, paste its JSON into <script type="application/json" id="lottie-confetti">.
  Player: lottie-web 5.12.2 from cdn.jsdelivr.net.

Countdown
  Counts down to Oct 4, 2026, 10:30 am Philippine time (UTC+8), then shows "It's Zoe's big day!".

Privacy note
  The page is set to be indexed by search engines. To keep it private to people who have the link, change
  <meta name="robots" content="index, follow, ..."> to <meta name="robots" content="noindex, nofollow">
  and in robots.txt use  Disallow: /
