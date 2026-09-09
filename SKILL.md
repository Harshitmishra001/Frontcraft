# SKILL.md — Website Development: UI/UX, Frontend Engineering, and Quality

## Purpose

Build websites and web applications that are understandable, usable, accessible, visually coherent, distinctive, technically sound, and genuinely functional.

This skill is not a prompt for producing attractive screenshots. It is an operating guide for an AI agent that must make design decisions, implement them, verify the rendered result, and correct failures.

The core principle is:

> Design for human understanding and user outcomes, not for maximum information density or screenshot aesthetics.

A successful implementation is one where the visual design, content hierarchy, interactions, real data, accessibility, responsive behavior, and engineering implementation reinforce the same product goal.

---

## Scope

Use this skill when creating, redesigning, or substantially modifying:

- Marketing websites
- SaaS applications
- Dashboards
- Internal tools
- Developer tools
- Research/workspace applications
- Data-heavy interfaces
- CRUD applications
- Document interfaces
- AI/ML applications
- Multi-page websites
- Responsive web applications

The skill covers product-oriented UI/UX, frontend implementation, content hierarchy, interaction design, accessibility, responsive design, performance considerations, real-data integration, visual QA, and final validation.

It does not replace a project's backend architecture, domain-specific engineering practices, security review, or legal/compliance requirements. It should work alongside those systems.

---

# 1. Operating Principles

## 1.1 Understand before designing

Before changing an existing product, establish what the product actually does and what must remain true.

Inspect the available project context:

- Existing frontend and routes
- Existing backend/API behavior
- Existing data model
- Existing components
- Existing design system, if any
- Existing user workflows
- Existing state and error handling
- Existing assets and content
- Existing constraints
- User requirements
- Reference screenshots or designs, if supplied

Do not invent missing product behavior merely to make the interface look complete.

For an existing application:

> Existing working functionality is the source of truth for what the product does. The redesign is the source of truth for how that functionality is presented.

Do not replace a working core pipeline, domain model, or workflow solely because a generic UI pattern would be easier to build.

## 1.2 Design around user goals

Do not start with a component inventory such as "dashboard, cards, charts, sidebar."

Start with:

> User goal → workflow → information needed → decision/action → interaction → visual presentation → components.

A component is justified because it helps a user accomplish something, not because the component is common in generated interfaces.

## 1.3 Design for the audience

Visual and interaction choices should be appropriate for the intended users and their environment, not merely the designer's taste.

Consider:

- Who is using the product?
- What are they trying to accomplish?
- What do they already know?
- How much attention do they have available?
- Are they scanning, comparing, reading deeply, creating, editing, or monitoring?
- What mistakes are likely?
- What information must be trusted?
- What constraints exist on their device or environment?

When audience information is not provided, infer cautiously from the product itself and label major assumptions internally rather than treating guesses as facts.

## 1.4 Optimize for outcomes, not screenshots

A visually polished interface that makes the user's task harder is not a successful design.

For marketing/conversion experiences, reduce friction toward the intended action.

For applications/tools, reduce friction toward task completion, understanding, investigation, creation, or decision-making as appropriate to the product.

The right question is not:

> Does this screen look impressive?

It is:

> Does this screen help the intended user accomplish the intended task clearly and efficiently?

## 1.5 Human comprehension beats information density

Do not try to display every available piece of information at once.

A long, scrollable interface is acceptable. Separate screens are acceptable. Progressive disclosure is acceptable. Accordions, drawers, detail views, tabs, and secondary navigation are acceptable when they improve comprehension.

Prefer:

> Primary information → supporting context → deeper detail

over:

> Everything simultaneously → tiny text → many cards → many badges.

The interface should make the most important information obvious without requiring the user to decode every element.

---

# 2. Evidence and Truthfulness Standard

This skill prioritizes trustworthy interfaces, especially for data-driven, document, analytics, AI, and research applications.

## 2.1 Never fabricate product evidence

Do not fabricate:

- Data
- Counts
- Metrics
- Facts
- Search results
- Documents
- Evidence
- Relationships
- Confidence values
- User activity
- Statuses
- Processing progress
- Analytics
- Testimonials
- Product capability
- Source excerpts
- Reasoning

