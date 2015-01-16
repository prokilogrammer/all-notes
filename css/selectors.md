# Selectors

- *Right to left*: Browsers parse selectors from right to left. Keep the right most selector specific to avoid sending the browser in a wild goose chase.
- *Keep them short*: Keep selectors short. This will improve performance and reusability. For example:
    #container header nav {...} /* BAD */
    .nav-link {..} /* GOOD */
- *Classes everywhere*: They keep the code reusable. They give context and description to css.
