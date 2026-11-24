<!--
Title: type(VF-1234): imperative summary, with the ticket scope optional, for example feat(VF-1234): add a CSV export.
The squash merge uses this title and body as the commit on main, so keep the body short and factual.
-->

## Summary

<!-- What changed and why. -->

## Testing

<!-- The automated tests you added or changed, and anything you checked by hand. -->

## Deploy steps

<!-- Anything a person must do when this is deployed, such as a command, new configuration or environment variables, or a data fix. Write "None" if
there is nothing. Anything not done at deploy gets a follow-up ticket. -->

## Definition of Done

CI checks the tests, style and static analysis. Tick what it cannot check, or strike through what does not apply.

- [ ] Automated tests cover the change, including a regression test for a bug fix
- [ ] No unnecessary dependency updates
- [ ] New configuration or environment variables are documented and added to every environment
- [ ] Documentation is updated for API, architecture or domain changes
- [ ] Privacy, security or Compliance approval is in place where a trigger applies
- [ ] The PO knows about new permissions or changed behaviour
