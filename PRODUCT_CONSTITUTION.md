# Foldworks Product Constitution

**Version:** 1.0
**Status:** Ratified
**Ratified:** 2026-10-17

## Preamble

Foldworks is a self-hosted visual catalogue for collecting, organizing, discovering, and building paper models.

It exists because a directory full of files is not the same thing as a collection.

Paper-model collectors accumulate PDFs, PDOs, image sheets, instructions, textures, photographs, archives, variants, scans, and other material across years or decades. Filesystems can store these things, but they do not understand what those things represent.

Foldworks does.

Foldworks treats a paper model as a coherent object with identity, presentation, build information, relationships, and assets. It provides a beautiful, searchable and durable layer over a collector's library without taking ownership of that library away from them.

This Constitution defines the principles Foldworks must preserve as the project evolves.

---

## I. THE MODEL IS THE FUNDAMENTAL OBJECT

Foldworks catalogues **models, not files**.

A model may contain one file or many:

- PDF patterns
- PDO files
- instruction booklets
- image sheets
- SVGs
- textures
- reference images
- photographs
- source archives
- alternate versions
- other related assets

These files are representations or assets belonging to a model.

The product must therefore be designed around the identity and meaning of the model rather than around individual files.

---

## II. FOLDWORKS SERVES COLLECTORS AND BUILDERS

Foldworks exists for people who collect, organize, preserve, discover and build paper models.

It should work for a person with fifty models and remain useful for someone with fifty thousand.

It should accommodate carefully organized libraries and collections accumulated chaotically over many years.

Users should not need to become librarians in order to use Foldworks.

Foldworks should make organization rewarding rather than burdensome.

---

## III. THE COLLECTION SHOULD BE A PLACE WORTH EXPLORING

Organization is necessary, but organization alone is not the product.

Foldworks should make a paper-model library pleasurable to browse.

Models should be visual, recognizable and discoverable. Search and filtering should allow users to ask meaningful questions about their collections rather than merely locate filenames.

The aspiration is not simply:

> "Where is this file?"

It is:

> "What do I have?"

> "What could I build?"

> "What have I forgotten about?"

> "Show me the models that fit what I want to build today."

A successful Foldworks library should feel less like browsing a filesystem and more like exploring a personal museum, workshop and catalogue.

---

## IV. PDO IS PROGRESSIVE ENHANCEMENT

Pepakura PDO is important to paper modelling and Foldworks should ultimately understand the format deeply.

PDO support may enable capabilities unavailable to simpler formats, including extracted metadata, textures, geometry, unfolded layouts, automatic renders and interactive visualization.

But **PDO does not define Foldworks.**

A PDF-only model is a first-class model.

An image-sheet model is a first-class model.

A scanned model is a first-class model.

A model whose format Foldworks only partially understands is still a first-class model.

PDO enriches the experience when available.

Its absence must never impoverish the fundamental experience.

---

## V. MISSING KNOWLEDGE IS ALLOWED

Foldworks must remain useful when metadata is incomplete, ambiguous or wrong.

Unknown designer?

Allowed.

Unknown scale?

Allowed.

No cover image?

Allowed.

Automatic identification failed?

Allowed.

The user must always be able to inspect, organize and edit a model manually.

Automation exists to reduce labour, not to make the user dependent upon successful automation.

Foldworks should gracefully represent uncertainty rather than invent certainty.

---

## VI. THE USER OWNS THE LIBRARY

The user's models belong to the user.

The user's files belong to the user.

The user's metadata belongs to the user.

The user's organizational work belongs to the user.

Foldworks must never deliberately trap those things inside Foldworks.

Where practical, self-hosted Foldworks should work with ordinary, understandable user-owned files and directories.

Foldworks may manage storage where appropriate, particularly in hosted environments, but storage management must never become ownership.

Users must be able to export their data and leave.

If Foldworks disappears tomorrow, a user's collection should remain recoverable, intelligible and useful.

**Foldworks must never hold a collection hostage.**

---

## VII. FOLDWORKS IS OPEN SOURCE

Foldworks will be open-source software.

There will not be a deliberately crippled "Community Edition" whose purpose is to withhold useful application features from people who self-host.

Self-hosted Foldworks is Foldworks.

The exact software license will be selected separately, but the license must be compatible with the project's commitment to genuine self-hosting, community participation and long-term user autonomy.

---

## VIII. FOLDWORKS CLOUD SELLS OPERATIONS, NOT ARTIFICIAL SCARCITY

Foldworks Cloud will exist for users who want Foldworks without operating Foldworks.

Cloud customers may pay for:

- computing
- storage
- backups
- upgrades
- monitoring
- infrastructure
- support
- convenience

They will not pay merely to unlock application features intentionally withheld from self-hosted users.

The commercial proposition is simple:

**Foldworks:** your server, your files, your responsibility.

**Foldworks Cloud:** the same Foldworks, operated for you.

A Cloud customer must be able to export their library and become a self-hosted user.

---

## IX. MULTI-USER FOLDWORKS IS STILL FOLDWORKS

Multi-user capability is not a premium Cloud feature.

Families, clubs, schools, makerspaces, design teams and other groups may legitimately want shared libraries on their own infrastructure.

Foldworks should therefore distinguish between **users** and **libraries**.

Users may belong to libraries.

Libraries contain models and their associated organizational data.

The architecture should preserve this distinction early enough that multi-user support can grow naturally from the product.

