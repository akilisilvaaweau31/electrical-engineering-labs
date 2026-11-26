# Repository decisions

These decisions describe the GitHub setup authored on 2026-11-25. Preserve the reasoning when revising a decision; link to a later replacement instead of silently rewriting history.

## D001 — Keep the existing subject folders

**Decision:** Keep `c-programming`, `circuits`, `digital-logic`, `embedded`, `ltspice`, `pcb-design`, and `projects`.

**Reason:** The inspected repository already used these categories. New guidance can fit them without moving existing work or creating a second competing structure.

**Effect:** New projects use a descriptive subfolder inside the most appropriate category. Cross-category navigation uses links rather than duplicate copies.

## D002 — Describe the evidence precisely

**Decision:** Label analytical, synthetic, software-tested, simulated, and measured work separately.

**Reason:** Each kind of evidence supports a different claim. A calculated value or generated reference is not a measurement.

**Effect:** Templates leave unperformed stages pending. Public project claims link to actual supporting artifacts.

## D003 — Keep setup references separate from performed labs

**Decision:** Place generated analytical references under `examples/github-setup/` and reusable forms under `templates/`.

**Reason:** These files are useful starting material, but they are not evidence that the owner completed a lab.

**Effect:** A performed project gets its own folder, explanation, and actual verification record.

## D004 — Preserve rights and attribution

**Decision:** This setup does not apply a new repository license or import third-party source/model files.

**Reason:** Selecting an open-source license is a deliberate rights decision. Public visibility alone does not settle redistribution rights.

**Effect:** The new instructional text, calculations, forms, and RC reference netlist are original material created for this setup with AI assistance. Future external code, models, images, and datasets need source/rights review and attribution. A license can be selected separately for material the owner is entitled to license.

## D005 — Keep execution deliberate

**Decision:** Supply issue and pull-request templates without automatic workflows.

**Reason:** The current additions are documentation, forms, and analytical references. They do not need a background runner or new service dependency.

**Effect:** Build, simulation, and measurement instructions describe future actions; they do not imply those actions ran.

## D006 — Make the public portfolio understandable

**Decision:** Favor concise project explanations and traceable evidence over skill badges or unsupported achievement claims.

**Reason:** A reviewer should be able to identify the problem, implementation, personal contribution, result, and limitations quickly.

**Effect:** Public documentation contains technical project information. Personal planning and sensitive records stay outside public project files.
