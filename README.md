# FSSAI–NABL Integrated Dashboard

Interactive dashboard for NABL-integrated laboratories and the regulators that recognise them, with an India map drill-down, scope filters, cross-regulator recognition view and regulator-specific sign-in.

Served via GitHub Pages from the `main` branch (`index.html`).

## Sign-in (prototype)

Nine accounts exist (Admin plus one per regulator). Each regulator sees only the labs it recognises; Admin sees the full register.

Accounts are defined in the `USERS` list inside `index.html` as `{role, email, salt, hash}` where `hash = SHA-256(salt:email:password)`. To change a password, recompute the hash, e.g.:

    python3 -c "import hashlib;print(hashlib.sha256(b'SALT:email@example.org:NEWPASSWORD').hexdigest())"

Note: the check runs in the browser and the lab data is bundled in the same file, so this is a presentation-level gate, not access control. Use a server-side login before sharing data that must stay restricted.
