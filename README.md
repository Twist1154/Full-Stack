# Full-Stack Project

This repository contains both the front-end and back-end as submodules.

## Cloning the Repository

Since this project uses **Git submodules**, you need to clone it properly to ensure both the front-end and back-end are included.

### Clone with Submodules:
```bash
git clone --recurse-submodules https://github.com/your-username/Full-Stack.git
```

If you forgot to use `--recurse-submodules`, initialize and update them manually:
```bash
cd Full-Stack
git submodule update --init --recursive
```

## Keeping Submodules Updated

When pulling updates from this repository, ensure the submodules are also updated:
```bash
git pull --recurse-submodules
```
Or manually update submodules:
```bash
git submodule update --remote --merge
```

## Working with Submodules

Each submodule is its own repository. To work inside them, navigate into the submodule directory and pull changes as you would in a regular Git repository:
```bash
cd front-end
git pull origin main
cd ../back-end
git pull origin main
```

## Pushing Changes

When making changes inside a submodule, commit and push them **inside the submodule first**:
```bash
cd front-end
git add .
git commit -m "Updated front-end"
git push origin main
cd ..
```
Do the same for the back-end if needed.

After updating submodules, go back to the root repository and commit the submodule updates:
```bash
git add front-end back-end
git commit -m "Updated submodule references"
git push origin main
```

## Troubleshooting

- If a submodule does not update correctly, try syncing it:
  ```bash
  git submodule sync
  git submodule update --init --recursive
  ```
- If a submodule is stuck on an old commit, ensure you're on the correct branch:
  ```bash
  cd front-end
  git checkout main
  git pull origin main
  ```
  Do the same for `back-end`.

## License

This project is licensed under [MIT License](LICENSE).

---


This project is licensed under [Hapo-Cloud].