Use real application data wherever it exists.

When real data is unavailable, choose one of these honest states:

1. Show an explicit empty state.
2. Show a loading state while real data is being retrieved.
3. Show an unavailable/not-supported state.
4. Create a clearly labeled demo/fixture mode only when the project explicitly needs one.

Never make fabricated content look like production data.

## 2.2 Evidence should retain meaningful context

When presenting a source, evidence, search match, code excerpt, document passage, or other grounded information, show enough surrounding real context for a human to understand and verify it.

Do not isolate a relevant sentence when the meaning depends on surrounding text.

For document interfaces, prefer:

> section/heading → surrounding text → highlighted evidence → surrounding text

Use the actual source content from the existing document/data pipeline. Do not generate plausible surrounding text to make a prototype look realistic.

## 2.3 Distinguish facts, inference, uncertainty, and provenance

When the product contains machine-generated analysis or derived information, the UI should distinguish what is directly sourced from what is inferred or uncertain.

Do not visually present generated reasoning as a primary source fact.

Use the product's actual confidence/uncertainty model if one exists. Do not invent numerical confidence just because a UI template has a confidence field.

## 2.4 Honest limitations are part of good UX

If the product cannot determine something, say so.

A smaller, honest capability is better than a polished fake capability.

This applies especially to AI products, extraction systems, search systems, recommendation systems, and prototypes.

---

# 3. Visual Hierarchy

Visual hierarchy is a primary design mechanism.

Do not assume users follow one universal scanning pattern. The video source used for this skill explicitly rejects treating the F-pattern as a universal law and recommends visual hierarchy instead. The practical rule is to deliberately guide attention by making important information more visually prominent and allowing less important information to recede.

## 3.1 Establish hierarchy before styling

Before selecting colors or components, answer:

- What is the single most important thing on this screen?
- What should the user notice second?
- What can be ignored initially?
- What needs to be visible now?
- What can be revealed later?
- What is evidence versus interpretation?
- What is an action versus passive information?

Then establish hierarchy using:

- Size
- Weight
- Position
- Spacing
- Contrast
- Typography
- Color
- Grouping
- Whitespace

## 3.2 Do not emphasize everything

If every component is bold, colored, bordered, elevated, and badge-heavy, hierarchy collapses.

Use visual emphasis sparingly.

> If everything is visually loud, nothing is visually important.

## 3.3 Primary actions

Primary actions should be visually distinguishable from surrounding content and secondary actions.

Use strong contrast and clear labels where appropriate.

Do not assume every primary action needs the largest button on the page. The correct prominence depends on the task.

Outlined/ghost buttons are not universally forbidden; they should be used only where their secondary priority remains obvious and accessible.

---

# 4. Layout and Information Architecture

## 4.1 Start from task structure

Choose layouts based on what the user needs to do.

Possible structures include, where appropriate:

- Single-column reading flow
- Two-column detail/source workspace
- Three-column investigation workspace
- List/detail split view
- Form workflow
- Step-by-step flow
- Search/results/detail
- Timeline
- Table/detail
- Canvas/workspace

Do not default to a dashboard layout merely because the application contains data.

## 4.2 Above-the-fold is not a hard requirement

Do not cram important information above the fold.

Scrolling is normal.

Allow the page to breathe and use progressive disclosure where deeper information exists.

## 4.3 Use whitespace as a hierarchy tool

Whitespace is not wasted space.

Use it to separate concepts, establish priority, and reduce cognitive load.

Do not compress sections solely to display more information at once.

## 4.4 Avoid card-everything layouts

Do not automatically put every section, metric, fact, paragraph, or action into a rounded card.

Use a mixture of:

- Open layouts
- Sections
- Dividers
- Columns
- Lists
- Tables
- Panels
- Typography
- Subtle backgrounds
- Cards where grouping genuinely benefits comprehension

Cards are a component, not an information architecture.

---

# 5. Scannability and Content Design

The video source emphasizes scannability. The broader principle is that users should be able to identify useful information quickly before deciding what to read deeply. Nielsen Norman Group similarly describes scanning as common behavior on web pages and recommends meaningful headings and concise structure. Treat these as evidence-informed design guidance, not an absolute law for every product or audience.

