# Plan: SPSS Quote Request Tool

## Overview
Build a standalone, single-file web application (`index.html`) titled **SPSS Quote Request Tool** using pure HTML5, CSS3, and modern JavaScript without external libraries. The tool enables prospective IBM SPSS customers or sales representatives to fill in comprehensive quote details based on official IBM SPSS licensing models (Subscription & Traditional On-Premises), validate inputs, view an instant preview, and generate an Outlook-compatible `mailto:` link with Outlook Web and copy-to-clipboard fallbacks.

---

## Sub-Tasks

### Sub-Task 1: HTML Structure & IBM Carbon Dark Layout
- **Intent**: Create the complete semantic HTML skeleton containing the pricing alert banner, header, structured form sections, modal/preview card, and action controls.
- **Expected Outcomes**:
  - Full HTML5 layout with accessibility attributes (`aria-*`, `<fieldset>`, `<legend>`, `<label for="...">`).
  - Alert banner integrated directly inside the header card highlighting the January 2027 SPSS pricing update.
  - Generous card panel sub-groupings with ample padding and breathing room.
  - Grouped form fields:
    1. Customer & Contact Information (Name, Company, Work Email, Country/Region)
    2. Licensing Model & Request Type (New Purchase, Renewal, Expansion, Not Sure; Subscription, Perpetual, Fixed Term; Deployment & Billing cadences)
    3. SPSS Statistics Edition / Tier (Base, Standard, Professional, Premium, Not Sure) with detailed capability descriptors
    4. Users, Environment & Industry (User Count, Windows/macOS, Industry Sector)
    5. Specific Add-ons & Bundles Needed (Amos, Custom Tables, Advanced Stats, Forecasting, Decision Trees, Complex Samples, Missing Values, Categories, Neural Networks, Other)
    6. Additional Requirements & Comments (Timeline, IBM Customer Number, Notes)
  - Action buttons: "Generate Quote Request" (primary) and "Clear Form" (secondary).
  - Modal / feedback container with Outlook Web deep link, mailto launch, and clipboard copy action.
- **Relevant Context**: `index.html`
- **Status**: [x] done

---

### Sub-Task 2: IBM Carbon Dark Aesthetics & Visual Grouping (CSS)
- **Intent**: Design a responsive, IBM Carbon Design System-inspired dark aesthetic (`#111519` background, `#1a2028` card layer, `#222a36` sub-panels, `#2a3443` inputs/tiles, `#2b3644` borders, `#0f62fe` primary blue).
- **Expected Outcomes**:
  - Distinct nested sub-cards (`.field-card`) for each option group, preventing visual clutter and button confusion.
  - Large interactive radio tiles with distinct circular indicators, bold headers, and descriptive helper text.
  - Checkbox cards with title and feature description for clear module identification.
  - Responsive multi-column grid layout for desktop, transitioning smoothly to single-column on mobile devices.
- **Relevant Context**: Embedded `<style>` block in `index.html`
- **Status**: [x] done

---

### Sub-Task 3: Form Logic, Mailto Generator & Clipboard Handling (JavaScript)
- **Intent**: Implement client-side form validation, destination email configuration (`averywiley@ibm.com`), Outlook-compatible mailto link generation, Outlook Web shortcut, and clipboard fallback.
- **Expected Outcomes**:
  - Required field validation with focused error highlighting.
  - Dynamic extraction of selected licensing model, deployment type, operating system, and add-on products.
  - Safe URL encoding for subject (`SPSS Quote Request - [Company]`) and structured email body formatted into professional executive sections.
  - Instant `mailto:` trigger on click.
- **Relevant Context**: Embedded `<script>` block in `index.html`
- **Status**: [x] done

---

### Sub-Task 4: Verification and Browser Testing
- **Intent**: Verify layout, responsiveness, validation, and functionality across viewports and email formatting scenarios.
- **Expected Outcomes**:
  - Valid HTML5 markup and clean console output with zero errors.
  - Tested across viewports and verified data output.
- **Relevant Context**: `index.html`
- **Status**: [x] done
