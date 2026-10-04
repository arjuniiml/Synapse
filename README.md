[README.md](https://github.com/user-attachments/files/33023839/README.md)
# IIM Lucknow Sports Facility Booking Sheet (Standalone HTML Version)

A lightweight, zero-dependency, Excel-style sports booking website built entirely in pure **HTML, CSS, and Vanilla JavaScript**.

---

### Features
1. **Excel Sheet Look & Feel**:
   - Classic Excel green ribbon and crisp spreadsheet grid.
   - Sticky facility column on the left and sticky 30-min time columns at the top.
   - Cells show `—` (Available), `G` (1 section), `G + H` (Two-section full capacity), or blocked reasons.

2. **Google SSO Simulation**:
   - Single sign-on screen restricted strictly to `@iiml.ac.in` email addresses.
   - Rejects non-IIML logins.
   - Direct drop into the main booking sheet (no distracting dashboards).

3. **Date Navigation & Sport Filtering**:
   - `[ ← ] [ 4 October 2026 ] [ → ]` day-to-day navigation (disables past dates).
   - Sport dropdown filter to isolate single facilities (Badminton, Basketball, Cricket, Football, Tennis, etc.) without leaving the sheet.

4. **Click-to-Book & Smart 60-Minute Slots**:
   - Click any `—` cell to open the booking popup.
   - Automatically populates Facility, Date, Time, and student credentials.
   - **Smart 60-min rule**: If slot 2 is already partially booked by another section, it safely books slot 1 and triggers an automated **Share Request** to the other section!

5. **Booked Slot Actions**:
   - Click any booked cell (`G` or `G + H`) to inspect POC 1 & POC 2 contact details.
   - **Request to Share**: If only 1 section has booked, other sections can request to share.
   - **Atomic Swap**: Propose an atomic slot exchange with another section.

6. **Notification Banner**:
   - Displays incoming swap and share requests at the top with `[ Accept ]` and `[ Reject ]`.

---

### How to Run Locally

You do **not** need Node.js, npm, or any build steps! Simply:

1. Double-click `index.html` to open it in **Chrome, Edge, Firefox, or Safari**.
2. Or serve it via any local web server:
   ```bash
   npx serve .
   # or with Python
   python -m http.server 8080
   ```

---

### How to Host on Vercel, Netlify, or GitHub Pages

Because this is a pure static HTML file:
- **Vercel**: Run `npx vercel` inside this folder or push to GitHub and import it on Vercel (framework preset: "Other").
- **GitHub Pages**: Go to your GitHub repository -> Settings -> Pages -> deploy from root.
- **Netlify**: Drag and drop this folder directly into the Netlify drop zone.
