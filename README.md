# lexicon
Handles all the Defintions and Standards

Here's some stuff from ChatGPT

## 🧠 Lexicon Data Model Overview

This outlines the semantic and structural types used within the Lexicon module.

- **Definition**
  - `Term` – Named concept or label (e.g., "Scat", "Act", "Infrastructure")
  - `Definition` – Versioned meaning of a term (includes prose, examples, source)
  - `Alias` – Alternative names for a term
  - `Relation` – Links between terms (e.g., "is_a", "part_of")
  - `Citation` – Tracks usage of a definition in other parts of the system

- **App**
  - `App` – Bundled functionality with its own help, awards, and modules
  - `Module` – Logical subcomponent of an App
    - `HelpBlock` – Structured help documentation
    - `CommandBlock` – Defines input/output behavior
    - `SchemaBlock` – Expected structure for facts or messages
    - `ConfigBlock` – Default configuration or behavior settings

- **Origin**
  - `Origin` – External interface for an App (e.g., DiscordOrigin)
  - `OriginMeta` – Contextual metadata (e.g., user ID, platform)
  - `OriginLink` – Connection between App and Origin

- **Block**
  - `Block` – General data unit within a module (structured JSON or text)
    - `FactBlock` – Immutable record of something that happened
    - `ActionBlock` – Describes a user or system action
    - `StateBlock` – Describes current or past state

- **Bit**
  - `Bit` – Smallest meaningful unit (key-value pair, tag, or flag)
    - Example: `"type": "Scat"`
    - Example: `"status": "active"`
    - Often embedded within Blocks or Metadata

---

> Each level supports composability and extensibility across all Unum systems.
