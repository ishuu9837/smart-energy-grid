# Verification — 1 October 2026

Verified the revised learning-focused website in the Codex browser through the local server.

- Desktop 1440 × 900: use-case layout and keyboard focus inspected. All four scenario controls change the setting, title, explanation, process and learning takeaway. Example titles confirmed: “When everyone switches on.”, “When the sunlight changes.”, “Notice the warning earlier.”, “A reading worth a closer look.”
- Mobile 390 × 844: navigation menu opens, section selection closes it, and adaptive-control components display correctly in a vertical flow.
- Narrow mobile 320 × 740: document width and scroll width both 320 px. Element geometry found no right-edge overflow.
- Tablet 768 × 1024: document width and scroll width both 768 px. Responsive image variants load successfully.
- Architecture: both data-pipeline and adaptive-control views work. Component selection and Enter-key activation update the detail panel. Selected state is exposed through aria-pressed.
- Simulation: defaults produce 90 MW adjusted demand, 60 MW renewable use, 30 MW conventional supply, 0 MW surplus and 10 MWh deferred energy. Demand 20 MW / renewable 200 MW / shift 30% produces 14 MW adjusted demand, zero conventional supply, 186 MW surplus and 6 MWh deferred energy. Demand 200 MW / renewable 0 MW / shift 30% produces 140 MW conventional supply and 60 MWh deferred energy. Reset returns 30 MW conventional supply.
- Expandable simulation assumptions open through the summary control.
- Anchor check: no broken section links. Visible body contains no “View presentations”, “Download PPTX”, duplicate-file note or slide attribution. Original presentation files and bibliography are outside the public web root.
- Images: all three in-page images loaded, with meaningful alt text. Hero uses its mobile crop at small widths. Original images were inspected before integration.
- Browser console: no error or warning logs observed.
- JavaScript syntax: npm run check passed after the revision.
- Reduced motion: stylesheet disables reveal transitions and smooth scrolling under prefers-reduced-motion; JavaScript also skips reveals when that preference is active. Focus-visible styles are defined for every interactive element.

No backend or live external data is part of this application. Ordinary use-case scenarios and the synthetic one-hour balance are explicitly illustrative. This is a responsive desktop-browser verification, not a test on physical phones or a formal accessibility certification.
