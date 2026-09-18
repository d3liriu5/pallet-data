# Real Data, Real Prototypes
 
This repo is a shared resource for anyone at Motive who wants to build prototypes, experiments, or internal tools using real fleet data&mdash;no deep technical expertise required, no placeholder content to wrangle.

The data is anonymized, not synthetic. It reflects real structural patterns, real edge cases, and real volume. The schema files here are maps: they tell you what data exists, what it's called, and how it connects — designed to be pasted directly into AI-assisted prototyping tools like v0, Claude Code, and Figma Make.

 
## Why prototype with real data?
 
Fake data doesn't cut it. A list of "Chandler Bing, Rachel Green, Ross Geller" won't tell you your layout breaks on long names. Placeholder numbers won't reveal that transaction amounts are weird and inconsistent. A hardcoded map pin doesn't reflect that 40% of your fleet parks in rural areas with no nearby landmarks.

Real data surfaces edge cases early, builds stakeholder confidence, and reduces rework when your prototype hands off to production. These schemas are structurally close to production&mdash;so what you design is what you'll actually ship against.


## What's in this repo
 
| File                         | Industry            | Pillars                                   | At a Glance Volume          |
|------------------------------|---------------------|-------------------------------------------|-----------------------------|
| `cd_schema.md`               | field services      | Fleet Ops, Motive Card                    | 1K card transactions/week   |
| `fx_schema.md`               | LTL freight         | Fleet Ops, Geofences, Maintenance         | 19K+ drivers, 18K+ vehicles |
| `cn_schema.md`               | managed services    | Fleet Ops, Safety, Coaching               | 6K+ safety events/week      |
 
**Not sure which one to use?** Start with `cn_schema.md` if your prototype is about where drivers are, how they're driving, or their status. Use `cd_schema.md` if your prototype touches money&mdash;fuel spend, card limits, transaction history. Use `fx_schema.md` for a representation of a large fleet with geofences across the country.

## How to use these files
 
Each schema file contains:
 
- **Plain-English table descriptions** — what each table stores, in human terms
- **Column listings** — every field name, its data type, and whether it can be empty
- **Entity relationship summary** — how the tables connect to each other, and what to watch out for

The workflow:
 
1. Open the relevant schema file and skim the table descriptions
2. Identify which tables and columns your prototype needs
3. Paste the schema (or the relevant section) into your AI-assisted prototyping tool of choice as context
4. Describe what you want to build

The data lives in Supabase and requires two credentials to connect: a `project URL` and an `anon key`. Request both from Manny on Slack, store them in a `.env` file locally, and never commit them to any repository. Your AI-assisted prototyping tool will help you establish a connection to the anonymized, live data.
 
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

 
## Contributing, feedback, and requests

More data exists beyond what's currently in this repo. If you're prototyping something and the schemas don't have what you need, don't assume it isn't available. Reach out to Manny and we'll figure it out together. Sometimes the raw data needs to be massaged, reshaped, or optimized before it's useful for a prototype, and in those cases a Supabase database function can be created to do that work for you. And if you come across data in your own work that you think others might find useful, let's talk about adding it to Supabase and updating the schema files here so everyone benefits.

The best way to request data, report an issue, or suggest an improvement is to open a GitHub Issue. You'll find the Issues tab at the top of the repo. Click New Issue, give it a descriptive title, and include as much context as you can&mdashwhat you're trying to build, what data you need, or what looks wrong and where.

Use issues for things like:
- Requesting data — you're prototyping something and the schemas don't have what you need
- Reporting a schema error — a column is missing, a description is wrong, or a relationship doesn't match what's in Supabase
- Proposing a new dataset — you've come across data you think others would find useful

If you'd rather not open an issue or want to talk it through first, reach out to Manny on Slack!
