# Refresh Project

Update the project to the latest state: pull code, update ske, and validate.

## Steps

1. **Pull latest changes**
   ```bash
   git pull
   ```

2. **If not on main branch, merge main**
   ```bash
   # Check current branch
   git branch --show-current
   # If not main/master, merge it:
   git fetch origin main
   git merge origin/main
   ```

3. **Reinstall ske to get latest version**
   You must uninstall first and clean the npm cache, or npm may use a cached version:
   ```bash
   npm uninstall -g ske
   npm cache clean --force
   npm install -g https://story-assets.ianbicking.org/packages/ske/dist/memory-atlas-ske-0.0.0-dev.tgz
   ```

4. **Update project configuration files**
   ```bash
   ske init --update
   ```
   This updates skill files, instruction templates, and refreshes the database schema.

5. **Validate the project**
   ```bash
   ske validate
   ```
   This checks consistency and commits any needed changes.

## When to Use

- Starting a new session after being away
- When instructed that ske has been updated
- When encountering unexpected ske errors (updating may fix them)
- Before starting significant work to ensure you have latest content
