### Fixed

- With `GITLAB_MCP_LIST_SUMMARY_DEFAULT=true`, `list_group_iterations`,
  `list_project_iterations`, and `list_group_iteration_cadences` now keep the
  full reply when `summary` is omitted. The summary dropped `start_date` and
  `due_date` (and the cadence settings), which is what these tools are asked
  for. Passing `summary: true` still summarizes.

### Changed

- A unit test now fails when a list tool is not classified for the list
  summary (excluded, content on request, native, or summary-safe with the
  fields its summary must keep), so a new list tool gets a decision before it
  ships.
