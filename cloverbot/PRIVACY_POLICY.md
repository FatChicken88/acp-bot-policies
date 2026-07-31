# Privacy Policy — Clover Bot

**Effective date:** 31 July 2026
**Last updated:** 31 July 2026

This policy explains what data Clover Bot ("the Bot"), operated by `[OPERATOR NAME]` ("we", "us", "our"), collects, why, and how long we keep it. It applies to everyone who uses the Bot or is present in a Discord server where the Bot is installed.

The Bot is an independent project and is not affiliated with or endorsed by Discord Inc.

## 1. Summary

The Bot stores **numeric Discord IDs and virtual point records** — nothing more. It does not store the text of your messages, your username, your email address, your IP address, or your avatar. Everything it stores is scoped to the specific Discord server it was recorded in.

## 2. Data We Store

All data is stored in a PostgreSQL database. The complete set of stored fields is:

| Table | Fields stored | Purpose |
|---|---|---|
| `clover_totals` | Discord user ID, server ID, current balance, lifetime total, timestamps | Track each member's clover balance |
| `transactions` | Discord user ID, server ID, shop item ID, purchase date | Record shop purchases and enforce per-item limits |
| `rank_up_history` | Discord user ID, server ID, ID of the staff member who performed the promotion, previous rank name, new rank name, cost, timestamp | Audit log of rank purchases |
| `reaction_counts` | Discord user ID, server ID, message ID, reaction timestamp | Count participation in reaction-based events without double-counting |
| `shop_items` | Server ID, item name, price, active flag, purchase limit, timestamps | Server-defined shop catalogue (contains no personal data) |
| `rankups` | Server ID, rank names, cost | Server-defined rank pricing (contains no personal data) |

Discord user IDs and server IDs are public numeric identifiers ("snowflakes") that Discord assigns to every account and server. Under data-protection laws such as the GDPR, a user ID is treated as personal data because it identifies you, which is why this policy covers it.

## 3. Data We Do Not Store

The Bot never writes any of the following to its database:

- **Message content.** The Bot does not request Discord's Message Content privileged intent. It receives the text of a message only when that message directly mentions the Bot, uses it to determine which command you invoked, and discards it. Ordinary conversation in your server is never visible to the Bot.
- **Usernames, nicknames, discriminators, or avatars.** These are fetched live from Discord's API when the Bot needs to display a leaderboard or check a permission, and are never written to the database.
- Email addresses, phone numbers, real names, IP addresses, or payment details
- Direct messages, voice data, or attachments
- Any data from servers the Bot has not been added to

## 4. Discord Permissions and Intents

The Bot requests the following Discord gateway intents:

| Intent | Privileged | Why |
|---|---|---|
| Guilds | No | Basic server and channel information |
| Guild Members | **Yes** | Resolve members and their roles to enforce command permissions and assign rank roles |
| Guild Emojis and Stickers | No | Render emoji correctly in responses |
| Guild Messages | No | Receive command messages that mention the Bot |
| Guild Message Reactions | No | Count reactions for participation events |

The Bot does **not** request the Message Content or Presence intents.

## 5. Why We Process This Data

We process this data solely to operate the features described in the [Terms of Service](./TERMS_OF_SERVICE.md): maintaining balances, displaying leaderboards, processing shop and rank purchases, counting event participation, and enforcing staff-only command permissions.

Where the GDPR applies, our lawful basis is **legitimate interest** — operating a points system that a server and its members have chosen to use. You may object to this processing at any time by asking for your data to be deleted (see section 8).

## 6. How Data Is Shared

We do not sell, rent, or trade your data, and we do not use it for advertising, profiling, or analytics.

Data is disclosed only in these circumstances:

- **Within your Discord server.** Balances, leaderboard positions, purchases, and rank changes are shown in Discord channels, so other members of that server can see them. Staff-only commands such as the transaction log are visible to server staff.
- **Our hosting provider.** The Bot and its database run on Heroku (a Salesforce company), which stores the data on our behalf as a processor.
- **Legal obligation.** If required by valid legal process.

## 7. Retention

We keep data for as long as the Bot is installed in your server and the record remains relevant:

- Balances persist until changed by server staff or cleared with the `clearclovers` command
- Transaction records persist until cleared with the `cleartransactions` command
- Rank-up history and reaction counts persist as an audit trail until deleted on request

If the Bot is removed from a server, remaining records for that server are deleted on request. Backups held by our hosting provider may retain deleted data for a short period before being overwritten.

## 8. Your Rights

You may request:

- **Access** — a copy of the records we hold for your Discord user ID
- **Deletion** — removal of all records associated with your Discord user ID
- **Objection or restriction** — that we stop processing your data

To make a request, contact `[CONTACT EMAIL]` and include your Discord user ID and the server concerned. We will respond within 30 days. We may ask you to verify control of the account, since a user ID alone does not prove identity.

Note that deleting your data resets your clover balance, purchase history, and rank history in that server, and this cannot be undone. Server staff may also delete records directly using the Bot's own commands.

Depending on where you live, you may also have the right to lodge a complaint with your local data-protection authority.

## 9. Children

The Bot is not directed at children under 13, or under the minimum age required by Discord in your country. We do not knowingly collect data from anyone below that age. If you believe we hold data for such a user, contact us and we will delete it.

## 10. Security

Data is transmitted over encrypted connections and stored in a database that is not publicly accessible. No system is perfectly secure, and we cannot guarantee absolute security. In the event of a breach affecting user data, we will notify affected servers and, where legally required, the relevant authority.

## 11. International Transfers

Our hosting provider's infrastructure may be located in the United States or the European Union. Using the Bot may therefore involve transferring your Discord user ID outside your country of residence.

## 12. Changes to This Policy

We may update this policy. Material changes will be reflected in the "Last updated" date above and, where practical, announced in servers using the Bot.

## 13. Contact

Questions, or access and deletion requests: `[CONTACT EMAIL]`