## 5.1 Make important content easy to find

Use:

- Meaningful headings
- Clear labels
- Short paragraphs when possible
- Strong first sentences
- Structured lists when appropriate
- Highlighted important terms when useful
- Consistent alignment
- Predictable information grouping

## 5.2 Do not over-explain in the interface

The interface should communicate primarily through structure and hierarchy.

Do not fill screens with explanatory prose simply because the model has more information available.

Expose deeper explanation when the user needs it.

## 5.3 Content should match user intent

Marketing pages, analytical tools, forms, dashboards, research environments, and CRUD applications have different content needs.

Do not apply a landing-page copywriting model to an operational application, or a data-table model to a storytelling page.

---

# 6. Typography

Typography is an information hierarchy mechanism, not decoration.

## 6.1 Establish a type scale

Define roles for:

- Display/title
- Page heading
- Section heading
- Subheading
- Body
- Metadata
- Labels
- Controls
- Captions
- Code/data where appropriate

Use semantic HTML headings where appropriate and keep the visual hierarchy consistent with the document structure.

## 6.2 Prioritize body readability

Do not use decorative or display-oriented fonts for long-form body text when doing so harms readability.

Choose typefaces appropriate to:

- Audience
- Product character
- Reading length
- Data density
- Platform support

## 6.3 Avoid tiny text as a layout repair

If information does not fit, first reconsider:

- hierarchy
- content amount
- progressive disclosure
- layout
- whitespace

Do not repeatedly reduce font size to rescue an overloaded composition.

## 6.4 Pair fonts intentionally

A serif/sans pairing can create hierarchy and personality, but it is not mandatory. A single well-chosen family may be better for some products.

Do not choose fonts because they are fashionable; choose them because they serve readability and the intended visual identity.

---

# 7. Color and Contrast

## 7.1 Build a color system

Do not choose colors independently per component.

Define semantic roles such as:

- Background
- Surface
- Primary text
- Secondary text
- Border/divider
- Primary action
- Secondary action
- Success
- Warning
- Error
- Informational accent

The visual system should remain coherent across states and screens.

## 7.2 Use the 60/30/10 rule as a heuristic, not a law

The video source recommends the 60/30/10 rule as a useful starting principle: roughly 60% dominant/base color, 30% brand color, and 10% accent.

Treat this as a heuristic only. Do not force the proportions when the product benefits from another distribution.

## 7.3 Accessibility comes before aesthetics

Validate contrast rather than relying on visual intuition.

WCAG 2.2 Level AA Success Criterion 1.4.3 specifies a minimum contrast ratio of 4.5:1 for normal text and 3:1 for large text, subject to the documented exceptions. citeturn413188search1turn413188search5

Do not use color alone to communicate important state distinctions. Pair color with text, shape, iconography, position, or another distinguishable cue.

## 7.4 Restraint beats color noise

Do not turn every status into a different bright color.

Color should direct attention and encode meaning, not compensate for weak layout hierarchy.

---

# 8. Distinctive Design and Anti-Pattern Control

The agent must actively avoid the visual patterns that make generated interfaces look generic.

## 8.1 Common anti-patterns

Do not default to:

- Generic dark navy + purple AI dashboard
- Purple/blue gradients everywhere
- Glowing borders
- Excessive glassmorphism
- Giant rounded cards
- KPI strips for applications that do not need KPIs
- Excessive pills/badges
- Tiny uppercase micro-labels for everything
- Every section inside a card
- Every action as a large colored button
- Random decorative charts
- Robot/AI illustrations for AI products without a real product reason
- Sparkles/glows purely as decoration
- Excessive shadows
- Generic sidebar + dashboard template without product justification
- Copying a recognizable product's design
- Placeholder skeletons presented as real content

## 8.2 Do not confuse "modern" with decorative effects

A modern interface can be:

- restrained
- editorial
- technical
- warm
- dense-but-readable
- minimal
- expressive

Modernity should come from composition, typography, interaction, proportion, and clarity more than visual effects.

## 8.3 Create product-specific identity

A distinctive design should emerge from the product's actual concepts.

Ask:

> What is unique about this product, and how can that uniqueness influence the visual language?

