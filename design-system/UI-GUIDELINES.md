# UI Guidelines

## Navigation & information architecture
A persistent left sidebar lists the top-level sections (e.g. jobs, schedules, settings); there is no top bar, since operators spend whole sessions in one section and a sidebar keeps section-switching to a single click. Each section is a flat list or table, not nested further than one level, so operators can scan and jump without drilling through menus.

## Layout & density
Default to a data-dense layout: tables and lists over large illustrative cards, `font-size-sm`/`font-size-xs` for most in-table text, and `space-2`/`space-3` rather than `space-5`/`space-6` for internal gaps, because operators are scanning many rows of state at once, not reading long-form content. Pages do not need to adapt below ~1024px width, since this is an internal tool used on desktop monitors, not a mobile surface.

## Component usage
Use `.table` for any list of more than a handful of same-shaped records (jobs, runs, logs) since it lets operators compare fields across rows. Use `.card` to group a single entity's details or a settings section, never for repeating list items, since repeating cards waste vertical space that a table uses efficiently. Use `.chip-success`/`.chip-warning`/`.chip-danger` for job/run status and `.chip-neutral` for inactive or informational tags, so status is recognizable by color before the label is read. Use `.btn-primary` once per view for the one primary action (e.g. "Run now"); every other action is `.btn-secondary`, so operators always know the default action at a glance.

## Theme
Light theme only for now. The product is used in bright, shared office/ops environments where a dark surface would reduce the legibility operators depend on for fast scanning; revisit if remote/on-call usage grows.

## Voice & tone
Copy is short, literal, and system-status-oriented ("Run failed at 14:02", not "Oops, something went wrong"), because operators need to act on precise state, not be reassured.
