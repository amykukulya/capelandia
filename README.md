# Capelandia — Squarespace Code Block Instructions
## Option 2: Inject custom homepage into your existing Squarespace site

This approach keeps your shop, about, and contact pages on Squarespace
but replaces the homepage with your custom design.

---

## BEFORE YOU START — Upload your images

1. In Squarespace go to: Design > File Storage (or Assets)
2. Upload these 5 files and copy each public URL after upload:
   - CAPELANDIAwhitecircle.png  → YOUR_LOGO_WHITE_CIRCLE_URL
   - CAPELANDIA_PNG.png          → YOUR_LOGO_DARK_URL
   - Capelandiahat.png           → YOUR_HAT_PHOTO_URL
   - Capelandia_copy.png         → YOUR_APPAREL_PHOTO_URL
   - capelandia_favicon.png      → YOUR_FAVICON_URL
3. Open squarespace-code-block.html in a text editor (Notepad, TextEdit)
4. Find and replace all 5 YOUR_*_URL placeholders with the real URLs

---

## STEP A — Inject the CSS override (hides Squarespace's header/footer)

1. In Squarespace: Pages > (hover over homepage) > gear icon ⚙
2. Click "Advanced" tab
3. In "Page Header Code Injection" box, paste ONLY the first <style> block
   from the top of squarespace-code-block.html
   (the block that says "STEP A: PASTE THIS IN PAGE HEADER CODE INJECTION")
4. Click Save

---

## STEP B — Add the Code Block to your homepage

1. Go to your Homepage and click Edit
2. Delete ALL existing content blocks on the page
3. Click the + button to add a block
4. Scroll to "More" > choose "Code"
5. In the code block, paste everything BELOW the "STEP B" comment
   in squarespace-code-block.html
   (this is the bulk of the file — from the Google Fonts link through the end)
6. Make sure "Display Source" is OFF (toggle it off if needed)
7. Click Apply / Done
8. Save and publish the page

---

## TIPS & KNOWN SQUARESPACE QUIRKS

- If the page still shows Squarespace's nav: double-check Step A was saved.
  Some templates need you to also go to Design > Custom CSS and add:
    #header { display: none !important; }
    footer.Footer { display: none !important; }

- Squarespace Business plan or higher is required for Code Blocks.

- The contact form in the code is a visual mock-up — it doesn't submit yet.
  To make it functional, either:
    a) Replace it with a Squarespace Form Block (add below the code block), or
    b) Add a Formspree action: change <button> to a proper <form> with
       action="https://formspree.io/f/YOUR_ID" method="POST"

- If Squarespace's CSS bleeds in and breaks your layout, add this to
  Design > Custom CSS:
    .page-section:has(#cp-site) { padding: 0 !important; }

- The Squarespace shop at /shop continues to work normally and is linked
  from your custom nav and shop section.

---

## RECOMMENDATION

Option 1 (Netlify) gives you 100% clean results with zero Squarespace
interference. Option 2 is more fragile. If you try Option 2 and run into
styling conflicts, switch to Option 1 — it's a 5-minute setup and your
shop links will still point to capelandia.com/shop on Squarespace.