For a document investigation tool, this could be evidence/provenance/context.

For a scheduling product, it might be time and availability.

For a map product, it might be spatial relationships.

Use the product's domain to avoid generic dashboards.

---

# 9. Reference-Image Mode

When the user provides a screenshot or visual reference, first determine whether it is:

- Inspiration
- A broad style reference
- An exact visual specification

If the user asks for an exact reproduction, treat the reference as the visual specification rather than merely an inspiration source.

Match as closely as technically practical:

- Overall composition
- Layout proportions
- Column structure
- Alignment
- Spacing
- Typography character
- Font scale
- Surface treatment
- Colors
- Border treatment
- Component sizes
- Visual density
- Hierarchy
- Scroll behavior

Do not replace the reference with the agent's preferred design.

At the same time, replace any illustrative data from the reference with the application's real dynamic data. The reference specifies appearance; the application specifies behavior and content.

After implementation, render the application and compare it visually against the reference. Fix discrepancies rather than assuming that approximate visual similarity is sufficient.

If the user asks for inspiration instead of reproduction, do not clone the reference. Derive principles and create an original design.

---

# 10. Functional UI: HTML Must Have Behavior

Every user-facing interactive element must be connected to real behavior or intentionally represented as unavailable/non-interactive.

Never create HTML controls and forget the behavior layer.

## 10.1 Functional-element rule

For every functional HTML element created, identify its behavioral implementation.

Examples:

- Search field → search handler/module
- Upload control → upload handler/module
- Filter → filter state/handler
- Sort control → sort logic
- Pagination → navigation/state logic
- Modal trigger → modal open/close logic
- Tabs → tab state and content switching
- Accordion → expansion state
- Form → validation and submission logic
- Delete button → delete action and confirmation logic
- Save button → persistence logic
- Navigation → actual route/navigation behavior
- Document control → actual document/page action
- Relationship control → actual relationship inspection

## 10.2 JavaScript-file requirement

For plain HTML/CSS/JavaScript implementations, create a relevant JavaScript file/module for every meaningful functional surface rather than creating HTML controls with no corresponding behavior implementation.

Examples:

```text
search.html
search.js

upload.html
upload.js

document-viewer.html
document-viewer.js

filters.html
filters.js
```

The file does not need to contain unfinished fabricated logic. It should establish the correct behavioral ownership and leave explicit, clear extension points for the real implementation.

For framework-based applications, behavior may live in the framework's component/module structure, but the responsibility must still be identifiable and traceable. Do not create decorative controls with no behavioral owner.

## 10.3 No dead controls

A button should either:

1. Work.
2. Be intentionally disabled with a truthful explanation.
3. Be a non-interactive visual element that is not presented as a control.

Do not leave fake navigation links, tabs, filters, buttons, or dropdowns merely because they look good.

## 10.4 Verify interactions

After implementation, test important controls instead of only checking that they render.

The minimum audit should cover:

- Navigation
- Primary CTAs
- Forms
- Search
- Filters
- Tabs
- Modals/drawers
- Pagination/infinite loading
- Uploads
- Expand/collapse interactions
- Document/evidence controls
- Error/retry paths

---

# 11. Semantic HTML and Native Behavior

Use the correct HTML element for the user's intended interaction.

MDN recommends semantic HTML because browsers provide built-in accessibility and behavior for appropriate elements. For example, a real `<button>` provides native keyboard accessibility that a clickable `<div>` does not. citeturn413188search0turn413188search2turn413188search3

Prefer:

- `<button>` for actions
- `<a href="...">` for navigation
- `<form>` for forms
- `<label>` for form controls
- Correct heading hierarchy
- `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>` when semantically appropriate
- Lists for lists
- Tables for tabular data
- Native inputs where suitable

Do not use `<div>` elements as buttons merely for styling convenience.

Do not use `href="#"` or JavaScript pseudo-links where a real button is appropriate. MDN notes that these approaches can create unexpected browser and accessibility behavior. citeturn413188search0turn413188search3

---

# 12. Accessibility

Accessibility is part of implementation, not a polish step.

At minimum, consider:

