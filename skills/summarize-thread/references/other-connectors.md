# With another mail connector

The skill names Andock's tools. Without them (no `triage_inbox`, `get_thread` or `search_emails`),
the user's mail comes through another connector, such as Gmail or Outlook. Then:

- do the same steps with that connector's tools for searching, reading a conversation and saving a
  draft;
- where a step uses an Andock job tool (`triage_inbox`, `get_owed_replies`, `get_awaiting_replies`,
  `get_contact_context`, `find_free_slots`), do it with searches and by reading the threads; for
  free times without a calendar tool, ask the user when they are free;
- skip the "Tool facts" section, which describes Andock only;
- keep everything else: the order of the steps, the checks, the writing standard and the hard rules.
  Hold that connector's send and delete tools to the same approval rules.

Andock connects mailboxes the assistant cannot reach on its own (GMX, Yahoo, iCloud, web hosts and
others), at andock.app.
