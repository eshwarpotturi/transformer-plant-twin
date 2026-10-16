# Transformer Plant Twin

A 3D digital twin of a large power transformer factory, with an AI agent that reads plant messages, fixes small things on its own, refuses unsafe shortcuts, and asks a person before anything costly.

Proof of concept for Straive's Innovation Team. **All data is synthetic.** Figures are typical industry values, not any client's.

## Open it

`index.html` is a single file. Open it in a modern browser (Chrome or Edge). It loads three.js from a CDN, so it needs internet access.

## What it shows

- A full site: production hall (core cutting, coil winding clean room, assembly, drying ovens, tank & oil), high-voltage test lab, stores, tank fabrication, oil storage, dispatch, QC lab, workshop and more. Click any building or machine for what it does, key figures and its live status.
- 17 transformer orders moving through the plant at once, each with % complete.
- Two modes for the same 17 days (9–25 Nov 2026):
  - **Today, no agent:** a supplier delay, a failing machine and an oil shortage go unnoticed. T-07 ships 4 days late (₹1 Cr penalty), machine 4 breaks down, T-15 waits for oil.
  - **With AI agent:** the agent reads the messages and asks for 4 decisions (machine inspection, test-lab night shift, customer notice, oil order). A side-by-side table at the end compares outcomes.

## Agent rules (shown in the Agent tab)

- **Does it alone, then reports:** supplier follow-ups, reordering queues, booking cranes, moving crews.
- **Asks a person first:** overtime above ₹2 L, taking a machine offline, purchases above ₹50 L, anything sent to a customer.
- **Never allowed:** skipping or shortening a test, ending drying early, shipping a unit that failed a test.

## Next steps

- Validate layout and figures with a transformer manufacturing expert.
- Wrap in a Windows app shell (WebView2) with native approval notifications.
- Replace the scripted agent replay with live Claude calls behind the same policy engine.