- Semantic HTML
- Keyboard access
- Visible focus states
- Accessible labels
- Form labels and validation
- Meaningful link/button text
- Text alternatives for informative images
- Logical source order
- Sufficient contrast
- Non-color-only state communication
- Appropriate focus management in overlays
- Resizable text
- Responsive content

WCAG 2.2 also requires that text be resizable up to 200% without loss of content or functionality under Success Criterion 1.4.4. citeturn413188search1

Do not remove native focus indicators unless a replacement remains clearly visible and accessible.

---

# 13. Responsive Design

Responsive design is a structural adaptation, not just shrinking desktop UI.

For each important screen, determine:

- What remains primary on small screens?
- What moves below the primary content?
- What becomes collapsible?
- What becomes a separate screen?
- What can disappear safely?
- What must remain visible?
- How do tables behave?
- How do dense panels stack?
- How do navigation and filtering change?

Test at realistic viewport sizes.

Do not rely on one desktop screenshot as proof of responsive quality.

---

# 14. Interaction and State Design

A production-quality interface must account for more than the happy path.

Design the states that the actual application can reach:

- Initial
- Loading
- Success
- Empty
- Error
- Partial
- Disabled
- Processing
- Unavailable
- Uncertain
- Permission-restricted, where relevant
- Offline/reconnecting, where relevant

Do not invent states that the application does not use merely to fill the design system.

Do not show fake progress percentages.

Skeletons are acceptable during loading, but they must disappear when real content is available.

---

# 15. Forms and Conversion

For forms and conversion-oriented sites, reduce friction.

The video source emphasizes clarity, scannability, motivation, and removing friction between user intent and the desired action.

Apply this contextually:

- Make the next action obvious.
- Ask only for information that is needed at that step.
- Provide useful labels.
- Validate close to the point of error.
- Preserve user input when reasonable.
- Give useful success/failure feedback.
- Avoid unnecessary steps.

For non-conversion applications, reinterpret "conversion" as successful completion of the user's intended task rather than forcing a sales model onto the UI.

Client-side validation is a usability enhancement, not a substitute for server-side validation. MDN explicitly notes this distinction. citeturn413188search2turn413188search3

---

# 16. Navigation

Navigation should reflect the product's mental model.

Do not copy the conventional sidebar merely because the product has multiple screens.

Navigation should answer:

- Where am I?
- Where can I go?
- What is the primary destination?
- How do I return?
- What context will be preserved?

The selected state should be clear but not visually noisy.

Avoid excessive navigation sections.

---

# 17. Component Architecture

Build reusable components around repeated behavior and repeated visual patterns.

Good abstraction:

> This interaction/visual structure repeats with the same responsibility.

Bad abstraction:

> This might be useful someday, so create a complex generic framework now.

Avoid both:

- Monolithic components
- Copy-pasted UI
- Premature over-abstraction

Keep component responsibilities understandable and easy to test.

---

# 18. Real Data and Dynamic Content

Connect the interface to the application's actual data sources.

Do not replace real data with static values merely to match a visual mockup.

If a reference image shows:

- a number
- a fact
- a document
- a user
- a chart
- a status
- a relationship

use the application's actual corresponding data.

The layout can stay visually faithful while the content remains dynamic.

Avoid hard-coded assignment examples and document-specific rules unless the product explicitly requires fixtures or demo mode.

---

# 19. Large Data and Long Content

Design for the actual scale the application is expected to support.

Consider:

- Long titles
- Long paragraphs
- Hundreds/thousands of records
- Missing fields
- Multiple evidence sources
- Large documents
- Slow requests
- Empty collections
- Pagination/infinite loading
- Search/filter state

Do not evaluate a list only with five short demo records.

Where large datasets exist, use appropriate rendering and data-loading strategies rather than simply squeezing more content onto the screen.

---

# 20. Performance

Performance is part of user experience.

Consider:

- Unnecessary JavaScript
- Large bundles
- Image sizes
- Font loading
- Lazy loading
- Expensive rendering
- Large lists
- Document rendering
- Network waterfalls
- Layout shifts

