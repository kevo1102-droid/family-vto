# Snyder Family VTO

Private, encrypted VTO for the Snyder family.

- `index.html` — VTO editor (Kevin + Casey)
- `casey.html` — questionnaire for Casey to fill and send back

Both files are encrypted with AES-256-GCM using PBKDF2 (via [staticrypt](https://github.com/robinmoisson/staticrypt)). Content is unreadable in source until unlocked with the password.

## Password

**`snyder`** (change by re-running `npx staticrypt src/*.html -p NEWPW`)

## Editing

Plaintext sources live in `src/` (gitignored — never committed). Edit those, then re-encrypt:

```bash
npx staticrypt src/index.html src/casey.html -p snyder --short -d .
```

## Live URLs

- Editor: https://kevo1102-droid.github.io/family-vto/
- Casey's questionnaire: https://kevo1102-droid.github.io/family-vto/casey.html
