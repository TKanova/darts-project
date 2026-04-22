# Darts Project

**Internships for High Schoolers — Kazakhstan**

Darts Project connects ambitious high school students with internships at Kazakhstan's leading companies: Forte Bank, KPMG, Ritz-Carlton, Kazakhtelecom, QazCloud, G&G, and TrustMe.

Live site: [dartsprojectqz.com](https://dartsprojectqz.com)

---

## What's on the site

| Section | Description |
|---|---|
| Hero | Intro headline, stats (50+ interns, 8 partners, 3 schools) |
| Find Your Match | 4-question quiz that recommends a partner company |
| About / Mission | Why Darts Project exists |
| How to Apply | 5-step application process |
| Alumni | Testimonials from past interns |
| Our Team | Team members grouped by school |
| Partners | Partner companies with links to become one |

---

## How to use

### For students

1. Go to [dartsprojectqz.com](https://dartsprojectqz.com)
2. Click **Find Your Match** and complete the 4-question quiz — it recommends which company fits you best
3. Click **Apply Now** or go to the *How to Apply* section
4. Send your CV, essay, and references to **dartsprojectqz@gmail.com**
5. Apply early — rolling admissions, early applicants get priority

### For partner companies

Email [dartsprojectqz@gmail.com](mailto:dartsprojectqz@gmail.com) or scroll to the *Partners* section and click **Get in touch**.

---

## Editing the site

Everything is in a single file: `index.html`

### Change text content

Open `index.html` and search for the section you want to edit. Each section has an `id`:

```
#hero       → hero headline and stats
#quiz       → quiz questions and result descriptions
#mission    → mission statement and values
#steps      → application steps
#alumni     → testimonial cards
#team       → team members
#partners   → partner company cards
#footer     → footer links and contact info
```

### Add a new alumni testimonial

Find the `alumni-grid` div and copy an existing card block:

```html
<div class="alumni-card reveal">
  <p class="alumni-quote">"Your quote here."</p>
  <div class="alumni-person">
    <div class="alumni-avatar">AB</div>
    <div>
      <div class="alumni-name">Full Name</div>
      <span class="alumni-company">Company Name</span>
    </div>
  </div>
</div>
```

### Add a new team member

Find the relevant `team-grid` div and add:

```html
<div class="team-card">
  <div class="team-photo">
    <img src="path/to/photo.jpg" alt="Name">
  </div>
  <div class="team-name">Full Name</div>
  <div class="team-role">Role</div>
</div>
```

If there's no photo, remove the `<img>` tag — the card will show initials automatically (add them as text inside `.team-photo`).

### Update the quiz results

In the `<script>` block, find `resultMap` and edit the company name (`co`) and description (`desc`) for each key:

```js
const resultMap = {
  finance:   { co: 'Forte Bank', desc: '...' },
  tech:      { co: 'QazCloud',   desc: '...' },
  ...
};
```

### Change colors

All colors are CSS variables at the top of the `<style>` block:

```css
:root {
  --red:       #C41E1E;
  --red-dark:  #9B1515;
  --red-light: #E63C3C;
  --cream:     #FAF7F2;
  --charcoal:  #1A1A1A;
}
```

---

## Deploying changes

The site is hosted on **GitHub Pages** from the `main` branch.

```bash
git add index.html
git commit -m "Your change description"
git push origin main
```

GitHub Pages rebuilds automatically — changes are live within ~1-2 minutes. If the old version still shows, open the site in a private/incognito browser tab to bypass cache.

---

## Contact

- Email: [dartsprojectqz@gmail.com](mailto:dartsprojectqz@gmail.com)
- Instagram: [@dartsproject_](https://instagram.com/dartsproject_)
- LinkedIn: [Darts Project](https://www.linkedin.com/company/darts-project/)
- Telegram: [@dartsproject](https://t.me/dartsproject)
