# Glossary

*Plain-English definitions, written for the records manager rather than the developer. Some are technical, most are not.*

**Archive**
A copy of records kept for as long as retention requires, and independently of the system that produced them. Distinct from a backup, which requires the original system to be usable.

**Audit trail**
The record of who changed what, and when. Often held inside the source system rather than in a separate log, and frequently overlooked at decommission.

**Backup**
A snapshot of a system taken for operational recovery. Useful only while the system it belongs to still exists and can be restored.

**Business system**
A system used to run current operations. Distinct from a records system, which is used to preserve what happened.

**Chain of custody**
The documented sequence of who held the data, from source to archive, showing it has not been altered or misused in transit.

**Conversion code**
An instruction inside a legacy database that turns a stored value into the value a user sees. Dates, currencies, coded lookups and computed fields typically rely on them.

**Cutover**
The point at which a new system takes over from the old one. Usually described in project plans as a single day; in practice a period, and often followed by months of parallel running.

**Decommission**
Switching the old system off for good. Irreversible once the licence lapses or the hardware retires.

**Dictionary**
The description a legacy system holds of its own data — which field means what, what type it is, how to convert it. Often the piece of intellectual property most needed to make sense of an extract afterwards.

**Disposal authority**
The document, published by the state or national records office, that sets which classes of record can be destroyed and when. Retention rules tell you what to keep; the disposal authority is what turns lawful destruction into an evidenced event.

**Flat file**
Data without structure or relationships. Fine for holding a single table. Insufficient for representing the records that connect to one another — a customer, their invoices, their payments.

**Legacy system**
Any system past active development, still holding records the organisation is obliged to keep. Not a judgment about age; it is defined by the vendor's posture, not the year of installation.

**Line-of-business system**
A system supporting a specific operational function — rating, licensing, HR, payroll, works. Public sector organisations typically run several alongside a central ERP.

**MultiValue**
A family of databases that store several values in a single field. UniVerse, UniData, D3, jBASE and Pick are examples. Extracting from them into modern tools requires unpacking the multiple values into separate rows or columns.

**Open format**
A file format defined by a public specification, not owned by a single vendor. CSV, Parquet and JSON are examples. The test that matters: can the file be opened in ten years without the software that produced it.

**Orphan record**
A record whose parent has been deleted or never existed — an invoice with no customer, a payment with no invoice. Common in old data, and useful to catch during migration.

**PII (Personally Identifiable Information)**
Any information that can identify a specific individual on its own or in combination — name, address, date of birth, tax file number, employee ID paired with details, and so on. Treated with heightened obligations under most privacy legislation.

**Public record**
A record produced or received by a public sector body in the course of its work. In most jurisdictions the term has a legal definition and carries specific retention, access and disposal obligations distinct from ordinary business records.

**Read-only archive**
An archive that cannot be modified after creation, and can be shown not to have been. The default expectation for anything that may be produced in evidence.

**Reconciliation**
Proving the archive matches the source. Numbers balance, counts agree, samples check out. The evidence that "we extracted everything" is more than a claim.

**Referential integrity**
Every reference in the data actually points to something. A record without integrity holds pointers that go nowhere. Rare in modern systems, common in decades-old ones.

**Retention schedule**
The list of record classes and how long each must be kept, published by the state or national records authority. Retention is set by law, not by the vendor.

**Source system**
The original system from which the data is extracted. In archiving contexts, always the legacy one.

**UAT (User Acceptance Testing)**
The stage of a migration or system project where the customer, not the vendor, confirms that the delivered data or system behaves as expected. What sign-off is given against — and what the customer commits to when they give it.

**UniVerse**
One example of a MultiValue database, used by a number of long-established public sector ERPs. Included here because "our data is in UniVerse" is a common answer to "what system are you on", and it explains why standard tools can't read it directly.

---

*Published by [Archiva Group](https://archivahq.com). Licensed for reuse with attribution — see [LICENSE](./LICENSE).*
