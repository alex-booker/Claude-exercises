# Super Calculator

## Project overview
A beginner-friendly Angular calculator built for teaching purposes. It was originally
shipped with three methods and a set of unit tests left empty as student exercises;
those exercises have since been completed (see "Exercises" below).

## Tech stack
- Angular 19 (standalone components, no NgModule)
- TypeScript 5.7
- Karma + Jasmine for unit tests

## How to run
- Install: `npm install`
- Dev server: `npm start` → http://localhost:4200
- Tests: `npm test`

## Project structure
```
src/
└── app/
    ├── app.component.ts        ← component logic: calculator state and button handlers
    ├── app.component.html      ← template: display, button grid, theme toggle
    ├── app.component.css       ← styles, including dark/light theme rules
    └── app.component.spec.ts   ← unit tests for the component
```
Everything lives in this single standalone `AppComponent` — there is no routing or
additional feature modules.

## Exercises
The following were originally left as TODOs and are now implemented in
`app.component.ts`:
- `pressToggleSign()` — flips the sign of the displayed number.
- `pressPercent()` — divides the displayed number by 100.
- `toggleTheme()` — switches between dark mode (default) and light mode; the light-mode
  color rules live in `app.component.css` under the `.light` class selectors.

The corresponding unit tests in `app.component.spec.ts` (previously marked
`🎯 YOUR TURN` with `pending(...)`) have also been written and pass.

## Coding conventions
- Comments are written to teach: they explain *why* a step exists, aimed at someone
  learning Angular, not just experienced contributors.
- Method and variable names are descriptive and match the button labels they handle
  (e.g. `pressDigit`, `pressOperator`, `pressEquals`).
- Keep the app as a single standalone component — don't introduce NgModules, routing,
  or extra components unless the exercise being worked on calls for it.