Current web.dev documentation identifies Largest Contentful Paint (LCP), Interaction to Next Paint (INP), and Cumulative Layout Shift (CLS) as the Core Web Vitals used to assess loading, responsiveness, and visual stability. Its documented "good" thresholds are ≤2.5s for LCP, ≤200ms for INP, and ≤0.1 for CLS, evaluated at the 75th percentile. These are performance targets, not guarantees or substitutes for product-specific profiling. citeturn413188search6

Do not optimize blindly. Measure the real application and address meaningful bottlenecks.

---

# 21. Assets, Fonts, and External Dependencies

Use project-appropriate assets and fonts.

Do not add external dependencies solely because a generated mockup used them.

Before adding a dependency, ask:

- Is it necessary?
- Does the project already provide this capability?
- What is the maintenance cost?
- What is the performance cost?
- Does it create a licensing or deployment issue?

When possible, integrate fonts and styling through the project's actual build system instead of leaving standalone CDN prototypes in the final application.

---

# 22. Visual QA Loop

Never treat "code compiles" as proof that the UI is complete.

The required loop is:

> Design → Implement → Render → Inspect → Compare → Fix → Render again.

## 22.1 Render the actual application

Inspect the actual running page, not just source code.

Check:

- Typography
- Spacing
- Alignment
- Widths/heights
- Component sizes
- Visual hierarchy
- Overflow
- Empty space
- Density
- Colors
- Borders
- Responsive behavior

## 22.2 Compare against requirements

For each important screen ask:

- Is the purpose immediately understandable?
- Is the primary information obvious?
- Is the next action obvious?
- Is the content readable?
- Is unnecessary information hidden or de-emphasized?
- Are important states represented honestly?
- Does the screen reflect actual product functionality?

## 22.3 Compare against references when provided

When a reference image exists, compare the rendered result directly.

Do not settle for "similar" if the user requested reproduction.

Fix the measurable differences that matter:

- proportions
- spacing
- typography
- alignment
- colors
- borders
- panel sizing
- composition

---

# 23. Anti-Placeholder Audit

Before completion, audit the entire application for anything fake, static, simulated, incomplete, or misleading.

Search the codebase and rendered UI for indicators such as:

- TODO
- FIXME
- placeholder
- mock
- dummy
- sample
- example
- fake
- prototype
- coming soon
- not implemented
- hard-coded
- lorem ipsum

Then manually inspect because not all placeholders are discoverable through keywords.

Audit:

- Pages
- Routes
- Components
- Modals
- Drawers
- Tabs
- Forms
- Search
- Filters
- Tables
- Document viewers
- Charts
- Relationship views
- Loading states
- Empty states
- Error states
- Mobile layouts

For each suspicious element, classify it:

A. Already real and connected.

B. Real capability exists but the UI is not connected.

C. Capability does not exist.

For B, connect it using the existing architecture.

For C, do not fake it. Remove it, clearly mark it unavailable, or implement the real capability if it is small, justified, and fits the architecture.

---

# 24. Functional Surface Audit

Every visible interactive surface must have an answer to:

> What happens when the user interacts with this?

Perform a deliberate audit of:

- Buttons
- Links
- Tabs
- Search fields
- Inputs
- Selects
- Checkboxes/radios
- Uploads
- Filters
- Sorting
- Pagination
- Accordions
- Modals
- Drawers
- Tooltips
- Navigation
- Document controls

No important control should exist solely because it makes the screenshot look complete.

---

# 25. Content and Data Realism

When a UI contains data-rich content, evaluate whether it looks and behaves like authentic application data.

Examples:

A PDF viewer should use real document content where available, not grey skeleton lines pretending to be a document.

A search result should use real search results.

A chart should use actual values or be clearly marked as an illustration/demo.

A relationship should originate from the product's actual relationship logic.

A fact should originate from the product's actual fact model.

A status should reflect actual application state.

The interface should not be more confident than the underlying data.

---

# 26. Design Review: Human-Eye Test

Before finalizing each major screen, perform a visual comprehension review.

Ask:

1. What does my eye see first?
2. Is that the right thing?
3. Can I understand the screen without reading every word?
4. Is the primary task obvious?
5. Is the page too dense?
6. Can some information be progressively disclosed?
7. Are cards, borders, badges, or colors doing unnecessary work?
8. Is there enough whitespace?
9. Is the typography readable?
10. Does the interface feel designed for the intended user rather than the developer?

