KAAMNA PROPOSAL WEBSITE — QUICK START

Files:
- index.html: complete responsive website, styles and JavaScript are included.

How to use:
1. Open index.html in a browser to preview it.
2. Upload index.html to your web hosting (for example, Hostinger File Manager) inside the website's public_html folder.
3. Share your website URL with Kaamna.

What works:
- Mobile-friendly romantic proposal page.
- NO button dodges pointer/touch/click.
- YES opens a cinematic-style animated surprise with hearts and a personal letter.
- Original gentle synth melody starts after YES (browser audio policy requires a user click).

About music and video:
- The site does not include a copyrighted Bollywood song or a pre-rendered video file. It uses a generated original melody and a CSS cinematic scene, so it works without external assets.
- To add a song you have permission to use, add it as assets/romantic-song.mp3 and add this line inside index.html before </body>:
  <script>document.getElementById('music').src='assets/romantic-song.mp3';</script>
  Then change the startMelody() call in the YES button handler to:
  const audio=document.getElementById('music'); audio.play().catch(()=>startMelody());
  For the music button, wire play/pause to the audio element.
- To use a personal proposal video, put it at assets/proposal.mp4 and add a <video controls playsinline> element inside the surprise section:
  <video controls playsinline style="width:100%;border-radius:16px" src="assets/proposal.mp4"></video>
- Browser autoplay restrictions mean audio should begin after a click/tap. Use music you have rights to share.

This is a standalone starter site and requires no build tools, libraries, or server-side code.
