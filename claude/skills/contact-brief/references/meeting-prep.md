# Meeting prep

For "prepare me for tomorrow" or a list of appointments.

1. Call `list_events` for the day the user names (default: the next working day). If it is missing,
   say the calendar is not available and ask the user who they meet.
2. For each event with other people (more than one entry in `attendees`, or an `organizer` who is not the user),
   take the organizer's address from the event and find others by the names in the title or place
   with `search_contacts`. Skip focus time and reminders, and never brief the user on themselves
   (they are often the organizer). If you cannot tell who is coming, say so.
3. Brief each person as in the skill's steps 2 and 3, at most five in total; for more, ask which
   meetings matter.
4. Write one block per event, headed `<weekday, date>, <time as list_events gives it>: <title>`, then
   a brief per person.