If the screen feels cluttered, do not automatically add more styling. Remove, group, reorder, or progressively disclose information.

---

# 27. Design Review: Anti-Generic Test

Ask:

- Does this look like a generic template?
- Does it rely on predictable AI-dashboard conventions?
- Is every section boxed?
- Are there too many pills?
- Are there too many metrics?
- Is color compensating for weak hierarchy?
- Is there excessive decorative treatment?
- Does it resemble a specific recognizable product too closely?
- Does the visual language reflect something specific about this product?

If it looks generic, redesign the structure before merely changing colors.

---

# 28. Design Review: Product-Truth Test

Ask:

- Does every meaningful number come from real data?
- Does every meaningful fact come from real data?
- Does every source actually exist?
- Does every evidence excerpt exist?
- Does every relationship come from the real system?
- Does every state reflect actual behavior?
- Are unsupported capabilities clearly identified as unsupported?
- Does the UI make claims stronger than the underlying data supports?

If any answer is uncertain, investigate the implementation instead of guessing.

---

# 29. Decision Framework for Ambiguity

When multiple design choices are possible, use this order of reasoning:

1. User goal
2. Product capability
3. Information hierarchy
4. Accessibility
5. Simplicity
6. Consistency
7. Visual polish
8. Decorative enhancement

Do not let decoration override usability.

When a user request conflicts with existing functionality, preserve real functionality unless the user explicitly requests a functional change.

When information is missing:

- Inspect the project.
- Look for existing data/API support.
- Prefer established project conventions.
- Make the smallest reasonable assumption.
- Avoid fabricating facts.

Ask the user only when the ambiguity materially changes the product and cannot reasonably be resolved from available context.

---

# 30. Website-Specific Rules for Different Product Types

Not every website should use the same structure.

## Marketing / landing pages

Prioritize:

- Clear proposition
- Audience relevance
- Visual hierarchy
- Trust
- Scannability
- Clear next action
- Reduced friction
- Mobile performance

## SaaS / product applications

Prioritize:

- Task completion
- Navigation
- Information hierarchy
- States
- Search/filtering
- Responsive behavior
- Data integrity

## Data-heavy applications

Prioritize:

- Readability
- Density management
- Filtering
- Sorting
- Progressive disclosure
- Persistent context
- Large-data behavior

## Research / investigation applications

Prioritize:

- Evidence
- Provenance
- Context
- Comparison
- Explanation
- Uncertainty
- Traceability

## AI applications

Prioritize:

- Clear distinction between source and generated output
- Honest uncertainty
- Input/output state visibility
- Useful error handling
- Evidence where relevant
- No fabricated capabilities

Do not force one product type's interaction model onto another.

---

# 31. Development Workflow

Follow this workflow unless the project has a stronger established process.

## Phase 1 — Understand

Determine the existing product, target users, actual capabilities, important workflows, constraints, and current UI.

## Phase 2 — Plan

Identify the user's main tasks and establish information hierarchy and navigation.

## Phase 3 — Design

Choose layout, typography, color, component language, and interaction patterns based on the product.

If reference images exist, determine whether they are inspiration or exact specifications.

## Phase 4 — Implement

Build the UI using the existing architecture and real data.

For every functional HTML surface, establish its behavioral implementation in the relevant JavaScript file/module/component.

## Phase 5 — Integrate

Connect forms, navigation, data, search, filters, document/evidence views, and other interactions to actual behavior.

## Phase 6 — Validate

Run the application and test actual workflows.

## Phase 7 — Visual QA

Render important states and inspect the actual UI.

Compare against requirements and references.

## Phase 8 — Correct

Fix functionality, readability, responsiveness, accessibility, and visual issues.

## Phase 9 — Audit

Perform placeholder, dead-control, accessibility, responsive, and product-truth audits.

## Phase 10 — Finalize

Only declare completion when the implemented experience, not just the code, satisfies the quality criteria.

---

# 32. Completion Criteria

The work is complete only when all of the following are true:

## Product

- The UI reflects the actual product.
- The primary user goals are clear.
- Important workflows are understandable.

## UX

