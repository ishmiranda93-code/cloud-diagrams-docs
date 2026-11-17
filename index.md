---
---

# Cloud Diagrams for Confluence — Documentation


Cloud Diagrams adds one macro to Confluence Cloud. You write a diagram as text (Mermaid syntax); it renders instantly, entirely in your browser. Nothing is sent to any server — the diagram source lives only in your page, in the macro's settings.


## Add a diagram


1. Edit a page, type /Cloud Diagrams, and pick the macro.
2. The editor opens with a working example already in place. Write or paste Mermaid code and watch the preview update as you type.
3. Save the macro, then publish the page. Readers see the rendered diagram.
## Diagram types

- **Architecture** (architecture-beta) — cloud architecture with service icons.
- **Flowchart** (flowchart) — processes and decisions.
- **Sequence** (sequenceDiagram) — interactions over time.
- **Class** (classDiagram) — data models and object structures.
## Cloud icons (architecture diagrams)

In an architecture-beta diagram, reference icons as logos:<name>:

```
architecture-beta
  service gw(logos:aws-api-gateway)[API Gateway]
  service fn(logos:aws-lambda)[Orders Lambda]
  service db(logos:aws-dynamodb)[Orders Table]
  gw:R --> L:fn
  fn:R --> L:db
```

Icon coverage in this version: **64 AWS service icons** (API Gateway, Lambda, S3, EC2, RDS, DynamoDB, SQS, CloudFront, and more), **Google Cloud** (Cloud Run, Cloud Functions, Google Cloud), and the **Microsoft Azure** mark. Icons render from files bundled with the app — no internet connection is used.

## Privacy and security

- The app has **no backend and no storage of its own**; it cannot see, copy, or transmit your diagrams.
- Rendering happens locally in the reader's browser; diagram text is stored only in your Confluence page.
- The app requests **no Confluence permissions** and makes **no external network connections**.
## Troubleshooting

- **Red error box instead of a diagram:** the Mermaid syntax has an error — edit the macro and check brackets and arrows; the message names the problem line where Mermaid reports one.
- **An icon shows as a generic box:** the icon name isn't in the bundled set — check the spelling against the coverage list above.
- **Diagram looks stale:** reload the page; rendering is done fresh in your browser on every view.
## Support

Contact Forge Studio via the Atlassian Marketplace listing for Cloud Diagrams for Confluence. Response target: 2 business days.

Privacy policy: [Privacy Policy](privacy.html)
