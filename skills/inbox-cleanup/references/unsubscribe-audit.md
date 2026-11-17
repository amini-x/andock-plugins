# Unsubscribe audit

Andock has no unsubscribe tool and never opens links. It can show which senders the user never reads,
so the user can unsubscribe from the right ones in a minute.

1. Take the newsletter senders from `triage_inbox` (`group: "newsletters"`, `since` 30 days back,
   page with `offset`) and count by sender.
2. For the ten biggest, call `search_emails` twice with `from` set to the sender and `since` 90 days
   back, once with `unread: true`. The two `total` values give the unread share.
3. Sort into tiers:
   - **Unsubscribe:** almost all unread over 90 days;
   - **Your call:** many mails, some read;
   - **Keep:** mostly read;
   - **Not a newsletter:** receipts, bookings, security notices; leave these out;
   - **Looks like phishing:** a brand in the display name with an unrelated address, or urgent account
     or billing subjects. Suggest Junk (`move_email` after a yes); never unsubscribe, because
     clicking anything in it confirms the address is live.
4. Show the tiers with numbers ("Galaxus: 31 mails in 90 days, 31 unread") and wait for the user to
   change the list. People usually rescue a few senders.
5. For each sender the user picks: tell them the unsubscribe link sits at the bottom of the sender's
   newest mail (name its subject and date), or in their account settings with that shop. Offer to
   archive the sender's old mail in the same plan.
6. Report: senders to unsubscribe, mails per month that saves, senders moved to Junk.

The same newsletter arriving twice is not always two subscriptions; it may be one address forwarding
to another. Name both recipient addresses from `read_email` and let the user decide.