But Foldworks must not burden its earliest useful versions with unnecessary SaaS infrastructure.

**Tenant awareness early. SaaS complexity later.**

---

## X. THE FILESYSTEM IS NOT THE ENEMY

Foldworks should understand existing collections rather than demand that existing collections conform to Foldworks.

Good directory structures may be encouraged.

They must not be prerequisites.

Foldworks should be capable of discovering useful structure in imperfect libraries while allowing users to improve that structure gradually.

The guiding principle is:

**Understand disorder. Encourage organization. Never require unnecessary reorganization merely to satisfy Foldworks.**

---

## XI. AI ASSISTS; HUMANS REMAIN RESPONSIBLE

Foldworks is intentionally being built with substantial assistance from generative AI.

This is part of the project, not something to conceal.

AI may contribute to:

- research
- architecture
- implementation
- testing
- documentation
- review
- analysis
- automation

But "built with AI" does not mean "generated by a prompt."

Human judgment remains responsible for product direction, acceptance, verification and ownership.

AI-generated implementation must be tested.

AI-generated claims must be questioned.

AI failures should be documented rather than hidden.

Domain expertise remains essential.

---

## XII. FOLDWORKS IS AN EXPERIMENT IN BOUTIQUE SOFTWARE

Foldworks tests a broader hypothesis:

**AI may make domain knowledge executable.**

Software development has historically required enough potential economic return to justify substantial engineering organizations and development costs.

That leaves many small communities underserved.

Foldworks asks whether AI-assisted development can lower that threshold enough for individuals and very small teams to create excellent software for niches previously considered too small to justify it.

Paper modelling is deliberately such a niche.

The project will therefore document not only the software produced, but the process used to produce it.

Successes matter.

Failures matter.

Human time matters.

AI costs matter.

Mistakes matter.

Corrections matter.

The experiment should be documented honestly enough that others can learn from it.

---

## XIII. THE REPOSITORY IS THE PROJECT'S INSTITUTIONAL MEMORY

Conversations are workshops.

The repository is the record.

Important product decisions must eventually become durable project artifacts:

- specifications
- architecture documents
- ADRs
- tests
- documentation
- code

No critical architectural or product principle should depend indefinitely upon the memory of a human or an AI conversation.

AI-specific instruction files must point toward shared canonical documentation rather than becoming competing sources of truth.

---

## XIV. BUILD THE SMALLEST COMPLETE EXPERIENCE

Foldworks should not attempt to implement its entire vision simultaneously.

The first meaningful version should prove one complete workflow exceptionally well:

Install Foldworks.

Create an account.

Import an ordinary paper model.

Generate an attractive presentation.

Edit its metadata.

Browse it.

Open it.

Access its original assets.

Find it again through search.

Only after that experience works well should Foldworks aggressively expand into deeper format intelligence, collection-scale automation, multi-user functionality and hosted infrastructure.

**Build one excellent vertical slice before building everything.**

---

## XV. DO NOT SOLVE SUCCESS BEFORE SUCCESS EXISTS

Foldworks should be architected responsibly without designing imaginary infrastructure for imaginary millions of users.

Preserve important future possibilities.

Avoid unnecessary future complexity.

Security, data integrity and migration paths require foresight.

Hypothetical scale does not justify premature engineering.

When Foldworks actually encounters scaling problems, Foldworks may solve them using evidence.

---

## XVI. THINGS FOLDWORKS REFUSES TO BECOME

Foldworks will not become:

**A proprietary prison.**
Users must be able to leave with their data.

**A crippleware funnel.**
Self-hosting will not exist merely to advertise features available only in a paid edition.

**A PDO-only catalogue.**
PDO is enhancement, not admission criteria.

**A glorified filesystem browser.**
Foldworks understands models and collections, not merely filenames.

**An AI dependency.**
Core organization must remain possible when automatic identification or external AI services are unavailable.

**A metadata bureaucracy.**
Users should not need perfect records before they can enjoy their collections.

**A replacement for Pepakura Designer.**
Foldworks may deeply understand PDO without attempting to become a complete arbitrary 3D unfolding and editing application.

**A SaaS architecture experiment disguised as a papercraft application.**
The useful product comes first.

**A platform that owns the user's collection.**
Foldworks exists to serve the collection and its owner, not the reverse.

---

## XVII. THE STANDARD FOR FUTURE DECISIONS

When a future product, design, architecture or business decision is unclear, ask:

1. Does this treat the model rather than the file as the primary object?
2. Does this preserve an excellent experience without PDO?
3. Does this preserve user ownership and portability?
4. Can the user recover from automation being wrong?
5. Does this work for self-hosted Foldworks without artificial feature restrictions?
6. Does this preserve the path toward legitimate multi-user use?
7. Are we solving a real problem or an imagined future problem?
8. Does this make the collection more useful or enjoyable?
9. Can this decision be documented, tested and maintained?
10. Would we still consider this respectful of the user if Foldworks ceased to exist tomorrow?

If a proposed direction repeatedly fails these tests, it probably does not belong in Foldworks.

---

## Closing Principle

Foldworks exists to turn a directory of paper-model files into a collection that can be understood, explored, preserved and enjoyed.

The software should be powerful without becoming possessive, intelligent without becoming indispensable, and ambitious without losing sight of the people whose collections it exists to serve.

**The collection belongs to the user.**

**The model is the object.**

**The software serves both.**