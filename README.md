# Unit-3-Touchstone-3
/* North Star Bakery - Touchstone 3 stylesheet
   Mobile-first: base styles are for phones; the media queries at the
   bottom enhance the layout for tablets and desktops. */

/* ---------- Design system: 4 colors, 2 fonts ---------- */
:root {
  --cream: #FFF8EE;     /* page background */
  --brown: #5C3317;     /* header, footer, headings */
  --orange: #A34A14;    /* links, buttons, accents */
  --charcoal: #2B2622;  /* body text */

  --font-heading: "Lora", Georgia, serif;
  --font-body: "Source Sans 3", "Segoe UI", Arial, sans-serif;

  --space: 1rem;
  --radius: 8px;
}

/* ---------- Base ---------- */
*,
*::before,
*::after {
  box-sizing: border-box;
}

body {
  margin: 0;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background: var(--cream);
  color: var(--charcoal);
  font-family: var(--font-body);
  font-size: 1.125rem;
  line-height: 1.6;
}

img,
video {
  display: block;
  max-width: 100%;
  height: auto;
  border-radius: var(--radius);
}

audio {
  width: 100%;
}

/* ---------- Typography ---------- */
h1,
h2,
h3 {
  font-family: var(--font-heading);
  color: var(--brown);
  line-height: 1.2;
  margin: 0 0 0.5rem;
}

h1 { font-size: 2rem; }
h2 { font-size: 1.5rem; }
h3 { font-size: 1.2rem; margin-top: 1.25rem; }

p { margin: 0 0 var(--space); }

a {
  color: var(--orange);
  text-underline-offset: 3px;
}

a:hover,
a:focus {
  color: var(--brown);
}

a:focus-visible,
button:focus-visible,
input:focus-visible,
select:focus-visible,
textarea:focus-visible {
  outline: 3px solid var(--orange);
  outline-offset: 2px;
}

/* ---------- Header and navigation (Flexbox) ---------- */
header {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
  padding: var(--space);
  background: var(--brown);
  color: var(--cream);
}

header img {
  width: 80px;
  height: 80px;
  border-radius: 50%;
}

.site-name {
  margin: 0;
  font-family: var(--font-heading);
  font-size: 1.5rem;
  font-weight: 700;
}

nav {
  width: 100%;
}

nav ul {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  margin: 0;
  padding: 0;
  list-style: none;
}

nav a {
  display: block;
  padding: 0.75rem 1rem;
  border: 2px solid var(--cream);
  border-radius: var(--radius);
  color: var(--cream);
  font-weight: 600;
  text-align: center;
  text-decoration: none;
}

nav a:hover,
nav a:focus {
  background: var(--cream);
  color: var(--brown);
}

nav a[aria-current="page"] {
  background: var(--cream);
  color: var(--brown);
}

/* ---------- Main content (Flexbox) ---------- */
main {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: var(--space);
  width: 100%;
  max-width: 70rem;
  margin: 0 auto;
  padding: var(--space);
}

main > section,
.page-intro {
  padding: 1.25rem;
  background: #fff;
  border: 2px solid var(--brown);
  border-radius: var(--radius);
}

main > section img,
main > section video,
main > section audio,
main > section picture {
  margin: 0.75rem 0 1rem;
}

main > section img,
main > section picture img {
  width: 100%;
  max-height: 26rem;
  object-fit: cover;
}

main ul {
  padding-left: 1.25rem;
}

main li {
  margin-bottom: 0.35rem;
}

.page-intro {
  background: var(--brown);
  border-color: var(--brown);
}

.page-intro h1,
.page-intro p {
  color: var(--cream);
}

.page-intro a {
  color: var(--cream);
}

.page-intro a:hover,
.page-intro a:focus {
  color: #fff;
}

.price {
  color: var(--brown);
  font-weight: 600;
}

figure {
  margin: 1rem 0 0;
}

figcaption {
  margin-top: 0.5rem;
  font-size: 1rem;
  font-style: italic;
}

address {
  margin-bottom: var(--space);
  font-style: normal;
}

/* ---------- Buttons ---------- */
.button,
button {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  border: 2px solid var(--orange);
  border-radius: var(--radius);
  background: var(--orange);
  color: #fff;
  font-family: var(--font-body);
  font-size: 1.125rem;
  font-weight: 600;
  text-decoration: none;
  cursor: pointer;
}

.button:hover,
.button:focus,
button:hover,
button:focus {
  background: var(--brown);
  border-color: var(--brown);
  color: #fff;
}

button.secondary {
  background: transparent;
  color: var(--orange);
}

button.secondary:hover,
button.secondary:focus {
  background: var(--brown);
  color: #fff;
}

.cta {
  text-align: center;
}

/* ---------- Form ---------- */
fieldset {
  margin: 0 0 var(--space);
  padding: 1rem;
  border: 2px solid var(--brown);
  border-radius: var(--radius);
}

legend {
  padding: 0 0.5rem;
  color: var(--brown);
  font-family: var(--font-heading);
  font-size: 1.2rem;
  font-weight: 700;
}

form p {
  margin-bottom: 1rem;
}

label {
  display: block;
  margin-bottom: 0.25rem;
  font-weight: 600;
}

input,
select,
textarea {
  display: block;
  width: 100%;
  padding: 0.65rem;
  border: 2px solid var(--charcoal);
  border-radius: var(--radius);
  background: #fff;
  color: var(--charcoal);
  font-family: var(--font-body);
  font-size: 1.125rem;
}

.buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 0.75rem;
}

/* ---------- Footer ---------- */
footer {
  padding: var(--space);
  background: var(--charcoal);
  color: var(--cream);
  font-size: 1rem;
  text-align: center;
}

footer p {
  margin: 0 0 0.4rem;
}

/* ---------- Tablet and desktop (min-width: 800px) ---------- */
@media (min-width: 800px) {
  h1 { font-size: 2.75rem; }
  h2 { font-size: 1.75rem; }

  /* Header: logo, name and navigation sit in one row */
  header {
    flex-direction: row;
    justify-content: space-between;
    padding: var(--space) 2rem;
    gap: 1rem;
  }

  header img {
    width: 90px;
    height: 90px;
  }

  nav {
    width: auto;
    margin-left: auto;
  }

  nav ul {
    flex-direction: row;
  }

  nav a {
    padding: 0.5rem 0.9rem;
    font-size: 1rem;
  }

  /* Content: sections flow into two columns */
  main {
    flex-direction: row;
    flex-wrap: wrap;
    align-items: flex-start;
    gap: 1.5rem;
    padding: 2rem;
  }

  main > section,
  .page-intro {
    flex: 1 1 calc(50% - 1.5rem);
  }

  main > .full {
    flex: 1 1 100%;
  }

  .page-intro {
    padding: 2rem;
  }

  /* Contact form: fieldsets sit side by side */
  form {
    display: flex;
    flex-wrap: wrap;
    align-items: flex-start;
    gap: 1.5rem;
  }

  fieldset {
    flex: 1 1 calc(50% - 1.5rem);
    margin: 0;
  }

  .buttons {
    flex: 1 1 100%;
  }

  footer {
    padding: 1.5rem 2rem;
  }
}
