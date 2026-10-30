# D.K. Home Solutions (Regd.) website

A responsive React + Vite website for D.K. Home Solutions, built with HTML, CSS and JavaScript. Includes service cards, enquiry form-to-WhatsApp flow, service details modal, gallery lightbox, contact links, responsive navigation, scroll reveals and reduced-motion support.

## Requirements
- Node.js 20.19+ or 22.12+ recommended
- npm
- Visual Studio Code (optional)

## Run locally
1. Extract the project ZIP.
2. Open the `dk-home-solutions` folder in Visual Studio Code.
3. Open Terminal → New Terminal.
4. Run:
   ```bash
   npm install
   npm run dev
   ```
5. Open the local URL Vite prints (usually `http://localhost:5173`).

## Production build
```bash
npm run build
npm run preview
```
The production site is generated in the `dist/` folder. Deploy `dist/` to a static host such as Netlify, Vercel, GitHub Pages (with appropriate Vite base configuration), or your own web hosting. No backend, database, or paid API is required for this version.

## Where to edit
- **Business details and WhatsApp number:** `src/main.jsx`, near the top (`PHONE1`, `PHONE2`, `WHATSAPP`, `ADDRESS`). WhatsApp must use country code 91 without the `+` sign: `919315143991`.
- **Services and service images:** the `services` array in `src/main.jsx`. Each `image` value is an Unsplash photo ID. `photo()` constructs the image URL. Gallery images are in the `gallery` array.
- **Text:** update the matching JSX sections in `src/main.jsx`.
- **Colours, spacing and responsive styles:** CSS variables at the top of `src/styles.css`, especially `--navy`, `--gold`, `--cream`, and `--muted`.
- **SEO metadata and page title:** `index.html`.
- **Business hours:** currently worded to call and confirm; update the business information card in `src/main.jsx` only when confirmed hours are available.

## Enquiry behaviour
The form validates required fields and the phone number, then opens WhatsApp with a prefilled message. The visitor must review and send that message in WhatsApp. The site does not save enquiries to a database. No customer form data is transmitted by this website before the visitor chooses to send it through WhatsApp.

## Photos
Photos use Unsplash image URLs and are illustrative stock photography, not representations of actual employees. An internet connection is required to load remote fonts and photos. Image URLs and availability may change; replace photo IDs with suitable free/appropriately licensed images when needed.

## Notes before publishing
- Confirm the business details, registration number, phone numbers and office address before publishing.
- Test WhatsApp on a device where WhatsApp Web/app is available.
- Test all image URLs and contact links on the intended hosting domain.
- Add a privacy notice and any legally required terms appropriate to your business before collecting enquiries at scale.
- The site does not make claims about employee verification, certifications, testimonials, ratings, awards or guaranteed availability.