- Visual hierarchy is deliberate.
- The interface is scannable without being cramped.
- Progressive disclosure is used where appropriate.
- The primary action is distinguishable.
- Unnecessary UI has been removed.

## Visual design

- Typography is intentional.
- Color has semantic purpose.
- Contrast is sufficient.
- Visual identity is coherent.
- The design does not look like a generic AI template.
- The interface has a product-specific visual character.

## Functionality

- Real data is used.
- Important controls work.
- Navigation works.
- Forms work.
- Loading/empty/error states are handled.
- No important UI is merely decorative.
- Functional HTML has an identifiable behavior implementation.
- Relevant JavaScript files/modules exist for required functionality.

## Truthfulness

- No fabricated production data.
- No fake evidence.
- No simulated capability presented as real.
- No fake processing progress.
- Limitations are honest.

## Accessibility

- Semantic HTML is used appropriately.
- Keyboard interaction works.
- Focus states are visible.
- Labels are present.
- Contrast is checked.
- Color is not the only state indicator.

## Responsive behavior

- Desktop works.
- Tablet works.
- Mobile works.
- Layout adapts structurally rather than merely shrinking.

## QA

- The rendered application has been inspected.
- Important interactions have been tested.
- Known visual discrepancies have been corrected.
- Placeholder/dead-control audit is complete.

---

# 33. Final Agent Self-Check

Before reporting completion, answer these questions internally:

### Product

What is the user's primary task?

Can the current UI help them complete it?

### Hierarchy

What is the first thing the user sees?

Is it the correct thing?

### Cognitive load

Am I showing information merely because it exists?

Could some detail be progressively disclosed?

### Visual quality

Does the interface look intentionally designed for this product?

Or does it look like a generic generated dashboard?

### Functionality

Does every important control actually do something?

Where is the behavior implemented?

### Realism

Is every meaningful piece of displayed data real?

Am I showing fake content anywhere?

### Accessibility

Can a keyboard user operate the interface?

Is important text readable and sufficiently contrasted?

### Responsiveness

What happens on a narrow screen?

### Verification

Did I inspect the rendered application rather than only the source code?

If the answer to any critical question is no, continue iterating.

---

# 34. Source Basis and Evidence Discipline

This skill combines:

1. Principles explicitly present in the user-provided video transcript, including visual hierarchy, accessible contrast, restrained use of color, typography hierarchy, reducing friction, clarity, scannability, audience-centered design, and continuous learning.
2. Engineering/accessibility guidance from authoritative web standards/documentation.
3. Practical design heuristics developed during iterative website/UI work.

Do not present heuristics as universal laws.

When a principle comes from a heuristic rather than a formal standard, treat it as a decision aid and test it against the product context.

Authoritative references used for the engineering portions of this skill include:

- W3C Web Content Accessibility Guidelines (WCAG) 2.2: https://www.w3.org/TR/WCAG22/
- MDN — HTML: A good basis for accessibility: https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Accessibility/HTML
- MDN — Semantic HTML: https://developer.mozilla.org/en-US/curriculum/core/semantic-html/
- MDN — Forms and buttons: https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/HTML_forms
- web.dev — Core Web Vitals thresholds: https://web.dev/articles/defining-core-web-vitals-thresholds
- Nielsen Norman Group — How Users Read on the Web: https://www.nngroup.com/articles/how-users-read-on-the-web/

The video transcript provided for this skill should be treated as a source for the speaker's stated design principles, not as a universal scientific authority. In particular, the transcript itself rejects treating the F-pattern as a universal rule and emphasizes visual hierarchy instead.

---

# 35. Core Philosophy

When in doubt, return to these principles:

> Understand the user before choosing the interface.

> Design the hierarchy before decorating the page.

> Use typography, whitespace, spacing, composition, and contrast to guide attention.

> Do not show everything merely because you can.

> Scrolling is better than clutter.

> Real functionality is better than convincing simulation.

> Real evidence is better than plausible filler.

> A clear simple interface is better than an impressive confusing one.

> A distinctive product identity is better than a generic AI aesthetic.

> Accessibility is part of design.

> Every functional control needs an actual behavioral implementation.

> Render and inspect the real application before declaring the work complete.

> Do not optimize the screenshot; optimize the human experience.
