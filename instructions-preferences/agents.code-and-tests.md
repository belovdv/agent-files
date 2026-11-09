## Code and Tests

Do not add comments that explain obvious behavior, such as "XxxBuilder builds Xxx," or repeat documentation already available elsewhere.

Avoid unit-test bloat:
- Do not write a unit test without an explicit reason.
- Do not test external functionality; check that the original project tests it.
- Keep each unit test much simpler than the code it tests. Do not test getters, configuration builders, or other boilerplate.
- Use unit tests primarily to support and document very complex isolated logic.
- Tests can simplify development and debugging. Remove temporary debugging tests afterward unless the code is expected to change frequently.
Use high-level integration tests for functional testing.
