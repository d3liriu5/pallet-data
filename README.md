# Pallet Data
 
This repo is a shared resource for anyone at Motive who wants to build prototypes, experiments, or internal tools using real fleet data&mdash;without needing deep technical expertise or wrangling fake placeholder content.

It contains anonymized schema files that represent the core parts of our platform. Think of them as maps: they tell you exactly what data exists, what it's called, and how it connects together. Pair them with v0, Claude Code, or Figma Make, and you can go from idea to working prototype in an afternoon.

 
## Why prototype with real data?
 
Fake data doesn't cut it. A list of "Chandler Bing, Rachel Green, Ross Geller" doesn't tell you whether your layout breaks when a name is unusually long. Placeholder numbers don't reveal that transaction patterns and amounts in real life are weird. A hardcoded map pin doesn't reflect that 40% of your fleet is parked in rural areas with no nearby landmarks.

Real data surfaces edge cases early, builds stakeholder confidence, and means less rework when your prototype hands off to production. The schemas in this repo are structurally similar to what's in production, allowing you to design and test against data that actually reflects reality.


## What's in this repo
 
| File | Dataset | What it covers |
|------|---------|----------------|
| `fx_schema.md` | Fleet Operations | Drivers, vehicles, live locations, geofences, safety events |
| `cd_schema.md` | Fleet + Motive Card | Everything in fx_schema.md, plus Motive Cards, spend profiles, transactions |
| `cn_schema.md` (coming soon) | Fleet + Safety | Drivers, vehicles, live locations, safety events, coaching |
 
**Not sure which one to use?** Start with `fx_schema.md` if your prototype is about where drivers are, how they're driving, or their status. Use `cd_schema.md` if your prototype touches money&mdash;fuel spend, card limits, transaction history. Use `cn_schema.md` if your prototype has a safety or coaching angle.


## How to use these files
 
Each schema file contains:
 
- **Plain-English table descriptions** — what each table stores, in human terms
- **Column listings** — every field name, its data type, and whether it can be empty
- **Entity relationship summary** — how the tables connect to each other, and what to watch out for

The workflow is simple:
 
1. Open the relevant schema file and skim the table descriptions
2. Identify which tables and columns your prototype needs
3. Paste the schema (or the relevant section) into your AI-assisted prototyping tool of choice as context
4. Describe what you want to build

The data lives in Supabase. To connect, you'll need two credentials&mdasha `project URL` and an `anon key`. Request both from Manny on Slack, store them in a .env file locally, and never commit them to any respository. Your AI-assisted prototyping tool will help you establish a connection to the anonymized, live data.
 
### v0
 
Paste your schema excerpt and describe the UI in a single prompt. v0 works best when you give it the table name, the columns you want, and a clear picture of the component.
 
> Using the schema below, build a React driver list component. Fetch from Supabase using URL `$SUPABASE_URL` and anon key `$SUPABASE_ANON_KEY`. Query the `fx_drivers` table and display each driver's full name, duty status (as a colored badge: green for on_duty, gray for off_duty), carrier city and state, and account status. Filter to active drivers only.
>
> [paste schema excerpt here]
 
### Claude Code
 
Give Claude Code the full schema file upfront — it handles long context well. Describe the prototype you want and let it wire the data connection for you.
 
> Here is my database schema:
>
> [paste schema file contents here]
>
> Using this schema and the Supabase JS client, build a simple dashboard page that shows a summary of fleet activity. Use `$SUPABASE_URL` as the project URL and `$SUPABASE_ANON_KEY` as the anon key. Pull from `fx_vehicles` and `fx_latest_vehicle_locations` to show a count of active vehicles, how many are currently assigned to a driver, and a list of the 10 most recently active vehicles with their location and assigned driver name.
 
### Figma Make

Figma Make is prompt-driven and has a native Supabase integration. Connect your Supabase project in the data settings using `$SUPABASE_URL` and `$SUPABASE_ANON_KEY`, then describe your UI in a prompt the same way you would in v0.
 
> Using the fx_drivers table, build a driver roster dashboard. Show each driver's full name, duty status as a colored badge, and carrier city and state. Filter to active drivers only and sort alphabetically by last name. Use our design library for components and styling.
>
> [paste schema excerpt here]


## A few things to know
 
- **Monetary values are mixed units.** Transaction amounts in `_card_transactions` are in dollars. Spend limits in `_spend_profiles` are in cents. Always divide spend profile limits by 100 before displaying or comparing them.
- **Location data is a snapshot.** The `_latest_vehicle_locations` tables store only the *current* position of each vehicle, not history. Reach out to Manny if you need historical location data.
- **Card assignments aren't mutually exclusive.** A card in `_cards` can be assigned to a driver, a vehicle, or an asset. Check which of the three `assigned_to_*` columns is non-null rather than assuming one is always set.
- **This data is anonymized, not synthetic.** It reflects real structural patterns, real edge cases, and real volume.

 
## Contributing, feedback, and requests

More data exists beyond what's currently in this repo. If you're prototyping something and the schemas don't have what you need, don't assume it isn't available. Reach out to Manny and we'll figure it out together. Sometimes the raw data needs to be massaged, reshaped, or optimized before it's useful for a prototype, and in those cases a Supabase database function can be created to do that work for you. And if you come across data in your own work that you think others might find useful, let's talk about adding it to Supabase and updating the schema files here so everyone benefits.

The best way to request data, report an issue, or suggest an improvement is to open a GitHub Issue. You'll find the Issues tab at the top of the repo. Click New Issue, give it a descriptive title, and include as much context as you can&mdashwhat you're trying to build, what data you need, or what looks wrong and where.

Use issues for things like:
- Requesting data — you're prototyping something and the schemas don't have what you need
- Reporting a schema error — a column is missing, a description is wrong, or a relationship doesn't match what's in Supabase
- Proposing a new dataset — you've come across data you think others would find useful

If you'd rather not open an issue or want to talk it through first, reach out to Manny on Slack!
