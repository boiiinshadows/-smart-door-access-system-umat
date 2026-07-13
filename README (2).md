# Smart Door Access System — UMaT Case Study

**Course:** EL 162/234
**Instructor:** Dr. Matthew Cobbinah

## Task

The Dean of ORIC, UMaT, requested a smart door access system for admin staff. Each staff member has an access code that must be protected from direct modification.

### Requirements

- `Staff` class with:
  - Public attribute: `s_name`
  - Private attribute: `__access_code`
  - Methods to:
    - View the access code (authorized users only)
    - Update the access code after validating its length
    - Display staff information
- Uses the `@property` decorator to manage the access code instead of traditional getter/setter methods

## Files

- `staff_access_system.ipynb` — implementation and demo

## How it works

`access_code` is a private attribute (`__access_code`, name-mangled by Python to `_Staff__access_code`). It's exposed through a `@property` getter for authorized reads, and a matching `@access_code.setter` that validates the new value (type check + minimum length of 4 characters) before allowing an update.
