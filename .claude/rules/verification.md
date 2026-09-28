# Verification rule

Verification is evidence, not confidence. Select the strongest practical method: unit/integration test, app execution, browser check and screenshot, actual API/model request, or deployment check. Exercise the happy path and at least the most likely failure path.

Record command/action, observed outcome, environment caveats, status (PASS/FAIL/BLOCKED), and owner in `docs/verification.md`. A blocked external credential or service is not a PASS; document the fallback and demo implication.
