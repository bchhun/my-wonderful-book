---
marp: true
theme: uncover
_class: invert
---

# Automated release notes

_Conventional commits_ + _Semantic versioning_ + _Semantic&nbsp;Release_ to the rescue 💖 !

---

# Conventional Commits ?

Explicit, standardised git commit history

---

## Git commit message with a specific format

```
Type (Scope): Subject

Optional body message
```

--- 

## Git commit message examples

```
fix(website): fixed header bug under android 6
-
feat(HAD2-1981): new pilaster calculation
-
chore: add docker container section in the README
- 
feat(api): added the JWT token check

BREAKING CHANGE: the API now requires a JWT token from the frontend
```

---

But but...My devs aren't disciplined enough to use conventional commits ! 😰

![w:600](https://i.imgur.com/HGptyBE.gif)

How can I force them to use it ?

---

~~Forcefully~~ Convince them to add a **Git hook** to automagically validate the repo's commit message format 🤓

* https://github.com/craicoverflow/sailr
* https://github.com/typicode/husky

---

# Git related recommendation

* squash your commits when making merge requests/pull requests

---

# Semantic Versioning

A version number scheme that is telling us what has been modified within its underlying code

---

Here is the _Visual Studio Code_ latest version: `1.48.2`

Its numbering structure: `<Major>.<Minor>.<Patch>`

---

| Version part | What                                               | Before | After |
|--------------|----------------------------------------------------|--------|-------|
| Major        | Introduce a new **backward-incompatible** change   | 1.0.0  | 2.0.0 |
| Minor        | Introduce a new **backward-compatible** change     | 1.0.0  | 1.1.0 |
| Patch        | Fix a bug while maintaining backward-compatibility | 1.0.0  | 1.0.1 |

---

| Version part | Code manipulation examples                                     |
|--------------|----------------------------------------------------------------|
| Major        | Remove an operation, i.e. remove an HTTP verb/path combination |
|              | Add a mandatory field to a request payload                     |
| Minor        | Add an optional field to a request payload                     |
| Patch        | fixed the mobile menu                                          |

---

| Version part | Conventional commit Type                       |
|--------------|------------------------------------------------|
| Major        | *feat* with BREAKING CHANGE in the commit body |
| Minor        | *feat*                                         |
| Patch        | *fix*, *docs*, *test*, *ci*                    |

---

# Local demo time !

---

# What's next ?

* Figure out how we can use it for a dotnet/mobile project
* Figure out how we can use it within Azure Devops continuous integration 😱
