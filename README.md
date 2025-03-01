
## What are we doing?

We’re adding a feature to our social media app that lets users:

1. Enter their birthday when they log in.
2. Show their birthday on their profile page for others to see.

This means users can type in their birth date (like month, day, and year), and then it’ll appear on their profile, like “Birthday: March 15, 1995,” if they want it shown.

## Why are we doing it?

We want to make our app more fun and personal. Birthdays are a big deal. People like celebrating them, and friends like knowing when to say “Happy Birthday!” By letting users add and show their birthdays:

- It helps users feel more connected to their friends.
- It gives people a reason to interact more (like posting birthday wishes).
- It makes profiles feel more complete and human.

Other social apps do this, and users expect it. Plus, it’s a simple way to make our app stickier. People might log in more around their birthday.

## How are we doing it?

Here’s the plan to build this:

1. **Collecting the Birthday:**
    - When a user signs up for the first time, we need to show a one-time pop-up asking, “When’s your birthday?” with fields for month, day, and year (e.g., dropdowns or a calendar picker).
    - They can skip it if they don’t want to add it now (like a “Maybe Later” button).
    - We’ll save this data in their account securely, tied to their user ID.
2. **Displaying the Birthday:**
    - On their profile page, we’ll add a new line under their bio (or wherever it fits) that says “Birthday: [Month] [Day], [Year]” (e.g., “Birthday: March 15, 1995”).
    - Users can choose if it’s public (everyone sees), private (only they see), or friends-only via a privacy toggle in settings.
    - If they don’t add a birthday, nothing shows up—no empty “Birthday: N/A” or anything awkward.
3. **Technical Stuff:**
    - Store the birthday as a date field in our database (e.g., YYYY-MM-DD format, like 1995-03-15).
    - Add a settings page option: “Show my birthday” with checkboxes for “Day and Month” and “Year” (so they can hide their age if they want).
    - Make sure it works on both mobile and web versions of the app.
4. **Edge Cases to Handle:**
    - **Young Users:** If someone enters a birthday that makes them under 13, block them from saving it and show a message: “You need to be 13+ to use this app per our rules.”
    - **Weird Dates:** If they pick something impossible (like a future date), show an error: “That’s not a real birthday—try again.”
    - **Time Zones:** Use the user’s local time zone for display (e.g., if they’re in Japan, it’s their March 15, not someone else’s).
    - **Updates:** Let users change their birthday later in settings, but limit it to once every 6 months so they don’t mess around too much.
    - **No Year:** If they only want to share month and day (e.g., “March 15”), allow that and just skip the year in the display.