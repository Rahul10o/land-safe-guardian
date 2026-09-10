# TerraAlert Safety

Build a mobile-first web app called "TerraAlert" (Landslide Disaster Management System) 

for residents, local authorities, and rescue teams in hilly, landslide-prone regions. 

This is a safety-critical app — prioritize clarity, speed, and high contrast over 

decorative styling. Must work well on low-end Android devices and in bright outdoor light.

=== DESIGN SYSTEM ===

Style: Clean, flat, high-contrast (NOT neumorphism/soft shadows)

Rounded corners: 12-16px on cards, inputs, buttons

Tap targets: minimum 48px height

Colors:

- Primary: #2C5AA0 (deep blue)

- Danger/Alert: #E63946 (strong red-orange)

- Warning: #F4A300 (amber)

- Success/Safe: #2A9D5C (green)

- Background: #F5F6FA (off-white)

- Text: #1A1A2E (near-black)

- Card background: #FFFFFF with 1px border #E0E2E8, no heavy shadows

Typography: bold, legible sans-serif, larger base font size (16px+) for readability

No color-only indicators — always pair color with icons/text for accessibility

=== USER ROLES ===

1. Resident/Citizen (default view)

2. Local Authority/Admin (dashboard with elevated permissions)

=== SCREENS TO BUILD ===

1. WELCOME / LOGIN

- App logo (mountain + warning triangle icon, primary blue)

- Email/password login, social login (Google, Facebook, Apple)

- "Sign up" link, "Forgot password" link

- Language selector (dropdown, top corner) for multilingual support

2. SIGN UP

- Name, email, phone, password fields

- Location selection (village/district dropdown or "use current location")

- Role selector: Resident or Authority (authority requires verification note)

3. HOME / RISK DASHBOARD (main screen after login)

- Top banner: current risk level for user's area — big colored badge 

  (green/amber/red) with icon, e.g. "Risk Level: MODERATE"

- Embedded map view showing risk zones color-coded by severity, user's location pin, 

  and nearby shelters

- Quick-access alert feed below map: scrollable cards showing recent alerts 

  (timestamp, severity icon, short description)

- Large floating "Report Incident" button (danger red, always visible/sticky)

- Bottom nav bar: Home | Map | Report | Alerts | Profile

4. INCIDENT REPORT FORM

- Photo upload (camera or gallery)

- Auto-captured GPS location (editable pin on mini-map)

- Incident type selector: crack in ground, water seepage, small slide, road blockage, other

- Severity slider: Low / Medium / High / Critical

- Optional text description

- Large "Submit Report" button (danger red)

- Confirmation screen after submit

5. ALERTS SCREEN

- Filterable list (All / Warnings / Evacuation Orders / Weather Updates)

- Each alert card: severity badge, title, timestamp, short description, "View Details" 

- Alert detail view: full description, affected zones on mini-map, recommended action, 

  source (authority name)

- Push notification opt-in banner if not enabled

6. EVACUATION / SAFETY INFO

- List of nearest shelters with distance, capacity status, and "Get Directions" button

- Step-by-step evacuation route on map from user's location

- Emergency contact numbers (large tap-to-call buttons): local authority, ambulance, 

  disaster helpline

- Offline-accessible safety checklist (what to pack, what to do before/during/after)

7. AUTHORITY DASHBOARD (admin role only)

- Overview stats: active alerts, pending incident reports, total residents in monitored area

- Map view with all reported incidents as pins (filterable by status: new/verified/resolved)

- "Create Alert" form: select affected zone(s), severity, message, auto-translate option

- Incident report review queue: approve/reject/escalate reported incidents

- Rainfall/weather data widget (placeholder for external API integration)

8. PROFILE / SETTINGS

- User info, edit profile

- Language preference

- Notification preferences (push, SMS, email toggles)

- Emergency contacts (personal, editable)

- Offline data sync status ("Last synced: 2 hours ago")

- Logout

=== FUNCTIONAL REQUIREMENTS ===

- Fully responsive, mobile-first

- All forms functional with validation and loading/success/error states

- Placeholder data for map, alerts, and reports (structured so it's easy to wire to a 

  real API later)

- Offline-friendly UI cues: show a banner "You're offline — showing last saved data" 

  when applicable

- Authentication logic can be placeholder/mock for now

- All interactive elements need visible focus states for accessibility

- WCAG AA contrast compliance throughout

Make the whole app feel calm and trustworthy in normal conditions, but instantly 

legible and urgent when showing active alerts or high-risk states.     Use the logo i provide

This project was built with [Lovable](https://lovable.dev).

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/94119aec-a491-424e-94d0-8d95095ca4d2).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```
